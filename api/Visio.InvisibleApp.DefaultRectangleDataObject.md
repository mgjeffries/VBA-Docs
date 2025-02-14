---
title: InvisibleApp.DefaultRectangleDataObject property (Visio)
keywords: vis_sdr.chm17560050
f1_keywords:
- vis_sdr.chm17560050
ms.prod: visio
api_name:
- Visio.InvisibleApp.DefaultRectangleDataObject
ms.assetid: 3ffedd3b-e769-a8a3-e6c0-0d75f7187466
ms.date: 06/25/2019
ms.localizationpriority: medium
---


# InvisibleApp.DefaultRectangleDataObject property (Visio)

Returns an **IDataObject** interface that represents the **Rectangle** tool used in the Microsoft Visio user interface. Read-only.


## Syntax

_expression_.**DefaultRectangleDataObject**

_expression_ An expression that returns an **[InvisibleApp](Visio.InvisibleApp.md)** object.


## Return value

IDataObject


## Remarks

By using the **DefaultRectangleDataObject** property to get an **IDataObject** interface, you can create a new rectangle shape linked to data—a result similar to what you would get by dragging a data recordset row onto the page. 

This property is useful in situations where no master is selected in a docked stencil.

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]