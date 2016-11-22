---
title: "Generics e attributi (Guida per programmatori C#) | Microsoft Docs"
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
  - "attributi [C#], con generics"
  - "generics [C#], attributi"
ms.assetid: da9fc326-4648-454a-8e13-3911a2edefd7
caps.latest.revision: 13
caps.handback.revision: 13
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# Generics e attributi (Guida per programmatori C#)
Non è possibile applicare attributi a tipi generici con modalità simili a quelle previste per i tipi non generici.  Per ulteriori informazioni sull'applicazione degli attributi, vedere [Attributi](../Topic/Attributes%20\(C%23%20and%20Visual%20Basic\).md).  
  
 Gli attributi personalizzati possono fare riferimento solo a tipi generici aperti, ovvero tipi generici per i quali non vengono forniti argomenti di tipo, nonché a tipi generici costruiti chiusi, che forniscono gli argomenti per tutti i parametri di tipo.  
  
 Negli esempi riportati di seguito viene utilizzato questo attributo personalizzato:  
  
 [!CODE [csProgGuideGenerics#48](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideGenerics#48)]  
  
 Un attributo può fare riferimento a un tipo generico aperto:  
  
 [!CODE [csProgGuideGenerics#49](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideGenerics#49)]  
  
 Specificare più parametri di tipo utilizzando il numero appropriato di virgole.  In questo esempio `GenericClass2` ha due parametri di tipo:  
  
 [!CODE [csProgGuideGenerics#50](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideGenerics#50)]  
  
 Un attributo può fare riferimento a un tipo generico costruito chiuso:  
  
 [!CODE [csProgGuideGenerics#51](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideGenerics#51)]  
  
 Un attributo che fa riferimento a un parametro di tipo generico genererà un errore in fase di compilazione:  
  
 [!CODE [csProgGuideGenerics#52](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideGenerics#52)]  
  
 Un tipo generico non può ereditare da <xref:System.Attribute>:  
  
 [!CODE [csProgGuideGenerics#53](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideGenerics#53)]  
  
 Per ottenere informazioni su un tipo generico o un parametro di tipo generico in fase di esecuzione, è possibile utilizzare i metodi di <xref:System.Reflection>.  Per ulteriori informazioni, vedere [Generics e reflection](../../../csharp/programming-guide/generics/generics-and-reflection.md).  
  
## Vedere anche  
 [Guida per programmatori C\#](../../../csharp/programming-guide/index.md)   
 [Generics](../../../csharp/programming-guide/generics/index.md)   
 [Attributi](../Topic/Extending%20Metadata%20Using%20Attributes.md)