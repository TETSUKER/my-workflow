### My workflow consist of

* [Fish](https://fishshell.com/) terminal
* [NeoVim](https://neovim.io/)
* [Dracula theme](https://draculatheme.com/)


### Shell setup

* [Fish](https://fishshell.com/) - user friendly terminal
```shell
sudo apt-add-repository ppa:fish-shell/release-3
sudo apt-get update
sudo apt-get install fish
```

* [Fisher](https://github.com/jorgebucaran/fisher) - fish plagin manager
```shell
curl -sL https://git.io/fisher | source && fisher install jorgebucaran/fisher
```

* [Nerd fonts](https://github.com/ryanoasis/nerd-fonts) - Powerline fonts. I use Hack
```shell
wget https://github.com/ryanoasis/nerd-fonts/archive/refs/heads/master.zip
cd nerd-fonts-master/
./install.sh Hack
```
* After installing font go to Edit -> Preferences in your terminal and set *Hack Nerd Font*

* [Tide](https://github.com/IlanCosman/tide) - Shell theme
```shell
fisher install IlanCosman/tide@v5
```

* Set fish as default terminal:
```shell
echo "/usr/bin/fish" | sudo tee -a /etc/shells
sudo chsh -s /usr/bin/fish
```


### NeoVim setup

* [NeoVim](https://neovim.io/) - need version 0.5 or higher
```shell
sudo add-apt-repository ppa:neovim-ppa/unstable
sudo apt-get update
sudo apt-get install neovim
```

* [vim-plug]() - vim plugin manager 
```shell
sh -c 'curl -fLo "${XDG_DATA_HOME:-$HOME/.local/share}"/nvim/site/autoload/plug.vim --create-dirs \
       https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim'
```

* [NeoVim config](init.vim) - put this file into this direcroty *~/.config/nvim/*

* Open `nvim` and start install plugins:
```shell
:source %
:PluginInstall
:call mkdp#util#install()
```

* LSP-TSServer require latest Node.js and npm, so install they if you haven't done before: 
```shell
sudo apt-get install curl
curl -sL https://deb.nodesource.com/setup_16.x | sudo -E bash -
sudo apt-get install nodejs
```

### Dracula theme

* Install theme in shell: `fisher install dracula/fish`

* Already install in config `Plugin 'dracula/vim', { 'name': 'dracula' }` and set by `colorscheme dracula`

