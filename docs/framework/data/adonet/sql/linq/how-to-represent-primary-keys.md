---
title: 'Como: declarar chaves primárias'
ms.date: 03/30/2017
ms.assetid: 63c65289-6539-42b2-8493-891c232018fa
ms.openlocfilehash: 02570176c8aef5cfdc7ba09fd6976f430900e8df
ms.sourcegitcommit: 5b475c1855b32cf78d2d1bbb4295e4c236f39464
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/24/2020
ms.locfileid: "91166229"
---
# <a name="how-to-represent-primary-keys"></a>Como: declarar chaves primárias

Use a [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <xref:System.Data.Linq.Mapping.ColumnAttribute.IsPrimaryKey%2A> propriedade no <xref:System.Data.Linq.Mapping.ColumnAttribute> atributo para designar uma propriedade ou campo para representar a chave primária para uma coluna de banco de dados.  
  
 Para exemplos de código, consulte <xref:System.Data.Linq.Mapping.ColumnAttribute.IsPrimaryKey%2A>.  
  
> [!NOTE]
> [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] não suporta colunas computadas como chaves primárias.  
  
### <a name="to-designate-a-property-or-field-as-a-primary-key"></a>Para designar uma propriedade ou um campo como uma chave primária  
  
1. Adicione a propriedade de <xref:System.Data.Linq.Mapping.ColumnAttribute.IsPrimaryKey%2A> ao atributo de <xref:System.Data.Linq.Mapping.ColumnAttribute> .  
  
2. Especificar o valor como `true`.  
  
## <a name="see-also"></a>Confira também

- [Modelo de objeto LINQ to SQL](the-linq-to-sql-object-model.md)
- [Como: personalizar classes de entidade usando o editor de códigos](how-to-customize-entity-classes-by-using-the-code-editor.md)
