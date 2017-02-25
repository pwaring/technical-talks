% Building Software and Documentation with GNU Make
% Paul Waring (paul@xk7.net)
% February 25, 2017

# What is GNU Make?

 - Tool for automating building software, documentation etc.
 - Other tools with similar names, e.g. pmake (BSD), nmake (Microsoft).
 - GNU Make sometimes shortened to gmake.
 - This talk is GNU Make specific, though a lot applies to other Makes.

# What does Make do?

 - Builds things based on whether they are 'out of date'.
 - Outdated is calculated based on file last modified timestamps.
 - `make` followed immediately by `make` -> no build.
 - Configured using a `Makefile`.

# Makefile components

 - Makefiles are a list of targets ('what to build').
 - Targets have rules ('how to build').
 - Targets have dependencies ('what to build first').
 - Some dependencies are targets in their own right.

# Makefile components

 - Not all targets are dependencies.
 - Not all dependencies are built by Make.
 - End result: directed graph.

# Make will build a target when...

 - The target does not exist.
 - The target is older than any of its dependencies (last modified time).

# Make will not build a target when...

 - The rules used to generate the target have changed.
 - A configuration variable is set which affects the rules.

# Make without a Makefile

 - Make has some implicit rules.
 - Compiling C source files to object files.
 - Linking object files to an executable.
 - `cd examples/no-makefile`
 - `make hello.o`
 - `make hello`

# Example: slides

 - Main target is `slides.html`.
 - Dependency of `slides.html` is `slides.md` which must be built/exist first.
 - `slides.md` is not a target, so not built by Make.
 - If `slides.html` does not exist, build it.
 - If (and only if) `slides.md` is newer than `slides.html`, rebuild `slides.html`.

# Slides Makefile

```makefile
#include "Makefile"
```

# Phony targets and clean

 - Common to have a `clean` target which removes intermediate files.
 - `clean` can also be used to force a full rebuild.
 - `.PHONY`: Stops Make being confused by file with same name as target.

# Make variables

 - Set: `VAR = VALUE`.
 - Set conditionally: `VAR ?= VALUE`.
 - Set environment: `make VAR=VALUE`.
 - Access: `$(VAR)`.

# Make variables

 - Built-in variables, e.g. `SHELL`.
 - Common variables, e.g. `CFLAGS`.

# Special variables

 - `$@`: Full target filename (i.e. what will be built).
 - `$*`: Target filename without the suffix, e.g. `hello.o` becomes `hello`.
 - `$<`: The file which triggered this rule.

# C example with explicit rules

```makefile
#include "examples/hello-c/Makefile"
```

# Example: Configuration management workshop

 - Two main targets: book and workshop notes.
 - Two outputs for notes: print and screen.
 - Files common to both book and notes.
 - [Configuration Management with Ansible](https://github.com/pwaring/configuration-management-ansible)

# Debugging

 - `-n`: Show commands which would be run.
 - Caution: Rules which generate side-effects.

# Parallel builds

 - `-j [number]`.
 - `--output-sync` does what it says (>= 4.0).
 - May cause problems with dependencies built out of order.
 - Requires Makefiles to be written with this in mind.
 - Example: Linux kernel.

# Recursive Make

 - Make can call itself recursively.
 - `cd src && $(MAKE) $@`.
 - Like parallel Make, use with caution.

# Autotools

 - Autoconf, Automake and Libtool.
 - Works on Linux (good), macOS (usually), Windows (good luck!).
 - End-user requires `make` and a POSIX shell (usually `bash`).
 - `./configure && make && sudo make install`.

# Automake

 - `Makefile.am` -> `Makefile.in`.
 - `./configure` turns `Makefile.in` into a platform-specific `Makefile` (via `config.status`).
 - Automake is a talk in itself.

# Gotchas

 - Indent with tabs not spaces (watch out for editors).
 - Changing C/C++ header files does not always rebuild dependent targets.
 - Last modified behaviour means occasional unnecessary rebuilds.
 - GNU Make uses `/bin/sh` by default (override with `SHELL=`).
 - Changing `Makefile` does *not* cause targets to be rebuilt.
 - Some variables are pre-set and `?=` can have unintended behaviour.

# Resources

 - [GNU Make manual](http://www.gnu.org/software/make/manual/).
 - [GNU Make vs nmake](http://nmake.alcatel-lucent.com/faq/gmake.html).
 - The GNU Make Book by John Graham-Cumming (No Starch Press).
 - Autotools by John Calcote (No Starch Press).
