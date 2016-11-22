---
title: "How to: Call Windows APIs (Visual Basic) | Microsoft Docs"
ms.custom: ""
ms.date: "11/17/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "API calls"
  - "Windows API, calling"
  - "API calls, platform invoke"
  - "calls, stored procedures"
ms.assetid: 27d75f0a-54ab-4ee1-b91d-43513a19b12d
caps.latest.revision: 14
caps.handback.revision: 14
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translationtype: Human Translation
---
# How to: Call Windows APIs (Visual Basic)
Nell'esempio riportato di seguito la funzione `MessageBox` viene definita e chiamata nel file user32.dll, quindi a essa viene passata una stringa.  
  
## Esempio  
 [!CODE [VbVbalrInterop#1](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrInterop#1)]  
  
## Compilazione del codice  
 L'esempio presenta i seguenti requisiti:  
  
-   Un riferimento allo spazio dei nomi <xref:System>.  
  
## Programmazione efficiente  
 Le seguenti condizioni possono generare un'eccezione:  
  
-   Il metodo non è statico, è astratto oppure è stato definito in precedenza.  Il tipo padre è un'interfaccia oppure la lunghezza del *nome* o di *nomeDll* è zero.  \(<xref:System.ArgumentException>\)  
  
-   Il *nome* o il *nomeDll* è `Nothing`.  \(<xref:System.ArgumentNullException>\)  
  
-   Il tipo contenitore è stato creato in precedenza utilizzando `CreateType`.  \(<xref:System.InvalidOperationException>\)  
  
## Vedere anche  
 [A Closer Look at Platform Invoke](http://msdn.microsoft.com/it-it/ba9dd55b-2eaa-45cd-8afd-75cb8d64d243)   
 [Platform Invoke Examples](../Topic/Platform%20Invoke%20Examples.md)   
 [Consuming Unmanaged DLL Functions](../Topic/Consuming%20Unmanaged%20DLL%20Functions.md)   
 [Defining a Method with Reflection Emit](http://msdn.microsoft.com/it-it/84fd3bf6-628f-41aa-83d9-b990cf926e81)   
 [Walkthrough: Calling Windows APIs](../../../visual-basic/programming-guide/com-interop/walkthrough-calling-windows-apis.md)   
 [COM Interop](../../../visual-basic/programming-guide/com-interop/index.md)