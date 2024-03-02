# Editing Setup

This document describes the editor setup used to create the paper.

https://www.geekering.com/programming-languages/filipesalgueiro/how-to-write-latex-documents-using-visual-studio-code/

## Installation

### MiKTex

This is the underlying system for managing TeX packages.

https://miktex.org/download

Debian:

```bash
curl -fsSL https://miktex.org/download/key | sudo tee /usr/share/keyrings/miktex-keyring.asc > /dev/null
echo "deb [signed-by=/usr/share/keyrings/miktex-keyring.asc] https://miktex.org/download/debian bookworm universe" | sudo tee /etc/apt/sources.list.d/miktex.list

sudo apt update
sudo apt install miktex
```

Setup completion:

- Open MiKTeX Console
- Select "Finish private setup"
- After restart it may say: "A MiKTeX Setup issue has been detected. So Far you have not checked for MiKTeX updates. Remedy: Check for MiKTeX updates."
- If so, click ok, navigate to updates and click "Check for updates" and then "Update now"
- For automatic package installation, go to Settings and for Package Installation -> Automatic installation choose "Always"

Alternatively, this can be done from command line:

```bash
miktexsetup finish  # finish private setup
initexmf --set-config-value [MPM]AutoInstall=1  # enable auto install
```

Guide on how to use MiKTeX Console: https://miktex.org/howto/miktex-console


### VSCode LaTeX Workshop

Install this extension: james-yu.latex-workshop

After that, simply put your .tex file in a folder and it can be edited. Compilation happens with green run arrow in top right.

## Links, Info and Wrigin

[Call for Papers](info/2024-Call-for-Papers.pdf) describes what is requested.<br>
(also available [online](https://ecer.pria.at/wp-content/uploads/2024/01/2024-Call-for-Papers.pdf))

The [IEEE Conferencing paper template](https://www.ieee.org/conferences/publishing/templates.html) should be used.

This document describes how to use the template and how a paper should be written with it: https://mirror.easyname.at/ctan/macros/latex/contrib/IEEEtran/IEEEtran_HOWTO.pdf

It is most important that the .tex document starts with this:

```tex
\documentclass[conference]{IEEEtran}
```





