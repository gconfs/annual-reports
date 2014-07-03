REPORTS=rapport_zeletochoy.pdf
REPORTS+=rapport_seirl.pdf
REPORTS+=rapport_bruce.pdf
REPORTS+=rapport_dettorer.pdf
REPORTS+=rapport_toogy.pdf
REPORTS+=rapport_nitnelave.pdf

EVAL=eval_s1.xls eval_s2.xls

UPLOADED_FILES=$(REPORTS) $(EVAL) logo_gconfs.png

all: report.pdf

downloads: $(UPLOADED_FILES)

report.pdf: downloads report.tex
	pdflatex report.tex
	pdflatex report.tex

$(UPLOADED_FILES):
	wget 'http://gconfs.fr/tmp/$@'

clean:
	rm -f report.{toc,aux,log} $(REPORTS) logo_gconfs.png

distclean: clean
	rm -f report.pdf $(UPLOADED_FILES)

.PHONY: all clean distclean
