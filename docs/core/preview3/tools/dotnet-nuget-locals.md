---
title: Comando dotnet-nuget-locals | .NET Core SDK
description: Il comando dotnet-nuget-locals cancella o elenca risorse NuGet locali quali cache delle richieste HTTP, cache temporanea o cartella globale dei pacchetti a livello di computer.
keywords: dotnet-nuget-locals, interfaccia della riga di comando, comando dell&quot;interfaccia della riga di comando, .NET Core
author: karann-msft
ms.author: mairaw
manager: wpickett
ms.date: 11/15/2016
ms.topic: article
ms.prod: .net-core
ms.technology: .net-core-technologies
ms.devlang: dotnet
ms.assetid: 8440229e-317e-4dc1-9463-cba5fdb12c3b
translationtype: Human Translation
ms.sourcegitcommit: 1a84c694945fe0c77468eb77274ab46618bccae6
ms.openlocfilehash: 08c51ecb4e042254c89f618d6baff1b407af0113

---

#<a name="dotnet-nuget-locals"></a>dotnet-nuget-locals

[!INCLUDE[preview-warning](../../../includes/warning.md)] 

## <a name="name"></a>Nome 
`dotnet-nuget-locals`: cancella o elenca risorse NuGet locali quali cache delle richieste HTTP, cache temporanea o cartella globale dei pacchetti a livello di computer. 

## <a name="synopsis"></a>Riepilogo

`dotnet nuget locals <cache_location> [--clear|--list] [--help] [--force-english-output]`

dove `<cache_location>` è uno dei valori seguenti: `all`, `http-cache`, `packages-cache`, `global-packages` o `temp`.

## <a name="description"></a>Descrizione

Il comando `dotnet nuget locals` cancella o elenca risorse NuGet locali quali cache delle richieste HTTP, cache temporanea o cartella globale dei pacchetti a livello di computer.

## <a name="arguments"></a>Argomenti

`all`

Indica che l'operazione specificata deve essere applicata a tutti i tipi di cache, ovvero alla cache delle richieste HTTP, alla cache globale dei pacchetti e alla cache temporanea.

`http-cache`

Indica che l'operazione specificata deve essere applicata soltanto alla cache delle richieste HTTP. Le altre posizioni di cache non sono interessate.

`global-packages`

Indica che l'operazione specificata deve essere applicata soltanto alla cache globale dei pacchetti. Le altre posizioni di cache non sono interessate.

`temp`

Indica che l'operazione specificata deve essere applicata soltanto alla cache temporanea. Le altre posizioni di cache non sono interessate.

## <a name="options"></a>Opzioni

`-h|--help`

Stampa una breve guida per il comando.  

`-c|--clear`

L'opzione "clear" viene usata per eseguire un'operazione di cancellazione sul tipo di cache specificato. Il contenuto delle directory della cache viene eliminato in modo ricorsivo. Affinché l'operazione abbia esito positivo, l'utente/gruppo che la esegue deve disporre delle autorizzazioni per i file presenti nelle directory della cache. In caso contrario, viene visualizzato un messaggio di errore con l'indicazione delle cartelle e/o dei file che non sono stati cancellati.

`-l|--list`

L'opzione "list" viene usata per visualizzare la posizione del tipo di cache specificato. 

`--force-english-output`

Forza la visualizzazione in inglese dell'output della riga di comando.

## <a name="examples"></a>Esempi

Visualizza i percorsi di tutte le directory locali della cache, ovvero directory della cache HTTP, directory della cache globale dei pacchetti e directory della cache temporanea.

`dotnet nuget locals –l all`

Visualizza il percorso della directory locale della cache HTTP:

`dotnet nuget locals --list http-cache`

Cancella tutti i file presenti in tutte le directory locali della cache, ovvero directory della cache HTTP, directory della cache globale dei pacchetti e directory della cache temporanea.

`dotnet nuget locals --clear all`

Cancella tutti i file presenti nella directory locale della cache globale dei pacchetti:

`dotnet nuget locals -c global-packages`

Cancella tutti i file presenti nella directory locale della cache temporanea:

`dotnet nuget locals -c temp`

## <a name="troubleshooting"></a>Risoluzione dei problemi

Per informazioni sui problemi e sugli errori più comuni relativi all'uso del comando `dotnet-nuget-locals`, vedere [Managing the NuGet cache](https://docs.nuget.org/ndocs/consume-packages/managing-the-nuget-cache) (Gestione della cache NuGet).



<!--HONumber=Nov16_HO3-->


