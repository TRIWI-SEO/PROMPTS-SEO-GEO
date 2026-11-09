# Prompts para otimizar conteúdo e ser citado por IAs (GEO)

**Para ser citado por ChatGPT, Gemini, Claude, Perplexity e AI Overviews, o conteúdo precisa responder de forma direta, em trechos que funcionam sozinhos, com a entidade clara e fonte em cada afirmação. Os prompts desta página reescrevem a abertura, diagnosticam a página e reorganizam o texto em blocos extraíveis.**

São três prompts em português, cada um com objetivo, campos a preencher, o prompt pronto para copiar e o alerta do que a IA pode errar. Todos funcionam no ChatGPT, no Claude, no Gemini e em outras IAs de conversa. A biblioteca completa, com 24 prompts em 8 tarefas, está no [README](README.md).

*Por equipe de SEO da TRIWI, com revisão de Ricardo Martins, fundador. Publicado em 09/11/2026. Atualizado em 09/11/2026.*

## Índice

- [Prompt para reescrever a abertura e virar resposta citável](#prompt-para-reescrever-a-abertura-e-virar-resposta-citável)
- [Prompt para diagnosticar por que um conteúdo não é citado pelas IAs](#prompt-para-diagnosticar-por-que-um-conteúdo-não-é-citado-pelas-ias)
- [Prompt para transformar um texto corrido em blocos extraíveis](#prompt-para-transformar-um-texto-corrido-em-blocos-extraíveis)
- [O que a TRIWI tem sobre conteúdo citado por IAs?](#o-que-a-triwi-tem-sobre-conteúdo-citado-por-ias)
- [Perguntas frequentes](#perguntas-frequentes)

## Prompt para reescrever a abertura e virar resposta citável

**Objetivo:** Fazer os primeiros parágrafos de um conteúdo responderem a pergunta de forma completa e autocontida, do jeito que buscadores e IAs extraem.

**Campos a preencher:** troque cada campo entre colchetes pela informação real antes de enviar.

| Campo | O que colocar |
|:---|:---|
| `[PERGUNTA]` | A pergunta, escrita como o público pergunta à IA |
| `[TEXTO]` | O conteúdo atual, ou pelo menos os primeiros parágrafos |
| `[FONTES]` | Links ou trechos das fontes que sustentam os números do texto |
| `[MARCA]` | Nome da marca que publica o conteúdo |

**Prompt pronto para copiar:**

```text
Reescreva a abertura do conteúdo abaixo para que ela possa ser extraída e citada por uma IA ou por um AI Overview como resposta à pergunta [PERGUNTA].

Texto atual:
[TEXTO]

Fontes que podem ser usadas:
[FONTES]

Regras:
1. As duas primeiras frases respondem a pergunta de forma completa, sem introdução e sem depender do resto do texto.
2. Use o nome da entidade (marca, produto, conceito) em vez de pronomes como "ele" ou "isso".
3. Inclua uma definição, um critério ou um número, mas só se ele estiver no texto atual ou nas fontes acima.
4. Logo depois, escreva uma frase de contexto: para quem vale, em que condição e desde quando.
5. Mantenha a voz da marca [MARCA] e o português do Brasil.

Entregue três versões e diga, para cada uma, o que ela prioriza.
```

> **O que a IA pode errar:** Para soar mais citável, a IA acrescenta números, anos e porcentagens que não estavam no texto. Uma abertura com dado inventado é justamente o trecho que outra IA vai copiar, com o nome da sua marca ao lado. Compare cada número da versão nova com a fonte original antes de publicar.

**Na TRIWI:** [Skill: criar conteúdo para SEO e IA](https://triwi.com.br/skills/criar-conteudo-para-seo-e-ia/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=ser-citado-por-ias), skill da TRIWI para instalar no Claude ou no ChatGPT, com a versão completa desta tarefa.

<sub>Código do prompt: GEO-01. Atualizado em 09/11/2026.</sub>

## Prompt para diagnosticar por que um conteúdo não é citado pelas IAs

**Objetivo:** Avaliar uma página com os critérios que tornam um texto uma boa fonte para respostas de IA e listar as mudanças que mais pesam.

**Campos a preencher:** troque cada campo entre colchetes pela informação real antes de enviar.

| Campo | O que colocar |
|:---|:---|
| `[PERGUNTA]` | A pergunta para a qual a página deveria ser citada |
| `[TEXTO]` | O conteúdo completo da página |

**Prompt pronto para copiar:**

```text
Analise o conteúdo abaixo como um sistema de busca com IA faria ao decidir se usa a página como fonte para responder à pergunta [PERGUNTA].

Texto:
[TEXTO]

Avalie cada item em uma linha, com o trecho que justifica:
1. A resposta à pergunta aparece de forma direta e autocontida? Em que parágrafo?
2. Há trechos que funcionam sozinhos, fora do contexto da página (definições, listas, tabelas, passo a passo)?
3. As afirmações importantes têm fonte, data e recorte?
4. A entidade principal está nomeada com clareza e sempre do mesmo jeito?
5. Há informação própria que outras páginas não têm (dado, caso, método, opinião de especialista)?
6. Há trechos vagos, promocionais ou genéricos que uma IA descartaria?

Depois, liste as cinco mudanças com mais chance de tornar a página uma fonte útil, em ordem.

Não afirme que a página será citada: nenhum ajuste garante citação.
```

> **O que a IA pode errar:** A IA não sabe como o ChatGPT, o Gemini ou o Perplexity escolhem fontes: ela descreve boas práticas plausíveis, não o funcionamento interno de cada sistema. Também não sabe se a página está indexada ou se o robô daquela IA tem acesso ao site. Para os AI Overviews, o Google diz que a página precisa estar indexada e apta a aparecer com snippet; confirme isso e o acesso dos robôs antes de reescrever o texto.

**Na TRIWI:** [Checklist de SEO para IA](https://triwi.com.br/checklist-de-seo-para-ia-50-pontos-para-dominar-o-geo/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=ser-citado-por-ias), checklist gratuito da TRIWI.

**Fonte oficial citada no alerta:** [Recursos de IA e seu site (Google Search Central)](https://developers.google.com/search/docs/appearance/ai-features?hl=pt-br), consultada em 09/11/2026.

<sub>Código do prompt: GEO-02. Atualizado em 09/11/2026.</sub>

## Prompt para transformar um texto corrido em blocos extraíveis

**Objetivo:** Reorganizar um conteúdo, sem mudar a informação, em perguntas, respostas curtas, tabelas e listas que buscadores e IAs conseguem extrair.

**Campos a preencher:** troque cada campo entre colchetes pela informação real antes de enviar.

| Campo | O que colocar |
|:---|:---|
| `[PÚBLICO]` | Quem lê o conteúdo |
| `[TEXTO]` | O conteúdo completo, como está publicado |

**Prompt pronto para copiar:**

```text
Reorganize o conteúdo abaixo, sem mudar a informação, para que ele fique fácil de extrair por buscadores e IAs. O público é [PÚBLICO].

Texto:
[TEXTO]

Faça:
1. Proponha títulos H2 e H3 em formato de pergunta real que esse público faria.
2. Abaixo de cada título, comece pela resposta em uma ou duas frases.
3. Transforme comparações em tabela, sequências em lista numerada e critérios em lista com marcadores.
4. Escreva um resumo de até cinco frases para o topo da página.
5. Aponte os trechos repetidos que podem sair.

Regras: não acrescente informação nova. Se faltar informação para responder um título, escreva (falta: o que falta) no lugar, para o autor completar.
```

> **O que a IA pode errar:** Ao reorganizar, a IA resume demais e some com nuances, exceções e ressalvas, que são justamente o que dá precisão ao texto. Também monta tabelas com células preenchidas por suposição. Leia o texto original e o novo lado a lado e confira que nenhuma condição ou exceção desapareceu.

**Na TRIWI:** [Guia de GEO: Otimização para IAs](https://triwi.com.br/guias/geo/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=ser-citado-por-ias), guia da TRIWI com o método completo.

<sub>Código do prompt: GEO-03. Atualizado em 09/11/2026.</sub>

## O que a TRIWI tem sobre conteúdo citado por IAs?

Os prompts desta página são a versão curta e aberta. Para o método completo, a TRIWI publica de graça:

| Recurso | Tipo | O que faz |
|:---|:---|:---|
| [Skill: criar conteúdo para SEO e IA](https://triwi.com.br/skills/criar-conteudo-para-seo-e-ia/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=ser-citado-por-ias) | Skill | Conduz a escrita de artigos, guias e páginas pensados para a busca e para as respostas de IA |
| [Guia de GEO: Otimização para IAs](https://triwi.com.br/guias/geo/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=ser-citado-por-ias) | Guia | Como a marca passa a ser citada por ChatGPT, Gemini, Claude, Perplexity e AI Overviews |
| [Checklist de SEO para IA](https://triwi.com.br/checklist-de-seo-para-ia-50-pontos-para-dominar-o-geo/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=ser-citado-por-ias) | Checklist | Mais de 50 pontos para revisar a presença de um site nas respostas das IAs |
| [Cheat sheet: os 10 fatores que fazem você ser citado por IAs](https://triwi.com.br/cheat-sheet-avancado-os-10-fatores-comprovados-que-fazem-voce-ser-citado-por-ias/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=ser-citado-por-ias) | Checklist | Resumo dos fatores que mais pesam para uma marca ser citada nas respostas de IA |

## Perguntas frequentes

<details>
<summary><strong>Existe prompt que garante citação no ChatGPT?</strong></summary>

Não. Nenhum texto garante citação: a IA escolhe as fontes a cada resposta, a partir do que encontra e do que já sabe sobre a marca. O que estes prompts fazem é dar à página as características de uma boa fonte. O efeito se mede com o mesmo conjunto de perguntas, mês após mês, como em [Prompts para medir a presença da marca nas IAs](prompts-para-medir-presenca-da-marca-nas-ias.md).
</details>

<details>
<summary><strong>Preciso de marcação especial ou de llms.txt para aparecer nos AI Overviews?</strong></summary>

Não, segundo a documentação [Recursos de IA e seu site](https://developers.google.com/search/docs/appearance/ai-features?hl=pt-br): a página precisa estar indexada e apta a aparecer com snippet, sem requisito técnico extra. Como a TRIWI trata o tema está no [Guia de GEO](https://triwi.com.br/guias/geo/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=citado-por-ias).
</details>

**Ver também na Base de Conhecimento da TRIWI:** [Conteúdo Citável](https://github.com/TRIWI-SEO/SEO-IA/blob/main/geo-seo-para-ia/conteudo-citavel-como-escrever-para-ser-referenciado-por-llms.md), [Como as LLMs Decidem o Que Citar](https://github.com/TRIWI-SEO/SEO-IA/blob/main/geo-seo-para-ia/como-as-llms-decidem-o-que-citar-arquitetura-de-informacao-para-ia.md), [SEO para IA: Como Aparecer nas Respostas do ChatGPT, Gemini e Claude](https://github.com/TRIWI-SEO/SEO-IA/blob/main/geo-seo-para-ia/seo-para-ia-como-aparecer-nas-respostas-do-chatgpt-gemini-e-claude.md), [AI Overviews: O Que São e Como Otimizar](https://github.com/TRIWI-SEO/SEO-IA/blob/main/geo-seo-para-ia/ai-overviews-o-que-sao-e-como-otimizar.md).

**Ver também no Glossário da TRIWI:** [GEO](https://triwi.com.br/glossario/seo/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=ser-citado-por-ias#seo-geo), [Citação em IAs](https://triwi.com.br/glossario/seo/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=ser-citado-por-ias#seo-citacao-em-ias), [AI Overviews](https://triwi.com.br/glossario/seo/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=ser-citado-por-ias#seo-ai-overviews), [Entidade](https://triwi.com.br/glossario/seo/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=ser-citado-por-ias#seo-entidade), [Query fan-out](https://triwi.com.br/glossario/seo/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=ser-citado-por-ias#seo-query-fan-out), [Grounding](https://triwi.com.br/glossario/inteligencia-artificial/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=ser-citado-por-ias#ia-grounding).

[Voltar para a biblioteca completa](README.md)

---

<p align="center">
  <strong>Quando alguém pergunta à IA sobre o seu mercado, ela cita a sua empresa?</strong><br>
  <a href="https://triwi.com.br/contato/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=ser-citado-por-ias">Que tal um café com a TRIWI?</a>
</p>

<p align="center">
  <sub>Biblioteca publicada e mantida pela equipe da TRIWI, agência 100% especializada em SEO e Otimização para IAs.</sub>
</p>
