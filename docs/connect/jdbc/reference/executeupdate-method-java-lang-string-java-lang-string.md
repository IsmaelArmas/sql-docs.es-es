---
title: Método executeUpdate (java.lang.String, java.lang.String) | Microsoft Docs
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: conceptual
apiname:
- SQLServerStatement.executeUpdate (java.lang.String[])
apilocation:
- sqljdbc.jar
apitype: Assembly
ms.assetid: 2f44a689-65c8-4c94-9574-e9c08ea7918e
author: MightyPen
ms.author: genemi
manager: craigg
ms.openlocfilehash: 83e035d659fd7b6b59c7b8d8a0799415bef5c112
ms.sourcegitcommit: 61381ef939415fe019285def9450d7583df1fed0
ms.translationtype: MTE75
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2018
ms.locfileid: "47611711"
---
# <a name="executeupdate-method-javalangstring-javalangstring"></a>Método executeUpdate (java.lang.String, java.lang.String)
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  Ejecuta la instrucción SQL dada e indica al [!INCLUDE[jdbcNoVersion](../../../includes/jdbcnoversion_md.md)] que las claves que se han generado automáticamente y están presentes en la matriz especificada deben estar disponibles para su recuperación.  
  
## <a name="syntax"></a>Sintaxis  
  
```  
  
public final int executeUpdate(java.lang.String sql,  
                               java.lang.String[] columnNames)  
```  
  
#### <a name="parameters"></a>Parámetros  
 *sql*  
  
 Un valor **String** que contiene una instrucción SQL.  
  
 *columnNames*  
  
 Una matriz de tipo **String** que indica que los nombres de columna de las claves generadas automáticamente deben estar disponibles.  
  
## <a name="return-value"></a>Valor devuelto  
 Un valor **int** que indica el número de filas afectadas; es 0 si se usa una instrucción DDL.  
  
## <a name="exceptions"></a>Excepciones  
 [SQLServerException](../../../connect/jdbc/reference/sqlserverexception-class.md)  
  
## <a name="remarks"></a>Notas  
 Este método executeUpdate especificado por el método executeUpdate de la interfaz java.sql.Statement.  
  
 Si la ejecución de un procedimiento almacenado produce un recuento de actualización mayor que uno o que genera más de un conjunto de resultados, use el método [execute](../../../connect/jdbc/reference/execute-method-sqlserverstatement.md) para ejecutar el procedimiento almacenado.  
  
## <a name="see-also"></a>Ver también  
 [Método executeUpdate &#40;SQLServerStatement&#41;](../../../connect/jdbc/reference/executeupdate-method-sqlserverstatement.md)   
 [Miembros SQLServerStatement](../../../connect/jdbc/reference/sqlserverstatement-members.md)   
 [Clase SQLServerStatement](../../../connect/jdbc/reference/sqlserverstatement-class.md)  
  
  
