---
title: Limite de taxa
redirect_from:
  - /v3/rate_limit
  - /v3/rate-limit
versions:
  free-pro-team: '*'
  enterprise-server: '*'
---

The REST API overview documentation describes the [rate limit rules](/rest/overview/resources-in-the-rest-api#rate-limiting). You can check your current rate limit status at any time using the Rate Limit API described below.

### Entender o seu status de limite de taxa

A API de pesquisa tem um [limite de taxa personalizado](/v3/search/#rate-limit), separado do limite de taxa que rege o restante da API REST. A API do GraphQL também tem um [limite de taxa personalizado](/v4/guides/resource-limitations/#rate-limit), que é separado e calculado de forma diferente dos limites de taxa na API REST.

Por esses motivos, a resposta da API do limite de taxa categoriza o seu limite de taxa. Under `resources`, you'll see four objects:

* O objeto `principal` fornece o status do limite de taxa para todos os recursos não relacionados à pesquisa na API REST.

* O objeto `de pesquisa` fornece o status do limite de taxa para a [API de pesquisa](/v3/search/).

* O objeto `graphql` fornece o status do limite de taxa para a [API do GraphQL](/v4/).

* O objeto `integration_manifest` fornece o status do limite de taxa para o ponto de extremidade [Conversão do código de manifesto do aplicativo GitHub](/apps/building-github-apps/creating-github-apps-from-a-manifest/#3-you-exchange-the-temporary-code-to-retrieve-the-app-configuration).

Para obter mais informações sobre os cabeçalhos e valores na resposta do limite de taxa, consulte "[Limitação de taxa](/v3/#rate-limiting)".

{% include rest_operations_at_current_path %}
