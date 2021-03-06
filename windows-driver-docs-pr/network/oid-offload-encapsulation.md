---
title: OID_OFFLOAD_ENCAPSULATION
author: windows-driver-content
description: This topic describes the OID_OFFLOAD_ENCAPSULATION object identifier (OID). 
ms.assetid: 8B5BE43C-1004-427A-B16D-5A2AA34C96CD
keywords:
- OID_OFFLOAD_ENCAPSULATION, WDK OIDs, WDK networking object identifiers, WDK networking OIDs
ms.author: windowsdriverdev
ms.date: 11/01/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
---

# OID_OFFLOAD_ENCAPSULATION

As a query request, overlying drivers use the OID_OFFLOAD_ENCAPSULATION OID to obtain the current task offload encapsulation settings of an underlying miniport adapter. NDIS handles this OID query for miniport drivers.

As a set request, overlying drivers use the OID_OFFLOAD_ENCAPSULATION OID to set the task offload encapsulation settings of an underlying miniport adapter. Miniport drivers that support task offload must handle this OID set request.

## Remarks

The InformationBuffer member of the [NDIS_OID_REQUEST](https://msdn.microsoft.com/library/windows/hardware/ff566710) structure contains an [NDIS_OFFLOAD_ENCAPSULATION](https://msdn.microsoft.com/library/windows/hardware/ff566702) structure.

### Miniport drivers

If a miniport driver does not support offload and this OID, the driver should return NDIS_STATUS_NOT_SUPPORTED.

Miniport drivers must use the contents of the [NDIS_OFFLOAD_ENCAPSULATION](https://msdn.microsoft.com/library/windows/hardware/ff566702) structure to update the currently reported TCP offload capabilities. After the update, the miniport driver must report the current task offload capabilities with the [NDIS_STATUS_TASK_OFFLOAD_CURRENT_CONFIG](ndis-status-task-offload-current-config.md) status indication. This status indication ensures that all of the overlying protocol drivers are updated with the new capabilities information.

This OID is used to activate activate all configured or enabled offloads, or deactivate all offloads (in other words, the hardware starts to perform the offloads). It does not provide fine control over individual offloads. [OID_TCP_OFFLOAD_PARAMETERS](oid-tcp-offload-parameters.md) is used to configure individual offloads and can also activate them. Most TCP/IP task offloads can be configured and activated with OID_TCP_OFFLOAD_PARAMETERS.

However, this OID's NDIS_OFFLOAD_ENCAPSULATION structure also covers two other encapsulation types that are not covered by OID_TCP_OFFLOAD_PARAMETERS's [NDIS_OFFLOAD_PARAMETERS](https://msdn.microsoft.com/library/windows/hardware/ff566706) structure: **NDIS_ENCAPSULATION_IEEE_802_3** and **NDIS_ENCAPSULATION_IEEE_LLC_SNAP_ROUTED**. Miniport drivers need to handle this difference in encapsulation types that are covered by the different OIDs.

If this OID is issued by the protocol driver to deactivate all offloads, the **Enabled** member of the NDIS_OFFLOAD_ENCAPSULATION member will be set to NDIS_OFFLOAD_SET_OFF.

### Setting encapsulation (protocol drivers)

Protocol drivers set OID_OFFLOAD_ENCAPSULATION after determining the system encapsulation requirements. A protocol driver can determine the capabilities of the underlying miniport adapter from the [NDIS_BIND_PARAMETERS](https://msdn.microsoft.com/library/windows/hardware/ff564832) structure or by querying [OID_TCP_OFFLOAD_CURRENT_CONFIG](oid-tcp-offload-current-config.md). The protocol driver must set an encapsulation type that the miniport adapter supports on at least one offload service.

If a miniport driver supports any offload type that supports the requested encapsulation type, the driver must return NDIS_STATUS_SUCCESS in response to a set of OID_OFFLOAD_ENCAPSULATION. Otherwise, the miniport driver should return NDIS_STATUS_INVALID_PARAMETER.

For send operations, a protocol driver can issue send requests by using only those offload types that the miniport adapter supports with the required encapsulation type. Therefore, if an OID set request of OID_OFFLOAD_ENCAPSULATION fails, the protocol driver must not use any offload settings in send requests that are directed to that miniport adapter.

For receive operations, the miniport driver must not start checksum or Internet protocol security (IPsec) offload services until after it receives an OID set request of OID_OFFLOAD_ENCAPSULATION.

### Obtaining current encapsulation settings (protocol drivers)

A protocol driver can issue an OID_OFFLOAD_ENCAPSULATION query only after setting the OID_OFFLOAD_ENCAPSULATION OID.

NDIS responds with an [NDIS_OFFLOAD_ENCAPSULATION](https://msdn.microsoft.com/library/windows/hardware/ff566702) structure that contains the current encapsulation settings.

Protocol drivers must be prepared to handle any NDIS_STATUS_Xxx failure code. If a failure occurs, the protocol driver must not attempt to perform any offload operations that are directed to the affected miniport adapter.

### See also

[NDIS_BIND_PARAMETERS](https://msdn.microsoft.com/library/windows/hardware/ff564832)  
[NDIS_OFFLOAD_ENCAPSULATION](https://msdn.microsoft.com/library/windows/hardware/ff566702)  
[NDIS_OID_REQUEST](https://msdn.microsoft.com/library/windows/hardware/ff566710)  
[NDIS_STATUS_TASK_OFFLOAD_CURRENT_CONFIG](ndis-status-task-offload-current-config.md)  
[OID_TCP_OFFLOAD_CURRENT_CONFIG](oid-tcp-offload-current-config.md)

## Requirements

| | |
| --- | --- |
| Version | Windows Vista and later |
| Header | Ntddndis.h (include Ndis.h) |

[Send comments about this topic to Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bnetvista\netvista%5D:%20OID_WWAN_DEVICE_CAPS_EX%20%20RELEASE:%20%288/8/2017%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Send comments about this topic to Microsoft")