# `buildpack-deps:questing`

## Docker Metadata

- Image ID: `sha256:70ba8062115e2afb7722923063ba6d4cb68510a95b7b6921b1f242f4416fdb43`
- Created: `2025-05-19T22:25:54Z`
- Virtual Size: ~ 1.77 Gb  
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

### `dpkg` source package: `aom=3.12.1-1`

Binary Packages:

- `libaom3:amd64=3.12.1-1`

Licenses: (parsed from: `/usr/share/doc/libaom3/copyright`)

- `BSD-2-Clause`
- `BSD-2-clause`
- `BSD-3-clause`
- `Expat`
- `ISC`
- `public-domain-md5`

Source:

```console
$ apt-get source -qq --print-uris aom=3.12.1-1
'http://archive.ubuntu.com/ubuntu/pool/main/a/aom/aom_3.12.1-1.dsc' aom_3.12.1-1.dsc 2552 SHA512:147a23137b5667e74edec009e524c562091c16d2d884a013b42519e8be8de36c03aa5df2b6804a62922944dc36394c2930a64c3f5a884e2fc6a3ce978e9a5f73
'http://archive.ubuntu.com/ubuntu/pool/main/a/aom/aom_3.12.1.orig.tar.gz' aom_3.12.1.orig.tar.gz 5504164 SHA512:a6c14b15518a029ebb4ea75344d84d2948f7ab03db7e2688a31dd170323ab4a5812f13dc5f14319961318842991f6ca5c843ffb85a2550aa63e89b2c0996528f
'http://archive.ubuntu.com/ubuntu/pool/main/a/aom/aom_3.12.1-1.debian.tar.xz' aom_3.12.1-1.debian.tar.xz 20464 SHA512:4ac2d1f3c0528d8458ec187058dbb888164502fac725e6785ee10368bcfd1e56ee0c886ca27572554e4aaf72601e14c89413321f3574085e5030ec1710ee01f9
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


### `dpkg` source package: `architecture-properties=0.2.6`

Binary Packages:

- `native-architecture=0.2.6`

Licenses: (parsed from: `/usr/share/doc/native-architecture/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris architecture-properties=0.2.6
'http://archive.ubuntu.com/ubuntu/pool/main/a/architecture-properties/architecture-properties_0.2.6.dsc' architecture-properties_0.2.6.dsc 1803 SHA512:9afa5d7161746d22fe3415d5d8016e63d2c6db514285893863025ec29e575aa45c0f53058c25245d7bc86fa9073876f5948e4df0fbf350df1de12c676a18f9da
'http://archive.ubuntu.com/ubuntu/pool/main/a/architecture-properties/architecture-properties_0.2.6.tar.xz' architecture-properties_0.2.6.tar.xz 5368 SHA512:e698d5cd2dd19f4ec07d5732f4023c7e663a9de4f15da56614d624a90611ceba012b8688405def94bc61b0d2197f79000409fa9c471bf1d8ad15bb1b834f3f19
```

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


### `dpkg` source package: `autoconf=2.72-3.1ubuntu1`

Binary Packages:

- `autoconf=2.72-3.1ubuntu1`

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
$ apt-get source -qq --print-uris autoconf=2.72-3.1ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/a/autoconf/autoconf_2.72-3.1ubuntu1.dsc' autoconf_2.72-3.1ubuntu1.dsc 1926 SHA512:1b65c2f5dc49006d9dc0d764247c82ef662c3a4ea6c2a8acff8929761685fc8b60f2257193ba159944c9e1adab38c495dad89c2c5c389606a000befde3ad1b7a
'http://archive.ubuntu.com/ubuntu/pool/main/a/autoconf/autoconf_2.72.orig.tar.xz' autoconf_2.72.orig.tar.xz 1389680 SHA512:c4e9fbd858666d3e5c3b4fe7f89aa3e8e3a0a00dc7e166f8147d937d911b77ba3ac6a016f9d223ccdd830bc8960b3e60397c0607cc6a1fd2c50c7492839ddd17
'http://archive.ubuntu.com/ubuntu/pool/main/a/autoconf/autoconf_2.72-3.1ubuntu1.debian.tar.xz' autoconf_2.72-3.1ubuntu1.debian.tar.xz 27368 SHA512:8857affd80e5ebed22acd25ea721acdefe1208df57be348a90d59e5a4b93ed4957e54eccf71ee3d56ed186bfba5a45424d2089e22fa3ddafdc335a9534557aaa
```

### `dpkg` source package: `automake-1.17=1:1.17-4ubuntu1`

Binary Packages:

- `automake=1:1.17-4ubuntu1`

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
$ apt-get source -qq --print-uris automake-1.17=1:1.17-4ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/a/automake-1.17/automake-1.17_1.17-4ubuntu1.dsc' automake-1.17_1.17-4ubuntu1.dsc 2385 SHA512:4084efb427a94d340b0b39b57d1d4a4e6a94c9a68e8a98a8be705cdbee86ee8181b0cd45edd1cdc544550a49478cdbb97ac0e0aec3bea46c5e780f963bc51879
'http://archive.ubuntu.com/ubuntu/pool/main/a/automake-1.17/automake-1.17_1.17.orig.tar.xz' automake-1.17_1.17.orig.tar.xz 1652632 SHA512:46aba1c9d64a6368b326020803a2999831c1deaf31eaa1c1dfdcfa5138a7f755643294e82a08b6daab3983b31eee725bdb7b9edc4e9a558374c7d1f1b8e854a7
'http://archive.ubuntu.com/ubuntu/pool/main/a/automake-1.17/automake-1.17_1.17.orig.tar.xz.asc' automake-1.17_1.17.orig.tar.xz.asc 833 SHA512:180dde452ec097a9267c334044a9ec16bb65cc6ccbc000b7eca0af81ed7ece6f4ce6f6c2be8a2cabca9d48fd46085c81f0ee5d020967104bc25f37f52927829a
'http://archive.ubuntu.com/ubuntu/pool/main/a/automake-1.17/automake-1.17_1.17-4ubuntu1.debian.tar.xz' automake-1.17_1.17-4ubuntu1.debian.tar.xz 15824 SHA512:08f1a1a8c33513108d5d01c2115d73b81c37e57c44caea287925b9a57238a0e982bca416bf9913d52d94ca630f1674b6c9ca5121e8675c7c3f0b39b3bcd229d5
```

### `dpkg` source package: `autotools-dev=20240727.1`

Binary Packages:

- `autotools-dev=20240727.1`

Licenses: (parsed from: `/usr/share/doc/autotools-dev/copyright`)

- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris autotools-dev=20240727.1
'http://archive.ubuntu.com/ubuntu/pool/main/a/autotools-dev/autotools-dev_20240727.1.dsc' autotools-dev_20240727.1.dsc 1661 SHA512:0fc92985b4585e2281145cc7ed1425eda146f462666b3ec2aff6559053e991188f2cbc28c556df4d3a1d6e45269d35aae321d5ef201ef6e534bad98a18e8b5fd
'http://archive.ubuntu.com/ubuntu/pool/main/a/autotools-dev/autotools-dev_20240727.1.tar.xz' autotools-dev_20240727.1.tar.xz 99716 SHA512:464f1acda3a0a62a30510d7aa218137128e41f5152436016c44220154859e8a49bbd42513b2136b3c94502003792f49f5d6aa2ac7f4d9b6bf4c1556e84a2758e
```

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


### `dpkg` source package: `binutils=2.45-3ubuntu3`

Binary Packages:

- `binutils=2.45-3ubuntu3`
- `binutils-common:amd64=2.45-3ubuntu3`
- `binutils-x86-64-linux-gnu=2.45-3ubuntu3`
- `libbinutils:amd64=2.45-3ubuntu3`
- `libctf-nobfd0:amd64=2.45-3ubuntu3`
- `libctf0:amd64=2.45-3ubuntu3`
- `libgprofng0:amd64=2.45-3ubuntu3`
- `libsframe2:amd64=2.45-3ubuntu3`

Licenses: (parsed from: `/usr/share/doc/binutils/copyright`, `/usr/share/doc/binutils-common/copyright`, `/usr/share/doc/binutils-x86-64-linux-gnu/copyright`, `/usr/share/doc/libbinutils/copyright`, `/usr/share/doc/libctf-nobfd0/copyright`, `/usr/share/doc/libctf0/copyright`, `/usr/share/doc/libgprofng0/copyright`, `/usr/share/doc/libsframe2/copyright`)

- `GFDL`
- `GPL`
- `LGPL`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `brotli=1.1.0-2build4`

Binary Packages:

- `libbrotli-dev:amd64=1.1.0-2build4`
- `libbrotli1:amd64=1.1.0-2build4`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/bzip2/1.0.8-6/


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

### `dpkg` source package: `cairo=1.18.4-1`

Binary Packages:

- `libcairo-gobject2:amd64=1.18.4-1`
- `libcairo-script-interpreter2:amd64=1.18.4-1`
- `libcairo2:amd64=1.18.4-1`
- `libcairo2-dev:amd64=1.18.4-1`

Licenses: (parsed from: `/usr/share/doc/libcairo-gobject2/copyright`, `/usr/share/doc/libcairo-script-interpreter2/copyright`, `/usr/share/doc/libcairo2/copyright`, `/usr/share/doc/libcairo2-dev/copyright`)

- `LGPL-2.1`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/cairo/1.18.4-1/


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
'http://archive.ubuntu.com/ubuntu/pool/main/c/coreutils-from/coreutils-from_0.0.0%7eubuntu24.dsc' coreutils-from_0.0.0~ubuntu24.dsc 1966 SHA512:2e03843c71f35a5e24b63b81f4cf203558d1c59fe7fad42ab13173737281829e9e4cd1b4840349dc2d28726008223655700123c8b0beb490ecdb5028336a6c36
'http://archive.ubuntu.com/ubuntu/pool/main/c/coreutils-from/coreutils-from_0.0.0%7eubuntu24.tar.xz' coreutils-from_0.0.0~ubuntu24.tar.xz 7384 SHA512:2841b9435326c202e040b260ebf067ea13d922ec498adc837a8f33ba50a7b0f0afe8682acebeb534e083f932adb71ac66895db8a3afd2bc72d945d2b81c0a5ac
```

### `dpkg` source package: `curl=8.14.1-1ubuntu2`

Binary Packages:

- `curl=8.14.1-1ubuntu2`
- `libcurl3t64-gnutls:amd64=8.14.1-1ubuntu2`
- `libcurl4-openssl-dev:amd64=8.14.1-1ubuntu2`
- `libcurl4t64:amd64=8.14.1-1ubuntu2`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/cyrus-sasl2/2.1.28+dfsg1-9/


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


### `dpkg` source package: `db-defaults=1:5.3.21ubuntu3`

Binary Packages:

- `libdb-dev:amd64=1:5.3.21ubuntu3`

Licenses: (parsed from: `/usr/share/doc/libdb-dev/copyright`)

- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris db-defaults=1:5.3.21ubuntu3
'http://archive.ubuntu.com/ubuntu/pool/main/d/db-defaults/db-defaults_5.3.21ubuntu3.dsc' db-defaults_5.3.21ubuntu3.dsc 1619 SHA512:679b84431228f1a5cfd06cd0ff57a55add21e3e050ee4fae5544f0db1b575558db1845b077612a39781d9e2cc0cac3ae36947c1a72db4dea41ae89f0cc4fc65a
'http://archive.ubuntu.com/ubuntu/pool/main/d/db-defaults/db-defaults_5.3.21ubuntu3.tar.xz' db-defaults_5.3.21ubuntu3.tar.xz 2832 SHA512:d47a21da2f8129e2c067cdb2398e087f2bfd3a6a206e3f3167456c84fc2d168cd100605e6582b7c865b8b8e1e0a59a7795e4267d39428b9ef92bd23b5a5293e0
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

### `dpkg` source package: `djvulibre=3.5.28-2.2`

Binary Packages:

- `libdjvulibre-dev:amd64=3.5.28-2.2`
- `libdjvulibre-text=3.5.28-2.2`
- `libdjvulibre21:amd64=3.5.28-2.2`

Licenses: (parsed from: `/usr/share/doc/libdjvulibre-dev/copyright`, `/usr/share/doc/libdjvulibre-text/copyright`, `/usr/share/doc/libdjvulibre21/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris djvulibre=3.5.28-2.2
'http://archive.ubuntu.com/ubuntu/pool/main/d/djvulibre/djvulibre_3.5.28-2.2.dsc' djvulibre_3.5.28-2.2.dsc 2375 SHA512:237c4eed5abd1f445a835d6a6bdecf44e23ee542bd0ec1a491840692156922e87bd0a9f30450bb8f241493fcf4df80ffe48184c03a1bdad5ba189928da3cca7d
'http://archive.ubuntu.com/ubuntu/pool/main/d/djvulibre/djvulibre_3.5.28.orig.tar.xz' djvulibre_3.5.28.orig.tar.xz 2959024 SHA512:4fdbecd2b7b583ee4211c9cda6638a3a831c883e2552b3c8ad09f69e8734831addc14f590faab8c58d7f9f017b527abccc384f6066e674e341cf43c96db49cb7
'http://archive.ubuntu.com/ubuntu/pool/main/d/djvulibre/djvulibre_3.5.28-2.2.debian.tar.xz' djvulibre_3.5.28-2.2.debian.tar.xz 18328 SHA512:a82bfac5c132ea1aa3ebd1e9d5e747a2e5b7f2f14b5cfc1a764ba0fe1da208e6903e21f1d465e62e10b0f668f145207adeec04a7c583003d866208898a63231c
```

### `dpkg` source package: `dpkg=1.22.21ubuntu3`

Binary Packages:

- `dpkg=1.22.21ubuntu3`
- `dpkg-dev=1.22.21ubuntu3`
- `libdpkg-perl=1.22.21ubuntu3`

Licenses: (parsed from: `/usr/share/doc/dpkg/copyright`, `/usr/share/doc/dpkg-dev/copyright`, `/usr/share/doc/libdpkg-perl/copyright`)

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

- `comerr-dev:amd64=2.1-1.47.2-3ubuntu1`
- `e2fsprogs=1.47.2-3ubuntu1`
- `libcom-err2:amd64=1.47.2-3ubuntu1`
- `libext2fs2t64:amd64=1.47.2-3ubuntu1`
- `libss2:amd64=1.47.2-3ubuntu1`
- `logsave=1.47.2-3ubuntu1`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `elfutils=0.193-1`

Binary Packages:

- `libelf1t64:amd64=0.193-1`

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
$ apt-get source -qq --print-uris elfutils=0.193-1
'http://archive.ubuntu.com/ubuntu/pool/main/e/elfutils/elfutils_0.193-1.dsc' elfutils_0.193-1.dsc 3315 SHA512:ee508b85f724967961e29d94cc7347ecb0e811d434a4878ad9e37931aacfa9d9ede2499b7c27e96b9b9a8f3bc6bd2f9736a347dcffc967e35f34925695fc0b99
'http://archive.ubuntu.com/ubuntu/pool/main/e/elfutils/elfutils_0.193.orig.tar.bz2' elfutils_0.193.orig.tar.bz2 11974916 SHA512:557e328e3de0d2a69d09c15a9333f705f3233584e2c6a7d3ce855d06a12dc129e69168d6be64082803630397bd64e1660a8b5324d4f162d17922e10ddb367d76
'http://archive.ubuntu.com/ubuntu/pool/main/e/elfutils/elfutils_0.193-1.debian.tar.xz' elfutils_0.193-1.debian.tar.xz 44644 SHA512:527dbc77d9b3a44f062841835a8bdf5a0f95c26ef293defe3d1dd4e9aea04f2d3fae246c3b985953ff3e7fa247de07fc41b6623a303dc416de2f7f35c438d1fc
```

### `dpkg` source package: `expat=2.7.1-2`

Binary Packages:

- `libexpat1:amd64=2.7.1-2`
- `libexpat1-dev:amd64=2.7.1-2`

Licenses: (parsed from: `/usr/share/doc/libexpat1/copyright`, `/usr/share/doc/libexpat1-dev/copyright`)

- `MIT`

Source:

```console
$ apt-get source -qq --print-uris expat=2.7.1-2
'http://archive.ubuntu.com/ubuntu/pool/main/e/expat/expat_2.7.1-2.dsc' expat_2.7.1-2.dsc 1964 SHA512:25467463ecc6f669ca84869666674039f7298bf7039603e6424ec360e1305c3ef1557f29dbe0b551eaf639dc242696d831f7d1a49516e00ed26a6c2af772e45c
'http://archive.ubuntu.com/ubuntu/pool/main/e/expat/expat_2.7.1.orig.tar.gz' expat_2.7.1.orig.tar.gz 8433717 SHA512:ea5452c511e18e0eb927eab46a47c7ced1b1be3b46232a38caef39aa86fd552a72f066db66ca824ade3ff2376b70ca72ca91bdf1d003770c91a38a47e8781b8f
'http://archive.ubuntu.com/ubuntu/pool/main/e/expat/expat_2.7.1-2.debian.tar.xz' expat_2.7.1-2.debian.tar.xz 13264 SHA512:bb0f77497469f0500a838908c5bf169e314bbdbe0990e419baed6130e382b56c830bdf3b662679f759373e6f106496858ddee6ba06092cf225ee55d2791e7492
```

### `dpkg` source package: `fftw3=3.3.10-2fakesync1build2`

Binary Packages:

- `libfftw3-bin=3.3.10-2fakesync1build2`
- `libfftw3-dev:amd64=3.3.10-2fakesync1build2`
- `libfftw3-double3:amd64=3.3.10-2fakesync1build2`
- `libfftw3-long3:amd64=3.3.10-2fakesync1build2`
- `libfftw3-quad3:amd64=3.3.10-2fakesync1build2`
- `libfftw3-single3:amd64=3.3.10-2fakesync1build2`

Licenses: (parsed from: `/usr/share/doc/libfftw3-bin/copyright`, `/usr/share/doc/libfftw3-dev/copyright`, `/usr/share/doc/libfftw3-double3/copyright`, `/usr/share/doc/libfftw3-long3/copyright`, `/usr/share/doc/libfftw3-quad3/copyright`, `/usr/share/doc/libfftw3-single3/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris fftw3=3.3.10-2fakesync1build2
'http://archive.ubuntu.com/ubuntu/pool/main/f/fftw3/fftw3_3.3.10-2fakesync1build2.dsc' fftw3_3.3.10-2fakesync1build2.dsc 2893 SHA512:f87f249e4cdfe01455e70947cf2c3db3a87733f79a35a9fe9bea8efd7150b7d55f925b86a913ed29c1169816f39a73d3ff956e4a44f9704fe3c06fb1c6caa522
'http://archive.ubuntu.com/ubuntu/pool/main/f/fftw3/fftw3_3.3.10.orig.tar.gz' fftw3_3.3.10.orig.tar.gz 4262403 SHA512:fa2ea740449fd06c833a82e1fff82bacd554188d500cbedff5a0bc185551799ef9ef9b8b1c227283abdbbdd185424d19df9c0f06ed88d5fe3d9c001d6fab6109
'http://archive.ubuntu.com/ubuntu/pool/main/f/fftw3/fftw3_3.3.10-2fakesync1build2.debian.tar.xz' fftw3_3.3.10-2fakesync1build2.debian.tar.xz 14828 SHA512:de62d3653d40d54e788285912ff6e2e31d5ddddab9d728f6b3f582253caf2e0cfa3e8e79883324f79a954d59a87f2e3369a0ed7fd8cce71c185ac1c356644932
```

### `dpkg` source package: `file=1:5.46-5`

Binary Packages:

- `file=1:5.46-5`
- `libmagic-mgc=1:5.46-5`
- `libmagic1t64:amd64=1:5.46-5`

Licenses: (parsed from: `/usr/share/doc/file/copyright`, `/usr/share/doc/libmagic-mgc/copyright`, `/usr/share/doc/libmagic1t64/copyright`)

- `BSD-2-Clause-alike`
- `BSD-2-Clause-netbsd`
- `BSD-2-Clause-regents`
- `MIT-Old-Style-with-legal-disclaimer-2`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/file/1:5.46-5/


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


### `dpkg` source package: `fontconfig=2.15.0-2.3ubuntu1`

Binary Packages:

- `fontconfig=2.15.0-2.3ubuntu1`
- `fontconfig-config=2.15.0-2.3ubuntu1`
- `libfontconfig-dev:amd64=2.15.0-2.3ubuntu1`
- `libfontconfig1:amd64=2.15.0-2.3ubuntu1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris fontconfig=2.15.0-2.3ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/f/fontconfig/fontconfig_2.15.0-2.3ubuntu1.dsc' fontconfig_2.15.0-2.3ubuntu1.dsc 2780 SHA512:55ad92aada8da2ff73fd104e6bda124c4721b460209bd11a554672662b539570c82d4947ec7bcddaaf22cf95ef0e11103c72cd8e901ad281c31b0901211ebd81
'http://archive.ubuntu.com/ubuntu/pool/main/f/fontconfig/fontconfig_2.15.0.orig.tar.xz' fontconfig_2.15.0.orig.tar.xz 1447820 SHA512:754cd5fffa198fc07a39cf7df683e9adfa7f54ab41fdff8c0eacc078fd35d3e01069ba343f2b045e0b40df88d9f1fc1ee0f7565799f9cb194a59cf95b64c4417
'http://archive.ubuntu.com/ubuntu/pool/main/f/fontconfig/fontconfig_2.15.0-2.3ubuntu1.debian.tar.xz' fontconfig_2.15.0-2.3ubuntu1.debian.tar.xz 33544 SHA512:f31328644fc622ad4f70fe04561d8ca67bd3f55079ffb051b428f8ae88b6c508915c8b73132f24bd1b2978ee7e4cdfa61f02d0efb13e6a46123fb937246ed9f7
```

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/freetype/2.13.3+dfsg-1/


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

### `dpkg` source package: `gcc-15=15.2.0-1ubuntu1`

Binary Packages:

- `cpp-15=15.2.0-1ubuntu1`
- `cpp-15-x86-64-linux-gnu=15.2.0-1ubuntu1`
- `g++-15=15.2.0-1ubuntu1`
- `g++-15-x86-64-linux-gnu=15.2.0-1ubuntu1`
- `gcc-15=15.2.0-1ubuntu1`
- `gcc-15-base:amd64=15.2.0-1ubuntu1`
- `gcc-15-x86-64-linux-gnu=15.2.0-1ubuntu1`
- `libasan8:amd64=15.2.0-1ubuntu1`
- `libatomic1:amd64=15.2.0-1ubuntu1`
- `libcc1-0:amd64=15.2.0-1ubuntu1`
- `libgcc-15-dev:amd64=15.2.0-1ubuntu1`
- `libgcc-s1:amd64=15.2.0-1ubuntu1`
- `libgomp1:amd64=15.2.0-1ubuntu1`
- `libhwasan0:amd64=15.2.0-1ubuntu1`
- `libitm1:amd64=15.2.0-1ubuntu1`
- `liblsan0:amd64=15.2.0-1ubuntu1`
- `libquadmath0:amd64=15.2.0-1ubuntu1`
- `libstdc++-15-dev:amd64=15.2.0-1ubuntu1`
- `libstdc++6:amd64=15.2.0-1ubuntu1`
- `libtsan2:amd64=15.2.0-1ubuntu1`
- `libubsan1:amd64=15.2.0-1ubuntu1`

Licenses: (parsed from: `/usr/share/doc/cpp-15/copyright`, `/usr/share/doc/cpp-15-x86-64-linux-gnu/copyright`, `/usr/share/doc/g++-15/copyright`, `/usr/share/doc/g++-15-x86-64-linux-gnu/copyright`, `/usr/share/doc/gcc-15/copyright`, `/usr/share/doc/gcc-15-base/copyright`, `/usr/share/doc/gcc-15-x86-64-linux-gnu/copyright`, `/usr/share/doc/libasan8/copyright`, `/usr/share/doc/libatomic1/copyright`, `/usr/share/doc/libcc1-0/copyright`, `/usr/share/doc/libgcc-15-dev/copyright`, `/usr/share/doc/libgcc-s1/copyright`, `/usr/share/doc/libgomp1/copyright`, `/usr/share/doc/libhwasan0/copyright`, `/usr/share/doc/libitm1/copyright`, `/usr/share/doc/liblsan0/copyright`, `/usr/share/doc/libquadmath0/copyright`, `/usr/share/doc/libstdc++-15-dev/copyright`, `/usr/share/doc/libstdc++6/copyright`, `/usr/share/doc/libtsan2/copyright`, `/usr/share/doc/libubsan1/copyright`)

- `Apache-2.0`
- `Artistic`
- `GFDL-1.2`
- `GPL`
- `GPL-3`
- `LGPL`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `gcc-defaults=1.222ubuntu1`

Binary Packages:

- `cpp=4:15.1.0-1ubuntu1`
- `cpp-x86-64-linux-gnu=4:15.1.0-1ubuntu1`
- `g++=4:15.1.0-1ubuntu1`
- `g++-x86-64-linux-gnu=4:15.1.0-1ubuntu1`
- `gcc=4:15.1.0-1ubuntu1`
- `gcc-x86-64-linux-gnu=4:15.1.0-1ubuntu1`

Licenses: (parsed from: `/usr/share/doc/cpp/copyright`, `/usr/share/doc/cpp-x86-64-linux-gnu/copyright`, `/usr/share/doc/g++/copyright`, `/usr/share/doc/g++-x86-64-linux-gnu/copyright`, `/usr/share/doc/gcc/copyright`, `/usr/share/doc/gcc-x86-64-linux-gnu/copyright`)

- `GPL-2`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `gdbm=1.26-1`

Binary Packages:

- `libgdbm-compat4t64:amd64=1.26-1`
- `libgdbm-dev:amd64=1.26-1`
- `libgdbm6t64:amd64=1.26-1`

Licenses: (parsed from: `/usr/share/doc/libgdbm-compat4t64/copyright`, `/usr/share/doc/libgdbm-dev/copyright`, `/usr/share/doc/libgdbm6t64/copyright`)

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

### `dpkg` source package: `gdk-pixbuf=2.42.12+dfsg-5`

Binary Packages:

- `gir1.2-gdkpixbuf-2.0:amd64=2.42.12+dfsg-5`
- `libgdk-pixbuf-2.0-0:amd64=2.42.12+dfsg-5`
- `libgdk-pixbuf-2.0-dev:amd64=2.42.12+dfsg-5`
- `libgdk-pixbuf2.0-bin=2.42.12+dfsg-5`
- `libgdk-pixbuf2.0-common=2.42.12+dfsg-5`

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
$ apt-get source -qq --print-uris gdk-pixbuf=2.42.12+dfsg-5
'http://archive.ubuntu.com/ubuntu/pool/main/g/gdk-pixbuf/gdk-pixbuf_2.42.12%2bdfsg-5.dsc' gdk-pixbuf_2.42.12+dfsg-5.dsc 3404 SHA512:a5fe010a333897cf0d6b65a00d1b7ff76a5b9084785101b29785d48e9db462f59650b9ad35b8634250cc761ed3a2dd1aa2d8d1cf680a5d00f13b2a9592ba1969
'http://archive.ubuntu.com/ubuntu/pool/main/g/gdk-pixbuf/gdk-pixbuf_2.42.12%2bdfsg.orig.tar.xz' gdk-pixbuf_2.42.12+dfsg.orig.tar.xz 6443656 SHA512:b27ce26fa876416dcb81d1e20679074fcb292f2574c7404cf0748e551888c59d62376499a0511411880fa30fe233757d578fd1d4025bde98e33ab6584c4850d5
'http://archive.ubuntu.com/ubuntu/pool/main/g/gdk-pixbuf/gdk-pixbuf_2.42.12%2bdfsg-5.debian.tar.xz' gdk-pixbuf_2.42.12+dfsg-5.debian.tar.xz 23092 SHA512:100909d8e3e478bc2051ab7cf5292f4f077248674bb6166074cd215e3bdc174c6dc77e5623cc46f1cb811cd0d136da7bb677480fc407e3f48a7717ce5865731b
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

### `dpkg` source package: `glib2.0=2.85.3-1`

Binary Packages:

- `gir1.2-glib-2.0:amd64=2.85.3-1`
- `gir1.2-glib-2.0-dev:amd64=2.85.3-1`
- `girepository-tools:amd64=2.85.3-1`
- `libgio-2.0-dev:amd64=2.85.3-1`
- `libgio-2.0-dev-bin=2.85.3-1`
- `libgirepository-2.0-0:amd64=2.85.3-1`
- `libglib2.0-0t64:amd64=2.85.3-1`
- `libglib2.0-bin=2.85.3-1`
- `libglib2.0-data=2.85.3-1`
- `libglib2.0-dev:amd64=2.85.3-1`
- `libglib2.0-dev-bin=2.85.3-1`

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

- http://snapshot.debian.org/package/glib2.0/2.85.3-1/


### `dpkg` source package: `glibc=2.42-0ubuntu1`

Binary Packages:

- `libc-bin=2.42-0ubuntu1`
- `libc-dev-bin=2.42-0ubuntu1`
- `libc6:amd64=2.42-0ubuntu1`
- `libc6-dev:amd64=2.42-0ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libc-bin/copyright`, `/usr/share/doc/libc-dev-bin/copyright`, `/usr/share/doc/libc6/copyright`, `/usr/share/doc/libc6-dev/copyright`)

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

- `libgmp-dev:amd64=2:6.3.0+dfsg-3ubuntu2`
- `libgmp10:amd64=2:6.3.0+dfsg-3ubuntu2`
- `libgmpxx4ldbl:amd64=2:6.3.0+dfsg-3ubuntu2`

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

- `libgnutls-dane0t64:amd64=3.8.9-3ubuntu1`
- `libgnutls-openssl27t64:amd64=3.8.9-3ubuntu1`
- `libgnutls28-dev:amd64=3.8.9-3ubuntu1`
- `libgnutls30t64:amd64=3.8.9-3ubuntu1`

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


### `dpkg` source package: `gobject-introspection=1.84.0-1`

Binary Packages:

- `gir1.2-freedesktop:amd64=1.84.0-1`
- `gir1.2-freedesktop-dev:amd64=1.84.0-1`

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
$ apt-get source -qq --print-uris gobject-introspection=1.84.0-1
'http://archive.ubuntu.com/ubuntu/pool/main/g/gobject-introspection/gobject-introspection_1.84.0-1.dsc' gobject-introspection_1.84.0-1.dsc 4202 SHA512:0d5587be0180225e62fb749c9c392a5edc133a3ca0d47ef49819a4ea7f43a1ba3cb2ca28bd14f030bd0f75184e8c81d5229c78be2e0785ac5601b09fffdf43cf
'http://archive.ubuntu.com/ubuntu/pool/main/g/gobject-introspection/gobject-introspection_1.84.0.orig-glib.tar.xz' gobject-introspection_1.84.0.orig-glib.tar.xz 5475296 SHA512:6968ac28451a72f2d8d50ce31a887be2c26ae2bc5ddba1a4aadaafb955c1bb11576017084006d78a6e6f09e88696534b94eb50c61b0b0509695a547de34c7620
'http://archive.ubuntu.com/ubuntu/pool/main/g/gobject-introspection/gobject-introspection_1.84.0.orig.tar.xz' gobject-introspection_1.84.0.orig.tar.xz 1080316 SHA512:764b5071472f93ed62bd64983c16fc4f73d4e20575d31eb475b40f4c6643080249aec4c5e9536d0ade719a99844cefa5a6e902b4d58e5644d0c0793212da3e5b
'http://archive.ubuntu.com/ubuntu/pool/main/g/gobject-introspection/gobject-introspection_1.84.0-1.debian.tar.xz' gobject-introspection_1.84.0-1.debian.tar.xz 58824 SHA512:16a4ab4ffcfe5492439f40ff35d1c2fe9737e34b0458f9e155189538b7fabd9b086fa4b69586e2d404ccc40ad0a612234e64a2fd3fc3833cd5db89018df26ad5
```

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

### `dpkg` source package: `icu=76.1-4ubuntu1`

Binary Packages:

- `icu-devtools=76.1-4ubuntu1`
- `libicu-dev:amd64=76.1-4ubuntu1`
- `libicu76:amd64=76.1-4ubuntu1`

Licenses: (parsed from: `/usr/share/doc/icu-devtools/copyright`, `/usr/share/doc/libicu-dev/copyright`, `/usr/share/doc/libicu76/copyright`)

- `GPL-3`
- `MIT`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `imagemagick=8:7.1.1.43+dfsg1-1ubuntu2`

Binary Packages:

- `imagemagick=8:7.1.1.43+dfsg1-1ubuntu2`
- `imagemagick-7-common=8:7.1.1.43+dfsg1-1ubuntu2`
- `imagemagick-7.q16=8:7.1.1.43+dfsg1-1ubuntu2`
- `libmagickcore-7-arch-config:amd64=8:7.1.1.43+dfsg1-1ubuntu2`
- `libmagickcore-7-headers=8:7.1.1.43+dfsg1-1ubuntu2`
- `libmagickcore-7.q16-10:amd64=8:7.1.1.43+dfsg1-1ubuntu2`
- `libmagickcore-7.q16-10-extra:amd64=8:7.1.1.43+dfsg1-1ubuntu2`
- `libmagickcore-7.q16-dev:amd64=8:7.1.1.43+dfsg1-1ubuntu2`
- `libmagickcore-dev=8:7.1.1.43+dfsg1-1ubuntu2`
- `libmagickwand-7-headers=8:7.1.1.43+dfsg1-1ubuntu2`
- `libmagickwand-7.q16-10:amd64=8:7.1.1.43+dfsg1-1ubuntu2`
- `libmagickwand-7.q16-dev:amd64=8:7.1.1.43+dfsg1-1ubuntu2`
- `libmagickwand-dev=8:7.1.1.43+dfsg1-1ubuntu2`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `imath=3.1.12-1ubuntu3`

Binary Packages:

- `libimath-3-1-29t64:amd64=3.1.12-1ubuntu3`
- `libimath-dev:amd64=3.1.12-1ubuntu3`

Licenses: (parsed from: `/usr/share/doc/libimath-3-1-29t64/copyright`, `/usr/share/doc/libimath-dev/copyright`)

- `imath`

Source:

```console
$ apt-get source -qq --print-uris imath=3.1.12-1ubuntu3
'http://archive.ubuntu.com/ubuntu/pool/universe/i/imath/imath_3.1.12-1ubuntu3.dsc' imath_3.1.12-1ubuntu3.dsc 2728 SHA512:d63dc15bf0401348cf5b8f3b931d2ef070651076bc092343d9599754c8f5392b7e4ea801db890b7e6176a11de3537dcf825cc10db230feeed34473dce95b1f8a
'http://archive.ubuntu.com/ubuntu/pool/universe/i/imath/imath_3.1.12.orig.tar.gz' imath_3.1.12.orig.tar.gz 604232 SHA512:32628dfcacb610310b81ffe017a66215cf5fb84c2e0a6ac8c94a68c048be3d2b97eb57965dd253770184d5824cce1e5440b8eefb2834666b273b3193ff108343
'http://archive.ubuntu.com/ubuntu/pool/universe/i/imath/imath_3.1.12.orig.tar.gz.asc' imath_3.1.12.orig.tar.gz.asc 287 SHA512:9b3978e44b531429aba42b9cc4969a470898d9d74652e3809edb0273ba9b127c471aec6570b5d352be738f59810091c0df2c70d39c16d2c32833d173b270f72c
'http://archive.ubuntu.com/ubuntu/pool/universe/i/imath/imath_3.1.12-1ubuntu3.debian.tar.xz' imath_3.1.12-1ubuntu3.debian.tar.xz 10224 SHA512:a17231679aec8877a0c301068ea46b6c314d61a25c562ef4956f9957a209c72a58cb511733faa6faa204a9f91ff063a5c504df40f820244666fc22ada5e12c3f
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

### `dpkg` source package: `jansson=2.14-2build3`

Binary Packages:

- `libjansson4:amd64=2.14-2build3`

Licenses: (parsed from: `/usr/share/doc/libjansson4/copyright`)

- `Expat`

Source:

```console
$ apt-get source -qq --print-uris jansson=2.14-2build3
'http://archive.ubuntu.com/ubuntu/pool/main/j/jansson/jansson_2.14-2build3.dsc' jansson_2.14-2build3.dsc 1937 SHA512:efd4a1e53db5f253d06f16cf97d8a4388cffc853309f4b6b0a15729c23eb8eda426da1ee9f6af2372f7c2fd38620c2785dcbc4b50620ad9b734aab2e87c24130
'http://archive.ubuntu.com/ubuntu/pool/main/j/jansson/jansson_2.14.orig.tar.gz' jansson_2.14.orig.tar.gz 141500 SHA512:c56e2e8d18819e3f5caa46edd4819694a240aeb3524a6f9d9f4465edf65b183d1870bd5d256cdd378d411a52979121369b951406fdf7bf323db5c30001fa1bc4
'http://archive.ubuntu.com/ubuntu/pool/main/j/jansson/jansson_2.14-2build3.debian.tar.xz' jansson_2.14-2build3.debian.tar.xz 5644 SHA512:707f7934f4dac1b8ce3da883b45a26db8382130dddecdb111da6d25d2235957c49d6649e68b2c4fba7193049240e5c7bc0adf83fd5e88e22d3320fb0c5d0e836
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

- `krb5-multidev:amd64=1.21.3-5ubuntu1`
- `libgssapi-krb5-2:amd64=1.21.3-5ubuntu1`
- `libgssrpc4t64:amd64=1.21.3-5ubuntu1`
- `libk5crypto3:amd64=1.21.3-5ubuntu1`
- `libkadm5clnt-mit12:amd64=1.21.3-5ubuntu1`
- `libkadm5srv-mit12:amd64=1.21.3-5ubuntu1`
- `libkdb5-10t64:amd64=1.21.3-5ubuntu1`
- `libkrb5-3:amd64=1.21.3-5ubuntu1`
- `libkrb5-dev:amd64=1.21.3-5ubuntu1`
- `libkrb5support0:amd64=1.21.3-5ubuntu1`

Licenses: (parsed from: `/usr/share/doc/krb5-multidev/copyright`, `/usr/share/doc/libgssapi-krb5-2/copyright`, `/usr/share/doc/libgssrpc4t64/copyright`, `/usr/share/doc/libk5crypto3/copyright`, `/usr/share/doc/libkadm5clnt-mit12/copyright`, `/usr/share/doc/libkadm5srv-mit12/copyright`, `/usr/share/doc/libkdb5-10t64/copyright`, `/usr/share/doc/libkrb5-3/copyright`, `/usr/share/doc/libkrb5-dev/copyright`, `/usr/share/doc/libkrb5support0/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris krb5=1.21.3-5ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.21.3-5ubuntu1.dsc' krb5_1.21.3-5ubuntu1.dsc 3950 SHA512:4eb16117d27b5ebcc2dd57fa2d60e92f0af8d17c6d1dc1239dad2eeb8601edc6cfa0470e2aaccb9cfc48a4756597aa6ac76741fe3601d2a02d1dd8f5848c8c26
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.21.3.orig.tar.gz' krb5_1.21.3.orig.tar.gz 9136145 SHA512:87bc06607f4d95ff604169cea22180703a42d667af05f66f1569b8bd592670c42820b335e5c279e8b4f066d1e7da20f1948a1e4def7c5d295c170cbfc7f49c71
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.21.3-5ubuntu1.debian.tar.xz' krb5_1.21.3-5ubuntu1.debian.tar.xz 111424 SHA512:347af1a11b7a4ec742367c4ca0247f3aa6b3fb7d3313d187b6a062e7330ec6a46ee71dac157f982b51566d6a89f1c23453a3759f594fa5056a416ef8a1608af8
```

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

### `dpkg` source package: `libdatrie=0.2.13-4`

Binary Packages:

- `libdatrie-dev:amd64=0.2.13-4`
- `libdatrie1:amd64=0.2.13-4`

Licenses: (parsed from: `/usr/share/doc/libdatrie-dev/copyright`, `/usr/share/doc/libdatrie1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris libdatrie=0.2.13-4
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libdatrie/libdatrie_0.2.13-4.dsc' libdatrie_0.2.13-4.dsc 2239 SHA512:d96e4fef8faacc25c229de91a605853620882ea231aca1f3bade1e67c4f5dce5ff9d6c0677f3c1d1bc0d064960ed957f4671dbd0d584994862032a5e95666893
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libdatrie/libdatrie_0.2.13.orig.tar.xz' libdatrie_0.2.13.orig.tar.xz 314072 SHA512:db3c879d825ead5871c12ef3a06bb093cb1708a6e7e20775eaf82356af9dd6ad54c6b5cabbe1773f2494d3dfa2426528fdd49441038b6294b70ccb1a3d90099a
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libdatrie/libdatrie_0.2.13-4.debian.tar.xz' libdatrie_0.2.13-4.debian.tar.xz 10068 SHA512:8cb5491476c00e9f05ad9148d6b056677ff8019a733ecf03011a53bfa4b614a177c9445eca3ddc71892a6505cc637b41b861ada1dc5f9e365a01d701cb7c133b
```

### `dpkg` source package: `libde265=1.0.16-1`

Binary Packages:

- `libde265-0:amd64=1.0.16-1`

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
$ apt-get source -qq --print-uris libde265=1.0.16-1
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libde265/libde265_1.0.16-1.dsc' libde265_1.0.16-1.dsc 2246 SHA512:23f62a07b90a0f06ef2516dae6ce702cd2667c3fe3177adf00c3c325ba7ee2ee53e33d93cbaed372421fa084739ceaf15396b851a235c4c26800ce69cfe748f6
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libde265/libde265_1.0.16.orig.tar.gz' libde265_1.0.16.orig.tar.gz 835657 SHA512:07f4dd75238030ed86f1b86d990a5a1c31866d5217db2aa23757432da214a19c5f4094a6c2f8fe3453c64d36ee745ca4f1e22a19a80b2685b6530431a35eb4e1
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libde265/libde265_1.0.16-1.debian.tar.xz' libde265_1.0.16-1.debian.tar.xz 136856 SHA512:32f390ab3fc42c5c5fdab23e6eb196433e6f1b34359553e82eb87c48101076479f6eb3c3fad150755f9b1a3711aaee8beeb34c32158442e27abc31f7a8e5cc58
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
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libdeflate/libdeflate_1.23-2.dsc' libdeflate_1.23-2.dsc 1743 SHA512:801a2cc0a6ceae6c8803993afb268324938fa63d2204ae2de03507c3465bc71a01799cceef8e73a2bfcac99dc405805e5fc84e8a3e25a25831bed8175364ed44
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libdeflate/libdeflate_1.23.orig.tar.gz' libdeflate_1.23.orig.tar.gz 197519 SHA512:c1effb9c5ee8d65bc12ae3d0669a4a394acace13cc146300ed24a7f12a0ec058f66729e1ffbae268711bdcc4151143752ab2d56a099dd6394b2735e8e2f1b671
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libdeflate/libdeflate_1.23-2.debian.tar.xz' libdeflate_1.23-2.debian.tar.xz 5624 SHA512:2b3d9fb55fba97b0dbc37b0b2c65554011ba938a189492f3910f9469589c438b18ecf26b6434171db7170da327142b5a8f6f38f9916c114edd0f5eb0d4a5a4ab
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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/libevent/2.1.12-stable-10/


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

### `dpkg` source package: `libffi=3.5.2-1`

Binary Packages:

- `libffi-dev:amd64=3.5.2-1`
- `libffi8:amd64=3.5.2-1`

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

### `dpkg` source package: `libheif=1.20.2-1`

Binary Packages:

- `libheif-plugin-aomdec:amd64=1.20.2-1`
- `libheif-plugin-libde265:amd64=1.20.2-1`
- `libheif1:amd64=1.20.2-1`

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

Source:

```console
$ apt-get source -qq --print-uris libheif=1.20.2-1
'http://archive.ubuntu.com/ubuntu/pool/main/libh/libheif/libheif_1.20.2-1.dsc' libheif_1.20.2-1.dsc 3697 SHA512:d526d6615fc001e13564fe1406ecc0530e8070c97a7bbbae6a156f6e4760c64201ab436aef71e93c80fcfe2464aeb166acea8ebd5362083159b40861651f6816
'http://archive.ubuntu.com/ubuntu/pool/main/libh/libheif/libheif_1.20.2.orig.tar.gz' libheif_1.20.2.orig.tar.gz 1787518 SHA512:0ab8669d2ee1ed619c89cbe3fa3a7618c25d26a7e4c65801dd4db163d4a584fde13b32ed0996461e81bd42ed4def8f4eb7b296b15b7819e90c0a7d5a8c08b06b
'http://archive.ubuntu.com/ubuntu/pool/main/libh/libheif/libheif_1.20.2-1.debian.tar.xz' libheif_1.20.2-1.debian.tar.xz 13724 SHA512:43c5bfbcc743a1bb541b23d9ae64b9bdf528876f754fc3eb446866696aaf55f78a47dbaeb5b3d54a86f1f58459ccddec3a7f07f7c64c54b400b64317784156da
```

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

### `dpkg` source package: `libidn2=2.3.8-4`

Binary Packages:

- `libidn2-0:amd64=2.3.8-4`
- `libidn2-dev:amd64=2.3.8-4`

Licenses: (parsed from: `/usr/share/doc/libidn2-0/copyright`, `/usr/share/doc/libidn2-dev/copyright`)

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

### `dpkg` source package: `libjpeg-turbo=2.1.5-4ubuntu2`

Binary Packages:

- `libjpeg-turbo8:amd64=2.1.5-4ubuntu2`
- `libjpeg-turbo8-dev:amd64=2.1.5-4ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libjpeg-turbo8/copyright`, `/usr/share/doc/libjpeg-turbo8-dev/copyright`)

- `BSD-3-clause`
- `BSD-BY-LC-NE`
- `Expat`
- `NTP`
- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris libjpeg-turbo=2.1.5-4ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/libj/libjpeg-turbo/libjpeg-turbo_2.1.5-4ubuntu2.dsc' libjpeg-turbo_2.1.5-4ubuntu2.dsc 2523 SHA512:8f34e6d7badb03e9c0dc2deb68f552c60a7ffdc47d956578fb4d6eac7471df7b1f80d1640cf4940cfb35a1b3e6dcfdc0470deae6f8084463ade83f0cc2fcf2ff
'http://archive.ubuntu.com/ubuntu/pool/main/libj/libjpeg-turbo/libjpeg-turbo_2.1.5.orig.tar.gz' libjpeg-turbo_2.1.5.orig.tar.gz 2264471 SHA512:20036303fbe5703a5742dc3778cc5deb2eb98d00a9852e7e80ba73c195bba011ec206c090589c482f1153f74505c3fe06d96af00f6beaa65a7fcf7ffaf626fc2
'http://archive.ubuntu.com/ubuntu/pool/main/libj/libjpeg-turbo/libjpeg-turbo_2.1.5-4ubuntu2.debian.tar.xz' libjpeg-turbo_2.1.5-4ubuntu2.debian.tar.xz 109028 SHA512:9708c3d6fbeba88976618fb61cbece16e7ee3d6e11de2e940d8ec3521ac3d235d8d98005d59c944587f33f9240f6b434d7b64458804d6ea369181596c5439ffc
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

### `dpkg` source package: `libmaxminddb=1.12.2-1`

Binary Packages:

- `libmaxminddb-dev:amd64=1.12.2-1`
- `libmaxminddb0:amd64=1.12.2-1`

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

- http://snapshot.debian.org/package/libmaxminddb/1.12.2-1/


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


### `dpkg` source package: `libpng1.6=1.6.50-1`

Binary Packages:

- `libpng-dev:amd64=1.6.50-1`
- `libpng16-16t64:amd64=1.6.50-1`

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
$ apt-get source -qq --print-uris libpng1.6=1.6.50-1
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpng1.6/libpng1.6_1.6.50-1.dsc' libpng1.6_1.6.50-1.dsc 2254 SHA512:286e2521f1834d640bd3e91775500f44e0cce363e45baa43334ec606fd974888fba3e575df382918257f6e60957571119b177a2f4a98bcbfa84c24091b93c368
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpng1.6/libpng1.6_1.6.50.orig.tar.gz' libpng1.6_1.6.50.orig.tar.gz 1582079 SHA512:34c806e0dda960b480ce2f5ea13e2e55a9540f07c51948be25d312b901c431bc814f730f9322a2e3b6f88d4104a0c49bde9e616762b342d07db44e2c7fd5f2dc
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpng1.6/libpng1.6_1.6.50-1.debian.tar.xz' libpng1.6_1.6.50-1.debian.tar.xz 33300 SHA512:c31aef43e649f7c060cb153449aea1bcfe0ff048b58ff95dc35ef77edfd011e4d86609742094e1e8cd444c5b8dd4177a21be16aae91e295825905179b2d8f352
```

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

### `dpkg` source package: `libraw=0.21.4-2`

Binary Packages:

- `libraw23t64:amd64=0.21.4-2`

Licenses: (parsed from: `/usr/share/doc/libraw23t64/copyright`)

- `CC-BY-SA-3.0`
- `CDDL-1.0`
- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libraw=0.21.4-2
'http://archive.ubuntu.com/ubuntu/pool/main/libr/libraw/libraw_0.21.4-2.dsc' libraw_0.21.4-2.dsc 2187 SHA512:fa920e02921a34543f86a5433821165f324f84e58293121da452ca7db48a21739f84a46f5581d0e300e35d8475c88a132384b0345659759dfa71b4d093aef5d7
'http://archive.ubuntu.com/ubuntu/pool/main/libr/libraw/libraw_0.21.4.orig.tar.gz' libraw_0.21.4.orig.tar.gz 566327 SHA512:d8366d62f32f02466128ecfedf9a9b39289834a73d89d57004cf7df63919e66808ba283cddf5843b25fe903d72eb988ac5b490525083e2b5d84a05c7679b4014
'http://archive.ubuntu.com/ubuntu/pool/main/libr/libraw/libraw_0.21.4-2.debian.tar.xz' libraw_0.21.4-2.debian.tar.xz 24312 SHA512:baa743a17360c6acf002d628e1b7a8c8fea3c6d6aaaa160e991f7fbc9252217ac1e0c0d642062b200f2a0e1b27f31bde1fa9a40c915a6a515594fd71f04fb1e6
```

### `dpkg` source package: `librsvg=2.60.0+dfsg-1build1`

Binary Packages:

- `gir1.2-rsvg-2.0:amd64=2.60.0+dfsg-1build1`
- `librsvg2-2:amd64=2.60.0+dfsg-1build1`
- `librsvg2-common:amd64=2.60.0+dfsg-1build1`
- `librsvg2-dev:amd64=2.60.0+dfsg-1build1`

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
$ apt-get source -qq --print-uris librsvg=2.60.0+dfsg-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/libr/librsvg/librsvg_2.60.0%2bdfsg-1build1.dsc' librsvg_2.60.0+dfsg-1build1.dsc 3081 SHA512:1bef73e631fc3dbeb72ce858a2144ea1e13425b087192660fe51dd34087758ceed55baba641485bb75108cf5860c0361187513613ac618c816f0bd167f0abd9f
'http://archive.ubuntu.com/ubuntu/pool/main/libr/librsvg/librsvg_2.60.0%2bdfsg.orig.tar.xz' librsvg_2.60.0+dfsg.orig.tar.xz 6735208 SHA512:7015dd4b5c1bc90eb24ec5939ef66d973fafb62a1fe6e2da8035b362e96aeb7bdbebdc5b13c9bf734a3d9bbda7ad58315e4806bfb3598a168aef6034b2f371d3
'http://archive.ubuntu.com/ubuntu/pool/main/libr/librsvg/librsvg_2.60.0%2bdfsg-1build1.debian.tar.xz' librsvg_2.60.0+dfsg-1build1.debian.tar.xz 10831804 SHA512:80e5119f2aa5d92308f88aaec95556557c38297319ab80bc13e959861c22686f4f105eeb747c60a8469110ac618e4177bc1b2066f61bb5efa42103792bdc7f4a
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
- `libselinux1-dev:amd64=3.8.1-1`

Licenses: (parsed from: `/usr/share/doc/libselinux1/copyright`, `/usr/share/doc/libselinux1-dev/copyright`)

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

- `libsepol-dev:amd64=3.8.1-1`
- `libsepol2:amd64=3.8.1-1`

Licenses: (parsed from: `/usr/share/doc/libsepol-dev/copyright`, `/usr/share/doc/libsepol2/copyright`)

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

### `dpkg` source package: `libsm=2:1.2.6-1`

Binary Packages:

- `libsm-dev:amd64=2:1.2.6-1`
- `libsm6:amd64=2:1.2.6-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libsm=2:1.2.6-1
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsm/libsm_1.2.6-1.dsc' libsm_1.2.6-1.dsc 2302 SHA512:e430e4fc18cc5dec8e39c9ec8634d48f97b2905ded3f768b8f49b6e80da6af571d63bcfb25c8550274a9bc65fb24bdf5747fefdf471c40050d1ecfe69d29d77d
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsm/libsm_1.2.6.orig.tar.gz' libsm_1.2.6.orig.tar.gz 467497 SHA512:316df49f1573ace0bccbfcdf2b1d22c91ec7a1ceb5b320d142fd33cca81e0e0582a0256764aef594f9b31ac5f63d8823dc04c8a6113019ec54ee26eb9323ded4
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsm/libsm_1.2.6.orig.tar.gz.asc' libsm_1.2.6.orig.tar.gz.asc 833 SHA512:b7a617bc09cdc9e4298576f014932165f6b3cc2dd3f96d35db92f46b7f93260705b37f501fbdefb5810eb8f64f64d9260c39cc5ad7660d226b292804798711ee
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsm/libsm_1.2.6-1.diff.gz' libsm_1.2.6-1.diff.gz 13291 SHA512:bf69da3befddae272ffb2bdf2c893fe7f5dc87b48d903a7939787b2e8f8d4c998428d759a86275dc785fb51ce80d1404ebdbb1db67e2ac6fccf8814035083099
```

### `dpkg` source package: `libssh2=1.11.1-1`

Binary Packages:

- `libssh2-1-dev:amd64=1.11.1-1`
- `libssh2-1t64:amd64=1.11.1-1`

Licenses: (parsed from: `/usr/share/doc/libssh2-1-dev/copyright`, `/usr/share/doc/libssh2-1t64/copyright`)

- `BSD3`
- `ISC`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/libssh2/1.11.1-1/


### `dpkg` source package: `libtasn1-6=4.20.0-2`

Binary Packages:

- `libtasn1-6:amd64=4.20.0-2`
- `libtasn1-6-dev:amd64=4.20.0-2`

Licenses: (parsed from: `/usr/share/doc/libtasn1-6/copyright`, `/usr/share/doc/libtasn1-6-dev/copyright`)

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

### `dpkg` source package: `libtool=2.5.4-4`

Binary Packages:

- `libltdl-dev:amd64=2.5.4-4`
- `libltdl7:amd64=2.5.4-4`
- `libtool=2.5.4-4`

Licenses: (parsed from: `/usr/share/doc/libltdl-dev/copyright`, `/usr/share/doc/libltdl7/copyright`, `/usr/share/doc/libtool/copyright`)

- `GFDL-1.3`
- `GFDL-NIV-1.3+`
- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/libtool/2.5.4-4/


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

### `dpkg` source package: `libx11=2:1.8.12-1`

Binary Packages:

- `libx11-6:amd64=2:1.8.12-1`
- `libx11-data=2:1.8.12-1`
- `libx11-dev:amd64=2:1.8.12-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/libx11/2:1.8.12-1/


### `dpkg` source package: `libxau=1:1.0.11-1`

Binary Packages:

- `libxau-dev:amd64=1:1.0.11-1`
- `libxau6:amd64=1:1.0.11-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/libxau/1:1.0.11-1/


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


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/libxcb/1.17.0-2/


### `dpkg` source package: `libxcrypt=1:4.4.38-1`

Binary Packages:

- `libcrypt-dev:amd64=1:4.4.38-1`
- `libcrypt1:amd64=1:4.4.38-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/libxcrypt/1:4.4.38-1/


### `dpkg` source package: `libxdmcp=1:1.1.5-1`

Binary Packages:

- `libxdmcp-dev:amd64=1:1.1.5-1`
- `libxdmcp6:amd64=1:1.1.5-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/libxdmcp/1:1.1.5-1/


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

### `dpkg` source package: `libxml2=2.14.5+dfsg-0.2`

Binary Packages:

- `libxml2-16:amd64=2.14.5+dfsg-0.2`
- `libxml2-dev:amd64=2.14.5+dfsg-0.2`

Licenses: (parsed from: `/usr/share/doc/libxml2-16/copyright`, `/usr/share/doc/libxml2-dev/copyright`)

- `ISC`
- `MIT-1`

Source:

```console
$ apt-get source -qq --print-uris libxml2=2.14.5+dfsg-0.2
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxml2/libxml2_2.14.5%2bdfsg-0.2.dsc' libxml2_2.14.5+dfsg-0.2.dsc 2985 SHA512:6b03f224f500ed11620f2efa05ed42ab0e6c7117d117918c4c6ea56106627c5bc285f4ec8f62dd0e246c58bdf4790a2e4c32000efd475b35cca76f1ed59b5242
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxml2/libxml2_2.14.5%2bdfsg.orig.tar.xz' libxml2_2.14.5+dfsg.orig.tar.xz 1536692 SHA512:8583875597ecae6ece4619b92d3c1ce11d5f3bb93027042d6cafb58ca2c297fc18120862f0aea10273bebe1056687737e28d5452701f7b3eea905076e2259e06
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxml2/libxml2_2.14.5%2bdfsg-0.2.debian.tar.xz' libxml2_2.14.5+dfsg-0.2.debian.tar.xz 36732 SHA512:534e849689eeab4f03302b58eb86c312c74e756e6824afb558183408aac16d675e02a390217be1d72d82acfb39950212c8787e2129e6868dc4ac49a403f63dfe
```

### `dpkg` source package: `libxrender=1:0.9.12-1`

Binary Packages:

- `libxrender-dev:amd64=1:0.9.12-1`
- `libxrender1:amd64=1:0.9.12-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxrender=1:0.9.12-1
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxrender/libxrender_0.9.12-1.dsc' libxrender_0.9.12-1.dsc 2258 SHA512:b8b744c8946fffcaf089dcfe8001a52be38efd3f19bfc87a4d2d454913ad0c8059d83d336de8ccbdd7c7bc92f28981289f63f77c70dfd537d31d7373200c2886
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxrender/libxrender_0.9.12.orig.tar.gz' libxrender_0.9.12.orig.tar.gz 450034 SHA512:b7cbe8ead3a4eeb7c42acede8569361cf11818d98d05ede75a5f0c48c3fb6b1c0b3b62bb2ba6aea19b4804938512e63ebed127928b1a553b518e3ab974bd089d
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxrender/libxrender_0.9.12.orig.tar.gz.asc' libxrender_0.9.12.orig.tar.gz.asc 833 SHA512:299b2654f2bd2b51033072a225a42f75b5e16aff65f6ff171defe9f692f95f69fbcda0b121caf7f4706ee0dd5f9ecef9b2d2ff50a729d40b280fbdeb80ff17cf
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxrender/libxrender_0.9.12-1.diff.gz' libxrender_0.9.12-1.diff.gz 21464 SHA512:91501f3b9bd7a6e2ae0f6038fa7b4e0ac036dcd9c0e58e4f2dbe2a8b7730a54eb506e61727a2822c7008a3693a1fe0dac107937cc79ea31c611fe2ada7198a10
```

### `dpkg` source package: `libxslt=1.1.43-0.1`

Binary Packages:

- `libxslt1-dev:amd64=1.1.43-0.1`
- `libxslt1.1:amd64=1.1.43-0.1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxslt=1.1.43-0.1
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxslt/libxslt_1.1.43-0.1.dsc' libxslt_1.1.43-0.1.dsc 2262 SHA512:ee49010fbcad06e04b5790062b09568a4ae56a5c6f177e7b9ef3a6fd1ef4dc46d67d68ef92ac84d76455960186bd23d1824b1ea45e556bb83a5231db4af8b18c
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxslt/libxslt_1.1.43.orig.tar.xz' libxslt_1.1.43.orig.tar.xz 1518364 SHA512:96110b0397a8f5791f489127574e2143845feb61bea0581d7b7e3c1101fd0718483bae81a7ce417b971bd678293bfd95daddad0dadd3e256c87d41a69faed85a
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxslt/libxslt_1.1.43-0.1.debian.tar.xz' libxslt_1.1.43-0.1.debian.tar.xz 22456 SHA512:bf4759d201b90be9c2280a0ad8747db6a70f016ee94145326c0db302027f28fa0f49a2dc9d123b84d690a0384828d7d9cd9977f8cb02ba6b8b9dda20dc89cadc
```

### `dpkg` source package: `libxt=1:1.2.1-1.2build1`

Binary Packages:

- `libxt-dev:amd64=1:1.2.1-1.2build1`
- `libxt6t64:amd64=1:1.2.1-1.2build1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libyaml=0.2.5-2build2`

Binary Packages:

- `libyaml-0-2:amd64=0.2.5-2build2`
- `libyaml-dev:amd64=0.2.5-2build2`

Licenses: (parsed from: `/usr/share/doc/libyaml-0-2/copyright`, `/usr/share/doc/libyaml-dev/copyright`)

- `Expat`
- `permissive`

Source:

```console
$ apt-get source -qq --print-uris libyaml=0.2.5-2build2
'http://archive.ubuntu.com/ubuntu/pool/main/liby/libyaml/libyaml_0.2.5-2build2.dsc' libyaml_0.2.5-2build2.dsc 2064 SHA512:c8e1c8a965740c00c870dbc774722c5ad493a50d779031da73e3eb61bcf1028c3cfcd78538af5abbc774181cdd2a33fa8c385e4bafdd2fb0daf4c01b4d3d62a5
'http://archive.ubuntu.com/ubuntu/pool/main/liby/libyaml/libyaml_0.2.5.orig.tar.gz' libyaml_0.2.5.orig.tar.gz 85055 SHA512:a0f01e3fc616b65b18a4aa17692ee8ea1a84dc6387d1cf02ac7ef7ab7f46b9744c2aac0a047ff69d6c2da1d2a2d7b355c877da0db57e34d95cd4f37213ab6e7e
'http://archive.ubuntu.com/ubuntu/pool/main/liby/libyaml/libyaml_0.2.5-2build2.debian.tar.xz' libyaml_0.2.5-2build2.debian.tar.xz 5788 SHA512:9418ef05afc122f5245f1cd0e9ddfbc39c61ee4adac2037ae0728ca4a37eaa8d9ce3057ec29bfc7d80d81c6925330d6e46e3c817c2b0f5d73c870e4275c5631e
```

### `dpkg` source package: `libzstd=1.5.7+dfsg-1build1`

Binary Packages:

- `libzstd-dev:amd64=1.5.7+dfsg-1build1`
- `libzstd1:amd64=1.5.7+dfsg-1build1`

Licenses: (parsed from: `/usr/share/doc/libzstd-dev/copyright`, `/usr/share/doc/libzstd1/copyright`)

- `BSD-3-clause`
- `Expat`
- `GPL-2`
- `zlib`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `linux=6.16.0-16.16`

Binary Packages:

- `linux-libc-dev:amd64=6.16.0-16.16`

Licenses: (parsed from: `/usr/share/doc/linux-libc-dev/copyright`)

- `GPL-2`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `lto-disabled-list=68`

Binary Packages:

- `lto-disabled-list=68`

Licenses: (parsed from: `/usr/share/doc/lto-disabled-list/copyright`)

- `GPL-2`
- `GPL-2+`

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

### `dpkg` source package: `lzo2=2.10-3`

Binary Packages:

- `liblzo2-2:amd64=2.10-3`

Licenses: (parsed from: `/usr/share/doc/liblzo2-2/copyright`)

- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/lzo2/2.10-3/


### `dpkg` source package: `m4=1.4.19-8`

Binary Packages:

- `m4=1.4.19-8`

Licenses: (parsed from: `/usr/share/doc/m4/copyright`)

- `GFDL`
- `GPL`

Source:

```console
$ apt-get source -qq --print-uris m4=1.4.19-8
'http://archive.ubuntu.com/ubuntu/pool/main/m/m4/m4_1.4.19-8.dsc' m4_1.4.19-8.dsc 1783 SHA512:96a7dce283af408cdcac4d74b9ed530fb4509c96b7f0d788e3b41fbcb68120c62f412a443e5b5d905509e6bf6539af34e2b842a0fa6fe96736e332d10f654cd1
'http://archive.ubuntu.com/ubuntu/pool/main/m/m4/m4_1.4.19.orig.tar.xz' m4_1.4.19.orig.tar.xz 1654908 SHA512:47f595845c89709727bda0b3fc78e3188ef78ec818965b395532e7041cabe9e49677ee4aca3d042930095a7f8df81de3da1026b23b6897be471f6cf13ddd512b
'http://archive.ubuntu.com/ubuntu/pool/main/m/m4/m4_1.4.19.orig.tar.xz.asc' m4_1.4.19.orig.tar.xz.asc 488 SHA512:d6ac9c6a54c57e9b53fb3e34a60d49df2f46a6e494da0a0c9ae8246b984e68a853b5d8c42677c1a0485c3f36b0bce10a481d3775c0edc1dbdfb27b43545bc31e
'http://archive.ubuntu.com/ubuntu/pool/main/m/m4/m4_1.4.19-8.debian.tar.xz' m4_1.4.19-8.debian.tar.xz 18044 SHA512:eb3fc2d0f314273e96c2fd4a034e2335639c3a42bd701f6e14a4575c12ff12a37e72019a8e528fd274756baaeb5ad29f4c12e5106b361946501ccf479450a1d4
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
'http://archive.ubuntu.com/ubuntu/pool/main/m/make-dfsg/make-dfsg_4.4.1-2.dsc' make-dfsg_4.4.1-2.dsc 1976 SHA512:7b9ea0aeda776b1724c74b0aa2857d3effda31b029a7b47a9d77a509ef33185d72d61827eb2e2bc81170f2172bd961e60379e30b5d1382859aee8181339f0685
'http://archive.ubuntu.com/ubuntu/pool/main/m/make-dfsg/make-dfsg_4.4.1.orig.tar.xz' make-dfsg_4.4.1.orig.tar.xz 1125180 SHA512:7efa533e7c85e0f394d2a9c422c1cf854f304871f0c692ff74eac18597fa53d1a79b41ba1c56b88d8c79f2e6dfb8c3c3ba8640af15756f455167d62e7ed7b04c
'http://archive.ubuntu.com/ubuntu/pool/main/m/make-dfsg/make-dfsg_4.4.1-2.debian.tar.xz' make-dfsg_4.4.1-2.debian.tar.xz 44088 SHA512:dd9442a94e3cd75ec0f2cc3f2f349fd34c25a0ba1dd5e24a62f5778b5002d9b7a4768578b9f814266fceb51b69726c9d37d33f66f3d7f3effca9d1ec786e187f
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

### `dpkg` source package: `mpclib3=1.3.1-1build3`

Binary Packages:

- `libmpc3:amd64=1.3.1-1build3`

Licenses: (parsed from: `/usr/share/doc/libmpc3/copyright`)

- `LGPL-3`

Source:

```console
$ apt-get source -qq --print-uris mpclib3=1.3.1-1build3
'http://archive.ubuntu.com/ubuntu/pool/main/m/mpclib3/mpclib3_1.3.1-1build3.dsc' mpclib3_1.3.1-1build3.dsc 1955 SHA512:57c43d7b61f64e9fb8c8aefaf7a1d724fa789f7cab7e7ac03c2d46e97d741b208823a1e44cfaf2e0eecde12729d0aaa54eebc25f10ae7f9ee7cbfdc2f38141bf
'http://archive.ubuntu.com/ubuntu/pool/main/m/mpclib3/mpclib3_1.3.1.orig.tar.gz' mpclib3_1.3.1.orig.tar.gz 773573 SHA512:4bab4ef6076f8c5dfdc99d810b51108ced61ea2942ba0c1c932d624360a5473df20d32b300fc76f2ba4aa2a97e1f275c9fd494a1ba9f07c4cb2ad7ceaeb1ae97
'http://archive.ubuntu.com/ubuntu/pool/main/m/mpclib3/mpclib3_1.3.1-1build3.debian.tar.xz' mpclib3_1.3.1-1build3.debian.tar.xz 4864 SHA512:3dc333c17db198bcd33eefc4a49b7c00e90f0ebd59af87326c415c043bdef857b76c1a8257ca3d793a68814f0ac766d20d07eaada8bb44c40a22d7e4ec7d1303
```

### `dpkg` source package: `mpfr4=4.2.2-1build1`

Binary Packages:

- `libmpfr6:amd64=4.2.2-1build1`

Licenses: (parsed from: `/usr/share/doc/libmpfr6/copyright`)

- `GFDL-1.2`
- `LGPL-3`

Source:

```console
$ apt-get source -qq --print-uris mpfr4=4.2.2-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/m/mpfr4/mpfr4_4.2.2-1build1.dsc' mpfr4_4.2.2-1build1.dsc 1958 SHA512:8483c16c2396eff67f00409b0bad2b28a9101f25c87e15e4e2ddac0f6b501001e26cf1d703870596d130cf49e0c6b98a057adefb9b52808e95c3ce2cf6379cd6
'http://archive.ubuntu.com/ubuntu/pool/main/m/mpfr4/mpfr4_4.2.2.orig.tar.xz' mpfr4_4.2.2.orig.tar.xz 1505596 SHA512:eb9e7f51b5385fb349cc4fba3a45ffdf0dd53be6dfc74932dc01258158a10514667960c530c47dd9dfc5aa18be2bd94859d80499844c5713710581e6ac6259a9
'http://archive.ubuntu.com/ubuntu/pool/main/m/mpfr4/mpfr4_4.2.2-1build1.debian.tar.xz' mpfr4_4.2.2-1build1.debian.tar.xz 12612 SHA512:67218d0638568497174a1131386585e28b31fdb5a961dc508f993e6ef653c2785d91daa8aaa431b34f9ce6aad87ed3f25a1627a5a0575be8c7f5954cb28207ec
```

### `dpkg` source package: `mysql-8.4=8.4.6-0ubuntu3`

Binary Packages:

- `libmysqlclient-dev=8.4.6-0ubuntu3`
- `libmysqlclient24:amd64=8.4.6-0ubuntu3`

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

Source:

```console
$ apt-get source -qq --print-uris mysql-8.4=8.4.6-0ubuntu3
'http://archive.ubuntu.com/ubuntu/pool/main/m/mysql-8.4/mysql-8.4_8.4.6-0ubuntu3.dsc' mysql-8.4_8.4.6-0ubuntu3.dsc 3764 SHA512:5e096fc1c14d2aae12cd1414a66f9e0aabd24f26162f03c7c281a6f31b3a33f6b7eca8c55345bb06c316e93a47fe1e8d6e951c2e8475d93f8166d590b927782c
'http://archive.ubuntu.com/ubuntu/pool/main/m/mysql-8.4/mysql-8.4_8.4.6.orig.tar.gz' mysql-8.4_8.4.6.orig.tar.gz 479211975 SHA512:2d498dc71eeede4368bd70fb1d1c012abd774732e341312f469afa3823c3b37489032b3290fa7531fb78c2b36251dbd1b8e1554c9330e18e56407f96fb8d4a1e
'http://archive.ubuntu.com/ubuntu/pool/main/m/mysql-8.4/mysql-8.4_8.4.6.orig.tar.gz.asc' mysql-8.4_8.4.6.orig.tar.gz.asc 833 SHA512:afcdbc55f74ad437f0811954c74edd9f203a527d35a6685407d13de8e0cadd511268064a92f3a05e7e05ecff0f81ba0341bab3a5897b5f6575af159626dd2e88
'http://archive.ubuntu.com/ubuntu/pool/main/m/mysql-8.4/mysql-8.4_8.4.6-0ubuntu3.debian.tar.xz' mysql-8.4_8.4.6-0ubuntu3.debian.tar.xz 135236 SHA512:5565f736f30b04fa62596ebf68a91261513603059d431e2cadd0eaf0f84b7638a4457215762739e5d95dea33b7859e612569c106fd489546cec49f9f02339157
```

### `dpkg` source package: `mysql-defaults=1.1.1ubuntu1`

Binary Packages:

- `default-libmysqlclient-dev:amd64=1.1.1ubuntu1`
- `mysql-common=5.8+1.1.1ubuntu1`

Licenses: (parsed from: `/usr/share/doc/default-libmysqlclient-dev/copyright`, `/usr/share/doc/mysql-common/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris mysql-defaults=1.1.1ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/m/mysql-defaults/mysql-defaults_1.1.1ubuntu1.dsc' mysql-defaults_1.1.1ubuntu1.dsc 2346 SHA512:77e64232d994672d6faf8fede229f910b25255dc9a0b85272b6de36a64b3a295ed5649d7b2c0f7e1206da309c2f36176fa2a21c51ce4b57180901074fcf9024a
'http://archive.ubuntu.com/ubuntu/pool/main/m/mysql-defaults/mysql-defaults_1.1.1ubuntu1.tar.xz' mysql-defaults_1.1.1ubuntu1.tar.xz 7568 SHA512:8b0e5a51716845bcfa1f922f41ca83677c07587b0a14335e8251317406a14d53c126e9fefb6d5ac531bd27057533b869287b1d862ad95d277cfc57e0e131631c
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
- `nettle-dev:amd64=3.10.1-1`

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
- `libnghttp2-dev:amd64=1.64.0-1.1build1`

Licenses: (parsed from: `/usr/share/doc/libnghttp2-14/copyright`, `/usr/share/doc/libnghttp2-dev/copyright`)

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

### `dpkg` source package: `openexr=3.1.13-2`

Binary Packages:

- `libopenexr-3-1-30:amd64=3.1.13-2`
- `libopenexr-dev=3.1.13-2`

Licenses: (parsed from: `/usr/share/doc/libopenexr-3-1-30/copyright`, `/usr/share/doc/libopenexr-dev/copyright`)

- `BSD-3-clause`
- `openexr`

Source:

```console
$ apt-get source -qq --print-uris openexr=3.1.13-2
'http://archive.ubuntu.com/ubuntu/pool/universe/o/openexr/openexr_3.1.13-2.dsc' openexr_3.1.13-2.dsc 2144 SHA512:b6fb1b31c486856cb1df6b563adb672739e14d83c8ee02a00fa9ff054b4b7ade2109e6ef69231888b75a043b09a5ce522afdf0805181155a0a552427777eaca7
'http://archive.ubuntu.com/ubuntu/pool/universe/o/openexr/openexr_3.1.13.orig.tar.gz' openexr_3.1.13.orig.tar.gz 20542408 SHA512:662ebfce32bc56e3b5140e7d1813b8c117ac6e806fe30c996b956465ce20ee43f1f535b97868a87a26d1d7909d7f59acbe383f335ab8d72ad1484408cbabf77b
'http://archive.ubuntu.com/ubuntu/pool/universe/o/openexr/openexr_3.1.13-2.debian.tar.xz' openexr_3.1.13-2.debian.tar.xz 19268 SHA512:15bf6e5ac0acabe728ba2ef5c6f962be82ac410ab3fa882bb5f9adaa8b11c9ea6d0366f0eb590c47609fc08f444289a9585b04fdfd85f2f4c8417167ba3d0ab3
```

### `dpkg` source package: `openjpeg2=2.5.3-2.1`

Binary Packages:

- `libopenjp2-7:amd64=2.5.3-2.1`
- `libopenjp2-7-dev:amd64=2.5.3-2.1`

Licenses: (parsed from: `/usr/share/doc/libopenjp2-7/copyright`, `/usr/share/doc/libopenjp2-7-dev/copyright`)

- `BSD-2`
- `BSD-3`
- `LIBPNG`
- `LIBTIFF`
- `LIBTIFF-GLARSON`
- `LIBTIFF-PIXAR`
- `MIT`
- `ZLIB`

Source:

```console
$ apt-get source -qq --print-uris openjpeg2=2.5.3-2.1
'http://archive.ubuntu.com/ubuntu/pool/main/o/openjpeg2/openjpeg2_2.5.3-2.1.dsc' openjpeg2_2.5.3-2.1.dsc 2571 SHA512:424df8f01abbc46082eb289c7b3c1af8fa75841c072d6ba96624844fc8e12519db7f346ddd8f26f22d02f886bb279353d686798c22e69f4c1b7f595bab6f0642
'http://archive.ubuntu.com/ubuntu/pool/main/o/openjpeg2/openjpeg2_2.5.3.orig.tar.xz' openjpeg2_2.5.3.orig.tar.xz 1393716 SHA512:aae4bf4d677a5c8395886b6ab051ffccb9d7bc0de2f4df44932296ab54ef3d936ac4848856ed6011dfb77c349e3383766634bf3e2244c2cf2c42aff55b98471b
'http://archive.ubuntu.com/ubuntu/pool/main/o/openjpeg2/openjpeg2_2.5.3-2.1.debian.tar.xz' openjpeg2_2.5.3-2.1.debian.tar.xz 15688 SHA512:4af7b0fb7b28acad335c4dbb40dd0bd17c2e30df3d6ef9cd31089c88ce83c197b218251398f7f17425e03036d2c0cf0e6962e6f8e7b3a49c6cbc9b37fef751a0
```

### `dpkg` source package: `openldap=2.6.10+dfsg-1ubuntu1`

Binary Packages:

- `libldap-common=2.6.10+dfsg-1ubuntu1`
- `libldap-dev:amd64=2.6.10+dfsg-1ubuntu1`
- `libldap2:amd64=2.6.10+dfsg-1ubuntu1`

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

- `libssl-dev:amd64=3.5.0-2ubuntu1`
- `libssl3t64:amd64=3.5.0-2ubuntu1`
- `openssl=3.5.0-2ubuntu1`
- `openssl-provider-legacy=3.5.0-2ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libssl-dev/copyright`, `/usr/share/doc/libssl3t64/copyright`, `/usr/share/doc/openssl/copyright`, `/usr/share/doc/openssl-provider-legacy/copyright`)

- `Apache-2.0`
- `Artistic`
- `GPL-1`
- `GPL-1+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `p11-kit=0.25.5-3ubuntu1`

Binary Packages:

- `libp11-kit-dev:amd64=0.25.5-3ubuntu1`
- `libp11-kit0:amd64=0.25.5-3ubuntu1`

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


### `dpkg` source package: `pango1.0=1.56.3-1`

Binary Packages:

- `gir1.2-pango-1.0:amd64=1.56.3-1`
- `libpango-1.0-0:amd64=1.56.3-1`
- `libpango1.0-dev:amd64=1.56.3-1`
- `libpangocairo-1.0-0:amd64=1.56.3-1`
- `libpangoft2-1.0-0:amd64=1.56.3-1`
- `libpangoxft-1.0-0:amd64=1.56.3-1`
- `pango1.0-tools=1.56.3-1`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/pango1.0/1.56.3-1/


### `dpkg` source package: `patch=2.8-2`

Binary Packages:

- `patch=2.8-2`

Licenses: (parsed from: `/usr/share/doc/patch/copyright`)

- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris patch=2.8-2
'http://archive.ubuntu.com/ubuntu/pool/main/p/patch/patch_2.8-2.dsc' patch_2.8-2.dsc 1689 SHA512:cf43a4b896395c4dfe05ae87636a18c47f34c4d149029c19ae2826f700254eb484f760ff41c793b7eb066e1b91e097d3dd2e40636f47a6efd6cbfa3df7f49565
'http://archive.ubuntu.com/ubuntu/pool/main/p/patch/patch_2.8.orig.tar.xz' patch_2.8.orig.tar.xz 907208 SHA512:d689d696660a662753e8660792733c3be0a94c76abfe7a28b0f9f70300c3a42d6437d081553a59bfde6e1b0d5ee13ed89be48d0b00b6da2cadbfc14a15ada603
'http://archive.ubuntu.com/ubuntu/pool/main/p/patch/patch_2.8-2.debian.tar.xz' patch_2.8-2.debian.tar.xz 9460 SHA512:3881b0cbd510932ee06ecb5ba85786d44f1ea7336ad8bd1ebd23d0e0ff1db2c589111781a9565388296b46985303d5c4102953b12a9d0035500e4554d0ed8bcd
```

### `dpkg` source package: `pcre2=10.46-1`

Binary Packages:

- `libpcre2-16-0:amd64=10.46-1`
- `libpcre2-32-0:amd64=10.46-1`
- `libpcre2-8-0:amd64=10.46-1`
- `libpcre2-dev:amd64=10.46-1`
- `libpcre2-posix3:amd64=10.46-1`

Licenses: (parsed from: `/usr/share/doc/libpcre2-16-0/copyright`, `/usr/share/doc/libpcre2-32-0/copyright`, `/usr/share/doc/libpcre2-8-0/copyright`, `/usr/share/doc/libpcre2-dev/copyright`, `/usr/share/doc/libpcre2-posix3/copyright`)

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/pkgconf/1.8.1-4/


### `dpkg` source package: `postgresql-17=17.6-1`

Binary Packages:

- `libpq-dev=17.6-1`
- `libpq5:amd64=17.6-1`

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
$ apt-get source -qq --print-uris postgresql-17=17.6-1
'http://archive.ubuntu.com/ubuntu/pool/main/p/postgresql-17/postgresql-17_17.6-1build1.dsc' postgresql-17_17.6-1build1.dsc 4269 SHA512:7a56ba352a33d2cc4db4bd724dad779c38edbda11ada44f3d1a4ab7a9c28b0e4d68a5d5b8e1bcc261a86e0dd7e604acfe09937a6e62567777ba7a89820dc27dd
'http://archive.ubuntu.com/ubuntu/pool/main/p/postgresql-17/postgresql-17_17.6.orig.tar.bz2' postgresql-17_17.6.orig.tar.bz2 21623975 SHA512:d377ed208b3fd1bf9611f148f4286e8c655374218cc3b12cd766917063001750f7dede140065874b7c8bdc2f2b3ecaf15c18cc6cd341929b2c3a574a7797a67e
'http://archive.ubuntu.com/ubuntu/pool/main/p/postgresql-17/postgresql-17_17.6-1build1.debian.tar.xz' postgresql-17_17.6-1build1.debian.tar.xz 27148 SHA512:66ad1acfcdd05506ea80ebe45854fa1f4e4aca61d92111d7df194e62d553603d98230177e618ed2f3020bd5d51cd8b3b9cb63f1ee52205b076b7333a288d12b6
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


### `dpkg` source package: `python-packaging=25.0-1`

Binary Packages:

- `python3-packaging=25.0-1`

Licenses: (parsed from: `/usr/share/doc/python3-packaging/copyright`)

- `Apache-2.0`
- `BSD-2-clause`
- `BSD-3-clause`
- `Expat`

Source:

```console
$ apt-get source -qq --print-uris python-packaging=25.0-1
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-packaging/python-packaging_25.0-1.dsc' python-packaging_25.0-1.dsc 1674 SHA512:2327d61477f19538c65e214f809986e57e6696eb043dace1d0193398ff1584f3ec46ad98c2abe56602a87ac1149fb007cddad9990c17c38b38406bf4f7b0b331
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-packaging/python-packaging_25.0.orig.tar.gz' python-packaging_25.0.orig.tar.gz 165727 SHA512:0672602d2e18c3aee71b3e567b0de572bc8613ee3d24a79a655ded23ac08ec4582193225bc0c0ea390ed81cf5efbb46e8afbe0798d14f2235f811f263c25728c
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-packaging/python-packaging_25.0-1.debian.tar.xz' python-packaging_25.0-1.debian.tar.xz 4144 SHA512:afcbcf5e090922e7e9935b41397056566c93180d4425d5c6d9a5eebc2c1c3d86c355cdc1189316c34fdb2343a6781d5634680425229aafb50e2c32434b7b562a
```

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

- `libreadline-dev:amd64=8.3-1ubuntu1`
- `libreadline8t64:amd64=8.3-1ubuntu1`
- `readline-common=8.3-1ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libreadline-dev/copyright`, `/usr/share/doc/libreadline8t64/copyright`, `/usr/share/doc/readline-common/copyright`)

- `GFDL`
- `GFDL-NIV-1.3+`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `ISC-no-attribution`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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
'http://archive.ubuntu.com/ubuntu/pool/main/r/rpcsvc-proto/rpcsvc-proto_1.4.3-1.dsc' rpcsvc-proto_1.4.3-1.dsc 1999 SHA512:3b63c54c958b9b1e8d76fe59bfb91d8ace5727427daad8bd421ddf149a373f4ab4de6c9b3b1350149f0bbc1a6d394648e50d764261a6f0f8ee5b653b10899358
'http://archive.ubuntu.com/ubuntu/pool/main/r/rpcsvc-proto/rpcsvc-proto_1.4.3.orig.tar.xz' rpcsvc-proto_1.4.3.orig.tar.xz 167964 SHA512:e46ba9ccdd6c520128bf3a154db90742f288a4d593b094a630141cdc5aeb834ffebf9b0eb6d5d0aad9faef3c445c75e2355cbc3e1382b50d29f4d2799441c6e9
'http://archive.ubuntu.com/ubuntu/pool/main/r/rpcsvc-proto/rpcsvc-proto_1.4.3-1.debian.tar.xz' rpcsvc-proto_1.4.3-1.debian.tar.xz 4228 SHA512:16c6107db0a7ba3971bed2ddbb95a5a3ba24bc387f7ef3b869504d2488080c2957bacb48961a5f8b46433e323151ed2644858fffdad566bc4a424da60965309f
```

### `dpkg` source package: `rtmpdump=2.4+20151223.gitfa8646d.1-2build7`

Binary Packages:

- `librtmp-dev:amd64=2.4+20151223.gitfa8646d.1-2build7`
- `librtmp1:amd64=2.4+20151223.gitfa8646d.1-2build7`

Licenses: (parsed from: `/usr/share/doc/librtmp-dev/copyright`, `/usr/share/doc/librtmp1/copyright`)

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


### `dpkg` source package: `shared-mime-info=2.4-5build2`

Binary Packages:

- `shared-mime-info=2.4-5build2`

Licenses: (parsed from: `/usr/share/doc/shared-mime-info/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris shared-mime-info=2.4-5build2
'http://archive.ubuntu.com/ubuntu/pool/main/s/shared-mime-info/shared-mime-info_2.4-5build2.dsc' shared-mime-info_2.4-5build2.dsc 2261 SHA512:4ce3dea6fb04925d62746770bab2279a3d817d9a44c5ed9a0e78f25dcb3190b8accc25bcd6343ad3bcfae9966e1824713419f2f3e0a1b92d2995e85a5e37d340
'http://archive.ubuntu.com/ubuntu/pool/main/s/shared-mime-info/shared-mime-info_2.4.orig.tar.bz2' shared-mime-info_2.4.orig.tar.bz2 7096347 SHA512:712f414e80919bf2a0f5083ced44c54a350948a526850466a6e9f35365dcfd97fad8bcdbb29945de2715a8f9b70a108e931c8500209a4d6e3dddf97af02771cb
'http://archive.ubuntu.com/ubuntu/pool/main/s/shared-mime-info/shared-mime-info_2.4-5build2.debian.tar.xz' shared-mime-info_2.4-5build2.debian.tar.xz 10916 SHA512:151bfa2ac5e81f4a98128ad7caa1cc00bc215eeb601835c50bdf4d68d4908c9a18c12b0cc2155927c9fd1b9250f6583b8cd9982460a471b50f9952987192120c
```

### `dpkg` source package: `sqlite3=3.46.1-7`

Binary Packages:

- `libsqlite3-0:amd64=3.46.1-7`
- `libsqlite3-dev:amd64=3.46.1-7`

Licenses: (parsed from: `/usr/share/doc/libsqlite3-0/copyright`, `/usr/share/doc/libsqlite3-dev/copyright`)

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

### `dpkg` source package: `sysprof=48.0-2`

Binary Packages:

- `libsysprof-capture-4-dev:amd64=48.0-2`

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
$ apt-get source -qq --print-uris sysprof=48.0-2
'http://archive.ubuntu.com/ubuntu/pool/main/s/sysprof/sysprof_48.0-2.dsc' sysprof_48.0-2.dsc 3085 SHA512:b3a1c68b0f07771d5d93900f916f86da859b1768b3ebc290c967f53529d4c230b71c826e826b274b3c30b07074659cdcdef38184cc60ffb2bb90fe92e0c88e6f
'http://archive.ubuntu.com/ubuntu/pool/main/s/sysprof/sysprof_48.0.orig.tar.xz' sysprof_48.0.orig.tar.xz 1224264 SHA512:f687907d616a7d67f605b7874f903714092e32937565206129ce43107205ad27d0e30d82c527e04e232e1420c3b2ff3f60618ba286e303ddd74d959b056be9bc
'http://archive.ubuntu.com/ubuntu/pool/main/s/sysprof/sysprof_48.0-2.debian.tar.xz' sysprof_48.0-2.debian.tar.xz 17728 SHA512:3a340e9aad168dd2acaa3a11de17c9a10675b972e4740a8e3d145a3e2d08c9240f4e70935a510b5acdb7ee99913378525de7f7679119181789b826ae7125a87b
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


### `dpkg` source package: `tiff=4.7.0-3ubuntu2`

Binary Packages:

- `libtiff-dev:amd64=4.7.0-3ubuntu2`
- `libtiff6:amd64=4.7.0-3ubuntu2`
- `libtiffxx6:amd64=4.7.0-3ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libtiff-dev/copyright`, `/usr/share/doc/libtiff6/copyright`, `/usr/share/doc/libtiffxx6/copyright`)

- `Hylafax`

Source:

```console
$ apt-get source -qq --print-uris tiff=4.7.0-3ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/t/tiff/tiff_4.7.0-3ubuntu2.dsc' tiff_4.7.0-3ubuntu2.dsc 2368 SHA512:e843694e2b1715ad3ae806763cc8ae003ed39ff8229b15a395e3018f86acb52815326af23098590b8847c098a04b907faed1fd5a5e2b9bd3d356715ad632a24c
'http://archive.ubuntu.com/ubuntu/pool/main/t/tiff/tiff_4.7.0.orig.tar.bz2' tiff_4.7.0.orig.tar.bz2 2111254 SHA512:6d6f39727a4403ffaae390d54f1d7a6ff926085480422cbc4e2168e8e6490bf283e69361860d0ca0d7951543f48be550641b76d814c24a1b4e4bff1da9e27c6d
'http://archive.ubuntu.com/ubuntu/pool/main/t/tiff/tiff_4.7.0-3ubuntu2.debian.tar.xz' tiff_4.7.0-3ubuntu2.debian.tar.xz 26264 SHA512:51d13db80e4d45d3737dec7420a5320e36ef06a3f01284e9291b3f8f131a33d22c13544db124f4a0f8db9182c809fbf3c5592a9cf59ee2bd8803a91f9f7c2665
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

### `dpkg` source package: `unbound=1.22.0-2ubuntu1`

Binary Packages:

- `libunbound8:amd64=1.22.0-2ubuntu1`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `unzip=6.0-28ubuntu6`

Binary Packages:

- `unzip=6.0-28ubuntu6`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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
- `libblkid-dev:amd64=2.41-4ubuntu3`
- `libblkid1:amd64=2.41-4ubuntu3`
- `liblastlog2-2:amd64=2.41-4ubuntu3`
- `libmount-dev:amd64=2.41-4ubuntu3`
- `libmount1:amd64=2.41-4ubuntu3`
- `libsmartcols1:amd64=2.41-4ubuntu3`
- `libuuid1:amd64=2.41-4ubuntu3`
- `login=1:4.16.0-2+really2.41-4ubuntu3`
- `mount=2.41-4ubuntu3`
- `util-linux=2.41-4ubuntu3`
- `uuid-dev:amd64=2.41-4ubuntu3`

Licenses: (parsed from: `/usr/share/doc/bsdutils/copyright`, `/usr/share/doc/libblkid-dev/copyright`, `/usr/share/doc/libblkid1/copyright`, `/usr/share/doc/liblastlog2-2/copyright`, `/usr/share/doc/libmount-dev/copyright`, `/usr/share/doc/libmount1/copyright`, `/usr/share/doc/libsmartcols1/copyright`, `/usr/share/doc/libuuid1/copyright`, `/usr/share/doc/login/copyright`, `/usr/share/doc/mount/copyright`, `/usr/share/doc/util-linux/copyright`, `/usr/share/doc/uuid-dev/copyright`)

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

### `dpkg` source package: `xorg=1:7.7+24ubuntu1`

Binary Packages:

- `x11-common=1:7.7+24ubuntu1`

Licenses: (parsed from: `/usr/share/doc/x11-common/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris xorg=1:7.7+24ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/x/xorg/xorg_7.7%2b24ubuntu1.dsc' xorg_7.7+24ubuntu1.dsc 2061 SHA512:5d509c36b48b1503b79eec13abc66cc1489c87fe6f54528b2caedf9b9004120e5dac65de1dd2250dea2c55a486a1bcf85d770709260cdccd131d732200ac9813
'http://archive.ubuntu.com/ubuntu/pool/main/x/xorg/xorg_7.7%2b24ubuntu1.tar.xz' xorg_7.7+24ubuntu1.tar.xz 241796 SHA512:12171b148181e632f50141a0cf897cd97d0fb6145cffb781973579addecd92f572d4584a95227754a7bd803a039790a951eccdff0e224b61488d730e2c51efa4
```

### `dpkg` source package: `xorgproto=2024.1-1`

Binary Packages:

- `x11proto-dev=2024.1-1`

Licenses: (parsed from: `/usr/share/doc/x11proto-dev/copyright`)

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


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/xtrans/1.4.0-1/


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

- `liblzma-dev:amd64=5.8.1-1build1`
- `liblzma5:amd64=5.8.1-1build1`
- `xz-utils=5.8.1-1build1`

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


### `dpkg` source package: `zlib=1:1.3.dfsg+really1.3.1-1ubuntu1`

Binary Packages:

- `zlib1g:amd64=1:1.3.dfsg+really1.3.1-1ubuntu1`
- `zlib1g-dev:amd64=1:1.3.dfsg+really1.3.1-1ubuntu1`

Licenses: (parsed from: `/usr/share/doc/zlib1g/copyright`, `/usr/share/doc/zlib1g-dev/copyright`)

- `Zlib`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

