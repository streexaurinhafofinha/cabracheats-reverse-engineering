Cabra Xits — Reverse Engineering

Sobre

Bom, esse repositório é basicamente o registro da análise e engenharia reversa que fizemos no Cabra Xits.

A ideia foi pegar o APK, desmontar a estrutura interna e começar a fuçar em tudo que pudesse revelar algo interessante sobre o funcionamento da aplicação. Desde arquivos internos até integrações externas, configurações e possíveis exposições de informações sensíveis.

Oq encontramos?

Durante todo o processo fomos explorando a estrutura do APK, fazendo uma análise mais profunda dos componentes e tentando entender oq realmente existia por trás da aplicação.

Alguns pontos que conseguimos investigar:

- AndroidManifest.xml e seus metadados.
- Permissões e componentes declarados.
- Activities, Services e Receivers.
- Código Smali e recursos XML.
- Endpoints e referências a serviços externos.
- Configurações de backend.
- Integrações com Firebase.
- Possíveis exposições de credenciais e configurações sensíveis.

Firebase

Uma das descobertas mais interessantes foi durante a análise da integração com Firebase.

Conseguimos localizar as configurações do serviço, identificar a API Key e verificar permissões de escrita (write) associadas ao ambiente analisado.

Isso abriu uma parte interessante da investigação, já que encontramos configurações que mereciam uma análise mais aprofundada em relação à exposição de recursos e às políticas de acesso.

Processo de análise

Primeiramente fizemos a decompilação do APK pra conseguir acessar toda a estrutura disponível.

Dps começamos a realizar uma inspeção mais minuciosa nos diretórios, fazendo buscas por strings, referências, metadados e configurações que pudessem revelar informações relevantes.

Também exploramos os arquivos Smali, recursos XML e o manifesto, tentando mapear melhor a arquitetura interna da aplicação.

No meio disso, conseguimos identificar referências ao Firebase e analisar as configurações relacionadas às permissões de acesso.

Basicamente, foi bastante exploração, análise estática, reconhecimento da estrutura e investigação de possíveis exposições.


Considerações

Esse projeto surgiu da curiosidade de entender melhor como uma aplicação Android funciona internamente e oq pode acabar ficando exposto durante seu desenvolvimento.

Não foi simplesmente abrir o APK e olhar alguns arquivos, mas sim explorar sua estrutura, correlacionar informações e investigar possíveis pontos de exposição.

As credenciais, chaves e informações sensíveis não serão disponibilizadas publicamente.

Créditos

streex
Equipe da thr3at

Reverse Engineering • Research • Android Analysis
