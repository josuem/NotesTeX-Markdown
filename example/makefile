REFERENCE :=  --citeproc --bibliography ./biblio.bib --csl ./ieee-with-url.csl
TEMPLATE := ../template/template_notestex.tex
FILTER := -F ../filter/pandoc-crossref

all: 
	pandoc notestex_ex.md $(FILTER) $(REFERENCE) --template $(TEMPLATE) -o ./notestex_ex.pdf

