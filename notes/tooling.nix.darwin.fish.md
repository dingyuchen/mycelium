---
id: aeyep204nrqd1svsek50ilw
title: Fish
desc: ''
updated: 1667461613883
created: 1667460877998
---

## Default shell

In `darwin-configuration.nix`, set
```
environment.shells = [ pkgs.fish ];
```
This should add `/run/current-system/sw/bin/fish` into `/etc/shells`.
Supposedly this avoids some problems with setting your default shell later.

Now also in `darwin-configuration.nix`, set 
```
users.users.<username>.shell = pkgs.fish;
```

If also using `home-manager`, set
```
programs.fish.enable = true;
```
in `home-manager.users.<username>`

### Aliases

I use a shortcut `ds` to trigger `darwin-rebuild switch`, and `ls` as `exa --icons`.
```
shellAliases = {
    ds = "darwin-rebuild switch";
    ls = "exa --icons";
}
```