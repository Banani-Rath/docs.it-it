---
title: "How to: Get a Value from a Property (Visual Basic) | Microsoft Docs"
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
  - "property values"
  - "Visual Basic code, procedures"
  - "values, properties"
  - "Visual Basic code, properties"
  - "properties [Visual Basic], values"
ms.assetid: 3954423e-6ab7-4a4c-b55c-a8d27be47891
caps.latest.revision: 11
caps.handback.revision: 11
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translationtype: Human Translation
---
# How to: Get a Value from a Property (Visual Basic)
Per recuperare il valore di una proprietà, includerne il nome in un'espressione.  
  
 La routine `Get` della proprietà recupera il valore, ma questo non viene chiamato esplicitamente per nome.  È possibile utilizzare la proprietà esattamente come si utilizzerebbe una variabile.  [!INCLUDE[vbprvb](../../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)] effettua le chiamate alle routine della proprietà.  
  
### Per recuperare un valore da una proprietà  
  
1.  Utilizzare il nome della proprietà in un'espressione in modo analogo al nome di una variabile.  È possibile utilizzare una proprietà in tutti i contesti in cui è consentito l'utilizzo di una variabile o di una costante.  
  
     In alternativa  
  
     Utilizzare il nome della proprietà che segue il segno di uguale \(`=`\) in un'istruzione di assegnazione.  
  
     Nell'esempio riportato di seguito viene letto il valore della proprietà `Now` di [!INCLUDE[vbprvb](../../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)] chiamando in modo implicito la rispettiva routine `Get`.  
  
     [!CODE [VbVbalrDateProperties#4](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrDateProperties#4)]  
  
2.  Se la proprietà accetta argomenti, far seguire il nome della proprietà da parentesi tra cui racchiudere l'elenco di argomenti.  Se non sono presenti argomenti, è possibile omettere le parentesi.  
  
3.  Racchiudere gli argomenti dell'elenco tra parentesi, separati da virgole.  Verificare di inserire gli argomenti nello stesso ordine con cui la proprietà definisce i parametri corrispondenti.  
  
 Il valore della proprietà viene utilizzato nell'espressione con le stesse modalità di una variabile o costante e viene quindi memorizzato nella variabile o proprietà a sinistra dell'istruzione di assegnazione.  
  
## Vedere anche  
 [Procedures](../../../../visual-basic/programming-guide/language-features/procedures/index.md)   
 [Routine Property](../../../../visual-basic/programming-guide/language-features/procedures/property-procedures.md)   
 [Procedure Parameters and Arguments](../../../../visual-basic/programming-guide/language-features/procedures/procedure-parameters-and-arguments.md)   
 [Property Statement](../../../../visual-basic/language-reference/statements/property-statement.md)   
 [Differences Between Properties and Variables in Visual Basic](../../../../visual-basic/programming-guide/language-features/procedures/differences-between-properties-and-variables.md)   
 [How to: Create a Property](../../../../visual-basic/programming-guide/language-features/procedures/how-to-create-a-property.md)   
 [How to: Declare a Property with Mixed Access Levels](../../../../visual-basic/programming-guide/language-features/procedures/how-to-declare-a-property-with-mixed-access-levels.md)   
 [How to: Call a Property Procedure](../../../../visual-basic/programming-guide/language-features/procedures/how-to-call-a-property-procedure.md)   
 [How to: Declare and Call a Default Property in Visual Basic](../../../../visual-basic/programming-guide/language-features/procedures/how-to-declare-and-call-a-default-property.md)   
 [How to: Put a Value in a Property](../../../../visual-basic/programming-guide/language-features/procedures/how-to-put-a-value-in-a-property.md)