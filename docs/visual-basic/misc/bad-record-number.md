---
title: Número de registro inválido
ms.date: 07/20/2015
f1_keywords:
- vbrID63
ms.assetid: 1fcc33f8-822a-4de9-a6e3-228ddb5824a6
ms.openlocfilehash: 8cbffc7714211fb10bedc3a73729eac59d98f0bb
ms.sourcegitcommit: bf5c5850654187705bc94cc40ebfb62fe346ab02
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/23/2020
ms.locfileid: "91086979"
---
# <a name="bad-record-number"></a>Número de registro inválido

O número do registro `a FileGet` na `FilePut` instrução,, `FileGetObject` ou `FilePutObject` é menor ou igual a zero.  
  
## <a name="to-correct-this-error"></a>Para corrigir este erro  
  
1. Verifique os cálculos usados na geração do número de registro. Verifique a ortografia das variáveis que contêm o número do registro ou usadas no cálculo de números de registro. Um nome de variável digitado incorretamente é declarado implicitamente e inicializado como zero, a menos que você tenha usado `Option Explicit On` no módulo.  
  
## <a name="see-also"></a>Confira também

- [Instrução Option Explicit](../language-reference/statements/option-explicit-statement.md)
