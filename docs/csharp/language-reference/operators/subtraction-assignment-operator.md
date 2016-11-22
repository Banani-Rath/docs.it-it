---
title: "Operatore /= (Riferimenti per C#) | Microsoft Docs"
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
  - "/=_CSharpKeyword"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "/= (operatore di assegnazione di divisione) [C#]"
  - "operatore di assegnazione di divisione (/=) [C#]"
ms.assetid: 50fc02b0-ee9c-4c3e-b58d-d591282caf1c
caps.latest.revision: 17
caps.handback.revision: 17
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# Operatore /= (Riferimenti per C#)
Operatore di assegnazione di divisione.  
  
## Note  
 Un'espressione che utilizza l'operatore di assegnazione `/=`, ad esempio  
  
```  
x /= y  
```  
  
 equivale a  
  
```  
x = x / y  
```  
  
 con la differenza che `x` viene valutato solo una volta.  Per i tipi numerici, l'[operatore \/](../../../csharp/language-reference/operators/division-operator.md) è già definito per l'esecuzione di divisioni.  
  
 L'operatore`/=` non può essere sottoposto direttamente a overload; tuttavia, i tipi definiti dall'utente possono eseguire l'overload dell'[operatore \/](../../../csharp/language-reference/operators/division-operator.md). Per ulteriori informazioni, vedere [operator](../../../csharp/language-reference/keywords/operator.md).  Su tutti gli operatori di assegnazione composti, l'overload dell'operatore binario esegue in modo implicito l'overload dell'assegnazione composta equivalente.  
  
## Esempio  
 [!CODE [csRefOperators#5](../CodeSnippet/VS_Snippets_VBCSharp/csrefOperators#5)]  
  
## Vedere anche  
 [Riferimenti per C\#](../../../csharp/language-reference/index.md)   
 [Guida per programmatori C\#](../../../csharp/programming-guide/index.md)   
 [Operatori](../../../csharp/language-reference/operators/index.md)