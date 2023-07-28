.PHONY: clean clean_all default view

JOBNAME = peter_pan

default: out/${JOBNAME}.pdf

out/${JOBNAME}.pdf: master.tex chapter_??.tex
	latexmk -xelatex -auxdir=aux -outdir=out -jobname=${JOBNAME} master.tex

clean:
	latexmk -xelatex -auxdir=aux -outdir=out -jobname=${JOBNAME} -c master.tex

clean_all:
	latexmk -xelatex -auxdir=aux -outdir=out -jobname=${JOBNAME} -C master.tex

view:
    xdg-open out/${JOBNAME}.pdf