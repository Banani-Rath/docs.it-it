---
title: "How to: Write Text to Files in the My Documents Directory in Visual Basic | Microsoft Docs"
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
  - "files, writing to"
  - "text, writing to files"
  - "examples [Visual Basic], text files"
  - "writing to files, in My Documents"
ms.assetid: 1c726124-781d-4976-9baa-ed46814ff3fe
caps.latest.revision: 19
caps.handback.revision: 19
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translationtype: Human Translation
---
# How to: Write Text to Files in the My Documents Directory in Visual Basic
L'oggetto `My.Computer.FileSystem.SpecialDirectories` consente di accedere a directory speciali, come la directory **Documenti**.  
  
## Procedura  
  
#### Per scrivere nuovo testo nei file della directory Documenti  
  
1.  Utilizzare la proprietà `My.Computer.FileSystem.SpecialDirectories.MyDocuments` per fornire il percorso.  
  
     [!CODE [VbFileIOWrite#1](../CodeSnippet/VS_Snippets_VBCSharp/VbFileIOWrite#1)]  
  
2.  Utilizzare il metodo `WriteAllText` per scrivere testo nel file specificato.  
  
     [!CODE [VbVbcnMyFileSystem#14](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnMyFileSystem#14)]  
  
## Esempio  
 [!CODE [VbFileIOWrite#2](../CodeSnippet/VS_Snippets_VBCSharp/VbFileIOWrite#2)]  
  
## Compilazione del codice  
 Sostituire `test.txt` con il nome del file in cui si desidera scrivere.  
  
## Programmazione efficiente  
 In questo codice vengono rigenerate tutte le eccezioni che possono verificarsi durante la scrittura di testo nel file.  È possibile ridurre la probabilità di eccezioni utilizzando controlli Windows Form quali i controlli dei componenti [OpenFileDialog](../Topic/OpenFileDialog%20Component%20\(Windows%20Forms\).md) e [SaveFileDialog](../Topic/SaveFileDialog%20Component%20\(Windows%20Forms\).md) che limitano le scelte dell'utente a nomi file validi.  Tuttavia, l'uso di questi controlli non è infallibile.  Il file system può subire variazioni nel tempo che intercorre tra la selezione di un file da parte dell'utente e il momento in cui il codice viene eseguito.  Pertanto, quando si utilizzano i file, la gestione delle eccezioni sarà quasi sempre necessaria.  
  
## Sicurezza di .NET Framework  
 Se eseguito in un contesto ad attendibilità parziale, il codice potrebbe generare un'eccezione a causa dell'insufficienza di privilegi.  Per ulteriori informazioni, vedere [Code Access Security Basics](../Topic/Code%20Access%20Security%20Basics.md).  
  
 In questo esempio viene creato un nuovo file.  Per poter creare un file in un'applicazione, è necessario che l'applicazione disponga dell'autorizzazione per la creazione della cartella.  Le autorizzazioni vengono impostate tramite gli elenchi di controllo di accesso \(ACL\).  Se il file è già esistente, l'applicazione necessita solo dell'autorizzazione per l'accesso in scrittura, ossia di un privilegio inferiore.  Laddove possibile, è più sicuro creare il file durante la fase di distribuzione e concedere l'accesso in lettura a un unico file, anziché concedere i privilegi per la creazione di una cartella.  È inoltre più sicuro scrivere i dati nelle cartelle utente anziché nella cartella radice o nella cartella **Programmi**.  Per ulteriori informazioni, vedere [ACL Technology Overview](http://msdn.microsoft.com/it-it/06fbf66d-6f02-4378-b863-b2f12e349045).  
  
## Vedere anche  
 <xref:System.IO.Path.Combine%2A?displayProperty=fullName>   
 <xref:Microsoft.VisualBasic.Devices.Computer>   
 <xref:Microsoft.VisualBasic.FileIO.FileSystem>   
 <xref:Microsoft.VisualBasic.FileIO.FileSystem.WriteAllText%2A>   
 <xref:Microsoft.VisualBasic.FileIO.SpecialDirectories>