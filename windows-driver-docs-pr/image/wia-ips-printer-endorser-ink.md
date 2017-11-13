---
title: WIA\_IPS\_PRINTER\_ENDORSER\_INK
description: The WIA\_IPS\_PRINTER\_ENDORSER\_INK property is used to report the current ink or toner status for the Imprinter/Endorser device.
MSHAttr:
- 'PreferredSiteName:MSDN'
- 'PreferredLib:/library/windows/hardware'
ms.assetid: CCD7C10A-7739-4E75-B30C-2C2E7FE90B13
keywords: ["WIA_IPS_PRINTER_ENDORSER_INK Imaging Devices"]
topic_type:
- apiref
api_name:
- WIA_IPS_PRINTER_ENDORSER_INK
api_location:
- Wiadef.h
api_type:
- HeaderDef
---

# WIA\_IPS\_PRINTER\_ENDORSER\_INK


The **WIA\_IPS\_PRINTER\_ENDORSER\_INK** property is used to report the current ink or toner status for the Imprinter/Endorser device. The property value indicates the remaining available ink, as a percentage of the total capacity. For example, a value of 50 indicates that there is half or 50% ink remaining. This property is initialized and maintained by the WIA mini-driver. This feature is available with Windows 8 and later versions of Windows.

Property Type: VT\_I4

Valid Values: WIA\_PROP\_LIST

Access Rights: Read-Write

Remarks
-------

The **WIA\_IPS\_PRINTER\_ENDORSER\_INK** property is optional for the Imprinter/Endorser items. The valid values for this property are between 0 and 100, inclusive.

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

 

 

[Send comments about this topic to Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bimage\image%5D:%20WIA_IPS_PRINTER_ENDORSER_INK%20%20RELEASE:%20%2811/13/2017%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Send comments about this topic to Microsoft")



