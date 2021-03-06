---
author: roygara
ms.service: storage
ms.topic: include
ms.date: 05/06/2019
ms.author: rogarana
ms.openlocfilehash: 8034a7a520cc50b2e57e0ad26205da2e408296a1
ms.sourcegitcommit: afa1411c3fb2084cccc4262860aab4f0b5c994ef
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2020
ms.locfileid: "88760589"
---
| Resource | Recursos compartidos de archivos estándar | Recursos compartidos de archivos Prémium |
|----------|---------------|------------------------------------------|
| Tamaño máximo de un recurso compartido de archivos | Sin mínimo; pago por uso | 100 GiB; aprovisionado |
| Tamaño máximo de un recurso compartido de archivos | 100 TiB*, 5 TiB | 100 TiB |
| Tamaño máximo de un archivo en un recurso compartido de archivos | 1 TiB | 4 TiB |
| Número máximo de archivos en un recurso compartido de archivos | Sin límite | Sin límite |
| Número máximo de IOPS por recurso compartido | 10 000 IOPS*, 1000 IOPS o 100 solicitudes in 100 ms | 100.000 IOPS |
| Número máximo de directivas de acceso almacenadas por recurso compartido de archivos | 5 | 5 |
| Rendimiento de destino para un único recurso compartido de archivos | hasta 300 MiB/s*, hasta 60 MiB/s,  | Consulte los valores de entrada y salida del recurso compartido de archivos Premium|
| Salida máxima para un único recurso compartido de archivos | Consulte el rendimiento de destino del recurso compartido de archivos estándar. | Hasta 6204 MiB/s |
| Entrada máxima para un único recurso compartido de archivos | Consulte el rendimiento de destino del recurso compartido de archivos estándar. | Hasta 4136 MiB/s |
| Número máximo de identificadores abiertos por archivo o directorio | 2\.000 identificadores abiertos | 2\.000 identificadores abiertos |
| Número máximo de instantáneas de recurso compartido | 200 instantáneas de recurso compartido | 200 instantáneas de recurso compartido |
| Longitud máxima del nombre de objeto (archivos y directorios) | 2048 caracteres | 2048 caracteres |
| Número máximo de componentes de la ruta de acceso (en la ruta de acceso \A\B\C\D, cada letra es un componente) | 255 caracteres | 255 caracteres |

\* El valor predeterminado en recursos compartidos de archivos estándar es de 5 TiB, consulte [Habilitar y crear recursos compartidos de archivos de gran tamaño](../articles/storage/files/storage-files-how-to-create-large-file-share.md) para obtener información detallada sobre cómo aumentar en escala los recursos compartidos de archivos estándar hasta 100 TiB.
