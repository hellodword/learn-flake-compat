```sh
# devShells.<system>.default
nix-shell
nix develop --extra-experimental-features nix-command --extra-experimental-features flakes

# devShells.<system>.dev
nix develop --extra-experimental-features nix-command --extra-experimental-features flakes .#dev

# packages.<system>.default
nix shell --extra-experimental-features nix-command --extra-experimental-features flakes

# packages.<system>.dev
nix shell --extra-experimental-features nix-command --extra-experimental-features flakes .#dev

# apps.<system>.default
# packages.<system>.default
echo hello | nix run --extra-experimental-features nix-command --extra-experimental-features flakes

# apps.<system>.dev
# packages.<system>.dev
echo hello | nix run --extra-experimental-features nix-command --extra-experimental-features flakes .#dev

# packages.<system>.default
nix-build
nix build --extra-experimental-features nix-command --extra-experimental-features flakes

# packages.<system>.dev
nix build --extra-experimental-features nix-command --extra-experimental-features flakes .#dev
```
