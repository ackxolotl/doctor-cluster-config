All hostnames can be looked up in [./hosts](./hosts). Most of the servers are in
[TU Munich](docs/tum). Some machines are in [Edinburgh](docs/edinburgh).

# Update all servers

1. Install [pyinvoke](https://github.com/pyinvoke/invoke) and rsync via pip or load via `nix develop`
2. Choose a deployment target:


``` console
$ inv -l
Available tasks:

  cleanup-gcroots
  deploy-doctor      Deploy to rpi4, that is used to control power relay
  deploy-edinburgh   Deploy to edinburgh servers starting with rose
  deploy-tum         Deploy to TUM servers
  reboot             Reboot hosts. example usage: fab --hosts clara.r,donna.r reboot
```

3. Run!

``` console
$ inv deploy-tum
```

# Add new users

Add chair members to [./modules/users.nix](./modules/users.nix) and students to [./modules/students.nix](./modules/students.nix).

For chair members use a uid in the 1000-2000. For new students use a uid in the
2000-3000 range. Check that the uid is unique across both files and in the
range between to avoid conflicts.

# Add new servers

For installing new servers, see [Add servers](docs/ADD_SERVER.md).

# Update system

We use [flakes](https://nixos.wiki/wiki/Flakes) to manage 
nixpkgs versions. To upgrade use:

``` console
$ nix flake update
```

Than commit `flake.lock`.

# Home-manager

To install home-manager for a user simply run:

``` console
$ nix-shell '<home-manager>' -A install
```

This will initiate your home-manager and will generate a file similar to the one in ```home/.config/nixpkgs/home.nix```

# Visual Studio Code Server support in NixOS

You can use [this](https://github.com/msteen/nixos-vscode-server) to enable support for VS Code Server in NixOS.

An example of the ```home.nix``` configured for VS Code support is shown in ```home/.config/nixpkgs/home.nix```.


# IPMI

On all new TUM rack machines we have IPMI support!!!

Generally, you can find the IPMI web interface at
`https://$HOST-mgmt.dse.in.tum.de/` (i.e. https://bill-mgmt.dse.in.tum.de)
once the device has been installed in the rack.  These addresses are only
available through the management network, so you must use the [RBG
vpn](https://vpn.rbg.tum.de/) for il1 to access them.

You can also retrieve the IP addresses assigned to the IPMI/BMC firmware by
running:

```
ipmitool lan print
```

on the machine. On the other host (i.e. your laptop) you can run the following command to get a serial console:

```
$ ipmitool -I lanplus -H <ipmi-ip-address> -U ADMIN -P "$(sops -d --extract '["ipmi-passwords"]' secrets.yml)" sol activate
```

The following will reboot the machine:

```
$ ipmitool -I lanplus -H <ipmi-ip-address> -U ADMIN -P "$(sops -d --extract '["ipmi-passwords"]' secrets.yml)" power cycle 
```

The IPMI password here is encrypted with
[sops](https://github.com/mozilla/sops). To decrypt it on your machine, your
age/pgp fingerprint must be added to `.sops.yaml` in this repository. And one of
the existing users must re-encrypt `secrets.yml` with your key. 

Then press enter to get a login prompt. The root password for all machines is
also stored in [secrets.yaml]().

# Monitoring

Hosts are monitored here: https://grafana.thalheim.io/d/Y3JuredMz/monitoring?orgId=1

# CI

All machines are build by [gitlab ci](https://gitlab.com/TUM-DSE/doctor-cluster-config/-/pipelines) on a
self-hosted runner. Gitlab will also propagate the build status to the github repository eventually. 
The resulting builds are uploaded to https://tum-dse.cachix.org from where
machines can download them while upgrading.
