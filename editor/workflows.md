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

```
o --- o ------------- o ----- o ------- o [master]
       \             /         \       /
        o --- o --- o [draft1]  o --- o [draft2]
```

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

```
                   [chapter-1]         [proofread-chapter-1]
        o --- o --- o   o ----- o ----- o
       /             \ /                 \
o --- o ------------- o -------- o ------ o [master]
       \                        /
        o ---- o ----- o ----- o
                               [chapter-2]
```

To collaborate on a book, it's more convenient if everyone can work independentely, while still being able to share changes when needed. The _Collaboration_ workflow is suited to collaboration, by keeping everyone's work on separate branches, and merging them in `master` as the book progresses.

The only principle is to create a branch every time you start working on a given task. A lot of things can be seen as a task:

- Writing a particular chapter or section
- Proofreading
- Reworking a part of the book
- Incorporating a [plugin](https://plugins.gitbook.com) and its functionality
- etc.

Once you are done with the task, people can easily see and review the work on your branch, and you can merge your work into `master`. If someone is working on another task in parallel, she will not be disrupted because she would be working on their own branch.

## Versionning


```
        [v1.0]            o --- o [v2.0]
       /                 /
o --- o --- o --- o --- o --- o --- o [master]

```

It is common for documentations to have a different version for every version of what they document. In this case, you can use branches to track versions of your documentation. The  `master` branch is where the work on the latest versions happen. When releasing a new version of the documentation, save the state of `master` in a branch as the previous version. The branch acts as a label to indicate this is the state of the book for version X of your documentation.

This has two benefits:

- You can publish different versions of your documentation (for example using the [versions plugin](https://plugins.gitbook.com/plugin/versions))
- You can still fix previous version of the documentation (found a typo ? just make a change on the appropriate version branch)


## Conclusion

Of course, branches are not reserved for a single use. Feel free use them as you see fit, and to mix workflows, or make up your own workflow! You can even suggest one to add to this documentation by [emailing us](mailto:contact@gitbook.com).
