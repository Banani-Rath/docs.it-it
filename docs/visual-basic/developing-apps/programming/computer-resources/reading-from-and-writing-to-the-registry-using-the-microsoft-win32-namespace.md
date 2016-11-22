---
title: "Lettura e scrittura nel Registro di sistema mediante lo spazio dei nomi Microsoft.Win32 (Visual Basic) | Microsoft Docs"
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
  - "Registro di sistema, Visual Basic"
ms.assetid: 4a0dcce0-c27b-4199-baa8-ee4528da6a56
caps.latest.revision: 20
caps.handback.revision: 20
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translationtype: Human Translation
---
# Lettura e scrittura nel Registro di sistema mediante lo spazio dei nomi Microsoft.Win32 (Visual Basic)
`My.Computer.Registry` dovrebbe essere in grado di soddisfare le esigenze di base della programmazione con il Registro di sistema, ma è possibile usare anche le classi <xref:Microsoft.Win32.Registry> e <xref:Microsoft.Win32.RegistryKey> dello spazio dei nomi <xref:Microsoft.Win32> di [!INCLUDE[dnprdnshort](../../../../csharp/getting-started/includes/dnprdnshort_md.md)].  
  
## Chiavi nella classe Registry  
 La classe <xref:Microsoft.Win32.Registry> include le chiavi di base del Registro di sistema che è possibile usare per accedere alle sottochiavi e ai relativi valori. Le chiavi di base sono di sola lettura. La tabella seguente elenca e descrive le sette chiavi esposte dalla classe <xref:Microsoft.Win32.Registry>.  
  
|**Chiave**|**Descrizione**|  
|----------------|---------------------|  
|<xref:Microsoft.Win32.Registry.ClassesRoot>|Definisce i tipi di documento e le relative proprietà.|  
|<xref:Microsoft.Win32.Registry.CurrentConfig>|Contiene informazioni non specifiche dell'utente sulla configurazione hardware.|  
|<xref:Microsoft.Win32.Registry.CurrentUser>|Contiene informazioni sulle preferenze dell'utente corrente, ad esempio le variabili di ambiente.|  
|<xref:Microsoft.Win32.Registry.DynData>|Contiene i dati dinamici del Registro di sistema, ad esempio quelli usati dai driver delle periferiche virtuali.|  
|<xref:Microsoft.Win32.Registry.LocalMachine>|Contiene cinque sottochiavi \(Hardware, SAM, Security, Software e System\) in cui sono disponibili i dati di configurazione relativi al computer locale.|  
|<xref:Microsoft.Win32.Registry.PerformanceData>|Contiene informazioni sulle prestazioni per i componenti software.|  
|<xref:Microsoft.Win32.Registry.Users>|Contiene informazioni sulle preferenze predefinite degli utenti.|  
  
> [!IMPORTANT]
>  È più sicuro scrivere dati per l'utente corrente \(<xref:Microsoft.Win32.Registry.CurrentUser>\) che non per il computer locale \(<xref:Microsoft.Win32.Registry.LocalMachine>\). Quando la chiave che si sta creando è stata precedentemente creata da un altro processo, probabilmente dannoso, si verifica una condizione comunemente definita "squatting". Per evitare che si verifichi tale situazione, usare un metodo, ad esempio <xref:Microsoft.Win32.RegistryKey.GetValue%2A>, che restituisce `Nothing` se la chiave non esiste già.  
  
## Lettura di un valore dal Registro di sistema  
 Il codice seguente illustra come leggere una stringa da HKEY\_CURRENT\_USER.  
  
 [!CODE [VbResourceTasks#20](../CodeSnippet/VS_Snippets_VBCSharp/VbResourceTasks#20)]  
  
 Il codice seguente legge, incrementa e quindi scrive una stringa in HKEY\_CURRENT\_USER.  
  
 [!CODE [VbResourceTasks#21](../CodeSnippet/VS_Snippets_VBCSharp/VbResourceTasks#21)]  
  
## Vedere anche  
 <xref:System.SystemException>   
 <xref:System.ApplicationException>   
 <xref:Microsoft.VisualBasic.MyServices.RegistryProxy>   
 [Try...Catch...Finally Statement](../../../../visual-basic/language-reference/statements/try-catch-finally-statement.md)   
 [Reading from and Writing to the Registry](../../../../visual-basic/developing-apps/programming/computer-resources/reading-from-and-writing-to-the-registry.md)   
 [Security and the Registry](../../../../visual-basic/developing-apps/programming/computer-resources/security-and-the-registry.md)