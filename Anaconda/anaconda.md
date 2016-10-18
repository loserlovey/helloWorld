---
title: Anaconda
tags: Anaconda Install Enviroment Clone
---

## Install Anaconda

[Download](https://www.continuum.io/downloads)

Install Anaconda3-4.2.0-Windows-x86_64

## Managing conda
conda update conda

conda --version

conda info

conda env list

conda info --envs

## Clone a new enviroment

conda create --name python3.5 --clone root

## Create a new enviroment with minimal required packages for scrapy

conda create --name python2.7 python=2.7 Twisted lxml pyOpenSSL 

## Activate enviroment

activate python2.7

## Deactivate current enviroment

deactivate 

## Delete enviroment

conda remove --name python3.5 --all

## Save current enviroment to a file

conda env export > e.yml

## Load enviroment from a file

conda env create -f e.yml

## Managing packages

conda list

conda list --name python2.7

conda remove --name python2.7 lxml

