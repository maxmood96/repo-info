# `buildpack-deps:noble-scm`

## Docker Metadata

- Image ID: `sha256:612678d4ea5037c12149c14ef1ebc742351224680e67be24b209970346cc7975`
- Created: `2024-02-02T06:18:18.634777296Z`
- Virtual Size: ~ 249.60 Mb  
  (total size of all layers on-disk)
- Arch: `linux`/`amd64`
- Command: `["/bin/bash"]`
- Environment:
  - `PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin`
- Labels:
  - `org.opencontainers.image.ref.name=ubuntu`
  - `org.opencontainers.image.version=24.04`

## `dpkg` (`.deb`-based packages)

### `dpkg` source package: `acl=2.3.1-4ubuntu1`

Binary Packages:

- `libacl1:amd64=2.3.1-4ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libacl1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2+`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris acl=2.3.1-4ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/a/acl/acl_2.3.1-4ubuntu1.dsc' acl_2.3.1-4ubuntu1.dsc 2649 SHA512:aebbd66e0ae95d321b46a9c8c3e81679aae434bdb1600812e5ec381d48ec11ce80140e0b6b6ede95c5faa87f06ec157d1c56d44d81640c5c9c9f50866d7ef303
'http://archive.ubuntu.com/ubuntu/pool/main/a/acl/acl_2.3.1.orig.tar.xz' acl_2.3.1.orig.tar.xz 355676 SHA512:7d02f05d17305f8587ab485395b00c7fdb8e44c1906d0d04b70a43a3020803e8b2b8c707abb6147f794867dfa87bd51769c2d3e11a3db55ecbd2006a6e6231dc
'http://archive.ubuntu.com/ubuntu/pool/main/a/acl/acl_2.3.1.orig.tar.xz.asc' acl_2.3.1.orig.tar.xz.asc 833 SHA512:be046f3bf1ac7e21d2a07bf6ea87c1fedeed2f9d370d8bf3de1aa0c448de5484b1523697415849b6b7ca23e48e3df5353f6aebe850eb20fc2044d2681c71f298
'http://archive.ubuntu.com/ubuntu/pool/main/a/acl/acl_2.3.1-4ubuntu1.debian.tar.xz' acl_2.3.1-4ubuntu1.debian.tar.xz 31452 SHA512:7c1b22e30196f25e69eef3bb7948ee3c6432ea4fbfd6befaa6f0b246d551d0093e61ecc12adcedb0114210fcd1c4dff500e8c0675a688b5d4a2f562c14d8c7bd
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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/apt/2.7.6/


### `dpkg` source package: `attr=1:2.5.2-1`

Binary Packages:

- `libattr1:amd64=1:2.5.2-1`

Licenses: (parsed from: `/usr/share/doc/libattr1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2+`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris attr=1:2.5.2-1
'http://archive.ubuntu.com/ubuntu/pool/main/a/attr/attr_2.5.2-1.dsc' attr_2.5.2-1.dsc 2477 SHA512:27eb1cb4556d1e0f6cbc0cffe1bb9ff23008e3db7b7b70806b69b6e4f2e5f75645a9520499bc34545e760126410ac57e6aade61596afc19d646768219e9c8534
'http://archive.ubuntu.com/ubuntu/pool/main/a/attr/attr_2.5.2.orig.tar.xz' attr_2.5.2.orig.tar.xz 334180 SHA512:f587ea544effb7cfed63b3027bf14baba2c2dbe3a9b6c0c45fc559f7e8cb477b3e9a4a826eae30f929409468c50d11f3e7dc6d2500f41e1af8662a7e96a30ef3
'http://archive.ubuntu.com/ubuntu/pool/main/a/attr/attr_2.5.2.orig.tar.xz.asc' attr_2.5.2.orig.tar.xz.asc 833 SHA512:16362013313d055dec307bcf755a9846f5153a78309a499f8cac4ff57a2154de2bc8f3b1400e81dba7a0bf0c67aa02a5d464898ed6e4aa721b64ec95fd313968
'http://archive.ubuntu.com/ubuntu/pool/main/a/attr/attr_2.5.2-1.debian.tar.xz' attr_2.5.2-1.debian.tar.xz 25848 SHA512:a37ab31ebedc533a4fc18ef3d755855f7ba1d819c65f5cd21778ccf787ed8fd675c96f3a99f56bb53ef441b7d7ebc5d521db65967fdad2410e1397c86efc7cca
```

### `dpkg` source package: `audit=1:3.1.2-2`

Binary Packages:

- `libaudit-common=1:3.1.2-2`
- `libaudit1:amd64=1:3.1.2-2`

Licenses: (parsed from: `/usr/share/doc/libaudit-common/copyright`, `/usr/share/doc/libaudit1/copyright`)

- `GPL-1`
- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris audit=1:3.1.2-2
'http://archive.ubuntu.com/ubuntu/pool/main/a/audit/audit_3.1.2-2.dsc' audit_3.1.2-2.dsc 2403 SHA512:c30f758ebdfaec781e1963d588542b050d0fc5aa6482b92ef884dbef2c3f0ece0ad95c59198397a8063aebc82a4b5fdee4123a569e1299d8e41c5f02be3243ff
'http://archive.ubuntu.com/ubuntu/pool/main/a/audit/audit_3.1.2.orig.tar.gz' audit_3.1.2.orig.tar.gz 1219860 SHA512:a97003a294ed3671df01e2952688e7d5eef59a35f6891feb53e67c4c7eab9ae8c2d18de41a5b5b20e0ad7156fac93aec05f32f6bc5eea706b42b6f27f676446a
'http://archive.ubuntu.com/ubuntu/pool/main/a/audit/audit_3.1.2-2.debian.tar.xz' audit_3.1.2-2.debian.tar.xz 18340 SHA512:efbde22d4859d2a3ecaa943d7536e85b222dd7d9fa8901507baa75577d91c64d4f7024aafda0744f5c968541a19f0d93e185fa2ab71dbeb7ab5f4004dc9386bf
```

### `dpkg` source package: `base-files=13ubuntu6`

Binary Packages:

- `base-files=13ubuntu6`

Licenses: (parsed from: `/usr/share/doc/base-files/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris base-files=13ubuntu6
'http://archive.ubuntu.com/ubuntu/pool/main/b/base-files/base-files_13ubuntu6.dsc' base-files_13ubuntu6.dsc 1654 SHA512:fbd25912c734c241c3353c66f391479df58f97fabf491e2a7c66453f8542574066830c98e1f94d88dd0fd77422e0c7377fbb71a2bd9a455b9534d90e78b600bf
'http://archive.ubuntu.com/ubuntu/pool/main/b/base-files/base-files_13ubuntu6.tar.xz' base-files_13ubuntu6.tar.xz 93196 SHA512:915c5c158c31ddf2b217b050d0102093629f89e61f0c91e53876297dbe91fa04136f516b6db2f655e757be6b5e652a886462eb4b2c8868fb75c8c419f740e8ab
```

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

### `dpkg` source package: `brotli=1.1.0-2`

Binary Packages:

- `libbrotli1:amd64=1.1.0-2`

Licenses: (parsed from: `/usr/share/doc/libbrotli1/copyright`)

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

### `dpkg` source package: `coreutils=9.4-2ubuntu2`

Binary Packages:

- `coreutils=9.4-2ubuntu2`

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
$ apt-get source -qq --print-uris coreutils=9.4-2ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/c/coreutils/coreutils_9.4-2ubuntu2.dsc' coreutils_9.4-2ubuntu2.dsc 2061 SHA512:f2f76a54259e5789aa715442aaf3fe7feab5675648cd7c79fa2e14fb7534722917e7c774fab47ee62b584a472325632171de7c0fe2242025eba19367e4c112fa
'http://archive.ubuntu.com/ubuntu/pool/main/c/coreutils/coreutils_9.4.orig.tar.xz' coreutils_9.4.orig.tar.xz 5979200 SHA512:7c55ee23b685a0462bbbd118b04d25278c902604a0dcf3bf4f8bf81faa0500dee5a7813cba6f586d676c98e520cafd420f16479619305e94ea6798d8437561f5
'http://archive.ubuntu.com/ubuntu/pool/main/c/coreutils/coreutils_9.4-2ubuntu2.debian.tar.xz' coreutils_9.4-2ubuntu2.debian.tar.xz 39368 SHA512:a52b2c1b6aef60a5fe70d741df1aab61fea459979f5aebaf8fd4de951963c34016a0ef0de470ecc7aa393bd1a9274f34d0799da049193a2007afab78c9e75a81
```

### `dpkg` source package: `curl=8.5.0-2ubuntu1`

Binary Packages:

- `curl=8.5.0-2ubuntu1`
- `libcurl3-gnutls:amd64=8.5.0-2ubuntu1`
- `libcurl4:amd64=8.5.0-2ubuntu1`

Licenses: (parsed from: `/usr/share/doc/curl/copyright`, `/usr/share/doc/libcurl3-gnutls/copyright`, `/usr/share/doc/libcurl4/copyright`)

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

### `dpkg` source package: `db5.3=5.3.28+dfsg2-4`

Binary Packages:

- `libdb5.3:amd64=5.3.28+dfsg2-4`

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

### `dpkg` source package: `debianutils=5.16`

Binary Packages:

- `debianutils=5.16`

Licenses: (parsed from: `/usr/share/doc/debianutils/copyright`)

- `GPL-2`
- `GPL-2+`
- `SMAIL-GPL`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris debianutils=5.16
'http://archive.ubuntu.com/ubuntu/pool/main/d/debianutils/debianutils_5.16.dsc' debianutils_5.16.dsc 1313 SHA512:74020c8c7211d226dc4c670d6c3580999159916259486d145f9b043f2dabef36ce54584636b715a8d454f676c61dd72399881dc59dcafef319bf17ef9a071246
'http://archive.ubuntu.com/ubuntu/pool/main/d/debianutils/debianutils_5.16.tar.xz' debianutils_5.16.tar.xz 105808 SHA512:60f5ae8ad094cfc4094741d58223fed37cd16e0ac07d79fde94134a090d0cdc1f2844a5842633c9e617130e56635d3ca1ee3515956216970a05d9bba543a6bce
```

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

### `dpkg` source package: `dpkg=1.22.2ubuntu2`

Binary Packages:

- `dpkg=1.22.2ubuntu2`

Licenses: (parsed from: `/usr/share/doc/dpkg/copyright`)

- `GPL-2`
- `GPL-2+`
- `public-domain-s-s-d`

Source:

```console
$ apt-get source -qq --print-uris dpkg=1.22.2ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/d/dpkg/dpkg_1.22.2ubuntu2.dsc' dpkg_1.22.2ubuntu2.dsc 3148 SHA512:c69604da1bc181a8494bdcf6f83a677135c308e0123b5ee8ec76c0a0380d32be5d9d5d43eec58c0a3053c74807ee3d1aab7c4658ccb7b6fa86b013281961531a
'http://archive.ubuntu.com/ubuntu/pool/main/d/dpkg/dpkg_1.22.2ubuntu2.tar.xz' dpkg_1.22.2ubuntu2.tar.xz 5629312 SHA512:41be0eea30101268e44acfd395d808652884c53e7b9a027a503b66cd2c55d06027d11e7c428c2ba50048ce97df665471bf5a5cd002e1df4a9a0db9aeb89b8d73
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

### `dpkg` source package: `expat=2.5.0-2`

Binary Packages:

- `libexpat1:amd64=2.5.0-2`

Licenses: (parsed from: `/usr/share/doc/libexpat1/copyright`)

- `MIT`

Source:

```console
$ apt-get source -qq --print-uris expat=2.5.0-2
'http://archive.ubuntu.com/ubuntu/pool/main/e/expat/expat_2.5.0-2.dsc' expat_2.5.0-2.dsc 1964 SHA512:a71f12ab67b948e890dd1d7e00339acb22cef4f834bc2cd26cbfc04eb5e0d65d56a22e41d384394862104e2e8da0309f4029b059a7adcfdc2d0b0d1acc64ca28
'http://archive.ubuntu.com/ubuntu/pool/main/e/expat/expat_2.5.0.orig.tar.gz' expat_2.5.0.orig.tar.gz 8320988 SHA512:779f0d0f3f2d8b33db0fd044864ab5ab1a40f20501f792fe90ad0d18de536c4765c3749f120e21fec11a0e6c89af1dc576d1fe261c871ca44a594f7b61fd1d9e
'http://archive.ubuntu.com/ubuntu/pool/main/e/expat/expat_2.5.0-2.debian.tar.xz' expat_2.5.0-2.debian.tar.xz 12804 SHA512:3603f3f3f3e4f0bc2c7a29a25aa7c9681ff4a93d48b7e5fabb0d58f8e048c3d7eb0487140f813bd925c4cb2b956a3bd2f68d8c3d75f79066624d83445739cb57
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

### `dpkg` source package: `gcc-13=13.2.0-9ubuntu1`

Binary Packages:

- `gcc-13-base:amd64=13.2.0-9ubuntu1`

Licenses: (parsed from: `/usr/share/doc/gcc-13-base/copyright`)

- `Artistic`
- `GFDL-1.2`
- `GPL`
- `GPL-2`
- `GPL-3`
- `LGPL`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `gcc-14=14-20240121-1ubuntu1`

Binary Packages:

- `gcc-14-base:amd64=14-20240121-1ubuntu1`
- `libgcc-s1:amd64=14-20240121-1ubuntu1`
- `libstdc++6:amd64=14-20240121-1ubuntu1`

Licenses: (parsed from: `/usr/share/doc/gcc-14-base/copyright`, `/usr/share/doc/libgcc-s1/copyright`, `/usr/share/doc/libstdc++6/copyright`)

- `Artistic`
- `GFDL-1.2`
- `GPL`
- `GPL-3`
- `LGPL`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `gdbm=1.23-5`

Binary Packages:

- `libgdbm-compat4:amd64=1.23-5`
- `libgdbm6:amd64=1.23-5`

Licenses: (parsed from: `/usr/share/doc/libgdbm-compat4/copyright`, `/usr/share/doc/libgdbm6/copyright`)

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

### `dpkg` source package: `glibc=2.38-3ubuntu1`

Binary Packages:

- `libc-bin=2.38-3ubuntu1`
- `libc6:amd64=2.38-3ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libc-bin/copyright`, `/usr/share/doc/libc6/copyright`)

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

### `dpkg` source package: `gnutls28=3.8.1-4ubuntu7`

Binary Packages:

- `libgnutls30:amd64=3.8.1-4ubuntu7`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `grep=3.11-4`

Binary Packages:

- `grep=3.11-4`

Licenses: (parsed from: `/usr/share/doc/grep/copyright`)

- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris grep=3.11-4
'http://archive.ubuntu.com/ubuntu/pool/main/g/grep/grep_3.11-4.dsc' grep_3.11-4.dsc 1642 SHA512:cabbf323b0a52e81b40ea54448f67d68a0a2569598a52a4750ee796d4fe16e342b5d63322339b30ff89e8d2f3e3cd977806311285ad55eb6ba195adf6dffd7a7
'http://archive.ubuntu.com/ubuntu/pool/main/g/grep/grep_3.11.orig.tar.xz' grep_3.11.orig.tar.xz 1703776 SHA512:f254a1905a08c8173e12fbdd4fd8baed9a200217fba9d7641f0d78e4e002c1f2a621152d67027d9b25f0bb2430898f5233dc70909d8464fd13d7dd9298e65c42
'http://archive.ubuntu.com/ubuntu/pool/main/g/grep/grep_3.11.orig.tar.xz.asc' grep_3.11.orig.tar.xz.asc 833 SHA512:487aba063373ca0594c519991f19b2a6a33b3da0d74735c890f3828fd0880e7e6f64495d2c8f9efa5da53d1eb2d446609bab2399a4b89dcb4510a632e31ffb54
'http://archive.ubuntu.com/ubuntu/pool/main/g/grep/grep_3.11-4.debian.tar.xz' grep_3.11-4.debian.tar.xz 20468 SHA512:6de805c7b789da79abf333b9c03f3e4e75aaf00a972a8bb6c31086d5ae571b0bdacd939b5c9c8a8b4ad46d2ed0a8358ccfe5f1c9dfad847a50365c2478ebb770
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

### `dpkg` source package: `init-system-helpers=1.66ubuntu1`

Binary Packages:

- `init-system-helpers=1.66ubuntu1`

Licenses: (parsed from: `/usr/share/doc/init-system-helpers/copyright`)

- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris init-system-helpers=1.66ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/i/init-system-helpers/init-system-helpers_1.66ubuntu1.dsc' init-system-helpers_1.66ubuntu1.dsc 2353 SHA512:f6aafcef04d63b54d6ff273312ff2a9194345b8725bfbbaac69793a3d016cbda730f2de8de9862d8038c36ca0fba39b868d6d640701ccf8db417094816d0e9db
'http://archive.ubuntu.com/ubuntu/pool/main/i/init-system-helpers/init-system-helpers_1.66ubuntu1.tar.xz' init-system-helpers_1.66ubuntu1.tar.xz 45100 SHA512:222f73347b0ce9eb137c8ce5dc36e9fedbc8dc5ed3f1fde7fbf52258a5437d0a10d3d610ca1d1b206646bb92a5355d1061705440b2d22d9109b5de6d1cb92e98
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

- `libgssapi-krb5-2:amd64=1.20.1-5build1`
- `libk5crypto3:amd64=1.20.1-5build1`
- `libkrb5-3:amd64=1.20.1-5build1`
- `libkrb5support0:amd64=1.20.1-5build1`

Licenses: (parsed from: `/usr/share/doc/libgssapi-krb5-2/copyright`, `/usr/share/doc/libk5crypto3/copyright`, `/usr/share/doc/libkrb5-3/copyright`, `/usr/share/doc/libkrb5support0/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris krb5=1.20.1-5build1
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.20.1-5build1.dsc' krb5_1.20.1-5build1.dsc 3933 SHA512:5b2da996dde2fb66fd44b759f21e641e8a408df17123283d1a245355d2f8ce880a56aea3a65c506404b59e2ca63708b49f0aa9dcffcf6837487f00af25fd1ff5
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.20.1.orig.tar.gz' krb5_1.20.1.orig.tar.gz 8661660 SHA512:6f57479f13f107cd84f30de5c758eb6b9fc59171329c13e5da6073b806755f8d163eb7bd84767ea861ad6458ea0c9eeb00ee044d3bcad01ef136e9888564b6a2
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.20.1.orig.tar.gz.asc' krb5_1.20.1.orig.tar.gz.asc 833 SHA512:1d3312bd67581e07adfdadf2c5fe394179631d8add8bd075efefe982a0de22369004e60a14422d426382c8c591e4181b9897088afe9d4e86f0b5a97e5954c67a
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.20.1-5build1.debian.tar.xz' krb5_1.20.1-5build1.debian.tar.xz 104588 SHA512:686aa216b2b5cce1c13e7f967d30eb79f0c9bf71dbffefbf4292d9eef3a36702aa819b8c5cd7a1e9a92e547c8af7d2a2ca647dd8311b1ee378aef8dbe41d6404
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

### `dpkg` source package: `libbsd=0.11.8-1`

Binary Packages:

- `libbsd0:amd64=0.11.8-1`

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
$ apt-get source -qq --print-uris libbsd=0.11.8-1
'http://archive.ubuntu.com/ubuntu/pool/main/libb/libbsd/libbsd_0.11.8-1.dsc' libbsd_0.11.8-1.dsc 2347 SHA512:1965d7bb9c545850f417a271d3ffbf6d91c2dba74e21001f2b9a871be0b421b3b1bce0dbebddefbe6c0fad4c5329fd112e66e1d4b13e728c250096ced54de11f
'http://archive.ubuntu.com/ubuntu/pool/main/libb/libbsd/libbsd_0.11.8.orig.tar.xz' libbsd_0.11.8.orig.tar.xz 432376 SHA512:0173fc20e2471f96bc6677500a02fbccef7463e023445f47681843c9a94b1fa9970c5af7d2f87f1a1e7f8a7bb60112988defc073828fd2a0dcd0e66e44e67295
'http://archive.ubuntu.com/ubuntu/pool/main/libb/libbsd/libbsd_0.11.8.orig.tar.xz.asc' libbsd_0.11.8.orig.tar.xz.asc 931 SHA512:a24355f9151f1da62e1f4f37280eec57ee7a32205b493d973d59231382c878e4373d4cf83ec41612536ef9361fe43e68331217c96c59b6741e7827272369ff2c
'http://archive.ubuntu.com/ubuntu/pool/main/libb/libbsd/libbsd_0.11.8-1.debian.tar.xz' libbsd_0.11.8-1.debian.tar.xz 18288 SHA512:a39515569718e2b5519201d6bf2c4a6dae5717e5ec58d2f28f6e0aa7c1484d36eeaa7f12fe33f62818a6af685a276ed2b61c6d285f7713c785d405279a37cab5
```

### `dpkg` source package: `libcap-ng=0.8.4-1`

Binary Packages:

- `libcap-ng0:amd64=0.8.4-1`

Licenses: (parsed from: `/usr/share/doc/libcap-ng0/copyright`)

- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris libcap-ng=0.8.4-1
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap-ng/libcap-ng_0.8.4-1.dsc' libcap-ng_0.8.4-1.dsc 1638 SHA512:b3498f32ab46abd932425c64776656a35439f91cbd0e27504cd355812d3776e3c30cdefc22d41b4bab5bce2f2ebb71a73d2548ae9777de99adac161960564236
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap-ng/libcap-ng_0.8.4.orig.tar.gz' libcap-ng_0.8.4.orig.tar.gz 59317 SHA512:3e640ba4bfa2d5b5d0eb463abca3b2c745b10e929571c0ec32eb068bdc41fd95e19f7131893a22ceebb4d1f1083d3d87d9a32f0808442d594ac5940791152acf
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap-ng/libcap-ng_0.8.4-1.debian.tar.xz' libcap-ng_0.8.4-1.debian.tar.xz 6836 SHA512:d18db686a3cd9509f7c78c43d1680a2b46cc21f896273765f016b6a1ba5e7ba0c0a65b9d404ffddb055c864134a4237cf0195cfd06975b9814e0100963cb23e3
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

### `dpkg` source package: `libffi=3.4.4-2`

Binary Packages:

- `libffi8:amd64=3.4.4-2`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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

### `dpkg` source package: `libmd=1.1.0-2`

Binary Packages:

- `libmd0:amd64=1.1.0-2`

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
$ apt-get source -qq --print-uris libmd=1.1.0-2
'http://archive.ubuntu.com/ubuntu/pool/main/libm/libmd/libmd_1.1.0-2.dsc' libmd_1.1.0-2.dsc 2280 SHA512:453c059f75fcd165dfd429b3a40df7214a75b279c141f86dfff7e0dbc654545ea4bd20e2e81c4bff3b8157765922df47b38ccc6795aeb07d461474d4e5f486ee
'http://archive.ubuntu.com/ubuntu/pool/main/libm/libmd/libmd_1.1.0.orig.tar.xz' libmd_1.1.0.orig.tar.xz 271228 SHA512:5d0da3337038e474fae7377bbc646d17214e72dc848a7aadc157f49333ce7b5ac1456e45d13674bd410ea08477c6115fc4282fed6c8e6a0bf63537a418c0df96
'http://archive.ubuntu.com/ubuntu/pool/main/libm/libmd/libmd_1.1.0.orig.tar.xz.asc' libmd_1.1.0.orig.tar.xz.asc 833 SHA512:b0ff3baa7eedc205ee6f8b844859145fa6922c39e8f62f1e997851a65b2881649b438a37baa5800d140541da6f4dacc9f92a370f945d7461937b8cdedeca1cef
'http://archive.ubuntu.com/ubuntu/pool/main/libm/libmd/libmd_1.1.0-2.debian.tar.xz' libmd_1.1.0-2.debian.tar.xz 8244 SHA512:6853f3371f7e980d177bf7ab6acf94ab9ffd2f645491aec5455e2ad277f449e3312908bdcb0d0eb6dece3f376075d845cfabff83d7ca7156cfe88237a3441551
```

### `dpkg` source package: `libnsl=1.3.0-3`

Binary Packages:

- `libnsl2:amd64=1.3.0-3`

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

Source:

```console
$ apt-get source -qq --print-uris libnsl=1.3.0-3
'http://archive.ubuntu.com/ubuntu/pool/main/libn/libnsl/libnsl_1.3.0-3.dsc' libnsl_1.3.0-3.dsc 1955 SHA512:b512bc0fe8e37f81c50f2964b4768c39ba5f6e0aedea1fc8aadf66bd3d5545e5167f25f304a1cadb189f58eb8e78caaef30498263e9dcd515db4459195cc06c5
'http://archive.ubuntu.com/ubuntu/pool/main/libn/libnsl/libnsl_1.3.0.orig.tar.xz' libnsl_1.3.0.orig.tar.xz 321488 SHA512:a5a6c3ccb2d1e724c8c1f65e55dcd09383eb1ae019c55f4c09441eadf23ffbc2196cfad259805b0ac40ddf3a10af0da453e4d739d67d46829c64d0995dab4e55
'http://archive.ubuntu.com/ubuntu/pool/main/libn/libnsl/libnsl_1.3.0-3.debian.tar.xz' libnsl_1.3.0-3.debian.tar.xz 4748 SHA512:f2184805d849afd033bc26ff1267d9163b766dcfe8e6db39966476b8cd908a9b28cfc7d90fad95c13f9d6107cf35a584e67f13a51703eb6dd34dc3ec46279480
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

### `dpkg` source package: `libseccomp=2.5.4-1ubuntu3`

Binary Packages:

- `libseccomp2:amd64=2.5.4-1ubuntu3`

Licenses: (parsed from: `/usr/share/doc/libseccomp2/copyright`)

- `LGPL-2.1`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libselinux=3.5-1build2`

Binary Packages:

- `libselinux1:amd64=3.5-1build2`

Licenses: (parsed from: `/usr/share/doc/libselinux1/copyright`)

- `GPL-2`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libsemanage=3.5-1build1`

Binary Packages:

- `libsemanage-common=3.5-1build1`
- `libsemanage2:amd64=3.5-1build1`

Licenses: (parsed from: `/usr/share/doc/libsemanage-common/copyright`, `/usr/share/doc/libsemanage2/copyright`)

- `GPL-2`
- `LGPL-2.1`
- `LGPL-2.1+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libsepol=3.5-2`

Binary Packages:

- `libsepol2:amd64=3.5-2`

Licenses: (parsed from: `/usr/share/doc/libsepol2/copyright`)

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

### `dpkg` source package: `libtirpc=1.3.4+ds-1build1`

Binary Packages:

- `libtirpc-common=1.3.4+ds-1build1`
- `libtirpc3:amd64=1.3.4+ds-1build1`

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
$ apt-get source -qq --print-uris libtirpc=1.3.4+ds-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtirpc/libtirpc_1.3.4%2bds-1build1.dsc' libtirpc_1.3.4+ds-1build1.dsc 2128 SHA512:ab4a4e9d4e4ca4da690d6ce1dde67ed7e3bff421edf2b79c1be85e8e3897f2079c93b0008fe7d5c228187ab936d5da0dbef21cb55b714721a225205d2302af5d
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtirpc/libtirpc_1.3.4%2bds.orig.tar.gz' libtirpc_1.3.4+ds.orig.tar.gz 700735 SHA512:125e26247f1ffbf5ce310657515eb84be03b69867e5efbacac6768f406470f9124b66124639daccd9af0c8220a8099cb5dbbe0a370315c61069aa73a5b53815d
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtirpc/libtirpc_1.3.4%2bds-1build1.debian.tar.xz' libtirpc_1.3.4+ds-1build1.debian.tar.xz 11508 SHA512:07df1846bbc77e3f42c31027d4c86b2c72eb38f0028589cb8864b03032dbabfe17df5a71fb8cf4b8685fd1afc7521b534f6d909af5ba6cb6d81453a967867f10
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

### `dpkg` source package: `libxcrypt=1:4.4.36-2`

Binary Packages:

- `libcrypt1:amd64=1:4.4.36-2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/libxcrypt/1:4.4.36-2/


### `dpkg` source package: `libzstd=1.5.5+dfsg2-2`

Binary Packages:

- `libzstd1:amd64=1.5.5+dfsg2-2`

Licenses: (parsed from: `/usr/share/doc/libzstd1/copyright`)

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

### `dpkg` source package: `mawk=1.3.4.20240123-1`

Binary Packages:

- `mawk=1.3.4.20240123-1`

Licenses: (parsed from: `/usr/share/doc/mawk/copyright`)

- `CC-BY-3.0`
- `GPL-2`
- `GPL-2.0-only`
- `X11`

Source:

```console
$ apt-get source -qq --print-uris mawk=1.3.4.20240123-1
'http://archive.ubuntu.com/ubuntu/pool/main/m/mawk/mawk_1.3.4.20240123-1.dsc' mawk_1.3.4.20240123-1.dsc 2180 SHA512:1e36a3b749264d158105450f6230586345fc83a2d8b62693ca2fa14c5359934d5fe78e64c5d5085a1234f96310acbe132295099a8526adbd02413ee28e34fc03
'http://archive.ubuntu.com/ubuntu/pool/main/m/mawk/mawk_1.3.4.20240123.orig.tar.gz' mawk_1.3.4.20240123.orig.tar.gz 413943 SHA512:f6d5da44280afeac4a9bb6d3788ed71ee816daaa5816f49b9d40add5292f3ae06e5af007a6c993d14405238cbb70ba4997fdd2fcd5901c9a1a4b61357045c4a6
'http://archive.ubuntu.com/ubuntu/pool/main/m/mawk/mawk_1.3.4.20240123.orig.tar.gz.asc' mawk_1.3.4.20240123.orig.tar.gz.asc 729 SHA512:3b4b8b8b7b74aff7061158a7c284d1949c09d52d78003b678c9dcc1da036a4d84b873103d76362866daf914d5a7d717c71baf13d30d7e882b03c5f87c8e4c452
'http://archive.ubuntu.com/ubuntu/pool/main/m/mawk/mawk_1.3.4.20240123-1.debian.tar.xz' mawk_1.3.4.20240123-1.debian.tar.xz 15600 SHA512:d873c86ea2f3c7dfdb7007225454feae801ed5022cbe8eee18313637f4744550e8345eb675c69fd4709287c807fb6048bdead3070d27059a7743dd2ec2c818d9
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

### `dpkg` source package: `mercurial=6.6.1-2`

Binary Packages:

- `mercurial=6.6.1-2`
- `mercurial-common=6.6.1-2`

Licenses: (parsed from: `/usr/share/doc/mercurial/copyright`, `/usr/share/doc/mercurial-common/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris mercurial=6.6.1-2
'http://archive.ubuntu.com/ubuntu/pool/universe/m/mercurial/mercurial_6.6.1-2.dsc' mercurial_6.6.1-2.dsc 2806 SHA512:2e168d80469dd010b54ccd9d83cc0360df605bb5f3c5da63dd8b72a452e295c956e1bbcdc18acc9b389c1e272b877fb8124f5f836a9593da2a440f0a164a7252
'http://archive.ubuntu.com/ubuntu/pool/universe/m/mercurial/mercurial_6.6.1.orig.tar.gz' mercurial_6.6.1.orig.tar.gz 8250933 SHA512:f16240f06a98a088e0229aa6584daa540eee92476a0a7934617c065c9f1012288cf3d6fb2d20fc7b247122bc360201f2e2c1c139c261a834f483bd09bef74d0c
'http://archive.ubuntu.com/ubuntu/pool/universe/m/mercurial/mercurial_6.6.1.orig.tar.gz.asc' mercurial_6.6.1.orig.tar.gz.asc 659 SHA512:293abe3d49f84495e117f37cdb1264dedf8220207267348cff3c575763d49e3a58997257493e12e80eea1ac612d1eb4ec598e2ea1144cabb309c4cd24d86c5ba
'http://archive.ubuntu.com/ubuntu/pool/universe/m/mercurial/mercurial_6.6.1-2.debian.tar.xz' mercurial_6.6.1-2.debian.tar.xz 70260 SHA512:d80d08cbbef02b284f107b3ba53ad20e8a86bd2711a17442edf1347fffa5f7c7df008f942b89a4952670d0db741b38638fe23a95239e74f575e261bbf2658881
```

### `dpkg` source package: `ncurses=6.4+20231209-1`

Binary Packages:

- `libncursesw6:amd64=6.4+20231209-1`
- `libtinfo6:amd64=6.4+20231209-1`
- `ncurses-base=6.4+20231209-1`
- `ncurses-bin=6.4+20231209-1`

Licenses: (parsed from: `/usr/share/doc/libncursesw6/copyright`, `/usr/share/doc/libtinfo6/copyright`, `/usr/share/doc/ncurses-base/copyright`, `/usr/share/doc/ncurses-bin/copyright`)

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/nghttp2/1.58.0-1/


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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `openssl=3.0.10-1ubuntu3`

Binary Packages:

- `libssl3:amd64=3.0.10-1ubuntu3`
- `openssl=3.0.10-1ubuntu3`

Licenses: (parsed from: `/usr/share/doc/libssl3/copyright`, `/usr/share/doc/openssl/copyright`)

- `Apache-2.0`
- `Artistic`
- `GPL-1`
- `GPL-1+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `pam=1.5.2-9.1ubuntu2`

Binary Packages:

- `libpam-modules:amd64=1.5.2-9.1ubuntu2`
- `libpam-modules-bin=1.5.2-9.1ubuntu2`
- `libpam-runtime=1.5.2-9.1ubuntu2`
- `libpam0g:amd64=1.5.2-9.1ubuntu2`

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
$ apt-get source -qq --print-uris pam=1.5.2-9.1ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/p/pam/pam_1.5.2-9.1ubuntu2.dsc' pam_1.5.2-9.1ubuntu2.dsc 2704 SHA512:da05e05a48a43a215425cd9fee1ac3952676da584dc06c10bff684a0189720c74e8d3e97592cabb579bd11546a916b264f8fe16a4d400394a94040fe6a0eaad6
'http://archive.ubuntu.com/ubuntu/pool/main/p/pam/pam_1.5.2.orig.tar.xz' pam_1.5.2.orig.tar.xz 988784 SHA512:fa16350c132d3e5fb82b60d991768fb596582639841b8ece645c684705467305ccf1302a0147ec222ab78c01b2c9114c5496dc1ca565d2b56bf315f29a815144
'http://archive.ubuntu.com/ubuntu/pool/main/p/pam/pam_1.5.2-9.1ubuntu2.debian.tar.xz' pam_1.5.2-9.1ubuntu2.debian.tar.xz 177148 SHA512:9f18032c920da3d7599c38c220b8dd3fa62da33437b1d36b06855bb7fcb54abae0b2c30cb853c6d06145f3e210c862b2d0ab2db8e0c92804ff4949d45449dde2
```

### `dpkg` source package: `pcre2=10.42-4ubuntu1`

Binary Packages:

- `libpcre2-8-0:amd64=10.42-4ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libpcre2-8-0/copyright`)

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

### `dpkg` source package: `python3-defaults=3.11.4-5ubuntu1`

Binary Packages:

- `libpython3-stdlib:amd64=3.11.4-5ubuntu1`
- `python3=3.11.4-5ubuntu1`
- `python3-minimal=3.11.4-5ubuntu1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris python3-defaults=3.11.4-5ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3-defaults/python3-defaults_3.11.4-5ubuntu1.dsc' python3-defaults_3.11.4-5ubuntu1.dsc 3108 SHA512:31f52ffb5ec12b2addc51a23e116788641777c51544a29393652c1614a5ebb55de429565c7086d6e1f21c9c2d51548b3159d214cec16a16e6fe1c83d7ff5a253
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3-defaults/python3-defaults_3.11.4-5ubuntu1.tar.gz' python3-defaults_3.11.4-5ubuntu1.tar.gz 146771 SHA512:3ce3ddb9e2953c0f06c3a67e405537410421788a9f61cc078d76c3a3957407f08740c35133a6b785588b4f5ac065c2f5a37ba8920f3fd19e7929df6c0b2ec6ed
```

### `dpkg` source package: `python3.11=3.11.7-2`

Binary Packages:

- `libpython3.11-minimal:amd64=3.11.7-2`
- `libpython3.11-stdlib:amd64=3.11.7-2`
- `python3.11=3.11.7-2`
- `python3.11-minimal=3.11.7-2`

Licenses: (parsed from: `/usr/share/doc/libpython3.11-minimal/copyright`, `/usr/share/doc/libpython3.11-stdlib/copyright`, `/usr/share/doc/python3.11/copyright`, `/usr/share/doc/python3.11-minimal/copyright`)

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

### `dpkg` source package: `readline=8.2-3`

Binary Packages:

- `libreadline8:amd64=8.2-3`
- `readline-common=8.2-3`

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
$ apt-get source -qq --print-uris readline=8.2-3
'http://archive.ubuntu.com/ubuntu/pool/main/r/readline/readline_8.2-3.dsc' readline_8.2-3.dsc 2783 SHA512:498fb4d387345d028dd5653c735a021c4354d01c61e487a57e165ddcdec6625b314823accb30dae04706b3d7d979d113a1e36534557b5b6aeb971c3ebfbaf562
'http://archive.ubuntu.com/ubuntu/pool/main/r/readline/readline_8.2.orig.tar.gz' readline_8.2.orig.tar.gz 3043952 SHA512:0a451d459146bfdeecc9cdd94bda6a6416d3e93abd80885a40b334312f16eb890f8618a27ca26868cebbddf1224983e631b1cbc002c1a4d1cd0d65fba9fea49a
'http://archive.ubuntu.com/ubuntu/pool/main/r/readline/readline_8.2-3.debian.tar.xz' readline_8.2-3.debian.tar.xz 33220 SHA512:d883b2353a7ed909792b68cf29d26a9e0befdccf538da0991b7ead1c9a22e500b1175c9af5013751b6d15bf3a957aca49d10d0ca3aae767251c600f6640dbd86
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

### `dpkg` source package: `rust-sequoia-sq=0.33.0-2`

Binary Packages:

- `sq=0.33.0-2`

Licenses: (parsed from: `/usr/share/doc/sq/copyright`)

- `GPL-2`
- `GPL-2.0-or-later`
- `LGPL-2`
- `LGPL-2.0-or-later`

Source:

```console
$ apt-get source -qq --print-uris rust-sequoia-sq=0.33.0-2
'http://archive.ubuntu.com/ubuntu/pool/universe/r/rust-sequoia-sq/rust-sequoia-sq_0.33.0-2.dsc' rust-sequoia-sq_0.33.0-2.dsc 3612 SHA512:9b26360d65943f43c2b521cc481e88cb0884e544c4818df34e95cb93d772d0e11f4e057aa340f3c94c28700859472d960dcaadba5af6557699fbfe449a0351a3
'http://archive.ubuntu.com/ubuntu/pool/universe/r/rust-sequoia-sq/rust-sequoia-sq_0.33.0.orig.tar.gz' rust-sequoia-sq_0.33.0.orig.tar.gz 388309 SHA512:c366c7c2f2fcc398194f20922fed72bf18ede12164f8d0438bac0ca08f0900004f3c1039f8cd3ee480ded3e42104cf6ac4365020b9f258dc115594112ec3b101
'http://archive.ubuntu.com/ubuntu/pool/universe/r/rust-sequoia-sq/rust-sequoia-sq_0.33.0-2.debian.tar.xz' rust-sequoia-sq_0.33.0-2.debian.tar.xz 4372 SHA512:ed02779e03a6751efbfc9bd190bc66877dc1637d37477fbc88fd91a9368ce2d2ecf716f66b54bb35f9ab0fd608c8382d5bdcb262f1fcd6d6f5c0dbe8def9811c
```

### `dpkg` source package: `sed=4.9-2`

Binary Packages:

- `sed=4.9-2`

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
$ apt-get source -qq --print-uris sed=4.9-2
'http://archive.ubuntu.com/ubuntu/pool/main/s/sed/sed_4.9-2.dsc' sed_4.9-2.dsc 1860 SHA512:b5b79f9c01ba73782f9f5691c4c744f18635f6e51c6d4fdfac5d8de42ee7e937713ad3a41153f01c23d9453f0a6d9b0d36f51d94cba051956f68f73c6ec2a03a
'http://archive.ubuntu.com/ubuntu/pool/main/s/sed/sed_4.9.orig.tar.xz' sed_4.9.orig.tar.xz 1397092 SHA512:36157a4b4a2430cf421b7bd07f1675d680d9f1616be96cf6ad6ee74a9ec0fe695f8d0b1e1f0b008bbb33cc7fcde5e1c456359bbbc63f8aebdd4fedc3982cf6dc
'http://archive.ubuntu.com/ubuntu/pool/main/s/sed/sed_4.9-2.debian.tar.xz' sed_4.9-2.debian.tar.xz 62756 SHA512:138008995afd81ea2a0b14a6a559293e94cc5a8c010b5912c6f961ac79c5623946f1093940ec28bc0d9b84a7dd741ff5370ad0728871ae514747d7107bb417dd
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

### `dpkg` source package: `sqlite3=3.45.0-1`

Binary Packages:

- `libsqlite3-0:amd64=3.45.0-1`

Licenses: (parsed from: `/usr/share/doc/libsqlite3-0/copyright`)

- `GPL-2`
- `GPL-2+`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/sqlite3/3.45.0-1/


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

### `dpkg` source package: `tar=1.35+dfsg-3`

Binary Packages:

- `tar=1.35+dfsg-3`

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
$ apt-get source -qq --print-uris tar=1.35+dfsg-3
'http://archive.ubuntu.com/ubuntu/pool/main/t/tar/tar_1.35%2bdfsg-3.dsc' tar_1.35+dfsg-3.dsc 2009 SHA512:15aa2d1b3e6ff0b73c60983e9e2744f4d78f66a39ede950222bd3efefa1041a83067ae5c25df0f015460303f68afd441249546a978e45d913f4a2385017c725e
'http://archive.ubuntu.com/ubuntu/pool/main/t/tar/tar_1.35%2bdfsg.orig.tar.xz' tar_1.35+dfsg.orig.tar.xz 2111608 SHA512:3aea32b5c8de229131308420d8a7aa57f7fd1b376980456dd1aa66f97509572750c3833ab9cc2edc6fdea51f802033598c83a0d6e7f18680b1638996f0acaae7
'http://archive.ubuntu.com/ubuntu/pool/main/t/tar/tar_1.35%2bdfsg-3.debian.tar.xz' tar_1.35+dfsg-3.debian.tar.xz 20824 SHA512:5cfb94a850ddaa969e5e5e6f607bd300e1cbffd56f0d8ff272b9e138dd7a9f25d760330bb426144dcd1f811e0df72b4ae8b9af7444d3226083fa51c66a6a4f1b
```

### `dpkg` source package: `tzdata=2023d-1ubuntu2`

Binary Packages:

- `tzdata=2023d-1ubuntu2`

Licenses: (parsed from: `/usr/share/doc/tzdata/copyright`)

- `ICU`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris tzdata=2023d-1ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/t/tzdata/tzdata_2023d-1ubuntu2.dsc' tzdata_2023d-1ubuntu2.dsc 2675 SHA512:bea023850103ec85567d3bffecf773f4999b71804170312e329dfc06a2b2ce0c1657105456560a4a0028bd8e805029335d1b8edd1e62a6ca4adfc9f0ec0eb5d5
'http://archive.ubuntu.com/ubuntu/pool/main/t/tzdata/tzdata_2023d.orig.tar.gz' tzdata_2023d.orig.tar.gz 449767 SHA512:81832b2d738c28cecbcb3906cc07568c5ae574adc9de35b25d4bf613581c92d471d67213b4261a56f0ec02efcf211b4e298b7e1dc367c972e726b0a2e9498df4
'http://archive.ubuntu.com/ubuntu/pool/main/t/tzdata/tzdata_2023d.orig.tar.gz.asc' tzdata_2023d.orig.tar.gz.asc 833 SHA512:3266f0ad4e05365fb09d48b9baeb884447cc4c16ecd4f0d2bf5f25b0aabe03b48fca11c19379a45545dc4f41acc68633c624d99d2700f439d9233ecab6d1f184
'http://archive.ubuntu.com/ubuntu/pool/main/t/tzdata/tzdata_2023d-1ubuntu2.debian.tar.xz' tzdata_2023d-1ubuntu2.debian.tar.xz 183532 SHA512:ae833beafff3ee7eb02d01f5a0052bfc413e53a2ae9b69022d797011efc3b914b91b1c1d8604bdc1474bcaf364f9650a6cfd4ee7a89444b1c2e33a3dc988296f
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

### `dpkg` source package: `usrmerge=38ubuntu1`

Binary Packages:

- `usrmerge=38ubuntu1`

Licenses: (parsed from: `/usr/share/doc/usrmerge/copyright`)

- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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
- `libblkid1:amd64=2.39.2-6ubuntu1`
- `libmount1:amd64=2.39.2-6ubuntu1`
- `libsmartcols1:amd64=2.39.2-6ubuntu1`
- `libuuid1:amd64=2.39.2-6ubuntu1`
- `mount=2.39.2-6ubuntu1`
- `util-linux=2.39.2-6ubuntu1`

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

- `liblzma5:amd64=5.4.5-0.3`

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
$ apt-get source -qq --print-uris xz-utils=5.4.5-0.3
'http://archive.ubuntu.com/ubuntu/pool/main/x/xz-utils/xz-utils_5.4.5-0.3.dsc' xz-utils_5.4.5-0.3.dsc 2720 SHA512:0af36bb4429ceb470975b3ff20b6e455aad41c3a22754bf5d93885aa79d8699db3c00b2613a9d22ccc936f0f96687190c74c5a4f53e694906b7edc103f2da6b9
'http://archive.ubuntu.com/ubuntu/pool/main/x/xz-utils/xz-utils_5.4.5.orig.tar.xz' xz-utils_5.4.5.orig.tar.xz 1680520 SHA512:5cbc3b5bb35a9f5773ad657788fe77013471e3b621c5a8149deb7389d48535926e5bed103456fcfe5ecb044b236b1055b03938a6cc877cfc749372b899fc79e5
'http://archive.ubuntu.com/ubuntu/pool/main/x/xz-utils/xz-utils_5.4.5.orig.tar.xz.asc' xz-utils_5.4.5.orig.tar.xz.asc 833 SHA512:7390e991d6eccc8bb2fd3d319fcde92df0abcdc163bd0210a1d5f6c7a80268f36ead88ce1ae1d6935084f608b515ed1cd87c30085fcc2ee9222fc78c4a37ddbb
'http://archive.ubuntu.com/ubuntu/pool/main/x/xz-utils/xz-utils_5.4.5-0.3.debian.tar.xz' xz-utils_5.4.5-0.3.debian.tar.xz 26944 SHA512:ec4ca5251586aebd86dfe2ed564a078e58658c5cc6f866691971ba294a735ba7bc00b4eae678794683197e7f92f532226c0fda5534701377a79ad5c3623f754d
```

### `dpkg` source package: `zlib=1:1.3.dfsg-3ubuntu1`

Binary Packages:

- `zlib1g:amd64=1:1.3.dfsg-3ubuntu1`

Licenses: (parsed from: `/usr/share/doc/zlib1g/copyright`)

- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris zlib=1:1.3.dfsg-3ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/z/zlib/zlib_1.3.dfsg-3ubuntu1.dsc' zlib_1.3.dfsg-3ubuntu1.dsc 3095 SHA512:f1decbdaccf4fe93258fb7bf639da9d5687e1b597006be8432709e3fcf97fa9b5b42afd4693e5e0ecace0e6a5358f105ee587440173aae405672557f4208e903
'http://archive.ubuntu.com/ubuntu/pool/main/z/zlib/zlib_1.3.dfsg.orig.tar.xz' zlib_1.3.dfsg.orig.tar.xz 1128572 SHA512:be6f020c691c61fe4ddcb27d3f8b2515435f544177e0b97286b5e85afc3862c1de6cd74a14ff6b065d620d046d35bf029fabfd1cf473f43a2cad60bf9ad55afe
'http://archive.ubuntu.com/ubuntu/pool/main/z/zlib/zlib_1.3.dfsg-3ubuntu1.debian.tar.xz' zlib_1.3.dfsg-3ubuntu1.debian.tar.xz 60544 SHA512:7cae3c176d6ba672edee2b70f1087bebc2a7f4a036c7132d65e83e6794e8245e1c3a92e6258dae231ee33c33cf2f09c3b4f4788d794b84a798d63b7938eed487
```
