PDF_FILES = slides-screen.pdf slides-print.pdf
PANDOC_FLAGS = -t beamer
PANDOC_SCREEN_FLAGS = $(PANDOC_FLAGS) -i
PANDOC_PRINT_FLAGS = $(PANDOC_FLAGS)

all: $(PDF_FILES) slides-s5.html slides-reveal.html slides-dz.html

slides-screen.pdf: slides.md
	pandoc $(PANDOC_SCREEN_FLAGS) $< -o $@

slides-print.pdf: slides.md
	pandoc $(PANDOC_PRINT_FLAGS) $< -o $@

slides-s5.html: slides.md
	filepp $< | pandoc -t s5 -s -o $@

slides-reveal.html: slides.md
	filepp $< | pandoc -t revealjs -s -o $@

slides-dz.html: slides.md
	filepp $< | pandoc -t dzslides -s -o $@

clean:
	rm -f $(PDF_FILES) *.log *.html

.PHONY: clean
