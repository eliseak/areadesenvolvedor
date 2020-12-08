# {version}
[{date}]

## Quebra de compatibilidade

* Melhora a estrutura em Financiamentos PN e PJ para contemplar as alterações referentes à Distribuição de Frequência: 
  - Converte o atributo `interestRate` para array, sendo renomeado como `interestRates` 
  - Remove atributo `fees` de `interestRates`
  - Adiciona `referentialRateIndexer` e `rate` em `interestRates` 

## Melhoria

* Adiciona descrição complementar dos valores da enumeração `period` na especificação Open API de métricas.
* Adiciona descrição dos atributos nas seguintes estruturas na API de métricas na especificação Open API:
    - `ErrorMetrics`;
    - `RejectionMetrics`;
    - `PeakTPSMetrics`;
    - `AverageTPSMetrics`;
    - `AverageMetrics`;
    - `InvocationMetrics`;
    - `EndpointDowntime`;
    - `EndpointUptime`;
    - `AvailabilityMetrics`;
    - `ResponseMetricsList`;

## Correção

* Corrigi o dicionário `personal_acounts.csv` onde a definição de `name` em `priorityServices` trazia um exemplo que não condiz com os valores da enumeração.
* Remove a definição de tamanho de máximo e expressão regular no atributo `name` de `priorityServices` em contas PN na especificação Open API, pois se trata de uma enumeração.
* Adiciona a definição de expressão regular no atributo `name` de `otherServices` em contas PN na especificação Open API, conforme dicionário de dados.
* Corrige o atributo de representação de expressão regular para os seguintes atributos na especificação Open API (estavam como `format` porém o utilizado é `pattern`):
    - `serviceBundleDetail` em contas PN/PJ.
    - `interestRate` em empréstimos PN/PJ.
    - `indexer` em financiamentos PN/PJ.
    - `fees` em financiamentos PN/PJ.
    - `indexer` em antecipação de recebíveis PN/PJ.
    - `fees` em antecipação de recebíveis PN/PJ.
* Atualiza da Visão de alto de nível das estruturas de dados de Dependências Próprias
* Adiciona mínimo e máximo de ocorrências nos atributos da especificação em OAS de Dependências Próprias, conforme indicado no dicionário de dados:
  - `companies`
  - `branches`
  - `phones`
  - `services`
  - `standards`
* Remove obrigatoriedade dos atributos de Dependências Próprias, conforme indicado no dicionário de dados:
  - `countryCallingCode`
  - `areaCode`
  - `number`
* Adiciona indicador de "Não se Aplica" na expressão regular nos atributos da API de Canais de Atendimento que são obrigatórios:
  - Todos os atributos `cnpjNumber` em Canais Telefônicos, Canais Eletrônicos, Correspondentes Bancários e Dependências Próprias
  - `countryCallingCode`, `areaCode`, `number` em Canais Telefônicos
  - `code`, `postCode` em Dependências Próprias
* Corrigi o path da especificação Open API das APIs comuns de `outage` para `outages`.
* Corrigi o pattern de `CNPJ` e descrição de `InterestRates` em adiantamento à Depositantes.
* Corrigi obrigatoriedade e tamanho máximo na especificação Open API para os seguintes atributos:
  - `maximumRate` em LoanInterestRate para PN e PJ;
  - `minimumRate` em LoanInterestRate para PN e PJ;
* Corrige descrição dos seguintes atributos: 
  - `fees` em Financiamentos PN e PJ
  - `prices` em Financiamentos PN e PJ
* Corrige a descrição dos atributos de `AverageMetrics` para que esteja condizendo com tempo médio de resposta;  

# 2.0.0
[30/11/2020]

Versão 2.0.0 liberada com quebra de compatibilidade pois houveram alterações obrigatoriedade, valores de enumerações e remoção de campos de algumas APIs.