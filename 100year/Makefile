SHELL=/bin/bash

all: tide.pdf

tide.pdf: tide.ps
	ps2pdf -dDEVICEHEIGHTPOINTS=1008 -dDEVICEWIDTHPOINTS=1823 tide.ps

tide.ps: plot Seattle_100yr_tide.csv.gz ekg
	for i in {0..99}; do zcat Seattle_100yr_tide.csv.gz | ./plot $$(( $$i * 140 )); done > tide.ps
