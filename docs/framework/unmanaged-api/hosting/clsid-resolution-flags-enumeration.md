---
title: Enumeração CLSID_RESOLUTION_FLAGS
ms.date: 03/30/2017
api_name:
- CLSID_RESOLUTION_FLAGS
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CLSID_RESOLUTION_FLAGS
helpviewer_keywords:
- CLSID_RESOLUTION_FLAGS enumeration [.NET Framework hosting]
ms.assetid: cd8b9879-962a-4811-aa46-2e2b6bae0d84
topic_type:
- apiref
ms.openlocfilehash: 5ac015f958d9504bbd14a66ead86548b8df32764
ms.sourcegitcommit: 27db07ffb26f76912feefba7b884313547410db5
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/19/2020
ms.locfileid: "83616769"
---
# <a name="clsid_resolution_flags-enumeration"></a>Enumeração CLSID_RESOLUTION_FLAGS
Contém valores que indicam como o Common Language Runtime (CLR) deve resolver um `CLSID` .  
  
## <a name="syntax"></a>Sintaxe  
  
```cpp  
typedef enum {  
    CLSID_RESOLUTION_DEFAULT      = 0x0,  
    CLSID_RESOLUTION_REGISTERED   = 0x1  
} CLSID_RESOLUTION_FLAGS;  
```  
  
## <a name="members"></a>Membros  
  
|Membro|Descrição|  
|------------|-----------------|  
|`CLSID_RESOLUTION_DEFAULT`|Indica o comportamento padrão.|  
|`CLSID_RESOLUTION_REGISTERED`|Indica que o tempo de execução pesquisa o registro e aplica a política Shim.|  
  
## <a name="requirements"></a>Requisitos  
 **Plataformas:** confira [Requisitos do sistema](../../get-started/system-requirements.md).  
  
 **Cabeçalho:** MSCorEE. h  
  
 **.NET Framework versões:**[!INCLUDE[net_current_v11plus](../../../../includes/net-current-v11plus-md.md)]  
  
## <a name="see-also"></a>Veja também

- [Hospedando enumerações](hosting-enumerations.md)
