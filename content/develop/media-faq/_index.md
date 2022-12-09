---
title: "Media FAQ"
menu:
    main:
        weight: 3
        parent: "Develop"

---
### Where is the WorldForge Media Repository?

The Media Repository is a Subversion repository located at https://svn.worldforge.org:886/svn/media/trunk/. Read-only access is allowed for anonymous users but if you wish to commit files then you need to contact one of the Media Team admins.
Best way to do that is to contact us on [Gitter](https://gitter.im/Worldforge/Lobby).

### What is Subversion (or SVN)?

The following description is taken from the introduction to the book [Version Control with Subversion](http://svnbook.red-bean.com/)
Subversion is a free/open-source version control system. That is, Subversion manages files and directories over time. A tree of files is placed into a central repository. The repository is much like an ordinary file server, except that it remembers every change ever made to your files and directories. This allows you to recover older versions of your data, or examine the history of how your data changed. In this regard, many people think of a version control system as a sort of "time machine".

The FAQ for Subversion is [here](http://subversion.apache.org/faq.html).

### How do I get a copy of the Media Repository?
First you need to read the [Media Repository Usage Guidelines](develop/media-repository-usage-guidelines). Failure to do what is suggested will cause you to lose any commit privileges.
Second you need to obtain an SVN client: google knows how and where,

Thirdly you need to re-read the [Media Repository Usage Guidelines](develop/media-repository-usage-guidelines/) and follow the instructions.

The whole media repository is about 20 GB on disk currently (2018-03-26). As Subversion keeps local copies of all files to do fast binary diffs, this means you have to get about 10 GB from the server if you want to check out everything.
### How do I checkout the media repository using the command line svn tool?

`svn co https://svn.worldforge.org:886/svn/media/trunk media`

This will get the current trunk media repository, and put it into the dir called 'media' in your local directory. You can use this checkout anonymously for reading the repository, for details on committing to the repository see the svn manual.
