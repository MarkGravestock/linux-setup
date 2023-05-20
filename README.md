## Linux (Ubuntu) setup

Here's how i setup Ubuntu (may work for other *nix variants)

### Shell customisation

#### [ZSH](https://zsh.sourceforge.io/Guide/zshguide.html) 

> ``sudo apt install zsh``

 Switch shells to ZSH

> ``chsh -s $(which zsh)``

#### [Oh my ZSH](https://ohmyz.sh/) 

Prerequisite

[Nerd Font](https://github.com/ryanoasis/nerd-fonts#patched-fonts)

>``git clone --filter=blob:none --sparse  https://github.com/ryanoasis/nerd-fonts.git``
>``cd nerd-fonts``
>``git sparse-checkout add patched-fonts/JetBrainsMono``
>``git sparse-checkout add patched-fonts/FiraCode``
>``git sparse-checkout add patched-fonts/Meslo``
>``./install.sh JetBrainsMono``
>``./install.sh FiraCode``
>``./install.sh Meslo``

> ``sh -c "$(wget https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh -O -)"``

Configure some plug-ins

> | Name | Description |
> |-----|-----|
> | blah | blah |

Install [Powerlevel10k](https://github.com/romkatv/powerlevel10k) Theme

>``git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k``

> set ``ZSH_THEME="powerlevel10k/powerlevel10k"``
> ``source ~/.zshrc``

#### [Starship](https://starship.rs/)

> ``curl -sS https://starship.rs/install.sh | sh``


