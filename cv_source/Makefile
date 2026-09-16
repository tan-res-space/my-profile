# Makefile for building multiple CV versions from cv.yaml
# Usage:
#   make all        - Generate LaTeX from YAML and build all PDFs
#   make generate   - Render cv_*.tex from cv.yaml
#   make test       - Validate YAML profiles without compiling
#   make detailed   - Build full detailed CV
#   make industry   - Build industry-focused CV
#   make brief      - Build brief/short CV
#   make noresearch - Build detailed CV without research/training
#   make clean      - Remove build artifacts

PYTHON ?= python3

# Auto-detect MacTeX path on macOS
TEXBIN := $(wildcard /Library/TeX/texbin)
ifneq ($(TEXBIN),)
  export PATH := $(TEXBIN):$(PATH)
endif

LATEX = pdflatex
BIBER = biber

VERSIONS = detailed industry brief noresearch
PDFS = $(addsuffix .pdf,$(addprefix cv_,$(VERSIONS)))

# Default target: render from YAML, then compile every version.
all: generate
	$(MAKE) $(PDFS)

generate:
	$(PYTHON) render_cv.py

test:
	$(PYTHON) render_cv.py --self-test

detailed: generate
	$(MAKE) cv_detailed.pdf
industry: generate
	$(MAKE) cv_industry.pdf
brief: generate
	$(MAKE) cv_brief.pdf
noresearch: generate
	$(MAKE) cv_noresearch.pdf

cv_%.pdf: cv_%.tex structure.tex publications.bib
	$(LATEX) cv_$*.tex
	$(BIBER) cv_$*
	$(LATEX) cv_$*.tex
	$(LATEX) cv_$*.tex

clean:
	rm -f *.aux *.bbl *.bcf *.blg *.log *.out *.run.xml *.toc
	rm -f $(PDFS)

cleanall: clean
	rm -f $(addsuffix .tex,$(addprefix cv_,$(VERSIONS)))

.PHONY: all generate test detailed industry brief noresearch clean cleanall
