# lookout

This is an unofficial Microsoft Outlook client. The official one from Microsoft is retired and got replaced with PWA. Read the blog [here](https://techcommunity.microsoft.com/t5/microsoft-outlook-blog/microsoft-outlook-progressive-web-app-now-available-on-linux/ba-p/3669846).

Please report bugs and enhancements in the issues section. We will attend them as soon as possible. Please review the open/close issues before raising a new one and avoid duplicates. We encourage everyone to join our chat room in [matrix](https://matrix.to/#/#lookout_community:gitter.im) and ask your questions. That's probably the quickest way to find solutions. Alternatively open a github discussion.

As this is a wrapper around the web version of outlook, we would not be able to add certain features. It's not because we don't want to, but we're fully dependent on Microsoft in certain cases. We may close the issue stating the same reason.

PRs and suggestions are welcomed. We will continue to support the community.

---

[![Gitter chat](https://badges.gitter.im/blackburn29/lookout.png)](https://gitter.im/lookout/community "Gitter chat")
![](https://img.shields.io/github/release/blackburn29/lookout.svg?style=flat)
![](https://img.shields.io/github/downloads/blackburn29/lookout/total.svg?style=flat)
![Build & Release](https://github.com/blackburn29/lookout/workflows/Build%20&%20Release/badge.svg)
![](https://img.shields.io/librariesio/github/blackburn29/lookout)
[![Known Vulnerabilities](https://snyk.io//test/github/blackburn29/lookout/badge.svg?targetFile=package.json)](https://snyk.io//test/github/blackburn29/lookout?targetFile=package.json)
[![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=blackburn29_lookout&metric=alert_status)](https://sonarcloud.io/summary/new_code?id=blackburn29_lookout)

Unofficial Microsoft Outlook client for Linux using [`Electron`](https://electronjs.org/).
It uses the Web App and wraps it as a standalone application using Electron.

## Downloads

Binaries available under [releases](https://github.com/blackburn29/lookout/releases) for `AppImage`, `rpm`, `deb`, `snap`, and `tar.gz`.

In the case of `AppImage`, we recommend using [`AppImageLauncher`](https://github.com/TheAssassin/AppImageLauncher) for the best desktop experience.

We have a dedicated deb and rpm repo at https://outlookforlinux.de hosted with :heart: by [Nils Büchner](https://github.com/nbuechner). Please follow the installation instructions below.

### Debian/Ubuntu and other derivatives
```bash
sudo mkdir -p /etc/apt/keyrings

sudo wget -qO /etc/apt/keyrings/lookout.asc https://repo.outlookforlinux.de/lookout.asc

echo "deb [signed-by=/etc/apt/keyrings/lookout.asc arch=$(dpkg --print-architecture)] https://repo.outlookforlinux.de/debian/ stable main" | sudo tee /etc/apt/sources.list.d/lookout-packages.list

sudo apt update

sudo apt install lookout
```
### RHEL/Fedora and other derivatives
```bash
curl -1sLf -o /tmp/lookout.asc https://repo.outlookforlinux.de/lookout.asc; rpm --import /tmp/lookout.asc; rm -f /tmp/lookout.asc

curl -1sLf -o /etc/yum.repos.d/lookout.repo https://repo.outlookforlinux.de/rpm/lookout.repo

yum update

yum install lookout
```

Also available in:

[![AUR: lookout](https://img.shields.io/badge/AUR-outlook--for--linux-blue.svg)](https://aur.archlinux.org/packages/lookout)

[![Pacstall: lookout-deb](https://img.shields.io/badge/Pacstall-outlook--for--linux--deb-00958C)](https://github.com/pacstall/pacstall-programs/tree/master/packages/lookout-deb)

[![Get it from the Snap Store](https://snapcraft.io/static/images/badges/en/snap-store-black.svg)](https://snapcraft.io/lookout)

<a href='https://flathub.org/apps/details/com.github.blackburn29.outlook_for_linux'><img width='170' alt='Download on Flathub' src='https://flathub.org/assets/badges/flathub-badge-en.png'/></a>

## Configuration and starting arguments

Please check in the config [`README.md`](app/config/README.md) of the config folder for startup or configuration options, to enable or disable certain features or behaviors.

## Running lookout in a firejail

A simple shell script that runs lookout in a firejail is hosted at https://codeberg.org/lars_uffmann/lookout-jailed. The script can be used both to start t4l, as well as to join meetings with an active t4l instance.

## Contributing

Please refer to the [`CONTRIBUTING.md`](CONTRIBUTING.md) file for more information about how to run this application from source, and/or how to contribute.

## Known issues

Known issues and workarounds can be found in the [`KNOWN_ISSUES.md`](KNOWN_ISSUES.md) file.

## History

Read about the history of this project in the [`HISTORY.md`](HISTORY.md) file.

## License

Some icons are from [Icon Duck](https://iconduck.com/sets/hugeicons-essential-free-icons) under the `CC BY 4.0` license.

License: [`GPLv3`](LICENSE.md)
