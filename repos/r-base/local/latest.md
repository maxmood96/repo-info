# `r-base:4.4.2`

## Docker Metadata

- Image ID: `sha256:242d80afc1301227a452e5055448e7c8f718009c98bb84197a26e473193f84dd`
- Created: `2024-11-01T03:11:38Z`
- Virtual Size: ~ 859.82 Mb  
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

### `dpkg` source package: `apt=2.9.30`

Binary Packages:

- `apt=2.9.30`
- `libapt-pkg7.0:amd64=2.9.30`

Licenses: (parsed from: `/usr/share/doc/apt/copyright`, `/usr/share/doc/libapt-pkg7.0/copyright`)

- `BSD-3-clause`
- `Expat`
- `GPL-2`
- `GPL-2+`
- `curl`

Source:

```console
$ apt-get source -qq --print-uris apt=2.9.30
'http://http.debian.net/debian/pool/main/a/apt/apt_2.9.30.dsc' apt_2.9.30.dsc 3162 SHA256:a422eaa28622926bbbffc93dacac6ce649726d21a513fe9b7c791b7f4352f5ec
'http://http.debian.net/debian/pool/main/a/apt/apt_2.9.30.tar.xz' apt_2.9.30.tar.xz 2402004 SHA256:2f98d5428ce89fc5a26143f6a5a5c7c5ec93beea2d18a6370465bdcd326de82b
```

### `dpkg` source package: `attr=1:2.5.2-2`

Binary Packages:

- `libattr1:amd64=1:2.5.2-2`

Licenses: (parsed from: `/usr/share/doc/libattr1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2+`
- `LGPL-2.1`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/attr/1:2.5.2-2/


### `dpkg` source package: `audit=1:4.0.2-2`

Binary Packages:

- `libaudit-common=1:4.0.2-2`
- `libaudit1:amd64=1:4.0.2-2+b1`

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

### `dpkg` source package: `base-passwd=3.6.6`

Binary Packages:

- `base-passwd=3.6.6`

Licenses: (parsed from: `/usr/share/doc/base-passwd/copyright`)

- `GPL-2`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris base-passwd=3.6.6
'http://http.debian.net/debian/pool/main/b/base-passwd/base-passwd_3.6.6.dsc' base-passwd_3.6.6.dsc 1844 SHA256:c751de08700db6c297f6795982fec0751b4a5a65b645c357e87dfe09eb5e54d0
'http://http.debian.net/debian/pool/main/b/base-passwd/base-passwd_3.6.6.tar.xz' base-passwd_3.6.6.tar.xz 60116 SHA256:cfcb17a5cfb5d7ce53f062b2a30c74ac7f9425af81010d3591aeffc60f269263
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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/bash/5.2.37-1/


### `dpkg` source package: `binutils=2.44-2`

Binary Packages:

- `binutils=2.44-2`
- `binutils-common:amd64=2.44-2`
- `binutils-x86-64-linux-gnu=2.44-2`
- `libbinutils:amd64=2.44-2`
- `libctf-nobfd0:amd64=2.44-2`
- `libctf0:amd64=2.44-2`
- `libgprofng0:amd64=2.44-2`
- `libsframe1:amd64=2.44-2`

Licenses: (parsed from: `/usr/share/doc/binutils/copyright`, `/usr/share/doc/binutils-common/copyright`, `/usr/share/doc/binutils-x86-64-linux-gnu/copyright`, `/usr/share/doc/libbinutils/copyright`, `/usr/share/doc/libctf-nobfd0/copyright`, `/usr/share/doc/libctf0/copyright`, `/usr/share/doc/libgprofng0/copyright`, `/usr/share/doc/libsframe1/copyright`)

- `GFDL`
- `GPL`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris binutils=2.44-2
'http://http.debian.net/debian/pool/main/b/binutils/binutils_2.44-2.dsc' binutils_2.44-2.dsc 11429 SHA256:4b08a4a2f3d2e4a2ebc1fda2d3a9362dfb14ad4bee8a9527cc3210254983a307
'http://http.debian.net/debian/pool/main/b/binutils/binutils_2.44.orig.tar.xz' binutils_2.44.orig.tar.xz 27504768 SHA256:c41a0272424f41bb01bf828e7ffef1b2d59d1788064fd6b5f1d971717e9320b8
'http://http.debian.net/debian/pool/main/b/binutils/binutils_2.44-2.debian.tar.xz' binutils_2.44-2.debian.tar.xz 130224 SHA256:439ae1459747b405c020d57e2d50b1da9c39ee67cfe11eac945b958ef4ee1fa4
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

### `dpkg` source package: `ca-certificates=20241223`

Binary Packages:

- `ca-certificates=20241223`

Licenses: (parsed from: `/usr/share/doc/ca-certificates/copyright`)

- `GPL-2`
- `GPL-2+`
- `MPL-2.0`

Source:

```console
$ apt-get source -qq --print-uris ca-certificates=20241223
'http://http.debian.net/debian/pool/main/c/ca-certificates/ca-certificates_20241223.dsc' ca-certificates_20241223.dsc 1766 SHA256:8b17779dedec18ad64b97ec99dd3b8f10ec06698e73242dbe7b8d992bd803a55
'http://http.debian.net/debian/pool/main/c/ca-certificates/ca-certificates_20241223.tar.xz' ca-certificates_20241223.tar.xz 278044 SHA256:dd8286d0a9dd35c756fea5f1df3fed1510fb891f376903891b003cd9b1ad7e03
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

### `dpkg` source package: `cdebconf=0.277`

Binary Packages:

- `libdebconfclient0:amd64=0.277`

Licenses: (parsed from: `/usr/share/doc/libdebconfclient0/copyright`)

- `BSD-2-Clause`
- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris cdebconf=0.277
'http://http.debian.net/debian/pool/main/c/cdebconf/cdebconf_0.277.dsc' cdebconf_0.277.dsc 2707 SHA256:12afc241658ae9bcbb11d239d06e708fb6138b417b7ce9c31ac642f57fcc4613
'http://http.debian.net/debian/pool/main/c/cdebconf/cdebconf_0.277.tar.xz' cdebconf_0.277.tar.xz 285420 SHA256:93a72ed5c5cab66f1f7439908348aa3bd97c4fa4a47416694e5dc3add2866e7b
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

### `dpkg` source package: `curl=8.12.1-2`

Binary Packages:

- `libcurl4t64:amd64=8.12.1-2`

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
$ apt-get source -qq --print-uris curl=8.12.1-2
'http://http.debian.net/debian/pool/main/c/curl/curl_8.12.1-2.dsc' curl_8.12.1-2.dsc 3252 SHA256:5b5c971eeb3e201afa114e2a869eefed47899abfa01c359a5a46c756cee033e9
'http://http.debian.net/debian/pool/main/c/curl/curl_8.12.1.orig.tar.gz' curl_8.12.1.orig.tar.gz 4181139 SHA256:7b40ea64947e0b440716a4d7f0b7aa56230a5341c8377d7b609649d4aea8dbcf
'http://http.debian.net/debian/pool/main/c/curl/curl_8.12.1.orig.tar.gz.asc' curl_8.12.1.orig.tar.gz.asc 488 SHA256:36d883bcf288d843caf587e7c8fd5feb6223b63420ae93517be6a4db928abe13
'http://http.debian.net/debian/pool/main/c/curl/curl_8.12.1-2.debian.tar.xz' curl_8.12.1-2.debian.tar.xz 52880 SHA256:8248ae609dd27d2e2b3717689b34f5c1c8473b798f59880e1a8230f7a040b22a
```

### `dpkg` source package: `cyrus-sasl2=2.1.28+dfsg1-8`

Binary Packages:

- `libsasl2-2:amd64=2.1.28+dfsg1-8+b1`
- `libsasl2-modules-db:amd64=2.1.28+dfsg1-8+b1`

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

### `dpkg` source package: `debconf=1.5.89`

Binary Packages:

- `debconf=1.5.89`

Licenses: (parsed from: `/usr/share/doc/debconf/copyright`)

- `BSD-2-clause`

Source:

```console
$ apt-get source -qq --print-uris debconf=1.5.89
'http://http.debian.net/debian/pool/main/d/debconf/debconf_1.5.89.dsc' debconf_1.5.89.dsc 2035 SHA256:a3c32a3d878fc5bb72ddc1dadeea6faa423cf7de538e8018188a066bde2504d3
'http://http.debian.net/debian/pool/main/d/debconf/debconf_1.5.89.tar.xz' debconf_1.5.89.tar.xz 574672 SHA256:6af2627425307318d410659104241f9a3c51aef49e57b066950baa4b18ad995f
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

### `dpkg` source package: `diffutils=1:3.10-2`

Binary Packages:

- `diffutils=1:3.10-2`

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
$ apt-get source -qq --print-uris diffutils=1:3.10-2
'http://http.debian.net/debian/pool/main/d/diffutils/diffutils_3.10-2.dsc' diffutils_3.10-2.dsc 1737 SHA256:e66b646eec15edcd185e4cc085deb8fe2925912a632a40cc98017f66ffecbab4
'http://http.debian.net/debian/pool/main/d/diffutils/diffutils_3.10.orig.tar.xz' diffutils_3.10.orig.tar.xz 1624240 SHA256:90e5e93cc724e4ebe12ede80df1634063c7a855692685919bfe60b556c9bd09e
'http://http.debian.net/debian/pool/main/d/diffutils/diffutils_3.10.orig.tar.xz.asc' diffutils_3.10.orig.tar.xz.asc 833 SHA256:a94faf8f1baa04ff220f7b2ccb137c16337284e023ebc4a1d5df475c08d810f7
'http://http.debian.net/debian/pool/main/d/diffutils/diffutils_3.10-2.debian.tar.xz' diffutils_3.10-2.debian.tar.xz 14244 SHA256:8791e985aa96c331a8994484936b0da5b86373648f32feb29d47864f0488d613
```

### `dpkg` source package: `dpkg=1.22.15`

Binary Packages:

- `dpkg=1.22.15`
- `dpkg-dev=1.22.15`
- `libdpkg-perl=1.22.15`

Licenses: (parsed from: `/usr/share/doc/dpkg/copyright`, `/usr/share/doc/dpkg-dev/copyright`, `/usr/share/doc/libdpkg-perl/copyright`)

- `GPL-2`
- `GPL-2+`
- `public-domain-s-s-d`

Source:

```console
$ apt-get source -qq --print-uris dpkg=1.22.15
'http://http.debian.net/debian/pool/main/d/dpkg/dpkg_1.22.15.dsc' dpkg_1.22.15.dsc 3144 SHA256:11a579d5e377da998c208dca8b23d33200d7024e7b8a45d6afc4ff6a71c813f8
'http://http.debian.net/debian/pool/main/d/dpkg/dpkg_1.22.15.tar.xz' dpkg_1.22.15.tar.xz 5739052 SHA256:e312687edaa05de52c47419569f9566bd9438ccc00158eb5e7c1b5bb4c3e88e0
```

### `dpkg` source package: `e2fsprogs=1.47.2-1`

Binary Packages:

- `libcom-err2:amd64=1.47.2-1`

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
$ apt-get source -qq --print-uris e2fsprogs=1.47.2-1
'http://http.debian.net/debian/pool/main/e/e2fsprogs/e2fsprogs_1.47.2-1.dsc' e2fsprogs_1.47.2-1.dsc 3032 SHA256:e6392801ad349ed0217c45684b61db03b33fae940ceb4de23b71a24dab4e1bfc
'http://http.debian.net/debian/pool/main/e/e2fsprogs/e2fsprogs_1.47.2.orig.tar.gz' e2fsprogs_1.47.2.orig.tar.gz 9996725 SHA256:6dcd67ff9d8b13274ba3f088e4318be4f5b71412cd863524423fc49d39a6371f
'http://http.debian.net/debian/pool/main/e/e2fsprogs/e2fsprogs_1.47.2.orig.tar.gz.asc' e2fsprogs_1.47.2.orig.tar.gz.asc 488 SHA256:2063f62a198dd3df21f789c990c2cf9b4a5de24ed55f0b78d86e97e98daffc9d
'http://http.debian.net/debian/pool/main/e/e2fsprogs/e2fsprogs_1.47.2-1.debian.tar.xz' e2fsprogs_1.47.2-1.debian.tar.xz 92348 SHA256:b9d1c79da5b32975f5771a5c487edbd9301729e6e813018209f31e2897a46617
```

### `dpkg` source package: `ed=1.21-1`

Binary Packages:

- `ed=1.21-1`

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
$ apt-get source -qq --print-uris ed=1.21-1
'http://http.debian.net/debian/pool/main/e/ed/ed_1.21-1.dsc' ed_1.21-1.dsc 1818 SHA256:551d6028a4d974947e80d8ddc9ce6aab5d2f301e7bd71308a953cbf66f1b776e
'http://http.debian.net/debian/pool/main/e/ed/ed_1.21.orig.tar.gz' ed_1.21.orig.tar.gz 93889 SHA256:45eacac8f964595cf7fa52ce9a7a699aa15ca1b13db57f06d4cbbf602f7a9a56
'http://http.debian.net/debian/pool/main/e/ed/ed_1.21-1.debian.tar.xz' ed_1.21-1.debian.tar.xz 8684 SHA256:78cc0d8d1526e842a175386ecabec98af514bc538024d345afacc030576367b1
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

### `dpkg` source package: `fontconfig=2.15.0-2`

Binary Packages:

- `fontconfig=2.15.0-2`
- `fontconfig-config=2.15.0-2`
- `libfontconfig1:amd64=2.15.0-2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris fontconfig=2.15.0-2
'http://http.debian.net/debian/pool/main/f/fontconfig/fontconfig_2.15.0-2.dsc' fontconfig_2.15.0-2.dsc 2665 SHA256:65dd1d9e3dc377d1c47800bfdcf92eecac050ed98a745ebcd77ca7d7b1f66497
'http://http.debian.net/debian/pool/main/f/fontconfig/fontconfig_2.15.0.orig.tar.xz' fontconfig_2.15.0.orig.tar.xz 1447820 SHA256:63a0658d0e06e0fa886106452b58ef04f21f58202ea02a94c39de0d3335d7c0e
'http://http.debian.net/debian/pool/main/f/fontconfig/fontconfig_2.15.0-2.debian.tar.xz' fontconfig_2.15.0-2.debian.tar.xz 58960 SHA256:3e7d7e89e2dbc26e419625c2e37b04766861504e3445e38d0480eef2092b6668
```

### `dpkg` source package: `foreign=0.8.88-1`

Binary Packages:

- `r-cran-foreign=0.8.88-1`

Licenses: (parsed from: `/usr/share/doc/r-cran-foreign/copyright`)

- `GPL`
- `GPL `

Source:

```console
$ apt-get source -qq --print-uris foreign=0.8.88-1
'http://http.debian.net/debian/pool/main/f/foreign/foreign_0.8.88-1.dsc' foreign_0.8.88-1.dsc 1838 SHA256:9993a7760ae4f943bc65e8fc837bc681d1f818bd79128ff6a69016ffd497e754
'http://http.debian.net/debian/pool/main/f/foreign/foreign_0.8.88.orig.tar.gz' foreign_0.8.88.orig.tar.gz 365436 SHA256:f0ba33eecad170796964a2491ea0d929d7dd934f8ffb24a5a7cc1bc227f69a81
'http://http.debian.net/debian/pool/main/f/foreign/foreign_0.8.88-1.debian.tar.xz' foreign_0.8.88-1.debian.tar.xz 4412 SHA256:8156f33beb28fe24baf99909de62257b1f6c298bb9c1a1e322900b687d109bb7
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

### `dpkg` source package: `gcc-14=14.2.0-17`

Binary Packages:

- `cpp-14=14.2.0-17`
- `cpp-14-x86-64-linux-gnu=14.2.0-17`
- `g++-14=14.2.0-17`
- `g++-14-x86-64-linux-gnu=14.2.0-17`
- `gcc-14=14.2.0-17`
- `gcc-14-base:amd64=14.2.0-17`
- `gcc-14-x86-64-linux-gnu=14.2.0-17`
- `gfortran-14=14.2.0-17`
- `gfortran-14-x86-64-linux-gnu=14.2.0-17`
- `libasan8:amd64=14.2.0-17`
- `libatomic1:amd64=14.2.0-17`
- `libcc1-0:amd64=14.2.0-17`
- `libgcc-14-dev:amd64=14.2.0-17`
- `libgcc-s1:amd64=14.2.0-17`
- `libgfortran-14-dev:amd64=14.2.0-17`
- `libgfortran5:amd64=14.2.0-17`
- `libgomp1:amd64=14.2.0-17`
- `libhwasan0:amd64=14.2.0-17`
- `libitm1:amd64=14.2.0-17`
- `liblsan0:amd64=14.2.0-17`
- `libquadmath0:amd64=14.2.0-17`
- `libstdc++-14-dev:amd64=14.2.0-17`
- `libstdc++6:amd64=14.2.0-17`
- `libtsan2:amd64=14.2.0-17`
- `libubsan1:amd64=14.2.0-17`

Licenses: (parsed from: `/usr/share/doc/cpp-14/copyright`, `/usr/share/doc/cpp-14-x86-64-linux-gnu/copyright`, `/usr/share/doc/g++-14/copyright`, `/usr/share/doc/g++-14-x86-64-linux-gnu/copyright`, `/usr/share/doc/gcc-14/copyright`, `/usr/share/doc/gcc-14-base/copyright`, `/usr/share/doc/gcc-14-x86-64-linux-gnu/copyright`, `/usr/share/doc/gfortran-14/copyright`, `/usr/share/doc/gfortran-14-x86-64-linux-gnu/copyright`, `/usr/share/doc/libasan8/copyright`, `/usr/share/doc/libatomic1/copyright`, `/usr/share/doc/libcc1-0/copyright`, `/usr/share/doc/libgcc-14-dev/copyright`, `/usr/share/doc/libgcc-s1/copyright`, `/usr/share/doc/libgfortran-14-dev/copyright`, `/usr/share/doc/libgfortran5/copyright`, `/usr/share/doc/libgomp1/copyright`, `/usr/share/doc/libhwasan0/copyright`, `/usr/share/doc/libitm1/copyright`, `/usr/share/doc/liblsan0/copyright`, `/usr/share/doc/libquadmath0/copyright`, `/usr/share/doc/libstdc++-14-dev/copyright`, `/usr/share/doc/libstdc++6/copyright`, `/usr/share/doc/libtsan2/copyright`, `/usr/share/doc/libubsan1/copyright`)

- `Artistic`
- `GFDL-1.2`
- `GPL`
- `GPL-3`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris gcc-14=14.2.0-17
'http://http.debian.net/debian/pool/main/g/gcc-14/gcc-14_14.2.0-17.dsc' gcc-14_14.2.0-17.dsc 47347 SHA256:8a58914cd74bf0eab1a908a4bff2d80a07ab8b8c6dc3790098c4f7c62122d743
'http://http.debian.net/debian/pool/main/g/gcc-14/gcc-14_14.2.0.orig.tar.gz' gcc-14_14.2.0.orig.tar.gz 94299633 SHA256:e162a5ef3f0077ecae598c6556908d2ab80841532df3398072a96a6df6e6aa29
'http://http.debian.net/debian/pool/main/g/gcc-14/gcc-14_14.2.0-17.debian.tar.xz' gcc-14_14.2.0-17.debian.tar.xz 2539600 SHA256:87528ffbf8cc154e06ca74e96e427cb45710edde2e25dfa0f9ac5073fc316b98
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

### `dpkg` source package: `glib2.0=2.83.4-1`

Binary Packages:

- `libglib2.0-0t64:amd64=2.83.4-1`

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
$ apt-get source -qq --print-uris glib2.0=2.83.4-1
'http://http.debian.net/debian/pool/main/g/glib2.0/glib2.0_2.83.4-1.dsc' glib2.0_2.83.4-1.dsc 4812 SHA256:241231f6b9564d9d0999e9e884c456323ae4d7e4ec060e97175379f5fbebd9fe
'http://http.debian.net/debian/pool/main/g/glib2.0/glib2.0_2.83.4.orig-unicode-data.tar.xz' glib2.0_2.83.4.orig-unicode-data.tar.xz 670200 SHA256:32a70bbae91a11aa6fabbea0b64063ef2ad9ec31e4b65289dad8730a3ecaf6be
'http://http.debian.net/debian/pool/main/g/glib2.0/glib2.0_2.83.4.orig.tar.xz' glib2.0_2.83.4.orig.tar.xz 5612896 SHA256:4edc4dc184f46d1220694b7775c5d7c62265c83b0e9632d844da127c181fc391
'http://http.debian.net/debian/pool/main/g/glib2.0/glib2.0_2.83.4-1.debian.tar.xz' glib2.0_2.83.4-1.debian.tar.xz 137612 SHA256:358e2706641e157609f704f0522064dc6bc036745162929e88b402fceaa4950d
```

### `dpkg` source package: `glibc=2.40-7`

Binary Packages:

- `libc-bin=2.40-7`
- `libc-dev-bin=2.40-7`
- `libc-l10n=2.40-7`
- `libc6:amd64=2.40-7`
- `libc6-dev:amd64=2.40-7`
- `locales=2.40-7`

Licenses: (parsed from: `/usr/share/doc/libc-bin/copyright`, `/usr/share/doc/libc-dev-bin/copyright`, `/usr/share/doc/libc-l10n/copyright`, `/usr/share/doc/libc6/copyright`, `/usr/share/doc/libc6-dev/copyright`, `/usr/share/doc/locales/copyright`)

- `BSD-2-clause`
- `BSD-3-clause-Berkeley`
- `BSD-3-clause-Carnegie`
- `BSD-3-clause-Oracle`
- `BSD-3-clause-WIDE`
- `BSD-like-Spencer`
- `BSL-1.0`
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
$ apt-get source -qq --print-uris glibc=2.40-7
'http://http.debian.net/debian/pool/main/g/glibc/glibc_2.40-7.dsc' glibc_2.40-7.dsc 7540 SHA256:2d0784faa6df105ecfad72d02c3c29473aeb925736995562aea3f24346c44719
'http://http.debian.net/debian/pool/main/g/glibc/glibc_2.40.orig.tar.xz' glibc_2.40.orig.tar.xz 19517224 SHA256:0b89b8c058eaa0f1121a814be6196ce2048235b43d95714ce8278fe72c7cc34a
'http://http.debian.net/debian/pool/main/g/glibc/glibc_2.40-7.debian.tar.xz' glibc_2.40-7.debian.tar.xz 458080 SHA256:2ba19a5313db27f43d50c7af511049de4077c66bdb681e792237a77fbd49d4b0
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

- `libharfbuzz0b:amd64=10.2.0-1`

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

### `dpkg` source package: `icu=72.1-6`

Binary Packages:

- `icu-devtools=72.1-6`
- `libicu-dev:amd64=72.1-6`
- `libicu72:amd64=72.1-6`

Licenses: (parsed from: `/usr/share/doc/icu-devtools/copyright`, `/usr/share/doc/libicu-dev/copyright`, `/usr/share/doc/libicu72/copyright`)

- `GPL-3`
- `MIT`

Source:

```console
$ apt-get source -qq --print-uris icu=72.1-6
'http://http.debian.net/debian/pool/main/i/icu/icu_72.1-6.dsc' icu_72.1-6.dsc 2239 SHA256:d9e89e723d0c50e7a051796b9a22ac21ebf68f0972ec978d1490f53d171a81a9
'http://http.debian.net/debian/pool/main/i/icu/icu_72.1.orig.tar.gz' icu_72.1.orig.tar.gz 26303933 SHA256:a2d2d38217092a7ed56635e34467f92f976b370e20182ad325edea6681a71d68
'http://http.debian.net/debian/pool/main/i/icu/icu_72.1.orig.tar.gz.asc' icu_72.1.orig.tar.gz.asc 659 SHA256:87b6ff610d587292cec0444fa8cbbfb12994cb89bade40578f5ba6470de245c7
'http://http.debian.net/debian/pool/main/i/icu/icu_72.1-6.debian.tar.xz' icu_72.1-6.debian.tar.xz 62864 SHA256:f5dd7b585d25be53b4e1da6a3e81924887d022052e0d007b3ca94495883ba32e
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

### `dpkg` source package: `krb5=1.21.3-4`

Binary Packages:

- `libgssapi-krb5-2:amd64=1.21.3-4`
- `libk5crypto3:amd64=1.21.3-4`
- `libkrb5-3:amd64=1.21.3-4`
- `libkrb5support0:amd64=1.21.3-4`

Licenses: (parsed from: `/usr/share/doc/libgssapi-krb5-2/copyright`, `/usr/share/doc/libk5crypto3/copyright`, `/usr/share/doc/libkrb5-3/copyright`, `/usr/share/doc/libkrb5support0/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris krb5=1.21.3-4
'http://http.debian.net/debian/pool/main/k/krb5/krb5_1.21.3-4.dsc' krb5_1.21.3-4.dsc 3377 SHA256:bd43c30b5b99caa717dd6938521d635f9a4eee25fd69cc75bc928d14d0b040f5
'http://http.debian.net/debian/pool/main/k/krb5/krb5_1.21.3.orig.tar.gz' krb5_1.21.3.orig.tar.gz 9136145 SHA256:b7a4cd5ead67fb08b980b21abd150ff7217e85ea320c9ed0c6dadd304840ad35
'http://http.debian.net/debian/pool/main/k/krb5/krb5_1.21.3.orig.tar.gz.asc' krb5_1.21.3.orig.tar.gz.asc 833 SHA256:85047c935fe949ef2e275885451b168557b923dd13a5aab0ef8fe6acd27b94d7
'http://http.debian.net/debian/pool/main/k/krb5/krb5_1.21.3-4.debian.tar.xz' krb5_1.21.3-4.debian.tar.xz 103508 SHA256:80516e0decadae2a2c5aa4f9ac641fd124e76857f2bf6aa1504bb4a1bcc3463c
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

### `dpkg` source package: `libdeflate=1.23-1`

Binary Packages:

- `libdeflate-dev:amd64=1.23-1+b1`
- `libdeflate0:amd64=1.23-1+b1`

Licenses: (parsed from: `/usr/share/doc/libdeflate-dev/copyright`, `/usr/share/doc/libdeflate0/copyright`)

- `Expat`

Source:

```console
$ apt-get source -qq --print-uris libdeflate=1.23-1
'http://http.debian.net/debian/pool/main/libd/libdeflate/libdeflate_1.23-1.dsc' libdeflate_1.23-1.dsc 2214 SHA256:392c29c266379d6f9c9b80ea4d1997305fb5cf64d192474b2191be07cc1edcf4
'http://http.debian.net/debian/pool/main/libd/libdeflate/libdeflate_1.23.orig.tar.gz' libdeflate_1.23.orig.tar.gz 197519 SHA256:1ab18349b9fb0ce8a0ca4116bded725be7dcbfa709e19f6f983d99df1fb8b25f
'http://http.debian.net/debian/pool/main/libd/libdeflate/libdeflate_1.23-1.debian.tar.xz' libdeflate_1.23-1.debian.tar.xz 5536 SHA256:1cf0ab0f0100c2d6b544982854fd4bb71c732be9bd1685af2098baf15d2171b1
```

### `dpkg` source package: `libffi=3.4.7-1`

Binary Packages:

- `libffi8:amd64=3.4.7-1`

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
$ apt-get source -qq --print-uris libffi=3.4.7-1
'http://http.debian.net/debian/pool/main/libf/libffi/libffi_3.4.7-1.dsc' libffi_3.4.7-1.dsc 1948 SHA256:905661067ccb62604691b4fdfffaaa29e0af6fe9994a61cb1e7ad6befc2eb5ae
'http://http.debian.net/debian/pool/main/libf/libffi/libffi_3.4.7.orig.tar.gz' libffi_3.4.7.orig.tar.gz 593636 SHA256:f07c08c9c14977eafb9b5f9277713d91358ec18fc8aaa5607d6790cde90cba12
'http://http.debian.net/debian/pool/main/libf/libffi/libffi_3.4.7-1.debian.tar.xz' libffi_3.4.7-1.debian.tar.xz 10776 SHA256:af65d5c7024e664f71ba2b3a0ff4b72dc885d8d1b75a7d2d596f3d8e36eb3229
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

### `dpkg` source package: `libjpeg-turbo=1:2.1.5-3.1`

Binary Packages:

- `libjpeg-dev:amd64=1:2.1.5-3.1`
- `libjpeg62-turbo:amd64=1:2.1.5-3.1`
- `libjpeg62-turbo-dev:amd64=1:2.1.5-3.1`

Licenses: (parsed from: `/usr/share/doc/libjpeg-dev/copyright`, `/usr/share/doc/libjpeg62-turbo/copyright`, `/usr/share/doc/libjpeg62-turbo-dev/copyright`)

- `BSD-3-clause`
- `BSD-BY-LC-NE`
- `Expat`
- `NTP`
- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris libjpeg-turbo=1:2.1.5-3.1
'http://http.debian.net/debian/pool/main/libj/libjpeg-turbo/libjpeg-turbo_2.1.5-3.1.dsc' libjpeg-turbo_2.1.5-3.1.dsc 2478 SHA256:3b1089198a0f5dd0f6af7a6bbb381c0c710eb1cedf4ae887115a4c8209f081f3
'http://http.debian.net/debian/pool/main/libj/libjpeg-turbo/libjpeg-turbo_2.1.5.orig.tar.gz' libjpeg-turbo_2.1.5.orig.tar.gz 2264471 SHA256:254f3642b04e309fee775123133c6464181addc150499561020312ec61c1bf7c
'http://http.debian.net/debian/pool/main/libj/libjpeg-turbo/libjpeg-turbo_2.1.5-3.1.debian.tar.xz' libjpeg-turbo_2.1.5-3.1.debian.tar.xz 107924 SHA256:ec48689b143c03fbc0a06e116f3916ca319afd8b9f2ef2b1226e245464878856
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

- `libpaper-utils=2.2.5-0.3+b1`
- `libpaper2:amd64=2.2.5-0.3+b1`

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

### `dpkg` source package: `libpng1.6=1.6.47-1`

Binary Packages:

- `libpng-dev:amd64=1.6.47-1`
- `libpng16-16t64:amd64=1.6.47-1`

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
$ apt-get source -qq --print-uris libpng1.6=1.6.47-1
'http://http.debian.net/debian/pool/main/libp/libpng1.6/libpng1.6_1.6.47-1.dsc' libpng1.6_1.6.47-1.dsc 2254 SHA256:e9e28a7505df31d6c26b57727f884445872ec367703d6776b286c5ce82c3087d
'http://http.debian.net/debian/pool/main/libp/libpng1.6/libpng1.6_1.6.47.orig.tar.gz' libpng1.6_1.6.47.orig.tar.gz 1571845 SHA256:631a4c58ea6c10c81f160c4b21fa8495b715d251698ebc2552077e8450f30454
'http://http.debian.net/debian/pool/main/libp/libpng1.6/libpng1.6_1.6.47-1.debian.tar.xz' libpng1.6_1.6.47-1.debian.tar.xz 33136 SHA256:de4d9948d99ebf4669f885ea9d3e4926ff4c745612980effe432c49867ecf5d3
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

### `dpkg` source package: `libselinux=3.7-3.1`

Binary Packages:

- `libselinux1:amd64=3.7-3.1`

Licenses: (parsed from: `/usr/share/doc/libselinux1/copyright`)

- `GPL-2`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/libselinux/3.7-3.1/


### `dpkg` source package: `libsemanage=3.7-2.1`

Binary Packages:

- `libsemanage-common=3.7-2.1`
- `libsemanage2:amd64=3.7-2.1+b1`

Licenses: (parsed from: `/usr/share/doc/libsemanage-common/copyright`, `/usr/share/doc/libsemanage2/copyright`)

- `GPL-2`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris libsemanage=3.7-2.1
'http://deb.debian.org/debian/pool/main/libs/libsemanage/libsemanage_3.7-2.1.dsc' libsemanage_3.7-2.1.dsc 2368 SHA256:7619c31cca56aacabf8bc9eec86db9e8fcf04dfb9568fb7b9e95816c110a6de2
'http://deb.debian.org/debian/pool/main/libs/libsemanage/libsemanage_3.7.orig.tar.gz' libsemanage_3.7.orig.tar.gz 182896 SHA256:e166cae29a417dab008db9ca0874023f353a3017b07693a036ed97487eda35b1
'http://deb.debian.org/debian/pool/main/libs/libsemanage/libsemanage_3.7.orig.tar.gz.asc' libsemanage_3.7.orig.tar.gz.asc 833 SHA256:02981e0224fdf0141fc29b950f7e5aab1653d5fee6dcbf6d6a5ff976e5720cc8
'http://deb.debian.org/debian/pool/main/libs/libsemanage/libsemanage_3.7-2.1.debian.tar.xz' libsemanage_3.7-2.1.debian.tar.xz 36680 SHA256:1625df7a9bcd8fa84a18d0a03bbf739ec6224fdac23c2e500d7c87620b789d17
```

Other potentially useful URLs:

- https://sources.debian.net/src/libsemanage/3.7-2.1/ (for browsing the source)
- https://sources.debian.net/src/libsemanage/3.7-2.1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libsemanage/3.7-2.1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libsepol=3.8-1`

Binary Packages:

- `libsepol2:amd64=3.8-1`

Licenses: (parsed from: `/usr/share/doc/libsepol2/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris libsepol=3.8-1
'http://http.debian.net/debian/pool/main/libs/libsepol/libsepol_3.8-1.dsc' libsepol_3.8-1.dsc 2326 SHA256:81fdb99a1b0e49f63c2f0add06dbbecb1d7aa60fc2b1376db2583b4478c54fdd
'http://http.debian.net/debian/pool/main/libs/libsepol/libsepol_3.8.orig.tar.gz' libsepol_3.8.orig.tar.gz 513780 SHA256:844fbdbf02334b9ce03833ad8a671053f67b4076d72db4f03e0ee2665ec2eb55
'http://http.debian.net/debian/pool/main/libs/libsepol/libsepol_3.8.orig.tar.gz.asc' libsepol_3.8.orig.tar.gz.asc 833 SHA256:64b85abaf972ac089491c6c3593e4b12855a5be9929f62b81f16ead8a22c01ea
'http://http.debian.net/debian/pool/main/libs/libsepol/libsepol_3.8-1.debian.tar.xz' libsepol_3.8-1.debian.tar.xz 32880 SHA256:fb59b99cc866ade5e19a07b1d79652e3331104be4444280d12d6d6e9daba23dd
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

### `dpkg` source package: `libxrender=1:0.9.10-1.1`

Binary Packages:

- `libxrender1:amd64=1:0.9.10-1.1+b4`

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

### `dpkg` source package: `libzstd=1.5.6+dfsg-2`

Binary Packages:

- `libzstd1:amd64=1.5.6+dfsg-2`

Licenses: (parsed from: `/usr/share/doc/libzstd1/copyright`)

- `BSD-3-clause`
- `Expat`
- `GPL-2`
- `zlib`

Source:

```console
$ apt-get source -qq --print-uris libzstd=1.5.6+dfsg-2
'http://http.debian.net/debian/pool/main/libz/libzstd/libzstd_1.5.6%2bdfsg-2.dsc' libzstd_1.5.6+dfsg-2.dsc 2369 SHA256:57f39cddb823019558f0f69f4fb9842a3b8c13cb3f9db8e6d8a7819c1e058b33
'http://http.debian.net/debian/pool/main/libz/libzstd/libzstd_1.5.6%2bdfsg.orig.tar.xz' libzstd_1.5.6+dfsg.orig.tar.xz 1815380 SHA256:b3a60c7059886641830adf32c979be8d211da5d73fd05c7768f86d12d5bccec3
'http://http.debian.net/debian/pool/main/libz/libzstd/libzstd_1.5.6%2bdfsg-2.debian.tar.xz' libzstd_1.5.6+dfsg-2.debian.tar.xz 23088 SHA256:5795e5c490e7087db756be093be00c02987ca7276713b7428e962a73b34294f1
```

### `dpkg` source package: `linux=6.12.16-1`

Binary Packages:

- `linux-libc-dev=6.12.16-1`

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
$ apt-get source -qq --print-uris linux=6.12.16-1
'http://http.debian.net/debian/pool/main/l/linux/linux_6.12.16-1.dsc' linux_6.12.16-1.dsc 206707 SHA256:c20771432603f423f147f0670dde0fb9c4059303e4a45790f02fa70c7a7e96ad
'http://http.debian.net/debian/pool/main/l/linux/linux_6.12.16.orig.tar.xz' linux_6.12.16.orig.tar.xz 150961864 SHA256:5e18ba76fa0c8996e9d70970bb4cd3956b138c63e6344b337637eb18b3d7ddab
'http://http.debian.net/debian/pool/main/l/linux/linux_6.12.16-1.debian.tar.xz' linux_6.12.16-1.debian.tar.xz 1594060 SHA256:6c22dd77f2b6a160bd7373e1e9c6ec8d6a93e190cb3810454f410f15afa10762
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

### `dpkg` source package: `lz4=1.10.0-3`

Binary Packages:

- `liblz4-1:amd64=1.10.0-3`

Licenses: (parsed from: `/usr/share/doc/liblz4-1/copyright`)

- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris lz4=1.10.0-3
'http://http.debian.net/debian/pool/main/l/lz4/lz4_1.10.0-3.dsc' lz4_1.10.0-3.dsc 1941 SHA256:2924972ba64b8f106f2bc56c697700047f8ff3f992265ef5e459219e512311eb
'http://http.debian.net/debian/pool/main/l/lz4/lz4_1.10.0.orig.tar.gz' lz4_1.10.0.orig.tar.gz 387114 SHA256:537512904744b35e232912055ccf8ec66d768639ff3abe5788d90d792ec5f48b
'http://http.debian.net/debian/pool/main/l/lz4/lz4_1.10.0-3.debian.tar.xz' lz4_1.10.0-3.debian.tar.xz 7484 SHA256:15b0f90c7c69c2e7b48edd075dc7df661abda62724adb745098e650abfa52af7
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

### `dpkg` source package: `ncurses=6.5+20250216-1`

Binary Packages:

- `libncurses-dev:amd64=6.5+20250216-1`
- `libncurses6:amd64=6.5+20250216-1`
- `libncursesw6:amd64=6.5+20250216-1`
- `libtinfo6:amd64=6.5+20250216-1`
- `ncurses-base=6.5+20250216-1`
- `ncurses-bin=6.5+20250216-1`

Licenses: (parsed from: `/usr/share/doc/libncurses-dev/copyright`, `/usr/share/doc/libncurses6/copyright`, `/usr/share/doc/libncursesw6/copyright`, `/usr/share/doc/libtinfo6/copyright`, `/usr/share/doc/ncurses-base/copyright`, `/usr/share/doc/ncurses-bin/copyright`)

- `BSD-3-clause`
- `MIT/X11`
- `X11`

Source:

```console
$ apt-get source -qq --print-uris ncurses=6.5+20250216-1
'http://http.debian.net/debian/pool/main/n/ncurses/ncurses_6.5%2b20250216-1.dsc' ncurses_6.5+20250216-1.dsc 3889 SHA256:b083bf77eab32b080b9c9e54693288bfd6f8628e853e14ca8f3c1b42a3768f91
'http://http.debian.net/debian/pool/main/n/ncurses/ncurses_6.5%2b20250216.orig.tar.gz' ncurses_6.5+20250216.orig.tar.gz 3774714 SHA256:b37baafa436e7133bb12a185cb8f60e1599b1947e9f0181c76f3190acf28b6eb
'http://http.debian.net/debian/pool/main/n/ncurses/ncurses_6.5%2b20250216.orig.tar.gz.asc' ncurses_6.5+20250216.orig.tar.gz.asc 729 SHA256:64f4d17923322176c44079f18f170e2164a59d551d7e4e9c1a6e4eebedc5dd6f
'http://http.debian.net/debian/pool/main/n/ncurses/ncurses_6.5%2b20250216-1.debian.tar.xz' ncurses_6.5+20250216-1.debian.tar.xz 49864 SHA256:371782f3db173999e9b2e01d35c361a39d8b9edea04e9dd2af4eaeee28141fe3
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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/nettle/3.10-1/


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

### `dpkg` source package: `nghttp3=1.6.0-2`

Binary Packages:

- `libnghttp3-9:amd64=1.6.0-2`

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
$ apt-get source -qq --print-uris nghttp3=1.6.0-2
'http://http.debian.net/debian/pool/main/n/nghttp3/nghttp3_1.6.0-2.dsc' nghttp3_1.6.0-2.dsc 1355 SHA256:4c12029b593f19c412f0484a05b93d1a7b755b82eb7d0f9d1f49f7092aac1dba
'http://http.debian.net/debian/pool/main/n/nghttp3/nghttp3_1.6.0.orig.tar.xz' nghttp3_1.6.0.orig.tar.xz 392480 SHA256:eaa901954bc494034d3738ef19130de69387d6a3da029044c60d9dae91792a8d
'http://http.debian.net/debian/pool/main/n/nghttp3/nghttp3_1.6.0-2.debian.tar.xz' nghttp3_1.6.0-2.debian.tar.xz 4568 SHA256:a4156b7c2c44d650d15025811b882bcd038ca977710a0b909842ee2e34c92180
```

### `dpkg` source package: `nlme=3.1.167-1`

Binary Packages:

- `r-cran-nlme=3.1.167-1`

Licenses: (parsed from: `/usr/share/doc/r-cran-nlme/copyright`)

- `GPL`
- `GPL `

Source:

```console
$ apt-get source -qq --print-uris nlme=3.1.167-1
'http://http.debian.net/debian/pool/main/n/nlme/nlme_3.1.167-1.dsc' nlme_3.1.167-1.dsc 1840 SHA256:ceffa59f02d27b847f6ce69ec884b6793f2de8347ff17f355e04f09d73e43a2e
'http://http.debian.net/debian/pool/main/n/nlme/nlme_3.1.167.orig.tar.gz' nlme_3.1.167.orig.tar.gz 849418 SHA256:dadc9ccb9b2089a533547437edd256a29a0e059365f11a81e7390bf48f2a8a49
'http://http.debian.net/debian/pool/main/n/nlme/nlme_3.1.167-1.debian.tar.xz' nlme_3.1.167-1.debian.tar.xz 7364 SHA256:ee6759b6de4afab5f1dff29b9982e8ca677ff5c5e09ab69223e78b2a5c939c25
```

### `dpkg` source package: `openblas=0.3.29+ds-2`

Binary Packages:

- `libopenblas0-pthread:amd64=0.3.29+ds-2`

Licenses: (parsed from: `/usr/share/doc/libopenblas0-pthread/copyright`)

- `Apache-2.0`
- `BSD-2-clause`
- `BSD-2-clause-texas`
- `BSD-3-clause`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris openblas=0.3.29+ds-2
'http://http.debian.net/debian/pool/main/o/openblas/openblas_0.3.29%2bds-2.dsc' openblas_0.3.29+ds-2.dsc 4578 SHA256:d72a2ddcf5a73e565d1b870a335695bbc703405e5e799b15eee7800538b22ba7
'http://http.debian.net/debian/pool/main/o/openblas/openblas_0.3.29%2bds.orig.tar.xz' openblas_0.3.29+ds.orig.tar.xz 2208664 SHA256:eb691e2cff83799400da22aa6ab93ebaa346ad317fea578b7ae119e226ce1b01
'http://http.debian.net/debian/pool/main/o/openblas/openblas_0.3.29%2bds-2.debian.tar.xz' openblas_0.3.29+ds-2.debian.tar.xz 25124 SHA256:fc0afe55eb03935cbe929302b708ed08decf2d3966a6fd748d8c918f3f36e188
```

### `dpkg` source package: `openldap=2.6.9+dfsg-1`

Binary Packages:

- `libldap2:amd64=2.6.9+dfsg-1`

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
$ apt-get source -qq --print-uris openldap=2.6.9+dfsg-1
'http://http.debian.net/debian/pool/main/o/openldap/openldap_2.6.9%2bdfsg-1.dsc' openldap_2.6.9+dfsg-1.dsc 3146 SHA256:73ecdf22c5c1a2eb46c8724f418881426585dc7a0719911d1dae6c735795d7aa
'http://http.debian.net/debian/pool/main/o/openldap/openldap_2.6.9%2bdfsg.orig.tar.xz' openldap_2.6.9+dfsg.orig.tar.xz 3753260 SHA256:dfce3ca171b4036b371455314dd35176b700ee988d3b556f156f37088516ef93
'http://http.debian.net/debian/pool/main/o/openldap/openldap_2.6.9%2bdfsg-1.debian.tar.xz' openldap_2.6.9+dfsg-1.debian.tar.xz 171288 SHA256:f12a08b62e8fa13d68e935611b248ce30bf4575e58e874b4906066250821747e
```

### `dpkg` source package: `openssl=3.4.1-1`

Binary Packages:

- `libssl3t64:amd64=3.4.1-1`
- `openssl=3.4.1-1`
- `openssl-provider-legacy=3.4.1-1`

Licenses: (parsed from: `/usr/share/doc/libssl3t64/copyright`, `/usr/share/doc/openssl/copyright`, `/usr/share/doc/openssl-provider-legacy/copyright`)

- `Apache-2.0`
- `Artistic`
- `GPL-1`
- `GPL-1+`

Source:

```console
$ apt-get source -qq --print-uris openssl=3.4.1-1
'http://http.debian.net/debian/pool/main/o/openssl/openssl_3.4.1-1.dsc' openssl_3.4.1-1.dsc 2808 SHA256:850f658197e44d13882b13929b04008c18e2f643ca2781eda180b5f288cb5699
'http://http.debian.net/debian/pool/main/o/openssl/openssl_3.4.1.orig.tar.gz' openssl_3.4.1.orig.tar.gz 18346056 SHA256:002a2d6b30b58bf4bea46c43bdd96365aaf8daa6c428782aa4feee06da197df3
'http://http.debian.net/debian/pool/main/o/openssl/openssl_3.4.1.orig.tar.gz.asc' openssl_3.4.1.orig.tar.gz.asc 833 SHA256:488c2d4051d5d27b1c0f9d21fd717630e0a2e1b82216875b2fb0fceeb0e8ea5a
'http://http.debian.net/debian/pool/main/o/openssl/openssl_3.4.1-1.debian.tar.xz' openssl_3.4.1-1.debian.tar.xz 50548 SHA256:ffd963c2e742809bedb03a9416e64426c585ec987fd6e3b5c3a1eed4d9fc882d
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
'http://http.debian.net/debian/pool/main/p/pam/pam_1.7.0-3.dsc' pam_1.7.0-3.dsc 2210 SHA256:55350f07d07d565e1323282b2ceda48559c335c27ec7199d99c4e803006349d0
'http://http.debian.net/debian/pool/main/p/pam/pam_1.7.0.orig.tar.xz' pam_1.7.0.orig.tar.xz 507824 SHA256:57dcd7a6b966ecd5bbd95e1d11173734691e16b68692fa59661cdae9b13b1697
'http://http.debian.net/debian/pool/main/p/pam/pam_1.7.0.orig.tar.xz.asc' pam_1.7.0.orig.tar.xz.asc 801 SHA256:7a8ea18ec7d9dd1f8cbf9055c32128cbca8241aa63e9fea44d56ce6f0e15e441
'http://http.debian.net/debian/pool/main/p/pam/pam_1.7.0-3.debian.tar.xz' pam_1.7.0-3.debian.tar.xz 132064 SHA256:ff446441cd74a3440b2bd32098d8865e959e497fde167b92ba776d1f354a0946
```

### `dpkg` source package: `pango1.0=1.56.1-1`

Binary Packages:

- `libpango-1.0-0:amd64=1.56.1-1`
- `libpangocairo-1.0-0:amd64=1.56.1-1`
- `libpangoft2-1.0-0:amd64=1.56.1-1`

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
$ apt-get source -qq --print-uris pango1.0=1.56.1-1
'http://http.debian.net/debian/pool/main/p/pango1.0/pango1.0_1.56.1-1.dsc' pango1.0_1.56.1-1.dsc 3690 SHA256:92df1c3706f369ced3116c601c61850bf9417132be24639dbd4d3e9c8ee653ca
'http://http.debian.net/debian/pool/main/p/pango1.0/pango1.0_1.56.1.orig.tar.xz' pango1.0_1.56.1.orig.tar.xz 1882616 SHA256:426be66460c98b8378573e7f6b0b2ab450f6bb6d2ec7cecc33ae81178f246480
'http://http.debian.net/debian/pool/main/p/pango1.0/pango1.0_1.56.1-1.debian.tar.xz' pango1.0_1.56.1-1.debian.tar.xz 43776 SHA256:e7aa37d87b2d7e92ceba963c63a7f1b721556ec672535176b25e17a31fa9b255
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

### `dpkg` source package: `perl=5.40.1-2`

Binary Packages:

- `libperl5.40:amd64=5.40.1-2`
- `perl=5.40.1-2`
- `perl-base=5.40.1-2`
- `perl-modules-5.40=5.40.1-2`

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
$ apt-get source -qq --print-uris perl=5.40.1-2
'http://http.debian.net/debian/pool/main/p/perl/perl_5.40.1-2.dsc' perl_5.40.1-2.dsc 2372 SHA256:a6a3011bb0422d31b6ae42b755ba3c2667e9de2a3d84559fcb70f8db354fe115
'http://http.debian.net/debian/pool/main/p/perl/perl_5.40.1.orig-regen-configure.tar.xz' perl_5.40.1.orig-regen-configure.tar.xz 421056 SHA256:4ea023d08101443f6ed9dc3bdd9bb5f5e08087678dc9e443d195df22da36209a
'http://http.debian.net/debian/pool/main/p/perl/perl_5.40.1.orig.tar.xz' perl_5.40.1.orig.tar.xz 13930924 SHA256:dfa20c2eef2b4af133525610bbb65dd13777ecf998c9c5b1ccf0d308e732ee3f
'http://http.debian.net/debian/pool/main/p/perl/perl_5.40.1-2.debian.tar.xz' perl_5.40.1-2.debian.tar.xz 167424 SHA256:fb98273ae62b5750534640cbfeb018c668538dd69d72c1bedec9f5a8a4999044
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

### `dpkg` source package: `procps=2:4.0.4-7`

Binary Packages:

- `libproc2-0:amd64=2:4.0.4-7`
- `procps=2:4.0.4-7`

Licenses: (parsed from: `/usr/share/doc/libproc2-0/copyright`, `/usr/share/doc/procps/copyright`)

- `GPL-2`
- `GPL-2.0+`
- `LGPL-2`
- `LGPL-2.0+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris procps=2:4.0.4-7
'http://http.debian.net/debian/pool/main/p/procps/procps_4.0.4-7.dsc' procps_4.0.4-7.dsc 2124 SHA256:460a4816eb0457adb04d059bd6950a7a94b0847859560ff5d02d703df5c00bc2
'http://http.debian.net/debian/pool/main/p/procps/procps_4.0.4.orig.tar.xz' procps_4.0.4.orig.tar.xz 1401540 SHA256:22870d6feb2478adb617ce4f09a787addaf2d260c5a8aa7b17d889a962c5e42e
'http://http.debian.net/debian/pool/main/p/procps/procps_4.0.4-7.debian.tar.xz' procps_4.0.4-7.debian.tar.xz 29964 SHA256:460a5fb98ad62b5a0256c180b3246099f5c3cb73c97b235aeafaa30fef561015
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

### `dpkg` source package: `r-cran-mass=7.3-64-1`

Binary Packages:

- `r-cran-mass=7.3-64-1`

Licenses: (parsed from: `/usr/share/doc/r-cran-mass/copyright`)

- `GPL-2`
- `GPL-2 | GPL-3`

Source:

```console
$ apt-get source -qq --print-uris r-cran-mass=7.3-64-1
'http://http.debian.net/debian/pool/main/r/r-cran-mass/r-cran-mass_7.3-64-1.dsc' r-cran-mass_7.3-64-1.dsc 1851 SHA256:261131c3b9cbc6ef3fc171922366461c2142856b58f14e0924896c80d92cd44c
'http://http.debian.net/debian/pool/main/r/r-cran-mass/r-cran-mass_7.3-64.orig.tar.gz' r-cran-mass_7.3-64.orig.tar.gz 510135 SHA256:bf313725b97fcf69fed86d1f70889ea612bfa9095f36aab47181cc76a8cdbb7f
'http://http.debian.net/debian/pool/main/r/r-cran-mass/r-cran-mass_7.3-64-1.debian.tar.xz' r-cran-mass_7.3-64-1.debian.tar.xz 6644 SHA256:5d7daf383681ed9995228a9f129011cd21267c17170cbcba3d6c112cf75a7f88
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

### `dpkg` source package: `rmatrix=1.7-2-1`

Binary Packages:

- `r-cran-matrix=1.7-2-1`

Licenses: (parsed from: `/usr/share/doc/r-cran-matrix/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris rmatrix=1.7-2-1
'http://http.debian.net/debian/pool/main/r/rmatrix/rmatrix_1.7-2-1.dsc' rmatrix_1.7-2-1.dsc 1860 SHA256:54daf03dbc09628fcdf1059e497357d640dfe05d5e747f4b0d22f7bc69c34254
'http://http.debian.net/debian/pool/main/r/rmatrix/rmatrix_1.7-2.orig.tar.gz' rmatrix_1.7-2.orig.tar.gz 2484712 SHA256:7f019d9ae5d69b799c929cacc3b17e06b09fa65e2db9e007be4753751e96c650
'http://http.debian.net/debian/pool/main/r/rmatrix/rmatrix_1.7-2-1.debian.tar.xz' rmatrix_1.7-2-1.debian.tar.xz 6104 SHA256:d5627ea57bb4ec3cdf1ac4836d4cf7494905c033c0e626fffd62c99d85a9282a
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

### `dpkg` source package: `rust-sequoia-sqv=1.2.1-6`

Binary Packages:

- `sqv=1.2.1-6+b1`

Licenses: (parsed from: `/usr/share/doc/sqv/copyright`)

- `GPL-2`
- `GPL-2.0-or-later`

Source:

```console
$ apt-get source -qq --print-uris rust-sequoia-sqv=1.2.1-6
'http://http.debian.net/debian/pool/main/r/rust-sequoia-sqv/rust-sequoia-sqv_1.2.1-6.dsc' rust-sequoia-sqv_1.2.1-6.dsc 2682 SHA256:8d5040a560ba35e066159a6a078dacedf1bd3b44b63fe1d3db1f6f3b7c00ed96
'http://http.debian.net/debian/pool/main/r/rust-sequoia-sqv/rust-sequoia-sqv_1.2.1.orig.tar.gz' rust-sequoia-sqv_1.2.1.orig.tar.gz 56163 SHA256:824eda88393780802dd75e466d6b18c433d8ba947bd8cd6a6385f22500533f5a
'http://http.debian.net/debian/pool/main/r/rust-sequoia-sqv/rust-sequoia-sqv_1.2.1-6.debian.tar.xz' rust-sequoia-sqv_1.2.1-6.debian.tar.xz 3708 SHA256:7f0daa814838476ec39ec80315c4bafc3e017367a618b510c3a484f6583953b6
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

### `dpkg` source package: `shadow=1:4.17.2-5`

Binary Packages:

- `login.defs=1:4.17.2-5`
- `passwd=1:4.17.2-5`

Licenses: (parsed from: `/usr/share/doc/login.defs/copyright`, `/usr/share/doc/passwd/copyright`)

- `BSD-3-clause`
- `GPL-1`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris shadow=1:4.17.2-5
'http://deb.debian.org/debian/pool/main/s/shadow/shadow_4.17.2-5.dsc' shadow_4.17.2-5.dsc 2851 SHA256:8263a9ce7fe7eaa621305c52a1a2bb39da52bfd259d58b40a88f9839323cdabe
'http://deb.debian.org/debian/pool/main/s/shadow/shadow_4.17.2.orig.tar.xz' shadow_4.17.2.orig.tar.xz 2320492 SHA256:a21cf0d34bffc4314cede01cff258689174fab30ca494ae8f45784d3d56c9849
'http://deb.debian.org/debian/pool/main/s/shadow/shadow_4.17.2.orig.tar.xz.asc' shadow_4.17.2.orig.tar.xz.asc 488 SHA256:008f23f86b1dd9c8b7116f28cf03d0dfef696e79bf5a8213aa083bc13a48c997
'http://deb.debian.org/debian/pool/main/s/shadow/shadow_4.17.2-5.debian.tar.xz' shadow_4.17.2-5.debian.tar.xz 168988 SHA256:20a3d23ec624c15892aaeccb1693dfed0470b63834c0ea870881c46d5f048f1d
```

Other potentially useful URLs:

- https://sources.debian.net/src/shadow/1:4.17.2-5/ (for browsing the source)
- https://sources.debian.net/src/shadow/1:4.17.2-5/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/shadow/1:4.17.2-5/ (for access to the source package after it no longer exists in the archive)

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

### `dpkg` source package: `systemd=257.3-1`

Binary Packages:

- `libsystemd0:amd64=257.3-1`
- `libudev1:amd64=257.3-1`

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
$ apt-get source -qq --print-uris systemd=257.3-1
'http://http.debian.net/debian/pool/main/s/systemd/systemd_257.3-1.dsc' systemd_257.3-1.dsc 8447 SHA256:76ef721ace1af712acfa1e1aeca96ab71ce2ab40aa0f135d46ec0ec32cc09bce
'http://http.debian.net/debian/pool/main/s/systemd/systemd_257.3.orig.tar.gz' systemd_257.3.orig.tar.gz 16227011 SHA256:99365d1a01bcc59a659ab59c7bae9c34f7eb2998f1656ee0a4aae05312eacdc9
'http://http.debian.net/debian/pool/main/s/systemd/systemd_257.3-1.debian.tar.xz' systemd_257.3-1.debian.tar.xz 178716 SHA256:e83d941f4162f6953ed3a9409258218bd98e9daa1f9b3d30267238011c29ddb7
```

### `dpkg` source package: `sysvinit=3.14-1`

Binary Packages:

- `sysvinit-utils=3.14-1`

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
$ apt-get source -qq --print-uris sysvinit=3.14-1
'http://deb.debian.org/debian/pool/main/s/sysvinit/sysvinit_3.14-1.dsc' sysvinit_3.14-1.dsc 2361 SHA256:5dd2c98a1abdb0857c7b870b29a01741a26649c77eb855c3dc8a9d1fbb8ca74b
'http://deb.debian.org/debian/pool/main/s/sysvinit/sysvinit_3.14.orig.tar.gz' sysvinit_3.14.orig.tar.gz 516357 SHA256:4e90a148707cf64113fc97343c053f9c0c9589551936b053999dcc69731f295f
'http://deb.debian.org/debian/pool/main/s/sysvinit/sysvinit_3.14-1.debian.tar.xz' sysvinit_3.14-1.debian.tar.xz 120812 SHA256:c23c9bfbae02404ea54f21811af12f635518fedb01806aa888f718aa8b9a7540
```

Other potentially useful URLs:

- https://sources.debian.net/src/sysvinit/3.14-1/ (for browsing the source)
- https://sources.debian.net/src/sysvinit/3.14-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/sysvinit/3.14-1/ (for access to the source package after it no longer exists in the archive)

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

### `dpkg` source package: `tzdata=2025a-2`

Binary Packages:

- `tzdata=2025a-2`

Licenses: (parsed from: `/usr/share/doc/tzdata/copyright`)

- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris tzdata=2025a-2
'http://http.debian.net/debian/pool/main/t/tzdata/tzdata_2025a-2.dsc' tzdata_2025a-2.dsc 2434 SHA256:d771f8a890290e321afbc2ea76a0ebff0f790e952dbda548dea935c7840cfac5
'http://http.debian.net/debian/pool/main/t/tzdata/tzdata_2025a.orig.tar.gz' tzdata_2025a.orig.tar.gz 462943 SHA256:4d5fcbc72c7c450ebfe0b659bd0f1c02fbf52fd7f517a9ea13fe71c21eb5f0d0
'http://http.debian.net/debian/pool/main/t/tzdata/tzdata_2025a.orig.tar.gz.asc' tzdata_2025a.orig.tar.gz.asc 833 SHA256:ed1d0264162b11f16a1c968adc413ed410458477ac094b4a2adc3357a069b2a2
'http://http.debian.net/debian/pool/main/t/tzdata/tzdata_2025a-2.debian.tar.xz' tzdata_2025a-2.debian.tar.xz 126520 SHA256:379aa6bd63cb804f2487b41e12fd6264e5541ba481f27a2438d34540cc9cefa9
```

### `dpkg` source package: `ucf=3.0050`

Binary Packages:

- `ucf=3.0050`

Licenses: (parsed from: `/usr/share/doc/ucf/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris ucf=3.0050
'http://http.debian.net/debian/pool/main/u/ucf/ucf_3.0050.dsc' ucf_3.0050.dsc 1512 SHA256:0c119d0ee69b4de8650726488485aec2954d52fada2df244cb7955a53485129f
'http://http.debian.net/debian/pool/main/u/ucf/ucf_3.0050.tar.xz' ucf_3.0050.tar.xz 70764 SHA256:60880652e8a25955008b566aba010798a9665fff72962b512511a7fd96a911a2
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

### `dpkg` source package: `util-linux=2.40.4-3`

Binary Packages:

- `bsdutils=1:2.40.4-3`
- `libblkid1:amd64=2.40.4-3`
- `libmount1:amd64=2.40.4-3`
- `libsmartcols1:amd64=2.40.4-3`
- `libuuid1:amd64=2.40.4-3`
- `login=1:4.16.0-2+really2.40.4-3`
- `mount=2.40.4-3`
- `util-linux=2.40.4-3`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/util-linux/2.40.4-3/


### `dpkg` source package: `vim=2:9.1.1113-1`

Binary Packages:

- `vim-common=2:9.1.1113-1`
- `vim-tiny=2:9.1.1113-1`

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
$ apt-get source -qq --print-uris vim=2:9.1.1113-1
'http://http.debian.net/debian/pool/main/v/vim/vim_9.1.1113-1.dsc' vim_9.1.1113-1.dsc 3230 SHA256:16ea6c861083e9135805b8506f3a9fba2ca5f8ad7e959b36fdaf6b153c8060d0
'http://http.debian.net/debian/pool/main/v/vim/vim_9.1.1113.orig.tar.xz' vim_9.1.1113.orig.tar.xz 12238172 SHA256:05c658958880af5d37506e96c125e43b3a21c7ee2cb905d9370a5b1b9d4640dc
'http://http.debian.net/debian/pool/main/v/vim/vim_9.1.1113-1.debian.tar.xz' vim_9.1.1113-1.debian.tar.xz 191084 SHA256:dce5f877ba2887f0ed81b1700042f939f2836269a6d20ad7991ca8f92a0c2bed
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
