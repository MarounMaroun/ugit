<h1 align="center">ugit</h1>
<p align="center"><img align="center" alt="ugit logo" height="100px" src="https://user-images.githubusercontent.com/34342551/115037937-a608d800-9eec-11eb-88a9-252da7d6f507.png"></p>
<h3 align="center"><code>Undo your last oopsie 🙈️ in git</code></h4>
<p align="center">
  <a href="https://github.com/Bhupesh-V/ugit/actions/workflows/build.yml">
    <img alt="build ugit" src="https://github.com/Bhupesh-V/ugit/actions/workflows/build.yml/badge.svg">
  </a>
  <a href="https://deepsource.io/gh/Bhupesh-V/ugit/?ref=repository-badge" target="_blank"><img alt="DeepSource" title="DeepSource" src="https://deepsource.io/gh/Bhupesh-V/ugit.svg/?label=active+issues&show_trend=true"/></a>
  <a href="https://github.com/Bhupesh-V/ugit/blob/master/LICENSE">
    <img alt="License: MIT" src="https://img.shields.io/github/license/Bhupesh-V/ugit" target="_blank" />
  </a>
  <a href="">
    <img alt="platform support linux and macos" src="https://img.shields.io/badge/platform-GNU/Linux %7C MacOS-blue">
  </a>
  <a href="https://twitter.com/bhupeshimself">
    <img alt="Twitter: bhupeshimself" src="https://img.shields.io/twitter/follow/bhupeshimself.svg?style=social" target="_blank" />
  </a>
  <img align="center" title="ugit demo: restore file to a previous commit" alt="ugit demo: restore file gif" src="https://user-images.githubusercontent.com/34342551/117250614-19a16380-ae61-11eb-97a9-8ba1695cc50a.gif"><br>
</p>

<h2><details><summary>More Video Demos ✨️</summary>

<h4>Undo <code>git add</code></h4>

https://user-images.githubusercontent.com/34342551/117613719-f1797380-b184-11eb-9ff1-689b125265a9.mp4

<h4>Undo <code>git branch -D</code></h4>

https://user-images.githubusercontent.com/34342551/117613828-18d04080-b185-11eb-808b-fa1a65876ee9.mp4

<h4>Undo <code>git merge</code></h4>

https://user-images.githubusercontent.com/34342551/117613992-4ddc9300-b185-11eb-9286-bdc8b3aa2a8d.mp4

</details></h2>

## Why `ugit`

- You did an accidental `git` command you didn't want to.
- You don't want to waste your time searching on _how to undo ..._
- Because ugit is cool

### [Motivations behind writing ugit 🙇‍♂️️](https://bhupesh-v.github.io/undo-your-last-git-mistake-with-ugit)

## What's in the box
`ugit` supports undoing following operations, some are a WIP. If you know of any other operations that can be undone and is not in the list, make sure to send a quick PR 💛️

- [x] Undo `git commit`
- [x] Undo `git add`
- [x] Undo `git push`
- [x] Undo `git branch -D` (branch delete)
- [x] Undo `git pull`
- [x] Undo `git reset`
- [x] Undo `git tag -d` (tag delete)
- [x] Undo `git stash apply`
- [x] Undo `git stash pop/drop/clear`
- [x] Undo accidental file delete (Restore a deleted file after a commit)
- [x] Undo (Restore) a file to a previous version
- [x] Undo `git merge`
- [ ] Undo `git tag` (rename a tag)
- [ ] Undo `git rebase`
- [ ] Undo `git cherry-pick`
- [ ] Undo `git worktree remove` (recover deleted work-tree)

Help me finish above tasks by contributing?

Have any other ideas/suggestions? [**Hop in to ugit discussions 💬️**](https://github.com/Bhupesh-V/ugit/discussions/7)

## Installation

**ugit** dependencies:

- `Bash`>=3
- GNU utils like `awk`, `grep`, `tput` etc
- [fzf](https://github.com/junegunn/fzf) (Install latest version. Minimum required 0.21.0)


1. Install the script using `curl`

   **Linux**
   ```bash
   curl -fsSL https://github.com/Bhupesh-V/ugit/releases/latest/download/ugit -o ugit && chmod +x ugit && mv ugit $HOME/.local/bin/
   ```

   **Mac**
   ```bash
   curl -fsSL https://github.com/Bhupesh-V/ugit/releases/latest/download/ugit -o ugit && chmod +x ugit && mv ugit /usr/local/bin
   ```
   
   Or Arch Linux users can install [**ugit via AUR**](https://aur.archlinux.org/packages/ugit).

2. Verify installation
   ```bash
   ugit --version
   ```
   Optionally run `ugit --help` to see help and management commands
   
   ```bash
   Undo your last oopsie in Git 🙈
   Usage: ugit [-h] [-v] [-u]

   ugit helps you undo your last git command without much effort
   Just run 'ugit' and search for what you want to undo

   Available options:

   -h, --help      Print this help and exit
   -v, --version   Print current ugit version
   -u, --update    Update ugit

   Contact 📬: varshneybhupesh@gmail.com for assistance
   Read the guide: https://bhupesh.gitbook.io/notes/git/how-to-undo-anything-in-git

   ```

## `ugit` in ...
**News**

- Featured on [Changelog News](https://changelog.com/news/ugit-helps-you-undo-your-last-git-command-with-grace-8X6L#discussion)
- The [guide was tweeted by GitHub](https://twitter.com/github/status/1392207961355862018?s=20) (the guide was complementary to ugit, since I was logging my research process there)

**Community**

- Alexander Alemayhu made a youtube tutorial on [Undoing Your Last Git Commit with Ugit](https://www.youtube.com/watch?v=nUnCgKb4tSc)

## Please read ⚠️

Git comes with a garbage collector ([in case you didn't know](https://git-scm.com/docs/git-gc)) therefore undoing some commands will become impossible if the entries are deleted from the reflog.
One way to prevent this is to increase default time limits before the reflog entries expire:
Add these configuration in your global `.gitconfig` file:

```gitconfig
[gc]
    # default 90 days
    reflogExpire = 200
```
Used to set how long records in a branches reflog should be preserved.

```gitconfig
[gc]
    # default 30 days
    reflogExpireUnreachable = 90

```
Used to set how long inaccessible reflog records should be preserved.

## Not satisfied? 😒️

You can read my in-process guide on [**How to undo anything in Git**](https://bhupesh.gitbook.io/notes/git/how-to-undo-anything-in-git)

## Author

:bust_in_silhouette: **Bhupesh Varshney**

- Web : [bhupesh-v.github.io](https://bhupesh-v.github.io)
- Twitter : [@bhupeshimself](https://twitter.com/bhupeshimself)
- DEV : [bhupesh](https://dev.to/bhupesh)

## Credit & Thanks
To all the SO threads that I will probably never visit again ;)

## ☺️ Show your support

Support me by giving a ⭐️ if this project helped you! or just [![Twitter URL](https://img.shields.io/twitter/url?style=social&url=https%3A%2F%2Fgithub.com%2FBhupesh-V%2Fugit%2F)](https://twitter.com/intent/tweet?url=https://github.com/Bhupesh-V/ugit&text=ugit%20via%20@bhupeshimself)

[![Support via PayPal](https://cdn.rawgit.com/twolfson/paypal-github-button/1.0.0/dist/button.svg)](https://www.paypal.me/BhupeshVarshney/)

## 📝 License

Copyright © 2021 [Bhupesh Varshney](https://github.com/Bhupesh-V).<br />
This project is [MIT](https://github.com/Bhupesh-V/ugit/blob/master/LICENSE) licensed.

## 👋 Contributing

Please read the [CONTRIBUTING](CONTRIBUTING.md) file for the process of submitting pull requests to us.

## Contributors ✨

Thanks goes to these wonderful people ([emoji key](https://allcontributors.org/docs/en/emoji-key)):

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore-start -->
<!-- markdownlint-disable -->
<table>
  <tr>
    <td align="center"><a href="https://github.com/sharan-aithal"><img src="https://avatars.githubusercontent.com/u/32029982?v=4?s=100" width="100px;" alt=""/><br /><sub><b>Sharan Aithal</b></sub></a><br /><a href="https://github.com/Bhupesh-V/ugit/commits?author=sharan-aithal" title="Code">💻</a> <a href="https://github.com/Bhupesh-V/ugit/commits?author=sharan-aithal" title="Documentation">📖</a></td>
    <td align="center"><a href="https://tabulate.tech"><img src="https://avatars.githubusercontent.com/u/58576759?v=4?s=100" width="100px;" alt=""/><br /><sub><b>Tabulate</b></sub></a><br /><a href="https://github.com/Bhupesh-V/ugit/commits?author=TabulateJarl8" title="Code">💻</a> <a href="#platform-TabulateJarl8" title="Packaging/porting to new platform">📦</a></td>
  </tr>
</table>

<!-- markdownlint-restore -->
<!-- prettier-ignore-end -->

<!-- ALL-CONTRIBUTORS-LIST:END -->

This project follows the [all-contributors](https://github.com/all-contributors/all-contributors) specification. Contributions of any kind welcome!
