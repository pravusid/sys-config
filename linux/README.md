# Linux 환경설정

## X Window 환경확인

`echo $XDG_SESSION_TYPE`

## 터미널 변경

`gsettings set org.gnome.desktop.default-applications.terminal exec {terminal-name}`

`sudo update-alternatives --config x-terminal-emulator`

### vim 다른 터미널 사용시 수정 (`/usr/share/applications/vim.desktop`)

```text
Exec=/usr/bin/tilix -e vim %F
Terminal=false
```

## 단축키 충돌

- `dconf-editor`
- `/org/gnome/desktop/wm/keybindings/`
- `activate-window-menu`: 비활성화
- `switch-to-workspace-up`, `switch-to-workspace-down`: `['<Super>Page_Up']`, `['<Super>Page_Down']`
- `switch-to-workspace-left`, `switch-to-workspace-right`: 비활성화

## color schemes

- <https://github.com/arcticicestudio/nord-dircolors/>
- <https://github.com/arcticicestudio/nord-gnome-terminal>
- <https://github.com/arcticicestudio/nord-gedit>