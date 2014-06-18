REPORTS=rapport_zeletochoy.pdf
# REPORTS+=rapport_seirl.pdf

all: report.pdf

report.pdf: logo_gconfs.png report.tex $(REPORTS)
	pdflatex report.tex
	pdflatex report.tex

rapport_%.pdf:
	wget 'http://gconfs.fr/tmp/$@'

logo_gconfs.png:
	wget 'http://gconfs.fr/tmp/logo_gconfs.png'

clean:
	rm -f report.{toc,aux,log} logo_gconfs.png $(REPORTS)

distclean: clean
	rm report.pdf

.PHONY: all clean distclean
