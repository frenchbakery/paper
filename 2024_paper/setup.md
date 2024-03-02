# Editing Setup

This document describes the editor setup used to create the paper.

(Maybe not: https://medium.com/@rcpassos/writing-latex-documents-in-visual-studio-code-with-latex-workshop-d9af6a6b2815)

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

Alternatively, this can be done from command line:

```bash
miktexsetup finish
```

Guide on how to use MiKTeX Console: https://miktex.org/howto/miktex-console


### VSCode LaTeX Workshop

Install this extension: james-yu.latex-workshop

