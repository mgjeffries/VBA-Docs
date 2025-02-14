---
title: FindReplace.MatchKashida property (Publisher)
keywords: vbapb10.chm8323082
f1_keywords:
- vbapb10.chm8323082
ms.prod: publisher
api_name:
- Publisher.FindReplace.MatchKashida
ms.assetid: ec2b5fa0-0549-b5c2-d8b9-666be1cbe193
ms.date: 06/07/2019
ms.localizationpriority: medium
---


# FindReplace.MatchKashida property (Publisher)

Sets or returns a **Boolean** representing whether a search operation will match kashidas. Read/write.


## Syntax

_expression_.**MatchKashida**

_expression_ A variable that represents a **[FindReplace](Publisher.FindReplace.md)** object.


## Return value

Boolean


## Remarks

This property may not be available depending on the language enabled on your operating system. The default value is **False**.

Returns **Access denied** if Arabic is not enabled.


## Example

This example finds the first occurrence of the word "" in an Arabic document matching kashidas.

```vb
Dim objDocument As Document 
 
Set objDocument = ActiveDocument 
With objDocument.Find 
 .Clear 
 .FindText = "" 
 .MatchKashida = True 
 .Execute 
End With 

```

<br/>

This example follows from the previous one except that kashidas will not be matched. Therefore the words "مــــحـــمـــــد" or "" will both be found because kashidas will be ignored.

```vb
Dim objDocument As Document 
 
Set objDocument = ActiveDocument 
With objDocument.Find 
 .Clear 
 .FindText = "مــــحـــمـــــد" 
 .MatchKashida = False 
 .Execute 
End With 

```

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]