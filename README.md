# Compiling A LaTeX Document Locally
These instructions will assist in creating a PDF document from a `.tex` LaTeX source code file. 

## Preliminaries
**This document assumes some basic proficiency in using the computers command line interface.** It also assumes a previous (and proper) local installation of a LaTeX distribution. Suggested LaTeX distributions are [TeXLive](http://www.tug.org/texlive/), [MikTeX](https://miktex.org/), and [MacTeX](http://www.tug.org/mactex/). For other distributions of LaTeX, these instructions may need to be slightly modified: namely the name of the suggested LaTeX PDF-Generating Tool.  

## Identifying Your LaTeX PDF-Generating Tool
When you installed your LaTeX distribution, it likely came with numerous tools that were added to your system. Many of these tools were added for LaTeX to function properly, and many of these tools were added for the user to interact with LaTeX in various ways. Among these installed tools will likely be `pdflatex` and `xelatex`, 2 common tools used to generate PDFs with LaTeX. 

In your command prompt, you can verify if these tools exist on your system by running `pdflatex --help` and `xelatex --help`. 

```bash
$ pdflatex
Usage: pdftex [OPTION]... [TEXNAME[.tex]] [COMMANDS]
   or: pdftex [OPTION]... \FIRST-LINE
   or: pdftex [OPTION]... &FMT ARGS
  Run pdfTeX on TEXNAME, usually creating TEXNAME.pdf.
  Any remaining COMMANDS are processed as pdfTeX input, after TEXNAME is read.
...
$ xelatex
Usage: xetex [OPTION]... [TEXNAME[.tex]] [COMMANDS]
   or: xetex [OPTION]... \FIRST-LINE
   or: xetex [OPTION]... &FMT ARGS
  Run XeTeX on TEXNAME, usually creating TEXNAME.pdf.
  Any remaining COMMANDS are processed as XeTeX input, after TEXNAME is read.
...
```

If your system was unable to find either of these commands, take a pause to check two things. 

1.  Identify if alternative PDF LaTeX tools exist with your installed distribution of LaTeX, and proceed with that alternative command.
    *   A simple google search for "***your latex distribution here*** pdf latex tools" 
2.  If your distribution of LaTeX was properly installed. 
    *   Check to see if your LaTeX distribution was properly installed to your system path. 
    *   Reinstalling the LaTeX system may be recommended.  
