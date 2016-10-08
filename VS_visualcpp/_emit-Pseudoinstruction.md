---
title: "_emit Pseudoinstruction"
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
ms.assetid: 004c48f3-364c-4e82-9a51-e326f9cc7b2b
caps.latest.revision: 11
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
# _emit Pseudoinstruction
## Microsoft Specific  
 The **_emit** pseudoinstruction defines one byte at the current location in the current text segment. The **_emit** pseudoinstruction resembles the [DB](../VS_visualcpp/DB.md) directive of MASM.  
  
 The following fragment places the bytes 0x4A, 0x43, and 0x4B into the code:  
  
```  
#define randasm __asm _emit 0x4A __asm _emit 0x43 __asm _emit 0x4B  
 .  
 .  
 .  
__asm {  
     randasm  
     }  
```  
  
> [!CAUTION]
>  If `_emit` generates instructions that modify registers, and you compile the application with optimizations, the compiler cannot determine what registers are affected. For example, if `_emit` generates an instruction that modifies the **rax** register, the compiler does not know that **rax** has changed. The compiler might then make an incorrect assumption about the value in that register after the inline assembler code executes. Consequently, your application might exhibit unpredictable behavior when it runs.  
  
 **END Microsoft Specific**  
  
## See Also  
 [Using Assembly Language in __asm Blocks](../VS_visualcpp/Using-Assembly-Language-in-__asm-Blocks.md)