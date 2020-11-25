## Create a new private repository on the command line

**Setting up a new Git Private Repo on the command line**

***Create a new repository on the command line***

```bash
touch README.md
git init
git add README.md
git config  user.email YOUR_EMAIL
git config  user.name YOUR_USERNAME
git commit -m "first commit"
curl -u YOUR_USERNAME:YOUR_TOKEN https://api.github.com/user/repos -d '{"name":<reponame>, "private":"true"}'
git remote add origin https://YOUR_USERNAME:YOUR_TOKEN@github.com/YOUR_USERNAME/<reponame>.git
git push -u origin master
```

***Push an existing repository from the command line***
```bash
git remote add origin https://YOUR_USERNAME:YOUR_TOKEN@github.com/YOUR_USERNAME/<reponame>.git
git push
```
