---
title: "Assertion and User-Supplied Messages (C++)"
ms.custom: na
ms.date: "10/14/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: na
ms.topic: "language-reference"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "user-supplied messages [C++], run time"
  - "user-supplied messages [C++], preprocessor time"
  - "#error%2C assert%2C static_assert [C++]"
  - "user-supplied messages [C++], compile time"
ms.assetid: ebf7d885-61c8-4233-b0ae-1c9a38e0f385
caps.latest.revision: 6
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
# Assertion and User-Supplied Messages (C++)
The C++ language supports three error handling mechanisms that help you debug your application: the [#error directive](../c/sharperror-directive--c-c---.md), the [static_assert](../cpp/static_assert.md) keyword, and the [assert Macro, _assert, _wassert](../crt/assert-macro--_assert--_wassert.md) macro. All three mechanisms issue error messages, and two also test software assertions. A software assertion specifies a condition that you expect to be true at a particular point in your program. If a compile time assertion fails, the compiler issues a diagnostic message and a compilation error. If a run-time assertion fails, the operating system issues a diagnostic message and closes your application.  
  
## Remarks  
 The lifetime of your application consists of a preprocessing, compile, and run time phase. Each error handling mechanism accesses debug information that is available during one of these phases. To debug effectively, select the mechanism that provides appropriate information about that phase:  
  
-   The [#error directive](../c/sharperror-directive--c-c---.md) is in effect at preprocessing time. It unconditionally emits a user-specified message and causes the compilation to fail with an error. The message can contain text that is manipulated by preprocessor directives but any resulting expression is not evaluated.  
  
-   The [static_assert](../cpp/static_assert.md) declaration is in effect at compile time. It tests a software assertion that is represented by a user-specified integral expression that can be converted to a Boolean. If the expression evaluates to zero (false), the compiler issues the user-specified message and the compilation fails with an error.  
  
     The `static_assert` declaration is especially useful for debugging templates because template arguments can be included in the user-specified expression.  
  
-   The [assert Macro, _assert, _wassert](../crt/assert-macro--_assert--_wassert.md) macro is in effect at run time. It evaluates a user-specified expression, and if the result is zero, the system issues a diagnostic message and closes your application. Many other macros, such as[_ASSERT](../crt/_assert--_asserte--_assert_expr-macros.md) and `_ASSERTE`, resemble this macro but issue different system-defined or user-defined diagnostic messages.  
  
## See Also  
 [#error Directive (C/C++)](../c/sharperror-directive--c-c---.md)   
 [assert Macro, _assert, _wassert](../crt/assert-macro--_assert--_wassert.md)   
 [_ASSERT, _ASSERTE, _ASSERT_EXPR Macros](../crt/_assert--_asserte--_assert_expr-macros.md)   
 [static_assert](../cpp/static_assert.md)   
 [_STATIC_ASSERT Macro](../crt/_static_assert-macro.md)   
 [Templates](../cpp/templates--c---.md)