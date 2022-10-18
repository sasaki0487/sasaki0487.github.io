---
title: Windows Ksproperty 使用方法
date: 2022-10-18
draft: false
slug: windows-ksproperty
image: ksproperty.png
categories:
    - 程式
---

KsProperty 可以用來讀寫相機的屬性，像是亮度、彩度、或是相機自定義的 extension unit 等  
MSDN 上的簡介在此  
[IKsControl：：KsProperty (ks.h) - Windows drivers | Microsoft Learn](https://learn.microsoft.com/zh-tw/windows-hardware/drivers/ddi/ks/nf-ks-ikscontrol-ksproperty)

從他的描述來看或許會有點誤導，下面是它的實際呼叫法，以讀取亮度為例。

```c++
HRESULT hr = S_OK;
KSPROPERTY_VIDEOPROCAMP_S kspIn = {0}
KSPROPERTY_VIDEOPROCAMP_S kspOut = {0}
ULONG valueSize = 0;
kspIn.Property.Set    = PROPSETID_VIDCAP_VIDEOPROCAMP;
kspIn.Property.Id     = KSPROPERTY_VIDEOPROCAMP_BRIGHTNESS;
kspIn.Property.Flags  = KSPROPERTY_TYPE_GET;
kspOut.Property.Set   = PROPSETID_VIDCAP_VIDEOPROCAMP;
kspOut.Property.Id    = KSPROPERTY_VIDEOPROCAMP_BRIGHTNESS;
kspOut.Property.Flags = KSPROPERTY_TYPE_GET;

hr = m_spIkscontrol->KsProperty(
    (PKSPROPERTY)&kspIn, sizeof(kspin),
    &kspOut, sizeof(kspout), &valueSize);
)

// 如果正確執行就可以從kspOut.Value取出值，須注意變數型態的轉換。
if(hr == S_OK){
    INT brightnessValue = (INT)kspOut.Value;
}
```
