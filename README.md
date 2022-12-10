# Thesis template, RUET, CSE

This template is a modification of [mdminhazulhaque/ruet-thesis-template-latex](https://github.com/mdminhazulhaque/ruet-thesis-template-latex). The changes have been made according to the requirements of the department as of 2022. Additional changes are:

- Usage of `subfiles` package has been removed. Instead, `\include{}` and `\input{}` commands has been used. Why? note sure which one is better, but `subfiles` was bothering me.
- The logo of the front page has been changed. Thanks to [Muntashir Al-Islam](https://github.com/MuntashirAkon) for providing the image.
- The content page format has been adjusted according to the requirements. Thanks to [Fuad Al Abir](https://github.com/fuad021).
- `listings` package has been replaced with `minted` package for code listing.
- `biblatex` package has been added for referencing.

## Usage

Download this repository as zip and open it as a project in [Overleaf](https://www.overleaf.com), or copy the project directly from [Overleaf](https://www.overleaf.com/read/fwzgfjndfhsc). You can also clone this repository and run it on your local machine, if you have all the required packages, but I recommend using Overleaf. It will be a lot easier.

If you want to change anything in the template, or need to add more packages, edit the `packages.sty` file.

## Equations
Use `align` environment for your numbered equations. You can reference them, if you label the line you want to refer to. You can use `\equref{}` for this purpose, but I prefer `\autoref{}` command from the `hyperref` package, which you can use to refer tables and images as well. Try it and see the difference.

For a multi-line equation, you can omit numbering for specific lines using `\nonumber` command.
```tex
\begin{align}
E_0 &= mc^2 \label{eq:example}\\
&= \text{your text} \nonumber
\end{align}
```

For unnumbered equations, or any other unnumbered environments, add a `*` at the end of the command, but before the curly braces, *e.g.* `\caption*{caption}`. However, you cannot refer to unnumbered environments. There may be a way around this, but I am not familiar with it.

## Referencing

The `biblatex` package is very handy for referencing in different styles. The requirement in CSE department is to use IEEE style formatting, so that's the one that has been set up. The commands that you will need at most, are:

- `\cite{}`
- `\citeauthor*{}`
- `\citetitle{}`

To keep record of papers you read, use Mendeley. They have a browser extension, which you can use to add papers to your library while browsing for papers online. Later, you can select specific papers in the library, and download bibtex for those papers. Mendeley also saves the pdf of the paper in the library, if it can find the pdf on that site.

If you cannot find bibtex for any document, or you want cite a website, try [ZoteroBib](https://zbib.org/). Add the document and/or website, and download the bibtex from the dropdown list from the bottom. The `abstract` field is not required, so you can remove it. Make sure to use escape sequence for special characters, or you will get compilation error.

## Code listing

If you need to add any source code to your document, use `minted` *e.g.*
```tex
\begin{minted}{c++}
#include <iostream>
using namesapce std;
int main(void){
    cout << "Hello World" << endl;
    return 0;
}
\end{minted}
```

The second parameter is the source language of the code you are listing.

See more examples and languages supported by `minted`: [Code Highlighting with minted - Overleaf](https://www.overleaf.com/learn/latex/Code_Highlighting_with_minted).

## Recommendation

Read documentations for better understanding. [CTAN](https://ctan.org/) is the tex archive for packages and their documentation. [Overleaf](https://www.overleaf.com/learn) also covers lots of tutorials with good explanation and examples.

To typeset your document in latex, always use [Overleaf](https://www.overleaf.com).