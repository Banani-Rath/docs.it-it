---
title: "How to: Define a Conversion Operator (Visual Basic) | Microsoft Docs"
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
  - "procedures, defining"
  - "operators [Visual Basic], defining"
  - "procedures, operator"
  - "operators [Visual Basic], overloading"
  - "return values, Operator procedures"
  - "operator overloading"
ms.assetid: 54203dfa-c24b-463f-9942-d5153e89e762
caps.latest.revision: 14
caps.handback.revision: 14
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translationtype: Human Translation
---
# How to: Define a Conversion Operator (Visual Basic)
Una volta definita una classe o una struttura, è possibile definire gli operatori di conversione dei tipi tra il tipo della classe o della struttura e un altro tipo di dati \(ad esempio `Integer`, `Double` o `String`\).  
  
 Definire la conversione dei tipi come routine [Funzione CType](../../../../visual-basic/language-reference/functions/ctype-function.md) all'interno della classe o della struttura.  Tutte le routine di conversione devono essere `Public Shared` e ognuna deve specificare [Widening](../../../../visual-basic/language-reference/modifiers/widening.md) oppure [Narrowing](../../../../visual-basic/language-reference/modifiers/narrowing.md).  
  
 La definizione di un operatore su una classe o una struttura viene anche detta *overload* dell'operatore.  
  
## Esempio  
 Nell'esempio riportato di seguito vengono definiti gli operatori di conversione tra una struttura denominata `digit` e un `Byte`.  
  
 [!CODE [VbVbcnProcedures#27](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnProcedures#27)]  
  
 È possibile testare la struttura `digit` mediante il codice riportato di seguito.  
  
 [!CODE [VbVbcnProcedures#28](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnProcedures#28)]  
  
## Vedere anche  
 [Operator Procedures](../../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md)   
 [How to: Define an Operator](../../../../visual-basic/programming-guide/language-features/procedures/how-to-define-an-operator.md)   
 [How to: Call an Operator Procedure](../../../../visual-basic/programming-guide/language-features/procedures/how-to-call-an-operator-procedure.md)   
 [How to: Use a Class that Defines Operators](../../../../visual-basic/programming-guide/language-features/procedures/how-to-use-a-class-that-defines-operators.md)   
 [Operator Statement](../../../../visual-basic/language-reference/statements/operator-statement.md)   
 [Structure Statement](../../../../visual-basic/language-reference/statements/structure-statement.md)   
 [How to: Declare a Structure](../../../../visual-basic/programming-guide/language-features/data-types/how-to-declare-a-structure.md)   
 [Implicit and Explicit Conversions](../../../../visual-basic/programming-guide/language-features/data-types/implicit-and-explicit-conversions.md)   
 [Widening and Narrowing Conversions](../../../../visual-basic/programming-guide/language-features/data-types/widening-and-narrowing-conversions.md)