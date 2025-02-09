---
title: FreeformBuilder object (Publisher)
keywords: vbapb10.chm3342335
f1_keywords:
- vbapb10.chm3342335
ms.prod: publisher
api_name:
- Publisher.FreeformBuilder
ms.assetid: 542df9f7-f636-a98e-01de-11005b5797cc
ms.date: 05/31/2019
ms.localizationpriority: medium
---


# FreeformBuilder object (Publisher)

Represents the geometry of a freeform while it is being built.
 
## Remarks

Use the **[BuildFreeform](Publisher.Shapes.BuildFreeform.md)** method of the **Shapes** collection to return a **FreeformBuilder** object.

Use the **AddNodes** method to add nodes to the freeform. Use the **ConvertToShape** method to create the shape defined in the **FreeformBuilder** object and add it to the **Shapes** collection. 

## Example

The following example adds a freeform with four segments to the active document.

```vb
Sub CreateNewFreeFormShape() 
 With ActiveDocument.Pages(1).Shapes.BuildFreeform( _ 
 EditingType:=msoEditingCorner, X1:=360, Y1:=200) 
 .AddNodes SegmentType:=msoSegmentCurve, _ 
 EditingType:=msoEditingCorner, X1:=380, Y1:=230, _ 
 X2:=400, Y2:=250, X3:=450, Y3:=300 
 .AddNodes SegmentType:=msoSegmentCurve, _ 
 EditingType:=msoEditingAuto, X1:=480, Y1:=200 
 .AddNodes SegmentType:=msoSegmentLine, _ 
 EditingType:=msoEditingAuto, X1:=480, Y1:=400 
 .AddNodes SegmentType:=msoSegmentLine, _ 
 EditingType:=msoEditingAuto, X1:=360, Y1:=200 
 .ConvertToShape 
 End With 
End Sub
```


## Methods

- [AddNodes](Publisher.FreeformBuilder.AddNodes.md)
- [ConvertToShape](Publisher.FreeformBuilder.ConvertToShape.md)

## Properties

- [Application](Publisher.FreeformBuilder.Application.md)
- [Parent](Publisher.FreeformBuilder.Parent.md)

## See also

- [Publisher Object Model Reference](overview/publisher/object-model.md)



[!include[Support and feedback](~/includes/feedback-boilerplate.md)]