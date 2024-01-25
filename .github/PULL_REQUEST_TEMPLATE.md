Thank you for your interest in contributing to the TOOLZ library

# PR_NAME
# 3 CAT+MSG Release note line (see bottom of page)
## Short description of the what the PR does
## Issue(s) Fixed + Issue Num
### Description of how this PR fixed the issues mentioned above
#### List of changes made
#### Must-DO Pre-PR Checklist

#### !! Example PR below!! ####
-----------------
# ZCASH SAPLING PARAM AUTO-DOWNLOAD PR #
# [GENERAL] [ENHANCEMENT] [Component] - Added ZCASH Sapling download to mkbootstrap script 'mkboot.sh'

## Added functionality to the mkbootstrap.sh script so that the SAPLING files are automatically downloaded and installed when the script is run, first run and all subsequent with check for precense of them, if missing they will get downloaded again.

## Fixes ISSUE #1001 - When starting node, it will hang and never start downloading blocks or showing connections to peers 

### This was due to the missing SAPLING param files not being downloaded when node is setup using 'installNewNode.sh' script after node was installed and param files were present at once point, but then somehow deleted; or when using this script as it was (checking for presence of param files but only notifying if not present, yet not downloading them).

#### Changes made:

- [ ] Added line; 'wget -O https://download.the.files.com/params'
- [ ] Added line; 'mv param/sapling/* /node/dir'
- [ ] Added email alert funtionality
- [ ] Removed the etc etc

##### Must-Do Pre-PR Checklist:

- [X] Tested end to end
- [X] Documentation updated / changed
- [X] Changelog entry
- [X] Build log updated
--------------------

#### Release Notes: 3 CATEGORY+MSG Line - Formatting and proper use
--------------
Help reviewers and the release process by writing release notes. Also include this at top directly under the PR/Feature name declaration, the second line in the PR after the name.

[CATEGORY] [TYPE] [LOCATION] - Message

    CATEGORY
  [----------]      TYPE
  [ CLI      ] [-------------]    LOCATION
  [ DOCS     ] [ BREAKING    ] [-------------]
  [ GENERAL  ] [ BUGFIX      ] [ {Component} ]
  [ INTERNAL ] [ ENHANCEMENT ] [ {Filename}  ]
  [ IOS      ] [ FEATURE     ] [ {Daemon} ]      |-----------|
  [ ANDROID  ] [ MINOR       ] [ {Framework} ] - | {Message} |
  [----------] [-------------] [-------------]   |-----------|

### EXAMPLE
 [INTERNAL] [FEATURE] [./scripts] - Added thing to script that does X and Y
