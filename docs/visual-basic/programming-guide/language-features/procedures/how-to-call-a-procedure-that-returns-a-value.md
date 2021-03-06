---
title: Como chamar um procedimento que retorna um valor
ms.date: 07/20/2015
helpviewer_keywords:
- procedure calls [Visual Basic], returning values
- Visual Basic code, procedures
- procedures [Visual Basic], calling
- procedures [Visual Basic], returning a value
ms.assetid: a445127b-0f5f-465a-98fb-3e514b93d115
ms.openlocfilehash: 53589f84c6675d1e7ae2a593341e5dac747132a9
ms.sourcegitcommit: bf5c5850654187705bc94cc40ebfb62fe346ab02
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/23/2020
ms.locfileid: "91083971"
---
# <a name="how-to-call-a-procedure-that-returns-a-value-visual-basic"></a>Como chamar um procedimento que retorna um valor (Visual Basic)

Um `Function` procedimento retorna um valor para o código de chamada. Você pode chamá-lo incluindo seu nome e argumentos no lado direito de uma instrução de atribuição ou em uma expressão.  
  
### <a name="to-call-a-function-procedure-within-an-expression"></a>Para chamar um procedimento Function dentro de uma expressão  
  
1. Use o `Function` nome do procedimento da mesma maneira que usaria uma variável. Você pode usar uma `Function` chamada de procedimento em qualquer lugar em que você possa usar uma variável ou constante em uma expressão.  
  
2. Siga o nome do procedimento com parênteses para colocar a lista de argumentos. Se não houver argumentos, você pode opcionalmente omitir os parênteses. No entanto, usar os parênteses torna seu código mais fácil de ler.  
  
3. Coloque os argumentos na lista de argumentos dentro dos parênteses, separados por vírgulas. Certifique-se de fornecer os argumentos na mesma ordem em que o `Function` procedimento define os parâmetros correspondentes.  
  
     Como alternativa, você pode passar um ou mais argumentos por nome. Para obter mais informações, consulte [passando argumentos por posição e por nome](./passing-arguments-by-position-and-by-name.md).  
  
4. O valor retornado do procedimento participa da expressão da mesma forma que o valor de uma variável ou constante.  
  
### <a name="to-call-a-function-procedure-in-an-assignment-statement"></a>Para chamar um procedimento Function em uma instrução de atribuição  
  
1. Use o `Function` nome do procedimento após o sinal de igual ( `=` ) na instrução de atribuição.  
  
2. Siga o nome do procedimento com parênteses para colocar a lista de argumentos. Se não houver argumentos, você pode opcionalmente omitir os parênteses. No entanto, usar os parênteses torna seu código mais fácil de ler.  
  
3. Coloque os argumentos na lista de argumentos dentro dos parênteses, separados por vírgulas. Certifique-se de fornecer os argumentos na mesma ordem em que o `Function` procedimento define os parâmetros correspondentes, a menos que você os esteja passando por nome.  
  
4. O valor retornado do procedimento é armazenado na variável ou propriedade no lado esquerdo da instrução de atribuição.  
  
## <a name="example"></a>Exemplo  

 O exemplo a seguir chama o Visual Basic <xref:Microsoft.VisualBasic.Interaction.Environ%2A> para recuperar o valor de uma variável de ambiente do sistema operacional. A primeira linha `Environ` é chamada dentro de uma expressão e a segunda linha a chama em uma instrução de atribuição. `Environ` usa o nome da variável como seu único argumento. Ele retorna o valor da variável para o código de chamada.  
  
 [!code-vb[VbVbcnProcedures#7](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#7)]  
  
## <a name="see-also"></a>Confira também

- [Procedimentos de função](./function-procedures.md)
- [Parâmetros e Argumentos de Procedimento](./procedure-parameters-and-arguments.md)
- [Instrução Function](../../../language-reference/statements/function-statement.md)
- [Como criar um procedimento que retorne um valor](./how-to-create-a-procedure-that-returns-a-value.md)
- [Como retornar um valor de um procedimento](./how-to-return-a-value-from-a-procedure.md)
- [Como chamar um procedimento que não retorne um valor](./how-to-call-a-procedure-that-does-not-return-a-value.md)
