# Nix notes

This is a collection of short notes about Nix and NixOS. Almost each note
corresponds to a page, to a Git commit, and to a Nix attribute that can be
built.

The result is a virtual machine image that actually runs as
[noteed.com](https://noteed.com).


## How to read these notes

The notes should be read with a copy of this repository. To make each note
correspond to a commit, this repository is heavily rebased. When studying a
particular note, especially the first ones, it is best to checkout the
corresponding commit to see only the relevant files for that note.

In other words, running `git log --patch --reverse` should be a readable
tutorial about Nix and NixOS. Indeed, the following table of content is
generated with `git log --reverse`!


## Bleeding edge

Note: building Digital Ocean images is a recent addition to nixpkgs, and
uploading a custom image is a recent feature of `doctl`. Assuming `../nixpkgs`
is a recent checkout (around 2019-12-13), I'm using a Nix shell like this:

```
$ NIX_PATH=nixpkgs=../nixpkgs nix-shell -p doctl
```


## Table of content


### Start here: building a Digital Ocean image

In this commit, we introduce a short Nix expression to build a virtual machine
image that can be run on Digital Ocean. The expression is short because all the
machinery to do the heavy lifting is in nixpkgs. [More.](site/image.md)