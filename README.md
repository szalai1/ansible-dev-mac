#  Setting up mac with ansible
Inspired by: https://github.com/geerlingguy/mac-dev-playbook

## bootstraping
```bas
# install brew or check https://brew.sh/
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
brew install git
# install python
brew install python
#install pip
python3 -m ensurepip --upgrade
python3 -m pip install ansible
```

Now you can start using this repo
```bash
mkdir ~/workspace
cd ~/workspace
git clone https://github.com/szalai1/ansible-dev-mac.git
cd ansible-dev-mac
ansible-galaxy install -r requirements.yaml
sudo ls
ansible-playbook local.yaml -i inventory
```

Install nix
`sh <(curl -L https://nixos.org/nix/install) --daemon`

Install vscode extensions
```
for e in `cat vscode-extensions.list`; do code --install-extension $e ; done
```

Fzf setup
`$(brew --prefix)/opt/fzf/install`

- Install Arc browser (invite only at the moment)
### TODO

[ ] secret handling

[ ] handling dot files: https://github.com/szalai1/dotfiles

[ ] adopt nix and direnv
