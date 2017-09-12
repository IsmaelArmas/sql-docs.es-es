---
title: DENEGAR permisos de texto completo (Transact-SQL) | Documentos de Microsoft
ms.custom: 
ms.date: 05/15/2017
ms.prod: sql-non-specified
ms.reviewer: 
ms.suite: 
ms.technology:
- database-engine
ms.tgt_pltfrm: 
ms.topic: language-reference
dev_langs:
- TSQL
helpviewer_keywords:
- full-text search [SQL Server], permissions
- denying permissions [SQL Server], fulll-text
- full-text catalogs [SQL Server], permissions
- full-text stoplist [SQL Server], permissions
- DENY statement, full-text permissions
ms.assetid: d86e9a1d-0938-4ec2-a169-2d0564f3642e
caps.latest.revision: 26
author: douglaslMS
ms.author: douglasl
manager: jhubbard
ms.translationtype: MT
ms.sourcegitcommit: 876522142756bca05416a1afff3cf10467f4c7f1
ms.openlocfilehash: 010507ec0b9fdcec89c6f8ee687b1c26b4c4436e
ms.contentlocale: es-es
ms.lasthandoff: 09/01/2017

---
# <a name="deny-full-text-permissions-transact-sql"></a>DENY (permisos de texto completo de Transact-SQL)
[!INCLUDE[tsql-appliesto-ss2008-asdb-xxxx-xxx_md](../../includes/tsql-appliesto-ss2008-asdb-xxxx-xxx-md.md)]

  Deniega permisos en un catálogo de texto completo y en listas de palabras irrelevantes de texto completo.  
  

 ![Icono de vínculo de tema](../../database-engine/configure-windows/media/topic-link.gif "Icono de vínculo de tema") [Convenciones de sintaxis de Transact-SQL](../../t-sql/language-elements/transact-sql-syntax-conventions-transact-sql.md)  
  
## <a name="syntax"></a>Sintaxis  
  
```  
DENY permission [ ,...n ] ON  
    FULLTEXT   
        {  
           CATALOG :: full-text_catalog_name  
           |  
           STOPLIST :: full-text_stoplist_name  
        }  
    TO database_principal [ ,...n ] [ CASCADE ]  
        [ AS denying_principal ]  
```  
  
## <a name="arguments"></a>Argumentos  
 *permiso*  
 Es el nombre de un permiso. Las asignaciones válidas de permisos a elementos protegibles se describen en la sección "Comentarios", más adelante en este tema.  
  
 EN el catálogo de texto completo **::***text_catalog_name completo*  
 Especifica el catálogo de texto completo en el que se deniega el permiso. El calificador de ámbito **::** es necesario.  
  
 EN FULLTEXT STOPLIST **::***text_stoplist_name completo*  
 Especifica la lista de palabras irrelevantes de texto completo en la que se deniega el permiso. El calificador de ámbito **::** es necesario.  
  
 *database_principal*  
 Especifica la entidad de seguridad a la que se deniega el permiso. Uno de los siguientes:  
  
-   usuario de base de datos  
  
-   rol de base de datos  
  
-   rol de aplicación  
  
-   usuario de base de datos asignado a un inicio de sesión de Windows  
  
-   usuario de base de datos asignado a un grupo de Windows  
  
-   usuario de base de datos asignado a un certificado  
  
-   usuario de base de datos asignado a una clave asimétrica  
  
-   usuario de base de datos no asignado a una entidad de seguridad del servidor  
  
 CASCADE  
 Indica que el permiso que se va a denegar también se denegará a otras entidades de seguridad a las que esta entidad de seguridad ha concedido permisos.  
  
 *denying_principal*  
 Especifica una entidad de seguridad de la que la entidad de seguridad que ejecuta esta consulta deriva su derecho de denegar el permiso. Uno de los siguientes:  
  
-   usuario de base de datos  
  
-   rol de base de datos  
  
-   rol de aplicación  
  
-   usuario de base de datos asignado a un inicio de sesión de Windows  
  
-   usuario de base de datos asignado a un grupo de Windows  
  
-   usuario de base de datos asignado a un certificado  
  
-   usuario de base de datos asignado a una clave asimétrica  
  
-   usuario de base de datos no asignado a una entidad de seguridad del servidor  
  
  
## <a name="fulltext-catalog-permissions"></a>Permisos FULLTEXT CATALOG  
 Un catálogo de texto completo es un elemento protegible en el nivel de base de datos que contiene la base de datos que es su entidad primaria en la jerarquía de permisos. Los permisos más limitados y específicos que se pueden denegar en un catálogo de texto completo se muestran en la siguiente tabla, junto con permisos más generales que los incluyen por implicación.  
  
|Permiso de catálogo de texto completo|Implícito en el permiso de catálogo de texto completo|Implícito en el permiso de base de datos|  
|-----------------------------------|----------------------------------------------|------------------------------------|  
|CONTROL|CONTROL|CONTROL|  
|TAKE OWNERSHIP|CONTROL|CONTROL|  
|ALTER|CONTROL|ALTER ANY FULLTEXT CATALOG|  
|REFERENCES|CONTROL|REFERENCES|  
|VIEW DEFINITION|CONTROL|VIEW DEFINITION|  
  
## <a name="fulltext-stoplist-permissions"></a>Permisos FULLTEXT STOPLIST  
 Una lista de palabras irrelevantes de texto completo es un elemento protegible en el nivel de base de datos que contiene la base de datos que es su entidad primaria en la jerarquía de permisos. Los permisos más limitados y específicos que se pueden denegar en una lista de palabras irrelevantes de texto completo se muestran en la siguiente tabla, junto con permisos más generales que los incluyen por implicación.  
  
|Permiso de lista de palabras irrelevantes de texto completo|Implícito en el permiso de lista de palabras irrelevantes de texto completo|Implícito en el permiso de base de datos|  
|------------------------------------|-----------------------------------------------|------------------------------------|  
|ALTER|CONTROL|ALTER ANY FULLTEXT CATALOG|  
|CONTROL|CONTROL|CONTROL|  
|REFERENCES|CONTROL|REFERENCES|  
|TAKE OWNERSHIP|CONTROL|CONTROL|  
|VIEW DEFINITION|CONTROL|VIEW DEFINITION|  
  
## <a name="permissions"></a>Permissions  
 Requiere el permiso CONTROL en el catálogo de texto completo. Si utiliza la opción AS, la entidad de seguridad especificada debe poseer el catálogo de texto completo.  
  
## <a name="see-also"></a>Vea también  
 [Crear rol de aplicación &#40; Transact-SQL &#41;](../../t-sql/statements/create-application-role-transact-sql.md)   
 [CREATE ASYMMETRIC KEY &#40;Transact-SQL&#41;](../../t-sql/statements/create-asymmetric-key-transact-sql.md)   
 [CREATE CERTIFICATE &#40;Transact-SQL&#41;](../../t-sql/statements/create-certificate-transact-sql.md)   
 [Crear catálogo de texto completo &#40; Transact-SQL &#41;](../../t-sql/statements/create-fulltext-catalog-transact-sql.md)   
 [Crear lista de palabras IRRELEVANTES de texto completo &#40; Transact-SQL &#41;](../../t-sql/statements/create-fulltext-stoplist-transact-sql.md)   
 [DENY &#40;Transact-SQL&#41;](../../t-sql/statements/deny-transact-sql.md)   
 [Jerarquía de cifrado](../../relational-databases/security/encryption/encryption-hierarchy.md)   
 [Sys.fn_my_permissions &#40; Transact-SQL &#41;](../../relational-databases/system-functions/sys-fn-my-permissions-transact-sql.md)   
 [Permisos de texto completo de GRANT &#40; Transact-SQL &#41;](../../t-sql/statements/grant-full-text-permissions-transact-sql.md)   
 [HAS_PERMS_BY_NAME &#40;Transact-SQL&#41;](../../t-sql/functions/has-perms-by-name-transact-sql.md)   
 [Permisos &#40;motor de base de datos&#41;](../../relational-databases/security/permissions-database-engine.md)   
 [Entidades de seguridad &#40;motor de base de datos&#41;](../../relational-databases/security/authentication-access/principals-database-engine.md)   
 [sys.fn_builtin_permissions &#40;Transact-SQL&#41;](../../relational-databases/system-functions/sys-fn-builtin-permissions-transact-sql.md)   
 [Sys.fulltext_catalogs &#40; Transact-SQL &#41;](../../relational-databases/system-catalog-views/sys-fulltext-catalogs-transact-sql.md)   
 [sys.fulltext_stoplists &#40;Transact-SQL&#41;](../../relational-databases/system-catalog-views/sys-fulltext-stoplists-transact-sql.md)  
  
  
