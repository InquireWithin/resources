# RESOURCES

### This is a repo for typically text-based files usually utilized by one of my scripts, or here for future use.


Files w/ "CRLF" in the name should be used for Windows, whereas "LF"-named files should be used for \*nix.

To convert files with "^M","0x13","0D","\x13" or "\r", which are carriage returns and are used in DOS to LF format for \*nix, run:


\*nix:
`sed -e "s/\r//g" originalfile > newfile`

dos/\*nix (perl needed):
`perl -p -e 's/\r//g' originalfile > newfile`

To change files from LF to CRLF:

for windows:

Personally I just open notepad++ on the file and go towards the bottom right where it will say 'Unix (LF)', change it to Windows (CRLF)

shell:

sed -i 's/$/\r/' filenamehere


