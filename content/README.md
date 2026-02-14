# Tyblog
This is the repository for my Hugo blog. You can reuse it!
## Prerequisites
- Your repo must be public
- Setup Github Pages for your repo
- Setup Hugo deployment workflow in github actions
## Adding a new post
First you will need a local copy of this repository. Let's call it Tyblog

1. Open tyblog as a vault in obsidian
2. Ctrl + n -> new note
3. Insert template "new-post-header" - this will automatically add date and structure
4. Write your post
5. It will be in root directory - when you're ready to publish, just move it to "posts"
6. go to cmd

```bash
cd tyblog
git add .
git commit -m "update"
git push origin main
```

**Tip:** create a script
1. In Windows
Build
```bash
echo cd tyblog > tdeploy.bat
echo git add . >> tdeploy.bat
echo git commit -m "update" >> tdeploy.bat
echo git push origin main >> tdeploy.bat
```

Run
```bash
tdeploy.bat #or win+R -> tdeploy
```

1. In Linux


