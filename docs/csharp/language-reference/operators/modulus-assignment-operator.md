---
title: "Operatore %= (Riferimenti per C#) | Microsoft Docs"
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
  - "%=_CSharpKeyword"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "%= (operatore di assegnazione) (assegnazione di modulo) [C#]"
  - "operatore di assegnazione di modulo (=%) [C#]"
ms.assetid: 47e5f068-1d97-4010-bd3b-e21b5d3a77f5
caps.latest.revision: 20
caps.handback.revision: 20
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# Operatore %= (Riferimenti per C#)
L'operatore di assegnazione di altri elementi.  
  
## Note  
 Un'espressione che utilizza l'operatore di assegnazione `%=`, ad esempio  
  
```  
x %= y  
```  
  
 equivale a  
  
```  
x = x % y  
```  
  
 con la differenza che `x` viene valutato solo una volta.  Per i tipi numerici, l'[operatore %](../../../csharp/language-reference/operators/modulus-operator.md) è predefinito per il calcolo del resto di una divisione.  
  
 L'operatore `%=` non può essere sottoposto direttamente a overload; tuttavia, i tipi definiti dall'utente possono eseguire l'overload dell'[operatore %](../../../csharp/language-reference/operators/modulus-operator.md). Per ulteriori informazioni, vedere [operatore](../../../csharp/language-reference/keywords/operator.md).  
  
## Esempio  
 [!CODE [csRefOperators#4](../CodeSnippet/VS_Snippets_VBCSharp/csrefOperators#4)]  
  
## Vedere anche  
 [Riferimenti per C\#](../../../csharp/language-reference/index.md)   
 [Guida per programmatori C\#](../../../csharp/programming-guide/index.md)   
 [Operatori](../../../csharp/language-reference/operators/index.md)