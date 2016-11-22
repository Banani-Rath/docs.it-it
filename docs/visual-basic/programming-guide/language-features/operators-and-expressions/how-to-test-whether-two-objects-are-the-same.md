---
title: "How to: Test Whether Two Objects Are the Same (Visual Basic) | Microsoft Docs"
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
  - "variables [Visual Basic], reference"
  - "Is operator [Visual Basic], comparing objects"
  - "reference variables"
  - "variables [Visual Basic], referring to same object"
  - "objects [Visual Basic], variables referring to same"
  - "Visual Basic code, operators"
ms.assetid: f760e828-8704-4256-bc2d-c22a4c93b524
caps.latest.revision: 11
caps.handback.revision: 11
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translationtype: Human Translation
---
# How to: Test Whether Two Objects Are the Same (Visual Basic)
Se si dispone di due variabili che fanno riferimento a degli oggetti, è possibile utilizzare l'operatore `Is` o `IsNot`, oppure entrambi, per stabilire se puntano alla stessa istanza.  
  
### Per verificare se due oggetti corrispondono  
  
-   Utilizzare l'operatore [Is Operator](../../../../visual-basic/language-reference/operators/is-operator.md) o [IsNot Operator](../../../../visual-basic/language-reference/operators/isnot-operator.md) con due variabili come operandi.  
  
     [!CODE [VbVbalrOperators#69](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrOperators#69)]  
  
 L'azione intrapresa dipende dal riferimento o meno alla stessa istanza da parte dei due oggetti.  Nell'esempio precedente viene confrontato il controllo `c` con il controllo attivo sul form `f`.  In assenza di controlli attivi, oppure se esiste un controllo attivo che tuttavia non corrisponde all'istanza del controllo specificata in `c`, l'istruzione `If` avrà esito negativo e verrà restituita la routine senza ulteriori elaborazioni.  
  
 L'utilizzo di `Is` o `IsNot` dipende dalle esigenze personali,  ad esempio potrebbe risultare più semplice leggere un operatore anziché l'altro in una determinata espressione.  
  
## Vedere anche  
 [Comparison Operators in Visual Basic](../../../../visual-basic/programming-guide/language-features/operators-and-expressions/comparison-operators.md)