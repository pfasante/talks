
all: main.pdf

plots: data/plots/sbox_serpent0_16n_10r_graph_inkscape.pdf data/plots/sbox_serpent1_16n_10r_graph_inkscape.pdf data/plots/sbox_serpent2_16n_10r_graph_inkscape.pdf data/plots/convergence_r1.pdf data/plots/convergence_r2.pdf data/plots/constant_round_keys.pdf data/plots/independent_round_keys.pdf data/plots/sbox_serpent0_16n_10r.pdf data/plots/sbox_serpent1_16n_10r.pdf data/plots/sbox_serpent2_16n_11r.pdf data/plots/sbox_serpent2_16n_10r.pdf data/plots/smallpresent4.pdf data/plots/smallpresent4_3r.pdf data/plots/smallpresent4_3r_hl.pdf data/plots/ssaes.pdf

data/plots/%.pdf: data/plots/%.tex
	latexmk -pdf -pdflatex="pdflatex -shell-escape" -use-make $(patsubst %.pdf,%.tex,$@)
	mv -t data/plots $(patsubst data/plots/%,%,$@)
	rm -f *.aux *.fdb_latexmk *.fls *.log

main.pdf: plots main.tex section1.tex section2.tex section3.tex section4.tex section5.tex
	latexmk -pdf -pdflatex="pdflatex -interactive=nonstopmode" -use-make main.tex

clean:
	latexmk -c
	rm -rf main.bbl
	rm -rf main.nav
	rm -rf main.run.xml
	rm -rf main.snm

clean-all: clean
	rm -rf data/plots/*.pdf

.PHONY: main.pdf all clean
