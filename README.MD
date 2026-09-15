<div align="center">
<img src="/images/THIRD-PATCH-LOGO.png" style="width: 300px; height: auto;" />
</div>

# ThirdPatch - Third-Party Patch Management for MSPs

## Intro
<div style="text-align: center;"> <a href="https://thirdpartypatching.com/">ThirdPatch Website</a> |
<a href="https://gallery.thirdpatch.com/">Package Gallery</a> |
<a href="https://docs.thirdpartypatching.com/">ThirdPatch Docs</a> </div>

ThirdPatch™ is an RMM-neutral solution for deploying and patching third-party software. It's designed for MSPs, and uses a package-based architecture to manage software in groups instead of app-by-app logic.

### Features
- Compatible with any RMM
- Application Library of 10,000+ apps
- Flat-rate pricing (no per-app or per-endpoint charges)
- Agentless client architecture for maximum security
- Architecture designed to be flexiable for MSP usecases

## Demo
This demo walks though installing ThirdPatch, using it to install applications, and using it to update those applications.


#### Install ThirdPatch

Run the following command in PowerShell as Administrator to install the ThirdPatch client:

    Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; if (!(Test-Path \"$env:PROGRAMDATA\\thirdpatch\\bin\\thirdpatch.exe\")) {iex ((New-Object System.Net.WebClient).DownloadString('https://thrdpt.ch/install'))}; thirdpatch source add -n="ThirdPatch Demo" -s="https://livedemo.thirdpatch.com/repository/community/"

#### Install Apps

In the same terminal, run this command to install a specific version of the Chromium web browser ([the open-source part of Google Chrome](https://www.chromium.org/Home/)):

    thirdpatch install chromium --version 150.0.7871.187

#### Update Apps

Run this command to update Chromium (and any other apps) to the latest version:

    thirdpatch upgrade

#### Uninstall Apps

This command will remove Chromium:

    thirdpatch uninstall chromium


## More

We have a full-length webinar covering ThirdPatch here:

[![Watch the video](https://i.ytimg.com/vi/ebEdAhuB4PY/hqdefault.jpg?sqp=-oaymwEnCNACELwBSFryq4qpAxkIARUAAIhCGAHYAQHiAQoIGBACGAY4AUAB&rs=AOn4CLDAgMw6AUGY2FQJBzfDhQSb2uELqQ)](https://youtu.be/ebEdAhuB4PY?si=yZe15kBDoBxnemHu)