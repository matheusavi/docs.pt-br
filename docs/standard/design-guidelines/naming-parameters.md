---
title: Parâmetros de nomeação
description: Aprenda as diretrizes para a nomenclatura de parâmetros. Por exemplo, use nomes de parâmetros descritivos & o camel case, & considere a nomenclatura com base no significado, em vez do tipo.
ms.date: 10/22/2008
helpviewer_keywords:
- parameters, names
- names [.NET Framework], parameters
ms.assetid: ca3c956e-725a-441b-b4e3-eab5d472f41c
ms.openlocfilehash: b62cfbd58f671745054c557041e5d60af345c8d3
ms.sourcegitcommit: 965a5af7918acb0a3fd3baf342e15d511ef75188
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/18/2020
ms.locfileid: "94820833"
---
# <a name="naming-parameters"></a>Parâmetros de nomeação
Além do motivo óbvio da legibilidade, é importante seguir as diretrizes para nomes de parâmetro, pois os parâmetros são exibidos na documentação e no designer quando as ferramentas de Design Visual fornecem funcionalidade de navegação de classe e IntelliSense.

 ✔️ usar camelCasing em nomes de parâmetro.

 ✔️ usar nomes de parâmetro descritivos.

 ✔️ CONSIDERAR o uso de nomes com base no significado de um parâmetro em vez do tipo do parâmetro.

### <a name="naming-operator-overload-parameters"></a>Parâmetros de sobrecarga de operador de nomenclatura
 ✔️ usar `left` e `right` para nomes de parâmetros de sobrecarga de operador binário se não houver significado para os parâmetros.

 ✔️ usar `value` para nomes de parâmetro de sobrecarga de operador unário se não houver significado para os parâmetros.

 ✔️ CONSIDERAR nomes significativos para parâmetros de sobrecarga de operador se isso adicionar um valor significativo.

 ❌ Não use abreviações ou índices numéricos para nomes de parâmetro de sobrecarga de operador.

 *Partes © 2005, 2009 Microsoft Corporation. Todos os direitos reservados.*

 *Reimpresso com permissão da Pearson Education, Inc. das [Diretrizes de Design do Framework: convenções, linguagens e padrões para bibliotecas do .NET reutilizável, 2ª edição](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) por Krzysztof Cwalina e Brad Abrams, publicado em 22 de outubro de 2008 por Addison-Wesley Professional como parte da série de desenvolvimento do Microsoft Windows.*

## <a name="see-also"></a>Confira também

- [Diretrizes de design de estrutura](index.md)
- [Diretrizes de nomenclatura](naming-guidelines.md)
