# Ergonaut One (Unofficial) ZMK Module

This repository contains the board files for the [Ergonaut One](https://github.com/ergonautkb/one) to allow users to build firmware. 
This can be done by adding the module to the west.yml found in your zmk-config's config directory. 
There is a full guide available for this here: [ZMK Modules Doc](https://zmk.dev/docs/features/modules)

> [!IMPORTANT]
> This is an unofficial ZMK module which contains specific features for my setups. It may even lack some necessary functionality
> for your needs. Consider using [the official module](https://github.com/ergonautkb/one-zmk-module) instead.

## Usage

Edit your west.yml file found in your zmk-config's config directory to add the Ergonaut One module. Example:

```
manifest:
  remotes:
    - name: zmkfirmware
      url-base: https://github.com/zmkfirmware
    - name: proostas
      url-base: https://github.com/proostas
  projects:
    - name: zmk
      remote: zmkfirmware
      revision: main
      import: app/west.yml
    - name: one-zmk-module
      remote: proostas
      revision: main
  self:
    path: config
```
Once you have the module added to your west.yml you can then build firmware as if it were in your config's shield directory or in ZMK main.
