# Ga Hing Woo (Jiaxing Hu)

I work on firmware, TEEs, embedded Linux and silicon bring-up on ARM and RISC-V.

## Now: the Rockchip RK3576, from firmware to Windows and Linux

- [edk2-rk3576](https://github.com/gahingwoo/edk2-rk3576): UEFI firmware for the LCKFB TaishanPi 3M, ArmSoM CM5-IO and Radxa ROCK 4D. It boots Linux on all three and Windows 11 on the TaishanPi 3M and CM5-IO.
- [wddm-mali-g52](https://github.com/gahingwoo/wddm-mali-g52): a WDDM 2.0 driver for the Mali-G52, with Mesa Panfrost as the user-mode driver. Direct3D 11 up to feature level 10_1, and OpenGL 3.1.
- [woa-rk3576-npu](https://github.com/gahingwoo/woa-rk3576-npu): a Windows driver for the NPU. Llama 3.2 1B decodes at 14 to 16 tokens a second.
- [woa-rk3576](https://github.com/gahingwoo/woa-rk3576): Windows drivers (eMMC, SD, USB, Ethernet, audio, video decoder) and a WinPE installer.
- [charsiu](https://github.com/gahingwoo/charsiu): an open LLM runtime on the mainline rocket driver, with no vendor userspace. Its README measures decode at 1.39x the vendor runtime's on the same board and NPU clock. It also runs on Windows.
- [charsiu-desktop](https://github.com/gahingwoo/charsiu-desktop): a chat app for charsiu on Windows and Linux.
- [maskrom-studio](https://github.com/gahingwoo/maskrom-studio): a desktop app that installs Windows or Armbian, updates the UEFI firmware and writes images over MaskROM.

## Upstream

Merged:

- Linux 7.3: two Rockchip IOMMU fixes, the ArmSoM CM5 and CM5-IO devicetree and bindings, and a Motorcomm PHY reference clock fix.
- Linux 7.4-rc: a CM5-IO devicetree comment fix, and three rocket driver fixes from my RK3576 NPU series.
- Rockchip power domain fixes for the RK3576 NPU, applied by Ulf Hansson to his fixes and next branches.
- [Trusted Firmware-A](https://review.trustedfirmware.org/c/TF-A/trusted-firmware-a/+/51089): drops a redundant RK3576 GIC build override.
- [OP-TEE #7821](https://github.com/OP-TEE/optee_os/pull/7821): RK3576 platform support.
- Armbian: an edge kernel with mainline U-Boot for the CM5-IO, the NPU on the CM5-IO and ROCK 4D, and the TaishanPi 3M as a new board.

In review:

- RK3576 NPU support for the rocket driver, now at v18 (8 patches). Reviewed-by tags from Heiko Stuebner, Krzysztof Kozlowski, Daniel Drake and Igor Paunovic, an Acked-by from Conor Dooley, and a Tested-by from Sidong Yang on RK3588.
- [OP-TEE #7841](https://github.com/OP-TEE/optee_os/pull/7841): OTP-based hardware unique key and the RK3576 hardware random number generator. Open.

## Other projects

Firmware and security:

- [bl32-rk3576](https://github.com/gahingwoo/bl32-rk3576): the OP-TEE platform port for the RK3576.
- [rp2350-tz-tee](https://github.com/gahingwoo/rp2350-tz-tee): a minimal TrustZone-M example on the RP2350's Cortex-M33, and a PMP example on its Hazard3 RISC-V cores, both checked on hardware over SWD.

NPU and AI:

- [kiln](https://github.com/gahingwoo/kiln): runs LLMs and vision models on the RK35xx NPU on a mainline kernel.
- [linux-rk3576-npu](https://github.com/gahingwoo/linux-rk3576-npu): RK3576 NPU mainlining and bring-up for the rocket driver.
- [mesa-rk3576](https://github.com/gahingwoo/mesa-rk3576): RK3576 support in Mesa's Teflon rocket driver.
- [vepu510-rk3576](https://github.com/gahingwoo/vepu510-rk3576): a driver for the RK3576 VEPU510 H.264 encoder.

Tools:

- [RKDevelopTool-GUI](https://github.com/gahingwoo/RKDevelopTool-GUI): Rockchip flashing and partition management on macOS and Linux.
- [SoC-Consistency](https://github.com/gahingwoo/SoC-Consistency): consistency checks for Linux SoC devicetrees.
- [edk2-webflash](https://github.com/gahingwoo/edk2-webflash): flashes edk2-rk3576 from the browser over WebUSB ([flash.gahingwoo.com](https://flash.gahingwoo.com/)).

## Links

[gahingwoo.com](https://gahingwoo.com/) · [evidence](https://gahingwoo.com/evidence/) · [blog](https://blog.gahingwoo.com/) · ORCID [0009-0002-0840-8951](https://orcid.org/0009-0002-0840-8951)

Preprint on the RK3576 NPU bring-up: [doi:10.5281/zenodo.21348016](https://doi.org/10.5281/zenodo.21348016). Version 1 blamed the hardware for a chained-task failure; version 2 withdraws that claim and traces the failure to ordinary faults in register and buffer generation.
