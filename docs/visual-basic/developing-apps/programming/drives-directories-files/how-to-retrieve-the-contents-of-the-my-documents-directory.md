---
title: "How to: Retrieve the Contents of the My Documents Directory in Visual Basic | Microsoft Docs"
ms.custom: ""
ms.date: "11/16/2016"
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
  - "My Documents directory"
ms.assetid: 26560d01-7dda-4457-8e95-21db23d71aea
caps.latest.revision: 13
caps.handback.revision: 13
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translationtype: Human Translation
---
# How to: Retrieve the Contents of the My Documents Directory in Visual Basic
È possibile utilizzare l'oggetto <xref:Microsoft.VisualBasic.FileIO.SpecialDirectories> per leggere dati in molte delle directory **All Users**, ad esempio **Documenti** o **Desktop**.  
  
### Per leggere i dati dalla cartella Documenti  
  
-   Utilizzare il metodo `ReadAllText` per leggere il testo dai singoli file in una determinata directory.  Il seguente codice consente di specificare una directory e un file e di utilizzare `ReadAllText` per leggerlo nella stringa denominata `patients`.  
  
     [!CODE [VbVbcnMyFileSystem#15](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnMyFileSystem#15)]  
  
## Vedere anche  
 <xref:Microsoft.VisualBasic.FileIO.SpecialDirectories>   
 <xref:Microsoft.VisualBasic.FileIO.FileSystem.ReadAllText%2A>