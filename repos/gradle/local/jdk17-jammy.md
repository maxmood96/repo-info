# `gradle:9.4.1-jdk17-jammy`

## Docker Metadata

- Image ID: `sha256:479b8739951d11b70be61603d2ced28cfb7a4ee29947f77714ccc7c0072c54f8`
- Created: `2026-04-15T21:30:21.55935798Z`
- Virtual Size: ~ 725.08 Mb  
  (total size of all layers on-disk)
- Arch: `linux`/`amd64`
- Entrypoint: `["/__cacert_entrypoint.sh"]`
- Command: `["gradle"]`
- Environment:
  - `PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin`
  - `JAVA_HOME=/opt/java/openjdk`
  - `LANG=en_US.UTF-8`
  - `LANGUAGE=en_US:en`
  - `LC_ALL=en_US.UTF-8`
  - `JAVA_VERSION=jdk-17.0.18+8`
  - `GRADLE_HOME=/opt/gradle`
  - `GRADLE_VERSION=9.4.1`
- Labels:
  - `org.opencontainers.image.version=22.04`

## `dpkg` (`.deb`-based packages)

### `dpkg` source package: `acl=2.3.1-1`

Binary Packages:

- `libacl1:amd64=2.3.1-1`

Licenses: (parsed from: `/usr/share/doc/libacl1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2+`
- `LGPL-2.1`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/acl/2.3.1-1/


### `dpkg` source package: `adduser=3.118ubuntu5`

Binary Packages:

- `adduser=3.118ubuntu5`

Licenses: (parsed from: `/usr/share/doc/adduser/copyright`)

- `GPL-2`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `apr-util=1.6.1-5ubuntu4.22.04.2`

Binary Packages:

- `libaprutil1:amd64=1.6.1-5ubuntu4.22.04.2`

Licenses: (parsed from: `/usr/share/doc/libaprutil1/copyright`)

- `Apache-2.0`

Source:

```console
$ apt-get source -qq --print-uris apr-util=1.6.1-5ubuntu4.22.04.2
'http://security.ubuntu.com/ubuntu/pool/main/a/apr-util/apr-util_1.6.1-5ubuntu4.22.04.2.dsc' apr-util_1.6.1-5ubuntu4.22.04.2.dsc 2643 SHA512:94b938e9b9f34a7d24d82a6e26409aa3fd61d13e6dd0cba2bb0fcd3096ee9c3e3b56dd6dcfad7b36f719e14af182f45f4ee2b4ddc37bdc4a64d9b24970cf24e9
'http://security.ubuntu.com/ubuntu/pool/main/a/apr-util/apr-util_1.6.1.orig.tar.bz2' apr-util_1.6.1.orig.tar.bz2 428595 SHA512:40eff8a37c0634f7fdddd6ca5e596b38de15fd10767a34c30bbe49c632816e8f3e1e230678034f578dd5816a94f246fb5dfdf48d644829af13bf28de3225205d
'http://security.ubuntu.com/ubuntu/pool/main/a/apr-util/apr-util_1.6.1-5ubuntu4.22.04.2.debian.tar.xz' apr-util_1.6.1-5ubuntu4.22.04.2.debian.tar.xz 344940 SHA512:b9a9c5aff57f47e50955a4c3a808c5cb450faeed572c1f60654edfcceb3d22e6f165dade59a5a9d713ae934ac1d4de0a38328fa70a53930f7235ce45eca466c6
```

### `dpkg` source package: `apr=1.7.0-8ubuntu0.22.04.2`

Binary Packages:

- `libapr1:amd64=1.7.0-8ubuntu0.22.04.2`

Licenses: (parsed from: `/usr/share/doc/libapr1/copyright`)

- `Apache-2.0`

Source:

```console
$ apt-get source -qq --print-uris apr=1.7.0-8ubuntu0.22.04.2
'http://security.ubuntu.com/ubuntu/pool/main/a/apr/apr_1.7.0-8ubuntu0.22.04.2.dsc' apr_1.7.0-8ubuntu0.22.04.2.dsc 1806 SHA512:3135eb205397415f93de6388813c286c7e10af78c505ad8759fda2175863ee036995e0738e547706b17f9efdaba9b909747aca8d3432b22f2110c048d7de5551
'http://security.ubuntu.com/ubuntu/pool/main/a/apr/apr_1.7.0.orig.tar.bz2' apr_1.7.0.orig.tar.bz2 872238 SHA512:3dc42d5caf17aab16f5c154080f020d5aed761e22db4c5f6506917f6bfd2bf8becfb40af919042bd4ce1077d5de74aa666f5edfba7f275efba78e8893c115148
'http://security.ubuntu.com/ubuntu/pool/main/a/apr/apr_1.7.0.orig.tar.bz2.asc' apr_1.7.0.orig.tar.bz2.asc 801 SHA512:19b2b128c7c4cb40db06149c75325013a716c783e28e366c1bacf289fdb5d305e5779d8dc55a63729250ad3338cd4c726e133c788fe53ab3519f1bc8d4da6f90
'http://security.ubuntu.com/ubuntu/pool/main/a/apr/apr_1.7.0-8ubuntu0.22.04.2.debian.tar.xz' apr_1.7.0-8ubuntu0.22.04.2.debian.tar.xz 224584 SHA512:b8c2f54c6034249574e0b56f80cffbac04b614caca2c05e6ddf840660e4b47025792b382a05d2c177b31030d9032875124f7b970f1149c1b792cf3472e43d9ea
```

### `dpkg` source package: `apt=2.4.14`

Binary Packages:

- `apt=2.4.14`
- `libapt-pkg6.0:amd64=2.4.14`

Licenses: (parsed from: `/usr/share/doc/apt/copyright`, `/usr/share/doc/libapt-pkg6.0/copyright`)

- `GPL-2`
- `GPLv2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `attr=1:2.5.1-1build1`

Binary Packages:

- `libattr1:amd64=1:2.5.1-1build1`

Licenses: (parsed from: `/usr/share/doc/libattr1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2+`
- `LGPL-2.1`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `audit=1:3.0.7-1build1`

Binary Packages:

- `libaudit-common=1:3.0.7-1build1`
- `libaudit1:amd64=1:3.0.7-1build1`

Licenses: (parsed from: `/usr/share/doc/libaudit-common/copyright`, `/usr/share/doc/libaudit1/copyright`)

- `GPL-1`
- `GPL-2`
- `LGPL-2.1`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `base-files=12ubuntu4.7`

Binary Packages:

- `base-files=12ubuntu4.7`

Licenses: (parsed from: `/usr/share/doc/base-files/copyright`)

- `GPL`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `base-passwd=3.5.52build1`

Binary Packages:

- `base-passwd=3.5.52build1`

Licenses: (parsed from: `/usr/share/doc/base-passwd/copyright`)

- `GPL-2`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `bash=5.1-6ubuntu1.1`

Binary Packages:

- `bash=5.1-6ubuntu1.1`

Licenses: (parsed from: `/usr/share/doc/bash/copyright`)

- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris bash=5.1-6ubuntu1.1
'http://security.ubuntu.com/ubuntu/pool/main/b/bash/bash_5.1-6ubuntu1.1.dsc' bash_5.1-6ubuntu1.1.dsc 2409 SHA512:8adffecbfd9ffe55500fb70616e4b441bccb95fda13762dc2cccc3605a25f34851b142d2c633f17a5a7e426f0c5010ad76b0a70d375f923e25f6c9f4c893c8e4
'http://security.ubuntu.com/ubuntu/pool/main/b/bash/bash_5.1.orig.tar.xz' bash_5.1.orig.tar.xz 5802740 SHA512:95d3acc542231cb893e1347c7d9dd66687f68cd347a0e9e126fde2d14e68c5b5530d1a5866eafa781e88aa013fcf72b4ad56d2e484c2ac7a69bd90bb149a9b86
'http://security.ubuntu.com/ubuntu/pool/main/b/bash/bash_5.1-6ubuntu1.1.debian.tar.xz' bash_5.1-6ubuntu1.1.debian.tar.xz 99944 SHA512:d7fb6110df70232bd3280c1140a812a1903968792f6608481c184bd28760d03323ada75ed3ca4da4eb6c56a84781d6e2f441e0ee83dd9364a9e37fd0fa2211e9
```

### `dpkg` source package: `binutils=2.38-4ubuntu2.12`

Binary Packages:

- `binutils=2.38-4ubuntu2.12`
- `binutils-common:amd64=2.38-4ubuntu2.12`
- `binutils-x86-64-linux-gnu=2.38-4ubuntu2.12`
- `libbinutils:amd64=2.38-4ubuntu2.12`
- `libctf-nobfd0:amd64=2.38-4ubuntu2.12`
- `libctf0:amd64=2.38-4ubuntu2.12`

Licenses: (parsed from: `/usr/share/doc/binutils/copyright`, `/usr/share/doc/binutils-common/copyright`, `/usr/share/doc/binutils-x86-64-linux-gnu/copyright`, `/usr/share/doc/libbinutils/copyright`, `/usr/share/doc/libctf-nobfd0/copyright`, `/usr/share/doc/libctf0/copyright`)

- `GFDL`
- `GPL`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris binutils=2.38-4ubuntu2.12
'http://security.ubuntu.com/ubuntu/pool/main/b/binutils/binutils_2.38-4ubuntu2.12.dsc' binutils_2.38-4ubuntu2.12.dsc 8865 SHA512:06762ac6f41bc85e93d660228b769563a44b5fbf6b9e4b8aec9b4e2246fb30554953c5605dcb93ad3c1d2da99af060036a6ae3459f21de3fa4e0308e9ab8d7dc
'http://security.ubuntu.com/ubuntu/pool/main/b/binutils/binutils_2.38.orig.tar.xz' binutils_2.38.orig.tar.xz 23651408 SHA512:8bf0b0d193c9c010e0518ee2b2e5a830898af206510992483b427477ed178396cd210235e85fd7bd99a96fc6d5eedbeccbd48317a10f752b7336ada8b2bb826d
'http://security.ubuntu.com/ubuntu/pool/main/b/binutils/binutils_2.38-4ubuntu2.12.debian.tar.xz' binutils_2.38-4ubuntu2.12.debian.tar.xz 333584 SHA512:5af64c9f54e69c49a0dd7b7fb4f7b720b7a456cecccb6077638d88eeb5541feef036de3c35194e1391220540267ea82471b3ef24db40cc559123abec654c2055
```

### `dpkg` source package: `breezy=3.2.1+bzr7585-1build1`

Binary Packages:

- `brz=3.2.1+bzr7585-1build1`
- `python3-breezy=3.2.1+bzr7585-1build1`

Licenses: (parsed from: `/usr/share/doc/brz/copyright`, `/usr/share/doc/python3-breezy/copyright`)

- `GPL-2`
- `GPL-2+`
- `MIT`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `brotli=1.0.9-2build6`

Binary Packages:

- `libbrotli1:amd64=1.0.9-2build6`

Licenses: (parsed from: `/usr/share/doc/libbrotli1/copyright`)

- `MIT`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `bzip2=1.0.8-5build1`

Binary Packages:

- `libbz2-1.0:amd64=1.0.8-5build1`

Licenses: (parsed from: `/usr/share/doc/libbz2-1.0/copyright`)

- `BSD-variant`
- `GPL-2`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ca-certificates=20240203~22.04.1`

Binary Packages:

- `ca-certificates=20240203~22.04.1`

Licenses: (parsed from: `/usr/share/doc/ca-certificates/copyright`)

- `GPL-2`
- `GPL-2+`
- `MPL-2.0`

Source:

```console
$ apt-get source -qq --print-uris ca-certificates=20240203~22.04.1
'http://security.ubuntu.com/ubuntu/pool/main/c/ca-certificates/ca-certificates_20240203%7e22.04.1.dsc' ca-certificates_20240203~22.04.1.dsc 1850 SHA512:af1c4a4a202eead02abba4808ce5e7b731f7e2db6b194e74ff9f5331b515213490ba63181f7ffc59f01f5bd13b7fe80519694c7ff21502cd7e2e095075896696
'http://security.ubuntu.com/ubuntu/pool/main/c/ca-certificates/ca-certificates_20240203%7e22.04.1.tar.xz' ca-certificates_20240203~22.04.1.tar.xz 263132 SHA512:64e97c5b258dfede258dd9b447d2a1f5a43db0e70309bb4e0259b8ed9d103e1a751fb563bb4902460667385d38325945e806726aa6db8876920dff670034f3f1
```

### `dpkg` source package: `cdebconf=0.261ubuntu1`

Binary Packages:

- `libdebconfclient0:amd64=0.261ubuntu1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `configobj=5.0.6-5ubuntu0.1`

Binary Packages:

- `python3-configobj=5.0.6-5ubuntu0.1`

Licenses: (parsed from: `/usr/share/doc/python3-configobj/copyright`)

- `BSD-3-clause`

Source:

```console
$ apt-get source -qq --print-uris configobj=5.0.6-5ubuntu0.1
'http://security.ubuntu.com/ubuntu/pool/main/c/configobj/configobj_5.0.6-5ubuntu0.1.dsc' configobj_5.0.6-5ubuntu0.1.dsc 2208 SHA512:49c716ab2a1b1d3ff901e6ab311967ea96364ed83f7cecb99dbae436b8d51ab416e6892c9c558367cf0c6c9d8b02d291de55230242a79d16df29bffb6d1ef89b
'http://security.ubuntu.com/ubuntu/pool/main/c/configobj/configobj_5.0.6.orig.tar.gz' configobj_5.0.6.orig.tar.gz 143664 SHA512:326eb86e362f281ebf07abcb1cf7616abb270c482eafe842371cda8708245ca5e8262f1644b7164664ecc10e9004ed061c9de18cd233a657d4697dbc3ba3c59d
'http://security.ubuntu.com/ubuntu/pool/main/c/configobj/configobj_5.0.6-5ubuntu0.1.debian.tar.xz' configobj_5.0.6-5ubuntu0.1.debian.tar.xz 8132 SHA512:969f90e9ff7110d678f838106f0feaaf324d538951f88974f76973cd54ca1a9312ae14e74aea0157213f467bd4a85322ab5b39b3284ab14fe6d95d00546cea3a
```

### `dpkg` source package: `coreutils=8.32-4.1ubuntu1.3`

Binary Packages:

- `coreutils=8.32-4.1ubuntu1.3`

Licenses: (parsed from: `/usr/share/doc/coreutils/copyright`)

- `GPL-3`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `curl=7.81.0-1ubuntu1.23`

Binary Packages:

- `curl=7.81.0-1ubuntu1.23`
- `libcurl3-gnutls:amd64=7.81.0-1ubuntu1.23`
- `libcurl4:amd64=7.81.0-1ubuntu1.23`

Licenses: (parsed from: `/usr/share/doc/curl/copyright`, `/usr/share/doc/libcurl3-gnutls/copyright`, `/usr/share/doc/libcurl4/copyright`)

- `BSD-3-Clause`
- `BSD-4-Clause`
- `ISC`
- `curl`
- `other`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris curl=7.81.0-1ubuntu1.23
'http://security.ubuntu.com/ubuntu/pool/main/c/curl/curl_7.81.0-1ubuntu1.23.dsc' curl_7.81.0-1ubuntu1.23.dsc 3143 SHA512:9038c454e1d7c358914c6031934b2088c08f5a86a3bc21516c5d88a1ed039258e8f5f3f9fc99b084937080f5d263a9508e184eacccc541bc2a647afbd5e69c58
'http://security.ubuntu.com/ubuntu/pool/main/c/curl/curl_7.81.0.orig.tar.gz' curl_7.81.0.orig.tar.gz 4188040 SHA512:e3084f0fa083f7f93eac923edbfdddb5fd0a372b94673ba9d4427a2b95508898c15ecdf63b99a1c1f6cf3215e27b06cbaa2b7073df038d43b362e586f92495d3
'http://security.ubuntu.com/ubuntu/pool/main/c/curl/curl_7.81.0.orig.tar.gz.asc' curl_7.81.0.orig.tar.gz.asc 488 SHA512:92bc5ede831551285d67b03abe8400c609ad31c9d33e324ee5c41b92dd5c2a0245a09a396bd76807b3e44bcfef944b1e16ac266264f7b85d27cc1c072a6e82bd
'http://security.ubuntu.com/ubuntu/pool/main/c/curl/curl_7.81.0-1ubuntu1.23.debian.tar.xz' curl_7.81.0-1ubuntu1.23.debian.tar.xz 86808 SHA512:d98d9f3ffc6a5742139745821711b915b7bb9f8ff8e0827c10cc9f96516e95f626275fe0aade377f07aa525e2e3d00881289aeda53144edc0f6b61a737ada2e2
```

### `dpkg` source package: `cyrus-sasl2=2.1.27+dfsg2-3ubuntu1.2`

Binary Packages:

- `libsasl2-2:amd64=2.1.27+dfsg2-3ubuntu1.2`
- `libsasl2-modules-db:amd64=2.1.27+dfsg2-3ubuntu1.2`

Licenses: (parsed from: `/usr/share/doc/libsasl2-2/copyright`, `/usr/share/doc/libsasl2-modules-db/copyright`)

- `BSD-2-clause`
- `BSD-2.2-clause`
- `BSD-3-clause`
- `BSD-3-clause-JANET`
- `BSD-3-clause-PADL`
- `BSD-4-clause`
- `BSD-4-clause-UC`
- `FSFULLR`
- `GPL-3`
- `GPL-3+`
- `IBM-as-is`
- `MIT-CMU`
- `MIT-Export`
- `MIT-OpenVision`
- `OpenLDAP`
- `OpenSSL`
- `RSA-MD`
- `SSLeay`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `dash=0.5.11+git20210903+057cd650a4ed-3build1`

Binary Packages:

- `dash=0.5.11+git20210903+057cd650a4ed-3build1`

Licenses: (parsed from: `/usr/share/doc/dash/copyright`)

- `BSD-3-Clause`
- `BSD-3-clause`
- `Expat`
- `FSFUL`
- `FSFULLR`
- `GPL-2`
- `GPL-2+`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `db5.3=5.3.28+dfsg1-0.8ubuntu3`

Binary Packages:

- `libdb5.3:amd64=5.3.28+dfsg1-0.8ubuntu3`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `debconf=1.5.79ubuntu1`

Binary Packages:

- `debconf=1.5.79ubuntu1`

Licenses: (parsed from: `/usr/share/doc/debconf/copyright`)

- `BSD-2-clause`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `debianutils=5.5-1ubuntu2`

Binary Packages:

- `debianutils=5.5-1ubuntu2`

Licenses: (parsed from: `/usr/share/doc/debianutils/copyright`)

- `GPL-2`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `diffutils=1:3.8-0ubuntu2`

Binary Packages:

- `diffutils=1:3.8-0ubuntu2`

Licenses: (parsed from: `/usr/share/doc/diffutils/copyright`)

- `GFDL`
- `GPL`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `dpkg=1.21.1ubuntu2.6`

Binary Packages:

- `dpkg=1.21.1ubuntu2.6`

Licenses: (parsed from: `/usr/share/doc/dpkg/copyright`)

- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`
- `public-domain-md5`
- `public-domain-s-s-d`

Source:

```console
$ apt-get source -qq --print-uris dpkg=1.21.1ubuntu2.6
'http://security.ubuntu.com/ubuntu/pool/main/d/dpkg/dpkg_1.21.1ubuntu2.6.dsc' dpkg_1.21.1ubuntu2.6.dsc 2254 SHA512:e5d28c73b84700cdbeb0f9f204e328538972dddd110fb6623eb1bdf0d85988000799408d564cb2b3c4af94b4d9bacf1a8eafb312a1e676bdd6518340082e44a4
'http://security.ubuntu.com/ubuntu/pool/main/d/dpkg/dpkg_1.21.1ubuntu2.6.tar.xz' dpkg_1.21.1ubuntu2.6.tar.xz 5017128 SHA512:2eb70e5ca3e2d0cafe460eb5236e81c3312e84426d5732cbc64952702e8e81fe9119d06a51fed1e9b72c58db8a9d4484ca6dddf5b92be351eb5a2c75ddd3c06c
```

### `dpkg` source package: `dulwich=0.20.31-1.1build1`

Binary Packages:

- `python3-dulwich=0.20.31-1.1build1`

Licenses: (parsed from: `/usr/share/doc/python3-dulwich/copyright`)

- `Apache-2`
- `Apache-2.0`
- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `e2fsprogs=1.46.5-2ubuntu1.2`

Binary Packages:

- `e2fsprogs=1.46.5-2ubuntu1.2`
- `libcom-err2:amd64=1.46.5-2ubuntu1.2`
- `libext2fs2:amd64=1.46.5-2ubuntu1.2`
- `libss2:amd64=1.46.5-2ubuntu1.2`
- `logsave=1.46.5-2ubuntu1.2`

Licenses: (parsed from: `/usr/share/doc/e2fsprogs/copyright`, `/usr/share/doc/libcom-err2/copyright`, `/usr/share/doc/libext2fs2/copyright`, `/usr/share/doc/libss2/copyright`, `/usr/share/doc/logsave/copyright`)

- `GPL-2`
- `LGPL-2`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `expat=2.4.7-1ubuntu0.7`

Binary Packages:

- `libexpat1:amd64=2.4.7-1ubuntu0.7`

Licenses: (parsed from: `/usr/share/doc/libexpat1/copyright`)

- `MIT`

Source:

```console
$ apt-get source -qq --print-uris expat=2.4.7-1ubuntu0.7
'http://security.ubuntu.com/ubuntu/pool/main/e/expat/expat_2.4.7-1ubuntu0.7.dsc' expat_2.4.7-1ubuntu0.7.dsc 1962 SHA512:25ef840e96fb88038fd85bb69e5b235bfbb75c6ff4f465a59aebefb33456f38e678c8cfddc422253769893502c1972c6c4616bd22867bc52e0d719cd5f83e0bd
'http://security.ubuntu.com/ubuntu/pool/main/e/expat/expat_2.4.7.orig.tar.gz' expat_2.4.7.orig.tar.gz 8316374 SHA512:91bc9792c4ba1d0ad835f633d8cfa62130692f48308eea8932ec5e13a01542120561b0f255b4adc58b1adae6f83632cbabf428b5b5c0d2ac6de542478a951232
'http://security.ubuntu.com/ubuntu/pool/main/e/expat/expat_2.4.7-1ubuntu0.7.debian.tar.xz' expat_2.4.7-1ubuntu0.7.debian.tar.xz 37472 SHA512:f8593c0ab26b2df80853d7d77b1e5047e6ed3590dcbcae4bdff507023ad61cf8c36b88a3420e9d44b723b1c2b72d6228993100f4d58c6cf520c3dc5433f167d0
```

### `dpkg` source package: `findutils=4.8.0-1ubuntu3`

Binary Packages:

- `findutils=4.8.0-1ubuntu3`

Licenses: (parsed from: `/usr/share/doc/findutils/copyright`)

- `GFDL-1.3`
- `GPL-3`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `fontconfig=2.13.1-4.2ubuntu5`

Binary Packages:

- `fontconfig=2.13.1-4.2ubuntu5`
- `fontconfig-config=2.13.1-4.2ubuntu5`
- `libfontconfig1:amd64=2.13.1-4.2ubuntu5`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `fonts-dejavu=2.37-2build1`

Binary Packages:

- `fonts-dejavu-core=2.37-2build1`

Licenses: (parsed from: `/usr/share/doc/fonts-dejavu-core/copyright`)

- `GPL-2`
- `GPL-2+`
- `bitstream-vera`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `freetype=2.11.1+dfsg-1ubuntu0.3`

Binary Packages:

- `libfreetype6:amd64=2.11.1+dfsg-1ubuntu0.3`

Licenses: (parsed from: `/usr/share/doc/libfreetype6/copyright`)

- `BSD-3-Clause`
- `BSL-1.0`
- `FSFAP`
- `FTL`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `MIT`
- `OpenGroup-BSD-like`
- `Public-Domain`
- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris freetype=2.11.1+dfsg-1ubuntu0.3
'http://security.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.11.1%2bdfsg-1ubuntu0.3.dsc' freetype_2.11.1+dfsg-1ubuntu0.3.dsc 3791 SHA512:956ef790ec1f6cd70d35dd4b47217e9268f909478672946b85d43a5d08c368ded5524a9e71a1c2cce003b6341291b04d1cfd831fc8a6b0b70b7880caaa0a189b
'http://security.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.11.1%2bdfsg.orig-ft2demos.tar.xz' freetype_2.11.1+dfsg.orig-ft2demos.tar.xz 257240 SHA512:93d68daefa8a49b4fc987a7356133299fe2a8e012415ea09ad7616ececcfd978fdf9fc7a2d855f7488f51a497d019acb89ef5774484babae66357b3083a883c5
'http://security.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.11.1%2bdfsg.orig-ft2demos.tar.xz.asc' freetype_2.11.1+dfsg.orig-ft2demos.tar.xz.asc 195 SHA512:407ffade07cc62c8838d26670dffc7c26b9baf4984c42b2b2467279dabda855536b403f5a7e9dc64a787163657ca81019fef6d1879973faf180d6230ab17cd05
'http://security.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.11.1%2bdfsg.orig-ft2docs.tar.xz' freetype_2.11.1+dfsg.orig-ft2docs.tar.xz 2038348 SHA512:c5e19d98425491682edc58230c48390925cc4b466169f655cf3b8575ba787a70feecdeb7a16224b132dcc32f17b041483d84056cda8e3132d98b531e46a26c36
'http://security.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.11.1%2bdfsg.orig-ft2docs.tar.xz.asc' freetype_2.11.1+dfsg.orig-ft2docs.tar.xz.asc 195 SHA512:df946695a1fbaa71009f48a8f0860177984728ec1c73385d1e55c07be027dd6a5e634c9dcbb49c51f8143b0d56a6cbf06393403341fb28cea7a8a2cc9a9c5592
'http://security.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.11.1%2bdfsg.orig.tar.xz' freetype_2.11.1+dfsg.orig.tar.xz 1988020 SHA512:6a9a0379679abf127761cabb2da39b8faf2ca4c322075da9b86d93363ac81ce909b9544377a784118ba91ca008baa680b9da474bd2da1bfe928d5a4c9114cb08
'http://security.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.11.1%2bdfsg-1ubuntu0.3.debian.tar.xz' freetype_2.11.1+dfsg-1ubuntu0.3.debian.tar.xz 42292 SHA512:068774dbcbd393912de1b89323f856121269e2031e662e8473372b1849e7b3d26714f2eb9d7623b49136c7b448b3267959f2c158557fbf771ef294ea799097dc
```

### `dpkg` source package: `gcc-12=12.3.0-1ubuntu1~22.04.3`

Binary Packages:

- `gcc-12-base:amd64=12.3.0-1ubuntu1~22.04.3`
- `libgcc-s1:amd64=12.3.0-1ubuntu1~22.04.3`
- `libstdc++6:amd64=12.3.0-1ubuntu1~22.04.3`

Licenses: (parsed from: `/usr/share/doc/gcc-12-base/copyright`, `/usr/share/doc/libgcc-s1/copyright`, `/usr/share/doc/libstdc++6/copyright`)

- `Artistic`
- `GFDL-1.2`
- `GPL`
- `GPL-2`
- `GPL-3`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris gcc-12=12.3.0-1ubuntu1~22.04.3
'http://security.ubuntu.com/ubuntu/pool/main/g/gcc-12/gcc-12_12.3.0-1ubuntu1%7e22.04.3.dsc' gcc-12_12.3.0-1ubuntu1~22.04.3.dsc 27845 SHA512:8e4d9743dc772aefc525a1ee04055e6c814e0a36b929ee2d2660bb341d44c06641b860fd567a750bc4fb3e90f1f5f9b6480931018a1681a6a87326e2200baffa
'http://security.ubuntu.com/ubuntu/pool/main/g/gcc-12/gcc-12_12.3.0.orig.tar.gz' gcc-12_12.3.0.orig.tar.gz 91555468 SHA512:a33ce506594e13cf96f0419e6d62b71f8906c87c69426218bf8679d281865f1b170bc2f7379216ae1d6ad9f6bdbf5819c34c65c7537fdb74179c27b0d4ab7b48
'http://security.ubuntu.com/ubuntu/pool/main/g/gcc-12/gcc-12_12.3.0-1ubuntu1%7e22.04.3.debian.tar.xz' gcc-12_12.3.0-1ubuntu1~22.04.3.debian.tar.xz 587456 SHA512:d7721ad3f05f4918ac658b7df557db130cd5549b138578a212f616dec53485d4e80a59c4ef2afc7b46ddd66e51dd77a4036d57e8f99a44a4c4be3eff854f62e3
```

### `dpkg` source package: `gdbm=1.23-1`

Binary Packages:

- `libgdbm-compat4:amd64=1.23-1`
- `libgdbm6:amd64=1.23-1`

Licenses: (parsed from: `/usr/share/doc/libgdbm-compat4/copyright`, `/usr/share/doc/libgdbm6/copyright`)

- `GFDL-NIV-1.3+`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/gdbm/1.23-1/


### `dpkg` source package: `git-lfs=3.0.2-1ubuntu0.3`

Binary Packages:

- `git-lfs=3.0.2-1ubuntu0.3`

Licenses: (parsed from: `/usr/share/doc/git-lfs/copyright`)

- `Expat`

Source:

```console
$ apt-get source -qq --print-uris git-lfs=3.0.2-1ubuntu0.3
'http://security.ubuntu.com/ubuntu/pool/universe/g/git-lfs/git-lfs_3.0.2-1ubuntu0.3.dsc' git-lfs_3.0.2-1ubuntu0.3.dsc 2778 SHA512:05e22b5e4afebf1ad5e5213e6a1d5df27b60b0bb5ff850beb172d3969bebe47c5275aef275464a2c95dcb2766e5a212ee0c49c79363515fea25206397cffd96e
'http://security.ubuntu.com/ubuntu/pool/universe/g/git-lfs/git-lfs_3.0.2.orig.tar.xz' git-lfs_3.0.2.orig.tar.xz 478588 SHA512:5026a08285cd9e8737a27dce836d53e2d14e1c8d8dc5f6664d0f6dbe696a2fdd8f461908fb184b70cf5817bfa86f94c5097d81db7736536e3d5f8661c4ed787b
'http://security.ubuntu.com/ubuntu/pool/universe/g/git-lfs/git-lfs_3.0.2-1ubuntu0.3.debian.tar.xz' git-lfs_3.0.2-1ubuntu0.3.debian.tar.xz 4432 SHA512:023ef83d2682cf50b7d9d38c272cbd009eb4c8ce7ef046a04c8f4750bd634cc9ab43307a46faa16c77d84f942670491bd6033ab949990d79fb8344d4afb54c75
```

### `dpkg` source package: `git=1:2.34.1-1ubuntu1.17`

Binary Packages:

- `git=1:2.34.1-1ubuntu1.17`
- `git-man=1:2.34.1-1ubuntu1.17`

Licenses: (parsed from: `/usr/share/doc/git/copyright`, `/usr/share/doc/git-man/copyright`)

- `Apache-2.0`
- `Artistic`
- `Artistic-1`
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
$ apt-get source -qq --print-uris git=1:2.34.1-1ubuntu1.17
'http://security.ubuntu.com/ubuntu/pool/main/g/git/git_2.34.1-1ubuntu1.17.dsc' git_2.34.1-1ubuntu1.17.dsc 2976 SHA512:9d1d28d9dd12727e504fcde25be88b6434c4a066ffa717384e69c6e3ad553671775f58a87f9d61dfbe518999b18ff50615b1c48445322a02990c9e8ccd26eee9
'http://security.ubuntu.com/ubuntu/pool/main/g/git/git_2.34.1.orig.tar.xz' git_2.34.1.orig.tar.xz 6623760 SHA512:a1a8e9e6f64b1da25508fbd2f783564dcdbe181fb5ff1ebab3bdac6db6094e18acc334479a1abf22ac17ce4f733cc3e10a664db9ab234cd523735a3f027b42db
'http://security.ubuntu.com/ubuntu/pool/main/g/git/git_2.34.1-1ubuntu1.17.debian.tar.xz' git_2.34.1-1ubuntu1.17.debian.tar.xz 789788 SHA512:93417529c6e674a0b8be999c61a15a36cb79b6bb40d25db323bfd9fd92250f505b8cca4913327eca4dbc093bb813a407806196362f0eae750556b91c233ebbf6
```

### `dpkg` source package: `glibc=2.35-0ubuntu3.13`

Binary Packages:

- `libc-bin=2.35-0ubuntu3.13`
- `libc6:amd64=2.35-0ubuntu3.13`
- `locales=2.35-0ubuntu3.13`

Licenses: (parsed from: `/usr/share/doc/libc-bin/copyright`, `/usr/share/doc/libc6/copyright`, `/usr/share/doc/locales/copyright`)

- `GFDL-1.3`
- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris glibc=2.35-0ubuntu3.13
'http://security.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.35-0ubuntu3.13.dsc' glibc_2.35-0ubuntu3.13.dsc 8758 SHA512:50389ac5696e2778dc579c9b01193b216380fe2042f361b99bb3868362ad8fea465e8ebde1d2b213211b8fe0618819026b0e1369f71e9d5bf044591508effa59
'http://security.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.35.orig.tar.xz' glibc_2.35.orig.tar.xz 18165952 SHA512:e7336ce27561be5d7c217832a1136fb327e057bd8d3f92925b35c97e3e9f9e486948b5a1e03e5e4090772ef06437a074d10b82e68f17f1ad8f22077ee39e1b66
'http://security.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.35.orig.tar.xz.asc' glibc_2.35.orig.tar.xz.asc 833 SHA512:2a1c152511dac05f9b4e48f7e7a6b59dbf2d8b71fea54f128173113357be26e86216e13c9865f617049e6858396a221a5abc704f65a786b22453945fd80265e9
'http://security.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.35-0ubuntu3.13.debian.tar.xz' glibc_2.35-0ubuntu3.13.debian.tar.xz 943368 SHA512:ace487d154c8039b45e69bf190d0a8e575292f0e4b7bc689ffe99a3b2f0d4272a896114d37f38352d598e5bcbb3b3c2d4d8cf0c0bc20eec532803a5ce6c16446
```

### `dpkg` source package: `gmp=2:6.2.1+dfsg-3ubuntu1`

Binary Packages:

- `libgmp10:amd64=2:6.2.1+dfsg-3ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libgmp10/copyright`)

- `GPL`
- `GPL-2`
- `GPL-3`
- `LGPL-3`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `gnupg2=2.2.27-3ubuntu2.5`

Binary Packages:

- `dirmngr=2.2.27-3ubuntu2.5`
- `gnupg=2.2.27-3ubuntu2.5`
- `gnupg-l10n=2.2.27-3ubuntu2.5`
- `gnupg-utils=2.2.27-3ubuntu2.5`
- `gpg=2.2.27-3ubuntu2.5`
- `gpg-agent=2.2.27-3ubuntu2.5`
- `gpg-wks-client=2.2.27-3ubuntu2.5`
- `gpg-wks-server=2.2.27-3ubuntu2.5`
- `gpgconf=2.2.27-3ubuntu2.5`
- `gpgsm=2.2.27-3ubuntu2.5`
- `gpgv=2.2.27-3ubuntu2.5`

Licenses: (parsed from: `/usr/share/doc/dirmngr/copyright`, `/usr/share/doc/gnupg/copyright`, `/usr/share/doc/gnupg-l10n/copyright`, `/usr/share/doc/gnupg-utils/copyright`, `/usr/share/doc/gpg/copyright`, `/usr/share/doc/gpg-agent/copyright`, `/usr/share/doc/gpg-wks-client/copyright`, `/usr/share/doc/gpg-wks-server/copyright`, `/usr/share/doc/gpgconf/copyright`, `/usr/share/doc/gpgsm/copyright`, `/usr/share/doc/gpgv/copyright`)

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
$ apt-get source -qq --print-uris gnupg2=2.2.27-3ubuntu2.5
'http://security.ubuntu.com/ubuntu/pool/main/g/gnupg2/gnupg2_2.2.27-3ubuntu2.5.dsc' gnupg2_2.2.27-3ubuntu2.5.dsc 3763 SHA512:178b162bff46e822775007ea3af32f1b63c131eb78d2184225b1e7904669a1338507dd34180e753c641a226c20c2b7967ea1570209020e52c621fb0e824bbc48
'http://security.ubuntu.com/ubuntu/pool/main/g/gnupg2/gnupg2_2.2.27.orig.tar.bz2' gnupg2_2.2.27.orig.tar.bz2 7191555 SHA512:cf336962116c9c08ac80b1299654b94948033ef51d6d5e7f54c2f07bbf7d92c7b0bddb606ceee2cdd837063f519b8d59af5a82816b840a0fc47d90c07b0e95ab
'http://security.ubuntu.com/ubuntu/pool/main/g/gnupg2/gnupg2_2.2.27-3ubuntu2.5.debian.tar.xz' gnupg2_2.2.27-3ubuntu2.5.debian.tar.xz 76672 SHA512:f3fd10428b50fca815afe5bdad9ee8db17f0eb3a8871a7935f94fc28da188cc1779e18bb84ed5a1cf86a464f46e818768d63aa61db9fac36a93ea05a37be9851
```

### `dpkg` source package: `gnutls28=3.7.3-4ubuntu1.8`

Binary Packages:

- `libgnutls30:amd64=3.7.3-4ubuntu1.8`

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
$ apt-get source -qq --print-uris gnutls28=3.7.3-4ubuntu1.8
'http://security.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.7.3-4ubuntu1.8.dsc' gnutls28_3.7.3-4ubuntu1.8.dsc 3575 SHA512:929c2320207c79ae6966863a6d30b0e916fd82af5ce1ad44439828699826c9a8e579dd06a6036371f6f3bf5ac2d8599db73f4543c91bcd76f430161b5be15a4c
'http://security.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.7.3.orig.tar.xz' gnutls28_3.7.3.orig.tar.xz 6119292 SHA512:3ace744affe23e284342658d6d2d2de49dd50065489cbc8be18fc7d38187253e5268ca54027ce5cd517056c249ac039a7481e4548cec04325de37ae85617d077
'http://security.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.7.3.orig.tar.xz.asc' gnutls28_3.7.3.orig.tar.xz.asc 833 SHA512:cd0d30298377deddf20a835863b71e3f119588061f659906ad2684004758943179531508b1c77c730e930e2131148095e60ad9be365353cce772472d5f5345df
'http://security.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.7.3-4ubuntu1.8.debian.tar.xz' gnutls28_3.7.3-4ubuntu1.8.debian.tar.xz 109652 SHA512:85cc05681f4aaea91faf6474c41a1866ee47835eb94d79030723c33e6effd6668412191e8bf675033fb52c1bc69e16e050583641c7b7898af08b23218e0d6e36
```

### `dpkg` source package: `grep=3.7-1build1`

Binary Packages:

- `grep=3.7-1build1`

Licenses: (parsed from: `/usr/share/doc/grep/copyright`)

- `GPL-3`
- `GPL-3+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `gzip=1.10-4ubuntu4.1`

Binary Packages:

- `gzip=1.10-4ubuntu4.1`

Licenses: (parsed from: `/usr/share/doc/gzip/copyright`)

- `FSF-manpages`
- `GFDL-1.3+-no-invariant`
- `GFDL-3`
- `GPL-3`
- `GPL-3+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `hostname=3.23ubuntu2`

Binary Packages:

- `hostname=3.23ubuntu2`

Licenses: (parsed from: `/usr/share/doc/hostname/copyright`)

- `GPL-2`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `init-system-helpers=1.62`

Binary Packages:

- `init-system-helpers=1.62`

Licenses: (parsed from: `/usr/share/doc/init-system-helpers/copyright`)

- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/init-system-helpers/1.62/


### `dpkg` source package: `keyutils=1.6.1-2ubuntu3`

Binary Packages:

- `libkeyutils1:amd64=1.6.1-2ubuntu3`

Licenses: (parsed from: `/usr/share/doc/libkeyutils1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2`
- `LGPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `krb5=1.19.2-2ubuntu0.7`

Binary Packages:

- `libgssapi-krb5-2:amd64=1.19.2-2ubuntu0.7`
- `libk5crypto3:amd64=1.19.2-2ubuntu0.7`
- `libkrb5-3:amd64=1.19.2-2ubuntu0.7`
- `libkrb5support0:amd64=1.19.2-2ubuntu0.7`

Licenses: (parsed from: `/usr/share/doc/libgssapi-krb5-2/copyright`, `/usr/share/doc/libk5crypto3/copyright`, `/usr/share/doc/libkrb5-3/copyright`, `/usr/share/doc/libkrb5support0/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris krb5=1.19.2-2ubuntu0.7
'http://security.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.19.2-2ubuntu0.7.dsc' krb5_1.19.2-2ubuntu0.7.dsc 3697 SHA512:e5705fc2f43b7b7fdc58c720c820f74fb1e07bcea2c5256f7013977c19bab00f4af4da92904bad3dc5e749ff4d7c480da8261d141d215e34b6f12dc9c0b50fe5
'http://security.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.19.2.orig.tar.gz' krb5_1.19.2.orig.tar.gz 8741053 SHA512:b90d6ed0e1e8a87eb5cb2c36d88b823a6a6caabf85e5d419adb8a930f7eea09a5f8491464e7e454cca7ba88be09d19415962fe0036ad2e31fc584f9fc0bbd470
'http://security.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.19.2-2ubuntu0.7.debian.tar.xz' krb5_1.19.2-2ubuntu0.7.debian.tar.xz 124844 SHA512:cc13c07edc27b07c2f4680f6edde898197e8fac06d3c55f83d5b5748c2b1813dff6add13e7d36e9c25e37c1090d90b8ed837bb6a05bf142ab062d1ef7c1148a4
```

### `dpkg` source package: `libassuan=2.5.5-1build1`

Binary Packages:

- `libassuan0:amd64=2.5.5-1build1`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libbsd=0.11.5-1`

Binary Packages:

- `libbsd0:amd64=0.11.5-1`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/libbsd/0.11.5-1/


### `dpkg` source package: `libcap-ng=0.7.9-2.2build3`

Binary Packages:

- `libcap-ng0:amd64=0.7.9-2.2build3`

Licenses: (parsed from: `/usr/share/doc/libcap-ng0/copyright`)

- `GPL-2`
- `GPL-3`
- `LGPL-2.1`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libcap2=1:2.44-1ubuntu0.22.04.2`

Binary Packages:

- `libcap2:amd64=1:2.44-1ubuntu0.22.04.2`

Licenses: (parsed from: `/usr/share/doc/libcap2/copyright`)

- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris libcap2=1:2.44-1ubuntu0.22.04.2
'http://security.ubuntu.com/ubuntu/pool/main/libc/libcap2/libcap2_2.44-1ubuntu0.22.04.2.dsc' libcap2_2.44-1ubuntu0.22.04.2.dsc 2318 SHA512:7762231edf17ffd462dcc81d4ce9fed38b1eb87eed0fc15ae34f95f8464a2d1f8b22a7ca4fc32ec015d81b6cd2f8e05b7f95936e414f1f8d9f400db1d8ef71f6
'http://security.ubuntu.com/ubuntu/pool/main/libc/libcap2/libcap2_2.44.orig.tar.xz' libcap2_2.44.orig.tar.xz 125568 SHA512:1bb323ca362923bd6bd0e2e4639cf8726975165a620a243b31e797056439eb7efb2bfbc8e5521636783a86c7415b2037b1638c98747b79183ca7d3d42a04ff20
'http://security.ubuntu.com/ubuntu/pool/main/libc/libcap2/libcap2_2.44-1ubuntu0.22.04.2.debian.tar.xz' libcap2_2.44-1ubuntu0.22.04.2.debian.tar.xz 23308 SHA512:7a6894c76276e367e7257aa6e2a3cf96d13afe870a42d1298284b4a3ae47ae53922ca4a38466e0b5bb51b832718f8634f72a22e90f996c5b77665454d87044fe
```

### `dpkg` source package: `libcbor=0.8.0-2ubuntu1`

Binary Packages:

- `libcbor0.8:amd64=0.8.0-2ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libcbor0.8/copyright`)

- `Apache-2.0`
- `Expat`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libedit=3.1-20210910-1build1`

Binary Packages:

- `libedit2:amd64=3.1-20210910-1build1`

Licenses: (parsed from: `/usr/share/doc/libedit2/copyright`)

- `BSD-3-clause`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `liberror-perl=0.17029-1`

Binary Packages:

- `liberror-perl=0.17029-1`

Licenses: (parsed from: `/usr/share/doc/liberror-perl/copyright`)

- `Artistic`
- `GPL-1`
- `GPL-1+`
- `MIT/X11`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/liberror-perl/0.17029-1/


### `dpkg` source package: `libffi=3.4.2-4`

Binary Packages:

- `libffi8:amd64=3.4.2-4`

Licenses: (parsed from: `/usr/share/doc/libffi8/copyright`)

- `GPL`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/libffi/3.4.2-4/


### `dpkg` source package: `libfido2=1.10.0-1`

Binary Packages:

- `libfido2-1:amd64=1.10.0-1`

Licenses: (parsed from: `/usr/share/doc/libfido2-1/copyright`)

- `BSD-2-clause`
- `ISC`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/libfido2/1.10.0-1/


### `dpkg` source package: `libgcrypt20=1.9.4-3ubuntu3`

Binary Packages:

- `libgcrypt20:amd64=1.9.4-3ubuntu3`

Licenses: (parsed from: `/usr/share/doc/libgcrypt20/copyright`)

- `GPL-2`
- `LGPL`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libgpg-error=1.43-3`

Binary Packages:

- `libgpg-error0:amd64=1.43-3`

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

- http://snapshot.debian.org/package/libgpg-error/1.43-3/


### `dpkg` source package: `libidn2=2.3.2-2build1`

Binary Packages:

- `libidn2-0:amd64=2.3.2-2build1`

Licenses: (parsed from: `/usr/share/doc/libidn2-0/copyright`)

- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `LGPL-3`
- `LGPL-3+`
- `Unicode`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libksba=1.6.0-2ubuntu0.2`

Binary Packages:

- `libksba8:amd64=1.6.0-2ubuntu0.2`

Licenses: (parsed from: `/usr/share/doc/libksba8/copyright`)

- `FSFUL`
- `GPL-3`
- `LGPL-2.1-or-later`

Source:

```console
$ apt-get source -qq --print-uris libksba=1.6.0-2ubuntu0.2
'http://security.ubuntu.com/ubuntu/pool/main/libk/libksba/libksba_1.6.0-2ubuntu0.2.dsc' libksba_1.6.0-2ubuntu0.2.dsc 2585 SHA512:ef96729e570627b7cf38ed0dcc3338097a81f690dde041fd9ea63b3c4b55c11ccf35ab7b2bbd196af3ca7834f8e5017cbb14436a7718034608f3276ca3db9f3f
'http://security.ubuntu.com/ubuntu/pool/main/libk/libksba/libksba_1.6.0.orig.tar.bz2' libksba_1.6.0.orig.tar.bz2 662120 SHA512:a7c76d41dfd8ec6383ac2de3c53848cd9f066b538f6f3cd43175e3c8095df51b96d0a24a573481c0c4856b09b7c224e2b562d88f5c0801e7acfb582ea2739c2b
'http://security.ubuntu.com/ubuntu/pool/main/libk/libksba/libksba_1.6.0.orig.tar.bz2.asc' libksba_1.6.0.orig.tar.bz2.asc 228 SHA512:fc381ea66eefdb431a5248fa3ac0751d7343d7f99cc7ebf7621b0763e6e31a80b45c5e17b09bbc7c1c1154e6a0152af1f13798f64959ac63f50b789ec046d7a3
'http://security.ubuntu.com/ubuntu/pool/main/libk/libksba/libksba_1.6.0-2ubuntu0.2.debian.tar.xz' libksba_1.6.0-2ubuntu0.2.debian.tar.xz 16004 SHA512:24a609ca522b5e3a1402ff5a97ce451869bdf0960902d171a89f2190d4de7c8442403d21f938cebeeafd0ae082bf03d76c0521b26a2c153257df784cf7894b43
```

### `dpkg` source package: `libmd=1.0.4-1build1`

Binary Packages:

- `libmd0:amd64=1.0.4-1build1`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libnsl=1.3.0-2build2`

Binary Packages:

- `libnsl2:amd64=1.3.0-2build2`

Licenses: (parsed from: `/usr/share/doc/libnsl2/copyright`)

- `BSD-3-clause`
- `GPL-2`
- `GPL-2+-autoconf-exception`
- `GPL-2+-libtool-exception`
- `GPL-3`
- `GPL-3+-autoconf-exception`
- `LGPL-2.1`
- `LGPL-2.1+`
- `MIT`
- `permissive-autoconf-m4`
- `permissive-autoconf-m4-no-warranty`
- `permissive-configure`
- `permissive-fsf`
- `permissive-makefile-in`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libpng1.6=1.6.37-3ubuntu0.4`

Binary Packages:

- `libpng16-16:amd64=1.6.37-3ubuntu0.4`

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
$ apt-get source -qq --print-uris libpng1.6=1.6.37-3ubuntu0.4
'http://security.ubuntu.com/ubuntu/pool/main/libp/libpng1.6/libpng1.6_1.6.37-3ubuntu0.4.dsc' libpng1.6_1.6.37-3ubuntu0.4.dsc 2340 SHA512:1d44a8319583139e83783ab5cdb38ff47d827579a57830d5e36e94fd9b6a4960320df2401c6415d3067e5b14a3beaa97ec89439194445bf637db02856d5495ab
'http://security.ubuntu.com/ubuntu/pool/main/libp/libpng1.6/libpng1.6_1.6.37.orig.tar.gz' libpng1.6_1.6.37.orig.tar.gz 1508805 SHA512:ccb3705c23b2724e86d072e2ac8cfc380f41fadfd6977a248d588a8ad57b6abe0e4155e525243011f245e98d9b7afbe2e8cc7fd4ff7d82fcefb40c0f48f88918
'http://security.ubuntu.com/ubuntu/pool/main/libp/libpng1.6/libpng1.6_1.6.37-3ubuntu0.4.debian.tar.xz' libpng1.6_1.6.37-3ubuntu0.4.debian.tar.xz 40160 SHA512:424cfa9b4c46257a350e94a856f849de3969171334d291b5434a3dab53866830a8676a71e4aadfee6b620b6e3b6426ac63dd7977d1bee9fbc92c9a22a8454247
```

### `dpkg` source package: `libpsl=0.21.0-1.2build2`

Binary Packages:

- `libpsl5:amd64=0.21.0-1.2build2`

Licenses: (parsed from: `/usr/share/doc/libpsl5/copyright`)

- `Chromium`
- `MIT`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libseccomp=2.5.3-2ubuntu3~22.04.1`

Binary Packages:

- `libseccomp2:amd64=2.5.3-2ubuntu3~22.04.1`

Licenses: (parsed from: `/usr/share/doc/libseccomp2/copyright`)

- `LGPL-2.1`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libselinux=3.3-1build2`

Binary Packages:

- `libselinux1:amd64=3.3-1build2`

Licenses: (parsed from: `/usr/share/doc/libselinux1/copyright`)

- `GPL-2`
- `LGPL-2.1`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libsemanage=3.3-1build2`

Binary Packages:

- `libsemanage-common=3.3-1build2`
- `libsemanage2:amd64=3.3-1build2`

Licenses: (parsed from: `/usr/share/doc/libsemanage-common/copyright`, `/usr/share/doc/libsemanage2/copyright`)

- `GPL`
- `LGPL`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libsepol=3.3-1build1`

Binary Packages:

- `libsepol2:amd64=3.3-1build1`

Licenses: (parsed from: `/usr/share/doc/libsepol2/copyright`)

- `GPL`
- `LGPL`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libssh=0.9.6-2ubuntu0.22.04.7`

Binary Packages:

- `libssh-4:amd64=0.9.6-2ubuntu0.22.04.7`

Licenses: (parsed from: `/usr/share/doc/libssh-4/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `LGPL-2.1`
- `LGPL-2.1+~OpenSSL`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris libssh=0.9.6-2ubuntu0.22.04.7
'http://security.ubuntu.com/ubuntu/pool/main/libs/libssh/libssh_0.9.6-2ubuntu0.22.04.7.dsc' libssh_0.9.6-2ubuntu0.22.04.7.dsc 2750 SHA512:3acf89ed9d648f06bdbefa325719b6ac37047ee12c76bb13ae2614ed8a1795da6812652ddba1df8f6769742b93b6a2d10c70b54eb41ca13b29246914f37c7f7a
'http://security.ubuntu.com/ubuntu/pool/main/libs/libssh/libssh_0.9.6.orig.tar.xz' libssh_0.9.6.orig.tar.xz 1053056 SHA512:4040ec4af937e95be2e41313ef6d4db60b46b8d4dea10c09402398127c1d1ca8843392d207088aeee3c7ef631c6ae7b66861327dcebf78ed3af0723777619fd1
'http://security.ubuntu.com/ubuntu/pool/main/libs/libssh/libssh_0.9.6.orig.tar.xz.asc' libssh_0.9.6.orig.tar.xz.asc 833 SHA512:1b6223efe9e4ce864cd8d97d517f9f0d38c1cd502b5874fdc6a58731038c2830a72ce753f02fc062d9d4d5922107ec9a2e62fe24a704bb5dec0dcfecdb569fe6
'http://security.ubuntu.com/ubuntu/pool/main/libs/libssh/libssh_0.9.6-2ubuntu0.22.04.7.debian.tar.xz' libssh_0.9.6-2ubuntu0.22.04.7.debian.tar.xz 75780 SHA512:56afabedcd355ba0e8c9935d446c2098c098f112a7aee8d3ec2916c8638c3ca77442bb06b883e260690876a668fa41b2d7e9a83694484f5eb095f206653244e7
```

### `dpkg` source package: `libtasn1-6=4.18.0-4ubuntu0.2`

Binary Packages:

- `libtasn1-6:amd64=4.18.0-4ubuntu0.2`

Licenses: (parsed from: `/usr/share/doc/libtasn1-6/copyright`)

- `GFDL-1.3`
- `GPL-3`
- `LGPL`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libtasn1-6=4.18.0-4ubuntu0.2
'http://security.ubuntu.com/ubuntu/pool/main/libt/libtasn1-6/libtasn1-6_4.18.0-4ubuntu0.2.dsc' libtasn1-6_4.18.0-4ubuntu0.2.dsc 2777 SHA512:76f8b50124689bee4c365df96a2086d7e281a14f15ba625dd02e688c3d85643e0f55757d11aff290fbc4f1d0a418e0a73ba362833308ce67b7f3313656460d4c
'http://security.ubuntu.com/ubuntu/pool/main/libt/libtasn1-6/libtasn1-6_4.18.0.orig.tar.gz' libtasn1-6_4.18.0.orig.tar.gz 1724441 SHA512:4f2f4afc7561fda7a1f1c6c525c3c3b08228a1a4aa8c3d3d5e02e993d8f83ccee1dd0f1b201cec0fbfc97043d4b1d7a95ffd34d65422a38b85b931ac7a015831
'http://security.ubuntu.com/ubuntu/pool/main/libt/libtasn1-6/libtasn1-6_4.18.0.orig.tar.gz.asc' libtasn1-6_4.18.0.orig.tar.gz.asc 228 SHA512:8ef3918a3130f695d2d5b26dd945084b931005eff8914c50a0ac9795d4cc6ec9e9645e2941ff4235cba3b4b2987ab1c7da65225e24ce16aaab844352ecdafbf6
'http://security.ubuntu.com/ubuntu/pool/main/libt/libtasn1-6/libtasn1-6_4.18.0-4ubuntu0.2.debian.tar.xz' libtasn1-6_4.18.0-4ubuntu0.2.debian.tar.xz 25324 SHA512:81237d28d0490af47955c5d759f283f0ab2dc6d961fe18193daf406b63d4773bddd53914382d4ca061f7a6b2e4fe8dd456be88537ebe0dbe2085874b70b20737
```

### `dpkg` source package: `libtirpc=1.3.2-2ubuntu0.1`

Binary Packages:

- `libtirpc-common=1.3.2-2ubuntu0.1`
- `libtirpc3:amd64=1.3.2-2ubuntu0.1`

Licenses: (parsed from: `/usr/share/doc/libtirpc-common/copyright`, `/usr/share/doc/libtirpc3/copyright`)

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
$ apt-get source -qq --print-uris libtirpc=1.3.2-2ubuntu0.1
'http://security.ubuntu.com/ubuntu/pool/main/libt/libtirpc/libtirpc_1.3.2-2ubuntu0.1.dsc' libtirpc_1.3.2-2ubuntu0.1.dsc 2201 SHA512:da9e64904445de59217c2bfa55ca9739e0b08ac4693a45a813b7fc67273e106a11e7076d39d24e5f62d242af4e2eaac9e5503072b57f4cf7bdfa579a82920e77
'http://security.ubuntu.com/ubuntu/pool/main/libt/libtirpc/libtirpc_1.3.2.orig.tar.bz2' libtirpc_1.3.2.orig.tar.bz2 513151 SHA512:8664d5c4f842ee5acf83b9c1cadb7871f17b8157a7c4500e2236dcfb3a25768cab39f7c5123758dcd7381e30eb028ddfa26a28f458283f2dcea3426c9878c255
'http://security.ubuntu.com/ubuntu/pool/main/libt/libtirpc/libtirpc_1.3.2-2ubuntu0.1.debian.tar.xz' libtirpc_1.3.2-2ubuntu0.1.debian.tar.xz 18364 SHA512:5440c46e49837b176b8087d82762002766e48a7d487e101049079637ebb93c21fbb1dccd63a319f72ee11d7964873c00dc98a7b5b320355d640df7f9e16ab1c7
```

### `dpkg` source package: `libunistring=1.0-1`

Binary Packages:

- `libunistring2:amd64=1.0-1`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/libunistring/1.0-1/


### `dpkg` source package: `libxcrypt=1:4.4.27-1`

Binary Packages:

- `libcrypt1:amd64=1:4.4.27-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/libxcrypt/1:4.4.27-1/


### `dpkg` source package: `libzstd=1.4.8+dfsg-3build1`

Binary Packages:

- `libzstd1:amd64=1.4.8+dfsg-3build1`

Licenses: (parsed from: `/usr/share/doc/libzstd1/copyright`)

- `BSD-3-clause`
- `Expat`
- `GPL-2`
- `zlib`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `lsb=11.1.0ubuntu4`

Binary Packages:

- `lsb-base=11.1.0ubuntu4`

Licenses: (parsed from: `/usr/share/doc/lsb-base/copyright`)

- `BSD-3-clause`
- `GPL-2`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `lz4=1.9.3-2build2`

Binary Packages:

- `liblz4-1:amd64=1.9.3-2build2`

Licenses: (parsed from: `/usr/share/doc/liblz4-1/copyright`)

- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `make-dfsg=4.3-4.1build1`

Binary Packages:

- `make=4.3-4.1build1`

Licenses: (parsed from: `/usr/share/doc/make/copyright`)

- `GPL-3`
- `GPL-3+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `mawk=1.3.4.20200120-3`

Binary Packages:

- `mawk=1.3.4.20200120-3`

Licenses: (parsed from: `/usr/share/doc/mawk/copyright`)

- `GPL-2`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/mawk/1.3.4.20200120-3/


### `dpkg` source package: `media-types=7.0.0`

Binary Packages:

- `media-types=7.0.0`

Licenses: (parsed from: `/usr/share/doc/media-types/copyright`)

- `ad-hoc`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/media-types/7.0.0/


### `dpkg` source package: `mercurial=6.1.1-1ubuntu1`

Binary Packages:

- `mercurial=6.1.1-1ubuntu1`
- `mercurial-common=6.1.1-1ubuntu1`

Licenses: (parsed from: `/usr/share/doc/mercurial/copyright`, `/usr/share/doc/mercurial-common/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `mpdecimal=2.5.1-2build2`

Binary Packages:

- `libmpdec3:amd64=2.5.1-2build2`

Licenses: (parsed from: `/usr/share/doc/libmpdec3/copyright`)

- `BSD`
- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ncurses=6.3-2ubuntu0.1`

Binary Packages:

- `libncurses6:amd64=6.3-2ubuntu0.1`
- `libncursesw6:amd64=6.3-2ubuntu0.1`
- `libtinfo6:amd64=6.3-2ubuntu0.1`
- `ncurses-base=6.3-2ubuntu0.1`
- `ncurses-bin=6.3-2ubuntu0.1`

Licenses: (parsed from: `/usr/share/doc/libncurses6/copyright`, `/usr/share/doc/libncursesw6/copyright`, `/usr/share/doc/libtinfo6/copyright`, `/usr/share/doc/ncurses-base/copyright`, `/usr/share/doc/ncurses-bin/copyright`)

- `BSD-3-clause`
- `MIT/X11`
- `X11`

Source:

```console
$ apt-get source -qq --print-uris ncurses=6.3-2ubuntu0.1
'http://security.ubuntu.com/ubuntu/pool/main/n/ncurses/ncurses_6.3-2ubuntu0.1.dsc' ncurses_6.3-2ubuntu0.1.dsc 3955 SHA512:e018fe9a8a641efddfcac0e92ce46dbba3067ddc6850e7223b3abc668f1620c1ea1564d80a63b94ff1c37705630eb2116d5c4449f1115315def4d4008e5f5926
'http://security.ubuntu.com/ubuntu/pool/main/n/ncurses/ncurses_6.3.orig.tar.gz' ncurses_6.3.orig.tar.gz 3583550 SHA512:5373f228cba6b7869210384a607a2d7faecfcbfef6dbfcd7c513f4e84fbd8bcad53ac7db2e7e84b95582248c1039dcfc7c4db205a618f7da22a166db482f0105
'http://security.ubuntu.com/ubuntu/pool/main/n/ncurses/ncurses_6.3.orig.tar.gz.asc' ncurses_6.3.orig.tar.gz.asc 729 SHA512:5673088e7d6af580e8f1e163687146adb51261cd3c75be9ea61368c7590efc0e5e4bc1c2ae76d717f289ff6609089c5ca1f7e4a572266d7b6c5daba98eabed2e
'http://security.ubuntu.com/ubuntu/pool/main/n/ncurses/ncurses_6.3-2ubuntu0.1.debian.tar.xz' ncurses_6.3-2ubuntu0.1.debian.tar.xz 56080 SHA512:d37d4fc956ad1410d0338ee4f5b465e58f35056e33d909a4871d738ef83d9002200d5c31f35ee23e6817db950fd2e227a87e5e01bde8df221dfa2650edb7583a
```

### `dpkg` source package: `nettle=3.7.3-1build2`

Binary Packages:

- `libhogweed6:amd64=3.7.3-1build2`
- `libnettle8:amd64=3.7.3-1build2`

Licenses: (parsed from: `/usr/share/doc/libhogweed6/copyright`, `/usr/share/doc/libnettle8/copyright`)

- `Expat`
- `GAP`
- `GPL`
- `GPL-2`
- `GPL-2+`
- `GPL-3+`
- `GPL-3+ with Autoconf exception`
- `LGPL`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-3+`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `nghttp2=1.43.0-1ubuntu0.2`

Binary Packages:

- `libnghttp2-14:amd64=1.43.0-1ubuntu0.2`

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
$ apt-get source -qq --print-uris nghttp2=1.43.0-1ubuntu0.2
'http://security.ubuntu.com/ubuntu/pool/main/n/nghttp2/nghttp2_1.43.0-1ubuntu0.2.dsc' nghttp2_1.43.0-1ubuntu0.2.dsc 2679 SHA512:2ad7840a04e95d55fa98b6693be289fcc86330c2b9ea06b08cdf9f1bd2c3e0bffe2f312433f243ea8b7fd8ffeeba9c840581b3eb1bef662f487d075a8428ad2a
'http://security.ubuntu.com/ubuntu/pool/main/n/nghttp2/nghttp2_1.43.0.orig.tar.bz2' nghttp2_1.43.0.orig.tar.bz2 4521786 SHA512:f2e6665ad6c73f0a1a8c7b34ca821a905868d41dafca913e6a054eb5afb534a85ae91618c1a4b098e43f350ca3703fd1ece7848f0a771e8393a3eb0581ceaf59
'http://security.ubuntu.com/ubuntu/pool/main/n/nghttp2/nghttp2_1.43.0-1ubuntu0.2.debian.tar.xz' nghttp2_1.43.0-1ubuntu0.2.debian.tar.xz 23788 SHA512:ebbbd0c00089e2b48feef151b00b952cfec456662f35d8dd68e886008cdb61bec788c5fa8bbd63614c18a2e06f187bf3112417e759a4f55a9c0db27511aa461a
```

### `dpkg` source package: `npth=1.6-3build2`

Binary Packages:

- `libnpth0:amd64=1.6-3build2`

Licenses: (parsed from: `/usr/share/doc/libnpth0/copyright`)

- `LGPL-2.1`
- `LGPL-2.1+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `openldap=2.5.20+dfsg-0ubuntu0.22.04.1`

Binary Packages:

- `libldap-2.5-0:amd64=2.5.20+dfsg-0ubuntu0.22.04.1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `openssh=1:8.9p1-3ubuntu0.14`

Binary Packages:

- `openssh-client=1:8.9p1-3ubuntu0.14`

Licenses: (parsed from: `/usr/share/doc/openssh-client/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `Expat-with-advertising-restriction`
- `Mazieres-BSD-style`
- `OpenSSH`
- `Powell-BSD-style`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris openssh=1:8.9p1-3ubuntu0.14
'http://security.ubuntu.com/ubuntu/pool/main/o/openssh/openssh_8.9p1-3ubuntu0.14.dsc' openssh_8.9p1-3ubuntu0.14.dsc 3380 SHA512:bdf0aa0aeb58edc9fa8249f3485d48fc73aaf3960eabeb8b5d02d7a1f3dea1a344b3cdd5ae4433280b1b1c8870588c80fd782955302939118a8d5437c11a2b46
'http://security.ubuntu.com/ubuntu/pool/main/o/openssh/openssh_8.9p1.orig.tar.gz' openssh_8.9p1.orig.tar.gz 1820282 SHA512:04bd38ea6fe4be31acc8c4e83de7d3dda66fb7207be2e4ba25d3b8118d13d098a283769da9e8ce1fc4fba7edf739c14efcc6c9137132919261a7f882314b0f6b
'http://security.ubuntu.com/ubuntu/pool/main/o/openssh/openssh_8.9p1.orig.tar.gz.asc' openssh_8.9p1.orig.tar.gz.asc 833 SHA512:fd0bbd285ff2f8791f5a512f087f32bce026b716d5ac213cd4ef28f08722601fb943514bee71b2ac4b9f9363e2f120ce6c60fed952d1d8e53dbcf2a6fe2e706b
'http://security.ubuntu.com/ubuntu/pool/main/o/openssh/openssh_8.9p1-3ubuntu0.14.debian.tar.xz' openssh_8.9p1-3ubuntu0.14.debian.tar.xz 202080 SHA512:58791f38bd28fc16e74b4adcb38ba8fa4d55d154ee7c358e2142db8122e21490ecc75026acedc3b20a182737c94eb18bb552508903ebf4a5be3b5c44d6aed22b
```

### `dpkg` source package: `openssl=3.0.2-0ubuntu1.23`

Binary Packages:

- `libssl3:amd64=3.0.2-0ubuntu1.23`
- `openssl=3.0.2-0ubuntu1.23`

Licenses: (parsed from: `/usr/share/doc/libssl3/copyright`, `/usr/share/doc/openssl/copyright`)

- `Apache-2.0`
- `Artistic`
- `GPL-1`
- `GPL-1+`

Source:

```console
$ apt-get source -qq --print-uris openssl=3.0.2-0ubuntu1.23
'http://security.ubuntu.com/ubuntu/pool/main/o/openssl/openssl_3.0.2-0ubuntu1.23.dsc' openssl_3.0.2-0ubuntu1.23.dsc 2730 SHA512:63c782499d5cee71f4d999ae0581c3b1f3ccc6f68b0147e1e3487c2dcd43e83c420b9a3d9bbf305ec6ed39f7dfc73e2386c2a5d89adc46878d8a36dd53d1d431
'http://security.ubuntu.com/ubuntu/pool/main/o/openssl/openssl_3.0.2.orig.tar.gz' openssl_3.0.2.orig.tar.gz 15038141 SHA512:f986850d5be908b4d6b5fd7091bc4652d7378c9bccebfbc5becd7753843c04c1eb61a1749c432139d263dfac33df0b1f6c773664b485cad47542266823a4eb03
'http://security.ubuntu.com/ubuntu/pool/main/o/openssl/openssl_3.0.2.orig.tar.gz.asc' openssl_3.0.2.orig.tar.gz.asc 488 SHA512:4303391a58107c76ad9b05510f5bfc95f687f4cb2f9ff5b03fb262ba99b573423ab83f0437471199954496799b343191b889ad9ef8fabdd7ee4ec3ec9b5f1d81
'http://security.ubuntu.com/ubuntu/pool/main/o/openssl/openssl_3.0.2-0ubuntu1.23.debian.tar.xz' openssl_3.0.2-0ubuntu1.23.debian.tar.xz 277852 SHA512:1de5b111ad19a4d0400c2195574737293a83a23d4f79ca44e86f09e8438f879d29888be39455f7483fdaf8a9314841ffb9511ace908813e7f849c4d98af53562
```

### `dpkg` source package: `p11-kit=0.24.0-6build1`

Binary Packages:

- `libp11-kit0:amd64=0.24.0-6build1`
- `p11-kit=0.24.0-6build1`
- `p11-kit-modules:amd64=0.24.0-6build1`

Licenses: (parsed from: `/usr/share/doc/libp11-kit0/copyright`, `/usr/share/doc/p11-kit/copyright`, `/usr/share/doc/p11-kit-modules/copyright`)

- `Apache-2.0`
- `BSD-3-Clause`
- `ISC`
- `ISC+IBM`
- `LGPL-2.1`
- `LGPL-2.1+`
- `permissive-like-automake-output`
- `same-as-rest-of-p11kit`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `pam=1.4.0-11ubuntu2.6`

Binary Packages:

- `libpam-modules:amd64=1.4.0-11ubuntu2.6`
- `libpam-modules-bin=1.4.0-11ubuntu2.6`
- `libpam-runtime=1.4.0-11ubuntu2.6`
- `libpam0g:amd64=1.4.0-11ubuntu2.6`

Licenses: (parsed from: `/usr/share/doc/libpam-modules/copyright`, `/usr/share/doc/libpam-modules-bin/copyright`, `/usr/share/doc/libpam-runtime/copyright`, `/usr/share/doc/libpam0g/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris pam=1.4.0-11ubuntu2.6
'http://security.ubuntu.com/ubuntu/pool/main/p/pam/pam_1.4.0-11ubuntu2.6.dsc' pam_1.4.0-11ubuntu2.6.dsc 2728 SHA512:18bfb2e4093ba1ef97a0ab9206a273c7180a607f3709567e72e5968b8d20999960869d6bbf806413066a1ba6c0dd64717015c5c20e83fb7cad31171b0e1a766e
'http://security.ubuntu.com/ubuntu/pool/main/p/pam/pam_1.4.0.orig.tar.xz' pam_1.4.0.orig.tar.xz 988908 SHA512:26eda95c45598a500bc142da4d1abf93d03b3bbb0f2390fa87c72dcbffa208dbfa115c0b411095c31ee9955e36422ccf3e2df3bd486818fafffef8c4310798c4
'http://security.ubuntu.com/ubuntu/pool/main/p/pam/pam_1.4.0-11ubuntu2.6.debian.tar.xz' pam_1.4.0-11ubuntu2.6.debian.tar.xz 187648 SHA512:5e2fe17f27a9fcc30940738efc3d8e0dc72bf2d8c9ab5bf8ecd508151ff00eb29e133d21980fe6c0acf24e201fc84af88b9134017747883c40ec78cdc7e306ae
```

### `dpkg` source package: `patiencediff=0.2.1-1build3`

Binary Packages:

- `python3-patiencediff=0.2.1-1build3`

Licenses: (parsed from: `/usr/share/doc/python3-patiencediff/copyright`)

- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `pcre2=10.39-3ubuntu0.1`

Binary Packages:

- `libpcre2-8-0:amd64=10.39-3ubuntu0.1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris pcre2=10.39-3ubuntu0.1
'http://security.ubuntu.com/ubuntu/pool/main/p/pcre2/pcre2_10.39-3ubuntu0.1.dsc' pcre2_10.39-3ubuntu0.1.dsc 2142 SHA512:8f062a4ba129491e0ec755f945b84e6e6d252e4d87b87ae0dc46156320095557093f7c3305a31cbca9252a2cbc172d701606030ebdae147eef3fbd5616b4ed99
'http://security.ubuntu.com/ubuntu/pool/main/p/pcre2/pcre2_10.39.orig.tar.gz' pcre2_10.39.orig.tar.gz 2309964 SHA512:fe17ea0191a91d4e4fe88a44a07883db594941376a6e38556e03ff3b594820596fd3e43be2d73b700ca68cd0c44e38c33cc891a57b8ed65e34cd832196bc09b2
'http://security.ubuntu.com/ubuntu/pool/main/p/pcre2/pcre2_10.39-3ubuntu0.1.diff.gz' pcre2_10.39-3ubuntu0.1.diff.gz 11214 SHA512:7b8848adbd237351d14e68cf13d26fe0330718d2e807c69b091d2eefdd4c5f4ebde9e3b403d898b52ffcff674eb6bd0ff6995190c1fc42668e4bf8173ded7f14
```

### `dpkg` source package: `pcre3=2:8.39-13ubuntu0.22.04.1`

Binary Packages:

- `libpcre3:amd64=2:8.39-13ubuntu0.22.04.1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris pcre3=2:8.39-13ubuntu0.22.04.1
'http://security.ubuntu.com/ubuntu/pool/main/p/pcre3/pcre3_8.39-13ubuntu0.22.04.1.dsc' pcre3_8.39-13ubuntu0.22.04.1.dsc 2101 SHA512:c2b619e559192c367485fec01cf65dbc49a67ec8f2fb9d5785fdf7dba052540d70c16b4316afc83f4765ef9b57f3e2c0e6f245500866476df8a8a90310584f62
'http://security.ubuntu.com/ubuntu/pool/main/p/pcre3/pcre3_8.39.orig.tar.bz2' pcre3_8.39.orig.tar.bz2 1560758 SHA512:8b0f14ae5947c4b2d74876a795b04e532fd71c2479a64dbe0ed817e7c7894ea3cae533413de8c17322d305cb7f4e275d72b43e4e828eaca77dc4bcaf04529cf6
'http://security.ubuntu.com/ubuntu/pool/main/p/pcre3/pcre3_8.39-13ubuntu0.22.04.1.debian.tar.gz' pcre3_8.39-13ubuntu0.22.04.1.debian.tar.gz 28251 SHA512:50aa437187fd45632213fe7b09a69dfbe2a58ad568a7f71c47ddab204db49850b732f17c8295788afd0c58d8134620a11aaa9fa259a980a0ab85ce043098a659
```

### `dpkg` source package: `perl=5.34.0-3ubuntu1.5`

Binary Packages:

- `libperl5.34:amd64=5.34.0-3ubuntu1.5`
- `perl=5.34.0-3ubuntu1.5`
- `perl-base=5.34.0-3ubuntu1.5`
- `perl-modules-5.34=5.34.0-3ubuntu1.5`

Licenses: (parsed from: `/usr/share/doc/libperl5.34/copyright`, `/usr/share/doc/perl/copyright`, `/usr/share/doc/perl-base/copyright`, `/usr/share/doc/perl-modules-5.34/copyright`)

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
$ apt-get source -qq --print-uris perl=5.34.0-3ubuntu1.5
'http://security.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.34.0-3ubuntu1.5.dsc' perl_5.34.0-3ubuntu1.5.dsc 2976 SHA512:e490cfc45a24fa7538f5a92054a19a52fd9675fe7a7e6e0e20b7a6c3e6939ec0cf1b39e71f2daebb8e5ab0968d851fdf1b713166d6855968fb47e846d7350020
'http://security.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.34.0.orig-regen-configure.tar.xz' perl_5.34.0.orig-regen-configure.tar.xz 415412 SHA512:2581152e0747105314c4fa4167f1f97d286436b996341b9b75e4099ba18f15eb0d2b42888622fbe9b5499d3fe304bc8aa9ad207a945f590135beccfb68ea28b0
'http://security.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.34.0.orig.tar.xz' perl_5.34.0.orig.tar.xz 12881416 SHA512:691b4b31eacec357191fba777612b4e3eae59e946a22998a50766697c0d61db1d42a9b3bc1e41abf0d1ca1893e4a7c06d7bf3290480cf03d7f79befd7a8a3267
'http://security.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.34.0-3ubuntu1.5.debian.tar.xz' perl_5.34.0-3ubuntu1.5.debian.tar.xz 200524 SHA512:bb565b5ee511cd73dccf9b596f356fd4d4a32dcd5a584fa73e806322a541706d6940c54732d20d6eb1fcc0bac06fcef5a98f5f6a592b83b12a8ada3157dfdc6f
```

### `dpkg` source package: `pinentry=1.1.1-1build2`

Binary Packages:

- `pinentry-curses=1.1.1-1build2`

Licenses: (parsed from: `/usr/share/doc/pinentry-curses/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-3`
- `LGPL-3+`
- `X11`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `procps=2:3.3.17-6ubuntu2.1`

Binary Packages:

- `libprocps8:amd64=2:3.3.17-6ubuntu2.1`
- `procps=2:3.3.17-6ubuntu2.1`

Licenses: (parsed from: `/usr/share/doc/libprocps8/copyright`, `/usr/share/doc/procps/copyright`)

- `GPL-2`
- `GPL-2.0+`
- `LGPL-2`
- `LGPL-2.0+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris procps=2:3.3.17-6ubuntu2.1
'http://security.ubuntu.com/ubuntu/pool/main/p/procps/procps_3.3.17-6ubuntu2.1.dsc' procps_3.3.17-6ubuntu2.1.dsc 2111 SHA512:585933efef8d8e93b4187c65b678d146960480386ac3172097c790723ffadbf1d5347e05cc6de2682adcb96dd5b45ec1f98a3e00cff33ad2b30f729939896aca
'http://security.ubuntu.com/ubuntu/pool/main/p/procps/procps_3.3.17.orig.tar.xz' procps_3.3.17.orig.tar.xz 1008428 SHA512:59e9a5013430fd9da508c4655d58375dc32e025bb502bb28fb9a92a48e4f2838b3355e92b4648f7384b2050064d17079bf4595d889822ebb5030006bc154a1a7
'http://security.ubuntu.com/ubuntu/pool/main/p/procps/procps_3.3.17-6ubuntu2.1.debian.tar.xz' procps_3.3.17-6ubuntu2.1.debian.tar.xz 35488 SHA512:720a52d14be82aecd59e2456fbb19574c99cc5281660a36994ef4aa619c14bbec43fd30b5e949446e5db6b6bebf8003a5f173298fe8bf56ac949d61ad0225a79
```

### `dpkg` source package: `python-certifi=2020.6.20-1`

Binary Packages:

- `python3-certifi=2020.6.20-1`

Licenses: (parsed from: `/usr/share/doc/python3-certifi/copyright`)

- `GPL-2`
- `MPL-2`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/python-certifi/2020.6.20-1/


### `dpkg` source package: `python-fastbencode=0.0.5-1build1`

Binary Packages:

- `python3-fastbencode=0.0.5-1build1`

Licenses: (parsed from: `/usr/share/doc/python3-fastbencode/copyright`)

- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python-urllib3=1.26.5-1~exp1ubuntu0.6`

Binary Packages:

- `python3-urllib3=1.26.5-1~exp1ubuntu0.6`

Licenses: (parsed from: `/usr/share/doc/python3-urllib3/copyright`)

- `Expat`
- `PSF-2`

Source:

```console
$ apt-get source -qq --print-uris python-urllib3=1.26.5-1~exp1ubuntu0.6
'http://security.ubuntu.com/ubuntu/pool/main/p/python-urllib3/python-urllib3_1.26.5-1%7eexp1ubuntu0.6.dsc' python-urllib3_1.26.5-1~exp1ubuntu0.6.dsc 2378 SHA512:226667a5b8bb0207862284fad2c128ec282461e907ff86ed56493da05f98a6c0552c41f362fe5902c6cf7d8be2cde6e32feb3503a94c59efdd943d29ee5434ad
'http://security.ubuntu.com/ubuntu/pool/main/p/python-urllib3/python-urllib3_1.26.5.orig.tar.gz' python-urllib3_1.26.5.orig.tar.gz 292865 SHA512:4a1899b223b00894d49f6dff5fc95d410e5b0ab28c11f7e3cd82d03e50438b0c5b0adf693a33fd80f1586312dc0012836713998674da15531bf82d52645881f6
'http://security.ubuntu.com/ubuntu/pool/main/p/python-urllib3/python-urllib3_1.26.5-1%7eexp1ubuntu0.6.debian.tar.xz' python-urllib3_1.26.5-1~exp1ubuntu0.6.debian.tar.xz 19228 SHA512:52ec174053aa17d372b8d1c4e4e1769c9a282a97ea337d3b19e5bffa78e777540b53fcdce830b863fae516380a1b5bb6ea20f63504380e84c0cda35b18e56317
```

### `dpkg` source package: `python3-defaults=3.10.6-1~22.04.1`

Binary Packages:

- `libpython3-stdlib:amd64=3.10.6-1~22.04.1`
- `python3=3.10.6-1~22.04.1`
- `python3-minimal=3.10.6-1~22.04.1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3.10=3.10.12-1~22.04.15`

Binary Packages:

- `libpython3.10-minimal:amd64=3.10.12-1~22.04.15`
- `libpython3.10-stdlib:amd64=3.10.12-1~22.04.15`
- `python3.10=3.10.12-1~22.04.15`
- `python3.10-minimal=3.10.12-1~22.04.15`

Licenses: (parsed from: `/usr/share/doc/libpython3.10-minimal/copyright`, `/usr/share/doc/libpython3.10-stdlib/copyright`, `/usr/share/doc/python3.10/copyright`, `/usr/share/doc/python3.10-minimal/copyright`)

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
$ apt-get source -qq --print-uris python3.10=3.10.12-1~22.04.15
'http://security.ubuntu.com/ubuntu/pool/main/p/python3.10/python3.10_3.10.12-1%7e22.04.15.dsc' python3.10_3.10.12-1~22.04.15.dsc 3110 SHA512:8ea2ec7063033873b4f53f039578d9de318b61240db5dc13a6e947803681d9bd66da508fa4d2a78ad89cf3715ffb9a57c046a89b1d1e674433e7c14a20875012
'http://security.ubuntu.com/ubuntu/pool/main/p/python3.10/python3.10_3.10.12.orig.tar.xz' python3.10_3.10.12.orig.tar.xz 19654836 SHA512:5ea018e71bfe7872e02eaf8aef56d5583c0880e4ce5fbbdf8ea76da20c2e94ac6a3ba8badb4b7d1bc21853402a3b63541b04181737417b1626e786b696595cf5
'http://security.ubuntu.com/ubuntu/pool/main/p/python3.10/python3.10_3.10.12-1%7e22.04.15.debian.tar.xz' python3.10_3.10.12-1~22.04.15.debian.tar.xz 269472 SHA512:8c46f573b40044406a8d596fdd3991139350eb86257c65ca01744f2f9504c4e4070302de52938a48272a56bfdbb676eee19756b719c1ed372f93a5b79335b80f
```

### `dpkg` source package: `readline=8.1.2-1`

Binary Packages:

- `libreadline8:amd64=8.1.2-1`
- `readline-common=8.1.2-1`

Licenses: (parsed from: `/usr/share/doc/libreadline8/copyright`, `/usr/share/doc/readline-common/copyright`)

- `GFDL`
- `GPL-3`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/readline/8.1.2-1/


### `dpkg` source package: `rtmpdump=2.4+20151223.gitfa8646d.1-2build4`

Binary Packages:

- `librtmp1:amd64=2.4+20151223.gitfa8646d.1-2build4`

Licenses: (parsed from: `/usr/share/doc/librtmp1/copyright`)

- `GPL-2`
- `LGPL-2.1`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `sed=4.8-1ubuntu2`

Binary Packages:

- `sed=4.8-1ubuntu2`

Licenses: (parsed from: `/usr/share/doc/sed/copyright`)

- `GPL-3`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `sensible-utils=0.0.17`

Binary Packages:

- `sensible-utils=0.0.17`

Licenses: (parsed from: `/usr/share/doc/sensible-utils/copyright`)

- `All-permissive`
- `GPL-2`
- `GPL-2+`
- `configure`
- `installsh`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/sensible-utils/0.0.17/


### `dpkg` source package: `serf=1.3.9-10ubuntu2`

Binary Packages:

- `libserf-1-1:amd64=1.3.9-10ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libserf-1-1/copyright`)

- `Apache`
- `Apache-2.0`
- `Zlib`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `shadow=1:4.8.1-2ubuntu2.2`

Binary Packages:

- `login=1:4.8.1-2ubuntu2.2`
- `passwd=1:4.8.1-2ubuntu2.2`

Licenses: (parsed from: `/usr/share/doc/login/copyright`, `/usr/share/doc/passwd/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris shadow=1:4.8.1-2ubuntu2.2
'http://security.ubuntu.com/ubuntu/pool/main/s/shadow/shadow_4.8.1-2ubuntu2.2.dsc' shadow_4.8.1-2ubuntu2.2.dsc 2060 SHA512:765de71da656f0fd36b0872e05c1f736b167faf3af9a52247e0810d260606fe440a541c5558a882f8a5d150d91f76f01303cada28ba5febe4d16042eda3da7c8
'http://security.ubuntu.com/ubuntu/pool/main/s/shadow/shadow_4.8.1.orig.tar.xz' shadow_4.8.1.orig.tar.xz 1611196 SHA512:780a983483d847ed3c91c82064a0fa902b6f4185225978241bc3bc03fcc3aa143975b46aee43151c6ba43efcfdb1819516b76ba7ad3d1d3c34fcc38ea42e917b
'http://security.ubuntu.com/ubuntu/pool/main/s/shadow/shadow_4.8.1-2ubuntu2.2.debian.tar.xz' shadow_4.8.1-2ubuntu2.2.debian.tar.xz 98488 SHA512:dfa83a48e365f57c4881e77307bdea56db3e1b78e28ae687e5346daf1e71fe8df3388329ef6e7c90377555367267719e42e9c7f752da5b897e731bd9ca50a581
```

### `dpkg` source package: `six=1.16.0-3ubuntu1`

Binary Packages:

- `python3-six=1.16.0-3ubuntu1`

Licenses: (parsed from: `/usr/share/doc/python3-six/copyright`)

- `Expat`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `sqlite3=3.37.2-2ubuntu0.5`

Binary Packages:

- `libsqlite3-0:amd64=3.37.2-2ubuntu0.5`

Licenses: (parsed from: `/usr/share/doc/libsqlite3-0/copyright`)

- `GPL-2`
- `GPL-2+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris sqlite3=3.37.2-2ubuntu0.5
'http://security.ubuntu.com/ubuntu/pool/main/s/sqlite3/sqlite3_3.37.2-2ubuntu0.5.dsc' sqlite3_3.37.2-2ubuntu0.5.dsc 2602 SHA512:fb731fd5ca44dbfa72f1b685980fc3cc66379f63fe0220460897f142eb91d43f81a2c1180864695157b764c22787621c958b0c2448d7ab820c1638cc7ad5f97d
'http://security.ubuntu.com/ubuntu/pool/main/s/sqlite3/sqlite3_3.37.2.orig-www.tar.xz' sqlite3_3.37.2.orig-www.tar.xz 5694016 SHA512:577e34b4ae18a3c73be6d955a2e2321e993f61decefbcca5112170072ea556eca93dcf55f3059fbcd96147124442b368150de7f68c603e84b80cbe0228ae78f8
'http://security.ubuntu.com/ubuntu/pool/main/s/sqlite3/sqlite3_3.37.2.orig.tar.xz' sqlite3_3.37.2.orig.tar.xz 7623768 SHA512:dfa51b0a32ab0597cd00ae7abdb53bb255102f397ff8409f3fdbefaad17bc7d5a25f53db90bed47feb1bf4a9a1a4707bc40440c6c5303f3ef5c49ded61558fed
'http://security.ubuntu.com/ubuntu/pool/main/s/sqlite3/sqlite3_3.37.2-2ubuntu0.5.debian.tar.xz' sqlite3_3.37.2-2ubuntu0.5.debian.tar.xz 33900 SHA512:47c8ee60e8f1b05eb8156a58ea6e909755895df5db9a7381fa8c9f79e7bd6b9a5e6d8f3fd39446d371485ac5feff5b4ac28ff97b4cea92de912de15b7c728e26
```

### `dpkg` source package: `subversion=1.14.1-3ubuntu0.22.04.1`

Binary Packages:

- `libsvn1:amd64=1.14.1-3ubuntu0.22.04.1`
- `subversion=1.14.1-3ubuntu0.22.04.1`

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
$ apt-get source -qq --print-uris subversion=1.14.1-3ubuntu0.22.04.1
'http://security.ubuntu.com/ubuntu/pool/universe/s/subversion/subversion_1.14.1-3ubuntu0.22.04.1.dsc' subversion_1.14.1-3ubuntu0.22.04.1.dsc 3362 SHA512:a9b308801753c35a0f2a69b3ba95a5b2e548f36613c76c31755f207fc9479af40b72f9f5e1a13490a6ee2efbd63288b308d7bb27853cc8070beca57238ad06a5
'http://security.ubuntu.com/ubuntu/pool/universe/s/subversion/subversion_1.14.1.orig.tar.gz' subversion_1.14.1.orig.tar.gz 11534165 SHA512:6cd780f6669c811264de03b94ea41487111957dfd817498699c91e5dbb975e4b9626de9c436c5722fd6a6fadc4fef35f51905c2c0f5fd4955cf0fadef9cba60e
'http://security.ubuntu.com/ubuntu/pool/universe/s/subversion/subversion_1.14.1.orig.tar.gz.asc' subversion_1.14.1.orig.tar.gz.asc 1288 SHA512:56f3b3ae63e10c503b741107261da955088749845693b34125f8e61c7850035021684b31944e99ed50628cc4f601081627c1472f83f8196eac3a289038a842f9
'http://security.ubuntu.com/ubuntu/pool/universe/s/subversion/subversion_1.14.1-3ubuntu0.22.04.1.debian.tar.xz' subversion_1.14.1-3ubuntu0.22.04.1.debian.tar.xz 432564 SHA512:622d2212a418ea1927e826ea82948ddd8693061fd6cfcf69b988fcaf0c8c3065a982d09e7fac0b629ca63d191f54d896b37bf69a761e68ddd7b4ac781e2d31e0
```

### `dpkg` source package: `systemd=249.11-0ubuntu3.20`

Binary Packages:

- `libsystemd0:amd64=249.11-0ubuntu3.20`
- `libudev1:amd64=249.11-0ubuntu3.20`

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


### `dpkg` source package: `sysvinit=3.01-1ubuntu1`

Binary Packages:

- `sysvinit-utils=3.01-1ubuntu1`

Licenses: (parsed from: `/usr/share/doc/sysvinit-utils/copyright`)

- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `tar=1.34+dfsg-1ubuntu0.1.22.04.2`

Binary Packages:

- `tar=1.34+dfsg-1ubuntu0.1.22.04.2`

Licenses: (parsed from: `/usr/share/doc/tar/copyright`)

- `GPL-2`
- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris tar=1.34+dfsg-1ubuntu0.1.22.04.2
'http://security.ubuntu.com/ubuntu/pool/main/t/tar/tar_1.34%2bdfsg-1ubuntu0.1.22.04.2.dsc' tar_1.34+dfsg-1ubuntu0.1.22.04.2.dsc 1829 SHA512:e716a22f84cf0ebc0250a4ebb5d7c1fb5f055470a376c20d37a9378e85535aba8d547b6fe64df17bdedd5130d47647613dd5f2083f93cae934961b1b5ba37077
'http://security.ubuntu.com/ubuntu/pool/main/t/tar/tar_1.34%2bdfsg.orig.tar.xz' tar_1.34+dfsg.orig.tar.xz 1981736 SHA512:ec5553c53c4a5f523f872a8095f699c17bf41400fbe2f0f8b45291ccbaf9ac51dea8445c81bd95697f8853c95dcad3250071d23dbbcab857a428ee92e647bde9
'http://security.ubuntu.com/ubuntu/pool/main/t/tar/tar_1.34%2bdfsg-1ubuntu0.1.22.04.2.debian.tar.xz' tar_1.34+dfsg-1ubuntu0.1.22.04.2.debian.tar.xz 20544 SHA512:9840407a1364154c831665c3f1739c80a84806567fe5ad27ee3ac70f4c18e27d7f2f9e0557b6e2a634ab39449a8fc95b96f1813f5c203df8ece5226a6afe8c7c
```

### `dpkg` source package: `tzdata=2026a-0ubuntu0.22.04.1`

Binary Packages:

- `tzdata=2026a-0ubuntu0.22.04.1`

Licenses: (parsed from: `/usr/share/doc/tzdata/copyright`)

- `ICU`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ubuntu-keyring=2021.03.26`

Binary Packages:

- `ubuntu-keyring=2021.03.26`

Licenses: (parsed from: `/usr/share/doc/ubuntu-keyring/copyright`)

- `GPL`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ucf=3.0043`

Binary Packages:

- `ucf=3.0043`

Licenses: (parsed from: `/usr/share/doc/ucf/copyright`)

- `GPL-2`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/ucf/3.0043/


### `dpkg` source package: `unzip=6.0-26ubuntu3.2`

Binary Packages:

- `unzip=6.0-26ubuntu3.2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `usrmerge=25ubuntu2`

Binary Packages:

- `usrmerge=25ubuntu2`

Licenses: (parsed from: `/usr/share/doc/usrmerge/copyright`)

- `GPL v2`
- `GPL-2`
- `later (please see /usr/share/common-licenses/GPL-2)`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `utf8proc=2.7.0-3`

Binary Packages:

- `libutf8proc2:amd64=2.7.0-3`

Licenses: (parsed from: `/usr/share/doc/libutf8proc2/copyright`)

- `Expat`
- `Unicode`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/utf8proc/2.7.0-3/


### `dpkg` source package: `util-linux=2.37.2-4ubuntu3.5`

Binary Packages:

- `bsdutils=1:2.37.2-4ubuntu3.5`
- `libblkid1:amd64=2.37.2-4ubuntu3.5`
- `libmount1:amd64=2.37.2-4ubuntu3.5`
- `libsmartcols1:amd64=2.37.2-4ubuntu3.5`
- `libuuid1:amd64=2.37.2-4ubuntu3.5`
- `mount=2.37.2-4ubuntu3.5`
- `util-linux=2.37.2-4ubuntu3.5`

Licenses: (parsed from: `/usr/share/doc/bsdutils/copyright`, `/usr/share/doc/libblkid1/copyright`, `/usr/share/doc/libmount1/copyright`, `/usr/share/doc/libsmartcols1/copyright`, `/usr/share/doc/libuuid1/copyright`, `/usr/share/doc/mount/copyright`, `/usr/share/doc/util-linux/copyright`)

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
$ apt-get source -qq --print-uris util-linux=2.37.2-4ubuntu3.5
'http://security.ubuntu.com/ubuntu/pool/main/u/util-linux/util-linux_2.37.2-4ubuntu3.5.dsc' util-linux_2.37.2-4ubuntu3.5.dsc 4550 SHA512:c4236797fd341679e55cf4137c5c48a1dcd22975b1f5787b1ec0fa539f3f3d7dfe559601f26501fe1227e87f623cde6e8d299ff34580bd4d25d8862e83fbecb7
'http://security.ubuntu.com/ubuntu/pool/main/u/util-linux/util-linux_2.37.2.orig.tar.xz' util-linux_2.37.2.orig.tar.xz 5621624 SHA512:38f0fe820445e3bfa79550e6581c230f98c7661566ccc4daa51c7208a5f972c61b4e57dfc86bed074fdbc7c40bc79f856be8f6a05a8860c1c0cecc4208e8b81d
'http://security.ubuntu.com/ubuntu/pool/main/u/util-linux/util-linux_2.37.2-4ubuntu3.5.debian.tar.xz' util-linux_2.37.2-4ubuntu3.5.debian.tar.xz 115268 SHA512:e0cd54819b53c5787ad0f96caea67ecaf6264a656f534296487bcfd2af520c51918aef8694294602aa899808a9dc76de3d69f138b16b23170f500b2ef92db242
```

### `dpkg` source package: `wget=1.21.2-2ubuntu1.1`

Binary Packages:

- `wget=1.21.2-2ubuntu1.1`

Licenses: (parsed from: `/usr/share/doc/wget/copyright`)

- `GFDL-1.2`
- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris wget=1.21.2-2ubuntu1.1
'http://security.ubuntu.com/ubuntu/pool/main/w/wget/wget_1.21.2-2ubuntu1.1.dsc' wget_1.21.2-2ubuntu1.1.dsc 2251 SHA512:66aa1cecef80eacb8780fdec1ba9a237e36796a22cfc3fcf4b1b095d2dbd98852c4557e3084dd45022154b4c01d8c9e980dac9239a2e27c717a75413513f8171
'http://security.ubuntu.com/ubuntu/pool/main/w/wget/wget_1.21.2.orig.tar.gz' wget_1.21.2.orig.tar.gz 5004576 SHA512:3e35f92604486ca459f26df97d392579f1d83a9254519e8ce249b410bacf70dddf716d6caa3b29fd4865163f60410b2b8ad1ca1f7bb3dbb2456386b7647b988d
'http://security.ubuntu.com/ubuntu/pool/main/w/wget/wget_1.21.2.orig.tar.gz.asc' wget_1.21.2.orig.tar.gz.asc 833 SHA512:c5349ed20902d4e4d76e681b9e14370d5c1f07d1ba9e600a82af67ac24fe79051b3beabbe563e6967c429cc344ee1bc46aff57c1ab0eb2db8d70e907df49c953
'http://security.ubuntu.com/ubuntu/pool/main/w/wget/wget_1.21.2-2ubuntu1.1.debian.tar.xz' wget_1.21.2-2ubuntu1.1.debian.tar.xz 65124 SHA512:1351dc5b7271f9e5cbf85bc0bbfe36b1645b0dfa4de20940e1dc20c297b43b540c958e4908c54f6e3663fc0d1e6094c1dffb7609ca8baebb842659886f1bdf97
```

### `dpkg` source package: `xxhash=0.8.1-1`

Binary Packages:

- `libxxhash0:amd64=0.8.1-1`

Licenses: (parsed from: `/usr/share/doc/libxxhash0/copyright`)

- `BSD-2-clause`
- `GPL-2`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/xxhash/0.8.1-1/


### `dpkg` source package: `xz-utils=5.2.5-2ubuntu1`

Binary Packages:

- `liblzma5:amd64=5.2.5-2ubuntu1`

Licenses: (parsed from: `/usr/share/doc/liblzma5/copyright`)

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `zlib=1:1.2.11.dfsg-2ubuntu9.2`

Binary Packages:

- `zlib1g:amd64=1:1.2.11.dfsg-2ubuntu9.2`

Licenses: (parsed from: `/usr/share/doc/zlib1g/copyright`)

- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris zlib=1:1.2.11.dfsg-2ubuntu9.2
'http://security.ubuntu.com/ubuntu/pool/main/z/zlib/zlib_1.2.11.dfsg-2ubuntu9.2.dsc' zlib_1.2.11.dfsg-2ubuntu9.2.dsc 2649 SHA512:08f3ca4c6680ddec9532de5e937c39aa891e1c2062e6da65a96aaa060c8111bbb63de6d5c36efd34f4d3892e6e334b50fa2947fde68b3ba276e6645027dd8715
'http://security.ubuntu.com/ubuntu/pool/main/z/zlib/zlib_1.2.11.dfsg.orig.tar.gz' zlib_1.2.11.dfsg.orig.tar.gz 370248 SHA512:92819807c0b8de655021bb2d5d182f9b6b381d3072d8c8dc1df34bbaa25d36bcba140c85f754a43cc466aac65850b7a7366aa0c93e804180e5b255e61d5748de
'http://security.ubuntu.com/ubuntu/pool/main/z/zlib/zlib_1.2.11.dfsg-2ubuntu9.2.debian.tar.xz' zlib_1.2.11.dfsg-2ubuntu9.2.debian.tar.xz 60140 SHA512:5e86b01c08d5027fab6682849e6065b750d2aecafe8bd6ca85fd729c1cca88031e46f869e20d0b0483d2a6128eab9754f530d0b25f009b684b18bd6f0e8c4ae8
```
