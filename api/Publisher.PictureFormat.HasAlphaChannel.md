---
title: PictureFormat.HasAlphaChannel property (Publisher)
keywords: vbapb10.chm3604758
f1_keywords:
- vbapb10.chm3604758
ms.prod: publisher
api_name:
- Publisher.PictureFormat.HasAlphaChannel
ms.assetid: 97739201-cd0d-cc78-a28e-935fb11da5b3
ms.date: 06/12/2019
ms.localizationpriority: medium
---


# PictureFormat.HasAlphaChannel property (Publisher)

Returns an **[MsoTriState](office.msotristate.md)** constant indicating whether the specified picture contains an alpha channel. Read-only.


## Syntax

_expression_.**HasAlphaChannel**

_expression_ A variable that represents a **[PictureFormat](Publisher.PictureFormat.md)** object.


## Return value

MsoTriState


## Remarks

An alpha channel is a special 8-bit channel used by some image processing software to contain additional data, such as masking or transparency information.

The **HasAlphaChannel** property value can be one of the **MsoTriState** constants declared in the Microsoft Office type library and shown in the following table.

|Constant|Description|
|:-----|:-----|
| **msoFalse**|The specified picture does not contain an alpha channel.|
| **msoTriStateMixed**|Indicates a combination of **msoTrue** and **msoFalse** for the specified shape range.|
| **msoTrue**|The specified picture contains an alpha channel.|

## Example

The following example returns whether the first shape on the first page of the active publication contains an alpha channel. If the picture is linked, and the original picture contains an alpha channel, that is also returned. This example assumes that the shape is a picture.

```vb
With ActiveDocument.Pages(1).Shapes(1).PictureFormat 
 If .HasAlphaChannel = msoTrue Then 
 Debug.Print .Filename 
 Debug.Print "This picture contains an alpha channel." 
 
 If .IsLinked = msoTrue Then 
 If .OriginalHasAlphaChannel = msoTrue Then 
 Debug.Print "The linked picture " & _ 
 "also contains an alpha channel." 
 End If 
 End If 
 End If 
End With 

```

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]