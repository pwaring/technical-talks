% Building Software and Documentation with GNU Make
% Paul Waring (paul@xk7.net)
% February 25, 2017

# What is GNU Make?

 - Tool for automating building software, documentation etc.
 - Other tools with similar names, e.g. pmake, nmake

# What does Make do?

 - Builds things based on whether they are 'out of date'.
 - Outdated is calculated based on file timestamps.
 - Configured using a `Makefile`.

# Makefile components

 - Makefiles are a list of targets ('what to build').
 - Targets have rules ('how to build').
 - Targets have dependencies ('what to build first').
 - Some dependencies are targets in their own right.
 - Not all targets are dependencies.
 - Not all dependencies are built by Make.

# Make without a Makefile

 - Make has some implicit rules.
 - Compiling C source files to object files.
 - Linking object files to an executable.
 - `cd examples/no-makefile`
 - `make hello.o`
 - `make hello`

# Simple C compiling example

```makefile
#include "examples/hello-c/Makefile"
```

# Example: slides

 - Main target is `slides.html`.
 - Dependency of `slides.html` is `slides.md` which must be built/exist first.
 - `slides.md` is not a target, so not built by Make.
 - If (and only if) `slides.md` changes, we want to rebuild `slides.html`.

# Make will build a target when...

 - The target does not exist.
 - The target is older than any of its dependencies (last modified time).

# Make will not build a target when...

 - The rules used to generate the target have changed.
 - A configuration variable is set which affects the rules.

# Make variables

 - User-defined variables
 - Where they can be set
 - Provide value if not already set
 - Common values, e.g. `CFLAGS`

# Phony targets and clean

 - Common to have a `clean` target which removes intermediate files.
 - `clean` can also be used to force a full rebuild.
 - `.PHONY`: Stops Make being confused by file with same name as target.

# Special variables

 - `$@`: Full target filename (i.e. what will be built).
 - `$*`: Target filename without the suffix, e.g. `hello.o` becomes `hello`.
 - `$<`: The file which triggered this rule.

# Debugging

 - `-n`: Show commands which would be run.

# Parallel builds

 - `-j [number]`
 - `--output-sync` does what it says (>= 4.0)
 - May cause problems with dependencies built out of order
 - Requires Makefiles to be written with this in mind
 - Linux kernel is an example

# Autoconf and Automake

 - Insert notes here.

# Gotchas

 - Indent with tabs not spaces (watch out for editors).
 - Changing header files does not always rebuild dependent targets.
 - Last modified behaviour means occasional unnecessary rebuilds.
 - GNU Make uses `/bin/sh` by default (override with `SHELL=`).
 - Changing `Makefile` does *not* cause targets to be rebuilt.

# Resources

 - [http://www.gnu.org/software/make/manual/](http://www.gnu.org/software/make/manual/)
 - The GNU Make Book by John Graham-Cumming (No Starch Press)
