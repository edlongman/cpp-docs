---
title: "ostrstream Class | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology:  
  - "cpp-standard-libraries"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: ['ostrstream', 'strstream/std::ostrstream::freeze', 'strstream/std::ostrstream::pcount', 'strstream/std::ostrstream::rdbuf', 'strstream/std::ostrstream::str']  
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "ostrstream class"
ms.assetid: e2e34679-b266-4728-a8e1-8eda5d400e46
caps.latest.revision: 20
author: "corob-msft"
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
# ostrstream Class
Describes an object that controls insertion of elements and encoded objects into a stream buffer of class [strstreambuf](../standard-library/strstreambuf-class.md).  
  
## Syntax  
  
```
class ostrstream : public ostream
```  
  
## Remarks  
 The object stores an object of class `strstreambuf`.  
  
> [!NOTE]
>  This class is deprecated. Consider using [ostringstream](../standard-library/sstream-typedefs.md#ostringstream) or [wostringstream](../standard-library/sstream-typedefs.md#wostringstream) instead.  
  
### Constructors  
  
|||  
|-|-|  
|[ostrstream](#ostrstream)|Constructs an object of type `ostrstream`.|  
  
### Member Functions  
  
|||  
|-|-|  
|[freeze](#freeze)|Causes a stream buffer to be unavailable through stream buffer operations.|  
|[pcount](#pcount)|Returns a count of the number of elements written to the controlled sequence.|  
|[rdbuf](#rdbuf)|Returns a pointer to the stream's associated `strstreambuf` object.|  
|[str](#str)|Calls [freeze](../standard-library/strstreambuf-class.md#freeze), and then returns a pointer to the beginning of the controlled sequence.|  
  
## Requirements  
 **Header:** \<strstream>  
  
 **Namespace:** std  
  
##  <a name="freeze"></a>  ostrstream::freeze  
 Causes a stream buffer to be unavailable through stream buffer operations.  
  
```
void freeze(bool _Freezeit = true);
```  
  
### Parameters  
 `_Freezeit`  
 A `bool` indicating whether you want the stream to be frozen.  
  
### Remarks  
 The member function calls [rdbuf](#rdbuf) -> [freeze](../standard-library/strstreambuf-class.md#freeze)(_ *Freezeit*).  
  
### Example  
  See [strstream::freeze](../standard-library/strstreambuf-class.md#freeze) for an example that uses **freeze**.  
  
##  <a name="ostrstream"></a>  ostrstream::ostrstream  
 Constructs an object of type `ostrstream`.  
  
```
ostrstream();

ostrstream(char* ptr,
    streamsize count,
    ios_base::openmode _Mode = ios_base::out);
```  
  
### Parameters  
 `ptr`  
 The buffer.  
  
 `count`  
 The size of the buffer in bytes.  
  
 `_Mode`  
 The input and output mode of the buffer. See [ios_base::openmode](../standard-library/ios-base-class.md#openmode) for more information.  
  
### Remarks  
 Both constructors initialize the base class by calling [ostream](../standard-library/ostream-typedefs.md#ostream)( **sb**), where **sb** is the stored object of class [strstreambuf](../standard-library/strstreambuf-class.md). The first constructor also initializes **sb** by calling `strstreambuf`. The second constructor initializes the base class one of two ways:  
  
-   If `_Mode` & **ios_base::app**== 0, then `ptr` must designate the first element of an array of `count` elements, and the constructor calls `strstreambuf`( `ptr`, `count`, `ptr`).  
  
-   Otherwise, `ptr` must designate the first element of an array of count elements that contains a C string whose first element is designated by `ptr`, and the constructor calls `strstreambuf`( `ptr`, `count`, `ptr` + `strlen`( `ptr`) ).  
  
##  <a name="pcount"></a>  ostrstream::pcount  
 Returns a count of the number of elements written to the controlled sequence.  
  
```
streamsize pcount() const;
```  
  
### Return Value  
 The number of elements written to the controlled sequence.  
  
### Remarks  
 The member function returns [rdbuf](#rdbuf) -> [pcount](../standard-library/strstreambuf-class.md#pcount).  
  
### Example  
  See [strstream::pcount](../standard-library/strstreambuf-class.md#pcount) for a sample that uses `pcount`.  
  
##  <a name="rdbuf"></a>  ostrstream::rdbuf  
 Returns a pointer to the stream's associated strstreambuf object.  
  
```
strstreambuf *rdbuf() const
```  
  
### Return Value  
 A pointer to the stream's associated strstreambuf object.  
  
### Remarks  
 The member function returns the address of the stored stream buffer of type **pointer** to [strstreambuf](../standard-library/strstreambuf-class.md).  
  
### Example  
  See [strstreambuf::pcount](../standard-library/strstreambuf-class.md#pcount) for a sample that uses `rdbuf`.  
  
##  <a name="str"></a>  ostrstream::str  
 Calls [freeze](../standard-library/strstreambuf-class.md#freeze), and then returns a pointer to the beginning of the controlled sequence.  
  
```
char *str();
```  
  
### Return Value  
 A pointer to the beginning of the controlled sequence.  
  
### Remarks  
 The member function returns [rdbuf](#rdbuf) -> [str](../standard-library/strstreambuf-class.md#str).  
  
### Example  
  See [strstream::str](../standard-library/strstreambuf-class.md#str) for a sample that uses **str**.  
  
## See Also  
 [ostream](../standard-library/ostream-typedefs.md#ostream)   
 [Thread Safety in the C++ Standard Library](../standard-library/thread-safety-in-the-cpp-standard-library.md)   
 [iostream Programming](../standard-library/iostream-programming.md)   
 [iostreams Conventions](../standard-library/iostreams-conventions.md)



