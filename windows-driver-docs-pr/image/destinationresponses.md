---
title: DestinationResponses element
description: The required DestinationResponses element is a collection of all of the responses to a client's scan destination requests.
MS-HAID:
- 'wsdss\_events\_c33cbebb-f9f0-46fe-806e-228ca0283fd2.xml'
- 'image.destinationresponses'
MSHAttr:
- 'PreferredSiteName:MSDN'
- 'PreferredLib:/library/windows/hardware'
ms.assetid: f373b584-eec9-412e-80b2-3d8a69f4b7ca
keywords: ["DestinationResponses element Imaging Devices"]
topic_type:
- apiref
api_name:
- wscn DestinationResponses
api_type:
- Schema
---

# DestinationResponses element


The required **DestinationResponses** element is a collection of all of the responses to a client's scan destination requests.

Usage
-----

``` syntax
<wscn:DestinationResponses>
  child elements
</wscn:DestinationResponses>
```

Attributes
----------

There are no attributes.

## Child elements


<table>
<colgroup>
<col width="100%" />
</colgroup>
<thead>
<tr class="header">
<th>Element</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>[<strong>DestinationResponse</strong>](destinationresponse.md)</p></td>
</tr>
</tbody>
</table>

## Parent elements


<table>
<colgroup>
<col width="100%" />
</colgroup>
<thead>
<tr class="header">
<th>Element</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>&lt;wse:SubscribeResponse&gt;</p></td>
</tr>
</tbody>
</table>

Remarks
-------

A WSD Scan Service must specify one [**DestinationResponse**](destinationresponse.md) child element in a **DestinationResponses** element for each [**ScanDestination**](scandestination.md) element that a client specifies in a **&lt;wse:Subscribe&gt;** request. The **&lt;wse:Subscribe&gt;** element is described in the specification.

## <span id="see_also"></span>See also


[**DestinationResponse**](destinationresponse.md)

[**ScanDestination**](scandestination.md)

 

 

[Send comments about this topic to Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bimage\image%5D:%20DestinationResponses%20element%20%20RELEASE:%20%2811/8/2017%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Send comments about this topic to Microsoft")




