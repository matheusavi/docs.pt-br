---
title: QUALQUERELEMENTO (Entity SQL)
ms.date: 03/30/2017
ms.assetid: 475a9ad6-8c8d-4f49-9970-af273e5360f1
ms.openlocfilehash: e060956545ca924fa6fedb80b2f53ff312f307a2
ms.sourcegitcommit: 5b475c1855b32cf78d2d1bbb4295e4c236f39464
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/24/2020
ms.locfileid: "91201194"
---
# <a name="anyelement-entity-sql"></a>QUALQUERELEMENTO (Entity SQL)

Extrai um elemento de uma coleção multivalorada.  
  
## <a name="syntax"></a>Sintaxe  
  
```csharp
ANYELEMENT ( expression )  
```  
  
## <a name="arguments"></a>Argumentos  

 `expression`  
 Qualquer expressão de consulta válida de que retornar uma coleção para extrair um elemento.  
  
## <a name="return-value"></a>Valor Retornado  

 Um único elemento na coleção ou um elemento arbitrário se a coleção tem mais de uma; se a coleção estiver vazia, retorna `null`. Se `collection` for uma coleção do tipo `Collection<T>` , `ANYELEMENT(collection)` será uma expressão válida que produz uma instância do tipo `T` .  
  
## <a name="remarks"></a>Comentários  

 ANYELEMENT extrai um elemento arbitrário de uma coleção multivalorado. Por exemplo, o exemplo a seguir tenta extrair um elemento singleton do conjunto `Customers` .  
  
```csharp
ANYELEMENT(Customers)  
```  
  
## <a name="example"></a>Exemplo  

 A seguinte consulta de [!INCLUDE[esql](../../../../../../includes/esql-md.md)] usa o operador de ANYELEMENT para extrair um elemento de uma coleção multivalorado. A consulta é baseada no modelo de vendas AdventureWorks. Para compilar e executar essa consulta, siga estas etapas:  
  
1. Siga o procedimento em [como executar uma consulta que retorna resultados de estruturaistype](../how-to-execute-a-query-that-returns-structuraltype-results.md).  
  
2. Passe a consulta a seguir como um argumento para o método `ExecuteStructuralTypeQuery`:  
  
 [!code-csharp[DP EntityServices Concepts 2#ANYELEMENT](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#anyelement)]  
  
## <a name="see-also"></a>Veja também

- [Referência de Entity SQL](entity-sql-reference.md)
- [Tipos estruturados que permitem valor nulo](nullable-structured-types-entity-sql.md)
