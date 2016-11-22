---
title: "params (Riferimenti per C#) | Microsoft Docs"
ms.custom: ""
ms.date: "11/17/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "params_CSharpKeyword"
  - "params"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "parametri [C#], params"
  - "params (parola chiave) [C#]"
ms.assetid: 1690815e-b52b-4967-8380-5780aff08012
caps.latest.revision: 24
caps.handback.revision: 24
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# params (Riferimenti per C#)
Utilizzando la parola chiave `params`, è possibile specificare un [parametro di metodo](../../../csharp/language-reference/keywords/method-parameters.md) che utilizza un numero variabile di argomenti.  
  
 È possibile inviare un elenco di argomenti separato da virgole del tipo specificato nella dichiarazione di parametri o una matrice di argomenti del tipo specificato.  È inoltre possibile non inviare alcun argomento.  Se non vengono inviati argomenti, la lunghezza dell'elenco `params` è zero.  
  
 In una dichiarazione di metodo non è possibile aggiungere ulteriori parametri dopo la parola chiave `params` ed è consentito l'uso di una sola parola chiave `params`.  
  
## Esempio  
 Nell'esempio seguente vengono dimostrate le varie modalità nelle quali è possibile inviare argomenti al parametro `params`.  
  
 [!CODE [csrefKeywordsMethodParams#5](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsMethodParams#5)]  
  
## Specifiche del linguaggio C\#  
 [!INCLUDE[CSharplangspec](../../../csharp/language-reference/keywords/includes/csharplangspec_md.md)]  
  
## Vedere anche  
 [Riferimenti per C\#](../../../csharp/language-reference/index.md)   
 [Guida per programmatori C\#](../../../csharp/programming-guide/index.md)   
 [Parole chiave di C\#](../../../csharp/language-reference/keywords/index.md)   
 [Parametri di metodo](../../../csharp/language-reference/keywords/method-parameters.md)