---
title: 'Como: implementar um particionador para particionamento estático'
ms.date: 03/30/2017
helpviewer_keywords:
- tasks, how to create a static partitioner
ms.assetid: f4410508-cac6-4ba7-bef1-c5e68b2794f3
ms.openlocfilehash: 1593f1bc3c17f162b20f8bd9f645d51393f2198c
ms.sourcegitcommit: 965a5af7918acb0a3fd3baf342e15d511ef75188
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/18/2020
ms.locfileid: "94817126"
---
# <a name="how-to-implement-a-partitioner-for-static-partitioning"></a>Como: implementar um particionador para particionamento estático
O exemplo a seguir mostra uma maneira de implementar um particionador personalizado simples para PLINQ que executa o particionamento estático. Como o particionador não oferece suporte a partições dinâmicas, não é consumido de <xref:System.Threading.Tasks.Parallel.ForEach%2A?displayProperty=nameWithType>. Esse particionador específico pode fornecer a agilização sobre o particionador de intervalo padrão para fontes de dados para as quais cada elemento requer um volume crescente de tempo de processamento.  
  
## <a name="example"></a>Exemplo  
 [!code-csharp[TPL_Partitioners#05](../../../samples/snippets/csharp/VS_Snippets_Misc/tpl_partitioners/cs/partitioners.cs#05)]  
  
 As partições neste exemplo baseiam-se na suposição de um aumento linear no tempo de processamento para cada elemento. No mundo real, pode ser difícil de prever os tempos de processamento dessa maneira. Se você estiver usando um particionador estático com uma fonte de dados específica, poderá otimizar a fórmula de particionamento para a fonte, adicionar lógica de balanceamento de carga ou usar uma abordagem de particionamento de parte, conforme demonstrado em [Como implementar as partições dinâmicas](how-to-implement-dynamic-partitions.md).  
  
## <a name="see-also"></a>Confira também

- [Particionadores personalizados para PLINQ e TPL](custom-partitioners-for-plinq-and-tpl.md)
