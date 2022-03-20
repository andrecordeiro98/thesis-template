# Thesis Template

This is a LaTeX thesis template compliant with the guidelines of Instituto Superior Técnico, University of Lisbon, as of 2022 (see the included file `guia-de-preparacao-da-dissertacao-1516.pdf`).

## Acknowledgements

Pedro Cosme and Diogo Ribeiro are responsible for the basis of this template, and the author is indebted to their work. A different version of this template is available [here](https://github.com/diogoribeiro98/IST_Master_Thesis_Template_V2).

Thanks to Tomás Cabrito for providing a placeholder image.

## How to use this template

A thorough description of the file structure and the commands used to define the typesetting can be found in the included file `ThesisTemplate-Guide.pdf`. 

### Online solution: Overleaf

Simply upload these files to an Overleaf project and hit the _Compile_ button. If you make changes to the _List of Symbols_ or _List of Abbreviations_, the auxiliary files must be deleted before recompiling.

### Local solution: TeXstudio

Download these files and open them with TeXstudio. To effect any changes to the _List of Abbreviations_ or _List of Symbols_ (or indeed to build them for the first time), you must first build the main file, then build the auxiliary files, and then _rebuild_ the main file.

There is a caveat regarding the _List of Symbols_ (a.k.a. _Nomenclature_, _Index_), where you must edit the compile command. Under `Options > Configure TeXstudio`, in the `Commands` tab, edit the `Makeindex` command to be
```
makeindex %.nlo -s nomencl.ist -o %.nls
```
noting that you can also define a hotkey for this command in the `Shortcuts` tab.

After this setup, the procedure is as follows,

- Build the main file (press `F5` or `Tools > Build & View`);
- Build the auxiliary files (use `Tools > Glossary` and `Tools > Index`);
- Build the main file _again_ (`F5`).

As long as you do not make any changes to the _List of Abbreviations_ or _List of Symbols_, you won't need to repeat this procedure to update the `.acr` and `.nls` auxiliary files, respectively.
