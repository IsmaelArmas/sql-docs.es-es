---
title: Finalizar la actividad de administración de dominios | Microsoft Docs
ms.custom: ''
ms.date: 06/13/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.technology: data-quality-services
ms.topic: conceptual
ms.assetid: ab6505ad-3090-453b-bb01-58435e7fa7c0
author: leolimsft
ms.author: lle
manager: craigg
ms.openlocfilehash: ec0413f72261bf2890c372773a13a662e9182498
ms.sourcegitcommit: dfb1e6deaa4919a0f4e654af57252cfb09613dd5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/11/2019
ms.locfileid: "56011196"
---
# <a name="end-the-domain-management-activity"></a>Finalizar la actividad Administración de dominios
  En este tema se describe cómo completar, cerrar o cancelar la actividad de administración de dominios en [!INCLUDE[ssDQSnoversion](../includes/ssdqsnoversion-md.md)] (DQS). La administración de dominios no se realiza mediante un asistente, por lo que los controles descritos a continuación se pueden utilizar desde cualquiera de las páginas de la actividad de administración de dominios.  
  
## <a name="end-domain-management"></a>Finalizar la administración de dominios  
 **Finalizar**  
 Haga clic en esta opción para finalizar la administración de dominios. Aparecerá un cuadro con las opciones siguientes:  
  
-   **Sí - publicar la base de conocimiento y salir**: Se publicará la base de conocimiento para que el usuario actual u otros usuarios puedan usar. La base de conocimiento no se bloqueará, su estado se establecerá en "vacía" (en la tabla de bases de conocimiento), y las actividades Administración de dominios y Detección de conocimiento estarán disponibles. Volverá a la pantalla Abrir base de conocimiento.  
  
-   **No - guardar el trabajo en la base de conocimiento y salir**: Se guardará su trabajo, la base de conocimiento permanecerá bloqueada y el estado de la base de conocimiento se establecerá en el trabajo. Las actividades Administración de dominios y Detección de conocimiento estarán disponibles. Volverá a la página de inicio.  
  
-   **Cancelar – permanecer en la pantalla actual**: Se cerrará la ventana emergente y se le devolverá a la pantalla de administración de dominios.  
  
 **Cancelar**  
 Haga clic en esta opción para terminar la actividad Administración de dominios (perdiendo los cambios realizados) y volver a la página de inicio de DQS.  
  
 **Cerrar**  
 Haga clic en esta opción para guardar el trabajo y volver a la página de inicio de DQS. La base de conocimiento se bloqueará, y su estado en la tabla de bases de conocimiento de la pantalla **Abrir base de conocimiento** será **Administración de dominios**. Después de hacer clic en **Cerrar**, para realizar la actividad Detección de conocimiento tendría que volver a la pantalla **Administración de dominios** , hacer clic en **Finalizar**y, por último, hacer clic en **Sí** para publicar la base de conocimiento o en **No** para guardar el trabajo en la base de conocimiento y salir.  Para obtener más información sobre cómo abrir una base de conocimiento bloqueada, vea [Open a Knowledge Base](../../2014/data-quality-services/open-a-knowledge-base.md).  
  
  
