# XA Extensions
**XA Extensions** is a set of extensions for **Sitecore Experience Accelerator** module.

The main goal of this solution is to show how you can integrate with **SXA** by creating custom modules.

Solution uses [Helix](http://helix.sitecore.net/)

# Extensions
### ToolboxSearchBox
Toolbox Search Box solves a problem of searching a proper toolbox section which contains rendering that you want to add to the page.
[Read more](https://alan-null.github.io/2017/05/sxa-toolbox-searchbox)

![ToolboxSearchBox demo](https://alan-null.github.io/images/posts/sxa-toolbox-searchbox/demo.gif)


### MultisiteManagement

Multisite Management solves a problem of manual removal and helps you to easy and quickly clean up your database.
[Read more](https://alan-null.github.io/2017/05/sxa-multisite-management)

![MultisiteManagement demo](https://alan-null.github.io/images/posts/sxa-multisite-management/demo.gif)

# Installation
## Clone Repository
Open command line and run following command
```
clone https://github.com/alan-null/XA.Extensions.git
```
## Install Sitecore & SXA
The next step is to create a new Sitecore instnace and then install SXA package.

Current **XA.Extensions** project is compatible with:

| Product   |      Version      |  Revision |
|----------|:-------------:|:------:|
| Sitecore |  **8.2** | rev. 170407 |
| SXA  |  **1.3** | rev. 170412 |


## Environment specific configs

1. Open repository root.
2. Make a copy of following files and remove `.example` from the file name:
   * `publishsettings.targets.example`,
   * `zzz.XA.Extensions.config.example`
3. Fill file content of each file with your settings
   * `publishsettings.targets` - set **publishUrl**. This is your site name (IIS site name),
   * `zzz.XA.Extensions.config` - set value of Sitecore variable named **sourceFolder**. Variable should point to the *src* folder from **XA.Extensions** repository


## Build and publish
- Open *PowerShell Console* as **Administrator**
- Navigate to **XA.Extensions** repository root
- Execute

 ```powershell
.\publish.ps1
```

**Alternative way:**

You can build whole solution using Visual Studio and publish selected projects using *WebPublish* (hit `Alt + B + H` and select publish).