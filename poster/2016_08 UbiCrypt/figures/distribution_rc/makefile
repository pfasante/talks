.PHONY: all clean

all: plot.pdf

plot.pdf: plot.tex data/*
	latexmk -pdf plot

clean:
	latexmk -c

clean-all: clean
	$(RM) -f plot.pdf
