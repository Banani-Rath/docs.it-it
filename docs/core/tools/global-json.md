---
title: Informazioni di riferimento di global.json | .NET Core
description: Informazioni di riferimento di global.json
keywords: .NET, .NET Core
author: aL3891
ms.author: mairaw
manager: wpickett
ms.date: 11/02/2016
ms.topic: article
ms.prod: .net-core
ms.technology: .net-core-technologies
ms.devlang: dotnet
ms.assetid: e1ac9659-425f-4486-a376-c12ca942ead8
translationtype: Human Translation
ms.sourcegitcommit: 6f3a46284bd5820520739577919fa202f5b784d7
ms.openlocfilehash: adce52849247f5b12d43b389a7699de04fe278c4

---

# <a name="globaljson-reference"></a>Informazioni di riferimento di global.json

Il file global.json viene usato in progetti .NET Core per definire i metadati della soluzione. Questo file viene usato quando il comando [dotnet-restore](dotnet-restore.md) viene richiamato per ripristinare le dipendenze di un progetto .NET Core.
In questo argomento di riferimento verrà presentato l'elenco delle proprietà che è possibile definire nel file global.json.

## <a name="projects"></a>progetti
Tipo: String[]

Specifica le cartelle in cui il sistema di compilazione deve cercare i progetti durante la risoluzione delle dipendenze. Il sistema di compilazione eseguirà solo la ricerca delle cartelle figlio di livello più alto.

Ad esempio:

```json
{
    "projects": [ "src", "test" ]
}
```

## <a name="packages"></a>pacchetti
Tipo: String

Il percorso per archiviare i pacchetti.

Ad esempio:
```json
{
    "packages": "packages-dir"
}
```

## <a name="sdk"></a>SDK
Tipo: Object

Specifica le informazioni sull'SDK.

### <a name="version"></a>version
Tipo: String

La versione dell'SDK da usare.

Ad esempio:

```json
{
    "sdk": {
        "version": "1.0.0-preview2-003121"
    }
}
```



<!--HONumber=Nov16_HO3-->


