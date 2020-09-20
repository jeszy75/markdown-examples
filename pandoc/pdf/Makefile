sources = $(wildcard *.md)
targets = $(sources:.md=.pdf)

PANDOC = pandoc
PANDOC_FLAGS = -t latex --pdf-engine=xelatex

.PHONY: all
all: $(targets)

%.pdf: %.md
	$(PANDOC) $< -o $@ $(PANDOC_FLAGS)

.PHONY: clean
clean:
	rm -f $(targets)

