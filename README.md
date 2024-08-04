# QMK Userspace

My QMK external userspace where personal customization resides.
The most significant customization is support for Vial.

## Development

The instruction below assumes you are already familiar with building QMK firmware and
have necessary dependencies (e.g., compiler toolchain for your target MCU) installed on your local machine.

1. Clone the repository with submodules: `git clone --recursive https://github.com/yudai-nkt/qmk_userspace.git `
1. Configure QMK CLI so that it can consume correct directories.
    - Enable userspace: `qmk config user.overlay_dir="$(realpath qmk_userspace)"`
    - Point `user.qmk_home` to the Vial submodule: `qmk config user.qmk_home="$(realpath qmk_userspace/vial-qmk)"`

Refer to [the QMK documentation](https://docs.qmk.fm/newbs_external_userspace)
for general guide on how to add build targets to your userspace and how to build them.


## License

All the code I write in this repository is released under the GNU General Public License v2.0 unless otherwise noted.

Keymaps for keyboards that are not designed by me might have a different license than GPL-2.0.
Make sure to refer to each license notice in such cases.
