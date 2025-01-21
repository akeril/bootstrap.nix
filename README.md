# bootstrap.nix

A simple bash script to help bootstrap NixOS installations. 

NixOS is a Linux distribution where everything is described as code, with one exception: during installation, the disk partitioning and formatting are manual steps. **disko** aims to correct this sad omission.

**bootstrap.nix** brings the NixOS installer and Disko together, enabling system installations with a single command.

## Usage

You need a flake which exposes both a `diskoConfiguration` and a `nixosConfiguration`. 

Run the following command:

```bash
nix --experimental-features 'nix-command flakes' run github:akeril/bootstrap.nix -- -f FLAKE_URI
```

Replace `FLAKE_URI` with the URI of your flake.


