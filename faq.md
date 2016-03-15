# F.A.Q.

This page gathers common questions and answers concerning GitBook.com.

##### Does GitBook supports RTL/bi-directional text ?

The [format](https://toolchain.gitbook.com) used by GitBook supports right to left, and bi-directional writing. To enable it, you either need to specify a language (ex: `ar`), or force GitBook to use RTL in your `book.json`:

``` json
{
    "language": "ar",
    "direction": "rtl"
}
```

With version 3.0 of GitBook, it's automatically detected according to the content.
_Note that, while the output book will indeed respect RTL, the Editor doesn't support RTL writing yet_.

##### My book is not being updated / I can't see any builds

If you linked your book to a GitHub repository but editing content doesn't trigger any build,
verify that the webhook has been correctly added to your GitHub repository (in your GitHub repository's settings -> Webhook). If the webhook is not present or invalid, add it back from your book's settings.

If you **changed the book's name or its owner's name** (it happens when transferring your book to a new owner), the webhook is now invalid, you need to add it back.


##### Duplicate account

When you register with a Social (Facebook, Twitter, GitHub or Google), then register again using the form, it creates two distinct accounts (one associated with your email, and another with your Social Account).

You need to remove one of these account, to do so:

1. Logout from the account associated with your email
2. Login back using the social account
3. Delete this account at [www.gitbook.com/settings](https://www.gitbook.com/settings)
4. Login back using your email
5. Associate the Social Account to your email account at [www.gitbook.com/settings](https://www.gitbook.com/settings)

##### An user is already associated to this GitHub account

See [Duplicate account](#duplicate-account).
