---
title: Módulos y prólogos (XQuery) | Microsoft Docs
ms.custom: ''
ms.date: 03/06/2017
ms.prod: sql
ms.prod_service: sql
ms.reviewer: ''
ms.technology: xml
ms.topic: language-reference
dev_langs:
- XML
helpviewer_keywords:
- XQuery, prolog
- prolog
ms.assetid: 0f17b4a4-6234-41d4-a996-6db4e27bff7e
author: rothja
ms.author: jroth
manager: craigg
ms.openlocfilehash: cc8c582f4a4e984bd203071f5ce59f986765e840
ms.sourcegitcommit: 0f7cf9b7ab23df15624d27c129ab3a539e8b6457
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/09/2018
ms.locfileid: "51291521"
---
# <a name="modules-and-prologs-xquery"></a>Módulos y prólogos (XQuery)
[!INCLUDE[tsql-appliesto-ss2012-xxxx-xxxx-xxx-md](../includes/tsql-appliesto-ss2012-xxxx-xxxx-xxx-md.md)]

  [Prólogo de XQuery](../xquery/modules-and-prologs-xquery-prolog.md) es una serie de declaraciones de espacio de nombres. Al utilizar la declaración de espacio de nombres en el prólogo, se puede especificar un enlace entre el prefijo y el espacio de nombres y utilizar el prefijo en el cuerpo de la consulta.  
  
## <a name="implementation-limitations"></a>Limitaciones de la implementación  
 En esta implementación no se admiten las siguientes especificaciones de XQuery:  
  
-   Declaración de módulos (`version`)  
  
-   Declaración de módulos (`module namespace`)  
  
-   Xmpspacedeclaration (`xmlspace`)  
  
-   Declaración de intercalaciones predeterminadas (`declare default collation`)  
  
-   Declaración de identificadores URI base (`declare base-uri`)  
  
-   Declaración de construcciones (`declare construction`)  
  
-   Declaración del orden predeterminado (`declare ordering`)  
  
-   Importación de esquemas (`import schema namespace`)  
  
-   Importación de módulos (`import module`)  
  
-   Declaración de variables en el prólogo (`declare variable`)  
  
-   Declaración de funciones (`declare function`)  
  
## <a name="in-this-section"></a>En esta sección  
 [Prólogo de XQuery](../xquery/modules-and-prologs-xquery-prolog.md)  
 Describe el prólogo de XQuery.  
  
## <a name="see-also"></a>Vea también  
 [Referencia del lenguaje XQuery &#40;SQL Server&#41;](../xquery/xquery-language-reference-sql-server.md)  
  
  
