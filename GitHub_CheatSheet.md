
> **Create patch**

Step 1) git add [all_changed_file_name]
Step 2) git commit –s
Enter msg for commit changes
Step 3) git format-patch -1
Create patch of last commit

> **Applying Patch**

Step 1) git apply --stat fix_empty_poster.patch
Give you about state of changes deletion in insertion
Step 2) git apply --check fix_empty_poster.patch
Check for errors on applying patch in advance
Step 3) git am <patch name> OR git am <patch name> --reject
--reject option will create reject file which cant be patched automatically

> **Abort failed patch**

```git am --abort```

> **Create all commit in form of patches**

```Git format-patch –[no of commits]```

> **Create new branch**

```Git checkout –b <branch name> <master branch to sync with>```
Eg:
```Git checkout -b Vishal master```

> **To list the branches that exist & to see current brach**

```Git branch -a```

> **Rename a branch**

```Git branch –m <oldname> <newname>```

> Switch a branch

```Git checkout <branch_Name>```

> Reset Branch to particular commit

```Git reset –hard <commit_id>```

> Add multiple file (INTERACTIVE) to Staging area

```Git add  –i```
Step 1 ) Press 2(update menu)
Step 2 ) Check for files separated by commas(like 1,3,7) OR 1 to N separated by dash(like 1-10)
Step 3 ) Press Enter  
