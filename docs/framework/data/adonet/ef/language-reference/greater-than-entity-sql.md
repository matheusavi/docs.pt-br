---
title: '>  (Maior que) (Entity SQL)'
ms.date: 03/30/2017
ms.assetid: 4cea865c-677c-4b06-99a1-010f2ae2394a
ms.openlocfilehash: 52a9f9f645aa51402ceb8cb0a40d2040d1c0802c
ms.sourcegitcommit: 5b475c1855b32cf78d2d1bbb4295e4c236f39464
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/24/2020
ms.locfileid: "91147938"
---
# <a name="-greater-than-entity-sql"></a>> (maior que) (Entity SQL)

Compara duas expressões para determinar se a expressão da esquerda tem um valor maior que a expressão da direita.  
  
## <a name="syntax"></a>Sintaxe  
  
```sql  
expression > expression  
```  
  
## <a name="arguments"></a>Argumentos  

 `expression`  
 Qualquer expressão válida. Ambas as expressões devem ter tipos de dados implicitamente conversíveis.  
  
## <a name="result-types"></a>Tipos de resultado  

 `true` se a expressão esquerda tem um valor maior que a expressão direita; caso contrário, `false`.  
  
## <a name="example"></a>Exemplo  

 A consulta Entity SQL a seguir usa > operador de comparação para comparar duas expressões para determinar se a expressão esquerda tem um valor maior que a expressão direita. A consulta é baseada no modelo de vendas AdventureWorks. Para compilar e executar essa consulta, siga estas etapas:  
  
1. Siga o procedimento em [como executar uma consulta que retorna resultados de estruturaistype](../how-to-execute-a-query-that-returns-structuraltype-results.md).  
  
2. Passe a consulta a seguir como um argumento para o método `ExecuteStructuralTypeQuery`:  
  
 [!code-sql[DP EntityServices Concepts#GREATER](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#greater)]  
  
## <a name="see-also"></a>Confira também

- [Referência de Entity SQL](entity-sql-reference.md)
