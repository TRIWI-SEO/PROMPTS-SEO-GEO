# Dicionário de Dados: Biblioteca Aberta de Prompts para SEO e GEO da TRIWI

Este dicionário descreve a base [prompts.csv](prompts.csv), a versão em dados da biblioteca [Prompts para SEO e GEO](../README.md): o que cada coluna significa, como o arquivo é formatado e como a base é mantida. A base está sob licença [CC BY 4.0](../LICENSE): o reuso é livre, inclusive comercial, desde que a TRIWI seja citada como fonte.

*Por equipe de SEO da TRIWI. Atualizado em 09/11/2026.*

## Quais bases existem?

| Arquivo | O que traz | Linhas |
|:---|:---|:---|
| [prompts.csv](prompts.csv) | Prompts para SEO e GEO, com código, tarefa, objetivo, texto completo, campos a preencher, alerta, recurso da TRIWI do mesmo tema e fonte oficial do alerta | 30 |

## Como abrir o arquivo?

O arquivo segue o mesmo padrão das outras bases abertas da TRIWI: codificação UTF-8, colunas separadas por vírgula, quebra de linha CRLF e datas no formato AAAA-MM-DD. Listas dentro de uma célula são separadas por ponto e vírgula.

A coluna prompt guarda o texto com as quebras de linha originais, entre aspas, como manda o padrão do formato. Se o Excel mostrar os acentos embaralhados, abra pelo menu Dados, opção De Texto/CSV, e escolha a codificação UTF-8.

## O que significa cada coluna?

| Coluna | Significado |
|:---|:---|
| id | Código do prompt, formado pela sigla da tarefa e um número, como KW-01; não muda depois de publicado |
| tarefa | Tarefa a que o prompt pertence: Pesquisa de palavras-chave; Análise de concorrência na SERP; Briefing de conteúdo; Conteúdo citado por IAs; Perguntas frequentes (FAQ); Títulos e descrições; Links internos; Auditoria de página; Relatório de SEO; Medição de presença nas IAs |
| titulo | Nome do prompt, igual ao título da seção na página da tarefa |
| objetivo | O que o prompt resolve, em uma frase |
| prompt | O texto completo, pronto para copiar, com os campos a preencher entre colchetes |
| campos | Lista dos campos entre colchetes e do que colocar em cada um, separados por ponto e vírgula, no formato [CAMPO]: descrição |
| alerta | O que a IA pode errar ao executar o prompt e como conferir |
| recurso_triwi_tipo | Tipo do recurso da TRIWI do mesmo tema: Artigo; Atualizações; Base de Conhecimento; Checklist; Ferramenta; Guia; Skill |
| recurso_triwi_nome | Nome do recurso da TRIWI |
| recurso_triwi_url | Endereço do recurso da TRIWI, sem parâmetro de campanha |
| fonte_oficial | Documentação oficial que sustenta o alerta, quando ele depende de uma regra de plataforma ou de lei; mais de uma fonte vem separada por ponto e vírgula; n/d quando o alerta descreve o comportamento da IA observado no uso |
| pagina | Arquivo da página da tarefa em que o prompt é publicado |
| atualizado_em | Data da última revisão da linha |

**Critério de contagem:** cada linha é um prompt com código próprio. Variações de um mesmo prompt (outro tom, outro tamanho) não viram linha nova; quando um prompt muda de propósito, ganha código novo e o antigo sai da base.

## Como a base é mantida?

A base é revisada pela equipe da TRIWI. Fontes oficiais citadas nos alertas são conferidas na data de revisão de cada linha; quando a regra de uma plataforma muda, o alerta é reescrito e a data é atualizada. Correções e sugestões chegam por [issue](../../../issues/new).
