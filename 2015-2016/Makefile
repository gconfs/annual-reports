#! /usr/bin/env make

PROJECT		= report-s1-2015-2016
TEAM		= gconfs
SOURCES		= report.md
OUTPUT		= ${PROJECT}_${TEAM}
FONTSIZE	= 12pt
HTEMPLATE	= ./headertemplate.md
TEMPLATE	= ./template
PANDOCOPTS	= -s -S \
		  --variable fontsize=${FONTSIZE}

all:: pdf

pdf::
	pandoc header.md ${HTEMPLATE} ${SOURCES} ${PANDOCOPTS} \
	  --latex-engine=xelatex \
	  --listings \
	  --template=${TEMPLATE}.tex \
	  -o ${OUTPUT}.pdf

tex::
	pandoc src/header.md ${HTEMPLATE} ${SOURCES} ${PANDOCOPTS} \
	  --latex-engine=xelatex \
	  --listings \
	  --template=${TEMPLATE}.tex \
	  -o ${OUTPUT}.tex

clean::
	rm -f ${OUTPUT}.*
