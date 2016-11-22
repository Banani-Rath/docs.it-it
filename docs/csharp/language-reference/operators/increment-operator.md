---
title: "Operatore ++ (Riferimenti per C#) | Microsoft Docs"
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
  - "++_CSharpKeyword"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "++ (operatore) [C#]"
  - "operatore di incremento (++) [C#]"
ms.assetid: e9dec353-070b-44fb-98ed-eb8fdf753feb
caps.latest.revision: 18
caps.handback.revision: 18
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# Operatore ++ (Riferimenti per C#)
L'operatore di incremento \(`++`\) incrementa il suo operando di 1. L'operatore di incremento può apparire prima o dopo il suo operando: `++variable` e `variable++`.  
  
## Note  
 Il primo modulo è un'operazione di incremento prefisso. Il risultato dell'operazione è il valore dell'operando dopo essere stato incrementato.  
  
 Il secondo modulo è un'operazione di incremento suffisso. Il risultato dell'operazione è il valore dell'operando prima di essere incrementato.  
  
 I tipi numerico e di enumerazione hanno operatori di incremento predefiniti. I tipi definiti dall'utente possono eseguire l'overload dell'operatore `++`. Le operazioni sui tipi integrali sono generalmente consentite sull'enumerazione.  
  
## Esempio  
 [!CODE [csRefOperators#3](../CodeSnippet/VS_Snippets_VBCSharp/csrefOperators#3)]  
  
## Vedere anche  
 [Riferimenti per C\#](../../../csharp/language-reference/index.md)   
 [Guida per programmatori C\#](../../../csharp/programming-guide/index.md)   
 [Operatori](../../../csharp/language-reference/operators/index.md)