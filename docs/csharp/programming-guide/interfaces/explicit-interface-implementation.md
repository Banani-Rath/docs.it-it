---
title: "Implementazione esplicita dell&#39;interfaccia (Guida per programmatori C#) | Microsoft Docs"
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
  - "interfacce esplicite [C#]"
  - "interfacce [C#], esplicite"
ms.assetid: 181c901f-0d4c-4f29-97fc-895079617bf2
caps.latest.revision: 14
caps.handback.revision: 14
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# Implementazione esplicita dell&#39;interfaccia (Guida per programmatori C#)
Se una [classe](../../../csharp/language-reference/keywords/class.md) implementa due interfacce che contengono un membro con la stessa firma e quest'ultimo viene implementato sulla classe, entrambe le interfacce utilizzeranno il membro come propria implementazione.  Nell'esempio seguente, tutte le chiamate a `Paint` richiamare lo stesso metodo.  
  
 [!CODE [csProgGuideInheritance#39](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideInheritance#39)]  
  
 Se tuttavia due membri di [interfaccia](../../../csharp/language-reference/keywords/interface.md) non eseguono la stessa funzione, l'implementazione di una o di entrambe le interfacce potrebbe non risultare corretta.  È possibile implementare un membro di interfaccia in modo esplicito, ossia creando un membro di classe che viene chiamato solo tramite l'interfaccia e che è specifico di tale interfaccia.  Per questa operazione è necessario assegnare al membro di classe il nome dell'interfaccia seguito da un punto.  Ad esempio:  
  
 [!CODE [csProgGuideInheritance#40](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideInheritance#40)]  
  
 Il membro di classe `IControl.Paint` è disponibile solo tramite l'interfaccia `IControl`, mentre `ISurface.Paint` è disponibile solo tramite `ISurface`.  Entrambe le implementazioni del metodo sono distinte e nessuna è direttamente disponibile sulla classe.  Ad esempio:  
  
 [!CODE [csProgGuideInheritance#41](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideInheritance#41)]  
  
 L'implementazione esplicita consente inoltre di risolvere i casi in cui due interfacce dichiarano membri diversi con lo stesso nome, ad esempio una proprietà e un metodo:  
  
 [!CODE [csProgGuideInheritance#42](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideInheritance#42)]  
  
 Per implementare entrambe le interfacce, una classe deve utilizzare l'implementazione esplicita per la proprietà P o il metodo P oppure per entrambi, in modo da evitare che venga generato un errore del compilatore.  Ad esempio:  
  
 [!CODE [csProgGuideInheritance#43](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideInheritance#43)]  
  
## Vedere anche  
 [Guida per programmatori C\#](../../../csharp/programming-guide/index.md)   
 [Classi e struct](../../../csharp/programming-guide/classes-and-structs/index.md)   
 [Interfacce](../../../csharp/programming-guide/interfaces/index.md)   
 [Ereditarietà](../../../csharp/programming-guide/classes-and-structs/inheritance.md)