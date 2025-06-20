On GitHub
- Go to https://github.com/settings/tokens
- Click on generate new token (classic)
- Put the scope `repo` 
- Click on create token
- Cut the token and paste on the terminal

To make `git push` without the token exec the command:
```sh
git config --global credential.helper store
```
