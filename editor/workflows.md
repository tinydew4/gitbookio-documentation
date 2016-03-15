# Workflows

You can always use GitBook and the Editor as any other editor. But GitBook uses [git](https://www.git-scm.com/) internally, and it comes with great features such as the **concept of branches**. The good news is branches are easy to work with, and you don't need to know git to use them. This chapter explains the concept of branches, and how you can use them in effective workflows.

## Working with branches

### The concept

A branch is a chronological history of the state of your book. All your writing in GitBook happens on branches. Even if you have not used branches so far, you have actually been writing on a single branch from the beginning. This branch is called `master` and is the default branch when creating a book. If you have been working on `master` from the beginning, `master` tracks, as a result, the complete history of the versions of your book.

```
A, B, C, D represent versions of your books resulting from successive changes.
Here, A is the book after creation. D is the last, current version.

A --> B --> C --> D [master]
```

#### Creating branches

Branches only become useful when you use more than one. At any time, you can create a new branch from another branch. This can be done from the Editor, in the branch menu (indicating the current branch `master`), by choosing **New Branch**, naming the new branch, and choosing the origin branch.

Suppose we created a branch from `master` that we called `experiment`, because we want to try experimental changes on our book. Doing so, we have just created a _copy_ of the `master` branch, so they both represent the same history:

```
A --- B --- C --- D [master, experiment]
```

Things become interesting once we start doing some changes from the `experiment` branch and we get to a version `E` of our book:

```
A --- B --- C --- D [master]
                   \
                    E [experiment]
```

`master` stayed at version `D`, while `experiment` progressed to version `E`. Meanwhile, we can continue some work on `master`, this will not affect our `experiment` branch:

```
A --- B --- C --- D --- F [master]
                   \
                    E [experiment]
```

Both branches have diverged. Now we can keep track of two different versions of our book at the same time and do experiment on our book, without messing up the `master` version!

#### Merging branches

Someday, we might be happy with how our `experiment` evolved and we will decide to merge it back into `master`.

```
A --- B --- C --- D --- F [master]
                   \
                    E --- G --- H [experiment]
```

This can be done from the Editor, in the branch menu, by choosing **Merge Branches**. You need to choose what branch to merge into what. Here, we would merge `experiment` into `master`. At this point, you may need to [resolve some conflicts](solving-conflicts.md). Otherwise, the changes you made on `experiment` are automatically incorporated into `master`:

```
A --- B --- C --- D --- F ------- I [master]
                   \             /
                    E --- G --- H [experiment]
```

You can now keep the `experiment` branch, or simply delete it from the branch menu:

```
A --- B --- C --- D --- F ------- I [master]
                   \             /
                    E --- G --- H
```

## Draft workflow

The GitBook Editor will trigger a new build, and publish the book each time you make changes to `master`. Changes can be saving a file, or editing the glossary or the summary. But, following the _Draft_ workflow, it is possible to work on a draft of your book then build it once it is finished only. To do so:

1. Create a new branch from the branches menu
   1. Enter a name that describes your modification, for example: "rework-chapter1"
   2. Select `master` as the origin branch
2. Make sure you are writing from your draft branch
3. Edit your draft as usual, until you are satisfied
4. Merge your draft branch into the `master` branch
5. This should trigger a build
6. You're done, you can delete your old draft branch

## Collaboration workflow

## Versionning
