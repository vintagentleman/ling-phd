.PHONY: all

all: tex biber tex tex xdvipdfmx

tex:
	tectonic -X compile --pass tex --keep-intermediates src/index.tex

biber:
	biber src/index

xdvipdfmx:
	xdvipdfmx src/index.xdv
	mv index.pdf build/
