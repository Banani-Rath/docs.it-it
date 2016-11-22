---
title: "Delegati generici (Guida per programmatori C#) | Microsoft Docs"
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
  - "delegati [C#], generics"
  - "generics [C#], delegati"
ms.assetid: bdea509c-44c1-4309-aaa9-15c7aee009df
caps.latest.revision: 16
caps.handback.revision: 16
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# Delegati generici (Guida per programmatori C#)
Un [delegato](../../../csharp/language-reference/keywords/delegate.md) può definire i propri parametri di tipo.  Il codice che fa riferimento al delegato generico può specificare l'argomento di tipo per creare un tipo costruito chiuso, analogamente a quanto avviene quando si crea un'istanza di una classe generica o si chiama un metodo generico, come illustrato nell'esempio riportato di seguito:  
  
 [!CODE [csProgGuideGenerics#36](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideGenerics#36)]  
  
 C\# versione 2.0 dispone di una nuova funzionalità denominata conversione dei gruppi di metodi, applicabile a tipi di delegati sia concreti che generici, che consente di scrivere la riga precedente con la seguente sintassi semplificata:  
  
 [!CODE [csProgGuideGenerics#37](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideGenerics#37)]  
  
 I delegati definiti in una classe generica possono utilizzare i parametri di tipo di classi generiche analogamente ai metodi di classi.  
  
 [!CODE [csProgGuideGenerics#38](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideGenerics#38)]  
  
 Il codice che fa riferimento al delegato deve specificare l'argomento di tipo della classe che lo contiene, come riportato di seguito:  
  
 [!CODE [csProgGuideGenerics#39](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideGenerics#39)]  
  
 I delegati generici sono particolarmente utili nella definizione di eventi in base al modello di progettazione tipico perché l'argomento del mittente può essere fortemente tipizzato e non deve più essere sottoposto a cast sull'oggetto <xref:System.Object> e da esso.  
  
 [!CODE [csProgGuideGenerics#40](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideGenerics#40)]  
  
## Vedere anche  
 <xref:System.Collections.Generic>   
 [Guida per programmatori C\#](../../../csharp/programming-guide/index.md)   
 [Introduzione ai generics](../../../csharp/programming-guide/generics/introduction-to-generics.md)   
 [Metodi generici](../../../csharp/programming-guide/generics/generic-methods.md)   
 [Classi generiche](../../../csharp/programming-guide/generics/generic-classes.md)   
 [Interfacce generiche](../../../csharp/programming-guide/generics/generic-interfaces.md)   
 [Delegati](../../../csharp/programming-guide/delegates/index.md)   
 [Generics](../Topic/Generics%20in%20the%20.NET%20Framework.md)