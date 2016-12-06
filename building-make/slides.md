% Building Software and Documentation with GNU Make
% Paul Waring (paul@xk7.net)
% February 18, 2017

# What is GNU Make?

 - Tool for automating building software, documentation etc.
 - Other tools with similar names, e.g. pmake, nmake

# Makefile components

 - Makefiles are a list of targets
 - Targets have dependencies
 - Dependencies have rules

```
target: dependencies
  rules
```

# Special variables

 - `$@`: Full target filename (i.e. what will be built).
 - `$*`: Target filename without the suffix, e.g. `hello.o` becomes `hello`.
 - `$<`: The file which triggered this rule.

# Gotchas

 - Indent with tabs not spaces (watch out for editors)
 - Changing header files does not always rebuild dependent targets
 - Last modified behaviour means occasional unnecessary rebuilds

# Resources

 - [http://www.gnu.org/software/make/manual/](http://www.gnu.org/software/make/manual/)
 - The GNU Make Book by John Graham-Cumming (No Starch Press)
