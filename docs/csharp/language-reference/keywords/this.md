---
title: "this (Riferimenti per C#) | Microsoft Docs"
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
  - "this"
  - "this_CSharpKeyword"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "this (parola chiave) [C#]"
ms.assetid: d4f827fe-4710-410b-89b8-867dad44b8a3
caps.latest.revision: 19
caps.handback.revision: 19
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# this (Riferimenti per C#)
La parola chiave `this` si riferisce all'istanza corrente della classe e viene anche utilizzata come modificatore del primo parametro di un metodo di estensione.  
  
> [!NOTE]
>  In questo articolo viene illustrato l'utilizzo della parola chiave `this` con le istanze della classe.  Per ulteriori informazioni sull'utilizzo nei metodi di estensione, vedere [Metodi di estensione](../../../csharp/programming-guide/classes-and-structs/extension-methods.md).  
  
 La parola chiave `this` viene generalmente utilizzata per le operazioni descritte di seguito.  
  
-   Qualificare i membri nascosti da nomi simili, ad esempio:  
  
 [!CODE [csrefKeywordsAccess#4](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsAccess#4)]  
  
-   Passare un oggetto come parametro ad altri metodi, ad esempio:  
  
    ```  
    CalcTax(this);  
    ```  
  
-   Dichiarare indicizzatori, ad esempio:  
  
 [!CODE [csrefKeywordsAccess#5](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsAccess#5)]  
  
 Dal momento che esistono solo a livello di classe e non come parte di un oggetto, le funzioni membro statiche non dispongono di un puntatore `this`.  Non è possibile fare riferimento a `this` in un membro statico.  
  
## Esempio  
 Nell'esempio riportato di seguito la parola chiave `this` viene utilizzata per qualificare i membri di classe `Employee`, `name` e `alias`, che sono nascosti da nomi simili.  La parola chiave viene inoltre utilizzata per passare un oggetto al metodo `CalcTax`, che appartiene a un'altra classe.  
  
 [!CODE [csrefKeywordsAccess#3](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsAccess#3)]  
  
## Specifiche del linguaggio C\#  
 [!INCLUDE[CSharplangspec](../../../csharp/language-reference/keywords/includes/csharplangspec_md.md)]  
  
## Vedere anche  
 [Riferimenti per C\#](../../../csharp/language-reference/index.md)   
 [Guida per programmatori C\#](../../../csharp/programming-guide/index.md)   
 [Parole chiave di C\#](../../../csharp/language-reference/keywords/index.md)   
 [base](../../../csharp/language-reference/keywords/base.md)   
 [Metodi](../../../csharp/programming-guide/classes-and-structs/methods.md)