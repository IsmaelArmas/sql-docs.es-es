---
title: RingN (tipo de datos geography) | Documentos de Microsoft
ms.custom: 
ms.date: 03/14/2017
ms.prod: sql-non-specified
ms.reviewer: 
ms.suite: 
ms.technology:
- database-engine
ms.tgt_pltfrm: 
ms.topic: language-reference
f1_keywords:
- RingN
- RingN_TSQL
dev_langs:
- TSQL
helpviewer_keywords:
- RingN method
ms.assetid: 30f47275-2727-4d22-bbec-c0c54bcb3ac2
caps.latest.revision: 14
author: BYHAM
ms.author: rickbyh
manager: jhubbard
ms.translationtype: MT
ms.sourcegitcommit: 876522142756bca05416a1afff3cf10467f4c7f1
ms.openlocfilehash: ddb30679406574a2f5f96687c4c04fae4c58f8e3
ms.contentlocale: es-es
ms.lasthandoff: 09/01/2017

---
# <a name="ringn-geography-data-type"></a>RingN (tipo de datos geography)
[!INCLUDE[tsql-appliesto-ss2008-asdb-xxxx-xxx_md](../../includes/tsql-appliesto-ss2008-asdb-xxxx-xxx-md.md)]

  Devuelve el anillo especificado de la **geography** instancia: `1 ≤ n ≤ NumRings()`.  
  
## <a name="syntax"></a>Sintaxis  
  
```  
  
.RingN (expression )  
```  
  
## <a name="arguments"></a>Argumentos  
 *expression*  
 Es un **int** expresión entre 1 y el número de anillos en una **polígono** instancia.  
  
## <a name="return-value"></a>Valor devuelto  
 [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)]tipo de valor devuelto: **geography**  
  
 Tipo de valor devuelto de CLR: **SqlGeography**  
  
## <a name="remarks"></a>Comentarios  
 Si el valor de índice del anillo  **n**  es menor que 1, este método produce una **ArgumentOutOfRangeException.** El valor de índice de anillo debe ser mayor o igual que 1 y debe ser menor o igual que el número devuelto por `NumRings()`.  
  
## <a name="examples"></a>Ejemplos  
 En este ejemplo se crea una instancia de `Polygon` con dos anillos y se devuelve el segundo anillo.  
  
```  
DECLARE @g geography;  
SET @g = geography::STGeomFromText('POLYGON((-122.358 47.653, -122.348 47.649, -122.348 47.658, -122.358 47.658, -122.358 47.653), (-122.357 47.654, -122.357 47.657, -122.349 47.657, -122.349 47.650, -122.357 47.654))', 4326);  
SELECT @g.RingN(2).ToString();  
```  
  
## <a name="see-also"></a>Vea también  
 [Métodos extendidos en instancias de Geography](../../t-sql/spatial-geography/extended-methods-on-geography-instances.md)   
 [NumRings &#40;tipo de datos geography&#41;](../../t-sql/spatial-geography/numrings-geography-data-type.md)  
  
  