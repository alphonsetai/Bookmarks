
> **Create new branch**

```Git checkout –b <branch name> <master branch to sync with>```
Eg:
```Git checkout -b Vishal master```

> **To list the branches that exist & to see current brach**

```Git branch -a```

> **Rename a branch**

```Git branch –m <oldname> <newname>```

> **Switch a branch**

```Git checkout <branch_Name>```

> **Create patch**

```git add [all_changed_file_name]```
```git commit –s```
*Note:* Enter msg for commit changes
```git format-patch -1```
*Note:* Create patch of last commit

> **Applying Patch**

```git apply --stat [patch_name.patch]```
*Note:* Give you about state of changes deletion in insertion
```git apply --check [patch_name.patch]```
*Note:* Check for errors on applying patch in advance
```git am [patch_name.patch] OR git am [patch_name.patch] --reject```
*Note:* --reject option will create reject file which cant be patched automatically

> **Abort failed patch**

```git am --abort```

> **Create all commit in form of patches**

```Git format-patch –[no of commits]```

> **Reset Branch to particular commit**

```Git reset –hard <commit_id>```

> **Add multiple file (INTERACTIVE) to Staging area**

```Git add  –i```
Step 1 ) Press 2(update menu)
Step 2 ) Add files separated by commas(like 1,3,7) OR 1 to N separated by dash(like 1-10)
Step 3 ) Press Enter  
