
# ansible-config

This repository provides an Ansible playbook for setting up a personal development environment, including configuration for bash, tmux, nvim, i3, asdf, and more.

## Usage

Run the following command to apply the playbook:

```
ansible-playbook main.yaml --ask-become-pass
```

## Roles Overview

- **dotfiles**: Clones your dotfiles repository, ensures correct permissions, removes unnecessary files, and symlinks configuration files using stow.
- **homebrew**: Installs prerequisites, clones and installs Homebrew, sets up bash completions, installs common CLI tools (yq, ripgrep, starship, asdf), and configures asdf initialization.
- **tmux**: Ensures permissions for tmux plugin and configuration directories, and clones the tmux plugin manager (TPM).

## Example: asdf plugin and tool installation

```
asdf plugin add java https://github.com/halcyon/asdf-java.git
asdf plugin add lua https://github.com/Stratus3D/asdf-lua.git
asdf plugin add maven https://github.com/halcyon/asdf-maven.git
asdf plugin add python https://github.com/danhper/asdf-python.git
asdf plugin add node https://github.com/asdf-vm/asdf-nodejs.git
asdf plugin add spring-boot https://github.com/joschi/asdf-spring-boot.git
```

```
asdf install java openjdk-22
asdf global java openjdk-22
asdf install lua 5.1
asdf global lua 5.1
asdf install maven 3.9.9
asdf global maven 3.9.9
asdf install python 3.10.0
asdf global python 3.10.0
asdf install spring-boot 3.3.5
asdf global spring-boot 3.3.5
asdf install node 22.0.0
asdf global node 22.0.0
```
