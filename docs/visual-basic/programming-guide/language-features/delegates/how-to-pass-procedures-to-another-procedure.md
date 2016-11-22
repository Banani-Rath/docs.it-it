---
title: "How to: Pass Procedures to Another Procedure in Visual Basic | Microsoft Docs"
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
  - "AddressOf operator"
  - "delegates [Visual Basic], passing procedures"
ms.assetid: 5adbba15-5a1d-413f-ab3e-3ff6cc0a4669
caps.latest.revision: 9
caps.handback.revision: 9
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translationtype: Human Translation
---
# How to: Pass Procedures to Another Procedure in Visual Basic
Nell'esempio riportato di seguito viene illustrato come passare una routine a un'altra routine con l'ausilio dei delegati.  
  
 Un delegato è un tipo che è possibile utilizzare come qualsiasi altro tipo in [!INCLUDE[vbprvb](../../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)].  Quando viene applicato a un nome di routine, l'operatore `AddressOf` restituisce un oggetto delegato.  
  
 Nell'esempio riportato di seguito viene illustrata una routine a cui è associato un delegato come parametro che può accettare un riferimento a un'altra routine e viene ottenuto con l'operatore `AddressOf`.  
  
### Per creare il delegato e le routine corrispondenti  
  
1.  Creare un delegato denominato `MathOperator`.  
  
     [!CODE [VbVbalrDelegates#1](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrDelegates#1)]  
  
2.  Creare una routine denominata `AddNumbers` con parametri e valore restituito corrispondenti a quelli di `MathOperator`, in modo che le firme coincidano.  
  
     [!CODE [VbVbalrDelegates#2](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrDelegates#2)]  
  
3.  Creare una routine denominata `SubtractNumbers` con una firma corrispondente a `MathOperator`.  
  
     [!CODE [VbVbalrDelegates#3](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrDelegates#3)]  
  
4.  Creare una routine denominata `DelegateTest` che accetta un delegato come parametro.  
  
     Questa routine può accettare un riferimento a `AddNumbers` o a `SubtractNumbers` poiché le relative firme corrispondono alla firma `MathOperator`.  
  
     [!CODE [VbVbalrDelegates#4](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrDelegates#4)]  
  
5.  Creare una routine denominata `Test` che chiama `DelegateTest` una volta utilizzando come parametro il delegato per `AddNumbers` e un'altra volta utilizzando come parametro il delegato per `SubtractNumbers`.  
  
     [!CODE [VbVbalrDelegates#5](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrDelegates#5)]  
  
     Quando viene chiamata, la routine `Test` visualizza innanzitutto il risultato della routine `AddNumbers` applicata a `5` e `3`, ovvero 8.  Quindi viene visualizzato il risultato di `SubtractNumbers` applicato a `9` e `3`, ovvero 6.  
  
## Vedere anche  
 [Delegates](../../../../visual-basic/programming-guide/language-features/delegates/delegates.md)   
 [AddressOf Operator](../../../../visual-basic/language-reference/operators/addressof-operator.md)   
 [Delegate Statement](../../../../visual-basic/language-reference/statements/delegate-statement.md)   
 [How to: Invoke a Delegate Method](../../../../visual-basic/programming-guide/language-features/delegates/how-to-invoke-a-delegate-method.md)