---
title: AVC\_FUNCTION\_CLR\_CONNECTINFO
description: AVC\_FUNCTION\_CLR\_CONNECTINFO
MS-HAID:
- 'avcref\_ca496369-e11b-4789-8527-633f013fa0e8.xml'
- 'stream.avc\_function\_clr\_connectinfo'
MSHAttr:
- 'PreferredSiteName:MSDN'
- 'PreferredLib:/library/windows/hardware'
ms.assetid: 035555c7-4668-4eda-aed1-44b2b5794ff5
keywords: ["AVC_FUNCTION_CLR_CONNECTINFO Streaming Media Devices"]
topic_type:
- apiref
api_name:
- AVC_FUNCTION_CLR_CONNECTINFO
api_type:
- NA
---

# AVC\_FUNCTION\_CLR\_CONNECTINFO


## <span id="ddk_avc_function_clr_connectinfo_ks"></span><span id="DDK_AVC_FUNCTION_CLR_CONNECTINFO_KS"></span>


The AVC\_FUNCTION\_CLR\_CONNECT\_INFO function code causes *avc.sys* to remove any cached AVCCONNECTINFO values.

### <span id="i_o_status_block"></span><span id="I_O_STATUS_BLOCK"></span>I/O Status Block

If successful, the AV/C protocol driver sets **Irp-&gt;IoStatus.Status** to STATUS\_SUCCESS.

Possible other return values include:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Return Value</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>STATUS_TIMEOUT</p></td>
<td><p>The request was made, but no response was received before all time-out and retry processing was complete.</p></td>
</tr>
<tr class="even">
<td><p>STATUS_REQUEST_ABORTED</p></td>
<td><p>Immediately abort when the IRP completion status is STATUS_REQUEST_ABORTED. This indicates that the device has been removed or is no longer available on the 1394 bus.</p></td>
</tr>
<tr class="odd">
<td><p>STATUS_*</p></td>
<td><p>Any other return code indicates that an error or warning occurred that was beyond the scope of the AV/C protocol.</p></td>
</tr>
</tbody>
</table>

 

### <span id="comments"></span><span id="COMMENTS"></span>Comments

This function uses the **PinId** member of the AVC\_MULTIFUNC\_IRB structure as shown below.

```
typedef struct _AVC_MULTIFUNC_IRB {
  AVC_IRB  Common;
  union {
    .
    .
    .
    AVC_PIN_ID PinId;
 .
    .
    .
  };
} AVC_MULTIFUNC_IRB, *PAVC_MULTIFUNC_IRB;
```

### <span id="requirements"></span><span id="REQUIREMENTS"></span>Requirements

**Headers:** Declared in *avc.h*. Include *avc.h*.

### <span id="avc_multifunc_irb_input"></span><span id="AVC_MULTIFUNC_IRB_INPUT"></span>AVC\_MULTIFUNC\_IRB Input

<span id="Common"></span><span id="common"></span><span id="COMMON"></span>**Common**  
The **Function** submember of this member must be set to **AVC\_FUNCTION\_CLR\_CONNECTINFO** from the AVC\_FUNCTION enumeration.

<span id="PinId"></span><span id="pinid"></span><span id="PINID"></span>**PinId**  
Specifies the offset (or ID) of the pin for which a connection is to be released.

This function code is not supported by virtual instances of *avc.sys*.

A subunit driver must use this function when the plug connections should no longer be made, even if the pin becomes "active" again.

This must be called at IRQL = PASSIVE\_LEVEL.

### <span id="see_also"></span><span id="SEE_ALSO"></span>See Also

[**AVC\_MULTIFUNC\_IRB**](https://msdn.microsoft.com/library/windows/hardware/ff554177), [**AVC\_PIN\_ID**](https://msdn.microsoft.com/library/windows/hardware/ff554187), [**AVC\_FUNCTION**](https://msdn.microsoft.com/library/windows/hardware/ff554145)

 

 

[Send comments about this topic to Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bstream\stream%5D:%20AVC_FUNCTION_CLR_CONNECTINFO%20%20RELEASE:%20%2811/22/2017%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Send comments about this topic to Microsoft")



