# KernelSU-Next + SUSFS kernel for Tecno Spark 10C (KI5K)

Build recipe (GitHub Actions + patches) for a custom kernel on the
Tecno Spark 10C, Unisoc T606 (UMS9230). This repo is for Unisoc chipsets only.

## Tested on
- Device: Tecno Spark 10C (KI5K), Android 12
- Build: KI5K-F065ABCDEAgAh-S-GL-20241211V618
- Kernel: 5.4.254
- KernelSU-Next: v3.4.0-legacy (kprobes hook mode)
- SUSFS: v1.5.5
- Chipset: Unisoc T606, confirmed working on both 4GB and 8GB RAM variants

## How to use
1. Fork this repo.
2. Open the Actions tab and run the build workflow.
3. Download the artifact and repack your own stock boot.img with it.
4. Back up your stock boot.img, then flash.

## Known limitations
- SUSFS hide rules (add_sus_path etc.) do not persist across reboot yet.
  They were only tested manually with ksu_susfs commands and are not
  wired into post-fs-data.sh/service.sh.
- Tested on Unisoc T606 only. Other Unisoc chipsets (e.g. T701) are untested — use at your own risk.

## Support
XDA thread: https://xdaforums.com/t/kernel-update-kernelsu-next-working-on-tecno-spark-10c-ki5k-unisoc-t606-kernel-5-4-254-susfs-next.4802134/
XDA: Peacemak
