all: paper.pdf camera-ready.pdf

paper.pdf: paper.tex lstcoq.tex mathpartir.sty references.bib proceedings.bib sigplanconf.cls related.tex intro.tex overview.tex development.tex defs.tex underhood.tex conclusion.tex evaluation.tex more.tex dependencies.eps stages.eps

	pdflatex --jobname=fcsl-pldi15 paper
	bibtex fcsl-pldi15 -min-crossrefs=5 
	pdflatex --jobname=fcsl-pldi15 paper
	pdflatex --jobname=fcsl-pldi15 paper

paper.ps: paper.tex lstcoq.tex mathpartir.sty references.bib proceedings.bib sigplanconf.cls related.tex intro.tex overview.tex development.tex defs.tex underhood.tex conclusion.tex evaluation.tex more.tex dependencies.eps stages.eps

	latex "\def\psflag{}\input{paper}"
	bibtex paper -min-crossrefs=5
	latex "\def\psflag{}\input{paper}"
	latex "\def\psflag{}\input{paper}" && dvips -Ppdf paper && mv paper.ps fcsl-pldi15-cr.ps

camera-ready.pdf: paper.tex lstcoq.tex mathpartir.sty references.bib proceedings.bib sigplanconf.cls related.tex intro.tex overview.tex development.tex defs.tex underhood.tex conclusion.tex evaluation.tex more.tex dependencies.eps stages.eps

	pdflatex --jobname=fcsl-pldi15-cr "\def\crflag{}\input{paper}"
	bibtex fcsl-pldi15-cr -min-crossrefs=5 
	pdflatex --jobname=fcsl-pldi15-cr "\def\crflag{}\input{paper}"
	pdflatex --jobname=fcsl-pldi15-cr "\def\crflag{}\input{paper}"

quick:
	pdflatex 

clean:
	rm -f *~ *.aux *.log *.blg *.dvi *.bm *.vrb *.toc *.nav *.out *.snm *.lof *.lot *.zip *.rel *.ps *.bbl paper.pdf fcsl-pldi15-cr.ps fcsl-pldi15.pdf fcsl-pldi15-cr.pdf

zip:
	zip paper.zip paper.tex lstcoq.tex mathpartir.sty references.bib proceedings.bib sigplanconf.cls related.tex intro.tex overview.tex development.tex defs.tex underhood.tex conclusion.tex evaluation.tex more.tex dependencies.eps stages.eps stages-eps-converted-to.pdf Makefile aec-badge-pldi.pdf aec-badge-pldi.pdf dependencies-eps-converted-to.pdf bibmacros.bib sigplanconf1.cls


