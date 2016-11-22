---
title: "bool (Riferimenti per C#) | Microsoft Docs"
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
  - "bool_CSharpKeyword"
  - "bool"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "bool (parola chiave) [C#]"
ms.assetid: 551cfe35-2632-4343-af49-33ad12da08e2
caps.latest.revision: 30
caps.handback.revision: 30
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# bool (Riferimenti per C#)
La parola chiave `bool` è un alias di <xref:System.Boolean?displayProperty=fullName>.  Viene utilizzata per dichiarare variabili per archiviare i valori Boolean, [true](../../../csharp/language-reference/keywords/true.md) e [false](../../../csharp/language-reference/keywords/false.md).  
  
> [!NOTE]
>  Se è necessaria una variabile booleana che possa avere anche il valore `null`, utilizzare `bool?`.  Per ulteriori informazioni, vedere [Tipi nullable](../../../csharp/programming-guide/nullable-types/index.md).  
  
## Valori letterali  
 È possibile assegnare un valore Boolean a una variabile `bool`.  È inoltre possibile assegnare un'espressione che restituisce `bool` a una variabile `bool`.  
  
 [!CODE [csrefKeywordsTypes#1](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsTypes#1)]  
  
 Il valore predefinito di una variabile `bool` è `false`.  Il valore predefinito di una variabile `bool?` è `null`.  
  
## Conversioni  
 In C\+\+ un valore di tipo `bool` può essere convertito in un valore di tipo `int`. In altri termini, `false` è equivalente a zero e `true` è equivalente a valori diversi da zero.  In C\# non viene eseguita alcuna conversione tra il tipo `bool` e gli altri tipi.  Ad esempio, l'istruzione `if` seguente non è valida in C\#:  
  
 [!CODE [csrefKeywordsTypes#2](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsTypes#2)]  
  
 Per eseguire il test di una variabile di tipo `int`, è necessario confrontarla esplicitamente con un valore, ad esempio zero, come illustrato di seguito:  
  
 [!CODE [csrefKeywordsTypes#3](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsTypes#3)]  
  
## Esempio  
 In questo esempio, il programma controlla che il carattere inserito da tastiera sia una lettera.  In caso affermativo, controlla se il carattere è minuscolo o maiuscolo  Questi controlli vengono eseguiti con <xref:System.Char.IsLetter%2A> e <xref:System.Char.IsLower%2A>, che restituiscono il tipo `bool`:  
  
 [!CODE [csrefKeywordsTypes#4](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsTypes#4)]  
  
## Specifiche del linguaggio C\#  
 [!INCLUDE[CSharplangspec](../../../csharp/language-reference/keywords/includes/csharplangspec_md.md)]  
  
## Vedere anche  
 [Riferimenti per C\#](../../../csharp/language-reference/index.md)   
 [Guida per programmatori C\#](../../../csharp/programming-guide/index.md)   
 [Parole chiave di C\#](../../../csharp/language-reference/keywords/index.md)   
 [Tabella dei tipi integrali](../../../csharp/language-reference/keywords/integral-types-table.md)   
 [Tabella dei tipi incorporati](../../../csharp/language-reference/keywords/built-in-types-table.md)   
 [Tabella delle conversioni numeriche implicite](../../../csharp/language-reference/keywords/implicit-numeric-conversions-table.md)   
 [Tabella delle conversioni numeriche esplicite](../../../csharp/language-reference/keywords/explicit-numeric-conversions-table.md)