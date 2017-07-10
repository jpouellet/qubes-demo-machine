# "Qubes Demo Machine"

## Why?

I have a machine I lend to people to try out Qubes with. In order to ensure each person starts with a clean setup and without any potential private information from the last person, I wipe and re-install the machines between users.

Setting up the machines exactly the way I like them to be before lending them out is a long/tedious/annoying process, so this is my attempt at automating it.

## Goals

My goals with this effort are:
- To hopefully save myself time in the long run
- To get more experience with salt
- To potentially inspire others to also set up "Qubes demo machines" and help grow the community :)

## What / To-do:

From a base Qubes 3.2 install

- [ ] Initial sanity
  - [ ] Update Dom0
  - [ ] Install fedora-24{,-minimal} templates
  - [ ] Update f24 templates
  - [ ] Switch sys-\* to fedora-24
  - [ ] Delete the Debian & Whonix templates (if installed)
  - [ ] Install Debian & Whonix templates past the apt bug
  - [ ] Update Debian & Whonix templates
  - [ ] Fix audio un-muting bug manually (*sigh*)
- [ ] Reload wireless driver on suspend/resume
- [ ] Main template setup
  - [ ] Make f24-kitchen-sink template clone
  - [ ] Put dotfiles in f24-kitchen-sink
  - [ ] Install google-chrome in f24-kitchen-sink
- [ ] DispVM customization
  - [ ] Make DispVM based on f24-kitchen-sink
  - [ ] Install .desktop file for google-chrome in DispVM
- [ ] Remove fedora-23\* template & VMs
- [ ] Setup Whonix AppVMs
- [ ] Dom0 customization
  - [ ] Switch screen locking to physlock
  - [ ] qvm-terminal
  - [ ] qvm-file-manager
  - [ ] ShiftIt-X11
  - [ ] qvm-screenshot-helper
  - [ ] Set up keyboard shortcuts
    - [ ] i3-like window movement (via shiftit)
    - [ ] Alt+Enter for new terminal in front VM
    - [ ] Alt+N for new file manager in front VM
    - [ ] Alt+Q for qubes-manager
  - [ ] Create help desktop shortcuts
    - [ ] Open Qubes docs index in misc-browsing
    - [ ] Open Qubes video tutorial in misc-browsing
- [ ] AppVM: misc browsing
  - [ ] Install chrome extensions
    - [ ] uBlock Origin
    - [ ] HTTPS Everywhere
  - [ ] Set home page to Qubes
- [ ] AppVM: secure remote access
  - [ ] Minimal template clone w/ SSH only
  - [ ] AppVM based on that
  - [ ] Remove AppVM shortcuts
  - [ ] Set restricted PATH (or not?)
- [ ] AppVM: file storage
  - [ ] Based on fedora-24-minimal
  - [ ] NetVM for DispVM: none
  - [ ] Open everything in DispVM
- [ ] AppVMs: pair for split-gpg
  - [ ] f24-minimal clone as key-holding template
  - [ ] AppVM (f24-kitchen-sink) for some project
  - [ ] AppVM (f24m-split-gpg) for project keys
  - [ ] point project VM at key-holding VM
  - [ ] Authorize qrexec policy for split-gpg between VM pair
  - [ ] generate demo keys (or not?)
- [ ] Windows
  - [ ] Download windows 7
  - [ ] Verify hash against pinned value
  - [ ] Make template from virtualbox img
  - [ ] Install Qubes windows tools
  - [ ] Update windows (how?)
  - [ ] Clone windows template & make AppVM
  - [ ] Set windows AppVM application shortcuts (paint, minesweeper, notepad, explorer, ...?)
