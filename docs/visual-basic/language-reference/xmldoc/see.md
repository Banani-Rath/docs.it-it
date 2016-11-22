---
title: "&lt;see&gt; (Visual Basic) | Microsoft Docs"
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
  - "see XML tag"
  - "<see> XML tag"
ms.assetid: 7e18f60b-ef4a-4678-a797-5eb918635ca9
caps.latest.revision: 10
caps.handback.revision: 10
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translationtype: Human Translation
---
# &lt;see&gt; (Visual Basic)
Specifica un collegamento a un altro membro.  
  
## Sintassi  
  
```  
<see cref="member"/>  
```  
  
#### Parametri  
 `member`  
 Riferimento a un membro o a un campo disponibile per essere chiamato dall'ambiente di compilazione corrente.  Il compilatore verifica l'esistenza dell'elemento di codice specificato e passa `member` al nome di elemento nel file XML di output.  Il parametro `member` deve essere visualizzato tra virgolette doppie \(" "\).  
  
## Note  
 Utilizzare il tag `<see>` per specificare un collegamento nel testo.  Utilizzare [\<seealso\>](../../../visual-basic/language-reference/xmldoc/seealso.md) per indicare il testo che si desidera visualizzare in una sezione "Vedere anche".  
  
 Eseguire la compilazione con [\/doc](../../../visual-basic/reference/command-line-compiler/doc.md) per elaborare in un file i commenti relativi alla documentazione.  
  
## Esempio  
 Nell'esempio riportato di seguito il tag `<see>` viene utilizzato nella sezione relativa alle osservazioni di `UpdateRecord` per fare riferimento al metodo `DoesRecordExist`.  
  
 [!CODE [VbVbcnXmlDocComments#6](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnXmlDocComments#6)]  
  
## Vedere anche  
 [XML Comment Tags](../../../visual-basic/language-reference/xmldoc/recommended-xml-tags-for-documentation-comments.md)