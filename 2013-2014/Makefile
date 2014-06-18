all: report.pdf

report.pdf: logo_gconfs.png report.tex
	pdflatex report.tex

logo_gconfs.png:
	wget 'http://gconfs.fr/tmp/logo_gconfs.png'

clean:
	rm -f report.{toc,aux,log} logo_gconfs.png

distclean: clean
	rm report.pdf

.PHONY: all clean distclean
