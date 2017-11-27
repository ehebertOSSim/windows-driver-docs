---
title: KSPROPERTY\_CROSSBAR\_CAN\_ROUTE
description: The KSPROPERTY\_CROSSBAR\_CAN\_ROUTE property retrieves whether the device is capable of supporting a specified routing. This property must be implemented.
MS-HAID:
- 'vidcapprop\_0b0c9276-2455-4b07-a726-a624afe9a80b.xml'
- 'stream.ksproperty\_crossbar\_can\_route'
MSHAttr:
- 'PreferredSiteName:MSDN'
- 'PreferredLib:/library/windows/hardware'
ms.assetid: bb966d0a-6ecf-4bbb-a881-30d468abe220
keywords: ["KSPROPERTY_CROSSBAR_CAN_ROUTE Streaming Media Devices"]
topic_type:
- apiref
api_name:
- KSPROPERTY_CROSSBAR_CAN_ROUTE
api_location:
- Ksmedia.h
api_type:
- HeaderDef
---

# KSPROPERTY\_CROSSBAR\_CAN\_ROUTE


The KSPROPERTY\_CROSSBAR\_CAN\_ROUTE property retrieves whether the device is capable of supporting a specified routing. This property must be implemented.

## <span id="ddk_ksproperty_crossbar_can_route_ks"></span><span id="DDK_KSPROPERTY_CROSSBAR_CAN_ROUTE_KS"></span>


### <span id="Usage_Summary_Table"></span><span id="usage_summary_table"></span><span id="USAGE_SUMMARY_TABLE"></span>Usage Summary Table

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th>Get</th>
<th>Set</th>
<th>Target</th>
<th>Property descriptor type</th>
<th>Property value type</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Yes</p></td>
<td><p>No</p></td>
<td><p>Filter</p></td>
<td><p>[<strong>KSPROPERTY_CROSSBAR_ROUTE_S</strong>](https://msdn.microsoft.com/library/windows/hardware/ff565128)</p></td>
<td><p>ULONG</p></td>
</tr>
</tbody>
</table>

 

The property value (operation data) is a ULONG that specifies whether the streaming minidriver supports a specified routing between the two pins. A nonzero value indicates that routing is supported. If the minidriver does not support routing between the two pins, this value is zero.

Remarks
-------

The **CanRoute** member of the KSPROPERTY\_CROSSBAR\_ROUTE\_S structure indicates if the device is capable of supporting a specified routing.

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
<td>Ksmedia.h (include Ksmedia.h)</td>
</tr>
</tbody>
</table>

## <span id="see_also"></span>See also


[**KSPROPERTY**](https://msdn.microsoft.com/library/windows/hardware/ff564262)

[**KSPROPERTY\_CROSSBAR\_ROUTE\_S**](https://msdn.microsoft.com/library/windows/hardware/ff565128)

 

 

[Send comments about this topic to Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bstream\stream%5D:%20KSPROPERTY_CROSSBAR_CAN_ROUTE%20%20RELEASE:%20%2811/22/2017%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Send comments about this topic to Microsoft")




