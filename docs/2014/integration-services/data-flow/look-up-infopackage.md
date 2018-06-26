---
title: Buscar Infopackage | Microsoft Docs
ms.custom: ''
ms.date: 06/13/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.suite: ''
ms.technology:
- integration-services
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 7c0cb7a4-cd07-44cc-85cb-eb1ad91f85fd
caps.latest.revision: 9
author: douglaslMS
ms.author: douglasl
manager: jhubbard
ms.openlocfilehash: 7f217126c83e1bc4f81971df3c3e7b5044f08171
ms.sourcegitcommit: 5dd5cad0c1bbd308471d6c885f516948ad67dfcf
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2018
ms.locfileid: "36112308"
---
# <a name="look-up-infopackage"></a>Buscar InfoPackage
  Use el cuadro de diálogo **Buscar InfoPackage** para buscar un InfoPackage que se haya definido en el sistema de SAP Netweaver BW. Cuando aparezca la lista de InfoPackages, seleccione el InfoPackage que desee y el destino rellenará las opciones asociadas a los valores necesarios.  
  
 El destino de SAP BW de [!INCLUDE[msCoName](../../includes/msconame-md.md)] Connector 1.1 for SAP BW usa el cuadro de diálogo **Buscar cadena de procesos** . Para obtener más información acerca del destino de SAP BW, vea [SAP BW Destination](sap-bw-destination.md).  
  
> [!IMPORTANT]  
>  La documentación de Microsoft Connector 1.1 for SAP BW da por supuesto que se está familiarizado con el entorno SAP Netweaver BW. Para obtener más información acerca de SAP Netweaver BW, o sobre cómo configurar los objetos y los procesos de SAP Netweaver BW, vea la documentación de SAP.  
  
 **Para abrir el cuadro de diálogo Buscar InfoPackage**  
  
1.  En [!INCLUDE[ssBIDevStudioFull](../../includes/ssbidevstudiofull-md.md)], abra el paquete de [!INCLUDE[ssISnoversion](../../includes/ssisnoversion-md.md)] que contiene el destino SAP BW.  
  
2.  En la pestaña **Flujo de datos** , haga doble clic en el destino de SAP BW.  
  
3.  En **Editor de destino SAP BW**, haga clic en **Administrador de conexiones** para abrir la página **Administrador de conexiones** del editor.  
  
4.  En la página **Administrador de conexiones** , en el cuadro del grupo **InfoPackage/InfoSource** , haga clic en **Buscar** para mostrar el cuadro de diálogo **Buscar InfoPackage** .  
  
## <a name="lookup-options"></a>Opciones de búsqueda  
 En los campos de búsqueda, puede filtrar los resultados mediante el carácter comodín de asterisco (*) o mediante una cadena parcial en combinación con el carácter comodín de asterisco. Sin embargo, si deja un campo de búsqueda vacío, la operación de búsqueda solamente se corresponderá con cadenas vacías en ese campo.  
  
 **InfoPackage**  
 Escriba el nombre del InfoPackage que desea buscar o un nombre parcial con el carácter comodín de asterisco (*). O bien, use el carácter comodín de asterisco por sí solo para incluir todos los InfoPackages.  
  
 **InfoSource**  
 Escriba el nombre del InfoSource que desea buscar o un nombre parcial con el carácter comodín de asterisco (*). O bien, use el carácter comodín de asterisco por sí solo para incluir todos los InfoPackages independientemente del InfoSource.  
  
 **Sistema de origen**  
 Escriba el nombre del sistema de origen o un nombre parcial con el carácter comodín de asterisco (*). O bien, use el carácter comodín de asterisco por sí solo para incluir todos los InfoPackages independientemente de los sistemas de origen.  
  
 **Buscar**  
 Permite buscar InfoPackages coincidentes que se hayan definido en el sistema SAP Netweaver BW.  
  
## <a name="lookup-results"></a>Buscar resultados  
 Después de hacer clic en el botón Buscar, aparece una lista de InfoPackages del sistema SAP Netweaver BW en una tabla con los siguientes encabezados de columna.  
  
 **InfoPackage**  
 Permite mostrar el nombre del InfoPackage que se haya definido en el sistema de SAP Netweaver BW.  
  
 **Tipo**  
 Permite mostrar el tipo de InfoPackage. En la siguiente tabla se muestran los posibles valores para el tipo.  
  
|Valor|Descripción|  
|-----------|-----------------|  
|de transacciones|Datos de transacción.|  
|Atr.|Datos de atributo.|  
|Textos|Textos.|  
  
 **Descripción**  
 Permite mostrar la descripción del InfoPackage.  
  
 **InfoSource**  
 Permite mostrar el nombre del InfoSource, en su caso, que está asociado al InfoPackage.  
  
 **Source System**  
 Permite mostrar el nombre del sistema de origen.  
  
 Cuando aparezca la lista de InfoPackages, seleccione el InfoPackage que desee y el destino rellenará las opciones asociadas a los valores necesarios.  
  
## <a name="see-also"></a>Vea también  
 [Editor de destino de SAP BW &#40;página Administrador de conexiones&#41;](sap-bw-destination-editor-connection-manager-page.md)   
 [Microsoft Connector 1.1 for SAP BW F1 Ayuda](../microsoft-connector-for-sap-bw-f1-help.md)  
  
  