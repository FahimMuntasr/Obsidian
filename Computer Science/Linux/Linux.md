Linux is a [[Unix]] based operating system. At the core it is a [kernel](Kernel.md) 

#### The Linux filesystem:

| /                 | root folder                                                           |
| ----------------- | --------------------------------------------------------------------- |
| /usr              | The **U**nix **S**ystem **R**esource, contains all system files       |
| /usr/bin          | Executable file **BIN**aries for applications installed on the system |
| /usr/share        | Program resources                                                     |
| /etc              | System configuration                                                  |
| /home             | User-owned data                                                       |
| /var              | Logs and caches                                                       |
| /home/`user-name` | Data owned the current user logged in                                 |
| /proc             | Runtime process data                                                  |
| /tmp              | Temporary data storage                                                |

Types of files,
when running the `ls -ld` command,
the output starts with the file-type as a letter where
- `-` is a regular file
- `d` is a directory
- `l` is a symbolic link
- `p` is a named pipe
- `c` is a character device file
- `b` is a block device file
- `s` is a unix socket

Symlinks
- Special type of file that points to the location of another file
- Created with `ln -s` 

