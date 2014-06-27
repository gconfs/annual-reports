REPORTS=rapport_zeletochoy.pdf
REPORTS+=rapport_seirl.pdf

UPLOADED_FILES=$(REPORTS) logo_gconfs.png eval_s1.pdf eval_s2.pdf

all: report.pdf

report.pdf: $(UPLOADED_FILES) report.tex
	pdflatex report.tex
	pdflatex report.tex

$(UPLOADED_FILES):
	wget 'http://gconfs.fr/tmp/$@'

clean:
	rm -f report.{toc,aux,log} $(UPLOADED_FILES)

distclean: clean
	rm -f report.pdf

.PHONY: all clean distclean
