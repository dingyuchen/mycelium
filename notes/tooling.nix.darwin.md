---
id: 6kkz0xmm5hm3yr3oqhyy4k6
title: Nix Darwin
desc: ''
updated: 1667459159994
created: 1666425579784
---

##  Why

Nix darwin brings the configuration.nix part of NixOS to macOS.
I think its a good starting point to find out more about the nix ecosystem and framework.

The main usecase for vanilla nix would be to create hermetic development environments, but that is not immediately necessary in the case of the work laptop, since most of the versioning and environment management is already handled by `spkit` and `make`.

Furthermore, it makes more sense to use `nix-darwin` to replace the base environment before setting up repo-specific `nix-shell`s to maintain the developer experience.

## Setting Up

```
darwin-rebuild switch -I darwin-config=dotfiles/darwin-configuration.nix
```
This sources the custom configuration. `ds` can be used as per normal after.


## Appendix

### GUI Apps

> Currently only system-level GUI apps are only linked into `~/Applications`
>
> Refer to https://github.com/LnL7/nix-darwin/issues/276

### FHS

[FHS](https://en.wikipedia.org/wiki/Filesystem_Hierarchy_Standard) versions of `vscode` and `vscodium` are not supported on macOS.
There is also no need to use the FHS versions, since GUI apps are better managed as `brew casks` at this point in time anyway.

## PatchELF