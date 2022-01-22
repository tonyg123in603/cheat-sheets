# sed Cheat-Sheet
**sed** or stream-editor is a Unix utility that parses and transforms text, using a simple, compact programming language. 

## Basic Use

The following example shows a typical, and the most common, use of sed: substitution. This usage was indeed the original motivation for sed:

`sed 's/regexp/replacement/g' inputFileName > outputFileName`

### Regular Expressions (RegEx)
- The caret (^) matches the beginning of the line.
- The dollar sign ($) matches the end of the line.
- The asterisk (*) matches zero or more occurrences of the previous character.
- The plus (+) matches one or more occurrence(s) of the previous character.
- The question mark (?) matches zero or one occurrence of the previous character.
- The dot (.) matches exactly one character.

### Quiet

To suppress automatic printing of pattern space use **sed -n**.

*Example:* `sed -n /xyz/p`

### In-Place editing

To edit file use the **sed -i FILE** option this safely changes the file contents without any output redirection needed.

*Example:* `sed -i 's/xyz/XYZ/' file.txt`

### Advanced RegEx

To use extended regular expressions use the **sed -E** option in the script.

*Example:* `sed -E `

## Basic Patterns

PATTERN | DESCRIPTION
---|---
`/xyz/p` | Print all with xyz
`/xyz/!p` | Print all without xyz
`/xyz/d` | Delete all with xyz
`/xyz/!d` | Delete all without xyz

