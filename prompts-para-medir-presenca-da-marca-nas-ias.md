# Prompts para medir a presença da marca nas IAs (Share of Model)

**Para medir a presença da marca nas IAs, faça sempre o mesmo conjunto de perguntas ao ChatGPT, Gemini, Claude, Perplexity e Copilot, registre quem é citado em cada resposta e calcule o Share of Model, a fatia das respostas em que a marca aparece. Os prompts desta página montam as perguntas, registram as respostas e consolidam o mês.**

São três prompts em português, cada um com objetivo, campos a preencher, o prompt pronto para copiar e o alerta do que a IA pode errar. Todos funcionam no ChatGPT, no Claude, no Gemini e em outras IAs de conversa. A biblioteca completa, com 24 prompts em 8 tarefas, está no [README](README.md).

*Por equipe de SEO da TRIWI, com revisão de Ricardo Martins, fundador. Publicado em 09/11/2026. Atualizado em 09/11/2026.*

## Índice

- [Prompt para montar o conjunto de perguntas que mede a marca nas IAs](#prompt-para-montar-o-conjunto-de-perguntas-que-mede-a-marca-nas-ias)
- [Prompt para registrar a resposta de uma IA em formato de tabela](#prompt-para-registrar-a-resposta-de-uma-ia-em-formato-de-tabela)
- [Prompt para consolidar o Share of Model do mês](#prompt-para-consolidar-o-share-of-model-do-mês)
- [O que a TRIWI tem sobre medição de presença nas IAs?](#o-que-a-triwi-tem-sobre-medição-de-presença-nas-ias)
- [Perguntas frequentes](#perguntas-frequentes)

## Prompt para montar o conjunto de perguntas que mede a marca nas IAs

**Objetivo:** Criar a lista fixa de perguntas que o público faz às IAs, separando perguntas com e sem marca, para medir o Share of Model todo mês.

**Campos a preencher:** troque cada campo entre colchetes pela informação real antes de enviar.

| Campo | O que colocar |
|:---|:---|
| `[MARCA]` | O nome da marca medida |
| `[OFERTA]` | O que a empresa vende |
| `[PÚBLICO]` | Quem compra |
| `[LOCAL]` | País, estado ou cidade em que a empresa atende |
| `[CONCORRENTES]` | As marcas concorrentes que entram na medição |

**Prompt pronto para copiar:**

```text
Quero medir com que frequência a marca [MARCA] aparece nas respostas de IAs como ChatGPT, Gemini, Claude, Perplexity e Copilot. A empresa vende [OFERTA] para [PÚBLICO] em [LOCAL], e os concorrentes que queremos acompanhar são: [CONCORRENTES].

Monte um conjunto de 30 a 50 perguntas, em português do Brasil, que esse público faria a uma IA, distribuídas em cinco categorias:
1. Descoberta: pedidos de indicação, como "quais são as melhores opções de ...", sem citar marca.
2. Problema: perguntas sobre a dor, sem pedir indicação.
3. Comparação: entre tipos de solução e entre as marcas citadas.
4. Decisão: critérios, riscos e como escolher.
5. Marca: perguntas que citam a marca [MARCA] pelo nome (reputação, avaliações, alternativas).

Para cada pergunta, indique a categoria e se ela cita marca ou não. Escreva como uma pessoa escreve para a IA, em linguagem natural, e não como palavra-chave.
```

> **O que a IA pode errar:** Um conjunto de perguntas só serve se for repetido igual, mês após mês. Revise a lista, congele e não deixe a IA reescrever as perguntas a cada rodada. Perguntas que citam a marca medem reputação, não descoberta: mantenha as duas separadas, senão o resultado parece melhor do que é.

**Na TRIWI:** [Share of Model: como medir a presença da sua marca nas IAs](https://github.com/TRIWI-SEO/SEO-IA/blob/main/geo-seo-para-ia/share-of-model-como-medir-a-presenca-da-sua-marca-nas-ias.md), guia aberto da Base de Conhecimento da TRIWI no GitHub.

<sub>Código do prompt: MED-01. Atualizado em 09/11/2026.</sub>

## Prompt para registrar a resposta de uma IA em formato de tabela

**Objetivo:** Extrair de uma resposta real de IA as marcas citadas, a posição, o tipo de menção e as fontes, numa linha de tabela pronta para a planilha de medição.

**Campos a preencher:** troque cada campo entre colchetes pela informação real antes de enviar.

| Campo | O que colocar |
|:---|:---|
| `[NOME DA IA]` | A IA que respondeu, com o modelo, se aparecer |
| `[DATA]` | O dia da coleta |
| `[PERGUNTA]` | A pergunta exatamente como foi feita, copiada do conjunto fixo |
| `[RESPOSTA COLADA]` | A resposta completa, com as fontes que ela mostrou |
| `[MARCA]` | A marca medida |

**Prompt pronto para copiar:**

```text
Abaixo está a resposta que a IA [NOME DA IA] deu em [DATA] à pergunta "[PERGUNTA]", coletada numa conversa nova, sem memória e sem personalização:
[RESPOSTA COLADA]

Extraia, sem interpretar além do texto:
1. Todas as marcas e empresas citadas, na ordem em que aparecem.
2. Para cada uma: a posição na resposta; se foi recomendada, apenas mencionada ou citada de forma negativa; o trecho exato.
3. As fontes ou links que a resposta mostrou, com o domínio de cada um.
4. Se a marca [MARCA] aparece: sim ou não, em que posição e com que tom.

Devolva uma linha de tabela por marca citada, com as colunas: data; IA; pergunta; marca; posição; tipo de menção; trecho; fonte citada.
Se uma informação não estiver na resposta, escreva n/d.
```

> **O que a IA pode errar:** Não peça à IA para dizer se ela costuma citar a sua marca: ela não tem registro das próprias respostas e vai responder o que parece plausível. A medição é feita colhendo respostas reais, numa conversa nova e sem memória, e depois extraindo os dados. As respostas variam de uma consulta para outra, então rode cada pergunta mais de uma vez e trabalhe com a frequência, não com uma resposta isolada.

**Na TRIWI:** [Guia de GEO: Otimização para IAs](https://triwi.com.br/guias/geo/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=medir-presenca-da-marca-nas-ias), guia da TRIWI com o método completo.

<sub>Código do prompt: MED-02. Atualizado em 09/11/2026.</sub>

## Prompt para consolidar o Share of Model do mês

**Objetivo:** Calcular, a partir das respostas coletadas, a fatia de respostas em que cada marca aparece, por IA e por tipo de pergunta, e comparar com o mês anterior.

**Campos a preencher:** troque cada campo entre colchetes pela informação real antes de enviar.

| Campo | O que colocar |
|:---|:---|
| `[MÊS]` | O mês da coleta |
| `[MARCA]` | A marca medida |
| `[TABELA DO MÊS]` | As linhas registradas no mês, no formato do prompt de registro |
| `[TABELA DO MÊS ANTERIOR]` | As linhas do mês anterior, no mesmo formato |

**Prompt pronto para copiar:**

```text
Abaixo está a tabela com todas as respostas coletadas em [MÊS] para o conjunto de perguntas da marca [MARCA], com uma linha por marca citada em cada resposta:
[TABELA DO MÊS]

E a tabela do mês anterior, no mesmo formato:
[TABELA DO MÊS ANTERIOR]

Calcule e mostre em tabela:
1. O Share of Model de cada marca: número de respostas em que a marca aparece dividido pelo total de respostas, por IA e no geral.
2. O mesmo cálculo separado entre perguntas que citam marca e perguntas sem marca.
3. A posição média de cada marca quando ela aparece.
4. Os domínios mais citados como fonte e quantas vezes cada um aparece.
5. A variação de cada indicador em relação ao mês anterior.

Mostre a fórmula de cada cálculo e os totais usados, para eu conferir. Depois, liste três observações que os números sustentam e três hipóteses que precisam de mais dados.
```

> **O que a IA pode errar:** A IA erra conta, principalmente em tabela longa, e erra com convicção. Use a resposta para a leitura, mas refaça os cálculos numa planilha a partir da tabela original. E não compare meses em que o conjunto de perguntas, as IAs ou a forma de coleta mudaram: a variação vira efeito do método, não da marca.

**Na TRIWI:** [Guia de Métricas de SEO e IA](https://triwi.com.br/guias/metricas-de-seo/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=medir-presenca-da-marca-nas-ias), guia da TRIWI com o método completo.

<sub>Código do prompt: MED-03. Atualizado em 09/11/2026.</sub>

## O que a TRIWI tem sobre medição de presença nas IAs?

Os prompts desta página são a versão curta e aberta. Para o método completo, a TRIWI publica de graça:

| Recurso | Tipo | O que faz |
|:---|:---|:---|
| [Guia de Métricas de SEO e IA](https://triwi.com.br/guias/metricas-de-seo/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=medir-presenca-da-marca-nas-ias) | Guia | Quais indicadores acompanhar para ligar SEO e GEO a resultado de negócio |
| [Guia de GEO: Otimização para IAs](https://triwi.com.br/guias/geo/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=medir-presenca-da-marca-nas-ias) | Guia | Como a marca passa a ser citada por ChatGPT, Gemini, Claude, Perplexity e AI Overviews |
| [Share of Model: como medir a presença da sua marca nas IAs](https://github.com/TRIWI-SEO/SEO-IA/blob/main/geo-seo-para-ia/share-of-model-como-medir-a-presenca-da-sua-marca-nas-ias.md) | Base de Conhecimento | O que é o Share of Model e como montar a medição |
| [Atualizações do Google e das IAs](https://triwi.com.br/atualizacoes/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=medir-presenca-da-marca-nas-ias) | Atualizações | Linhas do tempo das mudanças do Google e de seis IAs, para explicar variações de um mês para outro |

## Perguntas frequentes

<details>
<summary><strong>Dá para perguntar ao ChatGPT se ele cita a minha marca?</strong></summary>

Dá para perguntar, mas a resposta não vale como medição. A IA não guarda registro das respostas que deu a outras pessoas e responde o que parece plausível. A medição só funciona colhendo respostas reais, em conversa nova, com o mesmo conjunto de perguntas.
</details>

<details>
<summary><strong>Com que frequência medir?</strong></summary>

Uma vez por mês é o ritmo mais comum, sempre com as mesmas perguntas, nas mesmas IAs e com a mesma forma de coleta. Se o método mudar, comece uma série nova em vez de comparar com a antiga.
</details>

<details>
<summary><strong>Preciso de ferramenta paga para medir o Share of Model?</strong></summary>

Não para começar: uma planilha e os três prompts desta página resolvem a medição manual de algumas dezenas de perguntas. Ferramentas de monitoramento automatizam a coleta e ajudam quando o volume cresce.
</details>

**Ver também na Base de Conhecimento da TRIWI:** [Share of Model](https://github.com/TRIWI-SEO/SEO-IA/blob/main/geo-seo-para-ia/share-of-model-como-medir-a-presenca-da-sua-marca-nas-ias.md), [Métricas de SEO que Importam](https://github.com/TRIWI-SEO/SEO-IA/blob/main/metricas-e-ferramentas/metricas-de-seo-que-importam-kpis-focados-em-negocio.md), [Otimização para Perplexity, Claude e Outras IAs de Busca](https://github.com/TRIWI-SEO/SEO-IA/blob/main/geo-seo-para-ia/otimizacao-para-perplexity-claude-e-outras-ias-de-busca.md), [O Que é GEO](https://github.com/TRIWI-SEO/SEO-IA/blob/main/o-que-e-geo-generative-engine-optimization-guia-completo.md).

**Ver também no Glossário da TRIWI:** [Share of Model](https://triwi.com.br/glossario/seo/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=medir-presenca-da-marca-nas-ias#seo-share-of-model), [Citação em IAs](https://triwi.com.br/glossario/seo/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=medir-presenca-da-marca-nas-ias#seo-citacao-em-ias), [GEO](https://triwi.com.br/glossario/seo/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=medir-presenca-da-marca-nas-ias#seo-geo), [LLM](https://triwi.com.br/glossario/inteligencia-artificial/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=medir-presenca-da-marca-nas-ias#ia-llm), [Alucinação](https://triwi.com.br/glossario/inteligencia-artificial/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=medir-presenca-da-marca-nas-ias#ia-alucinacao).

[Voltar para a biblioteca completa](README.md)

---

<p align="center">
  <strong>Quer saber quanto a sua marca aparece nas IAs, comparada aos concorrentes?</strong><br>
  <a href="https://triwi.com.br/contato/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=medir-presenca-da-marca-nas-ias">Que tal um café com a TRIWI?</a>
</p>

<p align="center">
  <sub>Biblioteca publicada e mantida pela equipe da TRIWI, agência 100% especializada em SEO e Otimização para IAs.</sub>
</p>
