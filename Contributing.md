# Contributing Guide

This contains a guide for how to setup your computer, and the basic tools you'll need for any single project

# Tools You'll Need

1. A Git Client - use your favourite (like [GitHub for Desktop](https://desktop.github.com) or [SourceTree](https://www.sourcetreeapp.com/)), or if you'd rather stick to a terminal, pick up the [git terminal client](https://git-scm.com/downloads)

## Back End

1. Install the [dotnet SDK](https://dotnet.microsoft.com/download) which matches your operating system

1. Install [Powershell Core](https://github.com/powershell/powershell#get-powershell) (also known as Powershell 6)

1. Some of our applications require secret keys that only trusted developers have access to. If you want access to these keys, please get in contact with another member of the team who will give you the keys, and show you how to keep them out of source control

1. Install [SQL Server](https://www.microsoft.com/en-gb/sql-server/sql-server-downloads). This is a long process that depends entirely on your specific platform. If you're on OS X, you'll need to install the docker container version (which means you'll also need [docker](https://hub.docker.com/editions/community/docker-ce-desktop-mac))
  > [Windows Installation Guide](https://docs.microsoft.com/en-gb/sql/database-engine/install-windows/install-sql-server-from-the-installation-wizard-setup?view=sql-server-2017). Be sure to take specific care at step 13 to set the Instance ID to `MSSQLSERVER`
  > [Ubuntu Installation Guide](https://docs.microsoft.com/en-gb/sql/linux/quickstart-install-connect-ubuntu?view=sql-server-2017). Be sure to take specific care to set the default Instance ID to `MSSQLSERVER`
  
1. Install [Azure Data Studio](https://docs.microsoft.com/en-us/sql/azure-data-studio/download?view=sql-server-2017)

## Front End

1. Install [NodeJS](https://nodejs.org/en/download/)

1. Make sure you're running the latest npm version. If you're on Linux or OS X, follow [this guide](https://stackoverflow.com/a/6237400/5952236). If you're on Windows, follow [this guide](https://stackoverflow.com/a/31520672/5952236)

1. Install [Visual Studio Code](https://code.visualstudio.com/Download)

1. Install the [Debugger For Chrome](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-chrome) VS Code Extension

Other Visual Studio Code extensions that we recommend, but are not required are as follows:
1. [Angular Language Services](https://marketplace.visualstudio.com/items?itemName=Angular.ng-template)
1. [Beautify](https://marketplace.visualstudio.com/items?itemName=HookyQR.beautify)
1. [C#](https://marketplace.visualstudio.com/items?itemName=ms-vscode.csharp)
1. [GitLens](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens)
1. [IntelliSense for CSS class names in HTML](https://marketplace.visualstudio.com/items?itemName=Zignd.html-css-class-completion)
1. [npm](https://marketplace.visualstudio.com/items?itemName=eg2.vscode-npm-script)
1. [Path IntelliSense](https://marketplace.visualstudio.com/items?itemName=christian-kohler.path-intellisense)
1. [Powershell](https://marketplace.visualstudio.com/items?itemName=ms-vscode.PowerShell) - though we recommend that if you're on Windows, you change the powershell to use from Powershell 5 to  Powershell 6 (powershell core)
1. [VS Live Share](https://marketplace.visualstudio.com/items?itemName=MS-vsliveshare.vsliveshare)
1. [VS Live Share Audio](https://marketplace.visualstudio.com/items?itemName=MS-vsliveshare.vsliveshare-audio)

## Dev Ops

1. Install [Powershell Core](https://github.com/powershell/powershell#get-powershell) (also known as Powershell 6)

1. Build tools you'll need may include NodeJS and npm (see Front End above) as well as dotnet (see Back End above)

1. Travis-CI scripts can use Linux and Unix specific tools like `curl` and `zip`, which are not available on Windows. Equivalents can be found relatively easily, however, it is recommended that you test these in a Linux VM.
  > If you're on Windows, you can use any Linux VM you like, but we recommend [Windows Subsystem for Linux](https://docs.microsoft.com/en-us/windows/wsl/install-win10) with an Ubuntu distro

# Submitting a Change

1. Always create a PR for your change - never directly push your changes to `develop` or `master` branch

1. We generally don't accept PRs that don't have an associated issue. If you think there's a change that needs to happen - submit an issue first! There's a chance that someone's already working on it, or that it's worth reviewing by the team first

1. When you're ready to start work, clone the repository onto your local development environment

1. Make sure you're on the `develop` branch before you begin

1. Create a new branch from `develop` with the naming convention of `issue/{ticket #} - {ticket title}` where `ticket #` is replaced with the issue ID, and {ticket title} is replaced by the title of the ticket

1. Make all your changes in this branch

1. Submit a new PR to the `develop` branch with all your changes in. Leave any comments or notes that you want to, if you feel that it would be helpful for us

1. We'll approve or reject and comment on your change. If we reject it - we'll always explain why

# Code of conduct

We follow a strict code of conduct. Please read it [here](Code_of_Conduct.md) before making any community contributions (including comments)

# Most importantly though
From the team at Phoenix Apps Ltd,  
Thank you
