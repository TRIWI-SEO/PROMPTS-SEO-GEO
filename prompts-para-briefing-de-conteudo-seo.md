# Prompts para briefing de conteúdo de SEO no ChatGPT, Claude e Gemini

**Um prompt de briefing faz a IA planejar o conteúdo antes de escrever: intenção de busca, recorte, estrutura em perguntas, evidências a coletar e critérios de aceite. Os prompts desta página cobrem conteúdo novo, atualização de conteúdo que perdeu posição e página de produto ou serviço.**

São três prompts em português, cada um com objetivo, campos a preencher, o prompt pronto para copiar e o alerta do que a IA pode errar. Todos funcionam no ChatGPT, no Claude, no Gemini e em outras IAs de conversa. A biblioteca completa, com 24 prompts em 8 tarefas, está no [README](README.md).

*Por equipe de SEO da TRIWI, com revisão de Ricardo Martins, fundador. Publicado em 09/11/2026. Atualizado em 09/11/2026.*

## Índice

- [Prompt para montar o briefing de um conteúdo novo](#prompt-para-montar-o-briefing-de-um-conteúdo-novo)
- [Prompt para o briefing de atualização de um conteúdo que perdeu posição](#prompt-para-o-briefing-de-atualização-de-um-conteúdo-que-perdeu-posição)
- [Prompt para o briefing de uma página de produto ou serviço](#prompt-para-o-briefing-de-uma-página-de-produto-ou-serviço)
- [O que a TRIWI tem sobre briefing de conteúdo?](#o-que-a-triwi-tem-sobre-briefing-de-conteúdo)
- [Perguntas frequentes](#perguntas-frequentes)

## Prompt para montar o briefing de um conteúdo novo

**Objetivo:** Entregar ao redator um briefing com intenção, recorte, estrutura comentada, evidências a coletar e critérios de aceite, antes de qualquer linha de texto.

**Campos a preencher:** troque cada campo entre colchetes pela informação real antes de enviar.

| Campo | O que colocar |
|:---|:---|
| `[EMPRESA]` | Nome da empresa ou da marca |
| `[OFERTA]` | O que a empresa vende |
| `[PÚBLICO]` | Quem vai ler |
| `[PALAVRA PRINCIPAL]` | A busca que a página quer ganhar |
| `[PALAVRAS SECUNDÁRIAS]` | Variações e buscas relacionadas, separadas por vírgula |
| `[OBJETIVO]` | O que a página precisa gerar, como contato, venda ou cadastro |
| `[LINKS INTERNOS]` | URLs do site que o texto deve citar |

**Prompt pronto para copiar:**

```text
Monte o briefing de um conteúdo para SEO que um redator vai escrever.

Contexto:
- Empresa: [EMPRESA], que vende [OFERTA]
- Público: [PÚBLICO]
- Palavra-chave principal: [PALAVRA PRINCIPAL]
- Palavras secundárias: [PALAVRAS SECUNDÁRIAS]
- Objetivo de negócio da página: [OBJETIVO]
- Páginas do site que este conteúdo deve linkar: [LINKS INTERNOS]

O briefing deve ter:
1. Intenção de busca em uma frase: o que a pessoa quer resolver ao digitar a palavra principal.
2. Recorte: o que o conteúdo cobre, o que fica de fora e qual outra página cuida do que ficou de fora.
3. Resposta direta: o que os dois primeiros parágrafos precisam responder, sem introdução.
4. Estrutura comentada: títulos H2 e H3 em formato de pergunta real, com uma linha sobre o que cada seção precisa dizer.
5. Evidências a coletar: dados, exemplos, fontes oficiais e experiência própria da empresa que o texto precisa trazer.
6. Chamada para ação coerente com a intenção de quem chega.
7. Critérios de aceite: a lista do que o editor confere antes de aprovar.

Não escreva o texto. Não invente dados nem fontes: onde for preciso um dado, diga o que buscar e onde.
```

> **O que a IA pode errar:** A IA tende a propor a mesma estrutura de qualquer artigo (o que é, benefícios, dicas, conclusão), que não responde a intenção nem diferencia a página. Ela também sugere fontes e estudos que não existem. Compare a estrutura com os primeiros resultados do Google para a palavra principal e confira toda fonte sugerida antes de passar o briefing ao redator.

**Na TRIWI:** [Skill: criar um briefing de conteúdo para SEO](https://triwi.com.br/skills/criar-briefing-de-conteudo-para-seo/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=briefing-de-conteudo-seo), skill da TRIWI para instalar no Claude ou no ChatGPT, com a versão completa desta tarefa.

<sub>Código do prompt: BR-01. Atualizado em 09/11/2026.</sub>

## Prompt para o briefing de atualização de um conteúdo que perdeu posição

**Objetivo:** Decidir o que manter, atualizar, acrescentar e cortar num conteúdo que caiu no Google, separando o que os dados mostram do que é hipótese.

**Campos a preencher:** troque cada campo entre colchetes pela informação real antes de enviar.

| Campo | O que colocar |
|:---|:---|
| `[URL]` | Endereço da página que caiu |
| `[PALAVRA PRINCIPAL]` | A busca em que ela perdeu posição |
| `[DADOS DO SEARCH CONSOLE]` | Exportação do relatório de desempenho filtrado pela página, com alguns meses de histórico |
| `[TEXTO ATUAL]` | O texto publicado hoje |

**Prompt pronto para copiar:**

```text
O conteúdo publicado em [URL] perdeu posições para a busca [PALAVRA PRINCIPAL]. Estes são os dados do Search Console dos últimos meses (consulta, cliques, impressões, CTR e posição média, mês a mês):
[DADOS DO SEARCH CONSOLE]

Texto atual da página:
[TEXTO ATUAL]

Monte um briefing de atualização com:
1. Diagnóstico provável, separando o que os dados mostram do que é hipótese (queda de cliques com posição estável, queda de posição, mudança de intenção, conteúdo desatualizado).
2. O que manter: trechos que respondem bem e não devem ser reescritos.
3. O que atualizar: informações com data, exemplos e números que precisam ser revistos, com a fonte a consultar.
4. O que acrescentar: perguntas que a busca pede e o texto não responde.
5. O que cortar: trechos que fogem da intenção.
6. Data da página: recomende mudar a data visível só se o conteúdo mudar de fato.

Não reescreva o texto. Não afirme a causa da queda sem apoio nos dados que colei.
```

> **O que a IA pode errar:** A IA costuma atribuir qualquer queda a uma atualização do algoritmo ou a falta de palavra-chave, sem olhar os dados. Queda de cliques com posição estável, por exemplo, pode vir de um AI Overview que passou a aparecer na página de resultados, e não do texto. O Google orienta a não mudar a data de um conteúdo sem mudança real, então desconfie de recomendação que mexa só na data.

**Na TRIWI:** [Inventário e revisão de conteúdo](https://triwi.com.br/ferramentas/inventario-e-revisao-de-conteudo/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=briefing-de-conteudo-seo), ferramenta gratuita da TRIWI, no navegador e sem cadastro.

**Fonte oficial citada no alerta:** [Criar conteúdo útil, confiável e que prioriza as pessoas (Google Search Central)](https://developers.google.com/search/docs/fundamentals/creating-helpful-content?hl=pt-br), consultada em 09/11/2026.

<sub>Código do prompt: BR-02. Atualizado em 09/11/2026.</sub>

## Prompt para o briefing de uma página de produto ou serviço

**Objetivo:** Planejar uma página comercial na ordem em que o comprador decide, usando só diferenciais e provas que a empresa consegue sustentar.

**Campos a preencher:** troque cada campo entre colchetes pela informação real antes de enviar.

| Campo | O que colocar |
|:---|:---|
| `[TIPO DE PÁGINA]` | Produto, serviço, categoria ou página de solução |
| `[OFERTA]` | O produto ou serviço da página |
| `[EMPRESA]` | Nome da empresa ou da marca |
| `[PALAVRA PRINCIPAL]` | A busca que a página quer ganhar |
| `[PÚBLICO]` | Quem compra e em que momento chega à página |
| `[DIFERENCIAIS]` | O que a empresa tem de diferente e consegue provar |
| `[OBJEÇÕES]` | O que faz o cliente hesitar |
| `[RESTRIÇÕES]` | Regras do setor, do jurídico ou da marca |

**Prompt pronto para copiar:**

```text
Monte o briefing de uma página comercial do tipo [TIPO DE PÁGINA] para [OFERTA], da empresa [EMPRESA].

Contexto:
- Palavra-chave principal: [PALAVRA PRINCIPAL]
- Público e momento de compra: [PÚBLICO]
- Diferenciais comprovados (só o que a empresa consegue provar): [DIFERENCIAIS]
- Objeções que vendas mais ouve: [OBJEÇÕES]
- Restrições legais ou de marca: [RESTRIÇÕES]

O briefing deve definir:
1. A frase de abertura, que responde em uma linha o que é a oferta e para quem.
2. Os blocos da página na ordem de decisão do comprador: o que é, para quem serve, como funciona, provas, objeções e próximos passos.
3. A prova que entra em cada bloco (caso, número, certificação, depoimento real), só a partir do que listei.
4. As perguntas frequentes que a página precisa responder.
5. A chamada para ação principal e a secundária.
6. O que a página não pode prometer, com base nas restrições.

Não crie diferenciais, números, certificações ou depoimentos que não estejam no contexto.
```

> **O que a IA pode errar:** Em página comercial, a IA preenche lacunas com promessas: prazo de entrega, garantia, líder de mercado, número de clientes. Tudo soa plausível e pode ser falso ou proibido pelas regras do setor. Confira cada afirmação do briefing contra o que a empresa consegue provar e contra as normas do conselho profissional ou do órgão regulador do setor.

**Na TRIWI:** [Guia de Conteúdo para SEO e IA](https://triwi.com.br/guias/conteudo/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=briefing-de-conteudo-seo), guia da TRIWI com o método completo.

<sub>Código do prompt: BR-03. Atualizado em 09/11/2026.</sub>

## O que a TRIWI tem sobre briefing de conteúdo?

Os prompts desta página são a versão curta e aberta. Para o método completo, a TRIWI publica de graça:

| Recurso | Tipo | O que faz |
|:---|:---|:---|
| [Skill: criar um briefing de conteúdo para SEO](https://triwi.com.br/skills/criar-briefing-de-conteudo-para-seo/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=briefing-de-conteudo-seo) | Skill | Conduz o briefing completo, com perguntas a responder, evidências e critérios de aceite |
| [Gerador de briefing de conteúdo](https://triwi.com.br/ferramentas/gerador-de-briefing-de-conteudo/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=briefing-de-conteudo-seo) | Ferramenta | Monta o briefing de um conteúdo para SEO no navegador |
| [Inventário e revisão de conteúdo](https://triwi.com.br/ferramentas/inventario-e-revisao-de-conteudo/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=briefing-de-conteudo-seo) | Ferramenta | Organiza o inventário de páginas para decidir o que atualizar, consolidar ou remover |
| [Guia de Conteúdo para SEO e IA](https://triwi.com.br/guias/conteudo/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=briefing-de-conteudo-seo) | Guia | Como planejar e escrever conteúdo que ranqueia no Google e é citado pelas IAs |

## Perguntas frequentes

<details>
<summary><strong>Por que fazer briefing antes de pedir o texto à IA?</strong></summary>

Porque o texto sai tão bom quanto as decisões que vêm antes dele. Sem briefing, a IA decide sozinha a intenção, o recorte e as fontes, e costuma entregar o artigo genérico que já existe aos montes. Com briefing, quem escreve, pessoa ou IA, escreve o que a busca pede e o que só a sua empresa pode dizer.
</details>

<details>
<summary><strong>Qual a diferença entre estes prompts e a skill de briefing da TRIWI?</strong></summary>

O prompt é a versão curta e aberta, para colar numa conversa. A [skill de briefing da TRIWI](https://triwi.com.br/skills/criar-briefing-de-conteudo-para-seo/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=briefing) é a versão completa: instalada no Claude ou no ChatGPT, ela conduz o briefing com perguntas a responder, evidências e critérios de aceite em todas as rodadas.
</details>

**Ver também na Base de Conhecimento da TRIWI:** [Estratégia de Conteúdo para SEO](https://github.com/TRIWI-SEO/SEO-IA/blob/main/seo-de-conteudo/estrategia-de-conteudo-para-seo-guia-completo.md), [Copywriting para SEO](https://github.com/TRIWI-SEO/SEO-IA/blob/main/seo-de-conteudo/copywriting-para-seo-como-escrever-conteudo-que-rankeia-e-converte.md), [Content Pruning](https://github.com/TRIWI-SEO/SEO-IA/blob/main/seo-de-conteudo/content-pruning-como-remover-conteudo-para-melhorar-seu-seo.md).

**Ver também no Glossário da TRIWI:** [Briefing de conteúdo para SEO](https://triwi.com.br/glossario/seo/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=briefing-de-conteudo-seo#seo-briefing-de-conteudo-para-seo), [Intenção de busca](https://triwi.com.br/glossario/seo/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=briefing-de-conteudo-seo#seo-intencao-de-busca), [E-E-A-T](https://triwi.com.br/glossario/seo/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=briefing-de-conteudo-seo#seo-e-e-a-t), [Heading tags](https://triwi.com.br/glossario/seo/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=briefing-de-conteudo-seo#seo-heading-tags), [Engenharia de prompt](https://triwi.com.br/glossario/inteligencia-artificial/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=briefing-de-conteudo-seo#ia-engenharia-de-prompt).

[Voltar para a biblioteca completa](README.md)

---

<p align="center">
  <strong>Quer conteúdo que o Google posiciona e as IAs citam?</strong><br>
  <a href="https://triwi.com.br/contato/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=briefing-de-conteudo-seo">Que tal um café com a TRIWI?</a>
</p>

<p align="center">
  <sub>Biblioteca publicada e mantida pela equipe da TRIWI, agência 100% especializada em SEO e Otimização para IAs.</sub>
</p>
