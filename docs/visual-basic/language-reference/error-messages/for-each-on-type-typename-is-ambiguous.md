---
title: "'For Each' no tipo '<typename>' é ambíguo porque o tipo implementa várias instâncias de 'System.Collections.Generic.IEnumerable(Of T)'"
ms.date: 07/20/2015
f1_keywords:
- vbc32096
- bc32096
helpviewer_keywords:
- BC32096
ms.assetid: ed20d09c-913f-482e-89f8-c0a596c3ec24
ms.openlocfilehash: 0f19836efeabcf1d9e5097667c719c1f7d99cbbb
ms.sourcegitcommit: ff5a4eb5cffbcac9521bc44a907a118cd7e8638d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/17/2020
ms.locfileid: "92163461"
---
# <a name="bc32096-for-each-on-type-typename-is-ambiguous-because-the-type-implements-multiple-instantiations-of-systemcollectionsgenericienumerableof-t"></a>BC32096: ' for each ' no tipo ' \<typename> ' é ambíguo porque o tipo implementa várias instanciações de ' System. Collections. Generic. IEnumerable (Of T) '

Uma `For Each` instrução especifica uma variável de iterador que tem mais de um <xref:System.Collections.IEnumerable.GetEnumerator%2A> método.

 A variável de iterador deve ser de um tipo que implementa a <xref:System.Collections.IEnumerable?displayProperty=nameWithType> <xref:System.Collections.Generic.IEnumerable%601?displayProperty=nameWithType> interface ou em um dos `Collections` namespaces do .NET Framework. É possível que uma classe implemente mais de uma interface genérica construída, usando um argumento de tipo diferente para cada construção. Se uma classe que faz isso for usada para a variável de iterador, essa variável terá mais de um <xref:System.Collections.IEnumerable.GetEnumerator%2A> método. Nesse caso, Visual Basic não pode escolher qual método chamar.

 **ID do erro:** BC32096

## <a name="to-correct-this-error"></a>Para corrigir este erro

- Use o [Operador DirectCast](../operators/directcast-operator.md) ou o [Operador TryCast](../operators/trycast-operator.md) para converter o tipo de variável de iterador na interface que define o <xref:System.Collections.IEnumerable.GetEnumerator%2A> método que você deseja usar.

## <a name="see-also"></a>Veja também

- [Instrução For Each...Next](../statements/for-each-next-statement.md)
- [Interfaces](../../programming-guide/language-features/interfaces/index.md)
