---
title: SENO (Transact-SQL) | Documentos de Microsoft
ms.custom: 
ms.date: 03/03/2017
ms.prod: sql-non-specified
ms.reviewer: 
ms.suite: 
ms.technology:
- database-engine
ms.tgt_pltfrm: 
ms.topic: language-reference
f1_keywords:
- SIN_TSQL
- SIN
dev_langs:
- TSQL
helpviewer_keywords:
- SIN function
- sine
ms.assetid: bc1781e9-185f-4981-929b-e77371be6b26
caps.latest.revision: 21
author: BYHAM
ms.author: rickbyh
manager: jhubbard
ms.translationtype: MT
ms.sourcegitcommit: 876522142756bca05416a1afff3cf10467f4c7f1
ms.openlocfilehash: 42affad02c7bb85447e52f975ef992bab37dd474
ms.contentlocale: es-es
ms.lasthandoff: 09/01/2017

---
# <a name="sin-transact-sql"></a>SIN (Transact-SQL)
[!INCLUDE[tsql-appliesto-ss2008-all_md](../../includes/tsql-appliesto-ss2008-all-md.md)]

  Devuelve el seno trigonométrico del ángulo especificado, en radianes y en un valor numérico aproximado, **float**, expresión.  
  
 ![Icono de vínculo de tema](../../database-engine/configure-windows/media/topic-link.gif "Icono de vínculo de tema") [Convenciones de sintaxis de Transact-SQL](../../t-sql/language-elements/transact-sql-syntax-conventions-transact-sql.md)  
  
## <a name="syntax"></a>Sintaxis  
  
```  
-- Syntax for SQL Server, Azure SQL Database, Azure SQL Data Warehouse, Parallel Data Warehouse  
  
SIN ( float_expression )  
```  
  

## <a name="arguments"></a>Argumentos  
 *float_expression*  
 Es un [expresión](../../t-sql/language-elements/expressions-transact-sql.md) de tipo **float** o de un tipo que puede convertirse implícitamente a float.  
  
## <a name="return-types"></a>Tipos devueltos  
 **float**  
  
## <a name="examples"></a>Ejemplos  
 En el ejemplo siguiente se calcula el seno de un ángulo especificado.  
  
```  
DECLARE @angle float;  
SET @angle = 45.175643;  
SELECT 'The SIN of the angle is: ' + CONVERT(varchar,SIN(@angle));  
GO  
```  
  
 [!INCLUDE[ssResult](../../includes/ssresult-md.md)]  
  
```  
The SIN of the angle is: 0.929607                         
  
(1 row(s) affected)  
```  
  
## <a name="examples-includesssdwfullincludessssdwfull-mdmd-and-includesspdwincludessspdw-mdmd"></a>Ejemplos: [!INCLUDE[ssSDWfull](../../includes/sssdwfull-md.md)] y[!INCLUDE[ssPDW](../../includes/sspdw-md.md)]  
 En el ejemplo siguiente se calcula el seno de un ángulo especificado.  
  
```  
SELECT SIN(45.175643);  
```  
  
 [!INCLUDE[ssResult](../../includes/ssresult-md.md)]  
  
 `---------`  
  
 `0.929607`  
  
## <a name="see-also"></a>Vea también  
 [Funciones matemáticas &#40; Transact-SQL &#41;](../../t-sql/functions/mathematical-functions-transact-sql.md)  
  
  

