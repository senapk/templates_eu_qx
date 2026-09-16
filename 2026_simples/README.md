# Template de Resumo Simples em LaTeX

Este diretório contém um template em LaTeX para produção de resumo simples, com formatação acadêmica, suporte a instruções de revisão por cores e estrutura pronta para compilar.

As instruções gerais de instalação e compilação estão no [README principal](../README.md).

Estrutura principal:

- `main.tex` — arquivo principal do documento
- `resumo.sty` — estilo e configurações do template
- `header.pdf` — cabeçalho visual opcional do documento

## Especificidades do template

- Mantenha o arquivo `main.tex` aberto e edite o título, autores, e-mails, texto do resumo, palavras-chave e ODS.
- O resumo deve ser escrito em um único parágrafo, com 2.000 a 3.000 caracteres, incluindo palavras-chave e ODS.
- Informe de três a cinco palavras-chave, iniciadas por letra minúscula e separadas por ponto e vírgula.
- Informe apenas um Objetivo de Desenvolvimento Sustentável (ODS), usando a nomenclatura oficial em letra minúscula. Consulte: https://brasil.un.org/pt-br/sdgs
- O modelo aceita trabalhos de pesquisa e relatos de experiência, desde que apresente objetivo, desenvolvimento, resultados e conclusões.
- A linha `\EnableReviewColors` mantém cores para orientar a revisão do texto. Antes da submissão, comente essa linha ou substitua-a por `\DisableReviewColors`.
- O arquivo `header.pdf` é carregado automaticamente quando está presente no diretório do projeto.

## Observação

Este template foi preparado para um fluxo acadêmico de resumo simples. A formatação de margens, fonte, espaçamento, título, autores e cabeçalho é aplicada automaticamente pelo arquivo `resumo.sty`; evite alterar manualmente esses elementos no `main.tex`.
