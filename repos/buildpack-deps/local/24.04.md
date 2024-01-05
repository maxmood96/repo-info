# `buildpack-deps:noble`

## Docker Metadata

- Image ID: `sha256:e43f1eb6d168f3b288eff2a7b17e53a1b44626f2867d657f1444e572eb9509bc`
- Created: `2024-01-04T20:37:06.491793871Z`
- Virtual Size: ~ 907.20 Mb  
  (total size of all layers on-disk)
- Arch: `linux`/`amd64`
- Command: `["/bin/bash"]`
- Environment:
  - `PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin`
- Labels:
  - `org.opencontainers.image.ref.name=ubuntu`
  - `org.opencontainers.image.version=24.04`

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

### `dpkg` source package: `apr-util=1.6.3-1ubuntu1`

Binary Packages:

- `libaprutil1:amd64=1.6.3-1ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libaprutil1/copyright`)

- `Apache-2.0`

Source:

```console
$ apt-get source -qq --print-uris apr-util=1.6.3-1ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/a/apr-util/apr-util_1.6.3-1ubuntu1.dsc' apr-util_1.6.3-1ubuntu1.dsc 2904 SHA512:3db7e6c9beab7833a9a913011f84a8b59c617202a4941d3054fe649da609bbd19c20f216dc5eaa9fc0455be0369c52f4537957371f892008da7ba0cb78dc1055
'http://archive.ubuntu.com/ubuntu/pool/main/a/apr-util/apr-util_1.6.3.orig.tar.bz2' apr-util_1.6.3.orig.tar.bz2 432692 SHA512:8050a481eeda7532ef3751dbd8a5aa6c48354d52904a856ef9709484f4b0cc2e022661c49ddf55ec58253db22708ee0607dfa7705d9270e8fee117ae4f06a0fe
'http://archive.ubuntu.com/ubuntu/pool/main/a/apr-util/apr-util_1.6.3.orig.tar.bz2.asc' apr-util_1.6.3.orig.tar.bz2.asc 833 SHA512:6c483e823fb032b161b6bcf77f9a43945aee9afbe40050ebf042865434bc533d21168af20d4cdff597b60b782d8ac9322409a5c2a64bf921b22f5add2451d79d
'http://archive.ubuntu.com/ubuntu/pool/main/a/apr-util/apr-util_1.6.3-1ubuntu1.debian.tar.xz' apr-util_1.6.3-1ubuntu1.debian.tar.xz 341848 SHA512:624f0a037dbb045574f357573ac314c214225157b94cad1c72b71a0bc687e166a1ecf2077ec15af6ada6f4a8eebfb2632a47ad24314522e57f3ddcec1618c032
```

### `dpkg` source package: `apr=1.7.2-3`

Binary Packages:

- `libapr1:amd64=1.7.2-3`

Licenses: (parsed from: `/usr/share/doc/libapr1/copyright`)

- `Apache-2.0`

Source:

```console
$ apt-get source -qq --print-uris apr=1.7.2-3
'http://archive.ubuntu.com/ubuntu/pool/main/a/apr/apr_1.7.2-3.dsc' apr_1.7.2-3.dsc 2262 SHA512:011ea43f83fb42bb4a45e2b93b7c4bc7caf4db68c0b7760a50d731bc432646650316f6fc689dc221c818e70bd87a1e75e92e31bbc79b9b8f050b73ee1fa47f77
'http://archive.ubuntu.com/ubuntu/pool/main/a/apr/apr_1.7.2.orig.tar.bz2' apr_1.7.2.orig.tar.bz2 890218 SHA512:0a3a27ccc97bbe4865c1bc0b803012e3da6d5b1f17d4fb0da6f5f58eec01f6d2ae1f25e52896ea5f9c5ac04c5fddcfd1ac606b301c322cf40d5c4d4ce0a1b76e
'http://archive.ubuntu.com/ubuntu/pool/main/a/apr/apr_1.7.2.orig.tar.bz2.asc' apr_1.7.2.orig.tar.bz2.asc 833 SHA512:77da1e516b30032419b36da8453f56c6149ad18631772613adb095b6eccb7606dc51589d33d422572d3fcefe8f6129bfbb06d0ab7fde5848d873856f4ed93940
'http://archive.ubuntu.com/ubuntu/pool/main/a/apr/apr_1.7.2-3.debian.tar.xz' apr_1.7.2-3.debian.tar.xz 54404 SHA512:b3e02e907a52e96723381bc5b68ba1d7c3762d60cb58c25252c1ec0bc1678c26bb48c753554f39ac47ff8a768ef47182a190da561d46cabe3feb40a9fff011a5
```

### `dpkg` source package: `apt=2.7.6`

Binary Packages:

- `apt=2.7.6`
- `libapt-pkg6.0:amd64=2.7.6`

Licenses: (parsed from: `/usr/share/doc/apt/copyright`, `/usr/share/doc/libapt-pkg6.0/copyright`)

- `BSD-3-clause`
- `Expat`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris apt=2.7.6
'http://archive.ubuntu.com/ubuntu/pool/main/a/apt/apt_2.7.6.dsc' apt_2.7.6.dsc 2945 SHA512:00fe033fbeaa2f7e7133da0f92ea90c0a32ceb44c1c2a2d8d4dc18b4bf51081084c938525c83b00a1ae2c7dd110e271185ce6c0e52f0a0dfa05c828a7e55737d
'http://archive.ubuntu.com/ubuntu/pool/main/a/apt/apt_2.7.6.tar.xz' apt_2.7.6.tar.xz 2345736 SHA512:6d3efd270a6f7d5b2f020f7b5d68a6ecdd2e048c0c0545ab954651f89938ca74bf2f5488a6d769fb8268a5381368f384a28ffaaff235a15a9a4d289124e8a772
```

### `dpkg` source package: `attr=1:2.5.1-4`

Binary Packages:

- `libattr1:amd64=1:2.5.1-4`

Licenses: (parsed from: `/usr/share/doc/libattr1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2+`
- `LGPL-2.1`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/attr/1:2.5.1-4/


### `dpkg` source package: `audit=1:3.1.2-1`

Binary Packages:

- `libaudit-common=1:3.1.2-1`
- `libaudit1:amd64=1:3.1.2-1`

Licenses: (parsed from: `/usr/share/doc/libaudit-common/copyright`, `/usr/share/doc/libaudit1/copyright`)

- `GPL-1`
- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris audit=1:3.1.2-1
'http://archive.ubuntu.com/ubuntu/pool/main/a/audit/audit_3.1.2-1.dsc' audit_3.1.2-1.dsc 2403 SHA512:debc4623777d664ce4dfdb027eea41e5292036001fa4a19594c023ad01be028c8dfcb02bda6a9c217726a38a655f7ce9e159029a745e7bb9c24bbaf8955b10b4
'http://archive.ubuntu.com/ubuntu/pool/main/a/audit/audit_3.1.2.orig.tar.gz' audit_3.1.2.orig.tar.gz 1219860 SHA512:a97003a294ed3671df01e2952688e7d5eef59a35f6891feb53e67c4c7eab9ae8c2d18de41a5b5b20e0ad7156fac93aec05f32f6bc5eea706b42b6f27f676446a
'http://archive.ubuntu.com/ubuntu/pool/main/a/audit/audit_3.1.2-1.debian.tar.xz' audit_3.1.2-1.debian.tar.xz 18396 SHA512:9de616764f954e4f46adf0c793bb29ee060e47696bfe3e0f7c2fe59af816fc1111d6accccb20094a1424c8ee9c6099fb0e97aa28e04775559e225204502a3965
```

### `dpkg` source package: `autoconf=2.71-3`

Binary Packages:

- `autoconf=2.71-3`

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
$ apt-get source -qq --print-uris autoconf=2.71-3
'http://archive.ubuntu.com/ubuntu/pool/main/a/autoconf/autoconf_2.71-3.dsc' autoconf_2.71-3.dsc 1988 SHA512:77b5211bc883080da398a9b16ea5455b6e1562c4be7459844b58a61bcf57183bf6440547ef3bcc55b4ece3213347aaaa12dbf1603d5528d037cfb956413e29f6
'http://archive.ubuntu.com/ubuntu/pool/main/a/autoconf/autoconf_2.71.orig.tar.gz' autoconf_2.71.orig.tar.gz 2003781 SHA512:2bc5331f9807da8754b2ee623a30299cc0d103d6f98068a4c22263aab67ff148b7ad3a1646bd274e604bc08a8ef0ac2601e6422e641ad0cfab2222d60a58c5a8
'http://archive.ubuntu.com/ubuntu/pool/main/a/autoconf/autoconf_2.71-3.debian.tar.xz' autoconf_2.71-3.debian.tar.xz 23896 SHA512:12debf9cd25329130b7d9b00b77bbbfb7f3f26cdf6dbe60188203e3a66ed933f693de02c3816856e4157d5843647d7c834c3bd924345a7ac41ad35aac3689f63
```

### `dpkg` source package: `automake-1.16=1:1.16.5-1.3`

Binary Packages:

- `automake=1:1.16.5-1.3`

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
$ apt-get source -qq --print-uris automake-1.16=1:1.16.5-1.3
'http://archive.ubuntu.com/ubuntu/pool/main/a/automake-1.16/automake-1.16_1.16.5-1.3.dsc' automake-1.16_1.16.5-1.3.dsc 1973 SHA512:911924e07fb9951025d95d0827f431a63e78d55c95eafa8c61c2248bff6880a5902ac1be2ff4f104308bfe853b7cf4c4cdb860faa1fd7feb0f1a0912f0e4f330
'http://archive.ubuntu.com/ubuntu/pool/main/a/automake-1.16/automake-1.16_1.16.5.orig.tar.xz' automake-1.16_1.16.5.orig.tar.xz 1601740 SHA512:3084ae543aa3fb5a05104ffb2e66cfa9a53080f2343c44809707fd648516869511500dba50dae67ff10f92a1bf3b5a92b2a0fa01cda30adb69b9da03994d9d88
'http://archive.ubuntu.com/ubuntu/pool/main/a/automake-1.16/automake-1.16_1.16.5.orig.tar.xz.asc' automake-1.16_1.16.5.orig.tar.xz.asc 833 SHA512:032a7c39abb4cabbefa4eb9c15263baec0902e48c0c81364307361a41fd55be282b9640707c789f5ae572e8e60240e34d1b575a671b5710f5d2a5716fafc2d51
'http://archive.ubuntu.com/ubuntu/pool/main/a/automake-1.16/automake-1.16_1.16.5-1.3.debian.tar.xz' automake-1.16_1.16.5-1.3.debian.tar.xz 14164 SHA512:ca023f45d90ec57db7819688ae457c162ca4429b360bae8dacd6b8b5087a0da51956fd931f23573d7dd47f26422f702a70b219caa55bf76d395417b97af7d5de
```

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

### `dpkg` source package: `base-files=13ubuntu5`

Binary Packages:

- `base-files=13ubuntu5`

Licenses: (parsed from: `/usr/share/doc/base-files/copyright`)

- `GPL`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `base-passwd=3.6.3`

Binary Packages:

- `base-passwd=3.6.3`

Licenses: (parsed from: `/usr/share/doc/base-passwd/copyright`)

- `GPL-2`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris base-passwd=3.6.3
'http://archive.ubuntu.com/ubuntu/pool/main/b/base-passwd/base-passwd_3.6.3.dsc' base-passwd_3.6.3.dsc 1762 SHA512:1d39c7538096a9546d540c1d2d693527167b66258839493b5737e6532ade24096ab2f4b096c0de4276d55080081a52ca69dd4f3422a3fb35ee840c860fd95ac8
'http://archive.ubuntu.com/ubuntu/pool/main/b/base-passwd/base-passwd_3.6.3.tar.xz' base-passwd_3.6.3.tar.xz 58284 SHA512:fca97559c8fb205c590befad5a522f40fd07e7bbc99aec5c632064b428b4b7034e3186e4c258b9151c3bbca330cefade4a7345ac9bf6d439b80408cb5874662d
```

### `dpkg` source package: `bash=5.2.21-2ubuntu1`

Binary Packages:

- `bash=5.2.21-2ubuntu1`

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
$ apt-get source -qq --print-uris bash=5.2.21-2ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/b/bash/bash_5.2.21-2ubuntu1.dsc' bash_5.2.21-2ubuntu1.dsc 2321 SHA512:6da2aa60c4e3090d90b869ad5ee0eba13f29750470fcc5eb86fbbc4239fd9b496142b0b3ec62b8290f49e552debee50688762ffe2bff028492dcc3680d5c5013
'http://archive.ubuntu.com/ubuntu/pool/main/b/bash/bash_5.2.21.orig.tar.xz' bash_5.2.21.orig.tar.xz 5598816 SHA512:ccfd5201ebc32feb302db324868bec42a525a6b08176c77e16feb191fcd6ee4240182dcad783e6e3f010c6d33f356b2c628758f0387ef488ab8b3f932e54babb
'http://archive.ubuntu.com/ubuntu/pool/main/b/bash/bash_5.2.21-2ubuntu1.debian.tar.xz' bash_5.2.21-2ubuntu1.debian.tar.xz 94132 SHA512:f584f012395a09b82b798a62a6249de8a6fec8689d3c92d68c28bcd8c8f78dc5033945e75b7f83d2a78ea9d3e8885fca8d139d8713a2f85bc52fd9f11ccf673a
```

### `dpkg` source package: `binutils=2.41.50.20231214-1ubuntu1`

Binary Packages:

- `binutils=2.41.50.20231214-1ubuntu1`
- `binutils-common:amd64=2.41.50.20231214-1ubuntu1`
- `binutils-x86-64-linux-gnu=2.41.50.20231214-1ubuntu1`
- `libbinutils:amd64=2.41.50.20231214-1ubuntu1`
- `libctf-nobfd0:amd64=2.41.50.20231214-1ubuntu1`
- `libctf0:amd64=2.41.50.20231214-1ubuntu1`
- `libgprofng0:amd64=2.41.50.20231214-1ubuntu1`
- `libsframe1:amd64=2.41.50.20231214-1ubuntu1`

Licenses: (parsed from: `/usr/share/doc/binutils/copyright`, `/usr/share/doc/binutils-common/copyright`, `/usr/share/doc/binutils-x86-64-linux-gnu/copyright`, `/usr/share/doc/libbinutils/copyright`, `/usr/share/doc/libctf-nobfd0/copyright`, `/usr/share/doc/libctf0/copyright`, `/usr/share/doc/libgprofng0/copyright`, `/usr/share/doc/libsframe1/copyright`)

- `GFDL`
- `GPL`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris binutils=2.41.50.20231214-1ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/b/binutils/binutils_2.41.50.20231214-1ubuntu1.dsc' binutils_2.41.50.20231214-1ubuntu1.dsc 10145 SHA512:4183923a5063f2d3e02d1ef1689d179d95113ba7c7edd1dd597346a64c12793393b1f083119283bf043d66f77b36c3e5d81ab5dbfdb1e8e03ae76eccd54a9385
'http://archive.ubuntu.com/ubuntu/pool/main/b/binutils/binutils_2.41.50.20231214.orig.tar.xz' binutils_2.41.50.20231214.orig.tar.xz 23775244 SHA512:5fa03bf232f9714b2c72b5bf47e846c0a7f2e83657bf18fc0e653b96b8c3c7606a3f8b9e951e3dbe3056cd0f433142991765a12a4dcaf25caaa1cd9a8cdec510
'http://archive.ubuntu.com/ubuntu/pool/main/b/binutils/binutils_2.41.50.20231214-1ubuntu1.debian.tar.xz' binutils_2.41.50.20231214-1ubuntu1.debian.tar.xz 130312 SHA512:bde93bbc2b1cd03a6b132a232eb1516cb680ee7f468f27f372b45edabdea131e5f36e57bc7db12fd2971f3299370a65bf9c031dcd135d7de41456ec8e6e23a70
```

### `dpkg` source package: `boost1.83=1.83.0-2ubuntu1`

Binary Packages:

- `libboost-python1.83.0=1.83.0-2ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libboost-python1.83.0/copyright`)

- `Apache-2.0`
- `BSD2`
- `BSD3_DEShaw`
- `BSD3_Google`
- `BSL-1.0`
- `Caramel`
- `CrystalClear`
- `HP`
- `Jam`
- `Kempf`
- `MIT`
- `NIST`
- `OldBoost1`
- `OldBoost2`
- `OldBoost3`
- `Python`
- `SGI`
- `Spencer`
- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris boost1.83=1.83.0-2ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/b/boost1.83/boost1.83_1.83.0-2ubuntu1.dsc' boost1.83_1.83.0-2ubuntu1.dsc 10361 SHA512:2282c0e24c1bf8d2c8d760f1afc417c79a41f844f87e5bb3a85895850cbf981ed580cf06aefff0ac9ba9916190ee0e173efd0ed6842ac05e795dfa74f00f73a2
'http://archive.ubuntu.com/ubuntu/pool/main/b/boost1.83/boost1.83_1.83.0.orig.tar.xz' boost1.83_1.83.0.orig.tar.xz 77376520 SHA512:de285fe516794a888196c0b1fafd5b62dbd3acf7c2214287c3a51a02d127981fa56f09c436e8d5868ceb1f5e9e9490c96fe635ed9aa84fd96c21b557a23558c8
'http://archive.ubuntu.com/ubuntu/pool/main/b/boost1.83/boost1.83_1.83.0-2ubuntu1.debian.tar.xz' boost1.83_1.83.0-2ubuntu1.debian.tar.xz 378928 SHA512:62f50c7e664100a481a3e62585cda5489ec620ef3f06018d8b5eec3758cbc778431f850008e55837542b11038ce7495992adbaae5851928fe6fed2ec336a4255
```

### `dpkg` source package: `brotli=1.1.0-2`

Binary Packages:

- `libbrotli-dev:amd64=1.1.0-2`
- `libbrotli1:amd64=1.1.0-2`

Licenses: (parsed from: `/usr/share/doc/libbrotli-dev/copyright`, `/usr/share/doc/libbrotli1/copyright`)

- `MIT`

Source:

```console
$ apt-get source -qq --print-uris brotli=1.1.0-2
'http://archive.ubuntu.com/ubuntu/pool/main/b/brotli/brotli_1.1.0-2.dsc' brotli_1.1.0-2.dsc 2261 SHA512:ec6a97f2a23b7a6e9dc7f4f3675a9962d136f0c1a2cec470775087781e88020aee6fa83b8b2d1d82a2cf3a04181001362d9920147536209c7190a847c0c36a6d
'http://archive.ubuntu.com/ubuntu/pool/main/b/brotli/brotli_1.1.0.orig.tar.gz' brotli_1.1.0.orig.tar.gz 512036 SHA512:7a94f8b1ca1d3a411c6b5681bd2ed66183468f7b37a24741601d77ed4353577805de84c810dd26086d4afe6b11bfc4791db3ba7f6f9986bc7acbb8e9b43f488b
'http://archive.ubuntu.com/ubuntu/pool/main/b/brotli/brotli_1.1.0-2.debian.tar.xz' brotli_1.1.0-2.debian.tar.xz 5480 SHA512:640924469528a7d955bafa2662f411aefa265013d663aadcc4ab760d1519f7fbd8a03ef457f94250f2ad9ad96bc9b2f174be4be1367d06eff4cbe23a433d2676
```

### `dpkg` source package: `bzip2=1.0.8-5build1`

Binary Packages:

- `bzip2=1.0.8-5build1`
- `libbz2-1.0:amd64=1.0.8-5build1`
- `libbz2-dev:amd64=1.0.8-5build1`

Licenses: (parsed from: `/usr/share/doc/bzip2/copyright`, `/usr/share/doc/libbz2-1.0/copyright`, `/usr/share/doc/libbz2-dev/copyright`)

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

### `dpkg` source package: `cairo=1.18.0-1`

Binary Packages:

- `libcairo-gobject2:amd64=1.18.0-1`
- `libcairo-script-interpreter2:amd64=1.18.0-1`
- `libcairo2:amd64=1.18.0-1`
- `libcairo2-dev:amd64=1.18.0-1`

Licenses: (parsed from: `/usr/share/doc/libcairo-gobject2/copyright`, `/usr/share/doc/libcairo-script-interpreter2/copyright`, `/usr/share/doc/libcairo2/copyright`, `/usr/share/doc/libcairo2-dev/copyright`)

- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris cairo=1.18.0-1
'http://archive.ubuntu.com/ubuntu/pool/main/c/cairo/cairo_1.18.0-1.dsc' cairo_1.18.0-1.dsc 2772 SHA512:93d53a43e9fc5979ebfac817aa5cf36b884f65b04d666cfc39a5514095de677d98292f594e3cc5d46df074a9bf2c36f61bed391b807f02d126c1bbc7608037a0
'http://archive.ubuntu.com/ubuntu/pool/main/c/cairo/cairo_1.18.0.orig.tar.xz' cairo_1.18.0.orig.tar.xz 33761148 SHA512:6366c7d5e3fd3e12df2edc43aa4ed4c3a517de2ef0b1b3b30dfa8b69a7cae1dd55765801228cec308d2e9792037d0704ae49d95b7b12c06f20df092fa0534e1c
'http://archive.ubuntu.com/ubuntu/pool/main/c/cairo/cairo_1.18.0-1.debian.tar.xz' cairo_1.18.0-1.debian.tar.xz 29720 SHA512:da10f9f9282d9467bf6097f9102265c0d219ee51912ed4d8f788b76b4f0d96c987ac735253d54df913f79ee1ab184805fc59783a5966bdc6f024d5ac8b360a11
```

### `dpkg` source package: `cdebconf=0.271ubuntu1`

Binary Packages:

- `libdebconfclient0:amd64=0.271ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libdebconfclient0/copyright`)

- `BSD-2-Clause`
- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris cdebconf=0.271ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/c/cdebconf/cdebconf_0.271ubuntu1.dsc' cdebconf_0.271ubuntu1.dsc 2873 SHA512:063863ee7a8655838309f9fe2c13663ad9724a62896d841ee1edb1b00a1ab300a44acf9653d980b5f6ee1528b19229311615202125308bb1c264bb220cd6b186
'http://archive.ubuntu.com/ubuntu/pool/main/c/cdebconf/cdebconf_0.271ubuntu1.tar.xz' cdebconf_0.271ubuntu1.tar.xz 285500 SHA512:5dbd790591ce95012531c7177a2af3797d1216f1619e8df008d2a7276dde67c7e7bf884a2a11f40fd563e19c51cca355ac4d201a0c7069386b469aec0c2aa45f
```

### `dpkg` source package: `coreutils=9.4-2ubuntu1`

Binary Packages:

- `coreutils=9.4-2ubuntu1`

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


### `dpkg` source package: `curl=8.4.0-2ubuntu1`

Binary Packages:

- `curl=8.4.0-2ubuntu1`
- `libcurl3-gnutls:amd64=8.4.0-2ubuntu1`
- `libcurl4:amd64=8.4.0-2ubuntu1`
- `libcurl4-openssl-dev:amd64=8.4.0-2ubuntu1`

Licenses: (parsed from: `/usr/share/doc/curl/copyright`, `/usr/share/doc/libcurl3-gnutls/copyright`, `/usr/share/doc/libcurl4/copyright`, `/usr/share/doc/libcurl4-openssl-dev/copyright`)

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
$ apt-get source -qq --print-uris curl=8.4.0-2ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/c/curl/curl_8.4.0-2ubuntu1.dsc' curl_8.4.0-2ubuntu1.dsc 3159 SHA512:5693a8d8705dd9668e19b2bf9ddbb67230dbb6cb4332a12b19d404735f8d1623acd39abfdb95aac01e289021477de038f9d1fb8f75a5f1125eceb0fd8e82443e
'http://archive.ubuntu.com/ubuntu/pool/main/c/curl/curl_8.4.0.orig.tar.gz' curl_8.4.0.orig.tar.gz 4424232 SHA512:375d241effccde852cfba32aa61be406f6c6e8ef2773b48d57bfa1ff99fdf414dc08bdb6b3a65930e53b28e31246a4bc396c81054ae9c560a3bf58cca0ae78b0
'http://archive.ubuntu.com/ubuntu/pool/main/c/curl/curl_8.4.0.orig.tar.gz.asc' curl_8.4.0.orig.tar.gz.asc 488 SHA512:8341c5a8e5e0d0acc965cf80c226ca445fc69b823c4c5ac93a5aca00be44ac586f7a4e1399b707829b8469a2bd0e1a86a79489d28e842355bad6b7ba67f8d4ab
'http://archive.ubuntu.com/ubuntu/pool/main/c/curl/curl_8.4.0-2ubuntu1.debian.tar.xz' curl_8.4.0-2ubuntu1.debian.tar.xz 46484 SHA512:8d107b507a1123c5520ba90a9f582f822be200d04bb9caab1b806cd89d9c812619fb3b47e24ab4da6c1097e51f109e2ff18029af370baf7db970e07abc46173c
```

### `dpkg` source package: `cyrus-sasl2=2.1.28+dfsg1-4`

Binary Packages:

- `libsasl2-2:amd64=2.1.28+dfsg1-4`
- `libsasl2-modules-db:amd64=2.1.28+dfsg1-4`

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
$ apt-get source -qq --print-uris cyrus-sasl2=2.1.28+dfsg1-4
'http://archive.ubuntu.com/ubuntu/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.28%2bdfsg1-4.dsc' cyrus-sasl2_2.1.28+dfsg1-4.dsc 3224 SHA512:5c75d3bc7407255b1883e0ce0451ca480109b47a7ffe8ad5364f7bd8d9c22505ac2eff5fffa6ec7e402e3edfaf18cf3cbdbefc3a36b4a2f4681aef848b3281fa
'http://archive.ubuntu.com/ubuntu/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.28%2bdfsg1.orig.tar.xz' cyrus-sasl2_2.1.28+dfsg1.orig.tar.xz 794540 SHA512:e94075d09b38a50138b782323de286deb7b15008064f07df4fa682e94367e829d9bfafef48d5478f730fef8fde536bcc6d54cab0452b76473a3c620b3dc18fa2
'http://archive.ubuntu.com/ubuntu/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.28%2bdfsg1-4.debian.tar.xz' cyrus-sasl2_2.1.28+dfsg1-4.debian.tar.xz 96688 SHA512:a0e722ae8eab81871a92226791b0df9edaa3b9a4906def729791dc1a75060f5ab1ae83a70eb3ac141e63a05cd0513ad80fb29daa84883711f7c3da19011f9b5f
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

### `dpkg` source package: `dav1d=1.3.0-2`

Binary Packages:

- `libdav1d7:amd64=1.3.0-2`

Licenses: (parsed from: `/usr/share/doc/libdav1d7/copyright`)

- `BSD-2-clause`
- `ISC`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris dav1d=1.3.0-2
'http://archive.ubuntu.com/ubuntu/pool/universe/d/dav1d/dav1d_1.3.0-2.dsc' dav1d_1.3.0-2.dsc 2287 SHA512:5bfa438886bd17f5f100245f137ce41e3bfb4bd4f6a821060ba27c51577529e70cdd0827fce6f67e6e2e6591da3958ebec184fce96b63f75b3c50ecd686670b8
'http://archive.ubuntu.com/ubuntu/pool/universe/d/dav1d/dav1d_1.3.0.orig.tar.xz' dav1d_1.3.0.orig.tar.xz 885220 SHA512:a91d217b8656c452dd80f5597e988f0e7a2ea32b12092c2695e7dc388033db7b193f7a8c98413bec31d1c38af376561d39f7618b935c4feeb6498c5d2b43f6a4
'http://archive.ubuntu.com/ubuntu/pool/universe/d/dav1d/dav1d_1.3.0.orig.tar.xz.asc' dav1d_1.3.0.orig.tar.xz.asc 195 SHA512:11d831685cf8258cb779bbdf93ce95c7799f87b827fcf3e6f0f4b51fba942a6ca3a98b1dbb655ef3094dcd7b9112d56ea405c489656065f20b6e5ef641da625a
'http://archive.ubuntu.com/ubuntu/pool/universe/d/dav1d/dav1d_1.3.0-2.debian.tar.xz' dav1d_1.3.0-2.debian.tar.xz 8204 SHA512:599b7a61112cdbc78a4cf3d9ea4115524a8b8dc101fb0c872f12609266e01c17c60411cd644c714050a9fe77af1c3ce2e33c2b8f516d22af987d84eff76e4f70
```

### `dpkg` source package: `db-defaults=1:5.3.21ubuntu1`

Binary Packages:

- `libdb-dev:amd64=1:5.3.21ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libdb-dev/copyright`)

- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris db-defaults=1:5.3.21ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/d/db-defaults/db-defaults_5.3.21ubuntu1.dsc' db-defaults_5.3.21ubuntu1.dsc 1580 SHA512:df7ecb38474c44f16e41b6bf0fa637268ae6cacb315f6c4cd3d620c7007ff4c178257460b125c4d7360dbfd599d1d6f13d242a80e638f0a72f3df0affcd04738
'http://archive.ubuntu.com/ubuntu/pool/main/d/db-defaults/db-defaults_5.3.21ubuntu1.tar.xz' db-defaults_5.3.21ubuntu1.tar.xz 2528 SHA512:4b7e2ddcdedb904861fe89e27c1acdce70f9a224e0f48ff6a34adeea9d6312b602e7dbf03da56d32d4fc02ac6ec66714988cea27000bc190ee438f76bfbfd8ee
```

### `dpkg` source package: `db5.3=5.3.28+dfsg2-4`

Binary Packages:

- `libdb5.3:amd64=5.3.28+dfsg2-4`
- `libdb5.3-dev=5.3.28+dfsg2-4`

Licenses: (parsed from: `/usr/share/doc/libdb5.3/copyright`, `/usr/share/doc/libdb5.3-dev/copyright`)

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
$ apt-get source -qq --print-uris db5.3=5.3.28+dfsg2-4
'http://archive.ubuntu.com/ubuntu/pool/main/d/db5.3/db5.3_5.3.28%2bdfsg2-4.dsc' db5.3_5.3.28+dfsg2-4.dsc 2190 SHA512:f1055d77f4238356a0124c99d3f91765479ce40b7ebe769fc2f114dcd0e067f27d511e47d2211f01bc21de910eec087fee44ec731e8a317e9579539fb950ae1b
'http://archive.ubuntu.com/ubuntu/pool/main/d/db5.3/db5.3_5.3.28%2bdfsg2.orig.tar.xz' db5.3_5.3.28+dfsg2.orig.tar.xz 21287688 SHA512:f9c9d042702ef3fcfdd4b4859583048f3396b161009dc24b6d3a2c53533d58214239fc80e2c42db17e9f092df44d531502737f3b368b956bff49ef057b6b51ef
'http://archive.ubuntu.com/ubuntu/pool/main/d/db5.3/db5.3_5.3.28%2bdfsg2-4.debian.tar.xz' db5.3_5.3.28+dfsg2-4.debian.tar.xz 33624 SHA512:ba77be9eadb07a8a9e8e5ad3e51540e70e0a9e15bb0376e9c535d2488b091d75f8984b23ff786b43767005652529a7214a5b37de4649bb5e691d8c49be2c4733
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

### `dpkg` source package: `debianutils=5.14`

Binary Packages:

- `debianutils=5.14`

Licenses: (parsed from: `/usr/share/doc/debianutils/copyright`)

- `GPL-2`
- `GPL-2+`
- `SMAIL-GPL`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/debianutils/5.14/


### `dpkg` source package: `diffutils=1:3.10-1`

Binary Packages:

- `diffutils=1:3.10-1`

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
$ apt-get source -qq --print-uris diffutils=1:3.10-1
'http://archive.ubuntu.com/ubuntu/pool/main/d/diffutils/diffutils_3.10-1.dsc' diffutils_3.10-1.dsc 1715 SHA512:754b0ecc805723f61c8fa5dcfa1b667937bfb2b88d4a0385b071fc4b194a83b09f31d358429684908a39b10c0e0edf56743177a3bd5dcdd9b75fe1c368974dab
'http://archive.ubuntu.com/ubuntu/pool/main/d/diffutils/diffutils_3.10.orig.tar.xz' diffutils_3.10.orig.tar.xz 1624240 SHA512:219d2c815a120690c6589846271e43aee5c96c61a7ee4abbef97dfcdb3d6416652ed494b417de0ab6688c4322540d48be63b5e617beb6d20530b5d55d723ccbb
'http://archive.ubuntu.com/ubuntu/pool/main/d/diffutils/diffutils_3.10.orig.tar.xz.asc' diffutils_3.10.orig.tar.xz.asc 833 SHA512:91aa1fcfca224454e292540ea7813f4a0eb348f06a4374017326d524949775359fc833de597cc201c97f357eb6c675800828a6e3332572376f3554f1f2e1aca1
'http://archive.ubuntu.com/ubuntu/pool/main/d/diffutils/diffutils_3.10-1.debian.tar.xz' diffutils_3.10-1.debian.tar.xz 13952 SHA512:7fdb469643b31fc6e0a76a02ae900eef05d18c7895bdc2ff2db261500e4dca6cc3a08ef892e5126cc61e53124baaf32b88486f35424c17c86dd2ab3596255cb4
```

### `dpkg` source package: `djvulibre=3.5.28-2build3`

Binary Packages:

- `libdjvulibre-dev:amd64=3.5.28-2build3`
- `libdjvulibre-text=3.5.28-2build3`
- `libdjvulibre21:amd64=3.5.28-2build3`

Licenses: (parsed from: `/usr/share/doc/libdjvulibre-dev/copyright`, `/usr/share/doc/libdjvulibre-text/copyright`, `/usr/share/doc/libdjvulibre21/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris djvulibre=3.5.28-2build3
'http://archive.ubuntu.com/ubuntu/pool/main/d/djvulibre/djvulibre_3.5.28-2build3.dsc' djvulibre_3.5.28-2build3.dsc 2391 SHA512:b62ce50336f8330e03494bc9fad891e0edf05131ec37c30d9a90676f30efa419289f91cf8addd487219abe350abf3fd470dfb80906ebad3e445db756e2d34752
'http://archive.ubuntu.com/ubuntu/pool/main/d/djvulibre/djvulibre_3.5.28.orig.tar.xz' djvulibre_3.5.28.orig.tar.xz 2959024 SHA512:4fdbecd2b7b583ee4211c9cda6638a3a831c883e2552b3c8ad09f69e8734831addc14f590faab8c58d7f9f017b527abccc384f6066e674e341cf43c96db49cb7
'http://archive.ubuntu.com/ubuntu/pool/main/d/djvulibre/djvulibre_3.5.28-2build3.debian.tar.xz' djvulibre_3.5.28-2build3.debian.tar.xz 17612 SHA512:66b190da517dd0d7992a879b821082ee6dd20bd49467d11fe15aee41c5c5d58955f6ded1ca55db3016bfc43a7f4b7fe5370ee773058a8a5c8feba2aa463a7fc0
```

### `dpkg` source package: `dpkg=1.22.1ubuntu5`

Binary Packages:

- `dpkg=1.22.1ubuntu5`
- `dpkg-dev=1.22.1ubuntu5`
- `libdpkg-perl=1.22.1ubuntu5`

Licenses: (parsed from: `/usr/share/doc/dpkg/copyright`, `/usr/share/doc/dpkg-dev/copyright`, `/usr/share/doc/libdpkg-perl/copyright`)

- `GPL-2`
- `GPL-2+`
- `public-domain-s-s-d`

Source:

```console
$ apt-get source -qq --print-uris dpkg=1.22.1ubuntu5
'http://archive.ubuntu.com/ubuntu/pool/main/d/dpkg/dpkg_1.22.1ubuntu5.dsc' dpkg_1.22.1ubuntu5.dsc 3148 SHA512:a146e7e35075050c59e291bd8d4cc54196cd215d03c815b43054c32c6127ee7c50005914023be99e8a269a909002a54b4dcd669520fb198872f622645a87f358
'http://archive.ubuntu.com/ubuntu/pool/main/d/dpkg/dpkg_1.22.1ubuntu5.tar.xz' dpkg_1.22.1ubuntu5.tar.xz 5610676 SHA512:88c770a69c7087beae8abfe8f928178055edb855cbe72b870eb6a84fd8e88d9944d0e4688d8987d0c9b8f0bd7631332286a337fd98ff2ffecfc20e371486bcdf
```

### `dpkg` source package: `e2fsprogs=1.47.0-2ubuntu1`

Binary Packages:

- `comerr-dev:amd64=2.1-1.47.0-2ubuntu1`
- `e2fsprogs=1.47.0-2ubuntu1`
- `libcom-err2:amd64=1.47.0-2ubuntu1`
- `libext2fs2:amd64=1.47.0-2ubuntu1`
- `libss2:amd64=1.47.0-2ubuntu1`
- `logsave=1.47.0-2ubuntu1`

Licenses: (parsed from: `/usr/share/doc/comerr-dev/copyright`, `/usr/share/doc/e2fsprogs/copyright`, `/usr/share/doc/libcom-err2/copyright`, `/usr/share/doc/libext2fs2/copyright`, `/usr/share/doc/libss2/copyright`, `/usr/share/doc/logsave/copyright`)

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

### `dpkg` source package: `elfutils=0.190-1`

Binary Packages:

- `libelf1:amd64=0.190-1`

Licenses: (parsed from: `/usr/share/doc/libelf1/copyright`)

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
$ apt-get source -qq --print-uris elfutils=0.190-1
'http://archive.ubuntu.com/ubuntu/pool/main/e/elfutils/elfutils_0.190-1.dsc' elfutils_0.190-1.dsc 3248 SHA512:aa6fed189e51fd42d9de23de61d42915df8785df2033dbe3eaf838f9a1faf7f5009eb90521862e125e044d51b6633c022a0ad3164c0ec7eed75439bcc97fe5c4
'http://archive.ubuntu.com/ubuntu/pool/main/e/elfutils/elfutils_0.190.orig.tar.bz2' elfutils_0.190.orig.tar.bz2 9162766 SHA512:9c4f5328097e028286c42f29e39dc3d80914b656cdfbbe05b639e91bc787ae8ae64dd4d69a6e317ce30c01648ded10281b86a51e718295f4c589df1225a48102
'http://archive.ubuntu.com/ubuntu/pool/main/e/elfutils/elfutils_0.190-1.debian.tar.xz' elfutils_0.190-1.debian.tar.xz 43220 SHA512:9941b7ac4538cf41e2b09da99f017e75c552c7dc45c65e8cbbee13d2846c60621676d571af6e3a628dc119a355359d9ae589d459be262f8878d09e6ddc8ce91d
```

### `dpkg` source package: `expat=2.5.0-2`

Binary Packages:

- `libexpat1:amd64=2.5.0-2`
- `libexpat1-dev:amd64=2.5.0-2`

Licenses: (parsed from: `/usr/share/doc/libexpat1/copyright`, `/usr/share/doc/libexpat1-dev/copyright`)

- `MIT`

Source:

```console
$ apt-get source -qq --print-uris expat=2.5.0-2
'http://archive.ubuntu.com/ubuntu/pool/main/e/expat/expat_2.5.0-2.dsc' expat_2.5.0-2.dsc 1964 SHA512:a71f12ab67b948e890dd1d7e00339acb22cef4f834bc2cd26cbfc04eb5e0d65d56a22e41d384394862104e2e8da0309f4029b059a7adcfdc2d0b0d1acc64ca28
'http://archive.ubuntu.com/ubuntu/pool/main/e/expat/expat_2.5.0.orig.tar.gz' expat_2.5.0.orig.tar.gz 8320988 SHA512:779f0d0f3f2d8b33db0fd044864ab5ab1a40f20501f792fe90ad0d18de536c4765c3749f120e21fec11a0e6c89af1dc576d1fe261c871ca44a594f7b61fd1d9e
'http://archive.ubuntu.com/ubuntu/pool/main/e/expat/expat_2.5.0-2.debian.tar.xz' expat_2.5.0-2.debian.tar.xz 12804 SHA512:3603f3f3f3e4f0bc2c7a29a25aa7c9681ff4a93d48b7e5fabb0d58f8e048c3d7eb0487140f813bd925c4cb2b956a3bd2f68d8c3d75f79066624d83445739cb57
```

### `dpkg` source package: `fftw3=3.3.10-1ubuntu1`

Binary Packages:

- `libfftw3-double3:amd64=3.3.10-1ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libfftw3-double3/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris fftw3=3.3.10-1ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/f/fftw3/fftw3_3.3.10-1ubuntu1.dsc' fftw3_3.3.10-1ubuntu1.dsc 2853 SHA512:9b6e9b0e6f9777bcc80d92d42eff0482c62ff117e26512eff0cc26e42325f775489dd7d572da0bc73d6bc0af33a23aa5d120f56eba5247f4ef255f5a138d7d40
'http://archive.ubuntu.com/ubuntu/pool/main/f/fftw3/fftw3_3.3.10.orig.tar.gz' fftw3_3.3.10.orig.tar.gz 4262403 SHA512:fa2ea740449fd06c833a82e1fff82bacd554188d500cbedff5a0bc185551799ef9ef9b8b1c227283abdbbdd185424d19df9c0f06ed88d5fe3d9c001d6fab6109
'http://archive.ubuntu.com/ubuntu/pool/main/f/fftw3/fftw3_3.3.10-1ubuntu1.debian.tar.xz' fftw3_3.3.10-1ubuntu1.debian.tar.xz 14776 SHA512:0c1b49c0624bfb0e74af21a60b192d939edf7da3c49f1669a801a8884b77c07f380c2b83ab7ad56a4f6c2e6344bc8e1ab67c867d94cd528dde3404374b363a6e
```

### `dpkg` source package: `file=1:5.45-2`

Binary Packages:

- `file=1:5.45-2`
- `libmagic-mgc=1:5.45-2`
- `libmagic1:amd64=1:5.45-2`

Licenses: (parsed from: `/usr/share/doc/file/copyright`, `/usr/share/doc/libmagic-mgc/copyright`, `/usr/share/doc/libmagic1/copyright`)

- `BSD-2-Clause-alike`
- `BSD-2-Clause-netbsd`
- `BSD-2-Clause-regents`
- `MIT-Old-Style-with-legal-disclaimer-2`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris file=1:5.45-2
'http://archive.ubuntu.com/ubuntu/pool/main/f/file/file_5.45-2.dsc' file_5.45-2.dsc 2240 SHA512:6e766bc653ee7c422d7bfd92ca11daa16c267fc9008ff8f38c26c14d51b8786e134fb2c7af243ba9b8e4b4495251f697180e7f658a56b782128f5a2b6bbd8342
'http://archive.ubuntu.com/ubuntu/pool/main/f/file/file_5.45.orig.tar.gz' file_5.45.orig.tar.gz 1246503 SHA512:12611a59ff766c22a55db4b4a9f80f95a0a2e916a1d8593612c6ead32c247102a8fdc23693c6bf81bda9b604d951a62c0051e91580b1b79e190a3504c0efc20a
'http://archive.ubuntu.com/ubuntu/pool/main/f/file/file_5.45.orig.tar.gz.asc' file_5.45.orig.tar.gz.asc 169 SHA512:4bda3c9b23e534e31d8726eae110e108c538c88ca4884666989da9bedc5dcfd9cfcb3754e68885ca5310db67bff151f9bf4f21913f7b5046f158a9ca38bc00a4
'http://archive.ubuntu.com/ubuntu/pool/main/f/file/file_5.45-2.debian.tar.xz' file_5.45-2.debian.tar.xz 34452 SHA512:52f4e529af4017355a7b0e4c63a5005815ae1b1e83b5eb5aef03684e4a553fed3c1e5f37650424b932012f814bb4492607083ef09965a7ebad77fd62ccdef017
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

### `dpkg` source package: `fontconfig=2.14.2-6ubuntu1`

Binary Packages:

- `fontconfig=2.14.2-6ubuntu1`
- `fontconfig-config=2.14.2-6ubuntu1`
- `libfontconfig-dev:amd64=2.14.2-6ubuntu1`
- `libfontconfig1:amd64=2.14.2-6ubuntu1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris fontconfig=2.14.2-6ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/f/fontconfig/fontconfig_2.14.2-6ubuntu1.dsc' fontconfig_2.14.2-6ubuntu1.dsc 2775 SHA512:97e4df7f2984d7c0accc72424ffcbb64c72bc1450bfb23a0dea284690d875a12e5f2134b3bee5633a3d03af3517ea3c501909dc44d9bd1504d6e476fb84fbc82
'http://archive.ubuntu.com/ubuntu/pool/main/f/fontconfig/fontconfig_2.14.2.orig.tar.xz' fontconfig_2.14.2.orig.tar.xz 1440844 SHA512:23483e0ae6aa7589fd37f9949a4cf951c5bff981739dbb446881e4cea86a208c0ab31e2358666eac724af1dc6a689a42733a7ce91cd3e76d8d91eacedb318085
'http://archive.ubuntu.com/ubuntu/pool/main/f/fontconfig/fontconfig_2.14.2-6ubuntu1.debian.tar.xz' fontconfig_2.14.2-6ubuntu1.debian.tar.xz 29316 SHA512:8636664d8f9fec0ef6ac5da60a4d8fa2984ac4bd6aba9e8d23133e7ef0bc9f82f01ea0076cea5b163b725f4ecb24d994854aaf0682c63cf7f668df9f8e99564c
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

### `dpkg` source package: `freetype=2.13.2+dfsg-1`

Binary Packages:

- `libfreetype-dev:amd64=2.13.2+dfsg-1`
- `libfreetype6:amd64=2.13.2+dfsg-1`

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
$ apt-get source -qq --print-uris freetype=2.13.2+dfsg-1
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.13.2%2bdfsg-1.dsc' freetype_2.13.2+dfsg-1.dsc 3686 SHA512:0dd90c1910192646348782a84e1fafb2114fe7984a75f009c6cd4184b8b1664f8e7187c44ee7a6c8dea0d82b5752b6b51a817ac0e51625cbd90cd8d42be10c09
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.13.2%2bdfsg.orig-ft2demos.tar.xz' freetype_2.13.2+dfsg.orig-ft2demos.tar.xz 341140 SHA512:aa83ba4212ff7c4453b72f036136cb9b04cacf7d196388a3e4752613e000b3bb45a4dcf63d3d1d5b3d6ada10720304b532fb6e33ed6a5b399dcce45c27af9ade
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.13.2%2bdfsg.orig-ft2demos.tar.xz.asc' freetype_2.13.2+dfsg.orig-ft2demos.tar.xz.asc 833 SHA512:07680e2919643cb1b964c311f1590fddd38f42189944b3e5e46a9c6a84688255749506f8a745d52255e3599e5136f3e8761d746a67cdcd6e565b8eaecb9fd792
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.13.2%2bdfsg.orig-ft2docs.tar.xz' freetype_2.13.2+dfsg.orig-ft2docs.tar.xz 2173920 SHA512:ca3438dcf6f995af556d8db3cb3cfdcabb81ab5a7dd88464ff757e3e418b3219b0011857cde8a338372e30d8375486ac8e50914da2ea948dc874f70010bce60c
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.13.2%2bdfsg.orig-ft2docs.tar.xz.asc' freetype_2.13.2+dfsg.orig-ft2docs.tar.xz.asc 833 SHA512:b346579fcc8f073e586135c72140c64bb3d5ca46201b879e3976b39a62a14f6668a5009d39b078e51d51a7301e346b4de6f7e9ee365f9b44146e67579aaf6500
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.13.2%2bdfsg.orig.tar.xz' freetype_2.13.2+dfsg.orig.tar.xz 2220368 SHA512:8809693981ea7ef274d882245e3257305b65ad73e5ae36bb7e4ffc769a97b726d6bd07f1627dae456519e02e3eaa43269769d7ad363f49b9247d27d2c6f47d6d
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.13.2%2bdfsg-1.debian.tar.xz' freetype_2.13.2+dfsg-1.debian.tar.xz 43824 SHA512:4f33dfbd766e683ab23bb78ae0f217d7df3dd03966da97bb191ef9409ff9ecc59d41676cac1c8e1eebae3fef487401b7a96fd9e27f8dacedb75f03c500ec63b7
```

### `dpkg` source package: `fribidi=1.0.13-3`

Binary Packages:

- `libfribidi0:amd64=1.0.13-3`

Licenses: (parsed from: `/usr/share/doc/libfribidi0/copyright`)

- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris fribidi=1.0.13-3
'http://archive.ubuntu.com/ubuntu/pool/main/f/fribidi/fribidi_1.0.13-3.dsc' fribidi_1.0.13-3.dsc 2007 SHA512:801485436ef071306696f6c3db7dcad61d1e39c1cf4bb213aebe2ca13541dfa03f0751337c5b9ff3ec3719bfd5736e00c53a211f8c619541beb95f2fd2d3e5bc
'http://archive.ubuntu.com/ubuntu/pool/main/f/fribidi/fribidi_1.0.13.orig.tar.xz' fribidi_1.0.13.orig.tar.xz 1170100 SHA512:09357d842ff9e05b918f826e28e4a25ad996e17f73242ee9ce53fae9f37ec6c639f9cae4271577f6e0269f34265afc893858225c4a94610f0a6ee7580fb1fe07
'http://archive.ubuntu.com/ubuntu/pool/main/f/fribidi/fribidi_1.0.13-3.debian.tar.xz' fribidi_1.0.13-3.debian.tar.xz 8848 SHA512:fa9aa25785d36b7a08fe06314ea66b7bd8913df456fbdd2fe4be7e44910be1efe023de413bbe35e56383b2f9b35e71eae6d73b2ff7a168e32ed036e9f3877d8c
```

### `dpkg` source package: `gcc-13=13.2.0-9ubuntu1`

Binary Packages:

- `cpp-13=13.2.0-9ubuntu1`
- `g++-13=13.2.0-9ubuntu1`
- `gcc-13=13.2.0-9ubuntu1`
- `gcc-13-base:amd64=13.2.0-9ubuntu1`
- `libasan8:amd64=13.2.0-9ubuntu1`
- `libatomic1:amd64=13.2.0-9ubuntu1`
- `libcc1-0:amd64=13.2.0-9ubuntu1`
- `libgcc-13-dev:amd64=13.2.0-9ubuntu1`
- `libgcc-s1:amd64=13.2.0-9ubuntu1`
- `libgfortran5:amd64=13.2.0-9ubuntu1`
- `libgomp1:amd64=13.2.0-9ubuntu1`
- `libhwasan0:amd64=13.2.0-9ubuntu1`
- `libitm1:amd64=13.2.0-9ubuntu1`
- `liblsan0:amd64=13.2.0-9ubuntu1`
- `libquadmath0:amd64=13.2.0-9ubuntu1`
- `libstdc++-13-dev:amd64=13.2.0-9ubuntu1`
- `libstdc++6:amd64=13.2.0-9ubuntu1`
- `libtsan2:amd64=13.2.0-9ubuntu1`
- `libubsan1:amd64=13.2.0-9ubuntu1`

Licenses: (parsed from: `/usr/share/doc/cpp-13/copyright`, `/usr/share/doc/g++-13/copyright`, `/usr/share/doc/gcc-13/copyright`, `/usr/share/doc/gcc-13-base/copyright`, `/usr/share/doc/libasan8/copyright`, `/usr/share/doc/libatomic1/copyright`, `/usr/share/doc/libcc1-0/copyright`, `/usr/share/doc/libgcc-13-dev/copyright`, `/usr/share/doc/libgcc-s1/copyright`, `/usr/share/doc/libgfortran5/copyright`, `/usr/share/doc/libgomp1/copyright`, `/usr/share/doc/libhwasan0/copyright`, `/usr/share/doc/libitm1/copyright`, `/usr/share/doc/liblsan0/copyright`, `/usr/share/doc/libquadmath0/copyright`, `/usr/share/doc/libstdc++-13-dev/copyright`, `/usr/share/doc/libstdc++6/copyright`, `/usr/share/doc/libtsan2/copyright`, `/usr/share/doc/libubsan1/copyright`)

- `Artistic`
- `GFDL-1.2`
- `GPL`
- `GPL-2`
- `GPL-3`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris gcc-13=13.2.0-9ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-13/gcc-13_13.2.0-9ubuntu1.dsc' gcc-13_13.2.0-9ubuntu1.dsc 27690 SHA512:05aff43c50a1b96ecf3f5e373b0b200d157a7ea2d4c2625dec4653877ebdcd39b16bb08b66fcd9efc0e57e083aeb1dd3035525aed084e9d0f8749be5b74aa8d7
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-13/gcc-13_13.2.0.orig.tar.gz' gcc-13_13.2.0.orig.tar.gz 92596024 SHA512:cf149aff3cbee36bf23987e91016fa3f93dbcba8c88319876e6aa3cacd1dacea27d06ea7c4da6394a56d7d9d4f14ac928ead7d25502f0cc6db558f7f5cd99dff
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-13/gcc-13_13.2.0-9ubuntu1.debian.tar.xz' gcc-13_13.2.0-9ubuntu1.debian.tar.xz 1747988 SHA512:9a4555e1e25d7717cb4dc7941fd4af5f288baa12c5cbfff49116e58292dd95f3ae42a8ad36a63426cf1be7ed40359cbd5d274e4381782a7f9d23c4778a73a39e
```

### `dpkg` source package: `gcc-defaults=1.209ubuntu1`

Binary Packages:

- `cpp=4:13.2.0-2ubuntu1`
- `g++=4:13.2.0-2ubuntu1`
- `gcc=4:13.2.0-2ubuntu1`

Licenses: (parsed from: `/usr/share/doc/cpp/copyright`, `/usr/share/doc/g++/copyright`, `/usr/share/doc/gcc/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris gcc-defaults=1.209ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-defaults/gcc-defaults_1.209ubuntu1.dsc' gcc-defaults_1.209ubuntu1.dsc 14931 SHA512:8629bdfd395c43535f5d222999bccaf0d79e2d4eb7263752841339dc1f78b58507967e32d565de9ea5638632c0f8ce5afd4b529e45d51d28a730e36b09730503
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-defaults/gcc-defaults_1.209ubuntu1.tar.xz' gcc-defaults_1.209ubuntu1.tar.xz 48400 SHA512:cb9b43756e70cf5b173acb6fb4ca5cb76385541e5f3fc5a439420a111a3b823357736a59c0ca91add22e4feaabe486e33dd700da0845ca8f670fb2bd4d98f847
```

### `dpkg` source package: `gdbm=1.23-5`

Binary Packages:

- `libgdbm-compat4:amd64=1.23-5`
- `libgdbm-dev:amd64=1.23-5`
- `libgdbm6:amd64=1.23-5`

Licenses: (parsed from: `/usr/share/doc/libgdbm-compat4/copyright`, `/usr/share/doc/libgdbm-dev/copyright`, `/usr/share/doc/libgdbm6/copyright`)

- `GFDL-NIV-1.3+`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris gdbm=1.23-5
'http://archive.ubuntu.com/ubuntu/pool/main/g/gdbm/gdbm_1.23-5.dsc' gdbm_1.23-5.dsc 2426 SHA512:dce21f92cc0b05a4da96f9a163875f2fd017b9d2c6973d099e5fcdebd2eeaacd178447a4852f59ae38e8df40501e8a6f594bd6b629c0cdcc444e7a1ca6e32a1d
'http://archive.ubuntu.com/ubuntu/pool/main/g/gdbm/gdbm_1.23.orig.tar.gz' gdbm_1.23.orig.tar.gz 1115854 SHA512:918080cb0225b221c11eb7339634a95e00c526072395f7a3d46ccf42ef020dea7c4c5bec34aff2c4f16033e1fff6583252b7e978f68b8d7f8736b0e025838e10
'http://archive.ubuntu.com/ubuntu/pool/main/g/gdbm/gdbm_1.23.orig.tar.gz.asc' gdbm_1.23.orig.tar.gz.asc 181 SHA512:6653751c04584f10aa3325bd1cb5b9f7970a786dd2a99602ea620c11a86a9ba5c342aa52627bd06c03da822e9e1600dc034d9a8f42856a287fd67f6b9f161c71
'http://archive.ubuntu.com/ubuntu/pool/main/g/gdbm/gdbm_1.23-5.debian.tar.xz' gdbm_1.23-5.debian.tar.xz 18260 SHA512:b8df3a486f2446974a1f739d383c492cb19a597c577794f503c2395ea53425f8f385d0e761164dbd5efc82a6aa7705386376c12f70befdc03836d4a795ed2ec7
```

### `dpkg` source package: `gdk-pixbuf=2.42.10+dfsg-3`

Binary Packages:

- `gir1.2-gdkpixbuf-2.0:amd64=2.42.10+dfsg-3`
- `libgdk-pixbuf-2.0-0:amd64=2.42.10+dfsg-3`
- `libgdk-pixbuf-2.0-dev:amd64=2.42.10+dfsg-3`
- `libgdk-pixbuf2.0-bin=2.42.10+dfsg-3`
- `libgdk-pixbuf2.0-common=2.42.10+dfsg-3`

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
$ apt-get source -qq --print-uris gdk-pixbuf=2.42.10+dfsg-3
'http://archive.ubuntu.com/ubuntu/pool/main/g/gdk-pixbuf/gdk-pixbuf_2.42.10%2bdfsg-3.dsc' gdk-pixbuf_2.42.10+dfsg-3.dsc 3214 SHA512:c3cfd2f9d0ab1ea91dc0e2ec5049de265c90cb326b31215dea0cf8908f8e961fc44e91355f6c879004cb02e1d73796f29f8168f709017459d1dc2df2f0c3c5cb
'http://archive.ubuntu.com/ubuntu/pool/main/g/gdk-pixbuf/gdk-pixbuf_2.42.10%2bdfsg.orig.tar.xz' gdk-pixbuf_2.42.10+dfsg.orig.tar.xz 6439240 SHA512:34f8d7d44d12308c57bd9622efdb7344bad5a89bad7043b40d4d1cab4112ff505ebb9df98d788068ddd2e44cee193e7bcb4f1d56f0432cc859075425652a06fc
'http://archive.ubuntu.com/ubuntu/pool/main/g/gdk-pixbuf/gdk-pixbuf_2.42.10%2bdfsg-3.debian.tar.xz' gdk-pixbuf_2.42.10+dfsg-3.debian.tar.xz 21336 SHA512:28f94a46c001303c958c0593e7f3cf3a23d4136cedf790c8712f562c8c96f8433f91c424d1cd91147a304f66754b0a3ec74b9ab131c7871c69094d1aebae02d0
```

### `dpkg` source package: `git=1:2.43.0-1ubuntu1`

Binary Packages:

- `git=1:2.43.0-1ubuntu1`
- `git-man=1:2.43.0-1ubuntu1`

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
$ apt-get source -qq --print-uris git=1:2.43.0-1ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/g/git/git_2.43.0-1ubuntu1.dsc' git_2.43.0-1ubuntu1.dsc 2919 SHA512:36c73f26e603610e46109dd946c43425434fcbb7898c670f55108a92800f2211b09538456a332352c5251f59b87865723812a8bf71a9ab1bfc71fb1c2d942018
'http://archive.ubuntu.com/ubuntu/pool/main/g/git/git_2.43.0.orig.tar.xz' git_2.43.0.orig.tar.xz 7382996 SHA512:d0c1694ae23ff7d523e617b98d7c9a9753a2ee58f92c21b67a192d1c57398a62ff9c1a34558ae31af8dc8d95122c219f39f654e99a3b4e7cfc3dd07be9e13203
'http://archive.ubuntu.com/ubuntu/pool/main/g/git/git_2.43.0-1ubuntu1.debian.tar.xz' git_2.43.0-1ubuntu1.debian.tar.xz 765884 SHA512:ddbb89e10db076ad7447363fb51bd90ea32d264a166950a388f6e43799dc13a4d50d84b81858a131a11fe64a03a08e3ecfa6cffc7898ac783425faf66f597ec2
```

### `dpkg` source package: `glib2.0=2.78.3-1`

Binary Packages:

- `libglib2.0-0:amd64=2.78.3-1`
- `libglib2.0-bin=2.78.3-1`
- `libglib2.0-data=2.78.3-1`
- `libglib2.0-dev:amd64=2.78.3-1`
- `libglib2.0-dev-bin=2.78.3-1`

Licenses: (parsed from: `/usr/share/doc/libglib2.0-0/copyright`, `/usr/share/doc/libglib2.0-bin/copyright`, `/usr/share/doc/libglib2.0-data/copyright`, `/usr/share/doc/libglib2.0-dev/copyright`, `/usr/share/doc/libglib2.0-dev-bin/copyright`)

- `AFL-2.0`
- `Apache-2.0`
- `Apache-2.0 with LLVM exception`
- `BSD-3-clause-pcre`
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
- `Mingw-PD`
- `Old-GLib-Tests-permissive`
- `Plumb-PD`
- `Unicode-DFS-2016`
- `bzip2-1.0.6`

Source:

```console
$ apt-get source -qq --print-uris glib2.0=2.78.3-1
'http://archive.ubuntu.com/ubuntu/pool/main/g/glib2.0/glib2.0_2.78.3-1.dsc' glib2.0_2.78.3-1.dsc 3648 SHA512:2986302a24c0c957065effe133758337ae460b3bae912c989f2b5037e191aa9275c2da851bada2c36a80ffdcf301d112722661b2dbb08897ea13811a6cb577d1
'http://archive.ubuntu.com/ubuntu/pool/main/g/glib2.0/glib2.0_2.78.3.orig-unicode-data.tar.xz' glib2.0_2.78.3.orig-unicode-data.tar.xz 266184 SHA512:c818eae7b8df69b69abc2c59870eaad7488e3266afb5055b851fcbdd9dd96d9808787881631a8d840487acb3b40c18691b6c58d3df4735fa6eab41a5aa1295ff
'http://archive.ubuntu.com/ubuntu/pool/main/g/glib2.0/glib2.0_2.78.3.orig.tar.xz' glib2.0_2.78.3.orig.tar.xz 5321388 SHA512:9c1af75fb973d23ce0286d5b7836eea45f9628c148ced5ac10e10abceda05024ae4c57f01439824d3287d986527500b7b959828b630b6e4a3314b5224f4d7246
'http://archive.ubuntu.com/ubuntu/pool/main/g/glib2.0/glib2.0_2.78.3-1.debian.tar.xz' glib2.0_2.78.3-1.debian.tar.xz 119908 SHA512:8a1679448576949d8b30072ed0dadfb6f7ff7055c47d5f6b607454996b15c14e2954b1e5a9d58d0a389e34e0cfea28d55c10be1a3e6fb4954eb2ef7fbac212df
```

### `dpkg` source package: `glibc=2.38-3ubuntu1`

Binary Packages:

- `libc-bin=2.38-3ubuntu1`
- `libc-dev-bin=2.38-3ubuntu1`
- `libc6:amd64=2.38-3ubuntu1`
- `libc6-dev:amd64=2.38-3ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libc-bin/copyright`, `/usr/share/doc/libc-dev-bin/copyright`, `/usr/share/doc/libc6/copyright`, `/usr/share/doc/libc6-dev/copyright`)

- `GFDL-1.3`
- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris glibc=2.38-3ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.38-3ubuntu1.dsc' glibc_2.38-3ubuntu1.dsc 9310 SHA512:de01b8db04324f5d375a9ebd6247b3c0b126eac983edc6ff9e03b294bdeeb297630e4b7894e6b04ff81844d17d0342eeb22e662c5a97373f00c2508ee9ab5dc3
'http://archive.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.38.orig.tar.xz' glibc_2.38.orig.tar.xz 18913712 SHA512:a6dd5e42dcd63d58e2820c783522c8c895890b6e8c8e6c83b025553de0cc77cdf227e7044e431ead98c89c68a9ce4dd63509b47e647775fb2075f011849c1900
'http://archive.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.38.orig.tar.xz.asc' glibc_2.38.orig.tar.xz.asc 833 SHA512:32248467450f4530f8e84c03ea78d8293946e1b1def853eff9fb2cb51106e66cc3b024a254f3c2fabd2634f8192bd14e7df00c317f4230860d702c4d9ec7a01e
'http://archive.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.38-3ubuntu1.debian.tar.xz' glibc_2.38-3ubuntu1.debian.tar.xz 456828 SHA512:cad380328036402b74bf614a8970daec9be7a90bca5fa21552db56cecdd25122f5720eda8f2dc13dae4c583477458d485beceacbced9df4e46d7de44e36b7100
```

### `dpkg` source package: `gmp=2:6.3.0+dfsg-2ubuntu4`

Binary Packages:

- `libgmp-dev:amd64=2:6.3.0+dfsg-2ubuntu4`
- `libgmp10:amd64=2:6.3.0+dfsg-2ubuntu4`
- `libgmpxx4ldbl:amd64=2:6.3.0+dfsg-2ubuntu4`

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
- `gpg=2.2.40-1.1ubuntu1`
- `gpg-agent=2.2.40-1.1ubuntu1`
- `gpg-wks-client=2.2.40-1.1ubuntu1`
- `gpg-wks-server=2.2.40-1.1ubuntu1`
- `gpgconf=2.2.40-1.1ubuntu1`
- `gpgsm=2.2.40-1.1ubuntu1`
- `gpgv=2.2.40-1.1ubuntu1`

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
$ apt-get source -qq --print-uris gnupg2=2.2.40-1.1ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnupg2/gnupg2_2.2.40-1.1ubuntu1.dsc' gnupg2_2.2.40-1.1ubuntu1.dsc 3920 SHA512:c2cfd636e9bdfc8fe19d9213597325782fe15bd228d0e7d601f18c37d23c2be81c62337621bb835d2defc85feade8f67c4a7f680902d32c77f112cfa2258c7bb
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnupg2/gnupg2_2.2.40.orig.tar.bz2' gnupg2_2.2.40.orig.tar.bz2 7301631 SHA512:4c2f5fbf37ba6fbad0045aad23129186963010c673ea0b81801adc4f98efe14d6c7228e22815b6b26307c1fe5bb51cd088aa6a0f06a9325d3c021849ef81c594
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnupg2/gnupg2_2.2.40.orig.tar.bz2.asc' gnupg2_2.2.40.orig.tar.bz2.asc 228 SHA512:50e8abae322430bf4d3230d0291ca519663a1397fe0d0b8df29076808504b5fea2b984952d6dc51ecc239c12af8ecd5d93b88dd1c6bc0babf0b48a5a840b8ada
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnupg2/gnupg2_2.2.40-1.1ubuntu1.debian.tar.xz' gnupg2_2.2.40-1.1ubuntu1.debian.tar.xz 65264 SHA512:1efaad1ebfcda85888670e613bb4488ff2ad773190a593f4d2ac298e731a5641e84bfc2c0dba4b5fd8f1af455212a388b99f903dfc770a772d45b4ccaafcb2e1
```

### `dpkg` source package: `gnutls28=3.8.1-4ubuntu6`

Binary Packages:

- `libgnutls30:amd64=3.8.1-4ubuntu6`

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
$ apt-get source -qq --print-uris gnutls28=3.8.1-4ubuntu6
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.8.1-4ubuntu6.dsc' gnutls28_3.8.1-4ubuntu6.dsc 3338 SHA512:33717f1a9de0cd2848c761efa18e4fdebeb2a26cd2dd795fe8dafcc4db62b282bcbecd515a1d8b8d0e18f6c5d5c611f863c7569b3dd5488681367d7c4840d341
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.8.1.orig.tar.xz' gnutls28_3.8.1.orig.tar.xz 6447056 SHA512:22e78db86b835843df897d14ad633d8a553c0f9b1389daa0c2f864869c6b9ca889028d434f9552237dc4f1b37c978fbe0cce166e3768e5d4e8850ff69a6fc872
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.8.1.orig.tar.xz.asc' gnutls28_3.8.1.orig.tar.xz.asc 996 SHA512:ad42a077718a91b82959ee7ed8282b69e73825c70c5c60eb4a1f87aab055dee2ac74a03f489d5f11c2094ec6ac01ea44c0daffb61cb4daae714dcaf5ea89ecd0
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.8.1-4ubuntu6.debian.tar.xz' gnutls28_3.8.1-4ubuntu6.debian.tar.xz 73692 SHA512:64067f9c5a548cb44bc34c2a564531142bd27ce490773d5c9f4161cb4aebd9d290e5cb9a2e1df3ebd12e6b01bc53ec842ffe066447be7461860f49ba4aa178b0
```

### `dpkg` source package: `gobject-introspection=1.78.1-6`

Binary Packages:

- `gir1.2-freedesktop:amd64=1.78.1-6`
- `gir1.2-glib-2.0:amd64=1.78.1-6`
- `libgirepository-1.0-1:amd64=1.78.1-6`

Licenses: (parsed from: `/usr/share/doc/gir1.2-freedesktop/copyright`, `/usr/share/doc/gir1.2-glib-2.0/copyright`, `/usr/share/doc/libgirepository-1.0-1/copyright`)

- `AFL-2.0`
- `Apache-2.0`
- `Apache-2.0 with LLVM exception`
- `BSD-2-clause`
- `BSD-3-clause-pcre`
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
$ apt-get source -qq --print-uris gobject-introspection=1.78.1-6
'http://archive.ubuntu.com/ubuntu/pool/main/g/gobject-introspection/gobject-introspection_1.78.1-6.dsc' gobject-introspection_1.78.1-6.dsc 3663 SHA512:715c70832d66675a5322e1650ea2a9088a939a7e5b8a239fe7fd10622c939c3849b744d6821dbbfbdb97f0e1dfe620b52356ca701694a3ca32172552ebd3fbf5
'http://archive.ubuntu.com/ubuntu/pool/main/g/gobject-introspection/gobject-introspection_1.78.1.orig-glib.tar.xz' gobject-introspection_1.78.1.orig-glib.tar.xz 5327096 SHA512:3d06890002f4b13f831c83fbb70cfce529f9750e30888619e4d6277116be15d106379a03143412cf4b2a289c0cbdbbc299ecf17284fbffc06c791ecf7556c765
'http://archive.ubuntu.com/ubuntu/pool/main/g/gobject-introspection/gobject-introspection_1.78.1.orig.tar.xz' gobject-introspection_1.78.1.orig.tar.xz 1060296 SHA512:a3081882995a762645b04faa71082dbd523bee845519007e48b13235aad8a4cd4c74f0d042a6c17710125f945bd970e4b76e95a559274e294d595e04725a4e97
'http://archive.ubuntu.com/ubuntu/pool/main/g/gobject-introspection/gobject-introspection_1.78.1-6.debian.tar.xz' gobject-introspection_1.78.1-6.debian.tar.xz 53244 SHA512:07ad84c73387b4ee7c765d76272551f3c5489161b5defa9cd59fe51520f7b4abf19dd7574789eb83cc04c357e89a331addb49c2dce0ef78ebc6ea59bf55fe703
```

### `dpkg` source package: `graphite2=1.3.14-2`

Binary Packages:

- `libgraphite2-3:amd64=1.3.14-2`

Licenses: (parsed from: `/usr/share/doc/libgraphite2-3/copyright`)

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
$ apt-get source -qq --print-uris graphite2=1.3.14-2
'http://archive.ubuntu.com/ubuntu/pool/main/g/graphite2/graphite2_1.3.14-2.dsc' graphite2_1.3.14-2.dsc 2568 SHA512:e9f732ed3bd953ac5d6b90e1a0a353a35625ac3bb9e250696398afe772b64a4c35a76c5ca52ba2131d9e70d6597294c82397fe658b859358c0a2d0c21ee2eaa4
'http://archive.ubuntu.com/ubuntu/pool/main/g/graphite2/graphite2_1.3.14.orig.tar.gz' graphite2_1.3.14.orig.tar.gz 6629829 SHA512:49d127964d3f5c9403c7aecbfb5b18f32f25fe4919a81c49e0534e7123fe845423e16b0b8c8baaae21162b1150ab3e0f1c22c344e07d4364b6b8473c40a0822c
'http://archive.ubuntu.com/ubuntu/pool/main/g/graphite2/graphite2_1.3.14-2.debian.tar.xz' graphite2_1.3.14-2.debian.tar.xz 14168 SHA512:19ffd7d2c98c82177d8f2db5e4c509c30ba4ad916932d380133cb49be35d50c799dae204ca550d178a9711eafd4a46c5abab43eb255ca25253ad0dab768ed8ea
```

### `dpkg` source package: `grep=3.11-3`

Binary Packages:

- `grep=3.11-3`

Licenses: (parsed from: `/usr/share/doc/grep/copyright`)

- `GPL-3`
- `GPL-3+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/grep/3.11-3/


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

### `dpkg` source package: `harfbuzz=8.0.1-1build1`

Binary Packages:

- `libharfbuzz0b:amd64=8.0.1-1build1`

Licenses: (parsed from: `/usr/share/doc/libharfbuzz0b/copyright`)

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
$ apt-get source -qq --print-uris harfbuzz=8.0.1-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/h/harfbuzz/harfbuzz_8.0.1-1build1.dsc' harfbuzz_8.0.1-1build1.dsc 2866 SHA512:833300e2fbbfaf377bf0ad9185ca6efa039f1a7d3dda1ae3a5f7ea67ce55f6bec652698b01974cce7c026019510db2507ef6f8621363507549b7c690949b54a7
'http://archive.ubuntu.com/ubuntu/pool/main/h/harfbuzz/harfbuzz_8.0.1.orig.tar.xz' harfbuzz_8.0.1.orig.tar.xz 18792332 SHA512:e1292f059b07a5aa2f3fbf345b893209cac895c461b4abf30b8b76bcd03c79dd09f911450293403070e1a0bb08496a7f37693ba5a62a9d423dd6ba55e744444d
'http://archive.ubuntu.com/ubuntu/pool/main/h/harfbuzz/harfbuzz_8.0.1-1build1.debian.tar.xz' harfbuzz_8.0.1-1build1.debian.tar.xz 19680 SHA512:022df661442878452fbcb442a25249fb68f39abd3bd5bd81e5990a8d2f7061bcf915d7fad06d262344ffb1b37aa1970a432891ae0bd8c51aa60c42845c864895
```

### `dpkg` source package: `hicolor-icon-theme=0.17-2`

Binary Packages:

- `hicolor-icon-theme=0.17-2`

Licenses: (parsed from: `/usr/share/doc/hicolor-icon-theme/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris hicolor-icon-theme=0.17-2
'http://archive.ubuntu.com/ubuntu/pool/main/h/hicolor-icon-theme/hicolor-icon-theme_0.17-2.dsc' hicolor-icon-theme_0.17-2.dsc 2053 SHA512:5b8b3088f8d9469076d5d2a3448e1115a910958a4ba4b3bbeae287ae3e91fa3a26b87f544a1f92925230e33f6f20e96df51bc5ec01b2735e07bb3f9be2e06c3c
'http://archive.ubuntu.com/ubuntu/pool/main/h/hicolor-icon-theme/hicolor-icon-theme_0.17.orig.tar.xz' hicolor-icon-theme_0.17.orig.tar.xz 53016 SHA512:eca8655930aa7e234f42630041c0053fde067b970fad1f81c55fcd4c5046c03edfdf2ede72a3e78fba2908e7da53e9463d3c5ae12ab9f5ef261e29a49f9c7a8d
'http://archive.ubuntu.com/ubuntu/pool/main/h/hicolor-icon-theme/hicolor-icon-theme_0.17-2.debian.tar.xz' hicolor-icon-theme_0.17-2.debian.tar.xz 3536 SHA512:74b8de58f18f861f0f724419514b787495cf67b39abcfdbdc7be6923e44112b86710c015ea5e4c83301d201b503a1014fca335c6dadc522d7f7edca80f638489
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

### `dpkg` source package: `icu=74.2-1ubuntu1`

Binary Packages:

- `icu-devtools=74.2-1ubuntu1`
- `libicu-dev:amd64=74.2-1ubuntu1`
- `libicu74:amd64=74.2-1ubuntu1`

Licenses: (parsed from: `/usr/share/doc/icu-devtools/copyright`, `/usr/share/doc/libicu-dev/copyright`, `/usr/share/doc/libicu74/copyright`)

- `GPL-3`
- `MIT`

Source:

```console
$ apt-get source -qq --print-uris icu=74.2-1ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/i/icu/icu_74.2-1ubuntu1.dsc' icu_74.2-1ubuntu1.dsc 2274 SHA512:90e784c760b679f3a5caa6af0f9388693f230d2edc072315b14c81eec3b737649dc2ba706390ee2196faf1546d3904cbe2534b2ee2813434f53b537848a18722
'http://archive.ubuntu.com/ubuntu/pool/main/i/icu/icu_74.2.orig.tar.gz' icu_74.2.orig.tar.gz 26618071 SHA512:0cbe29122370ba03a8fb5b0f1494f598748044ad2aa4d66ba65fe98ebeb88da2d73d324ad6bfc44e004846e0ab5c9a34d1fdf3d6bdb3095c0d47e929b943e6db
'http://archive.ubuntu.com/ubuntu/pool/main/i/icu/icu_74.2.orig.tar.gz.asc' icu_74.2.orig.tar.gz.asc 659 SHA512:e961664f91a66afe898041fb42950f925854cfe7f5a287f691b90ad79c215a14300cdd1aad94a310aa2b1cdda3d850ab978d1fe2eadba5fd46f375f4bcefcd11
'http://archive.ubuntu.com/ubuntu/pool/main/i/icu/icu_74.2-1ubuntu1.debian.tar.xz' icu_74.2-1ubuntu1.debian.tar.xz 64320 SHA512:ac108288e56e95580cd850338724bed9f70a21fd15e40c43eaf0a3fd63805ff0869655d8a9dc26b0f7ea3b2f553f41281910b4a1e6e0828fe35690584cb39a26
```

### `dpkg` source package: `imagemagick=8:6.9.11.60+dfsg-1.6ubuntu1`

Binary Packages:

- `imagemagick=8:6.9.11.60+dfsg-1.6ubuntu1`
- `imagemagick-6-common=8:6.9.11.60+dfsg-1.6ubuntu1`
- `imagemagick-6.q16=8:6.9.11.60+dfsg-1.6ubuntu1`
- `libmagickcore-6-arch-config:amd64=8:6.9.11.60+dfsg-1.6ubuntu1`
- `libmagickcore-6-headers=8:6.9.11.60+dfsg-1.6ubuntu1`
- `libmagickcore-6.q16-6:amd64=8:6.9.11.60+dfsg-1.6ubuntu1`
- `libmagickcore-6.q16-6-extra:amd64=8:6.9.11.60+dfsg-1.6ubuntu1`
- `libmagickcore-6.q16-dev:amd64=8:6.9.11.60+dfsg-1.6ubuntu1`
- `libmagickcore-dev=8:6.9.11.60+dfsg-1.6ubuntu1`
- `libmagickwand-6-headers=8:6.9.11.60+dfsg-1.6ubuntu1`
- `libmagickwand-6.q16-6:amd64=8:6.9.11.60+dfsg-1.6ubuntu1`
- `libmagickwand-6.q16-dev:amd64=8:6.9.11.60+dfsg-1.6ubuntu1`
- `libmagickwand-dev=8:6.9.11.60+dfsg-1.6ubuntu1`

Licenses: (parsed from: `/usr/share/doc/imagemagick/copyright`, `/usr/share/doc/imagemagick-6-common/copyright`, `/usr/share/doc/imagemagick-6.q16/copyright`, `/usr/share/doc/libmagickcore-6-arch-config/copyright`, `/usr/share/doc/libmagickcore-6-headers/copyright`, `/usr/share/doc/libmagickcore-6.q16-6/copyright`, `/usr/share/doc/libmagickcore-6.q16-6-extra/copyright`, `/usr/share/doc/libmagickcore-6.q16-dev/copyright`, `/usr/share/doc/libmagickcore-dev/copyright`, `/usr/share/doc/libmagickwand-6-headers/copyright`, `/usr/share/doc/libmagickwand-6.q16-6/copyright`, `/usr/share/doc/libmagickwand-6.q16-dev/copyright`, `/usr/share/doc/libmagickwand-dev/copyright`)

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
- `TatcherUlrichPublicDomain`
- `aclocal`

Source:

```console
$ apt-get source -qq --print-uris imagemagick=8:6.9.11.60+dfsg-1.6ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/universe/i/imagemagick/imagemagick_6.9.11.60%2bdfsg-1.6ubuntu1.dsc' imagemagick_6.9.11.60+dfsg-1.6ubuntu1.dsc 5181 SHA512:ae83028055840700dd8f6ff93e1d15a2ea325353800884fde1318c3b9c73a2c165191739b306bd9776fa8dd59f82f5c77845817e9c15bb6261fda998c8795be8
'http://archive.ubuntu.com/ubuntu/pool/universe/i/imagemagick/imagemagick_6.9.11.60%2bdfsg.orig.tar.xz' imagemagick_6.9.11.60+dfsg.orig.tar.xz 9395144 SHA512:345a23eda96516fc7a213bd4a322bca4c8b690efe40ff7b498a448f8cedd7f0d600fae2cb6fff45bc995779a90d8c04b58288273eee97833ddebb4f9f2a3d14c
'http://archive.ubuntu.com/ubuntu/pool/universe/i/imagemagick/imagemagick_6.9.11.60%2bdfsg-1.6ubuntu1.debian.tar.xz' imagemagick_6.9.11.60+dfsg-1.6ubuntu1.debian.tar.xz 259460 SHA512:b14064854623591a848cb6ab57b550e9d864d2971497ec48d5c7a9e23d9ae4eae6ab297ea30b00175e947fc1ffc46463ae683423bba83728ce078f13a5502afa
```

### `dpkg` source package: `imath=3.1.9-3ubuntu2`

Binary Packages:

- `libimath-3-1-29:amd64=3.1.9-3ubuntu2`
- `libimath-dev:amd64=3.1.9-3ubuntu2`
- `python3-imath:amd64=3.1.9-3ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libimath-3-1-29/copyright`, `/usr/share/doc/libimath-dev/copyright`, `/usr/share/doc/python3-imath/copyright`)

- `imath`

Source:

```console
$ apt-get source -qq --print-uris imath=3.1.9-3ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/universe/i/imath/imath_3.1.9-3ubuntu2.dsc' imath_3.1.9-3ubuntu2.dsc 2648 SHA512:4d2a94b7ac3a27e8407d775ac6be140bc283da798f3469a8092b35b36efc4eedcfb0f7cb793a49bcedcb9755e6ec0c9060b28be38efe0093ea8cf0b9c15412ae
'http://archive.ubuntu.com/ubuntu/pool/universe/i/imath/imath_3.1.9.orig.tar.gz' imath_3.1.9.orig.tar.gz 598497 SHA512:ad96b2ac306fc13c01e8ea3256f885499c3f545be327feaba0f5e093b70b544bcca6f8b353fa7e35107aae515c19caced44331a95d0414f367ead4691ec73564
'http://archive.ubuntu.com/ubuntu/pool/universe/i/imath/imath_3.1.9.orig.tar.gz.asc' imath_3.1.9.orig.tar.gz.asc 287 SHA512:9b3978e44b531429aba42b9cc4969a470898d9d74652e3809edb0273ba9b127c471aec6570b5d352be738f59810091c0df2c70d39c16d2c32833d173b270f72c
'http://archive.ubuntu.com/ubuntu/pool/universe/i/imath/imath_3.1.9-3ubuntu2.debian.tar.xz' imath_3.1.9-3ubuntu2.debian.tar.xz 9484 SHA512:55b3d3ac8d8cea885acb63a32ff959cf23dd30b3084a80495c028b74861426dd7e22cb98fb1616c4daf8c7bfaf8a97e40da6f4f2911b2390cc017fdbcb51ecd3
```

### `dpkg` source package: `init-system-helpers=1.65.2ubuntu1`

Binary Packages:

- `init-system-helpers=1.65.2ubuntu1`

Licenses: (parsed from: `/usr/share/doc/init-system-helpers/copyright`)

- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `isl=0.26-3`

Binary Packages:

- `libisl23:amd64=0.26-3`

Licenses: (parsed from: `/usr/share/doc/libisl23/copyright`)

- `BSD-2-clause`
- `LGPL-2`
- `LGPL-2.1+`
- `MIT`

Source:

```console
$ apt-get source -qq --print-uris isl=0.26-3
'http://archive.ubuntu.com/ubuntu/pool/main/i/isl/isl_0.26-3.dsc' isl_0.26-3.dsc 1832 SHA512:83773ff0dc5e4f909530a9fee6c2ebed113bf1493f335ed44aaddb530dae55cfad31ad6f1b4c5426eecb7304d5ec159bab60edff4557ca5ef82f3bf1ca6e36e3
'http://archive.ubuntu.com/ubuntu/pool/main/i/isl/isl_0.26.orig.tar.xz' isl_0.26.orig.tar.xz 2035560 SHA512:9b5ec16d14e48f9ac9bf9cd379d3022959cfc617ade9e0d4caf2862299564fecba09d67dbdf1a4071f2f743a4fd0fabd0b0c3d15f5cddfe7226cdd5d6c2a0c66
'http://archive.ubuntu.com/ubuntu/pool/main/i/isl/isl_0.26-3.debian.tar.xz' isl_0.26-3.debian.tar.xz 24700 SHA512:23944f19bbc74fb546c6a0183c74605a038241eec1be2494f5ed2e3734c99d2484cbc4eac1168bd115a01651ab5a07138d1f4e75876c0f1836dd98f389a05616
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

- `libjbig-dev:amd64=2.1-6.1ubuntu1`
- `libjbig0:amd64=2.1-6.1ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libjbig-dev/copyright`, `/usr/share/doc/libjbig0/copyright`)

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

### `dpkg` source package: `krb5=1.20.1-5build1`

Binary Packages:

- `krb5-multidev:amd64=1.20.1-5build1`
- `libgssapi-krb5-2:amd64=1.20.1-5build1`
- `libgssrpc4:amd64=1.20.1-5build1`
- `libk5crypto3:amd64=1.20.1-5build1`
- `libkadm5clnt-mit12:amd64=1.20.1-5build1`
- `libkadm5srv-mit12:amd64=1.20.1-5build1`
- `libkdb5-10:amd64=1.20.1-5build1`
- `libkrb5-3:amd64=1.20.1-5build1`
- `libkrb5-dev:amd64=1.20.1-5build1`
- `libkrb5support0:amd64=1.20.1-5build1`

Licenses: (parsed from: `/usr/share/doc/krb5-multidev/copyright`, `/usr/share/doc/libgssapi-krb5-2/copyright`, `/usr/share/doc/libgssrpc4/copyright`, `/usr/share/doc/libk5crypto3/copyright`, `/usr/share/doc/libkadm5clnt-mit12/copyright`, `/usr/share/doc/libkadm5srv-mit12/copyright`, `/usr/share/doc/libkdb5-10/copyright`, `/usr/share/doc/libkrb5-3/copyright`, `/usr/share/doc/libkrb5-dev/copyright`, `/usr/share/doc/libkrb5support0/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris krb5=1.20.1-5build1
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.20.1-5build1.dsc' krb5_1.20.1-5build1.dsc 3933 SHA512:5b2da996dde2fb66fd44b759f21e641e8a408df17123283d1a245355d2f8ce880a56aea3a65c506404b59e2ca63708b49f0aa9dcffcf6837487f00af25fd1ff5
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.20.1.orig.tar.gz' krb5_1.20.1.orig.tar.gz 8661660 SHA512:6f57479f13f107cd84f30de5c758eb6b9fc59171329c13e5da6073b806755f8d163eb7bd84767ea861ad6458ea0c9eeb00ee044d3bcad01ef136e9888564b6a2
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.20.1.orig.tar.gz.asc' krb5_1.20.1.orig.tar.gz.asc 833 SHA512:1d3312bd67581e07adfdadf2c5fe394179631d8add8bd075efefe982a0de22369004e60a14422d426382c8c591e4181b9897088afe9d4e86f0b5a97e5954c67a
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.20.1-5build1.debian.tar.xz' krb5_1.20.1-5build1.debian.tar.xz 104588 SHA512:686aa216b2b5cce1c13e7f967d30eb79f0c9bf71dbffefbf4292d9eef3a36702aa819b8c5cd7a1e9a92e547c8af7d2a2ca647dd8311b1ee378aef8dbe41d6404
```

### `dpkg` source package: `lapack=3.11.0-2build1`

Binary Packages:

- `libblas3:amd64=3.11.0-2build1`
- `liblapack3:amd64=3.11.0-2build1`

Licenses: (parsed from: `/usr/share/doc/libblas3/copyright`, `/usr/share/doc/liblapack3/copyright`)

- `BSD-3-clause`
- `BSD-3-clause-intel`

Source:

```console
$ apt-get source -qq --print-uris lapack=3.11.0-2build1
'http://archive.ubuntu.com/ubuntu/pool/main/l/lapack/lapack_3.11.0-2build1.dsc' lapack_3.11.0-2build1.dsc 3331 SHA512:df95bf7d12c3ae3dd416ebc49d5d63df880f4d8178ac1c8ea5f114db48a901ca4bbc5bc36a025fc36b96455eddb12ecfb4e7b3f9972202791182a6ea99071fe4
'http://archive.ubuntu.com/ubuntu/pool/main/l/lapack/lapack_3.11.0.orig.tar.gz' lapack_3.11.0.orig.tar.gz 7723808 SHA512:fc3258b9d91a833149a68a89c5589b5113e90a8f9f41c3a73fbfccb1ecddd92d9462802c0f870f1c3dab392623452de4ef512727f5874ffdcba6a4845f78fc9a
'http://archive.ubuntu.com/ubuntu/pool/main/l/lapack/lapack_3.11.0-2build1.debian.tar.xz' lapack_3.11.0-2build1.debian.tar.xz 33008 SHA512:55d2d9715a46c2daffb3566c6b80be85d82af42d683638323a04c0b4e8a01a30bd52c711d4e08c7050ec09515c4195eba3ac92d6e49713354660866e5524de38
```

### `dpkg` source package: `lcms2=2.14-2`

Binary Packages:

- `liblcms2-2:amd64=2.14-2`
- `liblcms2-dev:amd64=2.14-2`

Licenses: (parsed from: `/usr/share/doc/liblcms2-2/copyright`, `/usr/share/doc/liblcms2-dev/copyright`)

- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `IJG`
- `MIT`

Source:

```console
$ apt-get source -qq --print-uris lcms2=2.14-2
'http://archive.ubuntu.com/ubuntu/pool/main/l/lcms2/lcms2_2.14-2.dsc' lcms2_2.14-2.dsc 1944 SHA512:0efbd4625439773c89535ad118567c240d8c555e8069712afcf139067cff5186d554824c6f2ed1d955c4b093bae0c4131419761726937e4b09256939944cc911
'http://archive.ubuntu.com/ubuntu/pool/main/l/lcms2/lcms2_2.14.orig.tar.gz' lcms2_2.14.orig.tar.gz 7406694 SHA512:92fba0a457ea81590eba0b8d98b7b621da6a83e3857948585e0b524235954954f9ac1670cf6a19b457c0fce22a87899ea4c5810db1ff2acf7c6b6e0dc4b61a1b
'http://archive.ubuntu.com/ubuntu/pool/main/l/lcms2/lcms2_2.14-2.debian.tar.xz' lcms2_2.14-2.debian.tar.xz 11728 SHA512:ddadbc46e78a7fbb6d75f13d7921b6710fb28c47cc2a311c7dc79e9a016ef98b81cef1e94d1b4b58af4f396b3dfb320d9f48ec6460a5afd31ead78a6040593b2
```

### `dpkg` source package: `lerc=4.0.0+ds-4ubuntu1`

Binary Packages:

- `liblerc-dev:amd64=4.0.0+ds-4ubuntu1`
- `liblerc4:amd64=4.0.0+ds-4ubuntu1`

Licenses: (parsed from: `/usr/share/doc/liblerc-dev/copyright`, `/usr/share/doc/liblerc4/copyright`)

- `Apache-2.0`

Source:

```console
$ apt-get source -qq --print-uris lerc=4.0.0+ds-4ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/l/lerc/lerc_4.0.0%2bds-4ubuntu1.dsc' lerc_4.0.0+ds-4ubuntu1.dsc 2704 SHA512:7db8f272a72a0bc98ca6786d9d2eefe12604198779765f50adef6c986c04cc1152a96ff4411313b444f89b3eb3f8638890fd9a3523667de8a833472fa3c00802
'http://archive.ubuntu.com/ubuntu/pool/main/l/lerc/lerc_4.0.0%2bds.orig.tar.xz' lerc_4.0.0+ds.orig.tar.xz 348140 SHA512:d5539360fa92f40319466fea73a66d0d03aedff886fb75985bfcaeeb77ef516b9fa24b8d83da09c114bf6090bbd68e64d9ac2649a19315895134fa86023478e1
'http://archive.ubuntu.com/ubuntu/pool/main/l/lerc/lerc_4.0.0%2bds-4ubuntu1.debian.tar.xz' lerc_4.0.0+ds-4ubuntu1.debian.tar.xz 7256 SHA512:e46d6e0ef0ce785d24da45d18ffc17b3a81a4d92ea73e0cef34d18dc049e5aad0dab9c57023b4d9ba057728121389b0164d532c281c80ec25a1ca628f5814192
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

### `dpkg` source package: `libcap-ng=0.8.3-3`

Binary Packages:

- `libcap-ng0:amd64=0.8.3-3`

Licenses: (parsed from: `/usr/share/doc/libcap-ng0/copyright`)

- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `LGPL-2.1`
- `LGPL-2.1+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/libcap-ng/0.8.3-3/


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

### `dpkg` source package: `libcbor=0.10.2-1.1ubuntu1`

Binary Packages:

- `libcbor0.10:amd64=0.10.2-1.1ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libcbor0.10/copyright`)

- `Expat`

Source:

```console
$ apt-get source -qq --print-uris libcbor=0.10.2-1.1ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcbor/libcbor_0.10.2-1.1ubuntu1.dsc' libcbor_0.10.2-1.1ubuntu1.dsc 2213 SHA512:5aa531f3358071f5709b01e684401ebca0df403b5cbefe219ec5f8690356a1a8596387d8adc90c173d1ab806bc47a5a17c755e6a17febcbddb8aa580413d62c4
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcbor/libcbor_0.10.2.orig.tar.gz' libcbor_0.10.2.orig.tar.gz 289450 SHA512:23c6177443778d4b4833ec7ed0d0e639a0d4863372e3a38d772fdce2673eae6d5cb2a31a2a021d1a699082ea53494977c907fd0e94149b97cb23a4b6d039228a
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcbor/libcbor_0.10.2-1.1ubuntu1.debian.tar.xz' libcbor_0.10.2-1.1ubuntu1.debian.tar.xz 5412 SHA512:815dc9102d7cdf74b42655b805a447cdd2fbeecea74b3ee63530f1159b1d8102d3b98ff65f76a4087812970fd45f6a455fc6d44fba4f1eb4f4c4ceef6533f09b
```

### `dpkg` source package: `libdatrie=0.2.13-2`

Binary Packages:

- `libdatrie1:amd64=0.2.13-2`

Licenses: (parsed from: `/usr/share/doc/libdatrie1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/libdatrie/0.2.13-2/


### `dpkg` source package: `libde265=1.0.15-1`

Binary Packages:

- `libde265-0:amd64=1.0.15-1`

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
$ apt-get source -qq --print-uris libde265=1.0.15-1
'http://archive.ubuntu.com/ubuntu/pool/universe/libd/libde265/libde265_1.0.15-1.dsc' libde265_1.0.15-1.dsc 1872 SHA512:e64027068710037b63b4d460d5500f4e4b49aa06b79c9dbbe7a0213f5a9bd2c4c3c2173ae0a373e3cbbcf0c49b1f5b8b903cba1146cfd64db6deb28a4f0ec645
'http://archive.ubuntu.com/ubuntu/pool/universe/libd/libde265/libde265_1.0.15.orig.tar.gz' libde265_1.0.15.orig.tar.gz 846016 SHA512:375d8e781108247e0e8b4d7a036d20cc5d0670bdbf6ddb40a6d3dbf912fa776d2f001fb762301cb97e4d43be29eb415b0cdbfc6e07aa18b3f2346f7409c64fce
'http://archive.ubuntu.com/ubuntu/pool/universe/libd/libde265/libde265_1.0.15-1.debian.tar.xz' libde265_1.0.15-1.debian.tar.xz 136584 SHA512:8a19d4478aaeee2f282bc0f8e267da1c35305cf882549433f8ab4f668754b59b66b5f444d2f2fc7bd3fdd5ef1302b25bf89674417b4a0763a4fbff587c1b52be
```

### `dpkg` source package: `libdeflate=1.18-1`

Binary Packages:

- `libdeflate-dev:amd64=1.18-1`
- `libdeflate0:amd64=1.18-1`

Licenses: (parsed from: `/usr/share/doc/libdeflate-dev/copyright`, `/usr/share/doc/libdeflate0/copyright`)

- `Expat`

Source:

```console
$ apt-get source -qq --print-uris libdeflate=1.18-1
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libdeflate/libdeflate_1.18-1.dsc' libdeflate_1.18-1.dsc 2196 SHA512:824d28b3bafc78541768956048eeca66e5b35717508295ca18700b52a7293c4f2e3e0acea82de204e0261963ca2d88236706268397bec3b30978ab21a31aa7a0
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libdeflate/libdeflate_1.18.orig.tar.gz' libdeflate_1.18.orig.tar.gz 184924 SHA512:8a60fa5850f323389370f931579f85a094a35b3db334f2a2afa61bee39ecebc797e93c6fe5deb4178e19d83a1427533975dba6c05ce0b1db88b43c9268d09124
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libdeflate/libdeflate_1.18-1.debian.tar.xz' libdeflate_1.18-1.debian.tar.xz 4756 SHA512:aa72680eec89c930c824029cfba0195365df3d8df142be76d90180af081d068860fc3a1f5d8fe0e3696c5b317d6c41ccc7fe2b891af0c7c75eb4c79b55c15093
```

### `dpkg` source package: `libedit=3.1-20230828-1`

Binary Packages:

- `libedit2:amd64=3.1-20230828-1`

Licenses: (parsed from: `/usr/share/doc/libedit2/copyright`)

- `BSD-3-clause`

Source:

```console
$ apt-get source -qq --print-uris libedit=3.1-20230828-1
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libedit/libedit_3.1-20230828-1.dsc' libedit_3.1-20230828-1.dsc 2267 SHA512:0a532f6638c4b8b23f6fe028a448d30cddc28f958300f22e2e5bf5baa7e1b06be1b1822a09b5df037450a0625566364efeec2e90ae1cc2c930f32d3e63535d07
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libedit/libedit_3.1-20230828.orig.tar.gz' libedit_3.1-20230828.orig.tar.gz 534072 SHA512:c7232376ef1bc128ed79f950a5f1f207f874011218682d7e6186f76443927df5483b46c4daa8cf02e327079259aee1a56e2b791aa682491eb802d90ff8940cca
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libedit/libedit_3.1-20230828-1.debian.tar.xz' libedit_3.1-20230828-1.debian.tar.xz 16624 SHA512:a5cd1eee42e5f007cff0799ab257500610e9d2825ec5c9c936712499e3040afbdbc8f3f72b49deaa63c4ee0c80048c15d9977495c331e824d2b80b661669239e
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

### `dpkg` source package: `libevent=2.1.12-stable-9`

Binary Packages:

- `libevent-2.1-7:amd64=2.1.12-stable-9`
- `libevent-core-2.1-7:amd64=2.1.12-stable-9`
- `libevent-dev=2.1.12-stable-9`
- `libevent-extra-2.1-7:amd64=2.1.12-stable-9`
- `libevent-openssl-2.1-7:amd64=2.1.12-stable-9`
- `libevent-pthreads-2.1-7:amd64=2.1.12-stable-9`

Licenses: (parsed from: `/usr/share/doc/libevent-2.1-7/copyright`, `/usr/share/doc/libevent-core-2.1-7/copyright`, `/usr/share/doc/libevent-dev/copyright`, `/usr/share/doc/libevent-extra-2.1-7/copyright`, `/usr/share/doc/libevent-openssl-2.1-7/copyright`, `/usr/share/doc/libevent-pthreads-2.1-7/copyright`)

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
$ apt-get source -qq --print-uris libevent=2.1.12-stable-9
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libevent/libevent_2.1.12-stable-9.dsc' libevent_2.1.12-stable-9.dsc 2377 SHA512:d46ed308d53e99334d6d9fceef5f7e0a77b10b298ae7c256f766cb28c955ca6c3c1f79b0db4260fb5978f169d9e5bda0ac26da3a25a383b67d64d177accee822
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libevent/libevent_2.1.12-stable.orig.tar.gz' libevent_2.1.12-stable.orig.tar.gz 1100847 SHA512:88d8944cd75cbe78bc4e56a6741ca67c017a3686d5349100f1c74f8a68ac0b6410ce64dff160be4a4ba0696ee29540dfed59aaf3c9a02f0c164b00307fcfe84f
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libevent/libevent_2.1.12-stable-9.debian.tar.xz' libevent_2.1.12-stable-9.debian.tar.xz 17676 SHA512:f569372bb7766833da6045d54bbeae58c21363bfb39b257536ea6271044e98e36c437b937f972f4054cf519858073bb2ae0f32c868e8ed68fc61e0ed290f620e
```

### `dpkg` source package: `libexif=0.6.24-1build1`

Binary Packages:

- `libexif-dev:amd64=0.6.24-1build1`
- `libexif12:amd64=0.6.24-1build1`

Licenses: (parsed from: `/usr/share/doc/libexif-dev/copyright`, `/usr/share/doc/libexif12/copyright`)

- `BSD-2-Clause`
- `GPL-2`
- `GPL-2+`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `MIT`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris libexif=0.6.24-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libexif/libexif_0.6.24-1build1.dsc' libexif_0.6.24-1build1.dsc 2211 SHA512:a087ff32fa00c47f7d9d47df7ecc53065ead75588a8ea4ffb1eaae25678aae79a713fbd4bc64a16d6667eb7ce86d9fe648409ef8d27fb5d2b3104f222cba9be6
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libexif/libexif_0.6.24.orig.tar.gz' libexif_0.6.24.orig.tar.gz 1140079 SHA512:0b15a157c1030490bf1c4239487dffda90daad467ac6281db2a1b34a8419fca32b4b5265452e75cbcd2c9dc9a829643231cd3749e88251ed1b596756d1c5a9f4
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libexif/libexif_0.6.24-1build1.debian.tar.xz' libexif_0.6.24-1build1.debian.tar.xz 11824 SHA512:0ba09c166ed6cc4f55e4ecc12193531cd4ab93a0274906488f5d9dd6f86f39b115e746d430c367b689b508ddc39912f716f003667bdc81ccb963f92dc941ed5f
```

### `dpkg` source package: `libffi=3.4.4-2`

Binary Packages:

- `libffi-dev:amd64=3.4.4-2`
- `libffi8:amd64=3.4.4-2`

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
$ apt-get source -qq --print-uris libffi=3.4.4-2
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libffi/libffi_3.4.4-2.dsc' libffi_3.4.4-2.dsc 1951 SHA512:9b1b51d3625ff3e903a1f89f567341ac68d27d28d2ca522d93c53ef4b59f7c49236579f3d80b007a0d7867c67d2330bfe9ec13a8190afbc3ce5330110147848d
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libffi/libffi_3.4.4.orig.tar.gz' libffi_3.4.4.orig.tar.gz 1362394 SHA512:88680aeb0fa0dc0319e5cd2ba45b4b5a340bc9b4bcf20b1e0613b39cd898f177a3863aa94034d8e23a7f6f44d858a53dcd36d1bb8dee13b751ef814224061889
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libffi/libffi_3.4.4-2.debian.tar.xz' libffi_3.4.4-2.debian.tar.xz 14172 SHA512:a0e37092340e9727acaca19f9a78535840dc2de9ea7a5beecbeca54f4b2080c9a0874c34094dfe79e01d0f993e24d4ee59829d493f5c0405ad9ace2d9b2e4f6a
```

### `dpkg` source package: `libfido2=1.14.0-1`

Binary Packages:

- `libfido2-1:amd64=1.14.0-1`

Licenses: (parsed from: `/usr/share/doc/libfido2-1/copyright`)

- `BSD-2-clause`
- `ISC`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris libfido2=1.14.0-1
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libfido2/libfido2_1.14.0-1.dsc' libfido2_1.14.0-1.dsc 2588 SHA512:a5bfd433af33b04dd6efa93450f8da9e858bbd8b1d48cb9b475a1b964127b3b0c10510d91298ef5fd003b6a8513ce5de3aa41c3c3a4b7f771e6cf8c54291c2a9
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libfido2/libfido2_1.14.0.orig.tar.gz' libfido2_1.14.0.orig.tar.gz 660289 SHA512:83454b0db0cc8546f377d0dd59f95785fe6b73cf28e499a6182a6ece4b7bce17c3e750155262adf71f339ec0b3b6c3d3d64a07b01c8428b4b91de97ae768f0e6
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libfido2/libfido2_1.14.0.orig.tar.gz.asc' libfido2_1.14.0.orig.tar.gz.asc 228 SHA512:0f0116e1eb13d1fb18bddba6817e8f279a316fe0d74631fb350ba4c71a09cfdeffc12f4f5664e49575bfb1a334794e9f82c3151a02ab6d3fd27c21d9f5f60c20
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libfido2/libfido2_1.14.0-1.debian.tar.xz' libfido2_1.14.0-1.debian.tar.xz 52896 SHA512:429be04bca8e98c6e970f50b3c0e7131000842f3d4d474c18fa18425958b1a70a01b10721ffa8b42db120f43c26e0d37e2e1b4f6a48ca3f9a3fd2bdd3fcd3545
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

### `dpkg` source package: `libgpg-error=1.47-3build1`

Binary Packages:

- `libgpg-error0:amd64=1.47-3build1`

Licenses: (parsed from: `/usr/share/doc/libgpg-error0/copyright`)

- `BSD-3-clause`
- `GPL-3`
- `GPL-3+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `g10-permissive`

Source:

```console
$ apt-get source -qq --print-uris libgpg-error=1.47-3build1
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgpg-error/libgpg-error_1.47-3build1.dsc' libgpg-error_1.47-3build1.dsc 3028 SHA512:ddd0f19b6b755eb0b2a63b8f66321ca41f107a1177c0aaed6d4576671f34d349387be715aa51fcc29b6fa529b545c72b4c61eb305635ba88c41f6b49517b4b6b
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgpg-error/libgpg-error_1.47.orig.tar.bz2' libgpg-error_1.47.orig.tar.bz2 1020862 SHA512:bbb4b15dae75856ee5b1253568674b56ad155524ae29a075cb5b0a7e74c4af685131775c3ea2226fff2f84ef80855e77aa661645d002b490a795c7ae57b66a30
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgpg-error/libgpg-error_1.47.orig.tar.bz2.asc' libgpg-error_1.47.orig.tar.bz2.asc 228 SHA512:babf3a17429aa7ad5d952099ea8d21bb5c9ba1bc74ea46f3027e0293449c32365208a05e141fa0bf033491320679b0b212f49919452f3dc63cce5d7f355d7195
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgpg-error/libgpg-error_1.47-3build1.debian.tar.xz' libgpg-error_1.47-3build1.debian.tar.xz 18676 SHA512:4996e0fb7f2f35143fe6f043f346aab7c45dc3569bca5f086ebded3a2a713b85ffd87a39cbe8978af0d1f6b50eef3d73685d41646cf5dd7186a745d4e631512a
```

### `dpkg` source package: `libheif=1.17.4-1ubuntu1`

Binary Packages:

- `libheif-plugin-dav1d:amd64=1.17.4-1ubuntu1`
- `libheif-plugin-libde265:amd64=1.17.4-1ubuntu1`
- `libheif1:amd64=1.17.4-1ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libheif-plugin-dav1d/copyright`, `/usr/share/doc/libheif-plugin-libde265/copyright`, `/usr/share/doc/libheif1/copyright`)

- `BOOST-1.0`
- `BSD-3-clause`
- `BSD-4-clause`
- `GPL-3`
- `GPL-3+`
- `LGPL-3`
- `LGPL-3+`
- `MIT`

Source:

```console
$ apt-get source -qq --print-uris libheif=1.17.4-1ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/universe/libh/libheif/libheif_1.17.4-1ubuntu1.dsc' libheif_1.17.4-1ubuntu1.dsc 3437 SHA512:1705bc44764898c5667f3f5047674756a9f85e2ff038b46c34cbd67d35b95d9d5b1dfc68134955c4a44c2b97b630fd0bf61057d3fe11b987d0b703a0df5df759
'http://archive.ubuntu.com/ubuntu/pool/universe/libh/libheif/libheif_1.17.4.orig.tar.gz' libheif_1.17.4.orig.tar.gz 1432474 SHA512:c9f1e06b3273260aec69d72be8f1043d7ee1fee3ced5402c3e9e97f8177f41be1a98f348e418f9312e5f151a4d8ca61d61a0879b4d1b1fe64b544c71964da464
'http://archive.ubuntu.com/ubuntu/pool/universe/libh/libheif/libheif_1.17.4-1ubuntu1.debian.tar.xz' libheif_1.17.4-1ubuntu1.debian.tar.xz 10012 SHA512:4f7f1ce0cd5c5c64e08fb785cf9fe4d03adf5b24b215ede45b4b75373efc28b007964e866b94c0809d75aa9de61b7fa566d52fea7cc77e25702298221b38599f
```

### `dpkg` source package: `libice=2:1.0.10-1build2`

Binary Packages:

- `libice-dev:amd64=2:1.0.10-1build2`
- `libice6:amd64=2:1.0.10-1build2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libice=2:1.0.10-1build2
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libice/libice_1.0.10-1build2.dsc' libice_1.0.10-1build2.dsc 2181 SHA512:ab928645b15c679673d1adcc53f23b126f4ca90accbef677c15a1bb8bd428e642db5e45ef77b255d9b0351c2501dd01eafb9108875fff7c98f4543432d7e6fbf
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libice/libice_1.0.10.orig.tar.gz' libice_1.0.10.orig.tar.gz 481960 SHA512:2d4757f7325eb01180b5d7433cc350eb9606bd3afe82dabc8aa164feda75ef03a0624d74786e655c536c24a80d0ccb2f1e3ecbb04d3459b23f85455006ca8a91
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libice/libice_1.0.10-1build2.diff.gz' libice_1.0.10-1build2.diff.gz 11679 SHA512:dc850d9603ac04ffee3e2de1d2f9786520f6d9829f210649756fac705b6fe2797eda307d45283533342dd425317928fbb5f61d94bfe0fcadbc8f1c0c2cb02d6c
```

### `dpkg` source package: `libidn2=2.3.4-1build1`

Binary Packages:

- `libidn2-0:amd64=2.3.4-1build1`

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
$ apt-get source -qq --print-uris libidn2=2.3.4-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libidn2/libidn2_2.3.4-1build1.dsc' libidn2_2.3.4-1build1.dsc 2544 SHA512:0f74769d4eb24386f8410e5fdbe95c6bd40e26aab34174a4c34311e835fcd6043dcf17c0b7d918cefd212922c78ae08d7b5bfe506e02f545906b6eec54472af8
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libidn2/libidn2_2.3.4.orig.tar.gz' libidn2_2.3.4.orig.tar.gz 2083823 SHA512:a6e90ccef56cfd0b37e3333ab3594bb3cec7ca42a138ca8c4f4ce142da208fa792f6c78ca00c01001c2bc02831abcbaf1cf9bcc346a5290fd7b30708f5a462f3
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libidn2/libidn2_2.3.4.orig.tar.gz.asc' libidn2_2.3.4.orig.tar.gz.asc 228 SHA512:d2a575723326ae256a60e3edf7766af65434f716e11f963bb7ac29b6b2ff2872b41684a1bd1c6f3a3921e8a083512eff1faf2b0fc02513095c2bcf3563312fe0
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libidn2/libidn2_2.3.4-1build1.debian.tar.xz' libidn2_2.3.4-1build1.debian.tar.xz 16088 SHA512:ee67682f1696987dd41ab4ff25681a86d189826ee4a5dc0673b457a7d0200c48c409db0c374fecc7c17965193ae2adb0ab96ae80cbabde5aae4125cc3f6a6634
```

### `dpkg` source package: `libjpeg-turbo=2.1.5-2ubuntu1`

Binary Packages:

- `libjpeg-turbo8:amd64=2.1.5-2ubuntu1`
- `libjpeg-turbo8-dev:amd64=2.1.5-2ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libjpeg-turbo8/copyright`, `/usr/share/doc/libjpeg-turbo8-dev/copyright`)

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

### `dpkg` source package: `libksba=1.6.5-2`

Binary Packages:

- `libksba8:amd64=1.6.5-2`

Licenses: (parsed from: `/usr/share/doc/libksba8/copyright`)

- `FSFUL`
- `GPL-3`
- `LGPL-2.1-or-later`

Source:

```console
$ apt-get source -qq --print-uris libksba=1.6.5-2
'http://archive.ubuntu.com/ubuntu/pool/main/libk/libksba/libksba_1.6.5-2.dsc' libksba_1.6.5-2.dsc 2482 SHA512:3ca2ec300cd9ff43cb1abc232f5ba2ebba96249ff8413d75e5a805e3c1eb04c65ab49e8ff63f2294f2d8a110af7b3fa5bc303074aeb8c2d00848b5b0ec88c045
'http://archive.ubuntu.com/ubuntu/pool/main/libk/libksba/libksba_1.6.5.orig.tar.bz2' libksba_1.6.5.orig.tar.bz2 708400 SHA512:959312ac0bb2dabcdd22217266daccdf3938d62ff2936c767cade76888757ece1bb6fe79f2c679db03d1baf3919757265d0ded216fee8b8d235e94a70fcf05de
'http://archive.ubuntu.com/ubuntu/pool/main/libk/libksba/libksba_1.6.5.orig.tar.bz2.asc' libksba_1.6.5.orig.tar.bz2.asc 228 SHA512:77dbe3f068f02936e2772f7c67572cf23373d141d8f9e35f5a332cbd806ac9543ff797dc36c87177d37518914203717a1df46d9208b5e163e32d5f405fe84154
'http://archive.ubuntu.com/ubuntu/pool/main/libk/libksba/libksba_1.6.5-2.debian.tar.xz' libksba_1.6.5-2.debian.tar.xz 14732 SHA512:459625423c5ea0c98ef9146e621cbafd82aac2c0a463f344d87f34fd1fca55c67f35ddf16577e61c8bbe1d7c8f086b6a12d768eede984efba3b35865fbf9d43c
```

### `dpkg` source package: `liblqr=0.4.2-2.1`

Binary Packages:

- `liblqr-1-0:amd64=0.4.2-2.1`
- `liblqr-1-0-dev:amd64=0.4.2-2.1`

Licenses: (parsed from: `/usr/share/doc/liblqr-1-0/copyright`, `/usr/share/doc/liblqr-1-0-dev/copyright`)

- `GPL-3`
- `GPLv3`
- `LGPL-3`

Source:

```console
$ apt-get source -qq --print-uris liblqr=0.4.2-2.1
'http://archive.ubuntu.com/ubuntu/pool/universe/libl/liblqr/liblqr_0.4.2-2.1.dsc' liblqr_0.4.2-2.1.dsc 2095 SHA512:ef20fa2551ce6399f0ecc42301c2d0292d624f4fd9252fd901d58d67ac7325f128cd5209661fe456dda31e4efbb6b48a80415a1b34f815dd7511eeb24e924d36
'http://archive.ubuntu.com/ubuntu/pool/universe/libl/liblqr/liblqr_0.4.2.orig.tar.gz' liblqr_0.4.2.orig.tar.gz 439884 SHA512:acfa5868c41ea145092711e84d6c9eb62cb725b3d7531917b0d91b7d4af2a9912b18a96edc2594a826f09dabe0a0a82936ceea7d1f31301a23d558b1450d2547
'http://archive.ubuntu.com/ubuntu/pool/universe/libl/liblqr/liblqr_0.4.2-2.1.debian.tar.xz' liblqr_0.4.2-2.1.debian.tar.xz 5300 SHA512:ba8ade073057be2c5b065d92c0a119049cb67b382ebbf6c2b8c59b1aec52bd60fd6c313c0a2e8d83f39e9733477b615c7a646c47ca9dbbe3c8469ff86078c027
```

### `dpkg` source package: `libmaxminddb=1.8.0-1`

Binary Packages:

- `libmaxminddb-dev:amd64=1.8.0-1`
- `libmaxminddb0:amd64=1.8.0-1`

Licenses: (parsed from: `/usr/share/doc/libmaxminddb-dev/copyright`, `/usr/share/doc/libmaxminddb0/copyright`)

- `Apache-2.0`
- `BSD-2-clause`
- `BSD-3-clause`
- `BSD-4-clause`
- `CC-BY-SA-3.0`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris libmaxminddb=1.8.0-1
'http://archive.ubuntu.com/ubuntu/pool/main/libm/libmaxminddb/libmaxminddb_1.8.0-1.dsc' libmaxminddb_1.8.0-1.dsc 2322 SHA512:490830245589d6e0a94bb306c2838b9f05b3f34f6e98855145f5fc7b74b78aba23df16872250051c02559535650ff46ee5aa6e70ce825edfebc648a74bf311d4
'http://archive.ubuntu.com/ubuntu/pool/main/libm/libmaxminddb/libmaxminddb_1.8.0.orig.tar.gz' libmaxminddb_1.8.0.orig.tar.gz 243661 SHA512:0e0be75e2aa869b7a4173bf6389293e62010410d3cf8b3467e31e5a3ee40d548d04a890a00ee0a115ab82a6eb4ec00ca9e991344da9a18e10c291656766a9e71
'http://archive.ubuntu.com/ubuntu/pool/main/libm/libmaxminddb/libmaxminddb_1.8.0-1.debian.tar.xz' libmaxminddb_1.8.0-1.debian.tar.xz 12472 SHA512:bd9a3112e0e39330ee805f2e0a7b68010d2c0aab29c68d83cece9dfe3bcb3dac870c3ce6ebf0de5b0fa15d97a49858049089d28bd23a5459685089cf1fabed36
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

### `dpkg` source package: `libnsl=1.3.0-3`

Binary Packages:

- `libnsl-dev:amd64=1.3.0-3`
- `libnsl2:amd64=1.3.0-3`

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
$ apt-get source -qq --print-uris libnsl=1.3.0-3
'http://archive.ubuntu.com/ubuntu/pool/main/libn/libnsl/libnsl_1.3.0-3.dsc' libnsl_1.3.0-3.dsc 1955 SHA512:b512bc0fe8e37f81c50f2964b4768c39ba5f6e0aedea1fc8aadf66bd3d5545e5167f25f304a1cadb189f58eb8e78caaef30498263e9dcd515db4459195cc06c5
'http://archive.ubuntu.com/ubuntu/pool/main/libn/libnsl/libnsl_1.3.0.orig.tar.xz' libnsl_1.3.0.orig.tar.xz 321488 SHA512:a5a6c3ccb2d1e724c8c1f65e55dcd09383eb1ae019c55f4c09441eadf23ffbc2196cfad259805b0ac40ddf3a10af0da453e4d739d67d46829c64d0995dab4e55
'http://archive.ubuntu.com/ubuntu/pool/main/libn/libnsl/libnsl_1.3.0-3.debian.tar.xz' libnsl_1.3.0-3.debian.tar.xz 4748 SHA512:f2184805d849afd033bc26ff1267d9163b766dcfe8e6db39966476b8cd908a9b28cfc7d90fad95c13f9d6107cf35a584e67f13a51703eb6dd34dc3ec46279480
```

### `dpkg` source package: `libpng1.6=1.6.40-2`

Binary Packages:

- `libpng-dev:amd64=1.6.40-2`
- `libpng16-16:amd64=1.6.40-2`

Licenses: (parsed from: `/usr/share/doc/libpng-dev/copyright`, `/usr/share/doc/libpng16-16/copyright`)

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
$ apt-get source -qq --print-uris libpng1.6=1.6.40-2
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpng1.6/libpng1.6_1.6.40-2.dsc' libpng1.6_1.6.40-2.dsc 2241 SHA512:8763fd045317e1f25cc8f9f68fa8da0633d87a0185e475a7ca4f880a233fef5ee83a0909c2e09f5988c06fa66c81ffe22823f4c0a032a7bcc1f0841ecdfe36a3
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpng1.6/libpng1.6_1.6.40.orig.tar.gz' libpng1.6_1.6.40.orig.tar.gz 1520834 SHA512:5f36a145c7d41f1c417d5f4e03be0155dae3499d72e67170acaad92c1af418c0bb6bc508e9b4b27ef4206bf0074cbf74978bade3bff28bc291867b8f8c2a38cf
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpng1.6/libpng1.6_1.6.40-2.debian.tar.xz' libpng1.6_1.6.40-2.debian.tar.xz 31148 SHA512:dab2d1a0533e2d0bbbbe8eab19397eaf79b23c8a300ddf229b3a286b80819964508da52ba6e1d77a0538ad6e4e02c133b68ebb7591b319847fdf3c41852e7af8
```

### `dpkg` source package: `libpsl=0.21.2-1build1`

Binary Packages:

- `libpsl5:amd64=0.21.2-1build1`

Licenses: (parsed from: `/usr/share/doc/libpsl5/copyright`)

- `Chromium`
- `MIT`
- `gnulib`

Source:

```console
$ apt-get source -qq --print-uris libpsl=0.21.2-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpsl/libpsl_0.21.2-1build1.dsc' libpsl_0.21.2-1build1.dsc 2251 SHA512:b7c6fcdb9cae56eb33573b6d6e9aee0e7993d2b77172942c7e702854427c71fdf0a6532a8d94c8f0e0008c590797e9b2b1a83202944e5501e55089fee8f7d9d3
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpsl/libpsl_0.21.2.orig.tar.xz' libpsl_0.21.2.orig.tar.xz 1870352 SHA512:5308feee863b84705246ce303c093e0c9fecd948ab382fd7480e9ea1ca5f72de42fc2c8f70472a97603580a3fd1eb2b552b093d79756e9fe93effba9f25b6aa4
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpsl/libpsl_0.21.2-1build1.debian.tar.xz' libpsl_0.21.2-1build1.debian.tar.xz 12008 SHA512:e55e3d759af6607c90afbf1608d3063f752809d75be2c1624523982cef8fc059d843197b6cda3fde0344790f33f6900a7d4694bfbebc7bd3dbd9be18d083a9b0
```

### `dpkg` source package: `libpthread-stubs=0.4-1build2`

Binary Packages:

- `libpthread-stubs0-dev:amd64=0.4-1build2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libpthread-stubs=0.4-1build2
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpthread-stubs/libpthread-stubs_0.4-1build2.dsc' libpthread-stubs_0.4-1build2.dsc 2034 SHA512:57efab978e28d3efc132b1c807bce87a563ec444e5ac3f2499a4474da55bc97dbd48d28f3260c5f1d539bbdcbb4afef1bcd23ff3954255d7b5a0e092239c55f6
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpthread-stubs/libpthread-stubs_0.4.orig.tar.gz' libpthread-stubs_0.4.orig.tar.gz 71252 SHA512:5293c847f5d0c47a6956dd85b6630866f717e51e1e9c48fa10f70aa1e8268adc778eaf92504989c5df58c0dcde656f036248993b0ea5f79d4303012bfeff3c72
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpthread-stubs/libpthread-stubs_0.4-1build2.diff.gz' libpthread-stubs_0.4-1build2.diff.gz 2546 SHA512:a11200d9b898e9f9dab8a0a6d08567dfbe9177949d28e467bd9ed45a8c48d0ad881bd66d5fc9873d6876e9c78af8cb9454a0aef8ee38e0492c720518a7e90476
```

### `dpkg` source package: `librsvg=2.54.7+dfsg-2`

Binary Packages:

- `gir1.2-rsvg-2.0:amd64=2.54.7+dfsg-2`
- `librsvg2-2:amd64=2.54.7+dfsg-2`
- `librsvg2-common:amd64=2.54.7+dfsg-2`
- `librsvg2-dev:amd64=2.54.7+dfsg-2`

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
- `CC-BY-3.0`
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
$ apt-get source -qq --print-uris librsvg=2.54.7+dfsg-2
'http://archive.ubuntu.com/ubuntu/pool/main/libr/librsvg/librsvg_2.54.7%2bdfsg-2.dsc' librsvg_2.54.7+dfsg-2.dsc 2960 SHA512:c09212d07343db08c0bcb3b12ded10156b3368b40748d5a6cb46d1b45ea1caa713ade27e6b1cb25a137172feb5d183bbce223b2fa0f069234128c8573b739046
'http://archive.ubuntu.com/ubuntu/pool/main/libr/librsvg/librsvg_2.54.7%2bdfsg.orig.tar.xz' librsvg_2.54.7+dfsg.orig.tar.xz 14342756 SHA512:e891cd9e2fc93f9f19b91ca99b0c6fe310227620a37ec93a78a69004a0466f47a3d9c8e7f4733e3b49e7f7c788c10adac58958394cd7004593d27df9ea67f4e4
'http://archive.ubuntu.com/ubuntu/pool/main/libr/librsvg/librsvg_2.54.7%2bdfsg-2.debian.tar.xz' librsvg_2.54.7+dfsg-2.debian.tar.xz 35544 SHA512:af5c96a6ff0c3f13d311e9378c17797d2afd8a5125f31930d339835db3d6ba89d37b554503ad915ce5b4d51d1923ad566572fb6158932ab3ec0cf9b8242de2ee
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

### `dpkg` source package: `libselinux=3.5-1build2`

Binary Packages:

- `libselinux1:amd64=3.5-1build2`
- `libselinux1-dev:amd64=3.5-1build2`

Licenses: (parsed from: `/usr/share/doc/libselinux1/copyright`, `/usr/share/doc/libselinux1-dev/copyright`)

- `GPL-2`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris libselinux=3.5-1build2
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libselinux/libselinux_3.5-1build2.dsc' libselinux_3.5-1build2.dsc 3007 SHA512:ac8e7137344bcf46bbb062ef0f07860c74481e6b4d635be1be40bafc7e0e84554a5e30f85b87f03bf90751ff2753fa3a2e5e4320ab64919df39bb27499c559da
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libselinux/libselinux_3.5.orig.tar.gz' libselinux_3.5.orig.tar.gz 211453 SHA512:4e13261a5821018a5f3cdce676f180bb62e5bc225981ca8a498ece0d1c88d9ba8eaa0ce4099dd0849309a8a7c5a9a0953df841a9922f2c284e5a109e5d937ba7
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libselinux/libselinux_3.5.orig.tar.gz.asc' libselinux_3.5.orig.tar.gz.asc 981 SHA512:ba486d29c92801a02f75213ef5bcc4a0c4a87afe9dfa797aa9bb495ded40f21e37b22d6ea114c0e480d669b090d1116e8b9cac9fa9ea29678d3647bc58d8bb29
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libselinux/libselinux_3.5-1build2.debian.tar.xz' libselinux_3.5-1build2.debian.tar.xz 35960 SHA512:87fe257d83f8de42662016790a0fccdfe984344b2d2c0a78895295d33e1b667e4270c5d2402609e95fdac30e596715032b4754d78b661a19842ea03690ac053f
```

### `dpkg` source package: `libsemanage=3.5-1build1`

Binary Packages:

- `libsemanage-common=3.5-1build1`
- `libsemanage2:amd64=3.5-1build1`

Licenses: (parsed from: `/usr/share/doc/libsemanage-common/copyright`, `/usr/share/doc/libsemanage2/copyright`)

- `GPL-2`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris libsemanage=3.5-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsemanage/libsemanage_3.5-1build1.dsc' libsemanage_3.5-1build1.dsc 3014 SHA512:aa134e2bd2dfa58d11966d7df7ca94738f2095d077dbf329c4c2fda2a0969cf923f64e9e81c8e1f25833bcb5fcf5f3ab8de6930332c9071398edb116d87f8d23
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsemanage/libsemanage_3.5.orig.tar.gz' libsemanage_3.5.orig.tar.gz 185060 SHA512:959fbd0d6bc6849da6caa13dc41c3f8818cbbd29f04b5d2ac7246c4b395b4f370f113a04cc9cfcb52be2afebfa636013ac4ad4011384c58c7ce066a45cae2751
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsemanage/libsemanage_3.5.orig.tar.gz.asc' libsemanage_3.5.orig.tar.gz.asc 981 SHA512:c0a5ddb69c32ddefa26b3d1ec676bcc373e959dd8b4a7fcf6e1f74a3ca8e9af22af851ca66d3c43a704215ff79d27244e33d23038ef2f52ccc321aeb5f0c2790
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsemanage/libsemanage_3.5-1build1.debian.tar.xz' libsemanage_3.5-1build1.debian.tar.xz 30032 SHA512:338ad06136b29a955ec5492d10fa620dd8745371112ba4376d757d38ba07c08c07901ceade44d7324306d409cc14715cb6fca67292f0e02baee07322a999c721
```

### `dpkg` source package: `libsepol=3.5-2`

Binary Packages:

- `libsepol-dev:amd64=3.5-2`
- `libsepol2:amd64=3.5-2`

Licenses: (parsed from: `/usr/share/doc/libsepol-dev/copyright`, `/usr/share/doc/libsepol2/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris libsepol=3.5-2
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsepol/libsepol_3.5-2.dsc' libsepol_3.5-2.dsc 2005 SHA512:b76be86626690e04932a2824aed67eb8194d710ccaf00bf59defe92a09ce88d12b267dc189188be736f0442b0bce4952ee58db7a3542b3adc14c21231305bb10
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsepol/libsepol_3.5.orig.tar.gz' libsepol_3.5.orig.tar.gz 497522 SHA512:66f45a9f4951589855961955db686b006b4c0cddead6ac49ad238a0e4a34775905bd10fb8cf0c0ff2ab64f9b7d8366b97fcd5b19c382dec39971a2835cc765c8
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsepol/libsepol_3.5.orig.tar.gz.asc' libsepol_3.5.orig.tar.gz.asc 981 SHA512:5aa46c3a7a5d7fa0d4376766b9444cdea1b14f3ec61725950a24fcb5ba2caae271a415c613807d06e4d9b04b40cda1525c12c442eed8a7e60fb5e5beacdaba3b
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsepol/libsepol_3.5-2.debian.tar.xz' libsepol_3.5-2.debian.tar.xz 27596 SHA512:87ab5579d0e742fd52509cab880c5e1362830ab6c6581a8ffbd39c7e21b0997b3a4d76357b7bbad7d736ea78b7028f431d10e46a35f7f93fbb8ca6f088ac37ee
```

### `dpkg` source package: `libsm=2:1.2.3-1build2`

Binary Packages:

- `libsm-dev:amd64=2:1.2.3-1build2`
- `libsm6:amd64=2:1.2.3-1build2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libsm=2:1.2.3-1build2
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsm/libsm_1.2.3-1build2.dsc' libsm_1.2.3-1build2.dsc 2170 SHA512:4dc5d9445614801154fb411ae2089c80c55adaea90a9d78a958724d70fc8ea8d36c9a898a478f18a9669f3448d9d9a948c632f2a4869287d1e1f88403e304096
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsm/libsm_1.2.3.orig.tar.gz' libsm_1.2.3.orig.tar.gz 445362 SHA512:03b77d86b33cdb3df4f9d65131a0025182f3cb0c17b33a90d236e8563b3011d225b9d006186302d07850edafa5b899aec6a086b8d437d357cd69fedd5f22d94b
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsm/libsm_1.2.3-1build2.diff.gz' libsm_1.2.3-1build2.diff.gz 9062 SHA512:c5ddeb48fe7c846b31382a5da42a2970ae12995afb322c6291977b7ffd2251d4d9e9dc163ecb008902ae8ee3c3a44526115bddc92b402c8f4a9ea0f29f1cb037
```

### `dpkg` source package: `libssh=0.10.6-2`

Binary Packages:

- `libssh-4:amd64=0.10.6-2`

Licenses: (parsed from: `/usr/share/doc/libssh-4/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `LGPL-2.1`
- `LGPL-2.1+~OpenSSL`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris libssh=0.10.6-2
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libssh/libssh_0.10.6-2.dsc' libssh_0.10.6-2.dsc 2742 SHA512:1e8e270da06c351fc4af1864efa5822a7e685208675517eb103d22a9f8e7e1c471978719505c926e96f357b1dbaaba91c4ad21bb3baa154cf5c3f93fb4cdf03b
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libssh/libssh_0.10.6.orig.tar.xz' libssh_0.10.6.orig.tar.xz 561036 SHA512:40c62d63c44e882999b71552c237d73fc7364313bd00b15a211a34aeff1b73693da441d2c8d4e40108d00fb7480ec7c5b6d472f9c0784b2359a179632ab0d6c1
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libssh/libssh_0.10.6.orig.tar.xz.asc' libssh_0.10.6.orig.tar.xz.asc 833 SHA512:214d7920bebc80a8e6838c64ed06e070709a96fabfb4fff657b55f9588bc0e1612887fe887d23de73ad3540f3bb85288e62eb6a11ccd4bc80afbd44d34ba70d4
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libssh/libssh_0.10.6-2.debian.tar.xz' libssh_0.10.6-2.debian.tar.xz 30464 SHA512:1ebb576d3352ad980f1fe400596b0535eab1314176e2b296fa2a3687407f4dbf1b7d1de0a667437fc208c243a11b2091838deb720a0b51b8f47d490582ddd5b6
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

### `dpkg` source package: `libthai=0.1.29-1build1`

Binary Packages:

- `libthai-data=0.1.29-1build1`
- `libthai0:amd64=0.1.29-1build1`

Licenses: (parsed from: `/usr/share/doc/libthai-data/copyright`, `/usr/share/doc/libthai0/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libtirpc=1.3.4+ds-1`

Binary Packages:

- `libtirpc-common=1.3.4+ds-1`
- `libtirpc-dev:amd64=1.3.4+ds-1`
- `libtirpc3:amd64=1.3.4+ds-1`

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
$ apt-get source -qq --print-uris libtirpc=1.3.4+ds-1
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtirpc/libtirpc_1.3.4%2bds-1.dsc' libtirpc_1.3.4+ds-1.dsc 2129 SHA512:2e21fcf13e32aafbf287c436ccfd9e9c03cbfccf8a13359887ad4f0499f437693fac1ffe15b471a9c0a4a0bb6fed9071c785ee825c86d919b07c68871c21dc4c
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtirpc/libtirpc_1.3.4%2bds.orig.tar.gz' libtirpc_1.3.4+ds.orig.tar.gz 700735 SHA512:125e26247f1ffbf5ce310657515eb84be03b69867e5efbacac6768f406470f9124b66124639daccd9af0c8220a8099cb5dbbe0a370315c61069aa73a5b53815d
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtirpc/libtirpc_1.3.4%2bds-1.debian.tar.xz' libtirpc_1.3.4+ds-1.debian.tar.xz 11436 SHA512:1f386ce39bbba9d76399581329460ec871364e33550b476fcfe71b341b8dbe644d6b0ce6e75c31b26b5393b4299869fd27cbcd68e3d5dbdddceebd68fbb6071e
```

### `dpkg` source package: `libtool=2.4.7-7`

Binary Packages:

- `libltdl-dev:amd64=2.4.7-7`
- `libltdl7:amd64=2.4.7-7`
- `libtool=2.4.7-7`

Licenses: (parsed from: `/usr/share/doc/libltdl-dev/copyright`, `/usr/share/doc/libltdl7/copyright`, `/usr/share/doc/libtool/copyright`)

- `GFDL-1.3`
- `GFDL-NIV-1.3+`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris libtool=2.4.7-7
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtool/libtool_2.4.7-7.dsc' libtool_2.4.7-7.dsc 2257 SHA512:ea8556ba972137c14a410c2744253cd594acd7511aeb98d4d48aa22fde5bad8c27a1bf23fa21f2bc6b4c45acdaa8003ce36b0b082eda9ecf066690579ab09f46
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtool/libtool_2.4.7.orig.tar.xz' libtool_2.4.7.orig.tar.xz 1026028 SHA512:424f4549aa713917859dc31e62153934c67b8b9d5718452f0e50bb8f6ef48ae6274cc4d4ddd905b15858d19c60daf8c194471e6ed0c8f76e7d55e7ef932a8d3a
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtool/libtool_2.4.7-7.debian.tar.xz' libtool_2.4.7-7.debian.tar.xz 40916 SHA512:f6ce4090de656b0ec1d264443bfdcdf4bcc03db92d539d05be80b8b026614d0dd2f0766276fa5be6de428cb7d51d374ced693900edaf3aa4d0354ed5c253c360
```

### `dpkg` source package: `libunistring=1.1-2`

Binary Packages:

- `libunistring5:amd64=1.1-2`

Licenses: (parsed from: `/usr/share/doc/libunistring5/copyright`)

- `FreeSoftware`
- `GFDL-1.2`
- `GFDL-NIV-1.2+`
- `GPL-2`
- `GPL-2+`
- `GPL-2+ with distribution exception`
- `GPL-2+ with distribution exception, Expat`
- `GPL-3`
- `GPL-3+`
- `LGPL-3`
- `LGPL-3+`
- `X11`

Source:

```console
$ apt-get source -qq --print-uris libunistring=1.1-2
'http://archive.ubuntu.com/ubuntu/pool/main/libu/libunistring/libunistring_1.1-2.dsc' libunistring_1.1-2.dsc 2031 SHA512:89a88cb017f67e0539028c9a99a7530bd407d3776c2535d792ed9f38c007bff056fa9702ee280e38cb4ab26218b899f1d03de3e7150fef29e38b82e8d0e80336
'http://archive.ubuntu.com/ubuntu/pool/main/libu/libunistring/libunistring_1.1.orig.tar.xz' libunistring_1.1.orig.tar.xz 2397676 SHA512:01a4267bbd301ea5c389b17ee918ae5b7d645da8b2c6c6f0f004ff2dead9f8e50cda2c6047358890a5fceadc8820ffc5154879193b9bb8970f3fb1fea1f411d6
'http://archive.ubuntu.com/ubuntu/pool/main/libu/libunistring/libunistring_1.1.orig.tar.xz.asc' libunistring_1.1.orig.tar.xz.asc 833 SHA512:f94912a52df8d7863de271315c8b5a7e1e0ab7aabb66273fcdb81c48aa0b23360b80fdb1df9f768aede47dd5a92a280868db41147139dfabecbc82511715db4d
'http://archive.ubuntu.com/ubuntu/pool/main/libu/libunistring/libunistring_1.1-2.debian.tar.xz' libunistring_1.1-2.debian.tar.xz 14008 SHA512:2ce7e2e2b2fc08f3f6a848ddad65e6b7f17735c4dde7d1af491c289ccc58c3d904702a9468bce5b45c1420fda1895941bd2c04a5aa65f615946f2ceb72637e6f
```

### `dpkg` source package: `libwebp=1.3.2-0.3`

Binary Packages:

- `libsharpyuv-dev:amd64=1.3.2-0.3`
- `libsharpyuv0:amd64=1.3.2-0.3`
- `libwebp-dev:amd64=1.3.2-0.3`
- `libwebp7:amd64=1.3.2-0.3`
- `libwebpdecoder3:amd64=1.3.2-0.3`
- `libwebpdemux2:amd64=1.3.2-0.3`
- `libwebpmux3:amd64=1.3.2-0.3`

Licenses: (parsed from: `/usr/share/doc/libsharpyuv-dev/copyright`, `/usr/share/doc/libsharpyuv0/copyright`, `/usr/share/doc/libwebp-dev/copyright`, `/usr/share/doc/libwebp7/copyright`, `/usr/share/doc/libwebpdecoder3/copyright`, `/usr/share/doc/libwebpdemux2/copyright`, `/usr/share/doc/libwebpmux3/copyright`)

- `Apache-2.0`
- `BSD-3-Clause`

Source:

```console
$ apt-get source -qq --print-uris libwebp=1.3.2-0.3
'http://archive.ubuntu.com/ubuntu/pool/main/libw/libwebp/libwebp_1.3.2-0.3.dsc' libwebp_1.3.2-0.3.dsc 2461 SHA512:ed22079efcc701953af3667b561df91d5e01c80d3e2c24a2710e95821343d0d0dbfbd2de9830ace001bd2a8d78519025816c39e89da12291d9ca44fe8605d9b2
'http://archive.ubuntu.com/ubuntu/pool/main/libw/libwebp/libwebp_1.3.2.orig.tar.gz' libwebp_1.3.2.orig.tar.gz 4162949 SHA512:2b624d2ecfbff6b4db2719e38f146722638ae262acd96327073a04451dd05fb27ef70c5681187821d251df728a6be7e89209c861c561a13bfb786495a830bc20
'http://archive.ubuntu.com/ubuntu/pool/main/libw/libwebp/libwebp_1.3.2-0.3.debian.tar.xz' libwebp_1.3.2-0.3.debian.tar.xz 15524 SHA512:5571dba6213387fe7e2beb62e162e30a259f6b048fabe2fc722e37dd275792e2ed91ab9b088e0e66de1cba0b5d3d4ab642a025aa8bd12a7d2cdd753ab106275d
```

### `dpkg` source package: `libwmf=0.2.13-1.1`

Binary Packages:

- `libwmf-0.2-7:amd64=0.2.13-1.1`
- `libwmf-dev=0.2.13-1.1`
- `libwmflite-0.2-7:amd64=0.2.13-1.1`

Licenses: (parsed from: `/usr/share/doc/libwmf-0.2-7/copyright`, `/usr/share/doc/libwmf-dev/copyright`, `/usr/share/doc/libwmflite-0.2-7/copyright`)

- `AGPL-3 with Font exception`
- `GD`
- `ISC`
- `LGPL-2`
- `LGPL-2+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris libwmf=0.2.13-1.1
'http://archive.ubuntu.com/ubuntu/pool/main/libw/libwmf/libwmf_0.2.13-1.1.dsc' libwmf_0.2.13-1.1.dsc 2345 SHA512:2e50190bbdc38f95e5a5b3da87889164b2d837a72a2b5cb97bf1db4ba08a762c98b8d2d828398401ee353897dfcf2b3e4a0ae95d9513d615bb15a72d713f9251
'http://archive.ubuntu.com/ubuntu/pool/main/libw/libwmf/libwmf_0.2.13.orig.tar.gz' libwmf_0.2.13.orig.tar.gz 3044235 SHA512:f45a936c9bc98fc1a5f2b0808b497119e4dcd3c132615fdddb7583e5719c7d1d7f85c16ebf313cad453e5b7ae3508bf6b80c4ed2b42322b7dec295d8f4eb86ce
'http://archive.ubuntu.com/ubuntu/pool/main/libw/libwmf/libwmf_0.2.13-1.1.debian.tar.xz' libwmf_0.2.13-1.1.debian.tar.xz 25784 SHA512:e73216fad961b5ce6f1451049dc476e3aa8632ca79d8984767fc53156cbcab4a0db61e52449afce8f266a7383ab8fa9920d85c7dd82bb505163d88f48288e573
```

### `dpkg` source package: `libx11=2:1.8.7-1`

Binary Packages:

- `libx11-6:amd64=2:1.8.7-1`
- `libx11-data=2:1.8.7-1`
- `libx11-dev:amd64=2:1.8.7-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libx11=2:1.8.7-1
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libx11/libx11_1.8.7-1.dsc' libx11_1.8.7-1.dsc 2480 SHA512:cb0627df8958b94a3cd7ec9e4395449faa818484106eed88824fed6e9cdf158c62fdfd9f0b68291133db327836ab25545421cf96e9dde6dec19db0987e2e55dd
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libx11/libx11_1.8.7.orig.tar.gz' libx11_1.8.7.orig.tar.gz 3185363 SHA512:67575740356aecc6a7a4898e92ff1007aa6a44ff506d80fe577c1bdc3d64a900edf545cf3e082e9f17c25f4afe28e724145d5e82ae428bdc44348d368d9451a6
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libx11/libx11_1.8.7.orig.tar.gz.asc' libx11_1.8.7.orig.tar.gz.asc 833 SHA512:92c410ca14412092680bd511f9536fcf1eb1f32632c33fb833246f8c90bb6dcb8045b9e12cbffa0b6093bf91fe8897ba76d2abb4303a343b4b7deb3b586098b4
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libx11/libx11_1.8.7-1.diff.gz' libx11_1.8.7-1.diff.gz 74344 SHA512:6cff79cc33e9def5846830754c75ebc021afefb322abe105292ab2db77ffeacdeb64539d5bd84584dc77e308c43b91c48b7316fa54678e6a5d0ac5217a23133f
```

### `dpkg` source package: `libxau=1:1.0.9-1build5`

Binary Packages:

- `libxau-dev:amd64=1:1.0.9-1build5`
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

- `libxcb-render0:amd64=1.15-1`
- `libxcb-render0-dev:amd64=1.15-1`
- `libxcb-shm0:amd64=1.15-1`
- `libxcb-shm0-dev:amd64=1.15-1`
- `libxcb1:amd64=1.15-1`
- `libxcb1-dev:amd64=1.15-1`

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

- `libxdmcp-dev:amd64=1:1.1.3-0ubuntu5`
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

- `libxext-dev:amd64=2:1.3.4-1build1`
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

### `dpkg` source package: `libxml2=2.9.14+dfsg-1.3build3`

Binary Packages:

- `libxml2:amd64=2.9.14+dfsg-1.3build3`
- `libxml2-dev:amd64=2.9.14+dfsg-1.3build3`

Licenses: (parsed from: `/usr/share/doc/libxml2/copyright`, `/usr/share/doc/libxml2-dev/copyright`)

- `ISC`
- `MIT-1`

Source:

```console
$ apt-get source -qq --print-uris libxml2=2.9.14+dfsg-1.3build3
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxml2/libxml2_2.9.14%2bdfsg-1.3build3.dsc' libxml2_2.9.14+dfsg-1.3build3.dsc 2947 SHA512:08fb7f927b5a261251c537bee3a85c498af4fc7627c6405c3ee9d86589fe3a7c31ae75d06d458d59b7d79e3aa52996d37b40d367e2b7d97807f7b126cf4d743a
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxml2/libxml2_2.9.14%2bdfsg.orig.tar.xz' libxml2_2.9.14+dfsg.orig.tar.xz 2351200 SHA512:1eacc9ac2cd8d38b8466659b3b9d84b94eb765c8f869d6cca0da131060bbc35c2b31c6148d59690547871a20cea339eac8fbe953b4fe37cf0900862f3fd9621b
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxml2/libxml2_2.9.14%2bdfsg-1.3build3.debian.tar.xz' libxml2_2.9.14+dfsg-1.3build3.debian.tar.xz 35208 SHA512:4b37cf4e86cbb6776ee901649257ee36da5986d7aadcbd283cb6c6efb6efdd76d7762a52df5533f18b980c24cc76ff765778c51393b6e21107de73f3621d15c4
```

### `dpkg` source package: `libxrender=1:0.9.10-1.1`

Binary Packages:

- `libxrender-dev:amd64=1:0.9.10-1.1`
- `libxrender1:amd64=1:0.9.10-1.1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxrender=1:0.9.10-1.1
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxrender/libxrender_0.9.10-1.1.dsc' libxrender_0.9.10-1.1.dsc 2072 SHA512:0cbb2a8642aad32961e86c36ae69b38b8a78f5894991c4efd54de89864ce3ef1821a6019c365e5e1af23a6c50727fb18045caa2dc261f677b3366ffe05cb0123
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxrender/libxrender_0.9.10.orig.tar.gz' libxrender_0.9.10.orig.tar.gz 373717 SHA512:7768e62b500f468460f88f27bc1130170b204b478573d9e4406867e557b5638b7c1e21d88d51f9e774ce2344780a384e3c3be51421275d2ee880f9a978a3a232
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxrender/libxrender_0.9.10-1.1.diff.gz' libxrender_0.9.10-1.1.diff.gz 15201 SHA512:079ceac53ac1cfa5ab7ba14356af16e581eb64a1a140861b55301a6ec9ecdd79e26b6719e8aabd90cd819a92517d80f25933f6b83f85eb2e1694bcb7540e9b78
```

### `dpkg` source package: `libxslt=1.1.35-1`

Binary Packages:

- `libxslt1-dev:amd64=1.1.35-1`
- `libxslt1.1:amd64=1.1.35-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxslt=1.1.35-1
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxslt/libxslt_1.1.35-1.dsc' libxslt_1.1.35-1.dsc 2155 SHA512:4bd19486b3a8bc9c4ef5b3a14ce9e3b4440d9c12b667ead50aab450841474fb24d60abc427373e5ffedcbcc4515695896a34c641dfebe52ab74cdd58a7cfe52b
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxslt/libxslt_1.1.35.orig.tar.xz' libxslt_1.1.35.orig.tar.xz 1827548 SHA512:9dd4a699235f50ae9b75b25137e387471635b4b2da0a4e4380879cd49f1513470fcfbfd775269b066eac513a1ffa6860c77ec42747168e2348248f09f60c8c96
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxslt/libxslt_1.1.35-1.debian.tar.xz' libxslt_1.1.35-1.debian.tar.xz 21420 SHA512:f3b04999fa4f9e2924406e110fafcebb8de63f6964409f8bf4efd43066e872042a81e0d7ae706819b35b01e99455c537cf9da725b7ae6e78d63f8fee07c60f52
```

### `dpkg` source package: `libxt=1:1.2.1-1.1`

Binary Packages:

- `libxt-dev:amd64=1:1.2.1-1.1`
- `libxt6:amd64=1:1.2.1-1.1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxt=1:1.2.1-1.1
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxt/libxt_1.2.1-1.1.dsc' libxt_1.2.1-1.1.dsc 2170 SHA512:b7d307ff8b4b80e2075b2d4d292543eb52206a2e9e6e38395c193e12ca7fec4262e11025472bacdd9c2de500b37283747a125760093b013c6993fd597bbe9749
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxt/libxt_1.2.1.orig.tar.gz' libxt_1.2.1.orig.tar.gz 1024473 SHA512:73c2fd8a6590ab5ee93cf646e4f41fb71d424961ecbf9bc13c68abdf539c63ab0c59a4d3b22195ba21859523f4cf0e937648424532794a1350a5891061096503
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxt/libxt_1.2.1.orig.tar.gz.asc' libxt_1.2.1.orig.tar.gz.asc 358 SHA512:135e01b8a79beac9530087dee1a5458c359b4f1ae8346e2502f72f4fc24be400477fda90944315c585e3416e80cb74d1a140d5dfec81e854a4996199a8b221dc
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxt/libxt_1.2.1-1.1.diff.gz' libxt_1.2.1-1.1.diff.gz 45585 SHA512:a88bd795883c88dc1c71a23b3a321e985f079819129e9a7e6fe37e95ca0f9b9650b18a9897bf7d0f894fc821f014dc74335296b58190ddfd69ffc74c291d6baa
```

### `dpkg` source package: `libyaml=0.2.5-1`

Binary Packages:

- `libyaml-0-2:amd64=0.2.5-1`
- `libyaml-dev:amd64=0.2.5-1`

Licenses: (parsed from: `/usr/share/doc/libyaml-0-2/copyright`, `/usr/share/doc/libyaml-dev/copyright`)

- `Expat`
- `permissive`

Source:

```console
$ apt-get source -qq --print-uris libyaml=0.2.5-1
'http://archive.ubuntu.com/ubuntu/pool/main/liby/libyaml/libyaml_0.2.5-1.dsc' libyaml_0.2.5-1.dsc 2071 SHA512:f98d96ba0e2555436999dfb6056a27008df5abd23804c25e9b67d39080f4cd910839a507af5cfcc2c3b1df147ee3035846ba1c1df8aa9abfd4c0ed2acafaab7d
'http://archive.ubuntu.com/ubuntu/pool/main/liby/libyaml/libyaml_0.2.5.orig.tar.gz' libyaml_0.2.5.orig.tar.gz 85055 SHA512:a0f01e3fc616b65b18a4aa17692ee8ea1a84dc6387d1cf02ac7ef7ab7f46b9744c2aac0a047ff69d6c2da1d2a2d7b355c877da0db57e34d95cd4f37213ab6e7e
'http://archive.ubuntu.com/ubuntu/pool/main/liby/libyaml/libyaml_0.2.5-1.debian.tar.xz' libyaml_0.2.5-1.debian.tar.xz 5324 SHA512:32fb54badad393df364cc3967856fac5dcc9820966c61bf9885a1f359598ab541626bd081957b4c92fb4204050d703c9dd0f09c903c3eb6d385cefe322e88e82
```

### `dpkg` source package: `libzstd=1.5.5+dfsg2-2`

Binary Packages:

- `libzstd-dev:amd64=1.5.5+dfsg2-2`
- `libzstd1:amd64=1.5.5+dfsg2-2`

Licenses: (parsed from: `/usr/share/doc/libzstd-dev/copyright`, `/usr/share/doc/libzstd1/copyright`)

- `BSD-3-clause`
- `Expat`
- `GPL-2`
- `zlib`

Source:

```console
$ apt-get source -qq --print-uris libzstd=1.5.5+dfsg2-2
'http://archive.ubuntu.com/ubuntu/pool/main/libz/libzstd/libzstd_1.5.5%2bdfsg2-2.dsc' libzstd_1.5.5+dfsg2-2.dsc 2375 SHA512:b4a49142abf47c7901e3859e9af1a2fa35350ddf03594eed4a0c5f8e656f684b93bc2acdf239fd7af6a6702e5c0671fd732e4b5abc3944fe4f7411237bd6eda4
'http://archive.ubuntu.com/ubuntu/pool/main/libz/libzstd/libzstd_1.5.5%2bdfsg2.orig.tar.xz' libzstd_1.5.5+dfsg2.orig.tar.xz 1784164 SHA512:0b24cf71636b36ae17f617f0a4a2e1253ba6a7bfcd8b6f4717cc59310e92d23bde0945f885fa80622d84961b85fa6ba74e3436ab1badc687e8a13ac428a71b8d
'http://archive.ubuntu.com/ubuntu/pool/main/libz/libzstd/libzstd_1.5.5%2bdfsg2-2.debian.tar.xz' libzstd_1.5.5+dfsg2-2.debian.tar.xz 21068 SHA512:97f1075658c370cc2b5b80b5e0fd437981740e4718736c1fea5229c237e15854ed701791d5e36e9e5c5435c54a9593af4ffb55b7238128c04bbfca0c0dbf2da3
```

### `dpkg` source package: `linux=6.6.0-14.14`

Binary Packages:

- `linux-libc-dev:amd64=6.6.0-14.14`

Licenses: (parsed from: `/usr/share/doc/linux-libc-dev/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris linux=6.6.0-14.14
'http://archive.ubuntu.com/ubuntu/pool/main/l/linux/linux_6.6.0-14.14.dsc' linux_6.6.0-14.14.dsc 9105 SHA512:107ceb41f2449dcafd08d49ab22dea96be38fd02d0d62a53c3faa941f0c02bbadbb89671917477404c96eca7775c21a143827d5958b091f9ff0ec5005419ee9a
'http://archive.ubuntu.com/ubuntu/pool/main/l/linux/linux_6.6.0.orig.tar.gz' linux_6.6.0.orig.tar.gz 224912857 SHA512:685a90e45f39f275a39821ee08d1a9efb4cb223370276c43de6388c08ae3ac54f95a087a76fec04dc3f1b5e4a94f7d2e6e2b01b08c0a4983f8bb08ba5e2d4c8c
'http://archive.ubuntu.com/ubuntu/pool/main/l/linux/linux_6.6.0-14.14.diff.gz' linux_6.6.0-14.14.diff.gz 4116102 SHA512:ec461b27bce3f74d6dfeb0bcb984c740c03c23538ed2be0384c603366482689fd7b7abe7b067c939b801b5ce792c931213eb206e4bf716670027ecb3244678bc
```

### `dpkg` source package: `lto-disabled-list=44`

Binary Packages:

- `lto-disabled-list=44`

Licenses: (parsed from: `/usr/share/doc/lto-disabled-list/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris lto-disabled-list=44
'http://archive.ubuntu.com/ubuntu/pool/main/l/lto-disabled-list/lto-disabled-list_44.dsc' lto-disabled-list_44.dsc 1435 SHA512:b48621697b6fcd2b2b2e680e31d85b17263ee325252e44f3202a6af0b3cf617904fb9d9c1d913395f250858517d45568b9288340584ddf2af21ca559c55d6cdc
'http://archive.ubuntu.com/ubuntu/pool/main/l/lto-disabled-list/lto-disabled-list_44.tar.xz' lto-disabled-list_44.tar.xz 13368 SHA512:77e965266c4513376bafaafa7fe5c24c2b5064bff6c14255b025721a71d611cd1b8ad6458da2d287f8da09ef8b79da08a0c3c44356c458ad930dc293a9cf4c9d
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

### `dpkg` source package: `lzo2=2.10-2build3`

Binary Packages:

- `liblzo2-2:amd64=2.10-2build3`

Licenses: (parsed from: `/usr/share/doc/liblzo2-2/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris lzo2=2.10-2build3
'http://archive.ubuntu.com/ubuntu/pool/main/l/lzo2/lzo2_2.10-2build3.dsc' lzo2_2.10-2build3.dsc 2058 SHA512:37c777797173360a4f835428066b3d9707e428452e7b6ec8b662828020f712123d0c39f1d534f2c9becc42cb91765bee7d0f1d4b7c61762f2af5cc1cbedd1bb9
'http://archive.ubuntu.com/ubuntu/pool/main/l/lzo2/lzo2_2.10.orig.tar.gz' lzo2_2.10.orig.tar.gz 600622 SHA512:a3dae5e4a6b93b1f5bf7435e8ab114a9be57252e9efc5dd444947d7a2d031b0819f34bcaeb35f60b5629a01b1238d738735a64db8f672be9690d3c80094511a4
'http://archive.ubuntu.com/ubuntu/pool/main/l/lzo2/lzo2_2.10-2build3.debian.tar.xz' lzo2_2.10-2build3.debian.tar.xz 7068 SHA512:e25f2f05621bb4d81e85e8a7e0d0c0673f0f5162db09bb6a3b07f766f58e8f50021a2453fa67bfb506bf1653a42f6a33fb786b66597ce138aa075bbb0d69f68a
```

### `dpkg` source package: `m4=1.4.19-4`

Binary Packages:

- `m4=1.4.19-4`

Licenses: (parsed from: `/usr/share/doc/m4/copyright`)

- `GFDL`
- `GPL`

Source:

```console
$ apt-get source -qq --print-uris m4=1.4.19-4
'http://archive.ubuntu.com/ubuntu/pool/main/m/m4/m4_1.4.19-4.dsc' m4_1.4.19-4.dsc 1637 SHA512:5c29da4a25ccbf3d0b37cb0e30e05e7ccce5f357563649493d8ab52e7304ecaa03e2d0473221e58b7490e13ed127f1455f08ec7308cb9155ee90b41f54fc58fd
'http://archive.ubuntu.com/ubuntu/pool/main/m/m4/m4_1.4.19.orig.tar.xz' m4_1.4.19.orig.tar.xz 1654908 SHA512:47f595845c89709727bda0b3fc78e3188ef78ec818965b395532e7041cabe9e49677ee4aca3d042930095a7f8df81de3da1026b23b6897be471f6cf13ddd512b
'http://archive.ubuntu.com/ubuntu/pool/main/m/m4/m4_1.4.19.orig.tar.xz.asc' m4_1.4.19.orig.tar.xz.asc 488 SHA512:d6ac9c6a54c57e9b53fb3e34a60d49df2f46a6e494da0a0c9ae8246b984e68a853b5d8c42677c1a0485c3f36b0bce10a481d3775c0edc1dbdfb27b43545bc31e
'http://archive.ubuntu.com/ubuntu/pool/main/m/m4/m4_1.4.19-4.debian.tar.xz' m4_1.4.19-4.debian.tar.xz 17308 SHA512:19b39bd3629328fccb47092787d8327924dabb37ce2f4bb3b5b715ff9474c0269b9bab0d4ede151e5c02c79cbbb21725b0ed67408907056cd4d39f4581fd24c8
```

### `dpkg` source package: `make-dfsg=4.3-4.1build1`

Binary Packages:

- `make=4.3-4.1build1`

Licenses: (parsed from: `/usr/share/doc/make/copyright`)

- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris make-dfsg=4.3-4.1build1
'http://archive.ubuntu.com/ubuntu/pool/main/m/make-dfsg/make-dfsg_4.3-4.1build1.dsc' make-dfsg_4.3-4.1build1.dsc 2072 SHA512:f5580f5dc9e7d4ee3a7bfcd82a42c0615a4828cac1f84db3c720260209cee3334d0a23ea78113cd2b26eaf233d46ec59743d14a8bd05cfd225f111ff739ad57d
'http://archive.ubuntu.com/ubuntu/pool/main/m/make-dfsg/make-dfsg_4.3.orig.tar.gz' make-dfsg_4.3.orig.tar.gz 1845906 SHA512:bdc150f9d256145923380d6e7058ab9b2b4e43fcb1d75ab2984fa8f859eab6852a68e4ea5f626633e0bec76fbebf1477378e268e8ffdb5cb2a53b29cbc439bc1
'http://archive.ubuntu.com/ubuntu/pool/main/m/make-dfsg/make-dfsg_4.3-4.1build1.diff.gz' make-dfsg_4.3-4.1build1.diff.gz 50780 SHA512:258dc63a0cea09995adfe4091599664e2ef0d5f81c990f980b0ddf9e02212177c4a23fa8d82e886ecbae33c84816c61530e97fd82c5347ff25a434a3aa6732ae
```

### `dpkg` source package: `mawk=1.3.4.20231126-1`

Binary Packages:

- `mawk=1.3.4.20231126-1`

Licenses: (parsed from: `/usr/share/doc/mawk/copyright`)

- `CC-BY-3.0`
- `GPL-2`
- `GPL-2.0-only`
- `X11`

Source:

```console
$ apt-get source -qq --print-uris mawk=1.3.4.20231126-1
'http://archive.ubuntu.com/ubuntu/pool/main/m/mawk/mawk_1.3.4.20231126-1.dsc' mawk_1.3.4.20231126-1.dsc 2180 SHA512:c8d1068997766c067f6b3a687d6a43ba8aafecba88519d66f5a6bfbd6ec151ccf2fb54aa2e79ff82e92c88d550227332f50415f28fd5227f58ebb21e9cab3b14
'http://archive.ubuntu.com/ubuntu/pool/main/m/mawk/mawk_1.3.4.20231126.orig.tar.gz' mawk_1.3.4.20231126.orig.tar.gz 413452 SHA512:faacd473df97fc51cf3ece652e0826b13c26e8de5fa87746dfcc097811a9464a71e5630a8f3b4d243e0c1dc0199751b64d9a1bf34fe5080b646c0e5fff231e0d
'http://archive.ubuntu.com/ubuntu/pool/main/m/mawk/mawk_1.3.4.20231126.orig.tar.gz.asc' mawk_1.3.4.20231126.orig.tar.gz.asc 729 SHA512:19a9725f84651f87ecb38350984a60fce52046df45be7c494e615db91f6b76229d3dba20211bca41b90a7370fbba97fcb7bb2fe475ffb880fac7f1116f14333f
'http://archive.ubuntu.com/ubuntu/pool/main/m/mawk/mawk_1.3.4.20231126-1.debian.tar.xz' mawk_1.3.4.20231126-1.debian.tar.xz 15544 SHA512:f33b2576e5eed9b446aaaa365a5f3795146b38e6c57046217e7820c27e35c2f556147e273288b52d3fb993f769bf99148f6e1ea4eac86f74a1981599078e6ce1
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

### `dpkg` source package: `mercurial=6.5.3-1`

Binary Packages:

- `mercurial=6.5.3-1`
- `mercurial-common=6.5.3-1`

Licenses: (parsed from: `/usr/share/doc/mercurial/copyright`, `/usr/share/doc/mercurial-common/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris mercurial=6.5.3-1
'http://archive.ubuntu.com/ubuntu/pool/universe/m/mercurial/mercurial_6.5.3-1.dsc' mercurial_6.5.3-1.dsc 2806 SHA512:8d2939b34347e5c43cfe7ff8a95e0e4bfac285ee01545c0eb230aa17f7883c7cfdd96c833cc57077b2cfa5f08fc6dedc6739462722d7cbc47e258f5d27501a37
'http://archive.ubuntu.com/ubuntu/pool/universe/m/mercurial/mercurial_6.5.3.orig.tar.gz' mercurial_6.5.3.orig.tar.gz 8235306 SHA512:af90ec414fbf9da518ce0de5b855b5dd6e4141f838ab0da54a40f31aa00245d21f14f1352fe537744fb6ae5a3e4f2723076f4773fafac649b8483fefd002b510
'http://archive.ubuntu.com/ubuntu/pool/universe/m/mercurial/mercurial_6.5.3.orig.tar.gz.asc' mercurial_6.5.3.orig.tar.gz.asc 659 SHA512:01ee8724a342a4a71431effdf336c2e4982921d83bf6e350e62dadcbda1f1c264d7453acc00738bdba46763a3567369cee22037e4fe35c9e4d822829506805f2
'http://archive.ubuntu.com/ubuntu/pool/universe/m/mercurial/mercurial_6.5.3-1.debian.tar.xz' mercurial_6.5.3-1.debian.tar.xz 69264 SHA512:058a3f4793dfc003eca044a93022c5442721f745f5a7d173e9b7e5184783e53cb1057f3084a4a9842dec323e9271d489db3b05b68d27c464501d401033ff908c
```

### `dpkg` source package: `mpclib3=1.3.1-1`

Binary Packages:

- `libmpc3:amd64=1.3.1-1`

Licenses: (parsed from: `/usr/share/doc/libmpc3/copyright`)

- `LGPL-3`

Source:

```console
$ apt-get source -qq --print-uris mpclib3=1.3.1-1
'http://archive.ubuntu.com/ubuntu/pool/main/m/mpclib3/mpclib3_1.3.1-1.dsc' mpclib3_1.3.1-1.dsc 1877 SHA512:242e6c50161e6a9123dd9599629cc11b2ebc3e572186cfcd09f94d72df9e23db7937b825515331ed00e5d0825585c0898b435d9213aa31be5c2648d5e0f54825
'http://archive.ubuntu.com/ubuntu/pool/main/m/mpclib3/mpclib3_1.3.1.orig.tar.gz' mpclib3_1.3.1.orig.tar.gz 773573 SHA512:4bab4ef6076f8c5dfdc99d810b51108ced61ea2942ba0c1c932d624360a5473df20d32b300fc76f2ba4aa2a97e1f275c9fd494a1ba9f07c4cb2ad7ceaeb1ae97
'http://archive.ubuntu.com/ubuntu/pool/main/m/mpclib3/mpclib3_1.3.1-1.debian.tar.xz' mpclib3_1.3.1-1.debian.tar.xz 4656 SHA512:637b992f2eeab690a45397851dd4665d88e026054a6da08404e5fd96fc4d4a583bbf21922e3282e93345a17e091a373492a3a426eb1b2d25d19c8d83d013fdd1
```

### `dpkg` source package: `mpfr4=4.2.1-1`

Binary Packages:

- `libmpfr6:amd64=4.2.1-1`

Licenses: (parsed from: `/usr/share/doc/libmpfr6/copyright`)

- `GFDL-1.2`
- `LGPL-3`

Source:

```console
$ apt-get source -qq --print-uris mpfr4=4.2.1-1
'http://archive.ubuntu.com/ubuntu/pool/main/m/mpfr4/mpfr4_4.2.1-1.dsc' mpfr4_4.2.1-1.dsc 1959 SHA512:ddb3f2fe908d50f06f2f36103c09eaeeca0e1d9b3660a45d6b284175523973c6adf2e9846e61f594306d590dcc46f518284b15debb43b818a8ff38f42d902e41
'http://archive.ubuntu.com/ubuntu/pool/main/m/mpfr4/mpfr4_4.2.1.orig.tar.xz' mpfr4_4.2.1.orig.tar.xz 1493608 SHA512:bc68c0d755d5446403644833ecbb07e37360beca45f474297b5d5c40926df1efc3e2067eecffdf253f946288bcca39ca89b0613f545d46a9e767d1d4cf358475
'http://archive.ubuntu.com/ubuntu/pool/main/m/mpfr4/mpfr4_4.2.1-1.debian.tar.xz' mpfr4_4.2.1-1.debian.tar.xz 12556 SHA512:b10465385039b7d17f81dd960d0adc3e92cf6a254a1949b1e88ca2a10da626f1333fd3bf3c37d903b87ffc5458260ac765cccbfc65bb4647953cfb85975fa333
```

### `dpkg` source package: `mysql-8.0=8.0.35-1ubuntu2`

Binary Packages:

- `libmysqlclient-dev=8.0.35-1ubuntu2`
- `libmysqlclient21:amd64=8.0.35-1ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libmysqlclient-dev/copyright`, `/usr/share/doc/libmysqlclient21/copyright`)

- `Artistic`
- `BSD-2-clause`
- `BSD-3-clause`
- `BSD-like`
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
$ apt-get source -qq --print-uris mysql-8.0=8.0.35-1ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/m/mysql-8.0/mysql-8.0_8.0.35-1ubuntu2.dsc' mysql-8.0_8.0.35-1ubuntu2.dsc 3789 SHA512:2931ec91aade1c2e936166451dff6e1d65c019211391341b2ee0a1db36d328cc46fdcde80c2c0b4c5a3578e25a251c29ad8e9b418464ac3074c5439fa33b1e78
'http://archive.ubuntu.com/ubuntu/pool/main/m/mysql-8.0/mysql-8.0_8.0.35.orig.tar.gz' mysql-8.0_8.0.35.orig.tar.gz 438111810 SHA512:2936f7a84aa5f96633b239d1dba3613462d88f3a2ea493a7d05aa9a9b590e9e36a30857f44fcdb11360242375d6106e80cd1b32e0c6cb14502c1518ad1a720b2
'http://archive.ubuntu.com/ubuntu/pool/main/m/mysql-8.0/mysql-8.0_8.0.35.orig.tar.gz.asc' mysql-8.0_8.0.35.orig.tar.gz.asc 833 SHA512:1d97b8046f31b93e19ebd01002008004d817c448e409934c86a28f0319b491acc2c4c2d950a9e4c34e326deb1e3e8b53ce3949947371fcf941e825fa056d380c
'http://archive.ubuntu.com/ubuntu/pool/main/m/mysql-8.0/mysql-8.0_8.0.35-1ubuntu2.debian.tar.xz' mysql-8.0_8.0.35-1ubuntu2.debian.tar.xz 145272 SHA512:e36d160b95ee57544e713037cbddbeb3a011d4386fbb5fae87cc0039c76cc484f039d103e76ba7c5724f485b8053b73e5b78624d7e09c277aca6100960987704
```

### `dpkg` source package: `mysql-defaults=1.1.0`

Binary Packages:

- `default-libmysqlclient-dev:amd64=1.1.0`
- `mysql-common=5.8+1.1.0`

Licenses: (parsed from: `/usr/share/doc/default-libmysqlclient-dev/copyright`, `/usr/share/doc/mysql-common/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris mysql-defaults=1.1.0
'http://archive.ubuntu.com/ubuntu/pool/main/m/mysql-defaults/mysql-defaults_1.1.0.dsc' mysql-defaults_1.1.0.dsc 2279 SHA512:a1743552a88c65e8258eb5174b488c68d5f58e78a13a7c16491855dfb1d83627041668bfbae6148d917a2fe70cfbd6571a22380522f3077413a9cb20e039e783
'http://archive.ubuntu.com/ubuntu/pool/main/m/mysql-defaults/mysql-defaults_1.1.0.tar.xz' mysql-defaults_1.1.0.tar.xz 7396 SHA512:e4fa4e01dbacc0655cea8e6c4d3b79e8edd9a8626977ef47d83fd155d4997bd36ff93377d368d26cea7fd6bd412dd058db5cc063ae3051c9d0ab4f3283e46995
```

### `dpkg` source package: `ncurses=6.4+20231209-1`

Binary Packages:

- `libncurses-dev:amd64=6.4+20231209-1`
- `libncurses6:amd64=6.4+20231209-1`
- `libncursesw6:amd64=6.4+20231209-1`
- `libtinfo6:amd64=6.4+20231209-1`
- `ncurses-base=6.4+20231209-1`
- `ncurses-bin=6.4+20231209-1`

Licenses: (parsed from: `/usr/share/doc/libncurses-dev/copyright`, `/usr/share/doc/libncurses6/copyright`, `/usr/share/doc/libncursesw6/copyright`, `/usr/share/doc/libtinfo6/copyright`, `/usr/share/doc/ncurses-base/copyright`, `/usr/share/doc/ncurses-bin/copyright`)

- `BSD-3-clause`
- `MIT/X11`
- `X11`

Source:

```console
$ apt-get source -qq --print-uris ncurses=6.4+20231209-1
'http://archive.ubuntu.com/ubuntu/pool/main/n/ncurses/ncurses_6.4%2b20231209-1.dsc' ncurses_6.4+20231209-1.dsc 3807 SHA512:c883e058d00b75e2d56d2bfafcb5dfee029c96cb79c9c17504dcea29b0183a2bc58a9d2d7ba028c90584821ad7c65abd99ff29b48404c4fbd472ea69e4952553
'http://archive.ubuntu.com/ubuntu/pool/main/n/ncurses/ncurses_6.4%2b20231209.orig.tar.gz' ncurses_6.4+20231209.orig.tar.gz 3673169 SHA512:293b91b20f676230e28dadfc6ec811ac898e56d558d919566bf515d91ee9bd5df222f56da593d5ce249550a38ad4a9d206df2761f170c7738c9e8a3ea564e42a
'http://archive.ubuntu.com/ubuntu/pool/main/n/ncurses/ncurses_6.4%2b20231209.orig.tar.gz.asc' ncurses_6.4+20231209.orig.tar.gz.asc 729 SHA512:39936242c7ef118f73d0d93d985a970b59c23f436dc7844084affa8ea76ae036b6794cba57e8320e20a3dd9eb1fce1344615a82780d4dcd750a47333d9d99e00
'http://archive.ubuntu.com/ubuntu/pool/main/n/ncurses/ncurses_6.4%2b20231209-1.debian.tar.xz' ncurses_6.4+20231209-1.debian.tar.xz 48812 SHA512:51a090855ed265a33a0ec26c8f75f958f8228744dba49803480d55957fae9c44169b7552e521f9ad2173c75f51872bf4d3c3a080bf3de304bf136f561f2cc373
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

### `dpkg` source package: `nghttp2=1.58.0-1`

Binary Packages:

- `libnghttp2-14:amd64=1.58.0-1`

Licenses: (parsed from: `/usr/share/doc/libnghttp2-14/copyright`)

- `BSD-2-clause`
- `Expat`
- `GPL-3`
- `GPL-3+ with autoconf exception`
- `MIT`
- `all-permissive`

Source:

```console
$ apt-get source -qq --print-uris nghttp2=1.58.0-1
'http://archive.ubuntu.com/ubuntu/pool/main/n/nghttp2/nghttp2_1.58.0-1.dsc' nghttp2_1.58.0-1.dsc 2534 SHA512:e5c4f7da9d382d75832ac94a71183eb88c87e1611c2c282b47230c26236303c75801b6dacf4acda35c45b995c95dc7482b25579aa68a52036f58b45528493dd2
'http://archive.ubuntu.com/ubuntu/pool/main/n/nghttp2/nghttp2_1.58.0.orig.tar.gz' nghttp2_1.58.0.orig.tar.gz 1061810 SHA512:70d7b37b57494847dd6ce940361a4add2dbbd0f533253cafb926089bbf9ad2376d52bf6334427521a133517fae14b7f96ca4c052c434c28ebcfb1a66db884d1d
'http://archive.ubuntu.com/ubuntu/pool/main/n/nghttp2/nghttp2_1.58.0-1.debian.tar.xz' nghttp2_1.58.0-1.debian.tar.xz 11788 SHA512:01a467dfce017ad47707e21ebef43b215ccdf7940e273fbc0e16ed616a59f38b260f70dde15e53ca24c545a9e489967b747c6f857b6794122fd519d1e7f353c1
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

### `dpkg` source package: `numpy=1:1.24.2-2`

Binary Packages:

- `python3-numpy=1:1.24.2-2`

Licenses: (parsed from: `/usr/share/doc/python3-numpy/copyright`)

- `BSD-2-Clause`
- `BSD-3-Clause`
- `MIT`
- `Public-Domain`
- `zlib`

Source:

```console
$ apt-get source -qq --print-uris numpy=1:1.24.2-2
'http://archive.ubuntu.com/ubuntu/pool/main/n/numpy/numpy_1.24.2-2.dsc' numpy_1.24.2-2.dsc 1886 SHA512:fc3636d119d9aa1bef25b84a4c30131ff6b9c4b12138d80a4a9c15b46f738bf52a33e657292ed0cd348a5b74bee86e28151dafdce384efe8bc8b58703695705e
'http://archive.ubuntu.com/ubuntu/pool/main/n/numpy/numpy_1.24.2.orig.tar.xz' numpy_1.24.2.orig.tar.xz 8239412 SHA512:312c67147e5d98f28ca5cb29ba956b8ba75284fe68e2639256bfc8803ce776ac02929a0ec91efcf926494fad5dfbf25f651a854ec8a95f26163143ac0d001bdb
'http://archive.ubuntu.com/ubuntu/pool/main/n/numpy/numpy_1.24.2-2.debian.tar.xz' numpy_1.24.2-2.debian.tar.xz 32064 SHA512:c08f9173d36602a5e9dd6c83254a88e8fbba1aae9dad1b3ceddecfb34f25a1276b2c5863ebf8b323806bbe0fa2b1d2ecdd4756133f5cb6bf1cc5ac541a62a7b5
```

### `dpkg` source package: `openexr=3.1.5-5.1`

Binary Packages:

- `libopenexr-3-1-30:amd64=3.1.5-5.1`
- `libopenexr-dev=3.1.5-5.1`

Licenses: (parsed from: `/usr/share/doc/libopenexr-3-1-30/copyright`, `/usr/share/doc/libopenexr-dev/copyright`)

- `BSD-3-clause`
- `openexr`

Source:

```console
$ apt-get source -qq --print-uris openexr=3.1.5-5.1
'http://archive.ubuntu.com/ubuntu/pool/universe/o/openexr/openexr_3.1.5-5.1.dsc' openexr_3.1.5-5.1.dsc 2489 SHA512:f8008331e6a9530219bf71306bc1c8f0da83b4a7c0dd684f77c20e842d0faa5317f1b798cb0023012d7fda88a7a13e6d616f0306f72349da08d4e47fd8da1614
'http://archive.ubuntu.com/ubuntu/pool/universe/o/openexr/openexr_3.1.5.orig.tar.gz' openexr_3.1.5.orig.tar.gz 20327926 SHA512:01ef16eacd2dde83c67b81522bae87f47ba272a41ce7d4e35d865dbdcaa03093e7ac504b95d2c1b3a19535f2364a4f937b0e0570c74243bb1c6e021fce7b620c
'http://archive.ubuntu.com/ubuntu/pool/universe/o/openexr/openexr_3.1.5.orig.tar.gz.asc' openexr_3.1.5.orig.tar.gz.asc 287 SHA512:9b3978e44b531429aba42b9cc4969a470898d9d74652e3809edb0273ba9b127c471aec6570b5d352be738f59810091c0df2c70d39c16d2c32833d173b270f72c
'http://archive.ubuntu.com/ubuntu/pool/universe/o/openexr/openexr_3.1.5-5.1.debian.tar.xz' openexr_3.1.5-5.1.debian.tar.xz 18828 SHA512:37d5507a3a3ed456ae189283923a3d9417cb321d5f7f1ffa94b86fffcd5f53ff3a1b9641906e0c970a59e9d6d14f7a8fd714726ce2e891dd14243967c287c67e
```

### `dpkg` source package: `openjpeg2=2.5.0-2`

Binary Packages:

- `libopenjp2-7:amd64=2.5.0-2`
- `libopenjp2-7-dev:amd64=2.5.0-2`

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

Source:

```console
$ apt-get source -qq --print-uris openjpeg2=2.5.0-2
'http://archive.ubuntu.com/ubuntu/pool/main/o/openjpeg2/openjpeg2_2.5.0-2.dsc' openjpeg2_2.5.0-2.dsc 2673 SHA512:ad2f14733d6142ccf6a410ebd6498326d33cde910211c39994f15e7c6fb4e5c3c9e2953bb6120178e0c52ab036f073d2dda6c2be0141a1e32c4c230b239b43a2
'http://archive.ubuntu.com/ubuntu/pool/main/o/openjpeg2/openjpeg2_2.5.0.orig.tar.xz' openjpeg2_2.5.0.orig.tar.xz 1221108 SHA512:a266297d60ff93e14dbee890b01a76870bda69f082dbe8932fc444ccd260c27aaaac8b22e3c00ca71930b2555a1cad6cf6ed0d5d882d9d13f472cc494cab8234
'http://archive.ubuntu.com/ubuntu/pool/main/o/openjpeg2/openjpeg2_2.5.0-2.debian.tar.xz' openjpeg2_2.5.0-2.debian.tar.xz 17388 SHA512:4cc7c0fd4237efdc79c209ad548e30477fc587ef9206a4e10d7b879309cb087c3ec0b6ee7a6350002405f303546ed54835f34d63a5681a8302f394ca0f985181
```

### `dpkg` source package: `openldap=2.6.6+dfsg-1~exp1ubuntu1`

Binary Packages:

- `libldap2:amd64=2.6.6+dfsg-1~exp1ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libldap2/copyright`)

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

### `dpkg` source package: `openssh=1:9.4p1-1ubuntu1`

Binary Packages:

- `openssh-client=1:9.4p1-1ubuntu1`

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
$ apt-get source -qq --print-uris openssh=1:9.4p1-1ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssh/openssh_9.4p1-1ubuntu1.dsc' openssh_9.4p1-1ubuntu1.dsc 3337 SHA512:d8117a2a82c66a4677763ebaefe79a68f82d9d4577e45cbe4ac4becd129a1a55f770e361476957221903072f57cae6622a673f600c12ae9a11bc05f0daaa722b
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssh/openssh_9.4p1.orig.tar.gz' openssh_9.4p1.orig.tar.gz 1845094 SHA512:0aaedeced7dbc70419c7245eb0e9db4ef570e0e7739b890ebae04d56da5fe8d147e8e150f3c943f60730976569e3ac6cc8da62ec7e2a78e2ef47d295ca0b1d25
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssh/openssh_9.4p1.orig.tar.gz.asc' openssh_9.4p1.orig.tar.gz.asc 833 SHA512:983b4ebaa3b98e70831ce686cb503270926c065163a2510eef0c5102ef50b6e665b889ee15ea8c0bd7c4bbddb19270f036e1d554a8212ef2c292f9c682c8631a
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssh/openssh_9.4p1-1ubuntu1.debian.tar.xz' openssh_9.4p1-1ubuntu1.debian.tar.xz 190660 SHA512:38e7f25668173012f746a669457907b88b85c0e9e0e66e98eb09501c0076268a1079f69b5c0459861dd0f1e3bf359cd0552370975b80bea2ca1fcbdba7144969
```

### `dpkg` source package: `openssl=3.0.10-1ubuntu3`

Binary Packages:

- `libssl-dev:amd64=3.0.10-1ubuntu3`
- `libssl3:amd64=3.0.10-1ubuntu3`
- `openssl=3.0.10-1ubuntu3`

Licenses: (parsed from: `/usr/share/doc/libssl-dev/copyright`, `/usr/share/doc/libssl3/copyright`, `/usr/share/doc/openssl/copyright`)

- `Apache-2.0`
- `Artistic`
- `GPL-1`
- `GPL-1+`

Source:

```console
$ apt-get source -qq --print-uris openssl=3.0.10-1ubuntu3
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssl/openssl_3.0.10-1ubuntu3.dsc' openssl_3.0.10-1ubuntu3.dsc 2473 SHA512:35ffad00cdd471d1b17d1648fc4bec3f6d301be6746b2f5e716fd7576269988db506016a13825f2d341ab35c8563c4bcd28d51afe88c770fe3ea6e46dfb0d928
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssl/openssl_3.0.10.orig.tar.gz' openssl_3.0.10.orig.tar.gz 15194904 SHA512:fc12f3beed5e2d2f4767aeb772ceb6ba26f6cbfabc247765854108266b27a1223134f0e81735867a9069bc9c07a14b9816e85903cef91bd1b90f781f0b98b61a
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssl/openssl_3.0.10-1ubuntu3.debian.tar.xz' openssl_3.0.10-1ubuntu3.debian.tar.xz 121200 SHA512:391ac9c86c93572e972f091b5a56437365c92ef530044449cea3b82967597af467abc46e13460e4838974d484c680b83fa7f79cdb44df8b681954335a69ff9a5
```

### `dpkg` source package: `p11-kit=0.25.3-2ubuntu2`

Binary Packages:

- `libp11-kit0:amd64=0.25.3-2ubuntu2`

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
$ apt-get source -qq --print-uris p11-kit=0.25.3-2ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/p/p11-kit/p11-kit_0.25.3-2ubuntu2.dsc' p11-kit_0.25.3-2ubuntu2.dsc 2645 SHA512:7dc7b2379e203df71ec61279ad8b02a952e45a235a1b89c4751329102b37b8ec9261c85bd08cbf896f9eb7ae184e46a21c2c725405fcaf13f0e1e4af5997f19d
'http://archive.ubuntu.com/ubuntu/pool/main/p/p11-kit/p11-kit_0.25.3.orig.tar.xz' p11-kit_0.25.3.orig.tar.xz 991528 SHA512:ad2d393bf122526cbba18dc9d5a13f2c1cad7d70125ec90ffd02059dfa5ef30ac59dfc0bb9bc6380c8f317e207c9e87e895f1945634f56ddf910c2958868fb4c
'http://archive.ubuntu.com/ubuntu/pool/main/p/p11-kit/p11-kit_0.25.3.orig.tar.xz.asc' p11-kit_0.25.3.orig.tar.xz.asc 228 SHA512:e275d64222dc5b15fd5d0f6927c8317dc7f85fdce8dea084a5cda8845ae1115e04680c7ebe774d7f97232a7aab271e8d264f2dbcb2d90833ad70b6fa7946b778
'http://archive.ubuntu.com/ubuntu/pool/main/p/p11-kit/p11-kit_0.25.3-2ubuntu2.debian.tar.xz' p11-kit_0.25.3-2ubuntu2.debian.tar.xz 25908 SHA512:0a09ade5e91672790bb1b191210ef17c5ed88cade440a16619239769b80b7552690323ab5f9ebdfc053fa2c602b8fdaa936af2f3374a7d38ac4a866e1e0f2792
```

### `dpkg` source package: `pam=1.5.2-9.1ubuntu1`

Binary Packages:

- `libpam-modules:amd64=1.5.2-9.1ubuntu1`
- `libpam-modules-bin=1.5.2-9.1ubuntu1`
- `libpam-runtime=1.5.2-9.1ubuntu1`
- `libpam0g:amd64=1.5.2-9.1ubuntu1`

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
$ apt-get source -qq --print-uris pam=1.5.2-9.1ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/p/pam/pam_1.5.2-9.1ubuntu1.dsc' pam_1.5.2-9.1ubuntu1.dsc 2741 SHA512:d4b7216f82b103713935acee9438bc25da29f3b21619d933e719016aded88a31971271bfdf8d798148a9b6f0768c262b8eb47a454aa17ec6c662530c056b9f95
'http://archive.ubuntu.com/ubuntu/pool/main/p/pam/pam_1.5.2.orig.tar.xz' pam_1.5.2.orig.tar.xz 988784 SHA512:fa16350c132d3e5fb82b60d991768fb596582639841b8ece645c684705467305ccf1302a0147ec222ab78c01b2c9114c5496dc1ca565d2b56bf315f29a815144
'http://archive.ubuntu.com/ubuntu/pool/main/p/pam/pam_1.5.2-9.1ubuntu1.debian.tar.xz' pam_1.5.2-9.1ubuntu1.debian.tar.xz 176544 SHA512:91ce7e7d2c575f9e8db5fd7c6903809d4cbec3c276136c7d32622753b22d87f94ed70d34379b671a016003a36ec4a3aa02c18c2578af31c100d3a3380bf11ee7
```

### `dpkg` source package: `pango1.0=1.51.0+ds-3`

Binary Packages:

- `libpango-1.0-0:amd64=1.51.0+ds-3`
- `libpangocairo-1.0-0:amd64=1.51.0+ds-3`
- `libpangoft2-1.0-0:amd64=1.51.0+ds-3`

Licenses: (parsed from: `/usr/share/doc/libpango-1.0-0/copyright`, `/usr/share/doc/libpangocairo-1.0-0/copyright`, `/usr/share/doc/libpangoft2-1.0-0/copyright`)

- `Apache-2`
- `Apache-2.0`
- `Bitstream-Vera`
- `CC0-1.0`
- `Chromium-BSD-style`
- `Example`
- `GPL-2+`
- `GPL-2.0`
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
$ apt-get source -qq --print-uris pango1.0=1.51.0+ds-3
'http://archive.ubuntu.com/ubuntu/pool/main/p/pango1.0/pango1.0_1.51.0%2bds-3.dsc' pango1.0_1.51.0+ds-3.dsc 3469 SHA512:c5beadea2796bdd48203fc1a748bc0cb4edd2994b7343f038808f50f2dc291799b0fc515a0e4f5af88292bed06a1381162d93cc7750cd177886ec44350ce9017
'http://archive.ubuntu.com/ubuntu/pool/main/p/pango1.0/pango1.0_1.51.0%2bds.orig.tar.xz' pango1.0_1.51.0+ds.orig.tar.xz 1731104 SHA512:2ed4ec6baf4e21da1f19d4ef43b1e3b1753229022f8e8ae6ac4ef910ab664defba8fd99391255d37f5b0f5b71ec3aee7f1ba15f5a449c04dfb07902fd700a635
'http://archive.ubuntu.com/ubuntu/pool/main/p/pango1.0/pango1.0_1.51.0%2bds-3.debian.tar.xz' pango1.0_1.51.0+ds-3.debian.tar.xz 41176 SHA512:6df56c735ee171ca44bb713d3cdbed7607d0dc4efea37929ee6c144f71f9e94bc4df9d23c3a1e5367acfeeb10227c1f3d0791cfc12e64b23dbb26e02c35078f4
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

### `dpkg` source package: `pcre2=10.42-4ubuntu1`

Binary Packages:

- `libpcre2-16-0:amd64=10.42-4ubuntu1`
- `libpcre2-32-0:amd64=10.42-4ubuntu1`
- `libpcre2-8-0:amd64=10.42-4ubuntu1`
- `libpcre2-dev:amd64=10.42-4ubuntu1`
- `libpcre2-posix3:amd64=10.42-4ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libpcre2-16-0/copyright`, `/usr/share/doc/libpcre2-32-0/copyright`, `/usr/share/doc/libpcre2-8-0/copyright`, `/usr/share/doc/libpcre2-dev/copyright`, `/usr/share/doc/libpcre2-posix3/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `BSD-3-clause-Cambridge with BINARY LIBRARY-LIKE PACKAGES exception`
- `X11`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris pcre2=10.42-4ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/p/pcre2/pcre2_10.42-4ubuntu1.dsc' pcre2_10.42-4ubuntu1.dsc 2190 SHA512:a372057713290809747c3333ed7b740532401cf60012f65dc680d2f71b5b0548ed21f50b033d6a7b7ec703064093deed729c9e63db8a19e24780301979a0c4b7
'http://archive.ubuntu.com/ubuntu/pool/main/p/pcre2/pcre2_10.42.orig.tar.gz' pcre2_10.42.orig.tar.gz 2397194 SHA512:a3db6c5c620775838819be616652e73ce00f5ef5c1f49f559ff3efb51a119d02f01254c5901c1f7d0c47c0ddfcf4313e38d6ca32c35381b8f87f36896d10e6f7
'http://archive.ubuntu.com/ubuntu/pool/main/p/pcre2/pcre2_10.42-4ubuntu1.diff.gz' pcre2_10.42-4ubuntu1.diff.gz 8296 SHA512:a9e8a3d8d1e5bcb274df0ce5e7d1f548bed69c0466c624026d9456013f4476826c5a4187c3042efcfc468cb40490a8d1ed02e1b542d5cf606e1a5f073f480278
```

### `dpkg` source package: `perl=5.36.0-10ubuntu1`

Binary Packages:

- `libperl5.36:amd64=5.36.0-10ubuntu1`
- `perl=5.36.0-10ubuntu1`
- `perl-base=5.36.0-10ubuntu1`
- `perl-modules-5.36=5.36.0-10ubuntu1`

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
$ apt-get source -qq --print-uris perl=5.36.0-10ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.36.0-10ubuntu1.dsc' perl_5.36.0-10ubuntu1.dsc 3005 SHA512:d6bbb4d9c87b71be0895611e74e5a70654daa18cdf67ca159770437c320778cec28b9d533ca7160a7d8a8905099187b2b04891e32c9fb6bafd217dfb0ee80a93
'http://archive.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.36.0.orig-regen-configure.tar.xz' perl_5.36.0.orig-regen-configure.tar.xz 417784 SHA512:4d16685f569a5b1dea79d607b6d62718111c32efaf5547bb9e1528bd755acf0c8fc74a1cc1f4d68fcb10aef9da7d8fea17a5cc10dabce6efa4721ab45ab03a65
'http://archive.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.36.0.orig.tar.xz' perl_5.36.0.orig.tar.xz 13051500 SHA512:6dd6ac2a77566c173c5ab9c238cf555f2c3e592e89abb5600bc23ce1cbd0c349e0233f6417cbbf1f6d0aefc6a734ba491285af0d3dc68a605b658b65c89f1dab
'http://archive.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.36.0-10ubuntu1.debian.tar.xz' perl_5.36.0-10ubuntu1.debian.tar.xz 172652 SHA512:785b2ac899ac3a4464d221d8fdffc126c5e79053e1cfc5c03b15d4f3c0ac3f653fb38e44f60db08749f9b33b029b1dfecf3735fb6c341e6316860d09f66a03b5
```

### `dpkg` source package: `pinentry=1.2.1-3ubuntu1`

Binary Packages:

- `pinentry-curses=1.2.1-3ubuntu1`

Licenses: (parsed from: `/usr/share/doc/pinentry-curses/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-3`
- `LGPL-3+`
- `X11`

Source:

```console
$ apt-get source -qq --print-uris pinentry=1.2.1-3ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/p/pinentry/pinentry_1.2.1-3ubuntu1.dsc' pinentry_1.2.1-3ubuntu1.dsc 3322 SHA512:fadeaa04c5eb8be10642f702183bd450b5a26da08270138c2a8a450ede5e3952ee6d9345402abe47583e3b25c028899fd0966e7fd5df555a7e4caf84456a8f5f
'http://archive.ubuntu.com/ubuntu/pool/main/p/pinentry/pinentry_1.2.1.orig.tar.bz2' pinentry_1.2.1.orig.tar.bz2 547698 SHA512:a665315628f4dcf07e16a22db3f3be15d7e7e93b3deec0546c7275b71b0e3bd65535a08af5e12d6339fd6595132df86529401d9d12bd17c428a3466e8dfafab6
'http://archive.ubuntu.com/ubuntu/pool/main/p/pinentry/pinentry_1.2.1.orig.tar.bz2.asc' pinentry_1.2.1.orig.tar.bz2.asc 390 SHA512:60b63b7fe2d6793840be55635f9a704cd42eda69ccaea2453d47b5f7a5198d313b8f23555972584f7f087fd5d0fc2a379bfc5f7512f325b018cc5c3e2e54a47e
'http://archive.ubuntu.com/ubuntu/pool/main/p/pinentry/pinentry_1.2.1-3ubuntu1.debian.tar.xz' pinentry_1.2.1-3ubuntu1.debian.tar.xz 19116 SHA512:4a0b8ff1d4cb1d2df691ae73f63c99b68efbbd01e0da3cf9664cbd7ad0f34a5b95c94c8f1c6e6c7c0199ffcf9d7998996a1e30d6c331080c6613914167905fbd
```

### `dpkg` source package: `pixman=0.42.2-1`

Binary Packages:

- `libpixman-1-0:amd64=0.42.2-1`
- `libpixman-1-dev:amd64=0.42.2-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris pixman=0.42.2-1
'http://archive.ubuntu.com/ubuntu/pool/main/p/pixman/pixman_0.42.2-1.dsc' pixman_0.42.2-1.dsc 2021 SHA512:cd8fe22f4c8de60b0966a8100ea3204c321f5223b620a890f5901afdee2030783cd0379e2b4df602c3581120cc2ad28684137e5e34fdc99c795baf32e1cfd959
'http://archive.ubuntu.com/ubuntu/pool/main/p/pixman/pixman_0.42.2.orig.tar.gz' pixman_0.42.2.orig.tar.gz 959669 SHA512:0a4e327aef89c25f8cb474fbd01de834fd2a1b13fdf7db11ab72072082e45881cd16060673b59d02054b1711ae69c6e2395f6ae9214225ee7153939efcd2fa5d
'http://archive.ubuntu.com/ubuntu/pool/main/p/pixman/pixman_0.42.2-1.diff.gz' pixman_0.42.2-1.diff.gz 319616 SHA512:c475710eace38c80cc59eb1ee6eee9002525fcb30a74e647186601fd1631b09fcafde136fa45618c034be1f75baf2d07f7c78eb92ee4539100fde25f21a834f7
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

### `dpkg` source package: `postgresql-16=16.1-1build1`

Binary Packages:

- `libpq-dev=16.1-1build1`
- `libpq5:amd64=16.1-1build1`

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
$ apt-get source -qq --print-uris postgresql-16=16.1-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/p/postgresql-16/postgresql-16_16.1-1build1.dsc' postgresql-16_16.1-1build1.dsc 4211 SHA512:1c0fb283d16fe1db1693f42df970feae9eb83549488d32592ac482afdd2e91f1783f0446280603e6556ea417e4186927b2d210099b0d89bbbc24c84f13963adf
'http://archive.ubuntu.com/ubuntu/pool/main/p/postgresql-16/postgresql-16_16.1.orig.tar.bz2' postgresql-16_16.1.orig.tar.bz2 24605482 SHA512:69f4635e5841452599f13b47df41ce2425ab34b4e4582fd2c635bc78d561fa36c5b03eccb4ae6569872dc74775be1b5a62dee20c9a4f12a43339250128352918
'http://archive.ubuntu.com/ubuntu/pool/main/p/postgresql-16/postgresql-16_16.1-1build1.debian.tar.xz' postgresql-16_16.1-1build1.debian.tar.xz 30708 SHA512:fc5ea4132a86f3b3f740c2e0e7309250d57ebefce04b1782da6a93d66db0cdd71b25fea0f8b9b724eba8a9c9cb1844ec92c6eec4814f0e758702105b48bf23b3
```

### `dpkg` source package: `procps=2:4.0.4-2ubuntu1`

Binary Packages:

- `libproc2-0:amd64=2:4.0.4-2ubuntu1`
- `procps=2:4.0.4-2ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libproc2-0/copyright`, `/usr/share/doc/procps/copyright`)

- `GPL-2`
- `GPL-2.0+`
- `LGPL-2`
- `LGPL-2.0+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris procps=2:4.0.4-2ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/p/procps/procps_4.0.4-2ubuntu1.dsc' procps_4.0.4-2ubuntu1.dsc 2243 SHA512:c015c10853fa71683afa03a970a3a50e51a218f3e84c29eeb9d62bd244a9b3dd34f95f557c34049c68b63f037efe22b4e42dda2e2b1671b4d764d812318a0c25
'http://archive.ubuntu.com/ubuntu/pool/main/p/procps/procps_4.0.4.orig.tar.xz' procps_4.0.4.orig.tar.xz 1401540 SHA512:94375544e2422fefc23d7634063c49ef1be62394c46039444f85e6d2e87e45cfadc33accba5ca43c96897b4295bfb0f88d55a30204598ddb26ef66f0420cefb4
'http://archive.ubuntu.com/ubuntu/pool/main/p/procps/procps_4.0.4-2ubuntu1.debian.tar.xz' procps_4.0.4-2ubuntu1.debian.tar.xz 36848 SHA512:a29f3ed92ae85b4f2a3255f354c904b7c71dd6a58c61d1051bde7e12daf1b28a898b007a4af393e0fc2327aa36d104f5f9e50f5c93b9a32ed71df3dafa7a44d3
```

### `dpkg` source package: `python3-defaults=3.11.4-5`

Binary Packages:

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

### `dpkg` source package: `python3-stdlib-extensions=3.11.5-1`

Binary Packages:

- `python3-distutils=3.11.5-1`
- `python3-lib2to3=3.11.5-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris python3-stdlib-extensions=3.11.5-1
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3-stdlib-extensions/python3-stdlib-extensions_3.11.5-1.dsc' python3-stdlib-extensions_3.11.5-1.dsc 2563 SHA512:b050010409ad04d8fe42d25ba72cf2dd9a8a35b339aa930dcd2a3f9c72d2de32a59a6b1be0de562ce8becd759d6af051676fcee9144c8f530e81ceb683116a15
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3-stdlib-extensions/python3-stdlib-extensions_3.11.5.orig.tar.xz' python3-stdlib-extensions_3.11.5.orig.tar.xz 1784144 SHA512:1a5c65bd1675d301d08101dc4a26b8775f76db91f049bb2168ab2e3d2d9e8952d11b6301537bdec082f3333d51058b032ce7a3e8dddf97655b0f5d5e12bc09bd
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3-stdlib-extensions/python3-stdlib-extensions_3.11.5-1.debian.tar.xz' python3-stdlib-extensions_3.11.5-1.debian.tar.xz 29120 SHA512:c6be4697ce59e507c5583387d6c55a745b3475cc71c8533f85003096a2f454b342a9fed65261950caa2875c45f3af56741ea432415b10d426be5e1825a7b4220
```

### `dpkg` source package: `python3.11=3.11.7-2`

Binary Packages:

- `libpython3.11:amd64=3.11.7-2`
- `libpython3.11-minimal:amd64=3.11.7-2`
- `libpython3.11-stdlib:amd64=3.11.7-2`
- `python3.11=3.11.7-2`
- `python3.11-minimal=3.11.7-2`

Licenses: (parsed from: `/usr/share/doc/libpython3.11/copyright`, `/usr/share/doc/libpython3.11-minimal/copyright`, `/usr/share/doc/libpython3.11-stdlib/copyright`, `/usr/share/doc/python3.11/copyright`, `/usr/share/doc/python3.11-minimal/copyright`)

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
$ apt-get source -qq --print-uris python3.11=3.11.7-2
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3.11/python3.11_3.11.7-2.dsc' python3.11_3.11.7-2.dsc 3781 SHA512:00494938186192f2baf0d005d7fee091bd6b2df10aefb228123eb9e55e3f94fea8feb87c22d18f34e6b930812f6b0dc06d757b676c3d3b5d7b7e5fb67f844bdd
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3.11/python3.11_3.11.7.orig.tar.xz' python3.11_3.11.7.orig.tar.xz 20074108 SHA512:11e06f2ffe1f66888cb5b4e9f607de815294d6863a77eda6ec6d7c724ef158df9f51881f4a956d4a6fa973c2fb6fd031d495e3496e9b0bb53793fb1cc8434c63
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3.11/python3.11_3.11.7-2.debian.tar.xz' python3.11_3.11.7-2.debian.tar.xz 213720 SHA512:9da1250c07017629c98e604298e5a23d265212711f913f0ed0137337c94ce74bbe1f38142e94088cc11ed62e50f21e878859054319c9c8252fe6dd4eda219b3a
```

### `dpkg` source package: `python3.12=3.12.1-2`

Binary Packages:

- `libpython3.12-minimal:amd64=3.12.1-2`
- `libpython3.12-stdlib:amd64=3.12.1-2`
- `python3.12=3.12.1-2`
- `python3.12-minimal=3.12.1-2`

Licenses: (parsed from: `/usr/share/doc/libpython3.12-minimal/copyright`, `/usr/share/doc/libpython3.12-stdlib/copyright`, `/usr/share/doc/python3.12/copyright`, `/usr/share/doc/python3.12-minimal/copyright`)

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
$ apt-get source -qq --print-uris python3.12=3.12.1-2
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3.12/python3.12_3.12.1-2.dsc' python3.12_3.12.1-2.dsc 3812 SHA512:c3626ee5ad2426f239a5fd8e5efca3c8167d76b9471ebddcb3fc63b4afdd1a8209c4392b1d7cd65efc43b6c484b733dec8237a68a1297c2ac89cdd6538cec905
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3.12/python3.12_3.12.1.orig.tar.xz' python3.12_3.12.1.orig.tar.xz 20583448 SHA512:44cf06b89ade692d87ca3105d8e3de5c7ce3f5fb318690fff513cf56f909ff5e0d0f6a0b22ae270b12e1fe3051b1bde3ec786506ec87c810b1d02e92e45dff07
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3.12/python3.12_3.12.1-2.debian.tar.xz' python3.12_3.12.1-2.debian.tar.xz 212012 SHA512:df02f1119ad4debefa6e371ecc03cf5f2fccabbe3c30f62f8b4a66d452789482c5d86b59f67c78ba5adf7569a3895e68543ce54cacb74b8f892fc5bebf8ed3bf
```

### `dpkg` source package: `readline=8.2-3`

Binary Packages:

- `libreadline-dev:amd64=8.2-3`
- `libreadline8:amd64=8.2-3`
- `readline-common=8.2-3`

Licenses: (parsed from: `/usr/share/doc/libreadline-dev/copyright`, `/usr/share/doc/libreadline8/copyright`, `/usr/share/doc/readline-common/copyright`)

- `GFDL`
- `GFDL-NIV-1.3+`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `ISC-no-attribution`

Source:

```console
$ apt-get source -qq --print-uris readline=8.2-3
'http://archive.ubuntu.com/ubuntu/pool/main/r/readline/readline_8.2-3.dsc' readline_8.2-3.dsc 2783 SHA512:498fb4d387345d028dd5653c735a021c4354d01c61e487a57e165ddcdec6625b314823accb30dae04706b3d7d979d113a1e36534557b5b6aeb971c3ebfbaf562
'http://archive.ubuntu.com/ubuntu/pool/main/r/readline/readline_8.2.orig.tar.gz' readline_8.2.orig.tar.gz 3043952 SHA512:0a451d459146bfdeecc9cdd94bda6a6416d3e93abd80885a40b334312f16eb890f8618a27ca26868cebbddf1224983e631b1cbc002c1a4d1cd0d65fba9fea49a
'http://archive.ubuntu.com/ubuntu/pool/main/r/readline/readline_8.2-3.debian.tar.xz' readline_8.2-3.debian.tar.xz 33220 SHA512:d883b2353a7ed909792b68cf29d26a9e0befdccf538da0991b7ead1c9a22e500b1175c9af5013751b6d15bf3a957aca49d10d0ca3aae767251c600f6640dbd86
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

### `dpkg` source package: `rust-sequoia-sq=0.31.0-2`

Binary Packages:

- `sq=0.31.0-2`

Licenses: (parsed from: `/usr/share/doc/sq/copyright`)

- `GPL-2`
- `GPL-2.0-or-later`

Source:

```console
$ apt-get source -qq --print-uris rust-sequoia-sq=0.31.0-2
'http://archive.ubuntu.com/ubuntu/pool/universe/r/rust-sequoia-sq/rust-sequoia-sq_0.31.0-2.dsc' rust-sequoia-sq_0.31.0-2.dsc 3494 SHA512:f46604694238f00323decbfae2ef5758c66b9bfba9c6f54332d3c37bca3412ceefc32a6d4235ecfb99f1e47ac09ba8e6a5dec13ca362a7c45c6f82492fa25a36
'http://archive.ubuntu.com/ubuntu/pool/universe/r/rust-sequoia-sq/rust-sequoia-sq_0.31.0.orig.tar.gz' rust-sequoia-sq_0.31.0.orig.tar.gz 369161 SHA512:846ddd47c9df1a79d2ad288105d969ec15008d54566a4c2d5f7a9374501f80849b43d38841d1d29bd7cfc33f53e20cc84cc207d929dee0d43d1f5426e82ecc7d
'http://archive.ubuntu.com/ubuntu/pool/universe/r/rust-sequoia-sq/rust-sequoia-sq_0.31.0-2.debian.tar.xz' rust-sequoia-sq_0.31.0-2.debian.tar.xz 4076 SHA512:284c1a56d223b1b1bffd4a18314496d0334ab419dde5a6f17163b78ce5e766549b24dc3c92576a49aba5727ce164b379bdd29cc221b5830155c17c7040ccee4b
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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/sed/4.9-1/


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

### `dpkg` source package: `serf=1.3.10-1`

Binary Packages:

- `libserf-1-1:amd64=1.3.10-1`

Licenses: (parsed from: `/usr/share/doc/libserf-1-1/copyright`)

- `Apache`
- `Apache-2.0`
- `Zlib`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/serf/1.3.10-1/


### `dpkg` source package: `setuptools=68.1.2-2`

Binary Packages:

- `python3-pkg-resources=68.1.2-2`

Licenses: (parsed from: `/usr/share/doc/python3-pkg-resources/copyright`)

- `Apache-2.0`
- `BSD-3-clause`

Source:

```console
$ apt-get source -qq --print-uris setuptools=68.1.2-2
'http://archive.ubuntu.com/ubuntu/pool/main/s/setuptools/setuptools_68.1.2-2.dsc' setuptools_68.1.2-2.dsc 2237 SHA512:3545841976b6a590e6c2d563e4d916177e13e9d88d8f1f30d1e56f0ca6845029a2a6d2a375d9daf030130fd502a4f3f4b6343bc2c0e7e21db33294c125b8425f
'http://archive.ubuntu.com/ubuntu/pool/main/s/setuptools/setuptools_68.1.2.orig.tar.gz' setuptools_68.1.2.orig.tar.gz 2198001 SHA512:a5a84102ce72f38162b190b91286013cb8660b45f383df04fba65e38c658a5c5b93cdf05f789436618fa596b3ca6688a7c54d31d6d10b729124d3b135660c328
'http://archive.ubuntu.com/ubuntu/pool/main/s/setuptools/setuptools_68.1.2-2.debian.tar.xz' setuptools_68.1.2-2.debian.tar.xz 14160 SHA512:47d4e755985af6ce35513ff3aebf288cad0c4829b2029e82d34dd7ff56fae612bcf0312e114effe8f8609b1e85c81ca71998d5b20bc7f0d76670e6e9c0dfbbd3
```

### `dpkg` source package: `shadow=1:4.13+dfsg1-3ubuntu1`

Binary Packages:

- `login=1:4.13+dfsg1-3ubuntu1`
- `passwd=1:4.13+dfsg1-3ubuntu1`

Licenses: (parsed from: `/usr/share/doc/login/copyright`, `/usr/share/doc/passwd/copyright`)

- `BSD-3-clause`
- `GPL-1`
- `GPL-2`
- `GPL-2+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris shadow=1:4.13+dfsg1-3ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/s/shadow/shadow_4.13%2bdfsg1-3ubuntu1.dsc' shadow_4.13+dfsg1-3ubuntu1.dsc 2514 SHA512:e0712f93f9039244b3e5d9623af429723e6281985368d303b06008359c2e201d632f831f2cf2f318472c90d437c5467f2651995bb0f63275b4f5aa071213918e
'http://archive.ubuntu.com/ubuntu/pool/main/s/shadow/shadow_4.13%2bdfsg1.orig.tar.xz' shadow_4.13+dfsg1.orig.tar.xz 1811752 SHA512:27106ca26d6e4c9e5833cf79811b10f656ade547bbc18b87faf79bbe0581a9e1467cbb6c354320e2d5233d17208d77742ebf197d32b6d2f08439e37e368ded1d
'http://archive.ubuntu.com/ubuntu/pool/main/s/shadow/shadow_4.13%2bdfsg1-3ubuntu1.debian.tar.xz' shadow_4.13+dfsg1-3ubuntu1.debian.tar.xz 94664 SHA512:931b99eefca127b84d1fb16ede72dfd3c1a20584d8d871fd0a8c857fdfb5c70188e0d02cde25d0fb67e58ccc94d39a34fb69f2954149ab06f2a190c87be43a4c
```

### `dpkg` source package: `shared-mime-info=2.4-1`

Binary Packages:

- `shared-mime-info=2.4-1`

Licenses: (parsed from: `/usr/share/doc/shared-mime-info/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris shared-mime-info=2.4-1
'http://archive.ubuntu.com/ubuntu/pool/main/s/shared-mime-info/shared-mime-info_2.4-1.dsc' shared-mime-info_2.4-1.dsc 2226 SHA512:12ee2e598fba93eb22b5c9c4f375950376568bdfad39aad03741ee08dd10b9604a94cad63015f3b61ae838c8e2e50a2e890117b52514169a73f286445589c2fe
'http://archive.ubuntu.com/ubuntu/pool/main/s/shared-mime-info/shared-mime-info_2.4.orig.tar.bz2' shared-mime-info_2.4.orig.tar.bz2 7096347 SHA512:712f414e80919bf2a0f5083ced44c54a350948a526850466a6e9f35365dcfd97fad8bcdbb29945de2715a8f9b70a108e931c8500209a4d6e3dddf97af02771cb
'http://archive.ubuntu.com/ubuntu/pool/main/s/shared-mime-info/shared-mime-info_2.4-1.debian.tar.xz' shared-mime-info_2.4-1.debian.tar.xz 10272 SHA512:e36261436147ad5607b324de732d6f4ca7139850ddba6f153af0d2f48e05b2f0d1d923994c6d3ab4d9c3bc46abc1754040ba099fcfae7b1ddf900d791b4a027f
```

### `dpkg` source package: `sqlite3=3.44.2-1`

Binary Packages:

- `libsqlite3-0:amd64=3.44.2-1`
- `libsqlite3-dev:amd64=3.44.2-1`

Licenses: (parsed from: `/usr/share/doc/libsqlite3-0/copyright`, `/usr/share/doc/libsqlite3-dev/copyright`)

- `GPL-2`
- `GPL-2+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris sqlite3=3.44.2-1
'http://archive.ubuntu.com/ubuntu/pool/main/s/sqlite3/sqlite3_3.44.2-1.dsc' sqlite3_3.44.2-1.dsc 2486 SHA512:893a7f753287b73d0edf8cb322ac15f9fcdac68cab7f88af80bf37c7baba459ed5469764f2f8fb0b2047a22282cccbac99abe5f0dc4ac1ae5c850ce529656ae6
'http://archive.ubuntu.com/ubuntu/pool/main/s/sqlite3/sqlite3_3.44.2.orig-www.tar.xz' sqlite3_3.44.2.orig-www.tar.xz 5671432 SHA512:9e8528fcfc5fa5311e24b956dd914af59f0f7616e423655e78a03351acf6d5d784b7d473c35aefcbfbcd216bcedbc8e26ce03c33f4ebed62d2f36e1f4ecad8a7
'http://archive.ubuntu.com/ubuntu/pool/main/s/sqlite3/sqlite3_3.44.2.orig.tar.xz' sqlite3_3.44.2.orig.tar.xz 8214772 SHA512:cfb4e82a375e5a53d5484f004d2b5615876e1cad1c7d31ffabb417cc61609137aab674ec47f148f825e45ceaa51cb5bf005de73005535d42f6ed61ad499331d9
'http://archive.ubuntu.com/ubuntu/pool/main/s/sqlite3/sqlite3_3.44.2-1.debian.tar.xz' sqlite3_3.44.2-1.debian.tar.xz 30200 SHA512:56de940549987ba7e0e8c6f9874e772ff4bb4a9b196da3281e13233c1ceb402a4decf33359c19f994d4faa84e2198e61e4bf7c9b611029513265ae7a6f81b733
```

### `dpkg` source package: `subversion=1.14.3-1`

Binary Packages:

- `libsvn1:amd64=1.14.3-1`
- `subversion=1.14.3-1`

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
$ apt-get source -qq --print-uris subversion=1.14.3-1
'http://archive.ubuntu.com/ubuntu/pool/universe/s/subversion/subversion_1.14.3-1.dsc' subversion_1.14.3-1.dsc 4046 SHA512:11775c8182a8940786e2d686a8eb8d25851d2b7baabb9e1910a8321d1c875c6b66980b88735ef3576a59265a7eb6f168a22404c430581a0dacd22f6ff4816c51
'http://archive.ubuntu.com/ubuntu/pool/universe/s/subversion/subversion_1.14.3.orig.tar.gz' subversion_1.14.3.orig.tar.gz 11621442 SHA512:12188a1c07b8b72594d27b1058c13b2ab81d0306d6da2853400be5a73f12ac5d5ff5ae80b6bfd0320e58d8d797b813d71d6c688ba230d3a010ebaf8bdd910c13
'http://archive.ubuntu.com/ubuntu/pool/universe/s/subversion/subversion_1.14.3.orig.tar.gz.asc' subversion_1.14.3.orig.tar.gz.asc 1724 SHA512:d3922207f672cf17446ce05aa1c7361f4c15279fd1182f7c44cab18be63b086cbac4f22830377f8a4e6ca3cc130dfd5cccaa5536c190b5ac8d786af6ecb7ef30
'http://archive.ubuntu.com/ubuntu/pool/universe/s/subversion/subversion_1.14.3-1.debian.tar.xz' subversion_1.14.3-1.debian.tar.xz 336856 SHA512:9639a8f6cff9e54f3226b30623e4e2bc763dde542ebd46ad12f27abfcb2c26e6f9abdf74fb134b62e7750f5e88697ba5453bcbc3e24c36ce0a19f04080c4fa17
```

### `dpkg` source package: `systemd=253.5-1ubuntu7`

Binary Packages:

- `libsystemd0:amd64=253.5-1ubuntu7`
- `libudev1:amd64=253.5-1ubuntu7`

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
$ apt-get source -qq --print-uris systemd=253.5-1ubuntu7
'http://archive.ubuntu.com/ubuntu/pool/main/s/systemd/systemd_253.5-1ubuntu7.dsc' systemd_253.5-1ubuntu7.dsc 6902 SHA512:d54dd5f36a6b7b71a67c758bddaafcf3025988484c3d3fcc5ba6abdcb2e030bb960507af89275d33c96abc9a8951eed5daf6f7910baeeaf30c4ea76cf6bcfd28
'http://archive.ubuntu.com/ubuntu/pool/main/s/systemd/systemd_253.5.orig.tar.gz' systemd_253.5.orig.tar.gz 12015672 SHA512:39709b485cd9287e26ac8e973fa1692b280bec3b96e1da6667e4a4f2ac2228aa072b22802720a254698d32c82f5306d7feb32229e4b6d54cc0e2b1e2caa4cc2e
'http://archive.ubuntu.com/ubuntu/pool/main/s/systemd/systemd_253.5-1ubuntu7.debian.tar.xz' systemd_253.5-1ubuntu7.debian.tar.xz 220320 SHA512:6fab6e06ee154f9ae84bef0f6c5775be759dee368a695f1b7e23d865c72cbf524499610fe0678f97ab943bd7c78143d5f06aa5fa8e1aafb8089aeb0f78854da6
```

### `dpkg` source package: `sysvinit=3.08-3ubuntu1`

Binary Packages:

- `sysvinit-utils=3.08-3ubuntu1`

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
$ apt-get source -qq --print-uris sysvinit=3.08-3ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/s/sysvinit/sysvinit_3.08-3ubuntu1.dsc' sysvinit_3.08-3ubuntu1.dsc 2495 SHA512:d204847d567b6b367005b9aa6746e7993ad811ac7fec85cc2a15d80ad06d1c01b37d2b518c0d21c2a2598b3a317fe537a86cb7546b7564cb6b37a9337b99d5aa
'http://archive.ubuntu.com/ubuntu/pool/main/s/sysvinit/sysvinit_3.08.orig.tar.gz' sysvinit_3.08.orig.tar.gz 513674 SHA512:63ed7ebd50944adce1a35af7798d0e2d6248f36a606f63bb7a567424555ec33e83c33b897528c801b4b4ac61b24d2a3555c9a690031c50a94e7ead83f37f8e96
'http://archive.ubuntu.com/ubuntu/pool/main/s/sysvinit/sysvinit_3.08-3ubuntu1.debian.tar.xz' sysvinit_3.08-3ubuntu1.debian.tar.xz 139156 SHA512:46c99bc70a9e9d4f5d3edcd16966ee046be3f26b34d47f7cb101b3e15ca50c1dd0fc3877c33ecc6bdd948d74a91cfc387c40ecdb019e966370f42233a965bca3
```

### `dpkg` source package: `tar=1.34+dfsg-1.4`

Binary Packages:

- `tar=1.34+dfsg-1.4`

Licenses: (parsed from: `/usr/share/doc/tar/copyright`)

- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `GPL-3+ with Bison exception`
- `LGPL-3`
- `LGPL-3+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/tar/1.34+dfsg-1.4/


### `dpkg` source package: `tiff=4.5.1+git230720-1ubuntu1`

Binary Packages:

- `libtiff-dev:amd64=4.5.1+git230720-1ubuntu1`
- `libtiff6:amd64=4.5.1+git230720-1ubuntu1`
- `libtiffxx6:amd64=4.5.1+git230720-1ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libtiff-dev/copyright`, `/usr/share/doc/libtiff6/copyright`, `/usr/share/doc/libtiffxx6/copyright`)

- `Hylafax`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `tzdata=2023d-1ubuntu1`

Binary Packages:

- `tzdata=2023d-1ubuntu1`

Licenses: (parsed from: `/usr/share/doc/tzdata/copyright`)

- `ICU`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris tzdata=2023d-1ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/t/tzdata/tzdata_2023d-1ubuntu1.dsc' tzdata_2023d-1ubuntu1.dsc 2675 SHA512:36f31007453fd296aff7da93a419a3d3905c9f8accc3f5daf2b5ec8cd7f5a5b8f5fe0fb10db68cd576f3cf69ef6022cb22d6fcf4d82a34b21d9803577aeae212
'http://archive.ubuntu.com/ubuntu/pool/main/t/tzdata/tzdata_2023d.orig.tar.gz' tzdata_2023d.orig.tar.gz 449767 SHA512:81832b2d738c28cecbcb3906cc07568c5ae574adc9de35b25d4bf613581c92d471d67213b4261a56f0ec02efcf211b4e298b7e1dc367c972e726b0a2e9498df4
'http://archive.ubuntu.com/ubuntu/pool/main/t/tzdata/tzdata_2023d.orig.tar.gz.asc' tzdata_2023d.orig.tar.gz.asc 833 SHA512:3266f0ad4e05365fb09d48b9baeb884447cc4c16ecd4f0d2bf5f25b0aabe03b48fca11c19379a45545dc4f41acc68633c624d99d2700f439d9233ecab6d1f184
'http://archive.ubuntu.com/ubuntu/pool/main/t/tzdata/tzdata_2023d-1ubuntu1.debian.tar.xz' tzdata_2023d-1ubuntu1.debian.tar.xz 183520 SHA512:826d410372b739375fdf28bd7f7a045c3de088acf62b92a2feb0b6e5f039845826fa065bc467ea82fccf93fa71895f5bdbdde40c18a366f6823c67ac7a16393f
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

### `dpkg` source package: `ucf=3.0043+nmu1`

Binary Packages:

- `ucf=3.0043+nmu1`

Licenses: (parsed from: `/usr/share/doc/ucf/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris ucf=3.0043+nmu1
'http://archive.ubuntu.com/ubuntu/pool/main/u/ucf/ucf_3.0043%2bnmu1.dsc' ucf_3.0043+nmu1.dsc 1567 SHA512:608423c255fa2c1072bcaa9c71addd0f393f008ebd321ef4939ed4d714aa43bea4c90979fa5817c19e3d7355415cc70aa8c80ff79760b4286411cfbd58242d77
'http://archive.ubuntu.com/ubuntu/pool/main/u/ucf/ucf_3.0043%2bnmu1.tar.xz' ucf_3.0043+nmu1.tar.xz 70916 SHA512:8949f197f6aec35ef7ff8c076ed9f863ef369c65de1a17947445c7182623393633e0094e882d50eadbb0435bf03b9a5cb5d11b6e3bd40e33d5d7b15425583b38
```

### `dpkg` source package: `unzip=6.0-28ubuntu1`

Binary Packages:

- `unzip=6.0-28ubuntu1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris unzip=6.0-28ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/u/unzip/unzip_6.0-28ubuntu1.dsc' unzip_6.0-28ubuntu1.dsc 1836 SHA512:d3e4624dcb937521ba0abf8696c7641877d752738e90ae62f62534220ad7d95c88885ed9619ada67b0b00c39c6de2deb703dceb2ec085ab1c090a1f0779296a4
'http://archive.ubuntu.com/ubuntu/pool/main/u/unzip/unzip_6.0.orig.tar.gz' unzip_6.0.orig.tar.gz 1376845 SHA512:0694e403ebc57b37218e00ec1a406cae5cc9c5b52b6798e0d4590840b6cdbf9ddc0d9471f67af783e960f8fa2e620394d51384257dca23d06bcd90224a80ce5d
'http://archive.ubuntu.com/ubuntu/pool/main/u/unzip/unzip_6.0-28ubuntu1.debian.tar.xz' unzip_6.0-28ubuntu1.debian.tar.xz 28440 SHA512:1a73f1dfc8cdc0e904618461327959d27342e75cf613a8129bb664e3704b3afe1de942960a676e4eff4a6bbfbef3f6b77c94b46f79b6a035413461a11a854146
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

### `dpkg` source package: `utf8proc=2.9.0-1`

Binary Packages:

- `libutf8proc3:amd64=2.9.0-1`

Licenses: (parsed from: `/usr/share/doc/libutf8proc3/copyright`)

- `Expat`
- `Unicode`

Source:

```console
$ apt-get source -qq --print-uris utf8proc=2.9.0-1
'http://archive.ubuntu.com/ubuntu/pool/universe/u/utf8proc/utf8proc_2.9.0-1.dsc' utf8proc_2.9.0-1.dsc 2187 SHA512:0ed1c0f94a5bbaa463b51f660bb306255898a579ce4eb3aaca9d47d582c0558fc23ce24243713cbd1e39441e72852796032e1395e3fa3866bbcb83d7062e5c35
'http://archive.ubuntu.com/ubuntu/pool/universe/u/utf8proc/utf8proc_2.9.0.orig.tar.gz' utf8proc_2.9.0.orig.tar.gz 193465 SHA512:544ed59812279af4135e5622e2e77b3f067765df819cf8b78e679dfc481e9baa5a357a33c40426c5053c1d5107109e3c4c191ed83f3f7c4a6b1769d04b17715c
'http://archive.ubuntu.com/ubuntu/pool/universe/u/utf8proc/utf8proc_2.9.0-1.debian.tar.xz' utf8proc_2.9.0-1.debian.tar.xz 5836 SHA512:2d2da5edc18932e7467c29d429ad11691555077ba120813cb94a41806464687e7f7165fd6a65f33630a4ac2e9dd2ae2e832be8cbb03f462b4aeef0a4086d4de6
```

### `dpkg` source package: `util-linux=2.39.2-6ubuntu1`

Binary Packages:

- `bsdutils=1:2.39.2-6ubuntu1`
- `libblkid-dev:amd64=2.39.2-6ubuntu1`
- `libblkid1:amd64=2.39.2-6ubuntu1`
- `libmount-dev:amd64=2.39.2-6ubuntu1`
- `libmount1:amd64=2.39.2-6ubuntu1`
- `libsmartcols1:amd64=2.39.2-6ubuntu1`
- `libuuid1:amd64=2.39.2-6ubuntu1`
- `mount=2.39.2-6ubuntu1`
- `util-linux=2.39.2-6ubuntu1`
- `uuid-dev:amd64=2.39.2-6ubuntu1`

Licenses: (parsed from: `/usr/share/doc/bsdutils/copyright`, `/usr/share/doc/libblkid-dev/copyright`, `/usr/share/doc/libblkid1/copyright`, `/usr/share/doc/libmount-dev/copyright`, `/usr/share/doc/libmount1/copyright`, `/usr/share/doc/libsmartcols1/copyright`, `/usr/share/doc/libuuid1/copyright`, `/usr/share/doc/mount/copyright`, `/usr/share/doc/util-linux/copyright`, `/usr/share/doc/uuid-dev/copyright`)

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
$ apt-get source -qq --print-uris util-linux=2.39.2-6ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/u/util-linux/util-linux_2.39.2-6ubuntu1.dsc' util-linux_2.39.2-6ubuntu1.dsc 4711 SHA512:a0fb49b3257ae4564fbb29f39c5b1152f0d327ccd7325125f70e1c73e8716ce6fe3985fca260b950baacfb49d6a70250f5ca33468c3b04dc75445abca4d64f73
'http://archive.ubuntu.com/ubuntu/pool/main/u/util-linux/util-linux_2.39.2.orig.tar.xz' util-linux_2.39.2.orig.tar.xz 8362220 SHA512:cebecdd62749d0aeea2c4faf7ad1606426eff03ef3b15cd9c2df1126f216a4ed546d8fc3218c649fa95944eb87a98bb6a7cdd0bea31057c481c5cf608ffc19a3
'http://archive.ubuntu.com/ubuntu/pool/main/u/util-linux/util-linux_2.39.2-6ubuntu1.debian.tar.xz' util-linux_2.39.2-6ubuntu1.debian.tar.xz 105504 SHA512:cb91c7b60ebd4359ba554f4099ecc42fea4a30d3427123b1d76156f455ccd641da4baf457f09535400569f590da9d83378541214da1b93be8154865f89efb906
```

### `dpkg` source package: `wget=1.21.4-1ubuntu1`

Binary Packages:

- `wget=1.21.4-1ubuntu1`

Licenses: (parsed from: `/usr/share/doc/wget/copyright`)

- `GFDL-1.2`
- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris wget=1.21.4-1ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/w/wget/wget_1.21.4-1ubuntu1.dsc' wget_1.21.4-1ubuntu1.dsc 2243 SHA512:6df457a879e59d52f56002a856f1932e68decaf445b7bb6aba4e1eeb292ecf78d3de6aadf7d4a0a384617bb6eda8c4b308db30ddfaf4c3ee0ac91ada1938a38f
'http://archive.ubuntu.com/ubuntu/pool/main/w/wget/wget_1.21.4.orig.tar.gz' wget_1.21.4.orig.tar.gz 5059591 SHA512:7a1539045174f6b97ab6980811c2ac1799edc20db72987b5ba9b1710cffb19669a7736813d15c8da3aa2d4a384246ff946b77ecb0baeb6fd3e12ae591f1bf6a3
'http://archive.ubuntu.com/ubuntu/pool/main/w/wget/wget_1.21.4.orig.tar.gz.asc' wget_1.21.4.orig.tar.gz.asc 854 SHA512:72603493c2d799dca08700175a2010d8736fd6d3cb9bea3987db8814e9f133ab0fbd1477892115f7fbbd1a7d4d416ec370bdbff6dbe8f00d1eea84f0c4f8d84b
'http://archive.ubuntu.com/ubuntu/pool/main/w/wget/wget_1.21.4-1ubuntu1.debian.tar.xz' wget_1.21.4-1ubuntu1.debian.tar.xz 63836 SHA512:3b4bd4d287a2aa772afec2f4ec737f96b020cffa9410e296264d41328869bf99669d4ec270b4bc5565d0f6b8a4802a3304ff88069084ef97b9394094b4ab15ea
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

### `dpkg` source package: `xorg=1:7.7+23ubuntu2`

Binary Packages:

- `x11-common=1:7.7+23ubuntu2`

Licenses: (parsed from: `/usr/share/doc/x11-common/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris xorg=1:7.7+23ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/x/xorg/xorg_7.7%2b23ubuntu2.dsc' xorg_7.7+23ubuntu2.dsc 2095 SHA512:f4befc0dd73c66f56856f16c4dc4051f58af50bd8819469df4bb309817952e00f2f4e29776282f85eeaef18a77fdd42cb1cfcb9a69432c4680b216039b37e480
'http://archive.ubuntu.com/ubuntu/pool/main/x/xorg/xorg_7.7%2b23ubuntu2.tar.gz' xorg_7.7+23ubuntu2.tar.gz 301762 SHA512:379e60ab57cc4f9adbf1f59295fca3930bbd638f4100d08c9f1f78bd6ef063e3396385b841e66389771c4ba5825875d738b9aa4b4dc2e3f79d0537415ac0852a
```

### `dpkg` source package: `xorgproto=2023.2-1`

Binary Packages:

- `x11proto-core-dev=2023.2-1`
- `x11proto-dev=2023.2-1`

Licenses: (parsed from: `/usr/share/doc/x11proto-core-dev/copyright`, `/usr/share/doc/x11proto-dev/copyright`)

- `MIT`
- `SGI`

Source:

```console
$ apt-get source -qq --print-uris xorgproto=2023.2-1
'http://archive.ubuntu.com/ubuntu/pool/main/x/xorgproto/xorgproto_2023.2-1.dsc' xorgproto_2023.2-1.dsc 3336 SHA512:d6459c917da1e6cc44e5661744780998f1cd3663dafb70621d304b6bc5113a6bd1d16f13a2b13739b065ea8fbf535096a3d1f0a5e9d145d823a86610baa247a4
'http://archive.ubuntu.com/ubuntu/pool/main/x/xorgproto/xorgproto_2023.2.orig.tar.gz' xorgproto_2023.2.orig.tar.gz 1150326 SHA512:9f03dcf7b2e7363523cdae6618f7c7db0041335aad505e0322571c391f2ef294957012a755b70e1dd24c3c0178e0423a36554032f552786d724eb9be31891436
'http://archive.ubuntu.com/ubuntu/pool/main/x/xorgproto/xorgproto_2023.2.orig.tar.gz.asc' xorgproto_2023.2.orig.tar.gz.asc 195 SHA512:bf84acc1adc37a2fe17193dec431a628980707200d8dd571c85f009bd5218d5470b3ac76d31756d10551dc75dfcfc791ec262c933837d0b8554181c2b99893b5
'http://archive.ubuntu.com/ubuntu/pool/main/x/xorgproto/xorgproto_2023.2-1.diff.gz' xorgproto_2023.2-1.diff.gz 25092 SHA512:ce40310bb67106bfe53052506d277c94e5a16a0c82a20e43944cdf57de1c724bc88af72aff3cd946f4d1f8527bc898f2d43ed9caa4d02a9dbf0647b6e3f3c798
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

### `dpkg` source package: `xxhash=0.8.2-2`

Binary Packages:

- `libxxhash0:amd64=0.8.2-2`

Licenses: (parsed from: `/usr/share/doc/libxxhash0/copyright`)

- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris xxhash=0.8.2-2
'http://archive.ubuntu.com/ubuntu/pool/main/x/xxhash/xxhash_0.8.2-2.dsc' xxhash_0.8.2-2.dsc 1969 SHA512:7922828f526e6ab7b421a3e3a7a45090fd64b5712e43df49597ed4dad0aa28c973c4b428d06cb9905b881f2c428caeac4d7d5538bf68c69c72662435fe64e5de
'http://archive.ubuntu.com/ubuntu/pool/main/x/xxhash/xxhash_0.8.2.orig.tar.gz' xxhash_0.8.2.orig.tar.gz 1141188 SHA512:3e3eef21432fe88bc4dd9940ccad0308fdea3537b06fa5ac0e74c1bde53413dff29c8b3fc617a8a42b9ce88fcf213311d338a31b1ce73b3729342c9e68f06c78
'http://archive.ubuntu.com/ubuntu/pool/main/x/xxhash/xxhash_0.8.2-2.debian.tar.xz' xxhash_0.8.2-2.debian.tar.xz 4920 SHA512:a88c7e6e538504d31e737feb21fd8af2d57537756bd2ecc5f5396349f3ed20ff87287602e5bcce04f67564a00b192de6b4a70b61c87d641a31248604bf1982b0
```

### `dpkg` source package: `xz-utils=5.4.5-0.3`

Binary Packages:

- `liblzma-dev:amd64=5.4.5-0.3`
- `liblzma5:amd64=5.4.5-0.3`
- `xz-utils=5.4.5-0.3`

Licenses: (parsed from: `/usr/share/doc/liblzma-dev/copyright`, `/usr/share/doc/liblzma5/copyright`, `/usr/share/doc/xz-utils/copyright`)

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
$ apt-get source -qq --print-uris xz-utils=5.4.5-0.3
'http://archive.ubuntu.com/ubuntu/pool/main/x/xz-utils/xz-utils_5.4.5-0.3.dsc' xz-utils_5.4.5-0.3.dsc 2720 SHA512:0af36bb4429ceb470975b3ff20b6e455aad41c3a22754bf5d93885aa79d8699db3c00b2613a9d22ccc936f0f96687190c74c5a4f53e694906b7edc103f2da6b9
'http://archive.ubuntu.com/ubuntu/pool/main/x/xz-utils/xz-utils_5.4.5.orig.tar.xz' xz-utils_5.4.5.orig.tar.xz 1680520 SHA512:5cbc3b5bb35a9f5773ad657788fe77013471e3b621c5a8149deb7389d48535926e5bed103456fcfe5ecb044b236b1055b03938a6cc877cfc749372b899fc79e5
'http://archive.ubuntu.com/ubuntu/pool/main/x/xz-utils/xz-utils_5.4.5.orig.tar.xz.asc' xz-utils_5.4.5.orig.tar.xz.asc 833 SHA512:7390e991d6eccc8bb2fd3d319fcde92df0abcdc163bd0210a1d5f6c7a80268f36ead88ce1ae1d6935084f608b515ed1cd87c30085fcc2ee9222fc78c4a37ddbb
'http://archive.ubuntu.com/ubuntu/pool/main/x/xz-utils/xz-utils_5.4.5-0.3.debian.tar.xz' xz-utils_5.4.5-0.3.debian.tar.xz 26944 SHA512:ec4ca5251586aebd86dfe2ed564a078e58658c5cc6f866691971ba294a735ba7bc00b4eae678794683197e7f92f532226c0fda5534701377a79ad5c3623f754d
```

### `dpkg` source package: `zlib=1:1.3.dfsg-3ubuntu1`

Binary Packages:

- `zlib1g:amd64=1:1.3.dfsg-3ubuntu1`
- `zlib1g-dev:amd64=1:1.3.dfsg-3ubuntu1`

Licenses: (parsed from: `/usr/share/doc/zlib1g/copyright`, `/usr/share/doc/zlib1g-dev/copyright`)

- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris zlib=1:1.3.dfsg-3ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/z/zlib/zlib_1.3.dfsg-3ubuntu1.dsc' zlib_1.3.dfsg-3ubuntu1.dsc 3095 SHA512:f1decbdaccf4fe93258fb7bf639da9d5687e1b597006be8432709e3fcf97fa9b5b42afd4693e5e0ecace0e6a5358f105ee587440173aae405672557f4208e903
'http://archive.ubuntu.com/ubuntu/pool/main/z/zlib/zlib_1.3.dfsg.orig.tar.xz' zlib_1.3.dfsg.orig.tar.xz 1128572 SHA512:be6f020c691c61fe4ddcb27d3f8b2515435f544177e0b97286b5e85afc3862c1de6cd74a14ff6b065d620d046d35bf029fabfd1cf473f43a2cad60bf9ad55afe
'http://archive.ubuntu.com/ubuntu/pool/main/z/zlib/zlib_1.3.dfsg-3ubuntu1.debian.tar.xz' zlib_1.3.dfsg-3ubuntu1.debian.tar.xz 60544 SHA512:7cae3c176d6ba672edee2b70f1087bebc2a7f4a036c7132d65e83e6794e8245e1c3a92e6258dae231ee33c33cf2f09c3b4f4788d794b84a798d63b7938eed487
```
