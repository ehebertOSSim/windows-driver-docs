---
title: MaxValue element
description: The required MaxValue element specifies the maximum value that the scan device supports for scanner configuration elements that require a range of values.
ms.assetid: a01833ff-06cd-47d3-9f54-2f1cf01cc1e6
keywords: ["MaxValue element Imaging Devices"]
topic_type:
- apiref
api_name:
- wscn MaxValue
api_type:
- Schema
ms.author: windowsdriverdev
ms.date: 11/28/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
---

# MaxValue element


The required **MaxValue** element specifies the maximum value that the scan device supports for scanner configuration elements that require a range of values.

Usage
-----

``` syntax
<wscn:MaxValue>
  text
</wscn:MaxValue>
```

Attributes
----------

There are no attributes.

Text value
----------

Required. For possible values, see the specific parent element.

## Child elements


There are no child elements.

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
<td><p>[<strong>CompressionQualityFactorSupported</strong>](compressionqualityfactorsupported.md)</p></td>
</tr>
<tr class="even">
<td><p>[<strong>ScalingHeight</strong>](scalingheight2.md)</p></td>
</tr>
<tr class="odd">
<td><p>[<strong>ScalingWidth</strong>](scalingwidth2.md)</p></td>
</tr>
</tbody>
</table>

Remarks
-------

The value of the **MaxValue** element depends on its parent element. For the possible values, see the appropriate parent element.

## <span id="see_also"></span>See also


[**CompressionQualityFactorSupported**](compressionqualityfactorsupported.md)

[**MinValue**](minvalue.md)

[**ScalingHeight**](scalingheight2.md)

[**ScalingWidth**](scalingwidth2.md)

 

 

[Send comments about this topic to Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bimage\image%5D:%20MaxValue%20element%20%20RELEASE:%20%2811/8/2017%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Send comments about this topic to Microsoft")





