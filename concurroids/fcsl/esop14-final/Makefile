all: paper

paper: paper.pdf

paper.pdf: paper.tex defs.tex abstract.tex intro4.tex overview3.tex related.tex conclusion.tex semantics2.tex model.tex soundness.tex fig-sem.tex actionsx.tex fig-sem.tex ticketed.tex references.bib proceedings-short.bib llncs.cls mathpartir.sty code.sty
	(pdflatex paper; bibtex paper -min-crossrefs=5; pdflatex paper; pdflatex paper)

# Delete everything that can be re-made
CLEAN=*.aux *.log *.blg *.bbl *.out paper.pdf *.dvi _region_.* concurroids-esop14.zip

clean:
	rm -f $(CLEAN)

zip: 
	zip concurroids-esop14.zip paper.tex defs.tex abstract.tex intro4.tex overview3.tex related.tex conclusion.tex semantics2.tex model.tex soundness.tex fig-sem.tex actionsx.tex fig-sem.tex ticketed.tex references.bib proceedings-short.bib llncs.cls mathpartir.sty code.sty Makefile



