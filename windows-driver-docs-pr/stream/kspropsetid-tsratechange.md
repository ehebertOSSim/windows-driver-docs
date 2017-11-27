---
title: KSPROPSETID\_TSRateChange
description: KSPROPSETID\_TSRateChange
MS-HAID:
- 'dvdref\_cb02f058-790c-4fb0-a827-c857c7f66a30.xml'
- 'stream.kspropsetid\_tsratechange'
MSHAttr:
- 'PreferredSiteName:MSDN'
- 'PreferredLib:/library/windows/hardware'
ms.assetid: bd2855e5-dd90-4ae3-a96e-e2163e94c7d6
---

# KSPROPSETID\_TSRateChange


## <span id="ddk_kspropsetid_tsratechange_ks"></span><span id="DDK_KSPROPSETID_TSRATECHANGE_KS"></span>


The KSPROPSETID\_TSRateChange property set defines properties to control time stamp rate changes. This property set can be used to implement fast-forward and rewind capabilities.

The KS\_AM\_PROPERTY\_TS\_RATE\_CHANGE enumeration in *Ksmedia.h* specifies the properties of this set.

Minidrivers can use KSPROPSETID\_TSRateChange for any MPEG2 stream, not just DVDs.

The following properties are defined:

[**KS\_AM\_RATE\_SimpleRateChange**](ks-am-rate-simpleratechange.md)

[**KS\_AM\_RATE\_ExactRateChange**](ks-am-rate-exactratechange.md)

[**KS\_AM\_RATE\_MaxFullDataRate**](ks-am-rate-maxfulldatarate.md)

[**KS\_AM\_RATE\_Step**](ks-am-rate-step.md)

 

 

[Send comments about this topic to Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bstream\stream%5D:%20KSPROPSETID_TSRateChange%20%20RELEASE:%20%2811/22/2017%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Send comments about this topic to Microsoft")



