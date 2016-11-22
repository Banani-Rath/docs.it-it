---
title: "Passaggio di matrici mediante ref e out (Guida per programmatori C#) | Microsoft Docs"
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
  - "matrici [C#], passaggio mediante ref e out"
ms.assetid: 6a2b261e-a1cc-49a6-b4f0-6cacae385a1e
caps.latest.revision: 16
caps.handback.revision: 16
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# Passaggio di matrici mediante ref e out (Guida per programmatori C#)
Analogamente a tutti i parametri [out](../../../csharp/language-reference/keywords/out.md), anche il parametro `out` di un tipo di matrice deve essere assegnato prima dell'uso, ovvero assegnato dal chiamato.  Di seguito è riportato un esempio.  
  
 [!CODE [csProgGuideArrays#39](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#39)]  
  
 Come tutti i parametri [ref](../../../csharp/language-reference/keywords/ref.md), anche il parametro `ref` di un tipo di matrice deve essere assolutamente assegnato dal chiamante.  Non è pertanto necessario che venga assegnato dal chiamato.  Il parametro `ref` di un tipo di matrice può risultare modificato in conseguenza della chiamata.  È ad esempio possibile che alla matrice venga assegnato il valore [null](../../../csharp/language-reference/keywords/null.md) o che venga inizializzata con una matrice diversa.  Di seguito è riportato un esempio.  
  
 [!CODE [csProgGuideArrays#40](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#40)]  
  
 Nei due esempi che seguono viene illustrata la differenza tra `out` e `ref` quando vengono utilizzati per passare matrici a metodi.  
  
## Esempio  
 In questo esempio la matrice `theArray` viene dichiarata nel chiamante \(il metodo `Main`\) e inizializzata nel metodo `FillArray`.  Gli elementi vengono quindi restituiti al chiamante e visualizzati.  
  
 [!CODE [csProgGuideArrays#37](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#37)]  
  
## Esempio  
 In questo esempio la matrice `theArray` viene inizializzata nel chiamante \(il metodo `Main`\) e passata al metodo `FillArray` utilizzando il parametro `ref`.  Alcuni degli elementi della matrice vengono aggiornati nel metodo `FillArray`.  Gli elementi vengono quindi restituiti al chiamante e visualizzati.  
  
 [!CODE [csProgGuideArrays#38](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#38)]  
  
## Vedere anche  
 [ref](../../../csharp/language-reference/keywords/ref.md)   
 [Modificatore del parametro out](../../../csharp/language-reference/keywords/out-parameter-modifier.md)   
 [Guida per programmatori C\#](../../../csharp/programming-guide/index.md)   
 [Matrici](../../../csharp/programming-guide/arrays/index.md)   
 [Matrici unidimensionali](../../../csharp/programming-guide/arrays/single-dimensional-arrays.md)   
 [Matrici multidimensionali](../../../csharp/programming-guide/arrays/multidimensional-arrays.md)   
 [Matrici irregolari](../../../csharp/programming-guide/arrays/jagged-arrays.md)