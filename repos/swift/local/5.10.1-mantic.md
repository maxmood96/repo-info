# `swift:5.10.1-mantic`

## Docker Metadata

- Image ID: `sha256:32355396f7b449e2f54aa6dececb17505e6b75fb3a748a118998dc95d0ff9ed2`
- Created: `2024-06-07T03:59:58.84992994Z`
- Virtual Size: ~ 3.01 Gb  
  (total size of all layers on-disk)
- Arch: `linux`/`amd64`
- Command: `["/bin/bash"]`
- Environment:
  - `PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin`
  - `SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561`
  - `SWIFT_PLATFORM=ubuntu23.10`
  - `SWIFT_BRANCH=swift-5.10.1-release`
  - `SWIFT_VERSION=swift-5.10.1-RELEASE`
  - `SWIFT_WEBROOT=https://download.swift.org`
- Labels:
  - `description=Docker Container for the Swift programming language`
  - `maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>`
  - `org.opencontainers.image.ref.name=ubuntu`
  - `org.opencontainers.image.version=23.10`

## `dpkg` (`.deb`-based packages)

### `dpkg` source package: `acl=2.3.1-3`

Binary Packages:

- `libacl1:amd64=2.3.1-3`

Licenses: (parsed from: `/usr/share/doc/libacl1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2+`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris acl=2.3.1-3
'http://archive.ubuntu.com/ubuntu/pool/main/a/acl/acl_2.3.1-3.dsc' acl_2.3.1-3.dsc 2508 SHA512:4162efc9071c57eeced2c4faa9b13c8f46dac98d7876db14c7bc37ec526c02f2a2aced5b828f594bfa101d37a594573e865b856a96538a524df66b715082e15c
'http://archive.ubuntu.com/ubuntu/pool/main/a/acl/acl_2.3.1.orig.tar.xz' acl_2.3.1.orig.tar.xz 355676 SHA512:7d02f05d17305f8587ab485395b00c7fdb8e44c1906d0d04b70a43a3020803e8b2b8c707abb6147f794867dfa87bd51769c2d3e11a3db55ecbd2006a6e6231dc
'http://archive.ubuntu.com/ubuntu/pool/main/a/acl/acl_2.3.1.orig.tar.xz.asc' acl_2.3.1.orig.tar.xz.asc 833 SHA512:be046f3bf1ac7e21d2a07bf6ea87c1fedeed2f9d370d8bf3de1aa0c448de5484b1523697415849b6b7ca23e48e3df5353f6aebe850eb20fc2044d2681c71f298
'http://archive.ubuntu.com/ubuntu/pool/main/a/acl/acl_2.3.1-3.debian.tar.xz' acl_2.3.1-3.debian.tar.xz 30968 SHA512:a29af03f79bf6cd50852c9538013458b8bdb579c2059df1682120ced75bf8023b32a4f4c2fff8466364d1c97ad4113f84fdfbdc1c991b3f5a7fee2b1db2692d0
```

### `dpkg` source package: `adduser=3.137ubuntu1`

Binary Packages:

- `adduser=3.137ubuntu1`

Licenses: (parsed from: `/usr/share/doc/adduser/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris adduser=3.137ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/a/adduser/adduser_3.137ubuntu1.dsc' adduser_3.137ubuntu1.dsc 1862 SHA512:4e32edd8d12689bc8f6fb2b5280b0504bbd19bdd963cebb32a016d87fbeb837cbfb9c4c544b37943adf346d33137c684936591ccbf5c89856a91f2777f00ae49
'http://archive.ubuntu.com/ubuntu/pool/main/a/adduser/adduser_3.137ubuntu1.tar.xz' adduser_3.137ubuntu1.tar.xz 280408 SHA512:46979160ef2f6b85097958cd11e549ae48efa24e1719155fd90ae7b322c0adac087cac7d0a709cd084ee11557575b05dfde89a9d63bcfd80fb47779c41098d48
```

### `dpkg` source package: `apt=2.7.3ubuntu0.1`

Binary Packages:

- `apt=2.7.3ubuntu0.1`
- `libapt-pkg6.0:amd64=2.7.3ubuntu0.1`

Licenses: (parsed from: `/usr/share/doc/apt/copyright`, `/usr/share/doc/libapt-pkg6.0/copyright`)

- `BSD-3-clause`
- `Expat`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris apt=2.7.3ubuntu0.1
'http://archive.ubuntu.com/ubuntu/pool/main/a/apt/apt_2.7.3ubuntu0.1.dsc' apt_2.7.3ubuntu0.1.dsc 3060 SHA512:2ed2e6bb90f8bd8efe674400c06b89f119204320f59cfee068e6f54d3de66d22bb2ddb502a93aae00050fbba328aacf9d0e269f51b8e81bceb8769de160fb709
'http://archive.ubuntu.com/ubuntu/pool/main/a/apt/apt_2.7.3ubuntu0.1.tar.xz' apt_2.7.3ubuntu0.1.tar.xz 2343160 SHA512:99e1d0335f3c71a9adf9964b880acebc03901381a548c0b1a53f281947b13e968a6ea674fffd5b5fd58868ddeb48302eb545365d87da95bb5e8b22c064e7673e
```

### `dpkg` source package: `attr=1:2.5.1-4`

Binary Packages:

- `libattr1:amd64=1:2.5.1-4`

Licenses: (parsed from: `/usr/share/doc/libattr1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2+`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris attr=1:2.5.1-4
'http://archive.ubuntu.com/ubuntu/pool/main/a/attr/attr_2.5.1-4.dsc' attr_2.5.1-4.dsc 2477 SHA512:acb8f17654b972fa6a9ac4701b863cff73313af8f86feaf1cf1f276a1484f02cef6fe9b6a39c4223bd1773163d223f611dbf1807dc655b3b557595130ab39290
'http://archive.ubuntu.com/ubuntu/pool/main/a/attr/attr_2.5.1.orig.tar.xz' attr_2.5.1.orig.tar.xz 318188 SHA512:9e5555260189bb6ef2440c76700ebb813ff70582eb63d446823874977307d13dfa3a347dfae619f8866943dfa4b24ccf67dadd7e3ea2637239fdb219be5d2932
'http://archive.ubuntu.com/ubuntu/pool/main/a/attr/attr_2.5.1.orig.tar.xz.asc' attr_2.5.1.orig.tar.xz.asc 833 SHA512:be4f3629ef66bd400bcdeaf8b6b1564dc729472a514d59fb4909a30f3269711dedea16002283e9aabbf83c374e0a3d70bc00f1136da0fed66a8184acdfd7e78f
'http://archive.ubuntu.com/ubuntu/pool/main/a/attr/attr_2.5.1-4.debian.tar.xz' attr_2.5.1-4.debian.tar.xz 32152 SHA512:933e59fb9dd43bf3b250dbc36276a52484271e893a96efa85648148ef84f5059b79152dad341fe6dbf5ab9dd71290e8aa6e7ceb4923ccecfe42046c096d29efe
```

### `dpkg` source package: `audit=1:3.1.1-1`

Binary Packages:

- `libaudit-common=1:3.1.1-1`
- `libaudit1:amd64=1:3.1.1-1`

Licenses: (parsed from: `/usr/share/doc/libaudit-common/copyright`, `/usr/share/doc/libaudit1/copyright`)

- `GPL-1`
- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris audit=1:3.1.1-1
'http://archive.ubuntu.com/ubuntu/pool/main/a/audit/audit_3.1.1-1.dsc' audit_3.1.1-1.dsc 2402 SHA512:860c8ba15c80cc17541ff6245fe1abc63681962476550aff63712f849ebab7ac5e50e2f4c21b4b472716ce15e6bcec656117e0acef2e2b8adc02abda17bf3863
'http://archive.ubuntu.com/ubuntu/pool/main/a/audit/audit_3.1.1.orig.tar.gz' audit_3.1.1.orig.tar.gz 1218111 SHA512:4917970cc4c7f786c464a6d101bf66d55d55ac4716cf415ff97177f08176a6301e946716d28cf5b16054538469b3140b97db99d55a28686a9a807eea60c070f3
'http://archive.ubuntu.com/ubuntu/pool/main/a/audit/audit_3.1.1-1.debian.tar.xz' audit_3.1.1-1.debian.tar.xz 18944 SHA512:ab98846a36aef4a1954b63973b57fa86e69e6012c7813068a0a7f224f30e4850c734e5ce568ed7485861fe4a362587512de4c00614326638d07bd6e3e7363af6
```

### `dpkg` source package: `base-files=13ubuntu2.1`

Binary Packages:

- `base-files=13ubuntu2.1`

Licenses: (parsed from: `/usr/share/doc/base-files/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris base-files=13ubuntu2.1
'http://archive.ubuntu.com/ubuntu/pool/main/b/base-files/base-files_13ubuntu2.1.dsc' base-files_13ubuntu2.1.dsc 1662 SHA512:ea52a840cd35f978a8d4b2076a258cdd1b96fe5b9e3d6b1fc6f13ed1de1d48821f3b4f9f0511ce2cf08b1c974f91f512d8ba64e528cf937a6a7a122c9c3c86bf
'http://archive.ubuntu.com/ubuntu/pool/main/b/base-files/base-files_13ubuntu2.1.tar.xz' base-files_13ubuntu2.1.tar.xz 93084 SHA512:3e099ed8d9fbee739047228613e2b3cf5dd7456bfa4d6d5b16d3217c77946ecbf371e2f942b4e36307eac9281193bc4b592eefd34f85de58d1c2170be5b7dc01
```

### `dpkg` source package: `base-passwd=3.6.1`

Binary Packages:

- `base-passwd=3.6.1`

Licenses: (parsed from: `/usr/share/doc/base-passwd/copyright`)

- `GPL-2`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris base-passwd=3.6.1
'http://archive.ubuntu.com/ubuntu/pool/main/b/base-passwd/base-passwd_3.6.1.dsc' base-passwd_3.6.1.dsc 1740 SHA512:b631fac3bb17d25bca3a04d74a542dcb7a97f29bd98da38dabd4c38ebfeb9638466876e20e60ea9b86f8168cc50f5ae2153a9a59d635114ff10bc9425a7a998e
'http://archive.ubuntu.com/ubuntu/pool/main/b/base-passwd/base-passwd_3.6.1.tar.xz' base-passwd_3.6.1.tar.xz 56072 SHA512:f26df2acbd103c60dd2003bc72ce043c05f66009464245d2740e4389374687e7c67114ee2120dab79546a29f9b5bd29fd8321f758fc7db32165125c4286593a8
```

### `dpkg` source package: `bash=5.2.15-2ubuntu1`

Binary Packages:

- `bash=5.2.15-2ubuntu1`

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
$ apt-get source -qq --print-uris bash=5.2.15-2ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/b/bash/bash_5.2.15-2ubuntu1.dsc' bash_5.2.15-2ubuntu1.dsc 2450 SHA512:2c4deb119d02436a930af8b6965823de57c636bedcfc9482e399fea4793f604542c8fc70d2aff522f589fd5f1f5f84b37b397d269897e913257201de03e42a82
'http://archive.ubuntu.com/ubuntu/pool/main/b/bash/bash_5.2.15.orig.tar.gz' bash_5.2.15.orig.tar.gz 9997221 SHA512:8322b26b8fd185a8c366970ce346075b4df76676d6e0f78c33d8bcac8c04a8e87bcf7cf74f5e259d90a750aa146b8baec69d1d2c2c12d26ea93472847c8dcd1f
'http://archive.ubuntu.com/ubuntu/pool/main/b/bash/bash_5.2.15-2ubuntu1.debian.tar.xz' bash_5.2.15-2ubuntu1.debian.tar.xz 103652 SHA512:b02e631ab2500c0633138e6c7fe682db4d138b9904d86c495e9d17ccff78ed5a88471d4e0288b7fabd98abc2398e1029b8f4a23f4d7550474c720addaf041bb2
```

### `dpkg` source package: `binutils=2.41-5ubuntu1`

Binary Packages:

- `binutils=2.41-5ubuntu1`
- `binutils-common:amd64=2.41-5ubuntu1`
- `binutils-x86-64-linux-gnu=2.41-5ubuntu1`
- `libbinutils:amd64=2.41-5ubuntu1`
- `libctf-nobfd0:amd64=2.41-5ubuntu1`
- `libctf0:amd64=2.41-5ubuntu1`
- `libgprofng0:amd64=2.41-5ubuntu1`
- `libsframe1:amd64=2.41-5ubuntu1`

Licenses: (parsed from: `/usr/share/doc/binutils/copyright`, `/usr/share/doc/binutils-common/copyright`, `/usr/share/doc/binutils-x86-64-linux-gnu/copyright`, `/usr/share/doc/libbinutils/copyright`, `/usr/share/doc/libctf-nobfd0/copyright`, `/usr/share/doc/libctf0/copyright`, `/usr/share/doc/libgprofng0/copyright`, `/usr/share/doc/libsframe1/copyright`)

- `GFDL`
- `GPL`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris binutils=2.41-5ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/b/binutils/binutils_2.41-5ubuntu1.dsc' binutils_2.41-5ubuntu1.dsc 9687 SHA512:cd0fc39618048e85364666297e7b89ec44985f6532cd76bd91769ae8ab182ce068edde293655c72392b5affa4313227fcc518695b831012143498f53c725be0c
'http://archive.ubuntu.com/ubuntu/pool/main/b/binutils/binutils_2.41.orig.tar.xz' binutils_2.41.orig.tar.xz 26765692 SHA512:5df45d0bd6ddabdce4f35878c041e46a92deef01e7dea5facc97fd65cc06b59abc6fba0eb454b68e571c7e14038dc823fe7f2263843e6e627b7444eaf0fe9374
'http://archive.ubuntu.com/ubuntu/pool/main/b/binutils/binutils_2.41-5ubuntu1.debian.tar.xz' binutils_2.41-5ubuntu1.debian.tar.xz 197056 SHA512:b1edb1fea3e46bd8e2e955ecee9347c9860ecacab37ac84c69a6758f1b6c52a25b2f7dc12a53840c1efddece8171a44a3159132582e17f97cbde3acd1aa3dedc
```

### `dpkg` source package: `brotli=1.0.9-2build8`

Binary Packages:

- `libbrotli1:amd64=1.0.9-2build8`

Licenses: (parsed from: `/usr/share/doc/libbrotli1/copyright`)

- `MIT`

Source:

```console
$ apt-get source -qq --print-uris brotli=1.0.9-2build8
'http://archive.ubuntu.com/ubuntu/pool/main/b/brotli/brotli_1.0.9-2build8.dsc' brotli_1.0.9-2build8.dsc 2285 SHA512:dd4dbaec5136b6ec2c96bfb495fd7bb6271cbcd74458792cddd73ad45332fe3dd8e4b7d10c4ea6b5e0c10668dc8cf322e910c8807e2297ed2c589ecc3902c014
'http://archive.ubuntu.com/ubuntu/pool/main/b/brotli/brotli_1.0.9.orig.tar.gz' brotli_1.0.9.orig.tar.gz 486984 SHA512:b8e2df955e8796ac1f022eb4ebad29532cb7e3aa6a4b6aee91dbd2c7d637eee84d9a144d3e878895bb5e62800875c2c01c8f737a1261020c54feacf9f676b5f5
'http://archive.ubuntu.com/ubuntu/pool/main/b/brotli/brotli_1.0.9-2build8.debian.tar.xz' brotli_1.0.9-2build8.debian.tar.xz 5884 SHA512:e09a1e108cbd266194f3c3760f12ee2a0608049882e9773356a457b4ca74029f8849c498fc8fdda3d101de6e1868b0776467c71ef22f2e9e245b4cb4871203cc
```

### `dpkg` source package: `bzip2=1.0.8-5build1`

Binary Packages:

- `libbz2-1.0:amd64=1.0.8-5build1`

Licenses: (parsed from: `/usr/share/doc/libbz2-1.0/copyright`)

- `BSD-variant`
- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris bzip2=1.0.8-5build1
'http://archive.ubuntu.com/ubuntu/pool/main/b/bzip2/bzip2_1.0.8-5build1.dsc' bzip2_1.0.8-5build1.dsc 1860 SHA512:dfb9cd3a99f8c80a27e088b6ba7f06f50bc2bdbc61f574ed8f77d0fa58ff07fa1c34a060351fd4b601537181143dd934caadd7a00eb97aea5933febb7b61743d
'http://archive.ubuntu.com/ubuntu/pool/main/b/bzip2/bzip2_1.0.8.orig.tar.gz' bzip2_1.0.8.orig.tar.gz 810029 SHA512:083f5e675d73f3233c7930ebe20425a533feedeaaa9d8cc86831312a6581cefbe6ed0d08d2fa89be81082f2a5abdabca8b3c080bf97218a1bd59dc118a30b9f3
'http://archive.ubuntu.com/ubuntu/pool/main/b/bzip2/bzip2_1.0.8-5build1.debian.tar.bz2' bzip2_1.0.8-5build1.debian.tar.bz2 26870 SHA512:e030c257c3458d780fd0ffc6f328efd69d0e875e81acd7441a7c6651194ebded61017c96aad7c99061f93d50dfc33056abe98c9a599abc900f49d51c4a1eed6f
```

### `dpkg` source package: `ca-certificates=20230311ubuntu1`

Binary Packages:

- `ca-certificates=20230311ubuntu1`

Licenses: (parsed from: `/usr/share/doc/ca-certificates/copyright`)

- `GPL-2`
- `GPL-2+`
- `MPL-2.0`

Source:

```console
$ apt-get source -qq --print-uris ca-certificates=20230311ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/c/ca-certificates/ca-certificates_20230311ubuntu1.dsc' ca-certificates_20230311ubuntu1.dsc 1846 SHA512:dd9af00eafa728a2d32ac7cc30e781f7983dbf3b56e85a1daa53ba958f364af60ae7dbc3c50ebd435398b127472ac19bf2658f6829ef8c8cc44c02c75f5858e7
'http://archive.ubuntu.com/ubuntu/pool/main/c/ca-certificates/ca-certificates_20230311ubuntu1.tar.xz' ca-certificates_20230311ubuntu1.tar.xz 258172 SHA512:15b59854164fccf1a057f4f97cb4b07a09c1bdcbfb8a36e9436ce50c50b447100e604edc35bfbf8a7ce64755fc40897c50f70503b3ba3cfcd0c6e1f3f4e6ba20
```

### `dpkg` source package: `cdebconf=0.270ubuntu1`

Binary Packages:

- `libdebconfclient0:amd64=0.270ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libdebconfclient0/copyright`)

- `BSD-2-Clause`
- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris cdebconf=0.270ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/c/cdebconf/cdebconf_0.270ubuntu1.dsc' cdebconf_0.270ubuntu1.dsc 2873 SHA512:03876bf61814c0d99bcdb548b27a33ea04b82d6d1431266b7afab72238a2e1410c5dccfa9409f360008f3808a1f930f1d870655c0c7b1bf2c689fc764739cefc
'http://archive.ubuntu.com/ubuntu/pool/main/c/cdebconf/cdebconf_0.270ubuntu1.tar.xz' cdebconf_0.270ubuntu1.tar.xz 285780 SHA512:37ac3c7a352dea023b10dad8202f31e037e8bf8d1fc5050a757107ea4ba5561ae0f74c6254778bf4dc3226f343e2c1873e41412708b845fd65fd23eb7969e6de
```

### `dpkg` source package: `coreutils=9.1-1ubuntu2.23.10.1`

Binary Packages:

- `coreutils=9.1-1ubuntu2.23.10.1`

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
$ apt-get source -qq --print-uris coreutils=9.1-1ubuntu2.23.10.1
'http://archive.ubuntu.com/ubuntu/pool/main/c/coreutils/coreutils_9.1-1ubuntu2.23.10.1.dsc' coreutils_9.1-1ubuntu2.23.10.1.dsc 2067 SHA512:250b1dd01211319439ae1caefbbd7d4e5dc7b2417d19f8c351d0b5e4e1641d5f2e98a94d7c4788595abd1d069f15980795cad4b618190a72219b65b8e32e7657
'http://archive.ubuntu.com/ubuntu/pool/main/c/coreutils/coreutils_9.1.orig.tar.xz' coreutils_9.1.orig.tar.xz 5712104 SHA512:a6ee2c549140b189e8c1b35e119d4289ec27244ec0ed9da0ac55202f365a7e33778b1dc7c4e64d1669599ff81a8297fe4f5adbcc8a3a2f75c919a43cd4b9bdfa
'http://archive.ubuntu.com/ubuntu/pool/main/c/coreutils/coreutils_9.1-1ubuntu2.23.10.1.debian.tar.xz' coreutils_9.1-1ubuntu2.23.10.1.debian.tar.xz 40548 SHA512:292b527f99b31536d6f3acde91effabe45833b4bc2c0f213069386a47fa946a687e81f0555f66c6e8309ef5111287d7be57ddab7acd5b48e64ff1ef7e2f6723d
```

### `dpkg` source package: `curl=8.2.1-1ubuntu3.3`

Binary Packages:

- `libcurl3-gnutls:amd64=8.2.1-1ubuntu3.3`
- `libcurl4:amd64=8.2.1-1ubuntu3.3`
- `libcurl4-openssl-dev:amd64=8.2.1-1ubuntu3.3`

Licenses: (parsed from: `/usr/share/doc/libcurl3-gnutls/copyright`, `/usr/share/doc/libcurl4/copyright`, `/usr/share/doc/libcurl4-openssl-dev/copyright`)

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
$ apt-get source -qq --print-uris curl=8.2.1-1ubuntu3.3
'http://archive.ubuntu.com/ubuntu/pool/main/c/curl/curl_8.2.1-1ubuntu3.3.dsc' curl_8.2.1-1ubuntu3.3.dsc 3094 SHA512:25b5f5a2ffa430680db978fd82ed2d74d61e68edccc347f5d47c9e5806aa4e8f6dff8c7417756c8c1982a8eb173190c883e69e6fe9e69bb4779116084e4b2114
'http://archive.ubuntu.com/ubuntu/pool/main/c/curl/curl_8.2.1.orig.tar.gz' curl_8.2.1.orig.tar.gz 4394020 SHA512:d0a906f4dff4c485e6dae930d9a7530147f4c0a0cbb46a83cb9be9d7bd6b9c320386c8be5bcdd3749f2d468b0daf39d06e8c581bab1fa792fd26da409a575cbd
'http://archive.ubuntu.com/ubuntu/pool/main/c/curl/curl_8.2.1-1ubuntu3.3.debian.tar.xz' curl_8.2.1-1ubuntu3.3.debian.tar.xz 56220 SHA512:f48cd788bd1c8dceb91d2060e11f3698b29a78d3ecb241ad3171187c733205f75a8e347e6fc2568f6d7acd6541035c6ade55a816d4d798c1ae185780189f62f6
```

### `dpkg` source package: `cyrus-sasl2=2.1.28+dfsg1-3`

Binary Packages:

- `libsasl2-2:amd64=2.1.28+dfsg1-3`
- `libsasl2-modules:amd64=2.1.28+dfsg1-3`
- `libsasl2-modules-db:amd64=2.1.28+dfsg1-3`

Licenses: (parsed from: `/usr/share/doc/libsasl2-2/copyright`, `/usr/share/doc/libsasl2-modules/copyright`, `/usr/share/doc/libsasl2-modules-db/copyright`)

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
$ apt-get source -qq --print-uris cyrus-sasl2=2.1.28+dfsg1-3
'http://archive.ubuntu.com/ubuntu/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.28%2bdfsg1-3.dsc' cyrus-sasl2_2.1.28+dfsg1-3.dsc 3330 SHA512:3ac2330cb2cd35120eb80cb45866595abaf1dd5fbd357236f8b8e63eee3dd81e41235c10725cdca9b2b6785c36aa1412052f7769fa051cfe57b476c1ad63b2fd
'http://archive.ubuntu.com/ubuntu/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.28%2bdfsg1.orig.tar.xz' cyrus-sasl2_2.1.28+dfsg1.orig.tar.xz 794540 SHA512:e94075d09b38a50138b782323de286deb7b15008064f07df4fa682e94367e829d9bfafef48d5478f730fef8fde536bcc6d54cab0452b76473a3c620b3dc18fa2
'http://archive.ubuntu.com/ubuntu/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.28%2bdfsg1-3.debian.tar.xz' cyrus-sasl2_2.1.28+dfsg1-3.debian.tar.xz 106568 SHA512:4f602a8532af0bd452ed5be4a018ef60a91527621fc3dca52efd86c2b0ee99697a6f9f7453c1a7fbbbfa130bb889da71ef10fb8d9604fdc8a710c50f302a620b
```

### `dpkg` source package: `dash=0.5.12-6ubuntu1`

Binary Packages:

- `dash=0.5.12-6ubuntu1`

Licenses: (parsed from: `/usr/share/doc/dash/copyright`)

- `BSD-3-Clause`
- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris dash=0.5.12-6ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/d/dash/dash_0.5.12-6ubuntu1.dsc' dash_0.5.12-6ubuntu1.dsc 2087 SHA512:4f7dab651cbcbb65749c58f99e13ebc9e4e035663c35a5954e79a55fb034f82f1755891b24eac6fdbdcd9d4ea41356f365e01e880a07bd36a0fd77e6da9c333d
'http://archive.ubuntu.com/ubuntu/pool/main/d/dash/dash_0.5.12.orig.tar.gz' dash_0.5.12.orig.tar.gz 246054 SHA512:13bd262be0089260cbd13530a9cf34690c0abeb2f1920eb5e61be7951b716f9f335b86279d425dbfae56cbd49231a8fdffdff70601a5177da3d543be6fc5eb17
'http://archive.ubuntu.com/ubuntu/pool/main/d/dash/dash_0.5.12-6ubuntu1.debian.tar.xz' dash_0.5.12-6ubuntu1.debian.tar.xz 39428 SHA512:bab3a9c5bbd839e4a8aaa50df73d4a71b1086dcfebd5d19d12811733382e04e48e694c5f87f901481540cd4e9819503ab246d0270dffde37baaa6dff3f65e454
```

### `dpkg` source package: `db5.3=5.3.28+dfsg2-2`

Binary Packages:

- `libdb5.3:amd64=5.3.28+dfsg2-2`

Licenses: (parsed from: `/usr/share/doc/libdb5.3/copyright`)

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
$ apt-get source -qq --print-uris db5.3=5.3.28+dfsg2-2
'http://archive.ubuntu.com/ubuntu/pool/main/d/db5.3/db5.3_5.3.28%2bdfsg2-2.dsc' db5.3_5.3.28+dfsg2-2.dsc 2183 SHA512:f9e34e976efb957df08c00d6da2f201e4c2179931942ffb8188cdf7eba24724f42907df0f8a3b275a5aa41ba07518b8a336b39a97e7d35c57dc398f52860585c
'http://archive.ubuntu.com/ubuntu/pool/main/d/db5.3/db5.3_5.3.28%2bdfsg2.orig.tar.xz' db5.3_5.3.28+dfsg2.orig.tar.xz 21287688 SHA512:f9c9d042702ef3fcfdd4b4859583048f3396b161009dc24b6d3a2c53533d58214239fc80e2c42db17e9f092df44d531502737f3b368b956bff49ef057b6b51ef
'http://archive.ubuntu.com/ubuntu/pool/main/d/db5.3/db5.3_5.3.28%2bdfsg2-2.debian.tar.xz' db5.3_5.3.28+dfsg2-2.debian.tar.xz 33560 SHA512:c710253211e0ce4d7adfd74ba2ebbc9aac3495f0f5506e18af584569ce77eabaf2c7eae0bc91826bee93ec2f1338ed3c0de6a89cc571af795c535e928afeca81
```

### `dpkg` source package: `debconf=1.5.82`

Binary Packages:

- `debconf=1.5.82`

Licenses: (parsed from: `/usr/share/doc/debconf/copyright`)

- `BSD-2-clause`

Source:

```console
$ apt-get source -qq --print-uris debconf=1.5.82
'http://archive.ubuntu.com/ubuntu/pool/main/d/debconf/debconf_1.5.82.dsc' debconf_1.5.82.dsc 2035 SHA512:bca5b8290d54709a706faaef77f16fb98fc074e7aacc8a40d650f4a76c1d843b8a2534cadbfe9f6170e6d4892b82d76f2fb16e474fb82bcc5e616024fae68be6
'http://archive.ubuntu.com/ubuntu/pool/main/d/debconf/debconf_1.5.82.tar.xz' debconf_1.5.82.tar.xz 571540 SHA512:5a9b26d90cf02e6f5b267e6e6416e91ac31115b124b05b4edd2dd785eea92a6d9c060f591dad6645784ff956a07555cb1bf11a35f4712d5bc308c4b6726da88a
```

### `dpkg` source package: `debianutils=5.8-1`

Binary Packages:

- `debianutils=5.8-1`

Licenses: (parsed from: `/usr/share/doc/debianutils/copyright`)

- `GPL-2`
- `GPL-2+`
- `SMAIL-GPL`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris debianutils=5.8-1
'http://archive.ubuntu.com/ubuntu/pool/main/d/debianutils/debianutils_5.8-1.dsc' debianutils_5.8-1.dsc 1647 SHA512:8e6471fa22098d7cf13750849ebc0ff2f2bdfd50490186d85e7c7e4bef94ca14b5e02f1339db91ce5df5cf926262d7842c4f5da01aa47c5ac9b6199dc72a0b70
'http://archive.ubuntu.com/ubuntu/pool/main/d/debianutils/debianutils_5.8.orig.tar.gz' debianutils_5.8.orig.tar.gz 260865 SHA512:7fddff17804ab334ac1ab3fa4b76a3fed8d83dc2dbf8d9ab1e486b5f226ac8363e98336cfa651c7630eef5fffa4551dbf7a5da1ba60f033b279f9aca624d58a2
'http://archive.ubuntu.com/ubuntu/pool/main/d/debianutils/debianutils_5.8-1.debian.tar.xz' debianutils_5.8-1.debian.tar.xz 22044 SHA512:7b0f1663447b894d69eb56391324604e705e0af3026fc1a3a08edf891e1c16e29c88e2aaae0c8632ecd2e1965b7118b2921117230139e93484154383dcdd0120
```

### `dpkg` source package: `diffutils=1:3.8-4`

Binary Packages:

- `diffutils=1:3.8-4`

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
$ apt-get source -qq --print-uris diffutils=1:3.8-4
'http://archive.ubuntu.com/ubuntu/pool/main/d/diffutils/diffutils_3.8-4.dsc' diffutils_3.8-4.dsc 1705 SHA512:b666ab8c76ddda9262d84f00e17b5139bae88d612233332e75f51f18975177460e6891cb3b28e20d8a9311df9aaa927a280cf4a7855d566e9569154e1237ae7e
'http://archive.ubuntu.com/ubuntu/pool/main/d/diffutils/diffutils_3.8.orig.tar.xz' diffutils_3.8.orig.tar.xz 1585120 SHA512:279441270987e70d5ecfaf84b6285a4866929c43ec877e50f154a788858d548a8a316f2fc26ad62f7348c8d289cb29a09d06dfadce1806e3d8b4ea88c8b1aa7c
'http://archive.ubuntu.com/ubuntu/pool/main/d/diffutils/diffutils_3.8.orig.tar.xz.asc' diffutils_3.8.orig.tar.xz.asc 833 SHA512:0464ac89209411993800666b45ff90243d22fbda53bf1d71c6870d565b39cc8d9c54c141b9d297a181ce74ad8fb5313953f416bced179ff7728a52a3e9a4f5a5
'http://archive.ubuntu.com/ubuntu/pool/main/d/diffutils/diffutils_3.8-4.debian.tar.xz' diffutils_3.8-4.debian.tar.xz 14428 SHA512:874a41a50f6db1b91a358445513a22a24871be830a10a9d192ac2957fa91a4c3e2265472fcf08f867b21a1c125b192ca559cc77c5ad51e35275a635d58ae1c8a
```

### `dpkg` source package: `dpkg=1.22.0ubuntu1.1`

Binary Packages:

- `dpkg=1.22.0ubuntu1.1`

Licenses: (parsed from: `/usr/share/doc/dpkg/copyright`)

- `GPL-2`
- `GPL-2+`
- `public-domain-s-s-d`

Source:

```console
$ apt-get source -qq --print-uris dpkg=1.22.0ubuntu1.1
'http://archive.ubuntu.com/ubuntu/pool/main/d/dpkg/dpkg_1.22.0ubuntu1.1.dsc' dpkg_1.22.0ubuntu1.1.dsc 3077 SHA512:9ac9f8b47cd66b7cb4946997aaaa5959b7fd3a5a33518da768da76cb895597e144a55dbff0bfbbb8205cac12de5f719d6fc0ba60936eb75d4668228e609f8251
'http://archive.ubuntu.com/ubuntu/pool/main/d/dpkg/dpkg_1.22.0ubuntu1.1.tar.xz' dpkg_1.22.0ubuntu1.1.tar.xz 5358400 SHA512:da9b2834b703e1c3d038207537ca587f1ad18c7d1bac543beec715381e3f6a2b40fcb56904880b922ee3c68e0e4d5c93f8f1b03c24731b90eb03c05b0b7c5e04
```

### `dpkg` source package: `e2fsprogs=1.47.0-2ubuntu1`

Binary Packages:

- `e2fsprogs=1.47.0-2ubuntu1`
- `libcom-err2:amd64=1.47.0-2ubuntu1`
- `libext2fs2:amd64=1.47.0-2ubuntu1`
- `libss2:amd64=1.47.0-2ubuntu1`
- `logsave=1.47.0-2ubuntu1`

Licenses: (parsed from: `/usr/share/doc/e2fsprogs/copyright`, `/usr/share/doc/libcom-err2/copyright`, `/usr/share/doc/libext2fs2/copyright`, `/usr/share/doc/libss2/copyright`, `/usr/share/doc/logsave/copyright`)

- `Apache-2`
- `Apache-2.0`
- `BSD-3-Clause`
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
$ apt-get source -qq --print-uris e2fsprogs=1.47.0-2ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/e/e2fsprogs/e2fsprogs_1.47.0-2ubuntu1.dsc' e2fsprogs_1.47.0-2ubuntu1.dsc 3211 SHA512:a0139d8d0528a623e8452366b24313d5bf4d1fa4ad493ab349965c9ad2e8eb00af99b5ea5cb597aaa151856f2be90e52df302b0d6e45d8f93d83ec4860c4650a
'http://archive.ubuntu.com/ubuntu/pool/main/e/e2fsprogs/e2fsprogs_1.47.0.orig.tar.gz' e2fsprogs_1.47.0.orig.tar.gz 9637717 SHA512:4f03a469d03cb0f0656bd17c64d944606fb25e68002e3e42c278f3775fee6bf776cc2061ae378b5df4f167a5c33444490111fdcbb140e0320445706f9d048dd0
'http://archive.ubuntu.com/ubuntu/pool/main/e/e2fsprogs/e2fsprogs_1.47.0.orig.tar.gz.asc' e2fsprogs_1.47.0.orig.tar.gz.asc 488 SHA512:cd3652ec12f694f1c1f5bd4af4964bb32ad832ba8a06a48864d12a998dc514e9a950ebdb475707a3abb8360852a3469794f2327f097328c99233beef575df144
'http://archive.ubuntu.com/ubuntu/pool/main/e/e2fsprogs/e2fsprogs_1.47.0-2ubuntu1.debian.tar.xz' e2fsprogs_1.47.0-2ubuntu1.debian.tar.xz 89008 SHA512:3e75641abe50c48202ea2ddb7bb23939201ae1d739298920525590474447c85cf921518cac05b167cbd02470ac19108abe12a25943759b300c11cf552aea7cb0
```

### `dpkg` source package: `expat=2.5.0-2ubuntu0.1`

Binary Packages:

- `libexpat1:amd64=2.5.0-2ubuntu0.1`
- `libexpat1-dev:amd64=2.5.0-2ubuntu0.1`

Licenses: (parsed from: `/usr/share/doc/libexpat1/copyright`, `/usr/share/doc/libexpat1-dev/copyright`)

- `MIT`

Source:

```console
$ apt-get source -qq --print-uris expat=2.5.0-2ubuntu0.1
'http://archive.ubuntu.com/ubuntu/pool/main/e/expat/expat_2.5.0-2ubuntu0.1.dsc' expat_2.5.0-2ubuntu0.1.dsc 2120 SHA512:f6230d394453cca9ce1e9e226277e053eb788b7cc04a85ea9fa6f89b4dc979e149fbd8f76eac8329ccc661a03dc3296cab63e43cd73814e5eec3ecaa8551eb5c
'http://archive.ubuntu.com/ubuntu/pool/main/e/expat/expat_2.5.0.orig.tar.gz' expat_2.5.0.orig.tar.gz 8320988 SHA512:779f0d0f3f2d8b33db0fd044864ab5ab1a40f20501f792fe90ad0d18de536c4765c3749f120e21fec11a0e6c89af1dc576d1fe261c871ca44a594f7b61fd1d9e
'http://archive.ubuntu.com/ubuntu/pool/main/e/expat/expat_2.5.0-2ubuntu0.1.debian.tar.xz' expat_2.5.0-2ubuntu0.1.debian.tar.xz 20320 SHA512:478556bc126a54ba9f854ac92ce3273e691398c97a1d42e7b5061cf94dfdb82b14280382a4985b73f483eb5129e6471afef8d6505a858c31c8ff54ab812aedbb
```

### `dpkg` source package: `findutils=4.9.0-5`

Binary Packages:

- `findutils=4.9.0-5`

Licenses: (parsed from: `/usr/share/doc/findutils/copyright`)

- `BSD-3-clause`
- `BSD-3-clause and/or GPL-3+`
- `FSFAP`
- `FSFULLR`
- `GFDL-1.3`
- `GFDL-NIV-1.3+`
- `GPL with automake exception`
- `GPL-2`
- `GPL-2+`
- `GPL-2+ with Autoconf-data exception`
- `GPL-3`
- `GPL-3+`
- `GPL-3+ with Autoconf-data exception`
- `GPL-3+ with Bison-2.2 exception`
- `ISC`
- `ISC and/or LGPL-2.1+`
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
$ apt-get source -qq --print-uris findutils=4.9.0-5
'http://archive.ubuntu.com/ubuntu/pool/main/f/findutils/findutils_4.9.0-5.dsc' findutils_4.9.0-5.dsc 2272 SHA512:8f901310a8e3b1957ee3a4ada366a070c0596a7e706dc6b917dde0ecf75737e72b9bfe1d0c2812676b733e077c93929c5899b0bb50e7e966e109b2473e75d698
'http://archive.ubuntu.com/ubuntu/pool/main/f/findutils/findutils_4.9.0.orig.tar.xz' findutils_4.9.0.orig.tar.xz 2046252 SHA512:ba4844f4403de0148ad14b46a3dbefd5a721f6257c864bf41a6789b11705408524751c627420b15a52af95564d8e5b52f0978474f640a62ab86a41d20cf14be9
'http://archive.ubuntu.com/ubuntu/pool/main/f/findutils/findutils_4.9.0.orig.tar.xz.asc' findutils_4.9.0.orig.tar.xz.asc 488 SHA512:b8e0b5471242912a20b9e468fa27b7f27339af5f7be8918173105262dee0152183bf4cf516844d348b206a694e028490d5d3b190f3aed8c698ba5444941f8dfc
'http://archive.ubuntu.com/ubuntu/pool/main/f/findutils/findutils_4.9.0-5.debian.tar.xz' findutils_4.9.0-5.debian.tar.xz 32744 SHA512:64b5df8347a4d698787dae61c0adac845b0dc66450736931e04c5ad072756a5e5191c8e4995e4fa5a568caf0f851518eb3c8358991a4e5749c3f2306b5446380
```

### `dpkg` source package: `fontconfig=2.14.2-4ubuntu1`

Binary Packages:

- `fontconfig-config=2.14.2-4ubuntu1`
- `libfontconfig1:amd64=2.14.2-4ubuntu1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris fontconfig=2.14.2-4ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/f/fontconfig/fontconfig_2.14.2-4ubuntu1.dsc' fontconfig_2.14.2-4ubuntu1.dsc 2430 SHA512:c727a4b4fbb1707fd993b9de35ab46c28ea1ebcb5a27cd78747cfbd5b19aadefd5a5e03c0b6cb1a0edf7b78a3a7d5f1d57a3303f8ab3f50255109d9eab7a218c
'http://archive.ubuntu.com/ubuntu/pool/main/f/fontconfig/fontconfig_2.14.2.orig.tar.xz' fontconfig_2.14.2.orig.tar.xz 1440844 SHA512:23483e0ae6aa7589fd37f9949a4cf951c5bff981739dbb446881e4cea86a208c0ab31e2358666eac724af1dc6a689a42733a7ce91cd3e76d8d91eacedb318085
'http://archive.ubuntu.com/ubuntu/pool/main/f/fontconfig/fontconfig_2.14.2-4ubuntu1.debian.tar.xz' fontconfig_2.14.2-4ubuntu1.debian.tar.xz 29108 SHA512:920f2b352d3a6871e044e31062d3a3928b43e53c1a8f518135927d09f371c139f21ce29178a04a1f3aea73a0de2743f23bbb81c44fe953a5d52d05d564ea2541
```

### `dpkg` source package: `fonts-noto=20201225-2`

Binary Packages:

- `fonts-noto-core=20201225-2`
- `fonts-noto-mono=20201225-2`

Licenses: (parsed from: `/usr/share/doc/fonts-noto-core/copyright`, `/usr/share/doc/fonts-noto-mono/copyright`)

- `GPL-3`
- `GPL-3+`
- `OFL-1.1`

Source:

```console
$ apt-get source -qq --print-uris fonts-noto=20201225-2
'http://archive.ubuntu.com/ubuntu/pool/main/f/fonts-noto/fonts-noto_20201225-2.dsc' fonts-noto_20201225-2.dsc 2377 SHA512:36234e61f8c356b83a89609872c184592084e4c56edbadad3181068f7f21464b8542d1bca9b9a4083762310b0970904a5a0e1c43b30876ec2807f5c663b29913
'http://archive.ubuntu.com/ubuntu/pool/main/f/fonts-noto/fonts-noto_20201225.orig.tar.gz' fonts-noto_20201225.orig.tar.gz 903613276 SHA512:240ae214729388e7000a4e12a1fc81b0b562ca6f3fcb4fcdef66a27c1b193825fbf2d0fd4cc8fbae4cd17f57e21fd1589150cb02b7b618d670742692b748f9ff
'http://archive.ubuntu.com/ubuntu/pool/main/f/fonts-noto/fonts-noto_20201225-2.debian.tar.xz' fonts-noto_20201225-2.debian.tar.xz 110764 SHA512:409610ac8c3ff677578a11f18da8fee6141aee74cad264bcbed65cd3f4c389704eafcac57f2913058f5d62f523ebd39b968b6f17b6a2aae4875953817ec378c3
```

### `dpkg` source package: `freetype=2.13.1+dfsg-1`

Binary Packages:

- `libfreetype6:amd64=2.13.1+dfsg-1`

Licenses: (parsed from: `/usr/share/doc/libfreetype6/copyright`)

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
$ apt-get source -qq --print-uris freetype=2.13.1+dfsg-1
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.13.1%2bdfsg-1.dsc' freetype_2.13.1+dfsg-1.dsc 3686 SHA512:4895ec7f089fc7996f111ed2ec41f9604887ce2cab5009635528478f4a3c27852e7810a851983315176f30bcf146769a1345300cf34bebb399068bb03e2f185c
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.13.1%2bdfsg.orig-ft2demos.tar.xz' freetype_2.13.1+dfsg.orig-ft2demos.tar.xz 339736 SHA512:c03205266a420c589eec2a95ca082ab1c5606215a477500fe1a2f31c2f30c327a61e1fececec4ca3268f1a8b92a0bc8310bacf26f276ec09062fa5c5b0878511
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.13.1%2bdfsg.orig-ft2demos.tar.xz.asc' freetype_2.13.1+dfsg.orig-ft2demos.tar.xz.asc 833 SHA512:ad8460a919e1c6d42c16f17a5c6b8129c1b251ecb1221d3414e1365e5e616371499c0668e6fda5564f0035dfb484261db4ea88fdcaebca42135056fdc0a1d3d5
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.13.1%2bdfsg.orig-ft2docs.tar.xz' freetype_2.13.1+dfsg.orig-ft2docs.tar.xz 2173864 SHA512:e18f0851c52689628fb7fa520c6165895650412bfe1ebab8417bf5738d5cc7d1877e78e4afbede0996938f33554f53a0ea7b837fe81497a12b10daae5b8829ed
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.13.1%2bdfsg.orig-ft2docs.tar.xz.asc' freetype_2.13.1+dfsg.orig-ft2docs.tar.xz.asc 833 SHA512:3250509e01b51bb3f0db62c943f35f83a8a3ff87cffa4b0b77e6836c192ac2711b1dcef04d0496799e466a1e3a631aa8d524513a8dcd4771728ddd2d15e43463
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.13.1%2bdfsg.orig.tar.xz' freetype_2.13.1+dfsg.orig.tar.xz 2224144 SHA512:d858b6eb1b1a6374e3cd9db89849750d100c74781bbc32f7483346febbf2118c3abca8d9f83fb2575c8609f8a7dc9379d7c64f7c928b3da6f72ff6fa57a83520
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.13.1%2bdfsg-1.debian.tar.xz' freetype_2.13.1+dfsg-1.debian.tar.xz 44484 SHA512:92b8cd686ce5f7058283fe320f9ed5c42ad2721562cb966d7308296fc126251b618dbf5c39d5250858fda82eead3e068f2fa426df2fbfba3d71aa25a4fd5cae3
```

### `dpkg` source package: `gcc-11=11.4.0-4ubuntu1`

Binary Packages:

- `gcc-11-base:amd64=11.4.0-4ubuntu1`
- `libasan6:amd64=11.4.0-4ubuntu1`
- `libgcc-11-dev:amd64=11.4.0-4ubuntu1`
- `libstdc++-11-dev:amd64=11.4.0-4ubuntu1`
- `libtsan0:amd64=11.4.0-4ubuntu1`

Licenses: (parsed from: `/usr/share/doc/gcc-11-base/copyright`, `/usr/share/doc/libasan6/copyright`, `/usr/share/doc/libgcc-11-dev/copyright`, `/usr/share/doc/libstdc++-11-dev/copyright`, `/usr/share/doc/libtsan0/copyright`)

- `Artistic`
- `GFDL-1.2`
- `GPL`
- `GPL-2`
- `GPL-3`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris gcc-11=11.4.0-4ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-11/gcc-11_11.4.0-4ubuntu1.dsc' gcc-11_11.4.0-4ubuntu1.dsc 22826 SHA512:47a8b5050b09e5246d81c152063bdabadf7d0d241d952303184fb42b420f26afc49beeaa028869ca04bca60e4f80a6327322eeef74c3ecfec1cd997509c18941
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-11/gcc-11_11.4.0.orig.tar.gz' gcc-11_11.4.0.orig.tar.gz 86949353 SHA512:c6fd2066dd230c7b4d4db75bb414dca062eb7f0565c8ea531183a51abd75c229ac0badeb5a959a09fc1a35de4ce5282cdb8142fe356f567da1fa50b1525983a5
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-11/gcc-11_11.4.0-4ubuntu1.debian.tar.xz' gcc-11_11.4.0-4ubuntu1.debian.tar.xz 585196 SHA512:788f773e0c6a29a61c7469af64daf0261542904124f4c63c1ea507ab4325a993b7103baa3baf02e84ec322959fabbd6600a93c5667c06f102b63436bee114c77
```

### `dpkg` source package: `gcc-13=13.2.0-4ubuntu3`

Binary Packages:

- `gcc-13-base:amd64=13.2.0-4ubuntu3`
- `libatomic1:amd64=13.2.0-4ubuntu3`
- `libgcc-s1:amd64=13.2.0-4ubuntu3`
- `libgomp1:amd64=13.2.0-4ubuntu3`
- `libitm1:amd64=13.2.0-4ubuntu3`
- `liblsan0:amd64=13.2.0-4ubuntu3`
- `libquadmath0:amd64=13.2.0-4ubuntu3`
- `libstdc++6:amd64=13.2.0-4ubuntu3`
- `libubsan1:amd64=13.2.0-4ubuntu3`

Licenses: (parsed from: `/usr/share/doc/gcc-13-base/copyright`, `/usr/share/doc/libatomic1/copyright`, `/usr/share/doc/libgcc-s1/copyright`, `/usr/share/doc/libgomp1/copyright`, `/usr/share/doc/libitm1/copyright`, `/usr/share/doc/liblsan0/copyright`, `/usr/share/doc/libquadmath0/copyright`, `/usr/share/doc/libstdc++6/copyright`, `/usr/share/doc/libubsan1/copyright`)

- `Artistic`
- `GFDL-1.2`
- `GPL`
- `GPL-2`
- `GPL-3`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris gcc-13=13.2.0-4ubuntu3
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-13/gcc-13_13.2.0-4ubuntu3.dsc' gcc-13_13.2.0-4ubuntu3.dsc 27652 SHA512:161ebdcff6af93dac86b5591e9ff35abfee8b2cad1c881c09e289c7cb6ed22c9a0c71a315061bc2e90eb992367d1e04a620a3eb386c75c6741dbd53efb2bdb15
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-13/gcc-13_13.2.0.orig.tar.gz' gcc-13_13.2.0.orig.tar.gz 92596024 SHA512:cf149aff3cbee36bf23987e91016fa3f93dbcba8c88319876e6aa3cacd1dacea27d06ea7c4da6394a56d7d9d4f14ac928ead7d25502f0cc6db558f7f5cd99dff
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-13/gcc-13_13.2.0-4ubuntu3.debian.tar.xz' gcc-13_13.2.0-4ubuntu3.debian.tar.xz 1581144 SHA512:7ea0e627632deafe26cf219e4288fb9e1a6b9a7df4c8d2177fce9111b021d5d580ceff5cdcaf11adccb3bb4c72d3aac289417b67365ef771b8a2de4b43301dc9
```

### `dpkg` source package: `gdbm=1.23-3`

Binary Packages:

- `libgdbm-compat4:amd64=1.23-3`
- `libgdbm6:amd64=1.23-3`

Licenses: (parsed from: `/usr/share/doc/libgdbm-compat4/copyright`, `/usr/share/doc/libgdbm6/copyright`)

- `GFDL-NIV-1.3+`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris gdbm=1.23-3
'http://archive.ubuntu.com/ubuntu/pool/main/g/gdbm/gdbm_1.23-3.dsc' gdbm_1.23-3.dsc 2583 SHA512:847e5955f668b7ed9e68ff9dd83f68582f53de50190d7fdade5a3ac0fdb9d2f76bf0e17aa5e873e29c2ac9f8b6e611980e80fc2084fd25cca8364ed4c23e0496
'http://archive.ubuntu.com/ubuntu/pool/main/g/gdbm/gdbm_1.23.orig.tar.gz' gdbm_1.23.orig.tar.gz 1115854 SHA512:918080cb0225b221c11eb7339634a95e00c526072395f7a3d46ccf42ef020dea7c4c5bec34aff2c4f16033e1fff6583252b7e978f68b8d7f8736b0e025838e10
'http://archive.ubuntu.com/ubuntu/pool/main/g/gdbm/gdbm_1.23.orig.tar.gz.asc' gdbm_1.23.orig.tar.gz.asc 181 SHA512:6653751c04584f10aa3325bd1cb5b9f7970a786dd2a99602ea620c11a86a9ba5c342aa52627bd06c03da822e9e1600dc034d9a8f42856a287fd67f6b9f161c71
'http://archive.ubuntu.com/ubuntu/pool/main/g/gdbm/gdbm_1.23-3.debian.tar.xz' gdbm_1.23-3.debian.tar.xz 18552 SHA512:bf4f6cc7fba1a2d1eb8aecbb373fdcbd6244040964def34c5559c2643ec02b2acb25f0ff7107336553b3e2abf9ceaf73453e1990988efd951f63c47e67ae4ac6
```

### `dpkg` source package: `git=1:2.40.1-1ubuntu1.1`

Binary Packages:

- `git=1:2.40.1-1ubuntu1.1`
- `git-man=1:2.40.1-1ubuntu1.1`

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
$ apt-get source -qq --print-uris git=1:2.40.1-1ubuntu1.1
'http://archive.ubuntu.com/ubuntu/pool/main/g/git/git_2.40.1-1ubuntu1.1.dsc' git_2.40.1-1ubuntu1.1.dsc 2927 SHA512:60b41b4eb929949bc5d1f405e03b915e77e5e182e0ae93cafc16717823c7df14ed74fc51c9af8897c8bba407e1a930f882eaa366570c265e7872ad78f2b002f7
'http://archive.ubuntu.com/ubuntu/pool/main/g/git/git_2.40.1.orig.tar.xz' git_2.40.1.orig.tar.xz 7185260 SHA512:9ab41c64c6e666c314683bc4925535e037d43f947b8d327ff7d0379ac12899f4effcc2fe4e47b1ce652ad7140aa4f01f3b99f9cc0cf854cfeface1a5d3e1893e
'http://archive.ubuntu.com/ubuntu/pool/main/g/git/git_2.40.1-1ubuntu1.1.debian.tar.xz' git_2.40.1-1ubuntu1.1.debian.tar.xz 756220 SHA512:d3105d95eedecaf1b1d8255d9a89c9a14f590d8fd390efa2dba395c9315665431a453e58f6bfea37136ca54eeabec79726ac6787695abf6f3e3f3b8ca0a48266
```

### `dpkg` source package: `glibc=2.38-1ubuntu6.3`

Binary Packages:

- `libc-bin=2.38-1ubuntu6.3`
- `libc-dev-bin=2.38-1ubuntu6.3`
- `libc-devtools=2.38-1ubuntu6.3`
- `libc6:amd64=2.38-1ubuntu6.3`
- `libc6-dev:amd64=2.38-1ubuntu6.3`

Licenses: (parsed from: `/usr/share/doc/libc-bin/copyright`, `/usr/share/doc/libc-dev-bin/copyright`, `/usr/share/doc/libc-devtools/copyright`, `/usr/share/doc/libc6/copyright`, `/usr/share/doc/libc6-dev/copyright`)

- `GFDL-1.3`
- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris glibc=2.38-1ubuntu6.3
'http://archive.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.38-1ubuntu6.3.dsc' glibc_2.38-1ubuntu6.3.dsc 9525 SHA512:344e712b809f055f8c188bb136d0c273a6623e066ed31ab519204edf4bd230365381b5b57b40d99ebe2e88234bda81bac64c95c7f5a2a24f4211faa5772f8a3e
'http://archive.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.38.orig.tar.xz' glibc_2.38.orig.tar.xz 18913712 SHA512:a6dd5e42dcd63d58e2820c783522c8c895890b6e8c8e6c83b025553de0cc77cdf227e7044e431ead98c89c68a9ce4dd63509b47e647775fb2075f011849c1900
'http://archive.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.38.orig.tar.xz.asc' glibc_2.38.orig.tar.xz.asc 833 SHA512:32248467450f4530f8e84c03ea78d8293946e1b1def853eff9fb2cb51106e66cc3b024a254f3c2fabd2634f8192bd14e7df00c317f4230860d702c4d9ec7a01e
'http://archive.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.38-1ubuntu6.3.debian.tar.xz' glibc_2.38-1ubuntu6.3.debian.tar.xz 466432 SHA512:def9295039770739f035d66aaaacda4fc57f4029aa3b06f95226ca697ca8dd7a21a73e7bdf49625d34057897f3b1a2a8369a74de47f8deb79ac797fdb855c7e4
```

### `dpkg` source package: `gmp=2:6.3.0+dfsg-2ubuntu4`

Binary Packages:

- `libgmp10:amd64=2:6.3.0+dfsg-2ubuntu4`

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
$ apt-get source -qq --print-uris gmp=2:6.3.0+dfsg-2ubuntu4
'http://archive.ubuntu.com/ubuntu/pool/main/g/gmp/gmp_6.3.0%2bdfsg-2ubuntu4.dsc' gmp_6.3.0+dfsg-2ubuntu4.dsc 2362 SHA512:752c712621f802d56b22b8031f1449ac69d8c271eb7d1f69cc2feeb85cf31849ece2ae488969e9502b9538f75343244bcbc622bbbc7a909d57eae2bf48c5e754
'http://archive.ubuntu.com/ubuntu/pool/main/g/gmp/gmp_6.3.0%2bdfsg.orig.tar.xz' gmp_6.3.0+dfsg.orig.tar.xz 1870556 SHA512:a422b29024464aeb26c69f64be1bc37407d74e0290f44f67fc040fe38b97f3eb7aa6ba8380722ef36cac39816d1c4f24b771159fb86d5979ef0791dcdef708bc
'http://archive.ubuntu.com/ubuntu/pool/main/g/gmp/gmp_6.3.0%2bdfsg-2ubuntu4.debian.tar.xz' gmp_6.3.0+dfsg-2ubuntu4.debian.tar.xz 38680 SHA512:79fc5aaa101f7cf4390dc9378e1c9e871b77822473c9ba19f0c4e305fa0e47f417bd7c7da0fdd5e939363ea9d5e111dfb755e7170b81aca038796220d72a8697
```

### `dpkg` source package: `gnupg2=2.2.40-1.1ubuntu1`

Binary Packages:

- `dirmngr=2.2.40-1.1ubuntu1`
- `gnupg=2.2.40-1.1ubuntu1`
- `gnupg-l10n=2.2.40-1.1ubuntu1`
- `gnupg-utils=2.2.40-1.1ubuntu1`
- `gnupg2=2.2.40-1.1ubuntu1`
- `gpg=2.2.40-1.1ubuntu1`
- `gpg-agent=2.2.40-1.1ubuntu1`
- `gpg-wks-client=2.2.40-1.1ubuntu1`
- `gpg-wks-server=2.2.40-1.1ubuntu1`
- `gpgconf=2.2.40-1.1ubuntu1`
- `gpgsm=2.2.40-1.1ubuntu1`
- `gpgv=2.2.40-1.1ubuntu1`

Licenses: (parsed from: `/usr/share/doc/dirmngr/copyright`, `/usr/share/doc/gnupg/copyright`, `/usr/share/doc/gnupg-l10n/copyright`, `/usr/share/doc/gnupg-utils/copyright`, `/usr/share/doc/gnupg2/copyright`, `/usr/share/doc/gpg/copyright`, `/usr/share/doc/gpg-agent/copyright`, `/usr/share/doc/gpg-wks-client/copyright`, `/usr/share/doc/gpg-wks-server/copyright`, `/usr/share/doc/gpgconf/copyright`, `/usr/share/doc/gpgsm/copyright`, `/usr/share/doc/gpgv/copyright`)

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
$ apt-get source -qq --print-uris gnupg2=2.2.40-1.1ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnupg2/gnupg2_2.2.40-1.1ubuntu1.dsc' gnupg2_2.2.40-1.1ubuntu1.dsc 3920 SHA512:c2cfd636e9bdfc8fe19d9213597325782fe15bd228d0e7d601f18c37d23c2be81c62337621bb835d2defc85feade8f67c4a7f680902d32c77f112cfa2258c7bb
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnupg2/gnupg2_2.2.40.orig.tar.bz2' gnupg2_2.2.40.orig.tar.bz2 7301631 SHA512:4c2f5fbf37ba6fbad0045aad23129186963010c673ea0b81801adc4f98efe14d6c7228e22815b6b26307c1fe5bb51cd088aa6a0f06a9325d3c021849ef81c594
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnupg2/gnupg2_2.2.40.orig.tar.bz2.asc' gnupg2_2.2.40.orig.tar.bz2.asc 228 SHA512:50e8abae322430bf4d3230d0291ca519663a1397fe0d0b8df29076808504b5fea2b984952d6dc51ecc239c12af8ecd5d93b88dd1c6bc0babf0b48a5a840b8ada
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnupg2/gnupg2_2.2.40-1.1ubuntu1.debian.tar.xz' gnupg2_2.2.40-1.1ubuntu1.debian.tar.xz 65264 SHA512:1efaad1ebfcda85888670e613bb4488ff2ad773190a593f4d2ac298e731a5641e84bfc2c0dba4b5fd8f1af455212a388b99f903dfc770a772d45b4ccaafcb2e1
```

### `dpkg` source package: `gnutls28=3.8.1-4ubuntu1.3`

Binary Packages:

- `libgnutls30:amd64=3.8.1-4ubuntu1.3`

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
$ apt-get source -qq --print-uris gnutls28=3.8.1-4ubuntu1.3
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.8.1-4ubuntu1.3.dsc' gnutls28_3.8.1-4ubuntu1.3.dsc 3346 SHA512:6315b8c521aa79d991f956802a7e8c1e72b7756c4f3fcb63a2f3f9c62bed7571311b144828e855910e678dd78a80bc03e9eabcbc84f4e5606e8c9d9a420519b9
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.8.1.orig.tar.xz' gnutls28_3.8.1.orig.tar.xz 6447056 SHA512:22e78db86b835843df897d14ad633d8a553c0f9b1389daa0c2f864869c6b9ca889028d434f9552237dc4f1b37c978fbe0cce166e3768e5d4e8850ff69a6fc872
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.8.1.orig.tar.xz.asc' gnutls28_3.8.1.orig.tar.xz.asc 996 SHA512:ad42a077718a91b82959ee7ed8282b69e73825c70c5c60eb4a1f87aab055dee2ac74a03f489d5f11c2094ec6ac01ea44c0daffb61cb4daae714dcaf5ea89ecd0
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.8.1-4ubuntu1.3.debian.tar.xz' gnutls28_3.8.1-4ubuntu1.3.debian.tar.xz 84868 SHA512:a012611a3fc5864d2803ac1d1179e660e215caf129c5279875370ac614932cfefc025181ded13236b59e9aefcea64cfe3d3a4049d4fe4f6f0e3152016cc476e3
```

### `dpkg` source package: `gpm=1.20.7-10build1`

Binary Packages:

- `libgpm2:amd64=1.20.7-10build1`

Licenses: (parsed from: `/usr/share/doc/libgpm2/copyright`)

- `GPL-2`
- `GPL-2.0+`
- `GPL-3`
- `GPL-3.0+`

Source:

```console
$ apt-get source -qq --print-uris gpm=1.20.7-10build1
'http://archive.ubuntu.com/ubuntu/pool/main/g/gpm/gpm_1.20.7-10build1.dsc' gpm_1.20.7-10build1.dsc 2019 SHA512:d59551a2b4d87e6a9ebac57b7a68292234926445ef7486f1bcc0c708ab99978f7e348edf2cf8719c7f454ff9092d7545220f443caba1799b3e98e06cbcd3ff83
'http://archive.ubuntu.com/ubuntu/pool/main/g/gpm/gpm_1.20.7.orig.tar.gz' gpm_1.20.7.orig.tar.gz 855027 SHA512:39b6ec1d78c03981a2298ce8fd92987dd7e070c767d8135bbb94d6f5fea2d1b9c75b39806c3e99618e2c40cbc29d1c1e4177714ce63ac86b8d9e7e07234feb54
'http://archive.ubuntu.com/ubuntu/pool/main/g/gpm/gpm_1.20.7-10build1.debian.tar.xz' gpm_1.20.7-10build1.debian.tar.xz 84844 SHA512:0841501055de50e7549924c60d7c975e23f300eb4d192e4ee46505b3dc37ea3d74b4a5a56805dab7b478575c4775945c22450503a035a209a75d5aa1654670ab
```

### `dpkg` source package: `grep=3.11-2`

Binary Packages:

- `grep=3.11-2`

Licenses: (parsed from: `/usr/share/doc/grep/copyright`)

- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris grep=3.11-2
'http://archive.ubuntu.com/ubuntu/pool/main/g/grep/grep_3.11-2.dsc' grep_3.11-2.dsc 1618 SHA512:faf7da2c0e441300787bc4ad52188bff8d667079867df26dcd86a54a9e5d6d919938c1fb3b51fd7125f761cfdba91020c2797562687943324cb53566d1629eb2
'http://archive.ubuntu.com/ubuntu/pool/main/g/grep/grep_3.11.orig.tar.xz' grep_3.11.orig.tar.xz 1703776 SHA512:f254a1905a08c8173e12fbdd4fd8baed9a200217fba9d7641f0d78e4e002c1f2a621152d67027d9b25f0bb2430898f5233dc70909d8464fd13d7dd9298e65c42
'http://archive.ubuntu.com/ubuntu/pool/main/g/grep/grep_3.11.orig.tar.xz.asc' grep_3.11.orig.tar.xz.asc 833 SHA512:487aba063373ca0594c519991f19b2a6a33b3da0d74735c890f3828fd0880e7e6f64495d2c8f9efa5da53d1eb2d446609bab2399a4b89dcb4510a632e31ffb54
'http://archive.ubuntu.com/ubuntu/pool/main/g/grep/grep_3.11-2.debian.tar.xz' grep_3.11-2.debian.tar.xz 20388 SHA512:25ebdf45c3268d3520fd650aba4c2e845c7aec7f59740d3fadcef939ae51b4d69fb8788253a648bbf8c3be315369d59a814c18307b6ac1ea4d20458241bd1860
```

### `dpkg` source package: `gzip=1.12-1ubuntu1`

Binary Packages:

- `gzip=1.12-1ubuntu1`

Licenses: (parsed from: `/usr/share/doc/gzip/copyright`)

- `FSF-manpages`
- `GFDL-1.3+-no-invariant`
- `GFDL-3`
- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris gzip=1.12-1ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/g/gzip/gzip_1.12-1ubuntu1.dsc' gzip_1.12-1ubuntu1.dsc 2303 SHA512:8b6f5ada04f3dbcb891f9af31a28cf1a161392f98f78724088752981a3453474b32ad2f7312c683bd65fba6b6fe14b26bbacbe462a3204acfe614f7c0f217ff5
'http://archive.ubuntu.com/ubuntu/pool/main/g/gzip/gzip_1.12.orig.tar.xz' gzip_1.12.orig.tar.xz 825548 SHA512:116326fe991828227de150336a0c016f4fe932dfbb728a16b4a84965256d9929574a4f5cfaf3cf6bb4154972ef0d110f26ab472c93e62ec9a5fd7a5d65abea24
'http://archive.ubuntu.com/ubuntu/pool/main/g/gzip/gzip_1.12.orig.tar.xz.asc' gzip_1.12.orig.tar.xz.asc 833 SHA512:1f4702797f7c5f1873c2f9c2f6210ba23824455d17ee82f50f0bf24240ed5bdf0090cf85338ccf76ba82422f8b4ad3a329d8bbf1350cb094d7bd61aa45550397
'http://archive.ubuntu.com/ubuntu/pool/main/g/gzip/gzip_1.12-1ubuntu1.debian.tar.xz' gzip_1.12-1ubuntu1.debian.tar.xz 19796 SHA512:247ee91f2d67935a809248c8134789a57e13db3534e7d7c5e0ab543a4b1024cc39c29b3fb2fc5805b42f87004187601e642c45fd1f51baa80b21441786e64da7
```

### `dpkg` source package: `hostname=3.23+nmu1ubuntu1`

Binary Packages:

- `hostname=3.23+nmu1ubuntu1`

Licenses: (parsed from: `/usr/share/doc/hostname/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris hostname=3.23+nmu1ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/h/hostname/hostname_3.23%2bnmu1ubuntu1.dsc' hostname_3.23+nmu1ubuntu1.dsc 1567 SHA512:95f3a3ae2197f342fbac41664b2aca64bac415a9b7675364f256512207fadfd2476786e186781c05724fcf0b1d37cbfa1560c6f363e27495e5d35efea92483c4
'http://archive.ubuntu.com/ubuntu/pool/main/h/hostname/hostname_3.23%2bnmu1ubuntu1.tar.xz' hostname_3.23+nmu1ubuntu1.tar.xz 13124 SHA512:c14a9a7e39812ba6be3a3ed62f1e95815437e78b8edfa4a0daa7fc5939a22b522df51eed30ef96940082cae95a9a53f1988e9740d9b423b728dfa5995f92937d
```

### `dpkg` source package: `icu=72.1-3ubuntu3`

Binary Packages:

- `icu-devtools=72.1-3ubuntu3`
- `libicu-dev:amd64=72.1-3ubuntu3`
- `libicu72:amd64=72.1-3ubuntu3`

Licenses: (parsed from: `/usr/share/doc/icu-devtools/copyright`, `/usr/share/doc/libicu-dev/copyright`, `/usr/share/doc/libicu72/copyright`)

- `GPL-3`
- `MIT`

Source:

```console
$ apt-get source -qq --print-uris icu=72.1-3ubuntu3
'http://archive.ubuntu.com/ubuntu/pool/main/i/icu/icu_72.1-3ubuntu3.dsc' icu_72.1-3ubuntu3.dsc 2359 SHA512:4345ac6b4fe35e4d9e23100002fa255cc5b569c61f968d047c10bdb6e66eb4bed6d15043af6c80dce613517bea2c9d203b0ded729c47c2dc073fd9eae83d082d
'http://archive.ubuntu.com/ubuntu/pool/main/i/icu/icu_72.1.orig.tar.gz' icu_72.1.orig.tar.gz 26303933 SHA512:848c341b37c0ff077e34a95d92c6200d5aaddd0ee5e06134101a74e04deb08256a5e817c8aefab020986abe810b7827dd7b2169a60dacd250c298870518dcae8
'http://archive.ubuntu.com/ubuntu/pool/main/i/icu/icu_72.1.orig.tar.gz.asc' icu_72.1.orig.tar.gz.asc 659 SHA512:8b5e841a3baa317a13cadf7deb3582a80cfab8e5bdae6bd04612ee7be3006d9acf07b015de01a94990fa350109a3c11e547482e4cb4ca986161cc701a8cd427b
'http://archive.ubuntu.com/ubuntu/pool/main/i/icu/icu_72.1-3ubuntu3.debian.tar.xz' icu_72.1-3ubuntu3.debian.tar.xz 64708 SHA512:31d09726ba3d81aaf7beb8537982187080b2c61587ba922bdceb4c80499e415f9eaf86d2418e7fc4956c7369a7970e58d53cf3694c042639b441d8cb88aa66c8
```

### `dpkg` source package: `init-system-helpers=1.65.2ubuntu1`

Binary Packages:

- `init-system-helpers=1.65.2ubuntu1`

Licenses: (parsed from: `/usr/share/doc/init-system-helpers/copyright`)

- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris init-system-helpers=1.65.2ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/i/init-system-helpers/init-system-helpers_1.65.2ubuntu1.dsc' init-system-helpers_1.65.2ubuntu1.dsc 2314 SHA512:37f649551c147cf7072b21d2c458ee7d9ca912ae7bca9980b49a53f4530011e65867e8ad5fedf42b6b393855454016340a7c6fee19b7224d600f52a0154afa15
'http://archive.ubuntu.com/ubuntu/pool/main/i/init-system-helpers/init-system-helpers_1.65.2ubuntu1.tar.xz' init-system-helpers_1.65.2ubuntu1.tar.xz 47788 SHA512:ec563fd3e71adf007a442911d1d8ea8b13f3c99229b28ecd1da8df6a895683049287d7f4d42ecf1b5574b6ce3fb124259522b777e76a5c33f18f80a0fad7a251
```

### `dpkg` source package: `jansson=2.14-2`

Binary Packages:

- `libjansson4:amd64=2.14-2`

Licenses: (parsed from: `/usr/share/doc/libjansson4/copyright`)

- `Expat`

Source:

```console
$ apt-get source -qq --print-uris jansson=2.14-2
'http://archive.ubuntu.com/ubuntu/pool/main/j/jansson/jansson_2.14-2.dsc' jansson_2.14-2.dsc 1980 SHA512:e1c579cae00db3083448345690769411d1aaf2607ea956fba24542d5427f6e0ed6e2b7159b32d617d708e77b986a61c3c938f2e956e317a253c2ff10be8130f1
'http://archive.ubuntu.com/ubuntu/pool/main/j/jansson/jansson_2.14.orig.tar.gz' jansson_2.14.orig.tar.gz 141500 SHA512:c56e2e8d18819e3f5caa46edd4819694a240aeb3524a6f9d9f4465edf65b183d1870bd5d256cdd378d411a52979121369b951406fdf7bf323db5c30001fa1bc4
'http://archive.ubuntu.com/ubuntu/pool/main/j/jansson/jansson_2.14-2.debian.tar.xz' jansson_2.14-2.debian.tar.xz 5428 SHA512:90520e3b81066b2441b0ac88d49c1bd7f55e1ae7727176cd8f397ed8cce88c6975c9a9bbbcc1f244ae83773e35695643d1dfab4136b19c624871fd7cbe3832bb
```

### `dpkg` source package: `jbigkit=2.1-6.1ubuntu1`

Binary Packages:

- `libjbig0:amd64=2.1-6.1ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libjbig0/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris jbigkit=2.1-6.1ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/j/jbigkit/jbigkit_2.1-6.1ubuntu1.dsc' jbigkit_2.1-6.1ubuntu1.dsc 2207 SHA512:0559e2551f3ca1106e89a7f2482a17c50ebe886b8d699f1387b6ca032408cdd7976f78871a2da6e16a310035ba1e709f75f0399f1305c098aebed84883e3a816
'http://archive.ubuntu.com/ubuntu/pool/main/j/jbigkit/jbigkit_2.1.orig.tar.gz' jbigkit_2.1.orig.tar.gz 438710 SHA512:c4127480470ef90db1ef3bd2caa444df10b50ed8df0bc9997db7612cb48b49278baf44965028f1807a21028eb965d677e015466306b44683c4ec75a23e1922cf
'http://archive.ubuntu.com/ubuntu/pool/main/j/jbigkit/jbigkit_2.1-6.1ubuntu1.debian.tar.xz' jbigkit_2.1-6.1ubuntu1.debian.tar.xz 11092 SHA512:74ea1ca6d2e5b4e624382c60ef08dcfc91a2babb0433747dd464283459989d5441f77df2878462d7ff15b6cd98dac530b0483bef0be08062e175bc24c8e4374a
```

### `dpkg` source package: `keyutils=1.6.3-2`

Binary Packages:

- `libkeyutils1:amd64=1.6.3-2`

Licenses: (parsed from: `/usr/share/doc/libkeyutils1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2`
- `LGPL-2+`

Source:

```console
$ apt-get source -qq --print-uris keyutils=1.6.3-2
'http://archive.ubuntu.com/ubuntu/pool/main/k/keyutils/keyutils_1.6.3-2.dsc' keyutils_1.6.3-2.dsc 2079 SHA512:25176970cfeccf59c7c798042029ff78150ad2f8a1a6871aabd34c8d8bf9cb7c7ef2b1cfe78cbd7b61207a21512de703bee26d580b2a2bc62acc4722ba6e186c
'http://archive.ubuntu.com/ubuntu/pool/main/k/keyutils/keyutils_1.6.3.orig.tar.gz' keyutils_1.6.3.orig.tar.gz 137022 SHA512:f65965b8566037078b8eeffa66c6fdbe121c8c2bea7fa5bce04cf7ba5ccc50d5b48e51f4a67ca91e4d5d9a12469e7e3eb3036c920ab25e3feba6e93b4c149cf9
'http://archive.ubuntu.com/ubuntu/pool/main/k/keyutils/keyutils_1.6.3-2.debian.tar.xz' keyutils_1.6.3-2.debian.tar.xz 13196 SHA512:cda54c621a40334005373a1dc90f93f3e1f6b5c5e0cbbd6299312526e77cc05e4e2eed4473e7e7f06847b5b47a7f2aee377362540ee48c9f38a5f5cf37931132
```

### `dpkg` source package: `krb5=1.20.1-3ubuntu1`

Binary Packages:

- `krb5-locales=1.20.1-3ubuntu1`
- `libgssapi-krb5-2:amd64=1.20.1-3ubuntu1`
- `libk5crypto3:amd64=1.20.1-3ubuntu1`
- `libkrb5-3:amd64=1.20.1-3ubuntu1`
- `libkrb5support0:amd64=1.20.1-3ubuntu1`

Licenses: (parsed from: `/usr/share/doc/krb5-locales/copyright`, `/usr/share/doc/libgssapi-krb5-2/copyright`, `/usr/share/doc/libk5crypto3/copyright`, `/usr/share/doc/libkrb5-3/copyright`, `/usr/share/doc/libkrb5support0/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris krb5=1.20.1-3ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.20.1-3ubuntu1.dsc' krb5_1.20.1-3ubuntu1.dsc 3920 SHA512:c9dfc58de924bef20e55cd82232a776e555c6c3f251929c169511d10c62844f4a8fe7f44cc73c39faaa095bdea567c1fcfd6a3ace63bb49b626676650c65553a
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.20.1.orig.tar.gz' krb5_1.20.1.orig.tar.gz 8661660 SHA512:6f57479f13f107cd84f30de5c758eb6b9fc59171329c13e5da6073b806755f8d163eb7bd84767ea861ad6458ea0c9eeb00ee044d3bcad01ef136e9888564b6a2
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.20.1.orig.tar.gz.asc' krb5_1.20.1.orig.tar.gz.asc 833 SHA512:1d3312bd67581e07adfdadf2c5fe394179631d8add8bd075efefe982a0de22369004e60a14422d426382c8c591e4181b9897088afe9d4e86f0b5a97e5954c67a
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.20.1-3ubuntu1.debian.tar.xz' krb5_1.20.1-3ubuntu1.debian.tar.xz 100536 SHA512:39ca9dfafb381bd346d5d63a1915b94b85a57d3e6f4803c4ac34d5ab9541c0f18153508bb99791330848a0208454b006c09db3599ff33b2b6bb6e02f61d26062
```

### `dpkg` source package: `lerc=4.0.0+ds-2ubuntu2`

Binary Packages:

- `liblerc4:amd64=4.0.0+ds-2ubuntu2`

Licenses: (parsed from: `/usr/share/doc/liblerc4/copyright`)

- `Apache-2.0`

Source:

```console
$ apt-get source -qq --print-uris lerc=4.0.0+ds-2ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/l/lerc/lerc_4.0.0%2bds-2ubuntu2.dsc' lerc_4.0.0+ds-2ubuntu2.dsc 1675 SHA512:d055e23e3b39fb7889c73dcd9a13ce2409d00be88e9a85776260c206162569ed85e2e5024d75c3d49ec09f019f5afa9cbd08b6a582150bce321b10182817673e
'http://archive.ubuntu.com/ubuntu/pool/main/l/lerc/lerc_4.0.0%2bds.orig.tar.xz' lerc_4.0.0+ds.orig.tar.xz 348140 SHA512:d5539360fa92f40319466fea73a66d0d03aedff886fb75985bfcaeeb77ef516b9fa24b8d83da09c114bf6090bbd68e64d9ac2649a19315895134fa86023478e1
'http://archive.ubuntu.com/ubuntu/pool/main/l/lerc/lerc_4.0.0%2bds-2ubuntu2.debian.tar.xz' lerc_4.0.0+ds-2ubuntu2.debian.tar.xz 7960 SHA512:34d2a1d2aace8916d208bec39143556fc3098e16d026a4d391a6c16bae8c61a2ec4323f61e9a26bff0470c7c9c33088103c5ee054e81f446629f3e32f9e5a96c
```

### `dpkg` source package: `less=590-2ubuntu0.23.10.2`

Binary Packages:

- `less=590-2ubuntu0.23.10.2`

Licenses: (parsed from: `/usr/share/doc/less/copyright`)

- `GPL-3`
- `GPL-3+`
- `Less`
- `Less,`
- `Spencer-86`
- `X11`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris less=590-2ubuntu0.23.10.2
'http://archive.ubuntu.com/ubuntu/pool/main/l/less/less_590-2ubuntu0.23.10.2.dsc' less_590-2ubuntu0.23.10.2.dsc 2213 SHA512:08859c844305e1658564b38926574a37ab89dff8330714365f2b5d62be27ad75e0ab1961f9861bd5f3cfed0d5690e24c7e6b9c30f8c67dcec5c1d1d88331175f
'http://archive.ubuntu.com/ubuntu/pool/main/l/less/less_590.orig.tar.gz' less_590.orig.tar.gz 352574 SHA512:426fa5840fd43c17bd5a452ad35ad24f2d6684623c6914403fd0059af62266bf2138e6828c7d73a1cef26a736c0d2b8ed4ab180eea8297281dae79a4228eb903
'http://archive.ubuntu.com/ubuntu/pool/main/l/less/less_590.orig.tar.gz.asc' less_590.orig.tar.gz.asc 163 SHA512:2dda1f8872db0af8eae5130275a789cb3d8f8973794259282ee6f65510db62a916ddf3395c44766302e8894862db5df700159df1e0c3a8e42940b8079d3d9421
'http://archive.ubuntu.com/ubuntu/pool/main/l/less/less_590-2ubuntu0.23.10.2.debian.tar.xz' less_590-2ubuntu0.23.10.2.debian.tar.xz 23280 SHA512:00f5e65d4103a532c57899dbf7b0a967d4bffaac81337406c81f9c16d6fad8ae13353067f1fb32aca348f7548890ea4ed2c18860f779218de3e7f032b776584c
```

### `dpkg` source package: `libassuan=2.5.6-1`

Binary Packages:

- `libassuan0:amd64=2.5.6-1`

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
'http://archive.ubuntu.com/ubuntu/pool/main/liba/libassuan/libassuan_2.5.6-1.dsc' libassuan_2.5.6-1.dsc 1997 SHA512:0a850d34564d555a25b067f6a60ab49a4e6dd07b5bf9a1cac175fbde3c1cf1499783d2a1c7de1464f2deacddf5b2ee4f94c47140ea0c920f731e961f8c45eccc
'http://archive.ubuntu.com/ubuntu/pool/main/liba/libassuan/libassuan_2.5.6.orig.tar.bz2' libassuan_2.5.6.orig.tar.bz2 577012 SHA512:dcca942d222a2c226a7e34ba7988ee0c3c55bd6032166eb472caf2053db89aeeea7a40e93d8c2887c7ee73c5f838e8b0725e8cfb595accc1606646559362f7ee
'http://archive.ubuntu.com/ubuntu/pool/main/liba/libassuan/libassuan_2.5.6.orig.tar.bz2.asc' libassuan_2.5.6.orig.tar.bz2.asc 228 SHA512:aaa1222607320c260d7339a95cca6532947782520b07df3198a5a228129e0247b87f6f3b6fea17590147fbc7345ea36bfa8da45116d3d85c6fc2d4a3df0f629b
'http://archive.ubuntu.com/ubuntu/pool/main/liba/libassuan/libassuan_2.5.6-1.debian.tar.xz' libassuan_2.5.6-1.debian.tar.xz 14284 SHA512:6cb39b7745e1f4312f48662821ddfc92247574e545c75456e655e938ee72a419749e82251a7bcdbb29c4145e8c2c65e62aaa3f08cca9b3993c2548d4ac68be85
```

### `dpkg` source package: `libbsd=0.11.7-4`

Binary Packages:

- `libbsd0:amd64=0.11.7-4`

Licenses: (parsed from: `/usr/share/doc/libbsd0/copyright`)

- `BSD-2-clause`
- `BSD-2-clause-NetBSD`
- `BSD-2-clause-author`
- `BSD-2-clause-verbatim`
- `BSD-3-clause`
- `BSD-3-clause-John-Birrell`
- `BSD-3-clause-Regents`
- `BSD-3-clause-author`
- `BSD-4-clause-Niels-Provos`
- `Beerware`
- `Expat`
- `ISC`
- `ISC-Original`
- `libutil-David-Nugent`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris libbsd=0.11.7-4
'http://archive.ubuntu.com/ubuntu/pool/main/libb/libbsd/libbsd_0.11.7-4.dsc' libbsd_0.11.7-4.dsc 2350 SHA512:9fc370950b1421a0ec801f1075fcf2d03d604f77a8f562c0e8647e0b68f821f9b6d0317b565f4db700fd1555aecdd6a3d66087b55e9a1944ffaea81de032a648
'http://archive.ubuntu.com/ubuntu/pool/main/libb/libbsd/libbsd_0.11.7.orig.tar.xz' libbsd_0.11.7.orig.tar.xz 418508 SHA512:51fda4724f41dd8a4628afd58c21236a7588d9045e337e06eeabf83805a9aaaa53705441ca901ad11f1c65f18e881523bdc97721a7d3d6a5cced27f2450d09a2
'http://archive.ubuntu.com/ubuntu/pool/main/libb/libbsd/libbsd_0.11.7.orig.tar.xz.asc' libbsd_0.11.7.orig.tar.xz.asc 833 SHA512:bdcce69ee261039900896c5be48659f1b6b809f3a6e8a5220aac30a6687926ac29e478a3ea737727d077d6575ee11b86eed896932568fdd261a9aaeb46d695b6
'http://archive.ubuntu.com/ubuntu/pool/main/libb/libbsd/libbsd_0.11.7-4.debian.tar.xz' libbsd_0.11.7-4.debian.tar.xz 21596 SHA512:24875c5a3b360ff1e2b0bb974e3b99f5bbd3b64a96f7948f94f2afc8c762d5e589fdfae2e81dc021bbc5cab6dbb63586c9cab9676067e4bd6afa5cd6b3612204
```

### `dpkg` source package: `libcap-ng=0.8.3-1build2`

Binary Packages:

- `libcap-ng0:amd64=0.8.3-1build2`

Licenses: (parsed from: `/usr/share/doc/libcap-ng0/copyright`)

- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris libcap-ng=0.8.3-1build2
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap-ng/libcap-ng_0.8.3-1build2.dsc' libcap-ng_0.8.3-1build2.dsc 2231 SHA512:0c6e48e6ef5e64cdf97cdb7f16a0cb8fd35e9928ac50f5e0d17035a93906914142c08a31f804a2de15364eeb87278c65ae3b2807cd01bd8b7b6c2e034124c021
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap-ng/libcap-ng_0.8.3.orig.tar.gz' libcap-ng_0.8.3.orig.tar.gz 455383 SHA512:0ef9bc7bc6b7b59991f43b79aa6cde3e8d2c22c4b9ced2af8deae501e01d51e893033d109cb8aa0fdcba190140110993089245346334d7b114d18f1bb1b55b97
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap-ng/libcap-ng_0.8.3-1build2.debian.tar.xz' libcap-ng_0.8.3-1build2.debian.tar.xz 10604 SHA512:bec471e45d3550a498e62c66ffe76e76fb799c6b1634b873ddcff61e7ecb7da906634c76323485452e0df85faa2ba530ba1608079e84413ab38b3365bda0a053
```

### `dpkg` source package: `libcap2=1:2.66-4ubuntu1`

Binary Packages:

- `libcap2:amd64=1:2.66-4ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libcap2/copyright`)

- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris libcap2=1:2.66-4ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap2/libcap2_2.66-4ubuntu1.dsc' libcap2_2.66-4ubuntu1.dsc 2336 SHA512:884095371ffcf06c2e1b5f2a5e9e68f369558767e969c22aeec741a5b57e8cc91ee0311876d165839b55211c93a36c1e1121ce9faaf8d48aa13013eebb0179f4
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap2/libcap2_2.66.orig.tar.xz' libcap2_2.66.orig.tar.xz 181592 SHA512:ac005b622f6e065f30ce282a5c87240e7b9da75366ee537aa4835bc501b44bc242c10a4ba4dc070e2415fc7f635d1c3c4e45fbeeaf962cf7973dda82bf6377f0
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap2/libcap2_2.66-4ubuntu1.debian.tar.xz' libcap2_2.66-4ubuntu1.debian.tar.xz 22076 SHA512:1f19fc5203de495bf3edb52249bcd6ea14a30b521f223cf75171b6b521c370bf8a21def958307d1712d6ad187b938d2a684ee400279f100c0836f24c7fab99cf
```

### `dpkg` source package: `libcbor=0.8.0-2ubuntu1`

Binary Packages:

- `libcbor0.8:amd64=0.8.0-2ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libcbor0.8/copyright`)

- `Apache-2.0`
- `Expat`

Source:

```console
$ apt-get source -qq --print-uris libcbor=0.8.0-2ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcbor/libcbor_0.8.0-2ubuntu1.dsc' libcbor_0.8.0-2ubuntu1.dsc 2196 SHA512:3dae3506bfaeee3e945c6a500be3f9f7a0de7f10f2924304dc933cc98c7b0f8be5618c14690f92d2c0d64e3c6f29eb5e8ba09185d82452a0d071e2355daff917
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcbor/libcbor_0.8.0.orig.tar.gz' libcbor_0.8.0.orig.tar.gz 267044 SHA512:694d2d3a78d80072f96e0afb73590ca1f3572e41d2117330ef4313ed06271743b048d3ba3259c6ffe9a802d5e441379d0e54787d1d42fed08dc81ac4f06c6dbc
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcbor/libcbor_0.8.0-2ubuntu1.debian.tar.xz' libcbor_0.8.0-2ubuntu1.debian.tar.xz 5472 SHA512:6c60981075bf118fd7a5df52cbc0d53be00abcc0257b97c3527409d37d400019787ed285d488938061ece9ac0423a936dc190c389ad7ae41a78bc573e6ceab4d
```

### `dpkg` source package: `libdeflate=1.18-1`

Binary Packages:

- `libdeflate0:amd64=1.18-1`

Licenses: (parsed from: `/usr/share/doc/libdeflate0/copyright`)

- `Expat`

Source:

```console
$ apt-get source -qq --print-uris libdeflate=1.18-1
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libdeflate/libdeflate_1.18-1.dsc' libdeflate_1.18-1.dsc 2196 SHA512:824d28b3bafc78541768956048eeca66e5b35717508295ca18700b52a7293c4f2e3e0acea82de204e0261963ca2d88236706268397bec3b30978ab21a31aa7a0
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libdeflate/libdeflate_1.18.orig.tar.gz' libdeflate_1.18.orig.tar.gz 184924 SHA512:8a60fa5850f323389370f931579f85a094a35b3db334f2a2afa61bee39ecebc797e93c6fe5deb4178e19d83a1427533975dba6c05ce0b1db88b43c9268d09124
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libdeflate/libdeflate_1.18-1.debian.tar.xz' libdeflate_1.18-1.debian.tar.xz 4756 SHA512:aa72680eec89c930c824029cfba0195365df3d8df142be76d90180af081d068860fc3a1f5d8fe0e3696c5b317d6c41ccc7fe2b891af0c7c75eb4c79b55c15093
```

### `dpkg` source package: `libedit=3.1-20221030-2`

Binary Packages:

- `libedit2:amd64=3.1-20221030-2`

Licenses: (parsed from: `/usr/share/doc/libedit2/copyright`)

- `BSD-3-clause`

Source:

```console
$ apt-get source -qq --print-uris libedit=3.1-20221030-2
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libedit/libedit_3.1-20221030-2.dsc' libedit_3.1-20221030-2.dsc 2281 SHA512:e3db9cccd742891543df891407449d207b14b392c1c1cc821c63fe3da51c9ecffe5954687e6ad088e6141f0b198be6716456c7370c7b5a49b7223654cf8669ae
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libedit/libedit_3.1-20221030.orig.tar.gz' libedit_3.1-20221030.orig.tar.gz 533261 SHA512:41eb46feaffa909e8790b9a9e304d5246e82ab366721196126a923d68b4d4964d0a433fe238f9d5e0a00aefb5c8cb66132150792929a793785ad091d91016f97
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libedit/libedit_3.1-20221030-2.debian.tar.xz' libedit_3.1-20221030-2.debian.tar.xz 16488 SHA512:ee07a5eda1c62e469a3d3680028c4d21892a7fc76c5259378a9218ae043120faa78df537d61cf1ee35dbbda3f94b093dae1d8143d8f5249ff9d5948faf82fb22
```

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
'http://archive.ubuntu.com/ubuntu/pool/main/libe/liberror-perl/liberror-perl_0.17029-2.dsc' liberror-perl_0.17029-2.dsc 2085 SHA512:9b469f24ebdd65c5aacfa41b7099cb1fec5214d98e6e0d793d55a56bc0f0edae8f2ad3c0e09f44558249ff5456f05704c213d7e84661e0e4d774e644d3fd405a
'http://archive.ubuntu.com/ubuntu/pool/main/libe/liberror-perl/liberror-perl_0.17029.orig.tar.gz' liberror-perl_0.17029.orig.tar.gz 33304 SHA512:266ba1feff897c1d162e69a83e595cb40da9a6e1d8b10cc5531626eff392c6da94be03ba722c74827fc2ea0d9d1c1e62e824d9021e098b700db65dd0b3acbd0a
'http://archive.ubuntu.com/ubuntu/pool/main/libe/liberror-perl/liberror-perl_0.17029-2.debian.tar.xz' liberror-perl_0.17029-2.debian.tar.xz 4608 SHA512:beb596444319797a60470e98c14e8e736fd5be9c307ba5482fe96bf77c1382603b1f2a58d68406ecbf2bc5469cab4654645f5469cf059336fef24605b235cb61
```

### `dpkg` source package: `libffi=3.4.4-1`

Binary Packages:

- `libffi8:amd64=3.4.4-1`

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
$ apt-get source -qq --print-uris libffi=3.4.4-1
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libffi/libffi_3.4.4-1.dsc' libffi_3.4.4-1.dsc 1951 SHA512:cfcf127389ffec7a5a32061cc39c39af23c1d78b113e72598c2e1a76d4f0e5b9d621eda2f59c20beac243f87eb11d459a158bb9e7d3ec37e17b70dc8a298db42
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libffi/libffi_3.4.4.orig.tar.gz' libffi_3.4.4.orig.tar.gz 1362394 SHA512:88680aeb0fa0dc0319e5cd2ba45b4b5a340bc9b4bcf20b1e0613b39cd898f177a3863aa94034d8e23a7f6f44d858a53dcd36d1bb8dee13b751ef814224061889
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libffi/libffi_3.4.4-1.debian.tar.xz' libffi_3.4.4-1.debian.tar.xz 10380 SHA512:6fdf678230a0ce9a6e70eefe20429705a497cb8e710a89a33695381274110bc6c022c80250668d2786e0264b743ae0b6db88550f45aec0485c606c56ce80dad9
```

### `dpkg` source package: `libfido2=1.13.0-1`

Binary Packages:

- `libfido2-1:amd64=1.13.0-1`

Licenses: (parsed from: `/usr/share/doc/libfido2-1/copyright`)

- `BSD-2-clause`
- `ISC`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris libfido2=1.13.0-1
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libfido2/libfido2_1.13.0-1.dsc' libfido2_1.13.0-1.dsc 2588 SHA512:403c7d2e80b175811bc40924e1c36175ea68ce166223596001e822ae7c3cd6364d0f1f01b3a1f08bdf486a99b5c5c91957baf58da8dc35ebaa8c05b024b64f8a
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libfido2/libfido2_1.13.0.orig.tar.gz' libfido2_1.13.0.orig.tar.gz 652777 SHA512:90f8452cee4c9cc72241478e697c5c692ccff5ab27752f2f296c3623ee297d1f80a85a359b4d0656c67790084c116aac921894e762eb52d3a79056e5014c03e7
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libfido2/libfido2_1.13.0.orig.tar.gz.asc' libfido2_1.13.0.orig.tar.gz.asc 228 SHA512:20e2c4ff34d3f4f605d7e73717f8e379e4124e675e9d3c9223e6053a2c80e0e615776f69efa0bc5cb15ed68ea3c5c9e2ec5567c9c183284fe005a071b31a8456
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libfido2/libfido2_1.13.0-1.debian.tar.xz' libfido2_1.13.0-1.debian.tar.xz 52864 SHA512:589525b352e3c18387d27905f99efdc034746abb8d8f22a8579885baadcbd841a543284daa422526da2646f64a2c670dba3c70e3fcf08c30327c74a37fdae0cd
```

### `dpkg` source package: `libgcrypt20=1.10.2-3ubuntu1`

Binary Packages:

- `libgcrypt20:amd64=1.10.2-3ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libgcrypt20/copyright`)

- `GPL-2`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris libgcrypt20=1.10.2-3ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgcrypt20/libgcrypt20_1.10.2-3ubuntu1.dsc' libgcrypt20_1.10.2-3ubuntu1.dsc 2906 SHA512:a77e7d0baa3a658bab8a46e6ced85b82902d7297c5372f973e253664780a49a7c3dd5747d7bf90f8669e947edf81d1dada0c03557836f8e2ee77fd72579b9630
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgcrypt20/libgcrypt20_1.10.2.orig.tar.bz2' libgcrypt20_1.10.2.orig.tar.bz2 3795164 SHA512:3a850baddfe8ffe8b3e96dc54af3fbb9e1dab204db1f06b9b90b8fbbfb7fb7276260cd1e61ba4dde5a662a2385385007478834e62e95f785d2e3d32652adb29e
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgcrypt20/libgcrypt20_1.10.2.orig.tar.bz2.asc' libgcrypt20_1.10.2.orig.tar.bz2.asc 228 SHA512:151ac009da846f4f97fc5f8d936c90da53a69e0824890b860249add4620480ca00e239b8b886f2e071e81095f120cf67c991ae981ac0fb58d56ea011c26957ab
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgcrypt20/libgcrypt20_1.10.2-3ubuntu1.debian.tar.xz' libgcrypt20_1.10.2-3ubuntu1.debian.tar.xz 37508 SHA512:c34fe218a47bdf4fd22b3819473723cdd3b4e75c046c535f2c24e5c6712a5664846f3a15b6438eab08cd3226da6b3963b495e70a12f2ce3ed0cc4bc018c2ba2f
```

### `dpkg` source package: `libgd2=2.3.3-9ubuntu1`

Binary Packages:

- `libgd3:amd64=2.3.3-9ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libgd3/copyright`)

- `BSD-3-clause`
- `GAP~Makefile.in`
- `GAP~configure`
- `GD`
- `GPL-2`
- `GPL-2+`
- `GPL-2+ with Autoconf exception`
- `HPND`
- `MIT`
- `WEBP`
- `XFIG`

Source:

```console
$ apt-get source -qq --print-uris libgd2=2.3.3-9ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgd2/libgd2_2.3.3-9ubuntu1.dsc' libgd2_2.3.3-9ubuntu1.dsc 2312 SHA512:c1647d24a157714f2ab2553a19bdcfbae900564b053b109e409457c5c03d46e86f98336a7235bb43a1e0ea6a10efb0e95d7b7f1976257c28c7cd3d7ce05b58c2
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgd2/libgd2_2.3.3.orig.tar.gz' libgd2_2.3.3.orig.tar.gz 3593182 SHA512:170699c03386a231d2de20868f34405aafda4c03ee69f5590e32d8400e371b73f6f01bda0fd03f1c0c62ac5fee9562b5e6d097a361c809a895dc508a438ded36
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgd2/libgd2_2.3.3-9ubuntu1.debian.tar.xz' libgd2_2.3.3-9ubuntu1.debian.tar.xz 32548 SHA512:8be77c4e887476a18229d52b7043da0ea0aed4a6ebed65090c1f3931403acbf9d18493060619f0783df231459036893ed257d2e5c89e186171716c0583587537
```

### `dpkg` source package: `libgpg-error=1.47-2`

Binary Packages:

- `libgpg-error0:amd64=1.47-2`

Licenses: (parsed from: `/usr/share/doc/libgpg-error0/copyright`)

- `BSD-3-clause`
- `GPL-3`
- `GPL-3+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `g10-permissive`

Source:

```console
$ apt-get source -qq --print-uris libgpg-error=1.47-2
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgpg-error/libgpg-error_1.47-2.dsc' libgpg-error_1.47-2.dsc 2896 SHA512:432611469c1a587b637b0c5d2d714267bf502c5a23f356833dba51f35d41dc77f9656d2230288312be480203900a710c4d05680bf43cbfd763e7c8a086fd2652
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgpg-error/libgpg-error_1.47.orig.tar.bz2' libgpg-error_1.47.orig.tar.bz2 1020862 SHA512:bbb4b15dae75856ee5b1253568674b56ad155524ae29a075cb5b0a7e74c4af685131775c3ea2226fff2f84ef80855e77aa661645d002b490a795c7ae57b66a30
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgpg-error/libgpg-error_1.47.orig.tar.bz2.asc' libgpg-error_1.47.orig.tar.bz2.asc 228 SHA512:babf3a17429aa7ad5d952099ea8d21bb5c9ba1bc74ea46f3027e0293449c32365208a05e141fa0bf033491320679b0b212f49919452f3dc63cce5d7f355d7195
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgpg-error/libgpg-error_1.47-2.debian.tar.xz' libgpg-error_1.47-2.debian.tar.xz 18540 SHA512:1675eb79550e249451dde1035cd875146eb29637f707eb49b8828b20b217b0a4df323e7cabc57fb5a32bbe8667d998cc395a11685432f5d8f48e9d698e96b3de
```

### `dpkg` source package: `libidn2=2.3.4-1`

Binary Packages:

- `libidn2-0:amd64=2.3.4-1`

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
$ apt-get source -qq --print-uris libidn2=2.3.4-1
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libidn2/libidn2_2.3.4-1.dsc' libidn2_2.3.4-1.dsc 1915 SHA512:6c135e607124a4574c43b857a02ae91b3bab4f9a779b13864982d39b07aa16f14381b569706ce4bbad824806a7de748a1e88592214c0806723da1ee33ee5098d
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libidn2/libidn2_2.3.4.orig.tar.gz' libidn2_2.3.4.orig.tar.gz 2083823 SHA512:a6e90ccef56cfd0b37e3333ab3594bb3cec7ca42a138ca8c4f4ce142da208fa792f6c78ca00c01001c2bc02831abcbaf1cf9bcc346a5290fd7b30708f5a462f3
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libidn2/libidn2_2.3.4.orig.tar.gz.asc' libidn2_2.3.4.orig.tar.gz.asc 228 SHA512:d2a575723326ae256a60e3edf7766af65434f716e11f963bb7ac29b6b2ff2872b41684a1bd1c6f3a3921e8a083512eff1faf2b0fc02513095c2bcf3563312fe0
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libidn2/libidn2_2.3.4-1.debian.tar.xz' libidn2_2.3.4-1.debian.tar.xz 16024 SHA512:0a0cffe0896656ccee725ec270b2cd7dad010d2dc1cb53e05fb8f06633567746e752cf86d0c0ab4eccd7535595ed63498340c3b2b3cec3a8a53d3bb7b3b0ac2f
```

### `dpkg` source package: `libjpeg-turbo=2.1.5-2ubuntu1`

Binary Packages:

- `libjpeg-turbo8:amd64=2.1.5-2ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libjpeg-turbo8/copyright`)

- `BSD-3-clause`
- `BSD-BY-LC-NE`
- `Expat`
- `NTP`
- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris libjpeg-turbo=2.1.5-2ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/libj/libjpeg-turbo/libjpeg-turbo_2.1.5-2ubuntu1.dsc' libjpeg-turbo_2.1.5-2ubuntu1.dsc 2506 SHA512:18ba0e5c7adba980760341bc97da11b0249cf6a098dade631edd3ef1cd5f5c01e30f79b3ce556a30ae32a218968b590984cf2b33942b8565bf222d00a42ae417
'http://archive.ubuntu.com/ubuntu/pool/main/libj/libjpeg-turbo/libjpeg-turbo_2.1.5.orig.tar.gz' libjpeg-turbo_2.1.5.orig.tar.gz 2264471 SHA512:20036303fbe5703a5742dc3778cc5deb2eb98d00a9852e7e80ba73c195bba011ec206c090589c482f1153f74505c3fe06d96af00f6beaa65a7fcf7ffaf626fc2
'http://archive.ubuntu.com/ubuntu/pool/main/libj/libjpeg-turbo/libjpeg-turbo_2.1.5-2ubuntu1.debian.tar.xz' libjpeg-turbo_2.1.5-2ubuntu1.debian.tar.xz 108396 SHA512:8ff55c71badcf8bb200b9ec72a76fa15f4e25d8785011f135d2dc4c082d7a0e5cf59ad0f9f12854bffe27a8667a48fa3f3294f627641e611d9b5f0bdae549446
```

### `dpkg` source package: `libjpeg8-empty=8c-2ubuntu11`

Binary Packages:

- `libjpeg8:amd64=8c-2ubuntu11`

Licenses: (parsed from: `/usr/share/doc/libjpeg8/copyright`)

- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libjpeg8-empty=8c-2ubuntu11
'http://archive.ubuntu.com/ubuntu/pool/main/libj/libjpeg8-empty/libjpeg8-empty_8c-2ubuntu11.dsc' libjpeg8-empty_8c-2ubuntu11.dsc 1579 SHA512:345994a54ea05e741e0e6d35f0a7fc39f45c3fc34a995e972ae6b2843baf0b2fcc0bf4726aa7bb86249e39f46a7e23a273d2430d0fcb9bb88f03c6e9d3c912aa
'http://archive.ubuntu.com/ubuntu/pool/main/libj/libjpeg8-empty/libjpeg8-empty_8c-2ubuntu11.tar.gz' libjpeg8-empty_8c-2ubuntu11.tar.gz 1959 SHA512:eb9cec5b6f3fa5e65950b72c14709d33e638b52a2bd2ac2f2297e0edb9e9e224e6da9bbe355e082026b92d980614e8fe40196e4a3ed7cdd560a65f03b138782b
```

### `dpkg` source package: `libksba=1.6.4-2`

Binary Packages:

- `libksba8:amd64=1.6.4-2`

Licenses: (parsed from: `/usr/share/doc/libksba8/copyright`)

- `FSFUL`
- `GPL-3`
- `LGPL-2.1-or-later`

Source:

```console
$ apt-get source -qq --print-uris libksba=1.6.4-2
'http://archive.ubuntu.com/ubuntu/pool/main/libk/libksba/libksba_1.6.4-2.dsc' libksba_1.6.4-2.dsc 2482 SHA512:34051a546f010964a6dfb88731890f495f783f8a1dc54d0295731893f27b8a6170108a49bb00f1a5f3db391ffb29a07bb2d95addcc025376fc076a207e89f430
'http://archive.ubuntu.com/ubuntu/pool/main/libk/libksba/libksba_1.6.4.orig.tar.bz2' libksba_1.6.4.orig.tar.bz2 668445 SHA512:07bc26584d1901b2975a02012d90084e3c247a7aeab56d7bcc7197ef0210ece0c4ffd5cb468b998ef696deadfcfdc5fa5dc367077863926503e8f7a8d06856a5
'http://archive.ubuntu.com/ubuntu/pool/main/libk/libksba/libksba_1.6.4.orig.tar.bz2.asc' libksba_1.6.4.orig.tar.bz2.asc 228 SHA512:f7c53c41927a5bdd3ed4e30ca06b61009ff8506cb6eb5d89c6fe60e23bac8a9bf6d74114c9df5c2c283f4adbf930c6ed916a45a91f4f4f6158e7af23df7b30e2
'http://archive.ubuntu.com/ubuntu/pool/main/libk/libksba/libksba_1.6.4-2.debian.tar.xz' libksba_1.6.4-2.debian.tar.xz 14652 SHA512:3631c4c2777d8120cea117c65cc990d6cadf31e9d7daedde80c640de19c839d1495d0ed42d38a1620e04ed93985da5de875b7f37a83271ee2f81564a6eaf8bd8
```

### `dpkg` source package: `libmd=1.1.0-1`

Binary Packages:

- `libmd0:amd64=1.1.0-1`

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
$ apt-get source -qq --print-uris libmd=1.1.0-1
'http://archive.ubuntu.com/ubuntu/pool/main/libm/libmd/libmd_1.1.0-1.dsc' libmd_1.1.0-1.dsc 2283 SHA512:0838dfa6755a4e0ce750bc31fa7db32e66000ebfae117b92ad7f1b81b89fbfd1e209ad6bf2d5e19df5ef7b5f4d057c39974f4c475626ea69cc93d05d7fd64ceb
'http://archive.ubuntu.com/ubuntu/pool/main/libm/libmd/libmd_1.1.0.orig.tar.xz' libmd_1.1.0.orig.tar.xz 271228 SHA512:5d0da3337038e474fae7377bbc646d17214e72dc848a7aadc157f49333ce7b5ac1456e45d13674bd410ea08477c6115fc4282fed6c8e6a0bf63537a418c0df96
'http://archive.ubuntu.com/ubuntu/pool/main/libm/libmd/libmd_1.1.0.orig.tar.xz.asc' libmd_1.1.0.orig.tar.xz.asc 833 SHA512:b0ff3baa7eedc205ee6f8b844859145fa6922c39e8f62f1e997851a65b2881649b438a37baa5800d140541da6f4dacc9f92a370f945d7461937b8cdedeca1cef
'http://archive.ubuntu.com/ubuntu/pool/main/libm/libmd/libmd_1.1.0-1.debian.tar.xz' libmd_1.1.0-1.debian.tar.xz 8156 SHA512:d5e657388c32afaa86e1ff86f35f354202065534173eadcc7118afefd1a37fc7f9e97a76f121f20ac7be8c6d53b7eeab242f2f52062e6679e4d470b969fcc581
```

### `dpkg` source package: `libnsl=1.3.0-2build2`

Binary Packages:

- `libnsl-dev:amd64=1.3.0-2build2`
- `libnsl2:amd64=1.3.0-2build2`

Licenses: (parsed from: `/usr/share/doc/libnsl-dev/copyright`, `/usr/share/doc/libnsl2/copyright`)

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

Source:

```console
$ apt-get source -qq --print-uris libnsl=1.3.0-2build2
'http://archive.ubuntu.com/ubuntu/pool/main/libn/libnsl/libnsl_1.3.0-2build2.dsc' libnsl_1.3.0-2build2.dsc 2087 SHA512:f13d28f34b0e71b04b5a0313b1cc79cdbe7d5e7f910d649af63b42824654e3cf01c02caa0e68309cb03350a17506e034800af1b1e3ab9af99fb64121c119215c
'http://archive.ubuntu.com/ubuntu/pool/main/libn/libnsl/libnsl_1.3.0.orig.tar.xz' libnsl_1.3.0.orig.tar.xz 321488 SHA512:a5a6c3ccb2d1e724c8c1f65e55dcd09383eb1ae019c55f4c09441eadf23ffbc2196cfad259805b0ac40ddf3a10af0da453e4d739d67d46829c64d0995dab4e55
'http://archive.ubuntu.com/ubuntu/pool/main/libn/libnsl/libnsl_1.3.0-2build2.debian.tar.xz' libnsl_1.3.0-2build2.debian.tar.xz 4868 SHA512:367904106ba925eaa667cc273b37afd052ba795b7ed004cdb501c13dd26b469df971ac10acec2bf57d91fa4839f356c7dcbcd4969914891152588365844ced9a
```

### `dpkg` source package: `libpng1.6=1.6.40-1`

Binary Packages:

- `libpng16-16:amd64=1.6.40-1`

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
$ apt-get source -qq --print-uris libpng1.6=1.6.40-1
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpng1.6/libpng1.6_1.6.40-1.dsc' libpng1.6_1.6.40-1.dsc 2241 SHA512:c0876953715827bf70a28f78ebb6e5ee5834b1a5b2da9179f3876d8cd280c1c84326b7c3366a94a5f5c191a6caff784ecda379b5effba958a4c1d24ca8ca1e62
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpng1.6/libpng1.6_1.6.40.orig.tar.gz' libpng1.6_1.6.40.orig.tar.gz 1520834 SHA512:5f36a145c7d41f1c417d5f4e03be0155dae3499d72e67170acaad92c1af418c0bb6bc508e9b4b27ef4206bf0074cbf74978bade3bff28bc291867b8f8c2a38cf
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpng1.6/libpng1.6_1.6.40-1.debian.tar.xz' libpng1.6_1.6.40-1.debian.tar.xz 31092 SHA512:0bdc1b6be62b824a5af6a3e5bd9cba89207cab9899732cab8bf882ebf83b3137c8724dd6ed1b2d6fc1125959f964c6f2a34c1a803b82ee5127c0f777182fc9d7
```

### `dpkg` source package: `libpsl=0.21.2-1`

Binary Packages:

- `libpsl5:amd64=0.21.2-1`

Licenses: (parsed from: `/usr/share/doc/libpsl5/copyright`)

- `Chromium`
- `MIT`
- `gnulib`

Source:

```console
$ apt-get source -qq --print-uris libpsl=0.21.2-1
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpsl/libpsl_0.21.2-1.dsc' libpsl_0.21.2-1.dsc 1622 SHA512:2bb260d1a03628b819a4b6be2e0c7c0ee51b599a5fd3535c0bb0622831f59d4a491be064708767bf8c395cec598ddc8b01a41c58fab1fd33354c13906224f707
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpsl/libpsl_0.21.2.orig.tar.xz' libpsl_0.21.2.orig.tar.xz 1870352 SHA512:5308feee863b84705246ce303c093e0c9fecd948ab382fd7480e9ea1ca5f72de42fc2c8f70472a97603580a3fd1eb2b552b093d79756e9fe93effba9f25b6aa4
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpsl/libpsl_0.21.2-1.debian.tar.xz' libpsl_0.21.2-1.debian.tar.xz 11940 SHA512:114ab8452d153bcad4e5702d6ef4172e8f5c43d69d3126bc06678135a54ae20bbe3e6c1e83cd2fc9cd8ae3b0add929a04b13cc6841c213687be259a07b558ed5
```

### `dpkg` source package: `libseccomp=2.5.4-1ubuntu3`

Binary Packages:

- `libseccomp2:amd64=2.5.4-1ubuntu3`

Licenses: (parsed from: `/usr/share/doc/libseccomp2/copyright`)

- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libseccomp=2.5.4-1ubuntu3
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libseccomp/libseccomp_2.5.4-1ubuntu3.dsc' libseccomp_2.5.4-1ubuntu3.dsc 2799 SHA512:ed969f1feed2e25afc3e67f09523113a265e10dfe5fbec5e93b088549e5953ab974333e567159d434402e1098ef4f6d305587285aa09eb15514ee594ddffda33
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libseccomp/libseccomp_2.5.4.orig.tar.gz' libseccomp_2.5.4.orig.tar.gz 637228 SHA512:92650bd7d1d48b383f402a536b97a017fd0f6ad1234daf4b938d01c92e8d134a01d2f2dd45fd9e2d025d7556bd1386ec360402145a87f20580c85949d62cea0e
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libseccomp/libseccomp_2.5.4.orig.tar.gz.asc' libseccomp_2.5.4.orig.tar.gz.asc 833 SHA512:10ce632da2762e3b5acb468194b2424d80bab786cc5923a8ee0b0684290282ef2f0a17192680afb36626c82e73a3ba64e73f248ed63cd3e55c3cf8cee4e1e447
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libseccomp/libseccomp_2.5.4-1ubuntu3.debian.tar.xz' libseccomp_2.5.4-1ubuntu3.debian.tar.xz 23700 SHA512:980b86e14cabebff0833bc63472e58a936c8f221cd0fc8ebd273c3fe81164d6617fd98a271c422e98deb346b358801069011f7488eca512225f0e1356c9a4469
```

### `dpkg` source package: `libselinux=3.5-1`

Binary Packages:

- `libselinux1:amd64=3.5-1`

Licenses: (parsed from: `/usr/share/doc/libselinux1/copyright`)

- `GPL-2`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris libselinux=3.5-1
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libselinux/libselinux_3.5-1.dsc' libselinux_3.5-1.dsc 2662 SHA512:2de111b672f95c6caafdd32f219e2036c47171ed1855ac42e51bd659a4adc611084a041a902ee3966efa800f8e13858aecfc56f5cb14618fb67663ba37f13318
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libselinux/libselinux_3.5.orig.tar.gz' libselinux_3.5.orig.tar.gz 211453 SHA512:4e13261a5821018a5f3cdce676f180bb62e5bc225981ca8a498ece0d1c88d9ba8eaa0ce4099dd0849309a8a7c5a9a0953df841a9922f2c284e5a109e5d937ba7
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libselinux/libselinux_3.5.orig.tar.gz.asc' libselinux_3.5.orig.tar.gz.asc 981 SHA512:ba486d29c92801a02f75213ef5bcc4a0c4a87afe9dfa797aa9bb495ded40f21e37b22d6ea114c0e480d669b090d1116e8b9cac9fa9ea29678d3647bc58d8bb29
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libselinux/libselinux_3.5-1.debian.tar.xz' libselinux_3.5-1.debian.tar.xz 35804 SHA512:4fff1551a292eb30f06397889efeb87bbf227ffc0325498a0dd18d3ed6269adddb57020c648d1271546d391e1a2fa166c921335627a632a3ea5aa72f3b19406e
```

### `dpkg` source package: `libsemanage=3.5-1`

Binary Packages:

- `libsemanage-common=3.5-1`
- `libsemanage2:amd64=3.5-1`

Licenses: (parsed from: `/usr/share/doc/libsemanage-common/copyright`, `/usr/share/doc/libsemanage2/copyright`)

- `GPL-2`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris libsemanage=3.5-1
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsemanage/libsemanage_3.5-1.dsc' libsemanage_3.5-1.dsc 2644 SHA512:73917cb27a588859c78e1ed4ff1ea7204480d1a6dc11a11339d5167897b3048eff2df9f65498d16d684587a4f4a5278dfabc0c12f924f248b0adb2acfdfa439f
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsemanage/libsemanage_3.5.orig.tar.gz' libsemanage_3.5.orig.tar.gz 185060 SHA512:959fbd0d6bc6849da6caa13dc41c3f8818cbbd29f04b5d2ac7246c4b395b4f370f113a04cc9cfcb52be2afebfa636013ac4ad4011384c58c7ce066a45cae2751
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsemanage/libsemanage_3.5.orig.tar.gz.asc' libsemanage_3.5.orig.tar.gz.asc 981 SHA512:c0a5ddb69c32ddefa26b3d1ec676bcc373e959dd8b4a7fcf6e1f74a3ca8e9af22af851ca66d3c43a704215ff79d27244e33d23038ef2f52ccc321aeb5f0c2790
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsemanage/libsemanage_3.5-1.debian.tar.xz' libsemanage_3.5-1.debian.tar.xz 29956 SHA512:333264bd9dd88af0e87c4aeabf99ca59e2bc6e1bbed10f0372d4fabc72f0fac0ce86e68d68bdbbb0a51bd133c218226e6027b1db3b7e9e718da995bbdec1d0e6
```

### `dpkg` source package: `libsepol=3.5-1`

Binary Packages:

- `libsepol2:amd64=3.5-1`

Licenses: (parsed from: `/usr/share/doc/libsepol2/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris libsepol=3.5-1
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsepol/libsepol_3.5-1.dsc' libsepol_3.5-1.dsc 2005 SHA512:8378eb7a3514918ba6c355bec5e6c48fc1a34900635cee77d73e942ae3c538228aa41f0c367dc63c30d01832edf2537592563473f379f7de661df1b5cef7d5cd
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsepol/libsepol_3.5.orig.tar.gz' libsepol_3.5.orig.tar.gz 497522 SHA512:66f45a9f4951589855961955db686b006b4c0cddead6ac49ad238a0e4a34775905bd10fb8cf0c0ff2ab64f9b7d8366b97fcd5b19c382dec39971a2835cc765c8
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsepol/libsepol_3.5.orig.tar.gz.asc' libsepol_3.5.orig.tar.gz.asc 981 SHA512:5aa46c3a7a5d7fa0d4376766b9444cdea1b14f3ec61725950a24fcb5ba2caae271a415c613807d06e4d9b04b40cda1525c12c442eed8a7e60fb5e5beacdaba3b
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsepol/libsepol_3.5-1.debian.tar.xz' libsepol_3.5-1.debian.tar.xz 27500 SHA512:f813e8003269b11851d027759f319ea527b07d202d40a23578a313ca6750b143e41a5a137b7772b329141544001f996c8b801b998e404d58686bc47da4a3064f
```

### `dpkg` source package: `libssh=0.10.5-3ubuntu1.2`

Binary Packages:

- `libssh-4:amd64=0.10.5-3ubuntu1.2`

Licenses: (parsed from: `/usr/share/doc/libssh-4/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `LGPL-2.1`
- `LGPL-2.1+~OpenSSL`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris libssh=0.10.5-3ubuntu1.2
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libssh/libssh_0.10.5-3ubuntu1.2.dsc' libssh_0.10.5-3ubuntu1.2.dsc 2857 SHA512:f40ff2d0ee47b2006a6cd223c2b2c24a16e00d6dbdee0e986c8ab80e6c3ba4369190fc88796bf7f16259af9eca36970d23870f05909ae94c38ab3457703ce0e9
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libssh/libssh_0.10.5.orig.tar.xz' libssh_0.10.5.orig.tar.xz 557776 SHA512:2b758f9df2b5937865d4aee775ffeafafe3ae6739a89dfc470e38c7394e3c3cb5fcf8f842fdae04929890ee7e47bf8f50e3a38e82dfd26a009f3aae009d589e0
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libssh/libssh_0.10.5.orig.tar.xz.asc' libssh_0.10.5.orig.tar.xz.asc 833 SHA512:aad5e75d0a5b2e93c6de08f2b6953f05dbef47e14a08eb75c57d3f519a8323064454ba5fbc86b3538489f571a5e446ed942f2b1cea2063c8645ef36815dd2511
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libssh/libssh_0.10.5-3ubuntu1.2.debian.tar.xz' libssh_0.10.5-3ubuntu1.2.debian.tar.xz 46392 SHA512:ca6862d5412e796d19d1c8dd2f252cc9489e4b3cd1d449a718364b7523dc02df430299eeb4ed0599ca3151f48f7e3b53da110aa8c0c815b53e0cc64f6866141e
```

### `dpkg` source package: `libtasn1-6=4.19.0-3`

Binary Packages:

- `libtasn1-6:amd64=4.19.0-3`

Licenses: (parsed from: `/usr/share/doc/libtasn1-6/copyright`)

- `GFDL-1.3`
- `GPL-3`
- `LGPL`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libtasn1-6=4.19.0-3
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtasn1-6/libtasn1-6_4.19.0-3.dsc' libtasn1-6_4.19.0-3.dsc 2662 SHA512:22e3935a2af804263921c947eaa149bcc1bf32f4bb8c704242d5773acdfca8d0f9d8fd8768a5d414b1741e2ead907f1a31e6a33369baf41443a0d26b59112cd3
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtasn1-6/libtasn1-6_4.19.0.orig.tar.gz' libtasn1-6_4.19.0.orig.tar.gz 1786576 SHA512:287f5eddfb5e21762d9f14d11997e56b953b980b2b03a97ed4cd6d37909bda1ed7d2cdff9da5d270a21d863ab7e54be6b85c05f1075ac5d8f0198997cf335ef4
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtasn1-6/libtasn1-6_4.19.0.orig.tar.gz.asc' libtasn1-6_4.19.0.orig.tar.gz.asc 228 SHA512:e0417625f8df22c6421914bf2d4f19d7f27260c24c04f50e59669681f326debe06ddef9dc5a2e20fda50feb30bbbf3f41597e64961257304ec2c407aa76d107e
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtasn1-6/libtasn1-6_4.19.0-3.debian.tar.xz' libtasn1-6_4.19.0-3.debian.tar.xz 22084 SHA512:abef85645cc23f8434bc6c4cdcb5d2ce01d47f82f3bc689848e027fd1888ddd4396b8cd9ad1abb712024fb2928d97c0dfb231da2eecfc6bdecffd6829c9d4b89
```

### `dpkg` source package: `libtirpc=1.3.3+ds-1`

Binary Packages:

- `libtirpc-common=1.3.3+ds-1`
- `libtirpc-dev:amd64=1.3.3+ds-1`
- `libtirpc3:amd64=1.3.3+ds-1`

Licenses: (parsed from: `/usr/share/doc/libtirpc-common/copyright`, `/usr/share/doc/libtirpc-dev/copyright`, `/usr/share/doc/libtirpc3/copyright`)

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
$ apt-get source -qq --print-uris libtirpc=1.3.3+ds-1
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtirpc/libtirpc_1.3.3%2bds-1.dsc' libtirpc_1.3.3+ds-1.dsc 2129 SHA512:08672fa78293f89a5bc5ffcc5d191fe885b84e4bd0eae5829bd391621a2188f3a36e4e6bb5aa9c4b6a4bfb443687471eec82352d627ac32c448354fd168988ad
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtirpc/libtirpc_1.3.3%2bds.orig.tar.gz' libtirpc_1.3.3+ds.orig.tar.gz 699030 SHA512:b32bef18da9763c04cb0d372472fea91ee88ec850d6cb3d8b398c67e47d93862a2f873f2e0a38dc5379d7d3887ac127dc4b43bddfc55403375a4cc839142a562
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtirpc/libtirpc_1.3.3%2bds-1.debian.tar.xz' libtirpc_1.3.3+ds-1.debian.tar.xz 11232 SHA512:fa7f5fd84993342230283de1dcd01db8f4aa61c1b100291b0ca09269c9d036d9f3c823986f8f6f0f492a2b24cc4522397e83c0f4e610b844845886e88c74e24e
```

### `dpkg` source package: `libunistring=1.0-2`

Binary Packages:

- `libunistring2:amd64=1.0-2`

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

Source:

```console
$ apt-get source -qq --print-uris libunistring=1.0-2
'http://archive.ubuntu.com/ubuntu/pool/main/libu/libunistring/libunistring_1.0-2.dsc' libunistring_1.0-2.dsc 2181 SHA512:40ad936d753f207f93223dab8e99b14d733e7b4f8234b7aa111789b4fb974116aa1339ede4accf3751ad44e379f1ecadf903e1c006b31e4a72bba65173f01c21
'http://archive.ubuntu.com/ubuntu/pool/main/libu/libunistring/libunistring_1.0.orig.tar.xz' libunistring_1.0.orig.tar.xz 2367800 SHA512:70d5ad82722844dbeacdfcb4d7593358e4a00a9222a98537add4b7f0bf4a2bb503dfb3cd627e52e2a5ca1d3da9e5daf38a6bd521197f92002e11e715fb1662d1
'http://archive.ubuntu.com/ubuntu/pool/main/libu/libunistring/libunistring_1.0.orig.tar.xz.asc' libunistring_1.0.orig.tar.xz.asc 833 SHA512:7e32f69fac79fc418ea0aac5eca8c09fd5acbbe781d00504cd24145e2da45ba5696f20c00d16647cee8a65de2397f71bd86522e619566e7413faae4e5d739cac
'http://archive.ubuntu.com/ubuntu/pool/main/libu/libunistring/libunistring_1.0-2.debian.tar.xz' libunistring_1.0-2.debian.tar.xz 14520 SHA512:cae7a131985dd7d47248acd7fdd4d3332b804bb9d06c2e05c94507c4549a5c0d56a88c4657e09410cf98beedde104796b7a3e51d62290cc6465717cb0b20753d
```

### `dpkg` source package: `libwebp=1.2.4-0.3`

Binary Packages:

- `libwebp7:amd64=1.2.4-0.3`

Licenses: (parsed from: `/usr/share/doc/libwebp7/copyright`)

- `Apache-2.0`

Source:

```console
$ apt-get source -qq --print-uris libwebp=1.2.4-0.3
'http://archive.ubuntu.com/ubuntu/pool/main/libw/libwebp/libwebp_1.2.4-0.3.dsc' libwebp_1.2.4-0.3.dsc 2379 SHA512:eecbaab33e59e437e95646e47deb86a9da0702dfb34ec8fb7f4e01d65c59e476f2e540b788f100e4952b6d39e3f6fab3abefd66d8625ac829180f32faf41db72
'http://archive.ubuntu.com/ubuntu/pool/main/libw/libwebp/libwebp_1.2.4.orig.tar.gz' libwebp_1.2.4.orig.tar.gz 4141376 SHA512:01f21e2c3057f5878b33664d0070832d78420de3cb2fe4379b07ae6a27bb569fd1c27a920fe324beccb96ae7bfa8c05fdd9e7b0aeba6de06ab4d8b084bb38803
'http://archive.ubuntu.com/ubuntu/pool/main/libw/libwebp/libwebp_1.2.4.orig.tar.gz.asc' libwebp_1.2.4.orig.tar.gz.asc 833 SHA512:a9a27c81550a3376f9d6e56f3914ee2ad11c3200fb555a5fcb14d7fcf8d8f32a80d8fa5c9a27908a02059a4e2eeb21b1bceaa2061a7c0e809481e47592ec2fa6
'http://archive.ubuntu.com/ubuntu/pool/main/libw/libwebp/libwebp_1.2.4-0.3.debian.tar.xz' libwebp_1.2.4-0.3.debian.tar.xz 12004 SHA512:3fcda9b916067fef35f8d5365271ba475557664e5da593e4e67a5dcb23266cca30922133066b81883758ec6cfde29d5b60b498c210edaf6aa00158ff3d49cc3a
```

### `dpkg` source package: `libx11=2:1.8.6-1ubuntu1`

Binary Packages:

- `libx11-6:amd64=2:1.8.6-1ubuntu1`
- `libx11-data=2:1.8.6-1ubuntu1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libx11=2:1.8.6-1ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libx11/libx11_1.8.6-1ubuntu1.dsc' libx11_1.8.6-1ubuntu1.dsc 2587 SHA512:798234b1e47069996851787d956bdb6816e1e6acc4ce38a81da21473d3e71fc42ad927b7ff9363a441b2d18187b89935cd78c9fc7cdb29f42254a513cbb43806
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libx11/libx11_1.8.6.orig.tar.gz' libx11_1.8.6.orig.tar.gz 3193457 SHA512:76ba1e30bd60c6988be7836db9795058541e0c64fb3d628713b78716e058fa2d2cd0a08549af21ada793c3dad7409b89ff7da8af3d1f0f4d5eb78801037977ff
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libx11/libx11_1.8.6.orig.tar.gz.asc' libx11_1.8.6.orig.tar.gz.asc 801 SHA512:9659724070bbaefcfbcb113ea8e29c605deaa263e1e4e4f9a96136187e3e2118b02c5193054710e443171a56c98aa283604ed1b064f80ba587f3554972385206
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libx11/libx11_1.8.6-1ubuntu1.diff.gz' libx11_1.8.6-1ubuntu1.diff.gz 77714 SHA512:27cfaf27adb7eab1a9d97a1871a23f0bcb01c19a5c0976a108bbedaac4f96bc5de059d497679dc1ebd04ec1cb85b3802d09668e0507cca7f01c7b228455bc462
```

### `dpkg` source package: `libxau=1:1.0.9-1build5`

Binary Packages:

- `libxau6:amd64=1:1.0.9-1build5`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxau=1:1.0.9-1build5
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxau/libxau_1.0.9-1build5.dsc' libxau_1.0.9-1build5.dsc 2315 SHA512:b9a9d6888a70e8c7e8161a322a425316ed181d00ad3881caea788aeda9c4346122a70c57d30b91e7692f5c0b468da9d784c228ead5487cfb2474f4fc42b83ada
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxau/libxau_1.0.9.orig.tar.gz' libxau_1.0.9.orig.tar.gz 394068 SHA512:3b22f34a4e35d17421189df8ce3f858b0914aef0cea0b12689dd8576f14eb811e39d6e32384251573daa7e3daba400deea98e7c0e29b4105138cf82195d7f875
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxau/libxau_1.0.9.orig.tar.gz.asc' libxau_1.0.9.orig.tar.gz.asc 801 SHA512:e59b2944591499d0c0291a8d80ad8ee2cb13ee00c32b0d26c6af12a2bb96c947d4d15924ef15b377b8d7640b75b50f9b8127ba53c582090b3f73b7bcf9e00b01
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxau/libxau_1.0.9-1build5.diff.gz' libxau_1.0.9-1build5.diff.gz 10579 SHA512:9485f97bc34a7b348a7bd276001ff5e455a17c8d6b6d6e4382496c38f470f1650f7177103d2b123f25f21ce62899ceb3112909ee92e9a604d302d3c63cb59e8f
```

### `dpkg` source package: `libxcb=1.15-1`

Binary Packages:

- `libxcb1:amd64=1.15-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxcb=1.15-1
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxcb/libxcb_1.15-1.dsc' libxcb_1.15-1.dsc 5344 SHA512:c86944cd1ec1fe3ae638765551f6061b27c2a83b64a2f3afafe605d4dab5ca7c6752d7ab585bff098dc26b814b435836047c990e7d873d45bbe396fa30ae645e
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxcb/libxcb_1.15.orig.tar.gz' libxcb_1.15.orig.tar.gz 650774 SHA512:4099899c37fdda62a9a0883863ee9e50b5072e8f396ba6f4594965d9f1743fb6ea991974a99974c6f39bac14ce9aad5669fa633ac1ad2390280d613cc66eb00e
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxcb/libxcb_1.15-1.diff.gz' libxcb_1.15-1.diff.gz 26267 SHA512:c2a77f0109f7f478623ec4b7f0799175a5cc5cfafdfb036c6fa879bd4d20ce736476534f5e2d2763137dc537a568164287a3b5334346b989b5a91d75beeb79a5
```

### `dpkg` source package: `libxcrypt=1:4.4.36-2`

Binary Packages:

- `libcrypt-dev:amd64=1:4.4.36-2`
- `libcrypt1:amd64=1:4.4.36-2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxcrypt=1:4.4.36-2
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxcrypt/libxcrypt_4.4.36-2.dsc' libxcrypt_4.4.36-2.dsc 1563 SHA512:dc89e5cf496906c63ac28a7dc7e73566eabec64347e5cec21343b735627a2153216dbd9fb49e4d26c327febbb914cf52fe1065e1cd05cc7408fbb14abe50929a
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxcrypt/libxcrypt_4.4.36.orig.tar.xz' libxcrypt_4.4.36.orig.tar.xz 392732 SHA512:82839d70fc068a4d4d5e14488ea7599e2430091ace53640d639628330eff52a058ac589b6b5a39bc6c83166e68cbf9b9e2024e0371df1f949336f633f2a1726e
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxcrypt/libxcrypt_4.4.36-2.debian.tar.xz' libxcrypt_4.4.36-2.debian.tar.xz 8284 SHA512:f6095cadce8d436bd6ebc51514bd8eb401f331d5c29256f8a15d37637ef1c8a7699fbff69a1bb11e10d5a7ed1370c6f3c8ebd975e3ecbf38b2dbf2852f2cca3f
```

### `dpkg` source package: `libxdmcp=1:1.1.3-0ubuntu5`

Binary Packages:

- `libxdmcp6:amd64=1:1.1.3-0ubuntu5`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxdmcp=1:1.1.3-0ubuntu5
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxdmcp/libxdmcp_1.1.3-0ubuntu5.dsc' libxdmcp_1.1.3-0ubuntu5.dsc 2252 SHA512:5b6df4dd48380acff08dbe1fe40258d33a2f431e27da076ce54e0a1714dacb1e031aa49e2ace3863dc2131de4df42aa76b423f44f520fd8b2dbb18c4bddcada1
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxdmcp/libxdmcp_1.1.3.orig.tar.gz' libxdmcp_1.1.3.orig.tar.gz 429668 SHA512:edd05654ad9ea893e9e08269e25ea050d10eaf9f997a08494e24127d1ba0c896cd5338b4595b155c8cbf576e1d910b76e6ad7820fee62d74644f1f276551e2f2
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxdmcp/libxdmcp_1.1.3-0ubuntu5.diff.gz' libxdmcp_1.1.3-0ubuntu5.diff.gz 18395 SHA512:552a04477a7852b2a68ba268dcd19cee9dd89c2774b6c86ca8f11180f6b179cc7853348653cf3b7d3e89a0079bef91308e8da2dfd34d0f42104f352e47ea07bd
```

### `dpkg` source package: `libxext=2:1.3.4-1build1`

Binary Packages:

- `libxext6:amd64=2:1.3.4-1build1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxext=2:1.3.4-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxext/libxext_1.3.4-1build1.dsc' libxext_1.3.4-1build1.dsc 2250 SHA512:d7a857fa82374d6b0f1435f55c697f82f5f17e9492d74eea29e04679eb6a5dd49aeb88abb048e904de207c57d16d5ad487067e6fb45696834ac5c934040d7e90
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxext/libxext_1.3.4.orig.tar.gz' libxext_1.3.4.orig.tar.gz 494434 SHA512:4eebd639fd57cb9b84a1e17e368f82fbf3d9f021eef5ad3fe31dd128500db57862a82c1e0d214d447cb7641b2be3fd7e949ee1196f2a482793c6628fb1e5cd70
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxext/libxext_1.3.4-1build1.diff.gz' libxext_1.3.4-1build1.diff.gz 12588 SHA512:bfcebe8e6e277dc1ea81063a4a4663e24b78f2b69439e3b8ed2209168016876f55e8e95c6a1828ab5bf7a1936ec795e14f4391b24ec8801e0102e00e953d46e4
```

### `dpkg` source package: `libxml2=2.9.14+dfsg-1.3ubuntu0.1`

Binary Packages:

- `libxml2:amd64=2.9.14+dfsg-1.3ubuntu0.1`
- `libxml2-dev:amd64=2.9.14+dfsg-1.3ubuntu0.1`

Licenses: (parsed from: `/usr/share/doc/libxml2/copyright`, `/usr/share/doc/libxml2-dev/copyright`)

- `ISC`
- `MIT-1`

Source:

```console
$ apt-get source -qq --print-uris libxml2=2.9.14+dfsg-1.3ubuntu0.1
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxml2/libxml2_2.9.14%2bdfsg-1.3ubuntu0.1.dsc' libxml2_2.9.14+dfsg-1.3ubuntu0.1.dsc 3038 SHA512:dbfe46bbedec63fbe10d10baceec5f3a15db4743a4d2eef918a7223367287a625314b0f7318d1b5d0676f676a2892e60a623b1ec76b6314dd5aa56eb50bdf7de
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxml2/libxml2_2.9.14%2bdfsg.orig.tar.xz' libxml2_2.9.14+dfsg.orig.tar.xz 2351200 SHA512:1eacc9ac2cd8d38b8466659b3b9d84b94eb765c8f869d6cca0da131060bbc35c2b31c6148d59690547871a20cea339eac8fbe953b4fe37cf0900862f3fd9621b
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxml2/libxml2_2.9.14%2bdfsg-1.3ubuntu0.1.debian.tar.xz' libxml2_2.9.14+dfsg-1.3ubuntu0.1.debian.tar.xz 35524 SHA512:ee6bc8cdeb81ecab14e8705356b1376c8b5fbcad3c25bfe729f38c871f0c4875760f4cf44e47084b1b90c6e0e9aa1e768c460b272315f4bf014501791c49ebf3
```

### `dpkg` source package: `libxmu=2:1.1.3-3`

Binary Packages:

- `libxmuu1:amd64=2:1.1.3-3`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxmu=2:1.1.3-3
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxmu/libxmu_1.1.3-3.dsc' libxmu_1.1.3-3.dsc 2165 SHA512:7868975bb24189125a57910121c07bfd40fcb57af86a61665d7480f34339c566f4684e1db849d4d589a0e01bb59925ee8de0089bff4df436502e714c3bcc1dec
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxmu/libxmu_1.1.3.orig.tar.gz' libxmu_1.1.3.orig.tar.gz 497343 SHA512:b92fb2e96519880e9f057ae4149bd1bd95584383c6224891f3d832d98ace9292269815fe51d06a4dfc257f51021c2f7367e2f529a7ebcc3dfc64f037720a1cb8
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxmu/libxmu_1.1.3-3.diff.gz' libxmu_1.1.3-3.diff.gz 8085 SHA512:afefb6de2e65cfd1174b58a25f4598966adc375378d6525b2ddac98dce20276ae9ce03b1eb14b3a3a186e2ce00b7d68133a2578048f2582c5bb7b6be42a16fa6
```

### `dpkg` source package: `libxpm=1:3.5.12-1.1ubuntu1`

Binary Packages:

- `libxpm4:amd64=1:3.5.12-1.1ubuntu1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxpm=1:3.5.12-1.1ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxpm/libxpm_3.5.12-1.1ubuntu1.dsc' libxpm_3.5.12-1.1ubuntu1.dsc 2179 SHA512:756c56eec8e6ad9472d74768e4d5c3b9e8d661bb7927f855f288d60b068ec56699d89f7322329cfd06794b831a4f6d00e463677a8537f2d664c51fce73532e2e
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxpm/libxpm_3.5.12.orig.tar.gz' libxpm_3.5.12.orig.tar.gz 529302 SHA512:17169016efc1e139f079290b2369fd62df8617867d97d2f50940521951a50f173118143109f0d7c552de92913cefc5ccaeb52225ccdd9abc89b3b85d9b5669f7
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxpm/libxpm_3.5.12-1.1ubuntu1.diff.gz' libxpm_3.5.12-1.1ubuntu1.diff.gz 23609 SHA512:30629fd3ead304c2061c8593934b28e9afb8d8c12bf30d844bb7362929507be53442bcb83933beed3d6640a065711968bd1414dfbd90ce59d624172674a7d713
```

### `dpkg` source package: `libzstd=1.5.5+dfsg2-1ubuntu2`

Binary Packages:

- `libzstd1:amd64=1.5.5+dfsg2-1ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libzstd1/copyright`)

- `BSD-3-clause`
- `Expat`
- `GPL-2`
- `zlib`

Source:

```console
$ apt-get source -qq --print-uris libzstd=1.5.5+dfsg2-1ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/libz/libzstd/libzstd_1.5.5%2bdfsg2-1ubuntu2.dsc' libzstd_1.5.5+dfsg2-1ubuntu2.dsc 2352 SHA512:5da90109c61965ef59b100bb1479c243c79c278a4f40bb4fb8dd547bdec153cd7e7f30764e83cd6d34e221425fa6360ffeea19235963a74936605f5e44dc5683
'http://archive.ubuntu.com/ubuntu/pool/main/libz/libzstd/libzstd_1.5.5%2bdfsg2.orig.tar.xz' libzstd_1.5.5+dfsg2.orig.tar.xz 1784164 SHA512:0b24cf71636b36ae17f617f0a4a2e1253ba6a7bfcd8b6f4717cc59310e92d23bde0945f885fa80622d84961b85fa6ba74e3436ab1badc687e8a13ac428a71b8d
'http://archive.ubuntu.com/ubuntu/pool/main/libz/libzstd/libzstd_1.5.5%2bdfsg2-1ubuntu2.debian.tar.xz' libzstd_1.5.5+dfsg2-1ubuntu2.debian.tar.xz 21400 SHA512:ea28ea8fb4eb2ccabb1d959c25dbdbc85b10467f18660c28d97687c3c8383458b70217182c4531da0e5838b91fb743defabf59a643466d12f2034aa373b2150f
```

### `dpkg` source package: `linux=6.5.0-41.41`

Binary Packages:

- `linux-libc-dev:amd64=6.5.0-41.41`

Licenses: (parsed from: `/usr/share/doc/linux-libc-dev/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris linux=6.5.0-41.41
'http://archive.ubuntu.com/ubuntu/pool/main/l/linux/linux_6.5.0-41.41.dsc' linux_6.5.0-41.41.dsc 9241 SHA512:6251d8ff867ffa7b49b024b23000dbe8548aa07aab943f8ae2006d551767c0e108654b9ff8fe984d44c412548518c477468140bf36b75d9eeab9b9d2e04dbc43
'http://archive.ubuntu.com/ubuntu/pool/main/l/linux/linux_6.5.0.orig.tar.gz' linux_6.5.0.orig.tar.gz 223513863 SHA512:efc66eef13698e7210b7dd30ac5f664f64b4b186e6061b322b369d3e27a46e35696f3ee441b12928211992867a06042beb3d31903e469e0bd78c13895afa853e
'http://archive.ubuntu.com/ubuntu/pool/main/l/linux/linux_6.5.0-41.41.diff.gz' linux_6.5.0-41.41.diff.gz 3563521 SHA512:ecf7b5b943569df75b0271898ea30a61384ce7a78174f2d8801b06d2b4ee722261afc097f76679e194fe9ffe6d67491cc06608a22e6c1cce9a630a55ef0f917a
```

### `dpkg` source package: `llvm-toolchain-13=1:13.0.1-13`

Binary Packages:

- `libclang-cpp13=1:13.0.1-13`
- `liblldb-13=1:13.0.1-13`
- `libllvm13:amd64=1:13.0.1-13`
- `python3-lldb-13=1:13.0.1-13`

Licenses: (parsed from: `/usr/share/doc/libclang-cpp13/copyright`, `/usr/share/doc/liblldb-13/copyright`, `/usr/share/doc/libllvm13/copyright`, `/usr/share/doc/python3-lldb-13/copyright`)

- `APACHE-2-LLVM-EXCEPTIONS`
- `Apache-2.0`
- `BSD-3-Clause`
- `BSD-3-clause`
- `MIT`
- `Python`
- `solar-public-domain`

Source:

```console
$ apt-get source -qq --print-uris llvm-toolchain-13=1:13.0.1-13
'http://archive.ubuntu.com/ubuntu/pool/universe/l/llvm-toolchain-13/llvm-toolchain-13_13.0.1-13.dsc' llvm-toolchain-13_13.0.1-13.dsc 7277 SHA512:e12070752031999dc3607b3c59b7d31be98dd5c3dee4f7f7ff3f58cb8af57f75ab5c3c1be81aa90e799a210618d8a252b094e3e8b8b4af7f25798a6d94c236ba
'http://archive.ubuntu.com/ubuntu/pool/universe/l/llvm-toolchain-13/llvm-toolchain-13_13.0.1.orig.tar.xz' llvm-toolchain-13_13.0.1.orig.tar.xz 121050160 SHA512:1387fabc239ba982bf7845cf8c611d87fb005a554d3d11701b4c0de1ee280c3402c32eca7e221d4c6c2b2d6b2782891606dbc33f2a7ae1c85211826009b19eac
'http://archive.ubuntu.com/ubuntu/pool/universe/l/llvm-toolchain-13/llvm-toolchain-13_13.0.1-13.debian.tar.xz' llvm-toolchain-13_13.0.1-13.debian.tar.xz 165072 SHA512:b84c73b259762941e9d09456b249d3d4c595d8c005b6909acefe25b14c994bdb2a3e480bb139acc1a83322526a17ce0e608ced49f2ac6e6db77ff14ca1597429
```

### `dpkg` source package: `lz4=1.9.4-1`

Binary Packages:

- `liblz4-1:amd64=1.9.4-1`

Licenses: (parsed from: `/usr/share/doc/liblz4-1/copyright`)

- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris lz4=1.9.4-1
'http://archive.ubuntu.com/ubuntu/pool/main/l/lz4/lz4_1.9.4-1.dsc' lz4_1.9.4-1.dsc 1951 SHA512:556aac9a8300772dc4016c09c5783ad38da73c2abe06a2074ed31ae2429972f81e49e883e11c1d9f25c63a8c8ea95cf7f738a1e9ebc2280a015615eb2c84ee10
'http://archive.ubuntu.com/ubuntu/pool/main/l/lz4/lz4_1.9.4.orig.tar.gz' lz4_1.9.4.orig.tar.gz 354063 SHA512:043a9acb2417624019d73db140d83b80f1d7c43a6fd5be839193d68df8fd0b3f610d7ed4d628c2a9184f7cde9a0fd1ba9d075d8251298e3eb4b3a77f52736684
'http://archive.ubuntu.com/ubuntu/pool/main/l/lz4/lz4_1.9.4-1.debian.tar.xz' lz4_1.9.4-1.debian.tar.xz 8128 SHA512:e89e2577dea9d76f6cac8c154c3fc6f77f501b5896ba949561e8a6a1e4982ad8de83d2deab8ca53dccab9856294dc2397d359cb0f4279b4f70b152c482043d88
```

### `dpkg` source package: `manpages=6.03-2`

Binary Packages:

- `manpages=6.03-2`
- `manpages-dev=6.03-2`

Licenses: (parsed from: `/usr/share/doc/manpages/copyright`, `/usr/share/doc/manpages-dev/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `BSD-4-clause`
- `Expat`
- `GPL-1+`
- `GPL-2`
- `GPL-2+`
- `Linux-man-pages-copyleft`

Source:

```console
$ apt-get source -qq --print-uris manpages=6.03-2
'http://archive.ubuntu.com/ubuntu/pool/main/m/manpages/manpages_6.03-2.dsc' manpages_6.03-2.dsc 1927 SHA512:cf454838c04b7bdb816d89e50bcbe1ccd7f11add7b9965a24525c965a4b891b011cf1e99d110d7e8e6ea267e9403fb39e30b331b9f63b4b71c20d42cdb01dbd9
'http://archive.ubuntu.com/ubuntu/pool/main/m/manpages/manpages_6.03.orig.tar.xz' manpages_6.03.orig.tar.xz 2198960 SHA512:fbba7e42f192ac0913648fa767382261d017edd8db220cbebe56e23699aae34e95660d0fccbc50dafb49878d0bdf86066cf3987a852fb01a1129da277ffe6e3a
'http://archive.ubuntu.com/ubuntu/pool/main/m/manpages/manpages_6.03-2.debian.tar.xz' manpages_6.03-2.debian.tar.xz 57956 SHA512:816417392314d31f6ca1cefab5ff0366cf2c9be9dd7d4f8bb9e7329afffb7d00f46e646ccfa1133bd74be416a9b76be76967a1e3170d1c8ba7630264cdd0bc94
```

### `dpkg` source package: `mawk=1.3.4.20230730-1`

Binary Packages:

- `mawk=1.3.4.20230730-1`

Licenses: (parsed from: `/usr/share/doc/mawk/copyright`)

- `CC-BY-3.0`
- `GPL-2`
- `GPL-2.0-only`
- `X11`

Source:

```console
$ apt-get source -qq --print-uris mawk=1.3.4.20230730-1
'http://archive.ubuntu.com/ubuntu/pool/main/m/mawk/mawk_1.3.4.20230730-1.dsc' mawk_1.3.4.20230730-1.dsc 2180 SHA512:a0bd0a9b8d369f08622b3c6ce46917adfa9e4f0f064d969e91ebc862dc484a3026138174ed66caa97a35a5cae65c11682f66f5b4793d31ac839935fd6f9cfdfd
'http://archive.ubuntu.com/ubuntu/pool/main/m/mawk/mawk_1.3.4.20230730.orig.tar.gz' mawk_1.3.4.20230730.orig.tar.gz 410248 SHA512:a38dad468db614e36149916656c22b0dcd3e66ce4be73dada355f9c96c3b4c864d81cbd65608cbed315050a36e2a3bd049e28ce41818cd5da260141b4548bf46
'http://archive.ubuntu.com/ubuntu/pool/main/m/mawk/mawk_1.3.4.20230730.orig.tar.gz.asc' mawk_1.3.4.20230730.orig.tar.gz.asc 729 SHA512:28b0d46248beb0244a9d584690b70338cb29f6b08c29350522e91d56ce2ab625f9696a637fa23b4b43448883f79c6a007d731367274285ec7fa45547f22b910d
'http://archive.ubuntu.com/ubuntu/pool/main/m/mawk/mawk_1.3.4.20230730-1.debian.tar.xz' mawk_1.3.4.20230730-1.debian.tar.xz 15492 SHA512:ee5a6a99a0f676d1601d8d3153c9c4d3d2cf51713937a973f253c210cd47d52c5f5200bd00a7cfa4a44cb22d76c6d9fc5a8f8b28ec0ad50528588d70017fca9c
```

### `dpkg` source package: `media-types=10.1.0`

Binary Packages:

- `media-types=10.1.0`

Licenses: (parsed from: `/usr/share/doc/media-types/copyright`)

- `ad-hoc`

Source:

```console
$ apt-get source -qq --print-uris media-types=10.1.0
'http://archive.ubuntu.com/ubuntu/pool/main/m/media-types/media-types_10.1.0.dsc' media-types_10.1.0.dsc 1624 SHA512:78ee4c91efa0eea0314213b1df7cc659f3b47556a648e07c4044f1ae7ae08ccd6c4d479e6425297ac79c38a2a607a157ed781c66751235cecee1eb1ed8edf6b5
'http://archive.ubuntu.com/ubuntu/pool/main/m/media-types/media-types_10.1.0.tar.xz' media-types_10.1.0.tar.xz 59052 SHA512:db92986166c6eedd44d839617c75a1f60704af6d87f92a5c9bb5f207a8e4e27f67b86e340745f6f41e793908d48eb609575678495194a21d368db2fc102b35c9
```

### `dpkg` source package: `ncurses=6.4+20230625-2`

Binary Packages:

- `libncurses6:amd64=6.4+20230625-2`
- `libncursesw6:amd64=6.4+20230625-2`
- `libtinfo6:amd64=6.4+20230625-2`
- `ncurses-base=6.4+20230625-2`
- `ncurses-bin=6.4+20230625-2`

Licenses: (parsed from: `/usr/share/doc/libncurses6/copyright`, `/usr/share/doc/libncursesw6/copyright`, `/usr/share/doc/libtinfo6/copyright`, `/usr/share/doc/ncurses-base/copyright`, `/usr/share/doc/ncurses-bin/copyright`)

- `BSD-3-clause`
- `MIT/X11`
- `X11`

Source:

```console
$ apt-get source -qq --print-uris ncurses=6.4+20230625-2
'http://archive.ubuntu.com/ubuntu/pool/main/n/ncurses/ncurses_6.4%2b20230625-2.dsc' ncurses_6.4+20230625-2.dsc 3807 SHA512:2b553a6bfdb99698cab4b3261ab8ba00d8f9204bed0297ceffa8508965386e63d85abed7148c552a2850256f980279bf5b57209afbbd15fde783ef6a32b559d1
'http://archive.ubuntu.com/ubuntu/pool/main/n/ncurses/ncurses_6.4%2b20230625.orig.tar.gz' ncurses_6.4+20230625.orig.tar.gz 3649551 SHA512:adb42d67bd82544ee7d9c2e001bef5f8fec7d9e6459e37f4664057a8e88176c9536b5804e847ab8525f78e6ca44841d1d44f84826bce9e443bdb1a4f59ed5bad
'http://archive.ubuntu.com/ubuntu/pool/main/n/ncurses/ncurses_6.4%2b20230625.orig.tar.gz.asc' ncurses_6.4+20230625.orig.tar.gz.asc 729 SHA512:49dce0e1d23288cdb97e786ed145554c4ef421c8944af91805c2359e79ef9aeffd6a386fc4519ef75d1adcf1d55c403204c6b1c30be69a872c5a5c07d1eac98a
'http://archive.ubuntu.com/ubuntu/pool/main/n/ncurses/ncurses_6.4%2b20230625-2.debian.tar.xz' ncurses_6.4+20230625-2.debian.tar.xz 48584 SHA512:5d6cc5875d813bb03f115309e790e7311f983607db16fba9ffc6385d5180253cd1368f7175cd475c0404e98aafde373d9a9f1c26bca1b7ce96b79f3495b2b557
```

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

### `dpkg` source package: `nettle=3.9.1-2`

Binary Packages:

- `libhogweed6:amd64=3.9.1-2`
- `libnettle8:amd64=3.9.1-2`

Licenses: (parsed from: `/usr/share/doc/libhogweed6/copyright`, `/usr/share/doc/libnettle8/copyright`)

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
$ apt-get source -qq --print-uris nettle=3.9.1-2
'http://archive.ubuntu.com/ubuntu/pool/main/n/nettle/nettle_3.9.1-2.dsc' nettle_3.9.1-2.dsc 2274 SHA512:4f48a301f663147237b7a74a2ff6ec85fd575650bcbd060ef273a86014d3f2a7048edfb3c6dfc95d73be2d92c7368469cd326e58785910caba21840b1f00f6bc
'http://archive.ubuntu.com/ubuntu/pool/main/n/nettle/nettle_3.9.1.orig.tar.gz' nettle_3.9.1.orig.tar.gz 2396741 SHA512:5939c4b43cf9ff6c6272245b85f123c81f8f4e37089fa4f39a00a570016d837f6e706a33226e4bbfc531b02a55b2756ff312461225ed88de338a73069e031ced
'http://archive.ubuntu.com/ubuntu/pool/main/n/nettle/nettle_3.9.1.orig.tar.gz.asc' nettle_3.9.1.orig.tar.gz.asc 573 SHA512:2ca8ab90c2a437c587987492be2a4c71658256020af725b48ee8f25771b7af28a9c1a8e300826dce58c4b691545d450ec44e668187daaa351a63a77eca4cedcb
'http://archive.ubuntu.com/ubuntu/pool/main/n/nettle/nettle_3.9.1-2.debian.tar.xz' nettle_3.9.1-2.debian.tar.xz 24440 SHA512:5ecbb74a3e05032f4d13cb6f393f6d23b7a2fff4240370f05d973a331c279d6c9cb0fd5ca7d551febf4fd54e30ebb296729284c6327114529c101edcf80ec2cb
```

### `dpkg` source package: `nghttp2=1.55.1-1ubuntu0.2`

Binary Packages:

- `libnghttp2-14:amd64=1.55.1-1ubuntu0.2`

Licenses: (parsed from: `/usr/share/doc/libnghttp2-14/copyright`)

- `BSD-2-clause`
- `Expat`
- `GPL-3`
- `GPL-3+ with autoconf exception`
- `MIT`
- `all-permissive`

Source:

```console
$ apt-get source -qq --print-uris nghttp2=1.55.1-1ubuntu0.2
'http://archive.ubuntu.com/ubuntu/pool/main/n/nghttp2/nghttp2_1.55.1-1ubuntu0.2.dsc' nghttp2_1.55.1-1ubuntu0.2.dsc 2665 SHA512:c2c6a7b082d907d1c4141f54094213bd39b48afbc8e6e7cbd0362bce5758cc33a4ff128854ccfae9216875a9f1a2383675495892f1ae39745bb89ca01a44a558
'http://archive.ubuntu.com/ubuntu/pool/main/n/nghttp2/nghttp2_1.55.1.orig.tar.gz' nghttp2_1.55.1.orig.tar.gz 1071258 SHA512:0ab1a987ec99f7b0652e75a93bebff9a5363f52758be1f6ae8626dcf9f4b2f931dec0a276cdd7b81522c61040e008345ecc5011c17a763b97a48b0f7e2615451
'http://archive.ubuntu.com/ubuntu/pool/main/n/nghttp2/nghttp2_1.55.1-1ubuntu0.2.debian.tar.xz' nghttp2_1.55.1-1ubuntu0.2.debian.tar.xz 19328 SHA512:4f006403451fe5684573530f42f1124cd0df6741085c3600377d0704b080f6a5b377cd692a6fcf1d2f17e272c498579ecd11d4a0b2f37975b444672173bbd3d7
```

### `dpkg` source package: `npth=1.6-3build2`

Binary Packages:

- `libnpth0:amd64=1.6-3build2`

Licenses: (parsed from: `/usr/share/doc/libnpth0/copyright`)

- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris npth=1.6-3build2
'http://archive.ubuntu.com/ubuntu/pool/main/n/npth/npth_1.6-3build2.dsc' npth_1.6-3build2.dsc 2063 SHA512:19ea7bd0ffc2b0aff06c52298c9a25c2f30619239bea09b571feb4a3d162f461a4529136e351da42b16ab3eaef5add24234f644e822e859ccb32de5bfd658ec0
'http://archive.ubuntu.com/ubuntu/pool/main/n/npth/npth_1.6.orig.tar.bz2' npth_1.6.orig.tar.bz2 300486 SHA512:2ed1012e14a9d10665420b9a23628be7e206fd9348111ec751349b93557ee69f1176bcf7e6b195b35b1c44a5e0e81ee33b713f03d79a33d1ecd9037035afeda2
'http://archive.ubuntu.com/ubuntu/pool/main/n/npth/npth_1.6-3build2.debian.tar.xz' npth_1.6-3build2.debian.tar.xz 10904 SHA512:426ab3ab9e27b3701d67cde0a4c4040aa9ccac22a0266321824487fe80a118ccd6860b6fa0fb5ca3c46dfa3c20053889fbb51a2e74618065b3aff059a0216c4c
```

### `dpkg` source package: `openldap=2.6.6+dfsg-1~exp1ubuntu1`

Binary Packages:

- `libldap-common=2.6.6+dfsg-1~exp1ubuntu1`
- `libldap2:amd64=2.6.6+dfsg-1~exp1ubuntu1`

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
$ apt-get source -qq --print-uris openldap=2.6.6+dfsg-1~exp1ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/o/openldap/openldap_2.6.6%2bdfsg-1%7eexp1ubuntu1.dsc' openldap_2.6.6+dfsg-1~exp1ubuntu1.dsc 3470 SHA512:7c1d353d8f310a2e3c19498cc4c45f9d05123fe732f1a82d56296fe899979d622276f3ecd8ef0b4f1cb67b162913a5e9b3c1ed402ff52e06cfe28301f0ff8500
'http://archive.ubuntu.com/ubuntu/pool/main/o/openldap/openldap_2.6.6%2bdfsg.orig.tar.xz' openldap_2.6.6+dfsg.orig.tar.xz 3746232 SHA512:50b7b1020926effc305db829b8782bf733aa83cbf94cce41b770af2f00c4136b07a11462a7b62bd7ef273d451e362267cd658549d9bea6b97f201ec1547dd4e4
'http://archive.ubuntu.com/ubuntu/pool/main/o/openldap/openldap_2.6.6%2bdfsg-1%7eexp1ubuntu1.debian.tar.xz' openldap_2.6.6+dfsg-1~exp1ubuntu1.debian.tar.xz 179316 SHA512:d1f351512ab8c23e2c4daa1a0f69e87824cb04cdfb86e9e9abb5646ca38ef04f798d718ceaf71c574274c23d3847cd1d202e31b0d8e978e59a3a5b294b793dd5
```

### `dpkg` source package: `openssh=1:9.3p1-1ubuntu3.3`

Binary Packages:

- `openssh-client=1:9.3p1-1ubuntu3.3`

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
$ apt-get source -qq --print-uris openssh=1:9.3p1-1ubuntu3.3
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssh/openssh_9.3p1-1ubuntu3.3.dsc' openssh_9.3p1-1ubuntu3.3.dsc 3106 SHA512:8cd966f9cbf33af7030fbfb6785e3531afcbdb0c93f833d75818640b01f15b66fe9dd8727d71179235662a7e4c4cde2274873e23b46ad5485945b0d789c54c38
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssh/openssh_9.3p1.orig.tar.gz' openssh_9.3p1.orig.tar.gz 1856839 SHA512:087ff6fe5f6caab4c6c3001d906399e02beffad7277280f11187420c2939fd4befdcb14643862a657ce4cad2f115b82a0a1a2c99df6ee54dcd76b53647637c19
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssh/openssh_9.3p1-1ubuntu3.3.debian.tar.xz' openssh_9.3p1-1ubuntu3.3.debian.tar.xz 199552 SHA512:662a7e77accfb9c8005b52ea89441ee7823cbbaabec1be61df3cef92657576fbd2baa9cebe74ae64ffc70e36170726b7ded2422367a5fe967c5657605bc3f22f
```

### `dpkg` source package: `openssl=3.0.10-1ubuntu2.3`

Binary Packages:

- `libssl3:amd64=3.0.10-1ubuntu2.3`
- `openssl=3.0.10-1ubuntu2.3`

Licenses: (parsed from: `/usr/share/doc/libssl3/copyright`, `/usr/share/doc/openssl/copyright`)

- `Apache-2.0`
- `Artistic`
- `GPL-1`
- `GPL-1+`

Source:

```console
$ apt-get source -qq --print-uris openssl=3.0.10-1ubuntu2.3
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssl/openssl_3.0.10-1ubuntu2.3.dsc' openssl_3.0.10-1ubuntu2.3.dsc 2781 SHA512:b6afb1ab9d7a13089dd80ebe649abb00eb6d199b926d81fb13b46971d99966b791cc87dd3e79a54684c5945c1315cbb3a8beffcaa006c399db8216c7b66ff67b
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssl/openssl_3.0.10.orig.tar.gz' openssl_3.0.10.orig.tar.gz 15194904 SHA512:fc12f3beed5e2d2f4767aeb772ceb6ba26f6cbfabc247765854108266b27a1223134f0e81735867a9069bc9c07a14b9816e85903cef91bd1b90f781f0b98b61a
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssl/openssl_3.0.10.orig.tar.gz.asc' openssl_3.0.10.orig.tar.gz.asc 833 SHA512:3d91e763dcb0bb37cf6586b75c5310c824b5ca75e59a206d759081a67bc016add501648a365aa479dc621f33b86e7aac26d1deb528b43a37187d91eb194b2bdc
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssl/openssl_3.0.10-1ubuntu2.3.debian.tar.xz' openssl_3.0.10-1ubuntu2.3.debian.tar.xz 180344 SHA512:b58d216eb34ca9b6754c512f86a51758cfffd52001f2c375e06cf0ea88582b2ab4cbb285769ac63a9e641fd4554dc79cc5bf9a1da86ba01ff2289513cb94acb9
```

### `dpkg` source package: `p11-kit=0.25.0-4ubuntu1`

Binary Packages:

- `libp11-kit0:amd64=0.25.0-4ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libp11-kit0/copyright`)

- `Apache-2.0`
- `BSD-3-Clause`
- `ISC`
- `ISC+IBM`
- `LGPL-2.1`
- `LGPL-2.1+`
- `permissive-like-automake-output`
- `same-as-rest-of-p11kit`

Source:

```console
$ apt-get source -qq --print-uris p11-kit=0.25.0-4ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/p/p11-kit/p11-kit_0.25.0-4ubuntu1.dsc' p11-kit_0.25.0-4ubuntu1.dsc 2608 SHA512:8476349970c06d63d1901f18addd135e2f82fb80297ae72ca574db4ce45f3c09ada4edc7e748b8d7969cd753f032c5e840da8716c63ec54e351e649e22429338
'http://archive.ubuntu.com/ubuntu/pool/main/p/p11-kit/p11-kit_0.25.0.orig.tar.xz' p11-kit_0.25.0.orig.tar.xz 958940 SHA512:e6df3cb224f6ff5671bd3c0557503b5f20bbfded1b6ec340b1dafcbd1b1725ea2d41d0e920756716e0fe9cb28270d115fe77b23ec876a15007b22e3f30d015fe
'http://archive.ubuntu.com/ubuntu/pool/main/p/p11-kit/p11-kit_0.25.0.orig.tar.xz.asc' p11-kit_0.25.0.orig.tar.xz.asc 228 SHA512:4ff7f240e9f166f1e28081f0e23d5b0dd699952fc1b7184dc881ec565eff3f4d5622664af3fc3add4cb828570b6ef77ff2036c467589a1e49605fefda3e73748
'http://archive.ubuntu.com/ubuntu/pool/main/p/p11-kit/p11-kit_0.25.0-4ubuntu1.debian.tar.xz' p11-kit_0.25.0-4ubuntu1.debian.tar.xz 25920 SHA512:6325ede913b64e317ddb851ed9f4ae673d8b3ceec300f95f5ad148ac51c49aaba6c506e31320d7ea4744da67ee1bdd817fdaa44a0478c407111a23094b0059d2
```

### `dpkg` source package: `pam=1.5.2-6ubuntu1.1`

Binary Packages:

- `libpam-modules:amd64=1.5.2-6ubuntu1.1`
- `libpam-modules-bin=1.5.2-6ubuntu1.1`
- `libpam-runtime=1.5.2-6ubuntu1.1`
- `libpam0g:amd64=1.5.2-6ubuntu1.1`

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
$ apt-get source -qq --print-uris pam=1.5.2-6ubuntu1.1
'http://archive.ubuntu.com/ubuntu/pool/main/p/pam/pam_1.5.2-6ubuntu1.1.dsc' pam_1.5.2-6ubuntu1.1.dsc 2704 SHA512:4973a12061bbb56c2881a4980355722b6e407601a1ddaf66c1365f8beda52d5dc46e2b30fdc25687abff8f82231cf9da6ed57d2844af8c87ca79f14a82f71966
'http://archive.ubuntu.com/ubuntu/pool/main/p/pam/pam_1.5.2.orig.tar.xz' pam_1.5.2.orig.tar.xz 988784 SHA512:fa16350c132d3e5fb82b60d991768fb596582639841b8ece645c684705467305ccf1302a0147ec222ab78c01b2c9114c5496dc1ca565d2b56bf315f29a815144
'http://archive.ubuntu.com/ubuntu/pool/main/p/pam/pam_1.5.2-6ubuntu1.1.debian.tar.xz' pam_1.5.2-6ubuntu1.1.debian.tar.xz 169216 SHA512:a9b76f7bd8bb2fc4f6e0c37a5c2053df767119f8420c515377249ae7dfcf493a469fb61888898f0cbd6702a7b429f2b75e08c544812357ad3d47d432a1a324ea
```

### `dpkg` source package: `patch=2.7.6-7build2`

Binary Packages:

- `patch=2.7.6-7build2`

Licenses: (parsed from: `/usr/share/doc/patch/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris patch=2.7.6-7build2
'http://archive.ubuntu.com/ubuntu/pool/main/p/patch/patch_2.7.6-7build2.dsc' patch_2.7.6-7build2.dsc 1838 SHA512:35ea8fc554a359197cc5ca13dcc3926499563e73e03d8e316d1433d01bc8066e0a138cdab0548d40ec73ee08fe719166c1959793219e798817d69afc94be7665
'http://archive.ubuntu.com/ubuntu/pool/main/p/patch/patch_2.7.6.orig.tar.xz' patch_2.7.6.orig.tar.xz 783756 SHA512:fcca87bdb67a88685a8a25597f9e015f5e60197b9a269fa350ae35a7991ed8da553939b4bbc7f7d3cfd863c67142af403b04165633acbce4339056a905e87fbd
'http://archive.ubuntu.com/ubuntu/pool/main/p/patch/patch_2.7.6-7build2.debian.tar.xz' patch_2.7.6-7build2.debian.tar.xz 15248 SHA512:fb482b8f4980bca77a7060aa54cbae01aec9536a72b1e009e9a0cb8f9a35979bf14dcd356b93a2227f18248e81a7e53aac09b7b0d4bd39021681826a9b3ba38f
```

### `dpkg` source package: `pcre2=10.42-4`

Binary Packages:

- `libpcre2-8-0:amd64=10.42-4`

Licenses: (parsed from: `/usr/share/doc/libpcre2-8-0/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `BSD-3-clause-Cambridge with BINARY LIBRARY-LIKE PACKAGES exception`
- `X11`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris pcre2=10.42-4
'http://archive.ubuntu.com/ubuntu/pool/main/p/pcre2/pcre2_10.42-4.dsc' pcre2_10.42-4.dsc 2302 SHA512:097275466e22a43e8d62b1ff1e10f87093ced5c9ed3bb5badc3a6d5c675c0757b24dee800a14a2bfd104fda5eebf8b0065d1977651739f8956d85923944ddddc
'http://archive.ubuntu.com/ubuntu/pool/main/p/pcre2/pcre2_10.42.orig.tar.gz' pcre2_10.42.orig.tar.gz 2397194 SHA512:a3db6c5c620775838819be616652e73ce00f5ef5c1f49f559ff3efb51a119d02f01254c5901c1f7d0c47c0ddfcf4313e38d6ca32c35381b8f87f36896d10e6f7
'http://archive.ubuntu.com/ubuntu/pool/main/p/pcre2/pcre2_10.42-4.diff.gz' pcre2_10.42-4.diff.gz 8111 SHA512:d13593a4e46d686238e766b253886eed102d8728a943f2f55d1459311d6e9715be46dd4fc2353d7375100d0200c9c0037521b5072f7ea30826c19af2d48f93e3
```

### `dpkg` source package: `perl=5.36.0-9ubuntu1.1`

Binary Packages:

- `libperl5.36:amd64=5.36.0-9ubuntu1.1`
- `perl=5.36.0-9ubuntu1.1`
- `perl-base=5.36.0-9ubuntu1.1`
- `perl-modules-5.36=5.36.0-9ubuntu1.1`

Licenses: (parsed from: `/usr/share/doc/libperl5.36/copyright`, `/usr/share/doc/perl/copyright`, `/usr/share/doc/perl-base/copyright`, `/usr/share/doc/perl-modules-5.36/copyright`)

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
$ apt-get source -qq --print-uris perl=5.36.0-9ubuntu1.1
'http://archive.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.36.0-9ubuntu1.1.dsc' perl_5.36.0-9ubuntu1.1.dsc 3009 SHA512:ffd2fa91526b4cfbca018c25c491dc3a0b5e2ff8bc7518045f9282289808a6e1020d24d7e8d2e2343639a9ead3f180ac94fb45e4bf00627682363b5975828853
'http://archive.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.36.0.orig-regen-configure.tar.xz' perl_5.36.0.orig-regen-configure.tar.xz 417784 SHA512:4d16685f569a5b1dea79d607b6d62718111c32efaf5547bb9e1528bd755acf0c8fc74a1cc1f4d68fcb10aef9da7d8fea17a5cc10dabce6efa4721ab45ab03a65
'http://archive.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.36.0.orig.tar.xz' perl_5.36.0.orig.tar.xz 13051500 SHA512:6dd6ac2a77566c173c5ab9c238cf555f2c3e592e89abb5600bc23ce1cbd0c349e0233f6417cbbf1f6d0aefc6a734ba491285af0d3dc68a605b658b65c89f1dab
'http://archive.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.36.0-9ubuntu1.1.debian.tar.xz' perl_5.36.0-9ubuntu1.1.debian.tar.xz 172720 SHA512:9213709c3e6718d3b8c5cb235e1c729e19a44e86622beebcaa553456a73e0373ca7d70d0b68544f2b4398a57245ea051a8e9249f00a9a44545f08d2d4b2b6099
```

### `dpkg` source package: `pinentry=1.2.1-1ubuntu1`

Binary Packages:

- `pinentry-curses=1.2.1-1ubuntu1`

Licenses: (parsed from: `/usr/share/doc/pinentry-curses/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-3`
- `LGPL-3+`
- `X11`

Source:

```console
$ apt-get source -qq --print-uris pinentry=1.2.1-1ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/p/pinentry/pinentry_1.2.1-1ubuntu1.dsc' pinentry_1.2.1-1ubuntu1.dsc 2999 SHA512:2e895300429edd2b707fded47ee07d66bf7d439417deae2a78720cf833152bf71f9357cc93632358c1d59963f1513ccaaa2c3904c4de51991d65b60cb19bcf2f
'http://archive.ubuntu.com/ubuntu/pool/main/p/pinentry/pinentry_1.2.1.orig.tar.bz2' pinentry_1.2.1.orig.tar.bz2 547698 SHA512:a665315628f4dcf07e16a22db3f3be15d7e7e93b3deec0546c7275b71b0e3bd65535a08af5e12d6339fd6595132df86529401d9d12bd17c428a3466e8dfafab6
'http://archive.ubuntu.com/ubuntu/pool/main/p/pinentry/pinentry_1.2.1.orig.tar.bz2.asc' pinentry_1.2.1.orig.tar.bz2.asc 390 SHA512:60b63b7fe2d6793840be55635f9a704cd42eda69ccaea2453d47b5f7a5198d313b8f23555972584f7f087fd5d0fc2a379bfc5f7512f325b018cc5c3e2e54a47e
'http://archive.ubuntu.com/ubuntu/pool/main/p/pinentry/pinentry_1.2.1-1ubuntu1.debian.tar.xz' pinentry_1.2.1-1ubuntu1.debian.tar.xz 18828 SHA512:94a82f96b7cf520c8335fea8a7be1beb8baf9e68e5939e3436837eca87ed0346bd295e406f6d546c74f0592332c6913e6c6b709c7dbe014bda769d556ce71238
```

### `dpkg` source package: `pkgconf=1.8.1-2`

Binary Packages:

- `libpkgconf3:amd64=1.8.1-2`
- `pkg-config:amd64=1.8.1-2`
- `pkgconf:amd64=1.8.1-2`
- `pkgconf-bin=1.8.1-2`

Licenses: (parsed from: `/usr/share/doc/libpkgconf3/copyright`, `/usr/share/doc/pkg-config/copyright`, `/usr/share/doc/pkgconf/copyright`, `/usr/share/doc/pkgconf-bin/copyright`)

- `BSD-2`
- `BSD-4`
- `GPL-2`
- `GPL-2+`
- `ISC`
- `X11`

Source:

```console
$ apt-get source -qq --print-uris pkgconf=1.8.1-2
'http://archive.ubuntu.com/ubuntu/pool/main/p/pkgconf/pkgconf_1.8.1-2.dsc' pkgconf_1.8.1-2.dsc 1638 SHA512:9c27cecac22ac56a68fb423384b920b64f8f9adc29015cd6dcc43baa43d39ff77bc7261f64034ab949ddb4edfe9410d363fb64629b10dd9184b8bce7a78db42e
'http://archive.ubuntu.com/ubuntu/pool/main/p/pkgconf/pkgconf_1.8.1.orig.tar.xz' pkgconf_1.8.1.orig.tar.xz 302372 SHA512:7a7d5204c1c9bfb6578bda56f299d1fa0300e69a133a65730b10ad77aefbf26fceb74ae77cecda326b3ed5db5736f27fcce94764b3a56d40f4bb99fecdc80bba
'http://archive.ubuntu.com/ubuntu/pool/main/p/pkgconf/pkgconf_1.8.1-2.debian.tar.xz' pkgconf_1.8.1-2.debian.tar.xz 15556 SHA512:b1f41553a2dbec8b25d46e6bb7aa55b948030a8557d9ad0435c1922ce7fb033fec80026653440ce03a04a99785edf6118eb7c62a5b92b460eade2f205b8a77da
```

### `dpkg` source package: `procps=2:4.0.3-1ubuntu1.23.10.1`

Binary Packages:

- `libproc2-0:amd64=2:4.0.3-1ubuntu1.23.10.1`
- `procps=2:4.0.3-1ubuntu1.23.10.1`

Licenses: (parsed from: `/usr/share/doc/libproc2-0/copyright`, `/usr/share/doc/procps/copyright`)

- `GPL-2`
- `GPL-2.0+`
- `LGPL-2`
- `LGPL-2.0+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris procps=2:4.0.3-1ubuntu1.23.10.1
'http://archive.ubuntu.com/ubuntu/pool/main/p/procps/procps_4.0.3-1ubuntu1.23.10.1.dsc' procps_4.0.3-1ubuntu1.23.10.1.dsc 2113 SHA512:1273187f092cc2c9abc30f4459d0e7357d71b3d65c3971f2cda370f84183b0ef2783961cca2662b52875250c2702883a65203073abc345019cb4a6bcaeeb2f9d
'http://archive.ubuntu.com/ubuntu/pool/main/p/procps/procps_4.0.3.orig.tar.xz' procps_4.0.3.orig.tar.xz 1294992 SHA512:be9dc5ac4a50fc1b8256af44ac2c5b50f74ef5e48c5c3dcac2779d508988daf3b60989d22db8fc8b699c2f2f338ad367e91b9c01ab46ac9fa0d5c5bbec6f16af
'http://archive.ubuntu.com/ubuntu/pool/main/p/procps/procps_4.0.3-1ubuntu1.23.10.1.debian.tar.xz' procps_4.0.3-1ubuntu1.23.10.1.debian.tar.xz 34400 SHA512:dc9c3dac33bfaabc2cc36540c96b2ac7501ab9002579d9d934fd4ac9ce4fe1c588dcaabf6e8dcff6aea3a73ad94d1e1ea3a04be4d9b729c4ef6671e978632153
```

### `dpkg` source package: `publicsuffix=20230209.2326-1`

Binary Packages:

- `publicsuffix=20230209.2326-1`

Licenses: (parsed from: `/usr/share/doc/publicsuffix/copyright`)

- `CC0`
- `MPL-2.0`

Source:

```console
$ apt-get source -qq --print-uris publicsuffix=20230209.2326-1
'http://archive.ubuntu.com/ubuntu/pool/main/p/publicsuffix/publicsuffix_20230209.2326-1.dsc' publicsuffix_20230209.2326-1.dsc 1409 SHA512:8b56ee4e46f86efa9fc17821d59f6e1e17d1b1b9074c72439fb698d59d8bb050941313e7dfccfbbcbbd1688e07dd0303fb234f59f0f9731bc2512f98444dac72
'http://archive.ubuntu.com/ubuntu/pool/main/p/publicsuffix/publicsuffix_20230209.2326.orig.tar.gz' publicsuffix_20230209.2326.orig.tar.gz 112089 SHA512:56f8d8d5c2bace5eedf0ff38ae772cb3e071725a7df5dd4779936331024d9a6f162677e0523b0b76020ec543e74811c371ff4347464501d3a4eacea92abf445b
'http://archive.ubuntu.com/ubuntu/pool/main/p/publicsuffix/publicsuffix_20230209.2326-1.debian.tar.xz' publicsuffix_20230209.2326-1.debian.tar.xz 15148 SHA512:85dc78ca01a9920f6ccbe28b9c03f9ad1a92feec9fa332b86edbe4647cb68f23bdf0347ea03039bc72166057b63edac5910d7538d0276cde475ad713c015ad24
```

### `dpkg` source package: `python3-defaults=3.11.4-5`

Binary Packages:

- `libpython3-dev:amd64=3.11.4-5`
- `libpython3-stdlib:amd64=3.11.4-5`
- `python3=3.11.4-5`
- `python3-minimal=3.11.4-5`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris python3-defaults=3.11.4-5
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3-defaults/python3-defaults_3.11.4-5.dsc' python3-defaults_3.11.4-5.dsc 3001 SHA512:d39f4d0c80dc998ec124eea3ec2c9cbc317ffdeb9d08cb98802400b889c540f48e21761c0da460c392402dac7fc481884568006b3d443226102e3b7cccec2f83
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3-defaults/python3-defaults_3.11.4-5.tar.gz' python3-defaults_3.11.4-5.tar.gz 146763 SHA512:493fe4be0396bd5a4dc23da544756450ad8f4ee0502345f2f0e7be43642a560d5e6144d3c693fa223f010d466481329cdda6347c733c890adb8ff18fb7e9122c
```

### `dpkg` source package: `python3.11=3.11.6-3`

Binary Packages:

- `libpython3.11:amd64=3.11.6-3`
- `libpython3.11-dev:amd64=3.11.6-3`
- `libpython3.11-minimal:amd64=3.11.6-3`
- `libpython3.11-stdlib:amd64=3.11.6-3`
- `python3.11=3.11.6-3`
- `python3.11-minimal=3.11.6-3`

Licenses: (parsed from: `/usr/share/doc/libpython3.11/copyright`, `/usr/share/doc/libpython3.11-dev/copyright`, `/usr/share/doc/libpython3.11-minimal/copyright`, `/usr/share/doc/libpython3.11-stdlib/copyright`, `/usr/share/doc/python3.11/copyright`, `/usr/share/doc/python3.11-minimal/copyright`)

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
$ apt-get source -qq --print-uris python3.11=3.11.6-3
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3.11/python3.11_3.11.6-3.dsc' python3.11_3.11.6-3.dsc 3655 SHA512:15109521f97428aeb6ab63d28b52d38096b96ea2c2bb4580dee68c3657dbae702a3e510b442088ae935dfa75e477c2e362cb4c44c2542fd6288f5fab803e4ce1
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3.11/python3.11_3.11.6.orig.tar.xz' python3.11_3.11.6.orig.tar.xz 20067204 SHA512:94b1038f6f53de0c44f99f72ed0f2e0791fd9d2a325ae00ba145b2b2c332c27b300b3ea3473017518089478f15e01867b1bb203c16610039cce36f8366de341a
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3.11/python3.11_3.11.6-3.debian.tar.xz' python3.11_3.11.6-3.debian.tar.xz 213928 SHA512:859c5e0fc4c1fb1dbf77a4608d0987aa018d91c2ae4960639fbfc4f51edae4817b93d8370e77a0ff24a2a37b6752b5e971887bc0bbd56685b1d206130d188662
```

### `dpkg` source package: `readline=8.2-1.3`

Binary Packages:

- `libreadline8:amd64=8.2-1.3`
- `readline-common=8.2-1.3`

Licenses: (parsed from: `/usr/share/doc/libreadline8/copyright`, `/usr/share/doc/readline-common/copyright`)

- `GFDL`
- `GFDL-NIV-1.3+`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `ISC-no-attribution`

Source:

```console
$ apt-get source -qq --print-uris readline=8.2-1.3
'http://archive.ubuntu.com/ubuntu/pool/main/r/readline/readline_8.2-1.3.dsc' readline_8.2-1.3.dsc 2553 SHA512:ae771c7d5d13e41c6b033ca1862ad2b7d78c1ea365f592a3703d1659b47c9b3ec068c5261dab470cec73b2d065d1f75e04fbd79d6800e65c114ac4267244a919
'http://archive.ubuntu.com/ubuntu/pool/main/r/readline/readline_8.2.orig.tar.gz' readline_8.2.orig.tar.gz 3043952 SHA512:0a451d459146bfdeecc9cdd94bda6a6416d3e93abd80885a40b334312f16eb890f8618a27ca26868cebbddf1224983e631b1cbc002c1a4d1cd0d65fba9fea49a
'http://archive.ubuntu.com/ubuntu/pool/main/r/readline/readline_8.2-1.3.debian.tar.xz' readline_8.2-1.3.debian.tar.xz 30016 SHA512:17d127126bcabeac5215266752c21a9f154f5c252319fa23885c4e5cd2d43372f830f9bc730a21d45e5ce6c4b1a3f3f649144febf2203f5c617b2e507b807a2b
```

### `dpkg` source package: `rpcsvc-proto=1.4.2-0ubuntu6`

Binary Packages:

- `rpcsvc-proto=1.4.2-0ubuntu6`

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
$ apt-get source -qq --print-uris rpcsvc-proto=1.4.2-0ubuntu6
'http://archive.ubuntu.com/ubuntu/pool/main/r/rpcsvc-proto/rpcsvc-proto_1.4.2-0ubuntu6.dsc' rpcsvc-proto_1.4.2-0ubuntu6.dsc 2113 SHA512:df8458b423e2d3f8d6da5c6fc19be2ad4ae50d7513e3fa98656b05a734fdc26b2403984ea7da8a0cb5c270f63feae7c258e1f817a3f4a27ffb25107e25f43525
'http://archive.ubuntu.com/ubuntu/pool/main/r/rpcsvc-proto/rpcsvc-proto_1.4.2.orig.tar.xz' rpcsvc-proto_1.4.2.orig.tar.xz 171620 SHA512:631fbfc00af94c5d7def0759f27e97dc14d400b4468c906719ae18ecef74815730798c882d1aaa4f90359224e7b829019b786baddc3097905b54f940ca85a714
'http://archive.ubuntu.com/ubuntu/pool/main/r/rpcsvc-proto/rpcsvc-proto_1.4.2-0ubuntu6.debian.tar.xz' rpcsvc-proto_1.4.2-0ubuntu6.debian.tar.xz 4268 SHA512:b7ee77b3714b10471fa5be73655f6ce37bd8ca4bfdb07011ac3621723616e69a2323dea9c93ee9ac5d2e9fd0230347224eaa8ae556ec2f2d4b399ec250a5008c
```

### `dpkg` source package: `rtmpdump=2.4+20151223.gitfa8646d.1-2build4`

Binary Packages:

- `librtmp1:amd64=2.4+20151223.gitfa8646d.1-2build4`

Licenses: (parsed from: `/usr/share/doc/librtmp1/copyright`)

- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris rtmpdump=2.4+20151223.gitfa8646d.1-2build4
'http://archive.ubuntu.com/ubuntu/pool/main/r/rtmpdump/rtmpdump_2.4%2b20151223.gitfa8646d.1-2build4.dsc' rtmpdump_2.4+20151223.gitfa8646d.1-2build4.dsc 2431 SHA512:7536b21c9c8be02e06171db49bf0b653e4b7738e6c01f74b0b7433c2986c731eafd1743f87836e7250a744d0e34dc700685bbe7128956a274e9a9832d32c891e
'http://archive.ubuntu.com/ubuntu/pool/main/r/rtmpdump/rtmpdump_2.4%2b20151223.gitfa8646d.1.orig.tar.gz' rtmpdump_2.4+20151223.gitfa8646d.1.orig.tar.gz 142213 SHA512:bdfcbab73179d614a295a7b136ea4c9d0ce4620883b493f298362784d245608cd6ad4b0ad30f94ed73a086b4555399521ae9e95b6375fce75e455ae68c055e7b
'http://archive.ubuntu.com/ubuntu/pool/main/r/rtmpdump/rtmpdump_2.4%2b20151223.gitfa8646d.1-2build4.debian.tar.xz' rtmpdump_2.4+20151223.gitfa8646d.1-2build4.debian.tar.xz 8376 SHA512:b01ac33a7251e3c0fad21897d31710766136027b656cb29903cf8f695893648631037a96fa18aa40eae7ad363394344aad4f2fae152622618b88f22133c03578
```

### `dpkg` source package: `sed=4.9-1`

Binary Packages:

- `sed=4.9-1`

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
$ apt-get source -qq --print-uris sed=4.9-1
'http://archive.ubuntu.com/ubuntu/pool/main/s/sed/sed_4.9-1.dsc' sed_4.9-1.dsc 2077 SHA512:5c7b4495f8e2e7f93f81d8bd01fc49905b35226d537c87c1ab87b8374a9afd446d7c3ffcc97d007d1b304cc5928b421c1bea3823b77aaa37dda05d08101bd645
'http://archive.ubuntu.com/ubuntu/pool/main/s/sed/sed_4.9.orig.tar.xz' sed_4.9.orig.tar.xz 1397092 SHA512:36157a4b4a2430cf421b7bd07f1675d680d9f1616be96cf6ad6ee74a9ec0fe695f8d0b1e1f0b008bbb33cc7fcde5e1c456359bbbc63f8aebdd4fedc3982cf6dc
'http://archive.ubuntu.com/ubuntu/pool/main/s/sed/sed_4.9.orig.tar.xz.asc' sed_4.9.orig.tar.xz.asc 833 SHA512:ceb235850184b99017783486e182ade9db38313d20b2b34d23f54d8affe180f7a191139b993e8ec7718ca33eff732f547ca4b3b59aaf865feaae611dfeae5c46
'http://archive.ubuntu.com/ubuntu/pool/main/s/sed/sed_4.9-1.debian.tar.xz' sed_4.9-1.debian.tar.xz 62616 SHA512:5f10389226e093abdf014187dd1e097522938051594158265b0f294cea36b45043081f89a40ec8a91f7fb9a9b907699ca02752cbeac2a5b156f0f702e97881c8
```

### `dpkg` source package: `sensible-utils=0.0.20`

Binary Packages:

- `sensible-utils=0.0.20`

Licenses: (parsed from: `/usr/share/doc/sensible-utils/copyright`)

- `All-permissive`
- `GPL-2`
- `GPL-2+`
- `configure`
- `installsh`

Source:

```console
$ apt-get source -qq --print-uris sensible-utils=0.0.20
'http://archive.ubuntu.com/ubuntu/pool/main/s/sensible-utils/sensible-utils_0.0.20.dsc' sensible-utils_0.0.20.dsc 1737 SHA512:0b0267948347d7aace0c6117228ffa005e5c36e61c9289c409c33d78349fed34956db655541774ec161dc4497d95ccc9d609557f6aaf1d335ced3689ef16a744
'http://archive.ubuntu.com/ubuntu/pool/main/s/sensible-utils/sensible-utils_0.0.20.tar.xz' sensible-utils_0.0.20.tar.xz 70608 SHA512:439b783003f9b9361baec01f2888f9638bf7d670b90e7262c50fdff2b724f53f83a776bda385003f61b0bbf37c3213208642e2f1289e93a1ba6b1da2107cb02f
```

### `dpkg` source package: `shadow=1:4.13+dfsg1-1ubuntu1.1`

Binary Packages:

- `login=1:4.13+dfsg1-1ubuntu1.1`
- `passwd=1:4.13+dfsg1-1ubuntu1.1`

Licenses: (parsed from: `/usr/share/doc/login/copyright`, `/usr/share/doc/passwd/copyright`)

- `BSD-3-clause`
- `GPL-1`
- `GPL-2`
- `GPL-2+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris shadow=1:4.13+dfsg1-1ubuntu1.1
'http://archive.ubuntu.com/ubuntu/pool/main/s/shadow/shadow_4.13%2bdfsg1-1ubuntu1.1.dsc' shadow_4.13+dfsg1-1ubuntu1.1.dsc 2221 SHA512:8f7f07c2e293ad3cf1bf256f344e87cb8f1499a302248777a21debd2649226c9d99b1dcd06d8065a66296a43eb6fe800bbc9e2b3c190693f7215d6bcbad1c90e
'http://archive.ubuntu.com/ubuntu/pool/main/s/shadow/shadow_4.13%2bdfsg1.orig.tar.xz' shadow_4.13+dfsg1.orig.tar.xz 1811752 SHA512:27106ca26d6e4c9e5833cf79811b10f656ade547bbc18b87faf79bbe0581a9e1467cbb6c354320e2d5233d17208d77742ebf197d32b6d2f08439e37e368ded1d
'http://archive.ubuntu.com/ubuntu/pool/main/s/shadow/shadow_4.13%2bdfsg1-1ubuntu1.1.debian.tar.xz' shadow_4.13+dfsg1-1ubuntu1.1.debian.tar.xz 93460 SHA512:69767fd4a8d59f6642877df62f6888097e3c6ec4afedc566aa2362aa76e1d447d2d79ef02d398d1793fc97528e6f111b45937621a88b184e6eec6e24f851a700
```

### `dpkg` source package: `six=1.16.0-4`

Binary Packages:

- `python3-six=1.16.0-4`

Licenses: (parsed from: `/usr/share/doc/python3-six/copyright`)

- `Expat`

Source:

```console
$ apt-get source -qq --print-uris six=1.16.0-4
'http://archive.ubuntu.com/ubuntu/pool/main/s/six/six_1.16.0-4.dsc' six_1.16.0-4.dsc 2069 SHA512:e17664b1ad4ebbbd878a87b13196f0d3a4345aef6461fe3bac7f18ff045a146d69062422913d53ce4f65960949ddc74deaa91f984b36e9bf255b4fc8c5ae5df4
'http://archive.ubuntu.com/ubuntu/pool/main/s/six/six_1.16.0.orig.tar.gz' six_1.16.0.orig.tar.gz 34041 SHA512:076fe31c8f03b0b52ff44346759c7dc8317da0972403b84dfe5898179f55acdba6c78827e0f8a53ff20afe8b76432c6fe0d655a75c24259d9acbaa4d9e8015c0
'http://archive.ubuntu.com/ubuntu/pool/main/s/six/six_1.16.0-4.debian.tar.xz' six_1.16.0-4.debian.tar.xz 4840 SHA512:3fc6474d75304c5f9604fb096c8b557d69d15f25c9d2e90e9c2238f52cf45aa26668750569a19b34b55c4d157c9d5f9cd1d1c06ccd6c2cdd51e8ee0f5152dd81
```

### `dpkg` source package: `sqlite3=3.42.0-1ubuntu0.1`

Binary Packages:

- `libsqlite3-0:amd64=3.42.0-1ubuntu0.1`

Licenses: (parsed from: `/usr/share/doc/libsqlite3-0/copyright`)

- `GPL-2`
- `GPL-2+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris sqlite3=3.42.0-1ubuntu0.1
'http://archive.ubuntu.com/ubuntu/pool/main/s/sqlite3/sqlite3_3.42.0-1ubuntu0.1.dsc' sqlite3_3.42.0-1ubuntu0.1.dsc 2601 SHA512:3769d4bffa700d8ff19f93c378ab6fba0aae5f2d265369a176eb3094da3681a7015757ecd49f2b47fff5206a8a5d04e79ec08d93924df29f1010d3006b2173f6
'http://archive.ubuntu.com/ubuntu/pool/main/s/sqlite3/sqlite3_3.42.0.orig-www.tar.xz' sqlite3_3.42.0.orig-www.tar.xz 5708628 SHA512:485fcc839414f74a41f4cf795b597fea793016502a9659d989679f3ecccf085909bde655bc605ce8a89029f2ff220e3977dfd35306ccab2c1d23b2e66ed8c6d6
'http://archive.ubuntu.com/ubuntu/pool/main/s/sqlite3/sqlite3_3.42.0.orig.tar.xz' sqlite3_3.42.0.orig.tar.xz 8129004 SHA512:a39b8b33761751d90d3b669834bfe10be81bc66bc8c8cfb80fe3d7690c16c74bcda0c9df0be5af855cb5c6b93829de8f22c2307edc01fb61721027ffb118b896
'http://archive.ubuntu.com/ubuntu/pool/main/s/sqlite3/sqlite3_3.42.0-1ubuntu0.1.debian.tar.xz' sqlite3_3.42.0-1ubuntu0.1.debian.tar.xz 30500 SHA512:5a3c648faa38f9932a086864b6c9cf23e877eb9ae3e0119f42fbcaa2e91f457de6c640d2b0eedef6e8346dbc35742df945977af67ea10712d3b083389ca3a51c
```

### `dpkg` source package: `systemd=253.5-1ubuntu6.1`

Binary Packages:

- `libsystemd0:amd64=253.5-1ubuntu6.1`
- `libudev1:amd64=253.5-1ubuntu6.1`

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
$ apt-get source -qq --print-uris systemd=253.5-1ubuntu6.1
'http://archive.ubuntu.com/ubuntu/pool/main/s/systemd/systemd_253.5-1ubuntu6.1.dsc' systemd_253.5-1ubuntu6.1.dsc 6910 SHA512:7aa167b2a6de8bd48b53a4bda661659fd340cf5bb31c7a848442abf3e201c761e478a41342ebaca016c376630fc25e6e88bc541222aaac5793fc3af74638cd91
'http://archive.ubuntu.com/ubuntu/pool/main/s/systemd/systemd_253.5.orig.tar.gz' systemd_253.5.orig.tar.gz 12015672 SHA512:39709b485cd9287e26ac8e973fa1692b280bec3b96e1da6667e4a4f2ac2228aa072b22802720a254698d32c82f5306d7feb32229e4b6d54cc0e2b1e2caa4cc2e
'http://archive.ubuntu.com/ubuntu/pool/main/s/systemd/systemd_253.5-1ubuntu6.1.debian.tar.xz' systemd_253.5-1ubuntu6.1.debian.tar.xz 220212 SHA512:613fa22f71f77d43f1c483b322f2e4601418ae584948e3088386f0edbf14e643730126de1d5b04bf5921c169cbe4a3a5d69c135bb8556b4e1098f97818bf1274
```

### `dpkg` source package: `sysvinit=3.07-1ubuntu1`

Binary Packages:

- `sysvinit-utils=3.07-1ubuntu1`

Licenses: (parsed from: `/usr/share/doc/sysvinit-utils/copyright`)

- `GPL-2`
- `GPL-2.0`
- `GPL-2.0+`
- `GPL-3`
- `GPL-3.0`

Source:

```console
$ apt-get source -qq --print-uris sysvinit=3.07-1ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/s/sysvinit/sysvinit_3.07-1ubuntu1.dsc' sysvinit_3.07-1ubuntu1.dsc 2466 SHA512:dfc1df22548ae8f82c974092aab9b701323b6d90921a5cfd203ea0109aa11c21490b4c052cd2a4ea9533651b124b9634d4767c7b144b70c4ae8bee473ad2a742
'http://archive.ubuntu.com/ubuntu/pool/main/s/sysvinit/sysvinit_3.07.orig.tar.gz' sysvinit_3.07.orig.tar.gz 513168 SHA512:16e20b9765c6b5e50b2f10fe9e88e00eddb79eb8ebfb632ef98a98796aaaf07a5016f89b1efacdeb36409fd1638d79bce01186d5c7fc907c63d6a9a7195428d9
'http://archive.ubuntu.com/ubuntu/pool/main/s/sysvinit/sysvinit_3.07-1ubuntu1.debian.tar.xz' sysvinit_3.07-1ubuntu1.debian.tar.xz 135556 SHA512:a3a284fa52a67fc81d29d0df0acb64833ae9ab30864aecfcb7f5545e1bf0eb6fcb99f4b76103b2cf98fca12cde421c5c0e66a2559ef7b92db9d39aa641f3d865
```

### `dpkg` source package: `tar=1.34+dfsg-1.2ubuntu1.1`

Binary Packages:

- `tar=1.34+dfsg-1.2ubuntu1.1`

Licenses: (parsed from: `/usr/share/doc/tar/copyright`)

- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `GPL-3+ with Bison exception`
- `LGPL-3`
- `LGPL-3+`

Source:

```console
$ apt-get source -qq --print-uris tar=1.34+dfsg-1.2ubuntu1.1
'http://archive.ubuntu.com/ubuntu/pool/main/t/tar/tar_1.34%2bdfsg-1.2ubuntu1.1.dsc' tar_1.34+dfsg-1.2ubuntu1.1.dsc 1805 SHA512:67c69e85ea9dfe43797e12afd46f363c9c5aecd8f80432adb999a79c9515d27054aefef30fbc8ee285a3ee7321ee193221462f1a3d679559a6bfe08fa1c37850
'http://archive.ubuntu.com/ubuntu/pool/main/t/tar/tar_1.34%2bdfsg.orig.tar.xz' tar_1.34+dfsg.orig.tar.xz 1981736 SHA512:ec5553c53c4a5f523f872a8095f699c17bf41400fbe2f0f8b45291ccbaf9ac51dea8445c81bd95697f8853c95dcad3250071d23dbbcab857a428ee92e647bde9
'http://archive.ubuntu.com/ubuntu/pool/main/t/tar/tar_1.34%2bdfsg-1.2ubuntu1.1.debian.tar.xz' tar_1.34+dfsg-1.2ubuntu1.1.debian.tar.xz 21572 SHA512:f15e5020b656da12968c3db5845d0ca716c7d72141b5d617847b56ea7b68ea18378504c4a009227f2f6868e31fbb5f38fdb5ad9c9d3a034e1897da92dff01107
```

### `dpkg` source package: `tiff=4.5.1+git230720-1ubuntu1.1`

Binary Packages:

- `libtiff6:amd64=4.5.1+git230720-1ubuntu1.1`

Licenses: (parsed from: `/usr/share/doc/libtiff6/copyright`)

- `Hylafax`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `tzdata=2024a-0ubuntu0.23.10`

Binary Packages:

- `tzdata=2024a-0ubuntu0.23.10`
- `tzdata-icu=2024a-0ubuntu0.23.10`

Licenses: (parsed from: `/usr/share/doc/tzdata/copyright`, `/usr/share/doc/tzdata-icu/copyright`)

- `ICU`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris tzdata=2024a-0ubuntu0.23.10
'http://archive.ubuntu.com/ubuntu/pool/main/t/tzdata/tzdata_2024a-0ubuntu0.23.10.dsc' tzdata_2024a-0ubuntu0.23.10.dsc 2699 SHA512:70a875967a528f6f53115308263028c924ba237ac60df25123d429100516578e3a3aa5c6b2769ad3a00b7e2c853af89053fdab2dc48702cf14986120cc3a81a3
'http://archive.ubuntu.com/ubuntu/pool/main/t/tzdata/tzdata_2024a.orig.tar.gz' tzdata_2024a.orig.tar.gz 451270 SHA512:1f09f1b2327cc9e1afc7e9045e83ee3377918dafe1bee2f282b6991828d03b3c70a4d3a17f9207dfb1361bb25bc214a8922a756e84fa114e9ba476226db57236
'http://archive.ubuntu.com/ubuntu/pool/main/t/tzdata/tzdata_2024a.orig.tar.gz.asc' tzdata_2024a.orig.tar.gz.asc 833 SHA512:a06ddc95002f2dcd3c071d020a74bc98aae2cbf56a502718f9bc08e90e0075b17aaaa653ceecd49a1133cdadfc43134365043f827b19c7dad68050dbda6ba77e
'http://archive.ubuntu.com/ubuntu/pool/main/t/tzdata/tzdata_2024a-0ubuntu0.23.10.debian.tar.xz' tzdata_2024a-0ubuntu0.23.10.debian.tar.xz 183208 SHA512:a121e2ff4ba3ded0a9a3f1a6933228095a909579e2c6ad6658448fa75a0627677529bcae1e2092e8142ac0abf5cd3d183b5c31a3e8d8bb3f880699f52757a522
```

### `dpkg` source package: `ubuntu-keyring=2021.03.26`

Binary Packages:

- `ubuntu-keyring=2021.03.26`

Licenses: (parsed from: `/usr/share/doc/ubuntu-keyring/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris ubuntu-keyring=2021.03.26
'http://archive.ubuntu.com/ubuntu/pool/main/u/ubuntu-keyring/ubuntu-keyring_2021.03.26.dsc' ubuntu-keyring_2021.03.26.dsc 1855 SHA512:7502f4f4d9a288fab9fb84b6ae5f8500cb3f14c68ed586b489dee95f12087b232bcecd9369e98258bb710afda50e5672dfbc6422b1436e896fb529dec8832252
'http://archive.ubuntu.com/ubuntu/pool/main/u/ubuntu-keyring/ubuntu-keyring_2021.03.26.tar.gz' ubuntu-keyring_2021.03.26.tar.gz 34529 SHA512:04a76e2bfa88fb428face9e01976ff98a3a26fe2b555340c14200fc6099ee3b474a6733486cedfe933933c0a6826ee3550660499d7b26bda8a27a620b1d6a35f
```

### `dpkg` source package: `unzip=6.0-28ubuntu1.1`

Binary Packages:

- `unzip=6.0-28ubuntu1.1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris unzip=6.0-28ubuntu1.1
'http://archive.ubuntu.com/ubuntu/pool/main/u/unzip/unzip_6.0-28ubuntu1.1.dsc' unzip_6.0-28ubuntu1.1.dsc 1819 SHA512:e2fc9fdc43f1fc4fc53fe31c0d5690b6414293c92d11761ff815cc50eb42123f6ab977d59110d66627d32e7eca3920e90fea41dc928213feb1289c6e95df455c
'http://archive.ubuntu.com/ubuntu/pool/main/u/unzip/unzip_6.0.orig.tar.gz' unzip_6.0.orig.tar.gz 1376845 SHA512:0694e403ebc57b37218e00ec1a406cae5cc9c5b52b6798e0d4590840b6cdbf9ddc0d9471f67af783e960f8fa2e620394d51384257dca23d06bcd90224a80ce5d
'http://archive.ubuntu.com/ubuntu/pool/main/u/unzip/unzip_6.0-28ubuntu1.1.debian.tar.xz' unzip_6.0-28ubuntu1.1.debian.tar.xz 28832 SHA512:9c9bbedc5afefad409d39f3b8228b3ca7b7d52629c7b27bf7a062127ea837c38cb24f4b5f11500a41204e399e920b772d3159239da64db6fd909976b4f40313a
```

### `dpkg` source package: `usrmerge=35ubuntu1`

Binary Packages:

- `usrmerge=35ubuntu1`

Licenses: (parsed from: `/usr/share/doc/usrmerge/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris usrmerge=35ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/u/usrmerge/usrmerge_35ubuntu1.dsc' usrmerge_35ubuntu1.dsc 1717 SHA512:187148b5844858d99506dadb3dc0f18f439df2f01835d1849d07cccfc2819405a0cd722a68ab67e483b4d5fd69e14ce7cf376710ef59edc4ec21610f98dc3c40
'http://archive.ubuntu.com/ubuntu/pool/main/u/usrmerge/usrmerge_35ubuntu1.tar.xz' usrmerge_35ubuntu1.tar.xz 15240 SHA512:5116c42163a7b972282ca7af66c268f29197a725fc91020bcd2fcd7ba31f150a705749f3fcf7b02b45d778ffff93e4bc93af0db9491dd28f82e7be9793e9fb0d
```

### `dpkg` source package: `util-linux=2.39.1-4ubuntu2.2`

Binary Packages:

- `bsdutils=1:2.39.1-4ubuntu2.2`
- `libblkid1:amd64=2.39.1-4ubuntu2.2`
- `libmount1:amd64=2.39.1-4ubuntu2.2`
- `libsmartcols1:amd64=2.39.1-4ubuntu2.2`
- `libuuid1:amd64=2.39.1-4ubuntu2.2`
- `mount=2.39.1-4ubuntu2.2`
- `util-linux=2.39.1-4ubuntu2.2`

Licenses: (parsed from: `/usr/share/doc/bsdutils/copyright`, `/usr/share/doc/libblkid1/copyright`, `/usr/share/doc/libmount1/copyright`, `/usr/share/doc/libsmartcols1/copyright`, `/usr/share/doc/libuuid1/copyright`, `/usr/share/doc/mount/copyright`, `/usr/share/doc/util-linux/copyright`)

- `BSD-3-clause`
- `BSD-4-clause`
- `BSLA`
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
$ apt-get source -qq --print-uris util-linux=2.39.1-4ubuntu2.2
'http://archive.ubuntu.com/ubuntu/pool/main/u/util-linux/util-linux_2.39.1-4ubuntu2.2.dsc' util-linux_2.39.1-4ubuntu2.2.dsc 4651 SHA512:1749aa06909567787f3a1881c72c17643f88a3600ded684f028653418f0bb65da2baad1b48a863df2d48b85b366cc62dace80ecd6162ac682daab27e1189275e
'http://archive.ubuntu.com/ubuntu/pool/main/u/util-linux/util-linux_2.39.1.orig.tar.xz' util-linux_2.39.1.orig.tar.xz 8351164 SHA512:8fe2c9014f6161330610f7470b870855cecbd3fab9c187b75d8f22e16573c82516050479be39cfb9f7dd6d7ef1cc298d31d839b194dda5ec4daf0d1197ac71e9
'http://archive.ubuntu.com/ubuntu/pool/main/u/util-linux/util-linux_2.39.1-4ubuntu2.2.debian.tar.xz' util-linux_2.39.1-4ubuntu2.2.debian.tar.xz 103512 SHA512:505638b4714a39e703b457ef48a343b6a18f5f68be8eb57a0e29f35986deb38130a46c8770a1a235197946d91bcf2ff07c07e2fd321127e52594902d9a02ce9e
```

### `dpkg` source package: `xauth=1:1.1.2-1`

Binary Packages:

- `xauth=1:1.1.2-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris xauth=1:1.1.2-1
'http://archive.ubuntu.com/ubuntu/pool/main/x/xauth/xauth_1.1.2-1.dsc' xauth_1.1.2-1.dsc 1840 SHA512:ec8325cddc322a10064a9ee996c2bfe1d83759cf09947c4c9bca09ae30e2a4c7c502ec266dc3f8e06d714a68f3a54d34841c42a3cfe9a5a6a746c8f55c9856cd
'http://archive.ubuntu.com/ubuntu/pool/main/x/xauth/xauth_1.1.2.orig.tar.gz' xauth_1.1.2.orig.tar.gz 214621 SHA512:9de9cec29e453824aad43824ff961ae5eada6604a190bc353bb665c40c6a1d40d436c44bf50209686c681c6adea6a08f456e02365de8f0feb3fa8a8fc01f5577
'http://archive.ubuntu.com/ubuntu/pool/main/x/xauth/xauth_1.1.2-1.diff.gz' xauth_1.1.2-1.diff.gz 18091 SHA512:2835e10e8ef17349d6213a76b28e8643f9bf5dd70de7a84ebe6fbcb21666ce0dba28cdfb8d04b9d4820447f4dbc94bbc217d573373ed2b83b09f5582c53b2920
```

### `dpkg` source package: `xxhash=0.8.1-1`

Binary Packages:

- `libxxhash0:amd64=0.8.1-1`

Licenses: (parsed from: `/usr/share/doc/libxxhash0/copyright`)

- `BSD-2-clause`
- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris xxhash=0.8.1-1
'http://archive.ubuntu.com/ubuntu/pool/main/x/xxhash/xxhash_0.8.1-1.dsc' xxhash_0.8.1-1.dsc 1966 SHA512:645799311fdf21568b23134cdf586a54bb32b58639adb8ebc1f5ad26fdfdc485506c87d763133163fde705b2f904d6f01f50e4d13ebec2b476d38e66ded2bf22
'http://archive.ubuntu.com/ubuntu/pool/main/x/xxhash/xxhash_0.8.1.orig.tar.gz' xxhash_0.8.1.orig.tar.gz 171552 SHA512:12feedd6a1859ef55e27218dbd6dcceccbb5a4da34cd80240d2f7d44cd246c7afdeb59830c2d5b90189bb5159293532208bf5bb622250102e12d6e1bad14a193
'http://archive.ubuntu.com/ubuntu/pool/main/x/xxhash/xxhash_0.8.1-1.debian.tar.xz' xxhash_0.8.1-1.debian.tar.xz 4572 SHA512:e59d4fc6f736d3af6f7be3ec64fc1ee4382e917a942e4000159652082e2f73f52ae0f72adb98505ac9bd8894a89800e21c0913ba4b511959f07a2bc84c341920
```

### `dpkg` source package: `xz-utils=5.4.1-0.2`

Binary Packages:

- `liblzma5:amd64=5.4.1-0.2`

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

Source:

```console
$ apt-get source -qq --print-uris xz-utils=5.4.1-0.2
'http://archive.ubuntu.com/ubuntu/pool/main/x/xz-utils/xz-utils_5.4.1-0.2.dsc' xz-utils_5.4.1-0.2.dsc 2621 SHA512:0c07970eedd5b1f67f8750f99dd7f86a1aef12cb1f1b3691fab1b1311d55de76ad597ac55c4e845adee3cdf8d8ba96ceeaed810b6688419934c20e3bafb8bb15
'http://archive.ubuntu.com/ubuntu/pool/main/x/xz-utils/xz-utils_5.4.1.orig.tar.xz' xz-utils_5.4.1.orig.tar.xz 1485272 SHA512:f890ee5207799fbc7bb9ae031f444d39d82275b0e1b8cc7f01fdb9270050e38849bd1269db2a2f12fe87b5e23e03f9e809a5c3456d066c0a56e6f98d728553ea
'http://archive.ubuntu.com/ubuntu/pool/main/x/xz-utils/xz-utils_5.4.1.orig.tar.xz.asc' xz-utils_5.4.1.orig.tar.xz.asc 833 SHA512:0802a4ae8f8fe700288b0fb1a4c9f59f71b26fcaea88cd368d36dcfd96a1deb2380a7b9af66b84d2f4faf68ff114d9b4b4e48b5b8362c37a8e528f13a4233cf3
'http://archive.ubuntu.com/ubuntu/pool/main/x/xz-utils/xz-utils_5.4.1-0.2.debian.tar.xz' xz-utils_5.4.1-0.2.debian.tar.xz 87432 SHA512:0d83bec7f80471ef4b3c5845cc2502807bb41f111970149244de1927618ed758d4e6da455f72eaa9d76acb41d4be685b968b1a8e5883f204277fde75fbc5d79b
```

### `dpkg` source package: `z3=4.8.12-3.1`

Binary Packages:

- `libz3-4:amd64=4.8.12-3.1`
- `libz3-dev:amd64=4.8.12-3.1`

Licenses: (parsed from: `/usr/share/doc/libz3-4/copyright`, `/usr/share/doc/libz3-dev/copyright`)

- `Expat`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris z3=4.8.12-3.1
'http://archive.ubuntu.com/ubuntu/pool/universe/z/z3/z3_4.8.12-3.1.dsc' z3_4.8.12-3.1.dsc 2663 SHA512:23ff8d51f15ca24e53cb0f48e83101d9858ed82c1749ac003e914d13866e2ad2c2f58aaeb85c55f380f23438afacf682506444688897ea9fb815caa3b9ce1b0f
'http://archive.ubuntu.com/ubuntu/pool/universe/z/z3/z3_4.8.12.orig.tar.gz' z3_4.8.12.orig.tar.gz 4803435 SHA512:0b377923bdaffaca1846aa2abd61003bbecadfcdfc908ed3097d0aac8f32028ac39d93fb4a9c2e2c2bfffbdbee80aa415875f17de6c2ee2ae8e2b7921f788c6e
'http://archive.ubuntu.com/ubuntu/pool/universe/z/z3/z3_4.8.12-3.1.debian.tar.xz' z3_4.8.12-3.1.debian.tar.xz 10420 SHA512:042d06c0c66bb6328f1b90f766109de31fa9e1921c313dddccf8199f6855fbddd6272764312ebc0773f920525620fed7d45a7bb2432e5ee7b866dcec87ed773d
```

### `dpkg` source package: `zlib=1:1.2.13.dfsg-1ubuntu5`

Binary Packages:

- `zlib1g:amd64=1:1.2.13.dfsg-1ubuntu5`
- `zlib1g-dev:amd64=1:1.2.13.dfsg-1ubuntu5`

Licenses: (parsed from: `/usr/share/doc/zlib1g/copyright`, `/usr/share/doc/zlib1g-dev/copyright`)

- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris zlib=1:1.2.13.dfsg-1ubuntu5
'http://archive.ubuntu.com/ubuntu/pool/main/z/zlib/zlib_1.2.13.dfsg-1ubuntu5.dsc' zlib_1.2.13.dfsg-1ubuntu5.dsc 2968 SHA512:f464da1d48704d87d498db0b2f5e00eaa7e2b58cad27b5493fb6ab96d9ee9555522197d3b948a140bbd7f72ef29e89515c6c17297dd4a2688fb02e7145a9c855
'http://archive.ubuntu.com/ubuntu/pool/main/z/zlib/zlib_1.2.13.dfsg.orig.tar.bz2' zlib_1.2.13.dfsg.orig.tar.bz2 1239825 SHA512:266ea72465ad1f0b63e42f8275c650615829929f2ff19064144c5bb942acd31cd8581ce45781c438fce949c6d9f3fa385efa59f754761441107ca1144fb56802
'http://archive.ubuntu.com/ubuntu/pool/main/z/zlib/zlib_1.2.13.dfsg-1ubuntu5.debian.tar.xz' zlib_1.2.13.dfsg-1ubuntu5.debian.tar.xz 57068 SHA512:2fba202da1d40363e844c0baba3b8af3878087eb7b2b31ab4ba5f26616b1dc9f135483036cc42fbf53a1c359a19370c491d49f01058c91180485229ac3b36343
```
