---
title: 'Propiedades de alerta: Nueva alerta (página General) | Microsoft Docs'
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: sql-tools
ms.reviewer: ''
ms.technology: ssms
ms.topic: conceptual
f1_keywords:
- sql13.ag.alert.general.f1
ms.assetid: f5c11610-62e3-44df-9800-a5dc35be4a09
author: stevestein
ms.author: sstein
manager: craigg
monikerRange: = azuresqldb-mi-current || >= sql-server-2016 || = sqlallproducts-allversions
ms.openlocfilehash: 6d6c4db00e382724ebf0f3f781a8cd0e907bc2e7
ms.sourcegitcommit: 61381ef939415fe019285def9450d7583df1fed0
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2018
ms.locfileid: "47630293"
---
# <a name="alert-properties---new-alert-general-page"></a>Propiedades de alerta - Nueva alerta (página General)
[!INCLUDE[appliesto-ss-asdbmi-xxxx-xxx-md](../../includes/appliesto-ss-asdbmi-xxxx-xxx-md.md)]


> [!IMPORTANT]  
> En [Instancia administrada de Azure SQL Database](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance), la mayoría de las características de agente SQL Server son compatibles actualmente, aunque no todas. Vea [Diferencias de T-SQL en Instancia administrada de Azure SQL Database](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-transact-sql-information#sql-server-agent) para obtener más información.

Utilice esta página para ver y modificar las propiedades generales de las alertas del Agente [!INCLUDE[msCoName](../../includes/msconame_md.md)] [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] .  

## <a name="options"></a>Opciones  
**Nombre**  
Cambie el nombre de la alerta.  
  
**Habilitar**  
Habilita la alerta. Si la alerta no está habilitada, no se producirán acciones especificadas en la alerta.  
  
**Tipo**  
Seleccione el tipo de alerta:  
  
-   **Alerta de evento de SQL Server** responde a los mensajes del registro de eventos de [!INCLUDE[msCoName](../../includes/msconame_md.md)] Windows.  
  
-   **Alerta de condición de rendimiento de SQL Server** responde a una condición específica del contador de rendimiento.  
  
-   **Alerta de evento WMI** responde a un evento Instrumental de administración de Windows (WMI).  
  
## <a name="sql-server-event-alert-options"></a>Opciones de Alerta de evento de SQL Server  
**Nombre de la base de datos**  
Especifica una base de datos para el evento o **todas las bases de datos** para responder a un mensaje independientemente de la base de datos en la que se produzca el evento.  
  
**Número de error**  
Especifica que este evento responde a un error e indica el número de error.  
  
**Severity**  
Especifica que este evento responde a mensajes con un nivel de gravedad específico e indica dicho nivel.  
  
**Mostrar alerta cuando el mensaje contenga**  
Filtra los eventos mediante una cadena específica. Cuando esta opción está seleccionada, la alerta solo responde a los eventos que contengan una cadena específica.  
  
**Texto del mensaje**  
Especifica la cadena que se va a utilizar para filtrar eventos.  
  
## <a name="sql-server-performance-condition-alerts"></a>Alertas de condición de rendimiento de SQL Server  
**Objeto**  
Especifica el objeto de rendimiento que se supervisará.  
  
**Contador**  
Especifica el contador del objeto de rendimiento que se supervisará.  
  
**Instancia**  
Especifica la instancia del contador que se supervisará.  
  
**Alertar si contador**  
Especifica el comportamiento del contador al que la alerta responde. Por ejemplo, si desea que la alerta responda a una condición en la que el valor del contador **Espacio disponible en tempdb (KB)** esté por debajo de un determinado valor, o bien que la alerta responda a una condición en la que las **Compilaciones SQL/seg.** estén por encima de un determinado valor.  
  
**Value**  
Especifica un valor para el contador.  
  
## <a name="wmi-event-alert-options"></a>Opciones de Alerta de evento WMI  
**Espacio de nombres**  
Especifica el espacio de nombres que se utilizará para la instrucción WQL (Lenguaje de consulta WMI). Solo se admite el espacio de nombres del equipo que ejecuta el Agente [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] .  
  
**Consulta**  
Especifica la instrucción WQL que identifica el evento al que responde la alerta.  
  
## <a name="see-also"></a>Ver también  
[Alertas](../../ssms/agent/alerts.md)  
[Usar WQL con el proveedor WMI para eventos de servidor](../../relational-databases/wmi-provider-server-events/using-wql-with-the-wmi-provider-for-server-events.md)  
[Crear una alerta con un número de error](../../ssms/agent/create-an-alert-using-an-error-number.md)  
[Create an Alert Using Severity Level](../../ssms/agent/create-an-alert-using-severity-level.md)  
  
