---
title: "Procedura: scrivere un costruttore di copia (Guida per programmatori C#) | Microsoft Docs"
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
  - "Linguaggio C#, costruttore di copia"
  - "costruttore di copia [C#]"
ms.assetid: fba899b5-fc41-428e-a745-3ebdbf37990a
caps.latest.revision: 20
caps.handback.revision: 20
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# Procedura: scrivere un costruttore di copia (Guida per programmatori C#)
C\# non fornisce un costruttore di copia per gli oggetti, tuttavia è possibile scriverne uno manualmente.  
  
## Esempio  
 Nell'esempio seguente, nella [classe](../../../csharp/language-reference/keywords/class.md) `Person` viene definito un costruttore di copia che accetta come argomento un'istanza di `Person`.  I valori delle proprietà dell'argomento vengono assegnati alle proprietà della nuova istanza di `Person`.  Il codice contiene un costruttore di copia alternativo che invia le proprietà `Name` e `Age` dell'istanza che si desidera copiare al costruttore di istanza della classe.  
  
 [!CODE [csProgGuideObjects#16](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#16)]  
  
## Vedere anche  
 <xref:System.ICloneable>   
 [Guida per programmatori C\#](../../../csharp/programming-guide/index.md)   
 [Classi e struct](../../../csharp/programming-guide/classes-and-structs/index.md)   
 [Costruttori](../../../csharp/programming-guide/classes-and-structs/constructors.md)   
 [Distruttori](../../../csharp/programming-guide/classes-and-structs/destructors.md)