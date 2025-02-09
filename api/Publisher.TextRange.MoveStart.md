---
title: TextRange.MoveStart method (Publisher)
keywords: vbapb10.chm5308423
f1_keywords:
- vbapb10.chm5308423
ms.prod: publisher
api_name:
- Publisher.TextRange.MoveStart
ms.assetid: 5a9c480b-3cb7-0fd8-59c0-e2f93a925164
ms.date: 06/15/2019
ms.localizationpriority: medium
---


# TextRange.MoveStart method (Publisher)

Moves the start position of the specified range. This method returns a **Long** that indicates the number of units by which the start position or the range or selection actually moved, or it returns 0 (zero) if the move was unsuccessful.


## Syntax

_expression_.**MoveStart** (_Unit_, _Size_)

_expression_ A variable that represents a **[TextRange](Publisher.TextRange.md)** object.


## Parameters

|Name|Required/Optional|Data type|Description|
|:-----|:-----|:-----|:-----|
|_Unit_|Required| **[PbTextUnit](publisher.pbtextunit.md)**|The unit by which the collapsed range or selection is to be moved. Can be one of the **PbTextUnit** constants declared in the Microsoft Publisher type library.|
|_Size_|Required| **Long**|The number of units to move. If this number is positive, the ending character position is moved forward in the document. If this number is negative, the end is moved backward. If the ending position overtakes the starting position, the range collapses and both character positions move together.|

## Return value

Long


## Example

This example sets a text range, moves the range's starting and ending character positions, and then formats the font for the range.

```vb
Sub MoveStartEnd() 
 Dim rngText As TextRange 
 
 Set rngText = ActiveDocument.Pages(1).Shapes(1).TextFrame _ 
 .TextRange.Paragraphs(Start:=3, Length:=1) 
 
 With rngText 
 .MoveStart Unit:=pbTextUnitLine, Size:=-2 
 .MoveEnd Unit:=pbTextUnitLine, Size:=1 
 With .Font 
 .Bold = msoTrue 
 .Size = 15 
 End With 
 End With 
 
End Sub
```

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]