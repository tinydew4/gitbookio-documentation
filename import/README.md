# Importing documents

Importing an existing document to GitBook is now easy. You have already access to this feature either on the **new book** form's Import tab or on the welcome page of an empty book.

### Accepted formats

| Type | Extension |
| ---- | --------- |
| Microsoft Word Document | .docx |
| DocBook v5.x | .xml |
| HyperText Markup Language | .html |

To use this feature as its most, we recommend using:
* Microsoft Word 2007+ documents
* DocBook v5.x documents

If you have existing DocBook documents in version 4, consider [converting it automatically](http://doccookbook.sourceforge.net/html/en/dbc.structure.db4-to-db5.html) to version 5 before use for optimized compatibility.

### Conversion

The import feature uses the [gitbook-convert](https://github.com/GitbookIO/gitbook-convert) node module. This module is in charge of every aspect of the conversion of the original document to markdown files. [gitbook-convert](https://github.com/GitbookIO/gitbook-convert) is smart enough to divide a big document into chapters and sub-chapters, based on the document's structure.

Thus, each first-level header of the original document will be converted to a chapter. If a chapter contains second-level headers, a folder is created for this chapter instead of a file. This folder will contain each sub-chapters. A `README.md` file is created along, containing the chapter preface. That is, the whole content before the first second-level header.

### Troubleshooting

Your feedback will be precious to improve [gitbook-convert](https://github.com/GitbookIO/gitbook-convert) based on the most common use-cases.

If you ever need more flexibility, consider using [gitbook-convert](https://github.com/GitbookIO/gitbook-convert) locally, create a repository and import it using GitHub or the **new book** Git tab.