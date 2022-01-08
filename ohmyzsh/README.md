
# oh-my-zsh setup
Steps to setup oh-my-zsh along with the necessary plugins and fonts

## Installation
1. Install zsh and make it as default for shell
  ```zsh
  sudo apt install zsh \
  chsh -s $(which zsh)
  ```

2. Install [oh my zsh](https://ohmyz.sh/#install)
  ```zsh
  sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
  ```

3. Install [Powerlevel10k - p10k](https://github.com/romkatv/powerlevel10k#oh-my-zsh) plugin
  ```zsh
  git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
  ```
4. Install [zsh auto suggestions](https://github.com/zsh-users/zsh-autosuggestions) plugin

  - Clone this repository into `$ZSH_CUSTOM/plugins` (by default `~/.oh-my-zsh/custom/plugins`)

    ```zsh
    git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
    ```
  - Add the plugin to the list of plugins for Oh My Zsh to load inside `~/.zshrc`(I've already added in .zshrc in my repo):

    ```zsh
    plugins=( 
        # other plugins...
        zsh-autosuggestions
    )
    ```
5. Install fira code for fonts and set it as terminal font in settings
    ```zsh
    sudo apt install fonts-firacode 
    ```

6. Set terminal profile theme to Dissonance 43 in [Gogh](https://mayccoll.github.io/Gogh/)
    ```zsh
      bash -c  "$(wget -qO- https://git.io/vQgMr)" 
    ``` 
7. Copy [alias file](supercharge.zsh) to custom folder under oh-my-zsh
    ```zsh
      cp ohmyzsh/supercharge.zsh ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/supercharge.zsh
    ```
Done !
