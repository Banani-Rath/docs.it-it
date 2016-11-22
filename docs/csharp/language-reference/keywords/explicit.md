---
title: "explicit (Riferimenti per C#) | Microsoft Docs"
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
  - "explicit_CSharpKeyword"
  - "explicit"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "explicit (parola chiave) [C#]"
ms.assetid: cfb8f42a-e411-4db2-af9b-796b05644846
caps.latest.revision: 21
caps.handback.revision: 21
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# explicit (Riferimenti per C#)
La parola chiave `explicit` dichiara un operatore di conversione di tipi definito dall'utente che è necessario richiamare con un cast.  Il seguente operatore esegue ad esempio la conversione da una classe denominata Fahrenheit a una classe denominata Celsius:  
  
 [!CODE [csrefKeywordsConversion#2](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsConversion#2)]  
  
 Questo operatore di conversione può essere richiamato nel seguente modo:  
  
 [!CODE [csrefKeywordsConversion#3](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsConversion#3)]  
  
 L'operatore di conversione esegue la conversione da un tipo di origine a un tipo di destinazione.  Il tipo di origine fornisce l'operatore di conversione.  A differenza di quanto avviene per le conversioni implicite, gli operatori di conversione espliciti devono essere richiamati mediante un cast.  Se un'operazione di conversione può provocare eccezioni o la perdita di informazioni, è opportuno contrassegnarla come `explicit`,  per evitare che il compilatore richiami automaticamente l'operazione di conversione con conseguenze imprevedibili.  
  
 Se si omettono i risultati del cast, viene generato l'errore in fase di compilazione CS0266.  
  
 Per ulteriori informazioni, vedere [Utilizzo degli operatori di conversione](../../../csharp/programming-guide/statements-expressions-operators/using-conversion-operators.md).  
  
## Esempio  
 Nell'esempio riportato di seguito vengono utilizzate una classe `Fahrenheit` e una classe `Celsius`, ciascuna delle quali fornisce un operatore di conversione esplicito all'altra classe.  
  
 [!CODE [csrefKeywordsConversion#1](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsConversion#1)]  
  
## Esempio  
 Nell'esempio riportato di seguito viene definita la struttura `Digit` che rappresenta una singola cifra decimale.  Viene definito un operatore per le conversioni da `byte` a `Digit`; tuttavia, poiché non è possibile convertire tutti i byte in un valore `Digit`, la conversione è esplicita.  
  
 [!CODE [csrefKeywordsConversion#4](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsConversion#4)]  
  
## Specifiche del linguaggio C\#  
 [!INCLUDE[CSharplangspec](../../../csharp/language-reference/keywords/includes/csharplangspec_md.md)]  
  
## Vedere anche  
 [Riferimenti per C\#](../../../csharp/language-reference/index.md)   
 [Guida per programmatori C\#](../../../csharp/programming-guide/index.md)   
 [Parole chiave di C\#](../../../csharp/language-reference/keywords/index.md)   
 [impliciti](../../../csharp/language-reference/keywords/implicit.md)   
 [operatore](../../../csharp/language-reference/keywords/operator.md)   
 [Procedura: implementare conversioni tra struct definite dall'utente](../../../csharp/programming-guide/statements-expressions-operators/how-to-implement-user-defined-conversions-between-structs.md)   
 [Conversioni esplicite definite dall'utente concatenate in C\#](http://go.microsoft.com/fwlink/?LinkId=112384)