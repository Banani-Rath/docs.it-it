---
title: "Operatore &amp; (Riferimenti per C#) | Microsoft Docs"
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
  - "&_CSharpKeyword"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "operatore AND bit per bit [C#]"
  - "e commerciale (operatore) (&) [C#]"
  - "& (operatore) [C#]"
  - "AND (operatore) (&) [C#]"
ms.assetid: afa346d5-90ec-4b1f-a2c8-3881f018741d
caps.latest.revision: 19
caps.handback.revision: 19
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# Operatore &amp; (Riferimenti per C#)
L'operatore & può essere utilizzato come operatore unario o binario.  
  
## Note  
 L'operatore unario & restituisce l'indirizzo dell'operando e richiede un contesto [unsafe](../../../csharp/language-reference/keywords/unsafe.md).  
  
 Gli operatori binari & sono già definiti per i tipi integrali e `bool`.  Per i tipi integrali, l'operatore & calcola l'operatore AND logico bit per bit degli operandi.  Per gli operandi `bool`, l'operatore & calcola l'operatore AND logico degli operandi. Il risultato sarà quindi `true` se e solo se entrambi gli operandi sono `true`.  
  
 L'operatore `&` valuta entrambi gli operatori indipendentemente dal valore del primo.  Ad esempio:  
  
 [!CODE [csRefOperators#37](../CodeSnippet/VS_Snippets_VBCSharp/csrefOperators#37)]  
  
 I tipi definiti dall'utente possono eseguire l'overload dell'operatore `&` binario. Vedere [operator](../../../csharp/language-reference/keywords/operator.md).  Le operazioni sui tipi integrali sono generalmente consentite sull'enumerazione.  Quando si esegue l'overload di un operatore binario, viene eseguito in modo implicito anche l'overload dell'eventuale operatore di assegnazione corrispondente.  
  
## Esempio  
 [!CODE [csRefOperators#38](../CodeSnippet/VS_Snippets_VBCSharp/csrefOperators#38)]  
  
## Vedere anche  
 [Riferimenti per C\#](../../../csharp/language-reference/index.md)   
 [Guida per programmatori C\#](../../../csharp/programming-guide/index.md)   
 [Operatori](../../../csharp/language-reference/operators/index.md)