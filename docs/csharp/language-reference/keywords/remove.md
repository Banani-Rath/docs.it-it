---
title: "remove (Riferimenti per C#) | Microsoft Docs"
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
  - "remove_CSharpKeyword"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "remove (funzione di accesso agli eventi) [C#]"
ms.assetid: c8223426-c17b-4fe2-8406-01564cf1dd2b
caps.latest.revision: 8
caps.handback.revision: 8
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# remove (Riferimenti per C#)
La parola chiave contestuale `remove` è utilizzata per definire una funzione di accesso di un evento personalizzato richiamata quando il codice client annulla la sottoscrizione di tale [evento](../../../csharp/language-reference/keywords/event.md).  Se si fornisce una funzione di accesso personalizzata `remove`, è necessario fornire anche una funzione di accesso [add](../../../csharp/language-reference/keywords/add.md).  
  
## Esempio  
 Nell'esempio seguente viene mostrato un evento che dispone di funzioni di accesso personalizzate [add](../../../csharp/language-reference/keywords/add.md) e `remove`.  Per l'esempio completo, vedere [Procedura: implementare eventi di interfaccia](../../../csharp/programming-guide/events/how-to-implement-interface-events.md).  
  
 [!CODE [csrefKeywordsContextual#15](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsContextual#15)]  
  
 Generalmente non è necessario fornire funzioni di accesso per un evento personalizzato.  Le funzioni di accesso che vengono generate automaticamente dal compilatore quando si dichiara un evento sono sufficienti per la maggior parte degli scenari.  
  
## Vedere anche  
 [Eventi](../../../csharp/programming-guide/events/index.md)