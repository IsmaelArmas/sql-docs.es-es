---
title: Usar el modo RAW con FOR XML | Microsoft Docs
ms.custom: ''
ms.date: 06/13/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.technology: xml
ms.topic: conceptual
helpviewer_keywords:
- FOR XML RAW mode
- XMLSCHEMA option
- FOR XML clause, RAW mode
- RAW FOR XML mode
- ELEMENTS directive
- RAW mode
- XMLDATA option
ms.assetid: 02c1bc0b-760c-4589-9ab1-6927c6d9c734
author: douglaslMS
ms.author: douglasl
manager: craigg
ms.openlocfilehash: d074ad6fe9dcd3a26a9c9be84a326291df9f5aed
ms.sourcegitcommit: 3da2edf82763852cff6772a1a282ace3034b4936
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/02/2018
ms.locfileid: "48084247"
---
# <a name="use-raw-mode-with-for-xml"></a>Usar el modo RAW con FOR XML
  El modo RAW transforma cada fila del conjunto de resultados de la consulta en un elemento XML que tiene el identificador genérico \<row> o el nombre del elemento, que se proporciona de manera opcional. De forma predeterminada, cada valor de columna del conjunto de filas que no es NULL se asigna a un atributo del elemento \<row>. Si se agrega la directiva ELEMENTS a la cláusula FOR XML, cada valor de columna se asigna a un subelemento del elemento \<row>. Opcionalmente, junto con la directiva ELEMENTS se puede especificar la opción XSINIL para asignar los valores de columna NULL del conjunto de resultados a un elemento que tenga el atributo, xsi:nil=`"`true`"`.  
  
 Se puede solicitar un esquema para el XML resultante. Si se especifica la opción XMLDATA se devuelve un esquema XDR en línea. Si se especifica la opción XMLSCHEMA se devuelve un esquema XSD en línea. El esquema aparece al principio de los datos. En el resultado, la referencia al espacio de nombres del esquema se repite en todos los elementos de nivel superior.  
  
 La opción BINARY BASE64 se debe especificar en la cláusula FOR XML para devolver los datos binarios en formato codificado en base 64. En el modo RAW, si se recuperan los datos binarios sin especificar la opción BINARY BASE64, se produce un error.  
  
## <a name="in-this-section"></a>En esta sección  
 Esta sección contiene los siguientes ejemplos:  
  
-   [Ejemplo: Recuperar información de modelos de productos como XML](example-retrieving-product-model-information-as-xml.md)  
  
-   [Ejemplo: Especificar XSINIL con la directiva ELEMENTS](example-specifying-xsinil-with-the-elements-directive.md)  
  
-   [Ejemplo: solicitar esquemas como resultados con las opciones XMLDATA y XMLSCHEMA](example-requesting-schemas-as-results-with-the-xmldata-and-xmlschema-options.md)  
  
-   [Ejemplo: Recuperar datos binarios](example-retrieving-binary-data.md)  
  
-   [Ejemplo: Cambiar el nombre del elemento &#60;row&#62;](example-renaming-the-row-element.md)  
  
-   [Ejemplo: Especificar un elemento raíz para el XML generado por FOR XML](example-specifying-a-root-element-for-the-xml-generated-by-for-xml.md)  
  
-   [Ejemplo: Consultar columnas de tipo XML](example-querying-xmltype-columns.md)  
  
## <a name="see-also"></a>Vea también  
 [Agregar espacios de nombres a consultas con WITH XMLNAMESPACES](add-namespaces-to-queries-with-with-xmlnamespaces.md)   
 [Usar el modo AUTO con FOR XML](use-auto-mode-with-for-xml.md)   
 [Usar el modo EXPLICIT con FOR XML](use-explicit-mode-with-for-xml.md)   
 [Usar el modo PATH con FOR XML](use-path-mode-with-for-xml.md)   
 [SELECT &#40;Transact-SQL&#41;](/sql/t-sql/queries/select-transact-sql)   
 [FOR XML &#40;SQL Server&#41;](../xml/for-xml-sql-server.md)  
  
  
