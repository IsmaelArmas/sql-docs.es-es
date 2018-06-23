---
title: Agregar columnas a una tabla (motor de base de datos) | Microsoft Docs
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
- inserting columns
- columns [SQL Server], adding
- adding columns
ms.assetid: abeb8d52-d562-4e29-9e1e-2923ae874859
caps.latest.revision: 17
author: craigg-msft
ms.author: craigg
manager: jhubbard
ms.openlocfilehash: 08e262af1a2e424f497aa39e7b136c62cb5ac09c
ms.sourcegitcommit: 5dd5cad0c1bbd308471d6c885f516948ad67dfcf
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2018
ms.locfileid: "36105112"
---
# <a name="add-columns-to-a-table-database-engine"></a>Agregar columnas a una tabla (motor de base de datos)
  En este tema se describe cómo agregar nuevas columnas a una tabla en [!INCLUDE[ssCurrent](../../includes/sscurrent-md.md)] mediante [!INCLUDE[ssManStudioFull](../../includes/ssmanstudiofull-md.md)] o [!INCLUDE[tsql](../../includes/tsql-md.md)].  
  
 **En este tema**  
  
-   **Antes de empezar:**  
  
     [Limitaciones y restricciones](#Restrictions)  
  
     [Seguridad](#Security)  
  
-   **Para insertar columnas con:**  
  
     [SQL Server Management Studio](#SSMSProcedure)  
  
     [Transact-SQL](#TsqlProcedure)  
  
##  <a name="BeforeYouBegin"></a> Antes de empezar  
  
###  <a name="Restrictions"></a> Limitaciones y restricciones  
 Al usar la instrucción ALTER TABLE para agregar columnas a una tabla, se agregan automáticamente las columnas al final de la tabla. Si desea que las columnas aparezcan en un orden concreto en la tabla, use [!INCLUDE[ssManStudioFull](../../includes/ssmanstudiofull-md.md)]. Sin embargo, tenga en cuenta que esto no es un procedimiento recomendado del diseño de base de datos. El procedimiento recomendado es especificar el orden en que las columnas se devuelven en el nivel de aplicación y de consulta. No debe confiar en el uso de SELECT * para devolver todas las columnas en un orden esperado según el orden en que están definidos en la tabla. Especifique siempre las columnas por nombre en las consultas y aplicaciones en el orden en que desea que aparezcan.  
  
###  <a name="Security"></a> Seguridad  
  
####  <a name="Permissions"></a> Permissions  
 Requiere el permiso ALTER en la tabla.  
  
##  <a name="SSMSProcedure"></a> Usar SQL Server Management Studio  
  
#### <a name="to-insert-columns-into-a-table-with-table-designer"></a>Para insertar columnas en una tabla con el Diseñador de tablas  
  
1.  En el **Explorador de objetos**, haga clic con el botón derecho en la tabla a la que quiera agregar columnas y elija **Diseño**.  
  
2.  Haga clic en la primera celda vacía de la columna **Nombre de columna** .  
  
3.  Escriba el nombre de columna en la celda. El nombre de la columna es un valor obligatorio.  
  
4.  Presione la tecla TAB para desplazarse a la celda **Tipo de datos** y seleccione un tipo de datos en el menú desplegable. Este valor también es obligatorio, por lo que si no elige ninguno, se le asignará un valor predeterminado.  
  
    > [!NOTE]  
    >  Puede cambiar el valor predeterminado en el cuadro de diálogo **Opciones** situado bajo **Herramientas para bases de datos**.  
  
5.  Continúe definiendo las propiedades de la columna en la pestaña **Propiedades de columna** .  
  
    > [!NOTE]  
    >  Los valores predeterminados de las propiedades de la columna se agregan cuando crea una columna nueva, pero se pueden cambiar en la pestaña **Propiedades de columna** .  
  
6.  Cuando haya terminado de agregar columnas, en la **archivo** menú, elija **guardar *** nombre de la tabla*.  
  
##  <a name="TsqlProcedure"></a> Usar Transact-SQL  
  
#### <a name="to-insert-columns-into-a-table"></a>Para insertar columnas en una tabla  
  
1.  Conéctese con el [!INCLUDE[ssDE](../../includes/ssde-md.md)].  
  
2.  En la barra Estándar, haga clic en **Nueva consulta**.  
  
3.  El ejemplo siguiente agrega dos columnas a la tabla `dbo.doc_exa`. Copie y pegue el siguiente ejemplo en la ventana de consulta y haga clic en **Ejecutar**.  
  
```  
ALTER TABLE dbo.doc_exa ADD column_b VARCHAR(20) NULL, column_c INT NULL ;  
```  
  
##  <a name="FollowUp"></a> Para obtener más información, consulte [ALTER TABLE &#40;Transact-SQL&#41;](/sql/t-sql/statements/alter-table-transact-sql)  
  
  