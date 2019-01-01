
git config credential.helper store

then

git pull

provide user-name and password and those details will be remembered later. The credentials are stored in a file on the disk, with the disk permissions of "just user readable/writable" but still in plaintext.

if you want to change password later

git pull

will fail, because it failed, it removes the offending user+password from the .git-credentials file, so now run

git pull

provide new password and it will work like before.

WARNING : If you use this method, your git account passwords will be saved in plaintext format, in the global .gitconfig file, e.g in linux it will be /home/[username]/.gitconfig

If this is undesirable to you, use an ssh key for your accounts instead.

--



You can set your username and password like this:

git config --global user.name "your username"

git config --global user.password "your password"

--

You can edit the ~/.gitconfig file to store your credentials

sudo nano ~/.gitconfig

Which should already have

[user]
        email = your@email.com
        user = gitUSER

You should add at the bottom of this file.

[credential]
        helper = store

The reason I recommend this option is cause it is global and if at any point you need to remove the option you know where to go and change it.

ONLY USE THIS OPTION IN YOU PERSONAL COMPUTER.

Then when you pull | clone| enter you git password, in general, the password will be saved in ~/.git-credentials in the format

https://GITUSER:GITPASSWORD@DOMAIN.XXX

WHERE DOMAIN.XXX COULD BE GITHUB.COM | BITBUCKET.ORG | OTHER