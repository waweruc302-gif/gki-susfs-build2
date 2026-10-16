# KernelSU-Next + SUSFS kernel for Tecno Spark 10C (KI5K)

Build recipe (GitHub Actions + patches) for a custom kernel on the
Tecno Spark 10C, Unisoc T606 (UMS9230).

## Tested on
- Device: Tecno Spark 10C (KI5K), Android 12
- Build: KI5K-F065ABCDEAgAh-S-GL-20241211V618
- Kernel: 5.4.254
- KernelSU-Next: v3.4.0-legacy (kprobes hook mode)
- SUSFS: v1.4.4
Tested on Unisoc T606, 4GB and 8GB RAM variants — confirmed working on both. This repo is for Unisoc chipsets only.

## How to use
1. Fork this repo.
2. Open the Actions tab and run the build workflow.
3. Download the artifact and repack your own stock boot.img with it.
4. Back up your stock boot.img, then flash.

## Known limitations
- SUSFS hide rules (add_sus_path etc.) do not persist across reboot yet.
  They were only tested manually with ksu_susfs commands and are not
  wired into post-fs-data.sh/service.sh.
- Only tested on one unit (4 GB RAM). Use at your own risk.

## Support
XDA thread: https://xdaforums.com/t/kernel-update-kernelsu-next-working-on-tecno-spark-10c-ki5k-unisoc-t606-kernel-5-4-254-susfs-next.4802134/
XDA: Peacemak
