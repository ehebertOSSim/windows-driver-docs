---
title: WIA\_DPS\_VERTICAL\_BED\_SIZE
description: The WIA\_DPS\_VERTICAL\_BED\_SIZE property contains the physical vertical dimensions of a scanner's flatbed, in thousandths of an inch (.001). The WIA minidriver creates and maintains this property.
MS-HAID:
- 'WIA\_PropTable\_3f6fbe9c-7f09-4760-b6b1-cf2c48c73040.xml'
- 'image.wia\_dps\_vertical\_bed\_size'
MSHAttr:
- 'PreferredSiteName:MSDN'
- 'PreferredLib:/library/windows/hardware'
ms.assetid: c4e02364-4785-45f4-8e43-056582bb6d1a
keywords: ["WIA_DPS_VERTICAL_BED_SIZE Imaging Devices"]
topic_type:
- apiref
api_name:
- WIA_DPS_VERTICAL_BED_SIZE
api_location:
- Wiadef.h
api_type:
- HeaderDef
---

# WIA\_DPS\_VERTICAL\_BED\_SIZE


The WIA\_DPS\_VERTICAL\_BED\_SIZE property contains the physical vertical dimensions of a scanner's flatbed, in thousandths of an inch (.001). The WIA minidriver creates and maintains this property.

## <span id="ddk_wia_dps_vertical_bed_size_si"></span><span id="DDK_WIA_DPS_VERTICAL_BED_SIZE_SI"></span>


Property Type: VT\_I4

Valid Values: WIA\_PROP\_NONE

Access Rights: Read-only

Requirements
------------

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Version</p></td>
<td><p>Beginning with Windows Vista, the WIA_DPS_VERTICAL_BED_SIZE property is still available at the root level of the WIA driver. But this property has been replaced with the WIA_IPS_MAX_VERTICAL_SIZE property, and you should consider it to be optional.</p></td>
</tr>
<tr class="even">
<td><p>Header</p></td>
<td>Wiadef.h (include Wiadef.h)</td>
</tr>
</tbody>
</table>

## <span id="see_also"></span>See also


[**WIA\_DPS\_HORIZONTAL\_BED\_SIZE**](wia-dps-horizontal-bed-size.md)

[**WIA\_IPS\_MAX\_VERTICAL\_SIZE**](wia-ips-max-vertical-size.md)

 

 

[Send comments about this topic to Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bimage\image%5D:%20WIA_DPS_VERTICAL_BED_SIZE%20%20RELEASE:%20%2811/13/2017%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Send comments about this topic to Microsoft")




