all: slides.pdf slides.html

slides.pdf: slides.md
	gpp slides.md | pandoc -t beamer -o slides.pdf

slides.html: slides.md
	gpp slides.md | pandoc -t s5 -V s5-url=../s5/default -s -o slides.html

clean:
	rm -f *.html *.pdf

.PHONY: clean
