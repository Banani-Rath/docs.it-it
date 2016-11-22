---
title: "How to: Log Exceptions in Visual Basic | Microsoft Docs"
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
  - "exceptions, logging"
  - "exceptions, tracking"
ms.assetid: a26c60e2-ae39-444a-aebb-33eccadc0eeb
caps.latest.revision: 19
caps.handback.revision: 19
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translationtype: Human Translation
---
# How to: Log Exceptions in Visual Basic
È possibile utilizzare gli oggetti `My.Application.Log` e `My.Log` per registrare informazioni sulle eccezioni che si verificano nell'applicazione.  Negli esempi riportati di seguito è illustrato l'utilizzo del metodo `My.Application.Log.WriteException` per registrare le eccezioni rilevate in modo esplicito e quelle non gestite.  
  
 Per registrare le informazioni di tracciatura, utilizzare il metodo `My.Application.Log.WriteEntry`.  Per ulteriori informazioni, vedere <xref:Microsoft.VisualBasic.Logging.Log.WriteEntry%2A>.  
  
### Per registrare un'eccezione gestita  
  
1.  Creare il metodo che genererà le informazioni sull'eccezione.  
  
     [!CODE [VbVbalrMyApplicationLog#9](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyApplicationLog#9)]  
  
2.  Utilizzare un blocco `Try...Catch` per rilevare l'eccezione.  
  
     [!CODE [VbVbalrMyApplicationLog#6](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyApplicationLog#6)]  
  
3.  Inserire il codice che potrebbe generare un'eccezione nel blocco `Try`.  
  
     Rimuovere il commento dalle righe `Dim` e `MsgBox` per indurre un'eccezione <xref:System.NullReferenceException>.  
  
     [!CODE [VbVbalrMyApplicationLog#7](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyApplicationLog#7)]  
  
4.  Nel blocco `Catch`, utilizzare il metodo `My.Application.Log.WriteException` per scrivere le informazioni sull'eccezione.  
  
     [!CODE [VbVbalrMyApplicationLog#8](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyApplicationLog#8)]  
  
     In l ' esempio seguente viene illustrato il codice completo per registrare un'eccezione gestita.  
  
     [!CODE [VbVbalrMyApplicationLog#10](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyApplicationLog#10)]  
  
### Per registrare un'eccezione non gestita  
  
1.  Selezionare un progetto in **Esplora soluzioni**.  Scegliere **Proprietà** dal menu **Progetto**.  
  
2.  Fare clic sulla scheda **Applicazione**.  
  
3.  Fare clic sul pulsante **Visualizza eventi di applicazioni** per aprire l'editor di codice.  
  
     Verrà aperto il file ApplicationEvents.vb.  
  
4.  Aprire il file ApplicationEvents.vb nell'editor del codice.  Scegliere **Eventi MyApplication** dal menu **Generale**.  
  
5.  Scegliere **UnhandledException** dal menu **Dichiarazioni**.  
  
     L'applicazione genera l'evento <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.UnhandledException> prima dell'esecuzione dell'applicazione principale.  
  
6.  Aggiungere il metodo `My.Application.Log.WriteException` al gestore eventi `UnhandledException`.  
  
     [!CODE [VbVbalrMyApplicationLog#4](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyApplicationLog#4)]  
  
     In l ' esempio seguente viene illustrato il codice completo per registrare un'eccezione non gestita.  
  
     [!CODE [VbVbalrMyApplicationLog#5](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyApplicationLog#5)]  
  
## Vedere anche  
 <xref:Microsoft.VisualBasic.Logging.Log?displayProperty=fullName>   
 <xref:Microsoft.VisualBasic.Logging.Log.WriteEntry%2A>   
 <xref:Microsoft.VisualBasic.Logging.Log.WriteException%2A>   
 [Utilizzo dei log applicazione](../../../../visual-basic/developing-apps/programming/log-info/working-with-application-logs.md)   
 [Procedura: scrivere messaggi di log](../../../../visual-basic/developing-apps/programming/log-info/how-to-write-log-messages.md)   
 [Procedura dettagliata: individuazione della posizione di inserimento delle informazioni con My.Application.Log](../../../../visual-basic/developing-apps/programming/log-info/walkthrough-determining-where-my-application-log-writes-information.md)   
 [Procedura dettagliata: modifica della posizione di inserimento delle informazioni con My.Application.Log](../../../../visual-basic/developing-apps/programming/log-info/walkthrough-changing-where-my-application-log-writes-information.md)