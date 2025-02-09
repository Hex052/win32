---
description: The OAHWND data type defines a window handle that can be used by OLE Automation clients, such as Microsoft Visual Basic 6.0.
ms.assetid: 80194b19-9c24-48f5-aca6-6ab33bd88c90
title: OAHWND (Control.h)
ms.topic: reference
ms.date: 4/26/2023
ms.custom: UpdateFrequency5
---

# OAHWND

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer) and [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine). **MediaPlayer** and **IMFMediaEngine** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** and **IMFMediaEngine** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The `OAHWND` data type defines a window handle that can be used by OLE Automation clients, such as Microsoft Visual Basic 6.0.


```C++
typedef LONG_PTR OAHWND;
```



## Requirements



| Requirement | Value |
|-------------------|--------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Control.h (include Dshow.h)</dt> </dl> |



## See also

<dl> <dt>

[DirectShow Data Types](directshow-data-types.md)
</dt> <dt>

[**IMediaEventEx::SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow)
</dt> <dt>

[**IVideoWindow Interface**](/windows/desktop/api/Control/nn-control-ivideowindow)
</dt> </dl>

 

 




