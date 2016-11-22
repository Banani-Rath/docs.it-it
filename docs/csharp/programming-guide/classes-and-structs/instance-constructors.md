---
title: "Costruttori di istanze (Guida per programmatori C#) | Microsoft Docs"
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
  - "costruttori [C#], costruttori di istanza"
  - "costruttori di istanze [C#]"
ms.assetid: 24663779-c1e5-4af4-a942-ca554e4c542d
caps.latest.revision: 26
caps.handback.revision: 26
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# Costruttori di istanze (Guida per programmatori C#)
I costruttori di istanza sono utilizzati per creare e inizializzare qualsiasi variabile membro di istanza quando si utilizza l'espressione [new](../../../csharp/language-reference/keywords/new.md) per creare un oggetto di una [classe](../../../csharp/language-reference/keywords/class.md).  Per inizializzare una classe [statica](../../../csharp/language-reference/keywords/static.md) o variabili statiche in una classe non statica, è necessario definire un costruttore statico.  Per ulteriori informazioni, vedere [Costruttori statici](../../../csharp/programming-guide/classes-and-structs/static-constructors.md).  
  
 Nell'esempio seguente viene illustrato un costruttore di istanza:  
  
 [!CODE [csProgGuideObjects#5](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#5)]  
  
> [!NOTE]
>  Per maggior chiarezza, questa classe contiene campi pubblici.  L'utilizzo di campi pubblici non è consigliato nella programmazione, perché consente a qualsiasi metodo in un punto qualsiasi di un programma di accedere senza restrizioni e senza alcuna verifica ai meccanismi interni di un oggetto.  I membri dati devono in genere essere privati e devono essere accessibili solo tramite metodi e proprietà di classi.  
  
 Questo costruttore di istanza viene chiamato quando viene creato un oggetto basato sulla classe `CoOrds`.  Un costruttore come questo, che non accetta argomenti, viene definito *costruttore predefinito*.  Tuttavia, risulta spesso utile per fornire costruttori aggiuntivi.  È ad esempio possibile aggiungere alla classe `CoOrds` un costruttore che consenta di specificare i valori iniziali per i membri dati:  
  
 [!CODE [csProgGuideObjects#76](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#76)]  
  
 In questo modo sarà possibile creare oggetti `CoOrd` con valori iniziali predefiniti o specifici, come illustrato di seguito:  
  
 [!CODE [csProgGuideObjects#77](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#77)]  
  
 Se una classe non dispone di un costruttore, viene generato automaticamente un costruttore predefinito e per inizializzare i campi dell'oggetto vengono utilizzati i valori predefiniti.  Ad esempio, un [int](../../../csharp/language-reference/keywords/int.md) viene inizializzato a 0.  Per ulteriori informazioni sui valori predefiniti, vedere [Tabella dei valori predefiniti](../../../csharp/language-reference/keywords/default-values-table.md).  Poiché il costruttore predefinito della classe `CoOrds` inizializza tutti i membri dati su zero, può pertanto essere rimosso completamente senza modificare il funzionamento della classe.  Per un esempio completo sull'utilizzo di più costruttori, vedere l'Esempio 1 più avanti in questo argomento. Per un esempio di costruttore generato automaticamente, vedere l'Esempio 2.  
  
 I costruttori di istanza possono inoltre essere utilizzati per chiamare i costruttori di istanza delle classi base.  Il costruttore di classi può richiamare il costruttore della classe base mediante l'inizializzatore, ad esempio:  
  
 [!CODE [csProgGuideObjects#78](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#78)]  
  
 In questo esempio la classe `Circle` passa i valori che rappresentano il raggio e l'altezza al costruttore fornito da `Shape`, da cui deriva `Circle`.  Per un esempio completo sull'utilizzo di `Shape` e `Circle`, vedere l'Esempio 3 di questo argomento.  
  
## Esempio 1  
 Nell'esempio riportato di seguito viene illustrata una classe con due costruttori di classi, uno senza argomenti e uno con due argomenti.  
  
 [!CODE [csProgGuideObjects#4](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#4)]  
  
## Esempio 2  
 Nell'esempio riportato di seguito la classe `Person` non ha alcun costruttore. In questo caso viene fornito automaticamente un costruttore predefinito e i campi vengono inizializzati sui valori predefiniti.  
  
 [!CODE [csProgGuideObjects#8](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#8)]  
  
 Si noti che il valore predefinito di `age` è `0` e il valore predefinito di `name` è `null`.  Per ulteriori informazioni sui valori predefiniti, vedere [Tabella dei valori predefiniti](../../../csharp/language-reference/keywords/default-values-table.md).  
  
## Esempio 3  
 Nell'esempio riportato di seguito viene illustrato l'utilizzo dell'inizializzatore della classe base.  La classe `Circle` è derivata dalla classe generale `Shape` e la classe `Cylinder` è derivata dalla classe `Circle`.  Il costruttore di ciascuna classe derivata utilizza il relativo inizializzatore della classe base.  
  
 [!CODE [csProgGuideObjects#9](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#9)]  
  
 Per ulteriori esempi su come richiamare i costruttori della classe base, vedere [virtuale](../../../csharp/language-reference/keywords/virtual.md), [override](../../../csharp/language-reference/keywords/override.md) e [base](../../../csharp/language-reference/keywords/base.md).  
  
## Vedere anche  
 [Guida per programmatori C\#](../../../csharp/programming-guide/index.md)   
 [Classi e struct](../../../csharp/programming-guide/classes-and-structs/index.md)   
 [Costruttori](../../../csharp/programming-guide/classes-and-structs/constructors.md)   
 [Distruttori](../../../csharp/programming-guide/classes-and-structs/destructors.md)   
 [statiche](../../../csharp/language-reference/keywords/static.md)