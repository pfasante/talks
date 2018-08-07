all: main.pdf

main.pdf: main.tex
	cp ../correct_logo.pdf logo.pdf
	cp ../correct_wortmarke.pdf wortmarke.pdf
	latexmk -pdf -use-make main.tex
	cp ../censored_logo.pdf logo.pdf
	cp ../censored_wortmarke.pdf wortmarke.pdf

clean:
	latexmk -c
	rm -rf main.bbl
	rm -rf main.nav
	rm -rf main.run.xml
	rm -rf main.snm

.PHONY: main.pdf all clean
