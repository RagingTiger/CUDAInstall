# Table of Contents
+ [Installing](https://github.com/RagingTiger/CUDAInstall#installing)
    - [macOS](http://github.com/RagingTiger/CUDAInstall#macos)
        + [CUDA-capable GPU](https://github.com/RagingTiger/CUDAInstall#cuda-capable-gpu)
        + [macOS and Xcode Version](https://github.com/RagingTiger/CUDAInstall#macos-and-xcode-version)
        + [NVIDIA CUDA Toolkit](https://github.com/RagingTiger/CUDAInstall#nvidia-cuda-toolkit-downloading)
            - [Downloading](https://github.com/RagingTiger/CUDAInstall#nvidia-cuda-toolkit-downloading)
            - [Installing](https://github.com/RagingTiger/CUDAInstall#nvidia-cuda-toolkit-installing)
            - [Verifying](https://github.com/RagingTiger/CUDAInstall#nvidia-cuda-toolkit-verifying)
    - [Linux](http://github.com/RagingTiger/CUDAInstall#linux)

# Installing
This section will cover installing CUDA on both `macOS` and `Linux`.


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

Now you can click the green download button and begin downloading the `NVIDIA CUDA Toolkit` [disk image](https://en.wikipedia.org/wiki/Apple_Disk_Image) to your downloads folder. Once the file has finished downloading, you will want to confirm the integrity of the file by verifying the checksum. If you follow the guide's instructions, you can use the following command to check the file:
```
$ openssl md5 <path/to/file>
```
Compare the output from this command to the entry for the `download file name` found on [this page](http://developer2.download.nvidia.com/compute/cuda/8.0/secure/Prod2/docs/sidebar/md5sum.txt?Ueb-ED3JLFmOvTGZl1tyoYj442TeiYjkuj7BC8aS3ryEECUEI11WSBwcdfO_7q8JCRHeuNvbRJgcilBGUzFP5PyYS8Fa33NdK5PpXGJ7MFhrU1QkHmZPuPi8byi4XEw6oGyPzqSuHaP6scPPJSU4KbXXr_w) (*the entry will have the same name as the file you downloaded*). The two checksums should match.

#### NVIDIA CUDA Toolkit: Installing
Now that the toolkit has been downloaded, and the integrity verified, we are ready to [install the CUDA toolkit](http://docs.nvidia.com/cuda/cuda-installation-guide-mac-os-x/index.html#install). When the `.dmg` file is mounted and opened the following series of screens will walk you through the installation process:

**Step 1**: Double click CUDA installer
<p align="center">
  <img src="https://github.com/RagingTiger/CUDAInstall/raw/7c06f9f9d62f4422b3750f37dee25db9911abbff/img/macos/NVIDIA_CUDA_Toolkit_install_step1.png"/>
</p>

**Step 2**: Read Agreement (optional) and click `Accept and Proceed`
<p align="center">
  <img src="https://github.com/RagingTiger/CUDAInstall/raw/7c06f9f9d62f4422b3750f37dee25db9911abbff/img/macos/NVIDIA_CUDA_Toolkit_install_step2.png"/>
</p>

**Step 3**: Select install packages (just leave all checked) and click `Next`
<p align="center">
  <img src="https://github.com/RagingTiger/CUDAInstall/raw/7c06f9f9d62f4422b3750f37dee25db9911abbff/img/macos/NVIDIA_CUDA_Toolkit_install_step3.png"/>
</p>

The installer will now go through and install each of the selected packages in the default locations:

+ CUDA Driver: `/Library/Frameworks/CUDA.framework`
    *This is the interface to the GPU. A Unix compatibility stub that refers to this driver is also installed at* `/usr/local/cuda/lib/libcuda.dylib`

+ CUDA Toolkit: `/Developer/NVIDIA/CUDA-X.X`
    *This is where additional tools (i.e. header files, compilers, debuggers, misc. binaries, etc...) will be installed*

+ CUDA Samples: `/Developer/NVIDIA/CUDA-X.X/samples`
    *This is where various sample programs that use CUDA will be located*

Before moving on to verification of the install, we need to set some [environment variables](https://en.wikipedia.org/wiki/Environment_variable) that will be used by programs, libraries, and applications that depend on the CUDA Driver/Toolkit (*NOTE: `CUDA-X.X` is just a place holder for the actual version of CUDA you have downloaded (e.g CUDA-8.0), do not literally use it.*):
```
export PATH=/Developer/NVIDIA/CUDA-X.X/bin${PATH:+:${PATH}}
export DYLD_LIBRARY_PATH=/Developer/NVIDIA/CUDA-X.X/lib\
                         ${DYLD_LIBRARY_PATH:+:${DYLD_LIBRARY_PATH}}
```
This will only temporarily set the environment variables (which may be ideal for the given situation), but to set them permanently you will need to edit your [shell rc](https://en.wikipedia.org/wiki/Configuration_file) file:
```
$ echo "# CUDA Environment Variables" >> ".$(basename $SHELL)rc"
$ echo "PATH=/Developer/NVIDIA/CUDA-X.X/bin${PATH:+:${PATH}}" >> ".$(basename $SHELL)rc"
$ echo "DYLD_LIBRARY_PATH=/Developer/NVIDIA/CUDA-X.X/lib${DYLD_LIBRARY_PATH:+:${DYLD_LIBRARY_PATH}}" >> ".$(basename $SHELL)rc"
```
This newly formed section of your `shell rc` file will be useful later for organizing other `CUDA` related environment variables used in other frameworks (e.g. [Tensorflow](https://www.tensorflow.org/install/install_mac), and [Darknet](https://pjreddie.com/darknet/install/)).

#### NVIDIA CUDA Toolkit: Verifying
With every installed and the correct environment variables set, we can begin to [verify everything is working](http://docs.nvidia.com/cuda/cuda-installation-guide-mac-os-x/index.html#verification). First, we [test the driver]() by running the following [kernel extension](https://en.wikipedia.org/wiki/Loadable_kernel_module) reporting command:
```
$ kexstat | grep -i cuda
```
*Note: this should return output with `com.nvidia.CUDA` somewhere*

Next we will simply make sure the `environment variables` are working and the [nvcc compiler](http://docs.nvidia.com/cuda/cuda-installation-guide-mac-os-x/index.html#compiler-verification) path can be found by the [shell](https://en.wikipedia.org/wiki/Unix_shell). Run the following command:
```
$ nvcc -V
```
Now lets test the compiler on some samples (e.g. the directory where the CUDA samples were installed: `/Developer/NVIDIA/CUDA-X.X/samples`):
```
$ cd /Developer/NVIDIA/CUDA-X.X/samples
$ sudo make -C 0_Simple/vectorAdd
$ sudo make -C 0_Simple/vectorAddDrv
$ sudo make -C 1_Utilities/deviceQuery
$ sudo make -C 1_Utilities/bandwidthTest
```
The newly compiled executable will be in the local directory `bin/x86_64/darwin/release`.

Now that the compiler is working, we need to [run a few tests](http://docs.nvidia.com/cuda/cuda-installation-guide-mac-os-x/index.html#runtime-verification). Execute the recently compiled executable `deviceQuery` as follows:
```
$ # navigate to /Developer/NVIDIA/CUDA-X.X/samples if not already there
$ cd /Developer/NVIDIA/CUDA-X.X/samples
$ # run deviceQuery
$ bin/x86_64/darwin/release/deviceQuery
```
This test should output something similar to the image below:
<p align="center">
  <img src="https://github.com/RagingTiger/CUDAInstall/raw/fe29d6ad34ea0cb8271b1916a56891bf76ac9ed6/img/macos/NVIDIA_CUDA_Toolkit_verify_deviceQuery.png"/>
</p>

While this test gives an assortment of information, the necessary information, confirming the GPU was found and CUDA-capable, is at the bottom: `deviceQuery, CUDA Driver = CUDART, CUDA Driver Version = 8.0, CUDA Runtime Version = 8.0, NumDevs = 1, Device0 = GeForce GT 750M
Result = PASS`. This indicates that a CUDA-capable GPU was found (in this case `Device0`) and it is working.

The final test will verify that the system and CUDA-capable GPU are communicating properly. Run the `bandwithTest` as follows:
```
$ # navigate to /Developer/NVIDIA/CUDA-X.X/samples if not already there
$ cd /Developer/NVIDIA/CUDA-X.X/samples
$ # run bandwidthTest
$ bin/x86_64/darwin/release/bandwidthTest
```
This test should have output similar to the below image:
<p align="center">
  <img src="https://github.com/RagingTiger/CUDAInstall/raw/fe29d6ad34ea0cb8271b1916a56891bf76ac9ed6/img/macos/NVIDIA_CUDA_Toolkit_verify_bandwidthTest.png"/>
</p>

The necessary information is at the bottom: `Result = PASS`

With these two tests successfully passed, you have finally completed the installation of CUDA for macOS. Now you can move on to installing your favorite framework(s).

## Linux
`TODO`
