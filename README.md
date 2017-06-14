# About
General info about installing CUDA on macOS and Linux

# Table of Contents
+ Installing
    - [macOS](http://github.com/RagingTiger/CUDAInstall#macos)
    - [Linux](http://github.com/RagingTiger/CUDAInstall#linux)

# Installing
This section will cover installing CUDA on both `macOS` and `Linux Ubuntu`.

## macOS
*This section will be referencing the [NVIDIA macOS CUDA Install Guide](http://docs.nvidia.com/cuda/cuda-installation-guide-mac-os-x/index.html#abstract)*

To get started with installing CUDA on macOS, you first need to understand
the [system requirements](http://docs.nvidia.com/cuda/cuda-installation-guide-mac-os-x/index.html#system-requirements). There are only a few conditions to be met to
be able to install and use CUDA on your macOS:

  + CUDA-capable GPU (i.e. the correct `hardware`)
  + macOS 10.11 or higher & Xcode 7.2 or higher (i.e. the correct `software`)
  + NVIDIA CUDA Toolkit (i.e. the `binaries and source code for CUDA`)

Each of these requirements will be discussed in the following sections.

#### CUDA-capable GPU
Not all GPUs are "CUDA-capable", so you must make sure that the GPU installed
in your system meets this requirement. To find out about your GPU, follow the instructions on [CUDA-capable GPUs](http://docs.nvidia.com/cuda/cuda-installation-guide-mac-os-x/index.html#cuda-enabled-gpu) in the macOS install guide.

#### macOS Version and Toolchain
Now that you have determined that your hardware is "CUDA-capable", you can verify that you have the necessary [macOS and Xcode versions installed](http://docs.nvidia.com/cuda/cuda-installation-guide-mac-os-x/index.html#mac-os-version):

| Xcode |   Apple LLVM  | 10.11 | 10.12 |
| ----- | ------------- | ----- | ----- |
|  7.2  |     7.0.3     |  YES  |   NO  |
|  8.2  |     8.0.0     |  NO   |   YES |

In the `above table`, the two far right columns represent `macOS version` **10.11** and **10.12** respectively, and the far left columns represent the `toolchain` that will be used to compile the CUDA library on macOS *(Translation: you must have either macOS 10.11 or 10.12 and you must install Xcode 7.2 if you have macOS 10.11, or you must install Xcode 8.2 if you have
macOS 10.12 )*. If you must install an older version of Xcode (i.e. 7.2), you will need an [Apple Developer account](https://developer.apple.com/).

Once you have installed the correct `Xcode version` for your system, you must
follow a few steps to ["link" the Xcode version](http://docs.nvidia.com/cuda/cuda-installation-guide-mac-os-x/index.html#xcode-version) that you want the system to use, and make sure you [install the command-line tools for Xcode](http://docs.nvidia.com/cuda/cuda-installation-guide-mac-os-x/index.html#verify-cli-installed).

#### NVIDIA CUDA Toolkit
At this point, having verified the `hardware and software` of your macOS system, you are ready to [download the NVIDIA CUDA Toolkit](http://docs.nvidia.com/cuda/cuda-installation-guide-mac-os-x/index.html#download) This simply involves going to this site (https://developer.nvidia.com/cuda-downloads) and following the steps shown in the images below:




## Linux
`TODO`
