# Ga Hing Woo (Jiaxing Hu)

[![ORCID](https://img.shields.io/badge/ORCID-0009--0002--0840--8951-A6CE39?logo=orcid&logoColor=white)](https://orcid.org/0009-0002-0840-8951) [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.21348017.svg)](https://doi.org/10.5281/zenodo.21348017) ![Focus](https://img.shields.io/badge/focus-silicon_bring--up-blue) ![Status](https://img.shields.io/badge/status-working-brightgreen)

I live in the low-level guts of ARM and RISC-V platforms: firmware, TEEs, embedded Linux, and silicon bring-up, across Cortex-A, Cortex-M, and RISC-V.

I brought the Rockchip RK3576 up the entire stack myself: TF-A, OP-TEE, U-Boot, EDK2/UEFI, Linux device trees, NPU. I landed a fix in Trusted Firmware-A (reviewed by Arm, ST and Rockchip engineers, merged to mainline) and shipped RK3576 platform support in OP-TEE (PR #7821).

On the NPU I worked both stacks. The vendor runtime (RKNPU/RKLLM) I got running real LLMs and vision on a mainline kernel (Llama-3.2-1B ~13 tok/s, Qwen2.5-1.5B ~9, MobileNet ~169 fps). On the fully open stack (mainline rocket driver) I reverse-engineered the undocumented compute registers, got a single int8 convolution byte-exact against a CPU reference, then localized why chained layers stall to fixed-function hardware below the driver under a falsification-first method (cross-confirmed on RK3568 and RK3588). Written up as a preprint (DOI above).

I've also extended this isolation work across ISAs on the RP2350: SWD-verified TrustZone-M on Cortex-M33 (proven by a caught SecureFault) and a sibling RISC-V PMP example on the Hazard3 cores.

**Works & Refs:** [kiln](https://github.com/gahingwoo/kiln) · [edk2-rk3576](https://github.com/gahingwoo/edk2-rk3576) · [bl32-rk3576](https://github.com/gahingwoo/bl32-rk3576) · [linux-rk3576-npu](https://github.com/gahingwoo/linux-rk3576-npu) · [preprint (DOI)](https://doi.org/10.5281/zenodo.21348017) · [vepu510-rk3576](https://github.com/gahingwoo/vepu510-rk3576) · [rp2350-tz-tee](https://github.com/gahingwoo/rp2350-tz-tee) · [SoC-Consistency](https://github.com/gahingwoo/SoC-Consistency) · [RKDevelopTool-GUI](https://github.com/gahingwoo/RKDevelopTool-GUI) · [OP-TEE #7821](https://github.com/OP-TEE/optee_os/pull/7821) · [OP-TEE #7841](https://github.com/OP-TEE/optee_os/pull/7841) · [TF-A #51089](https://review.trustedfirmware.org/c/TF-A/trusted-firmware-a/+/51089) · [gahingwoo.github.io](https://gahingwoo.github.io/)
