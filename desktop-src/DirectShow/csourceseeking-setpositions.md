---
description: CSourceSeeking.SetPositions method - The SetPositions method sets the current position and the stop position. This method implements the IMediaSeeking::SetPositions method.
ms.assetid: 4359fe1f-f922-4a4d-beaa-8e13c72f407c
title: CSourceSeeking.SetPositions method (Ctlutil.h)
ms.topic: reference
ms.date: 4/26/2023
topic_type: 
- APIRef
- kbSyntax
api_name: 
- CSourceSeeking.SetPositions
api_type: 
- COM
api_location: 
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.custom: UpdateFrequency5
---

# CSourceSeeking.SetPositions method

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer) and [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine). **MediaPlayer** and **IMFMediaEngine** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** and **IMFMediaEngine** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The `SetPositions` method sets the current position and the stop position. This method implements the [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) method.

## Syntax


```C++
HRESULT SetPositions(
   LONGLONG *pCurrent,
   DWORD    CurrentFlags,
   LONGLONG *pStop,
   DWORD    StopFlags
);
```



## Parameters

<dl> <dt>

*pCurrent* 
</dt> <dd>

Pointer to a variable that specifies the current position.

</dd> <dt>

*CurrentFlags* 
</dt> <dd>

Bitwise combination of flags. See Remarks.

</dd> <dt>

*pStop* 
</dt> <dd>

Pointer to a variable that specifies the stop time, in units of the current time format.

</dd> <dt>

*StopFlags* 
</dt> <dd>

Bitwise combination of flags. See Remarks.

</dd> </dl>

## Return value

Returns an **HRESULT** value. Possible values include those listed in the following table.



| Return code                                                                                  | Description                          |
|----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**S\_OK**</dt> </dl>         | Success<br/>                   |
| <dl> <dt>**E\_INVALIDARG**</dt> </dl> | Invalid flags<br/>             |
| <dl> <dt>**E\_POINTER**</dt> </dl>    | **NULL** pointer argument<br/> |



 

## Remarks

The following flags are supported:

-   AM\_SEEKING\_NoPositioning
-   AM\_SEEKING\_AbsolutePositioning
-   AM\_SEEKING\_RelativePositioning
-   AM\_SEEKING\_IncrementalPositioning (*pStop* only)

For more information, see [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions).

This method updates the values of the [**CSourceSeeking::m\_rtStart**](csourceseeking-m-rtstart.md) and [**CSourceSeeking::m\_rtStop**](csourceseeking-m-rtstop.md) member variables, and then calls the pure virtual methods [**CSourceSeeking::ChangeStart**](csourceseeking-changestart.md) and [**CSourceSeeking::ChangeStop**](csourceseeking-changestop.md).

## Requirements



| Requirement | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Library<br/> | <dl> <dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt> </dl> |



## See also

<dl> <dt>

[**CSourceSeeking Class**](csourceseeking.md)
</dt> </dl>

 

 




