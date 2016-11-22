---
title: "Procedura: scrivere messaggi di log (Visual Basic) | Microsoft Docs"
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
  - "oggetto My.Application.Log, scrittura di messaggi di log"
ms.assetid: 972a3e0c-2996-4623-a7a9-d7ebc4d207f8
caps.latest.revision: 20
caps.handback.revision: 20
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translationtype: Human Translation
---
# Procedura: scrivere messaggi di log (Visual Basic)
È possibile usare gli oggetti `My.Application.Log` e `My.Log` per registrare le informazioni sull'applicazione. Questo esempio illustra come usare il metodo `My.Application.Log.WriteEntry` per registrare le informazioni di traccia.  
  
 Per registrare le informazioni sulle eccezioni, usare il metodo `My.Application.Log.WriteException`. Vedere [How to: Log Exceptions](../../../../visual-basic/developing-apps/programming/log-info/how-to-log-exceptions.md).  
  
## Esempio  
 Nell'esempio seguente viene usato il metodo `My.Application.Log.WriteEntry` per scrivere le informazioni di traccia.  
  
 [!CODE [VbVbalrMyApplicationLog#11](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyApplicationLog#11)]  
  
## Sicurezza di .NET Framework  
 Verificare che i dati scritti nel log non contengano informazioni riservate, ad esempio le password degli utenti. Per altre informazioni, vedere [Utilizzo dei log applicazione](../../../../visual-basic/developing-apps/programming/log-info/working-with-application-logs.md).  
  
## Vedere anche  
 <xref:Microsoft.VisualBasic.Logging.Log?displayProperty=fullName>   
 <xref:Microsoft.VisualBasic.Logging.Log.WriteEntry%2A>   
 <xref:Microsoft.VisualBasic.Logging.Log.WriteException%2A>   
 [Utilizzo dei log applicazione](../../../../visual-basic/developing-apps/programming/log-info/working-with-application-logs.md)   
 [How to: Log Exceptions](../../../../visual-basic/developing-apps/programming/log-info/how-to-log-exceptions.md)   
 [Procedura dettagliata: individuazione della posizione di inserimento delle informazioni con My.Application.Log](../../../../visual-basic/developing-apps/programming/log-info/walkthrough-determining-where-my-application-log-writes-information.md)   
 [Procedura dettagliata: modifica della posizione di inserimento delle informazioni con My.Application.Log](../../../../visual-basic/developing-apps/programming/log-info/walkthrough-changing-where-my-application-log-writes-information.md)   
 [Walkthrough: Filtering My.Application.Log Output](../../../../visual-basic/developing-apps/programming/log-info/walkthrough-filtering-my-application-log-output.md)