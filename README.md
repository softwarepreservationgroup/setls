# setls

SETL-S by Nigel P. Chapman, with contributions by Julius J. VandeKopple.

Nigel P. Chapman created SETL-S at the University of Leeds, completing version 1.9 in 1980. Later, Julius J. "Jay" VandeKopple, working at New York University, adapted it for MS-DOS, and distributed versions through 2.2 in 1991. Chapman's Ph.D. thesis uses SETL-S as an example of the techniques it describes:

* Nigel P. Chapman. Theory and practice in the construction of efficient interpreters. University of Leeds, 1980.

This project includes the main source file for SETL-S, which is written in MINIMAL, and also includes the files distributed for version 2.2 on October 6, 1991.

The source code is distributed under the GNU Public License Version 3.0 -- see the file [LICENSE](LICENSE).

## Documents

* [J. VandeKopple.] README. [text](DISTR/README)
* [J. VandeKopple.] Quick Start Information for SETLS. Undated. [text](DISTR/START.DOC)
* J. VandeKopple. SETLS v2.2 Installation Documentation. [text](DISTR/INSTALL.DOC)
* J. VandeKopple. SETLS Users Guide: A Short Introduction to the SETLS Compiler. For SETLS v2.2. New York University, October 6, 1991. [text](DISTR/SETLS.DOC)
* [J. VandeKopple.] SETLS V2.1 Grammar. [text](DISTR/SETLSGRM.DOC)

## Source

* Nigel Chapman and J. VandeKopple. SETL-S Version 2.3, New York University and The University of Leeds, 1992. [SETLSN.MIN](src/SETLSN.MIN).

## SETLS Example Programs

* [EULER.STL](DISTR/EULER.STL)
* [EULER2.STL](DISTR/EULER2.STL)
* [FACT.STL](DISTR/FACT.STL)
* [PRIME1.STL](DISTR/PRIME1.STL)
* [PRIME2.STL](DISTR/PRIME2.STL)
* [TOPSORT1.STL](DISTR/TOPSORT1.STL)
* [TOPSORT2.STL](DISTR/TOPSORT2.STL)

There is also a copy of DVED, the Dewar Visual Editor, by Robert B. K. Dewar with these files: [DVED.COM](DISTR/DVED.COM), [DVED.DOC](DISTR/DVED.DOC), and [DVEDUSR.DOC](DISTR/DVEDUSR.DOC).

## Running SETLS

The files in DISTR will run on a real or emulated PC-compatible running MS-DOS. Alternatively, it can be run in a browser. Visit [https://virtualconsoles.com/online-emulators/dos/](https://virtualconsoles.com/online-emulators/dos/) and drag [DISTR-ZIP.zip](RAW/DISTR.zip) to the blue area on the web page, then press the blue Start button at the bottom. You’ll soon have a C:\> prompt; type “cd distr” to enter the directory, then type “setls fact” to run the factorial example, followed by two carriage returns to accept the default filenames for listing and executable. DVED is available in this same directory if you want to write a new program.

## Implementation

The MINIMAL language was originally designed to implement Macro Spitbol. MINIMAL in turn is implemented by a Spitbol program that translates MINIMAL to the assembly language of the target machine; then an assembler such as [NASM](https://www.nasm.us) is used to assemble the generated code, after which it is linked with an operating system interface library. To bootstrap Macro Spitbol, an existing Spitbol executable is required.

SETLS combines a translator and an interpreter in a single executable, so it bypasses the assembly step used by Macro Spitbol. See the comments in the [source code](src/SETLSN.MIN) for details.

See [https://github.com/spitbol](https://github.com/spitbol) for historical and modern versions of Macro Spitbol.

