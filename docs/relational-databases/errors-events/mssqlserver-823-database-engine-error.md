---
title: 'MSSQLSERVER: error del Motor de base de datos | Microsoft Docs'
ms.custom: 
ms.date: 04/04/2017
ms.prod: sql-server-2016
ms.reviewer: 
ms.suite: 
ms.technology:
- database-engine
ms.tgt_pltfrm: 
ms.topic: language-reference
helpviewer_keywords:
- 823 (Database Engine error)
ms.assetid: 0d9fce3c-3772-46ce-a7a3-4f4988dc6cae
caps.latest.revision: 24
author: BYHAM
ms.author: rickbyh
manager: jhubbard
ms.translationtype: Human Translation
ms.sourcegitcommit: 2edcce51c6822a89151c3c3c76fbaacb5edd54f4
ms.openlocfilehash: 9e44f9347c238f4522bcb1161d6b75ed2bb990b3
ms.contentlocale: es-es
ms.lasthandoff: 04/11/2017

---
# <a name="mssqlserver---database-engine-error"></a>MSSQLSERVER: error del Motor de base de datos
  
## <a name="details"></a>Detalles  
  
|||  
|-|-|  
|Nombre del producto|SQL Server|  
|Identificador del evento|823|  
|Origen del evento|MSSQLSERVER|  
|Componente|SQLEngine|  
|Nombre simbólico|B_HARDERR|  
|Texto del mensaje|El sistema operativo ha devuelto el error %ls en SQL Server durante %S_MSG en el desplazamiento %#016I64x del archivo '%ls'. Encontrará más detalles en los mensajes adicionales del registro de errores de SQL Server y el registro de eventos del sistema. Se trata de una condición de error grave de nivel de sistema que amenaza a la integridad de la base de datos y que debe corregirse inmediatamente. Ejecute una comprobación de coherencia completa de la base de datos (DBCC CHECKDB). Este error puede deberse a muchos factores. Para obtener más información vea los Libros en pantalla de SQL Server.|  
  
## <a name="explanation"></a>Explicación  
Error de solicitud de lectura o escritura de Windows. El código de error devuelto por Windows y el texto correspondiente se insertan en el mensaje. En el caso de la solicitud de lectura, [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] ya la habrá intentado cuatro veces. Suele ser el resultado de un error de hardware, pero puede estar causado por el controlador del dispositivo. Para obtener más información sobre el error 823, vea [http://support.microsoft.com/kb/828339](http://support.microsoft.com/kb/828339). Para obtener más información sobre los errores de E/S, vea el [capítulo 2 del documento sobre conceptos básicos de E/S de Microsoft SQL Server](http://go.microsoft.com/fwlink/?LinkId=69370).  
  
## <a name="user-action"></a>Acción del usuario  
Busque información adicional en el registro de eventos del sistema. Póngase en contacto con el fabricante del hardware o el servicio de Soporte técnico y Atención al cliente de Microsoft para determinar la causa y la acción correctora. Después de solucionar el error de hardware, restaure todas las bases de datos y ejecute DBCC CHECKDB.  
  
