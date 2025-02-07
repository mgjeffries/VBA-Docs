---
title: StartUpPosition property (Visual Basic for Applications)
keywords: vblr6.chm1100523
f1_keywords:
- vblr6.chm1100523
ms.prod: office
api_name:
- Office.StartUpPosition
ms.assetid: 0ceb1e6d-b45e-a1df-03df-fd73ce814a79
ms.date: 12/19/2018
ms.localizationpriority: medium
---


# StartUpPosition property

Returns or sets a value specifying the position of a **[UserForm](userform-window.md)** when it first appears.
Use one of four settings for **StartUpPosition**.

<br/>

|Setting|Value|Description|
|:-----|:-----|:-----|
|**Manual**|0|No initial setting specified.|
|**CenterOwner**|1|Center on the item to which the **UserForm** belongs.|
|**CenterScreen**|2|Center on the whole screen.|
|**WindowsDefault**|3|Position in upper-left corner of screen.|

## Remarks

You can set the **StartUpPosition** property programmatically or from the [Properties window](properties-window.md).

## Example

The following example uses the **[Load](load-statement.md)** statement and the **[Show](show-method.md)** method in UserForm1's Click event to load UserForm2 with the **StartUpPosition** property set to 3 (the Windows default position). The **Show** method then makes UserForm2 visible.


```vb
Private Sub UserForm_Click()
    Load UserForm2
    UserForm2.StartUpPosition = 3
    UserForm2.Show
End Sub
```

## See also

- [Objects (Visual Basic for Applications)](../objects-visual-basic-for-applications.md)
- [Visual Basic language reference](visual-basic-language-reference.md)

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]
