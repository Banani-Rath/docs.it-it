---
title: "Operatore &lt;&lt;= (Riferimenti per C#) | Microsoft Docs"
ms.custom: ""
ms.date: "11/17/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "<<=_CSharpKeyword"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "<<= (operatore di assegnazione left shift) [C#]"
  - "operatore di assegnazione left shift (<<=) [C#]"
ms.assetid: 3bc99c78-1edb-4827-86fc-bce6c3048871
caps.latest.revision: 16
caps.handback.revision: 16
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# Operatore &lt;&lt;= (Riferimenti per C#)
Operatore di assegnazione spostamento a sinistra.  
  
## Note  
 Un'espressione con il seguente formato:  
  
```  
x <<= y  
```  
  
 viene valutata come  
  
```  
x = x << y  
```  
  
 con la differenza che `x` viene valutato solo una volta.  L'[operatore \<\<](../../../csharp/language-reference/operators/left-shift-operator.md) sposta `x` verso sinistra del numero di bit specificato da `y`.  
  
 L'operatore `<<=` non può essere sottoposto direttamente a overload; tuttavia, i tipi definiti dall'utente possono eseguire l'overload dell'[operatore \<\<](../../../csharp/language-reference/operators/left-shift-operator.md). Per ulteriori informazioni, vedere [operator](../../../csharp/language-reference/keywords/operator.md).  
  
## Esempio  
 [!CODE [csRefOperators#12](../CodeSnippet/VS_Snippets_VBCSharp/csrefOperators#12)]  
  
## Vedere anche  
 [Riferimenti per C\#](../../../csharp/language-reference/index.md)   
 [Guida per programmatori C\#](../../../csharp/programming-guide/index.md)   
 [Operatori](../../../csharp/language-reference/operators/index.md)