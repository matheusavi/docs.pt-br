---
title: Como fazer referência à instância atual de um objeto
ms.date: 07/20/2015
helpviewer_keywords:
- variables [Visual Basic], object
- objects [Visual Basic], referring to current instance
- instances [Visual Basic], referring to current
- current instance
- object variables [Visual Basic]
ms.assetid: 7f9b2c77-03cd-428f-adc2-b18070226e7c
ms.openlocfilehash: 64d21fe4aaf6fd34bf880373a7ab3067fb67820e
ms.sourcegitcommit: bf5c5850654187705bc94cc40ebfb62fe346ab02
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/23/2020
ms.locfileid: "91077053"
---
# <a name="how-to-refer-to-the-current-instance-of-an-object-visual-basic"></a>Como fazer referência à instância atual de um objeto (Visual Basic)

A *instância atual* de um objeto é a instância na qual o código está sendo executado no momento.  
  
 Você usa a `Me` palavra-chave para se referir à instância atual.  
  
### <a name="to-refer-to-the-current-instance"></a>Para fazer referência à instância atual  
  
- Use a `Me` palavra-chave onde você normalmente usaria o nome de uma variável de objeto.  
  
    ```vb  
    Me.ForeColor = System.Drawing.Color.Crimson  
    Me.Close()  
    ```  
  
     Embora `Me` o se comporta como uma variável de objeto, você não pode declará-lo nem atribuir nada a ele. `Me` sempre refere-se à instância atual.  
  
## <a name="see-also"></a>Confira também

- [Variáveis de Objeto](object-variables.md)
- [Atribuição de variável do objeto](object-variable-assignment.md)
- [Me, My, MyBase e MyClass](../../program-structure/me-my-mybase-and-myclass.md)
