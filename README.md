### `zmk-config` Setup

I wanted to build multiple similar boards from the same branch, sharing as much configuration as I could. One aspect of this included moving all of the common behavior definitions into a [`shared.dtsi` file](./config/shared.dtsi), included in all of my keymaps, and using an `.override` file where I needed to adjust some of those nodes for a board (e.g. [the Planck](./config/planck_overrides.dtsi). I also had similar boards with different features (with and without display, for instance), and wanted distinctly named build artifacts, so instead of using the usual `build.yaml`, I added a new GitHub workflow for each distinct build configuration and created [separate `*.yaml` files](./.github/workflows) for each of those.

I also added a [separate workflow](./.github/workflows/draw-keymaps.yml) for `keymap-drawer`, to automatically produce keymap diagrams like the one below for any changes.

### Articles

- [Soldering](https://araxia.net/keyboards/soldering/): resources for soldering, particularly relevant for keyboards
- [Bespoke Solder Feeder](https://araxia.net/keyboards/solder-feeder/): a tool for feeding solder smoothly and evenly when soldering electronics
- [Keybinding Inventory](https://araxia.net/keyboards/keybindings-inventory/): all the bindings I want to accommodate on my keymaps
- [Magnetic Mounting Guide](https://araxia.net/keyboards/magnetic-mount/): guide for magnetic keyboard mounting/tenting
- [nice!view CS Pin Bodge](https://araxia.net/keyboards/nice-view-bodge): guide for adding a nice!view to a board without support for that display
- [My Keyboards](https://araxia.net/keyboards/my-keyboards): my keyboard inventory
- [Coconut Planck](https://araxia.net/keyboards/coconut-planck): transformation of Planck from `4x12` to `3x5+3(+12)`
- [Swept Corne](https://araxia.net/keyboards/swept-corne): write-up of my early experiences with a Swept Corne

### Current Keymap

I have transitioned from a `3x6+3` Corne layout to a `3x5+2`, still occasionally using `+3` on some boards. I have repurposed the now-unused outer pinky columns on my current Corne boards for activating modal layers for mouse pointer control and Discord use.

I generally test any new changes in ZMK and later port them to my [QMK config](https://github.com/SethMilliken/qmk_firmware/commits/seth) if I like them enough.

[![Split Keyboard Keymap](https://raw.githubusercontent.com/SethMilliken/swept-corne-zmk/seth/svg/corne.svg)](https://raw.githubusercontent.com/SethMilliken/swept-corne-zmk/seth/svg/corne.svg)

