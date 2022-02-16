# Notes on the M1 MacBook Pro

I got my new M1-based MacBook Pro (17,1) on Monday (11/23/2020). Here are some preliminary notes.
<!--more-->
This MBP 13" is identical to the previous Intel 13" outwardly, but inside, it's very different. I maxed it out with 16GB of RAM and a 2TB SSD and it's noticeably snappier. No the fan is never audible, and even when rendering a large 4K Motion file it only gets a little warm. And battery life is the best of any system I've ever used. It depends a lot on what I'm doing but it's always at least 9 hours and usually around 15. 

All that's great but you have to weigh it against the issues of software compatibility. Over time Apple Silicon's advantages over Intel will increase, while software issues will gradually disappear. But _today_ the issue of incompatible software could be significant[^compat], especially at the edges. 

[^compat]: See [this Register article](https://www.theregister.com/2020/11/18/apple_silicon_m1_mac_compatibility/) from 11/18 - but it's a moving target and things will get better over time.

The [Is Apple Silicon Ready website](https://isapplesiliconready.com) has a decent list of some big names that are (and aren't yet) native. But under the surface lurk many thousands of programs that just don't run. All Apple programs run natively. Many popular Mac programs run natively. Many CLI and dev tools don't run at all. 

Yes it's a cool architecture, yes it's really fast, but unless you feel like your machine is slow (I didn't feel that way with any Macs in the past couple of years), and you're sure the programs you need will work, it might be worth waiting until the Mac dev community gets with it. 

I'll keep track of the issues I'm encountering in the following table.[^lipo] Note: I'm using [Macports](https://www.macports.org) as my package manager. 

[^lipo]:  The ```lipo info``` command is helpful in determining whether a program is universal. (e.g. ```lipo -info /Applications/LastPass.app/Contents/MacOS/LastPass``` or ```lipo -info (status fish-path)```) The Mac Activity Monitor also has an "Architecture" column. 

| Program | Native? | Runs? | Notes|
| ---- | :----: | :----: | ---- |
| Google Chrome (87) | 😍 | 😍 | Stadia works, too! |
| Panic Nova | 😍 | 😍 | I'm using it to write this! |
| iTerm | 😍 | 😍 |  |
| ssh | 😍 | 😍 | Apple provided, OpenSSH_8.1p1, LibreSSL 2.7.3 |
| git, curl, nano, bash, zsh, vim, sed, grep, awk, python, perl, etc. | 😍 | 😍 | Apple provided |
| VSCode | 😍 | 😍 | [Insiders beta](https://code.visualstudio.com/insiders/#) some extensions fail |
| Fish shell | 😍 | 😍 | native out of the box, yay! |
| Rust | 😍 | 😍 | yay rustup! | 
| Emacs CLI | 😍 | 😍 | ```sudo port install emacs-devel``` works! |
| Emacs GUI | 😍 | 😍 | ```sudo port install emacs-app-devel``` |
| homebrew | 😍 | 😍 | Now M1 native, but many packages are not yet. I've switched to Macports for many reasons[^macports] |
| Dr Racket | 😍 | 😍 | Woo hoo! Thanks to Matthew Flatt! Requires building from source, for now. |
| Lastpass | ☠️ | 😍 | works fine and speed isn't an issue |
| Mailmate | ☠️ | 😍 | My preferred email program - seems to run fine under Rosetta 2 |
| MacPorts | ☠️ | 😍 | but many of the ports don't run[^macports] |
| Syncthing | ☠️ | 😍 | installed via Macports |
| Franz | ☠️ | 😍 | https://meetfranz.com an electron app - electron is getting updated so should these, eventually |
| ghcup | ☠️ | ☠️ | Haskell installer "Unknown architecture" |
| SBCL Lisp | ☠️ | ☠️ | won't install using MacPorts, but as a stopgap ECL is native |
| Docker | ☠️ | ☠️ | |

[^macports]: It's worth running ```sudo port selfupdate``` daily - many packages are being updated for Apple Silicon (just got gnupg updated for arm). I find Macports more Unix-y. This article helped me make the switch from Homebrew to Macports: [Thoughts on macOS Package Managers](https://saagarjha.com/blog/2019/04/26/thoughts-on-macos-package-managers/).

I suppose for some of the command-line utilities it might be possible to compile from source using gcc but many libraries aren't ported yet (notably gnutls), others like OpenJDK and Electron have been ported but we're still waiting for their dependent projects to update. Many apps have ARM versions; so maybe it's a Big Sur issue? 

Update: I built Racket CS from source (using the latest version from Github). It's now Apple native and man is it FAST! Faster even than Racket BC on my iMac Pro with 64GB of RAM. 

Honestly, two months in, I don't even want to use any other computer. The M1 MacBook is the best laptop I've ever owned. I'm very excited to see what Apple does in 2021. I'll probably replace all our Macs. Intel just doesn't cut it any more. 


