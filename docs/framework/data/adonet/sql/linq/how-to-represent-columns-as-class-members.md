---
title: 'Como: declarar colunas como membros de classe'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 7ab28021-4d15-4d9c-bf2e-6ccc0daa7d1a
ms.openlocfilehash: e73b017b5a500a8c48b3fe22557f6c6619f3b227
ms.sourcegitcommit: 5b475c1855b32cf78d2d1bbb4295e4c236f39464
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/24/2020
ms.locfileid: "91166344"
---
# <a name="how-to-represent-columns-as-class-members"></a>Como: declarar colunas como membros de classe

Use o [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <xref:System.Data.Linq.Mapping.ColumnAttribute> atributo para associar um campo ou propriedade a uma coluna de banco de dados.  
  
### <a name="to-map-a-field-or-property-to-a-database-column"></a>Para mapear um campo ou propriedade a uma coluna de base de dados  
  
- Adicione o atributo de <xref:System.Data.Linq.Mapping.ColumnAttribute> à declaração de propriedade ou campo.  
  
## <a name="example"></a>Exemplo  

 O código a seguir mapeia o campo de `CustomerID` na classe de `Customer` para a coluna de `CustomerID` na tabela de base de dados de `Customers` .  
  
 [!code-csharp[DLinqCustomize#2](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqCustomize/cs/Program.cs#2)]
 [!code-vb[DLinqCustomize#2](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqCustomize/vb/Module1.vb#2)]  
  
 Você não precisa especificar a propriedade de <xref:System.Data.Linq.Mapping.DataAttribute.Name%2A> se o nome pode ser inferido. Se você não especificar um nome, o nome é presumido ser o mesmo nome que a propriedade ou do campo.  
  
## <a name="see-also"></a>Confira também

- [Modelo de objeto LINQ to SQL](the-linq-to-sql-object-model.md)
- [Como: personalizar classes de entidade usando o editor de códigos](how-to-customize-entity-classes-by-using-the-code-editor.md)
