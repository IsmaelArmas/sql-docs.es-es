---
title: SQLGetInfo (biblioteca de cursores) | Microsoft Docs
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: conceptual
helpviewer_keywords:
- SQLGetInfo function [ODBC], Cursor Library
ms.assetid: 1b4d220d-2c07-4f56-987e-36813bb1a6ce
author: MightyPen
ms.author: genemi
manager: craigg
ms.openlocfilehash: 443f8e36e4b9f537f33774a97b6d2fa0659e620d
ms.sourcegitcommit: 61381ef939415fe019285def9450d7583df1fed0
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2018
ms.locfileid: "47715903"
---
# <a name="sqlgetinfo-cursor-library"></a>SQLGetInfo (biblioteca de cursores)
> [!IMPORTANT]  
>  Esta característica se quitará en una versión futura de Windows. Evite usar esta característica en nuevos trabajos de desarrollo y piense en modificar las aplicaciones que actualmente utilizan esta característica. Microsoft recomienda usar la funcionalidad de cursor del controlador.  
  
 Este tema describe el uso de la **SQLGetInfo** función en la biblioteca de cursores. Para obtener información general sobre **SQLGetInfo**, consulte [función SQLGetInfo](../../../odbc/reference/syntax/sqlgetinfo-function.md).  
  
 La biblioteca de cursores devuelve valores para los siguientes valores de *InfoType* (&#124; representa una operación OR bit a bit); para todos los demás valores de *InfoType*, llama a **SQLGetInfo** en el controlador.  
  
|*tipo de información*|Valor devuelto|  
|----------------|--------------------|  
|SQL_BOOKMARK_PERSISTENCE|SQL_BP_SCROLL|  
|SQL_DYNAMIC_CURSOR_ATTRIBUTES1|0|  
|SQL_DYNAMIC_CURSOR_ATTRIBUTES2|0|  
|SQL_FETCH_DIRECTION [1]|SQL_FD_FETCH_ABSOLUTE &AMP;#124; SQL_FD_FETCH_FIRST &AMP;#124; SQL_FD_FETCH_LAST &AMP;#124; SQL_FD_FETCH_NEXT &AMP;#124; SQL_FD_FETCH_PRIOR &AMP;#124; SQL_FD_FETCH_RELATIVE &AMP;#124; SQL_FD_FETCH_BOOKMARK|  
|SQL_FORWARD_ONLY_CURSOR_ATTRIBUTES1|SQL_CA1_NEXT &AMP;#124; SQL_CA1_ABSOLUTE &AMP;#124; SQL_CA1_RELATIVE &AMP;#124; SQL_CA1_LOCK_NO_CHANGE &AMP;#124; SQL_CA1_POS_POSITION &AMP;#124; SQL_CA1_POSITIONED_DELETE &AMP;#124; SQL_CA1_POSITIONED_UPDATE &AMP;#124; SQL_CA1_SELECT_FOR_UPDATE|  
|SQL_FORWARD_ONLY_CURSOR_ATTRIBUTES2|SQL_CA2_READ_ONLY_CONCUR &AMP;#124; SQL_CA2_OPT_VALUES_CONCURRENCY &AMP;#124; SQL_CA2_SENSITIVITY_UPDATES|  
|SQL_GETDATA_EXTENSIONS|SQL_GD_BLOCK &#124; todos los valores devueltos por el controlador **Nota:** cuando se recuperan los datos con **SQLFetchScroll**, **SQLGetData** admite la funcionalidad especificada con las máscaras de bits SQL_GD_ANY_COLUMN y SQL_GD_BOUND.|  
|SQL_KEYSET_DRIVEN_CURSOR_ATTRIBUTES1|0|  
|SQL_KEYSET_DRIVEN_CURSOR_ATTRIBUTES2|0|  
|SQL_LOCK_TYPES [1]|SQL_LCK_NO_CHANGE|  
|SQL_STATIC_CURSOR_ATTRIBUTES1|SQL_CA1_NEXT &AMP;#124; SQL_CA1_ABSOLUTE &AMP;#124; SQL_CA1_RELATIVE &AMP;#124; SQL_CA1_BOOKMARK &AMP;#124; SQL_CA1_LOCK_NO_CHANGE &AMP;#124; SQL_CA1_POS_POSITION &AMP;#124; SQL_CA1_POSITIONED_DELETE &AMP;#124; SQL_CA1_POSITIONED_UPDATE &AMP;#124; SQL_CA1_SELECT_FOR_UPDATE|  
|SQL_STATIC_CURSOR_ATTRIBUTES2|SQL_CA2_READ_ONLY_CONCUR &AMP;#124; SQL_CA2_OPT_VALUES_ SIMULTANEIDAD &AMP;#124; SQL_CA2_SENSITIVITY_UPDATES|  
|SQL_POS_OPERATIONS [1]|SQL_POS_POSITION|  
|SQL_POSITIONED_STATEMENTS [1]|SQL_PS_POSITIONED_DELETE &AMP;#124; SQL_PS_POSITIONED_UPDATE &AMP;#124; SQL_PS_SELECT_FOR_UPDATE|  
|SQL_ROW_UPDATES|"Y"|  
|SQL_SCROLL_CONCURRENCY [1]|SQL_SCCO_READ_ONLY &AMP;#124; SQL_SCCO_OPT_VALUES|  
|SQL_SCROLL_OPTIONS|SQL_SO_FORWARD_ONLY &AMP;#124; SQL_SO_STATIC|  
|SQL_STATIC_SENSITIVITY [1]|SQL_SS_UPDATES|  
  
 [1] se usa solo cuando se usa la biblioteca de cursores con un controlador ODBC 2.x.  
  
> [!IMPORTANT]  
>  La biblioteca de cursores implementa el mismo comportamiento del cursor cuando las transacciones se confirma o revierte como origen de datos. Es decir, confirmar o revertir una transacción, ya sea mediante una llamada a **SQLEndTran** o utilizando el atributo de conexión SQL_ATTR_AUTOCOMMIT, puede hacer que el origen de datos eliminar los planes de acceso y cerrar los cursores para todas las instrucciones en una conexión. Para obtener más información, vea los tipos de información SQL_CURSOR_COMMIT_BEHAVIOR y SQL_CURSOR_ROLLBACK_BEHAVIOR en [SQLGetInfo](../../../odbc/reference/syntax/sqlgetinfo-function.md).
