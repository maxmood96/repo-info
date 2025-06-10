# `ros:foxy-ros-base`

## Docker Metadata

- Image ID: `sha256:0d94b936914c0c299582ee509d62abd1fb86d1d181f68906a78efb53ed11289b`
- Created: `2020-11-17T19:36:01Z`
- Virtual Size: ~ 789.02 Mb  
  (total size of all layers on-disk)
- Arch: `linux`/`amd64`
- Entrypoint: `["/ros_entrypoint.sh"]`
- Command: `["bash"]`
- Environment:
  - `PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin`
  - `LANG=C.UTF-8`
  - `LC_ALL=C.UTF-8`
  - `ROS_DISTRO=foxy`
- Labels:
  - `org.opencontainers.image.ref.name=ubuntu`
  - `org.opencontainers.image.version=20.04`

## `dpkg` (`.deb`-based packages)

### `dpkg` source package: `acl=2.2.53-6`

Binary Packages:

- `libacl1:amd64=2.2.53-6`

Licenses: (parsed from: `/usr/share/doc/libacl1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2+`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris acl=2.2.53-6
'http://archive.ubuntu.com/ubuntu/pool/main/a/acl/acl_2.2.53-6.dsc' acl_2.2.53-6.dsc 2336 SHA256:02dad794aa09133e557552d75568324ed3e84fb56e93626e67993cf54a97df34
'http://archive.ubuntu.com/ubuntu/pool/main/a/acl/acl_2.2.53.orig.tar.gz' acl_2.2.53.orig.tar.gz 524300 SHA256:06be9865c6f418d851ff4494e12406568353b891ffe1f596b34693c387af26c7
'http://archive.ubuntu.com/ubuntu/pool/main/a/acl/acl_2.2.53.orig.tar.gz.asc' acl_2.2.53.orig.tar.gz.asc 833 SHA256:06849bece0b56a6a7269173abe101cff223bb9346d74027a3cd5ff80914abf4b
'http://archive.ubuntu.com/ubuntu/pool/main/a/acl/acl_2.2.53-6.debian.tar.xz' acl_2.2.53-6.debian.tar.xz 25108 SHA256:c80e6150d9b213e52f5e65ff78d4ee95a71b5a258c1f8b980365d20ed1753a5c
```

### `dpkg` source package: `adduser=3.118ubuntu2`

Binary Packages:

- `adduser=3.118ubuntu2`

Licenses: (parsed from: `/usr/share/doc/adduser/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris adduser=3.118ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/a/adduser/adduser_3.118ubuntu2.dsc' adduser_3.118ubuntu2.dsc 1131 SHA256:785f99d8c75c972cd42d3fab3afa07f97299bb1d70013fe5d295f045224774bb
'http://archive.ubuntu.com/ubuntu/pool/main/a/adduser/adduser_3.118ubuntu2.tar.xz' adduser_3.118ubuntu2.tar.xz 222364 SHA256:9429124c39c381b541005da6f0ae29831bd6533dd65c923e06ca2a7c310db382
```

### `dpkg` source package: `ann=1.1.2+doc-7build1`

Binary Packages:

- `libann0=1.1.2+doc-7build1`

Licenses: (parsed from: `/usr/share/doc/libann0/copyright`)

- `GPL-3`
- `GPL-3.0+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris ann=1.1.2+doc-7build1
'http://archive.ubuntu.com/ubuntu/pool/universe/a/ann/ann_1.1.2%2bdoc-7build1.dsc' ann_1.1.2+doc-7build1.dsc 2164 SHA256:a38a8d00ed46abf52eb1d02cf38ca6221b09005f31922fab47470735d929c66b
'http://archive.ubuntu.com/ubuntu/pool/universe/a/ann/ann_1.1.2%2bdoc.orig.tar.gz' ann_1.1.2+doc.orig.tar.gz 693957 SHA256:1a8053e4f1ee284430758a2d864e567d9b4b08c0f6562460c9913497fafc78c1
'http://archive.ubuntu.com/ubuntu/pool/universe/a/ann/ann_1.1.2%2bdoc-7build1.debian.tar.xz' ann_1.1.2+doc-7build1.debian.tar.xz 172220 SHA256:695d075be631b7675018fb26f4e17ecfd3566e393159b081dada16e86a18a1ef
```

### `dpkg` source package: `apt=2.0.10`

Binary Packages:

- `apt=2.0.10`
- `libapt-pkg6.0:amd64=2.0.10`

Licenses: (parsed from: `/usr/share/doc/apt/copyright`, `/usr/share/doc/libapt-pkg6.0/copyright`)

- `GPL-2`
- `GPLv2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `attr=1:2.4.48-5`

Binary Packages:

- `libattr1:amd64=1:2.4.48-5`

Licenses: (parsed from: `/usr/share/doc/libattr1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2+`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris attr=1:2.4.48-5
'http://archive.ubuntu.com/ubuntu/pool/main/a/attr/attr_2.4.48-5.dsc' attr_2.4.48-5.dsc 2433 SHA256:0b20a285b758083e2e202ffdd2930cef1bf84fee498791fc3e26b69a3bced01d
'http://archive.ubuntu.com/ubuntu/pool/main/a/attr/attr_2.4.48.orig.tar.gz' attr_2.4.48.orig.tar.gz 467840 SHA256:5ead72b358ec709ed00bbf7a9eaef1654baad937c001c044fe8b74c57f5324e7
'http://archive.ubuntu.com/ubuntu/pool/main/a/attr/attr_2.4.48.orig.tar.gz.asc' attr_2.4.48.orig.tar.gz.asc 833 SHA256:5d23c2c83cc13d170f1c209f48d0efa1fc46d16487b790e9996c5206dcfe0395
'http://archive.ubuntu.com/ubuntu/pool/main/a/attr/attr_2.4.48-5.debian.tar.xz' attr_2.4.48-5.debian.tar.xz 25560 SHA256:02238253d324250dabdc0434f7de045d85df93458995a465ac434f2a3978a312
```

### `dpkg` source package: `audit=1:2.8.5-2ubuntu6`

Binary Packages:

- `libaudit-common=1:2.8.5-2ubuntu6`
- `libaudit1:amd64=1:2.8.5-2ubuntu6`

Licenses: (parsed from: `/usr/share/doc/libaudit-common/copyright`, `/usr/share/doc/libaudit1/copyright`)

- `GPL-1`
- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris audit=1:2.8.5-2ubuntu6
'http://archive.ubuntu.com/ubuntu/pool/main/a/audit/audit_2.8.5-2ubuntu6.dsc' audit_2.8.5-2ubuntu6.dsc 2764 SHA256:b149fad8217d68a80299c1ef72539ee7d756146d692b7e51eade7341e60ac528
'http://archive.ubuntu.com/ubuntu/pool/main/a/audit/audit_2.8.5.orig.tar.gz' audit_2.8.5.orig.tar.gz 1140694 SHA256:0e5d4103646e00f8d1981e1cd2faea7a2ae28e854c31a803e907a383c5e2ecb7
'http://archive.ubuntu.com/ubuntu/pool/main/a/audit/audit_2.8.5-2ubuntu6.debian.tar.xz' audit_2.8.5-2ubuntu6.debian.tar.xz 18712 SHA256:d85ecf206bfe256a86e6d39602cd2744beda264a28e413f31c4da227e6542ea7
```

### `dpkg` source package: `base-files=11ubuntu5.8`

Binary Packages:

- `base-files=11ubuntu5.8`

Licenses: (parsed from: `/usr/share/doc/base-files/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris base-files=11ubuntu5.8
'http://archive.ubuntu.com/ubuntu/pool/main/b/base-files/base-files_11ubuntu5.8.dsc' base-files_11ubuntu5.8.dsc 1717 SHA512:65c5f40d4b01ba1cf93520637a3be8ecfa4b32231cdb9888ad261447559de95ac58a33213c3d6d0cefb811f0d9fb9607a3f9cb017301bd25e6424fe9161538bf
'http://archive.ubuntu.com/ubuntu/pool/main/b/base-files/base-files_11ubuntu5.8.tar.xz' base-files_11ubuntu5.8.tar.xz 80736 SHA512:7206dd2a3fb5da4e2901a8ad8cd710c525c9a404ce1364ad7f13816053c3fdaf06f720ac7531f653da2c875752b069200ba278683af4d7a559bba87fca104b5d
```

### `dpkg` source package: `base-passwd=3.5.47`

Binary Packages:

- `base-passwd=3.5.47`

Licenses: (parsed from: `/usr/share/doc/base-passwd/copyright`)

- `GPL-2`
- `PD`

Source:

```console
$ apt-get source -qq --print-uris base-passwd=3.5.47
'http://archive.ubuntu.com/ubuntu/pool/main/b/base-passwd/base-passwd_3.5.47.dsc' base-passwd_3.5.47.dsc 1757 SHA256:5a77a4cce51d1eb72e9d96d4083c641435c05888922c7bd3fa6b4395bf9afad3
'http://archive.ubuntu.com/ubuntu/pool/main/b/base-passwd/base-passwd_3.5.47.tar.xz' base-passwd_3.5.47.tar.xz 53024 SHA256:9810ae0216e96bf9fc7ca6163d47ef8ec7d1677f533451af5911d8202a490a23
```

### `dpkg` source package: `bash=5.0-6ubuntu1.2`

Binary Packages:

- `bash=5.0-6ubuntu1.2`

Licenses: (parsed from: `/usr/share/doc/bash/copyright`)

- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris bash=5.0-6ubuntu1.2
'http://archive.ubuntu.com/ubuntu/pool/main/b/bash/bash_5.0-6ubuntu1.2.dsc' bash_5.0-6ubuntu1.2.dsc 2296 SHA512:d93b919ae7b8e67e3b4e31d205e13006a37aa2a42378744599c3214ecab6544084856a739b38aaeb06742524e2ea302c8147f7a88dbc738e1e7ac0a29be0c0b8
'http://archive.ubuntu.com/ubuntu/pool/main/b/bash/bash_5.0.orig.tar.xz' bash_5.0.orig.tar.xz 5554808 SHA512:f3a719997a8515bae7e84701afafc9b2cdd23c95d29533adb678000b08eba968450b93d5576c3cffbeccbdcd95b713db830e8efeda689258dcfe6f15f0c5dec4
'http://archive.ubuntu.com/ubuntu/pool/main/b/bash/bash_5.0-6ubuntu1.2.debian.tar.xz' bash_5.0-6ubuntu1.2.debian.tar.xz 75200 SHA512:50de22a6cd140fcb95eca9172e9927a4eeddd90bfbd23072d5e209db1675f331716dfd54ef3281caa7020e3fa1aef9ca7caafc6a8d3067741b1ae41f7dff7724
```

### `dpkg` source package: `binutils=2.34-6ubuntu1.11`

Binary Packages:

- `binutils=2.34-6ubuntu1.11`
- `binutils-common:amd64=2.34-6ubuntu1.11`
- `binutils-x86-64-linux-gnu=2.34-6ubuntu1.11`
- `libbinutils:amd64=2.34-6ubuntu1.11`
- `libctf-nobfd0:amd64=2.34-6ubuntu1.11`
- `libctf0:amd64=2.34-6ubuntu1.11`

Licenses: (parsed from: `/usr/share/doc/binutils/copyright`, `/usr/share/doc/binutils-common/copyright`, `/usr/share/doc/binutils-x86-64-linux-gnu/copyright`, `/usr/share/doc/libbinutils/copyright`, `/usr/share/doc/libctf-nobfd0/copyright`, `/usr/share/doc/libctf0/copyright`)

- `GFDL`
- `GPL`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris binutils=2.34-6ubuntu1.11
'http://archive.ubuntu.com/ubuntu/pool/main/b/binutils/binutils_2.34-6ubuntu1.11.dsc' binutils_2.34-6ubuntu1.11.dsc 8833 SHA512:c5ac1761861a8d0a0d2149abd89f1e6fbd76c531f7a5614c926e2a32274470fc9c1f0abcb2780a8a2869097924aa82be694c0ff77b50843726811faf0f315294
'http://archive.ubuntu.com/ubuntu/pool/main/b/binutils/binutils_2.34.orig.tar.xz' binutils_2.34.orig.tar.xz 21637796 SHA512:2c7976939dcf5e8c5b7374cccd39bfe803b1bec73c6abfa0eb17c24e1942574c6bdb874c66a092a82adc443182eacd8a5a8001c19a76101f0c7ba40c27de0bbd
'http://archive.ubuntu.com/ubuntu/pool/main/b/binutils/binutils_2.34-6ubuntu1.11.debian.tar.xz' binutils_2.34-6ubuntu1.11.debian.tar.xz 189512 SHA512:4ad2ee0c6d64eccf3aea73c507a2a2f5092a41f2e2793de4a0c65e83319c63f49174dea2edaaba290bbba3f752367f500d6d72b6ba7db22044a8296ae2a27ff0
```

### `dpkg` source package: `brotli=1.0.7-6ubuntu0.1`

Binary Packages:

- `libbrotli1:amd64=1.0.7-6ubuntu0.1`

Licenses: (parsed from: `/usr/share/doc/libbrotli1/copyright`)

- `MIT`

Source:

```console
$ apt-get source -qq --print-uris brotli=1.0.7-6ubuntu0.1
'http://archive.ubuntu.com/ubuntu/pool/main/b/brotli/brotli_1.0.7-6ubuntu0.1.dsc' brotli_1.0.7-6ubuntu0.1.dsc 2385 SHA512:139a93e110c6cf50531bdfee5ec4a8751ca81d1e02d2f38b21c1a9a478064286ddeb6bfdf20af488f7e2f53219cf460a00e68b77ef1b860fbf0df67f300d303b
'http://archive.ubuntu.com/ubuntu/pool/main/b/brotli/brotli_1.0.7.orig.tar.gz' brotli_1.0.7.orig.tar.gz 23827908 SHA512:a82362aa36d2f2094bca0b2808d9de0d57291fb3a4c29d7c0ca0a37e73087ec5ac4df299c8c363e61106fccf2fe7f58b5cf76eb97729e2696058ef43b1d3930a
'http://archive.ubuntu.com/ubuntu/pool/main/b/brotli/brotli_1.0.7-6ubuntu0.1.debian.tar.xz' brotli_1.0.7-6ubuntu0.1.debian.tar.xz 13672 SHA512:eb24ee68d0a699bb8f382c7f80c313e0bb26bea6b22f74bf01af236eafe345cf602f7544da4a74eb8c8f70defcd6b867018df97a96e5e894535cf731400edaa8
```

### `dpkg` source package: `build-essential=12.8ubuntu1.1`

Binary Packages:

- `build-essential=12.8ubuntu1.1`

Licenses: (parsed from: `/usr/share/doc/build-essential/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris build-essential=12.8ubuntu1.1
'http://archive.ubuntu.com/ubuntu/pool/main/b/build-essential/build-essential_12.8ubuntu1.1.dsc' build-essential_12.8ubuntu1.1.dsc 2396 SHA512:b81700924952c944238b82f379ef95c853a08b3e608876df175b5a72585dc9ce7f603b731c266eaf488f406fd791fc2442e6f946b7bb07a2528c020867bf4c46
'http://archive.ubuntu.com/ubuntu/pool/main/b/build-essential/build-essential_12.8ubuntu1.1.tar.xz' build-essential_12.8ubuntu1.1.tar.xz 51248 SHA512:0276dcfb84a9e041b4e65cc79cb5f5a6970ecadd3de866a53d19b607d936b3aff91f3355ff7513ed327e28db002ad6267ff8b828e79be79056b46bb0952c86a6
```

### `dpkg` source package: `bullet=2.88+dfsg-2build2`

Binary Packages:

- `libbullet-dev:amd64=2.88+dfsg-2build2`
- `libbullet2.88:amd64=2.88+dfsg-2build2`

Licenses: (parsed from: `/usr/share/doc/libbullet-dev/copyright`, `/usr/share/doc/libbullet2.88/copyright`)

- `Apache-2.0`
- `BSD-2-clause`
- `BSD-3-clause`
- `BSL-1.0`
- `Elsevier-CDROM-License`
- `Expat`
- `GNU-All-Permissive-License`
- `GPL-2`
- `GPL-2+`
- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris bullet=2.88+dfsg-2build2
'http://archive.ubuntu.com/ubuntu/pool/universe/b/bullet/bullet_2.88%2bdfsg-2build2.dsc' bullet_2.88+dfsg-2build2.dsc 2399 SHA256:9016ee49e56110f633a5a9927653d79e77b6c0b288de16717ebd5c5d9efedeaf
'http://archive.ubuntu.com/ubuntu/pool/universe/b/bullet/bullet_2.88%2bdfsg.orig.tar.xz' bullet_2.88+dfsg.orig.tar.xz 2991880 SHA256:02ed84bfcbc5b63397ca2c5e03962d0a1e6f05a31a2a2aa0f96db281f8bfd88e
'http://archive.ubuntu.com/ubuntu/pool/universe/b/bullet/bullet_2.88%2bdfsg-2build2.debian.tar.xz' bullet_2.88+dfsg-2build2.debian.tar.xz 12864 SHA256:5b46ceec34db826eaddde72cfd2f0b91017b9d836015fb38ad67fe0d4f3d6dfe
```

### `dpkg` source package: `bzip2=1.0.8-2`

Binary Packages:

- `bzip2=1.0.8-2`
- `libbz2-1.0:amd64=1.0.8-2`

Licenses: (parsed from: `/usr/share/doc/bzip2/copyright`, `/usr/share/doc/libbz2-1.0/copyright`)

- `BSD-variant`
- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris bzip2=1.0.8-2
'http://archive.ubuntu.com/ubuntu/pool/main/b/bzip2/bzip2_1.0.8-2.dsc' bzip2_1.0.8-2.dsc 2180 SHA256:646cdcbb786a89a647cfafb280ef467143c06c445c4bf6fe69ec4a7882943064
'http://archive.ubuntu.com/ubuntu/pool/main/b/bzip2/bzip2_1.0.8.orig.tar.gz' bzip2_1.0.8.orig.tar.gz 810029 SHA256:ab5a03176ee106d3f0fa90e381da478ddae405918153cca248e682cd0c4a2269
'http://archive.ubuntu.com/ubuntu/pool/main/b/bzip2/bzip2_1.0.8-2.debian.tar.bz2' bzip2_1.0.8-2.debian.tar.bz2 26032 SHA256:237c8619bc9bc16f357b1077064a3e58aa1a230dadb4b9bb3bd8dc8f454afc0b
```

### `dpkg` source package: `ca-certificates=20240203~20.04.1`

Binary Packages:

- `ca-certificates=20240203~20.04.1`

Licenses: (parsed from: `/usr/share/doc/ca-certificates/copyright`)

- `GPL-2`
- `GPL-2+`
- `MPL-2.0`

Source:

```console
$ apt-get source -qq --print-uris ca-certificates=20240203~20.04.1
'http://archive.ubuntu.com/ubuntu/pool/main/c/ca-certificates/ca-certificates_20240203%7e20.04.1.dsc' ca-certificates_20240203~20.04.1.dsc 1850 SHA512:a5824851813f0c9994a26fa02c88f7c027e4ba6d2391274b11b5b12951460564d422595b386baa59ed0d81c4028089cd5ebfc6a1ab19874c0dbcc87e3aea26a2
'http://archive.ubuntu.com/ubuntu/pool/main/c/ca-certificates/ca-certificates_20240203%7e20.04.1.tar.xz' ca-certificates_20240203~20.04.1.tar.xz 263352 SHA512:a0d2af75999aa73500f34f7f36e3dbdc0a5dedf56713727531afd67f9c680ff28510fc2427056c9f7291afd9f17cccbb1ee906512e2955824a97b4c65b7889b9
```

### `dpkg` source package: `cairo=1.16.0-4ubuntu1`

Binary Packages:

- `libcairo2:amd64=1.16.0-4ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libcairo2/copyright`)

- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris cairo=1.16.0-4ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/c/cairo/cairo_1.16.0-4ubuntu1.dsc' cairo_1.16.0-4ubuntu1.dsc 2950 SHA256:f53596e412c2e1799d5e7e1c414d7db2cade33ba85fd912d39f60525b5a2e23b
'http://archive.ubuntu.com/ubuntu/pool/main/c/cairo/cairo_1.16.0.orig.tar.xz' cairo_1.16.0.orig.tar.xz 41997432 SHA256:5e7b29b3f113ef870d1e3ecf8adf21f923396401604bda16d44be45e66052331
'http://archive.ubuntu.com/ubuntu/pool/main/c/cairo/cairo_1.16.0-4ubuntu1.debian.tar.xz' cairo_1.16.0-4ubuntu1.debian.tar.xz 30416 SHA256:3725774f0a3f244a8b910e5a5e46bc731ee87372c6effb6c5af2d0db65c64426
```

### `dpkg` source package: `cdebconf=0.251ubuntu1`

Binary Packages:

- `libdebconfclient0:amd64=0.251ubuntu1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris cdebconf=0.251ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/c/cdebconf/cdebconf_0.251ubuntu1.dsc' cdebconf_0.251ubuntu1.dsc 2858 SHA256:0753b98ec773e743de19d393f444a8b88915ad75340cc58007eb7c309031121d
'http://archive.ubuntu.com/ubuntu/pool/main/c/cdebconf/cdebconf_0.251ubuntu1.tar.xz' cdebconf_0.251ubuntu1.tar.xz 276744 SHA256:d07848e52aecb70e82d8bafd082ecee3cccd7a8229b59527e07cc49023aa22d0
```

### `dpkg` source package: `cmake=3.16.3-1ubuntu1.20.04.1`

Binary Packages:

- `cmake=3.16.3-1ubuntu1.20.04.1`
- `cmake-data=3.16.3-1ubuntu1.20.04.1`

Licenses: (parsed from: `/usr/share/doc/cmake/copyright`, `/usr/share/doc/cmake-data/copyright`)

- `Apache-2.0`
- `BSD-2-clause`
- `BSD-3-clause`
- `BSD-4-clause`
- `GPL-2`
- `GPL-2+with_exception`
- `GPL-3`
- `GPL-3+with_exception`
- `ISC`
- `MIT-like`
- `zlib`

Source:

```console
$ apt-get source -qq --print-uris cmake=3.16.3-1ubuntu1.20.04.1
'http://archive.ubuntu.com/ubuntu/pool/main/c/cmake/cmake_3.16.3-1ubuntu1.20.04.1.dsc' cmake_3.16.3-1ubuntu1.20.04.1.dsc 3185 SHA512:ad2fbc3f429e1f652709d84284908cc7e263dbc85321d8abc88ba5533352487e0ac16c98087be77b2215ca2b6709ae04dfdb37bde151951da7c745c2569bfc42
'http://archive.ubuntu.com/ubuntu/pool/main/c/cmake/cmake_3.16.3.orig.tar.gz' cmake_3.16.3.orig.tar.gz 9111826 SHA512:ca9e0a142369735ef6469afb97f4463c981404bd59c7d48c1ef454dd705460a31a5dcffa4949b84b1ac723f5b7e79d67b250126fb42e1f15dab0ac2a17603672
'http://archive.ubuntu.com/ubuntu/pool/main/c/cmake/cmake_3.16.3-1ubuntu1.20.04.1.debian.tar.xz' cmake_3.16.3-1ubuntu1.20.04.1.debian.tar.xz 31164 SHA512:9fdbd91417d770f444cce1f49ee883ad702be8e748d8cdb7dc6ec84b69d9aeea09adf5c40a8784495f5cf26cec9a3be6f47665632c137689c4e7eb590b936fc3
```

### `dpkg` source package: `console-bridge=0.4.4+dfsg-1build1`

Binary Packages:

- `libconsole-bridge-dev:amd64=0.4.4+dfsg-1build1`
- `libconsole-bridge0.4:amd64=0.4.4+dfsg-1build1`

Licenses: (parsed from: `/usr/share/doc/libconsole-bridge-dev/copyright`, `/usr/share/doc/libconsole-bridge0.4/copyright`)

- `BSD-3-clause`

Source:

```console
$ apt-get source -qq --print-uris console-bridge=0.4.4+dfsg-1build1
'http://archive.ubuntu.com/ubuntu/pool/universe/c/console-bridge/console-bridge_0.4.4%2bdfsg-1build1.dsc' console-bridge_0.4.4+dfsg-1build1.dsc 2306 SHA256:fcdc1bde378e17db69a32bab6bb8f93161c8e1f58c0f47063f4a8dd2bec002b2
'http://archive.ubuntu.com/ubuntu/pool/universe/c/console-bridge/console-bridge_0.4.4%2bdfsg.orig.tar.xz' console-bridge_0.4.4+dfsg.orig.tar.xz 5688 SHA256:8fc6dacfeed0b67bb0fa96b8822b0f120961ff12830d1bee61f70cf5f3cbcb53
'http://archive.ubuntu.com/ubuntu/pool/universe/c/console-bridge/console-bridge_0.4.4%2bdfsg-1build1.debian.tar.xz' console-bridge_0.4.4+dfsg-1build1.debian.tar.xz 3744 SHA256:6033acc38324729d3cbff79210149ddc38be28ac2bfbcf703d352845314c49e3
```

### `dpkg` source package: `coreutils=8.30-3ubuntu2`

Binary Packages:

- `coreutils=8.30-3ubuntu2`

Licenses: (parsed from: `/usr/share/doc/coreutils/copyright`)

- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris coreutils=8.30-3ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/c/coreutils/coreutils_8.30-3ubuntu2.dsc' coreutils_8.30-3ubuntu2.dsc 2048 SHA256:f36fe0ac14978b240a750b79d2bbd737d6b1939296c3a287899933aa2a1906ea
'http://archive.ubuntu.com/ubuntu/pool/main/c/coreutils/coreutils_8.30.orig.tar.xz' coreutils_8.30.orig.tar.xz 5359532 SHA256:e831b3a86091496cdba720411f9748de81507798f6130adeaef872d206e1b057
'http://archive.ubuntu.com/ubuntu/pool/main/c/coreutils/coreutils_8.30-3ubuntu2.debian.tar.xz' coreutils_8.30-3ubuntu2.debian.tar.xz 39636 SHA256:98204ef9d94e5c567880cd0245fdb7940eaf7592d6c6830c300ad117628b351f
```

### `dpkg` source package: `cppcheck=1.90-4build1`

Binary Packages:

- `cppcheck=1.90-4build1`

Licenses: (parsed from: `/usr/share/doc/cppcheck/copyright`)

- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `ZLIB`

Source:

```console
$ apt-get source -qq --print-uris cppcheck=1.90-4build1
'http://archive.ubuntu.com/ubuntu/pool/universe/c/cppcheck/cppcheck_1.90-4build1.dsc' cppcheck_1.90-4build1.dsc 2070 SHA256:9cc46ce18123a609993a24e30bf02375b44bc6e24e416ea648353c599472932c
'http://archive.ubuntu.com/ubuntu/pool/universe/c/cppcheck/cppcheck_1.90.orig.tar.gz' cppcheck_1.90.orig.tar.gz 2543978 SHA256:59a94e2e9f10097b7246b26541fb63d41846a14cfa92ca0c4259c151998691ee
'http://archive.ubuntu.com/ubuntu/pool/universe/c/cppcheck/cppcheck_1.90-4build1.debian.tar.xz' cppcheck_1.90-4build1.debian.tar.xz 11404 SHA256:67ebd147f808dc6837c5eddab3d6f707a5cdf09e7ec1750223d29bd961e1b48e
```

### `dpkg` source package: `curl=7.68.0-1ubuntu2.25`

Binary Packages:

- `curl=7.68.0-1ubuntu2.25`
- `libcurl3-gnutls:amd64=7.68.0-1ubuntu2.25`
- `libcurl4:amd64=7.68.0-1ubuntu2.25`

Licenses: (parsed from: `/usr/share/doc/curl/copyright`, `/usr/share/doc/libcurl3-gnutls/copyright`, `/usr/share/doc/libcurl4/copyright`)

- `BSD-3-Clause`
- `BSD-4-Clause`
- `ISC`
- `curl`
- `other`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris curl=7.68.0-1ubuntu2.25
'http://archive.ubuntu.com/ubuntu/pool/main/c/curl/curl_7.68.0-1ubuntu2.25.dsc' curl_7.68.0-1ubuntu2.25.dsc 2737 SHA512:662f204efe6ad8fce4c4115cc6788c96084be2989440dbfd38ebf9cd02114581b237e8ac8caa555489b5d5bb55a84eb7b84f071e3f5bc52e36e94e098b4a9313
'http://archive.ubuntu.com/ubuntu/pool/main/c/curl/curl_7.68.0.orig.tar.gz' curl_7.68.0.orig.tar.gz 4096350 SHA512:58b42c08b1cf4cb6e68f8e469d5b5f6298eebe286ba2677ad29e1a7eefd15b8609af54544f4c5a7dadebbd3b23bd77700830f2f60fbea7ae3f2f306e640010b0
'http://archive.ubuntu.com/ubuntu/pool/main/c/curl/curl_7.68.0-1ubuntu2.25.debian.tar.xz' curl_7.68.0-1ubuntu2.25.debian.tar.xz 77412 SHA512:ed0c6526b6b35fd16a4264cf89cf9008585b7fb6785a36506b31bb9834285567aed856712967215e4f5e0e3a2cf917a70f8de9c83a1f5c6582b1042f5ebff16d
```

### `dpkg` source package: `cyrus-sasl2=2.1.27+dfsg-2ubuntu0.1`

Binary Packages:

- `libsasl2-2:amd64=2.1.27+dfsg-2ubuntu0.1`
- `libsasl2-modules-db:amd64=2.1.27+dfsg-2ubuntu0.1`

Licenses: (parsed from: `/usr/share/doc/libsasl2-2/copyright`, `/usr/share/doc/libsasl2-modules-db/copyright`)

- `BSD-4-clause`
- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris cyrus-sasl2=2.1.27+dfsg-2ubuntu0.1
'http://archive.ubuntu.com/ubuntu/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.27%2bdfsg-2ubuntu0.1.dsc' cyrus-sasl2_2.1.27+dfsg-2ubuntu0.1.dsc 3511 SHA512:70d73c119ef8986adbb0b8f52be7459f756ea8f8e2bf836b2c57e5230f63052999cd716d6585d4b1d65f854a471afbc0f344e88759e99c5ea129b82216400903
'http://archive.ubuntu.com/ubuntu/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.27%2bdfsg.orig.tar.xz' cyrus-sasl2_2.1.27+dfsg.orig.tar.xz 2058596 SHA512:a795e4362f85a50e223c5456d03526832eb29fdbc9e17a767045f8542638e3f987d382b79b072bcd694bd1a12cbb818cff6c326063ca2bbe05453c1acf7fb8ad
'http://archive.ubuntu.com/ubuntu/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.27%2bdfsg-2ubuntu0.1.debian.tar.xz' cyrus-sasl2_2.1.27+dfsg-2ubuntu0.1.debian.tar.xz 100804 SHA512:391bfecc0859839514a320739b93555f44e1101042d262c9c3c3623a5e1a73ca304f9509bd8bc2d62e691dc4c15570e8af5a52c97483fff8600d48eeb13ca518
```

### `dpkg` source package: `dash=0.5.10.2-6`

Binary Packages:

- `dash=0.5.10.2-6`

Licenses: (parsed from: `/usr/share/doc/dash/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris dash=0.5.10.2-6
'http://archive.ubuntu.com/ubuntu/pool/main/d/dash/dash_0.5.10.2-6.dsc' dash_0.5.10.2-6.dsc 1756 SHA256:d509a23ebdc4f107c911914590c1400e5a24383f35c5d6904e48d2afeff168ac
'http://archive.ubuntu.com/ubuntu/pool/main/d/dash/dash_0.5.10.2.orig.tar.gz' dash_0.5.10.2.orig.tar.gz 225196 SHA256:3c663919dc5c66ec991da14c7cf7e0be8ad00f3db73986a987c118862b5f6071
'http://archive.ubuntu.com/ubuntu/pool/main/d/dash/dash_0.5.10.2-6.debian.tar.xz' dash_0.5.10.2-6.debian.tar.xz 44232 SHA256:1448fbfc2541be52787da81ce03bb81ad6b1f380cba1b7e747abefdcd44f6c86
```

### `dpkg` source package: `db5.3=5.3.28+dfsg1-0.6ubuntu2`

Binary Packages:

- `libdb5.3:amd64=5.3.28+dfsg1-0.6ubuntu2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris db5.3=5.3.28+dfsg1-0.6ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/d/db5.3/db5.3_5.3.28%2bdfsg1-0.6ubuntu2.dsc' db5.3_5.3.28+dfsg1-0.6ubuntu2.dsc 3245 SHA256:d879f4921a2f573132031d9371f0eb020005bdce48d6e12b436bf3515dda8663
'http://archive.ubuntu.com/ubuntu/pool/main/d/db5.3/db5.3_5.3.28%2bdfsg1.orig.tar.xz' db5.3_5.3.28+dfsg1.orig.tar.xz 19723860 SHA256:b19bf3dd8ce74b95a7b215be9a7c8489e8e8f18da60d64d6340a06e75f497749
'http://archive.ubuntu.com/ubuntu/pool/main/d/db5.3/db5.3_5.3.28%2bdfsg1-0.6ubuntu2.debian.tar.xz' db5.3_5.3.28+dfsg1-0.6ubuntu2.debian.tar.xz 30172 SHA256:e606e7827f077efc92afc6f0d43c921fab4577d619eab06fab23182aefab7506
```

### `dpkg` source package: `dbus-python=1.2.16-1build1`

Binary Packages:

- `python3-dbus=1.2.16-1build1`

Licenses: (parsed from: `/usr/share/doc/python3-dbus/copyright`)

- `AFL-2.1`
- `Expat`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris dbus-python=1.2.16-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/d/dbus-python/dbus-python_1.2.16-1build1.dsc' dbus-python_1.2.16-1build1.dsc 3641 SHA256:8ecda77e26175c8f2fa6b8960e89161cd2571e3aa4f9d1580f1f1a3136b35a97
'http://archive.ubuntu.com/ubuntu/pool/main/d/dbus-python/dbus-python_1.2.16.orig.tar.gz' dbus-python_1.2.16.orig.tar.gz 576701 SHA256:11238f1d86c995d8aed2e22f04a1e3779f0d70e587caffeab4857f3c662ed5a4
'http://archive.ubuntu.com/ubuntu/pool/main/d/dbus-python/dbus-python_1.2.16.orig.tar.gz.asc' dbus-python_1.2.16.orig.tar.gz.asc 833 SHA256:0fcfcb9844226c5cde1690b74b3c094d802ea735392d3a8829f1b5993837e86c
'http://archive.ubuntu.com/ubuntu/pool/main/d/dbus-python/dbus-python_1.2.16-1build1.debian.tar.xz' dbus-python_1.2.16-1build1.debian.tar.xz 34532 SHA256:691fd294a727e96250e084ba3ee388d9e226b2808ce1edf58d1782000dbe1425
```

### `dpkg` source package: `dbus=1.12.16-2ubuntu2.3`

Binary Packages:

- `libdbus-1-3:amd64=1.12.16-2ubuntu2.3`

Licenses: (parsed from: `/usr/share/doc/libdbus-1-3/copyright`)

- `AFL-2.1`
- `AFL-2.1,`
- `BSD-3-clause`
- `BSD-3-clause-generic`
- `Expat`
- `GPL-2`
- `GPL-2+`
- `Tcl-BSDish`
- `g10-permissive`

Source:

```console
$ apt-get source -qq --print-uris dbus=1.12.16-2ubuntu2.3
'http://archive.ubuntu.com/ubuntu/pool/main/d/dbus/dbus_1.12.16-2ubuntu2.3.dsc' dbus_1.12.16-2ubuntu2.3.dsc 3737 SHA512:cfdecfc26b17ae7a5e8f4e68ba3fe21109dcb93886e65187606be2f37f9d43ce76b677cfca438805165feab4b8d8db6d981b6dc3d1c04263e391bda18a90784c
'http://archive.ubuntu.com/ubuntu/pool/main/d/dbus/dbus_1.12.16.orig.tar.gz' dbus_1.12.16.orig.tar.gz 2093296 SHA512:27ae805170e9515a8bb0fba5f29d414edc70e3b6b28b7b65bbea47035b8eafa9ac4820cdc92645be6035f6748f8aa45679e1ffc84ba74a64859a3056d318b9bb
'http://archive.ubuntu.com/ubuntu/pool/main/d/dbus/dbus_1.12.16.orig.tar.gz.asc' dbus_1.12.16.orig.tar.gz.asc 833 SHA512:6d19bf7be86ae1dc70550ba472e5761f3ed1a71007c00679e3a586d567776e82cf9869c9a7021c1324990615657a054b949dc5bbd8e60b0a8843ef6d977eda24
'http://archive.ubuntu.com/ubuntu/pool/main/d/dbus/dbus_1.12.16-2ubuntu2.3.debian.tar.xz' dbus_1.12.16-2ubuntu2.3.debian.tar.xz 73812 SHA512:21319e8a84d5206522a9b65ee81878cecb73cbfda839758987c2a96c7f2c258efe8165d0980f293d5be22ac1659afafb5cd727b09408d4da4057569f7a42ef39
```

### `dpkg` source package: `debconf=1.5.73`

Binary Packages:

- `debconf=1.5.73`

Licenses: (parsed from: `/usr/share/doc/debconf/copyright`)

- `BSD-2-clause`

Source:

```console
$ apt-get source -qq --print-uris debconf=1.5.73
'http://archive.ubuntu.com/ubuntu/pool/main/d/debconf/debconf_1.5.73.dsc' debconf_1.5.73.dsc 2081 SHA256:cdd4c049414cd167a4a9479d883e205bf5cebb19fc4bb6f132000a56291eb670
'http://archive.ubuntu.com/ubuntu/pool/main/d/debconf/debconf_1.5.73.tar.xz' debconf_1.5.73.tar.xz 570780 SHA256:513895b2b77d9fb72542152390e7d4c67fe1e08de75fdad44d54ce1e7d83ecef
```

### `dpkg` source package: `debianutils=4.9.1`

Binary Packages:

- `debianutils=4.9.1`

Licenses: (parsed from: `/usr/share/doc/debianutils/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris debianutils=4.9.1
'http://archive.ubuntu.com/ubuntu/pool/main/d/debianutils/debianutils_4.9.1.dsc' debianutils_4.9.1.dsc 1592 SHA256:d30866ea0352263fa7756010e8743ade350024b2fd491bc5befcbaa9a97626b7
'http://archive.ubuntu.com/ubuntu/pool/main/d/debianutils/debianutils_4.9.1.tar.xz' debianutils_4.9.1.tar.xz 157516 SHA256:af826685d9c56abfa873e84cd392539cd363cb0ba04a09d21187377e1b764091
```

### `dpkg` source package: `diffutils=1:3.7-3`

Binary Packages:

- `diffutils=1:3.7-3`

Licenses: (parsed from: `/usr/share/doc/diffutils/copyright`)

- `GFDL`
- `GPL`

Source:

```console
$ apt-get source -qq --print-uris diffutils=1:3.7-3
'http://archive.ubuntu.com/ubuntu/pool/main/d/diffutils/diffutils_3.7-3.dsc' diffutils_3.7-3.dsc 1453 SHA256:99dee94cec05454a65a9cb542bea1720dbd4c511d13f9784c9e3741e76a9b9ba
'http://archive.ubuntu.com/ubuntu/pool/main/d/diffutils/diffutils_3.7.orig.tar.xz' diffutils_3.7.orig.tar.xz 1448828 SHA256:b3a7a6221c3dc916085f0d205abf6b8e1ba443d4dd965118da364a1dc1cb3a26
'http://archive.ubuntu.com/ubuntu/pool/main/d/diffutils/diffutils_3.7-3.debian.tar.xz' diffutils_3.7-3.debian.tar.xz 11116 SHA256:a455228f12283b5f3c0165db4ab9b12071adc37fb9dd50dcb5e1b8851c524f1f
```

### `dpkg` source package: `distlib=0.3.0-1`

Binary Packages:

- `python3-distlib=0.3.0-1`

Licenses: (parsed from: `/usr/share/doc/python3-distlib/copyright`)

- `BSD-3-clause`
- `Python`

Source:

```console
$ apt-get source -qq --print-uris distlib=0.3.0-1
'http://archive.ubuntu.com/ubuntu/pool/universe/d/distlib/distlib_0.3.0-1.dsc' distlib_0.3.0-1.dsc 1808 SHA256:32f4bccc2f0634c40851cf9d67660e5e25d162b3e5e418904926ea2502d3065a
'http://archive.ubuntu.com/ubuntu/pool/universe/d/distlib/distlib_0.3.0.orig.tar.xz' distlib_0.3.0.orig.tar.xz 347040 SHA256:17d65941aafec32a187cfed56a3985ef68e5ca452ba30821299eee47929d696c
'http://archive.ubuntu.com/ubuntu/pool/universe/d/distlib/distlib_0.3.0-1.debian.tar.xz' distlib_0.3.0-1.debian.tar.xz 6388 SHA256:5da6fe7efcb3aeed405250f00f73d8a4fc9e1c71fdc9d169e09e97b55a21d25c
```

### `dpkg` source package: `distro-info-data=0.43ubuntu1.18`

Binary Packages:

- `distro-info-data=0.43ubuntu1.18`

Licenses: (parsed from: `/usr/share/doc/distro-info-data/copyright`)

- `ISC`

Source:

```console
$ apt-get source -qq --print-uris distro-info-data=0.43ubuntu1.18
'http://archive.ubuntu.com/ubuntu/pool/main/d/distro-info-data/distro-info-data_0.43ubuntu1.18.dsc' distro-info-data_0.43ubuntu1.18.dsc 1742 SHA512:f4b124f46ce52e4b7b01fb93646194990239b90ae28259f72d070900d8c8a501110cceb39255bba3b98c1ba26295163c350128d80c05ab8f9fa83f8a49eb7079
'http://archive.ubuntu.com/ubuntu/pool/main/d/distro-info-data/distro-info-data_0.43ubuntu1.18.tar.xz' distro-info-data_0.43ubuntu1.18.tar.xz 8572 SHA512:4df60c1ffd83f8c85e255126cb6399669bdf966a02246712b361d37286b3c34b0734a63e5404ca920912b1fff75efea0f955252cb76a4d5054523532d4a3bac4
```

### `dpkg` source package: `dpkg=1.19.7ubuntu3.2`

Binary Packages:

- `dpkg=1.19.7ubuntu3.2`
- `dpkg-dev=1.19.7ubuntu3.2`
- `libdpkg-perl=1.19.7ubuntu3.2`

Licenses: (parsed from: `/usr/share/doc/dpkg/copyright`, `/usr/share/doc/dpkg-dev/copyright`, `/usr/share/doc/libdpkg-perl/copyright`)

- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`
- `public-domain-md5`
- `public-domain-s-s-d`

Source:

```console
$ apt-get source -qq --print-uris dpkg=1.19.7ubuntu3.2
'http://archive.ubuntu.com/ubuntu/pool/main/d/dpkg/dpkg_1.19.7ubuntu3.2.dsc' dpkg_1.19.7ubuntu3.2.dsc 2237 SHA512:7784d9d17a2bd5d85a776a2d744bd496630dcd8bb83e2986ff76adef2596e8e1ab1ad809c282049c44b25cebb90b5d2ef59c2cafbad4dd5f8ffbcc475b263f3b
'http://archive.ubuntu.com/ubuntu/pool/main/d/dpkg/dpkg_1.19.7ubuntu3.2.tar.xz' dpkg_1.19.7ubuntu3.2.tar.xz 4732068 SHA512:a69c51b04fe52ca5ca44111baf83eeaff4cf5167f5322a4c1a7671dc4a6ce5e25095bad73ff4d9c197427d21f3bf1a246f99007dde8890f33c79bb572f7f95fc
```

### `dpkg` source package: `e2fsprogs=1.45.5-2ubuntu1.2`

Binary Packages:

- `e2fsprogs=1.45.5-2ubuntu1.2`
- `libcom-err2:amd64=1.45.5-2ubuntu1.2`
- `libext2fs2:amd64=1.45.5-2ubuntu1.2`
- `libss2:amd64=1.45.5-2ubuntu1.2`
- `logsave=1.45.5-2ubuntu1.2`

Licenses: (parsed from: `/usr/share/doc/e2fsprogs/copyright`, `/usr/share/doc/libcom-err2/copyright`, `/usr/share/doc/libext2fs2/copyright`, `/usr/share/doc/libss2/copyright`, `/usr/share/doc/logsave/copyright`)

- `GPL-2`
- `LGPL-2`

Source:

```console
$ apt-get source -qq --print-uris e2fsprogs=1.45.5-2ubuntu1.2
'http://archive.ubuntu.com/ubuntu/pool/main/e/e2fsprogs/e2fsprogs_1.45.5-2ubuntu1.2.dsc' e2fsprogs_1.45.5-2ubuntu1.2.dsc 3313 SHA512:b2637335d3247a54443d0967e994929adb52954277b1029a15292bc6fdc8db1ea00d5e2a6089c0b7a8419bfcff58cb60a6a7281d286265b4868d921d8daa0858
'http://archive.ubuntu.com/ubuntu/pool/main/e/e2fsprogs/e2fsprogs_1.45.5.orig.tar.gz' e2fsprogs_1.45.5.orig.tar.gz 7938826 SHA512:3ddb8d8aedfa68e1684d77e2bdd3cbbc16b2fbc633945a72ba617bea76c13253f3afa50655216a4071d787382272381b992cd6e7e3747780a5c3a64343158c98
'http://archive.ubuntu.com/ubuntu/pool/main/e/e2fsprogs/e2fsprogs_1.45.5.orig.tar.gz.asc' e2fsprogs_1.45.5.orig.tar.gz.asc 488 SHA512:1e3a19cf7943927c5e12ef3963a50af177e5627d9aa1c3eb081adb8e4671e46df3b6d512f6fcac002204d59b68716d94b04286d2cd85142a336c06bf28eaf3e1
'http://archive.ubuntu.com/ubuntu/pool/main/e/e2fsprogs/e2fsprogs_1.45.5-2ubuntu1.2.debian.tar.xz' e2fsprogs_1.45.5-2ubuntu1.2.debian.tar.xz 82932 SHA512:e038c9aa3af0593a6240840145b53742dbb2718dd58975e507b625eef3e341e5989ae0c7f02805a30ad213066af1cbfe8138f6baf500eedf66301dcb0966cb29
```

### `dpkg` source package: `eigen3=3.3.7-2`

Binary Packages:

- `libeigen3-dev=3.3.7-2`

Licenses: (parsed from: `/usr/share/doc/libeigen3-dev/copyright`)

- `BSD-3-clause`
- `LGPL-2.1`
- `LGPL-2.1+`
- `MPL-2`

Source:

```console
$ apt-get source -qq --print-uris eigen3=3.3.7-2
'http://archive.ubuntu.com/ubuntu/pool/universe/e/eigen3/eigen3_3.3.7-2.dsc' eigen3_3.3.7-2.dsc 2155 SHA256:9e2d13f3932ba7023c3ee9af4969dec19c0411aebe0711b5fcd6ce1386f2a85a
'http://archive.ubuntu.com/ubuntu/pool/universe/e/eigen3/eigen3_3.3.7.orig.tar.bz2' eigen3_3.3.7.orig.tar.bz2 1665168 SHA256:9f13cf90dedbe3e52a19f43000d71fdf72e986beb9a5436dddcd61ff9d77a3ce
'http://archive.ubuntu.com/ubuntu/pool/universe/e/eigen3/eigen3_3.3.7-2.debian.tar.xz' eigen3_3.3.7-2.debian.tar.xz 47904 SHA256:4385fbf5d17443dbc86884bb5d0a3aa5410b182db2f3ae9e983bc3120699d679
```

### `dpkg` source package: `empy=3.3.2-5.1`

Binary Packages:

- `python3-empy=3.3.2-5.1`

Licenses: (parsed from: `/usr/share/doc/python3-empy/copyright`)

- `GPL-2`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris empy=3.3.2-5.1
'http://archive.ubuntu.com/ubuntu/pool/universe/e/empy/empy_3.3.2-5.1.dsc' empy_3.3.2-5.1.dsc 2029 SHA256:529b5cbe61f295b7319e6f5209ac43447f505712c8a5956c9e3fe8c38a4f5de1
'http://archive.ubuntu.com/ubuntu/pool/universe/e/empy/empy_3.3.2.orig.tar.gz' empy_3.3.2.orig.tar.gz 138168 SHA256:99f016af2770c48ab57a65df7aae251360dc69a1514c15851458a71d4ddfea9c
'http://archive.ubuntu.com/ubuntu/pool/universe/e/empy/empy_3.3.2-5.1.debian.tar.xz' empy_3.3.2-5.1.debian.tar.xz 6896 SHA256:aa7d17e4f817d11418ca8669d5b366760853321701a14f5b686770a99cd192e8
```

### `dpkg` source package: `entrypoints=0.3-2ubuntu1`

Binary Packages:

- `python3-entrypoints=0.3-2ubuntu1`

Licenses: (parsed from: `/usr/share/doc/python3-entrypoints/copyright`)

- `Expat`

Source:

```console
$ apt-get source -qq --print-uris entrypoints=0.3-2ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/e/entrypoints/entrypoints_0.3-2ubuntu1.dsc' entrypoints_0.3-2ubuntu1.dsc 2242 SHA256:69e33fc89731b3c98f89b349a470ae7d3adc16c1cf3e95ae3b636ca05fc535f6
'http://archive.ubuntu.com/ubuntu/pool/main/e/entrypoints/entrypoints_0.3.orig.tar.gz' entrypoints_0.3.orig.tar.gz 11870 SHA256:f26eddc371e37d8e9f6663b77524d6731567f005bd1e4ac950c0e33c48fbc065
'http://archive.ubuntu.com/ubuntu/pool/main/e/entrypoints/entrypoints_0.3-2ubuntu1.debian.tar.xz' entrypoints_0.3-2ubuntu1.debian.tar.xz 3340 SHA256:2c6fbc04724453df61eea3dc0de472e01e7d9ccc89f03213f39f4e4a99c4e86d
```

### `dpkg` source package: `expat=2.2.9-1ubuntu0.8`

Binary Packages:

- `libexpat1:amd64=2.2.9-1ubuntu0.8`
- `libexpat1-dev:amd64=2.2.9-1ubuntu0.8`

Licenses: (parsed from: `/usr/share/doc/libexpat1/copyright`, `/usr/share/doc/libexpat1-dev/copyright`)

- `MIT`

Source:

```console
$ apt-get source -qq --print-uris expat=2.2.9-1ubuntu0.8
'http://archive.ubuntu.com/ubuntu/pool/main/e/expat/expat_2.2.9-1ubuntu0.8.dsc' expat_2.2.9-1ubuntu0.8.dsc 2109 SHA512:fa4d85bed1c8967c9c8889a560a031d45c1d5ef6bf8abee5c57944e9748ef8c721394ab4f031d2fa011b57eabed0deb3513b509486cfa14396f918ba2764e788
'http://archive.ubuntu.com/ubuntu/pool/main/e/expat/expat_2.2.9.orig.tar.gz' expat_2.2.9.orig.tar.gz 8273174 SHA512:e274fa7f30630450cb3ca681b266d765dbb7f5d00d1275ff9d9b2e2f6e1095893b8af4e3f4172ae6297c7a8a831a0a6becd484fe4bcdca09c37922f630780ef0
'http://archive.ubuntu.com/ubuntu/pool/main/e/expat/expat_2.2.9-1ubuntu0.8.debian.tar.xz' expat_2.2.9-1ubuntu0.8.debian.tar.xz 30356 SHA512:e919ddd7eac8c2a9b7b41d835106e80aa5dafca9fc89f9f8349f5f2c33ee8d5897e99dd6cdfa0216ecc62676310a98a20ee2b3874585fe5628fb557fe55f3155
```

### `dpkg` source package: `findutils=4.7.0-1ubuntu1`

Binary Packages:

- `findutils=4.7.0-1ubuntu1`

Licenses: (parsed from: `/usr/share/doc/findutils/copyright`)

- `GFDL-1.3`
- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris findutils=4.7.0-1ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/f/findutils/findutils_4.7.0-1ubuntu1.dsc' findutils_4.7.0-1ubuntu1.dsc 2446 SHA256:3d157948919082e66cb74e0f927efa3dd240d9fa9814973874d0fa77f3023ead
'http://archive.ubuntu.com/ubuntu/pool/main/f/findutils/findutils_4.7.0.orig.tar.xz' findutils_4.7.0.orig.tar.xz 1895048 SHA256:c5fefbdf9858f7e4feb86f036e1247a54c79fc2d8e4b7064d5aaa1f47dfa789a
'http://archive.ubuntu.com/ubuntu/pool/main/f/findutils/findutils_4.7.0.orig.tar.xz.asc' findutils_4.7.0.orig.tar.xz.asc 488 SHA256:2f620e6d941e241fac52344a89149ab1ffeefb0fb9e42174e17a508d59a31d0f
'http://archive.ubuntu.com/ubuntu/pool/main/f/findutils/findutils_4.7.0-1ubuntu1.debian.tar.xz' findutils_4.7.0-1ubuntu1.debian.tar.xz 27700 SHA256:dfb2329fd141384c2d76409c2e99f164cc25954115529245d80d5d41e3167731
```

### `dpkg` source package: `fontconfig=2.13.1-2ubuntu3`

Binary Packages:

- `fontconfig=2.13.1-2ubuntu3`
- `fontconfig-config=2.13.1-2ubuntu3`
- `libfontconfig1:amd64=2.13.1-2ubuntu3`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris fontconfig=2.13.1-2ubuntu3
'http://archive.ubuntu.com/ubuntu/pool/main/f/fontconfig/fontconfig_2.13.1-2ubuntu3.dsc' fontconfig_2.13.1-2ubuntu3.dsc 1959 SHA256:a9eebf6e6e88aa64d33fb3852c97718c212579f9714afd67cb6a9b8b116dd7aa
'http://archive.ubuntu.com/ubuntu/pool/main/f/fontconfig/fontconfig_2.13.1.orig.tar.bz2' fontconfig_2.13.1.orig.tar.bz2 1723639 SHA256:f655dd2a986d7aa97e052261b36aa67b0a64989496361eca8d604e6414006741
'http://archive.ubuntu.com/ubuntu/pool/main/f/fontconfig/fontconfig_2.13.1-2ubuntu3.debian.tar.xz' fontconfig_2.13.1-2ubuntu3.debian.tar.xz 26344 SHA256:342671f6a1e6d392958a6eec27541c6bdffc6498b469dcc46eca66c9d23a863a
```

### `dpkg` source package: `fonts-dejavu=2.37-1`

Binary Packages:

- `fonts-dejavu-core=2.37-1`

Licenses: (parsed from: `/usr/share/doc/fonts-dejavu-core/copyright`)

- `GPL-2`
- `GPL-2+`
- `bitstream-vera`

Source:

```console
$ apt-get source -qq --print-uris fonts-dejavu=2.37-1
'http://archive.ubuntu.com/ubuntu/pool/main/f/fonts-dejavu/fonts-dejavu_2.37-1.dsc' fonts-dejavu_2.37-1.dsc 2575 SHA256:f35ff7b2c8dbfda6564c9dedf088ba06cc6d279fdd8e7cccbd1ae08ded1bb71c
'http://archive.ubuntu.com/ubuntu/pool/main/f/fonts-dejavu/fonts-dejavu_2.37.orig.tar.bz2' fonts-dejavu_2.37.orig.tar.bz2 12050109 SHA256:4b21c5203f792343d5e90ab1cb0cf07e99887218abe3d83cd9a98cea9085e799
'http://archive.ubuntu.com/ubuntu/pool/main/f/fonts-dejavu/fonts-dejavu_2.37-1.debian.tar.xz' fonts-dejavu_2.37-1.debian.tar.xz 10424 SHA256:5105cdbfc086f4a83ab6871eb39cc904bf02aa52762402b7cacf33d0938122f7
```

### `dpkg` source package: `freetype=2.10.1-2ubuntu0.4`

Binary Packages:

- `libfreetype6:amd64=2.10.1-2ubuntu0.4`

Licenses: (parsed from: `/usr/share/doc/libfreetype6/copyright`)

- `Apache-2.0`
- `BSD-3-Clause`
- `FSFUL`
- `FSFULLR`
- `FTL`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `MIT`
- `MPL-1.1`
- `OFL-1.1`
- `OpenGroup-BSD-like`
- `Permissive`
- `Public-Domain`
- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris freetype=2.10.1-2ubuntu0.4
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.10.1-2ubuntu0.4.dsc' freetype_2.10.1-2ubuntu0.4.dsc 3864 SHA512:4f70190cb0ed93bd7d6207e122d83962aaf3cfd8ba410c64bf7fdfb9b5ec854fa9fb21b22fb5ebfa2db145209e1563b0c6c5f570d7c4bb26efb7392a6a51ff66
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.10.1.orig-ft2demos.tar.gz' freetype_2.10.1.orig-ft2demos.tar.gz 305328 SHA512:67b9dc1c03ca5588a53edd8b9cb7f27e5b52a5730add6887e6af776176ab66099bfe4a9e69d036511d32ae2f96e822a71a3c9213f1adfcc6fa45be81adf56f77
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.10.1.orig-ft2demos.tar.gz.asc' freetype_2.10.1.orig-ft2demos.tar.gz.asc 195 SHA512:8279e9e7ea4da030db388ac5960808d652553b97dc65bc517ebcae90834188d75101fbe29d334a0e2b0a17a723c7121ac28b1f14bab0bf29ec4c9c6df6575a67
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.10.1.orig-ft2docs.tar.gz' freetype_2.10.1.orig-ft2docs.tar.gz 2123885 SHA512:05dbe26c291d3fa39c167f3aa5d8da0f3d3992f8e7ec74e936547b3feb17c1a59753a111fc33b2edce12ed991c61161c0ef7084b91c770d73c4679b62edd5b2f
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.10.1.orig-ft2docs.tar.gz.asc' freetype_2.10.1.orig-ft2docs.tar.gz.asc 195 SHA512:48e283c72d808901b9754bb20242d493628610326f3492c6d1aa35fcdffffd4ec320f589d18442735cfc6cda7238399f4f339d58e4a536da46e2b5a13864972e
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.10.1.orig.tar.gz' freetype_2.10.1.orig.tar.gz 3478158 SHA512:346c682744bcf06ca9d71265c108a242ad7d78443eff20142454b72eef47ba6d76671a6e931ed4c4c9091dd8f8515ebdd71202d94b073d77931345ff93cfeaa7
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.10.1.orig.tar.gz.asc' freetype_2.10.1.orig.tar.gz.asc 195 SHA512:2a2750605d0fd11fbfe4f76d47ccd8e300473c3043b28a5c46f4f628e1da2c2f2308ee4f1b1b585daaf2c4b408718ee68eab6c5411e993ad9f95b08c35248178
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.10.1-2ubuntu0.4.debian.tar.xz' freetype_2.10.1-2ubuntu0.4.debian.tar.xz 118612 SHA512:d8cf58d1d2487c46c3de546a2eded527b760384a10b5a89ca5a65837b0ccb7ba20de6c051cc005e119c937496d4ba96df2e01311568b3bf150f3939f8f30b420
```

### `dpkg` source package: `fribidi=1.0.8-2ubuntu0.1`

Binary Packages:

- `libfribidi0:amd64=1.0.8-2ubuntu0.1`

Licenses: (parsed from: `/usr/share/doc/libfribidi0/copyright`)

- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris fribidi=1.0.8-2ubuntu0.1
'http://archive.ubuntu.com/ubuntu/pool/main/f/fribidi/fribidi_1.0.8-2ubuntu0.1.dsc' fribidi_1.0.8-2ubuntu0.1.dsc 2442 SHA512:f9047bc07f608d08ed75aa3a548a15123340b97b4841a1e5904dce11e713aef3df5b3399817d8fcfd77e342b0afe6e99dfe64bb86acd5b7eedd633da347ef869
'http://archive.ubuntu.com/ubuntu/pool/main/f/fribidi/fribidi_1.0.8.orig.tar.bz2' fribidi_1.0.8.orig.tar.bz2 2077095 SHA512:d66b1524b26d227fd6a628f438efb875c023ae3be708acaaad11f1f62d0902de0a5f57124458291ef2b0fcd89356c52ab8ae5559b0b5a93fa435b92f1d098ba2
'http://archive.ubuntu.com/ubuntu/pool/main/f/fribidi/fribidi_1.0.8-2ubuntu0.1.debian.tar.xz' fribidi_1.0.8-2ubuntu0.1.debian.tar.xz 10612 SHA512:2ad4f0c140d303f5d79ec5bba1b7211fac398768f0a07f47e0ad8d9844d61cc38c31daafaa9378a1dae9bec66917d7d46b15d1aaab34d3b15a738632fdf15feb
```

### `dpkg` source package: `gcc-10=10.5.0-1ubuntu1~20.04`

Binary Packages:

- `gcc-10-base:amd64=10.5.0-1ubuntu1~20.04`
- `libatomic1:amd64=10.5.0-1ubuntu1~20.04`
- `libcc1-0:amd64=10.5.0-1ubuntu1~20.04`
- `libgcc-s1:amd64=10.5.0-1ubuntu1~20.04`
- `libgfortran5:amd64=10.5.0-1ubuntu1~20.04`
- `libgomp1:amd64=10.5.0-1ubuntu1~20.04`
- `libitm1:amd64=10.5.0-1ubuntu1~20.04`
- `liblsan0:amd64=10.5.0-1ubuntu1~20.04`
- `libquadmath0:amd64=10.5.0-1ubuntu1~20.04`
- `libstdc++6:amd64=10.5.0-1ubuntu1~20.04`
- `libtsan0:amd64=10.5.0-1ubuntu1~20.04`
- `libubsan1:amd64=10.5.0-1ubuntu1~20.04`

Licenses: (parsed from: `/usr/share/doc/gcc-10-base/copyright`, `/usr/share/doc/libatomic1/copyright`, `/usr/share/doc/libcc1-0/copyright`, `/usr/share/doc/libgcc-s1/copyright`, `/usr/share/doc/libgfortran5/copyright`, `/usr/share/doc/libgomp1/copyright`, `/usr/share/doc/libitm1/copyright`, `/usr/share/doc/liblsan0/copyright`, `/usr/share/doc/libquadmath0/copyright`, `/usr/share/doc/libstdc++6/copyright`, `/usr/share/doc/libtsan0/copyright`, `/usr/share/doc/libubsan1/copyright`)

- `Artistic`
- `GFDL-1.2`
- `GPL`
- `GPL-2`
- `GPL-3`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris gcc-10=10.5.0-1ubuntu1~20.04
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-10/gcc-10_10.5.0-1ubuntu1%7e20.04.dsc' gcc-10_10.5.0-1ubuntu1~20.04.dsc 31130 SHA512:0adfb92474d09348ce0ef4a4a3edd143a054d2bcba01dbdf29f925066ecc6e4874a02d7ced1501d39c1e966a1b0f3b9bef6ddcc8181df9b77206cefedcef6f15
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-10/gcc-10_10.5.0.orig.tar.gz' gcc-10_10.5.0.orig.tar.gz 84203753 SHA512:0617b7353e3da37e30abecb3527a987bb444a57e2f18a1265f9b727b5f43a40068d7242f8ce92fe47810e883778c13a0c54c5126071a5c6abd786c02919f5c81
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-10/gcc-10_10.5.0-1ubuntu1%7e20.04.debian.tar.xz' gcc-10_10.5.0-1ubuntu1~20.04.debian.tar.xz 5953836 SHA512:d68b8b10628bec39c370c9af1baa39bd76f3fb885d765b2d449435981ab772443187cba3bcb629e69a4a7c4b1e890babc4ea9ed8a3a3eb9a8e7e1e76abb8b526
```

### `dpkg` source package: `gcc-9=9.4.0-1ubuntu1~20.04.2`

Binary Packages:

- `cpp-9=9.4.0-1ubuntu1~20.04.2`
- `g++-9=9.4.0-1ubuntu1~20.04.2`
- `gcc-9=9.4.0-1ubuntu1~20.04.2`
- `gcc-9-base:amd64=9.4.0-1ubuntu1~20.04.2`
- `libasan5:amd64=9.4.0-1ubuntu1~20.04.2`
- `libgcc-9-dev:amd64=9.4.0-1ubuntu1~20.04.2`
- `libstdc++-9-dev:amd64=9.4.0-1ubuntu1~20.04.2`

Licenses: (parsed from: `/usr/share/doc/cpp-9/copyright`, `/usr/share/doc/g++-9/copyright`, `/usr/share/doc/gcc-9/copyright`, `/usr/share/doc/gcc-9-base/copyright`, `/usr/share/doc/libasan5/copyright`, `/usr/share/doc/libgcc-9-dev/copyright`, `/usr/share/doc/libstdc++-9-dev/copyright`)

- `Artistic`
- `GFDL-1.2`
- `GPL`
- `GPL-2`
- `GPL-3`
- `LGPL`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris gcc-9=9.4.0-1ubuntu1~20.04.2
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-9/gcc-9_9.4.0-1ubuntu1%7e20.04.2.dsc' gcc-9_9.4.0-1ubuntu1~20.04.2.dsc 23760 SHA512:76d09db3de4bf585143b73bbfe9f46c66f9e00da33b08cb62cf95b70d21a704f95df61725527edb514c87356cc13ee4a2e2bb21b66f468469ace0d4893da0c34
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-9/gcc-9_9.4.0.orig.tar.gz' gcc-9_9.4.0.orig.tar.gz 92368536 SHA512:c10390524e900d3f0afd4516af097f536304fb2946ecf73eaba0472b953609ce8fbb5c7f0c20af9e54fe38fc8f45ec3b6ebd2051fa67225c73efa8362150c1c6
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-9/gcc-9_9.4.0-1ubuntu1%7e20.04.2.debian.tar.xz' gcc-9_9.4.0-1ubuntu1~20.04.2.debian.tar.xz 579772 SHA512:4f23eb26adf795d2794c7ef083caa0a0f73dd9d8e3e809139df9595f4ef29012a6c7a5b158441900d1a55f7bb6d80ea68d0bc422f0a18d9573df9db04b30945f
```

### `dpkg` source package: `gcc-defaults=1.185.1ubuntu2`

Binary Packages:

- `cpp=4:9.3.0-1ubuntu2`
- `g++=4:9.3.0-1ubuntu2`
- `gcc=4:9.3.0-1ubuntu2`

Licenses: (parsed from: `/usr/share/doc/cpp/copyright`, `/usr/share/doc/g++/copyright`, `/usr/share/doc/gcc/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris gcc-defaults=1.185.1ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-defaults/gcc-defaults_1.185.1ubuntu2.dsc' gcc-defaults_1.185.1ubuntu2.dsc 16544 SHA256:32c0331bc75ecbc0d013b9e11401d1fc64cbd7b0198274cb25a183a27b5c407f
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-defaults/gcc-defaults_1.185.1ubuntu2.tar.gz' gcc-defaults_1.185.1ubuntu2.tar.gz 58807 SHA256:342b5842c03073717bc98d6d9de7eb79027a1239735637743006933e5d44bb05
```

### `dpkg` source package: `gdbm=1.18.1-5`

Binary Packages:

- `libgdbm-compat4:amd64=1.18.1-5`
- `libgdbm6:amd64=1.18.1-5`

Licenses: (parsed from: `/usr/share/doc/libgdbm-compat4/copyright`, `/usr/share/doc/libgdbm6/copyright`)

- `GFDL-NIV-1.3+`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris gdbm=1.18.1-5
'http://archive.ubuntu.com/ubuntu/pool/main/g/gdbm/gdbm_1.18.1-5.dsc' gdbm_1.18.1-5.dsc 2635 SHA256:4c0c4498378c673c9d2d8dfb5b319a4830d2dd21e65faaaa8e0f09cb7f71606b
'http://archive.ubuntu.com/ubuntu/pool/main/g/gdbm/gdbm_1.18.1.orig.tar.gz' gdbm_1.18.1.orig.tar.gz 941863 SHA256:86e613527e5dba544e73208f42b78b7c022d4fa5a6d5498bf18c8d6f745b91dc
'http://archive.ubuntu.com/ubuntu/pool/main/g/gdbm/gdbm_1.18.1.orig.tar.gz.asc' gdbm_1.18.1.orig.tar.gz.asc 412 SHA256:3254738e7689e44ac65e78a766806828b8282e6bb1c0e5bb6156a99e567889a5
'http://archive.ubuntu.com/ubuntu/pool/main/g/gdbm/gdbm_1.18.1-5.debian.tar.xz' gdbm_1.18.1-5.debian.tar.xz 16348 SHA256:3c1a0e05b40a97ee51ce77c736c72c37738ba31b2720111d3bc99175a2c3a3ed
```

### `dpkg` source package: `git=1:2.25.1-1ubuntu3.14`

Binary Packages:

- `git=1:2.25.1-1ubuntu3.14`
- `git-man=1:2.25.1-1ubuntu3.14`

Licenses: (parsed from: `/usr/share/doc/git/copyright`, `/usr/share/doc/git-man/copyright`)

- `Apache-2.0`
- `Artistic`
- `Artistic-1`
- `BSD-2-clause`
- `Boost`
- `EDL-1.0`
- `Expat`
- `GPL`
- `GPL-1+`
- `GPL-2`
- `GPL-2+`
- `ISC`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `dlmalloc`
- `mingw-runtime`

Source:

```console
$ apt-get source -qq --print-uris git=1:2.25.1-1ubuntu3.14
'http://archive.ubuntu.com/ubuntu/pool/main/g/git/git_2.25.1-1ubuntu3.14.dsc' git_2.25.1-1ubuntu3.14.dsc 2966 SHA512:02725ad0ce0ecc76e3ade84a211989c02ab70ed3c3b6a8cd282645700374a0398a747f41392fa795e79d2f57e90cf6afd2b7ab4851ea3110e62f1d298b408f8e
'http://archive.ubuntu.com/ubuntu/pool/main/g/git/git_2.25.1.orig.tar.xz' git_2.25.1.orig.tar.xz 5875548 SHA512:15241143acfd8542d85d2709ac3c80dbd6e8d5234438f70c4f33cc71a2bdec3e32938df7f6351e2746d570b021d3bd0b70474ea4beec0c51d1fc45f9c287b344
'http://archive.ubuntu.com/ubuntu/pool/main/g/git/git_2.25.1-1ubuntu3.14.debian.tar.xz' git_2.25.1-1ubuntu3.14.debian.tar.xz 719124 SHA512:4ee6d3c92aad795c88aefba4aa245448aaee1b740494c34f3088716ebd70f54324cd1f7ca0d0e06c2980489f14a31f250d0a512f798dc3373c71818dc48e74c5
```

### `dpkg` source package: `glib2.0=2.64.6-1~ubuntu20.04.9`

Binary Packages:

- `libglib2.0-0:amd64=2.64.6-1~ubuntu20.04.9`

Licenses: (parsed from: `/usr/share/doc/libglib2.0-0/copyright`)

- `Expat`
- `GPL-2+`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris glib2.0=2.64.6-1~ubuntu20.04.9
'http://archive.ubuntu.com/ubuntu/pool/main/g/glib2.0/glib2.0_2.64.6-1%7eubuntu20.04.9.dsc' glib2.0_2.64.6-1~ubuntu20.04.9.dsc 3338 SHA512:7d323aa3bf099177c42c6e5fdd334721d54f55631306b83a0cc3c6b1697e6baf9f87603856c7414d3ff618f6ce58689ab3e31e1b9c7a21284b77242050196ddc
'http://archive.ubuntu.com/ubuntu/pool/main/g/glib2.0/glib2.0_2.64.6.orig.tar.xz' glib2.0_2.64.6.orig.tar.xz 4781576 SHA512:5cd82c4d9b143e7aa130c24e25fb9def06dd915ef8ad8ed3883931bf5cddecf69c2e669ef6aa1d910484ede75b671e7c48a4f3fe50aa78955bff57b04f0cf958
'http://archive.ubuntu.com/ubuntu/pool/main/g/glib2.0/glib2.0_2.64.6-1%7eubuntu20.04.9.debian.tar.xz' glib2.0_2.64.6-1~ubuntu20.04.9.debian.tar.xz 150280 SHA512:8a5b9233d3977a9273b492c5422aded88c3bed7a536981ea8c1b4ea7286ad79bc7b0339c43551a2d87304711b55c02827bd5bd3a6050754e778779efb6655f41
```

### `dpkg` source package: `glibc=2.31-0ubuntu9.17`

Binary Packages:

- `libc-bin=2.31-0ubuntu9.17`

Licenses: (parsed from: `/usr/share/doc/libc-bin/copyright`)

- `GPL-2`
- `LGPL-2.1`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `glibc=2.31-0ubuntu9.18`

Binary Packages:

- `libc-dev-bin=2.31-0ubuntu9.18`
- `libc6:amd64=2.31-0ubuntu9.18`
- `libc6-dev:amd64=2.31-0ubuntu9.18`

Licenses: (parsed from: `/usr/share/doc/libc-dev-bin/copyright`, `/usr/share/doc/libc6/copyright`, `/usr/share/doc/libc6-dev/copyright`)

- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris glibc=2.31-0ubuntu9.18
'http://archive.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.31-0ubuntu9.18.dsc' glibc_2.31-0ubuntu9.18.dsc 9422 SHA512:1bd1891516f6b1220687e948144cf9e84d1e8995c96bcccfdb77715daa0d0056cd93dc3f6afe904e671b77376914fa0407ce8269c1c19ebc859e8b456bb8c0fb
'http://archive.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.31.orig.tar.xz' glibc_2.31.orig.tar.xz 17317924 SHA512:2ff56628fe935cacbdf1825534f15d45cb87a159cbdb2e6a981590eeb6174ed4b3ff7041519cdecbd4f624ac20b745e2dd9614c420dd3ea186b8f36bc4c2453c
'http://archive.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.31-0ubuntu9.18.debian.tar.xz' glibc_2.31-0ubuntu9.18.debian.tar.xz 891764 SHA512:2801b7d414f6c69a37d36c14338bc16ee4da3f84a2aad03742fce58e9a0efc9e126b98e8a40b28ad8ec666c2ff0259d69d7add7385033b2f172a8c77226da61f
```

### `dpkg` source package: `gmp=2:6.2.0+dfsg-4ubuntu0.1`

Binary Packages:

- `libgmp10:amd64=2:6.2.0+dfsg-4ubuntu0.1`

Licenses: (parsed from: `/usr/share/doc/libgmp10/copyright`)

- `GPL`
- `GPL-2`
- `GPL-3`
- `LGPL-3`

Source:

```console
$ apt-get source -qq --print-uris gmp=2:6.2.0+dfsg-4ubuntu0.1
'http://archive.ubuntu.com/ubuntu/pool/main/g/gmp/gmp_6.2.0%2bdfsg-4ubuntu0.1.dsc' gmp_6.2.0+dfsg-4ubuntu0.1.dsc 2279 SHA512:6171e0fa69e6ddb3332a9fa4a23ca6006a451d19f0df717b1db8ed67c97104b247c9c711db4ea879318b2fd17345c2b63ae4e960613884f34ce0da85dc8f78ea
'http://archive.ubuntu.com/ubuntu/pool/main/g/gmp/gmp_6.2.0%2bdfsg.orig.tar.xz' gmp_6.2.0+dfsg.orig.tar.xz 1842912 SHA512:6ed6df69ced53b13e3e2d64d94f8a34c3257abd4c0967f16d48b064956e260a3d8fb424c84d47dca6d1308bd16b347af3740fce68ebd2d45f1d7f752422c2496
'http://archive.ubuntu.com/ubuntu/pool/main/g/gmp/gmp_6.2.0%2bdfsg-4ubuntu0.1.debian.tar.xz' gmp_6.2.0+dfsg-4ubuntu0.1.debian.tar.xz 21644 SHA512:b89b351bd9648108a15aa4db193610a36d59a9f75ddcbad2ea85004dbdf39553a6e611552351d2f37836eed3d99f152cba22fdbaa71b92f94635797b06404a27
```

### `dpkg` source package: `gnupg2=2.2.19-3ubuntu2.4`

Binary Packages:

- `dirmngr=2.2.19-3ubuntu2.4`
- `gnupg=2.2.19-3ubuntu2.4`
- `gnupg-l10n=2.2.19-3ubuntu2.4`
- `gnupg-utils=2.2.19-3ubuntu2.4`
- `gnupg2=2.2.19-3ubuntu2.4`
- `gpg=2.2.19-3ubuntu2.4`
- `gpg-agent=2.2.19-3ubuntu2.4`
- `gpg-wks-client=2.2.19-3ubuntu2.4`
- `gpg-wks-server=2.2.19-3ubuntu2.4`
- `gpgconf=2.2.19-3ubuntu2.4`
- `gpgsm=2.2.19-3ubuntu2.4`
- `gpgv=2.2.19-3ubuntu2.4`

Licenses: (parsed from: `/usr/share/doc/dirmngr/copyright`, `/usr/share/doc/gnupg/copyright`, `/usr/share/doc/gnupg-l10n/copyright`, `/usr/share/doc/gnupg-utils/copyright`, `/usr/share/doc/gnupg2/copyright`, `/usr/share/doc/gpg/copyright`, `/usr/share/doc/gpg-agent/copyright`, `/usr/share/doc/gpg-wks-client/copyright`, `/usr/share/doc/gpg-wks-server/copyright`, `/usr/share/doc/gpgconf/copyright`, `/usr/share/doc/gpgsm/copyright`, `/usr/share/doc/gpgv/copyright`)

- `BSD-3-clause`
- `CC0-1.0`
- `Expat`
- `GPL-3`
- `GPL-3+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`
- `LGPL-3+`
- `RFC-Reference`
- `TinySCHEME`
- `permissive`

Source:

```console
$ apt-get source -qq --print-uris gnupg2=2.2.19-3ubuntu2.4
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnupg2/gnupg2_2.2.19-3ubuntu2.4.dsc' gnupg2_2.2.19-3ubuntu2.4.dsc 3939 SHA512:a057c40bc8cc9e3f7d020a1d3a046389331f6032e05839537f81071582e4cfcb290cd019052b674b87d42e7c81924be1ee940af962327725f8f23cc36d080d81
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnupg2/gnupg2_2.2.19.orig.tar.bz2' gnupg2_2.2.19.orig.tar.bz2 6754972 SHA512:d7700136ac9f0a8cf04b33da4023a42427fced648c2f90d76250c92904353b85fe728bdd89a713d847e8d38e5900c98d46075614492fdc3d1421f927a92f49dd
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnupg2/gnupg2_2.2.19.orig.tar.bz2.asc' gnupg2_2.2.19.orig.tar.bz2.asc 906 SHA512:8b02ce09a50d2aa0c263f7042424ea815386fac56a8d8cea102d1aea2e75802f91bb2ebc7dc2d7a3157126d748ece554e0693d3bf355f908586cbadbe80c68fb
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnupg2/gnupg2_2.2.19-3ubuntu2.4.debian.tar.xz' gnupg2_2.2.19-3ubuntu2.4.debian.tar.xz 74588 SHA512:41307558e6bfded1a1547a5995d3cb28236f309ae206e95a5ec841dfa14f096d8f2d55b6cd976c03a8127483b25d54fa7bc9f2ddb76e5a6fb915cab783be79ba
```

### `dpkg` source package: `gnutls28=3.6.13-2ubuntu1.12`

Binary Packages:

- `libgnutls30:amd64=3.6.13-2ubuntu1.12`

Licenses: (parsed from: `/usr/share/doc/libgnutls30/copyright`)

- `Apache-2.0`
- `BSD-3-Clause`
- `CC0 license`
- `Expat`
- `GFDL-1.3`
- `GPL`
- `GPL-3`
- `GPLv3+`
- `LGPL`
- `LGPL-3`
- `LGPLv2.1+`
- `LGPLv3+_or_GPLv2+`
- `The main library is licensed under GNU Lesser`

Source:

```console
$ apt-get source -qq --print-uris gnutls28=3.6.13-2ubuntu1.12
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.6.13-2ubuntu1.12.dsc' gnutls28_3.6.13-2ubuntu1.12.dsc 3598 SHA512:2f471676f07ad88eda1da024cebf7d6223506e994055c016ace38562295c79485aa91581850a7ff3d1654a7c0f8e3a12138eaf175c79d6d6c84c8aadac040525
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.6.13.orig.tar.xz' gnutls28_3.6.13.orig.tar.xz 5958956 SHA512:23581952cb72c9a34f378c002bb62413d5a1243b74b48ad8dc49eaea4020d33c550f8dc1dd374cf7fbfa4187b0ca1c5698c8a0430398268a8b8a863f8633305c
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.6.13.orig.tar.xz.asc' gnutls28_3.6.13.orig.tar.xz.asc 667 SHA512:b343a8ace6a5c81c0c44b2cb65d8e83dfe5963c9bab04d9131fa8fd03cdf0c6f990d720af8767084e01bf5f7a7dbd0f048aefe68c3b6f1dc1ea1899d567a72f7
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.6.13-2ubuntu1.12.debian.tar.xz' gnutls28_3.6.13-2ubuntu1.12.debian.tar.xz 86900 SHA512:a7042093da477b770a4f8a2c11139b498d8d4c4707d54ed620c5a8a63a3a9bbd4874aa9bb208cc2d676782ee2a7039cd75f457c142ccd8f91b530afa918c3fea
```

### `dpkg` source package: `googletest=1.10.0-2`

Binary Packages:

- `google-mock:amd64=1.10.0-2`
- `googletest=1.10.0-2`
- `libgtest-dev:amd64=1.10.0-2`

Licenses: (parsed from: `/usr/share/doc/google-mock/copyright`, `/usr/share/doc/googletest/copyright`, `/usr/share/doc/libgtest-dev/copyright`)

- `Apache`
- `BSD-C3`
- `GAP`

Source:

```console
$ apt-get source -qq --print-uris googletest=1.10.0-2
'http://archive.ubuntu.com/ubuntu/pool/universe/g/googletest/googletest_1.10.0-2.dsc' googletest_1.10.0-2.dsc 2195 SHA256:c7b1a205d6f704d54e8fb34b680a6c4e7f71f91af0ee8b29fa05adcec5c569d1
'http://archive.ubuntu.com/ubuntu/pool/universe/g/googletest/googletest_1.10.0.orig.tar.bz2' googletest_1.10.0.orig.tar.bz2 702821 SHA256:369d5e65753f0e86ed96dac25088488ff852332cbf1be1db58d062eecc4c32bf
'http://archive.ubuntu.com/ubuntu/pool/universe/g/googletest/googletest_1.10.0-2.debian.tar.xz' googletest_1.10.0-2.debian.tar.xz 10468 SHA256:af49f7e0195db575ca6bd907c09e2e85b78685dd3374e00bda53624f436bddb1
```

### `dpkg` source package: `graphite2=1.3.13-11build1`

Binary Packages:

- `libgraphite2-3:amd64=1.3.13-11build1`

Licenses: (parsed from: `/usr/share/doc/libgraphite2-3/copyright`)

- `Artistic`
- `GPL-1`
- `GPL-1+`
- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `MPL-1.1`
- `custom-sil-open-font-license`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris graphite2=1.3.13-11build1
'http://archive.ubuntu.com/ubuntu/pool/main/g/graphite2/graphite2_1.3.13-11build1.dsc' graphite2_1.3.13-11build1.dsc 2636 SHA256:c0553cdbffa6ec465063753058007acdf956a1d3fda7336c356b663d4b73bd18
'http://archive.ubuntu.com/ubuntu/pool/main/g/graphite2/graphite2_1.3.13.orig.tar.gz' graphite2_1.3.13.orig.tar.gz 6664941 SHA256:2f9f609deeddfe2b193502adc8df3b0396694b799a433c36e85fd1242e654cd9
'http://archive.ubuntu.com/ubuntu/pool/main/g/graphite2/graphite2_1.3.13-11build1.debian.tar.xz' graphite2_1.3.13-11build1.debian.tar.xz 12132 SHA256:b25e456d2810c2965e968403e2e2fdaf159327f3db5f37c87adae905b40efa49
```

### `dpkg` source package: `graphviz=2.42.2-3build2`

Binary Packages:

- `graphviz=2.42.2-3build2`
- `libcdt5:amd64=2.42.2-3build2`
- `libcgraph6:amd64=2.42.2-3build2`
- `libgvc6=2.42.2-3build2`
- `libgvpr2:amd64=2.42.2-3build2`
- `liblab-gamut1:amd64=2.42.2-3build2`
- `libpathplan4:amd64=2.42.2-3build2`

Licenses: (parsed from: `/usr/share/doc/graphviz/copyright`, `/usr/share/doc/libcdt5/copyright`, `/usr/share/doc/libcgraph6/copyright`, `/usr/share/doc/libgvc6/copyright`, `/usr/share/doc/libgvpr2/copyright`, `/usr/share/doc/liblab-gamut1/copyright`, `/usr/share/doc/libpathplan4/copyright`)

- `EPL-1.0`
- `MIT`
- `X/MIT`
- `zlib-style`

Source:

```console
$ apt-get source -qq --print-uris graphviz=2.42.2-3build2
'http://archive.ubuntu.com/ubuntu/pool/universe/g/graphviz/graphviz_2.42.2-3build2.dsc' graphviz_2.42.2-3build2.dsc 3219 SHA256:2c0403f082fb1495d78ac4ba3b9d9b126be595c186cef15320efc9ee734c0e53
'http://archive.ubuntu.com/ubuntu/pool/universe/g/graphviz/graphviz_2.42.2.orig.tar.bz2' graphviz_2.42.2.orig.tar.bz2 30740923 SHA256:1daed697d9cdd7fac3b320336fa98dd3518dd211769301dc716869fc3d5409b1
'http://archive.ubuntu.com/ubuntu/pool/universe/g/graphviz/graphviz_2.42.2-3build2.debian.tar.xz' graphviz_2.42.2-3build2.debian.tar.xz 38456 SHA256:9962d2bfcf60248cfd281fadc8272681337d58b987770271c8ddbd0815f2dfba
```

### `dpkg` source package: `grep=3.4-1`

Binary Packages:

- `grep=3.4-1`

Licenses: (parsed from: `/usr/share/doc/grep/copyright`)

- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris grep=3.4-1
'http://archive.ubuntu.com/ubuntu/pool/main/g/grep/grep_3.4-1.dsc' grep_3.4-1.dsc 1674 SHA256:785f527cede9631f075bdd6c7f35e65e6b82897d009682766cf35839a393277d
'http://archive.ubuntu.com/ubuntu/pool/main/g/grep/grep_3.4.orig.tar.xz' grep_3.4.orig.tar.xz 1555820 SHA256:58e6751c41a7c25bfc6e9363a41786cff3ba5709cf11d5ad903cf7cce31cc3fb
'http://archive.ubuntu.com/ubuntu/pool/main/g/grep/grep_3.4.orig.tar.xz.asc' grep_3.4.orig.tar.xz.asc 833 SHA256:4c1871ff6b79c5e5ce0a192272c171d06ec20762b4b258688b1ca2e47d94b23e
'http://archive.ubuntu.com/ubuntu/pool/main/g/grep/grep_3.4-1.debian.tar.xz' grep_3.4-1.debian.tar.xz 104364 SHA256:582d181804ce72fcfc4c6a9f13ea1dd73ad04c2723b5da346b69ee5cd24a7d08
```

### `dpkg` source package: `gts=0.7.6+darcs121130-4`

Binary Packages:

- `libgts-0.7-5:amd64=0.7.6+darcs121130-4`

Licenses: (parsed from: `/usr/share/doc/libgts-0.7-5/copyright`)

- `LGPL-2`
- `LGPL-2+`

Source:

```console
$ apt-get source -qq --print-uris gts=0.7.6+darcs121130-4
'http://archive.ubuntu.com/ubuntu/pool/universe/g/gts/gts_0.7.6%2bdarcs121130-4.dsc' gts_0.7.6+darcs121130-4.dsc 2170 SHA256:3d7dbf72a2194891a485d03f8a002e8d149dc59a915a7bbf36b42c53408ef733
'http://archive.ubuntu.com/ubuntu/pool/universe/g/gts/gts_0.7.6%2bdarcs121130.orig.tar.gz' gts_0.7.6+darcs121130.orig.tar.gz 880569 SHA256:c23f72ab74bbf65599f8c0b599d6336fabe1ec2a09c19b70544eeefdc069b73b
'http://archive.ubuntu.com/ubuntu/pool/universe/g/gts/gts_0.7.6%2bdarcs121130-4.debian.tar.bz2' gts_0.7.6+darcs121130-4.debian.tar.bz2 13837 SHA256:1fcf9c79ca0b4fc3662de645ba4e65564ea974566a3ecd730e9908f1adc425cd
```

### `dpkg` source package: `gzip=1.10-0ubuntu4.1`

Binary Packages:

- `gzip=1.10-0ubuntu4.1`

Licenses: (parsed from: `/usr/share/doc/gzip/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris gzip=1.10-0ubuntu4.1
'http://archive.ubuntu.com/ubuntu/pool/main/g/gzip/gzip_1.10-0ubuntu4.1.dsc' gzip_1.10-0ubuntu4.1.dsc 2113 SHA512:27a7c1871b33b62f6cada63d43f43eae1f3a9a3d92b10a28a28ef7f85893aba3a9513ac031c96a0dedbdaa0507aafe8922631460ff2890ab663fb732283ba073
'http://archive.ubuntu.com/ubuntu/pool/main/g/gzip/gzip_1.10.orig.tar.gz' gzip_1.10.orig.tar.gz 1201421 SHA512:7939043e74554ced0c1c05d354ab4eb36cd6dce89ad79d02ccdc5ed6b7ee390759689b2d47c07227b9b44a62851afe7c76c4cae9f92527d999f3f1b4df1cccff
'http://archive.ubuntu.com/ubuntu/pool/main/g/gzip/gzip_1.10-0ubuntu4.1.debian.tar.xz' gzip_1.10-0ubuntu4.1.debian.tar.xz 31144 SHA512:26096584c400dc78d892f1721ad28778aa1a0c0476337bd37589c6d985f8636aad9c7fde55385c25ce1c8420a40c6ca33c06887f18b855ba8a5f45b980fe6c99
```

### `dpkg` source package: `harfbuzz=2.6.4-1ubuntu4.3`

Binary Packages:

- `libharfbuzz0b:amd64=2.6.4-1ubuntu4.3`

Licenses: (parsed from: `/usr/share/doc/libharfbuzz0b/copyright`)

- `MIT`

Source:

```console
$ apt-get source -qq --print-uris harfbuzz=2.6.4-1ubuntu4.3
'http://archive.ubuntu.com/ubuntu/pool/main/h/harfbuzz/harfbuzz_2.6.4-1ubuntu4.3.dsc' harfbuzz_2.6.4-1ubuntu4.3.dsc 2849 SHA512:440ad010c9ac348776dc8a09605f4d5ff6aa34716c72aa9af3e44950ac838011d20520881a7683b184f5e3a8a290cee16d82c1088af76180db7c3cd1fc3868cf
'http://archive.ubuntu.com/ubuntu/pool/main/h/harfbuzz/harfbuzz_2.6.4.orig.tar.xz' harfbuzz_2.6.4.orig.tar.xz 5967468 SHA512:d8664bb64fda11ff7646693070637e3827f8b3d1de50e11ecf108ce4d19c878b26b2ba4cff278da6e6cc0cb431e1630d9eaa7c32a9bebb9655a7aa8dabf7114f
'http://archive.ubuntu.com/ubuntu/pool/main/h/harfbuzz/harfbuzz_2.6.4-1ubuntu4.3.debian.tar.xz' harfbuzz_2.6.4-1ubuntu4.3.debian.tar.xz 15248 SHA512:5bc7e0450f50dfab7938534f0fd875715b5fc5f39c25b63d80573bd6ff4db3cc6e7f1e14aa691fe8b41029da5a22101269a3e4a346c786366f7ee42517065003
```

### `dpkg` source package: `heimdal=7.7.0+dfsg-1ubuntu1.4`

Binary Packages:

- `libasn1-8-heimdal:amd64=7.7.0+dfsg-1ubuntu1.4`
- `libgssapi3-heimdal:amd64=7.7.0+dfsg-1ubuntu1.4`
- `libhcrypto4-heimdal:amd64=7.7.0+dfsg-1ubuntu1.4`
- `libheimbase1-heimdal:amd64=7.7.0+dfsg-1ubuntu1.4`
- `libheimntlm0-heimdal:amd64=7.7.0+dfsg-1ubuntu1.4`
- `libhx509-5-heimdal:amd64=7.7.0+dfsg-1ubuntu1.4`
- `libkrb5-26-heimdal:amd64=7.7.0+dfsg-1ubuntu1.4`
- `libroken18-heimdal:amd64=7.7.0+dfsg-1ubuntu1.4`
- `libwind0-heimdal:amd64=7.7.0+dfsg-1ubuntu1.4`

Licenses: (parsed from: `/usr/share/doc/libasn1-8-heimdal/copyright`, `/usr/share/doc/libgssapi3-heimdal/copyright`, `/usr/share/doc/libhcrypto4-heimdal/copyright`, `/usr/share/doc/libheimbase1-heimdal/copyright`, `/usr/share/doc/libheimntlm0-heimdal/copyright`, `/usr/share/doc/libhx509-5-heimdal/copyright`, `/usr/share/doc/libkrb5-26-heimdal/copyright`, `/usr/share/doc/libroken18-heimdal/copyright`, `/usr/share/doc/libwind0-heimdal/copyright`)

- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`
- `custom`
- `none`

Source:

```console
$ apt-get source -qq --print-uris heimdal=7.7.0+dfsg-1ubuntu1.4
'http://archive.ubuntu.com/ubuntu/pool/main/h/heimdal/heimdal_7.7.0%2bdfsg-1ubuntu1.4.dsc' heimdal_7.7.0+dfsg-1ubuntu1.4.dsc 3391 SHA512:c28429267b0b1afbe9dd661cff51cf21109d6b2d56a148067c3b26aa1bb10644b43ad71fe4b2bebc5cde11ac1142e0275680206c2fa5244854a990046940d5cc
'http://archive.ubuntu.com/ubuntu/pool/main/h/heimdal/heimdal_7.7.0%2bdfsg.orig.tar.xz' heimdal_7.7.0+dfsg.orig.tar.xz 5945252 SHA512:14141f3fff264c9516f736bcc51c998df69cfaa7108d2387921299efd7e82d79b918dee4029905dc221c204d3340ffc17da9472baf80029372d7c13de328ec0a
'http://archive.ubuntu.com/ubuntu/pool/main/h/heimdal/heimdal_7.7.0%2bdfsg-1ubuntu1.4.debian.tar.xz' heimdal_7.7.0+dfsg-1ubuntu1.4.debian.tar.xz 138444 SHA512:4fd1d529d0a05c415cd5f729a0ed4401c8f590c142425718fa61a3e636be6d4b3efddbad218cb6f8b9583f47fa62335f838491f47c6e04af42f3706b4cbbbec9
```

### `dpkg` source package: `hostname=3.23`

Binary Packages:

- `hostname=3.23`

Licenses: (parsed from: `/usr/share/doc/hostname/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris hostname=3.23
'http://archive.ubuntu.com/ubuntu/pool/main/h/hostname/hostname_3.23.dsc' hostname_3.23.dsc 1402 SHA256:0694c083fad82da1fd33204557a30bfc745a689a64030ba360062daafe03ede0
'http://archive.ubuntu.com/ubuntu/pool/main/h/hostname/hostname_3.23.tar.gz' hostname_3.23.tar.gz 13672 SHA256:bc6d1954b22849869ff8b2a602e39f08b1702f686d4b58dd7927cdeb5b4876ef
```

### `dpkg` source package: `icu=66.1-2ubuntu2.1`

Binary Packages:

- `libicu66:amd64=66.1-2ubuntu2.1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris icu=66.1-2ubuntu2.1
'http://archive.ubuntu.com/ubuntu/pool/main/i/icu/icu_66.1-2ubuntu2.1.dsc' icu_66.1-2ubuntu2.1.dsc 2047 SHA512:202bb201876d0167afede5fcf4abc3cb55faf75059edac64d50e3560064fe2482608e2b2476669767fa7f80aaf845a3d1c6b619e737358eb726c5de03059a8c6
'http://archive.ubuntu.com/ubuntu/pool/main/i/icu/icu_66.1.orig.tar.gz' icu_66.1.orig.tar.gz 24361305 SHA512:78d87bce65a7bdf7e9a19bda13e353c60846816ff34025f829d1ff15f9ac49aa6061eb192173742be0eca105684ce0e39e95656147afe848520bf60274c8d246
'http://archive.ubuntu.com/ubuntu/pool/main/i/icu/icu_66.1.orig.tar.gz.asc' icu_66.1.orig.tar.gz.asc 833 SHA512:5e624e8a1f210e8671f683efa203b96eebb9a311ca9945705d77e05fc182291c064157660b094ec5a073088a70892fd74e977b57fdd0abddc48ac73a4ab8781c
'http://archive.ubuntu.com/ubuntu/pool/main/i/icu/icu_66.1-2ubuntu2.1.debian.tar.xz' icu_66.1-2ubuntu2.1.debian.tar.xz 29700 SHA512:f7a9e5f49e157ede3e5dbc1a03b1521fed15dedfbdd6d8e98672f36e9b643c93e0e6407a26b66d2677bc38a5fe0ee090d9e5931d106ee1cbac4eb969db451ace
```

### `dpkg` source package: `init-system-helpers=1.57`

Binary Packages:

- `init-system-helpers=1.57`

Licenses: (parsed from: `/usr/share/doc/init-system-helpers/copyright`)

- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris init-system-helpers=1.57
'http://archive.ubuntu.com/ubuntu/pool/main/i/init-system-helpers/init-system-helpers_1.57.dsc' init-system-helpers_1.57.dsc 1896 SHA256:88bb5af040c99f010b6d6947ff5c80ae4863ff787e0eeae91e99dcd15a10dbb8
'http://archive.ubuntu.com/ubuntu/pool/main/i/init-system-helpers/init-system-helpers_1.57.tar.xz' init-system-helpers_1.57.tar.xz 40460 SHA256:e9d83fd8756a42666fb5d19a8835813823295846659b4e58f138bb9b54e9f5dd
```

### `dpkg` source package: `isl=0.22.1-1`

Binary Packages:

- `libisl22:amd64=0.22.1-1`

Licenses: (parsed from: `/usr/share/doc/libisl22/copyright`)

- `BSD-2-clause`
- `LGPL-2`
- `LGPL-2.1+`
- `MIT`

Source:

```console
$ apt-get source -qq --print-uris isl=0.22.1-1
'http://archive.ubuntu.com/ubuntu/pool/main/i/isl/isl_0.22.1-1.dsc' isl_0.22.1-1.dsc 1860 SHA256:9e9925317ef448cf679040edb6572a2874d497f758b613d9fc633bdafab197cb
'http://archive.ubuntu.com/ubuntu/pool/main/i/isl/isl_0.22.1.orig.tar.xz' isl_0.22.1.orig.tar.xz 1676948 SHA256:28658ce0f0bdb95b51fd2eb15df24211c53284f6ca2ac5e897acc3169e55b60f
'http://archive.ubuntu.com/ubuntu/pool/main/i/isl/isl_0.22.1-1.debian.tar.xz' isl_0.22.1-1.debian.tar.xz 25252 SHA256:bbeb62cfc95e51c25448e127c29fa8ac8009a6f471861de28f326bab2404a406
```

### `dpkg` source package: `jbigkit=2.1-3.1ubuntu0.20.04.1`

Binary Packages:

- `libjbig0:amd64=2.1-3.1ubuntu0.20.04.1`

Licenses: (parsed from: `/usr/share/doc/libjbig0/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris jbigkit=2.1-3.1ubuntu0.20.04.1
'http://archive.ubuntu.com/ubuntu/pool/main/j/jbigkit/jbigkit_2.1-3.1ubuntu0.20.04.1.dsc' jbigkit_2.1-3.1ubuntu0.20.04.1.dsc 1796 SHA512:c7c24dd450b988659ccfc7fb08be2a316b49cc9ff789137759d3eca38186e3212d1821aa65d4e1d98a8c20efd9bbcedf79a4b097fdeb72c275d4e80577d8a573
'http://archive.ubuntu.com/ubuntu/pool/main/j/jbigkit/jbigkit_2.1.orig.tar.gz' jbigkit_2.1.orig.tar.gz 438710 SHA512:c4127480470ef90db1ef3bd2caa444df10b50ed8df0bc9997db7612cb48b49278baf44965028f1807a21028eb965d677e015466306b44683c4ec75a23e1922cf
'http://archive.ubuntu.com/ubuntu/pool/main/j/jbigkit/jbigkit_2.1-3.1ubuntu0.20.04.1.debian.tar.xz' jbigkit_2.1-3.1ubuntu0.20.04.1.debian.tar.xz 9804 SHA512:68f3c71ce89212aaa28a83721d5e1ede41aab92a4e066779db5c8f512ad569e565a8b9d2e8e65e36e71d4d19e85c07cc0e9d28762c002d1185963b01493fc593
```

### `dpkg` source package: `keyutils=1.6-6ubuntu1.1`

Binary Packages:

- `libkeyutils1:amd64=1.6-6ubuntu1.1`

Licenses: (parsed from: `/usr/share/doc/libkeyutils1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2`
- `LGPL-2+`

Source:

```console
$ apt-get source -qq --print-uris keyutils=1.6-6ubuntu1.1
'http://archive.ubuntu.com/ubuntu/pool/main/k/keyutils/keyutils_1.6-6ubuntu1.1.dsc' keyutils_1.6-6ubuntu1.1.dsc 2185 SHA512:268bf05775176fd5550b4e66a4b9132e0be3f54ab02b77b4995f3b053191ea5d157bc38bf53d067008b311751ba3bad02b463538b6ce209403b629480c42fc38
'http://archive.ubuntu.com/ubuntu/pool/main/k/keyutils/keyutils_1.6.orig.tar.bz2' keyutils_1.6.orig.tar.bz2 93973 SHA512:ee50da165099ea26904066d24b27c5165cb1eb78df6768cba3a534aa318a5c8d926ec6e5322a38c8cedaa768cd79bdcb26ef918aa8447df2e5dfbbe7b8f200ff
'http://archive.ubuntu.com/ubuntu/pool/main/k/keyutils/keyutils_1.6-6ubuntu1.1.debian.tar.xz' keyutils_1.6-6ubuntu1.1.debian.tar.xz 14556 SHA512:300ed4c9626de95616a7c799f14d4f8bf7dc0b765d1751d3c9d60f86b7c60801bfbb97bf26c5d0ab39e5e41d5f3021ca870748f9555433b0e6c4ba261f475c3b
```

### `dpkg` source package: `krb5=1.17-6ubuntu4.11`

Binary Packages:

- `libgssapi-krb5-2:amd64=1.17-6ubuntu4.11`
- `libk5crypto3:amd64=1.17-6ubuntu4.11`
- `libkrb5-3:amd64=1.17-6ubuntu4.11`
- `libkrb5support0:amd64=1.17-6ubuntu4.11`

Licenses: (parsed from: `/usr/share/doc/libgssapi-krb5-2/copyright`, `/usr/share/doc/libk5crypto3/copyright`, `/usr/share/doc/libkrb5-3/copyright`, `/usr/share/doc/libkrb5support0/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris krb5=1.17-6ubuntu4.11
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.17-6ubuntu4.11.dsc' krb5_1.17-6ubuntu4.11.dsc 3686 SHA512:05fcace8b993bbc5eaee400e1f996aaa51535e12002901365d2b83b608022feb25990fd4758d76e0bd28a0b825905f5fb119d29ffa8b93787513f8525e7dbdd8
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.17.orig.tar.gz' krb5_1.17.orig.tar.gz 8761763 SHA512:7462a578b936bd17f155a362dbb5d388e157a80a096549028be6c55400b11361c7f8a28e424fd5674801873651df4e694d536cae66728b7ae5e840e532358c52
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.17-6ubuntu4.11.debian.tar.xz' krb5_1.17-6ubuntu4.11.debian.tar.xz 166624 SHA512:3c84d746b06f0806bbb03cf5fdce0307be1994c7a0bfc315c8208b15889fc4acc89fb4c837216e54f22d1293889d3c365ecb22e7201b486c72929ada7ea0a4d7
```

### `dpkg` source package: `lapack=3.9.0-1build1`

Binary Packages:

- `libblas3:amd64=3.9.0-1build1`
- `liblapack3:amd64=3.9.0-1build1`

Licenses: (parsed from: `/usr/share/doc/libblas3/copyright`, `/usr/share/doc/liblapack3/copyright`)

- `BSD-3-clause`
- `BSD-3-clause-intel`

Source:

```console
$ apt-get source -qq --print-uris lapack=3.9.0-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/l/lapack/lapack_3.9.0-1build1.dsc' lapack_3.9.0-1build1.dsc 3413 SHA256:8657838da743a1f52b2cc08add3ce1f606cb8c2f6f6ef5321e1f21a927025952
'http://archive.ubuntu.com/ubuntu/pool/main/l/lapack/lapack_3.9.0.orig.tar.gz' lapack_3.9.0.orig.tar.gz 7534567 SHA256:106087f1bb5f46afdfba7f569d0cbe23dacb9a07cd24733765a0e89dbe1ad573
'http://archive.ubuntu.com/ubuntu/pool/main/l/lapack/lapack_3.9.0-1build1.debian.tar.xz' lapack_3.9.0-1build1.debian.tar.xz 27380 SHA256:1a264e2cb403441463e8e8b6cf78dc8cf8a32dd9ba73a05767b9cac089bbb847
```

### `dpkg` source package: `libarchive=3.4.0-2ubuntu1.5`

Binary Packages:

- `libarchive13:amd64=3.4.0-2ubuntu1.5`

Licenses: (parsed from: `/usr/share/doc/libarchive13/copyright`)

- `Apache-2.0`
- `BSD-1-clause-UCB`
- `BSD-124-clause-UCB`
- `BSD-2-clause`
- `BSD-3-clause-UCB`
- `BSD-4-clause-UCB`
- `Expat`
- `PD`

Source:

```console
$ apt-get source -qq --print-uris libarchive=3.4.0-2ubuntu1.5
'http://archive.ubuntu.com/ubuntu/pool/main/liba/libarchive/libarchive_3.4.0-2ubuntu1.5.dsc' libarchive_3.4.0-2ubuntu1.5.dsc 2617 SHA512:b37f17927c04a39a34517c7adb279620e0495246efaa1851f19cd0d102b18fb5cec6d97b90daa8e88d80846480ab79803df8412b251e79baffc0395230bed7e6
'http://archive.ubuntu.com/ubuntu/pool/main/liba/libarchive/libarchive_3.4.0.orig.tar.gz' libarchive_3.4.0.orig.tar.gz 6908093 SHA512:2f9e2a551a6bcab56fb1a030b5d656df7299a3d151465aa02f0420d344d2fada49dee4755b3abff9095f62519e14dc9af8afa1695ecc6d5fdb4f0b28e6ede852
'http://archive.ubuntu.com/ubuntu/pool/main/liba/libarchive/libarchive_3.4.0.orig.tar.gz.asc' libarchive_3.4.0.orig.tar.gz.asc 833 SHA512:9225e17345eec49af5a143d0a5bf69d68eaf0b1ffc635384f0c3b93cb4cbb99f052afce3f88bef38f4bb74d1a826e7277e6f4deef5f0b1e75e032e2f82f9e435
'http://archive.ubuntu.com/ubuntu/pool/main/liba/libarchive/libarchive_3.4.0-2ubuntu1.5.debian.tar.xz' libarchive_3.4.0-2ubuntu1.5.debian.tar.xz 54556 SHA512:717fd648de9cfac6b3c1e43bd9c05bd717c7b12cac9ea0394c051a7473e2ea4866a1542631594f1c3110c76b171d5713fac8bd666067206c932b14ec412fb164
```

### `dpkg` source package: `libassuan=2.5.3-7ubuntu2`

Binary Packages:

- `libassuan0:amd64=2.5.3-7ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libassuan0/copyright`)

- `GAP`
- `GAP~FSF`
- `GPL-2`
- `GPL-2+`
- `GPL-2+ with libtool exception`
- `GPL-3`
- `GPL-3+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`
- `LGPL-3+`

Source:

```console
$ apt-get source -qq --print-uris libassuan=2.5.3-7ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/liba/libassuan/libassuan_2.5.3-7ubuntu2.dsc' libassuan_2.5.3-7ubuntu2.dsc 2647 SHA256:014fbd728fc1d0e954ade2a8d975539fc00d455261ca14a88d78b9e29625ee41
'http://archive.ubuntu.com/ubuntu/pool/main/liba/libassuan/libassuan_2.5.3.orig.tar.bz2' libassuan_2.5.3.orig.tar.bz2 572348 SHA256:91bcb0403866b4e7c4bc1cc52ed4c364a9b5414b3994f718c70303f7f765e702
'http://archive.ubuntu.com/ubuntu/pool/main/liba/libassuan/libassuan_2.5.3.orig.tar.bz2.asc' libassuan_2.5.3.orig.tar.bz2.asc 952 SHA256:53b16a6619a2690b4f22da645a1d0c14b5664825c87b165ca5bd0de32607888a
'http://archive.ubuntu.com/ubuntu/pool/main/liba/libassuan/libassuan_2.5.3-7ubuntu2.debian.tar.xz' libassuan_2.5.3-7ubuntu2.debian.tar.xz 13936 SHA256:586836fdfffdc58b4d47548d0f6e54593daa78098c6276a788d8b66c3616e233
```

### `dpkg` source package: `libbsd=0.10.0-1`

Binary Packages:

- `libbsd0:amd64=0.10.0-1`

Licenses: (parsed from: `/usr/share/doc/libbsd0/copyright`)

- `BSD-2-clause`
- `BSD-2-clause-NetBSD`
- `BSD-2-clause-author`
- `BSD-2-clause-verbatim`
- `BSD-3-clause`
- `BSD-3-clause-John-Birrell`
- `BSD-3-clause-Regents`
- `BSD-3-clause-author`
- `BSD-4-clause-Christopher-G-Demetriou`
- `BSD-4-clause-Niels-Provos`
- `BSD-5-clause-Peter-Wemm`
- `Beerware`
- `Expat`
- `ISC`
- `ISC-Original`
- `public-domain`
- `public-domain-Colin-Plumb`

Source:

```console
$ apt-get source -qq --print-uris libbsd=0.10.0-1
'http://archive.ubuntu.com/ubuntu/pool/main/libb/libbsd/libbsd_0.10.0-1.dsc' libbsd_0.10.0-1.dsc 2197 SHA256:7c05e2c73658f64cbd4e1762b716cc7c4c1d68391191e82c7d266a351430edd6
'http://archive.ubuntu.com/ubuntu/pool/main/libb/libbsd/libbsd_0.10.0.orig.tar.xz' libbsd_0.10.0.orig.tar.xz 393576 SHA256:34b8adc726883d0e85b3118fa13605e179a62b31ba51f676136ecb2d0bc1a887
'http://archive.ubuntu.com/ubuntu/pool/main/libb/libbsd/libbsd_0.10.0.orig.tar.xz.asc' libbsd_0.10.0.orig.tar.xz.asc 833 SHA256:4362f6d811ffc06659ac5cf777d8d01157bedfc28720b41fb485afb0a5acc0c7
'http://archive.ubuntu.com/ubuntu/pool/main/libb/libbsd/libbsd_0.10.0-1.debian.tar.xz' libbsd_0.10.0-1.debian.tar.xz 16660 SHA256:4cf37d6d5b72702b31b07384612e07173e94e081feef71fec206f86ab38f2411
```

### `dpkg` source package: `libcap-ng=0.7.9-2.1build1`

Binary Packages:

- `libcap-ng0:amd64=0.7.9-2.1build1`

Licenses: (parsed from: `/usr/share/doc/libcap-ng0/copyright`)

- `GPL-2`
- `GPL-3`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libcap-ng=0.7.9-2.1build1
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap-ng/libcap-ng_0.7.9-2.1build1.dsc' libcap-ng_0.7.9-2.1build1.dsc 2158 SHA256:6d74cf5c418659d70bce8e9a4bf6f0ef0210dbcadac15e0c4d4471c4671230a1
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap-ng/libcap-ng_0.7.9.orig.tar.gz' libcap-ng_0.7.9.orig.tar.gz 449038 SHA256:4a1532bcf3731aade40936f6d6a586ed5a66ca4c7455e1338d1f6c3e09221328
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap-ng/libcap-ng_0.7.9-2.1build1.debian.tar.xz' libcap-ng_0.7.9-2.1build1.debian.tar.xz 6256 SHA256:b73a0a36bb0c1c8144828552dedb7b3493f4a08b1c31a0f1d7046cf1682eac7d
```

### `dpkg` source package: `libdatrie=0.2.12-3`

Binary Packages:

- `libdatrie1:amd64=0.2.12-3`

Licenses: (parsed from: `/usr/share/doc/libdatrie1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris libdatrie=0.2.12-3
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libdatrie/libdatrie_0.2.12-3.dsc' libdatrie_0.2.12-3.dsc 2260 SHA256:631b3aa1b0cf12bcb04df8a19a8370445801a176edce830e74c01f6a55f778aa
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libdatrie/libdatrie_0.2.12.orig.tar.xz' libdatrie_0.2.12.orig.tar.xz 310236 SHA256:452dcc4d3a96c01f80f7c291b42be11863cd1554ff78b93e110becce6e00b149
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libdatrie/libdatrie_0.2.12-3.debian.tar.xz' libdatrie_0.2.12-3.debian.tar.xz 9188 SHA256:10409d93b3762b8ac8e0851bb2b71f76c2c5b57df8999bf8b9686d951c8b7476
```

### `dpkg` source package: `liberror-perl=0.17029-1`

Binary Packages:

- `liberror-perl=0.17029-1`

Licenses: (parsed from: `/usr/share/doc/liberror-perl/copyright`)

- `Artistic`
- `GPL-1`
- `GPL-1+`
- `MIT/X11`

Source:

```console
$ apt-get source -qq --print-uris liberror-perl=0.17029-1
'http://archive.ubuntu.com/ubuntu/pool/main/libe/liberror-perl/liberror-perl_0.17029-1.dsc' liberror-perl_0.17029-1.dsc 2336 SHA256:0590467fe8c5f81bff9336e991462b2a9994b4876f4b732c8b8b31e927987cd7
'http://archive.ubuntu.com/ubuntu/pool/main/libe/liberror-perl/liberror-perl_0.17029.orig.tar.gz' liberror-perl_0.17029.orig.tar.gz 33304 SHA256:1a23f7913032aed6d4b68321373a3899ca66590f4727391a091ec19c95bf7adc
'http://archive.ubuntu.com/ubuntu/pool/main/libe/liberror-perl/liberror-perl_0.17029-1.debian.tar.xz' liberror-perl_0.17029-1.debian.tar.xz 4552 SHA256:a753b142c4c33ebf9cc98ae5f7a08da13b7c9ca2823ec26e45c96efb9c15c42e
```

### `dpkg` source package: `libffi=3.3-4`

Binary Packages:

- `libffi7:amd64=3.3-4`

Licenses: (parsed from: `/usr/share/doc/libffi7/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris libffi=3.3-4
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libffi/libffi_3.3-4.dsc' libffi_3.3-4.dsc 1932 SHA256:4190ad8e7ae9167a0c67c5926bc3705acb191745cca93ef845dbc06fc097f380
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libffi/libffi_3.3.orig.tar.gz' libffi_3.3.orig.tar.gz 1305466 SHA256:72fba7922703ddfa7a028d513ac15a85c8d54c8d67f55fa5a4802885dc652056
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libffi/libffi_3.3-4.debian.tar.xz' libffi_3.3-4.debian.tar.xz 9016 SHA256:0e8a6d9d87202d04d7646178479c3d365a845f9723da26625d533a169b378100
```

### `dpkg` source package: `libgcrypt20=1.8.5-5ubuntu1.1`

Binary Packages:

- `libgcrypt20:amd64=1.8.5-5ubuntu1.1`

Licenses: (parsed from: `/usr/share/doc/libgcrypt20/copyright`)

- `GPL-2`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris libgcrypt20=1.8.5-5ubuntu1.1
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgcrypt20/libgcrypt20_1.8.5-5ubuntu1.1.dsc' libgcrypt20_1.8.5-5ubuntu1.1.dsc 2915 SHA512:7b1cdda11632962e872b5d70b351851d95a3d5ed896f19650da618ef8ec835ed3aee54905b33f507ed16a7bae7d1ba0d5df8546712a1ee851bbed61d008250f9
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgcrypt20/libgcrypt20_1.8.5.orig.tar.bz2' libgcrypt20_1.8.5.orig.tar.bz2 2991291 SHA512:b55e16e838d1b1208e7673366971ae7c0f9c1c79e042f41c03d14ed74c5e387fa69ea81d5414ffda3d2b4f82ea5467fe13b00115727e257db22808cf351bde89
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgcrypt20/libgcrypt20_1.8.5.orig.tar.bz2.asc' libgcrypt20_1.8.5.orig.tar.bz2.asc 488 SHA512:3993c5e3f2f1714f40a9ad1a19782362c5b80c070ed8d76feacc503d8719f6775465f478098a092730e02683c665c5c91cf30e7700215aae2322be6230f207d6
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgcrypt20/libgcrypt20_1.8.5-5ubuntu1.1.debian.tar.xz' libgcrypt20_1.8.5-5ubuntu1.1.debian.tar.xz 34660 SHA512:ffcb506488147ceefe4c67c65de91f9d736d7e6a49d5ff3f04e8ec91a017a7c112c5bc46f6c71f07ff3dd565b494783cbd5b4f017f05c2a5b59f2955933d664b
```

### `dpkg` source package: `libgd2=2.2.5-5.2ubuntu2.4`

Binary Packages:

- `libgd3:amd64=2.2.5-5.2ubuntu2.4`

Licenses: (parsed from: `/usr/share/doc/libgd3/copyright`)

- `BSD-3-clause`
- `GAP~Makefile.in`
- `GAP~configure`
- `GD`
- `GPL-2`
- `GPL-2+`
- `GPL-2+ with Autoconf exception`
- `HPND`
- `MIT`
- `WEBP`
- `XFIG`

Source:

```console
$ apt-get source -qq --print-uris libgd2=2.2.5-5.2ubuntu2.4
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgd2/libgd2_2.2.5-5.2ubuntu2.4.dsc' libgd2_2.2.5-5.2ubuntu2.4.dsc 2369 SHA512:85ec82c758bf1dde2a9a10cf177067fd3acdc54be50700454e57c4177391daa93d0c31cd82c1c3dd5ec2b1468c767ae6b6202a9a0cf4d15846434f510e973fb7
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgd2/libgd2_2.2.5.orig.tar.gz' libgd2_2.2.5.orig.tar.gz 3326856 SHA512:e0556ec0d749ef988ee6b906c15f73d0871599b1cfacfc0965ea105b7f89e2ff6b0c6789ca98ef083449ce42831131220683581e007bf1b93140391624d0721c
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgd2/libgd2_2.2.5-5.2ubuntu2.4.debian.tar.xz' libgd2_2.2.5-5.2ubuntu2.4.debian.tar.xz 39052 SHA512:b503df88926af44625c9b30f29415c1bbfcd7eb106c0a2ac9b4b369baee1d79264e64f8f5a63abebdd03b16265a105283406d16a00e113e750be95ffca6a3941
```

### `dpkg` source package: `libgpg-error=1.37-1`

Binary Packages:

- `libgpg-error0:amd64=1.37-1`

Licenses: (parsed from: `/usr/share/doc/libgpg-error0/copyright`)

- `BSD-3-clause`
- `GPL-3`
- `GPL-3+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `g10-permissive`

Source:

```console
$ apt-get source -qq --print-uris libgpg-error=1.37-1
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgpg-error/libgpg-error_1.37-1.dsc' libgpg-error_1.37-1.dsc 2220 SHA256:e789ed6bf791c90e9ba28dc3923f54379862ca65bd286495942176dcfad5d8a7
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgpg-error/libgpg-error_1.37.orig.tar.bz2' libgpg-error_1.37.orig.tar.bz2 937282 SHA256:b32d6ff72a73cf79797f7f2d039e95e9c6f92f0c1450215410840ab62aea9763
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgpg-error/libgpg-error_1.37.orig.tar.bz2.asc' libgpg-error_1.37.orig.tar.bz2.asc 488 SHA256:394f0904c386f88e2b2db5042880a2a302cbc6e4ab902bacf3d338ded038066b
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgpg-error/libgpg-error_1.37-1.debian.tar.xz' libgpg-error_1.37-1.debian.tar.xz 17332 SHA256:09843b599726c1ab7b1fcd86ce617bd91d6378ff754c6da0b7e536ed1c3b6c16
```

### `dpkg` source package: `libice=2:1.0.10-0ubuntu1`

Binary Packages:

- `libice6:amd64=2:1.0.10-0ubuntu1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libice=2:1.0.10-0ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libice/libice_1.0.10-0ubuntu1.dsc' libice_1.0.10-0ubuntu1.dsc 1629 SHA256:51f58a0e5a5c5ea780baa3a057b61a921001831a4817da8825dbf592afccbdd6
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libice/libice_1.0.10.orig.tar.gz' libice_1.0.10.orig.tar.gz 481960 SHA256:1116bc64c772fd127a0d0c0ffa2833479905e3d3d8197740b3abd5f292f22d2d
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libice/libice_1.0.10-0ubuntu1.diff.gz' libice_1.0.10-0ubuntu1.diff.gz 6470 SHA256:a9187c11c1b372b0f4cb58c2fb21f780e9236fd7011bb32c4188c7b37112e8de
```

### `dpkg` source package: `libidn2=2.2.0-2`

Binary Packages:

- `libidn2-0:amd64=2.2.0-2`

Licenses: (parsed from: `/usr/share/doc/libidn2-0/copyright`)

- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `LGPL-3`
- `LGPL-3+`
- `Unicode`

Source:

```console
$ apt-get source -qq --print-uris libidn2=2.2.0-2
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libidn2/libidn2_2.2.0-2.dsc' libidn2_2.2.0-2.dsc 2436 SHA256:a5c5ece3748beaba9ce0a0b29cdab2fe9d861a965a7a96101a49f194acf759d6
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libidn2/libidn2_2.2.0.orig.tar.gz' libidn2_2.2.0.orig.tar.gz 2110743 SHA256:fc734732b506d878753ec6606982bf7b936e868c25c30ddb0d83f7d7056381fe
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libidn2/libidn2_2.2.0-2.debian.tar.xz' libidn2_2.2.0-2.debian.tar.xz 11184 SHA256:b38ce002d7eb1abbf2c870ac9570cd06a5087693f359b133defbf44b06f8784d
```

### `dpkg` source package: `libjpeg-turbo=2.0.3-0ubuntu1.20.04.3`

Binary Packages:

- `libjpeg-turbo8:amd64=2.0.3-0ubuntu1.20.04.3`

Licenses: (parsed from: `/usr/share/doc/libjpeg-turbo8/copyright`)

- `JPEG`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libjpeg-turbo=2.0.3-0ubuntu1.20.04.3
'http://archive.ubuntu.com/ubuntu/pool/main/libj/libjpeg-turbo/libjpeg-turbo_2.0.3-0ubuntu1.20.04.3.dsc' libjpeg-turbo_2.0.3-0ubuntu1.20.04.3.dsc 2337 SHA512:0855a6f5af33892e285752fc44766d902424b8390777b2432dbdff56a6e8275832010018012a54b395c64c0233cbd35f080000cc6780a4546549215638e4abc6
'http://archive.ubuntu.com/ubuntu/pool/main/libj/libjpeg-turbo/libjpeg-turbo_2.0.3.orig.tar.gz' libjpeg-turbo_2.0.3.orig.tar.gz 2161279 SHA512:745cc3d50b43dd84721bc3c341d561ffd7f54eda5bbe2d56cad62f4b51ea76da3b18aba9ca694a9db79379aba7a9971cb146387979e96ca6ece950871276cf2f
'http://archive.ubuntu.com/ubuntu/pool/main/libj/libjpeg-turbo/libjpeg-turbo_2.0.3-0ubuntu1.20.04.3.debian.tar.xz' libjpeg-turbo_2.0.3-0ubuntu1.20.04.3.debian.tar.xz 26328 SHA512:ce0f3f9e924cb24d114bccc65bada8f3f767e2a04f33d89f53cbbb59f884c87519e1d07d1610fa40af8dde5231a7d392e5483a30f563433fc41eef61fab32267
```

### `dpkg` source package: `libjpeg8-empty=8c-2ubuntu8`

Binary Packages:

- `libjpeg8:amd64=8c-2ubuntu8`

Licenses: (parsed from: `/usr/share/doc/libjpeg8/copyright`)

- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libjpeg8-empty=8c-2ubuntu8
'http://archive.ubuntu.com/ubuntu/pool/main/libj/libjpeg8-empty/libjpeg8-empty_8c-2ubuntu8.dsc' libjpeg8-empty_8c-2ubuntu8.dsc 1637 SHA256:e7f575dcb3e0d462513b6f928179baa0ff1d145273934b1041b714515096b407
'http://archive.ubuntu.com/ubuntu/pool/main/libj/libjpeg8-empty/libjpeg8-empty_8c-2ubuntu8.tar.gz' libjpeg8-empty_8c-2ubuntu8.tar.gz 1770 SHA256:48a4227e9fc70851a4f304b10624e02875bf6f4e2debfcbe4ba0dd85a3ec05c6
```

### `dpkg` source package: `libjsoncpp=1.7.4-3.1ubuntu2`

Binary Packages:

- `libjsoncpp1:amd64=1.7.4-3.1ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libjsoncpp1/copyright`)

- `Expat_or_PublicDomain_or_DualExpatPD`
- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris libjsoncpp=1.7.4-3.1ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/libj/libjsoncpp/libjsoncpp_1.7.4-3.1ubuntu2.dsc' libjsoncpp_1.7.4-3.1ubuntu2.dsc 2292 SHA256:29b690adbc515bc430e11cec45d9da7142e53893495beffe678e6b73a8f74b3d
'http://archive.ubuntu.com/ubuntu/pool/main/libj/libjsoncpp/libjsoncpp_1.7.4.orig.tar.gz' libjsoncpp_1.7.4.orig.tar.gz 205752 SHA256:10dcd0677e80727e572a1e462193e51a5fde3e023b99e144b2ee1a469835f769
'http://archive.ubuntu.com/ubuntu/pool/main/libj/libjsoncpp/libjsoncpp_1.7.4-3.1ubuntu2.debian.tar.xz' libjsoncpp_1.7.4-3.1ubuntu2.debian.tar.xz 8388 SHA256:1c21094022e664a66a2feb45f22520c6a66ecc6e558534647cf4fa7a14cb770a
```

### `dpkg` source package: `libksba=1.3.5-2ubuntu0.20.04.2`

Binary Packages:

- `libksba8:amd64=1.3.5-2ubuntu0.20.04.2`

Licenses: (parsed from: `/usr/share/doc/libksba8/copyright`)

- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris libksba=1.3.5-2ubuntu0.20.04.2
'http://archive.ubuntu.com/ubuntu/pool/main/libk/libksba/libksba_1.3.5-2ubuntu0.20.04.2.dsc' libksba_1.3.5-2ubuntu0.20.04.2.dsc 2697 SHA512:d0c165b3bdfbc90459056b2758bc46e3f392ca660ab25e7661adf9a0325cdddef11ba6aa0a6411e737e0ea6490e28e94e6575e11cd893bc93b21ed90ed256fff
'http://archive.ubuntu.com/ubuntu/pool/main/libk/libksba/libksba_1.3.5.orig.tar.bz2' libksba_1.3.5.orig.tar.bz2 620649 SHA512:60179bfd109b7b4fd8d2b30a3216540f03f5a13620d9a5b63f1f95788028708a420911619f172ba57e945a6a2fcd2ef7eaafc5585a0eb2b9652cfadf47bf39a2
'http://archive.ubuntu.com/ubuntu/pool/main/libk/libksba/libksba_1.3.5.orig.tar.bz2.asc' libksba_1.3.5.orig.tar.bz2.asc 287 SHA512:6b58b1c6ee924230e4f3b040836e85cb3b3f527f667bcb370c28d8ec702c884bcceab374688e02d0356dede81f9fcf975d726c1958d4d87e5c41757a6b2ba39e
'http://archive.ubuntu.com/ubuntu/pool/main/libk/libksba/libksba_1.3.5-2ubuntu0.20.04.2.debian.tar.xz' libksba_1.3.5-2ubuntu0.20.04.2.debian.tar.xz 15308 SHA512:a2289eb5c73dcef41bf8b66c70ddb216ebabf1912b81ad79af6db32c3b6c351a5c5dab703cabdbbc11026c6f7cc4433ca6a3ff6a031ee500cab625ba7ea30fc9
```

### `dpkg` source package: `libpng1.6=1.6.37-2`

Binary Packages:

- `libpng16-16:amd64=1.6.37-2`

Licenses: (parsed from: `/usr/share/doc/libpng16-16/copyright`)

- `Apache-2.0`
- `BSD-3-clause`
- `BSD-like-with-advertising-clause`
- `GPL-2`
- `GPL-2+`
- `expat`
- `libpng`
- `libpng OR Apache-2.0 OR BSD-3-clause`

Source:

```console
$ apt-get source -qq --print-uris libpng1.6=1.6.37-2
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpng1.6/libpng1.6_1.6.37-2.dsc' libpng1.6_1.6.37-2.dsc 2225 SHA256:4567a54b5804e068e61477e9cd78346557b85b72add10ef10f130a5be169662e
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpng1.6/libpng1.6_1.6.37.orig.tar.gz' libpng1.6_1.6.37.orig.tar.gz 1508805 SHA256:ca74a0dace179a8422187671aee97dd3892b53e168627145271cad5b5ac81307
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpng1.6/libpng1.6_1.6.37-2.debian.tar.xz' libpng1.6_1.6.37-2.debian.tar.xz 31844 SHA256:097cee0f0da4013d0231d37e090204ab3fa592b4fecdaaed3fca8d13affcaae8
```

### `dpkg` source package: `libpsl=0.21.0-1ubuntu1`

Binary Packages:

- `libpsl5:amd64=0.21.0-1ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libpsl5/copyright`)

- `Chromium`
- `MIT`

Source:

```console
$ apt-get source -qq --print-uris libpsl=0.21.0-1ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpsl/libpsl_0.21.0-1ubuntu1.dsc' libpsl_0.21.0-1ubuntu1.dsc 2383 SHA256:38d6cf06b8ac1929efe109ac3d5f37ea6e89ea82f7a5125db4dc7a7b5f3faf94
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpsl/libpsl_0.21.0.orig.tar.gz' libpsl_0.21.0.orig.tar.gz 8598583 SHA256:055aa87ec166c7afb985d0816c07ff440e1eb899881a318c51c69a0aeea8e279
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpsl/libpsl_0.21.0-1ubuntu1.debian.tar.xz' libpsl_0.21.0-1ubuntu1.debian.tar.xz 12476 SHA256:efd6c7ae8c244b582d6af943b5925d95a31a183abf695301f2fa49de9f694671
```

### `dpkg` source package: `libseccomp=2.5.1-1ubuntu1~20.04.2`

Binary Packages:

- `libseccomp2:amd64=2.5.1-1ubuntu1~20.04.2`

Licenses: (parsed from: `/usr/share/doc/libseccomp2/copyright`)

- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libseccomp=2.5.1-1ubuntu1~20.04.2
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libseccomp/libseccomp_2.5.1-1ubuntu1%7e20.04.2.dsc' libseccomp_2.5.1-1ubuntu1~20.04.2.dsc 2578 SHA512:ea3e505f936011ea2d37eb5c9c10fb0f7ead4f699180679940c1e27936c1b28fc96b40f98d4e25e1e058466244d08d29c2d538fff85d726808c2cec45f914509
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libseccomp/libseccomp_2.5.1.orig.tar.gz' libseccomp_2.5.1.orig.tar.gz 638811 SHA512:2be80a6323f9282dbeae8791724e5778b32e2382b2a3d1b0f77366371ec4072ea28128204f675cce101c091c0420d12c497e1a9ccbb7dc5bcbf61bfd777160af
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libseccomp/libseccomp_2.5.1-1ubuntu1%7e20.04.2.debian.tar.xz' libseccomp_2.5.1-1ubuntu1~20.04.2.debian.tar.xz 21168 SHA512:77187efe846d46f3cff589b048cd446f13f1d0d60274b54fa464e337288b9fd3979e1f3b6f4999af00e12738232b9397e485e977a732f74cb89cfa5bf90a21be
```

### `dpkg` source package: `libselinux=3.0-1build2`

Binary Packages:

- `libselinux1:amd64=3.0-1build2`

Licenses: (parsed from: `/usr/share/doc/libselinux1/copyright`)

- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libselinux=3.0-1build2
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libselinux/libselinux_3.0-1build2.dsc' libselinux_3.0-1build2.dsc 2565 SHA256:9a8d6c354ed06350606c009d899d117e71fda20887792b2c25b38222d0190d93
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libselinux/libselinux_3.0.orig.tar.gz' libselinux_3.0.orig.tar.gz 212096 SHA256:2ea2b30f671dae9d6b1391cbe8fb2ce5d36a3ee4fb1cd3c32f0d933c31b82433
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libselinux/libselinux_3.0-1build2.debian.tar.xz' libselinux_3.0-1build2.debian.tar.xz 23720 SHA256:ed85da0fe5561205c95f0f622562425dc7d8dd61ffd213a7fa914d778fe8da71
```

### `dpkg` source package: `libsemanage=3.0-1build2`

Binary Packages:

- `libsemanage-common=3.0-1build2`
- `libsemanage1:amd64=3.0-1build2`

Licenses: (parsed from: `/usr/share/doc/libsemanage-common/copyright`, `/usr/share/doc/libsemanage1/copyright`)

- `GPL`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris libsemanage=3.0-1build2
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsemanage/libsemanage_3.0-1build2.dsc' libsemanage_3.0-1build2.dsc 2678 SHA256:6231f4b00991657fafef2595eb571b2bcbe437de4ec9dc9929c0e69187db5f33
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsemanage/libsemanage_3.0.orig.tar.gz' libsemanage_3.0.orig.tar.gz 180745 SHA256:a497b0720d54eac427f1f3f618eed417e50ed8f4e47ed0f7a1d391bd416e84cf
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsemanage/libsemanage_3.0-1build2.debian.tar.xz' libsemanage_3.0-1build2.debian.tar.xz 17176 SHA256:38a646f91532c920c8c15a695c3585397ddbf032ecf49c52eb89d53c8eac48fb
```

### `dpkg` source package: `libsepol=3.0-1ubuntu0.1`

Binary Packages:

- `libsepol1:amd64=3.0-1ubuntu0.1`

Licenses: (parsed from: `/usr/share/doc/libsepol1/copyright`)

- `GPL`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris libsepol=3.0-1ubuntu0.1
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsepol/libsepol_3.0-1ubuntu0.1.dsc' libsepol_3.0-1ubuntu0.1.dsc 2084 SHA512:4fa31e95c4f00cdac984d0cd7ffdd4ca6d3a9be529723cc227316e9f4bb76b5910102f136aab505de422f9794c4641912720c8dffb10e6ae0523058fa96850d8
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsepol/libsepol_3.0.orig.tar.gz' libsepol_3.0.orig.tar.gz 473864 SHA512:82a5bae0afd9ae53b55ddcfc9f6dd61724a55e45aef1d9cd0122d1814adf2abe63c816a7ac63b64b401f5c67acb910dd8e0574eec546bed04da7842ab6c3bb55
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsepol/libsepol_3.0-1ubuntu0.1.debian.tar.xz' libsepol_3.0-1ubuntu0.1.debian.tar.xz 16980 SHA512:eeade6f2ad6eb2aa2846e850516f56da34bdf6dab2e6024c94799c273e6815976a09509b999306337107e3e21cbb5243c29dc515b4c48bfb51d2dfe9c3ed0da6
```

### `dpkg` source package: `libsm=2:1.2.3-1`

Binary Packages:

- `libsm6:amd64=2:1.2.3-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libsm=2:1.2.3-1
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsm/libsm_1.2.3-1.dsc' libsm_1.2.3-1.dsc 2063 SHA256:5488f8de81d53c32cbb5f062b6a6f262cd067283b8082041392dc60f0d04002c
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsm/libsm_1.2.3.orig.tar.gz' libsm_1.2.3.orig.tar.gz 445362 SHA256:1e92408417cb6c6c477a8a6104291001a40b3bb56a4a60608fdd9cd2c5a0f320
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsm/libsm_1.2.3-1.diff.gz' libsm_1.2.3-1.diff.gz 8929 SHA256:7eb99ab50b19f26d1470f89e4b46891f6a697cb1794a58ed0d1376cceaf1b6a9
```

### `dpkg` source package: `libssh=0.9.3-2ubuntu2.5`

Binary Packages:

- `libssh-4:amd64=0.9.3-2ubuntu2.5`

Licenses: (parsed from: `/usr/share/doc/libssh-4/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `LGPL-2.1`
- `LGPL-2.1+~OpenSSL`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris libssh=0.9.3-2ubuntu2.5
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libssh/libssh_0.9.3-2ubuntu2.5.dsc' libssh_0.9.3-2ubuntu2.5.dsc 2538 SHA512:dd905eeaa75320e90a03c9dd37bfc462bbaadd022d68c07b1224227cca57a71eed215c017e23df82a37821f87f32e608c4f6e3cabffdf175190e6ed0cf3e5140
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libssh/libssh_0.9.3.orig.tar.xz' libssh_0.9.3.orig.tar.xz 500068 SHA512:6e59718565daeca6d224426cc1095a112deff9af8e0b021917e04f08bb7409263c35724de95f591f38e26f0fb3bbbbc69b679b6775edc21dec158d241b076c6f
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libssh/libssh_0.9.3-2ubuntu2.5.debian.tar.xz' libssh_0.9.3-2ubuntu2.5.debian.tar.xz 54112 SHA512:784e6ec20522eb9526cb4f3981c9c4d3b80879a3d06f80617fb26fd604ab8459e425ac7482fe5a7f0e2ab7f408edab578b66ea0beda4abb6b1e5e0cc1cc9b1cf
```

### `dpkg` source package: `libtasn1-6=4.16.0-2ubuntu0.1`

Binary Packages:

- `libtasn1-6:amd64=4.16.0-2ubuntu0.1`

Licenses: (parsed from: `/usr/share/doc/libtasn1-6/copyright`)

- `GFDL-1.3`
- `GPL-3`
- `LGPL`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libtasn1-6=4.16.0-2ubuntu0.1
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtasn1-6/libtasn1-6_4.16.0-2ubuntu0.1.dsc' libtasn1-6_4.16.0-2ubuntu0.1.dsc 2746 SHA512:39ec03bb0c84ca378652bfadad5b20ee0a41235299330691608bd5ac050d15dd960866e90fe35cce4898b1eaa3fcb0a0d1e01ebb8bef69913ec3fce1a1eca210
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtasn1-6/libtasn1-6_4.16.0.orig.tar.gz' libtasn1-6_4.16.0.orig.tar.gz 1812442 SHA512:b356249535d5d592f9b59de39d21e26dd0f3f00ea47c9cef292cdd878042ea41ecbb7c8d2f02ac5839f5210092fe92a25acd343260ddf644887b031b167c2e71
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtasn1-6/libtasn1-6_4.16.0.orig.tar.gz.asc' libtasn1-6_4.16.0.orig.tar.gz.asc 488 SHA512:53254c2ce61e9bb889fe00b43ef2130ab9f122c44832538e3f7b38cb75ada1656213cf5c8c85321078c6b98d325c46eff41ea64d1971d3183f2ec568a18f7ed2
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtasn1-6/libtasn1-6_4.16.0-2ubuntu0.1.debian.tar.xz' libtasn1-6_4.16.0-2ubuntu0.1.debian.tar.xz 20324 SHA512:7b69f7ec20f5ec6208a6bded750a9fa95f1532ba22a7e294661195a84fc995c87d89bc6aeacf4630d3bd10bea4589e32413fcdeb08df0529b6d89ddf4091c6ec
```

### `dpkg` source package: `libthai=0.1.28-3`

Binary Packages:

- `libthai-data=0.1.28-3`
- `libthai0:amd64=0.1.28-3`

Licenses: (parsed from: `/usr/share/doc/libthai-data/copyright`, `/usr/share/doc/libthai0/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris libthai=0.1.28-3
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libthai/libthai_0.1.28-3.dsc' libthai_0.1.28-3.dsc 2346 SHA256:a6317b6a8e4ba40cedb10a9a659fc23885bfbe5eb8cf3a8b325a86064b0a542d
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libthai/libthai_0.1.28.orig.tar.xz' libthai_0.1.28.orig.tar.xz 413592 SHA256:ffe0a17b4b5aa11b153c15986800eca19f6c93a4025ffa5cf2cab2dcdf1ae911
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libthai/libthai_0.1.28-3.debian.tar.xz' libthai_0.1.28-3.debian.tar.xz 12128 SHA256:bca48abd9d040e844ebcb1f91a6ab4bcdfad66e36c1143f79d60461e933fddf9
```

### `dpkg` source package: `libtool=2.4.6-14`

Binary Packages:

- `libltdl7:amd64=2.4.6-14`

Licenses: (parsed from: `/usr/share/doc/libltdl7/copyright`)

- `GFDL`
- `GPL`

Source:

```console
$ apt-get source -qq --print-uris libtool=2.4.6-14
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtool/libtool_2.4.6-14.dsc' libtool_2.4.6-14.dsc 2500 SHA256:939797b7ce62f69641d319e5d38e53b1608cee649355046eec74271e9fcfb9df
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtool/libtool_2.4.6.orig.tar.xz' libtool_2.4.6.orig.tar.xz 973080 SHA256:7c87a8c2c8c0fc9cd5019e402bed4292462d00a718a7cd5f11218153bf28b26f
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtool/libtool_2.4.6.orig.tar.xz.asc' libtool_2.4.6.orig.tar.xz.asc 380 SHA256:ab68ebc45d60128a71fc36167cd29dcf3c3d6d639fd28663905ebaf3e2f43d6a
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtool/libtool_2.4.6-14.debian.tar.xz' libtool_2.4.6-14.debian.tar.xz 50832 SHA256:3ef693ea30def97a19fd94ffb2fa5421d5dc35cf7ad897a7161bd647eb4f2415
```

### `dpkg` source package: `libunistring=0.9.10-2`

Binary Packages:

- `libunistring2:amd64=0.9.10-2`

Licenses: (parsed from: `/usr/share/doc/libunistring2/copyright`)

- `FreeSoftware`
- `GFDL-1.2`
- `GFDL-1.2+`
- `GPL-2`
- `GPL-2+`
- `GPL-2+ with distribution exception`
- `GPL-3`
- `GPL-3+`
- `LGPL-3`
- `LGPL-3+`
- `MIT`

Source:

```console
$ apt-get source -qq --print-uris libunistring=0.9.10-2
'http://archive.ubuntu.com/ubuntu/pool/main/libu/libunistring/libunistring_0.9.10-2.dsc' libunistring_0.9.10-2.dsc 2206 SHA256:c6faf64e2d978ec074ebf88264730121dfd03cc1639df94b5dc3eb05b1678532
'http://archive.ubuntu.com/ubuntu/pool/main/libu/libunistring/libunistring_0.9.10.orig.tar.xz' libunistring_0.9.10.orig.tar.xz 2051320 SHA256:eb8fb2c3e4b6e2d336608377050892b54c3c983b646c561836550863003c05d7
'http://archive.ubuntu.com/ubuntu/pool/main/libu/libunistring/libunistring_0.9.10.orig.tar.xz.asc' libunistring_0.9.10.orig.tar.xz.asc 1310 SHA256:e1606f691034fa21b00e08269622743547c16d21cca6c8a64156b4774a49e78e
'http://archive.ubuntu.com/ubuntu/pool/main/libu/libunistring/libunistring_0.9.10-2.debian.tar.xz' libunistring_0.9.10-2.debian.tar.xz 40708 SHA256:5e291a1a15549d12c64575c72868a8c94586715d35062b5efb48fe9a9d09924e
```

### `dpkg` source package: `libuv1=1.34.2-1ubuntu1.5`

Binary Packages:

- `libuv1:amd64=1.34.2-1ubuntu1.5`

Licenses: (parsed from: `/usr/share/doc/libuv1/copyright`)

- `BSD-1-clause`
- `BSD-2-clause`
- `BSD-3-clause`
- `CC-BY-4.0`
- `Expat`
- `GPL-3`
- `GPL-3+`
- `ISC`

Source:

```console
$ apt-get source -qq --print-uris libuv1=1.34.2-1ubuntu1.5
'http://archive.ubuntu.com/ubuntu/pool/main/libu/libuv1/libuv1_1.34.2-1ubuntu1.5.dsc' libuv1_1.34.2-1ubuntu1.5.dsc 2128 SHA512:70f27eb8a8c45735215e56dee4040ff3c9ac0ca085f276ae77ef7ff2505612dd021e53372269af2511abc93ca23830bd0e30aad753130780f41265dabe16690d
'http://archive.ubuntu.com/ubuntu/pool/main/libu/libuv1/libuv1_1.34.2.orig.tar.gz' libuv1_1.34.2.orig.tar.gz 1245417 SHA512:c549be16d10c1935150a395126b07b45e93ccb6edfe4a03f24bf4de39476f1e0339f22c3960022ae6170c5bb0667c77b16eb0b434aae280a53145fe5369de033
'http://archive.ubuntu.com/ubuntu/pool/main/libu/libuv1/libuv1_1.34.2-1ubuntu1.5.debian.tar.xz' libuv1_1.34.2-1ubuntu1.5.debian.tar.xz 25824 SHA512:dd2ffe27b6fdfe68faaec7ea1886296904be9993f8e4ac98e22f27a24658b1a847c066353fa3404a1728d3ef520743038a1c76900edc6c6c8b9e554393e2f92c
```

### `dpkg` source package: `libwebp=0.6.1-2ubuntu0.20.04.3`

Binary Packages:

- `libwebp6:amd64=0.6.1-2ubuntu0.20.04.3`

Licenses: (parsed from: `/usr/share/doc/libwebp6/copyright`)

- `Apache-2.0`

Source:

```console
$ apt-get source -qq --print-uris libwebp=0.6.1-2ubuntu0.20.04.3
'http://archive.ubuntu.com/ubuntu/pool/main/libw/libwebp/libwebp_0.6.1-2ubuntu0.20.04.3.dsc' libwebp_0.6.1-2ubuntu0.20.04.3.dsc 2185 SHA512:33627b740e59b83196c414f859d31c037e12cf4ec92ac2db7e60356141422cd6c7bfcc41bb07cc08095a8797d35ea0e3d869bc195e7a010754f5ac3acbcd10b0
'http://archive.ubuntu.com/ubuntu/pool/main/libw/libwebp/libwebp_0.6.1.orig.tar.gz' libwebp_0.6.1.orig.tar.gz 3554290 SHA512:313b345a01c91eb07c2e4d46b93fcda9c50dca9e05e39f757238a679355514a2e9bc9bc220f3d3eb6d6a55148957cb2be14dac330203953337759841af1a32bf
'http://archive.ubuntu.com/ubuntu/pool/main/libw/libwebp/libwebp_0.6.1-2ubuntu0.20.04.3.debian.tar.xz' libwebp_0.6.1-2ubuntu0.20.04.3.debian.tar.xz 21132 SHA512:f9bbf3f92f5c1cebae08828e475d84bd854870a02d65ac9373a7c10a09e445f032b4bf4becd69b81a609e76f96f12b2d087c6065b1e8427cee2effcbf28377b8
```

### `dpkg` source package: `libx11=2:1.6.9-2ubuntu1.6`

Binary Packages:

- `libx11-6:amd64=2:1.6.9-2ubuntu1.6`
- `libx11-data=2:1.6.9-2ubuntu1.6`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libx11=2:1.6.9-2ubuntu1.6
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libx11/libx11_1.6.9-2ubuntu1.6.dsc' libx11_1.6.9-2ubuntu1.6.dsc 2671 SHA512:46674410511381909f8f29ee70138e3158098c0937784783574bbccca9ce43e319f49663df5d8fb6e5ee57e33bccaaf7b8c9590183bfda4c80a8b9ac7173594a
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libx11/libx11_1.6.9.orig.tar.gz' libx11_1.6.9.orig.tar.gz 2994329 SHA512:c79cf0924e920a2e8d2e9af45e73ed42b565dea79ac68d4c3889033738274694b29cedb62c057fec1aa7f7ad7dcf843334fccb43470bbae7922d42373c1c6045
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libx11/libx11_1.6.9.orig.tar.gz.asc' libx11_1.6.9.orig.tar.gz.asc 659 SHA512:56e53d1481be4e12f89af2fbcd297a3612996f5ca1eae39d6fe336f9b52832ea430ac0568e556b9e57291562c56590086871c08ec7ac046f15af4211f680adee
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libx11/libx11_1.6.9-2ubuntu1.6.diff.gz' libx11_1.6.9-2ubuntu1.6.diff.gz 71964 SHA512:61bbb0b65991c46fb5f63d4698abf3ac484cf156bbcc665583a549e729975e9b45adf41a865dd59ed719426da9c703bf733626dd829450ffc58e02139af9808f
```

### `dpkg` source package: `libxau=1:1.0.9-0ubuntu1`

Binary Packages:

- `libxau6:amd64=1:1.0.9-0ubuntu1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxau=1:1.0.9-0ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxau/libxau_1.0.9-0ubuntu1.dsc' libxau_1.0.9-0ubuntu1.dsc 1563 SHA256:b59509d1f8f6c0e21b8bbd46ac1dffcd7a21a635ff3ce9c0acf68ba60fcb5e11
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxau/libxau_1.0.9.orig.tar.gz' libxau_1.0.9.orig.tar.gz 394068 SHA256:1f123d8304b082ad63a9e89376400a3b1d4c29e67e3ea07b3f659cccca690eea
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxau/libxau_1.0.9-0ubuntu1.diff.gz' libxau_1.0.9-0ubuntu1.diff.gz 15142 SHA256:cf7e9d50c3b3b8dde3486ee6fcf9bb96585e2af32924e91c10c8612e48b5dce5
```

### `dpkg` source package: `libxaw=2:1.0.13-1`

Binary Packages:

- `libxaw7:amd64=2:1.0.13-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxaw=2:1.0.13-1
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxaw/libxaw_1.0.13-1.dsc' libxaw_1.0.13-1.dsc 2196 SHA256:9fdf48f9ff66c0889cda5030997fe919e5320e7988f32e20bb96602daa37e7f7
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxaw/libxaw_1.0.13.orig.tar.gz' libxaw_1.0.13.orig.tar.gz 848997 SHA256:7e74ac3e5f67def549722ff0333d6e6276b8becd9d89615cda011e71238ab694
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxaw/libxaw_1.0.13-1.diff.gz' libxaw_1.0.13-1.diff.gz 12643 SHA256:241f21ba0810d9d859a98ab60f100a366bc9e98cd946c736566a8ed1353a1bcc
```

### `dpkg` source package: `libxcb=1.14-2`

Binary Packages:

- `libxcb-render0:amd64=1.14-2`
- `libxcb-shm0:amd64=1.14-2`
- `libxcb1:amd64=1.14-2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxcb=1.14-2
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxcb/libxcb_1.14-2.dsc' libxcb_1.14-2.dsc 5344 SHA256:997dfadefa35a243a7160b62d628bb25e45439f61687459d581502905bcf1fb2
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxcb/libxcb_1.14.orig.tar.gz' libxcb_1.14.orig.tar.gz 640322 SHA256:2c7fcddd1da34d9b238c9caeda20d3bd7486456fc50b3cc6567185dbd5b0ad02
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxcb/libxcb_1.14-2.diff.gz' libxcb_1.14-2.diff.gz 25716 SHA256:92d7e0a80c3c7f2a5b5afd0c0702183f1c483338d678d67d8d0e61fd8989ba85
```

### `dpkg` source package: `libxcrypt=1:4.4.10-10ubuntu4`

Binary Packages:

- `libcrypt-dev:amd64=1:4.4.10-10ubuntu4`
- `libcrypt1:amd64=1:4.4.10-10ubuntu4`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxcrypt=1:4.4.10-10ubuntu4
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxcrypt/libxcrypt_4.4.10-10ubuntu4.dsc' libxcrypt_4.4.10-10ubuntu4.dsc 2216 SHA256:457576b36eaa34dcf28b19e942908221d0618e9e4a2c0b9e11ba9693770756a2
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxcrypt/libxcrypt_4.4.10.orig.tar.xz' libxcrypt_4.4.10.orig.tar.xz 372652 SHA256:f790a8eac4e4af3124d2844a24a7afb3a972368e4dff63d701599c2f2d065fd3
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxcrypt/libxcrypt_4.4.10-10ubuntu4.debian.tar.xz' libxcrypt_4.4.10-10ubuntu4.debian.tar.xz 5760 SHA256:b2e665b5224911d24dbcbddfc61b7a27428c3ecb744f29ceea1b2984496f2ffa
```

### `dpkg` source package: `libxdmcp=1:1.1.3-0ubuntu1`

Binary Packages:

- `libxdmcp6:amd64=1:1.1.3-0ubuntu1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxdmcp=1:1.1.3-0ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxdmcp/libxdmcp_1.1.3-0ubuntu1.dsc' libxdmcp_1.1.3-0ubuntu1.dsc 1608 SHA256:3f98e3917b5de252eb517c55743bcc5682b43c9f70ead33231ac4318bbc816e1
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxdmcp/libxdmcp_1.1.3.orig.tar.gz' libxdmcp_1.1.3.orig.tar.gz 429668 SHA256:2ef9653d32e09d1bf1b837d0e0311024979653fe755ad3aaada8db1aa6ea180c
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxdmcp/libxdmcp_1.1.3-0ubuntu1.diff.gz' libxdmcp_1.1.3-0ubuntu1.diff.gz 18079 SHA256:3037a57202b724ecd7db70c21a601f58277c02ba89e7e5d999973e5baf6d05ca
```

### `dpkg` source package: `libxext=2:1.3.4-0ubuntu1`

Binary Packages:

- `libxext6:amd64=2:1.3.4-0ubuntu1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxext=2:1.3.4-0ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxext/libxext_1.3.4-0ubuntu1.dsc' libxext_1.3.4-0ubuntu1.dsc 1727 SHA256:8319de2750f28c78e01267a5593776f10afd3f863d4820abe72dbf855a3a77ae
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxext/libxext_1.3.4.orig.tar.gz' libxext_1.3.4.orig.tar.gz 494434 SHA256:8ef0789f282826661ff40a8eef22430378516ac580167da35cc948be9041aac1
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxext/libxext_1.3.4-0ubuntu1.diff.gz' libxext_1.3.4-0ubuntu1.diff.gz 20663 SHA256:87a4d23f1f9ff53f3a6cd7cc35252a1249dc63d274c566ea7e23b23585a86170
```

### `dpkg` source package: `libxml2=2.9.10+dfsg-5ubuntu0.20.04.10`

Binary Packages:

- `libxml2:amd64=2.9.10+dfsg-5ubuntu0.20.04.10`
- `libxml2-utils=2.9.10+dfsg-5ubuntu0.20.04.10`

Licenses: (parsed from: `/usr/share/doc/libxml2/copyright`, `/usr/share/doc/libxml2-utils/copyright`)

- `ISC`
- `MIT-1`

Source:

```console
$ apt-get source -qq --print-uris libxml2=2.9.10+dfsg-5ubuntu0.20.04.10
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxml2/libxml2_2.9.10%2bdfsg-5ubuntu0.20.04.10.dsc' libxml2_2.9.10+dfsg-5ubuntu0.20.04.10.dsc 3125 SHA512:3023fba17f5c5fd742e2a396e247643f1b6e4681d02d4f8b9ae25a08cd282c4cc45d2879b3b6528a3e244e3e5d5d98ede9512b4bbf27bfedac2b3bbaf9a1fd66
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxml2/libxml2_2.9.10%2bdfsg.orig.tar.xz' libxml2_2.9.10+dfsg.orig.tar.xz 2503560 SHA512:605c6c0f8bf2c53208d0a036ff09a4025843f45139b711c90dc83066feda2f285a5578d55d4a58d33eedbe7485a5c1ec5608ba6c6beed1fb55649f87dca0cec3
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxml2/libxml2_2.9.10%2bdfsg-5ubuntu0.20.04.10.debian.tar.xz' libxml2_2.9.10+dfsg-5ubuntu0.20.04.10.debian.tar.xz 46084 SHA512:cd55ce806cf12d250c213abe228e1b43966c1af6a3e205abb94d858ef5dd76c6b8cbbd97bd5644dbf7e474911e80dfe38e0cd3a544ef2383e8f4668b77e442a8
```

### `dpkg` source package: `libxmu=2:1.1.3-0ubuntu1`

Binary Packages:

- `libxmu6:amd64=2:1.1.3-0ubuntu1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxmu=2:1.1.3-0ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxmu/libxmu_1.1.3-0ubuntu1.dsc' libxmu_1.1.3-0ubuntu1.dsc 1797 SHA256:ba64fdbc1b602eac436ae7ea58f57d72a45ee23b016eba542ce8b704508f717c
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxmu/libxmu_1.1.3.orig.tar.gz' libxmu_1.1.3.orig.tar.gz 497343 SHA256:5bd9d4ed1ceaac9ea023d86bf1c1632cd3b172dce4a193a72a94e1d9df87a62e
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxmu/libxmu_1.1.3-0ubuntu1.diff.gz' libxmu_1.1.3-0ubuntu1.diff.gz 6373 SHA256:7519cc7be957da29adc420426b57e1366228448c6205c5e4b89d04bfa948ffa7
```

### `dpkg` source package: `libxpm=1:3.5.12-1ubuntu0.20.04.2`

Binary Packages:

- `libxpm4:amd64=1:3.5.12-1ubuntu0.20.04.2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxpm=1:3.5.12-1ubuntu0.20.04.2
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxpm/libxpm_3.5.12-1ubuntu0.20.04.2.dsc' libxpm_3.5.12-1ubuntu0.20.04.2.dsc 2203 SHA512:034d036c884169883acaad3095e1749726f92125ecb24c0205f5fd584bcd9b38447b16f1f6e3b8189c37e93f62f151da3766918bed8c3caf4f158c17e09b2181
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxpm/libxpm_3.5.12.orig.tar.gz' libxpm_3.5.12.orig.tar.gz 529302 SHA512:17169016efc1e139f079290b2369fd62df8617867d97d2f50940521951a50f173118143109f0d7c552de92913cefc5ccaeb52225ccdd9abc89b3b85d9b5669f7
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxpm/libxpm_3.5.12-1ubuntu0.20.04.2.diff.gz' libxpm_3.5.12-1ubuntu0.20.04.2.diff.gz 19063 SHA512:1b2b6dc8bdd2ebcdd183dbfc85703ea811a4e6066be76e5b4954cf6d1bcb4dfbc82fe3a744ab432bb0adba063425152532bce448d08ec8eeffda8b3230e1892a
```

### `dpkg` source package: `libxrender=1:0.9.10-1`

Binary Packages:

- `libxrender1:amd64=1:0.9.10-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxrender=1:0.9.10-1
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxrender/libxrender_0.9.10-1.dsc' libxrender_0.9.10-1.dsc 2064 SHA256:95d6471218b44f4e60c48cea60cfb4865bbe861530add23f6c859515bee92dbd
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxrender/libxrender_0.9.10.orig.tar.gz' libxrender_0.9.10.orig.tar.gz 373717 SHA256:770527cce42500790433df84ec3521e8bf095dfe5079454a92236494ab296adf
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxrender/libxrender_0.9.10-1.diff.gz' libxrender_0.9.10-1.diff.gz 15399 SHA256:ff56a0a00119383adc5f1731e86155ae5c2de069e1d059a9da1d777917430588
```

### `dpkg` source package: `libxslt=1.1.34-4ubuntu0.20.04.3`

Binary Packages:

- `libxslt1.1:amd64=1.1.34-4ubuntu0.20.04.3`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxslt=1.1.34-4ubuntu0.20.04.3
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxslt/libxslt_1.1.34-4ubuntu0.20.04.3.dsc' libxslt_1.1.34-4ubuntu0.20.04.3.dsc 2514 SHA512:ce5f4fb988ddc96259e3ae09190ed990d798de57b2e6c9fd9c3187588e0e62e5aa8779a2138184d713ac8792ce790bda6200a8a3a51732c4d19eb6a661931acb
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxslt/libxslt_1.1.34.orig.tar.gz' libxslt_1.1.34.orig.tar.gz 3552258 SHA512:1516a11ad608b04740674060d2c5d733b88889de5e413b9a4e8bf8d1a90d712149df6d2b1345b615f529d7c7d3fa6dae12e544da828b39c7d415e54c0ee0776b
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxslt/libxslt_1.1.34.orig.tar.gz.asc' libxslt_1.1.34.orig.tar.gz.asc 488 SHA512:9b155d4571daede99cdbf2813a85fb04812737b5e23d3f7c9840225b38f3dbf171623a21645daaee190e7ff9ba38bde932922e96a2a2312c203ffa9917c3baea
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxslt/libxslt_1.1.34-4ubuntu0.20.04.3.debian.tar.xz' libxslt_1.1.34-4ubuntu0.20.04.3.debian.tar.xz 24648 SHA512:77b0a3713791c44094ba50f5cfa5ae8444917030d2a3be3fc15ac5cf0f1898054c76409d25fce85f1927ea4a4f004e1266d94592cecfbc4b6cbfa8b74a976351
```

### `dpkg` source package: `libxt=1:1.1.5-1`

Binary Packages:

- `libxt6:amd64=1:1.1.5-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxt=1:1.1.5-1
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxt/libxt_1.1.5-1.dsc' libxt_1.1.5-1.dsc 2109 SHA256:f44ae1393c9fd02c0b3dd03576c7b26e6c7b09de3271a87e018efadeed311639
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxt/libxt_1.1.5.orig.tar.gz' libxt_1.1.5.orig.tar.gz 962169 SHA256:b59bee38a9935565fa49dc1bfe84cb30173e2e07e1dcdf801430d4b54eb0caa3
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxt/libxt_1.1.5-1.diff.gz' libxt_1.1.5-1.diff.gz 14462 SHA256:822fe813d1ea9213e6fde91cbb607c0b6874341dc19b77b0f6649b8be8472d82
```

### `dpkg` source package: `libyaml=0.2.2-1`

Binary Packages:

- `libyaml-0-2:amd64=0.2.2-1`
- `libyaml-dev:amd64=0.2.2-1`

Licenses: (parsed from: `/usr/share/doc/libyaml-0-2/copyright`, `/usr/share/doc/libyaml-dev/copyright`)

- `Expat`
- `permissive`

Source:

```console
$ apt-get source -qq --print-uris libyaml=0.2.2-1
'http://archive.ubuntu.com/ubuntu/pool/main/liby/libyaml/libyaml_0.2.2-1.dsc' libyaml_0.2.2-1.dsc 1833 SHA256:b4baba985391f52409013a0c9303191e34aaa4c1c9200e4c01c4963df801db09
'http://archive.ubuntu.com/ubuntu/pool/main/liby/libyaml/libyaml_0.2.2.orig.tar.gz' libyaml_0.2.2.orig.tar.gz 602509 SHA256:689ef3ebdecfa81f3789ccd2481acc81fc0f22f3f5c947eed95c4c0802e356b8
'http://archive.ubuntu.com/ubuntu/pool/main/liby/libyaml/libyaml_0.2.2-1.debian.tar.xz' libyaml_0.2.2-1.debian.tar.xz 4112 SHA256:186aad3e4bcd95891a8c59249c59f862f5f71601058fda0bf020a9e9e39320fe
```

### `dpkg` source package: `libzstd=1.4.4+dfsg-3ubuntu0.1`

Binary Packages:

- `libzstd-dev:amd64=1.4.4+dfsg-3ubuntu0.1`
- `libzstd1:amd64=1.4.4+dfsg-3ubuntu0.1`

Licenses: (parsed from: `/usr/share/doc/libzstd-dev/copyright`, `/usr/share/doc/libzstd1/copyright`)

- `BSD-3-clause`
- `Expat`
- `GPL-2`
- `GPL-2+`
- `zlib`

Source:

```console
$ apt-get source -qq --print-uris libzstd=1.4.4+dfsg-3ubuntu0.1
'http://archive.ubuntu.com/ubuntu/pool/main/libz/libzstd/libzstd_1.4.4%2bdfsg-3ubuntu0.1.dsc' libzstd_1.4.4+dfsg-3ubuntu0.1.dsc 2381 SHA512:a135412be4afdea573f991d8e4822f9885dbd607c87fb22e72d2defa160cf64f85a6047a9c9120b6eda3b8927306407278779f9e7a6976d7b15fb08750f32f74
'http://archive.ubuntu.com/ubuntu/pool/main/libz/libzstd/libzstd_1.4.4%2bdfsg.orig.tar.xz' libzstd_1.4.4+dfsg.orig.tar.xz 1357144 SHA512:85c64662303dda72d61fcbe41dfc6b310e63b20b043f41d4fb5a5ebc38ea83986c8c217fb259dfc2c024538ee8a519bb944914542a0b3a5c4dd988d5fdb248b7
'http://archive.ubuntu.com/ubuntu/pool/main/libz/libzstd/libzstd_1.4.4%2bdfsg-3ubuntu0.1.debian.tar.xz' libzstd_1.4.4+dfsg-3ubuntu0.1.debian.tar.xz 17300 SHA512:0484891be5603d00bd57b799c708b9395fccbaa8c6c44f535377f6fa2c7ac22c01c8a3c1b45e1c1f3c30f19dc74d510626bf82067fcbfb53c39f1bcc2249affe
```

### `dpkg` source package: `linux=5.4.0-216.236`

Binary Packages:

- `linux-libc-dev:amd64=5.4.0-216.236`

Licenses: (parsed from: `/usr/share/doc/linux-libc-dev/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris linux=5.4.0-216.236
'http://archive.ubuntu.com/ubuntu/pool/main/l/linux/linux_5.4.0-216.236.dsc' linux_5.4.0-216.236.dsc 7401 SHA512:3c03811e64371dd5398677438064ed049fb8d40f34260756d05791530425ea4c942e474962d29af711321588bc3e76b8546c55e2411b6db344eff72fb567ebc4
'http://archive.ubuntu.com/ubuntu/pool/main/l/linux/linux_5.4.0.orig.tar.gz' linux_5.4.0.orig.tar.gz 170244619 SHA512:62b09a7231fd793973c5f59b16c4f6ffce621188b02a71915874b05e8e3f956fb6146d4a4fb1a4475bebe463949ca5a18da12842c3ce7c52e996e6bc4012a074
'http://archive.ubuntu.com/ubuntu/pool/main/l/linux/linux_5.4.0-216.236.diff.gz' linux_5.4.0-216.236.diff.gz 10183922 SHA512:60ba33a35bf972209a43eaeb018d7195edb633e119002bb1f1c949582b647e34d523d6d8166aaa305bda7c65b6c0e423324ab80e71d70544a30d72e78a7a5e2a
```

### `dpkg` source package: `lsb=11.1.0ubuntu2`

Binary Packages:

- `lsb-base=11.1.0ubuntu2`
- `lsb-release=11.1.0ubuntu2`

Licenses: (parsed from: `/usr/share/doc/lsb-base/copyright`, `/usr/share/doc/lsb-release/copyright`)

- `BSD-3-clause`
- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris lsb=11.1.0ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/l/lsb/lsb_11.1.0ubuntu2.dsc' lsb_11.1.0ubuntu2.dsc 2230 SHA256:983ff4ab1ab2b39af974e4b8f4373ab4028d0ee5a409e7cd40401fa8e6ecabde
'http://archive.ubuntu.com/ubuntu/pool/main/l/lsb/lsb_11.1.0ubuntu2.tar.xz' lsb_11.1.0ubuntu2.tar.xz 46024 SHA256:c6ab63b6702dc633988690aacde8ece3e460f8acd8f1af8e6a67ab2fe0798f41
```

### `dpkg` source package: `lxml=4.5.0-1ubuntu0.5`

Binary Packages:

- `python3-lxml:amd64=4.5.0-1ubuntu0.5`

Licenses: (parsed from: `/usr/share/doc/python3-lxml/copyright`)

- `GPL`
- `GPL2`
- `later`

Source:

```console
$ apt-get source -qq --print-uris lxml=4.5.0-1ubuntu0.5
'http://archive.ubuntu.com/ubuntu/pool/main/l/lxml/lxml_4.5.0-1ubuntu0.5.dsc' lxml_4.5.0-1ubuntu0.5.dsc 2355 SHA512:2174114c7e3762caed8c869f430f8e77b35c5325c30a809df7ae6e3f0360f57e3bfcf03f4fce3935409a2a7f0840cba166c974def7d56be98ff92a5e28203d57
'http://archive.ubuntu.com/ubuntu/pool/main/l/lxml/lxml_4.5.0.orig.tar.gz' lxml_4.5.0.orig.tar.gz 4531832 SHA512:7cb957b2ab9931c32984ad0808f51e650e82e2d9b14df3fd8df2dd8f2c5c261d26ebf2c672b723e89b00b867a0a8dbb9130023e48a5f302fd02d5409e1c8cd6c
'http://archive.ubuntu.com/ubuntu/pool/main/l/lxml/lxml_4.5.0-1ubuntu0.5.debian.tar.xz' lxml_4.5.0-1ubuntu0.5.debian.tar.xz 11628 SHA512:8c760c48ade6ca6ae980665273b98af3c2050c9f579e22777b8c56b9da1d8c91c7f8d663c06b26af4ed26b86122d0e49fbbe16189ddbd711d4374cd501224107
```

### `dpkg` source package: `lz4=1.9.2-2ubuntu0.20.04.1`

Binary Packages:

- `liblz4-1:amd64=1.9.2-2ubuntu0.20.04.1`

Licenses: (parsed from: `/usr/share/doc/liblz4-1/copyright`)

- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris lz4=1.9.2-2ubuntu0.20.04.1
'http://archive.ubuntu.com/ubuntu/pool/main/l/lz4/lz4_1.9.2-2ubuntu0.20.04.1.dsc' lz4_1.9.2-2ubuntu0.20.04.1.dsc 2095 SHA512:249c1370a5e277575429a778fe2be185a997eb82eb77e88f83da38ddb271956ff1d2ae96403c599d430ed13a0f37e125b4410d21e3d42fe2d47a1a376bff70ad
'http://archive.ubuntu.com/ubuntu/pool/main/l/lz4/lz4_1.9.2.orig.tar.gz' lz4_1.9.2.orig.tar.gz 305796 SHA512:ae714c61ec8e33ed91359b63f2896cfa102d66b730dce112b74696ec5850e59d88bd5527173e01e354a70fbe8f036557a47c767ee0766bc5f9c257978116c3c1
'http://archive.ubuntu.com/ubuntu/pool/main/l/lz4/lz4_1.9.2-2ubuntu0.20.04.1.debian.tar.xz' lz4_1.9.2-2ubuntu0.20.04.1.debian.tar.xz 13228 SHA512:330f522c3afd0c9a36c6d8b882cfd59aa32258906ad6bbcab3a5bcd4a530ce226905d8108f384615dedd749dc5faaa45f320b0eda98effabee433e97124fabc0
```

### `dpkg` source package: `make-dfsg=4.2.1-1.2`

Binary Packages:

- `make=4.2.1-1.2`

Licenses: (parsed from: `/usr/share/doc/make/copyright`)

- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris make-dfsg=4.2.1-1.2
'http://archive.ubuntu.com/ubuntu/pool/main/m/make-dfsg/make-dfsg_4.2.1-1.2.dsc' make-dfsg_4.2.1-1.2.dsc 2019 SHA256:0c8a2da5d51e03bf43e2929322d5a8406f08e5ee2d81a71ed6e5a8734f1b05cb
'http://archive.ubuntu.com/ubuntu/pool/main/m/make-dfsg/make-dfsg_4.2.1.orig.tar.gz' make-dfsg_4.2.1.orig.tar.gz 1485018 SHA256:480405e8995796ea47cc54b281b7855280f0d815d296a1af1993eeeb72074e39
'http://archive.ubuntu.com/ubuntu/pool/main/m/make-dfsg/make-dfsg_4.2.1-1.2.diff.gz' make-dfsg_4.2.1-1.2.diff.gz 53108 SHA256:80e0b96cee381391a5d3322317075e23d8474c92c5fa4fecd334bc2e0920887b
```

### `dpkg` source package: `mawk=1.3.4.20200120-2`

Binary Packages:

- `mawk=1.3.4.20200120-2`

Licenses: (parsed from: `/usr/share/doc/mawk/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris mawk=1.3.4.20200120-2
'http://archive.ubuntu.com/ubuntu/pool/main/m/mawk/mawk_1.3.4.20200120-2.dsc' mawk_1.3.4.20200120-2.dsc 1915 SHA256:5069c46872ac74f5221250dfb88b31b1f2dbb8a2617c1e013f8f80cc34638c6d
'http://archive.ubuntu.com/ubuntu/pool/main/m/mawk/mawk_1.3.4.20200120.orig.tar.gz' mawk_1.3.4.20200120.orig.tar.gz 468855 SHA256:7fd4cd1e1fae9290fe089171181bbc6291dfd9bca939ca804f0ddb851c8b8237
'http://archive.ubuntu.com/ubuntu/pool/main/m/mawk/mawk_1.3.4.20200120-2.debian.tar.xz' mawk_1.3.4.20200120-2.debian.tar.xz 7504 SHA256:b772ed2f016b0286980c46cbc1f1f4ae62887ef2aa3dff6ef10cae638f923f26
```

### `dpkg` source package: `mime-support=3.64ubuntu1`

Binary Packages:

- `mime-support=3.64ubuntu1`

Licenses: (parsed from: `/usr/share/doc/mime-support/copyright`)

- `Bellcore`
- `ad-hoc`

Source:

```console
$ apt-get source -qq --print-uris mime-support=3.64ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/m/mime-support/mime-support_3.64ubuntu1.dsc' mime-support_3.64ubuntu1.dsc 1729 SHA256:669ba4f3fd7594f1c32731b5636b499f44f21c7667148f6f0d16043708743fdc
'http://archive.ubuntu.com/ubuntu/pool/main/m/mime-support/mime-support_3.64ubuntu1.tar.xz' mime-support_3.64ubuntu1.tar.xz 33980 SHA256:5007d2ebc25935bfca6d4bdac0efdfc089a38c1be49d19f0422559f666e4f2c4
```

### `dpkg` source package: `more-itertools=4.2.0-1build1`

Binary Packages:

- `python3-more-itertools=4.2.0-1build1`

Licenses: (parsed from: `/usr/share/doc/python3-more-itertools/copyright`)

- `MIT-style`

Source:

```console
$ apt-get source -qq --print-uris more-itertools=4.2.0-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/m/more-itertools/more-itertools_4.2.0-1build1.dsc' more-itertools_4.2.0-1build1.dsc 2575 SHA256:9d1d9da8eccd7d1ab3308d0e1e45815119ced3b0e10b6720e944f48971d15669
'http://archive.ubuntu.com/ubuntu/pool/main/m/more-itertools/more-itertools_4.2.0.orig.tar.gz' more-itertools_4.2.0.orig.tar.gz 56871 SHA256:2b6b9893337bfd9166bee6a62c2b0c9fe7735dcf85948b387ec8cba30e85d8e8
'http://archive.ubuntu.com/ubuntu/pool/main/m/more-itertools/more-itertools_4.2.0-1build1.debian.tar.xz' more-itertools_4.2.0-1build1.debian.tar.xz 2732 SHA256:0802ec50fcdb7a1c579fd146f847d9835096005b96182752a829856e3bf3d50c
```

### `dpkg` source package: `mpclib3=1.1.0-1`

Binary Packages:

- `libmpc3:amd64=1.1.0-1`

Licenses: (parsed from: `/usr/share/doc/libmpc3/copyright`)

- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris mpclib3=1.1.0-1
'http://archive.ubuntu.com/ubuntu/pool/main/m/mpclib3/mpclib3_1.1.0-1.dsc' mpclib3_1.1.0-1.dsc 1990 SHA256:bb57824015b735bf72399a53f8c6a241e6a8bd402753b0fdcdaa5b99d0aef790
'http://archive.ubuntu.com/ubuntu/pool/main/m/mpclib3/mpclib3_1.1.0.orig.tar.gz' mpclib3_1.1.0.orig.tar.gz 701263 SHA256:6985c538143c1208dcb1ac42cedad6ff52e267b47e5f970183a3e75125b43c2e
'http://archive.ubuntu.com/ubuntu/pool/main/m/mpclib3/mpclib3_1.1.0-1.diff.gz' mpclib3_1.1.0-1.diff.gz 3794 SHA256:84b10a4ae958b3015e136b75be5fee22961255d19be655f7d0adae8d4f3bc977
```

### `dpkg` source package: `mpdecimal=2.4.2-3`

Binary Packages:

- `libmpdec2:amd64=2.4.2-3`

Licenses: (parsed from: `/usr/share/doc/libmpdec2/copyright`)

- `BSD`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris mpdecimal=2.4.2-3
'http://archive.ubuntu.com/ubuntu/pool/main/m/mpdecimal/mpdecimal_2.4.2-3.dsc' mpdecimal_2.4.2-3.dsc 1932 SHA256:4cdd04de9915af3c9d787f4922affc1993d76c25cd0715ffdd2658da37c86753
'http://archive.ubuntu.com/ubuntu/pool/main/m/mpdecimal/mpdecimal_2.4.2.orig.tar.gz' mpdecimal_2.4.2.orig.tar.gz 2271529 SHA256:83c628b90f009470981cf084c5418329c88b19835d8af3691b930afccb7d79c7
'http://archive.ubuntu.com/ubuntu/pool/main/m/mpdecimal/mpdecimal_2.4.2-3.debian.tar.xz' mpdecimal_2.4.2-3.debian.tar.xz 6352 SHA256:1baf12776a911bc77f76e16aa7600d4ace21a27817f4a56373093065205a9292
```

### `dpkg` source package: `mpfr4=4.0.2-1`

Binary Packages:

- `libmpfr6:amd64=4.0.2-1`

Licenses: (parsed from: `/usr/share/doc/libmpfr6/copyright`)

- `GFDL-1.2`
- `LGPL-3`

Source:

```console
$ apt-get source -qq --print-uris mpfr4=4.0.2-1
'http://archive.ubuntu.com/ubuntu/pool/main/m/mpfr4/mpfr4_4.0.2-1.dsc' mpfr4_4.0.2-1.dsc 1972 SHA256:9021ec2462ed0e73ea1379266740473abf5f826be819226497729f6c6b02e672
'http://archive.ubuntu.com/ubuntu/pool/main/m/mpfr4/mpfr4_4.0.2.orig.tar.xz' mpfr4_4.0.2.orig.tar.xz 1441996 SHA256:1d3be708604eae0e42d578ba93b390c2a145f17743a744d8f3f8c2ad5855a38a
'http://archive.ubuntu.com/ubuntu/pool/main/m/mpfr4/mpfr4_4.0.2-1.debian.tar.xz' mpfr4_4.0.2-1.debian.tar.xz 10544 SHA256:99c4d35654f33340f0efdec67142a34753157b20334cadad9018f5eab29738da
```

### `dpkg` source package: `ncurses=6.2-0ubuntu2.1`

Binary Packages:

- `libncurses6:amd64=6.2-0ubuntu2.1`
- `libncursesw6:amd64=6.2-0ubuntu2.1`
- `libtinfo6:amd64=6.2-0ubuntu2.1`
- `ncurses-base=6.2-0ubuntu2.1`
- `ncurses-bin=6.2-0ubuntu2.1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris ncurses=6.2-0ubuntu2.1
'http://archive.ubuntu.com/ubuntu/pool/main/n/ncurses/ncurses_6.2-0ubuntu2.1.dsc' ncurses_6.2-0ubuntu2.1.dsc 3597 SHA512:24d67535dba8750018bbfd33347fc8e702e1e47ef7cc80a452acb5dc8031a13c7a05a000e1b7b5f1a43e9a4c370e881ebf75124bfbe181c18370f56284371f64
'http://archive.ubuntu.com/ubuntu/pool/main/n/ncurses/ncurses_6.2.orig.tar.gz' ncurses_6.2.orig.tar.gz 3425862 SHA512:4c1333dcc30e858e8a9525d4b9aefb60000cfc727bc4a1062bace06ffc4639ad9f6e54f6bdda0e3a0e5ea14de995f96b52b3327d9ec633608792c99a1e8d840d
'http://archive.ubuntu.com/ubuntu/pool/main/n/ncurses/ncurses_6.2-0ubuntu2.1.debian.tar.xz' ncurses_6.2-0ubuntu2.1.debian.tar.xz 63588 SHA512:c30de5afa3ca85e34d5834d71efb6a01453be1ca7f7356ea39b7475dd287c2800e4219d4f497efc49bf0553065f8d727028908f631f1b756d43b825d16c5a16c
```

### `dpkg` source package: `net-tools=1.60+git20180626.aebd88e-1ubuntu1.3`

Binary Packages:

- `net-tools=1.60+git20180626.aebd88e-1ubuntu1.3`

Licenses: (parsed from: `/usr/share/doc/net-tools/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris net-tools=1.60+git20180626.aebd88e-1ubuntu1.3
'http://archive.ubuntu.com/ubuntu/pool/main/n/net-tools/net-tools_1.60%2bgit20180626.aebd88e-1ubuntu1.3.dsc' net-tools_1.60+git20180626.aebd88e-1ubuntu1.3.dsc 2189 SHA512:87f96a61b691c257837cf5b65171f7852bdf641a17ce365b9f970a2a394f21c91b7c9fd8c5df30bb4b83e611253567f6e71ca22ac3443bd718ccae140991d3b5
'http://archive.ubuntu.com/ubuntu/pool/main/n/net-tools/net-tools_1.60%2bgit20180626.aebd88e.orig.tar.gz' net-tools_1.60+git20180626.aebd88e.orig.tar.gz 288458 SHA512:7e2b0af97d1167b92ddf4caa7aa75f3407afe8ad65ca535632f5a083c558abffd1cee2cf288dbd10d671df0925bb4f873e19370c5c6af1f1ea5236f9bec479a8
'http://archive.ubuntu.com/ubuntu/pool/main/n/net-tools/net-tools_1.60%2bgit20180626.aebd88e-1ubuntu1.3.debian.tar.xz' net-tools_1.60+git20180626.aebd88e-1ubuntu1.3.debian.tar.xz 60148 SHA512:02d6c4f287f8fbdcbe35b5fa6ceca2f1c727952a0738d44e93d030877051d94d9a72070a8fb37035fda2d7318e5b6a4ea03307a5315a9a114baeada102560cd6
```

### `dpkg` source package: `netifaces=0.10.4-1ubuntu4`

Binary Packages:

- `python3-netifaces=0.10.4-1ubuntu4`

Licenses: (parsed from: `/usr/share/doc/python3-netifaces/copyright`)

- `MIT-style`

Source:

```console
$ apt-get source -qq --print-uris netifaces=0.10.4-1ubuntu4
'http://archive.ubuntu.com/ubuntu/pool/main/n/netifaces/netifaces_0.10.4-1ubuntu4.dsc' netifaces_0.10.4-1ubuntu4.dsc 2399 SHA256:dd7c2e32b8139501ba16aa17000358b0ed8f0c6b44d4f5ed0372a891a0320c25
'http://archive.ubuntu.com/ubuntu/pool/main/n/netifaces/netifaces_0.10.4.orig.tar.gz' netifaces_0.10.4.orig.tar.gz 22969 SHA256:9656a169cb83da34d732b0eb72b39373d48774aee009a3d1272b7ea2ce109cde
'http://archive.ubuntu.com/ubuntu/pool/main/n/netifaces/netifaces_0.10.4-1ubuntu4.debian.tar.xz' netifaces_0.10.4-1ubuntu4.debian.tar.xz 8596 SHA256:dffdb241c6c83c52fa2a975fc6291d5b004e2ae0b71d2b9daaeb704e3552951b
```

### `dpkg` source package: `nettle=3.5.1+really3.5.1-2ubuntu0.2`

Binary Packages:

- `libhogweed5:amd64=3.5.1+really3.5.1-2ubuntu0.2`
- `libnettle7:amd64=3.5.1+really3.5.1-2ubuntu0.2`

Licenses: (parsed from: `/usr/share/doc/libhogweed5/copyright`, `/usr/share/doc/libnettle7/copyright`)

- `GAP`
- `GPL`
- `GPL-2`
- `GPL-2+`
- `GPL-2+ with Autoconf exception`
- `LGPL`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1+`
- `other`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris nettle=3.5.1+really3.5.1-2ubuntu0.2
'http://archive.ubuntu.com/ubuntu/pool/main/n/nettle/nettle_3.5.1%2breally3.5.1-2ubuntu0.2.dsc' nettle_3.5.1+really3.5.1-2ubuntu0.2.dsc 2490 SHA512:a5b45f1154e48fd7d6c48c57ae17cdcb7cd4a352d6b97bb408a49f5f4f3b40388d23bc12b09602fc9d0d6e91e8bc5525b12f98568ec64c18c4d6ca9fe5048c36
'http://archive.ubuntu.com/ubuntu/pool/main/n/nettle/nettle_3.5.1%2breally3.5.1.orig.tar.gz' nettle_3.5.1+really3.5.1.orig.tar.gz 1989593 SHA512:f738121b9091cbe79435fb5d46b45cf6f10912320c233829356908127bab1cac6946ca56e022a832380c44f2c10f21d2feef64cb0f4f41e3da4a681dc0131784
'http://archive.ubuntu.com/ubuntu/pool/main/n/nettle/nettle_3.5.1%2breally3.5.1.orig.tar.gz.asc' nettle_3.5.1+really3.5.1.orig.tar.gz.asc 573 SHA512:d8921622f2165fb4a05e7e75f75d82c0eabb816f265bae3f3267def20d81386b1da1a29ebfc52bbe26875b94b2050dd5493119d0efcb5143bc21e2f69b8449dd
'http://archive.ubuntu.com/ubuntu/pool/main/n/nettle/nettle_3.5.1%2breally3.5.1-2ubuntu0.2.debian.tar.xz' nettle_3.5.1+really3.5.1-2ubuntu0.2.debian.tar.xz 27228 SHA512:389c303e679b6b6714f824f22bc8675c1ea4bdab0108b69e9514613109573d01592e3f80bf9a144866a159a9a09fa0f3218d62b9f6978bdfe5e95a18bcfe3a88
```

### `dpkg` source package: `nghttp2=1.40.0-1ubuntu0.3`

Binary Packages:

- `libnghttp2-14:amd64=1.40.0-1ubuntu0.3`

Licenses: (parsed from: `/usr/share/doc/libnghttp2-14/copyright`)

- `BSD-2-clause`
- `Expat`
- `GPL-3`
- `GPL-3+ with autoconf exception`
- `MIT`
- `SIL-OFL-1.1`
- `all-permissive`

Source:

```console
$ apt-get source -qq --print-uris nghttp2=1.40.0-1ubuntu0.3
'http://archive.ubuntu.com/ubuntu/pool/main/n/nghttp2/nghttp2_1.40.0-1ubuntu0.3.dsc' nghttp2_1.40.0-1ubuntu0.3.dsc 2679 SHA512:23dc554f410fa4a99a06515040490c3e2cf1200dc0ccea05499ff10eecf5434899732b6f9344a6090e7c48b0b29771acb63745b44e11a76def1e2cc2c939efc0
'http://archive.ubuntu.com/ubuntu/pool/main/n/nghttp2/nghttp2_1.40.0.orig.tar.bz2' nghttp2_1.40.0.orig.tar.bz2 1937537 SHA512:bc3f6dd8ccc3c6891b61206eeb2a74019b2559b4d75409e022c1a9ad0745d50cf8db7ca8e076993ab04a17f87455dc38159bf085bd844366dac82506e44656a0
'http://archive.ubuntu.com/ubuntu/pool/main/n/nghttp2/nghttp2_1.40.0-1ubuntu0.3.debian.tar.xz' nghttp2_1.40.0-1ubuntu0.3.debian.tar.xz 22112 SHA512:d7c1a1efdf9e7413475ba156b3ed21bf931bd494a1a404003a31ddd104ad403d9935b7655c8d650ff2ce67e4d8b6598ab9f8e757993d72dd6dbd776bac40d9af
```

### `dpkg` source package: `npth=1.6-1`

Binary Packages:

- `libnpth0:amd64=1.6-1`

Licenses: (parsed from: `/usr/share/doc/libnpth0/copyright`)

- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris npth=1.6-1
'http://archive.ubuntu.com/ubuntu/pool/main/n/npth/npth_1.6-1.dsc' npth_1.6-1.dsc 1925 SHA256:2c327ce494f702482e79ed620445cba303c4449dd0768fecee3ee7d5ade2544a
'http://archive.ubuntu.com/ubuntu/pool/main/n/npth/npth_1.6.orig.tar.bz2' npth_1.6.orig.tar.bz2 300486 SHA256:1393abd9adcf0762d34798dc34fdcf4d0d22a8410721e76f1e3afcd1daa4e2d1
'http://archive.ubuntu.com/ubuntu/pool/main/n/npth/npth_1.6-1.debian.tar.xz' npth_1.6-1.debian.tar.xz 10532 SHA256:d312d4a3cf1d082e2f2cf3ea752c41d34f7e120f77a941c6c1680e6093834353
```

### `dpkg` source package: `numpy=1:1.17.4-5ubuntu3.1`

Binary Packages:

- `python3-numpy=1:1.17.4-5ubuntu3.1`

Licenses: (parsed from: `/usr/share/doc/python3-numpy/copyright`)

- `BSD-3-Clause`
- `MIT`
- `PSF`
- `Public-Domain`

Source:

```console
$ apt-get source -qq --print-uris numpy=1:1.17.4-5ubuntu3.1
'http://archive.ubuntu.com/ubuntu/pool/main/n/numpy/numpy_1.17.4-5ubuntu3.1.dsc' numpy_1.17.4-5ubuntu3.1.dsc 2639 SHA512:b836f1f1e5e77ec1084aa02dcc44361ceff54cec3ca96be71828841409da89ad84d1f562f1d4f2a4365114fc625deafed7bf89dbd2536f95536319eb72650278
'http://archive.ubuntu.com/ubuntu/pool/main/n/numpy/numpy_1.17.4.orig.tar.xz' numpy_1.17.4.orig.tar.xz 3519384 SHA512:b103a713b30964d9196ee0aed13957bdddffa326abf6b923e565fd339322445df8c12de277ad95d81e861b30da8d5b16a6501d4af3cb7867caccc963c601b5fe
'http://archive.ubuntu.com/ubuntu/pool/main/n/numpy/numpy_1.17.4-5ubuntu3.1.debian.tar.xz' numpy_1.17.4-5ubuntu3.1.debian.tar.xz 35556 SHA512:b11df8c8d850a89b5bccfe8ca458ea9ab8b05ea258b0fbc4cc46a876b561007d30defd865fd10fcff080a1f2be15f19483f9dcf40483c1871384d76e10a0c041
```

### `dpkg` source package: `openldap=2.4.49+dfsg-2ubuntu1.10`

Binary Packages:

- `libldap-2.4-2:amd64=2.4.49+dfsg-2ubuntu1.10`
- `libldap-common=2.4.49+dfsg-2ubuntu1.10`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris openldap=2.4.49+dfsg-2ubuntu1.10
'http://archive.ubuntu.com/ubuntu/pool/main/o/openldap/openldap_2.4.49%2bdfsg-2ubuntu1.10.dsc' openldap_2.4.49+dfsg-2ubuntu1.10.dsc 3140 SHA512:091caf80949f3c45dd7eb17b0a94b7315c5964673590bcce5f4cc7a916054db73bd29eade6513bfee9dc9972d32aa214731e935a5a18a857f3971198d5878545
'http://archive.ubuntu.com/ubuntu/pool/main/o/openldap/openldap_2.4.49%2bdfsg.orig.tar.gz' openldap_2.4.49+dfsg.orig.tar.gz 4844726 SHA512:c2096f6e37bae8e4d4dcc5cc8dad783996bc8677e7e62a06b9f55857f8950726ca3e3b0d8368563c8985123175f63625354ad5ac271db8b55d3ac62e8906d4c7
'http://archive.ubuntu.com/ubuntu/pool/main/o/openldap/openldap_2.4.49%2bdfsg-2ubuntu1.10.debian.tar.xz' openldap_2.4.49+dfsg-2ubuntu1.10.debian.tar.xz 190520 SHA512:6782b86834c3643acd64ecf68643af47e030fded12ed90bf84c40072c63bdcd01ada54bdf0eb8ef54123c70d5b96dd447b498ed1a0e0c88efcd56126e2c9e646
```

### `dpkg` source package: `openssl=1.1.1f-1ubuntu2.24`

Binary Packages:

- `libssl-dev:amd64=1.1.1f-1ubuntu2.24`
- `libssl1.1:amd64=1.1.1f-1ubuntu2.24`
- `openssl=1.1.1f-1ubuntu2.24`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris openssl=1.1.1f-1ubuntu2.24
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssl/openssl_1.1.1f-1ubuntu2.24.dsc' openssl_1.1.1f-1ubuntu2.24.dsc 2470 SHA512:11ef114406e89c74d0a402e42f639fc4e4441d66df7f13ad7abefc9aa5b7e8fa4cf0337b679c2f23876edc78e222e927bcdbf58ae6ee5f856ad9d6970fcbde04
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssl/openssl_1.1.1f.orig.tar.gz' openssl_1.1.1f.orig.tar.gz 9792828 SHA512:b00bd9b5ad5298fbceeec6bb19c1ab0c106ca5cfb31178497c58bf7e0e0cf30fcc19c20f84e23af31cc126bf2447d3e4f8461db97bafa7bd78f69561932f000c
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssl/openssl_1.1.1f-1ubuntu2.24.debian.tar.xz' openssl_1.1.1f-1ubuntu2.24.debian.tar.xz 266728 SHA512:d397e9d44c8279700109eb5367e12ed547f18ad904f087fc17a82d5776f708636db5a3f51dc5b7fef86a126df02a78849ad2edf57b57cf400c31374a975f040b
```

### `dpkg` source package: `p11-kit=0.23.20-1ubuntu0.1`

Binary Packages:

- `libp11-kit0:amd64=0.23.20-1ubuntu0.1`

Licenses: (parsed from: `/usr/share/doc/libp11-kit0/copyright`)

- `BSD-3-Clause`
- `ISC`
- `ISC+IBM`
- `permissive-like-automake-output`
- `same-as-rest-of-p11kit`

Source:

```console
$ apt-get source -qq --print-uris p11-kit=0.23.20-1ubuntu0.1
'http://archive.ubuntu.com/ubuntu/pool/main/p/p11-kit/p11-kit_0.23.20-1ubuntu0.1.dsc' p11-kit_0.23.20-1ubuntu0.1.dsc 2532 SHA512:8b315f15df7cd3a09d11046030baa864a0f61a3dfba80d97d708590f54a5fc5c31c81428ccc40bf04e9e769abda1204ef5cd4753a24e743e2728d38cdfe14803
'http://archive.ubuntu.com/ubuntu/pool/main/p/p11-kit/p11-kit_0.23.20.orig.tar.xz' p11-kit_0.23.20.orig.tar.xz 822588 SHA512:1eb88773fdd49dd48c7e089744e9dbbf6c1033a4863f3bfe75a68d842804baa3c373cb1b28ee625dd69a6e16c89df4ac755e0928495dccf38c007c530f6cfa57
'http://archive.ubuntu.com/ubuntu/pool/main/p/p11-kit/p11-kit_0.23.20.orig.tar.xz.asc' p11-kit_0.23.20.orig.tar.xz.asc 854 SHA512:9f0e0e690698637269b7d020aafd92ab3d487770196e13357ce0e5425fa02d5e279f9524b3858bce8bdb925e1e4d9fa2219a68e5888c06e48c3b085a77d329e9
'http://archive.ubuntu.com/ubuntu/pool/main/p/p11-kit/p11-kit_0.23.20-1ubuntu0.1.debian.tar.xz' p11-kit_0.23.20-1ubuntu0.1.debian.tar.xz 24592 SHA512:b30c6640bb02f0651955447da65911942cd2e302bc5af0ab96787646e776486e317420682dd644079a47ac48d4e2732218545af56da7ec3d3af5fd0c7e55fb21
```

### `dpkg` source package: `pam=1.3.1-5ubuntu4.7`

Binary Packages:

- `libpam-modules:amd64=1.3.1-5ubuntu4.7`
- `libpam-modules-bin=1.3.1-5ubuntu4.7`
- `libpam-runtime=1.3.1-5ubuntu4.7`
- `libpam0g:amd64=1.3.1-5ubuntu4.7`

Licenses: (parsed from: `/usr/share/doc/libpam-modules/copyright`, `/usr/share/doc/libpam-modules-bin/copyright`, `/usr/share/doc/libpam-runtime/copyright`, `/usr/share/doc/libpam0g/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris pam=1.3.1-5ubuntu4.7
'http://archive.ubuntu.com/ubuntu/pool/main/p/pam/pam_1.3.1-5ubuntu4.7.dsc' pam_1.3.1-5ubuntu4.7.dsc 2724 SHA512:8a5b76e1928b1a568358349807188e5f367790531087a1116a10071ac11daaa25aa73ea95cf1d9197c7052fbbf993122ac9f257270b1b70dc98be29d1a989a81
'http://archive.ubuntu.com/ubuntu/pool/main/p/pam/pam_1.3.1.orig.tar.xz' pam_1.3.1.orig.tar.xz 912332 SHA512:6bc8e2a5b64686f0a23846221c5228c88418ba485b17c53b3a12f91262b5bb73566d6b6a5daa1f63bbae54310aee918b987e44a72ce809b4e7c668f0fadfe08e
'http://archive.ubuntu.com/ubuntu/pool/main/p/pam/pam_1.3.1-5ubuntu4.7.debian.tar.xz' pam_1.3.1-5ubuntu4.7.debian.tar.xz 172868 SHA512:85b8c3aadb9f2d88a887b7e91f73a533a55ab2a78a0c1999b1928c3e0a3601e5a5249d0b248d7a69734fb22bb9fc270a34370279466f65efc32af2c2425abb23
```

### `dpkg` source package: `pango1.0=1.44.7-2ubuntu4`

Binary Packages:

- `libpango-1.0-0:amd64=1.44.7-2ubuntu4`
- `libpangocairo-1.0-0:amd64=1.44.7-2ubuntu4`
- `libpangoft2-1.0-0:amd64=1.44.7-2ubuntu4`

Licenses: (parsed from: `/usr/share/doc/libpango-1.0-0/copyright`, `/usr/share/doc/libpangocairo-1.0-0/copyright`, `/usr/share/doc/libpangoft2-1.0-0/copyright`)

- `Chromium-BSD-style`
- `Example`
- `ICU`
- `LGPL-2`
- `LGPL-2+`
- `TCL`
- `Unicode`

Source:

```console
$ apt-get source -qq --print-uris pango1.0=1.44.7-2ubuntu4
'http://archive.ubuntu.com/ubuntu/pool/main/p/pango1.0/pango1.0_1.44.7-2ubuntu4.dsc' pango1.0_1.44.7-2ubuntu4.dsc 2915 SHA256:e7d7027628a38d12ee9e6f29f4f6d275757d9b1fdc9e55948194f233c55251fc
'http://archive.ubuntu.com/ubuntu/pool/main/p/pango1.0/pango1.0_1.44.7.orig.tar.xz' pango1.0_1.44.7.orig.tar.xz 521384 SHA256:66a5b6cc13db73efed67b8e933584509f8ddb7b10a8a40c3850ca4a985ea1b1f
'http://archive.ubuntu.com/ubuntu/pool/main/p/pango1.0/pango1.0_1.44.7-2ubuntu4.debian.tar.xz' pango1.0_1.44.7-2ubuntu4.debian.tar.xz 33516 SHA256:6f5f8c66299af90a94c4dbdfa146e840eec8bc2d183cd1fb42e8e7de6f335df5
```

### `dpkg` source package: `patch=2.7.6-6`

Binary Packages:

- `patch=2.7.6-6`

Licenses: (parsed from: `/usr/share/doc/patch/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris patch=2.7.6-6
'http://archive.ubuntu.com/ubuntu/pool/main/p/patch/patch_2.7.6-6.dsc' patch_2.7.6-6.dsc 1699 SHA256:ad31c243b982ad8dede14f7b4dfe5bb798bb1dc6d4e28c51a797c3af58477c13
'http://archive.ubuntu.com/ubuntu/pool/main/p/patch/patch_2.7.6.orig.tar.xz' patch_2.7.6.orig.tar.xz 783756 SHA256:ac610bda97abe0d9f6b7c963255a11dcb196c25e337c61f94e4778d632f1d8fd
'http://archive.ubuntu.com/ubuntu/pool/main/p/patch/patch_2.7.6-6.debian.tar.xz' patch_2.7.6-6.debian.tar.xz 14464 SHA256:75ea94b265763b65005381f1eceeaf3351a70ec5c3243bc161d702776414db02
```

### `dpkg` source package: `pcre2=10.34-7ubuntu0.1`

Binary Packages:

- `libpcre2-8-0:amd64=10.34-7ubuntu0.1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris pcre2=10.34-7ubuntu0.1
'http://archive.ubuntu.com/ubuntu/pool/main/p/pcre2/pcre2_10.34-7ubuntu0.1.dsc' pcre2_10.34-7ubuntu0.1.dsc 2142 SHA512:f37aadf191246ca9e4605a57e9a15e3bac768649c19970259b03b5792b52ca848206866be5b5b79fec659c6b2defa50dd263d2e0ff41d706e613c707cb5540fc
'http://archive.ubuntu.com/ubuntu/pool/main/p/pcre2/pcre2_10.34.orig.tar.gz' pcre2_10.34.orig.tar.gz 2271533 SHA512:820b3805fc7fcf3a80dfd42ff570efc8518fe3c50f3feb720319b95316619e5b8f6601b3c9522606315aecd5558ccfc8a04a89fab9921fdfc3400dc2caf17c22
'http://archive.ubuntu.com/ubuntu/pool/main/p/pcre2/pcre2_10.34-7ubuntu0.1.diff.gz' pcre2_10.34-7ubuntu0.1.diff.gz 10945 SHA512:92f25dddec9ca30dc7221ee09e5b401c59fbf86acd3612451f6c64e55f7a9f96fd9752ac7398f05aa59214d9649f63324ec0f6ede2f178653f361ae9adeb7e70
```

### `dpkg` source package: `pcre3=2:8.39-12ubuntu0.1`

Binary Packages:

- `libpcre3:amd64=2:8.39-12ubuntu0.1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris pcre3=2:8.39-12ubuntu0.1
'http://archive.ubuntu.com/ubuntu/pool/main/p/pcre3/pcre3_8.39-12ubuntu0.1.dsc' pcre3_8.39-12ubuntu0.1.dsc 2077 SHA512:8c8d2c065a5cfbc912747f44365b9d3c7dee77e2d5f1ff4049e1c505dfc792d2e44cf42dd108bb63fe23806d869927acfe52ae9e75160fbec9aa3ac6297ac8d1
'http://archive.ubuntu.com/ubuntu/pool/main/p/pcre3/pcre3_8.39.orig.tar.bz2' pcre3_8.39.orig.tar.bz2 1560758 SHA512:8b0f14ae5947c4b2d74876a795b04e532fd71c2479a64dbe0ed817e7c7894ea3cae533413de8c17322d305cb7f4e275d72b43e4e828eaca77dc4bcaf04529cf6
'http://archive.ubuntu.com/ubuntu/pool/main/p/pcre3/pcre3_8.39-12ubuntu0.1.debian.tar.gz' pcre3_8.39-12ubuntu0.1.debian.tar.gz 27476 SHA512:a6ca841c38badb86d9cf6170f24fe627688ebda39304f6adf6666c580fe64bb451c1ea4d3ed96d09b70d11a4c88cc05f38d45d72b985b3efaf1934d47acb0431
```

### `dpkg` source package: `perl=5.30.0-9ubuntu0.5`

Binary Packages:

- `libperl5.30:amd64=5.30.0-9ubuntu0.5`
- `perl=5.30.0-9ubuntu0.5`
- `perl-base=5.30.0-9ubuntu0.5`
- `perl-modules-5.30=5.30.0-9ubuntu0.5`

Licenses: (parsed from: `/usr/share/doc/libperl5.30/copyright`, `/usr/share/doc/perl/copyright`, `/usr/share/doc/perl-base/copyright`, `/usr/share/doc/perl-modules-5.30/copyright`)

- `Artistic`
- `Artistic,`
- `Artistic-2`
- `Artistic-dist`
- `BSD-3-clause`
- `BSD-3-clause-GENERIC`
- `BSD-3-clause-with-weird-numbering`
- `BSD-4-clause-POWERDOG`
- `BZIP`
- `CC0-1.0`
- `DONT-CHANGE-THE-GPL`
- `Expat`
- `GPL-1`
- `GPL-1+`
- `GPL-2`
- `GPL-2+`
- `GPL-3+-WITH-BISON-EXCEPTION`
- `HSIEH-BSD`
- `HSIEH-DERIVATIVE`
- `LGPL-2.1`
- `REGCOMP`
- `REGCOMP,`
- `RRA-KEEP-THIS-NOTICE`
- `SDBM-PUBLIC-DOMAIN`
- `TEXT-TABS`
- `Unicode`
- `ZLIB`

Source:

```console
$ apt-get source -qq --print-uris perl=5.30.0-9ubuntu0.5
'http://archive.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.30.0-9ubuntu0.5.dsc' perl_5.30.0-9ubuntu0.5.dsc 2962 SHA512:465120e571e4dc71b167a67cd945ba92476d3ce41fd8b39483e8058a6bddf534149d0fc1a0bfb0e6c83c5ec35b0720ab50ec035d3030978844b8965db9de5459
'http://archive.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.30.0.orig-regen-configure.tar.gz' perl_5.30.0.orig-regen-configure.tar.gz 833235 SHA512:ab977887b53249a2423708aa38ecbb8bdbfdb7ba533a795eaa20bac427b2eb326756b076ca11088036550a4db24418903c0565d168fe9641e18077a76d04274a
'http://archive.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.30.0.orig.tar.xz' perl_5.30.0.orig.tar.xz 12419868 SHA512:68a295eccd64debd9d6a10f0d5577f872a19ad8c2d702798f6b0f45b8c3af6ab3230768056e2131e9e2e2506d1035b27cfd627c845e32263fe448649c4b98ae9
'http://archive.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.30.0-9ubuntu0.5.debian.tar.xz' perl_5.30.0-9ubuntu0.5.debian.tar.xz 172444 SHA512:a7adf38eaa3c23d538c8c051ea0803a8c787e812d21e9d2a79b2e90475746699cc7dd4d4b914f2a79d7178db8fb9dd90b8e92d1c522b8db05467bbee9c8be678
```

### `dpkg` source package: `pinentry=1.1.0-3build1`

Binary Packages:

- `pinentry-curses=1.1.0-3build1`

Licenses: (parsed from: `/usr/share/doc/pinentry-curses/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-3`
- `LGPL-3+`
- `X11`

Source:

```console
$ apt-get source -qq --print-uris pinentry=1.1.0-3build1
'http://archive.ubuntu.com/ubuntu/pool/main/p/pinentry/pinentry_1.1.0-3build1.dsc' pinentry_1.1.0-3build1.dsc 2714 SHA256:69f7f343287886eebadb94177767d9aa74890d9f8420e3ab254803fcd21852bf
'http://archive.ubuntu.com/ubuntu/pool/main/p/pinentry/pinentry_1.1.0.orig.tar.bz2' pinentry_1.1.0.orig.tar.bz2 467702 SHA256:68076686fa724a290ea49cdf0d1c0c1500907d1b759a3bcbfbec0293e8f56570
'http://archive.ubuntu.com/ubuntu/pool/main/p/pinentry/pinentry_1.1.0-3build1.debian.tar.xz' pinentry_1.1.0-3build1.debian.tar.xz 17224 SHA256:2a11ee552389ba0499d6a9e1bfc38ee65a28bb97758832b982bbede68d2cb1b9
```

### `dpkg` source package: `pixman=0.38.4-0ubuntu2.1`

Binary Packages:

- `libpixman-1-0:amd64=0.38.4-0ubuntu2.1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris pixman=0.38.4-0ubuntu2.1
'http://archive.ubuntu.com/ubuntu/pool/main/p/pixman/pixman_0.38.4-0ubuntu2.1.dsc' pixman_0.38.4-0ubuntu2.1.dsc 2130 SHA512:9ec381b420c176be4e90baccddeff31e78bcfe97fa1f9008cac4eb7f93a2c3626ff25bf76765863dee92b48a8251b162d47b53b887d316b27617c246c1809c1d
'http://archive.ubuntu.com/ubuntu/pool/main/p/pixman/pixman_0.38.4.orig.tar.gz' pixman_0.38.4.orig.tar.gz 897926 SHA512:b66dc23c0bc7327cb90085cbc14ccf96ad58001a927f23af24e0258ca13f32d4255535862f1efcf00e9e723410aa9f51edf26fb01c8cde49379d1225acf7b5af
'http://archive.ubuntu.com/ubuntu/pool/main/p/pixman/pixman_0.38.4-0ubuntu2.1.diff.gz' pixman_0.38.4-0ubuntu2.1.diff.gz 320623 SHA512:457ad061efc8bb96fb74e0c3bd1cb811be2db56a315ed4634e8f94355a0ef0e96b42d32721c9778299960eca143c1165f52dbfd8fb25906e500eedd2267b8b89
```

### `dpkg` source package: `pkg-config=0.29.1-0ubuntu4`

Binary Packages:

- `pkg-config=0.29.1-0ubuntu4`

Licenses: (parsed from: `/usr/share/doc/pkg-config/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris pkg-config=0.29.1-0ubuntu4
'http://archive.ubuntu.com/ubuntu/pool/main/p/pkg-config/pkg-config_0.29.1-0ubuntu4.dsc' pkg-config_0.29.1-0ubuntu4.dsc 1799 SHA256:d60186d733ce808c04a0afeb4b6790161f4ffc5bae6a26a566eab047a31ef2dc
'http://archive.ubuntu.com/ubuntu/pool/main/p/pkg-config/pkg-config_0.29.1.orig.tar.gz' pkg-config_0.29.1.orig.tar.gz 2013454 SHA256:beb43c9e064555469bd4390dcfd8030b1536e0aa103f08d7abf7ae8cac0cb001
'http://archive.ubuntu.com/ubuntu/pool/main/p/pkg-config/pkg-config_0.29.1-0ubuntu4.diff.gz' pkg-config_0.29.1-0ubuntu4.diff.gz 9373 SHA256:ac6d503134b8fbaca066aa3dea622c69a58e8845896ffd75066d14de27a41d58
```

### `dpkg` source package: `procps=2:3.3.16-1ubuntu2.4`

Binary Packages:

- `libprocps8:amd64=2:3.3.16-1ubuntu2.4`
- `procps=2:3.3.16-1ubuntu2.4`

Licenses: (parsed from: `/usr/share/doc/libprocps8/copyright`, `/usr/share/doc/procps/copyright`)

- `GPL-2`
- `GPL-2.0+`
- `LGPL-2`
- `LGPL-2.0+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris procps=2:3.3.16-1ubuntu2.4
'http://archive.ubuntu.com/ubuntu/pool/main/p/procps/procps_3.3.16-1ubuntu2.4.dsc' procps_3.3.16-1ubuntu2.4.dsc 2108 SHA512:334d57eaf7ff4792b1222cc7bdb4230dc41aafad26f9320461b9bea42e025e4531fcd2f5cdfdffad7c42cbab2467dbca08fa73b8760cce77eb8f2d3902a1afc1
'http://archive.ubuntu.com/ubuntu/pool/main/p/procps/procps_3.3.16.orig.tar.xz' procps_3.3.16.orig.tar.xz 621892 SHA512:38db4f72fe40c2f027b23b18bbc8c29cfcdf6bcdb029199fe4bebede153943aa884157f56e792c399f9a4949cc514687500bb99a75a5e7ad7b9e878f52090304
'http://archive.ubuntu.com/ubuntu/pool/main/p/procps/procps_3.3.16-1ubuntu2.4.debian.tar.xz' procps_3.3.16-1ubuntu2.4.debian.tar.xz 35232 SHA512:cb4310496951e74a13ec439dbff8c655d0fdcd82bb96d58c0954002d24ed474bf028f4ff6606274ab301de2184b441517809019776b497415487020ebaa05d0f
```

### `dpkg` source package: `pycodestyle=2.5.0-2`

Binary Packages:

- `python3-pycodestyle=2.5.0-2`

Licenses: (parsed from: `/usr/share/doc/python3-pycodestyle/copyright`)

- `Expat`

Source:

```console
$ apt-get source -qq --print-uris pycodestyle=2.5.0-2
'http://archive.ubuntu.com/ubuntu/pool/universe/p/pycodestyle/pycodestyle_2.5.0-2.dsc' pycodestyle_2.5.0-2.dsc 2206 SHA256:9a2d0dbc3e871b5cf683cbf93866e9a9cdd8d98f5ea4cb9c4bfb13132f475efc
'http://archive.ubuntu.com/ubuntu/pool/universe/p/pycodestyle/pycodestyle_2.5.0.orig.tar.gz' pycodestyle_2.5.0.orig.tar.gz 98802 SHA256:e40a936c9a450ad81df37f549d676d127b1b66000a6c500caa2b085bc0ca976c
'http://archive.ubuntu.com/ubuntu/pool/universe/p/pycodestyle/pycodestyle_2.5.0-2.debian.tar.xz' pycodestyle_2.5.0-2.debian.tar.xz 4104 SHA256:96c91a5ef53df2e5efe545bcf54c26b4c3cfaa594f2c4f58e2020b5008f76763
```

### `dpkg` source package: `pydocstyle=2.1.1-1`

Binary Packages:

- `pydocstyle=2.1.1-1`
- `python3-pydocstyle=2.1.1-1`

Licenses: (parsed from: `/usr/share/doc/pydocstyle/copyright`, `/usr/share/doc/python3-pydocstyle/copyright`)

- `Expat`

Source:

```console
$ apt-get source -qq --print-uris pydocstyle=2.1.1-1
'http://archive.ubuntu.com/ubuntu/pool/universe/p/pydocstyle/pydocstyle_2.1.1-1.dsc' pydocstyle_2.1.1-1.dsc 2258 SHA256:2282b9a63257ac714bccabdd42b6a751393ff44403f3b83166210eb6d042692d
'http://archive.ubuntu.com/ubuntu/pool/universe/p/pydocstyle/pydocstyle_2.1.1.orig.tar.gz' pydocstyle_2.1.1.orig.tar.gz 54950 SHA256:de1a385a043270dfcd535dea0fa9c67208f237a758566dc2b945e368e3989bce
'http://archive.ubuntu.com/ubuntu/pool/universe/p/pydocstyle/pydocstyle_2.1.1-1.debian.tar.xz' pydocstyle_2.1.1-1.debian.tar.xz 3748 SHA256:00bb87a0e4695ae70453aae2d48ec2c5767c8871a9db028b2b7df83c6ea943ee
```

### `dpkg` source package: `pyflakes=2.1.1-2ubuntu1`

Binary Packages:

- `python3-pyflakes=2.1.1-2ubuntu1`

Licenses: (parsed from: `/usr/share/doc/python3-pyflakes/copyright`)

- `MIT`

Source:

```console
$ apt-get source -qq --print-uris pyflakes=2.1.1-2ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/universe/p/pyflakes/pyflakes_2.1.1-2ubuntu1.dsc' pyflakes_2.1.1-2ubuntu1.dsc 2409 SHA512:5a616d0abb100e030a02f60daf7c3bb1bb8f42400aea4d96ba3fcc82ae1a2d66e71657f701a6b91a79a456a5e843c3e14938a4d78681ae1ace1e3ca11c7e9f0f
'http://archive.ubuntu.com/ubuntu/pool/universe/p/pyflakes/pyflakes_2.1.1.orig.tar.gz' pyflakes_2.1.1.orig.tar.gz 58072 SHA512:7ebf5843b38146305c1063e070480fea8ec3b47fa1be546b1fafaeb242a688a5a001f978e7257fd71d5905b9a338b466ef17c7330725191587e9c40ba632c3f8
'http://archive.ubuntu.com/ubuntu/pool/universe/p/pyflakes/pyflakes_2.1.1-2ubuntu1.debian.tar.xz' pyflakes_2.1.1-2ubuntu1.debian.tar.xz 8068 SHA512:4fadc079527d001c3e63683a1fb24bfe7ea9e257c53837c135fda82dfae002b925f7a0f1cb0f1f09b49e641cd25470c76e9f46a3603a59b9cf3c4780dda6c4e8
```

### `dpkg` source package: `pygments=2.3.1+dfsg-1ubuntu2.2`

Binary Packages:

- `python3-pygments=2.3.1+dfsg-1ubuntu2.2`

Licenses: (parsed from: `/usr/share/doc/python3-pygments/copyright`)

- `Apache-2.0`

Source:

```console
$ apt-get source -qq --print-uris pygments=2.3.1+dfsg-1ubuntu2.2
'http://archive.ubuntu.com/ubuntu/pool/main/p/pygments/pygments_2.3.1%2bdfsg-1ubuntu2.2.dsc' pygments_2.3.1+dfsg-1ubuntu2.2.dsc 2478 SHA512:4ddb077858f5f5c612f2f531b16fc80b75291d8a25e6edf0f6617ea1abd2e12569f658d8882560249dbb80f61bf2fe7ae0639531325ca1e5ad3e439fcffea468
'http://archive.ubuntu.com/ubuntu/pool/main/p/pygments/pygments_2.3.1%2bdfsg.orig.tar.gz' pygments_2.3.1+dfsg.orig.tar.gz 1110919 SHA512:5a3a7412b92c5d1cf2a0f9faed36d8b39b7518fc24ec0bd936c20ca9188a219d8307051b4073165c2cda4bba1a2a2f5d09369d661b0b9ef39015ace5f6095cc8
'http://archive.ubuntu.com/ubuntu/pool/main/p/pygments/pygments_2.3.1%2bdfsg-1ubuntu2.2.debian.tar.xz' pygments_2.3.1+dfsg-1ubuntu2.2.debian.tar.xz 11068 SHA512:81f1fee4aafec7a82120a725b6622ecf4a055d04fa16f0c24b356ebeb04fcec875ae24ee897bdd1b4b3fa4de1e422bd0fc14ab6bd0067cf81e09f9444e1f1b93
```

### `dpkg` source package: `pyparsing=2.4.6-1`

Binary Packages:

- `python3-pyparsing=2.4.6-1`

Licenses: (parsed from: `/usr/share/doc/python3-pyparsing/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `Expat`
- `GPL-2`
- `GPL-3`
- `ellis-and-grant`
- `salvolainen`

Source:

```console
$ apt-get source -qq --print-uris pyparsing=2.4.6-1
'http://archive.ubuntu.com/ubuntu/pool/main/p/pyparsing/pyparsing_2.4.6-1.dsc' pyparsing_2.4.6-1.dsc 2436 SHA256:53f7f9804c8d98bce52495ee7b744f5224eec54639fb2f6422a5d9ffec14eccd
'http://archive.ubuntu.com/ubuntu/pool/main/p/pyparsing/pyparsing_2.4.6.orig.tar.gz' pyparsing_2.4.6.orig.tar.gz 649181 SHA256:4c830582a84fb022400b85429791bc551f1f4871c33f23e44f353119e92f969f
'http://archive.ubuntu.com/ubuntu/pool/main/p/pyparsing/pyparsing_2.4.6-1.debian.tar.xz' pyparsing_2.4.6-1.debian.tar.xz 7748 SHA256:83ea6c57f8c1057b08e4c2e3b637017ec9f27da5c7216d75c6a0aa5dea242fba
```

### `dpkg` source package: `pytest=4.6.9-1`

Binary Packages:

- `python3-pytest=4.6.9-1`

Licenses: (parsed from: `/usr/share/doc/python3-pytest/copyright`)

- `BSD-3-clause`
- `Expat`

Source:

```console
$ apt-get source -qq --print-uris pytest=4.6.9-1
'http://archive.ubuntu.com/ubuntu/pool/universe/p/pytest/pytest_4.6.9-1.dsc' pytest_4.6.9-1.dsc 3297 SHA256:c40707c78ec21d09749154c0a52cd8edf845196fcb5c840dd9f74546c49a511f
'http://archive.ubuntu.com/ubuntu/pool/universe/p/pytest/pytest_4.6.9.orig.tar.gz' pytest_4.6.9.orig.tar.gz 956816 SHA256:19e8f75eac01dd3f211edd465b39efbcbdc8fc5f7866d7dd49fedb30d8adf339
'http://archive.ubuntu.com/ubuntu/pool/universe/p/pytest/pytest_4.6.9-1.debian.tar.xz' pytest_4.6.9-1.debian.tar.xz 11892 SHA256:5dc519e7d737943b75117b8106a493e85a09a0c4a62a4cfe7e32af41577f158a
```

### `dpkg` source package: `python-argcomplete=1.8.1-1.3ubuntu1`

Binary Packages:

- `python3-argcomplete=1.8.1-1.3ubuntu1`

Licenses: (parsed from: `/usr/share/doc/python3-argcomplete/copyright`)

- `Apache-2.0`

Source:

```console
$ apt-get source -qq --print-uris python-argcomplete=1.8.1-1.3ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/universe/p/python-argcomplete/python-argcomplete_1.8.1-1.3ubuntu1.dsc' python-argcomplete_1.8.1-1.3ubuntu1.dsc 2159 SHA256:5bb7036a7934ab057d6b8b00c4ace07ab020ac038a3a8dd270605ef25d3d117b
'http://archive.ubuntu.com/ubuntu/pool/universe/p/python-argcomplete/python-argcomplete_1.8.1.orig.tar.gz' python-argcomplete_1.8.1.orig.tar.gz 53282 SHA256:2997cc0e17d8a2db4789dc84cfe02a0b1579f1f17d79b0b993e722d0acee0649
'http://archive.ubuntu.com/ubuntu/pool/universe/p/python-argcomplete/python-argcomplete_1.8.1-1.3ubuntu1.debian.tar.xz' python-argcomplete_1.8.1-1.3ubuntu1.debian.tar.xz 7380 SHA256:94617fce9110eec2c9f75ca01ec760c10bc496c3765729f3c4cb9ed52ffd5d61
```

### `dpkg` source package: `python-atomicwrites=1.1.5-2build1`

Binary Packages:

- `python3-atomicwrites=1.1.5-2build1`

Licenses: (parsed from: `/usr/share/doc/python3-atomicwrites/copyright`)

- `Expat`

Source:

```console
$ apt-get source -qq --print-uris python-atomicwrites=1.1.5-2build1
'http://archive.ubuntu.com/ubuntu/pool/universe/p/python-atomicwrites/python-atomicwrites_1.1.5-2build1.dsc' python-atomicwrites_1.1.5-2build1.dsc 2440 SHA256:cb40aad75d768ca492c68f1f63e74782a51710b2830776fba2c5ce5ac8c06f22
'http://archive.ubuntu.com/ubuntu/pool/universe/p/python-atomicwrites/python-atomicwrites_1.1.5.orig.tar.gz' python-atomicwrites_1.1.5.orig.tar.gz 11050 SHA256:04e9a6c3dae3651328cb51f420f5f5992b8c7fc0008c7a66606c58df011594d0
'http://archive.ubuntu.com/ubuntu/pool/universe/p/python-atomicwrites/python-atomicwrites_1.1.5-2build1.debian.tar.xz' python-atomicwrites_1.1.5-2build1.debian.tar.xz 2900 SHA256:98da22e821efc86d06c39ac4ab1e21e8ed8b01445bed84affa6dbdc5a50571f4
```

### `dpkg` source package: `python-attrs=19.3.0-2`

Binary Packages:

- `python3-attr=19.3.0-2`

Licenses: (parsed from: `/usr/share/doc/python3-attr/copyright`)

- `Expat`

Source:

```console
$ apt-get source -qq --print-uris python-attrs=19.3.0-2
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-attrs/python-attrs_19.3.0-2.dsc' python-attrs_19.3.0-2.dsc 2636 SHA256:a092161ca4df829e9a525623dd2dfd57fe5b98ce6a313053d62d9d11caa4c66f
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-attrs/python-attrs_19.3.0.orig.tar.xz' python-attrs_19.3.0.orig.tar.xz 104604 SHA256:706754d94b545e1661babe023d4b0a458fbf99ae5d9f678e3ac2ca55a0c31e91
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-attrs/python-attrs_19.3.0-2.debian.tar.xz' python-attrs_19.3.0-2.debian.tar.xz 4836 SHA256:21bb27d9bca4947528b2be35d2c38b91af2d07a44e23e443d9115de9a03caa79
```

### `dpkg` source package: `python-cffi=1.14.0-1build1`

Binary Packages:

- `python3-cffi-backend=1.14.0-1build1`

Licenses: (parsed from: `/usr/share/doc/python3-cffi-backend/copyright`)

- `Expat`

Source:

```console
$ apt-get source -qq --print-uris python-cffi=1.14.0-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-cffi/python-cffi_1.14.0-1build1.dsc' python-cffi_1.14.0-1build1.dsc 2919 SHA256:3ff41ebda23cbbc0e37c7fd324d8ba886a4371765732b365a3204d7fb53f9042
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-cffi/python-cffi_1.14.0.orig.tar.gz' python-cffi_1.14.0.orig.tar.gz 463065 SHA256:2d384f4a127a15ba701207f7639d94106693b6cd64173d6c8988e2c25f3ac2b6
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-cffi/python-cffi_1.14.0-1build1.debian.tar.xz' python-cffi_1.14.0-1build1.debian.tar.xz 6600 SHA256:1ad7f828cb4391776041edfba5182c2df03982401fc647dce43e73e24dfaa566
```

### `dpkg` source package: `python-cryptography=2.8-3ubuntu0.3`

Binary Packages:

- `python3-cryptography=2.8-3ubuntu0.3`

Licenses: (parsed from: `/usr/share/doc/python3-cryptography/copyright`)

- `Apache`
- `Apache-2.0`
- `Expat`

Source:

```console
$ apt-get source -qq --print-uris python-cryptography=2.8-3ubuntu0.3
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-cryptography/python-cryptography_2.8-3ubuntu0.3.dsc' python-cryptography_2.8-3ubuntu0.3.dsc 3681 SHA512:71a393ebcd27e99de7256af7ed80be9e91b668f1fba990d505a0ec47624bb797c932f8613d83089a793bdb7e096e86bf0ed33b63df419793687f28a128e40243
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-cryptography/python-cryptography_2.8.orig.tar.gz' python-cryptography_2.8.orig.tar.gz 504516 SHA512:bf3ca44123c693b0602be19445925f9efebd46c469909e47b7907d57141fb6bd99268c33e1fe3f42a08ab8b4edd4f98f21b6a682f530352313334dfd31ba91e7
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-cryptography/python-cryptography_2.8-3ubuntu0.3.debian.tar.xz' python-cryptography_2.8-3ubuntu0.3.debian.tar.xz 14124 SHA512:bec38d5c0fc5451e36b98435590301abba0f3ddf863d6d5307d7ba8c0ee5bb8ae39e8f97f7d807c1d25e5b2ad3bdac278329077ce0acf2344775139afa339a81
```

### `dpkg` source package: `python-dateutil=2.7.3-3ubuntu1`

Binary Packages:

- `python3-dateutil=2.7.3-3ubuntu1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris python-dateutil=2.7.3-3ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-dateutil/python-dateutil_2.7.3-3ubuntu1.dsc' python-dateutil_2.7.3-3ubuntu1.dsc 2486 SHA256:7f2eb996853d7e06d2cffdf7f67f7893bb6ea351d3ee352596db70b855254c90
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-dateutil/python-dateutil_2.7.3.orig.tar.gz' python-dateutil_2.7.3.orig.tar.gz 302871 SHA256:e27001de32f627c22380a688bcc43ce83504a7bc5da472209b4c70f02829f0b8
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-dateutil/python-dateutil_2.7.3.orig.tar.gz.asc' python-dateutil_2.7.3.orig.tar.gz.asc 833 SHA256:95caabf7dc886ac18900896e0aa1b30f9cf1a44461fb780acffe130b37ee5047
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-dateutil/python-dateutil_2.7.3-3ubuntu1.debian.tar.xz' python-dateutil_2.7.3-3ubuntu1.debian.tar.xz 13988 SHA256:39ad4bfff2dc3167de320fd181e204ee19206807c6ad7c9a2642ef53398c8c48
```

### `dpkg` source package: `python-distro=1.4.0-1`

Binary Packages:

- `python3-distro=1.4.0-1`

Licenses: (parsed from: `/usr/share/doc/python3-distro/copyright`)

- `Apache-2.0`

Source:

```console
$ apt-get source -qq --print-uris python-distro=1.4.0-1
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-distro/python-distro_1.4.0-1.dsc' python-distro_1.4.0-1.dsc 2087 SHA256:6bbd33b1e8512e3a57de77242d6688ee9df6a1ed62b2aca545b608708d9e9064
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-distro/python-distro_1.4.0.orig.tar.gz' python-distro_1.4.0.orig.tar.gz 53719 SHA256:362dde65d846d23baee4b5c058c8586f219b5a54be1cf5fc6ff55c4578392f57
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-distro/python-distro_1.4.0-1.debian.tar.xz' python-distro_1.4.0-1.debian.tar.xz 2784 SHA256:ac87fa42e0a37aeec87a988982725ca3c567dd687e7bfbfd1cff86167066b891
```

### `dpkg` source package: `python-docutils=0.16+dfsg-2`

Binary Packages:

- `docutils-common=0.16+dfsg-2`
- `python3-docutils=0.16+dfsg-2`

Licenses: (parsed from: `/usr/share/doc/docutils-common/copyright`, `/usr/share/doc/python3-docutils/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `GPL-3`
- `GPL-3+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `Python-2.1.1`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris python-docutils=0.16+dfsg-2
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-docutils/python-docutils_0.16%2bdfsg-2.dsc' python-docutils_0.16+dfsg-2.dsc 2526 SHA256:8b2368732cba4c0d1005a6c654a1ee752c55ea9f2ec96ebee9423774b08609c2
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-docutils/python-docutils_0.16%2bdfsg.orig.tar.xz' python-docutils_0.16+dfsg.orig.tar.xz 1347300 SHA256:eee46a039937dd648a03a534647cdbb2370b288076e12d9e330a3fe8ef66781e
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-docutils/python-docutils_0.16%2bdfsg-2.debian.tar.xz' python-docutils_0.16+dfsg-2.debian.tar.xz 31004 SHA256:9dfaaf463e199f9568eee750e153f6e747a51a8ea642c5d668acf04e068c8699
```

### `dpkg` source package: `python-flake8=3.7.9-2`

Binary Packages:

- `python3-flake8=3.7.9-2`

Licenses: (parsed from: `/usr/share/doc/python3-flake8/copyright`)

- `Expat`

Source:

```console
$ apt-get source -qq --print-uris python-flake8=3.7.9-2
'http://archive.ubuntu.com/ubuntu/pool/universe/p/python-flake8/python-flake8_3.7.9-2.dsc' python-flake8_3.7.9-2.dsc 2448 SHA256:31f0dd2abcc55921257f78c2dc173dd3aeb5125a47414c6231c0dcc7b1934c9a
'http://archive.ubuntu.com/ubuntu/pool/universe/p/python-flake8/python-flake8_3.7.9.orig.tar.gz' python-flake8_3.7.9.orig.tar.gz 150123 SHA256:45681a117ecc81e870cbf1262835ae4af5e7a8b08e40b944a8a6e6b895914cfb
'http://archive.ubuntu.com/ubuntu/pool/universe/p/python-flake8/python-flake8_3.7.9-2.debian.tar.xz' python-flake8_3.7.9-2.debian.tar.xz 8128 SHA256:04fe9a45f40318289976392f7deb58886210a1a6f5a678b5eaa1f7461ff2dd96
```

### `dpkg` source package: `python-ifcfg=0.18-2osrf~focal`

Binary Packages:

- `python3-ifcfg=0.18-2osrf~focal`

Licenses: (parsed from: `/usr/share/doc/python3-ifcfg/copyright`)

- `BSD-3-clause`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python-importlib-metadata=1.5.0-1`

Binary Packages:

- `python3-importlib-metadata=1.5.0-1`

Licenses: (parsed from: `/usr/share/doc/python3-importlib-metadata/copyright`)

- `Apache-2`
- `Apache-2.0`

Source:

```console
$ apt-get source -qq --print-uris python-importlib-metadata=1.5.0-1
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-importlib-metadata/python-importlib-metadata_1.5.0-1.dsc' python-importlib-metadata_1.5.0-1.dsc 2725 SHA256:a03afce78f7a775ea8717ba068522518e51fdda31710209e31a70c0ca27bbb8c
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-importlib-metadata/python-importlib-metadata_1.5.0.orig.tar.gz' python-importlib-metadata_1.5.0.orig.tar.gz 26738 SHA256:06f5b3a99029c7134207dd882428a66992a9de2bef7c2b699b5641f9886c3302
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-importlib-metadata/python-importlib-metadata_1.5.0-1.debian.tar.xz' python-importlib-metadata_1.5.0-1.debian.tar.xz 3288 SHA256:c9cd679ddf6cdd1873044ba50ff548b014a9426978ef7f7b8806d713e151a98e
```

### `dpkg` source package: `python-lark=0.8.1-1`

Binary Packages:

- `python3-lark=0.8.1-1`

Licenses: (parsed from: `/usr/share/doc/python3-lark/copyright`)

- `GPL-2`
- `GPL-2+`
- `MIT`

Source:

```console
$ apt-get source -qq --print-uris python-lark=0.8.1-1
'http://archive.ubuntu.com/ubuntu/pool/universe/p/python-lark/python-lark_0.8.1-1.dsc' python-lark_0.8.1-1.dsc 2167 SHA256:57a9b5f9975d6ad7d2a73c9fa559b6f682dc8fc79c73a61370753c9e527359d6
'http://archive.ubuntu.com/ubuntu/pool/universe/p/python-lark/python-lark_0.8.1.orig.tar.gz' python-lark_0.8.1.orig.tar.gz 301083 SHA256:64f8dd6f066097f86fd9aaff84a5ba98ecdcd0d10b8f3525f83b641b54643b63
'http://archive.ubuntu.com/ubuntu/pool/universe/p/python-lark/python-lark_0.8.1-1.debian.tar.xz' python-lark_0.8.1-1.debian.tar.xz 3748 SHA256:9661e0f1d3537d51c229966d0acd0518347019fb69c707f55a86ba6f0e2f908c
```

### `dpkg` source package: `python-mccabe=0.6.1-3`

Binary Packages:

- `python3-mccabe=0.6.1-3`

Licenses: (parsed from: `/usr/share/doc/python3-mccabe/copyright`)

- `Expat`

Source:

```console
$ apt-get source -qq --print-uris python-mccabe=0.6.1-3
'http://archive.ubuntu.com/ubuntu/pool/universe/p/python-mccabe/python-mccabe_0.6.1-3.dsc' python-mccabe_0.6.1-3.dsc 2110 SHA256:a8b69270e3d8754cd0ca7744fbd6843be62fd5d389b036952c7ff8ad6a8f203f
'http://archive.ubuntu.com/ubuntu/pool/universe/p/python-mccabe/python-mccabe_0.6.1.orig.tar.gz' python-mccabe_0.6.1.orig.tar.gz 8612 SHA256:dd8d182285a0fe56bace7f45b5e7d1a6ebcbf524e8f3bd87eb0f125271b8831f
'http://archive.ubuntu.com/ubuntu/pool/universe/p/python-mccabe/python-mccabe_0.6.1-3.debian.tar.xz' python-mccabe_0.6.1-3.debian.tar.xz 2452 SHA256:054a8306ee52e9cb67db427c82891175df0ce095f8df29593f65604d5fc9c0bf
```

### `dpkg` source package: `python-mock=3.0.5-1build1`

Binary Packages:

- `python3-mock=3.0.5-1build1`

Licenses: (parsed from: `/usr/share/doc/python3-mock/copyright`)

- `BSD-3-clause`

Source:

```console
$ apt-get source -qq --print-uris python-mock=3.0.5-1build1
'http://archive.ubuntu.com/ubuntu/pool/universe/p/python-mock/python-mock_3.0.5-1build1.dsc' python-mock_3.0.5-1build1.dsc 2494 SHA256:3a0adb359500edbaad2953899f85d06a65bf7e7cc27fb05e9d0e44be8ef59a49
'http://archive.ubuntu.com/ubuntu/pool/universe/p/python-mock/python-mock_3.0.5.orig.tar.gz' python-mock_3.0.5.orig.tar.gz 67887 SHA256:ff286cec703de8770f735269575ecb7d1c937b8851eba8de94d800df084e627c
'http://archive.ubuntu.com/ubuntu/pool/universe/p/python-mock/python-mock_3.0.5-1build1.debian.tar.xz' python-mock_3.0.5-1build1.debian.tar.xz 5956 SHA256:7c4eba9e6b8e7f2944770bd8340cdab0df0b81056cd81d614d6f19282a053dd1
```

### `dpkg` source package: `python-notify2=0.3-4`

Binary Packages:

- `python3-notify2=0.3-4`

Licenses: (parsed from: `/usr/share/doc/python3-notify2/copyright`)

- `BSD-3-Clause`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris python-notify2=0.3-4
'http://archive.ubuntu.com/ubuntu/pool/universe/p/python-notify2/python-notify2_0.3-4.dsc' python-notify2_0.3-4.dsc 2151 SHA256:27bf7d59c87e18940957df4f1d9905328918afd494ca5a85fc777f94d8938bd7
'http://archive.ubuntu.com/ubuntu/pool/universe/p/python-notify2/python-notify2_0.3.orig.tar.gz' python-notify2_0.3.orig.tar.gz 8798 SHA256:684281f91c51fc60bc7909a35bd21d043a2a421f4e269de1ed1f13845d1d6321
'http://archive.ubuntu.com/ubuntu/pool/universe/p/python-notify2/python-notify2_0.3-4.debian.tar.xz' python-notify2_0.3-4.debian.tar.xz 3416 SHA256:05fdd0fe156e92ee0df44debfdaf9f0ac95766599aaebfb149719c69d3265c2b
```

### `dpkg` source package: `python-packaging=20.3-1`

Binary Packages:

- `python3-packaging=20.3-1`

Licenses: (parsed from: `/usr/share/doc/python3-packaging/copyright`)

- `Apache-2.0`
- `BSD-3-clause`

Source:

```console
$ apt-get source -qq --print-uris python-packaging=20.3-1
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-packaging/python-packaging_20.3-1.dsc' python-packaging_20.3-1.dsc 2190 SHA256:37af2fd348eba9b638dde476c719e494fc2146031de75c7cbc66775affd45780
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-packaging/python-packaging_20.3.orig.tar.gz' python-packaging_20.3.orig.tar.gz 73015 SHA256:3c292b474fda1671ec57d46d739d072bfd495a4f51ad01a055121d81e952b7a3
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-packaging/python-packaging_20.3-1.debian.tar.xz' python-packaging_20.3-1.debian.tar.xz 2736 SHA256:b8d3d87e2352de60fefb49f7e3f8c562a5016e24cb3707da8bd8b358d695f4a7
```

### `dpkg` source package: `python-pbr=5.4.5-0ubuntu1`

Binary Packages:

- `python3-pbr=5.4.5-0ubuntu1`

Licenses: (parsed from: `/usr/share/doc/python3-pbr/copyright`)

- `Apache-2`
- `Apache-2.0`
- `BSD-2-clause`
- `BSD-3-clause`

Source:

```console
$ apt-get source -qq --print-uris python-pbr=5.4.5-0ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-pbr/python-pbr_5.4.5-0ubuntu1.dsc' python-pbr_5.4.5-0ubuntu1.dsc 3100 SHA256:3424d64cefe64ac0ac62131a1c4cf9bb9ce174d3f10790cad5ea3ae09adb9736
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-pbr/python-pbr_5.4.5.orig.tar.gz' python-pbr_5.4.5.orig.tar.gz 120510 SHA256:07f558fece33b05caf857474a366dfcc00562bca13dd8b47b2b3e22d9f9bf55c
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-pbr/python-pbr_5.4.5-0ubuntu1.debian.tar.xz' python-pbr_5.4.5-0ubuntu1.debian.tar.xz 9928 SHA256:bddf4a876641d84800276a43f999ed62c8c219381594e8a853598551488dcd7b
```

### `dpkg` source package: `python-pluggy=0.13.0-2`

Binary Packages:

- `python3-pluggy=0.13.0-2`

Licenses: (parsed from: `/usr/share/doc/python3-pluggy/copyright`)

- `Expat`

Source:

```console
$ apt-get source -qq --print-uris python-pluggy=0.13.0-2
'http://archive.ubuntu.com/ubuntu/pool/universe/p/python-pluggy/python-pluggy_0.13.0-2.dsc' python-pluggy_0.13.0-2.dsc 2431 SHA256:3fee6fdc62b335f47bb5bc934313a198433759671dfa8f24308a091ba8f9f610
'http://archive.ubuntu.com/ubuntu/pool/universe/p/python-pluggy/python-pluggy_0.13.0.orig.tar.gz' python-pluggy_0.13.0.orig.tar.gz 57726 SHA256:fa5fa1622fa6dd5c030e9cad086fa19ef6a0cf6d7a2d12318e10cb49d6d68f34
'http://archive.ubuntu.com/ubuntu/pool/universe/p/python-pluggy/python-pluggy_0.13.0-2.debian.tar.xz' python-pluggy_0.13.0-2.debian.tar.xz 2668 SHA256:9788c22d7aa7d7a9b82010d326a57598a768ee7fda92423ae8a57cb2dbbcd96d
```

### `dpkg` source package: `python-py=1.8.1-1ubuntu0.1`

Binary Packages:

- `python3-py=1.8.1-1ubuntu0.1`

Licenses: (parsed from: `/usr/share/doc/python3-py/copyright`)

- `Expat`

Source:

```console
$ apt-get source -qq --print-uris python-py=1.8.1-1ubuntu0.1
'http://archive.ubuntu.com/ubuntu/pool/universe/p/python-py/python-py_1.8.1-1ubuntu0.1.dsc' python-py_1.8.1-1ubuntu0.1.dsc 2325 SHA512:2dbd5362bfeda7885be35c977911c795fafcd7245d880c5911d70340223db7979a4a52e1c2f14830e9526ab816f472e99a22eb7c05dba8027bbd22c3838715f3
'http://archive.ubuntu.com/ubuntu/pool/universe/p/python-py/python-py_1.8.1.orig.tar.gz' python-py_1.8.1.orig.tar.gz 205568 SHA512:ba18fc5cc7a291c251f04e8565a35e94603eae718aad48252821f9d3b115a7cca4e640ea54d800eb71ec8ce345052d731fec9a115778b068526f394c5c45fb2a
'http://archive.ubuntu.com/ubuntu/pool/universe/p/python-py/python-py_1.8.1-1ubuntu0.1.debian.tar.xz' python-py_1.8.1-1ubuntu0.1.debian.tar.xz 13768 SHA512:c55259a4fc74cc84ef1c06835f339227b6f96ab0b93f2a90e5da5997cd4b8338761f5a24529653a4c3d687f0354b6af362d0b8ec37f7b00b559865aee8cd799d
```

### `dpkg` source package: `python-roman=2.0.0-3build1`

Binary Packages:

- `python3-roman=2.0.0-3build1`

Licenses: (parsed from: `/usr/share/doc/python3-roman/copyright`)

- `Python-2.1.1`
- `ZPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris python-roman=2.0.0-3build1
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-roman/python-roman_2.0.0-3build1.dsc' python-roman_2.0.0-3build1.dsc 2181 SHA256:cefa55af9e933a8b3d83359de500e170197320a2cdb3b4edaa2f9a7334e4d46b
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-roman/python-roman_2.0.0.orig.tar.gz' python-roman_2.0.0.orig.tar.gz 4968 SHA256:98f2c0fb3cdcfba465d12c85b3b7139fc4cd2177f1325f1bacfe00878c8fa7b9
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-roman/python-roman_2.0.0-3build1.debian.tar.xz' python-roman_2.0.0-3build1.debian.tar.xz 8680 SHA256:cf58cd8ac44d22da2aa0ad79957a4175b09552b4dd213c05fda34cde098584dc
```

### `dpkg` source package: `python-snowballstemmer=2.0.0-1`

Binary Packages:

- `python3-snowballstemmer=2.0.0-1`

Licenses: (parsed from: `/usr/share/doc/python3-snowballstemmer/copyright`)

- `BSD-3-Clause`

Source:

```console
$ apt-get source -qq --print-uris python-snowballstemmer=2.0.0-1
'http://archive.ubuntu.com/ubuntu/pool/universe/p/python-snowballstemmer/python-snowballstemmer_2.0.0-1.dsc' python-snowballstemmer_2.0.0-1.dsc 2069 SHA256:03620e434515f570a94525bc4de03c16ecabc8734dab9c163ce9b3b274a72558
'http://archive.ubuntu.com/ubuntu/pool/universe/p/python-snowballstemmer/python-snowballstemmer_2.0.0.orig.tar.gz' python-snowballstemmer_2.0.0.orig.tar.gz 79284 SHA256:df3bac3df4c2c01363f3dd2cfa78cce2840a79b9f1c2d2de9ce8d31683992f52
'http://archive.ubuntu.com/ubuntu/pool/universe/p/python-snowballstemmer/python-snowballstemmer_2.0.0-1.debian.tar.xz' python-snowballstemmer_2.0.0-1.debian.tar.xz 2472 SHA256:e90b052fbe5d5df202e9422ab2ca3fad0c5c36e49b27faa48cce9736f83a9995
```

### `dpkg` source package: `python-zipp=1.0.0-1ubuntu0.1`

Binary Packages:

- `python3-zipp=1.0.0-1ubuntu0.1`

Licenses: (parsed from: `/usr/share/doc/python3-zipp/copyright`)

- `Expat`

Source:

```console
$ apt-get source -qq --print-uris python-zipp=1.0.0-1ubuntu0.1
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-zipp/python-zipp_1.0.0-1ubuntu0.1.dsc' python-zipp_1.0.0-1ubuntu0.1.dsc 1955 SHA512:79429b0617aa749e730098a480487c9d06745ddf4409c3f76f5ea6c3430505a9a84da64838939b36d993dbc085817b68843455bdfc15ced988d9e369bcddd25c
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-zipp/python-zipp_1.0.0.orig.tar.gz' python-zipp_1.0.0.orig.tar.gz 10821 SHA512:dbfadfedd30ca4cb31ac4163f367134d96e57405ef00d5f4c19c0af7a141f78487dec29a0ba94975584fcb462d22c8b536bf29c67b7e298368072e897b0e9d82
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-zipp/python-zipp_1.0.0-1ubuntu0.1.debian.tar.xz' python-zipp_1.0.0-1ubuntu0.1.debian.tar.xz 3896 SHA512:1eb807009378b9d38a5b968e0f6c011ce3cd9462f78f79629e2561b4aa623c4f6b8817e062b46413779a2b147a6e4695da3fe6534a35af3fa18d40bd30b46d35
```

### `dpkg` source package: `python3-catkin-pkg-modules=0.5.2-1`

Binary Packages:

- `python3-catkin-pkg-modules=0.5.2-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-colcon-argcomplete=0.3.3-1`

Binary Packages:

- `python3-colcon-argcomplete=0.3.3-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-colcon-bash=0.4.2-1`

Binary Packages:

- `python3-colcon-bash=0.4.2-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-colcon-cd=0.1.1-1`

Binary Packages:

- `python3-colcon-cd=0.1.1-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-colcon-cmake=0.2.27-1`

Binary Packages:

- `python3-colcon-cmake=0.2.27-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-colcon-common-extensions=0.3.0-1`

Binary Packages:

- `python3-colcon-common-extensions=0.3.0-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-colcon-core=0.12.1-1`

Binary Packages:

- `python3-colcon-core=0.12.1-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-colcon-defaults=0.2.8-1`

Binary Packages:

- `python3-colcon-defaults=0.2.8-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-colcon-devtools=0.2.3-1`

Binary Packages:

- `python3-colcon-devtools=0.2.3-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-colcon-library-path=0.2.1-1`

Binary Packages:

- `python3-colcon-library-path=0.2.1-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-colcon-metadata=0.2.5-1`

Binary Packages:

- `python3-colcon-metadata=0.2.5-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-colcon-mixin=0.2.3-1`

Binary Packages:

- `python3-colcon-mixin=0.2.3-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-colcon-notification=0.2.15-1`

Binary Packages:

- `python3-colcon-notification=0.2.15-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-colcon-output=0.2.13-1`

Binary Packages:

- `python3-colcon-output=0.2.13-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-colcon-package-information=0.3.3-1`

Binary Packages:

- `python3-colcon-package-information=0.3.3-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-colcon-package-selection=0.2.10-2`

Binary Packages:

- `python3-colcon-package-selection=0.2.10-2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-colcon-parallel-executor=0.2.4-1`

Binary Packages:

- `python3-colcon-parallel-executor=0.2.4-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-colcon-pkg-config=0.1.0-1`

Binary Packages:

- `python3-colcon-pkg-config=0.1.0-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-colcon-powershell=0.3.7-1`

Binary Packages:

- `python3-colcon-powershell=0.3.7-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-colcon-python-setup-py=0.2.8-1`

Binary Packages:

- `python3-colcon-python-setup-py=0.2.8-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-colcon-recursive-crawl=0.2.1-1`

Binary Packages:

- `python3-colcon-recursive-crawl=0.2.1-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-colcon-ros=0.3.23-1`

Binary Packages:

- `python3-colcon-ros=0.3.23-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-colcon-test-result=0.3.8-1`

Binary Packages:

- `python3-colcon-test-result=0.3.8-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-colcon-zsh=0.4.0-1`

Binary Packages:

- `python3-colcon-zsh=0.4.0-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-defaults=3.8.2-0ubuntu2`

Binary Packages:

- `libpython3-dev:amd64=3.8.2-0ubuntu2`
- `libpython3-stdlib:amd64=3.8.2-0ubuntu2`
- `python3=3.8.2-0ubuntu2`
- `python3-dev=3.8.2-0ubuntu2`
- `python3-minimal=3.8.2-0ubuntu2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris python3-defaults=3.8.2-0ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3-defaults/python3-defaults_3.8.2-0ubuntu2.dsc' python3-defaults_3.8.2-0ubuntu2.dsc 2879 SHA256:3fa296ea2cd52738ebc44a1b83a8df500bf654356336d9bf057144171fe9ee7d
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3-defaults/python3-defaults_3.8.2-0ubuntu2.tar.gz' python3-defaults_3.8.2-0ubuntu2.tar.gz 138226 SHA256:e4969a54306421ebfd195d0c064935db7c53f9f152d8abaae63da33819235e9a
```

### `dpkg` source package: `python3-rosdep-modules=0.22.2-1`

Binary Packages:

- `python3-rosdep-modules=0.22.2-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-rosdep=0.22.2-1`

Binary Packages:

- `python3-rosdep=0.22.2-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-rosdistro-modules=0.9.0-1`

Binary Packages:

- `python3-rosdistro-modules=0.9.0-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-rospkg-modules=1.5.0-1`

Binary Packages:

- `python3-rospkg-modules=1.5.0-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-stdlib-extensions=3.8.10-0ubuntu1~20.04`

Binary Packages:

- `python3-distutils=3.8.10-0ubuntu1~20.04`
- `python3-lib2to3=3.8.10-0ubuntu1~20.04`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris python3-stdlib-extensions=3.8.10-0ubuntu1~20.04
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3-stdlib-extensions/python3-stdlib-extensions_3.8.10-0ubuntu1%7e20.04.dsc' python3-stdlib-extensions_3.8.10-0ubuntu1~20.04.dsc 2246 SHA512:7b78aa41ff95b914680a898c8f3c735e647a41c2b2c999870cbc9ce82b84e881ba2b009e0d08c4fbb7d5a782d07d652df13e9e0b94a229de58ddf4950c0d22c7
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3-stdlib-extensions/python3-stdlib-extensions_3.8.10.orig.tar.xz' python3-stdlib-extensions_3.8.10.orig.tar.xz 1099836 SHA512:3b1f63d04544d990f3a028c84239f333b5120db104325c3196c4791a6437a19b9d29d52a019f884a3cae3732836aa334a1cb20b3c8fa9ffba4f86d772114fe8a
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3-stdlib-extensions/python3-stdlib-extensions_3.8.10-0ubuntu1%7e20.04.debian.tar.xz' python3-stdlib-extensions_3.8.10-0ubuntu1~20.04.debian.tar.xz 24508 SHA512:ca4894ddf04e5f89c46183271e65978c4dadd90faac196e13600797b9b451356cea2a0ee2c1d25e82a11b4e192fc11c2125b533035cf75e8e28ff7fdc792c695
```

### `dpkg` source package: `python3-vcstool=0.3.0-1`

Binary Packages:

- `python3-vcstool=0.3.0-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3.8=3.8.10-0ubuntu1~20.04.18`

Binary Packages:

- `libpython3.8:amd64=3.8.10-0ubuntu1~20.04.18`
- `libpython3.8-dev:amd64=3.8.10-0ubuntu1~20.04.18`
- `libpython3.8-minimal:amd64=3.8.10-0ubuntu1~20.04.18`
- `libpython3.8-stdlib:amd64=3.8.10-0ubuntu1~20.04.18`
- `python3.8=3.8.10-0ubuntu1~20.04.18`
- `python3.8-dev=3.8.10-0ubuntu1~20.04.18`
- `python3.8-minimal=3.8.10-0ubuntu1~20.04.18`

Licenses: (parsed from: `/usr/share/doc/libpython3.8/copyright`, `/usr/share/doc/libpython3.8-dev/copyright`, `/usr/share/doc/libpython3.8-minimal/copyright`, `/usr/share/doc/libpython3.8-stdlib/copyright`, `/usr/share/doc/python3.8/copyright`, `/usr/share/doc/python3.8-dev/copyright`, `/usr/share/doc/python3.8-minimal/copyright`)

- `* Permission to use this software in any way is granted without`
- `By obtaining, using, and/or copying this software and/or its`
- `GPL-2`
- `Permission  is  hereby granted,  free  of charge,  to  any person`
- `Permission is hereby granted, free of charge, to any person obtaining`
- `Permission to use, copy, modify,`
- `Redistribution`
- `This software is provided 'as-is', without any express`
- `This software is provided as-is, without express`
- `binary forms, with`
- `distribute this software`
- `distribute this software and`
- `distribute this software for any`
- `implied`
- `its`
- `use in source`
- `without`

Source:

```console
$ apt-get source -qq --print-uris python3.8=3.8.10-0ubuntu1~20.04.18
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3.8/python3.8_3.8.10-0ubuntu1%7e20.04.18.dsc' python3.8_3.8.10-0ubuntu1~20.04.18.dsc 3549 SHA512:43914c7896adc3a397515c628e56d1f0aa0ea4210ed763516ae18ee15d1fbd6d926548943656fc5708046bf346d1c8c7c217d37dbf0ae41f7002fc84b33f3be7
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3.8/python3.8_3.8.10.orig.tar.xz' python3.8_3.8.10.orig.tar.xz 18433456 SHA512:0be69705483ff9692e12048a96180e586f9d84c8d53066629f7fb2389585eb75c0f3506bb8182936e322508f58b71f4d8c6dfebbab9049b31b49da11d3b98e80
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3.8/python3.8_3.8.10-0ubuntu1%7e20.04.18.debian.tar.xz' python3.8_3.8.10-0ubuntu1~20.04.18.debian.tar.xz 259508 SHA512:71d2415d0fe09a2952a51e800f63b089d0b3b6ca14f495ea7b79c2ec7f4bbb94146409c4d5c81bde6c2cbd916bb88a86c2a91e7cb368d3d67a8ec408766d5a63
```

### `dpkg` source package: `pyyaml=5.3.1-1ubuntu0.1`

Binary Packages:

- `python3-yaml=5.3.1-1ubuntu0.1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris pyyaml=5.3.1-1ubuntu0.1
'http://archive.ubuntu.com/ubuntu/pool/main/p/pyyaml/pyyaml_5.3.1-1ubuntu0.1.dsc' pyyaml_5.3.1-1ubuntu0.1.dsc 2418 SHA512:01b77bcc4fa21c3328d6eaa58d4b6b510a18c51cdecb9de5521620c7558b34cce15fbc9d0c2969acf5d44713b6c937c1b42b672bf55d6b3f990cb3f2d27b57f6
'http://archive.ubuntu.com/ubuntu/pool/main/p/pyyaml/pyyaml_5.3.1.orig.tar.gz' pyyaml_5.3.1.orig.tar.gz 269377 SHA512:87372877d396bd06cdb6b9052ef8822ef0589a211659bf27d7a1c4deca8429cb39e120a23e5d590d7adc0f8059ce1c8af42409bebd7c6d504d49dc8504d5683a
'http://archive.ubuntu.com/ubuntu/pool/main/p/pyyaml/pyyaml_5.3.1-1ubuntu0.1.debian.tar.xz' pyyaml_5.3.1-1ubuntu0.1.debian.tar.xz 8124 SHA512:d25762cc9ba93addbe4c9c99581a5eabe17c5c2129b7240180d0f4eae0610d44a2a4788a5b788aad9f1a508a154340910d6e0d8d3abe4804e2485352b94da292
```

### `dpkg` source package: `readline=8.0-4`

Binary Packages:

- `libreadline8:amd64=8.0-4`
- `readline-common=8.0-4`

Licenses: (parsed from: `/usr/share/doc/libreadline8/copyright`, `/usr/share/doc/readline-common/copyright`)

- `GFDL`
- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris readline=8.0-4
'http://archive.ubuntu.com/ubuntu/pool/main/r/readline/readline_8.0-4.dsc' readline_8.0-4.dsc 2434 SHA256:ac9c7bb7380fe740aef09f54becf482eb81032a33dc11f1a8f00e933c5f168f4
'http://archive.ubuntu.com/ubuntu/pool/main/r/readline/readline_8.0.orig.tar.gz' readline_8.0.orig.tar.gz 2975937 SHA256:e339f51971478d369f8a053a330a190781acb9864cf4c541060f12078948e461
'http://archive.ubuntu.com/ubuntu/pool/main/r/readline/readline_8.0-4.debian.tar.xz' readline_8.0-4.debian.tar.xz 30408 SHA256:60ed18dab6d6b7fc998a263d917f06d9cce6e1ccd19cd8bf4a9d33c5350cf8d6
```

### `dpkg` source package: `rhash=1.3.9-1`

Binary Packages:

- `librhash0:amd64=1.3.9-1`

Licenses: (parsed from: `/usr/share/doc/librhash0/copyright`)

- `0BSD`

Source:

```console
$ apt-get source -qq --print-uris rhash=1.3.9-1
'http://archive.ubuntu.com/ubuntu/pool/main/r/rhash/rhash_1.3.9-1.dsc' rhash_1.3.9-1.dsc 1990 SHA256:2c7d736fb4ddb0cec03e61b958921306cd8e0ba29ad2da4d9521739f25c7f053
'http://archive.ubuntu.com/ubuntu/pool/main/r/rhash/rhash_1.3.9.orig.tar.gz' rhash_1.3.9.orig.tar.gz 403415 SHA256:42b1006f998adb189b1f316bf1a60e3171da047a85c4aaded2d0d26c1476c9f6
'http://archive.ubuntu.com/ubuntu/pool/main/r/rhash/rhash_1.3.9.orig.tar.gz.asc' rhash_1.3.9.orig.tar.gz.asc 833 SHA256:db168ff736c3fc0983b705b8b95c63187ac79df554e11a47e5e719b242ff65d4
'http://archive.ubuntu.com/ubuntu/pool/main/r/rhash/rhash_1.3.9-1.debian.tar.xz' rhash_1.3.9-1.debian.tar.xz 9936 SHA256:64c6405e34a360297e9612564adb4af7fd0e2dc291f25df38252560c7ca1c11e
```

### `dpkg` source package: `ros-foxy-action-msgs=1.0.0-1focal.20230527.044538`

Binary Packages:

- `ros-foxy-action-msgs=1.0.0-1focal.20230527.044538`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-actionlib-msgs=2.0.5-1focal.20230527.050253`

Binary Packages:

- `ros-foxy-actionlib-msgs=2.0.5-1focal.20230527.050253`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-ament-cmake-auto=0.9.12-1focal.20230527.034119`

Binary Packages:

- `ros-foxy-ament-cmake-auto=0.9.12-1focal.20230527.034119`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-ament-cmake-auto/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-ament-cmake-copyright=0.9.8-1focal.20230527.034818`

Binary Packages:

- `ros-foxy-ament-cmake-copyright=0.9.8-1focal.20230527.034818`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-ament-cmake-copyright/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-ament-cmake-core=0.9.12-1focal.20230527.032458`

Binary Packages:

- `ros-foxy-ament-cmake-core=0.9.12-1focal.20230527.032458`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-ament-cmake-core/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-ament-cmake-cppcheck=0.9.8-1focal.20230527.034934`

Binary Packages:

- `ros-foxy-ament-cmake-cppcheck=0.9.8-1focal.20230527.034934`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-ament-cmake-cppcheck/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-ament-cmake-cpplint=0.9.8-1focal.20230527.035101`

Binary Packages:

- `ros-foxy-ament-cmake-cpplint=0.9.8-1focal.20230527.035101`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-ament-cmake-cpplint/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-ament-cmake-export-definitions=0.9.12-1focal.20230527.033021`

Binary Packages:

- `ros-foxy-ament-cmake-export-definitions=0.9.12-1focal.20230527.033021`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-ament-cmake-export-definitions/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-ament-cmake-export-dependencies=0.9.12-1focal.20230527.033513`

Binary Packages:

- `ros-foxy-ament-cmake-export-dependencies=0.9.12-1focal.20230527.033513`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-ament-cmake-export-dependencies/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-ament-cmake-export-include-directories=0.9.12-1focal.20230527.033159`

Binary Packages:

- `ros-foxy-ament-cmake-export-include-directories=0.9.12-1focal.20230527.033159`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-ament-cmake-export-include-directories/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-ament-cmake-export-interfaces=0.9.12-1focal.20230527.033435`

Binary Packages:

- `ros-foxy-ament-cmake-export-interfaces=0.9.12-1focal.20230527.033435`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-ament-cmake-export-interfaces/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-ament-cmake-export-libraries=0.9.12-1focal.20230527.033300`

Binary Packages:

- `ros-foxy-ament-cmake-export-libraries=0.9.12-1focal.20230527.033300`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-ament-cmake-export-libraries/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-ament-cmake-export-link-flags=0.9.12-1focal.20230527.033027`

Binary Packages:

- `ros-foxy-ament-cmake-export-link-flags=0.9.12-1focal.20230527.033027`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-ament-cmake-export-link-flags/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-ament-cmake-export-targets=0.9.12-1focal.20230527.033348`

Binary Packages:

- `ros-foxy-ament-cmake-export-targets=0.9.12-1focal.20230527.033348`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-ament-cmake-export-targets/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-ament-cmake-flake8=0.9.8-1focal.20230527.034934`

Binary Packages:

- `ros-foxy-ament-cmake-flake8=0.9.8-1focal.20230527.034934`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-ament-cmake-flake8/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-ament-cmake-gmock=0.9.12-1focal.20230527.033334`

Binary Packages:

- `ros-foxy-ament-cmake-gmock=0.9.12-1focal.20230527.033334`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-ament-cmake-gmock/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-ament-cmake-gtest=0.9.12-1focal.20230527.033233`

Binary Packages:

- `ros-foxy-ament-cmake-gtest=0.9.12-1focal.20230527.033233`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-ament-cmake-gtest/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-ament-cmake-include-directories=0.9.12-1focal.20230527.033241`

Binary Packages:

- `ros-foxy-ament-cmake-include-directories=0.9.12-1focal.20230527.033241`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-ament-cmake-include-directories/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-ament-cmake-libraries=0.9.12-1focal.20230527.033319`

Binary Packages:

- `ros-foxy-ament-cmake-libraries=0.9.12-1focal.20230527.033319`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-ament-cmake-libraries/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-ament-cmake-lint-cmake=0.9.8-1focal.20230527.034543`

Binary Packages:

- `ros-foxy-ament-cmake-lint-cmake=0.9.8-1focal.20230527.034543`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-ament-cmake-lint-cmake/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-ament-cmake-pep257=0.9.8-1focal.20230527.034930`

Binary Packages:

- `ros-foxy-ament-cmake-pep257=0.9.8-1focal.20230527.034930`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-ament-cmake-pep257/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-ament-cmake-pytest=0.9.12-1focal.20230527.033236`

Binary Packages:

- `ros-foxy-ament-cmake-pytest=0.9.12-1focal.20230527.033236`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-ament-cmake-pytest/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-ament-cmake-python=0.9.12-1focal.20230527.033035`

Binary Packages:

- `ros-foxy-ament-cmake-python=0.9.12-1focal.20230527.033035`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-ament-cmake-python/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-ament-cmake-ros=0.9.2-1focal.20230527.035553`

Binary Packages:

- `ros-foxy-ament-cmake-ros=0.9.2-1focal.20230527.035553`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-ament-cmake-target-dependencies=0.9.12-1focal.20230527.033419`

Binary Packages:

- `ros-foxy-ament-cmake-target-dependencies=0.9.12-1focal.20230527.033419`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-ament-cmake-target-dependencies/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-ament-cmake-test=0.9.12-1focal.20230527.033100`

Binary Packages:

- `ros-foxy-ament-cmake-test=0.9.12-1focal.20230527.033100`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-ament-cmake-test/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-ament-cmake-uncrustify=0.9.8-1focal.20230527.035043`

Binary Packages:

- `ros-foxy-ament-cmake-uncrustify=0.9.8-1focal.20230527.035043`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-ament-cmake-uncrustify/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-ament-cmake-version=0.9.12-1focal.20230527.033033`

Binary Packages:

- `ros-foxy-ament-cmake-version=0.9.12-1focal.20230527.033033`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-ament-cmake-version/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-ament-cmake-xmllint=0.9.8-1focal.20230527.035101`

Binary Packages:

- `ros-foxy-ament-cmake-xmllint=0.9.8-1focal.20230527.035101`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-ament-cmake-xmllint/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-ament-cmake=0.9.12-1focal.20230527.033726`

Binary Packages:

- `ros-foxy-ament-cmake=0.9.12-1focal.20230527.033726`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-ament-cmake/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-ament-copyright=0.9.8-1focal.20230527.033845`

Binary Packages:

- `ros-foxy-ament-copyright=0.9.8-1focal.20230527.033845`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-ament-copyright/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-ament-cppcheck=0.9.8-1focal.20230527.033020`

Binary Packages:

- `ros-foxy-ament-cppcheck=0.9.8-1focal.20230527.033020`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-ament-cppcheck/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-ament-cpplint=0.9.8-1focal.20230527.033950`

Binary Packages:

- `ros-foxy-ament-cpplint=0.9.8-1focal.20230527.033950`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-ament-cpplint/copyright`)

- `Apache License 2.0`
- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-ament-flake8=0.9.8-1focal.20230527.033314`

Binary Packages:

- `ros-foxy-ament-flake8=0.9.8-1focal.20230527.033314`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-ament-flake8/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-ament-index-cpp=1.1.0-1focal.20230527.035619`

Binary Packages:

- `ros-foxy-ament-index-cpp=1.1.0-1focal.20230527.035619`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-ament-index-python=1.1.0-1focal.20230527.034456`

Binary Packages:

- `ros-foxy-ament-index-python=1.1.0-1focal.20230527.034456`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-ament-lint-auto=0.9.8-1focal.20230527.033240`

Binary Packages:

- `ros-foxy-ament-lint-auto=0.9.8-1focal.20230527.033240`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-ament-lint-auto/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-ament-lint-cmake=0.9.8-1focal.20230527.034500`

Binary Packages:

- `ros-foxy-ament-lint-cmake=0.9.8-1focal.20230527.034500`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-ament-lint-cmake/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-ament-lint-common=0.9.8-1focal.20230527.035135`

Binary Packages:

- `ros-foxy-ament-lint-common=0.9.8-1focal.20230527.035135`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-ament-lint-common/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-ament-lint=0.9.8-1focal.20230527.033147`

Binary Packages:

- `ros-foxy-ament-lint=0.9.8-1focal.20230527.033147`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-ament-lint/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-ament-package=0.9.5-1focal.20210422.230933`

Binary Packages:

- `ros-foxy-ament-package=0.9.5-1focal.20210422.230933`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-ament-pep257=0.9.8-1focal.20230527.033555`

Binary Packages:

- `ros-foxy-ament-pep257=0.9.8-1focal.20230527.033555`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-ament-pep257/copyright`)

- `Apache License 2.0`
- `MIT`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-ament-uncrustify=0.9.8-1focal.20230527.034525`

Binary Packages:

- `ros-foxy-ament-uncrustify=0.9.8-1focal.20230527.034525`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-ament-uncrustify/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-ament-xmllint=0.9.8-1focal.20230527.033925`

Binary Packages:

- `ros-foxy-ament-xmllint=0.9.8-1focal.20230527.033925`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-ament-xmllint/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-builtin-interfaces=1.0.0-1focal.20230527.043831`

Binary Packages:

- `ros-foxy-builtin-interfaces=1.0.0-1focal.20230527.043831`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-class-loader=2.0.3-1focal.20230527.040750`

Binary Packages:

- `ros-foxy-class-loader=2.0.3-1focal.20230527.040750`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-common-interfaces=2.0.5-1focal.20230527.053021`

Binary Packages:

- `ros-foxy-common-interfaces=2.0.5-1focal.20230527.053021`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-composition-interfaces=1.0.0-1focal.20230527.044949`

Binary Packages:

- `ros-foxy-composition-interfaces=1.0.0-1focal.20230527.044949`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-console-bridge-vendor=1.2.4-1focal.20230527.035859`

Binary Packages:

- `ros-foxy-console-bridge-vendor=1.2.4-1focal.20230527.035859`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-diagnostic-msgs=2.0.5-1focal.20230527.050830`

Binary Packages:

- `ros-foxy-diagnostic-msgs=2.0.5-1focal.20230527.050830`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-domain-coordinator=0.9.2-1focal.20230527.033942`

Binary Packages:

- `ros-foxy-domain-coordinator=0.9.2-1focal.20230527.033942`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-eigen3-cmake-module=0.1.1-1focal.20230527.035045`

Binary Packages:

- `ros-foxy-eigen3-cmake-module=0.1.1-1focal.20230527.035045`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-fastcdr=1.0.13-1focal.20230527.033018`

Binary Packages:

- `ros-foxy-fastcdr=1.0.13-1focal.20230527.033018`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-fastrtps-cmake-module=1.0.4-1focal.20230527.035710`

Binary Packages:

- `ros-foxy-fastrtps-cmake-module=1.0.4-1focal.20230527.035710`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-fastrtps=2.1.4-1focal.20230527.035957`

Binary Packages:

- `ros-foxy-fastrtps=2.1.4-1focal.20230527.035957`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-fastrtps/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-foonathan-memory-vendor=1.2.0-1focal.20230527.035512`

Binary Packages:

- `ros-foxy-foonathan-memory-vendor=1.2.0-1focal.20230527.035512`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-geometry-msgs=2.0.5-1focal.20230527.045912`

Binary Packages:

- `ros-foxy-geometry-msgs=2.0.5-1focal.20230527.045912`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-geometry2=0.13.14-1focal.20230606.035309`

Binary Packages:

- `ros-foxy-geometry2=0.13.14-1focal.20230606.035309`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-geometry2/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-gmock-vendor=1.8.9001-1focal.20230527.033129`

Binary Packages:

- `ros-foxy-gmock-vendor=1.8.9001-1focal.20230527.033129`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-gtest-vendor=1.8.9001-1focal.20230527.033021`

Binary Packages:

- `ros-foxy-gtest-vendor=1.8.9001-1focal.20230527.033021`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-kdl-parser=2.4.1-2focal.20230527.040709`

Binary Packages:

- `ros-foxy-kdl-parser=2.4.1-2focal.20230527.040709`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-launch-ros=0.11.7-1focal.20230527.051922`

Binary Packages:

- `ros-foxy-launch-ros=0.11.7-1focal.20230527.051922`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-launch-ros/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-launch-testing-ament-cmake=0.10.10-1focal.20230527.035604`

Binary Packages:

- `ros-foxy-launch-testing-ament-cmake=0.10.10-1focal.20230527.035604`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-launch-testing-ament-cmake/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-launch-testing-ros=0.11.7-1focal.20230527.052148`

Binary Packages:

- `ros-foxy-launch-testing-ros=0.11.7-1focal.20230527.052148`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-launch-testing-ros/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-launch-testing=0.10.10-1focal.20230527.034909`

Binary Packages:

- `ros-foxy-launch-testing=0.10.10-1focal.20230527.034909`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-launch-testing/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-launch-xml=0.10.10-1focal.20230527.034905`

Binary Packages:

- `ros-foxy-launch-xml=0.10.10-1focal.20230527.034905`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-launch-xml/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-launch-yaml=0.10.10-1focal.20230527.034936`

Binary Packages:

- `ros-foxy-launch-yaml=0.10.10-1focal.20230527.034936`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-launch-yaml/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-launch=0.10.10-1focal.20230527.034732`

Binary Packages:

- `ros-foxy-launch=0.10.10-1focal.20230527.034732`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-launch/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-libstatistics-collector=1.0.2-1focal.20230527.051045`

Binary Packages:

- `ros-foxy-libstatistics-collector=1.0.2-1focal.20230527.051045`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-libstatistics-collector/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-libyaml-vendor=1.0.4-1focal.20230527.040802`

Binary Packages:

- `ros-foxy-libyaml-vendor=1.0.4-1focal.20230527.040802`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-lifecycle-msgs=1.0.0-1focal.20230527.044041`

Binary Packages:

- `ros-foxy-lifecycle-msgs=1.0.0-1focal.20230527.044041`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-message-filters=3.2.7-1focal.20230606.033844`

Binary Packages:

- `ros-foxy-message-filters=3.2.7-1focal.20230606.033844`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-message-filters/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-nav-msgs=2.0.5-1focal.20230527.050829`

Binary Packages:

- `ros-foxy-nav-msgs=2.0.5-1focal.20230527.050829`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-orocos-kdl=3.3.5-1focal.20230527.035509`

Binary Packages:

- `ros-foxy-orocos-kdl=3.3.5-1focal.20230527.035509`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-orocos-kdl/copyright`)

- `LGPL-2.1-or-later`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-osrf-pycommon=0.1.11-1focal.20230527.033202`

Binary Packages:

- `ros-foxy-osrf-pycommon=0.1.11-1focal.20230527.033202`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-pluginlib=2.5.4-1focal.20230527.040908`

Binary Packages:

- `ros-foxy-pluginlib=2.5.4-1focal.20230527.040908`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-python-cmake-module=0.8.1-1focal.20230527.035425`

Binary Packages:

- `ros-foxy-python-cmake-module=0.8.1-1focal.20230527.035425`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-rcl-action=1.1.14-1focal.20230527.051024`

Binary Packages:

- `ros-foxy-rcl-action=1.1.14-1focal.20230527.051024`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-rcl-interfaces=1.0.0-1focal.20230527.044147`

Binary Packages:

- `ros-foxy-rcl-interfaces=1.0.0-1focal.20230527.044147`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-rcl-lifecycle=1.1.14-1focal.20230527.051051`

Binary Packages:

- `ros-foxy-rcl-lifecycle=1.1.14-1focal.20230527.051051`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-rcl-logging-spdlog=1.1.0-1focal.20230527.040756`

Binary Packages:

- `ros-foxy-rcl-logging-spdlog=1.1.0-1focal.20230527.040756`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-rcl-yaml-param-parser=1.1.14-1focal.20230527.041257`

Binary Packages:

- `ros-foxy-rcl-yaml-param-parser=1.1.14-1focal.20230527.041257`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-rcl=1.1.14-1focal.20230527.050329`

Binary Packages:

- `ros-foxy-rcl=1.1.14-1focal.20230527.050329`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-rclcpp-action=2.4.3-1focal.20230527.053814`

Binary Packages:

- `ros-foxy-rclcpp-action=2.4.3-1focal.20230527.053814`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-rclcpp-action/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-rclcpp-components=2.4.3-1focal.20230527.053812`

Binary Packages:

- `ros-foxy-rclcpp-components=2.4.3-1focal.20230527.053812`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-rclcpp-components/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-rclcpp-lifecycle=2.4.3-1focal.20230527.053813`

Binary Packages:

- `ros-foxy-rclcpp-lifecycle=2.4.3-1focal.20230527.053813`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-rclcpp-lifecycle/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-rclcpp=2.4.3-1focal.20230527.051415`

Binary Packages:

- `ros-foxy-rclcpp=2.4.3-1focal.20230527.051415`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-rclcpp/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-rclpy=1.0.13-1focal.20230527.051412`

Binary Packages:

- `ros-foxy-rclpy=1.0.13-1focal.20230527.051412`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-rclpy/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-rcpputils=1.3.2-1focal.20230527.040309`

Binary Packages:

- `ros-foxy-rcpputils=1.3.2-1focal.20230527.040309`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-rcutils=1.1.5-1focal.20230527.035733`

Binary Packages:

- `ros-foxy-rcutils=1.1.5-1focal.20230527.035733`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-rcutils/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-rmw-dds-common=1.0.3-1focal.20230527.044005`

Binary Packages:

- `ros-foxy-rmw-dds-common=1.0.3-1focal.20230527.044005`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-rmw-fastrtps-cpp=1.3.2-1focal.20230527.045658`

Binary Packages:

- `ros-foxy-rmw-fastrtps-cpp=1.3.2-1focal.20230527.045658`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-rmw-fastrtps-cpp/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-rmw-fastrtps-shared-cpp=1.3.2-1focal.20230527.044759`

Binary Packages:

- `ros-foxy-rmw-fastrtps-shared-cpp=1.3.2-1focal.20230527.044759`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-rmw-fastrtps-shared-cpp/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-rmw-implementation-cmake=1.0.4-1focal.20230527.035429`

Binary Packages:

- `ros-foxy-rmw-implementation-cmake=1.0.4-1focal.20230527.035429`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-rmw-implementation-cmake/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-rmw-implementation=1.0.3-1focal.20230527.050044`

Binary Packages:

- `ros-foxy-rmw-implementation=1.0.3-1focal.20230527.050044`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-rmw=1.0.4-1focal.20230527.040801`

Binary Packages:

- `ros-foxy-rmw=1.0.4-1focal.20230527.040801`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-rmw/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-robot-state-publisher=2.4.5-1focal.20230606.034917`

Binary Packages:

- `ros-foxy-robot-state-publisher=2.4.5-1focal.20230606.034917`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-ros-base=0.9.2-1focal.20230606.035837`

Binary Packages:

- `ros-foxy-ros-base=0.9.2-1focal.20230606.035837`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-ros-core=0.9.2-1focal.20230527.064030`

Binary Packages:

- `ros-foxy-ros-core=0.9.2-1focal.20230527.064030`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-ros-environment=2.5.1-1focal.20230527.033325`

Binary Packages:

- `ros-foxy-ros-environment=2.5.1-1focal.20230527.033325`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-ros-workspace=1.0.2-1focal.20230527.032747`

Binary Packages:

- `ros-foxy-ros-workspace=1.0.2-1focal.20230527.032747`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-ros-workspace/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-ros2action=0.9.13-1focal.20230527.052737`

Binary Packages:

- `ros-foxy-ros2action=0.9.13-1focal.20230527.052737`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-ros2action/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-ros2bag=0.3.11-1focal.20230531.181845`

Binary Packages:

- `ros-foxy-ros2bag=0.3.11-1focal.20230531.181845`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-ros2bag/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-ros2cli=0.9.13-1focal.20230527.052009`

Binary Packages:

- `ros-foxy-ros2cli=0.9.13-1focal.20230527.052009`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-ros2cli/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-ros2component=0.9.13-1focal.20230527.054727`

Binary Packages:

- `ros-foxy-ros2component=0.9.13-1focal.20230527.054727`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-ros2component/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-ros2doctor=0.9.13-1focal.20230527.052802`

Binary Packages:

- `ros-foxy-ros2doctor=0.9.13-1focal.20230527.052802`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-ros2doctor/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-ros2interface=0.9.13-1focal.20230527.052807`

Binary Packages:

- `ros-foxy-ros2interface=0.9.13-1focal.20230527.052807`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-ros2interface/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-ros2launch=0.11.7-1focal.20230527.053001`

Binary Packages:

- `ros-foxy-ros2launch=0.11.7-1focal.20230527.053001`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-ros2launch/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-ros2lifecycle=0.9.13-1focal.20230527.063130`

Binary Packages:

- `ros-foxy-ros2lifecycle=0.9.13-1focal.20230527.063130`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-ros2lifecycle/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-ros2multicast=0.9.13-1focal.20230527.052239`

Binary Packages:

- `ros-foxy-ros2multicast=0.9.13-1focal.20230527.052239`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-ros2multicast/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-ros2node=0.9.13-1focal.20230527.052809`

Binary Packages:

- `ros-foxy-ros2node=0.9.13-1focal.20230527.052809`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-ros2node/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-ros2param=0.9.13-1focal.20230527.053234`

Binary Packages:

- `ros-foxy-ros2param=0.9.13-1focal.20230527.053234`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-ros2param/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-ros2pkg=0.9.13-1focal.20230527.052813`

Binary Packages:

- `ros-foxy-ros2pkg=0.9.13-1focal.20230527.052813`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-ros2pkg/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-ros2run=0.9.13-1focal.20230527.053005`

Binary Packages:

- `ros-foxy-ros2run=0.9.13-1focal.20230527.053005`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-ros2run/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-ros2service=0.9.13-1focal.20230527.052820`

Binary Packages:

- `ros-foxy-ros2service=0.9.13-1focal.20230527.052820`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-ros2service/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-ros2topic=0.9.13-1focal.20230527.052817`

Binary Packages:

- `ros-foxy-ros2topic=0.9.13-1focal.20230527.052817`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-ros2topic/copyright`)

- `Apache License 2.0`
- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-rosbag2-compression=0.3.11-1focal.20230531.180822`

Binary Packages:

- `ros-foxy-rosbag2-compression=0.3.11-1focal.20230531.180822`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-rosbag2-compression/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-rosbag2-converter-default-plugins=0.3.11-1focal.20230531.180822`

Binary Packages:

- `ros-foxy-rosbag2-converter-default-plugins=0.3.11-1focal.20230531.180822`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-rosbag2-converter-default-plugins/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-rosbag2-cpp=0.3.11-1focal.20230531.180409`

Binary Packages:

- `ros-foxy-rosbag2-cpp=0.3.11-1focal.20230531.180409`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-rosbag2-cpp/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-rosbag2-storage-default-plugins=0.3.11-1focal.20230531.180611`

Binary Packages:

- `ros-foxy-rosbag2-storage-default-plugins=0.3.11-1focal.20230531.180611`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-rosbag2-storage-default-plugins/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-rosbag2-storage=0.3.11-1focal.20230531.175921`

Binary Packages:

- `ros-foxy-rosbag2-storage=0.3.11-1focal.20230531.175921`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-rosbag2-storage/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-rosbag2-transport=0.3.11-1focal.20230531.181114`

Binary Packages:

- `ros-foxy-rosbag2-transport=0.3.11-1focal.20230531.181114`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-rosbag2-transport/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-rosbag2=0.3.11-1focal.20230531.182405`

Binary Packages:

- `ros-foxy-rosbag2=0.3.11-1focal.20230531.182405`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-rosbag2/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-rosgraph-msgs=1.0.0-1focal.20230527.044114`

Binary Packages:

- `ros-foxy-rosgraph-msgs=1.0.0-1focal.20230527.044114`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-rosidl-adapter=1.3.1-1focal.20230527.035912`

Binary Packages:

- `ros-foxy-rosidl-adapter=1.3.1-1focal.20230527.035912`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-rosidl-adapter/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-rosidl-cmake=1.3.1-1focal.20230527.040133`

Binary Packages:

- `ros-foxy-rosidl-cmake=1.3.1-1focal.20230527.040133`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-rosidl-cmake/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-rosidl-default-generators=1.0.1-1focal.20230527.043401`

Binary Packages:

- `ros-foxy-rosidl-default-generators=1.0.1-1focal.20230527.043401`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-rosidl-default-runtime=1.0.1-1focal.20230527.043504`

Binary Packages:

- `ros-foxy-rosidl-default-runtime=1.0.1-1focal.20230527.043504`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-rosidl-generator-c=1.3.1-1focal.20230527.040645`

Binary Packages:

- `ros-foxy-rosidl-generator-c=1.3.1-1focal.20230527.040645`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-rosidl-generator-c/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-rosidl-generator-cpp=1.3.1-1focal.20230527.040726`

Binary Packages:

- `ros-foxy-rosidl-generator-cpp=1.3.1-1focal.20230527.040726`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-rosidl-generator-cpp/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-rosidl-generator-py=0.9.7-1focal.20230527.042900`

Binary Packages:

- `ros-foxy-rosidl-generator-py=0.9.7-1focal.20230527.042900`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-rosidl-generator-py/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-rosidl-parser=1.3.1-1focal.20230527.035942`

Binary Packages:

- `ros-foxy-rosidl-parser=1.3.1-1focal.20230527.035942`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-rosidl-parser/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-rosidl-runtime-c=1.3.1-1focal.20230527.040236`

Binary Packages:

- `ros-foxy-rosidl-runtime-c=1.3.1-1focal.20230527.040236`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-rosidl-runtime-c/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-rosidl-runtime-cpp=1.3.1-1focal.20230527.035847`

Binary Packages:

- `ros-foxy-rosidl-runtime-cpp=1.3.1-1focal.20230527.035847`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-rosidl-runtime-cpp/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-rosidl-runtime-py=0.9.1-1focal.20230527.045800`

Binary Packages:

- `ros-foxy-rosidl-runtime-py=0.9.1-1focal.20230527.045800`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-rosidl-typesupport-c=1.0.3-1focal.20230527.041518`

Binary Packages:

- `ros-foxy-rosidl-typesupport-c=1.0.3-1focal.20230527.041518`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-rosidl-typesupport-c/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-rosidl-typesupport-cpp=1.0.3-1focal.20230527.041729`

Binary Packages:

- `ros-foxy-rosidl-typesupport-cpp=1.0.3-1focal.20230527.041729`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-rosidl-typesupport-cpp/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-rosidl-typesupport-fastrtps-c=1.0.4-1focal.20230527.042305`

Binary Packages:

- `ros-foxy-rosidl-typesupport-fastrtps-c=1.0.4-1focal.20230527.042305`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-rosidl-typesupport-fastrtps-cpp=1.0.4-1focal.20230527.042012`

Binary Packages:

- `ros-foxy-rosidl-typesupport-fastrtps-cpp=1.0.4-1focal.20230527.042012`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-rosidl-typesupport-interface=1.3.1-1focal.20230527.035917`

Binary Packages:

- `ros-foxy-rosidl-typesupport-interface=1.3.1-1focal.20230527.035917`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-rosidl-typesupport-interface/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-rosidl-typesupport-introspection-c=1.3.1-1focal.20230527.040649`

Binary Packages:

- `ros-foxy-rosidl-typesupport-introspection-c=1.3.1-1focal.20230527.040649`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-rosidl-typesupport-introspection-c/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-rosidl-typesupport-introspection-cpp=1.3.1-1focal.20230527.040723`

Binary Packages:

- `ros-foxy-rosidl-typesupport-introspection-cpp=1.3.1-1focal.20230527.040723`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-rosidl-typesupport-introspection-cpp/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-rpyutils=0.2.0-1focal.20230527.034059`

Binary Packages:

- `ros-foxy-rpyutils=0.2.0-1focal.20230527.034059`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-sensor-msgs=2.0.5-1focal.20230527.050830`

Binary Packages:

- `ros-foxy-sensor-msgs=2.0.5-1focal.20230527.050830`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-shape-msgs=2.0.5-1focal.20230527.051353`

Binary Packages:

- `ros-foxy-shape-msgs=2.0.5-1focal.20230527.051353`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-shared-queues-vendor=0.3.11-1focal.20230531.174659`

Binary Packages:

- `ros-foxy-shared-queues-vendor=0.3.11-1focal.20230531.174659`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-shared-queues-vendor/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-spdlog-vendor=1.1.3-1focal.20230527.035447`

Binary Packages:

- `ros-foxy-spdlog-vendor=1.1.3-1focal.20230527.035447`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-sqlite3-vendor=0.3.11-1focal.20230531.175149`

Binary Packages:

- `ros-foxy-sqlite3-vendor=0.3.11-1focal.20230531.175149`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-sqlite3-vendor/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-sros2-cmake=0.9.5-1focal.20230527.053024`

Binary Packages:

- `ros-foxy-sros2-cmake=0.9.5-1focal.20230527.053024`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-sros2=0.9.5-1focal.20230527.052820`

Binary Packages:

- `ros-foxy-sros2=0.9.5-1focal.20230527.052820`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-statistics-msgs=1.0.0-1focal.20230527.044115`

Binary Packages:

- `ros-foxy-statistics-msgs=1.0.0-1focal.20230527.044115`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-std-msgs=2.0.5-1focal.20230527.044919`

Binary Packages:

- `ros-foxy-std-msgs=2.0.5-1focal.20230527.044919`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-std-srvs=2.0.5-1focal.20230527.043944`

Binary Packages:

- `ros-foxy-std-srvs=2.0.5-1focal.20230527.043944`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-stereo-msgs=2.0.5-1focal.20230527.052604`

Binary Packages:

- `ros-foxy-stereo-msgs=2.0.5-1focal.20230527.052604`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-tf2-bullet=0.13.14-1focal.20230606.034924`

Binary Packages:

- `ros-foxy-tf2-bullet=0.13.14-1focal.20230606.034924`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-tf2-bullet/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-tf2-eigen=0.13.14-1focal.20230606.035027`

Binary Packages:

- `ros-foxy-tf2-eigen=0.13.14-1focal.20230606.035027`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-tf2-eigen/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-tf2-geometry-msgs=0.13.14-1focal.20230606.035033`

Binary Packages:

- `ros-foxy-tf2-geometry-msgs=0.13.14-1focal.20230606.035033`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-tf2-geometry-msgs/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-tf2-kdl=0.13.14-1focal.20230606.035047`

Binary Packages:

- `ros-foxy-tf2-kdl=0.13.14-1focal.20230606.035047`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-tf2-kdl/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-tf2-msgs=0.13.14-1focal.20230527.050829`

Binary Packages:

- `ros-foxy-tf2-msgs=0.13.14-1focal.20230527.050829`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-tf2-msgs/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-tf2-py=0.13.14-1focal.20230527.052045`

Binary Packages:

- `ros-foxy-tf2-py=0.13.14-1focal.20230527.052045`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-tf2-py/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-tf2-ros=0.13.14-1focal.20230606.034417`

Binary Packages:

- `ros-foxy-tf2-ros=0.13.14-1focal.20230606.034417`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-tf2-ros/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-tf2-sensor-msgs=0.13.14-1focal.20230606.035100`

Binary Packages:

- `ros-foxy-tf2-sensor-msgs=0.13.14-1focal.20230606.035100`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-tf2-sensor-msgs/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-tf2-tools=0.13.14-1focal.20230606.035129`

Binary Packages:

- `ros-foxy-tf2-tools=0.13.14-1focal.20230606.035129`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-tf2-tools/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-tf2=0.13.14-1focal.20230527.051426`

Binary Packages:

- `ros-foxy-tf2=0.13.14-1focal.20230527.051426`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-tf2/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-tinyxml-vendor=0.8.2-1focal.20230527.034005`

Binary Packages:

- `ros-foxy-tinyxml-vendor=0.8.2-1focal.20230527.034005`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-tinyxml2-vendor=0.7.4-1focal.20230527.034003`

Binary Packages:

- `ros-foxy-tinyxml2-vendor=0.7.4-1focal.20230527.034003`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-tracetools=1.0.5-2focal.20230527.035811`

Binary Packages:

- `ros-foxy-tracetools=1.0.5-2focal.20230527.035811`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-trajectory-msgs=2.0.5-1focal.20230527.051434`

Binary Packages:

- `ros-foxy-trajectory-msgs=2.0.5-1focal.20230527.051434`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-uncrustify-vendor=1.4.0-1focal.20230527.034017`

Binary Packages:

- `ros-foxy-uncrustify-vendor=1.4.0-1focal.20230527.034017`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-unique-identifier-msgs=2.1.3-1focal.20230527.043808`

Binary Packages:

- `ros-foxy-unique-identifier-msgs=2.1.3-1focal.20230527.043808`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-urdf=2.4.0-2focal.20230527.040328`

Binary Packages:

- `ros-foxy-urdf=2.4.0-2focal.20230527.040328`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-urdfdom-headers=1.0.5-1focal.20230527.033203`

Binary Packages:

- `ros-foxy-urdfdom-headers=1.0.5-1focal.20230527.033203`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-urdfdom=2.3.3-1focal.20230527.040139`

Binary Packages:

- `ros-foxy-urdfdom=2.3.3-1focal.20230527.040139`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-visualization-msgs=2.0.5-1focal.20230527.051643`

Binary Packages:

- `ros-foxy-visualization-msgs=2.0.5-1focal.20230527.051643`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-yaml-cpp-vendor=7.0.3-1focal.20230527.034033`

Binary Packages:

- `ros-foxy-yaml-cpp-vendor=7.0.3-1focal.20230527.034033`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-yaml-cpp-vendor/copyright`)

- `Apache License 2.0`
- `MIT`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-foxy-zstd-vendor=0.3.11-1focal.20230531.174848`

Binary Packages:

- `ros-foxy-zstd-vendor=0.3.11-1focal.20230531.174848`

Licenses: (parsed from: `/usr/share/doc/ros-foxy-zstd-vendor/copyright`)

- `Apache License 2.0`
- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `rtmpdump=2.4+20151223.gitfa8646d.1-2build1`

Binary Packages:

- `librtmp1:amd64=2.4+20151223.gitfa8646d.1-2build1`

Licenses: (parsed from: `/usr/share/doc/librtmp1/copyright`)

- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris rtmpdump=2.4+20151223.gitfa8646d.1-2build1
'http://archive.ubuntu.com/ubuntu/pool/main/r/rtmpdump/rtmpdump_2.4%2b20151223.gitfa8646d.1-2build1.dsc' rtmpdump_2.4+20151223.gitfa8646d.1-2build1.dsc 2439 SHA256:fd89213f2d41b00c212a411a945146c6b2e00fce1d1819a9ec380b0d91bd1077
'http://archive.ubuntu.com/ubuntu/pool/main/r/rtmpdump/rtmpdump_2.4%2b20151223.gitfa8646d.1.orig.tar.gz' rtmpdump_2.4+20151223.gitfa8646d.1.orig.tar.gz 142213 SHA256:5c032f5c8cc2937eb55a81a94effdfed3b0a0304b6376147b86f951e225e3ab5
'http://archive.ubuntu.com/ubuntu/pool/main/r/rtmpdump/rtmpdump_2.4%2b20151223.gitfa8646d.1-2build1.debian.tar.xz' rtmpdump_2.4+20151223.gitfa8646d.1-2build1.debian.tar.xz 8216 SHA256:b256cc2aa96c9b99918052c4badfab0339ba95a852eab5ae37aa8b53c259efd2
```

### `dpkg` source package: `sed=4.7-1`

Binary Packages:

- `sed=4.7-1`

Licenses: (parsed from: `/usr/share/doc/sed/copyright`)

- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris sed=4.7-1
'http://archive.ubuntu.com/ubuntu/pool/main/s/sed/sed_4.7-1.dsc' sed_4.7-1.dsc 1880 SHA256:dd0e8daed987929920f7729771f9c7a5b48d094923aaf686efd2ab19db776108
'http://archive.ubuntu.com/ubuntu/pool/main/s/sed/sed_4.7.orig.tar.xz' sed_4.7.orig.tar.xz 1298316 SHA256:2885768cd0a29ff8d58a6280a270ff161f6a3deb5690b2be6c49f46d4c67bd6a
'http://archive.ubuntu.com/ubuntu/pool/main/s/sed/sed_4.7-1.debian.tar.xz' sed_4.7-1.debian.tar.xz 59824 SHA256:a2ab8d50807fd2242f86d6c6257399e790445ab6f8932f7f487d34361b4fc483
```

### `dpkg` source package: `sensible-utils=0.0.12+nmu1`

Binary Packages:

- `sensible-utils=0.0.12+nmu1`

Licenses: (parsed from: `/usr/share/doc/sensible-utils/copyright`)

- `All-permissive`
- `GPL-2`
- `GPL-2+`
- `configure`
- `installsh`

Source:

```console
$ apt-get source -qq --print-uris sensible-utils=0.0.12+nmu1
'http://archive.ubuntu.com/ubuntu/pool/main/s/sensible-utils/sensible-utils_0.0.12%2bnmu1.dsc' sensible-utils_0.0.12+nmu1.dsc 1753 SHA256:68bcb3e542e29a8a0bf281d9145d0e4cd9def529af2ba0cfe0afee3c5af958bc
'http://archive.ubuntu.com/ubuntu/pool/main/s/sensible-utils/sensible-utils_0.0.12%2bnmu1.tar.xz' sensible-utils_0.0.12+nmu1.tar.xz 61988 SHA256:53c6606facf083adbbf0da04e6d774b31ff3f46c7ba36a82d3f182779f4c3f5b
```

### `dpkg` source package: `setuptools=45.2.0-1ubuntu0.3`

Binary Packages:

- `python3-pkg-resources=45.2.0-1ubuntu0.3`
- `python3-setuptools=45.2.0-1ubuntu0.3`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris setuptools=45.2.0-1ubuntu0.3
'http://archive.ubuntu.com/ubuntu/pool/main/s/setuptools/setuptools_45.2.0-1ubuntu0.3.dsc' setuptools_45.2.0-1ubuntu0.3.dsc 2186 SHA512:5632fbf19e0ca01b1a74008d46ebcbf19973aa7b07448a2bfbc158124d11146c11e8070c20a9ec24f2441d31c1ae9efe87278c86cfef5e2e2633576152b10015
'http://archive.ubuntu.com/ubuntu/pool/main/s/setuptools/setuptools_45.2.0.orig.tar.xz' setuptools_45.2.0.orig.tar.xz 463920 SHA512:27527811ec555298e9dc726125bd54767f8813ee4f12e0a7673c2015fbe8834dbdbc4160193aafc8bc26ec7e9b228d62fd094b2ad78ed5cfa01e0419f80cc7e0
'http://archive.ubuntu.com/ubuntu/pool/main/s/setuptools/setuptools_45.2.0-1ubuntu0.3.debian.tar.xz' setuptools_45.2.0-1ubuntu0.3.debian.tar.xz 18516 SHA512:f3b44b4ae1b82fb0621eacb26b0a743b59d92372ce8bda25b12fd0c57757a90f0a39cd6f1cbedbdd3aa22760678ceb1e06998419b8c0763707f00965f12e81d7
```

### `dpkg` source package: `sgml-base=1.29.1`

Binary Packages:

- `sgml-base=1.29.1`

Licenses: (parsed from: `/usr/share/doc/sgml-base/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris sgml-base=1.29.1
'http://archive.ubuntu.com/ubuntu/pool/main/s/sgml-base/sgml-base_1.29.1.dsc' sgml-base_1.29.1.dsc 1526 SHA256:dc6bf6e060834d9534e38c3c322772d69ff3b32ceceb3739a7d4af84ce3cff8c
'http://archive.ubuntu.com/ubuntu/pool/main/s/sgml-base/sgml-base_1.29.1.tar.xz' sgml-base_1.29.1.tar.xz 12260 SHA256:3cac1ae8527c8ea0b699f2fb3891a0d44e49ece74d4e127f306e43cdb57bd78e
```

### `dpkg` source package: `shadow=1:4.8.1-1ubuntu5.20.04.5`

Binary Packages:

- `login=1:4.8.1-1ubuntu5.20.04.5`
- `passwd=1:4.8.1-1ubuntu5.20.04.5`

Licenses: (parsed from: `/usr/share/doc/login/copyright`, `/usr/share/doc/passwd/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris shadow=1:4.8.1-1ubuntu5.20.04.5
'http://archive.ubuntu.com/ubuntu/pool/main/s/shadow/shadow_4.8.1-1ubuntu5.20.04.5.dsc' shadow_4.8.1-1ubuntu5.20.04.5.dsc 2081 SHA512:882dbe402de8ac195152445d0d1ff48a4eb925cb440d3c3d956739295527e81ec9c8631ad8dd09cfccb2b8054600698cfe49db718e9e8d725e0a57d99b9d75c6
'http://archive.ubuntu.com/ubuntu/pool/main/s/shadow/shadow_4.8.1.orig.tar.xz' shadow_4.8.1.orig.tar.xz 1611196 SHA512:780a983483d847ed3c91c82064a0fa902b6f4185225978241bc3bc03fcc3aa143975b46aee43151c6ba43efcfdb1819516b76ba7ad3d1d3c34fcc38ea42e917b
'http://archive.ubuntu.com/ubuntu/pool/main/s/shadow/shadow_4.8.1-1ubuntu5.20.04.5.debian.tar.xz' shadow_4.8.1-1ubuntu5.20.04.5.debian.tar.xz 88744 SHA512:b12978fe6b7f0de302a6070f245aba6abc97ee3cefe7ea4925c16d45547d850f4cfd7ab5e7eb7940176d7afe37d16feda3b3bd458a0151a3ffe6a330f0197db9
```

### `dpkg` source package: `six=1.14.0-2`

Binary Packages:

- `python3-six=1.14.0-2`

Licenses: (parsed from: `/usr/share/doc/python3-six/copyright`)

- `Expat`

Source:

```console
$ apt-get source -qq --print-uris six=1.14.0-2
'http://archive.ubuntu.com/ubuntu/pool/main/s/six/six_1.14.0-2.dsc' six_1.14.0-2.dsc 2426 SHA256:1655e1f7246bd08332615eb3f6bb7769435724cd60e2ed0c0ce717e1ffd89416
'http://archive.ubuntu.com/ubuntu/pool/main/s/six/six_1.14.0.orig.tar.gz' six_1.14.0.orig.tar.gz 33857 SHA256:236bdbdce46e6e6a3d61a337c0f8b763ca1e8717c03b369e87a7ec7ce1319c0a
'http://archive.ubuntu.com/ubuntu/pool/main/s/six/six_1.14.0-2.debian.tar.xz' six_1.14.0-2.debian.tar.xz 4368 SHA256:02a80f76758dde7a8b2f42cd05a20db56d956f4678a882f0aba905ee49847050
```

### `dpkg` source package: `spdlog=1:1.5.0-1`

Binary Packages:

- `libspdlog-dev=1:1.5.0-1`
- `libspdlog1=1:1.5.0-1`

Licenses: (parsed from: `/usr/share/doc/libspdlog-dev/copyright`, `/usr/share/doc/libspdlog1/copyright`)

- `BSD-2-clause`
- `Expat`

Source:

```console
$ apt-get source -qq --print-uris spdlog=1:1.5.0-1
'http://archive.ubuntu.com/ubuntu/pool/universe/s/spdlog/spdlog_1.5.0-1.dsc' spdlog_1.5.0-1.dsc 2074 SHA256:1ab904099f46b6a6c9d5c9bc3213993bcbd2e7d8af5456d981eda4ad77fa54e2
'http://archive.ubuntu.com/ubuntu/pool/universe/s/spdlog/spdlog_1.5.0.orig.tar.gz' spdlog_1.5.0.orig.tar.gz 270416 SHA256:b38e0bbef7faac2b82fed550a0c19b0d4e7f6737d5321d4fd8f216b80f8aee8a
'http://archive.ubuntu.com/ubuntu/pool/universe/s/spdlog/spdlog_1.5.0-1.debian.tar.xz' spdlog_1.5.0-1.debian.tar.xz 14132 SHA256:7a3c1ab179bf98e7fbd652b85fde6bffdefa222c2e1603c10ce00d0a89c67cb4
```

### `dpkg` source package: `sqlite3=3.31.1-4ubuntu0.7`

Binary Packages:

- `libsqlite3-0:amd64=3.31.1-4ubuntu0.7`
- `libsqlite3-dev:amd64=3.31.1-4ubuntu0.7`

Licenses: (parsed from: `/usr/share/doc/libsqlite3-0/copyright`, `/usr/share/doc/libsqlite3-dev/copyright`)

- `GPL-2`
- `GPL-2+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris sqlite3=3.31.1-4ubuntu0.7
'http://archive.ubuntu.com/ubuntu/pool/main/s/sqlite3/sqlite3_3.31.1-4ubuntu0.7.dsc' sqlite3_3.31.1-4ubuntu0.7.dsc 2519 SHA512:5a95cf4a361cf129002c273275357352ece6b58b26720441df24c8344089b877d9c9e56c36ac997aee0759905e550e3178c21eed446fdfddf3ea09f642b8e448
'http://archive.ubuntu.com/ubuntu/pool/main/s/sqlite3/sqlite3_3.31.1.orig-www.tar.xz' sqlite3_3.31.1.orig-www.tar.xz 5764424 SHA512:a47adacd46c673cfd674cb64fb54b054e69560aed8c8c429773f0eccdcdbce4be538397506eca8e2d169f4b46d0d47442b273e12d82f8c87e1aadf3ade458db6
'http://archive.ubuntu.com/ubuntu/pool/main/s/sqlite3/sqlite3_3.31.1.orig.tar.xz' sqlite3_3.31.1.orig.tar.xz 7108036 SHA512:67e1050efe2988fa3d0d7e4a87e147a8114c6ff9b6ca5307a068befb38e861930eaee0135048ff1abb1e6323b507cbc68a0aac3a8fe5f095d6fcea1547a7efaf
'http://archive.ubuntu.com/ubuntu/pool/main/s/sqlite3/sqlite3_3.31.1-4ubuntu0.7.debian.tar.xz' sqlite3_3.31.1-4ubuntu0.7.debian.tar.xz 38476 SHA512:89ca9fcb8770b285b37cb630b5e0afc3a192fd0df740c4d8bdcfffa3646efa982d50dce49781f6a26d79a783640a337e64351d901bced89102044a40937299b5
```

### `dpkg` source package: `sudo=1.8.31-1ubuntu1.5`

Binary Packages:

- `sudo=1.8.31-1ubuntu1.5`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris sudo=1.8.31-1ubuntu1.5
'http://archive.ubuntu.com/ubuntu/pool/main/s/sudo/sudo_1.8.31-1ubuntu1.5.dsc' sudo_1.8.31-1ubuntu1.5.dsc 2088 SHA512:de072a31054093420ad9979376f3ad748aff178f5adca5af851ec0f85d53d03152e0b73f9c75e768339a8054db96be72c8c87591ed8734e6f18553679eddd83e
'http://archive.ubuntu.com/ubuntu/pool/main/s/sudo/sudo_1.8.31.orig.tar.gz' sudo_1.8.31.orig.tar.gz 3350674 SHA512:b9e408a322938c7a712458e9012d8a5f648fba5b23a5057cf5d8372c7f931262595f1575c32c32b9cb1a04af670ff4611e7df48d197e5c4cc038d6b65439a28a
'http://archive.ubuntu.com/ubuntu/pool/main/s/sudo/sudo_1.8.31-1ubuntu1.5.debian.tar.xz' sudo_1.8.31-1ubuntu1.5.debian.tar.xz 42736 SHA512:3c45fd235857e0673d852a0d66b116ac2df41660899bc360901b7b498494daf7c8423b6764898f1659d23fcebbcd354668d6a83e8059095441e4258852d57c96
```

### `dpkg` source package: `systemd=245.4-4ubuntu3.24`

Binary Packages:

- `libsystemd0:amd64=245.4-4ubuntu3.24`
- `libudev1:amd64=245.4-4ubuntu3.24`

Licenses: (parsed from: `/usr/share/doc/libsystemd0/copyright`, `/usr/share/doc/libudev1/copyright`)

- `CC0-1.0`
- `Expat`
- `GPL-2`
- `GPL-2 with Linux-syscall-note exception`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris systemd=245.4-4ubuntu3.24
'http://archive.ubuntu.com/ubuntu/pool/main/s/systemd/systemd_245.4-4ubuntu3.24.dsc' systemd_245.4-4ubuntu3.24.dsc 5262 SHA512:a7368dff1d7ce06bde4459dd635d2f25d9085f7c2cb0a5c3cbc30f63d24bea8145ff22c29709e67414b5ebd63fdd834b9552644b4adfbeb2b03c4db7a19e6ffe
'http://archive.ubuntu.com/ubuntu/pool/main/s/systemd/systemd_245.4.orig.tar.gz' systemd_245.4.orig.tar.gz 9000780 SHA512:02036bb1ab05301a9d0dfdd4b9c9376e90134474482531e6e292122380be2f24f99177493dd3af6f8af1a8ed2599ee0996da91a3b1b7872bbfaf26a1c3e61b4c
'http://archive.ubuntu.com/ubuntu/pool/main/s/systemd/systemd_245.4-4ubuntu3.24.debian.tar.xz' systemd_245.4-4ubuntu3.24.debian.tar.xz 294744 SHA512:97dd99ebc167edaa5d32157039a9af54c1747a43ef7625f67a697c971f5755e6038e496d04cce45d77055894b7d84d5bfb86c47a037e911c41a297ddb092dec8
```

### `dpkg` source package: `sysvinit=2.96-2.1ubuntu1`

Binary Packages:

- `sysvinit-utils=2.96-2.1ubuntu1`

Licenses: (parsed from: `/usr/share/doc/sysvinit-utils/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris sysvinit=2.96-2.1ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/s/sysvinit/sysvinit_2.96-2.1ubuntu1.dsc' sysvinit_2.96-2.1ubuntu1.dsc 2751 SHA256:c8b5f2ef86c4c1b8bf6b8a48408a4aa0815b0cf416df51dc0a9b6b8134f7e42c
'http://archive.ubuntu.com/ubuntu/pool/main/s/sysvinit/sysvinit_2.96.orig.tar.xz' sysvinit_2.96.orig.tar.xz 122164 SHA256:2a2e26b72aa235a23ab1c8471005f890309ce1196c83fbc9413c57b9ab62b587
'http://archive.ubuntu.com/ubuntu/pool/main/s/sysvinit/sysvinit_2.96.orig.tar.xz.asc' sysvinit_2.96.orig.tar.xz.asc 313 SHA256:dfc184b95da12c8c888c8ae6b0f26fe8a23b07fbcdd240f6600a8a78b9439fa0
'http://archive.ubuntu.com/ubuntu/pool/main/s/sysvinit/sysvinit_2.96-2.1ubuntu1.debian.tar.xz' sysvinit_2.96-2.1ubuntu1.debian.tar.xz 128840 SHA256:528041e261c90a957d9794bddb07217c89484d9c76a0279da508baec9684c4e6
```

### `dpkg` source package: `tar=1.30+dfsg-7ubuntu0.20.04.4`

Binary Packages:

- `tar=1.30+dfsg-7ubuntu0.20.04.4`

Licenses: (parsed from: `/usr/share/doc/tar/copyright`)

- `GPL-2`
- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris tar=1.30+dfsg-7ubuntu0.20.04.4
'http://archive.ubuntu.com/ubuntu/pool/main/t/tar/tar_1.30%2bdfsg-7ubuntu0.20.04.4.dsc' tar_1.30+dfsg-7ubuntu0.20.04.4.dsc 1812 SHA512:a771e996dad6c7b2d75336bae73a0c9e52f030a7474bdebe519a9c072819530541ff3200046ddc5277b0204e1eac056ff3679062c182cb28404bdac73da768fa
'http://archive.ubuntu.com/ubuntu/pool/main/t/tar/tar_1.30%2bdfsg.orig.tar.xz' tar_1.30+dfsg.orig.tar.xz 1883220 SHA512:f9b3843bd4da03f58d6f88de70ecb36b8ac29312714fd2120ff00f17c99e6d77cc82a8f9de348f4c2bdba9a6cc8e8c6c78039b6c14cdee15d68f2517000c36f2
'http://archive.ubuntu.com/ubuntu/pool/main/t/tar/tar_1.30%2bdfsg-7ubuntu0.20.04.4.debian.tar.xz' tar_1.30+dfsg-7ubuntu0.20.04.4.debian.tar.xz 24572 SHA512:942a7fb6e2edb7e50b26b1588219d0a99caf17ff1dfa1748449c3fa84ab8cf3e3e94bafb8334cc3b8397562d6a3ecd57bc0df2ddb2b90644a361fa63426d2982
```

### `dpkg` source package: `tiff=4.1.0+git191117-2ubuntu0.20.04.14`

Binary Packages:

- `libtiff5:amd64=4.1.0+git191117-2ubuntu0.20.04.14`

Licenses: (parsed from: `/usr/share/doc/libtiff5/copyright`)

- `Hylafax`

Source:

```console
$ apt-get source -qq --print-uris tiff=4.1.0+git191117-2ubuntu0.20.04.14
'http://archive.ubuntu.com/ubuntu/pool/main/t/tiff/tiff_4.1.0%2bgit191117-2ubuntu0.20.04.14.dsc' tiff_4.1.0+git191117-2ubuntu0.20.04.14.dsc 2251 SHA512:c6d2d754172a3a27555e5a3014428a19659e201eee6053708e8f3326948ffd747d31fa8856b7b11e52c37f743689ea9fcad0788e6cfc146e74bff1dcbe46a2bb
'http://archive.ubuntu.com/ubuntu/pool/main/t/tiff/tiff_4.1.0%2bgit191117.orig.tar.xz' tiff_4.1.0+git191117.orig.tar.xz 1533524 SHA512:25b4bc4522fc2e7f3ca6857b87acd4481d8643566b1120c755020afc8b48949238ee2078bc43dd3ba7407eaa4e36b1b712d7056f101ddaf60f94dab8607870b8
'http://archive.ubuntu.com/ubuntu/pool/main/t/tiff/tiff_4.1.0%2bgit191117-2ubuntu0.20.04.14.debian.tar.xz' tiff_4.1.0+git191117-2ubuntu0.20.04.14.debian.tar.xz 53440 SHA512:94dff2dcc41465107620975a9117611f86664118c8cd911898425726ccba5905c0d74c919c9c19724b321dca5f178ca65ddc6585c5b2b87a59567f8ef4fc2e76
```

### `dpkg` source package: `tinyxml2=7.0.0+dfsg-1build1`

Binary Packages:

- `libtinyxml2-6a:amd64=7.0.0+dfsg-1build1`
- `libtinyxml2-dev:amd64=7.0.0+dfsg-1build1`

Licenses: (parsed from: `/usr/share/doc/libtinyxml2-6a/copyright`, `/usr/share/doc/libtinyxml2-dev/copyright`)

- `GPL-2`
- `GPL-2+`
- `zlib/libpng`

Source:

```console
$ apt-get source -qq --print-uris tinyxml2=7.0.0+dfsg-1build1
'http://archive.ubuntu.com/ubuntu/pool/universe/t/tinyxml2/tinyxml2_7.0.0%2bdfsg-1build1.dsc' tinyxml2_7.0.0+dfsg-1build1.dsc 2053 SHA256:32a192cfb676070970b8718b40df4cf48208d4c8758a02acafa346df0de4e1bf
'http://archive.ubuntu.com/ubuntu/pool/universe/t/tinyxml2/tinyxml2_7.0.0%2bdfsg.orig.tar.gz' tinyxml2_7.0.0+dfsg.orig.tar.gz 359355 SHA256:1eceb87c311b5bf44b2b7351fa6ffda810605d7de402348157262543cf7185ef
'http://archive.ubuntu.com/ubuntu/pool/universe/t/tinyxml2/tinyxml2_7.0.0%2bdfsg-1build1.debian.tar.xz' tinyxml2_7.0.0+dfsg-1build1.debian.tar.xz 5832 SHA256:2544da0103456b5d9dd8e372cd6e4b0e74921ed878203c80d0319aa87d970f47
```

### `dpkg` source package: `tinyxml=2.6.2-4+deb10u2build0.20.04.1`

Binary Packages:

- `libtinyxml-dev:amd64=2.6.2-4+deb10u2build0.20.04.1`
- `libtinyxml2.6.2v5:amd64=2.6.2-4+deb10u2build0.20.04.1`

Licenses: (parsed from: `/usr/share/doc/libtinyxml-dev/copyright`, `/usr/share/doc/libtinyxml2.6.2v5/copyright`)

- `ZLIB`

Source:

```console
$ apt-get source -qq --print-uris tinyxml=2.6.2-4+deb10u2build0.20.04.1
'http://archive.ubuntu.com/ubuntu/pool/universe/t/tinyxml/tinyxml_2.6.2-4%2bdeb10u2build0.20.04.1.dsc' tinyxml_2.6.2-4+deb10u2build0.20.04.1.dsc 2035 SHA512:8edbdfa723bf47d42c3515b63f9e0bb5b009d0a14ea1ba6395368a265960babc147d899ec0414eba381c63700258932e4366a87a50e9eaf11913c42d43d7fe2d
'http://archive.ubuntu.com/ubuntu/pool/universe/t/tinyxml/tinyxml_2.6.2.orig.tar.gz' tinyxml_2.6.2.orig.tar.gz 210124 SHA512:133b5db06131a90ad0c2b39b0063f1c8e65e67288a7e5d67e1f7d9ba32af10dc5dfa0462f9723985ee27debe8f09a10a25d4b5a5aaff2ede979b1cebe8e59d56
'http://archive.ubuntu.com/ubuntu/pool/universe/t/tinyxml/tinyxml_2.6.2-4%2bdeb10u2build0.20.04.1.debian.tar.xz' tinyxml_2.6.2-4+deb10u2build0.20.04.1.debian.tar.xz 5404 SHA512:b37f8d45629ca9ba38d54e0f60a925f20d5fdf7a3932610485852522e592b2d4ffa305f4df593bfa0f2a031ab8bd1fb1b6e5fd5b499fcccc6b80ca22cd098cb3
```

### `dpkg` source package: `tzdata=2025b-0ubuntu0.20.04.1`

Binary Packages:

- `tzdata=2025b-0ubuntu0.20.04.1`

Licenses: (parsed from: `/usr/share/doc/tzdata/copyright`)

- `ICU`

Source:

```console
$ apt-get source -qq --print-uris tzdata=2025b-0ubuntu0.20.04.1
'http://archive.ubuntu.com/ubuntu/pool/main/t/tzdata/tzdata_2025b-0ubuntu0.20.04.1.dsc' tzdata_2025b-0ubuntu0.20.04.1.dsc 2556 SHA512:28843f9fee4167f840e48538211e06c52086b1b60b44b06c4fdc35203005d80fe0a21aa6e82d02ae23fc863e9713f2d642230353a84cec22786a09175a91d059
'http://archive.ubuntu.com/ubuntu/pool/main/t/tzdata/tzdata_2025b.orig.tar.gz' tzdata_2025b.orig.tar.gz 464295 SHA512:7d83741f3cae81fac8131994b43c55b6da7328df18b706e5ee40e9b3212bc506e6f8fc90988b18da424ed59eff69bce593f2783b7b5f18eb483a17aeb94258d6
'http://archive.ubuntu.com/ubuntu/pool/main/t/tzdata/tzdata_2025b.orig.tar.gz.asc' tzdata_2025b.orig.tar.gz.asc 833 SHA512:ad39fe16b32fad7eee27ff968b4e8af23267ce586629ad70e7625136d2c3cc3a42295a87b3dc770c291aa9112c56301629c1fe379735f70008e62864ce4e735a
'http://archive.ubuntu.com/ubuntu/pool/main/t/tzdata/tzdata_2025b-0ubuntu0.20.04.1.debian.tar.xz' tzdata_2025b-0ubuntu0.20.04.1.debian.tar.xz 177140 SHA512:4f33cdde840cfbe81be4ced5893b0a62938f9b22a27d28b4a74f02a47290ecaed927bc698d28c2322c0640abfde8b646192fe457c2cd39de0e8f0ba9c6a5553c
```

### `dpkg` source package: `ubuntu-keyring=2020.02.11.4`

Binary Packages:

- `ubuntu-keyring=2020.02.11.4`

Licenses: (parsed from: `/usr/share/doc/ubuntu-keyring/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris ubuntu-keyring=2020.02.11.4
'http://archive.ubuntu.com/ubuntu/pool/main/u/ubuntu-keyring/ubuntu-keyring_2020.02.11.4.dsc' ubuntu-keyring_2020.02.11.4.dsc 1863 SHA512:1232fc109f9afe7f4245f841cb992aeb7329ec1c3d310a174b837c0584005a7c46ce73f6d49a52a3e6c0eea03369ea5f308093c1a849e8f6597f6df792a87fb1
'http://archive.ubuntu.com/ubuntu/pool/main/u/ubuntu-keyring/ubuntu-keyring_2020.02.11.4.tar.gz' ubuntu-keyring_2020.02.11.4.tar.gz 39250 SHA512:318562b6892dad995e334ec44f08f065b4c6abed2d29c1f96f6ee0fa4d91a5cedc9b62a152c56cdf26a30c3ea97a58c1d037e892d155af5593a4e26b9a25a1ae
```

### `dpkg` source package: `ucf=3.0038+nmu1`

Binary Packages:

- `ucf=3.0038+nmu1`

Licenses: (parsed from: `/usr/share/doc/ucf/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris ucf=3.0038+nmu1
'http://archive.ubuntu.com/ubuntu/pool/main/u/ucf/ucf_3.0038%2bnmu1.dsc' ucf_3.0038+nmu1.dsc 1420 SHA256:89b6f921a30e04a946f62e6996be7c16f2f7c383d20783cd4704b502c6d5b125
'http://archive.ubuntu.com/ubuntu/pool/main/u/ucf/ucf_3.0038%2bnmu1.tar.xz' ucf_3.0038+nmu1.tar.xz 65860 SHA256:d00bc3dd8d2f91317f52b5352fe129023c72babad55bc0dd4ece7b34183c7436
```

### `dpkg` source package: `uncrustify=0.69.0+dfsg1-1build1`

Binary Packages:

- `uncrustify=0.69.0+dfsg1-1build1`

Licenses: (parsed from: `/usr/share/doc/uncrustify/copyright`)

- `Artistic`
- `GPL`
- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris uncrustify=0.69.0+dfsg1-1build1
'http://archive.ubuntu.com/ubuntu/pool/universe/u/uncrustify/uncrustify_0.69.0%2bdfsg1-1build1.dsc' uncrustify_0.69.0+dfsg1-1build1.dsc 1964 SHA256:439bf27a7ab9125c00cdbafbff40929ba44fe78dcf649f9598c27458f09a88d2
'http://archive.ubuntu.com/ubuntu/pool/universe/u/uncrustify/uncrustify_0.69.0%2bdfsg1.orig.tar.xz' uncrustify_0.69.0+dfsg1.orig.tar.xz 794444 SHA256:4984ef2ab1d30b915f395ae3fa23e283dca467052b8cfc7a1a84bfb9ca735211
'http://archive.ubuntu.com/ubuntu/pool/universe/u/uncrustify/uncrustify_0.69.0%2bdfsg1-1build1.debian.tar.xz' uncrustify_0.69.0+dfsg1-1build1.debian.tar.xz 5216 SHA256:1acd5cb1f307c04367edf747c09e7e7cc5f46bcd5e8a54912760663c0533f98a
```

### `dpkg` source package: `util-linux=2.34-0.1ubuntu9.6`

Binary Packages:

- `bsdutils=1:2.34-0.1ubuntu9.6`
- `fdisk=2.34-0.1ubuntu9.6`
- `libblkid1:amd64=2.34-0.1ubuntu9.6`
- `libfdisk1:amd64=2.34-0.1ubuntu9.6`
- `libmount1:amd64=2.34-0.1ubuntu9.6`
- `libsmartcols1:amd64=2.34-0.1ubuntu9.6`
- `libuuid1:amd64=2.34-0.1ubuntu9.6`
- `mount=2.34-0.1ubuntu9.6`
- `util-linux=2.34-0.1ubuntu9.6`

Licenses: (parsed from: `/usr/share/doc/bsdutils/copyright`, `/usr/share/doc/fdisk/copyright`, `/usr/share/doc/libblkid1/copyright`, `/usr/share/doc/libfdisk1/copyright`, `/usr/share/doc/libmount1/copyright`, `/usr/share/doc/libsmartcols1/copyright`, `/usr/share/doc/libuuid1/copyright`, `/usr/share/doc/mount/copyright`, `/usr/share/doc/util-linux/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `BSD-4-clause`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `LGPL`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`
- `LGPL-3+`
- `MIT`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris util-linux=2.34-0.1ubuntu9.6
'http://archive.ubuntu.com/ubuntu/pool/main/u/util-linux/util-linux_2.34-0.1ubuntu9.6.dsc' util-linux_2.34-0.1ubuntu9.6.dsc 4045 SHA512:5576ac13d0333300fc8224d775ce446030facfaf39201bd8ea55f2ebd74375e8e53be6cfd93b997cd1f99d026ade4e2dfba4bb504efada60fbb901b2ca0868bd
'http://archive.ubuntu.com/ubuntu/pool/main/u/util-linux/util-linux_2.34.orig.tar.xz' util-linux_2.34.orig.tar.xz 4974812 SHA512:2d0b76f63d32e7afb7acf61a83fabbfd58baa34ab78b3a331ce87f9c676a5fd71c56a493ded95039540d2c46b6048caaa38d7fb4491eb3d52d7b09dc54655cd7
'http://archive.ubuntu.com/ubuntu/pool/main/u/util-linux/util-linux_2.34-0.1ubuntu9.6.debian.tar.xz' util-linux_2.34-0.1ubuntu9.6.debian.tar.xz 102952 SHA512:94a75311c3aa74a62d76c372b8d15285c6e574f65d8de668d430a658f6ebc1d171683a40d855140e62901776b8de306a88790396a4c8ac8bfb81128f0ef2d198
```

### `dpkg` source package: `wcwidth=0.1.8+dfsg1-3`

Binary Packages:

- `python3-wcwidth=0.1.8+dfsg1-3`

Licenses: (parsed from: `/usr/share/doc/python3-wcwidth/copyright`)

- `Expat`

Source:

```console
$ apt-get source -qq --print-uris wcwidth=0.1.8+dfsg1-3
'http://archive.ubuntu.com/ubuntu/pool/main/w/wcwidth/wcwidth_0.1.8%2bdfsg1-3.dsc' wcwidth_0.1.8+dfsg1-3.dsc 2288 SHA256:c3f0f96b3740fe4a05f922c8770eee136ff935fa6ed219632e1c908d5892c158
'http://archive.ubuntu.com/ubuntu/pool/main/w/wcwidth/wcwidth_0.1.8%2bdfsg1.orig.tar.xz' wcwidth_0.1.8+dfsg1.orig.tar.xz 10984 SHA256:e5c72c18558812dab3a5fb48efacf53bdb1a4b804095652446df177aa1d13817
'http://archive.ubuntu.com/ubuntu/pool/main/w/wcwidth/wcwidth_0.1.8%2bdfsg1-3.debian.tar.xz' wcwidth_0.1.8+dfsg1-3.debian.tar.xz 3684 SHA256:aac20871ac07b01486ce5ed1c225744a4b659e91a6884d1950d080e53e38d9d6
```

### `dpkg` source package: `xml-core=0.18+nmu1`

Binary Packages:

- `xml-core=0.18+nmu1`

Licenses: (parsed from: `/usr/share/doc/xml-core/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris xml-core=0.18+nmu1
'http://archive.ubuntu.com/ubuntu/pool/main/x/xml-core/xml-core_0.18%2bnmu1.dsc' xml-core_0.18+nmu1.dsc 1632 SHA256:3b4bc034193f99750141611ae1c836c6b742c88ed0af1420051f3fcae30bf5ae
'http://archive.ubuntu.com/ubuntu/pool/main/x/xml-core/xml-core_0.18%2bnmu1.tar.xz' xml-core_0.18+nmu1.tar.xz 21312 SHA256:3e07592404b8ac38924fb650227cf5c9dcfc9933bd632eb4430635cd54898471
```

### `dpkg` source package: `xorg=1:7.7+19ubuntu14`

Binary Packages:

- `x11-common=1:7.7+19ubuntu14`

Licenses: (parsed from: `/usr/share/doc/x11-common/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris xorg=1:7.7+19ubuntu14
'http://archive.ubuntu.com/ubuntu/pool/main/x/xorg/xorg_7.7%2b19ubuntu14.dsc' xorg_7.7+19ubuntu14.dsc 2107 SHA256:d9d6449510066c3b34216cf08f797f00f64df3494567b5478a60d0feb50b9d95
'http://archive.ubuntu.com/ubuntu/pool/main/x/xorg/xorg_7.7%2b19ubuntu14.tar.gz' xorg_7.7+19ubuntu14.tar.gz 299269 SHA256:b8a1c0f7b24ae5565f6f22ccf01cd0c8e46c4f5dad6c14bce4f3495e82138213
```

### `dpkg` source package: `xz-utils=5.2.4-1ubuntu1.1`

Binary Packages:

- `liblzma5:amd64=5.2.4-1ubuntu1.1`
- `xz-utils=5.2.4-1ubuntu1.1`

Licenses: (parsed from: `/usr/share/doc/liblzma5/copyright`, `/usr/share/doc/xz-utils/copyright`)

- `Autoconf`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `LGPL-2`
- `LGPL-2.1`
- `LGPL-2.1+`
- `PD`
- `PD-debian`
- `config-h`
- `noderivs`
- `none`
- `permissive-fsf`
- `permissive-nowarranty`
- `probably-PD`

Source:

```console
$ apt-get source -qq --print-uris xz-utils=5.2.4-1ubuntu1.1
'http://archive.ubuntu.com/ubuntu/pool/main/x/xz-utils/xz-utils_5.2.4-1ubuntu1.1.dsc' xz-utils_5.2.4-1ubuntu1.1.dsc 2604 SHA512:458e4bd7a0823dc7e5f1dcf11bd4d0653b5c3f2474835a8422918faa25ab5b5ad005aa42af70bb9a993480ae1fe4e787965b19bd2ba4bee2ddedcaa24c10376c
'http://archive.ubuntu.com/ubuntu/pool/main/x/xz-utils/xz-utils_5.2.4.orig.tar.xz' xz-utils_5.2.4.orig.tar.xz 1053868 SHA512:00db7dd31a61541b1ce6946e0f21106f418dd1ac3f27cdb8682979cbc3bd777cd6dd1f04f9ba257a0a7e24041e15ca40d0dd5c130380dce62280af67a0beb97f
'http://archive.ubuntu.com/ubuntu/pool/main/x/xz-utils/xz-utils_5.2.4.orig.tar.xz.asc' xz-utils_5.2.4.orig.tar.xz.asc 879 SHA512:dbfce0556bc85545ce3566a01c25e4876f560409fc2d48f2dc382b10fbd2538c61d8f2c3667d86fc7313aec86c05e53926015000320f19615e97875adae42450
'http://archive.ubuntu.com/ubuntu/pool/main/x/xz-utils/xz-utils_5.2.4-1ubuntu1.1.debian.tar.xz' xz-utils_5.2.4-1ubuntu1.1.debian.tar.xz 136944 SHA512:627df70d2ff3b0227d6dd74137a660c5d722cce059ee36c1db8a50105ba6c236910bba5687290a7d88c9a53ead2a3b3ab00216f279f26a57d7e4020c6db23a24
```

### `dpkg` source package: `zlib=1:1.2.11.dfsg-2ubuntu1.5`

Binary Packages:

- `zlib1g:amd64=1:1.2.11.dfsg-2ubuntu1.5`
- `zlib1g-dev:amd64=1:1.2.11.dfsg-2ubuntu1.5`

Licenses: (parsed from: `/usr/share/doc/zlib1g/copyright`, `/usr/share/doc/zlib1g-dev/copyright`)

- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris zlib=1:1.2.11.dfsg-2ubuntu1.5
'http://archive.ubuntu.com/ubuntu/pool/main/z/zlib/zlib_1.2.11.dfsg-2ubuntu1.5.dsc' zlib_1.2.11.dfsg-2ubuntu1.5.dsc 2649 SHA512:f28659c4389c08be0023850921a9a7fb29d5c1d79429fe2a4a754209102aa48e84835006bd79dfa5943ef8319969fa549a50668db10d22c37c46082cc58969d4
'http://archive.ubuntu.com/ubuntu/pool/main/z/zlib/zlib_1.2.11.dfsg.orig.tar.gz' zlib_1.2.11.dfsg.orig.tar.gz 370248 SHA512:92819807c0b8de655021bb2d5d182f9b6b381d3072d8c8dc1df34bbaa25d36bcba140c85f754a43cc466aac65850b7a7366aa0c93e804180e5b255e61d5748de
'http://archive.ubuntu.com/ubuntu/pool/main/z/zlib/zlib_1.2.11.dfsg-2ubuntu1.5.debian.tar.xz' zlib_1.2.11.dfsg-2ubuntu1.5.debian.tar.xz 56436 SHA512:f6e3a370612f2a836c36f674e7647dc6cf339bf698648a3630c9b71515d317f846345c9d0db6e1c73e627ce239245a24083e705b8dfe3baece638bb3f5c0b195
```
