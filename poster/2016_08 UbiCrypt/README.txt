Important files:
main.tex:
	you should not need to change anything here

settings.tex:
	this file is included in the preamble of main.tex
	so, you can load your packages here, define commands, ... what ever you do

content.tex:
	this file is included in the document body of the poster.
	so your content goes here -- well, thats obvious I guess ;)

biblio.bib:
	guess what, this can be your bibliography (if you need one..)

TODO for you:
	check settings.tex and adjust header (that is: title, author, advisors)


CHANGELOG:
v0.3
	changed poster header.
		It should only contain your name and your advisors (note the new advisors
		command in settings.tex instead of the previous \institute)
	changed background of motivation box to match grey background of header/footer
	corrected Typo in Acknowlegdements (it should say UbiCrypt)
v0.2
	changed math font to eulervm
	changed bibtex to biblatex
		(if you encounter problems, you might not have biber on your system
		(thats the "new" backend to process bibliographies). You can then
		change the backend for biblatex back to bibtex, by editing the main.tex.
		replace:
			\usepackage[%
				backend=biber,
				% ...
			]{biblatex}
		with:
			\usepackage[%
				backend=bibtex,
				% ...
			]{biblatex}
		If this still don't work, drop me an email or figure it out by yourself.
v0.1
	initial version
