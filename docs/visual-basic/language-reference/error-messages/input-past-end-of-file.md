---
title: Entrada passou do final do arquivo
ms.date: 07/20/2015
f1_keywords:
- vbrID62
ms.assetid: 65292704-6e7d-4622-9f50-eb655a59b016
ms.openlocfilehash: c0cb0373fb0652e9600ac8651661708414561aca
ms.sourcegitcommit: d2db216e46323f73b32ae312c9e4135258e5d68e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/22/2020
ms.locfileid: "90873960"
---
# <a name="input-past-end-of-file"></a>Entrada passou do final do arquivo

Uma `Input` instrução está lendo um arquivo vazio ou um em que todos os dados são usados, ou você usou a `EOF` função com um arquivo aberto para acesso binário.  
  
## <a name="to-correct-this-error"></a>Para corrigir este erro  
  
1. Use a `EOF` função imediatamente antes da `Input` instrução para detectar o final do arquivo.  
  
2. Se o arquivo for aberto para acesso binário, use `Seek` e `Loc` .  
  
## <a name="see-also"></a>Confira também

- <xref:Microsoft.VisualBasic.FileSystem.Input%2A>
- <xref:Microsoft.VisualBasic.FileSystem.EOF%2A>
- <xref:Microsoft.VisualBasic.FileSystem.Seek%2A>
- <xref:Microsoft.VisualBasic.FileSystem.Loc%2A>
