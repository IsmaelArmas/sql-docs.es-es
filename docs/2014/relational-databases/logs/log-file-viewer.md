---
title: Visor de archivos de registro | Microsoft Docs
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
- Log File Viewer
ms.assetid: a4ea7fc8-1cb2-4c98-bc86-8991c5e748b2
caps.latest.revision: 25
author: craigg-msft
ms.author: craigg
manager: jhubbard
ms.openlocfilehash: 3ff54718ce6ccc39030292041653ebe734594824
ms.sourcegitcommit: 5dd5cad0c1bbd308471d6c885f516948ad67dfcf
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2018
ms.locfileid: "36199359"
---
# <a name="log-file-viewer"></a>Visor de archivos de registro
  El Visor del archivo de registros de [!INCLUDE[ssManStudioFull](../../includes/ssmanstudiofull-md.md)] se usa para obtener acceso a la información sobre los errores y eventos capturados en los archivos de registro.  
  
## <a name="benefits-of-using-log-file-viewer"></a>Ventajas de usar el visor del archivo de registro  
 Puede ver los archivos de registro de [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] desde una instancia local o remota de [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] cuando la instancia de destino está sin conexión o no se puede iniciar. Puede tener acceso a los archivos de registro sin conexión de servidores registrados o mediante programación a través de consultas WMI y WQL (Lenguaje de la consulta de WMI). Para obtener más información, vea [Ver sin conexión archivos de registro](view-offline-log-files.md). Estos son los tipos de archivos de registro a que se puede tener acceso con el visor del archivo de registro:  
  
-   Recopilación de auditoría  
  
-   Recopilación de datos  
  
-   Correo electrónico de base de datos  
  
-   Historial de trabajos  
  
-   Planes de mantenimiento  
  
-   Planes de mantenimiento remoto  
  
-   SQL Server  
  
-   Agente SQL Server  
  
-   Windows NT (se puede tener acceso a estos eventos de Windows también desde el Visor de eventos).  
  
## <a name="log-file-viewer-tasks"></a>Tareas del visor del archivo de registros  
  
|Descripción de la tarea|Tema|  
|----------------------|-----------|  
|Describe cómo abrir el visor del archivo de registros dependiendo de la información que se desee ver.|[Abrir el Visor de archivos de registro](open-log-file-viewer.md)|  
|Describe cómo ver los archivos de registro sin conexión a través de servidores registrados y cómo comprobar los permisos de WMI.|[Ver sin conexión archivos de registro](view-offline-log-files.md)|  
|Proporciona la Ayuda F1 del visor del archivo de registro.|[Ayuda F1 del Visor de archivos de registro](log-file-viewer-f1-help.md)|  
  
## <a name="see-also"></a>Vea también  
 [SQL Server Audit &#40;motor de base de datos&#41;](../security/auditing/sql-server-audit-database-engine.md)   
 [Registro de errores del Agente SQL Server](../../ssms/agent/sql-server-agent-error-log.md)  
  
  