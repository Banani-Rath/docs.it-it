---
title: "Type of optional value for optional parameter &lt;parametername&gt; is not CLS-compliant | Microsoft Docs"
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
  - "BC40042"
  - "vbc40042"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "BC40042"
ms.assetid: 1d6eae29-4ad3-4434-bde4-a53b6051adf5
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translationtype: Human Translation
---
# Type of optional value for optional parameter &lt;parametername&gt; is not CLS-compliant
In una routine contrassegnata come `<CLSCompliant(True)>` viene dichiarato un parametro [Optional](../../../visual-basic/language-reference/modifiers/optional.md) con valore predefinito di tipo non conforme.  
  
 Per rendere conforme una routine con [Indipendenza del linguaggio e componenti indipendenti dal linguaggio](../Topic/Language%20Independence%20and%20Language-Independent%20Components.md) \(CLS\), è necessario utilizzare solo tipi CLS conformi.  Questa regola è valida per i tipi dei parametri, il tipo restituito e i tipi di tutte le relative variabili locali.  Quanto descritto vale anche per i valori predefiniti dei parametri facoltativi.  
  
 I seguenti tipi di dati [!INCLUDE[vbprvb](../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)] non sono conformi a CLS:  
  
-   [SByte Data Type](../../../visual-basic/language-reference/data-types/sbyte-data-type.md)  
  
-   [UInteger Data Type](../../../visual-basic/language-reference/data-types/uinteger-data-type.md)  
  
-   [ULong Data Type](../../../visual-basic/language-reference/data-types/ulong-data-type.md)  
  
-   [UShort Data Type](../../../visual-basic/language-reference/data-types/ushort-data-type.md)  
  
 Quando l'attributo <xref:System.CLSCompliantAttribute> viene applicato a un elemento di programmazione, il parametro `isCompliant` dell'attributo viene impostato su `True` o `False` per indicare la conformità o la non conformità.  L'impostazione predefinita per questo parametro non è disponibile, è necessario quindi specificare un valore.  
  
 Se a un elemento non viene applicato l'<xref:System.CLSCompliantAttribute>, l'elemento non sarà considerato conforme.  
  
 Per impostazione predefinita, si tratta di un messaggio di avviso.  Per informazioni su come nascondere gli avvisi o considerarli come errori, vedere [Configurazione degli avvisi in Visual Basic](/visual-studio/ide/configuring-warnings-in-visual-basic).  
  
 **ID errore:** BC40042  
  
### Per correggere l'errore  
  
-   Per assegnare al parametro facoltativo un valore predefinito di tipo particolare, rimuovere <xref:System.CLSCompliantAttribute>.  La routine non può essere conforme a CLS.  
  
-   Per rendere la routine conforme con CLS, modificare il tipo del valore predefinito nel tipo conforme più prossimo.  Al posto di `UInteger` ad esempio potrebbe essere possibile utilizzare `Integer` se non è necessario l'intervallo di valore al di sopra di 2.147.483.647.  Se è necessario l'intervallo esteso, è possibile sostituire `UInteger` con `Long`.  
  
-   Se si prevede l'interazione con oggetti COM o di automazione, tenere presente che altri tipi presentano un'ampiezza di dati diversi da [!INCLUDE[dnprdnshort](../../../csharp/getting-started/includes/dnprdnshort_md.md)].  `int`, ad esempio, in altri ambienti è spesso rappresentato con 16 bit.  Se si accetta un valore integer a 16 bit da un componente di questo tipo, è necessario eseguirne la dichiarazione come `Short` anziché come `Integer` nel codice [!INCLUDE[vbprvb](../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)] gestito.  
  
## Vedere anche  
 [\<PAVE OVER\> Writing CLS\-Compliant Code](http://msdn.microsoft.com/it-it/4c705105-69a2-4e5e-b24e-0633bc32c7f3)