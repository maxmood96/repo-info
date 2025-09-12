# `buildpack-deps:questing-curl`

## Docker Metadata

- Image ID: `sha256:a697fed1cc9f24d6bcc5de4f7bf723b8c1383a692979ff7d02b9442ae8c05ed4`
- Created: `2025-05-19T22:25:54Z`
- Virtual Size: ~ 124.86 Mb  
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

Source:

```console
$ apt-get source -qq --print-uris apt=3.1.5ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/a/apt/apt_3.1.5ubuntu1.dsc' apt_3.1.5ubuntu1.dsc 3206 SHA512:5a9df7531b7741671c1e01007f189f5f72e5825aa5c2eef857d86dbd5f5e95a30e3d37e1484947ba2b9dc34e07e92a8f9144a441e9311e59a4de2fef2693b5fa
'http://archive.ubuntu.com/ubuntu/pool/main/a/apt/apt_3.1.5ubuntu1.tar.xz' apt_3.1.5ubuntu1.tar.xz 2431636 SHA512:851a05dc03aadbe790bc0670be1ebf12528dde32ccaa8b2fda26841036df4bc450168b9d10796fc273d0f438237453b9952f5d7d79a082aa2f35579e07306224
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

Source:

```console
$ apt-get source -qq --print-uris audit=1:4.0.5-1
'http://archive.ubuntu.com/ubuntu/pool/main/a/audit/audit_4.0.5-1.dsc' audit_4.0.5-1.dsc 2405 SHA512:3c0f9a4d0efcd8a31a2f4eae4e84fbe42198d258f184997638736427e801fc08c88dada63e6c88eea0f99524e4bc3f6b2bf55095e76b03231943fefa114b8f47
'http://archive.ubuntu.com/ubuntu/pool/main/a/audit/audit_4.0.5.orig.tar.gz' audit_4.0.5.orig.tar.gz 622404 SHA512:14fa19922cf6436284e1448d5a0e069ce5066d2d49d28679fe3ad019be60c133aee6e345b36e0f482ea1fdeadad7d78676f931aab1c25b91a2d0b445dce3eedf
'http://archive.ubuntu.com/ubuntu/pool/main/a/audit/audit_4.0.5-1.debian.tar.xz' audit_4.0.5-1.debian.tar.xz 19844 SHA512:7f91a8b9ddc92ec4404b5e3e1f9720d283418acefd91213a0935ffb49a599a2927e443350c7731db845885a8173e12c77efef08fea5e677748c8afdb61c54f5e
```

### `dpkg` source package: `base-files=14ubuntu1`

Binary Packages:

- `base-files=14ubuntu1`

Licenses: (parsed from: `/usr/share/doc/base-files/copyright`)

- `GPL`
- `GPL-2+`
- `verbatim`

Source:

```console
$ apt-get source -qq --print-uris base-files=14ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/b/base-files/base-files_14ubuntu1.dsc' base-files_14ubuntu1.dsc 1479 SHA512:d33a20092d6f51207f7b4ffffe1986a54ffa2f4fd353a07797372c8fd97fdb49d46f754eb04833f5a70f831b6ab1c429c92727345189b670c35a58839e917c74
'http://archive.ubuntu.com/ubuntu/pool/main/b/base-files/base-files_14ubuntu1.tar.xz' base-files_14ubuntu1.tar.xz 96740 SHA512:da673abde0693651fdcdf63695304871d7aaf07484dd6e1844508e0ae2be2cad082de6d48c3fdd507345a8412c200bc4278690e647496c3c482ba643d7475a7d
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
- `libcurl4t64:amd64=8.14.1-1ubuntu2`

Licenses: (parsed from: `/usr/share/doc/curl/copyright`, `/usr/share/doc/libcurl4t64/copyright`)

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

Source:

```console
$ apt-get source -qq --print-uris glibc=2.42-0ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.42-0ubuntu1.dsc' glibc_2.42-0ubuntu1.dsc 7889 SHA512:b49a8ab428dec1ae894cee117763dfad419ceb34b1c0036382f6c3c748707779a075dcadc3f571b622d1659ede75b0818d3536ed8619786b3c83d22220f8caed
'http://archive.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.42.orig.tar.xz' glibc_2.42.orig.tar.xz 19930508 SHA512:73a617db8e0f0958c0575f7a1c5a35b72b7e070b6cbdd02a9bb134995ca7ca0909f1e50d7362c53d2572d72f1879bb201a61d5275bac16136895d9a34ef0c068
'http://archive.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.42.orig.tar.xz.asc' glibc_2.42.orig.tar.xz.asc 981 SHA512:d868220778e98d24aead10a585e6a903892e4d043cd96a404634c8aa03d001d624a46a5c0fe13c86f83f66396a1f360a10990966fe377e98a722914b5087575d
'http://archive.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.42-0ubuntu1.debian.tar.xz' glibc_2.42-0ubuntu1.debian.tar.xz 442528 SHA512:2a9b3d4d1f2239e04388d59a43fb5b5f7c252a0d34215ff782ef0c401949958f50aa11202b93915c787d279e6580d2a154fe95fa9430091af5570f1060e9c67c
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

Source:

```console
$ apt-get source -qq --print-uris pam=1.7.0-5ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/p/pam/pam_1.7.0-5ubuntu1.dsc' pam_1.7.0-5ubuntu1.dsc 2945 SHA512:ccbc1f219bba59e048af7ecd7b3bd5be2c24247a0c22f7cef331b094045ed9bc62934773a7b9bc3afa54b89459789e9fb16727d15e570ce5b46b6d47fa47ac1f
'http://archive.ubuntu.com/ubuntu/pool/main/p/pam/pam_1.7.0.orig.tar.xz' pam_1.7.0.orig.tar.xz 507824 SHA512:ab5cadb0eb5e95e36146fdbbc77eef4e5e0f38aeee4e819b080a1316f69969c3c33e4a2daf3246ded4c2e58ce517d7f1acb0d8de02a4898ff753f4c3aeec51cf
'http://archive.ubuntu.com/ubuntu/pool/main/p/pam/pam_1.7.0.orig.tar.xz.asc' pam_1.7.0.orig.tar.xz.asc 801 SHA512:573bef1d63c0ce4efb5d1efd71a582f6ff679f2e278c326f66e142175cf67e42404453d41b92c5ce201b7d41db7b0617695f0d0972a812f0ab19553dec37192e
'http://archive.ubuntu.com/ubuntu/pool/main/p/pam/pam_1.7.0-5ubuntu1.debian.tar.xz' pam_1.7.0-5ubuntu1.debian.tar.xz 193972 SHA512:eb579be919a07e8d1821d9d754547e819bdd8020c62d9f560fdc7eca18e57e894ae3f7d2ffb52ab9d7212e6d41dca39bf461cec297fe284a196d5603585a637f
```

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

Source:

```console
$ apt-get source -qq --print-uris procps=2:4.0.4-8ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/p/procps/procps_4.0.4-8ubuntu2.dsc' procps_4.0.4-8ubuntu2.dsc 2247 SHA512:f0a7514f32a9761ea987b324a78b6dfb1a951b73cd4a23c97868e7f5b1484d88cac1cee7f99e6365dfaa4f506e984b444c0e3e378fe9a5938a0f2440c5d5338c
'http://archive.ubuntu.com/ubuntu/pool/main/p/procps/procps_4.0.4.orig.tar.xz' procps_4.0.4.orig.tar.xz 1401540 SHA512:94375544e2422fefc23d7634063c49ef1be62394c46039444f85e6d2e87e45cfadc33accba5ca43c96897b4295bfb0f88d55a30204598ddb26ef66f0420cefb4
'http://archive.ubuntu.com/ubuntu/pool/main/p/procps/procps_4.0.4-8ubuntu2.debian.tar.xz' procps_4.0.4-8ubuntu2.debian.tar.xz 53800 SHA512:5a022b4c32a2c6543fa72e33e3474d995c9deaa629443c831fca5847ee5b71d6026108154ec9a3765acd47e98e21c7ef01df9da28c0b624976add2758e903a83
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

Source:

```console
$ apt-get source -qq --print-uris systemd=257.8-0ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/s/systemd/systemd_257.8-0ubuntu2.dsc' systemd_257.8-0ubuntu2.dsc 8466 SHA512:4957ec2140c375d2cd77ff1d20b5f52a71f3a7e9a2478672b9963ff78e7e6e2e79639d651b4c8b7cf04cd2b3e1f78bbf6d314abc9ff1d67b42bfc09dcbddf3b2
'http://archive.ubuntu.com/ubuntu/pool/main/s/systemd/systemd_257.8.orig.tar.gz' systemd_257.8.orig.tar.gz 16385060 SHA512:30331df5eb7a1556da8c017a0e6c07b8b99f0cb31da055c1b86c9b9e6fd7074f7c6746efa3e69711b73af48a15d61a84f35ad6e554d32a23441ba910398f7f65
'http://archive.ubuntu.com/ubuntu/pool/main/s/systemd/systemd_257.8-0ubuntu2.debian.tar.xz' systemd_257.8-0ubuntu2.debian.tar.xz 247892 SHA512:9e00de94c8b988f420cd295e9dec5684d0e920d36c574fa5a99336e26c2140c757f5d0e7d1c56199144e11debf0c617245f1904ceb29762dfe80c12a67d5addc
```

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

