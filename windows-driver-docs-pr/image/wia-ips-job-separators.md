---
title: WIA\_IPS\_JOB\_SEPARATORS
description: The WIA\_IPS\_JOB\_SEPARATORS property is used to enable the detection of job separators, and to configure the action that the device executes when it detects a job separator page. The WIA minidriver creates and maintains this property.
ms.assetid: 2ECD88EB-2B6F-477D-8F37-D4EECA580FAE
keywords: ["WIA_IPS_JOB_SEPARATORS Imaging Devices"]
topic_type:
- apiref
api_name:
- WIA_IPS_JOB_SEPARATORS
api_location:
- Wiadef.h
api_type:
- HeaderDef
ms.author: windowsdriverdev
ms.date: 11/28/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
---

# WIA\_IPS\_JOB\_SEPARATORS


The **WIA\_IPS\_JOB\_SEPARATORS** property is used to enable the detection of job separators, and to configure the action that the device executes when it detects a job separator page. The WIA minidriver creates and maintains this property.

## <span id="ddk_wia_ipa_depth_si"></span><span id="DDK_WIA_IPA_DEPTH_SI"></span>


Property Type: VT\_I4

Valid Values: WIA\_PROP\_LIST

Access Rights: Read/Write

Remarks
-------

The following table describes the valid values for the **WIA\_IPS\_JOB\_SEPARATORS** property.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Value</th>
<th>Definition</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>WIA_SEPARATOR_DISABLED</p></td>
<td><p>Job separators detection is disabled. This is the required default value if the property is supported.</p></td>
</tr>
<tr class="even">
<td><p>WIA_SEPARATOR_DETECT_SCAN_CONTINUE</p></td>
<td><p>Detect job separator page, scan the separator page, and continue scanning.</p></td>
</tr>
<tr class="odd">
<td><p>WIA_SEPARATOR_DETECT_SCAN_STOP</p></td>
<td><p>Detect job separator page, scan the separator page, and stop scanning.</p></td>
</tr>
<tr class="even">
<td><p>WIA_SEPARATOR_DETECT_NOSCAN_CONTINUE</p></td>
<td><p>Detect job separator page, do not scan (skip) the separator page, and continue scanning.</p></td>
</tr>
<tr class="odd">
<td><p>WIA_SEPARATOR_DETECT_NOSCAN_STOP</p></td>
<td><p>Detect job separator page, do not scan (skip) the separator page, and stop scanning.</p></td>
</tr>
</tbody>
</table>

 

This property is optional, and is valid only for the Feeder data source item (represented in the [**WIA\_IPA\_ITEM\_CATEGORY**](wia-ipa-item-category.md) property as WIA\_CATEGORY\_FEEDER).

Requirements
------------

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Header</p></td>
<td>Wiadef.h (include Wiadef.h)</td>
</tr>
</tbody>
</table>

 

 

[Send comments about this topic to Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bimage\image%5D:%20WIA_IPS_JOB_SEPARATORS%20%20RELEASE:%20%2811/13/2017%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Send comments about this topic to Microsoft")




