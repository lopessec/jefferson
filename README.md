# jefferson
JFFS2 filesystem extraction tool

This is a slightly modified version of the original work with fixes for better error handling

Installation
============
Just install the dependencies, clone or extract the project, browse to src folder and run jefferson


Dependencies
============
- `cstruct`
- `pyliblzma`

```bash
$ sudo pip install cstruct
$ sudo apt-get install python-lzma
```

Features
============
- Big/Little Endian support
- `JFFS2_COMPR_ZLIB`, `JFFS2_COMPR_RTIME`, and `JFFS2_COMPR_LZMA` compression support
- CRC checks - for now only enforced on `hdr_crc`
- Extraction of symlinks, directories, files, and device nodes
- Detection/handling of duplicate inode numbers. Occurs if multiple JFFS2 filesystems are found in one file and causes `jefferson` to treat segments as separate filesystems

Usage
============
```bash
$ jefferson filesystem.img -d outdir
```
