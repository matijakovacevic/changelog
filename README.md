# Changelog

Simple bash script to (version) update CHANGELOG.md using (local) GIT's commit messages and tags, while ignoring merge commits.


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

## Related stuff you should know about:

Keep a Changelog [https://keepachangelog.com/en/1.0.0/]

github - Good ways to manage a changelog using git? - Stack Overflow 
[https://stackoverflow.com/questions/3523534/good-ways-to-manage-a-changelog-using-git]

Semantic Versioning 2.0.0 [https://semver.org/]

How to Write a Git Commit Message [https://chris.beams.io/posts/git-commit/]

## Some libraries for managing:

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
