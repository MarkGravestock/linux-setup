## Linux (Ubuntu 22.04) setup

Here's how i setup Ubuntu (may work for other *nix variants). I'm running it under WSL2.
May require changes for other variants (e.g. package manager commands).

### Shell customisation

#### [ZSH](https://zsh.sourceforge.io/Guide/zshguide.html) 

> ``sudo apt install zsh``

 Switch shells to ZSH

> ``chsh -s $(which zsh)``

#### [Oh my ZSH](https://ohmyz.sh/) 

Prerequisite

[Nerd Font](https://github.com/ryanoasis/nerd-fonts#patched-fonts)

>``git clone --filter=blob:none --sparse  https://github.com/ryanoasis/nerd-fonts.git``
>
>``cd nerd-fonts``
>
>``git sparse-checkout add patched-fonts/Meslo``
>
>``./install.sh Meslo``

Install

> ``sh -c "$(wget https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh -O -)"``

Configure some plug-ins

> | Name | Description |
> |-----|-----|
> | git | The git plugin provides many aliases and a few useful functions [see details](https://github.com/xianmin/oh-my-zsh/blob/master/plugins/git/README.md) |
> | gradle | blah |
> | zsh-autosuggestions | ``git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions`` |
> | dotnet | This plugin provides completion and useful aliases for dotnet core [see details](https://github.com/xianmin/oh-my-zsh/blob/master/plugins/dotnet/README.md) |

Install [Powerlevel10k](https://github.com/romkatv/powerlevel10k) Theme

>``git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k``

> set ``ZSH_THEME="powerlevel10k/powerlevel10k"``
>
> ``source ~/.zshrc``

#### [Starship](https://starship.rs/)

> ``curl -sS https://starship.rs/install.sh | sh``

### Dev Tools

#### DotNet

Ensure Microsoft Package Registry is configured

[Instructions](https://learn.microsoft.com/en-us/dotnet/core/install/linux-ubuntu#register-the-microsoft-package-repository)

Install DotNet

>``sudo apt install	dotnet-sdk-7.0``

### Java SDK

Running ``java`` will suggest what ``apt install`` to run
