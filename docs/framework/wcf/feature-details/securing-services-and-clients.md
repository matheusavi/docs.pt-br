---
title: Protegendo serviços e clientes
ms.date: 03/30/2017
helpviewer_keywords:
- message security [WCF]
ms.assetid: e681f3bd-0c09-4a58-b0e4-0ecbdf1aa6c7
ms.openlocfilehash: 713737b129771967958fddf44e9ef28583d49422
ms.sourcegitcommit: 27a15a55019f6b5f2733961738babe94aec0def3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/15/2020
ms.locfileid: "90554072"
---
# <a name="securing-services-and-clients"></a>Protegendo serviços e clientes
As informações contidas nesta seção concentram-se na segurança de programação no Windows Communication Foundation (WCF). Em geral, isso inclui a seleção de uma associação apropriada fornecida pelo sistema, a definição das propriedades do elemento de segurança e a configuração das propriedades dos comportamentos de serviço que regem o modo como as credenciais são recuperadas para uso pelo serviço ou pelo cliente. Essas técnicas abrangem os requisitos de segurança da maioria dos usuários para a maioria dos cenários, conforme mostrado em [cenários de segurança comuns](common-security-scenarios.md). Se seu cenário exigir mais recursos, primeiro consulte [recursos de segurança com associações personalizadas](security-capabilities-with-custom-bindings.md); se uma solução não for aparente, consulte [estendendo a segurança](../extending/extending-security.md). Se você estiver criando (ou Interoperando com) um sistema que usa declarações avançadas, consulte os tópicos em [autorização](authorization-in-wcf.md).  
  
## <a name="in-this-section"></a>Nesta seção  
 [Programação de segurança do WCF](programming-wcf-security.md)  
 Uma visão geral do modelo de programação usado para proteger mensagens.  
  
 [Visão geral de segurança de transporte](transport-security-overview.md)  
 Uma visão geral de como proteger mensagens por meio da camada de transporte.  
  
 [Segurança de mensagem](message-security-in-wcf.md)  
 Resume os motivos para usar a segurança em nível de mensagem no Windows Communication Foundation (WCF).  
  
 [Sessões seguras](secure-sessions.md)  
 Uma discussão sobre as considerações necessárias ao proteger uma sessão do WCF.  
  
 [Trabalhando com certificados](working-with-certificates.md)  
 Uma explicação de algumas das tarefas comuns necessárias ao usar certificados X. 509.  
  
## <a name="reference"></a>Referência  
 <xref:System.ServiceModel>  
  
 <xref:System.ServiceModel.Channels>  
  
 <xref:System.ServiceModel.Security>  
  
## <a name="related-sections"></a>Seções relacionadas  
 [Conceitos de segurança](security-concepts.md)  
  
 [Segurança estendida](../extending/extending-security.md)  
  
 [Cenários comuns de segurança](common-security-scenarios.md)  
  
 [Associações e segurança](bindings-and-security.md)  
  
 [Recursos de segurança com associações personalizadas](security-capabilities-with-custom-bindings.md)  
  
 [Segurança estendida](../extending/extending-security.md)  
  
 [Autorização](authorization-in-wcf.md)  
  
## <a name="see-also"></a>Confira também

- [Programação de WCF básica](../basic-wcf-programming.md)
- [Modelo de segurança para o Windows Server app Fabric](/previous-versions/appfabric/ee677202(v=azure.10))
