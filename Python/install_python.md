# To set up the latest version of Python on macOS

To start learning Python, I first needed to install it. However, as I googled, I found that the macOS should come with Python pre-installed which is probably not the latest version. 
So I thought to check the version of Python in my Mac.

```bash
% python --version
```
But it answers back,
```bash
zsh: command not found: python
```
I had no idea why and thought to just install from website.
[Python download page](https://www.python.org/downloads/release/python-3122/)

After downloaded, I installed but it did not work properly or it was because there are 2 pythons.
Then out of blue, I remembered something and I came up with this below.

```bash
% python3 --version
Python 3.9.6
```

YES!
But still it's not the latest. The latest as of February 2024 is Python.12.2 (and is planned to be released 3.13 in October).


## So how can I get current version?

#### Prerequisites
* Homebrew is installed

### 1. Install `pyenv`
***
Using Homebrew I installed `pyenv`
(Confirmed it's not installed yet, just in case)
```bash
% pyenv -v
zsh: command not found:pyenv
```
```bash
% brew install pyenv
Running `brew update --auto-update`...
==> Auto-updated Homebrew!
Updated 2 taps (homebrew/core and homebrew/cask).
==> New Formulae
asmfmt       flowpipe     helm-docs    kin          openjph      tfautomv
deadfinder   g-ls         icloudpd     mtm          sui
==> New Casks
cleanupbuddy               hancom-docs                mumuplayer
easydevo                   lunarbar                   nrfutil

You have 8 outdated formulae installed.

==> Downloading https://ghcr.io/v2/homebrew/core/pyenv/manifests/2.3.35
######################################################################### 100.0%
==> Fetching dependencies for pyenv: openssl@3
==> Downloading https://ghcr.io/v2/homebrew/core/openssl/3/manifests/3.2.1
######################################################################### 100.0%

# ....

==> Pouring ca-certificates--2023-12-12.all.bottle.tar.gz
==> Regenerating CA certificate bundle from keychain, this may take a while...
🍺  /usr/local/Cellar/ca-certificates/2023-12-12: 3 files, 226.7KB
==> Installing openssl@3
==> Pouring openssl@3--3.2.1.sonoma.bottle.tar.gz
🍺  /usr/local/Cellar/openssl@3/3.2.1: 6,874 files, 32.5MB
==> Installing pyenv
==> Pouring pyenv--2.3.35.sonoma.bottle.tar.gz
🍺  /usr/local/Cellar/pyenv/2.3.35: 1,132 files, 3.4MB
==> Running `brew cleanup pyenv`...
Disable this behaviour by setting HOMEBREW_NO_INSTALL_CLEANUP.
Hide these hints with HOMEBREW_NO_ENV_HINTS (see `man brew`).
==> Upgrading 1 dependent of upgraded formulae:
Disable this behaviour by setting HOMEBREW_NO_INSTALLED_DEPENDENTS_CHECK.
Hide these hints with HOMEBREW_NO_ENV_HINTS (see `man brew`).
ruby-build 20231114 -> 20240119
==> Downloading https://ghcr.io/v2/homebrew/core/ruby-build/manifests/20240119
######################################################################### 100.0%
==> Fetching dependencies for ruby-build: autoconf
==> Downloading https://ghcr.io/v2/homebrew/core/autoconf/manifests/2.72
######################################################################### 100.0%
==> Fetching autoconf
==> Downloading https://ghcr.io/v2/homebrew/core/autoconf/blobs/sha256:12368e33b
######################################################################### 100.0%
==> Fetching ruby-build
==> Downloading https://ghcr.io/v2/homebrew/core/ruby-build/blobs/sha256:61f4463
######################################################################### 100.0%
==> Upgrading ruby-build
  20231114 -> 20240119 

==> Installing dependencies for ruby-build: autoconf
==> Installing ruby-build dependency: autoconf
==> Downloading https://ghcr.io/v2/homebrew/core/autoconf/manifests/2.72
Already downloaded: # ....

==> Pouring autoconf--2.72.sonoma.bottle.tar.gz
🍺  /usr/local/Cellar/autoconf/2.72: 71 files, 3.6MB
==> Installing ruby-build
==> Pouring ruby-build--20240119.all.bottle.tar.gz
🍺  /usr/local/Cellar/ruby-build/20240119: 599 files, 316.5KB
==> Running `brew cleanup ruby-build`...
Removing: /usr/local/Cellar/ruby-build/20231114... (592 files, 313.9KB)
==> Checking for dependents of upgraded formulae...
==> No broken dependents found!
```

It seems that it automatically updated Homebrew and upgraded ruby related file.

```bash
% pyenv -v 
```
```bash
pyenv 2.3.35
```

### 2. Set up `pyenv`
***
Add the following commands allow to write the initialization settings for pyenv into the .zshrc file
```bash
% echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.zshrc
% echo 'export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.zshrc
% echo 'eval "$(pyenv init -)"' >> ~/.zshrc
```

Reload the `.zshrc` file to apply changes 
```bash
% source ~/.zshrc
```

These commands do not display anything  when executed.

### 3. Install Python
***
Using pyenv, install Python finally.
See all available versions for `pyenv`

```bash
% pyenv install --list
```
Then it shows a long long list.
```bash
Available versions:
  2.1.3
  2.2.3
  2.3.7
  2.4.0
  2.4.1
  ....

  3.12.0
  3.12-dev
  3.12.1
  3.13.0a2
  3.13-dev
  ....

  stackless-3.5.4
  stackless-3.7.5
```

Since there was no 3.12.2, install a Python 3.12.1.

```bash
% pyenv install 3.12.1
```
```bash
python-build: use openssl@3 from homebrew
python-build: use readline from homebrew
Downloading Python-3.12.1.tar.xz...
-> https://www.python.org/ftp/python/3.12.1/Python-3.12.1.tar.xz
Installing Python-3.12.1...
python-build: use readline from homebrew
python-build: use zlib from xcode sdk
Installed Python-3.12.1 to /Users/####/.pyenv/versions/3.12.1
```
`'Installed Python-3.12.1'`  but...

Check on the installed Python

```bash
% python3 --version 
```
```bash
Python 3.12.2
```

## Completed. 
I couldn't find why it turned out to be the latest version but anyway now I have it.