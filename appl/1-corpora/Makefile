.PHONY: all

TECTONIC = tectonic -X compile --pass tex --keep-intermediates

all:
	$(TECTONIC) src/index.tex
	biber src/index
	$(TECTONIC) src/index.tex
	$(TECTONIC) src/index.tex
	xdvipdfmx src/index.xdv
	mv index.pdf build/

debug:
	$(TECTONIC) src/index.tex --print
