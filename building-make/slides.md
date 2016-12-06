% Building Software and Documentation with Make
% Paul Waring (paul@xk7.net)
% February 18, 2017

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
