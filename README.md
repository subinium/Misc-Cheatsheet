# Misc Cheatsheet

> **[한국어 버전 (Korean)](README.ko.md)**

This repo contains the following:

- A collection of development and research tips from experience
- Resources recommended for junior developers
- For those who love the terminal

## Linux

### [Server](linux/server.md)

- Transfer files between servers (`scp`)
- Access localhost externally (`ngrok`)
- Change server password (`passwd`)
- Use remote server ports on localhost (`ssh -L` or `ssh -R`)
- Use server GUI on local machine (`ssh -X` or `ssh -Y`)
- SSH key-based passwordless login (`ssh-keygen`)
- Simplify connections with ssh config (`~/.ssh/config`)

### [GPU](linux/gpu.md)

- Specify GPU for Python (`CUDA_VISIBLE_DEVICES`)
- Check CUDA version (`nvcc`)
- Monitor GPU usage (`nvidia-smi`)
- Monitor GPU usage 2 (`nvtop`)
- Monitor GPU usage 3 (`nvitop`)
- Simpler GPU monitoring (`gpustat`)

### [Util](linux/util.md)

- Prevent laptop from sleeping (`caffeinate`)
- Count files in a directory (`ls -l | grep ^- | wc -l`)
- Check remaining disk space (`df -h`)
- Use cat with syntax highlighting (`bat`)
- Keep directory when opening new tab in iTerm
- Create shortcuts with symbolic links (`ln -s`)
- Suppress pip install output (`pip install` with `-q`, `-qq`, `-qqq`)
- Enable mouse in tmux (`set -g mouse on`)
- Pretty-print JSON files (`jq`)
- Font recommendation (`D2 Coding`)
- Simplified man pages (`tldr`)
- Fuzzy finder for everything (`fzf`)
- Modern ls replacement (`eza`)

### Advanced Utils

- [fig](https://github.com/withfig/autocomplete) : Advanced terminal autocomplete (discontinued, now [Amazon CodeWhisperer for CLI](https://aws.amazon.com/codewhisperer/))
- [say](https://developer.apple.com/library/archive/documentation/UserExperience/Conceptual/SpeechSynthesisProgrammingGuide/FineTuning/FineTuning.html) : macOS built-in TTS command
- [zoxide](https://github.com/ajeetdsouza/zoxide) : Smarter `cd` command that learns your habits
- [starship](https://starship.rs/) : Fast, customizable cross-shell prompt

### [Vim](linux/vim.md)

- **[Combined vimrc](linux/.vimrc)**
- (vimrc) File type detection and syntax highlighting (`syntax on`, `filetype indent plugin on`)
- (vimrc) Highlight search results, brackets, etc. (`hlsearch`, `ruler`, `showmatch`)
- (vimrc) Convenient settings for Python editing (tab sizes, `autoindent`)
- (vimrc) Show line numbers (`nu` or `number`)
- (vimrc) Change cursor shape per mode
- Multi-line commenting in vim (`norm i#`, `norm 1x`)
- Save with sudo in vim (`w sudo! tee %`)

### [Git/Github](/linux/github.md)

- Github Profile Badge List: Customize your GitHub profile with badges
- Create and checkout a branch in one step (`git checkout -b` or `git switch -c`)
- Change commit date (`git commit --amend --no-edit --date`)
- Prevent Korean character errors (`core.precomposeunicode`, `core.quotepath`)

## Data Science

### Computer Vision

- [albumentations](https://github.com/albumentations-team/albumentations) : Image data augmentation library
- [ttach](https://github.com/qubvel/ttach) : Image Test Time Augmentation with PyTorch
- [timm](https://github.com/rwightman/pytorch-image-models) : PyTorch pre-trained SOTA image models
- [smp](https://github.com/qubvel/segmentation_models.pytorch) : PyTorch pre-trained SOTA image segmentation models

### Prototype

- [Streamlit](https://github.com/streamlit/streamlit) : Open-source tool to easily build web-based GUIs for ML models
- [Gradio](https://github.com/gradio-app/gradio) : Open-source tool to easily build web-based GUIs for ML models

### Tools

- [Jupyter Lab](https://jupyterlab.readthedocs.io/en/stable/getting_started/installation.html) : Next-generation Jupyter Notebook
- [Weights & Biases](https://wandb.ai/) : Web dashboard, more convenient than TensorBoard

### ETC

- [watermark](https://github.com/rasbt/watermark) : Jupyter extension to display library versions
- [holidays](https://github.com/dr-prodigy/python-holidays) : Get public holidays. Useful for time series data
- [pprint](https://docs.python.org/3/library/pprint.html) : Built-in library for pretty-printing

## Web

### [Flask](web/flask.md)

- What to do when Flask cache prevents refresh?

### Library & Service

- [Vercel](https://vercel.com/) : Easy deployment service

- CSS/Styles
  - [Tailwind UI](https://tailwindui.com/) : Utility-first CSS framework
  - [Headless UI](https://headlessui.dev/) : UI components designed for use with Tailwind UI
  - [Chakra UI](https://chakra-ui.com/) : User-friendly UI framework (recommended)
  - [Chakra Templates](https://chakra-templates.dev/) : Pre-built components made with Chakra
- React
  - [Reactour](https://github.com/elrumordelaluz/reactour) : Onboarding tour package for React
  - [react-i18next](https://github.com/i18next/react-i18next) : Internationalization package for React

### Data Visualization (JS)

- [D3](https://d3js.org/) : For users who want full customization
- [Plotly](https://plotly.com/) : Also available in Python
- [Recharts](https://recharts.org/)
- [Chart.js](https://www.chartjs.org/)
- [Highcharts](https://www.highcharts.com/)

## Tool

### Website

- Open Source
  - [Codepen](https://codepen.io/) : HTML/CSS/JS code snippet sharing site. Great for learning techniques from others
- Writing
  - [Thesaurus.com](https://www.thesaurus.com/) : Synonym dictionary
  - [Grammarly](https://app.grammarly.com/) : Grammar checker
  - [Korean Spell Checker](http://speller.cs.pusan.ac.kr/) : Please run this at least once on any Korean document...
- Design
  - [flaticon](https://www.flaticon.com/) : Royalty-free icons
  - [Unsplash](https://unsplash.com/) : Royalty-free images
  - [dafont.com](https://www.dafont.com/) : Free English fonts
  - [carbon](https://carbon.now.sh/) : Create beautiful code snippets for sharing
  - [2 Color Combinations](https://2colors.colorion.co/) : Useful for exploring 2-color combos in visualization/UI
- Trends
  - [GeekNews](https://news.hada.io/) : Great for following the latest dev/tech/startup news
  - [Product Hunt](https://www.producthunt.com/) : Platform for sharing startup products. Browse the latest SaaS and more
  - [Disquiet](https://disquiet.io/) : Platform connecting makers. Can be used similarly to Product Hunt
- ETC
  - [Ghost](https://ghost.org/) : Paid blogging platform if you don't like GitHub Pages or Tistory
  - [StackShare](https://stackshare.io/) : Tech stack sharing platform

### Note Taking

- [Notion](https://www.notion.so/) : The go-to note-taking tool
  - [oopy](https://www.oopy.io/) : Turn Notion pages into websites
- [Obsidian](https://obsidian.md/) : Tool with features similar to Roam
- [Craft](https://www.craft.do/) : Similar to Notion, cleaner feel on macOS
- [Bear](https://bear.app/) : Lightweight markdown tool
- [Roam Research](https://roamresearch.com/) : Graph-based markdown note-taking tool

### VSCode Extension

- [Sync VSCode settings with GitHub account](https://code.visualstudio.com/docs/editor/settings-sync)
- [GitLens](https://github.com/Axosoft/vscode-gitlens) : View git history forward/backward in VSCode

### Chrome Extension

- [Arxive](https://chrome.google.com/webstore/detail/arxive/hkoblclipggkhhbllgefhnbjdcajmelh/related?hl=ko) : Renames Arxiv paper titles from year-based to title-author format
- [Google Scholar Button](https://chrome.google.com/webstore/detail/google-scholar-button/ldipcbpaocekfooobnbcddclnhejkcpn?hl=en) : Search Google Scholar directly from the extension

### Application

- [Todoist](https://todoist.com/) : Todo list manager - great usability
- [TickTick](https://ticktick.com/) : Todo list manager - feature-rich
- [Mathpix Snip](https://mathpix.com/) : Convert math equation screenshots to LaTeX
- [1password](https://1password.com/) : Password manager
- [Habitica](https://habitica.com/) : Gamified habit/routine tracker

## Articles & Repo

- Articles
  - [Oh Wook-hwan, For Young Scholars Pursuing Academia as a Career](http://home.ewha.ac.kr/~oookwhan/essay/essay2-toyoung.htm) : Recommended reading for grad students
  - [A Junior Developer's Resume Writing Guide](https://techblog.woowahan.com/2531/) : Recommended for first-time CV writers (Korean)
  - [subicura's blog: Setting Up a macOS Dev Environment](https://subicura.com/2017/11/22/mac-os-development-environment-setup.html) : Mac initial setup guide (Korean)
- Repos
  - [Modern Unix](https://github.com/ibraheemdev/modern-unix) : Collection of awesome modern CLI tools
  - [awesome-devteam](https://github.com/leehosung/awesome-devteam) : Resources for building great dev teams (Korean)
- YouTube & Videos
  - [Ali Abdaal](https://www.youtube.com/channel/UCoOae5nYA7VqaXzerajD0lg) : Productivity YouTube channel
  - [How Great Leaders Inspire Action](https://www.ted.com/talks/simon_sinek_how_great_leaders_inspire_action/up-next?language=en) : Simon Sinek's TED talk on the Golden Circle. Why you should start with "Why"
- Books
  - [Tools of Titans (Tim Ferriss)](https://shopping.interpark.com/product/productInfo.do?prdNo=8577355413) : For those who want to grow
  - [Soft Skills (John Sonmez)](http://www.yes24.com/Product/Goods/23161141) : Diverse advice on skills developers need beyond coding
  - [Free to Focus (Michael Hyatt)](http://www.kyobobook.co.kr/product/detailViewKor.laf?mallGb=KOR&ejkGb=KOR&barcode=9791135465512) : Rethink productivity and make your life freer
