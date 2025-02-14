---
title: Report.DblClick event (Access)
keywords: vbaac10.chm13890
f1_keywords:
- vbaac10.chm13890
ms.prod: access
api_name:
- Access.Report.DblClick
ms.assetid: e4cd6226-8647-1a94-07a4-00ecef1ccde7
ms.date: 02/12/2019
ms.localizationpriority: medium
---


# Report.DblClick event (Access)

The **DblClick** event occurs when the user presses and releases the left mouse button twice over a report within the double-click time limit of the system.


## Syntax

_expression_.**DblClick** (_Cancel_)

_expression_ A variable that represents a **[Report](Access.Report.md)** object.


## Parameters

|Name|Required/Optional|Data type|Description|
|:-----|:-----|:-----|:-----|
| _Cancel_|Required|**Integer**|The setting determines if the **DblClick** event occurs. Setting the _Cancel_ argument to **True** (1) cancels the **DblClick** event.|

## Remarks

This event doesn't apply to check boxes, option buttons, or toggle buttons in an option group. It applies only to the option group itself.
    
This event doesn't apply to a label attached to another control, such as the label for a text box. It applies only to "freestanding" labels. Double-clicking an attached label has the same effect as double-clicking the associated control. The normal events for the control occur, not any events for the attached label.
    
To run a macro or event procedure when this event occurs, set the **OnDblClick** property to the name of the macro or to [Event Procedure].

For controls, the result of double-clicking depends on the control. For example, double-clicking a word in a text box selects the entire word. Double-clicking a control containing an OLE object starts the application used to create the object, allowing it to be edited.

If the **DblClick** event doesn't occur within the double-click time limit of the system, the form, form section, or control recognizes two **Click** events instead of a single **DblClick** event. The double-click time limit depends on the setting under **Double-Click Speed** on the **Buttons** tab of the **Mouse** option of the Windows Control Panel.

By running a macro or an event procedure when the **DblClick** event occurs, you can open a window or document when an icon is double-clicked.

Double-clicking a control causes both **Click** and **DblClick** events to occur. If the control doesn't already have the focus when you double-click it, the **Enter** and **GotFocus** events for the control occur before the **Click** and **DblClick** events.

For objects that receive mouse events, the events occur in this order:

> **MouseDown** → **MouseUp** → **Click** → **DblClick**

When you double-click a command button, the following events occur in this order:

> **MouseDown** → **MouseUp** → **Click** → **DblClick** → **MouseUp** → **Click**

The second click may have no effect (for example, if the **Click** macro or event procedure opens a modal dialog box in response to the first **Click** event). To prevent the second **Click** macro or event procedure from running, put a CancelEvent action in the **DblClick** macro or use the _Cancel_ argument in the **DblClick** event procedure. Note that  generally speaking, double-clicking a command button should be discouraged.

If you double-click any other control besides a command button, the second **Click** event doesn't occur.



[!include[Support and feedback](~/includes/feedback-boilerplate.md)]