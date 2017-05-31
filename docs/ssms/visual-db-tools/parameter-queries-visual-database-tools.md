---
title: "Consultas con parámetros (Visual Database Tools) | Microsoft Docs"
ms.custom: 
ms.date: 01/19/2017
ms.prod: sql-non-specified
ms.reviewer: 
ms.suite: 
ms.technology:
- tools-ssms
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- parameter queries [SQL Server]
ms.assetid: 4897c41a-324a-47b8-a30b-cbc9e9e19a8b
caps.latest.revision: 3
author: stevestein
ms.author: sstein
manager: jhubbard
translationtype: Human Translation
ms.sourcegitcommit: 2edcce51c6822a89151c3c3c76fbaacb5edd54f4
ms.openlocfilehash: 1d7b5cf2ad2bd8c96f98892334e76b076dbb16a7
ms.lasthandoff: 04/11/2017

---
# <a name="parameter-queries-visual-database-tools"></a>Consultas con parámetros (Visual Database Tools)
En algunos casos, tal vez necesite crear una consulta que pueda utilizar en muchas ocasiones, pero con un valor diferente cada vez. Por ejemplo, puede ejecutar habitualmente una consulta para buscar todos los `title_ids` escritos por un autor. Puede ejecutar la misma consulta para cada solicitud, con la salvedad de que el nombre o el Id. del autor serán diferentes cada vez.  
  
Para crear una consulta que pueda tener valores diferentes en distintas ocasiones, puede utilizar parámetros en la consulta. Un parámetro es un marcador de posición para un valor que se proporciona al ejecutar la consulta. Una instrucción SQL con un parámetro puede presentar el siguiente aspecto ("?" representaría el parámetro del Id. del autor):  
  
```  
SELECT title_id  
FROM titleauthor  
WHERE (au_id = ?)  
```  
  
## <a name="where-you-can-use-parameters"></a>Cuándo se pueden utilizar parámetros  
Puede utilizar parámetros como marcadores de posición para valores literales: tanto para valores de texto como para valores numéricos. Generalmente, los parámetros se utilizan como marcadores de posición en condiciones de búsqueda para filas individuales o para grupos (es decir, en las cláusulas WHERE o HAVING de una instrucción SQL).  
  
Se pueden utilizar parámetros como marcadores de posición en expresiones. Por ejemplo, si desea calcular precios con descuento, proporcione un valor de descuento distinto cada vez que ejecute una consulta. Para hacerlo, puede especificar la siguiente expresión:  
  
```  
(price * ?)  
```  
  
## <a name="specifying-unnamed-and-named-parameters"></a>Especificar parámetros con nombre y sin nombre  
Puede especificar dos tipos de parámetros: con nombre y sin nombre. Un parámetro sin nombre es un signo de interrogación de cierre (?) que se coloca en cualquier parte de la consulta en que se desea solicitar o sustituir un valor literal. Por ejemplo, si utiliza un parámetro sin nombre para buscar el Id. de un autor en la tabla `titleauthor` , la instrucción resultante en el [panel SQL](../../ssms/visual-db-tools/sql-pane-visual-database-tools.md) podría tener el siguiente aspecto:  
  
```  
SELECT title_id  
FROM titleauthor  
WHERE (au_id = ?)  
```  
  
Cuando ejecute la consulta en el [Diseñador de consultas y vistas](../../ssms/visual-db-tools/query-and-view-designer-tools-visual-database-tools.md), el [cuadro de diálogo Parámetros de la consulta](../../ssms/visual-db-tools/query-parameters-dialog-box-visual-database-tools.md) mostrará "?" como nombre del parámetro.  
  
Como alternativa, puede asignar un nombre a un parámetro. Los parámetros con nombre son especialmente útiles si dispone de varios parámetros en una consulta. Por ejemplo, si utiliza parámetros con nombre para buscar el nombre y los apellidos de un autor en la tabla `authors` , la instrucción resultante en el panel SQL podría presentar este aspecto:  
  
```  
SELECT au_id  
FROM authors  
WHERE au_fname = %first name% AND  
      au_lname = %last name%  
```  
  
> [!TIP]  
> Debe definir caracteres de prefijo y de sufijo antes de crear una consulta de parámetros con nombre.  
  
Cuando ejecute la consulta en el Diseñador de consultas y vistas, el [cuadro de diálogo Parámetros de la consulta](../../ssms/visual-db-tools/query-parameters-dialog-box-visual-database-tools.md) mostrará una lista de parámetros con nombre.  
  
## <a name="see-also"></a>Vea también  
[Realizar consultas con parámetros &amp;#40;Visual Database Tools&amp;#41;](../../ssms/visual-db-tools/query-with-parameters-visual-database-tools.md)  
[Tipos de consultas compatibles &amp;#40;Visual Database Tools&amp;#41;](../../ssms/visual-db-tools/supported-query-types-visual-database-tools.md)  
[Temas de procedimientos de diseño de consultas y vistas &amp;#40;Visual Database Tools&amp;#41;](../../ssms/visual-db-tools/design-queries-and-views-how-to-topics-visual-database-tools.md)  
  
