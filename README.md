# EXT2 Filesystem Implementation

This repository contains an implementation of the EXT2 filesystem. The EXT2 (Extended File System 2) is a widely used filesystem format in Linux-based operating systems. This implementation is intended for educational purposes and provides a basic structure of the EXT2 filesystem, including the superblock, block group descriptor table, block and inode bitmaps, and a simple directory structure.

## Features

- **Superblock**: The implementation includes the superblock of the EXT2 filesystem, which contains critical metadata about the filesystem, such as the number of inodes, blocks, block sizes, and more.

- **Block Group Descriptor Table**: The block group descriptor table stores information about each block group in the filesystem, including block and inode bitmap block numbers, the inode table block number, and the counts of free blocks and inodes.

- **Block and Inode Bitmaps**: Bitmaps are used to track which blocks and inodes are in use and which are free. This implementation initializes block and inode bitmaps with sample data.

- **Inode Table**: The inode table is an essential part of the filesystem, containing metadata about files and directories. The implementation initializes inodes for the root directory, lost+found directory, and sample files.

- **Directory Structure**: A simple directory structure is created, including the root directory, lost+found directory, and sample files like "hello-world" and "hello" (symbolic link).

## Building and Running

You can compile and run this implementation on a Linux system by following these steps:

1. Clone the repository to your local machine.

2. Compile the code using a C compiler (e.g., GCC) by running the following command in the repository's directory:

   ```shell
   gcc -o ext2fs ext2fs.c


## Usage

Run the compiled program to generate the EXT2 filesystem image:

```shell
./ext2fs


The program will create a file named cs111-base.img containing the EXT2 filesystem structure.

This implementation provides a basic structure of the EXT2 filesystem and generates a filesystem image. You can explore the generated filesystem image using tools like debugfs or by mounting it as a loop device in a Linux environment. Keep in mind that this implementation is simplified and does not include advanced filesystem features.
