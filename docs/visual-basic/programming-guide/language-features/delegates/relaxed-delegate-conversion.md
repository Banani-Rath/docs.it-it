---
title: "Relaxed Delegate Conversion (Visual Basic) | Microsoft Docs"
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
  - "relaxed delegate conversion [Visual Basic]"
  - "delegates [Visual Basic], relaxed conversion"
  - "conversions, relaxed delegate"
ms.assetid: 64f371d0-5416-4f65-b23b-adcbf556e81c
caps.latest.revision: 19
caps.handback.revision: 19
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translationtype: Human Translation
---
# Relaxed Delegate Conversion (Visual Basic)
La conversione di tipo relaxed del delegato consente di assegnare subroutine e funzioni a delegati o gestori anche quando le firme non sono identiche. Pertanto, l'associazione ai delegati diventa coerente con l'associazione già consentita nelle chiamate ai metodi.  
  
## Parametri e tipo restituito  
 Al posto della corrispondenza esatta delle firme, la conversione relaxed richiede il rispetto delle condizioni seguenti quando l'oggetto `Option Strict` è impostato su `On`:  
  
-   Una conversione verso un tipo di dati più grande è possibile dal tipo di dati di ogni parametro del delegato al tipo di dati del parametro corrispondente della funzione assegnata o `Sub`.  Nell'esempio seguente, il delegato `Del1` dispone di un parametro, ovvero di un oggetto `Integer`.  Il parametro `m` nelle espressioni lambda assegnate deve avere un tipo di dati per il quale vi sia una conversione verso un tipo di dati più grande da `Integer`, ad esempio `Long` o `Double`.  
  
     [!CODE [VbVbalrRelaxedDelegates#1](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrRelaxedDelegates#1)]  
  
     [!CODE [VbVbalrRelaxedDelegates#2](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrRelaxedDelegates#2)]  
  
     Le conversioni verso un tipo di dati più piccolo sono consentite solo quando `Option Strict` è impostato su `Off`.  
  
     [!CODE [VbVbalrRelaxedDelegates#8](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrRelaxedDelegates#8)]  
  
-   Una conversione verso un tipo di dati più grande è possibile nella direzione opposta dal tipo restituito della funzione assegnata o `Sub` al tipo restituito del delegato.  Negli esempi seguenti, il corpo di ogni espressione lambda assegnata deve restituire un tipo di dati che viene convertito verso il tipo più grande `Integer` poiché il tipo restituito dell'oggetto `del1` è `Integer`.  
  
     [!CODE [VbVbalrRelaxedDelegates#3](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrRelaxedDelegates#3)]  
  
 Se `Option Strict` è impostato su `Off`, la restrizione per la conversione verso un tipo di dati più grande viene rimossa in entrambe le direzioni.  
  
 [!CODE [VbVbalrRelaxedDelegates#4](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrRelaxedDelegates#4)]  
  
## Omissione delle specifiche dei parametri  
 I delegati di tipo relaxed consentono inoltre di omettere completamente le specifiche dei parametri nel metodo assegnato:  
  
 [!CODE [VbVbalrRelaxedDelegates#5](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrRelaxedDelegates#5)]  
  
 [!CODE [VbVbalrRelaxedDelegates#6](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrRelaxedDelegates#6)]  
  
 Tenere presente che non è possibile specificare alcuni parametri e ometterne altri.  
  
 [!CODE [VbVbalrRelaxedDelegates#15](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrRelaxedDelegates#15)]  
  
 La possibilità di omettere i parametri è utile in una situazione quale la definizione di un gestore eventi, in cui sono implicati vari parametri complessi.  Gli argomenti per alcuni gestori eventi non sono utilizzati.  Invece, il gestore accede direttamente allo stato del controllo nel quale l'evento è registrato e ignora gli argomenti.  I delegati di tipo relaxed consentono di omettere gli argomenti in tali dichiarazioni quando non risultano ambiguità.  Nell'esempio seguente, il metodo `OnClick` pienamente specificato può essere riscritto come `RelaxedOnClick`.  
  
```vb#  
Sub OnClick(ByVal sender As Object, ByVal e As EventArgs) Handles b.Click  
    MessageBox.Show("Hello World from" + b.Text)  
End Sub  
  
Sub RelaxedOnClick() Handles b.Click  
    MessageBox.Show("Hello World from" + b.Text)  
End Sub  
```  
  
## Esempi di AddressOf  
 Le espressioni lambda vengono utilizzate negli esempi precedenti per rendere facilmente individuabili le relazioni dei tipi.  Tuttavia, le stesse conversioni di tipo relaxed sono consentite per le assegnazioni del delegato che utilizzano `AddressOf`, `Handles` o `AddHandler`.  
  
 Nell'esempio seguente le funzioni `f1`, `f2`, `f3` e `f4` possono essere tutte assegnate a `Del1`.  
  
 [!CODE [VbVbalrRelaxedDelegates#1](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrRelaxedDelegates#1)]  
  
 [!CODE [VbVbalrRelaxedDelegates#7](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrRelaxedDelegates#7)]  
  
 [!CODE [VbVbalrRelaxedDelegates#9](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrRelaxedDelegates#9)]  
  
 L'esempio seguente è valido solo quando `Option Strict` è impostato su `Off`.  
  
 [!CODE [VbVbalrRelaxedDelegates#14](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrRelaxedDelegates#14)]  
  
## Eliminazione dei risultati delle funzioni  
 La conversione di tipo relaxed del delegato consente di assegnare una funzione a un delegato `Sub`, ignorando efficacemente il valore restituito della funzione.  Tuttavia, non è possibile assegnare una `Sub` a un delegato della funzione.  Nell'esempio seguente, l'indirizzo della funzione `doubler` viene assegnato al delegato `Sub` `Del3`.  
  
 [!CODE [VbVbalrRelaxedDelegates#10](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrRelaxedDelegates#10)]  
  
 [!CODE [VbVbalrRelaxedDelegates#11](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrRelaxedDelegates#11)]  
  
## Vedere anche  
 [Lambda Expressions](../../../../visual-basic/programming-guide/language-features/procedures/lambda-expressions.md)   
 [Widening and Narrowing Conversions](../../../../visual-basic/programming-guide/language-features/data-types/widening-and-narrowing-conversions.md)   
 [Delegates](../../../../visual-basic/programming-guide/language-features/delegates/delegates.md)   
 [How to: Pass Procedures to Another Procedure in Visual Basic](../../../../visual-basic/programming-guide/language-features/delegates/how-to-pass-procedures-to-another-procedure.md)   
 [Local Type Inference](../../../../visual-basic/programming-guide/language-features/variables/local-type-inference.md)   
 [Option Strict Statement](../../../../visual-basic/language-reference/statements/option-strict-statement.md)