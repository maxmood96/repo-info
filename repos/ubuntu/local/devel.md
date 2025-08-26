# `ubuntu:25.10`

## Docker Metadata

- Image ID: `sha256:c87762258ae22819f3e3ee204b4849ae3c15ffe5e307a15ff96bac235a7cf3fa`
- Created: `2025-08-06T07:01:58.158040403Z`
- Virtual Size: ~ 77.08 Mb  
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

### `dpkg` source package: `dpkg=1.22.21ubuntu1`

Binary Packages:

- `dpkg=1.22.21ubuntu1`

Licenses: (parsed from: `/usr/share/doc/dpkg/copyright`)

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

Source:

```console
$ apt-get source -qq --print-uris e2fsprogs=1.47.2-3ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/e/e2fsprogs/e2fsprogs_1.47.2-3ubuntu1.dsc' e2fsprogs_1.47.2-3ubuntu1.dsc 3292 SHA512:f22372ce4d6f16d1edfd4e6e268cb4ecce5b161a10773da4e726bae40f88dab34c243b28c6e53741db2b2aed2fd130b0513ff7277d1a2359984c43f6982e4b33
'http://archive.ubuntu.com/ubuntu/pool/main/e/e2fsprogs/e2fsprogs_1.47.2.orig.tar.gz' e2fsprogs_1.47.2.orig.tar.gz 9996725 SHA512:dd89139c5e2bf999a22d999686ef06ab42f6ad537c6aeaa3fe68d9734d734b7396fd7ab2fd8002be26860c5653991a666d0df06c804c2f1f07f1274468ec728f
'http://archive.ubuntu.com/ubuntu/pool/main/e/e2fsprogs/e2fsprogs_1.47.2.orig.tar.gz.asc' e2fsprogs_1.47.2.orig.tar.gz.asc 488 SHA512:a22d46cc37497861d5a7e50076b40b8be6f459790f6eaacf0446200776fb74492ca9bfc7abc19edda3c9f7f722c318827b02f9cfbbb2118a8e86bce4d446d56b
'http://archive.ubuntu.com/ubuntu/pool/main/e/e2fsprogs/e2fsprogs_1.47.2-3ubuntu1.debian.tar.xz' e2fsprogs_1.47.2-3ubuntu1.debian.tar.xz 105592 SHA512:f174a673d390f03e1d96fec49560c7d72463c135541107e868eb0b3d222366104dea976b330d155faaf626973d4d0cb68b5df853dc96789cdb0da049b47b75c9
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

### `dpkg` source package: `gcc-15=15.1.0-10ubuntu2`

Binary Packages:

- `gcc-15-base:amd64=15.1.0-10ubuntu2`
- `libgcc-s1:amd64=15.1.0-10ubuntu2`
- `libstdc++6:amd64=15.1.0-10ubuntu2`

Licenses: (parsed from: `/usr/share/doc/gcc-15-base/copyright`, `/usr/share/doc/libgcc-s1/copyright`, `/usr/share/doc/libstdc++6/copyright`)

- `Apache-2.0`
- `Artistic`
- `GFDL-1.2`
- `GPL`
- `GPL-3`
- `LGPL`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `glibc=2.41-9ubuntu1`

Binary Packages:

- `libc-bin=2.41-9ubuntu1`
- `libc6:amd64=2.41-9ubuntu1`

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

Source:

```console
$ apt-get source -qq --print-uris gmp=2:6.3.0+dfsg-3ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/g/gmp/gmp_6.3.0%2bdfsg-3ubuntu2.dsc' gmp_6.3.0+dfsg-3ubuntu2.dsc 2337 SHA512:e6c5be8da178f008fc856d593ad5aa06be9b604075559ba1e7e231da7b5d0a8ca3390b25a3ab9388c860462fa49e0d58c2e8c713642927457f865e5caa378696
'http://archive.ubuntu.com/ubuntu/pool/main/g/gmp/gmp_6.3.0%2bdfsg.orig.tar.xz' gmp_6.3.0+dfsg.orig.tar.xz 1870556 SHA512:a422b29024464aeb26c69f64be1bc37407d74e0290f44f67fc040fe38b97f3eb7aa6ba8380722ef36cac39816d1c4f24b771159fb86d5979ef0791dcdef708bc
'http://archive.ubuntu.com/ubuntu/pool/main/g/gmp/gmp_6.3.0%2bdfsg-3ubuntu2.debian.tar.xz' gmp_6.3.0+dfsg-3ubuntu2.debian.tar.xz 39724 SHA512:553121b4a70c4a8b46481ae156796354baebc1150e32dd4f4c32695b37b019fec0ac80a4fdae607cce7ab3fb83f83c37aac66ab04cb314e835012bd83c845d51
```

### `dpkg` source package: `gnupg2=2.4.7-17ubuntu3`

Binary Packages:

- `gpgv=2.4.7-17ubuntu3`

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

### `dpkg` source package: `openssl=3.5.0-2ubuntu1`

Binary Packages:

- `libssl3t64:amd64=3.5.0-2ubuntu1`
- `openssl-provider-legacy=3.5.0-2ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libssl3t64/copyright`, `/usr/share/doc/openssl-provider-legacy/copyright`)

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

### `dpkg` source package: `perl=5.40.1-6`

Binary Packages:

- `perl-base=5.40.1-6`

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

Source:

```console
$ apt-get source -qq --print-uris perl=5.40.1-6
'http://archive.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.40.1-6.dsc' perl_5.40.1-6.dsc 2372 SHA512:fe93e98e727db27f8c144f7a1579c8865cfdca2adb72f2e1b067632a6afe248b02e65ade086dd9dec815ac4f35783129563293920be9ee23ce198f132ccfd0d5
'http://archive.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.40.1.orig-regen-configure.tar.xz' perl_5.40.1.orig-regen-configure.tar.xz 421056 SHA512:933261779f476b0edda581270949c92e8e7dbe4bcaf1417398e708a321cdb748fe329acb703b2e74446cdfb03c20cefcab1eb972b852418ed3ea9b870db1fa86
'http://archive.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.40.1.orig.tar.xz' perl_5.40.1.orig.tar.xz 13930924 SHA512:3ff16b3462ce43ff38dab21b3dfc20f81772b8c9eac19ab96ba2d5e6cbb390e2302fa76c4879f915249357cd11c7ec0d548bcbf3ab2c156df1b9fca95da3f545
'http://archive.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.40.1-6.debian.tar.xz' perl_5.40.1-6.debian.tar.xz 172892 SHA512:30e13c93387f78c6d077fa154f2a646b17f0912dd0236b4424faa01ea3eedbcc7be309adaf4b8794b91a0abc586ecd3466164fd88977bb3196050ee70122b7ed
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

### `dpkg` source package: `sqlite3=3.46.1-6ubuntu1`

Binary Packages:

- `libsqlite3-0:amd64=3.46.1-6ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libsqlite3-0/copyright`)

- `GPL-2`
- `GPL-2+`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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

Source:

```console
$ apt-get source -qq --print-uris util-linux=2.41-4ubuntu3
'http://archive.ubuntu.com/ubuntu/pool/main/u/util-linux/util-linux_2.41-4ubuntu3.dsc' util-linux_2.41-4ubuntu3.dsc 5049 SHA512:dda2e0fe664a32164f0e07bb966eeb918cf0dda6eae7e811af08e07f43167ae97d08e9466be590fdf50dc454480e26f09012740947d2130449bbd4687ae7a7d6
'http://archive.ubuntu.com/ubuntu/pool/main/u/util-linux/util-linux_2.41.orig.tar.xz' util-linux_2.41.orig.tar.xz 9535724 SHA512:800ff92ee7a047732c0accb9dd759d6ed659947373ca72e0dd3ca601d0a6fed9db92c0838cfaff6bcdb8c08bdc1ffa675721893f42945885c57ccd59ab676318
'http://archive.ubuntu.com/ubuntu/pool/main/u/util-linux/util-linux_2.41-4ubuntu3.debian.tar.xz' util-linux_2.41-4ubuntu3.debian.tar.xz 127096 SHA512:6579c7027db5759a3deeb3693a6173d9b6e09f1baa3ce98b6b4431a9c3350fcdf9733eb196db2e6635b773ccde41025eca0abeb52231f56fb3c96c1db36eb649
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
