# Ga Hing Woo (Jiaxing Hu)

Final-year high school student heading to university — but most of my real work happens upstream. I live in the low-level guts of ARM platforms: firmware, TEEs, embedded Linux, and silicon bring-up, across both Cortex-A and Cortex-M.

I brought the Rockchip RK3576 up the entire stack myself — TF-A, OP-TEE, U-Boot, EDK2/UEFI, Linux device trees, NPU. I landed a fix in Trusted Firmware-A (reviewed by Arm, ST and Rockchip engineers, merged to mainline) and shipped RK3576 platform support in OP-TEE (PR #7821). I got the vendor NPU runtime running real LLMs and vision on a mainline kernel — Llama-3.2-1B at ~13 tok/s, Qwen2.5-1.5B at ~9, MobileNet at ~169 fps — while separately reverse-engineering the NPU's undocumented compute registers to push the open-source rocket driver further on RK3576, cross-checking with others on RK3568 and RK3588.

Lately I've been extending the same TrustZone work down to the M-profile world: a minimal, SWD-verified TrustZone-M example on the RP2350 (secure isolation proven by a caught SecureFault, secret never leaks).

Works & Refs: [kiln](https://github.com/gahingwoo/kiln) · [edk2-rk3576](https://github.com/gahingwoo/edk2-rk3576) · [bl32-rk3576](https://github.com/gahingwoo/bl32-rk3576) · [linux-rk3576-npu](https://github.com/gahingwoo/linux-rk3576-npu) · [rp2350-tz-tee](https://github.com/gahingwoo/rp2350-tz-tee) · [SoC-Consistency](https://github.com/gahingwoo/SoC-Consistency) · [RKDevelopTool-GUI](https://github.com/gahingwoo/RKDevelopTool-GUI) · [OP-TEE #7821](https://github.com/OP-TEE/optee_os/pull/7821) · [OP-TEE #7841](https://github.com/OP-TEE/optee_os/pull/7841) · [TF-A #51089](https://review.trustedfirmware.org/c/TF-A/trusted-firmware-a/+/51089) · [gahingwoo.github.io](https://gahingwoo.github.io/)
