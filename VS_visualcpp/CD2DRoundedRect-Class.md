---
title: "CD2DRoundedRect Class"
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
ms.topic: reference
ms.assetid: 06207fb5-e92b-41c0-bceb-b45d8f466531
caps.latest.revision: 15
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
# CD2DRoundedRect Class
A wrapper for `D2D1_ROUNDED_RECT`.  
  
## Syntax  
  
```  
class CD2DRoundedRect : public D2D1_ROUNDED_RECT;  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CD2DRoundedRect::CD2DRoundedRect](#cd2droundedrect__cd2droundedrect)|Overloaded. Constructs a `CD2DRoundedRect` object from `D2D1_ROUNDED_RECT` object.|  
  
## Inheritance Hierarchy  
 `D2D1_ROUNDED_RECT`  
  
 [CD2DRoundedRect](../VS_visualcpp/CD2DRoundedRect-Class.md)  
  
## Requirements  
 **Header:** afxrendertarget.h  
  
##  <a name="cd2droundedrect__cd2droundedrect"></a>  CD2DRoundedRect::CD2DRoundedRect  
 Constructs a CD2DRoundedRect object from CD2DRectF object.  
  
```  
CD2DRoundedRect(  
    const CD2DRectF& rectIn,  
    const CD2DSizeF& sizeRadius );  
  
CD2DRoundedRect(  
    const D2D1_ROUNDED_RECT& rectIn );  
  
CD2DRoundedRect(  
    const D2D1_ROUNDED_RECT* rectIn );  
```  
  
### Parameters  
 `rectIn`  
 source rectangle  
  
 `sizeRadius`  
 radius size  
  
## See Also  
 [Classes](../VS_visualcpp/MFC-Classes.md)