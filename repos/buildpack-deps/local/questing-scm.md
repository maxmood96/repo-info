# `buildpack-deps:questing-scm`

## Docker Metadata

- Image ID: `sha256:f9eae77a25dd29c2feb7729c6dba56436a2953d7bd2a17ce374b6e73837e77d3`
- Created: `2025-05-19T22:25:54Z`
- Virtual Size: ~ 270.17 Mb  
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

### `dpkg` source package: `adduser=3.152ubuntu1`

Binary Packages:

- `adduser=3.152ubuntu1`

Licenses: (parsed from: `/usr/share/doc/adduser/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris adduser=3.152ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/a/adduser/adduser_3.152ubuntu1.dsc' adduser_3.152ubuntu1.dsc 1807 SHA512:8578324c707f652ebff795071d35724e0f755457bfe6083dc5343ab969016b78b79e47bf9e3f7026f87708fb07eea8d0a2226669bc42424a9b693cc4e9d96c63
'http://archive.ubuntu.com/ubuntu/pool/main/a/adduser/adduser_3.152ubuntu1.tar.xz' adduser_3.152ubuntu1.tar.xz 337720 SHA512:0e91929dad1189bb67c554644204b222f35a2713310ad59a67eea2a307e9d6cc71c00466e57619bbd04eb5e8673a337e3319d3bd02d88e5498384be77fdf6168
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

### `dpkg` source package: `apt=3.1.5ubuntu1`

Binary Packages:

- `apt=3.1.5ubuntu1`
- `libapt-pkg7.0:amd64=3.1.5ubuntu1`

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
'http://archive.ubuntu.com/ubuntu/pool/main/a/attr/attr_2.5.2-3build1.dsc' attr_2.5.2-3build1.dsc 2501 SHA512:17905511e791b643ffcaf83181474b1d7a7d1c7287adc20e35011c51d729089a2922ef3a41a33337b8a9401567eb7bc4f61e7aed54ba6d9c29d709f9e51c1dd9
'http://archive.ubuntu.com/ubuntu/pool/main/a/attr/attr_2.5.2.orig.tar.xz' attr_2.5.2.orig.tar.xz 334180 SHA512:f587ea544effb7cfed63b3027bf14baba2c2dbe3a9b6c0c45fc559f7e8cb477b3e9a4a826eae30f929409468c50d11f3e7dc6d2500f41e1af8662a7e96a30ef3
'http://archive.ubuntu.com/ubuntu/pool/main/a/attr/attr_2.5.2.orig.tar.xz.asc' attr_2.5.2.orig.tar.xz.asc 833 SHA512:16362013313d055dec307bcf755a9846f5153a78309a499f8cac4ff57a2154de2bc8f3b1400e81dba7a0bf0c67aa02a5d464898ed6e4aa721b64ec95fd313968
'http://archive.ubuntu.com/ubuntu/pool/main/a/attr/attr_2.5.2-3build1.debian.tar.xz' attr_2.5.2-3build1.debian.tar.xz 32316 SHA512:223b89e4a0056bfcde8b3392a703759e004114daafeaee1e17d34078363ba6bb86eb43a45bc397966b27e4b4bd5740f854347de52095d9d95400829e02e8af36
```

### `dpkg` source package: `audit=1:4.0.5-1`

Binary Packages:

- `libaudit-common=1:4.0.5-1`
- `libaudit1:amd64=1:4.0.5-1`

Licenses: (parsed from: `/usr/share/doc/libaudit-common/copyright`, `/usr/share/doc/libaudit1/copyright`)

- `GPL-2`
- `LGPL-2.1`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/audit/1:4.0.5-1/


### `dpkg` source package: `base-files=14ubuntu1`

Binary Packages:

- `base-files=14ubuntu1`

Licenses: (parsed from: `/usr/share/doc/base-files/copyright`)

- `GPL`
- `GPL-2+`
- `verbatim`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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

### `dpkg` source package: `bash=5.2.37-2ubuntu4`

Binary Packages:

- `bash=5.2.37-2ubuntu4`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `bzip2=1.0.8-6`

Binary Packages:

- `libbz2-1.0:amd64=1.0.8-6`

Licenses: (parsed from: `/usr/share/doc/libbz2-1.0/copyright`)

- `BSD-variant`
- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris bzip2=1.0.8-6
'http://archive.ubuntu.com/ubuntu/pool/main/b/bzip2/bzip2_1.0.8-6build1.dsc' bzip2_1.0.8-6build1.dsc 2205 SHA512:47d8fdf23ef3206d24a55f853c22afe119fd7477b5b4216124e660ed1bb480dc1a1e50e37ebbbe230f83ed98ff8df5bf6757637970f4ba4fac16933f3a6ca24a
'http://archive.ubuntu.com/ubuntu/pool/main/b/bzip2/bzip2_1.0.8.orig.tar.gz' bzip2_1.0.8.orig.tar.gz 810029 SHA512:083f5e675d73f3233c7930ebe20425a533feedeaaa9d8cc86831312a6581cefbe6ed0d08d2fa89be81082f2a5abdabca8b3c080bf97218a1bd59dc118a30b9f3
'http://archive.ubuntu.com/ubuntu/pool/main/b/bzip2/bzip2_1.0.8-6build1.debian.tar.bz2' bzip2_1.0.8-6build1.debian.tar.bz2 27106 SHA512:a2ff1b0103beb918d33f75d8e096e9af2c3911604f81468045aa5e7f659f7e203d1144977a52a52b9abc9f1348fff7ed5f2d5bc8874795e68335a939b58a9e13
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

### `dpkg` source package: `cdebconf=0.279ubuntu1`

Binary Packages:

- `libdebconfclient0:amd64=0.279ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libdebconfclient0/copyright`)

- `BSD-2-Clause`
- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris cdebconf=0.279ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/c/cdebconf/cdebconf_0.279ubuntu1.dsc' cdebconf_0.279ubuntu1.dsc 2873 SHA512:fc4801dcb7bf517035d838096503f484bc7443588f17e8f177c5cdc6b865f861d8b14d2d735b82cca59d6583f65e36ea058daed37d1dd71b2890bed2fc42fa04
'http://archive.ubuntu.com/ubuntu/pool/main/c/cdebconf/cdebconf_0.279ubuntu1.tar.xz' cdebconf_0.279ubuntu1.tar.xz 287008 SHA512:f02dec8fe7b34d3ddcabdc5570cb13e34835211d24729f36ea9dd9cc079e746688480b41d7400c5819cbb0340fe82171ed4701b74b1f73645a209305340f67b8
```

### `dpkg` source package: `coreutils-from=0.0.0~ubuntu20`

Binary Packages:

- `coreutils=9.5-1ubuntu2+0.0.0~ubuntu20`
- `coreutils-from-gnu=0.0.0~ubuntu20`

Licenses: (parsed from: `/usr/share/doc/coreutils/copyright`, `/usr/share/doc/coreutils-from-gnu/copyright`)

- `GPL-3`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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
'http://archive.ubuntu.com/ubuntu/pool/main/c/coreutils-from/coreutils-from_0.0.0%7eubuntu23.dsc' coreutils-from_0.0.0~ubuntu23.dsc 1958 SHA512:82d3f67c0a976d91d71b043c386d96e891c20b9f2effeee1d487767523882a092753eed576a25731e18e1b6f01adfbf3f761dc094fcf23b4138a26ef53c83b14
'http://archive.ubuntu.com/ubuntu/pool/main/c/coreutils-from/coreutils-from_0.0.0%7eubuntu23.tar.xz' coreutils-from_0.0.0~ubuntu23.tar.xz 7316 SHA512:e8dfc2609ca771b6e6daa0ee9a30c16777e4e0f2ab779d0380e5e3df70eea9099ea061b06f355e6a3a127ab2c893ef62328b750887d60beaa587cc1fcb91f2f5
```

### `dpkg` source package: `curl=8.14.1-1ubuntu2`

Binary Packages:

- `curl=8.14.1-1ubuntu2`
- `libcurl3t64-gnutls:amd64=8.14.1-1ubuntu2`
- `libcurl4t64:amd64=8.14.1-1ubuntu2`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/db5.3/5.3.28+dfsg2-9/


### `dpkg` source package: `debconf=1.5.91`

Binary Packages:

- `debconf=1.5.91`

Licenses: (parsed from: `/usr/share/doc/debconf/copyright`)

- `BSD-2-clause`

Source:

```console
$ apt-get source -qq --print-uris debconf=1.5.91
'http://archive.ubuntu.com/ubuntu/pool/main/d/debconf/debconf_1.5.91.dsc' debconf_1.5.91.dsc 2035 SHA512:523a2aedd2925d7417f166daf896176225733d4f308959b7dbec80f4d8e9a177fb6b6d282297a7f8da13b50afadeda6210c095dd6cd75dfd41f6ffdef90a1c9f
'http://archive.ubuntu.com/ubuntu/pool/main/d/debconf/debconf_1.5.91.tar.xz' debconf_1.5.91.tar.xz 609964 SHA512:3c79aec120e660d0e74ae6a35747818a555172685d1258fff3c6622abe795858779159440f39bcf641955c335a07de8386cf0d0518cdae8193fe4f28d8492df8
```

### `dpkg` source package: `debianutils=5.23.2`

Binary Packages:

- `debianutils=5.23.2`

Licenses: (parsed from: `/usr/share/doc/debianutils/copyright`)

- `GPL-2`
- `GPL-2+`
- `SMAIL-GPL`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris debianutils=5.23.2
'http://archive.ubuntu.com/ubuntu/pool/main/d/debianutils/debianutils_5.23.2.dsc' debianutils_5.23.2.dsc 1908 SHA512:d58e2cf09f0b2a4b90c5fa5f5da814ae46784a009e7395b47c1e88d48deacd8cd04598303ed18f8b628bfc59867cfb9ad3a4b1015dc21d420e24cb45f1d54d12
'http://archive.ubuntu.com/ubuntu/pool/main/d/debianutils/debianutils_5.23.2.tar.xz' debianutils_5.23.2.tar.xz 82376 SHA512:2ccc3993abee6be0b9e861d7937984a096a29a677584665f638e5a51057051d48fcc54283c1f43ab1179505298735600e5ebedd3b41386aa5bc697c8c91cef6e
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
'http://archive.ubuntu.com/ubuntu/pool/main/d/diffutils/diffutils_3.10-4.dsc' diffutils_3.10-4.dsc 1875 SHA512:7bf4b24fa79e6c436125eb5c5926e7f4460c1108142a0d2d5662d9e6ee40e9425e22e282c784850790ae02032d6c1dc724c3b38a592e7f74949f732d4ce854bd
'http://archive.ubuntu.com/ubuntu/pool/main/d/diffutils/diffutils_3.10.orig.tar.xz' diffutils_3.10.orig.tar.xz 1624240 SHA512:219d2c815a120690c6589846271e43aee5c96c61a7ee4abbef97dfcdb3d6416652ed494b417de0ab6688c4322540d48be63b5e617beb6d20530b5d55d723ccbb
'http://archive.ubuntu.com/ubuntu/pool/main/d/diffutils/diffutils_3.10.orig.tar.xz.asc' diffutils_3.10.orig.tar.xz.asc 833 SHA512:91aa1fcfca224454e292540ea7813f4a0eb348f06a4374017326d524949775359fc833de597cc201c97f357eb6c675800828a6e3332572376f3554f1f2e1aca1
'http://archive.ubuntu.com/ubuntu/pool/main/d/diffutils/diffutils_3.10-4.debian.tar.xz' diffutils_3.10-4.debian.tar.xz 14304 SHA512:447d360101e549e520210cd6da9573cce293c1b59266d960b066da4eeff8ce473c19d2269e30cd82e33e162cd6c6b870755b3bb292d8592a51511ca19e974350
```

### `dpkg` source package: `dpkg=1.22.21ubuntu3`

Binary Packages:

- `dpkg=1.22.21ubuntu3`

Licenses: (parsed from: `/usr/share/doc/dpkg/copyright`)

- `GPL-2`
- `GPL-2+`
- `public-domain-s-s-d`

Source:

```console
$ apt-get source -qq --print-uris dpkg=1.22.21ubuntu3
'http://archive.ubuntu.com/ubuntu/pool/main/d/dpkg/dpkg_1.22.21ubuntu3.dsc' dpkg_1.22.21ubuntu3.dsc 3457 SHA512:b6ee366e65fe84d71d7fa8b0160b6b762e16a2bc2725795de3c255d48cbf8d0d3711aefc3a2b9a40fc924e99d34be5e30bc6d542686a0243a0e20487345b90fa
'http://archive.ubuntu.com/ubuntu/pool/main/d/dpkg/dpkg_1.22.21ubuntu3.tar.xz' dpkg_1.22.21ubuntu3.tar.xz 5675688 SHA512:f9219c5c8643c729cc9849fe4d4b4354fd684263d3c7f0eded7001b805153d3e60b1f22d3612a4e70b9f4b9a70213c56890e9578c6bbf337dc559ec17a62cd05
```

### `dpkg` source package: `e2fsprogs=1.47.2-3ubuntu1`

Binary Packages:

- `e2fsprogs=1.47.2-3ubuntu1`
- `libcom-err2:amd64=1.47.2-3ubuntu1`
- `libext2fs2t64:amd64=1.47.2-3ubuntu1`
- `libss2:amd64=1.47.2-3ubuntu1`
- `logsave=1.47.2-3ubuntu1`

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


### `dpkg` source package: `expat=2.7.1-2`

Binary Packages:

- `libexpat1:amd64=2.7.1-2`

Licenses: (parsed from: `/usr/share/doc/libexpat1/copyright`)

- `MIT`

Source:

```console
$ apt-get source -qq --print-uris expat=2.7.1-2
'http://archive.ubuntu.com/ubuntu/pool/main/e/expat/expat_2.7.1-2.dsc' expat_2.7.1-2.dsc 1964 SHA512:25467463ecc6f669ca84869666674039f7298bf7039603e6424ec360e1305c3ef1557f29dbe0b551eaf639dc242696d831f7d1a49516e00ed26a6c2af772e45c
'http://archive.ubuntu.com/ubuntu/pool/main/e/expat/expat_2.7.1.orig.tar.gz' expat_2.7.1.orig.tar.gz 8433717 SHA512:ea5452c511e18e0eb927eab46a47c7ced1b1be3b46232a38caef39aa86fd552a72f066db66ca824ade3ff2376b70ca72ca91bdf1d003770c91a38a47e8781b8f
'http://archive.ubuntu.com/ubuntu/pool/main/e/expat/expat_2.7.1-2.debian.tar.xz' expat_2.7.1-2.debian.tar.xz 13264 SHA512:bb0f77497469f0500a838908c5bf169e314bbdbe0990e419baed6130e382b56c830bdf3b662679f759373e6f106496858ddee6ba06092cf225ee55d2791e7492
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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/findutils/4.10.0-3/


### `dpkg` source package: `gcc-15=15.2.0-1ubuntu1`

Binary Packages:

- `gcc-15-base:amd64=15.2.0-1ubuntu1`
- `libgcc-s1:amd64=15.2.0-1ubuntu1`
- `libstdc++6:amd64=15.2.0-1ubuntu1`

Licenses: (parsed from: `/usr/share/doc/gcc-15-base/copyright`, `/usr/share/doc/libgcc-s1/copyright`, `/usr/share/doc/libstdc++6/copyright`)

- `Apache-2.0`
- `Artistic`
- `GFDL-1.2`
- `GPL`
- `GPL-3`
- `LGPL`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `gdbm=1.26-1`

Binary Packages:

- `libgdbm-compat4t64:amd64=1.26-1`
- `libgdbm6t64:amd64=1.26-1`

Licenses: (parsed from: `/usr/share/doc/libgdbm-compat4t64/copyright`, `/usr/share/doc/libgdbm6t64/copyright`)

- `GFDL-NIV-1.3+`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris gdbm=1.26-1
'http://archive.ubuntu.com/ubuntu/pool/main/g/gdbm/gdbm_1.26-1.dsc' gdbm_1.26-1.dsc 2234 SHA512:b323eaf698fd6ef3749ff671725565ae8f49f9fdcadeac003700c3a5dcaee9c6efdd4e2af75ba42c51d429c2e1c356afb62e59484889ae8ccb4b5df5d694ee83
'http://archive.ubuntu.com/ubuntu/pool/main/g/gdbm/gdbm_1.26.orig.tar.gz' gdbm_1.26.orig.tar.gz 1226591 SHA512:44aafe254f0950a8f5215d8f1337674f07b19f2a375f6eb19a7e39690028c80c3774b705c2b76b470ae74042b21f2ca77d02f6f57aa2ee50296db801220a3352
'http://archive.ubuntu.com/ubuntu/pool/main/g/gdbm/gdbm_1.26-1.debian.tar.xz' gdbm_1.26-1.debian.tar.xz 16832 SHA512:192efb75c21e1035ad5427375422385fc4534163bda7d11653d65a42429d8e39043ed3b76300e6b2d20abe8eb86fc4ac866a00626b198afe50dc47d3f48d5285
```

### `dpkg` source package: `git=1:2.51.0-1ubuntu1`

Binary Packages:

- `git=1:2.51.0-1ubuntu1`
- `git-man=1:2.51.0-1ubuntu1`

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
- `dlmalloc`
- `mingw-runtime`

Source:

```console
$ apt-get source -qq --print-uris git=1:2.51.0-1ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/g/git/git_2.51.0-1ubuntu1.dsc' git_2.51.0-1ubuntu1.dsc 2656 SHA512:995c8ac6af4331625936708fb1f4309bf7349dfc8b5037566c6a54238131a95c52dc7518ac6c4628a1ad8dbeb078b4bb9e8c5c3585afbb6a37dc6eea9f89acfe
'http://archive.ubuntu.com/ubuntu/pool/main/g/git/git_2.51.0.orig.tar.xz' git_2.51.0.orig.tar.xz 7857228 SHA512:2b8c59589266c0c9e58a9f4fda4a970a8a492e2e0ecbafc414fcfacac4a04251f0115b3676f4599a415b53906f1dea312b18a42e9bde455286abd62ec327beaf
'http://archive.ubuntu.com/ubuntu/pool/main/g/git/git_2.51.0-1ubuntu1.debian.tar.xz' git_2.51.0-1ubuntu1.debian.tar.xz 821848 SHA512:e5f8451664c213ba067010d0fca4121da7a813be833fdc0606fc99306c4aade63784db63162f5bd167312d247778a4393a24a82cd850fd93b18ecade75382511
```

### `dpkg` source package: `glibc=2.42-0ubuntu1`

Binary Packages:

- `libc-bin=2.42-0ubuntu1`
- `libc6:amd64=2.42-0ubuntu1`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `gnupg2=2.4.8-2ubuntu1`

Binary Packages:

- `dirmngr=2.4.8-2ubuntu1`
- `gnupg=2.4.8-2ubuntu1`
- `gpg=2.4.8-2ubuntu1`
- `gpg-agent=2.4.8-2ubuntu1`
- `gpgconf=2.4.8-2ubuntu1`
- `gpgsm=2.4.8-2ubuntu1`
- `gpgv=2.4.8-2ubuntu1`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `gnutls28=3.8.9-3ubuntu1`

Binary Packages:

- `libgnutls30t64:amd64=3.8.9-3ubuntu1`

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

### `dpkg` source package: `gzip=1.13-1ubuntu3`

Binary Packages:

- `gzip=1.13-1ubuntu3`

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

### `dpkg` source package: `keyutils=1.6.3-6ubuntu1`

Binary Packages:

- `libkeyutils1:amd64=1.6.3-6ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libkeyutils1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2`
- `LGPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `krb5=1.21.3-5ubuntu1`

Binary Packages:

- `libgssapi-krb5-2:amd64=1.21.3-5ubuntu1`
- `libk5crypto3:amd64=1.21.3-5ubuntu1`
- `libkrb5-3:amd64=1.21.3-5ubuntu1`
- `libkrb5support0:amd64=1.21.3-5ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libgssapi-krb5-2/copyright`, `/usr/share/doc/libk5crypto3/copyright`, `/usr/share/doc/libkrb5-3/copyright`, `/usr/share/doc/libkrb5support0/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris krb5=1.21.3-5ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.21.3-5ubuntu1.dsc' krb5_1.21.3-5ubuntu1.dsc 3950 SHA512:4eb16117d27b5ebcc2dd57fa2d60e92f0af8d17c6d1dc1239dad2eeb8601edc6cfa0470e2aaccb9cfc48a4756597aa6ac76741fe3601d2a02d1dd8f5848c8c26
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.21.3.orig.tar.gz' krb5_1.21.3.orig.tar.gz 9136145 SHA512:87bc06607f4d95ff604169cea22180703a42d667af05f66f1569b8bd592670c42820b335e5c279e8b4f066d1e7da20f1948a1e4def7c5d295c170cbfc7f49c71
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.21.3-5ubuntu1.debian.tar.xz' krb5_1.21.3-5ubuntu1.debian.tar.xz 111424 SHA512:347af1a11b7a4ec742367c4ca0247f3aa6b3fb7d3313d187b6a062e7330ec6a46ee71dac157f982b51566d6a89f1c23453a3759f594fa5056a416ef8a1608af8
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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/libbsd/0.12.2-2/


### `dpkg` source package: `libcap-ng=0.8.5-4build1`

Binary Packages:

- `libcap-ng0:amd64=0.8.5-4build1`

Licenses: (parsed from: `/usr/share/doc/libcap-ng0/copyright`)

- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `LGPL-2.1`
- `LGPL-2.1+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libcap2=1:2.75-7ubuntu1`

Binary Packages:

- `libcap2:amd64=1:2.75-7ubuntu1`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/libedit/3.1-20250104-1/


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

### `dpkg` source package: `libffi=3.5.2-1`

Binary Packages:

- `libffi8:amd64=3.5.2-1`

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

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/libffi/3.5.2-1/


### `dpkg` source package: `libfido2=1.16.0-2`

Binary Packages:

- `libfido2-1:amd64=1.16.0-2`

Licenses: (parsed from: `/usr/share/doc/libfido2-1/copyright`)

- `BSD-2-clause`
- `ISC`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris libfido2=1.16.0-2
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libfido2/libfido2_1.16.0-2.dsc' libfido2_1.16.0-2.dsc 2490 SHA512:d588b4d1bc4c9a2495626b2cfeb6d2e8d79c610686663c510538dfd0faf5172637e3a44fe2d2fae59d9034ba517b00f382454c7a4c73d5b16e8b9bcd645dc2ab
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libfido2/libfido2_1.16.0.orig.tar.xz' libfido2_1.16.0.orig.tar.xz 599884 SHA512:f85b5f8bb8c85a4371035f2875eb70f0e8dc8450279020d853cc19e200e4e68bddf93829b7c7675ac078e3b04c267e8cc6fb044302b9080913e2ba89e877cc38
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libfido2/libfido2_1.16.0-2.debian.tar.xz' libfido2_1.16.0-2.debian.tar.xz 65832 SHA512:26d499b0b4113d0ebf103b672aed3420f841f67f8c9fff714482a1f3655fe357c08f8668f03b27587d10d10d321970894fdda2ba21517eedd47cd916248007b3
```

### `dpkg` source package: `libgcrypt20=1.11.0-7`

Binary Packages:

- `libgcrypt20:amd64=1.11.0-7`

Licenses: (parsed from: `/usr/share/doc/libgcrypt20/copyright`)

- `GPL-2`
- `LGPL`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/libgcrypt20/1.11.0-7/


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

### `dpkg` source package: `libidn2=2.3.8-4`

Binary Packages:

- `libidn2-0:amd64=2.3.8-4`

Licenses: (parsed from: `/usr/share/doc/libidn2-0/copyright`)

- `Expat`
- `FSFAP`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`
- `LGPL-3+`
- `Unicode`

Source:

```console
$ apt-get source -qq --print-uris libidn2=2.3.8-4
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libidn2/libidn2_2.3.8-4.dsc' libidn2_2.3.8-4.dsc 2811 SHA512:0bf433efbaf75dadf72ba6c13d914f45cdd8b6c0c82432c1a1b7265b37488ccbdaa3799995d57a6c5afdfa1cfa233ed88a4c14f5e807d3a8d43fc7b0d374f7d8
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libidn2/libidn2_2.3.8.orig.tar.gz' libidn2_2.3.8.orig.tar.gz 718637 SHA512:e3f4ec5113f531d2b1827a11d7292318fdc49032c013b0076911b075b0e879428db9b45fe137aa37bf9c60e672b6883c035f9f45b2b42625031534965d518bc1
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libidn2/libidn2_2.3.8.orig.tar.gz.asc' libidn2_2.3.8.orig.tar.gz.asc 1223 SHA512:f5c7f1676018b1cd362e250dd8ad59150c34b11ede9a21dbaf6f2e88fa943c881db6e59bf3e9180567379173cb21c4c893d835db99f4ed9e94bd80f84fb8ee2c
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libidn2/libidn2_2.3.8-4.debian.tar.xz' libidn2_2.3.8-4.debian.tar.xz 18116 SHA512:af9e4879f9d3ee6e0c215a2860f5b18907641cc7f33fc0b00b17521ec8fa65ea9d18bfd945311b37d5fe5acb853a600f277af3cacc1f8d592fd607a36a0d5cd3
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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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

### `dpkg` source package: `libseccomp=2.6.0-2ubuntu1`

Binary Packages:

- `libseccomp2:amd64=2.6.0-2ubuntu1`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/libselinux/3.8.1-1/


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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/libssh2/1.11.1-1/


### `dpkg` source package: `libtasn1-6=4.20.0-2`

Binary Packages:

- `libtasn1-6:amd64=4.20.0-2`

Licenses: (parsed from: `/usr/share/doc/libtasn1-6/copyright`)

- `GFDL-1.3`
- `GPL-3`
- `LGPL`
- `LGPL-2.1`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/libtasn1-6/4.20.0-2/


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


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/libxcrypt/1:4.4.38-1/


### `dpkg` source package: `libzstd=1.5.7+dfsg-1build1`

Binary Packages:

- `libzstd1:amd64=1.5.7+dfsg-1build1`

Licenses: (parsed from: `/usr/share/doc/libzstd1/copyright`)

- `BSD-3-clause`
- `Expat`
- `GPL-2`
- `zlib`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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
'http://archive.ubuntu.com/ubuntu/pool/main/l/lz4/lz4_1.10.0-4build1.dsc' lz4_1.10.0-4build1.dsc 1965 SHA512:ede20a0c3a1c8824d1b008cce662dc6593ffcf3eeb72e89e535f84eb8b91396e2b2def6ce86ebd42710955892b10f9b6764eec3ac8b230efb0c0ca7d594e3b53
'http://archive.ubuntu.com/ubuntu/pool/main/l/lz4/lz4_1.10.0.orig.tar.gz' lz4_1.10.0.orig.tar.gz 387114 SHA512:8c4ceb217e6dc8e7e0beba99adc736aca8963867bcf9f970d621978ba11ce92855912f8b66138037a1d2ae171e8e17beb7be99281fea840106aa60373c455b28
'http://archive.ubuntu.com/ubuntu/pool/main/l/lz4/lz4_1.10.0-4build1.debian.tar.xz' lz4_1.10.0-4build1.debian.tar.xz 8152 SHA512:19dfb1fca73af402bcd18dab9436017767e4a66c7d759623f6cc60a0f08b287ad984c79b887df729a8307cf9b6dd28d41c6c5cd1addf85d2e4e9c59ca1cb1b4d
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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/ncurses/6.5+20250216-2/


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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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

### `dpkg` source package: `openldap=2.6.10+dfsg-1ubuntu1`

Binary Packages:

- `libldap-common=2.6.10+dfsg-1ubuntu1`
- `libldap2:amd64=2.6.10+dfsg-1ubuntu1`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `openssh=1:10.0p1-5ubuntu3`

Binary Packages:

- `openssh-client=1:10.0p1-5ubuntu3`

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


### `dpkg` source package: `openssl=3.5.0-2ubuntu1`

Binary Packages:

- `libssl3t64:amd64=3.5.0-2ubuntu1`
- `openssl=3.5.0-2ubuntu1`
- `openssl-provider-legacy=3.5.0-2ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libssl3t64/copyright`, `/usr/share/doc/openssl/copyright`, `/usr/share/doc/openssl-provider-legacy/copyright`)

- `Apache-2.0`
- `Artistic`
- `GPL-1`
- `GPL-1+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `p11-kit=0.25.5-3ubuntu1`

Binary Packages:

- `libp11-kit0:amd64=0.25.5-3ubuntu1`

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
$ apt-get source -qq --print-uris p11-kit=0.25.5-3ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/p/p11-kit/p11-kit_0.25.5-3ubuntu1.dsc' p11-kit_0.25.5-3ubuntu1.dsc 2398 SHA512:cf8d8bd028e6b264486c6a5b7c0e1a54295306c7e306acfd7920740c9e4e59c959e3f825f4a2ac32e473dbf7aac5e9375d409e55a7411fe8a2aba67c2652041f
'http://archive.ubuntu.com/ubuntu/pool/main/p/p11-kit/p11-kit_0.25.5.orig.tar.xz' p11-kit_0.25.5.orig.tar.xz 1002056 SHA512:177ec6ff5eb891901078306dce2bf3f5c1a0e5c2a8c493bdf5a08ae1ff1240fdf6952961e973c373f80ac3d1d5a9927e07f4da49e4ff92269d992e744889fc94
'http://archive.ubuntu.com/ubuntu/pool/main/p/p11-kit/p11-kit_0.25.5-3ubuntu1.debian.tar.xz' p11-kit_0.25.5-3ubuntu1.debian.tar.xz 33660 SHA512:eadb175d1f83a5ca208be2af7e1bfa4ebc688f1acd2635fd5e253267237decb365e2ca0e44f759938a07db480cce79e602a2ee9275b701ebabc9e1982a297b4e
```

### `dpkg` source package: `pam=1.7.0-5ubuntu1`

Binary Packages:

- `libpam-modules:amd64=1.7.0-5ubuntu1`
- `libpam-modules-bin=1.7.0-5ubuntu1`
- `libpam-runtime=1.7.0-5ubuntu1`
- `libpam0g:amd64=1.7.0-5ubuntu1`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `pcre2=10.46-1`

Binary Packages:

- `libpcre2-8-0:amd64=10.46-1`

Licenses: (parsed from: `/usr/share/doc/libpcre2-8-0/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `BSD-3-clause-Cambridge with BINARY LIBRARY-LIKE PACKAGES exception`
- `X11`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris pcre2=10.46-1
'http://archive.ubuntu.com/ubuntu/pool/main/p/pcre2/pcre2_10.46-1.dsc' pcre2_10.46-1.dsc 2337 SHA512:9b0e023c151a5f76178b0663b7b36c4650f352c3a3f86db04d845726414f35dff9e7452ae5812013a32e0aec66d729a16ae1cf7f47e60d06a6e46ca371bf5fc6
'http://archive.ubuntu.com/ubuntu/pool/main/p/pcre2/pcre2_10.46.orig.tar.gz' pcre2_10.46.orig.tar.gz 2718545 SHA512:8bc85f1e47633f4cab07e00b65e9f94a38bb8db56d7ea0a3068774a5ccfe5b777e6645c0a345dd265a06aa6672448ad51c9e56636c48ec87dae9f884a998e00b
'http://archive.ubuntu.com/ubuntu/pool/main/p/pcre2/pcre2_10.46-1.diff.gz' pcre2_10.46-1.diff.gz 8748 SHA512:b985f1cc087449f80ba19812bf903b798d3772bbddf599dbf377e5a41aedbec8c711bc7f1c2cfd51fbddc29f478961ab834dd64a34809c5bbeb6cd2cb8694165
```

### `dpkg` source package: `perl=5.40.1-6`

Binary Packages:

- `libperl5.40:amd64=5.40.1-6`
- `perl=5.40.1-6`
- `perl-base=5.40.1-6`
- `perl-modules-5.40=5.40.1-6`

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

- http://snapshot.debian.org/package/perl/5.40.1-6/


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

### `dpkg` source package: `procps=2:4.0.4-8ubuntu2`

Binary Packages:

- `libproc2-0:amd64=2:4.0.4-8ubuntu2`
- `procps=2:4.0.4-8ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libproc2-0/copyright`, `/usr/share/doc/procps/copyright`)

- `GPL-2`
- `GPL-2.0+`
- `LGPL-2`
- `LGPL-2.0+`
- `LGPL-2.1`
- `LGPL-2.1+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-defaults=3.13.7-1`

Binary Packages:

- `libpython3-stdlib:amd64=3.13.7-1`
- `python3=3.13.7-1`
- `python3-minimal=3.13.7-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris python3-defaults=3.13.7-1
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3-defaults/python3-defaults_3.13.7-1.dsc' python3-defaults_3.13.7-1.dsc 2346 SHA512:d224c5ced2a34850c186f17b5d4ede11214507ba5135841ca3ecde9c2b891dbeba06a1e844a205fc039d214cec3a430138786d1a80f931993d17b30e279a5bbe
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3-defaults/python3-defaults_3.13.7-1.tar.gz' python3-defaults_3.13.7-1.tar.gz 146793 SHA512:58aee233ad3f34b28b0031ec77872f8a027160659cb7eb31e8839cf98f9c6d977f1d211f681d687a58444f043a0dd30885933973fbeb8226e8aeed3ef5e7c39a
```

### `dpkg` source package: `python3.13=3.13.7-1`

Binary Packages:

- `libpython3.13-minimal:amd64=3.13.7-1`
- `libpython3.13-stdlib:amd64=3.13.7-1`
- `python3.13=3.13.7-1`
- `python3.13-minimal=3.13.7-1`

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
$ apt-get source -qq --print-uris python3.13=3.13.7-1
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3.13/python3.13_3.13.7-1.dsc' python3.13_3.13.7-1.dsc 3689 SHA512:2264e406b17c9346972627931d43543b5a8eabd7f7bedd8aa64288838cbf2fa4674688ee5bb410a56492f6974e5dde170e32a726689bdfd9e8d020429b5c5e28
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3.13/python3.13_3.13.7.orig.tar.xz' python3.13_3.13.7.orig.tar.xz 22769492 SHA512:73fa04db860e8b98c204f84d403598fcb802b19bfc8f2675df2fddb6b153b1643daf081746a043f57c8fa71b950a439581aa5204c2bfadb8cfd8864ca4f42f0d
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3.13/python3.13_3.13.7.orig.tar.xz.asc' python3.13_3.13.7.orig.tar.xz.asc 963 SHA512:71cd002c18ebb47861abd3309c8cf38972d3d916cca5595d895ba3940719243c66fa28595c2370a8846d9d1c4b3cb4ac5baeda9e9cf94be30302892d01df5e87
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3.13/python3.13_3.13.7-1.debian.tar.xz' python3.13_3.13.7-1.debian.tar.xz 260456 SHA512:08f8d15954f4040befb2def9bd7c167cadf76a929c9a3842b5034aa5eabce9592f82b464b8b46903e7a68308eab6453ad8b8fb7477800692b3bfafa96a0624bb
```

### `dpkg` source package: `readline=8.3-1ubuntu1`

Binary Packages:

- `libreadline8t64:amd64=8.3-1ubuntu1`
- `readline-common=8.3-1ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libreadline8t64/copyright`, `/usr/share/doc/readline-common/copyright`)

- `GFDL`
- `GFDL-NIV-1.3+`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `ISC-no-attribution`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `rtmpdump=2.4+20151223.gitfa8646d.1-2build7`

Binary Packages:

- `librtmp1:amd64=2.4+20151223.gitfa8646d.1-2build7`

Licenses: (parsed from: `/usr/share/doc/librtmp1/copyright`)

- `GPL-2`
- `LGPL-2.1`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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


### `dpkg` source package: `shadow=1:4.17.4-2ubuntu1`

Binary Packages:

- `login.defs=1:4.17.4-2ubuntu1`
- `passwd=1:4.17.4-2ubuntu1`

Licenses: (parsed from: `/usr/share/doc/login.defs/copyright`, `/usr/share/doc/passwd/copyright`)

- `BSD-3-clause`
- `GPL-1`
- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `sqlite3=3.46.1-7`

Binary Packages:

- `libsqlite3-0:amd64=3.46.1-7`

Licenses: (parsed from: `/usr/share/doc/libsqlite3-0/copyright`)

- `GPL-2`
- `GPL-2+`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/sqlite3/3.46.1-7/


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

### `dpkg` source package: `systemd=257.8-0ubuntu2`

Binary Packages:

- `libsystemd0:amd64=257.8-0ubuntu2`
- `libudev1:amd64=257.8-0ubuntu2`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/tar/1.35+dfsg-3.1/


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

### `dpkg` source package: `util-linux=2.41-4ubuntu3`

Binary Packages:

- `bsdutils=1:2.41-4ubuntu3`
- `libblkid1:amd64=2.41-4ubuntu3`
- `liblastlog2-2:amd64=2.41-4ubuntu3`
- `libmount1:amd64=2.41-4ubuntu3`
- `libsmartcols1:amd64=2.41-4ubuntu3`
- `libuuid1:amd64=2.41-4ubuntu3`
- `login=1:4.16.0-2+really2.41-4ubuntu3`
- `mount=2.41-4ubuntu3`
- `util-linux=2.41-4ubuntu3`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `wget=1.25.0-2ubuntu1`

Binary Packages:

- `wget=1.25.0-2ubuntu1`

Licenses: (parsed from: `/usr/share/doc/wget/copyright`)

- `GFDL-1.2`
- `GPL-3`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `zlib=1:1.3.dfsg+really1.3.1-1ubuntu1`

Binary Packages:

- `zlib1g:amd64=1:1.3.dfsg+really1.3.1-1ubuntu1`

Licenses: (parsed from: `/usr/share/doc/zlib1g/copyright`)

- `Zlib`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

