
> **Create new branch**

```git checkout –b [BRANCH_NAME] [MASTER_BRANCH_TO_SYNC_WITH]```
Eg:
```git checkout -b Vishal master```

> **List all branches**

```git branch -a``` 
 *Note:* '*' mark on current brach
 
 > **Edit Last Commit**

```git commit --amend -m "New commit message"``` 
 *Note:* Edit last commit

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

> **Check Patch & Clean Patch**

```~/linux-[VERSION]/scripts/checkpatch.pl [PATCH_NAME.patch]```
*Note:* It is a tool to check your coding style match Linux coding style or not. You can use -help to see what options you can use. After it check your file, the tool prints a result like compile result. The result show you which line has coding style errors and warnings, and reminds you how to modify your code. And also you can modify the script tool to match your own coding style.

```~/linux-[VERSION]/scripts/cleanpatch [PATCH_NAME.patch]```
*Note:* For removing with space error

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
git log --pretty=oneline --abbrev-commit
```


## Manual Patching 

> Statement
- Library(v1.0) + 2 Yr Development =  Directory1
- Library(v9.0-New_Release + Library_Vendor_Development) = Directory2
- Problem want to move our development in new library

Step 1) Extracting Only 2 Yr Development from Directory1

Create Directory1_1 = First Initial Commit
Create Directory1_2 = Last Development changes Commit

```diff -Naur Directory1_1 Directory1_2 > Diff.patch```

Step 2) Applying 2 Yr Development to Directory2

goto Directory2 ----Note: Don't get in Directory2

```patch -p0 < Diff.patch```

This patch creates reject files which will cant be modified automatically

Note: Name of Directories should make same if not patching properly

