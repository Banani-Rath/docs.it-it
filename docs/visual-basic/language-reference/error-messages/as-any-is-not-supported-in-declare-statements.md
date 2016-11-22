---
title: "&#39;As Any&#39; is not supported in &#39;Declare&#39; statements | Microsoft Docs"
ms.custom: ""
ms.date: "11/16/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "bc30828"
  - "vbc30828"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "BC30828"
ms.assetid: 7e5cf519-8b64-4ac5-8116-705fe26c846d
caps.latest.revision: 11
caps.handback.revision: 11
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translationtype: Human Translation
---
# &#39;As Any&#39; is not supported in &#39;Declare&#39; statements
In Visual Basic 6.0 e versioni precedenti il tipo di dati `Any` veniva utilizzato con le istruzioni `Declare` per consentire l'utilizzo di argomenti contenenti qualsiasi tipo di dati.  Poiché in [!INCLUDE[vbprvb](../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)] è supportato l'overload, il tipo di dati `Any` è obsoleto.  
  
 **ID errore:** BC30828  
  
### Per correggere l'errore  
  
1.  Dichiarare parametri del tipo specifico che si desidera utilizzare, come nel seguente esempio.  
  
     [!CODE [VbVbalrStatements#95](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStatements#95)]  
  
2.  Utilizzare l'attributo <xref:System.Runtime.InteropServices.MarshalAsAttribute> per specificare `As Any` quando la routine chiamata prevede `Void*`.  
  
     [!CODE [VbVbalrStatements#96](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStatements#96)]  
  
## Vedere anche  
 <xref:System.Runtime.InteropServices.MarshalAsAttribute>   
 [Walkthrough: Calling Windows APIs](../../../visual-basic/programming-guide/com-interop/walkthrough-calling-windows-apis.md)   
 [Declare Statement](../../../visual-basic/language-reference/statements/declare-statement.md)   
 [Creating Prototypes in Managed Code](../Topic/Creating%20Prototypes%20in%20Managed%20Code.md)