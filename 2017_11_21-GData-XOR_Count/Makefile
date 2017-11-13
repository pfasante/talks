
all: main.pdf

main.pdf: first.tex second.tex
	cp ../correct_logo.pdf logo.pdf
	cp ../correct_wortmarke.pdf wortmarke.pdf
	latexmk -pdf -use-make first.tex
	latexmk -pdf -use-make second.tex
	cp ../censored_logo.pdf logo.pdf
	cp ../censored_wortmarke.pdf wortmarke.pdf
	pdftk first.pdf cat 1-23 output start.pdf
	pdftk start.pdf second.pdf output main.pdf
	rm -rf start.pdf

clean:
	latexmk -c
	rm -rf first.bbl
	rm -rf first.nav
	rm -rf first.run.xml
	rm -rf first.snm
	rm -rf second.bbl
	rm -rf second.nav
	rm -rf second.run.xml
	rm -rf second.snm

.PHONY: main.pdf all clean
