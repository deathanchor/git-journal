# git-journal
Command line Diary or Journal keeping tool using git for history

## git-journal (gj)
Simple minimalized `git-journal` command to make journal, diary, or other type of daily or minutely entries for notes. This will use bash for now and will try to stick to minimal tools that are typically easy to install without a lot of dependencies.

For convienence, `git-journal` has a link `gj` for short-hand command use.

## Setup
Just put the files in your path, and run from anywhere. You need to initialize your git repo per the environment variables below.

### Environment Variables defaults
Change these enviroment variables as you please, but if unset they will default to the following:
```bash
# parent directory where your journal repository resides
GJ_DIR=~/git
# the name of your journal repository directory (git commands run in $GJ_DIR/$GJ_JOURNAL_NAME)
GJ_JOURNAL_NAME=myJournal
# whatever editor you want to use, most OS default to vi or vim
EDITOR=
```

## Usage

### Entry
From anywhere run the `gj` command with or without arguments. If arguements are provided it will use that for the Title of the file and first line of the file entry. If no arguemnts, the first line of the file will be used to determine the name of the file to be created after editor save and exit.

#### Example
```bash
$ date
Thu Dec  6 11:14:52 EST 2018
$ gj First Entry
```
This will create a file in the `$GJ_DIR/$GJ_JOURNAL_NAME/2018/12-Dec/06-Thu-11:14-EST_First_Entry` and open it with your `$EDITOR`. Once you save and exit the editor, it will add the file to git, commit with the same `First Entry` as the comment and `git push` the changes.

## Encryption
To keep this minimal, if you want your git repository encrypted on the cloud, I suggest you use keybase.io to create a git repository there which will have your git repository encrypted on the cloud, but will keep your local copy unencrypted for easy searching.

# Authors
Niko Janceski (@deathanchor)

