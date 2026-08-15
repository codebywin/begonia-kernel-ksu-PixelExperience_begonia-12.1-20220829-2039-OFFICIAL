---
name: Build Begonia KernelSU Next

on:
  workflow_dispatch:

permissions:
  contents: read
  copilot-requests: write

network:
  allowed:
    - defaults
    - github

---

# Build KernelSU Next for Redmi Note 8 Pro

Build a Linux 4.14 kernel for Xiaomi Redmi Note 8 Pro (begonia).

Target ROM:

- ROM: PixelExperience
- Version: 12.1
- Build: 2022-08-29
- Android: 12.1
- Architecture: arm64
- Device: begonia
- SoC: MediaTek MT6785
- Kernel: Linux 4.14
- Kernel type: non-GKI

Requirements:

1. Identify and use the exact PixelExperience begonia kernel source corresponding to the PixelExperience 12.1 build from 2022-08-29.

2. Verify the exact kernel commit before building. Do not guess the commit.

3. Identify and use the correct begonia defconfig. Do not guess the defconfig.

4. Identify the correct compiler/toolchain required by this kernel source.

5. Integrate KernelSU Next using its legacy/non-GKI method appropriate for Linux 4.14.

6. Preserve the original begonia device tree and kernel configuration.

7. Build the kernel for ARM64.

8. Build the required kernel image, including Image.gz-dtb if this kernel tree requires it.

9. Verify that the resulting kernel image was successfully generated.

10. Package the kernel into a flashable AnyKernel3 ZIP.

11. Name the final ZIP:

begonia-PE12.1-KernelSU-Next.zip

12. Upload the resulting ZIP as a GitHub Actions artifact.

IMPORTANT:

Do not guess the kernel commit.

Do not guess the defconfig.

Do not guess the compiler/toolchain.

Do not use a GKI configuration.

Do not replace the begonia device tree with a configuration from another device.

If the exact kernel source, commit, defconfig, or toolchain cannot be verified, stop the workflow and report the missing information instead of building an unverified kernel.

Before building, print the following information to the Actions log:

- Kernel repository
- Kernel commit
- Kernel version
- Defconfig
- Compiler/toolchain
- KernelSU Next version/commit
- Architecture
- Device tree configuration
