all: slides.html

slides.html: slides.md Makefile
	filepp slides.md | pandoc -t s5 -V s5-url=../s5/default -s -o slides.html

clean:
	rm -f *.html

.PHONY: clean
