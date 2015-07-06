# ocline
A simple line-based text reader and editor for the command line. Inspired by what I've heard GNU Ed is like. Except I've never used GNU Ed. I just know it doesn't act like this.

OCLine is a work in progress. Pull requests are encouraged, but won't necessarily be accepted. Keeping stuff under the MPL won't hurt your chances (a.k.a if you're going to PR, please keep stuff under the MPL).

# Usage

`ocline <file>` reads <file> line-by-line. (The user types return to display the next line).

`ocline <file> --write` reads <file> line-by-line in a similar way to `ocline <file>`, but the user's input is recorded, and if not blank, replaces the respective line of the file. To replace a line with a blank line, type `[BLANK]` in the prompt. Afterward, the user will have a chance to append any lines that they want to at the end of the file. To exit out of this, press Control-C. `ocline <file> --write` is experimental and does not work yet.

`ocline <file> --new` jumps right to the last part of the last example. It overwrites (or creates) <file>.

`ocline` takes the input from stdin and outputs it in the same manner as `ocline <file>` outputs <file>. Note that if you are typing manually into stdin, you will have to type Control-D when you are finished.
