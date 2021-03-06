# system configurations

## SHELL

- zsh-async

  ```sh
  git clone https://github.com/mafredri/zsh-async.git ~/.zsh-async
  ```

- oh-my-zsh

  ```sh
  sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
  ```

- starship: <https://starship.rs/>

  ```sh
  curl -fsSL https://starship.rs/install.sh | bash
  echo 'eval "$(starship init zsh)"' >> .zshenv
  ```

- fzf

  ```sh
  git clone --depth 1 https://github.com/junegunn/fzf.git ~/.fzf && ~/.fzf/install
  ```

### dotfiles

- env

  - [`.zprofile`](./.zprofile)
  - [`.zshenv`](./.zshenv)

- env for interactive

  - [`.zshrc`](./.zshrc)
  - [`.zshalias`](./.zshalias)
  - [`.zshfunc`](./.zshfunc)

- git

  - [`.gitconfig`](./.gitconfig) #(git-delta 필요)

## version manager

### asdf

```sh
# asdf
git clone https://github.com/asdf-vm/asdf.git ~/.asdf
cd ~/.asdf
git checkout "$(git describe --abbrev=0 --tags)"
chmod +x asdf.sh

# for help
asdf

# for update
asdf update

# add plugin
asdf plugin add <name> [git-url]
# update plugin
asdf plugin update --all

# for me
asdf plugin add go https://github.com/kennyp/asdf-golang
asdf plugin add python https://github.com/danhper/asdf-python
asdf plugin-add rust https://github.com/code-lever/asdf-rust.git
```

### fnm

```sh
# fnm
curl -fsSL https://fnm.vercel.app/install | bash

# for update
curl -fsSL https://fnm.vercel.app/install | bash -s -- --skip-shell

# for help
fnm
```

## vim

[`.vimrc`](./.vimrc)

```sh
# with curl
curl -fLo ~/.vim/autoload/plug.vim --create-dirs \
    https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim

# with wget
mkdir -p ~/.vim/autoload/
cd ~/.vim/autoload/
wget https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
```

vim-plug 설치: `.vimrc` 수정 후

```vim
:source %
:PlugInstall
```

만약 플러그인 설치가 제대로 되지 않았다면: `:PlugUpdate`
