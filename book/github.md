# GitHub Integration

GitBook integrates perfectly with [GitHub](https://github.com) as a host for the source of your book. When configured correctly, this has several effects:

- The Editor will make changes directly to the GitHub repository
- GitBook will watch for update on GitHub and trigger builds accordingly

{% hint style="info" %}
You should not use the GitBook repository for a book hosted on GitHub.
The GitHub repository becomes the main repository, which means GitBook will watch changes and update from GitHub, but it will never write back to your GitHub repository.
{% endhint %}

Integrating with GitHub is done in 3 steps:

1. Setting up [permissions](#setting-up-permissions)
2. [Linking your book](#hosting-your-book-on-github) to a GitHub repository
3. Setting up [webhooks](#webhooks)

## Setting up permissions

To integrate your book with GitHub, you need to authorize GitBook to access your GitHub account to some extent. From your [account's settings](https://www.gitbook.com/settings), connect your GitHub account and choose what you will allow:

- **Default permissions**: Allows you to authenticate with GitHub on GitBook.
- **Access to public repositories**: Allows editing books on your public GitHub repositories from the GitBook Web editor.
- **Access to private repositories**: Same as above, but for private repositories too.
- **Access to webhook**: Allows GitBook to create webhooks on your book repositories to trigger builds automatically.

## Hosting your book on GitHub

### Importing from an existing GitHub repository

When creating a new book, the `GitHub` tab let you choose one of your GitHub repository to import.
This requires to configure the correct [GitHub permissions](#setting-up-permissions)).
After creation, your book will show in GitBook, already linked to the GitHub sources, with a webhook configured to build the book on update.

### Transferring content to GitHub

If you started writing your book on GitBook and you now want to host its source on GitHub, don't worry, it's easy. To do so, you can either use the GitHub import tool, or operate from the command line.

##### Using the GitHub Import Tool

1. Use the **Import Tool** from GitHub:  [import.github.com/new](https://import.github.com/new)
2. Enter your GitBook git url, for example: `https://git.gitbook.com/MyName/MyBook.git` (this url can be found in your book settings).
3. Enter a name for your GitHub repository.
4. Enter your GitBook credentials (you can use your API token instead of your password) when prompted.
5. Done!

##### Using the command line

After creating a repository on GitHub:

{% hint style="danger" %}
This operation will overwrite the content of the GitHub repository
{% endhint %}

```
# Clone your GitBook repository (you'll need to enter your username and password)
$ git clone https://git.gitbook.com/MyName/MyBook.git ./mybook

# Enter the cloned book
cd ./mybook

# Push it to Github
$ git push https://github.com/username/repo.git master --force
```

## Webhooks

Webhooks notify GitBook when your the GitHub repository hosting your book changes.

If your book is not updated on GitBook, it is probably because of an incorrect webhook configuration. You can check the state of your webhook in your GitHub repository's settings.

To create a webhook, go to your book's settings and click on **Add a deployment webhook**.
