---
title: "Propriet&#224; dell&#39;interfaccia (Guida per programmatori C#) | Microsoft Docs"
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
  - "interfacce [C#], proprietà"
  - "proprietà [C#], nelle interfacce"
ms.assetid: 6503e9ed-33d7-44ec-b4c1-cc16c084b795
caps.latest.revision: 13
caps.handback.revision: 13
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# Propriet&#224; dell&#39;interfaccia (Guida per programmatori C#)
Le proprietà possono essere dichiarate su una [interfaccia](../../../csharp/language-reference/keywords/interface.md).  Nell'esempio seguente viene illustrata la funzione di accesso di un indicizzatore di interfaccia:  
  
 [!CODE [csProgGuideProperties#14](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideProperties#14)]  
  
 La funzione di accesso di una proprietà di interfaccia non include un corpo.  Lo scopo delle funzioni di accesso è quindi di indicare se la proprietà è in lettura\/scrittura, in sola scrittura o in sola lettura.  
  
## Esempio  
 Nell'esempio che segue l'interfaccia `IEmployee` è associata a una proprietà di lettura\/scrittura, `Name`, e a una proprietà in sola lettura, `Counter`.  La classe `Employee` implementa l'interfaccia `IEmployee` e utilizza le due proprietà.  Il programma legge il nome di un nuovo dipendente e il numero corrente di dipendenti, quindi visualizza il nome del dipendente e il relativo numero calcolato.  
  
 È possibile utilizzare il nome completo della proprietà, che fa riferimento all'interfaccia in cui il membro è dichiarato.  Di seguito è riportato un esempio:  
  
 [!CODE [csProgGuideProperties#16](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideProperties#16)]  
  
 Questo meccanismo è denominato [Implementazione esplicita dell'interfaccia](../../../csharp/programming-guide/interfaces/explicit-interface-implementation.md).  Se la classe `Employee`, ad esempio, implementa due interfacce, `ICitizen` e `IEmployee`, ed entrambe le interfacce sono associate alla proprietà `Name`, sarà necessaria l'implementazione esplicita del membro di interfaccia.  Pertanto, la dichiarazione di proprietà  
  
 [!CODE [csProgGuideProperties#16](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideProperties#16)]  
  
 implementa la proprietà `Name` nell'interfaccia `IEmployee`, mentre la dichiarazione  
  
 [!CODE [csProgGuideProperties#17](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideProperties#17)]  
  
 implementa la proprietà `Name` nell'interfaccia `ICitizen`.  
  
 [!CODE [csProgGuideProperties#15](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideProperties#15)]  
  
  **`210 Hazem Abolrous`**    
## Esempio di output  
 `Enter number of employees: 210`  
  
 `Enter the name of the new employee: Hazem Abolrous`  
  
 `The employee information:`  
  
 `Employee number: 211`  
  
 `Employee name: Hazem Abolrous`  
  
## Vedere anche  
 [Guida per programmatori C\#](../../../csharp/programming-guide/index.md)   
 [Proprietà](../../../csharp/programming-guide/classes-and-structs/properties.md)   
 [Utilizzo delle proprietà](../../../csharp/programming-guide/classes-and-structs/using-properties.md)   
 [Confronto tra proprietà e indicizzatori](../../../csharp/programming-guide/indexers/comparison-between-properties-and-indexers.md)   
 [Indicizzatori](../../../csharp/programming-guide/indexers/index.md)   
 [Interfacce](../../../csharp/programming-guide/interfaces/index.md)