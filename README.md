# Proofying Viewer
[![Github All Releases](https://img.shields.io/github/downloads/xr0038/proofying/total.svg?maxAge=2592000)](https://github.com/xr0038/proofying/) [![Python3](https://img.shields.io/badge/python-3-blue.svg)]() [![GPL3]( https://img.shields.io/badge/license-GPL3.0-blue.svg )](https://github.com/xr0038/proofying/blob/master/LICENSE)

A simple markdown viewer for displaying proofreading written in Python.

## Usage

~~~sh
# displaying a markdown document
proofying manuscript.md

# enabling MathJax
proofying -m manuscript_with_math.md
~~~


## Description
This program displays a markdown document using `misaka`, a fast markdown processing library, in a window. The document is immediately reloaded when the program detect updates in the document.

Building a code block by indent is disabled. Instead, a `fenced-code` option is enabled. The default extensions for `misaka` is summarized in the table below:


|Option|Description|
|---|---|
|`fenced-code`| enable fenced-code block using `~~~`|
|`disable-indented-code`| disable an indent code block|
|`underline`|_underline_ enabled by `_underline_`|
|`highlight`| |
|`quote`| enable a quotation using `>`|
|`math`| |
|`footnotes`| enable a footnote using `[^footnote]`|
|`tables`| this kind of table is available|
|`strikethrough`| ~~strike~~ enabled by `~~strike~~`|

Since `skip-html` and `escape` is enabled, any HTML tags are removed to prevent an attack using JavaScript.

MathJax is enabled by enabling an option `-m`. This downloads a code from http://cdn.mathjax.org. Thus, an Internet connection is required to convert mathematical expressions using MathJax. Note that this option allows MathJax to convert `$expression$` into a mathematical expression. A dollar sign should be used with particular care.


## Requirement
This program is depend on these packages:

- [PyQt4](https://pypi.python.org/pypi/PyQt4)
- [misaka](https://pypi.python.org/pypi/misaka)
- [argparse](https://pypi.python.org/pypi/argparse)

## License
This program is licensed by GNU General Public License. Detailed descriptions are available in [GPL3.0](https://github.com/xr0038/proofying/blob/master/LICENSE)
