
> **Create new branch**

```git checkout –b [BRANCH_NAME] [MASTER_BRANCH_TO_SYNC_WITH]```
Eg:
```git checkout -b Vishal master```

> **List all branches**

```git branch -a``` 
 *Note:* '*' mark on current brach

> **Rename a branch**

```git branch –m [OLD_NAME] [NEW_NAME]```

> **Switch a branch**

```git checkout [BRANCH_NAME]```

> **Delete a branch**

```git branch –D [BRANCH_NAME]```

> **Create patch**

```git add [ALL_CHANGED_FILES]```
*Note:* Check all changed files by 'git status'

```git commit –s```
*Note:* Enter msg for commit changes

```git format-patch -1```
*Note:* Create patch of last commit

> **Applying Patch**

```git apply --stat [PATCH_NAME.patch]```
*Note:* Give you about state of changes deletion in insertion

```git apply --check [PATCH_NAME.patch]```
*Note:* Check for errors on applying patch in advance

```git am [PATCH_NAME.patch] OR git am [PATCH_NAME.patch] --reject```
*Note:* --reject option will create reject file which cant be patched automatically

> **Abort failed patch**

```git am --abort```

> **Create all commit in form of patches**

```git format-patch –[NO_OF_COMMIT]```

> **Reset Branch to particular commit**

```git reset –hard [COMMIT_ID]```

> **Add multiple file (INTERACTIVE) to Staging area**

```git add  –i```

Step 1 ) Press 2(update menu)

Step 2 ) Add files separated by commas(like 1,3,7) OR 1 to N separated by dash(like 1-10)

Step 3 ) Press Enter  

> **Miscellaneous**

```
git config --global user.name [NAME]
git config --global user.email [EMAIL_ID]
git push origin  commit-id:master
git checkout [TAG_NAME]
git fetch –tags
git tags –l
git describe --tags
git name-rev --tags --name-only $(git rev-parse HEAD)
git status
git log
```
