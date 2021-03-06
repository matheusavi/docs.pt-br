---
title: "'<interfacename>.<membername>' já é implementado pela classe base '<baseclassname>'. Reimplementação de <type> assumido"
ms.date: 07/20/2015
f1_keywords:
- vbc42015
- bc42015
helpviewer_keywords:
- BC42015
ms.assetid: 658c070a-113e-4bd8-b294-12c243191160
ms.openlocfilehash: 8137f6b1712b6a0752a991f5a3d598b5f958252c
ms.sourcegitcommit: ff5a4eb5cffbcac9521bc44a907a118cd7e8638d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/17/2020
ms.locfileid: "92162811"
---
# <a name="bc42015-interfacenamemembername-is-already-implemented-by-the-base-class-baseclassname-re-implementation-of-type-assumed"></a>BC42015: ' \<interfacename> . \<membername> ' já está implementado pela classe base ' \<baseclassname> '. Reimplementação de \<type> assumido

Uma propriedade, um procedimento ou um evento em uma classe derivada usa uma `Implements` cláusula que especifica um membro de interface que já está implementado na classe base.

 Uma classe derivada pode reimplementar um membro de interface que é implementado por sua classe base. Isso não é o mesmo que substituir a implementação da classe base. Para obter mais informações, consulte [Implements](../statements/implements-clause.md).

 Por padrão, esta mensagem é um aviso. Para obter informações sobre como ocultar avisos ou tratar avisos como erros, consulte [Configurando avisos no Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic).

 **ID do erro:** BC42015

## <a name="to-correct-this-error"></a>Para corrigir este erro

- Se você pretende reimplementar o membro da interface, não precisa realizar nenhuma ação. O código em sua classe derivada acessa o membro reimplementado, a menos que você use a `MyBase` palavra-chave para acessar a implementação da classe base.

- Se você não pretende reimplementar o membro da interface, remova a `Implements` cláusula da propriedade, do procedimento ou da declaração de evento.

## <a name="see-also"></a>Veja também

- [Interfaces](../../programming-guide/language-features/interfaces/index.md)
