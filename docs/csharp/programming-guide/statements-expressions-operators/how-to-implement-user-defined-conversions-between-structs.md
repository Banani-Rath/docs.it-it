---
title: "Procedura: implementare conversioni tra struct definite dall&#39;utente (Guida per programmatori C#) | Microsoft Docs"
ms.custom: ""
ms.date: "11/17/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "conversioni definite dall'utente [C#]"
ms.assetid: 97839aef-8fbc-40d5-9769-6b569bc2710b
caps.latest.revision: 11
caps.handback.revision: 11
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# Procedura: implementare conversioni tra struct definite dall&#39;utente (Guida per programmatori C#)
In questo esempio vengono definite due struct, `RomanNumeral` e `BinaryNumeral`, e vengono mostrate delle conversioni tra esse.  
  
## Esempio  
 [!CODE [csProgGuideStatements#13](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideStatements#13)]  
  
## Programmazione efficiente  
  
-   Nell'esempio precedente l'istruzione:  
  
     [!CODE [csProgGuideStatements#14](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideStatements#14)]  
  
     esegue una conversione da `RomanNumeral` a `BinaryNumeral`.  Dal momento che non esiste alcuna conversione diretta da `RomanNumeral` a `BinaryNumeral`, utilizzare un cast per la conversione da `RomanNumeral` a `int` e un altro cast per la conversione da `int` a `BinaryNumeral`.  
  
-   L'istruzione:  
  
     [!CODE [csProgGuideStatements#15](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideStatements#15)]  
  
     esegue una conversione da `BinaryNumeral` a `RomanNumeral`.  Dal momento che `RomanNumeral` definisce una conversione implicita da `BinaryNumeral`, non è necessario alcun cast.  
  
## Vedere anche  
 [Riferimenti per C\#](../../../csharp/language-reference/index.md)   
 [Guida per programmatori C\#](../../../csharp/programming-guide/index.md)   
 [Operatori di conversione](../../../csharp/programming-guide/statements-expressions-operators/conversion-operators.md)