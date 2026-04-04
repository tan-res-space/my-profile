# Makefile for building multiple CV versions
# Usage:
#   make all        - Build all versions
#   make detailed   - Build full detailed CV (default)
#   make industry   - Build industry-focused CV
#   make brief      - Build brief/short CV
#   make noresearch - Build detailed CV without research/training
#   make clean      - Remove build artifacts

# Auto-detect MacTeX path on macOS
TEXBIN := $(wildcard /Library/TeX/texbin)
ifneq ($(TEXBIN),)
  export PATH := $(TEXBIN):$(PATH)
endif

LATEX = pdflatex
BIBER = biber

# Default target
all: detailed industry brief noresearch

detailed: cv_detailed.pdf
industry: cv_industry.pdf
brief: cv_brief.pdf
noresearch: cv_noresearch.pdf

# Full detailed CV (original)
cv_detailed.pdf: cv_detailed.tex structure.tex publications.bib
	$(LATEX) cv_detailed.tex
	$(BIBER) cv_detailed
	$(LATEX) cv_detailed.tex
	$(LATEX) cv_detailed.tex

# Industry version
cv_industry.pdf: cv_industry.tex cv_detailed.tex structure.tex publications.bib
	$(LATEX) cv_industry.tex
	$(BIBER) cv_industry
	$(LATEX) cv_industry.tex
	$(LATEX) cv_industry.tex

# Brief version
cv_brief.pdf: cv_brief.tex cv_detailed.tex structure.tex publications.bib
	$(LATEX) cv_brief.tex
	$(BIBER) cv_brief
	$(LATEX) cv_brief.tex
	$(LATEX) cv_brief.tex

# Detailed without research/training
cv_noresearch.pdf: cv_noresearch.tex cv_detailed.tex structure.tex publications.bib
	$(LATEX) cv_noresearch.tex
	$(BIBER) cv_noresearch
	$(LATEX) cv_noresearch.tex
	$(LATEX) cv_noresearch.tex

clean:
	rm -f *.aux *.bbl *.bcf *.blg *.log *.out *.run.xml *.toc
	rm -f cv_industry.pdf cv_brief.pdf cv_noresearch.pdf

cleanall: clean
	rm -f cv_detailed.pdf

.PHONY: all detailed industry brief noresearch clean cleanall
