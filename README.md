# Changelog update script

Simple bash script to (version) update CHANGELOG.md using local GIT commit messages and tags.

## Introduction

The whole point of the script is to automate the process of updating the changelog, by
writing your commit messages properly, so they are understood by others and properly "mark"
the changes done in your code.

A good article on "How to Write a Git Commit Message" [https://chris.beams.io/posts/git-commit/]

Generated output of the script can be seen in this package changelog file, 
thus following 'eat your own dog food' principle.

## Notice

The script is easily "hackable", meaning it doesn't have validation for tags and such.

The whole point of the script is to help you automate the process and by inputting
jibberish you will only do harm to your own time.

## MacOS notice

As the script uses GNU sed, it will not work on MacOS out-of-the-box (which uses BSD sed).
If you want it to work on MacOS, you need to install `gsed` (GNU sed) and symlink it as `sed`.

http://gridlab-d.shoutwiki.com/wiki/Mac_OSX/Gsed


## Installation

Per project
```bash
composer require --dev matijakovacevic/changelog
```

or globally
```bash
composer global require matijakovacevic/changelog
```

## Usage

If there is no CHANGELOG.md, the script will create it.
Otherwise, it gets the commits made from the last tag, ignoring merge commits, and
puts them in the CHANGELOG.md file, as items under the 'new version' header.

The header is generated according to the last found tag, following semantic versioning [https://semver.org/].
You can provide arguments like _(major|minor|patch)_ if there are tags to be parsed,
otherwise you can use your own version e.g. _1.5.2_

After completion, it will make a commit to the active branch, with changed CHANGELOG.md file 
and a commit message "changelog updated to $TAG"


```bash
changelog [major|minor|patch]
changelog 1.0.1
```

Per project (from composer bin folder)
```bash
./vendor/bin/changelog ...
```

or globally

```bash
changelog ...
```

## Related stuff:

Keep a Changelog [https://keepachangelog.com/en/1.0.0/]

github - Good ways to manage a changelog using git? - Stack Overflow 
[https://stackoverflow.com/questions/3523534/good-ways-to-manage-a-changelog-using-git]

## Some (more advanced) libraries:

As I'm currently in PHP ecosystem, most of these are PHP libraries:

> Semantic versioning helper library for PHP

SemVer [https://github.com/PHLAK/SemVer]

>Generate change logs from your repositorys on GitHub. 
Based on releases, issues, labels and pull requests

ins0/github-changelog-generator [https://github.com/ins0/github-changelog-generator]

>Automate the tedious tasks of software releases. Happily release and publish your Git repositories, npm packages, 
GitHub & GitLab releases, changelogs, and much more!

webpro/release-it [https://github.com/webpro/release-it]

>Jira & Git Workflow tool

Rentlio/jit [https://github.com/Rentlio/jit]


## Contribute

If you wish to contribute, you're free to make a pull request
