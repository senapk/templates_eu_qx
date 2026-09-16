# Makefile para compilar o template LaTeX

TARGET = main
LATEX = pdflatex
BIBER = biber

.PHONY: all pdf clean help

all: pdf

help:
	@echo "Comandos disponíveis:"
	@echo "  make pdf     - compila o documento em PDF"
	@echo "  make clean   - remove arquivos temporários e o PDF gerado"
	@echo "  make help    - mostra esta ajuda"

pdf: $(TARGET).pdf

$(TARGET).pdf: $(TARGET).tex estilo.sty referencias.bib
	@echo "==> Compilando LaTeX..."
	$(LATEX) -interaction=nonstopmode -synctex=1 $(TARGET).tex
	@echo "==> Processando bibliografia..."
	$(BIBER) $(TARGET)
	@echo "==> Atualizando referências..."
	$(LATEX) -interaction=nonstopmode -synctex=1 $(TARGET).tex
	$(LATEX) -interaction=nonstopmode -synctex=1 $(TARGET).tex
	@echo "==> PDF gerado: $(TARGET).pdf"

clean:
	@echo "==> Removendo arquivos temporários..."
	rm -f *.aux *.bbl *.bcf *.blg *.fdb_latexmk *.fls *.log *.out *.run.xml *.synctex.gz *.toc *.pdf
