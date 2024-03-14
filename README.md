# MySSHGuide
## What is this?
Small command repository so I don't lose the handy file with all commands I use for my SSH configuration and swapping of two accounts in GitHub.

## Commmands

### Check loaded keys:
ssh-add -l

### Check username/email currently logged in:
git config user.name/user.email

### Change username/main currently logged in:
git config user.name/email "Your New Name/Email“ (for a specific repository)
git config --global user.name "Your New Name" (for all repositories)

### Clear SSH agent and add your Key:
ssh-add -D (reset agent)
ssh-add /Your/file/path/

~/.ssh/id_rsa -> Default location on MAC for rsa files.

### Test your SSH connection:
ssh -T git@github.com

### How to configurate multiple users in SSH:
Ir ao config em ‘~/.ssh’ para configurar o ficheiro ‘nano’ e este comando:
Host github.com-(account)
  HostName github.com
  User git
  AddKeysToAgent yes
  UseKeychain yes
  IdentityFile (/path/to/your/private/key)
  IdentitiesOnly yes
(Alterar consoante utilizador)