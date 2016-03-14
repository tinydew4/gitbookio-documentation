# Creating or importing books

When creating books, your are prompted with several alternatives:

- Create from a _Basic_ book template
- Create from a _Science_ book template, already configured to use `mathjax`
- Import a book from GitHub, any git repository, or documents.

## Importing from an existing book on GitHub

When creating a new book, the `GitHub` tab let you choose one of your GitHub repository to import.
If you haven't integrated our account with GitHub, see the [GitHub Integration section](github.md)).
After creation, your book will show in GitBook, already linked to the GitHub sources, with a webhook configured to build the book on update.

## Importing from documents

Importing an existing document to GitBook is easy. Upload it when creating a book using the `Import` tab.

### Accepted formats

Here are the formats available for importation:

| Type | Extension |
| ---- | --------- |
| Microsoft Word Document | `.docx` |
| DocBook v5.x | `.xml` |
| HTML file | `.html` |

For better results, we recommend using:
* Microsoft Word 2007+ documents
* DocBook v5.x documents

For DocBook v4 documents, consider [converting them automatically to version 5](http://doccookbook.sourceforge.net/html/en/dbc.structure.db4-to-db5.html) for improved compatibility.

### Conversion

The import feature uses the [gitbook-convert](https://github.com/GitbookIO/gitbook-convert) CLI utility. This module converts the original document to markdown files, and generates a suitable `SUMMARY.md`.

[gitbook-convert](https://github.com/GitbookIO/gitbook-convert) infer a book structure from your document's structure, based on header levels. Top-level headers become chapters. Chapters are folders with a `README.md` as preface, and sub-chapters for every second-level headers. If no second-level headers are present, the chapter will consist of a single file instead of a folder.

Here is an example from a source document:

    This will be the book's preface (or README.md).
    * Section 1
        This will be the preface of chapter 1.
        * Subsection 1.1
            ...
            * Subsubsection 1.1.1
                ...
            * Subsubsection 1.1.2
                ...
        * Subsection 1.2

    * Section 2
        This will just be the content of chapter 2.

... to an output book structure:

    .
    ├── README.md
    ├── SUMMARY.md
    ├── chapter-1
    │   ├── README.md
    │   ├── subchapter-1-1.md
    │   └── subchapter-1-2.md
    └── chapter-2.md


For `.docx` documents, [gitbook-convert](https://github.com/GitbookIO/gitbook-convert) will also export all included images into an `assets/` folder.

If you ever need more flexibility, consider using [gitbook-convert](https://github.com/GitbookIO/gitbook-convert) locally, create a repository and import it using Git or GitHub.

### Troubleshooting

We're always happy to help out with your books or any other questions you might have. You can ask a question or signal an issue on the following form at [github.com/GitbookIO/gitbook-convert](https://github.com/GitbookIO/gitbook-convert/issues).


