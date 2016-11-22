---
title: "Procedura: utilizzare le funzionalit&#224; relative alla documentazione XML (Guida per programmatori C#) | Microsoft Docs"
ms.custom: ""
ms.date: "11/16/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "linguaggio C#, funzionalità della documentazione XML"
  - "documentazione XML [C#]"
ms.assetid: 8f33917b-9577-4c9a-818a-640dbbb0b399
caps.latest.revision: 19
caps.handback.revision: 19
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# Procedura: utilizzare le funzionalit&#224; relative alla documentazione XML (Guida per programmatori C#)
Nell'esempio seguente viene fornita una panoramica di base di un tipo di cui è stata documentato.  
  
## Esempio  
 [!CODE [csProgGuideDocComments#15](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideDocComments#15)]  
  
  **\/\/Questo file xml è stato generato con l'esempio di codice precedente.  \<?xml version\="1.0"?\>**  
**\<doc\>**  
 **\<assembly\>**  
 **\<nome\> xmlsample\<\/name\>**  
 **\<\/assembly\>**  
 **\<members\>**  
 **\<name\= del membro„T:SomeClass\>**   
 **\<summary\>**  
 **Inserire qui la documentazione di riepilogo a livello di classe.\<\/summary\>**  
 **\<remarks\>**  
 **È possibile associare commenti più estesi a un tipo o un membro**   
 **commenti tag\<\/remarks\>**  
 **\<\/member\>**  
 **\<name\= del membro„F:SomeClass.m\_Name\>**   
 **\<summary\>**  
 **archivio per il nome property\<\/summary\>**  
 **\<\/member\>**  
 **\<name\=„M:SomeClass. \#ctor„ del membro\>**   
 **\<riepilogo\> la classe constructor.\<\/summary\>**   
 **\<\/member\>**  
 **\<name\= del membro„M:SomeClass.SomeMethod \(System.String\)„\>**   
 **\<summary\>**  
 **Descrizione di SomeMethod.\<\/summary\>**  
 **\<name\= " s„ param\> La descrizione del parametro per s passa here\<\/param\>**  
 **\<seealso cref\="T:System.String"\>**  
 **È possibile utilizzare l'attributo cref in qualsiasi tag per fare riferimento a un tipo o a un membro**   
 **e il compilatore verificherà l'esistenza del riferimento.  \<\/seealso\>**  
 **\<\/member\>**  
 **\<name\= del membro„M:SomeClass.SomeOtherMethod\>**   
 **\<summary\>**  
 **Altro metodo.  \<\/summary\>**  
 **\<returns\>**  
 **I risultati restituiti vengono descritti tramite il tag returns.\<\/returns\>**  
 **\<cref\= di seealso„M:SomeClass.SomeMethod \(System.String\)„\>**   
 **Si noti l'utilizzo dell'attributo cref per fare riferimento a un metodo specifico \<\/seealso\>**  
 **\<\/member\>**  
 **\<name\= del membro„M:SomeClass.Main System.String \(\[\]\)„\>**   
 **\<summary\>**  
 **Punto di ingresso per l'applicazione.  \<\/summary\>**  
 **\<name\= " argomenti di tipo„ param\> Un elenco della riga di comando arguments\<\/param\>**  
 **\<\/member\>**  
 **\<name\= del membro„P:SomeClass.Name\>**   
 **\<summary\>**  
 **proprietà \<\/summary\> di nome**  
 **\<value\>**  
 **Un tag di valore viene utilizzato per descrivere la proprietà value\<\/value\>**  
 **\<\/member\>**  
 **\<\/members\>**  
**\<\/doc\>**    
## Compilazione del codice  
 Per compilare l'esempio, digitare la riga di comando seguente:  
  
 `csc XMLsample.cs /doc:XMLsample.xml`  
  
 Verrà creato il file XML XMLsample.xml, che è possibile visualizzare nel browser o tramite il comando di TYPE.  
  
## Programmazione efficiente  
 La documentazione XML inizia con \/\/\/.  Quando si crea un nuovo progetto, le procedure guidate impongono alcune linee \/\/\/iniziali in per l'utente.  L'elaborazione di questi commenti è regolata da alcune restrizioni:  
  
-   La documentazione deve essere utilizzare formato XML corretto.  Se il formato XML non è corretto, viene visualizzato un avviso viene generato l'evento e il file di documentazione conterrà un commento per informare che si è verificato un errore.  
  
-   Gli sviluppatori sono liberi di creare set di tag personalizzati.  Esiste un set di tag consigliato \(vedere la sezione di un ulteriore lettura\).  Alcuni dei tag consigliati hanno un significato speciale:  
  
    -   Il tag \<param\> viene utilizzato per descrivere i parametri.  Se utilizzato, il compilatore verifica l'esistenza del parametro e che tutti i parametri siano descritti nella documentazione.  Se la verifica ha esito negativo, il compilatore genera un avviso.  
  
    -   L'attributo `cref` può essere associato a qualsiasi tag per fornire un riferimento a un elemento del codice.  Il compilatore verifica dell'elemento del codice esistente.  Se la verifica ha esito negativo, il compilatore genera un avviso.  Il compilatore rispetta eventuali istruzioni `using` quando esegue la ricerca di un tipo descritto nell'attributo `cref`.  
  
    -   Il tag \<summary\> è utilizzato da IntelliSense in Visual Studio per visualizzare ulteriori informazioni su un tipo o membro.  
  
        > [!NOTE]
        >  Il file XML non fornisce informazioni complete sul tipo e i membri \(ad esempio, non contiene alcuna informazione sul tipo.  Per ottenere informazioni complete su un tipo o su un membro, è necessario utilizzare il file di documentazione con reflection sul tipo o sul membro effettivo.  
  
## Vedere anche  
 [Guida per programmatori C\#](../../../csharp/programming-guide/index.md)   
 [\/doc \(Process Documentation Comments\)](../../../csharp/language-reference/compiler-options/doc-compiler-option.md)   
 [Commenti relativi alla documentazione XML](../../../csharp/programming-guide/xmldoc/xml-documentation-comments.md)