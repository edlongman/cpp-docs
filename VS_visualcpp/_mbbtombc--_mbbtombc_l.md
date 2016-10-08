---
title: "_mbbtombc, _mbbtombc_l"
ms.custom: na
ms.date: 10/04/2016
ms.devlang: 
  - C++
  - C
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
apiname: 
  - _mbbtombc_l
  - _mbbtombc
apilocation: 
  - msvcrt.dll
  - msvcr80.dll
  - msvcr90.dll
  - msvcr100.dll
  - msvcr100_clr0400.dll
  - msvcr110.dll
  - msvcr110_clr0400.dll
  - msvcr120.dll
  - msvcr120_clr0400.dll
  - ucrtbase.dll
  - api-ms-win-crt-multibyte-l1-1-0.dll
apitype: DLLExport
ms.assetid: 78593389-b0fc-43b6-8c1f-2a6bf702d64e
caps.latest.revision: 19
manager: ghogen
translation.priority.ht: 
  - cs-cz
  - de-de
  - es-es
  - fr-fr
  - it-it
  - ja-jp
  - ko-kr
  - pl-pl
  - pt-br
  - ru-ru
  - tr-tr
  - zh-cn
  - zh-tw
---
# _mbbtombc, _mbbtombc_l
Converts a single-byte multibyte character to a corresponding double-byte multibyte character.  
  
> [!IMPORTANT]
>  This API cannot be used in applications that execute in the Windows Runtime. For more information, see [CRT functions not supported with /ZW](http://msdn.microsoft.com/library/windows/apps/jj606124.aspx).  
  
## Syntax  
  
```  
unsigned int _mbbtombc(  
   unsigned int c   
);  
unsigned int _mbbtombc_l(  
   unsigned int c,  
   _locale_t locale  
);  
```  
  
#### Parameters  
 `c`  
 Single-byte character to convert.  
  
 `locale`  
 Locale to use.  
  
## Return Value  
 If `_mbbtombc` successfully converts `c`, it returns a multibyte character; otherwise, it returns `c`.  
  
## Remarks  
 The `_mbbtombc` function converts a given single-byte multibyte character to a corresponding double-byte multibyte character. Characters must be within the range 0x20 – 0x7E or 0xA1 – 0xDF to be converted.  
  
 The output value is affected by the setting of the `LC_CTYPE` category setting of the locale; see [setlocale, _wsetlocale](../VS_visualcpp/setlocale--_wsetlocale.md) for more information. The versions of this function are identical, except that `_mbbtombc` uses the current locale for this locale-dependent behavior and `_mbbtombc_l` instead uses the locale parameter that's passed in. For more information, see [Locale](../VS_visualcpp/Locale.md).  
  
 In earlier versions, `_mbbtombc` was named `hantozen`. For new code, use `_mbbtombc`.  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_mbbtombc`|<mbstring.h>|  
|`_mbbtombc_l`|<mbstring.h>|  
  
 For more compatibility information, see [Compatibility](../VS_visualcpp/Compatibility.md).  
  
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](../Topic/Platform%20Invoke%20Examples.md).  
  
## See Also  
 [Data Conversion](../VS_visualcpp/Data-Conversion.md)   
 [_mbctombb, _mbctombb_l](../VS_visualcpp/_mbctombb--_mbctombb_l.md)