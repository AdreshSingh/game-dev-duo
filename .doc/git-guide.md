Absolutely. Here's the **cheat sheet** for your two GitHub accounts setup on Windows + VS Code.

 ## Your setup

 You have:

 - **`Arpit-devank`** → personal account
- **`AdreshSingh`** → second/work account

 SSH keys:

```
~/.ssh/github_personal
~/.ssh/github_work
```

 Your SSH config is:

```
Host github-personal
    HostName github.com
    User git
    IdentityFile ~/.ssh/github_personal
    IdentitiesOnly yes

Host github-work
    HostName github.com
    User git
    IdentityFile ~/.ssh/github_work
    IdentitiesOnly yes
```

 So:

```
github-personal → Arpit-devank
github-work     → AdreshSingh
```

 ## For a personal repo

 When cloning:

```
git clone git@github-personal:Arpit-devank/REPO_NAME.git
```

 For an existing repo:

```
git remote set-url origin git@github-personal:Arpit-devank/REPO_NAME.git
```

 Check:

```
git remote -v
```

 You should see:

```
git@github-personal:Arpit-devank/REPO_NAME.git
```

 Then:

```
git pull
git push
```

 VS Code's **Pull / Push / Sync** will use the correct account automatically.

 ## For your other account

 Use:

```
git clone git@github-work:AdreshSingh/REPO_NAME.git
```

 Or change an existing repo:

```
git remote set-url origin git@github-work:AdreshSingh/REPO_NAME.git
```

 Then normal:

```
git pull
git push
```

 ## The important idea

 You **don't need to switch GitHub accounts in VS Code**.

 The repository's remote decides which account is used:

```
git@github-personal:...  → Arpit-devank
git@github-work:...      → AdreshSingh
```

 So you can have both projects open in VS Code at the same time and push to different GitHub accounts. 🚀

 ### Your current `game-dev-duo`

 You've configured it as:

```
origin → git@github-personal:Arpit-devank/game-dev-duo.git
```

 So this project is now using **Arpit-devank**.

 For the latest code:

```
git pull
```

 And to upload your changes:

```
git add .
git commit -m "your message"
git push
```

 That's basically it. 🎯