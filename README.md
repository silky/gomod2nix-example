# Nix/Go setup

A simple nix flake (following [gomod2nix](https://github.com/nix-community/gomod2nix)) that shows how to
compile/run a go project with Nix via flakes.

### Pre-requisites

Install [Nix](https://nixos.org/download.html) and enable
[flakes](https://nixos.wiki/wiki/Flakes).

To install nix see: <https://nix.dev/tutorials/install-nix>.

Then, enable flakes by editing `~/.config/nix/nix.conf` and adding the
following line:

```
# In ~/.config/nix/nix.conf
experimental-features = nix-command flakes
```

Then, you can get a development environment by running `nix develop` in this
folder.

### Building

```
nix build
```

### Running

```
nix run
```

### Trivia

- You can add arbitrary programs to the shell by editing the <./shell.nix>
file appropriately. You can see that we've added `nodejs`.
- You can use [direnv](https://direnv.net/) to always enter the default shell
when you enter the folder. For more advanced usage, you can also use
[nix-direnv](https://github.com/nix-community/nix-direnv) so it's super
fast/cached. This is preferred.
