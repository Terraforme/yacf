TEXFILES = $(wildcard *.tex)
PDFFILES = $(TEXFILES:%.tex=target/%.pdf)

all: target $(PDFFILES) 
	mv -f *.pdf target/
	rm -f *.aux *.log *.pdf
	
target/%.pdf: %.tex
	pdflatex $^
	pdflatex $^

new:
	cp template.txt new.tex
	
target:
	mkdir target
	
clean:
	rm -f target/*
