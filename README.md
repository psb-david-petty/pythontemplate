# pythontemplate

This is a template for a Python project.

## Steps to follow

These steps are based on Github account `psb-david-petty` with private e-mail address `psb-david-petty@users.noreply.github.com` and with this repository `pythontemplate` being copied into repository `newpython`. Change these to match your account and repository.

- Follow [https://docs.github.com/en/github/creating-cloning-and-archiving-repositories/duplicating-a-repository](https://docs.github.com/en/github/creating-cloning-and-archiving-repositories/duplicating-a-repository) to duplicate this repository `pythontemplate` to repository `newpython`.
- Enable *GitHub Pages* for the `master` branch from *Settings*.
<p style="margin: 0 1em; padding: 0 1em; border-left: thick solid red;">Note: As of 2020/10/01, the default branch for Github repositories is `main` rather than `master`. At some point, this repository should follow the [renaming guidelines](https://github.com/github/renaming) and rename the main branch.</p>
- `git clone https://github.com/psb-david-petty/newpython.git` into the parent directory of the `newpython` local branch.
- Change the `.git/config` `url` of the `newpython` local branch as per [`https://gist.github.com/jexchan/2351996`](https://gist.github.com/jexchan/2351996) as follows:
  - from: `url = https://github.com/psb-david-petty/newpython.git`
  - to: `url = git@github.com-bhs:psb-david-petty/newpython.git`
- This SSH configuration is based on having followed the *[Generating a new SSH key and adding it to the ssh-agent](https://docs.github.com/en/free-pro-team@latest/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)* documentation. The change to `git@github.com-bhs` presupposes that `~/.ssh/` contains the files `id_rsa_bhs` and `id_rsa_bhs.pub` and that `~/.ssh/config` contains the following:

```
Host *
  AddKeysToAgent yes
  UseKeychain yes

Host github.com-bhs
  HostName github.com
  User git
  IdentityFile ~/.ssh/id_rsa_bhs
```
- **Note**: for these configuration to work, the key must be added to the `ssh-agent`. Use `ssh-add -l` to see whether the key has been added and, if not, use `ssh-add ~/.ssh/id_rsa_bhs`.
- Add the following to `.git/config` to associate commits with the correct account name:

```
[user]
  name = psb-david-petty
  email = psb-david-petty@users.noreply.github.com
```

- Rename and edit the Python files in `./src/`.

<hr>

[&#128279; permalink](https://psb-david-petty.github.io/pythontemplate) and [&#128297; repository](https://github.com/psb-david-petty/pythontemplate) for this page.
