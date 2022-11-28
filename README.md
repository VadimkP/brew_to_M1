# brew_to_M1

1. Create a Brewfile
Th first thing you’ll want to do is run brew bundle dump on your Intel Mac. This will create a Brewfile, which is just a list of all packages that have been installed with brew. Here’s part of mine to give you an idea of what it looks like.

```bash
brew bundle dump
```

2. ```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

On an M1 Mac it will create a new installation under /opt/homebrew (on Intel it’s under /usr/local/bin).

Edit your .bash_profile or .zshrc file to update any PATH additions or aliases to the new Homebrew installation. For example, alias nano=/opt/homebrew/bin/nano instead of alias nano=/usr/local/bin and export PATH="/opt/homebrew/bin:$PATH" in place of export PATH="/usr/local/bin:$PATH". But do read on for a solution that works with multiple Macs of different CPU architectures.

