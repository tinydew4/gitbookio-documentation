# Access & Permissions

While you can grant read/write access to collaborators on a personal book, members of an organization can have more granular access permissions for the organization's books.

This article also gives an overview

### Personnal Books

A book owned by a user account has two permission levels: the book owner and collaborators.

{% hint style="info" %}
Only the owner can delete or rename the book.
{% endhint %}

Collaborators can have granular permissions: Read-only access, Read & Write, Management.

### Organization Books

Permissions from [Organizations](../account/orgs.md) are applied to all books, except in the case where the member is also specified as a collaborator of book with a different set of permissions: Permissions from the book are overwritting permissions from the organization.

{% hint style="tip" %}
To disable write permission of an organization member on a specific book: add it as a collaborator of the book without the Write permission enabled.
{% endhint %}

### Collaborator Permissions

Permissions for collaborators on a book, or members of an organization have 3 levels of granularity:

| Type | Read the online version | Download PDF | Edit Content | Edit Settings |
| ---- | :---------------------: | :----------: | :----------: | :-----------: |
| **Read** |  ✅ | ✅ | 🚫 | 🚫 |
| **Write** |  ✅ | ✅ | ✅ | 🚫 |
| **Manage** |  ✅ | ✅ | ✅ | ✅ |


### Access Keys {#access-keys}

Giving read-only access to private books using collaborators requires to manually invite GitBook.com users as collaborators.

**Access Keys** are a better solution to give read-only access to a large number of people without requiring a GitBook.com account.

An access key is a unique URL, anyone with this URL can read and download the book. You can create a large number of access keys from the dashboard of your book or using the [API](http://developer.gitbook.com/books/keys/).

{% hint style="danger" %}
Anyone with the URL can access the content, an access key can be disabled if unintentionally shared.
{% endhint %}

