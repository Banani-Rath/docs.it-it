---
title: "Nothing and Strings in Visual Basic | Microsoft Docs"
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
  - "strings [Visual Basic], Nothing"
ms.assetid: 261380af-2024-4ecf-823b-43b1034d92cd
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translationtype: Human Translation
---
# Nothing and Strings in Visual Basic
Il runtime di [!INCLUDE[vbprvb](../../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)] e [!INCLUDE[dnprdnshort](../../../../csharp/getting-started/includes/dnprdnshort_md.md)] valutano `Nothing` in modo diverso quando si lavora con stringhe.  
  
## Visual Basic Runtime e .NET Framework  
 Si consideri l'esempio seguente:  
  
 [!CODE [VbVbalrStrings#47](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStrings#47)]  
  
 Il runtime di [!INCLUDE[vbprvb](../../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)] in genere valuta `Nothing` come una stringa vuota \(""\).  [!INCLUDE[dnprdnshort](../../../../csharp/getting-started/includes/dnprdnshort_md.md)] si comporta diversamente e genera un'eccezione ogni volta che si cerca di eseguire un'operazione stringa su `Nothing`.  
  
## Vedere anche  
 [Introduction to Strings in Visual Basic](../../../../visual-basic/programming-guide/language-features/strings/introduction-to-strings.md)