---
title: ". Operatore (Riferimenti per C#) | Microsoft Docs"
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
  - "._CSharpKeyword"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - ". operatore [C#]"
  - "punto (.) (operatore) [C#]"
  - "operatore di accesso al membro (.) [C#]"
ms.assetid: a1f54b52-b686-4ae5-a48e-a2a9ebd0eb7b
caps.latest.revision: 21
caps.handback.revision: 21
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# . Operatore (Riferimenti per C#)
L'operatore punto \(`.`\) viene utilizzato per l'accesso ai membri.  L'operatore punto specifica un membro di un tipo o di uno spazio dei nomi.  Ad esempio, l'operatore punto viene utilizzato per accedere a metodi specifici all'interno delle librerie di classi di .NET Framework:  
  
 [!CODE [csRefOperators#16](../CodeSnippet/VS_Snippets_VBCSharp/csrefOperators#16)]  
  
 Si consideri ad esempio la seguente classe:  
  
 [!CODE [csRefOperators#17](../CodeSnippet/VS_Snippets_VBCSharp/csrefOperators#17)]  
  
 [!CODE [csRefOperators#18](../CodeSnippet/VS_Snippets_VBCSharp/csrefOperators#18)]  
  
 La variabile `s` ha due membri: `a` e `b`. Per accedervi, utilizzare l'operatore punto, come mostrato nell'esempio.  
  
 [!CODE [csRefOperators#19](../CodeSnippet/VS_Snippets_VBCSharp/csrefOperators#19)]  
  
 Il punto viene inoltre utilizzato per formare nomi completi, ovvero nomi che specificano, ad esempio, lo spazio dei nomi o l'interfaccia a cui appartengono.  
  
 [!CODE [csRefOperators#20](../CodeSnippet/VS_Snippets_VBCSharp/csrefOperators#20)]  
  
 La direttiva using rende facoltativa la qualificazione di alcuni nomi:  
  
 [!CODE [csRefOperators#21](../CodeSnippet/VS_Snippets_VBCSharp/csrefOperators#21)]  
  
 Tuttavia, se l'identificatore è ambiguo, dovrà essere qualificato:  
  
 [!CODE [csRefOperators#22](../CodeSnippet/VS_Snippets_VBCSharp/csrefOperators#22)]  
  
## Specifiche del linguaggio C\#  
 [!INCLUDE[CSharplangspec](../../../csharp/language-reference/keywords/includes/csharplangspec_md.md)]  
  
## Vedere anche  
 [Riferimenti per C\#](../../../csharp/language-reference/index.md)   
 [Guida per programmatori C\#](../../../csharp/programming-guide/index.md)   
 [Operatori](../../../csharp/language-reference/operators/index.md)