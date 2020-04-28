---
title: Coleções e tipos de coleção para XAML
ms.date: 03/30/2017
ms.assetid: 58f8e7c6-9a41-4f25-8551-c042f1315baa
ms.openlocfilehash: 2ec58026c605df31489c8aab4c4cc714dab11474
ms.sourcegitcommit: de17a7a0a37042f0d4406f5ae5393531caeb25ba
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/24/2020
ms.locfileid: "82071293"
---
# <a name="collections-and-collection-types-for-xaml"></a><span data-ttu-id="a1351-102">Tipos de coletas e coleções para XAML</span><span class="sxs-lookup"><span data-stu-id="a1351-102">Collections and collection types for XAML</span></span>

<span data-ttu-id="a1351-103">Este artigo descreve como definir propriedades de tipos que se destinam a apoiar uma coleção e apoiar a sintaxe XAML para instanciar itens de coleta como elemento filho de um elemento de objeto pai ou elemento de propriedade.</span><span class="sxs-lookup"><span data-stu-id="a1351-103">This article describes how to define properties of types that are intended to support a collection, and to support the XAML syntax for instantiating collection items as element children of a parent object element or property element.</span></span>

## <a name="xaml-collection-concepts"></a><span data-ttu-id="a1351-104">Conceitos de Coleção XAML</span><span class="sxs-lookup"><span data-stu-id="a1351-104">XAML Collection Concepts</span></span>

<span data-ttu-id="a1351-105">Conceitualmente, qualquer relação no XAML onde há vários itens infantis dentro do escopo de um elemento objeto XAML ou elemento de propriedade XAML deve ser implementado como uma coleção.</span><span class="sxs-lookup"><span data-stu-id="a1351-105">Conceptually, any relationship in XAML where there are multiple child items within the scope of a XAML object element or XAML property element must be implemented as a collection.</span></span> <span data-ttu-id="a1351-106">Essa coleção deve estar associada a uma propriedade XAML específica do tipo XAML que é o pai nessa relação.</span><span class="sxs-lookup"><span data-stu-id="a1351-106">That collection must be associated with a particular XAML property of the XAML type that is the parent in that relationship.</span></span> <span data-ttu-id="a1351-107">A propriedade deve ser uma coleção porque um processador XAML espera atribuir cada item na marcação para ser um item recém-adicionado da propriedade de coleta de apoio.</span><span class="sxs-lookup"><span data-stu-id="a1351-107">The property must be a collection because a XAML processor expects to assign each item in markup to be a newly added item of the backing collection property.</span></span>

<span data-ttu-id="a1351-108">No nível de linguagem XAML, os requisitos exatos do suporte à coleta não são totalmente definidos.</span><span class="sxs-lookup"><span data-stu-id="a1351-108">At the XAML language level, the exact requirements of collection support are not fully defined.</span></span> <span data-ttu-id="a1351-109">O conceito de que uma coleção pode ser uma lista ou um dicionário (mas não ambos) é definido no nível de linguagem XAML, mas quais tipos de apoio representam listas ou dicionários não é definido pela língua XAML.</span><span class="sxs-lookup"><span data-stu-id="a1351-109">The concept that a collection can be either a list or a dictionary(but not both) is defined at the XAML language level, but which backing types represent either lists or dictionaries is not defined by the XAML language.</span></span>

<span data-ttu-id="a1351-110">Nos Serviços XAML .NET, o conceito de suporte à coleção XAML é mais claramente definido em termos de tipos de suporte .NET.</span><span class="sxs-lookup"><span data-stu-id="a1351-110">In .NET XAML Services, the concept of XAML collection support is more clearly defined in terms of .NET backing types.</span></span> <span data-ttu-id="a1351-111">Especificamente, o suporte xaml para coleções é baseado em vários conceitos e APIs .NET que são usados para listas e dicionários em programação geral .NET.</span><span class="sxs-lookup"><span data-stu-id="a1351-111">Specifically, the XAML support for collections is based on several .NET concepts and APIs that are used for lists and dictionaries in general .NET programming.</span></span>

1. <span data-ttu-id="a1351-112">A <xref:System.Collections.IList> interface indica uma coleção de listas.</span><span class="sxs-lookup"><span data-stu-id="a1351-112">The <xref:System.Collections.IList> interface indicates a list collection.</span></span>

2. <span data-ttu-id="a1351-113">A <xref:System.Collections.IDictionary> interface indica uma coleção de dicionários.</span><span class="sxs-lookup"><span data-stu-id="a1351-113">The <xref:System.Collections.IDictionary> interface indicates a dictionary collection.</span></span>

3. <span data-ttu-id="a1351-114"><xref:System.Array>representa uma matriz, e uma <xref:System.Collections.IList> matriz suporta métodos.</span><span class="sxs-lookup"><span data-stu-id="a1351-114"><xref:System.Array> represents an array, and an array supports <xref:System.Collections.IList> methods.</span></span>

<span data-ttu-id="a1351-115">Em cada um desses conceitos de coleção, um processador .NET `Add` XAML Services XAML espera chamar o método em uma instância específica do tipo de propriedade de coleção.</span><span class="sxs-lookup"><span data-stu-id="a1351-115">In each of these collection concepts, a .NET XAML Services XAML processor expects to call the `Add` method on a specific instance of the collection property's type.</span></span> <span data-ttu-id="a1351-116">Ou, em um cenário de serialização, um processador XAML produz instâncias discretas do tipo XAML para cada item encontrado na lista, dicionário ou matriz com base no conceito específico de "Itens" de cada coleção.</span><span class="sxs-lookup"><span data-stu-id="a1351-116">Or, in a serialization scenario, a XAML processor produces discrete XAML-type instances for each item found in the list, dictionary, or array based on each collection's specific concept of "Items".</span></span> <span data-ttu-id="a1351-117">Estes itens são: <xref:System.Collections.IList.Item%2A?displayProperty=nameWithType>; <xref:System.Collections.IDictionary.Item%2A?displayProperty=nameWithType>; o <xref:System.Array.System%23Collections%23IList%23Item%2A?displayProperty=nameWithType> explícito <xref:System.Array>para .</span><span class="sxs-lookup"><span data-stu-id="a1351-117">These items are: <xref:System.Collections.IList.Item%2A?displayProperty=nameWithType>; <xref:System.Collections.IDictionary.Item%2A?displayProperty=nameWithType>; the explicit <xref:System.Array.System%23Collections%23IList%23Item%2A?displayProperty=nameWithType> for <xref:System.Array>.</span></span>

## <a name="generic-collections"></a><span data-ttu-id="a1351-118">Coleções Genéricas</span><span class="sxs-lookup"><span data-stu-id="a1351-118">Generic Collections</span></span>

<span data-ttu-id="a1351-119">Coleções genéricas podem ser úteis para programação geral .NET, e também podem ser usadas para propriedades de coleção XAML.</span><span class="sxs-lookup"><span data-stu-id="a1351-119">Generic collections can be useful for general .NET programming, and can also be used for XAML collection properties.</span></span> <span data-ttu-id="a1351-120">No entanto, <xref:System.Collections.Generic.IList%601> as <xref:System.Collections.Generic.IDictionary%602> interfaces genéricas e não são identificadas pelos processadores XAML Services .NET como sendo equivalentes aos não genéricos <xref:System.Collections.IList> ou <xref:System.Collections.IDictionary>.</span><span class="sxs-lookup"><span data-stu-id="a1351-120">However, the generic interfaces <xref:System.Collections.Generic.IList%601> and <xref:System.Collections.Generic.IDictionary%602> are not identified by .NET XAML Services XAML processors as being equivalent to the non-generic <xref:System.Collections.IList> or <xref:System.Collections.IDictionary>.</span></span> <span data-ttu-id="a1351-121">Em vez de implementar as interfaces, uma abordagem recomendada para <xref:System.Collections.Generic.List%601> tipos <xref:System.Collections.Generic.Dictionary%602>de propriedade de coleta genérica é derivar das classes ou .</span><span class="sxs-lookup"><span data-stu-id="a1351-121">Rather than implementing the interfaces, a recommended approach for generic collection property types is to derive from the classes <xref:System.Collections.Generic.List%601> or <xref:System.Collections.Generic.Dictionary%602>.</span></span> <span data-ttu-id="a1351-122">Essas classes implementam as interfaces não genéricas e, portanto, incluem o suporte esperado para coleções XAML na implementação base.</span><span class="sxs-lookup"><span data-stu-id="a1351-122">These classes implement the non-generic interfaces and thus include the expected support for XAML collections in the base implementation.</span></span>

## <a name="read-only-collections-and-initialization-logic"></a><span data-ttu-id="a1351-123">Coleções somente leitura e lógica de inicialização</span><span class="sxs-lookup"><span data-stu-id="a1351-123">Read-Only Collections and Initialization Logic</span></span>

<span data-ttu-id="a1351-124">Na programação .NET, é um padrão de design comum fazer qualquer propriedade que detenha um valor de uma coleção como uma coleção somente leitura.</span><span class="sxs-lookup"><span data-stu-id="a1351-124">In .NET programming, it is a common design pattern to make any property that holds a value of a collection as a read-only collection.</span></span> <span data-ttu-id="a1351-125">Esse padrão permite que o caso que possui a propriedade de cobrança controle melhor o que acontece com a coleção..</span><span class="sxs-lookup"><span data-stu-id="a1351-125">This pattern permits the instance that owns the collection property to better control what happens to the collection..</span></span> <span data-ttu-id="a1351-126">Especificamente, o padrão impede a substituição acidental de toda a coleção pré-existente, definindo a propriedade.</span><span class="sxs-lookup"><span data-stu-id="a1351-126">Specifically, the pattern prevents accidental replacement of the entire pre-existing collection by setting the property.</span></span> <span data-ttu-id="a1351-127">Neste padrão, qualquer acesso à coleção por chamadores deve ser feito por métodos de chamada ou propriedades suportadas pelo tipo de coleta e/ou pelas interfaces de coleta relevantes, tais como <xref:System.Collections.IList>.</span><span class="sxs-lookup"><span data-stu-id="a1351-127">In this pattern, any access to the collection by callers should instead be made by calling methods or properties as supported by the collection type and/or the relevant collection interfaces such as <xref:System.Collections.IList>.</span></span>

<span data-ttu-id="a1351-128">O uso deste padrão implica que qualquer classe que exponha uma propriedade de coleção somente leitura deve primeiro inicializar essa propriedade para manter uma coleção vazia.</span><span class="sxs-lookup"><span data-stu-id="a1351-128">Using this pattern implies that any class that exposes a read-only collection property must first initialize that property to hold an empty collection.</span></span> <span data-ttu-id="a1351-129">Normalmente, a inicialização é realizada como parte do comportamento de construção da classe.</span><span class="sxs-lookup"><span data-stu-id="a1351-129">Typically the initialization is performed as part of the construction behavior for the class.</span></span> <span data-ttu-id="a1351-130">Para ser útil para xaml, é importante que tal lógica seja sempre referenciada pelo construtor sem parâmetros, pois xAML geralmente chama o construtor sem parâmetros antes de processar as propriedades (propriedades de coleta ou não).</span><span class="sxs-lookup"><span data-stu-id="a1351-130">To be useful for XAML, it is important that such logic is always referenced by the parameterless constructor, because XAML generally calls the parameterless constructor prior to processing the properties (collection properties or otherwise).</span></span>

## <a name="xaml-type-system-support-and-collections"></a><span data-ttu-id="a1351-131">Suporte e coleções do sistema do tipo XAML</span><span class="sxs-lookup"><span data-stu-id="a1351-131">XAML Type System Support and Collections</span></span>

<span data-ttu-id="a1351-132">Além da mecânica básica de analisar XAML e preencher ou serializar propriedades de coleção, o sistema tipo XAML implementado no .NET XAML Services inclui vários recursos de design que pertencem às coleções em XAML.</span><span class="sxs-lookup"><span data-stu-id="a1351-132">Beyond the basic mechanics of parsing XAML and populating or serializing collection properties, the XAML type system as implemented in .NET XAML Services includes several design features that pertain to collections in XAML.</span></span>

1. <span data-ttu-id="a1351-133"><xref:System.Xaml.XamlType.IsCollection%2A>retorna verdadeiro se o tipo XAML for suportado por um tipo que fornece suporte à coleção XAML.</span><span class="sxs-lookup"><span data-stu-id="a1351-133"><xref:System.Xaml.XamlType.IsCollection%2A> returns true if the XAML type is backed by a type that provides XAML collection support.</span></span>

2. <span data-ttu-id="a1351-134"><xref:System.Xaml.XamlType.IsDictionary%2A>e <xref:System.Xaml.XamlType.IsArray%2A> pode identificar ainda qual modo de coleta o tipo XAML suporta.</span><span class="sxs-lookup"><span data-stu-id="a1351-134"><xref:System.Xaml.XamlType.IsDictionary%2A> and <xref:System.Xaml.XamlType.IsArray%2A> can further identify which collection mode the XAML type supports.</span></span> <span data-ttu-id="a1351-135">Para processadores XAML personalizados que são baseados em Serviços XAML .NET <xref:System.Xaml.XamlWriter> e no sistema do tipo XAML, mas não com base nas implementações existentes, saber qual modo de coleta é usado pode ser necessário para saber qual método invocar para o processamento de coleta.</span><span class="sxs-lookup"><span data-stu-id="a1351-135">For custom XAML processors that are based on .NET XAML Services and the XAML type system but not based on existing <xref:System.Xaml.XamlWriter> implementations, knowing which collection mode is used might be necessary in order to know which method to invoke for collection processing.</span></span>

3. <span data-ttu-id="a1351-136">Cada um dos valores de propriedade anteriores é potencialmente influenciado por substituições de <xref:System.Xaml.XamlType.LookupCollectionKind%2A> um tipo XAML.</span><span class="sxs-lookup"><span data-stu-id="a1351-136">Each of the previous property values is potentially influenced by overrides of <xref:System.Xaml.XamlType.LookupCollectionKind%2A> on a XAML type.</span></span>