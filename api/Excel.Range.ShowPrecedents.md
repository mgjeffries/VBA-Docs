---
title: Range.ShowPrecedents method (Excel)
keywords: vbaxl10.chm144198
f1_keywords:
- vbaxl10.chm144198
ms.prod: excel
api_name:
- Excel.Range.ShowPrecedents
ms.assetid: 02b8ca94-d251-a6be-1551-1ba769c3c0fa
ms.date: 05/11/2019
ms.localizationpriority: medium
---


# Range.ShowPrecedents method (Excel)

Draws tracer arrows to the direct precedents of the range.


## Syntax

_expression_.**ShowPrecedents** (_Remove_)

_expression_ A variable that represents a **[Range](excel.range(object).md)** object.


## Parameters

|Name|Required/Optional|Data type|Description|
|:-----|:-----|:-----|:-----|
| _Remove_|Optional| **Variant**| **True** to remove one level of tracer arrows to direct precedents. **False** to expand one level of tracer arrows. The default value is **False**.|

## Return value

Variant


## Example

This example draws tracer arrows to the precedents of the active cell on Sheet1.

```vb
Worksheets("Sheet1").Activate 
ActiveCell.ShowPrecedents
```

<br/>

This example removes the tracer arrow for one level of precedents of the active cell on Sheet1.

```vb
Worksheets("Sheet1").Activate 
ActiveCell.ShowPrecedents remove:=True
```



[!include[Support and feedback](~/includes/feedback-boilerplate.md)]