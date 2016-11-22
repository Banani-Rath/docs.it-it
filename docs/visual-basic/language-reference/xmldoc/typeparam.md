---
title: "&lt;typeparam&gt; (Visual Basic) | Microsoft Docs"
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
  - "typeparam XML tag"
  - "<typeparam> XML tag"
ms.assetid: 1bb5ba78-f060-478c-905c-77a2e43639af
caps.latest.revision: 9
caps.handback.revision: 9
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translationtype: Human Translation
---
# &lt;typeparam&gt; (Visual Basic)
Definisce un nome e una descrizione di un parametro di tipo.  
  
## Sintassi  
  
```  
<typeparam name="name">description</typeparam>  
```  
  
#### Parametri  
 `name`  
 Nome del parametro del tipo.  Racchiudere il nome tra virgolette doppie \(" "\).  
  
 `description`  
 Descrizione del parametro di tipo.  
  
## Note  
 Utilizzare il tag `<typeparam>` nel commento per una dichiarazione di tipo o membro generico per descrivere uno dei parametri di tipo.  
  
 Eseguire la compilazione con [\/doc](../../../visual-basic/reference/command-line-compiler/doc.md) per elaborare in un file i commenti relativi alla documentazione.  
  
## Esempio  
 In questo esempio il tag `<typeparam>` viene utilizzato per descrivere il parametro `id`.  
  
 [!CODE [VbVbcnXmlDocComments#8](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnXmlDocComments#8)]  
  
## Vedere anche  
 [XML Comment Tags](../../../visual-basic/language-reference/xmldoc/recommended-xml-tags-for-documentation-comments.md)