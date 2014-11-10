SHELL=/bin/bash

all: tide.pdf

tide.pdf: tide.ps
	ps2pdf -dDEVICEHEIGHTPOINTS=1080 -dDEVICEWIDTHPOINTS=6984 tide.ps

tide.ps: plot Seattle_100yr_tide.csv.gz ekg
	for i in {0..27}; do zcat Seattle_100yr_tide.csv.gz | ./plot $$(( $$i * 475 )); done > tide.ps
