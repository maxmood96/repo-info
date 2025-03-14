# `buildpack-deps:plucky`

## Docker Metadata

- Image ID: `sha256:b377fcb0280136758e9f6b02cc6c4e2b35a7eac7d8ca6a8e375a02e437a7967f`
- Created: `2025-02-12T00:41:24Z`
- Virtual Size: ~ 926.93 Mb  
  (total size of all layers on-disk)
- Arch: `linux`/`amd64`
- Command: `["/bin/bash"]`
- Environment:
  - `PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin`
- Labels:
  - `org.opencontainers.image.ref.name=ubuntu`
  - `org.opencontainers.image.version=25.04`

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
'http://archive.ubuntu.com/ubuntu/pool/main/a/acl/acl_2.3.2-2.dsc' acl_2.3.2-2.dsc 2604 SHA512:8376928f8a96880edce6e6f1073623ed03bf3da4489807d531c0ecd4c5ff09d19754007e3533922389134aa55a4b64d6f71caa7186133d5a5f559eecf7e33427
'http://archive.ubuntu.com/ubuntu/pool/main/a/acl/acl_2.3.2.orig.tar.xz' acl_2.3.2.orig.tar.xz 371680 SHA512:c2d061dbfd28c00cecbc1ae614d67f3138202bf4d39b383f2df4c6a8b10b830f33acec620fb211f268478737dde4037d338a5823af445253cb088c48a135099b
'http://archive.ubuntu.com/ubuntu/pool/main/a/acl/acl_2.3.2.orig.tar.xz.asc' acl_2.3.2.orig.tar.xz.asc 833 SHA512:a425b385e3ce30e7146cf8b143ca269e3edd78af82a21dea76d10ea68215f9abcfb1ed8be24ce3b6dce24e6640df8d5d5f365a47399e37006a66c6a62a41fe41
'http://archive.ubuntu.com/ubuntu/pool/main/a/acl/acl_2.3.2-2.debian.tar.xz' acl_2.3.2-2.debian.tar.xz 24296 SHA512:58f4f202baa58a6912f85682b967dca282981c1b8d57ffcda1cd67784b5e3f1865ccd1c452d06a50978649d3cb5198d2d5d23004e103b5bd89352a7c1904444f
```

### `dpkg` source package: `adduser=3.137ubuntu2`

Binary Packages:

- `adduser=3.137ubuntu2`

Licenses: (parsed from: `/usr/share/doc/adduser/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris adduser=3.137ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/a/adduser/adduser_3.137ubuntu2.dsc' adduser_3.137ubuntu2.dsc 1688 SHA512:d0d9ec7cd37888ef35f697feb135951f5d929b889207911bda34519a9484f763324ed9f998ecbd97198b41613a5c7e4735f553ad23007af21aa6cccfd3586f6a
'http://archive.ubuntu.com/ubuntu/pool/main/a/adduser/adduser_3.137ubuntu2.tar.xz' adduser_3.137ubuntu2.tar.xz 280520 SHA512:56ef280c99f93fffdd0e877a8592e51351f200df4dcafb5c3d81a459682838896563751f825718fb5bdf3b733781b93aee6b7343526d59cc467522f31f2b9859
```

### `dpkg` source package: `aom=3.12.0-1`

Binary Packages:

- `libaom3:amd64=3.12.0-1`

Licenses: (parsed from: `/usr/share/doc/libaom3/copyright`)

- `BSD-2-Clause`
- `BSD-2-clause`
- `BSD-3-clause`
- `Expat`
- `ISC`
- `public-domain-md5`

Source:

```console
$ apt-get source -qq --print-uris aom=3.12.0-1
'http://archive.ubuntu.com/ubuntu/pool/main/a/aom/aom_3.12.0-1.dsc' aom_3.12.0-1.dsc 2287 SHA512:99db560496080409cc96797c7ea514440b01da597a0b96491d17911417556ae7bc4de2d9ad72e66d3248645eb914b7302cbc1a4f69e114eade5d653f22a8ff87
'http://archive.ubuntu.com/ubuntu/pool/main/a/aom/aom_3.12.0.orig.tar.gz' aom_3.12.0.orig.tar.gz 5503994 SHA512:d2fe29f90db7542a987ff812e8e015fc4b49b6637ecb8399e029324bed79b1e4849df663852e7339ebb34671a9123024a1b7abc150285a74c54703da2db45403
'http://archive.ubuntu.com/ubuntu/pool/main/a/aom/aom_3.12.0-1.debian.tar.xz' aom_3.12.0-1.debian.tar.xz 20404 SHA512:822514b763b2c1c659e1798d41f5476984d66431f3c56414b5076aa030426dc7bc8ce92e13e4ba905909a712abd6b3d22c3c25c03c04d5a07fb5207c29f2ea6e
```

### `dpkg` source package: `apr-util=1.6.3-3ubuntu2`

Binary Packages:

- `libaprutil1t64:amd64=1.6.3-3ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libaprutil1t64/copyright`)

- `Apache-2.0`

Source:

```console
$ apt-get source -qq --print-uris apr-util=1.6.3-3ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/a/apr-util/apr-util_1.6.3-3ubuntu2.dsc' apr-util_1.6.3-3ubuntu2.dsc 2684 SHA512:77084753ad19bf95ffefc897a560392ce9fad753cae1f3e53c8bfe39f97868cc76565c4256605f83c3271d8322797245bd02a03bd3ad4fc490ba43e96c005ea3
'http://archive.ubuntu.com/ubuntu/pool/main/a/apr-util/apr-util_1.6.3.orig.tar.bz2' apr-util_1.6.3.orig.tar.bz2 432692 SHA512:8050a481eeda7532ef3751dbd8a5aa6c48354d52904a856ef9709484f4b0cc2e022661c49ddf55ec58253db22708ee0607dfa7705d9270e8fee117ae4f06a0fe
'http://archive.ubuntu.com/ubuntu/pool/main/a/apr-util/apr-util_1.6.3-3ubuntu2.debian.tar.xz' apr-util_1.6.3-3ubuntu2.debian.tar.xz 342620 SHA512:e7a088f2fcf5d77bf5f7c3dbdd99e3cc120a6c1f81a3b04494159f37702b799bed18f592cc7e6916cbdfff5516a206afa9c7b20cd7b2ee499d4e8eb5facfd064
```

### `dpkg` source package: `apr=1.7.5-1`

Binary Packages:

- `libapr1t64:amd64=1.7.5-1`

Licenses: (parsed from: `/usr/share/doc/libapr1t64/copyright`)

- `Apache-2.0`

Source:

```console
$ apt-get source -qq --print-uris apr=1.7.5-1
'http://archive.ubuntu.com/ubuntu/pool/main/a/apr/apr_1.7.5-1.dsc' apr_1.7.5-1.dsc 2289 SHA512:2541530d64e4e18685867f63351f7dbf7574a3e7bbefe01b82dce9c82459a81bc02677bc0ef7db4d5edf074a5a2b255a0558e73458dd812d1ce9607a91ec76c5
'http://archive.ubuntu.com/ubuntu/pool/main/a/apr/apr_1.7.5.orig.tar.bz2' apr_1.7.5.orig.tar.bz2 898264 SHA512:d8a7553642da0c81261ac3992536efd9d43ecb9154934ef1a10ae808d6a3ce8198b40433091d3a6d04f61e67c59426fb5276193a37e810ae4bc74a8a10fb651b
'http://archive.ubuntu.com/ubuntu/pool/main/a/apr/apr_1.7.5.orig.tar.bz2.asc' apr_1.7.5.orig.tar.bz2.asc 833 SHA512:35bc67508d5cfe17593792417e5b78a614304f8b1014ffdea7644b23532579bf5a8e36c51abcbb723408cf2d47a9549c44516c1f204b6ed38154b1ea2b863357
'http://archive.ubuntu.com/ubuntu/pool/main/a/apr/apr_1.7.5-1.debian.tar.xz' apr_1.7.5-1.debian.tar.xz 64960 SHA512:2064f9c3a7eb77e054ec372d387c763f093e1a11e970771cc32c2b958de99e98e7bf469825c8780b6cdf90f619252a7765413560a5fe9b9c1da8c93b6e29999a
```

### `dpkg` source package: `apt=2.9.16`

Binary Packages:

- `apt=2.9.16`
- `libapt-pkg6.0t64:amd64=2.9.16`

Licenses: (parsed from: `/usr/share/doc/apt/copyright`, `/usr/share/doc/libapt-pkg6.0t64/copyright`)

- `BSD-3-clause`
- `Expat`
- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/apt/2.9.16/


### `dpkg` source package: `architecture-properties=0.2.5`

Binary Packages:

- `native-architecture=0.2.5`

Licenses: (parsed from: `/usr/share/doc/native-architecture/copyright`)

- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/architecture-properties/0.2.5/


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


### `dpkg` source package: `audit=1:4.0.2-2ubuntu1`

Binary Packages:

- `libaudit-common=1:4.0.2-2ubuntu1`
- `libaudit1:amd64=1:4.0.2-2ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libaudit-common/copyright`, `/usr/share/doc/libaudit1/copyright`)

- `GPL-1`
- `GPL-2`
- `LGPL-2.1`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `autoconf=2.72-3`

Binary Packages:

- `autoconf=2.72-3`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/autoconf/2.72-3/


### `dpkg` source package: `automake-1.17=1:1.17-3`

Binary Packages:

- `automake=1:1.17-3`

Licenses: (parsed from: `/usr/share/doc/automake/copyright`)

- `GFDL-1.3`
- `GFDL-NIV-1.3+`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `permissive`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/automake-1.17/1:1.17-3/


### `dpkg` source package: `autotools-dev=20220109.1`

Binary Packages:

- `autotools-dev=20220109.1`

Licenses: (parsed from: `/usr/share/doc/autotools-dev/copyright`)

- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris autotools-dev=20220109.1
'http://archive.ubuntu.com/ubuntu/pool/main/a/autotools-dev/autotools-dev_20220109.1.dsc' autotools-dev_20220109.1.dsc 1661 SHA512:aca60be8ed006832005e58bf176f8c7e8abe85986dbcc6d15d8b5c092c89322a132601784ef1f977d7e071c8b033debcef7c3cb5712765be00c2d298d9812d71
'http://archive.ubuntu.com/ubuntu/pool/main/a/autotools-dev/autotools-dev_20220109.1.tar.xz' autotools-dev_20220109.1.tar.xz 87340 SHA512:5427cc6897685355018db547ec39fd6bcc0ecbd73ba25869fb841f3503c1753af9a323d963a2b3150ef40ff07486f39377acdec878b2c054c1fa51de9afe01bb
```

### `dpkg` source package: `base-files=13.5ubuntu3`

Binary Packages:

- `base-files=13.5ubuntu3`

Licenses: (parsed from: `/usr/share/doc/base-files/copyright`)

- `GPL`
- `GPL-2+`
- `verbatim`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `base-passwd=3.6.5`

Binary Packages:

- `base-passwd=3.6.5`

Licenses: (parsed from: `/usr/share/doc/base-passwd/copyright`)

- `GPL-2`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/base-passwd/3.6.5/


### `dpkg` source package: `bash=5.2.37-1ubuntu1`

Binary Packages:

- `bash=5.2.37-1ubuntu1`

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
$ apt-get source -qq --print-uris bash=5.2.37-1ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/b/bash/bash_5.2.37-1ubuntu1.dsc' bash_5.2.37-1ubuntu1.dsc 2400 SHA512:98b84fcf0db93159f8dc53e9cf43baab971075ad518eaedf52ddbcb113dd90b8601401b6c7a63aed48810310c2d8a83f7ed67dbb7baaf857cb7ad34f3be79c4d
'http://archive.ubuntu.com/ubuntu/pool/main/b/bash/bash_5.2.37.orig.tar.xz' bash_5.2.37.orig.tar.xz 5600932 SHA512:c5380301114967378ace9ae4c510564cb7a827c221470aa532f2360a35000e7719ae081151f3d2ac86dff1d1465f64e60d9202fa6657d716ed6e449f77552158
'http://archive.ubuntu.com/ubuntu/pool/main/b/bash/bash_5.2.37-1ubuntu1.debian.tar.xz' bash_5.2.37-1ubuntu1.debian.tar.xz 95448 SHA512:4a0b91bdcdca3f30b625c4ee5ad71d351b46ae2f5388e66f4a7e23533673016715c10ecfa117f528ea68d8b6b87d417d839dffd3d2fbf577b8a20d074b188a45
```

### `dpkg` source package: `binutils=2.44-1ubuntu1`

Binary Packages:

- `binutils=2.44-1ubuntu1`
- `binutils-common:amd64=2.44-1ubuntu1`
- `binutils-x86-64-linux-gnu=2.44-1ubuntu1`
- `libbinutils:amd64=2.44-1ubuntu1`
- `libctf-nobfd0:amd64=2.44-1ubuntu1`
- `libctf0:amd64=2.44-1ubuntu1`
- `libgprofng0:amd64=2.44-1ubuntu1`
- `libsframe1:amd64=2.44-1ubuntu1`

Licenses: (parsed from: `/usr/share/doc/binutils/copyright`, `/usr/share/doc/binutils-common/copyright`, `/usr/share/doc/binutils-x86-64-linux-gnu/copyright`, `/usr/share/doc/libbinutils/copyright`, `/usr/share/doc/libctf-nobfd0/copyright`, `/usr/share/doc/libctf0/copyright`, `/usr/share/doc/libgprofng0/copyright`, `/usr/share/doc/libsframe1/copyright`)

- `GFDL`
- `GPL`
- `LGPL`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `brotli=1.1.0-2build3`

Binary Packages:

- `libbrotli-dev:amd64=1.1.0-2build3`
- `libbrotli1:amd64=1.1.0-2build3`

Licenses: (parsed from: `/usr/share/doc/libbrotli-dev/copyright`, `/usr/share/doc/libbrotli1/copyright`)

- `MIT`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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
'http://archive.ubuntu.com/ubuntu/pool/main/b/bzip2/bzip2_1.0.8-6.dsc' bzip2_1.0.8-6.dsc 1604 SHA512:ff346848f80a2d85266e27db27289e126ed016b0ee65f777594e92be388c9f76010419efcbe93dc1d5dde7fe356ee02e797e3579687252b0ae8f4152a245dcb2
'http://archive.ubuntu.com/ubuntu/pool/main/b/bzip2/bzip2_1.0.8.orig.tar.gz' bzip2_1.0.8.orig.tar.gz 810029 SHA512:083f5e675d73f3233c7930ebe20425a533feedeaaa9d8cc86831312a6581cefbe6ed0d08d2fa89be81082f2a5abdabca8b3c080bf97218a1bd59dc118a30b9f3
'http://archive.ubuntu.com/ubuntu/pool/main/b/bzip2/bzip2_1.0.8-6.debian.tar.bz2' bzip2_1.0.8-6.debian.tar.bz2 26991 SHA512:29a0df15aab88f4df3e4b3e13a04a428bae850b251d4b70541896b93fe28bce3397f9a7c5e3b251c81a8abd3e0a7911d31f546c1fe30a28c764ded587462831c
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
'http://archive.ubuntu.com/ubuntu/pool/main/c/ca-certificates/ca-certificates_20241223.dsc' ca-certificates_20241223.dsc 1766 SHA512:e5a51aade3643c30592dc3155af062b8147a7b9d5c809177e030824edd60082043b76773ff388e5108c3112f648ba371d24b3fdf8831ad1df13a923876449c05
'http://archive.ubuntu.com/ubuntu/pool/main/c/ca-certificates/ca-certificates_20241223.tar.xz' ca-certificates_20241223.tar.xz 278044 SHA512:d0d9a83276e546b71ca5ef65d06a3ff258397e30ea2395ba091910e40de37085e6a7a004bda87dd411e3f73ed70a8cc35bc7c534f62745df0f6df963557c9e7d
```

### `dpkg` source package: `cairo=1.18.2-2`

Binary Packages:

- `libcairo-gobject2:amd64=1.18.2-2`
- `libcairo-script-interpreter2:amd64=1.18.2-2`
- `libcairo2:amd64=1.18.2-2`
- `libcairo2-dev:amd64=1.18.2-2`

Licenses: (parsed from: `/usr/share/doc/libcairo-gobject2/copyright`, `/usr/share/doc/libcairo-script-interpreter2/copyright`, `/usr/share/doc/libcairo2/copyright`, `/usr/share/doc/libcairo2-dev/copyright`)

- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris cairo=1.18.2-2
'http://archive.ubuntu.com/ubuntu/pool/main/c/cairo/cairo_1.18.2-2.dsc' cairo_1.18.2-2.dsc 2763 SHA512:2ce8341b1caf77b3685e4816acc88b7ff2cf364b7be17db292a4f965e819e4ce7b99438bad1aaf2feb7ae4f898276c2ea77b9f20bf5a113903bb4f9fe5a76550
'http://archive.ubuntu.com/ubuntu/pool/main/c/cairo/cairo_1.18.2.orig.tar.xz' cairo_1.18.2.orig.tar.xz 32574256 SHA512:9b533ef65da120bdf6ec6e66b76c9a9a489b91951925357c2db9f399ce27fe03d10e500c4c03b72ad43d73bb5beb4d51e36c24443977a52ecfe1d24b07c99bef
'http://archive.ubuntu.com/ubuntu/pool/main/c/cairo/cairo_1.18.2-2.debian.tar.xz' cairo_1.18.2-2.debian.tar.xz 30396 SHA512:fadcbdd42490ff01217c7125b7635532cc658bc467df540b40b2a4e383ba150d0b2659f9ef9f30742a5cab2928bdcad09e4168e290d768cb9c1d745ad42e21ac
```

### `dpkg` source package: `cdebconf=0.274ubuntu1`

Binary Packages:

- `libdebconfclient0:amd64=0.274ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libdebconfclient0/copyright`)

- `BSD-2-Clause`
- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `coreutils=9.4-3.1ubuntu1`

Binary Packages:

- `coreutils=9.4-3.1ubuntu1`

Licenses: (parsed from: `/usr/share/doc/coreutils/copyright`)

- `BSD-4-clause-UC`
- `FSFULLR`
- `GFDL-1.3`
- `GFDL-NIV-1.3`
- `GPL-3`
- `GPL-3+`
- `ISC`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `curl=8.12.0+git20250209.89ed161+ds-1ubuntu1`

Binary Packages:

- `curl=8.12.0+git20250209.89ed161+ds-1ubuntu1`
- `libcurl3t64-gnutls:amd64=8.12.0+git20250209.89ed161+ds-1ubuntu1`
- `libcurl4-openssl-dev:amd64=8.12.0+git20250209.89ed161+ds-1ubuntu1`
- `libcurl4t64:amd64=8.12.0+git20250209.89ed161+ds-1ubuntu1`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `cyrus-sasl2=2.1.28+dfsg1-8build1`

Binary Packages:

- `libsasl2-2:amd64=2.1.28+dfsg1-8build1`
- `libsasl2-modules-db:amd64=2.1.28+dfsg1-8build1`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `dash=0.5.12-9ubuntu1`

Binary Packages:

- `dash=0.5.12-9ubuntu1`

Licenses: (parsed from: `/usr/share/doc/dash/copyright`)

- `BSD-3-Clause`
- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `db-defaults=1:5.3.21ubuntu2`

Binary Packages:

- `libdb-dev:amd64=1:5.3.21ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libdb-dev/copyright`)

- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris db-defaults=1:5.3.21ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/d/db-defaults/db-defaults_5.3.21ubuntu2.dsc' db-defaults_5.3.21ubuntu2.dsc 1663 SHA512:018dc4aedcf739f611a55d1ad1ee6ad62f0ed60d33ebfeb493ac9709e743f5cb2bd318ee246a3f52f0274424048c94c25f685889a82c16b24357c023f63917df
'http://archive.ubuntu.com/ubuntu/pool/main/d/db-defaults/db-defaults_5.3.21ubuntu2.tar.xz' db-defaults_5.3.21ubuntu2.tar.xz 2644 SHA512:7a41ab8046316afe6da9623ba36bf6803b6de49059f29acdb5d931009e3f317381713c3d2f68c4aeefa5bbed2e625196359b4735421d8e9caffd07f0f06184b4
```

### `dpkg` source package: `db5.3=5.3.28+dfsg2-9`

Binary Packages:

- `libdb5.3-dev=5.3.28+dfsg2-9`
- `libdb5.3t64:amd64=5.3.28+dfsg2-9`

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
$ apt-get source -qq --print-uris db5.3=5.3.28+dfsg2-9
'http://archive.ubuntu.com/ubuntu/pool/main/d/db5.3/db5.3_5.3.28%2bdfsg2-9.dsc' db5.3_5.3.28+dfsg2-9.dsc 2373 SHA512:f7b3ee10c42556df8b3fd016d9ebe4efc38d60aba8cbd7120d4573d8242c9260e7507cda3b7a2af3f5501ac3d7b27c5dcaccfc54235eb428f583d4d9adae21f5
'http://archive.ubuntu.com/ubuntu/pool/main/d/db5.3/db5.3_5.3.28%2bdfsg2.orig.tar.xz' db5.3_5.3.28+dfsg2.orig.tar.xz 21287688 SHA512:f9c9d042702ef3fcfdd4b4859583048f3396b161009dc24b6d3a2c53533d58214239fc80e2c42db17e9f092df44d531502737f3b368b956bff49ef057b6b51ef
'http://archive.ubuntu.com/ubuntu/pool/main/d/db5.3/db5.3_5.3.28%2bdfsg2-9.debian.tar.xz' db5.3_5.3.28+dfsg2-9.debian.tar.xz 36412 SHA512:9ed5d57168a50b8adae1c08cc7d1b307904a06a506d85e2faa2bbb4edfaf614b1ef5c3efe11ad71fc5d0f200459a1628c7d092fe121a53a619943c1424031796
```

### `dpkg` source package: `debconf=1.5.87ubuntu1`

Binary Packages:

- `debconf=1.5.87ubuntu1`

Licenses: (parsed from: `/usr/share/doc/debconf/copyright`)

- `BSD-2-clause`

Source:

```console
$ apt-get source -qq --print-uris debconf=1.5.87ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/d/debconf/debconf_1.5.87ubuntu1.dsc' debconf_1.5.87ubuntu1.dsc 2060 SHA512:422e0a4d7376387151ab57a90edac973559c84fd493dba73e9dc78928d1dadfbdc916268c5216dc1ecf49fd5894647696b8ed14525222f5618014e396bc219d3
'http://archive.ubuntu.com/ubuntu/pool/main/d/debconf/debconf_1.5.87ubuntu1.tar.xz' debconf_1.5.87ubuntu1.tar.xz 574428 SHA512:9e6b021155cd01c48552df9c3e61ee5b4dc7ed2355564819d595995715b1ba51301782b30f9710bb24769492844420973981c1e374841624897c703c642dfac9
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
'http://archive.ubuntu.com/ubuntu/pool/main/d/debianutils/debianutils_5.21.dsc' debianutils_5.21.dsc 1631 SHA512:14068decc92bb615468ca43d2c24eb0734ee7f45274629f079ffe7cae670a91254654911d58f3e4ce058ff6fbec985cfa8fb65408191ef2fa9bde5e6246ad36c
'http://archive.ubuntu.com/ubuntu/pool/main/d/debianutils/debianutils_5.21.tar.xz' debianutils_5.21.tar.xz 81916 SHA512:9d4c7505433e184d1b0467e3b0a0d649a5d20e5c75e70f0d8b0bffcf9694357a86cd36417b1d1b06285c6add4bf5c4361e49cba966c6993fb2dbe7c974366f98
```

### `dpkg` source package: `diffutils=1:3.10-1build1`

Binary Packages:

- `diffutils=1:3.10-1build1`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `djvulibre=3.5.28-2build4`

Binary Packages:

- `libdjvulibre-dev:amd64=3.5.28-2build4`
- `libdjvulibre-text=3.5.28-2build4`
- `libdjvulibre21:amd64=3.5.28-2build4`

Licenses: (parsed from: `/usr/share/doc/libdjvulibre-dev/copyright`, `/usr/share/doc/libdjvulibre-text/copyright`, `/usr/share/doc/libdjvulibre21/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris djvulibre=3.5.28-2build4
'http://archive.ubuntu.com/ubuntu/pool/main/d/djvulibre/djvulibre_3.5.28-2build4.dsc' djvulibre_3.5.28-2build4.dsc 2499 SHA512:55baf25f2ed6440d0a2bc111b493125a2762ab6ec60a26aae6ee33241ee00a0f3b73b998392e4593a7e8501765bb40b7b6c1d6c25edd14c1ad2eeda439867e63
'http://archive.ubuntu.com/ubuntu/pool/main/d/djvulibre/djvulibre_3.5.28.orig.tar.xz' djvulibre_3.5.28.orig.tar.xz 2959024 SHA512:4fdbecd2b7b583ee4211c9cda6638a3a831c883e2552b3c8ad09f69e8734831addc14f590faab8c58d7f9f017b527abccc384f6066e674e341cf43c96db49cb7
'http://archive.ubuntu.com/ubuntu/pool/main/d/djvulibre/djvulibre_3.5.28-2build4.debian.tar.xz' djvulibre_3.5.28-2build4.debian.tar.xz 17704 SHA512:ded773fa8599b2a3d0a1683d1bb59b276b82a76ed1d6ddc92ea04f5a5186d0c41058c8c99595a37b9a7f111755b52ef455b31cecb2bbca439bc5e2533fa4941b
```

### `dpkg` source package: `dpkg=1.22.11ubuntu4`

Binary Packages:

- `dpkg=1.22.11ubuntu4`
- `dpkg-dev=1.22.11ubuntu4`
- `libdpkg-perl=1.22.11ubuntu4`

Licenses: (parsed from: `/usr/share/doc/dpkg/copyright`, `/usr/share/doc/dpkg-dev/copyright`, `/usr/share/doc/libdpkg-perl/copyright`)

- `GPL-2`
- `GPL-2+`
- `public-domain-s-s-d`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `e2fsprogs=1.47.2-1ubuntu1`

Binary Packages:

- `comerr-dev:amd64=2.1-1.47.2-1ubuntu1`
- `e2fsprogs=1.47.2-1ubuntu1`
- `libcom-err2:amd64=1.47.2-1ubuntu1`
- `libext2fs2t64:amd64=1.47.2-1ubuntu1`
- `libss2:amd64=1.47.2-1ubuntu1`
- `logsave=1.47.2-1ubuntu1`

Licenses: (parsed from: `/usr/share/doc/comerr-dev/copyright`, `/usr/share/doc/e2fsprogs/copyright`, `/usr/share/doc/libcom-err2/copyright`, `/usr/share/doc/libext2fs2t64/copyright`, `/usr/share/doc/libss2/copyright`, `/usr/share/doc/logsave/copyright`)

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
$ apt-get source -qq --print-uris e2fsprogs=1.47.2-1ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/e/e2fsprogs/e2fsprogs_1.47.2-1ubuntu1.dsc' e2fsprogs_1.47.2-1ubuntu1.dsc 3289 SHA512:86e1d742f5459eae99979a4f6ee780c0ce2e26089e802b0fc0c03932a43bbf7b6b321b3d1f426b030352b6aa375d4b19aea82d1a913f92b3ee64e62480c66088
'http://archive.ubuntu.com/ubuntu/pool/main/e/e2fsprogs/e2fsprogs_1.47.2.orig.tar.gz' e2fsprogs_1.47.2.orig.tar.gz 9996725 SHA512:dd89139c5e2bf999a22d999686ef06ab42f6ad537c6aeaa3fe68d9734d734b7396fd7ab2fd8002be26860c5653991a666d0df06c804c2f1f07f1274468ec728f
'http://archive.ubuntu.com/ubuntu/pool/main/e/e2fsprogs/e2fsprogs_1.47.2.orig.tar.gz.asc' e2fsprogs_1.47.2.orig.tar.gz.asc 488 SHA512:a22d46cc37497861d5a7e50076b40b8be6f459790f6eaacf0446200776fb74492ca9bfc7abc19edda3c9f7f722c318827b02f9cfbbb2118a8e86bce4d446d56b
'http://archive.ubuntu.com/ubuntu/pool/main/e/e2fsprogs/e2fsprogs_1.47.2-1ubuntu1.debian.tar.xz' e2fsprogs_1.47.2-1ubuntu1.debian.tar.xz 94228 SHA512:3d50e03fabc43643c1e7ad1eafecf3ea2da8967b339ab46a20817e90aead1fd5dd61ae4f06d7d8cd7a634105a3f9b7bc230cff8b843d210a43957f16a1295e16
```

### `dpkg` source package: `elfutils=0.192-4`

Binary Packages:

- `libelf1t64:amd64=0.192-4`

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
$ apt-get source -qq --print-uris elfutils=0.192-4
'http://archive.ubuntu.com/ubuntu/pool/main/e/elfutils/elfutils_0.192-4.dsc' elfutils_0.192-4.dsc 3314 SHA512:8ccb71f2ccf9365d5cf3cd77cf5c5ca114fd347d56618f44400ae1e4e652453b81d601702be23d12bc6e1430001ef5c265e23ab9a4e9bb274291473f9c8e7831
'http://archive.ubuntu.com/ubuntu/pool/main/e/elfutils/elfutils_0.192.orig.tar.bz2' elfutils_0.192.orig.tar.bz2 11913897 SHA512:543188f5f2cfe5bc7955a878416c5f252edff9926754e5de0c6c57b132f21d9285c9b29e41281e93baad11d4ae7efbbf93580c114579c182103565fe99bd3909
'http://archive.ubuntu.com/ubuntu/pool/main/e/elfutils/elfutils_0.192-4.debian.tar.xz' elfutils_0.192-4.debian.tar.xz 44456 SHA512:a28abf785cf083b68c8e2adc8804bdabe7e5812a56326875b897b664f8a5311faeea51ee033f7dd5260289d32ab4f1e6db1667ca3eb1ba6f124ec4a5dcb05556
```

### `dpkg` source package: `expat=2.6.4-1`

Binary Packages:

- `libexpat1:amd64=2.6.4-1`
- `libexpat1-dev:amd64=2.6.4-1`

Licenses: (parsed from: `/usr/share/doc/libexpat1/copyright`, `/usr/share/doc/libexpat1-dev/copyright`)

- `MIT`

Source:

```console
$ apt-get source -qq --print-uris expat=2.6.4-1
'http://archive.ubuntu.com/ubuntu/pool/main/e/expat/expat_2.6.4-1.dsc' expat_2.6.4-1.dsc 1964 SHA512:f75677ea8a4a929aa59834ebc527a8c4f17408300f8c5ce171527c1583c24c3c370d6153e275f1b3503964003ba882203d3e761b9d1c4361d3821f4f1467235e
'http://archive.ubuntu.com/ubuntu/pool/main/e/expat/expat_2.6.4.orig.tar.gz' expat_2.6.4.orig.tar.gz 8419100 SHA512:6a6c5b0f6a1b2c70715701aeab688e476943704c492a0f2f8afd7fea84615a8d9569eb2b699912676058eff6a7bbdd78b48110ed67ab0250a3d41fe8f128f4e1
'http://archive.ubuntu.com/ubuntu/pool/main/e/expat/expat_2.6.4-1.debian.tar.xz' expat_2.6.4-1.debian.tar.xz 13124 SHA512:ce3aa1e7c4f90b31b6bab82ba1405d577936a95d43dcbfc9a1b5203277b2f61130bde5433d17c11da13e263752748dc6d24d6b430b7c8907001869cb7decebf6
```

### `dpkg` source package: `fftw3=3.3.10-2fakesync1build1`

Binary Packages:

- `libfftw3-bin=3.3.10-2fakesync1build1`
- `libfftw3-dev:amd64=3.3.10-2fakesync1build1`
- `libfftw3-double3:amd64=3.3.10-2fakesync1build1`
- `libfftw3-long3:amd64=3.3.10-2fakesync1build1`
- `libfftw3-quad3:amd64=3.3.10-2fakesync1build1`
- `libfftw3-single3:amd64=3.3.10-2fakesync1build1`

Licenses: (parsed from: `/usr/share/doc/libfftw3-bin/copyright`, `/usr/share/doc/libfftw3-dev/copyright`, `/usr/share/doc/libfftw3-double3/copyright`, `/usr/share/doc/libfftw3-long3/copyright`, `/usr/share/doc/libfftw3-quad3/copyright`, `/usr/share/doc/libfftw3-single3/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris fftw3=3.3.10-2fakesync1build1
'http://archive.ubuntu.com/ubuntu/pool/main/f/fftw3/fftw3_3.3.10-2fakesync1build1.dsc' fftw3_3.3.10-2fakesync1build1.dsc 2893 SHA512:39bde1bb12220e6b28d74408a69ac2fcbda08b62ac7a9d2ce5dc3734c6305ba64826bedabba6430826998050628e9d6ba15355d848ba072dada496fbea3cdef6
'http://archive.ubuntu.com/ubuntu/pool/main/f/fftw3/fftw3_3.3.10.orig.tar.gz' fftw3_3.3.10.orig.tar.gz 4262403 SHA512:fa2ea740449fd06c833a82e1fff82bacd554188d500cbedff5a0bc185551799ef9ef9b8b1c227283abdbbdd185424d19df9c0f06ed88d5fe3d9c001d6fab6109
'http://archive.ubuntu.com/ubuntu/pool/main/f/fftw3/fftw3_3.3.10-2fakesync1build1.debian.tar.xz' fftw3_3.3.10-2fakesync1build1.debian.tar.xz 14784 SHA512:4ccad34453fac43a72cb600bc2a6d9a28bf1d7feaff877c234c271f4b768588698d2be5a0d450a2090f046830a0442662fe3753eab63f0b4b313ae4f4fedc60c
```

### `dpkg` source package: `file=1:5.45-3build1`

Binary Packages:

- `file=1:5.45-3build1`
- `libmagic-mgc=1:5.45-3build1`
- `libmagic1t64:amd64=1:5.45-3build1`

Licenses: (parsed from: `/usr/share/doc/file/copyright`, `/usr/share/doc/libmagic-mgc/copyright`, `/usr/share/doc/libmagic1t64/copyright`)

- `BSD-2-Clause-alike`
- `BSD-2-Clause-netbsd`
- `BSD-2-Clause-regents`
- `MIT-Old-Style-with-legal-disclaimer-2`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris file=1:5.45-3build1
'http://archive.ubuntu.com/ubuntu/pool/main/f/file/file_5.45-3build1.dsc' file_5.45-3build1.dsc 2408 SHA512:366c97f8faa11661879e0907bda25730f24dd6369455d60723790152a6d3e67b858ce99de82b095cae396d0621efff6dcd25ae11ce8e5e4af75006623ad85f19
'http://archive.ubuntu.com/ubuntu/pool/main/f/file/file_5.45.orig.tar.gz' file_5.45.orig.tar.gz 1246503 SHA512:12611a59ff766c22a55db4b4a9f80f95a0a2e916a1d8593612c6ead32c247102a8fdc23693c6bf81bda9b604d951a62c0051e91580b1b79e190a3504c0efc20a
'http://archive.ubuntu.com/ubuntu/pool/main/f/file/file_5.45.orig.tar.gz.asc' file_5.45.orig.tar.gz.asc 169 SHA512:4bda3c9b23e534e31d8726eae110e108c538c88ca4884666989da9bedc5dcfd9cfcb3754e68885ca5310db67bff151f9bf4f21913f7b5046f158a9ca38bc00a4
'http://archive.ubuntu.com/ubuntu/pool/main/f/file/file_5.45-3build1.debian.tar.xz' file_5.45-3build1.debian.tar.xz 35964 SHA512:292021c05c73e2ea593af147e6df690a73df6ebf5b10408760be48c161ed341d974145aed93161d09fcea6a7ce0348edfea8a4c0ece9fdf54e1c33e5d3673b86
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
'http://archive.ubuntu.com/ubuntu/pool/main/f/findutils/findutils_4.10.0-3.dsc' findutils_4.10.0-3.dsc 2291 SHA512:7a651b7be4777d486eee6fc81ba656734e7952a1adae79c3c5d6a5f02441fa04841026dbbd3d9f2d627f4c627d7e0c54c6756e2ffaf3ba47222be3671c81d73b
'http://archive.ubuntu.com/ubuntu/pool/main/f/findutils/findutils_4.10.0.orig.tar.xz' findutils_4.10.0.orig.tar.xz 2240712 SHA512:b8b683d21cd26c6da4f41c56e83cadbda4780f8610a2bbd4b4e34bb1f339c3209721974b03e076d5eef0331fd876d947b398197aad37c29bbcc2e0405c641b34
'http://archive.ubuntu.com/ubuntu/pool/main/f/findutils/findutils_4.10.0.orig.tar.xz.asc' findutils_4.10.0.orig.tar.xz.asc 488 SHA512:a835153a0671309021be187bf78afee58d9682acb40545aaa9dd187f0ebdea0cfa5583bd03f363243633ea056ddb0a7a6603987ab5e34a608426cb4265ac6d8f
'http://archive.ubuntu.com/ubuntu/pool/main/f/findutils/findutils_4.10.0-3.debian.tar.xz' findutils_4.10.0-3.debian.tar.xz 33364 SHA512:578c4fa152b39e0e0b9d5ab1ea146889ae53cb623d01f84a93d0ba936c9355b2bc5eb20bd761e5638226a040d131edaba60cc573bb3ef4f04889cd5067d167f5
```

### `dpkg` source package: `fontconfig=2.15.0-1.1ubuntu2`

Binary Packages:

- `fontconfig=2.15.0-1.1ubuntu2`
- `fontconfig-config=2.15.0-1.1ubuntu2`
- `libfontconfig-dev:amd64=2.15.0-1.1ubuntu2`
- `libfontconfig1:amd64=2.15.0-1.1ubuntu2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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
'http://archive.ubuntu.com/ubuntu/pool/main/f/fonts-dejavu/fonts-dejavu_2.37-8.dsc' fonts-dejavu_2.37-8.dsc 2156 SHA512:c5632f8cf1fa690efc292e7ae8239265ac3a04e13423601d9a151b200ea36ae5242a0867428e3c7148c0cd5fa6b4ff3c368b53451f3234e20634f2fc6fe5c1fa
'http://archive.ubuntu.com/ubuntu/pool/main/f/fonts-dejavu/fonts-dejavu_2.37.orig.tar.bz2' fonts-dejavu_2.37.orig.tar.bz2 12050109 SHA512:e61fc8c675ef76edb49dd9a8caee62087280929bb8144b52aca2f8def30025c56246589ad8a6a806b9574e6876eedd16d57c70a6ce9c86817a2dfe39d8a2bb2b
'http://archive.ubuntu.com/ubuntu/pool/main/f/fonts-dejavu/fonts-dejavu_2.37-8.debian.tar.xz' fonts-dejavu_2.37-8.debian.tar.xz 13176 SHA512:7a19189a106a1243c64d43b050f87cba6f6c32d070f246aceb5ccc687401366825a31a653e45fa700e1593f7ed32340581988cfc1a489b5f8b705e80c2a891ee
```

### `dpkg` source package: `freetype=2.13.3+dfsg-1`

Binary Packages:

- `libfreetype-dev:amd64=2.13.3+dfsg-1`
- `libfreetype6:amd64=2.13.3+dfsg-1`

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
$ apt-get source -qq --print-uris freetype=2.13.3+dfsg-1
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.13.3%2bdfsg-1.dsc' freetype_2.13.3+dfsg-1.dsc 3680 SHA512:da953f9b177530c782fc32e09d5b53155c36f20664f35bf408a9ebe3d1f006d7df9d452ab358a7f707f1ff65223062b57cf1c8c55115dac9a493c593e76e63fd
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.13.3%2bdfsg.orig-ft2demos.tar.xz' freetype_2.13.3+dfsg.orig-ft2demos.tar.xz 342404 SHA512:e662a20ad2ff80534e8ea0df2f299e8f61350f13d279f80f8257b18352e863dd2c266791b85d3410b0c83966cb12e3ff49cf398b83a651dc73772df9fcf5936c
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.13.3%2bdfsg.orig-ft2demos.tar.xz.asc' freetype_2.13.3+dfsg.orig-ft2demos.tar.xz.asc 833 SHA512:c676452fb04b49824ce0a7287b46dc0234cee301bf80d31da01f5a1e7009ddbc0479866bfca62086fe23105436b0c02b9fb729b8fa24e7ca703c0fc357fe3675
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.13.3%2bdfsg.orig-ft2docs.tar.xz' freetype_2.13.3+dfsg.orig-ft2docs.tar.xz 2173852 SHA512:54ef9e3a4f0c298893268ed409f59aa1620a60c656ee3f8bdddbb91ffb2e70eea2f016a85c0a02eef699de362abee4aabae4482f0fa1cbf42967b5873fc84f2d
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.13.3%2bdfsg.orig-ft2docs.tar.xz.asc' freetype_2.13.3+dfsg.orig-ft2docs.tar.xz.asc 833 SHA512:bd1699aa0bf9f93a02b87a9c59ee6b69e4b24626fbcfbf9e0a0739f2634923bd397ee51379f57aae88465823ceb6bfe5cf6708a2bfa32d76f4a64ad6a9c08e3b
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.13.3%2bdfsg.orig.tar.xz' freetype_2.13.3+dfsg.orig.tar.xz 2201416 SHA512:634c2644bb70b93a605fae4d3e731cb13d149af4d01029ecf2d166b2e07cba07489303440a836057adc54f9bdabcceb7fde102dc5e5bf69f35c99ebae66f7293
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.13.3%2bdfsg-1.debian.tar.xz' freetype_2.13.3+dfsg-1.debian.tar.xz 43904 SHA512:b701ab41be470caf67fdf2efcd37f7504145d45872ce52d409a8e2a73b49031bc7159d0b1be02b4cc2b2abd82ca93e43d86b26bc3d3e7a08749f52ae5e3c9367
```

### `dpkg` source package: `fribidi=1.0.16-1`

Binary Packages:

- `libfribidi-dev:amd64=1.0.16-1`
- `libfribidi0:amd64=1.0.16-1`

Licenses: (parsed from: `/usr/share/doc/libfribidi-dev/copyright`, `/usr/share/doc/libfribidi0/copyright`)

- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris fribidi=1.0.16-1
'http://archive.ubuntu.com/ubuntu/pool/main/f/fribidi/fribidi_1.0.16-1.dsc' fribidi_1.0.16-1.dsc 2004 SHA512:ab6e3d4a38b769161d5c0dcf1f463e1f51617ef4c12aca1dddba05326d5e80380e344457eccf8761fc991d68ffe8081a6b23b8897403fa2b9d17b98e67fb9fe3
'http://archive.ubuntu.com/ubuntu/pool/main/f/fribidi/fribidi_1.0.16.orig.tar.xz' fribidi_1.0.16.orig.tar.xz 1098260 SHA512:e3a56f36155f6813e3609473639fc533de742309f561c463012dc90b412a1ac7694b765d92669b2cbfaee973ca0e92fa5e926e68a1a078921f26ef17d82ab651
'http://archive.ubuntu.com/ubuntu/pool/main/f/fribidi/fribidi_1.0.16-1.debian.tar.xz' fribidi_1.0.16-1.debian.tar.xz 8928 SHA512:1be896070e8d91e57bca6b694538050d43719c3fced6c12b7ed9e3948eff79c521fd03a4a1e5bfc1b3c4067fee980360094dbb0d8fb4e9375008fe9b56af45a7
```

### `dpkg` source package: `gcc-14=14.2.0-16ubuntu1`

Binary Packages:

- `cpp-14=14.2.0-16ubuntu1`
- `cpp-14-x86-64-linux-gnu=14.2.0-16ubuntu1`
- `g++-14=14.2.0-16ubuntu1`
- `g++-14-x86-64-linux-gnu=14.2.0-16ubuntu1`
- `gcc-14=14.2.0-16ubuntu1`
- `gcc-14-base:amd64=14.2.0-16ubuntu1`
- `gcc-14-x86-64-linux-gnu=14.2.0-16ubuntu1`
- `libasan8:amd64=14.2.0-16ubuntu1`
- `libatomic1:amd64=14.2.0-16ubuntu1`
- `libcc1-0:amd64=14.2.0-16ubuntu1`
- `libgcc-14-dev:amd64=14.2.0-16ubuntu1`
- `libgcc-s1:amd64=14.2.0-16ubuntu1`
- `libgomp1:amd64=14.2.0-16ubuntu1`
- `libhwasan0:amd64=14.2.0-16ubuntu1`
- `libitm1:amd64=14.2.0-16ubuntu1`
- `liblsan0:amd64=14.2.0-16ubuntu1`
- `libquadmath0:amd64=14.2.0-16ubuntu1`
- `libstdc++-14-dev:amd64=14.2.0-16ubuntu1`
- `libstdc++6:amd64=14.2.0-16ubuntu1`
- `libtsan2:amd64=14.2.0-16ubuntu1`
- `libubsan1:amd64=14.2.0-16ubuntu1`

Licenses: (parsed from: `/usr/share/doc/cpp-14/copyright`, `/usr/share/doc/cpp-14-x86-64-linux-gnu/copyright`, `/usr/share/doc/g++-14/copyright`, `/usr/share/doc/g++-14-x86-64-linux-gnu/copyright`, `/usr/share/doc/gcc-14/copyright`, `/usr/share/doc/gcc-14-base/copyright`, `/usr/share/doc/gcc-14-x86-64-linux-gnu/copyright`, `/usr/share/doc/libasan8/copyright`, `/usr/share/doc/libatomic1/copyright`, `/usr/share/doc/libcc1-0/copyright`, `/usr/share/doc/libgcc-14-dev/copyright`, `/usr/share/doc/libgcc-s1/copyright`, `/usr/share/doc/libgomp1/copyright`, `/usr/share/doc/libhwasan0/copyright`, `/usr/share/doc/libitm1/copyright`, `/usr/share/doc/liblsan0/copyright`, `/usr/share/doc/libquadmath0/copyright`, `/usr/share/doc/libstdc++-14-dev/copyright`, `/usr/share/doc/libstdc++6/copyright`, `/usr/share/doc/libtsan2/copyright`, `/usr/share/doc/libubsan1/copyright`)

- `Artistic`
- `GFDL-1.2`
- `GPL`
- `GPL-3`
- `LGPL`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `gcc-defaults=1.220ubuntu1`

Binary Packages:

- `cpp=4:14.2.0-1ubuntu1`
- `cpp-x86-64-linux-gnu=4:14.2.0-1ubuntu1`
- `g++=4:14.2.0-1ubuntu1`
- `g++-x86-64-linux-gnu=4:14.2.0-1ubuntu1`
- `gcc=4:14.2.0-1ubuntu1`
- `gcc-x86-64-linux-gnu=4:14.2.0-1ubuntu1`

Licenses: (parsed from: `/usr/share/doc/cpp/copyright`, `/usr/share/doc/cpp-x86-64-linux-gnu/copyright`, `/usr/share/doc/g++/copyright`, `/usr/share/doc/g++-x86-64-linux-gnu/copyright`, `/usr/share/doc/gcc/copyright`, `/usr/share/doc/gcc-x86-64-linux-gnu/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris gcc-defaults=1.220ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-defaults/gcc-defaults_1.220ubuntu1.dsc' gcc-defaults_1.220ubuntu1.dsc 37367 SHA512:c65f8611c4f8f10cb48d2ca3e6c70dee9e006119b9ea669af4d47508fa2a622c4c4cbad9b566324268d9d6fdd42023c5fe61f7212f3a145e78815942a4bee8df
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-defaults/gcc-defaults_1.220ubuntu1.tar.xz' gcc-defaults_1.220ubuntu1.tar.xz 56864 SHA512:8770e76a561e5ea9c0735fab78e228f5e06a3ef00af9fa365b68494f045f063a5dda6b2f8ec137692605c80d93b3e4e9b44c322243ba60478b7f71a6cb669f5f
```

### `dpkg` source package: `gdbm=1.24-2`

Binary Packages:

- `libgdbm-compat4t64:amd64=1.24-2`
- `libgdbm-dev:amd64=1.24-2`
- `libgdbm6t64:amd64=1.24-2`

Licenses: (parsed from: `/usr/share/doc/libgdbm-compat4t64/copyright`, `/usr/share/doc/libgdbm-dev/copyright`, `/usr/share/doc/libgdbm6t64/copyright`)

- `GFDL-NIV-1.3+`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris gdbm=1.24-2
'http://archive.ubuntu.com/ubuntu/pool/main/g/gdbm/gdbm_1.24-2.dsc' gdbm_1.24-2.dsc 2466 SHA512:b25a2656224dc0e7703375a50cb58cb3cb8b63f89a3a2c2e749b96fb40ae989f06a169bb0655dddecbe3e39fe856e8f22022c0b253d9dca303475f4361541dc2
'http://archive.ubuntu.com/ubuntu/pool/main/g/gdbm/gdbm_1.24.orig.tar.gz' gdbm_1.24.orig.tar.gz 1195931 SHA512:401ff8c707079f21da1ac1d6f4714a87f224b6f41943078487dc891be49f51fd1ac7a32fd599aae0fad185f2c6ba7432616d328fd6aaab068eb54db9562ff7fa
'http://archive.ubuntu.com/ubuntu/pool/main/g/gdbm/gdbm_1.24.orig.tar.gz.asc' gdbm_1.24.orig.tar.gz.asc 195 SHA512:c39d91aa6dee98851eac16b27a192300dab9545cff5e441d66a55a0939f1c6bc9e5ead0e96a48ef941f69d586b34d78e786d262d65e3b13ffe2c4f372d823fd6
'http://archive.ubuntu.com/ubuntu/pool/main/g/gdbm/gdbm_1.24-2.debian.tar.xz' gdbm_1.24-2.debian.tar.xz 16880 SHA512:bb98e8032f57a1dc33d34004e6b748a859aa465bd9fd6a592abe6d3ca09eedfebf05fbf0245d5c4eb01560ee0998f16016cd85ebc3367c25713795a9bab97a0f
```

### `dpkg` source package: `gdk-pixbuf=2.42.12+dfsg-2`

Binary Packages:

- `gir1.2-gdkpixbuf-2.0:amd64=2.42.12+dfsg-2`
- `libgdk-pixbuf-2.0-0:amd64=2.42.12+dfsg-2`
- `libgdk-pixbuf-2.0-dev:amd64=2.42.12+dfsg-2`
- `libgdk-pixbuf2.0-bin=2.42.12+dfsg-2`
- `libgdk-pixbuf2.0-common=2.42.12+dfsg-2`

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
$ apt-get source -qq --print-uris gdk-pixbuf=2.42.12+dfsg-2
'http://archive.ubuntu.com/ubuntu/pool/main/g/gdk-pixbuf/gdk-pixbuf_2.42.12%2bdfsg-2.dsc' gdk-pixbuf_2.42.12+dfsg-2.dsc 3091 SHA512:96739f914d30b473bf9e12043482ffe2d20a86f10226a27a7beecd11f0a8f1c5f87772469f4909aeb80574b94e61d0cf32c9cc9f2ceb2c985da48a21d28f3ed6
'http://archive.ubuntu.com/ubuntu/pool/main/g/gdk-pixbuf/gdk-pixbuf_2.42.12%2bdfsg.orig.tar.xz' gdk-pixbuf_2.42.12+dfsg.orig.tar.xz 6443656 SHA512:b27ce26fa876416dcb81d1e20679074fcb292f2574c7404cf0748e551888c59d62376499a0511411880fa30fe233757d578fd1d4025bde98e33ab6584c4850d5
'http://archive.ubuntu.com/ubuntu/pool/main/g/gdk-pixbuf/gdk-pixbuf_2.42.12%2bdfsg-2.debian.tar.xz' gdk-pixbuf_2.42.12+dfsg-2.debian.tar.xz 21832 SHA512:fb720f4eb83e41198137ab27f8695b2cc2cbe78105d70f5253ced117fe4378747aa71991576fd598840563d2d1486414c075aea19ac3ed18a9956ffdfd50021c
```

### `dpkg` source package: `git=1:2.47.1-1ubuntu1`

Binary Packages:

- `git=1:2.47.1-1ubuntu1`
- `git-man=1:2.47.1-1ubuntu1`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `glib2.0=2.83.3-2`

Binary Packages:

- `gir1.2-glib-2.0:amd64=2.83.3-2`
- `gir1.2-glib-2.0-dev:amd64=2.83.3-2`
- `girepository-tools:amd64=2.83.3-2`
- `libgio-2.0-dev:amd64=2.83.3-2`
- `libgio-2.0-dev-bin=2.83.3-2`
- `libgirepository-2.0-0:amd64=2.83.3-2`
- `libglib2.0-0t64:amd64=2.83.3-2`
- `libglib2.0-bin=2.83.3-2`
- `libglib2.0-data=2.83.3-2`
- `libglib2.0-dev:amd64=2.83.3-2`
- `libglib2.0-dev-bin=2.83.3-2`

Licenses: (parsed from: `/usr/share/doc/gir1.2-glib-2.0/copyright`, `/usr/share/doc/gir1.2-glib-2.0-dev/copyright`, `/usr/share/doc/girepository-tools/copyright`, `/usr/share/doc/libgio-2.0-dev/copyright`, `/usr/share/doc/libgio-2.0-dev-bin/copyright`, `/usr/share/doc/libgirepository-2.0-0/copyright`, `/usr/share/doc/libglib2.0-0t64/copyright`, `/usr/share/doc/libglib2.0-bin/copyright`, `/usr/share/doc/libglib2.0-data/copyright`, `/usr/share/doc/libglib2.0-dev/copyright`, `/usr/share/doc/libglib2.0-dev-bin/copyright`)

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/glib2.0/2.83.3-2/


### `dpkg` source package: `glibc=2.40-4ubuntu1`

Binary Packages:

- `libc-bin=2.40-4ubuntu1`
- `libc-dev-bin=2.40-4ubuntu1`
- `libc6:amd64=2.40-4ubuntu1`
- `libc6-dev:amd64=2.40-4ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libc-bin/copyright`, `/usr/share/doc/libc-dev-bin/copyright`, `/usr/share/doc/libc6/copyright`, `/usr/share/doc/libc6-dev/copyright`)

- `GFDL-1.3`
- `GPL-2`
- `LGPL-2.1`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `gmp=2:6.3.0+dfsg-2ubuntu7`

Binary Packages:

- `libgmp-dev:amd64=2:6.3.0+dfsg-2ubuntu7`
- `libgmp10:amd64=2:6.3.0+dfsg-2ubuntu7`
- `libgmpxx4ldbl:amd64=2:6.3.0+dfsg-2ubuntu7`

Licenses: (parsed from: `/usr/share/doc/libgmp-dev/copyright`, `/usr/share/doc/libgmp10/copyright`, `/usr/share/doc/libgmpxx4ldbl/copyright`)

- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `GPL-3+ with Bison exception`
- `LGPL-3`
- `LGPL-3+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `gnupg2=2.4.4-2ubuntu22`

Binary Packages:

- `dirmngr=2.4.4-2ubuntu22`
- `gnupg=2.4.4-2ubuntu22`
- `gnupg-utils=2.4.4-2ubuntu22`
- `gpg=2.4.4-2ubuntu22`
- `gpg-agent=2.4.4-2ubuntu22`
- `gpgconf=2.4.4-2ubuntu22`
- `gpgsm=2.4.4-2ubuntu22`
- `gpgv=2.4.4-2ubuntu22`
- `keyboxd=2.4.4-2ubuntu22`

Licenses: (parsed from: `/usr/share/doc/dirmngr/copyright`, `/usr/share/doc/gnupg/copyright`, `/usr/share/doc/gnupg-utils/copyright`, `/usr/share/doc/gpg/copyright`, `/usr/share/doc/gpg-agent/copyright`, `/usr/share/doc/gpgconf/copyright`, `/usr/share/doc/gpgsm/copyright`, `/usr/share/doc/gpgv/copyright`, `/usr/share/doc/keyboxd/copyright`)

- `BSD-3-clause`
- `CC0-1.0`
- `Expat`
- `GPL-2+`
- `GPL-2.0`
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
$ apt-get source -qq --print-uris gnupg2=2.4.4-2ubuntu22
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnupg2/gnupg2_2.4.4-2ubuntu22.dsc' gnupg2_2.4.4-2ubuntu22.dsc 3625 SHA512:2d8552f6d5282997b2958180de311f40782b8f4c8c0a150049332b03fd5a2a703aafe00c3624584c95cc065e9102519e9a713fff6dd10d3085eb185e60dcf28a
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnupg2/gnupg2_2.4.4.orig.tar.bz2' gnupg2_2.4.4.orig.tar.bz2 7886036 SHA512:3d1a3b08d1ce2319d238d8be96591e418ede1dc0b4ede33a4cc2fe40e9c56d5bbc27b1984736d8a786e7f292ddbc836846a8bdb4bf89f064e953c37cb54b94ef
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnupg2/gnupg2_2.4.4.orig.tar.bz2.asc' gnupg2_2.4.4.orig.tar.bz2.asc 386 SHA512:abb44c8bfa59e589bdcd660f1d1a2e268bade8729d95b34263e3d3b5388d1d2276420313989777938f17f97739c554808f97a63257ca0f53d2122a346d70ec85
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnupg2/gnupg2_2.4.4-2ubuntu22.debian.tar.xz' gnupg2_2.4.4-2ubuntu22.debian.tar.xz 88720 SHA512:a285e79a068e1677e9541abad31a0ea9ec3c7259bdec119af8244feb8694063aa6d5f66a8f0729d4e885908e67bea9bbe30d4cb44f6ac0febbf0a642100689f2
```

### `dpkg` source package: `gnutls28=3.8.9-2ubuntu1`

Binary Packages:

- `libgnutls-dane0t64:amd64=3.8.9-2ubuntu1`
- `libgnutls-openssl27t64:amd64=3.8.9-2ubuntu1`
- `libgnutls28-dev:amd64=3.8.9-2ubuntu1`
- `libgnutls30t64:amd64=3.8.9-2ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libgnutls-dane0t64/copyright`, `/usr/share/doc/libgnutls-openssl27t64/copyright`, `/usr/share/doc/libgnutls28-dev/copyright`, `/usr/share/doc/libgnutls30t64/copyright`)

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `gobject-introspection=1.82.0-4`

Binary Packages:

- `gir1.2-freedesktop:amd64=1.82.0-4`
- `gir1.2-freedesktop-dev:amd64=1.82.0-4`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/gobject-introspection/1.82.0-4/


### `dpkg` source package: `graphite2=1.3.14-2ubuntu1`

Binary Packages:

- `libgraphite2-3:amd64=1.3.14-2ubuntu1`
- `libgraphite2-dev:amd64=1.3.14-2ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libgraphite2-3/copyright`, `/usr/share/doc/libgraphite2-dev/copyright`)

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
$ apt-get source -qq --print-uris graphite2=1.3.14-2ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/g/graphite2/graphite2_1.3.14-2ubuntu1.dsc' graphite2_1.3.14-2ubuntu1.dsc 2650 SHA512:76b4ecf1d5c2fdbd4e50b434d39b83f7661a79047d14733b22f3b58ba621164b341a14cc6d0b018bd5101ecd8e9bcdcaa25ea6c05fab45eba64c96c41cde0902
'http://archive.ubuntu.com/ubuntu/pool/main/g/graphite2/graphite2_1.3.14.orig.tar.gz' graphite2_1.3.14.orig.tar.gz 6629829 SHA512:49d127964d3f5c9403c7aecbfb5b18f32f25fe4919a81c49e0534e7123fe845423e16b0b8c8baaae21162b1150ab3e0f1c22c344e07d4364b6b8473c40a0822c
'http://archive.ubuntu.com/ubuntu/pool/main/g/graphite2/graphite2_1.3.14-2ubuntu1.debian.tar.xz' graphite2_1.3.14-2ubuntu1.debian.tar.xz 14384 SHA512:6d25f7498c175c26533ae14088723110b9a35f5242e2b35e3a2cfe71bd92d2f855c013c11abce5c9cd058407c78940377c2fe97c1c6b3beaee41006ec24382a4
```

### `dpkg` source package: `grep=3.11-4build1`

Binary Packages:

- `grep=3.11-4build1`

Licenses: (parsed from: `/usr/share/doc/grep/copyright`)

- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris grep=3.11-4build1
'http://archive.ubuntu.com/ubuntu/pool/main/g/grep/grep_3.11-4build1.dsc' grep_3.11-4build1.dsc 2379 SHA512:5106f25775f36ba92fd7d73634d8c271fcea7dc9defef2f84d6080eb6a47dd0b1194272807267413807aa35d945c9bb66f076162d3eba539cc35eca5d255d2f9
'http://archive.ubuntu.com/ubuntu/pool/main/g/grep/grep_3.11.orig.tar.xz' grep_3.11.orig.tar.xz 1703776 SHA512:f254a1905a08c8173e12fbdd4fd8baed9a200217fba9d7641f0d78e4e002c1f2a621152d67027d9b25f0bb2430898f5233dc70909d8464fd13d7dd9298e65c42
'http://archive.ubuntu.com/ubuntu/pool/main/g/grep/grep_3.11.orig.tar.xz.asc' grep_3.11.orig.tar.xz.asc 833 SHA512:487aba063373ca0594c519991f19b2a6a33b3da0d74735c890f3828fd0880e7e6f64495d2c8f9efa5da53d1eb2d446609bab2399a4b89dcb4510a632e31ffb54
'http://archive.ubuntu.com/ubuntu/pool/main/g/grep/grep_3.11-4build1.debian.tar.xz' grep_3.11-4build1.debian.tar.xz 20584 SHA512:212c903c240071dda1d8e966991908730af26746558078262aa32b6b0683487cb510d9b9a2c40cafb31024e78e2c74d17eb5681e329aa142b0921b88cacef7eb
```

### `dpkg` source package: `gzip=1.12-1.1ubuntu1`

Binary Packages:

- `gzip=1.12-1.1ubuntu1`

Licenses: (parsed from: `/usr/share/doc/gzip/copyright`)

- `FSF-manpages`
- `GFDL-1.3+-no-invariant`
- `GFDL-3`
- `GPL-3`
- `GPL-3+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `harfbuzz=10.2.0-1`

Binary Packages:

- `gir1.2-harfbuzz-0.0:amd64=10.2.0-1`
- `libharfbuzz-cairo0:amd64=10.2.0-1`
- `libharfbuzz-dev:amd64=10.2.0-1`
- `libharfbuzz-gobject0:amd64=10.2.0-1`
- `libharfbuzz-icu0:amd64=10.2.0-1`
- `libharfbuzz-subset0:amd64=10.2.0-1`
- `libharfbuzz0b:amd64=10.2.0-1`

Licenses: (parsed from: `/usr/share/doc/gir1.2-harfbuzz-0.0/copyright`, `/usr/share/doc/libharfbuzz-cairo0/copyright`, `/usr/share/doc/libharfbuzz-dev/copyright`, `/usr/share/doc/libharfbuzz-gobject0/copyright`, `/usr/share/doc/libharfbuzz-icu0/copyright`, `/usr/share/doc/libharfbuzz-subset0/copyright`, `/usr/share/doc/libharfbuzz0b/copyright`)

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
'http://archive.ubuntu.com/ubuntu/pool/main/h/harfbuzz/harfbuzz_10.2.0-1.dsc' harfbuzz_10.2.0-1.dsc 2564 SHA512:298e1360eecf46909d0db80a85c679c5ecb16e750bd572145cc72c8e61e46710fd460c93d7b265e656e1043ce4c4bd43dfea19b25b6d94662070de30d63ed51b
'http://archive.ubuntu.com/ubuntu/pool/main/h/harfbuzz/harfbuzz_10.2.0.orig.tar.xz' harfbuzz_10.2.0.orig.tar.xz 17957608 SHA512:522028a5de91a042832b1634fc4b7636b1b42c5ee258882d155bc33fca7b30de19ca714b4f9ea8dc3d3f537142ca2305fcf5af04bec4edbf608f557c12742e54
'http://archive.ubuntu.com/ubuntu/pool/main/h/harfbuzz/harfbuzz_10.2.0-1.debian.tar.xz' harfbuzz_10.2.0-1.debian.tar.xz 20108 SHA512:52b16b140e1df7bbed5d240a608c30017626b16b31dba1b428d47797a0c4682172413202fe50e6b403c56599854077569abc8d5eef6f376653e3752bad1117d1
```

### `dpkg` source package: `hicolor-icon-theme=0.18-2`

Binary Packages:

- `hicolor-icon-theme=0.18-2`

Licenses: (parsed from: `/usr/share/doc/hicolor-icon-theme/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris hicolor-icon-theme=0.18-2
'http://archive.ubuntu.com/ubuntu/pool/main/h/hicolor-icon-theme/hicolor-icon-theme_0.18-2.dsc' hicolor-icon-theme_0.18-2.dsc 2325 SHA512:737bfba6c257b01f0eb9091d99f21b7592c14410980d5aaa4a1a5c04b942a51eafae84ad1d9e0b642c269ae7ffecafa7af6508063af1b49f00b23f4888d3ce37
'http://archive.ubuntu.com/ubuntu/pool/main/h/hicolor-icon-theme/hicolor-icon-theme_0.18.orig.tar.xz' hicolor-icon-theme_0.18.orig.tar.xz 29624 SHA512:07db44fb6bec797445740832fa2b3ba56f5f335834161a26a4e5f767a8c45c0885ef1189e887b56752bd20c4b1aac101c5d4a395df4177cd3817ee5105db0d37
'http://archive.ubuntu.com/ubuntu/pool/main/h/hicolor-icon-theme/hicolor-icon-theme_0.18.orig.tar.xz.asc' hicolor-icon-theme_0.18.orig.tar.xz.asc 833 SHA512:e00447c8918250978622a9465ac16181206deed977743d71faa068341f3aab4a1e98e70aed9f03e62806f2b3d8e1df20ff3b09332d0feda70d4532496154f0c2
'http://archive.ubuntu.com/ubuntu/pool/main/h/hicolor-icon-theme/hicolor-icon-theme_0.18-2.debian.tar.xz' hicolor-icon-theme_0.18-2.debian.tar.xz 9148 SHA512:2f29cfe942ddbe3cd3ca41006d1ab4e0014368767e6d8ac836ecf19bd7517301a422ee54c8970ee1d8b72b8bd8181aedb8cf4655bb88f6ebcd1903933077a8fb
```

### `dpkg` source package: `hostname=3.25`

Binary Packages:

- `hostname=3.25`

Licenses: (parsed from: `/usr/share/doc/hostname/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris hostname=3.25
'http://archive.ubuntu.com/ubuntu/pool/main/h/hostname/hostname_3.25.dsc' hostname_3.25.dsc 1519 SHA512:85590af72545c02ad4d84e63cf548b6277356f3b2cf448f5278409fbb87b40a2177a3bb983120effb838cdb8a546c5b243810ae558238fc5aff6f5fe1300e32b
'http://archive.ubuntu.com/ubuntu/pool/main/h/hostname/hostname_3.25.tar.xz' hostname_3.25.tar.xz 12804 SHA512:57b8e741cd3d895112d93ca8a7cbec95f3ad1a90c5691377ab8b242906bdcb932fa3401159432ec86f24bbbfe24c078832792c70e62e8d65a2317ee05a5efc64
```

### `dpkg` source package: `icu=76.1-1ubuntu2`

Binary Packages:

- `icu-devtools=76.1-1ubuntu2`
- `libicu-dev:amd64=76.1-1ubuntu2`
- `libicu76:amd64=76.1-1ubuntu2`

Licenses: (parsed from: `/usr/share/doc/icu-devtools/copyright`, `/usr/share/doc/libicu-dev/copyright`, `/usr/share/doc/libicu76/copyright`)

- `GPL-3`
- `MIT`

Source:

```console
$ apt-get source -qq --print-uris icu=76.1-1ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/i/icu/icu_76.1-1ubuntu2.dsc' icu_76.1-1ubuntu2.dsc 2343 SHA512:43e57fb6b7bc79604d11e1ba48fd5e2cd1958537118249768a4c80d8a7569b4fb2568fab4d1488d333b7c5b690650428e3b089e3bccbd7c0d014367cbe513ae3
'http://archive.ubuntu.com/ubuntu/pool/main/i/icu/icu_76.1.orig.tar.gz' icu_76.1.orig.tar.gz 27437767 SHA512:b702ab62fb37a1574d5f4a768326d0f8fa30d9db5b015605b5f8215b5d8547f83d84880c586d3dcc7b6c76f8d47ef34e04b0f51baa55908f737024dd79a42a6c
'http://archive.ubuntu.com/ubuntu/pool/main/i/icu/icu_76.1.orig.tar.gz.asc' icu_76.1.orig.tar.gz.asc 228 SHA512:c4bd81d4e98d7e37a6ba9540748c4ce1eb740d70bd689a13e2e51da76503b6e0287afd4d1cd3af4540210f37626dec998fcbd7269976cb801f238b789e604489
'http://archive.ubuntu.com/ubuntu/pool/main/i/icu/icu_76.1-1ubuntu2.debian.tar.xz' icu_76.1-1ubuntu2.debian.tar.xz 65132 SHA512:73cfe55930e1597e1e725b03005d9ff51e6332d159d2474c68139526c9dc41558a02a4f162a90b39a6d019599f3acc8b41f0899d1316aa3d2bf388c6c54e965d
```

### `dpkg` source package: `imagemagick=8:7.1.1.43+dfsg1-1`

Binary Packages:

- `imagemagick=8:7.1.1.43+dfsg1-1`
- `imagemagick-7-common=8:7.1.1.43+dfsg1-1`
- `imagemagick-7.q16=8:7.1.1.43+dfsg1-1`
- `libmagickcore-7-arch-config:amd64=8:7.1.1.43+dfsg1-1`
- `libmagickcore-7-headers=8:7.1.1.43+dfsg1-1`
- `libmagickcore-7.q16-10:amd64=8:7.1.1.43+dfsg1-1`
- `libmagickcore-7.q16-10-extra:amd64=8:7.1.1.43+dfsg1-1`
- `libmagickcore-7.q16-dev:amd64=8:7.1.1.43+dfsg1-1`
- `libmagickcore-dev=8:7.1.1.43+dfsg1-1`
- `libmagickwand-7-headers=8:7.1.1.43+dfsg1-1`
- `libmagickwand-7.q16-10:amd64=8:7.1.1.43+dfsg1-1`
- `libmagickwand-7.q16-dev:amd64=8:7.1.1.43+dfsg1-1`
- `libmagickwand-dev=8:7.1.1.43+dfsg1-1`

Licenses: (parsed from: `/usr/share/doc/imagemagick/copyright`, `/usr/share/doc/imagemagick-7-common/copyright`, `/usr/share/doc/imagemagick-7.q16/copyright`, `/usr/share/doc/libmagickcore-7-arch-config/copyright`, `/usr/share/doc/libmagickcore-7-headers/copyright`, `/usr/share/doc/libmagickcore-7.q16-10/copyright`, `/usr/share/doc/libmagickcore-7.q16-10-extra/copyright`, `/usr/share/doc/libmagickcore-7.q16-dev/copyright`, `/usr/share/doc/libmagickcore-dev/copyright`, `/usr/share/doc/libmagickwand-7-headers/copyright`, `/usr/share/doc/libmagickwand-7.q16-10/copyright`, `/usr/share/doc/libmagickwand-7.q16-dev/copyright`, `/usr/share/doc/libmagickwand-dev/copyright`)

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
$ apt-get source -qq --print-uris imagemagick=8:7.1.1.43+dfsg1-1
'http://archive.ubuntu.com/ubuntu/pool/universe/i/imagemagick/imagemagick_7.1.1.43%2bdfsg1-1.dsc' imagemagick_7.1.1.43+dfsg1-1.dsc 5129 SHA512:43b2f110f1add50dca8f193c87a05707baa5b9fa29029d90110928b169d0bab6075b3a4f852e335d5cb1dcf4ddfd45a3f6a99202c5168225b3d1d497357537b3
'http://archive.ubuntu.com/ubuntu/pool/universe/i/imagemagick/imagemagick_7.1.1.43%2bdfsg1.orig.tar.xz' imagemagick_7.1.1.43+dfsg1.orig.tar.xz 10501740 SHA512:790bc01e819d2e1c0a00581b8c8bbe10b185eb52e1cdf1312417c4bdca562fe4742374039a6d164e91c7e009f497a375ebf09f579902803b52f9e94354b72a31
'http://archive.ubuntu.com/ubuntu/pool/universe/i/imagemagick/imagemagick_7.1.1.43%2bdfsg1-1.debian.tar.xz' imagemagick_7.1.1.43+dfsg1-1.debian.tar.xz 275384 SHA512:cf44335ac54575d3f860b935e810ccf8a8b0cf94782fa393bf851fac99bb2f4b63f712131961ec63628f34e2d8400f65aa00b1995ff4b83692be8ea4d8e94d26
```

### `dpkg` source package: `imath=3.1.12-1ubuntu1`

Binary Packages:

- `libimath-3-1-29t64:amd64=3.1.12-1ubuntu1`
- `libimath-dev:amd64=3.1.12-1ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libimath-3-1-29t64/copyright`, `/usr/share/doc/libimath-dev/copyright`)

- `imath`

Source:

```console
$ apt-get source -qq --print-uris imath=3.1.12-1ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/universe/i/imath/imath_3.1.12-1ubuntu1.dsc' imath_3.1.12-1ubuntu1.dsc 2728 SHA512:16be0f55ee341daf74fb8f6867c1f1d7de9685056f1093d2af7d59e7eaef07d1fe5d26c21ad3efff8776e30df3f7d5cfaaad7a68b02c074bbba93703ba9b19b2
'http://archive.ubuntu.com/ubuntu/pool/universe/i/imath/imath_3.1.12.orig.tar.gz' imath_3.1.12.orig.tar.gz 604232 SHA512:32628dfcacb610310b81ffe017a66215cf5fb84c2e0a6ac8c94a68c048be3d2b97eb57965dd253770184d5824cce1e5440b8eefb2834666b273b3193ff108343
'http://archive.ubuntu.com/ubuntu/pool/universe/i/imath/imath_3.1.12.orig.tar.gz.asc' imath_3.1.12.orig.tar.gz.asc 287 SHA512:9b3978e44b531429aba42b9cc4969a470898d9d74652e3809edb0273ba9b127c471aec6570b5d352be738f59810091c0df2c70d39c16d2c32833d173b270f72c
'http://archive.ubuntu.com/ubuntu/pool/universe/i/imath/imath_3.1.12-1ubuntu1.debian.tar.xz' imath_3.1.12-1ubuntu1.debian.tar.xz 10172 SHA512:3c400791f845e9424585cdb7e51b1cfd6586a64d7d15e88392e1413b2e6f1c592cf0360e48e98c34e1ec16aa437b554a42087800268bd1678d45a0ad7ab4f14b
```

### `dpkg` source package: `init-system-helpers=1.67ubuntu1`

Binary Packages:

- `init-system-helpers=1.67ubuntu1`

Licenses: (parsed from: `/usr/share/doc/init-system-helpers/copyright`)

- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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
'http://archive.ubuntu.com/ubuntu/pool/main/i/isl/isl_0.27-1.dsc' isl_0.27-1.dsc 1829 SHA512:1dd37f08556f5adea516dfe737edac400b4aaf394b6e6dcbdc0bc194d96983f9e03523c1ecacb275e28dc415feacf3198376348cb543672ad742c1d6bb51ecc6
'http://archive.ubuntu.com/ubuntu/pool/main/i/isl/isl_0.27.orig.tar.xz' isl_0.27.orig.tar.xz 2056436 SHA512:6d6f50c3f6f26e0d3f67586dee6427d87999c426c94069a6f3012ec3c9a41adeebd50f43b5d2705db6abc12e38eb01c19f55dba113c0799da5f667eef46b2be0
'http://archive.ubuntu.com/ubuntu/pool/main/i/isl/isl_0.27-1.debian.tar.xz' isl_0.27-1.debian.tar.xz 24868 SHA512:71f034e81f666ebafa4ec331430fd679643e5d157b094f196c1a1841a0a22f79f46052523c8469ec95b71005e53a82599fe37c08e27b60d5d7f60e94eb50c916
```

### `dpkg` source package: `jansson=2.14-2build2`

Binary Packages:

- `libjansson4:amd64=2.14-2build2`

Licenses: (parsed from: `/usr/share/doc/libjansson4/copyright`)

- `Expat`

Source:

```console
$ apt-get source -qq --print-uris jansson=2.14-2build2
'http://archive.ubuntu.com/ubuntu/pool/main/j/jansson/jansson_2.14-2build2.dsc' jansson_2.14-2build2.dsc 2120 SHA512:46ec9f5477e738ee6ed2c10b7406dd0edcfe0148a394af3ca3ee214b14c9de95e691fefa34c3aa9770c1e23ec77d26b1f5149cc8faa4201f15680ba9f3a6d754
'http://archive.ubuntu.com/ubuntu/pool/main/j/jansson/jansson_2.14.orig.tar.gz' jansson_2.14.orig.tar.gz 141500 SHA512:c56e2e8d18819e3f5caa46edd4819694a240aeb3524a6f9d9f4465edf65b183d1870bd5d256cdd378d411a52979121369b951406fdf7bf323db5c30001fa1bc4
'http://archive.ubuntu.com/ubuntu/pool/main/j/jansson/jansson_2.14-2build2.debian.tar.xz' jansson_2.14-2build2.debian.tar.xz 5580 SHA512:1eec1f274a77512033b857a64bb26f8bc2fa98212c33c17dcfedbbd7f82711d32a803ad4ea4d8d158ef9949be2a69f3d5d4126fc4ac3b63c9200c361bba0f939
```

### `dpkg` source package: `jbigkit=2.1-6.1ubuntu2`

Binary Packages:

- `libjbig-dev:amd64=2.1-6.1ubuntu2`
- `libjbig0:amd64=2.1-6.1ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libjbig-dev/copyright`, `/usr/share/doc/libjbig0/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris jbigkit=2.1-6.1ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/j/jbigkit/jbigkit_2.1-6.1ubuntu2.dsc' jbigkit_2.1-6.1ubuntu2.dsc 2199 SHA512:6c5e2f89ed58fd018e27fa73352952192a347c19f8c0a454a2c9e3f9ab90d06bc578f522b32d074100f5de44a8d9d62b3d096fbb7f5f01e2bd803b37a8104de3
'http://archive.ubuntu.com/ubuntu/pool/main/j/jbigkit/jbigkit_2.1.orig.tar.gz' jbigkit_2.1.orig.tar.gz 438710 SHA512:c4127480470ef90db1ef3bd2caa444df10b50ed8df0bc9997db7612cb48b49278baf44965028f1807a21028eb965d677e015466306b44683c4ec75a23e1922cf
'http://archive.ubuntu.com/ubuntu/pool/main/j/jbigkit/jbigkit_2.1-6.1ubuntu2.debian.tar.xz' jbigkit_2.1-6.1ubuntu2.debian.tar.xz 11172 SHA512:1ecf331f4e530f5f3105c57c2d7b366591f113220745f143b9335f3e383bf04dd963d61aecc4c8eb16ef4ecc74a2f5e2743779d95dcd8626dc6eaea8b2824c18
```

### `dpkg` source package: `keyutils=1.6.3-4ubuntu2`

Binary Packages:

- `libkeyutils1:amd64=1.6.3-4ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libkeyutils1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2`
- `LGPL-2+`

Source:

```console
$ apt-get source -qq --print-uris keyutils=1.6.3-4ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/k/keyutils/keyutils_1.6.3-4ubuntu2.dsc' keyutils_1.6.3-4ubuntu2.dsc 2186 SHA512:3da12fdd088944b7f625699d87b48cbff1048191cc60f304abaf5b7e802a75ba0dadad84bac80c4d6d6071585422b550052fb9d6afb8c66addfe959c69d32cac
'http://archive.ubuntu.com/ubuntu/pool/main/k/keyutils/keyutils_1.6.3.orig.tar.gz' keyutils_1.6.3.orig.tar.gz 137022 SHA512:f65965b8566037078b8eeffa66c6fdbe121c8c2bea7fa5bce04cf7ba5ccc50d5b48e51f4a67ca91e4d5d9a12469e7e3eb3036c920ab25e3feba6e93b4c149cf9
'http://archive.ubuntu.com/ubuntu/pool/main/k/keyutils/keyutils_1.6.3-4ubuntu2.debian.tar.xz' keyutils_1.6.3-4ubuntu2.debian.tar.xz 14684 SHA512:454dd26c32f44c5c608288b243ff2a13a9aa4122e28f942be6c0ccca299d83901cefda9ef6bdad82b3bb8e8a1f0a9e4fd3e85f8f86ca8fdf159d086e99c07583
```

### `dpkg` source package: `krb5=1.21.3-4ubuntu1`

Binary Packages:

- `krb5-multidev:amd64=1.21.3-4ubuntu1`
- `libgssapi-krb5-2:amd64=1.21.3-4ubuntu1`
- `libgssrpc4t64:amd64=1.21.3-4ubuntu1`
- `libk5crypto3:amd64=1.21.3-4ubuntu1`
- `libkadm5clnt-mit12:amd64=1.21.3-4ubuntu1`
- `libkadm5srv-mit12:amd64=1.21.3-4ubuntu1`
- `libkdb5-10t64:amd64=1.21.3-4ubuntu1`
- `libkrb5-3:amd64=1.21.3-4ubuntu1`
- `libkrb5-dev:amd64=1.21.3-4ubuntu1`
- `libkrb5support0:amd64=1.21.3-4ubuntu1`

Licenses: (parsed from: `/usr/share/doc/krb5-multidev/copyright`, `/usr/share/doc/libgssapi-krb5-2/copyright`, `/usr/share/doc/libgssrpc4t64/copyright`, `/usr/share/doc/libk5crypto3/copyright`, `/usr/share/doc/libkadm5clnt-mit12/copyright`, `/usr/share/doc/libkadm5srv-mit12/copyright`, `/usr/share/doc/libkdb5-10t64/copyright`, `/usr/share/doc/libkrb5-3/copyright`, `/usr/share/doc/libkrb5-dev/copyright`, `/usr/share/doc/libkrb5support0/copyright`)

- `GPL-2`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `lcms2=2.16-2`

Binary Packages:

- `liblcms2-2:amd64=2.16-2`
- `liblcms2-dev:amd64=2.16-2`

Licenses: (parsed from: `/usr/share/doc/liblcms2-2/copyright`, `/usr/share/doc/liblcms2-dev/copyright`)

- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `IJG`
- `MIT`

Source:

```console
$ apt-get source -qq --print-uris lcms2=2.16-2
'http://archive.ubuntu.com/ubuntu/pool/main/l/lcms2/lcms2_2.16-2.dsc' lcms2_2.16-2.dsc 1972 SHA512:aef216c633a66a3d25890a8b10c99484b164c001c3301b4d7304bcaf7703f4a45a1e1f9d6b4cf7ab51dd4a55588da65b17b959412380fd644158aaa7d02c023a
'http://archive.ubuntu.com/ubuntu/pool/main/l/lcms2/lcms2_2.16.orig.tar.gz' lcms2_2.16.orig.tar.gz 7632822 SHA512:638dd6ad6787456c8145510d18b2d0727bd0a446a13ac2934aabc9531d1156eca2a2c0fd780a453823fbd35a1895f9d8de5dc4b3cab505459dd3f0535b4e837d
'http://archive.ubuntu.com/ubuntu/pool/main/l/lcms2/lcms2_2.16-2.debian.tar.xz' lcms2_2.16-2.debian.tar.xz 11908 SHA512:35efa3dee1a2ab47c18f97f29247dc2dbec35b39c3c783511520eed3ac3b29b067a1398b7d0cb86b07734f6b0ba41680e8f13cbf10a26e3241afe8344f4b14a5
```

### `dpkg` source package: `lerc=4.0.0+ds-5ubuntu1`

Binary Packages:

- `liblerc-dev:amd64=4.0.0+ds-5ubuntu1`
- `liblerc4:amd64=4.0.0+ds-5ubuntu1`

Licenses: (parsed from: `/usr/share/doc/liblerc-dev/copyright`, `/usr/share/doc/liblerc4/copyright`)

- `Apache-2.0`

Source:

```console
$ apt-get source -qq --print-uris lerc=4.0.0+ds-5ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/l/lerc/lerc_4.0.0%2bds-5ubuntu1.dsc' lerc_4.0.0+ds-5ubuntu1.dsc 2739 SHA512:3b9c2a8238c78ab2fa82d8a2b0f30a9e627c70eeba450710da1346f14f1e78bece63c6220fa90d1f0eb69455bb5a085d08a66dedd7d59436258e0aad7ab26e7e
'http://archive.ubuntu.com/ubuntu/pool/main/l/lerc/lerc_4.0.0%2bds.orig.tar.xz' lerc_4.0.0+ds.orig.tar.xz 348140 SHA512:d5539360fa92f40319466fea73a66d0d03aedff886fb75985bfcaeeb77ef516b9fa24b8d83da09c114bf6090bbd68e64d9ac2649a19315895134fa86023478e1
'http://archive.ubuntu.com/ubuntu/pool/main/l/lerc/lerc_4.0.0%2bds-5ubuntu1.debian.tar.xz' lerc_4.0.0+ds-5ubuntu1.debian.tar.xz 8720 SHA512:82bc4623d2174185c1b82e316aedb1d55815aec0e67f6fd5e6c6b559b2668e23a2edb80dbb6502bca3dd15ef4dc9628767256d2ad7e157002f05c4eb31cc83fa
```

### `dpkg` source package: `libassuan=3.0.1-2`

Binary Packages:

- `libassuan9:amd64=3.0.1-2`

Licenses: (parsed from: `/usr/share/doc/libassuan9/copyright`)

- `FSFULLR`
- `FSFULLRWD`
- `GPL-2`
- `GPL-2+ with Autoconf-data exception`
- `GPL-2+ with Libtool exception`
- `GPL-2.with.nonstandard.Autoconf-data.exception`
- `GPL-3`
- `GPL-3+`
- `GPL-3+ with Autoconf-2.0~Archive exception`
- `GPL-3+ with Autoconf-data exception`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`
- `LGPL-3+`
- `X11`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/libassuan/3.0.1-2/


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
'http://archive.ubuntu.com/ubuntu/pool/main/libb/libbsd/libbsd_0.12.2-2.dsc' libbsd_0.12.2-2.dsc 2446 SHA512:253b89208ff4acafb45c4294fe668d15d7a2f539745dffe6fdb4464fa672e39631dd92f17da4fe44f3084a967b783a39ea221cdd48fbbb30c49f520d60a0c447
'http://archive.ubuntu.com/ubuntu/pool/main/libb/libbsd/libbsd_0.12.2.orig.tar.xz' libbsd_0.12.2.orig.tar.xz 446032 SHA512:ce43e4f0486d5f00d4a8119ee863eaaa2f968cae4aa3d622976bb31ad601dfc565afacef7ebade5eba33fff1c329b5296c6387c008d1e1805d878431038f8b21
'http://archive.ubuntu.com/ubuntu/pool/main/libb/libbsd/libbsd_0.12.2.orig.tar.xz.asc' libbsd_0.12.2.orig.tar.xz.asc 833 SHA512:c2e56aa572ce50d6342c0e45622958eba40319e09d45dc3cff6296cb10eebc0c4154d6f758dd2470a1794251fc0273d05ac2d735698eae83183769df5f7d44c3
'http://archive.ubuntu.com/ubuntu/pool/main/libb/libbsd/libbsd_0.12.2-2.debian.tar.xz' libbsd_0.12.2-2.debian.tar.xz 18688 SHA512:82241267d3fdba624a118af842647cd2a57c202fb9a1f53b5303e258e3a55a9d33bf52e449c4d2656cd5baf8059f2976a082c592c30b0f4ac800ab48ab9d1dec
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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/libcap-ng/0.8.5-4/


### `dpkg` source package: `libcap2=1:2.66-5ubuntu3`

Binary Packages:

- `libcap2:amd64=1:2.66-5ubuntu3`

Licenses: (parsed from: `/usr/share/doc/libcap2/copyright`)

- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libcbor=0.10.2-1.2ubuntu2`

Binary Packages:

- `libcbor0.10:amd64=0.10.2-1.2ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libcbor0.10/copyright`)

- `Expat`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libdatrie=0.2.13-3build1`

Binary Packages:

- `libdatrie-dev:amd64=0.2.13-3build1`
- `libdatrie1:amd64=0.2.13-3build1`

Licenses: (parsed from: `/usr/share/doc/libdatrie-dev/copyright`, `/usr/share/doc/libdatrie1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris libdatrie=0.2.13-3build1
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libdatrie/libdatrie_0.2.13-3build1.dsc' libdatrie_0.2.13-3build1.dsc 2368 SHA512:37dc9a866dc340d8291bcb07cdb8a20f39ba8ee0dca0c8c37cbbfb9403afe0a8229b18f1d019a54d19855977ac499df9067e7ecdf0a297cedc4d239e67353272
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libdatrie/libdatrie_0.2.13.orig.tar.xz' libdatrie_0.2.13.orig.tar.xz 314072 SHA512:db3c879d825ead5871c12ef3a06bb093cb1708a6e7e20775eaf82356af9dd6ad54c6b5cabbe1773f2494d3dfa2426528fdd49441038b6294b70ccb1a3d90099a
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libdatrie/libdatrie_0.2.13-3build1.debian.tar.xz' libdatrie_0.2.13-3build1.debian.tar.xz 9776 SHA512:a44919cfcb079af400a09c4f9468cf16edc3fc05fe46bf57b7a22abd80130da91b5ce3b6d8c8cacfa8c0f48b751220b0b74bc624be433db01b3ab1aac9bc6524
```

### `dpkg` source package: `libde265=1.0.15-1build4`

Binary Packages:

- `libde265-0:amd64=1.0.15-1build4`

Licenses: (parsed from: `/usr/share/doc/libde265-0/copyright`)

- `BSD-4-clause`
- `GPL-3`
- `GPL-3+`
- `LGPL-3`
- `LGPL-3+`
- `other-1`
- `public-domain-1`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libdeflate=1.23-1`

Binary Packages:

- `libdeflate-dev:amd64=1.23-1`
- `libdeflate0:amd64=1.23-1`

Licenses: (parsed from: `/usr/share/doc/libdeflate-dev/copyright`, `/usr/share/doc/libdeflate0/copyright`)

- `Expat`

Source:

```console
$ apt-get source -qq --print-uris libdeflate=1.23-1
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libdeflate/libdeflate_1.23-1.dsc' libdeflate_1.23-1.dsc 2214 SHA512:38ee39d08cb0febc46a045b7543232a3e75fd4e13e7b935caf2f1dcf23013e4658eea80291d7be98f137bf03c35f11cfdbe49b732398c752b3bb5b64e3ab5dfd
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libdeflate/libdeflate_1.23.orig.tar.gz' libdeflate_1.23.orig.tar.gz 197519 SHA512:c1effb9c5ee8d65bc12ae3d0669a4a394acace13cc146300ed24a7f12a0ec058f66729e1ffbae268711bdcc4151143752ab2d56a099dd6394b2735e8e2f1b671
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libdeflate/libdeflate_1.23-1.debian.tar.xz' libdeflate_1.23-1.debian.tar.xz 5536 SHA512:055aa489f11601aeaee6b1d90fafaa8449ee26c870fe60e02d5683e66b0266dda9a5ffc5d0998b321aad8796d4cb0229897913d0f35376714b1dd53427959233
```

### `dpkg` source package: `libedit=3.1-20250104-1`

Binary Packages:

- `libedit2:amd64=3.1-20250104-1`

Licenses: (parsed from: `/usr/share/doc/libedit2/copyright`)

- `BSD-3-clause`

Source:

```console
$ apt-get source -qq --print-uris libedit=3.1-20250104-1
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libedit/libedit_3.1-20250104-1.dsc' libedit_3.1-20250104-1.dsc 2264 SHA512:3d793923e391f99ebf58e307b6fe385336eeab7973aaffa6be7bfd6ba66d082a325f920f0bea4e3fa745497c6f3cba1cc29b22679febb5f21054c9543f04cd4c
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libedit/libedit_3.1-20250104.orig.tar.gz' libedit_3.1-20250104.orig.tar.gz 546745 SHA512:4b4a8b4b1f2cb952bbb3d128605eba9bc7cd0ad35c44b2c099f067c8bea69455bd11faae4ff20384bbe0ea901b25a1249d8323dea4ccd6141a17393f62bb8df2
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libedit/libedit_3.1-20250104-1.debian.tar.xz' libedit_3.1-20250104-1.debian.tar.xz 16708 SHA512:c297c78cc62ac31051dcb5b601c1b462f62341d75a3f0d0b804920e6d64c881884e7f52762cc7b77a47a962fbb19744e04f2da9789a6a4344079d3009595170c
```

### `dpkg` source package: `liberror-perl=0.17029-2`

Binary Packages:

- `liberror-perl=0.17029-2`

Licenses: (parsed from: `/usr/share/doc/liberror-perl/copyright`)

- `Artistic`
- `GPL-1`
- `GPL-1+`
- `MIT/X11`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/liberror-perl/0.17029-2/


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
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libevent/libevent_2.1.12-stable-10.dsc' libevent_2.1.12-stable-10.dsc 2412 SHA512:969e1fd08a03875ec0148230fa9a755831b02d3723623e077320d509e1cf22eb6d7e5decbba26a76314d8060d55aac28c8f8a0ba556a00a51d9e50fec0570163
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libevent/libevent_2.1.12-stable.orig.tar.gz' libevent_2.1.12-stable.orig.tar.gz 1100847 SHA512:88d8944cd75cbe78bc4e56a6741ca67c017a3686d5349100f1c74f8a68ac0b6410ce64dff160be4a4ba0696ee29540dfed59aaf3c9a02f0c164b00307fcfe84f
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libevent/libevent_2.1.12-stable-10.debian.tar.xz' libevent_2.1.12-stable-10.debian.tar.xz 17908 SHA512:164b8ff27a7e9313e96fae90449888d878b8aa81ed0a1415813dd58be8db3eccf2358ec882986fa178d9c352b93c6a6e59200eaf954d7b1d8a92138fa5b8b895
```

### `dpkg` source package: `libexif=0.6.25-1`

Binary Packages:

- `libexif-dev:amd64=0.6.25-1`
- `libexif12:amd64=0.6.25-1`

Licenses: (parsed from: `/usr/share/doc/libexif-dev/copyright`, `/usr/share/doc/libexif12/copyright`)

- `BSD-3-Clause`
- `CC0-1.0`
- `GPL-2`
- `GPL-2.0`
- `LGPL-2.1`
- `LGPL-2.1-or-later`
- `LicenseRef-Wrobel`
- `MIT`

Source:

```console
$ apt-get source -qq --print-uris libexif=0.6.25-1
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libexif/libexif_0.6.25-1.dsc' libexif_0.6.25-1.dsc 2091 SHA512:88aef3e10eeae981c444a91ac6df72ef36746160b6877fbf1a04a2e74e4efd949a5b523958be89e907beec71b7a57e69b78314287a5b5a8d4d2ad9326620b15f
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libexif/libexif_0.6.25.orig.tar.gz' libexif_0.6.25.orig.tar.gz 1253324 SHA512:9e42af0d898a9d832d7b146a2085fb08eafdbb5ae476184aee1b495632172749d910f581246d22a0c68382ea9d969de54bd9539d4d877ad4dd6ca989e1b6d8db
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libexif/libexif_0.6.25-1.debian.tar.xz' libexif_0.6.25-1.debian.tar.xz 12104 SHA512:6dfe96e1debf860c3aa81bbcdd7a04ae88219702205082e38b38804390b4c7e5ed664ffc68b4c73c3fb29c0535622cddbb26ef071c9efd09c93f9f13ed8cb2b5
```

### `dpkg` source package: `libffi=3.4.6-1build1`

Binary Packages:

- `libffi-dev:amd64=3.4.6-1build1`
- `libffi8:amd64=3.4.6-1build1`

Licenses: (parsed from: `/usr/share/doc/libffi-dev/copyright`, `/usr/share/doc/libffi8/copyright`)

- `Expat`
- `GPL`
- `GPL-2+`
- `GPL-3+`
- `LGPL-2.1+`
- `MPL-1.1`
- `X11`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libfido2/libfido2_1.15.0-1.dsc' libfido2_1.15.0-1.dsc 2585 SHA512:d2f279927ea33d6f7b5d130d5058fc6fdb3f905ee51618e4f421d46a6fb7e638986987e7974483b67fe2bd32bb12607fe0adf7130d628ba5ec6f93c576e1c682
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libfido2/libfido2_1.15.0.orig.tar.gz' libfido2_1.15.0.orig.tar.gz 670019 SHA512:cca142e3b3b7e216289934785fcad6be3bcd344001445f04fcecf01d4f568523b949c7204eec2f32faf12605a98c7496b9f64bb34d6a312342fa997689e61635
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libfido2/libfido2_1.15.0.orig.tar.gz.asc' libfido2_1.15.0.orig.tar.gz.asc 228 SHA512:577f592b236e5182d92b7790600bd038b0b0019a7db0efada77e7af3ec04264fdb51cdb00ff5a32e68ca478951c59646b786c57a124932d43410e37a672d0fd5
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libfido2/libfido2_1.15.0-1.debian.tar.xz' libfido2_1.15.0-1.debian.tar.xz 52960 SHA512:574a8032af24a5c17669a4493ef75dcc787fb6a10cc233a875cda80269089d75f9001421a1625a17ba375305fcd597fe1ec76f82c39efea4697d7f1d6b3b89c3
```

### `dpkg` source package: `libgcrypt20=1.11.0-6ubuntu1`

Binary Packages:

- `libgcrypt20:amd64=1.11.0-6ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libgcrypt20/copyright`)

- `GPL-2`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris libgcrypt20=1.11.0-6ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgcrypt20/libgcrypt20_1.11.0-6ubuntu1.dsc' libgcrypt20_1.11.0-6ubuntu1.dsc 2984 SHA512:4f63db3009d6a91aa989f0b8c45d1a6f722f89f99829b464222d1fdddc0c1df383cf6403fedfa9739637f219b9756f11a4c4c245fe42908968af8b7701fc844b
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgcrypt20/libgcrypt20_1.11.0.orig.tar.bz2' libgcrypt20_1.11.0.orig.tar.bz2 4180345 SHA512:8e093e69e3c45d30838625ca008e995556f0d5b272de1c003d44ef94633bcc0d0ef5d95e8725eb531bfafb4490ac273488633e0c801200d4666194f86c3e270e
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgcrypt20/libgcrypt20_1.11.0.orig.tar.bz2.asc' libgcrypt20_1.11.0.orig.tar.bz2.asc 228 SHA512:eebd4c599bd8f375445566c3c73df5a223f256cb650cf18d8fed033a1f13a1fb8b9b10a17d686be21ad2bced60fc8e27d71b07e5f556a854a893e44c5dd81ae7
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgcrypt20/libgcrypt20_1.11.0-6ubuntu1.debian.tar.xz' libgcrypt20_1.11.0-6ubuntu1.debian.tar.xz 39784 SHA512:d7cb33ed130ba6de0339aa1030a13a5e272a2d43f26f9922107d1699f0c339c968aa538c014b817e8a2815141be2e2147deb7f0d3402be99ed256c14f621b105
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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/libgpg-error/1.51-2/


### `dpkg` source package: `libheif=1.19.5-1build1`

Binary Packages:

- `libheif-plugin-aomdec:amd64=1.19.5-1build1`
- `libheif-plugin-libde265:amd64=1.19.5-1build1`
- `libheif1:amd64=1.19.5-1build1`

Licenses: (parsed from: `/usr/share/doc/libheif-plugin-aomdec/copyright`, `/usr/share/doc/libheif-plugin-libde265/copyright`, `/usr/share/doc/libheif1/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `BSD-4-Clause-UC`
- `BSL-1.0`
- `Expat`
- `GPL-3`
- `GPL-3+`
- `LGPL-3`
- `LGPL-3+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libice=2:1.1.1-1`

Binary Packages:

- `libice-dev:amd64=2:1.1.1-1`
- `libice6:amd64=2:1.1.1-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libice=2:1.1.1-1
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libice/libice_1.1.1-1.dsc' libice_1.1.1-1.dsc 2021 SHA512:a96662e9557995e259d446b7272bc51c26250bbbb0884c2b1fe98d45276ef4ccca08d151b29d6669d6706c24d0978b49d0c75d19d3f5281c5d688a85de7ada98
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libice/libice_1.1.1.orig.tar.gz' libice_1.1.1.orig.tar.gz 489944 SHA512:e39fc7f76c19c4edc3e520b7cef16f9f65c4723f4d3603f7e664c54a5fe8fdd756f9a8bb2dc3b0ccf6646a8d1d202cba1cfa220e160b32e233a37c2cc7d13f1d
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libice/libice_1.1.1-1.diff.gz' libice_1.1.1-1.diff.gz 7355 SHA512:82b7e1a2049d0bca6d8df3c332f9de348668e144c4028bb376bdcee9b13b140bfcb32a7770bb4487ef81138a62ed1674c55c0611a0a948919af670bb3e02aa86
```

### `dpkg` source package: `libidn2=2.3.7-2build2`

Binary Packages:

- `libidn2-0:amd64=2.3.7-2build2`
- `libidn2-dev:amd64=2.3.7-2build2`

Licenses: (parsed from: `/usr/share/doc/libidn2-0/copyright`, `/usr/share/doc/libidn2-dev/copyright`)

- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `LGPL-3`
- `LGPL-3+`
- `Unicode`

Source:

```console
$ apt-get source -qq --print-uris libidn2=2.3.7-2build2
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libidn2/libidn2_2.3.7-2build2.dsc' libidn2_2.3.7-2build2.dsc 2643 SHA512:0c8575d0c7ab0ebe6bc8dfd3cbe966090f074793d7a91a11fcd7e5bcb0939c4d5cbfd25917396baf523e2a2d334b60e38774e04a7649a3a140ab9599f151cfa8
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libidn2/libidn2_2.3.7.orig.tar.gz' libidn2_2.3.7.orig.tar.gz 2155214 SHA512:eab5702bc0baed45492f8dde43a4d2ea3560ad80645e5f9e0cfa8d3b57bccd7fd782d04638e000ba07924a5d9f85e760095b55189188c4017b94705bef9b4a66
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libidn2/libidn2_2.3.7.orig.tar.gz.asc' libidn2_2.3.7.orig.tar.gz.asc 228 SHA512:00e5f8c3b6b1aef9ee341db99b339217080a57dbe65fba56798d60ad4be971a9535d8ae27e1f243b18b9fc9e900ada6c452b040a6c8094d5e05d8a76d1d79c03
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libidn2/libidn2_2.3.7-2build2.debian.tar.xz' libidn2_2.3.7-2build2.debian.tar.xz 16452 SHA512:55a812a877b2a8039d4105bb8509f389613ad8cb469eb560a3c08085578c448eff1ee1277f69df0505072b1d77ebc6104ad29cd0b6e84be5c56f74e5d0f8ba50
```

### `dpkg` source package: `libjpeg-turbo=2.1.5-3ubuntu2`

Binary Packages:

- `libjpeg-turbo8:amd64=2.1.5-3ubuntu2`
- `libjpeg-turbo8-dev:amd64=2.1.5-3ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libjpeg-turbo8/copyright`, `/usr/share/doc/libjpeg-turbo8-dev/copyright`)

- `BSD-3-clause`
- `BSD-BY-LC-NE`
- `Expat`
- `NTP`
- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris libjpeg-turbo=2.1.5-3ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/libj/libjpeg-turbo/libjpeg-turbo_2.1.5-3ubuntu2.dsc' libjpeg-turbo_2.1.5-3ubuntu2.dsc 2514 SHA512:d2c4cc928c9de4ebff4c5c90c558da3a09ffb0e7a336e1c3ed1a1561ccb5261f7c20ae4505b16ab8ff5853ede1d5aeccfcb0409f251fc49ac4b76bef2715a2ba
'http://archive.ubuntu.com/ubuntu/pool/main/libj/libjpeg-turbo/libjpeg-turbo_2.1.5.orig.tar.gz' libjpeg-turbo_2.1.5.orig.tar.gz 2264471 SHA512:20036303fbe5703a5742dc3778cc5deb2eb98d00a9852e7e80ba73c195bba011ec206c090589c482f1153f74505c3fe06d96af00f6beaa65a7fcf7ffaf626fc2
'http://archive.ubuntu.com/ubuntu/pool/main/libj/libjpeg-turbo/libjpeg-turbo_2.1.5-3ubuntu2.debian.tar.xz' libjpeg-turbo_2.1.5-3ubuntu2.debian.tar.xz 108780 SHA512:6099dbfaa7f42b0e48844a4b5e38bfb139b714143a6a18885cc604a1aed739abd774b2d32eebdddff4691ad8653653ef8a3ecebe1051ddf8792a6096523eb70d
```

### `dpkg` source package: `libjpeg8-empty=8c-2ubuntu11`

Binary Packages:

- `libjpeg-dev:amd64=8c-2ubuntu11`
- `libjpeg8:amd64=8c-2ubuntu11`
- `libjpeg8-dev:amd64=8c-2ubuntu11`

Licenses: (parsed from: `/usr/share/doc/libjpeg-dev/copyright`, `/usr/share/doc/libjpeg8/copyright`, `/usr/share/doc/libjpeg8-dev/copyright`)

- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libjpeg8-empty=8c-2ubuntu11
'http://archive.ubuntu.com/ubuntu/pool/main/libj/libjpeg8-empty/libjpeg8-empty_8c-2ubuntu11.dsc' libjpeg8-empty_8c-2ubuntu11.dsc 1579 SHA512:345994a54ea05e741e0e6d35f0a7fc39f45c3fc34a995e972ae6b2843baf0b2fcc0bf4726aa7bb86249e39f46a7e23a273d2430d0fcb9bb88f03c6e9d3c912aa
'http://archive.ubuntu.com/ubuntu/pool/main/libj/libjpeg8-empty/libjpeg8-empty_8c-2ubuntu11.tar.gz' libjpeg8-empty_8c-2ubuntu11.tar.gz 1959 SHA512:eb9cec5b6f3fa5e65950b72c14709d33e638b52a2bd2ac2f2297e0edb9e9e224e6da9bbe355e082026b92d980614e8fe40196e4a3ed7cdd560a65f03b138782b
```

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
'http://archive.ubuntu.com/ubuntu/pool/main/libk/libksba/libksba_1.6.7-2.dsc' libksba_1.6.7-2.dsc 2482 SHA512:239da32159ba455f0f76d8a89899e177a04e4621220d24c62b3faa341508d9ee9ac56fccee881b3c2bcba6965806f1c2083c49c47beb0c805ab8e8650975406b
'http://archive.ubuntu.com/ubuntu/pool/main/libk/libksba/libksba_1.6.7.orig.tar.bz2' libksba_1.6.7.orig.tar.bz2 706437 SHA512:60cb9df9f502ca479818f45b78c4bc2b78f6f359be2b8da489ea98f8896a43ab2c20cf97526b79a3220fb32f1701e62a6481fe61e91e567186ecf4f33d8e64d3
'http://archive.ubuntu.com/ubuntu/pool/main/libk/libksba/libksba_1.6.7.orig.tar.bz2.asc' libksba_1.6.7.orig.tar.bz2.asc 228 SHA512:66208b8e4fe76a753943f13a0e65b765eb496013f7f9aeb0b66a454dfb8c67794d1b70841a4014ef0c7ac4642d7b56c38b35cb34be9d8ee8ea6820cc13db53aa
'http://archive.ubuntu.com/ubuntu/pool/main/libk/libksba/libksba_1.6.7-2.debian.tar.xz' libksba_1.6.7-2.debian.tar.xz 14872 SHA512:92fd1450d10419f232cc0e0604f232aae57cff4b05b471b456ed21d40d36c1bfaba7f108cfc57a856d409cbd5421a47cb1d4ca848b127a73161e7f1c0e4e332e
```

### `dpkg` source package: `liblqr=0.4.2-2.1build2`

Binary Packages:

- `liblqr-1-0:amd64=0.4.2-2.1build2`
- `liblqr-1-0-dev:amd64=0.4.2-2.1build2`

Licenses: (parsed from: `/usr/share/doc/liblqr-1-0/copyright`, `/usr/share/doc/liblqr-1-0-dev/copyright`)

- `GPL-3`
- `GPLv3`
- `LGPL-3`

Source:

```console
$ apt-get source -qq --print-uris liblqr=0.4.2-2.1build2
'http://archive.ubuntu.com/ubuntu/pool/universe/libl/liblqr/liblqr_0.4.2-2.1build2.dsc' liblqr_0.4.2-2.1build2.dsc 2096 SHA512:30b38f252c27f4d20ef46e5c923eb0da2ba7e32fdb4277181980c6e0f82de4d5624cfd51339a3a16883357b1f6db4f6b8cf827be09f14c882752ec866ed5ca08
'http://archive.ubuntu.com/ubuntu/pool/universe/libl/liblqr/liblqr_0.4.2.orig.tar.gz' liblqr_0.4.2.orig.tar.gz 439884 SHA512:acfa5868c41ea145092711e84d6c9eb62cb725b3d7531917b0d91b7d4af2a9912b18a96edc2594a826f09dabe0a0a82936ceea7d1f31301a23d558b1450d2547
'http://archive.ubuntu.com/ubuntu/pool/universe/libl/liblqr/liblqr_0.4.2-2.1build2.debian.tar.xz' liblqr_0.4.2-2.1build2.debian.tar.xz 5448 SHA512:ff140c20c1683b3fc3c4a91682d72214a39ce60b4a3ecaf9bbfdf6229b79a48e2d38e26009f2243dafc953bad3c54ef8520de2dad51b762ba0d019691a678ce2
```

### `dpkg` source package: `libmaxminddb=1.11.0-1`

Binary Packages:

- `libmaxminddb-dev:amd64=1.11.0-1`
- `libmaxminddb0:amd64=1.11.0-1`

Licenses: (parsed from: `/usr/share/doc/libmaxminddb-dev/copyright`, `/usr/share/doc/libmaxminddb0/copyright`)

- `Apache-2.0`
- `BSD-2-clause`
- `BSD-3-clause`
- `Expat`
- `LGPL-3`
- `LGPL-3.0+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/libmaxminddb/1.11.0-1/


### `dpkg` source package: `libmd=1.1.0-2build2`

Binary Packages:

- `libmd0:amd64=1.1.0-2build2`

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
$ apt-get source -qq --print-uris libmd=1.1.0-2build2
'http://archive.ubuntu.com/ubuntu/pool/main/libm/libmd/libmd_1.1.0-2build2.dsc' libmd_1.1.0-2build2.dsc 2383 SHA512:d5d7a38fe932fa60a25630e0ba3ab5ef231b47ac5190e3b04e5c6130f8121a440594955031f9bc52338a29af0b119c696171b3447c46ac71967d7878fd572cd0
'http://archive.ubuntu.com/ubuntu/pool/main/libm/libmd/libmd_1.1.0.orig.tar.xz' libmd_1.1.0.orig.tar.xz 271228 SHA512:5d0da3337038e474fae7377bbc646d17214e72dc848a7aadc157f49333ce7b5ac1456e45d13674bd410ea08477c6115fc4282fed6c8e6a0bf63537a418c0df96
'http://archive.ubuntu.com/ubuntu/pool/main/libm/libmd/libmd_1.1.0.orig.tar.xz.asc' libmd_1.1.0.orig.tar.xz.asc 833 SHA512:b0ff3baa7eedc205ee6f8b844859145fa6922c39e8f62f1e997851a65b2881649b438a37baa5800d140541da6f4dacc9f92a370f945d7461937b8cdedeca1cef
'http://archive.ubuntu.com/ubuntu/pool/main/libm/libmd/libmd_1.1.0-2build2.debian.tar.xz' libmd_1.1.0-2build2.debian.tar.xz 8428 SHA512:3e4caf3b94503176a782241f319a5ed19fb3e9e8dd4056e59beb6fd7208c45ce77396fdd2e8a9c18ca19a65f93b49834853b13f2fbba59195e5499736113d776
```

### `dpkg` source package: `libpng1.6=1.6.46-4`

Binary Packages:

- `libpng-dev:amd64=1.6.46-4`
- `libpng16-16t64:amd64=1.6.46-4`

Licenses: (parsed from: `/usr/share/doc/libpng-dev/copyright`, `/usr/share/doc/libpng16-16t64/copyright`)

- `Apache-2.0`
- `BSD-3-clause`
- `BSD-like-with-advertising-clause`
- `GPL-2`
- `GPL-2+`
- `expat`
- `libpng`
- `libpng OR Apache-2.0 OR BSD-3-clause`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/libpng1.6/1.6.46-4/


### `dpkg` source package: `libpsl=0.21.2-1.1build1`

Binary Packages:

- `libpsl-dev:amd64=0.21.2-1.1build1`
- `libpsl5t64:amd64=0.21.2-1.1build1`

Licenses: (parsed from: `/usr/share/doc/libpsl-dev/copyright`, `/usr/share/doc/libpsl5t64/copyright`)

- `Chromium`
- `MIT`
- `gnulib`

Source:

```console
$ apt-get source -qq --print-uris libpsl=0.21.2-1.1build1
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpsl/libpsl_0.21.2-1.1build1.dsc' libpsl_0.21.2-1.1build1.dsc 2425 SHA512:f6036e1386802ab44ad0d65b81f4e81dd2ac084da738752f058d58f8d96074b2ab7b00e8275cdd73bedb18d5ae6ba1fc4b19fb95d4b61e58df5695225629ef7c
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpsl/libpsl_0.21.2.orig.tar.xz' libpsl_0.21.2.orig.tar.xz 1870352 SHA512:5308feee863b84705246ce303c093e0c9fecd948ab382fd7480e9ea1ca5f72de42fc2c8f70472a97603580a3fd1eb2b552b093d79756e9fe93effba9f25b6aa4
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpsl/libpsl_0.21.2-1.1build1.debian.tar.xz' libpsl_0.21.2-1.1build1.debian.tar.xz 12244 SHA512:316b41dc3611a45c0b7ab0ec7fc617d2c710f8e11d943daefa524fc92155b63e777504a11dbe1b8427e1ad6d15f98095c90cd115df71fb8f90449a461dc9cd3d
```

### `dpkg` source package: `libraw=0.21.3-1`

Binary Packages:

- `libraw23t64:amd64=0.21.3-1`

Licenses: (parsed from: `/usr/share/doc/libraw23t64/copyright`)

- `CC-BY-SA-3.0`
- `CDDL-1.0`
- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libraw=0.21.3-1
'http://archive.ubuntu.com/ubuntu/pool/main/libr/libraw/libraw_0.21.3-1.dsc' libraw_0.21.3-1.dsc 2364 SHA512:858d8729dc171e1a6a8150569ef291fe36ae3f6e1c25e98e1379eaabef8d6226f0d6ba919703de6771f65b70887fd597b0abb98fabff61415ffc7f16964fd584
'http://archive.ubuntu.com/ubuntu/pool/main/libr/libraw/libraw_0.21.3.orig.tar.gz' libraw_0.21.3.orig.tar.gz 566017 SHA512:c88d02685ac8854ca4f718206ceb95b17abffceee6501390d8447f9e8c78864d1dd0aedbdcf97e600244f97e1a50cbfea21d15a2557710c7d175f61915f9fe37
'http://archive.ubuntu.com/ubuntu/pool/main/libr/libraw/libraw_0.21.3-1.debian.tar.xz' libraw_0.21.3-1.debian.tar.xz 24172 SHA512:70fe95890764693998db20f30bd7b4aead86116a93dbdfad00c8dbb610e556a64951faaf0c3e5e0f78831af55c4ecab5a1d049cd764842b80ad3f25a49d83f7d
```

### `dpkg` source package: `librsvg=2.59.2+dfsg-1`

Binary Packages:

- `gir1.2-rsvg-2.0:amd64=2.59.2+dfsg-1`
- `librsvg2-2:amd64=2.59.2+dfsg-1`
- `librsvg2-common:amd64=2.59.2+dfsg-1`
- `librsvg2-dev:amd64=2.59.2+dfsg-1`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/librsvg/2.59.2+dfsg-1/


### `dpkg` source package: `libseccomp=2.5.5-1ubuntu5`

Binary Packages:

- `libseccomp2:amd64=2.5.5-1ubuntu5`

Licenses: (parsed from: `/usr/share/doc/libseccomp2/copyright`)

- `LGPL-2.1`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libselinux=3.7-3ubuntu2`

Binary Packages:

- `libselinux1:amd64=3.7-3ubuntu2`
- `libselinux1-dev:amd64=3.7-3ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libselinux1/copyright`, `/usr/share/doc/libselinux1-dev/copyright`)

- `GPL-2`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libsemanage=3.7-2build1`

Binary Packages:

- `libsemanage-common=3.7-2build1`
- `libsemanage2:amd64=3.7-2build1`

Licenses: (parsed from: `/usr/share/doc/libsemanage-common/copyright`, `/usr/share/doc/libsemanage2/copyright`)

- `GPL-2`
- `LGPL-2.1`
- `LGPL-2.1+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libsepol=3.7-1`

Binary Packages:

- `libsepol-dev:amd64=3.7-1`
- `libsepol2:amd64=3.7-1`

Licenses: (parsed from: `/usr/share/doc/libsepol-dev/copyright`, `/usr/share/doc/libsepol2/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris libsepol=3.7-1
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsepol/libsepol_3.7-1.dsc' libsepol_3.7-1.dsc 2085 SHA512:f6739a13677ec7575fa3a84c3877780c23fbdc65a1a4d1d4a5d9657438fc6b66ddb59390271837d04266c02e087a862ea6ab49cb302596fc95abd7c931a0a467
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsepol/libsepol_3.7.orig.tar.gz' libsepol_3.7.orig.tar.gz 511487 SHA512:85d12d0ba5a7a3225f08d041a18fd59641608db5e0a78a1e9649754e45be54a807cd422d4889b88da6e806b4af546336c7a0913448f08ac33dc6ffb983890ef8
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsepol/libsepol_3.7-1.debian.tar.xz' libsepol_3.7-1.debian.tar.xz 27632 SHA512:9809b3b82c0f816c7fb9b2ec2eb5be8ced95d2d774aebb0834c6848621d0b337ef2950d98602b75e1619db08fb90e4e59e5a0025dfa1a782222addc9535318d5
```

### `dpkg` source package: `libsm=2:1.2.4-1`

Binary Packages:

- `libsm-dev:amd64=2:1.2.4-1`
- `libsm6:amd64=2:1.2.4-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libsm=2:1.2.4-1
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsm/libsm_1.2.4-1.dsc' libsm_1.2.4-1.dsc 2328 SHA512:57cef70d0e1d0d3c9c54e2cd262100726c4c84b3d346236358e8a4de75dc4dfeda3b57d9e61b0751ef8f4541b7ced8c630acefbcab0200ccb62c67a35b6f8173
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsm/libsm_1.2.4.orig.tar.gz' libsm_1.2.4.orig.tar.gz 454517 SHA512:10c38e5aa30dd95c269b063f2ebba4452c53d23e5e2b8a62d9426e22c6b7b290af698a9b7aa6e0e72758f079dd3c371a3af34894ead7d2f340f5348a8d353bc2
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsm/libsm_1.2.4.orig.tar.gz.asc' libsm_1.2.4.orig.tar.gz.asc 801 SHA512:920b0ecd662aa64defce8f97f9755fb98bef38d9d895b34a3cd7ca625175a36cba56780768c8b715906fa8b92181ed408461bcf7ea0a5afbdb8f31a7e21c2b1e
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsm/libsm_1.2.4-1.diff.gz' libsm_1.2.4-1.diff.gz 13196 SHA512:7215911072fb777fc61d7fa5f4d07b6142a302062cf67a7ad4992436c5d9205180d48f623a6f70e80b6e6a86cad8ed2ad79d4798843aa2efdfe6dbf5469cba58
```

### `dpkg` source package: `libssh2=1.11.1-1`

Binary Packages:

- `libssh2-1-dev:amd64=1.11.1-1`
- `libssh2-1t64:amd64=1.11.1-1`

Licenses: (parsed from: `/usr/share/doc/libssh2-1-dev/copyright`, `/usr/share/doc/libssh2-1t64/copyright`)

- `BSD3`
- `ISC`

Source:

```console
$ apt-get source -qq --print-uris libssh2=1.11.1-1
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libssh2/libssh2_1.11.1-1.dsc' libssh2_1.11.1-1.dsc 2319 SHA512:e59c2d3bd93ca324d3876089fdaff21964e6c16a5cbcd523159fa15107d2dee3c700ba70794ed7062970fd513f8067dff1df3d50fcf1e0a780acebc9c5727ed1
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libssh2/libssh2_1.11.1.orig.tar.gz' libssh2_1.11.1.orig.tar.gz 1093012 SHA512:8703636fc28f0b12c8171712f3d605e0466a5bb9ba06e136c3203548fc3408ab07defd71dc801d7009a337e1e02fd60e8933a2a526d5ef0ce53153058d201233
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libssh2/libssh2_1.11.1.orig.tar.gz.asc' libssh2_1.11.1.orig.tar.gz.asc 488 SHA512:83e600ddd676013932297c4f3d2cf2e65b5308f7700d818b34f30d760c7495180e6d8dae70579c8bea95ea2d7ccb12fc42641e545e11ec4b6630a0e6b350b282
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libssh2/libssh2_1.11.1-1.debian.tar.xz' libssh2_1.11.1-1.debian.tar.xz 17136 SHA512:3ba3f52dc0ec7dee76952662e8628a56ef764b7b47405d311cc88ccc0484273e61452024902bfc4e32e5ce86fe041480c55c507dbafd060544e14c3acc10bebb
```

### `dpkg` source package: `libtasn1-6=4.19.0-3build1`

Binary Packages:

- `libtasn1-6:amd64=4.19.0-3build1`
- `libtasn1-6-dev:amd64=4.19.0-3build1`

Licenses: (parsed from: `/usr/share/doc/libtasn1-6/copyright`, `/usr/share/doc/libtasn1-6-dev/copyright`)

- `GFDL-1.3`
- `GPL-3`
- `LGPL`
- `LGPL-2.1`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libtext-charwidth-perl=0.04-11build4`

Binary Packages:

- `libtext-charwidth-perl:amd64=0.04-11build4`

Licenses: (parsed from: `/usr/share/doc/libtext-charwidth-perl/copyright`)

- `Artistic`
- `GPL-1+`

Source:

```console
$ apt-get source -qq --print-uris libtext-charwidth-perl=0.04-11build4
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtext-charwidth-perl/libtext-charwidth-perl_0.04-11build4.dsc' libtext-charwidth-perl_0.04-11build4.dsc 2265 SHA512:0fe85b9e64a3837989d81ace4214eb550cb80d6a7895f572c8e043021bca9f44cc43c32965ed66bf018dbb034aa0cc7ac2800e9782a9b64ce4c3589e1db1ac9f
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtext-charwidth-perl/libtext-charwidth-perl_0.04.orig.tar.bz2' libtext-charwidth-perl_0.04.orig.tar.bz2 8327 SHA512:37e47e23557a14fac3d1471017a2a9b637fa2c8a0b11d3feedfa40a2f2fdf48dbb7f1d9d855f5e56733e3da09436fd7e73360b105aa24194f31aabd8e87dddb4
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtext-charwidth-perl/libtext-charwidth-perl_0.04-11build4.debian.tar.xz' libtext-charwidth-perl_0.04-11build4.debian.tar.xz 3228 SHA512:cc89f58b8bc90cada87a10519f99aa344436eaa631b2fe5f09b817c9df8bf1ee761c35096d88329b9e4c52b8fd091ac68bbac258d86d4bd0a0a653f7b39b52ef
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
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtext-wrapi18n-perl/libtext-wrapi18n-perl_0.06-10.dsc' libtext-wrapi18n-perl_0.06-10.dsc 1829 SHA512:77c1d3d64cd6e31939367f8a5d5d8d5d1b0c4d3a9b2fd8edaf834b687ba9f212b6f33bfd708bb5983a51c7eb2f8e9058a26e3416526d681e6a9d87006399aa60
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtext-wrapi18n-perl/libtext-wrapi18n-perl_0.06.orig.tar.gz' libtext-wrapi18n-perl_0.06.orig.tar.gz 3797 SHA512:08b26bae38eea906ced417f88b494862e5485fe8d8ddf8bc69582b57d3d427393ba6bec9320e79541ccd7d63b20c6c7e5194ccd649cf79ef7caf9892c757ad96
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtext-wrapi18n-perl/libtext-wrapi18n-perl_0.06-10.debian.tar.xz' libtext-wrapi18n-perl_0.06-10.debian.tar.xz 3452 SHA512:490da004cdfe1b1ff967deef2846de80e8868b8aa0faef501097509c5d0bf8c814defb3d760be9ffae782e8fe3f4a5640ddfe222e59ab733aec4bc3b9d15ced7
```

### `dpkg` source package: `libthai=0.1.29-2build1`

Binary Packages:

- `libthai-data=0.1.29-2build1`
- `libthai-dev:amd64=0.1.29-2build1`
- `libthai0:amd64=0.1.29-2build1`

Licenses: (parsed from: `/usr/share/doc/libthai-data/copyright`, `/usr/share/doc/libthai-dev/copyright`, `/usr/share/doc/libthai0/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris libthai=0.1.29-2build1
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libthai/libthai_0.1.29-2build1.dsc' libthai_0.1.29-2build1.dsc 2451 SHA512:63a4a7a95532beb3aed3d7311b7f341689b89b0ff87e112a02a03448408a14464c4ad3339e16a1fae76fefacb8e72286850494c907d8c49e0c7eb83651d7ab36
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libthai/libthai_0.1.29.orig.tar.xz' libthai_0.1.29.orig.tar.xz 417728 SHA512:0ba1261581a1705a2a2546a3071acb3c63892dbf111f0dad415667165a6b9542a5e4549061c67b11ec53de7c9e70fceb3c04d794fd12a22d991a539dbacebda1
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libthai/libthai_0.1.29-2build1.debian.tar.xz' libthai_0.1.29-2build1.debian.tar.xz 12744 SHA512:40ede6bac42730219a2df5db772814ff4185e5464ea33ebde225b8a068bbbb277c5201ba6f0e6f8e57fdf2733925ead1b54a86463073cb79c402fde101774577
```

### `dpkg` source package: `libtool=2.5.4-3build1`

Binary Packages:

- `libltdl-dev:amd64=2.5.4-3build1`
- `libltdl7:amd64=2.5.4-3build1`
- `libtool=2.5.4-3build1`

Licenses: (parsed from: `/usr/share/doc/libltdl-dev/copyright`, `/usr/share/doc/libltdl7/copyright`, `/usr/share/doc/libtool/copyright`)

- `GFDL-1.3`
- `GFDL-NIV-1.3+`
- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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
'http://archive.ubuntu.com/ubuntu/pool/main/libu/libunistring/libunistring_1.3-1.dsc' libunistring_1.3-1.dsc 1578 SHA512:ae608322cf14e0c63923e3afe3c4579e27cd1cd0e759f0bd4952ea6d7139c67d77235bc2e37af22319d5581528b5ddaae18df2296778c6f3d139dcccf003d3c6
'http://archive.ubuntu.com/ubuntu/pool/main/libu/libunistring/libunistring_1.3.orig.tar.xz' libunistring_1.3.orig.tar.xz 2753448 SHA512:864d42b1d4ae4941fe5c8327d6726ab8e3a35d2d5f9d25ce4859a72ab2f549a7b68f58638cf8767d863f58161d1a4053495d185860964a942d6750e42facf931
'http://archive.ubuntu.com/ubuntu/pool/main/libu/libunistring/libunistring_1.3.orig.tar.xz.asc' libunistring_1.3.orig.tar.xz.asc 833 SHA512:829229528acc8f9d13de4c43fea6caddacaf1f1cc201a7927b2c140d7ac5a81e213a1a20ba67766d6867fbe301ddddf78685f5af54e67906160807d6e8028b5a
'http://archive.ubuntu.com/ubuntu/pool/main/libu/libunistring/libunistring_1.3-1.debian.tar.xz' libunistring_1.3-1.debian.tar.xz 28376 SHA512:9a9af7fb85038a76176004113b534ae557b465e51b8c9cb883cd8c56384d38d2dbb9452c89bde5d1475dd668c9225bebd92e3a0bd04e8be6099dd50c38e60f28
```

### `dpkg` source package: `libwebp=1.5.0-0.1`

Binary Packages:

- `libsharpyuv-dev:amd64=1.5.0-0.1`
- `libsharpyuv0:amd64=1.5.0-0.1`
- `libwebp-dev:amd64=1.5.0-0.1`
- `libwebp7:amd64=1.5.0-0.1`
- `libwebpdecoder3:amd64=1.5.0-0.1`
- `libwebpdemux2:amd64=1.5.0-0.1`
- `libwebpmux3:amd64=1.5.0-0.1`

Licenses: (parsed from: `/usr/share/doc/libsharpyuv-dev/copyright`, `/usr/share/doc/libsharpyuv0/copyright`, `/usr/share/doc/libwebp-dev/copyright`, `/usr/share/doc/libwebp7/copyright`, `/usr/share/doc/libwebpdecoder3/copyright`, `/usr/share/doc/libwebpdemux2/copyright`, `/usr/share/doc/libwebpmux3/copyright`)

- `Apache-2.0`
- `BSD-3-Clause`

Source:

```console
$ apt-get source -qq --print-uris libwebp=1.5.0-0.1
'http://archive.ubuntu.com/ubuntu/pool/main/libw/libwebp/libwebp_1.5.0-0.1.dsc' libwebp_1.5.0-0.1.dsc 2865 SHA512:49623160c996f394903114713989e1dcfc79702bfbbb4dd2251b155de86f154d0b2c6f413871fdb6bdb524953887e9814e31db60bead99866e42f5b47ffe3284
'http://archive.ubuntu.com/ubuntu/pool/main/libw/libwebp/libwebp_1.5.0.orig.tar.gz' libwebp_1.5.0.orig.tar.gz 4267494 SHA512:7a39594cf5585428f82d555b05e78aa63758a56841a313c0b74dfb4996afe37dddf92498d6123ff2a949a7209fb9097927f10ee75b5a38b481f110c892e5302b
'http://archive.ubuntu.com/ubuntu/pool/main/libw/libwebp/libwebp_1.5.0.orig.tar.gz.asc' libwebp_1.5.0.orig.tar.gz.asc 833 SHA512:892e6240b767d7b47fc4faa337aa78f1426359e155c94305377510b0a0c8a24830597b261ebb458f6310338afde487616bd6cca3347b624d8f46500487a3c067
'http://archive.ubuntu.com/ubuntu/pool/main/libw/libwebp/libwebp_1.5.0-0.1.debian.tar.xz' libwebp_1.5.0-0.1.debian.tar.xz 11284 SHA512:6f0fd21ea400ecfb4668d6d427a4ab8c50b68bcf6372c3bc7281f385a742c05bbae0062105039016501bf2fab7bfdd9a277ef1dde44ade2625b7cd2122a25d00
```

### `dpkg` source package: `libwmf=0.2.13-1.1build3`

Binary Packages:

- `libwmf-0.2-7:amd64=0.2.13-1.1build3`
- `libwmf-dev=0.2.13-1.1build3`
- `libwmflite-0.2-7:amd64=0.2.13-1.1build3`

Licenses: (parsed from: `/usr/share/doc/libwmf-0.2-7/copyright`, `/usr/share/doc/libwmf-dev/copyright`, `/usr/share/doc/libwmflite-0.2-7/copyright`)

- `AGPL-3 with Font exception`
- `GD`
- `ISC`
- `LGPL-2`
- `LGPL-2+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris libwmf=0.2.13-1.1build3
'http://archive.ubuntu.com/ubuntu/pool/main/libw/libwmf/libwmf_0.2.13-1.1build3.dsc' libwmf_0.2.13-1.1build3.dsc 2635 SHA512:c14c4480ca692ed9652cb54f75bac5ddbb79dc9a4fc2c3661ee6d52979e1f5d6fe454c5df1a418838383fb1eff3fcf4b151f770d156cbd3fed5a01d557f09bc7
'http://archive.ubuntu.com/ubuntu/pool/main/libw/libwmf/libwmf_0.2.13.orig.tar.gz' libwmf_0.2.13.orig.tar.gz 3044235 SHA512:f45a936c9bc98fc1a5f2b0808b497119e4dcd3c132615fdddb7583e5719c7d1d7f85c16ebf313cad453e5b7ae3508bf6b80c4ed2b42322b7dec295d8f4eb86ce
'http://archive.ubuntu.com/ubuntu/pool/main/libw/libwmf/libwmf_0.2.13-1.1build3.debian.tar.xz' libwmf_0.2.13-1.1build3.debian.tar.xz 25912 SHA512:0a2a4aeef81c7644eeebaa5ed800c26107472244667814477b153b0597c7fc9c8f2684e6e3a2bc4f3607e84adbcfa09c88116795eb21146b5fa792f0e87372be
```

### `dpkg` source package: `libx11=2:1.8.10-2`

Binary Packages:

- `libx11-6:amd64=2:1.8.10-2`
- `libx11-data=2:1.8.10-2`
- `libx11-dev:amd64=2:1.8.10-2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libx11=2:1.8.10-2
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libx11/libx11_1.8.10-2.dsc' libx11_1.8.10-2.dsc 2519 SHA512:2ce8cb348ccea3507deb6070f339a5d5113d41da2fb139ac9d40cdd2bbd76b46cd8e27cdf3c18ee9871ad737554a8971edef3b33e596afb1a21178ad596be21d
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libx11/libx11_1.8.10.orig.tar.gz' libx11_1.8.10.orig.tar.gz 3192536 SHA512:02427e04827707d69e96ebdbb2aaefa99c56d0b37f308548e01b81afbf3aa573f75226beaebdeb2076b3097060c0d5fcdd0d451205727dc29685c91eb6ecacbc
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libx11/libx11_1.8.10.orig.tar.gz.asc' libx11_1.8.10.orig.tar.gz.asc 833 SHA512:b411b317178e847633cd6e750923ac3d7320490a905121eefe486b73f31f7c0c17223652ee5123934c876588db541c29cc452111af25faa7ede5d102d38d75f2
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libx11/libx11_1.8.10-2.diff.gz' libx11_1.8.10-2.diff.gz 74852 SHA512:b7222ad84fa7cc2405d7275a94d5d01ef632cf0d2585e544c5fa2fa3589779e8ca663af542a9d180106b676efca18c19043366231bded31a68cf839fc5cde4ec
```

### `dpkg` source package: `libxau=1:1.0.11-1`

Binary Packages:

- `libxau-dev:amd64=1:1.0.11-1`
- `libxau6:amd64=1:1.0.11-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxau=1:1.0.11-1
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxau/libxau_1.0.11-1.dsc' libxau_1.0.11-1.dsc 2213 SHA512:4f74b4c0047a848495cf4f85ad17f8ca4c98213f10838ee1d4e17a07dff6a6837e00254595dcec48c720ac74d43437d0a4c56c12debe79139f78d300f90690e2
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxau/libxau_1.0.11.orig.tar.gz' libxau_1.0.11.orig.tar.gz 404973 SHA512:315625ae6657e817c09c83da53029488bd5140bc1048eef1072b12958457fdec6c41f79b190cf10885559d2e4c7d47110cd08369b438ca47749790c51edd8492
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxau/libxau_1.0.11.orig.tar.gz.asc' libxau_1.0.11.orig.tar.gz.asc 358 SHA512:97e4425f90e720800cf91f45cf3dcb92b88017cba0db6fa4e39978ad8871b7312a048f4b51622176488edfb5b620ba0d6f0ffd087f0b177f9abfe3d8854fab30
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxau/libxau_1.0.11-1.diff.gz' libxau_1.0.11-1.diff.gz 22671 SHA512:af623ee3c274d0e5aaaee788d61b09ac8695fc79a119e8e06a9f327db1629bd9ae154ff23c8a748836d0b4f014427353419fd506c7e4d1fd9037e291dfa5162d
```

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
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxcb/libxcb_1.17.0-2.dsc' libxcb_1.17.0-2.dsc 5318 SHA512:5a54b2c0274d7914ca5d11eac94a3547d30e4428ddcdd78c8c8efb3ec2b206f1b26b7b66c2925c758fe426efd4960a017cffefbd5c51ac0a3f9e966d150b973b
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxcb/libxcb_1.17.0.orig.tar.gz' libxcb_1.17.0.orig.tar.gz 661593 SHA512:58624a33d39371a7ff58368ed5a09c1c31bea3abd040173db1d41018de4208bc52d2fb8cfd7382ff34d01b98d01a3e314a71a808533880564cd51cd96624a7bb
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxcb/libxcb_1.17.0-2.diff.gz' libxcb_1.17.0-2.diff.gz 28069 SHA512:60ca4c10826b430b7c43bc2de504b1e6d09d152b7a41325437f5017ce39093d78c72b70189162c814b888701686fa12c2de8d3489a4ffe5b9703cd001bb817b8
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
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxcrypt/libxcrypt_4.4.38-1.dsc' libxcrypt_4.4.38-1.dsc 1573 SHA512:b5eb8267ac958ceec61885d333358a326893e998c0e4c4b1f6ca03d96830fc2e95c627995ef6b96578bd69d0f2f408aa30e168b6a9bb34348ad08368f71b1b6d
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxcrypt/libxcrypt_4.4.38.orig.tar.xz' libxcrypt_4.4.38.orig.tar.xz 394216 SHA512:4310a38e7cb8c337f52ea4ed47561ea548583426276f5ec1f6a52f9435e0508b8c81427947e69e7dc77dee6187fe0c16d1e90d261d857d52d0e58e737230dce4
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxcrypt/libxcrypt_4.4.38-1.debian.tar.xz' libxcrypt_4.4.38-1.debian.tar.xz 8512 SHA512:502912be5e86f84cdd66cae37fa615e2a151ed0ecc3ba904e1365be8230000aaefa20cdd60e27abeadb1960cc041fe05573cb153bb264a032e10db25ca937ad7
```

### `dpkg` source package: `libxdmcp=1:1.1.3-0ubuntu6`

Binary Packages:

- `libxdmcp-dev:amd64=1:1.1.3-0ubuntu6`
- `libxdmcp6:amd64=1:1.1.3-0ubuntu6`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libxext=2:1.3.4-1build2`

Binary Packages:

- `libxext-dev:amd64=2:1.3.4-1build2`
- `libxext6:amd64=2:1.3.4-1build2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxext=2:1.3.4-1build2
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxext/libxext_1.3.4-1build2.dsc' libxext_1.3.4-1build2.dsc 2250 SHA512:6b9b001f4dd81843f12ca625bb90a8ea78dda531f80d6fc9c90c071b6cc925d94c53b2d20abc42d21df77904ff5ba059025ce426cf25838918040da71b1a6ea4
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxext/libxext_1.3.4.orig.tar.gz' libxext_1.3.4.orig.tar.gz 494434 SHA512:4eebd639fd57cb9b84a1e17e368f82fbf3d9f021eef5ad3fe31dd128500db57862a82c1e0d214d447cb7641b2be3fd7e949ee1196f2a482793c6628fb1e5cd70
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxext/libxext_1.3.4-1build2.diff.gz' libxext_1.3.4-1build2.diff.gz 12720 SHA512:6ec71960a93504538ef944620b0af7bb2ffdf21270ddaf1715dec4faf79d0d1ec1372a148e9acb64a014b2a761eadf01f0b83955dda7ff2fdf942b5998bd1b34
```

### `dpkg` source package: `libxml2=2.12.7+dfsg+really2.9.14-0.2ubuntu3`

Binary Packages:

- `libxml2:amd64=2.12.7+dfsg+really2.9.14-0.2ubuntu3`
- `libxml2-dev:amd64=2.12.7+dfsg+really2.9.14-0.2ubuntu3`

Licenses: (parsed from: `/usr/share/doc/libxml2/copyright`, `/usr/share/doc/libxml2-dev/copyright`)

- `ISC`
- `MIT-1`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libxrender=1:0.9.10-1.1build1`

Binary Packages:

- `libxrender-dev:amd64=1:0.9.10-1.1build1`
- `libxrender1:amd64=1:0.9.10-1.1build1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxrender=1:0.9.10-1.1build1
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxrender/libxrender_0.9.10-1.1build1.dsc' libxrender_0.9.10-1.1build1.dsc 2204 SHA512:ac21ce52dc62e66c8e0e6c94c727a978b8b285755dd7c3de9b8bd34057bdef1ee23acdfbdd3efb2052734b763904c02e98cd71b4b0bb28a1673a6da3eb7cb8f6
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxrender/libxrender_0.9.10.orig.tar.gz' libxrender_0.9.10.orig.tar.gz 373717 SHA512:7768e62b500f468460f88f27bc1130170b204b478573d9e4406867e557b5638b7c1e21d88d51f9e774ce2344780a384e3c3be51421275d2ee880f9a978a3a232
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxrender/libxrender_0.9.10-1.1build1.diff.gz' libxrender_0.9.10-1.1build1.diff.gz 15274 SHA512:dca2b6bf90a6ce1ec30376a001f6f24f2d95e917c3a4890242022bf5eefa20c9c1e775c66c229cbb7ee47482650b9a0a750e7bf1890aec89d3bec6b692f4174a
```

### `dpkg` source package: `libxslt=1.1.39-0exp1ubuntu2`

Binary Packages:

- `libxslt1-dev:amd64=1.1.39-0exp1ubuntu2`
- `libxslt1.1:amd64=1.1.39-0exp1ubuntu2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxslt=1.1.39-0exp1ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxslt/libxslt_1.1.39-0exp1ubuntu2.dsc' libxslt_1.1.39-0exp1ubuntu2.dsc 2275 SHA512:8b73748d477f876f32ed31ea8a401cc2b554cb770ed3f20b2f74e6109c13bac4085209cd55d3a8aa0b21f325cd139af7f07a00b0914fb5ef70068f37a5912eda
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxslt/libxslt_1.1.39.orig.tar.xz' libxslt_1.1.39.orig.tar.xz 1578216 SHA512:c0c99dc63f8b2acb6cc3ad7ad684ffa2a427ee8d1740495cbf8a7c9b9c8679f96351b4b676c73ccc191014db4cb4ab42b9a0070f6295565f39dbc665c5c16f89
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxslt/libxslt_1.1.39-0exp1ubuntu2.debian.tar.xz' libxslt_1.1.39-0exp1ubuntu2.debian.tar.xz 21976 SHA512:a76a516c8a77e353fe17691890f40959ab11ccdfca2429ea8939aa6c08b825ce099496f8fa6ee189429794d2f75b54f990d4490103f353bd6f7eaae3cd23f959
```

### `dpkg` source package: `libxt=1:1.2.1-1.2build1`

Binary Packages:

- `libxt-dev:amd64=1:1.2.1-1.2build1`
- `libxt6t64:amd64=1:1.2.1-1.2build1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxt=1:1.2.1-1.2build1
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxt/libxt_1.2.1-1.2build1.dsc' libxt_1.2.1-1.2build1.dsc 2488 SHA512:ebe5d28a22400920f1ce994c3977affdb7da2033a8a6fe0d8b460b90d9eb37de4053843c9e6cc0addd0e712928870eae79d7bdbed0690577701f6d1bca400265
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxt/libxt_1.2.1.orig.tar.gz' libxt_1.2.1.orig.tar.gz 1024473 SHA512:73c2fd8a6590ab5ee93cf646e4f41fb71d424961ecbf9bc13c68abdf539c63ab0c59a4d3b22195ba21859523f4cf0e937648424532794a1350a5891061096503
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxt/libxt_1.2.1.orig.tar.gz.asc' libxt_1.2.1.orig.tar.gz.asc 358 SHA512:135e01b8a79beac9530087dee1a5458c359b4f1ae8346e2502f72f4fc24be400477fda90944315c585e3416e80cb74d1a140d5dfec81e854a4996199a8b221dc
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxt/libxt_1.2.1-1.2build1.diff.gz' libxt_1.2.1-1.2build1.diff.gz 45676 SHA512:e16fcaaba4f0574d31b7418b2a364a09eb9cee3008c4022a09ebd606ee2eecdcbb49c8e1562f1479b1eda5bdea977b3777c384848c21c437793a6a76cc007467
```

### `dpkg` source package: `libyaml=0.2.5-2`

Binary Packages:

- `libyaml-0-2:amd64=0.2.5-2`
- `libyaml-dev:amd64=0.2.5-2`

Licenses: (parsed from: `/usr/share/doc/libyaml-0-2/copyright`, `/usr/share/doc/libyaml-dev/copyright`)

- `Expat`
- `permissive`

Source:

```console
$ apt-get source -qq --print-uris libyaml=0.2.5-2
'http://archive.ubuntu.com/ubuntu/pool/main/liby/libyaml/libyaml_0.2.5-2.dsc' libyaml_0.2.5-2.dsc 2040 SHA512:34deabe0c6392cf1b036444fa734e2cedbcad1ce5be222a224c0a9db447f15b46fed7a22fb452af6a56e3d554457091d1b05c0738b35cee397888b463f634ca2
'http://archive.ubuntu.com/ubuntu/pool/main/liby/libyaml/libyaml_0.2.5.orig.tar.gz' libyaml_0.2.5.orig.tar.gz 85055 SHA512:a0f01e3fc616b65b18a4aa17692ee8ea1a84dc6387d1cf02ac7ef7ab7f46b9744c2aac0a047ff69d6c2da1d2a2d7b355c877da0db57e34d95cd4f37213ab6e7e
'http://archive.ubuntu.com/ubuntu/pool/main/liby/libyaml/libyaml_0.2.5-2.debian.tar.xz' libyaml_0.2.5-2.debian.tar.xz 5656 SHA512:975520b12a66fe8b5fda961efb7219e9f64581190c8be9831d75e1d958e99c459056a925114cdebec9c2373e7c89e53cf2561fc412ae9ac3aaf4a453aa7042ad
```

### `dpkg` source package: `libzstd=1.5.6+dfsg-2`

Binary Packages:

- `libzstd-dev:amd64=1.5.6+dfsg-2`
- `libzstd1:amd64=1.5.6+dfsg-2`

Licenses: (parsed from: `/usr/share/doc/libzstd-dev/copyright`, `/usr/share/doc/libzstd1/copyright`)

- `BSD-3-clause`
- `Expat`
- `GPL-2`
- `zlib`

Source:

```console
$ apt-get source -qq --print-uris libzstd=1.5.6+dfsg-2
'http://archive.ubuntu.com/ubuntu/pool/main/libz/libzstd/libzstd_1.5.6%2bdfsg-2.dsc' libzstd_1.5.6+dfsg-2.dsc 2369 SHA512:28574f72ec7ca9d3d309ae09db9652327564c1544ea2ae669297ca873e654a9a3065802e646768382b3af8846f836219aa8dc25e1c450f23656746ef362b7cd7
'http://archive.ubuntu.com/ubuntu/pool/main/libz/libzstd/libzstd_1.5.6%2bdfsg.orig.tar.xz' libzstd_1.5.6+dfsg.orig.tar.xz 1815380 SHA512:487f37a3cf2a14c57606f0593d43bde00265f59093edf61f10c3c3190676bd7d9fe81d67dc3ef3c925b9e3d6a9ad5ea9e49590a28253965e93b0e72c43acd9c7
'http://archive.ubuntu.com/ubuntu/pool/main/libz/libzstd/libzstd_1.5.6%2bdfsg-2.debian.tar.xz' libzstd_1.5.6+dfsg-2.debian.tar.xz 23088 SHA512:8b15a4c7a921237bc80558775e072c30f4e813b93b03f021c24ea2a81e30220975e9692e19d2589cbe244dec14337ef9c7615977f4b1e515d1b39de30cd7bb70
```

### `dpkg` source package: `linux=6.12.0-15.15`

Binary Packages:

- `linux-libc-dev:amd64=6.12.0-15.15`

Licenses: (parsed from: `/usr/share/doc/linux-libc-dev/copyright`)

- `GPL-2`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `lto-disabled-list=54`

Binary Packages:

- `lto-disabled-list=54`

Licenses: (parsed from: `/usr/share/doc/lto-disabled-list/copyright`)

- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `lz4=1.9.4-3`

Binary Packages:

- `liblz4-1:amd64=1.9.4-3`

Licenses: (parsed from: `/usr/share/doc/liblz4-1/copyright`)

- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/lz4/1.9.4-3/


### `dpkg` source package: `lzo2=2.10-3`

Binary Packages:

- `liblzo2-2:amd64=2.10-3`

Licenses: (parsed from: `/usr/share/doc/liblzo2-2/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris lzo2=2.10-3
'http://archive.ubuntu.com/ubuntu/pool/main/l/lzo2/lzo2_2.10-3.dsc' lzo2_2.10-3.dsc 1923 SHA512:fde8fa4920e2128fb34f7543e72a10adc8bb7467d33db7ba0edc0707b225c436df69e8e5b9e6a470f7ad73b15f203d1162d172f85806059b6b510bb5f59b8ad8
'http://archive.ubuntu.com/ubuntu/pool/main/l/lzo2/lzo2_2.10.orig.tar.gz' lzo2_2.10.orig.tar.gz 600622 SHA512:a3dae5e4a6b93b1f5bf7435e8ab114a9be57252e9efc5dd444947d7a2d031b0819f34bcaeb35f60b5629a01b1238d738735a64db8f672be9690d3c80094511a4
'http://archive.ubuntu.com/ubuntu/pool/main/l/lzo2/lzo2_2.10-3.debian.tar.xz' lzo2_2.10-3.debian.tar.xz 7228 SHA512:11a28d17b6167f2abcf5d9f3c8ce688ea7e74b81e775b0ac62233432747294ead7f6f856d8f2f13ba3694b86444a865b7e10883efe0423098be0d2a08e121f4f
```

### `dpkg` source package: `m4=1.4.19-5`

Binary Packages:

- `m4=1.4.19-5`

Licenses: (parsed from: `/usr/share/doc/m4/copyright`)

- `GFDL`
- `GPL`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/m4/1.4.19-5/


### `dpkg` source package: `make-dfsg=4.4.1-1`

Binary Packages:

- `make=4.4.1-1`

Licenses: (parsed from: `/usr/share/doc/make/copyright`)

- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris make-dfsg=4.4.1-1
'http://archive.ubuntu.com/ubuntu/pool/main/m/make-dfsg/make-dfsg_4.4.1-1.dsc' make-dfsg_4.4.1-1.dsc 1976 SHA512:55cb1a6826ee7ac7225c19a70a253da3abcbad022142eb74ea11071fb3567032221ebd8415dd778c1b0b67ef5572af906d795679818ca448dd995da41e4635b1
'http://archive.ubuntu.com/ubuntu/pool/main/m/make-dfsg/make-dfsg_4.4.1.orig.tar.xz' make-dfsg_4.4.1.orig.tar.xz 1125180 SHA512:7efa533e7c85e0f394d2a9c422c1cf854f304871f0c692ff74eac18597fa53d1a79b41ba1c56b88d8c79f2e6dfb8c3c3ba8640af15756f455167d62e7ed7b04c
'http://archive.ubuntu.com/ubuntu/pool/main/m/make-dfsg/make-dfsg_4.4.1-1.debian.tar.xz' make-dfsg_4.4.1-1.debian.tar.xz 44572 SHA512:e0be68fb774ccb04fa5bf07c690fe26d951bffdef21bc5088416d4134a80aa0f80e9e2cdee25b80ac2c1788b6d1df9cf2177ba02d439a3c34592675902374942
```

### `dpkg` source package: `mawk=1.3.4.20240905-1`

Binary Packages:

- `mawk=1.3.4.20240905-1`

Licenses: (parsed from: `/usr/share/doc/mawk/copyright`)

- `CC-BY-3.0`
- `GPL-2`
- `GPL-2.0-only`
- `X11`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/mawk/1.3.4.20240905-1/


### `dpkg` source package: `media-types=10.1.0`

Binary Packages:

- `media-types=10.1.0`

Licenses: (parsed from: `/usr/share/doc/media-types/copyright`)

- `ad-hoc`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/media-types/10.1.0/


### `dpkg` source package: `mercurial=6.9.1-2`

Binary Packages:

- `mercurial=6.9.1-2`
- `mercurial-common=6.9.1-2`

Licenses: (parsed from: `/usr/share/doc/mercurial/copyright`, `/usr/share/doc/mercurial-common/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/mercurial/6.9.1-2/


### `dpkg` source package: `mpclib3=1.3.1-1build2`

Binary Packages:

- `libmpc3:amd64=1.3.1-1build2`

Licenses: (parsed from: `/usr/share/doc/libmpc3/copyright`)

- `LGPL-3`

Source:

```console
$ apt-get source -qq --print-uris mpclib3=1.3.1-1build2
'http://archive.ubuntu.com/ubuntu/pool/main/m/mpclib3/mpclib3_1.3.1-1build2.dsc' mpclib3_1.3.1-1build2.dsc 1955 SHA512:0db012f9a6b64579eb2b40419184495e975f985b33b286410ba061ccca30581d1af1b9a6de0b6c258df8763103bfc58c9acfef89220df403c365d2626edecc46
'http://archive.ubuntu.com/ubuntu/pool/main/m/mpclib3/mpclib3_1.3.1.orig.tar.gz' mpclib3_1.3.1.orig.tar.gz 773573 SHA512:4bab4ef6076f8c5dfdc99d810b51108ced61ea2942ba0c1c932d624360a5473df20d32b300fc76f2ba4aa2a97e1f275c9fd494a1ba9f07c4cb2ad7ceaeb1ae97
'http://archive.ubuntu.com/ubuntu/pool/main/m/mpclib3/mpclib3_1.3.1-1build2.debian.tar.xz' mpclib3_1.3.1-1build2.debian.tar.xz 4824 SHA512:60e8bb220559964234c5c844ae684d7a1a1dadd23bff6c977f40bfa6f83e137055339b483c11182588a166aee55feb3c260075a0eeedf3df5f0e951694da945f
```

### `dpkg` source package: `mpfr4=4.2.1-1build2`

Binary Packages:

- `libmpfr6:amd64=4.2.1-1build2`

Licenses: (parsed from: `/usr/share/doc/libmpfr6/copyright`)

- `GFDL-1.2`
- `LGPL-3`

Source:

```console
$ apt-get source -qq --print-uris mpfr4=4.2.1-1build2
'http://archive.ubuntu.com/ubuntu/pool/main/m/mpfr4/mpfr4_4.2.1-1build2.dsc' mpfr4_4.2.1-1build2.dsc 2037 SHA512:31ec6ede37f6dbd315d965ff3a51fa6e228e91c76cb337b77963f3ec15e6b8ee69e3034858977bf21a6b2696579fd56e81f9d16a07caec7052cf0738be5ba6dd
'http://archive.ubuntu.com/ubuntu/pool/main/m/mpfr4/mpfr4_4.2.1.orig.tar.xz' mpfr4_4.2.1.orig.tar.xz 1493608 SHA512:bc68c0d755d5446403644833ecbb07e37360beca45f474297b5d5c40926df1efc3e2067eecffdf253f946288bcca39ca89b0613f545d46a9e767d1d4cf358475
'http://archive.ubuntu.com/ubuntu/pool/main/m/mpfr4/mpfr4_4.2.1-1build2.debian.tar.xz' mpfr4_4.2.1-1build2.debian.tar.xz 12748 SHA512:2e4e2edb471230785fee71b9cfeea9d1cb16736dfab7d3d62874ea251f763aa9f9500da24cdff0906070d90ddcec084ed9753784797c49727fadc6f8605934f2
```

### `dpkg` source package: `mysql-8.4=8.4.4-0ubuntu1`

Binary Packages:

- `libmysqlclient-dev=8.4.4-0ubuntu1`
- `libmysqlclient24:amd64=8.4.4-0ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libmysqlclient-dev/copyright`, `/usr/share/doc/libmysqlclient24/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `Boost-1.0`
- `GPL-2`
- `GPL-2+`
- `ISC`
- `LGPL`
- `LGPL-2`
- `public-domain`
- `zlib/libpng`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `mysql-defaults=1.1.1`

Binary Packages:

- `default-libmysqlclient-dev:amd64=1.1.1`
- `mysql-common=5.8+1.1.1`

Licenses: (parsed from: `/usr/share/doc/default-libmysqlclient-dev/copyright`, `/usr/share/doc/mysql-common/copyright`)

- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/mysql-defaults/1.1.1/


### `dpkg` source package: `ncurses=6.5+20250125-2`

Binary Packages:

- `libncurses-dev:amd64=6.5+20250125-2`
- `libncurses6:amd64=6.5+20250125-2`
- `libncursesw6:amd64=6.5+20250125-2`
- `libtinfo6:amd64=6.5+20250125-2`
- `ncurses-base=6.5+20250125-2`
- `ncurses-bin=6.5+20250125-2`

Licenses: (parsed from: `/usr/share/doc/libncurses-dev/copyright`, `/usr/share/doc/libncurses6/copyright`, `/usr/share/doc/libncursesw6/copyright`, `/usr/share/doc/libtinfo6/copyright`, `/usr/share/doc/ncurses-base/copyright`, `/usr/share/doc/ncurses-bin/copyright`)

- `BSD-3-clause`
- `MIT/X11`
- `X11`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/ncurses/6.5+20250125-2/


### `dpkg` source package: `netbase=6.4`

Binary Packages:

- `netbase=6.4`

Licenses: (parsed from: `/usr/share/doc/netbase/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris netbase=6.4
'http://archive.ubuntu.com/ubuntu/pool/main/n/netbase/netbase_6.4.dsc' netbase_6.4.dsc 898 SHA512:243ea79c8566581ff6137d0525195c0c9ceea2234cf74eb28aef5f6791ba35003e91bc063ce508c7be3038c05cf081db1d8f717d193f78554b7aa4a215d7c9ef
'http://archive.ubuntu.com/ubuntu/pool/main/n/netbase/netbase_6.4.tar.xz' netbase_6.4.tar.xz 32712 SHA512:cbc588e5fbef5e3e2c8a2dc49214237e8340bf3fae66973237d1714f67c039d4b8d6886581d92b45a004fa23ff016ad8c82cb15b6f752d1ffa23e3284fe0b80a
```

### `dpkg` source package: `nettle=3.10-1`

Binary Packages:

- `libhogweed6t64:amd64=3.10-1`
- `libnettle8t64:amd64=3.10-1`
- `nettle-dev:amd64=3.10-1`

Licenses: (parsed from: `/usr/share/doc/libhogweed6t64/copyright`, `/usr/share/doc/libnettle8t64/copyright`, `/usr/share/doc/nettle-dev/copyright`)

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
- `libnghttp2-dev:amd64=1.64.0-1`

Licenses: (parsed from: `/usr/share/doc/libnghttp2-14/copyright`, `/usr/share/doc/libnghttp2-dev/copyright`)

- `BSD-2-clause`
- `Expat`
- `GPL-3`
- `GPL-3+ with autoconf exception`
- `MIT`
- `all-permissive`

Source:

```console
$ apt-get source -qq --print-uris nghttp2=1.64.0-1
'http://archive.ubuntu.com/ubuntu/pool/main/n/nghttp2/nghttp2_1.64.0-1.dsc' nghttp2_1.64.0-1.dsc 2531 SHA512:621a42dd262564c1c64b59a1498719af1ccdb7ff35e54147e03664e1adfc9035533f412884876979e8c6ac44285acd726fea1ff9becedced216c73b68158547c
'http://archive.ubuntu.com/ubuntu/pool/main/n/nghttp2/nghttp2_1.64.0.orig.tar.gz' nghttp2_1.64.0.orig.tar.gz 1069782 SHA512:35f8230a0fa2825f0bc400d4852d8e8b484f659c67b00639ccd074a0029088f016e967db2f62b6b64af1f8ef684f5809a833e7f922e38b9405f7cc7756bcfb75
'http://archive.ubuntu.com/ubuntu/pool/main/n/nghttp2/nghttp2_1.64.0-1.debian.tar.xz' nghttp2_1.64.0-1.debian.tar.xz 38888 SHA512:a74da2e22238b95cd041c51be80b1afe85e563277ccdb47b3b5e63ce119b6ace669d4287b170a7c838dd84b73b57918d986d8128e8fc5e3626f0d0d1c3c6c0c8
```

### `dpkg` source package: `npth=1.8-1`

Binary Packages:

- `libnpth0t64:amd64=1.8-1`

Licenses: (parsed from: `/usr/share/doc/libnpth0t64/copyright`)

- `LGPL-2.1`
- `LGPL-2.1+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/npth/1.8-1/


### `dpkg` source package: `openexr=3.1.5-5.1build3`

Binary Packages:

- `libopenexr-3-1-30:amd64=3.1.5-5.1build3`
- `libopenexr-dev=3.1.5-5.1build3`

Licenses: (parsed from: `/usr/share/doc/libopenexr-3-1-30/copyright`, `/usr/share/doc/libopenexr-dev/copyright`)

- `BSD-3-clause`
- `openexr`

Source:

```console
$ apt-get source -qq --print-uris openexr=3.1.5-5.1build3
'http://archive.ubuntu.com/ubuntu/pool/universe/o/openexr/openexr_3.1.5-5.1build3.dsc' openexr_3.1.5-5.1build3.dsc 2629 SHA512:6754aafb095ee18dbd5f3df736e9e619af5189e3fb6d61245d64d18aaec9874e23b75daa51b8e55b61c93732163575f85496e1e61baf97de1470939dfe8eae8e
'http://archive.ubuntu.com/ubuntu/pool/universe/o/openexr/openexr_3.1.5.orig.tar.gz' openexr_3.1.5.orig.tar.gz 20327926 SHA512:01ef16eacd2dde83c67b81522bae87f47ba272a41ce7d4e35d865dbdcaa03093e7ac504b95d2c1b3a19535f2364a4f937b0e0570c74243bb1c6e021fce7b620c
'http://archive.ubuntu.com/ubuntu/pool/universe/o/openexr/openexr_3.1.5.orig.tar.gz.asc' openexr_3.1.5.orig.tar.gz.asc 287 SHA512:9b3978e44b531429aba42b9cc4969a470898d9d74652e3809edb0273ba9b127c471aec6570b5d352be738f59810091c0df2c70d39c16d2c32833d173b270f72c
'http://archive.ubuntu.com/ubuntu/pool/universe/o/openexr/openexr_3.1.5-5.1build3.debian.tar.xz' openexr_3.1.5-5.1build3.debian.tar.xz 18952 SHA512:717a1362e1150abf4d555725539bd4b873591646f1c48859c200cb9a7b46946e00824d58ce68cb5dbee4ab3231e77f01cb75624a3eca99f633a4a99ba72e4e09
```

### `dpkg` source package: `openjpeg2=2.5.0-2ubuntu3`

Binary Packages:

- `libopenjp2-7:amd64=2.5.0-2ubuntu3`
- `libopenjp2-7-dev:amd64=2.5.0-2ubuntu3`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `openldap=2.6.9+dfsg-1~exp2ubuntu1`

Binary Packages:

- `libldap-common=2.6.9+dfsg-1~exp2ubuntu1`
- `libldap-dev:amd64=2.6.9+dfsg-1~exp2ubuntu1`
- `libldap2:amd64=2.6.9+dfsg-1~exp2ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libldap-common/copyright`, `/usr/share/doc/libldap-dev/copyright`, `/usr/share/doc/libldap2/copyright`)

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
$ apt-get source -qq --print-uris openldap=2.6.9+dfsg-1~exp2ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/o/openldap/openldap_2.6.9%2bdfsg-1%7eexp2ubuntu1.dsc' openldap_2.6.9+dfsg-1~exp2ubuntu1.dsc 3342 SHA512:ed622ca107393458d44c4edceee660f4c1b2624a7492fa2cb215ea47024fec31e15a6c18223ba9f32d6a49b021a7e8086d26468243677d3344a31f2ed33418aa
'http://archive.ubuntu.com/ubuntu/pool/main/o/openldap/openldap_2.6.9%2bdfsg.orig.tar.xz' openldap_2.6.9+dfsg.orig.tar.xz 3753260 SHA512:0789b8ad8b2ede51741e18e3f090a258edc7abeda90cfadae98b9a22126be901f3640d4121411836608918418108dfb71ae0957dbd251d9c3ce6bd1b854dd799
'http://archive.ubuntu.com/ubuntu/pool/main/o/openldap/openldap_2.6.9%2bdfsg-1%7eexp2ubuntu1.debian.tar.xz' openldap_2.6.9+dfsg-1~exp2ubuntu1.debian.tar.xz 184000 SHA512:d41adc7b1e7758bdbf7cb2632aea24f84766719d88b811fff02b758a3fbc156e10effa4b0b63093aff6836ee6d5cfa4ae89c0b650de009d83c3f9228f11bbc0b
```

### `dpkg` source package: `openssh=1:9.9p1-3ubuntu2`

Binary Packages:

- `openssh-client=1:9.9p1-3ubuntu2`

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


### `dpkg` source package: `openssl=3.4.0-1ubuntu2`

Binary Packages:

- `libssl-dev:amd64=3.4.0-1ubuntu2`
- `libssl3t64:amd64=3.4.0-1ubuntu2`
- `openssl=3.4.0-1ubuntu2`
- `openssl-provider-legacy=3.4.0-1ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libssl-dev/copyright`, `/usr/share/doc/libssl3t64/copyright`, `/usr/share/doc/openssl/copyright`, `/usr/share/doc/openssl-provider-legacy/copyright`)

- `Apache-2.0`
- `Artistic`
- `GPL-1`
- `GPL-1+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `p11-kit=0.25.5-2ubuntu1`

Binary Packages:

- `libp11-kit-dev:amd64=0.25.5-2ubuntu1`
- `libp11-kit0:amd64=0.25.5-2ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libp11-kit-dev/copyright`, `/usr/share/doc/libp11-kit0/copyright`)

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `pam=1.5.3-7ubuntu4`

Binary Packages:

- `libpam-modules:amd64=1.5.3-7ubuntu4`
- `libpam-modules-bin=1.5.3-7ubuntu4`
- `libpam-runtime=1.5.3-7ubuntu4`
- `libpam0g:amd64=1.5.3-7ubuntu4`

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
$ apt-get source -qq --print-uris pam=1.5.3-7ubuntu4
'http://archive.ubuntu.com/ubuntu/pool/main/p/pam/pam_1.5.3-7ubuntu4.dsc' pam_1.5.3-7ubuntu4.dsc 2411 SHA512:ef7b41b13e21d2c2dbf64371956055f042a8d792d84b371489e285e3d46061034715ca5cb41f038b0f83a4046f5020cd7f7f434ee429d5c319d560f9a225b0be
'http://archive.ubuntu.com/ubuntu/pool/main/p/pam/pam_1.5.3.orig.tar.xz' pam_1.5.3.orig.tar.xz 1020076 SHA512:af88e8c1b6a9b737ffaffff7dd9ed8eec996d1fbb5804fb76f590bed66d8a1c2c6024a534d7a7b6d18496b300f3d6571a08874cf406cd2e8cea1d5eff49c136a
'http://archive.ubuntu.com/ubuntu/pool/main/p/pam/pam_1.5.3-7ubuntu4.debian.tar.xz' pam_1.5.3-7ubuntu4.debian.tar.xz 186684 SHA512:252162a6fc1ed9069fa3dcb039c62671f2fdfb705c9b90ee2fae346cb06c4523aeb0f148393cdee56d9b563ca1c110ccb14540e6efc7e9c19aff3efcec76afcb
```

### `dpkg` source package: `pango1.0=1.56.1-1`

Binary Packages:

- `gir1.2-pango-1.0:amd64=1.56.1-1`
- `libpango-1.0-0:amd64=1.56.1-1`
- `libpango1.0-dev:amd64=1.56.1-1`
- `libpangocairo-1.0-0:amd64=1.56.1-1`
- `libpangoft2-1.0-0:amd64=1.56.1-1`
- `libpangoxft-1.0-0:amd64=1.56.1-1`
- `pango1.0-tools=1.56.1-1`

Licenses: (parsed from: `/usr/share/doc/gir1.2-pango-1.0/copyright`, `/usr/share/doc/libpango-1.0-0/copyright`, `/usr/share/doc/libpango1.0-dev/copyright`, `/usr/share/doc/libpangocairo-1.0-0/copyright`, `/usr/share/doc/libpangoft2-1.0-0/copyright`, `/usr/share/doc/libpangoxft-1.0-0/copyright`, `/usr/share/doc/pango1.0-tools/copyright`)

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
'http://archive.ubuntu.com/ubuntu/pool/main/p/pango1.0/pango1.0_1.56.1-1.dsc' pango1.0_1.56.1-1.dsc 3690 SHA512:48f2e9e65ed9d9d1e2e091cab8893a15dd89ee65237a1662c9430fd33b0db644251e31457e6d1eb962053f5d75d32ea038aa52c0bb781102ff4316d0c7463abe
'http://archive.ubuntu.com/ubuntu/pool/main/p/pango1.0/pango1.0_1.56.1.orig.tar.xz' pango1.0_1.56.1.orig.tar.xz 1882616 SHA512:ce893f2f09922d3b8e862376d71465cd9eba45ac5de6b32681f3d3c226edb24b0949c705bb3f75a0c2eada46c524226c5b830b70719e6a95dfe374ce20f92011
'http://archive.ubuntu.com/ubuntu/pool/main/p/pango1.0/pango1.0_1.56.1-1.debian.tar.xz' pango1.0_1.56.1-1.debian.tar.xz 43776 SHA512:904d1ee24a6a71cb944ef4df9897da476c9d3ee8823549cd29f47350b9a90ff99f22439eff002083d67b6f52ab19c99dcafc7ceff48a17d50441a8b1e7c9c0c2
```

### `dpkg` source package: `patch=2.7.6-7build3`

Binary Packages:

- `patch=2.7.6-7build3`

Licenses: (parsed from: `/usr/share/doc/patch/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris patch=2.7.6-7build3
'http://archive.ubuntu.com/ubuntu/pool/main/p/patch/patch_2.7.6-7build3.dsc' patch_2.7.6-7build3.dsc 1838 SHA512:205ad1e6f47a5c039c878387f95ee3a91e2115ccd740f6d2e6ce0b7d9996bad38332739418e3cb70d215f93a083c3fc5174269893f5d3e200caf18ef0d8e1f05
'http://archive.ubuntu.com/ubuntu/pool/main/p/patch/patch_2.7.6.orig.tar.xz' patch_2.7.6.orig.tar.xz 783756 SHA512:fcca87bdb67a88685a8a25597f9e015f5e60197b9a269fa350ae35a7991ed8da553939b4bbc7f7d3cfd863c67142af403b04165633acbce4339056a905e87fbd
'http://archive.ubuntu.com/ubuntu/pool/main/p/patch/patch_2.7.6-7build3.debian.tar.xz' patch_2.7.6-7build3.debian.tar.xz 15324 SHA512:46d2d3d5da88ddf723891df3288165405794cf414c6fdad65723a0f7333e918676a04eaa254d2dbc7b682e4e214d6089af461b490c51a5c8e7e02d4743b4249f
```

### `dpkg` source package: `pcre2=10.42-4ubuntu3`

Binary Packages:

- `libpcre2-16-0:amd64=10.42-4ubuntu3`
- `libpcre2-32-0:amd64=10.42-4ubuntu3`
- `libpcre2-8-0:amd64=10.42-4ubuntu3`
- `libpcre2-dev:amd64=10.42-4ubuntu3`
- `libpcre2-posix3:amd64=10.42-4ubuntu3`

Licenses: (parsed from: `/usr/share/doc/libpcre2-16-0/copyright`, `/usr/share/doc/libpcre2-32-0/copyright`, `/usr/share/doc/libpcre2-8-0/copyright`, `/usr/share/doc/libpcre2-dev/copyright`, `/usr/share/doc/libpcre2-posix3/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `BSD-3-clause-Cambridge with BINARY LIBRARY-LIKE PACKAGES exception`
- `X11`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/perl/5.40.0-8/


### `dpkg` source package: `pinentry=1.3.1-2ubuntu2`

Binary Packages:

- `pinentry-curses=1.3.1-2ubuntu2`

Licenses: (parsed from: `/usr/share/doc/pinentry-curses/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-3`
- `LGPL-3+`
- `X11`

Source:

```console
$ apt-get source -qq --print-uris pinentry=1.3.1-2ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/p/pinentry/pinentry_1.3.1-2ubuntu2.dsc' pinentry_1.3.1-2ubuntu2.dsc 3384 SHA512:d2a156287cc70cfdc32ce61e277f34be136b8897f7d8b5e35939740f4e6b8f561d2445a7f0e4f293bf1749738a2ee1282d534fe11db9f11cac989c91edad3cb9
'http://archive.ubuntu.com/ubuntu/pool/main/p/pinentry/pinentry_1.3.1.orig.tar.bz2' pinentry_1.3.1.orig.tar.bz2 611233 SHA512:3b72034dc1792b1475acb6d605ff7c1bd7647a0f02d1b6bdcd475acdef24bc802f49e275055436c3271261c4b7a64168477a698aab812a145962146b2f67a0e2
'http://archive.ubuntu.com/ubuntu/pool/main/p/pinentry/pinentry_1.3.1.orig.tar.bz2.asc' pinentry_1.3.1.orig.tar.bz2.asc 390 SHA512:499926442059c8f349b66beb16b6cf22cf0919b65a601af1bd0d60c96f60d44e0ad2bd090324585da5cb09e75286e11a4b92c553aec43b87f6cbe8a1e599882c
'http://archive.ubuntu.com/ubuntu/pool/main/p/pinentry/pinentry_1.3.1-2ubuntu2.debian.tar.xz' pinentry_1.3.1-2ubuntu2.debian.tar.xz 23928 SHA512:186b9c3d672f395a7edf52329b30db2df8354a795888539ecbb4f0085fd57b5e283eda3c61633892ad9f115f1145a2f1e64914f6c236efed1beac3816a6b5954
```

### `dpkg` source package: `pixman=0.44.0-3`

Binary Packages:

- `libpixman-1-0:amd64=0.44.0-3`
- `libpixman-1-dev:amd64=0.44.0-3`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris pixman=0.44.0-3
'http://archive.ubuntu.com/ubuntu/pool/main/p/pixman/pixman_0.44.0-3.dsc' pixman_0.44.0-3.dsc 2019 SHA512:f9d02a262d9b471f479a8744cf4051320a6a610d512e69ec3607ef7ce79c36e3e8ecb4b510293b06875d5a31d5e8d0584cbd985068fb5905bf6ca5bbd560accc
'http://archive.ubuntu.com/ubuntu/pool/main/p/pixman/pixman_0.44.0.orig.tar.gz' pixman_0.44.0.orig.tar.gz 812995 SHA512:ded90b36587d449ce38610e615b4c5c02cddab614f96ecf46f560cf994bd93fb418b8d33b86c9ace310774f47044cfd37499e7593bfc3af58b11bacebe53c16c
'http://archive.ubuntu.com/ubuntu/pool/main/p/pixman/pixman_0.44.0-3.diff.gz' pixman_0.44.0-3.diff.gz 9417 SHA512:c9e3feb0d572dff8b2ae0a00654b0d0c56c1cb56c7b8c7675da038ad1f67c8a99c65276343bedb758a7bb4478d12cac90d0c4e8e70b6ce65e0a722c01408d606
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
'http://archive.ubuntu.com/ubuntu/pool/main/p/pkgconf/pkgconf_1.8.1-4.dsc' pkgconf_1.8.1-4.dsc 2130 SHA512:62975c1188d23cfe211a26d6e42ec580681f400fd11b7db070e2dba93a4e3927ae5492ca79de79d6325ca1342b66368ed2fe10c216927f01f8533f6de3c515dc
'http://archive.ubuntu.com/ubuntu/pool/main/p/pkgconf/pkgconf_1.8.1.orig.tar.xz' pkgconf_1.8.1.orig.tar.xz 302372 SHA512:7a7d5204c1c9bfb6578bda56f299d1fa0300e69a133a65730b10ad77aefbf26fceb74ae77cecda326b3ed5db5736f27fcce94764b3a56d40f4bb99fecdc80bba
'http://archive.ubuntu.com/ubuntu/pool/main/p/pkgconf/pkgconf_1.8.1-4.debian.tar.xz' pkgconf_1.8.1-4.debian.tar.xz 17736 SHA512:b1ab8b6a0dd98f07f7a882d43af6e7dedcc30ef3cc8d0958d9327c3531e02710fdaa3c6ae294498ea39ecc1a38a3f2a8036d2e6aed55936eaf5f3c82abf6a7d8
```

### `dpkg` source package: `postgresql-17=17.2-1build2`

Binary Packages:

- `libpq-dev=17.2-1build2`
- `libpq5:amd64=17.2-1build2`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `procps=2:4.0.4-4ubuntu5`

Binary Packages:

- `libproc2-0:amd64=2:4.0.4-4ubuntu5`
- `procps=2:4.0.4-4ubuntu5`

Licenses: (parsed from: `/usr/share/doc/libproc2-0/copyright`, `/usr/share/doc/procps/copyright`)

- `GPL-2`
- `GPL-2.0+`
- `LGPL-2`
- `LGPL-2.0+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris procps=2:4.0.4-4ubuntu5
'http://archive.ubuntu.com/ubuntu/pool/main/p/procps/procps_4.0.4-4ubuntu5.dsc' procps_4.0.4-4ubuntu5.dsc 2243 SHA512:aabf9b2b44668b0483484795b459643992c534339531c0e58d714c77ec10bfa3ebc3207ce80510dfc5922720c079f3d153d4393a4f46f1a2cf0ead23c5b15365
'http://archive.ubuntu.com/ubuntu/pool/main/p/procps/procps_4.0.4.orig.tar.xz' procps_4.0.4.orig.tar.xz 1401540 SHA512:94375544e2422fefc23d7634063c49ef1be62394c46039444f85e6d2e87e45cfadc33accba5ca43c96897b4295bfb0f88d55a30204598ddb26ef66f0420cefb4
'http://archive.ubuntu.com/ubuntu/pool/main/p/procps/procps_4.0.4-4ubuntu5.debian.tar.xz' procps_4.0.4-4ubuntu5.debian.tar.xz 38800 SHA512:3326242b1ebfd6060abe1f1411d32219839c8b73a3c23ffa55419aa3319f8e657288fc0cdbd1248b362c042e8668c8eaa2003dec2343b32c30bbff9506b8f759
```

### `dpkg` source package: `python-packaging=24.2-1`

Binary Packages:

- `python3-packaging=24.2-1`

Licenses: (parsed from: `/usr/share/doc/python3-packaging/copyright`)

- `Apache-2.0`
- `BSD-3-clause`

Source:

```console
$ apt-get source -qq --print-uris python-packaging=24.2-1
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-packaging/python-packaging_24.2-1.dsc' python-packaging_24.2-1.dsc 1911 SHA512:465d8cc14de47d6c78c43ca6566d59a10fd0f8dba19b75f00abde3bed36285de2c793bd154b3ea914c310d7bd7b5341c178e4ae26f1e50cfbe8e11e23b868f61
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-packaging/python-packaging_24.2.orig.tar.gz' python-packaging_24.2.orig.tar.gz 163950 SHA512:4d79d9c49c59255e9eb12cb1452ff9ee413a6a6f34a23c487d3d5712ddabe067f8c6dafe0c8111517682634deac2fd5db1346e3c0cc9f432eba94491aa459553
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-packaging/python-packaging_24.2-1.debian.tar.xz' python-packaging_24.2-1.debian.tar.xz 2964 SHA512:cfd50682d966887ca48a956f8f33c06677c71858b45cf199db3c77861465f3085fce75959e9d7b3b83e106712c8f3dbe5f1cbbb5f4ac5c484b3271d82d39cec3
```

### `dpkg` source package: `python3-defaults=3.13.1-1~exp2`

Binary Packages:

- `libpython3-stdlib:amd64=3.13.1-1~exp2`
- `python3=3.13.1-1~exp2`
- `python3-minimal=3.13.1-1~exp2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/python3-defaults/3.13.1-1~exp2/


### `dpkg` source package: `python3.13=3.13.2-1`

Binary Packages:

- `libpython3.13-minimal:amd64=3.13.2-1`
- `libpython3.13-stdlib:amd64=3.13.2-1`
- `python3.13=3.13.2-1`
- `python3.13-minimal=3.13.2-1`

Licenses: (parsed from: `/usr/share/doc/libpython3.13-minimal/copyright`, `/usr/share/doc/libpython3.13-stdlib/copyright`, `/usr/share/doc/python3.13/copyright`, `/usr/share/doc/python3.13-minimal/copyright`)

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
$ apt-get source -qq --print-uris python3.13=3.13.2-1
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3.13/python3.13_3.13.2-1.dsc' python3.13_3.13.2-1.dsc 3639 SHA512:be1258919d5935dd7a6fb15bb936e3658ce2cb834da55ad8971fd48fd113ef2a3655fa2f01ba8f557da2a2d5cd66cf9cf808af9ee4eb9c5bc90750ac1ee46f63
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3.13/python3.13_3.13.2.orig.tar.xz' python3.13_3.13.2.orig.tar.xz 22621108 SHA512:bb1c0598914c6d4326554faa568f660f10b20c701d0f36bf1fa58837b6498d728a407416b06ede39604caea1ca93f60545b83b01ae8ee65f55d4cc83242b63fe
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3.13/python3.13_3.13.2.orig.tar.xz.asc' python3.13_3.13.2.orig.tar.xz.asc 963 SHA512:5f019be530f688b0adf5d5cc9f2c2243e2f1dc7338559db14c1eedd12aadc85404d42c7aafd74e41828205d85f13f278876662ac30c8f3382a1ee081ba5f29f2
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3.13/python3.13_3.13.2-1.debian.tar.xz' python3.13_3.13.2-1.debian.tar.xz 260180 SHA512:549371e62227f644d117596521baa693c30aeb65b87818213ed28bea292acce1487e1b38d4cab320ad8086690a7cec687ff04726b3b2290ca6ce5ef1365b981d
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
'http://archive.ubuntu.com/ubuntu/pool/main/r/readline/readline_8.2-6.dsc' readline_8.2-6.dsc 2810 SHA512:b748d32b4dcb87a209cdecf6d28f5e799761577b787d8a116fb59dc73f2aa421d64687fd5f5359f5d46e8915676720b83685d8eb70e9d2840d8bf26a068d9e34
'http://archive.ubuntu.com/ubuntu/pool/main/r/readline/readline_8.2.orig.tar.gz' readline_8.2.orig.tar.gz 3043952 SHA512:0a451d459146bfdeecc9cdd94bda6a6416d3e93abd80885a40b334312f16eb890f8618a27ca26868cebbddf1224983e631b1cbc002c1a4d1cd0d65fba9fea49a
'http://archive.ubuntu.com/ubuntu/pool/main/r/readline/readline_8.2-6.debian.tar.xz' readline_8.2-6.debian.tar.xz 38396 SHA512:6e8f28dd4b3f7e579f97235d31dd19d5a452edb61af247652ffa4c5fd70de23d34581da71e8bba66beb69aa63311ce27177c27e55972cceb6ae886369faa2217
```

### `dpkg` source package: `rpcsvc-proto=1.4.2-0ubuntu7`

Binary Packages:

- `rpcsvc-proto=1.4.2-0ubuntu7`

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
$ apt-get source -qq --print-uris rpcsvc-proto=1.4.2-0ubuntu7
'http://archive.ubuntu.com/ubuntu/pool/main/r/rpcsvc-proto/rpcsvc-proto_1.4.2-0ubuntu7.dsc' rpcsvc-proto_1.4.2-0ubuntu7.dsc 2113 SHA512:898f925a91776d16b8f6934b502f0a05983079af42a633245d2f5e25975daf3eece0be7a999dc640739b0c29315a657d33c1d5e5ed03e74ab5b911638571a96c
'http://archive.ubuntu.com/ubuntu/pool/main/r/rpcsvc-proto/rpcsvc-proto_1.4.2.orig.tar.xz' rpcsvc-proto_1.4.2.orig.tar.xz 171620 SHA512:631fbfc00af94c5d7def0759f27e97dc14d400b4468c906719ae18ecef74815730798c882d1aaa4f90359224e7b829019b786baddc3097905b54f940ca85a714
'http://archive.ubuntu.com/ubuntu/pool/main/r/rpcsvc-proto/rpcsvc-proto_1.4.2-0ubuntu7.debian.tar.xz' rpcsvc-proto_1.4.2-0ubuntu7.debian.tar.xz 4336 SHA512:faf9f6eb4e7da5e4fed0e358e836cc4137f783079127cbabe3bed82f8ad2d08250d827d62f0f49df23604d685b7c55d6c30b8ec69dff0f14e3267ae180cb9f96
```

### `dpkg` source package: `rtmpdump=2.4+20151223.gitfa8646d.1-2build7`

Binary Packages:

- `librtmp-dev:amd64=2.4+20151223.gitfa8646d.1-2build7`
- `librtmp1:amd64=2.4+20151223.gitfa8646d.1-2build7`

Licenses: (parsed from: `/usr/share/doc/librtmp-dev/copyright`, `/usr/share/doc/librtmp1/copyright`)

- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris rtmpdump=2.4+20151223.gitfa8646d.1-2build7
'http://archive.ubuntu.com/ubuntu/pool/main/r/rtmpdump/rtmpdump_2.4%2b20151223.gitfa8646d.1-2build7.dsc' rtmpdump_2.4+20151223.gitfa8646d.1-2build7.dsc 2439 SHA512:5e2fb3986c0f0e2150c6054e0428adbf1719bb0c33f92ae4acb74a11e625d731ede0262f0d8887c769a95a61f3cd4d23d44bf2f375f0153eba6c0f25b68719c5
'http://archive.ubuntu.com/ubuntu/pool/main/r/rtmpdump/rtmpdump_2.4%2b20151223.gitfa8646d.1.orig.tar.gz' rtmpdump_2.4+20151223.gitfa8646d.1.orig.tar.gz 142213 SHA512:bdfcbab73179d614a295a7b136ea4c9d0ce4620883b493f298362784d245608cd6ad4b0ad30f94ed73a086b4555399521ae9e95b6375fce75e455ae68c055e7b
'http://archive.ubuntu.com/ubuntu/pool/main/r/rtmpdump/rtmpdump_2.4%2b20151223.gitfa8646d.1-2build7.debian.tar.xz' rtmpdump_2.4+20151223.gitfa8646d.1-2build7.debian.tar.xz 8464 SHA512:812edf4f933ad0f723404192bfbfceca86e58303169a30e3b1f47781b709b91a259621293533d31d7abd16bc522824e2db325426a4ce9a6b428b88d492ae4c6c
```

### `dpkg` source package: `rust-sequoia-sq=1.2.0-1`

Binary Packages:

- `sq=1.2.0-1`

Licenses: (parsed from: `/usr/share/doc/sq/copyright`)

- `GPL-2`
- `GPL-2.0-or-later`
- `LGPL-2`
- `LGPL-2.0-or-later`

Source:

```console
$ apt-get source -qq --print-uris rust-sequoia-sq=1.2.0-1
'http://archive.ubuntu.com/ubuntu/pool/universe/r/rust-sequoia-sq/rust-sequoia-sq_1.2.0-1.dsc' rust-sequoia-sq_1.2.0-1.dsc 4179 SHA512:be1f78bf2e854537bb99b1d26451c9985689e1b48f3a187450a20174a9aea29c1fff2bf02871ab8fe765e105a8d3a4a0e8c87dfdd8f536d71d13870b51294ab3
'http://archive.ubuntu.com/ubuntu/pool/universe/r/rust-sequoia-sq/rust-sequoia-sq_1.2.0.orig.tar.gz' rust-sequoia-sq_1.2.0.orig.tar.gz 750156 SHA512:7971ff890872249b5c85724e1dfc3de69769d6a52d5ecf9112679ce225560a8bf9c7e401887cf09e3138873a65fc83c1af65dac7fb89196aecf6009ed626ff4e
'http://archive.ubuntu.com/ubuntu/pool/universe/r/rust-sequoia-sq/rust-sequoia-sq_1.2.0-1.debian.tar.xz' rust-sequoia-sq_1.2.0-1.debian.tar.xz 5476 SHA512:4e5c6d910924fac384ac08ff2c08406fc05b59bd337aa69c1389922f80f491dd0b673cfedf06282eaa047ee143de3e605f565b25e242fc4ede483922dd2b1212
```

### `dpkg` source package: `sed=4.9-2build1`

Binary Packages:

- `sed=4.9-2build1`

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
$ apt-get source -qq --print-uris sed=4.9-2build1
'http://archive.ubuntu.com/ubuntu/pool/main/s/sed/sed_4.9-2build1.dsc' sed_4.9-2build1.dsc 1992 SHA512:c1fb23ca19645e3c77d7d466818b0ff15ec2fefa423d03c60746d3c441a767af9a551c0af022a5c17e69e58589b8004bc6e127dbb63d806c6269ba0ee2c1e8fd
'http://archive.ubuntu.com/ubuntu/pool/main/s/sed/sed_4.9.orig.tar.xz' sed_4.9.orig.tar.xz 1397092 SHA512:36157a4b4a2430cf421b7bd07f1675d680d9f1616be96cf6ad6ee74a9ec0fe695f8d0b1e1f0b008bbb33cc7fcde5e1c456359bbbc63f8aebdd4fedc3982cf6dc
'http://archive.ubuntu.com/ubuntu/pool/main/s/sed/sed_4.9-2build1.debian.tar.xz' sed_4.9-2build1.debian.tar.xz 62896 SHA512:e9e57380873aa800f7892d99dbebb362a2ba9f27cc984180753d306592d6ca572d0baa3c4faf4b10dbc2aa33985e759f668f1efb4e0b09e4ae2ae689e32969ad
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
'http://archive.ubuntu.com/ubuntu/pool/main/s/sensible-utils/sensible-utils_0.0.24.dsc' sensible-utils_0.0.24.dsc 1743 SHA512:7f5abddecd7ca44b37c278dbd1ba9515667cfea27fb4819e8b2187da199871855c53ba5115979484ec5f5ac0767c5ef054788d0082e10b597d502c8a620d1ff5
'http://archive.ubuntu.com/ubuntu/pool/main/s/sensible-utils/sensible-utils_0.0.24.tar.xz' sensible-utils_0.0.24.tar.xz 73568 SHA512:2db2b14bb4b8e616d0e22ac39c56e4e995ba565da59f624ea5ce8958d3eaf545d69136a518e30bd7183adde411607465d7d07fa8e88cc0d980b5d464f8a3b902
```

### `dpkg` source package: `serf=1.3.10-3ubuntu1`

Binary Packages:

- `libserf-1-1:amd64=1.3.10-3ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libserf-1-1/copyright`)

- `Apache`
- `Apache-2.0`
- `Zlib`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `shadow=1:4.16.0-7ubuntu1`

Binary Packages:

- `login.defs=1:4.16.0-7ubuntu1`
- `passwd=1:4.16.0-7ubuntu1`

Licenses: (parsed from: `/usr/share/doc/login.defs/copyright`, `/usr/share/doc/passwd/copyright`)

- `BSD-3-clause`
- `GPL-1`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris shadow=1:4.16.0-7ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/s/shadow/shadow_4.16.0-7ubuntu1.dsc' shadow_4.16.0-7ubuntu1.dsc 2579 SHA512:bf1e673a911f68bad1b56fa82527c19b296ce358f000233ddde5f5db862a55c146d58dccc4836e85712d4fdbdf8ea2b5bafeeceed7aba32b18f4de31b8f175b4
'http://archive.ubuntu.com/ubuntu/pool/main/s/shadow/shadow_4.16.0.orig.tar.xz' shadow_4.16.0.orig.tar.xz 2053720 SHA512:fdb6835b54b6507f853d9dcdbf4c794d8f808638226d6baf32c5b33e1aaef79159d7f957f4d515c9c770c6a735d74eeb70fa83337374bd0689341ee001fbb756
'http://archive.ubuntu.com/ubuntu/pool/main/s/shadow/shadow_4.16.0-7ubuntu1.debian.tar.xz' shadow_4.16.0-7ubuntu1.debian.tar.xz 184116 SHA512:ef799ce47e9d81a751e076297835776ecaeb6c8ffd2b6c6159bd55bbefdd1aade92e47539fc8813be83a6209051d31cb6ee89cd98ff5168dd001cc7227923f28
```

### `dpkg` source package: `shared-mime-info=2.4-5`

Binary Packages:

- `shared-mime-info=2.4-5`

Licenses: (parsed from: `/usr/share/doc/shared-mime-info/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris shared-mime-info=2.4-5
'http://archive.ubuntu.com/ubuntu/pool/main/s/shared-mime-info/shared-mime-info_2.4-5.dsc' shared-mime-info_2.4-5.dsc 2237 SHA512:57108936794b1dbeedec4865416a59ef045fd0c81e1f34f2af965968245cbe0e0e71616a26c4f6fd34f0fd25283fa0935d90e683af11111dac865627e584b714
'http://archive.ubuntu.com/ubuntu/pool/main/s/shared-mime-info/shared-mime-info_2.4.orig.tar.bz2' shared-mime-info_2.4.orig.tar.bz2 7096347 SHA512:712f414e80919bf2a0f5083ced44c54a350948a526850466a6e9f35365dcfd97fad8bcdbb29945de2715a8f9b70a108e931c8500209a4d6e3dddf97af02771cb
'http://archive.ubuntu.com/ubuntu/pool/main/s/shared-mime-info/shared-mime-info_2.4-5.debian.tar.xz' shared-mime-info_2.4-5.debian.tar.xz 10812 SHA512:842d469aec8fc0972357b3c4bb6a3704693c42635df62ab2e1d664e0afe52031e7fc067cff6cbb09a35d7b5c108c07ba301b6974b9589969228199a3945c7428
```

### `dpkg` source package: `sqlite3=3.46.1-1`

Binary Packages:

- `libsqlite3-0:amd64=3.46.1-1`
- `libsqlite3-dev:amd64=3.46.1-1`

Licenses: (parsed from: `/usr/share/doc/libsqlite3-0/copyright`, `/usr/share/doc/libsqlite3-dev/copyright`)

- `GPL-2`
- `GPL-2+`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/sqlite3/3.46.1-1/


### `dpkg` source package: `subversion=1.14.5-2`

Binary Packages:

- `libsvn1:amd64=1.14.5-2`
- `subversion=1.14.5-2`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/subversion/1.14.5-2/


### `dpkg` source package: `sysprof=48~beta-2`

Binary Packages:

- `libsysprof-capture-4-dev:amd64=48~beta-2`

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
$ apt-get source -qq --print-uris sysprof=48~beta-2
'http://archive.ubuntu.com/ubuntu/pool/main/s/sysprof/sysprof_48%7ebeta-2.dsc' sysprof_48~beta-2.dsc 3106 SHA512:a934d0d2562a822192421a6dcf47f2ff51ebfedda47cb468729e8d635610f8813d1c14fa230d5891bb3861ae0e1a36a4bd9f2ef43d663f0e00a05dd434602c2e
'http://archive.ubuntu.com/ubuntu/pool/main/s/sysprof/sysprof_48%7ebeta.orig.tar.xz' sysprof_48~beta.orig.tar.xz 1215220 SHA512:220f836590d74225e50b66a9bdd847ab049895aab8afb9caf963ced3ebf8527148e55cf9a68f1ada1b2596181ffd158fd94507870b2c0bf9ce400b6565e277fa
'http://archive.ubuntu.com/ubuntu/pool/main/s/sysprof/sysprof_48%7ebeta-2.debian.tar.xz' sysprof_48~beta-2.debian.tar.xz 17476 SHA512:00a1f565a346eee278c178c0c8334b940d5289d8a8ee540e8f87495b87f91909ec9d27ecaec1fe16ab71d680cce1756033f49fa6f89af96a3942a3f3fec0a3ee
```

### `dpkg` source package: `systemd=256.5-2ubuntu4`

Binary Packages:

- `libsystemd0:amd64=256.5-2ubuntu4`
- `libudev1:amd64=256.5-2ubuntu4`

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


### `dpkg` source package: `sysvinit=3.08-6ubuntu3`

Binary Packages:

- `sysvinit-utils=3.08-6ubuntu3`

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


### `dpkg` source package: `tar=1.35+dfsg-3build1`

Binary Packages:

- `tar=1.35+dfsg-3build1`

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


### `dpkg` source package: `tiff=4.5.1+git230720-4ubuntu4`

Binary Packages:

- `libtiff-dev:amd64=4.5.1+git230720-4ubuntu4`
- `libtiff6:amd64=4.5.1+git230720-4ubuntu4`
- `libtiffxx6:amd64=4.5.1+git230720-4ubuntu4`

Licenses: (parsed from: `/usr/share/doc/libtiff-dev/copyright`, `/usr/share/doc/libtiff6/copyright`, `/usr/share/doc/libtiffxx6/copyright`)

- `Hylafax`

Source:

```console
$ apt-get source -qq --print-uris tiff=4.5.1+git230720-4ubuntu4
'http://archive.ubuntu.com/ubuntu/pool/main/t/tiff/tiff_4.5.1%2bgit230720-4ubuntu4.dsc' tiff_4.5.1+git230720-4ubuntu4.dsc 2435 SHA512:04aa0fc51de733bf4f6dc468eb8b247352f0968f0c62bd55933b95eb5200b311736d1e765115f329406f76ffb0eba90b4aedb3c67ed912c21ff053d1eebfcadd
'http://archive.ubuntu.com/ubuntu/pool/main/t/tiff/tiff_4.5.1%2bgit230720.orig.tar.xz' tiff_4.5.1+git230720.orig.tar.xz 1781896 SHA512:6bf9653f5c65d17c2944b20d14a5d5ab3b89d461bc6eb935a54aa8df99ce7221aeb2172f06b44affd06d81aeaab5698b90b07fde883167d0abf51debaaa6f71b
'http://archive.ubuntu.com/ubuntu/pool/main/t/tiff/tiff_4.5.1%2bgit230720-4ubuntu4.debian.tar.xz' tiff_4.5.1+git230720-4ubuntu4.debian.tar.xz 29972 SHA512:6e7398bd9108946b8ad5d95b1a6af62408a2f8577c41102e78bb2a483a3e114964745f7b1190a26d8609a2f8f9265dc57170015a68a203785a74af7692090843
```

### `dpkg` source package: `tzdata=2024b-6ubuntu1`

Binary Packages:

- `tzdata=2024b-6ubuntu1`

Licenses: (parsed from: `/usr/share/doc/tzdata/copyright`)

- `ICU`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ubuntu-keyring=2023.11.28.1`

Binary Packages:

- `ubuntu-keyring=2023.11.28.1`

Licenses: (parsed from: `/usr/share/doc/ubuntu-keyring/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris ubuntu-keyring=2023.11.28.1
'http://archive.ubuntu.com/ubuntu/pool/main/u/ubuntu-keyring/ubuntu-keyring_2023.11.28.1.dsc' ubuntu-keyring_2023.11.28.1.dsc 1872 SHA512:4d3c094e1e01367eb8303808ea5bfea696ee672d855a64272c9222400bec397ebbaa57783bbc8eb4365f0631c9951edeb1b12f04efb3e34275408ef57620f023
'http://archive.ubuntu.com/ubuntu/pool/main/u/ubuntu-keyring/ubuntu-keyring_2023.11.28.1.tar.xz' ubuntu-keyring_2023.11.28.1.tar.xz 20236 SHA512:b17824a91d6e25c5658eae8d9ae509a4158b406768d5d4a8e117a230226ab7cd4327cf7e5b9bbb7baae7c66f3807d27926de85a1ea5c11a82684a890aeb8fd18
```

### `dpkg` source package: `ucf=3.0049`

Binary Packages:

- `ucf=3.0049`

Licenses: (parsed from: `/usr/share/doc/ucf/copyright`)

- `GPL-2`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/ucf/3.0049/


### `dpkg` source package: `unbound=1.22.0-1ubuntu1`

Binary Packages:

- `libunbound8:amd64=1.22.0-1ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libunbound8/copyright`)

- `BSD-2-VUT`
- `BSD-3-ADG`
- `BSD-3-CZ.NIC`
- `BSD-3-Farsight`
- `BSD-3-NLnetLabs`
- `BSD-3-NLnetLabs-Mekking`
- `BSD-3-Regents-DEC`
- `BSD-3-Todd-Miller`
- `BSD-3-VUT`
- `BSD-3-Viagénie`
- `BSD-3-WIDE`
- `GPL-3`
- `GPL-3+ with Bison exception`
- `ISC`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris unbound=1.22.0-1ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/u/unbound/unbound_1.22.0-1ubuntu1.dsc' unbound_1.22.0-1ubuntu1.dsc 3037 SHA512:ac17e4565bb349d6cd32a1615b3e2bbd4fb7885ff06e3b26a54ca7626c8361521e42e0a9e2ea6e8a08579e4d90c7f710b1e5473b7db3ac79158b32f5d3551ae8
'http://archive.ubuntu.com/ubuntu/pool/main/u/unbound/unbound_1.22.0.orig.tar.gz' unbound_1.22.0.orig.tar.gz 6682466 SHA512:6c873e19902ce6cd59cec7084d5dba1a5bd5fe4437c827ae69bdf9273bcd8d2d1ec0dc183076f8d2e1fd38730bf8c10852d678399f0b2ea8ccf7e39119568978
'http://archive.ubuntu.com/ubuntu/pool/main/u/unbound/unbound_1.22.0-1ubuntu1.debian.tar.xz' unbound_1.22.0-1ubuntu1.debian.tar.xz 29768 SHA512:fe8d444a4a36a63d0f452b91e77bf50df3ad34cbd78ba19f944215c2d98ff87c3b7c73c1cc111123db9e50065a54476df248ff94a5c98f360ec2c89a9b2a3f8b
```

### `dpkg` source package: `unzip=6.0-28ubuntu6`

Binary Packages:

- `unzip=6.0-28ubuntu6`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris unzip=6.0-28ubuntu6
'http://archive.ubuntu.com/ubuntu/pool/main/u/unzip/unzip_6.0-28ubuntu6.dsc' unzip_6.0-28ubuntu6.dsc 1883 SHA512:ea06f2ade23550e63c60fc72ea78226c53bf75e4fe309f94949e80177130a1a3752c341645c9df2febdd7d75508a3ef12ff6094606b317d061f569c219101dd6
'http://archive.ubuntu.com/ubuntu/pool/main/u/unzip/unzip_6.0.orig.tar.gz' unzip_6.0.orig.tar.gz 1376845 SHA512:0694e403ebc57b37218e00ec1a406cae5cc9c5b52b6798e0d4590840b6cdbf9ddc0d9471f67af783e960f8fa2e620394d51384257dca23d06bcd90224a80ce5d
'http://archive.ubuntu.com/ubuntu/pool/main/u/unzip/unzip_6.0-28ubuntu6.debian.tar.xz' unzip_6.0-28ubuntu6.debian.tar.xz 47148 SHA512:c45fdf158c89a3a8199d41d33e7c960e6689242ad00d48b8cb82815ab5e12384e8e3c5b1b3d6e3d83b37add7dda881cdf9a412b3201b03397322c95fe3d11fd5
```

### `dpkg` source package: `utf8proc=2.9.0-1build1`

Binary Packages:

- `libutf8proc3:amd64=2.9.0-1build1`

Licenses: (parsed from: `/usr/share/doc/libutf8proc3/copyright`)

- `Expat`
- `Unicode`

Source:

```console
$ apt-get source -qq --print-uris utf8proc=2.9.0-1build1
'http://archive.ubuntu.com/ubuntu/pool/universe/u/utf8proc/utf8proc_2.9.0-1build1.dsc' utf8proc_2.9.0-1build1.dsc 2294 SHA512:0a183389b81b1ad614d5a5bf1ace1a2fac8cd91ea7724da25b8443a006c71099cd5ea0d2dc909bfa4a580e816e9e34cc9c4f64a752fef5b0ece510e092690491
'http://archive.ubuntu.com/ubuntu/pool/universe/u/utf8proc/utf8proc_2.9.0.orig.tar.gz' utf8proc_2.9.0.orig.tar.gz 193465 SHA512:544ed59812279af4135e5622e2e77b3f067765df819cf8b78e679dfc481e9baa5a357a33c40426c5053c1d5107109e3c4c191ed83f3f7c4a6b1769d04b17715c
'http://archive.ubuntu.com/ubuntu/pool/universe/u/utf8proc/utf8proc_2.9.0-1build1.debian.tar.xz' utf8proc_2.9.0-1build1.debian.tar.xz 5956 SHA512:66f918055be1f55b39929c504521094860b66518c99f644a2d826a52076416a7e79d0ed6ec260617e47202e4907f69d7489549737d38ff920942c173e0867693
```

### `dpkg` source package: `util-linux=2.40.2-14ubuntu1`

Binary Packages:

- `bsdutils=1:2.40.2-14ubuntu1`
- `libblkid-dev:amd64=2.40.2-14ubuntu1`
- `libblkid1:amd64=2.40.2-14ubuntu1`
- `libmount-dev:amd64=2.40.2-14ubuntu1`
- `libmount1:amd64=2.40.2-14ubuntu1`
- `libsmartcols1:amd64=2.40.2-14ubuntu1`
- `libuuid1:amd64=2.40.2-14ubuntu1`
- `login=1:4.16.0-2+really2.40.2-14ubuntu1`
- `mount=2.40.2-14ubuntu1`
- `util-linux=2.40.2-14ubuntu1`
- `uuid-dev:amd64=2.40.2-14ubuntu1`

Licenses: (parsed from: `/usr/share/doc/bsdutils/copyright`, `/usr/share/doc/libblkid-dev/copyright`, `/usr/share/doc/libblkid1/copyright`, `/usr/share/doc/libmount-dev/copyright`, `/usr/share/doc/libmount1/copyright`, `/usr/share/doc/libsmartcols1/copyright`, `/usr/share/doc/libuuid1/copyright`, `/usr/share/doc/login/copyright`, `/usr/share/doc/mount/copyright`, `/usr/share/doc/util-linux/copyright`, `/usr/share/doc/uuid-dev/copyright`)

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
$ apt-get source -qq --print-uris util-linux=2.40.2-14ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/u/util-linux/util-linux_2.40.2-14ubuntu1.dsc' util-linux_2.40.2-14ubuntu1.dsc 4952 SHA512:970fc46fc8c726d9e4acfd901387173b75fb75fbf514edd44bc9acb631a95b198c89b78d431c13a7c59eb0a59427c858b9961710adf728e37699192ed8e5a3d4
'http://archive.ubuntu.com/ubuntu/pool/main/u/util-linux/util-linux_2.40.2.orig.tar.xz' util-linux_2.40.2.orig.tar.xz 8854820 SHA512:ffe20b915a518a150401d429b0338bc7022190e4ca0ef91a6d9eea345db8c1e11ad01784163b8fcf978506f3f5cad473f29d5d4ef93a4c66a5ae0ebd9fb0c8f2
'http://archive.ubuntu.com/ubuntu/pool/main/u/util-linux/util-linux_2.40.2-14ubuntu1.debian.tar.xz' util-linux_2.40.2-14ubuntu1.debian.tar.xz 126204 SHA512:920ac6f4216777ed0a150da248863ef816cdfbca2d6dd371567af6ad15539d9c3470b9fec051518d7cc2ee0dbd0190e8940eba633ac2ebc2952b2fe4e26ecb72
```

### `dpkg` source package: `wget=1.24.5-2ubuntu1`

Binary Packages:

- `wget=1.24.5-2ubuntu1`

Licenses: (parsed from: `/usr/share/doc/wget/copyright`)

- `GFDL-1.2`
- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris wget=1.24.5-2ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/w/wget/wget_1.24.5-2ubuntu1.dsc' wget_1.24.5-2ubuntu1.dsc 2288 SHA512:024e102f33abee32993adca81bb45f1d4c61a43740e25c6797f4fe491d7941281de2d6920a19693ab36f8ead9dd015a8161d2d80cfcf46d7edb73808490c84b0
'http://archive.ubuntu.com/ubuntu/pool/main/w/wget/wget_1.24.5.orig.tar.gz' wget_1.24.5.orig.tar.gz 5182521 SHA512:572aa54717e51a9eb9959e127c7afb696645088f32ff7df2cfe9d243957e34ee235e98988fa94649df023d2e3d62b6973e8c9f2eb92beba820dd96d5de2a950d
'http://archive.ubuntu.com/ubuntu/pool/main/w/wget/wget_1.24.5.orig.tar.gz.asc' wget_1.24.5.orig.tar.gz.asc 854 SHA512:f819dc43a466682ace38e8537698e3c7c3919203f77373bdaea1b63ead40c4d3663590209dfeb6187d98edd00e30848a3abd5735795fb47878924f1d9b2ee10d
'http://archive.ubuntu.com/ubuntu/pool/main/w/wget/wget_1.24.5-2ubuntu1.debian.tar.xz' wget_1.24.5-2ubuntu1.debian.tar.xz 65252 SHA512:7c3b80db521946b7209697f711ee21db1df2e7af20d046f23ebb3d23e80eaf9aea1b9ea882ed29aa05f76732aafce97168756f64fd1781f04a1958c63b53c85c
```

### `dpkg` source package: `xft=2.3.6-1build1`

Binary Packages:

- `libxft-dev:amd64=2.3.6-1build1`
- `libxft2:amd64=2.3.6-1build1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris xft=2.3.6-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/x/xft/xft_2.3.6-1build1.dsc' xft_2.3.6-1build1.dsc 2138 SHA512:448b5bf2f9d7b9245c70b0f81c82e4bf96f8f7bba4888bce5b7ad4dcaa0a568786b979bf59e2b6cbcf3d71adaba1a310fd4e4fd61ecc737c72fec8880a545cfc
'http://archive.ubuntu.com/ubuntu/pool/main/x/xft/xft_2.3.6.orig.tar.gz' xft_2.3.6.orig.tar.gz 447498 SHA512:291bec2cc297a6e39baff5c2dec37017f37f97b438468a6d6b66f496a9987936da6ee2e3ace77e4527d8c5fd09e1dd731b2f042fa74880f667b8a03a913512d2
'http://archive.ubuntu.com/ubuntu/pool/main/x/xft/xft_2.3.6-1build1.diff.gz' xft_2.3.6-1build1.diff.gz 18138 SHA512:c8566508d00ba5a57436311ccb862e8dbb9701a0f01ed787dec62ed24ca29c9c76835537b2997165e842e07aa22285b9e3183000347e777108e6d4f58d7992e0
```

### `dpkg` source package: `xorg-sgml-doctools=1:1.11-1.1`

Binary Packages:

- `xorg-sgml-doctools=1:1.11-1.1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris xorg-sgml-doctools=1:1.11-1.1
'http://archive.ubuntu.com/ubuntu/pool/main/x/xorg-sgml-doctools/xorg-sgml-doctools_1.11-1.1.dsc' xorg-sgml-doctools_1.11-1.1.dsc 1987 SHA512:1682e1a4d4be1bfb1242adfa22b2764a9425b035cbfae9fd58925d4904eb301fe48bf92fc5935e973d7653db001ab221a8eac8cc5e2840d5a2e0cb4f1bb4895c
'http://archive.ubuntu.com/ubuntu/pool/main/x/xorg-sgml-doctools/xorg-sgml-doctools_1.11.orig.tar.gz' xorg-sgml-doctools_1.11.orig.tar.gz 150367 SHA512:a2386e41a8e2f7deaded61e00eaeab922647c0d0f4e36268c4337dc71d2412b0ec433140d080a0fd118b6112ed0a4f960280f932fe8d4a90ea9dc8bedf1eb75e
'http://archive.ubuntu.com/ubuntu/pool/main/x/xorg-sgml-doctools/xorg-sgml-doctools_1.11-1.1.diff.gz' xorg-sgml-doctools_1.11-1.1.diff.gz 3296 SHA512:0ea09f6de75cf649fb82705a0470e5ba04edbe59ccfa26132e60120e04036b86e9ff47785fdcee2499fa005cbbdfc9e04ebdca619d0253ea558e2fe5501b9ec4
```

### `dpkg` source package: `xorg=1:7.7+23ubuntu3`

Binary Packages:

- `x11-common=1:7.7+23ubuntu3`

Licenses: (parsed from: `/usr/share/doc/x11-common/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris xorg=1:7.7+23ubuntu3
'http://archive.ubuntu.com/ubuntu/pool/main/x/xorg/xorg_7.7%2b23ubuntu3.dsc' xorg_7.7+23ubuntu3.dsc 2095 SHA512:dd0091767574109a7e1308a0222f8e5115529baa9def0d822f9812c1761eb43b03caa440ba80874a9c1470a52911e94e6e03f52dc94cf2339006e6bd9ea372a0
'http://archive.ubuntu.com/ubuntu/pool/main/x/xorg/xorg_7.7%2b23ubuntu3.tar.gz' xorg_7.7+23ubuntu3.tar.gz 301634 SHA512:16e7194bcbbc38f185130de2115817c2a34238a1541bbfff08239b0a84e3a5637d907dc1465556061645c6ff0845c47047231a0b384758162ace93d20db6e4d0
```

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
'http://archive.ubuntu.com/ubuntu/pool/main/x/xorgproto/xorgproto_2024.1-1.dsc' xorgproto_2024.1-1.dsc 3336 SHA512:2e7799b28e6267936afdc2b1926c40326d5bc3040801f57e41fee6ab32ed2d49df8a36c42900604e3f4f19c0d4ae0fbee611cadff3c7da365f0beeea9c331fc1
'http://archive.ubuntu.com/ubuntu/pool/main/x/xorgproto/xorgproto_2024.1.orig.tar.gz' xorgproto_2024.1.orig.tar.gz 1115486 SHA512:c2d67a98c5ba9b2f4d0b844c96dab342c497710753a8878b75dbf12ecd64b105c9ee3c5fd11eb91e45960420cf8dd7d02547072a32d5c53e58e009394fe33666
'http://archive.ubuntu.com/ubuntu/pool/main/x/xorgproto/xorgproto_2024.1.orig.tar.gz.asc' xorgproto_2024.1.orig.tar.gz.asc 195 SHA512:9dc7d40a50178f65b47bcd9a360b85f8d40f30e9151bf242d2eef9a12a3d8e5a1488af7e0c0c4c1dbc3e6cb447acd0735fe749290c46d021b4d7e10de3912a33
'http://archive.ubuntu.com/ubuntu/pool/main/x/xorgproto/xorgproto_2024.1-1.diff.gz' xorgproto_2024.1-1.diff.gz 25061 SHA512:0ba012c2ecad1f6b23d6286c76cfc7f130635e8d30cdb6b2a9a7cb7a0731bb17a5f974d4dcab8efbd104977d95d438295f850c0242d7f46b64a1562891766a08
```

### `dpkg` source package: `xtrans=1.4.0-1`

Binary Packages:

- `xtrans-dev=1.4.0-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris xtrans=1.4.0-1
'http://archive.ubuntu.com/ubuntu/pool/main/x/xtrans/xtrans_1.4.0-1.dsc' xtrans_1.4.0-1.dsc 1919 SHA512:ac171ce0f00e1741e97a4ddad630ccff69070c0ef60047071b3f940fad08cb468d5ded7b2d4f0f500aeda73f2b703d55a7a4bbe0d5fff88cc3381486a111f580
'http://archive.ubuntu.com/ubuntu/pool/main/x/xtrans/xtrans_1.4.0.orig.tar.gz' xtrans_1.4.0.orig.tar.gz 225941 SHA512:21287ccf18fe2ebd458765496b026d175bf47c6e8e5c21d5b9ea17203967efc0cf6928fa2f3385d289a680c7002c3640e4731937029e99933c2a64bb9fab5326
'http://archive.ubuntu.com/ubuntu/pool/main/x/xtrans/xtrans_1.4.0-1.diff.gz' xtrans_1.4.0-1.diff.gz 9522 SHA512:d6deaa9579fb61e6ffd296ffe6b083eb9de572001c0a5bc82229ecc3d50bf2ee2f6504b3daa533bd34f3d647d6bd2235728084ec0b59869f6446652b998797f7
```

### `dpkg` source package: `xxhash=0.8.2-2build1`

Binary Packages:

- `libxxhash0:amd64=0.8.2-2build1`

Licenses: (parsed from: `/usr/share/doc/libxxhash0/copyright`)

- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `xz-utils=5.6.3-1`

Binary Packages:

- `liblzma-dev:amd64=5.6.3-1`
- `liblzma5:amd64=5.6.3-1`
- `xz-utils=5.6.3-1`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/xz-utils/5.6.3-1/


### `dpkg` source package: `zlib=1:1.3.dfsg+really1.3.1-1ubuntu1`

Binary Packages:

- `zlib1g:amd64=1:1.3.dfsg+really1.3.1-1ubuntu1`
- `zlib1g-dev:amd64=1:1.3.dfsg+really1.3.1-1ubuntu1`

Licenses: (parsed from: `/usr/share/doc/zlib1g/copyright`, `/usr/share/doc/zlib1g-dev/copyright`)

- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris zlib=1:1.3.dfsg+really1.3.1-1ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/z/zlib/zlib_1.3.dfsg%2breally1.3.1-1ubuntu1.dsc' zlib_1.3.dfsg+really1.3.1-1ubuntu1.dsc 2993 SHA512:b87b9b973aa22f9cea28d9653bba4383a27203ffb391ff0df537225bbca131eb47b08bc12178bf4d05348e379159be275bddf2d611c97a6bcebd80a0f1ca6e8f
'http://archive.ubuntu.com/ubuntu/pool/main/z/zlib/zlib_1.3.dfsg%2breally1.3.1.orig.tar.gz' zlib_1.3.dfsg+really1.3.1.orig.tar.gz 1325737 SHA512:068cb731e400cfc435db292839737938199d05d77b3010c7b9b87c9d0a127c7545198cea2a620da124ea3dfdde02ab63672aa01fc6cfd1e1ab5a2d6f9ca454c8
'http://archive.ubuntu.com/ubuntu/pool/main/z/zlib/zlib_1.3.dfsg%2breally1.3.1-1ubuntu1.debian.tar.xz' zlib_1.3.dfsg+really1.3.1-1ubuntu1.debian.tar.xz 59676 SHA512:c4d82f270d4334711e26d5d328683d0214d3171a2cfaff0b5b613d4df28adabf01e69ec9f6093991ef8f124f289826f30f2fc64223956462d26c9d67866482fe
```
