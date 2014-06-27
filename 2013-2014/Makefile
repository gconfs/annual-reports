REPORTS=rapport_zeletochoy.pdf
REPORTS+=rapport_seirl.pdf
REPORTS+=rapport_bruce.pdf
REPORTS+=rapport_dettorer.pdf

UPLOADED_FILES=$(REPORTS) logo_gconfs.png eval_s1.pdf eval_s2.pdf

all: report.pdf

downloads: $(UPLOADED_FILES)

report.pdf: downloads report.tex
	pdflatex report.tex
	pdflatex report.tex

$(UPLOADED_FILES):
	wget 'http://gconfs.fr/tmp/$@'

clean:
	rm -f report.{toc,aux,log} $(UPLOADED_FILES)

distclean: clean
	rm -f report.pdf

.PHONY: all clean distclean
