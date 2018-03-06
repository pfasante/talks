.PHONY: main.pdf clean

all: main.pdf

main.pdf: main.tex settings.tex content.tex
	latexmk -pdf main

clean:
	latexmk -c
	$(RM) main.nav
	$(RM) main.run.xml
	$(RM) main.bbl
	$(RM) main.snm
