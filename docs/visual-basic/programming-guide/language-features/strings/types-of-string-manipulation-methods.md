---
title: "Types of String Manipulation Methods in Visual Basic | Microsoft Docs"
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
  - "strings [Visual Basic], manipulating [Visual Basic]"
  - "string manipulation"
ms.assetid: 905055cd-7f50-48fb-9eed-b0995af1dc1f
caps.latest.revision: 12
caps.handback.revision: 12
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translationtype: Human Translation
---
# Types of String Manipulation Methods in Visual Basic
Esistono vari modi di analizzare e modificare le stringhe.  Alcuni di essi fanno parte del linguaggio [!INCLUDE[vbprvb](../../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)], altri sono intrinseci alla classe `String`.  
  
## Linguaggio Visual Basic e .NET Framework  
 I metodi [!INCLUDE[vbprvb](../../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)] sono utilizzati come funzioni intrinseche del linguaggio e  non necessitano di una qualifica nel codice.  Nell'esempio seguente è illustrato il tipico utilizzo di un comando di gestione delle stringhe di [!INCLUDE[vbprvb](../../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)]:  
  
 [!CODE [VbVbalrStrings#44](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStrings#44)]  
  
 In questo esempio, attraverso la funzione `Mid` viene eseguita un'operazione diretta su `aString` e viene assegnato il valore a `bString`.  
  
 Per un elenco dei metodi per la gestione delle stringhe in Visual Basic, vedere [String Manipulation Summary](../../../../visual-basic/language-reference/keywords/string-manipulation-summary.md).  
  
### Metodi condivisi e di istanza  
 È inoltre possibile modificare le stringhe con i metodi della classe `String`.  Esistono due tipi di metodi in `String`: metodi *condivisi* e metodi *di istanza*.  
  
#### Metodi condivisi  
 Un metodo condiviso è un metodo che ha origine dalla classe `String` e che non necessita di un'istanza di tale classe per funzionare.  Questi metodi possono essere qualificati con il nome della classe \(`String`\) invece che con un'istanza della classe `String`.  Di seguito è riportato un esempio:  
  
 [!CODE [VbVbalrStrings#45](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStrings#45)]  
  
 Nell'esempio precedente, il metodo <xref:System.String.Copy%2A?displayProperty=fullName> è un metodo statico che agisce su un'espressione fornita e che assegna il valore risultante a `bString`.  
  
#### Metodi di istanza  
 I metodi di istanza, invece, hanno origine da un'istanza particolare di `String` ed è necessario qualificarli con il nome dell'istanza.  Di seguito è riportato un esempio:  
  
 [!CODE [VbVbalrStrings#46](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStrings#46)]  
  
 In questo esempio, il metodo <xref:System.String.Substring%2A?displayProperty=fullName> è un metodo dell'istanza di `String`, vale a dire `aString`.  Esso consente di eseguire un'operazione su `aString` e di assegnarne il valore a `bString`.  
  
 Per ulteriori informazioni, vedere la documentazione relativa alla classe <xref:System.String>.  
  
## Vedere anche  
 [Introduction to Strings in Visual Basic](../../../../visual-basic/programming-guide/language-features/strings/introduction-to-strings.md)