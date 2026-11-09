# Prompts para criar FAQ e perguntas frequentes com IA

**Uma boa FAQ responde as perguntas que o cliente faz de verdade, cada uma completa na primeira frase e apoiada só em informação da empresa. Os prompts desta página criam a FAQ de uma página, transformam o histórico do atendimento em perguntas e revisam uma FAQ já publicada.**

São três prompts em português, cada um com objetivo, campos a preencher, o prompt pronto para copiar e o alerta do que a IA pode errar. Todos funcionam no ChatGPT, no Claude, no Gemini e em outras IAs de conversa. A biblioteca completa, com 24 prompts em 8 tarefas, está no [README](README.md).

Desde 7 de maio de 2026, o Google não mostra mais o resultado enriquecido de perguntas frequentes, como registram as [Atualizações do Google](https://triwi.com.br/atualizacoes/google/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=faq) da TRIWI. A FAQ continua valendo pelo que responde ao leitor e às IAs.

*Por equipe de SEO da TRIWI, com revisão de Ricardo Martins, fundador. Publicado em 09/11/2026. Atualizado em 09/11/2026.*

## Índice

- [Prompt para criar as perguntas frequentes de uma página](#prompt-para-criar-as-perguntas-frequentes-de-uma-página)
- [Prompt para transformar o histórico do atendimento em FAQ](#prompt-para-transformar-o-histórico-do-atendimento-em-faq)
- [Prompt para revisar uma FAQ que já está publicada](#prompt-para-revisar-uma-faq-que-já-está-publicada)
- [O que a TRIWI tem sobre perguntas frequentes (FAQ)?](#o-que-a-triwi-tem-sobre-perguntas-frequentes-faq)
- [Perguntas frequentes](#perguntas-frequentes)

## Prompt para criar as perguntas frequentes de uma página

**Objetivo:** Escrever uma FAQ com as perguntas que o cliente faz de verdade e respostas curtas, completas na primeira frase e apoiadas só em informação da empresa.

**Campos a preencher:** troque cada campo entre colchetes pela informação real antes de enviar.

| Campo | O que colocar |
|:---|:---|
| `[PÁGINA]` | O endereço ou o tema da página |
| `[EMPRESA]` | Nome da empresa ou da marca |
| `[OFERTA]` | O que a empresa vende |
| `[PÚBLICO]` | Quem compra |
| `[PERGUNTAS DO ATENDIMENTO]` | Dúvidas reais recebidas por atendimento e vendas |
| `[PALAVRA PRINCIPAL]` | A busca principal da página |
| `[PERGUNTAS DA SERP]` | As perguntas do bloco de perguntas relacionadas do Google |
| `[INFORMAÇÕES DA EMPRESA]` | Políticas, prazos, condições e fatos que as respostas podem usar |

**Prompt pronto para copiar:**

```text
Crie as perguntas frequentes da página [PÁGINA] da empresa [EMPRESA], que vende [OFERTA] para [PÚBLICO].

Use como base, nesta ordem de prioridade:
1. As perguntas reais que o atendimento e vendas recebem: [PERGUNTAS DO ATENDIMENTO]
2. As perguntas relacionadas que o Google mostra para a busca [PALAVRA PRINCIPAL]: [PERGUNTAS DA SERP]
3. O que a página não responde e o comprador precisa saber.

Para cada pergunta:
1. Escreva a pergunta como o cliente pergunta, não como a empresa gostaria.
2. Responda na primeira frase, de forma completa, em até 60 palavras no total.
3. Use só a informação deste material: [INFORMAÇÕES DA EMPRESA]. Onde faltar, escreva "a confirmar com a empresa".

Entregue de oito a doze perguntas, sem repetir o que o corpo da página já responde com destaque.
```

> **O que a IA pode errar:** A IA responde perguntas sobre prazo, valor, garantia e política com informação plausível e inventada, e a FAQ é um dos trechos mais copiados por buscadores e IAs. Toda resposta precisa ser conferida por alguém da empresa. O resultado enriquecido de perguntas frequentes deixou de aparecer no Google em 7 de maio de 2026: a FAQ vale pelo que responde ao leitor e às IAs, não por um destaque visual na busca.

**Na TRIWI:** [Skill: criar conteúdo para SEO e IA](https://triwi.com.br/skills/criar-conteudo-para-seo-e-ia/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=faq-e-perguntas-frequentes), skill da TRIWI para instalar no Claude ou no ChatGPT, com a versão completa desta tarefa.

**Fonte oficial citada no alerta:** [Atualizações da documentação da Pesquisa Google, entrada de 8 de maio de 2026 (Google Search Central)](https://developers.google.com/search/updates?hl=pt-br), consultada em 09/11/2026.

<sub>Código do prompt: FAQ-01. Atualizado em 09/11/2026.</sub>

## Prompt para transformar o histórico do atendimento em FAQ

**Objetivo:** Agrupar as mensagens do atendimento por dúvida de fundo e transformar as mais frequentes em perguntas e respostas-modelo.

**Campos a preencher:** troque cada campo entre colchetes pela informação real antes de enviar.

| Campo | O que colocar |
|:---|:---|
| `[EMPRESA]` | Nome da empresa ou da marca |
| `[MENSAGENS]` | Mensagens do atendimento, sem nome, e-mail, telefone, documento ou número de pedido |
| `[POLÍTICAS DA EMPRESA]` | Regras de troca, prazo, pagamento, suporte e demais políticas oficiais |

**Prompt pronto para copiar:**

```text
Abaixo estão mensagens reais recebidas pelo atendimento da empresa [EMPRESA] (e-mails, chats e chamados), já sem dados pessoais:
[MENSAGENS]

Tarefa:
1. Agrupe as mensagens por dúvida de fundo, mesmo quando escritas de jeitos diferentes.
2. Ordene os grupos pela quantidade de mensagens.
3. Para cada grupo, escreva a pergunta na forma mais comum em que ela aparece e uma resposta-modelo que use só o que está nestas políticas: [POLÍTICAS DA EMPRESA].
4. Separe as dúvidas que indicam problema no produto ou na comunicação, e não falta de FAQ.

Não reproduza nome, e-mail, telefone, documento ou qualquer dado que identifique pessoas.
```

> **O que a IA pode errar:** Retire os dados pessoais antes de colar: nome, e-mail, telefone, documento e número de pedido não devem ir para a IA, pela LGPD e pela política da própria empresa. A IA também junta dúvidas diferentes num grupo só porque usam as mesmas palavras; confira os grupos maiores lendo algumas mensagens de cada um.

**Na TRIWI:** [LGPD e IA, no blog da TRIWI](https://triwi.com.br/lgpd-e-ia-interseccoes-lacunas-e-o-que-as-empresas-precisam-saber-agora/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=faq-e-perguntas-frequentes), artigo do blog da TRIWI.

**Fonte oficial citada no alerta:** [Autoridade Nacional de Proteção de Dados (ANPD)](https://www.gov.br/anpd/pt-br), consultada em 09/11/2026.

<sub>Código do prompt: FAQ-02. Atualizado em 09/11/2026.</sub>

## Prompt para revisar uma FAQ que já está publicada

**Objetivo:** Encontrar perguntas mal escritas, respostas que demoram a responder, informação desatualizada e repetições, sem mudar fatos sem confirmação.

**Campos a preencher:** troque cada campo entre colchetes pela informação real antes de enviar.

| Campo | O que colocar |
|:---|:---|
| `[PÁGINA]` | O endereço ou o tema da página |
| `[FAQ ATUAL]` | As perguntas e respostas como estão publicadas |

**Prompt pronto para copiar:**

```text
Revise as perguntas frequentes abaixo, publicadas na página [PÁGINA]:
[FAQ ATUAL]

Para cada pergunta, diga:
1. Se ela está escrita como o cliente pergunta ou como a empresa fala.
2. Se a resposta responde já na primeira frase.
3. Se há informação que pode estar desatualizada (prazo, valor, regra, data) e precisa ser conferida.
4. Se ela repete outra pergunta da lista ou o corpo da página.
5. A versão revisada, quando precisar.

No fim, liste as perguntas que faltam e as que podem sair.

Não altere fatos. Onde achar que um fato está errado, aponte e peça confirmação.
```

> **O que a IA pode errar:** A IA corrige o estilo e, no caminho, muda fatos: arredonda prazos, troca condições, generaliza regras. Revise as respostas novas contra as antigas, frase por frase, antes de publicar. Se a página tem dados estruturados de perguntas frequentes, o JSON-LD precisa repetir o texto revisado que está visível na página.

**Na TRIWI:** [Gerador de dados estruturados](https://triwi.com.br/ferramentas/gerador-de-dados-estruturados/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=faq-e-perguntas-frequentes), ferramenta gratuita da TRIWI, no navegador e sem cadastro.

<sub>Código do prompt: FAQ-03. Atualizado em 09/11/2026.</sub>

## O que a TRIWI tem sobre perguntas frequentes (FAQ)?

Os prompts desta página são a versão curta e aberta. Para o método completo, a TRIWI publica de graça:

| Recurso | Tipo | O que faz |
|:---|:---|:---|
| [Skill: criar conteúdo para SEO e IA](https://triwi.com.br/skills/criar-conteudo-para-seo-e-ia/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=faq-e-perguntas-frequentes) | Skill | Conduz a escrita de artigos, guias e páginas pensados para a busca e para as respostas de IA |
| [Gerador de dados estruturados](https://triwi.com.br/ferramentas/gerador-de-dados-estruturados/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=faq-e-perguntas-frequentes) | Ferramenta | Monta o JSON-LD de organização, artigo, produto, empresa local e outros tipos, pronto para colar |
| [Atualizações do Google](https://triwi.com.br/atualizacoes/google/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=faq-e-perguntas-frequentes) | Atualizações | Core updates, spam updates e mudanças de recursos da busca do Google, com data e fonte |
| [LGPD e IA, no blog da TRIWI](https://triwi.com.br/lgpd-e-ia-interseccoes-lacunas-e-o-que-as-empresas-precisam-saber-agora/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=faq-e-perguntas-frequentes) | Artigo | O que a proteção de dados muda no uso de IA pelas empresas |

## Perguntas frequentes

<details>
<summary><strong>Ainda vale ter FAQ depois que o Google tirou o resultado de perguntas frequentes?</strong></summary>

Vale. O que saiu foi o destaque visual na busca, não a utilidade da FAQ: ela continua respondendo as objeções de quem está decidindo e é um formato que as IAs aproveitam bem como trecho de resposta.
</details>

<details>
<summary><strong>A IA pode escrever as respostas da FAQ sozinha?</strong></summary>

Pode redigir, mas não pode decidir os fatos. Prazo, valor, condição e política têm de vir da empresa e passar por quem responde por eles. Por isso os prompts pedem a informação da empresa como campo e marcam o que falta como a confirmar.
</details>

<details>
<summary><strong>Esta biblioteca traz o código JSON-LD da FAQ?</strong></summary>

Não. Os prompts cuidam do texto. Para gerar o JSON-LD, use o [Gerador de dados estruturados](https://triwi.com.br/ferramentas/gerador-de-dados-estruturados/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=faq) da TRIWI; o tema está explicado no guia aberto [Schema Markup e Dados Estruturados para SEO](https://github.com/TRIWI-SEO/SEO-IA/blob/main/seo-tecnico/schema-markup-e-dados-estruturados-para-seo.md).
</details>

**Ver também na Base de Conhecimento da TRIWI:** [Schema Markup e Dados Estruturados para SEO](https://github.com/TRIWI-SEO/SEO-IA/blob/main/seo-tecnico/schema-markup-e-dados-estruturados-para-seo.md), [Dados Estruturados para IA](https://github.com/TRIWI-SEO/SEO-IA/blob/main/geo-seo-para-ia/dados-estruturados-para-ia-schema-markup-na-era-generativa.md), [Conteúdo Citável](https://github.com/TRIWI-SEO/SEO-IA/blob/main/geo-seo-para-ia/conteudo-citavel-como-escrever-para-ser-referenciado-por-llms.md).

**Ver também no Glossário da TRIWI:** [FAQPage](https://triwi.com.br/glossario/seo/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=faq-e-perguntas-frequentes#seo-faqpage), [People Also Ask](https://triwi.com.br/glossario/seo/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=faq-e-perguntas-frequentes#seo-people-also-ask), [Featured snippet](https://triwi.com.br/glossario/seo/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=faq-e-perguntas-frequentes#seo-featured-snippet), [Dados estruturados](https://triwi.com.br/glossario/seo/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=faq-e-perguntas-frequentes#seo-dados-estruturados), [Prompt](https://triwi.com.br/glossario/inteligencia-artificial/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=faq-e-perguntas-frequentes#ia-prompt).

[Voltar para a biblioteca completa](README.md)

---

<p align="center">
  <strong>Quer que as respostas sobre o seu mercado venham da sua empresa?</strong><br>
  <a href="https://triwi.com.br/contato/?utm_source=github&utm_medium=referral&utm_campaign=repo-prompts-seo-geo&utm_content=faq-e-perguntas-frequentes">Que tal um café com a TRIWI?</a>
</p>

<p align="center">
  <sub>Biblioteca publicada e mantida pela equipe da TRIWI, agência 100% especializada em SEO e Otimização para IAs.</sub>
</p>
