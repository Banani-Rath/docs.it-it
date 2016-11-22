---
title: "Matrici multidimensionali (Guida per programmatori C#) | Microsoft Docs"
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
  - "matrici [C#], multidimensionali"
  - "Matrici multidimensionali (C#)"
ms.assetid: 020ce02e-7dff-4273-8e53-bf0b33747232
caps.latest.revision: 16
caps.handback.revision: 16
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# Matrici multidimensionali (Guida per programmatori C#)
Le matrici possono avere più di una dimensione.  La dichiarazione che segue, ad esempio, crea una matrice bidimensionale di quattro righe e due colonne.  
  
 [!CODE [csProgGuideArrays#11](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#11)]  
  
 La dichiarazione che segue crea una matrice a tre dimensioni, 4, 2 e 3.  
  
 [!CODE [csProgGuideArrays#12](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#12)]  
  
## Inizializzazione di una matrice  
 È possibile inizializzare la matrice al momento della dichiarazione come illustrato nel seguente esempio.  
  
 [!CODE [csProgGuideArrays#13](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#13)]  
  
 È inoltre possibile inizializzare la matrice senza specificarne il numero di dimensioni.  
  
 [!CODE [csProgGuideArrays#14](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#14)]  
  
 Se si sceglie di dichiarare una variabile di matrice senza inizializzazione, sarà necessario utilizzare l'operatore `new` per assegnare una matrice alla variabile.  L'utilizzo di `new` è illustrato nell'esempio seguente.  
  
 [!CODE [csProgGuideArrays#15](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#15)]  
  
 Nell'esempio seguente viene assegnato un valore a un elemento specifico della matrice.  
  
 [!CODE [csProgGuideArrays#16](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#16)]  
  
 Analogamente, nell'esempio riportato di seguito viene ottenuto il valore di un elemento specifico di una matrice e viene assegnato alla variabile `elementValue`.  
  
 [!CODE [csProgGuideArrays#42](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#42)]  
  
 Nell'esempio di codice riportato di seguito gli elementi della matrice vengono inizializzati in base ai valori predefiniti, ad eccezione delle matrici irregolari.  
  
 [!CODE [csProgGuideArrays#17](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#17)]  
  
## Vedere anche  
 [Guida per programmatori C\#](../../../csharp/programming-guide/index.md)   
 [Matrici](../../../csharp/programming-guide/arrays/index.md)   
 [Matrici unidimensionali](../../../csharp/programming-guide/arrays/single-dimensional-arrays.md)   
 [Matrici irregolari](../../../csharp/programming-guide/arrays/jagged-arrays.md)