# google-chat-linux-git

An electron-base client for Google Hangouts Chat, since Google didn't see fit to provide one.

upstream project : https://github.com/robyf/google-chat-linux

I'm not the author of the app : praise **robyf** for his excellent work.

I'm barely maintaining it for my own use now that he left off.

## build and run

``sh
npm install
./google-chat-linux.sh
```

## make it work manually

electron 5 beta is required

```sh
npm install electron@beta
```

fix the rights on sandbox executable as the error message will suggest, OR if you're in a hurry :

```sh
export PATH=/path/to/node_modules/.bin:$PATH
export ELECTRON_DISABLE_SANDBOX=true; electron .
```

## Linux packages

## Arch

a package 'google-chat-linux-git' is availabe on AUR for Arch Linux and derivatives.

## Debian based

Run :

```sh
npm run dist
```

will build a .deb file in `dist/`.

Installation of the .deb file is untested... please provided feedback if you use it !

NOTE : You'll probably have to :

- either `sudo chown root:root /opt/google-chat-linux/chrome-sandbox && sudo chown 4755 /opt/google-chat-linux/chrome-sandbox` after the .deb is installed
- or run `export ELECTRON_DISABLE_SANDBOX=true` before the launch of `/opt/google-chat-linux/google-chat-linux`

The provided .desktop file takes care of it. (at least it should)
