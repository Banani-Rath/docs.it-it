---
title: "How to: Embed Expressions in XML Literals (Visual Basic) | Microsoft Docs"
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
  - "embedded expressions [Visual Basic]"
  - "XML literals [Visual Basic], embedded expressions"
ms.assetid: 75016fad-0141-42de-8564-5051be29487e
caps.latest.revision: 16
caps.handback.revision: 16
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translationtype: Human Translation
---
# How to: Embed Expressions in XML Literals (Visual Basic)
È possibile combinare i valori letterali XML con le espressioni incorporate per creare un documento, un frammento o un elemento XML che contengono il contenuto creato in fase di esecuzione.  Negli esempi seguenti viene illustrato come utilizzare le espressioni incorporate per popolare in fase di esecuzione contenuto dell'elemento, gli attributi e i nomi dell'elemento.  
  
 La sintassi per un'espressione incorporata è `<%=``exp``%>`, che è la stessa sintassi che utilizza [!INCLUDE[vstecasp](../../../../csharp/language-reference/preprocessor-directives/includes/vstecasp_md.md)]. Per ulteriori informazioni, vedere [Embedded Expressions in XML](../../../../visual-basic/programming-guide/language-features/xml/embedded-expressions-in-xml.md).  
  
 È inoltre possibile utilizzare le API [!INCLUDE[sqltecxlinq](../../../../csharp/programming-guide/concepts/linq/includes/sqltecxlinq_md.md)] per creare oggetti [!INCLUDE[sqltecxlinq](../../../../csharp/programming-guide/concepts/linq/includes/sqltecxlinq_md.md)].  Per ulteriori informazioni, vedere <xref:System.Xml.Linq.XElement>.  
  
## Procedure  
  
#### Inserire testo come contenuto dell'elemento  
  
-   Nell'esempio seguente viene illustrato come inserire il testo contenuto nella variabile `contactName` tra gli elementi nomi di apertura e chiusura.  
  
     [!CODE [VbXMLSamples#39](../CodeSnippet/VS_Snippets_VBCSharp/VbXMLSamples#39)]  
  
     Questo esempio produce il seguente output:  
  
    ```  
    <contact>  
      <name>Patrick Hines</name>  
    </contact>  
    ```  
  
#### Inserire testo come valore dell'attributo  
  
-   Nell'esempio seguente viene illustrato come inserire il testo contenuto nella variabile `phoneType` come valore dell'attributo di `type`.  
  
     [!CODE [VbXMLSamples#40](../CodeSnippet/VS_Snippets_VBCSharp/VbXMLSamples#40)]  
  
     Questo esempio produce il seguente output:  
  
    ```  
    <contact>  
      <phone type="home">206-555-0144</phone>  
    </contact>  
    ```  
  
#### Inserire testo per un nome di elemento  
  
-   Nell'esempio seguente viene illustrato come inserire il testo contenuto nella variabile `elementName` come nome di un elemento.  
  
     Quando si creano elementi utilizzando questa tecnica, è necessario chiuderli con il tag \<\/\>.  
  
     [!CODE [VbXMLSamples#41](../CodeSnippet/VS_Snippets_VBCSharp/VbXMLSamples#41)]  
  
     Questo esempio produce il seguente output:  
  
    ```  
    <contact>  
      <name>Patrick Hines</name>  
    </contact>  
    ```  
  
## Vedere anche  
 [How to: Create XML Literals](../../../../visual-basic/programming-guide/language-features/xml/how-to-create-xml-literals.md)   
 [Embedded Expressions in XML](../../../../visual-basic/programming-guide/language-features/xml/embedded-expressions-in-xml.md)   
 [Creating XML in Visual Basic](../../../../visual-basic/programming-guide/language-features/xml/creating-xml.md)   
 [XML](../../../../visual-basic/programming-guide/language-features/xml/index.md)