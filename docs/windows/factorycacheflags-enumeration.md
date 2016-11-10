---
title: "FactoryCacheFlags Enumeration"
ms.custom: na
ms.date: "10/14/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: na
ms.topic: "reference"
f1_keywords: 
  - "module/Microsoft::WRL::FactoryCacheFlags"
dev_langs: 
  - "C++"
ms.assetid: 6f54258f-0144-4264-9608-414e5905f6fb
caps.latest.revision: 3
ms.author: "mblome"
manager: "ghogen"
translation.priority.ht: 
  - "de-de"
  - "es-es"
  - "fr-fr"
  - "it-it"
  - "ja-jp"
  - "ko-kr"
  - "ru-ru"
  - "zh-cn"
  - "zh-tw"
translation.priority.mt: 
  - "cs-cz"
  - "pl-pl"
  - "pt-br"
  - "tr-tr"
---
# FactoryCacheFlags Enumeration
Determines whether factory objects are cached.  
  
## Syntax  
  
```cpp  
enum FactoryCacheFlags;  
```  
  
## Remarks  
 By default, the factory caching policy is specified as the [ModuleType](../windows/moduletype-enumeration.md) template parameter when you create a Module Class object. To override this policy, specify a `FactoryCacheFlags` value when you create a factory object.  
  
|||  
|-|-|  
|`FactoryCacheDefault`|The caching policy of the `Module` object is used.|  
|`FactoryCacheEnabled`|Enables factory caching regardless of the `ModuleType` template parameter that is used to create a `Module` object.|  
|`FactoryCacheDisabled`|Disables factory caching regardless of the `ModuleType` template parameter that is used to create a `Module` object.|  
  
## Requirements  
 **Header:** implements.h  
  
 **Namespace:** Microsoft::WRL  
  
## See Also  
 [Microsoft::WRL Namespace](../windows/microsoft--wrl-namespace.md)