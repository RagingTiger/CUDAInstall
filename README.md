# About
General info about installing CUDA on macOS and Linux

# Table of Contents
+ Installing
    - [macOS](http://github.com/RagingTiger/CUDAInstall#macos)
        + [CUDA-capable GPU]()
        + [macOS and Xcode Version]()
        + [NVIDIA CUDA Toolkit]()
            - [Downloading]()
            - [Installing]()
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

*Each of these requirements will be discussed in the following sections.*

#### CUDA-capable GPU
Not all GPUs are "CUDA-capable", so you must make sure that the GPU installed
in your system meets this requirement. To find out about your GPU, follow the instructions on [CUDA-capable GPUs](http://docs.nvidia.com/cuda/cuda-installation-guide-mac-os-x/index.html#cuda-enabled-gpu) in the macOS install guide.

#### macOS and Xcode Version
Now that you have determined that your hardware is "CUDA-capable", you can verify that you have the necessary [macOS and Xcode versions installed](http://docs.nvidia.com/cuda/cuda-installation-guide-mac-os-x/index.html#mac-os-version):

| Xcode |   Apple LLVM  | 10.11 | 10.12 |
| ----- | ------------- | ----- | ----- |
|  7.2  |     7.0.3     |  YES  |   NO  |
|  8.2  |     8.0.0     |  NO   |   YES |

In the `above table`, the two far right columns represent `macOS version` **10.11** and **10.12** respectively, and the far left columns represent the `toolchain` that will be used to compile the CUDA library on macOS *(Translation: you must have either macOS 10.11 or 10.12 and you must install Xcode 7.2 if you have macOS 10.11, or you must install Xcode 8.2 if you have
macOS 10.12 )*. If you must install an older version of Xcode (i.e. 7.2), you will need an [Apple Developer account](https://developer.apple.com/).

Once you have installed the correct `Xcode version` for your system, you must
follow a few steps to ["link" the Xcode version](http://docs.nvidia.com/cuda/cuda-installation-guide-mac-os-x/index.html#xcode-version) that you want the system to use, and make sure you [install the command-line tools for Xcode](http://docs.nvidia.com/cuda/cuda-installation-guide-mac-os-x/index.html#verify-cli-installed).

#### NVIDIA CUDA Toolkit: Downloading
At this point, having verified the `hardware and software` of your macOS system, you are ready to [download the NVIDIA CUDA Toolkit](http://docs.nvidia.com/cuda/cuda-installation-guide-mac-os-x/index.html#download) This simply involves going to this site (https://developer.nvidia.com/cuda-downloads) and following the steps shown in the images below:

**Step 1**: Go to [CUDA Toolkit downloads](https://developer.nvidia.com/cuda-downloads) page
<p align="center">
  <img src="https://github.com/RagingTiger/CUDAInstall/raw/7883f32be0e06fbf0a18bdec07f457cc56ff2c87/img/NVIDIA_CUDA_Toolkit_dwnld_step1.png"/>
</p>

**Step 2**: Click `Mac OSX`
<p align="center">
  <img src="https://github.com/RagingTiger/CUDAInstall/raw/7883f32be0e06fbf0a18bdec07f457cc56ff2c87/img/NVIDIA_CUDA_Toolkit_dwnld_step2.png"/>
</p>

**Step 3**: Choose your `macOS version`
<p align="center">
  <img src="https://github.com/RagingTiger/CUDAInstall/raw/7883f32be0e06fbf0a18bdec07f457cc56ff2c87/img/NVIDIA_CUDA_Toolkit_dwnld_step3.png"/>
</p>

**Step 4**: Choose your download option (either is fine)
<p align="center">
  <img src="https://github.com/RagingTiger/CUDAInstall/raw/7883f32be0e06fbf0a18bdec07f457cc56ff2c87/img/NVIDIA_CUDA_Toolkit_dwnld_step4.png"/>
</p>

Now you can click the green download button, and you begin downloading the `NVIDIA CUDA Toolkit` to your downloads folder. Once the [.dmg](https://en.wikipedia.org/wiki/Apple_Disk_Image) file has finished downloading, you will want to confirm the integrity of the file by verifying the checksum. If you follow the guide's instructions, you can use the following command to check the file:
```
$ openssl md5 <path/to/file>
```
Compare the output from this command to the entry for the `download file name` found on [this page](http://developer2.download.nvidia.com/compute/cuda/8.0/secure/Prod2/docs/sidebar/md5sum.txt?Ueb-ED3JLFmOvTGZl1tyoYj442TeiYjkuj7BC8aS3ryEECUEI11WSBwcdfO_7q8JCRHeuNvbRJgcilBGUzFP5PyYS8Fa33NdK5PpXGJ7MFhrU1QkHmZPuPi8byi4XEw6oGyPzqSuHaP6scPPJSU4KbXXr_w) (*the entry will have the same name as the file you downloaded*). The two checksums should match.

#### NVIDIA CUDA Toolkit: Installing
Now that the toolkit has been downloaded, and the integrity verified, we are ready to [install the CUDA toolkit](http://docs.nvidia.com/cuda/cuda-installation-guide-mac-os-x/index.html#install).

`TODO`



## Linux
`TODO`
