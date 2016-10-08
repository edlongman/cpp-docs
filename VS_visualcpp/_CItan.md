---
title: "_CItan"
ms.custom: na
ms.date: 10/03/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
apiname: 
  - _CItan
apilocation: 
  - msvcr100.dll
  - msvcr110_clr0400.dll
  - msvcr80.dll
  - msvcrt.dll
  - msvcr110.dll
  - msvcr90.dll
  - msvcr120.dll
apitype: DLLExport
ms.assetid: d1ea3113-50a2-45a6-b6bc-680fcdcc0928
caps.latest.revision: 5
manager: ghogen
translation.priority.ht: 
  - de-de
  - es-es
  - fr-fr
  - it-it
  - ja-jp
  - ko-kr
  - ru-ru
  - zh-cn
  - zh-tw
translation.priority.mt: 
  - cs-cz
  - pl-pl
  - pt-br
  - tr-tr
---
# _CItan
Calculates the tangent of the top value on the stack.  
  
## Syntax  
  
```  
void __cdecl _CItan();  
```  
  
## Remarks  
 This version of the `tan` function has a specialized calling convention that the compiler understands. The function speeds up the execution because it prevents copies from being generated and helps with register allocation.  
  
 The resulting value is pushed onto the top of the stack.  
  
## Requirements  
 **Platform:** x86  
  
## See Also  
 [Alphabetical Function Reference](../VS_visualcpp/CRT-Alphabetical-Function-Reference.md)   
 [tan, tanf, tanl, tanh, tanhf, tanhl](../VS_visualcpp/tan--tanf--tanl--tanh--tanhf--tanhl.md)