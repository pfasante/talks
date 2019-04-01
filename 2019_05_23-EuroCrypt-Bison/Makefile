all: main.pdf

main.pdf: main.tex data/spn.pdf data/differential-characteristic.pdf data/differential.pdf
	cp ../correct_logo.pdf logo.pdf
	cp ../correct_wortmarke.pdf wortmarke.pdf
	latexmk -pdf -use-make main.tex
	cp ../censored_logo.pdf logo.pdf
	cp ../censored_wortmarke.pdf wortmarke.pdf

data/spn.pdf: data/spn.tex
	cd data && latexmk -pdf spn.tex && cd ..

data/differential-characteristic.pdf: data/differential-characteristic.tex
	cd data && latexmk -pdf differential-characteristic.tex && cd ..

data/differential.pdf: data/differential.tex
	cd data && latexmk -pdf differential.tex && cd ..

clean:
	latexmk -c
	cd data && latexmk -c && cd ..
	rm -rf main.bbl
	rm -rf main.nav
	rm -rf main.run.xml
	rm -rf main.snm

.PHONY: main.pdf all clean
