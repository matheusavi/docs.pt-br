---
title: Membros protegidos
ms.date: 10/22/2008
helpviewer_keywords:
- members [.NET Framework], protected
- protected members
- classes [.NET Framework], unsealed
- classes [.NET Framework], protected members
- unsealed classes
- customizing class behavior
ms.assetid: aa0b58ee-3956-494d-ab48-471ae5db8740
ms.openlocfilehash: 3cc2ab3e605cfb5382f107dead0c95495858fc6b
ms.sourcegitcommit: 965a5af7918acb0a3fd3baf342e15d511ef75188
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/18/2020
ms.locfileid: "94828719"
---
# <a name="protected-members"></a>Membros protegidos
Os membros protegidos por si só não fornecem nenhuma extensibilidade, mas podem tornar a extensibilidade por meio de subclasses mais poderosas. Eles podem ser usados para expor opções de personalização avançadas sem desnecessariamente complicar a interface pública principal.

 Os designers de estrutura precisam ter cuidado com membros protegidos porque o nome "protegido" pode dar um falso aspecto de segurança. Qualquer pessoa pode fazer uma subclasse de uma classe sem lacre e acessar membros protegidos e, portanto, todas as mesmas práticas de codificação defensivas usadas para membros públicos se aplicam a membros protegidos.

 ✔️ Considere o uso de membros protegidos para personalização avançada.

 ✔️ tratar membros protegidos em classes sem lacre como públicas para fins de segurança, documentação e análise de compatibilidade.

 Qualquer pessoa pode herdar de uma classe e acessar os membros protegidos.

 *Partes © 2005, 2009 Microsoft Corporation. Todos os direitos reservados.*

 *Reimpresso com permissão da Pearson Education, Inc. das [Diretrizes de Design do Framework: convenções, linguagens e padrões para bibliotecas do .NET reutilizável, 2ª edição](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) por Krzysztof Cwalina e Brad Abrams, publicado em 22 de outubro de 2008 por Addison-Wesley Professional como parte da série de desenvolvimento do Microsoft Windows.*

## <a name="see-also"></a>Confira também

- [Diretrizes de design de estrutura](index.md)
- [Designer voltado para extensibilidade](designing-for-extensibility.md)
