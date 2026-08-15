Build a Linux 4.14 kernel for Xiaomi Redmi Note 8 Pro (begonia).

Target ROM:
PixelExperience 12.1
Build: 2022-08-29
Android: 12.1
Architecture: arm64

Requirements:
- Use the exact PixelExperience begonia kernel source.
- Use the exact kernel commit corresponding to the 2022-08-29 ROM.
- Use the correct begonia defconfig.
- Integrate KernelSU Next in legacy/non-GKI mode.
- Build Image.gz-dtb.
- Package the result as an AnyKernel3 flashable ZIP.
- Upload the ZIP as a GitHub Actions artifact.

Do not guess the kernel commit, defconfig,
toolchain, or DTB configuration.
If something cannot be verified, stop the build and report it.
