Strikethrough MVP

The objective of the MVP is to demonstrate a citation fixer with the bare minimum functionality. We should be able to
Take in a docx file as input
Identify some “citations” – we can start by just identifying random substrings of paragraphs
Modify the “citations” – we can change each character to something very basic like “aaaaa”
Save the modified citations into a word document.

We will achieve this by doing the following:

There exists a library called python-docx that can be used to work with docx files using Python. We can create a class CitationFixer that uses this python-docx library and has the following attributes / functions
Attributes (perhaps the paragraphs and footnotes can be stored implicitly, via a docx.Document)
Paragraphs
Footnotes (we don't have functionality for this yet)
Citations
Functions
read_file(path)
get_citations()
fix_citations()
save_document(path)

Determining how to represent the citations in the class is open-ended. We can include footnote citations, although that will require a bit of research / engineering, since python-docx doesn’t directly have support for extracting footnotes. Our citations can be random substrings of paragraphs. They can be encoded by (paragraph number, start index, (exclusive) end index). For now, we can just do <= 1 random substring per paragraph.

As seen in docx2python test.ipynb, we can actually view footnotes (although they may not be in order)
