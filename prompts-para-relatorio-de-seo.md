# Prompts para relatório de SEO e ROI no ChatGPT, Claude e Gemini

**Um bom relatório de SEO começa pelo resultado de negócio (conversões, receita, custo de aquisição) e só depois mostra cliques e posições. A IA ajuda a organizar e explicar os números quando recebe os dados, mas erra conta e confunde coincidência com causa. Os prompts desta página montam o relatório, investigam uma queda e calculam o ROI.**

São três prompts em português, cada um com objetivo, campos a preencher, o prompt pronto para copiar e o alerta do que a IA pode errar. Todos funcionam no ChatGPT, no Claude, no Gemini e em outras IAs de conversa. A biblioteca completa, com 30 prompts em 10 tarefas, está no [README](README.md).

*Por equipe de SEO da TRIWI, com revisão de Ricardo Martins, fundador. Publicado em 09/11/2026. Atualizado em 09/11/2026.*

## Índice

- [Prompt para transformar dados de SEO num relatório para a diretoria](#prompt-para-transformar-dados-de-seo-num-relatório-para-a-diretoria)
- [Prompt para investigar uma queda de tráfego orgânico](#prompt-para-investigar-uma-queda-de-tráfego-orgânico)
- [Prompt para calcular o ROI de SEO com os dados da empresa](#prompt-para-calcular-o-roi-de-seo-com-os-dados-da-empresa)
- [Qual o próximo passo?](#qual-o-próximo-passo)
- [O que a TRIWI tem sobre relatório de SEO?](#o-que-a-triwi-tem-sobre-relatório-de-seo)
- [Perguntas frequentes](#perguntas-frequentes)

## Prompt para transformar dados de SEO num relatório para a diretoria

**Objetivo:** Traduzir os números do Search Console e do analytics em resultado de negócio, numa página que a diretoria lê em poucos minutos.

**Campos a preencher:** troque cada campo entre colchetes pela informação real antes de enviar.

| Campo | O que colocar |
|:---|:---|
| `[EMPRESA]` | Nome da empresa |
| `[PÚBLICO DO RELATÓRIO]` | Quem vai ler, como diretoria, comercial ou conselho |
| `[PERÍODO]` | O mês ou trimestre do relatório |
| `[DADOS DO SEARCH CONSOLE]` | A exportação do relatório de desempenho, com o período anterior |
| `[DADOS DO ANALYTICS]` | Sessões, conversões e receita do canal orgânico, com o período anterior |
| `[AÇÕES DO PERÍODO]` | O que foi publicado, corrigido ou mudado no site |
| `[METAS]` | As metas de negócio que o SEO apoia |

**Prompt pronto para copiar:**

```text
Monte o relatório mensal de SEO de [EMPRESA] para [PÚBLICO DO RELATÓRIO], referente a [PERÍODO].

Dados do Search Console (cliques, impressões, CTR e posição, com o período anterior):
[DADOS DO SEARCH CONSOLE]

Dados do analytics do tráfego orgânico (sessões, conversões e receita, com o período anterior):
[DADOS DO ANALYTICS]

O que foi feito no período: [AÇÕES DO PERÍODO]
Metas de negócio do ano: [METAS]

Estrutura:
1. Resumo em três frases: o resultado de negócio do mês, a principal causa e a próxima decisão.
2. Indicadores de negócio primeiro (conversões e receita do orgânico), depois os de visibilidade (cliques, impressões, posição).
3. Busca de marca e busca sem marca separadas, quando os dados permitirem.
4. O que explica a variação, separando o que os dados mostram do que é hipótese.
5. Próximos passos, com o resultado esperado de cada um.

Regras: use só os números que colei e mostre a conta de cada variação. Não use jargão sem explicar. Não atribua resultado a uma ação sem dado que sustente.
```

> **O que a IA pode errar:** A IA trata clique do Search Console e sessão do analytics como se fossem a mesma coisa, e eles medem coisas diferentes. Ela também transforma coincidência em causa: se uma página foi publicada e o tráfego subiu, o relatório diz que uma causou a outra. Confira cada conta, mantenha as duas fontes separadas e exija o dado que sustenta cada explicação.

**Na TRIWI:** [Guia de Métricas de SEO e IA](https://triwi.com.br/guias/metricas-de-seo/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=relatorio-de-seo), guia da TRIWI com o método completo.

<sub>Código do prompt: REL-01. Atualizado em 09/11/2026.</sub>

## Prompt para investigar uma queda de tráfego orgânico

**Objetivo:** Organizar as causas possíveis de uma queda de tráfego, do mais provável ao menos provável, com o dado que confirma ou descarta cada uma.

**Campos a preencher:** troque cada campo entre colchetes pela informação real antes de enviar.

| Campo | O que colocar |
|:---|:---|
| `[SITE]` | O domínio do site |
| `[DATA DA QUEDA]` | O dia ou a semana em que a queda começou |
| `[DADOS DO SEARCH CONSOLE]` | Comparação de períodos por página e por consulta |
| `[MUDANÇAS NO SITE]` | O que mudou no site nas semanas anteriores |
| `[ATUALIZAÇÕES DO GOOGLE]` | As atualizações com data de início e fim no período |
| `[SAZONALIDADE]` | Meses de alta e de baixa do negócio |

**Prompt pronto para copiar:**

```text
O tráfego orgânico do site [SITE] caiu a partir de [DATA DA QUEDA].

Dados do Search Console antes e depois da queda, por página e por consulta:
[DADOS DO SEARCH CONSOLE]

Mudanças feitas no site no período (publicações, migração, mudança de template, redirecionamentos): [MUDANÇAS NO SITE]
Atualizações do Google registradas no período, conferidas no Painel de status da Pesquisa Google: [ATUALIZAÇÕES DO GOOGLE]
Sazonalidade conhecida do negócio: [SAZONALIDADE]

Tarefa:
1. Descreva a queda: concentrada em poucas páginas ou espalhada, em busca de marca ou sem marca, em cliques com posição estável ou em posição.
2. Liste as causas possíveis (problema técnico, mudança no site, atualização do Google, sazonalidade, mudança na página de resultados, perda para concorrente), cada uma com o dado que a confirma ou descarta.
3. Ordene da mais provável para a menos provável, com justificativa.
4. Diga o que verificar primeiro e onde.

Não aponte uma causa como certa sem dado que sustente.
```

> **O que a IA pode errar:** A IA culpa a atualização do Google por reflexo, e muitas quedas vêm de mudança no próprio site, de sazonalidade ou de um recurso novo na página de resultados. Ela também não sabe as datas reais das atualizações: confira no Painel de status da Pesquisa Google e cole no prompt. Uma queda que começou antes da atualização não foi causada por ela.

**Na TRIWI:** [Atualizações do Google](https://triwi.com.br/atualizacoes/google/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=relatorio-de-seo), linha do tempo de atualizações da TRIWI.

**Fonte oficial citada no alerta:** [Painel de status da Pesquisa Google](https://status.search.google.com/), consultada em 09/11/2026.

<sub>Código do prompt: REL-02. Atualizado em 09/11/2026.</sub>

## Prompt para calcular o ROI de SEO com os dados da empresa

**Objetivo:** Calcular o retorno do investimento em SEO a partir de receita, margem e investimento informados, com a conta aberta e as premissas declaradas.

**Campos a preencher:** troque cada campo entre colchetes pela informação real antes de enviar.

| Campo | O que colocar |
|:---|:---|
| `[EMPRESA]` | Nome da empresa |
| `[PERÍODO]` | O período do cálculo |
| `[INVESTIMENTO]` | Quanto foi investido em SEO no período |
| `[CONVERSÕES]` | Vendas ou leads do orgânico no período |
| `[TAXA DE FECHAMENTO]` | Quantos leads viram venda, ou não se aplica |
| `[TICKET MÉDIO]` | Valor médio de cada venda |
| `[MARGEM]` | Margem de contribuição do negócio |
| `[PARTE DE MARCA]` | Quanto do orgânico vem de buscas pelo nome da empresa |

**Prompt pronto para copiar:**

```text
Calcule o retorno sobre o investimento (ROI) do SEO de [EMPRESA] em [PERÍODO], com estes dados:

- Investimento em SEO no período (equipe, fornecedor, ferramentas, conteúdo): [INVESTIMENTO]
- Conversões atribuídas ao orgânico: [CONVERSÕES]
- Taxa de fechamento de lead em venda, se o site gera leads: [TAXA DE FECHAMENTO]
- Valor médio de cada venda: [TICKET MÉDIO]
- Margem de contribuição: [MARGEM]
- Parcela do orgânico que vem de busca de marca: [PARTE DE MARCA]

Tarefa:
1. Calcule a receita atribuída ao orgânico e o lucro bruto que ela gera.
2. Calcule o ROI: lucro atribuído menos investimento, dividido pelo investimento.
3. Refaça a conta sem a busca de marca, que em boa parte viria de qualquer jeito.
4. Mostre cada conta passo a passo e liste as premissas que mais mexem no resultado.

Não preencha dado que eu não informei. Se faltar algum, pare e diga qual.
```

> **O que a IA pode errar:** A IA erra conta e, quando falta um dado, completa com uma média de mercado sem avisar. Ela também calcula ROI sobre receita em vez de lucro, o que infla o resultado. Refaça a conta numa planilha, deixe as premissas escritas e separe busca de marca, que mede a força da marca mais do que o trabalho de SEO.

**Na TRIWI:** [Calculadora de ROI](https://triwi.com.br/ferramentas/calculadora-de-roi/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=relatorio-de-seo), ferramenta gratuita da TRIWI, no navegador e sem cadastro.

<sub>Código do prompt: REL-03. Atualizado em 09/11/2026.</sub>

## Qual o próximo passo?

Cada tarefa desta biblioteca é uma etapa do trabalho de SEO e GEO. Depois desta, o caminho natural é:

| Próxima tarefa | Para quê |
|:---|:---|
| [Prompts para medir a presença da marca nas IAs (Share of Model)](prompts-para-medir-presenca-da-marca-nas-ias.md) | Somar ao relatório a presença da marca nas respostas de IA |

## O que a TRIWI tem sobre relatório de SEO?

Os prompts desta página são a versão curta e aberta. Para o método completo, a TRIWI publica de graça:

| Recurso | Tipo | O que faz |
|:---|:---|:---|
| [Guia de Métricas de SEO e IA](https://triwi.com.br/guias/metricas-de-seo/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=relatorio-de-seo) | Guia | Quais indicadores acompanhar para ligar SEO e GEO a resultado de negócio |
| [Calculadora de ROI](https://triwi.com.br/ferramentas/calculadora-de-roi/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=relatorio-de-seo) | Ferramenta | Calcula o retorno sobre o investimento de uma iniciativa de marketing |
| [ROI de SEO: como calcular o retorno sobre investimento](https://github.com/TRIWI-SEO/SEO-IA/blob/main/metricas-e-ferramentas/roi-de-seo-como-calcular-o-retorno-sobre-investimento.md) | Base de Conhecimento | Como ligar o investimento em SEO a receita e lucro, com as premissas declaradas |
| [Atualizações do Google](https://triwi.com.br/atualizacoes/google/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=relatorio-de-seo) | Atualizações | Core updates, spam updates e mudanças de recursos da busca do Google, com data e fonte |

## Perguntas frequentes

<details>
<summary><strong>Quais números devem estar num relatório de SEO?</strong></summary>

Primeiro os de negócio: conversões, receita ou leads do orgânico e o custo de aquisição. Depois os de visibilidade, que explicam os primeiros: cliques, impressões, posição e presença nas IAs. O guia aberto [Métricas de SEO que Importam](https://github.com/TRIWI-SEO/SEO-IA/blob/main/metricas-e-ferramentas/metricas-de-seo-que-importam-kpis-focados-em-negocio.md) detalha cada um.
</details>

<details>
<summary><strong>Por que os cliques do Search Console não batem com as sessões do analytics?</strong></summary>

Porque medem coisas diferentes: o Search Console conta cliques no resultado do Google; o analytics conta sessões no site, depende do consentimento de cookies e do código instalado e atribui a origem por regras próprias. A diferença é normal; o que importa é acompanhar cada fonte com a mesma régua ao longo do tempo.
</details>

**Ver também na Base de Conhecimento da TRIWI:** [ROI de SEO](https://github.com/TRIWI-SEO/SEO-IA/blob/main/metricas-e-ferramentas/roi-de-seo-como-calcular-o-retorno-sobre-investimento.md), [Métricas de SEO que Importam](https://github.com/TRIWI-SEO/SEO-IA/blob/main/metricas-e-ferramentas/metricas-de-seo-que-importam-kpis-focados-em-negocio.md), [Google Search Console: Guia Completo para SEO](https://github.com/TRIWI-SEO/SEO-IA/blob/main/metricas-e-ferramentas/google-search-console-guia-completo-para-seo.md), [Atualizações do Google: Guia de Core Updates](https://github.com/TRIWI-SEO/SEO-IA/blob/main/tendencias-e-futuro/atualizacoes-do-google-guia-de-core-updates-e-seus-impactos.md).

**Ver também no Glossário da TRIWI:** [KPIs de SEO](https://triwi.com.br/glossario/seo/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=relatorio-de-seo#seo-kpis-de-seo), [Tráfego de marca e não marca](https://triwi.com.br/glossario/seo/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=relatorio-de-seo#seo-trafego-de-marca-e-nao-marca), [Core Update](https://triwi.com.br/glossario/seo/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=relatorio-de-seo#seo-core-update), [ROI](https://triwi.com.br/glossario/marketing/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=relatorio-de-seo#marketing-roi), [Atribuição](https://triwi.com.br/glossario/marketing/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=relatorio-de-seo#marketing-atribuicao).

[Voltar para a biblioteca completa](README.md)

---

<p align="center">
  <strong>Quer um SEO que aparece no relatório como venda, não só como clique?</strong><br>
  <a href="https://triwi.com.br/contato/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=relatorio-de-seo">Que tal um café com a TRIWI?</a>
</p>

<p align="center">
  <sub>Biblioteca publicada e mantida pela equipe da TRIWI, agência 100% especializada em SEO e Otimização para IAs.</sub>
</p>
