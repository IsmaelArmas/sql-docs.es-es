---
title: 'Tutorial: De archivos de datos SQL Server en el servicio de almacenamiento de Windows Azure | Documentos de Microsoft'
ms.custom: ''
ms.date: 06/13/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.suite: ''
ms.technology:
- database-engine
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: e69be67d-da1c-41ae-8c9a-6b12c8c2fb61
caps.latest.revision: 7
author: JennieHubbard
ms.author: jhubbard
manager: jhubbard
ms.openlocfilehash: cd793aad219d8e65a787dd3d872046df00cca414
ms.sourcegitcommit: 5dd5cad0c1bbd308471d6c885f516948ad67dfcf
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2018
ms.locfileid: "36202679"
---
# <a name="tutorial-sql-server-data-files-in-windows-azure-storage-service"></a>Tutorial: Archivos de datos de SQL Server en el servicio Azure Storage
  Este es el tutorial de Archivos de datos de SQL Server en el servicio Azure Storage. Este tutorial le ayudará a saber cómo almacenar archivos de datos de SQL Server en el servicio de almacenamiento Blob de Windows Azure directamente.  
  
 La compatibilidad con la integración de SQL Server para el servicio de almacenamiento Blob de Windows Azure es una mejora de SQL Server 2014. Para información general sobre la funcionalidad y las ventajas de usar esta funcionalidad, consulte [archivos de datos de SQL Server en Windows Azure](databases/sql-server-data-files-in-microsoft-azure.md).  
  
## <a name="what-you-will-learn"></a>Aprendizaje  
 Este tutorial contiene varias lecciones en las que se muestra cómo almacenar archivos de datos de SQL Server en el servicio Azure Storage. Cada una de las lecciones se centra en una tarea determinada. Primero, aprenderá a crear una cuenta de almacenamiento y un contenedor en Windows Azure. A continuación, aprenderá a crear una credencial de SQL Server para poder integrar SQL Server con Azure Storage. Después, creará una nueva base de datos en Azure Storage directamente. Por otra parte, el tutorial presentará escenarios de cifrado, migración y de copia de seguridad y restauración.  
  
 El tutorial se divide en nueve lecciones:  
  
 **[Lección 1: Crear el contenedor y la cuenta de almacenamiento de Azure de Windows](../tutorials/lesson-1-create-windows-azure-storage-account-and-container.md)**  
 En esta lección, creará una cuenta de Azure Storage y un contenedor.  
  
 **[Lección 2. Crear una directiva en el contenedor y generar una firma de acceso compartido &#40;SAS&#41; clave](lesson-1-create-stored-access-policy-and-shared-access-signature.md)**  
 En esta lección, creará una directiva en el contenedor de blobs y también generará una firma de acceso compartido.  
  
 **[Lección 3: Crear una credencial de SQL Server](lesson-2-create-a-sql-server-credential-using-a-shared-access-signature.md)**  
 En esta lección, creará una credencial para almacenar la información de seguridad usada para tener acceso a la cuenta de almacenamiento de Windows Azure.  
  
 **[Lección 4: Crear una base de datos en almacenamiento de Windows Azure](../relational-databases/lesson-3-database-backup-to-url.md)**  
 En esta lección, creará una base de datos de Azure Storage con la opción FILENAME de la instrucción CREATE DATABASE.  
  
 **[Lección 5. &#40;Opcional&#41; cifrar la base de datos mediante TDE](../relational-databases/lesson-4-restore-database-to-virtual-machine-from-url.md)**  
 En esta lección, cifrará la base de datos mediante un cifrado de datos transparente (TDE) y un certificado de servidor.  
  
 **[Lección 6: Migrar una base de datos de un origen de la máquina local a una máquina de destino en Windows Azure](lesson-5-backup-database-using-file-snapshot-backup.md)**  
 En esta lección, migrará una base de datos desde el entorno local a una máquina virtual de Windows Azure mediante la opción CREATE DATABASE FOR ATTACH.  
  
 **[Lección 7: Mover los archivos de datos al almacenamiento de Windows Azure](../relational-databases/lesson-6-generate-activity-and-backup-log-using-file-snapshot-backup.md)**  
 En esta lección, moverá los archivos de datos a Azure Storage mediante la instrucción ALTER DATABASE.  
  
 **[Lección 8: Restaurar una base de datos en almacenamiento de Windows Azure](../relational-databases/lesson-7-restore-a-database-to-a-point-in-time.md)**  
 En esta lección, restaurará una base de datos en Azure Storage con la opción MOVE de la instrucción RESTORE DATABASE.  
  
 **[Lección 9. Restaurar una base de datos de almacenamiento de Windows Azure](lesson-8-restore-as-new-database-from-log-backup.md)**  
 En esta lección, restaurará una base de datos desde Azure Storage con la opción MOVE de la instrucción RESTORE DATABASE.  
  
## <a name="see-also"></a>Vea también  
 [Archivos de datos SQL Server en Windows Azure](databases/sql-server-data-files-in-microsoft-azure.md)  
  
  