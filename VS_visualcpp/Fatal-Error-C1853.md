---
title: "Fatal Error C1853"
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
ms.topic: error-reference
ms.assetid: ceb9b4a5-92bf-4573-8a9f-3109cc7743ce
caps.latest.revision: 10
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
# Fatal Error C1853
'filename' precompiled header file is from a previous version of the compiler, or the precompiled header is C++ and you are using it from C (or vice versa)  
  
 Possible causes:  
  
-   The precompiled header was compiled with a previous compiler version. Try recompiling the header with the current compiler.  
  
-   The precompiled header is C++ and you are using it from C. Try recompiling the header for use with C by specifying one of the [/Tc](../VS_visualcpp/-Tc---Tp---TC---TP--Specify-Source-File-Type-.md) compiler options, or changing the suffix of the source file to "c". For more information, see [Two Choices for Precompiling Code](../VS_visualcpp/Two-Choices-for-Precompiling-Code.md).