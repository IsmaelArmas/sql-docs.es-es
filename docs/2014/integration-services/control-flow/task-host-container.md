---
title: Contenedor del host de la tarea | Microsoft Docs
ms.custom: ''
ms.date: 03/06/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.technology: integration-services
ms.topic: conceptual
f1_keywords:
- sql12.dts.designer.taskhostcontainer.f1
helpviewer_keywords:
- containers [Integration Services], Task Host
- Task Host container
ms.assetid: 7394a2c2-1b07-427d-b94a-9792e7783d35
author: douglaslMS
ms.author: douglasl
manager: craigg
ms.openlocfilehash: 010b6d8c59e99c4715d349881922bb5b01153e2b
ms.sourcegitcommit: ceb7e1b9e29e02bb0c6ca400a36e0fa9cf010fca
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/03/2018
ms.locfileid: "52790937"
---
# <a name="task-host-container"></a>contenedor de tarea
  El contenedor del host de la tarea encapsula una tarea individual. En el Diseñador [!INCLUDE[ssIS](../../includes/ssis-md.md)] , el host de la tarea no se configura por separado, sino al establecer las propiedades de la tarea que encapsula. Para obtener más información sobre las tareas encapsuladas por los contenedores del host de la tarea, vea [Integration Services Tasks](integration-services-tasks.md).  
  
 Este contenedor extiende el uso las de variables y los controladores de eventos al nivel de tarea. Para obtener más información, vea [Controladores de eventos de Integration Services &#40;SSIS&#41;](../integration-services-ssis-event-handlers.md) y [Variables de Integration Services &#40;SSIS&#41;](../integration-services-ssis-variables.md).  
  
## <a name="configuration-of-the-task-host"></a>Configuración del host de la tarea  
 Puede establecer propiedades en la ventana **Propiedades** de [!INCLUDE[ssBIDevStudioFull](../../includes/ssbidevstudiofull-md.md)] o mediante programación.  
  
 Para obtener información sobre cómo establecer estas propiedades en [!INCLUDE[ssBIDevStudioFull](../../includes/ssbidevstudiofull-md.md)], vea [Establecer las propiedades de tareas o contenedores](../set-the-properties-of-a-task-or-container.md).  
  
 Para obtener información sobre cómo establecer mediante programación estas propiedades, vea <xref:Microsoft.SqlServer.Dts.Runtime.TaskHost>.  
  
## <a name="related-tasks"></a>Related Tasks  
  
-   [Establecer las propiedades de tareas o contenedores](../set-the-properties-of-a-task-or-container.md)  
  
## <a name="see-also"></a>Vea también  
 [Contenedores de Integration Services](integration-services-containers.md)  
  
  
