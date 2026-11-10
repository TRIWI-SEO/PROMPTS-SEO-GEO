# Prompts para auditoria de página de SEO no ChatGPT, Claude e Gemini

**A IA ajuda a auditar uma página de SEO quando recebe o HTML, o texto ou o relatório de um rastreador, mas não rastreia o site, não mede velocidade e não vê o índice do Google. Os prompts desta página cobrem auditoria on-page, qualidade do conteúdo e priorização de relatório técnico.**

São três prompts em português, cada um com objetivo, campos a preencher, o prompt pronto para copiar e o alerta do que a IA pode errar. Todos funcionam no ChatGPT, no Claude, no Gemini e em outras IAs de conversa. A biblioteca completa, com 30 prompts em 10 tarefas, está no [README](README.md).

*Por equipe de SEO da TRIWI, com revisão de Ricardo Martins, fundador. Publicado em 09/11/2026. Atualizado em 09/11/2026.*

## Índice

- [Prompt para auditoria de SEO on-page a partir do HTML](#prompt-para-auditoria-de-seo-on-page-a-partir-do-html)
- [Prompt para avaliar a qualidade e o E-E-A-T de um conteúdo](#prompt-para-avaliar-a-qualidade-e-o-e-e-a-t-de-um-conteúdo)
- [Prompt para priorizar os problemas de um relatório de auditoria técnica](#prompt-para-priorizar-os-problemas-de-um-relatório-de-auditoria-técnica)
- [Qual o próximo passo?](#qual-o-próximo-passo)
- [O que a TRIWI tem sobre auditoria de página?](#o-que-a-triwi-tem-sobre-auditoria-de-página)
- [Perguntas frequentes](#perguntas-frequentes)

## Prompt para auditoria de SEO on-page a partir do HTML

**Objetivo:** Revisar os elementos de SEO de uma página (title, headings, links, imagens, marcações) com status, achado e correção recomendada, em ordem de peso.

**Campos a preencher:** troque cada campo entre colchetes pela informação real antes de enviar.

| Campo | O que colocar |
|:---|:---|
| `[PALAVRA PRINCIPAL]` | A busca que a página quer ganhar |
| `[PÚBLICO]` | Quem é o leitor da página |
| `[HTML]` | O código da página, de preferência o HTML renderizado que aparece na Inspeção de URL do Search Console |

**Prompt pronto para copiar:**

```text
Faça uma auditoria de SEO on-page da página abaixo. A busca que ela quer ganhar é [PALAVRA PRINCIPAL] e o público é [PÚBLICO].

Código HTML da página:
[HTML]

Avalie os itens abaixo, um por linha, com status (ok, ajustar ou crítico), o que encontrou e a correção recomendada:
1. Elemento title e meta description.
2. H1 e hierarquia de headings.
3. Resposta à intenção de busca nos primeiros parágrafos.
4. Links internos: quantidade, texto âncora e destino.
5. Imagens: atributo alt, dimensões declaradas e formato.
6. Dados estruturados presentes e erros visíveis no JSON-LD.
7. Canonical, meta robots e hreflang, se houver.
8. Sinais de autoria e de data: quem escreveu e quando a página foi atualizada.

Regras:
1. Avalie só o que está no HTML que colei. Se algo não aparece no código, escreva "não encontrado no HTML" em vez de supor.
2. Não avalie velocidade nem Core Web Vitals: isso exige medição real.
3. Ordene as correções da que mais pesa para a que menos pesa.
```

> **O que a IA pode errar:** A IA não abre a página como o robô do Google: ela lê o texto que você colou. Se o site monta o conteúdo com JavaScript, o código-fonte pode vir quase vazio e a IA vai apontar falhas que não existem na página renderizada. Ela também opina sobre velocidade sem medir. Para o HTML renderizado, use a Inspeção de URL do Search Console; para performance, o PageSpeed Insights.

**Na TRIWI:** [Analisador de SEO de HTML colado](https://triwi.com.br/ferramentas/analisador-de-seo-de-html/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=auditoria-de-pagina-seo), ferramenta gratuita da TRIWI, no navegador e sem cadastro.

**Fonte oficial citada no alerta:** [Noções básicas de JavaScript para SEO (Google Search Central)](https://developers.google.com/search/docs/crawling-indexing/javascript/javascript-seo-basics?hl=pt-br), consultada em 09/11/2026.

<sub>Código do prompt: AU-01. Atualizado em 09/11/2026.</sub>

## Prompt para avaliar a qualidade e o E-E-A-T de um conteúdo

**Objetivo:** Encontrar o que falta para um texto ser útil e confiável, com base nas perguntas de autoavaliação que o próprio Google publica.

**Campos a preencher:** troque cada campo entre colchetes pela informação real antes de enviar.

| Campo | O que colocar |
|:---|:---|
| `[TEMA]` | O assunto do conteúdo |
| `[AUTOR]` | Nome, cargo e experiência de quem assina |
| `[TEXTO]` | O conteúdo completo |

**Prompt pronto para copiar:**

```text
Avalie o conteúdo abaixo com as perguntas que o Google publica para autoavaliar conteúdo útil, confiável e feito para pessoas (experiência, especialização, autoridade e confiança, o E-E-A-T).

Tema: [TEMA]
Autor e credenciais: [AUTOR]
Texto:
[TEXTO]

Entregue:
1. Para cada pergunta de autoavaliação que se aplica ao texto, uma resposta (sim, em parte ou não) com o trecho que justifica.
2. Onde falta experiência própria: trechos genéricos que qualquer site escreveria e o que a empresa poderia acrescentar (caso, foto, dado próprio, opinião de especialista).
3. Afirmações que precisam de fonte e não têm.
4. Sinais de confiança ausentes: autoria, data, revisão técnica, política de correção.
5. As três mudanças que mais aumentariam a utilidade do texto, em ordem.

Não dê nota numérica de E-E-A-T: essa nota não existe no Google. Se não lembrar exatamente das perguntas do Google, diga isso em vez de inventar.
```

> **O que a IA pode errar:** E-E-A-T não é um número nem um fator medido diretamente, e a IA costuma devolver uma nota de E-E-A-T que não significa nada. Ela também confunde as diretrizes dos avaliadores de qualidade com o algoritmo. Use a resposta como lista de melhorias e compare com a página oficial do Google sobre conteúdo útil.

**Na TRIWI:** [E-E-A-T: o framework do Google para qualidade de conteúdo](https://github.com/TRIWI-SEO/SEO-IA/blob/main/seo-de-conteudo/e-e-a-t-o-framework-do-google-para-qualidade-de-conteudo.md), guia aberto da Base de Conhecimento da TRIWI no GitHub.

**Fonte oficial citada no alerta:** [Criar conteúdo útil, confiável e que prioriza as pessoas (Google Search Central)](https://developers.google.com/search/docs/fundamentals/creating-helpful-content?hl=pt-br), consultada em 09/11/2026.

<sub>Código do prompt: AU-02. Atualizado em 09/11/2026.</sub>

## Prompt para priorizar os problemas de um relatório de auditoria técnica

**Objetivo:** Transformar a exportação de um rastreador, com centenas de alertas, numa lista curta de correções em ordem de impacto no negócio.

**Campos a preencher:** troque cada campo entre colchetes pela informação real antes de enviar.

| Campo | O que colocar |
|:---|:---|
| `[FERRAMENTA]` | O rastreador usado, como Screaming Frog ou Semrush |
| `[SITE]` | O domínio auditado |
| `[NÚMERO DE PÁGINAS]` | Quantas páginas o site tem, aproximadamente |
| `[MODELO DE NEGÓCIO]` | Como o site gera receita, por exemplo loja virtual, geração de leads ou assinatura |
| `[PÁGINAS PRIORITÁRIAS]` | URLs que mais geram receita ou contatos |
| `[RELATÓRIO]` | A exportação do relatório, em texto ou CSV |

**Prompt pronto para copiar:**

```text
Abaixo está a exportação de um relatório de auditoria técnica feito com [FERRAMENTA] no site [SITE], que tem cerca de [NÚMERO DE PÁGINAS] páginas e vive de [MODELO DE NEGÓCIO]. As páginas que mais geram receita ou contatos são estas:
[PÁGINAS PRIORITÁRIAS]

Relatório:
[RELATÓRIO]

Tarefa:
1. Agrupe os problemas por tipo e diga quantas URLs cada tipo afeta, usando só os números do relatório.
2. Classifique cada tipo em: impede rastreamento ou indexação; afeta como a página aparece nos resultados; afeta a experiência; cosmético.
3. Monte uma lista de prioridade que cruze a gravidade com a importância das páginas afetadas, com as páginas prioritárias primeiro.
4. Para cada item da lista, escreva a correção em linguagem que um desenvolvedor entenda e como conferir que foi resolvida.
5. Liste os alertas do relatório que podem ser ignorados neste site e explique por quê.

Não acrescente problemas que não estão no relatório.
```

> **O que a IA pode errar:** Relatórios de auditoria geram centenas de alertas, e a IA tende a tratar todos como urgentes ou a repetir a gravidade que a ferramenta atribuiu. Ela não sabe quais páginas trazem receita se você não disser. Arquivos grandes podem ser lidos pela metade sem aviso: confira se os totais da resposta batem com os do relatório.

**Na TRIWI:** [Guia de SEO Técnico](https://triwi.com.br/guias/seo-tecnico/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=auditoria-de-pagina-seo), guia da TRIWI com o método completo.

<sub>Código do prompt: AU-03. Atualizado em 09/11/2026.</sub>

## Qual o próximo passo?

Cada tarefa desta biblioteca é uma etapa do trabalho de SEO e GEO. Depois desta, o caminho natural é:

| Próxima tarefa | Para quê |
|:---|:---|
| [Prompts para relatório de SEO e ROI no ChatGPT, Claude e Gemini](prompts-para-relatorio-de-seo.md) | Mostrar o efeito das correções em linguagem de negócio |

## O que a TRIWI tem sobre auditoria de página?

Os prompts desta página são a versão curta e aberta. Para o método completo, a TRIWI publica de graça:

| Recurso | Tipo | O que faz |
|:---|:---|:---|
| [Analisador de SEO de HTML colado](https://triwi.com.br/ferramentas/analisador-de-seo-de-html/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=auditoria-de-pagina-seo) | Ferramenta | Lê o HTML de uma página e mostra título, descrição, headings, links e marcações |
| [Checklist de SEO guiado](https://triwi.com.br/ferramentas/checklist-de-seo/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=auditoria-de-pagina-seo) | Ferramenta | Roteiro passo a passo para revisar os pontos essenciais de SEO de um site |
| [Guia de SEO Técnico](https://triwi.com.br/guias/seo-tecnico/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=auditoria-de-pagina-seo) | Guia | Rastreamento, indexação, performance, arquitetura e dados estruturados |
| [E-E-A-T: o framework do Google para qualidade de conteúdo](https://github.com/TRIWI-SEO/SEO-IA/blob/main/seo-de-conteudo/e-e-a-t-o-framework-do-google-para-qualidade-de-conteudo.md) | Base de Conhecimento | Experiência, especialização, autoridade e confiança, explicadas para quem produz conteúdo |

## Perguntas frequentes

<details>
<summary><strong>A IA consegue auditar um site inteiro?</strong></summary>

Sozinha, não. Ela não rastreia o site nem acessa o Search Console. O caminho é usar um rastreador e o Search Console para coletar os dados e a IA para organizar, priorizar e traduzir os achados em tarefas, como no prompt de relatório desta página.
</details>

<details>
<summary><strong>Por que a IA aponta erro numa página que está certa?</strong></summary>

Na maioria das vezes, porque leu o HTML inicial de um site que monta o conteúdo com JavaScript. O Google renderiza a página antes de indexar; a IA, não. Cole no prompt o HTML renderizado que a Inspeção de URL do Search Console mostra.
</details>

**Ver também na Base de Conhecimento da TRIWI:** [SEO On-Page](https://github.com/TRIWI-SEO/SEO-IA/blob/main/fundamentos-de-seo/seo-on-page-otimizacao-dentro-do-seu-site.md), [SEO Técnico: Guia Completo](https://github.com/TRIWI-SEO/SEO-IA/blob/main/seo-tecnico/seo-tecnico-guia-completo.md), [Crawling e Indexação](https://github.com/TRIWI-SEO/SEO-IA/blob/main/seo-tecnico/crawling-e-indexacao-como-garantir-que-o-google-encontre-seu-site.md), [Core Web Vitals](https://github.com/TRIWI-SEO/SEO-IA/blob/main/seo-tecnico/core-web-vitals-performance-que-impacta-rankeamento.md).

**Ver também no Glossário da TRIWI:** [Auditoria de SEO](https://triwi.com.br/glossario/seo/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=auditoria-de-pagina-seo#seo-auditoria-de-seo), [Heading tags](https://triwi.com.br/glossario/seo/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=auditoria-de-pagina-seo#seo-heading-tags), [Title tag](https://triwi.com.br/glossario/seo/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=auditoria-de-pagina-seo#seo-title-tag), [E-E-A-T](https://triwi.com.br/glossario/seo/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=auditoria-de-pagina-seo#seo-e-e-a-t), [Alucinação](https://triwi.com.br/glossario/inteligencia-artificial/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=auditoria-de-pagina-seo#ia-alucinacao).

[Voltar para a biblioteca completa](README.md)

---

<p align="center">
  <strong>Auditoria mostra o problema. Quer quem resolva, no Google e nas IAs?</strong><br>
  <a href="https://triwi.com.br/contato/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=auditoria-de-pagina-seo">Que tal um café com a TRIWI?</a>
</p>

<p align="center">
  <sub>Biblioteca publicada e mantida pela equipe da TRIWI, agência 100% especializada em SEO e Otimização para IAs.</sub>
</p>
