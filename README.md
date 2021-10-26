# Compiling A LaTeX Document To PDF
These instructions will assist in creating a PDF document from a `.tex` LaTeX source code file using the command line interface. Alternative graphical LaTeX compilers are available, and are not covered in this tutorial.

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

1.  Identify if alternative PDF LaTeX tools exist with your installed distribution of LaTeX
    *   A simple google search for "***your latex distribution here*** pdf latex tools" 
    *   Proceed with that alternative command in place of `xelatex` which will be used.
2.  If your distribution of LaTeX was properly installed. 
    *   Check to see if your LaTeX distribution was properly installed to your system path. 
    *   Reinstalling the LaTeX system may be recommended.  

## Compiling The Document
Now that an installed LaTeX PDF tool has been identified, we can proceed with compiling our actual main `.tex` file. First, locate your main `.tex` file locally on your system, and change directories to the location of that file. 

```
$ cd LaTeXProject
```

Now that you are located in your LaTeX project--where your main `.tex` file exists (which we will call `main.tex` for the sake of example)--you can compile the `main.tex` file with the command `xelatex main.tex`.  

```
$ xelatex main.tex
This is XeTeX, Version 3.141592653-2.6-0.999993 (TeX Live 2021/Arch Linux) (preloaded format=xelatex)
 restricted \write18 enabled.
entering extended mode
(./main.tex
LaTeX2e <2020-10-01> patch level 4
L3 programming layer <2021-02-18>
(/usr/share/texmf-dist/tex/latex/base/article.cls
Document Class: article 2020/04/10 v1.4m Standard LaTeX document class
(/usr/share/texmf-dist/tex/latex/base/size12.clo))
(/usr/share/texmf-dist/tex/latex/l3backend/l3backend-xetex.def
(|extractbb --version)) (./main.aux)
(/usr/share/texmf-dist/tex/latex/base/ts1cmr.fd) [1] (./main.aux) )
Output written on main.pdf (1 page).
Transcript written on main.log.
```

At this point, you can list the contents of the working directory and find the outputted PDF, corresponding to the filename of the provided `.tex` file. As the example uses a file called `main.tex`, the PDF generated above would be called `main.pdf`. You may also notice additional files corresponding to the file name after the compilation process. Files such as `main.aux` and `main.log`, which are auxiliary files and log files respectively. These files can be inspected for additional information on the results of the recently run compilation process, however they can typically be ignored. 

### Guided Instructions From Git Repository (Optional)
If you are following along with these instructions by cloning the provided git repository located at [https://github.com/jaxtonw/LaTeXCompilingInstructions](https://github.com/jaxtonw/LaTeXCompilingInstructions), this section will guide you in compiling the provided example LaTeX project. 

Assuming you have the cloned repository locally at the path `~/LaTeXCompilingInstructions` (modify path as needed), change directories into the provided `example` directory with a sample LaTeX project. 

```
$ cd ~/LaTeXCompilingInstructions/example
```

You can then list the contents of this directory to confirm it contain `main.tex`, the provided sample LaTeX file for you to compile. Once in the directory with this file, you can use your LaTeX PDF command of choice followed by the `main.tex` file name to generate the PDF located at `main.pdf`. 

```
$ xelatex main.tex
This is XeTeX, Version 3.141592653-2.6-0.999993 (TeX Live 2021/Arch Linux) (preloaded format=xelatex)
 restricted \write18 enabled.
entering extended mode
(./main.tex
LaTeX2e <2020-10-01> patch level 4
L3 programming layer <2021-02-18>
(/usr/share/texmf-dist/tex/latex/base/article.cls
Document Class: article 2020/04/10 v1.4m Standard LaTeX document class
(/usr/share/texmf-dist/tex/latex/base/size12.clo))
(/usr/share/texmf-dist/tex/latex/l3backend/l3backend-xetex.def
(|extractbb --version)) (./main.aux)
(/usr/share/texmf-dist/tex/latex/base/ts1cmr.fd) [1] (./main.aux) )
Output written on main.pdf (1 page).
Transcript written on main.log.
```

At this point, you can list the contents of the working directory and find the PDF `main.pdf`. You may also notice additional files such as `main.aux` and `main.log`, which are auxiliary files and log files respectively; generated during the compilation process. These files can be inspected for additional information on the results of the recently run compilation process, however they can typically be ignored. 
