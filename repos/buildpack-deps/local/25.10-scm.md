# `buildpack-deps:questing-scm`

## Docker Metadata

- Image ID: `sha256:c3f22bbd54ba81e7559df43016989392b1e6638694902af1667da7efde0b645e`
- Created: `2025-05-19T22:25:54Z`
- Virtual Size: ~ 271.43 Mb  
  (total size of all layers on-disk)
- Arch: `linux`/`amd64`
- Command: `["/bin/bash"]`
- Environment:
  - `PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin`
- Labels:
  - `org.opencontainers.image.ref.name=ubuntu`
  - `org.opencontainers.image.version=25.10`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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

### `dpkg` source package: `apt=3.1.0ubuntu3`

Binary Packages:

- `apt=3.1.0ubuntu3`
- `libapt-pkg7.0:amd64=3.1.0ubuntu3`

Licenses: (parsed from: `/usr/share/doc/apt/copyright`, `/usr/share/doc/libapt-pkg7.0/copyright`)

- `BSD-3-clause`
- `Expat`
- `GPL-2`
- `GPL-2+`
- `curl`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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
'http://archive.ubuntu.com/ubuntu/pool/main/a/attr/attr_2.5.2-3.dsc' attr_2.5.2-3.dsc 2576 SHA512:042c7034d0c3273b4e6a4485b25e6f7591af0382b3aa2f47e37e840ec12ef023d453fe93281bc95279243d8888d5faa37b141db2890df0a7004967776e519374
'http://archive.ubuntu.com/ubuntu/pool/main/a/attr/attr_2.5.2.orig.tar.xz' attr_2.5.2.orig.tar.xz 334180 SHA512:f587ea544effb7cfed63b3027bf14baba2c2dbe3a9b6c0c45fc559f7e8cb477b3e9a4a826eae30f929409468c50d11f3e7dc6d2500f41e1af8662a7e96a30ef3
'http://archive.ubuntu.com/ubuntu/pool/main/a/attr/attr_2.5.2.orig.tar.xz.asc' attr_2.5.2.orig.tar.xz.asc 833 SHA512:16362013313d055dec307bcf755a9846f5153a78309a499f8cac4ff57a2154de2bc8f3b1400e81dba7a0bf0c67aa02a5d464898ed6e4aa721b64ec95fd313968
'http://archive.ubuntu.com/ubuntu/pool/main/a/attr/attr_2.5.2-3.debian.tar.xz' attr_2.5.2-3.debian.tar.xz 32260 SHA512:9507aab496510a3d13feaa4dc4ae0e7837b9cd8a57d0198db2efd24c5a90ee1af1e9c1bd2e3df232f5e6c0c6be25874517bdcc668b7bc893fca6157a4723c8ef
```

### `dpkg` source package: `audit=1:4.0.2-2ubuntu2`

Binary Packages:

- `libaudit-common=1:4.0.2-2ubuntu2`
- `libaudit1:amd64=1:4.0.2-2ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libaudit-common/copyright`, `/usr/share/doc/libaudit1/copyright`)

- `GPL-1`
- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris audit=1:4.0.2-2ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/a/audit/audit_4.0.2-2ubuntu2.dsc' audit_4.0.2-2ubuntu2.dsc 2757 SHA512:168529e7b6d57c1d4b3d4624e5f81e8f31939907715c2f5104be4b78068641210fa5c8909dc9b3d0b5a400b7c354ce4a63facc7ea1d88423a4e65a3221152b50
'http://archive.ubuntu.com/ubuntu/pool/main/a/audit/audit_4.0.2.orig.tar.gz' audit_4.0.2.orig.tar.gz 1198769 SHA512:13d4d07b316fc1380d75baefbb1345b34286015d52e758c14b2f82781cf4cffc16b6eb29d999563ff40caa6d005630a5dfc44741e49b71291c9beb84ddc452a4
'http://archive.ubuntu.com/ubuntu/pool/main/a/audit/audit_4.0.2-2ubuntu2.debian.tar.xz' audit_4.0.2-2ubuntu2.debian.tar.xz 19532 SHA512:253bd3e605022824735845f050dce42948bd613751b7b2fc409771122a6ea58f462828c8a83f5a81fe123c4dcc12bf6f469f58915c8fc94e72c3f12a629947e2
```

### `dpkg` source package: `base-files=13.7ubuntu1`

Binary Packages:

- `base-files=13.7ubuntu1`

Licenses: (parsed from: `/usr/share/doc/base-files/copyright`)

- `GPL`
- `GPL-2+`
- `verbatim`

Source:

```console
$ apt-get source -qq --print-uris base-files=13.7ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/b/base-files/base-files_13.7ubuntu1.dsc' base-files_13.7ubuntu1.dsc 1373 SHA512:8a3f66bff12185acc02db134c6b41d24038d1b6dd52e97bf93a352d3fb98d3aa252f3d6caaf4fc9be5211b951fca4ed6940256f5e2c588f413b3274b1dacd324
'http://archive.ubuntu.com/ubuntu/pool/main/b/base-files/base-files_13.7ubuntu1.tar.xz' base-files_13.7ubuntu1.tar.xz 96600 SHA512:9452d6dbf0f91e9e7958c41274ccbcece1eb38d6e369248abf467aa302148ec84e3e264e002b6ea96a6bc5f4c91c51bca23a14c4a47308e709bbf22c8f7f0acc
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
'http://archive.ubuntu.com/ubuntu/pool/main/b/base-passwd/base-passwd_3.6.7.dsc' base-passwd_3.6.7.dsc 1891 SHA512:e56a81c1b38b1a83dd66119a7e7359843f27b5504a0423d5c8679a6c7ef3f5c27814bb6c3e3cbae7633dd61df67ebbcfd19d746f0cda7faf402f88479e7f4f62
'http://archive.ubuntu.com/ubuntu/pool/main/b/base-passwd/base-passwd_3.6.7.tar.xz' base-passwd_3.6.7.tar.xz 60872 SHA512:9a0f6c0b33396828e7aca57041ab3cf3dc800b2f9057360df2350558c668798c29774f540890f524643405c4b969e80b28c649757cf67cf1edc5e498718990e7
```

### `dpkg` source package: `bash=5.2.37-2ubuntu1`

Binary Packages:

- `bash=5.2.37-2ubuntu1`

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


### `dpkg` source package: `brotli=1.1.0-2build4`

Binary Packages:

- `libbrotli1:amd64=1.1.0-2build4`

Licenses: (parsed from: `/usr/share/doc/libbrotli1/copyright`)

- `MIT`

Source:

```console
$ apt-get source -qq --print-uris brotli=1.1.0-2build4
'http://archive.ubuntu.com/ubuntu/pool/main/b/brotli/brotli_1.1.0-2build4.dsc' brotli_1.1.0-2build4.dsc 2364 SHA512:9307728e51cd08c6df5b2c828bfbf8d68e294a89446100ad239acd86451ee70ed262514e336c7614a93abc3254b2aa48f5db528a32623b6d9344ad8bfffaae63
'http://archive.ubuntu.com/ubuntu/pool/main/b/brotli/brotli_1.1.0.orig.tar.gz' brotli_1.1.0.orig.tar.gz 512036 SHA512:7a94f8b1ca1d3a411c6b5681bd2ed66183468f7b37a24741601d77ed4353577805de84c810dd26086d4afe6b11bfc4791db3ba7f6f9986bc7acbb8e9b43f488b
'http://archive.ubuntu.com/ubuntu/pool/main/b/brotli/brotli_1.1.0-2build4.debian.tar.xz' brotli_1.1.0-2build4.debian.tar.xz 5740 SHA512:012bd62881d9e71caaf589e563c2f6198f86372abc7afb22b2ffbc757fde5f72191142bc83ec98093e258a14cd1dc92e2cb9734b6d8f957368b9c8c48bcabc17
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
'http://archive.ubuntu.com/ubuntu/pool/main/c/ca-certificates/ca-certificates_20250419.dsc' ca-certificates_20250419.dsc 1766 SHA512:a23a4c3bda0d9d16cf5575044d58b5dcee545e164cf455e31522927738dcf62cbccb8ff0520afdd36d53b22cff824388c492bcf85ebf28a9c5a35e8fcdafd745
'http://archive.ubuntu.com/ubuntu/pool/main/c/ca-certificates/ca-certificates_20250419.tar.xz' ca-certificates_20250419.tar.xz 277504 SHA512:5a66a4aabbc18bce752b9e2d362309812cb685e24c0bb52cbb04cde3284b023034955c0ba8c9a3fa065392ab8372d166e6cb17b82fb336cb485e2b63485e9631
```

### `dpkg` source package: `cdebconf=0.277ubuntu1`

Binary Packages:

- `libdebconfclient0:amd64=0.277ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libdebconfclient0/copyright`)

- `BSD-2-Clause`
- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris cdebconf=0.277ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/c/cdebconf/cdebconf_0.277ubuntu1.dsc' cdebconf_0.277ubuntu1.dsc 2873 SHA512:d02a094ef7249b90586cf2a1de7b512330d9b00569edd84392aed1611a22b9dfea63318378a748e72dc4c021281c355d3f3f2874350e2b5e74701054494059f1
'http://archive.ubuntu.com/ubuntu/pool/main/c/cdebconf/cdebconf_0.277ubuntu1.tar.xz' cdebconf_0.277ubuntu1.tar.xz 286968 SHA512:ebb8cee8ee8d84aaab49a03211d9cad56dec362d80e63f7375dad09e06eecb7a44811078327daf73d14f6bb9bbbba13adc1ac9ec03dbda0ea31c79532c5a6f12
```

### `dpkg` source package: `coreutils-from=0.0.0~ubuntu3`

Binary Packages:

- `coreutils=9.5-1ubuntu2+0.0.0~ubuntu3`
- `coreutils-from-gnu=0.0.0~ubuntu3`

Licenses: (parsed from: `/usr/share/doc/coreutils/copyright`, `/usr/share/doc/coreutils-from-gnu/copyright`)

- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris coreutils-from=0.0.0~ubuntu3
'http://archive.ubuntu.com/ubuntu/pool/main/c/coreutils-from/coreutils-from_0.0.0%7eubuntu3.dsc' coreutils-from_0.0.0~ubuntu3.dsc 1976 SHA512:8021ec61d1110891f048e658d6a0ad5f631b3945aabda0668cbd4719f1328757ab3ba89f6b8a119fd1a4e8d477f011e3efdeb2a6851d4d564a85539632a3310a
'http://archive.ubuntu.com/ubuntu/pool/main/c/coreutils-from/coreutils-from_0.0.0%7eubuntu3.tar.xz' coreutils-from_0.0.0~ubuntu3.tar.xz 5388 SHA512:1abbc5bf6a7f708effd682e6c6366d95e1cb22998c80bfd169168503ce8792d5deccbff2a3e7e2b023e0d50cd64a5a2c466dc60d7eb2a6431819023b430ddf03
```

### `dpkg` source package: `coreutils=9.5-1ubuntu2`

Binary Packages:

- `gnu-coreutils=9.5-1ubuntu2`

Licenses: (parsed from: `/usr/share/doc/gnu-coreutils/copyright`)

- `BSD-4-clause-UC`
- `FSFULLR`
- `GFDL-1.3`
- `GFDL-NIV-1.3`
- `GPL-3`
- `GPL-3+`
- `ISC`

Source:

```console
$ apt-get source -qq --print-uris coreutils=9.5-1ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/c/coreutils-from/coreutils-from_0.0.0%7eubuntu3.dsc' coreutils-from_0.0.0~ubuntu3.dsc 1976 SHA512:8021ec61d1110891f048e658d6a0ad5f631b3945aabda0668cbd4719f1328757ab3ba89f6b8a119fd1a4e8d477f011e3efdeb2a6851d4d564a85539632a3310a
'http://archive.ubuntu.com/ubuntu/pool/main/c/coreutils-from/coreutils-from_0.0.0%7eubuntu3.tar.xz' coreutils-from_0.0.0~ubuntu3.tar.xz 5388 SHA512:1abbc5bf6a7f708effd682e6c6366d95e1cb22998c80bfd169168503ce8792d5deccbff2a3e7e2b023e0d50cd64a5a2c466dc60d7eb2a6431819023b430ddf03
```

### `dpkg` source package: `curl=8.13.0-5ubuntu1`

Binary Packages:

- `curl=8.13.0-5ubuntu1`
- `libcurl3t64-gnutls:amd64=8.13.0-5ubuntu1`
- `libcurl4t64:amd64=8.13.0-5ubuntu1`

Licenses: (parsed from: `/usr/share/doc/curl/copyright`, `/usr/share/doc/libcurl3t64-gnutls/copyright`, `/usr/share/doc/libcurl4t64/copyright`)

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
'http://archive.ubuntu.com/ubuntu/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.28%2bdfsg1-9.dsc' cyrus-sasl2_2.1.28+dfsg1-9.dsc 3306 SHA512:35f2c9b47fb70e13ccffbc269a183beb95f50eb381f753a700631bf76a345f9316aa1f665395ce450060bb4cc51e60e72cadec2fd3256b68bc7f0f8988bf9a6c
'http://archive.ubuntu.com/ubuntu/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.28%2bdfsg1.orig.tar.xz' cyrus-sasl2_2.1.28+dfsg1.orig.tar.xz 794540 SHA512:e94075d09b38a50138b782323de286deb7b15008064f07df4fa682e94367e829d9bfafef48d5478f730fef8fde536bcc6d54cab0452b76473a3c620b3dc18fa2
'http://archive.ubuntu.com/ubuntu/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.28%2bdfsg1-9.debian.tar.xz' cyrus-sasl2_2.1.28+dfsg1-9.debian.tar.xz 99180 SHA512:1ff7193c671614f63632df7c5677f9c52e11eb172345068494b7dc739e7ff6f556f341a937239bbd7efab0d7a2fb12bd88d69da8a67e1ce77e27d08d8d99768b
```

### `dpkg` source package: `dash=0.5.12-12ubuntu1`

Binary Packages:

- `dash=0.5.12-12ubuntu1`

Licenses: (parsed from: `/usr/share/doc/dash/copyright`)

- `BSD-3-Clause`
- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris dash=0.5.12-12ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/d/dash/dash_0.5.12-12ubuntu1.dsc' dash_0.5.12-12ubuntu1.dsc 2060 SHA512:540bd534f36366297746f183d3613eb0848f4e18aa50b306d3e7c130cc2e107d6eb5b02bab2952efca336c20fbf8683d4f421e5cf82c81a026a6d385ab0c2f1c
'http://archive.ubuntu.com/ubuntu/pool/main/d/dash/dash_0.5.12.orig.tar.gz' dash_0.5.12.orig.tar.gz 246054 SHA512:13bd262be0089260cbd13530a9cf34690c0abeb2f1920eb5e61be7951b716f9f335b86279d425dbfae56cbd49231a8fdffdff70601a5177da3d543be6fc5eb17
'http://archive.ubuntu.com/ubuntu/pool/main/d/dash/dash_0.5.12-12ubuntu1.debian.tar.xz' dash_0.5.12-12ubuntu1.debian.tar.xz 47976 SHA512:5e7603682e51045e053e5d014cc4fe1af15fe2d903ef1fcc1ebbec066d895705639f4a087254c933163cbbd2afd94f061cbda9d6d66b9040a269d45c757f48fd
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
'http://archive.ubuntu.com/ubuntu/pool/main/d/db5.3/db5.3_5.3.28%2bdfsg2-9.dsc' db5.3_5.3.28+dfsg2-9.dsc 2373 SHA512:f7b3ee10c42556df8b3fd016d9ebe4efc38d60aba8cbd7120d4573d8242c9260e7507cda3b7a2af3f5501ac3d7b27c5dcaccfc54235eb428f583d4d9adae21f5
'http://archive.ubuntu.com/ubuntu/pool/main/d/db5.3/db5.3_5.3.28%2bdfsg2.orig.tar.xz' db5.3_5.3.28+dfsg2.orig.tar.xz 21287688 SHA512:f9c9d042702ef3fcfdd4b4859583048f3396b161009dc24b6d3a2c53533d58214239fc80e2c42db17e9f092df44d531502737f3b368b956bff49ef057b6b51ef
'http://archive.ubuntu.com/ubuntu/pool/main/d/db5.3/db5.3_5.3.28%2bdfsg2-9.debian.tar.xz' db5.3_5.3.28+dfsg2-9.debian.tar.xz 36412 SHA512:9ed5d57168a50b8adae1c08cc7d1b307904a06a506d85e2faa2bbb4edfaf614b1ef5c3efe11ad71fc5d0f200459a1628c7d092fe121a53a619943c1424031796
```

### `dpkg` source package: `debconf=1.5.87ubuntu1`

Binary Packages:

- `debconf=1.5.87ubuntu1`

Licenses: (parsed from: `/usr/share/doc/debconf/copyright`)

- `BSD-2-clause`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `debianutils=5.22`

Binary Packages:

- `debianutils=5.22`

Licenses: (parsed from: `/usr/share/doc/debianutils/copyright`)

- `GPL-2`
- `GPL-2+`
- `SMAIL-GPL`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/debianutils/5.22/


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
'http://archive.ubuntu.com/ubuntu/pool/main/d/diffutils/diffutils_3.10-4.dsc' diffutils_3.10-4.dsc 1875 SHA512:7bf4b24fa79e6c436125eb5c5926e7f4460c1108142a0d2d5662d9e6ee40e9425e22e282c784850790ae02032d6c1dc724c3b38a592e7f74949f732d4ce854bd
'http://archive.ubuntu.com/ubuntu/pool/main/d/diffutils/diffutils_3.10.orig.tar.xz' diffutils_3.10.orig.tar.xz 1624240 SHA512:219d2c815a120690c6589846271e43aee5c96c61a7ee4abbef97dfcdb3d6416652ed494b417de0ab6688c4322540d48be63b5e617beb6d20530b5d55d723ccbb
'http://archive.ubuntu.com/ubuntu/pool/main/d/diffutils/diffutils_3.10.orig.tar.xz.asc' diffutils_3.10.orig.tar.xz.asc 833 SHA512:91aa1fcfca224454e292540ea7813f4a0eb348f06a4374017326d524949775359fc833de597cc201c97f357eb6c675800828a6e3332572376f3554f1f2e1aca1
'http://archive.ubuntu.com/ubuntu/pool/main/d/diffutils/diffutils_3.10-4.debian.tar.xz' diffutils_3.10-4.debian.tar.xz 14304 SHA512:447d360101e549e520210cd6da9573cce293c1b59266d960b066da4eeff8ce473c19d2269e30cd82e33e162cd6c6b870755b3bb292d8592a51511ca19e974350
```

### `dpkg` source package: `dpkg=1.22.18ubuntu3`

Binary Packages:

- `dpkg=1.22.18ubuntu3`

Licenses: (parsed from: `/usr/share/doc/dpkg/copyright`)

- `GPL-2`
- `GPL-2+`
- `public-domain-s-s-d`

Source:

```console
$ apt-get source -qq --print-uris dpkg=1.22.18ubuntu3
'http://archive.ubuntu.com/ubuntu/pool/main/d/dpkg/dpkg_1.22.18ubuntu3.dsc' dpkg_1.22.18ubuntu3.dsc 3414 SHA512:e6b336219c532b8b90c18b047e55e9a75d772397a5aa37fe8c35f65be674363687a6231ac482b2e629aed663f5fb597124fadb610f1bba9a3714542605643863
'http://archive.ubuntu.com/ubuntu/pool/main/d/dpkg/dpkg_1.22.18ubuntu3.tar.xz' dpkg_1.22.18ubuntu3.tar.xz 5679260 SHA512:03f9afb70676ce904684e58739e66dcae766400f5db9f4ea8715a4f13afa8b529b89c55dfd12f3369442184d1dbc62ff78cf1a647c5db550ce3767cbc66876eb
```

### `dpkg` source package: `e2fsprogs=1.47.2-1ubuntu1`

Binary Packages:

- `e2fsprogs=1.47.2-1ubuntu1`
- `libcom-err2:amd64=1.47.2-1ubuntu1`
- `libext2fs2t64:amd64=1.47.2-1ubuntu1`
- `libss2:amd64=1.47.2-1ubuntu1`
- `logsave=1.47.2-1ubuntu1`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `expat=2.7.1-1`

Binary Packages:

- `libexpat1:amd64=2.7.1-1`

Licenses: (parsed from: `/usr/share/doc/libexpat1/copyright`)

- `MIT`

Source:

```console
$ apt-get source -qq --print-uris expat=2.7.1-1
'http://archive.ubuntu.com/ubuntu/pool/main/e/expat/expat_2.7.1-1.dsc' expat_2.7.1-1.dsc 1964 SHA512:f8bf1fc2f45b655c7374b53c4bdce69628e8e5157bb8913d632c4fd0b8f86eedb3e22886cc55684808897533453429d07d3532444916a28c657564783bb00826
'http://archive.ubuntu.com/ubuntu/pool/main/e/expat/expat_2.7.1.orig.tar.gz' expat_2.7.1.orig.tar.gz 8433717 SHA512:ea5452c511e18e0eb927eab46a47c7ced1b1be3b46232a38caef39aa86fd552a72f066db66ca824ade3ff2376b70ca72ca91bdf1d003770c91a38a47e8781b8f
'http://archive.ubuntu.com/ubuntu/pool/main/e/expat/expat_2.7.1-1.debian.tar.xz' expat_2.7.1-1.debian.tar.xz 13204 SHA512:bd4da088a12457086cace1c8ceb4379fb97a7c5fac183c0b7d1ef0ff84a92fcc3f58cd2fc35d31677c842f7e69c3e57b7df9931c0e30d79d7c9f9d4af8d83aac
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

### `dpkg` source package: `gcc-14=14.3.0-1ubuntu1`

Binary Packages:

- `gcc-14-base:amd64=14.3.0-1ubuntu1`

Licenses: (parsed from: `/usr/share/doc/gcc-14-base/copyright`)

- `Artistic`
- `GFDL-1.2`
- `GPL`
- `GPL-3`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris gcc-14=14.3.0-1ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-14/gcc-14_14.3.0-1ubuntu1.dsc' gcc-14_14.3.0-1ubuntu1.dsc 42455 SHA512:9190e73572b5cf2ae2ba8425db3575755aa56b699aa644fae82fbe8b7bf86beaacfa4b2ce571454bc5cd23aab264de82ee5b67fec052cc005d2a55f66d151b30
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-14/gcc-14_14.3.0.orig.tar.gz' gcc-14_14.3.0.orig.tar.gz 100117093 SHA512:cd51c26dde94fadbc677d04194eb49e4c02f4a695a835bcec4562d27e94d76f0bbbc6ffa448beeec2c077b89d51bfe0c18797840272f40b5b7e8be6fd49ae56c
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-14/gcc-14_14.3.0-1ubuntu1.debian.tar.xz' gcc-14_14.3.0-1ubuntu1.debian.tar.xz 571600 SHA512:a6b20cf066ff0b13bbef50d9fc8f112d91bbdc5594a5f2066fba31099f914f27f98b6a01b260072cc4804f0d15a7cec082fbe1521151c99a1fdbfad6b35f4e99
```

### `dpkg` source package: `gcc-15=15.1.0-5ubuntu1`

Binary Packages:

- `gcc-15-base:amd64=15.1.0-5ubuntu1`
- `libgcc-s1:amd64=15.1.0-5ubuntu1`
- `libstdc++6:amd64=15.1.0-5ubuntu1`

Licenses: (parsed from: `/usr/share/doc/gcc-15-base/copyright`, `/usr/share/doc/libgcc-s1/copyright`, `/usr/share/doc/libstdc++6/copyright`)

- `Apache-2.0`
- `Artistic`
- `GFDL-1.2`
- `GPL`
- `GPL-3`
- `LGPL`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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
'http://archive.ubuntu.com/ubuntu/pool/main/g/gdbm/gdbm_1.24-2.dsc' gdbm_1.24-2.dsc 2466 SHA512:b25a2656224dc0e7703375a50cb58cb3cb8b63f89a3a2c2e749b96fb40ae989f06a169bb0655dddecbe3e39fe856e8f22022c0b253d9dca303475f4361541dc2
'http://archive.ubuntu.com/ubuntu/pool/main/g/gdbm/gdbm_1.24.orig.tar.gz' gdbm_1.24.orig.tar.gz 1195931 SHA512:401ff8c707079f21da1ac1d6f4714a87f224b6f41943078487dc891be49f51fd1ac7a32fd599aae0fad185f2c6ba7432616d328fd6aaab068eb54db9562ff7fa
'http://archive.ubuntu.com/ubuntu/pool/main/g/gdbm/gdbm_1.24.orig.tar.gz.asc' gdbm_1.24.orig.tar.gz.asc 195 SHA512:c39d91aa6dee98851eac16b27a192300dab9545cff5e441d66a55a0939f1c6bc9e5ead0e96a48ef941f69d586b34d78e786d262d65e3b13ffe2c4f372d823fd6
'http://archive.ubuntu.com/ubuntu/pool/main/g/gdbm/gdbm_1.24-2.debian.tar.xz' gdbm_1.24-2.debian.tar.xz 16880 SHA512:bb98e8032f57a1dc33d34004e6b748a859aa465bd9fd6a592abe6d3ca09eedfebf05fbf0245d5c4eb01560ee0998f16016cd85ebc3367c25713795a9bab97a0f
```

### `dpkg` source package: `git=1:2.48.1-0ubuntu1`

Binary Packages:

- `git=1:2.48.1-0ubuntu1`
- `git-man=1:2.48.1-0ubuntu1`

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
$ apt-get source -qq --print-uris git=1:2.48.1-0ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/g/git/git_2.48.1-0ubuntu1.dsc' git_2.48.1-0ubuntu1.dsc 2793 SHA512:a8ba9423e2ed2f8183aca1de87630bb4cf2bb6ef0e3100bbd891ce593829b961a691f5a67d9044f2327a567967000257e9507774e4fffd2e5ed080cb3832048e
'http://archive.ubuntu.com/ubuntu/pool/main/g/git/git_2.48.1.orig.tar.xz' git_2.48.1.orig.tar.xz 7723580 SHA512:75c89ab4ca83adc46989a4b05a9b482b40a7ba69d15aa1c1f27d0cee37c2908e154a75d59b0a0a540647352b9c55020f1a5ad309f0eff78e9fd8e631ef9e4606
'http://archive.ubuntu.com/ubuntu/pool/main/g/git/git_2.48.1-0ubuntu1.debian.tar.xz' git_2.48.1-0ubuntu1.debian.tar.xz 795652 SHA512:00ecb7ae69752f59e3c5f57bff03ec7f08d5ae584e07e01e4e40440b9306f19b2ae20dcd0177cf44bd176a64a09603ab2081cff2cc79f492ee9195cdaf9f5342
```

### `dpkg` source package: `glibc=2.41-6ubuntu2`

Binary Packages:

- `libc-bin=2.41-6ubuntu2`
- `libc6:amd64=2.41-6ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libc-bin/copyright`, `/usr/share/doc/libc6/copyright`)

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
- `GFDL-1.3`
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
$ apt-get source -qq --print-uris glibc=2.41-6ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.41-6ubuntu2.dsc' glibc_2.41-6ubuntu2.dsc 8027 SHA512:84d61cacc57660981576fe289ce311fccb53c8060d8b04ba799614b647ea1959e91146b5075016df9dbd67e693ab87eacac2f7e0bbeeda20394560267b70e01b
'http://archive.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.41.orig.tar.xz' glibc_2.41.orig.tar.xz 19344868 SHA512:894a3e5a796bc13df30c26a5bfbe4d60b5dbdaac54e7763432235124b547070c7dda88c50584536870cab79183d8cad73a3ac6ed09bfe54fa8482aad07253169
'http://archive.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.41.orig.tar.xz.asc' glibc_2.41.orig.tar.xz.asc 981 SHA512:98462e1a1abce7ae7214b48bce160ff95ffb6634708d9952a0997575ae1fb06f4499e01953bace0933e07fddf583f0dfe93221c44192957a894a4126ab073ce8
'http://archive.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.41-6ubuntu2.debian.tar.xz' glibc_2.41-6ubuntu2.debian.tar.xz 458328 SHA512:0d13dddd61f37be277a5b2a70dea923f94dc4b76b579058320024255df6164fb5f8e12fcc05071997d748db03c68a93a5635d9372394e57333ec12a29f4c736f
```

### `dpkg` source package: `gmp=2:6.3.0+dfsg-3ubuntu2`

Binary Packages:

- `libgmp10:amd64=2:6.3.0+dfsg-3ubuntu2`

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
$ apt-get source -qq --print-uris gmp=2:6.3.0+dfsg-3ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/g/gmp/gmp_6.3.0%2bdfsg-3ubuntu2.dsc' gmp_6.3.0+dfsg-3ubuntu2.dsc 2337 SHA512:e6c5be8da178f008fc856d593ad5aa06be9b604075559ba1e7e231da7b5d0a8ca3390b25a3ab9388c860462fa49e0d58c2e8c713642927457f865e5caa378696
'http://archive.ubuntu.com/ubuntu/pool/main/g/gmp/gmp_6.3.0%2bdfsg.orig.tar.xz' gmp_6.3.0+dfsg.orig.tar.xz 1870556 SHA512:a422b29024464aeb26c69f64be1bc37407d74e0290f44f67fc040fe38b97f3eb7aa6ba8380722ef36cac39816d1c4f24b771159fb86d5979ef0791dcdef708bc
'http://archive.ubuntu.com/ubuntu/pool/main/g/gmp/gmp_6.3.0%2bdfsg-3ubuntu2.debian.tar.xz' gmp_6.3.0+dfsg-3ubuntu2.debian.tar.xz 39724 SHA512:553121b4a70c4a8b46481ae156796354baebc1150e32dd4f4c32695b37b019fec0ac80a4fdae607cce7ab3fb83f83c37aac66ab04cb314e835012bd83c845d51
```

### `dpkg` source package: `gnupg2=2.4.7-17ubuntu3`

Binary Packages:

- `dirmngr=2.4.7-17ubuntu3`
- `gnupg=2.4.7-17ubuntu3`
- `gpg=2.4.7-17ubuntu3`
- `gpg-agent=2.4.7-17ubuntu3`
- `gpgconf=2.4.7-17ubuntu3`
- `gpgsm=2.4.7-17ubuntu3`
- `gpgv=2.4.7-17ubuntu3`

Licenses: (parsed from: `/usr/share/doc/dirmngr/copyright`, `/usr/share/doc/gnupg/copyright`, `/usr/share/doc/gpg/copyright`, `/usr/share/doc/gpg-agent/copyright`, `/usr/share/doc/gpgconf/copyright`, `/usr/share/doc/gpgsm/copyright`, `/usr/share/doc/gpgv/copyright`)

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
$ apt-get source -qq --print-uris gnupg2=2.4.7-17ubuntu3
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnupg2/gnupg2_2.4.7-17ubuntu3.dsc' gnupg2_2.4.7-17ubuntu3.dsc 4586 SHA512:d9d294a262a01e911a5efc81a8648572f3aabd4d5fc658895ee70ccdc2931fc32abe052edc3bcd7e53e2b28c9f632ac01ff682c8fb4f844b792e178803bbacb3
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnupg2/gnupg2_2.4.7.orig.tar.bz2' gnupg2_2.4.7.orig.tar.bz2 8010244 SHA512:3e84f1679904bf0efb789df6466e468bd2be9149d52561f35e2380038133479bebf1c61ee7adf6d3564b370915f32111098c052be6e6acaf3083a807f9f36019
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnupg2/gnupg2_2.4.7.orig.tar.bz2.asc' gnupg2_2.4.7.orig.tar.bz2.asc 390 SHA512:6c0b9876ec8c79e04b495a888e1f83d43385422258fd0f603224a7913a4e6937fe2964457e3029e92bb667b4a586811ea54bd721d47f39d4bf25f6808795ec4d
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnupg2/gnupg2_2.4.7-17ubuntu3.debian.tar.xz' gnupg2_2.4.7-17ubuntu3.debian.tar.xz 111824 SHA512:9b0666501003732699c0163eb0739473420303fdd5ecbe40e9c9ab21de8399e12a9f92c50d868652922e6e67a0ba6b3d86897ca9adc67b9e79b3a9ac4bd950dd
```

### `dpkg` source package: `gnutls28=3.8.9-2ubuntu3`

Binary Packages:

- `libgnutls30t64:amd64=3.8.9-2ubuntu3`

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
$ apt-get source -qq --print-uris gnutls28=3.8.9-2ubuntu3
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.8.9-2ubuntu3.dsc' gnutls28_3.8.9-2ubuntu3.dsc 3380 SHA512:668bdb0d6e30c20d6043d1ac0bbdcf61fdce51d53ffab4999ecf30f6eb1ed2365e02dbb1335072c4951c84e5d18d660e955db1d975df8b02c9d2738e9b231c0c
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.8.9.orig.tar.xz' gnutls28_3.8.9.orig.tar.xz 6847364 SHA512:b3b201671bf4e75325610a0291d4cd36a669718e22b3685246b64bde97b5bd94f463ab376ed817869869714115f4ff11bdc53c32604bb04a8ff8e10daa6d1fc7
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.8.9.orig.tar.xz.asc' gnutls28_3.8.9.orig.tar.xz.asc 833 SHA512:0eb265bbbc1ee735ecf4e3d308eacf3e3aebe4a9b0848af1fb340ec18e78bb516e1c74a6a72d4764bb03086d88d3ada3cd7ed82861a8f4ca7a403d9a5eb9a3a7
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.8.9-2ubuntu3.debian.tar.xz' gnutls28_3.8.9-2ubuntu3.debian.tar.xz 85852 SHA512:babdee5c127c45d2e7525dc3ebd416c5fd557a6eff7beda3513bc500ab9a77eb4f924a5f1a6e3134cf99594f66c82e82dc70eafae215dd703c96197f93c0fe31
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

### `dpkg` source package: `gzip=1.13-1ubuntu3`

Binary Packages:

- `gzip=1.13-1ubuntu3`

Licenses: (parsed from: `/usr/share/doc/gzip/copyright`)

- `FSF-manpages`
- `GFDL-1.3+-no-invariant`
- `GFDL-3`
- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris gzip=1.13-1ubuntu3
'http://archive.ubuntu.com/ubuntu/pool/main/g/gzip/gzip_1.13-1ubuntu3.dsc' gzip_1.13-1ubuntu3.dsc 1933 SHA512:83f2c4c9726b75b65db28ced4450ec788d3e6dbab6aaf5ab80a6a20aca9fd23634344767ccfcfd109cceab9423d006b7a29b85b20c7c17319134c3e5afa6c97d
'http://archive.ubuntu.com/ubuntu/pool/main/g/gzip/gzip_1.13.orig.tar.xz' gzip_1.13.orig.tar.xz 838248 SHA512:e3d4d4aa4b2e53fdad980620307257c91dfbbc40bcec9baa8d4e85e8327f55e2ece552c9baf209df7b66a07103ab92d4954ac53c86c57fbde5e1dd461143f94c
'http://archive.ubuntu.com/ubuntu/pool/main/g/gzip/gzip_1.13-1ubuntu3.debian.tar.xz' gzip_1.13-1ubuntu3.debian.tar.xz 21364 SHA512:cc6c1acdb8ca29bfcdbc75c462504b57c867e13313bc229a8cebcf681ca0c347af8e5c36da072d1b6e38d13eeb06bca74b97cce4b67306d6d17be6ff66ba6537
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
'http://archive.ubuntu.com/ubuntu/pool/main/i/init-system-helpers/init-system-helpers_1.68.dsc' init-system-helpers_1.68.dsc 2209 SHA512:4c8477f718287a3001fc378938e2e3bdbf15dca7a8aac93fdb65fe458408294b15c7e05ad6b5bcf04eda927ba934ca7f201cea2ff93090c8906b7b5abadf920e
'http://archive.ubuntu.com/ubuntu/pool/main/i/init-system-helpers/init-system-helpers_1.68.tar.xz' init-system-helpers_1.68.tar.xz 45168 SHA512:3962845b388ee5c22de26a17e216ddd7f706d4f67729c80891c1457bf3e3fd70484b04f6d9d42adde7dad72da5529ac6feda97c9e2d4c0f4ccbfec2217a8e1b4
```

### `dpkg` source package: `keyutils=1.6.3-4ubuntu2`

Binary Packages:

- `libkeyutils1:amd64=1.6.3-4ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libkeyutils1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2`
- `LGPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `krb5=1.21.3-4ubuntu2`

Binary Packages:

- `libgssapi-krb5-2:amd64=1.21.3-4ubuntu2`
- `libk5crypto3:amd64=1.21.3-4ubuntu2`
- `libkrb5-3:amd64=1.21.3-4ubuntu2`
- `libkrb5support0:amd64=1.21.3-4ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libgssapi-krb5-2/copyright`, `/usr/share/doc/libk5crypto3/copyright`, `/usr/share/doc/libkrb5-3/copyright`, `/usr/share/doc/libkrb5support0/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris krb5=1.21.3-4ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.21.3-4ubuntu2.dsc' krb5_1.21.3-4ubuntu2.dsc 4090 SHA512:600109c8cd99e304e2e5b9141a3c0d535881a6d985e6c99a80900be90aefca20fc2b71c1ce9a99d1020a8957a6b2c9c3b30b43644e62e59066032aa37146aaad
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.21.3.orig.tar.gz' krb5_1.21.3.orig.tar.gz 9136145 SHA512:87bc06607f4d95ff604169cea22180703a42d667af05f66f1569b8bd592670c42820b335e5c279e8b4f066d1e7da20f1948a1e4def7c5d295c170cbfc7f49c71
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.21.3.orig.tar.gz.asc' krb5_1.21.3.orig.tar.gz.asc 833 SHA512:8992a5f5247315b9846aa73be4ee1ea223c0231a52d5c6c28718b1f3e3b45d62e2dad4aa5543a83163d1369bb79886b6c1c22766f22d8aa2f6b2575c54d0075c
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.21.3-4ubuntu2.debian.tar.xz' krb5_1.21.3-4ubuntu2.debian.tar.xz 110988 SHA512:64052c74bc443c7f08875ff71ef56d962ef55ac763b9034ca07369e089cbf0a293ac984d0ae67da4d8ef124a73adffcbed9787aab62f4794374d3e8801b4b2ce
```

### `dpkg` source package: `libassuan=3.0.2-2`

Binary Packages:

- `libassuan9:amd64=3.0.2-2`

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

Source:

```console
$ apt-get source -qq --print-uris libassuan=3.0.2-2
'http://archive.ubuntu.com/ubuntu/pool/main/liba/libassuan/libassuan_3.0.2-2.dsc' libassuan_3.0.2-2.dsc 2682 SHA512:73edc82147084f103adf4791ac4ad41f4558edaa31cb3669839df1af46e3e078d7201e051a77dfc910019517974e6147cbd3b0a47c2c223242a8c37ab173bfab
'http://archive.ubuntu.com/ubuntu/pool/main/liba/libassuan/libassuan_3.0.2.orig.tar.bz2' libassuan_3.0.2.orig.tar.bz2 593917 SHA512:a591eda350ecbf4fe8568b5087f69830df31f36ec67e2a50672aacea9bee16020f374a0bface459aeac1897c048072415ab5962a97034ce6fa413100b2a427fb
'http://archive.ubuntu.com/ubuntu/pool/main/liba/libassuan/libassuan_3.0.2.orig.tar.bz2.asc' libassuan_3.0.2.orig.tar.bz2.asc 228 SHA512:56e0a8288e498bbba504fdaa84060ef6dd30c72efd691d6d0e39069113a394f2da407d83adfd14f7ae25b8e8531f8e9dee859b52471261653dc2ed5f44ef22dc
'http://archive.ubuntu.com/ubuntu/pool/main/liba/libassuan/libassuan_3.0.2-2.debian.tar.xz' libassuan_3.0.2-2.debian.tar.xz 17536 SHA512:45fce9ebcc65162f74790c67d6615ead69fd201e5933df68431e3696c76367bfe521c346fe0bf4a8b914139fd9dc644885bfda9805cf32b51de9044493f4f3ba
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
'http://archive.ubuntu.com/ubuntu/pool/main/libb/libbsd/libbsd_0.12.2-2.dsc' libbsd_0.12.2-2.dsc 2446 SHA512:253b89208ff4acafb45c4294fe668d15d7a2f539745dffe6fdb4464fa672e39631dd92f17da4fe44f3084a967b783a39ea221cdd48fbbb30c49f520d60a0c447
'http://archive.ubuntu.com/ubuntu/pool/main/libb/libbsd/libbsd_0.12.2.orig.tar.xz' libbsd_0.12.2.orig.tar.xz 446032 SHA512:ce43e4f0486d5f00d4a8119ee863eaaa2f968cae4aa3d622976bb31ad601dfc565afacef7ebade5eba33fff1c329b5296c6387c008d1e1805d878431038f8b21
'http://archive.ubuntu.com/ubuntu/pool/main/libb/libbsd/libbsd_0.12.2.orig.tar.xz.asc' libbsd_0.12.2.orig.tar.xz.asc 833 SHA512:c2e56aa572ce50d6342c0e45622958eba40319e09d45dc3cff6296cb10eebc0c4154d6f758dd2470a1794251fc0273d05ac2d735698eae83183769df5f7d44c3
'http://archive.ubuntu.com/ubuntu/pool/main/libb/libbsd/libbsd_0.12.2-2.debian.tar.xz' libbsd_0.12.2-2.debian.tar.xz 18688 SHA512:82241267d3fdba624a118af842647cd2a57c202fb9a1f53b5303e258e3a55a9d33bf52e449c4d2656cd5baf8059f2976a082c592c30b0f4ac800ab48ab9d1dec
```

### `dpkg` source package: `libcap-ng=0.8.5-4build1`

Binary Packages:

- `libcap-ng0:amd64=0.8.5-4build1`

Licenses: (parsed from: `/usr/share/doc/libcap-ng0/copyright`)

- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris libcap-ng=0.8.5-4build1
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap-ng/libcap-ng_0.8.5-4build1.dsc' libcap-ng_0.8.5-4build1.dsc 2307 SHA512:445e82bbbd3ce274be18d37af59c4417c7278a6ff5497ee4b9dfa28054ebb58730eda206bdf0162de92e48e85ed5ca1d9ddcb9ef0c0d1ec54ae1a921ca6dcdbb
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap-ng/libcap-ng_0.8.5.orig.tar.gz' libcap-ng_0.8.5.orig.tar.gz 59265 SHA512:3bd868c7f263b77edd2feda831470b407f1086b434618e54336fb78bbf8bf3bad53f4c006a2118fb594b16554f8f7ec2acb76e08be5586d0261684e9ba139231
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap-ng/libcap-ng_0.8.5-4build1.debian.tar.xz' libcap-ng_0.8.5-4build1.debian.tar.xz 7872 SHA512:8b0b4c8aa95667190a30e1e8c7883404b92dbfb76d2ef4a52b3d4cfac95dcfec2a7850727feb0084f6fa1b6d249ca82bd8be6adb7796148c79c419b5efafda71
```

### `dpkg` source package: `libcap2=1:2.73-4ubuntu1`

Binary Packages:

- `libcap2:amd64=1:2.73-4ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libcap2/copyright`)

- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libcbor=0.10.2-2ubuntu1`

Binary Packages:

- `libcbor0.10:amd64=0.10.2-2ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libcbor0.10/copyright`)

- `Expat`

Source:

```console
$ apt-get source -qq --print-uris libcbor=0.10.2-2ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcbor/libcbor_0.10.2-2ubuntu1.dsc' libcbor_0.10.2-2ubuntu1.dsc 2275 SHA512:1991707066f3fdeb160e41906b685d21493386c0d2451e792c6233bfa37bd4429b6c64ab24d64dd0752f382823a1089ad352f29101dcf772dcba69ffd700dbd8
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcbor/libcbor_0.10.2.orig.tar.gz' libcbor_0.10.2.orig.tar.gz 289450 SHA512:23c6177443778d4b4833ec7ed0d0e639a0d4863372e3a38d772fdce2673eae6d5cb2a31a2a021d1a699082ea53494977c907fd0e94149b97cb23a4b6d039228a
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcbor/libcbor_0.10.2-2ubuntu1.debian.tar.xz' libcbor_0.10.2-2ubuntu1.debian.tar.xz 7308 SHA512:4105fe0d677f98d28da543995037818c756108cab254244584e669717c5874bda25e073579169d9dbc4075bb5957285c72deaa43c05ecb9a24fef608aca4854b
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

### `dpkg` source package: `liberror-perl=0.17030-1`

Binary Packages:

- `liberror-perl=0.17030-1`

Licenses: (parsed from: `/usr/share/doc/liberror-perl/copyright`)

- `Artistic`
- `GPL-1`
- `GPL-1+`
- `MIT/X11`

Source:

```console
$ apt-get source -qq --print-uris liberror-perl=0.17030-1
'http://archive.ubuntu.com/ubuntu/pool/main/libe/liberror-perl/liberror-perl_0.17030-1.dsc' liberror-perl_0.17030-1.dsc 2337 SHA512:1c039478eb6721fb61ac62f0daedf0e32e935f40625564a1dbc6f240776bb9bfaa05a2f0176296f08fcf939e7d967fd31274aca9d7522b05809bd32c97e511ec
'http://archive.ubuntu.com/ubuntu/pool/main/libe/liberror-perl/liberror-perl_0.17030.orig.tar.gz' liberror-perl_0.17030.orig.tar.gz 33488 SHA512:842e33fbc2f2bd6eaf03459263070311fde9ae06105438baf8920826ca26d3f46c18d0d49bfe85a3eb25dfe94e671db0e7d1f30a143b8d82bea47410bfbf7f01
'http://archive.ubuntu.com/ubuntu/pool/main/libe/liberror-perl/liberror-perl_0.17030-1.debian.tar.xz' liberror-perl_0.17030-1.debian.tar.xz 4660 SHA512:7a7d03e838840c466c34bcea97b43a1cc12f4baa87ed260164a04c01ca2aeec50286104b98ac074e5af44e8e68fac36823ba0ad04729fb2d8046487b42a2553b
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
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libffi/libffi_3.4.8-2.dsc' libffi_3.4.8-2.dsc 1948 SHA512:46b637679a3209f5d496bf84a2e23a98d95b6c10cbfc9b3e4b547b6093e4a1227218ff792fcefa5fa0a9f0b96d7de1b04b4d0152abd6209d0fb0aa5c299571b6
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libffi/libffi_3.4.8.orig.tar.gz' libffi_3.4.8.orig.tar.gz 595051 SHA512:064a43ddae005f3d0fa56db4da6071fae93aaae87a755b84888c0cb9c8fa2fe9bb452b3d9a382fab64c442c19d98a20ba15b8be92eba7bf3773815b31fb7824c
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libffi/libffi_3.4.8-2.debian.tar.xz' libffi_3.4.8-2.debian.tar.xz 11220 SHA512:df8d165621d1719a1eb416f12613495e15daf2e029e8608fcb5f35ff5ebd4fa98710b280506c4ab6c54177a40dce692d838677784a6809b90a8a6d1d52ce14a2
```

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

### `dpkg` source package: `libgpg-error=1.51-4`

Binary Packages:

- `libgpg-error0:amd64=1.51-4`

Licenses: (parsed from: `/usr/share/doc/libgpg-error0/copyright`)

- `BSD-3-clause`
- `GPL-3`
- `GPL-3+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `g10-permissive`

Source:

```console
$ apt-get source -qq --print-uris libgpg-error=1.51-4
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgpg-error/libgpg-error_1.51-4.dsc' libgpg-error_1.51-4.dsc 2956 SHA512:acc7f3b775e622d69b8cb62a249bbfd2bee8fe3f09568ed7bb80c17536b45effb228531a4e0edad795d77a2267aad5267416938603a22113dc265dfdb8c756e8
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgpg-error/libgpg-error_1.51.orig.tar.bz2' libgpg-error_1.51.orig.tar.bz2 1085510 SHA512:4489f615c6a0389577a7d1fd7d3917517bb2fe032abd9a6d87dfdbd165dabcf53f8780645934020bf27517b67a064297475888d5b368176cf06bc22f1e735e2b
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgpg-error/libgpg-error_1.51.orig.tar.bz2.asc' libgpg-error_1.51.orig.tar.bz2.asc 228 SHA512:526890917db6547b6b2fb5a462c2a74501187579e4f156845952ebfb01595a77a0eda94b24350349abaee3ee8caac1d7ea6da005115467b5892c758842af3003
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgpg-error/libgpg-error_1.51-4.debian.tar.xz' libgpg-error_1.51-4.debian.tar.xz 22332 SHA512:b94a5e257e623e40c02a0495b1b3abb3e08daa6c0be307a829910c1c156f9612049619db0b4cacebc9134a14347e9e12881e6df9e8ad49aed7f92fd98e8f7342
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
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libidn2/libidn2_2.3.8-2.dsc' libidn2_2.3.8-2.dsc 2961 SHA512:142c67327595556c9e180da78aaf9792f7093742312cc3648a52c1d9f4a6ea934005f9c54b091b4d0fa7af7eed0819fe10012d50c3eae7d9a4ee6b774aef0179
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libidn2/libidn2_2.3.8.orig.tar.gz' libidn2_2.3.8.orig.tar.gz 718637 SHA512:e3f4ec5113f531d2b1827a11d7292318fdc49032c013b0076911b075b0e879428db9b45fe137aa37bf9c60e672b6883c035f9f45b2b42625031534965d518bc1
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libidn2/libidn2_2.3.8.orig.tar.gz.asc' libidn2_2.3.8.orig.tar.gz.asc 1223 SHA512:f5c7f1676018b1cd362e250dd8ad59150c34b11ede9a21dbaf6f2e88fa943c881db6e59bf3e9180567379173cb21c4c893d835db99f4ed9e94bd80f84fb8ee2c
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libidn2/libidn2_2.3.8-2.debian.tar.xz' libidn2_2.3.8-2.debian.tar.xz 17532 SHA512:4a321abeeee77f54d310481be841b14efebde37ebc58dc5ba5ef6397643f9f1d71bcd20ea3a52a5ab087bf0b3e3359de74172415264afa4c8bdf8fd62d3fff66
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

### `dpkg` source package: `libpsl=0.21.2-1.1build1`

Binary Packages:

- `libpsl5t64:amd64=0.21.2-1.1build1`

Licenses: (parsed from: `/usr/share/doc/libpsl5t64/copyright`)

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

### `dpkg` source package: `libseccomp=2.5.5-1ubuntu6`

Binary Packages:

- `libseccomp2:amd64=2.5.5-1ubuntu6`

Licenses: (parsed from: `/usr/share/doc/libseccomp2/copyright`)

- `LGPL-2.1`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libselinux=3.8.1-1`

Binary Packages:

- `libselinux1:amd64=3.8.1-1`

Licenses: (parsed from: `/usr/share/doc/libselinux1/copyright`)

- `GPL-2`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris libselinux=3.8.1-1
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libselinux/libselinux_3.8.1-1.dsc' libselinux_3.8.1-1.dsc 3013 SHA512:4fa0806e0ca55a437264d359919dbf0fed36aad39f494cbb7d240b28d1e71527805e09b0a114c1912265a1ea8fc63d77bc5b1421b7b32e3e6febff0ca1881b06
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libselinux/libselinux_3.8.1.orig.tar.gz' libselinux_3.8.1.orig.tar.gz 204411 SHA512:646a31dff3b670a530adb9fc2fdc3ca9fe34a58e67e0fac52cc33bc7a01fa63c175987ef254c6c3bc7299cef137bc6f258dc378f4d70ae5c0fa0ece3bef42ab4
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libselinux/libselinux_3.8.1.orig.tar.gz.asc' libselinux_3.8.1.orig.tar.gz.asc 833 SHA512:ece79feb7758eafb8cf60092039596971140d8af7049671dfa8a7be6cc3167e928e361d8a9b26abfd855520413533890c280eec1e8107b260e3bbadb79c5159a
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libselinux/libselinux_3.8.1-1.debian.tar.xz' libselinux_3.8.1-1.debian.tar.xz 37812 SHA512:1af8b9c1c75f3f90fa86da9a10d09f52c8ffabc284e7d006461bd2f6f836b52f71d84ba13b5c037e36db720896aac48f260303850f37b1ab4400b4474be33673
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
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsemanage/libsemanage_3.8.1-1.dsc' libsemanage_3.8.1-1.dsc 2992 SHA512:4f7a5bb878ca14f351e6e15e0519f311dfe206aa318637349dad52f1b102cb360a4c4247d49396823745199c0bcd5b305e5c400a6cf2a08eeb5ab61efcd829f1
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsemanage/libsemanage_3.8.1.orig.tar.gz' libsemanage_3.8.1.orig.tar.gz 184618 SHA512:ac3729ba4934a48a33e082af35baa9e25e6806855afb0f0e4e22aa67be201518c3d4933b8cf4dec83e5acbe178301276f51850bb1b16bc13e027a470ac7f1eb5
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsemanage/libsemanage_3.8.1.orig.tar.gz.asc' libsemanage_3.8.1.orig.tar.gz.asc 833 SHA512:b21cf3e0a5e28ddddaaded81fc00080d13a8aaac44357bf980fa1c28899e50e0791b66f407eaffd6ce0719caee356e02e576947949cf5cb34665fe0bb90f7108
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsemanage/libsemanage_3.8.1-1.debian.tar.xz' libsemanage_3.8.1-1.debian.tar.xz 37572 SHA512:70cd6ee56d4af85bdd944267519ba90482c85a294baa0b634316e464c260f3f00a1f0084120a0cc257ee4179eedb3765dd91318648b184d678ad18980663674c
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
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsepol/libsepol_3.8.1-1.dsc' libsepol_3.8.1-1.dsc 2347 SHA512:a87f034f24b7bba40b77f66cee5bfaa42121c2a55d70e9f86fd4d3cd760fe52aca247176ea904ead56bf5d0257e8d31215816dc3df697de5391b6d395fcc6e04
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsepol/libsepol_3.8.1.orig.tar.gz' libsepol_3.8.1.orig.tar.gz 513830 SHA512:6a66fbbc25f4ca5f58b07d19a70f3f6c233594ea5bc5a9f5d9f008eb03a83cea84ae0f03329f340b95e4f7135981d06cb9e66a7b3ca2f1494a71bbdcb5a01665
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsepol/libsepol_3.8.1.orig.tar.gz.asc' libsepol_3.8.1.orig.tar.gz.asc 833 SHA512:855233e6aec9e1cdff00c45edabd0a3a8de06bcd92edb0e3d3cf825e4cf4490c00c7094ca5350407e48e4ee40611a0405d58a54bde72491a8aff28f81771a54d
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsepol/libsepol_3.8.1-1.debian.tar.xz' libsepol_3.8.1-1.debian.tar.xz 21432 SHA512:a2d773bb641dda5e9d1c08f7ff1c6b9963801beb57126b30d60d5146692179e01d97b80cd12a388fec9e0a0545351fbaa4618dc8797b29a84b02e0e69711bab6
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
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libssh2/libssh2_1.11.1-1.dsc' libssh2_1.11.1-1.dsc 2319 SHA512:e59c2d3bd93ca324d3876089fdaff21964e6c16a5cbcd523159fa15107d2dee3c700ba70794ed7062970fd513f8067dff1df3d50fcf1e0a780acebc9c5727ed1
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libssh2/libssh2_1.11.1.orig.tar.gz' libssh2_1.11.1.orig.tar.gz 1093012 SHA512:8703636fc28f0b12c8171712f3d605e0466a5bb9ba06e136c3203548fc3408ab07defd71dc801d7009a337e1e02fd60e8933a2a526d5ef0ce53153058d201233
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libssh2/libssh2_1.11.1.orig.tar.gz.asc' libssh2_1.11.1.orig.tar.gz.asc 488 SHA512:83e600ddd676013932297c4f3d2cf2e65b5308f7700d818b34f30d760c7495180e6d8dae70579c8bea95ea2d7ccb12fc42641e545e11ec4b6630a0e6b350b282
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libssh2/libssh2_1.11.1-1.debian.tar.xz' libssh2_1.11.1-1.debian.tar.xz 17136 SHA512:3ba3f52dc0ec7dee76952662e8628a56ef764b7b47405d311cc88ccc0484273e61452024902bfc4e32e5ce86fe041480c55c507dbafd060544e14c3acc10bebb
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
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtasn1-6/libtasn1-6_4.20.0-2.dsc' libtasn1-6_4.20.0-2.dsc 2665 SHA512:250e24dd3def4ee1fde380a2d1d323461e03fb54a8d729481ebffc4d81229aa5261b5045dd427b3e413d5a040cd8d882f98cc002c798d5ae5ebd1e2abab6a896
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtasn1-6/libtasn1-6_4.20.0.orig.tar.gz' libtasn1-6_4.20.0.orig.tar.gz 1783873 SHA512:0c0660085f5e80537aa3d65197967029be6cc5e27d7029789713902989c1694fdb49421ae0415b79b953e11893bb4bdaada85f7aff847dd0bb4075c91887e7b4
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtasn1-6/libtasn1-6_4.20.0.orig.tar.gz.asc' libtasn1-6_4.20.0.orig.tar.gz.asc 1223 SHA512:bb5da128c20ed8f1e7c681c779ac3d2e455c661d779a4a7a70a6cabc1ea4139df9d0acfd145545acc8fe41df6490fd7d3c2df4b8d7560891291abbf56ac3afdb
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtasn1-6/libtasn1-6_4.20.0-2.debian.tar.xz' libtasn1-6_4.20.0-2.debian.tar.xz 18640 SHA512:9db15608ffaf0aaf9be92fe0654f4cdc37e59eebcc35cc0e136779965efdc53944f09aacabece25b3f571981ebd8659621f1e3f0a2b6a8ebb625eaa645f14a93
```

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
'http://archive.ubuntu.com/ubuntu/pool/main/libu/libunistring/libunistring_1.3-2.dsc' libunistring_1.3-2.dsc 2215 SHA512:b5f352f94a03ff54581afe4cd88b1e5ffac6ae7fd45c95bc55f2cc3de24090a0c18d948a43405443388d42e537488c36d4638e33b81061f45f5c591d472148f9
'http://archive.ubuntu.com/ubuntu/pool/main/libu/libunistring/libunistring_1.3.orig.tar.xz' libunistring_1.3.orig.tar.xz 2753448 SHA512:864d42b1d4ae4941fe5c8327d6726ab8e3a35d2d5f9d25ce4859a72ab2f549a7b68f58638cf8767d863f58161d1a4053495d185860964a942d6750e42facf931
'http://archive.ubuntu.com/ubuntu/pool/main/libu/libunistring/libunistring_1.3.orig.tar.xz.asc' libunistring_1.3.orig.tar.xz.asc 833 SHA512:829229528acc8f9d13de4c43fea6caddacaf1f1cc201a7927b2c140d7ac5a81e213a1a20ba67766d6867fbe301ddddf78685f5af54e67906160807d6e8028b5a
'http://archive.ubuntu.com/ubuntu/pool/main/libu/libunistring/libunistring_1.3-2.debian.tar.xz' libunistring_1.3-2.debian.tar.xz 28480 SHA512:31079e73da30c7e0eab7bf1fa81936d2655df6f7d216fdfae418c54b8c168828d467af9cde17c2f9102a4479260c74a63cb50701ede8652097efbe47eb6086e5
```

### `dpkg` source package: `libxcrypt=1:4.4.38-1`

Binary Packages:

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

### `dpkg` source package: `libzstd=1.5.7+dfsg-1build1`

Binary Packages:

- `libzstd1:amd64=1.5.7+dfsg-1build1`

Licenses: (parsed from: `/usr/share/doc/libzstd1/copyright`)

- `BSD-3-clause`
- `Expat`
- `GPL-2`
- `zlib`

Source:

```console
$ apt-get source -qq --print-uris libzstd=1.5.7+dfsg-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/libz/libzstd/libzstd_1.5.7%2bdfsg-1build1.dsc' libzstd_1.5.7+dfsg-1build1.dsc 2395 SHA512:2192492db6f5ee2dfd1dee7eecee69a93ef5e74c070156798e70578f15d263a50eb12d070a389372530cefa4378304bc9e4b550b809f308eb77d4a5f7c8653c1
'http://archive.ubuntu.com/ubuntu/pool/main/libz/libzstd/libzstd_1.5.7%2bdfsg.orig.tar.xz' libzstd_1.5.7+dfsg.orig.tar.xz 1834780 SHA512:74604a877f899df6a47e88b895334c0fe35af9d096d472f535e772b156bf61e5529833173ea766dbf5e58fc20ce40a2e47ff1cbed8ff7f2bbd506c6634ae5145
'http://archive.ubuntu.com/ubuntu/pool/main/libz/libzstd/libzstd_1.5.7%2bdfsg-1build1.debian.tar.xz' libzstd_1.5.7+dfsg-1build1.debian.tar.xz 23108 SHA512:a83443c8aed0f4ff3430c87d8eef120e7e926b5d53759d8632c0c618007bce76df1099a0498f442d02284dd32a6f426a8f258490513357a7502c30279b50668e
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
'http://archive.ubuntu.com/ubuntu/pool/main/l/lz4/lz4_1.10.0-4.dsc' lz4_1.10.0-4.dsc 1941 SHA512:359c0b31d3ea1017f7beac58a54394ca547b5656d0d02fe6685ed854486166ab17f10fcfaf052d0b4e94d802f6ed3b7bdd555652ebbe6d79a6d079ffc19acd1c
'http://archive.ubuntu.com/ubuntu/pool/main/l/lz4/lz4_1.10.0.orig.tar.gz' lz4_1.10.0.orig.tar.gz 387114 SHA512:8c4ceb217e6dc8e7e0beba99adc736aca8963867bcf9f970d621978ba11ce92855912f8b66138037a1d2ae171e8e17beb7be99281fea840106aa60373c455b28
'http://archive.ubuntu.com/ubuntu/pool/main/l/lz4/lz4_1.10.0-4.debian.tar.xz' lz4_1.10.0-4.debian.tar.xz 8080 SHA512:66d6522837ddda23e264f4cbf6c08506868c29183ce476f06297732b6d5d4746ece4e99f6797741f55accbed188d13ab9889cd571dedf38c3b0e8f365323e27e
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
'http://archive.ubuntu.com/ubuntu/pool/main/m/mawk/mawk_1.3.4.20250131-1.dsc' mawk_1.3.4.20250131-1.dsc 2969 SHA512:59ace327f075ca3a95ecb593157d1b3d447ec1a8e82cd6b0c95fe721cec780261549d443d33f9745e655c711c2c2c9cfe1196bc9c6c1b10ee84cf6b02c059394
'http://archive.ubuntu.com/ubuntu/pool/main/m/mawk/mawk_1.3.4.20250131.orig.tar.gz' mawk_1.3.4.20250131.orig.tar.gz 433213 SHA512:100b1f5ee190d2841d5dee449c53601a6d32453e47b232de919f3489f6f7040d0c6d21f6c7d30df616b04abde2db9799c5eb16570c1f88dbc10fcd75c5838042
'http://archive.ubuntu.com/ubuntu/pool/main/m/mawk/mawk_1.3.4.20250131.orig.tar.gz.asc' mawk_1.3.4.20250131.orig.tar.gz.asc 729 SHA512:0d8ac93bdafcd8915b0d2d2b675f8d5cf2aeba655cd04af4b4037336b74b320e02db360b7d18b796aedc09fbabc8a42e471766ea24219bad7a1cbff4f7679552
'http://archive.ubuntu.com/ubuntu/pool/main/m/mawk/mawk_1.3.4.20250131-1.debian.tar.xz' mawk_1.3.4.20250131-1.debian.tar.xz 16008 SHA512:c4ebe147a302078a8dfe4f064a988f6dbce748c236c4df237a58190de56fc2abab6fd4c47cd0d6ea28dc44a3286d1cf7ad2e8f6661578495a0f168a574bc6cf8
```

### `dpkg` source package: `media-types=13.0.0`

Binary Packages:

- `media-types=13.0.0`

Licenses: (parsed from: `/usr/share/doc/media-types/copyright`)

- `ad-hoc`

Source:

```console
$ apt-get source -qq --print-uris media-types=13.0.0
'http://archive.ubuntu.com/ubuntu/pool/main/m/media-types/media-types_13.0.0.dsc' media-types_13.0.0.dsc 1647 SHA512:09ef23639d7e42320e574b424e4327410cc1a163b4a69e6593471f1b6081934e64d358ef429158a2c7eaea41e59f652c4e8b7097087366043ee728d427920deb
'http://archive.ubuntu.com/ubuntu/pool/main/m/media-types/media-types_13.0.0.tar.xz' media-types_13.0.0.tar.xz 62960 SHA512:93231661b4bafa3ec3150ef4e440cfa20fdd7c1764b497efcbcb63079cb8501ebaed13075cbe7773996d66cda76c0ca59f2eae615663615b0444bb38670f78b9
```

### `dpkg` source package: `mercurial=7.0.1-2`

Binary Packages:

- `mercurial=7.0.1-2`
- `mercurial-common=7.0.1-2`

Licenses: (parsed from: `/usr/share/doc/mercurial/copyright`, `/usr/share/doc/mercurial-common/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris mercurial=7.0.1-2
'http://archive.ubuntu.com/ubuntu/pool/universe/m/mercurial/mercurial_7.0.1-2.dsc' mercurial_7.0.1-2.dsc 2881 SHA512:9c09f0df68a4eb043866ab2eb44cb33a79786fc104940bc251db2a2ab790b7e40457c2b5bebd9e2576c78e8d8bca40fa1e12da0c237d82c236f32b78fdcc70f8
'http://archive.ubuntu.com/ubuntu/pool/universe/m/mercurial/mercurial_7.0.1.orig.tar.gz' mercurial_7.0.1.orig.tar.gz 8981165 SHA512:42abab36e17c2edee2dc715a1af684540b21ab2fc7058335e5a166db90c36f9217dc15bf94daeaf45e7ac725f1fc849bf0ec54d06e9fa307a041f34d768a8fb3
'http://archive.ubuntu.com/ubuntu/pool/universe/m/mercurial/mercurial_7.0.1.orig.tar.gz.asc' mercurial_7.0.1.orig.tar.gz.asc 833 SHA512:74d47f413c4038cbfa4377f2177e26df0cc26795fd55fbc25a9b2e64005591b0e1646bd9778e6c6978004b0f9d37a828ecb9fab62f07bd581236826fa08d1dce
'http://archive.ubuntu.com/ubuntu/pool/universe/m/mercurial/mercurial_7.0.1-2.debian.tar.xz' mercurial_7.0.1-2.debian.tar.xz 55672 SHA512:cea247268a72c2f47ad9f14bebe2941f9be2450ebf4e4a23d4c769617bc4458bc95ddf3500b87751839b907f6adf007645f83c33edb23e00973484dc032c9700
```

### `dpkg` source package: `ncurses=6.5+20250216-2`

Binary Packages:

- `libncursesw6:amd64=6.5+20250216-2`
- `libtinfo6:amd64=6.5+20250216-2`
- `ncurses-base=6.5+20250216-2`
- `ncurses-bin=6.5+20250216-2`

Licenses: (parsed from: `/usr/share/doc/libncursesw6/copyright`, `/usr/share/doc/libtinfo6/copyright`, `/usr/share/doc/ncurses-base/copyright`, `/usr/share/doc/ncurses-bin/copyright`)

- `BSD-3-clause`
- `MIT/X11`
- `X11`

Source:

```console
$ apt-get source -qq --print-uris ncurses=6.5+20250216-2
'http://archive.ubuntu.com/ubuntu/pool/main/n/ncurses/ncurses_6.5%2b20250216-2.dsc' ncurses_6.5+20250216-2.dsc 3890 SHA512:31270767544127e7606435e7f3c7863f6891527cf865172103c355ffca20ef541511aa34524d95a67fa0834d6db81007c933a4b44b1cb075a59048827a5156dd
'http://archive.ubuntu.com/ubuntu/pool/main/n/ncurses/ncurses_6.5%2b20250216.orig.tar.gz' ncurses_6.5+20250216.orig.tar.gz 3774714 SHA512:c1f4b59469e553716371950036d707e1acc2363a100ba97fdc76713994fc20aa2003e97ad5b0f036f128546566f039cc6731ed32ceb06aae390937fe74a7f13f
'http://archive.ubuntu.com/ubuntu/pool/main/n/ncurses/ncurses_6.5%2b20250216.orig.tar.gz.asc' ncurses_6.5+20250216.orig.tar.gz.asc 729 SHA512:245c5f9b521415da59e78d1ba830f291a97cbe0d231e0303c1dbf3bc4f0cfee58799ec96fb58aec453f12fda8a2a286ef25d421442d3535818d3653c7435f662
'http://archive.ubuntu.com/ubuntu/pool/main/n/ncurses/ncurses_6.5%2b20250216-2.debian.tar.xz' ncurses_6.5+20250216-2.debian.tar.xz 50420 SHA512:9320a766d0122da06330f6bbcf14aa5fc13b600ea76b0a2a060a620c16e443c4f3d318c47668a0acb72ed257f8400fa3b262ce9c904332af482a81bceef889e7
```

### `dpkg` source package: `netbase=6.5`

Binary Packages:

- `netbase=6.5`

Licenses: (parsed from: `/usr/share/doc/netbase/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris netbase=6.5
'http://archive.ubuntu.com/ubuntu/pool/main/n/netbase/netbase_6.5.dsc' netbase_6.5.dsc 899 SHA512:1092aa10f8b59cbd88bd382fcd3042fdc1b1344af98de75b7cf2cfdaa005e164fcea2ea604652936dfdaeb0d79430b083782794a0f79d1cab5dec615e7acda26
'http://archive.ubuntu.com/ubuntu/pool/main/n/netbase/netbase_6.5.tar.xz' netbase_6.5.tar.xz 32544 SHA512:d64a5dc98bfa3ecef65cb061888fb8a948e853692fd56b523409304df9b5426369ec3c9b61731cacaadab5876ec24bb63631fece935641b533a8763792311fb3
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
'http://archive.ubuntu.com/ubuntu/pool/main/n/nettle/nettle_3.10.1-1.dsc' nettle_3.10.1-1.dsc 2053 SHA512:f72ed4ec2168e73e16a49f7af1730c3152503f544c9e4a3a75003db8b107b48c82cca0425dfb860cf33b110bd440077523980472559b128201d613e55a4331ad
'http://archive.ubuntu.com/ubuntu/pool/main/n/nettle/nettle_3.10.1.orig.tar.gz' nettle_3.10.1.orig.tar.gz 2643267 SHA512:e8673bbcde9cde859ccae75ed6c9c30591e68a995a7c6d724106cfd67a5a5bd45b3468d742443b6565628849d0fd29505a28ca5ee4e89dd13197cdb51429f96c
'http://archive.ubuntu.com/ubuntu/pool/main/n/nettle/nettle_3.10.1-1.debian.tar.xz' nettle_3.10.1-1.debian.tar.xz 25036 SHA512:2e28dec9813cae7fc0a28262f56c7e671521dac4b54266538c67f445773af41b7a8070caa5f40c39c2d4e50730993e12089297c7dd6f8efe65e8455f2a795902
```

### `dpkg` source package: `nghttp2=1.64.0-1.1build1`

Binary Packages:

- `libnghttp2-14:amd64=1.64.0-1.1build1`

Licenses: (parsed from: `/usr/share/doc/libnghttp2-14/copyright`)

- `BSD-2-clause`
- `Expat`
- `GPL-3`
- `GPL-3+ with autoconf exception`
- `MIT`
- `all-permissive`

Source:

```console
$ apt-get source -qq --print-uris nghttp2=1.64.0-1.1build1
'http://archive.ubuntu.com/ubuntu/pool/main/n/nghttp2/nghttp2_1.64.0-1.1build1.dsc' nghttp2_1.64.0-1.1build1.dsc 2538 SHA512:1c2dafd71567ef061aef83645374621a06db8ef2785611a8ae35158901d101c2ff9764501af9e31b3fa25ca3a585ff1af553b903b1af04850995f1b60790f585
'http://archive.ubuntu.com/ubuntu/pool/main/n/nghttp2/nghttp2_1.64.0.orig.tar.gz' nghttp2_1.64.0.orig.tar.gz 1069782 SHA512:35f8230a0fa2825f0bc400d4852d8e8b484f659c67b00639ccd074a0029088f016e967db2f62b6b64af1f8ef684f5809a833e7f922e38b9405f7cc7756bcfb75
'http://archive.ubuntu.com/ubuntu/pool/main/n/nghttp2/nghttp2_1.64.0-1.1build1.debian.tar.xz' nghttp2_1.64.0-1.1build1.debian.tar.xz 39428 SHA512:76c5ae970719067d9be67c99494784fee3715cd0f33031c1c2b0e757c702bc3bfaba1becd58c7f176f4bfd8a0349aa06b15bc6ff59cbe83b79556d9994465c80
```

### `dpkg` source package: `npth=1.8-3`

Binary Packages:

- `libnpth0t64:amd64=1.8-3`

Licenses: (parsed from: `/usr/share/doc/libnpth0t64/copyright`)

- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris npth=1.8-3
'http://archive.ubuntu.com/ubuntu/pool/main/n/npth/npth_1.8-3.dsc' npth_1.8-3.dsc 2188 SHA512:8421638b6566673ba904e22d04efe1b6b9da3acf7a1481e5dd9d5d2feeeb15bcd68d19b57a484baf1e2133cba227c0c0173619519a6db8959fa71ca2f842480f
'http://archive.ubuntu.com/ubuntu/pool/main/n/npth/npth_1.8.orig.tar.bz2' npth_1.8.orig.tar.bz2 317739 SHA512:34fdeea3d8a7a594d8fdbcc6d5d389b5c8e282e8e84c1491b1e51960c0fa007df6a1d62543f0107f0772f3215557d4b25c2a9c7067cb0ae2f8de7b4d63d09fb4
'http://archive.ubuntu.com/ubuntu/pool/main/n/npth/npth_1.8.orig.tar.bz2.asc' npth_1.8.orig.tar.bz2.asc 390 SHA512:2d2d26d2bde77997187792f724b89b6c1ba7ad845c0087d78d7bd2eef688136df8fa8ea02c5199c0a3ad602bf228af0fadf82ecd3ff4b9ed35c71d009bb2e1a5
'http://archive.ubuntu.com/ubuntu/pool/main/n/npth/npth_1.8-3.debian.tar.xz' npth_1.8-3.debian.tar.xz 8668 SHA512:a7fbc1c6106e04988fe6b18adf35a00bb7fe50e7212b046309a4dd42c90d7fc788a4d03abf2c628bd108db9ecfd2ec26aaa0d32b19a699a5f333daae446d5cc3
```

### `dpkg` source package: `openldap=2.6.9+dfsg-2ubuntu1`

Binary Packages:

- `libldap-common=2.6.9+dfsg-2ubuntu1`
- `libldap2:amd64=2.6.9+dfsg-2ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libldap-common/copyright`, `/usr/share/doc/libldap2/copyright`)

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
$ apt-get source -qq --print-uris openldap=2.6.9+dfsg-2ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/o/openldap/openldap_2.6.9%2bdfsg-2ubuntu1.dsc' openldap_2.6.9+dfsg-2ubuntu1.dsc 3377 SHA512:2e96420e2415ed996eec4cac9fc98daa1a309db3a1849251008fc507cf1f714647ad401bd1387baa9139c09352b156b7c94ea5505228d8a2733f1e7d8da8ff11
'http://archive.ubuntu.com/ubuntu/pool/main/o/openldap/openldap_2.6.9%2bdfsg.orig.tar.xz' openldap_2.6.9+dfsg.orig.tar.xz 3753260 SHA512:0789b8ad8b2ede51741e18e3f090a258edc7abeda90cfadae98b9a22126be901f3640d4121411836608918418108dfb71ae0957dbd251d9c3ce6bd1b854dd799
'http://archive.ubuntu.com/ubuntu/pool/main/o/openldap/openldap_2.6.9%2bdfsg-2ubuntu1.debian.tar.xz' openldap_2.6.9+dfsg-2ubuntu1.debian.tar.xz 184328 SHA512:519c318c45e9d536aa71a8902746c5fe67ea3069939dc447a0534b4749f1f28ff88585b168b87e42f524a2dc92bc96d2345b1a5d0265f20857c42a7431e0b68d
```

### `dpkg` source package: `openssh=1:9.9p1-3ubuntu3.1`

Binary Packages:

- `openssh-client=1:9.9p1-3ubuntu3.1`

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
$ apt-get source -qq --print-uris openssh=1:9.9p1-3ubuntu3.1
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssh/openssh_9.9p1-3ubuntu3.1.dsc' openssh_9.9p1-3ubuntu3.1.dsc 3488 SHA512:a77de83df0e5dd71bdd3dabed2ff1f99875d1c74a2d0046291065df8878b71dcf30d5b8f01485fa1c95acbab6b1e403f766a45c1c59fe222ac33398c969775b8
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssh/openssh_9.9p1.orig.tar.gz' openssh_9.9p1.orig.tar.gz 1964864 SHA512:3cc0ed97f3e29ecbd882eca79239f02eb5a1606fce4f3119ddc3c5e86128aa3ff12dc85000879fccc87b60e7d651cfe37376607ac66075fede2118deaa685d6d
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssh/openssh_9.9p1.orig.tar.gz.asc' openssh_9.9p1.orig.tar.gz.asc 833 SHA512:916e975c54eb68c0b2f0b0006522b241cbe54c4caa88d31537a6278490c93d9d732c2ab3a080ac084bf75cbdd5402901ec68583cbe7c7cde4a8e40e7a8b78c28
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssh/openssh_9.9p1-3ubuntu3.1.debian.tar.xz' openssh_9.9p1-3ubuntu3.1.debian.tar.xz 212396 SHA512:1e2e866c2dfa109c148a22f096102d9884014857eb263020e31ba182cf2d5c6baca0f936e5f9d7f19ad165ef609f5169bbcb66ccec4a9140aba16ab4f66e31fc
```

### `dpkg` source package: `openssl=3.4.1-1ubuntu3`

Binary Packages:

- `libssl3t64:amd64=3.4.1-1ubuntu3`
- `openssl=3.4.1-1ubuntu3`
- `openssl-provider-legacy=3.4.1-1ubuntu3`

Licenses: (parsed from: `/usr/share/doc/libssl3t64/copyright`, `/usr/share/doc/openssl/copyright`, `/usr/share/doc/openssl-provider-legacy/copyright`)

- `Apache-2.0`
- `Artistic`
- `GPL-1`
- `GPL-1+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `p11-kit=0.25.5-2ubuntu3`

Binary Packages:

- `libp11-kit0:amd64=0.25.5-2ubuntu3`

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


### `dpkg` source package: `pam=1.5.3-7ubuntu5`

Binary Packages:

- `libpam-modules:amd64=1.5.3-7ubuntu5`
- `libpam-modules-bin=1.5.3-7ubuntu5`
- `libpam-runtime=1.5.3-7ubuntu5`
- `libpam0g:amd64=1.5.3-7ubuntu5`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `pcre2=10.45-1`

Binary Packages:

- `libpcre2-8-0:amd64=10.45-1`

Licenses: (parsed from: `/usr/share/doc/libpcre2-8-0/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `BSD-3-clause-Cambridge with BINARY LIBRARY-LIKE PACKAGES exception`
- `X11`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris pcre2=10.45-1
'http://archive.ubuntu.com/ubuntu/pool/main/p/pcre2/pcre2_10.45-1.dsc' pcre2_10.45-1.dsc 2337 SHA512:97973e68d44bc30766050038affbf71d06130d62971d050d6b09d2af1bfe9b8072ebc00c7275c3d1ff6963716b2d5cd0358135ccf73ecb34fbd3b76cea922c05
'http://archive.ubuntu.com/ubuntu/pool/main/p/pcre2/pcre2_10.45.orig.tar.gz' pcre2_10.45.orig.tar.gz 2715958 SHA512:6ec01a05ce65be61e5974dcc2ccd2e2b5c6db183e3a592530205c7d3259b730df3a9ab999d204f3c52e5a14ae88f32f94306b4501eb9629568ce6158985e2fa6
'http://archive.ubuntu.com/ubuntu/pool/main/p/pcre2/pcre2_10.45-1.diff.gz' pcre2_10.45-1.diff.gz 8659 SHA512:2c7444846c31495693f5b94357a9f94b3ccb1664ee9eff68433fc4d0e94dbbf32eb24611718daf8338466283d450bfab547946aabae990803c61efeb091b7964
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
'http://archive.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.40.1-3.dsc' perl_5.40.1-3.dsc 2372 SHA512:096e4d6ca6fd31b114744058a378db78cd66957ca7d84f71fc452a4f338ccb3fed2d92e389be9ff5a93233d2b26dd3aa14e3da78f53b1dcc80ecd68ed94d1b4d
'http://archive.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.40.1.orig-regen-configure.tar.xz' perl_5.40.1.orig-regen-configure.tar.xz 421056 SHA512:933261779f476b0edda581270949c92e8e7dbe4bcaf1417398e708a321cdb748fe329acb703b2e74446cdfb03c20cefcab1eb972b852418ed3ea9b870db1fa86
'http://archive.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.40.1.orig.tar.xz' perl_5.40.1.orig.tar.xz 13930924 SHA512:3ff16b3462ce43ff38dab21b3dfc20f81772b8c9eac19ab96ba2d5e6cbb390e2302fa76c4879f915249357cd11c7ec0d548bcbf3ab2c156df1b9fca95da3f545
'http://archive.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.40.1-3.debian.tar.xz' perl_5.40.1-3.debian.tar.xz 167844 SHA512:790047da8e61cabb7ac3d0aff715cdf86a9757ca1858d1fdeb4f7679f1a1aaeec9d9289be848058849bd801d52da0e0eafe88711d4c31c5ba3d2e34a9db08e57
```

### `dpkg` source package: `pinentry=1.3.1-2ubuntu3`

Binary Packages:

- `pinentry-curses=1.3.1-2ubuntu3`

Licenses: (parsed from: `/usr/share/doc/pinentry-curses/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-3`
- `LGPL-3+`
- `X11`

Source:

```console
$ apt-get source -qq --print-uris pinentry=1.3.1-2ubuntu3
'http://archive.ubuntu.com/ubuntu/pool/main/p/pinentry/pinentry_1.3.1-2ubuntu3.dsc' pinentry_1.3.1-2ubuntu3.dsc 3384 SHA512:5772b45e2d27342da414c513462675f987b3673efc7147bf92a6c479c4b2a7ca2a0d1a6051edaefe2d2a0fb6b1d866ef15f6523a17bebed7dae10ebe4a4f697b
'http://archive.ubuntu.com/ubuntu/pool/main/p/pinentry/pinentry_1.3.1.orig.tar.bz2' pinentry_1.3.1.orig.tar.bz2 611233 SHA512:3b72034dc1792b1475acb6d605ff7c1bd7647a0f02d1b6bdcd475acdef24bc802f49e275055436c3271261c4b7a64168477a698aab812a145962146b2f67a0e2
'http://archive.ubuntu.com/ubuntu/pool/main/p/pinentry/pinentry_1.3.1.orig.tar.bz2.asc' pinentry_1.3.1.orig.tar.bz2.asc 390 SHA512:499926442059c8f349b66beb16b6cf22cf0919b65a601af1bd0d60c96f60d44e0ad2bd090324585da5cb09e75286e11a4b92c553aec43b87f6cbe8a1e599882c
'http://archive.ubuntu.com/ubuntu/pool/main/p/pinentry/pinentry_1.3.1-2ubuntu3.debian.tar.xz' pinentry_1.3.1-2ubuntu3.debian.tar.xz 23960 SHA512:ce3ac0abab9cc57ba9f2f41526190e5aef2e65aee09c8348b501abee1b7d604e95cfcf607737ceb5427c5f5258dee14143b02fa472382b8e498d3071822dfc16
```

### `dpkg` source package: `procps=2:4.0.4-7ubuntu1`

Binary Packages:

- `libproc2-0:amd64=2:4.0.4-7ubuntu1`
- `procps=2:4.0.4-7ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libproc2-0/copyright`, `/usr/share/doc/procps/copyright`)

- `GPL-2`
- `GPL-2.0+`
- `LGPL-2`
- `LGPL-2.0+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris procps=2:4.0.4-7ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/p/procps/procps_4.0.4-7ubuntu1.dsc' procps_4.0.4-7ubuntu1.dsc 2231 SHA512:838b2c69725050eda8d6ab3e4297593a1e89f16b86ad5ff8d8fe3413efc3686f11d3e1c8e04ede0ab6e22106a360f1861db614614a8ad46fc98b76523ac1518f
'http://archive.ubuntu.com/ubuntu/pool/main/p/procps/procps_4.0.4.orig.tar.xz' procps_4.0.4.orig.tar.xz 1401540 SHA512:94375544e2422fefc23d7634063c49ef1be62394c46039444f85e6d2e87e45cfadc33accba5ca43c96897b4295bfb0f88d55a30204598ddb26ef66f0420cefb4
'http://archive.ubuntu.com/ubuntu/pool/main/p/procps/procps_4.0.4-7ubuntu1.debian.tar.xz' procps_4.0.4-7ubuntu1.debian.tar.xz 38588 SHA512:26b50f8931c1df0750e0f7f36d585253a1443367f45242365207b6281b045583397a59f69b40ece53a22115988afd190d4b8742801fe75f852b4565aae228f30
```

### `dpkg` source package: `python3-defaults=3.13.3-1`

Binary Packages:

- `libpython3-stdlib:amd64=3.13.3-1`
- `python3=3.13.3-1`
- `python3-minimal=3.13.3-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/python3-defaults/3.13.3-1/


### `dpkg` source package: `python3.13=3.13.3-4`

Binary Packages:

- `libpython3.13-minimal:amd64=3.13.3-4`
- `libpython3.13-stdlib:amd64=3.13.3-4`
- `python3.13=3.13.3-4`
- `python3.13-minimal=3.13.3-4`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/python3.13/3.13.3-4/


### `dpkg` source package: `readline=8.2-6`

Binary Packages:

- `libreadline8t64:amd64=8.2-6`
- `readline-common=8.2-6`

Licenses: (parsed from: `/usr/share/doc/libreadline8t64/copyright`, `/usr/share/doc/readline-common/copyright`)

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

### `dpkg` source package: `rtmpdump=2.4+20151223.gitfa8646d.1-2build7`

Binary Packages:

- `librtmp1:amd64=2.4+20151223.gitfa8646d.1-2build7`

Licenses: (parsed from: `/usr/share/doc/librtmp1/copyright`)

- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris rtmpdump=2.4+20151223.gitfa8646d.1-2build7
'http://archive.ubuntu.com/ubuntu/pool/main/r/rtmpdump/rtmpdump_2.4%2b20151223.gitfa8646d.1-2build7.dsc' rtmpdump_2.4+20151223.gitfa8646d.1-2build7.dsc 2439 SHA512:5e2fb3986c0f0e2150c6054e0428adbf1719bb0c33f92ae4acb74a11e625d731ede0262f0d8887c769a95a61f3cd4d23d44bf2f375f0153eba6c0f25b68719c5
'http://archive.ubuntu.com/ubuntu/pool/main/r/rtmpdump/rtmpdump_2.4%2b20151223.gitfa8646d.1.orig.tar.gz' rtmpdump_2.4+20151223.gitfa8646d.1.orig.tar.gz 142213 SHA512:bdfcbab73179d614a295a7b136ea4c9d0ce4620883b493f298362784d245608cd6ad4b0ad30f94ed73a086b4555399521ae9e95b6375fce75e455ae68c055e7b
'http://archive.ubuntu.com/ubuntu/pool/main/r/rtmpdump/rtmpdump_2.4%2b20151223.gitfa8646d.1-2build7.debian.tar.xz' rtmpdump_2.4+20151223.gitfa8646d.1-2build7.debian.tar.xz 8464 SHA512:812edf4f933ad0f723404192bfbfceca86e58303169a30e3b1f47781b709b91a259621293533d31d7abd16bc522824e2db325426a4ce9a6b428b88d492ae4c6c
```

### `dpkg` source package: `rust-sequoia-sq=1.3.1-2`

Binary Packages:

- `sq=1.3.1-2`

Licenses: (parsed from: `/usr/share/doc/sq/copyright`)

- `GPL-2`
- `GPL-2.0-or-later`
- `LGPL-2`
- `LGPL-2.0-or-later`

Source:

```console
$ apt-get source -qq --print-uris rust-sequoia-sq=1.3.1-2
'http://archive.ubuntu.com/ubuntu/pool/universe/r/rust-sequoia-sq/rust-sequoia-sq_1.3.1-2.dsc' rust-sequoia-sq_1.3.1-2.dsc 4163 SHA512:557f28801b86868f7e695a966368bf501d05fa1f2d7c5e7e90768259fa247ddd0d87554d7ef19cfc9bccfdba1c11ccab41f6810db9fc09c440f7b1585ecbfff9
'http://archive.ubuntu.com/ubuntu/pool/universe/r/rust-sequoia-sq/rust-sequoia-sq_1.3.1.orig.tar.gz' rust-sequoia-sq_1.3.1.orig.tar.gz 740320 SHA512:3aa4468b7bcb27532907ce759852e6b92b394a2fc91953b9f3723b9deaab3661c84fb298d79ef3332467aa7a5ca1158d6a8bd65dd961d30aafdcfb34a867c880
'http://archive.ubuntu.com/ubuntu/pool/universe/r/rust-sequoia-sq/rust-sequoia-sq_1.3.1-2.debian.tar.xz' rust-sequoia-sq_1.3.1-2.debian.tar.xz 5484 SHA512:6fbf4afad5467af36659ca8792092e6c32ab292fd4774f7a470b54b86a075398d06a4fc07916c3cdfa85c882651fdb8350b1a23fdc7621e6620fada444ed4661
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
'http://archive.ubuntu.com/ubuntu/pool/main/s/sensible-utils/sensible-utils_0.0.25.dsc' sensible-utils_0.0.25.dsc 1718 SHA512:db01b4591b5aa5c047df49de49bb154b02063d06a221cd590ed3211eb549b68c6b4493c96fe50b2ad0f3ceafa28b53fbc082d4433ac2d4f2a6f93558af0ac41b
'http://archive.ubuntu.com/ubuntu/pool/main/s/sensible-utils/sensible-utils_0.0.25.tar.xz' sensible-utils_0.0.25.tar.xz 76132 SHA512:42b3536abbbc70f0c8ac69a6b34ed7c3576d7835ec690f9acd8bb4e57cb22386dd7e22ac5a43b33f3a1f5d04ec2bbc4255119a1e45008cbe632baf61c87fb1e9
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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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
'http://archive.ubuntu.com/ubuntu/pool/main/s/sqlite3/sqlite3_3.46.1-6.dsc' sqlite3_3.46.1-6.dsc 2632 SHA512:e45f4fb4944b79b7c5858d8daa7a1d2b6c0316873014c4bee4fe30b547ac13e2a0792588733509ba6be43e17761ebfced8ca74c60ab0839f5af338ed36a8d4ff
'http://archive.ubuntu.com/ubuntu/pool/main/s/sqlite3/sqlite3_3.46.1.orig-www.tar.xz' sqlite3_3.46.1.orig-www.tar.xz 5861820 SHA512:a5ec0f57d014b2f33d679cfbae0ca1935eb84871376b29216ffcc286a92a363a823ca0ec729a000d702054ee90b2fcc1887c1fb4bebfabcd14894f8ef91b7ad6
'http://archive.ubuntu.com/ubuntu/pool/main/s/sqlite3/sqlite3_3.46.1.orig.tar.xz' sqlite3_3.46.1.orig.tar.xz 8456776 SHA512:47d3c900d95641c89d5d807881e20e97f3b7889cf44c76d48715066ba5c1860defcd17498440d79bcc49b15c2ea28e81ed4b5b159f9e947941e5c1ee27de06ba
'http://archive.ubuntu.com/ubuntu/pool/main/s/sqlite3/sqlite3_3.46.1-6.debian.tar.xz' sqlite3_3.46.1-6.debian.tar.xz 33932 SHA512:3621094c25b6ab349e00c9368ec478fe7de59ca59edc8dc3c1fa92336e7de0b2d0d58856d228215edd265ff47887be1025184ad1786c33086affc1a38d157e20
```

### `dpkg` source package: `subversion=1.14.5-3`

Binary Packages:

- `libsvn1:amd64=1.14.5-3`
- `subversion=1.14.5-3`

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
$ apt-get source -qq --print-uris subversion=1.14.5-3
'http://archive.ubuntu.com/ubuntu/pool/universe/s/subversion/subversion_1.14.5-3.dsc' subversion_1.14.5-3.dsc 4080 SHA512:9b032c2a901679035928ef3f7619b7842292d4f74158b0208d680d48b3fe5dfea544963efa66c35d06dc1df328ecea0c703361154e3a2511b88d92ce2a00f027
'http://archive.ubuntu.com/ubuntu/pool/universe/s/subversion/subversion_1.14.5.orig.tar.gz' subversion_1.14.5.orig.tar.gz 11645728 SHA512:a8e9f5bf9f32e4fa9a5873544c9228a392af0b4ec1126389a98cd8830c0644fc9d4b88bcb800c0e2c40bd58517cfaba23d79164c774d2cb3267a897c1d599634
'http://archive.ubuntu.com/ubuntu/pool/universe/s/subversion/subversion_1.14.5.orig.tar.gz.asc' subversion_1.14.5.orig.tar.gz.asc 2382 SHA512:b85c4d6e77194b5edff12e3e57c7d673226253048ddf3b622bb4dee6a8aed9153d3c69477876a7caae9eebe2ff5930e42993e34c8fc33d9fa65f9a57bc005d24
'http://archive.ubuntu.com/ubuntu/pool/universe/s/subversion/subversion_1.14.5-3.debian.tar.xz' subversion_1.14.5-3.debian.tar.xz 297732 SHA512:e8a5735b03dd93281580562bce537f5884e864ad91aeac83fd92620be1a3db8a77875c45a1c55f13276330ce90375391ef78485ce5e6740dfad040cfad06b9cd
```

### `dpkg` source package: `systemd=257.4-1ubuntu3`

Binary Packages:

- `libsystemd0:amd64=257.4-1ubuntu3`
- `libudev1:amd64=257.4-1ubuntu3`

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


### `dpkg` source package: `sysvinit=3.14-4ubuntu1`

Binary Packages:

- `sysvinit-utils=3.14-4ubuntu1`

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
$ apt-get source -qq --print-uris sysvinit=3.14-4ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/s/sysvinit/sysvinit_3.14-4ubuntu1.dsc' sysvinit_3.14-4ubuntu1.dsc 2234 SHA512:be97da93ce36ad3b7711f196ea0ecb2ee3516a655c3dd6644a0bc1dcb8d39d77fe7de6b99e3e40c7c8f7759d6a01325b08d2077e18cb3155b8123c2e24ca2da4
'http://archive.ubuntu.com/ubuntu/pool/main/s/sysvinit/sysvinit_3.14.orig.tar.gz' sysvinit_3.14.orig.tar.gz 516357 SHA512:557b6ed9090e6594806b71c9fd054f32972fc6e7bffa4ef92a9dda42c5db08100f226b7b43c0433c1a1e9b16a3ebc483cb42d9aa29a5a3cfd5fc1c60984ef478
'http://archive.ubuntu.com/ubuntu/pool/main/s/sysvinit/sysvinit_3.14-4ubuntu1.debian.tar.xz' sysvinit_3.14-4ubuntu1.debian.tar.xz 123480 SHA512:64c33968bbd52ef4841aff5132ba9310fcbfeacbacdf5f502aa1f04ea4fe37f211fde5848ffb6efebee230ca6d9bbc6e66dc0f89b824caec5e7b152f7576a36e
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
'http://archive.ubuntu.com/ubuntu/pool/main/t/tar/tar_1.35%2bdfsg-3.1.dsc' tar_1.35+dfsg-3.1.dsc 2017 SHA512:5659687f13ffd338bb7fb31427d0945dfef0e31cee1f5e646e32884c3927699d007dcb4128c0e5d2c8d886080ba47cfadc7d00abe75ee16c8f5f5ddfbd109e03
'http://archive.ubuntu.com/ubuntu/pool/main/t/tar/tar_1.35%2bdfsg.orig.tar.xz' tar_1.35+dfsg.orig.tar.xz 2111608 SHA512:3aea32b5c8de229131308420d8a7aa57f7fd1b376980456dd1aa66f97509572750c3833ab9cc2edc6fdea51f802033598c83a0d6e7f18680b1638996f0acaae7
'http://archive.ubuntu.com/ubuntu/pool/main/t/tar/tar_1.35%2bdfsg-3.1.debian.tar.xz' tar_1.35+dfsg-3.1.debian.tar.xz 21540 SHA512:dd2f35961b183870644c62191b1cc60c2ddf29127e895757c249e65f2299d8b642b43f57e875f0a68bf894637d83a45132e01eecff361655963dcc1d393b4198
```

### `dpkg` source package: `tzdata=2025b-3ubuntu1`

Binary Packages:

- `tzdata=2025b-3ubuntu1`

Licenses: (parsed from: `/usr/share/doc/tzdata/copyright`)

- `ICU`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris tzdata=2025b-3ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/t/tzdata/tzdata_2025b-3ubuntu1.dsc' tzdata_2025b-3ubuntu1.dsc 2680 SHA512:8becc3875726fdba138887f585d87b91190400185f4d905f0f3305b13f784d8c63c534b8a1907b39c606f2b0f771741c93c2edd238504efbb5dfb8828064c5bd
'http://archive.ubuntu.com/ubuntu/pool/main/t/tzdata/tzdata_2025b.orig.tar.gz' tzdata_2025b.orig.tar.gz 464295 SHA512:7d83741f3cae81fac8131994b43c55b6da7328df18b706e5ee40e9b3212bc506e6f8fc90988b18da424ed59eff69bce593f2783b7b5f18eb483a17aeb94258d6
'http://archive.ubuntu.com/ubuntu/pool/main/t/tzdata/tzdata_2025b.orig.tar.gz.asc' tzdata_2025b.orig.tar.gz.asc 833 SHA512:ad39fe16b32fad7eee27ff968b4e8af23267ce586629ad70e7625136d2c3cc3a42295a87b3dc770c291aa9112c56301629c1fe379735f70008e62864ce4e735a
'http://archive.ubuntu.com/ubuntu/pool/main/t/tzdata/tzdata_2025b-3ubuntu1.debian.tar.xz' tzdata_2025b-3ubuntu1.debian.tar.xz 188516 SHA512:6d898b62361f658a6317bff9a9042db7619cbc16b2558fe6cdc361c0c0f68467c366e23988fea30eeb2b1833e1680877b95cd93efcb1d3219e126601417cfa4b
```

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

### `dpkg` source package: `ucf=3.0052`

Binary Packages:

- `ucf=3.0052`

Licenses: (parsed from: `/usr/share/doc/ucf/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris ucf=3.0052
'http://archive.ubuntu.com/ubuntu/pool/main/u/ucf/ucf_3.0052.dsc' ucf_3.0052.dsc 1512 SHA512:04b2579fe93e2d7275325e229a045012e90535b2d795285403faf25096ec813c8895eef29733638e615f651950e591fe6fc68f0e47710b2c958edbab2254e112
'http://archive.ubuntu.com/ubuntu/pool/main/u/ucf/ucf_3.0052.tar.xz' ucf_3.0052.tar.xz 71488 SHA512:388c59769867d510eb1583dd98168b3bd6cb678bf753cde781b09ad3ebc8d38a1811293253c15dad272cfa529967474dc629f1d27b00fc4473eea6745fdc0b42
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
- `libblkid1:amd64=2.40.2-14ubuntu1`
- `libmount1:amd64=2.40.2-14ubuntu1`
- `libsmartcols1:amd64=2.40.2-14ubuntu1`
- `libuuid1:amd64=2.40.2-14ubuntu1`
- `login=1:4.16.0-2+really2.40.2-14ubuntu1`
- `mount=2.40.2-14ubuntu1`
- `util-linux=2.40.2-14ubuntu1`

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


### `dpkg` source package: `wget=1.25.0-2ubuntu1`

Binary Packages:

- `wget=1.25.0-2ubuntu1`

Licenses: (parsed from: `/usr/share/doc/wget/copyright`)

- `GFDL-1.2`
- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris wget=1.25.0-2ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/w/wget/wget_1.25.0-2ubuntu1.dsc' wget_1.25.0-2ubuntu1.dsc 2358 SHA512:473d7d1f0efdfb44a68bdf7be569f889b46981893d49cf56ef008f725a1e11cdf52b3e6764077d15b60d0b0bdf6acd8caedf66c6b0f90a687749abb39183ba7e
'http://archive.ubuntu.com/ubuntu/pool/main/w/wget/wget_1.25.0.orig.tar.gz' wget_1.25.0.orig.tar.gz 5263736 SHA512:a7ce33c07a1a206a8574b6e9ea7cc5292315df0914edbcf05a014d35ae9e3d24699a46818b409b884ada57428cf30502f4bbb3767cae2c6934e4e7fb2d0c5036
'http://archive.ubuntu.com/ubuntu/pool/main/w/wget/wget_1.25.0.orig.tar.gz.asc' wget_1.25.0.orig.tar.gz.asc 854 SHA512:73915033967f8ac4908bc235441cc74d3b60998d46e3fdd1bba36d680f4747a8eb28a20a7ef696eb3aec0a22ae79b68a1ee7bf1570f89cd26997b99283e73147
'http://archive.ubuntu.com/ubuntu/pool/main/w/wget/wget_1.25.0-2ubuntu1.debian.tar.xz' wget_1.25.0-2ubuntu1.debian.tar.xz 31460 SHA512:d082fc9ba5da757a70eeb24bb2e2278d141c35924930d834721fe10d5b35b1c12e6784958eb85a1cac5c99fc9437eadab2dad692f63914aebdd5bcfb5bc5dff1
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
'http://archive.ubuntu.com/ubuntu/pool/main/x/xxhash/xxhash_0.8.3-2.dsc' xxhash_0.8.3-2.dsc 1969 SHA512:c5cc95f63ea3eab2a2459e01d48a50b729b3af63ad0e3121e2b3776b54f1ab097f827a7cfb95b5d13ff4a1465a3d88f8876b6651f825fedf2f481b77b3118639
'http://archive.ubuntu.com/ubuntu/pool/main/x/xxhash/xxhash_0.8.3.orig.tar.gz' xxhash_0.8.3.orig.tar.gz 1147630 SHA512:8b5c8b9aad4e869f28310b12cc314037feda81d92f26c23eaecdb35dc65042ca2e65f2e9606033e62a31bcc737a9a950500ffcbdb8677d6ab20e820ea14f2b79
'http://archive.ubuntu.com/ubuntu/pool/main/x/xxhash/xxhash_0.8.3-2.debian.tar.xz' xxhash_0.8.3-2.debian.tar.xz 5144 SHA512:737e2b1da8c6abb1c6bd84de7815513dbcbb72312bab4325003bc6bb91e363a44f862360dfd6b47d7286a6a7b59ba8c6892f9027fcda5924ba3d8d7baaee0d38
```

### `dpkg` source package: `xz-utils=5.8.1-1build1`

Binary Packages:

- `liblzma5:amd64=5.8.1-1build1`

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

Source:

```console
$ apt-get source -qq --print-uris xz-utils=5.8.1-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/x/xz-utils/xz-utils_5.8.1-1build1.dsc' xz-utils_5.8.1-1build1.dsc 2728 SHA512:a40b53808c99e10535adcf0ca3c37ceb5aa9bc4170c796e159a214b8ed68bc2248a2beb939b2a2d299c1fa4d2e7d75391cc49762533403df7e45736247177e15
'http://archive.ubuntu.com/ubuntu/pool/main/x/xz-utils/xz-utils_5.8.1.orig.tar.xz' xz-utils_5.8.1.orig.tar.xz 1461872 SHA512:34dbc874a697f4fd17127b3dc828236dd7fd35120a77e0867325273c5d56c4ecddc8a39dce6cbdb3141fff32c56001f4ab18edfa572076d10f2fd55b07ff2b9e
'http://archive.ubuntu.com/ubuntu/pool/main/x/xz-utils/xz-utils_5.8.1.orig.tar.xz.asc' xz-utils_5.8.1.orig.tar.xz.asc 833 SHA512:0d851011a5fdd3d36f42c9ddaf163cacfefb8a38e2ad2a2004cb65cfce7fc5bb3df518f6f4fdd3465881246a578d7c36623fd4ef69f83614604fe1b8c343218b
'http://archive.ubuntu.com/ubuntu/pool/main/x/xz-utils/xz-utils_5.8.1-1build1.debian.tar.xz' xz-utils_5.8.1-1build1.debian.tar.xz 24680 SHA512:0411243787e5b942f08a75dbc86620b5c76b80d242a9649c031ee8f2c9ce105b8d2d742d9acc6a9d224f110b01281302cc1deacef8b9dd5a6e3d83b0be155403
```

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
