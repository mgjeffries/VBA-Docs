---
title: Form.Caption property (Access)
keywords: vbaac10.chm13351
f1_keywords:
- vbaac10.chm13351
ms.prod: access
api_name:
- Access.Form.Caption
ms.assetid: 44dcd309-7a07-c4b3-2d85-d1bc09f98843
ms.date: 03/05/2019
ms.localizationpriority: medium
---


# Form.Caption property (Access)

Gets or sets the text that appears in the title bar in Form view. Read/write **String**.


## Syntax

_expression_.**Caption**

_expression_ A variable that represents a **[Form](Access.Form.md)** object.

## Remarks

The **Caption** property is a string expression that can contain up to 2,048 characters. Captions for forms and reports that are too long to display in the title bar are truncated.

If you don't set a caption for a form, button, or label, Microsoft Access will assign the object a unique name based on the object, such as Form1.

Use the **Caption** property to assign an access key to a label or command button. In the caption, include an ampersand (&) immediately preceding the character that you want to use as an access key. The character will be underlined. You can press Alt plus the underlined character to move the focus to that control on a form.

Include two ampersands (&&) in the setting for a caption if you want to display an ampersand itself in the caption text. For example, to display **Save & Exit**, you should type **Save && Exit** in the **Caption** property box.


[!include[Support and feedback](~/includes/feedback-boilerplate.md)]


