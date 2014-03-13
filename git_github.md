#Git and Github - What, Why and How?

##What is git?

"What exactly is this git thing?!", you ask.

Well, git is a *distributed version control system*.
What does this mean, really? It means that:

- *Version control system*
  Git allows you to track changes to your work, keeping previous versions in
  history, and allowing you to revert back to them if something goes wrong (and
          eventually, something usually does).
  You may know other version control systems like SVN and Mercurial. Git does
  the same (and more), but sometimes in different (often better) ways.
- [*Distributed*](http://git-scm.com/book/en/Getting-Started-About-Version-Control#Distributed-Version-Control-Systems)
  Unlike SVN, for instance, git is a *distributed* version control system. That
  means that there is no single central repository as the only point of
  access. In git, everyone working in a project has a complete, working
  repository, and can connect to other repositories to share work (we will talk
          about this later on).
- *Local operations*
  As said above, everyone working in a project in git has their own repository.
  This repository is local to the developer's computer, which means that, for
  most of the operations, you don't need access to a server, or even an internet
  connection. You can work in an airplane, in a tropical beach, you name it.
  This also means that, by not going to the server every time, git is also
  faster. It may not seem much, but after a while this can save you a lot of
  time.

##Why ~is git~ should I use git?

"OK, so I know what this git thing is... But why should I use it?", you ask
again, clearly not satisfied.

So, if the previous items didn't convince you, let me list them, and others, as
a set of advantages:

- With git you can track changes to your work and revert when something goes
wrong
  (Advantage versus having no version control at all)
- You can work offline without a hitch
  (Try working in SVN without access to the server)
- There are effectively multiple backups of the code
  (Since everyone has a repository, each person has a complete copy of the whole
   history of the code)
- It is faster
  You don't have to wait for anyone else for (almost) anything. And the program
  itself was built thinking of speed.
- It's easier to collaborate
  (Since everyone has a repository, anyone can work in any part of the code
   without getting on someone else's toes. You can also get someone else's code
   without having to go through the central repository first. This can be useful
   for reviewing.)
- No more branch/merge fear
  (Compared to previous version control systems, git allows for *much* easier
   branching and merging. We'll see this later, but for now let's just say that
   the ability to switch between branches whenever you'd like and merge them
   (nearly) without any problems is *really* nice.)
- More agile workflows
  (The ability to branch and merge easily allows for some interesting and very
   helpful workflows (which, again, we'll talk about later))
- Used everywhere
  If nothing else convinces you, just know that *a lot* of projects use it. From
  very small ones (e.g. a lot of stuff that's on github) to big ones (e.g. the
  Linux kernel). So, it's not some newfangled curiosity that's going
  away in a few months. It's here to stay.

Convinced now?
Then, let's take a look at how git works and how you should work with it.

##How does it work?!

First, the basics:

###3 Sections

Git divides your workspace into 3 sections:

![Git - 3 sections](3sectionsimage.png)

- Working directory (also called working copy)
  This is what you work on. The working directory includes any new files
  created, new changes to existing files, etc. When you look at your project
  folder you see your working directory.
- Staging area (also sometimes called index)
  The staging area is where changes (editing, adding or removing files) are
  placed in preparation to be sent to the repository. When you `commit` (see
  below), only changes in the staging area are sent.
- Repository (local to your computer)
  When changes are sent to the repository (committed), they are now effectively
  under version control. Once here, you can later recover previous changes,
  check any file's history, etc. When your work gets here, it's safe.


####Basic workflow
