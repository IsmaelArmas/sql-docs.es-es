---
title: Revisar asignación de tipos de datos (Asistente para importación y exportación de SQL Server) | Microsoft Docs
ms.custom: ''
ms.date: 06/14/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.suite: ''
ms.technology:
- integration-services
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- sql12.dts.impexpwizard.reviewissues.f1
ms.assetid: 0625c4f9-b8ff-4593-b884-39398b9d43af
caps.latest.revision: 18
author: douglaslMS
ms.author: douglasl
manager: jhubbard
ms.openlocfilehash: 3f49bc9a31fcf2cf348f7616a337b51a9b7e5229
ms.sourcegitcommit: 5dd5cad0c1bbd308471d6c885f516948ad67dfcf
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2018
ms.locfileid: "36103604"
---
# <a name="review-data-type-mapping-sql-server-import-and-export-wizard"></a>Revisar asignación de tipos de datos (Asistente para importación y exportación de SQL Server)
  Use la **revisar Data Type Mapping** página para revisar información detallada sobre las conversiones de tipos de datos que el asistente tiene que llevar a cabo para que sea compatible con el destino de los datos de origen. Esta información incluye indicaciones visuales para distinguir las conversiones que se espera que sean correctas de las que podrían producir errores o truncamientos. En cada conversión puede decidir si aceptar la conversión que el asistente sugiere, y especificar cómo administrar los errores que se produzcan.  
  
 Para más información acerca de este asistente, consulte [SQL Server Import and Export Wizard](import-and-export-data-with-the-sql-server-import-and-export-wizard.md). Para obtener información acerca de las opciones para iniciar el asistente y sobre los permisos necesarios para ejecutar el asistente correctamente, consulte [ejecutar la importación de SQL Server y el Asistente para exportación de](start-the-sql-server-import-and-export-wizard.md).  
  
 El propósito de la [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] Import and Export Wizard consiste en copiar datos desde un origen a un destino. El asistente también puede crear una base de datos y tablas de destino. Sin embargo, si tiene que copiar diversas bases de datos o tablas, u otros tipos de objetos de bases de datos, debe utilizar el Asistente para copiar bases de datos. Para más información, consulte [Use the Copy Database Wizard](../../relational-databases/databases/use-the-copy-database-wizard.md).  
  
## <a name="options"></a>Opciones  
 La página **Revisar asignación de tipos de datos** consta de una lista **Tabla** , una lista **Asignación de tipo de datos** y opciones de control de errores.  
  
### <a name="table-list"></a>Lista de la tabla  
 La parte superior de la **revisar problemas de tipos de datos** página es una **tabla** lista que muestra las tablas para ser transferidos desde el origen al destino. En la tabla siguiente se describen las columnas de esta lista.  
  
|columna|Descripción|  
|------------|-----------------|  
|Icono de origen|Indica la probabilidad de que las conversiones de tipos de datos sean correctas:<br /><br /> Un icono de marca de verificación verde indica que el asistente espera que todas las conversiones de tipos de datos para esta tabla sean correctas.<br /><br /> Un icono de signo de admiración amarillo indica que debería revisar las conversiones individuales que el asistente realizará. Para revisar estas conversiones, seleccione la tabla y, a continuación, revise las conversiones para las columnas individuales en la lista **Asignación de tipo de datos** .<br /><br /> Un icono de error rojo indica que el asistente no puede realizar algunas de las conversiones para esta tabla de forma confiable.|  
|**Source**|Muestra el nombre de la tabla de origen.|  
|Icono de destino|Indica si el destino ya existe o lo crea el asistente:<br /><br /> Un icono de tabla indica que el destino es una tabla existente.<br /><br /> Un icono de tabla con un rayo de sol indica que el destino es una tabla nueva que el asistente va a crear.|  
|**Destino**|Muestra el nombre de la tabla de destino.|  
  
 Para ver información de conversión sobre una tabla individual, seleccione una tabla de esta **tabla** cuadrícula. La información de conversión para la tabla seleccionada aparece en las columnas en la cuadrícula **Asignación de tipo de datos** en la parte inferior de la página.  
  
### <a name="data-type-mapping-list"></a>Lista Asignación de tipo de datos  
 La parte inferior de la **revisar problemas de tipos de datos** página es la **asignar tipos de datos** lista. Esta cuadrícula proporciona información de conversión detallada sobre las columnas de la tabla que está seleccionada en la lista **Tabla** . En la tabla siguiente se describen las columnas de esta lista.  
  
|columna|Descripción|  
|------------|-----------------|  
|Icono de conversión|Indica la probabilidad de que las conversiones de tipos de datos sean correctas:<br /><br /> Un icono de marca de verificación verde indica que el asistente espera que la conversión de los tipos de datos de esta columna sea correcta.<br /><br /> Un icono de signo de admiración amarillo indica que debería revisar la conversión que el asistente va a realizar. Para revisar la conversión, haga doble clic en la columna para ver el cuadro de diálogo **Detalles de conversión de columna** .<br /><br /> Un icono de error rojo indica que el asistente no puede realizar la conversión de forma confiable.|  
|**Columna de origen**|Muestra el nombre de la columna de origen.|  
|**Tipo de origen**|Muestra el tipo de datos de la columna de origen.|  
|**Columna de destino**|Muestra el nombre de la columna de destino.|  
|**Tipo de destino**|Muestra el tipo de datos de la columna de destino.|  
|**Convertir**|Especifique si la conversión planeada debería continuar:<br /><br /> Active la casilla para hacer que el asistente continúe con la conversión planeada.<br /><br /> Desactive la casilla para cancelar la conversión de los tipos de datos.|  
|**Al producirse un error**|Especifique cómo controla el asistente los errores:<br /><br /> Use la **On Error (global)** configuración.<br /><br /> Termine con un error y detenga el proceso de importación o exportación.<br /><br /> Omita el error.|  
|**Al producirse truncamiento**|Especifique cómo controla el asistente el truncamiento:<br /><br /> Use la **al producirse truncamiento (global)** configuración.<br /><br /> Producirá un error y detener la importación o exportación proceso<br /><br /> Omita el truncamiento.|  
  
 Para ver información detallada sobre la conversión de una columna de datos en particular, haga doble clic en cualquier fila de la lista. El cuadro de diálogo **Detalles de conversión de columna** se abre y muestra información de conversión más detallada para la columna.  
  
### <a name="error-handling-options"></a>Opciones de control de errores  
 **Al producirse un error (global)**  
 Especifique cómo controla el asistente los errores:  
  
-   Termine con un error y detenga el proceso de importación o exportación.  
  
-   Omita el error y continúe el proceso de importación o exportación.  
  
 Este valor se aplica a todas las conversiones que tienen seleccionado **Usar global** en la columna **Al producirse un error** de la lista **Asignación de tipo de datos** .  
  
 **Al producirse truncamiento (global)**  
 Especifique cómo controla el asistente el truncamiento:  
  
-   Termine con un error y detenga el proceso de importación o exportación.  
  
-   Omita el trocamiento y continúe el proceso de importación o exportación.  
  
 Este valor se aplica a todas las conversiones que tienen seleccionado **Usar global** en la columna **Al producirse truncamiento** de la lista **Asignación de tipo de datos** .  
  
  