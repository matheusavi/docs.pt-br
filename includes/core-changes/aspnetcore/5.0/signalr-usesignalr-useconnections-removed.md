---
ms.openlocfilehash: 329ef39c7626ecd743577f336a4c8cd4a38fb082
ms.sourcegitcommit: e48a54ebe62e874500a7043f6ee0b77a744d55b4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/26/2020
ms.locfileid: "80291662"
---
### <a name="signalr-usesignalr-and-useconnections-methods-removed"></a>Signalr: métodos UseSignalR e UseConnections removidos

No ASP.NET Core 3,0, o Signalr adotou o roteamento de ponto de extremidade. Como parte dessa alteração, o <xref:Microsoft.AspNetCore.Builder.SignalRAppBuilderExtensions.UseSignalR%2A> , <xref:Microsoft.AspNetCore.Builder.ConnectionsAppBuilderExtensions.UseConnections%2A> e alguns métodos relacionados foram marcados como obsoletos. No ASP.NET Core 5,0, esses métodos obsoletos foram removidos. Para obter a lista completa de métodos, consulte [APIs afetadas](#affected-apis).

Para obter uma discussão sobre esse problema, consulte [dotnet/aspnetcore # 20082](https://github.com/dotnet/aspnetcore/issues/20082).

#### <a name="version-introduced"></a>Versão introduzida

5,0 Preview 3

#### <a name="old-behavior"></a>Comportamento antigo

Os hubs de sinalização e os manipuladores de conexão podem ser registrados no pipeline de middleware usando os `UseSignalR` `UseConnections` métodos ou.

#### <a name="new-behavior"></a>Novo comportamento

Os hubs de sinalização e os manipuladores de conexão devem ser registrados no <xref:Microsoft.AspNetCore.Builder.EndpointRoutingApplicationBuilderExtensions.UseEndpoints%2A> usando os <xref:Microsoft.AspNetCore.SignalR.HubRouteBuilder.MapHub%2A> <xref:Microsoft.AspNetCore.Http.Connections.ConnectionsRouteBuilder.MapConnectionHandler%2A> métodos de extensão e no <xref:Microsoft.AspNetCore.Routing.IEndpointRouteBuilder> .

#### <a name="reason-for-change"></a>Motivo da alteração

Os métodos antigos tinham lógica de roteamento personalizada que não interagia com outros componentes de roteamento em ASP.NET Core. No ASP.NET Core 3,0, um novo sistema de roteamento de uso geral, chamado de roteamento de ponto de extremidade, foi introduzido. O Signalr habilitado para roteamento de ponto de extremidade para interagir com outros componentes de roteamento. Alternar para esse modelo permite que os usuários percebam os benefícios completos do roteamento do ponto de extremidade. Consequentemente, os métodos antigos foram removidos.

#### <a name="recommended-action"></a>Ação recomendada

Remova o código que chama `UseSignalR` ou `UseConnections` do método do projeto `Startup.Configure` . Substitua-o por chamadas para `MapHub` ou `MapConnectionHandler` , respectivamente, no corpo de uma chamada para `UseEndpoints` . Por exemplo:

**Código antigo:**

```csharp
app.UseSignalR(routes =>
{
    routes.MapHub<SomeHub>("/path");
});
```

**Novo código:**

```csharp
app.UseEndpoints(endpoints =>
{
    endpoints.MapHub<SomeHub>("/path");
});
```

Em geral, suas `MapHub` chamadas e anteriores `MapConnectionHandler` podem ser transferidas diretamente do corpo de `UseSignalR` e `UseConnections` para `UseEndpoints` com pouca ou nenhuma alteração necessária.

#### <a name="category"></a>Categoria

ASP.NET Core

#### <a name="affected-apis"></a>APIs afetadas

- <xref:Microsoft.AspNetCore.Builder.ConnectionsAppBuilderExtensions.UseConnections%2A?displayProperty=nameWithType>
- <xref:Microsoft.AspNetCore.Builder.SignalRAppBuilderExtensions.UseSignalR%2A?displayProperty=nameWithType>
- <xref:Microsoft.AspNetCore.Http.Connections.ConnectionsRouteBuilder.MapConnections%2A?displayProperty=nameWithType>
- <xref:Microsoft.AspNetCore.Http.Connections.ConnectionsRouteBuilder.MapConnectionHandler%2A?displayProperty=nameWithType>
- <xref:Microsoft.AspNetCore.SignalR.HubRouteBuilder.MapHub%2A?displayProperty=nameWithType>

<!--

#### Affected APIs

- `Overload:Microsoft.AspNetCore.Builder.ConnectionsAppBuilderExtensions.UseConnections`
- `Overload:Microsoft.AspNetCore.Builder.SignalRAppBuilderExtensions.UseSignalR`
- `Overload:Microsoft.AspNetCore.Http.Connections.ConnectionsRouteBuilder.MapConnections`
- `Overload:Microsoft.AspNetCore.Http.Connections.ConnectionsRouteBuilder.MapConnectionHandler`
- `Overload:Microsoft.AspNetCore.SignalR.HubRouteBuilder.MapHub`

-->
