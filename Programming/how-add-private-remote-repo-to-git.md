### Step 1 Generate ssh keys. (note this needs to be done once per device)

run this command in your terminal: 
```
ssh-keygen -t ed25519 -C "youremail@gmail.com"
```
then run this:
```
cat ~/.ssh/id_ed25519.pub
```
copy the output from the cat command

### Step 2 Add it to github

Go to github then click your profile in the top right corner.
Select settings and then "SSH and GPG keys".
From there add new key and paste the output from the cat command

### Step 3 Switch from https to ssh

If you have added the repo to git already then run this command:

```
git remote set-url origin git@github.com:YOURUSERNAME/REPO_NAME.git
```
(note I am using origin as the default remote repository's name)

If you haven't then run this command
```
git remote add origin git@github.com:YOURUSERNAME/REPO_NAME.git
```
