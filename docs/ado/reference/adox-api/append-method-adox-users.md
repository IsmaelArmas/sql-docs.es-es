---
title: Append (método) (usuarios ADOX) | Microsoft Docs
ms.prod: sql
ms.prod_service: connectivity
ms.technology: connectivity
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: conceptual
apitype: COM
f1_keywords:
- Users::raw_Append
- Users::Append
helpviewer_keywords:
- Append method [ADOX]
ms.assetid: b80bc5d5-78ca-4f75-956b-2ac658029cc7
author: MightyPen
ms.author: genemi
manager: craigg
ms.openlocfilehash: e56391357e7a11c47efdf0ffaf3c9ae9704d5db3
ms.sourcegitcommit: 61381ef939415fe019285def9450d7583df1fed0
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2018
ms.locfileid: "47787214"
---
# <a name="append-method-adox-users"></a>Append (método) (usuarios ADOX)
Agrega un nuevo [usuario](../../../ado/reference/adox-api/user-object-adox.md) de objeto para el [usuarios](../../../ado/reference/adox-api/users-collection-adox.md) colección.  
  
## <a name="syntax"></a>Sintaxis  
  
```  
  
Users.Append User[,Password]  
```  
  
#### <a name="parameters"></a>Parámetros  
 *Usuario*  
 Un **Variant** valor que contiene el **usuario** objeto anexar o el nombre del usuario para crear y anexar.  
  
 *Contraseña*  
 Opcional. Un **cadena** valor que contiene la contraseña del usuario. El *contraseña* parámetro corresponde al valor especificado por el [ChangePassword](../../../ado/reference/adox-api/changepassword-method-adox.md) método de un **usuario** objeto.  
  
## <a name="remarks"></a>Comentarios  
 El **usuarios** colección de un [catálogo](../../../ado/reference/adox-api/catalog-object-adox.md) representa todas las de los usuarios del catálogo. El **usuarios** colección para un [grupo](../../../ado/reference/adox-api/group-object-adox.md) representa sólo los usuarios que tienen una pertenencia al grupo específico.  
  
 Se producirá un error si el proveedor no admite la creación de usuarios.  
  
> [!NOTE]
>  Antes de anexar una **usuario** de objeto para el **usuarios** colección de un **grupo** objeto, un **usuario** objeto con el mismo [nombre ](../../../ado/reference/adox-api/name-property-adox.md) ya debe existir en lo que se debe anexar el **usuarios** colección de la **catálogo**.  
  
## <a name="applies-to"></a>Se aplica a  
 [Colección de usuarios (ADOX)](../../../ado/reference/adox-api/users-collection-adox.md)  
  
## <a name="see-also"></a>Vea también  
 [Usuarios y grupos, ChangePassword ejemplo de métodos Append (VB)](../../../ado/reference/adox-api/groups-and-users-append-changepassword-methods-example-vb.md)   
 [Append (método) (columnas ADOX)](../../../ado/reference/adox-api/append-method-adox-columns.md)   
 [Append (método) (grupos ADOX)](../../../ado/reference/adox-api/append-method-adox-groups.md)   
 [Append (método) (índices ADOX)](../../../ado/reference/adox-api/append-method-adox-indexes.md)   
 [Append (método) (claves ADOX)](../../../ado/reference/adox-api/append-method-adox-keys.md)   
 [Append (método) (procedimientos ADOX)](../../../ado/reference/adox-api/append-method-adox-procedures.md)   
 [Append (método) (tablas ADOX)](../../../ado/reference/adox-api/append-method-adox-tables.md)   
 [Append (método) (vistas ADOX)](../../../ado/reference/adox-api/append-method-adox-views.md)
