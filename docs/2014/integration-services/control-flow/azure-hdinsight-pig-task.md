---
title: Tarea de Pig de Azure HDInsight | Microsoft Docs
ms.custom: ''
ms.date: 02/28/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.technology: integration-services
ms.topic: conceptual
f1_keywords:
- sql12.dts.designer.afppigtask.f1
- sql11.dts.designer.afppigtask.f1
ms.assetid: 26f34f64-f344-486e-9190-acf71aef29a8
author: douglaslMS
ms.author: douglasl
manager: craigg
ms.openlocfilehash: 30340a873846e20911a7f14694f9602c17d960e8
ms.sourcegitcommit: ceb7e1b9e29e02bb0c6ca400a36e0fa9cf010fca
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/03/2018
ms.locfileid: "52749417"
---
# <a name="azure-hdinsight-pig-task"></a>Tarea de Pig de Azure HDInsight
Utilice la **tarea de Pig de Azure HDInsight** para ejecutar el script de Pig en un clúster de Azure HDInsight.
     
Para agregar una **tarea de Pig de Azure HDInsight**, arrástrela al Diseñador de SSIS y haga doble clic o haga clic con el botón derecho y haga clic en **Editar** para ver el siguiente cuadro de diálogo: **Azure HDInsight Pig Task Editor** (Editor de tareas de Pig de Azure HDInsight).  
  
 La lista siguiente describe los campos de este cuadro de diálogo.  
  
1.  Para el campo **HDInsightConnection**, seleccione un Administrador de conexiones de Azure HDInsight existente o cree uno nuevo que haga referencia al clúster de Azure que se usó para ejecutar el script.
  
2.  Para el campo **AzureStorageConnection**, seleccione un Administrador de conexiones de Azure Storage existente o cree uno nuevo que haga referencia a una cuenta de Azure Storage asociada con el clúster. Esto solo es necesario si quiere descargar los registros de error y la salida de ejecución del script.
 
3.  Para el campo **BlobContainer**, especifique el nombre del contenedor de almacenamiento asociado con el clúster. Esto solo es necesario si quiere descargar los registros de error y la salida de ejecución del script.
  
4.  Para el campo **LocalLogFolder**, especifique la carpeta en la que se descargarán los registros de error y la salida de ejecución de script. Esto solo es necesario si quiere descargar los registros de error y la salida de ejecución de script.   
  
5.  Hay dos maneras de especificar el script de Pig que se va a ejecutar:
  
    1.  **Secuencia de comandos en línea**: Especifique el **Script** campo escribiendo el script para ejecutarlo en línea el **escriba el Script** cuadro de diálogo.
  
    2.  **Archivo de script**: Cargue el archivo de script en Azure Blob Storage y especifique el **BlobName** campo. Si el blob no está en el contenedor ni en la cuenta de almacenamiento predeterminados asociados con el clúster de HDInsight, deben especificarse los campos **ExternalStorageAccountName** y **ExternalBlobContainer**. Para un blob externo, asegúrese de que está configurado como accesible públicamente.  
  
     Si se especifican ambos, se usará el archivo de script y se omitirá el script en línea.
