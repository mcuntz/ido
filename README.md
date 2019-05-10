# ido
Collection of command line scripts.

All scripts have -h command line option displaying a help screen.

### Scripts

| | | |
| --- | --- | ------------------------------------------------------------------------------------------------------------- |
| | catfiles | Concatenate files with identical headers. Leaves header of first file and removes all subsequent headers. |
| | cleanlatexdiff | Clean internal LaTeX commands of latexdiff output to simple \add and \del commands. |
| | cutbyname | Wrapper of cut command where one specifies the fields by name in a header line. |
| | ido\_bash\_completion | source ido\_bash\_complete in .bash\_profile to get completion of command line options of all ido scripts with tab. |
| | iinvert | Invert colours or colour channel in image using ImageMagick. |
| | irename | Batch rename several files using an sed expression. |
| | ireplace | Applies sed expression on several files, e.g. replacing a string in the files. |
| | ireverse | Reverses the lines in a file leaving a header. |
| | itranspose | Transposes a file and writes it to standard out, optionally removing a header. |
| | izip | Wrapper for zip utility: if 'izip directory' then 'zip -r directory.zip directory' will be called. |
| | unix2mac | Converts unix, dos/windows and mac text file formats into each other. Other names: mac2unix, mac2win, unix2win, win2mac, win2unix |
| | psmerge | Merges several pdf or postscript files into one single pdf or postscript file. Other names: pdfmerge |
| | pssplit | Splits pdf or postscript file into files with individual pages using ghostscript. Other names: pdfsplit |

### Examples

| | |
| --- | --------------------------------------------------------- |
| | % catfiles -n 1 -o out infile* |
| | % latexdiff --flatten old.tex new.tex \| cleanlatexdiff > diff.tex |
| | % sed 's/2002/2003/' infile \| cutbyname -f 'date,co2' -d ',' \| tr ',' ' ' > outfile |
| | % iinvert -s LCH -c C -d 600 -o image.png image.pdf |
| | % irename -f 's/DSC\_/Photo/' \*.jpg |
| | % ireplace '/exp/s/exp=.\*/exp=moc01/' moc.\* |
| | % ireverse -s 1 infile > outfile |
| | % itranspose -s 1 -d ',' -c infile > outfile |
| | % izip mydir |
| | % win2unix -q \*.txt |
| | % pdfmerge -o all.pdf \*.pdf \*.ps |
| | % pdfsplit in.pdf pages\_ |

**Copyright (c) 2012-2019 Matthias Cuntz - mc (at) macu (dot) de**
