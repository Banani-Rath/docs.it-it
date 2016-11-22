---
title: "&lt;paramref&gt; (Guida per programmatori C#) | Microsoft Docs"
ms.custom: ""
ms.date: "11/16/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "paramref"
  - "<paramref>"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "<paramref> (tag XML C#)"
  - "paramref (tag XML C#)"
ms.assetid: 756c24c1-f591-40e8-a838-559761539b0b
caps.latest.revision: 12
caps.handback.revision: 12
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# &lt;paramref&gt; (Guida per programmatori C#)
## Sintassi  
  
```  
<paramref name="name"/>  
```  
  
#### Parametri  
 `name`  
 Nome del parametro a cui fare riferimento.  Racchiudere il nome tra virgolette doppie \(" "\).  
  
## Note  
 Il tag \<paramref\> consente di indicare che una parola nei commenti del codice, ad esempio in un blocco \<summary\> o \<remarks\>, fa riferimento a un parametro.  È possibile elaborare il file XML in modo da formattare tale parola in modo specifico, ad esempio in grassetto o corsivo.  
  
 Eseguire la compilazione con [\/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) per elaborare in un file i commenti per la creazione della documentazione.  
  
## Esempio  
 [!CODE [csProgGuideDocComments#7](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideDocComments#7)]  
  
## Vedere anche  
 [Guida per programmatori C\#](../../../csharp/programming-guide/index.md)   
 [Tag consigliati per i commenti relativi alla documentazione](../../../csharp/programming-guide/xmldoc/recommended-tags-for-documentation-comments.md)