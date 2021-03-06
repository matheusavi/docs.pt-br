---
title: Converter cadeias de caracteres em tipos
description: Entenda a análise da cadeia de caracteres no .NET. A análise converte uma cadeia de caracteres que representa um tipo base .NET nesse tipo base. A análise é a operação inversa para formatação.
ms.date: 03/30/2017
helpviewer_keywords:
- parsing strings, about parsing strings
- IFormatProvider interface, parsing strings
- base types, parsing strings
- Parse method
- parsing strings
ms.assetid: 5e758b41-db93-456b-8999-99b7304b090d
ms.openlocfilehash: 8fbfe8596e49ed101ea7d6bb65298e432a6fac13
ms.sourcegitcommit: 965a5af7918acb0a3fd3baf342e15d511ef75188
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/18/2020
ms.locfileid: "94821899"
---
# <a name="parse-strings-in-net"></a>Analisar cadeias de caracteres no .NET

Uma operação de *análise* converte uma cadeia de caracteres que representa um tipo de base .net nesse tipo base. Por exemplo, uma operação de análise é usada para converter uma cadeia de caracteres em um número de ponto flutuante ou em um valor de data e hora. O método usado com mais frequência para executar uma operação de análise é o método `Parse`. Como a análise é a operação inversa da formatação (que envolve a conversão de um tipo base em sua representação de cadeia de caracteres), muitas das mesmas regras e convenções se aplicam. Assim como a formatação usa um objeto que implementa a interface <xref:System.IFormatProvider> para fornecer informações de formatação que diferenciam a cultura, a análise também usa um objeto que implementa a interface <xref:System.IFormatProvider> para determinar como interpretar uma representação de cadeia de caracteres. Para obter mais informações, consulte [tipos de formato](formatting-types.md).

## <a name="in-this-section"></a>Nesta seção
 [Analisando cadeias de caracteres numéricas](parsing-numeric.md)\
 Descreve como converter cadeias de caracteres em tipos numéricos do .NET.

 [Cadeias de caracteres de data e hora de análise](parsing-datetime.md)\
 Descreve como converter cadeias de caracteres em tipos **DateTime** do .NET.

 [Analisando outras cadeias de caracteres](parsing-other.md)\
 Descreve como converter cadeias de caracteres em tipos **Char**, **Boolean** e **Enum**.

## <a name="related-sections"></a>Seções relacionadas
 [Tipos de formatação](formatting-types.md)\
 Descreve conceitos básicos de formatação, como especificadores de formato e provedores de formato.

 [Conversão de tipo no .NET](type-conversion.md)\
 Descreve como converter tipos.
