---
title: Chart.SetDefaultChart method (Project)
ms.prod: project-server
ms.assetid: e0586f53-9ca4-7d06-97ed-ecc418644d9d
ms.date: 06/08/2017
ms.localizationpriority: medium
---


# Chart.SetDefaultChart method (Project)
Specifies the name of the default chart template that Project uses when creating new charts.

## Syntax

_expression_. `SetDefaultChart` _(varName)_

_expression_ A variable that represents a **[Chart](Project.Chart.md)** object.


## Parameters



|Name|Required/Optional|Data type|Description|
|:-----|:-----|:-----|:-----|
| _varName_|Required|**Variant**|The name of the chart template. The name can be a string for the name of a chart in the gallery or a user-defined template, or the name can be a constant for a built-in chart template.|
| _varName_|Required|**Variant**||

## Return value

 **Nothing**


## See also


[Chart Object](Project.chart.md)
[SaveChartTemplate Method](Project.chart.savecharttemplate.md)

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]