all: tide.pdf

tide.pdf: tide.ps
	ps2pdf -dDEVICEHEIGHTPOINTS=864 -dDEVICEWIDTHPOINTS=9600 tide.ps

tide.ps: plot Seattle_100yr_tide.csv.gz ekg
	zcat Seattle_100yr_tide.csv.gz | ./plot > tide.ps
