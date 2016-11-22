---
title: "How to: Enable Tabbing Between Shapes (Visual Studio) | Microsoft Docs"
ms.custom: ""
ms.date: "11/17/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "Line control, implementing tabbing"
  - "Shape control, implementing tabbing"
ms.assetid: 09731b34-3900-4fcb-a9df-ce5280328433
caps.latest.revision: 14
caps.handback.revision: 14
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translationtype: Human Translation
---
# How to: Enable Tabbing Between Shapes (Visual Studio)
I controlli Line e Shape non dispongono di proprietà `TabStop` o `TabIndex`, ma è comunque possibile attivare la tabulazione tra di esse.  Nell'esempio riportato di seguito, premendo i tasti CTRL e TAB è possibile passare da una forma all'altra. Premendo solo il tasto TAB è possibile passare da un pulsante all'altro.  
  
> [!NOTE]
>  Il computer potrebbe mostrare nomi o percorsi diversi per alcuni elementi dell'interfaccia utente di Visual Studio nelle istruzioni seguenti.  Questi elementi sono determinati dall'edizione di Visual Studio in uso e dalle impostazioni utilizzate.  Per ulteriori informazioni, vedere [Customizing Development Settings in Visual Studio](http://msdn.microsoft.com/it-it/22c4debb-4e31-47a8-8f19-16f328d7dcd3).  
  
### Per attivare la tabulazione tra le forme  
  
1.  Trascinare tre controlli <xref:Microsoft.VisualBasic.PowerPacks.RectangleShape> e due controlli <xref:System.Windows.Forms.Button> dalla **Casella degli strumenti** al form.  
  
2.  Nell'editor di codice, aggiungere un'istruzione `Imports` o `using` all'inizio del modulo:  
  
    ```vb#  
    Imports Microsoft.VisualBasic.PowerPacks  
    ```  
  
    ```c#  
    using Microsoft.VisualBasic.PowerPacks;  
    ```  
  
3.  Nella routine evento, aggiungere il codice seguente:  
  
     [!CODE [VbPowerPacksTabbing#1](../CodeSnippet/VS_Snippets_VBCSharp/VbPowerPacksTabbing#1)]  
  
4.  Nella routine evento `Button1_PreviewKeyDown`, aggiungere il codice seguente:  
  
     [!CODE [VbPowerPacksTabbing#2](../CodeSnippet/VS_Snippets_VBCSharp/VbPowerPacksTabbing#2)]  
  
## Vedere anche  
 [How to: Draw Shapes with the OvalShape and RectangleShape Controls](../../../visual-basic/developing-apps/windows-forms/how-to-draw-shapes-with-the-ovalshape-and-rectangleshape-controls.md)   
 [How to: Draw Lines with the LineShape Control](../../../visual-basic/developing-apps/windows-forms/how-to-draw-lines-with-the-lineshape-control-visual-studio.md)   
 [Introduction to the Line and Shape Controls](../../../visual-basic/developing-apps/windows-forms/introduction-to-the-line-and-shape-controls-visual-studio.md)