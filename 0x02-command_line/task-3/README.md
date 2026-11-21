# Task 3 - Finding Files & Searching File Contents

## Purpose of find
find locates files and directories by name, type or location,
for example: find practice/search-lab -type f -name "*.txt"

## Purpose of grep
grep searches inside files for a word or pattern and prints the matching lines.
Options used: -n shows line numbers, -i ignores uppercase/lowercase, -R searches recursively.

## Finding a filename vs searching inside a file
find looks at file names, types and locations. grep looks at the text inside the files.
find tells me where a file is, and grep tells me which lines contain a word.

## Combined find and grep command
find practice/search-lab -type f -name "*.txt" -exec grep -Hni "JavaScript" {} +
find selects all .txt files, then -exec runs grep on them. -H prints the file name,
-n the line number and -i ignores case, so I see the matching file and line.
