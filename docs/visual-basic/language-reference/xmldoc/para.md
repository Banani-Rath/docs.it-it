---
title: "&lt;para&gt; (Visual Basic) | Microsoft Docs"
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
  - "<para> XML tag"
  - "para XML tag"
ms.assetid: a3a18b6c-6416-4358-94ec-37b22675fd37
caps.latest.revision: 9
caps.handback.revision: 9
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translationtype: Human Translation
---
# &lt;para&gt; (Visual Basic)
Specifica la formattazione del contenuto come paragrafo.  
  
## Sintassi  
  
```  
<para>content</para>  
```  
  
#### Parametri  
 `content`  
 Testo del paragrafo.  
  
## Note  
 Il tag `<para>` viene utilizzato all'interno di un tag, quale [\<summary\>](../../../visual-basic/language-reference/xmldoc/summary.md), [\<remarks\>](../../../visual-basic/language-reference/xmldoc/remarks.md) o [\<returns\>](../../../visual-basic/language-reference/xmldoc/returns.md) e consente di aggiungere struttura al testo.  
  
 Eseguire la compilazione con [\/doc](../../../visual-basic/reference/command-line-compiler/doc.md) per elaborare in un file i commenti relativi alla documentazione.  
  
## Esempio  
 Nell'esempio riportato di seguito il tag `<para>` viene utilizzato per suddividere la sezione delle osservazioni relativa al metodo `UpdateRecord` in due paragrafi.  
  
 [!CODE [VbVbcnXmlDocComments#6](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnXmlDocComments#6)]  
  
## Vedere anche  
 [XML Comment Tags](../../../visual-basic/language-reference/xmldoc/recommended-xml-tags-for-documentation-comments.md)