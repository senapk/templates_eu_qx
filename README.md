# Templates de Resumos em LaTeX

Este repositório reúne dois templates em LaTeX para produção de trabalhos acadêmicos:

- `2026_expandido/` — template de resumo expandido, com seções, referências bibliográficas, figuras, tabelas e outros elementos de um trabalho científico.
- `2026_simples/` — template de resumo simples, organizado em um único texto com orientações para contexto, desenvolvimento, resultados e conclusões.

Consulte o README de cada pasta para conhecer as regras e especificidades do respectivo template:

- [README do resumo expandido](2026_expandido/README.md)
- [README do resumo simples](2026_simples/README.md)

## Requisitos

Para compilar os templates, é necessária uma instalação do LaTeX com:

- compilador LaTeX (`pdflatex`);
- pacotes extras do LaTeX, incluindo suporte à língua portuguesa, fontes, cores e elementos gráficos;
- `biber`, necessário para a bibliografia do template de resumo expandido.

## Instalação do LaTeX

Se o sistema ainda não tiver o LaTeX instalado, use uma das opções abaixo.

<details>
<summary><strong>Windows</strong></summary>

### MiKTeX

1. Acesse https://miktex.org/download.
2. Baixe e execute o instalador do MiKTeX.
3. Na instalação, marque a opção para instalar automaticamente pacotes ausentes.
4. Confirme a instalação no terminal:

```powershell
pdflatex --version
biber --version
```

### VS Code

Instale a extensão "LaTeX Workshop" para compilar e visualizar os documentos diretamente no editor.

</details>

<details>
<summary><strong>Linux</strong></summary>

### Ubuntu / Debian

```bash
sudo apt update
sudo apt install -y texlive-latex-base texlive-latex-extra texlive-lang-portuguese texlive-bibtex-extra biber
```

### Fedora

```bash
sudo dnf install -y texlive-scheme-full biber
```

### Arch Linux

```bash
sudo pacman -S texlive-most biber
```

### Verificação

```bash
pdflatex --version
biber --version
```

</details>

## Compilar os projetos

Os comandos devem ser executados dentro da pasta do template escolhido.

### VS Code

Abra o arquivo `main.tex` da pasta desejada no VS Code e use a extensão "LaTeX Workshop" para executar a compilação e visualizar o PDF.

### TexStudio

Abra o arquivo `main.tex` da pasta desejada no TexStudio e use o botão de compilação do programa.

### Terminal: resumo expandido

O resumo expandido possui um `Makefile` que executa a sequência necessária, incluindo o processamento da bibliografia:

```bash
cd 2026_expandido
make
```

Também é possível usar `make pdf`. Para remover os arquivos temporários e o PDF gerado, use `make clean`.

### Terminal: resumo simples

O resumo simples não possui bibliografia nem `Makefile`. Compile-o diretamente com:

```bash
cd 2026_simples
pdflatex -interaction=nonstopmode main.tex
```

## PDF gerado

Em ambos os templates, o arquivo final é gerado como:

```text
main.pdf
```

Se o PDF não refletir alguma alteração, compile novamente. No resumo expandido, mantenha a sequência do `Makefile` para atualizar corretamente as referências.
