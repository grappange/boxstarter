# Boxstarter

[Boxstarter](http://boxstarter.org/) setup scripts for setting up a customized windows environment in a completely unattended manner using PowerShell and [Chocolatey](https://chocolatey.org/) packages. The [Devenv.ps1](roles/Devenv.ps1) boxstarter script installs my development environment for C#.Net and Java/Scala web development. Beyond unattended software installs, boxstarter will set:

* Explorer Options: Show hidden files/folders, Show file extensions
* Taskbar Options: Small taskbar, always combine taskbar buttons
* Set PowerShell execution policy to "Unrestricted"
* Install all pending Windows Updates
* Install Microsoft Hyper-V virtualization



## Getting Started
### Web Installer

Invoke the Boxstarter WebLauncher by pasting to the URL below in Internet Explorer or by invoking it as a START command in either the Command prompt or PowerShell:

```
START http://boxstarter.org/package/nr/url?https://raw.githubusercontent.com/bcowdery/boxstarter/master/roles/Devenv.ps1
```

*You can use any browser that supports "Click Once" applications. This is limited to IE unless you add extensions to [Chrome](https://chrome.google.com/webstore/detail/clickonce-for-google-chro/kekahkplibinaibelipdcikofmedafmb) and [Firefox](https://addons.mozilla.org/en-us/firefox/addon/fxclickonce/). You can also use the Command prompt or a Powershell console, both using the same command as long as IE is your default browser. This is rarely an issue as IE is the most common default on new machines anyways.*


### Command Line
You can also run the installer scripts from a local clone of this repository using the `install [role]` command. This script will install Chocolatey and the Boxstarter shell before running the Boxstarter package.

```
> install Devenv
```


## Troubleshooting

**Allow Empty Checksums**

Occurs on newer versions of Boxstarter and Chocolatey due to a [recent Update](https://github.com/mwrock/boxstarter/issues/198). This can be fixed by downgrading Chocolatey to version 0.9.10.3.

```
choco upgrade chocolatey --version 0.9.10.3 --allow-downgrade
```
