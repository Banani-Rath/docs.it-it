---
title: "How to: Read From Comma-Delimited Text Files in Visual Basic | Microsoft Docs"
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
  - "files, parsing"
  - "text files, tasks"
  - "reading text files, comma-delimited"
  - "text files, reading"
ms.assetid: a8413fe4-0dba-49c8-8692-44fb67a9ec4f
caps.latest.revision: 19
caps.handback.revision: 19
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translationtype: Human Translation
---
# How to: Read From Comma-Delimited Text Files in Visual Basic
L'oggetto `TextFieldParser` consente di analizzare in modo facile ed efficace i file di testo strutturati, ad esempio i log.  La proprietà `TextFieldType` definisce se si tratta di un file delimitato o di un file con campi di testo a larghezza fissa.  
  
### Per analizzare un file di testo delimitato da virgole  
  
1.  Creare un nuovo oggetto `TextFieldParser`.  Nel codice riportato di seguito viene creato l'oggetto `TextFieldParser` denominato `MyReader` e viene aperto il file `test.txt`.  
  
     [!CODE [VbFileIORead#15](../CodeSnippet/VS_Snippets_VBCSharp/VbFileIORead#15)]  
  
2.  Definire il tipo `TextField` e il delimitatore.  Nel codice riportato di seguito viene definita la proprietà `TextFieldType` come `Delimited` e il delimitatore come ",".  
  
     [!CODE [VbFileIORead#16](../CodeSnippet/VS_Snippets_VBCSharp/VbFileIORead#16)]  
  
3.  Scorrere i campi nel file.  Se sono presenti righe danneggiate, segnalare l'errore e continuare l'analisi.  Nel codice riportato di seguito viene eseguito un ciclo nel file, visualizzando ciascun campo e segnalando qualsiasi campo formattato in modo errato.  
  
     [!CODE [VbFileIORead#17](../CodeSnippet/VS_Snippets_VBCSharp/VbFileIORead#17)]  
  
4.  Chiudere i blocchi `While` e `Using` con `End While` e `End Using`.  
  
     [!CODE [VbFileIORead#18](../CodeSnippet/VS_Snippets_VBCSharp/VbFileIORead#18)]  
  
## Esempio  
 Nell'esempio riportato di seguito la lettura viene eseguita dal file `test.txt`.  
  
 [!CODE [VbFileIORead#19](../CodeSnippet/VS_Snippets_VBCSharp/VbFileIORead#19)]  
  
## Programmazione efficiente  
 Le seguenti condizioni possono generare un'eccezione:  
  
-   Non è possibile analizzare una riga utilizzando il formato specificato \(<xref:Microsoft.VisualBasic.FileIO.MalformedLineException>\).  Nel messaggio di eccezione viene specificata la riga che ha generato l'eccezione, mentre la proprietà <xref:Microsoft.VisualBasic.FileIO.TextFieldParser.ErrorLine%2A> viene assegnata al testo contenuto nella riga.  
  
-   Il file specificato non esiste \(<xref:System.IO.FileNotFoundException>\).  
  
-   Un contesto di attendibilità parziale in cui gli utenti non dispongono di autorizzazioni sufficienti per accedere al file  \(<xref:System.Security.SecurityException>\).  
  
-   Il percorso è troppo lungo \(<xref:System.IO.PathTooLongException>\).  
  
-   L'utente non dispone delle autorizzazioni sufficienti per accedere al file \(<xref:System.UnauthorizedAccessException>\).  
  
## Vedere anche  
 <xref:Microsoft.VisualBasic.FileIO.TextFieldParser?displayProperty=fullName>   
 [How to: Read From Fixed\-width Text Files](../../../../visual-basic/developing-apps/programming/drives-directories-files/how-to-read-from-fixed-width-text-files.md)   
 [How to: Read From Text Files with Multiple Formats](../../../../visual-basic/developing-apps/programming/drives-directories-files/how-to-read-from-text-files-with-multiple-formats.md)   
 [Parsing Text Files with the TextFieldParser Object](../../../../visual-basic/developing-apps/programming/drives-directories-files/parsing-text-files-with-the-textfieldparser-object.md)   
 [Walkthrough: Manipulating Files and Directories in Visual Basic](../../../../visual-basic/developing-apps/programming/drives-directories-files/walkthrough-manipulating-files-and-directories.md)   
 [Troubleshooting: Reading from and Writing to Text Files](../../../../visual-basic/developing-apps/programming/drives-directories-files/troubleshooting-reading-from-and-writing-to-text-files.md)   
 [Risoluzione dei problemi relativi alle eccezioni: Microsoft.VisualBasic.FileIO.TextFieldParser.MalformedLineException](../Topic/Troubleshooting%20Exceptions:%20Microsoft.VisualBasic.FileIO.TextFieldParser.MalformedLineException.md)