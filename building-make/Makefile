PDF_FILES = slides-screen.pdf slides-print.pdf
PANDOC_FLAGS = -t beamer
PANDOC_SCREEN_FLAGS = $(PANDOC_FLAGS) -i
PANDOC_PRINT_FLAGS = $(PANDOC_FLAGS)

all: $(PDF_FILES)

slides-screen.pdf: slides.md
	pandoc $(PANDOC_SCREEN_FLAGS) $< -o $@

slides-print.pdf: slides.md
	pandoc $(PANDOC_PRINT_FLAGS) $< -o $@

clean:
	rm -f $(PDF_FILES)

.PHONY: clean
