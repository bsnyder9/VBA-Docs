---
title: ShapeRange.ConnectorFormat property (Publisher)
keywords: vbapb10.chm2293814
f1_keywords:
- vbapb10.chm2293814
ms.prod: publisher
api_name:
- Publisher.ShapeRange.ConnectorFormat
ms.assetid: 1a1516bd-ef27-0b37-09dd-45af8a531a76
ms.date: 06/14/2019
ms.localizationpriority: medium
---


# ShapeRange.ConnectorFormat property (Publisher)

Returns a **[ConnectorFormat](Publisher.ConnectorFormat.md)** object that contains connector formatting properties. Applies to **Shape** or **ShapeRange** objects that represent connectors.


## Syntax

_expression_.**ConnectorFormat**

_expression_ A variable that represents a **[ShapeRange](Publisher.ShapeRange.md)** object.


## Example

This example adds two rectangles to the first page in the active publication and connects them with a curved connector.

```vb
Dim shpRect1 As Shape 
Dim shpRect2 As Shape 
 
With ActiveDocument.Pages(1).Shapes 
 
 ' Add two new rectangles. 
 Set shpRect1 = .AddShape(Type:=msoShapeRectangle, _ 
 Left:=100, Top:=50, Width:=200, Height:=100) 
 Set shpRect2 = .AddShape(Type:=msoShapeRectangle, _ 
 Left:=300, Top:=300, Width:=200, Height:=100) 
 
 ' Add a new curved connector. 
 With .AddConnector(Type:=msoConnectorCurve, _ 
 BeginX:=0, BeginY:=0, EndX:=100, EndY:=100) _ 
 .ConnectorFormat 
 
 ' Connect the new connector to the two rectangles. 
 .BeginConnect ConnectedShape:=shpRect1, ConnectionSite:=1 
 .EndConnect ConnectedShape:=shpRect2, ConnectionSite:=1 
 
 ' Reroute the connector to create the shortest path. 
 .Parent.RerouteConnections 
 End With 
 
End With 

```

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]