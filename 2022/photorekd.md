Fill up your disk like bleachbit, but instead of
using zeroes, actually fill the disk with file
headers.

So someone running `photorec` or forensic recovery
software gets a full disk.

Bonus points catalogue:

 * zip/rar/7z bombs
 * deleted dirs that have cyclical references
 * real images that suck
   * valid data but too large to view
   * nested, overlapping files that are actually valid images
   * PNG files with RLE abuse to exhaust memory
 * postscript data with recursion and infinite loops
 * stick to utf8 where possible to fuck with string parsers
 * file metadata sections that opens strings that never end
 * use tricks from fuzzers to exhaust memory 
 * randomly generated so impossible to detect by signature alone
