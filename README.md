# Tyblog
This is the repository for my Hugo blog. You can reuse it!
## Prerequisites
- Your repo must be public
- Setup Github Pages for your repo
- Setup Hugo deployment workflow in github actions
- 
## Adding a new post
First you will need a local copy of this repository. Let's call it Tyblog.

```bash
git clone https://github.com/atysen/tysengardenblog.git tyblog
```

or if you already have it locally

```bash
git pull --rebase origin main
```

Then

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

### Publish script - Windows
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

or win + R => tdeploy

### Publish script - Linux
Build
```bash
echo '#!/bin/bash' > tdeploy.sh
echo 'cd tyblog' >> tdeploy.sh
echo 'git add .' >> tdeploy.sh
echo 'git commit -m "update"' >> tdeploy.sh
echo 'git push origin main' >> tdeploy.sh
chmod +x tdeploy.sh
```

Run
```bash
./tdeploy.sh # or alt +F2 -> ./tdeploy.sh
```

#### Optional -> create the command

Put your script in /usr/local/bin/
```bash
sudo mv tdeploy.sh /usr/local/bin/tdeploy 
sudo chmod +x /usr/local/bin/tdeploy
```

Now you can run (alt+F2):
```bash
deployt
```
