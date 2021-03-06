---
title: archivo de inclusión
description: archivo de inclusión
services: virtual-machines
author: roygara
ms.service: virtual-machines
ms.topic: include
ms.date: 07/14/2020
ms.author: rogarana
ms.custom: include file
ms.openlocfilehash: f6175a797b14077cafacaca1f2fd48f36e945d9e
ms.sourcegitcommit: e71da24cc108efc2c194007f976f74dd596ab013
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/29/2020
ms.locfileid: "87425017"
---
Los discos compartidos solo se pueden habilitar para un subconjunto de tipos de disco. Actualmente, solo los discos Ultra Disks y SSD Premium pueden habilitar discos compartidos. Cada disco administrado que tiene discos compartidos habilitados está sujeto a las siguientes limitaciones, organizadas según el tipo de disco:

### <a name="ultra-disks"></a>Discos Ultra

Los discos Ultra Disks tienen su propia lista independiente de limitaciones, que no están relacionadas con los discos compartidos. Para conocer las limitaciones de Ultra Disks, vea [Uso de Azure Ultra Disks](../articles/virtual-machines/linux/disks-enable-ultra-ssd.md).

Al compartir discos Ultra Disks, estos tienen las siguientes limitaciones adicionales:

- Actualmente, se limita a la compatibilidad con Azure Resource Manager o SDK. 
- Solo se pueden usar discos básicos con algunas versiones del clúster de conmutación por error de Windows Server. Para más información, consulte [Requisitos de hardware y opciones de almacenamiento de clústeres de conmutación por error](https://docs.microsoft.com/windows-server/failover-clustering/clustering-requirements).

Los discos Ultra Disks compartidos están disponibles en todas las regiones que admiten este tipo de disco de forma predeterminada y no requieren que se registren para poder usarlos.

### <a name="premium-ssds"></a>SSD Premium

- Solo se admite actualmente en la región Centro-oeste de EE. UU.
- Actualmente, se limita a la compatibilidad con Azure Resource Manager o SDK. 
- Solo se puede habilitar en discos de datos, no en discos de sistema operativo.
- El almacenamiento en caché del host de **solo lectura** no está disponible para los discos SSD premium con `maxShares>1`.
- La expansión de disco no está disponible para los discos SSD premium con `maxShares>1`.
- Al usar conjuntos de disponibilidad y conjuntos de escalado de máquinas virtuales con discos compartidos de Azure, la [alineación del dominio de error del almacenamiento](https://docs.microsoft.com/azure/virtual-machines/windows/manage-availability#use-managed-disks-for-vms-in-an-availability-set) con el dominio de error de la máquina virtual no se exige para el disco de datos compartido.
- Al usar [grupos con ubicación por proximidad (PPG)](../articles/virtual-machines/windows/proximity-placement-groups.md), todas las máquinas virtuales que comparten un disco deben ser parte del mismo grupo con ubicación por proximidad.
- Solo se pueden usar discos básicos con algunas versiones del clúster de conmutación por error de Windows Server. Para más información, consulte [Requisitos de hardware y opciones de almacenamiento de clústeres de conmutación por error](https://docs.microsoft.com/windows-server/failover-clustering/clustering-requirements).
- La compatibilidad con Azure Backup y Azure Site Recovery todavía no está disponible.

Si está interesado en probar unidades SSD Premium compartidas, [regístrese para obtener acceso](https://aka.ms/AzureSharedDiskGASignUp).