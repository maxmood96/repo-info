# `ubuntu:25.04`

## Docker Metadata

- Image ID: `sha256:aaaffc146c5b1e592e4bd51fd789c6f3c3d15c4372662fa5e5d6a4afdf5ba1ef`
- Created: `2024-12-13T03:57:04.336571461Z`
- Virtual Size: ~ 82.14 Mb  
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

### `dpkg` source package: `bzip2=1.0.8-6`

Binary Packages:

- `libbz2-1.0:amd64=1.0.8-6`

Licenses: (parsed from: `/usr/share/doc/libbz2-1.0/copyright`)

- `BSD-variant`
- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris bzip2=1.0.8-6
'http://archive.ubuntu.com/ubuntu/pool/main/b/bzip2/bzip2_1.0.8-6.dsc' bzip2_1.0.8-6.dsc 1604 SHA512:ff346848f80a2d85266e27db27289e126ed016b0ee65f777594e92be388c9f76010419efcbe93dc1d5dde7fe356ee02e797e3579687252b0ae8f4152a245dcb2
'http://archive.ubuntu.com/ubuntu/pool/main/b/bzip2/bzip2_1.0.8.orig.tar.gz' bzip2_1.0.8.orig.tar.gz 810029 SHA512:083f5e675d73f3233c7930ebe20425a533feedeaaa9d8cc86831312a6581cefbe6ed0d08d2fa89be81082f2a5abdabca8b3c080bf97218a1bd59dc118a30b9f3
'http://archive.ubuntu.com/ubuntu/pool/main/b/bzip2/bzip2_1.0.8-6.debian.tar.bz2' bzip2_1.0.8-6.debian.tar.bz2 26991 SHA512:29a0df15aab88f4df3e4b3e13a04a428bae850b251d4b70541896b93fe28bce3397f9a7c5e3b251c81a8abd3e0a7911d31f546c1fe30a28c764ded587462831c
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


### `dpkg` source package: `dpkg=1.22.11ubuntu3`

Binary Packages:

- `dpkg=1.22.11ubuntu3`

Licenses: (parsed from: `/usr/share/doc/dpkg/copyright`)

- `GPL-2`
- `GPL-2+`
- `public-domain-s-s-d`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `e2fsprogs=1.47.1-1ubuntu1`

Binary Packages:

- `e2fsprogs=1.47.1-1ubuntu1`
- `libcom-err2:amd64=1.47.1-1ubuntu1`
- `libext2fs2t64:amd64=1.47.1-1ubuntu1`
- `libss2:amd64=1.47.1-1ubuntu1`
- `logsave=1.47.1-1ubuntu1`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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

### `dpkg` source package: `gcc-14=14.2.0-9ubuntu1`

Binary Packages:

- `gcc-14-base:amd64=14.2.0-9ubuntu1`
- `libgcc-s1:amd64=14.2.0-9ubuntu1`
- `libstdc++6:amd64=14.2.0-9ubuntu1`

Licenses: (parsed from: `/usr/share/doc/gcc-14-base/copyright`, `/usr/share/doc/libgcc-s1/copyright`, `/usr/share/doc/libstdc++6/copyright`)

- `Artistic`
- `GFDL-1.2`
- `GPL`
- `GPL-3`
- `LGPL`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `glibc=2.40-1ubuntu3`

Binary Packages:

- `libc-bin=2.40-1ubuntu3`
- `libc6:amd64=2.40-1ubuntu3`

Licenses: (parsed from: `/usr/share/doc/libc-bin/copyright`, `/usr/share/doc/libc6/copyright`)

- `GFDL-1.3`
- `GPL-2`
- `LGPL-2.1`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `gmp=2:6.3.0+dfsg-2ubuntu7`

Binary Packages:

- `libgmp10:amd64=2:6.3.0+dfsg-2ubuntu7`

Licenses: (parsed from: `/usr/share/doc/libgmp10/copyright`)

- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `GPL-3+ with Bison exception`
- `LGPL-3`
- `LGPL-3+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `gnupg2=2.4.4-2ubuntu21`

Binary Packages:

- `gpgv=2.4.4-2ubuntu21`

Licenses: (parsed from: `/usr/share/doc/gpgv/copyright`)

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `gnutls28=3.8.8-2ubuntu1`

Binary Packages:

- `libgnutls30t64:amd64=3.8.8-2ubuntu1`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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

### `dpkg` source package: `init-system-helpers=1.67ubuntu1`

Binary Packages:

- `init-system-helpers=1.67ubuntu1`

Licenses: (parsed from: `/usr/share/doc/init-system-helpers/copyright`)

- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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


### `dpkg` source package: `libffi=3.4.6-1build1`

Binary Packages:

- `libffi8:amd64=3.4.6-1build1`

Licenses: (parsed from: `/usr/share/doc/libffi8/copyright`)

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


### `dpkg` source package: `libidn2=2.3.7-2build2`

Binary Packages:

- `libidn2-0:amd64=2.3.7-2build2`

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
$ apt-get source -qq --print-uris libidn2=2.3.7-2build2
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libidn2/libidn2_2.3.7-2build2.dsc' libidn2_2.3.7-2build2.dsc 2643 SHA512:0c8575d0c7ab0ebe6bc8dfd3cbe966090f074793d7a91a11fcd7e5bcb0939c4d5cbfd25917396baf523e2a2d334b60e38774e04a7649a3a140ab9599f151cfa8
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libidn2/libidn2_2.3.7.orig.tar.gz' libidn2_2.3.7.orig.tar.gz 2155214 SHA512:eab5702bc0baed45492f8dde43a4d2ea3560ad80645e5f9e0cfa8d3b57bccd7fd782d04638e000ba07924a5d9f85e760095b55189188c4017b94705bef9b4a66
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libidn2/libidn2_2.3.7.orig.tar.gz.asc' libidn2_2.3.7.orig.tar.gz.asc 228 SHA512:00e5f8c3b6b1aef9ee341db99b339217080a57dbe65fba56798d60ad4be971a9535d8ae27e1f243b18b9fc9e900ada6c452b040a6c8094d5e05d8a76d1d79c03
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libidn2/libidn2_2.3.7-2build2.debian.tar.xz' libidn2_2.3.7-2build2.debian.tar.xz 16452 SHA512:55a812a877b2a8039d4105bb8509f389613ad8cb469eb560a3c08085578c448eff1ee1277f69df0505072b1d77ebc6104ad29cd0b6e84be5c56f74e5d0f8ba50
```

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

### `dpkg` source package: `libseccomp=2.5.5-1ubuntu5`

Binary Packages:

- `libseccomp2:amd64=2.5.5-1ubuntu5`

Licenses: (parsed from: `/usr/share/doc/libseccomp2/copyright`)

- `LGPL-2.1`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libselinux=3.7-3ubuntu1`

Binary Packages:

- `libselinux1:amd64=3.7-3ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libselinux1/copyright`)

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
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsepol/libsepol_3.7-1.dsc' libsepol_3.7-1.dsc 2085 SHA512:f6739a13677ec7575fa3a84c3877780c23fbdc65a1a4d1d4a5d9657438fc6b66ddb59390271837d04266c02e087a862ea6ab49cb302596fc95abd7c931a0a467
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsepol/libsepol_3.7.orig.tar.gz' libsepol_3.7.orig.tar.gz 511487 SHA512:85d12d0ba5a7a3225f08d041a18fd59641608db5e0a78a1e9649754e45be54a807cd422d4889b88da6e806b4af546336c7a0913448f08ac33dc6ffb983890ef8
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsepol/libsepol_3.7-1.debian.tar.xz' libsepol_3.7-1.debian.tar.xz 27632 SHA512:9809b3b82c0f816c7fb9b2ec2eb5be8ced95d2d774aebb0834c6848621d0b337ef2950d98602b75e1619db08fb90e4e59e5a0025dfa1a782222addc9535318d5
```

### `dpkg` source package: `libtasn1-6=4.19.0-3build1`

Binary Packages:

- `libtasn1-6:amd64=4.19.0-3build1`

Licenses: (parsed from: `/usr/share/doc/libtasn1-6/copyright`)

- `GFDL-1.3`
- `GPL-3`
- `LGPL`
- `LGPL-2.1`

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

### `dpkg` source package: `libxcrypt=1:4.4.36-5`

Binary Packages:

- `libcrypt1:amd64=1:4.4.36-5`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/libxcrypt/1:4.4.36-5/


### `dpkg` source package: `libzstd=1.5.6+dfsg-1`

Binary Packages:

- `libzstd1:amd64=1.5.6+dfsg-1`

Licenses: (parsed from: `/usr/share/doc/libzstd1/copyright`)

- `BSD-3-clause`
- `Expat`
- `GPL-2`
- `zlib`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/libzstd/1.5.6+dfsg-1/


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


### `dpkg` source package: `ncurses=6.5-2`

Binary Packages:

- `libncursesw6:amd64=6.5-2`
- `libtinfo6:amd64=6.5-2`
- `ncurses-base=6.5-2`
- `ncurses-bin=6.5-2`

Licenses: (parsed from: `/usr/share/doc/libncursesw6/copyright`, `/usr/share/doc/libtinfo6/copyright`, `/usr/share/doc/ncurses-base/copyright`, `/usr/share/doc/ncurses-bin/copyright`)

- `BSD-3-clause`
- `MIT/X11`
- `X11`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/ncurses/6.5-2/


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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/nettle/3.10-1/


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


### `dpkg` source package: `openssl=3.3.1-2ubuntu2`

Binary Packages:

- `libssl3t64:amd64=3.3.1-2ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libssl3t64/copyright`)

- `Apache-2.0`
- `Artistic`
- `GPL-1`
- `GPL-1+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `p11-kit=0.25.5-2ubuntu1`

Binary Packages:

- `libp11-kit0:amd64=0.25.5-2ubuntu1`

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

### `dpkg` source package: `pcre2=10.42-4ubuntu3`

Binary Packages:

- `libpcre2-8-0:amd64=10.42-4ubuntu3`

Licenses: (parsed from: `/usr/share/doc/libpcre2-8-0/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `BSD-3-clause-Cambridge with BINARY LIBRARY-LIKE PACKAGES exception`
- `X11`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `perl=5.40.0-8`

Binary Packages:

- `perl-base=5.40.0-8`

Licenses: (parsed from: `/usr/share/doc/perl-base/copyright`)

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

### `dpkg` source package: `shadow=1:4.15.3-3ubuntu2`

Binary Packages:

- `login=1:4.15.3-3ubuntu2`
- `passwd=1:4.15.3-3ubuntu2`

Licenses: (parsed from: `/usr/share/doc/login/copyright`, `/usr/share/doc/passwd/copyright`)

- `BSD-3-clause`
- `GPL-1`
- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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

### `dpkg` source package: `util-linux=2.40.2-1ubuntu2`

Binary Packages:

- `bsdutils=1:2.40.2-1ubuntu2`
- `libblkid1:amd64=2.40.2-1ubuntu2`
- `libmount1:amd64=2.40.2-1ubuntu2`
- `libsmartcols1:amd64=2.40.2-1ubuntu2`
- `libuuid1:amd64=2.40.2-1ubuntu2`
- `mount=2.40.2-1ubuntu2`
- `util-linux=2.40.2-1ubuntu2`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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

- `liblzma5:amd64=5.6.3-1`

Licenses: (parsed from: `/usr/share/doc/liblzma5/copyright`)

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

Licenses: (parsed from: `/usr/share/doc/zlib1g/copyright`)

- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris zlib=1:1.3.dfsg+really1.3.1-1ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/z/zlib/zlib_1.3.dfsg%2breally1.3.1-1ubuntu1.dsc' zlib_1.3.dfsg+really1.3.1-1ubuntu1.dsc 2993 SHA512:b87b9b973aa22f9cea28d9653bba4383a27203ffb391ff0df537225bbca131eb47b08bc12178bf4d05348e379159be275bddf2d611c97a6bcebd80a0f1ca6e8f
'http://archive.ubuntu.com/ubuntu/pool/main/z/zlib/zlib_1.3.dfsg%2breally1.3.1.orig.tar.gz' zlib_1.3.dfsg+really1.3.1.orig.tar.gz 1325737 SHA512:068cb731e400cfc435db292839737938199d05d77b3010c7b9b87c9d0a127c7545198cea2a620da124ea3dfdde02ab63672aa01fc6cfd1e1ab5a2d6f9ca454c8
'http://archive.ubuntu.com/ubuntu/pool/main/z/zlib/zlib_1.3.dfsg%2breally1.3.1-1ubuntu1.debian.tar.xz' zlib_1.3.dfsg+really1.3.1-1ubuntu1.debian.tar.xz 59676 SHA512:c4d82f270d4334711e26d5d328683d0214d3171a2cfaff0b5b613d4df28adabf01e69ec9f6093991ef8f124f289826f30f2fc64223956462d26c9d67866482fe
```
