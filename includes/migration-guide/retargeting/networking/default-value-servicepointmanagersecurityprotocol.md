---
ms.openlocfilehash: 8aff4b1aa329d6fdfebf3b62e9279e9dfe5de0a4
ms.sourcegitcommit: 27a15a55019f6b5f2733961738babe94aec0def3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/15/2020
ms.locfileid: "90606912"
---
### <a name="default-value-of-servicepointmanagersecurityprotocol-is-securityprotocoltypesystemdefault"></a>O valor padrão de ServicePointManager.SecurityProtocol é SecurityProtocolType.System.Default

#### <a name="details"></a>Detalhes

A partir dos aplicativos destinados ao .NET Framework 4.7, o valor padrão da propriedade <xref:System.Net.ServicePointManager.SecurityProtocol?displayProperty=nameWithType> é <xref:System.Net.SecurityProtocolType.SystemDefault?displayProperty=nameWithType>. Essa alteração permite que APIs de rede do .NET Framework baseadas em SslStream (como FTP, HTTPS e SMTP) herdem os protocolos de segurança padrão do sistema operacional em vez de usar valores embutidos em código definidos pelo .NET Framework. O padrão varia de acordo com o sistema operacional e qualquer configuração personalizada executada pelo administrador do sistema. Para obter informações sobre o protocolo SChannel padrão em cada versão do sistema operacional Windows, confira [Protocols in TLS/SSL (Schannel SSP)](/windows/desktop/SecAuthN/protocols-in-tls-ssl--schannel-ssp-) [Protocolos em TLS/SSL (Schannel SSP)].</p>Para aplicativos direcionados a uma versão anterior do .NET Framework, o valor padrão da propriedade <xref:System.Net.ServicePointManager.SecurityProtocol?displayProperty=nameWithType> depende da versão do .NET Framework de destino. Consulte a [seção de Rede das Alterações de redirecionamento para a migração do .NET Framework 4.5.2 para 4.6](~/docs/framework/migration-guide/retargeting/4.5.2-4.6.md#networking) para obter mais informações.

#### <a name="suggestion"></a>Sugestão

Esta alteração afeta aplicativos direcionados ao .NET Framework 4.7 ou a versões posteriores. Se você preferir usar um protocolo definido em vez de contar com o padrão do sistema, defina explicitamente o valor da propriedade <xref:System.Net.ServicePointManager.SecurityProtocol?displayProperty=nameWithType>. Se essa alteração for indesejável, você poderá recusá-la adicionando um parâmetro de configuração à [\<runtime>](~/docs/framework/configure-apps/file-schema/runtime/runtime-element.md) seção do arquivo de configuração do aplicativo. O exemplo a seguir mostra a seção `<runtime>` e a opção de recusa `Switch.System.Net.DontEnableSystemDefaultTlsVersions`:

```xml
<runtime>
  <AppContextSwitchOverrides value="Switch.System.Net.DontEnableSystemDefaultTlsVersions=true" />
</runtime>
```

| Name    | Valor       |
|:--------|:------------|
| Escopo   | Secundária       |
| Versão | 4.7         |
| Tipo    | Redirecionando |

#### <a name="affected-apis"></a>APIs afetadas

- <xref:System.Net.ServicePointManager.SecurityProtocol?displayProperty=nameWithType>
