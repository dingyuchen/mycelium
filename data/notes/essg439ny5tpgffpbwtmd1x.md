- [How to Learn Nix, Part 1: What's all this about?](https://ianthehenry.com/posts/how-to-learn-nix/introduction/)

    - I gave Nix another try recently,

- [How to Learn Nix, Part 2: Prior knowledge](https://ianthehenry.com/posts/how-to-learn-nix/prior-knowledge/)

    - I remember there being a total of three different ways to get software on my NixOS box:
        - System-wide services, like `sshd` or `nginx` that are run by systemd. These are declared in the file `/etc/nixos/configuration.nix` and NixOS installed them (somehow).
        - User software that I use interactively, like `rg` or `git`. I installed these commands with `nix-env -i` on a per-user basis.
            - > so is this the difference between `nix-env -iA` and `nix-env -i` ?
        - Project-specific software, only visible when running in a `nix-shell`. Declared in a file called `shell.nix` in the project’s directory. This is where I would put things like `rustc` or whatever – all the build dependencies for a project.
            - > This feels like the biggest value proposition of Nix, but also entirely useless at my current point in life, since my work deals with `Go` exclusively.

- [How to Learn Nix, Part 3: What we talk about when we talk about Nix](https://ianthehenry.com/posts/how-to-learn-nix/glossary/)

    - I decide to start learning Nix by reading through the glossary.
        - > sldkfjsk
