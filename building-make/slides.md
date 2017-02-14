% Building Software and Documentation with GNU Make
% Paul Waring (paul@xk7.net)
% February 25, 2017

# What is GNU Make?

 - Tool for automating building software, documentation etc.
 - Other tools with similar names, e.g. pmake, nmake

# Make without a Makefile

 - Make has some built-in rules.
 - Compiling C source files to object files.
 - Linking object files to an executable.
 - `cd examples/no-makefile`
 - `make hello.o`
 - `make hello`

# Makefile components

 - Makefiles are a list of targets ('what to build').
 - Targets have rules ('how to build').
 - Targets have dependencies ('what to build first').
 - Some dependencies are targets in their own right.
 - Not all targets are dependencies.

# Example: slides

 - Main target is `slides.html`.
 - Dependency of `slides.html` is `slides.md` which must be built/exist first.
 - `slides.md` is not a target, so not built by Make.
 - If (and only if) `slides.md` changes, we want to rebuild `slides.html`.

```
target: dependencies
  rules
```

# Make will build a target when...

 - The target does not exist.
 - The target is older than any of its dependencies (last modified time).

# Make will not build a target when...

 - The rules used to generate the target have changed.

# Special variables

 - `$@`: Full target filename (i.e. what will be built).
 - `$*`: Target filename without the suffix, e.g. `hello.o` becomes `hello`.
 - `$<`: The file which triggered this rule.

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
