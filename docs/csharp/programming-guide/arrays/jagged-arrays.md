---
title: "Matrici irregolari (Guida per programmatori C#) | Microsoft Docs"
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
  - "matrici [C#], irregolari"
  - "matrici irregolari [C#]"
ms.assetid: 537c65a6-0e0a-4a00-a2b8-086f38519c70
caps.latest.revision: 24
caps.handback.revision: 24
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# Matrici irregolari (Guida per programmatori C#)
Una matrice di matrici è una matrice i cui elementi sono costituiti da matrici.  Gli elementi di una matrice irregolare possono presentare dimensioni e misure differenti.  Una matrice irregolare è anche detta "matrice di matrici". Negli esempi di codice riportati di seguito viene illustrato come dichiarare, inizializzare e accedere alle matrici irregolari.  
  
 Di seguito è riportata la dichiarazione di una matrice unidimensionale di tre elementi, ciascuno dei quali è una matrice unidimensionale di interi:  
  
 [!CODE [csProgGuideArrays#19](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#19)]  
  
 Per poter utilizzare `jaggedArray`, è necessario che i corrispondenti elementi siano stati inizializzati.  È possibile inizializzare gli elementi nel modo seguente:  
  
 [!CODE [csProgGuideArrays#20](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#20)]  
  
 Ciascuno degli elementi è costituito da una matrice unidimensionale di interi.  Il primo elemento è una matrice di 5 interi, il secondo una matrice di 4 interi e il terzo una matrice di 2 interi.  
  
 È anche possibile utilizzare inizializzatori per immettere i valori negli elementi delle matrici. In questo caso, non occorre conoscere la dimensione delle matrici.  Di seguito è riportato un esempio:  
  
 [!CODE [csProgGuideArrays#21](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#21)]  
  
 È inoltre possibile inizializzare la matrice al momento della dichiarazione, come nell'esempio che segue:  
  
 [!CODE [csProgGuideArrays#22](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#22)]  
  
 È possibile utilizzare la seguente forma abbreviata.  Si noti che è possibile omettere l'operatore `new` poiché non è prevista alcuna inizializzazione predefinita per gli elementi:  
  
 [!CODE [csProgGuideArrays#23](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#23)]  
  
 Gli elementi di una matrice irregolare sono tipi di riferimento inizializzati su `null`.  
  
 È possibile accedere a singoli elementi di una matrice, come negli esempi che seguono:  
  
 [!CODE [csProgGuideArrays#24](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#24)]  
  
 È possibile combinare matrici irregolari e matrici multidimensionali.  Di seguito sono riportate la dichiarazione e l'inizializzazione di una matrice irregolare unidimensionale che contiene tre elementi matrice bidimensionali con dimensioni diverse.  Per ulteriori informazioni sulle matrici bidimensionali, vedere [Matrici multidimensionali](../../../csharp/programming-guide/arrays/multidimensional-arrays.md).  
  
 [!CODE [csProgGuideArrays#25](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#25)]  
  
 È possibile accedere a singoli elementi, come illustrato in questo esempio, in cui viene visualizzato il valore dell'elemento `[1,0]` della prima matrice \(valore `5`\):  
  
 [!CODE [csProgGuideArrays#26](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#26)]  
  
 Il metodo `Length` restituisce il numero di matrici contenute nella matrice irregolare.  Si supponga, ad esempio, che sia stata dichiarata la matrice precedente. In questo caso, la riga  
  
 [!CODE [csProgGuideArrays#27](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#27)]  
  
 restituisce un valore di 3.  
  
## Esempio  
 In questo esempio viene compilata una matrice i cui elementi sono costituiti da matrici.  Ciascun elemento della matrice ha una dimensione differente.  
  
 [!CODE [csProgGuideArrays#18](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#18)]  
  
## Vedere anche  
 <xref:System.Array>   
 [Guida per programmatori C\#](../../../csharp/programming-guide/index.md)   
 [Matrici](../../../csharp/programming-guide/arrays/index.md)   
 [Matrici unidimensionali](../../../csharp/programming-guide/arrays/single-dimensional-arrays.md)   
 [Matrici multidimensionali](../../../csharp/programming-guide/arrays/multidimensional-arrays.md)