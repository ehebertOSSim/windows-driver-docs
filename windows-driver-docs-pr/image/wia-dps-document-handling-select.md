---
title: WIA\_DPS\_DOCUMENT\_HANDLING\_SELECT
description: The WIA\_DPS\_DOCUMENT\_HANDLING\_SELECT property contains the current scanner acquisition source and mode.
MS-HAID:
- 'WIA\_PropTable\_735f913e-3c4e-44c9-9e3b-05a58e2410d1.xml'
- 'image.wia\_dps\_document\_handling\_select'
MSHAttr:
- 'PreferredSiteName:MSDN'
- 'PreferredLib:/library/windows/hardware'
ms.assetid: 17964dc5-8008-4f9c-abcd-cc72c1d6c398
keywords: ["WIA_DPS_DOCUMENT_HANDLING_SELECT Imaging Devices"]
topic_type:
- apiref
api_name:
- WIA_DPS_DOCUMENT_HANDLING_SELECT
api_location:
- Wiadef.h
api_type:
- HeaderDef
---

# WIA\_DPS\_DOCUMENT\_HANDLING\_SELECT


The WIA\_DPS\_DOCUMENT\_HANDLING\_SELECT property contains the current scanner acquisition source and mode.

## <span id="ddk_wia_dps_document_handling_select_si"></span><span id="DDK_WIA_DPS_DOCUMENT_HANDLING_SELECT_SI"></span>


Property Type: VT\_I4

Valid Values: WIA\_PROP\_FLAG

Access Rights: Read/write

Remarks
-------

An application reads the WIA\_DPS\_DOCUMENT\_HANDLING\_SELECT property to determine the current acquisition source of a scanner, or an application write this property to set the source and mode of the scanner. In addition, applications use this property to enable and disable duplexer functionality. The WIA minidriver creates and maintains this property.

The following table describes the constants that are valid with WIA\_DPS\_DOCUMENT\_HANDLING\_SELECT.

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
<td><p>BACK_FIRST</p></td>
<td><p>Scan the back of the document first. This value is valid only when DUPLEX is set.</p></td>
</tr>
<tr class="even">
<td><p>BACK_ONLY</p></td>
<td><p>Scan the back <em>only</em>. This value is valid only when DUPLEX is set.</p></td>
</tr>
<tr class="odd">
<td><p>DUPLEX</p></td>
<td><p>Scan by using duplexer operations.</p></td>
</tr>
<tr class="even">
<td><p>FRONT_FIRST</p></td>
<td><p>Scan the front of the document first. This value is valid only when DUPLEX is set.</p></td>
</tr>
<tr class="odd">
<td><p>FRONT_ONLY</p></td>
<td><p>Scan the front <em>only</em>.</p></td>
</tr>
</tbody>
</table>

 

The values DUPLEX and FRONT\_ONLY are mutually exclusive--set one or the other, but not both.

The following table describes the constants that are valid with this property with Microsoft Windows XP but are obsolete with Windows Vista and later.

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
<td><p>AUTO_ADVANCE</p></td>
<td><p>Enable automatic feeding of the next document after a scan.</p></td>
</tr>
<tr class="even">
<td><p>FEEDER</p></td>
<td><p>Scan by using the document feeder.</p></td>
</tr>
<tr class="odd">
<td><p>FLATBED</p></td>
<td><p>Scan by using the flatbed.</p></td>
</tr>
<tr class="even">
<td><p>NEXT_PAGE</p></td>
<td><p>Scan the next page of the document.</p></td>
</tr>
<tr class="odd">
<td><p>PREFEED</p></td>
<td><p>Enable pre-feed mode. Preposition the next document while scanning.</p></td>
</tr>
</tbody>
</table>

 

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
<td><p>Available for Microsoft Windows XP. For Windows Vista and later, use the WIA_IPS_DOCUMENT_HANDLING_SELECT property.</p></td>
</tr>
<tr class="even">
<td><p>Header</p></td>
<td>Wiadef.h (include Wiadef.h)</td>
</tr>
</tbody>
</table>

## <span id="see_also"></span>See also


[**WIA\_IPS\_DOCUMENT\_HANDLING\_SELECT**](wia-ips-document-handling-select.md)

 

 

[Send comments about this topic to Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bimage\image%5D:%20WIA_DPS_DOCUMENT_HANDLING_SELECT%20%20RELEASE:%20%2811/13/2017%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Send comments about this topic to Microsoft")




