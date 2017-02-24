CC = clang
CFLAGS = -Weverything -Werror
SOURCES = hello.c
OBJECTS = $(subst .c,.o,$(SOURCES))
EXECUTABLE = hello

$(EXECUTABLE): $(OBJECTS)
	$(CC) $(OBJECTS) -o $(EXECUTABLE)

%.o: %.c
	$(CC) $(CFLAGS) -c $< -o $@

clean:
	-rm -f $(OBJECTS) $(EXECUTABLE)

.PHONY: clean
