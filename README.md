 <div align="right">
    <img src="https://img.shields.io/static/v1?label=Language&message=shell&color=%235BB97E&style=flat-square"/>
    <img src="https://img.shields.io/github/license/dougmb/fuzzy-pkg-finder?color=%235BB97E&label=LIC&style=flat-square"/>
</div>
 <div align="center"><h1>📦<br>Fuzzy-pkg-finder (fork)</h1></div>

> Fork of [ericlay/fuzzy-pkg-finder](https://github.com/ericlay/fuzzy-pkg-finder), which is no longer maintained.

**Simple cli utility using fzf to search and install/list/remove packages.**\
 \
![Screenshot](https://raw.githubusercontent.com/ericlay/fuzzy-pkg-finder/master/fpf.png) \
 \
Leverages the power of fzf to search package names and descriptions then presents complete package information in preview pane. \
On selection will hand off to Pacman or Paru/Yay to complete transaction. \
  \
*For use with Pacman/Yay/Paru package managers only.*\
 \

### Changes from upstream
- Fix preview commands failing on non-bash shells (fish, zsh) due to process substitution `<()` syntax

 \
Installation: \
Manual build and install:
```
git clone https://github.com/dougmb/fuzzy-pkg-finder
cd fuzzy-pkg-finder
makepkg -sric
```
 \
Usage:
```
Syntax: fpf [-a| --aur] [-l| --list-installed] [-la| --list-aur-installed]
              [R| --remove] [-o| --orphans] [-U | --update] [-h | --help]
Defaults to Pacman if no options passed

Searching for a package:
ex: fpf [pkg name] for official repo search
ex: fpf -a [pkg name] for aur search

Options:
-a, --aur
    Search/List and install from AUR with Yay

-l, --list-installed
    Search/List installed packages from official repo

-la, --list-aur-installed
    Search/List installed packages from AUR

-R, -remove
     Search/List installed packages for removal

-o, --orphans
     Search/List orphaned packages for removal

-U, --update
     Shows packages with updates available

-h, --help
     Print this help screen
```
\
Keybinds:
```
'ctrl + /' Toggle the preview window
'ctrl + h' Show help in the preview window
'ctrl + k' Show the keybinds in the preview window
'ctrl + n' Move to the next selected item
'ctrl + b' Back to previoius selected item

When browsing AUR or installed Aur pkgs:
'ctrl + p' Preview the highlighted pkgbuild file
'ctrl + x' Return to the highlighted pkg info
```
