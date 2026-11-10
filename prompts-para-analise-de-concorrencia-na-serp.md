# Prompts para análise de concorrência na SERP do Google

**Analisar a concorrência na SERP é ler quem aparece na página de resultados do Google, por quê e o que falta nela. A IA faz bem essa leitura quando recebe os resultados coletados, com data e local; de memória, descreve uma SERP que não existe. Os prompts desta página leem uma SERP, comparam páginas e mapeiam domínios.**

São três prompts em português, cada um com objetivo, campos a preencher, o prompt pronto para copiar e o alerta do que a IA pode errar. Todos funcionam no ChatGPT, no Claude, no Gemini e em outras IAs de conversa. A biblioteca completa, com 30 prompts em 10 tarefas, está no [README](README.md).

*Por equipe de SEO da TRIWI, com revisão de Ricardo Martins, fundador. Publicado em 09/11/2026. Atualizado em 09/11/2026.*

## Índice

- [Prompt para ler a página de resultados de uma busca](#prompt-para-ler-a-página-de-resultados-de-uma-busca)
- [Prompt para comparar a sua página com as que estão à frente](#prompt-para-comparar-a-sua-página-com-as-que-estão-à-frente)
- [Prompt para mapear quais sites dominam um grupo de buscas](#prompt-para-mapear-quais-sites-dominam-um-grupo-de-buscas)
- [Qual o próximo passo?](#qual-o-próximo-passo)
- [O que a TRIWI tem sobre análise de concorrência na SERP?](#o-que-a-triwi-tem-sobre-análise-de-concorrência-na-serp)
- [Perguntas frequentes](#perguntas-frequentes)

## Prompt para ler a página de resultados de uma busca

**Objetivo:** Entender qual intenção o Google está atendendo numa busca, que tipo de página ganha e que ângulo ninguém ocupou, a partir da SERP coletada.

**Campos a preencher:** troque cada campo entre colchetes pela informação real antes de enviar.

| Campo | O que colocar |
|:---|:---|
| `[PALAVRA PRINCIPAL]` | A busca analisada |
| `[DATA]` | O dia da coleta |
| `[RESULTADOS DA SERP]` | Título, URL e descrição dos dez primeiros resultados e a lista dos recursos que apareceram |
| `[SITE]` | O domínio do seu site |

**Prompt pronto para copiar:**

```text
Abaixo estão os dez primeiros resultados orgânicos do Google Brasil para a busca [PALAVRA PRINCIPAL], coletados em [DATA], com título, URL e descrição de cada um, e os recursos que apareceram na página (AI Overview, perguntas relacionadas, vídeos, mapa, produtos):
[RESULTADOS DA SERP]

Analise:
1. Qual intenção o Google está atendendo: aprender, comparar, comprar, encontrar um lugar ou uma marca? Justifique com os resultados.
2. Que tipos de página aparecem (artigo, categoria, produto, ferramenta, vídeo, fórum) e quantos de cada.
3. Que ângulo se repete nos títulos e o que nenhum resultado oferece.
4. Que recursos da página de resultados disputam o clique com os resultados orgânicos.
5. Que tipo de página, com que ângulo, teria chance real de entrar nesses resultados, considerando o site [SITE].

Use apenas os resultados que colei. Não descreva resultados de memória.
```

> **O que a IA pode errar:** Sem a SERP colada, a IA descreve de memória uma página de resultados que pode ser de outro país, de outro idioma ou de anos atrás. Mesmo com busca na web ativada, o que ela vê não é o que um usuário no Brasil vê. Colete a SERP numa janela anônima, com a localização certa, e registre a data.

**Na TRIWI:** [Análise de concorrência em SEO: como identificar oportunidades](https://github.com/TRIWI-SEO/SEO-IA/blob/main/metricas-e-ferramentas/analise-de-concorrencia-em-seo-como-identificar-oportunidades.md), guia aberto da Base de Conhecimento da TRIWI no GitHub.

<sub>Código do prompt: SERP-01. Atualizado em 09/11/2026.</sub>

## Prompt para comparar a sua página com as que estão à frente

**Objetivo:** Descobrir o que as páginas mais bem posicionadas cobrem e a sua não, e o que a sua tem de próprio, sem cair na armadilha de escrever mais.

**Campos a preencher:** troque cada campo entre colchetes pela informação real antes de enviar.

| Campo | O que colocar |
|:---|:---|
| `[PALAVRA PRINCIPAL]` | A busca disputada |
| `[MINHA URL]` | O endereço da sua página |
| `[TEXTO DA MINHA PÁGINA]` | O texto da sua página |
| `[URL 1]` | Endereço do primeiro concorrente |
| `[TEXTO 1]` | Texto do primeiro concorrente |
| `[URL 2]` | Endereço do segundo concorrente |
| `[TEXTO 2]` | Texto do segundo concorrente |
| `[URL 3]` | Endereço do terceiro concorrente |
| `[TEXTO 3]` | Texto do terceiro concorrente |

**Prompt pronto para copiar:**

```text
Compare a minha página com as três que estão à frente dela no Google Brasil para a busca [PALAVRA PRINCIPAL].

Minha página ([MINHA URL]):
[TEXTO DA MINHA PÁGINA]

Concorrente 1 ([URL 1]):
[TEXTO 1]

Concorrente 2 ([URL 2]):
[TEXTO 2]

Concorrente 3 ([URL 3]):
[TEXTO 3]

Entregue uma tabela com uma linha por critério e uma coluna por página: resposta direta à busca; subtemas cobertos; provas e fontes; experiência própria; formatos (tabela, lista, vídeo, ferramenta); sinais de atualização; chamada para ação.

Depois, liste:
1. Os subtemas que os concorrentes cobrem e a minha página não.
2. O que a minha página tem e os concorrentes não, e que deve ganhar destaque.
3. As cinco mudanças com mais impacto, em ordem.

Não copie trechos dos concorrentes nem sugira copiar. Não estime autoridade de domínio nem backlinks: esses dados não estão no material.
```

> **O que a IA pode errar:** A IA compara só o texto, e uma página pode estar à frente por motivos que não aparecem nele: autoridade do domínio, links, histórico, marca. Ela também tende a recomendar escrever mais porque os concorrentes são longos. O Google diz que não tem contagem de palavras preferida: o que pesa é cobrir a intenção de quem busca.

**Na TRIWI:** [Guia de SEO](https://triwi.com.br/guias/seo/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=analise-de-concorrencia-na-serp), guia da TRIWI com o método completo.

**Fonte oficial citada no alerta:** [Criar conteúdo útil, confiável e que prioriza as pessoas (Google Search Central)](https://developers.google.com/search/docs/fundamentals/creating-helpful-content?hl=pt-br), consultada em 09/11/2026.

<sub>Código do prompt: SERP-02. Atualizado em 09/11/2026.</sub>

## Prompt para mapear quais sites dominam um grupo de buscas

**Objetivo:** Ver, num conjunto de buscas importantes, quem ocupa as primeiras posições, onde os concorrentes diretos dominam e onde há espaço aberto.

**Campos a preencher:** troque cada campo entre colchetes pela informação real antes de enviar.

| Campo | O que colocar |
|:---|:---|
| `[SETOR]` | O mercado analisado |
| `[DATA]` | O dia da coleta |
| `[TABELA DE BUSCAS E DOMÍNIOS]` | Uma linha por busca, com os três domínios do topo |
| `[CONCORRENTES]` | Os domínios que a empresa considera concorrentes diretos |
| `[EMPRESA]` | Nome da empresa que vai usar a análise |

**Prompt pronto para copiar:**

```text
Abaixo está uma tabela com as buscas mais importantes do mercado de [SETOR] e os domínios que apareceram nas três primeiras posições orgânicas de cada uma, coletada em [DATA]:
[TABELA DE BUSCAS E DOMÍNIOS]

Tarefa:
1. Conte quantas vezes cada domínio aparece e em quais buscas, usando só a tabela.
2. Classifique os domínios em: concorrente direto, portal ou mídia, marketplace, órgão oficial, fórum ou comunidade, outro. Os concorrentes diretos são: [CONCORRENTES].
3. Mostre em que buscas nenhum concorrente direto aparece (espaço aberto) e em quais eles dominam.
4. Diga que tipo de conteúdo cada grupo de domínios usa para ocupar essas posições.
5. Sugira por onde a empresa [EMPRESA] deveria começar, com justificativa.

Não acrescente domínios que não estão na tabela. Quando não souber o que é um domínio, classifique como "a conferir".
```

> **O que a IA pode errar:** Ao classificar domínios, a IA deduz o que cada site é pelo nome e erra com frequência: confunde marca com portal, ou um concorrente com um fornecedor. Também pode errar a contagem em tabelas longas. Por isso o prompt pede a lista de concorrentes e o rótulo a conferir. Confira os maiores números na planilha original.

**Na TRIWI:** [Gerador de buscas avançadas (Dorks)](https://triwi.com.br/ferramentas/gerador-de-buscas-avancadas-dorks/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=analise-de-concorrencia-na-serp), ferramenta gratuita da TRIWI, no navegador e sem cadastro.

<sub>Código do prompt: SERP-03. Atualizado em 09/11/2026.</sub>

## Qual o próximo passo?

Cada tarefa desta biblioteca é uma etapa do trabalho de SEO e GEO. Depois desta, o caminho natural é:

| Próxima tarefa | Para quê |
|:---|:---|
| [Prompts para briefing de conteúdo de SEO no ChatGPT, Claude e Gemini](prompts-para-briefing-de-conteudo-seo.md) | Levar para o briefing o ângulo que nenhum resultado ocupa |

## O que a TRIWI tem sobre análise de concorrência na SERP?

Os prompts desta página são a versão curta e aberta. Para o método completo, a TRIWI publica de graça:

| Recurso | Tipo | O que faz |
|:---|:---|:---|
| [Análise de concorrência em SEO: como identificar oportunidades](https://github.com/TRIWI-SEO/SEO-IA/blob/main/metricas-e-ferramentas/analise-de-concorrencia-em-seo-como-identificar-oportunidades.md) | Base de Conhecimento | Como ler a concorrência na busca e transformar o que ela deixa aberto em oportunidade |
| [Gerador de buscas avançadas (Dorks)](https://triwi.com.br/ferramentas/gerador-de-buscas-avancadas-dorks/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=analise-de-concorrencia-na-serp) | Ferramenta | Monta operadores de busca do Google para investigar sites, concorrentes e oportunidades |
| [Guia de SEO](https://triwi.com.br/guias/seo/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=analise-de-concorrencia-na-serp) | Guia | O que é SEO, como funciona e como gerar resultado de negócio com busca orgânica |
| [Guia de Palavras-chave e Intenção de Busca](https://triwi.com.br/guias/palavras-chave/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=analise-de-concorrencia-na-serp) | Guia | Como encontrar, priorizar e mapear palavras-chave pela intenção de quem busca |

## Perguntas frequentes

<details>
<summary><strong>O ChatGPT com busca na web vê a mesma SERP que eu?</strong></summary>

Não necessariamente. A busca da IA usa o próprio sistema, com outra localização e outra personalização, e devolve um resumo, não a página de resultados. Para análise de concorrência, colete a SERP você mesmo, em janela anônima e com a localização certa, e cole no prompt.
</details>

<details>
<summary><strong>Concorrente na SERP é o mesmo que concorrente comercial?</strong></summary>

Nem sempre. Na página de resultados, quem disputa o clique pode ser um portal, um marketplace, um órgão oficial ou um fórum. Por isso o prompt de mapeamento separa o concorrente direto dos outros tipos de domínio.
</details>

**Ver também na Base de Conhecimento da TRIWI:** [Análise de Concorrência em SEO](https://github.com/TRIWI-SEO/SEO-IA/blob/main/metricas-e-ferramentas/analise-de-concorrencia-em-seo-como-identificar-oportunidades.md), [O Fim dos 10 Links Azuis](https://github.com/TRIWI-SEO/SEO-IA/blob/main/tendencias-e-futuro/o-fim-dos-10-links-azuis-como-a-serp-esta-evoluindo.md), [Intenção de Busca](https://github.com/TRIWI-SEO/SEO-IA/blob/main/fundamentos-de-seo/intencao-de-busca-o-fundamento-que-muda-tudo-em-seo.md), [Fatores de Rankeamento do Google](https://github.com/TRIWI-SEO/SEO-IA/blob/main/fundamentos-de-seo/fatores-de-rankeamento-do-google.md).

**Ver também no Glossário da TRIWI:** [SERP](https://triwi.com.br/glossario/seo/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=analise-de-concorrencia-na-serp#seo-serp), [Análise de concorrência em SEO](https://triwi.com.br/glossario/seo/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=analise-de-concorrencia-na-serp#seo-analise-de-concorrencia-em-seo), [Intenção de busca](https://triwi.com.br/glossario/seo/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=analise-de-concorrencia-na-serp#seo-intencao-de-busca), [Featured snippet](https://triwi.com.br/glossario/seo/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=analise-de-concorrencia-na-serp#seo-featured-snippet), [People Also Ask](https://triwi.com.br/glossario/seo/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=analise-de-concorrencia-na-serp#seo-people-also-ask).

[Voltar para a biblioteca completa](README.md)

---

<p align="center">
  <strong>Quer saber por que o concorrente aparece e a sua empresa não?</strong><br>
  <a href="https://triwi.com.br/contato/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=analise-de-concorrencia-na-serp">Que tal um café com a TRIWI?</a>
</p>

<p align="center">
  <sub>Biblioteca publicada e mantida pela equipe da TRIWI, agência 100% especializada em SEO e Otimização para IAs.</sub>
</p>
