---
title: "HUGE_VAL, _HUGE"
ms.custom: na
ms.date: 10/03/2016
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
  - _HUGE
apilocation: 
  - msvcrt.dll
apitype: DLLExport
ms.assetid: 3f044b45-02cd-46b2-b1de-87fd0441dd6a
caps.latest.revision: 9
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
# HUGE_VAL, _HUGE
## Syntax  
  
```  
  
#include <math.h>  
  
```  
  
## Remarks  
 `HUGE_VAL` is the largest representable double value. This value is returned by many run-time math functions when an error occurs. For some functions, –`HUGE_VAL` is returned. `HUGE_VAL` is defined as `_HUGE`, but run-time math functions return `HUGE_VAL`. You should also use `HUGE_VAL` in your code for consistency.  
  
## See Also  
 [Global Constants](../VS_visualcpp/Global-Constants.md)