---
title: "Procedura: implementare in modo esplicito i membri di due interfacce (Guida per programmatori C#) | Microsoft Docs"
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
  - "ereditarietà [C#], implementazione esplicita dei membri d'interfaccia"
  - "interfacce [C#], implementazione esplicita con ereditarietà"
ms.assetid: 8b402ddc-dff9-4869-89cb-d718c764e68e
caps.latest.revision: 15
caps.handback.revision: 15
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# Procedura: implementare in modo esplicito i membri di due interfacce (Guida per programmatori C#)
L'implementazione esplicita dell'[interfaccia](../../../csharp/language-reference/keywords/interface.md) consente inoltre al programmatore di implementare due interfacce che presentano gli stessi nomi di membri e di operare un'implementazione separata per ciascun membro dell'interfaccia.  In questo sono visualizzate le dimensioni di una casella sia in unità di misura decimali che in unità di misura inglesi.  La [classe](../../../csharp/language-reference/keywords/class.md) Box implementa due interfacce, IEnglishDimensions e IMetricDimensions, che rappresentano i diversi sistemi di misura.  Entrambe le interfacce presentano gli stessi nomi di membri: Length e Width.  
  
## Esempio  
 [!CODE [csProgGuideInheritance#9](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideInheritance#9)]  
  
## Programmazione efficiente  
 Se si desidera esprimere le misure predefinite in unità inglesi, implementare i metodi Length e Width normalmente e implementare in modo esplicito i metodi Length e Width dall'interfaccia IMetricDimensions:  
  
 [!CODE [csProgGuideInheritance#10](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideInheritance#10)]  
  
 In questo caso è possibile accedere alle unità di misura inglesi dall'istanza di classe e alle unità decimali dall'istanza di interfaccia:  
  
 [!CODE [csProgGuideInheritance#11](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideInheritance#11)]  
  
## Vedere anche  
 [Guida per programmatori C\#](../../../csharp/programming-guide/index.md)   
 [Classi e struct](../../../csharp/programming-guide/classes-and-structs/index.md)   
 [Interfacce](../../../csharp/programming-guide/interfaces/index.md)   
 [Procedura: implementare in modo esplicito i membri di interfaccia](../../../csharp/programming-guide/interfaces/how-to-explicitly-implement-interface-members.md)