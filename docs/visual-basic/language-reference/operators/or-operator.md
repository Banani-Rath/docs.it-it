---
title: "Or Operator (Visual Basic) | Microsoft Docs"
ms.custom: ""
ms.date: "11/17/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vb.Or"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "Or operator"
  - "operators [Visual Basic], bitwise"
  - "inclusive Or operator"
  - "bitwise operators, OR operator"
  - "Or keyword"
  - "operators [Visual Basic], inclusive or"
  - "operators [Visual Basic], disjunction"
  - "bitwise comparison"
  - "logical disjunction"
  - "disjunction operator"
ms.assetid: 41ed6905-bf3d-468a-9e3b-03c10d461891
caps.latest.revision: 12
caps.handback.revision: 12
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translationtype: Human Translation
---
# Or Operator (Visual Basic)
Esegue una disgiunzione logica tra due espressioni `Boolean` oppure una disgiunzione bit per bit tra due espressioni numeriche.  
  
## Sintassi  
  
```  
  
result = expression1 Or expression2  
```  
  
## Parti  
 `result`  
 Obbligatorio.  Qualsiasi espressione `Boolean` o numerica.  Nel caso di un confronto tra valori `Boolean`, `result` rappresenta la disgiunzione logica inclusiva di due valori `Boolean`.  Nel caso di operazioni bit per bit, `result` è invece un valore numerico che rappresenta la disgiunzione bit per bit inclusiva di due schemi di bit numerici.  
  
 `expression1`  
 Obbligatorio.  Qualsiasi espressione `Boolean` o numerica.  
  
 `expression2`  
 Obbligatorio.  Qualsiasi espressione `Boolean` o numerica.  
  
## Note  
 Per un confronto tra valori `Boolean`, `result` è `False` soltanto se `expression1` ed `expression2` restituiscono entrambi `False`.  Nella tabella riportata di seguito viene illustrato come si determina il valore di `result`.  
  
|Se `expression1` è|Ed `expression2` è|Il valore di `result` sarà|  
|------------------------|------------------------|--------------------------------|  
|`True`|`True`|`True`|  
|`True`|`False`|`True`|  
|`False`|`True`|`True`|  
|`False`|`False`|`False`|  
  
> [!NOTE]
>  In un confronto tra valori `Boolean` l'operatore `Or` valuta sempre entrambe le espressioni, inclusa l'eventuale esecuzione di chiamate di routine.  L'[OrElse Operator](../../../visual-basic/language-reference/operators/orelse-operator.md) esegue un'operazione di *corto circuito*. In altri termini, se `expression1` è `True`, `expression2` non verrà valutata.  
  
 Nelle operazioni bit per bit l'operatore `Or` esegue un confronto bit per bit tra bit che occupano la stessa posizione in due espressioni numeriche e imposta il bit corrispondente in `result` in base ai valori riportati nella seguente tabella.  
  
|Se il bit nel parametro `expression1` è|E il bit in `expression2` è|Il bit in `result` sarà|  
|---------------------------------------------|---------------------------------|-----------------------------|  
|1|1|1|  
|1|0|1|  
|0|1|1|  
|0|0|0|  
  
> [!NOTE]
>  Poiché il livello di precedenza degli operatori logici e bit per bit è inferiore rispetto a quello degli operatori aritmetici e relazionali, è necessario racchiudere le operazioni bit per bit tra parentesi per garantire un'esecuzione accurata.  
  
## Tipi di dati  
 Se gli operandi sono costituiti da un'espressione `Boolean` e un'espressione numerica, l'espressione `Boolean` verrà convertita in un valore numerico \(–1 per `True` e 0 per `False`\) e verrà eseguita un'operazione bit per bit.  
  
 Nel caso di un confronto tra valori `Boolean` il tipo di dati del risultato sarà `Boolean`,  mentre per un confronto bit per bit il tipo di dati del risultato sarà un tipo numerico appropriato ai tipi di dati di `expression1` e `expression2`.  Per informazioni, vedere la tabella "Confronti relazionali e bit per bit" in [Data Types of Operator Results](../../../visual-basic/language-reference/operators/data-types-of-operator-results.md).  
  
## Overload  
 L'operatore `Or` può essere sottoposto a *overload*. In altri termini, una classe o una struttura può ridefinirne il comportamento quando un operando specifica il tipo di tale classe o struttura.  Se il codice utilizza l'operatore su una classe o una struttura di questo tipo, è importante comprendere il comportamento ridefinito di tale operatore.  Per ulteriori informazioni, vedere [Operator Procedures](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md).  
  
## Esempio  
 Nell'esempio riportato di seguito l'operatore `Or` viene utilizzato per eseguire una disgiunzione logica inclusiva tra due espressioni.  Il risultato è un valore `Boolean` che indica se una delle due espressioni è `True`.  
  
 [!CODE [VbVbalrOperators#35](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrOperators#35)]  
  
 I risultati ottenuti dall'esempio precedente sono rispettivamente `True`, `True` e `False`.  
  
## Esempio  
 Nell'esempio riportato di seguito l'operatore `Or` viene utilizzato per eseguire la disgiunzione logica inclusiva dei singoli bit di due espressioni numeriche.  Il bit nello schema dei risultati viene impostato se uno dei bit corrispondenti negli operandi è impostato su 1.  
  
 [!CODE [VbVbalrOperators#36](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrOperators#36)]  
  
 I risultati ottenuti dall'esempio precedente sono rispettivamente 10, 14 e 14.  
  
## Vedere anche  
 [Logical\/Bitwise Operators](../../../visual-basic/language-reference/operators/logical-bitwise-operators.md)   
 [Operator Precedence in Visual Basic](../../../visual-basic/language-reference/operators/operator-precedence.md)   
 [Operators Listed by Functionality](../../../visual-basic/language-reference/operators/operators-listed-by-functionality.md)   
 [OrElse Operator](../../../visual-basic/language-reference/operators/orelse-operator.md)   
 [Logical and Bitwise Operators in Visual Basic](../../../visual-basic/programming-guide/language-features/operators-and-expressions/logical-and-bitwise-operators.md)