---
title: Marcadores | Microsoft Docs
description: Marcadores en el controlador OLE DB para SQL Server
ms.custom: ''
ms.date: 06/14/2018
ms.prod: sql
ms.prod_service: database-engine, sql-database, sql-data-warehouse, pdw
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
helpviewer_keywords:
- bookmarks [OLE DB]
- OLE DB Driver for SQL Server, bookmarks
- rowsets [OLE DB], bookmarks
- OLE DB rowsets, bookmarks
author: pmasl
ms.author: pelopes
manager: craigg
ms.openlocfilehash: 228aef19efd1efd6ffa2c189094d20daf35fe1d4
ms.sourcegitcommit: 61381ef939415fe019285def9450d7583df1fed0
ms.translationtype: MTE75
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2018
ms.locfileid: "47597320"
---
# <a name="bookmarks"></a>Marcadores
[!INCLUDE[appliesto-ss-asdb-asdw-pdw-md](../../../includes/appliesto-ss-asdb-asdw-pdw-md.md)]

[!INCLUDE[Driver_OLEDB_Download](../../../includes/driver_oledb_download.md)]

  Marcadores permiten a los consumidores volver rápidamente a una fila. Gracias a los marcadores, los consumidores pueden tener acceso de forma aleatoria a las filas en función del valor de marcador. La columna de marcador es la columna 0 en el conjunto de filas. El consumidor establece el valor de campo dwFlag de la estructura de enlace en DBCOLUMNSINFO_ISBOOKMARK para indicar que la columna se utiliza de marcador. El consumidor establece también la propiedad de conjunto de filas DBPROP_BOOKMARKS en VARIANT_TRUE. Esto permite que la columna 0 esté presente en el conjunto de filas. Después, se usa el método **IRowsetLocate::GetRowsAt** para capturar las filas, empezando por la fila especificada como desplazamiento desde un marcador.  
  
## <a name="see-also"></a>Ver también  
 [Conjuntos de filas](../../oledb/ole-db-rowsets/rowsets.md)  
  
  
