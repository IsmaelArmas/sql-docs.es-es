---
title: Quite las referencias a las tablas del sistema no documentadas | Documentos de Microsoft
ms.custom: ''
ms.date: 06/13/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.suite: ''
ms.technology:
- database-engine
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- undocumented system tables [SQL Server]
- system tables [SQL Server]
ms.assetid: 010b1236-2219-4bf4-a6db-e3fc3abfa37a
caps.latest.revision: 28
author: JennieHubbard
ms.author: jhubbard
manager: jhubbard
ms.openlocfilehash: cd8ff349ae3e065233ea104d34016a919b9fd6e7
ms.sourcegitcommit: 5dd5cad0c1bbd308471d6c885f516948ad67dfcf
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2018
ms.locfileid: "36202430"
---
# <a name="remove-references-to-undocumented-system-tables"></a>Quitar referencias a tablas del sistema no documentadas
  Muchas tablas del sistema que no estaban documentadas en las versiones anteriores han cambiado o ya no existen; por consiguiente, si se utilizan dichas tablas, se pueden producir errores tras la actualización. Dado que el Asesor de actualizaciones busca referencias a nombres de tablas del sistema, le informará sobre aquellas referencias a tablas del usuario que tengan el mismo nombre que una tabla del sistema.  
  
## <a name="component"></a>Componente  
 [!INCLUDE[ssDE](../../includes/ssde-md.md)]  
  
## <a name="description"></a>Descripción  
 Las siguientes tablas del sistema no documentadas se han quitado:  
  
-   **spt_datatype_info**  
  
-   **spt_datatype_info_ext**  
  
-   **spt_provider_types**  
  
-   **spt_server_info**  
  
-   **spt_values**  
  
-   **sysfulltextnotify**  
  
-   **syslocks**  
  
-   **sysproperties**  
  
-   **sysprotects_aux**  
  
-   **sysprotects_view**  
  
-   **SYSREMOTE_CATALOGS**  
  
-   **SYSREMOTE_COLUMN_PRIVILEGES**  
  
-   **SYSREMOTE_COLUMNS**  
  
-   **SYSREMOTE_FOREIGN_KEYS**  
  
-   **SYSREMOTE_INDEXES**  
  
-   **SYSREMOTE_PRIMARY_KEYS**  
  
-   **SYSREMOTE_PROVIDER_TYPES**  
  
-   **SYSREMOTE_SCHEMATA**  
  
-   **SYSREMOTE_STATISTICS**  
  
-   **SYSREMOTE_TABLE_PRIVILEGES**  
  
-   **SYSREMOTE_TABLES**  
  
-   **SYSREMOTE_VIEWS**  
  
-   **syssegments**  
  
-   **sysxlogins**  
  
## <a name="corrective-action"></a>Acción correctora  
 Modifique las aplicaciones según la tabla siguiente.  
  
|En lugar de|Utilice|  
|----------------|---------|  
|**sysfulltextnotify**|La propiedad**TableFulltextPendingChanges** de la función OBJECTPROPERTYEX.|  
|**syslocks**|La vista de administración dinámica**sys.dm_tran_locks** , sp_lock o la vista de compatibilidad **sys.syslockinfo** .|  
|**sysproperties**|La vista de catálogo**sys.extended_properties** o la función **fn_listextendedproperty** |  
|**sysxlogins**|La vista de catálogo**sys.server_principals** o la vista de compatibilidad **syslogins** .|  
|todas las tablas **spt_**|Ningún reemplazo disponible|  
  
## <a name="see-also"></a>Vea también  
 [Problemas de actualización de motor de base de datos](../../../2014/sql-server/install/database-engine-upgrade-issues.md)   
 [Asesor de actualizaciones de SQL Server 2014 &#91;nuevo&#93;](/sql/2014/sql-server/install/sql-server-2014-upgrade-advisor)  
  
  