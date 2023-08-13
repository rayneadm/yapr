

# Start some git project

```
mkdir yapr && cd yapr  
git init  
git status 
```
**mkdir yapr && cd yapr** -  it'll create project directory  
**git init** - inicialise locale area for git project  
**git status** - show repositary status  

---

## Work with git 

#### After touch or edit some project files in git project directory you can run few commands:<br>

```
git status __#it'll show untracked files__<br>
git add filename __#Add filename to tracking by git__<br>
git add --all __#Add all filest in directory to  tracking by git__<br>
git add . __#The same command as a *git add --all* just add all files to project__<br>

```



After *git add .*  **git status* __#Show project status__<br>
Use *git commit* to fix changes and make a comment<br><br>

git commit -m "Description of changes" __#if you nead to make some big description skip key **-m** it'll open your default editor, where you can write anything for comment.__

git log __#it'll show history oof commit__

```

---

# Work with remote repositary

Run *ls -la ~/.ssh* to know have you any ssh keys or no<br>
if you don't see any files with .pub they'll nead to create.<br>
Read about [ssh-keygen](https://docs.github.com/ru/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent) <br>


On your local mashine run:<br>

*pbcopy < ~/.ssh/id_rsa.pub* this command will copy ~/.ssh/id_rsa.pub <br>
or <br>
*cat  ~/.ssh/id_rsa.pub* and copy result<br>

On the github.com go to your profile setting, SSH and GPG keys and run **New SSH key** green button.<br>
Past your public key and add some description. <br>

To Check connection result run: <br>

**ssh -T git@github.com** <br>
You'll see someting like: *Hi **YouName**! You've successfully authenticated, but GitHub does not provide shell access.*<br>

It means that everything is ok.

---

# Send your project to remote repositary
Create new project on the github.com, like the same on a local mashine ** yapr **<br>
Run green button **Code** then Local-Clone choose SSH and copy URL like: <br>
*git@github.com:**YouName**/yapr.git* <br>

On a local mashine run few commands:<br>

git remote add origin git@github.com:**YouName**/yapr.git __#It'll set remote repositary__<br>

git remote -v  __#Show connected repositary__<br>

git branch -M main __#Set branch name__<br>
git push -u origin main __#Send your files on a github.com__<br>




