---
title: "How to: Dial Modems Attached to Serial Ports in Visual Basic | Microsoft Docs"
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
  - "modems, dialing"
  - "serial ports, dialing"
  - "My.Computer.Ports object"
ms.assetid: 3834db40-f431-45f1-b671-dc91787164b6
caps.latest.revision: 19
caps.handback.revision: 19
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translationtype: Human Translation
---
# How to: Dial Modems Attached to Serial Ports in Visual Basic
In questo argomento viene descritto come utilizzare `My.Computer.Ports` per comporre numeri con un modem in [!INCLUDE[vbprvb](../../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)].  
  
 Di solito, il modem è collegato a una delle porte seriali del computer.  Per consentire la comunicazione tra l'applicazione e il modem, è necessario che i comandi vengano inviati alla porta seriale appropriata.  
  
### Per comporre un numero con modem  
  
1.  Individuare la porta seriale alla quale è collegato il modem.  In questo esempio il modem è collegato a COM1.  
  
2.  Utilizzare il metodo `My.Computer.Ports.OpenSerialPort` per ottenere un riferimento alla porta.  Per ulteriori informazioni, vedere <xref:Microsoft.VisualBasic.Devices.Ports.OpenSerialPort%2A>.  
  
     Il blocco `Using` consente all'applicazione di chiudere la porta seriale anche se viene generata un'eccezione.  Tutto il codice relativo alla porta seriale deve essere contenuto all'interno di questo blocco o di un blocco `Try...Catch...Finally`.  
  
     [!CODE [VbVbalrMyComputer#28](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyComputer#28)]  
  
3.  Impostare la proprietà `DtrEnable` per indicare che il computer è pronto per accettare una trasmissione in entrata dal modem.  
  
     [!CODE [VbVbalrMyComputer#29](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyComputer#29)]  
  
4.  Inviare il comando di composizione e il numero di telefono al modem attraverso la porta seriale utilizzando il metodo <xref:System.IO.Ports.SerialPort.Write%2A>.  
  
     [!CODE [VbVbalrMyComputer#30](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyComputer#30)]  
  
## Esempio  
 [!CODE [VbVbalrMyComputer#27](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyComputer#27)]  
  
 Questo esempio di codice è anche disponibile come frammento di codice IntelliSense.  Nella casella di selezione dei frammenti di codice, si trova in **Connettività e rete**.  Per ulteriori informazioni, vedere [Frammenti di codice](/visual-studio/ide/code-snippets).  
  
## Compilazione del codice  
 Per questo esempio è richiesto un riferimento allo spazio dei nomi <xref:System?displayProperty=fullName>.  
  
## Programmazione efficiente  
 In questo esempio il modem è collegato alla porta COM1.  Si consiglia di impostare il codice in modo che consenta all'utente di selezionare la porta seriale desiderata da un elenco di porte disponibili.  Per ulteriori informazioni, vedere [How to: Show Available Serial Ports](../../../../visual-basic/developing-apps/programming/computer-resources/how-to-show-available-serial-ports.md).  
  
 Nell'esempio riportato di seguito viene utilizzato un blocco `Using` per accertarsi che l'applicazione chiuda la porta anche se genera un'eccezione.  Per ulteriori informazioni, vedere [Using Statement](../../../../visual-basic/language-reference/statements/using-statement.md).  
  
 In questo esempio, l'applicazione scollega la porta seriale dopo la composizione dei numeri con modem.  Realisticamente, sarà necessario trasferire i dati da e verso il modem.  Per ulteriori informazioni, vedere [How to: Receive Strings From Serial Ports](../../../../visual-basic/developing-apps/programming/computer-resources/how-to-receive-strings-from-serial-ports.md).  
  
## Vedere anche  
 <xref:Microsoft.VisualBasic.Devices.Ports>   
 <xref:System.IO.Ports.SerialPort?displayProperty=fullName>   
 [How to: Send Strings to Serial Ports](../../../../visual-basic/developing-apps/programming/computer-resources/how-to-send-strings-to-serial-ports.md)   
 [How to: Receive Strings From Serial Ports](../../../../visual-basic/developing-apps/programming/computer-resources/how-to-receive-strings-from-serial-ports.md)   
 [How to: Show Available Serial Ports](../../../../visual-basic/developing-apps/programming/computer-resources/how-to-show-available-serial-ports.md)