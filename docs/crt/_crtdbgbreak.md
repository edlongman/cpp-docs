---
title: "_CrtDbgBreak"
ms.custom: na
ms.date: "10/14/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: na
ms.topic: "article"
apiname: 
  - "_CrtDbgBreak"
apilocation: 
  - "msvcrt.dll"
  - "msvcr80.dll"
  - "msvcr90.dll"
  - "msvcr100.dll"
  - "msvcr100_clr0400.dll"
  - "msvcr110.dll"
  - "msvcr110_clr0400.dll"
  - "msvcr120.dll"
  - "msvcr120_clr0400.dll"
  - "ucrtbase.dll"
apitype: "DLLExport"
f1_keywords: 
  - "_CrtDbgBreak"
  - "CrtDbgBreak"
dev_langs: 
  - "C++"
  - "C"
helpviewer_keywords: 
  - "CrtDbgBreak function"
  - "_CrtDbgBreak function"
ms.assetid: 01f8b4a2-a2c7-4e1f-9f39-e573b4a7871f
caps.latest.revision: 12
ms.author: "corob"
manager: "ghogen"
translation.priority.ht: 
  - "cs-cz"
  - "de-de"
  - "es-es"
  - "fr-fr"
  - "it-it"
  - "ja-jp"
  - "ko-kr"
  - "pl-pl"
  - "pt-br"
  - "ru-ru"
  - "tr-tr"
  - "zh-cn"
  - "zh-tw"
---
# _CrtDbgBreak
Sets a break point on a particular line of code. (Used in debug mode only.)  
  
## Syntax  
  
```  
void _CrtDbgBreak( void );  
```  
  
## Return Value  
 There is no return value.  
  
## Remarks  
 The `_CrtDbgBreak` function sets a debug breakpoint on the particular line of code where the function resides. This function is used in debug mode only and is dependent on `_DEBUG` being previously defined.  
  
 For more information about using other hook-capable run-time functions and writing your own client-defined hook functions, see [Writing Your Own Debug Hook Functions](../Topic/Debug%20Hook%20Function%20Writing.md).  
  
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](../Topic/Platform%20Invoke%20Examples.md).  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_CrtDbgBreak`|\<CRTDBG.h>|  
  
## Libraries  
 Debug versions of [C run-time libraries](../crt/crt-library-features.md) only.  
  
## See Also  
 [Debug Routines](../crt/debug-routines.md)   
 [__debugbreak](../intrinsics/__debugbreak.md)