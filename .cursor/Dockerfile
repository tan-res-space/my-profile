FROM ubuntu:24.04

ENV DEBIAN_FRONTEND=noninteractive

# System toolchain for the Jekyll site (Ruby) and the LaTeX CV build (TeX Live).
# These are slow, stable dependencies, so they live in the image rather than in `install`.
RUN apt-get update \
    && apt-get install -y --no-install-recommends \
        ca-certificates \
        curl \
        git \
        make \
        build-essential \
        zlib1g-dev \
        ruby-full \
        texlive-latex-recommended \
        texlive-latex-extra \
        texlive-fonts-recommended \
        texlive-fonts-extra \
        texlive-bibtex-extra \
        texlive-plain-generic \
        tex-gyre \
        biber \
        latexmk \
    && gem install bundler --no-document \
    && rm -rf /var/lib/apt/lists/*

# The base image ships an `ubuntu` user (uid 1000); use it for all agent work.
USER ubuntu
