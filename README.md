## CharCount utility

**CharCount** is a Windows utility to read text or binary files to produce frequency counts of all characters in the file.

This summary often shows unexpected characters in files, especially in very large files.

The summary shows the counts for each hex character x'00' through x'FF' in the file, but suppresses rows or columns that are zero.  Pure ASCII text files should contain only characters x'00' through x'7E'.

The **CharCount** result for a binary file will often show the full 16-by-16 matrix.

Example 1
---------
An ASCII text file with the letters "ABC" also has a line-feed (x'0A') and carriage return (x'0D') at the end of each line.

If created in Linux, the file only has a line-feed (x'0A') at the end of the line.

Press the *Control Codes* button to see a description of most values under x'20'.

To process a file, press the *Select File* button and select the file, or using Windows Explorer, simply drag and drop the file onto the middle of the window.

![Example 1](Screens/CharCount-ABC-text.png)

Example 2
---------
An ASCII text file with a DNA sequence in FASTA format might look like this, with many characters appearing in the file.  The file has 213 lines and was likely created in a Windows environment since the number of x'0A' and x'0D' characters are the same.

![Example 2](Screens/CharCount-FASTA-raw.png)


Example 3
---------
The FASTA file in Example 2 consists of a "Defline" as the first line, followed by 212 rows of DNA sequences that consist of only As, Cs, Gs and Ts.  To ignore the defline and only count the sequence nucleotides, check the *Assume FASTA File* box before processing the file.

![Example 3](Screens/CharCount-FASTA-Sequence.png)


Delphi Source Code
------------------
The repository has complete Delphi source code, which was compiled using Delphi XE3.  The compiled executable, **CharCount.exe**, requires no special installation and can be run from any directory.


Comment
-------

Run **CharCount** with a binary file (like an .exe, .jpg, or .png) to see almost all possible characters, x'00' through x'FF', in a file.

