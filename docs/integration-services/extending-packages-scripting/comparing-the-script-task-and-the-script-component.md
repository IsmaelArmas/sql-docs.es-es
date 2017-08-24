---
title: "Comparación de la tarea Script y el componente de Script | Documentos de Microsoft"
ms.custom: 
ms.date: 03/17/2017
ms.prod: sql-server-2016
ms.reviewer: 
ms.suite: 
ms.technology:
- dbe-xml
ms.tgt_pltfrm: 
ms.topic: reference
applies_to:
- SQL Server 2016 Preview
dev_langs:
- VB
helpviewer_keywords:
- Script task [Integration Services], comparing to Script component
- Script component [Integration Services], comparing to Script task
ms.assetid: 4b73753a-4239-491b-b7a6-abc63ba83d2d
caps.latest.revision: 39
author: douglaslMS
ms.author: douglasl
manager: jhubbard
ms.translationtype: MT
ms.sourcegitcommit: 1419847dd47435cef775a2c55c0578ff4406cddc
ms.openlocfilehash: 0413b4b88a1f0326dad1ba261aea647cefd43302
ms.contentlocale: es-es
ms.lasthandoff: 08/03/2017

---
# <a name="comparing-the-script-task-and-the-script-component"></a>Comparar la tarea Script y el componente de script
  La tarea de Script, disponible en la ventana flujo de Control de la [!INCLUDE[ssISnoversion](../../includes/ssisnoversion-md.md)] diseñador y el componente de Script, disponible en la ventana flujo de datos, tienen fines muy diferentes un [!INCLUDE[ssISnoversion](../../includes/ssisnoversion-md.md)] paquete. La tarea es una herramienta de flujo de control de uso general, en tanto que el componente actúa como un origen, transformación o destino en el flujo de datos. A pesar de sus fines diferentes, sin embargo, la tarea Script y el componente de script tienen algunas similitudes en las herramientas de codificación que utilizan y los objetos del paquete que ponen a disposición del desarrollador de software. Comprender sus similitudes y diferencias puede ayudarle a utilizar la tarea y el componente de manera más eficaz.  
  
## <a name="similarities-between-the-script-task-and-the-script-component"></a>Similitudes entre la tarea Script y el componente de script  
 La tarea Script y el componente de script comparten las siguientes características comunes.  
  
|Característica|Description|  
|-------------|-----------------|  
|Dos modos en tiempo de diseño|Tanto en la tarea como en el componente, se comienza especificando las propiedades en el editor y, a continuación, se cambia al entorno de desarrollo para escribir código.|  
|[!INCLUDE[msCoName](../../includes/msconame-md.md)][!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] Tools for Applications (VSTA)|Tanto la tarea como el componente usan el mismo IDE de VSTA y admiten código escrito en [!INCLUDE[msCoName](../../includes/msconame-md.md)] Visual Basic o [!INCLUDE[msCoName](../../includes/msconame-md.md)] Visual C#.|  
|Scripts precompilados|A partir de [!INCLUDE[ssISversion10](../../includes/ssisversion10-md.md)], todos los scripts están precompilados. En versiones anteriores, podía especificar si se precompilaban o no los scripts.<br /><br /> El script se precompila en código binario, lo que permite una ejecución más rápida, pero aumenta el tamaño del paquete.|  
|depuración|La tarea y el componente admiten ambos puntos de interrupción y recorridos paso a paso por el código mientras se depura en el entorno de diseño. Para obtener más información, consulte [codificar y depurar la tarea Script](../../integration-services/extending-packages-scripting/task/coding-and-debugging-the-script-task.md) y [codificar y depurar el componente de Script](../../integration-services/extending-packages-scripting/data-flow-script-component/coding-and-debugging-the-script-component.md).|  
  
## <a name="differences-between-the-script-task-and-the-script-component"></a>Diferencias entre la tarea Script y el componente de script  
 La tarea Script y el componente de script tienen las siguientes diferencias notables.  
  
|Característica|Tarea Script|Componente de script|  
|-------------|-----------------|----------------------|  
|Flujo de control/flujo de datos|La tarea Script se configura en la pestaña Flujo de control del diseñador y se ejecuta fuera del flujo de datos del paquete.|El componente de script se configura en la página Flujo de datos del diseñador y representa un origen, transformación o destino en la tarea Flujo de datos.|  
|Finalidad|Una tarea Script puede realizar prácticamente cualquier tarea de uso general.|Con el componente de script, debe especificar si desea crear un origen, transformación o destino.|  
|Ejecución|Una tarea Script ejecuta código personalizado en algún punto del flujo de trabajo del paquete. Solo se ejecuta una vez, a menos que se incluya en un contenedor de bucles o en un controlador de eventos.|Un componente de Script también se ejecuta una vez, pero normalmente ejecuta su rutina de procesamiento principal una vez para cada fila de datos del flujo de datos.|  
|Editor|El **Editor de la tarea de secuencia de comandos** tiene tres páginas: **General**, **Script**, y **expresiones**. Solo el **ReadOnlyVariables** y **ReadWriteVariables**, y **ScriptLanguage** propiedades afectan directamente al código que se puede escribir.|El **Editor de transformación Script** tiene hasta cuatro páginas: **columnas de entrada**, **entradas y salidas**, **Script**, y **administradores de conexión**. Los metadatos y propiedades que configura en cada una de estas páginas determinan los miembros de las clases base que se generan automáticamente para su uso en el código.|  
|Interacción con el paquete|En el código escrito para una tarea de secuencia de comandos, utilice la **Dts** propiedad para tener acceso a otras características del paquete. El **Dts** propiedad es un miembro de la **ScriptMain** clase.|En el código del componente de script, utiliza propiedades de descriptor de acceso con tipo para tener acceso a ciertas características del paquete como variables y administradores de conexión.<br /><br /> El **PreExecute** método puede tener acceso a solo las variables de solo lectura. El **PostExecute** método puede tener acceso de solo lectura y las variables de lectura/escritura.<br /><br /> Para obtener más información acerca de estos métodos, consulte [codificar y depurar el componente de Script](../../integration-services/extending-packages-scripting/data-flow-script-component/coding-and-debugging-the-script-component.md).|  
|Utilizar variables|La tarea de secuencia de comandos utiliza el <xref:Microsoft.SqlServer.Dts.Tasks.ScriptTask.ScriptObjectModel.Variables%2A> propiedad de la **Dts** objeto para tener acceso a variables que están disponibles a través de la tarea <xref:Microsoft.SqlServer.Dts.Tasks.ScriptTask.ScriptTask.ReadOnlyVariables%2A> y <xref:Microsoft.SqlServer.Dts.Tasks.ScriptTask.ScriptTask.ReadWriteVariables%2A> propiedades. Por ejemplo:<br /><br /> [Visual Basic]<br /><br /> `Dim myVar as String` <br /> `myVar = Dts.Variables(“MyStringVariable”).Value.ToString`<br /><br /> [C#]<br /><br /> `string myVar;` <br /> `myVar = Dts.Variables["MyStringVariable"].Value.ToString();`|El componente de script utiliza propiedades de descriptor de acceso con tipo de la clase base generada automáticamente, creadas a partir de las propiedades <xref:Microsoft.SqlServer.Dts.Pipeline.ScriptComponent.ReadOnlyVariables%2A> y <xref:Microsoft.SqlServer.Dts.Pipeline.ScriptComponent.ReadWriteVariables%2A> del componente. Por ejemplo:<br /><br /> [Visual Basic]<br /><br /> `Dim myVar as String` <br /> `myVar = Me.Variables.MyStringVariable`<br /><br /> [C#]<br /><br /> `string myVar;` <br /> `myVar = this.Variables.MyStringVariable;`|  
|Utilizar conexiones|La tarea de secuencia de comandos utiliza el <xref:Microsoft.SqlServer.Dts.Tasks.ScriptTask.ScriptObjectModel.Connections%2A> propiedad de la **Dts** objeto a los administradores de conexión de acceso definidos en el paquete. Por ejemplo:<br /><br /> [Visual Basic]<br /><br /> `Dim myFlatFileConnection As String` <br /> `myFlatFileConnection = _     DirectCast(Dts.Connections("Test Flat File Connection").AcquireConnection(Dts.Transaction), _     String)`<br /><br /> [C#]<br /><br /> `string myFlatFileConnection;` <br /> `myFlatFileConnection = (Dts.Connections["Test Flat File Connection"].AcquireConnection(Dts.Transaction) as String);`|El componente de script utiliza propiedades de descriptor de acceso con tipo de la clase base generada automáticamente, creadas a partir de la lista de administradores de conexión escrita por el usuario en la página Administradores de conexión del editor. Por ejemplo:<br /><br /> [Visual Basic]<br /><br /> `Dim connMgr As IDTSConnectionManager100` <br /> `connMgr = Me.Connections.MyADONETConnection`<br /><br /> [C#]<br /><br /> `IDTSConnectionManager100 connMgr;` <br /> `connMgr = this.Connections.MyADONETConnection;`|  
|Provocar eventos|La tarea de secuencia de comandos utiliza el <xref:Microsoft.SqlServer.Dts.Tasks.ScriptTask.ScriptObjectModel.Events%2A> propiedad de la **Dts** objeto para provocar eventos. Por ejemplo:<br /><br /> [Visual Basic]<br /><br /> `Dts.Events.FireError(0, "Event Snippet", _     ex.Message & ControlChars.CrLf & ex.StackTrace, _     "", 0)`<br /><br /> [C#]<br /><br /> `Dts.Events.FireError(0, "Event Snippet", ex.Message + "\r" + ex.StackTrace, "", 0);`|El componente de script provoca errores, advertencias y mensajes informativos utilizando los métodos de la interfaz <xref:Microsoft.SqlServer.Dts.Pipeline.Wrapper.IDTSComponentMetaData100> que devuelve la propiedad <xref:Microsoft.SqlServer.Dts.Pipeline.ScriptComponent.ComponentMetaData%2A>. Por ejemplo:<br /><br /> [Visual Basic]<br /><br /> `Dim myMetadata as IDTSComponentMetaData100 myMetaData = Me.ComponentMetaData myMetaData.FireError(...)`|  
|Registro|La tarea de secuencia de comandos utiliza el <xref:Microsoft.SqlServer.Dts.Tasks.ScriptTask.ScriptObjectModel.Log%2A> método de la **Dts** objeto para registrar información en proveedores de registro habilitados. Por ejemplo:<br /><br /> [Visual Basic]<br /><br /> `Dim bt(0) As Byte Dts.Log("Test Log Event", _     0, _     bt)`<br /><br /> [C#]<br /><br /> `byte[] bt = new byte[0];` <br /> `Dts.Log("Test Log Event", 0, bt);`|El componente de script utiliza el método <xref:Microsoft.SqlServer.Dts.Pipeline.ScriptComponent.Log%2A> de la clase base generada automáticamente para registrar información en los proveedores de registro habilitados. Por ejemplo:<br /><br /> [Visual Basic]<br /><br /> `Dim bt(0) As Byte`<br /><br /> `Me.Log("Test Log Event", _`<br /><br /> `0, _`<br /><br /> `bt)`<br /><br /> [C#]<br /><br /> `byte[] bt = new byte[0]; this.Log("Test Log Event", 0, bt);`|  
|Devolver resultados|La tarea de secuencia de comandos utiliza el <xref:Microsoft.SqlServer.Dts.Tasks.ScriptTask.ScriptObjectModel.TaskResult%2A> propiedad y opcional <xref:Microsoft.SqlServer.Dts.Tasks.ScriptTask.ScriptObjectModel.ExecutionValue%2A> propiedad de la **Dts** objeto que se va a notificar el tiempo de ejecución de sus resultados.|El componente de script se ejecuta como parte de la tarea Flujo de datos y no notifica resultados mediante estas propiedades.|  
  
## <a name="see-also"></a>Vea también  
 [Extender el paquete con la tarea de secuencia de comandos](../../integration-services/extending-packages-scripting/task/extending-the-package-with-the-script-task.md)   
 [Extender el flujo de datos con el componente de Script](../../integration-services/extending-packages-scripting/data-flow-script-component/extending-the-data-flow-with-the-script-component.md)   
  
  