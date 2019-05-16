---
title: Comentários de documentação XML – Guia de Programação em C#
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- cs.xml
helpviewer_keywords:
- XML [C#], code comments
- comments [C#], XML
- documentation comments [C#]
- C# source code files
- C# language, XML code comments
- XML documentation comments [C#]
ms.assetid: 803b7f7b-7428-4725-b5db-9a6cff273199
ms.openlocfilehash: 85d75d6420404f278c4a8b16eb9bf30aff958f7c
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65645774"
---
# <a name="xml-documentation-comments-c-programming-guide"></a><span data-ttu-id="7df08-102">Comentários de documentação XML (Guia de Programação em C#)</span><span class="sxs-lookup"><span data-stu-id="7df08-102">XML Documentation Comments (C# Programming Guide)</span></span>
<span data-ttu-id="7df08-103">No Visual C#, você pode criar documentação para seu código ao incluir elementos XML nos campos de comentários especiais (indicados por barras triplas) no código-fonte logo antes do bloco de código ao qual os comentários se referem, por exemplo:</span><span class="sxs-lookup"><span data-stu-id="7df08-103">In Visual C# you can create documentation for your code by including XML elements in special comment fields (indicated by triple slashes) in the source code directly before the code block to which the comments refer, for example:</span></span>  
  
```csharp  
/// <summary>  
///  This class performs an important function.  
/// </summary>  
public class MyClass {}  
```  
  
 <span data-ttu-id="7df08-104">Ao compilar com a opção [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md), o compilador pesquisará todas as marcas XML no código-fonte e criará um arquivo de documentação XML.</span><span class="sxs-lookup"><span data-stu-id="7df08-104">When you compile with the [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) option, the compiler will search for all XML tags in the source code and create an XML documentation file.</span></span> <span data-ttu-id="7df08-105">Para criar a documentação final com base no arquivo gerado pelo compilador, crie uma ferramenta personalizada ou use uma ferramenta como o [DocFX](https://dotnet.github.io/docfx/) ou o [Sandcastle](https://github.com/EWSoftware/SHFB).</span><span class="sxs-lookup"><span data-stu-id="7df08-105">To create the final documentation based on the compiler-generated file, you can create a custom tool or use a tool such as [DocFX](https://dotnet.github.io/docfx/) or [Sandcastle](https://github.com/EWSoftware/SHFB).</span></span>  
  
 <span data-ttu-id="7df08-106">Para consultar elementos XML (por exemplo, sua função processa elementos XML específicos que você deseja descrever em um comentário da documentação XML), você pode usar o mecanismo de citação padrão (`<` e `>`).</span><span class="sxs-lookup"><span data-stu-id="7df08-106">To refer to XML elements (for example, your function processes specific XML elements that you want to describe in an XML documentation comment), you can use the standard quoting mechanism (`<` and `>`).</span></span>  <span data-ttu-id="7df08-107">Para consultar identificadores genéricos em elementos de referência de código (`cref`), você pode usar os caracteres de escape (por exemplo, `cref="List&lt;T&gt;"`) ou chaves (`cref="List{T}"`).</span><span class="sxs-lookup"><span data-stu-id="7df08-107">To refer to generic identifiers in code reference (`cref`) elements, you can use either the escape characters (for example, `cref="List&lt;T&gt;"`) or braces (`cref="List{T}"`).</span></span>  <span data-ttu-id="7df08-108">Como um caso especial, o compilador analisa as chaves como colchetes angulares para tornar o comentário da documentação menos incômodo para o autor ao fazer referência a identificadores genéricos.</span><span class="sxs-lookup"><span data-stu-id="7df08-108">As a special case, the compiler parses the braces as angle brackets to make the documentation comment less cumbersome to author when referring to generic identifiers.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="7df08-109">Os comentários da documentação XML não são metadados; eles não estão incluídos no assembly compilado e, portanto, não são acessíveis através de reflexão.</span><span class="sxs-lookup"><span data-stu-id="7df08-109">The XML documentation comments are not metadata; they are not included in the compiled assembly and therefore they are not accessible through reflection.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="7df08-110">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="7df08-110">In This Section</span></span>  
  
- [<span data-ttu-id="7df08-111">Marcas recomendadas para comentários de documentação</span><span class="sxs-lookup"><span data-stu-id="7df08-111">Recommended Tags for Documentation Comments</span></span>](../../../csharp/programming-guide/xmldoc/recommended-tags-for-documentation-comments.md)  
  
- [<span data-ttu-id="7df08-112">Processando o Arquivo XML</span><span class="sxs-lookup"><span data-stu-id="7df08-112">Processing the XML File</span></span>](../../../csharp/programming-guide/xmldoc/processing-the-xml-file.md)  
  
- [<span data-ttu-id="7df08-113">Delimitadores para marcas de documentação</span><span class="sxs-lookup"><span data-stu-id="7df08-113">Delimiters for Documentation Tags</span></span>](../../../csharp/programming-guide/xmldoc/delimiters-for-documentation-tags.md)  
  
- [<span data-ttu-id="7df08-114">Como: usar as funcionalidades da documentação XML</span><span class="sxs-lookup"><span data-stu-id="7df08-114">How to: Use the XML Documentation Features</span></span>](../../../csharp/programming-guide/xmldoc/how-to-use-the-xml-documentation-features.md)  
  
## <a name="related-sections"></a><span data-ttu-id="7df08-115">Seções relacionadas</span><span class="sxs-lookup"><span data-stu-id="7df08-115">Related Sections</span></span>  
 <span data-ttu-id="7df08-116">Para obter mais informações, consulte:</span><span class="sxs-lookup"><span data-stu-id="7df08-116">For more information, see:</span></span>  
  
- [<span data-ttu-id="7df08-117">/doc (comentários da documentação de processos)</span><span class="sxs-lookup"><span data-stu-id="7df08-117">/doc (Process Documentation Comments)</span></span>](../../../csharp/language-reference/compiler-options/doc-compiler-option.md)  
  
## <a name="c-language-specification"></a><span data-ttu-id="7df08-118">Especificação da Linguagem C#</span><span class="sxs-lookup"><span data-stu-id="7df08-118">C# Language Specification</span></span>  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="7df08-119">Consulte também</span><span class="sxs-lookup"><span data-stu-id="7df08-119">See also</span></span>

- [<span data-ttu-id="7df08-120">Guia de Programação em C#</span><span class="sxs-lookup"><span data-stu-id="7df08-120">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)