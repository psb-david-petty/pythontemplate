# pythontemplate

This is a template for a Python project.

## Steps to follow

These steps are based on Github account `psb-david-petty` and this repository `pythontemplate` being copied into repository `newpython`. Change to match your repo.

- Follow [https://docs.github.com/en/github/creating-cloning-and-archiving-repositories/duplicating-a-repository](https://docs.github.com/en/github/creating-cloning-and-archiving-repositories/duplicating-a-repository) to duplicate this repository `pythontemplate` to repository `newpython`.
- Enable *GitHub Pages* for the `master` branch from *Settings*.
- `git clone https://github.com/psb-david-petty/newpython.git` into the parent directory of the `newpython` local branch.
- Change the `.git/config` `url` of the `newpython` local branch as per [`https://gist.github.com/jexchan/2351996`](https://gist.github.com/jexchan/2351996) as follows:
  - from: `url = https://github.com/psb-david-petty/newpython.git`
  - to: `url = git@github.com-bhs:psb-david-petty/newpython.git`
- The change to `git@github.com-bhs` presupposes that `~/.ssh/` contains the files `id_rsa_bhs` and `id_rsa_bhs` and that `~/.ssh/config` contains the following:
```
Host *
  AddKeysToAgent yes
  UseKeychain yes

Host github.com-bhs
  HostName github.com
  User git
  IdentityFile ~/.ssh/id_rsa_bhs
  ```
  - Rename and edit the Python files in `./src/`.


<hr>

[&#128279; permalink](https://psb-david-petty.github.io/pythontemplate) and [&#128297; repository](https://github.com/psb-david-petty/pythontemplate) for this page.
