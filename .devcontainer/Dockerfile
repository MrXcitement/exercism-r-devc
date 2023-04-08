## Build on the 'GO' base image including the exercism cli and
## the R programming environment.
## Note: on local arm64/Apple Silicon do not use -buster variants
## https://github.com/devcontainers/images/tree/main/src/go
FROM mcr.microsoft.com/devcontainers/go

## Install the exercism client
RUN go install -x github.com/exercism/cli/exercism@latest

## Update system and install R and package requirements
RUN apt-get update \
    && apt-get -y upgrade \
    && DEBIAN_FRONTEND=noninteractive apt-get -y install --no-install-recommends \
        libfontconfig1-dev \
        libfreetype6-dev \
        libfribidi-dev \
        libgit2-dev \
        libharfbuzz-dev \
        libjpeg-dev \
        libpng-dev \
        libtiff5-dev \
        libxml2-dev \
        r-base \
        r-base-dev \
    && apt-get autoremove -y \
    && apt-get clean -y \
    && rm -rf /var/lib/apt/lists/*

## Install packages into R
RUN /usr/bin/R --silent --slave --no-save --no-restore \
    -e "install.packages(c('devtools', 'httpgd', 'languageserver', 'testthat')); \
        devtools::install_github('ManuelHentschel/vscDebugger')"
