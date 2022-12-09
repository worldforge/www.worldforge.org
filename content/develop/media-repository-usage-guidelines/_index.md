---
title: "Media Repository Guidelines"
menu:
    main:
        weight: 4
        parent: "Develop"

---
{{< imgstyle alchemist.jpg "An alchemist" "float:right; padding: 5px;">}}

Historically, the WorldForge project had no less than four (!) different CVS repositories for its media needs (three of which were used concurrently). Migrating all this data to subversion in a sensible way was a major nightmare, and also more than two man-weeks of work. To make sure the daily administration of the repository will not become a similar burden the Media Team requires that all users of the Media Repository, but especially all artists wishing to commit to it, follow the following rules:

### Visitors and Artists:
* Only check out /svn/media/trunk or sub-trees of it.
This contains the current media data and there is normally no need for you to check out all of /svn/media, which would take a ton of bandwidth, cpu time and disk-space.
* Make sure you retrieve and read the relevant README.txt and LICENSE files for the section you're interested in. Especially in the ancient areas of the repository as not everything is licensed under the GPL/GFDL dual license.

### Artists only:
* **NO test commits**. To perform a commit "just to see if you can" really messes up the repository history which is very hard to fix and makes the whole project look stupid.
There is a special repository for password testing, learning how to use your client, etc.
* **NO commits to ancient**! This is for historic purposes only.
* Don't touch other people's copyright information.
* Make sure to check out the media repository before committing back to the repository.
* You should always do a svn diff (or at least a svn status) on your working copy before commiting. Use TortoiseSVN's preview feature and review if the changes you are about to commit are really what you intended to commit.
* Enter sensible log messages. A short description of what you changed/created is helpful for others.
* The results of separate work should be committed separately - even if you worked at multiple tasks concurrently. You'll have to identify which file changed because of which task, and if a file has changes from both tasks, this becomes difficult. An easier solution is to have two working copies from the beginning.
* If you are unsure if something you want to do is acceptable, discuss it on #media with one of the Media Team admins.