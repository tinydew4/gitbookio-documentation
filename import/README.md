# Importing documents

Importing an existing document to GitBook is now easy.

You already have access to this feature either on the Import tab when creating a new book or on the welcome page of an empty book.

### Accepted formats

| Type | Extension |
| ---- | --------- |
| Microsoft Word Document | .docx |
| DocBook v5.x | .xml |
| HTML file | .html |

To use this feature as its most, we recommend using:
* Microsoft Word 2007+ documents
* DocBook v5.x documents

If you have existing DocBook documents in version 4, consider [converting it automatically](http://doccookbook.sourceforge.net/html/en/dbc.structure.db4-to-db5.html) to version 5 for optimized compatibility.

### Conversion

The import feature uses the [gitbook-convert](https://github.com/GitbookIO/gitbook-convert) node module. This module is in charge of every aspect of the conversion of the original document to markdown files, along with the creation of the `SUMMARY.md`.

[gitbook-convert](https://github.com/GitbookIO/gitbook-convert) is smart enough to divide a big document into chapters and sub-chapters, based on the document's structure. Thus, each first-level header of the original document will be converted to a chapter. If a chapter contains second-level headers, a folder instead of a new file is created for this chapter. This folder will contain each sub-chapters.

In a chapter's folder, a `README.md` file containing the chapter preface is created. The whole content before the first second-level header is considered to be a chapter preface. The same rule apply for the whole content before the first first-level header which is used as the book's preface.

For `.docx` documents, [gitbook-convert](https://github.com/GitbookIO/gitbook-convert) will also export all included images into the `assets/` folder.

### Troubleshooting

Your feedback will be precious to improve [gitbook-convert](https://github.com/GitbookIO/gitbook-convert) based on the most common use-cases.

If you ever need more flexibility, consider using [gitbook-convert](https://github.com/GitbookIO/gitbook-convert) locally, create a repository and import it using Git or GitHub.