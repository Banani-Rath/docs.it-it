---
title: "Procedura: dichiarare e usare propriet&#224; Read Write (Guida per programmatori C#) | Microsoft Docs"
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
  - "get (funzione di accesso) [C#], dichiarazione di proprietà"
  - "set (funzione di accesso) [C#]"
  - "proprietà [C#], dichiarazione"
  - "proprietà in lettura e scrittura [C#]"
  - "funzioni di accesso [C#], dichiarazione di proprietà con"
ms.assetid: a4962fef-af7e-4c4b-a929-4ae4d646ab8a
caps.latest.revision: 19
caps.handback.revision: 19
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# Procedura: dichiarare e usare propriet&#224; Read Write (Guida per programmatori C#)
Le proprietà offrono i vantaggi dei membri dati pubblici senza i rischi associati all'accesso non protetto, non controllato e non verificato ai dati di un oggetto.  Ciò si ottiene tramite le *funzioni di accesso*, ossia metodi speciali che assegnano e recuperano valori dal membro dati sottostante.  La funzione di accesso [set](../../../csharp/language-reference/keywords/set.md) consente l'assegnazione di valori ai membri dati, mentre la funzione di accesso [get](../../../csharp/language-reference/keywords/get.md) recupera i valori dei membri dati.  
  
 Questo esempio presenta una classe `Person` con due proprietà: `Name` \(string\) e `Age` \(int\).  Entrambe le proprietà forniscono le funzioni di accesso `get` e `set`, quindi vengono considerate proprietà in lettura\/scrittura.  
  
## Esempio  
 [!CODE [csProgGuideObjects#33](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#33)]  
  
## Programmazione efficiente  
 Nell'esempio precedente le proprietà `Name` e `Age` sono [pubbliche](../../../csharp/language-reference/keywords/public.md) e comprendono una funzione di accesso `get` e una funzione di accesso `set`.  In questo modo qualsiasi oggetto può leggere e scrivere tali proprietà.  È a volte preferibile, tuttavia, escludere una delle funzioni di accesso.  Se ad esempio la funzione di accesso `set` viene omessa, la proprietà diventa in sola lettura:  
  
 [!CODE [csProgGuideObjects#87](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#87)]  
  
 In alternativa è possibile esporre una funzione di accesso pubblicamente ma rendere l'altra privata o protetta.  Per ulteriori informazioni, vedere [Accessibilità asimmetrica delle funzioni di accesso](../../../csharp/programming-guide/classes-and-structs/restricting-accessor-accessibility.md).  
  
 Una volta dichiarate le proprietà, è possibile utilizzare questi metodi come se si trattasse di campi della classe.  Questo consente di utilizzare una sintassi molto semplice quando si desidera ottenere o impostare il valore di una proprietà, come nelle seguenti istruzioni:  
  
 [!CODE [csProgGuideObjects#35](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#35)]  
  
 Tenere presente che in un metodo `set` di una proprietà è disponibile una variabile `value` speciale.  Tale variabile contiene il valore specificato dall'utente, ad esempio:  
  
 [!CODE [csProgGuideObjects#36](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#36)]  
  
 La sintassi per l'incremento della proprietà `Age` per un oggetto `Person` è molto semplice:  
  
 [!CODE [csProgGuideObjects#37](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#37)]  
  
 Se si utilizzassero due metodi `set` e `get` distinti per impostare le proprietà, sarebbe necessaria una stringa di codice del seguente tipo:  
  
```  
person.SetAge(person.GetAge() + 1);   
```  
  
 In questo esempio viene eseguito l'override del metodo `ToString`:  
  
 [!CODE [csProgGuideObjects#38](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#38)]  
  
 Il metodo `ToString` non è utilizzato in modo esplicito nel programma,  ma viene richiamato per impostazione predefinita dalle chiamate a `WriteLine`.  
  
## Vedere anche  
 [Guida per programmatori C\#](../../../csharp/programming-guide/index.md)   
 [Proprietà](../../../csharp/programming-guide/classes-and-structs/properties.md)   
 [Classi e struct](../../../csharp/programming-guide/classes-and-structs/index.md)