# Installs an Arch Linux Desktop

This is an ansible recipe I use to rebuild my Arch desktop, so it's quite personalized, but I hope you can use it to base off and build your own.

## Usage

1. Start by editing vars/package-list.yml to add or remove package depending on your workstation/server to install.

2. Modify ../inventory/hosts.example. If you are only going to install a workstation locally, you don't need to change this; only if you plan to install serveral workstations at the same time.

3. Install the oficial packages by running
```bash
ansible-playbook pacman-packages.yml -i ../inventory/hosts.example -K
```
4. Install yaourt and makepkg, needed for AUR by running:
```bash
ansible-playbook yaourt-install.yml -i ../inventory/hosts.example -K
```
5. Install the AUR based packages by running:
```bash
ansible-playbook aur-desktop.yml -i ../inventory/hosts.example -K 
```

## TODO
- [x] The ansible pacman module seems to fail idempotency tests. I need to debug if this is a thing with one of my packages or in general with the module. Solution: It seem I needed to replace "libreoffice" for "libreoffice-fresh" to solve idempotency on the pacman module.
- [ ] Add automated testing. Partial. About half of the recipes are being tested.
