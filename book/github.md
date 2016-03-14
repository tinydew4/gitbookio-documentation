# GitHub Integration

GitBook integrates perfectly with [GitHub](https://github.com) as a host for the source of your book.

## Setting up permissions

To integrate your book with GitHub, you need to authorize GitBook to access your GitHub account to some extent. From your [account's settings](https://www.gitbook.com/settings), connect your GitHub account and choose what you will allow:

- **Default permissions**: Allows you to log in with GitHub to your GitBook account.
- **Access to public repositories**: Allows editing books on your public GitHub repositories from the GitBook Web editor.
- **Access to private repositories**: Same as above, but for private repositories too.
- **Access to webhook**: Allows GitBook to create webhooks on your book repositories to trigger builds automatically.

## Hosting you book on GitHub

You can configure GitBook to use a GitHub repository to host a book. This is done automatically if you [imported a book from GitHub](create#importing-from-an-existing-book-on-github).
Otherwise you need to:

1. Open the GitHub section in your book settings
2. Enter your repository id (such as: `YourGitHubUserName/RepoName`)
3. Save your settings
4. (Optionnal) Click on **Export to GitHub** to transfer your book's content, if any, over GitHub

Now the Editor will make changes directly to GitHub. You might want to setup a [webhook](webhooks) to automatically trigger builds.

{% hint style="danger" %}
The GitHub repository will become the main repository. You should no longer use the GitBook repository afterward.
The sync is unidirectional, which means GitBook will watch changes made on GitHub, but it will never write back to your GitHub repository.
{% endhint %}
