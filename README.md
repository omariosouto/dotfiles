# My Dot files:

## Automate this
```sh
### Instalando Git e coisas básicas
xcode-select --install

### Oh My ZSH
sudo sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
git clone https://github.com/lukechilds/zsh-nvm ~/.oh-my-zsh/custom/plugins/zsh-nvm 
rm -rf ~/.zshrc

### Install rosetta
/usr/sbin/softwareupdate --install-rosetta --agree-to-license

### Setup dos dotfiles
git clone https://github.com/omariosouto/dotfiles.git ~/.dotfiles
cd ~/.dotfiles
ln -s ~/.dotfiles/.zshrc ~/.zshrc
ln -s ~/.dotfiles/.gitconfig ~/.gitconfig

### Instalando o Home brew
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> /Users/mariosouto/.profile && eval "$(/opt/homebrew/bin/brew shellenv)"
brew bundle --file ~/.dotfiles/Brewfile

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
cd ~/.dotfiles && brew bundle dump --force
```
