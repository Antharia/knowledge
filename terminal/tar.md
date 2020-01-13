## What is tar.xz file?

**tar** is a utility that combines multiple files into one single file. The main advantage of a utility like tar is in transferring files.

Due to the overhead, transferring 100 files of 1 KB will take longer than transferring one file of 100 KB. 

Using **tar**, you can archive several files into one single file and thus you save time and bandwidth while transferring the file.

But **tar** itself doesn’t compress files. If you use tar to combine 100 files of 1 KB each, the resultant **tar** file will probably be around 100 KB only.

To further save time and bandwidth, compression utilities are used. These compression tools will reduce the size of the resultant tar file. XZ is one such compression tool and it utilizes LZMA compression algorithm.

## Extracting tar.xz file in Linux

Extracting a tar xz file is fairly simple. You just need to make sure that you have support for xz compression utility on your Linux distribution.

xz compression tool is available through xz-utils package in most Linux distributions. Most of the time, you’ll already have the xz-utils installed by default.

But you should still ensure that it is installed on your system. You can use your Linux distribution’s package manager to install it.

On Debian or Ubuntu, you can install xz-utils with the following command:

sudo apt install xz-utils

Once you have the xz compression support on your Linux distribution, you can extract the tar.xz file using the standard tar command:

>> tar -xf file.tar.xz

In here:

    -x means extract the archived file
    -f means following is the archived file name

Why did you need to specify x (extract ) here? Because tar can also be used for creating (compressing) files.

So you need to specify which operation you are performing with tar command, compression (c) or extraction (x).
