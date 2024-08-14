# `r-base:4.4.1`

## Docker Metadata

- Image ID: `sha256:41138379afa1e9e804dcacdcdfcd06f5f173cb7f50f059905ef63159c97e48ed`
- Created: `2024-06-16T13:02:54Z`
- Virtual Size: ~ 858.25 Mb  
  (total size of all layers on-disk)
- Arch: `linux`/`amd64`
- Command: `["R"]`
- Environment:
  - `PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin`
  - `LC_ALL=en_US.UTF-8`
  - `LANG=en_US.UTF-8`
  - `R_BASE_VERSION=4.4.1`
- Labels:
  - `org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>`
  - `org.opencontainers.image.licenses=GPL-2.0-or-later`
  - `org.opencontainers.image.source=https://github.com/rocker-org/rocker`
  - `org.opencontainers.image.vendor=Rocker Project`

## `dpkg` (`.deb`-based packages)

### `dpkg` source package: `acl=2.3.2-2`

Binary Packages:

- `libacl1:amd64=2.3.2-2`

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

### `dpkg` source package: `apt=2.9.7`

Binary Packages:

- `apt=2.9.7`
- `libapt-pkg6.0t64:amd64=2.9.7`

Licenses: (parsed from: `/usr/share/doc/apt/copyright`, `/usr/share/doc/libapt-pkg6.0t64/copyright`)

- `BSD-3-clause`
- `Expat`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris apt=2.9.7
'http://deb.debian.org/debian/pool/main/a/apt/apt_2.9.7.dsc' apt_2.9.7.dsc 2973 SHA256:01507aa067a54dc47c998e53728dcd999e1eeddbffeaea3daaef66a98b3e9779
'http://deb.debian.org/debian/pool/main/a/apt/apt_2.9.7.tar.xz' apt_2.9.7.tar.xz 2385996 SHA256:cb99af6e1fe13d975c8d46c960af714d3bafdcfed8e151dd90a94695dd4ac15b
```

Other potentially useful URLs:

- https://sources.debian.net/src/apt/2.9.7/ (for browsing the source)
- https://sources.debian.net/src/apt/2.9.7/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/apt/2.9.7/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `attr=1:2.5.2-1`

Binary Packages:

- `libattr1:amd64=1:2.5.2-1`

Licenses: (parsed from: `/usr/share/doc/libattr1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2+`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris attr=1:2.5.2-1
'http://http.debian.net/debian/pool/main/a/attr/attr_2.5.2-1.dsc' attr_2.5.2-1.dsc 2477 SHA256:5c14953fc436d6c4ba6dd4a00b2f82a923d5745cc2c993a630e50d9cabaeca0b
'http://http.debian.net/debian/pool/main/a/attr/attr_2.5.2.orig.tar.xz' attr_2.5.2.orig.tar.xz 334180 SHA256:f2e97b0ab7ce293681ab701915766190d607a1dba7fae8a718138150b700a70b
'http://http.debian.net/debian/pool/main/a/attr/attr_2.5.2.orig.tar.xz.asc' attr_2.5.2.orig.tar.xz.asc 833 SHA256:eeac729088d3c6379e91b7596cb3582e46b047c47f0fa3c5c77f9c9e84dc3a4c
'http://http.debian.net/debian/pool/main/a/attr/attr_2.5.2-1.debian.tar.xz' attr_2.5.2-1.debian.tar.xz 25848 SHA256:b4d0670ea47811670bb619252973c7fb186e54b28bd5f2ac3c1a34d6fd089741
```

### `dpkg` source package: `audit=1:3.1.2-4`

Binary Packages:

- `libaudit-common=1:3.1.2-4`
- `libaudit1:amd64=1:3.1.2-4+b1`

Licenses: (parsed from: `/usr/share/doc/libaudit-common/copyright`, `/usr/share/doc/libaudit1/copyright`)

- `GPL-1`
- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris audit=1:3.1.2-4
'http://http.debian.net/debian/pool/main/a/audit/audit_3.1.2-4.dsc' audit_3.1.2-4.dsc 2408 SHA256:2c3e056802722d320d9bc37bb47e1999d2878772076c7f28621404fa8f07d871
'http://http.debian.net/debian/pool/main/a/audit/audit_3.1.2.orig.tar.gz' audit_3.1.2.orig.tar.gz 1219860 SHA256:c0b1792d1f0a88c6f1828710509cbb987059fc68712c97669ca90eae103d287d
'http://http.debian.net/debian/pool/main/a/audit/audit_3.1.2-4.debian.tar.xz' audit_3.1.2-4.debian.tar.xz 18724 SHA256:fa0f2f46093f2b76c960f08c66605a10c0de646383366dc26c32304676324ec6
```

### `dpkg` source package: `base-files=13.5`

Binary Packages:

- `base-files=13.5`

Licenses: (parsed from: `/usr/share/doc/base-files/copyright`)

- `GPL`
- `GPL-2+`
- `verbatim`

Source:

```console
$ apt-get source -qq --print-uris base-files=13.5
'http://http.debian.net/debian/pool/main/b/base-files/base-files_13.5.dsc' base-files_13.5.dsc 1100 SHA256:e5e4772aae38b90b23b882f18a277f9c9dc72f1861a0743bd26ec1af0a056492
'http://http.debian.net/debian/pool/main/b/base-files/base-files_13.5.tar.xz' base-files_13.5.tar.xz 68200 SHA256:a478a680b60c63c0ae78fef166ae681adc945b29a2aea4c2d03ba2921b72d419
```

### `dpkg` source package: `base-passwd=3.6.4`

Binary Packages:

- `base-passwd=3.6.4`

Licenses: (parsed from: `/usr/share/doc/base-passwd/copyright`)

- `GPL-2`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris base-passwd=3.6.4
'http://http.debian.net/debian/pool/main/b/base-passwd/base-passwd_3.6.4.dsc' base-passwd_3.6.4.dsc 1762 SHA256:83d6855b38a0ab900d28d14bc3a0c0b97c60d5461143e51ccc2b0f8f7ea92cc8
'http://http.debian.net/debian/pool/main/b/base-passwd/base-passwd_3.6.4.tar.xz' base-passwd_3.6.4.tar.xz 58420 SHA256:4b5232c5910932215b87bbde6f3c6c9a97021fe7902bd837b1ede8cc0be84a65
```

### `dpkg` source package: `bash=5.2.21-2.1`

Binary Packages:

- `bash=5.2.21-2.1+b1`

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
$ apt-get source -qq --print-uris bash=5.2.21-2.1
'http://http.debian.net/debian/pool/main/b/bash/bash_5.2.21-2.1.dsc' bash_5.2.21-2.1.dsc 2278 SHA256:97801c8f716396cd88cf8b69da3b6ea70f2b3ef6f9415df40e836d373feba536
'http://http.debian.net/debian/pool/main/b/bash/bash_5.2.21.orig.tar.xz' bash_5.2.21.orig.tar.xz 5598816 SHA256:ec21ab4efd6bd7a6e2802fbda622b81bfc43a8095d721234d4bf075797683014
'http://http.debian.net/debian/pool/main/b/bash/bash_5.2.21-2.1.debian.tar.xz' bash_5.2.21-2.1.debian.tar.xz 87940 SHA256:7452fd5408bd8415eee5e561a83d318972a584f10911818f8a8dd30e4f5acacd
```

### `dpkg` source package: `binutils=2.43-2`

Binary Packages:

- `binutils=2.43-2`
- `binutils-common:amd64=2.43-2`
- `binutils-x86-64-linux-gnu=2.43-2`
- `libbinutils:amd64=2.43-2`
- `libctf-nobfd0:amd64=2.43-2`
- `libctf0:amd64=2.43-2`
- `libgprofng0:amd64=2.43-2`
- `libsframe1:amd64=2.43-2`

Licenses: (parsed from: `/usr/share/doc/binutils/copyright`, `/usr/share/doc/binutils-common/copyright`, `/usr/share/doc/binutils-x86-64-linux-gnu/copyright`, `/usr/share/doc/libbinutils/copyright`, `/usr/share/doc/libctf-nobfd0/copyright`, `/usr/share/doc/libctf0/copyright`, `/usr/share/doc/libgprofng0/copyright`, `/usr/share/doc/libsframe1/copyright`)

- `GFDL`
- `GPL`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris binutils=2.43-2
'http://http.debian.net/debian/pool/main/b/binutils/binutils_2.43-2.dsc' binutils_2.43-2.dsc 12097 SHA256:a966b40dba64a61514a9c737277cf5a8a3366ce29f4aa7836b6a5f87f69211b4
'http://http.debian.net/debian/pool/main/b/binutils/binutils_2.43.orig.tar.xz' binutils_2.43.orig.tar.xz 28409824 SHA256:b52ba0bde25b710f92331e99e6d2e2afc72b86ca98b941c4acf3f4d2dcb17e1a
'http://http.debian.net/debian/pool/main/b/binutils/binutils_2.43-2.debian.tar.xz' binutils_2.43-2.debian.tar.xz 125160 SHA256:7bb6a84b544065839ff749cd91eab0865e06ac014253edb5c07aec77eb7503a9
```

### `dpkg` source package: `boot=1.3-30-1`

Binary Packages:

- `r-cran-boot=1.3-30-1`

Licenses: (parsed from: `/usr/share/doc/r-cran-boot/copyright`)

- `'unlimited distribution'`

Source:

```console
$ apt-get source -qq --print-uris boot=1.3-30-1
'http://http.debian.net/debian/pool/main/b/boot/boot_1.3-30-1.dsc' boot_1.3-30-1.dsc 1802 SHA256:8c98b1d49df72488902afd90c201e95b4415a483d6f4fdb1e66598a245b95273
'http://http.debian.net/debian/pool/main/b/boot/boot_1.3-30.orig.tar.gz' boot_1.3-30.orig.tar.gz 237087 SHA256:5509d62bd6e6c21b6ef352ab7846d89027bddbfb727fd0cf55da59558bd3fe97
'http://http.debian.net/debian/pool/main/b/boot/boot_1.3-30-1.debian.tar.xz' boot_1.3-30-1.debian.tar.xz 5372 SHA256:f29afa7c1c6ddce841935bf2dd56478d06a3cc89b2c0dc0ccba9021949b661ef
```

### `dpkg` source package: `brotli=1.1.0-2`

Binary Packages:

- `libbrotli1:amd64=1.1.0-2+b4`

Licenses: (parsed from: `/usr/share/doc/libbrotli1/copyright`)

- `MIT`

Source:

```console
$ apt-get source -qq --print-uris brotli=1.1.0-2
'http://http.debian.net/debian/pool/main/b/brotli/brotli_1.1.0-2.dsc' brotli_1.1.0-2.dsc 2261 SHA256:39b06802a852629132d549a7f7449dee7f435e801706714a4bc2ea2f15b28f36
'http://http.debian.net/debian/pool/main/b/brotli/brotli_1.1.0.orig.tar.gz' brotli_1.1.0.orig.tar.gz 512036 SHA256:10973f4b4199eafa1d5735ef661ddb2ec2f97319ee9fd1824d4aabe08cff5265
'http://http.debian.net/debian/pool/main/b/brotli/brotli_1.1.0-2.debian.tar.xz' brotli_1.1.0-2.debian.tar.xz 5480 SHA256:3d913a3740bcad9a294007575a6beb1846beadbd62b44fb2bf9fdaeddea3236f
```

### `dpkg` source package: `build-essential=12.10`

Binary Packages:

- `build-essential=12.10`

Licenses: (parsed from: `/usr/share/doc/build-essential/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris build-essential=12.10
'http://http.debian.net/debian/pool/main/b/build-essential/build-essential_12.10.dsc' build-essential_12.10.dsc 2172 SHA256:b2d9c962b539f011807fdd62761f749eed12a7f061d75c3752a48bd2060030d4
'http://http.debian.net/debian/pool/main/b/build-essential/build-essential_12.10.tar.xz' build-essential_12.10.tar.xz 51760 SHA256:a367724c8788696a7cc6f8f09b341949c49fcd06684c3f0e3a1113bbaf75194a
```

### `dpkg` source package: `bzip2=1.0.8-5.1`

Binary Packages:

- `bzip2=1.0.8-5.1`
- `libbz2-1.0:amd64=1.0.8-5.1`
- `libbz2-dev:amd64=1.0.8-5.1`

Licenses: (parsed from: `/usr/share/doc/bzip2/copyright`, `/usr/share/doc/libbz2-1.0/copyright`, `/usr/share/doc/libbz2-dev/copyright`)

- `BSD-variant`
- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris bzip2=1.0.8-5.1
'http://http.debian.net/debian/pool/main/b/bzip2/bzip2_1.0.8-5.1.dsc' bzip2_1.0.8-5.1.dsc 2189 SHA256:210e367658236ea084627394015d466554f1ed2353a5feee5756335dc56074e6
'http://http.debian.net/debian/pool/main/b/bzip2/bzip2_1.0.8.orig.tar.gz' bzip2_1.0.8.orig.tar.gz 810029 SHA256:ab5a03176ee106d3f0fa90e381da478ddae405918153cca248e682cd0c4a2269
'http://http.debian.net/debian/pool/main/b/bzip2/bzip2_1.0.8-5.1.debian.tar.bz2' bzip2_1.0.8-5.1.debian.tar.bz2 26823 SHA256:8d07df2356a8105cc1ad4a64eba54c89aeb732fdc285e845cea1f6f66dda432d
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

### `dpkg` source package: `cairo=1.18.0-3`

Binary Packages:

- `libcairo2:amd64=1.18.0-3+b1`

Licenses: (parsed from: `/usr/share/doc/libcairo2/copyright`)

- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris cairo=1.18.0-3
'http://http.debian.net/debian/pool/main/c/cairo/cairo_1.18.0-3.dsc' cairo_1.18.0-3.dsc 2756 SHA256:3f94d6aeeb32e21aab2f672e0892c590c46d46d4908ceb5f93ef4cbdfbdcaad0
'http://http.debian.net/debian/pool/main/c/cairo/cairo_1.18.0.orig.tar.xz' cairo_1.18.0.orig.tar.xz 33761148 SHA256:243a0736b978a33dee29f9cca7521733b78a65b5418206fef7bd1c3d4cf10b64
'http://http.debian.net/debian/pool/main/c/cairo/cairo_1.18.0-3.debian.tar.xz' cairo_1.18.0-3.debian.tar.xz 29796 SHA256:af6c4100ac6a729d039319ef7f83f7998a92946e019da5ed4e5bde2c27429a78
```

### `dpkg` source package: `cdebconf=0.272`

Binary Packages:

- `libdebconfclient0:amd64=0.272`

Licenses: (parsed from: `/usr/share/doc/libdebconfclient0/copyright`)

- `BSD-2-Clause`
- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris cdebconf=0.272
'http://http.debian.net/debian/pool/main/c/cdebconf/cdebconf_0.272.dsc' cdebconf_0.272.dsc 2707 SHA256:6b7c44f5d9881eb26c5f1d18d01015702b6fee1ce3751f8c5512d9371637eee7
'http://http.debian.net/debian/pool/main/c/cdebconf/cdebconf_0.272.tar.xz' cdebconf_0.272.tar.xz 284488 SHA256:822883bc337bb06be4a9e6dba2fedf8d9ec3596cef8456be76eed6382ac773f9
```

### `dpkg` source package: `cluster=2.1.6-1`

Binary Packages:

- `r-cran-cluster=2.1.6-1`

Licenses: (parsed from: `/usr/share/doc/r-cran-cluster/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris cluster=2.1.6-1
'http://http.debian.net/debian/pool/main/c/cluster/cluster_2.1.6-1.dsc' cluster_2.1.6-1.dsc 1831 SHA256:2a30de784a94d98b08ce82e1c6da81c851c83587ec87012b3df0f5d2ea759598
'http://http.debian.net/debian/pool/main/c/cluster/cluster_2.1.6.orig.tar.gz' cluster_2.1.6.orig.tar.gz 369050 SHA256:d1c50efafd35a55387cc5b36086b97d5591e0b33c48dc718005d2f5907113164
'http://http.debian.net/debian/pool/main/c/cluster/cluster_2.1.6-1.debian.tar.xz' cluster_2.1.6-1.debian.tar.xz 4356 SHA256:7c0fc2b7d445438fc5d92c8289369c8611024c07aa62f1203d16927842d4fb4d
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

### `dpkg` source package: `coreutils=9.4-3.1`

Binary Packages:

- `coreutils=9.4-3.1`

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
$ apt-get source -qq --print-uris coreutils=9.4-3.1
'http://http.debian.net/debian/pool/main/c/coreutils/coreutils_9.4-3.1.dsc' coreutils_9.4-3.1.dsc 1868 SHA256:f18173c5b03135ec14e901748317ef5d05273dfbdebd76938988e2404f185aa1
'http://http.debian.net/debian/pool/main/c/coreutils/coreutils_9.4.orig.tar.xz' coreutils_9.4.orig.tar.xz 5979200 SHA256:ea613a4cf44612326e917201bbbcdfbd301de21ffc3b59b6e5c07e040b275e52
'http://http.debian.net/debian/pool/main/c/coreutils/coreutils_9.4-3.1.debian.tar.xz' coreutils_9.4-3.1.debian.tar.xz 29604 SHA256:326454b01befcd4116543c624f5515387f57f9655284330d1abb7c593abc001f
```

### `dpkg` source package: `curl=8.9.1-2`

Binary Packages:

- `libcurl4t64:amd64=8.9.1-2`

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
$ apt-get source -qq --print-uris curl=8.9.1-2
'http://http.debian.net/debian/pool/main/c/curl/curl_8.9.1-2.dsc' curl_8.9.1-2.dsc 3279 SHA256:955e5786e00c488eff1df859a22bd451ae8cf3cd7b0b457985aed0e4db4ed157
'http://http.debian.net/debian/pool/main/c/curl/curl_8.9.1.orig.tar.gz' curl_8.9.1.orig.tar.gz 4200000 SHA256:291124a007ee5111997825940b3876b3048f7d31e73e9caa681b80fe48b2dcd5
'http://http.debian.net/debian/pool/main/c/curl/curl_8.9.1.orig.tar.gz.asc' curl_8.9.1.orig.tar.gz.asc 488 SHA256:0bff807d70e37880e89c539439d86e1004a7f8a011b06c713de9bd64afb550e5
'http://http.debian.net/debian/pool/main/c/curl/curl_8.9.1-2.debian.tar.xz' curl_8.9.1-2.debian.tar.xz 51912 SHA256:5271b8306f3cdca09d3f57f2aac9b6e06db818dde977a97b51a5f5619fa1a064
```

### `dpkg` source package: `cyrus-sasl2=2.1.28+dfsg1-7`

Binary Packages:

- `libsasl2-2:amd64=2.1.28+dfsg1-7`
- `libsasl2-modules-db:amd64=2.1.28+dfsg1-7`

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
$ apt-get source -qq --print-uris cyrus-sasl2=2.1.28+dfsg1-7
'http://http.debian.net/debian/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.28%2bdfsg1-7.dsc' cyrus-sasl2_2.1.28+dfsg1-7.dsc 3223 SHA256:892d527c81c9332b8392e86e35feee992ba1f7f1148ea21ecc7abfa1b2e5f84f
'http://http.debian.net/debian/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.28%2bdfsg1.orig.tar.xz' cyrus-sasl2_2.1.28+dfsg1.orig.tar.xz 794540 SHA256:e796a5d85d1a85e1b433d43504e467f9075c7ebc0b45730a3996cf11b1deada4
'http://http.debian.net/debian/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.28%2bdfsg1-7.debian.tar.xz' cyrus-sasl2_2.1.28+dfsg1-7.debian.tar.xz 98928 SHA256:f0f78918499794014036065f015f6d5f7d314c13015e4116a86182fa4993fad5
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

### `dpkg` source package: `db5.3=5.3.28+dfsg2-7`

Binary Packages:

- `libdb5.3t64:amd64=5.3.28+dfsg2-7`

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
$ apt-get source -qq --print-uris db5.3=5.3.28+dfsg2-7
'http://http.debian.net/debian/pool/main/d/db5.3/db5.3_5.3.28%2bdfsg2-7.dsc' db5.3_5.3.28+dfsg2-7.dsc 2374 SHA256:f7313fb306b5bf7ad6a428bffb581e649318859df139e35dd47c3d1f733803b2
'http://http.debian.net/debian/pool/main/d/db5.3/db5.3_5.3.28%2bdfsg2.orig.tar.xz' db5.3_5.3.28+dfsg2.orig.tar.xz 21287688 SHA256:ad41b507415dec8316e828b2230242af2251d2c86eefa3c7aa9ef47c5239ef33
'http://http.debian.net/debian/pool/main/d/db5.3/db5.3_5.3.28%2bdfsg2-7.debian.tar.xz' db5.3_5.3.28+dfsg2-7.debian.tar.xz 35232 SHA256:9cee8969e1f440ec8aa2fbacd3a5819907829e0e7e7f1f746dccaa2c93fbf3f2
```

### `dpkg` source package: `debconf=1.5.87`

Binary Packages:

- `debconf=1.5.87`

Licenses: (parsed from: `/usr/share/doc/debconf/copyright`)

- `BSD-2-clause`

Source:

```console
$ apt-get source -qq --print-uris debconf=1.5.87
'http://http.debian.net/debian/pool/main/d/debconf/debconf_1.5.87.dsc' debconf_1.5.87.dsc 2035 SHA256:f46059b530efcb86082ee703225356869727e25babf9c3ad0c4a2e48f87e2977
'http://http.debian.net/debian/pool/main/d/debconf/debconf_1.5.87.tar.xz' debconf_1.5.87.tar.xz 574232 SHA256:2b813be2ab3904a9194a07f2d97ab8e1d79c47ec2ca2f6a1f238c3cb4ff31c66
```

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

### `dpkg` source package: `debianutils=5.20`

Binary Packages:

- `debianutils=5.20`

Licenses: (parsed from: `/usr/share/doc/debianutils/copyright`)

- `GPL-2`
- `GPL-2+`
- `SMAIL-GPL`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris debianutils=5.20
'http://http.debian.net/debian/pool/main/d/debianutils/debianutils_5.20.dsc' debianutils_5.20.dsc 1631 SHA256:ceb4258f9923aef343cc281419140b00e89274eb2e89d12e459bcd8a9abc1ef1
'http://http.debian.net/debian/pool/main/d/debianutils/debianutils_5.20.tar.xz' debianutils_5.20.tar.xz 80776 SHA256:dce8731adee52d1620d562c1d98b8f4177b4ae591b7a17091ffe09700dbd4be8
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

### `dpkg` source package: `e2fsprogs=1.47.1-1`

Binary Packages:

- `e2fsprogs=1.47.1-1`
- `libcom-err2:amd64=1.47.1-1`
- `libext2fs2t64:amd64=1.47.1-1`
- `libss2:amd64=1.47.1-1`
- `logsave=1.47.1-1`

Licenses: (parsed from: `/usr/share/doc/e2fsprogs/copyright`, `/usr/share/doc/libcom-err2/copyright`, `/usr/share/doc/libext2fs2t64/copyright`, `/usr/share/doc/libss2/copyright`, `/usr/share/doc/logsave/copyright`)

- `Apache-2`
- `Apache-2.0`
- `BSD-3-Clause`
- `BSD-3-Clause-Variant`
- `BSD-4-Clause-CMU`
- `Expat`
- `GPL`
- `GPL-2`
- `GPL-2+ with Texinfo exception`
- `ISC`
- `Kazlib`
- `LGPL-2`
- `Latex2e`
- `MIT-US-export`

Source:

```console
$ apt-get source -qq --print-uris e2fsprogs=1.47.1-1
'http://http.debian.net/debian/pool/main/e/e2fsprogs/e2fsprogs_1.47.1-1.dsc' e2fsprogs_1.47.1-1.dsc 2936 SHA256:04ae87a924fa3c9826db58af7e48c48659979c3e71b81a64bcaa48bf6e82507e
'http://http.debian.net/debian/pool/main/e/e2fsprogs/e2fsprogs_1.47.1.orig.tar.gz' e2fsprogs_1.47.1.orig.tar.gz 9952468 SHA256:9afcd201f39429d2db2492aeb13dba5e75d6cc50682b732dca35643bd5f092e3
'http://http.debian.net/debian/pool/main/e/e2fsprogs/e2fsprogs_1.47.1.orig.tar.gz.asc' e2fsprogs_1.47.1.orig.tar.gz.asc 488 SHA256:19b5fed0eb91cd58f0f82252a7d3f72a803dc2f497bfa765034551d9feb06781
'http://http.debian.net/debian/pool/main/e/e2fsprogs/e2fsprogs_1.47.1-1.debian.tar.xz' e2fsprogs_1.47.1-1.debian.tar.xz 89808 SHA256:8d4a4b695ca9012c4e21a727ba9f00bf09c2b7adffd83813e998bfa76ed106b0
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

### `dpkg` source package: `expat=2.6.2-1`

Binary Packages:

- `libexpat1:amd64=2.6.2-1`

Licenses: (parsed from: `/usr/share/doc/libexpat1/copyright`)

- `MIT`

Source:

```console
$ apt-get source -qq --print-uris expat=2.6.2-1
'http://http.debian.net/debian/pool/main/e/expat/expat_2.6.2-1.dsc' expat_2.6.2-1.dsc 1964 SHA256:fbc41fccaa7d701b271bff810b65f49b3c78e1a0180d048bc947955cc4612446
'http://http.debian.net/debian/pool/main/e/expat/expat_2.6.2.orig.tar.gz' expat_2.6.2.orig.tar.gz 8416128 SHA256:fbd032683370d761ba68dba2566d3280a154f5290634172d60a79b24d366d9dc
'http://http.debian.net/debian/pool/main/e/expat/expat_2.6.2-1.debian.tar.xz' expat_2.6.2-1.debian.tar.xz 12920 SHA256:ace5f5235455778222d01a5df08a9dfa3a1a8e015fc11b9c1d18a7d73cfa26fa
```

### `dpkg` source package: `findutils=4.10.0-2`

Binary Packages:

- `findutils=4.10.0-2`

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
$ apt-get source -qq --print-uris findutils=4.10.0-2
'http://deb.debian.org/debian/pool/main/f/findutils/findutils_4.10.0-2.dsc' findutils_4.10.0-2.dsc 2291 SHA256:85ee961402f3b28edc080a130c3106c993e72adffd19fee5dd6e17e033d74891
'http://deb.debian.org/debian/pool/main/f/findutils/findutils_4.10.0.orig.tar.xz' findutils_4.10.0.orig.tar.xz 2240712 SHA256:1387e0b67ff247d2abde998f90dfbf70c1491391a59ddfecb8ae698789f0a4f5
'http://deb.debian.org/debian/pool/main/f/findutils/findutils_4.10.0.orig.tar.xz.asc' findutils_4.10.0.orig.tar.xz.asc 488 SHA256:7f53670eea6bd114e014571221eb652855c1129a3ed99f2a9257c2a313cc216f
'http://deb.debian.org/debian/pool/main/f/findutils/findutils_4.10.0-2.debian.tar.xz' findutils_4.10.0-2.debian.tar.xz 33208 SHA256:7b2a72130847761b6acea3243004103c8a0518762688c7aecde000d3695f543f
```

Other potentially useful URLs:

- https://sources.debian.net/src/findutils/4.10.0-2/ (for browsing the source)
- https://sources.debian.net/src/findutils/4.10.0-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/findutils/4.10.0-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `fontconfig=2.15.0-1.1`

Binary Packages:

- `fontconfig=2.15.0-1.1`
- `fontconfig-config=2.15.0-1.1`
- `libfontconfig1:amd64=2.15.0-1.1`

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

### `dpkg` source package: `freetype=2.13.2+dfsg-1`

Binary Packages:

- `libfreetype6:amd64=2.13.2+dfsg-1+b4`

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
$ apt-get source -qq --print-uris freetype=2.13.2+dfsg-1
'http://http.debian.net/debian/pool/main/f/freetype/freetype_2.13.2%2bdfsg-1.dsc' freetype_2.13.2+dfsg-1.dsc 3686 SHA256:0e00399f7835b49c2606053b6681d2ef43693c6d5d7e6c86c29d1784c5e95e5a
'http://http.debian.net/debian/pool/main/f/freetype/freetype_2.13.2%2bdfsg.orig-ft2demos.tar.xz' freetype_2.13.2+dfsg.orig-ft2demos.tar.xz 341140 SHA256:99ee2ed8b98bcfad17bc57c2d9699d764f20fe29ad304c69b8eb28834ca3b48e
'http://http.debian.net/debian/pool/main/f/freetype/freetype_2.13.2%2bdfsg.orig-ft2demos.tar.xz.asc' freetype_2.13.2+dfsg.orig-ft2demos.tar.xz.asc 833 SHA256:e58ba462f7bdcdc5899f777d33453c1ce6f6e46b080047580f45c9fd9f2dc08c
'http://http.debian.net/debian/pool/main/f/freetype/freetype_2.13.2%2bdfsg.orig-ft2docs.tar.xz' freetype_2.13.2+dfsg.orig-ft2docs.tar.xz 2173920 SHA256:685c25e1035a5076e5097186b3143b9c06878f3f9087d0a81e4d8538d5d15424
'http://http.debian.net/debian/pool/main/f/freetype/freetype_2.13.2%2bdfsg.orig-ft2docs.tar.xz.asc' freetype_2.13.2+dfsg.orig-ft2docs.tar.xz.asc 833 SHA256:d7e17c8a3bce50181530ebe06346f506cbfc92ecc5ca7cc395c7dbb24a71a5c0
'http://http.debian.net/debian/pool/main/f/freetype/freetype_2.13.2%2bdfsg.orig.tar.xz' freetype_2.13.2+dfsg.orig.tar.xz 2220368 SHA256:48c78a4194adfcd15a4d089f3206dab8454c311f5577f3ef7eaef95f777f86e6
'http://http.debian.net/debian/pool/main/f/freetype/freetype_2.13.2%2bdfsg-1.debian.tar.xz' freetype_2.13.2+dfsg-1.debian.tar.xz 43824 SHA256:c1db3a2bf2a754fc3666b06757f4055fa7f964b256aaa520f6b7142b68e3c0bb
```

### `dpkg` source package: `fribidi=1.0.15-1`

Binary Packages:

- `libfribidi0:amd64=1.0.15-1`

Licenses: (parsed from: `/usr/share/doc/libfribidi0/copyright`)

- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris fribidi=1.0.15-1
'http://http.debian.net/debian/pool/main/f/fribidi/fribidi_1.0.15-1.dsc' fribidi_1.0.15-1.dsc 2004 SHA256:fe428965937cf253b71efb5de0b214c8bbb2a024a13d09635938ff9fa0052283
'http://http.debian.net/debian/pool/main/f/fribidi/fribidi_1.0.15.orig.tar.xz' fribidi_1.0.15.orig.tar.xz 1166860 SHA256:0bbc7ff633bfa208ae32d7e369cf5a7d20d5d2557a0b067c9aa98bcbf9967587
'http://http.debian.net/debian/pool/main/f/fribidi/fribidi_1.0.15-1.debian.tar.xz' fribidi_1.0.15-1.debian.tar.xz 8888 SHA256:e0ec140d8bcabaaf5edcfe10e6bb268d8150a76d657bbfe9e3415569d4b67440
```

### `dpkg` source package: `gcc-14=14.2.0-2`

Binary Packages:

- `cpp-14=14.2.0-2`
- `cpp-14-x86-64-linux-gnu=14.2.0-2`
- `g++-14=14.2.0-2`
- `g++-14-x86-64-linux-gnu=14.2.0-2`
- `gcc-14=14.2.0-2`
- `gcc-14-base:amd64=14.2.0-2`
- `gcc-14-x86-64-linux-gnu=14.2.0-2`
- `gfortran-14=14.2.0-2`
- `gfortran-14-x86-64-linux-gnu=14.2.0-2`
- `libasan8:amd64=14.2.0-2`
- `libatomic1:amd64=14.2.0-2`
- `libcc1-0:amd64=14.2.0-2`
- `libgcc-14-dev:amd64=14.2.0-2`
- `libgcc-s1:amd64=14.2.0-2`
- `libgfortran-14-dev:amd64=14.2.0-2`
- `libgfortran5:amd64=14.2.0-2`
- `libgomp1:amd64=14.2.0-2`
- `libhwasan0:amd64=14.2.0-2`
- `libitm1:amd64=14.2.0-2`
- `liblsan0:amd64=14.2.0-2`
- `libquadmath0:amd64=14.2.0-2`
- `libstdc++-14-dev:amd64=14.2.0-2`
- `libstdc++6:amd64=14.2.0-2`
- `libtsan2:amd64=14.2.0-2`
- `libubsan1:amd64=14.2.0-2`

Licenses: (parsed from: `/usr/share/doc/cpp-14/copyright`, `/usr/share/doc/cpp-14-x86-64-linux-gnu/copyright`, `/usr/share/doc/g++-14/copyright`, `/usr/share/doc/g++-14-x86-64-linux-gnu/copyright`, `/usr/share/doc/gcc-14/copyright`, `/usr/share/doc/gcc-14-base/copyright`, `/usr/share/doc/gcc-14-x86-64-linux-gnu/copyright`, `/usr/share/doc/gfortran-14/copyright`, `/usr/share/doc/gfortran-14-x86-64-linux-gnu/copyright`, `/usr/share/doc/libasan8/copyright`, `/usr/share/doc/libatomic1/copyright`, `/usr/share/doc/libcc1-0/copyright`, `/usr/share/doc/libgcc-14-dev/copyright`, `/usr/share/doc/libgcc-s1/copyright`, `/usr/share/doc/libgfortran-14-dev/copyright`, `/usr/share/doc/libgfortran5/copyright`, `/usr/share/doc/libgomp1/copyright`, `/usr/share/doc/libhwasan0/copyright`, `/usr/share/doc/libitm1/copyright`, `/usr/share/doc/liblsan0/copyright`, `/usr/share/doc/libquadmath0/copyright`, `/usr/share/doc/libstdc++-14-dev/copyright`, `/usr/share/doc/libstdc++6/copyright`, `/usr/share/doc/libtsan2/copyright`, `/usr/share/doc/libubsan1/copyright`)

- `Artistic`
- `GFDL-1.2`
- `GPL`
- `GPL-3`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris gcc-14=14.2.0-2
'http://http.debian.net/debian/pool/main/g/gcc-14/gcc-14_14.2.0-2.dsc' gcc-14_14.2.0-2.dsc 46572 SHA256:ec6f4d89f91eef87f5403e394421f366bc4016161fa65ff01972aae727f3825f
'http://http.debian.net/debian/pool/main/g/gcc-14/gcc-14_14.2.0.orig.tar.gz' gcc-14_14.2.0.orig.tar.gz 94299633 SHA256:e162a5ef3f0077ecae598c6556908d2ab80841532df3398072a96a6df6e6aa29
'http://http.debian.net/debian/pool/main/g/gcc-14/gcc-14_14.2.0-2.debian.tar.xz' gcc-14_14.2.0-2.debian.tar.xz 1641968 SHA256:39186bd12fbe63e10ea6d9284392f31bae05700a47813121e3542895dc2e777c
```

### `dpkg` source package: `gcc-defaults=1.219`

Binary Packages:

- `cpp=4:14.1.0-2`
- `cpp-x86-64-linux-gnu=4:14.1.0-2`
- `g++=4:14.1.0-2`
- `g++-x86-64-linux-gnu=4:14.1.0-2`
- `gcc=4:14.1.0-2`
- `gcc-x86-64-linux-gnu=4:14.1.0-2`
- `gfortran=4:14.1.0-2`
- `gfortran-x86-64-linux-gnu=4:14.1.0-2`

Licenses: (parsed from: `/usr/share/doc/cpp/copyright`, `/usr/share/doc/cpp-x86-64-linux-gnu/copyright`, `/usr/share/doc/g++/copyright`, `/usr/share/doc/g++-x86-64-linux-gnu/copyright`, `/usr/share/doc/gcc/copyright`, `/usr/share/doc/gcc-x86-64-linux-gnu/copyright`, `/usr/share/doc/gfortran/copyright`, `/usr/share/doc/gfortran-x86-64-linux-gnu/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris gcc-defaults=1.219
'http://http.debian.net/debian/pool/main/g/gcc-defaults/gcc-defaults_1.219.dsc' gcc-defaults_1.219.dsc 36895 SHA256:4f90df7abb0a10fd943ce1bd03053ddf1c893405cb5cdc86492bca90f932436f
'http://http.debian.net/debian/pool/main/g/gcc-defaults/gcc-defaults_1.219.tar.xz' gcc-defaults_1.219.tar.xz 64700 SHA256:f6e2eee21d8c05bc24f54855cd659b8fd9a8ac012aa23af3d8537f5ca2679cef
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

### `dpkg` source package: `glib2.0=2.81.1-3`

Binary Packages:

- `libglib2.0-0t64:amd64=2.81.1-3`

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
$ apt-get source -qq --print-uris glib2.0=2.81.1-3
'http://http.debian.net/debian/pool/main/g/glib2.0/glib2.0_2.81.1-3.dsc' glib2.0_2.81.1-3.dsc 4532 SHA256:4ddf730e1ff06282109860a82fc3d939f50076be1248001d7ff019fe71d59d09
'http://http.debian.net/debian/pool/main/g/glib2.0/glib2.0_2.81.1.orig-unicode-data.tar.xz' glib2.0_2.81.1.orig-unicode-data.tar.xz 262908 SHA256:9bf66a7e9f2f18cbd7a72f561dc1f997990b53243435008777109c823cd7e1ea
'http://http.debian.net/debian/pool/main/g/glib2.0/glib2.0_2.81.1.orig.tar.xz' glib2.0_2.81.1.orig.tar.xz 5538528 SHA256:629365cde729a7b76b062fc218a109a84bbc4668ca0c92ab590ecccf969f824c
'http://http.debian.net/debian/pool/main/g/glib2.0/glib2.0_2.81.1-3.debian.tar.xz' glib2.0_2.81.1-3.debian.tar.xz 132340 SHA256:0269356b85d341f6d1a02507f083698fee2177b40fe0de6271332cc33b673dc7
```

### `dpkg` source package: `glibc=2.39-6`

Binary Packages:

- `libc-bin=2.39-6`
- `libc-dev-bin=2.39-6`
- `libc-l10n=2.39-6`
- `libc6:amd64=2.39-6`
- `libc6-dev:amd64=2.39-6`
- `locales=2.39-6`

Licenses: (parsed from: `/usr/share/doc/libc-bin/copyright`, `/usr/share/doc/libc-dev-bin/copyright`, `/usr/share/doc/libc-l10n/copyright`, `/usr/share/doc/libc6/copyright`, `/usr/share/doc/libc6-dev/copyright`, `/usr/share/doc/locales/copyright`)

- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris glibc=2.39-6
'http://http.debian.net/debian/pool/main/g/glibc/glibc_2.39-6.dsc' glibc_2.39-6.dsc 7550 SHA256:cc87529a64264bd02661b058e5e49808df329a18daa80311e87b95bc622f1a74
'http://http.debian.net/debian/pool/main/g/glibc/glibc_2.39.orig.tar.xz' glibc_2.39.orig.tar.xz 19076836 SHA256:207e5c93a158e5b45a2b42530660fe7717d4b45e00f96e58496389c2ef868157
'http://http.debian.net/debian/pool/main/g/glibc/glibc_2.39-6.debian.tar.xz' glibc_2.39-6.debian.tar.xz 452016 SHA256:4bf30eea4909beb71db0bccd8d1add18922934c16f02bea5586bfc77a582a9f2
```

### `dpkg` source package: `gmp=2:6.3.0+dfsg-2`

Binary Packages:

- `libgmp10:amd64=2:6.3.0+dfsg-2+b1`

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
$ apt-get source -qq --print-uris gmp=2:6.3.0+dfsg-2
'http://http.debian.net/debian/pool/main/g/gmp/gmp_6.3.0%2bdfsg-2.dsc' gmp_6.3.0+dfsg-2.dsc 2251 SHA256:31bf88a2899f7a6eb2dc0db438ba2b27f87562dfe73815a3bbc8b65675ba1a51
'http://http.debian.net/debian/pool/main/g/gmp/gmp_6.3.0%2bdfsg.orig.tar.xz' gmp_6.3.0+dfsg.orig.tar.xz 1870556 SHA256:bd2966e6d277f79328e894a5a9f3ba3fbf2ed2be81def5f48623e30c23fb1572
'http://http.debian.net/debian/pool/main/g/gmp/gmp_6.3.0%2bdfsg-2.debian.tar.xz' gmp_6.3.0+dfsg-2.debian.tar.xz 19156 SHA256:07fbc1f67c1c076575f8196f3b5a2d2be0268be10940ca59293d7f1669365f4e
```

### `dpkg` source package: `gnupg2=2.2.43-8`

Binary Packages:

- `gpgv=2.2.43-8`

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
$ apt-get source -qq --print-uris gnupg2=2.2.43-8
'http://http.debian.net/debian/pool/main/g/gnupg2/gnupg2_2.2.43-8.dsc' gnupg2_2.2.43-8.dsc 3834 SHA256:8cd7674efe59b305abe9faf50895582c2276f066dadb8a6ce9586311c0d8a365
'http://http.debian.net/debian/pool/main/g/gnupg2/gnupg2_2.2.43.orig.tar.bz2' gnupg2_2.2.43.orig.tar.bz2 7435426 SHA256:a3b34c40f455d93054d33cf4cf2a8ce41149d499eca2fbb759619de04822d453
'http://http.debian.net/debian/pool/main/g/gnupg2/gnupg2_2.2.43.orig.tar.bz2.asc' gnupg2_2.2.43.orig.tar.bz2.asc 228 SHA256:adb6964121fde1299f0db31fe7380812f4b6bb66f4eaabdc4ab5c79480e6b701
'http://http.debian.net/debian/pool/main/g/gnupg2/gnupg2_2.2.43-8.debian.tar.xz' gnupg2_2.2.43-8.debian.tar.xz 139592 SHA256:a99aef15523464a944797f89c01da967fc4860ec9c0897686844e2552583a8fe
```

### `dpkg` source package: `gnutls28=3.8.6-2`

Binary Packages:

- `libgnutls30t64:amd64=3.8.6-2`

Licenses: (parsed from: `/usr/share/doc/libgnutls30t64/copyright`)

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
$ apt-get source -qq --print-uris gnutls28=3.8.6-2
'http://http.debian.net/debian/pool/main/g/gnutls28/gnutls28_3.8.6-2.dsc' gnutls28_3.8.6-2.dsc 3269 SHA256:4ec462fc0173a7e33a7051586ea4486b4856cbd97e38e9a96f88f033cf0862f8
'http://http.debian.net/debian/pool/main/g/gnutls28/gnutls28_3.8.6.orig.tar.xz' gnutls28_3.8.6.orig.tar.xz 6517476 SHA256:2e1588aae53cb32d43937f1f4eca28febd9c0c7aa1734fc5dd61a7e81e0ebcdd
'http://http.debian.net/debian/pool/main/g/gnutls28/gnutls28_3.8.6.orig.tar.xz.asc' gnutls28_3.8.6.orig.tar.xz.asc 228 SHA256:53ad69e21ea74447117aa55e51853c49e745f2c1e2de97539c6fbbec306cf65e
'http://http.debian.net/debian/pool/main/g/gnutls28/gnutls28_3.8.6-2.debian.tar.xz' gnutls28_3.8.6-2.debian.tar.xz 77512 SHA256:7a71826206b082d6742fafcb6dee37aa9ae147b9bad8a69875f5eed8ea7a915b
```

### `dpkg` source package: `graphite2=1.3.14-2`

Binary Packages:

- `libgraphite2-3:amd64=1.3.14-2`

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

### `dpkg` source package: `gzip=1.12-1.1`

Binary Packages:

- `gzip=1.12-1.1`

Licenses: (parsed from: `/usr/share/doc/gzip/copyright`)

- `FSF-manpages`
- `GFDL-1.3+-no-invariant`
- `GFDL-3`
- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris gzip=1.12-1.1
'http://http.debian.net/debian/pool/main/g/gzip/gzip_1.12-1.1.dsc' gzip_1.12-1.1.dsc 2167 SHA256:212bff0edd2ccbbf816d7168f46f81d714b57043c249411e2e2d0fd71c3d3e40
'http://http.debian.net/debian/pool/main/g/gzip/gzip_1.12.orig.tar.xz' gzip_1.12.orig.tar.xz 825548 SHA256:ce5e03e519f637e1f814011ace35c4f87b33c0bbabeec35baf5fbd3479e91956
'http://http.debian.net/debian/pool/main/g/gzip/gzip_1.12.orig.tar.xz.asc' gzip_1.12.orig.tar.xz.asc 833 SHA256:3ed9ab54452576e0be0d477c772c9f47baa36415133fef7dd1fcf7b15480ba32
'http://http.debian.net/debian/pool/main/g/gzip/gzip_1.12-1.1.debian.tar.xz' gzip_1.12-1.1.debian.tar.xz 19244 SHA256:d48d5314c0255114f43964f78b87262299bbac840e5f511a078e2d2590937ad6
```

### `dpkg` source package: `harfbuzz=8.3.0-2`

Binary Packages:

- `libharfbuzz0b:amd64=8.3.0-2+b1`

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
$ apt-get source -qq --print-uris harfbuzz=8.3.0-2
'http://http.debian.net/debian/pool/main/h/harfbuzz/harfbuzz_8.3.0-2.dsc' harfbuzz_8.3.0-2.dsc 2892 SHA256:e4464683b4936fd977ee5b62c9a6786a9be4966d111dea6b9278922819816895
'http://http.debian.net/debian/pool/main/h/harfbuzz/harfbuzz_8.3.0.orig.tar.xz' harfbuzz_8.3.0.orig.tar.xz 19002808 SHA256:109501eaeb8bde3eadb25fab4164e993fbace29c3d775bcaa1c1e58e2f15f847
'http://http.debian.net/debian/pool/main/h/harfbuzz/harfbuzz_8.3.0-2.debian.tar.xz' harfbuzz_8.3.0-2.debian.tar.xz 19796 SHA256:36267a5c7d65ce26dee24491aa8d95af6afe860c9dc4f908d7d3a1d290f9a896
```

### `dpkg` source package: `hostname=3.23+nmu2`

Binary Packages:

- `hostname=3.23+nmu2`

Licenses: (parsed from: `/usr/share/doc/hostname/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris hostname=3.23+nmu2
'http://http.debian.net/debian/pool/main/h/hostname/hostname_3.23%2bnmu2.dsc' hostname_3.23+nmu2.dsc 1431 SHA256:03fe3dcdda4e3abc3a5d8d7ed6eb63558d9fa0dfe68412667eac73945b47e506
'http://http.debian.net/debian/pool/main/h/hostname/hostname_3.23%2bnmu2.tar.xz' hostname_3.23+nmu2.tar.xz 12944 SHA256:e94bc2323862e1b49635c2b638aa905f14aa91d9eb525be8e8811a773ca3a60d
```

### `dpkg` source package: `icu=72.1-5`

Binary Packages:

- `icu-devtools=72.1-5`
- `libicu-dev:amd64=72.1-5`
- `libicu72:amd64=72.1-5`

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

### `dpkg` source package: `init-system-helpers=1.66`

Binary Packages:

- `init-system-helpers=1.66`

Licenses: (parsed from: `/usr/share/doc/init-system-helpers/copyright`)

- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris init-system-helpers=1.66
'http://http.debian.net/debian/pool/main/i/init-system-helpers/init-system-helpers_1.66.dsc' init-system-helpers_1.66.dsc 2234 SHA256:a1e2276879abfe63174797c94969bc8591b8a05f2bad6ae3f27379b472877d6d
'http://http.debian.net/debian/pool/main/i/init-system-helpers/init-system-helpers_1.66.tar.xz' init-system-helpers_1.66.tar.xz 44976 SHA256:da058b5623a7d3f39aee1761b173478fdbbdfdf743fd66e876e56039c708ce53
```

### `dpkg` source package: `isl=0.26-3`

Binary Packages:

- `libisl23:amd64=0.26-3+b2`

Licenses: (parsed from: `/usr/share/doc/libisl23/copyright`)

- `BSD-2-clause`
- `LGPL-2`
- `LGPL-2.1+`
- `MIT`

Source:

```console
$ apt-get source -qq --print-uris isl=0.26-3
'http://http.debian.net/debian/pool/main/i/isl/isl_0.26-3.dsc' isl_0.26-3.dsc 1832 SHA256:b943ed41e0d04bd86ea1a9a10e49a0ac1996ac534b67b968df4320880ec6e6e7
'http://http.debian.net/debian/pool/main/i/isl/isl_0.26.orig.tar.xz' isl_0.26.orig.tar.xz 2035560 SHA256:a0b5cb06d24f9fa9e77b55fabbe9a3c94a336190345c2555f9915bb38e976504
'http://http.debian.net/debian/pool/main/i/isl/isl_0.26-3.debian.tar.xz' isl_0.26-3.debian.tar.xz 24700 SHA256:c4a9367d892a12da46c54cbf6475f447e137ac3eff857baa91af94c99daed0a5
```

### `dpkg` source package: `jansson=2.14-2`

Binary Packages:

- `libjansson4:amd64=2.14-2+b2`

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

- `libjbig0:amd64=2.1-6.1+b1`

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

### `dpkg` source package: `keyutils=1.6.3-3`

Binary Packages:

- `libkeyutils1:amd64=1.6.3-3`

Licenses: (parsed from: `/usr/share/doc/libkeyutils1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2`
- `LGPL-2+`

Source:

```console
$ apt-get source -qq --print-uris keyutils=1.6.3-3
'http://http.debian.net/debian/pool/main/k/keyutils/keyutils_1.6.3-3.dsc' keyutils_1.6.3-3.dsc 2079 SHA256:0a4178e10982c7351da7db5b44b5c18807613ad066cb2e157d0756019764f0c1
'http://http.debian.net/debian/pool/main/k/keyutils/keyutils_1.6.3.orig.tar.gz' keyutils_1.6.3.orig.tar.gz 137022 SHA256:a61d5706136ae4c05bd48f86186bcfdbd88dd8bd5107e3e195c924cfc1b39bb4
'http://http.debian.net/debian/pool/main/k/keyutils/keyutils_1.6.3-3.debian.tar.xz' keyutils_1.6.3-3.debian.tar.xz 13328 SHA256:8c078d9de91f930df174eebc60e063e8fff574ac36c0f7ee18f7e21635d60af0
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

### `dpkg` source package: `lapack=3.12.0-3`

Binary Packages:

- `libblas-dev:amd64=3.12.0-3`
- `libblas3:amd64=3.12.0-3`
- `liblapack-dev:amd64=3.12.0-3`
- `liblapack3:amd64=3.12.0-3`

Licenses: (parsed from: `/usr/share/doc/libblas-dev/copyright`, `/usr/share/doc/libblas3/copyright`, `/usr/share/doc/liblapack-dev/copyright`, `/usr/share/doc/liblapack3/copyright`)

- `BSD-3-clause`
- `BSD-3-clause-intel`

Source:

```console
$ apt-get source -qq --print-uris lapack=3.12.0-3
'http://http.debian.net/debian/pool/main/l/lapack/lapack_3.12.0-3.dsc' lapack_3.12.0-3.dsc 3307 SHA256:e00e9d07a748ee1e48e6c3d879459de13d172bd267b45894b7893d2b15d8ea34
'http://http.debian.net/debian/pool/main/l/lapack/lapack_3.12.0.orig.tar.gz' lapack_3.12.0.orig.tar.gz 7933607 SHA256:eac9570f8e0ad6f30ce4b963f4f033f0f643e7c3912fc9ee6cd99120675ad48b
'http://http.debian.net/debian/pool/main/l/lapack/lapack_3.12.0-3.debian.tar.xz' lapack_3.12.0-3.debian.tar.xz 28756 SHA256:ff6dacfcd3d8502b2fe53ae8296a00f322055cdfbdb5b2edc1b292d522dc936e
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

### `dpkg` source package: `lerc=4.0.0+ds-4`

Binary Packages:

- `liblerc4:amd64=4.0.0+ds-4+b1`

Licenses: (parsed from: `/usr/share/doc/liblerc4/copyright`)

- `Apache-2.0`

Source:

```console
$ apt-get source -qq --print-uris lerc=4.0.0+ds-4
'http://http.debian.net/debian/pool/main/l/lerc/lerc_4.0.0%2bds-4.dsc' lerc_4.0.0+ds-4.dsc 2638 SHA256:1f5758010599f9fd8b52ecea0541addeb0ea968f37d383a747abaa2a956f717e
'http://http.debian.net/debian/pool/main/l/lerc/lerc_4.0.0%2bds.orig.tar.xz' lerc_4.0.0+ds.orig.tar.xz 348140 SHA256:acf855502fd3b950ee78f0b67bc9e9b39316b3526fbf6d8b8b1a9482fb756723
'http://http.debian.net/debian/pool/main/l/lerc/lerc_4.0.0%2bds-4.debian.tar.xz' lerc_4.0.0+ds-4.debian.tar.xz 8280 SHA256:513db93f198180d601bba09356bd447c57d3a6360119e289cba897bf9054e5ac
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

### `dpkg` source package: `libbsd=0.12.2-1`

Binary Packages:

- `libbsd0:amd64=0.12.2-1`

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
$ apt-get source -qq --print-uris libbsd=0.12.2-1
'http://http.debian.net/debian/pool/main/libb/libbsd/libbsd_0.12.2-1.dsc' libbsd_0.12.2-1.dsc 2347 SHA256:18bfe06bd7f6d5e3f77f7827bcf129014918952cdcd6102288afdae8120dc6c9
'http://http.debian.net/debian/pool/main/libb/libbsd/libbsd_0.12.2.orig.tar.xz' libbsd_0.12.2.orig.tar.xz 446032 SHA256:b88cc9163d0c652aaf39a99991d974ddba1c3a9711db8f1b5838af2a14731014
'http://http.debian.net/debian/pool/main/libb/libbsd/libbsd_0.12.2.orig.tar.xz.asc' libbsd_0.12.2.orig.tar.xz.asc 833 SHA256:620dc92f158ebe0a650c0e92214a8121b927276895dc9a1dcaa38f627fa0fcb0
'http://http.debian.net/debian/pool/main/libb/libbsd/libbsd_0.12.2-1.debian.tar.xz' libbsd_0.12.2-1.debian.tar.xz 18612 SHA256:618f0d116e18729cb7d5b93095e112c429aad294993b4def2c0498761d4646e9
```

### `dpkg` source package: `libcap-ng=0.8.5-1`

Binary Packages:

- `libcap-ng0:amd64=0.8.5-1+b1`

Licenses: (parsed from: `/usr/share/doc/libcap-ng0/copyright`)

- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris libcap-ng=0.8.5-1
'http://http.debian.net/debian/pool/main/libc/libcap-ng/libcap-ng_0.8.5-1.dsc' libcap-ng_0.8.5-1.dsc 1638 SHA256:0b4a6e7ff74f5d888295bfab7f65f37255fb150e07bd8cedc0678c198b47bba0
'http://http.debian.net/debian/pool/main/libc/libcap-ng/libcap-ng_0.8.5.orig.tar.gz' libcap-ng_0.8.5.orig.tar.gz 59265 SHA256:e4be07fdd234f10b866433f224d183626003c65634ed0552b02e654a380244c2
'http://http.debian.net/debian/pool/main/libc/libcap-ng/libcap-ng_0.8.5-1.debian.tar.xz' libcap-ng_0.8.5-1.debian.tar.xz 7400 SHA256:17156cf9ef58de3e8c34a357c6afa47d54a42d2c185ffbd43fde7c4cf04937f1
```

### `dpkg` source package: `libcap2=1:2.66-5`

Binary Packages:

- `libcap2:amd64=1:2.66-5`

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

- `libdatrie1:amd64=0.2.13-3`

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

### `dpkg` source package: `libdeflate=1.20-1`

Binary Packages:

- `libdeflate-dev:amd64=1.20-1`
- `libdeflate0:amd64=1.20-1`

Licenses: (parsed from: `/usr/share/doc/libdeflate-dev/copyright`, `/usr/share/doc/libdeflate0/copyright`)

- `Expat`

Source:

```console
$ apt-get source -qq --print-uris libdeflate=1.20-1
'http://deb.debian.org/debian/pool/main/libd/libdeflate/libdeflate_1.20-1.dsc' libdeflate_1.20-1.dsc 2207 SHA256:5038f48807c424612469c143aa789ba11b6afb71138913e87e2190e4395acb87
'http://deb.debian.org/debian/pool/main/libd/libdeflate/libdeflate_1.20.orig.tar.gz' libdeflate_1.20.orig.tar.gz 194212 SHA256:ed1454166ced78913ff3809870a4005b7170a6fd30767dc478a09b96847b9c2a
'http://deb.debian.org/debian/pool/main/libd/libdeflate/libdeflate_1.20-1.debian.tar.xz' libdeflate_1.20-1.debian.tar.xz 5316 SHA256:64eb481ac31d52f88d953fd9b8d133697ffe027aa945dbc544d7b12233491807
```

Other potentially useful URLs:

- https://sources.debian.net/src/libdeflate/1.20-1/ (for browsing the source)
- https://sources.debian.net/src/libdeflate/1.20-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libdeflate/1.20-1/ (for access to the source package after it no longer exists in the archive)

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

### `dpkg` source package: `libgcrypt20=1.11.0-2`

Binary Packages:

- `libgcrypt20:amd64=1.11.0-2`

Licenses: (parsed from: `/usr/share/doc/libgcrypt20/copyright`)

- `GPL-2`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris libgcrypt20=1.11.0-2
'http://deb.debian.org/debian/pool/main/libg/libgcrypt20/libgcrypt20_1.11.0-2.dsc' libgcrypt20_1.11.0-2.dsc 2819 SHA256:35ea254a40e96af7958d73e645d256233012e195dd3169dfe0a004d6432c7f24
'http://deb.debian.org/debian/pool/main/libg/libgcrypt20/libgcrypt20_1.11.0.orig.tar.bz2' libgcrypt20_1.11.0.orig.tar.bz2 4180345 SHA256:09120c9867ce7f2081d6aaa1775386b98c2f2f246135761aae47d81f58685b9c
'http://deb.debian.org/debian/pool/main/libg/libgcrypt20/libgcrypt20_1.11.0.orig.tar.bz2.asc' libgcrypt20_1.11.0.orig.tar.bz2.asc 228 SHA256:9fedf4f7bb80d5178d4e26ec2f03ba5fc44eddfc72c2e9966d7d619aeee3df2c
'http://deb.debian.org/debian/pool/main/libg/libgcrypt20/libgcrypt20_1.11.0-2.debian.tar.xz' libgcrypt20_1.11.0-2.debian.tar.xz 37376 SHA256:1b80362366cc39096720dbeee909cc298f621c7691ea3c7011ac52ff395c73d0
```

Other potentially useful URLs:

- https://sources.debian.net/src/libgcrypt20/1.11.0-2/ (for browsing the source)
- https://sources.debian.net/src/libgcrypt20/1.11.0-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libgcrypt20/1.11.0-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libgpg-error=1.49-2`

Binary Packages:

- `libgpg-error0:amd64=1.49-2`

Licenses: (parsed from: `/usr/share/doc/libgpg-error0/copyright`)

- `BSD-3-clause`
- `GPL-3`
- `GPL-3+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `g10-permissive`

Source:

```console
$ apt-get source -qq --print-uris libgpg-error=1.49-2
'http://deb.debian.org/debian/pool/main/libg/libgpg-error/libgpg-error_1.49-2.dsc' libgpg-error_1.49-2.dsc 2896 SHA256:8638b6639998a745cb377f8011609d5ed0b211f72cd01e63573a058d71e29cea
'http://deb.debian.org/debian/pool/main/libg/libgpg-error/libgpg-error_1.49.orig.tar.bz2' libgpg-error_1.49.orig.tar.bz2 1081175 SHA256:8b79d54639dbf4abc08b5406fb2f37e669a2dec091dd024fb87dd367131c63a9
'http://deb.debian.org/debian/pool/main/libg/libgpg-error/libgpg-error_1.49.orig.tar.bz2.asc' libgpg-error_1.49.orig.tar.bz2.asc 228 SHA256:2b781c0b6cd865c28ec1006cf9fb4390303b2d52ffc7ed09bcb58a01348ef870
'http://deb.debian.org/debian/pool/main/libg/libgpg-error/libgpg-error_1.49-2.debian.tar.xz' libgpg-error_1.49-2.debian.tar.xz 18804 SHA256:c60d7a21430651e8f36474bdb585096dd4fd52dc403fb99dfa2a874068211282
```

Other potentially useful URLs:

- https://sources.debian.net/src/libgpg-error/1.49-2/ (for browsing the source)
- https://sources.debian.net/src/libgpg-error/1.49-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libgpg-error/1.49-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libice=2:1.0.10-1`

Binary Packages:

- `libice6:amd64=2:1.0.10-1+b1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libice=2:1.0.10-1
'http://http.debian.net/debian/pool/main/libi/libice/libice_1.0.10-1.dsc' libice_1.0.10-1.dsc 2049 SHA256:adb7b4e250db838a476a44b5a941c8f935ac2b20858186f09228cd3e0696034d
'http://http.debian.net/debian/pool/main/libi/libice/libice_1.0.10.orig.tar.gz' libice_1.0.10.orig.tar.gz 481960 SHA256:1116bc64c772fd127a0d0c0ffa2833479905e3d3d8197740b3abd5f292f22d2d
'http://http.debian.net/debian/pool/main/libi/libice/libice_1.0.10-1.diff.gz' libice_1.0.10-1.diff.gz 11349 SHA256:d186b3877416a7e80f1923fe2fc736d576e585a41450bcf4cd5e74f9dd099362
```

### `dpkg` source package: `libidn2=2.3.7-2`

Binary Packages:

- `libidn2-0:amd64=2.3.7-2`

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

- `libjpeg-dev:amd64=1:2.1.5-3`
- `libjpeg62-turbo:amd64=1:2.1.5-3`
- `libjpeg62-turbo-dev:amd64=1:2.1.5-3`

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

- `libmd0:amd64=1.1.0-2`

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

### `dpkg` source package: `libpaper=1.1.29`

Binary Packages:

- `libpaper-utils=1.1.29+b1`
- `libpaper1:amd64=1.1.29+b1`

Licenses: (parsed from: `/usr/share/doc/libpaper-utils/copyright`, `/usr/share/doc/libpaper1/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris libpaper=1.1.29
'http://http.debian.net/debian/pool/main/libp/libpaper/libpaper_1.1.29.dsc' libpaper_1.1.29.dsc 1604 SHA256:940adde11d3bd19c3be7e3e16cdd737ca8fa52fac31e002d2530beea3e64cfc9
'http://http.debian.net/debian/pool/main/libp/libpaper/libpaper_1.1.29.tar.gz' libpaper_1.1.29.tar.gz 44942 SHA256:26330e21e9a3124658d515fd850b0cde546ff42d89b2596a5264c5f1677f0547
```

### `dpkg` source package: `libpng1.6=1.6.43-5`

Binary Packages:

- `libpng-dev:amd64=1.6.43-5`
- `libpng16-16t64:amd64=1.6.43-5`

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
$ apt-get source -qq --print-uris libpng1.6=1.6.43-5
'http://http.debian.net/debian/pool/main/libp/libpng1.6/libpng1.6_1.6.43-5.dsc' libpng1.6_1.6.43-5.dsc 2269 SHA256:ef8d2c8a58893d500db27f88d95edda16c2832ab0ffbef23c7f7177b2e967222
'http://http.debian.net/debian/pool/main/libp/libpng1.6/libpng1.6_1.6.43.orig.tar.gz' libpng1.6_1.6.43.orig.tar.gz 1554715 SHA256:fecc95b46cf05e8e3fc8a414750e0ba5aad00d89e9fdf175e94ff041caf1a03a
'http://http.debian.net/debian/pool/main/libp/libpng1.6/libpng1.6_1.6.43-5.debian.tar.xz' libpng1.6_1.6.43-5.debian.tar.xz 31476 SHA256:449bf2a0008548dd2c37e9a3b511596bf2650568562a9c1b932be8bb3f256d00
```

### `dpkg` source package: `libpsl=0.21.2-1.1`

Binary Packages:

- `libpsl5t64:amd64=0.21.2-1.1`

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

### `dpkg` source package: `libseccomp=2.5.5-1`

Binary Packages:

- `libseccomp2:amd64=2.5.5-1+b1`

Licenses: (parsed from: `/usr/share/doc/libseccomp2/copyright`)

- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libseccomp=2.5.5-1
'http://http.debian.net/debian/pool/main/libs/libseccomp/libseccomp_2.5.5-1.dsc' libseccomp_2.5.5-1.dsc 2708 SHA256:d8ea2fb22a4ed90001a34ace6e6a6f41fd1d9404de923182f2dde6037fec22e5
'http://http.debian.net/debian/pool/main/libs/libseccomp/libseccomp_2.5.5.orig.tar.gz' libseccomp_2.5.5.orig.tar.gz 642445 SHA256:248a2c8a4d9b9858aa6baf52712c34afefcf9c9e94b76dce02c1c9aa25fb3375
'http://http.debian.net/debian/pool/main/libs/libseccomp/libseccomp_2.5.5.orig.tar.gz.asc' libseccomp_2.5.5.orig.tar.gz.asc 833 SHA256:f3bf8a946020d3047581f11fe6ac71971a842115ddb362562b193861ef57d97b
'http://http.debian.net/debian/pool/main/libs/libseccomp/libseccomp_2.5.5-1.debian.tar.xz' libseccomp_2.5.5-1.debian.tar.xz 17608 SHA256:0e14e878a97657d8ff660f32477461abbd3ce366e5c24df4e4385c3e64cacaac
```

### `dpkg` source package: `libselinux=3.5-2`

Binary Packages:

- `libselinux1:amd64=3.5-2+b3`

Licenses: (parsed from: `/usr/share/doc/libselinux1/copyright`)

- `GPL-2`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris libselinux=3.5-2
'http://http.debian.net/debian/pool/main/libs/libselinux/libselinux_3.5-2.dsc' libselinux_3.5-2.dsc 2662 SHA256:cd6baa8aebf37a88355291bf5cb11a311463479fed8a9f479043d1fc12de25cc
'http://http.debian.net/debian/pool/main/libs/libselinux/libselinux_3.5.orig.tar.gz' libselinux_3.5.orig.tar.gz 211453 SHA256:9a3a3705ac13a2ccca2de6d652b6356fead10f36fb33115c185c5ccdf29eec19
'http://http.debian.net/debian/pool/main/libs/libselinux/libselinux_3.5.orig.tar.gz.asc' libselinux_3.5.orig.tar.gz.asc 981 SHA256:fd37d441e0c08cabe9ac8f7815f52355bab2011549ec5792424fe18be9e1e015
'http://http.debian.net/debian/pool/main/libs/libselinux/libselinux_3.5-2.debian.tar.xz' libselinux_3.5-2.debian.tar.xz 35992 SHA256:e385f14d9700187495a82e433b02b139aebe89c8ceccab5a21598dfef518b0de
```

### `dpkg` source package: `libsemanage=3.5-1`

Binary Packages:

- `libsemanage-common=3.5-1`
- `libsemanage2:amd64=3.5-1+b4`

Licenses: (parsed from: `/usr/share/doc/libsemanage-common/copyright`, `/usr/share/doc/libsemanage2/copyright`)

- `GPL-2`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris libsemanage=3.5-1
'http://http.debian.net/debian/pool/main/libs/libsemanage/libsemanage_3.5-1.dsc' libsemanage_3.5-1.dsc 2644 SHA256:7415394f12030387ebca4ab7845830984b1ceb7ec3256d30a1733ba7f59d18c1
'http://http.debian.net/debian/pool/main/libs/libsemanage/libsemanage_3.5.orig.tar.gz' libsemanage_3.5.orig.tar.gz 185060 SHA256:f53534e50247538280ed0d76c6ce81d8fb3939bd64cadb89da10dba42e40dd9c
'http://http.debian.net/debian/pool/main/libs/libsemanage/libsemanage_3.5.orig.tar.gz.asc' libsemanage_3.5.orig.tar.gz.asc 981 SHA256:f9126c861c666f3308b60cea4405c5e686a056113ca3cbd0a5b0e4af7600c8f5
'http://http.debian.net/debian/pool/main/libs/libsemanage/libsemanage_3.5-1.debian.tar.xz' libsemanage_3.5-1.debian.tar.xz 29956 SHA256:78b11321d014bd52e1fb67c38db5ec6518b0b566b58c6e35a18e894dacc24aee
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

### `dpkg` source package: `libsm=2:1.2.3-1`

Binary Packages:

- `libsm6:amd64=2:1.2.3-1+b1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libsm=2:1.2.3-1
'http://http.debian.net/debian/pool/main/libs/libsm/libsm_1.2.3-1.dsc' libsm_1.2.3-1.dsc 2063 SHA256:5488f8de81d53c32cbb5f062b6a6f262cd067283b8082041392dc60f0d04002c
'http://http.debian.net/debian/pool/main/libs/libsm/libsm_1.2.3.orig.tar.gz' libsm_1.2.3.orig.tar.gz 445362 SHA256:1e92408417cb6c6c477a8a6104291001a40b3bb56a4a60608fdd9cd2c5a0f320
'http://http.debian.net/debian/pool/main/libs/libsm/libsm_1.2.3-1.diff.gz' libsm_1.2.3-1.diff.gz 8929 SHA256:7eb99ab50b19f26d1470f89e4b46891f6a697cb1794a58ed0d1376cceaf1b6a9
```

### `dpkg` source package: `libssh2=1.11.0-7`

Binary Packages:

- `libssh2-1t64:amd64=1.11.0-7`

Licenses: (parsed from: `/usr/share/doc/libssh2-1t64/copyright`)

- `BSD3`
- `ISC`

Source:

```console
$ apt-get source -qq --print-uris libssh2=1.11.0-7
'http://http.debian.net/debian/pool/main/libs/libssh2/libssh2_1.11.0-7.dsc' libssh2_1.11.0-7.dsc 2328 SHA256:8c6c145427dddd3844ab55f9a8ee77f834dbdee05e1f7ebbc25ebf7623b53c70
'http://http.debian.net/debian/pool/main/libs/libssh2/libssh2_1.11.0.orig.tar.gz' libssh2_1.11.0.orig.tar.gz 1053562 SHA256:3736161e41e2693324deb38c26cfdc3efe6209d634ba4258db1cecff6a5ad461
'http://http.debian.net/debian/pool/main/libs/libssh2/libssh2_1.11.0.orig.tar.gz.asc' libssh2_1.11.0.orig.tar.gz.asc 488 SHA256:b6a32c85a3f9b6f30f2b3595ba034b48a8508ee9c94708ef811f58fd7adfcdee
'http://http.debian.net/debian/pool/main/libs/libssh2/libssh2_1.11.0-7.debian.tar.xz' libssh2_1.11.0-7.debian.tar.xz 17000 SHA256:f579fa06d5f2ca2dd89634cb8e40557c4c1606308823ac99a258bdde2cd3bdb6
```

### `dpkg` source package: `libtasn1-6=4.19.0-3`

Binary Packages:

- `libtasn1-6:amd64=4.19.0-3+b2`

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
- `libthai0:amd64=0.1.29-2`

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
- `libtirpc-dev:amd64=1.3.4+ds-1.3`
- `libtirpc3t64:amd64=1.3.4+ds-1.3`

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

### `dpkg` source package: `libunistring=1.2-1`

Binary Packages:

- `libunistring5:amd64=1.2-1`

Licenses: (parsed from: `/usr/share/doc/libunistring5/copyright`)

- `FreeSoftware`
- `GFDL-1.2`
- `GFDL-NIV-1.2+`
- `GPL-2`
- `GPL-2+`
- `GPL-2+ with distribution exception`
- `GPL-2+ with distribution exception, Expat`
- `GPL-3`
- `GPL-3+`
- `LGPL-3`
- `LGPL-3+`
- `X11`

Source:

```console
$ apt-get source -qq --print-uris libunistring=1.2-1
'http://http.debian.net/debian/pool/main/libu/libunistring/libunistring_1.2-1.dsc' libunistring_1.2-1.dsc 2181 SHA256:5d951adce58920ab7e598f04b903f402382557ad102576d01184553437467dd6
'http://http.debian.net/debian/pool/main/libu/libunistring/libunistring_1.2.orig.tar.xz' libunistring_1.2.orig.tar.xz 2502196 SHA256:632bd65ed74a881ca8a0309a1001c428bd1cbd5cd7ddbf8cedcd2e65f4dcdc44
'http://http.debian.net/debian/pool/main/libu/libunistring/libunistring_1.2.orig.tar.xz.asc' libunistring_1.2.orig.tar.xz.asc 833 SHA256:91da3f033231a635dae9e0161c834b74e890e1eba19d4e5972b26c5c312ac2cb
'http://http.debian.net/debian/pool/main/libu/libunistring/libunistring_1.2-1.debian.tar.xz' libunistring_1.2-1.debian.tar.xz 13656 SHA256:0605dbb77c072393abaa9e6ec8507d57d91f62aee4d7a7f968f295e4e9ab3bcf
```

### `dpkg` source package: `libwebp=1.4.0-0.1`

Binary Packages:

- `libsharpyuv0:amd64=1.4.0-0.1`
- `libwebp7:amd64=1.4.0-0.1`

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

### `dpkg` source package: `libx11=2:1.8.7-1`

Binary Packages:

- `libx11-6:amd64=2:1.8.7-1+b1`
- `libx11-data=2:1.8.7-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libx11=2:1.8.7-1
'http://http.debian.net/debian/pool/main/libx/libx11/libx11_1.8.7-1.dsc' libx11_1.8.7-1.dsc 2480 SHA256:96eddec7e55ab344ce654c5043d59bc8da6470eb7849a578c843af965dda79d1
'http://http.debian.net/debian/pool/main/libx/libx11/libx11_1.8.7.orig.tar.gz' libx11_1.8.7.orig.tar.gz 3185363 SHA256:793ebebf569f12c864b77401798d38814b51790fce206e01a431e5feb982e20b
'http://http.debian.net/debian/pool/main/libx/libx11/libx11_1.8.7.orig.tar.gz.asc' libx11_1.8.7.orig.tar.gz.asc 833 SHA256:c1cba69555c89e503abac81ebf1113a756f2fafd72677e7862b40f12208e0260
'http://http.debian.net/debian/pool/main/libx/libx11/libx11_1.8.7-1.diff.gz' libx11_1.8.7-1.diff.gz 74344 SHA256:57adc62acb0ba21a4cf444aaf03ea4adc7f732215df22afa8b8d6fd31d799d95
```

### `dpkg` source package: `libxau=1:1.0.9-1`

Binary Packages:

- `libxau6:amd64=1:1.0.9-1+b1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxau=1:1.0.9-1
'http://http.debian.net/debian/pool/main/libx/libxau/libxau_1.0.9-1.dsc' libxau_1.0.9-1.dsc 2183 SHA256:e6e059652cda7e5a49b6c9a70667639f32d629c20320487d16c642a06c1ebf85
'http://http.debian.net/debian/pool/main/libx/libxau/libxau_1.0.9.orig.tar.gz' libxau_1.0.9.orig.tar.gz 394068 SHA256:1f123d8304b082ad63a9e89376400a3b1d4c29e67e3ea07b3f659cccca690eea
'http://http.debian.net/debian/pool/main/libx/libxau/libxau_1.0.9.orig.tar.gz.asc' libxau_1.0.9.orig.tar.gz.asc 801 SHA256:af6104aaf3c5ede529e381237dd60f49640ec96593a84502fa493b86582b2f04
'http://http.debian.net/debian/pool/main/libx/libxau/libxau_1.0.9-1.diff.gz' libxau_1.0.9-1.diff.gz 10193 SHA256:7b34899563f172e8f11d061de41b58fe1c32f8683d985e57686677ccb7299a9a
```

### `dpkg` source package: `libxcb=1.17.0-2`

Binary Packages:

- `libxcb-render0:amd64=1.17.0-2`
- `libxcb-shm0:amd64=1.17.0-2`
- `libxcb1:amd64=1.17.0-2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxcb=1.17.0-2
'http://http.debian.net/debian/pool/main/libx/libxcb/libxcb_1.17.0-2.dsc' libxcb_1.17.0-2.dsc 5318 SHA256:b2728d156f79d2e757e7378cfcefca52bd570739d2efffa87e1aaeaf4f21de3a
'http://http.debian.net/debian/pool/main/libx/libxcb/libxcb_1.17.0.orig.tar.gz' libxcb_1.17.0.orig.tar.gz 661593 SHA256:2c69287424c9e2128cb47ffe92171e10417041ec2963bceafb65cb3fcf8f0b85
'http://http.debian.net/debian/pool/main/libx/libxcb/libxcb_1.17.0-2.diff.gz' libxcb_1.17.0-2.diff.gz 28069 SHA256:c5b33b67a61d0d1c1b624bf88a8150f4be1ba9b46e855e38f03a8f73858af558
```

### `dpkg` source package: `libxcrypt=1:4.4.36-4`

Binary Packages:

- `libcrypt-dev:amd64=1:4.4.36-4`
- `libcrypt1:amd64=1:4.4.36-4`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxcrypt=1:4.4.36-4
'http://http.debian.net/debian/pool/main/libx/libxcrypt/libxcrypt_4.4.36-4.dsc' libxcrypt_4.4.36-4.dsc 1563 SHA256:8509256bf6ddedebfaf14ad777541d225a6c956f590602f85f5639efc652bfef
'http://http.debian.net/debian/pool/main/libx/libxcrypt/libxcrypt_4.4.36.orig.tar.xz' libxcrypt_4.4.36.orig.tar.xz 392732 SHA256:7b7abbc89f13f5194211aa6861ed954e4fa3a210a4cb64f7e13dc8cf413e7f2a
'http://http.debian.net/debian/pool/main/libx/libxcrypt/libxcrypt_4.4.36-4.debian.tar.xz' libxcrypt_4.4.36-4.debian.tar.xz 8216 SHA256:e61d8a486e6a80a2e3d629296988f8ff2e4dfbef018ec7e94543b5918ca1f329
```

### `dpkg` source package: `libxdmcp=1:1.1.2-3`

Binary Packages:

- `libxdmcp6:amd64=1:1.1.2-3+b1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxdmcp=1:1.1.2-3
'http://http.debian.net/debian/pool/main/libx/libxdmcp/libxdmcp_1.1.2-3.dsc' libxdmcp_1.1.2-3.dsc 2145 SHA256:f9697dca6a275aeee9a3eee9fb2d55e0f77485481e8b84efc6950fc9b1988460
'http://http.debian.net/debian/pool/main/libx/libxdmcp/libxdmcp_1.1.2.orig.tar.gz' libxdmcp_1.1.2.orig.tar.gz 404115 SHA256:6f7c7e491a23035a26284d247779174dedc67e34e93cc3548b648ffdb6fc57c0
'http://http.debian.net/debian/pool/main/libx/libxdmcp/libxdmcp_1.1.2-3.diff.gz' libxdmcp_1.1.2-3.diff.gz 18017 SHA256:5844df115c17e5ba40ac116f80373304d821c607e763ef6f40562421f5cc0cf3
```

### `dpkg` source package: `libxext=2:1.3.4-1`

Binary Packages:

- `libxext6:amd64=2:1.3.4-1+b1`

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

- `libxmuu1:amd64=2:1.1.3-3+b2`

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

- `libxrender1:amd64=1:0.9.10-1.1+b1`

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

- `libxss1:amd64=1:1.2.3-1+b1`

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

- `libxt6t64:amd64=1:1.2.1-1.2`

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

- `libzstd1:amd64=1.5.6+dfsg-1`

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

### `dpkg` source package: `linux=6.10.3-1`

Binary Packages:

- `linux-libc-dev=6.10.3-1`

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
$ apt-get source -qq --print-uris linux=6.10.3-1
'http://http.debian.net/debian/pool/main/l/linux/linux_6.10.3-1.dsc' linux_6.10.3-1.dsc 234339 SHA256:535af850f7e725c2e9a7ca85e092a924f564bbb5aa8e99c2fed43ce99d25a013
'http://http.debian.net/debian/pool/main/l/linux/linux_6.10.3.orig.tar.xz' linux_6.10.3.orig.tar.xz 147942752 SHA256:f43634ad6fd852f81ec252d0451d20bf0ddb3c08007ee700ec3b4b0b7590e4c4
'http://http.debian.net/debian/pool/main/l/linux/linux_6.10.3-1.debian.tar.xz' linux_6.10.3-1.debian.tar.xz 1582204 SHA256:9c5573a30ef13ace3c79d6025025d64d663cd7bd0f7fd4954c06fd14b35d0aa0
```

### `dpkg` source package: `littler=0.3.20-1`

Binary Packages:

- `littler=0.3.20-1`
- `r-cran-littler=0.3.20-1`

Licenses: (parsed from: `/usr/share/doc/littler/copyright`, `/usr/share/doc/r-cran-littler/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris littler=0.3.20-1
'http://http.debian.net/debian/pool/main/l/littler/littler_0.3.20-1.dsc' littler_0.3.20-1.dsc 1874 SHA256:32d5e850ba9237e174a52406e0b013d4aac4b1d8204856b7ca5a64a666ca275a
'http://http.debian.net/debian/pool/main/l/littler/littler_0.3.20.orig.tar.gz' littler_0.3.20.orig.tar.gz 125661 SHA256:9810cca571878782afdd579d81404eb8a951ea4b9171d6bf7bdee7d7ed5b065a
'http://http.debian.net/debian/pool/main/l/littler/littler_0.3.20-1.debian.tar.xz' littler_0.3.20-1.debian.tar.xz 7136 SHA256:809c149ac73569b7c5e62b1112ede9943c405dfcfdba5aedd1cb0ed0c4181f91
```

### `dpkg` source package: `lz4=1.9.4-3`

Binary Packages:

- `liblz4-1:amd64=1.9.4-3`

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

### `dpkg` source package: `make-dfsg=4.3-4.1`

Binary Packages:

- `make=4.3-4.1`

Licenses: (parsed from: `/usr/share/doc/make/copyright`)

- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris make-dfsg=4.3-4.1
'http://http.debian.net/debian/pool/main/m/make-dfsg/make-dfsg_4.3-4.1.dsc' make-dfsg_4.3-4.1.dsc 2019 SHA256:d2523d94f4d4198df6801f238d36cf0dea2ab5521f1d19ee76b2e8ee1f1918bb
'http://http.debian.net/debian/pool/main/m/make-dfsg/make-dfsg_4.3.orig.tar.gz' make-dfsg_4.3.orig.tar.gz 1845906 SHA256:be4c17542578824e745f83bcd2a9ba264206187247cb6a5f5df99b0a9d1f9047
'http://http.debian.net/debian/pool/main/m/make-dfsg/make-dfsg_4.3-4.1.diff.gz' make-dfsg_4.3-4.1.diff.gz 50940 SHA256:753c254ecaba425ebe2e0a0fb4d299847701e1c3eeb43df563e39975cae56b4c
```

### `dpkg` source package: `mawk=1.3.4.20240622-2`

Binary Packages:

- `mawk=1.3.4.20240622-2`

Licenses: (parsed from: `/usr/share/doc/mawk/copyright`)

- `CC-BY-3.0`
- `GPL-2`
- `GPL-2.0-only`
- `X11`

Source:

```console
$ apt-get source -qq --print-uris mawk=1.3.4.20240622-2
'http://http.debian.net/debian/pool/main/m/mawk/mawk_1.3.4.20240622-2.dsc' mawk_1.3.4.20240622-2.dsc 2969 SHA256:cc95afc29fa8e4406f42cd3887de7a10b9d70a84d70341d4e7c962438686db2f
'http://http.debian.net/debian/pool/main/m/mawk/mawk_1.3.4.20240622.orig.tar.gz' mawk_1.3.4.20240622.orig.tar.gz 414190 SHA256:4e917e87a7a9fbaf76995784a4b0b5dc0dd954b977d0983030f78f6a07b1a765
'http://http.debian.net/debian/pool/main/m/mawk/mawk_1.3.4.20240622.orig.tar.gz.asc' mawk_1.3.4.20240622.orig.tar.gz.asc 729 SHA256:1c66d8d18bf562d492a3b33a379c51ec80e111f8203a9546969fd7e436cb7041
'http://http.debian.net/debian/pool/main/m/mawk/mawk_1.3.4.20240622-2.debian.tar.xz' mawk_1.3.4.20240622-2.debian.tar.xz 16136 SHA256:66d5c0f334acce8cd329f3807252d19c53b6b3cecbbf4d42d7c239f54f3ad296
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

- `libmpc3:amd64=1.3.1-1+b2`

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

- `libmpfr6:amd64=4.2.1-1+b1`

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

- `libncurses-dev:amd64=6.5-2`
- `libncurses6:amd64=6.5-2`
- `libncursesw6:amd64=6.5-2`
- `libtinfo6:amd64=6.5-2`
- `ncurses-base=6.5-2`
- `ncurses-bin=6.5-2`

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

- `libhogweed6t64:amd64=3.10-1`
- `libnettle8t64:amd64=3.10-1`

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

### `dpkg` source package: `nghttp2=1.62.1-2`

Binary Packages:

- `libnghttp2-14:amd64=1.62.1-2`

Licenses: (parsed from: `/usr/share/doc/libnghttp2-14/copyright`)

- `BSD-2-clause`
- `Expat`
- `GPL-3`
- `GPL-3+ with autoconf exception`
- `MIT`
- `all-permissive`

Source:

```console
$ apt-get source -qq --print-uris nghttp2=1.62.1-2
'http://http.debian.net/debian/pool/main/n/nghttp2/nghttp2_1.62.1-2.dsc' nghttp2_1.62.1-2.dsc 2531 SHA256:5f457052ee3dad45dce4848fc5bc25106fd5e519972de5788b0841e07e31aee5
'http://http.debian.net/debian/pool/main/n/nghttp2/nghttp2_1.62.1.orig.tar.gz' nghttp2_1.62.1.orig.tar.gz 1066103 SHA256:73c8af772dd2b30cedc114d37291cf1485b0a7ce11833595fc2aec7b3ce3ba5c
'http://http.debian.net/debian/pool/main/n/nghttp2/nghttp2_1.62.1-2.debian.tar.xz' nghttp2_1.62.1-2.debian.tar.xz 38852 SHA256:82131a80852fcc53d378d4e3cb0e27d0b6044ac595d01806b807713942fbfcac
```

### `dpkg` source package: `nlme=3.1.165-1`

Binary Packages:

- `r-cran-nlme=3.1.165-1`

Licenses: (parsed from: `/usr/share/doc/r-cran-nlme/copyright`)

- `GPL`
- `GPL `

Source:

```console
$ apt-get source -qq --print-uris nlme=3.1.165-1
'http://http.debian.net/debian/pool/main/n/nlme/nlme_3.1.165-1.dsc' nlme_3.1.165-1.dsc 1840 SHA256:3ee9e678743381304dd74978beca7ccb0fad3c77e17a100d89b93b126af07d16
'http://http.debian.net/debian/pool/main/n/nlme/nlme_3.1.165.orig.tar.gz' nlme_3.1.165.orig.tar.gz 856244 SHA256:fc37bba493c2138be2f38fcfd2a67327d81ab91a37bad6f698226bb400ec9499
'http://http.debian.net/debian/pool/main/n/nlme/nlme_3.1.165-1.debian.tar.xz' nlme_3.1.165-1.debian.tar.xz 7332 SHA256:581d6f61ec4ef62f29998d05526bcc03fe97c6aa7b310b49928be6fd38beadb5
```

### `dpkg` source package: `openblas=0.3.28+ds-1`

Binary Packages:

- `libopenblas0-pthread:amd64=0.3.28+ds-1`

Licenses: (parsed from: `/usr/share/doc/libopenblas0-pthread/copyright`)

- `Apache-2.0`
- `BSD-2-clause`
- `BSD-2-clause-texas`
- `BSD-3-clause`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris openblas=0.3.28+ds-1
'http://http.debian.net/debian/pool/main/o/openblas/openblas_0.3.28%2bds-1.dsc' openblas_0.3.28+ds-1.dsc 4553 SHA256:85b752cfca840defa44cfe2ffc106152ab134eab6ff472427c170a6f9ff59788
'http://http.debian.net/debian/pool/main/o/openblas/openblas_0.3.28%2bds.orig.tar.xz' openblas_0.3.28+ds.orig.tar.xz 2181324 SHA256:938211591b6ad62285830021192b2a0f98bca70cc7f9aac68edca56e1c4e380d
'http://http.debian.net/debian/pool/main/o/openblas/openblas_0.3.28%2bds-1.debian.tar.xz' openblas_0.3.28+ds-1.debian.tar.xz 24832 SHA256:a34090fa3f32e4eb012b138de0a2f67814612c8a9e865505dae09ab9a246c581
```

### `dpkg` source package: `openldap=2.5.18+dfsg-2`

Binary Packages:

- `libldap-2.5-0:amd64=2.5.18+dfsg-2`

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
$ apt-get source -qq --print-uris openldap=2.5.18+dfsg-2
'http://http.debian.net/debian/pool/main/o/openldap/openldap_2.5.18%2bdfsg-2.dsc' openldap_2.5.18+dfsg-2.dsc 3312 SHA256:0825ff7a10b669bce5b31199ec4a2dcf018080011a1c1020774cec734b465a45
'http://http.debian.net/debian/pool/main/o/openldap/openldap_2.5.18%2bdfsg.orig.tar.xz' openldap_2.5.18+dfsg.orig.tar.xz 3684372 SHA256:06c2f0ee591594ae28cfbde843a70b3e009b1f09d7f3110a1570236ac46a86b5
'http://http.debian.net/debian/pool/main/o/openldap/openldap_2.5.18%2bdfsg-2.debian.tar.xz' openldap_2.5.18+dfsg-2.debian.tar.xz 170128 SHA256:a3606da0c79d9f34a7cae36dac835ffd2ccdd4eda51eea1fdf6d209698fcfc13
```

### `dpkg` source package: `openssl=3.2.2-1`

Binary Packages:

- `libssl3t64:amd64=3.2.2-1`
- `openssl=3.2.2-1`

Licenses: (parsed from: `/usr/share/doc/libssl3t64/copyright`, `/usr/share/doc/openssl/copyright`)

- `Apache-2.0`
- `Artistic`
- `GPL-1`
- `GPL-1+`

Source:

```console
$ apt-get source -qq --print-uris openssl=3.2.2-1
'http://deb.debian.org/debian/pool/main/o/openssl/openssl_3.2.2-1.dsc' openssl_3.2.2-1.dsc 2482 SHA256:0a8f3309b0119606f3fc23007401739504fa5505de98fc0d4c08a9cfc7b2d082
'http://deb.debian.org/debian/pool/main/o/openssl/openssl_3.2.2.orig.tar.gz' openssl_3.2.2.orig.tar.gz 17744472 SHA256:197149c18d9e9f292c43f0400acaba12e5f52cacfe050f3d199277ea738ec2e7
'http://deb.debian.org/debian/pool/main/o/openssl/openssl_3.2.2.orig.tar.gz.asc' openssl_3.2.2.orig.tar.gz.asc 833 SHA256:e236f8871cb18de290430e257dadd06732e7a4f8d8c6f8ffa6abb4686050ac51
'http://deb.debian.org/debian/pool/main/o/openssl/openssl_3.2.2-1.debian.tar.xz' openssl_3.2.2-1.debian.tar.xz 66696 SHA256:ec28f43520ef7fa49f13581c0aaa39086c606874ed10c0e27c4cf75b3d75f9f6
```

Other potentially useful URLs:

- https://sources.debian.net/src/openssl/3.2.2-1/ (for browsing the source)
- https://sources.debian.net/src/openssl/3.2.2-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/openssl/3.2.2-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `p11-kit=0.25.5-2`

Binary Packages:

- `libp11-kit0:amd64=0.25.5-2`

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
'http://http.debian.net/debian/pool/main/p/p11-kit/p11-kit_0.25.5-2.dsc' p11-kit_0.25.5-2.dsc 2538 SHA256:5953f5639503fe32217117e222bbc231130d9e79dda74259b4017b7bfc5bd910
'http://http.debian.net/debian/pool/main/p/p11-kit/p11-kit_0.25.5.orig.tar.xz' p11-kit_0.25.5.orig.tar.xz 1002056 SHA256:04d0a86450cdb1be018f26af6699857171a188ac6d5b8c90786a60854e1198e5
'http://http.debian.net/debian/pool/main/p/p11-kit/p11-kit_0.25.5.orig.tar.xz.asc' p11-kit_0.25.5.orig.tar.xz.asc 228 SHA256:066c92b9d2accb2fda6a2f71e676fb6526fcc153051b1f04ee7d7c8c96a09989
'http://http.debian.net/debian/pool/main/p/p11-kit/p11-kit_0.25.5-2.debian.tar.xz' p11-kit_0.25.5-2.debian.tar.xz 24108 SHA256:df84eb66f6dd2a53796dfbb2edc58a4b37046b19a8d186baf072163cd6c9c528
```

### `dpkg` source package: `pam=1.5.3-7`

Binary Packages:

- `libpam-modules:amd64=1.5.3-7`
- `libpam-modules-bin=1.5.3-7`
- `libpam-runtime=1.5.3-7`
- `libpam0g:amd64=1.5.3-7`

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

### `dpkg` source package: `pango1.0=1.54.0+ds-1`

Binary Packages:

- `libpango-1.0-0:amd64=1.54.0+ds-1`
- `libpangocairo-1.0-0:amd64=1.54.0+ds-1`
- `libpangoft2-1.0-0:amd64=1.54.0+ds-1`

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
$ apt-get source -qq --print-uris pango1.0=1.54.0+ds-1
'http://http.debian.net/debian/pool/main/p/pango1.0/pango1.0_1.54.0%2bds-1.dsc' pango1.0_1.54.0+ds-1.dsc 3514 SHA256:e29894677383fc7f080936665c98eda9fcc5de9bab9266911e18c28f1f90f2c5
'http://http.debian.net/debian/pool/main/p/pango1.0/pango1.0_1.54.0%2bds.orig.tar.xz' pango1.0_1.54.0+ds.orig.tar.xz 1745280 SHA256:2275f1160e492b442a7dfbaa10cf8aeaea83cea1ff0ee1eed9d88fa1e21aebe8
'http://http.debian.net/debian/pool/main/p/pango1.0/pango1.0_1.54.0%2bds-1.debian.tar.xz' pango1.0_1.54.0+ds-1.debian.tar.xz 43584 SHA256:99f63d649520792c5761757ab914c48b53be9fd747049ff516da7d8d257c86dc
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

### `dpkg` source package: `pcre2=10.42-4`

Binary Packages:

- `libpcre2-16-0:amd64=10.42-4+b1`
- `libpcre2-32-0:amd64=10.42-4+b1`
- `libpcre2-8-0:amd64=10.42-4+b1`
- `libpcre2-dev:amd64=10.42-4+b1`
- `libpcre2-posix3:amd64=10.42-4+b1`

Licenses: (parsed from: `/usr/share/doc/libpcre2-16-0/copyright`, `/usr/share/doc/libpcre2-32-0/copyright`, `/usr/share/doc/libpcre2-8-0/copyright`, `/usr/share/doc/libpcre2-dev/copyright`, `/usr/share/doc/libpcre2-posix3/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `BSD-3-clause-Cambridge with BINARY LIBRARY-LIKE PACKAGES exception`
- `X11`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris pcre2=10.42-4
'http://http.debian.net/debian/pool/main/p/pcre2/pcre2_10.42-4.dsc' pcre2_10.42-4.dsc 2302 SHA256:2796d9332a4b4abe5eeada4aa287e8f9765a497b4363e3c49815a6bca5845cfe
'http://http.debian.net/debian/pool/main/p/pcre2/pcre2_10.42.orig.tar.gz' pcre2_10.42.orig.tar.gz 2397194 SHA256:c33b418e3b936ee3153de2c61cc638e7e4fe3156022a5c77d0711bcbb9d64f1f
'http://http.debian.net/debian/pool/main/p/pcre2/pcre2_10.42-4.diff.gz' pcre2_10.42-4.diff.gz 8111 SHA256:b583a75e90b029616c6867eccfeb21031e62df98dd4462f9d13ccb95bb2f09e6
```

### `dpkg` source package: `perl=5.38.2-5`

Binary Packages:

- `libperl5.38t64:amd64=5.38.2-5`
- `perl=5.38.2-5`
- `perl-base=5.38.2-5`
- `perl-modules-5.38=5.38.2-5`

Licenses: (parsed from: `/usr/share/doc/libperl5.38t64/copyright`, `/usr/share/doc/perl/copyright`, `/usr/share/doc/perl-base/copyright`, `/usr/share/doc/perl-modules-5.38/copyright`)

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
$ apt-get source -qq --print-uris perl=5.38.2-5
'http://http.debian.net/debian/pool/main/p/perl/perl_5.38.2-5.dsc' perl_5.38.2-5.dsc 2938 SHA256:c3d9624788c42bcf14003bd110013858906279596a487735cc39494778070137
'http://http.debian.net/debian/pool/main/p/perl/perl_5.38.2.orig-regen-configure.tar.xz' perl_5.38.2.orig-regen-configure.tar.xz 418808 SHA256:4d1b34cc058f9963cb89785ecc040d57f6d7725cd83329cfa4ef8b27566454d2
'http://http.debian.net/debian/pool/main/p/perl/perl_5.38.2.orig.tar.xz' perl_5.38.2.orig.tar.xz 13679524 SHA256:d91115e90b896520e83d4de6b52f8254ef2b70a8d545ffab33200ea9f1cf29e8
'http://http.debian.net/debian/pool/main/p/perl/perl_5.38.2-5.debian.tar.xz' perl_5.38.2-5.debian.tar.xz 168016 SHA256:ef455488cb518f06cb10f3ed927b05e86df347ed22942874bd3f08a197047b0a
```

### `dpkg` source package: `pixman=0.42.2-1`

Binary Packages:

- `libpixman-1-0:amd64=0.42.2-1+b1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris pixman=0.42.2-1
'http://http.debian.net/debian/pool/main/p/pixman/pixman_0.42.2-1.dsc' pixman_0.42.2-1.dsc 2021 SHA256:393302f5ba22d1206c456902baa02cdd577cb74fe35ec6659f587cce67b91b3d
'http://http.debian.net/debian/pool/main/p/pixman/pixman_0.42.2.orig.tar.gz' pixman_0.42.2.orig.tar.gz 959669 SHA256:ea1480efada2fd948bc75366f7c349e1c96d3297d09a3fe62626e38e234a625e
'http://http.debian.net/debian/pool/main/p/pixman/pixman_0.42.2-1.diff.gz' pixman_0.42.2-1.diff.gz 319616 SHA256:dd6472676c68260a298e52f45c485d3cc85c4bf25df8af0f68e37acff7bfed8a
```

### `dpkg` source package: `pkgconf=1.8.1-3`

Binary Packages:

- `libpkgconf3:amd64=1.8.1-3`
- `pkgconf:amd64=1.8.1-3`
- `pkgconf-bin=1.8.1-3`

Licenses: (parsed from: `/usr/share/doc/libpkgconf3/copyright`, `/usr/share/doc/pkgconf/copyright`, `/usr/share/doc/pkgconf-bin/copyright`)

- `BSD-2`
- `BSD-4`
- `GPL-2`
- `GPL-2+`
- `ISC`
- `X11`

Source:

```console
$ apt-get source -qq --print-uris pkgconf=1.8.1-3
'http://http.debian.net/debian/pool/main/p/pkgconf/pkgconf_1.8.1-3.dsc' pkgconf_1.8.1-3.dsc 1638 SHA256:8c103ef4a3e65c6e1559a2e3534e623b32e925e455d32396b06b4dc9231403f2
'http://http.debian.net/debian/pool/main/p/pkgconf/pkgconf_1.8.1.orig.tar.xz' pkgconf_1.8.1.orig.tar.xz 302372 SHA256:644361ada2942be05655d4452eb018791647c31bba429b287f1f68deb2dc6840
'http://http.debian.net/debian/pool/main/p/pkgconf/pkgconf_1.8.1-3.debian.tar.xz' pkgconf_1.8.1-3.debian.tar.xz 15852 SHA256:d1527b3fccaf4c63e50cef4057f64c13a4c30591995fb9e6a58f4f928338f095
```

### `dpkg` source package: `r-base=4.4.1-1`

Binary Packages:

- `r-base=4.4.1-1`
- `r-base-core=4.4.1-1`
- `r-base-dev=4.4.1-1`
- `r-recommended=4.4.1-1`

Licenses: (parsed from: `/usr/share/doc/r-base/copyright`, `/usr/share/doc/r-base-core/copyright`, `/usr/share/doc/r-base-dev/copyright`, `/usr/share/doc/r-recommended/copyright`)

- `Artistic`
- `GPL-2`
- `GPL-3`
- `LGPL-2`
- `LGPL-2.1`
- `LGPL-3`

Source:

```console
$ apt-get source -qq --print-uris r-base=4.4.1-1
'http://http.debian.net/debian/pool/main/r/r-base/r-base_4.4.1-1.dsc' r-base_4.4.1-1.dsc 2939 SHA256:392708779e998676f415532c9dca25bfdea34b24bcc186d8a54d8538a9ff67ae
'http://http.debian.net/debian/pool/main/r/r-base/r-base_4.4.1.orig.tar.gz' r-base_4.4.1.orig.tar.gz 37353459 SHA256:b4cb675deaaeb7299d3b265d218cde43f192951ce5b89b7bb1a5148a36b2d94d
'http://http.debian.net/debian/pool/main/r/r-base/r-base_4.4.1-1.debian.tar.xz' r-base_4.4.1-1.debian.tar.xz 99948 SHA256:022ab8bf36e0c8148cf10298423b30f336c750a9d385652e1026726b07672c7e
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

### `dpkg` source package: `readline=8.2-4`

Binary Packages:

- `libreadline-dev:amd64=8.2-4`
- `libreadline8t64:amd64=8.2-4`
- `readline-common=8.2-4`

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
$ apt-get source -qq --print-uris readline=8.2-4
'http://http.debian.net/debian/pool/main/r/readline/readline_8.2-4.dsc' readline_8.2-4.dsc 2811 SHA256:c363fc6bc293a4bbb429e89f069eefbff99c754a6e41fcd1b967db6848ea321d
'http://http.debian.net/debian/pool/main/r/readline/readline_8.2.orig.tar.gz' readline_8.2.orig.tar.gz 3043952 SHA256:3feb7171f16a84ee82ca18a36d7b9be109a52c04f492a053331d7d1095007c35
'http://http.debian.net/debian/pool/main/r/readline/readline_8.2-4.debian.tar.xz' readline_8.2-4.debian.tar.xz 33700 SHA256:dcd6d20ed594b864fc8d964f4f3a76dfbfa22193c0fad6d095bfd3fadad4b8d9
```

### `dpkg` source package: `rmatrix=1.7-0-3`

Binary Packages:

- `r-cran-matrix=1.7-0-3`

Licenses: (parsed from: `/usr/share/doc/r-cran-matrix/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris rmatrix=1.7-0-3
'http://http.debian.net/debian/pool/main/r/rmatrix/rmatrix_1.7-0-3.dsc' rmatrix_1.7-0-3.dsc 1860 SHA256:523ea89ed973b9acf62a5f62d5f44b10565761510f00d9cd1fa16dbb021c5a02
'http://http.debian.net/debian/pool/main/r/rmatrix/rmatrix_1.7-0.orig.tar.gz' rmatrix_1.7-0.orig.tar.gz 2471290 SHA256:fb97bba0df370222eb4f7e2da2e94dd01053b5e054b1c51829ff9a6efc08ad37
'http://http.debian.net/debian/pool/main/r/rmatrix/rmatrix_1.7-0-3.debian.tar.xz' rmatrix_1.7-0-3.debian.tar.xz 6060 SHA256:57c145b929c54530e09fe89f88a750709d6ab13823943da26743de0ab39479c2
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

- `librtmp1:amd64=2.4+20151223.gitfa8646d.1-2+b4`

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

### `dpkg` source package: `shadow=1:4.15.3-2`

Binary Packages:

- `login=1:4.15.3-2`
- `passwd=1:4.15.3-2`

Licenses: (parsed from: `/usr/share/doc/login/copyright`, `/usr/share/doc/passwd/copyright`)

- `BSD-3-clause`
- `GPL-1`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris shadow=1:4.15.3-2
'http://deb.debian.org/debian/pool/main/s/shadow/shadow_4.15.3-2.dsc' shadow_4.15.3-2.dsc 2642 SHA256:590dd3eaec38bd6ab1ff06f44633ebd913c66f951004c4024ba2004bce32837c
'http://deb.debian.org/debian/pool/main/s/shadow/shadow_4.15.3.orig.tar.xz' shadow_4.15.3.orig.tar.xz 2054548 SHA256:32303f204907eb0d6c32b7908414885be53a4caf00f149f54991ac3ce424652e
'http://deb.debian.org/debian/pool/main/s/shadow/shadow_4.15.3-2.debian.tar.xz' shadow_4.15.3-2.debian.tar.xz 171112 SHA256:c1e568ca0bf83fc72c26e566e162a465480ec89e1c1f3d8d8ea865344295334e
```

Other potentially useful URLs:

- https://sources.debian.net/src/shadow/1:4.15.3-2/ (for browsing the source)
- https://sources.debian.net/src/shadow/1:4.15.3-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/shadow/1:4.15.3-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `survival=3.7-0-1`

Binary Packages:

- `r-cran-survival=3.7-0-1`

Licenses: (parsed from: `/usr/share/doc/r-cran-survival/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris survival=3.7-0-1
'http://http.debian.net/debian/pool/main/s/survival/survival_3.7-0-1.dsc' survival_3.7-0-1.dsc 1861 SHA256:c92017025736f7ac54a3de80be0308712394fb16a7254c4767a77d9a33a1b79b
'http://http.debian.net/debian/pool/main/s/survival/survival_3.7-0.orig.tar.gz' survival_3.7-0.orig.tar.gz 6918683 SHA256:cd96b08ec928b0028f69c942cc788e190b4543c8518d71deb6d8a712de44feef
'http://http.debian.net/debian/pool/main/s/survival/survival_3.7-0-1.debian.tar.xz' survival_3.7-0-1.debian.tar.xz 6368 SHA256:0477f8f04224af8b57003d3b1c7609b5007075c925c799311d02d05807b119bc
```

### `dpkg` source package: `systemd=256.4-2`

Binary Packages:

- `libsystemd0:amd64=256.4-2`
- `libudev1:amd64=256.4-2`

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

- http://snapshot.debian.org/package/systemd/256.4-2/


### `dpkg` source package: `sysvinit=3.09-2`

Binary Packages:

- `sysvinit-utils=3.09-2`

Licenses: (parsed from: `/usr/share/doc/sysvinit-utils/copyright`)

- `GPL-2`
- `GPL-2.0`
- `GPL-2.0+`
- `GPL-3`
- `GPL-3.0`
- `LGPL-2.1`
- `LGPL-2.1+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/sysvinit/3.09-2/


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

Source:

```console
$ apt-get source -qq --print-uris tar=1.35+dfsg-3
'http://http.debian.net/debian/pool/main/t/tar/tar_1.35%2bdfsg-3.dsc' tar_1.35+dfsg-3.dsc 2009 SHA256:0ea713a8af04a41d297202e7ac20813735328a5f8d4de3882fba5595709955f8
'http://http.debian.net/debian/pool/main/t/tar/tar_1.35%2bdfsg.orig.tar.xz' tar_1.35+dfsg.orig.tar.xz 2111608 SHA256:9ae57e981c1e73c0eebc2b26c9b0c4497fe310ef1d516ea430efb5470b71f7a8
'http://http.debian.net/debian/pool/main/t/tar/tar_1.35%2bdfsg-3.debian.tar.xz' tar_1.35+dfsg-3.debian.tar.xz 20824 SHA256:6028f2172de2498b8fc2baef4854796d829ae7ba2a91de4f7615fe1a56729313
```

### `dpkg` source package: `tcl8.6=8.6.14+dfsg-1`

Binary Packages:

- `libtcl8.6:amd64=8.6.14+dfsg-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris tcl8.6=8.6.14+dfsg-1
'http://http.debian.net/debian/pool/main/t/tcl8.6/tcl8.6_8.6.14%2bdfsg-1.dsc' tcl8.6_8.6.14+dfsg-1.dsc 2120 SHA256:7a1177cbc18123f6205599e48a819daca9e249c4feef3f7a523325a15c7e95de
'http://http.debian.net/debian/pool/main/t/tcl8.6/tcl8.6_8.6.14%2bdfsg.orig.tar.gz' tcl8.6_8.6.14+dfsg.orig.tar.gz 7091313 SHA256:dc6b06142abfc46692c2f614064f930aa0d3ea2d59ee185dc27399b5d0503ee1
'http://http.debian.net/debian/pool/main/t/tcl8.6/tcl8.6_8.6.14%2bdfsg-1.debian.tar.xz' tcl8.6_8.6.14+dfsg-1.debian.tar.xz 14392 SHA256:dc8d6589b1394ad85995316cbd61468fcd320dafb54b6fb80af571fea3ee0c9a
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

### `dpkg` source package: `tiff=4.5.1+git230720-4`

Binary Packages:

- `libtiff6:amd64=4.5.1+git230720-4`

Licenses: (parsed from: `/usr/share/doc/libtiff6/copyright`)

- `Hylafax`

Source:

```console
$ apt-get source -qq --print-uris tiff=4.5.1+git230720-4
'http://http.debian.net/debian/pool/main/t/tiff/tiff_4.5.1%2bgit230720-4.dsc' tiff_4.5.1+git230720-4.dsc 2322 SHA256:84f3fe1110e4633c897e63a6cc0122d2db3afb36140f089ec727ffe0f61facd1
'http://http.debian.net/debian/pool/main/t/tiff/tiff_4.5.1%2bgit230720.orig.tar.xz' tiff_4.5.1+git230720.orig.tar.xz 1781896 SHA256:0e51bcf3a3ffa5fc76ea6aeb74a797f95c84544fcc8b6a1ec5def967a78e9e12
'http://http.debian.net/debian/pool/main/t/tiff/tiff_4.5.1%2bgit230720-4.debian.tar.xz' tiff_4.5.1+git230720-4.debian.tar.xz 26260 SHA256:a4ba563349fe2e53759703dce1aa476cbb3621ab3b4389df97faf60dd06067ad
```

### `dpkg` source package: `tk8.6=8.6.14-1`

Binary Packages:

- `libtk8.6:amd64=8.6.14-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris tk8.6=8.6.14-1
'http://http.debian.net/debian/pool/main/t/tk8.6/tk8.6_8.6.14-1.dsc' tk8.6_8.6.14-1.dsc 2155 SHA256:8bd5f18ca453634ca47774f84759e49fc14c63a4ee42420bd993b552fa12ef8d
'http://http.debian.net/debian/pool/main/t/tk8.6/tk8.6_8.6.14.orig.tar.gz' tk8.6_8.6.14.orig.tar.gz 4510695 SHA256:8ffdb720f47a6ca6107eac2dd877e30b0ef7fac14f3a84ebbd0b3612cee41a94
'http://http.debian.net/debian/pool/main/t/tk8.6/tk8.6_8.6.14-1.debian.tar.xz' tk8.6_8.6.14-1.debian.tar.xz 10784 SHA256:338adc7b48ca96204b66332260349e77aba89731942c6ff597219cc08acfb336
```

### `dpkg` source package: `tzdata=2024a-4`

Binary Packages:

- `tzdata=2024a-4`

Licenses: (parsed from: `/usr/share/doc/tzdata/copyright`)

- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris tzdata=2024a-4
'http://http.debian.net/debian/pool/main/t/tzdata/tzdata_2024a-4.dsc' tzdata_2024a-4.dsc 2429 SHA256:053c342511ece9a0eec2c9d60a6670dd9bce379dcb0bfad88d2167a2786ecb3f
'http://http.debian.net/debian/pool/main/t/tzdata/tzdata_2024a.orig.tar.gz' tzdata_2024a.orig.tar.gz 451270 SHA256:0d0434459acbd2059a7a8da1f3304a84a86591f6ed69c6248fffa502b6edffe3
'http://http.debian.net/debian/pool/main/t/tzdata/tzdata_2024a.orig.tar.gz.asc' tzdata_2024a.orig.tar.gz.asc 833 SHA256:f64725f9f65419e7b009e3b95b75ea9516382d0be64aef63d78654d9c569ed0d
'http://http.debian.net/debian/pool/main/t/tzdata/tzdata_2024a-4.debian.tar.xz' tzdata_2024a-4.debian.tar.xz 124152 SHA256:ff5dbfa986ebcb1705ca0256163738c56538baf3a6778f53d616407d8da9ccac
```

### `dpkg` source package: `ucf=3.0043+nmu1`

Binary Packages:

- `ucf=3.0043+nmu1`

Licenses: (parsed from: `/usr/share/doc/ucf/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris ucf=3.0043+nmu1
'http://http.debian.net/debian/pool/main/u/ucf/ucf_3.0043%2bnmu1.dsc' ucf_3.0043+nmu1.dsc 1567 SHA256:5ef70fa7a58cd3f162932661453a1e9d21d749b47a1aa84198f7c4cd9eac20ee
'http://http.debian.net/debian/pool/main/u/ucf/ucf_3.0043%2bnmu1.tar.xz' ucf_3.0043+nmu1.tar.xz 70916 SHA256:a07143046236cb082517e346362306cb3fe4d3634cad1add40c905b0e0ecf58c
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

### `dpkg` source package: `util-linux=2.40.2-1`

Binary Packages:

- `bsdutils=1:2.40.2-1`
- `libblkid1:amd64=2.40.2-1`
- `libmount1:amd64=2.40.2-1`
- `libsmartcols1:amd64=2.40.2-1`
- `libuuid1:amd64=2.40.2-1`
- `mount=2.40.2-1`
- `util-linux=2.40.2-1`

Licenses: (parsed from: `/usr/share/doc/bsdutils/copyright`, `/usr/share/doc/libblkid1/copyright`, `/usr/share/doc/libmount1/copyright`, `/usr/share/doc/libsmartcols1/copyright`, `/usr/share/doc/libuuid1/copyright`, `/usr/share/doc/mount/copyright`, `/usr/share/doc/util-linux/copyright`)

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
$ apt-get source -qq --print-uris util-linux=2.40.2-1
'http://deb.debian.org/debian/pool/main/u/util-linux/util-linux_2.40.2-1.dsc' util-linux_2.40.2-1.dsc 4895 SHA256:248acada7559476267ba3df897cf57c6fab8c36b8d4e0e358a407823982e20cc
'http://deb.debian.org/debian/pool/main/u/util-linux/util-linux_2.40.2.orig.tar.xz' util-linux_2.40.2.orig.tar.xz 8854820 SHA256:d78b37a66f5922d70edf3bdfb01a6b33d34ed3c3cafd6628203b2a2b67c8e8b3
'http://deb.debian.org/debian/pool/main/u/util-linux/util-linux_2.40.2-1.debian.tar.xz' util-linux_2.40.2-1.debian.tar.xz 107084 SHA256:96189569a03febed4118c89e3e8c58a2d094772db1f2913bedd885caf4b80a43
```

Other potentially useful URLs:

- https://sources.debian.net/src/util-linux/2.40.2-1/ (for browsing the source)
- https://sources.debian.net/src/util-linux/2.40.2-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/util-linux/2.40.2-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `vim=2:9.1.0496-1`

Binary Packages:

- `vim-common=2:9.1.0496-1`
- `vim-tiny=2:9.1.0496-1+b1`

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
- `Vim`
- `Vim-Regexp`
- `X11`
- `XPM`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris vim=2:9.1.0496-1
'http://http.debian.net/debian/pool/main/v/vim/vim_9.1.0496-1.dsc' vim_9.1.0496-1.dsc 3202 SHA256:71a7875f5124187f5f68e4d692f40737313dce6a5fa0c7d93f5b1a4508ac9f50
'http://http.debian.net/debian/pool/main/v/vim/vim_9.1.0496.orig.tar.xz' vim_9.1.0496.orig.tar.xz 11866004 SHA256:27c3c1e931164873d5ac1fac250a204a4cc63454f2298c07717179985eefe43d
'http://http.debian.net/debian/pool/main/v/vim/vim_9.1.0496-1.debian.tar.xz' vim_9.1.0496-1.debian.tar.xz 187972 SHA256:5317a138b711411885479ceab0e6a574f6205ea95eb7f30fd78b571e2def8a12
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

### `dpkg` source package: `xauth=1:1.1.2-1`

Binary Packages:

- `xauth=1:1.1.2-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris xauth=1:1.1.2-1
'http://http.debian.net/debian/pool/main/x/xauth/xauth_1.1.2-1.dsc' xauth_1.1.2-1.dsc 1840 SHA256:5b6f718530b68c385368bae7267e7dd0044882290e7b3e4fbe6d63bb8d65c9f0
'http://http.debian.net/debian/pool/main/x/xauth/xauth_1.1.2.orig.tar.gz' xauth_1.1.2.orig.tar.gz 214621 SHA256:84d27a1023d8da524c134f424b312e53cb96e08871f96868aa20316bfcbbc054
'http://http.debian.net/debian/pool/main/x/xauth/xauth_1.1.2-1.diff.gz' xauth_1.1.2-1.diff.gz 18091 SHA256:6afd6f9a3c9b6320e4b523bbe6e5ff3960d59310c9b0efc8b6496d39144710ed
```

### `dpkg` source package: `xdg-utils=1.1.3-4.1`

Binary Packages:

- `xdg-utils=1.1.3-4.1`

Licenses: (parsed from: `/usr/share/doc/xdg-utils/copyright`)

- `Expat`

Source:

```console
$ apt-get source -qq --print-uris xdg-utils=1.1.3-4.1
'http://http.debian.net/debian/pool/main/x/xdg-utils/xdg-utils_1.1.3-4.1.dsc' xdg-utils_1.1.3-4.1.dsc 1756 SHA256:c54ae65034c4c3e9f2208a44990111d34fc5ed1e689efd3907a2a8e5e965ccac
'http://http.debian.net/debian/pool/main/x/xdg-utils/xdg-utils_1.1.3.orig.tar.gz' xdg-utils_1.1.3.orig.tar.gz 297170 SHA256:d798b08af8a8e2063ddde6c9fa3398ca81484f27dec642c5627ffcaa0d4051d9
'http://http.debian.net/debian/pool/main/x/xdg-utils/xdg-utils_1.1.3-4.1.debian.tar.xz' xdg-utils_1.1.3-4.1.debian.tar.xz 15660 SHA256:0ea0b550719ab75f9a0fe58ed907673c5bcfc2bd87537845534694c502740aed
```

### `dpkg` source package: `xft=2.3.6-1`

Binary Packages:

- `libxft2:amd64=2.3.6-1+b1`

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

- `libxxhash0:amd64=0.8.2-2+b1`

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

### `dpkg` source package: `xz-utils=5.6.2-2`

Binary Packages:

- `liblzma-dev:amd64=5.6.2-2`
- `liblzma5:amd64=5.6.2-2`
- `xz-utils=5.6.2-2`

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
$ apt-get source -qq --print-uris xz-utils=5.6.2-2
'http://http.debian.net/debian/pool/main/x/xz-utils/xz-utils_5.6.2-2.dsc' xz-utils_5.6.2-2.dsc 2704 SHA256:3eadad7376915923c17d22cbe3905c3985b538ada1f46dc742a1675819130af5
'http://http.debian.net/debian/pool/main/x/xz-utils/xz-utils_5.6.2.orig.tar.xz' xz-utils_5.6.2.orig.tar.xz 1307448 SHA256:a9db3bb3d64e248a0fae963f8fb6ba851a26ba1822e504dc0efd18a80c626caf
'http://http.debian.net/debian/pool/main/x/xz-utils/xz-utils_5.6.2.orig.tar.xz.asc' xz-utils_5.6.2.orig.tar.xz.asc 833 SHA256:297c242cb55ae70242e8773ee8099c6561b9d8a49dab3b3cfccb33465c108e20
'http://http.debian.net/debian/pool/main/x/xz-utils/xz-utils_5.6.2-2.debian.tar.xz' xz-utils_5.6.2-2.debian.tar.xz 24560 SHA256:b269af8285f4226b2e70e98e917a16b83cbe316e27d6121d11a0b89f0d39a7c9
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

- `zlib1g:amd64=1:1.3.dfsg+really1.3.1-1`
- `zlib1g-dev:amd64=1:1.3.dfsg+really1.3.1-1`

Licenses: (parsed from: `/usr/share/doc/zlib1g/copyright`, `/usr/share/doc/zlib1g-dev/copyright`)

- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris zlib=1:1.3.dfsg+really1.3.1-1
'http://http.debian.net/debian/pool/main/z/zlib/zlib_1.3.dfsg%2breally1.3.1-1.dsc' zlib_1.3.dfsg+really1.3.1-1.dsc 2637 SHA256:ede2791e29c1d3b422f9208bdd7edf040c20445ea1e7453a72037576e64fa197
'http://http.debian.net/debian/pool/main/z/zlib/zlib_1.3.dfsg%2breally1.3.1.orig.tar.gz' zlib_1.3.dfsg+really1.3.1.orig.tar.gz 1325737 SHA256:60dd315c07f616887caa029408308a018ace66e3d142726a97db164b3b8f69fb
'http://http.debian.net/debian/pool/main/z/zlib/zlib_1.3.dfsg%2breally1.3.1-1.debian.tar.xz' zlib_1.3.dfsg+really1.3.1-1.debian.tar.xz 16576 SHA256:9ed525955ce9fb0c1b39be8ff98f73450dbfc6305a9a27e6149c8972d38a0a9e
```
