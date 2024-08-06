# `buildpack-deps:sid`

## Docker Metadata

- Image ID: `sha256:4adea96ff5bbbe3d2cf37062cdb0220b675cd88975454fab80ca974dbc85ab5c`
- Created: `2024-07-23T06:11:00.08989968Z`
- Virtual Size: ~ 947.20 Mb  
  (total size of all layers on-disk)
- Arch: `linux`/`amd64`
- Command: `["bash"]`
- Environment:
  - `PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin`

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
'http://deb.debian.org/debian/pool/main/a/acl/acl_2.3.2-2.dsc' acl_2.3.2-2.dsc 2604 SHA256:1f42130ccb5442fe2db2aee1dcc03c51a31512dd2519a38e8fc9270c5abbc807
'http://deb.debian.org/debian/pool/main/a/acl/acl_2.3.2.orig.tar.xz' acl_2.3.2.orig.tar.xz 371680 SHA256:97203a72cae99ab89a067fe2210c1cbf052bc492b479eca7d226d9830883b0bd
'http://deb.debian.org/debian/pool/main/a/acl/acl_2.3.2.orig.tar.xz.asc' acl_2.3.2.orig.tar.xz.asc 833 SHA256:184c6a903490885a096095db67b433a04542c6569f167cbe8115268c0f227273
'http://deb.debian.org/debian/pool/main/a/acl/acl_2.3.2-2.debian.tar.xz' acl_2.3.2-2.debian.tar.xz 24296 SHA256:e27b6e194c0a7554595d76f96acdceb800631bdc46c36457b73bc7e4a0c5f2ee
```

Other potentially useful URLs:

- https://sources.debian.net/src/acl/2.3.2-2/ (for browsing the source)
- https://sources.debian.net/src/acl/2.3.2-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/acl/2.3.2-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `adduser=3.137`

Binary Packages:

- `adduser=3.137`

Licenses: (parsed from: `/usr/share/doc/adduser/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris adduser=3.137
'http://deb.debian.org/debian/pool/main/a/adduser/adduser_3.137.dsc' adduser_3.137.dsc 1671 SHA256:e4be6fbfa9db7ca7054a1c31dd2f1503340187b547112c960f2482ce3642f837
'http://deb.debian.org/debian/pool/main/a/adduser/adduser_3.137.tar.xz' adduser_3.137.tar.xz 279192 SHA256:229a61803664c2850f7d8d93e6650cd0b340ea3bbd1b954271719679ea3b0dd0
```

Other potentially useful URLs:

- https://sources.debian.net/src/adduser/3.137/ (for browsing the source)
- https://sources.debian.net/src/adduser/3.137/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/adduser/3.137/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `apr-util=1.6.3-2`

Binary Packages:

- `libaprutil1t64:amd64=1.6.3-2`

Licenses: (parsed from: `/usr/share/doc/libaprutil1t64/copyright`)

- `Apache-2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/apr-util/1.6.3-2/


### `dpkg` source package: `apr=1.7.2-3.2`

Binary Packages:

- `libapr1t64:amd64=1.7.2-3.2`

Licenses: (parsed from: `/usr/share/doc/libapr1t64/copyright`)

- `Apache-2.0`

Source:

```console
$ apt-get source -qq --print-uris apr=1.7.2-3.2
'http://deb.debian.org/debian/pool/main/a/apr/apr_1.7.2-3.2.dsc' apr_1.7.2-3.2.dsc 2323 SHA256:e6beb42d176608fce031f271017b650658c633f5e31080047541b9549ee2715a
'http://deb.debian.org/debian/pool/main/a/apr/apr_1.7.2.orig.tar.bz2' apr_1.7.2.orig.tar.bz2 890218 SHA256:75e77cc86776c030c0a5c408dfbd0bf2a0b75eed5351e52d5439fa1e5509a43e
'http://deb.debian.org/debian/pool/main/a/apr/apr_1.7.2.orig.tar.bz2.asc' apr_1.7.2.orig.tar.bz2.asc 833 SHA256:3e45e804041cfd112d3710db11424e861a6f96e5b8908fcb73bc558f7d480f37
'http://deb.debian.org/debian/pool/main/a/apr/apr_1.7.2-3.2.debian.tar.xz' apr_1.7.2-3.2.debian.tar.xz 54572 SHA256:0758509e6cda3f6f3f367e84e8ef1c05d58450936f78f4163f22b0df8a663a6c
```

Other potentially useful URLs:

- https://sources.debian.net/src/apr/1.7.2-3.2/ (for browsing the source)
- https://sources.debian.net/src/apr/1.7.2-3.2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/apr/1.7.2-3.2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `apt=2.9.6`

Binary Packages:

- `apt=2.9.6`
- `libapt-pkg6.0t64:amd64=2.9.6`

Licenses: (parsed from: `/usr/share/doc/apt/copyright`, `/usr/share/doc/libapt-pkg6.0t64/copyright`)

- `BSD-3-clause`
- `Expat`
- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/apt/2.9.6/


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
'http://deb.debian.org/debian/pool/main/a/attr/attr_2.5.2-1.dsc' attr_2.5.2-1.dsc 2477 SHA256:5c14953fc436d6c4ba6dd4a00b2f82a923d5745cc2c993a630e50d9cabaeca0b
'http://deb.debian.org/debian/pool/main/a/attr/attr_2.5.2.orig.tar.xz' attr_2.5.2.orig.tar.xz 334180 SHA256:f2e97b0ab7ce293681ab701915766190d607a1dba7fae8a718138150b700a70b
'http://deb.debian.org/debian/pool/main/a/attr/attr_2.5.2.orig.tar.xz.asc' attr_2.5.2.orig.tar.xz.asc 833 SHA256:eeac729088d3c6379e91b7596cb3582e46b047c47f0fa3c5c77f9c9e84dc3a4c
'http://deb.debian.org/debian/pool/main/a/attr/attr_2.5.2-1.debian.tar.xz' attr_2.5.2-1.debian.tar.xz 25848 SHA256:b4d0670ea47811670bb619252973c7fb186e54b28bd5f2ac3c1a34d6fd089741
```

Other potentially useful URLs:

- https://sources.debian.net/src/attr/1:2.5.2-1/ (for browsing the source)
- https://sources.debian.net/src/attr/1:2.5.2-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/attr/1:2.5.2-1/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/a/audit/audit_3.1.2-4.dsc' audit_3.1.2-4.dsc 2408 SHA256:2c3e056802722d320d9bc37bb47e1999d2878772076c7f28621404fa8f07d871
'http://deb.debian.org/debian/pool/main/a/audit/audit_3.1.2.orig.tar.gz' audit_3.1.2.orig.tar.gz 1219860 SHA256:c0b1792d1f0a88c6f1828710509cbb987059fc68712c97669ca90eae103d287d
'http://deb.debian.org/debian/pool/main/a/audit/audit_3.1.2-4.debian.tar.xz' audit_3.1.2-4.debian.tar.xz 18724 SHA256:fa0f2f46093f2b76c960f08c66605a10c0de646383366dc26c32304676324ec6
```

Other potentially useful URLs:

- https://sources.debian.net/src/audit/1:3.1.2-4/ (for browsing the source)
- https://sources.debian.net/src/audit/1:3.1.2-4/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/audit/1:3.1.2-4/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `autoconf=2.71-3`

Binary Packages:

- `autoconf=2.71-3`

Licenses: (parsed from: `/usr/share/doc/autoconf/copyright`)

- `GFDL-1.3`
- `GFDL-1.3+`
- `GPL-2`
- `GPL-2+`
- `GPL-2+ with Autoconf exception`
- `GPL-3`
- `GPL-3+`
- `GPL-3+ with Autoconf exception`
- `GPL-3+ with Texinfo exception`
- `MIT-X-Consortium`
- `no-modification`
- `other`
- `permissive`
- `permissive-long-disclaimer`
- `permissive-short-disclaimer`
- `permissive-without-disclaimer`
- `permissive-without-notices-or-disclaimer`

Source:

```console
$ apt-get source -qq --print-uris autoconf=2.71-3
'http://deb.debian.org/debian/pool/main/a/autoconf/autoconf_2.71-3.dsc' autoconf_2.71-3.dsc 1988 SHA256:2230ca8950e9b1abeeba54844c9e8184891fa2474a101c25f5d125bdacb92ef2
'http://deb.debian.org/debian/pool/main/a/autoconf/autoconf_2.71.orig.tar.gz' autoconf_2.71.orig.tar.gz 2003781 SHA256:431075ad0bf529ef13cb41e9042c542381103e80015686222b8a9d4abef42a1c
'http://deb.debian.org/debian/pool/main/a/autoconf/autoconf_2.71-3.debian.tar.xz' autoconf_2.71-3.debian.tar.xz 23896 SHA256:3c12ade6e26e8ccacd8e35de3eb93a1fcf360b02364cbe4690b958a749daf4d7
```

Other potentially useful URLs:

- https://sources.debian.net/src/autoconf/2.71-3/ (for browsing the source)
- https://sources.debian.net/src/autoconf/2.71-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/autoconf/2.71-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `automake-1.16=1:1.16.5-1.3`

Binary Packages:

- `automake=1:1.16.5-1.3`

Licenses: (parsed from: `/usr/share/doc/automake/copyright`)

- `GFDL-1.3`
- `GFDL-NIV-1.3+`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `permissive`

Source:

```console
$ apt-get source -qq --print-uris automake-1.16=1:1.16.5-1.3
'http://deb.debian.org/debian/pool/main/a/automake-1.16/automake-1.16_1.16.5-1.3.dsc' automake-1.16_1.16.5-1.3.dsc 1973 SHA256:88bb6aad124dc9c8f8f37910f66bf79f19e1c4a1e5c69860e3e9005d2adc4d8d
'http://deb.debian.org/debian/pool/main/a/automake-1.16/automake-1.16_1.16.5.orig.tar.xz' automake-1.16_1.16.5.orig.tar.xz 1601740 SHA256:f01d58cd6d9d77fbdca9eb4bbd5ead1988228fdb73d6f7a201f5f8d6b118b469
'http://deb.debian.org/debian/pool/main/a/automake-1.16/automake-1.16_1.16.5.orig.tar.xz.asc' automake-1.16_1.16.5.orig.tar.xz.asc 833 SHA256:3a161ab65921eed55e1a94251d97c8451d4ba3431b55ca560e95a951b5f1d73a
'http://deb.debian.org/debian/pool/main/a/automake-1.16/automake-1.16_1.16.5-1.3.debian.tar.xz' automake-1.16_1.16.5-1.3.debian.tar.xz 14164 SHA256:357d34b964943f5c46f518e3a7ddaa9342de76f1a01bac83039dc338ca84d421
```

Other potentially useful URLs:

- https://sources.debian.net/src/automake-1.16/1:1.16.5-1.3/ (for browsing the source)
- https://sources.debian.net/src/automake-1.16/1:1.16.5-1.3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/automake-1.16/1:1.16.5-1.3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `autotools-dev=20220109.1`

Binary Packages:

- `autotools-dev=20220109.1`

Licenses: (parsed from: `/usr/share/doc/autotools-dev/copyright`)

- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris autotools-dev=20220109.1
'http://deb.debian.org/debian/pool/main/a/autotools-dev/autotools-dev_20220109.1.dsc' autotools-dev_20220109.1.dsc 1661 SHA256:f9ccc67437ff52a7882d6b91e7ca8bf0a316c0c1452093992bd5c5fc3b29c090
'http://deb.debian.org/debian/pool/main/a/autotools-dev/autotools-dev_20220109.1.tar.xz' autotools-dev_20220109.1.tar.xz 87340 SHA256:8b05e5ad56cd7d9a15e9b2931eb429b6324bb89f1b46de3baf3651286dead8c1
```

Other potentially useful URLs:

- https://sources.debian.net/src/autotools-dev/20220109.1/ (for browsing the source)
- https://sources.debian.net/src/autotools-dev/20220109.1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/autotools-dev/20220109.1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `base-files=13.3`

Binary Packages:

- `base-files=13.3`

Licenses: (parsed from: `/usr/share/doc/base-files/copyright`)

- `GPL`
- `GPL-2+`
- `verbatim`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/base-files/13.3/


### `dpkg` source package: `base-passwd=3.6.4`

Binary Packages:

- `base-passwd=3.6.4`

Licenses: (parsed from: `/usr/share/doc/base-passwd/copyright`)

- `GPL-2`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris base-passwd=3.6.4
'http://deb.debian.org/debian/pool/main/b/base-passwd/base-passwd_3.6.4.dsc' base-passwd_3.6.4.dsc 1762 SHA256:83d6855b38a0ab900d28d14bc3a0c0b97c60d5461143e51ccc2b0f8f7ea92cc8
'http://deb.debian.org/debian/pool/main/b/base-passwd/base-passwd_3.6.4.tar.xz' base-passwd_3.6.4.tar.xz 58420 SHA256:4b5232c5910932215b87bbde6f3c6c9a97021fe7902bd837b1ede8cc0be84a65
```

Other potentially useful URLs:

- https://sources.debian.net/src/base-passwd/3.6.4/ (for browsing the source)
- https://sources.debian.net/src/base-passwd/3.6.4/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/base-passwd/3.6.4/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `bash=5.2.21-2.1`

Binary Packages:

- `bash=5.2.21-2.1`

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
'http://deb.debian.org/debian/pool/main/b/bash/bash_5.2.21-2.1.dsc' bash_5.2.21-2.1.dsc 2278 SHA256:97801c8f716396cd88cf8b69da3b6ea70f2b3ef6f9415df40e836d373feba536
'http://deb.debian.org/debian/pool/main/b/bash/bash_5.2.21.orig.tar.xz' bash_5.2.21.orig.tar.xz 5598816 SHA256:ec21ab4efd6bd7a6e2802fbda622b81bfc43a8095d721234d4bf075797683014
'http://deb.debian.org/debian/pool/main/b/bash/bash_5.2.21-2.1.debian.tar.xz' bash_5.2.21-2.1.debian.tar.xz 87940 SHA256:7452fd5408bd8415eee5e561a83d318972a584f10911818f8a8dd30e4f5acacd
```

Other potentially useful URLs:

- https://sources.debian.net/src/bash/5.2.21-2.1/ (for browsing the source)
- https://sources.debian.net/src/bash/5.2.21-2.1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/bash/5.2.21-2.1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `binutils=2.42.90.20240720-2`

Binary Packages:

- `binutils=2.42.90.20240720-2`
- `binutils-common:amd64=2.42.90.20240720-2`
- `binutils-x86-64-linux-gnu=2.42.90.20240720-2`
- `libbinutils:amd64=2.42.90.20240720-2`
- `libctf-nobfd0:amd64=2.42.90.20240720-2`
- `libctf0:amd64=2.42.90.20240720-2`
- `libgprofng0:amd64=2.42.90.20240720-2`
- `libsframe1:amd64=2.42.90.20240720-2`

Licenses: (parsed from: `/usr/share/doc/binutils/copyright`, `/usr/share/doc/binutils-common/copyright`, `/usr/share/doc/binutils-x86-64-linux-gnu/copyright`, `/usr/share/doc/libbinutils/copyright`, `/usr/share/doc/libctf-nobfd0/copyright`, `/usr/share/doc/libctf0/copyright`, `/usr/share/doc/libgprofng0/copyright`, `/usr/share/doc/libsframe1/copyright`)

- `GFDL`
- `GPL`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris binutils=2.42.90.20240720-2
'http://deb.debian.org/debian/pool/main/b/binutils/binutils_2.42.90.20240720-2.dsc' binutils_2.42.90.20240720-2.dsc 12646 SHA256:cab6e44ec9584960eb9f576189dc55e89fd174683af9ca0e72c39f78e1a6f468
'http://deb.debian.org/debian/pool/main/b/binutils/binutils_2.42.90.20240720.orig.tar.xz' binutils_2.42.90.20240720.orig.tar.xz 24093004 SHA256:a76aab99156873ed4527a74a18883079b581bc493cd409b3605f7e5270053a7f
'http://deb.debian.org/debian/pool/main/b/binutils/binutils_2.42.90.20240720-2.debian.tar.xz' binutils_2.42.90.20240720-2.debian.tar.xz 122420 SHA256:7851213ebdaba7530105e510da1b87f45a7479a3dcf178738d15e704fe071e91
```

Other potentially useful URLs:

- https://sources.debian.net/src/binutils/2.42.90.20240720-2/ (for browsing the source)
- https://sources.debian.net/src/binutils/2.42.90.20240720-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/binutils/2.42.90.20240720-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `brotli=1.1.0-2`

Binary Packages:

- `libbrotli-dev:amd64=1.1.0-2+b4`
- `libbrotli1:amd64=1.1.0-2+b4`

Licenses: (parsed from: `/usr/share/doc/libbrotli-dev/copyright`, `/usr/share/doc/libbrotli1/copyright`)

- `MIT`

Source:

```console
$ apt-get source -qq --print-uris brotli=1.1.0-2
'http://deb.debian.org/debian/pool/main/b/brotli/brotli_1.1.0-2.dsc' brotli_1.1.0-2.dsc 2261 SHA256:39b06802a852629132d549a7f7449dee7f435e801706714a4bc2ea2f15b28f36
'http://deb.debian.org/debian/pool/main/b/brotli/brotli_1.1.0.orig.tar.gz' brotli_1.1.0.orig.tar.gz 512036 SHA256:10973f4b4199eafa1d5735ef661ddb2ec2f97319ee9fd1824d4aabe08cff5265
'http://deb.debian.org/debian/pool/main/b/brotli/brotli_1.1.0-2.debian.tar.xz' brotli_1.1.0-2.debian.tar.xz 5480 SHA256:3d913a3740bcad9a294007575a6beb1846beadbd62b44fb2bf9fdaeddea3236f
```

Other potentially useful URLs:

- https://sources.debian.net/src/brotli/1.1.0-2/ (for browsing the source)
- https://sources.debian.net/src/brotli/1.1.0-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/brotli/1.1.0-2/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/b/bzip2/bzip2_1.0.8-5.1.dsc' bzip2_1.0.8-5.1.dsc 2189 SHA256:210e367658236ea084627394015d466554f1ed2353a5feee5756335dc56074e6
'http://deb.debian.org/debian/pool/main/b/bzip2/bzip2_1.0.8.orig.tar.gz' bzip2_1.0.8.orig.tar.gz 810029 SHA256:ab5a03176ee106d3f0fa90e381da478ddae405918153cca248e682cd0c4a2269
'http://deb.debian.org/debian/pool/main/b/bzip2/bzip2_1.0.8-5.1.debian.tar.bz2' bzip2_1.0.8-5.1.debian.tar.bz2 26823 SHA256:8d07df2356a8105cc1ad4a64eba54c89aeb732fdc285e845cea1f6f66dda432d
```

Other potentially useful URLs:

- https://sources.debian.net/src/bzip2/1.0.8-5.1/ (for browsing the source)
- https://sources.debian.net/src/bzip2/1.0.8-5.1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/bzip2/1.0.8-5.1/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/c/ca-certificates/ca-certificates_20240203.dsc' ca-certificates_20240203.dsc 1766 SHA256:629afee9b327ce4df4ad0d77ad7b10383474a432e1af30516a7e81669420109b
'http://deb.debian.org/debian/pool/main/c/ca-certificates/ca-certificates_20240203.tar.xz' ca-certificates_20240203.tar.xz 263276 SHA256:3286d3fc42c4d11b7086711a85f865b44065ce05cf1fb5376b2abed07622a9c6
```

Other potentially useful URLs:

- https://sources.debian.net/src/ca-certificates/20240203/ (for browsing the source)
- https://sources.debian.net/src/ca-certificates/20240203/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/ca-certificates/20240203/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `cairo=1.18.0-3`

Binary Packages:

- `libcairo-gobject2:amd64=1.18.0-3+b1`
- `libcairo-script-interpreter2:amd64=1.18.0-3+b1`
- `libcairo2:amd64=1.18.0-3+b1`
- `libcairo2-dev:amd64=1.18.0-3+b1`

Licenses: (parsed from: `/usr/share/doc/libcairo-gobject2/copyright`, `/usr/share/doc/libcairo-script-interpreter2/copyright`, `/usr/share/doc/libcairo2/copyright`, `/usr/share/doc/libcairo2-dev/copyright`)

- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris cairo=1.18.0-3
'http://deb.debian.org/debian/pool/main/c/cairo/cairo_1.18.0-3.dsc' cairo_1.18.0-3.dsc 2756 SHA256:3f94d6aeeb32e21aab2f672e0892c590c46d46d4908ceb5f93ef4cbdfbdcaad0
'http://deb.debian.org/debian/pool/main/c/cairo/cairo_1.18.0.orig.tar.xz' cairo_1.18.0.orig.tar.xz 33761148 SHA256:243a0736b978a33dee29f9cca7521733b78a65b5418206fef7bd1c3d4cf10b64
'http://deb.debian.org/debian/pool/main/c/cairo/cairo_1.18.0-3.debian.tar.xz' cairo_1.18.0-3.debian.tar.xz 29796 SHA256:af6c4100ac6a729d039319ef7f83f7998a92946e019da5ed4e5bde2c27429a78
```

Other potentially useful URLs:

- https://sources.debian.net/src/cairo/1.18.0-3/ (for browsing the source)
- https://sources.debian.net/src/cairo/1.18.0-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/cairo/1.18.0-3/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/c/cdebconf/cdebconf_0.272.dsc' cdebconf_0.272.dsc 2707 SHA256:6b7c44f5d9881eb26c5f1d18d01015702b6fee1ce3751f8c5512d9371637eee7
'http://deb.debian.org/debian/pool/main/c/cdebconf/cdebconf_0.272.tar.xz' cdebconf_0.272.tar.xz 284488 SHA256:822883bc337bb06be4a9e6dba2fedf8d9ec3596cef8456be76eed6382ac773f9
```

Other potentially useful URLs:

- https://sources.debian.net/src/cdebconf/0.272/ (for browsing the source)
- https://sources.debian.net/src/cdebconf/0.272/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/cdebconf/0.272/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/c/coreutils/coreutils_9.4-3.1.dsc' coreutils_9.4-3.1.dsc 1868 SHA256:f18173c5b03135ec14e901748317ef5d05273dfbdebd76938988e2404f185aa1
'http://deb.debian.org/debian/pool/main/c/coreutils/coreutils_9.4.orig.tar.xz' coreutils_9.4.orig.tar.xz 5979200 SHA256:ea613a4cf44612326e917201bbbcdfbd301de21ffc3b59b6e5c07e040b275e52
'http://deb.debian.org/debian/pool/main/c/coreutils/coreutils_9.4-3.1.debian.tar.xz' coreutils_9.4-3.1.debian.tar.xz 29604 SHA256:326454b01befcd4116543c624f5515387f57f9655284330d1abb7c593abc001f
```

Other potentially useful URLs:

- https://sources.debian.net/src/coreutils/9.4-3.1/ (for browsing the source)
- https://sources.debian.net/src/coreutils/9.4-3.1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/coreutils/9.4-3.1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `curl=8.8.0-4`

Binary Packages:

- `curl=8.8.0-4`
- `libcurl3t64-gnutls:amd64=8.8.0-4`
- `libcurl4-openssl-dev:amd64=8.8.0-4`
- `libcurl4t64:amd64=8.8.0-4`

Licenses: (parsed from: `/usr/share/doc/curl/copyright`, `/usr/share/doc/libcurl3t64-gnutls/copyright`, `/usr/share/doc/libcurl4-openssl-dev/copyright`, `/usr/share/doc/libcurl4t64/copyright`)

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
$ apt-get source -qq --print-uris curl=8.8.0-4
'http://deb.debian.org/debian/pool/main/c/curl/curl_8.8.0-4.dsc' curl_8.8.0-4.dsc 3225 SHA256:000f31064f1a81ee7ecb523cf7aff821211c5420985646dd21698f549f0b4bc6
'http://deb.debian.org/debian/pool/main/c/curl/curl_8.8.0.orig.tar.gz' curl_8.8.0.orig.tar.gz 4152714 SHA256:77c0e1cd35ab5b45b659645a93b46d660224d0024f1185e8a95cdb27ae3d787d
'http://deb.debian.org/debian/pool/main/c/curl/curl_8.8.0.orig.tar.gz.asc' curl_8.8.0.orig.tar.gz.asc 488 SHA256:200ce86394b29564df060eb6eaec7e5d107c214b30401ce920f294b3b9c107a6
'http://deb.debian.org/debian/pool/main/c/curl/curl_8.8.0-4.debian.tar.xz' curl_8.8.0-4.debian.tar.xz 51216 SHA256:476e0b37498c1f2cfaba3e4605066e6c7e89ecd66a124f60a8dfdf85fd9ca1dc
```

Other potentially useful URLs:

- https://sources.debian.net/src/curl/8.8.0-4/ (for browsing the source)
- https://sources.debian.net/src/curl/8.8.0-4/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/curl/8.8.0-4/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `cyrus-sasl2=2.1.28+dfsg1-6`

Binary Packages:

- `libsasl2-2:amd64=2.1.28+dfsg1-6`
- `libsasl2-modules-db:amd64=2.1.28+dfsg1-6`

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
$ apt-get source -qq --print-uris cyrus-sasl2=2.1.28+dfsg1-6
'http://deb.debian.org/debian/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.28%2bdfsg1-6.dsc' cyrus-sasl2_2.1.28+dfsg1-6.dsc 3224 SHA256:79223015bc6fa0655d5d56207bb4ee7c3ca37122f2d425d5f9dd066ced9cf67d
'http://deb.debian.org/debian/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.28%2bdfsg1.orig.tar.xz' cyrus-sasl2_2.1.28+dfsg1.orig.tar.xz 794540 SHA256:e796a5d85d1a85e1b433d43504e467f9075c7ebc0b45730a3996cf11b1deada4
'http://deb.debian.org/debian/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.28%2bdfsg1-6.debian.tar.xz' cyrus-sasl2_2.1.28+dfsg1-6.debian.tar.xz 98280 SHA256:8968db0ae6acd8f87a51bc2e57419b5055b9bb23cdf2f822a8496d0e9c32b2d1
```

Other potentially useful URLs:

- https://sources.debian.net/src/cyrus-sasl2/2.1.28+dfsg1-6/ (for browsing the source)
- https://sources.debian.net/src/cyrus-sasl2/2.1.28+dfsg1-6/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/cyrus-sasl2/2.1.28+dfsg1-6/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/d/dash/dash_0.5.12-9.dsc' dash_0.5.12-9.dsc 1455 SHA256:aa5165888c75a39ec70477132329c7583863ee9762b6d07dc71fa2a5cdb84783
'http://deb.debian.org/debian/pool/main/d/dash/dash_0.5.12.orig.tar.gz' dash_0.5.12.orig.tar.gz 246054 SHA256:6a474ac46e8b0b32916c4c60df694c82058d3297d8b385b74508030ca4a8f28a
'http://deb.debian.org/debian/pool/main/d/dash/dash_0.5.12-9.debian.tar.xz' dash_0.5.12-9.debian.tar.xz 40096 SHA256:b5314d8c6cafae389559d6101dea059426263c95020ef5c547a59bcf5c0af2cc
```

Other potentially useful URLs:

- https://sources.debian.net/src/dash/0.5.12-9/ (for browsing the source)
- https://sources.debian.net/src/dash/0.5.12-9/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/dash/0.5.12-9/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `dav1d=1.4.3-1`

Binary Packages:

- `libdav1d7:amd64=1.4.3-1`

Licenses: (parsed from: `/usr/share/doc/libdav1d7/copyright`)

- `BSD-2-clause`
- `ISC`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris dav1d=1.4.3-1
'http://deb.debian.org/debian/pool/main/d/dav1d/dav1d_1.4.3-1.dsc' dav1d_1.4.3-1.dsc 2287 SHA256:26e5cfb9996484bf222a04038658c8edd9c435d86ef4afc19e317333da70177d
'http://deb.debian.org/debian/pool/main/d/dav1d/dav1d_1.4.3.orig.tar.xz' dav1d_1.4.3.orig.tar.xz 970088 SHA256:42fe524bcc82ea3a830057178faace22923a79bad3d819a4962d8cfc54c36f19
'http://deb.debian.org/debian/pool/main/d/dav1d/dav1d_1.4.3.orig.tar.xz.asc' dav1d_1.4.3.orig.tar.xz.asc 195 SHA256:f3356e8e3d1f8bb8150fe7f2ac2c1d1e4362eaecfbde936536544717b683abc4
'http://deb.debian.org/debian/pool/main/d/dav1d/dav1d_1.4.3-1.debian.tar.xz' dav1d_1.4.3-1.debian.tar.xz 8428 SHA256:5949571adea1e9559ab7e058abbcdf2164df2c0aa8f4e8fa608c6f0c5f892cb8
```

Other potentially useful URLs:

- https://sources.debian.net/src/dav1d/1.4.3-1/ (for browsing the source)
- https://sources.debian.net/src/dav1d/1.4.3-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/dav1d/1.4.3-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `db-defaults=5.3.3`

Binary Packages:

- `libdb-dev:amd64=5.3.3+b2`

Licenses: (parsed from: `/usr/share/doc/libdb-dev/copyright`)

- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris db-defaults=5.3.3
'http://deb.debian.org/debian/pool/main/d/db-defaults/db-defaults_5.3.3.dsc' db-defaults_5.3.3.dsc 1321 SHA256:774706cfb3a12d52a9cfa7c915aa001652e89c56887ca080a314744881a3e21b
'http://deb.debian.org/debian/pool/main/d/db-defaults/db-defaults_5.3.3.tar.xz' db-defaults_5.3.3.tar.xz 2432 SHA256:f4a44815b88fb3ae516ea5612b87882cceb9c54afa9184e91d7fdb3d1942f6a5
```

Other potentially useful URLs:

- https://sources.debian.net/src/db-defaults/5.3.3/ (for browsing the source)
- https://sources.debian.net/src/db-defaults/5.3.3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/db-defaults/5.3.3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `db5.3=5.3.28+dfsg2-7`

Binary Packages:

- `libdb5.3-dev=5.3.28+dfsg2-7`
- `libdb5.3t64:amd64=5.3.28+dfsg2-7`

Licenses: (parsed from: `/usr/share/doc/libdb5.3-dev/copyright`, `/usr/share/doc/libdb5.3t64/copyright`)

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
'http://deb.debian.org/debian/pool/main/d/db5.3/db5.3_5.3.28%2bdfsg2-7.dsc' db5.3_5.3.28+dfsg2-7.dsc 2374 SHA256:f7313fb306b5bf7ad6a428bffb581e649318859df139e35dd47c3d1f733803b2
'http://deb.debian.org/debian/pool/main/d/db5.3/db5.3_5.3.28%2bdfsg2.orig.tar.xz' db5.3_5.3.28+dfsg2.orig.tar.xz 21287688 SHA256:ad41b507415dec8316e828b2230242af2251d2c86eefa3c7aa9ef47c5239ef33
'http://deb.debian.org/debian/pool/main/d/db5.3/db5.3_5.3.28%2bdfsg2-7.debian.tar.xz' db5.3_5.3.28+dfsg2-7.debian.tar.xz 35232 SHA256:9cee8969e1f440ec8aa2fbacd3a5819907829e0e7e7f1f746dccaa2c93fbf3f2
```

Other potentially useful URLs:

- https://sources.debian.net/src/db5.3/5.3.28+dfsg2-7/ (for browsing the source)
- https://sources.debian.net/src/db5.3/5.3.28+dfsg2-7/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/db5.3/5.3.28+dfsg2-7/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/d/debian-archive-keyring/debian-archive-keyring_2023.4.dsc' debian-archive-keyring_2023.4.dsc 1261 SHA256:c97d048486078fcc6866a477df83b19270ae872102f4ed64b5a5e9995ff79afa
'http://deb.debian.org/debian/pool/main/d/debian-archive-keyring/debian-archive-keyring_2023.4.tar.xz' debian-archive-keyring_2023.4.tar.xz 177568 SHA256:7f9b64d7c5e748b0cb99fd0674d872111c219e119f296912c59fc61ab49bb78a
```

Other potentially useful URLs:

- https://sources.debian.net/src/debian-archive-keyring/2023.4/ (for browsing the source)
- https://sources.debian.net/src/debian-archive-keyring/2023.4/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/debian-archive-keyring/2023.4/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/d/debianutils/debianutils_5.20.dsc' debianutils_5.20.dsc 1631 SHA256:ceb4258f9923aef343cc281419140b00e89274eb2e89d12e459bcd8a9abc1ef1
'http://deb.debian.org/debian/pool/main/d/debianutils/debianutils_5.20.tar.xz' debianutils_5.20.tar.xz 80776 SHA256:dce8731adee52d1620d562c1d98b8f4177b4ae591b7a17091ffe09700dbd4be8
```

Other potentially useful URLs:

- https://sources.debian.net/src/debianutils/5.20/ (for browsing the source)
- https://sources.debian.net/src/debianutils/5.20/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/debianutils/5.20/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/d/diffutils/diffutils_3.10-1.dsc' diffutils_3.10-1.dsc 1715 SHA256:f7542884c67d44f0af356c5365a3fef8a298f1fbcbebf9df81cfbc6d6937f05f
'http://deb.debian.org/debian/pool/main/d/diffutils/diffutils_3.10.orig.tar.xz' diffutils_3.10.orig.tar.xz 1624240 SHA256:90e5e93cc724e4ebe12ede80df1634063c7a855692685919bfe60b556c9bd09e
'http://deb.debian.org/debian/pool/main/d/diffutils/diffutils_3.10.orig.tar.xz.asc' diffutils_3.10.orig.tar.xz.asc 833 SHA256:a94faf8f1baa04ff220f7b2ccb137c16337284e023ebc4a1d5df475c08d810f7
'http://deb.debian.org/debian/pool/main/d/diffutils/diffutils_3.10-1.debian.tar.xz' diffutils_3.10-1.debian.tar.xz 13952 SHA256:ebf51a7ceff8c882f997ca428232fd3b58ac59a70840c4b10f8fcfaa881598ce
```

Other potentially useful URLs:

- https://sources.debian.net/src/diffutils/1:3.10-1/ (for browsing the source)
- https://sources.debian.net/src/diffutils/1:3.10-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/diffutils/1:3.10-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `djvulibre=3.5.28-2`

Binary Packages:

- `libdjvulibre-dev:amd64=3.5.28-2+b1`
- `libdjvulibre-text=3.5.28-2`
- `libdjvulibre21:amd64=3.5.28-2+b1`

Licenses: (parsed from: `/usr/share/doc/libdjvulibre-dev/copyright`, `/usr/share/doc/libdjvulibre-text/copyright`, `/usr/share/doc/libdjvulibre21/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris djvulibre=3.5.28-2
'http://deb.debian.org/debian/pool/main/d/djvulibre/djvulibre_3.5.28-2.dsc' djvulibre_3.5.28-2.dsc 2388 SHA256:0b5f31e70a8f81afec47e67e9465dbece7756f0c7f88da643f0dda82bf78a1ba
'http://deb.debian.org/debian/pool/main/d/djvulibre/djvulibre_3.5.28.orig.tar.xz' djvulibre_3.5.28.orig.tar.xz 2959024 SHA256:1223b7bf7c8dfe2e290882f3bfb88ba2468b30495a1bf8dfd54dc7e810987887
'http://deb.debian.org/debian/pool/main/d/djvulibre/djvulibre_3.5.28-2.debian.tar.xz' djvulibre_3.5.28-2.debian.tar.xz 17420 SHA256:6f85dcd7cdb856cc3e4a31fc381e73a6cab717c90e058f474fb4d2ab29635d91
```

Other potentially useful URLs:

- https://sources.debian.net/src/djvulibre/3.5.28-2/ (for browsing the source)
- https://sources.debian.net/src/djvulibre/3.5.28-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/djvulibre/3.5.28-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `dpkg=1.22.8`

Binary Packages:

- `dpkg=1.22.8`
- `dpkg-dev=1.22.8`
- `libdpkg-perl=1.22.8`

Licenses: (parsed from: `/usr/share/doc/dpkg/copyright`, `/usr/share/doc/dpkg-dev/copyright`, `/usr/share/doc/libdpkg-perl/copyright`)

- `GPL-2`
- `GPL-2+`
- `public-domain-s-s-d`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/dpkg/1.22.8/


### `dpkg` source package: `e2fsprogs=1.47.1-1`

Binary Packages:

- `comerr-dev:amd64=2.1-1.47.1-1`
- `e2fsprogs=1.47.1-1`
- `libcom-err2:amd64=1.47.1-1`
- `libext2fs2t64:amd64=1.47.1-1`
- `libss2:amd64=1.47.1-1`
- `logsave=1.47.1-1`

Licenses: (parsed from: `/usr/share/doc/comerr-dev/copyright`, `/usr/share/doc/e2fsprogs/copyright`, `/usr/share/doc/libcom-err2/copyright`, `/usr/share/doc/libext2fs2t64/copyright`, `/usr/share/doc/libss2/copyright`, `/usr/share/doc/logsave/copyright`)

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
'http://deb.debian.org/debian/pool/main/e/e2fsprogs/e2fsprogs_1.47.1-1.dsc' e2fsprogs_1.47.1-1.dsc 2936 SHA256:04ae87a924fa3c9826db58af7e48c48659979c3e71b81a64bcaa48bf6e82507e
'http://deb.debian.org/debian/pool/main/e/e2fsprogs/e2fsprogs_1.47.1.orig.tar.gz' e2fsprogs_1.47.1.orig.tar.gz 9952468 SHA256:9afcd201f39429d2db2492aeb13dba5e75d6cc50682b732dca35643bd5f092e3
'http://deb.debian.org/debian/pool/main/e/e2fsprogs/e2fsprogs_1.47.1.orig.tar.gz.asc' e2fsprogs_1.47.1.orig.tar.gz.asc 488 SHA256:19b5fed0eb91cd58f0f82252a7d3f72a803dc2f497bfa765034551d9feb06781
'http://deb.debian.org/debian/pool/main/e/e2fsprogs/e2fsprogs_1.47.1-1.debian.tar.xz' e2fsprogs_1.47.1-1.debian.tar.xz 89808 SHA256:8d4a4b695ca9012c4e21a727ba9f00bf09c2b7adffd83813e998bfa76ed106b0
```

Other potentially useful URLs:

- https://sources.debian.net/src/e2fsprogs/1.47.1-1/ (for browsing the source)
- https://sources.debian.net/src/e2fsprogs/1.47.1-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/e2fsprogs/1.47.1-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `elfutils=0.191-2`

Binary Packages:

- `libelf1t64:amd64=0.191-2`

Licenses: (parsed from: `/usr/share/doc/libelf1t64/copyright`)

- `BSD-2-clause`
- `GFDL-1.3`
- `GFDL-NIV-1.3`
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
$ apt-get source -qq --print-uris elfutils=0.191-2
'http://deb.debian.org/debian/pool/main/e/elfutils/elfutils_0.191-2.dsc' elfutils_0.191-2.dsc 3275 SHA256:3bed7fdf1fec10afe7531ff34e8def33dfa5f0df97854bbfeb5216ff9e848a39
'http://deb.debian.org/debian/pool/main/e/elfutils/elfutils_0.191.orig.tar.bz2' elfutils_0.191.orig.tar.bz2 9310088 SHA256:df76db71366d1d708365fc7a6c60ca48398f14367eb2b8954efc8897147ad871
'http://deb.debian.org/debian/pool/main/e/elfutils/elfutils_0.191-2.debian.tar.xz' elfutils_0.191-2.debian.tar.xz 44404 SHA256:46d49ba0c62cd64ab8eafebaffea278ff584048fd66289031203919abdf2b58a
```

Other potentially useful URLs:

- https://sources.debian.net/src/elfutils/0.191-2/ (for browsing the source)
- https://sources.debian.net/src/elfutils/0.191-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/elfutils/0.191-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `expat=2.6.2-1`

Binary Packages:

- `libexpat1:amd64=2.6.2-1`
- `libexpat1-dev:amd64=2.6.2-1`

Licenses: (parsed from: `/usr/share/doc/libexpat1/copyright`, `/usr/share/doc/libexpat1-dev/copyright`)

- `MIT`

Source:

```console
$ apt-get source -qq --print-uris expat=2.6.2-1
'http://deb.debian.org/debian/pool/main/e/expat/expat_2.6.2-1.dsc' expat_2.6.2-1.dsc 1964 SHA256:fbc41fccaa7d701b271bff810b65f49b3c78e1a0180d048bc947955cc4612446
'http://deb.debian.org/debian/pool/main/e/expat/expat_2.6.2.orig.tar.gz' expat_2.6.2.orig.tar.gz 8416128 SHA256:fbd032683370d761ba68dba2566d3280a154f5290634172d60a79b24d366d9dc
'http://deb.debian.org/debian/pool/main/e/expat/expat_2.6.2-1.debian.tar.xz' expat_2.6.2-1.debian.tar.xz 12920 SHA256:ace5f5235455778222d01a5df08a9dfa3a1a8e015fc11b9c1d18a7d73cfa26fa
```

Other potentially useful URLs:

- https://sources.debian.net/src/expat/2.6.2-1/ (for browsing the source)
- https://sources.debian.net/src/expat/2.6.2-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/expat/2.6.2-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `fftw3=3.3.10-1`

Binary Packages:

- `libfftw3-double3:amd64=3.3.10-1+b3`

Licenses: (parsed from: `/usr/share/doc/libfftw3-double3/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris fftw3=3.3.10-1
'http://deb.debian.org/debian/pool/main/f/fftw3/fftw3_3.3.10-1.dsc' fftw3_3.3.10-1.dsc 2771 SHA256:5c6a64c8047e33f122fb1eebd4316178e3da86da16de70da0527906adcf22924
'http://deb.debian.org/debian/pool/main/f/fftw3/fftw3_3.3.10.orig.tar.gz' fftw3_3.3.10.orig.tar.gz 4144100 SHA256:56c932549852cddcfafdab3820b0200c7742675be92179e59e6215b340e26467
'http://deb.debian.org/debian/pool/main/f/fftw3/fftw3_3.3.10-1.debian.tar.xz' fftw3_3.3.10-1.debian.tar.xz 14520 SHA256:a19c2fa4eebb123626a8df89387e3437369d234f68799d3b2c0c9fb84b9ca875
```

Other potentially useful URLs:

- https://sources.debian.net/src/fftw3/3.3.10-1/ (for browsing the source)
- https://sources.debian.net/src/fftw3/3.3.10-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/fftw3/3.3.10-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `file=1:5.45-3`

Binary Packages:

- `file=1:5.45-3`
- `libmagic-mgc=1:5.45-3`
- `libmagic1t64:amd64=1:5.45-3`

Licenses: (parsed from: `/usr/share/doc/file/copyright`, `/usr/share/doc/libmagic-mgc/copyright`, `/usr/share/doc/libmagic1t64/copyright`)

- `BSD-2-Clause-alike`
- `BSD-2-Clause-netbsd`
- `BSD-2-Clause-regents`
- `MIT-Old-Style-with-legal-disclaimer-2`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris file=1:5.45-3
'http://deb.debian.org/debian/pool/main/f/file/file_5.45-3.dsc' file_5.45-3.dsc 2268 SHA256:5f406d2169753ca86828bfa41e5a9db3059f984004e6d07ba02edfd7de0f37ab
'http://deb.debian.org/debian/pool/main/f/file/file_5.45.orig.tar.gz' file_5.45.orig.tar.gz 1246503 SHA256:fc97f51029bb0e2c9f4e3bffefdaf678f0e039ee872b9de5c002a6d09c784d82
'http://deb.debian.org/debian/pool/main/f/file/file_5.45.orig.tar.gz.asc' file_5.45.orig.tar.gz.asc 169 SHA256:81aacbee95911bd9825e81748d42f41dadf846ba13165462dc428467ed9ee075
'http://deb.debian.org/debian/pool/main/f/file/file_5.45-3.debian.tar.xz' file_5.45-3.debian.tar.xz 35856 SHA256:6637b243f7811317d4e07219b14f4f40777c7ab3783a8d7834f53695e01e263e
```

Other potentially useful URLs:

- https://sources.debian.net/src/file/1:5.45-3/ (for browsing the source)
- https://sources.debian.net/src/file/1:5.45-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/file/1:5.45-3/ (for access to the source package after it no longer exists in the archive)

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
- `libfontconfig-dev:amd64=2.15.0-1.1`
- `libfontconfig1:amd64=2.15.0-1.1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris fontconfig=2.15.0-1.1
'http://deb.debian.org/debian/pool/main/f/fontconfig/fontconfig_2.15.0-1.1.dsc' fontconfig_2.15.0-1.1.dsc 2673 SHA256:8690eef21f60128a5a0bad56d8cd67fb19023f407b18cb3b14daef2a0af39277
'http://deb.debian.org/debian/pool/main/f/fontconfig/fontconfig_2.15.0.orig.tar.xz' fontconfig_2.15.0.orig.tar.xz 1447820 SHA256:63a0658d0e06e0fa886106452b58ef04f21f58202ea02a94c39de0d3335d7c0e
'http://deb.debian.org/debian/pool/main/f/fontconfig/fontconfig_2.15.0-1.1.debian.tar.xz' fontconfig_2.15.0-1.1.debian.tar.xz 59068 SHA256:1fa268da49c325269255072c504fd9f1d84a1410a301bf93ed980699de49a291
```

Other potentially useful URLs:

- https://sources.debian.net/src/fontconfig/2.15.0-1.1/ (for browsing the source)
- https://sources.debian.net/src/fontconfig/2.15.0-1.1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/fontconfig/2.15.0-1.1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `fonts-dejavu=2.37-8`

Binary Packages:

- `fonts-dejavu-core=2.37-8`
- `fonts-dejavu-mono=2.37-8`

Licenses: (parsed from: `/usr/share/doc/fonts-dejavu-core/copyright`, `/usr/share/doc/fonts-dejavu-mono/copyright`)

- `GPL-2`
- `GPL-2+`
- `bitstream-vera`

Source:

```console
$ apt-get source -qq --print-uris fonts-dejavu=2.37-8
'http://deb.debian.org/debian/pool/main/f/fonts-dejavu/fonts-dejavu_2.37-8.dsc' fonts-dejavu_2.37-8.dsc 2156 SHA256:219f7f8fba98827caaa296520730171ec230d3090ed8b6d663edb66839b48847
'http://deb.debian.org/debian/pool/main/f/fonts-dejavu/fonts-dejavu_2.37.orig.tar.bz2' fonts-dejavu_2.37.orig.tar.bz2 12050109 SHA256:4b21c5203f792343d5e90ab1cb0cf07e99887218abe3d83cd9a98cea9085e799
'http://deb.debian.org/debian/pool/main/f/fonts-dejavu/fonts-dejavu_2.37-8.debian.tar.xz' fonts-dejavu_2.37-8.debian.tar.xz 13176 SHA256:2401402245dec8a59fc5f0f8eff76d203a38440797f7f223e1d044e07c2d41fb
```

Other potentially useful URLs:

- https://sources.debian.net/src/fonts-dejavu/2.37-8/ (for browsing the source)
- https://sources.debian.net/src/fonts-dejavu/2.37-8/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/fonts-dejavu/2.37-8/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `freetype=2.13.2+dfsg-1`

Binary Packages:

- `libfreetype-dev:amd64=2.13.2+dfsg-1+b4`
- `libfreetype6:amd64=2.13.2+dfsg-1+b4`

Licenses: (parsed from: `/usr/share/doc/libfreetype-dev/copyright`, `/usr/share/doc/libfreetype6/copyright`)

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
'http://deb.debian.org/debian/pool/main/f/freetype/freetype_2.13.2%2bdfsg-1.dsc' freetype_2.13.2+dfsg-1.dsc 3686 SHA256:0e00399f7835b49c2606053b6681d2ef43693c6d5d7e6c86c29d1784c5e95e5a
'http://deb.debian.org/debian/pool/main/f/freetype/freetype_2.13.2%2bdfsg.orig-ft2demos.tar.xz' freetype_2.13.2+dfsg.orig-ft2demos.tar.xz 341140 SHA256:99ee2ed8b98bcfad17bc57c2d9699d764f20fe29ad304c69b8eb28834ca3b48e
'http://deb.debian.org/debian/pool/main/f/freetype/freetype_2.13.2%2bdfsg.orig-ft2demos.tar.xz.asc' freetype_2.13.2+dfsg.orig-ft2demos.tar.xz.asc 833 SHA256:e58ba462f7bdcdc5899f777d33453c1ce6f6e46b080047580f45c9fd9f2dc08c
'http://deb.debian.org/debian/pool/main/f/freetype/freetype_2.13.2%2bdfsg.orig-ft2docs.tar.xz' freetype_2.13.2+dfsg.orig-ft2docs.tar.xz 2173920 SHA256:685c25e1035a5076e5097186b3143b9c06878f3f9087d0a81e4d8538d5d15424
'http://deb.debian.org/debian/pool/main/f/freetype/freetype_2.13.2%2bdfsg.orig-ft2docs.tar.xz.asc' freetype_2.13.2+dfsg.orig-ft2docs.tar.xz.asc 833 SHA256:d7e17c8a3bce50181530ebe06346f506cbfc92ecc5ca7cc395c7dbb24a71a5c0
'http://deb.debian.org/debian/pool/main/f/freetype/freetype_2.13.2%2bdfsg.orig.tar.xz' freetype_2.13.2+dfsg.orig.tar.xz 2220368 SHA256:48c78a4194adfcd15a4d089f3206dab8454c311f5577f3ef7eaef95f777f86e6
'http://deb.debian.org/debian/pool/main/f/freetype/freetype_2.13.2%2bdfsg-1.debian.tar.xz' freetype_2.13.2+dfsg-1.debian.tar.xz 43824 SHA256:c1db3a2bf2a754fc3666b06757f4055fa7f964b256aaa520f6b7142b68e3c0bb
```

Other potentially useful URLs:

- https://sources.debian.net/src/freetype/2.13.2+dfsg-1/ (for browsing the source)
- https://sources.debian.net/src/freetype/2.13.2+dfsg-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/freetype/2.13.2+dfsg-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `fribidi=1.0.13-3`

Binary Packages:

- `libfribidi0:amd64=1.0.13-3+b1`

Licenses: (parsed from: `/usr/share/doc/libfribidi0/copyright`)

- `LGPL-2.1`
- `LGPL-2.1+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/fribidi/1.0.13-3/


### `dpkg` source package: `gcc-13=13.3.0-3`

Binary Packages:

- `cpp-13=13.3.0-3`
- `cpp-13-x86-64-linux-gnu=13.3.0-3`
- `g++-13=13.3.0-3`
- `g++-13-x86-64-linux-gnu=13.3.0-3`
- `gcc-13=13.3.0-3`
- `gcc-13-base:amd64=13.3.0-3`
- `gcc-13-x86-64-linux-gnu=13.3.0-3`
- `libgcc-13-dev:amd64=13.3.0-3`
- `libstdc++-13-dev:amd64=13.3.0-3`

Licenses: (parsed from: `/usr/share/doc/cpp-13/copyright`, `/usr/share/doc/cpp-13-x86-64-linux-gnu/copyright`, `/usr/share/doc/g++-13/copyright`, `/usr/share/doc/g++-13-x86-64-linux-gnu/copyright`, `/usr/share/doc/gcc-13/copyright`, `/usr/share/doc/gcc-13-base/copyright`, `/usr/share/doc/gcc-13-x86-64-linux-gnu/copyright`, `/usr/share/doc/libgcc-13-dev/copyright`, `/usr/share/doc/libstdc++-13-dev/copyright`)

- `Artistic`
- `GFDL-1.2`
- `GPL`
- `GPL-2`
- `GPL-3`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris gcc-13=13.3.0-3
'http://deb.debian.org/debian/pool/main/g/gcc-13/gcc-13_13.3.0-3.dsc' gcc-13_13.3.0-3.dsc 39089 SHA256:d2ba75c090668af4aa96974fd02dfd6d19d6b7c0ba2688c95af48088ed78fd0d
'http://deb.debian.org/debian/pool/main/g/gcc-13/gcc-13_13.3.0.orig.tar.gz' gcc-13_13.3.0.orig.tar.gz 90346516 SHA256:2fde6610c97427ca320113b8ed99d75439c15b7d75d0a5410256a9cf4a8e5402
'http://deb.debian.org/debian/pool/main/g/gcc-13/gcc-13_13.3.0-3.debian.tar.xz' gcc-13_13.3.0-3.debian.tar.xz 622412 SHA256:81fb6654b9fde5b134d4ddf13dd3ee5aa5b77e1db742eb5c4e4680e46d64e78a
```

Other potentially useful URLs:

- https://sources.debian.net/src/gcc-13/13.3.0-3/ (for browsing the source)
- https://sources.debian.net/src/gcc-13/13.3.0-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/gcc-13/13.3.0-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `gcc-14=14.1.0-5`

Binary Packages:

- `gcc-14-base:amd64=14.1.0-5`
- `libasan8:amd64=14.1.0-5`
- `libatomic1:amd64=14.1.0-5`
- `libcc1-0:amd64=14.1.0-5`
- `libgcc-s1:amd64=14.1.0-5`
- `libgomp1:amd64=14.1.0-5`
- `libhwasan0:amd64=14.1.0-5`
- `libitm1:amd64=14.1.0-5`
- `liblsan0:amd64=14.1.0-5`
- `libquadmath0:amd64=14.1.0-5`
- `libstdc++6:amd64=14.1.0-5`
- `libtsan2:amd64=14.1.0-5`
- `libubsan1:amd64=14.1.0-5`

Licenses: (parsed from: `/usr/share/doc/gcc-14-base/copyright`, `/usr/share/doc/libasan8/copyright`, `/usr/share/doc/libatomic1/copyright`, `/usr/share/doc/libcc1-0/copyright`, `/usr/share/doc/libgcc-s1/copyright`, `/usr/share/doc/libgomp1/copyright`, `/usr/share/doc/libhwasan0/copyright`, `/usr/share/doc/libitm1/copyright`, `/usr/share/doc/liblsan0/copyright`, `/usr/share/doc/libquadmath0/copyright`, `/usr/share/doc/libstdc++6/copyright`, `/usr/share/doc/libtsan2/copyright`, `/usr/share/doc/libubsan1/copyright`)

- `Artistic`
- `GFDL-1.2`
- `GPL`
- `GPL-3`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris gcc-14=14.1.0-5
'http://deb.debian.org/debian/pool/main/g/gcc-14/gcc-14_14.1.0-5.dsc' gcc-14_14.1.0-5.dsc 46515 SHA256:fcbcce74c791c352ad7a4bcdd63b46116c570b631beb56a15976aa1d967c4768
'http://deb.debian.org/debian/pool/main/g/gcc-14/gcc-14_14.1.0.orig.tar.gz' gcc-14_14.1.0.orig.tar.gz 94259732 SHA256:c5f6bb263e0b8ce27a0716b8bc9d61586079bcde0498a9ddda6db175fa8cd73a
'http://deb.debian.org/debian/pool/main/g/gcc-14/gcc-14_14.1.0-5.debian.tar.xz' gcc-14_14.1.0-5.debian.tar.xz 3251472 SHA256:8286da945ba2fffd0262b069e511ca480c8521b4845dc123d144475ad15eade8
```

Other potentially useful URLs:

- https://sources.debian.net/src/gcc-14/14.1.0-5/ (for browsing the source)
- https://sources.debian.net/src/gcc-14/14.1.0-5/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/gcc-14/14.1.0-5/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `gcc-defaults=1.214`

Binary Packages:

- `cpp=4:13.2.0-7`
- `cpp-x86-64-linux-gnu=4:13.2.0-7`
- `g++=4:13.2.0-7`
- `g++-x86-64-linux-gnu=4:13.2.0-7`
- `gcc=4:13.2.0-7`
- `gcc-x86-64-linux-gnu=4:13.2.0-7`

Licenses: (parsed from: `/usr/share/doc/cpp/copyright`, `/usr/share/doc/cpp-x86-64-linux-gnu/copyright`, `/usr/share/doc/g++/copyright`, `/usr/share/doc/g++-x86-64-linux-gnu/copyright`, `/usr/share/doc/gcc/copyright`, `/usr/share/doc/gcc-x86-64-linux-gnu/copyright`)

- `GPL-2`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/gcc-defaults/1.214/


### `dpkg` source package: `gdbm=1.23-6`

Binary Packages:

- `libgdbm-compat4t64:amd64=1.23-6`
- `libgdbm-dev:amd64=1.23-6`
- `libgdbm6t64:amd64=1.23-6`

Licenses: (parsed from: `/usr/share/doc/libgdbm-compat4t64/copyright`, `/usr/share/doc/libgdbm-dev/copyright`, `/usr/share/doc/libgdbm6t64/copyright`)

- `GFDL-NIV-1.3+`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris gdbm=1.23-6
'http://deb.debian.org/debian/pool/main/g/gdbm/gdbm_1.23-6.dsc' gdbm_1.23-6.dsc 2466 SHA256:fc3ea29c616ddf72a8d7cdc866de5ebad68192ac92bef70d574c13c892a9b1fd
'http://deb.debian.org/debian/pool/main/g/gdbm/gdbm_1.23.orig.tar.gz' gdbm_1.23.orig.tar.gz 1115854 SHA256:74b1081d21fff13ae4bd7c16e5d6e504a4c26f7cde1dca0d963a484174bbcacd
'http://deb.debian.org/debian/pool/main/g/gdbm/gdbm_1.23.orig.tar.gz.asc' gdbm_1.23.orig.tar.gz.asc 181 SHA256:64ebb68cc68e8915d62cb20ea40323c00b56051f844589ee0a52169fff34cecb
'http://deb.debian.org/debian/pool/main/g/gdbm/gdbm_1.23-6.debian.tar.xz' gdbm_1.23-6.debian.tar.xz 17800 SHA256:778993a6bcc16780aa203e87e1fae64d9165d88616522f23094e7467672b7f36
```

Other potentially useful URLs:

- https://sources.debian.net/src/gdbm/1.23-6/ (for browsing the source)
- https://sources.debian.net/src/gdbm/1.23-6/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/gdbm/1.23-6/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `gdk-pixbuf=2.42.12+dfsg-1`

Binary Packages:

- `gir1.2-gdkpixbuf-2.0:amd64=2.42.12+dfsg-1`
- `libgdk-pixbuf-2.0-0:amd64=2.42.12+dfsg-1`
- `libgdk-pixbuf-2.0-dev:amd64=2.42.12+dfsg-1`
- `libgdk-pixbuf2.0-bin=2.42.12+dfsg-1`
- `libgdk-pixbuf2.0-common=2.42.12+dfsg-1`

Licenses: (parsed from: `/usr/share/doc/gir1.2-gdkpixbuf-2.0/copyright`, `/usr/share/doc/libgdk-pixbuf-2.0-0/copyright`, `/usr/share/doc/libgdk-pixbuf-2.0-dev/copyright`, `/usr/share/doc/libgdk-pixbuf2.0-bin/copyright`, `/usr/share/doc/libgdk-pixbuf2.0-common/copyright`)

- `CC0-1.0`
- `GPL-2`
- `GPL-2+`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris gdk-pixbuf=2.42.12+dfsg-1
'http://deb.debian.org/debian/pool/main/g/gdk-pixbuf/gdk-pixbuf_2.42.12%2bdfsg-1.dsc' gdk-pixbuf_2.42.12+dfsg-1.dsc 3214 SHA256:812ca8729a97e91c754067ac296fc727884534868c987f36016bb972c49417b9
'http://deb.debian.org/debian/pool/main/g/gdk-pixbuf/gdk-pixbuf_2.42.12%2bdfsg.orig.tar.xz' gdk-pixbuf_2.42.12+dfsg.orig.tar.xz 6443656 SHA256:2fab7a828f1a017a235cd800cf0b47d83733037bade493337c46ed79e7ef3678
'http://deb.debian.org/debian/pool/main/g/gdk-pixbuf/gdk-pixbuf_2.42.12%2bdfsg-1.debian.tar.xz' gdk-pixbuf_2.42.12+dfsg-1.debian.tar.xz 21576 SHA256:ae0b3a9c557c734ade86f68f5a4ae8413981e3b97ca5d8ae6dc60508ba26be46
```

Other potentially useful URLs:

- https://sources.debian.net/src/gdk-pixbuf/2.42.12+dfsg-1/ (for browsing the source)
- https://sources.debian.net/src/gdk-pixbuf/2.42.12+dfsg-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/gdk-pixbuf/2.42.12+dfsg-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `git=1:2.45.2-1`

Binary Packages:

- `git=1:2.45.2-1`
- `git-man=1:2.45.2-1`

Licenses: (parsed from: `/usr/share/doc/git/copyright`, `/usr/share/doc/git-man/copyright`)

- `Apache-2.0`
- `Artistic`
- `Artistic-1`
- `BSD-3-clause`
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
- `Zlib`
- `dlmalloc`
- `mingw-runtime`

Source:

```console
$ apt-get source -qq --print-uris git=1:2.45.2-1
'http://deb.debian.org/debian/pool/main/g/git/git_2.45.2-1.dsc' git_2.45.2-1.dsc 2825 SHA256:4b40fdfeb10d0b9f156848667055695febc428f0698e7b2bb1655192838faf6b
'http://deb.debian.org/debian/pool/main/g/git/git_2.45.2.orig.tar.xz' git_2.45.2.orig.tar.xz 7487680 SHA256:51bfe87eb1c02fed1484051875365eeab229831d30d0cec5d89a14f9e40e9adb
'http://deb.debian.org/debian/pool/main/g/git/git_2.45.2-1.debian.tar.xz' git_2.45.2-1.debian.tar.xz 777720 SHA256:cb8a380dfc4add25674e83357f0cb68bc1bf8db15ff050ae1766109c53d59f0a
```

Other potentially useful URLs:

- https://sources.debian.net/src/git/1:2.45.2-1/ (for browsing the source)
- https://sources.debian.net/src/git/1:2.45.2-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/git/1:2.45.2-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `glib2.0=2.80.4-1`

Binary Packages:

- `gir1.2-glib-2.0:amd64=2.80.4-1`
- `gir1.2-glib-2.0-dev:amd64=2.80.4-1`
- `libgirepository-2.0-0:amd64=2.80.4-1`
- `libglib2.0-0t64:amd64=2.80.4-1`
- `libglib2.0-bin=2.80.4-1`
- `libglib2.0-data=2.80.4-1`
- `libglib2.0-dev:amd64=2.80.4-1`
- `libglib2.0-dev-bin=2.80.4-1`

Licenses: (parsed from: `/usr/share/doc/gir1.2-glib-2.0/copyright`, `/usr/share/doc/gir1.2-glib-2.0-dev/copyright`, `/usr/share/doc/libgirepository-2.0-0/copyright`, `/usr/share/doc/libglib2.0-0t64/copyright`, `/usr/share/doc/libglib2.0-bin/copyright`, `/usr/share/doc/libglib2.0-data/copyright`, `/usr/share/doc/libglib2.0-dev/copyright`, `/usr/share/doc/libglib2.0-dev-bin/copyright`)

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
$ apt-get source -qq --print-uris glib2.0=2.80.4-1
'http://deb.debian.org/debian/pool/main/g/glib2.0/glib2.0_2.80.4-1.dsc' glib2.0_2.80.4-1.dsc 4532 SHA256:7e1d4f7025dc60497e27e9b4008859afd2b84419c0a8e3b4e606e81715adf7a7
'http://deb.debian.org/debian/pool/main/g/glib2.0/glib2.0_2.80.4.orig-unicode-data.tar.xz' glib2.0_2.80.4.orig-unicode-data.tar.xz 263900 SHA256:f87fab5f2d5c59bcf801925d5bdf8c9cee85839d47f7ff820f053ec7b82b38cd
'http://deb.debian.org/debian/pool/main/g/glib2.0/glib2.0_2.80.4.orig.tar.xz' glib2.0_2.80.4.orig.tar.xz 5535760 SHA256:24e029c5dfc9b44e4573697adf33078a9827c48938555004b3b9096fa4ea034f
'http://deb.debian.org/debian/pool/main/g/glib2.0/glib2.0_2.80.4-1.debian.tar.xz' glib2.0_2.80.4-1.debian.tar.xz 132236 SHA256:d8d80a8d0cd85c799314a8bc6644baf464975486b3cccb12f7dfd8f0af717bce
```

Other potentially useful URLs:

- https://sources.debian.net/src/glib2.0/2.80.4-1/ (for browsing the source)
- https://sources.debian.net/src/glib2.0/2.80.4-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/glib2.0/2.80.4-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `glibc=2.39-5`

Binary Packages:

- `libc-bin=2.39-5`
- `libc-dev-bin=2.39-5`
- `libc6:amd64=2.39-5`
- `libc6-dev:amd64=2.39-5`

Licenses: (parsed from: `/usr/share/doc/libc-bin/copyright`, `/usr/share/doc/libc-dev-bin/copyright`, `/usr/share/doc/libc6/copyright`, `/usr/share/doc/libc6-dev/copyright`)

- `GPL-2`
- `LGPL-2.1`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/glibc/2.39-5/


### `dpkg` source package: `gmp=2:6.3.0+dfsg-2`

Binary Packages:

- `libgmp-dev:amd64=2:6.3.0+dfsg-2+b1`
- `libgmp10:amd64=2:6.3.0+dfsg-2+b1`
- `libgmpxx4ldbl:amd64=2:6.3.0+dfsg-2+b1`

Licenses: (parsed from: `/usr/share/doc/libgmp-dev/copyright`, `/usr/share/doc/libgmp10/copyright`, `/usr/share/doc/libgmpxx4ldbl/copyright`)

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
'http://deb.debian.org/debian/pool/main/g/gmp/gmp_6.3.0%2bdfsg-2.dsc' gmp_6.3.0+dfsg-2.dsc 2251 SHA256:31bf88a2899f7a6eb2dc0db438ba2b27f87562dfe73815a3bbc8b65675ba1a51
'http://deb.debian.org/debian/pool/main/g/gmp/gmp_6.3.0%2bdfsg.orig.tar.xz' gmp_6.3.0+dfsg.orig.tar.xz 1870556 SHA256:bd2966e6d277f79328e894a5a9f3ba3fbf2ed2be81def5f48623e30c23fb1572
'http://deb.debian.org/debian/pool/main/g/gmp/gmp_6.3.0%2bdfsg-2.debian.tar.xz' gmp_6.3.0+dfsg-2.debian.tar.xz 19156 SHA256:07fbc1f67c1c076575f8196f3b5a2d2be0268be10940ca59293d7f1669365f4e
```

Other potentially useful URLs:

- https://sources.debian.net/src/gmp/2:6.3.0+dfsg-2/ (for browsing the source)
- https://sources.debian.net/src/gmp/2:6.3.0+dfsg-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/gmp/2:6.3.0+dfsg-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `gnupg2=2.2.43-7`

Binary Packages:

- `dirmngr=2.2.43-7`
- `gnupg=2.2.43-7`
- `gnupg-l10n=2.2.43-7`
- `gpg=2.2.43-7`
- `gpg-agent=2.2.43-7`
- `gpgconf=2.2.43-7`
- `gpgsm=2.2.43-7`
- `gpgv=2.2.43-7`

Licenses: (parsed from: `/usr/share/doc/dirmngr/copyright`, `/usr/share/doc/gnupg/copyright`, `/usr/share/doc/gnupg-l10n/copyright`, `/usr/share/doc/gpg/copyright`, `/usr/share/doc/gpg-agent/copyright`, `/usr/share/doc/gpgconf/copyright`, `/usr/share/doc/gpgsm/copyright`, `/usr/share/doc/gpgv/copyright`)

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/gnupg2/2.2.43-7/


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
'http://deb.debian.org/debian/pool/main/g/gnutls28/gnutls28_3.8.6-2.dsc' gnutls28_3.8.6-2.dsc 3269 SHA256:4ec462fc0173a7e33a7051586ea4486b4856cbd97e38e9a96f88f033cf0862f8
'http://deb.debian.org/debian/pool/main/g/gnutls28/gnutls28_3.8.6.orig.tar.xz' gnutls28_3.8.6.orig.tar.xz 6517476 SHA256:2e1588aae53cb32d43937f1f4eca28febd9c0c7aa1734fc5dd61a7e81e0ebcdd
'http://deb.debian.org/debian/pool/main/g/gnutls28/gnutls28_3.8.6.orig.tar.xz.asc' gnutls28_3.8.6.orig.tar.xz.asc 228 SHA256:53ad69e21ea74447117aa55e51853c49e745f2c1e2de97539c6fbbec306cf65e
'http://deb.debian.org/debian/pool/main/g/gnutls28/gnutls28_3.8.6-2.debian.tar.xz' gnutls28_3.8.6-2.debian.tar.xz 77512 SHA256:7a71826206b082d6742fafcb6dee37aa9ae147b9bad8a69875f5eed8ea7a915b
```

Other potentially useful URLs:

- https://sources.debian.net/src/gnutls28/3.8.6-2/ (for browsing the source)
- https://sources.debian.net/src/gnutls28/3.8.6-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/gnutls28/3.8.6-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `gobject-introspection=1.80.1-3`

Binary Packages:

- `gir1.2-freedesktop:amd64=1.80.1-3+b1`
- `gir1.2-freedesktop-dev:amd64=1.80.1-3+b1`

Licenses: (parsed from: `/usr/share/doc/gir1.2-freedesktop/copyright`, `/usr/share/doc/gir1.2-freedesktop-dev/copyright`)

- `AFL-2.0`
- `Apache-2.0`
- `Apache-2.0 with LLVM exception`
- `BSD-2-clause`
- `CC-BY-SA-3.0`
- `CC0-1.0`
- `Expat`
- `FSFAP`
- `FSFULLR`
- `GPL with Autoconf exception`
- `GPL-2`
- `GPL-2+`
- `Kuchling-PD`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`
- `LGPL-3+`
- `MPL-1.1`
- `Plumb-PD`
- `Unicode-DFS-2016`
- `bzip2-1.0.6`

Source:

```console
$ apt-get source -qq --print-uris gobject-introspection=1.80.1-3
'http://deb.debian.org/debian/pool/main/g/gobject-introspection/gobject-introspection_1.80.1-3.dsc' gobject-introspection_1.80.1-3.dsc 4172 SHA256:298257a1a06f5a8757ee72ee774e7bf1e23a547eec7357c7ef1d0ac753629ed1
'http://deb.debian.org/debian/pool/main/g/gobject-introspection/gobject-introspection_1.80.1.orig-glib.tar.xz' gobject-introspection_1.80.1.orig-glib.tar.xz 5475296 SHA256:b3764dd6e29b664085921dd4dd6ba2430fc19760ab6857ecfa3ebd4e8c1d114c
'http://deb.debian.org/debian/pool/main/g/gobject-introspection/gobject-introspection_1.80.1.orig.tar.xz' gobject-introspection_1.80.1.orig.tar.xz 1040228 SHA256:a1df7c424e15bda1ab639c00e9051b9adf5cea1a9e512f8a603b53cd199bc6d8
'http://deb.debian.org/debian/pool/main/g/gobject-introspection/gobject-introspection_1.80.1-3.debian.tar.xz' gobject-introspection_1.80.1-3.debian.tar.xz 58368 SHA256:31437422e697152b858eff480feb8fd713a72df38ba6cc648ed5570de2ea9883
```

Other potentially useful URLs:

- https://sources.debian.net/src/gobject-introspection/1.80.1-3/ (for browsing the source)
- https://sources.debian.net/src/gobject-introspection/1.80.1-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/gobject-introspection/1.80.1-3/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/g/graphite2/graphite2_1.3.14-2.dsc' graphite2_1.3.14-2.dsc 2568 SHA256:98ee6be2e35e2a4f7dbc71a21315399d59c4f79339cb832c6caccf8f62342d26
'http://deb.debian.org/debian/pool/main/g/graphite2/graphite2_1.3.14.orig.tar.gz' graphite2_1.3.14.orig.tar.gz 6629829 SHA256:7a3b342c5681921ce2e0c2496509d30b5b078399d5a7bd2358f95166d57d91df
'http://deb.debian.org/debian/pool/main/g/graphite2/graphite2_1.3.14-2.debian.tar.xz' graphite2_1.3.14-2.debian.tar.xz 14168 SHA256:dc46cc532a54adfc7ed5798061795120325bf0722221b2a6299f49c403ee9cd4
```

Other potentially useful URLs:

- https://sources.debian.net/src/graphite2/1.3.14-2/ (for browsing the source)
- https://sources.debian.net/src/graphite2/1.3.14-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/graphite2/1.3.14-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `grep=3.11-4`

Binary Packages:

- `grep=3.11-4`

Licenses: (parsed from: `/usr/share/doc/grep/copyright`)

- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris grep=3.11-4
'http://deb.debian.org/debian/pool/main/g/grep/grep_3.11-4.dsc' grep_3.11-4.dsc 1642 SHA256:dd6f8eb933bc05446e483f7792c8bf0a1aba9d498e65c6ccafe64e9bf27ac054
'http://deb.debian.org/debian/pool/main/g/grep/grep_3.11.orig.tar.xz' grep_3.11.orig.tar.xz 1703776 SHA256:1db2aedde89d0dea42b16d9528f894c8d15dae4e190b59aecc78f5a951276eab
'http://deb.debian.org/debian/pool/main/g/grep/grep_3.11.orig.tar.xz.asc' grep_3.11.orig.tar.xz.asc 833 SHA256:89ec23ffd59b68822732dc8204fc89883c3af30a90ae390feb94346d9d09a589
'http://deb.debian.org/debian/pool/main/g/grep/grep_3.11-4.debian.tar.xz' grep_3.11-4.debian.tar.xz 20468 SHA256:f10394b7589c58ca7de4b580692b1b59431f898cb2068e86222c174e093fdf49
```

Other potentially useful URLs:

- https://sources.debian.net/src/grep/3.11-4/ (for browsing the source)
- https://sources.debian.net/src/grep/3.11-4/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/grep/3.11-4/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/g/gzip/gzip_1.12-1.1.dsc' gzip_1.12-1.1.dsc 2167 SHA256:212bff0edd2ccbbf816d7168f46f81d714b57043c249411e2e2d0fd71c3d3e40
'http://deb.debian.org/debian/pool/main/g/gzip/gzip_1.12.orig.tar.xz' gzip_1.12.orig.tar.xz 825548 SHA256:ce5e03e519f637e1f814011ace35c4f87b33c0bbabeec35baf5fbd3479e91956
'http://deb.debian.org/debian/pool/main/g/gzip/gzip_1.12.orig.tar.xz.asc' gzip_1.12.orig.tar.xz.asc 833 SHA256:3ed9ab54452576e0be0d477c772c9f47baa36415133fef7dd1fcf7b15480ba32
'http://deb.debian.org/debian/pool/main/g/gzip/gzip_1.12-1.1.debian.tar.xz' gzip_1.12-1.1.debian.tar.xz 19244 SHA256:d48d5314c0255114f43964f78b87262299bbac840e5f511a078e2d2590937ad6
```

Other potentially useful URLs:

- https://sources.debian.net/src/gzip/1.12-1.1/ (for browsing the source)
- https://sources.debian.net/src/gzip/1.12-1.1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/gzip/1.12-1.1/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/h/harfbuzz/harfbuzz_8.3.0-2.dsc' harfbuzz_8.3.0-2.dsc 2892 SHA256:e4464683b4936fd977ee5b62c9a6786a9be4966d111dea6b9278922819816895
'http://deb.debian.org/debian/pool/main/h/harfbuzz/harfbuzz_8.3.0.orig.tar.xz' harfbuzz_8.3.0.orig.tar.xz 19002808 SHA256:109501eaeb8bde3eadb25fab4164e993fbace29c3d775bcaa1c1e58e2f15f847
'http://deb.debian.org/debian/pool/main/h/harfbuzz/harfbuzz_8.3.0-2.debian.tar.xz' harfbuzz_8.3.0-2.debian.tar.xz 19796 SHA256:36267a5c7d65ce26dee24491aa8d95af6afe860c9dc4f908d7d3a1d290f9a896
```

Other potentially useful URLs:

- https://sources.debian.net/src/harfbuzz/8.3.0-2/ (for browsing the source)
- https://sources.debian.net/src/harfbuzz/8.3.0-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/harfbuzz/8.3.0-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `hicolor-icon-theme=0.18-1`

Binary Packages:

- `hicolor-icon-theme=0.18-1`

Licenses: (parsed from: `/usr/share/doc/hicolor-icon-theme/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris hicolor-icon-theme=0.18-1
'http://deb.debian.org/debian/pool/main/h/hicolor-icon-theme/hicolor-icon-theme_0.18-1.dsc' hicolor-icon-theme_0.18-1.dsc 2325 SHA256:97e0afba92378c0bf4bfeb5d10e9cc3a811811e7b23f712bd6e18b46f0f0d7c3
'http://deb.debian.org/debian/pool/main/h/hicolor-icon-theme/hicolor-icon-theme_0.18.orig.tar.xz' hicolor-icon-theme_0.18.orig.tar.xz 29624 SHA256:db0e50a80aa3bf64bb45cbca5cf9f75efd9348cf2ac690b907435238c3cf81d7
'http://deb.debian.org/debian/pool/main/h/hicolor-icon-theme/hicolor-icon-theme_0.18.orig.tar.xz.asc' hicolor-icon-theme_0.18.orig.tar.xz.asc 833 SHA256:0fe29ecd5d445805e33b33d7ff35813eabab2100806c06dd002efd35b37fb855
'http://deb.debian.org/debian/pool/main/h/hicolor-icon-theme/hicolor-icon-theme_0.18-1.debian.tar.xz' hicolor-icon-theme_0.18-1.debian.tar.xz 9100 SHA256:659512f9e592c31feef303069315f0052987ee619609a741c41a2dc820592608
```

Other potentially useful URLs:

- https://sources.debian.net/src/hicolor-icon-theme/0.18-1/ (for browsing the source)
- https://sources.debian.net/src/hicolor-icon-theme/0.18-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/hicolor-icon-theme/0.18-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `hostname=3.23+nmu2`

Binary Packages:

- `hostname=3.23+nmu2`

Licenses: (parsed from: `/usr/share/doc/hostname/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris hostname=3.23+nmu2
'http://deb.debian.org/debian/pool/main/h/hostname/hostname_3.23%2bnmu2.dsc' hostname_3.23+nmu2.dsc 1431 SHA256:03fe3dcdda4e3abc3a5d8d7ed6eb63558d9fa0dfe68412667eac73945b47e506
'http://deb.debian.org/debian/pool/main/h/hostname/hostname_3.23%2bnmu2.tar.xz' hostname_3.23+nmu2.tar.xz 12944 SHA256:e94bc2323862e1b49635c2b638aa905f14aa91d9eb525be8e8811a773ca3a60d
```

Other potentially useful URLs:

- https://sources.debian.net/src/hostname/3.23+nmu2/ (for browsing the source)
- https://sources.debian.net/src/hostname/3.23+nmu2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/hostname/3.23+nmu2/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/i/icu/icu_72.1-5.dsc' icu_72.1-5.dsc 2239 SHA256:0059598c83340a461c89bf51affe20ae8f84431c0c1a39f1b8e9c80ee892cabc
'http://deb.debian.org/debian/pool/main/i/icu/icu_72.1.orig.tar.gz' icu_72.1.orig.tar.gz 26303933 SHA256:a2d2d38217092a7ed56635e34467f92f976b370e20182ad325edea6681a71d68
'http://deb.debian.org/debian/pool/main/i/icu/icu_72.1.orig.tar.gz.asc' icu_72.1.orig.tar.gz.asc 659 SHA256:87b6ff610d587292cec0444fa8cbbfb12994cb89bade40578f5ba6470de245c7
'http://deb.debian.org/debian/pool/main/i/icu/icu_72.1-5.debian.tar.xz' icu_72.1-5.debian.tar.xz 62532 SHA256:fce0ce962faacae576d3312f2e421a17433e620994dcd1ea168cf4a48147303e
```

Other potentially useful URLs:

- https://sources.debian.net/src/icu/72.1-5/ (for browsing the source)
- https://sources.debian.net/src/icu/72.1-5/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/icu/72.1-5/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `imagemagick=8:6.9.13.12+dfsg1-1`

Binary Packages:

- `imagemagick=8:6.9.13.12+dfsg1-1`
- `imagemagick-6-common=8:6.9.13.12+dfsg1-1`
- `imagemagick-6.q16=8:6.9.13.12+dfsg1-1`
- `libmagickcore-6-arch-config:amd64=8:6.9.13.12+dfsg1-1`
- `libmagickcore-6-headers=8:6.9.13.12+dfsg1-1`
- `libmagickcore-6.q16-7-extra:amd64=8:6.9.13.12+dfsg1-1`
- `libmagickcore-6.q16-7t64:amd64=8:6.9.13.12+dfsg1-1`
- `libmagickcore-6.q16-dev:amd64=8:6.9.13.12+dfsg1-1`
- `libmagickcore-dev=8:6.9.13.12+dfsg1-1`
- `libmagickwand-6-headers=8:6.9.13.12+dfsg1-1`
- `libmagickwand-6.q16-7t64:amd64=8:6.9.13.12+dfsg1-1`
- `libmagickwand-6.q16-dev:amd64=8:6.9.13.12+dfsg1-1`
- `libmagickwand-dev=8:6.9.13.12+dfsg1-1`

Licenses: (parsed from: `/usr/share/doc/imagemagick/copyright`, `/usr/share/doc/imagemagick-6-common/copyright`, `/usr/share/doc/imagemagick-6.q16/copyright`, `/usr/share/doc/libmagickcore-6-arch-config/copyright`, `/usr/share/doc/libmagickcore-6-headers/copyright`, `/usr/share/doc/libmagickcore-6.q16-7-extra/copyright`, `/usr/share/doc/libmagickcore-6.q16-7t64/copyright`, `/usr/share/doc/libmagickcore-6.q16-dev/copyright`, `/usr/share/doc/libmagickcore-dev/copyright`, `/usr/share/doc/libmagickwand-6-headers/copyright`, `/usr/share/doc/libmagickwand-6.q16-7t64/copyright`, `/usr/share/doc/libmagickwand-6.q16-dev/copyright`, `/usr/share/doc/libmagickwand-dev/copyright`)

- `Artistic`
- `BSD-with-FSF-change-public-domain`
- `GNU-All-Permissive-License`
- `GPL-1`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL2+-with-Autoconf-Macros-exception`
- `GPL3+-with-Autoconf-Macros-exception`
- `GPL3+-with-Autoconf-Macros-exception-GNU`
- `ImageMagick`
- `ImageMagickLicensePartEZXML`
- `ImageMagickLicensePartFIG`
- `ImageMagickLicensePartGsview`
- `ImageMagickLicensePartOpenSSH`
- `ImageMagickPartGraphicsMagick`
- `ImageMagickPartlibjpeg`
- `ImageMagickPartlibsquish`
- `Imagemagick`
- `LGPL-3`
- `LGPL-3+`
- `Magick++`
- `Makefile-in`
- `Perllikelicence`
- `aclocal`

Source:

```console
$ apt-get source -qq --print-uris imagemagick=8:6.9.13.12+dfsg1-1
'http://deb.debian.org/debian/pool/main/i/imagemagick/imagemagick_6.9.13.12%2bdfsg1-1.dsc' imagemagick_6.9.13.12+dfsg1-1.dsc 5106 SHA256:a6352e88577b25beff4a0ec289b21ea5f079e793ff022bb2bea92558136a0428
'http://deb.debian.org/debian/pool/main/i/imagemagick/imagemagick_6.9.13.12%2bdfsg1.orig.tar.xz' imagemagick_6.9.13.12+dfsg1.orig.tar.xz 9829420 SHA256:0e3979571e2ba9a0d90c449a40972a26268a1b952f5c039fa857cc02cbca659a
'http://deb.debian.org/debian/pool/main/i/imagemagick/imagemagick_6.9.13.12%2bdfsg1-1.debian.tar.xz' imagemagick_6.9.13.12+dfsg1-1.debian.tar.xz 260856 SHA256:111d2ceac8358fb19b9156e20fddcf82407ee0414b0be017a963a6182b5a042c
```

Other potentially useful URLs:

- https://sources.debian.net/src/imagemagick/8:6.9.13.12+dfsg1-1/ (for browsing the source)
- https://sources.debian.net/src/imagemagick/8:6.9.13.12+dfsg1-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/imagemagick/8:6.9.13.12+dfsg1-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `imath=3.1.11-2`

Binary Packages:

- `libimath-3-1-29t64:amd64=3.1.11-2+b1`
- `libimath-dev:amd64=3.1.11-2+b1`

Licenses: (parsed from: `/usr/share/doc/libimath-3-1-29t64/copyright`, `/usr/share/doc/libimath-dev/copyright`)

- `imath`

Source:

```console
$ apt-get source -qq --print-uris imath=3.1.11-2
'http://deb.debian.org/debian/pool/main/i/imath/imath_3.1.11-2.dsc' imath_3.1.11-2.dsc 2721 SHA256:553646f1b219d774cef595a614befb63da83ceeb5ef69b1a952dfd97b32e0f5c
'http://deb.debian.org/debian/pool/main/i/imath/imath_3.1.11.orig.tar.gz' imath_3.1.11.orig.tar.gz 596585 SHA256:9057849585e49b8b85abe7cc1e76e22963b01bfdc3b6d83eac90c499cd760063
'http://deb.debian.org/debian/pool/main/i/imath/imath_3.1.11.orig.tar.gz.asc' imath_3.1.11.orig.tar.gz.asc 287 SHA256:a2c4ac5151789903ca8ab3093a2798491463ccf2abfd003a20f96453e505dd5f
'http://deb.debian.org/debian/pool/main/i/imath/imath_3.1.11-2.debian.tar.xz' imath_3.1.11-2.debian.tar.xz 9760 SHA256:a05989958c0dc2aec5cfd21e1f9b632017443794c41528d1c89366951eafc361
```

Other potentially useful URLs:

- https://sources.debian.net/src/imath/3.1.11-2/ (for browsing the source)
- https://sources.debian.net/src/imath/3.1.11-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/imath/3.1.11-2/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/i/init-system-helpers/init-system-helpers_1.66.dsc' init-system-helpers_1.66.dsc 2234 SHA256:a1e2276879abfe63174797c94969bc8591b8a05f2bad6ae3f27379b472877d6d
'http://deb.debian.org/debian/pool/main/i/init-system-helpers/init-system-helpers_1.66.tar.xz' init-system-helpers_1.66.tar.xz 44976 SHA256:da058b5623a7d3f39aee1761b173478fdbbdfdf743fd66e876e56039c708ce53
```

Other potentially useful URLs:

- https://sources.debian.net/src/init-system-helpers/1.66/ (for browsing the source)
- https://sources.debian.net/src/init-system-helpers/1.66/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/init-system-helpers/1.66/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/i/isl/isl_0.26-3.dsc' isl_0.26-3.dsc 1832 SHA256:b943ed41e0d04bd86ea1a9a10e49a0ac1996ac534b67b968df4320880ec6e6e7
'http://deb.debian.org/debian/pool/main/i/isl/isl_0.26.orig.tar.xz' isl_0.26.orig.tar.xz 2035560 SHA256:a0b5cb06d24f9fa9e77b55fabbe9a3c94a336190345c2555f9915bb38e976504
'http://deb.debian.org/debian/pool/main/i/isl/isl_0.26-3.debian.tar.xz' isl_0.26-3.debian.tar.xz 24700 SHA256:c4a9367d892a12da46c54cbf6475f447e137ac3eff857baa91af94c99daed0a5
```

Other potentially useful URLs:

- https://sources.debian.net/src/isl/0.26-3/ (for browsing the source)
- https://sources.debian.net/src/isl/0.26-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/isl/0.26-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `jansson=2.14-2`

Binary Packages:

- `libjansson4:amd64=2.14-2+b2`

Licenses: (parsed from: `/usr/share/doc/libjansson4/copyright`)

- `Expat`

Source:

```console
$ apt-get source -qq --print-uris jansson=2.14-2
'http://deb.debian.org/debian/pool/main/j/jansson/jansson_2.14-2.dsc' jansson_2.14-2.dsc 1980 SHA256:6296ddd9c0a022bd1b70074aefb171cfcdf5694a04ffd32b35fd66097621af87
'http://deb.debian.org/debian/pool/main/j/jansson/jansson_2.14.orig.tar.gz' jansson_2.14.orig.tar.gz 141500 SHA256:c739578bf6b764aa0752db9a2fdadcfe921c78f1228c7ec0bb47fa804c55d17b
'http://deb.debian.org/debian/pool/main/j/jansson/jansson_2.14-2.debian.tar.xz' jansson_2.14-2.debian.tar.xz 5428 SHA256:e89fe4fd8221f6934ddb50f2e7f8404311928d0e23e49a5599f3d3d14ee8cb88
```

Other potentially useful URLs:

- https://sources.debian.net/src/jansson/2.14-2/ (for browsing the source)
- https://sources.debian.net/src/jansson/2.14-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/jansson/2.14-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `jbigkit=2.1-6.1`

Binary Packages:

- `libjbig-dev:amd64=2.1-6.1+b1`
- `libjbig0:amd64=2.1-6.1+b1`

Licenses: (parsed from: `/usr/share/doc/libjbig-dev/copyright`, `/usr/share/doc/libjbig0/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris jbigkit=2.1-6.1
'http://deb.debian.org/debian/pool/main/j/jbigkit/jbigkit_2.1-6.1.dsc' jbigkit_2.1-6.1.dsc 2089 SHA256:8dea586c47cb4b2436f77fd33ef4a702b9da936d74de8332a72a8ddbe8124e09
'http://deb.debian.org/debian/pool/main/j/jbigkit/jbigkit_2.1.orig.tar.gz' jbigkit_2.1.orig.tar.gz 438710 SHA256:de7106b6bfaf495d6865c7dd7ac6ca1381bd12e0d81405ea81e7f2167263d932
'http://deb.debian.org/debian/pool/main/j/jbigkit/jbigkit_2.1-6.1.debian.tar.xz' jbigkit_2.1-6.1.debian.tar.xz 9244 SHA256:c9ba99e84d18b1affdc97b26b625721ed06b41a92996d9b426b62c0dbe3868cd
```

Other potentially useful URLs:

- https://sources.debian.net/src/jbigkit/2.1-6.1/ (for browsing the source)
- https://sources.debian.net/src/jbigkit/2.1-6.1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/jbigkit/2.1-6.1/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/k/keyutils/keyutils_1.6.3-3.dsc' keyutils_1.6.3-3.dsc 2079 SHA256:0a4178e10982c7351da7db5b44b5c18807613ad066cb2e157d0756019764f0c1
'http://deb.debian.org/debian/pool/main/k/keyutils/keyutils_1.6.3.orig.tar.gz' keyutils_1.6.3.orig.tar.gz 137022 SHA256:a61d5706136ae4c05bd48f86186bcfdbd88dd8bd5107e3e195c924cfc1b39bb4
'http://deb.debian.org/debian/pool/main/k/keyutils/keyutils_1.6.3-3.debian.tar.xz' keyutils_1.6.3-3.debian.tar.xz 13328 SHA256:8c078d9de91f930df174eebc60e063e8fff574ac36c0f7ee18f7e21635d60af0
```

Other potentially useful URLs:

- https://sources.debian.net/src/keyutils/1.6.3-3/ (for browsing the source)
- https://sources.debian.net/src/keyutils/1.6.3-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/keyutils/1.6.3-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `krb5=1.21.3-3`

Binary Packages:

- `krb5-multidev:amd64=1.21.3-3`
- `libgssapi-krb5-2:amd64=1.21.3-3`
- `libgssrpc4t64:amd64=1.21.3-3`
- `libk5crypto3:amd64=1.21.3-3`
- `libkadm5clnt-mit12:amd64=1.21.3-3`
- `libkadm5srv-mit12:amd64=1.21.3-3`
- `libkdb5-10t64:amd64=1.21.3-3`
- `libkrb5-3:amd64=1.21.3-3`
- `libkrb5-dev:amd64=1.21.3-3`
- `libkrb5support0:amd64=1.21.3-3`

Licenses: (parsed from: `/usr/share/doc/krb5-multidev/copyright`, `/usr/share/doc/libgssapi-krb5-2/copyright`, `/usr/share/doc/libgssrpc4t64/copyright`, `/usr/share/doc/libk5crypto3/copyright`, `/usr/share/doc/libkadm5clnt-mit12/copyright`, `/usr/share/doc/libkadm5srv-mit12/copyright`, `/usr/share/doc/libkdb5-10t64/copyright`, `/usr/share/doc/libkrb5-3/copyright`, `/usr/share/doc/libkrb5-dev/copyright`, `/usr/share/doc/libkrb5support0/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris krb5=1.21.3-3
'http://deb.debian.org/debian/pool/main/k/krb5/krb5_1.21.3-3.dsc' krb5_1.21.3-3.dsc 3381 SHA256:561af05f1e9c42ca9eab01eaa7ea6cd903494bb5b462917c8fff7d86bbedc872
'http://deb.debian.org/debian/pool/main/k/krb5/krb5_1.21.3.orig.tar.gz' krb5_1.21.3.orig.tar.gz 9136145 SHA256:b7a4cd5ead67fb08b980b21abd150ff7217e85ea320c9ed0c6dadd304840ad35
'http://deb.debian.org/debian/pool/main/k/krb5/krb5_1.21.3.orig.tar.gz.asc' krb5_1.21.3.orig.tar.gz.asc 833 SHA256:85047c935fe949ef2e275885451b168557b923dd13a5aab0ef8fe6acd27b94d7
'http://deb.debian.org/debian/pool/main/k/krb5/krb5_1.21.3-3.debian.tar.xz' krb5_1.21.3-3.debian.tar.xz 103380 SHA256:c7b7bceb2f1bd782d0118904bded8ddaba1aaa54f1b3b2fc0dc3ecaeac450b5b
```

Other potentially useful URLs:

- https://sources.debian.net/src/krb5/1.21.3-3/ (for browsing the source)
- https://sources.debian.net/src/krb5/1.21.3-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/krb5/1.21.3-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `lcms2=2.14-2`

Binary Packages:

- `liblcms2-2:amd64=2.14-2+b1`
- `liblcms2-dev:amd64=2.14-2+b1`

Licenses: (parsed from: `/usr/share/doc/liblcms2-2/copyright`, `/usr/share/doc/liblcms2-dev/copyright`)

- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `IJG`
- `MIT`

Source:

```console
$ apt-get source -qq --print-uris lcms2=2.14-2
'http://deb.debian.org/debian/pool/main/l/lcms2/lcms2_2.14-2.dsc' lcms2_2.14-2.dsc 1944 SHA256:65d7bd751c1dd0d0b70eaeb3a743849d19446b454c7bcf736de194e047784934
'http://deb.debian.org/debian/pool/main/l/lcms2/lcms2_2.14.orig.tar.gz' lcms2_2.14.orig.tar.gz 7406694 SHA256:28474ea6f6591c4d4cee972123587001a4e6e353412a41b3e9e82219818d5740
'http://deb.debian.org/debian/pool/main/l/lcms2/lcms2_2.14-2.debian.tar.xz' lcms2_2.14-2.debian.tar.xz 11728 SHA256:06ce5d9b473dce422f2387c2e18d646b7f639deae10e5a80bb2e4c5e45f1f6b5
```

Other potentially useful URLs:

- https://sources.debian.net/src/lcms2/2.14-2/ (for browsing the source)
- https://sources.debian.net/src/lcms2/2.14-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/lcms2/2.14-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `lerc=4.0.0+ds-4`

Binary Packages:

- `liblerc-dev:amd64=4.0.0+ds-4+b1`
- `liblerc4:amd64=4.0.0+ds-4+b1`

Licenses: (parsed from: `/usr/share/doc/liblerc-dev/copyright`, `/usr/share/doc/liblerc4/copyright`)

- `Apache-2.0`

Source:

```console
$ apt-get source -qq --print-uris lerc=4.0.0+ds-4
'http://deb.debian.org/debian/pool/main/l/lerc/lerc_4.0.0%2bds-4.dsc' lerc_4.0.0+ds-4.dsc 2638 SHA256:1f5758010599f9fd8b52ecea0541addeb0ea968f37d383a747abaa2a956f717e
'http://deb.debian.org/debian/pool/main/l/lerc/lerc_4.0.0%2bds.orig.tar.xz' lerc_4.0.0+ds.orig.tar.xz 348140 SHA256:acf855502fd3b950ee78f0b67bc9e9b39316b3526fbf6d8b8b1a9482fb756723
'http://deb.debian.org/debian/pool/main/l/lerc/lerc_4.0.0%2bds-4.debian.tar.xz' lerc_4.0.0+ds-4.debian.tar.xz 8280 SHA256:513db93f198180d601bba09356bd447c57d3a6360119e289cba897bf9054e5ac
```

Other potentially useful URLs:

- https://sources.debian.net/src/lerc/4.0.0+ds-4/ (for browsing the source)
- https://sources.debian.net/src/lerc/4.0.0+ds-4/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/lerc/4.0.0+ds-4/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libassuan=2.5.6-1`

Binary Packages:

- `libassuan0:amd64=2.5.6-1+b1`

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
$ apt-get source -qq --print-uris libassuan=2.5.6-1
'http://deb.debian.org/debian/pool/main/liba/libassuan/libassuan_2.5.6-1.dsc' libassuan_2.5.6-1.dsc 1997 SHA256:5216dd7bca769143cf39673b018a11b2601fde867fd4b62226088bb9177415b5
'http://deb.debian.org/debian/pool/main/liba/libassuan/libassuan_2.5.6.orig.tar.bz2' libassuan_2.5.6.orig.tar.bz2 577012 SHA256:e9fd27218d5394904e4e39788f9b1742711c3e6b41689a31aa3380bd5aa4f426
'http://deb.debian.org/debian/pool/main/liba/libassuan/libassuan_2.5.6.orig.tar.bz2.asc' libassuan_2.5.6.orig.tar.bz2.asc 228 SHA256:a1be6f5611de2f563a904c539e0415dd5823d9e1c4c0c1071418e7412174eaea
'http://deb.debian.org/debian/pool/main/liba/libassuan/libassuan_2.5.6-1.debian.tar.xz' libassuan_2.5.6-1.debian.tar.xz 14284 SHA256:58a3077b2ecda637de25f54320a3ad2087a250f6f8118271ea22968a4e994ca7
```

Other potentially useful URLs:

- https://sources.debian.net/src/libassuan/2.5.6-1/ (for browsing the source)
- https://sources.debian.net/src/libassuan/2.5.6-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libassuan/2.5.6-1/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/libb/libbsd/libbsd_0.12.2-1.dsc' libbsd_0.12.2-1.dsc 2347 SHA256:18bfe06bd7f6d5e3f77f7827bcf129014918952cdcd6102288afdae8120dc6c9
'http://deb.debian.org/debian/pool/main/libb/libbsd/libbsd_0.12.2.orig.tar.xz' libbsd_0.12.2.orig.tar.xz 446032 SHA256:b88cc9163d0c652aaf39a99991d974ddba1c3a9711db8f1b5838af2a14731014
'http://deb.debian.org/debian/pool/main/libb/libbsd/libbsd_0.12.2.orig.tar.xz.asc' libbsd_0.12.2.orig.tar.xz.asc 833 SHA256:620dc92f158ebe0a650c0e92214a8121b927276895dc9a1dcaa38f627fa0fcb0
'http://deb.debian.org/debian/pool/main/libb/libbsd/libbsd_0.12.2-1.debian.tar.xz' libbsd_0.12.2-1.debian.tar.xz 18612 SHA256:618f0d116e18729cb7d5b93095e112c429aad294993b4def2c0498761d4646e9
```

Other potentially useful URLs:

- https://sources.debian.net/src/libbsd/0.12.2-1/ (for browsing the source)
- https://sources.debian.net/src/libbsd/0.12.2-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libbsd/0.12.2-1/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/libc/libcap-ng/libcap-ng_0.8.5-1.dsc' libcap-ng_0.8.5-1.dsc 1638 SHA256:0b4a6e7ff74f5d888295bfab7f65f37255fb150e07bd8cedc0678c198b47bba0
'http://deb.debian.org/debian/pool/main/libc/libcap-ng/libcap-ng_0.8.5.orig.tar.gz' libcap-ng_0.8.5.orig.tar.gz 59265 SHA256:e4be07fdd234f10b866433f224d183626003c65634ed0552b02e654a380244c2
'http://deb.debian.org/debian/pool/main/libc/libcap-ng/libcap-ng_0.8.5-1.debian.tar.xz' libcap-ng_0.8.5-1.debian.tar.xz 7400 SHA256:17156cf9ef58de3e8c34a357c6afa47d54a42d2c185ffbd43fde7c4cf04937f1
```

Other potentially useful URLs:

- https://sources.debian.net/src/libcap-ng/0.8.5-1/ (for browsing the source)
- https://sources.debian.net/src/libcap-ng/0.8.5-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libcap-ng/0.8.5-1/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/libc/libcap2/libcap2_2.66-5.dsc' libcap2_2.66-5.dsc 2204 SHA256:7d8fd6db23376ad9ded85aebd5d5ed9cf133b1e561d3ac2b43fdf5b0b63739a8
'http://deb.debian.org/debian/pool/main/libc/libcap2/libcap2_2.66.orig.tar.xz' libcap2_2.66.orig.tar.xz 181592 SHA256:15c40ededb3003d70a283fe587a36b7d19c8b3b554e33f86129c059a4bb466b2
'http://deb.debian.org/debian/pool/main/libc/libcap2/libcap2_2.66-5.debian.tar.xz' libcap2_2.66-5.debian.tar.xz 21648 SHA256:fee7fdec4c806808b3e4c56e53ff5614b92186ecc6fd23a9e88694cdd938c452
```

Other potentially useful URLs:

- https://sources.debian.net/src/libcap2/1:2.66-5/ (for browsing the source)
- https://sources.debian.net/src/libcap2/1:2.66-5/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libcap2/1:2.66-5/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libcbor=0.10.2-1.2`

Binary Packages:

- `libcbor0.10:amd64=0.10.2-1.2`

Licenses: (parsed from: `/usr/share/doc/libcbor0.10/copyright`)

- `Expat`

Source:

```console
$ apt-get source -qq --print-uris libcbor=0.10.2-1.2
'http://deb.debian.org/debian/pool/main/libc/libcbor/libcbor_0.10.2-1.2.dsc' libcbor_0.10.2-1.2.dsc 2164 SHA256:507f5d432c75dcff46de2c0db2b7552691c441ca0c0864370a6185919b2b959b
'http://deb.debian.org/debian/pool/main/libc/libcbor/libcbor_0.10.2.orig.tar.gz' libcbor_0.10.2.orig.tar.gz 289450 SHA256:e75f712215d7b7e5c89ef322a09b701f7159f028b8b48978865725f00f79875b
'http://deb.debian.org/debian/pool/main/libc/libcbor/libcbor_0.10.2-1.2.debian.tar.xz' libcbor_0.10.2-1.2.debian.tar.xz 5444 SHA256:7cd5d61a121429e643c067dce022068ac0c5cf4c1f841f1ae2948215c4888790
```

Other potentially useful URLs:

- https://sources.debian.net/src/libcbor/0.10.2-1.2/ (for browsing the source)
- https://sources.debian.net/src/libcbor/0.10.2-1.2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libcbor/0.10.2-1.2/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/libd/libdatrie/libdatrie_0.2.13-3.dsc' libdatrie_0.2.13-3.dsc 2236 SHA256:6ddcaf319da01cc044f9b335b6b01b608a0380ccdaecb06bda71710b6f4395bb
'http://deb.debian.org/debian/pool/main/libd/libdatrie/libdatrie_0.2.13.orig.tar.xz' libdatrie_0.2.13.orig.tar.xz 314072 SHA256:12231bb2be2581a7f0fb9904092d24b0ed2a271a16835071ed97bed65267f4be
'http://deb.debian.org/debian/pool/main/libd/libdatrie/libdatrie_0.2.13-3.debian.tar.xz' libdatrie_0.2.13-3.debian.tar.xz 9668 SHA256:e656d536beb5db9e52ef92dd1fccd5480ebd21e4eddbfe013c51a1e2ec45cf38
```

Other potentially useful URLs:

- https://sources.debian.net/src/libdatrie/0.2.13-3/ (for browsing the source)
- https://sources.debian.net/src/libdatrie/0.2.13-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libdatrie/0.2.13-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libde265=1.0.15-1`

Binary Packages:

- `libde265-0:amd64=1.0.15-1+b1`

Licenses: (parsed from: `/usr/share/doc/libde265-0/copyright`)

- `BSD-4-clause`
- `GPL-3`
- `GPL-3+`
- `LGPL-3`
- `LGPL-3+`
- `other-1`
- `public-domain-1`

Source:

```console
$ apt-get source -qq --print-uris libde265=1.0.15-1
'http://deb.debian.org/debian/pool/main/libd/libde265/libde265_1.0.15-1.dsc' libde265_1.0.15-1.dsc 1872 SHA256:41fe11a559a57a8cdf19978c55f58f0d83de78c61e1367f8b73d05bdcce416eb
'http://deb.debian.org/debian/pool/main/libd/libde265/libde265_1.0.15.orig.tar.gz' libde265_1.0.15.orig.tar.gz 846016 SHA256:00251986c29d34d3af7117ed05874950c875dd9292d016be29d3b3762666511d
'http://deb.debian.org/debian/pool/main/libd/libde265/libde265_1.0.15-1.debian.tar.xz' libde265_1.0.15-1.debian.tar.xz 136584 SHA256:70cb236e55972d2d1bc062bacd68320ad402e0d378c79c99224a512208c90e5b
```

Other potentially useful URLs:

- https://sources.debian.net/src/libde265/1.0.15-1/ (for browsing the source)
- https://sources.debian.net/src/libde265/1.0.15-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libde265/1.0.15-1/ (for access to the source package after it no longer exists in the archive)

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

### `dpkg` source package: `libedit=3.1-20240517-1`

Binary Packages:

- `libedit2:amd64=3.1-20240517-1`

Licenses: (parsed from: `/usr/share/doc/libedit2/copyright`)

- `BSD-3-clause`

Source:

```console
$ apt-get source -qq --print-uris libedit=3.1-20240517-1
'http://deb.debian.org/debian/pool/main/libe/libedit/libedit_3.1-20240517-1.dsc' libedit_3.1-20240517-1.dsc 2264 SHA256:2943a877f4bf3ef8389edeae0d69f13f0b6fe31aedccdcf9e852108438334e79
'http://deb.debian.org/debian/pool/main/libe/libedit/libedit_3.1-20240517.orig.tar.gz' libedit_3.1-20240517.orig.tar.gz 534690 SHA256:3a489097bb4115495f3bd85ae782852b7097c556d9500088d74b6fa38dbd12ff
'http://deb.debian.org/debian/pool/main/libe/libedit/libedit_3.1-20240517-1.debian.tar.xz' libedit_3.1-20240517-1.debian.tar.xz 16700 SHA256:cae1b7d78da2b15c59122bd7651060bf01c6de0e8a42af5de95ec5a916e8b92b
```

Other potentially useful URLs:

- https://sources.debian.net/src/libedit/3.1-20240517-1/ (for browsing the source)
- https://sources.debian.net/src/libedit/3.1-20240517-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libedit/3.1-20240517-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `liberror-perl=0.17029-2`

Binary Packages:

- `liberror-perl=0.17029-2`

Licenses: (parsed from: `/usr/share/doc/liberror-perl/copyright`)

- `Artistic`
- `GPL-1`
- `GPL-1+`
- `MIT/X11`

Source:

```console
$ apt-get source -qq --print-uris liberror-perl=0.17029-2
'http://deb.debian.org/debian/pool/main/libe/liberror-perl/liberror-perl_0.17029-2.dsc' liberror-perl_0.17029-2.dsc 2085 SHA256:48c6ca66e03144a8bec4f32b2419f34d70e8a00500b01ea3bb6a5cab0c03e164
'http://deb.debian.org/debian/pool/main/libe/liberror-perl/liberror-perl_0.17029.orig.tar.gz' liberror-perl_0.17029.orig.tar.gz 33304 SHA256:1a23f7913032aed6d4b68321373a3899ca66590f4727391a091ec19c95bf7adc
'http://deb.debian.org/debian/pool/main/libe/liberror-perl/liberror-perl_0.17029-2.debian.tar.xz' liberror-perl_0.17029-2.debian.tar.xz 4608 SHA256:60deb5d5cbc4b478f8db4cfa0ac6c512e85eea5fcd7fc7285c26a9942d3b8b67
```

Other potentially useful URLs:

- https://sources.debian.net/src/liberror-perl/0.17029-2/ (for browsing the source)
- https://sources.debian.net/src/liberror-perl/0.17029-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/liberror-perl/0.17029-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libevent=2.1.12-stable-10`

Binary Packages:

- `libevent-2.1-7t64:amd64=2.1.12-stable-10`
- `libevent-core-2.1-7t64:amd64=2.1.12-stable-10`
- `libevent-dev=2.1.12-stable-10`
- `libevent-extra-2.1-7t64:amd64=2.1.12-stable-10`
- `libevent-openssl-2.1-7t64:amd64=2.1.12-stable-10`
- `libevent-pthreads-2.1-7t64:amd64=2.1.12-stable-10`

Licenses: (parsed from: `/usr/share/doc/libevent-2.1-7t64/copyright`, `/usr/share/doc/libevent-core-2.1-7t64/copyright`, `/usr/share/doc/libevent-dev/copyright`, `/usr/share/doc/libevent-extra-2.1-7t64/copyright`, `/usr/share/doc/libevent-openssl-2.1-7t64/copyright`, `/usr/share/doc/libevent-pthreads-2.1-7t64/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `BSL`
- `Expat`
- `FSFUL`
- `FSFULLR`
- `FSFULLR-No-Warranty`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `ISC`
- `curl`

Source:

```console
$ apt-get source -qq --print-uris libevent=2.1.12-stable-10
'http://deb.debian.org/debian/pool/main/libe/libevent/libevent_2.1.12-stable-10.dsc' libevent_2.1.12-stable-10.dsc 2412 SHA256:43ebc80590ab06ab0bdc6a07d4e5d85b4c5ce4ef61bf82103edcc4603873abe0
'http://deb.debian.org/debian/pool/main/libe/libevent/libevent_2.1.12-stable.orig.tar.gz' libevent_2.1.12-stable.orig.tar.gz 1100847 SHA256:92e6de1be9ec176428fd2367677e61ceffc2ee1cb119035037a27d346b0403bb
'http://deb.debian.org/debian/pool/main/libe/libevent/libevent_2.1.12-stable-10.debian.tar.xz' libevent_2.1.12-stable-10.debian.tar.xz 17908 SHA256:82743ad3391b9868516826b37e60a199aae9830f94d1ba5042f62dcbbe375349
```

Other potentially useful URLs:

- https://sources.debian.net/src/libevent/2.1.12-stable-10/ (for browsing the source)
- https://sources.debian.net/src/libevent/2.1.12-stable-10/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libevent/2.1.12-stable-10/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libexif=0.6.24-1`

Binary Packages:

- `libexif-dev:amd64=0.6.24-1+b1`
- `libexif12:amd64=0.6.24-1+b1`

Licenses: (parsed from: `/usr/share/doc/libexif-dev/copyright`, `/usr/share/doc/libexif12/copyright`)

- `BSD-2-Clause`
- `GPL-2`
- `GPL-2+`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `MIT`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris libexif=0.6.24-1
'http://deb.debian.org/debian/pool/main/libe/libexif/libexif_0.6.24-1.dsc' libexif_0.6.24-1.dsc 2116 SHA256:81f5fa53f45e786ed0b2bdf4b94c25d6b25eafda7ab15ce47e94501a276ff93d
'http://deb.debian.org/debian/pool/main/libe/libexif/libexif_0.6.24.orig.tar.gz' libexif_0.6.24.orig.tar.gz 1140079 SHA256:d3fb7c47829ec4d2def39aa38f4c35a0891763448a05dbf216a329a12bf198f9
'http://deb.debian.org/debian/pool/main/libe/libexif/libexif_0.6.24-1.debian.tar.xz' libexif_0.6.24-1.debian.tar.xz 11720 SHA256:9f0aca42c1221865ce4c0738301d5e0e99ff2ebed7e3bbbcce7e68605b991784
```

Other potentially useful URLs:

- https://sources.debian.net/src/libexif/0.6.24-1/ (for browsing the source)
- https://sources.debian.net/src/libexif/0.6.24-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libexif/0.6.24-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libffi=3.4.6-1`

Binary Packages:

- `libffi-dev:amd64=3.4.6-1`
- `libffi8:amd64=3.4.6-1`

Licenses: (parsed from: `/usr/share/doc/libffi-dev/copyright`, `/usr/share/doc/libffi8/copyright`)

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
'http://deb.debian.org/debian/pool/main/libf/libffi/libffi_3.4.6-1.dsc' libffi_3.4.6-1.dsc 1948 SHA256:6734a8f8e237a7d5c4f52503f5e9cc193d16f8930a201bbf737f09cb31cfe28e
'http://deb.debian.org/debian/pool/main/libf/libffi/libffi_3.4.6.orig.tar.gz' libffi_3.4.6.orig.tar.gz 598175 SHA256:9ac790464c1eb2f5ab5809e978a1683e9393131aede72d1b0a0703771d3c6cda
'http://deb.debian.org/debian/pool/main/libf/libffi/libffi_3.4.6-1.debian.tar.xz' libffi_3.4.6-1.debian.tar.xz 10636 SHA256:7126c310b616e9c4c8fdd50bd857f54379d26897ab55383a25e89b6cbd69729c
```

Other potentially useful URLs:

- https://sources.debian.net/src/libffi/3.4.6-1/ (for browsing the source)
- https://sources.debian.net/src/libffi/3.4.6-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libffi/3.4.6-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libfido2=1.15.0-1`

Binary Packages:

- `libfido2-1:amd64=1.15.0-1`

Licenses: (parsed from: `/usr/share/doc/libfido2-1/copyright`)

- `BSD-2-clause`
- `ISC`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris libfido2=1.15.0-1
'http://deb.debian.org/debian/pool/main/libf/libfido2/libfido2_1.15.0-1.dsc' libfido2_1.15.0-1.dsc 2585 SHA256:eb792b5b55bfd5421ce9abb30797317767b9b3e5884a071ab31e16a39ba21aba
'http://deb.debian.org/debian/pool/main/libf/libfido2/libfido2_1.15.0.orig.tar.gz' libfido2_1.15.0.orig.tar.gz 670019 SHA256:abaab1318d21d262ece416fb8a7132fa9374bda89f6fa52b86a98a2f5712b61e
'http://deb.debian.org/debian/pool/main/libf/libfido2/libfido2_1.15.0.orig.tar.gz.asc' libfido2_1.15.0.orig.tar.gz.asc 228 SHA256:7b757a545a07c989c75528d884d863a52ba61a4cc94661338dbbb2b7e62560ee
'http://deb.debian.org/debian/pool/main/libf/libfido2/libfido2_1.15.0-1.debian.tar.xz' libfido2_1.15.0-1.debian.tar.xz 52960 SHA256:4c20c21cffd478556f2fd2ab1ab529fd75bc1fc499f0851a45af91f78c3b4626
```

Other potentially useful URLs:

- https://sources.debian.net/src/libfido2/1.15.0-1/ (for browsing the source)
- https://sources.debian.net/src/libfido2/1.15.0-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libfido2/1.15.0-1/ (for access to the source package after it no longer exists in the archive)

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/libgpg-error/1.49-2/


### `dpkg` source package: `libheif=1.17.6-4`

Binary Packages:

- `libheif-plugin-dav1d:amd64=1.17.6-4+b2`
- `libheif-plugin-libde265:amd64=1.17.6-4+b2`
- `libheif1:amd64=1.17.6-4+b2`

Licenses: (parsed from: `/usr/share/doc/libheif-plugin-dav1d/copyright`, `/usr/share/doc/libheif-plugin-libde265/copyright`, `/usr/share/doc/libheif1/copyright`)

- `BSD-3-clause`
- `BSD-4-Clause-UC`
- `BSL-1.0`
- `Expat`
- `GPL-3`
- `GPL-3+`
- `LGPL-3`
- `LGPL-3+`

Source:

```console
$ apt-get source -qq --print-uris libheif=1.17.6-4
'http://deb.debian.org/debian/pool/main/libh/libheif/libheif_1.17.6-4.dsc' libheif_1.17.6-4.dsc 3497 SHA256:30215c9797c5b609d7d3a9ddd57ed6bf918fa58b8e0faaecad2db6b0c24a0550
'http://deb.debian.org/debian/pool/main/libh/libheif/libheif_1.17.6.orig.tar.gz' libheif_1.17.6.orig.tar.gz 1433302 SHA256:8390baf4913eda0a183e132cec62b875fb2ef507ced5ddddc98dfd2f17780aee
'http://deb.debian.org/debian/pool/main/libh/libheif/libheif_1.17.6-4.debian.tar.xz' libheif_1.17.6-4.debian.tar.xz 11292 SHA256:bb59c6ecb3ffeca0f0fd2db4b24feca6286d52041209309a500dfc75b2d9e3d2
```

Other potentially useful URLs:

- https://sources.debian.net/src/libheif/1.17.6-4/ (for browsing the source)
- https://sources.debian.net/src/libheif/1.17.6-4/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libheif/1.17.6-4/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libice=2:1.0.10-1`

Binary Packages:

- `libice-dev:amd64=2:1.0.10-1+b1`
- `libice6:amd64=2:1.0.10-1+b1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libice=2:1.0.10-1
'http://deb.debian.org/debian/pool/main/libi/libice/libice_1.0.10-1.dsc' libice_1.0.10-1.dsc 2049 SHA256:adb7b4e250db838a476a44b5a941c8f935ac2b20858186f09228cd3e0696034d
'http://deb.debian.org/debian/pool/main/libi/libice/libice_1.0.10.orig.tar.gz' libice_1.0.10.orig.tar.gz 481960 SHA256:1116bc64c772fd127a0d0c0ffa2833479905e3d3d8197740b3abd5f292f22d2d
'http://deb.debian.org/debian/pool/main/libi/libice/libice_1.0.10-1.diff.gz' libice_1.0.10-1.diff.gz 11349 SHA256:d186b3877416a7e80f1923fe2fc736d576e585a41450bcf4cd5e74f9dd099362
```

Other potentially useful URLs:

- https://sources.debian.net/src/libice/2:1.0.10-1/ (for browsing the source)
- https://sources.debian.net/src/libice/2:1.0.10-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libice/2:1.0.10-1/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/libi/libidn2/libidn2_2.3.7-2.dsc' libidn2_2.3.7-2.dsc 1963 SHA256:ba763f71c75847be4c68557a937484ff9e676c0af8be9a6796c914dab1363a5f
'http://deb.debian.org/debian/pool/main/libi/libidn2/libidn2_2.3.7.orig.tar.gz' libidn2_2.3.7.orig.tar.gz 2155214 SHA256:4c21a791b610b9519b9d0e12b8097bf2f359b12f8dd92647611a929e6bfd7d64
'http://deb.debian.org/debian/pool/main/libi/libidn2/libidn2_2.3.7.orig.tar.gz.asc' libidn2_2.3.7.orig.tar.gz.asc 228 SHA256:d4e78fc1c5a5c35980be3a04dd864574f450d55921360b0aa19326c75ada4a98
'http://deb.debian.org/debian/pool/main/libi/libidn2/libidn2_2.3.7-2.debian.tar.xz' libidn2_2.3.7-2.debian.tar.xz 16276 SHA256:1f0ca3a2bb2c745056933cb41d212965b6571c9a436f83d33cba15e932d88d29
```

Other potentially useful URLs:

- https://sources.debian.net/src/libidn2/2.3.7-2/ (for browsing the source)
- https://sources.debian.net/src/libidn2/2.3.7-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libidn2/2.3.7-2/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/libj/libjpeg-turbo/libjpeg-turbo_2.1.5-3.dsc' libjpeg-turbo_2.1.5-3.dsc 2499 SHA256:a05e6bd60e85b10d12ed705e84262ceadbac95f63a0ef947d783e3ae8da8e747
'http://deb.debian.org/debian/pool/main/libj/libjpeg-turbo/libjpeg-turbo_2.1.5.orig.tar.gz' libjpeg-turbo_2.1.5.orig.tar.gz 2264471 SHA256:254f3642b04e309fee775123133c6464181addc150499561020312ec61c1bf7c
'http://deb.debian.org/debian/pool/main/libj/libjpeg-turbo/libjpeg-turbo_2.1.5-3.debian.tar.xz' libjpeg-turbo_2.1.5-3.debian.tar.xz 107996 SHA256:18631a8db64da29c6fe86aef840a417a3a8205373679ae870e8f1cdcb22a32b4
```

Other potentially useful URLs:

- https://sources.debian.net/src/libjpeg-turbo/1:2.1.5-3/ (for browsing the source)
- https://sources.debian.net/src/libjpeg-turbo/1:2.1.5-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libjpeg-turbo/1:2.1.5-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libksba=1.6.7-2`

Binary Packages:

- `libksba8:amd64=1.6.7-2`

Licenses: (parsed from: `/usr/share/doc/libksba8/copyright`)

- `FSFUL`
- `GPL-3`
- `LGPL-2.1-or-later`

Source:

```console
$ apt-get source -qq --print-uris libksba=1.6.7-2
'http://deb.debian.org/debian/pool/main/libk/libksba/libksba_1.6.7-2.dsc' libksba_1.6.7-2.dsc 2482 SHA256:47f8b314c6b74fdcfb42390327dc0441c6ba6bfdb4511ca12e2b4478fc452e1c
'http://deb.debian.org/debian/pool/main/libk/libksba/libksba_1.6.7.orig.tar.bz2' libksba_1.6.7.orig.tar.bz2 706437 SHA256:cf72510b8ebb4eb6693eef765749d83677a03c79291a311040a5bfd79baab763
'http://deb.debian.org/debian/pool/main/libk/libksba/libksba_1.6.7.orig.tar.bz2.asc' libksba_1.6.7.orig.tar.bz2.asc 228 SHA256:cd704f8100151752b12776fa87dac42a3f99334ed155bcbcbaeda8e786581316
'http://deb.debian.org/debian/pool/main/libk/libksba/libksba_1.6.7-2.debian.tar.xz' libksba_1.6.7-2.debian.tar.xz 14872 SHA256:28f0ef1f9dd2a7f1cef23e49393d750d50aade01476462d8d5225a23e4ad9929
```

Other potentially useful URLs:

- https://sources.debian.net/src/libksba/1.6.7-2/ (for browsing the source)
- https://sources.debian.net/src/libksba/1.6.7-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libksba/1.6.7-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `liblqr=0.4.2-2.1`

Binary Packages:

- `liblqr-1-0:amd64=0.4.2-2.1+b1`
- `liblqr-1-0-dev:amd64=0.4.2-2.1+b1`

Licenses: (parsed from: `/usr/share/doc/liblqr-1-0/copyright`, `/usr/share/doc/liblqr-1-0-dev/copyright`)

- `GPL-3`
- `GPLv3`
- `LGPL-3`

Source:

```console
$ apt-get source -qq --print-uris liblqr=0.4.2-2.1
'http://deb.debian.org/debian/pool/main/libl/liblqr/liblqr_0.4.2-2.1.dsc' liblqr_0.4.2-2.1.dsc 2095 SHA256:c54c34cd2f7470a29366eeacde2ca4859a97d684a406fb81a918b970c01d617c
'http://deb.debian.org/debian/pool/main/libl/liblqr/liblqr_0.4.2.orig.tar.gz' liblqr_0.4.2.orig.tar.gz 439884 SHA256:d4c22373432cca749e4326cd41fce365e6ff857c0bfd7a5302b8eb34b69f0336
'http://deb.debian.org/debian/pool/main/libl/liblqr/liblqr_0.4.2-2.1.debian.tar.xz' liblqr_0.4.2-2.1.debian.tar.xz 5300 SHA256:284a002f1ecac63ac17b1aafbb230da9ce7bd9efe2d5b94e8cad49b607eb2564
```

Other potentially useful URLs:

- https://sources.debian.net/src/liblqr/0.4.2-2.1/ (for browsing the source)
- https://sources.debian.net/src/liblqr/0.4.2-2.1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/liblqr/0.4.2-2.1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libmaxminddb=1.9.1-1`

Binary Packages:

- `libmaxminddb-dev:amd64=1.9.1-1`
- `libmaxminddb0:amd64=1.9.1-1`

Licenses: (parsed from: `/usr/share/doc/libmaxminddb-dev/copyright`, `/usr/share/doc/libmaxminddb0/copyright`)

- `Apache-2.0`
- `BSD-2-clause`
- `BSD-3-clause`
- `BSD-4-clause`
- `CC-BY-SA-3.0`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris libmaxminddb=1.9.1-1
'http://deb.debian.org/debian/pool/main/libm/libmaxminddb/libmaxminddb_1.9.1-1.dsc' libmaxminddb_1.9.1-1.dsc 2322 SHA256:4d6bfda7a076000a0027b2a15491e59959c5a0d2bc9f8721750ce60003f6a0ba
'http://deb.debian.org/debian/pool/main/libm/libmaxminddb/libmaxminddb_1.9.1.orig.tar.gz' libmaxminddb_1.9.1.orig.tar.gz 243507 SHA256:cc9c69e84c7f0ba557e165f013815cd3bfd25d62824d06c08c44c158acbd82d4
'http://deb.debian.org/debian/pool/main/libm/libmaxminddb/libmaxminddb_1.9.1-1.debian.tar.xz' libmaxminddb_1.9.1-1.debian.tar.xz 12488 SHA256:16bdb54584734c8b1ecbf397e058599a745ecb36210cd46ae73174f98f200b6f
```

Other potentially useful URLs:

- https://sources.debian.net/src/libmaxminddb/1.9.1-1/ (for browsing the source)
- https://sources.debian.net/src/libmaxminddb/1.9.1-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libmaxminddb/1.9.1-1/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/libm/libmd/libmd_1.1.0-2.dsc' libmd_1.1.0-2.dsc 2280 SHA256:46cc951cd6d71bbfeff4522de66f968fb92601ec4cc622b07f6ac0a2a36ac5f0
'http://deb.debian.org/debian/pool/main/libm/libmd/libmd_1.1.0.orig.tar.xz' libmd_1.1.0.orig.tar.xz 271228 SHA256:1bd6aa42275313af3141c7cf2e5b964e8b1fd488025caf2f971f43b00776b332
'http://deb.debian.org/debian/pool/main/libm/libmd/libmd_1.1.0.orig.tar.xz.asc' libmd_1.1.0.orig.tar.xz.asc 833 SHA256:402fd3024e43ab975733d09e661804a58ca58697194e4b15216b1217cfe1dadb
'http://deb.debian.org/debian/pool/main/libm/libmd/libmd_1.1.0-2.debian.tar.xz' libmd_1.1.0-2.debian.tar.xz 8244 SHA256:3b6ff35fc921eb5450fa9bf2d300c9e058e3771f96f8f13f759768fadd53324c
```

Other potentially useful URLs:

- https://sources.debian.net/src/libmd/1.1.0-2/ (for browsing the source)
- https://sources.debian.net/src/libmd/1.1.0-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libmd/1.1.0-2/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/libp/libpng1.6/libpng1.6_1.6.43-5.dsc' libpng1.6_1.6.43-5.dsc 2269 SHA256:ef8d2c8a58893d500db27f88d95edda16c2832ab0ffbef23c7f7177b2e967222
'http://deb.debian.org/debian/pool/main/libp/libpng1.6/libpng1.6_1.6.43.orig.tar.gz' libpng1.6_1.6.43.orig.tar.gz 1554715 SHA256:fecc95b46cf05e8e3fc8a414750e0ba5aad00d89e9fdf175e94ff041caf1a03a
'http://deb.debian.org/debian/pool/main/libp/libpng1.6/libpng1.6_1.6.43-5.debian.tar.xz' libpng1.6_1.6.43-5.debian.tar.xz 31476 SHA256:449bf2a0008548dd2c37e9a3b511596bf2650568562a9c1b932be8bb3f256d00
```

Other potentially useful URLs:

- https://sources.debian.net/src/libpng1.6/1.6.43-5/ (for browsing the source)
- https://sources.debian.net/src/libpng1.6/1.6.43-5/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libpng1.6/1.6.43-5/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/libp/libpsl/libpsl_0.21.2-1.1.dsc' libpsl_0.21.2-1.1.dsc 2285 SHA256:b9b5496ca2bffb827cb0b2d997469908a2b7a7475c20a11c02f9dcd1ed2a0cc9
'http://deb.debian.org/debian/pool/main/libp/libpsl/libpsl_0.21.2.orig.tar.xz' libpsl_0.21.2.orig.tar.xz 1870352 SHA256:11e34380f2c81d6e72c710464aae3b680df4ddcc1007826c630fb03c7ca6aa54
'http://deb.debian.org/debian/pool/main/libp/libpsl/libpsl_0.21.2-1.1.debian.tar.xz' libpsl_0.21.2-1.1.debian.tar.xz 12120 SHA256:0eccab147b6dfbfb7f5ad40fb5bd9f888d72a0fe44e7d1801811c34a9acad1a7
```

Other potentially useful URLs:

- https://sources.debian.net/src/libpsl/0.21.2-1.1/ (for browsing the source)
- https://sources.debian.net/src/libpsl/0.21.2-1.1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libpsl/0.21.2-1.1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libraw=0.21.2-2.1`

Binary Packages:

- `libraw23t64:amd64=0.21.2-2.1`

Licenses: (parsed from: `/usr/share/doc/libraw23t64/copyright`)

- `CC-BY-SA-3.0`
- `CDDL-1.0`
- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libraw=0.21.2-2.1
'http://deb.debian.org/debian/pool/main/libr/libraw/libraw_0.21.2-2.1.dsc' libraw_0.21.2-2.1.dsc 2220 SHA256:1d0510d78871d5e4dbd146919ddf3496e55f478178e36a847fa54c058a046290
'http://deb.debian.org/debian/pool/main/libr/libraw/libraw_0.21.2.orig.tar.gz' libraw_0.21.2.orig.tar.gz 565383 SHA256:7ac056e0d9e814d808f6973a950bbf45e71b53283eed07a7ea87117a6c0ced96
'http://deb.debian.org/debian/pool/main/libr/libraw/libraw_0.21.2-2.1.debian.tar.xz' libraw_0.21.2-2.1.debian.tar.xz 24724 SHA256:0dd4a22e32a164304549b3ef6295face72761d649372485e041247ec2f9cc853
```

Other potentially useful URLs:

- https://sources.debian.net/src/libraw/0.21.2-2.1/ (for browsing the source)
- https://sources.debian.net/src/libraw/0.21.2-2.1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libraw/0.21.2-2.1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `librsvg=2.58.0+dfsg-1`

Binary Packages:

- `gir1.2-rsvg-2.0:amd64=2.58.0+dfsg-1`
- `librsvg2-2:amd64=2.58.0+dfsg-1`
- `librsvg2-common:amd64=2.58.0+dfsg-1`
- `librsvg2-dev:amd64=2.58.0+dfsg-1`

Licenses: (parsed from: `/usr/share/doc/gir1.2-rsvg-2.0/copyright`, `/usr/share/doc/librsvg2-2/copyright`, `/usr/share/doc/librsvg2-common/copyright`, `/usr/share/doc/librsvg2-dev/copyright`)

- `0BSD`
- `0BSD,`
- `Apache-2.0`
- `Apache-2.0,`
- `BSD-2-clause`
- `BSD-2-clause,`
- `BSD-3-clause`
- `BSD-3-clause,`
- `Boost-1.0`
- `Boost-1.0,`
- `CC-zero-waive-1.0-us`
- `Expat`
- `Expat,`
- `FSFAP`
- `LGPL-2`
- `LGPL-2+`
- `MPL-2.0`
- `MPL-2.0,`
- `OFL-1.1`
- `Sun-permissive`
- `Sun-permissive,`
- `Unlicense`
- `Unlicense,`
- `zlib`

Source:

```console
$ apt-get source -qq --print-uris librsvg=2.58.0+dfsg-1
'http://deb.debian.org/debian/pool/main/libr/librsvg/librsvg_2.58.0%2bdfsg-1.dsc' librsvg_2.58.0+dfsg-1.dsc 3068 SHA256:42072c44c91dcea364dc18fa0c51d8b95caa05802e308816b5a68cf2729918b9
'http://deb.debian.org/debian/pool/main/libr/librsvg/librsvg_2.58.0%2bdfsg.orig.tar.xz' librsvg_2.58.0+dfsg.orig.tar.xz 5736316 SHA256:5e59425031069e9310207664e8fd75004d1dc7ce09f1750f7978aa8e87ab7e49
'http://deb.debian.org/debian/pool/main/libr/librsvg/librsvg_2.58.0%2bdfsg-1.debian.tar.xz' librsvg_2.58.0+dfsg-1.debian.tar.xz 29507800 SHA256:a472c7c840ac61dabd27a1aff5ac17fb874f0b855032bc0b1c6ec0c1d58834b6
```

Other potentially useful URLs:

- https://sources.debian.net/src/librsvg/2.58.0+dfsg-1/ (for browsing the source)
- https://sources.debian.net/src/librsvg/2.58.0+dfsg-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/librsvg/2.58.0+dfsg-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libseccomp=2.5.5-1`

Binary Packages:

- `libseccomp2:amd64=2.5.5-1+b1`

Licenses: (parsed from: `/usr/share/doc/libseccomp2/copyright`)

- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libseccomp=2.5.5-1
'http://deb.debian.org/debian/pool/main/libs/libseccomp/libseccomp_2.5.5-1.dsc' libseccomp_2.5.5-1.dsc 2708 SHA256:d8ea2fb22a4ed90001a34ace6e6a6f41fd1d9404de923182f2dde6037fec22e5
'http://deb.debian.org/debian/pool/main/libs/libseccomp/libseccomp_2.5.5.orig.tar.gz' libseccomp_2.5.5.orig.tar.gz 642445 SHA256:248a2c8a4d9b9858aa6baf52712c34afefcf9c9e94b76dce02c1c9aa25fb3375
'http://deb.debian.org/debian/pool/main/libs/libseccomp/libseccomp_2.5.5.orig.tar.gz.asc' libseccomp_2.5.5.orig.tar.gz.asc 833 SHA256:f3bf8a946020d3047581f11fe6ac71971a842115ddb362562b193861ef57d97b
'http://deb.debian.org/debian/pool/main/libs/libseccomp/libseccomp_2.5.5-1.debian.tar.xz' libseccomp_2.5.5-1.debian.tar.xz 17608 SHA256:0e14e878a97657d8ff660f32477461abbd3ce366e5c24df4e4385c3e64cacaac
```

Other potentially useful URLs:

- https://sources.debian.net/src/libseccomp/2.5.5-1/ (for browsing the source)
- https://sources.debian.net/src/libseccomp/2.5.5-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libseccomp/2.5.5-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libselinux=3.5-2`

Binary Packages:

- `libselinux1:amd64=3.5-2+b3`
- `libselinux1-dev:amd64=3.5-2+b3`

Licenses: (parsed from: `/usr/share/doc/libselinux1/copyright`, `/usr/share/doc/libselinux1-dev/copyright`)

- `GPL-2`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris libselinux=3.5-2
'http://deb.debian.org/debian/pool/main/libs/libselinux/libselinux_3.5-2.dsc' libselinux_3.5-2.dsc 2662 SHA256:cd6baa8aebf37a88355291bf5cb11a311463479fed8a9f479043d1fc12de25cc
'http://deb.debian.org/debian/pool/main/libs/libselinux/libselinux_3.5.orig.tar.gz' libselinux_3.5.orig.tar.gz 211453 SHA256:9a3a3705ac13a2ccca2de6d652b6356fead10f36fb33115c185c5ccdf29eec19
'http://deb.debian.org/debian/pool/main/libs/libselinux/libselinux_3.5.orig.tar.gz.asc' libselinux_3.5.orig.tar.gz.asc 981 SHA256:fd37d441e0c08cabe9ac8f7815f52355bab2011549ec5792424fe18be9e1e015
'http://deb.debian.org/debian/pool/main/libs/libselinux/libselinux_3.5-2.debian.tar.xz' libselinux_3.5-2.debian.tar.xz 35992 SHA256:e385f14d9700187495a82e433b02b139aebe89c8ceccab5a21598dfef518b0de
```

Other potentially useful URLs:

- https://sources.debian.net/src/libselinux/3.5-2/ (for browsing the source)
- https://sources.debian.net/src/libselinux/3.5-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libselinux/3.5-2/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/libs/libsemanage/libsemanage_3.5-1.dsc' libsemanage_3.5-1.dsc 2644 SHA256:7415394f12030387ebca4ab7845830984b1ceb7ec3256d30a1733ba7f59d18c1
'http://deb.debian.org/debian/pool/main/libs/libsemanage/libsemanage_3.5.orig.tar.gz' libsemanage_3.5.orig.tar.gz 185060 SHA256:f53534e50247538280ed0d76c6ce81d8fb3939bd64cadb89da10dba42e40dd9c
'http://deb.debian.org/debian/pool/main/libs/libsemanage/libsemanage_3.5.orig.tar.gz.asc' libsemanage_3.5.orig.tar.gz.asc 981 SHA256:f9126c861c666f3308b60cea4405c5e686a056113ca3cbd0a5b0e4af7600c8f5
'http://deb.debian.org/debian/pool/main/libs/libsemanage/libsemanage_3.5-1.debian.tar.xz' libsemanage_3.5-1.debian.tar.xz 29956 SHA256:78b11321d014bd52e1fb67c38db5ec6518b0b566b58c6e35a18e894dacc24aee
```

Other potentially useful URLs:

- https://sources.debian.net/src/libsemanage/3.5-1/ (for browsing the source)
- https://sources.debian.net/src/libsemanage/3.5-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libsemanage/3.5-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libsepol=3.5-2`

Binary Packages:

- `libsepol-dev:amd64=3.5-2+b1`
- `libsepol2:amd64=3.5-2+b1`

Licenses: (parsed from: `/usr/share/doc/libsepol-dev/copyright`, `/usr/share/doc/libsepol2/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris libsepol=3.5-2
'http://deb.debian.org/debian/pool/main/libs/libsepol/libsepol_3.5-2.dsc' libsepol_3.5-2.dsc 2005 SHA256:0f7b4750fbb8f34841c31784e8fbc1a94949a83adbcb7103f0ae061198bc55e7
'http://deb.debian.org/debian/pool/main/libs/libsepol/libsepol_3.5.orig.tar.gz' libsepol_3.5.orig.tar.gz 497522 SHA256:78fdaf69924db780bac78546e43d9c44074bad798c2c415d0b9bb96d065ee8a2
'http://deb.debian.org/debian/pool/main/libs/libsepol/libsepol_3.5.orig.tar.gz.asc' libsepol_3.5.orig.tar.gz.asc 981 SHA256:2309ab5e7cd38e2eb9196f92a60e00d4508cb293f1181d34a5a050128c9b7b24
'http://deb.debian.org/debian/pool/main/libs/libsepol/libsepol_3.5-2.debian.tar.xz' libsepol_3.5-2.debian.tar.xz 27596 SHA256:05de2029893ec20cde7687178003fc5161d606259dad218ad46e7332db922695
```

Other potentially useful URLs:

- https://sources.debian.net/src/libsepol/3.5-2/ (for browsing the source)
- https://sources.debian.net/src/libsepol/3.5-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libsepol/3.5-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libsm=2:1.2.3-1`

Binary Packages:

- `libsm-dev:amd64=2:1.2.3-1+b1`
- `libsm6:amd64=2:1.2.3-1+b1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libsm=2:1.2.3-1
'http://deb.debian.org/debian/pool/main/libs/libsm/libsm_1.2.3-1.dsc' libsm_1.2.3-1.dsc 2063 SHA256:5488f8de81d53c32cbb5f062b6a6f262cd067283b8082041392dc60f0d04002c
'http://deb.debian.org/debian/pool/main/libs/libsm/libsm_1.2.3.orig.tar.gz' libsm_1.2.3.orig.tar.gz 445362 SHA256:1e92408417cb6c6c477a8a6104291001a40b3bb56a4a60608fdd9cd2c5a0f320
'http://deb.debian.org/debian/pool/main/libs/libsm/libsm_1.2.3-1.diff.gz' libsm_1.2.3-1.diff.gz 8929 SHA256:7eb99ab50b19f26d1470f89e4b46891f6a697cb1794a58ed0d1376cceaf1b6a9
```

Other potentially useful URLs:

- https://sources.debian.net/src/libsm/2:1.2.3-1/ (for browsing the source)
- https://sources.debian.net/src/libsm/2:1.2.3-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libsm/2:1.2.3-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libssh2=1.11.0-5`

Binary Packages:

- `libssh2-1t64:amd64=1.11.0-5`

Licenses: (parsed from: `/usr/share/doc/libssh2-1t64/copyright`)

- `BSD3`
- `ISC`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/libssh2/1.11.0-5/


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
'http://deb.debian.org/debian/pool/main/libt/libtasn1-6/libtasn1-6_4.19.0-3.dsc' libtasn1-6_4.19.0-3.dsc 2662 SHA256:7fd9618be5b99035c7387d969b73365a57b1f6f01ec4abe0af332829af718190
'http://deb.debian.org/debian/pool/main/libt/libtasn1-6/libtasn1-6_4.19.0.orig.tar.gz' libtasn1-6_4.19.0.orig.tar.gz 1786576 SHA256:1613f0ac1cf484d6ec0ce3b8c06d56263cc7242f1c23b30d82d23de345a63f7a
'http://deb.debian.org/debian/pool/main/libt/libtasn1-6/libtasn1-6_4.19.0.orig.tar.gz.asc' libtasn1-6_4.19.0.orig.tar.gz.asc 228 SHA256:8410c0c004f3509c218a98b276b3308b9c46f48068e8b1a6d9ebfd61ea9f357a
'http://deb.debian.org/debian/pool/main/libt/libtasn1-6/libtasn1-6_4.19.0-3.debian.tar.xz' libtasn1-6_4.19.0-3.debian.tar.xz 22084 SHA256:acb32dc03d8c2aeb10e0fb1c2a0247efdab0a6dc5e8f8a4d3cdcfe5ad26bb0df
```

Other potentially useful URLs:

- https://sources.debian.net/src/libtasn1-6/4.19.0-3/ (for browsing the source)
- https://sources.debian.net/src/libtasn1-6/4.19.0-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libtasn1-6/4.19.0-3/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/libt/libthai/libthai_0.1.29-2.dsc' libthai_0.1.29-2.dsc 2319 SHA256:564814dc31a466566cb50c077c5f6c5926a451594f52a0fc6b6367100445dddb
'http://deb.debian.org/debian/pool/main/libt/libthai/libthai_0.1.29.orig.tar.xz' libthai_0.1.29.orig.tar.xz 417728 SHA256:fc80cc7dcb50e11302b417cebd24f2d30a8b987292e77e003267b9100d0f4bcd
'http://deb.debian.org/debian/pool/main/libt/libthai/libthai_0.1.29-2.debian.tar.xz' libthai_0.1.29-2.debian.tar.xz 12644 SHA256:18a66bc2e766f475c206492612eabe3a206642bb69866236eb4a0a4126bf4f41
```

Other potentially useful URLs:

- https://sources.debian.net/src/libthai/0.1.29-2/ (for browsing the source)
- https://sources.debian.net/src/libthai/0.1.29-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libthai/0.1.29-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libtool=2.4.7-7`

Binary Packages:

- `libltdl-dev:amd64=2.4.7-7+b1`
- `libltdl7:amd64=2.4.7-7+b1`
- `libtool=2.4.7-7`

Licenses: (parsed from: `/usr/share/doc/libltdl-dev/copyright`, `/usr/share/doc/libltdl7/copyright`, `/usr/share/doc/libtool/copyright`)

- `GFDL-1.3`
- `GFDL-NIV-1.3+`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris libtool=2.4.7-7
'http://deb.debian.org/debian/pool/main/libt/libtool/libtool_2.4.7-7.dsc' libtool_2.4.7-7.dsc 2257 SHA256:c6045c55f34fcd3b7a4194059d498085d4a6d0bc4c6a0cb3825fb3859461dc7a
'http://deb.debian.org/debian/pool/main/libt/libtool/libtool_2.4.7.orig.tar.xz' libtool_2.4.7.orig.tar.xz 1026028 SHA256:dd637e270439b208907ceead3f163470ed2ce5723ef97ffbda6463c64b57128a
'http://deb.debian.org/debian/pool/main/libt/libtool/libtool_2.4.7-7.debian.tar.xz' libtool_2.4.7-7.debian.tar.xz 40916 SHA256:217a33c2f4474f4f23c69fa0bc694f9d380885003f02785ed69248b0dfb1d449
```

Other potentially useful URLs:

- https://sources.debian.net/src/libtool/2.4.7-7/ (for browsing the source)
- https://sources.debian.net/src/libtool/2.4.7-7/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libtool/2.4.7-7/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/libu/libunistring/libunistring_1.2-1.dsc' libunistring_1.2-1.dsc 2181 SHA256:5d951adce58920ab7e598f04b903f402382557ad102576d01184553437467dd6
'http://deb.debian.org/debian/pool/main/libu/libunistring/libunistring_1.2.orig.tar.xz' libunistring_1.2.orig.tar.xz 2502196 SHA256:632bd65ed74a881ca8a0309a1001c428bd1cbd5cd7ddbf8cedcd2e65f4dcdc44
'http://deb.debian.org/debian/pool/main/libu/libunistring/libunistring_1.2.orig.tar.xz.asc' libunistring_1.2.orig.tar.xz.asc 833 SHA256:91da3f033231a635dae9e0161c834b74e890e1eba19d4e5972b26c5c312ac2cb
'http://deb.debian.org/debian/pool/main/libu/libunistring/libunistring_1.2-1.debian.tar.xz' libunistring_1.2-1.debian.tar.xz 13656 SHA256:0605dbb77c072393abaa9e6ec8507d57d91f62aee4d7a7f968f295e4e9ab3bcf
```

Other potentially useful URLs:

- https://sources.debian.net/src/libunistring/1.2-1/ (for browsing the source)
- https://sources.debian.net/src/libunistring/1.2-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libunistring/1.2-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libwebp=1.4.0-0.1`

Binary Packages:

- `libsharpyuv-dev:amd64=1.4.0-0.1`
- `libsharpyuv0:amd64=1.4.0-0.1`
- `libwebp-dev:amd64=1.4.0-0.1`
- `libwebp7:amd64=1.4.0-0.1`
- `libwebpdecoder3:amd64=1.4.0-0.1`
- `libwebpdemux2:amd64=1.4.0-0.1`
- `libwebpmux3:amd64=1.4.0-0.1`

Licenses: (parsed from: `/usr/share/doc/libsharpyuv-dev/copyright`, `/usr/share/doc/libsharpyuv0/copyright`, `/usr/share/doc/libwebp-dev/copyright`, `/usr/share/doc/libwebp7/copyright`, `/usr/share/doc/libwebpdecoder3/copyright`, `/usr/share/doc/libwebpdemux2/copyright`, `/usr/share/doc/libwebpmux3/copyright`)

- `Apache-2.0`
- `BSD-3-Clause`

Source:

```console
$ apt-get source -qq --print-uris libwebp=1.4.0-0.1
'http://deb.debian.org/debian/pool/main/libw/libwebp/libwebp_1.4.0-0.1.dsc' libwebp_1.4.0-0.1.dsc 2569 SHA256:c21ed5aa518a60d590e9435e998bf223114e6248f619b6af81cd82e7ebf39b51
'http://deb.debian.org/debian/pool/main/libw/libwebp/libwebp_1.4.0.orig.tar.gz' libwebp_1.4.0.orig.tar.gz 4281370 SHA256:61f873ec69e3be1b99535634340d5bde750b2e4447caa1db9f61be3fd49ab1e5
'http://deb.debian.org/debian/pool/main/libw/libwebp/libwebp_1.4.0.orig.tar.gz.asc' libwebp_1.4.0.orig.tar.gz.asc 833 SHA256:9a25a1f6c2bec4a4ec05ece3bd6938f0e9b47e432d58067d3877dba4fbcf6214
'http://deb.debian.org/debian/pool/main/libw/libwebp/libwebp_1.4.0-0.1.debian.tar.xz' libwebp_1.4.0-0.1.debian.tar.xz 11048 SHA256:d137689ec52cb7dd5851bea0e73a9d6e032b35df79e821ce1db770109f1eaf65
```

Other potentially useful URLs:

- https://sources.debian.net/src/libwebp/1.4.0-0.1/ (for browsing the source)
- https://sources.debian.net/src/libwebp/1.4.0-0.1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libwebp/1.4.0-0.1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libwmf=0.2.13-1.1`

Binary Packages:

- `libwmf-0.2-7:amd64=0.2.13-1.1+b2`
- `libwmf-dev=0.2.13-1.1+b2`
- `libwmflite-0.2-7:amd64=0.2.13-1.1+b2`

Licenses: (parsed from: `/usr/share/doc/libwmf-0.2-7/copyright`, `/usr/share/doc/libwmf-dev/copyright`, `/usr/share/doc/libwmflite-0.2-7/copyright`)

- `AGPL-3 with Font exception`
- `GD`
- `ISC`
- `LGPL-2`
- `LGPL-2+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris libwmf=0.2.13-1.1
'http://deb.debian.org/debian/pool/main/libw/libwmf/libwmf_0.2.13-1.1.dsc' libwmf_0.2.13-1.1.dsc 2345 SHA256:05907248aae50ef26e44f518b628008b86cb8666513e568473fb62dfdee504af
'http://deb.debian.org/debian/pool/main/libw/libwmf/libwmf_0.2.13.orig.tar.gz' libwmf_0.2.13.orig.tar.gz 3044235 SHA256:18ba69febd2f515d98a2352de284a8051896062ac9728d2ead07bc39ea75a068
'http://deb.debian.org/debian/pool/main/libw/libwmf/libwmf_0.2.13-1.1.debian.tar.xz' libwmf_0.2.13-1.1.debian.tar.xz 25784 SHA256:0032481fbf98810ca446ab8931392acd13bfee29d1df4000fb783b7126f8e0f4
```

Other potentially useful URLs:

- https://sources.debian.net/src/libwmf/0.2.13-1.1/ (for browsing the source)
- https://sources.debian.net/src/libwmf/0.2.13-1.1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libwmf/0.2.13-1.1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libx11=2:1.8.7-1`

Binary Packages:

- `libx11-6:amd64=2:1.8.7-1+b1`
- `libx11-data=2:1.8.7-1`
- `libx11-dev:amd64=2:1.8.7-1+b1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libx11=2:1.8.7-1
'http://deb.debian.org/debian/pool/main/libx/libx11/libx11_1.8.7-1.dsc' libx11_1.8.7-1.dsc 2480 SHA256:96eddec7e55ab344ce654c5043d59bc8da6470eb7849a578c843af965dda79d1
'http://deb.debian.org/debian/pool/main/libx/libx11/libx11_1.8.7.orig.tar.gz' libx11_1.8.7.orig.tar.gz 3185363 SHA256:793ebebf569f12c864b77401798d38814b51790fce206e01a431e5feb982e20b
'http://deb.debian.org/debian/pool/main/libx/libx11/libx11_1.8.7.orig.tar.gz.asc' libx11_1.8.7.orig.tar.gz.asc 833 SHA256:c1cba69555c89e503abac81ebf1113a756f2fafd72677e7862b40f12208e0260
'http://deb.debian.org/debian/pool/main/libx/libx11/libx11_1.8.7-1.diff.gz' libx11_1.8.7-1.diff.gz 74344 SHA256:57adc62acb0ba21a4cf444aaf03ea4adc7f732215df22afa8b8d6fd31d799d95
```

Other potentially useful URLs:

- https://sources.debian.net/src/libx11/2:1.8.7-1/ (for browsing the source)
- https://sources.debian.net/src/libx11/2:1.8.7-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libx11/2:1.8.7-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libxau=1:1.0.9-1`

Binary Packages:

- `libxau-dev:amd64=1:1.0.9-1+b1`
- `libxau6:amd64=1:1.0.9-1+b1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxau=1:1.0.9-1
'http://deb.debian.org/debian/pool/main/libx/libxau/libxau_1.0.9-1.dsc' libxau_1.0.9-1.dsc 2183 SHA256:e6e059652cda7e5a49b6c9a70667639f32d629c20320487d16c642a06c1ebf85
'http://deb.debian.org/debian/pool/main/libx/libxau/libxau_1.0.9.orig.tar.gz' libxau_1.0.9.orig.tar.gz 394068 SHA256:1f123d8304b082ad63a9e89376400a3b1d4c29e67e3ea07b3f659cccca690eea
'http://deb.debian.org/debian/pool/main/libx/libxau/libxau_1.0.9.orig.tar.gz.asc' libxau_1.0.9.orig.tar.gz.asc 801 SHA256:af6104aaf3c5ede529e381237dd60f49640ec96593a84502fa493b86582b2f04
'http://deb.debian.org/debian/pool/main/libx/libxau/libxau_1.0.9-1.diff.gz' libxau_1.0.9-1.diff.gz 10193 SHA256:7b34899563f172e8f11d061de41b58fe1c32f8683d985e57686677ccb7299a9a
```

Other potentially useful URLs:

- https://sources.debian.net/src/libxau/1:1.0.9-1/ (for browsing the source)
- https://sources.debian.net/src/libxau/1:1.0.9-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libxau/1:1.0.9-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libxcb=1.17.0-2`

Binary Packages:

- `libxcb-render0:amd64=1.17.0-2`
- `libxcb-render0-dev:amd64=1.17.0-2`
- `libxcb-shm0:amd64=1.17.0-2`
- `libxcb-shm0-dev:amd64=1.17.0-2`
- `libxcb1:amd64=1.17.0-2`
- `libxcb1-dev:amd64=1.17.0-2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxcb=1.17.0-2
'http://deb.debian.org/debian/pool/main/libx/libxcb/libxcb_1.17.0-2.dsc' libxcb_1.17.0-2.dsc 5318 SHA256:b2728d156f79d2e757e7378cfcefca52bd570739d2efffa87e1aaeaf4f21de3a
'http://deb.debian.org/debian/pool/main/libx/libxcb/libxcb_1.17.0.orig.tar.gz' libxcb_1.17.0.orig.tar.gz 661593 SHA256:2c69287424c9e2128cb47ffe92171e10417041ec2963bceafb65cb3fcf8f0b85
'http://deb.debian.org/debian/pool/main/libx/libxcb/libxcb_1.17.0-2.diff.gz' libxcb_1.17.0-2.diff.gz 28069 SHA256:c5b33b67a61d0d1c1b624bf88a8150f4be1ba9b46e855e38f03a8f73858af558
```

Other potentially useful URLs:

- https://sources.debian.net/src/libxcb/1.17.0-2/ (for browsing the source)
- https://sources.debian.net/src/libxcb/1.17.0-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libxcb/1.17.0-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libxcrypt=1:4.4.36-4`

Binary Packages:

- `libcrypt-dev:amd64=1:4.4.36-4`
- `libcrypt1:amd64=1:4.4.36-4`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxcrypt=1:4.4.36-4
'http://deb.debian.org/debian/pool/main/libx/libxcrypt/libxcrypt_4.4.36-4.dsc' libxcrypt_4.4.36-4.dsc 1563 SHA256:8509256bf6ddedebfaf14ad777541d225a6c956f590602f85f5639efc652bfef
'http://deb.debian.org/debian/pool/main/libx/libxcrypt/libxcrypt_4.4.36.orig.tar.xz' libxcrypt_4.4.36.orig.tar.xz 392732 SHA256:7b7abbc89f13f5194211aa6861ed954e4fa3a210a4cb64f7e13dc8cf413e7f2a
'http://deb.debian.org/debian/pool/main/libx/libxcrypt/libxcrypt_4.4.36-4.debian.tar.xz' libxcrypt_4.4.36-4.debian.tar.xz 8216 SHA256:e61d8a486e6a80a2e3d629296988f8ff2e4dfbef018ec7e94543b5918ca1f329
```

Other potentially useful URLs:

- https://sources.debian.net/src/libxcrypt/1:4.4.36-4/ (for browsing the source)
- https://sources.debian.net/src/libxcrypt/1:4.4.36-4/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libxcrypt/1:4.4.36-4/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libxdmcp=1:1.1.2-3`

Binary Packages:

- `libxdmcp-dev:amd64=1:1.1.2-3+b1`
- `libxdmcp6:amd64=1:1.1.2-3+b1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxdmcp=1:1.1.2-3
'http://deb.debian.org/debian/pool/main/libx/libxdmcp/libxdmcp_1.1.2-3.dsc' libxdmcp_1.1.2-3.dsc 2145 SHA256:f9697dca6a275aeee9a3eee9fb2d55e0f77485481e8b84efc6950fc9b1988460
'http://deb.debian.org/debian/pool/main/libx/libxdmcp/libxdmcp_1.1.2.orig.tar.gz' libxdmcp_1.1.2.orig.tar.gz 404115 SHA256:6f7c7e491a23035a26284d247779174dedc67e34e93cc3548b648ffdb6fc57c0
'http://deb.debian.org/debian/pool/main/libx/libxdmcp/libxdmcp_1.1.2-3.diff.gz' libxdmcp_1.1.2-3.diff.gz 18017 SHA256:5844df115c17e5ba40ac116f80373304d821c607e763ef6f40562421f5cc0cf3
```

Other potentially useful URLs:

- https://sources.debian.net/src/libxdmcp/1:1.1.2-3/ (for browsing the source)
- https://sources.debian.net/src/libxdmcp/1:1.1.2-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libxdmcp/1:1.1.2-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libxext=2:1.3.4-1`

Binary Packages:

- `libxext-dev:amd64=2:1.3.4-1+b1`
- `libxext6:amd64=2:1.3.4-1+b1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxext=2:1.3.4-1
'http://deb.debian.org/debian/pool/main/libx/libxext/libxext_1.3.4-1.dsc' libxext_1.3.4-1.dsc 2118 SHA256:25024f57d955739c6b858822bf93ec3c71400b56fc0d666826f440e3661fd7c0
'http://deb.debian.org/debian/pool/main/libx/libxext/libxext_1.3.4.orig.tar.gz' libxext_1.3.4.orig.tar.gz 494434 SHA256:8ef0789f282826661ff40a8eef22430378516ac580167da35cc948be9041aac1
'http://deb.debian.org/debian/pool/main/libx/libxext/libxext_1.3.4-1.diff.gz' libxext_1.3.4-1.diff.gz 12509 SHA256:b975870d6a7b791ffbe2d57efdf6e20c250c5e76d12e45b04c8655f593bb8337
```

Other potentially useful URLs:

- https://sources.debian.net/src/libxext/2:1.3.4-1/ (for browsing the source)
- https://sources.debian.net/src/libxext/2:1.3.4-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libxext/2:1.3.4-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libxml2=2.12.7+dfsg-3`

Binary Packages:

- `libxml2:amd64=2.12.7+dfsg-3+b1`
- `libxml2-dev:amd64=2.12.7+dfsg-3+b1`

Licenses: (parsed from: `/usr/share/doc/libxml2/copyright`, `/usr/share/doc/libxml2-dev/copyright`)

- `ISC`
- `MIT-1`

Source:

```console
$ apt-get source -qq --print-uris libxml2=2.12.7+dfsg-3
'http://deb.debian.org/debian/pool/main/libx/libxml2/libxml2_2.12.7%2bdfsg-3.dsc' libxml2_2.12.7+dfsg-3.dsc 2594 SHA256:cf0fcf8d484250f7e667f943866fd0c75d5237b92386fad7b9d3e159292ad724
'http://deb.debian.org/debian/pool/main/libx/libxml2/libxml2_2.12.7%2bdfsg.orig.tar.xz' libxml2_2.12.7+dfsg.orig.tar.xz 1810596 SHA256:133559b73cc1995c6d5678bca51781e0f68e7a09cf859abad8dea326fca342e4
'http://deb.debian.org/debian/pool/main/libx/libxml2/libxml2_2.12.7%2bdfsg-3.debian.tar.xz' libxml2_2.12.7+dfsg-3.debian.tar.xz 27652 SHA256:3d5850caec7d8e2336a6b21c280d513c9e1ac1b9524dc13f98561c52c9025221
```

Other potentially useful URLs:

- https://sources.debian.net/src/libxml2/2.12.7+dfsg-3/ (for browsing the source)
- https://sources.debian.net/src/libxml2/2.12.7+dfsg-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libxml2/2.12.7+dfsg-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libxrender=1:0.9.10-1.1`

Binary Packages:

- `libxrender-dev:amd64=1:0.9.10-1.1+b1`
- `libxrender1:amd64=1:0.9.10-1.1+b1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxrender=1:0.9.10-1.1
'http://deb.debian.org/debian/pool/main/libx/libxrender/libxrender_0.9.10-1.1.dsc' libxrender_0.9.10-1.1.dsc 2072 SHA256:348ab15d05f1d802da485e4c6abdb9d5419691fb7c8ce44ca5b17b2b7f889ce8
'http://deb.debian.org/debian/pool/main/libx/libxrender/libxrender_0.9.10.orig.tar.gz' libxrender_0.9.10.orig.tar.gz 373717 SHA256:770527cce42500790433df84ec3521e8bf095dfe5079454a92236494ab296adf
'http://deb.debian.org/debian/pool/main/libx/libxrender/libxrender_0.9.10-1.1.diff.gz' libxrender_0.9.10-1.1.diff.gz 15201 SHA256:caf8c84085b3b0d073f738fa12d32d4eca2d8b669cb3c7f1b1cd2ce64b7b10b7
```

Other potentially useful URLs:

- https://sources.debian.net/src/libxrender/1:0.9.10-1.1/ (for browsing the source)
- https://sources.debian.net/src/libxrender/1:0.9.10-1.1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libxrender/1:0.9.10-1.1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libxslt=1.1.35-1.1`

Binary Packages:

- `libxslt1-dev:amd64=1.1.35-1.1`
- `libxslt1.1:amd64=1.1.35-1.1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxslt=1.1.35-1.1
'http://deb.debian.org/debian/pool/main/libx/libxslt/libxslt_1.1.35-1.1.dsc' libxslt_1.1.35-1.1.dsc 2163 SHA256:102a6976eb833e719d34339e4a8346553d89325b8850c4fad0942a58aad03abe
'http://deb.debian.org/debian/pool/main/libx/libxslt/libxslt_1.1.35.orig.tar.xz' libxslt_1.1.35.orig.tar.xz 1827548 SHA256:8247f33e9a872c6ac859aa45018bc4c4d00b97e2feac9eebc10c93ce1f34dd79
'http://deb.debian.org/debian/pool/main/libx/libxslt/libxslt_1.1.35-1.1.debian.tar.xz' libxslt_1.1.35-1.1.debian.tar.xz 22212 SHA256:6e7107620dc85c9d16e2650297cb1f86fe3e38ad0ee8d646e90fc3608f522eaf
```

Other potentially useful URLs:

- https://sources.debian.net/src/libxslt/1.1.35-1.1/ (for browsing the source)
- https://sources.debian.net/src/libxslt/1.1.35-1.1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libxslt/1.1.35-1.1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libxt=1:1.2.1-1.2`

Binary Packages:

- `libxt-dev:amd64=1:1.2.1-1.2`
- `libxt6t64:amd64=1:1.2.1-1.2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxt=1:1.2.1-1.2
'http://deb.debian.org/debian/pool/main/libx/libxt/libxt_1.2.1-1.2.dsc' libxt_1.2.1-1.2.dsc 2373 SHA256:780be4cf9b0b90757758691dc8196d85322b30a599c36fb8fe368b7060c7b774
'http://deb.debian.org/debian/pool/main/libx/libxt/libxt_1.2.1.orig.tar.gz' libxt_1.2.1.orig.tar.gz 1024473 SHA256:6da1bfa9dd0ed87430a5ce95b129485086394df308998ebe34d98e378e3dfb33
'http://deb.debian.org/debian/pool/main/libx/libxt/libxt_1.2.1.orig.tar.gz.asc' libxt_1.2.1.orig.tar.gz.asc 358 SHA256:da406cc94c25ca6773bb37c2055e2eb5665491f7ca6dfc9ea04f0f30ea3fd098
'http://deb.debian.org/debian/pool/main/libx/libxt/libxt_1.2.1-1.2.diff.gz' libxt_1.2.1-1.2.diff.gz 45635 SHA256:d4c510871909584398d88552b69cc5e92e124098ce544be93ef1743d0d112d4c
```

Other potentially useful URLs:

- https://sources.debian.net/src/libxt/1:1.2.1-1.2/ (for browsing the source)
- https://sources.debian.net/src/libxt/1:1.2.1-1.2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libxt/1:1.2.1-1.2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libyaml=0.2.5-1`

Binary Packages:

- `libyaml-0-2:amd64=0.2.5-1+b1`
- `libyaml-dev:amd64=0.2.5-1+b1`

Licenses: (parsed from: `/usr/share/doc/libyaml-0-2/copyright`, `/usr/share/doc/libyaml-dev/copyright`)

- `Expat`
- `permissive`

Source:

```console
$ apt-get source -qq --print-uris libyaml=0.2.5-1
'http://deb.debian.org/debian/pool/main/liby/libyaml/libyaml_0.2.5-1.dsc' libyaml_0.2.5-1.dsc 2071 SHA256:1edbf86e5cd76937ff62892ba6c2537456d645d834d4cd4a82430b8be7051bf4
'http://deb.debian.org/debian/pool/main/liby/libyaml/libyaml_0.2.5.orig.tar.gz' libyaml_0.2.5.orig.tar.gz 85055 SHA256:fa240dbf262be053f3898006d502d514936c818e422afdcf33921c63bed9bf2e
'http://deb.debian.org/debian/pool/main/liby/libyaml/libyaml_0.2.5-1.debian.tar.xz' libyaml_0.2.5-1.debian.tar.xz 5324 SHA256:8730e0510129e516c3c7c1cda7428e02a0a122699e57ed203f835a338a686d1f
```

Other potentially useful URLs:

- https://sources.debian.net/src/libyaml/0.2.5-1/ (for browsing the source)
- https://sources.debian.net/src/libyaml/0.2.5-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libyaml/0.2.5-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libzstd=1.5.6+dfsg-1`

Binary Packages:

- `libzstd-dev:amd64=1.5.6+dfsg-1`
- `libzstd1:amd64=1.5.6+dfsg-1`

Licenses: (parsed from: `/usr/share/doc/libzstd-dev/copyright`, `/usr/share/doc/libzstd1/copyright`)

- `BSD-3-clause`
- `Expat`
- `GPL-2`
- `zlib`

Source:

```console
$ apt-get source -qq --print-uris libzstd=1.5.6+dfsg-1
'http://deb.debian.org/debian/pool/main/libz/libzstd/libzstd_1.5.6%2bdfsg-1.dsc' libzstd_1.5.6+dfsg-1.dsc 2369 SHA256:c1774527814630f8e3ec1a6025d6b7a188ceccee002815ed143c3653e3b0b510
'http://deb.debian.org/debian/pool/main/libz/libzstd/libzstd_1.5.6%2bdfsg.orig.tar.xz' libzstd_1.5.6+dfsg.orig.tar.xz 1815380 SHA256:b3a60c7059886641830adf32c979be8d211da5d73fd05c7768f86d12d5bccec3
'http://deb.debian.org/debian/pool/main/libz/libzstd/libzstd_1.5.6%2bdfsg-1.debian.tar.xz' libzstd_1.5.6+dfsg-1.debian.tar.xz 22624 SHA256:33e540298d9fa29e12426a66e4b0b7715b3143659d16246e09c33f2fb69bad17
```

Other potentially useful URLs:

- https://sources.debian.net/src/libzstd/1.5.6+dfsg-1/ (for browsing the source)
- https://sources.debian.net/src/libzstd/1.5.6+dfsg-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libzstd/1.5.6+dfsg-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `linux=6.9.10-1`

Binary Packages:

- `linux-libc-dev=6.9.10-1`

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
$ apt-get source -qq --print-uris linux=6.9.10-1
'http://deb.debian.org/debian/pool/main/l/linux/linux_6.9.10-1.dsc' linux_6.9.10-1.dsc 232044 SHA256:ad77373a342b900a68a8c9c47b61d4afb52cb954a81d784e3cc30fc9459e2438
'http://deb.debian.org/debian/pool/main/l/linux/linux_6.9.10.orig.tar.xz' linux_6.9.10.orig.tar.xz 146876388 SHA256:794f1f8f737eeab4002e3ec7f2e4466cfaadd96ff0b0bb37df2dd573ac398f29
'http://deb.debian.org/debian/pool/main/l/linux/linux_6.9.10-1.debian.tar.xz' linux_6.9.10-1.debian.tar.xz 1550368 SHA256:1863636e8d7bc6ef5bd3cb175343d7fa7ee10eb3410fc1d49e78f06d6ffaeb45
```

Other potentially useful URLs:

- https://sources.debian.net/src/linux/6.9.10-1/ (for browsing the source)
- https://sources.debian.net/src/linux/6.9.10-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/linux/6.9.10-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `lz4=1.9.4-2`

Binary Packages:

- `liblz4-1:amd64=1.9.4-2`

Licenses: (parsed from: `/usr/share/doc/liblz4-1/copyright`)

- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/lz4/1.9.4-2/


### `dpkg` source package: `lzo2=2.10-3`

Binary Packages:

- `liblzo2-2:amd64=2.10-3`

Licenses: (parsed from: `/usr/share/doc/liblzo2-2/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris lzo2=2.10-3
'http://deb.debian.org/debian/pool/main/l/lzo2/lzo2_2.10-3.dsc' lzo2_2.10-3.dsc 1923 SHA256:d3efa3ce5107bafda50ca2769e4ad896a34f7ed0b70600c1d986d6937898786c
'http://deb.debian.org/debian/pool/main/l/lzo2/lzo2_2.10.orig.tar.gz' lzo2_2.10.orig.tar.gz 600622 SHA256:c0f892943208266f9b6543b3ae308fab6284c5c90e627931446fb49b4221a072
'http://deb.debian.org/debian/pool/main/l/lzo2/lzo2_2.10-3.debian.tar.xz' lzo2_2.10-3.debian.tar.xz 7228 SHA256:cf18b57e9a0a5c5f816facd5905e5c8dce0f99d2598b8416dab46b0064ba2cd2
```

Other potentially useful URLs:

- https://sources.debian.net/src/lzo2/2.10-3/ (for browsing the source)
- https://sources.debian.net/src/lzo2/2.10-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/lzo2/2.10-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `m4=1.4.19-4`

Binary Packages:

- `m4=1.4.19-4`

Licenses: (parsed from: `/usr/share/doc/m4/copyright`)

- `GFDL`
- `GPL`

Source:

```console
$ apt-get source -qq --print-uris m4=1.4.19-4
'http://deb.debian.org/debian/pool/main/m/m4/m4_1.4.19-4.dsc' m4_1.4.19-4.dsc 1637 SHA256:a52a24925928296b2574462d72bb1393e0cd54527a1ed2278aa2708bac543176
'http://deb.debian.org/debian/pool/main/m/m4/m4_1.4.19.orig.tar.xz' m4_1.4.19.orig.tar.xz 1654908 SHA256:63aede5c6d33b6d9b13511cd0be2cac046f2e70fd0a07aa9573a04a82783af96
'http://deb.debian.org/debian/pool/main/m/m4/m4_1.4.19.orig.tar.xz.asc' m4_1.4.19.orig.tar.xz.asc 488 SHA256:9700ba4dca539b06e033b4e3ab37fa5b983becb6c14569a8b8aa02dee6ab666c
'http://deb.debian.org/debian/pool/main/m/m4/m4_1.4.19-4.debian.tar.xz' m4_1.4.19-4.debian.tar.xz 17308 SHA256:c3fe8fe88dc5ba0d4dc114bea085dbc8421b7044b566a9a60b23499ff174c72f
```

Other potentially useful URLs:

- https://sources.debian.net/src/m4/1.4.19-4/ (for browsing the source)
- https://sources.debian.net/src/m4/1.4.19-4/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/m4/1.4.19-4/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `make-dfsg=4.3-4.1`

Binary Packages:

- `make=4.3-4.1`

Licenses: (parsed from: `/usr/share/doc/make/copyright`)

- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris make-dfsg=4.3-4.1
'http://deb.debian.org/debian/pool/main/m/make-dfsg/make-dfsg_4.3-4.1.dsc' make-dfsg_4.3-4.1.dsc 2019 SHA256:d2523d94f4d4198df6801f238d36cf0dea2ab5521f1d19ee76b2e8ee1f1918bb
'http://deb.debian.org/debian/pool/main/m/make-dfsg/make-dfsg_4.3.orig.tar.gz' make-dfsg_4.3.orig.tar.gz 1845906 SHA256:be4c17542578824e745f83bcd2a9ba264206187247cb6a5f5df99b0a9d1f9047
'http://deb.debian.org/debian/pool/main/m/make-dfsg/make-dfsg_4.3-4.1.diff.gz' make-dfsg_4.3-4.1.diff.gz 50940 SHA256:753c254ecaba425ebe2e0a0fb4d299847701e1c3eeb43df563e39975cae56b4c
```

Other potentially useful URLs:

- https://sources.debian.net/src/make-dfsg/4.3-4.1/ (for browsing the source)
- https://sources.debian.net/src/make-dfsg/4.3-4.1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/make-dfsg/4.3-4.1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `mariadb=1:11.4.2-4`

Binary Packages:

- `libmariadb-dev=1:11.4.2-4`
- `libmariadb-dev-compat=1:11.4.2-4`
- `libmariadb3:amd64=1:11.4.2-4`
- `mariadb-common=1:11.4.2-4`

Licenses: (parsed from: `/usr/share/doc/libmariadb-dev/copyright`, `/usr/share/doc/libmariadb-dev-compat/copyright`, `/usr/share/doc/libmariadb3/copyright`, `/usr/share/doc/mariadb-common/copyright`)

- `Artistic`
- `BSD-2-Clause`
- `BSD-2-clause`
- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`
- `GPL-2+-with-bison-exception`
- `GPL-3+-with-bison-exception`
- `LGPL`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `SWsoft`
- `public-domain`
- `unlimited-free-doc`
- `zlib/libpng`

Source:

```console
$ apt-get source -qq --print-uris mariadb=1:11.4.2-4
'http://deb.debian.org/debian/pool/main/m/mariadb/mariadb_11.4.2-4.dsc' mariadb_11.4.2-4.dsc 5632 SHA256:dac33e7519506e5786c902eedc87cf5f4f5e20c396f1245a69ea2f57931d6e30
'http://deb.debian.org/debian/pool/main/m/mariadb/mariadb_11.4.2.orig.tar.gz' mariadb_11.4.2.orig.tar.gz 107373265 SHA256:8c600e38adb899316c1cb11c68b87979668f4fb9d858000e347e6d8b7abe51b0
'http://deb.debian.org/debian/pool/main/m/mariadb/mariadb_11.4.2.orig.tar.gz.asc' mariadb_11.4.2.orig.tar.gz.asc 833 SHA256:d35fc7c4e63e402e1cdaac6a6cd7adf1f461834f5c34d4630515e6cd70c58a4f
'http://deb.debian.org/debian/pool/main/m/mariadb/mariadb_11.4.2-4.debian.tar.xz' mariadb_11.4.2-4.debian.tar.xz 281052 SHA256:9bc15c9451dc9bcd8168ba254ed25b1511d3b519590768e6eecedc615f005c60
```

Other potentially useful URLs:

- https://sources.debian.net/src/mariadb/1:11.4.2-4/ (for browsing the source)
- https://sources.debian.net/src/mariadb/1:11.4.2-4/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/mariadb/1:11.4.2-4/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/m/mawk/mawk_1.3.4.20240622-2.dsc' mawk_1.3.4.20240622-2.dsc 2969 SHA256:cc95afc29fa8e4406f42cd3887de7a10b9d70a84d70341d4e7c962438686db2f
'http://deb.debian.org/debian/pool/main/m/mawk/mawk_1.3.4.20240622.orig.tar.gz' mawk_1.3.4.20240622.orig.tar.gz 414190 SHA256:4e917e87a7a9fbaf76995784a4b0b5dc0dd954b977d0983030f78f6a07b1a765
'http://deb.debian.org/debian/pool/main/m/mawk/mawk_1.3.4.20240622.orig.tar.gz.asc' mawk_1.3.4.20240622.orig.tar.gz.asc 729 SHA256:1c66d8d18bf562d492a3b33a379c51ec80e111f8203a9546969fd7e436cb7041
'http://deb.debian.org/debian/pool/main/m/mawk/mawk_1.3.4.20240622-2.debian.tar.xz' mawk_1.3.4.20240622-2.debian.tar.xz 16136 SHA256:66d5c0f334acce8cd329f3807252d19c53b6b3cecbbf4d42d7c239f54f3ad296
```

Other potentially useful URLs:

- https://sources.debian.net/src/mawk/1.3.4.20240622-2/ (for browsing the source)
- https://sources.debian.net/src/mawk/1.3.4.20240622-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/mawk/1.3.4.20240622-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `media-types=10.1.0`

Binary Packages:

- `media-types=10.1.0`

Licenses: (parsed from: `/usr/share/doc/media-types/copyright`)

- `ad-hoc`

Source:

```console
$ apt-get source -qq --print-uris media-types=10.1.0
'http://deb.debian.org/debian/pool/main/m/media-types/media-types_10.1.0.dsc' media-types_10.1.0.dsc 1624 SHA256:1470ba869117eed57ba24c1e54664116a7ab6b4417e4b911e8c8051ffe19d626
'http://deb.debian.org/debian/pool/main/m/media-types/media-types_10.1.0.tar.xz' media-types_10.1.0.tar.xz 59052 SHA256:c35ec1ae0d0446aa903322f8f91a908a0d4270444326bfbad24b61fbe5600a0d
```

Other potentially useful URLs:

- https://sources.debian.net/src/media-types/10.1.0/ (for browsing the source)
- https://sources.debian.net/src/media-types/10.1.0/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/media-types/10.1.0/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `mercurial=6.8-3`

Binary Packages:

- `mercurial=6.8-3`
- `mercurial-common=6.8-3`

Licenses: (parsed from: `/usr/share/doc/mercurial/copyright`, `/usr/share/doc/mercurial-common/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris mercurial=6.8-3
'http://deb.debian.org/debian/pool/main/m/mercurial/mercurial_6.8-3.dsc' mercurial_6.8-3.dsc 2786 SHA256:051145ba1b2692c0c925729eaa717457a8a89614d54b2ceb3248ee4d114dc1c2
'http://deb.debian.org/debian/pool/main/m/mercurial/mercurial_6.8.orig.tar.gz' mercurial_6.8.orig.tar.gz 8322075 SHA256:08e4d0e5da8af1132b51e6bc3350180ad57adcd935f097b6d0bc119a2c2c0a10
'http://deb.debian.org/debian/pool/main/m/mercurial/mercurial_6.8.orig.tar.gz.asc' mercurial_6.8.orig.tar.gz.asc 659 SHA256:7cda2cb212a21ad66713ac7699442d542add753959059cd4acec33c761d10181
'http://deb.debian.org/debian/pool/main/m/mercurial/mercurial_6.8-3.debian.tar.xz' mercurial_6.8-3.debian.tar.xz 54960 SHA256:483041fa1b832b20a941abe6b6b593126921b64ccc17b0312b8693bcf448cfe9
```

Other potentially useful URLs:

- https://sources.debian.net/src/mercurial/6.8-3/ (for browsing the source)
- https://sources.debian.net/src/mercurial/6.8-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/mercurial/6.8-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `mpclib3=1.3.1-1`

Binary Packages:

- `libmpc3:amd64=1.3.1-1+b2`

Licenses: (parsed from: `/usr/share/doc/libmpc3/copyright`)

- `LGPL-3`

Source:

```console
$ apt-get source -qq --print-uris mpclib3=1.3.1-1
'http://deb.debian.org/debian/pool/main/m/mpclib3/mpclib3_1.3.1-1.dsc' mpclib3_1.3.1-1.dsc 1877 SHA256:b2252a499fd0f8e92ce2cf7d8e68477ffc9dd06127803a91f0a1115822efec75
'http://deb.debian.org/debian/pool/main/m/mpclib3/mpclib3_1.3.1.orig.tar.gz' mpclib3_1.3.1.orig.tar.gz 773573 SHA256:ab642492f5cf882b74aa0cb730cd410a81edcdbec895183ce930e706c1c759b8
'http://deb.debian.org/debian/pool/main/m/mpclib3/mpclib3_1.3.1-1.debian.tar.xz' mpclib3_1.3.1-1.debian.tar.xz 4656 SHA256:25adb496258adacad69c022d712f96fbc465bcef9fd4751829dc351d9ce6a45d
```

Other potentially useful URLs:

- https://sources.debian.net/src/mpclib3/1.3.1-1/ (for browsing the source)
- https://sources.debian.net/src/mpclib3/1.3.1-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/mpclib3/1.3.1-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `mpfr4=4.2.1-1`

Binary Packages:

- `libmpfr6:amd64=4.2.1-1+b1`

Licenses: (parsed from: `/usr/share/doc/libmpfr6/copyright`)

- `GFDL-1.2`
- `LGPL-3`

Source:

```console
$ apt-get source -qq --print-uris mpfr4=4.2.1-1
'http://deb.debian.org/debian/pool/main/m/mpfr4/mpfr4_4.2.1-1.dsc' mpfr4_4.2.1-1.dsc 1959 SHA256:2fb0ea6c37591f03c7f3445fc6a298a10dbd9d7662ccb441f7da0e514d71986a
'http://deb.debian.org/debian/pool/main/m/mpfr4/mpfr4_4.2.1.orig.tar.xz' mpfr4_4.2.1.orig.tar.xz 1493608 SHA256:277807353a6726978996945af13e52829e3abd7a9a5b7fb2793894e18f1fcbb2
'http://deb.debian.org/debian/pool/main/m/mpfr4/mpfr4_4.2.1-1.debian.tar.xz' mpfr4_4.2.1-1.debian.tar.xz 12556 SHA256:06c6c90efe3653d44527bcd6cfd66563d62409bbb348eb32f33b480e30ad9993
```

Other potentially useful URLs:

- https://sources.debian.net/src/mpfr4/4.2.1-1/ (for browsing the source)
- https://sources.debian.net/src/mpfr4/4.2.1-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/mpfr4/4.2.1-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `mysql-defaults=1.1.1`

Binary Packages:

- `default-libmysqlclient-dev:amd64=1.1.1`
- `mysql-common=5.8+1.1.1`

Licenses: (parsed from: `/usr/share/doc/default-libmysqlclient-dev/copyright`, `/usr/share/doc/mysql-common/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris mysql-defaults=1.1.1
'http://deb.debian.org/debian/pool/main/m/mysql-defaults/mysql-defaults_1.1.1.dsc' mysql-defaults_1.1.1.dsc 2202 SHA256:4fd91907a56a2251e2e0dc0faa37c52299a2ae8d68e457cd250ac29d160090f1
'http://deb.debian.org/debian/pool/main/m/mysql-defaults/mysql-defaults_1.1.1.tar.xz' mysql-defaults_1.1.1.tar.xz 7460 SHA256:054d8da3bfd3419081a7ccb795ad614c235e8aa06674c5588cb88973467c1cdc
```

Other potentially useful URLs:

- https://sources.debian.net/src/mysql-defaults/1.1.1/ (for browsing the source)
- https://sources.debian.net/src/mysql-defaults/1.1.1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/mysql-defaults/1.1.1/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/n/ncurses/ncurses_6.5-2.dsc' ncurses_6.5-2.dsc 3799 SHA256:c55a25d4697a881a12f98d9e69448a879fca1391663768822a7cc981b62b2b4c
'http://deb.debian.org/debian/pool/main/n/ncurses/ncurses_6.5.orig.tar.gz' ncurses_6.5.orig.tar.gz 3688489 SHA256:136d91bc269a9a5785e5f9e980bc76ab57428f604ce3e5a5a90cebc767971cc6
'http://deb.debian.org/debian/pool/main/n/ncurses/ncurses_6.5.orig.tar.gz.asc' ncurses_6.5.orig.tar.gz.asc 729 SHA256:c7541cdb9e27c159548d6ab2115b4e923d06d174dce7307f4a943de9421f3751
'http://deb.debian.org/debian/pool/main/n/ncurses/ncurses_6.5-2.debian.tar.xz' ncurses_6.5-2.debian.tar.xz 49852 SHA256:19df80accc1c6d978ca54eba2542ea77248e7a894bbf42a093aee0b4981fddf3
```

Other potentially useful URLs:

- https://sources.debian.net/src/ncurses/6.5-2/ (for browsing the source)
- https://sources.debian.net/src/ncurses/6.5-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/ncurses/6.5-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `netbase=6.4`

Binary Packages:

- `netbase=6.4`

Licenses: (parsed from: `/usr/share/doc/netbase/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris netbase=6.4
'http://deb.debian.org/debian/pool/main/n/netbase/netbase_6.4.dsc' netbase_6.4.dsc 898 SHA256:dc26cfcaa49fd874cc27c65216b2f8b6d3ad62845b78da4bdf0aea55592af756
'http://deb.debian.org/debian/pool/main/n/netbase/netbase_6.4.tar.xz' netbase_6.4.tar.xz 32712 SHA256:fa6621826ff1150e581bd90bc3c8a4ecafe5df90404f207db6dcdf2c75f26ad7
```

Other potentially useful URLs:

- https://sources.debian.net/src/netbase/6.4/ (for browsing the source)
- https://sources.debian.net/src/netbase/6.4/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/netbase/6.4/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/n/nettle/nettle_3.10-1.dsc' nettle_3.10-1.dsc 2276 SHA256:25c9563ad861d8c62246687cc1aaace7d897db0e1aa287ef68485b89687aa739
'http://deb.debian.org/debian/pool/main/n/nettle/nettle_3.10.orig.tar.gz' nettle_3.10.orig.tar.gz 2640485 SHA256:b4c518adb174e484cb4acea54118f02380c7133771e7e9beb98a0787194ee47c
'http://deb.debian.org/debian/pool/main/n/nettle/nettle_3.10.orig.tar.gz.asc' nettle_3.10.orig.tar.gz.asc 573 SHA256:83f20f4bb5cc18335dacab8b8d01ddbae1b28453d889c5efcc2123987a8e09ca
'http://deb.debian.org/debian/pool/main/n/nettle/nettle_3.10-1.debian.tar.xz' nettle_3.10-1.debian.tar.xz 24936 SHA256:fd7181ca135b8a560b048ffba5b9f75e2ce7d0d61d3223c278c77ea89500b660
```

Other potentially useful URLs:

- https://sources.debian.net/src/nettle/3.10-1/ (for browsing the source)
- https://sources.debian.net/src/nettle/3.10-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/nettle/3.10-1/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/n/nghttp2/nghttp2_1.62.1-2.dsc' nghttp2_1.62.1-2.dsc 2531 SHA256:5f457052ee3dad45dce4848fc5bc25106fd5e519972de5788b0841e07e31aee5
'http://deb.debian.org/debian/pool/main/n/nghttp2/nghttp2_1.62.1.orig.tar.gz' nghttp2_1.62.1.orig.tar.gz 1066103 SHA256:73c8af772dd2b30cedc114d37291cf1485b0a7ce11833595fc2aec7b3ce3ba5c
'http://deb.debian.org/debian/pool/main/n/nghttp2/nghttp2_1.62.1-2.debian.tar.xz' nghttp2_1.62.1-2.debian.tar.xz 38852 SHA256:82131a80852fcc53d378d4e3cb0e27d0b6044ac595d01806b807713942fbfcac
```

Other potentially useful URLs:

- https://sources.debian.net/src/nghttp2/1.62.1-2/ (for browsing the source)
- https://sources.debian.net/src/nghttp2/1.62.1-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/nghttp2/1.62.1-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `nghttp3=1.3.0-2`

Binary Packages:

- `libnghttp3-9:amd64=1.3.0-2`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/nghttp3/1.3.0-2/


### `dpkg` source package: `ngtcp2=1.5.0-2`

Binary Packages:

- `libngtcp2-16:amd64=1.5.0-2`
- `libngtcp2-crypto-gnutls8:amd64=1.5.0-2`

Licenses: (parsed from: `/usr/share/doc/libngtcp2-16/copyright`, `/usr/share/doc/libngtcp2-crypto-gnutls8/copyright`)

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/ngtcp2/1.5.0-2/


### `dpkg` source package: `npth=1.6-3.1`

Binary Packages:

- `libnpth0t64:amd64=1.6-3.1`

Licenses: (parsed from: `/usr/share/doc/libnpth0t64/copyright`)

- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris npth=1.6-3.1
'http://deb.debian.org/debian/pool/main/n/npth/npth_1.6-3.1.dsc' npth_1.6-3.1.dsc 1967 SHA256:3545fbabbf59c9427a6dc98f903f4ac50786fdfc2ce3f42a21668ec3151c25f7
'http://deb.debian.org/debian/pool/main/n/npth/npth_1.6.orig.tar.bz2' npth_1.6.orig.tar.bz2 300486 SHA256:1393abd9adcf0762d34798dc34fdcf4d0d22a8410721e76f1e3afcd1daa4e2d1
'http://deb.debian.org/debian/pool/main/n/npth/npth_1.6-3.1.debian.tar.xz' npth_1.6-3.1.debian.tar.xz 10924 SHA256:e2fb2f56060991436622ddc1dc52df8f3f3e87bc9325a8b30920fce5aa0f3e30
```

Other potentially useful URLs:

- https://sources.debian.net/src/npth/1.6-3.1/ (for browsing the source)
- https://sources.debian.net/src/npth/1.6-3.1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/npth/1.6-3.1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `openexr=3.1.5-5.1`

Binary Packages:

- `libopenexr-3-1-30:amd64=3.1.5-5.1+b2`
- `libopenexr-dev=3.1.5-5.1+b2`

Licenses: (parsed from: `/usr/share/doc/libopenexr-3-1-30/copyright`, `/usr/share/doc/libopenexr-dev/copyright`)

- `BSD-3-clause`
- `openexr`

Source:

```console
$ apt-get source -qq --print-uris openexr=3.1.5-5.1
'http://deb.debian.org/debian/pool/main/o/openexr/openexr_3.1.5-5.1.dsc' openexr_3.1.5-5.1.dsc 2489 SHA256:aca9636b9d8c54158342ba15547a01d86765203ce94af9e404924c39df54d040
'http://deb.debian.org/debian/pool/main/o/openexr/openexr_3.1.5.orig.tar.gz' openexr_3.1.5.orig.tar.gz 20327926 SHA256:93925805c1fc4f8162b35f0ae109c4a75344e6decae5a240afdfce25f8a433ec
'http://deb.debian.org/debian/pool/main/o/openexr/openexr_3.1.5.orig.tar.gz.asc' openexr_3.1.5.orig.tar.gz.asc 287 SHA256:a2c4ac5151789903ca8ab3093a2798491463ccf2abfd003a20f96453e505dd5f
'http://deb.debian.org/debian/pool/main/o/openexr/openexr_3.1.5-5.1.debian.tar.xz' openexr_3.1.5-5.1.debian.tar.xz 18828 SHA256:f4ab9368399d9915e122b6b2da5962c1832c58dac20564fa6c88b1c8c70fdf40
```

Other potentially useful URLs:

- https://sources.debian.net/src/openexr/3.1.5-5.1/ (for browsing the source)
- https://sources.debian.net/src/openexr/3.1.5-5.1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/openexr/3.1.5-5.1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `openjpeg2=2.5.0-2`

Binary Packages:

- `libopenjp2-7:amd64=2.5.0-2+b3`
- `libopenjp2-7-dev:amd64=2.5.0-2+b3`

Licenses: (parsed from: `/usr/share/doc/libopenjp2-7/copyright`, `/usr/share/doc/libopenjp2-7-dev/copyright`)

- `BSD-2`
- `BSD-3`
- `LIBPNG`
- `LIBTIFF`
- `LIBTIFF-GLARSON`
- `LIBTIFF-PIXAR`
- `MIT`
- `ZLIB`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris openjpeg2=2.5.0-2
'http://deb.debian.org/debian/pool/main/o/openjpeg2/openjpeg2_2.5.0-2.dsc' openjpeg2_2.5.0-2.dsc 2673 SHA256:c29fc2afc7bf6fa1a3d02e9c78dd2159db2ef12a5fe62bc786500c91f01ffc04
'http://deb.debian.org/debian/pool/main/o/openjpeg2/openjpeg2_2.5.0.orig.tar.xz' openjpeg2_2.5.0.orig.tar.xz 1221108 SHA256:007e19d772c8b6b22e35379630b06ff3549e49ba719d96453607a36ad7b4de73
'http://deb.debian.org/debian/pool/main/o/openjpeg2/openjpeg2_2.5.0-2.debian.tar.xz' openjpeg2_2.5.0-2.debian.tar.xz 17388 SHA256:7bedc8ba24e39dddc65e3e87f70c5dcced44661d360379efd5077fd24333ee9c
```

Other potentially useful URLs:

- https://sources.debian.net/src/openjpeg2/2.5.0-2/ (for browsing the source)
- https://sources.debian.net/src/openjpeg2/2.5.0-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/openjpeg2/2.5.0-2/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/o/openldap/openldap_2.5.18%2bdfsg-2.dsc' openldap_2.5.18+dfsg-2.dsc 3312 SHA256:0825ff7a10b669bce5b31199ec4a2dcf018080011a1c1020774cec734b465a45
'http://deb.debian.org/debian/pool/main/o/openldap/openldap_2.5.18%2bdfsg.orig.tar.xz' openldap_2.5.18+dfsg.orig.tar.xz 3684372 SHA256:06c2f0ee591594ae28cfbde843a70b3e009b1f09d7f3110a1570236ac46a86b5
'http://deb.debian.org/debian/pool/main/o/openldap/openldap_2.5.18%2bdfsg-2.debian.tar.xz' openldap_2.5.18+dfsg-2.debian.tar.xz 170128 SHA256:a3606da0c79d9f34a7cae36dac835ffd2ccdd4eda51eea1fdf6d209698fcfc13
```

Other potentially useful URLs:

- https://sources.debian.net/src/openldap/2.5.18+dfsg-2/ (for browsing the source)
- https://sources.debian.net/src/openldap/2.5.18+dfsg-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/openldap/2.5.18+dfsg-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `openssh=1:9.7p1-7`

Binary Packages:

- `openssh-client=1:9.7p1-7`

Licenses: (parsed from: `/usr/share/doc/openssh-client/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `Expat-with-advertising-restriction`
- `Mazieres-BSD-style`
- `OpenSSH`
- `Powell-BSD-style`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/openssh/1:9.7p1-7/


### `dpkg` source package: `openssl=3.2.2-1`

Binary Packages:

- `libssl-dev:amd64=3.2.2-1`
- `libssl3t64:amd64=3.2.2-1`
- `openssl=3.2.2-1`

Licenses: (parsed from: `/usr/share/doc/libssl-dev/copyright`, `/usr/share/doc/libssl3t64/copyright`, `/usr/share/doc/openssl/copyright`)

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
'http://deb.debian.org/debian/pool/main/p/pam/pam_1.5.3-7.dsc' pam_1.5.3-7.dsc 2253 SHA256:05666dde2c8057ff436975a5da7dad91210ab5a5dfdaea43976ac4a6bc75b1e7
'http://deb.debian.org/debian/pool/main/p/pam/pam_1.5.3.orig.tar.xz' pam_1.5.3.orig.tar.xz 1020076 SHA256:7ac4b50feee004a9fa88f1dfd2d2fa738a82896763050cd773b3c54b0a818283
'http://deb.debian.org/debian/pool/main/p/pam/pam_1.5.3.orig.tar.xz.asc' pam_1.5.3.orig.tar.xz.asc 801 SHA256:ce5690766060d60a8f0fba447f480d8d49988821740698cbdf2ecfd84dc8895c
'http://deb.debian.org/debian/pool/main/p/pam/pam_1.5.3-7.debian.tar.xz' pam_1.5.3-7.debian.tar.xz 139288 SHA256:494106a8f40a5436b82f8955e04a83598439b48636f16a30d0b6a32d86d0fc61
```

Other potentially useful URLs:

- https://sources.debian.net/src/pam/1.5.3-7/ (for browsing the source)
- https://sources.debian.net/src/pam/1.5.3-7/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/pam/1.5.3-7/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/p/pango1.0/pango1.0_1.54.0%2bds-1.dsc' pango1.0_1.54.0+ds-1.dsc 3514 SHA256:e29894677383fc7f080936665c98eda9fcc5de9bab9266911e18c28f1f90f2c5
'http://deb.debian.org/debian/pool/main/p/pango1.0/pango1.0_1.54.0%2bds.orig.tar.xz' pango1.0_1.54.0+ds.orig.tar.xz 1745280 SHA256:2275f1160e492b442a7dfbaa10cf8aeaea83cea1ff0ee1eed9d88fa1e21aebe8
'http://deb.debian.org/debian/pool/main/p/pango1.0/pango1.0_1.54.0%2bds-1.debian.tar.xz' pango1.0_1.54.0+ds-1.debian.tar.xz 43584 SHA256:99f63d649520792c5761757ab914c48b53be9fd747049ff516da7d8d257c86dc
```

Other potentially useful URLs:

- https://sources.debian.net/src/pango1.0/1.54.0+ds-1/ (for browsing the source)
- https://sources.debian.net/src/pango1.0/1.54.0+ds-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/pango1.0/1.54.0+ds-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `patch=2.7.6-7`

Binary Packages:

- `patch=2.7.6-7`

Licenses: (parsed from: `/usr/share/doc/patch/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris patch=2.7.6-7
'http://deb.debian.org/debian/pool/main/p/patch/patch_2.7.6-7.dsc' patch_2.7.6-7.dsc 1706 SHA256:d954fd576d935ac54b7d44d4976eb52d0da84a57f7bad90c6e5bd5e33595030a
'http://deb.debian.org/debian/pool/main/p/patch/patch_2.7.6.orig.tar.xz' patch_2.7.6.orig.tar.xz 783756 SHA256:ac610bda97abe0d9f6b7c963255a11dcb196c25e337c61f94e4778d632f1d8fd
'http://deb.debian.org/debian/pool/main/p/patch/patch_2.7.6-7.debian.tar.xz' patch_2.7.6-7.debian.tar.xz 15084 SHA256:7725f30b042d8cf63516e480036e93ca2ff0ce5ad3754db4a4e69d33e96a2624
```

Other potentially useful URLs:

- https://sources.debian.net/src/patch/2.7.6-7/ (for browsing the source)
- https://sources.debian.net/src/patch/2.7.6-7/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/patch/2.7.6-7/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/p/pcre2/pcre2_10.42-4.dsc' pcre2_10.42-4.dsc 2302 SHA256:2796d9332a4b4abe5eeada4aa287e8f9765a497b4363e3c49815a6bca5845cfe
'http://deb.debian.org/debian/pool/main/p/pcre2/pcre2_10.42.orig.tar.gz' pcre2_10.42.orig.tar.gz 2397194 SHA256:c33b418e3b936ee3153de2c61cc638e7e4fe3156022a5c77d0711bcbb9d64f1f
'http://deb.debian.org/debian/pool/main/p/pcre2/pcre2_10.42-4.diff.gz' pcre2_10.42-4.diff.gz 8111 SHA256:b583a75e90b029616c6867eccfeb21031e62df98dd4462f9d13ccb95bb2f09e6
```

Other potentially useful URLs:

- https://sources.debian.net/src/pcre2/10.42-4/ (for browsing the source)
- https://sources.debian.net/src/pcre2/10.42-4/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/pcre2/10.42-4/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/p/perl/perl_5.38.2-5.dsc' perl_5.38.2-5.dsc 2938 SHA256:c3d9624788c42bcf14003bd110013858906279596a487735cc39494778070137
'http://deb.debian.org/debian/pool/main/p/perl/perl_5.38.2.orig-regen-configure.tar.xz' perl_5.38.2.orig-regen-configure.tar.xz 418808 SHA256:4d1b34cc058f9963cb89785ecc040d57f6d7725cd83329cfa4ef8b27566454d2
'http://deb.debian.org/debian/pool/main/p/perl/perl_5.38.2.orig.tar.xz' perl_5.38.2.orig.tar.xz 13679524 SHA256:d91115e90b896520e83d4de6b52f8254ef2b70a8d545ffab33200ea9f1cf29e8
'http://deb.debian.org/debian/pool/main/p/perl/perl_5.38.2-5.debian.tar.xz' perl_5.38.2-5.debian.tar.xz 168016 SHA256:ef455488cb518f06cb10f3ed927b05e86df347ed22942874bd3f08a197047b0a
```

Other potentially useful URLs:

- https://sources.debian.net/src/perl/5.38.2-5/ (for browsing the source)
- https://sources.debian.net/src/perl/5.38.2-5/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/perl/5.38.2-5/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `pinentry=1.2.1-3`

Binary Packages:

- `pinentry-curses=1.2.1-3+b2`

Licenses: (parsed from: `/usr/share/doc/pinentry-curses/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-3`
- `LGPL-3+`
- `X11`

Source:

```console
$ apt-get source -qq --print-uris pinentry=1.2.1-3
'http://deb.debian.org/debian/pool/main/p/pinentry/pinentry_1.2.1-3.dsc' pinentry_1.2.1-3.dsc 3170 SHA256:679a692b8a34c68a9146869347a09164d952a4b79dd2daa6ca20a1caa6aed8e8
'http://deb.debian.org/debian/pool/main/p/pinentry/pinentry_1.2.1.orig.tar.bz2' pinentry_1.2.1.orig.tar.bz2 547698 SHA256:457a185e5a85238fb945a955dc6352ab962dc8b48720b62fc9fa48c7540a4067
'http://deb.debian.org/debian/pool/main/p/pinentry/pinentry_1.2.1.orig.tar.bz2.asc' pinentry_1.2.1.orig.tar.bz2.asc 390 SHA256:9f7d9c7509e4ff4161a043893d76183bd975230fcad671b643c90f78e500ba95
'http://deb.debian.org/debian/pool/main/p/pinentry/pinentry_1.2.1-3.debian.tar.xz' pinentry_1.2.1-3.debian.tar.xz 18864 SHA256:7919390ebf6fdf2f8e4e05231bc1348edb119396d29d66718478775bb4c9a0ba
```

Other potentially useful URLs:

- https://sources.debian.net/src/pinentry/1.2.1-3/ (for browsing the source)
- https://sources.debian.net/src/pinentry/1.2.1-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/pinentry/1.2.1-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `pixman=0.42.2-1`

Binary Packages:

- `libpixman-1-0:amd64=0.42.2-1+b1`
- `libpixman-1-dev:amd64=0.42.2-1+b1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris pixman=0.42.2-1
'http://deb.debian.org/debian/pool/main/p/pixman/pixman_0.42.2-1.dsc' pixman_0.42.2-1.dsc 2021 SHA256:393302f5ba22d1206c456902baa02cdd577cb74fe35ec6659f587cce67b91b3d
'http://deb.debian.org/debian/pool/main/p/pixman/pixman_0.42.2.orig.tar.gz' pixman_0.42.2.orig.tar.gz 959669 SHA256:ea1480efada2fd948bc75366f7c349e1c96d3297d09a3fe62626e38e234a625e
'http://deb.debian.org/debian/pool/main/p/pixman/pixman_0.42.2-1.diff.gz' pixman_0.42.2-1.diff.gz 319616 SHA256:dd6472676c68260a298e52f45c485d3cc85c4bf25df8af0f68e37acff7bfed8a
```

Other potentially useful URLs:

- https://sources.debian.net/src/pixman/0.42.2-1/ (for browsing the source)
- https://sources.debian.net/src/pixman/0.42.2-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/pixman/0.42.2-1/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/p/pkgconf/pkgconf_1.8.1-3.dsc' pkgconf_1.8.1-3.dsc 1638 SHA256:8c103ef4a3e65c6e1559a2e3534e623b32e925e455d32396b06b4dc9231403f2
'http://deb.debian.org/debian/pool/main/p/pkgconf/pkgconf_1.8.1.orig.tar.xz' pkgconf_1.8.1.orig.tar.xz 302372 SHA256:644361ada2942be05655d4452eb018791647c31bba429b287f1f68deb2dc6840
'http://deb.debian.org/debian/pool/main/p/pkgconf/pkgconf_1.8.1-3.debian.tar.xz' pkgconf_1.8.1-3.debian.tar.xz 15852 SHA256:d1527b3fccaf4c63e50cef4057f64c13a4c30591995fb9e6a58f4f928338f095
```

Other potentially useful URLs:

- https://sources.debian.net/src/pkgconf/1.8.1-3/ (for browsing the source)
- https://sources.debian.net/src/pkgconf/1.8.1-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/pkgconf/1.8.1-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `postgresql-16=16.3-1`

Binary Packages:

- `libpq-dev=16.3-1+b1`
- `libpq5:amd64=16.3-1+b1`

Licenses: (parsed from: `/usr/share/doc/libpq-dev/copyright`, `/usr/share/doc/libpq5/copyright`)

- `Artistic`
- `BSD-2-clause`
- `BSD-3-Clause`
- `BSD-3-clause`
- `Custom-Unicode`
- `Custom-pg_dump`
- `Custom-regex`
- `GPL-1`
- `PostgreSQL`
- `Tcl`
- `double-metaphone`
- `nagaysau-ishii`

Source:

```console
$ apt-get source -qq --print-uris postgresql-16=16.3-1
'http://deb.debian.org/debian/pool/main/p/postgresql-16/postgresql-16_16.3-1.dsc' postgresql-16_16.3-1.dsc 4237 SHA256:e0e58b8ff4305155b99f510f95ed48bc163d7b686572e432e1074ae865e6ec21
'http://deb.debian.org/debian/pool/main/p/postgresql-16/postgresql-16_16.3.orig.tar.bz2' postgresql-16_16.3.orig.tar.bz2 24737644 SHA256:331963d5d3dc4caf4216a049fa40b66d6bcb8c730615859411b9518764e60585
'http://deb.debian.org/debian/pool/main/p/postgresql-16/postgresql-16_16.3-1.debian.tar.xz' postgresql-16_16.3-1.debian.tar.xz 31856 SHA256:fda53b9c8d539d0437b8ccd99b0b379bc5a068d87104b94150c0b9e538ee405f
```

Other potentially useful URLs:

- https://sources.debian.net/src/postgresql-16/16.3-1/ (for browsing the source)
- https://sources.debian.net/src/postgresql-16/16.3-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/postgresql-16/16.3-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `procps=2:4.0.4-5`

Binary Packages:

- `libproc2-0:amd64=2:4.0.4-5`
- `procps=2:4.0.4-5`

Licenses: (parsed from: `/usr/share/doc/libproc2-0/copyright`, `/usr/share/doc/procps/copyright`)

- `GPL-2`
- `GPL-2.0+`
- `LGPL-2`
- `LGPL-2.0+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris procps=2:4.0.4-5
'http://deb.debian.org/debian/pool/main/p/procps/procps_4.0.4-5.dsc' procps_4.0.4-5.dsc 2124 SHA256:aae3a3e796c488d1ba06f0cb5d2d0f36d1fd5c741fb293618197e95c1bf04f03
'http://deb.debian.org/debian/pool/main/p/procps/procps_4.0.4.orig.tar.xz' procps_4.0.4.orig.tar.xz 1401540 SHA256:22870d6feb2478adb617ce4f09a787addaf2d260c5a8aa7b17d889a962c5e42e
'http://deb.debian.org/debian/pool/main/p/procps/procps_4.0.4-5.debian.tar.xz' procps_4.0.4-5.debian.tar.xz 29300 SHA256:4e489d908bcda90e9f74434cdae7d8beb2bfd289e624321e4d8d8be45c68879e
```

Other potentially useful URLs:

- https://sources.debian.net/src/procps/2:4.0.4-5/ (for browsing the source)
- https://sources.debian.net/src/procps/2:4.0.4-5/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/procps/2:4.0.4-5/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `python-packaging=24.1-1`

Binary Packages:

- `python3-packaging=24.1-1`

Licenses: (parsed from: `/usr/share/doc/python3-packaging/copyright`)

- `Apache-2.0`
- `BSD-3-clause`

Source:

```console
$ apt-get source -qq --print-uris python-packaging=24.1-1
'http://deb.debian.org/debian/pool/main/p/python-packaging/python-packaging_24.1-1.dsc' python-packaging_24.1-1.dsc 1932 SHA256:5488568ea7de9ef6489087021d495d82a49604e9bad0728a82d256c966cec97f
'http://deb.debian.org/debian/pool/main/p/python-packaging/python-packaging_24.1.orig.tar.gz' python-packaging_24.1.orig.tar.gz 148788 SHA256:026ed72c8ed3fcce5bf8950572258698927fd1dbda10a5e981cdf0ac37f4f002
'http://deb.debian.org/debian/pool/main/p/python-packaging/python-packaging_24.1-1.debian.tar.xz' python-packaging_24.1-1.debian.tar.xz 2948 SHA256:1aeb604044c1e0178b062cf12412b558ab26e865789c62d09cf6b4b11f6d5e13
```

Other potentially useful URLs:

- https://sources.debian.net/src/python-packaging/24.1-1/ (for browsing the source)
- https://sources.debian.net/src/python-packaging/24.1-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/python-packaging/24.1-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `python3-defaults=3.12.4-1`

Binary Packages:

- `libpython3-stdlib:amd64=3.12.4-1`
- `python3=3.12.4-1`
- `python3-minimal=3.12.4-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris python3-defaults=3.12.4-1
'http://deb.debian.org/debian/pool/main/p/python3-defaults/python3-defaults_3.12.4-1.dsc' python3-defaults_3.12.4-1.dsc 2988 SHA256:b146253d3fffdf0a1bddc485aed8f2e1d83b501a376d7184587086e8907c7728
'http://deb.debian.org/debian/pool/main/p/python3-defaults/python3-defaults_3.12.4-1.tar.gz' python3-defaults_3.12.4-1.tar.gz 146851 SHA256:5ed419073282df22cddeb50a44b36f5607104d52999b93525dcd3970ea9a478f
```

Other potentially useful URLs:

- https://sources.debian.net/src/python3-defaults/3.12.4-1/ (for browsing the source)
- https://sources.debian.net/src/python3-defaults/3.12.4-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/python3-defaults/3.12.4-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `python3.12=3.12.4-3`

Binary Packages:

- `libpython3.12-minimal:amd64=3.12.4-3`
- `libpython3.12-stdlib:amd64=3.12.4-3`
- `python3.12=3.12.4-3`
- `python3.12-minimal=3.12.4-3`

Licenses: (parsed from: `/usr/share/doc/libpython3.12-minimal/copyright`, `/usr/share/doc/libpython3.12-stdlib/copyright`, `/usr/share/doc/python3.12/copyright`, `/usr/share/doc/python3.12-minimal/copyright`)

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
$ apt-get source -qq --print-uris python3.12=3.12.4-3
'http://deb.debian.org/debian/pool/main/p/python3.12/python3.12_3.12.4-3.dsc' python3.12_3.12.4-3.dsc 3761 SHA256:1da1d5ae9ee8e9e7b8476cb51e3a96d9ccf758e6cc37e6fdc96668fb40970ed2
'http://deb.debian.org/debian/pool/main/p/python3.12/python3.12_3.12.4.orig.tar.xz' python3.12_3.12.4.orig.tar.xz 20659356 SHA256:f6d419a6d8743ab26700801b4908d26d97e8b986e14f95de31b32de2b0e79554
'http://deb.debian.org/debian/pool/main/p/python3.12/python3.12_3.12.4-3.debian.tar.xz' python3.12_3.12.4-3.debian.tar.xz 293772 SHA256:1126e7f05d3e32cd59770ddd934a3462e1b1e8bc7e293e8b733298677db6c94d
```

Other potentially useful URLs:

- https://sources.debian.net/src/python3.12/3.12.4-3/ (for browsing the source)
- https://sources.debian.net/src/python3.12/3.12.4-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/python3.12/3.12.4-3/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/r/readline/readline_8.2-4.dsc' readline_8.2-4.dsc 2811 SHA256:c363fc6bc293a4bbb429e89f069eefbff99c754a6e41fcd1b967db6848ea321d
'http://deb.debian.org/debian/pool/main/r/readline/readline_8.2.orig.tar.gz' readline_8.2.orig.tar.gz 3043952 SHA256:3feb7171f16a84ee82ca18a36d7b9be109a52c04f492a053331d7d1095007c35
'http://deb.debian.org/debian/pool/main/r/readline/readline_8.2-4.debian.tar.xz' readline_8.2-4.debian.tar.xz 33700 SHA256:dcd6d20ed594b864fc8d964f4f3a76dfbfa22193c0fad6d095bfd3fadad4b8d9
```

Other potentially useful URLs:

- https://sources.debian.net/src/readline/8.2-4/ (for browsing the source)
- https://sources.debian.net/src/readline/8.2-4/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/readline/8.2-4/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/r/rpcsvc-proto/rpcsvc-proto_1.4.3-1.dsc' rpcsvc-proto_1.4.3-1.dsc 1999 SHA256:7d8e122bd18b02fe0de6d467a0ecdafff74035b3e1ed0da1c0c792d9c015682f
'http://deb.debian.org/debian/pool/main/r/rpcsvc-proto/rpcsvc-proto_1.4.3.orig.tar.xz' rpcsvc-proto_1.4.3.orig.tar.xz 167964 SHA256:69315e94430f4e79c74d43422f4a36e6259e97e67e2677b2c7d7060436bd99b1
'http://deb.debian.org/debian/pool/main/r/rpcsvc-proto/rpcsvc-proto_1.4.3-1.debian.tar.xz' rpcsvc-proto_1.4.3-1.debian.tar.xz 4228 SHA256:02034b9dadcf3af5424f72eb65c3842c8d7117b6b78e7a3c798316ceb60843d1
```

Other potentially useful URLs:

- https://sources.debian.net/src/rpcsvc-proto/1.4.3-1/ (for browsing the source)
- https://sources.debian.net/src/rpcsvc-proto/1.4.3-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/rpcsvc-proto/1.4.3-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `rtmpdump=2.4+20151223.gitfa8646d.1-2`

Binary Packages:

- `librtmp1:amd64=2.4+20151223.gitfa8646d.1-2+b4`

Licenses: (parsed from: `/usr/share/doc/librtmp1/copyright`)

- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris rtmpdump=2.4+20151223.gitfa8646d.1-2
'http://deb.debian.org/debian/pool/main/r/rtmpdump/rtmpdump_2.4%2b20151223.gitfa8646d.1-2.dsc' rtmpdump_2.4+20151223.gitfa8646d.1-2.dsc 2299 SHA256:a296819cd2ab5880b67ad963ef0867cb10e462f4403e52565aa863eb05bb1370
'http://deb.debian.org/debian/pool/main/r/rtmpdump/rtmpdump_2.4%2b20151223.gitfa8646d.1.orig.tar.gz' rtmpdump_2.4+20151223.gitfa8646d.1.orig.tar.gz 142213 SHA256:5c032f5c8cc2937eb55a81a94effdfed3b0a0304b6376147b86f951e225e3ab5
'http://deb.debian.org/debian/pool/main/r/rtmpdump/rtmpdump_2.4%2b20151223.gitfa8646d.1-2.debian.tar.xz' rtmpdump_2.4+20151223.gitfa8646d.1-2.debian.tar.xz 8096 SHA256:26d47de07d16285e4ca55b0828cbbf1ba35e671f9b3500a87e301fe755d26882
```

Other potentially useful URLs:

- https://sources.debian.net/src/rtmpdump/2.4+20151223.gitfa8646d.1-2/ (for browsing the source)
- https://sources.debian.net/src/rtmpdump/2.4+20151223.gitfa8646d.1-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/rtmpdump/2.4+20151223.gitfa8646d.1-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `rust-sequoia-sq=0.33.0-3`

Binary Packages:

- `sq=0.33.0-3`

Licenses: (parsed from: `/usr/share/doc/sq/copyright`)

- `GPL-2`
- `GPL-2.0-or-later`
- `LGPL-2`
- `LGPL-2.0-or-later`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/rust-sequoia-sq/0.33.0-3/


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
'http://deb.debian.org/debian/pool/main/s/sed/sed_4.9-2.dsc' sed_4.9-2.dsc 1860 SHA256:17f10deac1b327cb2a623352cdc33444ac9c109359a0caa46b3980b0e415f671
'http://deb.debian.org/debian/pool/main/s/sed/sed_4.9.orig.tar.xz' sed_4.9.orig.tar.xz 1397092 SHA256:6e226b732e1cd739464ad6862bd1a1aba42d7982922da7a53519631d24975181
'http://deb.debian.org/debian/pool/main/s/sed/sed_4.9-2.debian.tar.xz' sed_4.9-2.debian.tar.xz 62756 SHA256:549fa5cec6eb4fde8cc74ca263b8bf42f947ede677e39d2afeedf661da1d4e52
```

Other potentially useful URLs:

- https://sources.debian.net/src/sed/4.9-2/ (for browsing the source)
- https://sources.debian.net/src/sed/4.9-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/sed/4.9-2/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/s/sensible-utils/sensible-utils_0.0.24.dsc' sensible-utils_0.0.24.dsc 1743 SHA256:f84ac7cccca8e0f3f9e5c0d5173c7d1f22afdc0a98210120d1d35a92b4baf9df
'http://deb.debian.org/debian/pool/main/s/sensible-utils/sensible-utils_0.0.24.tar.xz' sensible-utils_0.0.24.tar.xz 73568 SHA256:620602b900bad2b9856556a7895ea146110f602cd526a1cc03068a0bc9542803
```

Other potentially useful URLs:

- https://sources.debian.net/src/sensible-utils/0.0.24/ (for browsing the source)
- https://sources.debian.net/src/sensible-utils/0.0.24/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/sensible-utils/0.0.24/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `serf=1.3.10-3`

Binary Packages:

- `libserf-1-1:amd64=1.3.10-3`

Licenses: (parsed from: `/usr/share/doc/libserf-1-1/copyright`)

- `Apache`
- `Apache-2.0`
- `Zlib`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/serf/1.3.10-3/


### `dpkg` source package: `shadow=1:4.15.3-2`

Binary Packages:

- `login=1:4.15.3-2`
- `passwd=1:4.15.3-2`

Licenses: (parsed from: `/usr/share/doc/login/copyright`, `/usr/share/doc/passwd/copyright`)

- `BSD-3-clause`
- `GPL-1`
- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/shadow/1:4.15.3-2/


### `dpkg` source package: `shared-mime-info=2.4-5`

Binary Packages:

- `shared-mime-info=2.4-5`

Licenses: (parsed from: `/usr/share/doc/shared-mime-info/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris shared-mime-info=2.4-5
'http://deb.debian.org/debian/pool/main/s/shared-mime-info/shared-mime-info_2.4-5.dsc' shared-mime-info_2.4-5.dsc 2237 SHA256:daadcf9aadf96cb45875856d8046f692d1e563bda5687150d993f9deba274a39
'http://deb.debian.org/debian/pool/main/s/shared-mime-info/shared-mime-info_2.4.orig.tar.bz2' shared-mime-info_2.4.orig.tar.bz2 7096347 SHA256:32dc32ae39ff1c1bf8434dd3b36770b48538a1772bc0298509d034f057005992
'http://deb.debian.org/debian/pool/main/s/shared-mime-info/shared-mime-info_2.4-5.debian.tar.xz' shared-mime-info_2.4-5.debian.tar.xz 10812 SHA256:10eceaa29c5927dcc9cc9ba419f7bbdee68542cc5cfb3be15dde3e36735a3206
```

Other potentially useful URLs:

- https://sources.debian.net/src/shared-mime-info/2.4-5/ (for browsing the source)
- https://sources.debian.net/src/shared-mime-info/2.4-5/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/shared-mime-info/2.4-5/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `sqlite3=3.46.0-1`

Binary Packages:

- `libsqlite3-0:amd64=3.46.0-1`
- `libsqlite3-dev:amd64=3.46.0-1`

Licenses: (parsed from: `/usr/share/doc/libsqlite3-0/copyright`, `/usr/share/doc/libsqlite3-dev/copyright`)

- `GPL-2`
- `GPL-2+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris sqlite3=3.46.0-1
'http://deb.debian.org/debian/pool/main/s/sqlite3/sqlite3_3.46.0-1.dsc' sqlite3_3.46.0-1.dsc 2486 SHA256:a3670d98d23bba15261b67969e4f1634d4205e7c24182ad112b0e02f0fc0acc8
'http://deb.debian.org/debian/pool/main/s/sqlite3/sqlite3_3.46.0.orig-www.tar.xz' sqlite3_3.46.0.orig-www.tar.xz 5770196 SHA256:a0b01ec1240b617e2d15d564c77cabe15c74515a0e677c51ad92a85c2b7d477d
'http://deb.debian.org/debian/pool/main/s/sqlite3/sqlite3_3.46.0.orig.tar.xz' sqlite3_3.46.0.orig.tar.xz 8342408 SHA256:22f02709430f9622e2043b18cdb189cea2e24231a3127071fb064a23e9de2933
'http://deb.debian.org/debian/pool/main/s/sqlite3/sqlite3_3.46.0-1.debian.tar.xz' sqlite3_3.46.0-1.debian.tar.xz 30432 SHA256:ee1c6b293fd5e91ae4d5a14c1465ef5035afafcdef136902de3de43c75f77afb
```

Other potentially useful URLs:

- https://sources.debian.net/src/sqlite3/3.46.0-1/ (for browsing the source)
- https://sources.debian.net/src/sqlite3/3.46.0-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/sqlite3/3.46.0-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `subversion=1.14.3-2`

Binary Packages:

- `libsvn1:amd64=1.14.3-2+b1`
- `subversion=1.14.3-2+b1`

Licenses: (parsed from: `/usr/share/doc/libsvn1/copyright`, `/usr/share/doc/subversion/copyright`)

- `AFL-3`
- `Apache-2.0`
- `BSD-2-clause`
- `BSD-3-clause`
- `BoostAcMacros`
- `Expat`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `Svnwrap`
- `Unicode`
- `Utfwidth`

Source:

```console
$ apt-get source -qq --print-uris subversion=1.14.3-2
'http://deb.debian.org/debian/pool/main/s/subversion/subversion_1.14.3-2.dsc' subversion_1.14.3-2.dsc 4046 SHA256:c603f04a22bf8b3df99d697afa579540c3b7a4e7274cb925db0805d6c3bdf570
'http://deb.debian.org/debian/pool/main/s/subversion/subversion_1.14.3.orig.tar.gz' subversion_1.14.3.orig.tar.gz 11621442 SHA256:cf70775e5ed075ebc6a63fe8619dc6b530da254a3f61ba53a502dd83c8f14afc
'http://deb.debian.org/debian/pool/main/s/subversion/subversion_1.14.3.orig.tar.gz.asc' subversion_1.14.3.orig.tar.gz.asc 1724 SHA256:e0d93fb48ba707a201f32f350774797333013c7a53cd6c785665717f0e9cfbc5
'http://deb.debian.org/debian/pool/main/s/subversion/subversion_1.14.3-2.debian.tar.xz' subversion_1.14.3-2.debian.tar.xz 338424 SHA256:820de690b8c487b033a4e4742981a8f94d82b32e2181111e426730bc6bfa4777
```

Other potentially useful URLs:

- https://sources.debian.net/src/subversion/1.14.3-2/ (for browsing the source)
- https://sources.debian.net/src/subversion/1.14.3-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/subversion/1.14.3-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `sysprof=46.0-2`

Binary Packages:

- `libsysprof-capture-4-dev:amd64=46.0-2`

Licenses: (parsed from: `/usr/share/doc/libsysprof-capture-4-dev/copyright`)

- `BSD-2-Clause-Patent`
- `BSD-3-Clause`
- `GPL-2`
- `GPL-2.0+`
- `GPL-3`
- `GPL-3.0+`
- `LGPL-2`
- `LGPL-2.0+`
- `LGPL-3`
- `LGPL-3.0+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris sysprof=46.0-2
'http://deb.debian.org/debian/pool/main/s/sysprof/sysprof_46.0-2.dsc' sysprof_46.0-2.dsc 2811 SHA256:0ec16be42b10d3449062cc237fe627374b0eba92e944f7a3188720e951705436
'http://deb.debian.org/debian/pool/main/s/sysprof/sysprof_46.0.orig.tar.xz' sysprof_46.0.orig.tar.xz 1170396 SHA256:73aa7e75ebab3e4e0946a05a723df7e6ee4249e3b9e884dba35500aba2a1d176
'http://deb.debian.org/debian/pool/main/s/sysprof/sysprof_46.0-2.debian.tar.xz' sysprof_46.0-2.debian.tar.xz 16528 SHA256:f865661611882c9eb5b9c99f84eec004798ec9c7df5497e7f498af9a158e02ba
```

Other potentially useful URLs:

- https://sources.debian.net/src/sysprof/46.0-2/ (for browsing the source)
- https://sources.debian.net/src/sysprof/46.0-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/sysprof/46.0-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `systemd=256.2-1`

Binary Packages:

- `libsystemd0:amd64=256.2-1`
- `libudev1:amd64=256.2-1`

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

- http://snapshot.debian.org/package/systemd/256.2-1/


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

Source:

```console
$ apt-get source -qq --print-uris sysvinit=3.09-2
'http://deb.debian.org/debian/pool/main/s/sysvinit/sysvinit_3.09-2.dsc' sysvinit_3.09-2.dsc 2347 SHA256:5074f58c20f0eb7e4397964c1b0c6e235076ff951fcaf5918bad9235b2d65e87
'http://deb.debian.org/debian/pool/main/s/sysvinit/sysvinit_3.09.orig.tar.gz' sysvinit_3.09.orig.tar.gz 514145 SHA256:991c5d0100165d7896dae9df6a69877311cdd5349e32f7fc6960859f5f60a6ce
'http://deb.debian.org/debian/pool/main/s/sysvinit/sysvinit_3.09-2.debian.tar.xz' sysvinit_3.09-2.debian.tar.xz 121120 SHA256:35e587b8bf604e857037bf50d28be8169a25d3217f094b65baf98dd4c34719b0
```

Other potentially useful URLs:

- https://sources.debian.net/src/sysvinit/3.09-2/ (for browsing the source)
- https://sources.debian.net/src/sysvinit/3.09-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/sysvinit/3.09-2/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/t/tar/tar_1.35%2bdfsg-3.dsc' tar_1.35+dfsg-3.dsc 2009 SHA256:0ea713a8af04a41d297202e7ac20813735328a5f8d4de3882fba5595709955f8
'http://deb.debian.org/debian/pool/main/t/tar/tar_1.35%2bdfsg.orig.tar.xz' tar_1.35+dfsg.orig.tar.xz 2111608 SHA256:9ae57e981c1e73c0eebc2b26c9b0c4497fe310ef1d516ea430efb5470b71f7a8
'http://deb.debian.org/debian/pool/main/t/tar/tar_1.35%2bdfsg-3.debian.tar.xz' tar_1.35+dfsg-3.debian.tar.xz 20824 SHA256:6028f2172de2498b8fc2baef4854796d829ae7ba2a91de4f7615fe1a56729313
```

Other potentially useful URLs:

- https://sources.debian.net/src/tar/1.35+dfsg-3/ (for browsing the source)
- https://sources.debian.net/src/tar/1.35+dfsg-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/tar/1.35+dfsg-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `tiff=4.5.1+git230720-4`

Binary Packages:

- `libtiff-dev:amd64=4.5.1+git230720-4`
- `libtiff6:amd64=4.5.1+git230720-4`
- `libtiffxx6:amd64=4.5.1+git230720-4`

Licenses: (parsed from: `/usr/share/doc/libtiff-dev/copyright`, `/usr/share/doc/libtiff6/copyright`, `/usr/share/doc/libtiffxx6/copyright`)

- `Hylafax`

Source:

```console
$ apt-get source -qq --print-uris tiff=4.5.1+git230720-4
'http://deb.debian.org/debian/pool/main/t/tiff/tiff_4.5.1%2bgit230720-4.dsc' tiff_4.5.1+git230720-4.dsc 2322 SHA256:84f3fe1110e4633c897e63a6cc0122d2db3afb36140f089ec727ffe0f61facd1
'http://deb.debian.org/debian/pool/main/t/tiff/tiff_4.5.1%2bgit230720.orig.tar.xz' tiff_4.5.1+git230720.orig.tar.xz 1781896 SHA256:0e51bcf3a3ffa5fc76ea6aeb74a797f95c84544fcc8b6a1ec5def967a78e9e12
'http://deb.debian.org/debian/pool/main/t/tiff/tiff_4.5.1%2bgit230720-4.debian.tar.xz' tiff_4.5.1+git230720-4.debian.tar.xz 26260 SHA256:a4ba563349fe2e53759703dce1aa476cbb3621ab3b4389df97faf60dd06067ad
```

Other potentially useful URLs:

- https://sources.debian.net/src/tiff/4.5.1+git230720-4/ (for browsing the source)
- https://sources.debian.net/src/tiff/4.5.1+git230720-4/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/tiff/4.5.1+git230720-4/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `tzdata=2024a-4`

Binary Packages:

- `tzdata=2024a-4`

Licenses: (parsed from: `/usr/share/doc/tzdata/copyright`)

- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris tzdata=2024a-4
'http://deb.debian.org/debian/pool/main/t/tzdata/tzdata_2024a-4.dsc' tzdata_2024a-4.dsc 2429 SHA256:053c342511ece9a0eec2c9d60a6670dd9bce379dcb0bfad88d2167a2786ecb3f
'http://deb.debian.org/debian/pool/main/t/tzdata/tzdata_2024a.orig.tar.gz' tzdata_2024a.orig.tar.gz 451270 SHA256:0d0434459acbd2059a7a8da1f3304a84a86591f6ed69c6248fffa502b6edffe3
'http://deb.debian.org/debian/pool/main/t/tzdata/tzdata_2024a.orig.tar.gz.asc' tzdata_2024a.orig.tar.gz.asc 833 SHA256:f64725f9f65419e7b009e3b95b75ea9516382d0be64aef63d78654d9c569ed0d
'http://deb.debian.org/debian/pool/main/t/tzdata/tzdata_2024a-4.debian.tar.xz' tzdata_2024a-4.debian.tar.xz 124152 SHA256:ff5dbfa986ebcb1705ca0256163738c56538baf3a6778f53d616407d8da9ccac
```

Other potentially useful URLs:

- https://sources.debian.net/src/tzdata/2024a-4/ (for browsing the source)
- https://sources.debian.net/src/tzdata/2024a-4/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/tzdata/2024a-4/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `ucf=3.0043+nmu1`

Binary Packages:

- `ucf=3.0043+nmu1`

Licenses: (parsed from: `/usr/share/doc/ucf/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris ucf=3.0043+nmu1
'http://deb.debian.org/debian/pool/main/u/ucf/ucf_3.0043%2bnmu1.dsc' ucf_3.0043+nmu1.dsc 1567 SHA256:5ef70fa7a58cd3f162932661453a1e9d21d749b47a1aa84198f7c4cd9eac20ee
'http://deb.debian.org/debian/pool/main/u/ucf/ucf_3.0043%2bnmu1.tar.xz' ucf_3.0043+nmu1.tar.xz 70916 SHA256:a07143046236cb082517e346362306cb3fe4d3634cad1add40c905b0e0ecf58c
```

Other potentially useful URLs:

- https://sources.debian.net/src/ucf/3.0043+nmu1/ (for browsing the source)
- https://sources.debian.net/src/ucf/3.0043+nmu1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/ucf/3.0043+nmu1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `unzip=6.0-28`

Binary Packages:

- `unzip=6.0-28`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris unzip=6.0-28
'http://deb.debian.org/debian/pool/main/u/unzip/unzip_6.0-28.dsc' unzip_6.0-28.dsc 1359 SHA256:f5b486028b61a145b591fdd96aaeaf89ef6eef164a299f43bd5e6704bdefc8a2
'http://deb.debian.org/debian/pool/main/u/unzip/unzip_6.0.orig.tar.gz' unzip_6.0.orig.tar.gz 1376845 SHA256:036d96991646d0449ed0aa952e4fbe21b476ce994abc276e49d30e686708bd37
'http://deb.debian.org/debian/pool/main/u/unzip/unzip_6.0-28.debian.tar.xz' unzip_6.0-28.debian.tar.xz 25032 SHA256:e51364116c84739c591728ecc841113a914fa11358fd10ff0d6813524d811bb9
```

Other potentially useful URLs:

- https://sources.debian.net/src/unzip/6.0-28/ (for browsing the source)
- https://sources.debian.net/src/unzip/6.0-28/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/unzip/6.0-28/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `usrmerge=39`

Binary Packages:

- `usr-is-merged=39`

Licenses: (parsed from: `/usr/share/doc/usr-is-merged/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris usrmerge=39
'http://deb.debian.org/debian/pool/main/u/usrmerge/usrmerge_39.dsc' usrmerge_39.dsc 981 SHA256:44027067423faefd31ac321c283fc9b07184fecbd5304ed41490c03825b89a28
'http://deb.debian.org/debian/pool/main/u/usrmerge/usrmerge_39.tar.xz' usrmerge_39.tar.xz 14908 SHA256:90b4ee198469292da4ee8b4ce2ec7b3ec439d61e6beb3ed9d3fa82b0e46e7fa3
```

Other potentially useful URLs:

- https://sources.debian.net/src/usrmerge/39/ (for browsing the source)
- https://sources.debian.net/src/usrmerge/39/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/usrmerge/39/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `utf8proc=2.9.0-1`

Binary Packages:

- `libutf8proc3:amd64=2.9.0-1+b1`

Licenses: (parsed from: `/usr/share/doc/libutf8proc3/copyright`)

- `Expat`
- `Unicode`

Source:

```console
$ apt-get source -qq --print-uris utf8proc=2.9.0-1
'http://deb.debian.org/debian/pool/main/u/utf8proc/utf8proc_2.9.0-1.dsc' utf8proc_2.9.0-1.dsc 2187 SHA256:bb9fd54cb4584ee7c677901312608249f503aa910ca60db043d3273b86dd228a
'http://deb.debian.org/debian/pool/main/u/utf8proc/utf8proc_2.9.0.orig.tar.gz' utf8proc_2.9.0.orig.tar.gz 193465 SHA256:18c1626e9fc5a2e192311e36b3010bfc698078f692888940f1fa150547abb0c1
'http://deb.debian.org/debian/pool/main/u/utf8proc/utf8proc_2.9.0-1.debian.tar.xz' utf8proc_2.9.0-1.debian.tar.xz 5836 SHA256:b285489bb5d293ce24d2eea42450f3ef15ff13a23fc422de6a0cf5760872f789
```

Other potentially useful URLs:

- https://sources.debian.net/src/utf8proc/2.9.0-1/ (for browsing the source)
- https://sources.debian.net/src/utf8proc/2.9.0-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/utf8proc/2.9.0-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `util-linux=2.40.2-1`

Binary Packages:

- `bsdutils=1:2.40.2-1`
- `libblkid-dev:amd64=2.40.2-1`
- `libblkid1:amd64=2.40.2-1`
- `libmount-dev:amd64=2.40.2-1`
- `libmount1:amd64=2.40.2-1`
- `libsmartcols1:amd64=2.40.2-1`
- `libuuid1:amd64=2.40.2-1`
- `mount=2.40.2-1`
- `util-linux=2.40.2-1`
- `uuid-dev:amd64=2.40.2-1`

Licenses: (parsed from: `/usr/share/doc/bsdutils/copyright`, `/usr/share/doc/libblkid-dev/copyright`, `/usr/share/doc/libblkid1/copyright`, `/usr/share/doc/libmount-dev/copyright`, `/usr/share/doc/libmount1/copyright`, `/usr/share/doc/libsmartcols1/copyright`, `/usr/share/doc/libuuid1/copyright`, `/usr/share/doc/mount/copyright`, `/usr/share/doc/util-linux/copyright`, `/usr/share/doc/uuid-dev/copyright`)

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

- http://snapshot.debian.org/package/util-linux/2.40.2-1/


### `dpkg` source package: `wget=1.24.5-1`

Binary Packages:

- `wget=1.24.5-1`

Licenses: (parsed from: `/usr/share/doc/wget/copyright`)

- `GFDL-1.2`
- `GPL-3`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/wget/1.24.5-1/


### `dpkg` source package: `xorg-sgml-doctools=1:1.11-1.1`

Binary Packages:

- `xorg-sgml-doctools=1:1.11-1.1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris xorg-sgml-doctools=1:1.11-1.1
'http://deb.debian.org/debian/pool/main/x/xorg-sgml-doctools/xorg-sgml-doctools_1.11-1.1.dsc' xorg-sgml-doctools_1.11-1.1.dsc 1987 SHA256:6aac68e597386c10b02646d2026a833d301749a938701f4ca8efd4d19ad34295
'http://deb.debian.org/debian/pool/main/x/xorg-sgml-doctools/xorg-sgml-doctools_1.11.orig.tar.gz' xorg-sgml-doctools_1.11.orig.tar.gz 150367 SHA256:986326d7b4dd2ad298f61d8d41fe3929ac6191c6000d6d7e47a8ffc0c34e7426
'http://deb.debian.org/debian/pool/main/x/xorg-sgml-doctools/xorg-sgml-doctools_1.11-1.1.diff.gz' xorg-sgml-doctools_1.11-1.1.diff.gz 3296 SHA256:0c11e15d4f9aaacd38452a6a37d064f1a07058dcead7ab1e2aca223ec0a94d11
```

Other potentially useful URLs:

- https://sources.debian.net/src/xorg-sgml-doctools/1:1.11-1.1/ (for browsing the source)
- https://sources.debian.net/src/xorg-sgml-doctools/1:1.11-1.1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/xorg-sgml-doctools/1:1.11-1.1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `xorg=1:7.7+23.1`

Binary Packages:

- `x11-common=1:7.7+23.1`

Licenses: (parsed from: `/usr/share/doc/x11-common/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris xorg=1:7.7+23.1
'http://deb.debian.org/debian/pool/main/x/xorg/xorg_7.7%2b23.1.dsc' xorg_7.7+23.1.dsc 1983 SHA256:0d448530e9e3640a98bc3ac5840af8ab62f369bea0483eca9741d508987d19c1
'http://deb.debian.org/debian/pool/main/x/xorg/xorg_7.7%2b23.1.tar.gz' xorg_7.7+23.1.tar.gz 292366 SHA256:1620333d14424eadae77ef44ac702a65ef5b53c169c993181687ee1d198d538b
```

Other potentially useful URLs:

- https://sources.debian.net/src/xorg/1:7.7+23.1/ (for browsing the source)
- https://sources.debian.net/src/xorg/1:7.7+23.1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/xorg/1:7.7+23.1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `xorgproto=2024.1-1`

Binary Packages:

- `x11proto-core-dev=2024.1-1`
- `x11proto-dev=2024.1-1`

Licenses: (parsed from: `/usr/share/doc/x11proto-core-dev/copyright`, `/usr/share/doc/x11proto-dev/copyright`)

- `MIT`
- `SGI`

Source:

```console
$ apt-get source -qq --print-uris xorgproto=2024.1-1
'http://deb.debian.org/debian/pool/main/x/xorgproto/xorgproto_2024.1-1.dsc' xorgproto_2024.1-1.dsc 3336 SHA256:56c08773592f3cf529bc087449de421aac0645b5c43fad41387b856b5e29fab7
'http://deb.debian.org/debian/pool/main/x/xorgproto/xorgproto_2024.1.orig.tar.gz' xorgproto_2024.1.orig.tar.gz 1115486 SHA256:4f6b9b4faf91e5df8265b71843a91fc73dc895be6210c84117a996545df296ce
'http://deb.debian.org/debian/pool/main/x/xorgproto/xorgproto_2024.1.orig.tar.gz.asc' xorgproto_2024.1.orig.tar.gz.asc 195 SHA256:41d650fd19f3df1ae8ad24c2570638d5cdadff819613f8cff96d17310d35347c
'http://deb.debian.org/debian/pool/main/x/xorgproto/xorgproto_2024.1-1.diff.gz' xorgproto_2024.1-1.diff.gz 25061 SHA256:f250a5bc693079f84dc0caad3cc282433940d3665ff9a77b8dc4dc0961f83d1b
```

Other potentially useful URLs:

- https://sources.debian.net/src/xorgproto/2024.1-1/ (for browsing the source)
- https://sources.debian.net/src/xorgproto/2024.1-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/xorgproto/2024.1-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `xtrans=1.4.0-1`

Binary Packages:

- `xtrans-dev=1.4.0-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris xtrans=1.4.0-1
'http://deb.debian.org/debian/pool/main/x/xtrans/xtrans_1.4.0-1.dsc' xtrans_1.4.0-1.dsc 1919 SHA256:dd74ab9199e8f45215b566a9317cac7953bf063ce6893c185eccaf0fb4d84d8f
'http://deb.debian.org/debian/pool/main/x/xtrans/xtrans_1.4.0.orig.tar.gz' xtrans_1.4.0.orig.tar.gz 225941 SHA256:48ed850ce772fef1b44ca23639b0a57e38884045ed2cbb18ab137ef33ec713f9
'http://deb.debian.org/debian/pool/main/x/xtrans/xtrans_1.4.0-1.diff.gz' xtrans_1.4.0-1.diff.gz 9522 SHA256:0dac18165654d79e0796b80fab4c1104998d29e6d0b098af0426a1d72399521e
```

Other potentially useful URLs:

- https://sources.debian.net/src/xtrans/1.4.0-1/ (for browsing the source)
- https://sources.debian.net/src/xtrans/1.4.0-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/xtrans/1.4.0-1/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/x/xxhash/xxhash_0.8.2-2.dsc' xxhash_0.8.2-2.dsc 1969 SHA256:8fbf9f5a50a4cf48e771e157e386bd2b2938e46cecd4bc53117ee1a4a615af1d
'http://deb.debian.org/debian/pool/main/x/xxhash/xxhash_0.8.2.orig.tar.gz' xxhash_0.8.2.orig.tar.gz 1141188 SHA256:baee0c6afd4f03165de7a4e67988d16f0f2b257b51d0e3cb91909302a26a79c4
'http://deb.debian.org/debian/pool/main/x/xxhash/xxhash_0.8.2-2.debian.tar.xz' xxhash_0.8.2-2.debian.tar.xz 4920 SHA256:fcbdd52df60936173524743680f6d3c504b9a90553fe113cd0aa531faf4f2c4d
```

Other potentially useful URLs:

- https://sources.debian.net/src/xxhash/0.8.2-2/ (for browsing the source)
- https://sources.debian.net/src/xxhash/0.8.2-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/xxhash/0.8.2-2/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/x/xz-utils/xz-utils_5.6.2-2.dsc' xz-utils_5.6.2-2.dsc 2704 SHA256:3eadad7376915923c17d22cbe3905c3985b538ada1f46dc742a1675819130af5
'http://deb.debian.org/debian/pool/main/x/xz-utils/xz-utils_5.6.2.orig.tar.xz' xz-utils_5.6.2.orig.tar.xz 1307448 SHA256:a9db3bb3d64e248a0fae963f8fb6ba851a26ba1822e504dc0efd18a80c626caf
'http://deb.debian.org/debian/pool/main/x/xz-utils/xz-utils_5.6.2.orig.tar.xz.asc' xz-utils_5.6.2.orig.tar.xz.asc 833 SHA256:297c242cb55ae70242e8773ee8099c6561b9d8a49dab3b3cfccb33465c108e20
'http://deb.debian.org/debian/pool/main/x/xz-utils/xz-utils_5.6.2-2.debian.tar.xz' xz-utils_5.6.2-2.debian.tar.xz 24560 SHA256:b269af8285f4226b2e70e98e917a16b83cbe316e27d6121d11a0b89f0d39a7c9
```

Other potentially useful URLs:

- https://sources.debian.net/src/xz-utils/5.6.2-2/ (for browsing the source)
- https://sources.debian.net/src/xz-utils/5.6.2-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/xz-utils/5.6.2-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `zlib=1:1.3.dfsg+really1.3.1-1`

Binary Packages:

- `zlib1g:amd64=1:1.3.dfsg+really1.3.1-1`
- `zlib1g-dev:amd64=1:1.3.dfsg+really1.3.1-1`

Licenses: (parsed from: `/usr/share/doc/zlib1g/copyright`, `/usr/share/doc/zlib1g-dev/copyright`)

- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris zlib=1:1.3.dfsg+really1.3.1-1
'http://deb.debian.org/debian/pool/main/z/zlib/zlib_1.3.dfsg%2breally1.3.1-1.dsc' zlib_1.3.dfsg+really1.3.1-1.dsc 2637 SHA256:ede2791e29c1d3b422f9208bdd7edf040c20445ea1e7453a72037576e64fa197
'http://deb.debian.org/debian/pool/main/z/zlib/zlib_1.3.dfsg%2breally1.3.1.orig.tar.gz' zlib_1.3.dfsg+really1.3.1.orig.tar.gz 1325737 SHA256:60dd315c07f616887caa029408308a018ace66e3d142726a97db164b3b8f69fb
'http://deb.debian.org/debian/pool/main/z/zlib/zlib_1.3.dfsg%2breally1.3.1-1.debian.tar.xz' zlib_1.3.dfsg+really1.3.1-1.debian.tar.xz 16576 SHA256:9ed525955ce9fb0c1b39be8ff98f73450dbfc6305a9a27e6149c8972d38a0a9e
```

Other potentially useful URLs:

- https://sources.debian.net/src/zlib/1:1.3.dfsg+really1.3.1-1/ (for browsing the source)
- https://sources.debian.net/src/zlib/1:1.3.dfsg+really1.3.1-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/zlib/1:1.3.dfsg+really1.3.1-1/ (for access to the source package after it no longer exists in the archive)
