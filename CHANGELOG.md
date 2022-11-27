# Changelog

## v1.0.2

* Fixed the systemd kernel command line getting duplicated when ran multiple times.
* Documented support for PVE 7.3 in meta.

## v1.0.1

* The role now automatically detects the CPU type (`intel`/`amd`) of the system to generate the appropriate cmdline.
* The role now automatically detects the system boot type (`systemd`/`grub`) to modify the appropriate file.
* Added new variables to override the generated/detected ones in case of error.

## v1.0.0

* Initial release of the `mirceanton.proxmox_iommu` role 🚀
