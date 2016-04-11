# Solving conflicts

## What are conflicts ?

Conflicts happen when two people edit the same part of a page/document at the same time on different computers. They also happen when you want to merge changes made by a branch into another branch of a book. GitBook can typically merge changes back together, but sometimes it’s too ambiguous for GitBook to decide by itself. That's when we need your help.

## Resolving conflicts

Though you can always resolve conflicts using the command line, you can also do it from the convenience of the Editor.

When you save/commit your work, or when your merge branches, and the Editor detects conflicts, the conflict resolution UI is displayed. From there, you are only a few steps away from being done:

1. Select an unresolved conflict in the list
2. Resolve it by editing the content and _marking it as solved_
3. Repeat for the remaining conflicts, and hit the **Apply** button

### List of conflicts

Files with conflicts that require your intervention are listed in the sidebar. All conflicts need to be resolved, and you can quickly see which one you already resolved thanks to the checkmark. Selecting a file will bring it in the editor so you can resolve the conflicts.

### Merge editor

The current file is displayed here as two versions. Initially, the version on the left side is your version of the file. It is your version that you need to edit to include changes from others (their version is displayed on the right side). When dealing with branches, the left side is the branch you are merging _into_, the right side is the one you are merging _from_.

{% hint style="tip" %}
If you ever made a mistake and want to restore your version of the file, you can do so with the clock-like button in the toolbar.
{% endhint %}

### Marking as solved

You can mark a conflict as solved by hitting the dedicated button in the toolbar, or clicking the indicator near its entry in the conflicts list. This is merely used to keep track of your progress and make sure you don't forget to resolve a conflict before validating. In particular, it has no effect such as saving the file ; changes are automatically kept as you edit the files.

## Feedback

Since the conflict resolution UI is a recent addition to the Editor, we always appreciate feedbacks. Don't hesitate to send your suggestions using [our contact form](https://www.gitbook.com/contact).
