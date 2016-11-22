---
title: "&lt;paramref&gt; (Visual Basic) | Microsoft Docs"
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
  - "paramref XML tag"
  - "<paramref> XML tag"
ms.assetid: 8979d53b-beb1-41b7-b41e-6bbea1c17a03
caps.latest.revision: 9
caps.handback.revision: 9
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translationtype: Human Translation
---
# &lt;paramref&gt; (Visual Basic)
Formatta una parola come parametro.  
  
## Sintassi  
  
```  
<paramref name="name"/>  
```  
  
#### Parametri  
 `name`  
 Nome del parametro a cui fare riferimento.  Racchiudere il nome tra virgolette doppie \(" "\).  
  
## Note  
 Il tag `<paramref>` consente di indicare che una parola è un parametro.  Il file XML può essere elaborato in modo da formattare il parametro in maniera specifica.  
  
 Eseguire la compilazione con [\/doc](../../../visual-basic/reference/command-line-compiler/doc.md) per elaborare in un file i commenti relativi alla documentazione.  
  
## Esempio  
 In questo esempio il tag `<paramref>` viene utilizzato per fare riferimento al parametro `id`.  
  
 [!CODE [VbVbcnXmlDocComments#6](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnXmlDocComments#6)]  
  
## Vedere anche  
 [XML Comment Tags](../../../visual-basic/language-reference/xmldoc/recommended-xml-tags-for-documentation-comments.md)