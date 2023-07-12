## Installing Nix: the package manager (Linux)
There are two ways of installing **Nix** - multi-user vs single-user. Multi-user installation is recommended over single-user since it ensures better isolation and sharing of build with other users. Cons are root is needed and it's harder to uninstall. Choose your preferred way based on your requirements.

- ### Multi-user installation
```
sh <(curl -L https://nixos.org/nix/install) --daemon
```

- ### Single-user installation
```
sh <(curl -L https://nixos.org/nix/install) --no-daemon
```

#### To test if it's working correctly, run
```
nix-env --version
```
