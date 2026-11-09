# Prompts para pesquisa de palavras-chave no ChatGPT, Claude e Gemini

**Prompts de pesquisa de palavras-chave geram e organizam ideias de busca, mas não medem demanda: a IA não tem acesso a volume de busca. Os prompts desta página expandem um tema por intenção, agrupam uma lista exportada em clusters e levantam as perguntas que o público faz antes de comprar.**

São três prompts em português, cada um com objetivo, campos a preencher, o prompt pronto para copiar e o alerta do que a IA pode errar. Todos funcionam no ChatGPT, no Claude, no Gemini e em outras IAs de conversa. A biblioteca completa, com 24 prompts em 8 tarefas, está no [README](README.md).

*Por equipe de SEO da TRIWI, com revisão de Ricardo Martins, fundador. Publicado em 09/11/2026. Atualizado em 09/11/2026.*

## Índice

- [Prompt para expandir um tema em palavras-chave por intenção de busca](#prompt-para-expandir-um-tema-em-palavras-chave-por-intenção-de-busca)
- [Prompt para agrupar palavras-chave em clusters e páginas](#prompt-para-agrupar-palavras-chave-em-clusters-e-páginas)
- [Prompt para descobrir as perguntas que o público faz antes de comprar](#prompt-para-descobrir-as-perguntas-que-o-público-faz-antes-de-comprar)
- [O que a TRIWI tem sobre pesquisa de palavras-chave?](#o-que-a-triwi-tem-sobre-pesquisa-de-palavras-chave)
- [Perguntas frequentes](#perguntas-frequentes)

## Prompt para expandir um tema em palavras-chave por intenção de busca

**Objetivo:** Transformar um tema, produto ou serviço numa lista inicial de buscas reais, agrupadas por intenção, para depois validar o volume numa ferramenta de palavras-chave.

**Campos a preencher:** troque cada campo entre colchetes pela informação real antes de enviar.

| Campo | O que colocar |
|:---|:---|
| `[TEMA]` | O assunto, produto ou serviço que vai ser trabalhado |
| `[EMPRESA]` | Nome da empresa ou da marca |
| `[OFERTA]` | O que a empresa vende, em uma frase |
| `[PÚBLICO]` | Quem compra, com cargo, perfil ou momento de vida |
| `[LOCAL]` | País, estado ou cidade em que a empresa atende |

**Prompt pronto para copiar:**

```text
Você é um especialista em SEO no Brasil. Vou trabalhar o tema [TEMA] para a empresa [EMPRESA], que vende [OFERTA] para [PÚBLICO] em [LOCAL].

Liste as buscas que esse público faz no Google, em português do Brasil, do jeito que as pessoas digitam, incluindo abreviações, erros comuns e perguntas completas.

Agrupe as buscas em quatro intenções:
1. Informacional: a pessoa quer aprender ou entender.
2. Comparativa: está avaliando opções.
3. Transacional: quer comprar ou contratar.
4. Navegacional: procura uma marca ou um site específico.

Entregue uma tabela com as colunas: busca; intenção; etapa da jornada; tipo de página que responde melhor (artigo, página de produto, página de categoria, comparativo, ferramenta).

Regras:
1. Não invente volume de busca, dificuldade nem custo por clique. Você não tem esses dados.
2. Não repita a mesma busca com variação mínima de plural ou de ordem das palavras.
3. Marque com (validar) toda busca que você não tem segurança de que o público usa.
4. No fim, liste as dez buscas de cauda longa com mais chance de trazer cliente e explique cada escolha em uma frase.
```

> **O que a IA pode errar:** A IA não tem acesso a volume de busca e costuma inventar números quando alguém pede. Ela também sugere buscas que ninguém faz, escritas como um redator escreveria e não como o público digita. Valide cada busca no Planejador de palavras-chave do Google Ads ou na ferramenta que você usa, e só depois priorize.

**Na TRIWI:** [Guia de Palavras-chave e Intenção de Busca](https://triwi.com.br/guias/palavras-chave/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=pesquisa-de-palavras-chave), guia da TRIWI com o método completo.

<sub>Código do prompt: KW-01. Atualizado em 09/11/2026.</sub>

## Prompt para agrupar palavras-chave em clusters e páginas

**Objetivo:** Organizar uma lista exportada de uma ferramenta, já com volume, em grupos que viram páginas, e apontar onde duas páginas do site disputam a mesma busca.

**Campos a preencher:** troque cada campo entre colchetes pela informação real antes de enviar.

| Campo | O que colocar |
|:---|:---|
| `[FERRAMENTA]` | A ferramenta de onde saiu a lista, como Google Ads, Semrush ou Ahrefs |
| `[SITE]` | O domínio do site |
| `[PÁGINAS DO SITE]` | URL e título das páginas que já existem sobre o tema |
| `[LISTA DE PALAVRAS]` | A lista exportada, com uma palavra e o volume por linha |

**Prompt pronto para copiar:**

```text
Abaixo está uma lista de palavras-chave exportada de [FERRAMENTA], com o volume mensal no Brasil. O site é [SITE] e estas são as páginas que já existem:
[PÁGINAS DO SITE]

Lista de palavras-chave:
[LISTA DE PALAVRAS]

Tarefa:
1. Agrupe as palavras em clusters. Um cluster reúne buscas que uma única página consegue responder bem, porque têm a mesma intenção e pedem o mesmo tipo de resultado.
2. Para cada cluster, informe: nome do cluster; palavra principal (a de maior volume com a intenção certa); palavras secundárias; intenção; soma do volume informado na lista; página existente que deve responder ou "página nova".
3. Aponte os casos em que duas páginas existentes disputam o mesmo cluster (canibalização) e diga qual delas deveria ficar com ele.
4. Liste as palavras que ficaram fora de qualquer cluster e explique por quê.

Regras:
1. Use apenas os volumes da lista. Não estime os que faltam.
2. Quando não tiver segurança sobre a intenção de uma busca, diga que é preciso olhar a página de resultados do Google antes de decidir.
3. No fim, informe quantas palavras recebeu e quantas distribuiu, para eu conferir que nenhuma se perdeu.
```

> **O que a IA pode errar:** Agrupar por semelhança de palavra é o erro mais comum da IA: duas buscas parecidas podem pedir páginas diferentes, e duas buscas diferentes podem caber na mesma página. A prova está no Google mostrar resultados parecidos para as duas. Confira a página de resultados dos clusters mais importantes antes de criar ou fundir páginas. Listas longas também podem ser cortadas sem aviso: mande em blocos e confira se o total devolvido bate com o enviado.

**Na TRIWI:** [Organizador de palavras-chave em massa](https://triwi.com.br/ferramentas/organizador-de-palavras-chave-em-massa/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=pesquisa-de-palavras-chave), ferramenta gratuita da TRIWI, no navegador e sem cadastro.

<sub>Código do prompt: KW-02. Atualizado em 09/11/2026.</sub>

## Prompt para descobrir as perguntas que o público faz antes de comprar

**Objetivo:** Levantar dúvidas, objeções e comparações do público a partir de material real de atendimento e vendas, para virar pauta, FAQ e página.

**Campos a preencher:** troque cada campo entre colchetes pela informação real antes de enviar.

| Campo | O que colocar |
|:---|:---|
| `[EMPRESA]` | Nome da empresa ou da marca |
| `[OFERTA]` | O que a empresa vende, em uma frase |
| `[PÚBLICO]` | Quem compra |
| `[MATERIAL DOS CLIENTES]` | Trechos reais de atendimento, vendas, avaliações e comentários, sem dados pessoais |
| `[SETOR]` | O mercado em que a empresa atua |

**Prompt pronto para copiar:**

```text
Sou da empresa [EMPRESA], que vende [OFERTA] para [PÚBLICO]. Abaixo estão trechos reais de conversas com clientes (atendimento, vendas, avaliações e comentários):
[MATERIAL DOS CLIENTES]

Com base nesse material e no que você sabe sobre o mercado de [SETOR] no Brasil:
1. Liste as perguntas que essas pessoas fariam ao Google ou a uma IA antes de comprar, escritas como elas perguntariam.
2. Separe as perguntas em cinco grupos: dúvidas sobre o problema; dúvidas sobre a solução; comparações entre opções; objeções (valor, prazo, risco, confiança); dúvidas depois da compra.
3. Marque com (do material) as perguntas que saíram do material que colei e com (hipótese) as que você deduziu.
4. Indique, para cada grupo, que tipo de conteúdo responde melhor.

Não cite números de mercado nem estatísticas. Se precisar de um dado para responder, escreva "dado a confirmar".
```

> **O que a IA pode errar:** Sem material real, a IA devolve as perguntas genéricas que valem para qualquer empresa do setor, e todo concorrente que usar o mesmo prompt chega à mesma lista. O valor deste prompt está no material que você cola. Trate as perguntas marcadas como hipótese como pauta a validar, não como demanda comprovada.

**Na TRIWI:** [Skill: planejar conteúdos para 90 dias](https://triwi.com.br/skills/planejar-conteudos-para-90-dias/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=pesquisa-de-palavras-chave), skill da TRIWI para instalar no Claude ou no ChatGPT, com a versão completa desta tarefa.

<sub>Código do prompt: KW-03. Atualizado em 09/11/2026.</sub>

## O que a TRIWI tem sobre pesquisa de palavras-chave?

Os prompts desta página são a versão curta e aberta. Para o método completo, a TRIWI publica de graça:

| Recurso | Tipo | O que faz |
|:---|:---|:---|
| [Guia de Palavras-chave e Intenção de Busca](https://triwi.com.br/guias/palavras-chave/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=pesquisa-de-palavras-chave) | Guia | Como encontrar, priorizar e mapear palavras-chave pela intenção de quem busca |
| [Organizador de palavras-chave em massa](https://triwi.com.br/ferramentas/organizador-de-palavras-chave-em-massa/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=pesquisa-de-palavras-chave) | Ferramenta | Agrupa e organiza listas grandes de palavras-chave, sem cadastro |
| [Gerador de buscas avançadas (Dorks)](https://triwi.com.br/ferramentas/gerador-de-buscas-avancadas-dorks/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=pesquisa-de-palavras-chave) | Ferramenta | Monta operadores de busca do Google para investigar sites, concorrentes e oportunidades |
| [Skill: planejar conteúdos para 90 dias](https://triwi.com.br/skills/planejar-conteudos-para-90-dias/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=pesquisa-de-palavras-chave) | Skill | Transforma metas de negócio e dúvidas do público num plano de conteúdo de 90 dias |

## Perguntas frequentes

<details>
<summary><strong>O ChatGPT substitui uma ferramenta de palavras-chave?</strong></summary>

Não. Ele ajuda a pensar nas buscas e a organizar listas, mas não sabe quantas pessoas buscam cada termo nem como está a concorrência. Use a IA para gerar e agrupar ideias, e uma fonte de dados, como o Planejador de palavras-chave do Google Ads ou o Search Console, para decidir.
</details>

<details>
<summary><strong>Como saber se duas palavras-chave cabem na mesma página?</strong></summary>

Busque as duas no Google e compare os resultados. Se as páginas que aparecem são parecidas, uma página só atende as duas buscas; se são diferentes, cada busca pede a sua. A explicação está no guia aberto [Intenção de Busca](https://github.com/TRIWI-SEO/SEO-IA/blob/main/fundamentos-de-seo/intencao-de-busca-o-fundamento-que-muda-tudo-em-seo.md), da Base de Conhecimento da TRIWI.
</details>

**Ver também na Base de Conhecimento da TRIWI:** [Pesquisa de Palavras-chave](https://github.com/TRIWI-SEO/SEO-IA/blob/main/seo-de-conteudo/pesquisa-de-palavras-chave-como-encontrar-as-oportunidades-certas.md), [Intenção de Busca](https://github.com/TRIWI-SEO/SEO-IA/blob/main/fundamentos-de-seo/intencao-de-busca-o-fundamento-que-muda-tudo-em-seo.md), [Pilarização e Pulverização](https://github.com/TRIWI-SEO/SEO-IA/blob/main/seo-de-conteudo/pilarizacao-e-pulverizacao-a-estrategia-de-conteudo-que-gera-autoridade-topical.md).

**Ver também no Glossário da TRIWI:** [Pesquisa de palavras-chave](https://triwi.com.br/glossario/seo/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=pesquisa-de-palavras-chave#seo-pesquisa-de-palavras-chave), [Intenção de busca](https://triwi.com.br/glossario/seo/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=pesquisa-de-palavras-chave#seo-intencao-de-busca), [Cauda longa](https://triwi.com.br/glossario/seo/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=pesquisa-de-palavras-chave#seo-cauda-longa), [Canibalização de palavras-chave](https://triwi.com.br/glossario/seo/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=pesquisa-de-palavras-chave#seo-canibalizacao-de-palavras-chave), [Prompt](https://triwi.com.br/glossario/inteligencia-artificial/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=pesquisa-de-palavras-chave#ia-prompt).

[Voltar para a biblioteca completa](README.md)

---

<p align="center">
  <strong>Quer saber quais buscas trazem cliente para a sua empresa, no Google e nas IAs?</strong><br>
  <a href="https://triwi.com.br/contato/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=pesquisa-de-palavras-chave">Que tal um café com a TRIWI?</a>
</p>

<p align="center">
  <sub>Biblioteca publicada e mantida pela equipe da TRIWI, agência 100% especializada em SEO e Otimização para IAs.</sub>
</p>
