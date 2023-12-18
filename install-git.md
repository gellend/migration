# Git Installation and GitHub Setup

In case of a disaster or the need for a quick connection between your local Git and GitHub account, follow the steps below:

1. Check for Existing SSH Keys

   `ls -al ~/.ssh`

2. Generate a New SSH Key

   Choose **one** of the following commands:

   `ssh-keygen -t rsa -b 4096 -C "your_email@example.com"`

   OR

   `ssh-keygen -t ed25519 -C "your_email@example.com"`

3. Add Your SSH Key to the ssh-agent

   `eval "$(ssh-agent -s)"`

   `ssh-add ~/.ssh/your_key`

4. Add a New SSH Key to Your GitHub Account

   `cat ~/.ssh/your_key.pub`

   Then, go to **Settings -> SSH and GPG keys -> New SSH key** on GitHub. You need to input twice for **Authentication Key** and **Signing Key**.

5. Commit Signature Verification with SSH Key

   `git config --global gpg.format ssh`

   `git config --global user.signingkey /PATH/TO/.SSH/KEY.PUB`

6. Optional: Auto-sign Your Commits

   `git config --global commit.gpgsign true`

7. Test your SSH key

   `ssh -T git@github.com`

8. Optional: Auto-Make Remote Branch

   `git config --global push.autoSetupRemote true`
