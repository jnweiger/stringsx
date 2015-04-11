# stringsx

A simplified strings tool, similar to the tool that
comes with gnu binutils, but with the following differences

* no -e switch. We support all encodings simultaneously

* '\0' characters are stripped, and have no effect, unless
  multiple '\0' charachters occur in a row.

* adjustable fuzzyness: 3 chars in a row with their 8th bit
  set are accepted, control chars except '\t', '\n', '\r'
  always cut a string.

* Strings need not be '\0' terminated.

* no support for file sections. We always scan the entire file.

Implemented in both perl and C. Compile the C version, if you
find significant speed issues with the perl version.

