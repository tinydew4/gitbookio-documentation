# Update your book using GIT

If you want to update your book from the command line, you can use [GIT](http://git-scm.com) to push your content:

### GIT Url

Each book is associated with a Git HTTPS url. The format for the Git url is:

```
https://git.gitbook.com/{{UserName}}/{{Book}}.git
```

{% hint style="info" %}
The SSH protocol is not yet supported on the GitBook's git server
{% endhint %}

### Authentication

The git server is using your basic GitBook login to authenticate you. When prompted enter your GitBook username and your password (you can also use your API token).

### Saving your credentials

To avoid having to enter your password on each new push, you can add your GitBook credentials to your `~/.netrc` file. Create or append to an existing `~/.netrc` file something like below:

```
machine git.gitbook.com
  login USERNAME-or-EMAIL
  password API-TOKEN-or-PASSWORD
```

We recommend using an **API TOKEN** for security reasons, you can create one at [gitbook.com/settings/tokens](https://www.gitbook.com/settings/tokens)

### Create a new repository on the command line

{% hint style="info" %}
Since GitBook's repositories are already initialized with an example, you have to "push force" to replace the existing content.
{% endhint %}

```
touch README.md SUMMARY.md
git init
git add README.md SUMMARY.md
git commit -m "first commit"
git remote add gitbook https://git.gitbook.com/{{UserName}}/{{Book}}.git
git push -u gitbook master -f
```

### Push an existing repository

```
git remote add gitbook https://git.gitbook.com/{{UserName}}/{{Book}}.git
git push -u gitbook master -f
```