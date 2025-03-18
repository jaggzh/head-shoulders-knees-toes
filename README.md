# `head-shoulders-knees-toes` (aka `htt` (head torso toes)

## Overview
`head-shoulders-knees-toes` (symlinked as `htt`) is a Perl script designed to preview a file's contents by displaying four evenly spaced chunks from the file in a terminal window. It properly accounts for terminal height, even when receiving piped input.

## Screenshot(s)
![Example previewing a python script](i/screenshot1.png)

## Features
- Done in perl because it has a very fast load and runtime [compared to python at least]
- Detects terminal height to determine optimal chunk sizes.
- Works with piped input or files.
- Displays four evenly spaced sections from the file.
- Preserves space for dividers and prompt return.

## Future features (if ever)
- Syntax highlighting
- Auto-reduction of count of lines of imports/use/include lines in head
- Make tons of money off this to support my family (translate to all languages: "this was said tongue-in-cheek"; ie. it was a joke.)

## Usage
```sh
cat largefile.txt | htt
htt < largefile.txt
htt largefile.txt
```

## Installation
1. Place `head-shoulders-knees-toes` in a directory in your `$PATH`.
2. Create a symlink:
```sh
ln -s head-shoulders-knees-toes htt
```
3. Make it executable:
```sh
chmod +x head-shoulders-knees-toes
```

## Output
```sh
{chunk0 from top of file}
..
{chunk1 from later}
..
{chunk2 from later}
..
{chunk3 from very end}
```

## Notes
- This script respects terminal height and ensures content fits within the visible area.
- Ideal for quickly previewing large files.


