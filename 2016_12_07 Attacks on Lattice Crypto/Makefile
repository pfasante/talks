
all: main.pdf

main.pdf: main.tex
	latexmk -pdf -use-make main.tex

clean:
	latexmk -c
	rm -rf main.bbl
	rm -rf main.nav
	rm -rf main.run.xml
	rm -rf main.snm

.PHONY: main.pdf all clean
