# new feature

Created in Notepad++ then saved to d:\git\new-feature.md

git status
and a bunch of git commands:

C:\Users>git --version
git version 2.5.3.windows.1

d:\git>git log
Date:   Mon Feb 15 12:24:39 2021 +1100

    added 3rd line in readme feature

d:\git>git checkout develop
Already on 'develop'

d:\git>git flow init -d
Using default branch names.

Which branch should be used for bringing forth production releases?
   - develop
   - feature/new-feature
   - master
Branch name for production releases: [master]

Which branch should be used for integration of the "next release"?
   - develop
   - feature/new-feature
Branch name for "next release" development: [develop]

How to name your supporting branch prefixes?
Feature branches? [feature/]
Release branches? [release/]
Hotfix branches? [hotfix/]
Support branches? [support/]
Version tag prefix? []

d:\git>git branch
* develop
  feature/new-feature
  master


d:\git>git flow feature finish new-feature
Already on 'develop'
Already up-to-date.
Deleted branch feature/new-feature (was 63d37a0).

Summary of actions:
- The feature branch 'feature/new-feature' was merged into 'develop'
- Feature branch 'feature/new-feature' has been removed
- You are now on branch 'develop'


d:\git>git branch
* develop
  master

d:\git>git flow feature start a-new-feature
Switched to a new branch 'feature/a-new-feature'

Summary of actions:
- A new branch 'feature/a-new-feature' was created, based on 'develop'
- You are now on branch 'feature/a-new-feature'

Now, start committing on your feature. When done, use:

     git flow feature finish a-new-feature


d:\git>git status
On branch feature/a-new-feature
Untracked files:
  (use "git add <file>..." to include in what will be committed)

        new-feature.md

nothing added to commit but untracked files present (use "git add" to track)

d:\git>git add -A

d:\git>git commit -am "added new feature"
 1 file changed, 5 insertions(+)
 create mode 100644 new-feature.md

d:\git>git status
On branch feature/a-new-feature
nothing to commit, working directory clean

d:\git>git remote add origin https://github.com/pcross42/git-work-flow.git

d:\git>git remote -v
origin  https://github.com/pcross42/git-work-flow.git (fetch)
origin  https://github.com/pcross42/git-work-flow.git (push)

d:\git>git checkout master
Switched to branch 'master'

d:\git>git push origin master

Counting objects: 6, done.
Delta compression using up to 8 threads.
Compressing objects: 100% (2/2), done.
Writing objects: 100% (6/6), 486 bytes | 0 bytes/s, done.
Total 6 (delta 0), reused 0 (delta 0)
To https://github.com/pcross42/git-work-flow.git
 * [new branch]      master -> master

d:\git>git push origin develop
Counting objects: 6, done.
Delta compression using up to 8 threads.
Compressing objects: 100% (3/3), done.
Writing objects: 100% (6/6), 573 bytes | 0 bytes/s, done.
Total 6 (delta 0), reused 0 (delta 0)
remote:
remote: Create a pull request for 'develop' on GitHub by visiting:
remote:      https://github.com/pcross42/git-work-flow/pull/new/develop
remote:
To https://github.com/pcross42/git-work-flow.git
 * [new branch]      develop -> develop

d:\git>git flow feature
  a-new-feature

d:\git>git flow feature publish a-new-feature
Counting objects: 3, done.
Delta compression using up to 8 threads.
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 357 bytes | 0 bytes/s, done.
Total 3 (delta 0), reused 0 (delta 0)
remote:
remote: Create a pull request for 'feature/a-new-feature' on GitHub by visiting:
remote:      https://github.com/pcross42/git-work-flow/pull/new/feature/a-new-feature
remote:
To https://github.com/pcross42/git-work-flow.git
 * [new branch]      feature/a-new-feature -> feature/a-new-feature
Switched to branch 'feature/a-new-feature'
Your branch is up-to-date with 'origin/feature/a-new-feature'.

Summary of actions:
- A new remote branch 'feature/a-new-feature' was created
- The local branch 'feature/a-new-feature' was configured to track the remote branch
- You are now on branch 'feature/a-new-feature'

git commit -am "updated new-feature with commands"
git push origin feature/a-new-feature