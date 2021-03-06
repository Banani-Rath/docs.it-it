---
title: Thread safety nelle espressioni regolari
description: Thread safety nelle espressioni regolari
keywords: .NET, .NET Core
author: stevehoag
manager: wpickett
ms.date: 07/28/2016
ms.topic: article
ms.prod: .net-core
ms.technology: .net-core-technologies
ms.devlang: dotnet
ms.assetid: dc64b681-b3aa-4911-8e30-0764a8b6a852
translationtype: Human Translation
ms.sourcegitcommit: fb00da6505c9edb6a49d2003ae9bcb8e74c11d6c
ms.openlocfilehash: ab71ad5ff9148f00f392fddd3c89acbcab874015

---

# <a name="thread-safety-in-regular-expressions"></a>Thread safety nelle espressioni regolari

La classe [Regex](xref:System.Text.RegularExpressions.Regex) è thread-safe e non modificabile (di sola lettura). Ciò significa che è possibile creare oggetti [Regex](xref:System.Text.RegularExpressions.Regex) in qualsiasi thread e condividerli fra i thread; i metodi corrispondenti possono essere chiamati da qualsiasi thread e non modificano in nessun caso uno stato globale.

Tuttavia gli oggetti risultato ([Match](xref:System.Text.RegularExpressions.Match) e [MatchCollection)](xref:System.Text.RegularExpressions.MatchCollection) restituiti da [Regex](xref:System.Text.RegularExpressions.Regex) vanno usati in un unico thread. Sebbene molti di questi oggetti non siano modificabili a livello logico, le loro implementazioni potrebbero ritardare l'elaborazione di determinati risultati per migliorare le prestazioni; di conseguenza, i chiamanti dovranno serializzare l'accesso a tali oggetti.

Se risulta necessario condividere oggetti risultato [Regex](xref:System.Text.RegularExpressions.Regex) su più thread, tali oggetti possono essere convertiti in istanze thread-safe chiamando i relativi metodi sincronizzati. Fatta eccezione per gli enumeratori, tutte le classi di espressioni regolari sono thread-safe o possono essere convertite in oggetti thread-safe mediante un metodo sincronizzato.

L'unica eccezione è costituita dagli enumeratori. Un'applicazione deve serializzare le chiamate agli enumeratori di raccolta. La regola indica che se una raccolta può essere enumerata in più thread contemporaneamente, è necessario sincronizzare i metodi di enumeratore sull'oggetto radice della raccolta attraversata dall'enumeratore.

## <a name="see-also"></a>Vedere anche

[Espressioni regolari .NET](regular-expressions.md)




<!--HONumber=Nov16_HO3-->


