---
title: Instalar o .NET Core no CentOS-.NET Core
description: Demonstra as várias maneiras de instalar o SDK do .NET Core e o tempo de execução do .NET Core no CentOS.
author: thraka
ms.author: adegeo
ms.date: 06/04/2020
ms.openlocfilehash: 743bd4ce47fdecef512f9605d8ec5503eb6da9ba
ms.sourcegitcommit: cdb295dd1db589ce5169ac9ff096f01fd0c2da9d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/09/2020
ms.locfileid: "84603135"
---
# <a name="install-net-core-sdk-or-net-core-runtime-on-centos"></a><span data-ttu-id="43d0d-103">Instalar o SDK do .NET Core ou o tempo de execução do .NET Core no CentOS</span><span class="sxs-lookup"><span data-stu-id="43d0d-103">Install .NET Core SDK or .NET Core Runtime on CentOS</span></span>

<span data-ttu-id="43d0d-104">O .NET Core tem suporte no CentOS.</span><span class="sxs-lookup"><span data-stu-id="43d0d-104">.NET Core is supported on CentOS.</span></span> <span data-ttu-id="43d0d-105">Este artigo descreve como instalar o .NET Core no CentOS.</span><span class="sxs-lookup"><span data-stu-id="43d0d-105">This article describes how to install .NET Core on CentOS.</span></span>

[!INCLUDE [linux-intro-sdk-vs-runtime](includes/linux-intro-sdk-vs-runtime.md)]

[!INCLUDE [linux-install-package-manager-x64-vs-arm](includes/linux-install-package-manager-x64-vs-arm.md)]

## <a name="supported-distributions"></a><span data-ttu-id="43d0d-106">Distribuições com suporte</span><span class="sxs-lookup"><span data-stu-id="43d0d-106">Supported distributions</span></span>

<span data-ttu-id="43d0d-107">A tabela a seguir é uma lista de versões do .NET Core com suporte atualmente no CentOS 7 e no CentOS 8.</span><span class="sxs-lookup"><span data-stu-id="43d0d-107">The following table is a list of currently supported .NET Core releases on both CentOS 7 and CentOS 8.</span></span> <span data-ttu-id="43d0d-108">Essas versões permanecem com suporte até que a versão do [.NET Core atinja o fim do suporte](https://dotnet.microsoft.com/platform/support/policy/dotnet-core) ou a versão do CentOS não seja mais suportada.</span><span class="sxs-lookup"><span data-stu-id="43d0d-108">These versions remain supported until either the version of [.NET Core reaches end-of-support](https://dotnet.microsoft.com/platform/support/policy/dotnet-core) or the version of CentOS is no longer supported.</span></span>

- <span data-ttu-id="43d0d-109">Um ✔️ indica que a versão do CentOS ou do .NET Core ainda tem suporte.</span><span class="sxs-lookup"><span data-stu-id="43d0d-109">A ✔️ indicates that the version of CentOS or .NET Core is still supported.</span></span>
- <span data-ttu-id="43d0d-110">Um ❌ indica que a versão do CentOS ou do .NET Core não tem suporte nessa versão do CentOS.</span><span class="sxs-lookup"><span data-stu-id="43d0d-110">A ❌ indicates that the version of CentOS or .NET Core isn't supported on that CentOS release.</span></span>
- <span data-ttu-id="43d0d-111">Quando uma versão do CentOS e uma versão do .NET Core têm ✔️, há suporte para essa combinação de so e .NET.</span><span class="sxs-lookup"><span data-stu-id="43d0d-111">When both a version of CentOS and a version of .NET Core have ✔️, that OS and .NET combination are supported.</span></span>

| <span data-ttu-id="43d0d-112">CentOS</span><span class="sxs-lookup"><span data-stu-id="43d0d-112">CentOS</span></span>                   | <span data-ttu-id="43d0d-113">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="43d0d-113">.NET Core 2.1</span></span> | <span data-ttu-id="43d0d-114">.NET Core 3.1</span><span class="sxs-lookup"><span data-stu-id="43d0d-114">.NET Core 3.1</span></span> | <span data-ttu-id="43d0d-115">Versão prévia do .NET 5 (somente instalação manual)</span><span class="sxs-lookup"><span data-stu-id="43d0d-115">.NET 5 Preview (manual install only)</span></span> |
|--------------------------|---------------|---------------|----------------|
| <span data-ttu-id="43d0d-116">✔️ [8](#centos-8-)</span><span class="sxs-lookup"><span data-stu-id="43d0d-116">✔️ [8](#centos-8-)</span></span> | <span data-ttu-id="43d0d-117">✔️ 2,1</span><span class="sxs-lookup"><span data-stu-id="43d0d-117">✔️ 2.1</span></span>        | <span data-ttu-id="43d0d-118">✔️ 3,1</span><span class="sxs-lookup"><span data-stu-id="43d0d-118">✔️ 3.1</span></span>        | <span data-ttu-id="43d0d-119">versão prévia do ✔️ 5,0</span><span class="sxs-lookup"><span data-stu-id="43d0d-119">✔️ 5.0 Preview</span></span> |
| <span data-ttu-id="43d0d-120">✔️ [7](#centos-7-)</span><span class="sxs-lookup"><span data-stu-id="43d0d-120">✔️ [7](#centos-7-)</span></span> | <span data-ttu-id="43d0d-121">✔️ 2,1</span><span class="sxs-lookup"><span data-stu-id="43d0d-121">✔️ 2.1</span></span>        | <span data-ttu-id="43d0d-122">✔️ 3,1</span><span class="sxs-lookup"><span data-stu-id="43d0d-122">✔️ 3.1</span></span>        | <span data-ttu-id="43d0d-123">versão prévia do ✔️ 5,0</span><span class="sxs-lookup"><span data-stu-id="43d0d-123">✔️ 5.0 Preview</span></span> |

<span data-ttu-id="43d0d-124">Não há mais suporte para as seguintes versões do .NET Core.</span><span class="sxs-lookup"><span data-stu-id="43d0d-124">The following versions of .NET Core are no longer supported.</span></span> <span data-ttu-id="43d0d-125">Os downloads para eles ainda permanecem publicados:</span><span class="sxs-lookup"><span data-stu-id="43d0d-125">The downloads for these still remain published:</span></span>

- <span data-ttu-id="43d0d-126">3.0</span><span class="sxs-lookup"><span data-stu-id="43d0d-126">3.0</span></span>
- <span data-ttu-id="43d0d-127">2.2</span><span class="sxs-lookup"><span data-stu-id="43d0d-127">2.2</span></span>
- <span data-ttu-id="43d0d-128">2,0</span><span class="sxs-lookup"><span data-stu-id="43d0d-128">2.0</span></span>

[!INCLUDE [linux-install-package-manager-x64-vs-arm](includes/linux-install-package-manager-x64-vs-arm.md)]

## <a name="how-to-install-other-versions"></a><span data-ttu-id="43d0d-129">Como instalar outras versões</span><span class="sxs-lookup"><span data-stu-id="43d0d-129">How to install other versions</span></span>

[!INCLUDE [package-manager-switcher](./includes/package-manager-heading-hack-pkgname.md)]

## <a name="centos-8-"></a><span data-ttu-id="43d0d-130">CentOS 8 ✔️</span><span class="sxs-lookup"><span data-stu-id="43d0d-130">CentOS 8 ✔️</span></span>

<span data-ttu-id="43d0d-131">O .NET Core 3,1 está disponível nos repositórios de pacotes padrão do CentOS 8.</span><span class="sxs-lookup"><span data-stu-id="43d0d-131">.NET Core 3.1 is available in the default package repositories for CentOS 8.</span></span>

[!INCLUDE [linux-dnf-install-31](includes/linux-install-31-dnf.md)]

## <a name="centos-7-"></a><span data-ttu-id="43d0d-132">CentOS 7 ✔️</span><span class="sxs-lookup"><span data-stu-id="43d0d-132">CentOS 7 ✔️</span></span>

[!INCLUDE [linux-prep-intro-generic](includes/linux-prep-intro-generic.md)]

```bash
sudo rpm -Uvh https://packages.microsoft.com/config/centos/7/packages-microsoft-prod.rpm
```

[!INCLUDE [linux-yum-install-31](includes/linux-install-31-yum.md)]

## <a name="troubleshoot-the-package-manager"></a><span data-ttu-id="43d0d-133">Solucionar problemas do Gerenciador de pacotes</span><span class="sxs-lookup"><span data-stu-id="43d0d-133">Troubleshoot the package manager</span></span>

<span data-ttu-id="43d0d-134">Esta seção fornece informações sobre erros comuns que você pode obter ao usar o Gerenciador de pacotes para instalar o .NET Core.</span><span class="sxs-lookup"><span data-stu-id="43d0d-134">This section provides information on common errors you may get while using the package manager to install .NET Core.</span></span>

### <a name="failed-to-fetch"></a><span data-ttu-id="43d0d-135">Falha ao buscar</span><span class="sxs-lookup"><span data-stu-id="43d0d-135">Failed to fetch</span></span>

[!INCLUDE [package-manager-failed-to-fetch-rpm](includes/package-manager-failed-to-fetch-rpm.md)]

## <a name="snap"></a><span data-ttu-id="43d0d-136">Snap</span><span class="sxs-lookup"><span data-stu-id="43d0d-136">Snap</span></span>

[!INCLUDE [linux-install-snap](includes/linux-install-snap.md)]

## <a name="dependencies"></a><span data-ttu-id="43d0d-137">Dependências</span><span class="sxs-lookup"><span data-stu-id="43d0d-137">Dependencies</span></span>

[!INCLUDE [linux-install-dependencies](includes/linux-install-dependencies.md)]

## <a name="scripted-install"></a><span data-ttu-id="43d0d-138">Instalação com script</span><span class="sxs-lookup"><span data-stu-id="43d0d-138">Scripted install</span></span>

[!INCLUDE [linux-install-scripted](includes/linux-install-scripted.md)]

## <a name="manual-install"></a><span data-ttu-id="43d0d-139">Instalação manual</span><span class="sxs-lookup"><span data-stu-id="43d0d-139">Manual install</span></span>

[!INCLUDE [linux-install-manual](includes/linux-install-manual.md)]

## <a name="next-steps"></a><span data-ttu-id="43d0d-140">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="43d0d-140">Next steps</span></span>

- [<span data-ttu-id="43d0d-141">Tutorial: criar um aplicativo de console com SDK do .NET Core usando Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="43d0d-141">Tutorial: Create a console application with .NET Core SDK using Visual Studio Code</span></span>](../tutorials/with-visual-studio-code.md)