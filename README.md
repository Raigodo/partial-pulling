**setup:**
-main
  -my-folder
    -b.txt
    -c.txt
  -a.txt

-branch2
  -my-folder
    -c.txt
    -include-me.txt
    -exclude-ne.txt
  -a.txt
  -include-me.txt
  -exclude-ne.txt

**changes:**
make some changes in branch2 (whatever you wish)

**used command to merge (pure git used)**
```
git checkout branch2
git checkout -b temp-branch
git rm exclude-me.txt
git rm my-folder/exclude-me.txt
// remove every file we want to exclude (can be automated by using advanced stuff)
git add .
git commit -m "Merged changes from branch2 excluding exclude-me files"
git checkout main
git merge temp-branch
git push origin main
git branch -d temp-branch
```

thats all :)
