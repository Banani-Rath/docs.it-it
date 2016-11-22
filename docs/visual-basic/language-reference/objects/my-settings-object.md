---
title: "My.Settings Object | Microsoft Docs"
ms.custom: ""
ms.date: "11/17/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "My.MySettingsProperty.Settings"
  - "My.Settings"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "My.Settings object"
ms.assetid: 41f30dc1-202a-4273-b9b7-5728941f996c
caps.latest.revision: 16
caps.handback.revision: 16
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translationtype: Human Translation
---
# My.Settings Object
Fornisce proprietà e metodi per accedere alle impostazioni dell'applicazione.  
  
## Note  
 L'oggetto `My.Settings` fornisce accesso alle impostazioni dell'applicazione e consente di memorizzare e recuperare dinamicamente le impostazioni delle proprietà e altre informazioni per l'applicazione.  Per ulteriori informazioni, vedere [Gestione delle impostazioni di un'applicazione \(.NET\)](/visual-studio/ide/managing-application-settings-dotnet).  
  
## Proprietà  
 Le proprietà dell'oggetto `My.Settings` consentono di accedere alle impostazioni dell'applicazione.  Per aggiungere o rimuovere impostazioni, utilizzare **Progettazione impostazioni**.  
  
 A ogni impostazione sono associati **Nome**, **Tipo**, **Ambito** e **Valore** e queste impostazioni determinano il modo in cui la proprietà di accesso a ciascuna impostazione viene visualizzata nell'oggetto `My.Settings`:  
  
-   **Nome** consente di determinare il nome della proprietà.  
  
-   **Tipo** consente di determinare il tipo della proprietà.  
  
-   **Ambito** indica se la proprietà è in sola lettura.  Se il valore è **Applicazione**, la proprietà è in sola lettura; se il valore è **Utente**, la proprietà è in lettura\/scrittura.  
  
-   **Valore** è il valore predefinito della proprietà.  
  
## Metodi  
  
|||  
|-|-|  
|Metodo|Descrizione|  
|`Reload`|Consente di ricaricare le impostazioni dell'utente dagli ultimi valori salvati.|  
|`Save`|Salva le impostazioni correnti dell'utente.|  
  
 L'oggetto `My.Settings` fornisce inoltre proprietà e metodi avanzati, ereditati dalla classe <xref:System.Configuration.ApplicationSettingsBase>.  
  
## Attività  
 Nella tabella riportata di seguito sono elencati esempi di attività relative all'oggetto `My.Settings`.  
  
|||  
|-|-|  
|Per|Vedere|  
|Leggere un'impostazione dell'applicazione|[How to: Read Application Settings in Visual Basic](../../../visual-basic/developing-apps/programming/app-settings/how-to-read-application-settings.md)|  
|Modificare un'impostazione dell'utente|[How to: Change User Settings in Visual Basic](../../../visual-basic/developing-apps/programming/app-settings/how-to-change-user-settings.md)|  
|Mantenere le impostazioni dell'utente|[How to: Persist User Settings in Visual Basic](../../../visual-basic/developing-apps/programming/app-settings/how-to-persist-user-settings.md)|  
|Creare una griglia di proprietà per le impostazioni dell'utente|[How to: Create Property Grids for User Settings in Visual Basic](../../../visual-basic/developing-apps/programming/app-settings/how-to-create-property-grids-for-user-settings.md)|  
  
## Esempio  
 Nell'esempio riportato di seguito viene mostrato il valore dell'impostazione `Nickname`.  
  
 [!CODE [VbVbalrMyResources#14](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyResources#14)]  
  
 Perché l'esempio funzioni, l'applicazione deve disporre dell'impostazione `Nickname`, di tipo `String`.  
  
## Vedere anche  
 <xref:System.Configuration.ApplicationSettingsBase>   
 [How to: Read Application Settings in Visual Basic](../../../visual-basic/developing-apps/programming/app-settings/how-to-read-application-settings.md)   
 [How to: Change User Settings in Visual Basic](../../../visual-basic/developing-apps/programming/app-settings/how-to-change-user-settings.md)   
 [How to: Persist User Settings in Visual Basic](../../../visual-basic/developing-apps/programming/app-settings/how-to-persist-user-settings.md)   
 [How to: Create Property Grids for User Settings in Visual Basic](../../../visual-basic/developing-apps/programming/app-settings/how-to-create-property-grids-for-user-settings.md)   
 [Gestione delle impostazioni di un'applicazione \(.NET\)](/visual-studio/ide/managing-application-settings-dotnet)