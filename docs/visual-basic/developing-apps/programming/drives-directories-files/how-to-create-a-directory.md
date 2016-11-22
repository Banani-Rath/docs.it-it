---
title: "How to: Create a Directory in Visual Basic | Microsoft Docs"
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
  - "directories [Visual Basic], creating"
  - "folders [Visual Basic], creating"
ms.assetid: 0351a2ca-24d8-43b5-bb39-9b99e6401cff
caps.latest.revision: 19
caps.handback.revision: 19
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translationtype: Human Translation
---
# How to: Create a Directory in Visual Basic
Utilizzare il metodo `CreateDirectory` dell'oggetto `My.Computer.FileSystem` per la creazione di directory.  
  
 Se la directory esiste già non verrà generata alcuna eccezione.  
  
### Per creare una directory  
  
-   Utilizzare il metodo `CreateDirectory` specificando il percorso completo della posizione in cui deve essere creata la directory.  Nell'esempio riportato di seguito viene creata la directory `NewDirectory` in `C:\Documents and Settings\All Users\Documents`.  
  
     [!CODE [VbVbcnMyFileSystem#2](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnMyFileSystem#2)]  
  
## Programmazione efficiente  
 Le seguenti condizioni possono generare un'eccezione:  
  
-   Il nome della directory non è corretto.  Ad esempio, contiene caratteri non consentiti oppure è solo uno spazio vuoto \(<xref:System.ArgumentException>\).  
  
-   La directory padre della directory da creare è di sola lettura \(<xref:System.IO.IOException>\).  
  
-   Il nome della directory è `Nothing` \(<xref:System.ArgumentNullException>\).  
  
-   Il nome della directory è troppo lungo \(<xref:System.IO.PathTooLongException>\).  
  
-   Il nome della directory contiene solo i due punti ":" \(<xref:System.NotSupportedException>\).  
  
-   L'utente non dispone dell'autorizzazione per la creazione della directory \(<xref:System.UnauthorizedAccessException>\).  
  
-   L'utente non dispone dell'autorizzazione in una situazione di attendibilità parziale \(<xref:System.Security.SecurityException>\).  
  
## Vedere anche  
 <xref:Microsoft.VisualBasic.FileIO.FileSystem.CreateDirectory%2A>   
 [Creating, Deleting, and Moving Files and Directories](../../../../visual-basic/developing-apps/programming/drives-directories-files/creating-deleting-and-moving-files-and-directories.md)