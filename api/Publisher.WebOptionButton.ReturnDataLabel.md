---
title: WebOptionButton.ReturnDataLabel property (Publisher)
keywords: vbapb10.chm4259843
f1_keywords:
- vbapb10.chm4259843
ms.prod: publisher
api_name:
- Publisher.WebOptionButton.ReturnDataLabel
ms.assetid: 22b4a4d6-1068-2b35-d054-42bbea3f9098
ms.date: 06/18/2019
ms.localizationpriority: medium
---


# WebOptionButton.ReturnDataLabel property (Publisher)

Returns or sets a **String** that represents the text used by the webpage to label the specified web object when the page is submitted. Read/write.


## Syntax

_expression_.**ReturnDataLabel**

_expression_ A variable that represents a **[WebOptionButton](Publisher.WebOptionButton.md)** object.


## Example

This example creates a new web text box and specifies the label for the text in the text box when the page is submitted.

```vb
Sub LabelWebTextBoxControl() 
 With ActiveDocument.Pages(1).Shapes _ 
 .AddWebControl(Type:=pbWebControlSingleLineTextBox, _ 
 Left:=100, Top:=100, Width:=300, Height:=15).WebTextBox 
 .DefaultText = "Please enter your name here" 
 .Limit = 70 
 .RequiredControl = msoTrue 
 .ReturnDataLabel = "Full_Name" 
 End With 
End Sub
```

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]