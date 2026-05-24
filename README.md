# Coffin problems

This project catalogues the so-called _Coffin problems_:
mathematical problems that in the 1960s, 1970s, and 1980s
were administered at the entrance examinations of some Soviet universities
for the purpose of preventing the enrolment of applicants who were deemed undesirable,
category which mainly included people of Jewish descent.
The problems were given at the oral exams to the 'undesirable' candidates.

This repository's goal is to exhaustively catalogue these problems, and to provide solutions.
Some problems also admit interesting generalisations, which are also catalogued.

For historical information on the topic, consult the [historical references](#additional-references).


## Download

> [!NOTE]
> Solutions have not yet been written for all problems.

Download in PDF format:
<h3 align="center">
  <a href="https://coffinproblems.github.io/coffins/coffins_problems_and_solutions.pdf" download>
    Download
  </a>
</h3>
<br>


Alternate download options are also available, for downloading separately the problem statements and the solutions.  
Other formats are also provided:
- **minimal PDF**: PDF file without introduction, table of contents, and references;
- **EPUB MathML**: reflowable ebook, with math content in MathML format;
- **EPUB SVG**: reflowable ebook, with math content rendered as SVG;
<!--
- **TeX source**: standalone `.tex` file.
-->

> [!NOTE]
> At the moment, EPUB files are problematic:
> - EPUB files with MathML are not provided, due to issues in generating them;
> - EPUB files with SVG are provided, but they exhibit some formatting issues.

|                        | PDF              | Minimal PDF      | EPUB MathML      | EPUB SVG         |
|:----------------------:|:----------------:|:----------------:|:----------------:|:----------------:|
| Problems               | [Download](https://coffinproblems.github.io/coffins/coffins_problems_no_solutions.pdf)  | [Download](https://coffinproblems.github.io/coffins/coffins_problems_no_solutions_minimal.pdf)        | \[Not available\] | [Download](https://coffinproblems.github.io/coffins/coffins_problems_no_solutions-svg.epub)  |
| Solutions              | [Download](https://coffinproblems.github.io/coffins/coffins_solutions.pdf)              | [Download](https://coffinproblems.github.io/coffins/coffins_solutions_minimal.pdf)                    | \[Not available\] | [Download](https://coffinproblems.github.io/coffins/coffins_solutions-svg.epub)              |
| Problems and solutions | [Download](https://coffinproblems.github.io/coffins/coffins_problems_and_solutions.pdf) | [Download](https://coffinproblems.github.io/coffins/coffins_problems_and_solutions_minimal.pdf)       | \[Not available\] | [Download](https://coffinproblems.github.io/coffins/coffins_problems_and_solutions-svg.epub) |

<br>

The same are also available for the **generalisations of the problems**:

|                        | PDF              | Minimal PDF       | EPUB MathML       | EPUB SVG         |
|:----------------------:|:----------------:|:-----------------:|:-----------------:|:----------------:|
| Problems               | [Download](https://coffinproblems.github.io/coffins/coffins_generalised_problems_no_solutions.pdf)  | [Download](https://coffinproblems.github.io/coffins/coffins_generalised_problems_no_solutions_minimal.pdf)  | \[Not available\] | [Download](https://coffinproblems.github.io/coffins/coffins_generalised_problems_no_solutions-svg.epub)  |
| Solutions              | [Download](https://coffinproblems.github.io/coffins/coffins_generalised_solutions.pdf)              | [Download](https://coffinproblems.github.io/coffins/coffins_generalised_solutions_minimal.pdf)              | \[Not available\] | [Download](https://coffinproblems.github.io/coffins/coffins_generalised_solutions-svg.epub)              |
| Problems and solutions | [Download](https://coffinproblems.github.io/coffins/coffins_generalised_problems_and_solutions.pdf) | [Download](https://coffinproblems.github.io/coffins/coffins_generalised_problems_and_solutions_minimal.pdf) | \[Not available\] | [Download](https://coffinproblems.github.io/coffins/coffins_generalised_problems_and_solutions-svg.epub) |


## Status

The current number of documented problems is: 111.

Currently, not all solutions have been written.

The problems have been categorised by topic, as follows:
- **Evaluations** (4 problems): problems that ask to determine the value of an expression;
- **Comparisons** (6 problems): problems that ask to determine which of two numbers is greater than the other;
- **Equations** (13 problems): problems that ask to solve an equation or system of equations over the real or complex numbers;
- **Inequations** (6 problems): problems that ask to solve an inequation;
- **Algebra and Number Theory** (13 problems): problems in Algebra or in Number Theory;
- **Analysis** (7 problems): problems in Analysis;
- **Plane Geometry** (27 problems): problems in planar Euclidean Geometry;
- **Solid Geometry** (21 problems): problems in 3D Geometry;
- **Geometric constructions** (12 problems): problems that ask to perform constructions via only straightedge and compass;
- **Other problems** (2 problems): problems that do not fit in any specific category.


## Contributing

More details are provided in [CONTRIBUTING.md](CONTRIBUTING.md).

> [!IMPORTANT]
> Please, when opening an issue or leaving a comment
> about a coffin problems, hide in an expandable block of text
> any information pertaining to the solution of the problem,
> so that people who wish to solve the problems independently don't get accidental hints.

A non-exhaustive list of welcomed contributions:
- Submit coffin problems that are not already documented here.
- Submit additional references, sources, or other resources that corroborate some of the already documented coffin problems.
- Submit additional historical references.
- Help digitising and/or translating the historical documents used as sources: see the dedicated repository [`resources`](https://github.com/coffinproblems/resources).
- Report errors, inaccuracies, etc.
- Suggest improvements in the wording throughout the document.
- Propose additional solutions to problems, or improvements to the existing ones.
- Suggest possible improvements to the LaTeX source code.
- Sift through the references to see if any of them contain any information that was missed.
- Sift through user discussions about relevant topics to see if there is any new information. See [here](CONTRIBUTING.md/#sift-through-sources) for details.
- Help to identify and contact people that might have useful information.

See [CONTRIBUTING.md](CONTRIBUTING.md) for more details.


## Building

### Requirements
A TeX distribution is needed.
Some features are not available in TeX distribution versions prior to 2024;
for compiling with those older versions, the branch [`alt`](https://github.com/coffinproblems/coffins/tree/alt) is provided (and the build instructions are the same).

<details><summary>More info</summary>
<p>

This project makes use of the LaTeX package [`l3sys-query`](https://ctan.org/pkg/l3sys-query)
for reading the first-level subdirectories inside `src/problems/` without requiring shell escape.  
In the branch `alt`, those subdirectories are renamed to only numbers to make them accessible with a standard `\loop` macro.

</p>
</details>


### Generate PDF

The following command, run from within the `src` directory, generates the "default" PDF file,
containing the original problems (with the statements in the first part of the document, and the solutions in the second part):
```shell
latexmk main.tex
```
The resulting file is placed in the `output` directory (outside of `src`),
and the intermediate auxiliary files are placed in the `build` directory (outside of `src`).

> [!NOTE]
> If the build process is carried out in a Docker container, the `output` directory should be mounted to the container in order to get access to the generated output files.
> Similarly, the `build` directory needs to be mounted in order to have access to the logs and the other auxiliary files.

#### TeX engines
Compilation is possible with the pdfLaTeX and LuaLaTeX compilation engines;
the engine used by default is LuaLaTeX.

To compile with pdfLaTeX, set the `-pdflatex` option when running `latexmk`:
```shell
latexmk -pdflatex main.tex
```
or change `$pdf_mode = 4` to `$pdf_mode = 1` in the `latexmkrc` file (located in the `src` directory).


### Generate ebook

> [!WARNING]
> ebook generation is currently not reliable.

> [!NOTE]
> The following instructions utilize the [`tex4ebook`](https://github.com/michal-h21/tex4ebook) command,
> which is generally already included with TeX distributions.  
> It is recommended to have [`tidy`](https://github.com/htacg/tidy-html5) installed,
> which, if available, is used by `tex4ebook`.

For generating an ebook in `EPUB3` format, run this command from within the `src` directory:
```shell
tex4ebook --build-dir ../build_epub3 --output-dir ../output -f epub3 main.tex mathml
```
This generates the document in `EPUB` version 3, with mathematical notation encoded in the `MathML` format.
> [!IMPORTANT]
> The `MathML`-encoded results are currently broken:
> the generated documents have incomplete formulas, and messed up text and formatting,
> or fail to build entirely.  
> Encoding Maths content as `svg` or `png` produces more usable results,
> though some issues persist.

For `SVG` Maths, use this command:
```shell
tex4ebook --build-dir ../build_ebook_svg --output-dir ../output -f epub main.tex svg
```

For `PNG` Maths, use this command:
```shell
tex4ebook --build-dir ../build_ebook_png --output-dir ../output -f epub main.tex png
```

> [!NOTE]
> The `epub` option in the above two commands can be replaced by any format among `epub`, `epub3`, `mobi`, `azw`, `azw3`;
> but in order to generate ebooks in `mobi`, `azw` and `azw3` formats,
> [calibre](https://github.com/kovidgoyal/calibre) needs to be installed,
> because `tex4ebook` uses the command `ebook-convert`, provided by calibre.

> [!NOTE]
> The commands described above use pdfTeX as engine.
> Compilation with LuaTeX is currently not working.  
> In any case, to use LuaTeX as engine anyway, use `tex4ebook -l` in place of `tex4ebook` in the commands.


### Compilation variants

Various compilation options are available for customising the document.
They are identified by the following keywords:
- `ORIGINAL`: to print the original problems
- `GENERALISED`: to print the generalised problems
- `ALL`: to print both the original and the generalised problems (equivalent to setting both `ORIGINAL` and `GENERALISED`)
> [!NOTE]
> `ORIGINAL` is enabled by default if none among `GENERALISED` and `ALL` is set.

- `UNCATEGORISED`: to not subdivide the problems into categories by topic
- `NUMBERCATEGORIES`: to make the categories sections numbered (only has effect if `UNCATEGORISED` is not set)
- `GLOBALNUMBERING`: to number the problems globally instead of within sections (this is automatic if `UNCATEGORISED` is set)

- `NOSOLUTIONS`: to not print the solutions
- `ONLYSOLUTIONS`: to only print the solutions
> [!WARNING]
> Setting both `NOSOLUTIONS` and `ONLYSOLUTIONS` will result in an empty document.

- `NOSOURCES`: to omit printing the sources at each problem statement
- `MOREREFS`: to print additional references for further reading (at the end of the document, after the main references)
- `FORUMREFS`: to print references to user discussions (at the end of the document, after the other references)

- `MINIMAL`: to omit introduction, table of contents, sources, and references

<br>

To specify the desired options when building the document as a PDF,
use the following command to compile, replacing each "`OPTION`" with a desired option from the above list
(any number of options can be specified with this syntax):
```shell
latexmk -g -usepretex='\def\OPTION{} \def\OPTION{}' main.tex
```

To specify options in ebook generation,
add `"" "" '\\def\\OPTION{} \\def\\OPTION{}'`
at the end of the `tex4ebook` command, like this:
```shell
tex4ebook --build-dir ../build_ebook_svg --output-dir ../output -f epub -e main.tex svg "" "" '\\def\\OPTION{} \\def\\OPTION{}'
```
> [!IMPORTANT]
> Make sure to enclose the string of options in single quotes,
> or escape the backslashes if using double quotes: `"\\\\def\\\\OPTION{} \\\\def\\\\OPTION{}"`.
> Make sure that the string containing the options is the fifth positional argument;
> if omitting the `svg` or `png` or `mathml` argument, then an extra empty string `""` is needed in its place.

<br>


<details><summary>Some examples</summary>
<p>

- to get the generalised problems:
```shell
latexmk -g -usepretex='\def\GENERALISED{}' main.tex
```
```shell
tex4ebook -B ../build_ebook_svg -d ../output -f epub main.tex svg "" "" '\\def\\GENERALISED{}'
```
- to get the statements of the original problems, without the solutions:
```shell
latexmk -g -usepretex='\def\NOSOLUTIONS{}' main.tex
```
```shell
tex4ebook -B ../build_ebook_svg -d ../output -f epub main.tex svg "" "" '\\def\\NOSOLUTIONS{}'
```
- to get the solutions to the generalised problems:
```shell
latexmk -g -usepretex='\def\GENERALISED{} \def\ONLYSOLUTIONS{}' main.tex
```
```shell
tex4ebook -B ../build_ebook_svg -d ../output -f epub main.tex svg "" "" '\\def\\GENERALISED{} \\def\\ONLYSOLUTIONS{}'
```
- to get a minimal document, containing both original and generalised problems, without subdividing the problems by topic:
```shell
latexmk -g -usepretex='\def\ALL{} \def\UNCATEGORISED{} \def\MINIMAL{}' main.tex
```
```shell
tex4ebook -B ../build_ebook_svg -d ../output -f epub main.tex svg "" "" '\\def\\ALL{} \\def\\UNCATEGORISED{} \\def\\MINIMAL{}'
```

</p>
</details>


### Reproducible builds

PDF builds are reproducible.  
In order to reproduce a PDF build,
use the same TeX distribution, version, and engine as the target file,
set the environment variable `SOURCE_DATE_EPOCH` to match that of the target build
(and consider setting `FORCE_SOURCE_DATE=1` too),
set the same compilation options (if any),
and use the same `-jobname`:
```shell
SOURCE_DATE_EPOCH=0 FORCE_SOURCE_DATE=1 latexmk -g -usepretex='\def\OPTION{} \def\OPTION{}' main.tex -jobname="jobname"
```
All the required parameters are kept up-to-date [here](https://coffinproblems.github.io/coffins/build_env.txt).


### PDF standards compliance

The PDF files are conformant with
the [PDF/A-4f](https://pdfa.org/resource/iso-19005-4-pdf-a-4/) standard,
and the accessibility standards
[PDF/UA-2](https://pdfa.org/iso-14289-2-pdfua-2/)
and [WTPDF-1.0 (Well-Tagged PDF)](https://pdfa.org/wtpdf);
their PDF version is [PDF 2.0](https://pdfa.org/resource/iso-32000-2/).

When building the project from source, by default the standard is set to
[PDF/A-2u](https://pdfa.org/resource/iso-19005-2-pdf-a-2/),
with PDF version [PDF 1.7](https://pdfa.org/resource/iso-32000-1/).

For building PDFs satisfying the other standards (`PDF/A-4f`, `PDF/UA-2`, `WTPDF-1.0`, `PDF 2.0`)
use the compilation option `TAGPDF` (together with any other desired compilation options):
```shell
latexmk -g -usepretex='\def\TAGPDF{}' main.tex
```
> [!NOTE]
> A TeX distribution version from 2025 or later is required for this.
> Additionally, compilation needs to be performed with LuaLaTeX (not with PDFLaTeX).

It is also possible to build PDF files satisfying
the [PDF/A-3a](https://pdfa.org/resource/iso-19005-3-pdf-a-3/) standard
and the accessibility standard [PDF/UA-1](https://pdfa.org/resource/iso-14289-pdfua/),
under PDF version [PDF 1.7](https://pdfa.org/resource/iso-32000-1/);
to do so, set the compilation option `PDFAA` (together with any other desired compilation options):
```shell
latexmk -g -usepretex='\def\PDFAA{}' main.tex
```
> [!NOTE]
> A TeX distribution version from 2025 or later is required for this.
> Additionally, compilation needs to be performed with LuaLaTeX (not with PDFLaTeX).

#### Compliance validation
Verifying that a PDF file is conformant to certain PDF standards
can be done with [VeraPDF](https://verapdf.org/),
either online at [https://demo.verapdf.org/](https://demo.verapdf.org/),
or locally.
To test a PDF file locally, run the following command (note that it requires VeraPDF to be installed):
```shell
verapdf --flavour 0 --format text path/to/file.pdf
```


<!--
### `.tex` source file
In order to generate a single `.tex` source file, a Python script is provided in the `scripts` directory.
Usage requires having Python installed.
It is used by running the following command from within the `src` directory:
```shell
python ../scripts/flatten.py main.tex
```
Some of the previously described compilation options can be used in the command, with this syntax:
```shell
python ../scripts/flatten.py main.tex OPTION OPTION
```
The other options instead are to be applied when compiling the resulting `.tex` file.

> [!WARNING]
> This Python script is meant as an alternate way to merge together the individual `.tex` files of each problem into a single `.tex` file.
> As such:
> - any changes made to the project structure require adjusting the Python script accordingly;
> - changes made to the files in `src/commands` are not going to be reflected when using this Python script;
> - modifying the `main.tex` file is likely to cause issues when running the Python script, if it does not get adjusted accordingly.
> Minimal logic is included in the Python script to account for some small changes in the `main.tex` and other files, but it is not robust.
-->


## Contact

The project can be contacted at:
- project email address: [coffin-problems@proton.me](mailto:coffin-problems@proton.me)
- maintainer: [luciano.spettoli@protonmail.com](mailto:luciano.spettoli@protonmail.com)


## License

This work is made available without restrictions.
See [LICENSE](LICENSE).


## References

> [!NOTE]
> The references are also available in `bib` format in the file [`references.bib`](/src/references/references.bib)

- Tanya Khovanova, Alexey Radul: _Jewish Problems_, 2011. (Preprint of _Killer Problems_).
    - doi: [10.48550/arXiv.1110.1556](https://doi.org/10.48550/arXiv.1110.1556)
    - URL: [https://arxiv.org/abs/1110.1556](https://arxiv.org/abs/1110.1556)
      (archived [here](https://web.archive.org/web/20260211015757/https://arxiv.org/pdf/1110.1556))

- Tanya Khovanova, Alexey Radul: _Killer Problems_, 2012.
  In _The American Mathematical Monthly_, volume 119.10, pages 815–823.
    - doi: [amer.math.monthly.119.10.815](https://doi.org/10.4169/amer.math.monthly.119.10.815)

- Tanya Khovanova: _Main list of math "coffin" problems_, 2005.
    - URL: [https://www.tanyakhovanova.com/Coffins/coffinsmain.html](https://www.tanyakhovanova.com/Coffins/coffinsmain.html)
      (archived [here](https://web.archive.org/web/20251207003425/https://www.tanyakhovanova.com/Coffins/coffinsmain.html))

- Tanya Khovanova: _Math “coffin” submitted by others_, 2008.
    - URL: [https://www.tanyakhovanova.com/Coffins/othercoffins.html](https://www.tanyakhovanova.com/Coffins/othercoffins.html)
      (archived [here](https://web.archive.org/web/20250517004330/https://www.tanyakhovanova.com/Coffins/othercoffins.html))

- Jay Egenhoff: _Math as a tool of anti-semitism_, 2014.
  In _The Mathematics Enthusiast_, volume 11.3, article 11, pages 649–664.
    - doi: [10.54870/1551-3440.1320](https://doi.org/10.54870/1551-3440.1320)
    - URL [https://scholarworks.umt.edu/cgi/viewcontent.cgi?article=1320&context=tme](https://scholarworks.umt.edu/cgi/viewcontent.cgi?article=1320&context=tme)
      (archived [here](https://web.archive.org/web/20240412101427/https://scholarworks.umt.edu/cgi/viewcontent.cgi?article=1320&context=tme))

- Alexander Khaniyevich Shen: _Entrance examinations to the Mekh-mat_, 1994.
  In _The Mathematical Intelligencer_, volume 16.4, pages 6–10.
    - doi: [10.1142/9789812701169_0008](https://doi.org/10.1142/9789812701169_0008)
    - URL: [http://www.3038.org/press/shen.pdf](http://www.3038.org/press/shen.pdf)
      (archived [here](https://web.archive.org/web/20260107193055/http://www.3038.org/press/shen.pdf))
    - Russian version: [https://www.lirmm.fr/~ashen/alexander-shen.narod.ru/vershik.pdf](https://www.lirmm.fr/~ashen/alexander-shen.narod.ru/vershik.pdf)
      (archived [here](https://web.archive.org/web/20240918040436/https://www.lirmm.fr/~ashen/alexander-shen.narod.ru/vershik.pdf))
      and at [https://alexander-shen.narod.ru/vershik.pdf](https://alexander-shen.narod.ru/vershik.pdf)
      (archived [here](https://web.archive.org/web/20250912070826/https://alexander-shen.narod.ru/vershik.pdf))

- Ilan Vardi: _Mekh-Mat entrance examinations problems_, 2000.
  (The final version of the document is contained in _You failed your math test, Comrade Einstein_ by Mikhail Arkadyevich Shifman, at pages 22–95).
    - doi: [10.1142/9789812701169_0001](https://doi.org/10.1142/9789812701169_0001)
    - URL: [https://www.lix.polytechnique.fr/Labo/Ilan.Vardi/mekh-mat.ps](https://www.lix.polytechnique.fr/Labo/Ilan.Vardi/mekh-mat.ps),
      (archived [here](https://web.archive.org/web/20251225204859/https://www.lix.polytechnique.fr/Labo/Ilan.Vardi/mekh-mat.ps));
      PDF version: [https://www.tanyakhovanova.com/Coffins/Vardi-solutions.pdf](https://www.tanyakhovanova.com/Coffins/Vardi-solutions.pdf)
      (archived [here](https://web.archive.org/web/20251207000147/https://www.tanyakhovanova.com/Coffins/Vardi-solutions.pdf))

- Boris Ilyich Kanevsky, Valery Anatolievich Senderov: _Intellectual Genocide: entrance examinations for Jews at MGU, MFTI, MIFP_, 1980.
  (Available in _You failed your math test, Comrade Einstein_ by Mikhail Arkadyevich Shifman, at pages 129–152).
    - doi: [10.1142/9789812701169_0004](https://doi.org/10.1142/9789812701169_0004)
    - Russian version: [https://www.lirmm.fr/~ashen/senderov/ig-text.pdf](https://www.lirmm.fr/~ashen/senderov/ig-text.pdf)
      (archived [here](https://web.archive.org/web/20250505152510/https://www.lirmm.fr/~ashen/senderov/ig-text.pdf))
    - Original typewritten document: [https://www.lirmm.fr/~ashen/senderov/ig-color.djvu](https://www.lirmm.fr/~ashen/senderov/ig-color.djvu)
      (archived [here](https://web.archive.org/web/20260201181835/https://www.lirmm.fr/~ashen/senderov/ig-color.djvu))

- Grigory Abelevich Freiman: _It seems I am a Jew_, 1980 (Southern Illinois University Press).
    - URL: [https://archive.org/details/freiman-english-it-seems-i-am-a-jew](https://archive.org/details/freiman-english-it-seems-i-am-a-jew)
      and [https://www.lirmm.fr/~ashen/senderov/freiman-english.pdf](https://www.lirmm.fr/~ashen/senderov/freiman-english.pdf)
      (archived [here](https://web.archive.org/web/20220121234736/https://www.lirmm.fr/~ashen/senderov/freiman-english.pdf))
    - Russian version: [https://archive.org/details/freiman-rus-tex](https://archive.org/details/freiman-rus-tex)
      and [https://www.lirmm.fr/~ashen/senderov/freiman-rus-tex.pdf](https://www.lirmm.fr/~ashen/senderov/freiman-rus-tex.pdf)
      (archived [here](https://web.archive.org/web/20220121234713/https://www.lirmm.fr/~ashen/senderov/freiman-rus-tex.pdf))

- Melvyn Bernard Nathanson: _Appendix B_, 1979,
  to _It seems I am a Jew_ by Grigory Abelevich Freiman, 1980, pages 95–96.

- Moscow Helsinki Group: _Discrimination against Jews in University Admissions_, 1979.
    - URL: [https://www.lirmm.fr/~ashen/senderov/mhg-112+pril.pdf](https://www.lirmm.fr/~ashen/senderov/mhg-112+pril.pdf)
      (archived [here](https://web.archive.org/web/20220121234719/https://www.lirmm.fr/~ashen/senderov/mhg-112+pril.pdf))

- Boris Ilyich Kanevsky, Valery Anatolievich Senderov: _Admission results of graduates of six Moscow Schools to the Faculty of Mechanics and Mathematics at Moscow State University_, 1979;
  appendix to _Discrimination against Jews in University Admissions_ by Moscow Helsinki Group.

- Aleksandr Sergeyevich Demidov: _On entrance examinations (conclusions and proposals based on analysis of documentary data)_.
    - URL: [https://www.lirmm.fr/~ashen/senderov/demidov.pdf](https://www.lirmm.fr/~ashen/senderov/demidov.pdf)
      (archived [here](https://web.archive.org/web/20220121234744/https://www.lirmm.fr/~ashen/senderov/demidov.pdf))

- Edward Vladimirovich Frenkel: _Love and Math: the heart of hidden reality_, 2013 (Basic Books), chapter 3.
    - URL of the relevant excerpt: [https://www.newcriterion.com/issues/2012/10/the-fifth-problem-math-anti-semitism-in-the-soviet-union](https://web.archive.org/web/20171010070710/https://www.newcriterion.com/issues/2012/10/the-fifth-problem-math-anti-semitism-in-the-soviet-union)
    - Russian version: [https://inosmi.ru/20121111/202009718.html](https://inosmi.ru/20121111/202009718.html)
      (archived [here](https://web.archive.org/web/20260209065935/https://inosmi.ru/20121111/202009718.html))
    - Book webpage: [https://www.edwardfrenkel.com/lovemath/](https://www.edwardfrenkel.com/lovemath/)
    - ISBN: 978-0-465-06995-8

- Mikhail Arkadyevich Shifman: _You failed your math test, Comrade Einstein_, 2005 (World Scientific).
    - doi: [10.1142/5791](https://doi.org/10.1142/5791)
    - URL: [https://www-users.cse.umn.edu/~shifman/EinsteinBook.pdf](https://www-users.cse.umn.edu/~shifman/EinsteinBook.pdf)
      (archived [here](https://web.archive.org/web/20251004025002/https://www-users.cse.umn.edu/~shifman/EinsteinBook.pdf))
    - ISBN: 978-9-812-56358-3

- Mikhail Arkadyevich Shifman: _Through the prizm of time — Angles of reflection_, Epilogue to “Comrade Einstein”.
    - URL: [https://www-users.cse.umn.edu/~shifman/Epilogue_12_28_2016.pdf](https://www-users.cse.umn.edu/~shifman/Epilogue_12_28_2016.pdf)
      (archived [here](https://web.archive.org/web/20251116145012/https://www-users.cse.umn.edu/~shifman/Epilogue_12_28_2016.pdf))
    - Updated version: [https://www.lirmm.fr/~ashen/senderov/shifman2020.pdf](https://www.lirmm.fr/~ashen/senderov/shifman2020.pdf)
      (archived [here](https://web.archive.org/web/20220121234737/https://www.lirmm.fr/~ashen/senderov/shifman2020.pdf))
      and [https://www.academia.edu/23377054/](https://www.academia.edu/23377054/THROUGH_THE_PRIZM_OF_TIME_ANGLES_OF_REFLECTION_Epilogue_to_Comrade_Einstein_Updated_4_28_2020);
      another updated version, differing only in the last two pages, is available at
      [https://www.academia.edu/101548394/](https://www.academia.edu/101548394/Epilogue_May_6_2023_To_You_Just_Failed_Your_Math_Test_Comrade_Einstein_World_Scientific_Singapore_2005_)

- Sergei Tabachnikov: _Review of “You failed your math test, Comrade Einstein” by M. Shifman_, 2020.
  In _The Mathematical Intelligencer_, volume 42, pages 83–87.
    - doi: [10.1007/s00283-020-09976-y](https://doi.org/10.1007/s00283-020-09976-y)
    - URL: [https://drive.google.com/file/d/1hrcikumwsJ-svqattfX_cvc76CaU-6HG/](https://drive.google.com/file/d/1hrcikumwsJ-svqattfX_cvc76CaU-6HG/)
      (archived [here](https://web.archive.org/web/20260201183616/https://drive.usercontent.google.com/download?id=1hrcikumwsJ-svqattfX_cvc76CaU-6HG))

- User "arbat" on LiveJournal, 2003.
    - URL: [https://bbb.livejournal.com/787297.html?thread=2688609#t2688609](https://bbb.livejournal.com/787297.html?thread=2688609#t2688609)
      (archived [here](https://archive.today/OX7Ks#selection-11435.0-11422.12),
      [here](https://ljsear.ch/savedcopy?comm=1344985597),
      and [here](https://web.archive.org/web/20260201212300/https://ljsear.ch/savedcopy?comm=1344985597)).  
      See also: [https://bbb.livejournal.com/787297.html?thread=2698081#t2698081](https://bbb.livejournal.com/787297.html?thread=2698081#t2698081)
      (archived [here](https://ljsear.ch/savedcopy?comm=1875114955) and [here](https://web.archive.org/web/20260201212808/https://ljsear.ch/savedcopy?comm=1875114955)),
      and [https://bbb.livejournal.com/787297.html?thread=2708577#t2708577](https://bbb.livejournal.com/787297.html?thread=2708577#t2708577)
      (archived [here](https://ljsear.ch/savedcopy?comm=1236687776) and [here](https://web.archive.org/web/20260201212439/https://ljsear.ch/savedcopy?comm=1236687776)),
      and [https://bbb.livejournal.com/787297.html?thread=2733921#t2733921](https://bbb.livejournal.com/787297.html?thread=2733921#t2733921)
      (archived [here](https://web.archive.org/web/20260211051731/https://bbb.livejournal.com/787297.html?replyto=2733921)
      and [here](https://archive.today/z2tE0#t2733921)).

- User "azb1958" on LiveJournal, 2013.
    - URL: [https://azb1958.livejournal.com/34112.html](https://azb1958.livejournal.com/34112.html)
      (archived [here](https://web.archive.org/web/20210925084745/https://azb1958.livejournal.com/34112.html)).
      See also [https://azb1958.livejournal.com/34112.html?thread=141376#t141376](https://azb1958.livejournal.com/34112.html?thread=141376#t141376)
      (archived [here](https://web.archive.org/web/20260307191841/https://azb1958.livejournal.com/34112.html?replyto=141376))

- Vladimir Kelman, 2013.
    - URL: [https://kerosinka.livejournal.com/1633.html?thread=383329#t383329](https://kerosinka.livejournal.com/1633.html?thread=383329#t383329)
      (archived [here](https://web.archive.org/web/20260222040201/https://kerosinka.livejournal.com/1633.html?replyto=383329),
      [here](https://archive.today/CF4qL#t383329),
      [here](https://ljsear.ch/savedcopy?comm=1194975920),
      and [here](https://web.archive.org/web/20260201215430/https://ljsear.ch/savedcopy?comm=1194975920))

- User "nieuwe_zijde" on Blogger, 2009.
    - URL: [https://avzel.blogspot.com/2009/07/blog-post_30.html?showComment=1254948495163#c1386969495227008652](https://avzel.blogspot.com/2009/07/blog-post_30.html?showComment=1254948495163#c1386969495227008652)
      (archived [here](https://web.archive.org/web/20190610091539/https://avzel.blogspot.com/2009/07/blog-post_30.html?showComment=1254948495163#c1386969495227008652))

- _Selected entrance examination problems at the Faculty of Mechanics and Mathematics of Moscow State University in 1979_.
    - URL: [https://www.lirmm.fr/~ashen/senderov/zadachi-1979-color.djvu](https://www.lirmm.fr/~ashen/senderov/zadachi-1979-color.djvu)
      (archived [here](https://web.archive.org/web/20260227111932/https://www.lirmm.fr/~ashen/senderov/zadachi-1979-color.djvu))

- _Selected entrance examination problems at the Faculty of Mechanics and Mathematics of Moscow State University in 1982_.
    - URL: [https://www.lirmm.fr/~ashen/senderov/zadachi-1982.djvu](https://www.lirmm.fr/~ashen/senderov/zadachi-1982.djvu)
      (archived [here](https://web.archive.org/web/20260223071158/https://www.lirmm.fr/~ashen/senderov/zadachi-1982.djvu))

- _Selected entrance examination problems at the Faculty of Mechanics and Mathematics of Moscow State University in 1986_.
    - URL: [https://www.lirmm.fr/~ashen/senderov/zadachi-1986-color.djvu](https://www.lirmm.fr/~ashen/senderov/zadachi-1986-color.djvu)
      (archived [here](https://web.archive.org/web/20260226060451/https://www.lirmm.fr/~ashen/senderov/zadachi-1986-color.djvu))


### Additional references

For a more complete historical overview, below are some additional resources.
> [!NOTE]
> These additional resources are also listed in `bib` format in the file [`further_reading.bib`](/src/references/further_reading.bib).

- Alexander Khaniyevich Shen: _Materials related to entrance exams_.
  Collection of many resources.
    - URL: [https://www.lirmm.fr/~ashen/senderov/](https://www.lirmm.fr/~ashen/senderov/)
      (archived [here](https://web.archive.org/web/20260202212304/https://www.lirmm.fr/~ashen/senderov/))

- Gina Bari Kolata: _Anti-semitism alleged in Soviet Mathematics_, 1978.
  In _Science_, volume 202.4373, pages 1167–1170.
    - doi: [10.1126/science.202.4373.1167](https://doi.org/10.1126/science.202.4373.1167)
    - URL: [https://www.science.org/doi/10.1126/science.202.4373.1167](https://www.science.org/doi/10.1126/science.202.4373.1167)

- Gina Bari Kolata: _A program to aid Soviet Jewish mathematicians_, 1978.
  In _Science_, volume 202.4373, page 1168.
    - doi: [10.1126/science.202.4373.1168](https://doi.org/10.1126/science.202.4373.1168)
    - URL: [https://www.science.org/doi/10.1126/science.202.4373.1168](https://www.science.org/doi/10.1126/science.202.4373.1168)
      (archived [here](https://web.archive.org/web/20230124012023/https://www.science.org/cms/10.1126/science.202.4373.1168/asset/5d075426-3a0b-4ff5-8151-a506de58ce0d/assets/science.202.4373.1168.fp.png))

- George Greene: _Problems_, 1979 (in response to _Anti-semitism alleged in Soviet Mathematics_ by Gina Bari Kolata).
  In _Science_, volume 203.4380, page 501.
    - doi: [10.1126/science.203.4380.501.b](https://doi.org/10.1126/science.203.4380.501.b)
    - URL: [https://www.science.org/doi/10.1126/science.203.4380.501.b](https://www.science.org/doi/10.1126/science.203.4380.501.b)
      (archived [here](https://web.archive.org/web/20260521211118im_/https://www.science.org/cms/10.1126/science.203.4380.501.b/asset/f7a439ea-4571-4bc3-b63e-f051f0d89576/assets/science.203.4380.501.b.fp.png))

- Gina Bari Kolata: _Response: Problems_, 1979 (in response to _Problems_ by George Greene).
  In _Science_, volume 203.4380, page 501.
    - doi: [10.1126/science.203.4380.501.c](https://doi.org/10.1126/science.203.4380.501.c)
    - URL: [https://www.science.org/doi/10.1126/science.203.4380.501.c](https://www.science.org/doi/10.1126/science.203.4380.501.c)
      (archived [here](https://web.archive.org/web/20240310231109im_/https://www.science.org/cms/10.1126/science.203.4380.501.a/asset/660b82a2-8d72-45c6-b611-f99c4f61ba33/assets/science.203.4380.501.a.fp.png))

- Lev Semyonovich Pontryagin: _Soviet anti-semitism: reply by Pontryagin_, 1979 (in response to _Anti-semitism alleged in Soviet Mathematics_ by Gina Bari Kolata).
  In _Science_, volume 205.4411, pages 1083–1084.
    - doi: [10.1126/science.205.4411.1083](https://doi.org/10.1126/science.205.4411.1083)
    - URL: [https://www.science.org/doi/10.1126/science.205.4411.1083](https://www.science.org/doi/10.1126/science.205.4411.1083)

- Lipman Bers, R. H. Bing, Henri Cartan, P. D. Lax, Saunders Mac Lane, Deane Montgomery, Georges de Rham, Marshall Stone, Oscar Zariski: _An unpublished reply_, 1980.
  In _Science_, volume 208.4439, page 6.
    - doi: [10.1126/science.208.4439.6.c](https://doi.org/10.1126/science.208.4439.6.c)
    - URL: [https://www.science.org/doi/10.1126/science.208.4439.6.c](https://www.science.org/doi/10.1126/science.208.4439.6.c)
      (archived [here](https://web.archive.org/web/20240120062937/https://www.science.org/cms/10.1126/science.208.4439.6.c/asset/81c1037b-fda2-4a40-b2b0-c396bc556471/assets/science.208.4439.6.c.fp.png))


- Alexander Lichtman: _Moscow's new wave of anti-semitism_, 1980.
    - URL: [https://www.csmonitor.com/1980/0430/043032.html](https://www.csmonitor.com/1980/0430/043032.html)
      (archived [here](https://web.archive.org/web/20230321081745/https://www.jewishheroes.live/kanevskiy-boris))

- Alexey Savelyev: _Memo to a Jew entering the Faculty of Mechanics and Mathematics of Moscow State University_.
    - URL: [https://arzamas.academy/materials/1148](https://web.archive.org/web/20171023084427/https://arzamas.academy/materials/1148)
      (also [here](https://web.archive.org/web/20161210142921/https://arzamas.academy/materials/1148))

- Anatoly Moiseevich Vershik: _Admission to the mathematics faculty in Russia in the 1970s and 1980s_, 1994.
  In _The Mathematical Intelligencer_, volume 16.4, pages 4–5.
    - doi: [10.1142/9789812701169_0007](https://doi.org/https://www.lirmm.fr/~ashen/senderov/demidov.pdf)
    - URL: [http://www.3038.org/press/vershik.pdf](http://www.3038.org/press/vershik.pdf)
      (archived [here](https://web.archive.org/web/20260101182201/http://www.3038.org/press/vershik.pdf))

- Mark E. Saul: _Kerosinka: an episode in the history of Soviet Mathematics_, 1999.
  In _The Notices of the American Mathematical Society_, volume 46.10, pages 1217–1220.
    - URL: [https://www.ams.org/notices/199910/fea-saul.pdf](https://www.ams.org/notices/199910/fea-saul.pdf)
      (archived [here](https://web.archive.org/web/20250225121117/https://www.ams.org/notices/199910/fea-saul.pdf))

- George Geza Szpiro: _Bella Abramovna Subbotovskaya and the “Jewish People’s University”_, 2007.
  In _The Notices of the American Mathematical Society_, volume 54.10, pages 1326–1330.
    - doi: [10.1090/mbk/073/14](https://doi.org/10.1090/mbk/073/14)
    - URL: [https://www.ams.org/notices/200710/tx071001326p.pdf](https://www.ams.org/notices/200710/tx071001326p.pdf)
      (archived [here](https://web.archive.org/web/20250410163521/https://www.ams.org/notices/200710/tx071001326p.pdf))

- Valery Anatolievich Senderov: _Without partaking of the Buffalo — In memory of Bella Abramovna Subbotovskaya_, 2011.
    - URL: [https://volgograd.yabloko.ru/news/index.phtml?id=1871](https://web.archive.org/web/20190927215546/https://volgograd.yabloko.ru/news/index.phtml?id=1871)

- _Bella Subbotovskaya and her University_, 2007.
    - Part 1: [https://www.youtube.com/watch?v=Xyak7yINMsI](https://www.youtube.com/watch?v=Xyak7yINMsI)
    - Part 2: [https://www.youtube.com/watch?v=8CEN6nIN4Dk](https://www.youtube.com/watch?v=8CEN6nIN4Dk)
    - Part 3: [https://www.youtube.com/watch?v=NDmzWMM_8wQ](https://www.youtube.com/watch?v=NDmzWMM_8wQ)

- Wikipedia: _Bella Abramovna Subbotovskaya_.
    - Russian page: [https://ru.wikipedia.org/wiki/Субботовская,_Белла_Абрамовна](https://ru.wikipedia.org/wiki/%D0%A1%D1%83%D0%B1%D0%B1%D0%BE%D1%82%D0%BE%D0%B2%D1%81%D0%BA%D0%B0%D1%8F,_%D0%91%D0%B5%D0%BB%D0%BB%D0%B0_%D0%90%D0%B1%D1%80%D0%B0%D0%BC%D0%BE%D0%B2%D0%BD%D0%B0)
    - English page: [https://en.wikipedia.org/wiki/Bella_Subbotovskaya](https://en.wikipedia.org/wiki/Bella_Subbotovskaya)

- Jewish Agency: _Anti-semitism in Soviet Science: research and memories — In memory of Bella Subbotovskaya_.
    - Russian page: [https://www.jafi.org/JewishAgency/Russian/Education/Jewish+History/40/JPUM/Download.htm](https://web.archive.org/web/20110726200847/https://www.jafi.org/JewishAgency/Russian/Education/Jewish+History/40/JPUM/Download.htm)
    - English page: [https://www.jafi.org/JewishAgency/English/Jewish+Education/Compelling+Content/Eye+on+Israel/Aliyah/40/Scientists/Download.htm](https://web.archive.org/web/20080215090531/https://www.jafi.org/JewishAgency/English/Jewish+Education/Compelling+Content/Eye+on+Israel/Aliyah/40/Scientists/Download.htm)

- Wikipedia: _Antisemitism in Soviet Mathematics_. In particular, see the cited references.
  The Russian page is very thorough and cites many sources.
    - Russian page: [https://ru.wikipedia.org/wiki/Антисемитизм_в_советской_математике](https://ru.wikipedia.org/wiki/%D0%90%D0%BD%D1%82%D0%B8%D1%81%D0%B5%D0%BC%D0%B8%D1%82%D0%B8%D0%B7%D0%BC_%D0%B2_%D1%81%D0%BE%D0%B2%D0%B5%D1%82%D1%81%D0%BA%D0%BE%D0%B9_%D0%BC%D0%B0%D1%82%D0%B5%D0%BC%D0%B0%D1%82%D0%B8%D0%BA%D0%B5)
    - English page: [https://en.wikipedia.org/wiki/Antisemitism_in_Soviet_mathematics](https://en.wikipedia.org/wiki/Antisemitism_in_Soviet_mathematics)

- Ilya Polyak: _Notes on anti-semitism in Soviet Science_, 2003.
    - URL: [https://proza.ru/2003/12/24-97](https://proza.ru/2003/12/24-97)
      (archived [here](https://web.archive.org/web/20180306150842/https://www.proza.ru/2003/12/24-97))

- Alexander Kostinsky, Vladimir Gubailovsky: _Discrimination in admission to higher education institutions in the Soviet Union_, 2005.
    - URL: [https://www.svoboda.org/a/126672.html](https://www.svoboda.org/a/126672.html)
      (archived [here](https://web.archive.org/web/20260113102947/https://www.svoboda.org/a/126672.html)
      and [here](https://web.archive.org/web/20090711093724/https://www.svobodanews.ru/content/article/126672.html))

- Yuli Kosharovsky: _We are Jews again: Jewish activism in the Soviet Union_, Volume 2, Part 5, chapter 31.
    - URL of the relevant excerpt: [https://pubs.ejwiki.org/wiki/Юлий_Кошаровский%E2%97%8F%E2%97%8FМы_снова_евреи%E2%97%8FГлава_31](https://web.archive.org/web/20260121124848/https://pubs.ejwiki.org/wiki/%D0%AE%D0%BB%D0%B8%D0%B9_%D0%9A%D0%BE%D1%88%D0%B0%D1%80%D0%BE%D0%B2%D1%81%D0%BA%D0%B8%D0%B9%E2%97%8F%E2%97%8F%D0%9C%D1%8B_%D1%81%D0%BD%D0%BE%D0%B2%D0%B0_%D0%B5%D0%B2%D1%80%D0%B5%D0%B8%E2%97%8F%D0%93%D0%BB%D0%B0%D0%B2%D0%B0_31)
      and [https://kosharovsky.com/глава-31-дети-в-отказе/](https://web.archive.org/web/20220707140409/https://kosharovsky.com/%D0%B3%D0%BB%D0%B0%D0%B2%D0%B0-31-%D0%B4%D0%B5%D1%82%D0%B8-%D0%B2-%D0%BE%D1%82%D0%BA%D0%B0%D0%B7%D0%B5/)
    - Book: [https://pubs.ejwiki.org/wiki/Юлий_Кошаровский%E2%97%8F%E2%97%8FМы_снова_евреи](https://web.archive.org/web/20250613231740/https://pubs.ejwiki.org/wiki/%D0%AE%D0%BB%D0%B8%D0%B9_%D0%9A%D0%BE%D1%88%D0%B0%D1%80%D0%BE%D0%B2%D1%81%D0%BA%D0%B8%D0%B9%E2%97%8F%E2%97%8F%D0%9C%D1%8B_%D1%81%D0%BD%D0%BE%D0%B2%D0%B0_%D0%B5%D0%B2%D1%80%D0%B5%D0%B8)


- Mikhail Anatolyevich Tsfasman: _The fate of Mathematics in Russia_, 2009.
    - URL: [https://polit.ru/article/2009/01/30/matematika/](https://web.archive.org/web/20191009025605/https://polit.ru/article/2009/01/30/matematika/)

- Natalia Demina, Yuliy Sergeevich Ilyashenko: _"In Russia it is necessary to preserve all healthy, original forms of science and education"_, 2009.
    - URL: [https://www.polit.ru/article/2009/07/14/ilyashenko1/](https://web.archive.org/web/20151208115700/https://www.polit.ru/article/2009/07/14/ilyashenko1/)

- Natalia Demina, Yuliy Sergeevich Ilyashenko: _The «Black 20th Anniversary» of the Faculty of Mechanics and Mathematics of Moscow State University_, 2009.
    - URL: [https://www.polit.ru/article/2009/07/28/ilyashenko2/](https://web.archive.org/web/20191023194611/https://www.polit.ru/article/2009/07/28/ilyashenko2/)

- Leonid Kostyukov: _Witness of the Black Years_, 2009.
    - URL: [https://polit.ru/article/2009/07/30/mehmat/](https://web.archive.org/web/20210421103958/https://polit.ru/article/2009/07/30/mehmat/)

- Leonid Kostyukov: _Refrigerator and wheelbarrow_, 2011.
    - URL: [https://polit.ru/country/2011/06/12/ussr.html](https://web.archive.org/web/20110615203740/https://polit.ru/country/2011/06/12/ussr.html)

- Natalia Demina, Anatoly Moiseevich Vershik: _Through the eyes of a mathematician_, 2013.
    - URL: [https://polit.ru/article/2013/02/25/vershik1/](https://web.archive.org/web/20161109084614/https://polit.ru/article/2013/02/25/vershik1/)

- Joseph Polterovich: _Valery Senderov, righteous of the world_, 2012.
    - URL: [https://polit.ru/article/2012/11/11/senderov/](https://web.archive.org/web/20201022095751/https://polit.ru/article/2012/11/11/senderov/)

- Natalia Demina, Valery Anatolievich Senderov: _Against the tide_, 2014.
    - URL: [https://polit.ru/article/2014/12/23/senderov_memory/](https://web.archive.org/web/20200803190845/https://polit.ru/article/2014/12/23/senderov_memory/)

- Mikhail Arkadyevich Shifman, Boris Ilyich Kanevsky, Konstantin Sonin: _Senderov — fighter against intellectual genocide_, 2012.
    - URL: [https://www.trv-science.ru/2012/12/senderov-borec-s-intellektualnym-genocidom/](https://www.trv-science.ru/2012/12/senderov-borec-s-intellektualnym-genocidom/)
      (archived [here](https://web.archive.org/web/20260223172204/https://www.trv-science.ru/2012/12/senderov-borec-s-intellektualnym-genocidom/))

- Anna Rudnitskaya: _Prince Myshkin is against anti-semites_, 2012.
    - URL: [https://www.jewish.ru/history/hatred/2012/11/news994313124.php](https://web.archive.org/web/20161102010551/https://www.jewish.ru/history/hatred/2012/11/news994313124.php)

- Pavel Protsenko: _Valery Senderov needs help: help the modern «Prince Myshkin»!_, 2012.
    - URL: [https://graniru.org/blogs/free/entries/207860.html](https://graniru.org/blogs/free/entries/207860.html)
      (archived [here](https://web.archive.org/web/20190924102029/https://graniru.org/blogs/free/entries/207860.html))

- Pavel Protsenko: _Only mercy is constant: help Valery Senderov_, 2012.
    - URL: [https://graniru.org/blogs/free/entries/208635.html](https://graniru.org/blogs/free/entries/208635.html)
      (archived [here](https://web.archive.org/web/20230907073217/https://graniru.org/blogs/free/entries/208635.html))

- Jewish Heroes: _Boris Kanevsky_, 2021.
    - URL: [https://www.jewishheroes.live/heroes/kanevskiy-boris](https://www.jewishheroes.live/heroes/kanevskiy-boris)
      (archived [here](https://web.archive.org/web/20251212223702/https://www.jewishheroes.live/heroes/kanevskiy-boris));
      see also [https://www.jewishheroes.live/kanevskiy-boris](https://web.archive.org/web/20230321081745/https://www.jewishheroes.live/kanevskiy-boris)

- Moscow Helsinki Group: _Members of the MHG (1976–1982) — Meyman Naum Natanovich_.
    - URL: [https://www.mhg.ru/history/1B3270D](https://web.archive.org/web/20160104204800/https://www.mhg.ru/history/1B3270D)


- Canadian Mathematical Society: _Three Honoured for Outstanding Research Achievements_, 2009.
    - URL: [https://www2.cms.math.ca/MediaReleases/2009/res-prizes#jw](https://www2.cms.math.ca/MediaReleases/2009/res-prizes#jw)
      (archived [here](https://web.archive.org/web/20251110162537/https://www2.cms.math.ca/MediaReleases/2009/res-prizes#jw))

- Karl Grandin (editor): _Andre Geim — Biographical_, 2010 (The Nobel Foundation).
  Also contained in _Nobel Lectures in Physics (2006–2010)_ by Lars Brink (editor), 2014 (World Scientific), at pages 297–309.
    - URL: [https://www.nobelprize.org/prizes/physics/2010/geim/biographical/](https://www.nobelprize.org/prizes/physics/2010/geim/biographical/)
      (archived [here](https://web.archive.org/web/20260215111152/https://www.nobelprize.org/prizes/physics/2010/geim/biographical/))
    - Book: [https://archive.org/details/nobel-lectures-in-physics-1942-1962-by-nobel-foundation%2D%7A%2D%6C%69%62%2E%6F%72%67/](https://archive.org/details/nobel-lectures-in-physics-1942-1962-by-nobel-foundation%2D%7A%2D%6C%69%62%2E%6F%72%67/Nobel%20Lectures%20in%20Physics%20%282006%20-%202010%29%20by%20Lars%20Brink%2C%20Lars%20Brink%20%28%7A%2D%6C%69%62%2E%6F%72%67%29/)
    - Book ISBN: 978-981-4612-67-8 and 978-981-4612-68-5

- Natalia Demina, Andre Geim: _«I — European citizen»_, 2016.
    - URL: [https://www.trv-science.ru/2016/08/ya-grazhdanin-evropy/](https://web.archive.org/web/20231024053243/https://www.trv-science.ru/2016/08/ya-grazhdanin-evropy/)


- Igor Pak: _College admissions I. Discrimination and lies, Jews and Harvard_, 2012.
    - URL: [https://igorpak.wordpress.com/2012/12/26/college-admissions-discrimination/](https://igorpak.wordpress.com/2012/12/26/college-admissions-discrimination/)
      (archived [here](https://web.archive.org/web/20260227175113/https://igorpak.wordpress.com/2012/12/26/college-admissions-discrimination/))

- Mark Ginsburg: _Pogroms in Russian Mathematics_, 2014.
  In _Time and Place_, volume 2.30.
    - URL: [https://reading-hall.ru/publication.php?id=9699](https://reading-hall.ru/publication.php?id=9699)
      (archived [here](https://web.archive.org/web/20250510165806/https://reading-hall.ru/publication.php?id=9699))


- Natalya Frolova: _«I behaved incorrectly at the exam – like a Jew». How in the USSR, the fifth column prevented people from entering the Faculty of Mechanics and Mathematics at Moscow State University_, 2020.
    - URL: [https://theins.ru/confession/234674](https://theins.ru/confession/234674)
      (archived [here](https://web.archive.org/web/20260302165041/https://theins.ru/confession/234674))

- Natalya Frolova: _«Are they going to take us – straight to Auschwitz?» Anti-semitism at Moscow State University in the Soviet era in the memoirs of human rights activists_, 2020.
    - URL: [https://theins.ru/knigi/234677](https://theins.ru/knigi/234677)
      (archived [here](https://web.archive.org/web/20251102182455/https://theins.ru/knigi/234677))


- Bella Kerdman: _Unfinished book_, 2000.
    - URL: [https://www.vestnik.com/issues/2000/0229/win/kerdman.htm](https://web.archive.org/web/20110804234656/https://www.vestnik.com/issues/2000/0229/win/kerdman.htm)

- Asya Entova _All too familiar discrimination_, 2008.
    - URL: [https://asya.rjews.net/politik/081200-diskrim.shtml](https://asya.rjews.net/politik/081200-diskrim.shtml)
      (archived [here](https://web.archive.org/web/20090618034104/https://asya.rjews.net/politik/081200-diskrim.shtml))

- Tanya Khovanova: _A Hole for Jews_, 2009.
    - URL: [https://blog.tanyakhovanova.com/2009/03/a-hole-for-jews/](https://blog.tanyakhovanova.com/2009/03/a-hole-for-jews/)
      (archived [here](https://web.archive.org/web/20251201030836/https://blog.tanyakhovanova.com/2009/03/a-hole-for-jews/))

- Tanya Khovanova: _The Defining Moment_, 2009.
    - URL: [https://blog.tanyakhovanova.com/2009/09/the-defining-moment/](https://blog.tanyakhovanova.com/2009/09/the-defining-moment/)
      (archived [here](https://web.archive.org/web/20260212113602/https://blog.tanyakhovanova.com/2009/09/the-defining-moment/))

- Tanya Khovanova: _A Math Exam’s Hidden Agenda_, 2011.
    - URL: [https://blog.tanyakhovanova.com/2011/05/a-math-exams-hidden-agenda/](https://blog.tanyakhovanova.com/2011/05/a-math-exams-hidden-agenda/)
      (archived [here](https://web.archive.org/web/20251208080600/https://blog.tanyakhovanova.com/2011/05/a-math-exams-hidden-agenda/))

- Tanya Khovanova: _The Hidden Agenda Revealed_, 2011.
    - URL: [https://blog.tanyakhovanova.com/2011/05/the-hidden-agenda-revealed/](https://blog.tanyakhovanova.com/2011/05/the-hidden-agenda-revealed/)
      (archived [here](https://web.archive.org/web/20251205120747/https://blog.tanyakhovanova.com/2011/05/the-hidden-agenda-revealed/))

- Tanya Khovanova: _The Oral Exam_, 2011.
    - URL: [https://blog.tanyakhovanova.com/2011/05/the-oral-exam/](https://blog.tanyakhovanova.com/2011/05/the-oral-exam/)
      (archived [here](https://web.archive.org/web/20210224202653/https://blog.tanyakhovanova.com/2011/05/the-oral-exam/))

- Tanya Khovanova: _Arnold’s Advice_, 2022.
    - URL: [https://blog.tanyakhovanova.com/2022/04/arnolds-advice/](https://blog.tanyakhovanova.com/2022/04/arnolds-advice/)
      (archived [here](https://web.archive.org/web/20260217211323/https://blog.tanyakhovanova.com/2022/04/arnolds-advice/))


- Yevgeni Berkovich: _Editor's word_, 2003.
  In _Notes on Jewish History_, Number 34.
    - URL: [https://berkovich-zametki.com/Nomer34/Redakt0.htm](https://berkovich-zametki.com/Nomer34/Redakt0.htm)
      (archived [here](https://web.archive.org/web/20120601130734/https://berkovich-zametki.com/Nomer34/Redakt0.htm))

- Yevgeni Berkovich: _Mikhail Tsalenko_.
    - URL: [https://z.berkovich-zametki.com/avtory/calenko/](https://z.berkovich-zametki.com/avtory/calenko/)
      (archived [here](https://web.archive.org/web/20111012070346/https://berkovich-zametki.com/Avtory/Calenko.htm))

- Mikhail Shamshonovich Tsalenko: _Facts that it is preferable not to remember_, 2009 (written in 1988).
  (See also the comments).
    - URL: [https://berkovich-zametki.com/2011/Zametki/Nomer7/Calenko1.php](https://berkovich-zametki.com/2011/Zametki/Nomer7/Calenko1.php)
      (archived [here](https://web.archive.org/web/20260218071345/https://berkovich-zametki.com/2011/Zametki/Nomer7/Calenko1.php))

- Mikhail Shamshonovich Tsalenko: _Episodes of life_, 2011.
    - URL: [https://berkovich-zametki.com/2011/Zametki/Nomer9/Calenko1.php](https://berkovich-zametki.com/2011/Zametki/Nomer9/Calenko1.php)
      (archived [here](https://web.archive.org/web/20260301080722/https://berkovich-zametki.com/2011/Zametki/Nomer9/Calenko1.php))

- Mikhail Shamshonovich Tsalenko: _A look back from the blind eyes — Last month of Summer_, 2013.
    - URL: [https://7iskusstv.com/2013/Nomer6/Calenko1.php](https://7iskusstv.com/2013/Nomer6/Calenko1.php)
      (archived [here](https://web.archive.org/web/20241210235501/https://7iskusstv.com/2013/Nomer6/Calenko1.php))

- Mikhail Shamshonovich Tsalenko: _A look back from the blind eyes — Time for change_, 2013.
    - URL: [https://7iskusstv.com/2013/Nomer5/Calenko1.php](https://7iskusstv.com/2013/Nomer5/Calenko1.php)
      (archived [here](https://web.archive.org/web/20251217071520/https://7iskusstv.com/2013/Nomer5/Calenko1.php))

- Vladimir Ilyich Babitsky: _Smoke of the Fatherland_, 2013.
    - URL: [https://www.berkovich-zametki.com/2013/Zametki/Nomer2/Babicky1.php](https://www.berkovich-zametki.com/2013/Zametki/Nomer2/Babicky1.php)
      (archived [here](https://web.archive.org/web/20241227041051/https://www.berkovich-zametki.com/2013/Zametki/Nomer2/Babicky1.php))


- Julia Schulman, Michael Hsieh: _Coffin Problems — How Soviet anti-Semitism buried Jewish scientists_, 2021.
    - URL: [https://www.tabletmag.com/sections/science/articles/coffin-problems-soviet-anti-semitism-scientists](https://www.tabletmag.com/sections/science/articles/coffin-problems-soviet-anti-semitism-scientists)
      (archived [here](https://web.archive.org/web/20251114163500/https://www.tabletmag.com/sections/science/articles/coffin-problems-soviet-anti-semitism-scientists))


- Alexander Taratorin: _Flying over Moscow – 5. Part 1_, 2005.
    - URL: [https://npj.netangels.ru/atorin/15196](https://web.archive.org/web/20121128081413/https://npj.netangels.ru/atorin/15196)

- Ilya Volodarsky: _Soviet College Admission — My Dad's Story (1970)_, 2013.
    - URL: [https://ivolo.me/soviet-college-admission/](https://web.archive.org/web/20171113174440/https://ivolo.me/soviet-college-admission/)


- Boris Maftsir: _Episode 5. The glass walls of Soviet Jews – where one can study – and where one cannot_, 2025.
    - URL: [https://www.youtube.com/watch?v=dzanR8x5S2U](https://www.youtube.com/watch?v=dzanR8x5S2U)


- Jessica Ravitz: _Shining light on Emory school's past anti-semitism prompts healing – and, for one man, questions_, 2012.
    - URL: [https://religion.blogs.cnn.com/2012/10/13/shining-light-on-emorys-reign-of-terror-prompts-healing-and-for-one-man-questions/](https://web.archive.org/web/20220705152654/https://religion.blogs.cnn.com/2012/10/13/shining-light-on-emorys-reign-of-terror-prompts-healing-and-for-one-man-questions/)

- Svetlana Reiter: _«I have no business in this synagogue» «31 controversial issues» of Russian history: internationalism and the «fifth column»_, 2014.
    - URL: [https://lenta.ru/articles/2014/03/17/paragraph5](https://lenta.ru/articles/2014/03/17/paragraph5)
      (archived [here](https://web.archive.org/web/20260128105444/https://lenta.ru/articles/2014/03/17/paragraph5/))


- Alina Adams: _The Nesting Dolls_, 2020 (HarperCollins).
  Fictional story inspired by the real historic events.
    - URL: [https://www.bookbrowse.com/mag/btb/index.cfm/book_number/4131/the-nesting-dolls](https://www.bookbrowse.com/mag/btb/index.cfm/book_number/4131/the-nesting-dolls)
      (archived [here](https://web.archive.org/web/20250906141906/https://www.bookbrowse.com/mag/btb/index.cfm/book_number/4131/the-nesting-dolls))
    - ISBN: 978-0-06-291094-3


### User discussions

Relevant user discussions and forum posts.
> [!NOTE]
> These references are also listed in `bib` format in the file [`discussions.bib`](/src/references/discussions.bib).


- Alexander Khaniyevich Shen: _Some more texts by Senderov and others_, 2014.
    - URL: [https://www.facebook.com/alexander.shen.182/posts/10152637548893423](https://www.facebook.com/alexander.shen.182/posts/10152637548893423)


- russhatter: _Memoirs about coffins and Mekh-Mat_, 2009.
    - URL: [https://russhatter.livejournal.com/124217.html](https://russhatter.livejournal.com/124217.html?noscroll)
      (archived [here](https://archive.today/5JF0n))

- taki_net: _Remembering the bloody Mekh-Mat_, 2009.
    - URL: [https://taki-net.livejournal.com/573156.html](https://taki-net.livejournal.com/573156.html?noscroll)
      (archived [here](https://archive.today/P1PqZ))

- Boris Lvin: _A long and sad memoir about failure to enter Leningrad State University + a small reflection_, 2003.
    - URL: [https://bbb.livejournal.com/787297.html](https://bbb.livejournal.com/787297.html?noscroll)
      (archive: [page 1](https://archive.today/UbZ0v), [page 2](https://archive.today/8EMmA))

- Boris Lvin: _Again about entering universities_, 2003.
    - URL: [https://bbb.livejournal.com/787891.html](https://bbb.livejournal.com/787891.html?noscroll)
      (archived [here](https://archive.today/ssMnb))

- cema: _About Jews in Kerosinka_, 2003.
    - URL: [https://kerosinka.livejournal.com/1633.html](https://kerosinka.livejournal.com/1633.html?noscroll)
      (archived [here](https://archive.today/15tTW)
      and [here](https://web.archive.org/web/20260306182450/https://kerosinka.livejournal.com/1633.html))

- sTHINKs, 2010.
    - URL: [https://sthinks.livejournal.com/111250.html](https://sthinks.livejournal.com/111250.html?noscroll)
      (archived [here](https://archive.today/WLmKm))

- Dina Safyan: _Per aspera ad astra_, 2013.
    - URL: [https://sid75.livejournal.com/106678.html](https://sid75.livejournal.com/106678.html?noscroll)
      (archive: [page 1](https://archive.today/VO9D5),
                [page 2](https://archive.today/Px14N),
                [page 3](https://archive.today/4r1iR),
                [page 4](https://archive.today/TIF7z),
                [page 5](https://archive.today/ULk8g),
                [page 6](https://archive.today/J1ZWY),
                [page 7](https://archive.today/K4EXF),
                [page 8](https://archive.today/YVZa2))

- Dima Shkolnik: _Witness from the other side_, 2003.
    - URL: [https://scolar.livejournal.com/71769.html](https://scolar.livejournal.com/71769.html?noscroll)
      (archived [here](https://archive.today/8dGma))

- Lilya Polenova: _atorin [Alexander Taratorin] recounts how he entered the University_, 2005.
    - URL: [https://polenova.livejournal.com/8679.html](https://polenova.livejournal.com/8679.html?noscroll)
      (archive: [page 1](https://archive.today/8bngb), [page 2](https://archive.today/jQjzM), [page 3](https://archive.today/ExiwV))

- Alexander Khaniyevich Shen: _letter from Shafarevich, early 1990s_, 2017.
    - URL: [https://a-shen.livejournal.com/106775.html](https://a-shen.livejournal.com/106775.html?noscroll)
      (archived [here](https://archive.today/lr8vA))

- Alexander Khaniyevich Shen: _in memory of Valery Anatolyevich Senderov (continued)_, 2014.
    - URL: [https://a-shen.livejournal.com/72572.html](https://a-shen.livejournal.com/72572.html?noscroll)
      (archived [here](https://archive.today/pCMym))

- Anatoly Vorobey: _A quick look at LiveJournal: Jewish quotas_, 2003.
    - URL: [https://avva.livejournal.com/831661.html](https://avva.livejournal.com/831661.html?noscroll)
      (archived [here](https://archive.today/VgiAr) and [here](https://web.archive.org/web/20260306162431/https://avva.livejournal.com/831661.html?noscroll))

- ipain: _series 1 - Experiments with the "cleansing" situation. Material and experiments_, 2003.
    - URL: [https://ipain.livejournal.com/177018.html](https://ipain.livejournal.com/177018.html?noscroll)
      (archived [here](https://archive.today/hiyQc))

- ipain: _there is not a single interview with a single employee of the "anti-Jewish department" of the KGB_, 2003.
    - URL: [https://ipain.livejournal.com/177695.html](https://ipain.livejournal.com/177695.html?noscroll)
      (archived [here](https://archive.today/I9G4z))

- mariko_11: _Mathematician Bella Subbotovskaya_, 2013.
    - URL: [https://womantory.livejournal.com/225848.html](https://womantory.livejournal.com/225848.html?noscroll)
      (archived [here](https://archive.today/q61II) and [here](https://web.archive.org/web/20190927215540/https://womantory.livejournal.com/225848.html))

- greenbat: _The topic of national quotas for higher education during the Soviet era_, 2003.
    - URL: [https://greenbat.livejournal.com/101851.html](https://greenbat.livejournal.com/101851.html?noscroll)
      (archived [here](https://archive.today/tybcm))

- sasha_br: _Once again on anti-semitism_, 2012.
    - URL: [https://sasha-br.livejournal.com/80500.html](https://sasha-br.livejournal.com/80500.html?noscroll)
      (archived [here](https://web.archive.org/web/20260307114843/https://sasha-br.livejournal.com/80500.html?noscroll)
      and [here](https://archive.today/6IEcE))

- Konstantin Sonin: _For those who like to delve into the distant past_, 2012.
    - URL: [https://ksonin.livejournal.com/467920.html](https://ksonin.livejournal.com/467920.html?noscroll)
      (archive: [page 1](https://archive.today/CcBaJ), [page 2](https://archive.today/RZIij), [page 3](https://archive.today/7TSUq))

- Konstantin Sonin: _My admission to Moscow State University_, 2017.
    - URL: [https://ksonin.livejournal.com/627754.html](https://ksonin.livejournal.com/627754.html?noscroll)
      (archive: [page 1](https://archive.today/HHeq9), [page 2](https://archive.today/AcACt))

- Tatiana Mikhailova: _On discrimination_, 2012.
    - URL: [https://tatiana-mikhail.livejournal.com/63806.html](https://tatiana-mikhail.livejournal.com/63806.html?noscroll)
      (archived [here](https://archive.today/63Bff))

- azb1958: _named after A. A. Zhdanov_, 2013.
    - URL: [https://azb1958.livejournal.com/34112.html](https://azb1958.livejournal.com/34112.html?noscroll)
      (archived [here](https://archive.today/tDxV6))

- Andrey Rakovsky: _State anti-Semitism in the USSR — Episode one. Discriminatory quotas for Jews in universities_, 2009.
    - URL: [https://a-rakovskij.livejournal.com/265100.html](https://a-rakovskij.livejournal.com/265100.html?noscroll)
      (archived [here](https://archive.today/Nogo3))

- Alexander Khaniyevich Shen: _note to historians_, 2011.
    - URL: [https://a-shen.livejournal.com/22135.html](https://a-shen.livejournal.com/22135.html?noscroll)
      (archive: [page 1](https://archive.today/mOpHc), [page 2](https://archive.today/LaPRI))

- Alexander Khaniyevich Shen: _I saw several links to my old text about the entrance exams_, 2013.
    - URL: [https://a-shen.livejournal.com/45925.html](https://a-shen.livejournal.com/45925.html?noscroll)
      (archived [here](https://archive.today/vi8uo))

- Mikhail Arkadyevich Shifman: _A meaningless post. Preamble (written on the plane)_, 2013.
    - URL: [https://traveller2.livejournal.com/354839.html](https://traveller2.livejournal.com/354839.html?noscroll)
      (archive: [page 1](https://archive.today/u67Kz), [page 2](https://archive.today/25Kft);
      also [here](https://archive.today/5yldG))

- Mikhail Arkadyevich Shifman: _Continuation of the meaningless post (and I am writing on the plane again)_, 2013.
    - URL: [https://traveller2.livejournal.com/356025.html](https://traveller2.livejournal.com/356025.html?noscroll)
      (archived [here](https://archive.today/vbFC2);
      more recent: [page 1](https://archive.today/NfOlf), [page 2](https://archive.today/LBHbQ))

- Andrei Vladlenovich Zelevinsky: _About the Mekh-mat and more_, 2009.
    - URL: [https://avzel.blogspot.com/2009/07/blog-post_30.html](https://avzel.blogspot.com/2009/07/blog-post_30.html)
      (archived [here](https://web.archive.org/web/20151123003650/https://avzel.blogspot.com/2009/07/blog-post_30.html))

- kamen_jahr: _I'm looking for: documents regarding the state anti-semitism in the USSR (from 1953)_, 2009.
    - URL: [https://ru-history.livejournal.com/1752751.html](https://ru-history.livejournal.com/1752751.html?noscroll)
      (archived [here](https://archive.today/L9lnZ))

- Misha Verbitsky: _"People's University" (1978 - 82)_, 2005.
    - URL: [https://lj.rossia.org/users/tiphareth/649498.html](https://lj.rossia.org/users/tiphareth/649498.html)
      (archived [here](https://archive.today/K2MSL))

- bravchick: _When did they stop taking Jews to the Mekh-Mat?_, 2012.
    - URL: [https://bravchick.livejournal.com/66265.html](https://bravchick.livejournal.com/66265.html?noscroll)
      (archive: [page 1](https://archive.today/5mLAv), [page 2](https://archive.today/fbVyJ))


- Mikhail Arkadyevich Shifman: _Vadim Knizhnik_, 2012.
    - URL: [https://traveller2.livejournal.com/275323.html](https://traveller2.livejournal.com/275323.html?noscroll)
      (archived [here](https://archive.today/0mTb6))

- Mikhail Arkadyevich Shifman: _More on Vadim Knizhnik_, 2017.
    - URL: [https://traveller2.dreamwidth.org/663683.html](https://traveller2.dreamwidth.org/663683.html?noscroll)
      (archived [here](https://web.archive.org/web/20250707230058/https://traveller2.dreamwidth.org/663683.html) and [here](https://archive.today/k63xA))

- Mikhail Arkadyevich Shifman: _It is time to say good bye. Variations on the theme_, 2013.
    - URL: [https://traveller2.livejournal.com/356617.html](https://traveller2.livejournal.com/356617.html?noscroll)
      (archived [here](https://archive.today/yrwVP))

- experiment8or: _Participating in a flash mob: career guidance_, 2013.
    - URL: [https://experiment8or.livejournal.com/172565.html](https://experiment8or.livejournal.com/172565.html?noscroll)
      (archived [here](https://archive.today/iHM20))

- medovoy: _How it was done in Dolgoprudny_, 2013.
    - URL: [https://medovoy.livejournal.com/713.html](https://medovoy.livejournal.com/713.html?noscroll)
      (archived [here](https://archive.today/rZx7Q))

- Alexander Alexandrovich Kirillov Jr.: _Lupanov_, 2006.
    - URL: [https://aa-kir.livejournal.com/21176.html](https://aa-kir.livejournal.com/21176.html?noscroll)
      (archived [here](https://archive.today/QLyUr))

- taki_net: _"The best Soviet education in the world"_, 2011.
    - URL: [https://taki-net.livejournal.com/1154824.html](https://taki-net.livejournal.com/1154824.html?noscroll)
      (archived [here](https://archive.today/l9NLK))

- Anton Nossik: _Startup: thank you Joseph Goebbels for our happy childhood_, 2014.
    - URL: [https://dolboeb.livejournal.com/2663695.html](https://dolboeb.livejournal.com/2663695.html?noscroll)
      (archive: [page 1](https://archive.today/3DMM8),
                [page 2](https://archive.today/tzQgQ),
                [page 3](https://archive.today/9CrIb),
                [page 4](https://archive.today/YS6wT),
                [page 5](https://archive.today/cKqKg),
                [page 6](https://archive.today/3NGv0),
                [page 7](https://archive.today/LsZbv),
                [page 8](https://archive.today/oXDOe),
                [page 9](https://archive.today/QGieY))

- yigal_s: _licking old wounds_, 2006.
    - URL: [https://yigal-s.livejournal.com/282328.html](https://yigal-s.livejournal.com/282328.html?noscroll)
      (archived [here](https://archive.today/TiYWp))

- shkrobius: _Anti-antisemite_, 2012.
    - URL: [https://shkrobius.livejournal.com/389866.html](https://shkrobius.livejournal.com/389866.html?noscroll)
      (archived [here](https://archive.today/TgK1R))

- sumlenny: _Read this detailed explanation of why the USSR collapsed_, 2012.
    - URL: [https://sumlenny.livejournal.com/1360919.html](https://web.archive.org/web/20121219070619/https://sumlenny.livejournal.com/1360919.html)


- Discussion about _Soviet College Admission — My Dad's Story (1970)_ by Ilya Volodarsky.
    - URL: [https://news.ycombinator.com/item?id=5340553](https://news.ycombinator.com/item?id=5340553)
      (archived [here](https://web.archive.org/web/20201011224757/https://news.ycombinator.com/item?id=5340553))

- Discussion about _The Fifth problem: math and anti-Semitism in the Soviet Union_ (excerpt from _Love and Math_) by Edward Frenkel.
    - URL: [https://news.ycombinator.com/item?id=4752047](https://news.ycombinator.com/item?id=4752047)
      (archived [here](https://web.archive.org/web/20171106013949/https://news.ycombinator.com/item?id=4752047))

- Another discussion about _The Fifth problem: math and anti-Semitism in the Soviet Union_ (excerpt from _Love and Math_) by Edward Frenkel.
    - URL: [https://news.ycombinator.com/item?id=6999846](https://news.ycombinator.com/item?id=6999846)
      (archived [here](https://web.archive.org/web/20260306193655/https://news.ycombinator.com/item?id=6999846))

- Discussion about _Jewish problems_ by Tanya Khovanova.
    - URL: [https://news.ycombinator.com/item?id=4759642](https://news.ycombinator.com/item?id=4759642)
      (archived [here](https://web.archive.org/web/20171110234423/https://news.ycombinator.com/item?id=4759642))


- _Was there discrimination against Jewish people at the entrance exams to the most prestigious universities in the USSR?_, 2013.
    - URL: [https://history.stackexchange.com/questions/8774/](https://history.stackexchange.com/questions/8774/was-there-discrimination-against-jewish-people-at-the-entrance-exams-to-the-most)
      (archived [here](https://web.archive.org/web/20220407183721/https://history.stackexchange.com/questions/8774/was-there-discrimination-against-jewish-people-at-the-entrance-exams-to-the-most))
