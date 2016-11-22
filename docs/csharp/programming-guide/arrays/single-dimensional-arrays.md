---
title: "Matrici unidimensionali (Guida per programmatori C#) | Microsoft Docs"
ms.custom: ""
ms.date: "11/17/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "matrici [C#], unidimensionali"
  - "matrici unidimensionali [C#]"
ms.assetid: 2cec1196-1de0-49d2-baf2-c607c33310e8
caps.latest.revision: 18
caps.handback.revision: 18
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# Matrici unidimensionali (Guida per programmatori C#)
È possibile dichiarare una matrice unidimensionale composta da cinque interi, come illustrato nell'esempio che segue:  
  
 [!CODE [csProgGuideArrays#4](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#4)]  
  
 Questa matrice contiene gli elementi da `array[0]` a `array[4]` compresi.  L'operatore [new](../../../csharp/language-reference/keywords/new.md) viene utilizzato per creare la matrice e inizializzarne gli elementi con i corrispondenti valori predefiniti.  In questo esempio tutti gli elementi della matrice sono inizializzati a zero.  
  
 Allo stesso modo è possibile dichiarare una matrice contenente elementi stringa.  Di seguito è riportato un esempio:  
  
 [!CODE [csProgGuideArrays#5](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#5)]  
  
## Inizializzazione di una matrice  
 È possibile inizializzare una matrice al momento della dichiarazione, nel qual caso non è necessario specificarne il numero di dimensioni, in quanto è già fornito dal numero di elementi presente nell'elenco di inizializzazione.  Di seguito è riportato un esempio:  
  
 [!CODE [csProgGuideArrays#6](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#6)]  
  
 Allo stesso modo, è possibile inizializzare una matrice di stringhe.  Di seguito è illustrata la dichiarazione di una matrice di stringhe in cui ciascun elemento della matrice è inizializzato con il nome di un giorno della settimana:  
  
 [!CODE [csProgGuideArrays#7](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#7)]  
  
 Quando si inizializza una matrice al momento della dichiarazione, è possibile utilizzare le seguenti abbreviazioni:  
  
 [!CODE [csProgGuideArrays#8](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#8)]  
  
 È possibile dichiarare una variabile di matrice senza inizializzazione, ma sarà necessario utilizzare l'operatore `new` quando si assegna una matrice a questa variabile.  Di seguito è riportato un esempio:  
  
 [!CODE [csProgGuideArrays#9](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#9)]  
  
 In C\# 3.0 vengono introdotte le matrici tipizzate in modo implicito.  Per ulteriori informazioni, vedere [Matrici tipizzate in modo implicito](../../../csharp/programming-guide/arrays/implicitly-typed-arrays.md).  
  
## Matrici di tipo valore e di tipo riferimento  
 Si consideri la seguente dichiarazione di matrice:  
  
 [!CODE [csProgGuideArrays#10](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#10)]  
  
 Il risultato di questa istruzione è diverso a seconda che `SomeType` sia un tipo di valore o un tipo di riferimento.  Se si tratta di un tipo valore, l'istruzione crea una matrice di 10 elementi, ciascuno del tipo `SomeType`.  Se `SomeType` è un tipo di riferimento, l'istruzione creerà una matrice di 10 elementi, ciascuno dei quali verrà inizializzato con un riferimento a null.  
  
 Per ulteriori informazioni sui tipi valore e sui tipi riferimento, vedere [Tipi](../../../csharp/language-reference/keywords/types.md).  
  
## Vedere anche  
 <xref:System.Array>   
 [Guida per programmatori C\#](../../../csharp/programming-guide/index.md)   
 [Matrici](../../../csharp/programming-guide/arrays/index.md)   
 [Matrici multidimensionali](../../../csharp/programming-guide/arrays/multidimensional-arrays.md)   
 [Matrici irregolari](../../../csharp/programming-guide/arrays/jagged-arrays.md)