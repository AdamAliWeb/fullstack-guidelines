# Git & Github

## References

- **[Git Reference](https://git-scm.com/)**
- **[Github Documentation](https://docs.github.com/en)**

## Workflows

### Setup a global user

```bash
    git config --global user.name "githubUsername"
    git config --global user.email "githubEmail@gmail.com"
```

### Initialize a Github repo with tags

```bash
   git init
   git add .
   git tag -a "App Version" -m "Tag Message"
   git commit -m "Commit message"
   git remote add origin https://github.com/user/repository.git
   git push --tags
   git push -u origin main
```

### Configure SSH Key

To establish a connection in my PC through the new SSH Keys method and be able to push to my repositories more comfortable, I have to follow these steps:

```bash
ssh-keygen -t ed25519 -C "emailAddress@gmail.com"
```

You can change the location of the keys and add a password. Each time you try to establish a connection you have to write that password. But you can just skip that part hitting enter.

Then you have to add the key to your github profile. Enter to `settings -> SSH and GPG Keys` and then create a new key. You have to paste the key content in order to add the key, to do that smoothly there is a command you can use to have it already on the clipboard

```bash
clip < ~/.ssh/id_ed25519.pub
```

For the last step to test and establish the connection you have enter this command. If it ask you to establish connection type `yes`

```bash
ssh -T git@github.com
```

### How to deploy your project to Github pages

Go to your repository, then `settings > pages` and in the Branch options select the Branch you would like to deploy, this will take a while. You also can setup Github Actions if your project requires a build process.

### To display your commits and branches history into a log

- Commits:

  ```bash
    git log > commits.log
  ```

- Branches:

  ```bash
    git log --graph --oneline --decorate --all > graph.log
  ```

- Examples
  - **[commits](./commits.log)**
  - **[branches](./graph.log)**

### How to update a commit

1. `git commit --amend -m "an updated commit message"` to change its message

2. `git commit --amend --no-edit` will update a file into the commit without changing it's commit message. You had to staged your file first after the 1st commit

## Tools

- **[Gitignore.io](https://www.toptal.com/developers/gitignore)**: It's a tool that allows you to generate template for your `.gitignore` file depending on the type of the project you working on.

## Tips & Tricks

1. Github Pages is used for static site hosting, no server-side rendering

2. When pulling from a repository it's better to use `git pull --rebase`. This instead of merging the commits you put the new commits in you local work

3. While merging or rebasing, If you made a mistake you can go back adding `--abort` after git merge/rebase.

4. To be able to check the commits which weren't pushed, use `git log --oneline --branches --not --remotes`

5. To go back to a previous commit it depends if the commit was pushed to the repo. If no then use `git reset "commit"`. If yes then use `git revert`
