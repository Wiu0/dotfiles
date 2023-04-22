# dotfiles

## Automate this
```sh
### Instalando Git e coisas básicas
xcode-select --install

### Fish (https://gist.github.com/idleberg/9c7aaa3abedc58694df5)
# Installation

1. Install [fish](http://fishshell.com/) via [Brew](http://brew.sh/)
2. Optionally install [Oh My Fish!](https://github.com/oh-my-fish/oh-my-fish) 
3. Add fish to known shells
4. Set default shell to fish

```bash
brew install fish  
curl -L https://get.oh-my.fish | fish
sudo bash -c 'echo $(which fish) >> /etc/shells'
chsh -s $(which fish)
```

### Install rosetta
/usr/sbin/softwareupdate --install-rosetta --agree-to-license

### Setup dot dotfiles
git clone --recurse-submodules https://github.com/wiu0/dotfiles.git ~/git/myself/dotfiles/.config/ .dotfiles
cd ~/git/myself/dotfiles/.config/ .dotfiles
ln -s ~/git/myself/dotfiles/.config/ .dotfiles/.zshrc ~/.zshrc
ln -s ~/git/myself/dotfiles/.config/ .dotfiles/.gitconfig ~/.gitconfig

### Instalando o Home brew
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> $HOME/.profile && eval 
"$(/opt/homebrew/bin/brew shellenv)"
brew bundle --file ~/git/myself/dotfiles/.config/ .dotfiles/Brewfile

#### Java Fixes
sudo ln -sfn /opt/homebrew/opt/openjdk/libexec/openjdk.jdk /Library/Java/JavaVirtualMachines/openjdk.jdk

### Finalização
cd ~ && mkdir ./dev
```

## Post install
```sh
#### Flutter Specific
flutter doctor --android-licenses
```

## How to extract current installed files?
```sh
cd ~/git/myself/dotfiles/.config/ .dotfiles && brew bundle dump --force && git add . && git commit -m "update" && git push 
```

