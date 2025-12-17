# Solução de Dados e IA para Canais Críticos Bancários

 **Apresentação completa do case (PDF):** 
 
[Visualizar slides do projeto](slide/Solucao_Dados_IA_Canais_Criticos.pdf)


## Cenário

Imagine um banco digital em crescimento acelerado, com milhares de clientes ativos e múltiplos canais de atendimento funcionando simultaneamente: telefone, aplicativo, WhatsApp e redes sociais.

Apesar da forte migração para os canais digitais, o banco enfrenta um cenário paradoxal: os canais mais utilizados pelos clientes são justamente aqueles que apresentam **maior SLA**, **maior índice de reabertura de chamados** e **maior insatisfação**.

Além disso, o time de dados recebe bases relevantes para análise, mas encontra uma limitação comum no ambiente bancário real: **as tabelas não se conectam perfeitamente**, seja por anonimização de dados, LGPD ou decisões arquiteturais.

Com isso, o desafio deixa de ser apenas técnico e passa a ser estratégico:

Como gerar valor real para o negócio, melhorar canais críticos e redesenhar jornadas sensíveis do cliente, mesmo com dados imperfeitos?

Pensando nesse cenário, desenvolvi este projeto com o objetivo de **criar uma solução de dados e inteligência artificial aplicável ao dia a dia bancário**, conectando análise, automação e experiência do cliente.

> Mesmo com limitações de dados, é possível gerar impacto real quando se aplica pensamento de produto, estratégia e tecnologia de forma integrada.


## Objetivo

O objetivo deste projeto foi **desenvolver uma solução integrada de dados e IA para canais críticos de atendimento bancário**, capaz de:

- Gerar insights estratégicos a partir de bases não totalmente integráveis;
- Automatizar atendimentos simples com uso de IA, mantendo segurança e controle humano;
- Redesenhar jornadas críticas do cliente, reduzindo atrito, custo operacional e frustração.

A proposta não foi apenas analisar dados, mas **construir uma solução de negócio escalável e orientada à experiência do cliente**.


## Ferramentas Utilizadas

- SQL Server  
- Power BI  
- Python  
- Power Automate  
- AI Builder  
- Inteligência Artificial (NLP e classificação de texto)
- Figma
- Conceitos de Modelagem de Dados  
- Arquitetura de fluxo de automação
- Fundamentos de LGPD e privacidade de dados  


## Planejamento da Solução

Antes da execução, a solução foi planejada em **três grandes frentes**, que juntas formam um único produto de dados:

1. Análise de dados e geração de insights estratégicos  
2. Automação inteligente de canais críticos com IA + protótipo
3. Redesenho da jornada do cliente (AS-IS → TO-BE)  

Essas frentes se complementam: os insights orientam a automação, e ambas sustentam a evolução da jornada do cliente.


## Etapas da Solução


### 1. Análise de Dados e Geração de Insights

#### Contexto dos Dados

As bases disponibilizadas para análise foram:

- **BaseGeral**: dados de clientes, produtos e atendimentos (CPF completo)  
- **BaseNome**: dados de perfil e segmentação (CPF anonimizado)  
- **BaseUF**: dados regionais (CPF anonimizado)  

#### Limitação Encontrada

A BaseGeral utiliza CPF completo como identificador, enquanto as demais utilizam CPF anonimizado, o que impede a integração direta entre as tabelas.

Essa limitação foi tratada como parte do cenário real bancário, onde privacidade e arquitetura de dados impactam diretamente as análises.

#### Principais Insights

Mesmo com análises isoladas, foi possível identificar oportunidades relevantes:

- A faixa etária de **25 a 40 anos** concentra maior renda ativa e potencial de consumo de produtos de maior margem;
- Clientes já preferem canais digitais, porém esses canais apresentam:
  - SLA mais elevado;
  - Maior índice de reabertura de chamados;
- Existe espaço para **cross-sell e criação de bundles de produtos**, especialmente para clientes com apenas conta corrente.

Esses insights fundamentam as próximas etapas da solução e foram obtidos por meio de análises e visualizações de dados em Python, utilizando Pandas para manipulação 
dos dados e Matplotlib para geração de gráficos.


### 2. Automação Inteligente de Canais Críticos com IA

#### Cenário

O banco recebe cerca de **500 comentários diários no Instagram**, mas a equipe consegue responder manualmente apenas cerca de **30% desse volume**.

Isso gera atrasos, insatisfação e uso ineficiente do time humano.

#### Objetivo da Automação

Automatizar interações simples e recorrentes, mantendo o atendimento humano apenas para casos sensíveis.

#### Fluxo de Automação Proposto

1. Captura de novo comentário  
2. Registro da interação em banco de dados (Data Lake)  
3. Classificação automática por IA (AI Builder)  
4. Decisão por categoria:
   - Reclamação grave → encaminhamento para análise humana  
   - Elogio ou dúvida → resposta automática  
   - Spam → descarte  
5. Publicação da resposta (quando aplicável)  
6. Registro final da interação  
7. Monitoramento contínuo do desempenho  

#### Protótipo e Testes

Foi criado um protótipo com comentários reais para simular o funcionamento do fluxo.

Resultados obtidos:

- **83% de acurácia** na classificação das intenções  
- **75% de qualidade** nas respostas automáticas  

O fluxo se mostrou funcional e escalável, com necessidade de refinamento apenas em cenários sensíveis.


### 3. Redesenho da Jornada do Cliente — Contestação de Compra

#### AS-IS (Situação Atual)

- Forte dependência do telefone  
- Pouca transparência de status  
- Cliente inseguro e ansioso  
- Alto volume de ligações apenas para acompanhamento  

#### TO-BE (Jornada Digital Integrada)

A proposta redesenha completamente a experiência do cliente:

- Autosserviço no aplicativo  
- Bloqueio imediato do cartão  
- Cartão virtual provisório  
- Estorno mais rápido  
- Notificações proativas de status  

#### Impactos Esperados

- Redução significativa de ligações  
- Cliente ativo durante todo o processo  
- Aumento da confiança e satisfação  
- Jornada mais fluida e previsível  


## Resultado Final da Solução

A integração das três frentes resulta em uma **Solução de Dados e IA para Canais Críticos Bancários**, focada em:

- Eficiência operacional  
- Melhoria de SLA em canais digitais  
- Redução de custos  
- Aumento de satisfação e retenção  
- Escalabilidade do atendimento  


## Considerações Finais

Este projeto demonstra como **dados, mesmo com limitações reais**, podem ser transformados em estratégia quando conectados a IA e automação.

Mais do que um case técnico, a solução reflete um pensamento orientado a negócio, experiência do cliente e tomada de decisão baseada em dados — pilares essenciais para organizações orientadas ao digital.


## Possíveis Melhorias

- Integração de métricas de atendimento em dashboards no Power BI  
- Treinamento contínuo do modelo de IA com feedback humano  
- Expansão da automação para outros canais críticos  
- Uso de IA generativa para respostas mais contextualizadas  


**Autoria:** Sarah Vitoria Rodrigues  

Projeto desenvolvido a partir de um desafio real, estruturado como uma solução de dados e IA com foco em negócio e experiência do cliente — 2025