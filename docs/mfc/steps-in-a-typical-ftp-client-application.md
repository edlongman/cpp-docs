---
title: "Steps in a Typical FTP Client Application"
ms.custom: na
ms.date: "10/14/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: na
ms.topic: "article"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "Internet client applications, FTP table"
  - "FTP (File Transfer Protocol)"
  - "WinInet classes, FTP"
  - "FTP (File Transfer Protocol), client applications"
  - "Internet applications, FTP client applications"
ms.assetid: 70bed7b5-6040-40d1-bc77-702e63a698f2
caps.latest.revision: 9
ms.author: "mblome"
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
# Steps in a Typical FTP Client Application
A typical FTP client application creates a [CInternetSession](../mfcref/cinternetsession-class.md) and a [CFtpConnection](../mfcref/cftpconnection-class.md) object. Note that these MFC WinInet classes do not actually control the proxy type settings; IIS does.  
  
 Also, see these Knowledge Base articles:  
  
-   HOWTO: FTP with CERN-Based Proxy Using WinInet API (Article ID: Q166961)  
  
-   SAMPLE: FTP with CERN-Based Password Protected Proxy (Article ID: Q216214)  
  
-   Internet Services Manager Fails to Show Installed Proxy Services (Article ID: Q216802)  
  
 The following table shows the steps you might perform in a typical FTP client application.  
  
|Your goal|Actions you take|Effects|  
|---------------|----------------------|-------------|  
|Begin an FTP session.|Create a [CInternetSession](../mfcref/cinternetsession-class.md) object.|Initializes WinInet and connects to server.|  
|Connect to an FTP server.|Use [CInternetSession::GetFtpConnection](../Topic/CInternetSession::GetFtpConnection.md).|Returns a [CFtpConnection](../mfcref/cftpconnection-class.md) object.|  
|Change to a new FTP directory on the server.|Use [CFtpConnection::SetCurrentDirectory](../Topic/CFtpConnection::SetCurrentDirectory.md).|Changes the directory you are currently connected to on the server.|  
|Find the first file in the FTP directory.|Use [CFtpFileFind::FindFile](../Topic/CFtpFileFind::FindFile.md).|Finds the first file. Returns FALSE if no files are found.|  
|Find the next file in the FTP directory.|Use [CFtpFileFind::FindNextFile](../Topic/CFtpFileFind::FindNextFile.md).|Finds the next file. Returns FALSE if the file is not found.|  
|Open the file found by **FindFile** or `FindNextFile` for reading or writing.|Use [CFtpConnection::OpenFile](../Topic/CFtpConnection::OpenFile.md), using the file name returned by [FindFile](../Topic/CFtpFileFind::FindFile.md) or [FindNextFile](../Topic/CFtpFileFind::FindNextFile.md).|Opens the file on the server for reading or writing. Returns a [CInternetFile](../mfcref/cinternetfile-class.md) object.|  
|Read from or write to the file.|Use [CInternetFile::Read](../Topic/CInternetFile::Read.md) or [CInternetFile::Write](../Topic/CInternetFile::Write.md).|Reads or writes the specified number of bytes, using a buffer you supply.|  
|Handle exceptions.|Use the [CInternetException](../mfcref/cinternetexception-class.md) class.|Handles all common Internet exception types.|  
|End the FTP session.|Dispose of the [CInternetSession](../mfcref/cinternetsession-class.md) object.|Automatically cleans up open file handles and connections.|  
  
## See Also  
 [Win32 Internet Extensions (WinInet)](../mfc/win32-internet-extensions--wininet-.md)   
 [Prerequisites for Internet Client Classes](../mfc/prerequisites-for-internet-client-classes.md)   
 [Writing an Internet Client Application Using MFC WinInet Classes](../mfc/writing-an-internet-client-application-using-mfc-wininet-classes.md)