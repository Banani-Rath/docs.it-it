---
title: Comando dotnet | .NET Core SDK
description: Informazioni sul comando dotnet (il driver generico per gli strumenti dell&quot;interfaccia della riga di comando di .NET Core) e sul relativo utilizzo.
keywords: dotnet, interfaccia della riga di comando, comando dell&quot;interfaccia della riga di comando, .NET Core
author: mairaw
manager: wpickett
ms.date: 10/07/2016
ms.topic: article
ms.prod: .net-core
ms.technology: .net-core-technologies
ms.devlang: dotnet
ms.assetid: 93015521-2127-4fe9-8fce-ca79bcc4ff49
translationtype: Human Translation
ms.sourcegitcommit: c6ee3f5663d0a3f62914e8de474cca4d15340c9d
ms.openlocfilehash: 77c37ac3d4d0ba9ad1feac539debe40b0ee31161

---

#<a name="dotnet-command"></a>Comando dotnet

## <a name="name"></a>Nome

dotnet: driver generale per l'esecuzione dei comandi della riga di comando

## <a name="synopsis"></a>Riepilogo

`dotnet [--version] [--verbose] [--info] [command] [arguments] [--help]`

## <a name="description"></a>Descrizione
`dotnet` è un driver generico per la toolchain dell'interfaccia della riga di comando. Se richiamato autonomamente, specificherà brevi istruzioni di utilizzo. 

Ogni funzionalità specifica viene implementata come un comando. Per usare la funzionalità, il comando viene specificato dopo `dotnet`, ad esempio [`dotnet build`](dotnet-build.md). Tutti gli argomenti che seguono il comando sono gli argomenti del comando. 

`dotnet` viene usato come comando autonomo solo per eseguire app portabili. Per eseguire l'applicazione, specificare solo un file DLL di un'applicazione portabile dopo il verbo `dotnet`.    

## <a name="options"></a>Opzioni

`-v|--verbose`

Abilita l'output dettagliato.

`--version`

Stampa la versione degli strumenti dell'interfaccia della riga di comando.

`--info`

Stampa informazioni più dettagliate sugli strumenti dell'interfaccia della riga di comando, ad esempio il sistema operativo corrente, l'Agente integrità sistema di commit per la versione e così via. 

`-h|--help`

Stampa una breve guida per il comando. Se si usa solo con `dotnet`, stampa inoltre un elenco dei comandi disponibili.  

## <a name="dotnet-commands"></a>Comandi dotnet

Per dotnet sono disponibili i comandi seguenti:

* [dotnet-new](dotnet-new.md)
   * Inizializza un progetto di applicazione console C# o F#.
* [dotnet-restore](dotnet-restore.md)
  * Ripristina le dipendenze per una determinata applicazione. 
* [dotnet-build](dotnet-build.md)
  * Compila un'applicazione .NET Core.
* [dotnet-publish](dotnet-publish.md)
   * Pubblica un'applicazione autonoma o un'applicazione portabile .NET.
* [dotnet-run](dotnet-run.md)
   * Esegue l'applicazione dall'origine.
* [dotnet-test](dotnet-test.md)
   * Esegue test usando un Test Runner specificato nel file project.json.
* [dotnet-pack](dotnet-pack.md)
   * Crea un pacchetto NuGet del codice.

## <a name="examples"></a>Esempi

Inizializzare un'applicazione console .NET Core di esempio che può essere compilata ed eseguita:

`dotnet new`

Ripristinare le dipendenze per una determinata applicazione:

`dotnet restore`

Compilare un progetto e le relative dipendenze in una determinata directory: 

`dotnet build`

Eseguire un'app portabile denominata `myapp.dll`: `dotnet myapp.dll`

## <a name="environment"></a>Ambiente 

`DOTNET_PACKAGES`

Cache dei pacchetti principali. Se non è impostato, il percorso predefinito è $HOME/.nuget/packages in Unix o %HOME%\NuGet\Packages in Windows.

`DOTNET_SERVICING`

Specifica il percorso dell'indice di manutenzione che l'host condiviso deve usare durante il caricamento del runtime.

`DOTNET_CLI_TELEMETRY_OPTOUT`

Specifica se i dati relativi all'utilizzo degli strumenti .NET Core vengono raccolti e inviati a Microsoft. `true` per rifiutare esplicitamente la funzionalità di telemetria (i valori accettati sono True, 1 o Sì). In caso contrario, `false` (i valori accettati sono False, 0 o no). Se non è impostato, il valore predefinito è `false`, pertanto la funzionalità di telemetria è attiva.


<!--HONumber=Nov16_HO1-->


