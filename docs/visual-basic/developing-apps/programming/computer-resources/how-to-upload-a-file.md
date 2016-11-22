---
title: "How to: Upload a File in Visual Basic | Microsoft Docs"
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
  - "networks, uploading files"
  - "files, uploading"
  - "uploading files"
  - "UploadFile method"
  - "My.Computer.Network.UploadFile method"
ms.assetid: a8b37924-c523-4fd3-b5ca-cb0074df29cd
caps.latest.revision: 22
caps.handback.revision: 22
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translationtype: Human Translation
---
# How to: Upload a File in Visual Basic
È possibile utilizzare il metodo <xref:Microsoft.VisualBasic.Devices.Network.UploadFile%2A> per caricare un file e archiviarlo in una posizione remota.  Se il parametro `ShowUI` è impostato su `True`, verrà visualizzata una finestra di dialogo in cui viene illustrato lo stato di avanzamento del processo di download e che consente di annullare l'operazione.  
  
### Per caricare un file  
  
-   Utilizzare il metodo `UploadFile` per caricare un file, specificando il percorso del file di origine e il percorso della directory di destinazione come una stringa o un URI \(Uniform Resource Identifier\). Nell'esempio riportato di seguito viene caricato il file `Order.txt` in `http://www.cohowinery.com/uploads.aspx`.  
  
     [!CODE [VbResourceTasks#6](../CodeSnippet/VS_Snippets_VBCSharp/VbResourceTasks#6)]  
  
### Per caricare un file e visualizzare lo stato di avanzamento dell'operazione  
  
-   Utilizzare il metodo `UploadFile` per caricare un file, specificando il percorso del file di origine e il percorso della directory di destinazione come una stringa o URI.  Nell'esempio riportato di seguito viene caricato il file `Order.txt` in `http://www.cohowinery.com/uploads.aspx` senza fornire un nome utente o una password, viene mostrato lo stato di avanzamento del processo di caricamento ed è previsto un intervallo di timeout di 500 millisecondi.  
  
     [!CODE [VbResourceTasks#7](../CodeSnippet/VS_Snippets_VBCSharp/VbResourceTasks#7)]  
  
### Per caricare un file, fornendo un nome utente e una password  
  
-   Utilizzare il metodo `UploadFile` per caricare un file, specificando il percorso del file di origine e il percorso della directory di destinazione come una stringa o URI e il nome utente e la password.  Nell'esempio riportato di seguito viene caricato il file `Order.txt` in `http://www.cohowinery.com/uploads.aspx`, fornendo il nome utente `anonymous` e una password vuota.  
  
     [!CODE [VbResourceTasks#8](../CodeSnippet/VS_Snippets_VBCSharp/VbResourceTasks#8)]  
  
## Programmazione efficiente  
 Le seguenti condizioni possono generare un'eccezione:  
  
-   Il percorso del file locale non è valido \(<xref:System.ArgumentException>\).  
  
-   Autenticazione non riuscita \(<xref:System.Security.SecurityException>\).  
  
-   Timeout della connessione \(<xref:System.TimeoutException>\).  
  
## Vedere anche  
 <xref:Microsoft.VisualBasic.Devices.Network?displayProperty=fullName>   
 <xref:Microsoft.VisualBasic.Devices.Network.UploadFile%2A>   
 [How to: Download a File](../../../../visual-basic/developing-apps/programming/computer-resources/how-to-download-a-file.md)   
 [Procedura: analizzare percorsi di file](../../../../visual-basic/developing-apps/programming/drives-directories-files/how-to-parse-file-paths.md)