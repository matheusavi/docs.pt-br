---
title: Métodos de System.Math
ms.date: 03/30/2017
ms.assetid: 0f299521-6f41-4720-bd70-67c93fc50948
ms.openlocfilehash: e91c8ea95d21288ad2577f1550333febd448766d
ms.sourcegitcommit: 5b475c1855b32cf78d2d1bbb4295e4c236f39464
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/24/2020
ms.locfileid: "91158195"
---
# <a name="systemmath-methods"></a>Métodos de System.Math

[!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] não oferece suporte aos seguintes métodos de <xref:System.Math> .  
  
- <xref:System.Math.DivRem%28System.Int32%2CSystem.Int32%2CSystem.Int32%40%29?displayProperty=nameWithType>  
  
- <xref:System.Math.DivRem%28System.Int64%2CSystem.Int64%2CSystem.Int64%40%29?displayProperty=nameWithType>  
  
- <xref:System.Math.IEEERemainder%28System.Double%2CSystem.Double%29?displayProperty=nameWithType>  
  
## <a name="differences-from-net"></a>Diferenças do .NET  

 O.NET Framework tem a semântica por arredondamento diferente do SQL Server. O <xref:System.Math.Round%2A> método na .NET Framework executa o *arredondamento do banco*, em que os números terminam em 0,5 arredondado para o dígito par mais próximo, em vez de para o próximo dígito superior. Por exemplo, círculos 2,5 a 2, quando círculos 3,5 a 4. (Essa técnica ajuda a evitar a polarização sistemática para os valores mais altos em grandes transações de dados.)  
  
 Em SQL, a função de `ROUND` vez arredondará sempre fora de 0. Portanto círculos 2,5 a 3, contrastado com o arredondamento para 2 no.NET Framework.  
  
 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] passa completamente a semântica do SQL `ROUND` e não tenta implementar arredondamento bancário.  
  
## <a name="see-also"></a>Confira também

- [Tipos de dados e funções](data-types-and-functions.md)
