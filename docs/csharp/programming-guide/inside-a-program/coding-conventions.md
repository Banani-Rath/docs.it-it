---
title: "Convenzioni di codifica C# (Guida per programmatori C#) | Microsoft Docs"
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
  - "linguaggio C#, convenzioni di codifica"
  - "convenzioni di codifica, C#"
  - "Visual C#, convenzioni di codifica"
ms.assetid: f4f60de9-d49b-4fb6-bab1-20e19ea24710
caps.latest.revision: 32
caps.handback.revision: 32
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# Convenzioni di codifica C# (Guida per programmatori C#)
La [specifica del linguaggio C\#](http://go.microsoft.com/fwlink/?LinkId=199552) non definisce uno standard di codifica.  Tuttavia, le linee guida riportate in questo argomento vengono usate da Microsoft per sviluppare gli esempi e la documentazione.  
  
 Le convenzioni di codifica hanno gli scopi seguenti:  
  
-   Creano un aspetto coerente per il codice in modo che chi legge possa concentrarsi sul contenuto, non sul layout.  
  
-   Consentono a chi legge di comprendere il codice più rapidamente, formulando presupposti basati sulle esperienze precedenti.  
  
-   Facilitano la copia, la modifica e la gestione del codice.  
  
-   Illustrano procedure consigliate di C\#.  
  
## Convenzioni di denominazione  
  
-   Negli esempi brevi che non includono [direttive using](../../../csharp/language-reference/keywords/using-directive.md), usare qualifiche dello spazio dei nomi.  Se si è certi che uno spazio dei nomi viene importato per impostazione predefinita in un progetto, non è necessario specificare in modo completo i nomi da tale spazio dei nomi.  I nomi completi possono essere interrotti dopo un punto \(.\) se sono troppo lunghi per una singola riga, come illustrato nell'esempio seguente.  
  
     [!CODE [csProgGuideCodingConventions#1](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#1)]  
  
-   Non è necessario modificare i nomi degli oggetti creati usando gli strumenti di progettazione di Visual Studio per adattarli ad altre linee guida.  
  
## Convenzioni di layout  
 Un layout appropriato usa la formattazione per mettere in evidenza la struttura del codice e per facilitare la lettura del codice.  Gli esempi Microsoft sono conformi alle convenzioni seguenti:  
  
-   Usare le impostazioni dell'Editor di codice predefinite \(rientri intelligenti, rientri di quattro caratteri, tabulazioni salvate come spazi\).  Per altre informazioni, vedere [Opzioni, Editor di testo, C\#, Formattazione](/visual-studio/ide/reference/options-text-editor-csharp-formatting)  
  
-   Scrivere una sola istruzione per riga.  
  
-   Scrivere una sola dichiarazione per riga.  
  
-   Se le righe di continuazione non sono rientrate automaticamente, impostare un rientro con un punto di tabulazione \(quattro spazi\).  
  
-   Aggiungere almeno una riga vuota tra le definizioni di metodo e proprietà.  
  
-   Usare le parentesi per rendere visibili le clausole in un'espressione, come illustrato nel codice seguente.  
  
     [!CODE [csProgGuideCodingConventions#2](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#2)]  
  
## Convenzioni relative ai commenti  
  
-   Posizionare il commento su una riga separata, non alla fine di una riga di codice.  
  
-   Iniziare il commento con una lettera maiuscola.  
  
-   Terminare il commento con un punto finale.  
  
-   Inserire uno spazio tra i delimitatori di commento \(\/\/\) e il testo del commento, come illustrato nell'esempio seguente.  
  
     [!CODE [csProgGuideCodingConventions#3](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#3)]  
  
-   Non creare blocchi formattati di asterischi intorno ai commenti.  
  
## Linee guida della lingua  
 Nelle sezioni seguenti vengono descritte le procedure che il team C\# deve seguire per preparare campioni ed esempi di codice.  
  
### Tipo di dati String  
  
-   Usare l'operatore `+` per concatenare stringhe brevi, come illustrato nel codice seguente.  
  
     [!CODE [csProgGuideCodingConventions#6](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#6)]  
  
-   Per accodare stringhe nei cicli, specialmente quando si lavora con grandi quantità di testo, usare un oggetto <xref:System.Text.StringBuilder>.  
  
     [!CODE [csProgGuideCodingConventions#7](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#7)]  
  
### Variabili locali tipizzate in modo implicito  
  
-   Usare la [tipizzazione implicita](../../../csharp/programming-guide/classes-and-structs/implicitly-typed-local-variables.md) per le variabili locali quando il tipo della variabile è ovvio dal lato destro dell'assegnazione o il tipo preciso non è importante.  
  
     [!CODE [csProgGuideCodingConventions#8](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#8)]  
  
-   Non usare [var](../../../csharp/language-reference/keywords/var.md) quando il tipo non è evidente dal lato destro dell'assegnazione.  
  
     [!CODE [csProgGuideCodingConventions#9](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#9)]  
  
-   Non basarsi sul nome della variabile per specificare il tipo della variabile.  Potrebbe non essere corretto.  
  
     [!CODE [csProgGuideCodingConventions#10](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#10)]  
  
-   Evitare l'utilizzo di `var` al posto di [dynamic](../../../csharp/language-reference/keywords/dynamic.md).  
  
-   Usare la tipizzazione implicita per determinare il tipo della variabile del ciclo nei cicli [for](../../../csharp/language-reference/keywords/for.md) e [foreach](../../../csharp/language-reference/keywords/foreach-in.md).  
  
     Nell'esempio seguente viene usata la tipizzazione implicita in un'istruzione `for`.  
  
     [!CODE [csProgGuideCodingConventions#11](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#11)]  
  
     Nell'esempio seguente viene usata la tipizzazione implicita in un'istruzione `foreach`.  
  
     [!CODE [csProgGuideCodingConventions#12](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#12)]  
  
### Tipi di dati non firmati  
  
-   In generale, usare `int` anziché tipi non firmati.  L'utilizzo di `int` è comune in C\# ed è più facile interagire con altre librerie, quando si usa `int`.  
  
### Matrici  
  
-   Usare la sintassi concisa quando si inizializzano le matrici nella riga della dichiarazione.  
  
     [!CODE [csProgGuideCodingConventions#13](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#13)]  
  
### Delegati  
  
-   Usare la sintassi concisa per creare istanze di un tipo delegato.  
  
     [!CODE [csProgGuideCodingConventions#14](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#14)]  
  
     [!CODE [csProgGuideCodingConventions#15](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#15)]  
  
### Istruzioni try\-catch e using nella gestione delle eccezioni  
  
-   Usare un'istruzione [try\-catch](../../../csharp/language-reference/keywords/try-catch.md) per la gestione della maggior parte delle eccezioni.  
  
     [!CODE [csProgGuideCodingConventions#16](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#16)]  
  
-   Semplificare il codice usando l'[istruzione using](../../../csharp/language-reference/keywords/using-statement.md) di C\#.  Se si ha un'istruzione [try\-finally](../../../csharp/language-reference/keywords/try-finally.md) in cui l'unico codice nel blocco `finally` è una chiamata al metodo <xref:System.IDisposable.Dispose%2A>, usare invece un'istruzione `using`.  
  
     [!CODE [csProgGuideCodingConventions#17](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#17)]  
  
### Operatori && e &#124;&#124;  
  
-   Per evitare eccezioni e migliorare le prestazioni evitando confronti non necessari, usare l'operatore [&&](../../../csharp/language-reference/operators/conditional-and-operator.md) anziché [&](../../../csharp/language-reference/operators/and-operator.md) e [&#124;&#124;](../../../csharp/language-reference/operators/conditional-or-operator.md) invece di                                       [&#124;](../../../csharp/language-reference/operators/or-operator.md) quando si eseguono confronti, come illustrato nell'esempio seguente.  
  
     [!CODE [csProgGuideCodingConventions#18](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#18)]  
  
### Operatore New  
  
-   Usare il modulo conciso della creazione dell'istanza di oggetto, con la tipizzazione implicita, come illustrato nella dichiarazione seguente.  
  
     [!CODE [csProgGuideCodingConventions#19](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#19)]  
  
     La riga precedente è equivalente alla dichiarazione seguente.  
  
     [!CODE [csProgGuideCodingConventions#20](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#20)]  
  
-   Usare gli inizializzatori di oggetto per semplificare la creazione di un oggetto.  
  
     [!CODE [csProgGuideCodingConventions#21](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#21)]  
  
### Gestione di eventi  
  
-   Se si definisce un gestore eventi che non è necessario rimuovere successivamente, usare un'espressione lambda.  
  
     [!CODE [csProgGuideCodingConventions#22](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#22)]  
  
     [!CODE [csProgGuideCodingConventions#23](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#23)]  
  
### Membri static  
  
-   Chiamare i membri [static](../../../csharp/language-reference/keywords/static.md) usando il nome della classe: *ClassName.StaticMember*.  Questa pratica rende più leggibile il codice semplificando l'accesso statico.  Non qualificare un membro statico definito in una classe base con il nome di una classe derivata.  Nonostante il codice venga compilato, la leggibilità del codice è fuorviante mentre il codice potrebbe essere interrotto in futuro, se si aggiunge un membro statico con lo stesso nome alla classe derivata.  
  
### Query LINQ  
  
-   Usare nomi significativi per le variabili di query.  Nell'esempio seguente viene usato `seattleCustomers` per i clienti che si trovano a Seattle.  
  
     [!CODE [csProgGuideCodingConventions#25](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#25)]  
  
-   Usare gli alias per assicurarsi che i nomi delle proprietà di tipi anonimi siano scritti correttamente in maiuscolo, usando la convenzione Pascal.  
  
     [!CODE [csProgGuideCodingConventions#26](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#26)]  
  
-   Rinominare le proprietà quando i nomi delle proprietà nel risultato potrebbero risultare ambigui.  Ad esempio, se la query restituisce un nome cliente un ID del server di distribuzione, anziché lasciarli come `Name` e `ID` nei risultati, rinominarli per spiegare che `Name` è il nome di un cliente e `ID` è l'ID di un server di distribuzione.  
  
     [!CODE [csProgGuideCodingConventions#27](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#27)]  
  
-   Usare la tipizzazione implicita nella dichiarazione di variabili di query e variabili di intervallo.  
  
     [!CODE [csProgGuideCodingConventions#25](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#25)]  
  
-   Allineare le clausole di query sotto la clausola [from](../../../csharp/language-reference/keywords/from-clause.md), come illustrato negli esempi precedenti.  
  
-   Usare le clausole [where](../../../csharp/language-reference/keywords/where-clause.md) prima di altre clausole di query per garantire che successive clausole di query agiscano su un set di dati ridotto e filtrato.  
  
     [!CODE [csProgGuideCodingConventions#29](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#29)]  
  
-   Usare più clausole `from` invece di una clausola [join](../../../csharp/language-reference/keywords/join-clause.md) per accedere a raccolte interne.  Ad esempio, ogni raccolta di oggetti `Student` potrebbe contenere una raccolta di punteggi del test.  Quando viene eseguita la query seguente, viene restituito ogni punteggio superiore a 90, e il cognome dello studente che ha ricevuto il punteggio.  
  
     [!CODE [csProgGuideCodingConventions#30](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#30)]  
  
## Sicurezza  
 Seguire le linee guida in [Secure Coding Guidelines](../Topic/Secure%20Coding%20Guidelines.md).  
  
## Vedere anche  
 [Visual Basic Coding Conventions](../../../visual-basic/programming-guide/program-structure/coding-conventions.md)   
 [Secure Coding Guidelines](../Topic/Secure%20Coding%20Guidelines.md)