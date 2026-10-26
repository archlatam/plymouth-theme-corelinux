# Core Linux Plymouth theme

Plymouth theme for Core Linux by ArchLatam community.

## Installation

```bash
# Copy theme to Plymouth themes directory
sudo cp -r usr/share/plymouth/themes/corelinux /usr/share/plymouth/themes/

# Set theme as default
sudo plymouth-set-default-theme corelinux

# Rebuild initrd
sudo mkinitcpio -P
```

## Requirements

- Plymouth installed on your system
- A working Plymouth configuration

## Found any issue?

If you encounter any problems with this theme, please open an issue on the [GitHub repository](https://github.com/archlatam/plymouth-theme-corelinux/issues).

## How to contribute?

We appreciate contributions! Please follow these steps:

1. [Fork this repository](https://github.com/archlatam/plymouth-theme-corelinux/fork)
2. Create a branch: `git checkout -b my-feature`
3. Make your changes and commit using [conventional commits](https://www.conventionalcommits.org/): `git commit -m "feat: add new feature"`
4. Push to your fork: `git push origin my-feature`
5. Create a Pull Request

## License

GPL-3.0
