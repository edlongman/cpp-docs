---
title: "How BSCMAKE Builds a .Bsc File"
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
ms.assetid: 8512b33e-c856-44a2-87bd-01ab10b52a95
caps.latest.revision: 7
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
# How BSCMAKE Builds a .Bsc File
BSCMAKE builds or rebuilds a .bsc file in the most efficient way it can. To avoid potential problems, it is important to understand the build process.  
  
 When BSCMAKE builds a browse information file, it truncates the .sbr files to zero length. During a subsequent build of the same file, a zero-length (or empty) .sbr file tells BSCMAKE that the .sbr file has no new contribution to make. It lets BSCMAKE know that an update of that part of the file is not required and an incremental build will be sufficient. During every build (unless the /n option is specified), BSCMAKE first attempts to update the file incrementally by using only those .sbr files that have changed.  
  
 BSCMAKE looks for a .bsc file that has the name specified with the /o option. If /o is not specified, BSCMAKE looks for a file that has the base name of the first .sbr file and a .bsc extension. If the file exists, BSCMAKE performs an incremental build of the browse information file using only the contributing .sbr files. If the file does not exist, BSCMAKE performs a full build using all .sbr files. The rules for builds are as follows:  
  
-   For a full build to succeed, all specified .sbr files must exist and must not be truncated. If an .sbr file is truncated, you must rebuild it (by recompiling or assembling) before running BSCMAKE.  
  
-   For an incremental build to succeed, the .bsc file must exist. All contributing .sbr files, even empty files, must exist and must be specified on the BSCMAKE command line. If you omit an .sbr file from the command line, BSCMAKE removes its contribution from the file.  
  
## See Also  
 [Building a .Bsc File](../VS_visualcpp/Building-a-.Bsc-File.md)