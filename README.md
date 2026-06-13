# segundo-cerebro-nlp-commodities
Caderno temático sobre análise de sentimentos para predição de commodities — Bootcamp Bradesco
# 🧠 Segundo Cérebro com IA: Análise de Sentimentos para Predição de Commodities

> **Bootcamp Bradesco · Desafio Prático NotebookLM**
> Caderno Temático construído com curadoria ativa de fontes abertas, engenharia de prompts documentada e miniguia consolidado para revisão e portfólio.

---

## 📌 Contexto e Objetivos

### Por que esse tema?

O Brasil é o maior exportador mundial de soja, café, açúcar e carne bovina. Bancos como o Bradesco gerenciam carteiras bilionárias de crédito rural e financiamento agrícola — e a volatilidade de preços de commodities é o principal fator de risco dessas operações.

A pergunta que este projeto responde é:

> **É possível usar IA para extrair sinais preditivos de volatilidade de commodities a partir do "humor" de notícias financeiras?**

A resposta, segundo a literatura científica mais recente, é **sim** — e a técnica se chama **Análise de Sentimentos com Processamento de Linguagem Natural (PLN/NLP)**.

### Objetivos do Estudo

| # | Objetivo | Resultado Esperado |
|---|----------|--------------------|
| 1 | Compreender como modelos de linguagem (BERT, LSTM) classificam sentimentos em textos financeiros | Conceito aplicado ao contexto bancário |
| 2 | Identificar como bancos usam NLP para antecipar movimentos de mercado | Casos de uso reais documentados |
| 3 | Mapear as fontes de dados abertas disponíveis no Brasil para esse tipo de análise | Lista curada e acessível |
| 4 | Construir prompts estratégicos reutilizáveis para o NotebookLM | Banco de prompts documentado |
| 5 | Produzir glossário e resumos estruturados para revisão rápida | Miniguia final consolidado |

---

## 📚 Curadoria de Fontes

Todas as fontes abaixo são abertas, gratuitas e foram carregadas no NotebookLM para composição deste caderno temático. A seleção prioriza: relevância ao contexto bancário brasileiro, rigor acadêmico e acessibilidade para iniciantes em dados.

### Fonte 1 — FinBERT-PT-BR: Análise de Sentimentos em Textos Financeiros em Português

- **Instituição:** Sociedade Brasileira de Computação (SBC) — BWAIF 2023
- **Por que escolhi:** É o único modelo BERT treinado especificamente para textos financeiros em **português brasileiro**. Diretamente aplicável a notícias da Globo Rural, Valor Econômico e relatórios do CONAB.
- **Link:** [Download PDF direto](https://sol.sbc.org.br/index.php/bwaif/article/download/24960/24781/)

### Fonte 2 — PLN e Modelos Preditivos no Mercado Financeiro

- **Instituição:** Revista Contemporânea (2025)
- **Por que escolhi:** Revisão completa que conecta LSTM e BERT à previsão de tendências de mercado, com discussão de desafios éticos e técnicos — essencial para uma visão crítica do tema.
- **Link:** [Download PDF direto](https://ojs.revistacontemporanea.com/ojs/index.php/home/article/download/8335/5803/23717)

### Fonte 3 — Análise de Sentimentos e Indicadores Técnicos de Ativos

- **Instituição:** Brazilian Journals (2021)
- **Por que escolhi:** Demonstra empiricamente a correlação entre polaridade de notícias e variação de preço de ativos — exatamente o mecanismo que um banco usaria para gestão de risco em crédito rural.
- **Link:** [Download PDF direto](https://ojs.brazilianjournals.com.br/ojs/index.php/BJB/article/download/24482/19554/63003)

### Fonte 4 — Forecasting Commodity Price Shocks Using Agentic Generative AI

- **Instituição:** arXiv (2025)
- **Por que escolhi:** Artigo de fronteira que combina sinais de preço histórico com extração de notícias via LLM para prever choques em commodities. Representa o estado da arte e o caminho futuro dessa área.
- **Link:** [Download PDF direto](https://arxiv.org/pdf/2508.06497)

### Fonte 5 — Narrativas do Banco Central e Previsões Macroeconômicas via ML

- **Instituição:** ANPEC / UFPB (2022)
- **Por que escolhi:** Mostra como o próprio Banco Central brasileiro já aplica técnicas de NLP nas atas do COPOM para previsão macroeconômica — validando que essa abordagem é institucionalizada no setor financeiro nacional.
- **Link:** [Download PDF direto](https://www.anpec.org.br/encontro/2022/submissao/files_I/i4-dcb2aec395e0613c42cef5c5f33ffe00.pdf)

---

## 🔬 Engenharia de Prompts e "Cicatrizes"

Esta seção documenta o processo real de extração de conhecimento no NotebookLM: as perguntas estratégicas formuladas, as variações testadas e as dificuldades encontradas. É aqui que o raciocínio se torna visível.

---

### Bloco 1 — Mapeamento Conceitual

**Prompt v1 (raso):**
```
O que é análise de sentimentos?
```
**Problema identificado:** A resposta foi genérica demais, sem ancoragem no contexto de commodities ou bancos. Não aproveitou as fontes carregadas.

**Prompt v2 (refinado):**
```
Com base nas fontes carregadas, explique o que é análise de sentimentos aplicada
ao mercado financeiro e dê um exemplo prático de como ela poderia ser usada por
um banco para avaliar risco de crédito em operações de financiamento agrícola.
```
**Resultado:** O NotebookLM conectou o conceito ao FinBERT-PT-BR e citou o exemplo das atas do COPOM, gerando uma resposta com ancoragem real nas fontes.

**Lição aprendida (cicatriz):** Sempre especifique o contexto de aplicação e peça exemplo prático. Prompts abertos demais geram respostas enciclopédicas, não aplicadas.

---

### Bloco 2 — Aprofundamento Técnico

**Prompt v1 (confuso):**
```
Como funciona o BERT?
```
**Problema:** Resposta técnica densa, sem conexão com o caso de uso de commodities.

**Prompt v2 (contextualizado):**
```
De forma acessível para iniciantes, explique a diferença entre BERT e LSTM
para análise de sentimentos em notícias financeiras. Qual deles seria mais
adequado para um banco analisar manchetes diárias sobre soja e petróleo?
Justifique com base nas fontes.
```
**Resultado:** Resposta comparativa clara: LSTM captura sequência temporal de preços; BERT entende nuance e ironia em texto. Para notícias, BERT ganha. Para séries de preços combinadas com texto, usar os dois juntos.

**Lição aprendida (cicatriz):** A comparação A vs B força o modelo a estruturar o raciocínio. Pedir justificativa nas fontes evita respostas inventadas.

---

### Bloco 3 — Conexão com o Contexto Bancário

**Prompt estratégico:**
```
Com base nos artigos carregados, descreva 3 formas concretas como um banco
brasileiro (como Bradesco ou BNDES) poderia usar análise de sentimentos em
notícias para melhorar decisões de crédito rural. Para cada forma, indique:
(a) qual dado de entrada seria necessário,
(b) qual modelo de IA seria mais indicado,
(c) qual seria o risco de usar esse modelo sem validação humana.
```
**Resultado obtido:**
1. **Monitoramento de risco de inadimplência:** Alimentar modelo com manchetes da semana e alertar gerentes quando sentimento negativo sobre soja ultrapassar limiar — entrada: RSS de portais agrícolas; modelo: FinBERT-PT-BR; risco: falsos positivos em épocas de entressafra.
2. **Precificação dinâmica de seguros rurais:** Ajustar prêmios conforme sentimento do mercado — entrada: relatórios CONAB + notícias; modelo: BERT + regressão; risco: viés de cobertura midiática regional.
3. **Suporte à concessão de crédito:** Score de sentimento como variável adicional ao score de crédito tradicional — entrada: histórico de notícias 90 dias; modelo: LSTM-BERT híbrido; risco: discriminação indireta se manchetes forem enviesadas por região.

**Lição aprendida (cicatriz):** Estruturar o prompt com subitens (a), (b), (c) é equivalente a usar uma rubrica de avaliação. O modelo responde com a mesma estrutura pedida — útil para documentação e apresentação.

---

### Bloco 4 — Troubleshooting de Alucinação

**Situação:**
Ao perguntar sobre "o modelo mais preciso para prever preços de soja no Brasil", o NotebookLM citou um estudo com números de acurácia que não existiam nas fontes carregadas.

**Prompt corretivo:**
```
Você citou uma acurácia de 94% para o modelo X. Em qual das fontes carregadas
esse número aparece? Se não aparecer em nenhuma, reescreva a resposta
usando apenas informações verificáveis nas fontes disponíveis.
```
**Resultado:** O modelo reconheceu a alucinação e reescreveu a resposta com linguagem mais cautelosa ("os estudos sugerem que modelos deep learning tendem a superar ARIMA em horizontes curtos, mas os valores exatos variam conforme o conjunto de dados").

**Lição aprendida (cicatriz):** Sempre questione números específicos. Pedir que o modelo aponte a fonte exata é a melhor técnica anti-alucinação no NotebookLM.

---

### Banco de Prompts Reutilizáveis

Os prompts abaixo funcionam para qualquer tema no NotebookLM. Substitua os termos em colchetes pelo seu contexto.

```
# Prompt de Mapeamento Conceitual
"Explique [conceito] de forma acessível para iniciantes, com um exemplo prático
aplicado ao contexto de [área de aplicação], usando as fontes carregadas."

# Prompt de Comparação Técnica
"Compare [tecnologia A] e [tecnologia B] para a tarefa de [objetivo].
Qual seria mais adequada para [caso de uso específico]? Justifique com as fontes."

# Prompt de Aplicação Setorial
"Descreva [N] formas concretas como [tipo de organização] poderia usar
[tecnologia] para [objetivo de negócio]. Para cada uma, indique:
(a) dado de entrada necessário, (b) modelo indicado, (c) risco de uso sem validação."

# Prompt Anti-Alucinação
"Você mencionou [afirmação]. Em qual fonte carregada essa informação aparece?
Se não estiver em nenhuma, reescreva usando apenas dados verificáveis."

# Prompt de Síntese para Revisão
"Resuma os principais achados das fontes carregadas sobre [tema] em
no máximo 5 pontos, do mais básico ao mais avançado, como se fosse
explicar para alguém que nunca estudou o assunto."

# Prompt de Glossário
"Liste os 10 termos técnicos mais importantes do tema [assunto] que aparecem
nas fontes, com definição em linguagem simples e exemplo de uso prático em banco."
```

---

## 📖 Miniguia de Estudo — Entrega Final Consolidada

### Resumos Estruturados

#### O que é Análise de Sentimentos no contexto financeiro?

É uma técnica de PLN que classifica automaticamente textos (notícias, relatórios, tweets, atas) como **positivos**, **negativos** ou **neutros** em relação a um ativo ou mercado. Quando aplicada a commodities, permite que sistemas bancários monitorem o "humor" do mercado agrícola em tempo real, sem depender apenas de dados históricos de preço.

#### Como funciona na prática (fluxo simplificado)?

```
[Fonte de texto]        [Pré-processamento]     [Modelo de IA]        [Saída]
Notícias agrícolas  →   Tokenização/limpeza  →  FinBERT / LSTM    →  Score de sentimento
Atas do COPOM           Lemmatização            Classificação         Alerta de risco
Relatórios CONAB        Remoção de stopwords    Polaridade            Variável de crédito
```

#### Por que isso importa para bancos?

Segundo o estudo da ANPEC (2022), o Banco Central já usa NLP em atas do COPOM para previsões macroeconômicas. O FinBERT-PT-BR (SBC, 2023) demonstrou que modelos treinados em português capturam nuances do mercado brasileiro que modelos genéricos em inglês perdem. O artigo do arXiv (2025) mostra que a fusão de sinais de preço com notícias melhora a acurácia preditiva em choques de commodities.

#### Limitações importantes (visão crítica)

- Modelos de sentimentos são enviesados pelo viés da cobertura midiática — regiões menos cobertas pela imprensa têm menos dados.
- "Sentimento positivo" em notícias não implica causalidade no preço — é um sinal, não uma certeza.
- Modelos black-box como BERT têm baixa interpretabilidade, o que é um problema regulatório no setor bancário brasileiro (BACEN Resolução 4.557).
- Dados históricos de notícias em português com qualidade são escassos — o FinBERT-PT-BR foi treinado em corpus limitado.

---

### Glossário dos Principais Conceitos

| Termo | Definição Simples | Exemplo no Contexto Bancário |
|-------|-------------------|------------------------------|
| **PLN / NLP** | Área da IA que ensina computadores a entender linguagem humana | Ler mil notícias sobre soja em segundos e classificar o tom |
| **Tokenização** | Dividir um texto em unidades menores (palavras ou subpalavras) para o modelo processar | "Preço da soja cai" → ["preço", "da", "soja", "cai"] |
| **Lemmatização** | Reduzir palavras à sua forma base | "caindo", "caiu", "cairá" → "cair" |
| **Corpus** | Conjunto de textos usado para treinar ou consultar um modelo | Todas as notícias da Globo Rural dos últimos 5 anos |
| **BERT** | Modelo de linguagem do Google que entende contexto bidirecional | Diferencia "banco cresceu" (instituição) de "banco do rio" |
| **FinBERT** | Versão do BERT treinada em textos financeiros | Classifica "lucro abaixo do esperado" como sentimento negativo |
| **LSTM** | Rede neural que aprende padrões em sequências temporais | Identifica que preços de café sempre sobem antes da safra |
| **Polaridade** | Medida do sentimento: positivo (+1), neutro (0) ou negativo (-1) | Manchete sobre geada no Paraná → polaridade -0.87 |
| **Score de sentimento** | Número que resume o humor do mercado em um período | Média semanal de polaridade das notícias sobre milho |
| **Alucinação (IA)** | Quando o modelo gera informação falsa com confiança | Citar uma acurácia de 94% que não existe em nenhum estudo |
| **Stopwords** | Palavras sem valor semântico removidas no pré-processamento | "de", "o", "a", "que", "é" |
| **Fine-tuning** | Ajustar um modelo pré-treinado para uma tarefa específica | Treinar o FinBERT em notícias de commodities brasileiras |
| **Viés algorítmico** | Erro sistemático causado por dados de treino não representativos | Modelo treinado só em notícias do Sudeste falha no Norte |
| **Black-box** | Modelo cujo raciocínio interno não é interpretável | BERT decide, mas não explica por que classificou assim |
| **Interpretabilidade** | Capacidade de entender por que um modelo tomou uma decisão | Exigência regulatória do BACEN para modelos de crédito |

---

### Prompts Reutilizáveis para Revisão Futura

Use estes prompts no NotebookLM (ou em qualquer LLM) ao revisitar o tema:

**Para revisão rápida:**
```
"Em 3 parágrafos, resuma o que aprendi sobre análise de sentimentos
aplicada a commodities: conceito, como funciona e por que bancos usam."
```

**Para aprofundamento técnico:**
```
"Quais são as diferenças entre BERT e LSTM para análise de sentimentos
em séries financeiras? Quando usar cada um?"
```

**Para conexão com o mercado de trabalho:**
```
"Que habilidades técnicas um analista de dados em banco precisa ter
para trabalhar com NLP aplicado a risco de crédito rural?"
```

**Para avaliação crítica:**
```
"Quais são os 3 principais riscos de usar análise de sentimentos
como variável em modelos de crédito bancário? Como mitigá-los?"
```

**Para criação de apresentação:**
```
"Crie um roteiro de 5 slides explicando análise de sentimentos para
commodities para uma audiência de gerentes de banco sem formação técnica."
```

---

## 🗂️ Estrutura do Repositório

```
segundo-cerebro-commodities-nlp/
│
├── README.md                          ← Este arquivo (documento principal)
│
├── fontes/
│   ├── 01_finbert_ptbr_sbc_2023.pdf
│   ├── 02_pln_mercado_financeiro_2025.pdf
│   ├── 03_sentimentos_indicadores_2021.pdf
│   ├── 04_commodity_shocks_arxiv_2025.pdf
│   └── 05_bacen_narrativas_ml_2022.pdf
│
├── prompts/
│   └── banco_de_prompts.md            ← Todos os prompts documentados
│
└── miniguia/
    ├── resumos_estruturados.md
    └── glossario.md
```

---

## 🔗 Referências Completas

1. SILVA, R. et al. **FinBERT-PT-BR: Análise de Sentimentos em Textos Financeiros em Português**. SBC/BWAIF, 2023. [PDF](https://sol.sbc.org.br/index.php/bwaif/article/download/24960/24781/)

2. AUTORES. **PLN e Modelos Preditivos no Mercado Financeiro**. Revista Contemporânea, v.5, n.6, 2025. [PDF](https://ojs.revistacontemporanea.com/ojs/index.php/home/article/download/8335/5803/23717)

3. AUTORES. **Análise de Sentimentos e Indicadores Técnicos**. Brazilian Journals, 2021. [PDF](https://ojs.brazilianjournals.com.br/ojs/index.php/BJB/article/download/24482/19554/63003)

4. AUTORES. **Forecasting Commodity Price Shocks Using Agentic Generative AI**. arXiv, 2025. [PDF](https://arxiv.org/pdf/2508.06497)

5. PITTA, D.; NÓBREGA, C. **Narrativas do Banco Central e Previsões Macroeconômicas via ML**. ANPEC, 2022. [PDF](https://www.anpec.org.br/encontro/2022/submissao/files_I/i4-dcb2aec395e0613c42cef5c5f33ffe00.pdf)

---

*Projeto desenvolvido como parte do Bootcamp Bradesco · Desafio Prático NotebookLM · DIO Platform*

