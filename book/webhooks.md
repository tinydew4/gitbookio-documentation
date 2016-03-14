# Webhooks

Webhooks notify GitBook when your the GitHub repository hosting your book changes.

If your book is not updated on GitBook, it is probably because of an incorrect webhook configuration. You can check the state of your webhook in your GitHub repository's settings.

## Setting up a webhook

Using webhooks requires to [link your GitHub account](github.md) with the correct permission for webhooks, and to [link your book to a GitHub repository](github.md#hosting-you-book-on-github). Then to create a webhook, just click on **Add a deployment webhook** in your book's settings.

Now any commit on GitHub will trigger builds on GitBook.
