---
title: "How to: Load XML from a File, String, or Stream (Visual Basic) | Microsoft Docs"
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
  - "XML [Visual Basic], loading"
  - "LINQ to XML [Visual Basic], loading XML from files"
ms.assetid: 2b02dcec-4cca-4575-b4ad-89ceb87b984c
caps.latest.revision: 13
caps.handback.revision: 13
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translationtype: Human Translation
---
# How to: Load XML from a File, String, or Stream (Visual Basic)
È possibile creare [XML Literals](../../../../visual-basic/language-reference/xml-literals/index.md) e popolarli con contenuti da un'origine esterna, ad esempio un file, un una stringa o un flusso, utilizzando vari metodi.  Tali metodi sono riportati nell'esempio seguente.  
  
 [!INCLUDE[note_settings_general](../../../../csharp/language-reference/compiler-messages/includes/note_settings_general_md.md)]  
  
### Per caricare XML da un file  
  
-   Per popolare un valore letterale XML come un oggetto <xref:System.Xml.Linq.XElement> o <xref:System.Xml.Linq.XDocument> da un file, utilizzare il metodo `Load`.  Questo metodo accetta come input un percorso file, un flusso di testo o un flusso XML.  
  
     Nell'esempio di codice seguente viene illustrato come utilizzare il metodo <xref:System.Xml.Linq.XDocument.Load%28System.String%29> per popolare un oggetto <xref:System.Xml.Linq.XDocument> con XML da un file di testo.  
  
     [!CODE [VbXMLSamples#43](../CodeSnippet/VS_Snippets_VBCSharp/VbXMLSamples#43)]  
  
### Per caricare XML da una stringa  
  
-   Per popolare un valore letterale XML come un oggetto <xref:System.Xml.Linq.XElement> o <xref:System.Xml.Linq.XDocument> da una stringa, utilizzare il metodo `Parse`.  
  
     Nell'esempio di codice seguente viene illustrato come utilizzare il metodo <xref:System.Xml.Linq.XDocument.Parse%28System.String%29?displayProperty=fullName> per popolare un oggetto <xref:System.Xml.Linq.XDocument> con XML da una stringa.  
  
     [!CODE [VbXMLSamples#47](../CodeSnippet/VS_Snippets_VBCSharp/VbXMLSamples#47)]  
  
### Per caricare XML da un flusso  
  
-   Per popolare un valore letterale XML come un oggetto <xref:System.Xml.Linq.XElement> o <xref:System.Xml.Linq.XDocument> da un flusso, utilizzare il metodo `Load` oppure il metodo <xref:System.Xml.Linq.XNode.ReadFrom%2A?displayProperty=fullName>.  
  
 Nell'esempio di codice seguente viene illustrato l'utilizzo del metodo <xref:System.Xml.Linq.XNode.ReadFrom%2A> per popolare un oggetto <xref:System.Xml.Linq.XDocument> con XML da un flusso XML.  
  
 [!CODE [VbXMLSamples#46](../CodeSnippet/VS_Snippets_VBCSharp/VbXMLSamples#46)]  
  
## Vedere anche  
 <xref:System.Xml.Linq.XDocument.Load%2A?displayProperty=fullName>   
 <xref:System.Xml.Linq.XElement.Load%2A?displayProperty=fullName>   
 <xref:System.Xml.Linq.XElement.Parse%2A?displayProperty=fullName>   
 <xref:System.Xml.Linq.XDocument.Parse%2A?displayProperty=fullName>   
 <xref:System.Xml.Linq.XNode.ReadFrom%2A?displayProperty=fullName>   
 [XML Literals](../../../../visual-basic/language-reference/xml-literals/index.md)   
 [XML](../../../../visual-basic/programming-guide/language-features/xml/index.md)   
 [Manipulating XML in Visual Basic](../../../../visual-basic/programming-guide/language-features/xml/manipulating-xml.md)