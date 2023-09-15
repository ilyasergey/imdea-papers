all: paper.pdf

paper.pdf: paper.tex defs.tex background2.tex intro5.tex overview2.tex conclusion.tex examples2.tex flatcombine2.tex related.tex appendix.tex references.bib bibmacros.bib proceedings-short.bib fctrans.pdf llncs.cls *.sty Makefile
	pdflatex paper
	bibtex paper -min-crossrefs=5
	pdflatex paper
	pdflatex paper paper.pdf

quick: paper.tex defs.tex background2.tex intro5.tex overview2.tex conclusion.tex examples2.tex flatcombine2.tex related.tex appendix.tex references.bib bibmacros.bib proceedings-short.bib fctrans.pdf llncs.cls *.sty Makefile
	pdflatex paper

ext: paper.tex defs.tex background2.tex intro5.tex overview2.tex conclusion.tex examples2.tex flatcombine2.tex related.tex appendix.tex references.bib bibmacros.bib proceedings-short.bib fctrans.pdf llncs.cls *.sty Makefile
	pdflatex --jobname=paper-extended "\def\extflag{}\input{paper}"

clean: 
	rm -f {paper,paper-extended}.{out,dvi,ps,pdf,log} *.{toc,blg,bbl,aux,rel} paper *.log *~ paper.zip *.tar.gz

zip:
	zip paper.zip paper.tex defs.tex background2.tex intro5.tex overview2.tex conclusion.tex examples2.tex flatcombine2.tex related.tex appendix.tex references.bib bibmacros.bib proceedings-short.bib fctrans.pdf llncs.cls *.sty Makefile

tar:
	tar -zcvf paper-39.tar.gz paper.tex defs.tex background2.tex intro5.tex overview2.tex conclusion.tex examples2.tex flatcombine2.tex related.tex appendix.tex references.bib bibmacros.bib proceedings-short.bib fctrans.pdf llncs.cls *.sty Makefile copyright-esop15-scanned.pdf
