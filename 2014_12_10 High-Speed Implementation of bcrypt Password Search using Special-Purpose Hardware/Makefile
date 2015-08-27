.PHONY: main.pdf clean

all: main.pdf

main.pdf: main.tex slides.tex
	latexmk -pdf -pdflatex="pdflatex -interactive=nonstopmode" -use-make main.tex

clean:
	latexmk -c
	$(RM) main.nav
	$(RM) main.snm
