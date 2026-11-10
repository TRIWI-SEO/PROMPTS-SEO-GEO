# Prompts para links internos de SEO no ChatGPT, Claude e Gemini

**Links internos dizem ao Google e às IAs quais páginas importam e como os assuntos do site se conectam. A IA ajuda a planejar e revisar esses links quando recebe a lista real de páginas do site; sem ela, inventa URLs. Os prompts desta página planejam os links de uma página nova, revisam textos âncora e acham páginas órfãs.**

São três prompts em português, cada um com objetivo, campos a preencher, o prompt pronto para copiar e o alerta do que a IA pode errar. Todos funcionam no ChatGPT, no Claude, no Gemini e em outras IAs de conversa. A biblioteca completa, com 30 prompts em 10 tarefas, está no [README](README.md).

*Por equipe de SEO da TRIWI, com revisão de Ricardo Martins, fundador. Publicado em 09/11/2026. Atualizado em 09/11/2026.*

## Índice

- [Prompt para planejar os links internos de uma página nova](#prompt-para-planejar-os-links-internos-de-uma-página-nova)
- [Prompt para revisar os textos âncora de uma página](#prompt-para-revisar-os-textos-âncora-de-uma-página)
- [Prompt para encontrar páginas órfãs e páginas com poucos links](#prompt-para-encontrar-páginas-órfãs-e-páginas-com-poucos-links)
- [Qual o próximo passo?](#qual-o-próximo-passo)
- [O que a TRIWI tem sobre links internos?](#o-que-a-triwi-tem-sobre-links-internos)
- [Perguntas frequentes](#perguntas-frequentes)

## Prompt para planejar os links internos de uma página nova

**Objetivo:** Decidir quais páginas do site devem apontar para um conteúdo novo, com que texto âncora, e para quais páginas ele deve apontar.

**Campos a preencher:** troque cada campo entre colchetes pela informação real antes de enviar.

| Campo | O que colocar |
|:---|:---|
| `[SITE]` | O domínio do site |
| `[URL NOVA]` | O endereço da página nova |
| `[ASSUNTO DA PÁGINA NOVA]` | O tema e a busca principal da página nova |
| `[PÁGINAS DO SITE]` | Uma linha por página existente, com URL, título e busca principal |

**Prompt pronto para copiar:**

```text
Vou publicar uma página nova no site [SITE] e preciso planejar os links internos dela.

Página nova:
- Endereço: [URL NOVA]
- Assunto e busca principal: [ASSUNTO DA PÁGINA NOVA]

Páginas que já existem no site (URL, título e busca principal de cada uma):
[PÁGINAS DO SITE]

Tarefa:
1. Liste as páginas existentes que deveriam linkar para a página nova, com o motivo, o trecho onde o link entra e o texto âncora sugerido.
2. Liste as páginas existentes para as quais a página nova deveria linkar, com o mesmo detalhe.
3. Indique qual página funciona como página central do tema (a que reúne o assunto) e se a página nova deve ficar abaixo dela.

Regras:
1. Use só URLs da lista. Não invente endereços.
2. O texto âncora descreve o destino, é conciso e não repete a mesma palavra-chave exata em todos os links.
3. Nada de "clique aqui" ou "leia mais".
4. Só sugira link onde ele ajuda quem está lendo aquele trecho.
```

> **O que a IA pode errar:** A IA inventa URLs que parecem existir e sugere links entre páginas sem relação só porque dividem uma palavra. Ela também tende a repetir a mesma âncora com a palavra-chave exata, o que o Google desaconselha. Confira que cada URL sugerida abre e leia cada link no trecho em que ele entra antes de publicar.

**Na TRIWI:** [Planejador de arquitetura SEO](https://triwi.com.br/ferramentas/planejador-de-arquitetura-seo/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=links-internos-seo), ferramenta gratuita da TRIWI, no navegador e sem cadastro.

**Fonte oficial citada no alerta:** [Práticas recomendadas de links para o Google (Google Search Central)](https://developers.google.com/search/docs/crawling-indexing/links-crawlable?hl=pt-br), consultada em 09/11/2026.

<sub>Código do prompt: LI-01. Atualizado em 09/11/2026.</sub>

## Prompt para revisar os textos âncora de uma página

**Objetivo:** Encontrar âncoras genéricas, enganosas ou forçadas numa página e propor textos que descrevem o destino de cada link.

**Campos a preencher:** troque cada campo entre colchetes pela informação real antes de enviar.

| Campo | O que colocar |
|:---|:---|
| `[SITE]` | O domínio do site |
| `[CONTEÚDO COM LINKS]` | O texto da página com os links visíveis, ou o HTML |
| `[TÍTULOS DOS DESTINOS]` | URL e título de cada página que recebe link |

**Prompt pronto para copiar:**

```text
Revise os links internos da página abaixo, do site [SITE].

Conteúdo da página, com os links (texto âncora e URL de destino):
[CONTEÚDO COM LINKS]

Título de cada página de destino:
[TÍTULOS DOS DESTINOS]

Para cada link, entregue numa tabela: texto âncora atual; URL de destino; problema (genérico, não descreve o destino, palavra-chave forçada, link repetido, nenhum); texto âncora sugerido.

Depois, aponte:
1. Trechos que falam de um assunto que tem página no site e estão sem link.
2. Links que podem sair porque não ajudam o leitor naquele ponto.

Use só os destinos da lista. Não sugira links para páginas que não estão nela.
```

> **O que a IA pode errar:** Sem o título das páginas de destino, a IA deduz do que cada uma trata pela URL e sugere âncoras que prometem outra coisa. Ela também troca âncoras naturais por palavra-chave exata, o que soa forçado para o leitor. O teste é o do Google: lido sozinho, o texto âncora tem de dizer do que trata a página de destino.

**Na TRIWI:** [Analisador de links internos](https://triwi.com.br/ferramentas/analisador-de-links-internos/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=links-internos-seo), ferramenta gratuita da TRIWI, no navegador e sem cadastro.

**Fonte oficial citada no alerta:** [Práticas recomendadas de links para o Google (Google Search Central)](https://developers.google.com/search/docs/crawling-indexing/links-crawlable?hl=pt-br), consultada em 09/11/2026.

<sub>Código do prompt: LI-02. Atualizado em 09/11/2026.</sub>

## Prompt para encontrar páginas órfãs e páginas com poucos links

**Objetivo:** Cruzar a exportação do rastreador com a lista de páginas que importam e achar as que não recebem link interno nenhum ou recebem poucos.

**Campos a preencher:** troque cada campo entre colchetes pela informação real antes de enviar.

| Campo | O que colocar |
|:---|:---|
| `[SITE]` | O domínio do site |
| `[FERRAMENTA]` | O rastreador usado, como Screaming Frog |
| `[EXPORTAÇÃO DO RASTREADOR]` | URL e número de links internos recebidos por página |
| `[LISTA DE URLS IMPORTANTES]` | As URLs do sitemap ou do relatório de páginas do Search Console |

**Prompt pronto para copiar:**

```text
Abaixo estão dois arquivos do site [SITE]:

1. Exportação do rastreador [FERRAMENTA], com cada URL encontrada e a quantidade de links internos que ela recebe:
[EXPORTAÇÃO DO RASTREADOR]

2. Lista de URLs que deveriam estar no ar e ser encontradas, vinda do sitemap ou do Search Console:
[LISTA DE URLS IMPORTANTES]

Tarefa:
1. Liste as páginas órfãs: estão na lista 2 e não aparecem na exportação do rastreador.
2. Liste as páginas da lista 2 que recebem poucos links internos, da que recebe menos para a que recebe mais.
3. Para cada página das duas listas, sugira de duas a três páginas do site que poderiam linkar para ela, usando só URLs da exportação.
4. Separe as páginas que talvez devam sair do site em vez de receber links (duplicadas, desatualizadas, sem função), com o motivo.

Use só os dados dos dois arquivos. No fim, informe quantas URLs recebeu em cada arquivo e quantas classificou.
```

> **O que a IA pode errar:** Página órfã não aparece no rastreador, justamente porque nenhum link leva a ela: só se encontra cruzando com o sitemap ou com o Search Console, e a IA não faz esse cruzamento sem os dois arquivos. Em listas longas, ela também perde URLs no caminho. Confira se os totais informados no fim batem com os arquivos enviados.

**Na TRIWI:** [Arquitetura de site para SEO](https://github.com/TRIWI-SEO/SEO-IA/blob/main/seo-tecnico/arquitetura-de-site-para-seo.md), guia aberto da Base de Conhecimento da TRIWI no GitHub.

**Fonte oficial citada no alerta:** [Práticas recomendadas de links para o Google (Google Search Central)](https://developers.google.com/search/docs/crawling-indexing/links-crawlable?hl=pt-br), consultada em 09/11/2026.

<sub>Código do prompt: LI-03. Atualizado em 09/11/2026.</sub>

## Qual o próximo passo?

Cada tarefa desta biblioteca é uma etapa do trabalho de SEO e GEO. Depois desta, o caminho natural é:

| Próxima tarefa | Para quê |
|:---|:---|
| [Prompts para auditoria de página de SEO no ChatGPT, Claude e Gemini](prompts-para-auditoria-de-pagina-seo.md) | Conferir a página publicada de ponta a ponta |

## O que a TRIWI tem sobre links internos?

Os prompts desta página são a versão curta e aberta. Para o método completo, a TRIWI publica de graça:

| Recurso | Tipo | O que faz |
|:---|:---|:---|
| [Analisador de links internos](https://triwi.com.br/ferramentas/analisador-de-links-internos/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=links-internos-seo) | Ferramenta | Mapeia a linkagem interna para encontrar páginas órfãs e páginas com poucos links |
| [Planejador de arquitetura SEO](https://triwi.com.br/ferramentas/planejador-de-arquitetura-seo/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=links-internos-seo) | Ferramenta | Desenha a hierarquia de páginas e categorias de um site pensando em busca |
| [Arquitetura de site para SEO](https://github.com/TRIWI-SEO/SEO-IA/blob/main/seo-tecnico/arquitetura-de-site-para-seo.md) | Base de Conhecimento | Como organizar páginas, categorias e links para o Google entender o site |
| [Pilarização e pulverização](https://github.com/TRIWI-SEO/SEO-IA/blob/main/seo-de-conteudo/pilarizacao-e-pulverizacao-a-estrategia-de-conteudo-que-gera-autoridade-topical.md) | Base de Conhecimento | Como páginas centrais e de apoio se ligam para construir autoridade num tema |

## Perguntas frequentes

<details>
<summary><strong>Quantos links internos uma página deve ter?</strong></summary>

Não existe número ideal, segundo a [documentação do Google sobre links](https://developers.google.com/search/docs/crawling-indexing/links-crawlable?hl=pt-br): o que importa é toda página importante receber link de pelo menos uma outra página do site e cada link ajudar quem lê. Se uma página parece ter links demais, provavelmente tem.
</details>

<details>
<summary><strong>Posso usar a palavra-chave exata em todos os textos âncora?</strong></summary>

Não é o recomendado. O Google pede âncoras descritivas e concisas e avisa que forçar palavra-chave no texto âncora pode violar as políticas de spam. Varie o texto e descreva o destino como o leitor entenderia.
</details>

**Ver também na Base de Conhecimento da TRIWI:** [Arquitetura de Site para SEO](https://github.com/TRIWI-SEO/SEO-IA/blob/main/seo-tecnico/arquitetura-de-site-para-seo.md), [Pilarização e Pulverização](https://github.com/TRIWI-SEO/SEO-IA/blob/main/seo-de-conteudo/pilarizacao-e-pulverizacao-a-estrategia-de-conteudo-que-gera-autoridade-topical.md), [SEO On-Page](https://github.com/TRIWI-SEO/SEO-IA/blob/main/fundamentos-de-seo/seo-on-page-otimizacao-dentro-do-seu-site.md).

**Ver também no Glossário da TRIWI:** [Link interno](https://triwi.com.br/glossario/seo/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=links-internos-seo#seo-link-interno), [Texto âncora](https://triwi.com.br/glossario/seo/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=links-internos-seo#seo-texto-ancora), [Página órfã](https://triwi.com.br/glossario/seo/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=links-internos-seo#seo-pagina-orfa), [Arquitetura do site](https://triwi.com.br/glossario/seo/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=links-internos-seo#seo-arquitetura-do-site), [Link equity](https://triwi.com.br/glossario/seo/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=links-internos-seo#seo-link-equity).

[Voltar para a biblioteca completa](README.md)

---

<p align="center">
  <strong>Quer um site que o Google entende e as IAs citam?</strong><br>
  <a href="https://triwi.com.br/contato/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=links-internos-seo">Que tal um café com a TRIWI?</a>
</p>

<p align="center">
  <sub>Biblioteca publicada e mantida pela equipe da TRIWI, agência 100% especializada em SEO e Otimização para IAs.</sub>
</p>
