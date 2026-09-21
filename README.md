# Ga Hing Woo (Jiaxing Hu)

[![ORCID](https://img.shields.io/badge/ORCID-0009--0002--0840--8951-A6CE39?logo=orcid&logoColor=white)](https://orcid.org/0009-0002-0840-8951) [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.21348016.svg)](https://doi.org/10.5281/zenodo.21348016) ![Focus](https://img.shields.io/badge/focus-silicon_bring--up-blue) ![Status](https://img.shields.io/badge/status-working-brightgreen)

I live in the low-level guts of ARM and RISC-V platforms: firmware, TEEs, embedded Linux, and silicon bring-up, across Cortex-A, Cortex-M, and RISC-V.

I brought the Rockchip RK3576 up the entire stack myself: TF-A, OP-TEE, U-Boot, EDK2/UEFI, Linux device trees, NPU. Merged fixes in Trusted Firmware-A and OP-TEE (PR #7821), plus two IOMMU fixes, a devicetree series, and a PHY fix applied directly by the IOMMU, Rockchip SoC and net maintainers (all five now in mainline for 7.3).

On the NPU I worked both stacks: the vendor runtime (RKNPU/RKLLM) running real LLMs and vision on a mainline kernel (Llama-3.2-1B ~17 tok/s, MobileNet ~169 fps), and the fully open rocket driver, where I reverse-engineered the compute registers until MobileNet V1 classified end to end on the NPU. Version 1 of that preprint blamed the hardware for chained layers stalling; it was a 16-bit field written as 12, and version 2 withdraws it and is mostly about how the error survived thirty-eight days. I also review other contributors' patches in that driver: caught a real bug in one, and got a Tested-by back on my own series from hardware I don't own.

I've also extended this isolation work across ISAs on the RP2350: SWD-verified TrustZone-M on its Cortex-M33, and a sibling PMP example on its Hazard3 RISC-V cores, same repo.

**Works & Refs:** [gahingwoo.com](https://gahingwoo.com/) · [evidence](https://gahingwoo.com/evidence/) · [kiln](https://github.com/gahingwoo/kiln) · [edk2-rk3576](https://github.com/gahingwoo/edk2-rk3576) · [bl32-rk3576](https://github.com/gahingwoo/bl32-rk3576) · [linux-rk3576-npu](https://github.com/gahingwoo/linux-rk3576-npu) · [charsiu](https://github.com/gahingwoo/charsiu) · [mesa-rk3576](https://github.com/gahingwoo/mesa-rk3576) · [preprint (DOI)](https://doi.org/10.5281/zenodo.21348016) · [vepu510-rk3576](https://github.com/gahingwoo/vepu510-rk3576) · [rp2350-tz-tee](https://github.com/gahingwoo/rp2350-tz-tee) · [SoC-Consistency](https://github.com/gahingwoo/SoC-Consistency) · [RKDevelopTool-GUI](https://github.com/gahingwoo/RKDevelopTool-GUI) · [OP-TEE #7821](https://github.com/OP-TEE/optee_os/pull/7821) · [OP-TEE #7841 (pending)](https://github.com/OP-TEE/optee_os/pull/7841) · [TF-A #51089](https://review.trustedfirmware.org/c/TF-A/trusted-firmware-a/+/51089) · [blog](https://blog.gahingwoo.com/)

