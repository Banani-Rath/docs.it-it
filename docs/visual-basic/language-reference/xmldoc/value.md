---
title: "&lt;value&gt; (Visual Basic) | Microsoft Docs"
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
  - "<value> XML tag"
  - "value XML tag"
ms.assetid: 0b84b02e-9e6d-41b5-a926-0d5dc76dacb5
caps.latest.revision: 10
caps.handback.revision: 10
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translationtype: Human Translation
---
# &lt;value&gt; (Visual Basic)
Specifica la descrizione di una proprietà.  
  
## Sintassi  
  
```  
<value>property-description</value>  
```  
  
#### Parametri  
 `property-description`  
 Descrizione della proprietà.  
  
## Note  
 Il tag `<value>` consente di descrivere una proprietà.  Tenere presente che l'aggiunta di una proprietà mediante la creazione guidata di codice nell'ambiente di sviluppo di Visual Studio determina l'aggiunta di un tag [\<summary\>](../../../visual-basic/language-reference/xmldoc/summary.md) alla nuova proprietà.  È quindi necessario aggiungere manualmente un tag `<value>` per descrivere il valore rappresentato dalla proprietà.  
  
 Eseguire la compilazione con [\/doc](../../../visual-basic/reference/command-line-compiler/doc.md) per elaborare in un file i commenti relativi alla documentazione.  
  
## Esempio  
 Nell'esempio riportato di seguito il tag `<value>` viene utilizzato per descrivere il valore della proprietà `Counter`.  
  
 [!CODE [VbVbcnXmlDocComments#1](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnXmlDocComments#1)]  
  
## Vedere anche  
 [XML Comment Tags](../../../visual-basic/language-reference/xmldoc/recommended-xml-tags-for-documentation-comments.md)