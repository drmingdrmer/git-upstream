# git-upstream

Manage upstream git repos.

It creates a standalone branch "git-upstream-config-branch" to store config file
thus the extra config file does not mess up other files.

## Install:

-   Copy this script to a dir in PATH.

-   Run following command to create a branch to store config:

        git upstream init

    Edit the configure file.
    Save and checkout to master.

## Configure

Configure file ".gitupstream" syntax:

    <upstream_name_1>     <upstream_url_1>
    <upstream_name_2>     <upstream_url_2>
    ...

Example:

    > cat .gitupstream
    chriswolfvision     git@github.com:chriswolfvision/eplot.git


With above config, "git upstream" will:

-   Add missing remote.
-   Try to set-url for each upstream.
-   fetch -p the upstream repo.
