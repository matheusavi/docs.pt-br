---
title: 'Como: Escrever uma função de agregação PLINQ personalizada'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- PLINQ queries, how to create aggregate function
ms.assetid: 5a70dd49-ab2a-4798-b551-196ee7042b1a
ms.openlocfilehash: d04f90e9c763c8ddba5ba07b650ffb878869ff3a
ms.sourcegitcommit: 965a5af7918acb0a3fd3baf342e15d511ef75188
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/18/2020
ms.locfileid: "94825462"
---
# <a name="how-to-write-a-custom-plinq-aggregate-function"></a>Como: Escrever uma função de agregação PLINQ personalizada
Este exemplo mostra como usar o método <xref:System.Linq.ParallelEnumerable.Aggregate%2A> para aplicar uma função de agregação personalizada a uma sequência de origem.  
  
> [!WARNING]
> Este exemplo tem como objetivo demonstrar o uso e pode não executar tão rápido quanto a consulta LINQ to Objects sequencial equivalente. Para saber mais sobre agilização, confira [Noções básicas sobre agilização no PLINQ](understanding-speedup-in-plinq.md).  
  
## <a name="example"></a>Exemplo  
 O exemplo a seguir calcula o desvio padrão de uma sequência de números inteiros.  
  
 [!code-csharp[PLINQ#31](../../../samples/snippets/csharp/VS_Snippets_Misc/plinq/cs/plinqsamples.cs#31)]
 [!code-vb[PLINQ#31](../../../samples/snippets/visualbasic/VS_Snippets_Misc/plinq/vb/plinqsnippets1.vb#31)]  
  
 Este exemplo usa uma sobrecarga do operador de consulta padrão de agregação que é exclusivo ao PLINQ. Essa sobrecarga usa um <xref:System.Func%603?displayProperty=nameWithType> adicional como o terceiro parâmetro de entrada. Este delegado combina os resultados de todos os threads antes de executar o cálculo final nos resultados agregados. Neste exemplo, somamos todos os threads.  
  
 Observe que quando um corpo da expressão lambda é composto por uma única expressão, o valor de retorno do delegado <xref:System.Func%602?displayProperty=nameWithType> é o valor da expressão.  
  
## <a name="see-also"></a>Confira também

- <xref:System.Linq.ParallelEnumerable>
- [LINQ paralelo (PLINQ)](introduction-to-plinq.md)
