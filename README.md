# adibiton.github.io


### Setup development environment (Mac OSX)
Prerequisite:
- Ruby <version>
```
brew install rbenv
rbenv init
rbenv install <version>
rbenv global <version>
```
- Bundler
```
gem install bundler
```
#### Clone this repo
```
git clone ...
```
#### Install Jekyll
```
bundle install
```

### Build localy
```
bundle exec jekyll serve
```
preview site at: http://localhost:4000

### Create new post

under **_posts** folder add new file with the convention:
`YEAR-MONTH-DAY-title.md`

all posts must start with the following header:

```
---
layout: post
title:  "some title"
---
```

### Create new draft
Drafts are posts which are not ready to publish.
In order to create one, add a markdown file under **_drafts** folder.

In order to preview drafts, run:

```
bundle exec jekyll serve --drafts
```
