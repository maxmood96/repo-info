# `buildpack-deps:questing`

## Docker Metadata

- Image ID: `sha256:2e3f02d0b0b7c7b8c990cd8870e385abe3beeabc4d1311c8cd9bbaf3ec15215c`
- Created: `2025-05-19T22:25:54Z`
- Virtual Size: ~ 1.75 Gb  
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

### `dpkg` source package: `apt=3.1.3`

Binary Packages:

- `apt=3.1.3`
- `libapt-pkg7.0:amd64=3.1.3`

Licenses: (parsed from: `/usr/share/doc/apt/copyright`, `/usr/share/doc/libapt-pkg7.0/copyright`)

- `BSD-3-clause`
- `Expat`
- `GPL-2`
- `GPL-2+`
- `curl`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/apt/3.1.3/


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
'http://archive.ubuntu.com/ubuntu/pool/main/a/attr/attr_2.5.2-3.dsc' attr_2.5.2-3.dsc 2576 SHA512:042c7034d0c3273b4e6a4485b25e6f7591af0382b3aa2f47e37e840ec12ef023d453fe93281bc95279243d8888d5faa37b141db2890df0a7004967776e519374
'http://archive.ubuntu.com/ubuntu/pool/main/a/attr/attr_2.5.2.orig.tar.xz' attr_2.5.2.orig.tar.xz 334180 SHA512:f587ea544effb7cfed63b3027bf14baba2c2dbe3a9b6c0c45fc559f7e8cb477b3e9a4a826eae30f929409468c50d11f3e7dc6d2500f41e1af8662a7e96a30ef3
'http://archive.ubuntu.com/ubuntu/pool/main/a/attr/attr_2.5.2.orig.tar.xz.asc' attr_2.5.2.orig.tar.xz.asc 833 SHA512:16362013313d055dec307bcf755a9846f5153a78309a499f8cac4ff57a2154de2bc8f3b1400e81dba7a0bf0c67aa02a5d464898ed6e4aa721b64ec95fd313968
'http://archive.ubuntu.com/ubuntu/pool/main/a/attr/attr_2.5.2-3.debian.tar.xz' attr_2.5.2-3.debian.tar.xz 32260 SHA512:9507aab496510a3d13feaa4dc4ae0e7837b9cd8a57d0198db2efd24c5a90ee1af1e9c1bd2e3df232f5e6c0c6be25874517bdcc668b7bc893fca6157a4723c8ef
```

### `dpkg` source package: `audit=1:4.0.5-1`

Binary Packages:

- `libaudit-common=1:4.0.5-1`
- `libaudit1:amd64=1:4.0.5-1`

Licenses: (parsed from: `/usr/share/doc/libaudit-common/copyright`, `/usr/share/doc/libaudit1/copyright`)

- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris audit=1:4.0.5-1
'http://archive.ubuntu.com/ubuntu/pool/main/a/audit/audit_4.0.5-1.dsc' audit_4.0.5-1.dsc 2405 SHA512:3c0f9a4d0efcd8a31a2f4eae4e84fbe42198d258f184997638736427e801fc08c88dada63e6c88eea0f99524e4bc3f6b2bf55095e76b03231943fefa114b8f47
'http://archive.ubuntu.com/ubuntu/pool/main/a/audit/audit_4.0.5.orig.tar.gz' audit_4.0.5.orig.tar.gz 622404 SHA512:14fa19922cf6436284e1448d5a0e069ce5066d2d49d28679fe3ad019be60c133aee6e345b36e0f482ea1fdeadad7d78676f931aab1c25b91a2d0b445dce3eedf
'http://archive.ubuntu.com/ubuntu/pool/main/a/audit/audit_4.0.5-1.debian.tar.xz' audit_4.0.5-1.debian.tar.xz 19844 SHA512:7f91a8b9ddc92ec4404b5e3e1f9720d283418acefd91213a0935ffb49a599a2927e443350c7731db845885a8173e12c77efef08fea5e677748c8afdb61c54f5e
```

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

### `dpkg` source package: `base-files=13.7ubuntu1`

Binary Packages:

- `base-files=13.7ubuntu1`

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

Source:

```console
$ apt-get source -qq --print-uris bash=5.2.37-2ubuntu4
'http://archive.ubuntu.com/ubuntu/pool/main/b/bash/bash_5.2.37-2ubuntu4.dsc' bash_5.2.37-2ubuntu4.dsc 2267 SHA512:d36a0000b9910248949d24d53cdc7f89705f31adfea652c8b0f5903dd53cded07f4cf63a6cd5b4ba0981a51b65cef308595b75a935f61dc2bb25bc13bf622b83
'http://archive.ubuntu.com/ubuntu/pool/main/b/bash/bash_5.2.37.orig.tar.xz' bash_5.2.37.orig.tar.xz 5600932 SHA512:c5380301114967378ace9ae4c510564cb7a827c221470aa532f2360a35000e7719ae081151f3d2ac86dff1d1465f64e60d9202fa6657d716ed6e449f77552158
'http://archive.ubuntu.com/ubuntu/pool/main/b/bash/bash_5.2.37-2ubuntu4.debian.tar.xz' bash_5.2.37-2ubuntu4.debian.tar.xz 96112 SHA512:889c36bbba715630fdbaec8f31c8828f061c29f8de8ab255f60616f1a487229140d3aa62da8eced5407cf66e7f493f1adc95f0518495a631df3869b4b069fee5
```

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

Source:

```console
$ apt-get source -qq --print-uris binutils=2.45-3ubuntu3
'http://archive.ubuntu.com/ubuntu/pool/main/b/binutils/binutils_2.45-3ubuntu3.dsc' binutils_2.45-3ubuntu3.dsc 8951 SHA512:8d7819105969610b0bc2ac694eabc537c9c49b3a5d6995b6ca95ac1fd8bb020394a08aba748f14679f7b71105a2dd899afe31e373f96a658cabaa08d3d127ed4
'http://archive.ubuntu.com/ubuntu/pool/main/b/binutils/binutils_2.45.orig.tar.xz' binutils_2.45.orig.tar.xz 27868232 SHA512:c7b10a7466d9fd398d7a0b3f2a43318432668d714f2ec70069a31bdc93c86d28e0fe83792195727167743707fbae45337c0873a0786416db53bbf22860c16ce7
'http://archive.ubuntu.com/ubuntu/pool/main/b/binutils/binutils_2.45-3ubuntu3.debian.tar.xz' binutils_2.45-3ubuntu3.debian.tar.xz 143116 SHA512:84b470f06e7fb84ca9646e881262a37ed61f0306669068bcd8a1e4380365c6177e51de41e54c31141fff6f003e6d091f927b417439fcf3df4b6a8e0cc52902eb
```

### `dpkg` source package: `brotli=1.1.0-2build4`

Binary Packages:

- `libbrotli-dev:amd64=1.1.0-2build4`
- `libbrotli1:amd64=1.1.0-2build4`

Licenses: (parsed from: `/usr/share/doc/libbrotli-dev/copyright`, `/usr/share/doc/libbrotli1/copyright`)

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

Source:

```console
$ apt-get source -qq --print-uris cairo=1.18.4-1
'http://archive.ubuntu.com/ubuntu/pool/main/c/cairo/cairo_1.18.4-1.dsc' cairo_1.18.4-1.dsc 2763 SHA512:10a8f66af47ad841224eb6cbfd43e2c2c2217b3437582c0458c244a2e7bbc2dffecd3f43a59cca168b2af924c744d414247896cbd032c73a2fcb2c23574660d1
'http://archive.ubuntu.com/ubuntu/pool/main/c/cairo/cairo_1.18.4.orig.tar.xz' cairo_1.18.4.orig.tar.xz 32578804 SHA512:863679f817ed67dc2c916c035d740916e27e7e69c04fca63936e37d274e7f4c79848d16c8f7c481798864602e8847c489f698df89b785cbc576c925dbd513316
'http://archive.ubuntu.com/ubuntu/pool/main/c/cairo/cairo_1.18.4-1.debian.tar.xz' cairo_1.18.4-1.debian.tar.xz 29920 SHA512:f0b298463141bbd82e12e0d1cc6c9e53f3263a4f8eaeb5a5a8d90f985537c26fea69e278324ea8d3c5bc1f43cba2d3e05802297d0e209adbbed58828810d867e
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

Source:

```console
$ apt-get source -qq --print-uris curl=8.14.1-1ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/c/curl/curl_8.14.1-1ubuntu2.dsc' curl_8.14.1-1ubuntu2.dsc 3259 SHA512:1a5fa26df83be94be78301c62f59aa64f4120b7efeffbb42188f35de571101838e3ca577234a32d82c23ec590aabe24930e0b7a67365284c6a6b16f0740e3e93
'http://archive.ubuntu.com/ubuntu/pool/main/c/curl/curl_8.14.1.orig.tar.gz' curl_8.14.1.orig.tar.gz 4250332 SHA512:22307bd41d5ded22e7e53e2412b3218763db9b7c32b1254df26172e6cf00d1650c66874dfc03037da89a5bd72ffbca1eeb83784be62a38d5779484376f3a53c7
'http://archive.ubuntu.com/ubuntu/pool/main/c/curl/curl_8.14.1.orig.tar.gz.asc' curl_8.14.1.orig.tar.gz.asc 488 SHA512:c9b7ad3407660e87fed16a4184a5d75f08815ab569dc8972115430fe750ca5a0a7c72b60e9bacc5ff50084256d1ebc80bb2141f664fa1e0fb239cb86b03f8819
'http://archive.ubuntu.com/ubuntu/pool/main/c/curl/curl_8.14.1-1ubuntu2.debian.tar.xz' curl_8.14.1-1ubuntu2.debian.tar.xz 52948 SHA512:1dab78f1c997f977d121afeec0d2eb372e575e6e5d479f2fb41f15b31db9855f37d996f1efc71fe96dbd6f6775805630f71ac5727eb1953022b2f8a14ef84a17
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

Source:

```console
$ apt-get source -qq --print-uris db5.3=5.3.28+dfsg2-9
'http://archive.ubuntu.com/ubuntu/pool/main/d/db5.3/db5.3_5.3.28%2bdfsg2-9.dsc' db5.3_5.3.28+dfsg2-9.dsc 2373 SHA512:f7b3ee10c42556df8b3fd016d9ebe4efc38d60aba8cbd7120d4573d8242c9260e7507cda3b7a2af3f5501ac3d7b27c5dcaccfc54235eb428f583d4d9adae21f5
'http://archive.ubuntu.com/ubuntu/pool/main/d/db5.3/db5.3_5.3.28%2bdfsg2.orig.tar.xz' db5.3_5.3.28+dfsg2.orig.tar.xz 21287688 SHA512:f9c9d042702ef3fcfdd4b4859583048f3396b161009dc24b6d3a2c53533d58214239fc80e2c42db17e9f092df44d531502737f3b368b956bff49ef057b6b51ef
'http://archive.ubuntu.com/ubuntu/pool/main/d/db5.3/db5.3_5.3.28%2bdfsg2-9.debian.tar.xz' db5.3_5.3.28+dfsg2-9.debian.tar.xz 36412 SHA512:9ed5d57168a50b8adae1c08cc7d1b307904a06a506d85e2faa2bbb4edfaf614b1ef5c3efe11ad71fc5d0f200459a1628c7d092fe121a53a619943c1424031796
```

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

### `dpkg` source package: `dpkg=1.22.21ubuntu1`

Binary Packages:

- `dpkg=1.22.21ubuntu1`
- `dpkg-dev=1.22.21ubuntu1`
- `libdpkg-perl=1.22.21ubuntu1`

Licenses: (parsed from: `/usr/share/doc/dpkg/copyright`, `/usr/share/doc/dpkg-dev/copyright`, `/usr/share/doc/libdpkg-perl/copyright`)

- `GPL-2`
- `GPL-2+`
- `public-domain-s-s-d`

Source:

```console
$ apt-get source -qq --print-uris dpkg=1.22.21ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/d/dpkg/dpkg_1.22.21ubuntu1.dsc' dpkg_1.22.21ubuntu1.dsc 3457 SHA512:28c297d283fe5924fc9a7df9f44ff326c301e1b8cf35c06d27ab53ee83591e30f7a323ed56bf1e21f9c83fa738b04fe67a150eea2694f2c412b3546c4a05b675
'http://archive.ubuntu.com/ubuntu/pool/main/d/dpkg/dpkg_1.22.21ubuntu1.tar.xz' dpkg_1.22.21ubuntu1.tar.xz 5672416 SHA512:ec720f3c5da070b636ab120965c19ac1806b37bf0389dc43a1fb73d263bdb77a4ba6bf68f3a57e430b722e6519cbfe3ab52ce255a87eb2daba1830089ecb5544
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

Source:

```console
$ apt-get source -qq --print-uris e2fsprogs=1.47.2-3ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/e/e2fsprogs/e2fsprogs_1.47.2-3ubuntu1.dsc' e2fsprogs_1.47.2-3ubuntu1.dsc 3292 SHA512:f22372ce4d6f16d1edfd4e6e268cb4ecce5b161a10773da4e726bae40f88dab34c243b28c6e53741db2b2aed2fd130b0513ff7277d1a2359984c43f6982e4b33
'http://archive.ubuntu.com/ubuntu/pool/main/e/e2fsprogs/e2fsprogs_1.47.2.orig.tar.gz' e2fsprogs_1.47.2.orig.tar.gz 9996725 SHA512:dd89139c5e2bf999a22d999686ef06ab42f6ad537c6aeaa3fe68d9734d734b7396fd7ab2fd8002be26860c5653991a666d0df06c804c2f1f07f1274468ec728f
'http://archive.ubuntu.com/ubuntu/pool/main/e/e2fsprogs/e2fsprogs_1.47.2.orig.tar.gz.asc' e2fsprogs_1.47.2.orig.tar.gz.asc 488 SHA512:a22d46cc37497861d5a7e50076b40b8be6f459790f6eaacf0446200776fb74492ca9bfc7abc19edda3c9f7f722c318827b02f9cfbbb2118a8e86bce4d446d56b
'http://archive.ubuntu.com/ubuntu/pool/main/e/e2fsprogs/e2fsprogs_1.47.2-3ubuntu1.debian.tar.xz' e2fsprogs_1.47.2-3ubuntu1.debian.tar.xz 105592 SHA512:f174a673d390f03e1d96fec49560c7d72463c135541107e868eb0b3d222366104dea976b330d155faaf626973d4d0cb68b5df853dc96789cdb0da049b47b75c9
```

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

Source:

```console
$ apt-get source -qq --print-uris file=1:5.46-5
'http://archive.ubuntu.com/ubuntu/pool/main/f/file/file_5.46-5.dsc' file_5.46-5.dsc 2268 SHA512:3cc79f4d9fae23aa3da5c22c989cbfd48b05ac29606b10bee4506225239cf5e6efb1720000b55e6e187279389d795404e885b9be5677eeafc479be157b486dfd
'http://archive.ubuntu.com/ubuntu/pool/main/f/file/file_5.46.orig.tar.gz' file_5.46.orig.tar.gz 1312892 SHA512:a6cb7325c49fd4af159b7555bdd38149e48a5097207acbe5e36deb5b7493ad6ea94d703da6e0edece5bb32959581741f4213707e5cb0528cd46d75a97a5242dc
'http://archive.ubuntu.com/ubuntu/pool/main/f/file/file_5.46.orig.tar.gz.asc' file_5.46.orig.tar.gz.asc 201 SHA512:a6e6fe92d909a9b153c88828942c2963b3b683cda5f6d7ae281e4ca42b30a582e82094b182976515ee85689200b8f6512d34b7f39291cbf9623d583ce688530a
'http://archive.ubuntu.com/ubuntu/pool/main/f/file/file_5.46-5.debian.tar.xz' file_5.46-5.debian.tar.xz 37008 SHA512:c90a5b25655e714d86d3a888b81d2b67c4c2af4ffbdfd700f5a76fb95f799094eee67604545b84a79bd09821037bc3df4d65d072462c023fa89ab4b2c4fc11ae
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

### `dpkg` source package: `gcc-15=15.1.0-11ubuntu1`

Binary Packages:

- `cpp-15=15.1.0-11ubuntu1`
- `cpp-15-x86-64-linux-gnu=15.1.0-11ubuntu1`
- `g++-15=15.1.0-11ubuntu1`
- `g++-15-x86-64-linux-gnu=15.1.0-11ubuntu1`
- `gcc-15=15.1.0-11ubuntu1`
- `gcc-15-base:amd64=15.1.0-11ubuntu1`
- `gcc-15-x86-64-linux-gnu=15.1.0-11ubuntu1`
- `libasan8:amd64=15.1.0-11ubuntu1`
- `libatomic1:amd64=15.1.0-11ubuntu1`
- `libcc1-0:amd64=15.1.0-11ubuntu1`
- `libgcc-15-dev:amd64=15.1.0-11ubuntu1`
- `libgcc-s1:amd64=15.1.0-11ubuntu1`
- `libgomp1:amd64=15.1.0-11ubuntu1`
- `libhwasan0:amd64=15.1.0-11ubuntu1`
- `libitm1:amd64=15.1.0-11ubuntu1`
- `liblsan0:amd64=15.1.0-11ubuntu1`
- `libquadmath0:amd64=15.1.0-11ubuntu1`
- `libstdc++-15-dev:amd64=15.1.0-11ubuntu1`
- `libstdc++6:amd64=15.1.0-11ubuntu1`
- `libtsan2:amd64=15.1.0-11ubuntu1`
- `libubsan1:amd64=15.1.0-11ubuntu1`

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

Source:

```console
$ apt-get source -qq --print-uris gcc-defaults=1.222ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-defaults/gcc-defaults_1.222ubuntu1.dsc' gcc-defaults_1.222ubuntu1.dsc 37375 SHA512:8005980d3223247bf7de7b41511d4d3b55c37876b2a107680754b679d8f08fec0e407c96c28262428515dd463f59a09b28ce4759ff3ad59666cfd5f555dd496d
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-defaults/gcc-defaults_1.222ubuntu1.tar.xz' gcc-defaults_1.222ubuntu1.tar.xz 56852 SHA512:e2616cad2f99e6b514ef35bf5263fda5369179270d8b628c7f2969ce1feed6fbfea9fe4aa4d8831e68a9f502c7be3fa0938656c9333716b1621cbd91fe3f5502
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

### `dpkg` source package: `gdk-pixbuf=2.42.12+dfsg-4build1`

Binary Packages:

- `gir1.2-gdkpixbuf-2.0:amd64=2.42.12+dfsg-4build1`
- `libgdk-pixbuf-2.0-0:amd64=2.42.12+dfsg-4build1`
- `libgdk-pixbuf-2.0-dev:amd64=2.42.12+dfsg-4build1`
- `libgdk-pixbuf2.0-bin=2.42.12+dfsg-4build1`
- `libgdk-pixbuf2.0-common=2.42.12+dfsg-4build1`

Licenses: (parsed from: `/usr/share/doc/gir1.2-gdkpixbuf-2.0/copyright`, `/usr/share/doc/libgdk-pixbuf-2.0-0/copyright`, `/usr/share/doc/libgdk-pixbuf-2.0-dev/copyright`, `/usr/share/doc/libgdk-pixbuf2.0-bin/copyright`, `/usr/share/doc/libgdk-pixbuf2.0-common/copyright`)

- `CC0-1.0`
- `GPL-2`
- `GPL-2+`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `git=1:2.50.0-1ubuntu2`

Binary Packages:

- `git=1:2.50.0-1ubuntu2`
- `git-man=1:2.50.0-1ubuntu2`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `glib2.0=2.85.2-2`

Binary Packages:

- `gir1.2-glib-2.0:amd64=2.85.2-2`
- `gir1.2-glib-2.0-dev:amd64=2.85.2-2`
- `girepository-tools:amd64=2.85.2-2`
- `libgio-2.0-dev:amd64=2.85.2-2`
- `libgio-2.0-dev-bin=2.85.2-2`
- `libgirepository-2.0-0:amd64=2.85.2-2`
- `libglib2.0-0t64:amd64=2.85.2-2`
- `libglib2.0-bin=2.85.2-2`
- `libglib2.0-data=2.85.2-2`
- `libglib2.0-dev:amd64=2.85.2-2`
- `libglib2.0-dev-bin=2.85.2-2`

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

- http://snapshot.debian.org/package/glib2.0/2.85.2-2/


### `dpkg` source package: `glibc=2.41-9ubuntu1`

Binary Packages:

- `libc-bin=2.41-9ubuntu1`
- `libc-dev-bin=2.41-9ubuntu1`
- `libc6:amd64=2.41-9ubuntu1`
- `libc6-dev:amd64=2.41-9ubuntu1`

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

Source:

```console
$ apt-get source -qq --print-uris gnutls28=3.8.9-3ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.8.9-3ubuntu1.dsc' gnutls28_3.8.9-3ubuntu1.dsc 3343 SHA512:b30b0e3a74727eaf6b36b263e21cd4257703aa50d4d77edfae7fd66a784dd9084c6df42ae0bba614203b42a3fc236e8fc5750bf0031e9fdc8e60cf93efbfed2a
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.8.9.orig.tar.xz' gnutls28_3.8.9.orig.tar.xz 6847364 SHA512:b3b201671bf4e75325610a0291d4cd36a669718e22b3685246b64bde97b5bd94f463ab376ed817869869714115f4ff11bdc53c32604bb04a8ff8e10daa6d1fc7
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.8.9.orig.tar.xz.asc' gnutls28_3.8.9.orig.tar.xz.asc 833 SHA512:0eb265bbbc1ee735ecf4e3d308eacf3e3aebe4a9b0848af1fb340ec18e78bb516e1c74a6a72d4764bb03086d88d3ada3cd7ed82861a8f4ca7a403d9a5eb9a3a7
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.8.9-3ubuntu1.debian.tar.xz' gnutls28_3.8.9-3ubuntu1.debian.tar.xz 93052 SHA512:ed0929749ee36fe9c828c725a2e979cff3d2878785e0a9ba9a18d467e317b62829500eb115b47bcf70e3fda5fe134699354611b560584b61ce149ce2a0bf019a
```

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

Source:

```console
$ apt-get source -qq --print-uris gzip=1.13-1ubuntu3
'http://archive.ubuntu.com/ubuntu/pool/main/g/gzip/gzip_1.13-1ubuntu3.dsc' gzip_1.13-1ubuntu3.dsc 1933 SHA512:83f2c4c9726b75b65db28ced4450ec788d3e6dbab6aaf5ab80a6a20aca9fd23634344767ccfcfd109cceab9423d006b7a29b85b20c7c17319134c3e5afa6c97d
'http://archive.ubuntu.com/ubuntu/pool/main/g/gzip/gzip_1.13.orig.tar.xz' gzip_1.13.orig.tar.xz 838248 SHA512:e3d4d4aa4b2e53fdad980620307257c91dfbbc40bcec9baa8d4e85e8327f55e2ece552c9baf209df7b66a07103ab92d4954ac53c86c57fbde5e1dd461143f94c
'http://archive.ubuntu.com/ubuntu/pool/main/g/gzip/gzip_1.13-1ubuntu3.debian.tar.xz' gzip_1.13-1ubuntu3.debian.tar.xz 21364 SHA512:cc6c1acdb8ca29bfcdbc75c462504b57c867e13313bc229a8cebcf681ca0c347af8e5c36da072d1b6e38d13eeb06bca74b97cce4b67306d6d17be6ff66ba6537
```

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

Source:

```console
$ apt-get source -qq --print-uris icu=76.1-4ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/i/icu/icu_76.1-4ubuntu1.dsc' icu_76.1-4ubuntu1.dsc 1940 SHA512:45ea8859874b6b95ab3e064db2cdd7f5525f6865405df2506662aa71599d1b44977c7d8c7fe8e809b15f15381e9f2fb23d1bde68f0a26aa3596978ae24c8c5a7
'http://archive.ubuntu.com/ubuntu/pool/main/i/icu/icu_76.1.orig.tar.gz' icu_76.1.orig.tar.gz 27437767 SHA512:b702ab62fb37a1574d5f4a768326d0f8fa30d9db5b015605b5f8215b5d8547f83d84880c586d3dcc7b6c76f8d47ef34e04b0f51baa55908f737024dd79a42a6c
'http://archive.ubuntu.com/ubuntu/pool/main/i/icu/icu_76.1-4ubuntu1.debian.tar.xz' icu_76.1-4ubuntu1.debian.tar.xz 67176 SHA512:e89750ea2a4f5ca0d7d00769f848019fda8d1842907f22aaff47c5828de4d05ceec96cad55a1e98698b96b3a82b11a610cd3483dce84e0ec3d470d1f8d3ee271
```

### `dpkg` source package: `imagemagick=8:7.1.1.43+dfsg1-1ubuntu1`

Binary Packages:

- `imagemagick=8:7.1.1.43+dfsg1-1ubuntu1`
- `imagemagick-7-common=8:7.1.1.43+dfsg1-1ubuntu1`
- `imagemagick-7.q16=8:7.1.1.43+dfsg1-1ubuntu1`
- `libmagickcore-7-arch-config:amd64=8:7.1.1.43+dfsg1-1ubuntu1`
- `libmagickcore-7-headers=8:7.1.1.43+dfsg1-1ubuntu1`
- `libmagickcore-7.q16-10:amd64=8:7.1.1.43+dfsg1-1ubuntu1`
- `libmagickcore-7.q16-10-extra:amd64=8:7.1.1.43+dfsg1-1ubuntu1`
- `libmagickcore-7.q16-dev:amd64=8:7.1.1.43+dfsg1-1ubuntu1`
- `libmagickcore-dev=8:7.1.1.43+dfsg1-1ubuntu1`
- `libmagickwand-7-headers=8:7.1.1.43+dfsg1-1ubuntu1`
- `libmagickwand-7.q16-10:amd64=8:7.1.1.43+dfsg1-1ubuntu1`
- `libmagickwand-7.q16-dev:amd64=8:7.1.1.43+dfsg1-1ubuntu1`
- `libmagickwand-dev=8:7.1.1.43+dfsg1-1ubuntu1`

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
$ apt-get source -qq --print-uris imagemagick=8:7.1.1.43+dfsg1-1ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/universe/i/imagemagick/imagemagick_7.1.1.43%2bdfsg1-1ubuntu1.dsc' imagemagick_7.1.1.43+dfsg1-1ubuntu1.dsc 5132 SHA512:fc346801273f5449383ee119df1fbb1be118d34bcf326cc5d2cc626efe145a8eb7a2d879afa90a5169eb9cc8dd1d240d344d5975ca43211037da106b2e6a180e
'http://archive.ubuntu.com/ubuntu/pool/universe/i/imagemagick/imagemagick_7.1.1.43%2bdfsg1.orig.tar.xz' imagemagick_7.1.1.43+dfsg1.orig.tar.xz 10501740 SHA512:790bc01e819d2e1c0a00581b8c8bbe10b185eb52e1cdf1312417c4bdca562fe4742374039a6d164e91c7e009f497a375ebf09f579902803b52f9e94354b72a31
'http://archive.ubuntu.com/ubuntu/pool/universe/i/imagemagick/imagemagick_7.1.1.43%2bdfsg1-1ubuntu1.debian.tar.xz' imagemagick_7.1.1.43+dfsg1-1ubuntu1.debian.tar.xz 275420 SHA512:439c8cae2c8d2119608004cddb93b7016f6c993bb91405f7d02e7a4b4f78e5c9c7db7393dc3b2d6a953b392340faf8a3be293fb4865e25b8ea789f016204bc42
```

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

### `dpkg` source package: `jansson=2.14-2build2`

Binary Packages:

- `libjansson4:amd64=2.14-2build2`

Licenses: (parsed from: `/usr/share/doc/libjansson4/copyright`)

- `Expat`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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

Source:

```console
$ apt-get source -qq --print-uris keyutils=1.6.3-6ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/k/keyutils/keyutils_1.6.3-6ubuntu1.dsc' keyutils_1.6.3-6ubuntu1.dsc 2186 SHA512:eda07ee111900ad3882b52bba143947626dd7371b9af7ad367e2c4b5984cbea6a7dbd93547f5d686e2e049c6bd6b39f12b332923d6c07f5fd8d0601b695f1bcd
'http://archive.ubuntu.com/ubuntu/pool/main/k/keyutils/keyutils_1.6.3.orig.tar.gz' keyutils_1.6.3.orig.tar.gz 137022 SHA512:f65965b8566037078b8eeffa66c6fdbe121c8c2bea7fa5bce04cf7ba5ccc50d5b48e51f4a67ca91e4d5d9a12469e7e3eb3036c920ab25e3feba6e93b4c149cf9
'http://archive.ubuntu.com/ubuntu/pool/main/k/keyutils/keyutils_1.6.3-6ubuntu1.debian.tar.xz' keyutils_1.6.3-6ubuntu1.debian.tar.xz 17444 SHA512:8d79cf30bf84466992f2c4991621775c7b65da39aea88f864623434305687c9d89815d91a3db04f6fbfdc9a2a2cb9f24a593e7c864e6ddba04d192ba6898832d
```

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

### `dpkg` source package: `libcap2=1:2.75-7ubuntu1`

Binary Packages:

- `libcap2:amd64=1:2.75-7ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libcap2/copyright`)

- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris libcap2=1:2.75-7ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap2/libcap2_2.75-7ubuntu1.dsc' libcap2_2.75-7ubuntu1.dsc 2785 SHA512:44103fcdef11ed9c54ee1b99223d20efcb0ccdd7a3b38649bb7d8145a10054d85e9a81d0ec8084d3d3abdf7db3b1f23f66fc40dd8d24858cf377fce602b7de5f
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap2/libcap2_2.75.orig.tar.xz' libcap2_2.75.orig.tar.xz 197868 SHA512:229e9b62a1d54024107cbf321fffcb152c0071154554a3fcee6e09e19cc47fd1fd862575135a4fc589b79a043f760bf40d26ea9fd58638f26e809533c017d65f
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap2/libcap2_2.75.orig.tar.xz.asc' libcap2_2.75.orig.tar.xz.asc 833 SHA512:6a6af52ef3a48356d8c205827aa039ed852ec4a1cfea44f00613457380478ebd4946caf933a8ebdf98899b14340b9a7ef9b7151c4659329e2fd80590667d59d9
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap2/libcap2_2.75-7ubuntu1.debian.tar.xz' libcap2_2.75-7ubuntu1.debian.tar.xz 23040 SHA512:e17ce599c0f9eef547f8ee2f5c288d22f771a899f8806c8e511f2fe4af15cbdfc24f01aaeabd1ce4575c2b8c7aa3105d470618e76cef10bc4b82c1622f46e65b
```

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

Source:

```console
$ apt-get source -qq --print-uris libffi=3.5.2-1
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libffi/libffi_3.5.2-1.dsc' libffi_3.5.2-1.dsc 1954 SHA512:62ac97319a4d6e6514a4acf3c1b57ce0052d3ff3b21cc5d63357d95b60794bf9f16deb369b1042a5ea46957226dd6de3601869ff585a4636b05f6a775dd3c1b0
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libffi/libffi_3.5.2.orig.tar.gz' libffi_3.5.2.orig.tar.gz 598870 SHA512:4579932becbe33b2cb3c7a6327a9b47fee67f225ebb4677870ed4402bb7c186966a5b8645dc8a09128af51dcba27c23537e6a34567dbea4e3dc3728cfb51e038
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libffi/libffi_3.5.2-1.debian.tar.xz' libffi_3.5.2-1.debian.tar.xz 10900 SHA512:e8d0e21bbe4ebbe1cc2089b41a299e32200beb6fee09d532eed02b021abf5be6b0f6ff01b1b79b0e7bb818112a502a023cb46dd0977ee7acc923f953612b1b68
```

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

Source:

```console
$ apt-get source -qq --print-uris libgcrypt20=1.11.0-7
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgcrypt20/libgcrypt20_1.11.0-7.dsc' libgcrypt20_1.11.0-7.dsc 2945 SHA512:e01d101b294b25808f0582a028541b9250b57284ba7cd61ca47de19214a43b1681ae7c1a119b882e4a388ef7904150436289b133e1029d3dbac8916bd7b7eebe
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgcrypt20/libgcrypt20_1.11.0.orig.tar.bz2' libgcrypt20_1.11.0.orig.tar.bz2 4180345 SHA512:8e093e69e3c45d30838625ca008e995556f0d5b272de1c003d44ef94633bcc0d0ef5d95e8725eb531bfafb4490ac273488633e0c801200d4666194f86c3e270e
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgcrypt20/libgcrypt20_1.11.0.orig.tar.bz2.asc' libgcrypt20_1.11.0.orig.tar.bz2.asc 228 SHA512:eebd4c599bd8f375445566c3c73df5a223f256cb650cf18d8fed033a1f13a1fb8b9b10a17d686be21ad2bced60fc8e27d71b07e5f556a854a893e44c5dd81ae7
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgcrypt20/libgcrypt20_1.11.0-7.debian.tar.xz' libgcrypt20_1.11.0-7.debian.tar.xz 40452 SHA512:a28c2b413e212d05d7d2f95b9282c9ed9c6406564c746b7da1ed87ac9331dcfa96ad8284cb1ef9db645934d94bd584fde70efde0d97f5691e335dedcb0d183f2
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

### `dpkg` source package: `libheif=1.19.8-1`

Binary Packages:

- `libheif-plugin-aomdec:amd64=1.19.8-1`
- `libheif-plugin-libde265:amd64=1.19.8-1`
- `libheif1:amd64=1.19.8-1`

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

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/libheif/1.19.8-1/


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

### `dpkg` source package: `libidn2=2.3.8-2`

Binary Packages:

- `libidn2-0:amd64=2.3.8-2`
- `libidn2-dev:amd64=2.3.8-2`

Licenses: (parsed from: `/usr/share/doc/libidn2-0/copyright`, `/usr/share/doc/libidn2-dev/copyright`)

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

Source:

```console
$ apt-get source -qq --print-uris libmaxminddb=1.12.2-1
'http://archive.ubuntu.com/ubuntu/pool/main/libm/libmaxminddb/libmaxminddb_1.12.2-1.dsc' libmaxminddb_1.12.2-1.dsc 2235 SHA512:889a0fb420729162a0aa97ce4004c1816ec786407f3bbb065b94622344987bfe1a0e81ecf95a5f3949d5b6bd3b52955f3aa59aa1eb09e4559a655c52ed72210a
'http://archive.ubuntu.com/ubuntu/pool/main/libm/libmaxminddb/libmaxminddb_1.12.2.orig.tar.gz' libmaxminddb_1.12.2.orig.tar.gz 369848 SHA512:88cbccecba2025128babcfb0102f7688982194601974bd3ceaa45ec1bd535e5b6a50c2ce2f214ba5774959987cc64e7f686f76e11672555c690b57a51b1575fa
'http://archive.ubuntu.com/ubuntu/pool/main/libm/libmaxminddb/libmaxminddb_1.12.2-1.debian.tar.xz' libmaxminddb_1.12.2-1.debian.tar.xz 6912 SHA512:9e740ecc2d70574398b563e454ee5016a1663025bf972523e781165c152bf5c670d2eab3012a77ee5f3013ea8f48f0a0e07bbb7a198e301f14ce8f74649970b3
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

### `dpkg` source package: `libpng1.6=1.6.50-1~exp1`

Binary Packages:

- `libpng-dev:amd64=1.6.50-1~exp1`
- `libpng16-16t64:amd64=1.6.50-1~exp1`

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

- http://snapshot.debian.org/package/libpng1.6/1.6.50-1~exp1/


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

Source:

```console
$ apt-get source -qq --print-uris libseccomp=2.6.0-2ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libseccomp/libseccomp_2.6.0-2ubuntu1.dsc' libseccomp_2.6.0-2ubuntu1.dsc 2745 SHA512:6b84f8f24824fdd75d0aa3b20e0105b8c0deee0c761cb76fb51930fc835581bdde3f258c08e686dc9366a8b8fc2db47d2830aaabbd502da9265e6f0549606dc2
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libseccomp/libseccomp_2.6.0.orig.tar.gz' libseccomp_2.6.0.orig.tar.gz 685655 SHA512:9039478656d9b670af2ff4cb67b6b1fa315821e59d2f82ba6247e988859ddc7e3d15fea159eccca161bf2890828bb62aa6ab4d6b7ff55f27a9d6bd9532eeee1b
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libseccomp/libseccomp_2.6.0.orig.tar.gz.asc' libseccomp_2.6.0.orig.tar.gz.asc 833 SHA512:973b69c58085a1567f860e621e3a197be02c0ca71dad664234418cf5c00c39767efd37a7c4016f1be5bd588262617b6603855262db2ee6f31bc16061bc130e0f
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libseccomp/libseccomp_2.6.0-2ubuntu1.debian.tar.xz' libseccomp_2.6.0-2ubuntu1.debian.tar.xz 27796 SHA512:85090c6ebe8c9963999da1adacdde5512294343beda682fd75b3186cd199e0f863eabd6982a612dd7e11229a99d1ee5d6b3a6bb37182d229b97a6103dc677533
```

### `dpkg` source package: `libselinux=3.8.1-1`

Binary Packages:

- `libselinux1:amd64=3.8.1-1`
- `libselinux1-dev:amd64=3.8.1-1`

Licenses: (parsed from: `/usr/share/doc/libselinux1/copyright`, `/usr/share/doc/libselinux1-dev/copyright`)

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
- `libtasn1-6-dev:amd64=4.20.0-2`

Licenses: (parsed from: `/usr/share/doc/libtasn1-6/copyright`, `/usr/share/doc/libtasn1-6-dev/copyright`)

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

Source:

```console
$ apt-get source -qq --print-uris libtool=2.5.4-4
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtool/libtool_2.5.4-4.dsc' libtool_2.5.4-4.dsc 2232 SHA512:ad43301bed7e3f4b4cd1d71dac22d30ae9bfdbf4324d43ac8822c73e3848c3ec61b81de534903a2e5d9c2e8e7968a0c8eb52e5900927283162b2e05fc97118f3
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtool/libtool_2.5.4.orig.tar.xz' libtool_2.5.4.orig.tar.xz 1069572 SHA512:c8ff1fc71373313185ecfff8d282bf3547b8a2d2e102aa4475d7db4945d4f4bfd45cd0d79a8e00a1c1394246908e586f8ccfd9f1cf86ff837b5c6ad7cc57a750
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtool/libtool_2.5.4-4.debian.tar.xz' libtool_2.5.4-4.debian.tar.xz 37504 SHA512:7de009c8737c8d90e648102e95dd73464f6ed4d14fbe9bb8566bd0b44b00205b2350dce2c13378125bc6a209980f2a036fdfe25f7a4b883fc2bff63b0b10eddd
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


Source:

```console
$ apt-get source -qq --print-uris libx11=2:1.8.12-1
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libx11/libx11_1.8.12-1.dsc' libx11_1.8.12-1.dsc 2490 SHA512:26bcf37afdfeb2a35b5f28740e402f3e3ad21396ce909226603ccf4293685afcbfe84e8164c72764b8abce8507a13435f698eba7e74f41dda164bb013ff3311b
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libx11/libx11_1.8.12.orig.tar.gz' libx11_1.8.12.orig.tar.gz 3215077 SHA512:82d62d01176bbb8ee225f6dba741dcbccded62486ae4c70bc7158aa2a19dcf4a795ee9d475a875ed8843a4ae185eb4899d06dac4000b5fe8b5bbb5e13b450153
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libx11/libx11_1.8.12.orig.tar.gz.asc' libx11_1.8.12.orig.tar.gz.asc 833 SHA512:37b5f57a55cb75cb218937175ad06752ab85391c23ac91006a19fe32b82fc86f4b5eca11dba9b38c7d38efbf98aba3eeadcf3cf7bddf11175334ebe8e4d94d23
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libx11/libx11_1.8.12-1.diff.gz' libx11_1.8.12-1.diff.gz 74466 SHA512:819ff6d3ecf0db908457a7a2552e6c42b3cdd3c7bcefd6a9b11b2620952a20c345a106fd57907953969a851bdb37ed2c8f6c6aba1ab3c214e0408388e15a3456
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

### `dpkg` source package: `libxdmcp=1:1.1.5-1`

Binary Packages:

- `libxdmcp-dev:amd64=1:1.1.5-1`
- `libxdmcp6:amd64=1:1.1.5-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxdmcp=1:1.1.5-1
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxdmcp/libxdmcp_1.1.5-1.dsc' libxdmcp_1.1.5-1.dsc 2331 SHA512:a278f99e232e356e41acbf7eec04515527b81c08b19559459dbde7f765fd10c9c34109ca88f62c3fddfc89f31def34ba2b6d9c0c2a8ed9da4328f95540f00ba7
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxdmcp/libxdmcp_1.1.5.orig.tar.gz' libxdmcp_1.1.5.orig.tar.gz 442597 SHA512:400add8f47c28fe9cb80d6159a7268e7f5029d13a6219f3e07087455d99f807aa5b372242be9c14fbb7164b3c8180b8dc5edfeb620412bcbee246162f53c61d3
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxdmcp/libxdmcp_1.1.5.orig.tar.gz.asc' libxdmcp_1.1.5.orig.tar.gz.asc 833 SHA512:e44c62904e5680ede9c3188c2fcf8e453c09d5f89e2958be34196e6f1130177f2e7bbd324337b5ee1902817c09357be0144dd91c2b6fd4e943edebe532c5193c
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxdmcp/libxdmcp_1.1.5-1.diff.gz' libxdmcp_1.1.5-1.diff.gz 9764 SHA512:f817a7787b5dcb9e462382778405ce9b9cfdb693e382c8455396fccec86655fc8e5dd9e83faadf07031830dd922b290cf4da0b4aa3af49dfa2042068c9c76d75
```

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

### `dpkg` source package: `libxml2=2.14.5+dfsg-0exp2`

Binary Packages:

- `libxml2-16:amd64=2.14.5+dfsg-0exp2`
- `libxml2-dev:amd64=2.14.5+dfsg-0exp2`

Licenses: (parsed from: `/usr/share/doc/libxml2-16/copyright`, `/usr/share/doc/libxml2-dev/copyright`)

- `ISC`
- `MIT-1`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/libxml2/2.14.5+dfsg-0exp2/


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

### `dpkg` source package: `libxslt=1.1.43-0exp1`

Binary Packages:

- `libxslt1-dev:amd64=1.1.43-0exp1`
- `libxslt1.1:amd64=1.1.43-0exp1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/libxslt/1.1.43-0exp1/


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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/libyaml/0.2.5-2/


### `dpkg` source package: `libzstd=1.5.7+dfsg-1build1`

Binary Packages:

- `libzstd-dev:amd64=1.5.7+dfsg-1build1`
- `libzstd1:amd64=1.5.7+dfsg-1build1`

Licenses: (parsed from: `/usr/share/doc/libzstd-dev/copyright`, `/usr/share/doc/libzstd1/copyright`)

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

### `dpkg` source package: `linux=6.16.0-13.13`

Binary Packages:

- `linux-libc-dev:amd64=6.16.0-13.13`

Licenses: (parsed from: `/usr/share/doc/linux-libc-dev/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris linux=6.16.0-13.13
'http://archive.ubuntu.com/ubuntu/pool/main/l/linux/linux_6.16.0-13.13.dsc' linux_6.16.0-13.13.dsc 8485 SHA512:1bd5fd4d3dc3ef6ff1effadfa8446d927ccae6b3166aa41f4da6ee2277a759dbe2178cb32ab029e3a9f71bde2c2eff856c5e269db0d8ea27fb5f31077e6aa74a
'http://archive.ubuntu.com/ubuntu/pool/main/l/linux/linux_6.16.0.orig.tar.gz' linux_6.16.0.orig.tar.gz 247360331 SHA512:abc1360664e5cce86228f64e34f1363aec712a9ac8f84cb0ac75df25fd68cb3d8ba3160aa616e3a78efb3616106ab0df2be0a43e215eda934490191e9bcd9b2b
'http://archive.ubuntu.com/ubuntu/pool/main/l/linux/linux_6.16.0-13.13.diff.gz' linux_6.16.0-13.13.diff.gz 1344358 SHA512:c4654e0034767fb8c0ee26b40412ac3f5b5f98561799528b68652f2cc8b43dc1006287754a5325a5e7d9bca39f1cbc1aced0c188049b8aa2d906de7c8b7bca52
```

### `dpkg` source package: `lto-disabled-list=66`

Binary Packages:

- `lto-disabled-list=66`

Licenses: (parsed from: `/usr/share/doc/lto-disabled-list/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris lto-disabled-list=66
'http://archive.ubuntu.com/ubuntu/pool/main/l/lto-disabled-list/lto-disabled-list_66.dsc' lto-disabled-list_66.dsc 1441 SHA512:55c3aeb78f8833afba4a69582fff5d2b9442614b98712a0f0f33f09897413681859087aae9fc499f898edf917c2cb45c7418ab8a123e19e01d5ce619907ea9f7
'http://archive.ubuntu.com/ubuntu/pool/main/l/lto-disabled-list/lto-disabled-list_66.tar.xz' lto-disabled-list_66.tar.xz 14112 SHA512:bcdda3952c24cdca24ef91a505d3ac4e430e9351b998083f72c5babcb22a22de3a977e53f6c5824817115bf17752d4252098f40667f5358fd27182c8dcd123b8
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

### `dpkg` source package: `mysql-8.4=8.4.6-0ubuntu1`

Binary Packages:

- `libmysqlclient-dev=8.4.6-0ubuntu1`
- `libmysqlclient24:amd64=8.4.6-0ubuntu1`

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
$ apt-get source -qq --print-uris mysql-8.4=8.4.6-0ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/m/mysql-8.4/mysql-8.4_8.4.6-0ubuntu1.dsc' mysql-8.4_8.4.6-0ubuntu1.dsc 3768 SHA512:2fed917f226f5d5e61cb2848c7fa1ad1e54b922c376bee582d3e34748d1e0886849e3a295df27d42d172094db3b14e97273d1dfb8d8da92c545612a9a68798b1
'http://archive.ubuntu.com/ubuntu/pool/main/m/mysql-8.4/mysql-8.4_8.4.6.orig.tar.gz' mysql-8.4_8.4.6.orig.tar.gz 479211975 SHA512:2d498dc71eeede4368bd70fb1d1c012abd774732e341312f469afa3823c3b37489032b3290fa7531fb78c2b36251dbd1b8e1554c9330e18e56407f96fb8d4a1e
'http://archive.ubuntu.com/ubuntu/pool/main/m/mysql-8.4/mysql-8.4_8.4.6.orig.tar.gz.asc' mysql-8.4_8.4.6.orig.tar.gz.asc 833 SHA512:afcdbc55f74ad437f0811954c74edd9f203a527d35a6685407d13de8e0cadd511268064a92f3a05e7e05ecff0f81ba0341bab3a5897b5f6575af159626dd2e88
'http://archive.ubuntu.com/ubuntu/pool/main/m/mysql-8.4/mysql-8.4_8.4.6-0ubuntu1.debian.tar.xz' mysql-8.4_8.4.6-0ubuntu1.debian.tar.xz 134908 SHA512:c5434013285e5255571e0a2a2d29fc1cc5924cff766c576e9873f1bb2f2981a7b9fd5a1808df42c4f37fdc7f85b2177a902906ca530928ea7bf8dda04ddab38f
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

### `dpkg` source package: `openldap=2.6.9+dfsg-2ubuntu1`

Binary Packages:

- `libldap-common=2.6.9+dfsg-2ubuntu1`
- `libldap-dev:amd64=2.6.9+dfsg-2ubuntu1`
- `libldap2:amd64=2.6.9+dfsg-2ubuntu1`

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

Source:

```console
$ apt-get source -qq --print-uris openssh=1:10.0p1-5ubuntu3
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssh/openssh_10.0p1-5ubuntu3.dsc' openssh_10.0p1-5ubuntu3.dsc 3499 SHA512:774e4ac59f411ac290d55532ed3911adf185d943db7978c87c1af84494e37377b227ffbefa4c587b65f2d44112b2d7feb8bac0d7896515970e4fb1be0b2a8eac
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssh/openssh_10.0p1.orig.tar.gz' openssh_10.0p1.orig.tar.gz 1972675 SHA512:2daa1fcf95793b23810142077e68ddfabdf3732b207ef4f033a027f72d733d0e9bcdb6f757e7f3a5934b972de05bfaae3baae381cfc7a400cd8ab4d4e277a0ed
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssh/openssh_10.0p1.orig.tar.gz.asc' openssh_10.0p1.orig.tar.gz.asc 833 SHA512:6ab9deb4233ff159e55a18c9fc07d5ff8a41723dad74aa3d803e1476b585f5662aba34f8a7a1f5fe1d248f3ff3cd663f2c2fb8e399c6a4723b6215b0eb423d13
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssh/openssh_10.0p1-5ubuntu3.debian.tar.xz' openssh_10.0p1-5ubuntu3.debian.tar.xz 212856 SHA512:a3a48f59beed8d6f689bbb22bd5a17bf28db51be53067d2efd12cc04970d9fe0e392f18396d97b39ac0305713fb485be1a2731be217e14ee977285ae91c4e406
```

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

Source:

```console
$ apt-get source -qq --print-uris openssl=3.5.0-2ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssl/openssl_3.5.0-2ubuntu1.dsc' openssl_3.5.0-2ubuntu1.dsc 2426 SHA512:c98a0800a7ba381d46626f498d2459e50910215376f780194a0c990956aba8dfe083504b1930df00dcaead8eadcc79166502c8aab06b8e9b6832643cca2c49fd
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssl/openssl_3.5.0.orig.tar.gz' openssl_3.5.0.orig.tar.gz 53136912 SHA512:39cc80e2843a2ee30f3f5de25cd9d0f759ad8de71b0b39f5a679afaaa74f4eb58d285ae50e29e4a27b139b49343ac91d1f05478f96fb0c6b150f16d7b634676f
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssl/openssl_3.5.0-2ubuntu1.debian.tar.xz' openssl_3.5.0-2ubuntu1.debian.tar.xz 67920 SHA512:04f38405929f0cae06bbc231d0ab18d07561375873adae3454c775826fe84d973040a84dc4c84de1fbd677325acce8e1f0b7d6e2f0cc823b38190510d613428a
```

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

Source:

```console
$ apt-get source -qq --print-uris pam=1.7.0-5ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/p/pam/pam_1.7.0-5ubuntu1.dsc' pam_1.7.0-5ubuntu1.dsc 2945 SHA512:ccbc1f219bba59e048af7ecd7b3bd5be2c24247a0c22f7cef331b094045ed9bc62934773a7b9bc3afa54b89459789e9fb16727d15e570ce5b46b6d47fa47ac1f
'http://archive.ubuntu.com/ubuntu/pool/main/p/pam/pam_1.7.0.orig.tar.xz' pam_1.7.0.orig.tar.xz 507824 SHA512:ab5cadb0eb5e95e36146fdbbc77eef4e5e0f38aeee4e819b080a1316f69969c3c33e4a2daf3246ded4c2e58ce517d7f1acb0d8de02a4898ff753f4c3aeec51cf
'http://archive.ubuntu.com/ubuntu/pool/main/p/pam/pam_1.7.0.orig.tar.xz.asc' pam_1.7.0.orig.tar.xz.asc 801 SHA512:573bef1d63c0ce4efb5d1efd71a582f6ff679f2e278c326f66e142175cf67e42404453d41b92c5ce201b7d41db7b0617695f0d0972a812f0ab19553dec37192e
'http://archive.ubuntu.com/ubuntu/pool/main/p/pam/pam_1.7.0-5ubuntu1.debian.tar.xz' pam_1.7.0-5ubuntu1.debian.tar.xz 193972 SHA512:eb579be919a07e8d1821d9d754547e819bdd8020c62d9f560fdc7eca18e57e894ae3f7d2ffb52ab9d7212e6d41dca39bf461cec297fe284a196d5603585a637f
```

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

Source:

```console
$ apt-get source -qq --print-uris pango1.0=1.56.3-1
'http://archive.ubuntu.com/ubuntu/pool/main/p/pango1.0/pango1.0_1.56.3-1.dsc' pango1.0_1.56.3-1.dsc 3690 SHA512:156386e6be66670865b3d2fdcc8f11c5fad5a5ea3854ec5132cb7c0236040ee9a4fc2bd5c66937e8feb0dad5a8a2280f516d9f49e63f6db2e3b52654710b47d8
'http://archive.ubuntu.com/ubuntu/pool/main/p/pango1.0/pango1.0_1.56.3.orig.tar.xz' pango1.0_1.56.3.orig.tar.xz 1883584 SHA512:adb5aa66ea0c45f7bb112867a77f25d31d39bbb18fd8d41df0c1fd329714def874aa3cb8a49847561a75b0824c2abf8ce09a610d088e88d7de015c36a1536ac0
'http://archive.ubuntu.com/ubuntu/pool/main/p/pango1.0/pango1.0_1.56.3-1.debian.tar.xz' pango1.0_1.56.3-1.debian.tar.xz 43788 SHA512:3e65b9846014c38a12145fb3f45f3da6ab656965154459d58e5877bac2e38ebe997878c920ca1cbb39149b9123130a27a733ff0887e0c1a1f487e46252844a79
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
'http://archive.ubuntu.com/ubuntu/pool/main/p/patch/patch_2.8-2.dsc' patch_2.8-2.dsc 1689 SHA512:cf43a4b896395c4dfe05ae87636a18c47f34c4d149029c19ae2826f700254eb484f760ff41c793b7eb066e1b91e097d3dd2e40636f47a6efd6cbfa3df7f49565
'http://archive.ubuntu.com/ubuntu/pool/main/p/patch/patch_2.8.orig.tar.xz' patch_2.8.orig.tar.xz 907208 SHA512:d689d696660a662753e8660792733c3be0a94c76abfe7a28b0f9f70300c3a42d6437d081553a59bfde6e1b0d5ee13ed89be48d0b00b6da2cadbfc14a15ada603
'http://archive.ubuntu.com/ubuntu/pool/main/p/patch/patch_2.8-2.debian.tar.xz' patch_2.8-2.debian.tar.xz 9460 SHA512:3881b0cbd510932ee06ecb5ba85786d44f1ea7336ad8bd1ebd23d0e0ff1db2c589111781a9565388296b46985303d5c4102953b12a9d0035500e4554d0ed8bcd
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
'http://archive.ubuntu.com/ubuntu/pool/main/p/pcre2/pcre2_10.45-1.dsc' pcre2_10.45-1.dsc 2337 SHA512:97973e68d44bc30766050038affbf71d06130d62971d050d6b09d2af1bfe9b8072ebc00c7275c3d1ff6963716b2d5cd0358135ccf73ecb34fbd3b76cea922c05
'http://archive.ubuntu.com/ubuntu/pool/main/p/pcre2/pcre2_10.45.orig.tar.gz' pcre2_10.45.orig.tar.gz 2715958 SHA512:6ec01a05ce65be61e5974dcc2ccd2e2b5c6db183e3a592530205c7d3259b730df3a9ab999d204f3c52e5a14ae88f32f94306b4501eb9629568ce6158985e2fa6
'http://archive.ubuntu.com/ubuntu/pool/main/p/pcre2/pcre2_10.45-1.diff.gz' pcre2_10.45-1.diff.gz 8659 SHA512:2c7444846c31495693f5b94357a9f94b3ccb1664ee9eff68433fc4d0e94dbbf32eb24611718daf8338466283d450bfab547946aabae990803c61efeb091b7964
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

Source:

```console
$ apt-get source -qq --print-uris perl=5.40.1-6
'http://archive.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.40.1-6.dsc' perl_5.40.1-6.dsc 2372 SHA512:fe93e98e727db27f8c144f7a1579c8865cfdca2adb72f2e1b067632a6afe248b02e65ade086dd9dec815ac4f35783129563293920be9ee23ce198f132ccfd0d5
'http://archive.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.40.1.orig-regen-configure.tar.xz' perl_5.40.1.orig-regen-configure.tar.xz 421056 SHA512:933261779f476b0edda581270949c92e8e7dbe4bcaf1417398e708a321cdb748fe329acb703b2e74446cdfb03c20cefcab1eb972b852418ed3ea9b870db1fa86
'http://archive.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.40.1.orig.tar.xz' perl_5.40.1.orig.tar.xz 13930924 SHA512:3ff16b3462ce43ff38dab21b3dfc20f81772b8c9eac19ab96ba2d5e6cbb390e2302fa76c4879f915249357cd11c7ec0d548bcbf3ab2c156df1b9fca95da3f545
'http://archive.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.40.1-6.debian.tar.xz' perl_5.40.1-6.debian.tar.xz 172892 SHA512:30e13c93387f78c6d077fa154f2a646b17f0912dd0236b4424faa01ea3eedbcc7be309adaf4b8794b91a0abc586ecd3466164fd88977bb3196050ee70122b7ed
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

### `dpkg` source package: `postgresql-17=17.5-1build1`

Binary Packages:

- `libpq-dev=17.5-1build1`
- `libpq5:amd64=17.5-1build1`

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
$ apt-get source -qq --print-uris postgresql-17=17.5-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/p/postgresql-17/postgresql-17_17.5-1build1.dsc' postgresql-17_17.5-1build1.dsc 4269 SHA512:bc53637eeaaad879c3a3818203137626e7fe9ea00a3682b1810b15c04e31adbcf0f414a4d72b73e1fce7f17e76ac7a2d42ba9ff70ccfcf5d502236d6d4801c62
'http://archive.ubuntu.com/ubuntu/pool/main/p/postgresql-17/postgresql-17_17.5.orig.tar.bz2' postgresql-17_17.5.orig.tar.bz2 21595174 SHA512:deae865e6c8e2ef5bb622288f790c5b83d22235496513e60351354970ff193eb885fb632c2d1321b8311c88c05b76a370d8d838473936c8438dbb569086b139f
'http://archive.ubuntu.com/ubuntu/pool/main/p/postgresql-17/postgresql-17_17.5-1build1.debian.tar.xz' postgresql-17_17.5-1build1.debian.tar.xz 27680 SHA512:94d3f4e53f00f822e5bc890372db4df0ed7c47f873ba645c2a24908286102e688ffa2071b588529ec5d6faf9b679c358eecdcc862e1b9728fab1a53f28c43b19
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

Source:

```console
$ apt-get source -qq --print-uris procps=2:4.0.4-8ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/p/procps/procps_4.0.4-8ubuntu2.dsc' procps_4.0.4-8ubuntu2.dsc 2247 SHA512:f0a7514f32a9761ea987b324a78b6dfb1a951b73cd4a23c97868e7f5b1484d88cac1cee7f99e6365dfaa4f506e984b444c0e3e378fe9a5938a0f2440c5d5338c
'http://archive.ubuntu.com/ubuntu/pool/main/p/procps/procps_4.0.4.orig.tar.xz' procps_4.0.4.orig.tar.xz 1401540 SHA512:94375544e2422fefc23d7634063c49ef1be62394c46039444f85e6d2e87e45cfadc33accba5ca43c96897b4295bfb0f88d55a30204598ddb26ef66f0420cefb4
'http://archive.ubuntu.com/ubuntu/pool/main/p/procps/procps_4.0.4-8ubuntu2.debian.tar.xz' procps_4.0.4-8ubuntu2.debian.tar.xz 53800 SHA512:5a022b4c32a2c6543fa72e33e3474d995c9deaa629443c831fca5847ee5b71d6026108154ec9a3765acd47e98e21c7ef01df9da28c0b624976add2758e903a83
```

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

### `dpkg` source package: `python3-defaults=3.13.5-1`

Binary Packages:

- `libpython3-stdlib:amd64=3.13.5-1`
- `python3=3.13.5-1`
- `python3-minimal=3.13.5-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris python3-defaults=3.13.5-1
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3-defaults/python3-defaults_3.13.5-1.dsc' python3-defaults_3.13.5-1.dsc 2346 SHA512:e00c42b2e1bda3c12caeb7e0bfef033fc5981801c7d04f93118e7af4d8f6864428aa5bd60c6f9f846399756b10773acdcc053c8136bc38394f2c262a7d4552b0
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3-defaults/python3-defaults_3.13.5-1.tar.gz' python3-defaults_3.13.5-1.tar.gz 146839 SHA512:93ee55c9bc404797ed5e2910a6af909f59fce277f16ac532c7da968172912310181593252505ce00c360de28a4c5e0ab46a071996fe72631cfe59124c4ab2031
```

### `dpkg` source package: `python3.13=3.13.5-2`

Binary Packages:

- `libpython3.13-minimal:amd64=3.13.5-2`
- `libpython3.13-stdlib:amd64=3.13.5-2`
- `python3.13=3.13.5-2`
- `python3.13-minimal=3.13.5-2`

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

- http://snapshot.debian.org/package/python3.13/3.13.5-2/


### `dpkg` source package: `readline=8.3-1`

Binary Packages:

- `libreadline-dev:amd64=8.3-1`
- `libreadline8t64:amd64=8.3-1`
- `readline-common=8.3-1`

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
$ apt-get source -qq --print-uris readline=8.3-1
'http://archive.ubuntu.com/ubuntu/pool/main/r/readline/readline_8.3-1.dsc' readline_8.3-1.dsc 2817 SHA512:f5fca4244cb1809000664f3d8bf2519406bbe69d690fa933026adc07eef3904012600a2be060688024532f7b1c7ad0757342dfc694313a14a6c7e372050192ee
'http://archive.ubuntu.com/ubuntu/pool/main/r/readline/readline_8.3.orig.tar.gz' readline_8.3.orig.tar.gz 3419642 SHA512:513002753dcf5db9213dbbb61d51217245f6a40d33b1dd45238e8062dfa8eef0c890b87a5548e11db959e842724fb572c4d3d7fb433773762a63c30efe808344
'http://archive.ubuntu.com/ubuntu/pool/main/r/readline/readline_8.3-1.debian.tar.xz' readline_8.3-1.debian.tar.xz 33652 SHA512:26e48c406faddd88a65278f03a39061953aa319f1a1c846036254e42dc156b644f509006d1313b61c00c40e5749bc4028e554ed8f65810d4c018d5869292bb26
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


### `dpkg` source package: `shadow=1:4.17.4-2ubuntu1`

Binary Packages:

- `login.defs=1:4.17.4-2ubuntu1`
- `passwd=1:4.17.4-2ubuntu1`

Licenses: (parsed from: `/usr/share/doc/login.defs/copyright`, `/usr/share/doc/passwd/copyright`)

- `BSD-3-clause`
- `GPL-1`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris shadow=1:4.17.4-2ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/s/shadow/shadow_4.17.4-2ubuntu1.dsc' shadow_4.17.4-2ubuntu1.dsc 2817 SHA512:908a0ce0a95ac050118375bcf786ca7bb043c97c4d3f574ce521b2ef921255704779ab20a936c52dd95f586cd28a8d8340669d663e0ee8fa87c3e63af2889e4d
'http://archive.ubuntu.com/ubuntu/pool/main/s/shadow/shadow_4.17.4.orig.tar.xz' shadow_4.17.4.orig.tar.xz 2326584 SHA512:06830f654650312a79ccd6d729a51808b324d594abf1c05d56a2d0880936df292ec5c9fd6c7f4ad59a6d0f2bf5be0af42afe6386c24c2c087fd64fff301bade3
'http://archive.ubuntu.com/ubuntu/pool/main/s/shadow/shadow_4.17.4.orig.tar.xz.asc' shadow_4.17.4.orig.tar.xz.asc 488 SHA512:24f14397a975e4b09be087705a96544ff8ad76e0aa8c708ed4a53db3a295ad0a33fd0797fc570dcbb2446d4e103a3e43922a93168f65012eba5d3fe31549ebdd
'http://archive.ubuntu.com/ubuntu/pool/main/s/shadow/shadow_4.17.4-2ubuntu1.debian.tar.xz' shadow_4.17.4-2ubuntu1.debian.tar.xz 181584 SHA512:59fcf740cc018da0e6d0fc92c33b3629264ff64a598424856b1e5f5c38cab51d128c9235da13d7303bc960049de1d0b2a1bf3ca34d4c4bef73af094198180627
```

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

### `dpkg` source package: `sqlite3=3.46.1-6ubuntu1`

Binary Packages:

- `libsqlite3-0:amd64=3.46.1-6ubuntu1`
- `libsqlite3-dev:amd64=3.46.1-6ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libsqlite3-0/copyright`, `/usr/share/doc/libsqlite3-dev/copyright`)

- `GPL-2`
- `GPL-2+`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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

### `dpkg` source package: `systemd=257.7-1ubuntu1`

Binary Packages:

- `libsystemd0:amd64=257.7-1ubuntu1`
- `libudev1:amd64=257.7-1ubuntu1`

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

### `dpkg` source package: `tiff=4.7.0-3ubuntu1`

Binary Packages:

- `libtiff-dev:amd64=4.7.0-3ubuntu1`
- `libtiff6:amd64=4.7.0-3ubuntu1`
- `libtiffxx6:amd64=4.7.0-3ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libtiff-dev/copyright`, `/usr/share/doc/libtiff6/copyright`, `/usr/share/doc/libtiffxx6/copyright`)

- `Hylafax`

Source:

```console
$ apt-get source -qq --print-uris tiff=4.7.0-3ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/t/tiff/tiff_4.7.0-3ubuntu1.dsc' tiff_4.7.0-3ubuntu1.dsc 2368 SHA512:20e569ac16dc7a043dd000fbb0dd10afdd0dfb436e362663ec0c592514fd0e8362ba5f5b11abcc3d7ae063d30715f0bec63ac7ffbc1dd335d1658b522cee7912
'http://archive.ubuntu.com/ubuntu/pool/main/t/tiff/tiff_4.7.0.orig.tar.bz2' tiff_4.7.0.orig.tar.bz2 2111254 SHA512:6d6f39727a4403ffaae390d54f1d7a6ff926085480422cbc4e2168e8e6490bf283e69361860d0ca0d7951543f48be550641b76d814c24a1b4e4bff1da9e27c6d
'http://archive.ubuntu.com/ubuntu/pool/main/t/tiff/tiff_4.7.0-3ubuntu1.debian.tar.xz' tiff_4.7.0-3ubuntu1.debian.tar.xz 24196 SHA512:f9b88223c96b3b8a92d56b2162cc6131b9656fa74c4ceb266b9cc1b9d8bfaea9b9a7d5c325640354b5c8294d422c485dee04d5787836eaa0a7df63fab375934b
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

Source:

```console
$ apt-get source -qq --print-uris unbound=1.22.0-2ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/u/unbound/unbound_1.22.0-2ubuntu1.dsc' unbound_1.22.0-2ubuntu1.dsc 3284 SHA512:0e0df41943dc86ae738bcfcef9e983b62cc9f0147321f9ab4e52bc5b2504bb506eb42e95f24dfc0bcadda895d3bc78c60fce63cd11e23abe74b842ac3bf6d7ec
'http://archive.ubuntu.com/ubuntu/pool/main/u/unbound/unbound_1.22.0.orig.tar.gz' unbound_1.22.0.orig.tar.gz 6682466 SHA512:6c873e19902ce6cd59cec7084d5dba1a5bd5fe4437c827ae69bdf9273bcd8d2d1ec0dc183076f8d2e1fd38730bf8c10852d678399f0b2ea8ccf7e39119568978
'http://archive.ubuntu.com/ubuntu/pool/main/u/unbound/unbound_1.22.0.orig.tar.gz.asc' unbound_1.22.0.orig.tar.gz.asc 833 SHA512:afbf5a125f104a25576b1c416b32f68d715b41a025fc3a61e6ee3bc28f9988b4277c7f0dd188c51cbe5641f51ade20f740ea131d1a7b5db38e2d1462a9edbb69
'http://archive.ubuntu.com/ubuntu/pool/main/u/unbound/unbound_1.22.0-2ubuntu1.debian.tar.xz' unbound_1.22.0-2ubuntu1.debian.tar.xz 32444 SHA512:e84ccbbde0e51b5ba9932b9b80ecfccbd6a5f313ff5a8609148510ba4deba7272b9260cb51d25adf214573634c787b198340b9cd49d722795cecd935538d8ff8
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

Source:

```console
$ apt-get source -qq --print-uris util-linux=2.41-4ubuntu3
'http://archive.ubuntu.com/ubuntu/pool/main/u/util-linux/util-linux_2.41-4ubuntu3.dsc' util-linux_2.41-4ubuntu3.dsc 5049 SHA512:dda2e0fe664a32164f0e07bb966eeb918cf0dda6eae7e811af08e07f43167ae97d08e9466be590fdf50dc454480e26f09012740947d2130449bbd4687ae7a7d6
'http://archive.ubuntu.com/ubuntu/pool/main/u/util-linux/util-linux_2.41.orig.tar.xz' util-linux_2.41.orig.tar.xz 9535724 SHA512:800ff92ee7a047732c0accb9dd759d6ed659947373ca72e0dd3ca601d0a6fed9db92c0838cfaff6bcdb8c08bdc1ffa675721893f42945885c57ccd59ab676318
'http://archive.ubuntu.com/ubuntu/pool/main/u/util-linux/util-linux_2.41-4ubuntu3.debian.tar.xz' util-linux_2.41-4ubuntu3.debian.tar.xz 127096 SHA512:6579c7027db5759a3deeb3693a6173d9b6e09f1baa3ce98b6b4431a9c3350fcdf9733eb196db2e6635b773ccde41025eca0abeb52231f56fb3c96c1db36eb649
```

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


Source:

```console
$ apt-get source -qq --print-uris xtrans=1.4.0-1
'http://archive.ubuntu.com/ubuntu/pool/main/x/xtrans/xtrans_1.4.0-1.dsc' xtrans_1.4.0-1.dsc 1919 SHA512:ac171ce0f00e1741e97a4ddad630ccff69070c0ef60047071b3f940fad08cb468d5ded7b2d4f0f500aeda73f2b703d55a7a4bbe0d5fff88cc3381486a111f580
'http://archive.ubuntu.com/ubuntu/pool/main/x/xtrans/xtrans_1.4.0.orig.tar.gz' xtrans_1.4.0.orig.tar.gz 225941 SHA512:21287ccf18fe2ebd458765496b026d175bf47c6e8e5c21d5b9ea17203967efc0cf6928fa2f3385d289a680c7002c3640e4731937029e99933c2a64bb9fab5326
'http://archive.ubuntu.com/ubuntu/pool/main/x/xtrans/xtrans_1.4.0-1.diff.gz' xtrans_1.4.0-1.diff.gz 9522 SHA512:d6deaa9579fb61e6ffd296ffe6b083eb9de572001c0a5bc82229ecc3d50bf2ee2f6504b3daa533bd34f3d647d6bd2235728084ec0b59869f6446652b998797f7
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
