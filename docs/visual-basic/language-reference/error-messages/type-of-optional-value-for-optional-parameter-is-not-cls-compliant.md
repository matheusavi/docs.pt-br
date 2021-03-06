---
title: O tipo de valor opcional para o parâmetro opcional <parametername> não é compatível com CLS
ms.date: 07/20/2015
f1_keywords:
- BC40042
- vbc40042
helpviewer_keywords:
- BC40042
ms.assetid: 1d6eae29-4ad3-4434-bde4-a53b6051adf5
ms.openlocfilehash: e4fd7f0fd219eba7f20b62e0357d2139a21c0af7
ms.sourcegitcommit: ff5a4eb5cffbcac9521bc44a907a118cd7e8638d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/17/2020
ms.locfileid: "92162681"
---
# <a name="bc40042-type-of-optional-value-for-optional-parameter-parametername-is-not-cls-compliant"></a>BC40042: tipo de valor opcional para o parâmetro opcional \<parametername> não tem conformidade com CLS

Um procedimento é marcado como `<CLSCompliant(True)>` , mas declara um parâmetro [opcional](../modifiers/optional.md) com o valor padrão de um tipo não compatível.

 Para que um procedimento seja compatível com a [independência de idioma e](../../../standard/language-independence-and-language-independent-components.md) com os componentes de Language-Independent (CLS), ele deve usar somente tipos em conformidade com CLS. Isso se aplica aos tipos de parâmetros, ao tipo de retorno e aos tipos de todas as suas variáveis locais. Ele também se aplica aos valores padrão de parâmetros opcionais.

 Os tipos de dados a seguir Visual Basic não são compatíveis com CLS:

- [Tipo de Dados SByte](../data-types/sbyte-data-type.md)

- [Tipo de Dados UInteger](../data-types/uinteger-data-type.md)

- [Tipo de Dados ULong](../data-types/ulong-data-type.md)

- [Tipo de Dados UShort](../data-types/ushort-data-type.md)

 Quando você aplica o <xref:System.CLSCompliantAttribute> atributo a um elemento de programação, você define o parâmetro do atributo `isCompliant` como `True` ou `False` para indicar conformidade ou não conformidade. Não há nenhum padrão para esse parâmetro, e você deve fornecer um valor.

 Se você não se aplicar <xref:System.CLSCompliantAttribute> a um elemento, será considerado como não compatível.

 Por padrão, esta mensagem é um aviso. Para obter informações sobre como ocultar avisos ou tratar avisos como erros, consulte [Configurando avisos no Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic).

 **ID do erro:** BC40042

## <a name="to-correct-this-error"></a>Para corrigir este erro

- Se o parâmetro opcional deve ter um valor padrão desse tipo específico, remova <xref:System.CLSCompliantAttribute> . O procedimento não pode ser compatível com CLS.

- Se o procedimento deve ser compatível com CLS, altere o tipo desse valor padrão para o tipo em conformidade com CLS mais próximo. Por exemplo, no lugar de `UInteger` você pode ser capaz de usar `Integer` se não precisar do intervalo de valores acima de 2.147.483.647. Se você precisar do intervalo estendido, poderá substituir `UInteger` por `Long` .

- Se você estiver fazendo a interface com automação ou objetos COM, tenha em mente que alguns tipos têm larguras de dados diferentes das .NET Framework. Por exemplo, `int` geralmente é 16 bits em outros ambientes. Se você estiver aceitando um inteiro de 16 bits desse componente, declare-o como `Short` em vez de `Integer` em seu código de Visual Basic gerenciado.
