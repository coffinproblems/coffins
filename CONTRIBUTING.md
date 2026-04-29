# Contributing

> [!NOTE]
> When opening a ticket or leaving a comment,
> make sure to hide in an expandable block of text any information that is related to a solution to any of the problems,
> or that could otherwise give hints towards a solution.
> 
> This is to avoid spoiling solutions to people who wish to solve the problems without external help.


## Submit new coffin problems

If you know of any potential coffin problem not already included in this project,
please submit it by opening an issue with [this issue template](https://github.com/coffinproblems/coffins/issues/new?template=new_coffin_problem.yml), or by contacting the project;
in your submission, include any and all related information, such as, if possible:
- the formulation of the problem as it was originally administered, or as close as possible to it
  (including its formulation in the original language, if known);
- the context in which the problem was administered;
- the source of your information;
- who was given the problem, when, where, by whom, and, possibly, what is their story.


## Contacting others

To make this project as exhaustive as possible,
contacting people that have first-hand experiences would be of great value.
- If you have first-hand experience or knowledge, please get in contact; see [contact information](README.md/#contact).
- If you know some people that may have first-hand experience or knowledge,
  consider reaching out to them to ask whether they are willing to get in contact with this project.
- If you find publicly available contact information for someone that you think could possess helpful information,
  you can communicate it to the project maintainer.


## Submit new references

If you know of any resource not already mentioned in this project,
even if it doesn't contain any additional information,
and even if it is only tangentially related,
please submit it by opening an issue with [this issue template](https://github.com/coffinproblems/coffins/issues/new?template=new_reference.yml), or by contacting the project.
Include with your submission any related information, such as
authors, publishing date, and a citation to the source.

For example, if you are able to provide scans of documents that are not otherwise available online,
(or that are only available in poor quality), please do so.

Even if you only know of the potential existence of other resources, without having access to them,
please share what you know about that, with as much information as you are able to include.

If you know of alternate versions of some of the resources documented in this project,
even if they do not appear to contain extra information,
submit them by opening an issue with [this issue template](https://github.com/coffinproblems/coffins/issues/new?template=alt_reference.yml), or by contacting the project.
Please make sure to mention the source where the document comes from.


## Digitisation of resources

Some of the historical sources for this project are available only in the form of scans of handwritten or typewritten documents,
often with poor legibility and poor accessibility.
Help is needed to digitise them, make them more accessible, and validate the results.

In many cases, the documents are written in Russian language:
for these, help is also needed to provide accurate translations,
and to validate the results.

This work is carried out in the dedicated repository [`resources`](https://github.com/coffinproblems/resources); see there for details.


## Sift through sources

The references, listed [here](README.md/#references), may still contain useful information that was missed,
especially among the non-English ones.
Thus, any help in thoroughly reading each source is welcomed.  
Additionally, older, archived, versions of each reference should be checked as well.

Particular examples of resources that need to be carefully and thoroughly read are:
- the English Wikipedia page [https://en.wikipedia.org/wiki/Antisemitism_in_Soviet_mathematics](https://en.wikipedia.org/wiki/Antisemitism_in_Soviet_mathematics),
  and each of the references it cites;
- the Russian Wikipedia page [https://ru.wikipedia.org/wiki/Антисемитизм_в_советской_математике](https://ru.wikipedia.org/wiki/%D0%90%D0%BD%D1%82%D0%B8%D1%81%D0%B5%D0%BC%D0%B8%D1%82%D0%B8%D0%B7%D0%BC_%D0%B2_%D1%81%D0%BE%D0%B2%D0%B5%D1%82%D1%81%D0%BA%D0%BE%D0%B9_%D0%BC%D0%B0%D1%82%D0%B5%D0%BC%D0%B0%D1%82%D0%B8%D0%BA%D0%B5),
  and in particular the many references that it cites;
- _Through the prizm of time — Angles of reflection_,Epilogue to “Comrade Einstein”, by Mikhail Shifman:
  [this version](https://www-users.cse.umn.edu/~shifman/Epilogue_12_28_2016.pdf),
  [this updated version](https://www.lirmm.fr/~ashen/senderov/shifman2020.pdf), and
  [this other updated version](https://www.academia.edu/101548394/Epilogue_May_6_2023_To_You_Just_Failed_Your_Math_Test_Comrade_Einstein_World_Scientific_Singapore_2005_);
- the resources collected [here](https://www.lirmm.fr/~ashen/senderov/);
- the user discussions and posts, mainly on LiveJournal, listed [here](README.md/#user-discussions).

For the purposes of this project, "useful information" refers mainly to:
  - a new coffin problem;
  - a new reference for a (non-new) coffin problem;
  - a new source;
  - names of people that could have useful information (recursively).

To report the results of the effort, open an issue for each new piece of information uncovered, using the corresponding issue template;
also open a discussion to mark the source as done,
(even when the source did not end up containing new information).

Priority should be given to the sources that have the fewest reports,
but working on those that have already been worked on by others is also needed, so as to have multiple confirmations.


## Compare different versions of the same document

Some of the documents cited as references exist in multiple versions,
and, in some cases, there are differences between the various versions of the same resource
(for example, some of the documents that have both an English and a Russian version available
have differences in the statements of the problems, or one version contains more coffin problems than the other).

Help is needed to compare the various versions of the documents, to check for any meaningful difference.
Some of the comparisons to be performed are the following:
  - between archived versions of the references;
  - between English and Russian versions of the same document;
  - between the different versions of _Through the prizm of time — Angles of reflection_, Epilogue to “Comrade Einstein” by Mikhail Shifman;
  - between the English and Russian versions of _Entrance examinations to the Mekh-mat_ by Alexander Shen, and between the multiple PDFs available;
  - between the articles contained in _You failed your math test, Comrade Einstein_ by Mikhail Shifman and the standalone versions of the same articles;


## Report errors

Errors, typos, inaccuracies, etc. can be reported by opening an issue with [this issue template](https://github.com/coffinproblems/coffins/issues/new?template=error_report.yml).



## Report code issues

Bugs in the source code can be reported via [this issue template](https://github.com/coffinproblems/coffins/issues/new?template=bug_report.yml).


## Suggest improvements

Suggestions for improvements in the wording, phrasing, grammar, etc.
can be made by opening an issue with [this issue template](https://github.com/coffinproblems/coffins/issues/new?template=proposal.yml), or by opening a pull request.


## Code contributions

Suggestions for improvements in the LaTeX source code or in the project structure
can be made by opening an issue or a pull request.

Particularly, help is needed for the following:
- making the MathML via "Structured Elements" (`mathml-SE`) work;
- making EPUB generation work correctly for MathML, SVG and PNG Math rendering.


## Submit solutions

If you know of solutions to some problems that are different from the already documented ones,
you can submit them via [this issue template](https://github.com/coffinproblems/coffins/issues/new?template=new_solution.yml) or by opening a pull request.

> [!NOTE]
> The maintainer of the project wishes to solve each problem independently,
> so submissions of solutions may remain unread for some time.

> [!NOTE]
> To avoid spoiling solutions to people who wish to solve the problems without external help,
> make sure to hide the solution in an hidden/expandable block of text when submitting it.



# Documentation

Here, the project structure is documented.

The `src` directory is where the LaTeX source code is contained:
- the `latexmkrc` file contains the configuration for generating the PDF; it sets `lualatex` as the default compiler
- the `main.tex` file is the root file
- the `pdfinfo.tex` file contains the settings for generating a tagged PDF or PDF/A, and metadata information
- the `references` directory contains the `.bib` files for the sources of the problems and for additional references
- the `preamble` directory contains the document preamble:
    - `preamble.tex` is the root file
    - `references.tex` sets the settings for the references
    - `typography.tex` sets the font and typographical settings
    - `metadata.tex` is for setting up hyperlinks, bookmarks, and some metadata
    - `custom_sections.tex` contains definitions of sectioning commands and associated counters
    - the directory `maths` is for loading packages and definitions related to typesetting of mathematical content:
        - `maths.tex` is the root file; it loads the main Mathematics packages
        - `scalemath.tex` contains a placeholder implementation for commands that typeset mathematical expressions in an intermediate size;
          in particular, it defines `\mfrac` and `\mbinom` for medium-sized fractions and binomial coefficients
        - `delimiters.tex` contains definitions of delimiters using `\DeclarePairedDelimiter` provided by `mathtools`;
          it also loads the `mleftright` package for fixing the spacing between operators and delimiters
        - `operators.tex` contains definitions of operators via `\DeclareMathOperator`
- the `commands` directory contains the logic for inputting the problems and solutions in the document:
    - `flags.tex` manages the compilation options, generating appropriate booleans
    - `insertions.tex` defines the commands for adding an individual problem and its solutions to the document
    - `include_problems.tex` defines the command for triggering the inclusion of the problems in the document
- the `sections` directory contains the `.tex` files for the introduction and for the problems, with one file for the original problems and one for the generalised ones
- the `problems` directory contains the problems and solutions
    - each of the first level subdirectories represents one of the categories in which the problems have been divided;
        - inside, there is a file `sec.tex` which contains the name of the category the command that creates the corresponding section
        - there is also a file named `description.tex` which contains a brief description of the category of problems; currently, this is not incuded in the document
        - the problems are stored in directories named `problem_1`, `problem_2`, etc.;
            - inside, the `reference.tex` file cites the sources in which that problem was documented
            - the directory `original` is for the original problem, and `generalised`, if present, is for the generalisation;
                - the statement of the problem is contained in the file `statement.tex`
                - the solution is in the file `solution.tex`, or, if there are multiple solutions, the corresponding files are named `solution_1.tex`, `solution_2.tex`, etc.
