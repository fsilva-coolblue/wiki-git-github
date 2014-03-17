#Git - branching

If you're working alone in your own project, just doing one thing (or a very
linear set of things), then the basic workflow we saw works fine.
However, when you want to collaborate with others (and not interfere in their
work), or work on new features while keeping old stable versions readily
available (e.g. for bug fixing), then you need branches (even if you think you
don't).

You may remember from older version control systems like CVS and SVN that
branches were these heavy things that created more problems than they solved,
and merging was a nightmare. Well, not any more.

In git, merging is not only very easy, it is actually encouraged, and pretty
much part of every decent workflow you find.

##Branches in git

Git uses "lightweight" branches. This means that they are simply a pointer to a
commit. Nothing is copied when you create a branch, git just creates a new
pointer and makes it point to the latest commit, and that's it. You may not see
the advantage of this, but let's just say that it's what allows git to
be so good at branching and merging.

In git you are always working in a branch. This is called the current branch,
and the default (created along with the repository) is `master`.

##How to do it

###Create a branch

In the command line, to create a new branch and immediately switch to it, you run `git checkout -b <branch_name>`.
If, for some reason, you want to simply create a new branch but remain in the
current one, you can use `git branch <branch_name>`.

In SourceTree, just press the `Branch` button:
![SourceTree - Create branch](img/sourcetree-createbranch.png)
The `Checkout New Branch` checkbox is checked by default. Uncheck it if you do
not want to switch to the new branch after its creation.

###Switch to (checkout) a branch

As said before, branches in git are simply pointers to commits. And, as we saw
in [the previous
article](https://sites.google.com/a/coolblue.nl/it-wiki/algemeen/version-control/git-an-introduction/1-git-basics#TOC-Checkout),
you can (in the command line) checkout a commit by running `git checkout`. So,
in the command line, you can checkout a branch by doing `git checkout branch_name`.
In SourceTree, you right-click the branch you want to select and choose the
`Checkout <branch>...` option.
![SourceTree - Checkout branch](img/sourcetree-checkoutbranch.png)


