# Prompts para title e meta description de SEO no ChatGPT, Claude e Gemini

**O title e a meta description decidem se a pessoa clica no seu resultado. A IA escreve boas opções quando recebe a busca, o que a página entrega e a marca, mas erra a contagem de caracteres e inventa promessas. Os prompts desta página escrevem para uma página, reescrevem títulos com CTR baixo e geram textos em lote.**

São três prompts em português, cada um com objetivo, campos a preencher, o prompt pronto para copiar e o alerta do que a IA pode errar. Todos funcionam no ChatGPT, no Claude, no Gemini e em outras IAs de conversa. A biblioteca completa, com 24 prompts em 8 tarefas, está no [README](README.md).

*Por equipe de SEO da TRIWI, com revisão de Ricardo Martins, fundador. Publicado em 09/11/2026. Atualizado em 09/11/2026.*

## Índice

- [Prompt para escrever o title e a meta description de uma página](#prompt-para-escrever-o-title-e-a-meta-description-de-uma-página)
- [Prompt para reescrever títulos de páginas com CTR baixo](#prompt-para-reescrever-títulos-de-páginas-com-ctr-baixo)
- [Prompt para gerar títulos e descrições em lote, sem duplicar](#prompt-para-gerar-títulos-e-descrições-em-lote-sem-duplicar)
- [O que a TRIWI tem sobre títulos e descrições?](#o-que-a-triwi-tem-sobre-títulos-e-descrições)
- [Perguntas frequentes](#perguntas-frequentes)

## Prompt para escrever o title e a meta description de uma página

**Objetivo:** Criar opções de title e de meta description que descrevem a página com fidelidade, trazem a busca principal e convencem a clicar.

**Campos a preencher:** troque cada campo entre colchetes pela informação real antes de enviar.

| Campo | O que colocar |
|:---|:---|
| `[PALAVRA PRINCIPAL]` | A busca principal da página |
| `[RESUMO DA PÁGINA]` | O que a página entrega, em uma ou duas frases |
| `[MARCA]` | O nome da marca como deve aparecer no title |
| `[DIFERENCIAL]` | O que a página tem de específico e consegue provar |

**Prompt pronto para copiar:**

```text
Escreva o elemento title e a meta description da página descrita abaixo.

- Palavra-chave principal: [PALAVRA PRINCIPAL]
- O que a página entrega: [RESUMO DA PÁGINA]
- Marca: [MARCA]
- Diferencial que a página comprova: [DIFERENCIAL]

Regras para o title:
1. Comece pela palavra-chave principal ou por uma variação natural dela.
2. Descreva o conteúdo real da página, sem prometer o que ela não entrega.
3. Termine com a marca, separada por dois-pontos, vírgula ou barra vertical.
4. Mire em até 60 caracteres, para reduzir a chance de corte.

Regras para a meta description:
1. Resuma o que a pessoa encontra e por que vale clicar, em uma ou duas frases.
2. Mire em até 155 caracteres.
3. Não use aspas duplas, que quebram o atributo content quando não são escapadas.

Entregue cinco opções de cada, com a contagem de caracteres ao lado, e diga qual combinação você escolheria e por quê.
```

> **O que a IA pode errar:** A IA conta caracteres mal e costuma errar a contagem que ela mesma escreve ao lado; confira numa ferramenta. O Google não tem limite oficial de caracteres para title nem para meta description: corta pela largura da tela, pode reescrever o título a partir de outros elementos da página e usa outro trecho do texto como descrição quando acha melhor. Os 60 e os 155 caracteres são referência prática, não regra.

**Na TRIWI:** [Simulador de resultado no Google](https://triwi.com.br/ferramentas/simulador-de-resultado-no-google/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=titulos-e-meta-descriptions), ferramenta gratuita da TRIWI, no navegador e sem cadastro.

**Fontes oficiais citadas no alerta:** [Como o Google gera os links de título (Google Search Central)](https://developers.google.com/search/docs/appearance/title-link?hl=pt-br), [Como o Google gera os snippets (Google Search Central)](https://developers.google.com/search/docs/appearance/snippet?hl=pt-br), consultadas em 09/11/2026.

<sub>Código do prompt: TD-01. Atualizado em 09/11/2026.</sub>

## Prompt para reescrever títulos de páginas com CTR baixo

**Objetivo:** Encontrar páginas que aparecem muito e são pouco clicadas e propor títulos e descrições que respondam melhor à consulta.

**Campos a preencher:** troque cada campo entre colchetes pela informação real antes de enviar.

| Campo | O que colocar |
|:---|:---|
| `[SITE]` | O domínio do site |
| `[TABELA DO SEARCH CONSOLE]` | URL, consulta principal, impressões, cliques, CTR, posição média e title atual de cada página |
| `[MARCA]` | O nome da marca como deve aparecer no title |

**Prompt pronto para copiar:**

```text
Abaixo estão páginas do site [SITE] com muitas impressões e taxa de cliques (CTR) baixa no Search Console, com a consulta principal, a posição média e o title atual de cada uma:
[TABELA DO SEARCH CONSOLE]

Para cada página:
1. Diga por que o title atual pode estar perdendo o clique: não responde a consulta, é genérico, é cortado, é igual aos concorrentes ou promete pouco.
2. Escreva duas alternativas de title que respondam a consulta principal.
3. Escreva uma meta description nova.

Regras: não use números, anos ou promessas que a página não comprova. Não use caixa alta para chamar atenção nem emojis. Mantenha a marca [MARCA] no fim do title.
```

> **O que a IA pode errar:** CTR baixo nem sempre é culpa do título: posição média pior que a quinta, AI Overview, anúncios e outros recursos na página de resultados derrubam o clique sem relação com o texto, e a IA não vê nada disso na tabela. Priorize as páginas com posição boa e CTR abaixo do de páginas parecidas do mesmo site, e meça de novo algumas semanas depois da troca.

**Na TRIWI:** [Analisador de CSV do Search Console](https://triwi.com.br/ferramentas/analisador-de-csv-do-search-console/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=titulos-e-meta-descriptions), ferramenta gratuita da TRIWI, no navegador e sem cadastro.

<sub>Código do prompt: TD-02. Atualizado em 09/11/2026.</sub>

## Prompt para gerar títulos e descrições em lote, sem duplicar

**Objetivo:** Escrever title e meta description para muitas páginas parecidas (produtos, categorias, unidades) seguindo um padrão e sem repetir textos.

**Campos a preencher:** troque cada campo entre colchetes pela informação real antes de enviar.

| Campo | O que colocar |
|:---|:---|
| `[TIPO DE PÁGINA]` | Produto, categoria, unidade, cidade ou outro tipo |
| `[SITE]` | O domínio do site |
| `[LISTA DE PÁGINAS]` | Uma linha por página, com URL, nome e atributos |
| `[PADRÃO DO TITLE]` | O modelo do title, como nome do produto, dois-pontos, atributo principal e a marca no fim |

**Prompt pronto para copiar:**

```text
Abaixo está uma lista de páginas do tipo [TIPO DE PÁGINA] do site [SITE], com URL, nome e atributos principais de cada uma:
[LISTA DE PÁGINAS]

Escreva um title e uma meta description para cada página, seguindo este padrão:
- Title: [PADRÃO DO TITLE]
- Meta description: uma frase com o que a página tem de específico, usando os atributos da lista.

Regras:
1. Nenhum title e nenhuma descrição pode repetir outro da lista.
2. Use só os atributos que estão na lista. Não invente característica, condição comercial ou prazo.
3. Devolva uma tabela com as colunas: URL; title; caracteres do title; meta description; caracteres da descrição.
4. Devolva exatamente o mesmo número de linhas que recebeu. Se pular alguma, avise.
```

> **O que a IA pode errar:** Em listas longas a IA pula linhas, repete descrições quase iguais e, perto do fim, começa a inventar atributos. Mande em lotes de cinquenta a cem páginas, confira se o número de linhas devolvidas bate com o enviado e passe o resultado por um auditor de duplicidade antes de subir.

**Na TRIWI:** [Auditor de títulos e descrições em massa](https://triwi.com.br/ferramentas/auditor-de-titulos-e-descricoes-em-massa/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=titulos-e-meta-descriptions), ferramenta gratuita da TRIWI, no navegador e sem cadastro.

<sub>Código do prompt: TD-03. Atualizado em 09/11/2026.</sub>

## O que a TRIWI tem sobre títulos e descrições?

Os prompts desta página são a versão curta e aberta. Para o método completo, a TRIWI publica de graça:

| Recurso | Tipo | O que faz |
|:---|:---|:---|
| [Simulador de resultado no Google](https://triwi.com.br/ferramentas/simulador-de-resultado-no-google/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=titulos-e-meta-descriptions) | Ferramenta | Mostra como título, URL e descrição devem aparecer no resultado antes de publicar |
| [Auditor de títulos e descrições em massa](https://triwi.com.br/ferramentas/auditor-de-titulos-e-descricoes-em-massa/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=titulos-e-meta-descriptions) | Ferramenta | Revisa títulos e meta descriptions de muitas páginas: tamanho, duplicidade e ausência |
| [Analisador de CSV do Search Console](https://triwi.com.br/ferramentas/analisador-de-csv-do-search-console/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=titulos-e-meta-descriptions) | Ferramenta | Lê a exportação do Search Console para analisar consultas e páginas fora da interface |
| [Guia de SEO](https://triwi.com.br/guias/seo/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=titulos-e-meta-descriptions) | Guia | O que é SEO, como funciona e como gerar resultado de negócio com busca orgânica |

## Perguntas frequentes

<details>
<summary><strong>Qual o tamanho ideal do title e da meta description?</strong></summary>

O Google não define limite de caracteres para nenhum dos dois: ele corta o texto pela largura da tela. Como referência prática, títulos de até 60 caracteres e descrições de até 155 costumam aparecer inteiros. Confira no [Simulador de resultado no Google](https://triwi.com.br/ferramentas/simulador-de-resultado-no-google/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=titulos) da TRIWI.
</details>

<details>
<summary><strong>Por que o Google mostra um título diferente do que eu escrevi?</strong></summary>

Porque ele gera o link de título automaticamente e pode usar o H1, outros títulos da página, textos de links e outros elementos quando acha que o title não descreve bem a página. Um title fiel ao conteúdo e coerente com o H1 reduz a reescrita.
</details>

**Ver também na Base de Conhecimento da TRIWI:** [SEO On-Page](https://github.com/TRIWI-SEO/SEO-IA/blob/main/fundamentos-de-seo/seo-on-page-otimizacao-dentro-do-seu-site.md), [Google Search Console: Guia Completo para SEO](https://github.com/TRIWI-SEO/SEO-IA/blob/main/metricas-e-ferramentas/google-search-console-guia-completo-para-seo.md), [Métricas de SEO que Importam](https://github.com/TRIWI-SEO/SEO-IA/blob/main/metricas-e-ferramentas/metricas-de-seo-que-importam-kpis-focados-em-negocio.md).

**Ver também no Glossário da TRIWI:** [Title tag](https://triwi.com.br/glossario/seo/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=titulos-e-meta-descriptions#seo-title-tag), [Meta description](https://triwi.com.br/glossario/seo/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=titulos-e-meta-descriptions#seo-meta-description), [CTR](https://triwi.com.br/glossario/seo/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=titulos-e-meta-descriptions#seo-ctr), [Snippet](https://triwi.com.br/glossario/seo/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=titulos-e-meta-descriptions#seo-snippet), [SERP](https://triwi.com.br/glossario/seo/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=titulos-e-meta-descriptions#seo-serp).

[Voltar para a biblioteca completa](README.md)

---

<p align="center">
  <strong>Quer mais cliques do Google e mais citações nas IAs?</strong><br>
  <a href="https://triwi.com.br/contato/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=titulos-e-meta-descriptions">Que tal um café com a TRIWI?</a>
</p>

<p align="center">
  <sub>Biblioteca publicada e mantida pela equipe da TRIWI, agência 100% especializada em SEO e Otimização para IAs.</sub>
</p>
