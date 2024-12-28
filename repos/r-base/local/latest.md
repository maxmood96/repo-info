# `r-base:4.4.2`

## Docker Metadata

- Image ID: `sha256:7739708d29e9633074aabd03059e9b3c2afbbe3489d3fc1d1acf7c96d238aea9`
- Created: `2024-11-01T03:11:38Z`
- Virtual Size: ~ 863.92 Mb  
  (total size of all layers on-disk)
- Arch: `linux`/`amd64`
- Command: `["R"]`
- Environment:
  - `PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin`
  - `LC_ALL=en_US.UTF-8`
  - `LANG=en_US.UTF-8`
  - `R_BASE_VERSION=4.4.2`
- Labels:
  - `org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>`
  - `org.opencontainers.image.licenses=GPL-2.0-or-later`
  - `org.opencontainers.image.source=https://github.com/rocker-org/rocker`
  - `org.opencontainers.image.vendor=Rocker Project`

## `dpkg` (`.deb`-based packages)

### `dpkg` source package: `acl=2.3.2-2`

Binary Packages:

- `libacl1:amd64=2.3.2-2+b1`

Licenses: (parsed from: `/usr/share/doc/libacl1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2+`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris acl=2.3.2-2
'http://http.debian.net/debian/pool/main/a/acl/acl_2.3.2-2.dsc' acl_2.3.2-2.dsc 2604 SHA256:1f42130ccb5442fe2db2aee1dcc03c51a31512dd2519a38e8fc9270c5abbc807
'http://http.debian.net/debian/pool/main/a/acl/acl_2.3.2.orig.tar.xz' acl_2.3.2.orig.tar.xz 371680 SHA256:97203a72cae99ab89a067fe2210c1cbf052bc492b479eca7d226d9830883b0bd
'http://http.debian.net/debian/pool/main/a/acl/acl_2.3.2.orig.tar.xz.asc' acl_2.3.2.orig.tar.xz.asc 833 SHA256:184c6a903490885a096095db67b433a04542c6569f167cbe8115268c0f227273
'http://http.debian.net/debian/pool/main/a/acl/acl_2.3.2-2.debian.tar.xz' acl_2.3.2-2.debian.tar.xz 24296 SHA256:e27b6e194c0a7554595d76f96acdceb800631bdc46c36457b73bc7e4a0c5f2ee
```

### `dpkg` source package: `apt=2.9.17`

Binary Packages:

- `apt=2.9.17`
- `libapt-pkg6.0t64:amd64=2.9.17`

Licenses: (parsed from: `/usr/share/doc/apt/copyright`, `/usr/share/doc/libapt-pkg6.0t64/copyright`)

- `BSD-3-clause`
- `Expat`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris apt=2.9.17
'http://deb.debian.org/debian/pool/main/a/apt/apt_2.9.17.dsc' apt_2.9.17.dsc 3003 SHA256:e982849d9e091ba1dc331b6833a53b7b7f7e0b412e213936a012da501a29c0bf
'http://deb.debian.org/debian/pool/main/a/apt/apt_2.9.17.tar.xz' apt_2.9.17.tar.xz 2390108 SHA256:30a0f5bb66e50e66355eaa810097192f977dfeb5c2aa57b9c4f59870be7b0d04
```

Other potentially useful URLs:

- https://sources.debian.net/src/apt/2.9.17/ (for browsing the source)
- https://sources.debian.net/src/apt/2.9.17/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/apt/2.9.17/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `attr=1:2.5.2-2`

Binary Packages:

- `libattr1:amd64=1:2.5.2-2`

Licenses: (parsed from: `/usr/share/doc/libattr1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2+`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris attr=1:2.5.2-2
'http://http.debian.net/debian/pool/main/a/attr/attr_2.5.2-2.dsc' attr_2.5.2-2.dsc 2576 SHA256:814f167854daf20640bf4d83aa086135000e31f355d69711ef611235b7b999ac
'http://http.debian.net/debian/pool/main/a/attr/attr_2.5.2.orig.tar.xz' attr_2.5.2.orig.tar.xz 334180 SHA256:f2e97b0ab7ce293681ab701915766190d607a1dba7fae8a718138150b700a70b
'http://http.debian.net/debian/pool/main/a/attr/attr_2.5.2.orig.tar.xz.asc' attr_2.5.2.orig.tar.xz.asc 833 SHA256:eeac729088d3c6379e91b7596cb3582e46b047c47f0fa3c5c77f9c9e84dc3a4c
'http://http.debian.net/debian/pool/main/a/attr/attr_2.5.2-2.debian.tar.xz' attr_2.5.2-2.debian.tar.xz 26592 SHA256:23c0ad870c6f6a75080d11b66e07cdb9db95805d61e218dc30f070d2f001ab9b
```

### `dpkg` source package: `audit=1:4.0.2-2`

Binary Packages:

- `libaudit-common=1:4.0.2-2`
- `libaudit1:amd64=1:4.0.2-2`

Licenses: (parsed from: `/usr/share/doc/libaudit-common/copyright`, `/usr/share/doc/libaudit1/copyright`)

- `GPL-1`
- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris audit=1:4.0.2-2
'http://http.debian.net/debian/pool/main/a/audit/audit_4.0.2-2.dsc' audit_4.0.2-2.dsc 2408 SHA256:d0b9457933409cd3287bc0b8bfb10f41c08fb5b24bd5c5b8364125d5a6894974
'http://http.debian.net/debian/pool/main/a/audit/audit_4.0.2.orig.tar.gz' audit_4.0.2.orig.tar.gz 1198769 SHA256:d5d1b5d50ee4a2d0d17875bc6ae6bd6a7d5b34d9557ea847a39faec531faaa0a
'http://http.debian.net/debian/pool/main/a/audit/audit_4.0.2-2.debian.tar.xz' audit_4.0.2-2.debian.tar.xz 19228 SHA256:33030d53299c57cda73e9e45813b8488f9bc3ad8992aef0b740afabbf66a2ba2
```

### `dpkg` source package: `base-files=13.6`

Binary Packages:

- `base-files=13.6`

Licenses: (parsed from: `/usr/share/doc/base-files/copyright`)

- `GPL`
- `GPL-2+`
- `verbatim`

Source:

```console
$ apt-get source -qq --print-uris base-files=13.6
'http://http.debian.net/debian/pool/main/b/base-files/base-files_13.6.dsc' base-files_13.6.dsc 1100 SHA256:f5fd18c61694f108b0f6fe0387d89c5eb581fb445db6253fac5f27eb26779d37
'http://http.debian.net/debian/pool/main/b/base-files/base-files_13.6.tar.xz' base-files_13.6.tar.xz 68264 SHA256:ebe8647287f951ebf5f6ac94067a4cf14bf61752ca0ecc342245d13b1c520258
```

### `dpkg` source package: `base-passwd=3.6.5`

Binary Packages:

- `base-passwd=3.6.5`

Licenses: (parsed from: `/usr/share/doc/base-passwd/copyright`)

- `GPL-2`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris base-passwd=3.6.5
'http://http.debian.net/debian/pool/main/b/base-passwd/base-passwd_3.6.5.dsc' base-passwd_3.6.5.dsc 1762 SHA256:18802a37a5b32e5271e27512f3017c9aaf91497e96517fa5c586a50b03c71f6c
'http://http.debian.net/debian/pool/main/b/base-passwd/base-passwd_3.6.5.tar.xz' base-passwd_3.6.5.tar.xz 60064 SHA256:bd30ab67b1f8029d3e70d3419e5033fb4595ab91c91307c3b7c00978e8d111b2
```

### `dpkg` source package: `bash=5.2.37-1`

Binary Packages:

- `bash=5.2.37-1`

Licenses: (parsed from: `/usr/share/doc/bash/copyright`)

- `BSD-4-clause-UC`
- `GFDL-1.3`
- `GFDL-NIV-1.3`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `GPL-3+ with Bison exception`
- `Latex2e`
- `MIT-like`
- `permissive`

Source:

```console
$ apt-get source -qq --print-uris bash=5.2.37-1
'http://http.debian.net/debian/pool/main/b/bash/bash_5.2.37-1.dsc' bash_5.2.37-1.dsc 2294 SHA256:b278d0b2286838ffaa2b6529306625337404cd1ae6b52e9db7e54282462c0e5e
'http://http.debian.net/debian/pool/main/b/bash/bash_5.2.37.orig.tar.xz' bash_5.2.37.orig.tar.xz 5600932 SHA256:370704c9c859f4060b7df19055e43bb9b5fa09d887699cf6ba87885c5485d36a
'http://http.debian.net/debian/pool/main/b/bash/bash_5.2.37-1.debian.tar.xz' bash_5.2.37-1.debian.tar.xz 88276 SHA256:262083ffaddbe164060c03df7316fa1eca817443f56a652bb807cd2f9f365c74
```

### `dpkg` source package: `binutils=2.43.50.20241221-1`

Binary Packages:

- `binutils=2.43.50.20241221-1`
- `binutils-common:amd64=2.43.50.20241221-1`
- `binutils-x86-64-linux-gnu=2.43.50.20241221-1`
- `libbinutils:amd64=2.43.50.20241221-1`
- `libctf-nobfd0:amd64=2.43.50.20241221-1`
- `libctf0:amd64=2.43.50.20241221-1`
- `libgprofng0:amd64=2.43.50.20241221-1`
- `libsframe1:amd64=2.43.50.20241221-1`

Licenses: (parsed from: `/usr/share/doc/binutils/copyright`, `/usr/share/doc/binutils-common/copyright`, `/usr/share/doc/binutils-x86-64-linux-gnu/copyright`, `/usr/share/doc/libbinutils/copyright`, `/usr/share/doc/libctf-nobfd0/copyright`, `/usr/share/doc/libctf0/copyright`, `/usr/share/doc/libgprofng0/copyright`, `/usr/share/doc/libsframe1/copyright`)

- `GFDL`
- `GPL`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris binutils=2.43.50.20241221-1
'http://http.debian.net/debian/pool/main/b/binutils/binutils_2.43.50.20241221-1.dsc' binutils_2.43.50.20241221-1.dsc 11358 SHA256:aeadff5e2005516323b10821c103067648899ad65561050e4a8c43eda1ff0707
'http://http.debian.net/debian/pool/main/b/binutils/binutils_2.43.50.20241221.orig.tar.xz' binutils_2.43.50.20241221.orig.tar.xz 24064816 SHA256:f05cd50497fb19149e7b32c5073ee62577bcc24e9173192f314c8bbb088fdf46
'http://http.debian.net/debian/pool/main/b/binutils/binutils_2.43.50.20241221-1.debian.tar.xz' binutils_2.43.50.20241221-1.debian.tar.xz 125032 SHA256:9db056ebff16eccc35c35ff861801322ff7ace1536438ea938b129e1b1f09222
```

### `dpkg` source package: `boot=1.3-31-1`

Binary Packages:

- `r-cran-boot=1.3-31-1`

Licenses: (parsed from: `/usr/share/doc/r-cran-boot/copyright`)

- `'unlimited distribution'`

Source:

```console
$ apt-get source -qq --print-uris boot=1.3-31-1
'http://http.debian.net/debian/pool/main/b/boot/boot_1.3-31-1.dsc' boot_1.3-31-1.dsc 1802 SHA256:15bdbf98a606f95343f3de7e723bb5ad4e755c4e2fcb9f87fa71796129952aee
'http://http.debian.net/debian/pool/main/b/boot/boot_1.3-31.orig.tar.gz' boot_1.3-31.orig.tar.gz 238458 SHA256:d8542e8cd1b503ca412e774908f386c0522a991296d57560ebded0f3d201c8d2
'http://http.debian.net/debian/pool/main/b/boot/boot_1.3-31-1.debian.tar.xz' boot_1.3-31-1.debian.tar.xz 5432 SHA256:30e2ef6fd66cb3ea1605071f003180650dac54f84ab25ec664e6a8fc57e57891
```

### `dpkg` source package: `brotli=1.1.0-2`

Binary Packages:

- `libbrotli1:amd64=1.1.0-2+b6`

Licenses: (parsed from: `/usr/share/doc/libbrotli1/copyright`)

- `MIT`

Source:

```console
$ apt-get source -qq --print-uris brotli=1.1.0-2
'http://http.debian.net/debian/pool/main/b/brotli/brotli_1.1.0-2.dsc' brotli_1.1.0-2.dsc 2261 SHA256:39b06802a852629132d549a7f7449dee7f435e801706714a4bc2ea2f15b28f36
'http://http.debian.net/debian/pool/main/b/brotli/brotli_1.1.0.orig.tar.gz' brotli_1.1.0.orig.tar.gz 512036 SHA256:10973f4b4199eafa1d5735ef661ddb2ec2f97319ee9fd1824d4aabe08cff5265
'http://http.debian.net/debian/pool/main/b/brotli/brotli_1.1.0-2.debian.tar.xz' brotli_1.1.0-2.debian.tar.xz 5480 SHA256:3d913a3740bcad9a294007575a6beb1846beadbd62b44fb2bf9fdaeddea3236f
```

### `dpkg` source package: `build-essential=12.12`

Binary Packages:

- `build-essential=12.12`

Licenses: (parsed from: `/usr/share/doc/build-essential/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris build-essential=12.12
'http://http.debian.net/debian/pool/main/b/build-essential/build-essential_12.12.dsc' build-essential_12.12.dsc 2259 SHA256:c947434e212c70963a1767c492b2a098fa2389bf6ce1b0be2a8971dead43a255
'http://http.debian.net/debian/pool/main/b/build-essential/build-essential_12.12.tar.xz' build-essential_12.12.tar.xz 51772 SHA256:091efa279e3a3609c4b013cf123ff4d7ec105f7df7b759e09ea93047039c2110
```

### `dpkg` source package: `bzip2=1.0.8-6`

Binary Packages:

- `bzip2=1.0.8-6`
- `libbz2-1.0:amd64=1.0.8-6`
- `libbz2-dev:amd64=1.0.8-6`

Licenses: (parsed from: `/usr/share/doc/bzip2/copyright`, `/usr/share/doc/libbz2-1.0/copyright`, `/usr/share/doc/libbz2-dev/copyright`)

- `BSD-variant`
- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris bzip2=1.0.8-6
'http://http.debian.net/debian/pool/main/b/bzip2/bzip2_1.0.8-6.dsc' bzip2_1.0.8-6.dsc 1604 SHA256:cd3bfd77254a6b5ef1be144bdc90a0dd374bc8206afd98ba4abf828741b79820
'http://http.debian.net/debian/pool/main/b/bzip2/bzip2_1.0.8.orig.tar.gz' bzip2_1.0.8.orig.tar.gz 810029 SHA256:ab5a03176ee106d3f0fa90e381da478ddae405918153cca248e682cd0c4a2269
'http://http.debian.net/debian/pool/main/b/bzip2/bzip2_1.0.8-6.debian.tar.bz2' bzip2_1.0.8-6.debian.tar.bz2 26991 SHA256:648ed0dac9a041ba6951e0cca521628aa39947cefee78139f7b934a5dc502095
```

### `dpkg` source package: `ca-certificates=20240203`

Binary Packages:

- `ca-certificates=20240203`

Licenses: (parsed from: `/usr/share/doc/ca-certificates/copyright`)

- `GPL-2`
- `GPL-2+`
- `MPL-2.0`

Source:

```console
$ apt-get source -qq --print-uris ca-certificates=20240203
'http://http.debian.net/debian/pool/main/c/ca-certificates/ca-certificates_20240203.dsc' ca-certificates_20240203.dsc 1766 SHA256:629afee9b327ce4df4ad0d77ad7b10383474a432e1af30516a7e81669420109b
'http://http.debian.net/debian/pool/main/c/ca-certificates/ca-certificates_20240203.tar.xz' ca-certificates_20240203.tar.xz 263276 SHA256:3286d3fc42c4d11b7086711a85f865b44065ce05cf1fb5376b2abed07622a9c6
```

### `dpkg` source package: `cairo=1.18.2-2`

Binary Packages:

- `libcairo2:amd64=1.18.2-2`

Licenses: (parsed from: `/usr/share/doc/libcairo2/copyright`)

- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris cairo=1.18.2-2
'http://http.debian.net/debian/pool/main/c/cairo/cairo_1.18.2-2.dsc' cairo_1.18.2-2.dsc 2763 SHA256:31a79f10ecd571d7c1f6fdc57940a92a3f87912aa727d095b8b80b94e8c66d6f
'http://http.debian.net/debian/pool/main/c/cairo/cairo_1.18.2.orig.tar.xz' cairo_1.18.2.orig.tar.xz 32574256 SHA256:a62b9bb42425e844cc3d6ddde043ff39dbabedd1542eba57a2eb79f85889d45a
'http://http.debian.net/debian/pool/main/c/cairo/cairo_1.18.2-2.debian.tar.xz' cairo_1.18.2-2.debian.tar.xz 30396 SHA256:0ee2cd7c17803cbe8da585493e68a59019c001176e4ce02d14b1af197398b098
```

### `dpkg` source package: `cdebconf=0.274`

Binary Packages:

- `libdebconfclient0:amd64=0.274`

Licenses: (parsed from: `/usr/share/doc/libdebconfclient0/copyright`)

- `BSD-2-Clause`
- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris cdebconf=0.274
'http://http.debian.net/debian/pool/main/c/cdebconf/cdebconf_0.274.dsc' cdebconf_0.274.dsc 2707 SHA256:ec08db9e6d8cc24f7747ca2090701154a21115b45d2d31c938b9d6105552d691
'http://http.debian.net/debian/pool/main/c/cdebconf/cdebconf_0.274.tar.xz' cdebconf_0.274.tar.xz 284912 SHA256:5488e03ad1269a6b8fbc3427ad4cac305ac896c90e57cf11f882cceb3eecba10
```

### `dpkg` source package: `cluster=2.1.8-1`

Binary Packages:

- `r-cran-cluster=2.1.8-1`

Licenses: (parsed from: `/usr/share/doc/r-cran-cluster/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris cluster=2.1.8-1
'http://http.debian.net/debian/pool/main/c/cluster/cluster_2.1.8-1.dsc' cluster_2.1.8-1.dsc 1831 SHA256:1d37abd0cfd833260e2d229adf3eeb6d22fc770b49f06debbd7b724843b15a3b
'http://http.debian.net/debian/pool/main/c/cluster/cluster_2.1.8.orig.tar.gz' cluster_2.1.8.orig.tar.gz 371978 SHA256:c32a462e34694c99d58da953efa74882b5427f8c5db7cb226ae15c54ce6060ca
'http://http.debian.net/debian/pool/main/c/cluster/cluster_2.1.8-1.debian.tar.xz' cluster_2.1.8-1.debian.tar.xz 4388 SHA256:0eea61dc38e51718e050c9c127a4fcfa3aaa39f8834549e282069d0797acc8a5
```

### `dpkg` source package: `codetools=0.2-20-1`

Binary Packages:

- `r-cran-codetools=0.2-20-1`

Licenses: (parsed from: `/usr/share/doc/r-cran-codetools/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris codetools=0.2-20-1
'http://http.debian.net/debian/pool/main/c/codetools/codetools_0.2-20-1.dsc' codetools_0.2-20-1.dsc 1859 SHA256:298e275af68522d839af2738a384e20c7d6f094d30483c06ba089025c70dd76e
'http://http.debian.net/debian/pool/main/c/codetools/codetools_0.2-20.orig.tar.gz' codetools_0.2-20.orig.tar.gz 38683 SHA256:3be6f375ec178723ddfd559d1e8e85bfeee04a5fbaf9f53f2f844e1669fea863
'http://http.debian.net/debian/pool/main/c/codetools/codetools_0.2-20-1.debian.tar.xz' codetools_0.2-20-1.debian.tar.xz 2916 SHA256:b244f4268d17492bde7834747e48f92657ad8adc5fc69aa12757d988744a4700
```

### `dpkg` source package: `coreutils=9.5-1`

Binary Packages:

- `coreutils=9.5-1+b1`

Licenses: (parsed from: `/usr/share/doc/coreutils/copyright`)

- `BSD-4-clause-UC`
- `FSFULLR`
- `GFDL-1.3`
- `GFDL-NIV-1.3`
- `GPL-3`
- `GPL-3+`
- `ISC`

Source:

```console
$ apt-get source -qq --print-uris coreutils=9.5-1
'http://http.debian.net/debian/pool/main/c/coreutils/coreutils_9.5-1.dsc' coreutils_9.5-1.dsc 2104 SHA256:83558c321a5e7a39dcf538a5a425f03486fbd2e6d95941a17ed98d04ed5ea7af
'http://http.debian.net/debian/pool/main/c/coreutils/coreutils_9.5.orig.tar.xz' coreutils_9.5.orig.tar.xz 6007136 SHA256:cd328edeac92f6a665de9f323c93b712af1858bc2e0d88f3f7100469470a1b8a
'http://http.debian.net/debian/pool/main/c/coreutils/coreutils_9.5.orig.tar.xz.asc' coreutils_9.5.orig.tar.xz.asc 833 SHA256:b2843cd7c5972c7bc4d01fc34eb82e5a3ec84a199363288e3999304e3dddc805
'http://http.debian.net/debian/pool/main/c/coreutils/coreutils_9.5-1.debian.tar.xz' coreutils_9.5-1.debian.tar.xz 21768 SHA256:fe704f7ba9b23cbc857e755bd3ec987228166b1342c1651f04bd16649b71d84d
```

### `dpkg` source package: `curl=8.11.1-1`

Binary Packages:

- `libcurl4t64:amd64=8.11.1-1`

Licenses: (parsed from: `/usr/share/doc/libcurl4t64/copyright`)

- `BSD-3-Clause`
- `BSD-3-clause`
- `BSD-4-Clause-UC`
- `FSFULLR`
- `GPL-2`
- `GPL-2+ with Autoconf-data exception`
- `GPL-2+ with Libtool exception`
- `GPL-3+ with Autoconf-data exception`
- `ISC`
- `OLDAP-2.8`
- `X11`
- `curl`

Source:

```console
$ apt-get source -qq --print-uris curl=8.11.1-1
'http://http.debian.net/debian/pool/main/c/curl/curl_8.11.1-1.dsc' curl_8.11.1-1.dsc 3252 SHA256:6611dcd0c91d6dc8b4363b8a4472812a3044a04cba2304c64a0d1c6d06d91069
'http://http.debian.net/debian/pool/main/c/curl/curl_8.11.1.orig.tar.gz' curl_8.11.1.orig.tar.gz 4169067 SHA256:a889ac9dbba3644271bd9d1302b5c22a088893719b72be3487bc3d401e5c4e80
'http://http.debian.net/debian/pool/main/c/curl/curl_8.11.1.orig.tar.gz.asc' curl_8.11.1.orig.tar.gz.asc 484 SHA256:d6c44df0a8e6958ef8d38fceda44f219db666b8215da6b33dc7dda81fcfc696b
'http://http.debian.net/debian/pool/main/c/curl/curl_8.11.1-1.debian.tar.xz' curl_8.11.1-1.debian.tar.xz 53972 SHA256:511130b8192911c22e03832a005531dd8990d9f5821640b6bac12a750d54bf33
```

### `dpkg` source package: `cyrus-sasl2=2.1.28+dfsg1-8`

Binary Packages:

- `libsasl2-2:amd64=2.1.28+dfsg1-8`
- `libsasl2-modules-db:amd64=2.1.28+dfsg1-8`

Licenses: (parsed from: `/usr/share/doc/libsasl2-2/copyright`, `/usr/share/doc/libsasl2-modules-db/copyright`)

- `BSD-2-clause`
- `BSD-2.2-clause`
- `BSD-3-Clause-Attribution`
- `BSD-3-clause`
- `BSD-3-clause-JANET`
- `BSD-3-clause-PADL`
- `BSD-4-clause-UC`
- `FSFULLR`
- `GPL-3`
- `GPL-3+`
- `IBM-as-is`
- `MIT-CMU`
- `MIT-Export`
- `MIT-OpenVision`
- `OpenLDAP`
- `RSA-MD`

Source:

```console
$ apt-get source -qq --print-uris cyrus-sasl2=2.1.28+dfsg1-8
'http://http.debian.net/debian/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.28%2bdfsg1-8.dsc' cyrus-sasl2_2.1.28+dfsg1-8.dsc 3223 SHA256:7c886aa8944aa704d5b0dd5923471d10ec1408a766e2766da3d51ce41916cfb8
'http://http.debian.net/debian/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.28%2bdfsg1.orig.tar.xz' cyrus-sasl2_2.1.28+dfsg1.orig.tar.xz 794540 SHA256:e796a5d85d1a85e1b433d43504e467f9075c7ebc0b45730a3996cf11b1deada4
'http://http.debian.net/debian/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.28%2bdfsg1-8.debian.tar.xz' cyrus-sasl2_2.1.28+dfsg1-8.debian.tar.xz 98980 SHA256:21fbc554dbc7fef34307bcae76679d608e8fbe3d60727a4c61b9da2108194a27
```

### `dpkg` source package: `dash=0.5.12-9`

Binary Packages:

- `dash=0.5.12-9`

Licenses: (parsed from: `/usr/share/doc/dash/copyright`)

- `BSD-3-Clause`
- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris dash=0.5.12-9
'http://http.debian.net/debian/pool/main/d/dash/dash_0.5.12-9.dsc' dash_0.5.12-9.dsc 1455 SHA256:aa5165888c75a39ec70477132329c7583863ee9762b6d07dc71fa2a5cdb84783
'http://http.debian.net/debian/pool/main/d/dash/dash_0.5.12.orig.tar.gz' dash_0.5.12.orig.tar.gz 246054 SHA256:6a474ac46e8b0b32916c4c60df694c82058d3297d8b385b74508030ca4a8f28a
'http://http.debian.net/debian/pool/main/d/dash/dash_0.5.12-9.debian.tar.xz' dash_0.5.12-9.debian.tar.xz 40096 SHA256:b5314d8c6cafae389559d6101dea059426263c95020ef5c547a59bcf5c0af2cc
```

### `dpkg` source package: `db5.3=5.3.28+dfsg2-9`

Binary Packages:

- `libdb5.3t64:amd64=5.3.28+dfsg2-9`

Licenses: (parsed from: `/usr/share/doc/libdb5.3t64/copyright`)

- `Artistic`
- `BSD-3-clause`
- `BSD-3-clause-fjord`
- `GPL`
- `GPL-3`
- `MIT-old`
- `Ms-PL`
- `Sleepycat`
- `TCL-like`
- `X11`
- `zlib`

Source:

```console
$ apt-get source -qq --print-uris db5.3=5.3.28+dfsg2-9
'http://http.debian.net/debian/pool/main/d/db5.3/db5.3_5.3.28%2bdfsg2-9.dsc' db5.3_5.3.28+dfsg2-9.dsc 2373 SHA256:045f392c75dffc9d4f3bd44978b90ca8d45b935cf0ae4202bf79a760f2ce07b1
'http://http.debian.net/debian/pool/main/d/db5.3/db5.3_5.3.28%2bdfsg2.orig.tar.xz' db5.3_5.3.28+dfsg2.orig.tar.xz 21287688 SHA256:ad41b507415dec8316e828b2230242af2251d2c86eefa3c7aa9ef47c5239ef33
'http://http.debian.net/debian/pool/main/d/db5.3/db5.3_5.3.28%2bdfsg2-9.debian.tar.xz' db5.3_5.3.28+dfsg2-9.debian.tar.xz 36412 SHA256:21fe6ee0491c83d0c34fe52e0e0e423946172eff68262584a0cc8ef880c36b74
```

### `dpkg` source package: `debconf=1.5.87`

Binary Packages:

- `debconf=1.5.87`

Licenses: (parsed from: `/usr/share/doc/debconf/copyright`)

- `BSD-2-clause`

Source:

```console
$ apt-get source -qq --print-uris debconf=1.5.87
'http://deb.debian.org/debian/pool/main/d/debconf/debconf_1.5.87.dsc' debconf_1.5.87.dsc 2035 SHA256:f46059b530efcb86082ee703225356869727e25babf9c3ad0c4a2e48f87e2977
'http://deb.debian.org/debian/pool/main/d/debconf/debconf_1.5.87.tar.xz' debconf_1.5.87.tar.xz 574232 SHA256:2b813be2ab3904a9194a07f2d97ab8e1d79c47ec2ca2f6a1f238c3cb4ff31c66
```

Other potentially useful URLs:

- https://sources.debian.net/src/debconf/1.5.87/ (for browsing the source)
- https://sources.debian.net/src/debconf/1.5.87/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/debconf/1.5.87/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `debian-archive-keyring=2023.4`

Binary Packages:

- `debian-archive-keyring=2023.4`

Licenses: (parsed from: `/usr/share/doc/debian-archive-keyring/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris debian-archive-keyring=2023.4
'http://http.debian.net/debian/pool/main/d/debian-archive-keyring/debian-archive-keyring_2023.4.dsc' debian-archive-keyring_2023.4.dsc 1261 SHA256:c97d048486078fcc6866a477df83b19270ae872102f4ed64b5a5e9995ff79afa
'http://http.debian.net/debian/pool/main/d/debian-archive-keyring/debian-archive-keyring_2023.4.tar.xz' debian-archive-keyring_2023.4.tar.xz 177568 SHA256:7f9b64d7c5e748b0cb99fd0674d872111c219e119f296912c59fc61ab49bb78a
```

### `dpkg` source package: `debianutils=5.21`

Binary Packages:

- `debianutils=5.21`

Licenses: (parsed from: `/usr/share/doc/debianutils/copyright`)

- `GPL-2`
- `GPL-2+`
- `SMAIL-GPL`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris debianutils=5.21
'http://http.debian.net/debian/pool/main/d/debianutils/debianutils_5.21.dsc' debianutils_5.21.dsc 1631 SHA256:9e26a955c62d09a9401aeb53cb190eca078b2cc13ea33ec874e944e95c21935e
'http://http.debian.net/debian/pool/main/d/debianutils/debianutils_5.21.tar.xz' debianutils_5.21.tar.xz 81916 SHA256:0053dcfd89e5c7dbfb2632450c00af6b8a646eeaaf185bbc8f2915488f994fe5
```

### `dpkg` source package: `diffutils=1:3.10-1`

Binary Packages:

- `diffutils=1:3.10-1`

Licenses: (parsed from: `/usr/share/doc/diffutils/copyright`)

- `FSFAP`
- `FSFULLR`
- `GFDL-1.3`
- `GFDL-NIV-1.3`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `GPL-3+ with autoconf exception`
- `GPL-3+ with texinfo exception`
- `LGPL-2`
- `LGPL-2.0+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`
- `LGPL-3.0+`
- `X11`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris diffutils=1:3.10-1
'http://http.debian.net/debian/pool/main/d/diffutils/diffutils_3.10-1.dsc' diffutils_3.10-1.dsc 1715 SHA256:f7542884c67d44f0af356c5365a3fef8a298f1fbcbebf9df81cfbc6d6937f05f
'http://http.debian.net/debian/pool/main/d/diffutils/diffutils_3.10.orig.tar.xz' diffutils_3.10.orig.tar.xz 1624240 SHA256:90e5e93cc724e4ebe12ede80df1634063c7a855692685919bfe60b556c9bd09e
'http://http.debian.net/debian/pool/main/d/diffutils/diffutils_3.10.orig.tar.xz.asc' diffutils_3.10.orig.tar.xz.asc 833 SHA256:a94faf8f1baa04ff220f7b2ccb137c16337284e023ebc4a1d5df475c08d810f7
'http://http.debian.net/debian/pool/main/d/diffutils/diffutils_3.10-1.debian.tar.xz' diffutils_3.10-1.debian.tar.xz 13952 SHA256:ebf51a7ceff8c882f997ca428232fd3b58ac59a70840c4b10f8fcfaa881598ce
```

### `dpkg` source package: `dpkg=1.22.11`

Binary Packages:

- `dpkg=1.22.11`
- `dpkg-dev=1.22.11`
- `libdpkg-perl=1.22.11`

Licenses: (parsed from: `/usr/share/doc/dpkg/copyright`, `/usr/share/doc/dpkg-dev/copyright`, `/usr/share/doc/libdpkg-perl/copyright`)

- `GPL-2`
- `GPL-2+`
- `public-domain-s-s-d`

Source:

```console
$ apt-get source -qq --print-uris dpkg=1.22.11
'http://http.debian.net/debian/pool/main/d/dpkg/dpkg_1.22.11.dsc' dpkg_1.22.11.dsc 3144 SHA256:d850ae15f8a43c981edaace2003f93d44f6f23666917bd26472f266d172a03fa
'http://http.debian.net/debian/pool/main/d/dpkg/dpkg_1.22.11.tar.xz' dpkg_1.22.11.tar.xz 5697040 SHA256:f318eb949b8e7ecd802b17b1a7e7cf4b17094c9577e1060653e9b838cdd31d80
```

### `dpkg` source package: `e2fsprogs=1.47.2~rc1-2`

Binary Packages:

- `e2fsprogs=1.47.2~rc1-2`
- `libcom-err2:amd64=1.47.2~rc1-2`
- `libext2fs2t64:amd64=1.47.2~rc1-2`
- `libss2:amd64=1.47.2~rc1-2`
- `logsave=1.47.2~rc1-2`

Licenses: (parsed from: `/usr/share/doc/e2fsprogs/copyright`, `/usr/share/doc/libcom-err2/copyright`, `/usr/share/doc/libext2fs2t64/copyright`, `/usr/share/doc/libss2/copyright`, `/usr/share/doc/logsave/copyright`)

- `0BSD`
- `Apache-2`
- `Apache-2.0`
- `BSD-3-Clause`
- `BSD-3-Clause-Variant`
- `BSD-4-Clause-CMU`
- `Expat`
- `GPL`
- `GPL-2`
- `GPL-2+`
- `GPL-2+ with Texinfo exception`
- `ISC`
- `Kazlib`
- `LGPL-2`
- `Latex2e`
- `MIT-US-export`

Source:

```console
$ apt-get source -qq --print-uris e2fsprogs=1.47.2~rc1-2
'http://http.debian.net/debian/pool/main/e/e2fsprogs/e2fsprogs_1.47.2%7erc1-2.dsc' e2fsprogs_1.47.2~rc1-2.dsc 3075 SHA256:fb57d921390560a0052c87caed8e1f5f66c42164862e588bc6c8263a85704ef7
'http://http.debian.net/debian/pool/main/e/e2fsprogs/e2fsprogs_1.47.2%7erc1.orig.tar.gz' e2fsprogs_1.47.2~rc1.orig.tar.gz 9963142 SHA256:4f8ce7e2b5053632e061dbf4c4271979f518c53fd2410f34e7878397b9e42160
'http://http.debian.net/debian/pool/main/e/e2fsprogs/e2fsprogs_1.47.2%7erc1.orig.tar.gz.asc' e2fsprogs_1.47.2~rc1.orig.tar.gz.asc 488 SHA256:da3519df23ec0db8383fa97bb6d4ab9d8ef8b77a594991ab93ec6a72028dac59
'http://http.debian.net/debian/pool/main/e/e2fsprogs/e2fsprogs_1.47.2%7erc1-2.debian.tar.xz' e2fsprogs_1.47.2~rc1-2.debian.tar.xz 95620 SHA256:bad108df28c67ae4abb82a6e57dbc47fec7bbed68621a898c9b6e44ceb130540
```

### `dpkg` source package: `ed=1.20.2-2`

Binary Packages:

- `ed=1.20.2-2`

Licenses: (parsed from: `/usr/share/doc/ed/copyright`)

- `BSD-2-Clause`
- `FCONF`
- `FDOC`
- `FLOG`
- `GFDL-1.3`
- `GFDL-NIV-1.3+`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris ed=1.20.2-2
'http://http.debian.net/debian/pool/main/e/ed/ed_1.20.2-2.dsc' ed_1.20.2-2.dsc 1832 SHA256:83505e343d10bf809b391b6296798a16d76eba8bcdf63239f28f5f7030bdbefd
'http://http.debian.net/debian/pool/main/e/ed/ed_1.20.2.orig.tar.gz' ed_1.20.2.orig.tar.gz 93153 SHA256:d45f9c4db61d6f5cf59f6daea118ed881976ec87742feae3cc35bffa7e99005f
'http://http.debian.net/debian/pool/main/e/ed/ed_1.20.2-2.debian.tar.xz' ed_1.20.2-2.debian.tar.xz 8652 SHA256:b3695b6d5a9cd8231897e362db22c77d129d72495513f8b65366b276de47f0f3
```

### `dpkg` source package: `expat=2.6.4-1`

Binary Packages:

- `libexpat1:amd64=2.6.4-1`

Licenses: (parsed from: `/usr/share/doc/libexpat1/copyright`)

- `MIT`

Source:

```console
$ apt-get source -qq --print-uris expat=2.6.4-1
'http://http.debian.net/debian/pool/main/e/expat/expat_2.6.4-1.dsc' expat_2.6.4-1.dsc 1964 SHA256:efcb13c3ce2a9426bca993176431353622712018b47c2e677f3db568745c9ded
'http://http.debian.net/debian/pool/main/e/expat/expat_2.6.4.orig.tar.gz' expat_2.6.4.orig.tar.gz 8419100 SHA256:372b18f6527d162fa9658f1c74d22a37429b82d822f5a1e1fc7e00f6045a06a2
'http://http.debian.net/debian/pool/main/e/expat/expat_2.6.4-1.debian.tar.xz' expat_2.6.4-1.debian.tar.xz 13124 SHA256:d58fe77a081ebd753c91d71f428c5081e5ec0d918bfaf6dfd19f7e0134b8dc95
```

### `dpkg` source package: `findutils=4.10.0-3`

Binary Packages:

- `findutils=4.10.0-3`

Licenses: (parsed from: `/usr/share/doc/findutils/copyright`)

- `BSD-3-clause`
- `FSFAP`
- `FSFULLR`
- `GFDL-1.3`
- `GFDL-NIV-1.3+`
- `GPL`
- `GPL with automake exception`
- `GPL-2`
- `GPL-2+`
- `GPL-2+ with Autoconf-data exception`
- `GPL-3`
- `GPL-3+`
- `GPL-3+ with Autoconf-data exception`
- `GPL-3+ with Bison-2.2 exception`
- `ISC`
- `LGPL`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`
- `LGPL-3+`
- `X11`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris findutils=4.10.0-3
'http://http.debian.net/debian/pool/main/f/findutils/findutils_4.10.0-3.dsc' findutils_4.10.0-3.dsc 2291 SHA256:fa6b67056d9e5b4d8edbfc8ab95ac15ac769b140284426973f6a1ef07a4594ec
'http://http.debian.net/debian/pool/main/f/findutils/findutils_4.10.0.orig.tar.xz' findutils_4.10.0.orig.tar.xz 2240712 SHA256:1387e0b67ff247d2abde998f90dfbf70c1491391a59ddfecb8ae698789f0a4f5
'http://http.debian.net/debian/pool/main/f/findutils/findutils_4.10.0.orig.tar.xz.asc' findutils_4.10.0.orig.tar.xz.asc 488 SHA256:7f53670eea6bd114e014571221eb652855c1129a3ed99f2a9257c2a313cc216f
'http://http.debian.net/debian/pool/main/f/findutils/findutils_4.10.0-3.debian.tar.xz' findutils_4.10.0-3.debian.tar.xz 33364 SHA256:7d19668508523a6fcfb7731f5646305a8b1a00a3105ee3f0a5f167adf93a8a46
```

### `dpkg` source package: `fontconfig=2.15.0-1.1`

Binary Packages:

- `fontconfig=2.15.0-1.1+b1`
- `fontconfig-config=2.15.0-1.1+b1`
- `libfontconfig1:amd64=2.15.0-1.1+b1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris fontconfig=2.15.0-1.1
'http://http.debian.net/debian/pool/main/f/fontconfig/fontconfig_2.15.0-1.1.dsc' fontconfig_2.15.0-1.1.dsc 2673 SHA256:8690eef21f60128a5a0bad56d8cd67fb19023f407b18cb3b14daef2a0af39277
'http://http.debian.net/debian/pool/main/f/fontconfig/fontconfig_2.15.0.orig.tar.xz' fontconfig_2.15.0.orig.tar.xz 1447820 SHA256:63a0658d0e06e0fa886106452b58ef04f21f58202ea02a94c39de0d3335d7c0e
'http://http.debian.net/debian/pool/main/f/fontconfig/fontconfig_2.15.0-1.1.debian.tar.xz' fontconfig_2.15.0-1.1.debian.tar.xz 59068 SHA256:1fa268da49c325269255072c504fd9f1d84a1410a301bf93ed980699de49a291
```

### `dpkg` source package: `foreign=0.8.87-1`

Binary Packages:

- `r-cran-foreign=0.8.87-1`

Licenses: (parsed from: `/usr/share/doc/r-cran-foreign/copyright`)

- `GPL`
- `GPL `

Source:

```console
$ apt-get source -qq --print-uris foreign=0.8.87-1
'http://http.debian.net/debian/pool/main/f/foreign/foreign_0.8.87-1.dsc' foreign_0.8.87-1.dsc 1838 SHA256:dc789ccaed136d7c6e4ea5dc818854f6964314dfcf25e2a6f58636277f213567
'http://http.debian.net/debian/pool/main/f/foreign/foreign_0.8.87.orig.tar.gz' foreign_0.8.87.orig.tar.gz 365280 SHA256:1a24acf4c8e87acc740599e950388b88e5beab7e54f699a015366fbd86db2856
'http://http.debian.net/debian/pool/main/f/foreign/foreign_0.8.87-1.debian.tar.xz' foreign_0.8.87-1.debian.tar.xz 4404 SHA256:4e2f2c6d374b6c1b0241fbbb99e0a72f8ef0bed81097bc1b690e1a4c87c016d2
```

### `dpkg` source package: `freetype=2.13.3+dfsg-1`

Binary Packages:

- `libfreetype6:amd64=2.13.3+dfsg-1`

Licenses: (parsed from: `/usr/share/doc/libfreetype6/copyright`)

- `BSD-3-Clause`
- `BSL-1.0`
- `Expat`
- `FSFAP`
- `FTL`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `MIT-Modern-Variant`
- `MIT-SMC`
- `OpenGroup-MIT`
- `Public-Domain`
- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris freetype=2.13.3+dfsg-1
'http://http.debian.net/debian/pool/main/f/freetype/freetype_2.13.3%2bdfsg-1.dsc' freetype_2.13.3+dfsg-1.dsc 3680 SHA256:122104ec96184391361f4ee9e5c70e83b05a5c0b90030f2b94befb0fad0664c3
'http://http.debian.net/debian/pool/main/f/freetype/freetype_2.13.3%2bdfsg.orig-ft2demos.tar.xz' freetype_2.13.3+dfsg.orig-ft2demos.tar.xz 342404 SHA256:8775e5ffded1a885ba2ccb3ea0e82c73306a03b764080c3e4c79da15b5c9a28a
'http://http.debian.net/debian/pool/main/f/freetype/freetype_2.13.3%2bdfsg.orig-ft2demos.tar.xz.asc' freetype_2.13.3+dfsg.orig-ft2demos.tar.xz.asc 833 SHA256:931bfa17e59c0ec7db391160f43977e0907f36ea3c39d7e6063731cd4612dd51
'http://http.debian.net/debian/pool/main/f/freetype/freetype_2.13.3%2bdfsg.orig-ft2docs.tar.xz' freetype_2.13.3+dfsg.orig-ft2docs.tar.xz 2173852 SHA256:b7b66149bea769e226fd3d6d1eee6160e5b6beb4249b088071434fbe85fd1070
'http://http.debian.net/debian/pool/main/f/freetype/freetype_2.13.3%2bdfsg.orig-ft2docs.tar.xz.asc' freetype_2.13.3+dfsg.orig-ft2docs.tar.xz.asc 833 SHA256:65c66aec6244d247540430b21d3e80b677f1361906347a5be7fad371d46655da
'http://http.debian.net/debian/pool/main/f/freetype/freetype_2.13.3%2bdfsg.orig.tar.xz' freetype_2.13.3+dfsg.orig.tar.xz 2201416 SHA256:686ec73cbf6783b245dd068a09ce807b729ac0f8a46dd70f7867923c32fdf4de
'http://http.debian.net/debian/pool/main/f/freetype/freetype_2.13.3%2bdfsg-1.debian.tar.xz' freetype_2.13.3+dfsg-1.debian.tar.xz 43904 SHA256:e2de836c8bb52c5a59173465bfddbf476a277f3f065ba322d111c5046ef8b8c8
```

### `dpkg` source package: `fribidi=1.0.16-1`

Binary Packages:

- `libfribidi0:amd64=1.0.16-1`

Licenses: (parsed from: `/usr/share/doc/libfribidi0/copyright`)

- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris fribidi=1.0.16-1
'http://http.debian.net/debian/pool/main/f/fribidi/fribidi_1.0.16-1.dsc' fribidi_1.0.16-1.dsc 2004 SHA256:10f003abcad934adde409c94f2780ec9638517dc1cc495b2a1df03a13c1d4315
'http://http.debian.net/debian/pool/main/f/fribidi/fribidi_1.0.16.orig.tar.xz' fribidi_1.0.16.orig.tar.xz 1098260 SHA256:1b1cde5b235d40479e91be2f0e88a309e3214c8ab470ec8a2744d82a5a9ea05c
'http://http.debian.net/debian/pool/main/f/fribidi/fribidi_1.0.16-1.debian.tar.xz' fribidi_1.0.16-1.debian.tar.xz 8928 SHA256:8d1cd7177a436b25ca8153e3dd2b9fb6da411a2c3cb0105eaadf4e42b777da6f
```

### `dpkg` source package: `gcc-14=14.2.0-11`

Binary Packages:

- `cpp-14=14.2.0-11`
- `cpp-14-x86-64-linux-gnu=14.2.0-11`
- `g++-14=14.2.0-11`
- `g++-14-x86-64-linux-gnu=14.2.0-11`
- `gcc-14=14.2.0-11`
- `gcc-14-base:amd64=14.2.0-11`
- `gcc-14-x86-64-linux-gnu=14.2.0-11`
- `gfortran-14=14.2.0-11`
- `gfortran-14-x86-64-linux-gnu=14.2.0-11`
- `libasan8:amd64=14.2.0-11`
- `libatomic1:amd64=14.2.0-11`
- `libcc1-0:amd64=14.2.0-11`
- `libgcc-14-dev:amd64=14.2.0-11`
- `libgcc-s1:amd64=14.2.0-11`
- `libgfortran-14-dev:amd64=14.2.0-11`
- `libgfortran5:amd64=14.2.0-11`
- `libgomp1:amd64=14.2.0-11`
- `libhwasan0:amd64=14.2.0-11`
- `libitm1:amd64=14.2.0-11`
- `liblsan0:amd64=14.2.0-11`
- `libquadmath0:amd64=14.2.0-11`
- `libstdc++-14-dev:amd64=14.2.0-11`
- `libstdc++6:amd64=14.2.0-11`
- `libtsan2:amd64=14.2.0-11`
- `libubsan1:amd64=14.2.0-11`

Licenses: (parsed from: `/usr/share/doc/cpp-14/copyright`, `/usr/share/doc/cpp-14-x86-64-linux-gnu/copyright`, `/usr/share/doc/g++-14/copyright`, `/usr/share/doc/g++-14-x86-64-linux-gnu/copyright`, `/usr/share/doc/gcc-14/copyright`, `/usr/share/doc/gcc-14-base/copyright`, `/usr/share/doc/gcc-14-x86-64-linux-gnu/copyright`, `/usr/share/doc/gfortran-14/copyright`, `/usr/share/doc/gfortran-14-x86-64-linux-gnu/copyright`, `/usr/share/doc/libasan8/copyright`, `/usr/share/doc/libatomic1/copyright`, `/usr/share/doc/libcc1-0/copyright`, `/usr/share/doc/libgcc-14-dev/copyright`, `/usr/share/doc/libgcc-s1/copyright`, `/usr/share/doc/libgfortran-14-dev/copyright`, `/usr/share/doc/libgfortran5/copyright`, `/usr/share/doc/libgomp1/copyright`, `/usr/share/doc/libhwasan0/copyright`, `/usr/share/doc/libitm1/copyright`, `/usr/share/doc/liblsan0/copyright`, `/usr/share/doc/libquadmath0/copyright`, `/usr/share/doc/libstdc++-14-dev/copyright`, `/usr/share/doc/libstdc++6/copyright`, `/usr/share/doc/libtsan2/copyright`, `/usr/share/doc/libubsan1/copyright`)

- `Artistic`
- `GFDL-1.2`
- `GPL`
- `GPL-3`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris gcc-14=14.2.0-11
'http://http.debian.net/debian/pool/main/g/gcc-14/gcc-14_14.2.0-11.dsc' gcc-14_14.2.0-11.dsc 47423 SHA256:56d568cc2f18349fffe94d45bd8737924950c9ee045b6445c878870a7aca4205
'http://http.debian.net/debian/pool/main/g/gcc-14/gcc-14_14.2.0.orig.tar.gz' gcc-14_14.2.0.orig.tar.gz 94299633 SHA256:e162a5ef3f0077ecae598c6556908d2ab80841532df3398072a96a6df6e6aa29
'http://http.debian.net/debian/pool/main/g/gcc-14/gcc-14_14.2.0-11.debian.tar.xz' gcc-14_14.2.0-11.debian.tar.xz 2464428 SHA256:fe73888417aa5079b21a51d329c25923c2ea7aceae3ac5946c941e4e189c3863
```

### `dpkg` source package: `gcc-defaults=1.220`

Binary Packages:

- `cpp=4:14.2.0-1`
- `cpp-x86-64-linux-gnu=4:14.2.0-1`
- `g++=4:14.2.0-1`
- `g++-x86-64-linux-gnu=4:14.2.0-1`
- `gcc=4:14.2.0-1`
- `gcc-x86-64-linux-gnu=4:14.2.0-1`
- `gfortran=4:14.2.0-1`
- `gfortran-x86-64-linux-gnu=4:14.2.0-1`

Licenses: (parsed from: `/usr/share/doc/cpp/copyright`, `/usr/share/doc/cpp-x86-64-linux-gnu/copyright`, `/usr/share/doc/g++/copyright`, `/usr/share/doc/g++-x86-64-linux-gnu/copyright`, `/usr/share/doc/gcc/copyright`, `/usr/share/doc/gcc-x86-64-linux-gnu/copyright`, `/usr/share/doc/gfortran/copyright`, `/usr/share/doc/gfortran-x86-64-linux-gnu/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris gcc-defaults=1.220
'http://http.debian.net/debian/pool/main/g/gcc-defaults/gcc-defaults_1.220.dsc' gcc-defaults_1.220.dsc 36895 SHA256:abfa2d362033435385e733f97d0cace1fbc917fd4160c81cc89abac38d3cdc37
'http://http.debian.net/debian/pool/main/g/gcc-defaults/gcc-defaults_1.220.tar.xz' gcc-defaults_1.220.tar.xz 54044 SHA256:d40fbdb57f351a58e050c3e1037201853e88e3f673242b62357dc20030ad4805
```

### `dpkg` source package: `gdbm=1.24-2`

Binary Packages:

- `libgdbm-compat4t64:amd64=1.24-2`
- `libgdbm6t64:amd64=1.24-2`

Licenses: (parsed from: `/usr/share/doc/libgdbm-compat4t64/copyright`, `/usr/share/doc/libgdbm6t64/copyright`)

- `GFDL-NIV-1.3+`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris gdbm=1.24-2
'http://http.debian.net/debian/pool/main/g/gdbm/gdbm_1.24-2.dsc' gdbm_1.24-2.dsc 2466 SHA256:28acecf1cf00240942833c04079a02bb4c199a48faa1f4ca90f0ea9b79dc5841
'http://http.debian.net/debian/pool/main/g/gdbm/gdbm_1.24.orig.tar.gz' gdbm_1.24.orig.tar.gz 1195931 SHA256:695e9827fdf763513f133910bc7e6cfdb9187943a4fec943e57449723d2b8dbf
'http://http.debian.net/debian/pool/main/g/gdbm/gdbm_1.24.orig.tar.gz.asc' gdbm_1.24.orig.tar.gz.asc 195 SHA256:8fb2f87e817ed6bd1d7ef2ab976f6a0046814a5ff28a06c521b796e0d3fd1226
'http://http.debian.net/debian/pool/main/g/gdbm/gdbm_1.24-2.debian.tar.xz' gdbm_1.24-2.debian.tar.xz 16880 SHA256:736d23450674c1bf0b03a2f65b83870b0801bc3747df3099df970c1479b0ab63
```

### `dpkg` source package: `glib2.0=2.82.4-1`

Binary Packages:

- `libglib2.0-0t64:amd64=2.82.4-1`

Licenses: (parsed from: `/usr/share/doc/libglib2.0-0t64/copyright`)

- `AFL-2.0`
- `Apache-2.0`
- `Apache-2.0 with LLVM exception`
- `CC-BY-SA-3.0`
- `CC0-1.0`
- `Expat`
- `FSFULLR`
- `GPL-2`
- `GPL-2+`
- `Iconv-PD`
- `Janik-permissive`
- `Kuchling-PD`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`
- `LGPL-3+`
- `MPL-1.1`
- `Mingw-PD`
- `Plumb-PD`
- `Unicode-DFS-2016`
- `bzip2-1.0.6`
- `cmph`
- `old-glib-tests`

Source:

```console
$ apt-get source -qq --print-uris glib2.0=2.82.4-1
'http://http.debian.net/debian/pool/main/g/glib2.0/glib2.0_2.82.4-1.dsc' glib2.0_2.82.4-1.dsc 4921 SHA256:ade70c1236a6c3878b68987bbeb420e1f65587e9e068bddd766445df647c2dd1
'http://http.debian.net/debian/pool/main/g/glib2.0/glib2.0_2.82.4.orig-unicode-data.tar.xz' glib2.0_2.82.4.orig-unicode-data.tar.xz 262908 SHA256:9bf66a7e9f2f18cbd7a72f561dc1f997990b53243435008777109c823cd7e1ea
'http://http.debian.net/debian/pool/main/g/glib2.0/glib2.0_2.82.4.orig.tar.xz' glib2.0_2.82.4.orig.tar.xz 5556896 SHA256:37dd0877fe964cd15e9a2710b044a1830fb1bd93652a6d0cb6b8b2dff187c709
'http://http.debian.net/debian/pool/main/g/glib2.0/glib2.0_2.82.4-1.debian.tar.xz' glib2.0_2.82.4-1.debian.tar.xz 135364 SHA256:26701ddce443871a59c59bab6b0a734d0dee29a6cbafee6792b00d9dd96a3083
```

### `dpkg` source package: `glibc=2.40-4`

Binary Packages:

- `libc-bin=2.40-4`
- `libc-dev-bin=2.40-4`
- `libc-l10n=2.40-4`
- `libc6:amd64=2.40-4`
- `libc6-dev:amd64=2.40-4`
- `locales=2.40-4`

Licenses: (parsed from: `/usr/share/doc/libc-bin/copyright`, `/usr/share/doc/libc-dev-bin/copyright`, `/usr/share/doc/libc-l10n/copyright`, `/usr/share/doc/libc6/copyright`, `/usr/share/doc/libc6-dev/copyright`, `/usr/share/doc/locales/copyright`)

- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris glibc=2.40-4
'http://http.debian.net/debian/pool/main/g/glibc/glibc_2.40-4.dsc' glibc_2.40-4.dsc 7550 SHA256:d0f6c6d2447a1a77dce87efa30a084e22c81ac9fe6f60def138b98b9938cb373
'http://http.debian.net/debian/pool/main/g/glibc/glibc_2.40.orig.tar.xz' glibc_2.40.orig.tar.xz 19517224 SHA256:0b89b8c058eaa0f1121a814be6196ce2048235b43d95714ce8278fe72c7cc34a
'http://http.debian.net/debian/pool/main/g/glibc/glibc_2.40-4.debian.tar.xz' glibc_2.40-4.debian.tar.xz 444396 SHA256:b8c69dbbac85c6cfbe3cee18b90c4363438e1f1140e36bc64e23fde4cb368820
```

### `dpkg` source package: `gmp=2:6.3.0+dfsg-3`

Binary Packages:

- `libgmp10:amd64=2:6.3.0+dfsg-3`

Licenses: (parsed from: `/usr/share/doc/libgmp10/copyright`)

- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `GPL-3+ with Bison exception`
- `LGPL-3`
- `LGPL-3+`

Source:

```console
$ apt-get source -qq --print-uris gmp=2:6.3.0+dfsg-3
'http://http.debian.net/debian/pool/main/g/gmp/gmp_6.3.0%2bdfsg-3.dsc' gmp_6.3.0+dfsg-3.dsc 2251 SHA256:f7b64af28f52b7346bb8581e01d3c19daf769639345f234f8ae1e29c42171443
'http://http.debian.net/debian/pool/main/g/gmp/gmp_6.3.0%2bdfsg.orig.tar.xz' gmp_6.3.0+dfsg.orig.tar.xz 1870556 SHA256:bd2966e6d277f79328e894a5a9f3ba3fbf2ed2be81def5f48623e30c23fb1572
'http://http.debian.net/debian/pool/main/g/gmp/gmp_6.3.0%2bdfsg-3.debian.tar.xz' gmp_6.3.0+dfsg-3.debian.tar.xz 19912 SHA256:1d890bbe25dd649d2ddba1926483176520e50f22115a00566f250b613b8c20ad
```

### `dpkg` source package: `gnupg2=2.2.45-2`

Binary Packages:

- `gpgv=2.2.45-2`

Licenses: (parsed from: `/usr/share/doc/gpgv/copyright`)

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
$ apt-get source -qq --print-uris gnupg2=2.2.45-2
'http://http.debian.net/debian/pool/main/g/gnupg2/gnupg2_2.2.45-2.dsc' gnupg2_2.2.45-2.dsc 3873 SHA256:27640274a66ba8449475377949a4e5fb5679293a8dbe5fff707d726c9bacfa5b
'http://http.debian.net/debian/pool/main/g/gnupg2/gnupg2_2.2.45.orig.tar.bz2' gnupg2_2.2.45.orig.tar.bz2 7447141 SHA256:d1abecd2b6c052749fd5748ba9de7021567e06b573dc6becac8df25cb87500e8
'http://http.debian.net/debian/pool/main/g/gnupg2/gnupg2_2.2.45.orig.tar.bz2.asc' gnupg2_2.2.45.orig.tar.bz2.asc 228 SHA256:4c70f582308e218bfd5ca3e4176d39c8fa15d39d3183c836daf13ab5371f68dd
'http://http.debian.net/debian/pool/main/g/gnupg2/gnupg2_2.2.45-2.debian.tar.xz' gnupg2_2.2.45-2.debian.tar.xz 141036 SHA256:28fb29abeed25c221ec7877f5f028fb972fe3d7cc26040d09bb84d72d2cc6280
```

### `dpkg` source package: `gnutls28=3.8.8-2`

Binary Packages:

- `libgnutls30t64:amd64=3.8.8-2`

Licenses: (parsed from: `/usr/share/doc/libgnutls30t64/copyright`)

- `Apache-2.0`
- `BSD-3-Clause`
- `CC0 license`
- `Expat`
- `FSFAP`
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
$ apt-get source -qq --print-uris gnutls28=3.8.8-2
'http://http.debian.net/debian/pool/main/g/gnutls28/gnutls28_3.8.8-2.dsc' gnutls28_3.8.8-2.dsc 3236 SHA256:b9166175cbd952f9d5ec0ee8868d49a3213f6646d64ade9416969dd4587eeb07
'http://http.debian.net/debian/pool/main/g/gnutls28/gnutls28_3.8.8.orig.tar.xz' gnutls28_3.8.8.orig.tar.xz 6696460 SHA256:ac4f020e583880b51380ed226e59033244bc536cad2623f2e26f5afa2939d8fb
'http://http.debian.net/debian/pool/main/g/gnutls28/gnutls28_3.8.8.orig.tar.xz.asc' gnutls28_3.8.8.orig.tar.xz.asc 854 SHA256:add4e5e0c1a4b5c7c870c0c0c0a328a6c579f6e1cd49577e90e26273e1b67473
'http://http.debian.net/debian/pool/main/g/gnutls28/gnutls28_3.8.8-2.debian.tar.xz' gnutls28_3.8.8-2.debian.tar.xz 77860 SHA256:058641644beb97899fc18558251e86ec314d2aaa8a995b96518f0ce3ef32a4e7
```

### `dpkg` source package: `graphite2=1.3.14-2`

Binary Packages:

- `libgraphite2-3:amd64=1.3.14-2+b1`

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
$ apt-get source -qq --print-uris graphite2=1.3.14-2
'http://http.debian.net/debian/pool/main/g/graphite2/graphite2_1.3.14-2.dsc' graphite2_1.3.14-2.dsc 2568 SHA256:98ee6be2e35e2a4f7dbc71a21315399d59c4f79339cb832c6caccf8f62342d26
'http://http.debian.net/debian/pool/main/g/graphite2/graphite2_1.3.14.orig.tar.gz' graphite2_1.3.14.orig.tar.gz 6629829 SHA256:7a3b342c5681921ce2e0c2496509d30b5b078399d5a7bd2358f95166d57d91df
'http://http.debian.net/debian/pool/main/g/graphite2/graphite2_1.3.14-2.debian.tar.xz' graphite2_1.3.14-2.debian.tar.xz 14168 SHA256:dc46cc532a54adfc7ed5798061795120325bf0722221b2a6299f49c403ee9cd4
```

### `dpkg` source package: `grep=3.11-4`

Binary Packages:

- `grep=3.11-4`

Licenses: (parsed from: `/usr/share/doc/grep/copyright`)

- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris grep=3.11-4
'http://http.debian.net/debian/pool/main/g/grep/grep_3.11-4.dsc' grep_3.11-4.dsc 1642 SHA256:dd6f8eb933bc05446e483f7792c8bf0a1aba9d498e65c6ccafe64e9bf27ac054
'http://http.debian.net/debian/pool/main/g/grep/grep_3.11.orig.tar.xz' grep_3.11.orig.tar.xz 1703776 SHA256:1db2aedde89d0dea42b16d9528f894c8d15dae4e190b59aecc78f5a951276eab
'http://http.debian.net/debian/pool/main/g/grep/grep_3.11.orig.tar.xz.asc' grep_3.11.orig.tar.xz.asc 833 SHA256:89ec23ffd59b68822732dc8204fc89883c3af30a90ae390feb94346d9d09a589
'http://http.debian.net/debian/pool/main/g/grep/grep_3.11-4.debian.tar.xz' grep_3.11-4.debian.tar.xz 20468 SHA256:f10394b7589c58ca7de4b580692b1b59431f898cb2068e86222c174e093fdf49
```

### `dpkg` source package: `gzip=1.12-1.2`

Binary Packages:

- `gzip=1.12-1.2`

Licenses: (parsed from: `/usr/share/doc/gzip/copyright`)

- `FSF-manpages`
- `GFDL-1.3+-no-invariant`
- `GFDL-3`
- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris gzip=1.12-1.2
'http://http.debian.net/debian/pool/main/g/gzip/gzip_1.12-1.2.dsc' gzip_1.12-1.2.dsc 2278 SHA256:4445d382766432e1b15f2bea0d7a4f2b3fbf886e88cfc6db4044b778b46df650
'http://http.debian.net/debian/pool/main/g/gzip/gzip_1.12.orig.tar.xz' gzip_1.12.orig.tar.xz 825548 SHA256:ce5e03e519f637e1f814011ace35c4f87b33c0bbabeec35baf5fbd3479e91956
'http://http.debian.net/debian/pool/main/g/gzip/gzip_1.12.orig.tar.xz.asc' gzip_1.12.orig.tar.xz.asc 833 SHA256:3ed9ab54452576e0be0d477c772c9f47baa36415133fef7dd1fcf7b15480ba32
'http://http.debian.net/debian/pool/main/g/gzip/gzip_1.12-1.2.debian.tar.xz' gzip_1.12-1.2.debian.tar.xz 19384 SHA256:afdc8cd336e5612658bd2ea029c6e215d5a2bc70c6fda24956bf554b33b147f8
```

### `dpkg` source package: `harfbuzz=10.1.0-1`

Binary Packages:

- `libharfbuzz0b:amd64=10.1.0-1`

Licenses: (parsed from: `/usr/share/doc/libharfbuzz0b/copyright`)

- `Apache-2.0`
- `CC0-1.0`
- `Expat`
- `FSFAP`
- `FSFUL`
- `FSFULLR`
- `GPL-2`
- `GPL-2+ with AutoConf exception`
- `GPL-2+ with Font exception`
- `GPL-2+ with LibTool exception`
- `GPL-3`
- `GPL-3+`
- `GPL-3+ with AutoConf exception`
- `ISC`
- `LGPL-2.1`
- `LGPL-2.1+`
- `MIT`
- `Monotype`
- `OFL-1.1`
- `UFL-1.0`
- `Unicode`

Source:

```console
$ apt-get source -qq --print-uris harfbuzz=10.1.0-1
'http://http.debian.net/debian/pool/main/h/harfbuzz/harfbuzz_10.1.0-1.dsc' harfbuzz_10.1.0-1.dsc 2864 SHA256:f6351b6b26cdb4e3e3146de03486a4e5fc730c3c07705beaced3620134757f1e
'http://http.debian.net/debian/pool/main/h/harfbuzz/harfbuzz_10.1.0.orig.tar.xz' harfbuzz_10.1.0.orig.tar.xz 17922136 SHA256:6ce3520f2d089a33cef0fc48321334b8e0b72141f6a763719aaaecd2779ecb82
'http://http.debian.net/debian/pool/main/h/harfbuzz/harfbuzz_10.1.0-1.debian.tar.xz' harfbuzz_10.1.0-1.debian.tar.xz 19928 SHA256:4ada493020259363ebecbd9f3f68055f884f8bf82365108ad5dd9ba790908d31
```

### `dpkg` source package: `hostname=3.25`

Binary Packages:

- `hostname=3.25`

Licenses: (parsed from: `/usr/share/doc/hostname/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris hostname=3.25
'http://http.debian.net/debian/pool/main/h/hostname/hostname_3.25.dsc' hostname_3.25.dsc 1519 SHA256:80aadf116c3423044be69a4cef8ba2766f412bd4d46a500aacb61f303c19c4ef
'http://http.debian.net/debian/pool/main/h/hostname/hostname_3.25.tar.xz' hostname_3.25.tar.xz 12804 SHA256:5bb5d1be011158090157c9e7587ae5606c262a5020ecdc5caac6686b9910592e
```

### `dpkg` source package: `icu=72.1-5`

Binary Packages:

- `icu-devtools=72.1-5+b1`
- `libicu-dev:amd64=72.1-5+b1`
- `libicu72:amd64=72.1-5+b1`

Licenses: (parsed from: `/usr/share/doc/icu-devtools/copyright`, `/usr/share/doc/libicu-dev/copyright`, `/usr/share/doc/libicu72/copyright`)

- `GPL-3`
- `MIT`

Source:

```console
$ apt-get source -qq --print-uris icu=72.1-5
'http://http.debian.net/debian/pool/main/i/icu/icu_72.1-5.dsc' icu_72.1-5.dsc 2239 SHA256:0059598c83340a461c89bf51affe20ae8f84431c0c1a39f1b8e9c80ee892cabc
'http://http.debian.net/debian/pool/main/i/icu/icu_72.1.orig.tar.gz' icu_72.1.orig.tar.gz 26303933 SHA256:a2d2d38217092a7ed56635e34467f92f976b370e20182ad325edea6681a71d68
'http://http.debian.net/debian/pool/main/i/icu/icu_72.1.orig.tar.gz.asc' icu_72.1.orig.tar.gz.asc 659 SHA256:87b6ff610d587292cec0444fa8cbbfb12994cb89bade40578f5ba6470de245c7
'http://http.debian.net/debian/pool/main/i/icu/icu_72.1-5.debian.tar.xz' icu_72.1-5.debian.tar.xz 62532 SHA256:fce0ce962faacae576d3312f2e421a17433e620994dcd1ea168cf4a48147303e
```

### `dpkg` source package: `init-system-helpers=1.67`

Binary Packages:

- `init-system-helpers=1.67`

Licenses: (parsed from: `/usr/share/doc/init-system-helpers/copyright`)

- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris init-system-helpers=1.67
'http://http.debian.net/debian/pool/main/i/init-system-helpers/init-system-helpers_1.67.dsc' init-system-helpers_1.67.dsc 2234 SHA256:26e89df8709f6af0bc7629df7d6ccd327227ab9be8788c9232ffe9b559a7e86d
'http://http.debian.net/debian/pool/main/i/init-system-helpers/init-system-helpers_1.67.tar.xz' init-system-helpers_1.67.tar.xz 45180 SHA256:3fa7f7f1cffd0300363b49062c953023705009640e50141b00362e9fb40c5556
```

### `dpkg` source package: `isl=0.27-1`

Binary Packages:

- `libisl23:amd64=0.27-1`

Licenses: (parsed from: `/usr/share/doc/libisl23/copyright`)

- `BSD-2-clause`
- `LGPL-2`
- `LGPL-2.1+`
- `MIT`

Source:

```console
$ apt-get source -qq --print-uris isl=0.27-1
'http://http.debian.net/debian/pool/main/i/isl/isl_0.27-1.dsc' isl_0.27-1.dsc 1829 SHA256:35ceb67dbb1b4098431b184e342143c2bd94c4a41ebfb3a983e3be31440b0453
'http://http.debian.net/debian/pool/main/i/isl/isl_0.27.orig.tar.xz' isl_0.27.orig.tar.xz 2056436 SHA256:6d8babb59e7b672e8cb7870e874f3f7b813b6e00e6af3f8b04f7579965643d5c
'http://http.debian.net/debian/pool/main/i/isl/isl_0.27-1.debian.tar.xz' isl_0.27-1.debian.tar.xz 24868 SHA256:1ac2e33075903489d4284ff4e86645405e68a282a80432ee4ee0c43397f59224
```

### `dpkg` source package: `jansson=2.14-2`

Binary Packages:

- `libjansson4:amd64=2.14-2+b3`

Licenses: (parsed from: `/usr/share/doc/libjansson4/copyright`)

- `Expat`

Source:

```console
$ apt-get source -qq --print-uris jansson=2.14-2
'http://http.debian.net/debian/pool/main/j/jansson/jansson_2.14-2.dsc' jansson_2.14-2.dsc 1980 SHA256:6296ddd9c0a022bd1b70074aefb171cfcdf5694a04ffd32b35fd66097621af87
'http://http.debian.net/debian/pool/main/j/jansson/jansson_2.14.orig.tar.gz' jansson_2.14.orig.tar.gz 141500 SHA256:c739578bf6b764aa0752db9a2fdadcfe921c78f1228c7ec0bb47fa804c55d17b
'http://http.debian.net/debian/pool/main/j/jansson/jansson_2.14-2.debian.tar.xz' jansson_2.14-2.debian.tar.xz 5428 SHA256:e89fe4fd8221f6934ddb50f2e7f8404311928d0e23e49a5599f3d3d14ee8cb88
```

### `dpkg` source package: `jbigkit=2.1-6.1`

Binary Packages:

- `libjbig0:amd64=2.1-6.1+b2`

Licenses: (parsed from: `/usr/share/doc/libjbig0/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris jbigkit=2.1-6.1
'http://http.debian.net/debian/pool/main/j/jbigkit/jbigkit_2.1-6.1.dsc' jbigkit_2.1-6.1.dsc 2089 SHA256:8dea586c47cb4b2436f77fd33ef4a702b9da936d74de8332a72a8ddbe8124e09
'http://http.debian.net/debian/pool/main/j/jbigkit/jbigkit_2.1.orig.tar.gz' jbigkit_2.1.orig.tar.gz 438710 SHA256:de7106b6bfaf495d6865c7dd7ac6ca1381bd12e0d81405ea81e7f2167263d932
'http://http.debian.net/debian/pool/main/j/jbigkit/jbigkit_2.1-6.1.debian.tar.xz' jbigkit_2.1-6.1.debian.tar.xz 9244 SHA256:c9ba99e84d18b1affdc97b26b625721ed06b41a92996d9b426b62c0dbe3868cd
```

### `dpkg` source package: `kernsmooth=2.23-24-1`

Binary Packages:

- `r-cran-kernsmooth=2.23-24-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris kernsmooth=2.23-24-1
'http://http.debian.net/debian/pool/main/k/kernsmooth/kernsmooth_2.23-24-1.dsc' kernsmooth_2.23-24-1.dsc 1891 SHA256:370bf641158785a92cf30b5476d7b4ec7abafe793f514b53cef7faf9a819124d
'http://http.debian.net/debian/pool/main/k/kernsmooth/kernsmooth_2.23-24.orig.tar.gz' kernsmooth_2.23-24.orig.tar.gz 26067 SHA256:d0b3ec39547ffd92565e91b0c3bb637f3b30e7a46afe416d8790b8c4f528ac5f
'http://http.debian.net/debian/pool/main/k/kernsmooth/kernsmooth_2.23-24-1.debian.tar.xz' kernsmooth_2.23-24-1.debian.tar.xz 3472 SHA256:3eb1235fa87c243ef68c3639da4800a7e11a5bfaa5791e52199e2d864141939e
```

### `dpkg` source package: `keyutils=1.6.3-4`

Binary Packages:

- `libkeyutils1:amd64=1.6.3-4`

Licenses: (parsed from: `/usr/share/doc/libkeyutils1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2`
- `LGPL-2+`

Source:

```console
$ apt-get source -qq --print-uris keyutils=1.6.3-4
'http://http.debian.net/debian/pool/main/k/keyutils/keyutils_1.6.3-4.dsc' keyutils_1.6.3-4.dsc 2193 SHA256:1943ee7376e7abedfebce2285c04a5c1d3062f63fce14ab2bcfbf65c52073b89
'http://http.debian.net/debian/pool/main/k/keyutils/keyutils_1.6.3.orig.tar.gz' keyutils_1.6.3.orig.tar.gz 137022 SHA256:a61d5706136ae4c05bd48f86186bcfdbd88dd8bd5107e3e195c924cfc1b39bb4
'http://http.debian.net/debian/pool/main/k/keyutils/keyutils_1.6.3-4.debian.tar.xz' keyutils_1.6.3-4.debian.tar.xz 13872 SHA256:d64f58058ba3f3776e068fdd4cddf9a7a81b19006563a1e8d10894d949923806
```

### `dpkg` source package: `krb5=1.21.3-3`

Binary Packages:

- `libgssapi-krb5-2:amd64=1.21.3-3`
- `libk5crypto3:amd64=1.21.3-3`
- `libkrb5-3:amd64=1.21.3-3`
- `libkrb5support0:amd64=1.21.3-3`

Licenses: (parsed from: `/usr/share/doc/libgssapi-krb5-2/copyright`, `/usr/share/doc/libk5crypto3/copyright`, `/usr/share/doc/libkrb5-3/copyright`, `/usr/share/doc/libkrb5support0/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris krb5=1.21.3-3
'http://http.debian.net/debian/pool/main/k/krb5/krb5_1.21.3-3.dsc' krb5_1.21.3-3.dsc 3381 SHA256:561af05f1e9c42ca9eab01eaa7ea6cd903494bb5b462917c8fff7d86bbedc872
'http://http.debian.net/debian/pool/main/k/krb5/krb5_1.21.3.orig.tar.gz' krb5_1.21.3.orig.tar.gz 9136145 SHA256:b7a4cd5ead67fb08b980b21abd150ff7217e85ea320c9ed0c6dadd304840ad35
'http://http.debian.net/debian/pool/main/k/krb5/krb5_1.21.3.orig.tar.gz.asc' krb5_1.21.3.orig.tar.gz.asc 833 SHA256:85047c935fe949ef2e275885451b168557b923dd13a5aab0ef8fe6acd27b94d7
'http://http.debian.net/debian/pool/main/k/krb5/krb5_1.21.3-3.debian.tar.xz' krb5_1.21.3-3.debian.tar.xz 103380 SHA256:c7b7bceb2f1bd782d0118904bded8ddaba1aaa54f1b3b2fc0dc3ecaeac450b5b
```

### `dpkg` source package: `lapack=3.12.0-4`

Binary Packages:

- `libblas-dev:amd64=3.12.0-4`
- `libblas3:amd64=3.12.0-4`
- `liblapack-dev:amd64=3.12.0-4`
- `liblapack3:amd64=3.12.0-4`

Licenses: (parsed from: `/usr/share/doc/libblas-dev/copyright`, `/usr/share/doc/libblas3/copyright`, `/usr/share/doc/liblapack-dev/copyright`, `/usr/share/doc/liblapack3/copyright`)

- `BSD-3-clause`
- `BSD-3-clause-intel`

Source:

```console
$ apt-get source -qq --print-uris lapack=3.12.0-4
'http://http.debian.net/debian/pool/main/l/lapack/lapack_3.12.0-4.dsc' lapack_3.12.0-4.dsc 3327 SHA256:2c13292e8119fad639fe9dcc69bf2e4f23eb1969dd972d21246ba6749ce784ea
'http://http.debian.net/debian/pool/main/l/lapack/lapack_3.12.0.orig.tar.gz' lapack_3.12.0.orig.tar.gz 7933607 SHA256:eac9570f8e0ad6f30ce4b963f4f033f0f643e7c3912fc9ee6cd99120675ad48b
'http://http.debian.net/debian/pool/main/l/lapack/lapack_3.12.0-4.debian.tar.xz' lapack_3.12.0-4.debian.tar.xz 28852 SHA256:e891b232d71d4cf2fae4aa8e27542369b6348cdce2125b8daa38234201e8fdc5
```

### `dpkg` source package: `lattice=0.22-6-1`

Binary Packages:

- `r-cran-lattice=0.22-6-1`

Licenses: (parsed from: `/usr/share/doc/r-cran-lattice/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris lattice=0.22-6-1
'http://http.debian.net/debian/pool/main/l/lattice/lattice_0.22-6-1.dsc' lattice_0.22-6-1.dsc 1838 SHA256:1623a40c65783047d7393f169c1cc52bcee867ea927947f4e27d3bcffab0f72e
'http://http.debian.net/debian/pool/main/l/lattice/lattice_0.22-6.orig.tar.gz' lattice_0.22-6.orig.tar.gz 598581 SHA256:4b377211e472ece7872b9d6759f9b9c660b09594500462eb6146312a1d4d00f7
'http://http.debian.net/debian/pool/main/l/lattice/lattice_0.22-6-1.debian.tar.xz' lattice_0.22-6-1.debian.tar.xz 5392 SHA256:369910459b7895e751975546aeb636a7afbae27eba1458039fefeb22b97e0846
```

### `dpkg` source package: `lerc=4.0.0+ds-5`

Binary Packages:

- `liblerc4:amd64=4.0.0+ds-5`

Licenses: (parsed from: `/usr/share/doc/liblerc4/copyright`)

- `Apache-2.0`

Source:

```console
$ apt-get source -qq --print-uris lerc=4.0.0+ds-5
'http://http.debian.net/debian/pool/main/l/lerc/lerc_4.0.0%2bds-5.dsc' lerc_4.0.0+ds-5.dsc 2673 SHA256:84de8dac3dd5f5edc005c5c02be58c1f549f9365ad4147c138c85e07d624cc12
'http://http.debian.net/debian/pool/main/l/lerc/lerc_4.0.0%2bds.orig.tar.xz' lerc_4.0.0+ds.orig.tar.xz 348140 SHA256:acf855502fd3b950ee78f0b67bc9e9b39316b3526fbf6d8b8b1a9482fb756723
'http://http.debian.net/debian/pool/main/l/lerc/lerc_4.0.0%2bds-5.debian.tar.xz' lerc_4.0.0+ds-5.debian.tar.xz 8576 SHA256:28ab2b1c19c845cd493e804bb9c43b47f72d5852281ebf832ed68a7576afbf6d
```

### `dpkg` source package: `less=643-1`

Binary Packages:

- `less=643-1`

Licenses: (parsed from: `/usr/share/doc/less/copyright`)

- `GPL-3`
- `GPL-3+`
- `Less`
- `Less,`
- `Spencer-86`
- `X11`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris less=643-1
'http://http.debian.net/debian/pool/main/l/less/less_643-1.dsc' less_643-1.dsc 1883 SHA256:0a3de7248142639c6deaf5f355627bcbbe52c2773459100275761b6e648f5e63
'http://http.debian.net/debian/pool/main/l/less/less_643.orig.tar.gz' less_643.orig.tar.gz 592291 SHA256:2911b5432c836fa084c8a2e68f6cd6312372c026a58faaa98862731c8b6052e8
'http://http.debian.net/debian/pool/main/l/less/less_643.orig.tar.gz.asc' less_643.orig.tar.gz.asc 163 SHA256:72eaaf892e2f17e188aa17acf1e3d4c6dbf15c68b1b9726a360ed4bbbd3837d3
'http://http.debian.net/debian/pool/main/l/less/less_643-1.debian.tar.xz' less_643-1.debian.tar.xz 23292 SHA256:1df050060f1cbc071737e4f1c29497b08ea6c4fc79866f9cee484429a15e92cc
```

### `dpkg` source package: `libbsd=0.12.2-2`

Binary Packages:

- `libbsd0:amd64=0.12.2-2`

Licenses: (parsed from: `/usr/share/doc/libbsd0/copyright`)

- `BSD-2-clause`
- `BSD-2-clause-NetBSD`
- `BSD-2-clause-author`
- `BSD-2-clause-verbatim`
- `BSD-3-clause`
- `BSD-3-clause-John-Birrell`
- `BSD-3-clause-Regents`
- `BSD-3-clause-author`
- `BSD-5-clause-Peter-Wemm`
- `Beerware`
- `Expat`
- `ISC`
- `ISC-Original`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris libbsd=0.12.2-2
'http://http.debian.net/debian/pool/main/libb/libbsd/libbsd_0.12.2-2.dsc' libbsd_0.12.2-2.dsc 2446 SHA256:01eb1d0c896096f9038213f5f00376ecfd1c0d1def21b7042f28ae070e4837e3
'http://http.debian.net/debian/pool/main/libb/libbsd/libbsd_0.12.2.orig.tar.xz' libbsd_0.12.2.orig.tar.xz 446032 SHA256:b88cc9163d0c652aaf39a99991d974ddba1c3a9711db8f1b5838af2a14731014
'http://http.debian.net/debian/pool/main/libb/libbsd/libbsd_0.12.2.orig.tar.xz.asc' libbsd_0.12.2.orig.tar.xz.asc 833 SHA256:620dc92f158ebe0a650c0e92214a8121b927276895dc9a1dcaa38f627fa0fcb0
'http://http.debian.net/debian/pool/main/libb/libbsd/libbsd_0.12.2-2.debian.tar.xz' libbsd_0.12.2-2.debian.tar.xz 18688 SHA256:36c878a32c1f190ca2cb474de5c6139990a6c029906493d3566770b1ebd569bf
```

### `dpkg` source package: `libcap-ng=0.8.5-4`

Binary Packages:

- `libcap-ng0:amd64=0.8.5-4`

Licenses: (parsed from: `/usr/share/doc/libcap-ng0/copyright`)

- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris libcap-ng=0.8.5-4
'http://http.debian.net/debian/pool/main/libc/libcap-ng/libcap-ng_0.8.5-4.dsc' libcap-ng_0.8.5-4.dsc 1710 SHA256:a5745b7d68a11068ae5beddcc7fbc94cd87dd81cb2d7495e7d48610603be3526
'http://http.debian.net/debian/pool/main/libc/libcap-ng/libcap-ng_0.8.5.orig.tar.gz' libcap-ng_0.8.5.orig.tar.gz 59265 SHA256:e4be07fdd234f10b866433f224d183626003c65634ed0552b02e654a380244c2
'http://http.debian.net/debian/pool/main/libc/libcap-ng/libcap-ng_0.8.5-4.debian.tar.xz' libcap-ng_0.8.5-4.debian.tar.xz 7816 SHA256:f5d4e7f38bdbca87de77317ce95f973883081370ef257019b484e29e3368a20d
```

### `dpkg` source package: `libcap2=1:2.66-5`

Binary Packages:

- `libcap2:amd64=1:2.66-5+b1`

Licenses: (parsed from: `/usr/share/doc/libcap2/copyright`)

- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris libcap2=1:2.66-5
'http://http.debian.net/debian/pool/main/libc/libcap2/libcap2_2.66-5.dsc' libcap2_2.66-5.dsc 2204 SHA256:7d8fd6db23376ad9ded85aebd5d5ed9cf133b1e561d3ac2b43fdf5b0b63739a8
'http://http.debian.net/debian/pool/main/libc/libcap2/libcap2_2.66.orig.tar.xz' libcap2_2.66.orig.tar.xz 181592 SHA256:15c40ededb3003d70a283fe587a36b7d19c8b3b554e33f86129c059a4bb466b2
'http://http.debian.net/debian/pool/main/libc/libcap2/libcap2_2.66-5.debian.tar.xz' libcap2_2.66-5.debian.tar.xz 21648 SHA256:fee7fdec4c806808b3e4c56e53ff5614b92186ecc6fd23a9e88694cdd938c452
```

### `dpkg` source package: `libdatrie=0.2.13-3`

Binary Packages:

- `libdatrie1:amd64=0.2.13-3+b1`

Licenses: (parsed from: `/usr/share/doc/libdatrie1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris libdatrie=0.2.13-3
'http://http.debian.net/debian/pool/main/libd/libdatrie/libdatrie_0.2.13-3.dsc' libdatrie_0.2.13-3.dsc 2236 SHA256:6ddcaf319da01cc044f9b335b6b01b608a0380ccdaecb06bda71710b6f4395bb
'http://http.debian.net/debian/pool/main/libd/libdatrie/libdatrie_0.2.13.orig.tar.xz' libdatrie_0.2.13.orig.tar.xz 314072 SHA256:12231bb2be2581a7f0fb9904092d24b0ed2a271a16835071ed97bed65267f4be
'http://http.debian.net/debian/pool/main/libd/libdatrie/libdatrie_0.2.13-3.debian.tar.xz' libdatrie_0.2.13-3.debian.tar.xz 9668 SHA256:e656d536beb5db9e52ef92dd1fccd5480ebd21e4eddbfe013c51a1e2ec45cf38
```

### `dpkg` source package: `libdeflate=1.22-1`

Binary Packages:

- `libdeflate-dev:amd64=1.22-1`
- `libdeflate0:amd64=1.22-1`

Licenses: (parsed from: `/usr/share/doc/libdeflate-dev/copyright`, `/usr/share/doc/libdeflate0/copyright`)

- `Expat`

Source:

```console
$ apt-get source -qq --print-uris libdeflate=1.22-1
'http://http.debian.net/debian/pool/main/libd/libdeflate/libdeflate_1.22-1.dsc' libdeflate_1.22-1.dsc 2213 SHA256:c33d1cf493eeb1563cbb9b44ce9089d8a58fea1c62408b9d32850c95df5426e4
'http://http.debian.net/debian/pool/main/libd/libdeflate/libdeflate_1.22.orig.tar.gz' libdeflate_1.22.orig.tar.gz 197720 SHA256:7f343c7bf2ba46e774d8a632bf073235e1fd27723ef0a12a90f8947b7fe851d6
'http://http.debian.net/debian/pool/main/libd/libdeflate/libdeflate_1.22-1.debian.tar.xz' libdeflate_1.22-1.debian.tar.xz 5536 SHA256:48b09829eac1c2985fb646aa29129019662966e3dd807454129057ea8eff0079
```

### `dpkg` source package: `libffi=3.4.6-1`

Binary Packages:

- `libffi8:amd64=3.4.6-1`

Licenses: (parsed from: `/usr/share/doc/libffi8/copyright`)

- `Expat`
- `GPL`
- `GPL-2+`
- `GPL-3+`
- `LGPL-2.1+`
- `MPL-1.1`
- `X11`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris libffi=3.4.6-1
'http://http.debian.net/debian/pool/main/libf/libffi/libffi_3.4.6-1.dsc' libffi_3.4.6-1.dsc 1948 SHA256:6734a8f8e237a7d5c4f52503f5e9cc193d16f8930a201bbf737f09cb31cfe28e
'http://http.debian.net/debian/pool/main/libf/libffi/libffi_3.4.6.orig.tar.gz' libffi_3.4.6.orig.tar.gz 598175 SHA256:9ac790464c1eb2f5ab5809e978a1683e9393131aede72d1b0a0703771d3c6cda
'http://http.debian.net/debian/pool/main/libf/libffi/libffi_3.4.6-1.debian.tar.xz' libffi_3.4.6-1.debian.tar.xz 10636 SHA256:7126c310b616e9c4c8fdd50bd857f54379d26897ab55383a25e89b6cbd69729c
```

### `dpkg` source package: `libgcrypt20=1.11.0-6`

Binary Packages:

- `libgcrypt20:amd64=1.11.0-6`

Licenses: (parsed from: `/usr/share/doc/libgcrypt20/copyright`)

- `GPL-2`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris libgcrypt20=1.11.0-6
'http://http.debian.net/debian/pool/main/libg/libgcrypt20/libgcrypt20_1.11.0-6.dsc' libgcrypt20_1.11.0-6.dsc 2877 SHA256:9d14f1cfec9a9c6523f9c469132634467daa43f83203f6339447fb6722b54b42
'http://http.debian.net/debian/pool/main/libg/libgcrypt20/libgcrypt20_1.11.0.orig.tar.bz2' libgcrypt20_1.11.0.orig.tar.bz2 4180345 SHA256:09120c9867ce7f2081d6aaa1775386b98c2f2f246135761aae47d81f58685b9c
'http://http.debian.net/debian/pool/main/libg/libgcrypt20/libgcrypt20_1.11.0.orig.tar.bz2.asc' libgcrypt20_1.11.0.orig.tar.bz2.asc 228 SHA256:9fedf4f7bb80d5178d4e26ec2f03ba5fc44eddfc72c2e9966d7d619aeee3df2c
'http://http.debian.net/debian/pool/main/libg/libgcrypt20/libgcrypt20_1.11.0-6.debian.tar.xz' libgcrypt20_1.11.0-6.debian.tar.xz 39088 SHA256:f1b8c0dc512241b427d8c2f7617355a7f4c98def3d5689495b6051a275a1357f
```

### `dpkg` source package: `libgpg-error=1.51-2`

Binary Packages:

- `libgpg-error0:amd64=1.51-2`

Licenses: (parsed from: `/usr/share/doc/libgpg-error0/copyright`)

- `BSD-3-clause`
- `GPL-3`
- `GPL-3+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `g10-permissive`

Source:

```console
$ apt-get source -qq --print-uris libgpg-error=1.51-2
'http://http.debian.net/debian/pool/main/libg/libgpg-error/libgpg-error_1.51-2.dsc' libgpg-error_1.51-2.dsc 2935 SHA256:a41a00868707d70d95e45180440bcf768826fda08116c5a68ac68ebd8ce09ab0
'http://http.debian.net/debian/pool/main/libg/libgpg-error/libgpg-error_1.51.orig.tar.bz2' libgpg-error_1.51.orig.tar.bz2 1085510 SHA256:be0f1b2db6b93eed55369cdf79f19f72750c8c7c39fc20b577e724545427e6b2
'http://http.debian.net/debian/pool/main/libg/libgpg-error/libgpg-error_1.51.orig.tar.bz2.asc' libgpg-error_1.51.orig.tar.bz2.asc 228 SHA256:5e8c9179635b3105f4c07d09168fda9ce039607e926628aec6a06134908be918
'http://http.debian.net/debian/pool/main/libg/libgpg-error/libgpg-error_1.51-2.debian.tar.xz' libgpg-error_1.51-2.debian.tar.xz 19800 SHA256:0b36279edb54d572cf85e20f392b932583090b760c2209cf826f2a4c116273de
```

### `dpkg` source package: `libice=2:1.1.1-1`

Binary Packages:

- `libice6:amd64=2:1.1.1-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libice=2:1.1.1-1
'http://http.debian.net/debian/pool/main/libi/libice/libice_1.1.1-1.dsc' libice_1.1.1-1.dsc 2021 SHA256:88722aa66d7f1807d1b0d3ae5bc62f8f06424dc5e970b1c73a0ea2fdf171f0b8
'http://http.debian.net/debian/pool/main/libi/libice/libice_1.1.1.orig.tar.gz' libice_1.1.1.orig.tar.gz 489944 SHA256:04fbd34a11ba08b9df2e3cdb2055c2e3c1c51b3257f683d7fcf42dabcf8e1210
'http://http.debian.net/debian/pool/main/libi/libice/libice_1.1.1-1.diff.gz' libice_1.1.1-1.diff.gz 7355 SHA256:8ce8ffaf775b0868e0633053fcd0755850938ddda9d977232e536a206c063d18
```

### `dpkg` source package: `libidn2=2.3.7-2`

Binary Packages:

- `libidn2-0:amd64=2.3.7-2+b1`

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
$ apt-get source -qq --print-uris libidn2=2.3.7-2
'http://http.debian.net/debian/pool/main/libi/libidn2/libidn2_2.3.7-2.dsc' libidn2_2.3.7-2.dsc 1963 SHA256:ba763f71c75847be4c68557a937484ff9e676c0af8be9a6796c914dab1363a5f
'http://http.debian.net/debian/pool/main/libi/libidn2/libidn2_2.3.7.orig.tar.gz' libidn2_2.3.7.orig.tar.gz 2155214 SHA256:4c21a791b610b9519b9d0e12b8097bf2f359b12f8dd92647611a929e6bfd7d64
'http://http.debian.net/debian/pool/main/libi/libidn2/libidn2_2.3.7.orig.tar.gz.asc' libidn2_2.3.7.orig.tar.gz.asc 228 SHA256:d4e78fc1c5a5c35980be3a04dd864574f450d55921360b0aa19326c75ada4a98
'http://http.debian.net/debian/pool/main/libi/libidn2/libidn2_2.3.7-2.debian.tar.xz' libidn2_2.3.7-2.debian.tar.xz 16276 SHA256:1f0ca3a2bb2c745056933cb41d212965b6571c9a436f83d33cba15e932d88d29
```

### `dpkg` source package: `libjpeg-turbo=1:2.1.5-3`

Binary Packages:

- `libjpeg-dev:amd64=1:2.1.5-3+b1`
- `libjpeg62-turbo:amd64=1:2.1.5-3+b1`
- `libjpeg62-turbo-dev:amd64=1:2.1.5-3+b1`

Licenses: (parsed from: `/usr/share/doc/libjpeg-dev/copyright`, `/usr/share/doc/libjpeg62-turbo/copyright`, `/usr/share/doc/libjpeg62-turbo-dev/copyright`)

- `BSD-3-clause`
- `BSD-BY-LC-NE`
- `Expat`
- `NTP`
- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris libjpeg-turbo=1:2.1.5-3
'http://http.debian.net/debian/pool/main/libj/libjpeg-turbo/libjpeg-turbo_2.1.5-3.dsc' libjpeg-turbo_2.1.5-3.dsc 2499 SHA256:a05e6bd60e85b10d12ed705e84262ceadbac95f63a0ef947d783e3ae8da8e747
'http://http.debian.net/debian/pool/main/libj/libjpeg-turbo/libjpeg-turbo_2.1.5.orig.tar.gz' libjpeg-turbo_2.1.5.orig.tar.gz 2264471 SHA256:254f3642b04e309fee775123133c6464181addc150499561020312ec61c1bf7c
'http://http.debian.net/debian/pool/main/libj/libjpeg-turbo/libjpeg-turbo_2.1.5-3.debian.tar.xz' libjpeg-turbo_2.1.5-3.debian.tar.xz 107996 SHA256:18631a8db64da29c6fe86aef840a417a3a8205373679ae870e8f1cdcb22a32b4
```

### `dpkg` source package: `libmd=1.1.0-2`

Binary Packages:

- `libmd0:amd64=1.1.0-2+b1`

Licenses: (parsed from: `/usr/share/doc/libmd0/copyright`)

- `BSD-2-clause`
- `BSD-2-clause-NetBSD`
- `BSD-3-clause`
- `BSD-3-clause-Aaron-D-Gifford`
- `Beerware`
- `ISC`
- `public-domain-md4`
- `public-domain-md5`
- `public-domain-sha1`

Source:

```console
$ apt-get source -qq --print-uris libmd=1.1.0-2
'http://http.debian.net/debian/pool/main/libm/libmd/libmd_1.1.0-2.dsc' libmd_1.1.0-2.dsc 2280 SHA256:46cc951cd6d71bbfeff4522de66f968fb92601ec4cc622b07f6ac0a2a36ac5f0
'http://http.debian.net/debian/pool/main/libm/libmd/libmd_1.1.0.orig.tar.xz' libmd_1.1.0.orig.tar.xz 271228 SHA256:1bd6aa42275313af3141c7cf2e5b964e8b1fd488025caf2f971f43b00776b332
'http://http.debian.net/debian/pool/main/libm/libmd/libmd_1.1.0.orig.tar.xz.asc' libmd_1.1.0.orig.tar.xz.asc 833 SHA256:402fd3024e43ab975733d09e661804a58ca58697194e4b15216b1217cfe1dadb
'http://http.debian.net/debian/pool/main/libm/libmd/libmd_1.1.0-2.debian.tar.xz' libmd_1.1.0-2.debian.tar.xz 8244 SHA256:3b6ff35fc921eb5450fa9bf2d300c9e058e3771f96f8f13f759768fadd53324c
```

### `dpkg` source package: `libpaper=2.2.5-0.3`

Binary Packages:

- `libpaper-utils=2.2.5-0.3`
- `libpaper2:amd64=2.2.5-0.3`

Licenses: (parsed from: `/usr/share/doc/libpaper-utils/copyright`, `/usr/share/doc/libpaper2/copyright`)

- `Expat`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `X11`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris libpaper=2.2.5-0.3
'http://http.debian.net/debian/pool/main/libp/libpaper/libpaper_2.2.5-0.3.dsc' libpaper_2.2.5-0.3.dsc 1863 SHA256:c81d68db130d6930282c46a4ce471c198193ca0e22d2659245f5bc82464931fe
'http://http.debian.net/debian/pool/main/libp/libpaper/libpaper_2.2.5.orig.tar.xz' libpaper_2.2.5.orig.tar.xz 524008 SHA256:c41cd29f49bb8c2fbc14964a6307451dfd3cada15c1edcc82de878f937cca6a3
'http://http.debian.net/debian/pool/main/libp/libpaper/libpaper_2.2.5-0.3.debian.tar.xz' libpaper_2.2.5-0.3.debian.tar.xz 25072 SHA256:f34d1a3b1125977ddd30d72aac9cd1105165f7368b58f51c5c55160442d4a31f
```

### `dpkg` source package: `libpng1.6=1.6.44-3`

Binary Packages:

- `libpng-dev:amd64=1.6.44-3`
- `libpng16-16t64:amd64=1.6.44-3`

Licenses: (parsed from: `/usr/share/doc/libpng-dev/copyright`, `/usr/share/doc/libpng16-16t64/copyright`)

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
$ apt-get source -qq --print-uris libpng1.6=1.6.44-3
'http://http.debian.net/debian/pool/main/libp/libpng1.6/libpng1.6_1.6.44-3.dsc' libpng1.6_1.6.44-3.dsc 2254 SHA256:a28e586623a116c1392d0144929ea10e02466b1e7e437fa95a948215316078b4
'http://http.debian.net/debian/pool/main/libp/libpng1.6/libpng1.6_1.6.44.orig.tar.gz' libpng1.6_1.6.44.orig.tar.gz 1558044 SHA256:0ef5b633d0c65f780c4fced27ff832998e71478c13b45dfb6e94f23a82f64f7c
'http://http.debian.net/debian/pool/main/libp/libpng1.6/libpng1.6_1.6.44-3.debian.tar.xz' libpng1.6_1.6.44-3.debian.tar.xz 31652 SHA256:c3c58c5cea3b4c8459ccf1bdfbaf35baa8d865a8b3b2fc322ccd6dc3697610c1
```

### `dpkg` source package: `libpsl=0.21.2-1.1`

Binary Packages:

- `libpsl5t64:amd64=0.21.2-1.1+b1`

Licenses: (parsed from: `/usr/share/doc/libpsl5t64/copyright`)

- `Chromium`
- `MIT`
- `gnulib`

Source:

```console
$ apt-get source -qq --print-uris libpsl=0.21.2-1.1
'http://http.debian.net/debian/pool/main/libp/libpsl/libpsl_0.21.2-1.1.dsc' libpsl_0.21.2-1.1.dsc 2285 SHA256:b9b5496ca2bffb827cb0b2d997469908a2b7a7475c20a11c02f9dcd1ed2a0cc9
'http://http.debian.net/debian/pool/main/libp/libpsl/libpsl_0.21.2.orig.tar.xz' libpsl_0.21.2.orig.tar.xz 1870352 SHA256:11e34380f2c81d6e72c710464aae3b680df4ddcc1007826c630fb03c7ca6aa54
'http://http.debian.net/debian/pool/main/libp/libpsl/libpsl_0.21.2-1.1.debian.tar.xz' libpsl_0.21.2-1.1.debian.tar.xz 12120 SHA256:0eccab147b6dfbfb7f5ad40fb5bd9f888d72a0fe44e7d1801811c34a9acad1a7
```

### `dpkg` source package: `libseccomp=2.5.5-2`

Binary Packages:

- `libseccomp2:amd64=2.5.5-2`

Licenses: (parsed from: `/usr/share/doc/libseccomp2/copyright`)

- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libseccomp=2.5.5-2
'http://http.debian.net/debian/pool/main/libs/libseccomp/libseccomp_2.5.5-2.dsc' libseccomp_2.5.5-2.dsc 2708 SHA256:e69657cf7b3cf0219d4c6d72c81db1f7f2d9a8e090fd8a983d17a4a80363dcc2
'http://http.debian.net/debian/pool/main/libs/libseccomp/libseccomp_2.5.5.orig.tar.gz' libseccomp_2.5.5.orig.tar.gz 642445 SHA256:248a2c8a4d9b9858aa6baf52712c34afefcf9c9e94b76dce02c1c9aa25fb3375
'http://http.debian.net/debian/pool/main/libs/libseccomp/libseccomp_2.5.5.orig.tar.gz.asc' libseccomp_2.5.5.orig.tar.gz.asc 833 SHA256:f3bf8a946020d3047581f11fe6ac71971a842115ddb362562b193861ef57d97b
'http://http.debian.net/debian/pool/main/libs/libseccomp/libseccomp_2.5.5-2.debian.tar.xz' libseccomp_2.5.5-2.debian.tar.xz 39004 SHA256:82fa4dfbea7c0ce54d18781230b9625c44fc83f495ef4a468beb2a33e98897ef
```

### `dpkg` source package: `libselinux=3.7-3`

Binary Packages:

- `libselinux1:amd64=3.7-3+b1`

Licenses: (parsed from: `/usr/share/doc/libselinux1/copyright`)

- `GPL-2`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris libselinux=3.7-3
'http://http.debian.net/debian/pool/main/libs/libselinux/libselinux_3.7-3.dsc' libselinux_3.7-3.dsc 2990 SHA256:18559f82479feb99d429eb20e4b4572825cb8cb8ce0d2534b69c145f80cd7230
'http://http.debian.net/debian/pool/main/libs/libselinux/libselinux_3.7.orig.tar.gz' libselinux_3.7.orig.tar.gz 194834 SHA256:ea03f42d13a4f95757997dba8cf0b26321fac5d2f164418b4cc856a92d2b17bd
'http://http.debian.net/debian/pool/main/libs/libselinux/libselinux_3.7.orig.tar.gz.asc' libselinux_3.7.orig.tar.gz.asc 833 SHA256:8dbd0457d227a7182b0a1f2f8659c2f4dd4ae837f5e69a17d1698f6c31c37f31
'http://http.debian.net/debian/pool/main/libs/libselinux/libselinux_3.7-3.debian.tar.xz' libselinux_3.7-3.debian.tar.xz 41912 SHA256:db181834077ab5bbfc7118b3414d003b412f21463acd1924a25f826fa0f484ed
```

### `dpkg` source package: `libsemanage=3.7-2`

Binary Packages:

- `libsemanage-common=3.7-2`
- `libsemanage2:amd64=3.7-2+b1`

Licenses: (parsed from: `/usr/share/doc/libsemanage-common/copyright`, `/usr/share/doc/libsemanage2/copyright`)

- `GPL-2`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris libsemanage=3.7-2
'http://http.debian.net/debian/pool/main/libs/libsemanage/libsemanage_3.7-2.dsc' libsemanage_3.7-2.dsc 2965 SHA256:77fd2cef54cbd51c3d76a622a0aefe4488ae9403db32c5c92c801bce181690ae
'http://http.debian.net/debian/pool/main/libs/libsemanage/libsemanage_3.7.orig.tar.gz' libsemanage_3.7.orig.tar.gz 182896 SHA256:e166cae29a417dab008db9ca0874023f353a3017b07693a036ed97487eda35b1
'http://http.debian.net/debian/pool/main/libs/libsemanage/libsemanage_3.7.orig.tar.gz.asc' libsemanage_3.7.orig.tar.gz.asc 833 SHA256:02981e0224fdf0141fc29b950f7e5aab1653d5fee6dcbf6d6a5ff976e5720cc8
'http://http.debian.net/debian/pool/main/libs/libsemanage/libsemanage_3.7-2.debian.tar.xz' libsemanage_3.7-2.debian.tar.xz 35172 SHA256:eeb1ca76456ea4caf7850699d5999b7a9f5b49ebaa6a5a6929e84848305a297b
```

### `dpkg` source package: `libsepol=3.7-1`

Binary Packages:

- `libsepol2:amd64=3.7-1`

Licenses: (parsed from: `/usr/share/doc/libsepol2/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris libsepol=3.7-1
'http://http.debian.net/debian/pool/main/libs/libsepol/libsepol_3.7-1.dsc' libsepol_3.7-1.dsc 2085 SHA256:d5c8df3195e58607d769d6030b4254013bf483723084a42656cfb50a38b91fff
'http://http.debian.net/debian/pool/main/libs/libsepol/libsepol_3.7.orig.tar.gz' libsepol_3.7.orig.tar.gz 511487 SHA256:cd741e25244e7ef6cd934d633614131a266c3eaeab33d8bfa45e8a93b45cc901
'http://http.debian.net/debian/pool/main/libs/libsepol/libsepol_3.7-1.debian.tar.xz' libsepol_3.7-1.debian.tar.xz 27632 SHA256:fe5c57d69d081d60d423185bf339aa10755eb629d38f4129dd9944be64c6991b
```

### `dpkg` source package: `libsm=2:1.2.4-1`

Binary Packages:

- `libsm6:amd64=2:1.2.4-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libsm=2:1.2.4-1
'http://http.debian.net/debian/pool/main/libs/libsm/libsm_1.2.4-1.dsc' libsm_1.2.4-1.dsc 2328 SHA256:60c65ac4b34d5ca2655ce18ee3dacc5d8f8d205e93e6417b54f597483331bca4
'http://http.debian.net/debian/pool/main/libs/libsm/libsm_1.2.4.orig.tar.gz' libsm_1.2.4.orig.tar.gz 454517 SHA256:51464ce1abce323d5b6707ceecf8468617106e1a8a98522f8342db06fd024c15
'http://http.debian.net/debian/pool/main/libs/libsm/libsm_1.2.4.orig.tar.gz.asc' libsm_1.2.4.orig.tar.gz.asc 801 SHA256:4c35e61cac3f5dca052c387674db3b7c99588915ea4804df83d8648ee6f08203
'http://http.debian.net/debian/pool/main/libs/libsm/libsm_1.2.4-1.diff.gz' libsm_1.2.4-1.diff.gz 13196 SHA256:21a56eeee249592af6fcefb991c1091530cf6f2f650359174ce6a05cdd085235
```

### `dpkg` source package: `libssh2=1.11.1-1`

Binary Packages:

- `libssh2-1t64:amd64=1.11.1-1`

Licenses: (parsed from: `/usr/share/doc/libssh2-1t64/copyright`)

- `BSD3`
- `ISC`

Source:

```console
$ apt-get source -qq --print-uris libssh2=1.11.1-1
'http://http.debian.net/debian/pool/main/libs/libssh2/libssh2_1.11.1-1.dsc' libssh2_1.11.1-1.dsc 2319 SHA256:f97f7ac25300908b255a29c63055e78684e68c12c308edb016747da1de592377
'http://http.debian.net/debian/pool/main/libs/libssh2/libssh2_1.11.1.orig.tar.gz' libssh2_1.11.1.orig.tar.gz 1093012 SHA256:d9ec76cbe34db98eec3539fe2c899d26b0c837cb3eb466a56b0f109cabf658f7
'http://http.debian.net/debian/pool/main/libs/libssh2/libssh2_1.11.1.orig.tar.gz.asc' libssh2_1.11.1.orig.tar.gz.asc 488 SHA256:f5618c9356a1d5a8059d6cf64015d86547f06b2b8b1f542fbbaf381a736c8075
'http://http.debian.net/debian/pool/main/libs/libssh2/libssh2_1.11.1-1.debian.tar.xz' libssh2_1.11.1-1.debian.tar.xz 17136 SHA256:f3b9e55f706c89e9408478a1eecb0067b8e18902e0cab168f44194fcc53641cf
```

### `dpkg` source package: `libtasn1-6=4.19.0-3`

Binary Packages:

- `libtasn1-6:amd64=4.19.0-3+b3`

Licenses: (parsed from: `/usr/share/doc/libtasn1-6/copyright`)

- `GFDL-1.3`
- `GPL-3`
- `LGPL`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libtasn1-6=4.19.0-3
'http://http.debian.net/debian/pool/main/libt/libtasn1-6/libtasn1-6_4.19.0-3.dsc' libtasn1-6_4.19.0-3.dsc 2662 SHA256:7fd9618be5b99035c7387d969b73365a57b1f6f01ec4abe0af332829af718190
'http://http.debian.net/debian/pool/main/libt/libtasn1-6/libtasn1-6_4.19.0.orig.tar.gz' libtasn1-6_4.19.0.orig.tar.gz 1786576 SHA256:1613f0ac1cf484d6ec0ce3b8c06d56263cc7242f1c23b30d82d23de345a63f7a
'http://http.debian.net/debian/pool/main/libt/libtasn1-6/libtasn1-6_4.19.0.orig.tar.gz.asc' libtasn1-6_4.19.0.orig.tar.gz.asc 228 SHA256:8410c0c004f3509c218a98b276b3308b9c46f48068e8b1a6d9ebfd61ea9f357a
'http://http.debian.net/debian/pool/main/libt/libtasn1-6/libtasn1-6_4.19.0-3.debian.tar.xz' libtasn1-6_4.19.0-3.debian.tar.xz 22084 SHA256:acb32dc03d8c2aeb10e0fb1c2a0247efdab0a6dc5e8f8a4d3cdcfe5ad26bb0df
```

### `dpkg` source package: `libthai=0.1.29-2`

Binary Packages:

- `libthai-data=0.1.29-2`
- `libthai0:amd64=0.1.29-2+b1`

Licenses: (parsed from: `/usr/share/doc/libthai-data/copyright`, `/usr/share/doc/libthai0/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris libthai=0.1.29-2
'http://http.debian.net/debian/pool/main/libt/libthai/libthai_0.1.29-2.dsc' libthai_0.1.29-2.dsc 2319 SHA256:564814dc31a466566cb50c077c5f6c5926a451594f52a0fc6b6367100445dddb
'http://http.debian.net/debian/pool/main/libt/libthai/libthai_0.1.29.orig.tar.xz' libthai_0.1.29.orig.tar.xz 417728 SHA256:fc80cc7dcb50e11302b417cebd24f2d30a8b987292e77e003267b9100d0f4bcd
'http://http.debian.net/debian/pool/main/libt/libthai/libthai_0.1.29-2.debian.tar.xz' libthai_0.1.29-2.debian.tar.xz 12644 SHA256:18a66bc2e766f475c206492612eabe3a206642bb69866236eb4a0a4126bf4f41
```

### `dpkg` source package: `libtirpc=1.3.4+ds-1.3`

Binary Packages:

- `libtirpc-common=1.3.4+ds-1.3`
- `libtirpc-dev:amd64=1.3.4+ds-1.3+b1`
- `libtirpc3t64:amd64=1.3.4+ds-1.3+b1`

Licenses: (parsed from: `/usr/share/doc/libtirpc-common/copyright`, `/usr/share/doc/libtirpc-dev/copyright`, `/usr/share/doc/libtirpc3t64/copyright`)

- `BSD-2-Clause`
- `BSD-3-Clause`
- `BSD-4-Clause`
- `GPL-2`
- `LGPL-2.1`
- `LGPL-2.1+`
- `PERMISSIVE`
- `__AUTO_PERMISSIVE__`

Source:

```console
$ apt-get source -qq --print-uris libtirpc=1.3.4+ds-1.3
'http://http.debian.net/debian/pool/main/libt/libtirpc/libtirpc_1.3.4%2bds-1.3.dsc' libtirpc_1.3.4+ds-1.3.dsc 1914 SHA256:6a402591fda2b06314da2058f0b846bdb4c5a5d3219c4e42d7c227204467f3b5
'http://http.debian.net/debian/pool/main/libt/libtirpc/libtirpc_1.3.4%2bds.orig.tar.gz' libtirpc_1.3.4+ds.orig.tar.gz 700735 SHA256:730101dbb756b258164e496109bfdeee87eb0fcc05cd5a820e5f34537a1e637d
'http://http.debian.net/debian/pool/main/libt/libtirpc/libtirpc_1.3.4%2bds-1.3.debian.tar.xz' libtirpc_1.3.4+ds-1.3.debian.tar.xz 11892 SHA256:afd52c61c81c5b9ab1eddf4e367dbd05984e2db62802b4fd267a3d0012793d0a
```

### `dpkg` source package: `libunistring=1.3-1`

Binary Packages:

- `libunistring5:amd64=1.3-1`

Licenses: (parsed from: `/usr/share/doc/libunistring5/copyright`)

- `BSD-3-clause`
- `FreeSoftware`
- `GFDL-1.2+`
- `GFDL-1.3+`
- `GPL-2`
- `GPL-2+`
- `GPL-2+ with distribution exception`
- `GPL-2+ with distribution exception, Expat`
- `GPL-3`
- `GPL-3+`
- `ISC`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`
- `LGPL-3+`
- `Unicode-DFS-2016`
- `X11`
- `bsd-3-clause`
- `gfdl-1.2+`
- `gfdl-1.3+`
- `isc`
- `public-domain`
- `unicode-dfs-2016`

Source:

```console
$ apt-get source -qq --print-uris libunistring=1.3-1
'http://http.debian.net/debian/pool/main/libu/libunistring/libunistring_1.3-1.dsc' libunistring_1.3-1.dsc 1578 SHA256:2d734e00be507e74a873e1689d69e1bdde31c06d208c31543ea24e5ff1614bab
'http://http.debian.net/debian/pool/main/libu/libunistring/libunistring_1.3.orig.tar.xz' libunistring_1.3.orig.tar.xz 2753448 SHA256:f245786c831d25150f3dfb4317cda1acc5e3f79a5da4ad073ddca58886569527
'http://http.debian.net/debian/pool/main/libu/libunistring/libunistring_1.3.orig.tar.xz.asc' libunistring_1.3.orig.tar.xz.asc 833 SHA256:62201b5b7ce9c0b033c50cefa5d7769dff4b7cee8205572e0cf917653cae9e33
'http://http.debian.net/debian/pool/main/libu/libunistring/libunistring_1.3-1.debian.tar.xz' libunistring_1.3-1.debian.tar.xz 28376 SHA256:f1cfdaa0e9c330099ff15050395944814ad450bc87a6deae0b78a67fcdabe4d4
```

### `dpkg` source package: `libwebp=1.4.0-0.1`

Binary Packages:

- `libsharpyuv0:amd64=1.4.0-0.1+b1`
- `libwebp7:amd64=1.4.0-0.1+b1`

Licenses: (parsed from: `/usr/share/doc/libsharpyuv0/copyright`, `/usr/share/doc/libwebp7/copyright`)

- `Apache-2.0`
- `BSD-3-Clause`

Source:

```console
$ apt-get source -qq --print-uris libwebp=1.4.0-0.1
'http://http.debian.net/debian/pool/main/libw/libwebp/libwebp_1.4.0-0.1.dsc' libwebp_1.4.0-0.1.dsc 2569 SHA256:c21ed5aa518a60d590e9435e998bf223114e6248f619b6af81cd82e7ebf39b51
'http://http.debian.net/debian/pool/main/libw/libwebp/libwebp_1.4.0.orig.tar.gz' libwebp_1.4.0.orig.tar.gz 4281370 SHA256:61f873ec69e3be1b99535634340d5bde750b2e4447caa1db9f61be3fd49ab1e5
'http://http.debian.net/debian/pool/main/libw/libwebp/libwebp_1.4.0.orig.tar.gz.asc' libwebp_1.4.0.orig.tar.gz.asc 833 SHA256:9a25a1f6c2bec4a4ec05ece3bd6938f0e9b47e432d58067d3877dba4fbcf6214
'http://http.debian.net/debian/pool/main/libw/libwebp/libwebp_1.4.0-0.1.debian.tar.xz' libwebp_1.4.0-0.1.debian.tar.xz 11048 SHA256:d137689ec52cb7dd5851bea0e73a9d6e032b35df79e821ce1db770109f1eaf65
```

### `dpkg` source package: `libx11=2:1.8.10-2`

Binary Packages:

- `libx11-6:amd64=2:1.8.10-2`
- `libx11-data=2:1.8.10-2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libx11=2:1.8.10-2
'http://http.debian.net/debian/pool/main/libx/libx11/libx11_1.8.10-2.dsc' libx11_1.8.10-2.dsc 2519 SHA256:3c251eb0a8ac14ddaeac6ca1720d993e1164086b42c5f979df428ada4f029479
'http://http.debian.net/debian/pool/main/libx/libx11/libx11_1.8.10.orig.tar.gz' libx11_1.8.10.orig.tar.gz 3192536 SHA256:b7a1a90d881bb7b94df5cf31509e6b03f15c0972d3ac25ab0441f5fbc789650f
'http://http.debian.net/debian/pool/main/libx/libx11/libx11_1.8.10.orig.tar.gz.asc' libx11_1.8.10.orig.tar.gz.asc 833 SHA256:783f7cee17473f10248d2bbfbd446735ef47d8c7da24736c7b5c15caf7576dda
'http://http.debian.net/debian/pool/main/libx/libx11/libx11_1.8.10-2.diff.gz' libx11_1.8.10-2.diff.gz 74852 SHA256:6c5853a7ab0c012a20821396122509da105dcf432d33d52da98898cc0b0d391e
```

### `dpkg` source package: `libxau=1:1.0.11-1`

Binary Packages:

- `libxau6:amd64=1:1.0.11-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxau=1:1.0.11-1
'http://http.debian.net/debian/pool/main/libx/libxau/libxau_1.0.11-1.dsc' libxau_1.0.11-1.dsc 2213 SHA256:6058ab58b243ae2b175eee067b868f37b74cd4e8cc40b90607ce6d9ee99c50f9
'http://http.debian.net/debian/pool/main/libx/libxau/libxau_1.0.11.orig.tar.gz' libxau_1.0.11.orig.tar.gz 404973 SHA256:3a321aaceb803577a4776a5efe78836eb095a9e44bbc7a465d29463e1a14f189
'http://http.debian.net/debian/pool/main/libx/libxau/libxau_1.0.11.orig.tar.gz.asc' libxau_1.0.11.orig.tar.gz.asc 358 SHA256:72320a0c036cc2d36bebdd7d279c402620e2f3553f639581dfb23736803ce258
'http://http.debian.net/debian/pool/main/libx/libxau/libxau_1.0.11-1.diff.gz' libxau_1.0.11-1.diff.gz 22671 SHA256:0af3f94102f73c585c48a6b17f54c92e154f6b560a061871d437bd720edd5314
```

### `dpkg` source package: `libxcb=1.17.0-2`

Binary Packages:

- `libxcb-render0:amd64=1.17.0-2+b1`
- `libxcb-shm0:amd64=1.17.0-2+b1`
- `libxcb1:amd64=1.17.0-2+b1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxcb=1.17.0-2
'http://http.debian.net/debian/pool/main/libx/libxcb/libxcb_1.17.0-2.dsc' libxcb_1.17.0-2.dsc 5318 SHA256:b2728d156f79d2e757e7378cfcefca52bd570739d2efffa87e1aaeaf4f21de3a
'http://http.debian.net/debian/pool/main/libx/libxcb/libxcb_1.17.0.orig.tar.gz' libxcb_1.17.0.orig.tar.gz 661593 SHA256:2c69287424c9e2128cb47ffe92171e10417041ec2963bceafb65cb3fcf8f0b85
'http://http.debian.net/debian/pool/main/libx/libxcb/libxcb_1.17.0-2.diff.gz' libxcb_1.17.0-2.diff.gz 28069 SHA256:c5b33b67a61d0d1c1b624bf88a8150f4be1ba9b46e855e38f03a8f73858af558
```

### `dpkg` source package: `libxcrypt=1:4.4.36-5`

Binary Packages:

- `libcrypt-dev:amd64=1:4.4.36-5`
- `libcrypt1:amd64=1:4.4.36-5`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxcrypt=1:4.4.36-5
'http://http.debian.net/debian/pool/main/libx/libxcrypt/libxcrypt_4.4.36-5.dsc' libxcrypt_4.4.36-5.dsc 1576 SHA256:660fca79ca38888ed61e26f7ef6990299586471ff8462d6900abf1afe1e569e3
'http://http.debian.net/debian/pool/main/libx/libxcrypt/libxcrypt_4.4.36.orig.tar.xz' libxcrypt_4.4.36.orig.tar.xz 392732 SHA256:7b7abbc89f13f5194211aa6861ed954e4fa3a210a4cb64f7e13dc8cf413e7f2a
'http://http.debian.net/debian/pool/main/libx/libxcrypt/libxcrypt_4.4.36-5.debian.tar.xz' libxcrypt_4.4.36-5.debian.tar.xz 9184 SHA256:c520211106ab811788ba37fc766166a6cf17156882a13d7f0ab9de5834f95b52
```

### `dpkg` source package: `libxdmcp=1:1.1.5-1`

Binary Packages:

- `libxdmcp6:amd64=1:1.1.5-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxdmcp=1:1.1.5-1
'http://http.debian.net/debian/pool/main/libx/libxdmcp/libxdmcp_1.1.5-1.dsc' libxdmcp_1.1.5-1.dsc 2331 SHA256:d4a124405528eba3cf8794cc4fb8c4339ad74e79dd916fc0565b3a30c9fc1fe3
'http://http.debian.net/debian/pool/main/libx/libxdmcp/libxdmcp_1.1.5.orig.tar.gz' libxdmcp_1.1.5.orig.tar.gz 442597 SHA256:31a7abc4f129dcf6f27ae912c3eedcb94d25ad2e8f317f69df6eda0bc4e4f2f3
'http://http.debian.net/debian/pool/main/libx/libxdmcp/libxdmcp_1.1.5.orig.tar.gz.asc' libxdmcp_1.1.5.orig.tar.gz.asc 833 SHA256:0c7666da02d66ab785584cd16a6f9324f0d949555734e70b3b1385e525c7860b
'http://http.debian.net/debian/pool/main/libx/libxdmcp/libxdmcp_1.1.5-1.diff.gz' libxdmcp_1.1.5-1.diff.gz 9764 SHA256:7ec2e7da28c38723aa115ce2bd18389f7d73e716b0f50bec9e6e0d1b24f19954
```

### `dpkg` source package: `libxext=2:1.3.4-1`

Binary Packages:

- `libxext6:amd64=2:1.3.4-1+b2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxext=2:1.3.4-1
'http://http.debian.net/debian/pool/main/libx/libxext/libxext_1.3.4-1.dsc' libxext_1.3.4-1.dsc 2118 SHA256:25024f57d955739c6b858822bf93ec3c71400b56fc0d666826f440e3661fd7c0
'http://http.debian.net/debian/pool/main/libx/libxext/libxext_1.3.4.orig.tar.gz' libxext_1.3.4.orig.tar.gz 494434 SHA256:8ef0789f282826661ff40a8eef22430378516ac580167da35cc948be9041aac1
'http://http.debian.net/debian/pool/main/libx/libxext/libxext_1.3.4-1.diff.gz' libxext_1.3.4-1.diff.gz 12509 SHA256:b975870d6a7b791ffbe2d57efdf6e20c250c5e76d12e45b04c8655f593bb8337
```

### `dpkg` source package: `libxmu=2:1.1.3-3`

Binary Packages:

- `libxmuu1:amd64=2:1.1.3-3+b3`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxmu=2:1.1.3-3
'http://http.debian.net/debian/pool/main/libx/libxmu/libxmu_1.1.3-3.dsc' libxmu_1.1.3-3.dsc 2165 SHA256:d9dfadd0a6be92f88b1151c695e5799f889a39047176f80a91fcba24333cd063
'http://http.debian.net/debian/pool/main/libx/libxmu/libxmu_1.1.3.orig.tar.gz' libxmu_1.1.3.orig.tar.gz 497343 SHA256:5bd9d4ed1ceaac9ea023d86bf1c1632cd3b172dce4a193a72a94e1d9df87a62e
'http://http.debian.net/debian/pool/main/libx/libxmu/libxmu_1.1.3-3.diff.gz' libxmu_1.1.3-3.diff.gz 8085 SHA256:6f599ddd7951a1db5c1899fcd2a7c0289ae4ec9f9a783bc5e5b209b83c7ea12d
```

### `dpkg` source package: `libxrender=1:0.9.10-1.1`

Binary Packages:

- `libxrender1:amd64=1:0.9.10-1.1+b3`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxrender=1:0.9.10-1.1
'http://http.debian.net/debian/pool/main/libx/libxrender/libxrender_0.9.10-1.1.dsc' libxrender_0.9.10-1.1.dsc 2072 SHA256:348ab15d05f1d802da485e4c6abdb9d5419691fb7c8ce44ca5b17b2b7f889ce8
'http://http.debian.net/debian/pool/main/libx/libxrender/libxrender_0.9.10.orig.tar.gz' libxrender_0.9.10.orig.tar.gz 373717 SHA256:770527cce42500790433df84ec3521e8bf095dfe5079454a92236494ab296adf
'http://http.debian.net/debian/pool/main/libx/libxrender/libxrender_0.9.10-1.1.diff.gz' libxrender_0.9.10-1.1.diff.gz 15201 SHA256:caf8c84085b3b0d073f738fa12d32d4eca2d8b669cb3c7f1b1cd2ce64b7b10b7
```

### `dpkg` source package: `libxss=1:1.2.3-1`

Binary Packages:

- `libxss1:amd64=1:1.2.3-1+b2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxss=1:1.2.3-1
'http://http.debian.net/debian/pool/main/libx/libxss/libxss_1.2.3-1.dsc' libxss_1.2.3-1.dsc 2203 SHA256:783dbcd49a0934d994693af676ee98734dad070ab2434a6afe831c2de0ecca1d
'http://http.debian.net/debian/pool/main/libx/libxss/libxss_1.2.3.orig.tar.gz' libxss_1.2.3.orig.tar.gz 385215 SHA256:4f74e7e412144591d8e0616db27f433cfc9f45aae6669c6c4bb03e6bf9be809a
'http://http.debian.net/debian/pool/main/libx/libxss/libxss_1.2.3.orig.tar.gz.asc' libxss_1.2.3.orig.tar.gz.asc 705 SHA256:4e900524d56c8e7263365267efa91bb3671110c9eb28ccab58f70e2188f0b91b
'http://http.debian.net/debian/pool/main/libx/libxss/libxss_1.2.3-1.diff.gz' libxss_1.2.3-1.diff.gz 7145 SHA256:9d381b48f1377f27c506113e1f9b7d6ee286b856421f7f2b27017f01dccfef04
```

### `dpkg` source package: `libxt=1:1.2.1-1.2`

Binary Packages:

- `libxt6t64:amd64=1:1.2.1-1.2+b1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxt=1:1.2.1-1.2
'http://http.debian.net/debian/pool/main/libx/libxt/libxt_1.2.1-1.2.dsc' libxt_1.2.1-1.2.dsc 2373 SHA256:780be4cf9b0b90757758691dc8196d85322b30a599c36fb8fe368b7060c7b774
'http://http.debian.net/debian/pool/main/libx/libxt/libxt_1.2.1.orig.tar.gz' libxt_1.2.1.orig.tar.gz 1024473 SHA256:6da1bfa9dd0ed87430a5ce95b129485086394df308998ebe34d98e378e3dfb33
'http://http.debian.net/debian/pool/main/libx/libxt/libxt_1.2.1.orig.tar.gz.asc' libxt_1.2.1.orig.tar.gz.asc 358 SHA256:da406cc94c25ca6773bb37c2055e2eb5665491f7ca6dfc9ea04f0f30ea3fd098
'http://http.debian.net/debian/pool/main/libx/libxt/libxt_1.2.1-1.2.diff.gz' libxt_1.2.1-1.2.diff.gz 45635 SHA256:d4c510871909584398d88552b69cc5e92e124098ce544be93ef1743d0d112d4c
```

### `dpkg` source package: `libzstd=1.5.6+dfsg-1`

Binary Packages:

- `libzstd1:amd64=1.5.6+dfsg-1+b1`

Licenses: (parsed from: `/usr/share/doc/libzstd1/copyright`)

- `BSD-3-clause`
- `Expat`
- `GPL-2`
- `zlib`

Source:

```console
$ apt-get source -qq --print-uris libzstd=1.5.6+dfsg-1
'http://http.debian.net/debian/pool/main/libz/libzstd/libzstd_1.5.6%2bdfsg-1.dsc' libzstd_1.5.6+dfsg-1.dsc 2369 SHA256:c1774527814630f8e3ec1a6025d6b7a188ceccee002815ed143c3653e3b0b510
'http://http.debian.net/debian/pool/main/libz/libzstd/libzstd_1.5.6%2bdfsg.orig.tar.xz' libzstd_1.5.6+dfsg.orig.tar.xz 1815380 SHA256:b3a60c7059886641830adf32c979be8d211da5d73fd05c7768f86d12d5bccec3
'http://http.debian.net/debian/pool/main/libz/libzstd/libzstd_1.5.6%2bdfsg-1.debian.tar.xz' libzstd_1.5.6+dfsg-1.debian.tar.xz 22624 SHA256:33e540298d9fa29e12426a66e4b0b7715b3143659d16246e09c33f2fb69bad17
```

### `dpkg` source package: `linux=6.12.6-1`

Binary Packages:

- `linux-libc-dev=6.12.6-1`

Licenses: (parsed from: `/usr/share/doc/linux-libc-dev/copyright`)

- `BSD-2-clause`
- `CRYPTOGAMS`
- `GPL-2`
- `GPL-2+-or-X11`
- `LGPL-2.1`
- `Unicode-data`
- `Xen-interface`

Source:

```console
$ apt-get source -qq --print-uris linux=6.12.6-1
'http://http.debian.net/debian/pool/main/l/linux/linux_6.12.6-1.dsc' linux_6.12.6-1.dsc 204594 SHA256:2c54b4b3201cf7552a35af22fc5210824796f2bdf9210005ef6635f72d214ed0
'http://http.debian.net/debian/pool/main/l/linux/linux_6.12.6.orig.tar.xz' linux_6.12.6.orig.tar.xz 150922048 SHA256:d027b4b03de7cbb4e6c67bafb2cf24e772701550611523635d16da88ae1974e2
'http://http.debian.net/debian/pool/main/l/linux/linux_6.12.6-1.debian.tar.xz' linux_6.12.6-1.debian.tar.xz 1562024 SHA256:deee32b730b6a7b3ae5d7c3b763801b723760ba076e998727c3a96ddc95687c4
```

### `dpkg` source package: `littler=0.3.20-2`

Binary Packages:

- `littler=0.3.20-2`
- `r-cran-littler=0.3.20-2`

Licenses: (parsed from: `/usr/share/doc/littler/copyright`, `/usr/share/doc/r-cran-littler/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris littler=0.3.20-2
'http://http.debian.net/debian/pool/main/l/littler/littler_0.3.20-2.dsc' littler_0.3.20-2.dsc 1874 SHA256:a1372228b6acae61f4dd566fa4b02cc074ffc1d00dcd6abd65ea54ee70f5d8c0
'http://http.debian.net/debian/pool/main/l/littler/littler_0.3.20.orig.tar.gz' littler_0.3.20.orig.tar.gz 125661 SHA256:9810cca571878782afdd579d81404eb8a951ea4b9171d6bf7bdee7d7ed5b065a
'http://http.debian.net/debian/pool/main/l/littler/littler_0.3.20-2.debian.tar.xz' littler_0.3.20-2.debian.tar.xz 7040 SHA256:8b0a8bdd2595d22c0cb6ab5ab1cf8e013d1ff0aa73a68a8095f7589103975462
```

### `dpkg` source package: `lz4=1.9.4-3`

Binary Packages:

- `liblz4-1:amd64=1.9.4-3+b1`

Licenses: (parsed from: `/usr/share/doc/liblz4-1/copyright`)

- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris lz4=1.9.4-3
'http://http.debian.net/debian/pool/main/l/lz4/lz4_1.9.4-3.dsc' lz4_1.9.4-3.dsc 1934 SHA256:30365311787d4d9753a83d88dad9fa4a085e075db5cdee50be54b241f1265abb
'http://http.debian.net/debian/pool/main/l/lz4/lz4_1.9.4.orig.tar.gz' lz4_1.9.4.orig.tar.gz 354063 SHA256:0b0e3aa07c8c063ddf40b082bdf7e37a1562bda40a0ff5272957f3e987e0e54b
'http://http.debian.net/debian/pool/main/l/lz4/lz4_1.9.4-3.debian.tar.xz' lz4_1.9.4-3.debian.tar.xz 7076 SHA256:199c96cd86297cde59c56286ecd1b4ffa334dc73c0f54d39b5058f7e0b73a31c
```

### `dpkg` source package: `make-dfsg=4.4.1-1`

Binary Packages:

- `make=4.4.1-1`

Licenses: (parsed from: `/usr/share/doc/make/copyright`)

- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris make-dfsg=4.4.1-1
'http://http.debian.net/debian/pool/main/m/make-dfsg/make-dfsg_4.4.1-1.dsc' make-dfsg_4.4.1-1.dsc 1976 SHA256:4207e14d2dfceadcfabd1bc5b392b37b004afe2670e76cff27d607c8a8f1e3ef
'http://http.debian.net/debian/pool/main/m/make-dfsg/make-dfsg_4.4.1.orig.tar.xz' make-dfsg_4.4.1.orig.tar.xz 1125180 SHA256:3b16b00ea1079af9f8096bbc71ff7cc00c249fc6a862003da3c42308a0adb0fe
'http://http.debian.net/debian/pool/main/m/make-dfsg/make-dfsg_4.4.1-1.debian.tar.xz' make-dfsg_4.4.1-1.debian.tar.xz 44572 SHA256:5fa0b82841979963c0512ef2147698fc24adb5f8d783172d7a3c6d68e3464f7e
```

### `dpkg` source package: `mawk=1.3.4.20240905-1`

Binary Packages:

- `mawk=1.3.4.20240905-1`

Licenses: (parsed from: `/usr/share/doc/mawk/copyright`)

- `CC-BY-3.0`
- `GPL-2`
- `GPL-2.0-only`
- `X11`

Source:

```console
$ apt-get source -qq --print-uris mawk=1.3.4.20240905-1
'http://http.debian.net/debian/pool/main/m/mawk/mawk_1.3.4.20240905-1.dsc' mawk_1.3.4.20240905-1.dsc 2969 SHA256:df6bed9b7f37975fb7228fa5a3eb381bfe67cb3f3a4333ea8e69ddab4c881177
'http://http.debian.net/debian/pool/main/m/mawk/mawk_1.3.4.20240905.orig.tar.gz' mawk_1.3.4.20240905.orig.tar.gz 423935 SHA256:a39967927dfa1b0116efc45b944a0f5b5b4c34f8e842a4b223dcdd7b367399e0
'http://http.debian.net/debian/pool/main/m/mawk/mawk_1.3.4.20240905.orig.tar.gz.asc' mawk_1.3.4.20240905.orig.tar.gz.asc 729 SHA256:4360beec9fc972eba02f7af0a5340bd9a420c810d2424f50d34104b17386ac56
'http://http.debian.net/debian/pool/main/m/mawk/mawk_1.3.4.20240905-1.debian.tar.xz' mawk_1.3.4.20240905-1.debian.tar.xz 15980 SHA256:3908cbe4d9c42f8cca1f2d3a5c77d6a9a630696c375ac25b99a19277d7925443
```

### `dpkg` source package: `mgcv=1.9-1-1`

Binary Packages:

- `r-cran-mgcv=1.9-1-1`

Licenses: (parsed from: `/usr/share/doc/r-cran-mgcv/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris mgcv=1.9-1-1
'http://http.debian.net/debian/pool/main/m/mgcv/mgcv_1.9-1-1.dsc' mgcv_1.9-1-1.dsc 1826 SHA256:402384fa1204a1101155a3c265e71927396ebad3a97a57c817db7e24cf5b4b94
'http://http.debian.net/debian/pool/main/m/mgcv/mgcv_1.9-1.orig.tar.gz' mgcv_1.9-1.orig.tar.gz 1083217 SHA256:700fbc37bedd3a49505b9bc4949faee156d9cfb4f669d797d06a10a15a5bdb32
'http://http.debian.net/debian/pool/main/m/mgcv/mgcv_1.9-1-1.debian.tar.xz' mgcv_1.9-1-1.debian.tar.xz 5528 SHA256:cf18ffe6e93b47a69db0b2c8d577312230fbe4bd3ce2fb2a050f8efa86593076
```

### `dpkg` source package: `mpclib3=1.3.1-1`

Binary Packages:

- `libmpc3:amd64=1.3.1-1+b3`

Licenses: (parsed from: `/usr/share/doc/libmpc3/copyright`)

- `LGPL-3`

Source:

```console
$ apt-get source -qq --print-uris mpclib3=1.3.1-1
'http://http.debian.net/debian/pool/main/m/mpclib3/mpclib3_1.3.1-1.dsc' mpclib3_1.3.1-1.dsc 1877 SHA256:b2252a499fd0f8e92ce2cf7d8e68477ffc9dd06127803a91f0a1115822efec75
'http://http.debian.net/debian/pool/main/m/mpclib3/mpclib3_1.3.1.orig.tar.gz' mpclib3_1.3.1.orig.tar.gz 773573 SHA256:ab642492f5cf882b74aa0cb730cd410a81edcdbec895183ce930e706c1c759b8
'http://http.debian.net/debian/pool/main/m/mpclib3/mpclib3_1.3.1-1.debian.tar.xz' mpclib3_1.3.1-1.debian.tar.xz 4656 SHA256:25adb496258adacad69c022d712f96fbc465bcef9fd4751829dc351d9ce6a45d
```

### `dpkg` source package: `mpfr4=4.2.1-1`

Binary Packages:

- `libmpfr6:amd64=4.2.1-1+b2`

Licenses: (parsed from: `/usr/share/doc/libmpfr6/copyright`)

- `GFDL-1.2`
- `LGPL-3`

Source:

```console
$ apt-get source -qq --print-uris mpfr4=4.2.1-1
'http://http.debian.net/debian/pool/main/m/mpfr4/mpfr4_4.2.1-1.dsc' mpfr4_4.2.1-1.dsc 1959 SHA256:2fb0ea6c37591f03c7f3445fc6a298a10dbd9d7662ccb441f7da0e514d71986a
'http://http.debian.net/debian/pool/main/m/mpfr4/mpfr4_4.2.1.orig.tar.xz' mpfr4_4.2.1.orig.tar.xz 1493608 SHA256:277807353a6726978996945af13e52829e3abd7a9a5b7fb2793894e18f1fcbb2
'http://http.debian.net/debian/pool/main/m/mpfr4/mpfr4_4.2.1-1.debian.tar.xz' mpfr4_4.2.1-1.debian.tar.xz 12556 SHA256:06c6c90efe3653d44527bcd6cfd66563d62409bbb348eb32f33b480e30ad9993
```

### `dpkg` source package: `ncurses=6.5-2`

Binary Packages:

- `libncurses-dev:amd64=6.5-2+b1`
- `libncurses6:amd64=6.5-2+b1`
- `libncursesw6:amd64=6.5-2+b1`
- `libtinfo6:amd64=6.5-2+b1`
- `ncurses-base=6.5-2`
- `ncurses-bin=6.5-2+b1`

Licenses: (parsed from: `/usr/share/doc/libncurses-dev/copyright`, `/usr/share/doc/libncurses6/copyright`, `/usr/share/doc/libncursesw6/copyright`, `/usr/share/doc/libtinfo6/copyright`, `/usr/share/doc/ncurses-base/copyright`, `/usr/share/doc/ncurses-bin/copyright`)

- `BSD-3-clause`
- `MIT/X11`
- `X11`

Source:

```console
$ apt-get source -qq --print-uris ncurses=6.5-2
'http://http.debian.net/debian/pool/main/n/ncurses/ncurses_6.5-2.dsc' ncurses_6.5-2.dsc 3799 SHA256:c55a25d4697a881a12f98d9e69448a879fca1391663768822a7cc981b62b2b4c
'http://http.debian.net/debian/pool/main/n/ncurses/ncurses_6.5.orig.tar.gz' ncurses_6.5.orig.tar.gz 3688489 SHA256:136d91bc269a9a5785e5f9e980bc76ab57428f604ce3e5a5a90cebc767971cc6
'http://http.debian.net/debian/pool/main/n/ncurses/ncurses_6.5.orig.tar.gz.asc' ncurses_6.5.orig.tar.gz.asc 729 SHA256:c7541cdb9e27c159548d6ab2115b4e923d06d174dce7307f4a943de9421f3751
'http://http.debian.net/debian/pool/main/n/ncurses/ncurses_6.5-2.debian.tar.xz' ncurses_6.5-2.debian.tar.xz 49852 SHA256:19df80accc1c6d978ca54eba2542ea77248e7a894bbf42a093aee0b4981fddf3
```

### `dpkg` source package: `nettle=3.10-1`

Binary Packages:

- `libhogweed6t64:amd64=3.10-1+b1`
- `libnettle8t64:amd64=3.10-1+b1`

Licenses: (parsed from: `/usr/share/doc/libhogweed6t64/copyright`, `/usr/share/doc/libnettle8t64/copyright`)

- `Expat`
- `GAP`
- `GPL`
- `GPL-2`
- `GPL-2+`
- `GPL-3+ with Autoconf exception`
- `LGPL`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-3+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris nettle=3.10-1
'http://http.debian.net/debian/pool/main/n/nettle/nettle_3.10-1.dsc' nettle_3.10-1.dsc 2276 SHA256:25c9563ad861d8c62246687cc1aaace7d897db0e1aa287ef68485b89687aa739
'http://http.debian.net/debian/pool/main/n/nettle/nettle_3.10.orig.tar.gz' nettle_3.10.orig.tar.gz 2640485 SHA256:b4c518adb174e484cb4acea54118f02380c7133771e7e9beb98a0787194ee47c
'http://http.debian.net/debian/pool/main/n/nettle/nettle_3.10.orig.tar.gz.asc' nettle_3.10.orig.tar.gz.asc 573 SHA256:83f20f4bb5cc18335dacab8b8d01ddbae1b28453d889c5efcc2123987a8e09ca
'http://http.debian.net/debian/pool/main/n/nettle/nettle_3.10-1.debian.tar.xz' nettle_3.10-1.debian.tar.xz 24936 SHA256:fd7181ca135b8a560b048ffba5b9f75e2ce7d0d61d3223c278c77ea89500b660
```

### `dpkg` source package: `nghttp2=1.64.0-1`

Binary Packages:

- `libnghttp2-14:amd64=1.64.0-1`

Licenses: (parsed from: `/usr/share/doc/libnghttp2-14/copyright`)

- `BSD-2-clause`
- `Expat`
- `GPL-3`
- `GPL-3+ with autoconf exception`
- `MIT`
- `all-permissive`

Source:

```console
$ apt-get source -qq --print-uris nghttp2=1.64.0-1
'http://http.debian.net/debian/pool/main/n/nghttp2/nghttp2_1.64.0-1.dsc' nghttp2_1.64.0-1.dsc 2531 SHA256:2707e30147f7f5c5562245f1760876476798cf0cac10a9784f8e66a4d14d42a3
'http://http.debian.net/debian/pool/main/n/nghttp2/nghttp2_1.64.0.orig.tar.gz' nghttp2_1.64.0.orig.tar.gz 1069782 SHA256:b452dc69a1fcbc9375389b8b154175d8b7b125cdd713fc426774c2b79a1ebd77
'http://http.debian.net/debian/pool/main/n/nghttp2/nghttp2_1.64.0-1.debian.tar.xz' nghttp2_1.64.0-1.debian.tar.xz 38888 SHA256:3085083399b3f02bfc00e9b4f9c286ddd33c9624b622713a55ebbd8c398625eb
```

### `dpkg` source package: `nlme=3.1.166-1`

Binary Packages:

- `r-cran-nlme=3.1.166-1`

Licenses: (parsed from: `/usr/share/doc/r-cran-nlme/copyright`)

- `GPL`
- `GPL `

Source:

```console
$ apt-get source -qq --print-uris nlme=3.1.166-1
'http://http.debian.net/debian/pool/main/n/nlme/nlme_3.1.166-1.dsc' nlme_3.1.166-1.dsc 1840 SHA256:d2bb805e8e2ba75d986cbc6fb957d7ef45102fda36f5c1c34f7f1832fde634ae
'http://http.debian.net/debian/pool/main/n/nlme/nlme_3.1.166.orig.tar.gz' nlme_3.1.166.orig.tar.gz 847668 SHA256:237a14ee8d78755b11a7efe234b95be40b46fbdd1b4aaf463f6d532be1909762
'http://http.debian.net/debian/pool/main/n/nlme/nlme_3.1.166-1.debian.tar.xz' nlme_3.1.166-1.debian.tar.xz 7356 SHA256:323169f8f85f6bf81d11726bd56f867cee4adc422a607b53f4093c2bfe3be035
```

### `dpkg` source package: `openblas=0.3.28+ds-4`

Binary Packages:

- `libopenblas0-pthread:amd64=0.3.28+ds-4`

Licenses: (parsed from: `/usr/share/doc/libopenblas0-pthread/copyright`)

- `Apache-2.0`
- `BSD-2-clause`
- `BSD-2-clause-texas`
- `BSD-3-clause`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris openblas=0.3.28+ds-4
'http://http.debian.net/debian/pool/main/o/openblas/openblas_0.3.28%2bds-4.dsc' openblas_0.3.28+ds-4.dsc 4553 SHA256:860e640caba9c7803373ca21855b4ff3f0ebfbf40f0359133723c171f9ee17d6
'http://http.debian.net/debian/pool/main/o/openblas/openblas_0.3.28%2bds.orig.tar.xz' openblas_0.3.28+ds.orig.tar.xz 2181324 SHA256:938211591b6ad62285830021192b2a0f98bca70cc7f9aac68edca56e1c4e380d
'http://http.debian.net/debian/pool/main/o/openblas/openblas_0.3.28%2bds-4.debian.tar.xz' openblas_0.3.28+ds-4.debian.tar.xz 25780 SHA256:6d84590990f0a8f4787ea29fcd09d7f63ff2ccd31418c907c49abe67e0200f8c
```

### `dpkg` source package: `openldap=2.5.19+dfsg-1`

Binary Packages:

- `libldap-2.5-0:amd64=2.5.19+dfsg-1`

Licenses: (parsed from: `/usr/share/doc/libldap-2.5-0/copyright`)

- `BSD-3-clause`
- `BSD-3-clause-California`
- `BSD-3-clause-variant`
- `BSD-4-clause-California`
- `Beerware`
- `Expat`
- `Expat-ISC`
- `Expat-UNM`
- `F5`
- `FSF-unlimited`
- `GPL-2`
- `GPL-2+`
- `GPL-2+ with Autoconf exception`
- `GPL-2+ with Libtool exception`
- `GPL-3`
- `GPL-3+`
- `GPL-3+ with Autoconf exception`
- `GPL-3+ with Libtool exception`
- `JCG`
- `MIT-XC`
- `NeoSoft-permissive`
- `OpenLDAP-2.8`
- `UMich`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris openldap=2.5.19+dfsg-1
'http://http.debian.net/debian/pool/main/o/openldap/openldap_2.5.19%2bdfsg-1.dsc' openldap_2.5.19+dfsg-1.dsc 3312 SHA256:c2819be9061fe0752ef8bd1e1df4c1fbcc494fce95d504c6614f6a8e64ce5d10
'http://http.debian.net/debian/pool/main/o/openldap/openldap_2.5.19%2bdfsg.orig.tar.xz' openldap_2.5.19+dfsg.orig.tar.xz 3718696 SHA256:8a81909c9a816f8a0eb374d290a540b82e9331e4a7b3e4cf7de75bc6437a723c
'http://http.debian.net/debian/pool/main/o/openldap/openldap_2.5.19%2bdfsg-1.debian.tar.xz' openldap_2.5.19+dfsg-1.debian.tar.xz 170420 SHA256:610de35516d759e47ac81b6158b09b52b4f952bb564cba1fb9eec6bb50b1d10f
```

### `dpkg` source package: `openssl=3.3.2-2`

Binary Packages:

- `libssl3t64:amd64=3.3.2-2`
- `openssl=3.3.2-2`
- `openssl-provider-legacy=3.3.2-2`

Licenses: (parsed from: `/usr/share/doc/libssl3t64/copyright`, `/usr/share/doc/openssl/copyright`, `/usr/share/doc/openssl-provider-legacy/copyright`)

- `Apache-2.0`
- `Artistic`
- `GPL-1`
- `GPL-1+`

Source:

```console
$ apt-get source -qq --print-uris openssl=3.3.2-2
'http://http.debian.net/debian/pool/main/o/openssl/openssl_3.3.2-2.dsc' openssl_3.3.2-2.dsc 2808 SHA256:4a2d357c049c5f0da96fb9615e6ddbfface5a71de1dfa8a95120a251d1a3105d
'http://http.debian.net/debian/pool/main/o/openssl/openssl_3.3.2.orig.tar.gz' openssl_3.3.2.orig.tar.gz 18076531 SHA256:2e8a40b01979afe8be0bbfb3de5dc1c6709fedb46d6c89c10da114ab5fc3d281
'http://http.debian.net/debian/pool/main/o/openssl/openssl_3.3.2.orig.tar.gz.asc' openssl_3.3.2.orig.tar.gz.asc 833 SHA256:8a9ba21af0d770b3f9ee098269cfeb220a8b296639e6ad5d0593ffb7a15a742b
'http://http.debian.net/debian/pool/main/o/openssl/openssl_3.3.2-2.debian.tar.xz' openssl_3.3.2-2.debian.tar.xz 52228 SHA256:d5d0c7c5a35e10b580b016866a75a454da3b477f90516501fa1861989befc33b
```

### `dpkg` source package: `p11-kit=0.25.5-2`

Binary Packages:

- `libp11-kit0:amd64=0.25.5-2+b1`

Licenses: (parsed from: `/usr/share/doc/libp11-kit0/copyright`)

- `Apache-2.0`
- `BSD-3-clause`
- `FSFAP`
- `FSFULLR`
- `GPL-2+ with Autoconf-data exception`
- `GPL-3+ with Autoconf-data exception`
- `ISC`
- `LGPL-2.1`
- `LGPL-2.1+`
- `X11`
- `customFSFUL`
- `customFSFULLRWD`

Source:

```console
$ apt-get source -qq --print-uris p11-kit=0.25.5-2
'http://deb.debian.org/debian/pool/main/p/p11-kit/p11-kit_0.25.5-2.dsc' p11-kit_0.25.5-2.dsc 2538 SHA256:5953f5639503fe32217117e222bbc231130d9e79dda74259b4017b7bfc5bd910
'http://deb.debian.org/debian/pool/main/p/p11-kit/p11-kit_0.25.5.orig.tar.xz' p11-kit_0.25.5.orig.tar.xz 1002056 SHA256:04d0a86450cdb1be018f26af6699857171a188ac6d5b8c90786a60854e1198e5
'http://deb.debian.org/debian/pool/main/p/p11-kit/p11-kit_0.25.5.orig.tar.xz.asc' p11-kit_0.25.5.orig.tar.xz.asc 228 SHA256:066c92b9d2accb2fda6a2f71e676fb6526fcc153051b1f04ee7d7c8c96a09989
'http://deb.debian.org/debian/pool/main/p/p11-kit/p11-kit_0.25.5-2.debian.tar.xz' p11-kit_0.25.5-2.debian.tar.xz 24108 SHA256:df84eb66f6dd2a53796dfbb2edc58a4b37046b19a8d186baf072163cd6c9c528
```

Other potentially useful URLs:

- https://sources.debian.net/src/p11-kit/0.25.5-2/ (for browsing the source)
- https://sources.debian.net/src/p11-kit/0.25.5-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/p11-kit/0.25.5-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `pam=1.5.3-7`

Binary Packages:

- `libpam-modules:amd64=1.5.3-7+b1`
- `libpam-modules-bin=1.5.3-7+b1`
- `libpam-runtime=1.5.3-7`
- `libpam0g:amd64=1.5.3-7+b1`

Licenses: (parsed from: `/usr/share/doc/libpam-modules/copyright`, `/usr/share/doc/libpam-modules-bin/copyright`, `/usr/share/doc/libpam-runtime/copyright`, `/usr/share/doc/libpam0g/copyright`)

- `BSD-3-clause`
- `BSD-tcp_wrappers`
- `Beerware`
- `GPL`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+ with Bison exception`
- `LGPL-2`
- `LGPL-2+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris pam=1.5.3-7
'http://http.debian.net/debian/pool/main/p/pam/pam_1.5.3-7.dsc' pam_1.5.3-7.dsc 2253 SHA256:05666dde2c8057ff436975a5da7dad91210ab5a5dfdaea43976ac4a6bc75b1e7
'http://http.debian.net/debian/pool/main/p/pam/pam_1.5.3.orig.tar.xz' pam_1.5.3.orig.tar.xz 1020076 SHA256:7ac4b50feee004a9fa88f1dfd2d2fa738a82896763050cd773b3c54b0a818283
'http://http.debian.net/debian/pool/main/p/pam/pam_1.5.3.orig.tar.xz.asc' pam_1.5.3.orig.tar.xz.asc 801 SHA256:ce5690766060d60a8f0fba447f480d8d49988821740698cbdf2ecfd84dc8895c
'http://http.debian.net/debian/pool/main/p/pam/pam_1.5.3-7.debian.tar.xz' pam_1.5.3-7.debian.tar.xz 139288 SHA256:494106a8f40a5436b82f8955e04a83598439b48636f16a30d0b6a32d86d0fc61
```

### `dpkg` source package: `pango1.0=1.55.0+ds-3`

Binary Packages:

- `libpango-1.0-0:amd64=1.55.0+ds-3`
- `libpangocairo-1.0-0:amd64=1.55.0+ds-3`
- `libpangoft2-1.0-0:amd64=1.55.0+ds-3`

Licenses: (parsed from: `/usr/share/doc/libpango-1.0-0/copyright`, `/usr/share/doc/libpangocairo-1.0-0/copyright`, `/usr/share/doc/libpangoft2-1.0-0/copyright`)

- `Apache-2`
- `Apache-2.0`
- `Bitstream-Vera`
- `Chromium-BSD-style`
- `Example`
- `ICU`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `OFL-1.1`
- `TCL`
- `Unicode`

Source:

```console
$ apt-get source -qq --print-uris pango1.0=1.55.0+ds-3
'http://http.debian.net/debian/pool/main/p/pango1.0/pango1.0_1.55.0%2bds-3.dsc' pango1.0_1.55.0+ds-3.dsc 3699 SHA256:4416d6562e5691382eca3e05c1394cb03a51fc35756f907861ec022d4898289f
'http://http.debian.net/debian/pool/main/p/pango1.0/pango1.0_1.55.0%2bds.orig.tar.xz' pango1.0_1.55.0+ds.orig.tar.xz 1878496 SHA256:93d98c0931d081b1d06869287c05007bebabad5419ff2cf66723d9e01d6afb4d
'http://http.debian.net/debian/pool/main/p/pango1.0/pango1.0_1.55.0%2bds-3.debian.tar.xz' pango1.0_1.55.0+ds-3.debian.tar.xz 43500 SHA256:6a5c4b7e0a7876901d475f016f13bb40c53f832f82c0dfc20e53f50b667d36a0
```

### `dpkg` source package: `patch=2.7.6-7`

Binary Packages:

- `patch=2.7.6-7`

Licenses: (parsed from: `/usr/share/doc/patch/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris patch=2.7.6-7
'http://http.debian.net/debian/pool/main/p/patch/patch_2.7.6-7.dsc' patch_2.7.6-7.dsc 1706 SHA256:d954fd576d935ac54b7d44d4976eb52d0da84a57f7bad90c6e5bd5e33595030a
'http://http.debian.net/debian/pool/main/p/patch/patch_2.7.6.orig.tar.xz' patch_2.7.6.orig.tar.xz 783756 SHA256:ac610bda97abe0d9f6b7c963255a11dcb196c25e337c61f94e4778d632f1d8fd
'http://http.debian.net/debian/pool/main/p/patch/patch_2.7.6-7.debian.tar.xz' patch_2.7.6-7.debian.tar.xz 15084 SHA256:7725f30b042d8cf63516e480036e93ca2ff0ce5ad3754db4a4e69d33e96a2624
```

### `dpkg` source package: `pcre2=10.44-5`

Binary Packages:

- `libpcre2-16-0:amd64=10.44-5`
- `libpcre2-32-0:amd64=10.44-5`
- `libpcre2-8-0:amd64=10.44-5`
- `libpcre2-dev:amd64=10.44-5`
- `libpcre2-posix3:amd64=10.44-5`

Licenses: (parsed from: `/usr/share/doc/libpcre2-16-0/copyright`, `/usr/share/doc/libpcre2-32-0/copyright`, `/usr/share/doc/libpcre2-8-0/copyright`, `/usr/share/doc/libpcre2-dev/copyright`, `/usr/share/doc/libpcre2-posix3/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `BSD-3-clause-Cambridge with BINARY LIBRARY-LIKE PACKAGES exception`
- `X11`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris pcre2=10.44-5
'http://http.debian.net/debian/pool/main/p/pcre2/pcre2_10.44-5.dsc' pcre2_10.44-5.dsc 2340 SHA256:6c27cbc1f6d00a5465b1f312363cec6a35a624a670475d13df21cc7cc8d54923
'http://http.debian.net/debian/pool/main/p/pcre2/pcre2_10.44.orig.tar.gz' pcre2_10.44.orig.tar.gz 2552792 SHA256:86b9cb0aa3bcb7994faa88018292bc704cdbb708e785f7c74352ff6ea7d3175b
'http://http.debian.net/debian/pool/main/p/pcre2/pcre2_10.44-5.diff.gz' pcre2_10.44-5.diff.gz 16032 SHA256:6077896df1f7fff961a3ee82ff29d571694f7fd85f030fc60d67f9bc326c395e
```

### `dpkg` source package: `perl=5.40.0-8`

Binary Packages:

- `libperl5.40:amd64=5.40.0-8`
- `perl=5.40.0-8`
- `perl-base=5.40.0-8`
- `perl-modules-5.40=5.40.0-8`

Licenses: (parsed from: `/usr/share/doc/libperl5.40/copyright`, `/usr/share/doc/perl/copyright`, `/usr/share/doc/perl-base/copyright`, `/usr/share/doc/perl-modules-5.40/copyright`)

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
- `FSFAP`
- `GPL-1`
- `GPL-1+`
- `GPL-2`
- `GPL-2+`
- `GPL-3+-WITH-BISON-EXCEPTION`
- `LGPL-2.1`
- `REGCOMP`
- `REGCOMP,`
- `SDBM-PUBLIC-DOMAIN`
- `TEXT-TABS`
- `Unicode`
- `ZLIB`

Source:

```console
$ apt-get source -qq --print-uris perl=5.40.0-8
'http://http.debian.net/debian/pool/main/p/perl/perl_5.40.0-8.dsc' perl_5.40.0-8.dsc 2933 SHA256:8e28c6d3de17f273c8c56888c6e9ae18f76f680e5bb4f805b4abb5f8d1da5387
'http://http.debian.net/debian/pool/main/p/perl/perl_5.40.0.orig-regen-configure.tar.xz' perl_5.40.0.orig-regen-configure.tar.xz 421080 SHA256:9b1f7f1f680cfd0174d1e11b4f8d06cce079798a0549f083f1c9ba15156be211
'http://http.debian.net/debian/pool/main/p/perl/perl_5.40.0.orig.tar.xz' perl_5.40.0.orig.tar.xz 13804184 SHA256:d5325300ad267624cb0b7d512cfdfcd74fa7fe00c455c5b51a6bd53e5e199ef9
'http://http.debian.net/debian/pool/main/p/perl/perl_5.40.0-8.debian.tar.xz' perl_5.40.0-8.debian.tar.xz 168236 SHA256:dc3776e2abbef5be6d533b8f9ce926b5770ae36025386679476fdf237e33f736
```

### `dpkg` source package: `pixman=0.44.0-3`

Binary Packages:

- `libpixman-1-0:amd64=0.44.0-3`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris pixman=0.44.0-3
'http://http.debian.net/debian/pool/main/p/pixman/pixman_0.44.0-3.dsc' pixman_0.44.0-3.dsc 2019 SHA256:b05388a6cb71550a2ed425e9689b09b1dc458fa06d842f87328ede5e0eb7345f
'http://http.debian.net/debian/pool/main/p/pixman/pixman_0.44.0.orig.tar.gz' pixman_0.44.0.orig.tar.gz 812995 SHA256:89a4c1e1e45e0b23dffe708202cb2eaffde0fe3727d7692b2e1739fec78a7dac
'http://http.debian.net/debian/pool/main/p/pixman/pixman_0.44.0-3.diff.gz' pixman_0.44.0-3.diff.gz 9417 SHA256:820f71488852530f2a662bb6bdcc8bd8e065a15800d8b459d7ec69e6ffc98a85
```

### `dpkg` source package: `pkgconf=1.8.1-4`

Binary Packages:

- `libpkgconf3:amd64=1.8.1-4`
- `pkgconf:amd64=1.8.1-4`
- `pkgconf-bin=1.8.1-4`

Licenses: (parsed from: `/usr/share/doc/libpkgconf3/copyright`, `/usr/share/doc/pkgconf/copyright`, `/usr/share/doc/pkgconf-bin/copyright`)

- `BSD-2`
- `BSD-4`
- `GPL-2`
- `GPL-2+`
- `ISC`
- `X11`

Source:

```console
$ apt-get source -qq --print-uris pkgconf=1.8.1-4
'http://http.debian.net/debian/pool/main/p/pkgconf/pkgconf_1.8.1-4.dsc' pkgconf_1.8.1-4.dsc 2130 SHA256:782a764448d1ecf39f80c7a1747c28fcbde1800b615eee6a46639a17e58b62f9
'http://http.debian.net/debian/pool/main/p/pkgconf/pkgconf_1.8.1.orig.tar.xz' pkgconf_1.8.1.orig.tar.xz 302372 SHA256:644361ada2942be05655d4452eb018791647c31bba429b287f1f68deb2dc6840
'http://http.debian.net/debian/pool/main/p/pkgconf/pkgconf_1.8.1-4.debian.tar.xz' pkgconf_1.8.1-4.debian.tar.xz 17736 SHA256:e56c56a5f40eb0d57bebcb79983a755e16cf1e1595a6fec7f02b20bd58baa734
```

### `dpkg` source package: `procps=2:4.0.4-6`

Binary Packages:

- `libproc2-0:amd64=2:4.0.4-6`
- `procps=2:4.0.4-6`

Licenses: (parsed from: `/usr/share/doc/libproc2-0/copyright`, `/usr/share/doc/procps/copyright`)

- `GPL-2`
- `GPL-2.0+`
- `LGPL-2`
- `LGPL-2.0+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris procps=2:4.0.4-6
'http://http.debian.net/debian/pool/main/p/procps/procps_4.0.4-6.dsc' procps_4.0.4-6.dsc 2124 SHA256:dd3c79032588cac32413c5d1d1dd164a79eacc14af57636bacd6c62c4c1b12d1
'http://http.debian.net/debian/pool/main/p/procps/procps_4.0.4.orig.tar.xz' procps_4.0.4.orig.tar.xz 1401540 SHA256:22870d6feb2478adb617ce4f09a787addaf2d260c5a8aa7b17d889a962c5e42e
'http://http.debian.net/debian/pool/main/p/procps/procps_4.0.4-6.debian.tar.xz' procps_4.0.4-6.debian.tar.xz 29412 SHA256:8c7106ed54c4c4151e53e230b6abc605b880307c349e94dde186d131c863811d
```

### `dpkg` source package: `r-base=4.4.2-1`

Binary Packages:

- `r-base=4.4.2-1`
- `r-base-core=4.4.2-1`
- `r-base-dev=4.4.2-1`
- `r-recommended=4.4.2-1`

Licenses: (parsed from: `/usr/share/doc/r-base/copyright`, `/usr/share/doc/r-base-core/copyright`, `/usr/share/doc/r-base-dev/copyright`, `/usr/share/doc/r-recommended/copyright`)

- `Artistic`
- `GPL-2`
- `GPL-3`
- `LGPL-2`
- `LGPL-2.1`
- `LGPL-3`

Source:

```console
$ apt-get source -qq --print-uris r-base=4.4.2-1
'http://http.debian.net/debian/pool/main/r/r-base/r-base_4.4.2-1.dsc' r-base_4.4.2-1.dsc 2906 SHA256:4a4ea52c4f43ad386e94ef76d7de4818b6f0be43aa8d3bdbf7c2d1ef51ab5611
'http://http.debian.net/debian/pool/main/r/r-base/r-base_4.4.2.orig.tar.gz' r-base_4.4.2.orig.tar.gz 37582785 SHA256:1578cd603e8d866b58743e49d8bf99c569e81079b6a60cf33cdf7bdffeb817ec
'http://http.debian.net/debian/pool/main/r/r-base/r-base_4.4.2-1.debian.tar.xz' r-base_4.4.2-1.debian.tar.xz 100592 SHA256:c17da84e76400bc6f38a489c867c4a5e112fa8f685f01bb7f60ce42caf604d36
```

### `dpkg` source package: `r-cran-class=7.3-22-2`

Binary Packages:

- `r-cran-class=7.3-22-2`

Licenses: (parsed from: `/usr/share/doc/r-cran-class/copyright`)

- `GPL-2`
- `GPL-2 | GPL-3`

Source:

```console
$ apt-get source -qq --print-uris r-cran-class=7.3-22-2
'http://http.debian.net/debian/pool/main/r/r-cran-class/r-cran-class_7.3-22-2.dsc' r-cran-class_7.3-22-2.dsc 1873 SHA256:f1b705a3b059c4315228192b468c007b1414f26834a5ef5ea985ac7f928afdc2
'http://http.debian.net/debian/pool/main/r/r-cran-class/r-cran-class_7.3-22.orig.tar.gz' r-cran-class_7.3-22.orig.tar.gz 20812 SHA256:b6994164e93843fcc7e08dfdc8c8b4af6a5a10ef7153d2e72a6855342508d15c
'http://http.debian.net/debian/pool/main/r/r-cran-class/r-cran-class_7.3-22-2.debian.tar.xz' r-cran-class_7.3-22-2.debian.tar.xz 3300 SHA256:1c13438d7b1645c7f4b027488d93b4362698de4805b8a75c121d7a5ca8579098
```

### `dpkg` source package: `r-cran-docopt=0.7.1-2`

Binary Packages:

- `r-cran-docopt=0.7.1-2`

Licenses: (parsed from: `/usr/share/doc/r-cran-docopt/copyright`)

- `MIT`

Source:

```console
$ apt-get source -qq --print-uris r-cran-docopt=0.7.1-2
'http://http.debian.net/debian/pool/main/r/r-cran-docopt/r-cran-docopt_0.7.1-2.dsc' r-cran-docopt_0.7.1-2.dsc 2087 SHA256:f7713b448b9b14766351e295d3ee0059f3a1c6319ecdf5ef33d5da40bc609d1b
'http://http.debian.net/debian/pool/main/r/r-cran-docopt/r-cran-docopt_0.7.1.orig.tar.gz' r-cran-docopt_0.7.1.orig.tar.gz 29465 SHA256:9f473887e4607e9b21fd4ab02e802858d0ac2ca6dad9e357a9d884a47fe4b0ff
'http://http.debian.net/debian/pool/main/r/r-cran-docopt/r-cran-docopt_0.7.1-2.debian.tar.xz' r-cran-docopt_0.7.1-2.debian.tar.xz 2472 SHA256:3358c9988254f326b3d2a351f3a75fd3c655d56de13e7f822cceaf39fb1f7fca
```

### `dpkg` source package: `r-cran-mass=7.3-61-1`

Binary Packages:

- `r-cran-mass=7.3-61-1`

Licenses: (parsed from: `/usr/share/doc/r-cran-mass/copyright`)

- `GPL-2`
- `GPL-2 | GPL-3`

Source:

```console
$ apt-get source -qq --print-uris r-cran-mass=7.3-61-1
'http://http.debian.net/debian/pool/main/r/r-cran-mass/r-cran-mass_7.3-61-1.dsc' r-cran-mass_7.3-61-1.dsc 1851 SHA256:a06aee48f3cc177c2a66acd60878ac75efdad0b4b69a8eef25c8cc6c5f52e9a6
'http://http.debian.net/debian/pool/main/r/r-cran-mass/r-cran-mass_7.3-61.orig.tar.gz' r-cran-mass_7.3-61.orig.tar.gz 509902 SHA256:3144c8bf579dd7b7c47c259728c27f53f53e294e7ed307da434dfd144e800a90
'http://http.debian.net/debian/pool/main/r/r-cran-mass/r-cran-mass_7.3-61-1.debian.tar.xz' r-cran-mass_7.3-61-1.debian.tar.xz 6616 SHA256:397bb8aa1ca89c4b93eea30ea7050c983821a84eff3256e09a12fddb4b17a03e
```

### `dpkg` source package: `r-cran-nnet=7.3-19-2`

Binary Packages:

- `r-cran-nnet=7.3-19-2`

Licenses: (parsed from: `/usr/share/doc/r-cran-nnet/copyright`)

- `GPL-2`
- `GPL-2 | GPL-3`

Source:

```console
$ apt-get source -qq --print-uris r-cran-nnet=7.3-19-2
'http://http.debian.net/debian/pool/main/r/r-cran-nnet/r-cran-nnet_7.3-19-2.dsc' r-cran-nnet_7.3-19-2.dsc 1848 SHA256:02c98934d24d70696c760e0e4fa8fae998a6ea275eb039ab140ef30d564523a3
'http://http.debian.net/debian/pool/main/r/r-cran-nnet/r-cran-nnet_7.3-19.orig.tar.gz' r-cran-nnet_7.3-19.orig.tar.gz 29152 SHA256:a9241f469270d3b03bbab7dc0d3c6a06a84010af16ba82fd3bd6660b35382ce7
'http://http.debian.net/debian/pool/main/r/r-cran-nnet/r-cran-nnet_7.3-19-2.debian.tar.xz' r-cran-nnet_7.3-19-2.debian.tar.xz 3332 SHA256:49aaccdda8d36b3f195ba69de26066b2e1245803a9ab4dafa536589fa85977b7
```

### `dpkg` source package: `r-cran-spatial=7.3-17-1`

Binary Packages:

- `r-cran-spatial=7.3-17-1`

Licenses: (parsed from: `/usr/share/doc/r-cran-spatial/copyright`)

- `GPL-2`
- `GPL-2 | GPL-3`

Source:

```console
$ apt-get source -qq --print-uris r-cran-spatial=7.3-17-1
'http://http.debian.net/debian/pool/main/r/r-cran-spatial/r-cran-spatial_7.3-17-1.dsc' r-cran-spatial_7.3-17-1.dsc 1884 SHA256:2b53f753efcdc641ef16e58e1bed93ee4a9d7bf52864e95359422d6c5ad4b5c0
'http://http.debian.net/debian/pool/main/r/r-cran-spatial/r-cran-spatial_7.3-17.orig.tar.gz' r-cran-spatial_7.3-17.orig.tar.gz 44661 SHA256:f1003ed8cff2a47169a4787c8be46e8c2c501cc06c8b1e5f97bf62507e5f5dd7
'http://http.debian.net/debian/pool/main/r/r-cran-spatial/r-cran-spatial_7.3-17-1.debian.tar.xz' r-cran-spatial_7.3-17-1.debian.tar.xz 3224 SHA256:1299d2624d2cd604237e97116659b15f60eb6bb6179c5265cee1b89a6b708fe8
```

### `dpkg` source package: `readline=8.2-6`

Binary Packages:

- `libreadline-dev:amd64=8.2-6`
- `libreadline8t64:amd64=8.2-6`
- `readline-common=8.2-6`

Licenses: (parsed from: `/usr/share/doc/libreadline-dev/copyright`, `/usr/share/doc/libreadline8t64/copyright`, `/usr/share/doc/readline-common/copyright`)

- `GFDL`
- `GFDL-NIV-1.3+`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `ISC-no-attribution`

Source:

```console
$ apt-get source -qq --print-uris readline=8.2-6
'http://http.debian.net/debian/pool/main/r/readline/readline_8.2-6.dsc' readline_8.2-6.dsc 2810 SHA256:6f94c7144d6b6b1ff88aaebd81480e87f8773b7638031782aac12ef93ffd2e71
'http://http.debian.net/debian/pool/main/r/readline/readline_8.2.orig.tar.gz' readline_8.2.orig.tar.gz 3043952 SHA256:3feb7171f16a84ee82ca18a36d7b9be109a52c04f492a053331d7d1095007c35
'http://http.debian.net/debian/pool/main/r/readline/readline_8.2-6.debian.tar.xz' readline_8.2-6.debian.tar.xz 38396 SHA256:d1cf806644dbce298cf929f1cc9b3af5a50cd7db97b6f69db280c1eb2f544376
```

### `dpkg` source package: `rmatrix=1.7-1-1`

Binary Packages:

- `r-cran-matrix=1.7-1-1`

Licenses: (parsed from: `/usr/share/doc/r-cran-matrix/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris rmatrix=1.7-1-1
'http://http.debian.net/debian/pool/main/r/rmatrix/rmatrix_1.7-1-1.dsc' rmatrix_1.7-1-1.dsc 1860 SHA256:df99e963a6303e43882e1ab2ea44807bfa392ca28af5ca82cd4de673f9f78c10
'http://http.debian.net/debian/pool/main/r/rmatrix/rmatrix_1.7-1.orig.tar.gz' rmatrix_1.7-1.orig.tar.gz 2480082 SHA256:a2cabbf04e4e2cafbd0a04281f130bb58e4f7653a91951368a404ef8682b38a1
'http://http.debian.net/debian/pool/main/r/rmatrix/rmatrix_1.7-1-1.debian.tar.xz' rmatrix_1.7-1-1.debian.tar.xz 6068 SHA256:a5632c6829dfe7967b728d10cf3ab2a5d2f56601f962da225a94044ca7c06dbe
```

### `dpkg` source package: `rpart=4.1.23-1`

Binary Packages:

- `r-cran-rpart=4.1.23-1`

Licenses: (parsed from: `/usr/share/doc/r-cran-rpart/copyright`)

- `GPL-2`
- `GPL-2+ | license included below`

Source:

```console
$ apt-get source -qq --print-uris rpart=4.1.23-1
'http://http.debian.net/debian/pool/main/r/rpart/rpart_4.1.23-1.dsc' rpart_4.1.23-1.dsc 1843 SHA256:84bfc4124dbebd5c3f22a7789ce61cb85d78bef62d8aa617e9438948996b0ac2
'http://http.debian.net/debian/pool/main/r/rpart/rpart_4.1.23.orig.tar.gz' rpart_4.1.23.orig.tar.gz 618016 SHA256:f9b89aed6aa6cea656a2dcb271574e969ce2b1c98beb07bd91e17339f6daabaf
'http://http.debian.net/debian/pool/main/r/rpart/rpart_4.1.23-1.debian.tar.xz' rpart_4.1.23-1.debian.tar.xz 4424 SHA256:5cb2cd24d3faede047e4637de541ddf5dc350ad1309ba0cc3c8e974328ee34f3
```

### `dpkg` source package: `rpcsvc-proto=1.4.3-1`

Binary Packages:

- `rpcsvc-proto=1.4.3-1`

Licenses: (parsed from: `/usr/share/doc/rpcsvc-proto/copyright`)

- `BSD-3-clause`
- `GPL-2`
- `GPL-2+-autoconf-exception`
- `GPL-3`
- `GPL-3+-autoconf-exception`
- `MIT`
- `permissive-autoconf-m4`
- `permissive-autoconf-m4-no-warranty`
- `permissive-configure`
- `permissive-fsf`
- `permissive-makefile-in`

Source:

```console
$ apt-get source -qq --print-uris rpcsvc-proto=1.4.3-1
'http://http.debian.net/debian/pool/main/r/rpcsvc-proto/rpcsvc-proto_1.4.3-1.dsc' rpcsvc-proto_1.4.3-1.dsc 1999 SHA256:7d8e122bd18b02fe0de6d467a0ecdafff74035b3e1ed0da1c0c792d9c015682f
'http://http.debian.net/debian/pool/main/r/rpcsvc-proto/rpcsvc-proto_1.4.3.orig.tar.xz' rpcsvc-proto_1.4.3.orig.tar.xz 167964 SHA256:69315e94430f4e79c74d43422f4a36e6259e97e67e2677b2c7d7060436bd99b1
'http://http.debian.net/debian/pool/main/r/rpcsvc-proto/rpcsvc-proto_1.4.3-1.debian.tar.xz' rpcsvc-proto_1.4.3-1.debian.tar.xz 4228 SHA256:02034b9dadcf3af5424f72eb65c3842c8d7117b6b78e7a3c798316ceb60843d1
```

### `dpkg` source package: `rtmpdump=2.4+20151223.gitfa8646d.1-2`

Binary Packages:

- `librtmp1:amd64=2.4+20151223.gitfa8646d.1-2+b5`

Licenses: (parsed from: `/usr/share/doc/librtmp1/copyright`)

- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris rtmpdump=2.4+20151223.gitfa8646d.1-2
'http://http.debian.net/debian/pool/main/r/rtmpdump/rtmpdump_2.4%2b20151223.gitfa8646d.1-2.dsc' rtmpdump_2.4+20151223.gitfa8646d.1-2.dsc 2299 SHA256:a296819cd2ab5880b67ad963ef0867cb10e462f4403e52565aa863eb05bb1370
'http://http.debian.net/debian/pool/main/r/rtmpdump/rtmpdump_2.4%2b20151223.gitfa8646d.1.orig.tar.gz' rtmpdump_2.4+20151223.gitfa8646d.1.orig.tar.gz 142213 SHA256:5c032f5c8cc2937eb55a81a94effdfed3b0a0304b6376147b86f951e225e3ab5
'http://http.debian.net/debian/pool/main/r/rtmpdump/rtmpdump_2.4%2b20151223.gitfa8646d.1-2.debian.tar.xz' rtmpdump_2.4+20151223.gitfa8646d.1-2.debian.tar.xz 8096 SHA256:26d47de07d16285e4ca55b0828cbbf1ba35e671f9b3500a87e301fe755d26882
```

### `dpkg` source package: `sed=4.9-2`

Binary Packages:

- `sed=4.9-2`

Licenses: (parsed from: `/usr/share/doc/sed/copyright`)

- `BSD-4-clause-UC`
- `BSL-1`
- `GFDL-1.3`
- `GFDL-NIV-1.3+`
- `GPL-3`
- `GPL-3+`
- `ISC`
- `X11`
- `pcre`

Source:

```console
$ apt-get source -qq --print-uris sed=4.9-2
'http://http.debian.net/debian/pool/main/s/sed/sed_4.9-2.dsc' sed_4.9-2.dsc 1860 SHA256:17f10deac1b327cb2a623352cdc33444ac9c109359a0caa46b3980b0e415f671
'http://http.debian.net/debian/pool/main/s/sed/sed_4.9.orig.tar.xz' sed_4.9.orig.tar.xz 1397092 SHA256:6e226b732e1cd739464ad6862bd1a1aba42d7982922da7a53519631d24975181
'http://http.debian.net/debian/pool/main/s/sed/sed_4.9-2.debian.tar.xz' sed_4.9-2.debian.tar.xz 62756 SHA256:549fa5cec6eb4fde8cc74ca263b8bf42f947ede677e39d2afeedf661da1d4e52
```

### `dpkg` source package: `sensible-utils=0.0.24`

Binary Packages:

- `sensible-utils=0.0.24`

Licenses: (parsed from: `/usr/share/doc/sensible-utils/copyright`)

- `All-permissive`
- `GPL-2`
- `GPL-2+`
- `configure`
- `installsh`

Source:

```console
$ apt-get source -qq --print-uris sensible-utils=0.0.24
'http://http.debian.net/debian/pool/main/s/sensible-utils/sensible-utils_0.0.24.dsc' sensible-utils_0.0.24.dsc 1743 SHA256:f84ac7cccca8e0f3f9e5c0d5173c7d1f22afdc0a98210120d1d35a92b4baf9df
'http://http.debian.net/debian/pool/main/s/sensible-utils/sensible-utils_0.0.24.tar.xz' sensible-utils_0.0.24.tar.xz 73568 SHA256:620602b900bad2b9856556a7895ea146110f602cd526a1cc03068a0bc9542803
```

### `dpkg` source package: `shadow=1:4.16.0-7`

Binary Packages:

- `login.defs=1:4.16.0-7`
- `passwd=1:4.16.0-7`

Licenses: (parsed from: `/usr/share/doc/login.defs/copyright`, `/usr/share/doc/passwd/copyright`)

- `BSD-3-clause`
- `GPL-1`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris shadow=1:4.16.0-7
'http://http.debian.net/debian/pool/main/s/shadow/shadow_4.16.0-7.dsc' shadow_4.16.0-7.dsc 2614 SHA256:c43f54503e32265b335a5a26c49b98371277dba2f8d189f2a76ff64365f94003
'http://http.debian.net/debian/pool/main/s/shadow/shadow_4.16.0.orig.tar.xz' shadow_4.16.0.orig.tar.xz 2053720 SHA256:a0255570541a356c3718966987c8be0658691fda804826fda7576c8e69e0cfda
'http://http.debian.net/debian/pool/main/s/shadow/shadow_4.16.0-7.debian.tar.xz' shadow_4.16.0-7.debian.tar.xz 170412 SHA256:24af58e3025ca769fcd9ce3e08f21059dcb85c3b14df93687c2b3d4cbace71d2
```

### `dpkg` source package: `survival=3.7-0-1`

Binary Packages:

- `r-cran-survival=3.7-0-1`

Licenses: (parsed from: `/usr/share/doc/r-cran-survival/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris survival=3.7-0-1
'http://deb.debian.org/debian/pool/main/s/survival/survival_3.7-0-1.dsc' survival_3.7-0-1.dsc 1861 SHA256:c92017025736f7ac54a3de80be0308712394fb16a7254c4767a77d9a33a1b79b
'http://deb.debian.org/debian/pool/main/s/survival/survival_3.7-0.orig.tar.gz' survival_3.7-0.orig.tar.gz 6918683 SHA256:cd96b08ec928b0028f69c942cc788e190b4543c8518d71deb6d8a712de44feef
'http://deb.debian.org/debian/pool/main/s/survival/survival_3.7-0-1.debian.tar.xz' survival_3.7-0-1.debian.tar.xz 6368 SHA256:0477f8f04224af8b57003d3b1c7609b5007075c925c799311d02d05807b119bc
```

Other potentially useful URLs:

- https://sources.debian.net/src/survival/3.7-0-1/ (for browsing the source)
- https://sources.debian.net/src/survival/3.7-0-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/survival/3.7-0-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `systemd=257-2`

Binary Packages:

- `libsystemd0:amd64=257-2`
- `libudev1:amd64=257-2`

Licenses: (parsed from: `/usr/share/doc/libsystemd0/copyright`, `/usr/share/doc/libudev1/copyright`)

- `CC0-1.0`
- `Expat`
- `GPL-2`
- `GPL-2 with Linux-syscall-note exception`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/systemd/257-2/


### `dpkg` source package: `sysvinit=3.11-1`

Binary Packages:

- `sysvinit-utils=3.11-1`

Licenses: (parsed from: `/usr/share/doc/sysvinit-utils/copyright`)

- `GPL-2`
- `GPL-2.0`
- `GPL-2.0+`
- `GPL-3`
- `GPL-3.0`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris sysvinit=3.11-1
'http://http.debian.net/debian/pool/main/s/sysvinit/sysvinit_3.11-1.dsc' sysvinit_3.11-1.dsc 2347 SHA256:ba903d31738ab67544f8517f97c316909db1151da4218423b2a5666322842634
'http://http.debian.net/debian/pool/main/s/sysvinit/sysvinit_3.11.orig.tar.gz' sysvinit_3.11.orig.tar.gz 514791 SHA256:32dd3370c2fb55cac87ee6b8e25074f769fd3ef1122ecfbb19fd7fea8a4d0414
'http://http.debian.net/debian/pool/main/s/sysvinit/sysvinit_3.11-1.debian.tar.xz' sysvinit_3.11-1.debian.tar.xz 121272 SHA256:8fd6c705ebc0c5136e7ecbf2819eabf4fbba66476a3778cdd44d7ff9e8495205
```

### `dpkg` source package: `tar=1.35+dfsg-3`

Binary Packages:

- `tar=1.35+dfsg-3`

Licenses: (parsed from: `/usr/share/doc/tar/copyright`)

- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `GPL-3+ with Bison exception`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`
- `LGPL-3+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/tar/1.35+dfsg-3/


### `dpkg` source package: `tcl8.6=8.6.15+dfsg-2`

Binary Packages:

- `libtcl8.6:amd64=8.6.15+dfsg-2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris tcl8.6=8.6.15+dfsg-2
'http://http.debian.net/debian/pool/main/t/tcl8.6/tcl8.6_8.6.15%2bdfsg-2.dsc' tcl8.6_8.6.15+dfsg-2.dsc 2120 SHA256:1b70dab97b2cf1834f63e408f70dd463643e08f92f7821cdef1c1a0589d22976
'http://http.debian.net/debian/pool/main/t/tcl8.6/tcl8.6_8.6.15%2bdfsg.orig.tar.gz' tcl8.6_8.6.15+dfsg.orig.tar.gz 7032260 SHA256:4d8a1f3a7e069bf567ee7dac82a8955279157681a13460fc993cd20194972de3
'http://http.debian.net/debian/pool/main/t/tcl8.6/tcl8.6_8.6.15%2bdfsg-2.debian.tar.xz' tcl8.6_8.6.15+dfsg-2.debian.tar.xz 14456 SHA256:acfc1c879dc1d6af2dafebca3ae2ea03a44ee8bb9eea313f929518975be077e6
```

### `dpkg` source package: `tex-gyre=20180621-6`

Binary Packages:

- `fonts-texgyre=20180621-6`

Licenses: (parsed from: `/usr/share/doc/fonts-texgyre/copyright`)

- `DejaVu-License`
- `GPL-2`
- `GPL-2+`
- `GUST-Font-License`

Source:

```console
$ apt-get source -qq --print-uris tex-gyre=20180621-6
'http://http.debian.net/debian/pool/main/t/tex-gyre/tex-gyre_20180621-6.dsc' tex-gyre_20180621-6.dsc 2241 SHA256:83a26e65fee0ac79f31a44e083e03da2fef7b031c70d0f336796782cc0fed099
'http://http.debian.net/debian/pool/main/t/tex-gyre/tex-gyre_20180621.orig.tar.gz' tex-gyre_20180621.orig.tar.gz 24033627 SHA256:fe6b0f8ca6890d4a369f36c3b45bc30470069701a2f59042178ad5933fc9cdb8
'http://http.debian.net/debian/pool/main/t/tex-gyre/tex-gyre_20180621-6.debian.tar.xz' tex-gyre_20180621-6.debian.tar.xz 11632 SHA256:731e04abb52038a7de626e4679d6b823b2d692be029bb88399951fb69b286f67
```

### `dpkg` source package: `tiff=4.5.1+git230720-5`

Binary Packages:

- `libtiff6:amd64=4.5.1+git230720-5`

Licenses: (parsed from: `/usr/share/doc/libtiff6/copyright`)

- `Hylafax`

Source:

```console
$ apt-get source -qq --print-uris tiff=4.5.1+git230720-5
'http://http.debian.net/debian/pool/main/t/tiff/tiff_4.5.1%2bgit230720-5.dsc' tiff_4.5.1+git230720-5.dsc 2322 SHA256:bef3be0797e0117a34abdab78b398294adc28947f891978f7e1264d45e0cbec8
'http://http.debian.net/debian/pool/main/t/tiff/tiff_4.5.1%2bgit230720.orig.tar.xz' tiff_4.5.1+git230720.orig.tar.xz 1781896 SHA256:0e51bcf3a3ffa5fc76ea6aeb74a797f95c84544fcc8b6a1ec5def967a78e9e12
'http://http.debian.net/debian/pool/main/t/tiff/tiff_4.5.1%2bgit230720-5.debian.tar.xz' tiff_4.5.1+git230720-5.debian.tar.xz 26764 SHA256:01c212410561b6a4ff00f3449def450a782c21db55ebc1820e82500dc503fe07
```

### `dpkg` source package: `tk8.6=8.6.15-1`

Binary Packages:

- `libtk8.6:amd64=8.6.15-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris tk8.6=8.6.15-1
'http://http.debian.net/debian/pool/main/t/tk8.6/tk8.6_8.6.15-1.dsc' tk8.6_8.6.15-1.dsc 2155 SHA256:eed4e29c1685bf635db4e9b812692a88fdb834afb3b7284bbcd23bcff12373cd
'http://http.debian.net/debian/pool/main/t/tk8.6/tk8.6_8.6.15.orig.tar.gz' tk8.6_8.6.15.orig.tar.gz 4590766 SHA256:550969f35379f952b3020f3ab7b9dd5bfd11c1ef7c9b7c6a75f5c49aca793fec
'http://http.debian.net/debian/pool/main/t/tk8.6/tk8.6_8.6.15-1.debian.tar.xz' tk8.6_8.6.15-1.debian.tar.xz 10792 SHA256:ff09a6e900825d78d996f5e71a7808ed856530cbab5219eee7835a3e5567aa24
```

### `dpkg` source package: `tzdata=2024b-4`

Binary Packages:

- `tzdata=2024b-4`

Licenses: (parsed from: `/usr/share/doc/tzdata/copyright`)

- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris tzdata=2024b-4
'http://http.debian.net/debian/pool/main/t/tzdata/tzdata_2024b-4.dsc' tzdata_2024b-4.dsc 2429 SHA256:baa6f241342304f528f52306bc434f725fd9c483a0d258871cf6c8504d6a1ef7
'http://http.debian.net/debian/pool/main/t/tzdata/tzdata_2024b.orig.tar.gz' tzdata_2024b.orig.tar.gz 459393 SHA256:70e754db126a8d0db3d16d6b4cb5f7ec1e04d5f261255e4558a67fe92d39e550
'http://http.debian.net/debian/pool/main/t/tzdata/tzdata_2024b.orig.tar.gz.asc' tzdata_2024b.orig.tar.gz.asc 833 SHA256:5bc86ae1ee1f600eefefd5377faf5519d4863c960efb625286638d077178d883
'http://http.debian.net/debian/pool/main/t/tzdata/tzdata_2024b-4.debian.tar.xz' tzdata_2024b-4.debian.tar.xz 124468 SHA256:ef869fc42e8e9e0e9f230d23e4972bacf553bb2d5c8e1468fe71059a233dc3fb
```

### `dpkg` source package: `ucf=3.0046`

Binary Packages:

- `ucf=3.0046`

Licenses: (parsed from: `/usr/share/doc/ucf/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris ucf=3.0046
'http://http.debian.net/debian/pool/main/u/ucf/ucf_3.0046.dsc' ucf_3.0046.dsc 1512 SHA256:21e5e780515e0db2bf21c021cc8d511d70eee64b0ee4cd0e4e38e95c109ea4b3
'http://http.debian.net/debian/pool/main/u/ucf/ucf_3.0046.tar.xz' ucf_3.0046.tar.xz 67032 SHA256:cb5114f63a9351c34c8ad51090eac50a53bcd0c1fc92ae21d758ac91ab8c5a39
```

### `dpkg` source package: `unzip=6.0-28`

Binary Packages:

- `unzip=6.0-28`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris unzip=6.0-28
'http://http.debian.net/debian/pool/main/u/unzip/unzip_6.0-28.dsc' unzip_6.0-28.dsc 1359 SHA256:f5b486028b61a145b591fdd96aaeaf89ef6eef164a299f43bd5e6704bdefc8a2
'http://http.debian.net/debian/pool/main/u/unzip/unzip_6.0.orig.tar.gz' unzip_6.0.orig.tar.gz 1376845 SHA256:036d96991646d0449ed0aa952e4fbe21b476ce994abc276e49d30e686708bd37
'http://http.debian.net/debian/pool/main/u/unzip/unzip_6.0-28.debian.tar.xz' unzip_6.0-28.debian.tar.xz 25032 SHA256:e51364116c84739c591728ecc841113a914fa11358fd10ff0d6813524d811bb9
```

### `dpkg` source package: `usrmerge=39`

Binary Packages:

- `usr-is-merged=39`

Licenses: (parsed from: `/usr/share/doc/usr-is-merged/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris usrmerge=39
'http://http.debian.net/debian/pool/main/u/usrmerge/usrmerge_39.dsc' usrmerge_39.dsc 981 SHA256:44027067423faefd31ac321c283fc9b07184fecbd5304ed41490c03825b89a28
'http://http.debian.net/debian/pool/main/u/usrmerge/usrmerge_39.tar.xz' usrmerge_39.tar.xz 14908 SHA256:90b4ee198469292da4ee8b4ce2ec7b3ec439d61e6beb3ed9d3fa82b0e46e7fa3
```

### `dpkg` source package: `util-linux=2.40.2-12`

Binary Packages:

- `bsdutils=1:2.40.2-12`
- `libblkid1:amd64=2.40.2-12`
- `libmount1:amd64=2.40.2-12`
- `libsmartcols1:amd64=2.40.2-12`
- `libuuid1:amd64=2.40.2-12`
- `login=1:4.16.0-2+really2.40.2-12`
- `mount=2.40.2-12`
- `util-linux=2.40.2-12`

Licenses: (parsed from: `/usr/share/doc/bsdutils/copyright`, `/usr/share/doc/libblkid1/copyright`, `/usr/share/doc/libmount1/copyright`, `/usr/share/doc/libsmartcols1/copyright`, `/usr/share/doc/libuuid1/copyright`, `/usr/share/doc/login/copyright`, `/usr/share/doc/mount/copyright`, `/usr/share/doc/util-linux/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `BSD-4-clause`
- `BSLA`
- `Expat`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `ISC`
- `LGPL`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`
- `LGPL-3+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris util-linux=2.40.2-12
'http://http.debian.net/debian/pool/main/u/util-linux/util-linux_2.40.2-12.dsc' util-linux_2.40.2-12.dsc 5120 SHA256:16ece1c86c673d69cb1a19371b1cbaf5b300243a2519983b66c14186e119b32f
'http://http.debian.net/debian/pool/main/u/util-linux/util-linux_2.40.2.orig.tar.xz' util-linux_2.40.2.orig.tar.xz 8854820 SHA256:d78b37a66f5922d70edf3bdfb01a6b33d34ed3c3cafd6628203b2a2b67c8e8b3
'http://http.debian.net/debian/pool/main/u/util-linux/util-linux_2.40.2-12.debian.tar.xz' util-linux_2.40.2-12.debian.tar.xz 113456 SHA256:fd08132a8186d773c5e4dfd4f89cc48183fb01f1c92d15dcbf95bd508e3928af
```

### `dpkg` source package: `vim=2:9.1.0861-1`

Binary Packages:

- `vim-common=2:9.1.0861-1`
- `vim-tiny=2:9.1.0861-1`

Licenses: (parsed from: `/usr/share/doc/vim-common/copyright`, `/usr/share/doc/vim-tiny/copyright`)

- `Apache`
- `Apache-2.0`
- `Artistic`
- `Artistic-1`
- `BSD-2-clause`
- `BSD-3-clause`
- `Compaq`
- `EDL-1`
- `Expat`
- `GPL-1`
- `GPL-1+`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `OPL-1+`
- `UC`
- `Unlicense`
- `Vim`
- `Vim-Regexp`
- `X11`
- `XPM`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris vim=2:9.1.0861-1
'http://http.debian.net/debian/pool/main/v/vim/vim_9.1.0861-1.dsc' vim_9.1.0861-1.dsc 3230 SHA256:ebfc6908990d7f18fb84c77e5bf0976f24c158f9a1d877a835c9e0c28b0ed813
'http://http.debian.net/debian/pool/main/v/vim/vim_9.1.0861.orig.tar.xz' vim_9.1.0861.orig.tar.xz 12089652 SHA256:9cdb88b891770fb151c074d7a4957b3441ab0720b07af3e463c7dfd158b29f6b
'http://http.debian.net/debian/pool/main/v/vim/vim_9.1.0861-1.debian.tar.xz' vim_9.1.0861-1.debian.tar.xz 189148 SHA256:7b5c4ef0658f50d7d447649ecbdea2b3b4b5f5cdc4bd1195c1ffce8cc98a45ec
```

### `dpkg` source package: `wget=1.24.5-2`

Binary Packages:

- `wget=1.24.5-2+b1`

Licenses: (parsed from: `/usr/share/doc/wget/copyright`)

- `GFDL-1.2`
- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris wget=1.24.5-2
'http://http.debian.net/debian/pool/main/w/wget/wget_1.24.5-2.dsc' wget_1.24.5-2.dsc 2212 SHA256:6d0c93504683c1bcfcfcf0fe65bfb6d9d1e1e4f2a0f80719bb3bf41859731662
'http://http.debian.net/debian/pool/main/w/wget/wget_1.24.5.orig.tar.gz' wget_1.24.5.orig.tar.gz 5182521 SHA256:fa2dc35bab5184ecbc46a9ef83def2aaaa3f4c9f3c97d4bd19dcb07d4da637de
'http://http.debian.net/debian/pool/main/w/wget/wget_1.24.5.orig.tar.gz.asc' wget_1.24.5.orig.tar.gz.asc 854 SHA256:2991bfab0481793d3587d5e94531d1f48297877e1d1ff88d0bc03f1b0fb19fe5
'http://http.debian.net/debian/pool/main/w/wget/wget_1.24.5-2.debian.tar.xz' wget_1.24.5-2.debian.tar.xz 61884 SHA256:e0457915d31b96d1725c45ee8bf240a9d715cf23db972a09f4a49c32412e619e
```

### `dpkg` source package: `xauth=1:1.1.2-1.1`

Binary Packages:

- `xauth=1:1.1.2-1.1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris xauth=1:1.1.2-1.1
'http://http.debian.net/debian/pool/main/x/xauth/xauth_1.1.2-1.1.dsc' xauth_1.1.2-1.1.dsc 1828 SHA256:042ec790bd830c17bf1fe195d292f4eed29f0e095db1fb4e5156008ddda2ddd1
'http://http.debian.net/debian/pool/main/x/xauth/xauth_1.1.2.orig.tar.gz' xauth_1.1.2.orig.tar.gz 214621 SHA256:84d27a1023d8da524c134f424b312e53cb96e08871f96868aa20316bfcbbc054
'http://http.debian.net/debian/pool/main/x/xauth/xauth_1.1.2-1.1.diff.gz' xauth_1.1.2-1.1.diff.gz 18218 SHA256:763c20707faf0ba512294c83dcb2df4541e37eeb53eb596af608b0188de5243e
```

### `dpkg` source package: `xdg-utils=1.2.1-2`

Binary Packages:

- `xdg-utils=1.2.1-2`

Licenses: (parsed from: `/usr/share/doc/xdg-utils/copyright`)

- `Expat`

Source:

```console
$ apt-get source -qq --print-uris xdg-utils=1.2.1-2
'http://http.debian.net/debian/pool/main/x/xdg-utils/xdg-utils_1.2.1-2.dsc' xdg-utils_1.2.1-2.dsc 2137 SHA256:954ff8314f513926f03677d3ec830b8195eaf7714ba8d80d54547871049d6280
'http://http.debian.net/debian/pool/main/x/xdg-utils/xdg-utils_1.2.1.orig.tar.gz' xdg-utils_1.2.1.orig.tar.gz 307637 SHA256:f6b648c064464c2636884c05746e80428110a576f8daacf46ef2e554dcfdae75
'http://http.debian.net/debian/pool/main/x/xdg-utils/xdg-utils_1.2.1-2.debian.tar.xz' xdg-utils_1.2.1-2.debian.tar.xz 13612 SHA256:f288e1abb87d0b8a510776d55c5085e8f30ed6459f3f4a07dd9332a8d1162a98
```

### `dpkg` source package: `xft=2.3.6-1`

Binary Packages:

- `libxft2:amd64=2.3.6-1+b3`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris xft=2.3.6-1
'http://http.debian.net/debian/pool/main/x/xft/xft_2.3.6-1.dsc' xft_2.3.6-1.dsc 2006 SHA256:252220495bd12fac30d8f1b1994916beaed9c5149138dcc62e230fee17339530
'http://http.debian.net/debian/pool/main/x/xft/xft_2.3.6.orig.tar.gz' xft_2.3.6.orig.tar.gz 447498 SHA256:b7e59f69e0bbabe9438088775f7e5a7c16a572e58b11f9722519385d38192df5
'http://http.debian.net/debian/pool/main/x/xft/xft_2.3.6-1.diff.gz' xft_2.3.6-1.diff.gz 17995 SHA256:9d4c64fc52626134a3f753df88fceaba0cb460bd9b56544f0e42178deca77019
```

### `dpkg` source package: `xorg=1:7.7+23.1`

Binary Packages:

- `x11-common=1:7.7+23.1`

Licenses: (parsed from: `/usr/share/doc/x11-common/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris xorg=1:7.7+23.1
'http://http.debian.net/debian/pool/main/x/xorg/xorg_7.7%2b23.1.dsc' xorg_7.7+23.1.dsc 1983 SHA256:0d448530e9e3640a98bc3ac5840af8ab62f369bea0483eca9741d508987d19c1
'http://http.debian.net/debian/pool/main/x/xorg/xorg_7.7%2b23.1.tar.gz' xorg_7.7+23.1.tar.gz 292366 SHA256:1620333d14424eadae77ef44ac702a65ef5b53c169c993181687ee1d198d538b
```

### `dpkg` source package: `xxhash=0.8.2-2`

Binary Packages:

- `libxxhash0:amd64=0.8.2-2+b2`

Licenses: (parsed from: `/usr/share/doc/libxxhash0/copyright`)

- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris xxhash=0.8.2-2
'http://http.debian.net/debian/pool/main/x/xxhash/xxhash_0.8.2-2.dsc' xxhash_0.8.2-2.dsc 1969 SHA256:8fbf9f5a50a4cf48e771e157e386bd2b2938e46cecd4bc53117ee1a4a615af1d
'http://http.debian.net/debian/pool/main/x/xxhash/xxhash_0.8.2.orig.tar.gz' xxhash_0.8.2.orig.tar.gz 1141188 SHA256:baee0c6afd4f03165de7a4e67988d16f0f2b257b51d0e3cb91909302a26a79c4
'http://http.debian.net/debian/pool/main/x/xxhash/xxhash_0.8.2-2.debian.tar.xz' xxhash_0.8.2-2.debian.tar.xz 4920 SHA256:fcbdd52df60936173524743680f6d3c504b9a90553fe113cd0aa531faf4f2c4d
```

### `dpkg` source package: `xz-utils=5.6.3-1`

Binary Packages:

- `liblzma-dev:amd64=5.6.3-1+b1`
- `liblzma5:amd64=5.6.3-1+b1`
- `xz-utils=5.6.3-1+b1`

Licenses: (parsed from: `/usr/share/doc/liblzma-dev/copyright`, `/usr/share/doc/liblzma5/copyright`, `/usr/share/doc/xz-utils/copyright`)

- `0BSD`
- `FSFUL`
- `FSFULLR`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3.0-or-later-WITH-Autoconf-exception-macro`
- `LGPL-2.1`
- `LGPL-2.1+`
- `PD`
- `PD-debian`
- `noderivs`
- `none`
- `permissive-nowarranty`

Source:

```console
$ apt-get source -qq --print-uris xz-utils=5.6.3-1
'http://http.debian.net/debian/pool/main/x/xz-utils/xz-utils_5.6.3-1.dsc' xz-utils_5.6.3-1.dsc 2704 SHA256:840b9ae0e893d043de548c6df65a3a957dcd3977723eccf308ae8a61bb5dd288
'http://http.debian.net/debian/pool/main/x/xz-utils/xz-utils_5.6.3.orig.tar.xz' xz-utils_5.6.3.orig.tar.xz 1328224 SHA256:db0590629b6f0fa36e74aea5f9731dc6f8df068ce7b7bafa45301832a5eebc3a
'http://http.debian.net/debian/pool/main/x/xz-utils/xz-utils_5.6.3.orig.tar.xz.asc' xz-utils_5.6.3.orig.tar.xz.asc 833 SHA256:76b873c890e0b2cc0d3e790183d58acad724a8856a9ecb8491e127e5e5049837
'http://http.debian.net/debian/pool/main/x/xz-utils/xz-utils_5.6.3-1.debian.tar.xz' xz-utils_5.6.3-1.debian.tar.xz 24548 SHA256:5de83aba4db209d8a30b9aaa390a8009086c42e1575a92182cb234c73c784f58
```

### `dpkg` source package: `zip=3.0-14`

Binary Packages:

- `zip=3.0-14`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris zip=3.0-14
'http://http.debian.net/debian/pool/main/z/zip/zip_3.0-14.dsc' zip_3.0-14.dsc 1335 SHA256:8f868b949e1ed397a9ae83f6ea384efc6ecdfadd38d964cfdb30b86966f433a3
'http://http.debian.net/debian/pool/main/z/zip/zip_3.0.orig.tar.gz' zip_3.0.orig.tar.gz 1118845 SHA256:f0e8bb1f9b7eb0b01285495a2699df3a4b766784c1765a8f1aeedf63c0806369
'http://http.debian.net/debian/pool/main/z/zip/zip_3.0-14.debian.tar.xz' zip_3.0-14.debian.tar.xz 9160 SHA256:b479d23f1d1070b2053cc8311494a21f1d46ee404c8a0446ea740b8ad2d25a6d
```

### `dpkg` source package: `zlib=1:1.3.dfsg+really1.3.1-1`

Binary Packages:

- `zlib1g:amd64=1:1.3.dfsg+really1.3.1-1+b1`
- `zlib1g-dev:amd64=1:1.3.dfsg+really1.3.1-1+b1`

Licenses: (parsed from: `/usr/share/doc/zlib1g/copyright`, `/usr/share/doc/zlib1g-dev/copyright`)

- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris zlib=1:1.3.dfsg+really1.3.1-1
'http://http.debian.net/debian/pool/main/z/zlib/zlib_1.3.dfsg%2breally1.3.1-1.dsc' zlib_1.3.dfsg+really1.3.1-1.dsc 2637 SHA256:ede2791e29c1d3b422f9208bdd7edf040c20445ea1e7453a72037576e64fa197
'http://http.debian.net/debian/pool/main/z/zlib/zlib_1.3.dfsg%2breally1.3.1.orig.tar.gz' zlib_1.3.dfsg+really1.3.1.orig.tar.gz 1325737 SHA256:60dd315c07f616887caa029408308a018ace66e3d142726a97db164b3b8f69fb
'http://http.debian.net/debian/pool/main/z/zlib/zlib_1.3.dfsg%2breally1.3.1-1.debian.tar.xz' zlib_1.3.dfsg+really1.3.1-1.debian.tar.xz 16576 SHA256:9ed525955ce9fb0c1b39be8ff98f73450dbfc6305a9a27e6149c8972d38a0a9e
```
