---
title: Ferramentas do Azure para Visual Studio 2015
description: Obtenha as ferramentas para começar a usar as bibliotecas .NET do Azure no Visual Studio 2015.
ms.date: 10/19/2017
ms.custom: azure-sdk-dotnet
ms.openlocfilehash: a29709d56f2debe04d49ee4eafdc27acd4ca480f
ms.sourcegitcommit: 34dc3c0d0d0a1cc418abff259d9daa8078d00b81
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/19/2020
ms.locfileid: "82071923"
---
# <a name="azure-tools-for-visual-studio-2015"></a><span data-ttu-id="618a6-103">Ferramentas do Azure para Visual Studio 2015</span><span class="sxs-lookup"><span data-stu-id="618a6-103">Azure tools for Visual Studio 2015</span></span>

<span data-ttu-id="618a6-104">A maneira mais rápida e fácil de instalar o **SDK do Azure para Visual Studio 2015** e o **SDK do Service Fabric e Ferramentas para Visual Studio 2015** é usando o [Web Platform Installer](https://www.microsoft.com/web/downloads/platform.aspx).</span><span class="sxs-lookup"><span data-stu-id="618a6-104">The quickest and easiest way to install the **Azure SDK for Visual Studio 2015** and **Service Fabric SDK and Tools for Visual Studio 2015** is using the [Web Platform Installer](https://www.microsoft.com/web/downloads/platform.aspx).</span></span> <span data-ttu-id="618a6-105">O Microsoft Web Platform Installer é uma ferramenta gratuita que simplifica o download, a instalação e a atualização de alguns dos componentes do Microsoft Web Platform, incluindo as ferramentas do Azure para Visual Studio 2015.</span><span class="sxs-lookup"><span data-stu-id="618a6-105">The Microsoft Web Platform Installer is a free tool that streamlines downloading, installing, and updating some of the components of the Microsoft Web Platform, including Azure tools for Visual Studio 2015.</span></span> <span data-ttu-id="618a6-106">Esses SDKs também podem ser baixados e instalados como componentes individuais na [página Downloads do Azure](https://azure.microsoft.com/downloads/).</span><span class="sxs-lookup"><span data-stu-id="618a6-106">These SDKs can also be downloaded and installed as individual components from the [Azure Downloads page](https://azure.microsoft.com/downloads/).</span></span>

## <a name="using-the-web-platform-installer"></a><span data-ttu-id="618a6-107">Usando o Web Platform Installer</span><span class="sxs-lookup"><span data-stu-id="618a6-107">Using the Web Platform Installer</span></span>

1. <span data-ttu-id="618a6-108">Baixe e execute este [bootstrapper do Web Platform Installer](https://www.microsoft.com/web/handlers/webpi.ashx?command=getinstallerredirect&appid=VWDOrVs2015AzurePack;MicrosoftAzure-ServiceFabric-VS2015).</span><span class="sxs-lookup"><span data-stu-id="618a6-108">Download and run this [Web Platform Installer bootstrapper](https://www.microsoft.com/web/handlers/webpi.ashx?command=getinstallerredirect&appid=VWDOrVs2015AzurePack;MicrosoftAzure-ServiceFabric-VS2015).</span></span>

2. <span data-ttu-id="618a6-109">O bootstrapper instalará o Web Platform Installer (se necessário) e colocará automaticamente as últimas versões dos itens do **SDK do Azure para Visual Studio 2015** e do **SDK do Service Fabric e Ferramentas para Visual Studio 2015** na sua lista *Itens a serem instalados*.</span><span class="sxs-lookup"><span data-stu-id="618a6-109">The bootstrapper will install Web Platform Installer (if needed) and automatically put the latest versions of the  **Azure SDK for Visual Studio 2015** and **Service Fabric SDK and Tools for Visual Studio 2015** items in your *Items to be installed* list.</span></span> <span data-ttu-id="618a6-110">Clique em **Instalar**.</span><span class="sxs-lookup"><span data-stu-id="618a6-110">Click **Install**.</span></span>

    ![Web Platform Installer](../media/sdk/vs2015-install/webpi.png)

3. <span data-ttu-id="618a6-112">Na próxima tela, clique em **Aceito**.</span><span class="sxs-lookup"><span data-stu-id="618a6-112">On the next screen, click **I Accept**.</span></span> <span data-ttu-id="618a6-113">O Web PI começará a baixar e instalar os componentes selecionados.</span><span class="sxs-lookup"><span data-stu-id="618a6-113">Web PI will begin downloading and installing the components you selected.</span></span>

4. <span data-ttu-id="618a6-114">Depois que a instalação for concluída, ela exibirá uma tela de confirmação.</span><span class="sxs-lookup"><span data-stu-id="618a6-114">After the installation is finished, it will display a confirmation screen.</span></span> <span data-ttu-id="618a6-115">Clique em **Concluir**.</span><span class="sxs-lookup"><span data-stu-id="618a6-115">Click **Finish**.</span></span> <span data-ttu-id="618a6-116">Agora você pode fechar o Web Platform Installer.</span><span class="sxs-lookup"><span data-stu-id="618a6-116">You can now close Web Platform Installer.</span></span>

## <a name="verifying-the-installation"></a><span data-ttu-id="618a6-117">Verificando a instalação</span><span class="sxs-lookup"><span data-stu-id="618a6-117">Verifying the installation</span></span>

1. <span data-ttu-id="618a6-118">No Visual Studio 2015, clique no menu **Ferramentas** e clique em **Extensões e Atualizações...**.</span><span class="sxs-lookup"><span data-stu-id="618a6-118">In Visual Studio 2015, click the **Tools** menu, and then click **Extensions and Updates...**.</span></span>

2. <span data-ttu-id="618a6-119">A lista exibida conterá várias ferramentas do Azure, como **Ferramentas do Serviço de Aplicativo do Microsoft Azure**, **Serviço Conectado do Armazenamento do Microsoft Azure** e **Ferramentas do Service Fabric**.</span><span class="sxs-lookup"><span data-stu-id="618a6-119">The displayed list will contain several Azure tools, such as **Microsoft Azure App Service Tools**, **Microsoft Azure Storage Connected Service**, and **Service Fabric Tools**.</span></span>

    ![Extensões e atualizações](../media/sdk/vs2015-install/ext-tools.png)