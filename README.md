# Ga Hing Woo (Jiaxing Hu)

I am in my final year of high school and preparing to begin university, with a focus on low-level firmware, embedded Linux, and ARM platform bring-up. My recent work focuses on the Rockchip RK3576, including the boot chain from secure firmware and bootloaders through UEFI, Linux, desktop operating systems, and accelerator support.

I enjoy projects where the result has to survive contact with real hardware, upstream review, and other developers' boards.

## Selected Work

### Rockchip RK3576 Platform Bring-up

I have been building a complete software stack for RK3576-based devices, covering firmware, secure-world components, bootloaders, UEFI, device trees, Linux, and desktop operating-system support.

Key repositories:

- [edk2-rk3576](https://github.com/gahingwoo/edk2-rk3576) - UEFI firmware for RK3576 devices, with support across multiple boards and hardware-tested boot paths.
- [woa-rk3576](https://github.com/gahingwoo/woa-rk3576) - Windows on Arm work for RK3576 devices.
- [linux-rk3576-npu](https://github.com/gahingwoo/linux-rk3576-npu) - RK3576 NPU bring-up work, extending platform support beyond boot and desktop enablement into accelerator integration.
- [bl32-rk3576](https://github.com/gahingwoo/bl32-rk3576) - OP-TEE BL32 platform port for Rockchip RK3576.
- [u-boot](https://github.com/gahingwoo/u-boot) - U-Boot work and board bring-up experiments.
- [trusted-firmware-a](https://github.com/gahingwoo/trusted-firmware-a) - Trusted Firmware-A work related to RK3576 platform support.

### Upstream Firmware Contributions

Some of the work has gone beyond personal repositories and into upstream review:

- OP-TEE RK3576 platform port: passed automated checks, reproduced by another developer on real hardware, and approved pending merge.
- Trusted Firmware-A fix: removed a leftover configuration override that could silently break builds without a secure OS; the patch was reviewed by engineers from STMicroelectronics, Google, and Rockchip, approved by a Rockchip code owner, and merged upstream.

References:

- [OP-TEE PR #7821](https://github.com/OP-TEE/optee_os/pull/7821)
- [Trusted Firmware-A Gerrit #51089](https://review.trustedfirmware.org/c/TF-A/trusted-firmware-a/+/51089)

### SoC Consistency Checking

[SoC-Consistency](https://github.com/gahingwoo/SoC-Consistency) is a Python tool for system-level consistency checking of Linux SoC device trees. It models relationships such as power rails, clocks, pin muxing, and interrupt routing so that hardware-integration errors can be caught before they become runtime failures.

The project grew from real debugging experience during board bring-up: bugs that pass normal syntax validation can still cause suspend/resume failures, memory corruption, or unsafe IO configuration when the hardware model is wrong.

### Rockchip Flashing Utility

[RKDevelopTool-GUI](https://github.com/gahingwoo/RKDevelopTool-GUI) is a cross-platform graphical utility for Rockchip firmware flashing and partition management on macOS and Linux. It is intended to make low-level device work more accessible and less error-prone for people using Rockchip boards.

## Technical Areas

- ARM firmware and secure boot flow
- OP-TEE, Trusted Firmware-A, U-Boot, and EDK2/TianoCore
- Linux device trees and board support packages
- Rockchip RK3576 platform development
- NPU and accelerator bring-up
- Embedded Linux, Python tooling, and hardware debugging
- Android and Wear OS companion utilities

## Contact

- GitHub: [@gahingwoo](https://github.com/gahingwoo)
- Project pages: [gahingwoo.github.io](https://gahingwoo.github.io/)
