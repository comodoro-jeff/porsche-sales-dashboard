# Porsche Sales Dashboard — Análise Interativa de Vendas

Dashboard interativa desenvolvida a partir de uma base de vendas da Porsche, com o objetivo de transformar dados tabulares em informações visuais e indicadores capazes de responder a perguntas de negócio. O projeto explora a utilização de Inteligência Artificial Generativa no desenvolvimento de interfaces analíticas em HTML, permitindo a construção de uma solução interativa, independente do Excel e disponibilizada publicamente na web.

## Objetivo

Transformar uma planilha de vendas da Porsche em uma dashboard interativa, acessível por meio de um navegador, que permita explorar o desempenho comercial da marca e identificar padrões de vendas a partir de diferentes dimensões de análise.

A solução foi desenvolvida para:

- Transformar uma base de vendas em uma interface analítica interativa.
- Responder a perguntas de negócio por meio de gráficos e indicadores.
- Permitir a exploração dos dados por diferentes filtros.
- Apresentar indicadores consolidados de vendas e receita.
- Disponibilizar a dashboard publicamente por meio do GitHub Pages.

## Perguntas de Negócio

Foram selecionadas três perguntas para orientar a análise, considerando diferentes perspectivas sobre o comportamento das vendas.

### 1. Qual foi o modelo mais popular em cada estado?

**Justificativa:** compreender a preferência regional pelos diferentes modelos permite identificar diferenças no comportamento dos consumidores e possíveis concentrações de demanda por região.

### 2. Qual foi a trajetória de vendas de um modelo no decorrer dos anos?

**Justificativa:** a análise temporal possibilita identificar tendências, oscilações e mudanças no volume de comercialização, contribuindo para compreender o comportamento de cada modelo ao longo do tempo.

### 3. Em qual modelo os carros usados são mais procurados que os zero milhas?

**Justificativa:** identificar modelos com maior participação de veículos usados permite compreender diferenças no comportamento de compra e na composição da demanda entre as categorias de veículos.

## Dados e Preparação da Base

O projeto utilizou uma planilha de vendas da Porsche como fonte de dados.

Antes de utilizar a base na construção da dashboard, foram realizadas etapas de preparação para melhorar a consistência das informações disponibilizadas à ferramenta de Inteligência Artificial Generativa.

O tratamento contemplou:

- Identificação e tratamento de datas inválidas.
- Remoção de colunas que continham dados inconsistentes para a análise.
- Seleção das colunas sanitizadas que seriam utilizadas na dashboard.
- Conversão dos valores de preço para um formato numérico adequado à realização de operações e cálculos.

As informações foram organizadas de maneira a permitir operações de agregação, comparação e segmentação, necessárias para a construção dos indicadores e visualizações.

## Dashboard Interativa

A solução foi desenvolvida em HTML, concentrando sua implementação em um único arquivo (`index.html`).

A interface foi organizada em seções que apresentam indicadores executivos, filtros interativos, visualizações analíticas e um registro detalhado das transações.

### Indicadores Executivos

A dashboard apresenta indicadores consolidados para acompanhar o desempenho geral das vendas:

- Receita total consolidada.
- Total de vendas.
- Ticket médio.
- Proporção de veículos usados.
- Modelo líder no recorte selecionado.

Também são apresentados indicadores complementares, como a quantidade e a proporção de veículos entregues.

### Filtros e Segmentação

A interface permite segmentar os dados considerando diferentes dimensões:

- Modelo da Porsche.
- Mês de venda.
- Ano de venda.
- Milhas do veículo.
- Estado.

Além dos filtros, foi implementada a possibilidade de alternar o agrupamento dos modelos entre:

- Linha principal: agrupamento por família de modelos, como 911 e Cayenne.
- Versão completa: identificação das versões específicas dos veículos.

A funcionalidade de limpeza dos filtros permite retornar à visualização consolidada.

### Visualizações Analíticas

As três perguntas de negócio são respondidas por meio de visualizações específicas:

- **Liderança regional:** gráfico e tabela com o modelo mais popular em cada estado, incluindo informações de vendas e receita.
- **Evolução temporal:** visualização da trajetória de vendas de um modelo ao longo dos períodos disponíveis.
- **Mercado secundário:** comparação entre veículos usados e zero milhas por modelo.

### Registro de Transações

A dashboard também disponibiliza uma tabela detalhada das transações, permitindo consultar informações como:

- Identificador da venda.
- Data da venda.
- Modelo.
- Ano de fabricação.
- Milhagem.
- Condição do veículo.
- Estado e cidade.
- Preço.
- Status da transação.

## Identidade Visual

A identidade visual foi concebida para transmitir elegância, velocidade e profissionalismo, buscando coerência com o posicionamento da Porsche.

Como referência estética, foi utilizado o site da Ferrari de São Paulo:

[https://saopaulo.ferraridealers.com/pt-PT](https://saopaulo.ferraridealers.com/pt-PT)

A proposta visual priorizou uma apresentação limpa e refinada, com atenção à paleta de cores, tipografia, hierarquia das informações e organização dos elementos gráficos.

Foram utilizadas as famílias tipográficas Cormorant Garamond e Inter, combinando características editoriais e contemporâneas.

## Metodologia de Desenvolvimento e Utilização de IA Generativa

A construção da dashboard foi realizada com o auxílio do Gemini, utilizando sua interface convencional de conversação, sem a utilização de agentes especializados ou ferramentas como Canvas.

A Inteligência Artificial Generativa foi utilizada como ferramenta de apoio à implementação da interface HTML, interpretação dos requisitos de visualização e refinamento dos elementos apresentados.

O desenvolvimento foi organizado em quatro etapas.

### 1. Preparação dos Dados

A planilha original foi submetida a um processo de limpeza e sanitização, com tratamento de datas inválidas, remoção de colunas com dados sujos e conversão dos valores monetários para formatos adequados à análise.

Após essa etapa, foi utilizada uma versão preparada da base para orientar a construção da dashboard.

### 2. Construção do Prompt Inicial

Foi elaborado um prompt contendo os requisitos funcionais e visuais da solução, especificando os filtros, as perguntas de negócio, os indicadores de topo e a referência estética desejada.

**Prompt inicial utilizado:**

```text
Chat, crie uma dashboard em HTML que seja um arquivo único com os seguintes filtros:

# Filtros

- Modelo da Porsche
- Mês de Venda
- Ano de Venda
- Milhas do Veículo
- Estados

Além disso, ele deve responder as seguintes perguntas de negócio:

# Perguntas de Negócio

- Qual foi o modelo mais popular em cada estado?
- Qual foi a trajetória de vendas de um modelo no decorrer do(s) ano(s)?
- Em qual modelo os carros usados são mais procurados que os zero milhas?

Cada pergunta deve ser respondida por um gráfico ou por um indicador; também inclua indicadores de topo, como o total de vendas e a receita.

O visual deverá ser limpo e refinado, passando um ar europeu de elegância, velocidade e profissionalismo.

Como referência, use o site da Ferrari de São Paulo:
https://saopaulo.ferraridealers.com/pt-PT

Por fim, o nome do arquivo html deverá ser index.html.
```

### 3. Refinamento Iterativo

Após a geração da primeira versão, foram realizadas interações adicionais com o Gemini para corrigir e complementar elementos que não estavam sendo apresentados conforme o esperado. Os refinamentos tiveram como foco:

- Corrigir gráficos que não estavam aparecendo.
- Ajustar indicadores e valores que não estavam sendo exibidos.
- Adequar as visualizações às perguntas de negócio propostas.
- Melhorar a apresentação e a consistência dos elementos da dashboard.

O processo foi conduzido por meio de instruções em linguagem natural, permitindo ajustar a implementação progressivamente até alcançar a versão final. A versão final incorporou elementos complementares aos requisitos iniciais, como indicadores adicionais, agrupamento por família, versão específica dos modelos e uma tabela detalhada de transações.

### 4. Publicação

Após a conclusão dos ajustes, o arquivo HTML foi baixado e salvo como `index.html`. Em seguida, foi criado um repositório público no GitHub, no qual o arquivo foi disponibilizado. A publicação foi realizada por meio do GitHub Pages, utilizando a funcionalidade disponível nas configurações do repositório. Dessa forma, a dashboard passou a ser acessível por um endereço público, sem necessidade de executar uma aplicação localmente.

## Tecnologias e Ferramentas

- HTML
- Gemini — Inteligência Artificial Generativa
- GitHub
- GitHub Pages

## Evidências do Projeto

Abaixo estão reunidas as evidências visuais da solução desenvolvida.

### Dashboard Completa

![Dashboard Porsche — Visão geral](assets/images/dashboard-overview.png)

### Exemplo de Filtro Aplicado

![Dashboard Porsche — Exemplo de filtro](assets/images/dashboard-filter.png)

As imagens apresentam a interface desenvolvida e um exemplo de utilização dos filtros interativos.

## Acesso à Dashboard

**[Acessar Dashboard Interativa — Porsche Sales Dashboard](https://comodoro-jeff.github.io/porsche-sales-dashboard/)**

O código-fonte da aplicação está disponível neste repositório, no arquivo `index.html`.

## Estrutura do Repositório

```text
porsche-sales-dashboard/
│
├── assets/
│   └── images/
│       ├── dashboard-overview.png
│       └── dashboard-filter.png
│
├── README.md
│
└── index.html
```

## Considerações Finais

O projeto demonstrou, na prática, a utilização de Inteligência Artificial Generativa como ferramenta de apoio à construção de soluções analíticas e interfaces interativas.

Além da elaboração da dashboard, o desenvolvimento envolveu etapas de preparação de dados, definição de perguntas de negócio, especificação de requisitos, refinamento iterativo de código e publicação de uma aplicação web estática. A solução evidencia como uma base originalmente organizada em uma planilha pode ser transformada em uma experiência de exploração de dados mais acessível, visual e interativa, permitindo investigar diferentes perspectivas comerciais sem depender da interface tradicional de uma planilha eletrônica.
