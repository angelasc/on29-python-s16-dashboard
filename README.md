<h1 align="center">
  <img src="assets/reprograma-fundos-claros.png" alt="logo reprograma" width="500">
</h1>

# Reprograma | Bootcamp de Análise de Dados
## 🚀 Exercícios para Casa 
Turma Online on29 | Semana 16 | 2024 | Professora Michelli Silva

Este repositório contém os exercícios desenvolvidos durante a **Semana 16** do curso de Análise de Dados da turma Online On29 da Reprograma. Os desafios foram realizados para consolidar os conhecimentos adquiridos em aula.  

## 📌 Descrição
Nesta semana, exploramos a criação de dashboards interativos com o objetivo de facilitar a visualização e a interpretação dos dados. Utilizamos a biblioteca Plotly para criar gráficos interativos e Dash para integrar esses gráficos em um painel completo, permitindo uma análise dinâmica e prática.

## 🎯 Objetivos do projeto
- Criar visualizações interativas com Plotly.
- Construir um dashboard com Dash para exibir múltiplos gráficos e informações de forma organizada.
- Integrar as funcionalidades interativas para permitir que os usuários explorem os dados de maneira eficiente.
- Desenvolver habilidades para criar dashboards dinâmicos que possibilitem análises em tempo real.

## 📝 Conteúdo do Repositório  
O repositório está organizado da seguinte maneira:
- app.py: Código principal onde o dashboard é configurado, e as visualizações interativas são inseridas.
- data.csv: Arquivo de dados utilizado para alimentar os gráficos do dashboard (caso aplicável).
- requirements.txt: Arquivo contendo dependências necessárias para o projeto. 

## 🖥️ Tecnologias utilizadas
- Python: Linguagem de programação utilizada para construir o dashboard e realizar a análise dos dados.
- Dash: Framework para construir dashboards interativos em Python.
- Plotly: Biblioteca para criar gráficos interativos e visualizações de dados.
- Pandas: Biblioteca para manipulação e análise de dados.


---


### Instruções
Antes de começar, vamos organizar nosso setup.
* Fork esse repositório 
* Clone o fork na sua máquina (Para isso basta abrir o seu terminal e digitar `git clone url-do-seu-repositorio-forkado`)
* Entre na pasta do seu repositório (Para isso basta abrir o seu terminal e digitar `cd nome-do-seu-repositorio-forkado`)

### Resumo
O que veremos na aula de hoje?
* [Principais Ferramentas de Visualização de Dados (BI)](#principais-ferramentas-de-visualização-de-dados-bi)
* [Objetivos de um Dashboard](#objetivos-de-um-dashboard)
* [O que são KPIs](#o-que-são-kpis-key-performance-indicators)
* [Design, boas práticas e acessibilidade para dashboards](#design-boas-práticas-e-acessibilidade-para-dashboards)
* [LGPD](#lgpd)

## Conteúdo
# Principais Ferramentas de Visualização de Dados (BI)



![O Quadrante Mágico para plataformas de análise e inteligência de negócios mostra 20 fornecedores posicionados nos quadrantes de Líderes, Desafiantes, Visionários ou Players de Nicho, conforme junho de 2024. Os fornecedores são avaliados com base na capacidade de execução e na completude da visão, para ajudar a guiar decisões de investimento.](https://raw.githubusercontent.com/reprograma/on29-python-s16-dashboard/main/assets/Figure_1_Magic_Quadrant_for_Analytics_and_Business_Intelligence_Platforms.png "Figura 1")

*Figura 1: Quadrante Mágico para Plataformas de Análise e Inteligência de Negócios, junho de 2024 (Gartner). Fonte: [https://www.gartner.com/doc/reprints?id=1-2HW1JC8Q&ct=240620&st=sb](https://www.gartner.com/doc/reprints?id=1-2HW1JC8Q&ct=240620&st=sb)*

Veremos brevemente sobre quatro plataformas que são líderes:

**[Power BI](https://www.microsoft.com/pt-br/power-platform/products/power-bi):** é uma solução de análise de negócios baseada em nuvem que permite reunir diferentes fontes de dados, analisá-las e apresentar a análise de dados por meio de visualizações, relatórios e painéis.

**[Qlik Sense](https://www.qlik.com):** é uma ferramenta de visualização de dados projetada para grandes empresas e indivíduos que desejam usar a análise aumentada para analisar dados.

**[Looker Studio](https://lookerstudio.google.com):** é uma ferramenta de visualização de dados da Google que permite a criação de relatórios e dashboards personalizados. Antigo Google Data Studio.

**[Tableau](https://www.tableau.com):** é uma ferramenta avançada e popular de visualização de dados que permite analisar dados de várias fontes simultaneamente. Adquirida em 2019 pela Salesforce.

Cada plataforma tem seus pontos fortes e fracos, não havendo uma "melhor" ou "pior" universal. A escolha da ferramenta ideal depende muito das necessidades específicas da empresa e do contexto em que ela será utilizada. Atualmente, Power BI e Tableau são amplamente usados no mercado, não necessariamente por serem as melhores em todos os aspectos, mas porque muitas empresas já as adotaram, criaram uma base de conhecimento interna e integraram essas ferramentas em seus processos. A familiaridade com essas plataformas e o suporte da comunidade também contribuem para sua popularidade. Por isso, ao escolher uma ferramenta de BI, é importante considerar não apenas os recursos técnicos, mas também o ecossistema e o suporte disponíveis.

Seguindo nosso conteúdo sobre Dashboards com Tableau, vamos ver primeiramente a definição de dashboard e seus objetivos.


# Objetivos de um Dashboard

Um dashboard é uma ferramenta visual que organiza e apresenta informações importantes de maneira clara e concisa, permitindo uma análise rápida e uma tomada de decisão eficiente. 

Seus principais objetivos são:

#### Consolidar dados
Agrupar dados de várias fontes em um único lugar para facilitar o acesso e a análise.\
**Benefício:** Reduz o tempo gasto na busca de informações dispersas, proporcionando uma visão completa e integrada dos dados.

#### Facilitar a tomada de decisão
Fornecer informações essenciais de maneira clara e intuitiva para apoiar decisões informadas e baseadas em dados.\
**Benefício:** Ajuda gestores e equipes a tomar decisões mais rápidas e precisas, baseadas em dados atualizados e relevantes.

#### Identificar tendências e padrões
Visualizar dados históricos e em tempo real para identificar tendências, padrões e anomalias.\
**Benefício:** Permite prever comportamentos futuros, preparar-se para mudanças e ajustar estratégias conforme necessário.

#### Comunicar informações eficazmente
Apresentar dados complexos de forma simplificada e visualmente atraente para facilitar a compreensão e a comunicação.\
**Benefício:** Melhora a clareza e a eficiência na comunicação de insights e resultados para diferentes públicos, incluindo stakeholders não técnicos.

#### Monitorar indicadores de desempenho (KPIs)
Exibir métricas e KPIs críticos em tempo real para avaliar o desempenho de processos, projetos ou negócios.\
**Benefício:** Permite identificar rapidamente áreas que estão performando bem e aquelas que precisam de atenção, ajudando a focar em ações corretivas ou preventivas.


### Benefícios de um dashboard bem projetado

**Clareza e Concisão:** Apresenta informações complexas de maneira clara e acessível.

**Interatividade:** Permite aos usuários interagir com os dados, filtrando e detalhando informações conforme necessário.

**Atualização em tempo real (ou quase):** Fornece dados atualizados, permitindo monitoramento e reação rápida a mudanças. Dependendo das necessidades do negócio e das capacidades técnicas, essa atualização pode ser em tempo real, diária (D-1), semanal, ou conforme definido pelos requisitos da organização.

**Customização:** Pode ser adaptado para atender às necessidades específicas de diferentes usuários e funções dentro da organização.

Um dos objetivos listados foi monitorar KPIs, e falaremos sobre esses indicadores agora.


# O que são KPIs (_Key Performance Indicators_)? 

KPIs (Indicadores Chave de Desempenho) são métricas utilizadas para avaliar e medir o desempenho de processos, projetos, equipes ou organizações em relação a objetivos estratégicos definidos. Eles fornecem uma maneira objetiva de acompanhar o progresso e a eficácia das ações implementadas, ajudando na tomada de decisões informadas.


### Características:

**Relevância:** Devem estar diretamente ligados aos objetivos estratégicos da organização.

**Mensurabilidade:** Devem ser quantificáveis para permitir uma avaliação objetiva.

**Alcance:** Devem ser claros quanto ao que está sendo medido e a quem se aplica.

**Temporalidade:** Devem ser monitorados regularmente para fornecer dados atualizados sobre o desempenho.

**Comparabilidade:** Devem permitir a comparação ao longo do tempo ou entre diferentes áreas da organização.


### Tipos: 

Em geral, existem 4 tipos diferentes de indicadores-chave, conforme explicamos abaixo. \




1. **Indicadores de produtividade**

Os KPIs de produtividade estão relacionados às necessidades de recursos para a entrega dos produtos e serviços aos clientes. Nesse sentido, eles ajudam a delimitar melhor os custos e otimizar o uso dos insumos. Um bom exemplo de um indicador de produtividade é o tempo de produção gasto em uma determinada atividade.



2. **Indicadores de qualidade**

Os KPIs de qualidade medem a eficiência dos processos em entregar aquilo que era esperado. Em geral, é utilizado para avaliar a satisfação dos clientes internos e externos em relação aos produtos e serviços prestados. A média de notas da pesquisa de satisfação é um exemplo desse indicador.



3. **Indicadores de capacidade**

Os KPIs de capacidade medem o quanto a empresa é capaz de entregar em volume de produtos e serviços. Trata-se de indicadores essenciais para determinar o crescimento ou a retração na base de produção e pode se beneficiar bastante do uso de inteligência de dados para a tomada de decisões mais precisas. Um exemplo de indicador de capacidade é o volume de produção por pessoa.



4. **Indicadores estratégicos**

Por fim, os KPIs estratégicos estão diretamente ligados às metas estabelecidas no planejamento estratégico do negócio. Esses indicadores mostram o quão perto (ou longe) a empresa está de alcançar seus objetivos e permitem a implementação de planos de ação caso seja necessário. Um exemplo desse indicador é o faturamento.


### Como definir KPIs:

**Identificar Objetivos Estratégicos:**



* Compreender os principais objetivos da organização, projeto ou processo.
* Alinhar os KPIs com esses objetivos para garantir relevância e impacto.

**Selecionar Métricas Adequadas:**



* Escolher métricas que sejam relevantes, mensuráveis e comparáveis.
* Garantir que as métricas selecionadas possam fornecer insights acionáveis.

**Estabelecer Metas:**



* Definir metas claras e alcançáveis para cada KPI.
* Utilizar benchmarks internos e externos para orientar a definição de metas.

**Coletar Dados:**



* Implementar sistemas e processos para coletar dados precisos e atualizados.
* Utilizar ferramentas de software para automatizar a coleta e análise de dados.

**Monitorar e Revisar Regularmente:**



* Acompanhar os KPIs regularmente para avaliar o progresso e a eficácia.
* Revisar e ajustar os KPIs conforme necessário para refletir mudanças nos objetivos ou no ambiente operacional.


### Benefícios dos KPIs:

**Foco Estratégico:** Ajudam a alinhar esforços com os objetivos estratégicos da organização.

**Tomada de Decisão Informada:** Fornecem dados objetivos para apoiar a tomada de decisões.

**Transparência e Responsabilidade:** Tornam o desempenho visível, promovendo transparência e responsabilidade.

**Melhoria Contínua:** Identificam áreas de melhoria e permitem o acompanhamento do progresso ao longo do tempo.

**Motivação:** Podem servir como motivadores, incentivando equipes e indivíduos a alcançar metas estabelecidas.


### Exemplos práticos de KPIs:

Empresas:



* Receita Mensal Recorrente (MRR)
* Custo de Aquisição de Cliente (CAC)
* Retorno sobre Investimento (ROI)

Saúde:



* Taxa de Ocupação Hospitalar
* Tempo Médio de Espera para Atendimento
* Taxa de Infecção Hospitalar

Educação:



* Taxa de Graduação
* Média de Notas dos Alunos
* Taxa de Evasão Escolar

Serviço ao Cliente:



* Tempo Médio de Resposta
* Satisfação do Cliente (NPS)
* Taxa de Resolução no Primeiro Contato

Agora que já sabemos sobre os indicadores-chaves, veremos um pouco mais profundamente questões de design e boas práticas, partindo dos principais erros ao se construir um dashboard, e como evitá-los:


# Design, boas práticas e acessibilidade para dashboards


## Principais erros na criação de dashboards

#### Poluição visual

Incluir muitos gráficos, cores, ou elementos desnecessários que tornam o dashboard confuso. Exemplo: um dashboard com múltiplos gráficos de diferentes tipos, cores vibrantes e sem um esquema claro de organização.

**Solução:** Simplificar o design, usar um esquema de cores consistente e destacar apenas as informações mais importantes.

#### Uso inadequado de gráficos

Escolher tipos de gráficos que não representam corretamente os dados. Exemplo: utilizar um gráfico de pizza para mostrar variações mínimas entre categorias ou eixos truncados que distorcem a percepção das diferenças nos dados.

**Solução:** Selecionar gráficos que melhor correspondam à natureza dos dados e à mensagem que se deseja transmitir.

💡Vale a leitura:
* [https://pt.khanacademy.org/math/pt-9-ano/probabilidade-e-estistica-9ano/graficos-e-tabelas-9ano/a/erro-de-leitura-em-graficos](https://pt.khanacademy.org/math/pt-9-ano/probabilidade-e-estistica-9ano/graficos-e-tabelas-9ano/a/erro-de-leitura-em-graficos)
* [https://www.statisticshowto.com/probability-and-statistics/descriptive-statistics/misleading-graphs/](https://www.statisticshowto.com/probability-and-statistics/descriptive-statistics/misleading-graphs/)

#### Falta de hierarquia visual

Não organizar as informações de maneira que o usuário possa identificar rapidamente o que é mais importante. Exemplo: todas as informações são apresentadas com o mesmo destaque, dificultando a identificação do que é mais importante.

**Solução:** Utilizar tamanho, cor e disposição para criar uma hierarquia clara, destacando as informações mais críticas.

#### Dados desatualizados

Mostrar dados que não são atuais ou não refletem a situação atual.

**Solução:** Garantir que o dashboard seja atualizado regularmente com os dados mais recentes.

#### Ignorar o público-alvo

Criar dashboards sem considerar as necessidades e o nível de conhecimento dos usuários finais.

**Solução:** Conhecer o público-alvo e adaptar a complexidade e o tipo de informação exibida de acordo com suas necessidades.

#### Falta de contexto

Apresentar dados sem fornecer o contexto necessário para interpretá-los corretamente.

**Solução:** Incluir comparações históricas, metas, ou benchmarks para dar aos usuários uma melhor compreensão dos dados.

#### Inacessibilidade

Criar dashboards que não são acessíveis a todos os usuários, incluindo aqueles com deficiências.

**Solução:** Seguir as melhores práticas de acessibilidade, como o uso de textos alternativos, cores contrastantes, e opções de navegação via teclado.

#### Excesso de detalhes

Mostrar muitos detalhes que podem sobrecarregar o usuário e obscurecer as principais conclusões.

**Solução:** Focar nas principais métricas e fornecer a opção de explorar mais detalhes conforme necessário.

#### Gráficos 3D

Utilizar gráficos 3D que podem distorcer a percepção dos dados.

**Solução:** Preferir gráficos 2D que são mais precisos e fáceis de interpretar.


### Como evitar esses erros

**Planejamento e Design:** Investir tempo no planejamento do layout e no design do dashboard para garantir clareza e eficácia. Criar protótipos é sempre uma [boa opção](https://awari.com.br/prototipo-de-dashboard-no-figma-aprenda-a-criar-interfaces-incriveis/).

**Teste com usuários finais:** Testar os dashboards com uma amostra do público-alvo e coletar feedback para melhorias.

**Atualização contínua:** Monitorar e atualizar os dashboards regularmente para garantir que eles permanecem relevantes e precisos.


### Por que evitar gráficos 3D 


#### Passagem de informação errada

**Distorção Visual**

Gráficos 3D podem distorcer a percepção dos dados, fazendo com que elementos pareçam maiores ou menores do que realmente são. Isso pode levar a interpretações erradas dos dados, prejudicando a tomada de decisões.

Exemplo: Em um gráfico de barras 3D, as barras mais próximas do observador parecem maiores que as mais distantes, independentemente dos valores reais.

**Ambiguidade de perspectiva**

A perspectiva tridimensional pode criar ambiguidade, dificultando a comparação precisa entre os valores, reduzindo a clareza e a precisão da análise visual dos dados.

Exemplo: Em um gráfico de pizza 3D, as fatias podem parecer desproporcionalmente maiores ou menores dependendo do ângulo de visão.

**Sombreamento e Reflexos**

Efeitos de sombreamento e reflexos em gráficos 3D podem obscurecer partes dos dados, podendo levar a uma interpretação equivocada ou incompleta dos dados apresentados.

Exemplo: Reflexos em uma superfície curva de um gráfico 3D podem esconder ou destacar indevidamente certas partes dos dados.


#### Questões de Acessibilidade

**Dificuldade para Pessoas Monoculares**

Pessoas monoculares, que possuem visão em apenas um olho, têm dificuldade em perceber profundidade e perspectiva tridimensional. Assim, Gráficos 3D podem ser difíceis de interpretar corretamente para essas pessoas, tornando a análise de dados menos acessível.

**Limitações de Cores e Contraste**

Gráficos 3D muitas vezes dependem de gradientes de cor e sombreamento, que podem ser difíceis de discernir para pessoas com deficiências visuais, como daltonismo. Desse modo, inclui uma dificuldade em distinguir entre diferentes elementos do gráfico, prejudicando a clareza da informação.

**Compatibilidade com Leitores de Tela**

Ferramentas de acessibilidade, como leitores de tela, não conseguem interpretar gráficos 3D de forma eficaz. Isso faz com que usuários que dependem dessas ferramentas possam não conseguir acessar as informações apresentadas em gráficos 3D.

Evitar gráficos 3D é uma prática recomendada para garantir a precisão, clareza e acessibilidade dos dados apresentados. Gráficos 2D, bem projetados, com cores e contrastes adequados, e acompanhados de descrições alternativas, proporcionam uma experiência de análise de dados mais eficaz e inclusiva.

💡Evite sempre detalhes desnecessários como sombreamentos e texturas, mesmo em gráficos 2D.


## Design e Boas Práticas para Dashboards 

**Limitar a quantidade de informações**



* Utilizar uma quantidade limitada de gráficos e elementos por dashboard.
* Priorizar as métricas e KPIs mais importantes para o objetivo do dashboard.

**Fazer uso de espaços em branco**



* Utilizar espaços em branco para criar uma separação visual entre diferentes seções e gráficos.
* Garantir que cada elemento tenha espaço suficiente ao redor para ser claramente distinguível.

**Uso moderado e adequado de cores**



* Escolher uma paleta de cores consistente e evitar o uso excessivo de cores.
* Utilizar cores para destacar informações importantes e manter o restante neutro.
* Utilizar cores de forma coerente para representar categorias ou valores similares.
* Evitar combinações de cores que possam ser difíceis de distinguir para pessoas com daltonismo.

**Escolher o tipo de gráfico adequado**



* Selecionar o tipo de gráfico que melhor representa os dados e facilita a compreensão.
* Evitar gráficos de pizza para muitas categorias e preferir gráficos de barras ou linhas.

**Manter a proporcionalidade**



* Garantir que os gráficos de pizza e outros gráficos proporcionais sejam dimensionados corretamente.
* Evitar truncamento de eixos, a menos que seja absolutamente necessário e claramente indicado.

**Organização lógica**



* Organizar visualmente os dados de forma lógica e intuitiva, agrupando informações relacionadas.
* Utilizar hierarquias visuais para guiar o olhar do usuário


![Diagrama de fundo amarelo que mostra o ordenamento adequado de exibição de informações dada sua importância. A imagem é dividida em quatro quadrantes, sendo o primeiro para a informação importante, o segundo, à direita, e o terceiro, abaixo do primeiro à esquerda, para informação secundária ou mais específica, e o quarto, abaixo à direita, para a informação menos importante.](https://www.dashboarddesign.com.br/wp-content/uploads/2019/04/Ordenamento-do-conteudo-2.png "Figura 2")

*Figura 2: Diagrama que mostra o ordenamento mais adequado de informações dada a sua importância.*

**Títulos e legendas informativos**



* Adicionar títulos e legendas claros e descritivos para cada gráfico e seção.
* Garantir que os títulos expliquem claramente o que o gráfico ou a seção representa.

**Glossário informativo**



* Definir termos e métricas: Inclua definições claras para todos os termos e métricas usadas no dashboard.
* Facilitar a compreensão: Assegure que todos os usuários, independentemente do seu nível de conhecimento, compreendam os dados.
* Promover consistência: Evite mal-entendidos e promova uma interpretação uniforme dos dados.
* Referência rápida: Disponibilize uma referência rápida e fácil de acessar para esclarecer dúvidas instantaneamente.
* Suporte à decisão: Facilite a tomada de decisões informadas ao garantir que todos entendam exatamente o que os dados representam.

💡[https://www.linkedin.com/pulse/creating-glossary-your-dashboard-why-its-important-how-singh/](https://www.linkedin.com/pulse/creating-glossary-your-dashboard-why-its-important-how-singh/) (em inglês)

**Tamanhos de fonte apropriados**



* Utilizar tamanhos de fonte adequados para textos e rótulos (mínimo de 12-14pt para textos principais).
* Garantir que todos os textos sejam facilmente legíveis em diferentes dispositivos.

**Contrastes adequados**



* Utilizar contrastes de cor que garantam a legibilidade (verificar com ferramentas de contraste, como o simulador de contraste do WebAIM).
* Evitar combinações de cores que possam ser difíceis de distinguir.


## Acessibilidade para Dashboards

**Descrições alternativas**



* Adicionar descrições alternativas para elementos gráficos, explicando o conteúdo e o contexto.
* Garantir que as descrições sejam concisas e informativas.

**Dicas de Ferramenta (Tooltips)**



* Forneça explicações adicionais e contextuais sobre os dados ao passar o cursor sobre elementos gráficos.
* Apresente detalhes adicionais que não cabem no visual principal, como valores específicos ou descrições de métricas (para descrições, considere também o Glossário como dito antes).
* Garanta que os tooltips sejam compatíveis com tecnologias assistivas, como leitores de tela, para melhorar a acessibilidade para usuários com deficiência visual.

**Acessibilidade via teclado**



* Garantir que todos os elementos interativos sejam acessíveis via teclado.
* Testar a navegação por teclado e corrigir problemas identificados.

💡[https://help.tableau.com/current/pro/desktop/pt-br/access_keyboard_navigation.htm](https://help.tableau.com/current/pro/desktop/pt-br/access_keyboard_navigation.htm)

**Testes de acessibilidade**



* Utilizar ferramentas específicas para testar a acessibilidade dos dashboards (por exemplo, ferramentas do [WAVE](https://wave.webaim.org/) ou [Lighthouse](https://learn.microsoft.com/pt-br/microsoft-edge/devtools-guide-chromium/accessibility/lighthouse) [[outro link](https://mwpt.com.br/como-avaliar-a-acessibilidade-de-aplicacoes-web-com-o-lighthouse/)]).
* Implementar as recomendações fornecidas pelas ferramentas de teste.


# LGPD

A Lei Geral de Proteção de Dados Pessoais (LGPD), Lei nº 13.709/2018, é a legislação brasileira que regula o tratamento de dados pessoais, tanto online quanto offline, por pessoas físicas ou jurídicas, públicas ou privadas. A LGPD tem como objetivo garantir a privacidade e a proteção dos dados pessoais dos cidadãos, estabelecendo direitos dos titulares dos dados, obrigações dos controladores e operadores, e sanções para quem descumprir a lei.

💡Links importantes:

Lei:\
[https://www.gov.br/esporte/pt-br/acesso-a-informacao/lgpd](https://www.gov.br/esporte/pt-br/acesso-a-informacao/lgpd)\
[https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm)

Princípios da LGPD:\
[https://www.gov.br/esporte/pt-br/acesso-a-informacao/lgpd/principios-da-lgpd](https://www.gov.br/esporte/pt-br/acesso-a-informacao/lgpd/principios-da-lgpd)

Tipos de dados:\
[https://www.gov.br/esporte/pt-br/acesso-a-informacao/lgpd/classificacao-dos-dados](https://www.gov.br/esporte/pt-br/acesso-a-informacao/lgpd/classificacao-dos-dados)

Glossário:\
[https://www.gov.br/esporte/pt-br/acesso-a-informacao/lgpd/glossario-de-termos-tecnicos-da-lgpd](https://www.gov.br/esporte/pt-br/acesso-a-informacao/lgpd/glossario-de-termos-tecnicos-da-lgpd)


## Importância do cuidado com LGPD no contexto de um analista de dados 

**Proteção da Privacidade**

Mesmo não sendo responsáveis pela coleta dos dados, os analistas de dados manipulam e apresentam informações pessoais que podem identificar indivíduos. Assim, é importante garantir que os dados apresentados sejam tratados de maneira ética e segura é fundamental para proteger a privacidade dos titulares.

**Conformidade Legal**

Garantir que as visualizações não exponham dados sensíveis indevidamente, pois a não conformidade pode resultar em multas significativas, sanções administrativas e danos à reputação da empresa.

**Segurança dos Dados**

Implementar práticas para garantir que os dashboards ou resultados de análises sejam seguros e que dados sensíveis não sejam acessíveis sem autorização. Prevenir vazamentos de dados e acessos não autorizados é crucial para manter a integridade das informações e a confiança dos usuários.

**Anonimização e Agregação de Dados**

Utilizar técnicas de anonimização e agregação para proteger a identidade dos indivíduos ao apresentar seus dados, reduzindo o risco de exposição de informações pessoais, cumprindo os requisitos da LGPD para proteção de dados. A anonimização é uma técnica de processamento de dados que remove ou modifica informações que possam identificar a pessoa, garantindo sua desvinculação. Nestes casos, a LGPD não se aplicará ao dado.

Ressalta-se que o dado somente é considerado anonimizado se não permitir que, por meios técnicos ou outros, seja reconstruído o caminho para revelar quem é o titular do dado. Se a identificação ocorrer, não se tratará de dado anonimizado, mas sim de dado pseudonimizado, e estará sujeito à LGPD.

**Transparência e Consentimento**

Assegurar que os dados utilizados tiveram seu uso consentido pelo titular.

**Responsabilidade Social e Ética:**

Demonstrar um compromisso com a proteção dos dados pessoais, mesmo na fase de visualização e análise.

Para analistas de dados, a conformidade com a LGPD envolve garantir que as visualizações de dados protejam a privacidade dos indivíduos e cumpram os requisitos legais. Isso inclui práticas como anonimização, agregação de dados, implementação de controles de acesso e garantir a transparência e o consentimento no uso dos dados. A proteção dos dados pessoais nas análises não só evita sanções legais, mas também fortalece a confiança dos usuários e demonstra responsabilidade social e ética.

***
### Exercícios 
* [Exercicio para sala](https://github.com/mflilian/repo-example/tree/main/exercicios/para-sala)
* [Exercicio para casa](https://github.com/mflilian/repo-example/tree/main/exercicios/para-casa)

### Material da aula 
* [Slides](https://www.canva.com/design/DAGKPjtXJec/7EVh60A4UAXhC6oC13qfAA/view?utm_content=DAGKPjtXJec&utm_campaign=designshare&utm_medium=link2&utm_source=uniquelinks&utlId=GQoLKn2AkQ) 
* [Base de Dados](https://github.com/reprograma/on29-python-s16-dashboard/tree/main/material/base_final_s14_olist.csv)

### Links Úteis
- [Indicação de livros de visualização de dados](https://www.tableau.com/pt-br/learn/articles/books-about-data-visualization)
- ["Livro de Receitas" de Visualizações no Tableau](https://public.tableau.com/views/CookBook/VizCookbook)
- [Trilha de conhecimento para letramento em dados](https://trailhead.salesforce.com/pt-BR/content/learn/trails/build-your-data-literacy)
- [Exemplos de belas visualizações de dados](https://www.tableau.com/pt-br/learn/articles/best-beautiful-data-visualization-examples)
- [Trilha de storytelling com Tableau (inglês)](https://trailhead.salesforce.com/content/learn/modules/data-storytelling-tableau-public?utm_campaign=trailblazer_blog&utm_content=careers_feb24_data-skills&utm_medium=blog-360&utm_source=salesforce)
- [Guia de visualização de dados](https://www.tableau.com/pt-br/learn/articles/data-visualization)
- [Dicas de como criar um bom dashboard](https://www.dashboarddesign.com.br/a-importancia-de-um-bom-design-para-a-criacao-de-dashboards-eficientes-no-excel/)
- [Artigo de lista de acessibilidade para Tableau (inglês)](https://portal.lancaster.ac.uk/ask/checklist-tableau/)
- [Comparativo de ferramentas de BI (2022)](https://www.reddit.com/r/PowerBI/comments/s3o6hi/the_most_indepth_comparison_of_bi_tools_followup/#lightbox)



<p align="center">
Desenvolvido com :purple_heart:  
</p>

