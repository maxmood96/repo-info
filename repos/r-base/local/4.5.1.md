# `r-base:4.5.1`

## Docker Metadata

- Image ID: `sha256:34f43a399fd2946301d44547f825eb2b3b3328facef824b72948508f17bee87c`
- Created: `2025-06-13T15:18:05Z`
- Virtual Size: ~ 864.89 Mb  
  (total size of all layers on-disk)
- Arch: `linux`/`amd64`
- Command: `["R"]`
- Environment:
  - `PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin`
  - `LC_ALL=en_US.UTF-8`
  - `LANG=en_US.UTF-8`
  - `R_BASE_VERSION=4.5.1`
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

### `dpkg` source package: `apt=3.0.2`

Binary Packages:

- `apt=3.0.2`
- `libapt-pkg7.0:amd64=3.0.2`

Licenses: (parsed from: `/usr/share/doc/apt/copyright`, `/usr/share/doc/libapt-pkg7.0/copyright`)

- `BSD-3-clause`
- `Expat`
- `GPL-2`
- `GPL-2+`
- `curl`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/apt/3.0.2/


### `dpkg` source package: `attr=1:2.5.2-3`

Binary Packages:

- `libattr1:amd64=1:2.5.2-3`

Licenses: (parsed from: `/usr/share/doc/libattr1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2+`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris attr=1:2.5.2-3
'http://http.debian.net/debian/pool/main/a/attr/attr_2.5.2-3.dsc' attr_2.5.2-3.dsc 2576 SHA256:c2ae3e15db059029030ddf4fdac179d8f90d423f2310a6ef8c745ba28ac18b0a
'http://http.debian.net/debian/pool/main/a/attr/attr_2.5.2.orig.tar.xz' attr_2.5.2.orig.tar.xz 334180 SHA256:f2e97b0ab7ce293681ab701915766190d607a1dba7fae8a718138150b700a70b
'http://http.debian.net/debian/pool/main/a/attr/attr_2.5.2.orig.tar.xz.asc' attr_2.5.2.orig.tar.xz.asc 833 SHA256:eeac729088d3c6379e91b7596cb3582e46b047c47f0fa3c5c77f9c9e84dc3a4c
'http://http.debian.net/debian/pool/main/a/attr/attr_2.5.2-3.debian.tar.xz' attr_2.5.2-3.debian.tar.xz 32260 SHA256:153f98c87575277ea021e24dae36293b7738699174438a2060b47e8312b771e3
```

### `dpkg` source package: `audit=1:4.0.2-2`

Binary Packages:

- `libaudit-common=1:4.0.2-2`
- `libaudit1:amd64=1:4.0.2-2+b2`

Licenses: (parsed from: `/usr/share/doc/libaudit-common/copyright`, `/usr/share/doc/libaudit1/copyright`)

- `GPL-1`
- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris audit=1:4.0.2-2
'http://deb.debian.org/debian/pool/main/a/audit/audit_4.0.2-2.dsc' audit_4.0.2-2.dsc 2408 SHA256:d0b9457933409cd3287bc0b8bfb10f41c08fb5b24bd5c5b8364125d5a6894974
'http://deb.debian.org/debian/pool/main/a/audit/audit_4.0.2.orig.tar.gz' audit_4.0.2.orig.tar.gz 1198769 SHA256:d5d1b5d50ee4a2d0d17875bc6ae6bd6a7d5b34d9557ea847a39faec531faaa0a
'http://deb.debian.org/debian/pool/main/a/audit/audit_4.0.2-2.debian.tar.xz' audit_4.0.2-2.debian.tar.xz 19228 SHA256:33030d53299c57cda73e9e45813b8488f9bc3ad8992aef0b740afabbf66a2ba2
```

Other potentially useful URLs:

- https://sources.debian.net/src/audit/1:4.0.2-2/ (for browsing the source)
- https://sources.debian.net/src/audit/1:4.0.2-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/audit/1:4.0.2-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `base-files=13.8`

Binary Packages:

- `base-files=13.8`

Licenses: (parsed from: `/usr/share/doc/base-files/copyright`)

- `GPL`
- `GPL-2+`
- `verbatim`

Source:

```console
$ apt-get source -qq --print-uris base-files=13.8
'http://http.debian.net/debian/pool/main/b/base-files/base-files_13.8.dsc' base-files_13.8.dsc 1215 SHA256:7affd67993afe347ed581d242fdb591ca4585a513446d24ad5e313f4d2895785
'http://http.debian.net/debian/pool/main/b/base-files/base-files_13.8.tar.xz' base-files_13.8.tar.xz 68600 SHA256:b2776447ed88d510aa5fa65f0b8ad144811e59d7bf943b977d29c94de0c7e368
```

### `dpkg` source package: `base-passwd=3.6.7`

Binary Packages:

- `base-passwd=3.6.7`

Licenses: (parsed from: `/usr/share/doc/base-passwd/copyright`)

- `GPL-2`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris base-passwd=3.6.7
'http://http.debian.net/debian/pool/main/b/base-passwd/base-passwd_3.6.7.dsc' base-passwd_3.6.7.dsc 1891 SHA256:23dafe71f85d7595d9e20efba17729c1c975a33bd469cf09bfad9e96b1f542f3
'http://http.debian.net/debian/pool/main/b/base-passwd/base-passwd_3.6.7.tar.xz' base-passwd_3.6.7.tar.xz 60872 SHA256:cf869870fed7862b57bfa9e99cd5cd6f365e2349705a1b65af7fc182629bd1ab
```

### `dpkg` source package: `bash=5.2.37-2`

Binary Packages:

- `bash=5.2.37-2+b3`

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
$ apt-get source -qq --print-uris bash=5.2.37-2
'http://http.debian.net/debian/pool/main/b/bash/bash_5.2.37-2.dsc' bash_5.2.37-2.dsc 2162 SHA256:7e5f6d5a26093e812f8841d5cf3245054102e86986017d8edd859417b03707f9
'http://http.debian.net/debian/pool/main/b/bash/bash_5.2.37.orig.tar.xz' bash_5.2.37.orig.tar.xz 5600932 SHA256:370704c9c859f4060b7df19055e43bb9b5fa09d887699cf6ba87885c5485d36a
'http://http.debian.net/debian/pool/main/b/bash/bash_5.2.37-2.debian.tar.xz' bash_5.2.37-2.debian.tar.xz 88360 SHA256:42e03ef523258b61fa765b8c9719d7bf461f2a274260d07fbe45ca7e4627923a
```

### `dpkg` source package: `binutils=2.44-3`

Binary Packages:

- `binutils=2.44-3`
- `binutils-common:amd64=2.44-3`
- `binutils-x86-64-linux-gnu=2.44-3`
- `libbinutils:amd64=2.44-3`
- `libctf-nobfd0:amd64=2.44-3`
- `libctf0:amd64=2.44-3`
- `libgprofng0:amd64=2.44-3`
- `libsframe1:amd64=2.44-3`

Licenses: (parsed from: `/usr/share/doc/binutils/copyright`, `/usr/share/doc/binutils-common/copyright`, `/usr/share/doc/binutils-x86-64-linux-gnu/copyright`, `/usr/share/doc/libbinutils/copyright`, `/usr/share/doc/libctf-nobfd0/copyright`, `/usr/share/doc/libctf0/copyright`, `/usr/share/doc/libgprofng0/copyright`, `/usr/share/doc/libsframe1/copyright`)

- `GFDL`
- `GPL`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris binutils=2.44-3
'http://http.debian.net/debian/pool/main/b/binutils/binutils_2.44-3.dsc' binutils_2.44-3.dsc 11429 SHA256:5abd1ae1adb61fd8ecbadfdc16668738668e81c745884aefa0ce97791b2a74b8
'http://http.debian.net/debian/pool/main/b/binutils/binutils_2.44.orig.tar.xz' binutils_2.44.orig.tar.xz 27504768 SHA256:c41a0272424f41bb01bf828e7ffef1b2d59d1788064fd6b5f1d971717e9320b8
'http://http.debian.net/debian/pool/main/b/binutils/binutils_2.44-3.debian.tar.xz' binutils_2.44-3.debian.tar.xz 131700 SHA256:555c856d6fb5a797c2692c24c3083e7b1a76811a470eaab01d90c969c2f92784
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

- `libbrotli1:amd64=1.1.0-2+b7`

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

### `dpkg` source package: `ca-certificates=20250419`

Binary Packages:

- `ca-certificates=20250419`

Licenses: (parsed from: `/usr/share/doc/ca-certificates/copyright`)

- `GPL-2`
- `GPL-2+`
- `MPL-2.0`

Source:

```console
$ apt-get source -qq --print-uris ca-certificates=20250419
'http://http.debian.net/debian/pool/main/c/ca-certificates/ca-certificates_20250419.dsc' ca-certificates_20250419.dsc 1766 SHA256:3fc919369a3b84e34a959faa8bdffb9bd2c5a7d4a948a4b07a09a5d43e257030
'http://http.debian.net/debian/pool/main/c/ca-certificates/ca-certificates_20250419.tar.xz' ca-certificates_20250419.tar.xz 277504 SHA256:33b44ef78653ecd3f0f2f13e5bba6be466be2e7da72182f737912b81798ba5d2
```

### `dpkg` source package: `cairo=1.18.4-1`

Binary Packages:

- `libcairo2:amd64=1.18.4-1+b1`

Licenses: (parsed from: `/usr/share/doc/libcairo2/copyright`)

- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris cairo=1.18.4-1
'http://http.debian.net/debian/pool/main/c/cairo/cairo_1.18.4-1.dsc' cairo_1.18.4-1.dsc 2763 SHA256:717ca0717208ae5ef1ab354e47328867ee7038fe65fb75e0ce366139b34bf67f
'http://http.debian.net/debian/pool/main/c/cairo/cairo_1.18.4.orig.tar.xz' cairo_1.18.4.orig.tar.xz 32578804 SHA256:445ed8208a6e4823de1226a74ca319d3600e83f6369f99b14265006599c32ccb
'http://http.debian.net/debian/pool/main/c/cairo/cairo_1.18.4-1.debian.tar.xz' cairo_1.18.4-1.debian.tar.xz 29920 SHA256:bf2d9ea10097fd06faf6b4ef2149677e7aa0eb8abf85aa5d46851ea11a713f68
```

### `dpkg` source package: `cdebconf=0.278`

Binary Packages:

- `libdebconfclient0:amd64=0.278`

Licenses: (parsed from: `/usr/share/doc/libdebconfclient0/copyright`)

- `BSD-2-Clause`
- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris cdebconf=0.278
'http://http.debian.net/debian/pool/main/c/cdebconf/cdebconf_0.278.dsc' cdebconf_0.278.dsc 2707 SHA256:57ed5abc75180c6e400b0c5e2d2fc5a179478d2460231fe7232ffbd6c65d9415
'http://http.debian.net/debian/pool/main/c/cdebconf/cdebconf_0.278.tar.xz' cdebconf_0.278.tar.xz 285660 SHA256:d66b6500dcc041c39553b62ff2f50b1d0f2ba29435cf1b79f66512a0a3b8156a
```

### `dpkg` source package: `cluster=2.1.8.1-1`

Binary Packages:

- `r-cran-cluster=2.1.8.1-1`

Licenses: (parsed from: `/usr/share/doc/r-cran-cluster/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris cluster=2.1.8.1-1
'http://http.debian.net/debian/pool/main/c/cluster/cluster_2.1.8.1-1.dsc' cluster_2.1.8.1-1.dsc 1845 SHA256:c085f1ba08fb98239dd0f65f49262ae77d835056d8998e5179695aae65f85152
'http://http.debian.net/debian/pool/main/c/cluster/cluster_2.1.8.1.orig.tar.gz' cluster_2.1.8.1.orig.tar.gz 372103 SHA256:4b95b78e09b17ddca72edc0bb180c753c004ed2f61c3eb12e0451ac77f441e57
'http://http.debian.net/debian/pool/main/c/cluster/cluster_2.1.8.1-1.debian.tar.xz' cluster_2.1.8.1-1.debian.tar.xz 4392 SHA256:e4a98e91a7f14ae37690affc02c8f18553563c80d8dfbb886206b5b53f634b3c
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

### `dpkg` source package: `coreutils=9.7-3`

Binary Packages:

- `coreutils=9.7-3`

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
$ apt-get source -qq --print-uris coreutils=9.7-3
'http://http.debian.net/debian/pool/main/c/coreutils/coreutils_9.7-3.dsc' coreutils_9.7-3.dsc 2122 SHA256:c3a207e3aaad165765c7a6fab89045f5fd20035fea6830b9f9ebbb92ebfbff89
'http://http.debian.net/debian/pool/main/c/coreutils/coreutils_9.7.orig.tar.xz' coreutils_9.7.orig.tar.xz 6158960 SHA256:e8bb26ad0293f9b5a1fc43fb42ba970e312c66ce92c1b0b16713d7500db251bf
'http://http.debian.net/debian/pool/main/c/coreutils/coreutils_9.7.orig.tar.xz.asc' coreutils_9.7.orig.tar.xz.asc 833 SHA256:5070e9428bd372a7fa1f66b395b81092bb40c98f9f56a2e2bc55c47fd387e901
'http://http.debian.net/debian/pool/main/c/coreutils/coreutils_9.7-3.debian.tar.xz' coreutils_9.7-3.debian.tar.xz 26820 SHA256:483f77876a080577f63da1d004cc1cf17d16df65d6925aefdd3294c6101eccfb
```

### `dpkg` source package: `curl=8.14.1-2`

Binary Packages:

- `libcurl4t64:amd64=8.14.1-2`

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
$ apt-get source -qq --print-uris curl=8.14.1-2
'http://http.debian.net/debian/pool/main/c/curl/curl_8.14.1-2.dsc' curl_8.14.1-2.dsc 3231 SHA256:71c691d6cb639a75279d2de44575773b5ce27af00bf6f9d7692e5f38568e33b6
'http://http.debian.net/debian/pool/main/c/curl/curl_8.14.1.orig.tar.gz' curl_8.14.1.orig.tar.gz 4250332 SHA256:6766ada7101d292b42b8b15681120acd68effa4a9660935853cf6d61f0d984d4
'http://http.debian.net/debian/pool/main/c/curl/curl_8.14.1.orig.tar.gz.asc' curl_8.14.1.orig.tar.gz.asc 488 SHA256:39cc2ec8ddc39d04e3e7101bbed46d858d0875cbb297a6bfa20959fa2bc7d5c7
'http://http.debian.net/debian/pool/main/c/curl/curl_8.14.1-2.debian.tar.xz' curl_8.14.1-2.debian.tar.xz 53264 SHA256:a092f75f452d610d516ec6619ecc355a4cc877afb212ab017c41e7d9c0fb1a1f
```

### `dpkg` source package: `cyrus-sasl2=2.1.28+dfsg1-9`

Binary Packages:

- `libsasl2-2:amd64=2.1.28+dfsg1-9`
- `libsasl2-modules-db:amd64=2.1.28+dfsg1-9`

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
$ apt-get source -qq --print-uris cyrus-sasl2=2.1.28+dfsg1-9
'http://http.debian.net/debian/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.28%2bdfsg1-9.dsc' cyrus-sasl2_2.1.28+dfsg1-9.dsc 3306 SHA256:179cda376ee9f9a54098f902174299dd183ae78c703f72b86bd4c3297db4c153
'http://http.debian.net/debian/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.28%2bdfsg1.orig.tar.xz' cyrus-sasl2_2.1.28+dfsg1.orig.tar.xz 794540 SHA256:e796a5d85d1a85e1b433d43504e467f9075c7ebc0b45730a3996cf11b1deada4
'http://http.debian.net/debian/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.28%2bdfsg1-9.debian.tar.xz' cyrus-sasl2_2.1.28+dfsg1-9.debian.tar.xz 99180 SHA256:8215afa01ee2907da0a650bfa6b9cf0fae12f2611a098eedd853b5e71adf6623
```

### `dpkg` source package: `dash=0.5.12-12`

Binary Packages:

- `dash=0.5.12-12`

Licenses: (parsed from: `/usr/share/doc/dash/copyright`)

- `BSD-3-Clause`
- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris dash=0.5.12-12
'http://http.debian.net/debian/pool/main/d/dash/dash_0.5.12-12.dsc' dash_0.5.12-12.dsc 1460 SHA256:589efc4d87a4ae4745c273bdb33198d7c4f28a71736a8ece81d3677cf9c6e5ce
'http://http.debian.net/debian/pool/main/d/dash/dash_0.5.12.orig.tar.gz' dash_0.5.12.orig.tar.gz 246054 SHA256:6a474ac46e8b0b32916c4c60df694c82058d3297d8b385b74508030ca4a8f28a
'http://http.debian.net/debian/pool/main/d/dash/dash_0.5.12-12.debian.tar.xz' dash_0.5.12-12.debian.tar.xz 47300 SHA256:a278acb5d9a1f5d9a086d36a547287cbf3105b8f33c0e62d86d264decf5ba1ad
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

### `dpkg` source package: `debconf=1.5.91`

Binary Packages:

- `debconf=1.5.91`

Licenses: (parsed from: `/usr/share/doc/debconf/copyright`)

- `BSD-2-clause`

Source:

```console
$ apt-get source -qq --print-uris debconf=1.5.91
'http://http.debian.net/debian/pool/main/d/debconf/debconf_1.5.91.dsc' debconf_1.5.91.dsc 2035 SHA256:1aa3ceaef24ef533cfffe7f9ca750c6325dbaea86a7abca77cb4439ceae930d8
'http://http.debian.net/debian/pool/main/d/debconf/debconf_1.5.91.tar.xz' debconf_1.5.91.tar.xz 609964 SHA256:18f3f43924ccc870be483d7c5f1a9be59e51ae1da403059d654666b5a175bf15
```

### `dpkg` source package: `debian-archive-keyring=2025.1`

Binary Packages:

- `debian-archive-keyring=2025.1`

Licenses: (parsed from: `/usr/share/doc/debian-archive-keyring/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris debian-archive-keyring=2025.1
'http://http.debian.net/debian/pool/main/d/debian-archive-keyring/debian-archive-keyring_2025.1.dsc' debian-archive-keyring_2025.1.dsc 1267 SHA256:09604bd8d4562a1e942e5d1a19a6b82447cbdeb2e7c7f0df7c32a2503647ea47
'http://http.debian.net/debian/pool/main/d/debian-archive-keyring/debian-archive-keyring_2025.1.tar.xz' debian-archive-keyring_2025.1.tar.xz 138248 SHA256:2d019c3fa19c42da4d37571e473c296286dad0214cb3bd5cafd99f04a8bf5471
```

### `dpkg` source package: `debianutils=5.23.1`

Binary Packages:

- `debianutils=5.23.1`

Licenses: (parsed from: `/usr/share/doc/debianutils/copyright`)

- `GPL-2`
- `GPL-2+`
- `SMAIL-GPL`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris debianutils=5.23.1
'http://http.debian.net/debian/pool/main/d/debianutils/debianutils_5.23.1.dsc' debianutils_5.23.1.dsc 1318 SHA256:0431d45c27aa5d60cdfa0ff300df4708e07c9f60a606afbeb20fb4c318c6eca5
'http://http.debian.net/debian/pool/main/d/debianutils/debianutils_5.23.1.tar.xz' debianutils_5.23.1.tar.xz 82152 SHA256:206c669cbf431da30904d4f9e69d049cb711714f5c137b66bf0b1f66d58710bc
```

### `dpkg` source package: `diffutils=1:3.10-4`

Binary Packages:

- `diffutils=1:3.10-4`

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
$ apt-get source -qq --print-uris diffutils=1:3.10-4
'http://http.debian.net/debian/pool/main/d/diffutils/diffutils_3.10-4.dsc' diffutils_3.10-4.dsc 1875 SHA256:087b414ddfc92161a30186926bc4b4ac02c7cba589b0323561cacd54c8b48392
'http://http.debian.net/debian/pool/main/d/diffutils/diffutils_3.10.orig.tar.xz' diffutils_3.10.orig.tar.xz 1624240 SHA256:90e5e93cc724e4ebe12ede80df1634063c7a855692685919bfe60b556c9bd09e
'http://http.debian.net/debian/pool/main/d/diffutils/diffutils_3.10.orig.tar.xz.asc' diffutils_3.10.orig.tar.xz.asc 833 SHA256:a94faf8f1baa04ff220f7b2ccb137c16337284e023ebc4a1d5df475c08d810f7
'http://http.debian.net/debian/pool/main/d/diffutils/diffutils_3.10-4.debian.tar.xz' diffutils_3.10-4.debian.tar.xz 14304 SHA256:8588b6ffb897ccff46c583e58ef50500b2511eee41949b21e8afa5439712c2c7
```

### `dpkg` source package: `dpkg=1.22.20`

Binary Packages:

- `dpkg=1.22.20`
- `dpkg-dev=1.22.20`
- `libdpkg-perl=1.22.20`

Licenses: (parsed from: `/usr/share/doc/dpkg/copyright`, `/usr/share/doc/dpkg-dev/copyright`, `/usr/share/doc/libdpkg-perl/copyright`)

- `GPL-2`
- `GPL-2+`
- `public-domain-s-s-d`

Source:

```console
$ apt-get source -qq --print-uris dpkg=1.22.20
'http://http.debian.net/debian/pool/main/d/dpkg/dpkg_1.22.20.dsc' dpkg_1.22.20.dsc 3449 SHA256:507420a03f1d2504c94af875be6f6fc5cb072bdacf41bbecdafe3cf6cd938846
'http://http.debian.net/debian/pool/main/d/dpkg/dpkg_1.22.20.tar.xz' dpkg_1.22.20.tar.xz 5741308 SHA256:f21bd89cca601500a7ecc446160be72413d822fe09b4ea155c9593b46321d5e4
```

### `dpkg` source package: `e2fsprogs=1.47.2-3`

Binary Packages:

- `libcom-err2:amd64=1.47.2-3+b1`

Licenses: (parsed from: `/usr/share/doc/libcom-err2/copyright`)

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
$ apt-get source -qq --print-uris e2fsprogs=1.47.2-3
'http://http.debian.net/debian/pool/main/e/e2fsprogs/e2fsprogs_1.47.2-3.dsc' e2fsprogs_1.47.2-3.dsc 3035 SHA256:860abb653ecbe01a11bb7e41c9e09a45e83847bffa585f7a3d3c0f9401c9d4bb
'http://http.debian.net/debian/pool/main/e/e2fsprogs/e2fsprogs_1.47.2.orig.tar.gz' e2fsprogs_1.47.2.orig.tar.gz 9996725 SHA256:6dcd67ff9d8b13274ba3f088e4318be4f5b71412cd863524423fc49d39a6371f
'http://http.debian.net/debian/pool/main/e/e2fsprogs/e2fsprogs_1.47.2.orig.tar.gz.asc' e2fsprogs_1.47.2.orig.tar.gz.asc 488 SHA256:2063f62a198dd3df21f789c990c2cf9b4a5de24ed55f0b78d86e97e98daffc9d
'http://http.debian.net/debian/pool/main/e/e2fsprogs/e2fsprogs_1.47.2-3.debian.tar.xz' e2fsprogs_1.47.2-3.debian.tar.xz 103684 SHA256:5517aae5ce5196e49fa314492f0639ad7a1692c9521d703b6c81acff77a1564e
```

### `dpkg` source package: `ed=1.21.1-1`

Binary Packages:

- `ed=1.21.1-1`

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
$ apt-get source -qq --print-uris ed=1.21.1-1
'http://http.debian.net/debian/pool/main/e/ed/ed_1.21.1-1.dsc' ed_1.21.1-1.dsc 1832 SHA256:c35f79215fc1039fb00379c9b63dafebf9f9c262b168a006ca657137dbfc41ca
'http://http.debian.net/debian/pool/main/e/ed/ed_1.21.1.orig.tar.gz' ed_1.21.1.orig.tar.gz 94252 SHA256:bb88a08496ffbaeca59bda93e5da195ef993522fb74f4fcfbf2619ff39f83b44
'http://http.debian.net/debian/pool/main/e/ed/ed_1.21.1-1.debian.tar.xz' ed_1.21.1-1.debian.tar.xz 8696 SHA256:ba8d3de70c1db8e50c978cf3b60beddf45b0c6c6931989865c20e550696d84ab
```

### `dpkg` source package: `expat=2.7.1-1`

Binary Packages:

- `libexpat1:amd64=2.7.1-1`

Licenses: (parsed from: `/usr/share/doc/libexpat1/copyright`)

- `MIT`

Source:

```console
$ apt-get source -qq --print-uris expat=2.7.1-1
'http://http.debian.net/debian/pool/main/e/expat/expat_2.7.1-1.dsc' expat_2.7.1-1.dsc 1964 SHA256:4ffb7f7a8adf961deaaec47654866eb965bafeda54bbf006fbad56d33c2d1290
'http://http.debian.net/debian/pool/main/e/expat/expat_2.7.1.orig.tar.gz' expat_2.7.1.orig.tar.gz 8433717 SHA256:85372797ff0673a8fc4a6be16466bb5a0ca28c0dcf3c6f7ac1686b4a3ba2aabb
'http://http.debian.net/debian/pool/main/e/expat/expat_2.7.1-1.debian.tar.xz' expat_2.7.1-1.debian.tar.xz 13204 SHA256:1c604a215810ed6598dcf49d87462a3b79c9d780aaf997ee1814b7afc1f25022
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

### `dpkg` source package: `fontconfig=2.15.0-2.3`

Binary Packages:

- `fontconfig=2.15.0-2.3`
- `fontconfig-config=2.15.0-2.3`
- `libfontconfig1:amd64=2.15.0-2.3`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris fontconfig=2.15.0-2.3
'http://http.debian.net/debian/pool/main/f/fontconfig/fontconfig_2.15.0-2.3.dsc' fontconfig_2.15.0-2.3.dsc 2673 SHA256:d5c3b910e470fdd00048813863f2e25e330c61b5cb3c795edf30cb3c52a657d0
'http://http.debian.net/debian/pool/main/f/fontconfig/fontconfig_2.15.0.orig.tar.xz' fontconfig_2.15.0.orig.tar.xz 1447820 SHA256:63a0658d0e06e0fa886106452b58ef04f21f58202ea02a94c39de0d3335d7c0e
'http://http.debian.net/debian/pool/main/f/fontconfig/fontconfig_2.15.0-2.3.debian.tar.xz' fontconfig_2.15.0-2.3.debian.tar.xz 59516 SHA256:af8e98e3801427f8957f86dc18303fcfbae329c0fab5bc06b5d5a0d26a53295f
```

### `dpkg` source package: `foreign=0.8.90-1`

Binary Packages:

- `r-cran-foreign=0.8.90-1`

Licenses: (parsed from: `/usr/share/doc/r-cran-foreign/copyright`)

- `GPL`
- `GPL `

Source:

```console
$ apt-get source -qq --print-uris foreign=0.8.90-1
'http://http.debian.net/debian/pool/main/f/foreign/foreign_0.8.90-1.dsc' foreign_0.8.90-1.dsc 1838 SHA256:0d566e1a8829fb9214d5904e64c63181a27b26acbd5f1aec362328afac3188bb
'http://http.debian.net/debian/pool/main/f/foreign/foreign_0.8.90.orig.tar.gz' foreign_0.8.90.orig.tar.gz 365447 SHA256:1dc6798002a50b9014227a2d20c0c2450fe6feb991a4a0b3bee36c0ee779a196
'http://http.debian.net/debian/pool/main/f/foreign/foreign_0.8.90-1.debian.tar.xz' foreign_0.8.90-1.debian.tar.xz 4424 SHA256:f203d8448d6fc3c970cd361b7ed3b87a8bc67be9891a53e6629827a08c54f215
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

### `dpkg` source package: `gcc-14=14.2.0-19`

Binary Packages:

- `cpp-14=14.2.0-19`
- `cpp-14-x86-64-linux-gnu=14.2.0-19`
- `g++-14=14.2.0-19`
- `g++-14-x86-64-linux-gnu=14.2.0-19`
- `gcc-14=14.2.0-19`
- `gcc-14-base:amd64=14.2.0-19`
- `gcc-14-x86-64-linux-gnu=14.2.0-19`
- `gfortran-14=14.2.0-19`
- `gfortran-14-x86-64-linux-gnu=14.2.0-19`
- `libasan8:amd64=14.2.0-19`
- `libatomic1:amd64=14.2.0-19`
- `libcc1-0:amd64=14.2.0-19`
- `libgcc-14-dev:amd64=14.2.0-19`
- `libgcc-s1:amd64=14.2.0-19`
- `libgfortran-14-dev:amd64=14.2.0-19`
- `libgfortran5:amd64=14.2.0-19`
- `libgomp1:amd64=14.2.0-19`
- `libhwasan0:amd64=14.2.0-19`
- `libitm1:amd64=14.2.0-19`
- `liblsan0:amd64=14.2.0-19`
- `libquadmath0:amd64=14.2.0-19`
- `libstdc++-14-dev:amd64=14.2.0-19`
- `libstdc++6:amd64=14.2.0-19`
- `libtsan2:amd64=14.2.0-19`
- `libubsan1:amd64=14.2.0-19`

Licenses: (parsed from: `/usr/share/doc/cpp-14/copyright`, `/usr/share/doc/cpp-14-x86-64-linux-gnu/copyright`, `/usr/share/doc/g++-14/copyright`, `/usr/share/doc/g++-14-x86-64-linux-gnu/copyright`, `/usr/share/doc/gcc-14/copyright`, `/usr/share/doc/gcc-14-base/copyright`, `/usr/share/doc/gcc-14-x86-64-linux-gnu/copyright`, `/usr/share/doc/gfortran-14/copyright`, `/usr/share/doc/gfortran-14-x86-64-linux-gnu/copyright`, `/usr/share/doc/libasan8/copyright`, `/usr/share/doc/libatomic1/copyright`, `/usr/share/doc/libcc1-0/copyright`, `/usr/share/doc/libgcc-14-dev/copyright`, `/usr/share/doc/libgcc-s1/copyright`, `/usr/share/doc/libgfortran-14-dev/copyright`, `/usr/share/doc/libgfortran5/copyright`, `/usr/share/doc/libgomp1/copyright`, `/usr/share/doc/libhwasan0/copyright`, `/usr/share/doc/libitm1/copyright`, `/usr/share/doc/liblsan0/copyright`, `/usr/share/doc/libquadmath0/copyright`, `/usr/share/doc/libstdc++-14-dev/copyright`, `/usr/share/doc/libstdc++6/copyright`, `/usr/share/doc/libtsan2/copyright`, `/usr/share/doc/libubsan1/copyright`)

- `Artistic`
- `GFDL-1.2`
- `GPL`
- `GPL-3`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris gcc-14=14.2.0-19
'http://http.debian.net/debian/pool/main/g/gcc-14/gcc-14_14.2.0-19.dsc' gcc-14_14.2.0-19.dsc 47347 SHA256:7db1e202cce66617e9134a662c877a3a773de5b612fd52179815877e0ecfb847
'http://http.debian.net/debian/pool/main/g/gcc-14/gcc-14_14.2.0.orig.tar.gz' gcc-14_14.2.0.orig.tar.gz 94299633 SHA256:e162a5ef3f0077ecae598c6556908d2ab80841532df3398072a96a6df6e6aa29
'http://http.debian.net/debian/pool/main/g/gcc-14/gcc-14_14.2.0-19.debian.tar.xz' gcc-14_14.2.0-19.debian.tar.xz 2577016 SHA256:31cbab4bafa48aa1c540497bd8098cbcf98e673778f927651ed944709f687781
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

### `dpkg` source package: `glib2.0=2.84.3-1`

Binary Packages:

- `libglib2.0-0t64:amd64=2.84.3-1`

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
$ apt-get source -qq --print-uris glib2.0=2.84.3-1
'http://http.debian.net/debian/pool/main/g/glib2.0/glib2.0_2.84.3-1.dsc' glib2.0_2.84.3-1.dsc 4924 SHA256:9114a7819e4009f4b23c05918ce62cedb305b08942dffbec1e08ff5c01ca21ce
'http://http.debian.net/debian/pool/main/g/glib2.0/glib2.0_2.84.3.orig-unicode-data.tar.xz' glib2.0_2.84.3.orig-unicode-data.tar.xz 660708 SHA256:c1742461e8c0e9673a3453a3127671169de9cb0138493e5c916f1b989530efcd
'http://http.debian.net/debian/pool/main/g/glib2.0/glib2.0_2.84.3.orig.tar.xz' glib2.0_2.84.3.orig.tar.xz 5615704 SHA256:aa4f87c3225bf57ca85f320888f7484901a17934ca37023c3bd8435a72db863e
'http://http.debian.net/debian/pool/main/g/glib2.0/glib2.0_2.84.3-1.debian.tar.xz' glib2.0_2.84.3-1.debian.tar.xz 138248 SHA256:b56895045df075b7fc358f412ef9fe3eeda3f80231b9cbb30b220fec1539f4bf
```

### `dpkg` source package: `glibc=2.41-9`

Binary Packages:

- `libc-bin=2.41-9`
- `libc-dev-bin=2.41-9`
- `libc-l10n=2.41-9`
- `libc6:amd64=2.41-9`
- `libc6-dev:amd64=2.41-9`
- `locales=2.41-9`

Licenses: (parsed from: `/usr/share/doc/libc-bin/copyright`, `/usr/share/doc/libc-dev-bin/copyright`, `/usr/share/doc/libc-l10n/copyright`, `/usr/share/doc/libc6/copyright`, `/usr/share/doc/libc6-dev/copyright`, `/usr/share/doc/locales/copyright`)

- `BSD-2-clause`
- `BSD-3-clause-Berkeley`
- `BSD-3-clause-Carnegie`
- `BSD-3-clause-Oracle`
- `BSD-3-clause-WIDE`
- `BSD-like-Spencer`
- `BSL-1.0`
- `CORE-MATH`
- `Carnegie`
- `DEC`
- `FSFAP`
- `GPL-2`
- `GPL-2+`
- `GPL-2+-with-link-exception`
- `GPL-3`
- `GPL-3+`
- `IBM`
- `ISC`
- `Inner-Net`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-2.1+-with-link-exception`
- `LGPL-3`
- `LGPL-3+`
- `MIT-like-Lord`
- `PCRE`
- `SunPro`
- `Unicode-DFS-2016`
- `Univ-Coimbra`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris glibc=2.41-9
'http://http.debian.net/debian/pool/main/g/glibc/glibc_2.41-9.dsc' glibc_2.41-9.dsc 7540 SHA256:9bb699c6780fc17a03014cdacfafd2cca8a9574c0452cc01668e8034532e2460
'http://http.debian.net/debian/pool/main/g/glibc/glibc_2.41.orig.tar.xz' glibc_2.41.orig.tar.xz 20323540 SHA256:f24aa441021121a79266f0d75242706cab8843a47901fefe74527491807f1998
'http://http.debian.net/debian/pool/main/g/glibc/glibc_2.41-9.debian.tar.xz' glibc_2.41-9.debian.tar.xz 433452 SHA256:afa8cbb8c71ab1fffafdbb5e7fa8227443cdc761a157a15b49b1d4592053ba83
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

### `dpkg` source package: `gnutls28=3.8.9-2`

Binary Packages:

- `libgnutls30t64:amd64=3.8.9-2`

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
$ apt-get source -qq --print-uris gnutls28=3.8.9-2
'http://http.debian.net/debian/pool/main/g/gnutls28/gnutls28_3.8.9-2.dsc' gnutls28_3.8.9-2.dsc 3236 SHA256:ee7571c280c896765fd3e5baa2f5b422a57b6227616120e95b7a79565d575cf0
'http://http.debian.net/debian/pool/main/g/gnutls28/gnutls28_3.8.9.orig.tar.xz' gnutls28_3.8.9.orig.tar.xz 6847364 SHA256:69e113d802d1670c4d5ac1b99040b1f2d5c7c05daec5003813c049b5184820ed
'http://http.debian.net/debian/pool/main/g/gnutls28/gnutls28_3.8.9.orig.tar.xz.asc' gnutls28_3.8.9.orig.tar.xz.asc 833 SHA256:7631d47762865d4ef494492cca794cf0fe6a8be892a4aa02f362ae29006d3054
'http://http.debian.net/debian/pool/main/g/gnutls28/gnutls28_3.8.9-2.debian.tar.xz' gnutls28_3.8.9-2.debian.tar.xz 78404 SHA256:69786eec12ca5559bdf3ccc47c18e93190149e83d92a3d2b79c9068ad101642e
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

### `dpkg` source package: `gzip=1.13-1`

Binary Packages:

- `gzip=1.13-1`

Licenses: (parsed from: `/usr/share/doc/gzip/copyright`)

- `FSF-manpages`
- `GFDL-1.3+-no-invariant`
- `GFDL-3`
- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris gzip=1.13-1
'http://http.debian.net/debian/pool/main/g/gzip/gzip_1.13-1.dsc' gzip_1.13-1.dsc 1884 SHA256:4942638dbb63dc5690e0a95ed70ee9f11e93565c43941c2485da3e561ec72028
'http://http.debian.net/debian/pool/main/g/gzip/gzip_1.13.orig.tar.xz' gzip_1.13.orig.tar.xz 838248 SHA256:7454eb6935db17c6655576c2e1b0fabefd38b4d0936e0f87f48cd062ce91a057
'http://http.debian.net/debian/pool/main/g/gzip/gzip_1.13.orig.tar.xz.asc' gzip_1.13.orig.tar.xz.asc 833 SHA256:aa752d6460fff2e0064857f1c6057d2dc49a28a45ad28c6b29c525851d6771f1
'http://http.debian.net/debian/pool/main/g/gzip/gzip_1.13-1.debian.tar.xz' gzip_1.13-1.debian.tar.xz 19028 SHA256:29319b3f91d8e03d940d4d7c0f2a5fe5ec4f2ba4a0e621c9ef2682f2d0240dd2
```

### `dpkg` source package: `harfbuzz=10.2.0-1`

Binary Packages:

- `libharfbuzz0b:amd64=10.2.0-1+b1`

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
$ apt-get source -qq --print-uris harfbuzz=10.2.0-1
'http://http.debian.net/debian/pool/main/h/harfbuzz/harfbuzz_10.2.0-1.dsc' harfbuzz_10.2.0-1.dsc 2564 SHA256:be25f4a4d1ca2032fbb51530649579fa843fa39c3f1941d1c644955e741f282d
'http://http.debian.net/debian/pool/main/h/harfbuzz/harfbuzz_10.2.0.orig.tar.xz' harfbuzz_10.2.0.orig.tar.xz 17957608 SHA256:620e3468faec2ea8685d32c46a58469b850ef63040b3565cde05959825b48227
'http://http.debian.net/debian/pool/main/h/harfbuzz/harfbuzz_10.2.0-1.debian.tar.xz' harfbuzz_10.2.0-1.debian.tar.xz 20108 SHA256:9bbdda73722f662b8a52c39a7d4d9ef6e024c0d4dd2cb41d825b066b6d170633
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

### `dpkg` source package: `icu=76.1-4`

Binary Packages:

- `icu-devtools=76.1-4`
- `libicu-dev:amd64=76.1-4`
- `libicu76:amd64=76.1-4`

Licenses: (parsed from: `/usr/share/doc/icu-devtools/copyright`, `/usr/share/doc/libicu-dev/copyright`, `/usr/share/doc/libicu76/copyright`)

- `GPL-3`
- `MIT`

Source:

```console
$ apt-get source -qq --print-uris icu=76.1-4
'http://http.debian.net/debian/pool/main/i/icu/icu_76.1-4.dsc' icu_76.1-4.dsc 2236 SHA256:2587ef23962b42a074ceab2f0407058f8e3fca0e6edd5d7c0bc1df6c683724a6
'http://http.debian.net/debian/pool/main/i/icu/icu_76.1.orig.tar.gz' icu_76.1.orig.tar.gz 27437767 SHA256:dfacb46bfe4747410472ce3e1144bf28a102feeaa4e3875bac9b4c6cf30f4f3e
'http://http.debian.net/debian/pool/main/i/icu/icu_76.1.orig.tar.gz.asc' icu_76.1.orig.tar.gz.asc 228 SHA256:6ef6ef96376eb6550f2b450e08b84c29238f60a77b89273f1521e1b57db73472
'http://http.debian.net/debian/pool/main/i/icu/icu_76.1-4.debian.tar.xz' icu_76.1-4.debian.tar.xz 65216 SHA256:5f9ff8b3a8e89a01b52c84bfebd35e7825ac561669d24e5a3d5f25d158e4f412
```

### `dpkg` source package: `init-system-helpers=1.68`

Binary Packages:

- `init-system-helpers=1.68`

Licenses: (parsed from: `/usr/share/doc/init-system-helpers/copyright`)

- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris init-system-helpers=1.68
'http://http.debian.net/debian/pool/main/i/init-system-helpers/init-system-helpers_1.68.dsc' init-system-helpers_1.68.dsc 2209 SHA256:58bf10802cf5d2496059368948a80d4a49f768d27b918fbe6dc28353c6cda72c
'http://http.debian.net/debian/pool/main/i/init-system-helpers/init-system-helpers_1.68.tar.xz' init-system-helpers_1.68.tar.xz 45168 SHA256:cdf1c7fe87362a4e3f7446a95b75c29ca6071fda3911adb269508203cd3c458d
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

### `dpkg` source package: `kernsmooth=2.23-26-1`

Binary Packages:

- `r-cran-kernsmooth=2.23-26-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris kernsmooth=2.23-26-1
'http://http.debian.net/debian/pool/main/k/kernsmooth/kernsmooth_2.23-26-1.dsc' kernsmooth_2.23-26-1.dsc 1891 SHA256:a9cc51d9ffeb82bd4989518d7448537dfeaa25b41e42347665dfdec5762dceb8
'http://http.debian.net/debian/pool/main/k/kernsmooth/kernsmooth_2.23-26.orig.tar.gz' kernsmooth_2.23-26.orig.tar.gz 27607 SHA256:b465bdac197f7faa787e625412ae03d1b7c2c134b1c924cfeb775faf9c4da73e
'http://http.debian.net/debian/pool/main/k/kernsmooth/kernsmooth_2.23-26-1.debian.tar.xz' kernsmooth_2.23-26-1.debian.tar.xz 3504 SHA256:d6ca5f4d034a59c6960042015350e6371d89ff8d9e68fe7758e47cc00561e71b
```

### `dpkg` source package: `keyutils=1.6.3-6`

Binary Packages:

- `libkeyutils1:amd64=1.6.3-6`

Licenses: (parsed from: `/usr/share/doc/libkeyutils1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2`
- `LGPL-2+`

Source:

```console
$ apt-get source -qq --print-uris keyutils=1.6.3-6
'http://http.debian.net/debian/pool/main/k/keyutils/keyutils_1.6.3-6.dsc' keyutils_1.6.3-6.dsc 2100 SHA256:e63869474c390d5d5bdee8492f7b2f4d6034ff10d8190da18593620c0f35fbf8
'http://http.debian.net/debian/pool/main/k/keyutils/keyutils_1.6.3.orig.tar.gz' keyutils_1.6.3.orig.tar.gz 137022 SHA256:a61d5706136ae4c05bd48f86186bcfdbd88dd8bd5107e3e195c924cfc1b39bb4
'http://http.debian.net/debian/pool/main/k/keyutils/keyutils_1.6.3-6.debian.tar.xz' keyutils_1.6.3-6.debian.tar.xz 16588 SHA256:6fc3c1217b8e92df9dff73e4919c45dff4ada5fd414ab57329af487f4476466a
```

### `dpkg` source package: `krb5=1.21.3-5`

Binary Packages:

- `libgssapi-krb5-2:amd64=1.21.3-5`
- `libk5crypto3:amd64=1.21.3-5`
- `libkrb5-3:amd64=1.21.3-5`
- `libkrb5support0:amd64=1.21.3-5`

Licenses: (parsed from: `/usr/share/doc/libgssapi-krb5-2/copyright`, `/usr/share/doc/libk5crypto3/copyright`, `/usr/share/doc/libkrb5-3/copyright`, `/usr/share/doc/libkrb5support0/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris krb5=1.21.3-5
'http://http.debian.net/debian/pool/main/k/krb5/krb5_1.21.3-5.dsc' krb5_1.21.3-5.dsc 3983 SHA256:88e736b6439d0fe30317ae7c38c3093b7139f1b7709997debe28d756f92de353
'http://http.debian.net/debian/pool/main/k/krb5/krb5_1.21.3.orig.tar.gz' krb5_1.21.3.orig.tar.gz 9136145 SHA256:b7a4cd5ead67fb08b980b21abd150ff7217e85ea320c9ed0c6dadd304840ad35
'http://http.debian.net/debian/pool/main/k/krb5/krb5_1.21.3.orig.tar.gz.asc' krb5_1.21.3.orig.tar.gz.asc 833 SHA256:85047c935fe949ef2e275885451b168557b923dd13a5aab0ef8fe6acd27b94d7
'http://http.debian.net/debian/pool/main/k/krb5/krb5_1.21.3-5.debian.tar.xz' krb5_1.21.3-5.debian.tar.xz 104424 SHA256:521fdfaf5cda93a64cc70afd357dc31ea6f4128ff5a489b036b58887eceddd46
```

### `dpkg` source package: `lapack=3.12.1-2`

Binary Packages:

- `libblas-dev:amd64=3.12.1-2`
- `libblas3:amd64=3.12.1-2`
- `liblapack-dev:amd64=3.12.1-2`
- `liblapack3:amd64=3.12.1-2`

Licenses: (parsed from: `/usr/share/doc/libblas-dev/copyright`, `/usr/share/doc/libblas3/copyright`, `/usr/share/doc/liblapack-dev/copyright`, `/usr/share/doc/liblapack3/copyright`)

- `BSD-3-clause`
- `BSD-3-clause-intel`

Source:

```console
$ apt-get source -qq --print-uris lapack=3.12.1-2
'http://http.debian.net/debian/pool/main/l/lapack/lapack_3.12.1-2.dsc' lapack_3.12.1-2.dsc 3352 SHA256:dc0ba2038289b24a16a72a6acdf134d650cd01580582cf7147c7858a3068a307
'http://http.debian.net/debian/pool/main/l/lapack/lapack_3.12.1.orig.tar.gz' lapack_3.12.1.orig.tar.gz 8067087 SHA256:2ca6407a001a474d4d4d35f3a61550156050c48016d949f0da0529c0aa052422
'http://http.debian.net/debian/pool/main/l/lapack/lapack_3.12.1-2.debian.tar.xz' lapack_3.12.1-2.debian.tar.xz 28420 SHA256:aa6d43273038ac9eca59930f1ac06ca920c3c8a66d25cc142a6d682d845c3fd9
```

### `dpkg` source package: `lattice=0.22-7-1`

Binary Packages:

- `r-cran-lattice=0.22-7-1`

Licenses: (parsed from: `/usr/share/doc/r-cran-lattice/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris lattice=0.22-7-1
'http://http.debian.net/debian/pool/main/l/lattice/lattice_0.22-7-1.dsc' lattice_0.22-7-1.dsc 1838 SHA256:65cab033d638165efe6b8998d9d70603f5c8ec7b339bc9b2e6ef99a4c296432d
'http://http.debian.net/debian/pool/main/l/lattice/lattice_0.22-7.orig.tar.gz' lattice_0.22-7.orig.tar.gz 598622 SHA256:400fa62b95e90410d52a36cee2ddeb025dd49695e55fe3db709fe60886bff9f7
'http://http.debian.net/debian/pool/main/l/lattice/lattice_0.22-7-1.debian.tar.xz' lattice_0.22-7-1.debian.tar.xz 5400 SHA256:6992ffd8f0603cfafae3983913627cf40ef6a8c8cc4291580aa5eb1598d1db13
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

### `dpkg` source package: `less=668-1`

Binary Packages:

- `less=668-1`

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
$ apt-get source -qq --print-uris less=668-1
'http://http.debian.net/debian/pool/main/l/less/less_668-1.dsc' less_668-1.dsc 1889 SHA256:84c63a051999d30deab36131d98345d4277105dadfd5d7c63ffea6a631f498f1
'http://http.debian.net/debian/pool/main/l/less/less_668.orig.tar.gz' less_668.orig.tar.gz 649770 SHA256:2819f55564d86d542abbecafd82ff61e819a3eec967faa36cd3e68f1596a44b8
'http://http.debian.net/debian/pool/main/l/less/less_668.orig.tar.gz.asc' less_668.orig.tar.gz.asc 195 SHA256:5b24942fb8e4352fc22ddff6ccaa61eb978d590fb3eecd26591f5cca8965ab03
'http://http.debian.net/debian/pool/main/l/less/less_668-1.debian.tar.xz' less_668-1.debian.tar.xz 22332 SHA256:83e659f43c11ee8591685744cd71e6b99e8cb430224649ac98557068d881e4ce
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

- `libcap-ng0:amd64=0.8.5-4+b1`

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

### `dpkg` source package: `libcap2=1:2.75-8`

Binary Packages:

- `libcap2:amd64=1:2.75-8`

Licenses: (parsed from: `/usr/share/doc/libcap2/copyright`)

- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris libcap2=1:2.75-8
'http://http.debian.net/debian/pool/main/libc/libcap2/libcap2_2.75-8.dsc' libcap2_2.75-8.dsc 2678 SHA256:c6d522981e8cbcbaffbe65862ddd1ce4b2a843204e97c515ad62b5dd0ded160c
'http://http.debian.net/debian/pool/main/libc/libcap2/libcap2_2.75.orig.tar.xz' libcap2_2.75.orig.tar.xz 197868 SHA256:de4e7e064c9ba451d5234dd46e897d7c71c96a9ebf9a0c445bc04f4742d83632
'http://http.debian.net/debian/pool/main/libc/libcap2/libcap2_2.75.orig.tar.xz.asc' libcap2_2.75.orig.tar.xz.asc 833 SHA256:c71b593e7c3160fd7f406641074d93462bbc4906c9243937a0e232f42d5c54d2
'http://http.debian.net/debian/pool/main/libc/libcap2/libcap2_2.75-8.debian.tar.xz' libcap2_2.75-8.debian.tar.xz 22696 SHA256:be1526f049478095e06a011d28c8375ee936b12248dd546658ed3477a75e9049
```

### `dpkg` source package: `libdatrie=0.2.13-4`

Binary Packages:

- `libdatrie1:amd64=0.2.13-4`

Licenses: (parsed from: `/usr/share/doc/libdatrie1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris libdatrie=0.2.13-4
'http://http.debian.net/debian/pool/main/libd/libdatrie/libdatrie_0.2.13-4.dsc' libdatrie_0.2.13-4.dsc 2239 SHA256:ad895c68efd7a51b9df6e8857ddc2153d637cf68a424ef03fcdddd2e2f06c111
'http://http.debian.net/debian/pool/main/libd/libdatrie/libdatrie_0.2.13.orig.tar.xz' libdatrie_0.2.13.orig.tar.xz 314072 SHA256:12231bb2be2581a7f0fb9904092d24b0ed2a271a16835071ed97bed65267f4be
'http://http.debian.net/debian/pool/main/libd/libdatrie/libdatrie_0.2.13-4.debian.tar.xz' libdatrie_0.2.13-4.debian.tar.xz 10068 SHA256:25de18a063f716c352c0906e36357e46b9d24c24a4825ab5a0c453ac4e2e1ca9
```

### `dpkg` source package: `libdeflate=1.23-2`

Binary Packages:

- `libdeflate-dev:amd64=1.23-2`
- `libdeflate0:amd64=1.23-2`

Licenses: (parsed from: `/usr/share/doc/libdeflate-dev/copyright`, `/usr/share/doc/libdeflate0/copyright`)

- `Expat`

Source:

```console
$ apt-get source -qq --print-uris libdeflate=1.23-2
'http://http.debian.net/debian/pool/main/libd/libdeflate/libdeflate_1.23-2.dsc' libdeflate_1.23-2.dsc 1743 SHA256:fbec7154ffff5193ef71c196e1e7348a154b1ed35c2a9ce3ece5fcc947303d77
'http://http.debian.net/debian/pool/main/libd/libdeflate/libdeflate_1.23.orig.tar.gz' libdeflate_1.23.orig.tar.gz 197519 SHA256:1ab18349b9fb0ce8a0ca4116bded725be7dcbfa709e19f6f983d99df1fb8b25f
'http://http.debian.net/debian/pool/main/libd/libdeflate/libdeflate_1.23-2.debian.tar.xz' libdeflate_1.23-2.debian.tar.xz 5624 SHA256:6d3101de26f30c25e4900fecc3b6da34543771d6014767af29850bc3ff3cbd09
```

### `dpkg` source package: `libffi=3.4.8-2`

Binary Packages:

- `libffi8:amd64=3.4.8-2`

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
$ apt-get source -qq --print-uris libffi=3.4.8-2
'http://http.debian.net/debian/pool/main/libf/libffi/libffi_3.4.8-2.dsc' libffi_3.4.8-2.dsc 1948 SHA256:4424defe3f37c0084f062e03330b2ba3d3f927367c33be455cfacf7f85a78161
'http://http.debian.net/debian/pool/main/libf/libffi/libffi_3.4.8.orig.tar.gz' libffi_3.4.8.orig.tar.gz 595051 SHA256:cbb7f0b3b095dc506387ec1e35b891bfb4891d05b90a495bc69a10f2293f80ff
'http://http.debian.net/debian/pool/main/libf/libffi/libffi_3.4.8-2.debian.tar.xz' libffi_3.4.8-2.debian.tar.xz 11220 SHA256:f23ac79a19895ebb6bbb539263d0d945ebc2d3e91217a597f5819777f08b401c
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

### `dpkg` source package: `libidn2=2.3.8-2`

Binary Packages:

- `libidn2-0:amd64=2.3.8-2`

Licenses: (parsed from: `/usr/share/doc/libidn2-0/copyright`)

- `Expat`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `LGPL-3`
- `LGPL-3+`
- `Unicode`

Source:

```console
$ apt-get source -qq --print-uris libidn2=2.3.8-2
'http://http.debian.net/debian/pool/main/libi/libidn2/libidn2_2.3.8-2.dsc' libidn2_2.3.8-2.dsc 2961 SHA256:af3327227dbbf12fff281f71b7feb90371d2dbe597f3129e38b93c3faadcea61
'http://http.debian.net/debian/pool/main/libi/libidn2/libidn2_2.3.8.orig.tar.gz' libidn2_2.3.8.orig.tar.gz 718637 SHA256:bbad1678d35d28e2c62e6a2577083829461402d9e47b908791c55314a5cb5e04
'http://http.debian.net/debian/pool/main/libi/libidn2/libidn2_2.3.8.orig.tar.gz.asc' libidn2_2.3.8.orig.tar.gz.asc 1223 SHA256:8995cab7db361d9d6989eab26d9b521c74236960a5d78250121c8d369b013bd8
'http://http.debian.net/debian/pool/main/libi/libidn2/libidn2_2.3.8-2.debian.tar.xz' libidn2_2.3.8-2.debian.tar.xz 17532 SHA256:ab95c2bab110557505ba437bc162f67a5a85fa9d8a2e55501245dc7f0fe2e412
```

### `dpkg` source package: `libjpeg-turbo=1:2.1.5-4`

Binary Packages:

- `libjpeg-dev:amd64=1:2.1.5-4`
- `libjpeg62-turbo:amd64=1:2.1.5-4`
- `libjpeg62-turbo-dev:amd64=1:2.1.5-4`

Licenses: (parsed from: `/usr/share/doc/libjpeg-dev/copyright`, `/usr/share/doc/libjpeg62-turbo/copyright`, `/usr/share/doc/libjpeg62-turbo-dev/copyright`)

- `BSD-3-clause`
- `BSD-BY-LC-NE`
- `Expat`
- `NTP`
- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris libjpeg-turbo=1:2.1.5-4
'http://http.debian.net/debian/pool/main/libj/libjpeg-turbo/libjpeg-turbo_2.1.5-4.dsc' libjpeg-turbo_2.1.5-4.dsc 2508 SHA256:26cbf22aa3b3e327df072513f14a5ddfb4a7b9a3d78c46a5dccfd711c13ac743
'http://http.debian.net/debian/pool/main/libj/libjpeg-turbo/libjpeg-turbo_2.1.5.orig.tar.gz' libjpeg-turbo_2.1.5.orig.tar.gz 2264471 SHA256:254f3642b04e309fee775123133c6464181addc150499561020312ec61c1bf7c
'http://http.debian.net/debian/pool/main/libj/libjpeg-turbo/libjpeg-turbo_2.1.5-4.debian.tar.xz' libjpeg-turbo_2.1.5-4.debian.tar.xz 108128 SHA256:739e7dc22904dccdc5ab105de57a6e4c1515c0e841e68226e6410ff4976e0e91
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

- `libpaper-utils=2.2.5-0.3+b2`
- `libpaper2:amd64=2.2.5-0.3+b2`

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

### `dpkg` source package: `libpng1.6=1.6.48-1`

Binary Packages:

- `libpng-dev:amd64=1.6.48-1`
- `libpng16-16t64:amd64=1.6.48-1`

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
$ apt-get source -qq --print-uris libpng1.6=1.6.48-1
'http://http.debian.net/debian/pool/main/libp/libpng1.6/libpng1.6_1.6.48-1.dsc' libpng1.6_1.6.48-1.dsc 2254 SHA256:dd8742533bd0201d64c94e019460ddf28141f369fc78f52c19028d58530f87f0
'http://http.debian.net/debian/pool/main/libp/libpng1.6/libpng1.6_1.6.48.orig.tar.gz' libpng1.6_1.6.48.orig.tar.gz 1572923 SHA256:b17e99026055727e8cba99160c3a9a7f9af788e9f786daeadded5a42243f1dd0
'http://http.debian.net/debian/pool/main/libp/libpng1.6/libpng1.6_1.6.48-1.debian.tar.xz' libpng1.6_1.6.48-1.debian.tar.xz 33240 SHA256:647c6b09cdb628200e2213b75f6ab3fe0a4fe18f21fe78c6821ecb15e154e7d2
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

### `dpkg` source package: `libseccomp=2.6.0-2`

Binary Packages:

- `libseccomp2:amd64=2.6.0-2`

Licenses: (parsed from: `/usr/share/doc/libseccomp2/copyright`)

- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libseccomp=2.6.0-2
'http://http.debian.net/debian/pool/main/libs/libseccomp/libseccomp_2.6.0-2.dsc' libseccomp_2.6.0-2.dsc 2622 SHA256:d05f94536558d34fa339326c6f958a3357b51efac8234470b5d97b69472db765
'http://http.debian.net/debian/pool/main/libs/libseccomp/libseccomp_2.6.0.orig.tar.gz' libseccomp_2.6.0.orig.tar.gz 685655 SHA256:83b6085232d1588c379dc9b9cae47bb37407cf262e6e74993c61ba72d2a784dc
'http://http.debian.net/debian/pool/main/libs/libseccomp/libseccomp_2.6.0.orig.tar.gz.asc' libseccomp_2.6.0.orig.tar.gz.asc 833 SHA256:52e338fa958128293cbd25d2be189e34da41c4f4abbb1b641cf58f373c001f94
'http://http.debian.net/debian/pool/main/libs/libseccomp/libseccomp_2.6.0-2.debian.tar.xz' libseccomp_2.6.0-2.debian.tar.xz 20800 SHA256:ed705ec85719403e77d004c99c0b06b795f090c66fcae265c4bcf37ffea9cc27
```

### `dpkg` source package: `libselinux=3.8.1-1`

Binary Packages:

- `libselinux1:amd64=3.8.1-1`

Licenses: (parsed from: `/usr/share/doc/libselinux1/copyright`)

- `GPL-2`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris libselinux=3.8.1-1
'http://http.debian.net/debian/pool/main/libs/libselinux/libselinux_3.8.1-1.dsc' libselinux_3.8.1-1.dsc 3013 SHA256:e430b782a396e266f86c32fa779efadebfd40e6a0d10ddbd786fc47905f723b9
'http://http.debian.net/debian/pool/main/libs/libselinux/libselinux_3.8.1.orig.tar.gz' libselinux_3.8.1.orig.tar.gz 204411 SHA256:ec2d2789f931152d21c1db1eb4bc202ce4eccede34d9be9e360e3b45243cee2c
'http://http.debian.net/debian/pool/main/libs/libselinux/libselinux_3.8.1.orig.tar.gz.asc' libselinux_3.8.1.orig.tar.gz.asc 833 SHA256:7f983714a780d89f7677e7ba140ce29974022b8ba225f60246b6c33de1477dd6
'http://http.debian.net/debian/pool/main/libs/libselinux/libselinux_3.8.1-1.debian.tar.xz' libselinux_3.8.1-1.debian.tar.xz 37812 SHA256:1af25952374f083cf3d6d0edd5beb938f2e53c30eb404afa1e32fcd1cb127db7
```

### `dpkg` source package: `libsemanage=3.8.1-1`

Binary Packages:

- `libsemanage-common=3.8.1-1`
- `libsemanage2:amd64=3.8.1-1`

Licenses: (parsed from: `/usr/share/doc/libsemanage-common/copyright`, `/usr/share/doc/libsemanage2/copyright`)

- `GPL-2`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris libsemanage=3.8.1-1
'http://http.debian.net/debian/pool/main/libs/libsemanage/libsemanage_3.8.1-1.dsc' libsemanage_3.8.1-1.dsc 2992 SHA256:b22bfc4ab2cd47fac46cc9e45d418bb30eb540c3e5c1052d6c669f53e180e4e5
'http://http.debian.net/debian/pool/main/libs/libsemanage/libsemanage_3.8.1.orig.tar.gz' libsemanage_3.8.1.orig.tar.gz 184618 SHA256:7b39127b219cc70bfd935a4af6b0f2ba83d4b35c916f253c7e942c23ab490f07
'http://http.debian.net/debian/pool/main/libs/libsemanage/libsemanage_3.8.1.orig.tar.gz.asc' libsemanage_3.8.1.orig.tar.gz.asc 833 SHA256:5b4856cb5823fba1b247ff1b5355692706da68a4df61a936d1b33b1f9e9b2f3d
'http://http.debian.net/debian/pool/main/libs/libsemanage/libsemanage_3.8.1-1.debian.tar.xz' libsemanage_3.8.1-1.debian.tar.xz 37572 SHA256:6d1e5bd4d06bbd25ced1b75fba394c3e2157bd604cf1cd33fb581793d70bd7b8
```

### `dpkg` source package: `libsepol=3.8.1-1`

Binary Packages:

- `libsepol2:amd64=3.8.1-1`

Licenses: (parsed from: `/usr/share/doc/libsepol2/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris libsepol=3.8.1-1
'http://http.debian.net/debian/pool/main/libs/libsepol/libsepol_3.8.1-1.dsc' libsepol_3.8.1-1.dsc 2347 SHA256:0351ffc8c3f66918c9e4ecae9244ae2af27857d8795e424e384ddda794718c34
'http://http.debian.net/debian/pool/main/libs/libsepol/libsepol_3.8.1.orig.tar.gz' libsepol_3.8.1.orig.tar.gz 513830 SHA256:0e78705305f955abd4c0654d37a5477ee26349ab74db9e2b03a7868897ae1ddf
'http://http.debian.net/debian/pool/main/libs/libsepol/libsepol_3.8.1.orig.tar.gz.asc' libsepol_3.8.1.orig.tar.gz.asc 833 SHA256:183f6cf96054986704d4224f89518e9139370385c43a533078f45ca688dca8b6
'http://http.debian.net/debian/pool/main/libs/libsepol/libsepol_3.8.1-1.debian.tar.xz' libsepol_3.8.1-1.debian.tar.xz 21432 SHA256:7aac515a941f8dd19581b16c664b3098962e6a8ed7fa0afdafd306a85c667619
```

### `dpkg` source package: `libsm=2:1.2.6-1`

Binary Packages:

- `libsm6:amd64=2:1.2.6-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libsm=2:1.2.6-1
'http://http.debian.net/debian/pool/main/libs/libsm/libsm_1.2.6-1.dsc' libsm_1.2.6-1.dsc 2302 SHA256:d0ab34a54b145ea728242638b878d05f84bcb71feabf075c5e9510cc608aab93
'http://http.debian.net/debian/pool/main/libs/libsm/libsm_1.2.6.orig.tar.gz' libsm_1.2.6.orig.tar.gz 467497 SHA256:166b4b50d606cdd83f1ddc61b5b9162600034f848b3e32ccbb0e63536b7d6cdd
'http://http.debian.net/debian/pool/main/libs/libsm/libsm_1.2.6.orig.tar.gz.asc' libsm_1.2.6.orig.tar.gz.asc 833 SHA256:b5e59abae8a79ae9901e73178dacf5af9d7c3b91704fd86de85d305fd7a17a7f
'http://http.debian.net/debian/pool/main/libs/libsm/libsm_1.2.6-1.diff.gz' libsm_1.2.6-1.diff.gz 13291 SHA256:7cc1d915c18fa6c34cc57c44ca844b62e99fba79b70c0941466d3747e15f2195
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

### `dpkg` source package: `libtasn1-6=4.20.0-2`

Binary Packages:

- `libtasn1-6:amd64=4.20.0-2`

Licenses: (parsed from: `/usr/share/doc/libtasn1-6/copyright`)

- `GFDL-1.3`
- `GPL-3`
- `LGPL`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libtasn1-6=4.20.0-2
'http://http.debian.net/debian/pool/main/libt/libtasn1-6/libtasn1-6_4.20.0-2.dsc' libtasn1-6_4.20.0-2.dsc 2665 SHA256:54800d16bf3c7eaf675356f2e9d30226991710d78717219bb6425dcc453a55a2
'http://http.debian.net/debian/pool/main/libt/libtasn1-6/libtasn1-6_4.20.0.orig.tar.gz' libtasn1-6_4.20.0.orig.tar.gz 1783873 SHA256:92e0e3bd4c02d4aeee76036b2ddd83f0c732ba4cda5cb71d583272b23587a76c
'http://http.debian.net/debian/pool/main/libt/libtasn1-6/libtasn1-6_4.20.0.orig.tar.gz.asc' libtasn1-6_4.20.0.orig.tar.gz.asc 1223 SHA256:0faa628b6a3e4bb84ca5f00f127c6dfa1fc96a7ad88030dd7aa048753cf4b201
'http://http.debian.net/debian/pool/main/libt/libtasn1-6/libtasn1-6_4.20.0-2.debian.tar.xz' libtasn1-6_4.20.0-2.debian.tar.xz 18640 SHA256:d9d911708f4863437b88eeff7f779d39f6b77613dc2851c64db2bd8160a07c30
```

### `dpkg` source package: `libtext-charwidth-perl=0.04-11`

Binary Packages:

- `libtext-charwidth-perl:amd64=0.04-11+b4`

Licenses: (parsed from: `/usr/share/doc/libtext-charwidth-perl/copyright`)

- `Artistic`
- `GPL-1+`

Source:

```console
$ apt-get source -qq --print-uris libtext-charwidth-perl=0.04-11
'http://http.debian.net/debian/pool/main/libt/libtext-charwidth-perl/libtext-charwidth-perl_0.04-11.dsc' libtext-charwidth-perl_0.04-11.dsc 2162 SHA256:8a4f6e7a44880f8b4dd8f3dc0c97a39c6fef979f99899de4962c9ccfe84a2577
'http://http.debian.net/debian/pool/main/libt/libtext-charwidth-perl/libtext-charwidth-perl_0.04.orig.tar.bz2' libtext-charwidth-perl_0.04.orig.tar.bz2 8327 SHA256:2990c13c3f4a5479d7dbc5a94b86c23798cf0dc7df54ffe54e065f072558b6ed
'http://http.debian.net/debian/pool/main/libt/libtext-charwidth-perl/libtext-charwidth-perl_0.04-11.debian.tar.xz' libtext-charwidth-perl_0.04-11.debian.tar.xz 3016 SHA256:2590d0b6ee7b9cea5396debb96190077210874b4847e844f9eb0d8a4d87ba19c
```

### `dpkg` source package: `libtext-wrapi18n-perl=0.06-10`

Binary Packages:

- `libtext-wrapi18n-perl=0.06-10`

Licenses: (parsed from: `/usr/share/doc/libtext-wrapi18n-perl/copyright`)

- `Artistic`
- `GPL-1`
- `GPL-1+`

Source:

```console
$ apt-get source -qq --print-uris libtext-wrapi18n-perl=0.06-10
'http://http.debian.net/debian/pool/main/libt/libtext-wrapi18n-perl/libtext-wrapi18n-perl_0.06-10.dsc' libtext-wrapi18n-perl_0.06-10.dsc 1829 SHA256:726c08c23af488c28b70600a5c1632468f1535cb50dcd5255cc153a4f8558ed9
'http://http.debian.net/debian/pool/main/libt/libtext-wrapi18n-perl/libtext-wrapi18n-perl_0.06.orig.tar.gz' libtext-wrapi18n-perl_0.06.orig.tar.gz 3797 SHA256:432c2a801efe9f12d631124c1163439eac4c99449ba13d80133c45ecacc627f5
'http://http.debian.net/debian/pool/main/libt/libtext-wrapi18n-perl/libtext-wrapi18n-perl_0.06-10.debian.tar.xz' libtext-wrapi18n-perl_0.06-10.debian.tar.xz 3452 SHA256:751073476ee62cc3430ff0afcab74a4e02b432199d7612e1fd63105fc89ec378
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

### `dpkg` source package: `libtirpc=1.3.6+ds-1`

Binary Packages:

- `libtirpc-common=1.3.6+ds-1`
- `libtirpc-dev:amd64=1.3.6+ds-1`
- `libtirpc3t64:amd64=1.3.6+ds-1`

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
$ apt-get source -qq --print-uris libtirpc=1.3.6+ds-1
'http://http.debian.net/debian/pool/main/libt/libtirpc/libtirpc_1.3.6%2bds-1.dsc' libtirpc_1.3.6+ds-1.dsc 2154 SHA256:737f9f15b21f8ea4226a2aa8c18c956e69e6eb3546c4c8ec9f5194380e2cd4e6
'http://http.debian.net/debian/pool/main/libt/libtirpc/libtirpc_1.3.6%2bds.orig.tar.gz' libtirpc_1.3.6+ds.orig.tar.gz 704513 SHA256:f9eeeb368d733e11f18ddb750a41bdf9089ba5f9476404da848c2cd295624f0d
'http://http.debian.net/debian/pool/main/libt/libtirpc/libtirpc_1.3.6%2bds-1.debian.tar.xz' libtirpc_1.3.6+ds-1.debian.tar.xz 11924 SHA256:3aecc6669961a233b6adda8a1d2136777b68dcf64c61dd6986262199b2e5b95b
```

### `dpkg` source package: `libunistring=1.3-2`

Binary Packages:

- `libunistring5:amd64=1.3-2`

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
$ apt-get source -qq --print-uris libunistring=1.3-2
'http://http.debian.net/debian/pool/main/libu/libunistring/libunistring_1.3-2.dsc' libunistring_1.3-2.dsc 2215 SHA256:0c09938cace7fbbf36c73af8bc2243fd2f70d3fe336539e8d4c10d0e61742571
'http://http.debian.net/debian/pool/main/libu/libunistring/libunistring_1.3.orig.tar.xz' libunistring_1.3.orig.tar.xz 2753448 SHA256:f245786c831d25150f3dfb4317cda1acc5e3f79a5da4ad073ddca58886569527
'http://http.debian.net/debian/pool/main/libu/libunistring/libunistring_1.3.orig.tar.xz.asc' libunistring_1.3.orig.tar.xz.asc 833 SHA256:62201b5b7ce9c0b033c50cefa5d7769dff4b7cee8205572e0cf917653cae9e33
'http://http.debian.net/debian/pool/main/libu/libunistring/libunistring_1.3-2.debian.tar.xz' libunistring_1.3-2.debian.tar.xz 28480 SHA256:feaf9761d365430178ea46feefeb602b435c21acf5924918e2257238e0378fc9
```

### `dpkg` source package: `libwebp=1.5.0-0.1`

Binary Packages:

- `libsharpyuv0:amd64=1.5.0-0.1`
- `libwebp7:amd64=1.5.0-0.1`

Licenses: (parsed from: `/usr/share/doc/libsharpyuv0/copyright`, `/usr/share/doc/libwebp7/copyright`)

- `Apache-2.0`
- `BSD-3-Clause`

Source:

```console
$ apt-get source -qq --print-uris libwebp=1.5.0-0.1
'http://http.debian.net/debian/pool/main/libw/libwebp/libwebp_1.5.0-0.1.dsc' libwebp_1.5.0-0.1.dsc 2865 SHA256:2e7be6f202ebfaac738278bebc10b151768aef60857e63734018ced4d59b9c9a
'http://http.debian.net/debian/pool/main/libw/libwebp/libwebp_1.5.0.orig.tar.gz' libwebp_1.5.0.orig.tar.gz 4267494 SHA256:7d6fab70cf844bf6769077bd5d7a74893f8ffd4dfb42861745750c63c2a5c92c
'http://http.debian.net/debian/pool/main/libw/libwebp/libwebp_1.5.0.orig.tar.gz.asc' libwebp_1.5.0.orig.tar.gz.asc 833 SHA256:1383ff0b093f57d65f5a902e1bc51c550795ce4713b38712c60bb9151e15dcd6
'http://http.debian.net/debian/pool/main/libw/libwebp/libwebp_1.5.0-0.1.debian.tar.xz' libwebp_1.5.0-0.1.debian.tar.xz 11284 SHA256:0dc0e727dc5f5e04ddd41b482f964626e92658099981b57ddd156b530ae01826
```

### `dpkg` source package: `libx11=2:1.8.12-1`

Binary Packages:

- `libx11-6:amd64=2:1.8.12-1`
- `libx11-data=2:1.8.12-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libx11=2:1.8.12-1
'http://http.debian.net/debian/pool/main/libx/libx11/libx11_1.8.12-1.dsc' libx11_1.8.12-1.dsc 2490 SHA256:745fb04a4b0f8942183f6ac84ebd9e2dae1416c37f90abeaacabb57dc11286f5
'http://http.debian.net/debian/pool/main/libx/libx11/libx11_1.8.12.orig.tar.gz' libx11_1.8.12.orig.tar.gz 3215077 SHA256:220fbcf54b6e4d8dc40076ff4ab87954358019982490b33c7802190b62d89ce1
'http://http.debian.net/debian/pool/main/libx/libx11/libx11_1.8.12.orig.tar.gz.asc' libx11_1.8.12.orig.tar.gz.asc 833 SHA256:c3d177c8efcef9d3a1963956de0edc56ef2dd63d13dc39d3d7473dc9011fca65
'http://http.debian.net/debian/pool/main/libx/libx11/libx11_1.8.12-1.diff.gz' libx11_1.8.12-1.diff.gz 74466 SHA256:2231b0ec8ce2eb380256b67eb30c05d90b0e92d75dd583c24e0bf640b3078977
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

### `dpkg` source package: `libxcrypt=1:4.4.38-1`

Binary Packages:

- `libcrypt-dev:amd64=1:4.4.38-1`
- `libcrypt1:amd64=1:4.4.38-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxcrypt=1:4.4.38-1
'http://http.debian.net/debian/pool/main/libx/libxcrypt/libxcrypt_4.4.38-1.dsc' libxcrypt_4.4.38-1.dsc 1573 SHA256:feba1874a84616791c1c17f9a290c9e97562b2904b3b0200edc82a2db54f3f07
'http://http.debian.net/debian/pool/main/libx/libxcrypt/libxcrypt_4.4.38.orig.tar.xz' libxcrypt_4.4.38.orig.tar.xz 394216 SHA256:6a275a356622c64ba9f693892215dbb399c003a7a4afeed9c4c74070eaab20f4
'http://http.debian.net/debian/pool/main/libx/libxcrypt/libxcrypt_4.4.38-1.debian.tar.xz' libxcrypt_4.4.38-1.debian.tar.xz 8512 SHA256:6b87bcb5325e417ab3f4c01c364233444b4c9008a69ec1d6fababb3f6e693a5e
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

- `libxext6:amd64=2:1.3.4-1+b3`

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

- `libxmuu1:amd64=2:1.1.3-3+b4`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxmu=2:1.1.3-3
'http://http.debian.net/debian/pool/main/libx/libxmu/libxmu_1.1.3-3.dsc' libxmu_1.1.3-3.dsc 2165 SHA256:d9dfadd0a6be92f88b1151c695e5799f889a39047176f80a91fcba24333cd063
'http://http.debian.net/debian/pool/main/libx/libxmu/libxmu_1.1.3.orig.tar.gz' libxmu_1.1.3.orig.tar.gz 497343 SHA256:5bd9d4ed1ceaac9ea023d86bf1c1632cd3b172dce4a193a72a94e1d9df87a62e
'http://http.debian.net/debian/pool/main/libx/libxmu/libxmu_1.1.3-3.diff.gz' libxmu_1.1.3-3.diff.gz 8085 SHA256:6f599ddd7951a1db5c1899fcd2a7c0289ae4ec9f9a783bc5e5b209b83c7ea12d
```

### `dpkg` source package: `libxrender=1:0.9.12-1`

Binary Packages:

- `libxrender1:amd64=1:0.9.12-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxrender=1:0.9.12-1
'http://http.debian.net/debian/pool/main/libx/libxrender/libxrender_0.9.12-1.dsc' libxrender_0.9.12-1.dsc 2258 SHA256:2980c127d296455f4e9bcaf5ba114284fa0735ce3ef5b613dbe99d854bc87ca3
'http://http.debian.net/debian/pool/main/libx/libxrender/libxrender_0.9.12.orig.tar.gz' libxrender_0.9.12.orig.tar.gz 450034 SHA256:0fff64125819c02d1102b6236f3d7d861a07b5216d8eea336c3811d31494ecf7
'http://http.debian.net/debian/pool/main/libx/libxrender/libxrender_0.9.12.orig.tar.gz.asc' libxrender_0.9.12.orig.tar.gz.asc 833 SHA256:0bbd310ac3974ef398cf4d8a4b362b0b4d60ceb43e6eba393c3cc740b03816fc
'http://http.debian.net/debian/pool/main/libx/libxrender/libxrender_0.9.12-1.diff.gz' libxrender_0.9.12-1.diff.gz 21464 SHA256:c0d3e91a3aa474772c242dcbb997504dff4c28e177d9b7fbb70c50ce7bf56fc5
```

### `dpkg` source package: `libxss=1:1.2.3-1`

Binary Packages:

- `libxss1:amd64=1:1.2.3-1+b3`

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

- `libxt6t64:amd64=1:1.2.1-1.2+b2`

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

### `dpkg` source package: `libzstd=1.5.7+dfsg-1`

Binary Packages:

- `libzstd-dev:amd64=1.5.7+dfsg-1`
- `libzstd1:amd64=1.5.7+dfsg-1`

Licenses: (parsed from: `/usr/share/doc/libzstd-dev/copyright`, `/usr/share/doc/libzstd1/copyright`)

- `BSD-3-clause`
- `Expat`
- `GPL-2`
- `zlib`

Source:

```console
$ apt-get source -qq --print-uris libzstd=1.5.7+dfsg-1
'http://http.debian.net/debian/pool/main/libz/libzstd/libzstd_1.5.7%2bdfsg-1.dsc' libzstd_1.5.7+dfsg-1.dsc 2371 SHA256:8f6ab97fa772d921334e50fa5756a0951e23c718dc913e43a228f28c1a23adf9
'http://http.debian.net/debian/pool/main/libz/libzstd/libzstd_1.5.7%2bdfsg.orig.tar.xz' libzstd_1.5.7+dfsg.orig.tar.xz 1834780 SHA256:0c092ef267edce57ba7f3f2645c861f72eaf5e76273c6c3632869423464b90a5
'http://http.debian.net/debian/pool/main/libz/libzstd/libzstd_1.5.7%2bdfsg-1.debian.tar.xz' libzstd_1.5.7+dfsg-1.debian.tar.xz 23036 SHA256:5e88424d919941291f79e1bfada6cb1a6f748671d9de7d4b7d931f361f183a15
```

### `dpkg` source package: `linux=6.12.33-1`

Binary Packages:

- `linux-libc-dev=6.12.33-1`

Licenses: (parsed from: `/usr/share/doc/linux-libc-dev/copyright`)

- `BSD-2-clause`
- `GPL-2`
- `GPL-2+-or-X11`
- `LGPL-2.1`
- `Unicode-data`
- `Xen-interface`

Source:

```console
$ apt-get source -qq --print-uris linux=6.12.33-1
'http://http.debian.net/debian/pool/main/l/linux/linux_6.12.33-1.dsc' linux_6.12.33-1.dsc 219407 SHA256:bdbfdcfc7243a398393bc75b98a7c022151968979ea3ca7cecc68644edf42562
'http://http.debian.net/debian/pool/main/l/linux/linux_6.12.33.orig.tar.xz' linux_6.12.33.orig.tar.xz 151068244 SHA256:3de838b5ffa93d48687fcaf0fbc6dcba1a6c73672b4884a271f862f525f82b48
'http://http.debian.net/debian/pool/main/l/linux/linux_6.12.33-1.debian.tar.xz' linux_6.12.33-1.debian.tar.xz 1645304 SHA256:b3e845b88b85278231bc043c006b4f339dfef301acbaf11844a1091a6b4dbc81
```

### `dpkg` source package: `littler=0.3.21-1`

Binary Packages:

- `littler=0.3.21-1`
- `r-cran-littler=0.3.21-1`

Licenses: (parsed from: `/usr/share/doc/littler/copyright`, `/usr/share/doc/r-cran-littler/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris littler=0.3.21-1
'http://http.debian.net/debian/pool/main/l/littler/littler_0.3.21-1.dsc' littler_0.3.21-1.dsc 1874 SHA256:6c4c5d6ca4b508b42975ebb39a936646b654dacaa8823b25d3eeb14a55e36490
'http://http.debian.net/debian/pool/main/l/littler/littler_0.3.21.orig.tar.gz' littler_0.3.21.orig.tar.gz 129864 SHA256:9e8be7aca97ef31ecc7af845954caddf52f9dad4d28ee1392dca829b75e64085
'http://http.debian.net/debian/pool/main/l/littler/littler_0.3.21-1.debian.tar.xz' littler_0.3.21-1.debian.tar.xz 7040 SHA256:46d6509af2b1343d9871c0d4dc3715b28d20c815f232bef8ae9310358f706088
```

### `dpkg` source package: `lz4=1.10.0-4`

Binary Packages:

- `liblz4-1:amd64=1.10.0-4`

Licenses: (parsed from: `/usr/share/doc/liblz4-1/copyright`)

- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris lz4=1.10.0-4
'http://http.debian.net/debian/pool/main/l/lz4/lz4_1.10.0-4.dsc' lz4_1.10.0-4.dsc 1941 SHA256:394c635aa75a21cd5896680e48821c05336645072ae866b2717d53f36b9ba851
'http://http.debian.net/debian/pool/main/l/lz4/lz4_1.10.0.orig.tar.gz' lz4_1.10.0.orig.tar.gz 387114 SHA256:537512904744b35e232912055ccf8ec66d768639ff3abe5788d90d792ec5f48b
'http://http.debian.net/debian/pool/main/l/lz4/lz4_1.10.0-4.debian.tar.xz' lz4_1.10.0-4.debian.tar.xz 8080 SHA256:8d276c3254182c2c9cf319b9a6504cf257c56b441f37d3db8ad97d33d46a0911
```

### `dpkg` source package: `make-dfsg=4.4.1-2`

Binary Packages:

- `make=4.4.1-2`

Licenses: (parsed from: `/usr/share/doc/make/copyright`)

- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris make-dfsg=4.4.1-2
'http://http.debian.net/debian/pool/main/m/make-dfsg/make-dfsg_4.4.1-2.dsc' make-dfsg_4.4.1-2.dsc 1976 SHA256:c3116d3a50914a68c7c1c32ca825b5fdea1c609b8c7cdd4119b79addf7e931ce
'http://http.debian.net/debian/pool/main/m/make-dfsg/make-dfsg_4.4.1.orig.tar.xz' make-dfsg_4.4.1.orig.tar.xz 1125180 SHA256:3b16b00ea1079af9f8096bbc71ff7cc00c249fc6a862003da3c42308a0adb0fe
'http://http.debian.net/debian/pool/main/m/make-dfsg/make-dfsg_4.4.1-2.debian.tar.xz' make-dfsg_4.4.1-2.debian.tar.xz 44088 SHA256:c785b80bd83b8294f104da43aee9573ba3e175e2e9a77ac00a49f0a569d6e061
```

### `dpkg` source package: `mawk=1.3.4.20250131-1`

Binary Packages:

- `mawk=1.3.4.20250131-1`

Licenses: (parsed from: `/usr/share/doc/mawk/copyright`)

- `CC-BY-3.0`
- `GPL-2`
- `GPL-2.0-only`
- `X11`

Source:

```console
$ apt-get source -qq --print-uris mawk=1.3.4.20250131-1
'http://http.debian.net/debian/pool/main/m/mawk/mawk_1.3.4.20250131-1.dsc' mawk_1.3.4.20250131-1.dsc 2969 SHA256:147dd01670e2ebf61f3c78470e0025b87d14e69c7ba9cfafd54da32a355dea84
'http://http.debian.net/debian/pool/main/m/mawk/mawk_1.3.4.20250131.orig.tar.gz' mawk_1.3.4.20250131.orig.tar.gz 433213 SHA256:51bcb82d577b141d896d9d9c3077d7aaa209490132e9f2b9573ba8511b3835be
'http://http.debian.net/debian/pool/main/m/mawk/mawk_1.3.4.20250131.orig.tar.gz.asc' mawk_1.3.4.20250131.orig.tar.gz.asc 729 SHA256:bc83f127727edb42a91d516770c8d0d3cdb5f6e541aa3cb5213b79dae494db95
'http://http.debian.net/debian/pool/main/m/mawk/mawk_1.3.4.20250131-1.debian.tar.xz' mawk_1.3.4.20250131-1.debian.tar.xz 16008 SHA256:23dea8244bf4f116ec3cd202ab5d4693207d82d986cd0a3d79442b916be4e2b7
```

### `dpkg` source package: `mgcv=1.9-3-1`

Binary Packages:

- `r-cran-mgcv=1.9-3-1`

Licenses: (parsed from: `/usr/share/doc/r-cran-mgcv/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris mgcv=1.9-3-1
'http://http.debian.net/debian/pool/main/m/mgcv/mgcv_1.9-3-1.dsc' mgcv_1.9-3-1.dsc 1826 SHA256:e0ebc9ab153c1b0ba46a80478937be0540a9f8b2673c7024fd4a34af146ab1b4
'http://http.debian.net/debian/pool/main/m/mgcv/mgcv_1.9-3.orig.tar.gz' mgcv_1.9-3.orig.tar.gz 1127049 SHA256:43f0ccdba176890a1d7bbe9a0a0859222e1fbcc97064c6e6ad7a3f545fd82f1d
'http://http.debian.net/debian/pool/main/m/mgcv/mgcv_1.9-3-1.debian.tar.xz' mgcv_1.9-3-1.debian.tar.xz 5584 SHA256:07e733e9c18e14c7a9beee77590c2386d594b16b76cfda1298a9a604b50ed728
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

### `dpkg` source package: `mpfr4=4.2.2-1`

Binary Packages:

- `libmpfr6:amd64=4.2.2-1`

Licenses: (parsed from: `/usr/share/doc/libmpfr6/copyright`)

- `GFDL-1.2`
- `LGPL-3`

Source:

```console
$ apt-get source -qq --print-uris mpfr4=4.2.2-1
'http://http.debian.net/debian/pool/main/m/mpfr4/mpfr4_4.2.2-1.dsc' mpfr4_4.2.2-1.dsc 1960 SHA256:08ee7b45f8a9980570508770a9d48f70d4c1962fd7c98af4a78cbc3747002ecd
'http://http.debian.net/debian/pool/main/m/mpfr4/mpfr4_4.2.2.orig.tar.xz' mpfr4_4.2.2.orig.tar.xz 1505596 SHA256:b67ba0383ef7e8a8563734e2e889ef5ec3c3b898a01d00fa0a6869ad81c6ce01
'http://http.debian.net/debian/pool/main/m/mpfr4/mpfr4_4.2.2-1.debian.tar.xz' mpfr4_4.2.2-1.debian.tar.xz 12564 SHA256:3e203524cdc516a99ec8a676dd9d21435b5f020e624149d39f4c530393d5a563
```

### `dpkg` source package: `ncurses=6.5+20250216-2`

Binary Packages:

- `libncurses-dev:amd64=6.5+20250216-2`
- `libncurses6:amd64=6.5+20250216-2`
- `libncursesw6:amd64=6.5+20250216-2`
- `libtinfo6:amd64=6.5+20250216-2`
- `ncurses-base=6.5+20250216-2`
- `ncurses-bin=6.5+20250216-2`

Licenses: (parsed from: `/usr/share/doc/libncurses-dev/copyright`, `/usr/share/doc/libncurses6/copyright`, `/usr/share/doc/libncursesw6/copyright`, `/usr/share/doc/libtinfo6/copyright`, `/usr/share/doc/ncurses-base/copyright`, `/usr/share/doc/ncurses-bin/copyright`)

- `BSD-3-clause`
- `MIT/X11`
- `X11`

Source:

```console
$ apt-get source -qq --print-uris ncurses=6.5+20250216-2
'http://http.debian.net/debian/pool/main/n/ncurses/ncurses_6.5%2b20250216-2.dsc' ncurses_6.5+20250216-2.dsc 3890 SHA256:00539cc2bc6bb84be1b8a8a5decf606682e14b6f39b76b9aa090e65d2c2d4580
'http://http.debian.net/debian/pool/main/n/ncurses/ncurses_6.5%2b20250216.orig.tar.gz' ncurses_6.5+20250216.orig.tar.gz 3774714 SHA256:b37baafa436e7133bb12a185cb8f60e1599b1947e9f0181c76f3190acf28b6eb
'http://http.debian.net/debian/pool/main/n/ncurses/ncurses_6.5%2b20250216.orig.tar.gz.asc' ncurses_6.5+20250216.orig.tar.gz.asc 729 SHA256:64f4d17923322176c44079f18f170e2164a59d551d7e4e9c1a6e4eebedc5dd6f
'http://http.debian.net/debian/pool/main/n/ncurses/ncurses_6.5%2b20250216-2.debian.tar.xz' ncurses_6.5+20250216-2.debian.tar.xz 50420 SHA256:546930a8992ae3325d8c38378f290265d969cf6333cfae9648ac6d69e1e8a8a6
```

### `dpkg` source package: `nettle=3.10.1-1`

Binary Packages:

- `libhogweed6t64:amd64=3.10.1-1`
- `libnettle8t64:amd64=3.10.1-1`

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
$ apt-get source -qq --print-uris nettle=3.10.1-1
'http://http.debian.net/debian/pool/main/n/nettle/nettle_3.10.1-1.dsc' nettle_3.10.1-1.dsc 2053 SHA256:7b440850ce04b341363f3f5e23dfb9f96ebf7d52e0ef7ba2d07120c90ca61b3c
'http://http.debian.net/debian/pool/main/n/nettle/nettle_3.10.1.orig.tar.gz' nettle_3.10.1.orig.tar.gz 2643267 SHA256:b0fcdd7fc0cdea6e80dcf1dd85ba794af0d5b4a57e26397eee3bc193272d9132
'http://http.debian.net/debian/pool/main/n/nettle/nettle_3.10.1-1.debian.tar.xz' nettle_3.10.1-1.debian.tar.xz 25036 SHA256:2d40d02ddac5985d8833532a17a0ef96cb685ee0547ee9617ec13793b22e34c6
```

### `dpkg` source package: `nghttp2=1.64.0-1.1`

Binary Packages:

- `libnghttp2-14:amd64=1.64.0-1.1`

Licenses: (parsed from: `/usr/share/doc/libnghttp2-14/copyright`)

- `BSD-2-clause`
- `Expat`
- `GPL-3`
- `GPL-3+ with autoconf exception`
- `MIT`
- `all-permissive`

Source:

```console
$ apt-get source -qq --print-uris nghttp2=1.64.0-1.1
'http://http.debian.net/debian/pool/main/n/nghttp2/nghttp2_1.64.0-1.1.dsc' nghttp2_1.64.0-1.1.dsc 2514 SHA256:1d0393fc66b1db3e9e842a2a02bf41e7c25b020704ef601b7e5d3f5a0e74cc00
'http://http.debian.net/debian/pool/main/n/nghttp2/nghttp2_1.64.0.orig.tar.gz' nghttp2_1.64.0.orig.tar.gz 1069782 SHA256:b452dc69a1fcbc9375389b8b154175d8b7b125cdd713fc426774c2b79a1ebd77
'http://http.debian.net/debian/pool/main/n/nghttp2/nghttp2_1.64.0-1.1.debian.tar.xz' nghttp2_1.64.0-1.1.debian.tar.xz 39356 SHA256:02b15d82ad6b62a149481fd2871bda26486457821e9a4fa28897f55e1294f379
```

### `dpkg` source package: `nghttp3=1.8.0-1`

Binary Packages:

- `libnghttp3-9:amd64=1.8.0-1`

Licenses: (parsed from: `/usr/share/doc/libnghttp3-9/copyright`)

- `FSFAP`
- `FSFUL`
- `FSFULLR`
- `GPL-2`
- `GPL-2+ with Autoconf generic exception`
- `GPL-2+ with Libtool Exception`
- `GPL-3`
- `GPL-3+`
- `GPL-3+ with Autoconf generic exception`
- `MIT`

Source:

```console
$ apt-get source -qq --print-uris nghttp3=1.8.0-1
'http://http.debian.net/debian/pool/main/n/nghttp3/nghttp3_1.8.0-1.dsc' nghttp3_1.8.0-1.dsc 1603 SHA256:ffc623e78be62361a82f0a2e7b9a19ff0bcdfc371b8bcc1842039499a12adba2
'http://http.debian.net/debian/pool/main/n/nghttp3/nghttp3_1.8.0.orig.tar.xz' nghttp3_1.8.0.orig.tar.xz 398640 SHA256:a9dd28970977e6802a3eaf2cfaeae6d0fae60c8d2c0f2c4ce600036a7998ee9a
'http://http.debian.net/debian/pool/main/n/nghttp3/nghttp3_1.8.0.orig.tar.xz.asc' nghttp3_1.8.0.orig.tar.xz.asc 833 SHA256:c2549dd50a5ad392610d108244357c1cc750fd5bf4a5ef91de1d94d11c49b0cf
'http://http.debian.net/debian/pool/main/n/nghttp3/nghttp3_1.8.0-1.debian.tar.xz' nghttp3_1.8.0-1.debian.tar.xz 8228 SHA256:fc0cfa954de5b8fef85bd13e1edcbfccb463ce211905e925921b608390c840c9
```

### `dpkg` source package: `nlme=3.1.168-1`

Binary Packages:

- `r-cran-nlme=3.1.168-1`

Licenses: (parsed from: `/usr/share/doc/r-cran-nlme/copyright`)

- `GPL`
- `GPL `

Source:

```console
$ apt-get source -qq --print-uris nlme=3.1.168-1
'http://http.debian.net/debian/pool/main/n/nlme/nlme_3.1.168-1.dsc' nlme_3.1.168-1.dsc 1840 SHA256:a3e233c4708c7d2a4ac1c4695d9ac6b5ee8fb7ab7380b0623044b9f7f9f01959
'http://http.debian.net/debian/pool/main/n/nlme/nlme_3.1.168.orig.tar.gz' nlme_3.1.168.orig.tar.gz 860576 SHA256:23b78468344cb6775dee5e0d9c8133032d64f08ebaba20776508a0443a897362
'http://http.debian.net/debian/pool/main/n/nlme/nlme_3.1.168-1.debian.tar.xz' nlme_3.1.168-1.debian.tar.xz 7376 SHA256:92c007f10be211cc87764096d2eb935e9e373dd4e3249726a51b7747415478b8
```

### `dpkg` source package: `openblas=0.3.29+ds-3`

Binary Packages:

- `libopenblas0-pthread:amd64=0.3.29+ds-3`

Licenses: (parsed from: `/usr/share/doc/libopenblas0-pthread/copyright`)

- `Apache-2.0`
- `BSD-2-clause`
- `BSD-2-clause-texas`
- `BSD-3-clause`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris openblas=0.3.29+ds-3
'http://http.debian.net/debian/pool/main/o/openblas/openblas_0.3.29%2bds-3.dsc' openblas_0.3.29+ds-3.dsc 4579 SHA256:b5ee492da8dd40f0ce693635a6a9259c3634d2ff1a569d5baf18a53d62e2629c
'http://http.debian.net/debian/pool/main/o/openblas/openblas_0.3.29%2bds.orig.tar.xz' openblas_0.3.29+ds.orig.tar.xz 2208664 SHA256:eb691e2cff83799400da22aa6ab93ebaa346ad317fea578b7ae119e226ce1b01
'http://http.debian.net/debian/pool/main/o/openblas/openblas_0.3.29%2bds-3.debian.tar.xz' openblas_0.3.29+ds-3.debian.tar.xz 25544 SHA256:2f5d0b3a5c06209a737d1f0064d94583989504bc4a07019f78f46337b09e2e79
```

### `dpkg` source package: `openldap=2.6.10+dfsg-1`

Binary Packages:

- `libldap2:amd64=2.6.10+dfsg-1`

Licenses: (parsed from: `/usr/share/doc/libldap2/copyright`)

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
$ apt-get source -qq --print-uris openldap=2.6.10+dfsg-1
'http://http.debian.net/debian/pool/main/o/openldap/openldap_2.6.10%2bdfsg-1.dsc' openldap_2.6.10+dfsg-1.dsc 3285 SHA256:05cdd431ef995904f094f4464ca78d5d3b2abdbe4eefacd72446ff8443a2ffac
'http://http.debian.net/debian/pool/main/o/openldap/openldap_2.6.10%2bdfsg.orig.tar.xz' openldap_2.6.10+dfsg.orig.tar.xz 3754560 SHA256:e871102bda1e42155fd4d6be4825a297e1c593cb0907b84fc7dde888dc847877
'http://http.debian.net/debian/pool/main/o/openldap/openldap_2.6.10%2bdfsg-1.debian.tar.xz' openldap_2.6.10+dfsg-1.debian.tar.xz 170112 SHA256:2dc95ade5655d67c9043e45b5601734fdb7f668267682d087b595a80de24a500
```

### `dpkg` source package: `openssl=3.5.0-2`

Binary Packages:

- `libssl3t64:amd64=3.5.0-2`
- `openssl=3.5.0-2`
- `openssl-provider-legacy=3.5.0-2`

Licenses: (parsed from: `/usr/share/doc/libssl3t64/copyright`, `/usr/share/doc/openssl/copyright`, `/usr/share/doc/openssl-provider-legacy/copyright`)

- `Apache-2.0`
- `Artistic`
- `GPL-1`
- `GPL-1+`

Source:

```console
$ apt-get source -qq --print-uris openssl=3.5.0-2
'http://http.debian.net/debian/pool/main/o/openssl/openssl_3.5.0-2.dsc' openssl_3.5.0-2.dsc 2637 SHA256:f40cac5c47c23869fdccd4ba9143227f763b4c0d9b79652be3ae631979408100
'http://http.debian.net/debian/pool/main/o/openssl/openssl_3.5.0.orig.tar.gz' openssl_3.5.0.orig.tar.gz 53136912 SHA256:344d0a79f1a9b08029b0744e2cc401a43f9c90acd1044d09a530b4885a8e9fc0
'http://http.debian.net/debian/pool/main/o/openssl/openssl_3.5.0.orig.tar.gz.asc' openssl_3.5.0.orig.tar.gz.asc 833 SHA256:cdede0397099346374e8b31fcc5cc490e4a05205a7426eb34a02cf9800de044b
'http://http.debian.net/debian/pool/main/o/openssl/openssl_3.5.0-2.debian.tar.xz' openssl_3.5.0-2.debian.tar.xz 51924 SHA256:654257ddd41e086c16d0c6c249cc700bd20a20409d5e1f49d72270268de5206e
```

### `dpkg` source package: `p11-kit=0.25.5-3`

Binary Packages:

- `libp11-kit0:amd64=0.25.5-3`

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
$ apt-get source -qq --print-uris p11-kit=0.25.5-3
'http://http.debian.net/debian/pool/main/p/p11-kit/p11-kit_0.25.5-3.dsc' p11-kit_0.25.5-3.dsc 2538 SHA256:65e21a68dd942741bba82f5bf20901f616b64de91a976d92a54a0cb314896544
'http://http.debian.net/debian/pool/main/p/p11-kit/p11-kit_0.25.5.orig.tar.xz' p11-kit_0.25.5.orig.tar.xz 1002056 SHA256:04d0a86450cdb1be018f26af6699857171a188ac6d5b8c90786a60854e1198e5
'http://http.debian.net/debian/pool/main/p/p11-kit/p11-kit_0.25.5.orig.tar.xz.asc' p11-kit_0.25.5.orig.tar.xz.asc 228 SHA256:066c92b9d2accb2fda6a2f71e676fb6526fcc153051b1f04ee7d7c8c96a09989
'http://http.debian.net/debian/pool/main/p/p11-kit/p11-kit_0.25.5-3.debian.tar.xz' p11-kit_0.25.5-3.debian.tar.xz 24184 SHA256:3800ea81e4615898813f533834ad37ec270f6f7d4c9413c84e712075a197849c
```

### `dpkg` source package: `pam=1.7.0-3`

Binary Packages:

- `libpam-modules:amd64=1.7.0-3`
- `libpam-modules-bin=1.7.0-3`
- `libpam-runtime=1.7.0-3`
- `libpam0g:amd64=1.7.0-3`

Licenses: (parsed from: `/usr/share/doc/libpam-modules/copyright`, `/usr/share/doc/libpam-modules-bin/copyright`, `/usr/share/doc/libpam-runtime/copyright`, `/usr/share/doc/libpam0g/copyright`)

- `BSD-3-clause`
- `BSD-tcp_wrappers`
- `Beerware`
- `GPL`
- `GPL-1`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+ with Bison exception`
- `LGPL-2`
- `LGPL-2+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris pam=1.7.0-3
'http://deb.debian.org/debian/pool/main/p/pam/pam_1.7.0-3.dsc' pam_1.7.0-3.dsc 2210 SHA256:55350f07d07d565e1323282b2ceda48559c335c27ec7199d99c4e803006349d0
'http://deb.debian.org/debian/pool/main/p/pam/pam_1.7.0.orig.tar.xz' pam_1.7.0.orig.tar.xz 507824 SHA256:57dcd7a6b966ecd5bbd95e1d11173734691e16b68692fa59661cdae9b13b1697
'http://deb.debian.org/debian/pool/main/p/pam/pam_1.7.0.orig.tar.xz.asc' pam_1.7.0.orig.tar.xz.asc 801 SHA256:7a8ea18ec7d9dd1f8cbf9055c32128cbca8241aa63e9fea44d56ce6f0e15e441
'http://deb.debian.org/debian/pool/main/p/pam/pam_1.7.0-3.debian.tar.xz' pam_1.7.0-3.debian.tar.xz 132064 SHA256:ff446441cd74a3440b2bd32098d8865e959e497fde167b92ba776d1f354a0946
```

Other potentially useful URLs:

- https://sources.debian.net/src/pam/1.7.0-3/ (for browsing the source)
- https://sources.debian.net/src/pam/1.7.0-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/pam/1.7.0-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `pango1.0=1.56.3-1`

Binary Packages:

- `libpango-1.0-0:amd64=1.56.3-1`
- `libpangocairo-1.0-0:amd64=1.56.3-1`
- `libpangoft2-1.0-0:amd64=1.56.3-1`

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
$ apt-get source -qq --print-uris pango1.0=1.56.3-1
'http://http.debian.net/debian/pool/main/p/pango1.0/pango1.0_1.56.3-1.dsc' pango1.0_1.56.3-1.dsc 3690 SHA256:173af22e6447fd24322d8ffbed4bbafd090b88ea463c416701b9aa37cae75266
'http://http.debian.net/debian/pool/main/p/pango1.0/pango1.0_1.56.3.orig.tar.xz' pango1.0_1.56.3.orig.tar.xz 1883584 SHA256:2606252bc25cd8d24e1b7f7e92c3a272b37acd6734347b73b47a482834ba2491
'http://http.debian.net/debian/pool/main/p/pango1.0/pango1.0_1.56.3-1.debian.tar.xz' pango1.0_1.56.3-1.debian.tar.xz 43788 SHA256:00576a0cd3fd4ded5edcd5b5e1c710ee8034b00b49907b2d9c3e38906151f816
```

### `dpkg` source package: `patch=2.8-2`

Binary Packages:

- `patch=2.8-2`

Licenses: (parsed from: `/usr/share/doc/patch/copyright`)

- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris patch=2.8-2
'http://http.debian.net/debian/pool/main/p/patch/patch_2.8-2.dsc' patch_2.8-2.dsc 1689 SHA256:41fbd3f2c99f60dcbe02699ff01955a47711377b20987352b957bd55e02e2088
'http://http.debian.net/debian/pool/main/p/patch/patch_2.8.orig.tar.xz' patch_2.8.orig.tar.xz 907208 SHA256:f87cee69eec2b4fcbf60a396b030ad6aa3415f192aa5f7ee84cad5e11f7f5ae3
'http://http.debian.net/debian/pool/main/p/patch/patch_2.8-2.debian.tar.xz' patch_2.8-2.debian.tar.xz 9460 SHA256:9a740460988c910c5538e4d24df00d9961d19dee014c63e92f5d60e611fa60c4
```

### `dpkg` source package: `pcre2=10.45-1`

Binary Packages:

- `libpcre2-16-0:amd64=10.45-1`
- `libpcre2-32-0:amd64=10.45-1`
- `libpcre2-8-0:amd64=10.45-1`
- `libpcre2-dev:amd64=10.45-1`
- `libpcre2-posix3:amd64=10.45-1`

Licenses: (parsed from: `/usr/share/doc/libpcre2-16-0/copyright`, `/usr/share/doc/libpcre2-32-0/copyright`, `/usr/share/doc/libpcre2-8-0/copyright`, `/usr/share/doc/libpcre2-dev/copyright`, `/usr/share/doc/libpcre2-posix3/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `BSD-3-clause-Cambridge with BINARY LIBRARY-LIKE PACKAGES exception`
- `X11`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris pcre2=10.45-1
'http://http.debian.net/debian/pool/main/p/pcre2/pcre2_10.45-1.dsc' pcre2_10.45-1.dsc 2337 SHA256:9b9d6aa2c970a416cb6808ac894d18fe37dd6df0497e2d75c13bb86429fa7b35
'http://http.debian.net/debian/pool/main/p/pcre2/pcre2_10.45.orig.tar.gz' pcre2_10.45.orig.tar.gz 2715958 SHA256:0e138387df7835d7403b8351e2226c1377da804e0737db0e071b48f07c9d12ee
'http://http.debian.net/debian/pool/main/p/pcre2/pcre2_10.45-1.diff.gz' pcre2_10.45-1.diff.gz 8659 SHA256:02ef5e4fbdf274f344c7be0efb3d1bdff538bd621e6988cc0a3d2c43da40b351
```

### `dpkg` source package: `perl=5.40.1-3`

Binary Packages:

- `libperl5.40:amd64=5.40.1-3`
- `perl=5.40.1-3`
- `perl-base=5.40.1-3`
- `perl-modules-5.40=5.40.1-3`

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
$ apt-get source -qq --print-uris perl=5.40.1-3
'http://http.debian.net/debian/pool/main/p/perl/perl_5.40.1-3.dsc' perl_5.40.1-3.dsc 2372 SHA256:97f69bf3cf3a4318a2a2a54cff072e3e870ed5426e7c578831791b63221f40b8
'http://http.debian.net/debian/pool/main/p/perl/perl_5.40.1.orig-regen-configure.tar.xz' perl_5.40.1.orig-regen-configure.tar.xz 421056 SHA256:4ea023d08101443f6ed9dc3bdd9bb5f5e08087678dc9e443d195df22da36209a
'http://http.debian.net/debian/pool/main/p/perl/perl_5.40.1.orig.tar.xz' perl_5.40.1.orig.tar.xz 13930924 SHA256:dfa20c2eef2b4af133525610bbb65dd13777ecf998c9c5b1ccf0d308e732ee3f
'http://http.debian.net/debian/pool/main/p/perl/perl_5.40.1-3.debian.tar.xz' perl_5.40.1-3.debian.tar.xz 167844 SHA256:6144b016c000ebdf5643b41b2fb579a5845e17461d187983f82e7d26b637f146
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

### `dpkg` source package: `procps=2:4.0.4-8`

Binary Packages:

- `libproc2-0:amd64=2:4.0.4-8`
- `procps=2:4.0.4-8`

Licenses: (parsed from: `/usr/share/doc/libproc2-0/copyright`, `/usr/share/doc/procps/copyright`)

- `GPL-2`
- `GPL-2.0+`
- `LGPL-2`
- `LGPL-2.0+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris procps=2:4.0.4-8
'http://http.debian.net/debian/pool/main/p/procps/procps_4.0.4-8.dsc' procps_4.0.4-8.dsc 2124 SHA256:996c2e0af9956dd1dfb9604720eb24ec21a79a53c320c7125794f8ac2791a640
'http://http.debian.net/debian/pool/main/p/procps/procps_4.0.4.orig.tar.xz' procps_4.0.4.orig.tar.xz 1401540 SHA256:22870d6feb2478adb617ce4f09a787addaf2d260c5a8aa7b17d889a962c5e42e
'http://http.debian.net/debian/pool/main/p/procps/procps_4.0.4-8.debian.tar.xz' procps_4.0.4-8.debian.tar.xz 45408 SHA256:0d1723a0134f8b6ae2619a4e9878084c06f92e36ab7c163086d713f2ed064f3d
```

### `dpkg` source package: `r-base=4.5.1-1`

Binary Packages:

- `r-base=4.5.1-1`
- `r-base-core=4.5.1-1`
- `r-base-dev=4.5.1-1`
- `r-recommended=4.5.1-1`

Licenses: (parsed from: `/usr/share/doc/r-base/copyright`, `/usr/share/doc/r-base-core/copyright`, `/usr/share/doc/r-base-dev/copyright`, `/usr/share/doc/r-recommended/copyright`)

- `Artistic`
- `GPL-2`
- `GPL-3`
- `LGPL-2`
- `LGPL-2.1`
- `LGPL-3`

Source:

```console
$ apt-get source -qq --print-uris r-base=4.5.1-1
'http://http.debian.net/debian/pool/main/r/r-base/r-base_4.5.1-1.dsc' r-base_4.5.1-1.dsc 2907 SHA256:1772cedb9d84b0b02d100ea4506a0ac7c52f228545f80bb206872e0673d55dce
'http://http.debian.net/debian/pool/main/r/r-base/r-base_4.5.1.orig.tar.gz' r-base_4.5.1.orig.tar.gz 40518816 SHA256:b42a7921400386645b10105b91c68728787db5c4c83c9f6c30acdce632e1bb70
'http://http.debian.net/debian/pool/main/r/r-base/r-base_4.5.1-1.debian.tar.xz' r-base_4.5.1-1.debian.tar.xz 100912 SHA256:ec782967247a319a9e1f1b7f072e30a3cc3aec2478d915729214743d23af5ba0
```

### `dpkg` source package: `r-cran-class=7.3-23-1`

Binary Packages:

- `r-cran-class=7.3-23-1`

Licenses: (parsed from: `/usr/share/doc/r-cran-class/copyright`)

- `GPL-2`
- `GPL-2 | GPL-3`

Source:

```console
$ apt-get source -qq --print-uris r-cran-class=7.3-23-1
'http://http.debian.net/debian/pool/main/r/r-cran-class/r-cran-class_7.3-23-1.dsc' r-cran-class_7.3-23-1.dsc 1873 SHA256:67260b6a959736c538cd4574488a7ebe6c56a8a561b4bdf12a854f5db05cb4ac
'http://http.debian.net/debian/pool/main/r/r-cran-class/r-cran-class_7.3-23.orig.tar.gz' r-cran-class_7.3-23.orig.tar.gz 22058 SHA256:4d1adb12eae045f15641516d795177dd1d3074c0a86ac633000507c4822891f1
'http://http.debian.net/debian/pool/main/r/r-cran-class/r-cran-class_7.3-23-1.debian.tar.xz' r-cran-class_7.3-23-1.debian.tar.xz 3316 SHA256:cffa8348b0495dad67767a1d6ee38762dd25cf5674c44635cf83ff928f39ff5a
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

### `dpkg` source package: `r-cran-mass=7.3-65-1`

Binary Packages:

- `r-cran-mass=7.3-65-1`

Licenses: (parsed from: `/usr/share/doc/r-cran-mass/copyright`)

- `GPL-2`
- `GPL-2 | GPL-3`

Source:

```console
$ apt-get source -qq --print-uris r-cran-mass=7.3-65-1
'http://http.debian.net/debian/pool/main/r/r-cran-mass/r-cran-mass_7.3-65-1.dsc' r-cran-mass_7.3-65-1.dsc 1851 SHA256:530e4881166d5a06103cd8bd8ea1378269390fd788a2092e948684759edef6e0
'http://http.debian.net/debian/pool/main/r/r-cran-mass/r-cran-mass_7.3-65.orig.tar.gz' r-cran-mass_7.3-65.orig.tar.gz 510322 SHA256:b07ef1e3c364ce56269b4a8a7759cc9f87c876554f91293437bb578cfe38172f
'http://http.debian.net/debian/pool/main/r/r-cran-mass/r-cran-mass_7.3-65-1.debian.tar.xz' r-cran-mass_7.3-65-1.debian.tar.xz 6656 SHA256:7afbb1ad2accbdd53ec74654d9b6bebbcd31a0e474fbaca4289b9928c85c275c
```

### `dpkg` source package: `r-cran-nnet=7.3-20-1`

Binary Packages:

- `r-cran-nnet=7.3-20-1`

Licenses: (parsed from: `/usr/share/doc/r-cran-nnet/copyright`)

- `GPL-2`
- `GPL-2 | GPL-3`

Source:

```console
$ apt-get source -qq --print-uris r-cran-nnet=7.3-20-1
'http://http.debian.net/debian/pool/main/r/r-cran-nnet/r-cran-nnet_7.3-20-1.dsc' r-cran-nnet_7.3-20-1.dsc 1848 SHA256:420c69ec7bb32356568e0f9cd4e72de5afdad2de8263fc185095ccb7cc1f5e9a
'http://http.debian.net/debian/pool/main/r/r-cran-nnet/r-cran-nnet_7.3-20.orig.tar.gz' r-cran-nnet_7.3-20.orig.tar.gz 31285 SHA256:8f33e17e0eb161cfbc1bfee4875baa23c66fcdba8215a64a63402b099db2b555
'http://http.debian.net/debian/pool/main/r/r-cran-nnet/r-cran-nnet_7.3-20-1.debian.tar.xz' r-cran-nnet_7.3-20-1.debian.tar.xz 3352 SHA256:128815fe8f2cec37a1e8826ceba2345014208e99a8b2f34fe6e11a6ba430f2aa
```

### `dpkg` source package: `r-cran-spatial=7.3-18-1`

Binary Packages:

- `r-cran-spatial=7.3-18-1`

Licenses: (parsed from: `/usr/share/doc/r-cran-spatial/copyright`)

- `GPL-2`
- `GPL-2 | GPL-3`

Source:

```console
$ apt-get source -qq --print-uris r-cran-spatial=7.3-18-1
'http://http.debian.net/debian/pool/main/r/r-cran-spatial/r-cran-spatial_7.3-18-1.dsc' r-cran-spatial_7.3-18-1.dsc 1884 SHA256:8a1529c41d35fdb85098bb0ee4c677045a395ad0a9d6f6f4d12840efd5ee9e11
'http://http.debian.net/debian/pool/main/r/r-cran-spatial/r-cran-spatial_7.3-18.orig.tar.gz' r-cran-spatial_7.3-18.orig.tar.gz 46556 SHA256:cc46693d69745af8ec95b557e7a8ee4e1865df69dc0d25723629fd8e9ea43055
'http://http.debian.net/debian/pool/main/r/r-cran-spatial/r-cran-spatial_7.3-18-1.debian.tar.xz' r-cran-spatial_7.3-18-1.debian.tar.xz 3228 SHA256:62b62f43f100841ac79518bde24676d4dcfb4f9133b0643f6a8f3ac92a554bde
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

### `dpkg` source package: `rmatrix=1.7-3-1`

Binary Packages:

- `r-cran-matrix=1.7-3-1`

Licenses: (parsed from: `/usr/share/doc/r-cran-matrix/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris rmatrix=1.7-3-1
'http://http.debian.net/debian/pool/main/r/rmatrix/rmatrix_1.7-3-1.dsc' rmatrix_1.7-3-1.dsc 1860 SHA256:bb6f1b26797cf808babba5363b0f56a6488391513085850205cd146bf0ee3ce7
'http://http.debian.net/debian/pool/main/r/rmatrix/rmatrix_1.7-3.orig.tar.gz' rmatrix_1.7-3.orig.tar.gz 2485083 SHA256:6642e9db8cddf32a051972fd5a634bf7edbdc925c5c2d139bf71e92df00fb44e
'http://http.debian.net/debian/pool/main/r/rmatrix/rmatrix_1.7-3-1.debian.tar.xz' rmatrix_1.7-3-1.debian.tar.xz 6092 SHA256:28df0515e7efba903f9f2510addb1203d0ba11b4b563ee1b672eb49c1531f343
```

### `dpkg` source package: `rpart=4.1.24-1`

Binary Packages:

- `r-cran-rpart=4.1.24-1`

Licenses: (parsed from: `/usr/share/doc/r-cran-rpart/copyright`)

- `GPL-2`
- `GPL-2+ | license included below`

Source:

```console
$ apt-get source -qq --print-uris rpart=4.1.24-1
'http://http.debian.net/debian/pool/main/r/rpart/rpart_4.1.24-1.dsc' rpart_4.1.24-1.dsc 1843 SHA256:bc9677338746e43252b9e23974bb64365143d04db7b2cdd457ddb807e75b77a0
'http://http.debian.net/debian/pool/main/r/rpart/rpart_4.1.24.orig.tar.gz' rpart_4.1.24.orig.tar.gz 620065 SHA256:4ab169a764d9857d299313aae0e7764bcea9220576e537cf165d4f8117e72f29
'http://http.debian.net/debian/pool/main/r/rpart/rpart_4.1.24-1.debian.tar.xz' rpart_4.1.24-1.debian.tar.xz 4436 SHA256:471f830d8b7eb7ca5acde84993e2920a0ad771707f7549893cbb290195597565
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

### `dpkg` source package: `rust-sequoia-sqv=1.3.0-3`

Binary Packages:

- `sqv=1.3.0-3`

Licenses: (parsed from: `/usr/share/doc/sqv/copyright`)

- `LGPL-2`
- `LGPL-2.0-or-later`

Source:

```console
$ apt-get source -qq --print-uris rust-sequoia-sqv=1.3.0-3
'http://http.debian.net/debian/pool/main/r/rust-sequoia-sqv/rust-sequoia-sqv_1.3.0-3.dsc' rust-sequoia-sqv_1.3.0-3.dsc 2704 SHA256:98ad852ed30d42d3b0d6ce40d2f56a96fb443cc6fa2caeaa12516fe5bbe544af
'http://http.debian.net/debian/pool/main/r/rust-sequoia-sqv/rust-sequoia-sqv_1.3.0.orig.tar.gz' rust-sequoia-sqv_1.3.0.orig.tar.gz 140759 SHA256:8924571d26720b245292ad3c450e4061fcb24890461874790549747bffa35e60
'http://http.debian.net/debian/pool/main/r/rust-sequoia-sqv/rust-sequoia-sqv_1.3.0-3.debian.tar.xz' rust-sequoia-sqv_1.3.0-3.debian.tar.xz 3876 SHA256:be04e0365bc1206617a3e55d507bfce2e972819fb737e23a1112a717cc89b9bc
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

### `dpkg` source package: `sensible-utils=0.0.25`

Binary Packages:

- `sensible-utils=0.0.25`

Licenses: (parsed from: `/usr/share/doc/sensible-utils/copyright`)

- `All-permissive`
- `GPL-2`
- `GPL-2+`
- `configure`
- `installsh`

Source:

```console
$ apt-get source -qq --print-uris sensible-utils=0.0.25
'http://http.debian.net/debian/pool/main/s/sensible-utils/sensible-utils_0.0.25.dsc' sensible-utils_0.0.25.dsc 1718 SHA256:7d0deb8fca88c2e095a838b4ba2443c5c07f1501907b331a7ef051178c90a5a8
'http://http.debian.net/debian/pool/main/s/sensible-utils/sensible-utils_0.0.25.tar.xz' sensible-utils_0.0.25.tar.xz 76132 SHA256:b905fcb981397db693bbcdda2ba9af712552a092f3bacd621112ccc98ddce4bd
```

### `dpkg` source package: `shadow=1:4.17.4-2`

Binary Packages:

- `login.defs=1:4.17.4-2`
- `passwd=1:4.17.4-2`

Licenses: (parsed from: `/usr/share/doc/login.defs/copyright`, `/usr/share/doc/passwd/copyright`)

- `BSD-3-clause`
- `GPL-1`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris shadow=1:4.17.4-2
'http://http.debian.net/debian/pool/main/s/shadow/shadow_4.17.4-2.dsc' shadow_4.17.4-2.dsc 2851 SHA256:920de0d3be5303f2c0511d5531c1815abc258b15af8f9c511c8aa6d8e1a91a86
'http://http.debian.net/debian/pool/main/s/shadow/shadow_4.17.4.orig.tar.xz' shadow_4.17.4.orig.tar.xz 2326584 SHA256:554801054694ff7d8a7abdf0d6ece34e2f16e111673cc01b8c9ee1278451181e
'http://http.debian.net/debian/pool/main/s/shadow/shadow_4.17.4.orig.tar.xz.asc' shadow_4.17.4.orig.tar.xz.asc 488 SHA256:82437d2b54790b3a6734c526b757e693cd0c734ec6afd69f9a9cf0eb1dad8dc4
'http://http.debian.net/debian/pool/main/s/shadow/shadow_4.17.4-2.debian.tar.xz' shadow_4.17.4-2.debian.tar.xz 167792 SHA256:97eaf0b3682a8a1a1ae6e4c4fac00885a7433d2487e636bde7c1c406e66bdb23
```

### `dpkg` source package: `sqlite3=3.46.1-6`

Binary Packages:

- `libsqlite3-0:amd64=3.46.1-6`

Licenses: (parsed from: `/usr/share/doc/libsqlite3-0/copyright`)

- `GPL-2`
- `GPL-2+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris sqlite3=3.46.1-6
'http://http.debian.net/debian/pool/main/s/sqlite3/sqlite3_3.46.1-6.dsc' sqlite3_3.46.1-6.dsc 2632 SHA256:4637cd474d831b938bd8e38ce02719514487df7c191ddcfd1ad1cea0676c5c14
'http://http.debian.net/debian/pool/main/s/sqlite3/sqlite3_3.46.1.orig-www.tar.xz' sqlite3_3.46.1.orig-www.tar.xz 5861820 SHA256:648df41a8e532882b1905df45919aae4bafaf74c455f66bc86f1f52f45c8b8f0
'http://http.debian.net/debian/pool/main/s/sqlite3/sqlite3_3.46.1.orig.tar.xz' sqlite3_3.46.1.orig.tar.xz 8456776 SHA256:d0cdd2ece271b29e7ce18095745d892517ee26d0f270065b3a25c2e9eb11639c
'http://http.debian.net/debian/pool/main/s/sqlite3/sqlite3_3.46.1-6.debian.tar.xz' sqlite3_3.46.1-6.debian.tar.xz 33932 SHA256:a58092e00376a61e2b72546a19c2da44cc4982146a2827b1fe84cb3a1577a641
```

### `dpkg` source package: `survival=3.8-3-1`

Binary Packages:

- `r-cran-survival=3.8-3-1`

Licenses: (parsed from: `/usr/share/doc/r-cran-survival/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris survival=3.8-3-1
'http://http.debian.net/debian/pool/main/s/survival/survival_3.8-3-1.dsc' survival_3.8-3-1.dsc 1861 SHA256:69ed685e38174f9dca3fc3aaed3bcdc2195602c799f2dec0942d45099f16aa8e
'http://http.debian.net/debian/pool/main/s/survival/survival_3.8-3.orig.tar.gz' survival_3.8-3.orig.tar.gz 9537074 SHA256:dcab05a57d37a561c7426f6213d49852dc4f462180dd28b5325ff4b6a5e59915
'http://http.debian.net/debian/pool/main/s/survival/survival_3.8-3-1.debian.tar.xz' survival_3.8-3-1.debian.tar.xz 6384 SHA256:4b50bb4b568f0e66d697fbf1aeef0e9825231f274755e838a339eed051d00808
```

### `dpkg` source package: `systemd=257.6-1`

Binary Packages:

- `libsystemd0:amd64=257.6-1`
- `libudev1:amd64=257.6-1`

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
$ apt-get source -qq --print-uris systemd=257.6-1
'http://deb.debian.org/debian/pool/main/s/systemd/systemd_257.6-1.dsc' systemd_257.6-1.dsc 8614 SHA256:6edd1e36ac1c7759796182701b83f45a9e96c86a708d153ca64a83b82e4383f3
'http://deb.debian.org/debian/pool/main/s/systemd/systemd_257.6.orig.tar.gz' systemd_257.6.orig.tar.gz 16321562 SHA256:1ac656c61e595cc6e653883d554caadd2053f323d9065c0daff69f83368b120c
'http://deb.debian.org/debian/pool/main/s/systemd/systemd_257.6-1.debian.tar.xz' systemd_257.6-1.debian.tar.xz 182228 SHA256:e93575db3db98d4f0612798560a1f334ebcaf3033212635dd9d5ee4a11bc1455
```

Other potentially useful URLs:

- https://sources.debian.net/src/systemd/257.6-1/ (for browsing the source)
- https://sources.debian.net/src/systemd/257.6-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/systemd/257.6-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `sysvinit=3.14-4`

Binary Packages:

- `sysvinit-utils=3.14-4`

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
$ apt-get source -qq --print-uris sysvinit=3.14-4
'http://http.debian.net/debian/pool/main/s/sysvinit/sysvinit_3.14-4.dsc' sysvinit_3.14-4.dsc 2375 SHA256:1cfe65682218077e6f76011f0c5caacc9f2ab214d55893307d4a54c93312ac92
'http://http.debian.net/debian/pool/main/s/sysvinit/sysvinit_3.14.orig.tar.gz' sysvinit_3.14.orig.tar.gz 516357 SHA256:4e90a148707cf64113fc97343c053f9c0c9589551936b053999dcc69731f295f
'http://http.debian.net/debian/pool/main/s/sysvinit/sysvinit_3.14-4.debian.tar.xz' sysvinit_3.14-4.debian.tar.xz 122156 SHA256:2ba0aa763232112696bce50ee5acc707a515fcbd5b2c194193bfa7a0a525bff6
```

### `dpkg` source package: `tar=1.35+dfsg-3.1`

Binary Packages:

- `tar=1.35+dfsg-3.1`

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
$ apt-get source -qq --print-uris tar=1.35+dfsg-3.1
'http://http.debian.net/debian/pool/main/t/tar/tar_1.35%2bdfsg-3.1.dsc' tar_1.35+dfsg-3.1.dsc 2017 SHA256:5bb58d4966d94c99a9f1b182676089ecc05058d62fdb927f5c07539d9cda4077
'http://http.debian.net/debian/pool/main/t/tar/tar_1.35%2bdfsg.orig.tar.xz' tar_1.35+dfsg.orig.tar.xz 2111608 SHA256:9ae57e981c1e73c0eebc2b26c9b0c4497fe310ef1d516ea430efb5470b71f7a8
'http://http.debian.net/debian/pool/main/t/tar/tar_1.35%2bdfsg-3.1.debian.tar.xz' tar_1.35+dfsg-3.1.debian.tar.xz 21540 SHA256:0d0278034b82ed84dce04a461879b6e1871e4cb416a0ff04d3d35ff05fc30a53
```

### `dpkg` source package: `tcl8.6=8.6.16+dfsg-1`

Binary Packages:

- `libtcl8.6:amd64=8.6.16+dfsg-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris tcl8.6=8.6.16+dfsg-1
'http://http.debian.net/debian/pool/main/t/tcl8.6/tcl8.6_8.6.16%2bdfsg-1.dsc' tcl8.6_8.6.16+dfsg-1.dsc 2120 SHA256:684b346f5012d23350f66916eaba4682cdd8e38dac5788543538a2857dab20ac
'http://http.debian.net/debian/pool/main/t/tcl8.6/tcl8.6_8.6.16%2bdfsg.orig.tar.gz' tcl8.6_8.6.16+dfsg.orig.tar.gz 7037224 SHA256:c3b6a803ea2e55cafa8b4b52546a6b3bb3722927dcf4bebe3a6549fd353702ea
'http://http.debian.net/debian/pool/main/t/tcl8.6/tcl8.6_8.6.16%2bdfsg-1.debian.tar.xz' tcl8.6_8.6.16+dfsg-1.debian.tar.xz 14472 SHA256:66060c7937da5bae2a6be123c1240b682ad285cba6853f1d5f2e5d6fb3d049b1
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

### `dpkg` source package: `tiff=4.7.0-3`

Binary Packages:

- `libtiff6:amd64=4.7.0-3`

Licenses: (parsed from: `/usr/share/doc/libtiff6/copyright`)

- `Hylafax`

Source:

```console
$ apt-get source -qq --print-uris tiff=4.7.0-3
'http://http.debian.net/debian/pool/main/t/tiff/tiff_4.7.0-3.dsc' tiff_4.7.0-3.dsc 2255 SHA256:d5a9ee9829b123b5cbaaae1ff81a1f376bffd5f56a741ded4e051d6a8cd79ab3
'http://http.debian.net/debian/pool/main/t/tiff/tiff_4.7.0.orig.tar.bz2' tiff_4.7.0.orig.tar.bz2 2111254 SHA256:2b8b5c4e79cb2a4651796602e45d6179b7f18bc283feab417b8e881ef7e81862
'http://http.debian.net/debian/pool/main/t/tiff/tiff_4.7.0-3.debian.tar.xz' tiff_4.7.0-3.debian.tar.xz 24088 SHA256:cfcd813984a236bafff7d6b3e458d771970328c6843b1f9334e44275fd646b3e
```

### `dpkg` source package: `tk8.6=8.6.16-1`

Binary Packages:

- `libtk8.6:amd64=8.6.16-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris tk8.6=8.6.16-1
'http://http.debian.net/debian/pool/main/t/tk8.6/tk8.6_8.6.16-1.dsc' tk8.6_8.6.16-1.dsc 2155 SHA256:963a9428610a4bbcd0b7d51bbc3eb6a6ba4aa0fe194e0da62a8b0a39ccb262a5
'http://http.debian.net/debian/pool/main/t/tk8.6/tk8.6_8.6.16.orig.tar.gz' tk8.6_8.6.16.orig.tar.gz 4591625 SHA256:be9f94d3575d4b3099d84bc3c10de8994df2d7aa405208173c709cc404a7e5fe
'http://http.debian.net/debian/pool/main/t/tk8.6/tk8.6_8.6.16-1.debian.tar.xz' tk8.6_8.6.16-1.debian.tar.xz 10800 SHA256:fa4128d89bd5e80ed90bef0f015de5f3054aab301109eaef336847aa9aca7ac0
```

### `dpkg` source package: `tzdata=2025b-3`

Binary Packages:

- `tzdata=2025b-3`

Licenses: (parsed from: `/usr/share/doc/tzdata/copyright`)

- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris tzdata=2025b-3
'http://deb.debian.org/debian/pool/main/t/tzdata/tzdata_2025b-3.dsc' tzdata_2025b-3.dsc 2434 SHA256:2b3a207d8eef325bb92503866ab8de4bf132798bf1871e0fa3a09ceffbb66a40
'http://deb.debian.org/debian/pool/main/t/tzdata/tzdata_2025b.orig.tar.gz' tzdata_2025b.orig.tar.gz 464295 SHA256:11810413345fc7805017e27ea9fa4885fd74cd61b2911711ad038f5d28d71474
'http://deb.debian.org/debian/pool/main/t/tzdata/tzdata_2025b.orig.tar.gz.asc' tzdata_2025b.orig.tar.gz.asc 833 SHA256:829c06258175c0143754a89e26d7445c243a86cef8e9cf7d020b128f6d82496b
'http://deb.debian.org/debian/pool/main/t/tzdata/tzdata_2025b-3.debian.tar.xz' tzdata_2025b-3.debian.tar.xz 126968 SHA256:f74bb46d68823bbe8ca8ec004f1effe0b5dfcb47d405a51804a62cd8dcef2623
```

Other potentially useful URLs:

- https://sources.debian.net/src/tzdata/2025b-3/ (for browsing the source)
- https://sources.debian.net/src/tzdata/2025b-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/tzdata/2025b-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `ucf=3.0052`

Binary Packages:

- `ucf=3.0052`

Licenses: (parsed from: `/usr/share/doc/ucf/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris ucf=3.0052
'http://http.debian.net/debian/pool/main/u/ucf/ucf_3.0052.dsc' ucf_3.0052.dsc 1512 SHA256:9117f54533d23ad74371e91c3038e13b1aa0fabd51a382f47a5af81e9b5ee591
'http://http.debian.net/debian/pool/main/u/ucf/ucf_3.0052.tar.xz' ucf_3.0052.tar.xz 71488 SHA256:94130b4840618a65543ca4c12f4de062081008f42f36d0abfbd75098ebe9a7eb
```

### `dpkg` source package: `unzip=6.0-29`

Binary Packages:

- `unzip=6.0-29`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris unzip=6.0-29
'http://http.debian.net/debian/pool/main/u/unzip/unzip_6.0-29.dsc' unzip_6.0-29.dsc 1464 SHA256:ecc73beeb9a18f354124b87f6713facb726ffd4b732ce7a6e144d073a1e777ae
'http://http.debian.net/debian/pool/main/u/unzip/unzip_6.0.orig.tar.gz' unzip_6.0.orig.tar.gz 1376845 SHA256:036d96991646d0449ed0aa952e4fbe21b476ce994abc276e49d30e686708bd37
'http://http.debian.net/debian/pool/main/u/unzip/unzip_6.0-29.debian.tar.xz' unzip_6.0-29.debian.tar.xz 25876 SHA256:14043e5ea351c02b3bc8676e1e6d20d79b9a690b6d7520e8138ac629cc048417
```

### `dpkg` source package: `util-linux=2.41-5`

Binary Packages:

- `bsdutils=1:2.41-5`
- `libblkid1:amd64=2.41-5`
- `liblastlog2-2:amd64=2.41-5`
- `libmount1:amd64=2.41-5`
- `libsmartcols1:amd64=2.41-5`
- `libuuid1:amd64=2.41-5`
- `login=1:4.16.0-2+really2.41-5`
- `mount=2.41-5`
- `util-linux=2.41-5`

Licenses: (parsed from: `/usr/share/doc/bsdutils/copyright`, `/usr/share/doc/libblkid1/copyright`, `/usr/share/doc/liblastlog2-2/copyright`, `/usr/share/doc/libmount1/copyright`, `/usr/share/doc/libsmartcols1/copyright`, `/usr/share/doc/libuuid1/copyright`, `/usr/share/doc/login/copyright`, `/usr/share/doc/mount/copyright`, `/usr/share/doc/util-linux/copyright`)

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
$ apt-get source -qq --print-uris util-linux=2.41-5
'http://http.debian.net/debian/pool/main/u/util-linux/util-linux_2.41-5.dsc' util-linux_2.41-5.dsc 4942 SHA256:9e84dcc64170262f850aa5fd65902846a1ebf054d556ab5c4ec17fa16b00e628
'http://http.debian.net/debian/pool/main/u/util-linux/util-linux_2.41.orig.tar.xz' util-linux_2.41.orig.tar.xz 9535724 SHA256:81ee93b3cfdfeb7d7c4090cedeba1d7bbce9141fd0b501b686b3fe475ddca4c6
'http://http.debian.net/debian/pool/main/u/util-linux/util-linux_2.41-5.debian.tar.xz' util-linux_2.41-5.debian.tar.xz 120144 SHA256:20ad832160d5ed8de4759ce00652f620ce642ab583c3c1c431b68a15cdba1d07
```

### `dpkg` source package: `vim=2:9.1.1230-2`

Binary Packages:

- `vim-common=2:9.1.1230-2`
- `vim-tiny=2:9.1.1230-2`

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
$ apt-get source -qq --print-uris vim=2:9.1.1230-2
'http://http.debian.net/debian/pool/main/v/vim/vim_9.1.1230-2.dsc' vim_9.1.1230-2.dsc 3230 SHA256:10e96236a45dcf5b1fb3b6a3146072f89b7d4c0af79456b6bfa0688383b41d47
'http://http.debian.net/debian/pool/main/v/vim/vim_9.1.1230.orig.tar.xz' vim_9.1.1230.orig.tar.xz 12331388 SHA256:203640cca8fa97603868ef42f34eeb723803ab15fd141b68b1cba54b7993b2bf
'http://http.debian.net/debian/pool/main/v/vim/vim_9.1.1230-2.debian.tar.xz' vim_9.1.1230-2.debian.tar.xz 191956 SHA256:3f06690fe44914764a260531d71f9bf63d58c9156b86660bd323dd0e7038898d
```

### `dpkg` source package: `wget=1.25.0-2`

Binary Packages:

- `wget=1.25.0-2`

Licenses: (parsed from: `/usr/share/doc/wget/copyright`)

- `GFDL-1.2`
- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris wget=1.25.0-2
'http://http.debian.net/debian/pool/main/w/wget/wget_1.25.0-2.dsc' wget_1.25.0-2.dsc 2251 SHA256:32caf133042db927360a8c35357e4b2877eb83ff0ca144ceb64508947d894f55
'http://http.debian.net/debian/pool/main/w/wget/wget_1.25.0.orig.tar.gz' wget_1.25.0.orig.tar.gz 5263736 SHA256:766e48423e79359ea31e41db9e5c289675947a7fcf2efdcedb726ac9d0da3784
'http://http.debian.net/debian/pool/main/w/wget/wget_1.25.0.orig.tar.gz.asc' wget_1.25.0.orig.tar.gz.asc 854 SHA256:47f0989685931c3df6166061069659bc13a75b221a62041625007fa2dad7411b
'http://http.debian.net/debian/pool/main/w/wget/wget_1.25.0-2.debian.tar.xz' wget_1.25.0-2.debian.tar.xz 27884 SHA256:45d4411e892d12af710ddff536d2daf430031387e336153f5f996cf536487b90
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

- `libxft2:amd64=2.3.6-1+b4`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris xft=2.3.6-1
'http://http.debian.net/debian/pool/main/x/xft/xft_2.3.6-1.dsc' xft_2.3.6-1.dsc 2006 SHA256:252220495bd12fac30d8f1b1994916beaed9c5149138dcc62e230fee17339530
'http://http.debian.net/debian/pool/main/x/xft/xft_2.3.6.orig.tar.gz' xft_2.3.6.orig.tar.gz 447498 SHA256:b7e59f69e0bbabe9438088775f7e5a7c16a572e58b11f9722519385d38192df5
'http://http.debian.net/debian/pool/main/x/xft/xft_2.3.6-1.diff.gz' xft_2.3.6-1.diff.gz 17995 SHA256:9d4c64fc52626134a3f753df88fceaba0cb460bd9b56544f0e42178deca77019
```

### `dpkg` source package: `xorg=1:7.7+24`

Binary Packages:

- `x11-common=1:7.7+24`

Licenses: (parsed from: `/usr/share/doc/x11-common/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris xorg=1:7.7+24
'http://http.debian.net/debian/pool/main/x/xorg/xorg_7.7%2b24.dsc' xorg_7.7+24.dsc 1970 SHA256:3bff9d33df4e1e27c64e777f2fbf68b5f0de93f3985783e953ecaa2d00a636f9
'http://http.debian.net/debian/pool/main/x/xorg/xorg_7.7%2b24.tar.xz' xorg_7.7+24.tar.xz 234100 SHA256:d3a417626799a1a989c34f76a930597e3feee46710b55a334e01a5233cf1daf2
```

### `dpkg` source package: `xxhash=0.8.3-2`

Binary Packages:

- `libxxhash0:amd64=0.8.3-2`

Licenses: (parsed from: `/usr/share/doc/libxxhash0/copyright`)

- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris xxhash=0.8.3-2
'http://http.debian.net/debian/pool/main/x/xxhash/xxhash_0.8.3-2.dsc' xxhash_0.8.3-2.dsc 1969 SHA256:9d1f7aaace7871fbdb8775d756c6eaca84e6ad5d8e9c6ac465b7e0adc06ff90c
'http://http.debian.net/debian/pool/main/x/xxhash/xxhash_0.8.3.orig.tar.gz' xxhash_0.8.3.orig.tar.gz 1147630 SHA256:aae608dfe8213dfd05d909a57718ef82f30722c392344583d3f39050c7f29a80
'http://http.debian.net/debian/pool/main/x/xxhash/xxhash_0.8.3-2.debian.tar.xz' xxhash_0.8.3-2.debian.tar.xz 5144 SHA256:13824bfb2b2367225dfe3090d0ae050614f1c470a47db7232a2e9d4b2b14ad31
```

### `dpkg` source package: `xz-utils=5.8.1-1`

Binary Packages:

- `liblzma-dev:amd64=5.8.1-1`
- `liblzma5:amd64=5.8.1-1`
- `xz-utils=5.8.1-1`

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
$ apt-get source -qq --print-uris xz-utils=5.8.1-1
'http://http.debian.net/debian/pool/main/x/xz-utils/xz-utils_5.8.1-1.dsc' xz-utils_5.8.1-1.dsc 2704 SHA256:a11c19074a9e6b3bd4e566166278d9ebd23915fd0d400fbe6d16eb000d845284
'http://http.debian.net/debian/pool/main/x/xz-utils/xz-utils_5.8.1.orig.tar.xz' xz-utils_5.8.1.orig.tar.xz 1461872 SHA256:0b54f79df85912504de0b14aec7971e3f964491af1812d83447005807513cd9e
'http://http.debian.net/debian/pool/main/x/xz-utils/xz-utils_5.8.1.orig.tar.xz.asc' xz-utils_5.8.1.orig.tar.xz.asc 833 SHA256:4138f4ceca1aa7fd2085fb15a23f6d495d27bca6d3c49c429a8520ea622c27ae
'http://http.debian.net/debian/pool/main/x/xz-utils/xz-utils_5.8.1-1.debian.tar.xz' xz-utils_5.8.1-1.debian.tar.xz 24624 SHA256:a731db6d87e211c7b4e6f1af2fbb5369cd381d8cb0f1e00e8bc30304ae6f00b0
```

### `dpkg` source package: `zip=3.0-15`

Binary Packages:

- `zip=3.0-15`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris zip=3.0-15
'http://http.debian.net/debian/pool/main/z/zip/zip_3.0-15.dsc' zip_3.0-15.dsc 1439 SHA256:1cee3f25b904023d12c46e55628a79328ce21e47e32737358b3cd99233b5bc6d
'http://http.debian.net/debian/pool/main/z/zip/zip_3.0.orig.tar.gz' zip_3.0.orig.tar.gz 1118845 SHA256:f0e8bb1f9b7eb0b01285495a2699df3a4b766784c1765a8f1aeedf63c0806369
'http://http.debian.net/debian/pool/main/z/zip/zip_3.0-15.debian.tar.xz' zip_3.0-15.debian.tar.xz 10692 SHA256:6dc1711c67640e8d1dee867ff53e84387ddb980c40885bd088ac98c330bffce9
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
