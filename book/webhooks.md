# Webhooks

Webhooks notify GitBook when your the GitHub repository hosting your book changes.

If your book is not updated on GitBook, it is probably because of an incorrect webhook configuration. You can check the state of your webhook in your GitHub repository's settings.

## Setting up a webhook

Using webhooks requires to [link your GitHub account](github) and [link your book to a GitHub repository](github#hosting-you-book-on-github). Then to create a webhook, just click on **Add a deployment webhook** in your book's settings.

You can now edit your GitHub repository from the web editor (if you have authorized the correct permissions), and your commits on GitHub will trigger builds on GitBook.
