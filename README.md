# Ga Hing Woo (Jiaxing Hu)

Final-year high school student heading to university — but most of my real work happens 
upstream. I live in the low-level guts of ARM platforms: firmware, embedded Linux, and 
silicon bring-up, mostly on the Rockchip RK3576.

I've brought the RK3576 up the entire stack myself — TF-A, OP-TEE, U-Boot, EDK2/UEFI, 
Linux device trees, NPU. I landed a fix in Trusted Firmware-A (reviewed by Arm, ST and 
Rockchip engineers, merged to mainline) and shipped RK3576 platform support in OP-TEE 
(PR #7821). Most recently I got the RK3576 NPU running real LLMs and vision models on a 
mainline kernel — Llama-3.2-1B at ~13 tok/s or (Qwen2.5-1.5B at ~9), MobileNet at ~150 fps — and I'm mapping out 
its undocumented register interface to help bring an open-source driver to the whole 
RK35xx family.

Works & Refs: [kiln](https://github.com/gahingwoo/kiln) · [edk2-rk3576](https://github.com/gahingwoo/edk2-rk3576) · [bl32-rk3576](https://github.com/gahingwoo/bl32-rk3576) · [linux-rk3576-npu](https://github.com/gahingwoo/linux-rk3576-npu) · [SoC-Consistency](https://github.com/gahingwoo/SoC-Consistency) · [RKDevelopTool-GUI](https://github.com/gahingwoo/RKDevelopTool-GUI) · [OP-TEE #7821](https://github.com/OP-TEE/optee_os/pull/7821) · [OP-TEE #7841](https://github.com/OP-TEE/optee_os/pull/7841) · [TF-A #51089](https://review.trustedfirmware.org/c/TF-A/trusted-firmware-a/+/51089) · [gahingwoo.github.io](https://gahingwoo.github.io/)
