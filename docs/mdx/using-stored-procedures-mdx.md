---
title: Usar procedimientos almacenados (MDX) | Documentos de Microsoft
ms.custom: 
ms.date: 03/02/2016
ms.prod: sql-server-2016
ms.reviewer: 
ms.suite: 
ms.technology:
- analysis-services
ms.tgt_pltfrm: 
ms.topic: language-reference
dev_langs:
- kbMDX
helpviewer_keywords:
- user-defined functions [MDX]
- stored procedures [MDX]
ms.assetid: 818fb2ad-f88b-4d0c-9f70-f378aed42e8e
caps.latest.revision: 27
author: Minewiskan
ms.author: owend
manager: erikre
ms.translationtype: MT
ms.sourcegitcommit: 1419847dd47435cef775a2c55c0578ff4406cddc
ms.openlocfilehash: 2c24641d2be7e4e2130d21881b94a9bcd1698fd7
ms.contentlocale: es-es
ms.lasthandoff: 08/02/2017

---
# <a name="using-stored-procedures-mdx"></a>Usar procedimientos almacenados (MDX)
[!INCLUDE[tsql-appliesto-ss2008-xxxx-xxxx-xxx_md](../includes/tsql-appliesto-ss2008-xxxx-xxxx-xxx-md.md)]

  Puede ampliar la funcionalidad de [!INCLUDE[ssASnoversion](../includes/ssasnoversion-md.md)] y MDX (Expresiones Multidimensionales) escribiendo funciones definidas por el usuario o procedimientos almacenados de .NET. Para obtener más información, vea [ADOMD.NET Server Programming](../analysis-services/multidimensional-models-adomd-net-server/adomd-net-server-programming.md)  
  
 Cuando haga referencia o llame a un procedimiento almacenado, especifique el nombre de la función seguido de paréntesis. Dentro de los paréntesis puede especificar expresiones denominadas argumentos, que proporcionan los datos que se van a pasar a los parámetros. Cuando llame una función, debe proporcionar valores de argumentos para todos los parámetros, así como especificar los valores de argumentos en la misma secuencia en la que se definen los parámetros en la función definida por el usuario.  
  
 La consulta de ejemplo siguiente supone que tiene un ensamblado denominado SampleAssembly registrado en su servidor de [!INCLUDE[ssASnoversion](../includes/ssasnoversion-md.md)]:  
  
```  
SELECT SampleAssembly.RandomSample([Geography].[State-Province].Members, 5) on ROWS,   
[Date].[Calendar].[Calendar Year] on COLUMNS  
FROM [Adventure Works]  
WHERE [Measures].[Reseller Freight Cost]  
```  
  
> [!NOTE]  
>  *Procedimiento almacenado* es la terminología utilizada en [!INCLUDE[msCoName](../includes/msconame-md.md)] [!INCLUDE[ssNoVersion](../includes/ssnoversion-md.md)] [!INCLUDE[ssASnoversion](../includes/ssasnoversion-md.md)] para estos tipos de funciones. Las versiones anteriores de [!INCLUDE[ssASnoversion](../includes/ssasnoversion-md.md)] llama a estos tipos de funciones como *funciones definidas por el usuario*.  
  
## <a name="types-of-stored-procedures"></a>Tipos de procedimientos almacenados  
 [!INCLUDE[ssASnoversion](../includes/ssasnoversion-md.md)] es compatible con ambos tipos de ensamblados: COM y CLR. Se recomienda usar los ensamblados CLR porque ofrecen una seguridad mejorada. Si se instala Microsoft Office Excel en el servidor, también se pueden usar funciones de Excel.  
  
> [!NOTE]  
>  Los ensamblados COM de Microsoft Visual Basic para Aplicaciones (VBA) se registran de forma automática.  
  
## <a name="see-also"></a>Vea también  
 [Funciones &#40; La sintaxis de MDX &#41;](../mdx/functions-mdx-syntax.md)  
  
  
