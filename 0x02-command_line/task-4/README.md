# Task 4 - Automated Website Project Generator

## What the script does
create_website.sh creates a basic website project with index.html, css/style.css,
js/script.js, an images folder, and README.md files in every folder.

## How to run it
./task-4/create_website.sh

## Default output location
~/radius-projects/website-project/

## Custom output location
Give the path as the first argument:
./task-4/create_website.sh "$HOME/radius-projects/custom website"
The path is quoted so folder names with spaces work.

## How existing directories are protected
Before creating anything, the script checks if the destination exists using
[ -e "$DEST" ]. If it exists, the script prints an error message and stops with
exit 1, so nothing is overwritten, changed or deleted.
