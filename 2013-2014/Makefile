all:: report

report:: logo
	pdflatex report.tex 

logo::
	if ! [ -e 'logo_gconfs.png' ]; then \
			wget 'http://gconfs.fr/tmp/logo_gconfs.png'; \
	fi
