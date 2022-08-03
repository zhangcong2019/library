explaining the makefile:

target: prerequisites - the rule head
$@ - means the target
$^ - means all prerequisites
$< - means just the first prerequisite
ar - a Linux tool to create, modify, and extract from archives see the man pages for further information. The options in this case mean:
r - replace files existing inside the archive
c - create a archive if not already existent
s - create an object-file index into the archive
