---
title: "How to: Group Related Constant Values Together (Visual Basic) | Microsoft Docs"
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
  - "enumerations [Visual Basic], constants"
  - "constants, grouping together"
ms.assetid: 09d61da5-c940-4126-a79f-ba93c36653dc
caps.latest.revision: 17
caps.handback.revision: 17
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translationtype: Human Translation
---
# How to: Group Related Constant Values Together (Visual Basic)
L'enumerazione rappresenta il modo migliore per raggruppare le costanti correlate.  Per creare un'enumerazione, utilizzare l'istruzione `Enum` nella sezione dichiarazioni di una classe o di un modulo.  Per ulteriori informazioni, vedere [How to: Declare an Enumeration](../../../../visual-basic/programming-guide/language-features/constants-enums/how-to-declare-enumerations.md).  
  
### Per raggruppare i valori delle costanti correlate  
  
1.  Scrivere una dichiarazione che comprenda un livello di accesso al codice, la parola chiave `Enum` e un nome valido.  Nell'esempio riportato di seguito viene creata l'enumerazione `Private` `temperatureValues`.  
  
     [!CODE [VbEnumsTask#21](../CodeSnippet/VS_Snippets_VBCSharp/VbEnumsTask#21)]  
  
2.  Definire le costanti nell'enumerazione.  Nell'esempio riportato di seguito viene creata l'enumerazione `Public` `temperatureValues` e vengono assegnati i relativi valori.  
  
     [!CODE [VbEnumsTask#1](../CodeSnippet/VS_Snippets_VBCSharp/VbEnumsTask#1)]  
  
## Vedere anche  
 [Enumerations and Name Qualification](../../../../visual-basic/programming-guide/language-features/constants-enums/enumerations-and-name-qualification.md)   
 [How to: Refer to an Enumeration Member](../../../../visual-basic/programming-guide/language-features/constants-enums/how-to-refer-to-an-enumeration-member.md)   
 [When to Use an Enumeration](../../../../visual-basic/programming-guide/language-features/constants-enums/when-to-use-an-enumeration.md)   
 [Constants Overview](../../../../visual-basic/programming-guide/language-features/constants-enums/constants-overview.md)   
 [Constant and Literal Data Types](../../../../visual-basic/programming-guide/language-features/constants-enums/constant-and-literal-data-types.md)   
 [Constants and Enumerations](../../../../visual-basic/language-reference/constants-and-enumerations.md)