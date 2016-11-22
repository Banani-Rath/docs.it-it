---
title: "Walkthrough: Encrypting and Decrypting Strings in Visual Basic | Microsoft Docs"
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
  - "encryption, strings"
  - "strings [Visual Basic], encrypting"
  - "decryption, strings"
  - "strings [Visual Basic], decrypting"
ms.assetid: 1f51e40a-2f88-43e2-a83e-28a0b5c0d6fd
caps.latest.revision: 18
caps.handback.revision: 18
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translationtype: Human Translation
---
# Walkthrough: Encrypting and Decrypting Strings in Visual Basic
In questa procedura dettagliata viene illustrato l'utilizzo della classe <xref:System.Security.Cryptography.DESCryptoServiceProvider> per la crittografia e decrittografia di stringhe mediante la versione del provider di servizi di crittografia \(CSP\) dell'algoritmo Triple Data Encryption Standard \(<xref:System.Security.Cryptography.TripleDES>\).  Il primo passo è la creazione di una classe wrapper semplice che incapsula l'algoritmo 3DES e memorizza i dati crittografati come stringa con codifica Base 64.  Il wrapper viene quindi utilizzato per archiviare in modo protetto i dati personali dell'utente in un file di testo pubblicamente accessibile.  
  
 È possibile utilizzare la crittografia per proteggere informazioni riservate dell'utente \(ad esempio, la password\) e impedire a utenti non autorizzati la lettura delle credenziali.  È possibile impedire che l'identità di un utente autorizzato venga prelevata, proteggere le risorse dell'utente e fornire il non ripudio.  La crittografia consente inoltre di proteggere i dati dell'utente dall'accesso di utenti non autorizzati.  
  
 Per ulteriori informazioni, vedere [Servizi di crittografia](../Topic/Cryptographic%20Services.md).  
  
> [!IMPORTANT]
>  Gli algoritmi Rijndael, noto ora come Advanced Encryption Standard \(AES\), e Triple Data Encryption Standard \(3DES\) garantiscono una maggiore sicurezza rispetto al DES in quanto più complessi dal punto di vista del calcolo.  Per ulteriori informazioni, vedere <xref:System.Security.Cryptography.DES> e <xref:System.Security.Cryptography.Rijndael>.  
  
### Per creare il wrapper di crittografia  
  
1.  Creare una classe `Simple3Des` per incapsulare i metodi di crittografia e decrittografia.  
  
     [!CODE [VbVbalrStrings#38](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStrings#38)]  
  
2.  Aggiungere un'importazione dello spazio dei nomi di crittografia all'inizio del file che contiene la classe `Simple3Des`.  
  
     [!CODE [VbVbalrStrings#77](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStrings#77)]  
  
3.  Nella classe `Simple3Des`, aggiungere un campo privato per archiviare il provider di servizi crittografici 3DES.  
  
     [!CODE [VbVbalrStrings#39](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStrings#39)]  
  
4.  Aggiungere un metodo privato per creare una matrice di byte di lunghezza specificata dall'hash della chiave indicata.  
  
     [!CODE [VbVbalrStrings#41](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStrings#41)]  
  
5.  Aggiungere un costruttore per inizializzare il provider di servizi crittografici 3DES.  
  
     Il parametro `key` controlla i metodi `EncryptData` e `DecryptData`.  
  
     [!CODE [VbVbalrStrings#40](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStrings#40)]  
  
6.  Aggiungere un metodo pubblico per la crittografia della stringa.  
  
     [!CODE [VbVbalrStrings#42](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStrings#42)]  
  
7.  Aggiungere un metodo pubblico per la decrittografia della stringa.  
  
     [!CODE [VbVbalrStrings#43](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStrings#43)]  
  
     È ora possibile utilizzare la classe wrapper per proteggere le risorse dell'utente.  Nel seguente esempio, la classe viene utilizzata per archiviare in modo protetto i dati personali dell'utente in un file di testo accessibile pubblicamente.  
  
### Per verificare il funzionamento del wrapper di crittografia  
  
1.  Aggiungere in un'altra classe un metodo che utilizza il metodo `EncryptData` del wrapper per crittografare una stringa e scriverla nella cartella Documenti dell'utente.  
  
     [!CODE [VbVbalrStrings#78](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStrings#78)]  
  
2.  Aggiungere un metodo con cui è possibile leggere la stringa crittografata nella cartella Documenti dell'utente e decrittografare tale stringa con il metodo `DecryptData` del wrapper.  
  
     [!CODE [VbVbalrStrings#79](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStrings#79)]  
  
3.  Aggiungere il codice dell'interfaccia dell'utente per chiamare i metodi `TestEncoding` e `TestDecoding`.  
  
4.  Eseguire l'applicazione.  
  
     Se viene fornita una password errata, non è possibile decrittografare i dati durante la verifica dell'applicazione.  
  
## Vedere anche  
 <xref:System.Security.Cryptography>   
 <xref:System.Security.Cryptography.DESCryptoServiceProvider>   
 <xref:System.Security.Cryptography.DES>   
 <xref:System.Security.Cryptography.TripleDES>   
 <xref:System.Security.Cryptography.Rijndael>   
 [Servizi di crittografia](../Topic/Cryptographic%20Services.md)