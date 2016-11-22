---
title: "Passaggio di matrici come argomenti (Guida per programmatori C#) | Microsoft Docs"
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
  - "matrici [C#], passaggio come argomenti"
ms.assetid: f3a0971e-c87c-4a1f-8262-bc0a3b712772
caps.latest.revision: 21
caps.handback.revision: 21
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# Passaggio di matrici come argomenti (Guida per programmatori C#)
Le matrici possono essere passate come argomenti ai parametri di metodo.  Le matrici sono infatti tipi di parametri, pertanto il metodo può modificare il valore degli elementi.  
  
## Passaggio di matrici unidimensionali come parametri  
 È possibile passare una matrice unidimensionale inizializzata a un metodo.  L'istruzione seguente, ad esempio, invia una matrice a un metodo di stampa.  
  
 [!CODE [csProgGuideArrays#34](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#34)]  
  
 Nel codice seguente viene illustrata un'implementazione parziale del metodo di stampa.  
  
 [!CODE [csProgGuideArrays#33](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#33)]  
  
 È possibile inizializzare e passare una nuova matrice in un passaggio, come mostrato nell'esempio seguente.  
  
 [!CODE [CsProgGuideArrays#35](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#35)]  
  
## Esempio  
  
### Descrizione  
 Nell'esempio seguente, una matrice di stringhe viene inizializzata e passata come argomento a un metodo `PrintArray` per le stringhe.  Nel metodo vengono visualizzati gli elementi della matrice.  Vengono quindi chiamati i metodi `ChangeArray` e `ChangeArrayElement` per dimostrare che l'invio di un argomento di matrice per valore non impedisce le modifiche agli elementi della matrice.  
  
### Codice  
 [!CODE [csProgGuideArrays#30](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#30)]  
  
## Passaggio di matrici multidimensionali come parametri  
 Una matrice multidimensionale inizializzata viene passata a un metodo nello stesso modo di una matrice unidimensionale.  
  
 [!CODE [csProgGuideArrays#41](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#41)]  
  
 Nel codice seguente viene illustrata una dichiarazione parziale di un metodo di stampa che accetta una matrice bidimensionale come argomento.  
  
 [!CODE [csProgGuideArrays#36](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#36)]  
  
 È possibile inizializzare e passare una nuova matrice in un passaggio, come mostrato nell'esempio seguente.  
  
 [!CODE [csProgGuideArrays#32](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#32)]  
  
## Esempio  
  
### Descrizione  
 Nell'esempio seguente, una matrice bidimensionale di Integer viene inizializzata e passata al metodo `Print2DArray`.  Nel metodo vengono visualizzati gli elementi della matrice.  
  
### Codice  
 [!CODE [csProgGuideArrays#31](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#31)]  
  
## Vedere anche  
 [Guida per programmatori C\#](../../../csharp/programming-guide/index.md)   
 [Matrici](../../../csharp/programming-guide/arrays/index.md)   
 [Matrici unidimensionali](../../../csharp/programming-guide/arrays/single-dimensional-arrays.md)   
 [Matrici multidimensionali](../../../csharp/programming-guide/arrays/multidimensional-arrays.md)   
 [Matrici irregolari](../../../csharp/programming-guide/arrays/jagged-arrays.md)