+++
title = "GitTips"
author = ["Prasad Ghole"]
date = 2025-04-20T00:00:00+05:30
layout = ""
linkTitle = ""
markup = ""
slug = ""
tags = ["git"]
type = ""
url = ""
draft = false
toc = false
summary = "Git tool tips"
+++

## Working with Forked repos {#working-with-forked-repos}


### Merge changes from forked repo {#merge-changes-from-forked-repo}

For my neovim kickstart I have forked the <https://github.com/nvim-lua/kickstart.nvim.git> to sync my changes with this branch I need to regularly merge this branch master changes.

{{< highlight shell >}}
git remote add upstream https://github.com/nvim-lua/kickstart.nvim.git

git fetch upstream

# Checkout my branch in this case names are same 
git checkout master 

# Merge the original upstream
git merge upsteam/master 
{{< /highlight >}}


## Git Push {#git-push}

Instead of providing branch name or set upstream branch we can always push current branch by

{{< highlight shell >}}
git config --global push.autoSetupRemote true
{{< /highlight >}}

