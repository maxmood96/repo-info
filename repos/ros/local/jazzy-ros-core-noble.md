# `ros:jazzy-ros-core`

## Docker Metadata

- Image ID: `sha256:5b20c925c68bf455766410e82359ba652d4ffdec1b1abd553cbe062f8776a838`
- Created: `2026-04-07T02:28:27.752112077Z`
- Virtual Size: ~ 488.72 Mb  
  (total size of all layers on-disk)
- Arch: `linux`/`amd64`
- Entrypoint: `["/ros_entrypoint.sh"]`
- Command: `["bash"]`
- Environment:
  - `PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin`
  - `LANG=C.UTF-8`
  - `LC_ALL=C.UTF-8`
  - `ROS_DISTRO=jazzy`
- Labels:
  - `org.opencontainers.image.version=24.04`

## `dpkg` (`.deb`-based packages)

### `dpkg` source package: `acl=2.3.2-1build1.1`

Binary Packages:

- `libacl1:amd64=2.3.2-1build1.1`

Licenses: (parsed from: `/usr/share/doc/libacl1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2+`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris acl=2.3.2-1build1.1
'http://archive.ubuntu.com/ubuntu/pool/main/a/acl/acl_2.3.2-1build1.1.dsc' acl_2.3.2-1build1.1.dsc 2616 SHA512:484c1b046c3d1fa9fc2837cb0612da89ea65fab4ed823ac41b0d7b3fc5deb12d1a30208e24ccc04ae9529a105ddd36d8ead48c22eb14df37f97b1d9e05dfb7bb
'http://archive.ubuntu.com/ubuntu/pool/main/a/acl/acl_2.3.2.orig.tar.xz' acl_2.3.2.orig.tar.xz 371680 SHA512:c2d061dbfd28c00cecbc1ae614d67f3138202bf4d39b383f2df4c6a8b10b830f33acec620fb211f268478737dde4037d338a5823af445253cb088c48a135099b
'http://archive.ubuntu.com/ubuntu/pool/main/a/acl/acl_2.3.2.orig.tar.xz.asc' acl_2.3.2.orig.tar.xz.asc 833 SHA512:a425b385e3ce30e7146cf8b143ca269e3edd78af82a21dea76d10ea68215f9abcfb1ed8be24ce3b6dce24e6640df8d5d5f365a47399e37006a66c6a62a41fe41
'http://archive.ubuntu.com/ubuntu/pool/main/a/acl/acl_2.3.2-1build1.1.debian.tar.xz' acl_2.3.2-1build1.1.debian.tar.xz 23472 SHA512:02e1eadeccb773f30f67c40aaf9cef3401cd771870c7aa82e94bcfbdf3f885879abec23a79ad8103e559dcd02b5ab7b92633890040d2b4db1f984a2a4c4aa232
```

### `dpkg` source package: `adduser=3.137ubuntu1`

Binary Packages:

- `adduser=3.137ubuntu1`

Licenses: (parsed from: `/usr/share/doc/adduser/copyright`)

- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `apt=2.8.3`

Binary Packages:

- `apt=2.8.3`
- `libapt-pkg6.0t64:amd64=2.8.3`

Licenses: (parsed from: `/usr/share/doc/apt/copyright`, `/usr/share/doc/libapt-pkg6.0t64/copyright`)

- `BSD-3-clause`
- `Expat`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris apt=2.8.3
'http://archive.ubuntu.com/ubuntu/pool/main/a/apt/apt_2.8.3.dsc' apt_2.8.3.dsc 2973 SHA512:02223363e56b43eb224e418f9ff470228777eaac1355c787b0e648e4eae0686d3aa38f28aaf95ad75007f2529b32d5fb535024dd2a634b3fad014c95de0f33a0
'http://archive.ubuntu.com/ubuntu/pool/main/a/apt/apt_2.8.3.tar.xz' apt_2.8.3.tar.xz 2354680 SHA512:bb79bdeb9a0685efd3e9dd2e491001445ebdbccd889ab4c05c2eb0c048117f769bab86ce4a1889acd426222f2eae97fa43aa83a8227690ca061ce25787343c25
```

### `dpkg` source package: `attr=1:2.5.2-1build1.1`

Binary Packages:

- `libattr1:amd64=1:2.5.2-1build1.1`

Licenses: (parsed from: `/usr/share/doc/libattr1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2+`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris attr=1:2.5.2-1build1.1
'http://archive.ubuntu.com/ubuntu/pool/main/a/attr/attr_2.5.2-1build1.1.dsc' attr_2.5.2-1build1.1.dsc 2588 SHA512:14b89e51d44ebe63fffb1b060ec9106b8a7724f6373b095bf1a31c7da73e835be5a97f7210d1a7709e4513acab3360f423d32ef1acb519124b31165ea6674bc8
'http://archive.ubuntu.com/ubuntu/pool/main/a/attr/attr_2.5.2.orig.tar.xz' attr_2.5.2.orig.tar.xz 334180 SHA512:f587ea544effb7cfed63b3027bf14baba2c2dbe3a9b6c0c45fc559f7e8cb477b3e9a4a826eae30f929409468c50d11f3e7dc6d2500f41e1af8662a7e96a30ef3
'http://archive.ubuntu.com/ubuntu/pool/main/a/attr/attr_2.5.2.orig.tar.xz.asc' attr_2.5.2.orig.tar.xz.asc 833 SHA512:16362013313d055dec307bcf755a9846f5153a78309a499f8cac4ff57a2154de2bc8f3b1400e81dba7a0bf0c67aa02a5d464898ed6e4aa721b64ec95fd313968
'http://archive.ubuntu.com/ubuntu/pool/main/a/attr/attr_2.5.2-1build1.1.debian.tar.xz' attr_2.5.2-1build1.1.debian.tar.xz 26032 SHA512:768a95c9ecf2d2ecd5081f28a1e9982f1222bb437a3e93af44c1ffb4b24fb61c8a43ef78fc7f2ffc80f47c020db005e361f4bf83425d83a43e3de8b82ea40c68
```

### `dpkg` source package: `audit=1:3.1.2-2.1build1.1`

Binary Packages:

- `libaudit-common=1:3.1.2-2.1build1.1`
- `libaudit1:amd64=1:3.1.2-2.1build1.1`

Licenses: (parsed from: `/usr/share/doc/libaudit-common/copyright`, `/usr/share/doc/libaudit1/copyright`)

- `GPL-1`
- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris audit=1:3.1.2-2.1build1.1
'http://archive.ubuntu.com/ubuntu/pool/main/a/audit/audit_3.1.2-2.1build1.1.dsc' audit_3.1.2-2.1build1.1.dsc 2848 SHA512:3e54e808c6130829a386f25a3a40a35ae1598955407ca5eb1c400cabe4226da47688c0970e35bba4d841c73f3c625cce08130982657d9c5debdf98d78b717fb6
'http://archive.ubuntu.com/ubuntu/pool/main/a/audit/audit_3.1.2.orig.tar.gz' audit_3.1.2.orig.tar.gz 1219860 SHA512:a97003a294ed3671df01e2952688e7d5eef59a35f6891feb53e67c4c7eab9ae8c2d18de41a5b5b20e0ad7156fac93aec05f32f6bc5eea706b42b6f27f676446a
'http://archive.ubuntu.com/ubuntu/pool/main/a/audit/audit_3.1.2-2.1build1.1.debian.tar.xz' audit_3.1.2-2.1build1.1.debian.tar.xz 18860 SHA512:0d536e42718911a3b237816d67a1cb05f0c4e591dcf6aa2e17a657711e27b523bb8f79e06c895a107f0fa0039bdc192cfffd16f7b0c17eced8102bd902ac16e7
```

### `dpkg` source package: `base-files=13ubuntu10.4`

Binary Packages:

- `base-files=13ubuntu10.4`

Licenses: (parsed from: `/usr/share/doc/base-files/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris base-files=13ubuntu10.4
'http://archive.ubuntu.com/ubuntu/pool/main/b/base-files/base-files_13ubuntu10.4.dsc' base-files_13ubuntu10.4.dsc 1642 SHA512:1bf22ef81d38cdb8a29da336c044dc919c8bcf10f6e02c8171702530009e189a93070413fa4f192d9298c8cd746e0af6ecf075d2f95252bc6ff6da041595807d
'http://archive.ubuntu.com/ubuntu/pool/main/b/base-files/base-files_13ubuntu10.4.tar.xz' base-files_13ubuntu10.4.tar.xz 94240 SHA512:c78f43e4453664958f6fc99e7f6b09b974cfeb502ee4f89c11040ed47f88e2d115034c3db1408148e341acb5930e3abcf6955c76e1230ee343a7032516d7b86d
```

### `dpkg` source package: `base-passwd=3.6.3build1`

Binary Packages:

- `base-passwd=3.6.3build1`

Licenses: (parsed from: `/usr/share/doc/base-passwd/copyright`)

- `GPL-2`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `bash=5.2.21-2ubuntu4`

Binary Packages:

- `bash=5.2.21-2ubuntu4`

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


### `dpkg` source package: `brotli=1.1.0-2build2`

Binary Packages:

- `libbrotli1:amd64=1.1.0-2build2`

Licenses: (parsed from: `/usr/share/doc/libbrotli1/copyright`)

- `MIT`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `bzip2=1.0.8-5.1build0.1`

Binary Packages:

- `libbz2-1.0:amd64=1.0.8-5.1build0.1`

Licenses: (parsed from: `/usr/share/doc/libbz2-1.0/copyright`)

- `BSD-variant`
- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris bzip2=1.0.8-5.1build0.1
'http://archive.ubuntu.com/ubuntu/pool/main/b/bzip2/bzip2_1.0.8-5.1build0.1.dsc' bzip2_1.0.8-5.1build0.1.dsc 2220 SHA512:1233c3065a9355482c826f35f7859450a868a6e98ef7793dcc1ae68d68360c840ed8bd21af872501d36803c10b9b2516556e8bb716f3d0ff5cdaa877a1ab95df
'http://archive.ubuntu.com/ubuntu/pool/main/b/bzip2/bzip2_1.0.8.orig.tar.gz' bzip2_1.0.8.orig.tar.gz 810029 SHA512:083f5e675d73f3233c7930ebe20425a533feedeaaa9d8cc86831312a6581cefbe6ed0d08d2fa89be81082f2a5abdabca8b3c080bf97218a1bd59dc118a30b9f3
'http://archive.ubuntu.com/ubuntu/pool/main/b/bzip2/bzip2_1.0.8-5.1build0.1.debian.tar.bz2' bzip2_1.0.8-5.1build0.1.debian.tar.bz2 26927 SHA512:ee39a01bcd6b31d70b3dfaa14bf7f943cb3711d073569cf9e35092062742077801ca287425c855a499114335748f2f791a7ff07eb502f2601a3d58f5041e7413
```

### `dpkg` source package: `ca-certificates=20240203`

Binary Packages:

- `ca-certificates=20240203`

Licenses: (parsed from: `/usr/share/doc/ca-certificates/copyright`)

- `GPL-2`
- `GPL-2+`
- `MPL-2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/ca-certificates/20240203/


### `dpkg` source package: `catch2=3.4.0-1build1`

Binary Packages:

- `catch2=3.4.0-1build1`

Licenses: (parsed from: `/usr/share/doc/catch2/copyright`)

- `BSD-3`
- `Boost-1.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `cdebconf=0.271ubuntu3`

Binary Packages:

- `libdebconfclient0:amd64=0.271ubuntu3`

Licenses: (parsed from: `/usr/share/doc/libdebconfclient0/copyright`)

- `BSD-2-Clause`
- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `cmake=3.28.3-1build7`

Binary Packages:

- `cmake=3.28.3-1build7`
- `cmake-data=3.28.3-1build7`

Licenses: (parsed from: `/usr/share/doc/cmake/copyright`, `/usr/share/doc/cmake-data/copyright`)

- `Apache-2.0`
- `BSD-0-Clause`
- `BSD-2-Clause`
- `BSD-3-Clause`
- `BSD-3-clause`
- `BSD-4-Clause`
- `Expat`
- `FSFAP`
- `GPL-2`
- `GPL-2+ with Bison exception`
- `GPL-3`
- `GPL-3+ with Bison exception`
- `ISC`
- `Zlib`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `console-bridge=1.0.1+dfsg2-3build1`

Binary Packages:

- `libconsole-bridge-dev:amd64=1.0.1+dfsg2-3build1`
- `libconsole-bridge1.0:amd64=1.0.1+dfsg2-3build1`

Licenses: (parsed from: `/usr/share/doc/libconsole-bridge-dev/copyright`, `/usr/share/doc/libconsole-bridge1.0/copyright`)

- `BSD-3-clause`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `coreutils=9.4-3ubuntu6.2`

Binary Packages:

- `coreutils=9.4-3ubuntu6.2`

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
$ apt-get source -qq --print-uris coreutils=9.4-3ubuntu6.2
'http://archive.ubuntu.com/ubuntu/pool/main/c/coreutils/coreutils_9.4-3ubuntu6.2.dsc' coreutils_9.4-3ubuntu6.2.dsc 2030 SHA512:b885d99011e59f8af8972a546b7d2f764367dd78ffe5df19e9b28903ed82d1d1db3fbbea8d2e9f16f16344c147b8bb61de41d9f6c2f71c4bf274d820bc0d802e
'http://archive.ubuntu.com/ubuntu/pool/main/c/coreutils/coreutils_9.4.orig.tar.xz' coreutils_9.4.orig.tar.xz 5979200 SHA512:7c55ee23b685a0462bbbd118b04d25278c902604a0dcf3bf4f8bf81faa0500dee5a7813cba6f586d676c98e520cafd420f16479619305e94ea6798d8437561f5
'http://archive.ubuntu.com/ubuntu/pool/main/c/coreutils/coreutils_9.4-3ubuntu6.2.debian.tar.xz' coreutils_9.4-3ubuntu6.2.debian.tar.xz 42032 SHA512:7f80c2e3bca8b6bd8fa099a8604b308703052e2be2cd68d340c03440124fa55d1a3c4fa1cbeb628b066a6cda107cbe6c909f9fdcf1052697fc4255276f34506b
```

### `dpkg` source package: `cppcheck=2.13.0-2ubuntu3`

Binary Packages:

- `cppcheck=2.13.0-2ubuntu3`

Licenses: (parsed from: `/usr/share/doc/cppcheck/copyright`)

- `BSD-2`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `ZLIB`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `curl=8.5.0-2ubuntu10.8`

Binary Packages:

- `curl=8.5.0-2ubuntu10.8`
- `libcurl4t64:amd64=8.5.0-2ubuntu10.8`

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

Source:

```console
$ apt-get source -qq --print-uris curl=8.5.0-2ubuntu10.8
'http://archive.ubuntu.com/ubuntu/pool/main/c/curl/curl_8.5.0-2ubuntu10.8.dsc' curl_8.5.0-2ubuntu10.8.dsc 3051 SHA512:cdff7efe8d9e9693e138fbe1ac018e0f0ace38d4fcd68f1829fb7eb2f506b592e048b56109a89a54a0032fc7faa9b77a1655af7f956eca1152b9dfa811ed943f
'http://archive.ubuntu.com/ubuntu/pool/main/c/curl/curl_8.5.0.orig.tar.gz' curl_8.5.0.orig.tar.gz 4372979 SHA512:1ff70e8fd5f233b373dea2a031d46698c03ed35f384c2eacbe9368f9daed65e91d7f45ade350c3ac3dd3d662c913b17cdc8702a0c23879b0c78fbd396fd0b926
'http://archive.ubuntu.com/ubuntu/pool/main/c/curl/curl_8.5.0-2ubuntu10.8.debian.tar.xz' curl_8.5.0-2ubuntu10.8.debian.tar.xz 68580 SHA512:77e8200e621f66172bc9b53c25d0c53dc5ec08add353c2c72f2584b6e0fb15937e01611c6c8d5795ad8d3186bf60327e4ddaf3b3d48cbac97f2d080c3a1ffc18
```

### `dpkg` source package: `cyrus-sasl2=2.1.28+dfsg1-5ubuntu3.1`

Binary Packages:

- `libsasl2-2:amd64=2.1.28+dfsg1-5ubuntu3.1`
- `libsasl2-modules-db:amd64=2.1.28+dfsg1-5ubuntu3.1`

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
$ apt-get source -qq --print-uris cyrus-sasl2=2.1.28+dfsg1-5ubuntu3.1
'http://archive.ubuntu.com/ubuntu/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.28%2bdfsg1-5ubuntu3.1.dsc' cyrus-sasl2_2.1.28+dfsg1-5ubuntu3.1.dsc 3501 SHA512:3a6f5d06ebf66b8f547eeae248414f9af7cc8a3f499d7d55d919e1c5b8a0851b624d28d48ea90a04d67261f350a890461156946909e83427e09237a8d90ed0bc
'http://archive.ubuntu.com/ubuntu/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.28%2bdfsg1.orig.tar.xz' cyrus-sasl2_2.1.28+dfsg1.orig.tar.xz 794540 SHA512:e94075d09b38a50138b782323de286deb7b15008064f07df4fa682e94367e829d9bfafef48d5478f730fef8fde536bcc6d54cab0452b76473a3c620b3dc18fa2
'http://archive.ubuntu.com/ubuntu/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.28%2bdfsg1-5ubuntu3.1.debian.tar.xz' cyrus-sasl2_2.1.28+dfsg1-5ubuntu3.1.debian.tar.xz 98324 SHA512:7e2fb71cd5693f9504158125385657920df46efcd63e28b14d0553772e2f2d906cd0c25425762e75adadec4a18715eee12c945dc4d27ce2d8c118efcb65175a5
```

### `dpkg` source package: `dash=0.5.12-6ubuntu5`

Binary Packages:

- `dash=0.5.12-6ubuntu5`

Licenses: (parsed from: `/usr/share/doc/dash/copyright`)

- `BSD-3-Clause`
- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `db5.3=5.3.28+dfsg2-7`

Binary Packages:

- `libdb5.3t64:amd64=5.3.28+dfsg2-7`

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

- http://snapshot.debian.org/package/db5.3/5.3.28+dfsg2-7/


### `dpkg` source package: `debconf=1.5.86ubuntu1`

Binary Packages:

- `debconf=1.5.86ubuntu1`

Licenses: (parsed from: `/usr/share/doc/debconf/copyright`)

- `BSD-2-clause`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `debianutils=5.17build1`

Binary Packages:

- `debianutils=5.17build1`

Licenses: (parsed from: `/usr/share/doc/debianutils/copyright`)

- `GPL-2`
- `GPL-2+`
- `SMAIL-GPL`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `diffutils=1:3.10-1build1`

Binary Packages:

- `diffutils=1:3.10-1build1`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `dpkg=1.22.6ubuntu6.5`

Binary Packages:

- `dpkg=1.22.6ubuntu6.5`

Licenses: (parsed from: `/usr/share/doc/dpkg/copyright`)

- `GPL-2`
- `GPL-2+`
- `public-domain-s-s-d`

Source:

```console
$ apt-get source -qq --print-uris dpkg=1.22.6ubuntu6.5
'http://archive.ubuntu.com/ubuntu/pool/main/d/dpkg/dpkg_1.22.6ubuntu6.5.dsc' dpkg_1.22.6ubuntu6.5.dsc 3156 SHA512:6c6f43612ac5f74937a2a83525ebb66a21af81e4678fd2b3bafbcb490e0e33be6a611b1475c205de378b64efdf7c615abd46b78c58b6c232145e7d2b75fe9d7b
'http://archive.ubuntu.com/ubuntu/pool/main/d/dpkg/dpkg_1.22.6ubuntu6.5.tar.xz' dpkg_1.22.6ubuntu6.5.tar.xz 5547360 SHA512:a52c556b632205b84bf8e795f68f54fe7e78b251561d032be76ecde9c5e3d9a74c5358476956ab8c3b2fb0266a5f4a03f3d67ec7039e62dc56905ee8c52d2d5d
```

### `dpkg` source package: `e2fsprogs=1.47.0-2.4~exp1ubuntu4.1`

Binary Packages:

- `e2fsprogs=1.47.0-2.4~exp1ubuntu4.1`
- `libcom-err2:amd64=1.47.0-2.4~exp1ubuntu4.1`
- `libext2fs2t64:amd64=1.47.0-2.4~exp1ubuntu4.1`
- `libss2:amd64=1.47.0-2.4~exp1ubuntu4.1`
- `logsave=1.47.0-2.4~exp1ubuntu4.1`

Licenses: (parsed from: `/usr/share/doc/e2fsprogs/copyright`, `/usr/share/doc/libcom-err2/copyright`, `/usr/share/doc/libext2fs2t64/copyright`, `/usr/share/doc/libss2/copyright`, `/usr/share/doc/logsave/copyright`)

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
$ apt-get source -qq --print-uris e2fsprogs=1.47.0-2.4~exp1ubuntu4.1
'http://archive.ubuntu.com/ubuntu/pool/main/e/e2fsprogs/e2fsprogs_1.47.0-2.4%7eexp1ubuntu4.1.dsc' e2fsprogs_1.47.0-2.4~exp1ubuntu4.1.dsc 3294 SHA512:0b9616118928aee8c2893dd1d6444735fd2c1852975414fbfeccb8d94bd01c34b49111282d728f835d539a17b6642b1c20509b17367b0bafc1d417b2910621b0
'http://archive.ubuntu.com/ubuntu/pool/main/e/e2fsprogs/e2fsprogs_1.47.0.orig.tar.gz' e2fsprogs_1.47.0.orig.tar.gz 9637717 SHA512:4f03a469d03cb0f0656bd17c64d944606fb25e68002e3e42c278f3775fee6bf776cc2061ae378b5df4f167a5c33444490111fdcbb140e0320445706f9d048dd0
'http://archive.ubuntu.com/ubuntu/pool/main/e/e2fsprogs/e2fsprogs_1.47.0.orig.tar.gz.asc' e2fsprogs_1.47.0.orig.tar.gz.asc 488 SHA512:cd3652ec12f694f1c1f5bd4af4964bb32ad832ba8a06a48864d12a998dc514e9a950ebdb475707a3abb8360852a3469794f2327f097328c99233beef575df144
'http://archive.ubuntu.com/ubuntu/pool/main/e/e2fsprogs/e2fsprogs_1.47.0-2.4%7eexp1ubuntu4.1.debian.tar.xz' e2fsprogs_1.47.0-2.4~exp1ubuntu4.1.debian.tar.xz 90580 SHA512:c95606b9d20cdfeacedf1b7fb7185406562117a71afaae5e1c246f30a510ba46abe79e12221503e3809a8595caa967835f640990dd41921ca6ec5abbea20a371
```

### `dpkg` source package: `empy=3.3.4-2`

Binary Packages:

- `python3-empy=3.3.4-2`

Licenses: (parsed from: `/usr/share/doc/python3-empy/copyright`)

- `GPL-2`
- `LGPL-2.1+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/empy/3.3.4-2/


### `dpkg` source package: `expat=2.6.1-2ubuntu0.4`

Binary Packages:

- `libexpat1:amd64=2.6.1-2ubuntu0.4`
- `libexpat1-dev:amd64=2.6.1-2ubuntu0.4`

Licenses: (parsed from: `/usr/share/doc/libexpat1/copyright`, `/usr/share/doc/libexpat1-dev/copyright`)

- `MIT`

Source:

```console
$ apt-get source -qq --print-uris expat=2.6.1-2ubuntu0.4
'http://archive.ubuntu.com/ubuntu/pool/main/e/expat/expat_2.6.1-2ubuntu0.4.dsc' expat_2.6.1-2ubuntu0.4.dsc 1945 SHA512:82a09968f6bdffeae412f3e96d26d09f43fc3e6a6c5bc57aa61eb6c589184d67f252ae3d36c30425dc8c7bcae62f15a745a13598bb9354a8d7b1fa5f8bf1cafe
'http://archive.ubuntu.com/ubuntu/pool/main/e/expat/expat_2.6.1.orig.tar.gz' expat_2.6.1.orig.tar.gz 8414649 SHA512:cf6c64fc0ca55dd172ca8a6ca10d1fb2c915d0f941b0068f42cb90488022dea73e04119c49a1bd4ab9a5d425ddc132ae5f22260ff6d2e25204637a1169e7bd4f
'http://archive.ubuntu.com/ubuntu/pool/main/e/expat/expat_2.6.1-2ubuntu0.4.debian.tar.xz' expat_2.6.1-2ubuntu0.4.debian.tar.xz 31092 SHA512:8d460f748c1b1d2e35805ec2f390b029841dc5dc0e3380205d65e12d30b3d15ea47c4572d13886192227a8a262224817fb90be75c75c43fcb299dee7bf6e545e
```

### `dpkg` source package: `findutils=4.9.0-5build1`

Binary Packages:

- `findutils=4.9.0-5build1`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `flake8-builtins=2.1.0-1`

Binary Packages:

- `python3-flake8-builtins=2.1.0-1`

Licenses: (parsed from: `/usr/share/doc/python3-flake8-builtins/copyright`)

- `GPL-2`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/flake8-builtins/2.1.0-1/


### `dpkg` source package: `flake8-comprehensions=3.14.0-1`

Binary Packages:

- `python3-flake8-comprehensions=3.14.0-1`

Licenses: (parsed from: `/usr/share/doc/python3-flake8-comprehensions/copyright`)

- `Expat`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/flake8-comprehensions/3.14.0-1/


### `dpkg` source package: `flake8-docstrings=1.6.0-2`

Binary Packages:

- `python3-flake8-docstrings=1.6.0-2`

Licenses: (parsed from: `/usr/share/doc/python3-flake8-docstrings/copyright`)

- `Expat`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/flake8-docstrings/1.6.0-2/


### `dpkg` source package: `flake8-import-order=0.18.2-2`

Binary Packages:

- `python3-flake8-import-order=0.18.2-2`

Licenses: (parsed from: `/usr/share/doc/python3-flake8-import-order/copyright`)

- `LGPL-3`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/flake8-import-order/0.18.2-2/


### `dpkg` source package: `flake8-quotes=3.4.0-1`

Binary Packages:

- `python3-flake8-quotes=3.4.0-1`

Licenses: (parsed from: `/usr/share/doc/python3-flake8-quotes/copyright`)

- `Expat`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/flake8-quotes/3.4.0-1/


### `dpkg` source package: `fmtlib=9.1.0+ds1-2`

Binary Packages:

- `libfmt-dev:amd64=9.1.0+ds1-2`
- `libfmt9:amd64=9.1.0+ds1-2`

Licenses: (parsed from: `/usr/share/doc/libfmt-dev/copyright`, `/usr/share/doc/libfmt9/copyright`)

- `BSD-2-Clause`
- `CC0-1.0`
- `Expat`
- `Expat with embedded exception`
- `Python`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/fmtlib/9.1.0+ds1-2/


### `dpkg` source package: `gcc-14=14.2.0-4ubuntu2~24.04.1`

Binary Packages:

- `gcc-14-base:amd64=14.2.0-4ubuntu2~24.04.1`
- `libatomic1:amd64=14.2.0-4ubuntu2~24.04.1`
- `libgcc-s1:amd64=14.2.0-4ubuntu2~24.04.1`
- `libgfortran5:amd64=14.2.0-4ubuntu2~24.04.1`
- `libstdc++6:amd64=14.2.0-4ubuntu2~24.04.1`

Licenses: (parsed from: `/usr/share/doc/gcc-14-base/copyright`, `/usr/share/doc/libatomic1/copyright`, `/usr/share/doc/libgcc-s1/copyright`, `/usr/share/doc/libgfortran5/copyright`, `/usr/share/doc/libstdc++6/copyright`)

- `Artistic`
- `GFDL-1.2`
- `GPL`
- `GPL-3`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris gcc-14=14.2.0-4ubuntu2~24.04.1
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-14/gcc-14_14.2.0-4ubuntu2%7e24.04.1.dsc' gcc-14_14.2.0-4ubuntu2~24.04.1.dsc 46930 SHA512:e73c3c31529bf34e4cc91360a18ceed91c752bcd8344da68a0b9e9a178b0981fac02e88f12861b4dc60b261fe51fe931b4b27955d39191bc2c84142d704f4d51
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-14/gcc-14_14.2.0.orig.tar.gz' gcc-14_14.2.0.orig.tar.gz 97158172 SHA512:88621e344786a78d825110dbd46a9dc811ab0a3414bde97a700b0c90991020dc31dbba89cdbed24ef2875a63ae9c0adffdbc1064262e5270d80920c9964bfb21
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-14/gcc-14_14.2.0-4ubuntu2%7e24.04.1.debian.tar.xz' gcc-14_14.2.0-4ubuntu2~24.04.1.debian.tar.xz 1950432 SHA512:039f728b7fd2256dad82e120d48dbec7fbece9c1fb5bbfca9019312d5a4e6a799d2c81fa09b377b850375a89be262aa080587df562f4bd6b7b6eba17ab9e29f9
```

### `dpkg` source package: `glibc=2.39-0ubuntu8.7`

Binary Packages:

- `libc-bin=2.39-0ubuntu8.7`
- `libc-dev-bin=2.39-0ubuntu8.7`
- `libc6:amd64=2.39-0ubuntu8.7`
- `libc6-dev:amd64=2.39-0ubuntu8.7`

Licenses: (parsed from: `/usr/share/doc/libc-bin/copyright`, `/usr/share/doc/libc-dev-bin/copyright`, `/usr/share/doc/libc6/copyright`, `/usr/share/doc/libc6-dev/copyright`)

- `GFDL-1.3`
- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris glibc=2.39-0ubuntu8.7
'http://archive.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.39-0ubuntu8.7.dsc' glibc_2.39-0ubuntu8.7.dsc 9257 SHA512:413efc529754f26d91d4c9efb8b697df56dce1650c58016463795c487e9c11e6c296ee97ae652a1a4d395921075b85929ac02c649e19e5ecb2c24a300942003f
'http://archive.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.39.orig.tar.xz' glibc_2.39.orig.tar.xz 18520988 SHA512:818f58172a52815b4338ea9f2a69ecaa3335492b9f8f64cbf8afb24c0d737982341968ecd79631cae3d3074ab0ae4bc6056fc4ba3ffe790849dc374835cd57e2
'http://archive.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.39.orig.tar.xz.asc' glibc_2.39.orig.tar.xz.asc 833 SHA512:5c054af523bbf5c2453363c023eadd1a75b6a5ff55c739011030115d3b117dbfc7d80cc74fbf157ea74a8d24aa14ff560c675374f875ec5c1ed3030e26a5ee07
'http://archive.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.39-0ubuntu8.7.debian.tar.xz' glibc_2.39-0ubuntu8.7.debian.tar.xz 469880 SHA512:12758ed1b5e0337ad202f8a66332fdbea8a217531a2a01819847d08207afa65b114943d712b8b27f83f0f370c07371fddd9ed20661f683fbb4d9386cd4f57893
```

### `dpkg` source package: `gmp=2:6.3.0+dfsg-2ubuntu6.1`

Binary Packages:

- `libgmp10:amd64=2:6.3.0+dfsg-2ubuntu6.1`

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
$ apt-get source -qq --print-uris gmp=2:6.3.0+dfsg-2ubuntu6.1
'http://archive.ubuntu.com/ubuntu/pool/main/g/gmp/gmp_6.3.0%2bdfsg-2ubuntu6.1.dsc' gmp_6.3.0+dfsg-2ubuntu6.1.dsc 2345 SHA512:e6e58b32456ebc4fcb86e1a82553030439ff5c26bbbf48d9a26bca5ebab4d0f81fb587f262a94f8e7158edb14b538bcf3f5bc0ed0bd32ea5b1d950820b286a88
'http://archive.ubuntu.com/ubuntu/pool/main/g/gmp/gmp_6.3.0%2bdfsg.orig.tar.xz' gmp_6.3.0+dfsg.orig.tar.xz 1870556 SHA512:a422b29024464aeb26c69f64be1bc37407d74e0290f44f67fc040fe38b97f3eb7aa6ba8380722ef36cac39816d1c4f24b771159fb86d5979ef0791dcdef708bc
'http://archive.ubuntu.com/ubuntu/pool/main/g/gmp/gmp_6.3.0%2bdfsg-2ubuntu6.1.debian.tar.xz' gmp_6.3.0+dfsg-2ubuntu6.1.debian.tar.xz 38908 SHA512:6c64c2cacd9736f7bd88fe6364a2f6f7281d0f3031b602d3dbfed8b9035bc2f024462498dda0efdec4d3a411d15a80c6c8fa3283c149d3d0fb2f77665c470880
```

### `dpkg` source package: `gnupg2=2.4.4-2ubuntu17.4`

Binary Packages:

- `dirmngr=2.4.4-2ubuntu17.4`
- `gnupg=2.4.4-2ubuntu17.4`
- `gnupg-utils=2.4.4-2ubuntu17.4`
- `gnupg2=2.4.4-2ubuntu17.4`
- `gpg=2.4.4-2ubuntu17.4`
- `gpg-agent=2.4.4-2ubuntu17.4`
- `gpgconf=2.4.4-2ubuntu17.4`
- `gpgsm=2.4.4-2ubuntu17.4`
- `gpgv=2.4.4-2ubuntu17.4`
- `keyboxd=2.4.4-2ubuntu17.4`

Licenses: (parsed from: `/usr/share/doc/dirmngr/copyright`, `/usr/share/doc/gnupg/copyright`, `/usr/share/doc/gnupg-utils/copyright`, `/usr/share/doc/gnupg2/copyright`, `/usr/share/doc/gpg/copyright`, `/usr/share/doc/gpg-agent/copyright`, `/usr/share/doc/gpgconf/copyright`, `/usr/share/doc/gpgsm/copyright`, `/usr/share/doc/gpgv/copyright`, `/usr/share/doc/keyboxd/copyright`)

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
$ apt-get source -qq --print-uris gnupg2=2.4.4-2ubuntu17.4
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnupg2/gnupg2_2.4.4-2ubuntu17.4.dsc' gnupg2_2.4.4-2ubuntu17.4.dsc 3984 SHA512:a6a2f49070db5db2bb85b7fd916728ed4e24e21e2746b2386b27f5573c13f9c2d9d55deabeac1fd9c0ce977d66706157a31e1ed386d663d1962176d3c0df74de
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnupg2/gnupg2_2.4.4.orig.tar.bz2' gnupg2_2.4.4.orig.tar.bz2 7886036 SHA512:3d1a3b08d1ce2319d238d8be96591e418ede1dc0b4ede33a4cc2fe40e9c56d5bbc27b1984736d8a786e7f292ddbc836846a8bdb4bf89f064e953c37cb54b94ef
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnupg2/gnupg2_2.4.4.orig.tar.bz2.asc' gnupg2_2.4.4.orig.tar.bz2.asc 386 SHA512:abb44c8bfa59e589bdcd660f1d1a2e268bade8729d95b34263e3d3b5388d1d2276420313989777938f17f97739c554808f97a63257ca0f53d2122a346d70ec85
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnupg2/gnupg2_2.4.4-2ubuntu17.4.debian.tar.xz' gnupg2_2.4.4-2ubuntu17.4.debian.tar.xz 97376 SHA512:61b874e2aa964df31649d1344281b7f99f1bde0b414719f1ff525f2e631729480d0eabf3c3e94643178a6674b3816e40ea92658e84ace8474351ef35620a464b
```

### `dpkg` source package: `gnutls28=3.8.3-1.1ubuntu3.5`

Binary Packages:

- `libgnutls30t64:amd64=3.8.3-1.1ubuntu3.5`

Licenses: (parsed from: `/usr/share/doc/libgnutls30t64/copyright`)

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
$ apt-get source -qq --print-uris gnutls28=3.8.3-1.1ubuntu3.5
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.8.3-1.1ubuntu3.5.dsc' gnutls28_3.8.3-1.1ubuntu3.5.dsc 3397 SHA512:f27e044c5a43a466d94883b9578e7e5b8dda3b807de4dbbf533e34701c2146f43696260a47c18bf85d8801db1ab457d5a6772741f0f1dffcd31120203181ad5d
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.8.3.orig.tar.xz' gnutls28_3.8.3.orig.tar.xz 6463720 SHA512:74eddba01ce4c2ffdca781c85db3bb52c85f1db3c09813ee2b8ceea0608f92ca3912fd9266f55deb36a8ba4d01802895ca5d5d219e7d9caec45e1a8534e45a84
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.8.3.orig.tar.xz.asc' gnutls28_3.8.3.orig.tar.xz.asc 854 SHA512:8a13a834b57172b9504313eeb7d733d2c3d72971dd8adaa837bbd9d73b12fe2a67f7d07fbbaf643a34ff95acaa82458a88ce4118152ede8ece9be5a089b693c8
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.8.3-1.1ubuntu3.5.debian.tar.xz' gnutls28_3.8.3-1.1ubuntu3.5.debian.tar.xz 109884 SHA512:66368bfc1a4266368bef58642388468f00e6da678632b7d7fb3d19c06f95d8b5187be80732d1b1b3c38dd1cdc280fc978b73e5f25a88baa74129e2185258e819
```

### `dpkg` source package: `googletest=1.14.0-1`

Binary Packages:

- `google-mock:amd64=1.14.0-1`
- `googletest=1.14.0-1`
- `libgtest-dev:amd64=1.14.0-1`

Licenses: (parsed from: `/usr/share/doc/google-mock/copyright`, `/usr/share/doc/googletest/copyright`, `/usr/share/doc/libgtest-dev/copyright`)

- `BSD-C3`
- `GAP`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/googletest/1.14.0-1/


### `dpkg` source package: `grep=3.11-4build1`

Binary Packages:

- `grep=3.11-4build1`

Licenses: (parsed from: `/usr/share/doc/grep/copyright`)

- `GPL-3`
- `GPL-3+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `gzip=1.12-1ubuntu3.1`

Binary Packages:

- `gzip=1.12-1ubuntu3.1`

Licenses: (parsed from: `/usr/share/doc/gzip/copyright`)

- `FSF-manpages`
- `GFDL-1.3+-no-invariant`
- `GFDL-3`
- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris gzip=1.12-1ubuntu3.1
'http://archive.ubuntu.com/ubuntu/pool/main/g/gzip/gzip_1.12-1ubuntu3.1.dsc' gzip_1.12-1ubuntu3.1.dsc 2042 SHA512:724f7290e5acc87e29768d9cbfa191760f3558778f2c059689535b5bccf5738ceb6f341c301e9730703060bae88e7022c396a026b7d83abfe030fe4d8619b83d
'http://archive.ubuntu.com/ubuntu/pool/main/g/gzip/gzip_1.12.orig.tar.xz' gzip_1.12.orig.tar.xz 825548 SHA512:116326fe991828227de150336a0c016f4fe932dfbb728a16b4a84965256d9929574a4f5cfaf3cf6bb4154972ef0d110f26ab472c93e62ec9a5fd7a5d65abea24
'http://archive.ubuntu.com/ubuntu/pool/main/g/gzip/gzip_1.12-1ubuntu3.1.debian.tar.xz' gzip_1.12-1ubuntu3.1.debian.tar.xz 21180 SHA512:e7353110d35f58a3a5628f05f05a1744112715e9691b3c17aa0b4d0e8441997bb06c2e1d4ddbda9a4f7decadb561b43b808bab25a57f6a146c124336bc1f16ec
```

### `dpkg` source package: `hostname=3.23+nmu2ubuntu2`

Binary Packages:

- `hostname=3.23+nmu2ubuntu2`

Licenses: (parsed from: `/usr/share/doc/hostname/copyright`)

- `GPL-2`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `icu=74.2-1ubuntu3.1`

Binary Packages:

- `libicu74:amd64=74.2-1ubuntu3.1`

Licenses: (parsed from: `/usr/share/doc/libicu74/copyright`)

- `GPL-3`
- `MIT`

Source:

```console
$ apt-get source -qq --print-uris icu=74.2-1ubuntu3.1
'http://archive.ubuntu.com/ubuntu/pool/main/i/icu/icu_74.2-1ubuntu3.1.dsc' icu_74.2-1ubuntu3.1.dsc 2350 SHA512:97c4d28b6887488adcf0079fbb43ec668ba2f38b9b924c391989316e6698c48fe430e5b7dd8cf5323915becbb98fe1748e19ce19402d2a3ed8416bd465de2d9a
'http://archive.ubuntu.com/ubuntu/pool/main/i/icu/icu_74.2.orig.tar.gz' icu_74.2.orig.tar.gz 26618071 SHA512:0cbe29122370ba03a8fb5b0f1494f598748044ad2aa4d66ba65fe98ebeb88da2d73d324ad6bfc44e004846e0ab5c9a34d1fdf3d6bdb3095c0d47e929b943e6db
'http://archive.ubuntu.com/ubuntu/pool/main/i/icu/icu_74.2.orig.tar.gz.asc' icu_74.2.orig.tar.gz.asc 659 SHA512:e961664f91a66afe898041fb42950f925854cfe7f5a287f691b90ad79c215a14300cdd1aad94a310aa2b1cdda3d850ab978d1fe2eadba5fd46f375f4bcefcd11
'http://archive.ubuntu.com/ubuntu/pool/main/i/icu/icu_74.2-1ubuntu3.1.debian.tar.xz' icu_74.2-1ubuntu3.1.debian.tar.xz 64432 SHA512:967f2dfd11ea2a11f0cee4558b78b067ae2e169d279b39a1f2796457554f9147f23bb79c9f7873314c197f6a17598a989a58ab7bd3f12d49f0ec5b71a9666ed4
```

### `dpkg` source package: `init-system-helpers=1.66ubuntu1`

Binary Packages:

- `init-system-helpers=1.66ubuntu1`

Licenses: (parsed from: `/usr/share/doc/init-system-helpers/copyright`)

- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `keyutils=1.6.3-3build1`

Binary Packages:

- `libkeyutils1:amd64=1.6.3-3build1`

Licenses: (parsed from: `/usr/share/doc/libkeyutils1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2`
- `LGPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `kmod=31+20240202-2ubuntu7.1`

Binary Packages:

- `libkmod2:amd64=31+20240202-2ubuntu7.1`

Licenses: (parsed from: `/usr/share/doc/libkmod2/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris kmod=31+20240202-2ubuntu7.1
'http://archive.ubuntu.com/ubuntu/pool/main/k/kmod/kmod_31%2b20240202-2ubuntu7.1.dsc' kmod_31+20240202-2ubuntu7.1.dsc 2288 SHA512:64558f5c34ab88a3eb2d87b138efc6a6e9e23e30e67d1c8ca8c654c5fe9db5386ba23191184031e573e33995bc22257ac13ee3cca01e0ea10f1fd97af1c60c16
'http://archive.ubuntu.com/ubuntu/pool/main/k/kmod/kmod_31%2b20240202.orig.tar.xz' kmod_31+20240202.orig.tar.xz 253852 SHA512:9f9f344fbbcde8d3d479ff0c48adabb96442ccdf4190dcfde1c5ee797e2e85c6518b4a9d9451ebb0cf6d36364cd3e6a8f4301f87659b6b9b0b0cb0c7d3535a93
'http://archive.ubuntu.com/ubuntu/pool/main/k/kmod/kmod_31%2b20240202-2ubuntu7.1.debian.tar.xz' kmod_31+20240202-2ubuntu7.1.debian.tar.xz 15108 SHA512:e4c0c7aaec0900878ffafa2511e177fcde2a3a3b8178daa39e4f8e3546259be08401b770bfd111b78f2083571de3557da3524a75026b6d6eb3cd58859e379fac
```

### `dpkg` source package: `krb5=1.20.1-6ubuntu2.6`

Binary Packages:

- `libgssapi-krb5-2:amd64=1.20.1-6ubuntu2.6`
- `libk5crypto3:amd64=1.20.1-6ubuntu2.6`
- `libkrb5-3:amd64=1.20.1-6ubuntu2.6`
- `libkrb5support0:amd64=1.20.1-6ubuntu2.6`

Licenses: (parsed from: `/usr/share/doc/libgssapi-krb5-2/copyright`, `/usr/share/doc/libk5crypto3/copyright`, `/usr/share/doc/libkrb5-3/copyright`, `/usr/share/doc/libkrb5support0/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris krb5=1.20.1-6ubuntu2.6
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.20.1-6ubuntu2.6.dsc' krb5_1.20.1-6ubuntu2.6.dsc 4125 SHA512:6bafe41a37f8bf133ccd7e1aa0d63a1464b411af60ee408a03de69debae259794606011ff42370d168f6bf74af34d90b635c007c9876657af7124259af84c99a
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.20.1.orig.tar.gz' krb5_1.20.1.orig.tar.gz 8661660 SHA512:6f57479f13f107cd84f30de5c758eb6b9fc59171329c13e5da6073b806755f8d163eb7bd84767ea861ad6458ea0c9eeb00ee044d3bcad01ef136e9888564b6a2
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.20.1.orig.tar.gz.asc' krb5_1.20.1.orig.tar.gz.asc 833 SHA512:1d3312bd67581e07adfdadf2c5fe394179631d8add8bd075efefe982a0de22369004e60a14422d426382c8c591e4181b9897088afe9d4e86f0b5a97e5954c67a
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.20.1-6ubuntu2.6.debian.tar.xz' krb5_1.20.1-6ubuntu2.6.debian.tar.xz 122284 SHA512:402e34a374db1ece1ce0a604d84d697c590596d5e99601895d9c50c96fcbd8cb08d21b04201296411324b3ae4f169f2295aff825cee182cbbf139ccb16588fc9
```

### `dpkg` source package: `lapack=3.12.0-3build1.1`

Binary Packages:

- `libblas3:amd64=3.12.0-3build1.1`
- `liblapack3:amd64=3.12.0-3build1.1`

Licenses: (parsed from: `/usr/share/doc/libblas3/copyright`, `/usr/share/doc/liblapack3/copyright`)

- `BSD-3-clause`
- `BSD-3-clause-intel`

Source:

```console
$ apt-get source -qq --print-uris lapack=3.12.0-3build1.1
'http://archive.ubuntu.com/ubuntu/pool/main/l/lapack/lapack_3.12.0-3build1.1.dsc' lapack_3.12.0-3build1.1.dsc 3417 SHA512:76e42e9014e007655171abcca32667d3d200dd35bc9fc5cca0a1402e79cfb56132334fbc2c19493f9dde445c101a1ac34aa46af3fcea2c5a468a2435ab293c4d
'http://archive.ubuntu.com/ubuntu/pool/main/l/lapack/lapack_3.12.0.orig.tar.gz' lapack_3.12.0.orig.tar.gz 7933607 SHA512:f8f3c733a0221be0b3f5618235408ac59cbd4e5f1c4eab5f509b831a6ec6a9ef14b8849aa6ea10810df1aff90186ca454d15e9438d1dd271c2449d42d3da9dda
'http://archive.ubuntu.com/ubuntu/pool/main/l/lapack/lapack_3.12.0-3build1.1.debian.tar.xz' lapack_3.12.0-3build1.1.debian.tar.xz 28916 SHA512:42ca6ffeaec371df0f7242aa6fa932a9cfc3044baa941063dae3be23a4645c5c12e94e51d6c20969a1f5627dbedd165c7e72532d336379fb70248338fed89242
```

### `dpkg` source package: `libarchive=3.7.2-2ubuntu0.6`

Binary Packages:

- `libarchive13t64:amd64=3.7.2-2ubuntu0.6`

Licenses: (parsed from: `/usr/share/doc/libarchive13t64/copyright`)

- `Apache-2.0`
- `BSD-1-clause-UCB`
- `BSD-124-clause-UCB`
- `BSD-2-clause`
- `BSD-3-clause-UCB`
- `BSD-4-clause-UCB`
- `CC0-1.0`
- `Expat`
- `OpenSSL+SSLeay`
- `PD`

Source:

```console
$ apt-get source -qq --print-uris libarchive=3.7.2-2ubuntu0.6
'http://archive.ubuntu.com/ubuntu/pool/main/liba/libarchive/libarchive_3.7.2-2ubuntu0.6.dsc' libarchive_3.7.2-2ubuntu0.6.dsc 2733 SHA512:1391a0262aace597c13c9ca49ab66bf962edc2a119a726271a9d11d3469cd664881b8e5e18ab3e0a0368f2b44e12ebc3a80a417530bf37ab86f142afb71b08cf
'http://archive.ubuntu.com/ubuntu/pool/main/liba/libarchive/libarchive_3.7.2.orig.tar.xz' libarchive_3.7.2.orig.tar.xz 5237056 SHA512:a21bebb27b808cb7d2ed13a70739904a1b7b55661d8dea83c9897a0129cf71e20c962f13666c571782ff0f4f753ca885619c2097d9e7691c2dee4e6e4b9a2971
'http://archive.ubuntu.com/ubuntu/pool/main/liba/libarchive/libarchive_3.7.2.orig.tar.xz.asc' libarchive_3.7.2.orig.tar.xz.asc 659 SHA512:c2ce850088245d7723720737d74d1cc1819984d01b3f9e4ed96b0757f4c6d6d511b78792181a12400c563632d74edcd0c2c3a4b7527cba40ada7ef74488078fc
'http://archive.ubuntu.com/ubuntu/pool/main/liba/libarchive/libarchive_3.7.2-2ubuntu0.6.debian.tar.xz' libarchive_3.7.2-2ubuntu0.6.debian.tar.xz 38028 SHA512:61ad04e7c320b27130bc8cbd930e43e6874028b13ae059e1580461a4e7f904d58c2d800221f57d81a2fe956579e87a9b3045f79bc4ab44eb944f440ece06283e
```

### `dpkg` source package: `libassuan=2.5.6-1build1`

Binary Packages:

- `libassuan0:amd64=2.5.6-1build1`

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


### `dpkg` source package: `libcap-ng=0.8.4-2build2`

Binary Packages:

- `libcap-ng0:amd64=0.8.4-2build2`

Licenses: (parsed from: `/usr/share/doc/libcap-ng0/copyright`)

- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `LGPL-2.1`
- `LGPL-2.1+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libcap2=1:2.66-5ubuntu2.2`

Binary Packages:

- `libcap2:amd64=1:2.66-5ubuntu2.2`

Licenses: (parsed from: `/usr/share/doc/libcap2/copyright`)

- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris libcap2=1:2.66-5ubuntu2.2
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap2/libcap2_2.66-5ubuntu2.2.dsc' libcap2_2.66-5ubuntu2.2.dsc 2319 SHA512:563c9151918f788fb7ea210505c3f2f4c6375af6fa58f760d4efd051ac3bcb9a0dff8fc0407486c834b5a477831af8a50aaeb14728c93ffe88edf48e2a86391f
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap2/libcap2_2.66.orig.tar.xz' libcap2_2.66.orig.tar.xz 181592 SHA512:ac005b622f6e065f30ce282a5c87240e7b9da75366ee537aa4835bc501b44bc242c10a4ba4dc070e2415fc7f635d1c3c4e45fbeeaf962cf7973dda82bf6377f0
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap2/libcap2_2.66-5ubuntu2.2.debian.tar.xz' libcap2_2.66-5ubuntu2.2.debian.tar.xz 23076 SHA512:fd58def706a8d3f3f594ad986bf9385c2cba8af6f73f4bb04011815fe8b1e700368a2a15e7390842b3aba9ae72de9928009731bf1f318b48d8975e505f8f7f33
```

### `dpkg` source package: `libffi=3.4.6-1build1`

Binary Packages:

- `libffi8:amd64=3.4.6-1build1`

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


### `dpkg` source package: `libgcrypt20=1.10.3-2build1`

Binary Packages:

- `libgcrypt20:amd64=1.10.3-2build1`

Licenses: (parsed from: `/usr/share/doc/libgcrypt20/copyright`)

- `GPL-2`
- `LGPL`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libgpg-error=1.47-3build2.1`

Binary Packages:

- `libgpg-error0:amd64=1.47-3build2.1`

Licenses: (parsed from: `/usr/share/doc/libgpg-error0/copyright`)

- `BSD-3-clause`
- `GPL-3`
- `GPL-3+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `g10-permissive`

Source:

```console
$ apt-get source -qq --print-uris libgpg-error=1.47-3build2.1
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgpg-error/libgpg-error_1.47-3build2.1.dsc' libgpg-error_1.47-3build2.1.dsc 3007 SHA512:4123fef7fe452ad802c1f3d38e63d9bfc0b97610a9b32359316a5cb1fc4d85e7842804360e341e0ad9e52d876c5a0a992a76d094a9c08831af829c6462bfa127
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgpg-error/libgpg-error_1.47.orig.tar.bz2' libgpg-error_1.47.orig.tar.bz2 1020862 SHA512:bbb4b15dae75856ee5b1253568674b56ad155524ae29a075cb5b0a7e74c4af685131775c3ea2226fff2f84ef80855e77aa661645d002b490a795c7ae57b66a30
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgpg-error/libgpg-error_1.47.orig.tar.bz2.asc' libgpg-error_1.47.orig.tar.bz2.asc 228 SHA512:babf3a17429aa7ad5d952099ea8d21bb5c9ba1bc74ea46f3027e0293449c32365208a05e141fa0bf033491320679b0b212f49919452f3dc63cce5d7f355d7195
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgpg-error/libgpg-error_1.47-3build2.1.debian.tar.xz' libgpg-error_1.47-3build2.1.debian.tar.xz 18776 SHA512:7e9c008e3d0501fe45d0f9b342d8a8bf88ef7995bba63b458aa419a4592606ad71f731c54287e6e32e6533c84420206f97f8e031a999df6d57a8fd45328f6f55
```

### `dpkg` source package: `libidn2=2.3.7-2build1.1`

Binary Packages:

- `libidn2-0:amd64=2.3.7-2build1.1`

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
$ apt-get source -qq --print-uris libidn2=2.3.7-2build1.1
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libidn2/libidn2_2.3.7-2build1.1.dsc' libidn2_2.3.7-2build1.1.dsc 2651 SHA512:5e382469d7280794c3eac36d0837cdf31bf2719e1dd6332d428da56de2960e7375558e65102359bb46af8c23724cf8d812a2900d36deb70d977e2069dc82db32
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libidn2/libidn2_2.3.7.orig.tar.gz' libidn2_2.3.7.orig.tar.gz 2155214 SHA512:eab5702bc0baed45492f8dde43a4d2ea3560ad80645e5f9e0cfa8d3b57bccd7fd782d04638e000ba07924a5d9f85e760095b55189188c4017b94705bef9b4a66
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libidn2/libidn2_2.3.7.orig.tar.gz.asc' libidn2_2.3.7.orig.tar.gz.asc 228 SHA512:00e5f8c3b6b1aef9ee341db99b339217080a57dbe65fba56798d60ad4be971a9535d8ae27e1f243b18b9fc9e900ada6c452b040a6c8094d5e05d8a76d1d79c03
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libidn2/libidn2_2.3.7-2build1.1.debian.tar.xz' libidn2_2.3.7-2build1.1.debian.tar.xz 16468 SHA512:5f8a3e69bcf2dfe58617153b4da23ea1fd9cf9c6aaf894045b8e8f6cb2ab0d8ce73df204fe165fd7ebad3dfda1ddfc1b1442ce5c99fa00d224e3924df64e133c
```

### `dpkg` source package: `libjsoncpp=1.9.5-6build1`

Binary Packages:

- `libjsoncpp25:amd64=1.9.5-6build1`

Licenses: (parsed from: `/usr/share/doc/libjsoncpp25/copyright`)

- `Expat_or_PublicDomain_or_DualExpatPD`
- `GPL-3`
- `GPL-3+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libksba=1.6.6-1build1`

Binary Packages:

- `libksba8:amd64=1.6.6-1build1`

Licenses: (parsed from: `/usr/share/doc/libksba8/copyright`)

- `FSFUL`
- `GPL-3`
- `LGPL-2.1-or-later`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libmd=1.1.0-2build1.1`

Binary Packages:

- `libmd0:amd64=1.1.0-2build1.1`

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
$ apt-get source -qq --print-uris libmd=1.1.0-2build1.1
'http://archive.ubuntu.com/ubuntu/pool/main/libm/libmd/libmd_1.1.0-2build1.1.dsc' libmd_1.1.0-2build1.1.dsc 2391 SHA512:f8b23db30a025da74030294c8580158376e908df287cf62cd8d7901e600c015514080a48a069d141c86ab7d157a9dce220d1186a9d6d693fe6916ffa5747b289
'http://archive.ubuntu.com/ubuntu/pool/main/libm/libmd/libmd_1.1.0.orig.tar.xz' libmd_1.1.0.orig.tar.xz 271228 SHA512:5d0da3337038e474fae7377bbc646d17214e72dc848a7aadc157f49333ce7b5ac1456e45d13674bd410ea08477c6115fc4282fed6c8e6a0bf63537a418c0df96
'http://archive.ubuntu.com/ubuntu/pool/main/libm/libmd/libmd_1.1.0.orig.tar.xz.asc' libmd_1.1.0.orig.tar.xz.asc 833 SHA512:b0ff3baa7eedc205ee6f8b844859145fa6922c39e8f62f1e997851a65b2881649b438a37baa5800d140541da6f4dacc9f92a370f945d7461937b8cdedeca1cef
'http://archive.ubuntu.com/ubuntu/pool/main/libm/libmd/libmd_1.1.0-2build1.1.debian.tar.xz' libmd_1.1.0-2build1.1.debian.tar.xz 8448 SHA512:b013b32fbc71ca9195e4ce9b25f5440cf746e539d72090a0f50e226783ee4885050f8e245fe75fe76775c84d6dcaf6ce684cbd9dd89d09265fae3c9f27a885af
```

### `dpkg` source package: `libpsl=0.21.2-1.1build1`

Binary Packages:

- `libpsl5t64:amd64=0.21.2-1.1build1`

Licenses: (parsed from: `/usr/share/doc/libpsl5t64/copyright`)

- `Chromium`
- `MIT`
- `gnulib`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libseccomp=2.5.5-1ubuntu3.1`

Binary Packages:

- `libseccomp2:amd64=2.5.5-1ubuntu3.1`

Licenses: (parsed from: `/usr/share/doc/libseccomp2/copyright`)

- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libseccomp=2.5.5-1ubuntu3.1
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libseccomp/libseccomp_2.5.5-1ubuntu3.1.dsc' libseccomp_2.5.5-1ubuntu3.1.dsc 2838 SHA512:bb64748ac6031e104c70a59a06e1b00ab4c516e3342b2bef50a7cd0dcf4fe3bfc316288da871994cfe39b42da968831efb20a8c51c3df74ab82983d9ecffdfc4
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libseccomp/libseccomp_2.5.5.orig.tar.gz' libseccomp_2.5.5.orig.tar.gz 642445 SHA512:f630e7a7e53a21b7ccb4d3e7b37616b89aeceba916677c8e3032830411d77a14c2d74dcf594cd193b1acc11f52595072e28316dc44300e54083d5d7b314a38da
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libseccomp/libseccomp_2.5.5.orig.tar.gz.asc' libseccomp_2.5.5.orig.tar.gz.asc 833 SHA512:a32a7146598f9183179ad15603181d1066e806d01f7c5f215d5405ad8618c06a265d05fff3b4a6cc49c50a577d93d6b920e85f6a581786b3db7389f52a4638e2
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libseccomp/libseccomp_2.5.5-1ubuntu3.1.debian.tar.xz' libseccomp_2.5.5-1ubuntu3.1.debian.tar.xz 24484 SHA512:89e68d82dd1985352e7ff0057fb1682c6b5beb0857c7329034d696bdc81e880f395309f065c23ff1f92ac7ad1a3c5ca46fe264309ce2be7dcbd0367d9e39cbde
```

### `dpkg` source package: `libselinux=3.5-2ubuntu2.1`

Binary Packages:

- `libselinux1:amd64=3.5-2ubuntu2.1`

Licenses: (parsed from: `/usr/share/doc/libselinux1/copyright`)

- `GPL-2`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris libselinux=3.5-2ubuntu2.1
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libselinux/libselinux_3.5-2ubuntu2.1.dsc' libselinux_3.5-2ubuntu2.1.dsc 3098 SHA512:bcf60f1ab7020ca57ad20b8b4dbd3d6c0b0f97a768c1c0c047c562a2b50ed8c73ffa13c002729ef7aba353768c03e72749d29fc9882982a531fda950b3a17de8
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libselinux/libselinux_3.5.orig.tar.gz' libselinux_3.5.orig.tar.gz 211453 SHA512:4e13261a5821018a5f3cdce676f180bb62e5bc225981ca8a498ece0d1c88d9ba8eaa0ce4099dd0849309a8a7c5a9a0953df841a9922f2c284e5a109e5d937ba7
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libselinux/libselinux_3.5.orig.tar.gz.asc' libselinux_3.5.orig.tar.gz.asc 981 SHA512:ba486d29c92801a02f75213ef5bcc4a0c4a87afe9dfa797aa9bb495ded40f21e37b22d6ea114c0e480d669b090d1116e8b9cac9fa9ea29678d3647bc58d8bb29
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libselinux/libselinux_3.5-2ubuntu2.1.debian.tar.xz' libselinux_3.5-2ubuntu2.1.debian.tar.xz 38112 SHA512:0e09406649d1a80e9c96b7791a2e4fbf6b5818b21d3ffa40dd2191c92be737cd506cd21ea375f25f2582e3a9bfc75d157816e33473b2ad676dcb3d346743e9a4
```

### `dpkg` source package: `libsemanage=3.5-1build5`

Binary Packages:

- `libsemanage-common=3.5-1build5`
- `libsemanage2:amd64=3.5-1build5`

Licenses: (parsed from: `/usr/share/doc/libsemanage-common/copyright`, `/usr/share/doc/libsemanage2/copyright`)

- `GPL-2`
- `LGPL-2.1`
- `LGPL-2.1+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libsepol=3.5-2build1`

Binary Packages:

- `libsepol2:amd64=3.5-2build1`

Licenses: (parsed from: `/usr/share/doc/libsepol2/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `Zlib`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libssh=0.10.6-2ubuntu0.4`

Binary Packages:

- `libssh-4:amd64=0.10.6-2ubuntu0.4`

Licenses: (parsed from: `/usr/share/doc/libssh-4/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `LGPL-2.1`
- `LGPL-2.1+~OpenSSL`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris libssh=0.10.6-2ubuntu0.4
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libssh/libssh_0.10.6-2ubuntu0.4.dsc' libssh_0.10.6-2ubuntu0.4.dsc 2723 SHA512:ac04327b00245b0587b437293e7294bdb42f62463e1213a335e5ddb52d80332bb1abe0b7d7bea2a80ef7bd60597aeb809a9c657632d17c02d088af35b7e2c4d7
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libssh/libssh_0.10.6.orig.tar.xz' libssh_0.10.6.orig.tar.xz 561036 SHA512:40c62d63c44e882999b71552c237d73fc7364313bd00b15a211a34aeff1b73693da441d2c8d4e40108d00fb7480ec7c5b6d472f9c0784b2359a179632ab0d6c1
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libssh/libssh_0.10.6.orig.tar.xz.asc' libssh_0.10.6.orig.tar.xz.asc 833 SHA512:214d7920bebc80a8e6838c64ed06e070709a96fabfb4fff657b55f9588bc0e1612887fe887d23de73ad3540f3bb85288e62eb6a11ccd4bc80afbd44d34ba70d4
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libssh/libssh_0.10.6-2ubuntu0.4.debian.tar.xz' libssh_0.10.6-2ubuntu0.4.debian.tar.xz 56400 SHA512:6cbb685d4e981014fa7aa01509ead2ab95ce665ed94d2ccbeb2c8394e972c40567543cd7e9e9cd6eba77af1ff9212dd2493a9e45150179caaa6c40a7c4e2fa9b
```

### `dpkg` source package: `libtasn1-6=4.19.0-3ubuntu0.24.04.2`

Binary Packages:

- `libtasn1-6:amd64=4.19.0-3ubuntu0.24.04.2`

Licenses: (parsed from: `/usr/share/doc/libtasn1-6/copyright`)

- `GFDL-1.3`
- `GPL-3`
- `LGPL`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libtasn1-6=4.19.0-3ubuntu0.24.04.2
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtasn1-6/libtasn1-6_4.19.0-3ubuntu0.24.04.2.dsc' libtasn1-6_4.19.0-3ubuntu0.24.04.2.dsc 2801 SHA512:1f6d7b3a05b8f9b804d00fe726dbcd0ae0ed60d38483cecb45c8ddc6607a7cf11e1f7ea8e1001afc56b5c74be98893f063aa2dfd203df3f4c25fe211ca229692
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtasn1-6/libtasn1-6_4.19.0.orig.tar.gz' libtasn1-6_4.19.0.orig.tar.gz 1786576 SHA512:287f5eddfb5e21762d9f14d11997e56b953b980b2b03a97ed4cd6d37909bda1ed7d2cdff9da5d270a21d863ab7e54be6b85c05f1075ac5d8f0198997cf335ef4
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtasn1-6/libtasn1-6_4.19.0.orig.tar.gz.asc' libtasn1-6_4.19.0.orig.tar.gz.asc 228 SHA512:e0417625f8df22c6421914bf2d4f19d7f27260c24c04f50e59669681f326debe06ddef9dc5a2e20fda50feb30bbbf3f41597e64961257304ec2c407aa76d107e
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtasn1-6/libtasn1-6_4.19.0-3ubuntu0.24.04.2.debian.tar.xz' libtasn1-6_4.19.0-3ubuntu0.24.04.2.debian.tar.xz 25112 SHA512:b64b55ad6138f12b1191039c1db36cba1b6add98bab5c399b338517284b4091ede2ce7a2e71f46f97c50584fb670bc2dd295caab108973aed0552353c1cb3158
```

### `dpkg` source package: `libunistring=1.1-2build1.1`

Binary Packages:

- `libunistring5:amd64=1.1-2build1.1`

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
$ apt-get source -qq --print-uris libunistring=1.1-2build1.1
'http://archive.ubuntu.com/ubuntu/pool/main/libu/libunistring/libunistring_1.1-2build1.1.dsc' libunistring_1.1-2build1.1.dsc 2292 SHA512:94e0463201534ac0db023f29ffde1c63b479ead150a59a0bd27b9e0fc425976e3eb057657bf4f9e0c572816dc5219d8df9cb5ec872bc433d4166a888f8ab69c8
'http://archive.ubuntu.com/ubuntu/pool/main/libu/libunistring/libunistring_1.1.orig.tar.xz' libunistring_1.1.orig.tar.xz 2397676 SHA512:01a4267bbd301ea5c389b17ee918ae5b7d645da8b2c6c6f0f004ff2dead9f8e50cda2c6047358890a5fceadc8820ffc5154879193b9bb8970f3fb1fea1f411d6
'http://archive.ubuntu.com/ubuntu/pool/main/libu/libunistring/libunistring_1.1.orig.tar.xz.asc' libunistring_1.1.orig.tar.xz.asc 833 SHA512:f94912a52df8d7863de271315c8b5a7e1e0ab7aabb66273fcdb81c48aa0b23360b80fdb1df9f768aede47dd5a92a280868db41147139dfabecbc82511715db4d
'http://archive.ubuntu.com/ubuntu/pool/main/libu/libunistring/libunistring_1.1-2build1.1.debian.tar.xz' libunistring_1.1-2build1.1.debian.tar.xz 14188 SHA512:c8c03af60f056eeb8d5b16ca5e6df6029506266f383d1f5ca61be8ae6a64ad50a918b5c818db1f1d88fc9086169290df1e25749c9aacb0054ea308c1f92ecdb8
```

### `dpkg` source package: `liburcu=0.14.0-3.1build1`

Binary Packages:

- `liburcu-dev:amd64=0.14.0-3.1build1`
- `liburcu8t64:amd64=0.14.0-3.1build1`

Licenses: (parsed from: `/usr/share/doc/liburcu-dev/copyright`, `/usr/share/doc/liburcu8t64/copyright`)

- `BSD-2-clause`
- `Expat`
- `FSFAP`
- `GPL-2`
- `GPL-2 with Autoconf-data exception`
- `GPL-2+`
- `GPL-2+ with Autoconf-2.0~Archive exception`
- `GPL-3`
- `GPL-3+`
- `GPL-3+ with Autoconf-2.0~Archive exception`
- `LGPL-2.1`
- `LGPL-2.1+`
- `MIT-MINIMAL`
- `MIT~Boehm`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libuv1=1.48.0-1.1build1`

Binary Packages:

- `libuv1t64:amd64=1.48.0-1.1build1`

Licenses: (parsed from: `/usr/share/doc/libuv1t64/copyright`)

- `Apache-2.0`
- `BSD-2-clause`
- `CC-BY-4.0`
- `Expat`
- `GPL3+ with autoconf exception`
- `ISC`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libxcrypt=1:4.4.36-4build1`

Binary Packages:

- `libcrypt-dev:amd64=1:4.4.36-4build1`
- `libcrypt1:amd64=1:4.4.36-4build1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libxml2=2.9.14+dfsg-1.3ubuntu3.7`

Binary Packages:

- `libxml2:amd64=2.9.14+dfsg-1.3ubuntu3.7`
- `libxml2-utils=2.9.14+dfsg-1.3ubuntu3.7`

Licenses: (parsed from: `/usr/share/doc/libxml2/copyright`, `/usr/share/doc/libxml2-utils/copyright`)

- `ISC`
- `MIT-1`

Source:

```console
$ apt-get source -qq --print-uris libxml2=2.9.14+dfsg-1.3ubuntu3.7
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxml2/libxml2_2.9.14%2bdfsg-1.3ubuntu3.7.dsc' libxml2_2.9.14+dfsg-1.3ubuntu3.7.dsc 3083 SHA512:bd10326e5294c4a92fb4918a363cb8861f7a20fc876ec1c11e7edb6482a53aee85471a0c274244eeeda96f65b57aa260071d9aa033f169cd4e7fdc943ef09e5d
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxml2/libxml2_2.9.14%2bdfsg.orig.tar.xz' libxml2_2.9.14+dfsg.orig.tar.xz 2351200 SHA512:1eacc9ac2cd8d38b8466659b3b9d84b94eb765c8f869d6cca0da131060bbc35c2b31c6148d59690547871a20cea339eac8fbe953b4fe37cf0900862f3fd9621b
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxml2/libxml2_2.9.14%2bdfsg-1.3ubuntu3.7.debian.tar.xz' libxml2_2.9.14+dfsg-1.3ubuntu3.7.debian.tar.xz 52444 SHA512:4090c7600387e0ed6dc7acfa7f691d6ee3cbcd2da2ba305848a42c6497f9ac4cbc2c87b8c2c0659b15afc7373f8aef2a8473a465157a1cc3a1d982b79c2d2ba9
```

### `dpkg` source package: `libxslt=1.1.39-0exp1ubuntu0.24.04.3`

Binary Packages:

- `libxslt1.1:amd64=1.1.39-0exp1ubuntu0.24.04.3`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxslt=1.1.39-0exp1ubuntu0.24.04.3
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxslt/libxslt_1.1.39-0exp1ubuntu0.24.04.3.dsc' libxslt_1.1.39-0exp1ubuntu0.24.04.3.dsc 2352 SHA512:7709b2e2900154e58c792fa288a99ab1b90863e7e02400e510507b78aeb7b1e0e302995146e247c371fe8311cfe42d4861e8d6c176b045dc118d65902dbf61ff
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxslt/libxslt_1.1.39.orig.tar.xz' libxslt_1.1.39.orig.tar.xz 1578216 SHA512:c0c99dc63f8b2acb6cc3ad7ad684ffa2a427ee8d1740495cbf8a7c9b9c8679f96351b4b676c73ccc191014db4cb4ab42b9a0070f6295565f39dbc665c5c16f89
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxslt/libxslt_1.1.39-0exp1ubuntu0.24.04.3.debian.tar.xz' libxslt_1.1.39-0exp1ubuntu0.24.04.3.debian.tar.xz 24380 SHA512:e9ea90695741f2a81ccf3ca36c1ffd3806ce158242a77e29f0282bf4b124d5dcc0f8b60bd870c56d168a71f61f43b667720c37741a23dd9a4280b0c22063c69f
```

### `dpkg` source package: `libyaml=0.2.5-1build1`

Binary Packages:

- `libyaml-0-2:amd64=0.2.5-1build1`
- `libyaml-dev:amd64=0.2.5-1build1`

Licenses: (parsed from: `/usr/share/doc/libyaml-0-2/copyright`, `/usr/share/doc/libyaml-dev/copyright`)

- `Expat`
- `permissive`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libzstd=1.5.5+dfsg2-2build1.1`

Binary Packages:

- `libzstd1:amd64=1.5.5+dfsg2-2build1.1`

Licenses: (parsed from: `/usr/share/doc/libzstd1/copyright`)

- `BSD-3-clause`
- `Expat`
- `GPL-2`
- `zlib`

Source:

```console
$ apt-get source -qq --print-uris libzstd=1.5.5+dfsg2-2build1.1
'http://archive.ubuntu.com/ubuntu/pool/main/libz/libzstd/libzstd_1.5.5%2bdfsg2-2build1.1.dsc' libzstd_1.5.5+dfsg2-2build1.1.dsc 2485 SHA512:58915fc819994cbf1e5db663bcdf266ebf0d9967a25e549645be22c27fe7390a5cc000af3a40494895c0102b95c41caf54cb0ed1b3331e9921bfae181a9603b9
'http://archive.ubuntu.com/ubuntu/pool/main/libz/libzstd/libzstd_1.5.5%2bdfsg2.orig.tar.xz' libzstd_1.5.5+dfsg2.orig.tar.xz 1784164 SHA512:0b24cf71636b36ae17f617f0a4a2e1253ba6a7bfcd8b6f4717cc59310e92d23bde0945f885fa80622d84961b85fa6ba74e3436ab1badc687e8a13ac428a71b8d
'http://archive.ubuntu.com/ubuntu/pool/main/libz/libzstd/libzstd_1.5.5%2bdfsg2-2build1.1.debian.tar.xz' libzstd_1.5.5+dfsg2-2build1.1.debian.tar.xz 21288 SHA512:8d57d913e68ec6722378c7d04b1513ac565b8bdda527f615aaa13f3270c423c1f1ee9575b50330c827de64dc66b25a60cbfe5b53d197346a0cff27d5fb735e40
```

### `dpkg` source package: `linux=6.8.0-107.107`

Binary Packages:

- `linux-libc-dev:amd64=6.8.0-107.107`

Licenses: (parsed from: `/usr/share/doc/linux-libc-dev/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris linux=6.8.0-107.107
'http://archive.ubuntu.com/ubuntu/pool/main/l/linux/linux_6.8.0-107.107.dsc' linux_6.8.0-107.107.dsc 9448 SHA512:a2069dc5b1994656b0fe485b39f4547e3968f23f1057abbfa8a254e57c7e1bc4bbc60901cdff6f1d3748bfbcd8d48aa927dce7861e8592a2367c1c41d2e6bff4
'http://archive.ubuntu.com/ubuntu/pool/main/l/linux/linux_6.8.0.orig.tar.gz' linux_6.8.0.orig.tar.gz 230060117 SHA512:296f93b24e1f7d116377ba8ccd0d8a977e82248ef469586e52db496190092572e90bc05704760424d215261fcbf62e7240819dffd0976b0f6407361e1eac380c
'http://archive.ubuntu.com/ubuntu/pool/main/l/linux/linux_6.8.0-107.107.diff.gz' linux_6.8.0-107.107.diff.gz 8169381 SHA512:dffef069d2e339e9dd9f5f77da173a49b48adc3c8f870fd032d108023f3fd3b9b66f85afa33245c66eab39042c996cbf198188a83b554809c3472bb5ef181bfb
```

### `dpkg` source package: `lsb-release-minimal=12.0-2`

Binary Packages:

- `lsb-release=12.0-2`

Licenses: (parsed from: `/usr/share/doc/lsb-release/copyright`)

- `ISC`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/lsb-release-minimal/12.0-2/


### `dpkg` source package: `ltt-control=2.13.11-2.1build4`

Binary Packages:

- `liblttng-ctl0t64:amd64=2.13.11-2.1build4`
- `lttng-tools=2.13.11-2.1build4`

Licenses: (parsed from: `/usr/share/doc/liblttng-ctl0t64/copyright`, `/usr/share/doc/lttng-tools/copyright`)

- `BSD-2-clause`
- `Expat`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `LGPL-2.1`
- `LGPL-2.1+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `lxml=5.2.1-1`

Binary Packages:

- `python3-lxml:amd64=5.2.1-1`

Licenses: (parsed from: `/usr/share/doc/python3-lxml/copyright`)

- `GPL`
- `GPL2`
- `later`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/lxml/5.2.1-1/


### `dpkg` source package: `lz4=1.9.4-1build1.1`

Binary Packages:

- `liblz4-1:amd64=1.9.4-1build1.1`

Licenses: (parsed from: `/usr/share/doc/liblz4-1/copyright`)

- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris lz4=1.9.4-1build1.1
'http://archive.ubuntu.com/ubuntu/pool/main/l/lz4/lz4_1.9.4-1build1.1.dsc' lz4_1.9.4-1build1.1.dsc 2061 SHA512:92ed13e86d10857d6a9d0398ce200b54b6aa66d45f9f72bda5fddec53fb00291d48e6efb932085a57361c364c551a8d0e2dfe12331abcafc92b7f61884a239cd
'http://archive.ubuntu.com/ubuntu/pool/main/l/lz4/lz4_1.9.4.orig.tar.gz' lz4_1.9.4.orig.tar.gz 354063 SHA512:043a9acb2417624019d73db140d83b80f1d7c43a6fd5be839193d68df8fd0b3f610d7ed4d628c2a9184f7cde9a0fd1ba9d075d8251298e3eb4b3a77f52736684
'http://archive.ubuntu.com/ubuntu/pool/main/l/lz4/lz4_1.9.4-1build1.1.debian.tar.xz' lz4_1.9.4-1build1.1.debian.tar.xz 8356 SHA512:deb05c99d5ba5702997608b9c5fbe72b1a383bce253e0e25c409746c44d98245c559c0744767a18d32bdb5303a575c18f5c784fe4ad0b03565a13450c86c74f1
```

### `dpkg` source package: `mawk=1.3.4.20240123-1build1`

Binary Packages:

- `mawk=1.3.4.20240123-1build1`

Licenses: (parsed from: `/usr/share/doc/mawk/copyright`)

- `CC-BY-3.0`
- `GPL-2`
- `GPL-2.0-only`
- `X11`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `media-types=10.1.0`

Binary Packages:

- `media-types=10.1.0`

Licenses: (parsed from: `/usr/share/doc/media-types/copyright`)

- `ad-hoc`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/media-types/10.1.0/


### `dpkg` source package: `more-itertools=10.2.0-1`

Binary Packages:

- `python3-more-itertools=10.2.0-1`

Licenses: (parsed from: `/usr/share/doc/python3-more-itertools/copyright`)

- `MIT-style`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/more-itertools/10.2.0-1/


### `dpkg` source package: `ncurses=6.4+20240113-1ubuntu2`

Binary Packages:

- `libncursesw6:amd64=6.4+20240113-1ubuntu2`
- `libtinfo6:amd64=6.4+20240113-1ubuntu2`
- `ncurses-base=6.4+20240113-1ubuntu2`
- `ncurses-bin=6.4+20240113-1ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libncursesw6/copyright`, `/usr/share/doc/libtinfo6/copyright`, `/usr/share/doc/ncurses-base/copyright`, `/usr/share/doc/ncurses-bin/copyright`)

- `BSD-3-clause`
- `MIT/X11`
- `X11`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `netbase=6.4`

Binary Packages:

- `netbase=6.4`

Licenses: (parsed from: `/usr/share/doc/netbase/copyright`)

- `GPL-2`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/netbase/6.4/


### `dpkg` source package: `nettle=3.9.1-2.2build1.1`

Binary Packages:

- `libhogweed6t64:amd64=3.9.1-2.2build1.1`
- `libnettle8t64:amd64=3.9.1-2.2build1.1`

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
$ apt-get source -qq --print-uris nettle=3.9.1-2.2build1.1
'http://archive.ubuntu.com/ubuntu/pool/main/n/nettle/nettle_3.9.1-2.2build1.1.dsc' nettle_3.9.1-2.2build1.1.dsc 2325 SHA512:4673af3a6485b78bb8bd7fff908aaf86fabe2220f26ab8acee89ae6b1fa0d2ca12c529c677d7b9b5709068d3c0fbf38d88d2eddacf55aabe01e10d6e8451c832
'http://archive.ubuntu.com/ubuntu/pool/main/n/nettle/nettle_3.9.1.orig.tar.gz' nettle_3.9.1.orig.tar.gz 2396741 SHA512:5939c4b43cf9ff6c6272245b85f123c81f8f4e37089fa4f39a00a570016d837f6e706a33226e4bbfc531b02a55b2756ff312461225ed88de338a73069e031ced
'http://archive.ubuntu.com/ubuntu/pool/main/n/nettle/nettle_3.9.1.orig.tar.gz.asc' nettle_3.9.1.orig.tar.gz.asc 573 SHA512:2ca8ab90c2a437c587987492be2a4c71658256020af725b48ee8f25771b7af28a9c1a8e300826dce58c4b691545d450ec44e668187daaa351a63a77eca4cedcb
'http://archive.ubuntu.com/ubuntu/pool/main/n/nettle/nettle_3.9.1-2.2build1.1.debian.tar.xz' nettle_3.9.1-2.2build1.1.debian.tar.xz 24848 SHA512:6d53ab1bd7e520c8ed10b36db6a5c584dd034ace0ef71f88445b74e566ffd35b7cc2d33267f51ce391c5833ff978d93eadd10fdb16373aee163a8434032348c8
```

### `dpkg` source package: `nghttp2=1.59.0-1ubuntu0.2`

Binary Packages:

- `libnghttp2-14:amd64=1.59.0-1ubuntu0.2`

Licenses: (parsed from: `/usr/share/doc/libnghttp2-14/copyright`)

- `BSD-2-clause`
- `Expat`
- `GPL-3`
- `GPL-3+ with autoconf exception`
- `MIT`
- `all-permissive`

Source:

```console
$ apt-get source -qq --print-uris nghttp2=1.59.0-1ubuntu0.2
'http://archive.ubuntu.com/ubuntu/pool/main/n/nghttp2/nghttp2_1.59.0-1ubuntu0.2.dsc' nghttp2_1.59.0-1ubuntu0.2.dsc 2624 SHA512:f0162428c3f2f3663af8a36ca08b732f3d70240387533816945a6164aff280ae53a9060bc322d619463dbbe28c9a8bafc93c6b0106c3d40c0dd56e561dd2f075
'http://archive.ubuntu.com/ubuntu/pool/main/n/nghttp2/nghttp2_1.59.0.orig.tar.gz' nghttp2_1.59.0.orig.tar.gz 1055492 SHA512:bcb53ff45afae003f11a9feaa21dd80a3abfcde9b3a7fd1f04fc4382d71b5d4430e2d015765a7ae8d68454fcf06e4560c4cb585133aefb237d6ea526f61a8ebd
'http://archive.ubuntu.com/ubuntu/pool/main/n/nghttp2/nghttp2_1.59.0-1ubuntu0.2.debian.tar.xz' nghttp2_1.59.0-1ubuntu0.2.debian.tar.xz 14204 SHA512:b2ca6c685f1366b42eca185a76451f33223b59f172f8842e910394244d7e4bd14b8ceca4e03ccf6658e9cb2649213924f304ed8d5ba143f680388053c7289e66
```

### `dpkg` source package: `node-jquery=3.6.1+dfsg+~3.5.14-1`

Binary Packages:

- `libjs-jquery=3.6.1+dfsg+~3.5.14-1`

Licenses: (parsed from: `/usr/share/doc/libjs-jquery/copyright`)

- `Expat`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/node-jquery/3.6.1+dfsg+~3.5.14-1/


### `dpkg` source package: `npth=1.6-3.1build1`

Binary Packages:

- `libnpth0t64:amd64=1.6-3.1build1`

Licenses: (parsed from: `/usr/share/doc/libnpth0t64/copyright`)

- `LGPL-2.1`
- `LGPL-2.1+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `numactl=2.0.18-1ubuntu0.24.04.1`

Binary Packages:

- `libnuma1:amd64=2.0.18-1ubuntu0.24.04.1`

Licenses: (parsed from: `/usr/share/doc/libnuma1/copyright`)

- `GPL`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris numactl=2.0.18-1ubuntu0.24.04.1
'http://archive.ubuntu.com/ubuntu/pool/main/n/numactl/numactl_2.0.18-1ubuntu0.24.04.1.dsc' numactl_2.0.18-1ubuntu0.24.04.1.dsc 2144 SHA512:d264cd5a7c4c9793f1cdcf9a1ddceb29495b99514809e91c75323ef187c8825dc66c76f358c63cff7a64cc7ace031b0d3b432793366bbed489a26ee13b00c15f
'http://archive.ubuntu.com/ubuntu/pool/main/n/numactl/numactl_2.0.18.orig.tar.gz' numactl_2.0.18.orig.tar.gz 218289 SHA512:fc062e7fcfd90e3d26d0e3b144b4c4328b54874aef6ad0c91d7740e5989787a182037c5d409ce9271f0a6459d4d7e70f49cc5f701d93b64a15d3b7772accb9b4
'http://archive.ubuntu.com/ubuntu/pool/main/n/numactl/numactl_2.0.18-1ubuntu0.24.04.1.debian.tar.xz' numactl_2.0.18-1ubuntu0.24.04.1.debian.tar.xz 7936 SHA512:dfa172698cb88e33a00b88735b9b643538471786c4b0e54160e8c10004b82a7b94cd0466bb8206bb632710512964298cc32f2341d8f0983b9cf6235057b4bc8d
```

### `dpkg` source package: `numpy=1:1.26.4+ds-6ubuntu1`

Binary Packages:

- `python3-numpy=1:1.26.4+ds-6ubuntu1`

Licenses: (parsed from: `/usr/share/doc/python3-numpy/copyright`)

- `Apache-2`
- `Apache-2.0`
- `BSD-3-Clause`
- `Expat`
- `ZLib`
- `Zlib`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `openldap=2.6.10+dfsg-0ubuntu0.24.04.1`

Binary Packages:

- `libldap2:amd64=2.6.10+dfsg-0ubuntu0.24.04.1`

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
$ apt-get source -qq --print-uris openldap=2.6.10+dfsg-0ubuntu0.24.04.1
'http://archive.ubuntu.com/ubuntu/pool/main/o/openldap/openldap_2.6.10%2bdfsg-0ubuntu0.24.04.1.dsc' openldap_2.6.10+dfsg-0ubuntu0.24.04.1.dsc 3653 SHA512:828b648db337736f5560dd9a9a8d1b49cd3a6c642cb0891091879a48783fdd9a38a074e5b8b244524021a2c4949e93edaba4e712870c1da8614c647ab8603319
'http://archive.ubuntu.com/ubuntu/pool/main/o/openldap/openldap_2.6.10%2bdfsg.orig.tar.xz' openldap_2.6.10+dfsg.orig.tar.xz 3754560 SHA512:9c24cab12ea4002560670d1a6053c00582aea1713e3db262bbf5aae7666c6d50ef28e7b59ca4dbe5c5b5903e56268911a935a58ef852239c259830458e804f62
'http://archive.ubuntu.com/ubuntu/pool/main/o/openldap/openldap_2.6.10%2bdfsg-0ubuntu0.24.04.1.debian.tar.xz' openldap_2.6.10+dfsg-0ubuntu0.24.04.1.debian.tar.xz 191132 SHA512:5a64a165cd7602cff38528b117e8b5f29b8953cf3edf3cc8ff87b68ce8a84b60a0dc7c3a346dab38d0fde602a2b0a8f490af221a02891dc9624a454121dc1c00
```

### `dpkg` source package: `openssl=3.0.13-0ubuntu3.7`

Binary Packages:

- `libssl-dev:amd64=3.0.13-0ubuntu3.7`
- `libssl3t64:amd64=3.0.13-0ubuntu3.7`
- `openssl=3.0.13-0ubuntu3.7`

Licenses: (parsed from: `/usr/share/doc/libssl3t64/copyright`)

- `Apache-2.0`
- `Artistic`
- `GPL-1`
- `GPL-1+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `p11-kit=0.25.3-4ubuntu2.1`

Binary Packages:

- `libp11-kit0:amd64=0.25.3-4ubuntu2.1`

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
$ apt-get source -qq --print-uris p11-kit=0.25.3-4ubuntu2.1
'http://archive.ubuntu.com/ubuntu/pool/main/p/p11-kit/p11-kit_0.25.3-4ubuntu2.1.dsc' p11-kit_0.25.3-4ubuntu2.1.dsc 2405 SHA512:8333b22df20f4febfcc6bdf987695d9bee2f0c578a60d15d76fc4099c22fd294dff01772bed717fc220773524a8b674f4ef1ad6b3343856c3c5f8e4adbafc5dc
'http://archive.ubuntu.com/ubuntu/pool/main/p/p11-kit/p11-kit_0.25.3.orig.tar.xz' p11-kit_0.25.3.orig.tar.xz 991528 SHA512:ad2d393bf122526cbba18dc9d5a13f2c1cad7d70125ec90ffd02059dfa5ef30ac59dfc0bb9bc6380c8f317e207c9e87e895f1945634f56ddf910c2958868fb4c
'http://archive.ubuntu.com/ubuntu/pool/main/p/p11-kit/p11-kit_0.25.3-4ubuntu2.1.debian.tar.xz' p11-kit_0.25.3-4ubuntu2.1.debian.tar.xz 26028 SHA512:531ecb33634ae9056eac7bac90579b12113a3800fca4d2e4e2e42266e34ed9b96bdbe322b9c6e54ee1fad20ae9760d92e5fc0bae558477add44f3a587913806b
```

### `dpkg` source package: `pam=1.5.3-5ubuntu5.5`

Binary Packages:

- `libpam-modules:amd64=1.5.3-5ubuntu5.5`
- `libpam-modules-bin=1.5.3-5ubuntu5.5`
- `libpam-runtime=1.5.3-5ubuntu5.5`
- `libpam0g:amd64=1.5.3-5ubuntu5.5`

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
$ apt-get source -qq --print-uris pam=1.5.3-5ubuntu5.5
'http://archive.ubuntu.com/ubuntu/pool/main/p/pam/pam_1.5.3-5ubuntu5.5.dsc' pam_1.5.3-5ubuntu5.5.dsc 2727 SHA512:59b875e301869358617068f0e2ebcc884ae8c2fad24c487b15d347ee4b826df9a008aa74fa14aa99fc1300ab9fd07dbef6f025e50a005937a093df692f9befc0
'http://archive.ubuntu.com/ubuntu/pool/main/p/pam/pam_1.5.3.orig.tar.xz' pam_1.5.3.orig.tar.xz 1020076 SHA512:af88e8c1b6a9b737ffaffff7dd9ed8eec996d1fbb5804fb76f590bed66d8a1c2c6024a534d7a7b6d18496b300f3d6571a08874cf406cd2e8cea1d5eff49c136a
'http://archive.ubuntu.com/ubuntu/pool/main/p/pam/pam_1.5.3-5ubuntu5.5.debian.tar.xz' pam_1.5.3-5ubuntu5.5.debian.tar.xz 204688 SHA512:9c4e286ce3ea8bce267b7571f518e434a704d8c9a46c5de8cee1d0bf4b5303474a5549e5b188ba8b306b282a1797ab3418d299195557da8e275c5f005776f10d
```

### `dpkg` source package: `pcre2=10.42-4ubuntu2.1`

Binary Packages:

- `libpcre2-8-0:amd64=10.42-4ubuntu2.1`

Licenses: (parsed from: `/usr/share/doc/libpcre2-8-0/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `BSD-3-clause-Cambridge with BINARY LIBRARY-LIKE PACKAGES exception`
- `X11`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris pcre2=10.42-4ubuntu2.1
'http://archive.ubuntu.com/ubuntu/pool/main/p/pcre2/pcre2_10.42-4ubuntu2.1.dsc' pcre2_10.42-4ubuntu2.1.dsc 2277 SHA512:4a66de3dd3c3f3ef6fa078cbdfacd59282da53206c0753f9ddd01fa67b501425ea5e9350e0cece9d31b4194fca5b107146fe8bba97a06c02c431a91891226a6d
'http://archive.ubuntu.com/ubuntu/pool/main/p/pcre2/pcre2_10.42.orig.tar.gz' pcre2_10.42.orig.tar.gz 2397194 SHA512:a3db6c5c620775838819be616652e73ce00f5ef5c1f49f559ff3efb51a119d02f01254c5901c1f7d0c47c0ddfcf4313e38d6ca32c35381b8f87f36896d10e6f7
'http://archive.ubuntu.com/ubuntu/pool/main/p/pcre2/pcre2_10.42-4ubuntu2.1.diff.gz' pcre2_10.42-4ubuntu2.1.diff.gz 8431 SHA512:a739c00ba25573d4e57490d487efcd1f4afbafb820ccb6063fe9d25f22d9a1f9bf7cc91cd89c5ffbb0b533f06133e4beaa16e5aee7f64e8939872ebb933c2f00
```

### `dpkg` source package: `perl=5.38.2-3.2ubuntu0.2`

Binary Packages:

- `perl-base=5.38.2-3.2ubuntu0.2`

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
$ apt-get source -qq --print-uris perl=5.38.2-3.2ubuntu0.2
'http://archive.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.38.2-3.2ubuntu0.2.dsc' perl_5.38.2-3.2ubuntu0.2.dsc 3036 SHA512:bdd956f4f04ef15d13659bac27cce96c4d98caaacc586525302c9e14c865e7c9ae81b7369caf636fd73074edcbc56a6e204e3c2ab0c8f2db52f8fece9f0d4b6c
'http://archive.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.38.2.orig-regen-configure.tar.xz' perl_5.38.2.orig-regen-configure.tar.xz 418808 SHA512:c4ea40ce9eda247c2ced678a75bdbd8bc292baee5ec3490cb00b1947277e1e0e9e5160d108676380efff13d4f1304f0c8d4eaa2c7e66e543ecd57e513075cb8c
'http://archive.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.38.2.orig.tar.xz' perl_5.38.2.orig.tar.xz 13679524 SHA512:0ca51e447c7a18639627c281a1c7ae6662c773745ea3c86bede46336d5514ecc97ded2c61166e1ac15635581489dc596368907aa3a775b34db225b76d7402d10
'http://archive.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.38.2-3.2ubuntu0.2.debian.tar.xz' perl_5.38.2-3.2ubuntu0.2.debian.tar.xz 171736 SHA512:9511993218de5c72dabb87e2ba13a00b034fbb96637b3791515cbac26fa9820067d95d48f165766cce1086304936c1de6150140023915437a91050f27aced32e
```

### `dpkg` source package: `pinentry=1.2.1-3ubuntu5`

Binary Packages:

- `pinentry-curses=1.2.1-3ubuntu5`

Licenses: (parsed from: `/usr/share/doc/pinentry-curses/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-3`
- `LGPL-3+`
- `X11`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `pkgconf=1.8.1-2build1`

Binary Packages:

- `libpkgconf3:amd64=1.8.1-2build1`
- `pkg-config:amd64=1.8.1-2build1`
- `pkgconf:amd64=1.8.1-2build1`
- `pkgconf-bin=1.8.1-2build1`

Licenses: (parsed from: `/usr/share/doc/libpkgconf3/copyright`, `/usr/share/doc/pkg-config/copyright`, `/usr/share/doc/pkgconf/copyright`, `/usr/share/doc/pkgconf-bin/copyright`)

- `BSD-2`
- `BSD-4`
- `GPL-2`
- `GPL-2+`
- `ISC`
- `X11`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `popt=1.19+dfsg-1build1`

Binary Packages:

- `libpopt0:amd64=1.19+dfsg-1build1`

Licenses: (parsed from: `/usr/share/doc/libpopt0/copyright`)

- `GPL-2`
- `GPL-2+`
- `expat`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `procps=2:4.0.4-4ubuntu3.2`

Binary Packages:

- `libproc2-0:amd64=2:4.0.4-4ubuntu3.2`
- `procps=2:4.0.4-4ubuntu3.2`

Licenses: (parsed from: `/usr/share/doc/libproc2-0/copyright`, `/usr/share/doc/procps/copyright`)

- `GPL-2`
- `GPL-2.0+`
- `LGPL-2`
- `LGPL-2.0+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris procps=2:4.0.4-4ubuntu3.2
'http://archive.ubuntu.com/ubuntu/pool/main/p/procps/procps_4.0.4-4ubuntu3.2.dsc' procps_4.0.4-4ubuntu3.2.dsc 2251 SHA512:3c342f5b82345d0320eefb03be09254259f33a08058ebdaa4bb8130bc8dc295138e2b19729c0f14752ecdad774fd24aae942b1ffa6a591fc0365487031c595d9
'http://archive.ubuntu.com/ubuntu/pool/main/p/procps/procps_4.0.4.orig.tar.xz' procps_4.0.4.orig.tar.xz 1401540 SHA512:94375544e2422fefc23d7634063c49ef1be62394c46039444f85e6d2e87e45cfadc33accba5ca43c96897b4295bfb0f88d55a30204598ddb26ef66f0420cefb4
'http://archive.ubuntu.com/ubuntu/pool/main/p/procps/procps_4.0.4-4ubuntu3.2.debian.tar.xz' procps_4.0.4-4ubuntu3.2.debian.tar.xz 38784 SHA512:51e3e1f8f9e206eecf009e8cb9d32147b12f5961288a07d458e270ae77a9048baef52ec11d921dfd9d8362d3db48d987bac74afcab89f266a0138718ef20844a
```

### `dpkg` source package: `pycodestyle=2.11.1-1`

Binary Packages:

- `python3-pycodestyle=2.11.1-1`

Licenses: (parsed from: `/usr/share/doc/python3-pycodestyle/copyright`)

- `Expat`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/pycodestyle/2.11.1-1/


### `dpkg` source package: `pydocstyle=6.3.0-1.1`

Binary Packages:

- `pydocstyle=6.3.0-1.1`
- `python3-pydocstyle=6.3.0-1.1`

Licenses: (parsed from: `/usr/share/doc/pydocstyle/copyright`, `/usr/share/doc/python3-pydocstyle/copyright`)

- `Expat`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/pydocstyle/6.3.0-1.1/


### `dpkg` source package: `pyflakes=3.2.0-1`

Binary Packages:

- `python3-pyflakes=3.2.0-1`

Licenses: (parsed from: `/usr/share/doc/python3-pyflakes/copyright`)

- `MIT`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/pyflakes/3.2.0-1/


### `dpkg` source package: `pygments=2.17.2+dfsg-1`

Binary Packages:

- `python3-pygments=2.17.2+dfsg-1`

Licenses: (parsed from: `/usr/share/doc/python3-pygments/copyright`)

- `Apache-2.0`
- `BSD-2-clause`
- `ISO-1986`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/pygments/2.17.2+dfsg-1/


### `dpkg` source package: `pyparsing=3.1.1-1`

Binary Packages:

- `python3-pyparsing=3.1.1-1`

Licenses: (parsed from: `/usr/share/doc/python3-pyparsing/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `Expat`
- `MIT/X11`
- `ellis-and-grant`
- `salvolainen`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/pyparsing/3.1.1-1/


### `dpkg` source package: `pytest=7.4.4-1`

Binary Packages:

- `python3-pytest=7.4.4-1`

Licenses: (parsed from: `/usr/share/doc/python3-pytest/copyright`)

- `Expat`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/pytest/7.4.4-1/


### `dpkg` source package: `python-argcomplete=3.1.4-1ubuntu0.1`

Binary Packages:

- `python3-argcomplete=3.1.4-1ubuntu0.1`

Licenses: (parsed from: `/usr/share/doc/python3-argcomplete/copyright`)

- `Apache-2.0`

Source:

```console
$ apt-get source -qq --print-uris python-argcomplete=3.1.4-1ubuntu0.1
'http://archive.ubuntu.com/ubuntu/pool/universe/p/python-argcomplete/python-argcomplete_3.1.4-1ubuntu0.1.dsc' python-argcomplete_3.1.4-1ubuntu0.1.dsc 2509 SHA512:5ae742ceebbfc3f34cd8fbeed2c0744afc0c6dccdeb93acb9e3b83229f83f6f0f3eaead2357773b2e913d801222caaaaf09c95d6abae12f8f6af78c869c7dbc0
'http://archive.ubuntu.com/ubuntu/pool/universe/p/python-argcomplete/python-argcomplete_3.1.4.orig.tar.gz' python-argcomplete_3.1.4.orig.tar.gz 79529 SHA512:d5108273fb570ec42667acefd1cf397e2fbedb3d4fbc31bb2b3206cdbb3275fde88b4d40e9dc65045b6a94334e6b5b9136054c6291edc21dcd0542f1369fe4b1
'http://archive.ubuntu.com/ubuntu/pool/universe/p/python-argcomplete/python-argcomplete_3.1.4-1ubuntu0.1.debian.tar.xz' python-argcomplete_3.1.4-1ubuntu0.1.debian.tar.xz 8116 SHA512:7dc0b8cbb1d6beec393ef3d29ff16bbd856779fb98448513e501b5504a2a024065a1786ba0d54b481542746a38bc440fa42f2e82e70d1c215ffbf98188e4e0c3
```

### `dpkg` source package: `python-cffi=1.16.0-2build1`

Binary Packages:

- `python3-cffi-backend:amd64=1.16.0-2build1`

Licenses: (parsed from: `/usr/share/doc/python3-cffi-backend/copyright`)

- `Expat`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python-cryptography=41.0.7-4ubuntu0.4`

Binary Packages:

- `python3-cryptography=41.0.7-4ubuntu0.4`

Licenses: (parsed from: `/usr/share/doc/python3-cryptography/copyright`)

- `Apache`
- `Apache-2.0`
- `Expat`

Source:

```console
$ apt-get source -qq --print-uris python-cryptography=41.0.7-4ubuntu0.4
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-cryptography/python-cryptography_41.0.7-4ubuntu0.4.dsc' python-cryptography_41.0.7-4ubuntu0.4.dsc 3363 SHA512:76eb71ffa12cca2beb0bf55a493544fb2ebfa2cafb0a37f51de480caf1d8e3191e6517071dd303aa36d7cb38d7cf9d43c63641bef1cb657c5883aa5f75c5d7a7
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-cryptography/python-cryptography_41.0.7.orig.tar.gz' python-cryptography_41.0.7.orig.tar.gz 630892 SHA512:c678da6dfc02d84ca9a26bc42844da8ba356f5dc839fefa0b63636c99107b18415b5970d721b72075fc0f8aefc3785dbf143327ceb7f4ebd075df41291b63219
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-cryptography/python-cryptography_41.0.7-4ubuntu0.4.debian.tar.xz' python-cryptography_41.0.7-4ubuntu0.4.debian.tar.xz 13648 SHA512:49815bdd8c8c9345e777bc2dcdb6b3c81773cad6aafb3536424ccc696ee633f46081ca88881d34fec68b76e29d1925d4a4f29a66331b041e38ee74cabfb0d0fb
```

### `dpkg` source package: `python-dateutil=2.8.2-3ubuntu1`

Binary Packages:

- `python3-dateutil=2.8.2-3ubuntu1`

Licenses: (parsed from: `/usr/share/doc/python3-dateutil/copyright`)

- `BSD-3-clause`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python-distro=1.9.0-1`

Binary Packages:

- `python3-distro=1.9.0-1`

Licenses: (parsed from: `/usr/share/doc/python3-distro/copyright`)

- `Apache-2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/python-distro/1.9.0-1/


### `dpkg` source package: `python-docutils=0.20.1+dfsg-3`

Binary Packages:

- `docutils-common=0.20.1+dfsg-3`
- `python3-docutils=0.20.1+dfsg-3`

Licenses: (parsed from: `/usr/share/doc/docutils-common/copyright`, `/usr/share/doc/python3-docutils/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `Expat`
- `GPL-3`
- `GPL-3+`
- `Python-2.1.1`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/python-docutils/0.20.1+dfsg-3/


### `dpkg` source package: `python-flake8=7.0.0-1`

Binary Packages:

- `python3-flake8=7.0.0-1`

Licenses: (parsed from: `/usr/share/doc/python3-flake8/copyright`)

- `Expat`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/python-flake8/7.0.0-1/


### `dpkg` source package: `python-importlib-metadata=4.12.0-1`

Binary Packages:

- `python3-importlib-metadata=4.12.0-1`

Licenses: (parsed from: `/usr/share/doc/python3-importlib-metadata/copyright`)

- `Apache-2`
- `Apache-2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/python-importlib-metadata/4.12.0-1/


### `dpkg` source package: `python-iniconfig=1.1.1-2`

Binary Packages:

- `python3-iniconfig=1.1.1-2`

Licenses: (parsed from: `/usr/share/doc/python3-iniconfig/copyright`)

- `Expat`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/python-iniconfig/1.1.1-2/


### `dpkg` source package: `python-lark=1.1.9-1`

Binary Packages:

- `python3-lark=1.1.9-1`

Licenses: (parsed from: `/usr/share/doc/python3-lark/copyright`)

- `GPL-2`
- `GPL-2+-with-bootloader-exception`
- `MIT`
- `MPL-2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/python-lark/1.1.9-1/


### `dpkg` source package: `python-mccabe=0.7.0-1`

Binary Packages:

- `python3-mccabe=0.7.0-1`

Licenses: (parsed from: `/usr/share/doc/python3-mccabe/copyright`)

- `Expat`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/python-mccabe/0.7.0-1/


### `dpkg` source package: `python-packaging=24.0-1`

Binary Packages:

- `python3-packaging=24.0-1`

Licenses: (parsed from: `/usr/share/doc/python3-packaging/copyright`)

- `Apache-2.0`
- `BSD-3-clause`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/python-packaging/24.0-1/


### `dpkg` source package: `python-pluggy=1.4.0-1`

Binary Packages:

- `python3-pluggy=1.4.0-1`

Licenses: (parsed from: `/usr/share/doc/python3-pluggy/copyright`)

- `Expat`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/python-pluggy/1.4.0-1/


### `dpkg` source package: `python-psutil=5.9.8-2build2`

Binary Packages:

- `python3-psutil=5.9.8-2build2`

Licenses: (parsed from: `/usr/share/doc/python3-psutil/copyright`)

- `BSD-3-clause`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python-roman=3.3-3`

Binary Packages:

- `python3-roman=3.3-3`

Licenses: (parsed from: `/usr/share/doc/python3-roman/copyright`)

- `Python-2.1.1`
- `ZPL-2.1`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/python-roman/3.3-3/


### `dpkg` source package: `python-zipp=1.0.0-6ubuntu0.1`

Binary Packages:

- `python3-zipp=1.0.0-6ubuntu0.1`

Licenses: (parsed from: `/usr/share/doc/python3-zipp/copyright`)

- `Expat`

Source:

```console
$ apt-get source -qq --print-uris python-zipp=1.0.0-6ubuntu0.1
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-zipp/python-zipp_1.0.0-6ubuntu0.1.dsc' python-zipp_1.0.0-6ubuntu0.1.dsc 1616 SHA512:114339a929ac0ea228882adeeb5d4e13856151fcc88c77ee1e531abff30e9c47cf1dc22ba84a3a04391611fdf733cea02c6b28315d028fc48c489fdaf00067e6
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-zipp/python-zipp_1.0.0.orig.tar.gz' python-zipp_1.0.0.orig.tar.gz 10821 SHA512:dbfadfedd30ca4cb31ac4163f367134d96e57405ef00d5f4c19c0af7a141f78487dec29a0ba94975584fcb462d22c8b536bf29c67b7e298368072e897b0e9d82
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-zipp/python-zipp_1.0.0-6ubuntu0.1.debian.tar.xz' python-zipp_1.0.0-6ubuntu0.1.debian.tar.xz 4188 SHA512:5d6b7d14ded6a5c2ae9769a023a01c37c85eab5013bf9c747b086d39a0fe43294c48a2ccc92f81df14e399872d36a4cfb19b03dcc51318e32da8a7cc3ecf66e7
```

### `dpkg` source package: `python3-catkin-pkg-modules=1.1.0-2`

Binary Packages:

- `python3-catkin-pkg-modules=1.1.0-2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-defaults=3.12.3-0ubuntu2.1`

Binary Packages:

- `libpython3-dev:amd64=3.12.3-0ubuntu2.1`
- `libpython3-stdlib:amd64=3.12.3-0ubuntu2.1`
- `python3=3.12.3-0ubuntu2.1`
- `python3-dev=3.12.3-0ubuntu2.1`
- `python3-minimal=3.12.3-0ubuntu2.1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris python3-defaults=3.12.3-0ubuntu2.1
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3-defaults/python3-defaults_3.12.3-0ubuntu2.1.dsc' python3-defaults_3.12.3-0ubuntu2.1.dsc 3116 SHA512:34bd93d70a55ea6e57e2c8adb7fab3a23507161c2ca61b2c089208cf3706455ef7e072cc04b68af9c1ecb04ed9636e65524501d9e2eb837319f220f275582c4b
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3-defaults/python3-defaults_3.12.3-0ubuntu2.1.tar.gz' python3-defaults_3.12.3-0ubuntu2.1.tar.gz 147765 SHA512:9a729a8df22e37d473d39b8c9c95b8c5a7ad8dfd244b3c87576d389f48543edeeaa0bd8b0557de3224d0dbd0f06e02b573cb18adf685a54c02bb485a21ec36e5
```

### `dpkg` source package: `python3-rosdistro-modules=1.0.1-1`

Binary Packages:

- `python3-rosdistro-modules=1.0.1-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-rospkg-modules=1.6.1-1`

Binary Packages:

- `python3-rospkg-modules=1.6.1-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3.12=3.12.3-1ubuntu0.12`

Binary Packages:

- `libpython3.12-dev:amd64=3.12.3-1ubuntu0.12`
- `libpython3.12-minimal:amd64=3.12.3-1ubuntu0.12`
- `libpython3.12-stdlib:amd64=3.12.3-1ubuntu0.12`
- `libpython3.12t64:amd64=3.12.3-1ubuntu0.12`
- `python3.12=3.12.3-1ubuntu0.12`
- `python3.12-dev=3.12.3-1ubuntu0.12`
- `python3.12-minimal=3.12.3-1ubuntu0.12`

Licenses: (parsed from: `/usr/share/doc/libpython3.12-dev/copyright`, `/usr/share/doc/libpython3.12-minimal/copyright`, `/usr/share/doc/libpython3.12-stdlib/copyright`, `/usr/share/doc/libpython3.12t64/copyright`, `/usr/share/doc/python3.12/copyright`, `/usr/share/doc/python3.12-dev/copyright`, `/usr/share/doc/python3.12-minimal/copyright`)

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
$ apt-get source -qq --print-uris python3.12=3.12.3-1ubuntu0.12
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3.12/python3.12_3.12.3-1ubuntu0.12.dsc' python3.12_3.12.3-1ubuntu0.12.dsc 3311 SHA512:8a8634302a6f30b362f63b5c4b5ef128755b290706588b85770c0c9a397210ddbbb1645e045856d1392e7fb69c8824d7e1e7355a5dd83fb6c0e83fd939aea557
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3.12/python3.12_3.12.3.orig.tar.xz' python3.12_3.12.3.orig.tar.xz 20625068 SHA512:4a2213b108e7f1f1525baa8348e68b2a2336d925e60d0a59f0225fc470768a2c8031edafc0b8243f94dbae18afda335ee5adf2785328c2218fd64cbb439f13a4
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3.12/python3.12_3.12.3-1ubuntu0.12.debian.tar.xz' python3.12_3.12.3-1ubuntu0.12.debian.tar.xz 271148 SHA512:bc1400f4a5bc52d349e5c993ab217a329970f75e0fa068a9e7d71aac0c289bd30091184ffeb4b9d1b5a27e205c3932bf1c36acec4c26649d3b84d52a5e9ef553
```

### `dpkg` source package: `pyyaml=6.0.1-2build2`

Binary Packages:

- `python3-yaml=6.0.1-2build2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `readline=8.2-4build1`

Binary Packages:

- `libreadline8t64:amd64=8.2-4build1`
- `readline-common=8.2-4build1`

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


### `dpkg` source package: `rhash=1.4.3-3build1`

Binary Packages:

- `librhash0:amd64=1.4.3-3build1`

Licenses: (parsed from: `/usr/share/doc/librhash0/copyright`)

- `0BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-apt-source=1.1.0~noble`

Binary Packages:

- `ros2-apt-source=1.1.0~noble`

Licenses: (parsed from: `/usr/share/doc/ros2-apt-source/copyright`)

- `Apache-2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-action-msgs=2.0.3-1noble.20260126.172111`

Binary Packages:

- `ros-jazzy-action-msgs=2.0.3-1noble.20260126.172111`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-action-msgs/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-actionlib-msgs=5.3.6-1noble.20260126.173038`

Binary Packages:

- `ros-jazzy-actionlib-msgs=5.3.6-1noble.20260126.173038`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-actionlib-msgs/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-auto=2.5.5-1noble.20260121.182432`

Binary Packages:

- `ros-jazzy-ament-cmake-auto=2.5.5-1noble.20260121.182432`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-auto/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-copyright=0.17.4-1noble.20260121.181252`

Binary Packages:

- `ros-jazzy-ament-cmake-copyright=0.17.4-1noble.20260121.181252`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-copyright/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-core=2.5.5-1noble.20260121.175042`

Binary Packages:

- `ros-jazzy-ament-cmake-core=2.5.5-1noble.20260121.175042`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-core/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-cppcheck=0.17.4-1noble.20260121.181240`

Binary Packages:

- `ros-jazzy-ament-cmake-cppcheck=0.17.4-1noble.20260121.181240`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-cppcheck/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-cpplint=0.17.4-1noble.20260121.181235`

Binary Packages:

- `ros-jazzy-ament-cmake-cpplint=0.17.4-1noble.20260121.181235`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-cpplint/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-export-definitions=2.5.5-1noble.20260121.180318`

Binary Packages:

- `ros-jazzy-ament-cmake-export-definitions=2.5.5-1noble.20260121.180318`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-export-definitions/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-export-dependencies=2.5.5-1noble.20260121.180807`

Binary Packages:

- `ros-jazzy-ament-cmake-export-dependencies=2.5.5-1noble.20260121.180807`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-export-dependencies/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-export-include-directories=2.5.5-1noble.20260121.180330`

Binary Packages:

- `ros-jazzy-ament-cmake-export-include-directories=2.5.5-1noble.20260121.180330`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-export-include-directories/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-export-interfaces=2.5.5-1noble.20260121.180318`

Binary Packages:

- `ros-jazzy-ament-cmake-export-interfaces=2.5.5-1noble.20260121.180318`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-export-interfaces/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-export-libraries=2.5.5-1noble.20260121.180240`

Binary Packages:

- `ros-jazzy-ament-cmake-export-libraries=2.5.5-1noble.20260121.180240`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-export-libraries/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-export-link-flags=2.5.5-1noble.20260121.180211`

Binary Packages:

- `ros-jazzy-ament-cmake-export-link-flags=2.5.5-1noble.20260121.180211`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-export-link-flags/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-export-targets=2.5.5-1noble.20260121.180310`

Binary Packages:

- `ros-jazzy-ament-cmake-export-targets=2.5.5-1noble.20260121.180310`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-export-targets/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-flake8=0.17.4-1noble.20260121.181222`

Binary Packages:

- `ros-jazzy-ament-cmake-flake8=0.17.4-1noble.20260121.181222`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-flake8/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-gen-version-h=2.5.5-1noble.20260121.180336`

Binary Packages:

- `ros-jazzy-ament-cmake-gen-version-h=2.5.5-1noble.20260121.180336`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-gen-version-h/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-gmock=2.5.5-1noble.20260121.181129`

Binary Packages:

- `ros-jazzy-ament-cmake-gmock=2.5.5-1noble.20260121.181129`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-gmock/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-gtest=2.5.5-1noble.20260121.181049`

Binary Packages:

- `ros-jazzy-ament-cmake-gtest=2.5.5-1noble.20260121.181049`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-gtest/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-include-directories=2.5.5-1noble.20260121.180338`

Binary Packages:

- `ros-jazzy-ament-cmake-include-directories=2.5.5-1noble.20260121.180338`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-include-directories/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-libraries=2.5.5-1noble.20260121.180341`

Binary Packages:

- `ros-jazzy-ament-cmake-libraries=2.5.5-1noble.20260121.180341`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-libraries/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-lint-cmake=0.17.4-1noble.20260121.181237`

Binary Packages:

- `ros-jazzy-ament-cmake-lint-cmake=0.17.4-1noble.20260121.181237`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-lint-cmake/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-pep257=0.17.4-1noble.20260121.181149`

Binary Packages:

- `ros-jazzy-ament-cmake-pep257=0.17.4-1noble.20260121.181149`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-pep257/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-pytest=2.5.5-1noble.20260121.181159`

Binary Packages:

- `ros-jazzy-ament-cmake-pytest=2.5.5-1noble.20260121.181159`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-pytest/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-python=2.5.5-1noble.20260121.180343`

Binary Packages:

- `ros-jazzy-ament-cmake-python=2.5.5-1noble.20260121.180343`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-python/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-ros=0.12.0-3noble.20260121.182437`

Binary Packages:

- `ros-jazzy-ament-cmake-ros=0.12.0-3noble.20260121.182437`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-ros/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-target-dependencies=2.5.5-1noble.20260121.180808`

Binary Packages:

- `ros-jazzy-ament-cmake-target-dependencies=2.5.5-1noble.20260121.180808`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-target-dependencies/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-test=2.5.5-1noble.20260121.180905`

Binary Packages:

- `ros-jazzy-ament-cmake-test=2.5.5-1noble.20260121.180905`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-test/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-uncrustify=0.17.4-1noble.20260121.182252`

Binary Packages:

- `ros-jazzy-ament-cmake-uncrustify=0.17.4-1noble.20260121.182252`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-uncrustify/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-version=2.5.5-1noble.20260121.180401`

Binary Packages:

- `ros-jazzy-ament-cmake-version=2.5.5-1noble.20260121.180401`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-version/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-xmllint=0.17.4-1noble.20260121.181202`

Binary Packages:

- `ros-jazzy-ament-cmake-xmllint=0.17.4-1noble.20260121.181202`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-xmllint/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake=2.5.5-1noble.20260121.181635`

Binary Packages:

- `ros-jazzy-ament-cmake=2.5.5-1noble.20260121.181635`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-copyright=0.17.4-1noble.20260121.175820`

Binary Packages:

- `ros-jazzy-ament-copyright=0.17.4-1noble.20260121.175820`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-copyright/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cppcheck=0.17.4-1noble.20260121.180207`

Binary Packages:

- `ros-jazzy-ament-cppcheck=0.17.4-1noble.20260121.180207`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cppcheck/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cpplint=0.17.4-1noble.20260121.180155`

Binary Packages:

- `ros-jazzy-ament-cpplint=0.17.4-1noble.20260121.180155`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cpplint/copyright`)

- `Apache License 2.0`
- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-flake8=0.17.4-1noble.20260121.175806`

Binary Packages:

- `ros-jazzy-ament-flake8=0.17.4-1noble.20260121.175806`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-flake8/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-index-cpp=1.8.2-1noble.20260121.182447`

Binary Packages:

- `ros-jazzy-ament-index-cpp=1.8.2-1noble.20260121.182447`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-index-cpp/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-index-python=1.8.2-1noble.20260121.175733`

Binary Packages:

- `ros-jazzy-ament-index-python=1.8.2-1noble.20260121.175733`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-index-python/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-lint-auto=0.17.4-1noble.20260121.181208`

Binary Packages:

- `ros-jazzy-ament-lint-auto=0.17.4-1noble.20260121.181208`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-lint-auto/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-lint-cmake=0.17.4-1noble.20260121.180141`

Binary Packages:

- `ros-jazzy-ament-lint-cmake=0.17.4-1noble.20260121.180141`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-lint-cmake/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-lint-common=0.17.4-1noble.20260121.182324`

Binary Packages:

- `ros-jazzy-ament-lint-common=0.17.4-1noble.20260121.182324`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-lint-common/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-lint=0.17.4-1noble.20260121.175735`

Binary Packages:

- `ros-jazzy-ament-lint=0.17.4-1noble.20260121.175735`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-lint/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-package=0.16.5-1noble.20260121.174946`

Binary Packages:

- `ros-jazzy-ament-package=0.16.5-1noble.20260121.174946`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-package/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-pep257=0.17.4-1noble.20260121.175813`

Binary Packages:

- `ros-jazzy-ament-pep257=0.17.4-1noble.20260121.175813`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-pep257/copyright`)

- `Apache License 2.0`
- `MIT`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-uncrustify=0.17.4-1noble.20260121.182220`

Binary Packages:

- `ros-jazzy-ament-uncrustify=0.17.4-1noble.20260121.182220`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-uncrustify/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-xmllint=0.17.4-1noble.20260121.175852`

Binary Packages:

- `ros-jazzy-ament-xmllint=0.17.4-1noble.20260121.175852`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-xmllint/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-builtin-interfaces=2.0.3-1noble.20260126.171712`

Binary Packages:

- `ros-jazzy-builtin-interfaces=2.0.3-1noble.20260126.171712`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-builtin-interfaces/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-class-loader=2.7.0-3noble.20260126.170731`

Binary Packages:

- `ros-jazzy-class-loader=2.7.0-3noble.20260126.170731`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-class-loader/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-common-interfaces=5.3.6-1noble.20260126.175440`

Binary Packages:

- `ros-jazzy-common-interfaces=5.3.6-1noble.20260126.175440`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-common-interfaces/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-composition-interfaces=2.0.3-1noble.20260126.173540`

Binary Packages:

- `ros-jazzy-composition-interfaces=2.0.3-1noble.20260126.173540`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-composition-interfaces/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-console-bridge-vendor=1.7.1-3noble.20260121.184936`

Binary Packages:

- `ros-jazzy-console-bridge-vendor=1.7.1-3noble.20260121.184936`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-console-bridge-vendor/copyright`)

- `Apache License 2.0`
- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-diagnostic-msgs=5.3.6-1noble.20260126.174048`

Binary Packages:

- `ros-jazzy-diagnostic-msgs=5.3.6-1noble.20260126.174048`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-diagnostic-msgs/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-domain-coordinator=0.12.0-3noble.20260121.175748`

Binary Packages:

- `ros-jazzy-domain-coordinator=0.12.0-3noble.20260121.175748`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-domain-coordinator/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-fastcdr=2.2.5-1noble.20260121.175748`

Binary Packages:

- `ros-jazzy-fastcdr=2.2.5-1noble.20260121.175748`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-fastcdr/copyright`)

- `Apache 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-fastrtps-cmake-module=3.6.3-1noble.20260121.183908`

Binary Packages:

- `ros-jazzy-fastrtps-cmake-module=3.6.3-1noble.20260121.183908`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-fastrtps-cmake-module/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-fastrtps=2.14.5-2noble.20260121.180353`

Binary Packages:

- `ros-jazzy-fastrtps=2.14.5-2noble.20260121.180353`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-fastrtps/copyright`)

- `Apache 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-foonathan-memory-vendor=1.3.1-3noble.20260121.180217`

Binary Packages:

- `ros-jazzy-foonathan-memory-vendor=1.3.1-3noble.20260121.180217`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-foonathan-memory-vendor/copyright`)

- `Apache License 2.0`
- `zlib License`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-geometry-msgs=5.3.6-1noble.20260126.173651`

Binary Packages:

- `ros-jazzy-geometry-msgs=5.3.6-1noble.20260126.173651`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-geometry-msgs/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-gmock-vendor=1.14.9000-2noble.20260121.175918`

Binary Packages:

- `ros-jazzy-gmock-vendor=1.14.9000-2noble.20260121.175918`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-gmock-vendor/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-gtest-vendor=1.14.9000-2noble.20260121.175751`

Binary Packages:

- `ros-jazzy-gtest-vendor=1.14.9000-2noble.20260121.175751`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-gtest-vendor/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-launch-ros=0.26.11-1noble.20260126.175625`

Binary Packages:

- `ros-jazzy-launch-ros=0.26.11-1noble.20260126.175625`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-launch-ros/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-launch-testing-ament-cmake=3.4.10-1noble.20260121.185614`

Binary Packages:

- `ros-jazzy-launch-testing-ament-cmake=3.4.10-1noble.20260121.185614`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-launch-testing-ament-cmake/copyright`)

- `Apache License 2.0`
- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-launch-testing-ros=0.26.11-1noble.20260126.192739`

Binary Packages:

- `ros-jazzy-launch-testing-ros=0.26.11-1noble.20260126.192739`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-launch-testing-ros/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-launch-testing=3.4.10-1noble.20260121.180201`

Binary Packages:

- `ros-jazzy-launch-testing=3.4.10-1noble.20260121.180201`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-launch-testing/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-launch-xml=3.4.10-1noble.20260121.180051`

Binary Packages:

- `ros-jazzy-launch-xml=3.4.10-1noble.20260121.180051`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-launch-xml/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-launch-yaml=3.4.10-1noble.20260121.180052`

Binary Packages:

- `ros-jazzy-launch-yaml=3.4.10-1noble.20260121.180052`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-launch-yaml/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-launch=3.4.10-1noble.20260121.175939`

Binary Packages:

- `ros-jazzy-launch=3.4.10-1noble.20260121.175939`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-launch/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-libstatistics-collector=1.7.4-1noble.20260126.174616`

Binary Packages:

- `ros-jazzy-libstatistics-collector=1.7.4-1noble.20260126.174616`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-libstatistics-collector/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-libyaml-vendor=1.6.3-2noble.20260121.185520`

Binary Packages:

- `ros-jazzy-libyaml-vendor=1.6.3-2noble.20260121.185520`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-libyaml-vendor/copyright`)

- `Apache License 2.0`
- `MIT`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-lifecycle-msgs=2.0.3-1noble.20260126.172741`

Binary Packages:

- `ros-jazzy-lifecycle-msgs=2.0.3-1noble.20260126.172741`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-lifecycle-msgs/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-nav-msgs=5.3.6-1noble.20260126.174111`

Binary Packages:

- `ros-jazzy-nav-msgs=5.3.6-1noble.20260126.174111`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-nav-msgs/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-osrf-pycommon=2.1.7-1noble.20260121.175902`

Binary Packages:

- `ros-jazzy-osrf-pycommon=2.1.7-1noble.20260121.175902`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-osrf-pycommon/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-pluginlib=5.4.4-1noble.20260126.171259`

Binary Packages:

- `ros-jazzy-pluginlib=5.4.4-1noble.20260126.171259`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-pluginlib/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-python-cmake-module=0.11.1-2noble.20260121.185427`

Binary Packages:

- `ros-jazzy-python-cmake-module=0.11.1-2noble.20260121.185427`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-python-cmake-module/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rcl-action=9.2.9-1noble.20260126.174622`

Binary Packages:

- `ros-jazzy-rcl-action=9.2.9-1noble.20260126.174622`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rcl-action/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rcl-interfaces=2.0.3-1noble.20260126.172904`

Binary Packages:

- `ros-jazzy-rcl-interfaces=2.0.3-1noble.20260126.172904`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rcl-interfaces/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rcl-lifecycle=9.2.9-1noble.20260126.174629`

Binary Packages:

- `ros-jazzy-rcl-lifecycle=9.2.9-1noble.20260126.174629`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rcl-lifecycle/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rcl-logging-interface=3.1.1-1noble.20260121.182751`

Binary Packages:

- `ros-jazzy-rcl-logging-interface=3.1.1-1noble.20260121.182751`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rcl-logging-interface/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rcl-logging-spdlog=3.1.1-1noble.20260126.170620`

Binary Packages:

- `ros-jazzy-rcl-logging-spdlog=3.1.1-1noble.20260126.170620`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rcl-logging-spdlog/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rcl-yaml-param-parser=9.2.9-1noble.20260126.170951`

Binary Packages:

- `ros-jazzy-rcl-yaml-param-parser=9.2.9-1noble.20260126.170951`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rcl-yaml-param-parser/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rcl=9.2.9-1noble.20260126.174356`

Binary Packages:

- `ros-jazzy-rcl=9.2.9-1noble.20260126.174356`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rcl/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rclcpp-action=28.1.16-1noble.20260126.175649`

Binary Packages:

- `ros-jazzy-rclcpp-action=28.1.16-1noble.20260126.175649`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rclcpp-action/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rclcpp-components=28.1.16-1noble.20260126.175650`

Binary Packages:

- `ros-jazzy-rclcpp-components=28.1.16-1noble.20260126.175650`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rclcpp-components/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rclcpp-lifecycle=28.1.16-1noble.20260126.175705`

Binary Packages:

- `ros-jazzy-rclcpp-lifecycle=28.1.16-1noble.20260126.175705`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rclcpp-lifecycle/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rclcpp=28.1.16-1noble.20260126.174811`

Binary Packages:

- `ros-jazzy-rclcpp=28.1.16-1noble.20260126.174811`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rclcpp/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rclpy=7.1.9-1noble.20260126.174822`

Binary Packages:

- `ros-jazzy-rclpy=7.1.9-1noble.20260126.174822`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rclpy/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rcpputils=2.11.3-1noble.20260126.165804`

Binary Packages:

- `ros-jazzy-rcpputils=2.11.3-1noble.20260126.165804`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rcpputils/copyright`)

- `Apache License 2.0`
- `BSD-3-Clause`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rcutils=6.7.5-1noble.20260121.182606`

Binary Packages:

- `ros-jazzy-rcutils=6.7.5-1noble.20260121.182606`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rcutils/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rmw-dds-common=3.1.1-1noble.20260126.172514`

Binary Packages:

- `ros-jazzy-rmw-dds-common=3.1.1-1noble.20260126.172514`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rmw-dds-common/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rmw-fastrtps-cpp=8.4.3-1noble.20260126.173317`

Binary Packages:

- `ros-jazzy-rmw-fastrtps-cpp=8.4.3-1noble.20260126.173317`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rmw-fastrtps-cpp/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rmw-fastrtps-shared-cpp=8.4.3-1noble.20260126.172842`

Binary Packages:

- `ros-jazzy-rmw-fastrtps-shared-cpp=8.4.3-1noble.20260126.172842`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rmw-fastrtps-shared-cpp/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rmw-implementation-cmake=7.3.3-1noble.20260121.233918`

Binary Packages:

- `ros-jazzy-rmw-implementation-cmake=7.3.3-1noble.20260121.233918`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rmw-implementation-cmake/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rmw-implementation=2.15.6-1noble.20260126.174148`

Binary Packages:

- `ros-jazzy-rmw-implementation=2.15.6-1noble.20260126.174148`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rmw-implementation/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rmw=7.3.3-1noble.20260121.233900`

Binary Packages:

- `ros-jazzy-rmw=7.3.3-1noble.20260121.233900`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rmw/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ros-core=0.11.0-1noble.20260126.203057`

Binary Packages:

- `ros-jazzy-ros-core=0.11.0-1noble.20260126.203057`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ros-core/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ros-environment=4.2.1-1noble.20260121.180302`

Binary Packages:

- `ros-jazzy-ros-environment=4.2.1-1noble.20260121.180302`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ros-environment/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ros-workspace=1.0.3-7noble.20260121.175541`

Binary Packages:

- `ros-jazzy-ros-workspace=1.0.3-7noble.20260121.175541`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ros-workspace/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ros2action=0.32.8-1noble.20260126.192817`

Binary Packages:

- `ros-jazzy-ros2action=0.32.8-1noble.20260126.192817`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ros2action/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ros2cli-common-extensions=0.3.1-1noble.20260126.203029`

Binary Packages:

- `ros-jazzy-ros2cli-common-extensions=0.3.1-1noble.20260126.203029`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ros2cli-common-extensions/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ros2cli=0.32.8-1noble.20260126.192739`

Binary Packages:

- `ros-jazzy-ros2cli=0.32.8-1noble.20260126.192739`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ros2cli/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ros2component=0.32.8-1noble.20260126.202956`

Binary Packages:

- `ros-jazzy-ros2component=0.32.8-1noble.20260126.202956`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ros2component/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ros2doctor=0.32.8-1noble.20260126.192820`

Binary Packages:

- `ros-jazzy-ros2doctor=0.32.8-1noble.20260126.192820`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ros2doctor/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ros2interface=0.32.8-1noble.20260126.202239`

Binary Packages:

- `ros-jazzy-ros2interface=0.32.8-1noble.20260126.202239`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ros2interface/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ros2launch=0.26.11-1noble.20260126.202330`

Binary Packages:

- `ros-jazzy-ros2launch=0.26.11-1noble.20260126.202330`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ros2launch/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ros2lifecycle=0.32.8-1noble.20260126.193225`

Binary Packages:

- `ros-jazzy-ros2lifecycle=0.32.8-1noble.20260126.193225`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ros2lifecycle/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ros2multicast=0.32.8-1noble.20260126.202240`

Binary Packages:

- `ros-jazzy-ros2multicast=0.32.8-1noble.20260126.202240`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ros2multicast/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ros2node=0.32.8-1noble.20260126.192838`

Binary Packages:

- `ros-jazzy-ros2node=0.32.8-1noble.20260126.192838`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ros2node/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ros2param=0.32.8-1noble.20260126.193357`

Binary Packages:

- `ros-jazzy-ros2param=0.32.8-1noble.20260126.193357`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ros2param/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ros2pkg=0.32.8-1noble.20260126.202246`

Binary Packages:

- `ros-jazzy-ros2pkg=0.32.8-1noble.20260126.202246`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ros2pkg/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ros2plugin=5.4.4-1noble.20260126.202329`

Binary Packages:

- `ros-jazzy-ros2plugin=5.4.4-1noble.20260126.202329`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ros2plugin/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ros2run=0.32.8-1noble.20260126.202337`

Binary Packages:

- `ros-jazzy-ros2run=0.32.8-1noble.20260126.202337`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ros2run/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ros2service=0.32.8-1noble.20260126.193042`

Binary Packages:

- `ros-jazzy-ros2service=0.32.8-1noble.20260126.193042`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ros2service/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ros2topic=0.32.8-1noble.20260126.192902`

Binary Packages:

- `ros-jazzy-ros2topic=0.32.8-1noble.20260126.192902`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ros2topic/copyright`)

- `Apache License 2.0`
- `BSD-3-Clause`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosgraph-msgs=2.0.3-1noble.20260126.172519`

Binary Packages:

- `ros-jazzy-rosgraph-msgs=2.0.3-1noble.20260126.172519`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosgraph-msgs/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-adapter=4.6.7-1noble.20260121.190135`

Binary Packages:

- `ros-jazzy-rosidl-adapter=4.6.7-1noble.20260121.190135`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-adapter/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-cli=4.6.7-1noble.20260121.175929`

Binary Packages:

- `ros-jazzy-rosidl-cli=4.6.7-1noble.20260121.175929`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-cli/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-cmake=4.6.7-1noble.20260121.190524`

Binary Packages:

- `ros-jazzy-rosidl-cmake=4.6.7-1noble.20260121.190524`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-cmake/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-core-generators=0.2.0-3noble.20260126.171359`

Binary Packages:

- `ros-jazzy-rosidl-core-generators=0.2.0-3noble.20260126.171359`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-core-generators/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-core-runtime=0.2.0-3noble.20260126.171359`

Binary Packages:

- `ros-jazzy-rosidl-core-runtime=0.2.0-3noble.20260126.171359`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-core-runtime/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-default-generators=1.6.0-3noble.20260126.172405`

Binary Packages:

- `ros-jazzy-rosidl-default-generators=1.6.0-3noble.20260126.172405`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-default-generators/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-default-runtime=1.6.0-3noble.20260126.172405`

Binary Packages:

- `ros-jazzy-rosidl-default-runtime=1.6.0-3noble.20260126.172405`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-default-runtime/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-dynamic-typesupport-fastrtps=0.1.0-3noble.20260121.185132`

Binary Packages:

- `ros-jazzy-rosidl-dynamic-typesupport-fastrtps=0.1.0-3noble.20260121.185132`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-dynamic-typesupport-fastrtps/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-dynamic-typesupport=0.1.2-3noble.20260121.184932`

Binary Packages:

- `ros-jazzy-rosidl-dynamic-typesupport=0.1.2-3noble.20260121.184932`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-dynamic-typesupport/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-generator-c=4.6.7-1noble.20260121.190725`

Binary Packages:

- `ros-jazzy-rosidl-generator-c=4.6.7-1noble.20260121.190725`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-generator-c/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-generator-cpp=4.6.7-1noble.20260121.190850`

Binary Packages:

- `ros-jazzy-rosidl-generator-cpp=4.6.7-1noble.20260121.190850`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-generator-cpp/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-generator-py=0.22.2-1noble.20260126.170959`

Binary Packages:

- `ros-jazzy-rosidl-generator-py=0.22.2-1noble.20260126.170959`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-generator-py/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-generator-type-description=4.6.7-1noble.20260121.190319`

Binary Packages:

- `ros-jazzy-rosidl-generator-type-description=4.6.7-1noble.20260121.190319`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-generator-type-description/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-parser=4.6.7-1noble.20260121.190242`

Binary Packages:

- `ros-jazzy-rosidl-parser=4.6.7-1noble.20260121.190242`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-parser/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-pycommon=4.6.7-1noble.20260121.190342`

Binary Packages:

- `ros-jazzy-rosidl-pycommon=4.6.7-1noble.20260121.190342`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-pycommon/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-runtime-c=4.6.7-1noble.20260121.184806`

Binary Packages:

- `ros-jazzy-rosidl-runtime-c=4.6.7-1noble.20260121.184806`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-runtime-c/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-runtime-cpp=4.6.7-1noble.20260121.184935`

Binary Packages:

- `ros-jazzy-rosidl-runtime-cpp=4.6.7-1noble.20260121.184935`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-runtime-cpp/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-runtime-py=0.13.1-2noble.20260121.190344`

Binary Packages:

- `ros-jazzy-rosidl-runtime-py=0.13.1-2noble.20260121.190344`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-runtime-py/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-typesupport-c=3.2.2-1noble.20260126.170729`

Binary Packages:

- `ros-jazzy-rosidl-typesupport-c=3.2.2-1noble.20260126.170729`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-typesupport-c/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-typesupport-cpp=3.2.2-1noble.20260126.171247`

Binary Packages:

- `ros-jazzy-rosidl-typesupport-cpp=3.2.2-1noble.20260126.171247`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-typesupport-cpp/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-typesupport-fastrtps-c=3.6.3-1noble.20260122.000946`

Binary Packages:

- `ros-jazzy-rosidl-typesupport-fastrtps-c=3.6.3-1noble.20260122.000946`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-typesupport-fastrtps-c/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-typesupport-fastrtps-cpp=3.6.3-1noble.20260121.234335`

Binary Packages:

- `ros-jazzy-rosidl-typesupport-fastrtps-cpp=3.6.3-1noble.20260121.234335`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-typesupport-fastrtps-cpp/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-typesupport-interface=4.6.7-1noble.20260121.184738`

Binary Packages:

- `ros-jazzy-rosidl-typesupport-interface=4.6.7-1noble.20260121.184738`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-typesupport-interface/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-typesupport-introspection-c=4.6.7-1noble.20260121.190852`

Binary Packages:

- `ros-jazzy-rosidl-typesupport-introspection-c=4.6.7-1noble.20260121.190852`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-typesupport-introspection-c/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-typesupport-introspection-cpp=4.6.7-1noble.20260121.191156`

Binary Packages:

- `ros-jazzy-rosidl-typesupport-introspection-cpp=4.6.7-1noble.20260121.191156`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-typesupport-introspection-cpp/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rpyutils=0.4.2-1noble.20260121.175712`

Binary Packages:

- `ros-jazzy-rpyutils=0.4.2-1noble.20260121.175712`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rpyutils/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-sensor-msgs=5.3.6-1noble.20260126.174323`

Binary Packages:

- `ros-jazzy-sensor-msgs=5.3.6-1noble.20260126.174323`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-sensor-msgs/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-service-msgs=2.0.3-1noble.20260126.172035`

Binary Packages:

- `ros-jazzy-service-msgs=2.0.3-1noble.20260126.172035`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-service-msgs/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-shape-msgs=5.3.6-1noble.20260126.175236`

Binary Packages:

- `ros-jazzy-shape-msgs=5.3.6-1noble.20260126.175236`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-shape-msgs/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-spdlog-vendor=1.6.1-1noble.20260121.181931`

Binary Packages:

- `ros-jazzy-spdlog-vendor=1.6.1-1noble.20260121.181931`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-spdlog-vendor/copyright`)

- `Apache License 2.0`
- `MIT`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-sros2-cmake=0.13.5-1noble.20260126.202307`

Binary Packages:

- `ros-jazzy-sros2-cmake=0.13.5-1noble.20260126.202307`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-sros2-cmake/copyright`)

- `Apache 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-sros2=0.13.5-1noble.20260126.192847`

Binary Packages:

- `ros-jazzy-sros2=0.13.5-1noble.20260126.192847`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-sros2/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-statistics-msgs=2.0.3-1noble.20260126.172518`

Binary Packages:

- `ros-jazzy-statistics-msgs=2.0.3-1noble.20260126.172518`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-statistics-msgs/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-std-msgs=5.3.6-1noble.20260126.172518`

Binary Packages:

- `ros-jazzy-std-msgs=5.3.6-1noble.20260126.172518`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-std-msgs/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-std-srvs=5.3.6-1noble.20260126.173903`

Binary Packages:

- `ros-jazzy-std-srvs=5.3.6-1noble.20260126.173903`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-std-srvs/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-stereo-msgs=5.3.6-1noble.20260126.175233`

Binary Packages:

- `ros-jazzy-stereo-msgs=5.3.6-1noble.20260126.175233`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-stereo-msgs/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-tinyxml2-vendor=0.9.2-1noble.20260121.184817`

Binary Packages:

- `ros-jazzy-tinyxml2-vendor=0.9.2-1noble.20260121.184817`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-tinyxml2-vendor/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-tracetools=8.2.5-1noble.20260121.233820`

Binary Packages:

- `ros-jazzy-tracetools=8.2.5-1noble.20260121.233820`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-tracetools/copyright`)

- `Apache 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-trajectory-msgs=5.3.6-1noble.20260126.174426`

Binary Packages:

- `ros-jazzy-trajectory-msgs=5.3.6-1noble.20260126.174426`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-trajectory-msgs/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-type-description-interfaces=2.0.3-1noble.20260126.172111`

Binary Packages:

- `ros-jazzy-type-description-interfaces=2.0.3-1noble.20260126.172111`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-type-description-interfaces/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-uncrustify-vendor=3.0.1-1noble.20260121.181949`

Binary Packages:

- `ros-jazzy-uncrustify-vendor=3.0.1-1noble.20260121.181949`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-uncrustify-vendor/copyright`)

- `Apache License 2.0`
- `GNU General Public License v2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-unique-identifier-msgs=2.5.0-3noble.20260126.171713`

Binary Packages:

- `ros-jazzy-unique-identifier-msgs=2.5.0-3noble.20260126.171713`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-unique-identifier-msgs/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-visualization-msgs=5.3.6-1noble.20260126.174847`

Binary Packages:

- `ros-jazzy-visualization-msgs=5.3.6-1noble.20260126.174847`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-visualization-msgs/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `rpcsvc-proto=1.4.2-0ubuntu7`

Binary Packages:

- `rpcsvc-proto=1.4.2-0ubuntu7`

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


### `dpkg` source package: `sensible-utils=0.0.22`

Binary Packages:

- `sensible-utils=0.0.22`

Licenses: (parsed from: `/usr/share/doc/sensible-utils/copyright`)

- `All-permissive`
- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`
- `configure`
- `installsh`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/sensible-utils/0.0.22/


### `dpkg` source package: `setuptools=68.1.2-2ubuntu1.2`

Binary Packages:

- `python3-pkg-resources=68.1.2-2ubuntu1.2`
- `python3-setuptools=68.1.2-2ubuntu1.2`

Licenses: (parsed from: `/usr/share/doc/python3-pkg-resources/copyright`, `/usr/share/doc/python3-setuptools/copyright`)

- `Apache-2.0`
- `BSD-3-clause`

Source:

```console
$ apt-get source -qq --print-uris setuptools=68.1.2-2ubuntu1.2
'http://archive.ubuntu.com/ubuntu/pool/main/s/setuptools/setuptools_68.1.2-2ubuntu1.2.dsc' setuptools_68.1.2-2ubuntu1.2.dsc 2296 SHA512:4d7bf690b646aaaef52f1bdddba79dc2402fb941afb24f2fd4ad0339018c285ea77e7d856ce839bf99a82b3c27d99e1dfb4b6ffc27b2a5dceacf2e017292b109
'http://archive.ubuntu.com/ubuntu/pool/main/s/setuptools/setuptools_68.1.2.orig.tar.gz' setuptools_68.1.2.orig.tar.gz 2198001 SHA512:a5a84102ce72f38162b190b91286013cb8660b45f383df04fba65e38c658a5c5b93cdf05f789436618fa596b3ca6688a7c54d31d6d10b729124d3b135660c328
'http://archive.ubuntu.com/ubuntu/pool/main/s/setuptools/setuptools_68.1.2-2ubuntu1.2.debian.tar.xz' setuptools_68.1.2-2ubuntu1.2.debian.tar.xz 17712 SHA512:48a17f679f1122b494c68d35436ebc5f248a42bea2f0deea70b81f6d29496b15ce62e71f1e6ef35ca851a77bb0ebac94452aea32779fbecddbe832ef93184c65
```

### `dpkg` source package: `sgml-base=1.31`

Binary Packages:

- `sgml-base=1.31`

Licenses: (parsed from: `/usr/share/doc/sgml-base/copyright`)

- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/sgml-base/1.31/


### `dpkg` source package: `shadow=1:4.13+dfsg1-4ubuntu3.2`

Binary Packages:

- `login=1:4.13+dfsg1-4ubuntu3.2`
- `passwd=1:4.13+dfsg1-4ubuntu3.2`

Licenses: (parsed from: `/usr/share/doc/login/copyright`, `/usr/share/doc/passwd/copyright`)

- `BSD-3-clause`
- `GPL-1`
- `GPL-2`
- `GPL-2+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris shadow=1:4.13+dfsg1-4ubuntu3.2
'http://archive.ubuntu.com/ubuntu/pool/main/s/shadow/shadow_4.13%2bdfsg1-4ubuntu3.2.dsc' shadow_4.13+dfsg1-4ubuntu3.2.dsc 2400 SHA512:705091aa67f89349a8eb829d3abbac649a417080b7c2d9aa46d0a887dacee4a1cb52642c0bc4e7cdb4b277e5747ae516330174d959522bb5d33bc8c54449a190
'http://archive.ubuntu.com/ubuntu/pool/main/s/shadow/shadow_4.13%2bdfsg1.orig.tar.xz' shadow_4.13+dfsg1.orig.tar.xz 1811752 SHA512:27106ca26d6e4c9e5833cf79811b10f656ade547bbc18b87faf79bbe0581a9e1467cbb6c354320e2d5233d17208d77742ebf197d32b6d2f08439e37e368ded1d
'http://archive.ubuntu.com/ubuntu/pool/main/s/shadow/shadow_4.13%2bdfsg1-4ubuntu3.2.debian.tar.xz' shadow_4.13+dfsg1-4ubuntu3.2.debian.tar.xz 96392 SHA512:67cd7c7f869250d39ebb7af023ae4aca6eef88de143a85510135d547bb6988895ef02d9aff798888e5d507f415d7d17193c354b2437764b0c4bea18b1178531d
```

### `dpkg` source package: `six=1.16.0-4`

Binary Packages:

- `python3-six=1.16.0-4`

Licenses: (parsed from: `/usr/share/doc/python3-six/copyright`)

- `Expat`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/six/1.16.0-4/


### `dpkg` source package: `snowball=2.2.0-4build1`

Binary Packages:

- `python3-snowballstemmer=2.2.0-4build1`

Licenses: (parsed from: `/usr/share/doc/python3-snowballstemmer/copyright`)

- `BSD-3-snowball`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `spdlog=1:1.12.0+ds-2build1`

Binary Packages:

- `libspdlog-dev:amd64=1:1.12.0+ds-2build1`
- `libspdlog1.12:amd64=1:1.12.0+ds-2build1`

Licenses: (parsed from: `/usr/share/doc/libspdlog-dev/copyright`, `/usr/share/doc/libspdlog1.12/copyright`)

- `Expat`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `sphinx=7.2.6-6`

Binary Packages:

- `libjs-sphinxdoc=7.2.6-6`

Licenses: (parsed from: `/usr/share/doc/libjs-sphinxdoc/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/sphinx/7.2.6-6/


### `dpkg` source package: `sqlite3=3.45.1-1ubuntu2.5`

Binary Packages:

- `libsqlite3-0:amd64=3.45.1-1ubuntu2.5`

Licenses: (parsed from: `/usr/share/doc/libsqlite3-0/copyright`)

- `GPL-2`
- `GPL-2+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris sqlite3=3.45.1-1ubuntu2.5
'http://archive.ubuntu.com/ubuntu/pool/main/s/sqlite3/sqlite3_3.45.1-1ubuntu2.5.dsc' sqlite3_3.45.1-1ubuntu2.5.dsc 2601 SHA512:fb56794498668ca451db41d705708b505877abaa88f4bd36b47d7642f3f9513fb3597c77517e05dd821c90a341de8c032c3f7f39ebdc40a33b99a1802f51907a
'http://archive.ubuntu.com/ubuntu/pool/main/s/sqlite3/sqlite3_3.45.1.orig-www.tar.xz' sqlite3_3.45.1.orig-www.tar.xz 5693812 SHA512:dbbf32bad3912dca4d1d3366053c66dc53745d4e5c6892c10470b7452f338de03eee1406cb6c5a972c9890bd71a7b30563e4863f27bf0f2813a92ffdfd95832f
'http://archive.ubuntu.com/ubuntu/pool/main/s/sqlite3/sqlite3_3.45.1.orig.tar.xz' sqlite3_3.45.1.orig.tar.xz 8257884 SHA512:8ea4a50fe730b072271978bbeee074d567bc8cbaa3bb4a8b8802e012d470fd482d800532eedea48a54fd64785f3b02aab7b033c8e2767a5e8b9f02a9cc844b80
'http://archive.ubuntu.com/ubuntu/pool/main/s/sqlite3/sqlite3_3.45.1-1ubuntu2.5.debian.tar.xz' sqlite3_3.45.1-1ubuntu2.5.debian.tar.xz 35260 SHA512:a031e8f6aeefbb9ea45439a24dc82f9e74b12c3e92b6444057648cc07187c00a0ca6cf32a6c51c0e50787f41d525c687cc3dad7492b46d785fa1088b04d10ea1
```

### `dpkg` source package: `systemd=255.4-1ubuntu8.14`

Binary Packages:

- `libsystemd0:amd64=255.4-1ubuntu8.14`
- `libudev1:amd64=255.4-1ubuntu8.14`

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
$ apt-get source -qq --print-uris systemd=255.4-1ubuntu8.14
'http://security.ubuntu.com/ubuntu/pool/main/s/systemd/systemd_255.4-1ubuntu8.14.dsc' systemd_255.4-1ubuntu8.14.dsc 7324 SHA512:cc3b0d413b31e1995708683ea8bfb139952b74783ccfcc8c4dcc1d0b3950ebecfa58eeb54f01a5d44e38ee85b55107c830ce42d2571c2042da8d0cc2a204aa1e
'http://security.ubuntu.com/ubuntu/pool/main/s/systemd/systemd_255.4.orig.tar.gz' systemd_255.4.orig.tar.gz 14952427 SHA512:8a2bde11a55f7f788ba7751789a5e9be6ce9634e88d54e49f6e832c4c49020c6cacaf2a610fe26f92998b0cbf43c6c2150a96b2c0953d23261009f57d71ea979
'http://security.ubuntu.com/ubuntu/pool/main/s/systemd/systemd_255.4-1ubuntu8.14.debian.tar.xz' systemd_255.4-1ubuntu8.14.debian.tar.xz 262172 SHA512:a7e3657be6aebac7b2baeacc4e179db686565a3db05f0730ce8f10e36d075dc8db8af43433ec712c3f45331b061614f76dedbfe08d00dd7f06c4a79e2fdde11d
```

### `dpkg` source package: `sysvinit=3.08-6ubuntu3`

Binary Packages:

- `sysvinit-utils=3.08-6ubuntu3`

Licenses: (parsed from: `/usr/share/doc/sysvinit-utils/copyright`)

- `GPL-2`
- `GPL-2.0`
- `GPL-2.0+`
- `GPL-3`
- `GPL-3.0`
- `LGPL-2.1`
- `LGPL-2.1+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `tar=1.35+dfsg-3build1`

Binary Packages:

- `tar=1.35+dfsg-3build1`

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


### `dpkg` source package: `tinyxml2=10.0.0+dfsg-2`

Binary Packages:

- `libtinyxml2-10:amd64=10.0.0+dfsg-2`
- `libtinyxml2-dev:amd64=10.0.0+dfsg-2`

Licenses: (parsed from: `/usr/share/doc/libtinyxml2-10/copyright`, `/usr/share/doc/libtinyxml2-dev/copyright`)

- `GPL-2`
- `GPL-2+`
- `zlib/libpng`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/tinyxml2/10.0.0+dfsg-2/


### `dpkg` source package: `tzdata=2026a-0ubuntu0.24.04.1`

Binary Packages:

- `tzdata=2026a-0ubuntu0.24.04.1`

Licenses: (parsed from: `/usr/share/doc/tzdata/copyright`)

- `ICU`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris tzdata=2026a-0ubuntu0.24.04.1
'http://archive.ubuntu.com/ubuntu/pool/main/t/tzdata/tzdata_2026a-0ubuntu0.24.04.1.dsc' tzdata_2026a-0ubuntu0.24.04.1.dsc 2728 SHA512:a798cda54f303c368e7a8b650bc17589573286744ccd32feb7023c654ee8b656d66038e144bbfc5c489f313d426ab0b10e62f4772b28c9dadcb036f3a3435c34
'http://archive.ubuntu.com/ubuntu/pool/main/t/tzdata/tzdata_2026a.orig.tar.gz' tzdata_2026a.orig.tar.gz 471812 SHA512:407e8e93aaa054a22a4a7d6d8cf480a20630073bf1a00956df16b10318f239a12015de38fad3072249193e314d6fddbff4e74afa40a88f7bf5c9eecc7659ea15
'http://archive.ubuntu.com/ubuntu/pool/main/t/tzdata/tzdata_2026a.orig.tar.gz.asc' tzdata_2026a.orig.tar.gz.asc 833 SHA512:e84300a1a26c9bcd1f53dc9807794fc3424a362dff7101615592c8f323c4e5ad72be82c4d36220e2666376945f4aaaaa2fbcb87486eda90f23ea1b37e4cf3833
'http://archive.ubuntu.com/ubuntu/pool/main/t/tzdata/tzdata_2026a-0ubuntu0.24.04.1.debian.tar.xz' tzdata_2026a-0ubuntu0.24.04.1.debian.tar.xz 188416 SHA512:84d284dba6a64e9b0b3d26f5b74a4ab57907edf0643f7e97393801aff6fa2ae70c1d94493111165c825fff41911f14da58f067c71fb9017e27b2578fad44f089
```

### `dpkg` source package: `ubuntu-keyring=2023.11.28.1`

Binary Packages:

- `ubuntu-keyring=2023.11.28.1`

Licenses: (parsed from: `/usr/share/doc/ubuntu-keyring/copyright`)

- `GPL`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `uncrustify=0.78.1+dfsg1-1`

Binary Packages:

- `uncrustify=0.78.1+dfsg1-1`

Licenses: (parsed from: `/usr/share/doc/uncrustify/copyright`)

- `Artistic`
- `GPL`
- `GPL-2`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/uncrustify/0.78.1+dfsg1-1/


### `dpkg` source package: `underscore=1.13.4~dfsg+~1.11.4-3`

Binary Packages:

- `libjs-underscore=1.13.4~dfsg+~1.11.4-3`

Licenses: (parsed from: `/usr/share/doc/libjs-underscore/copyright`)

- `BSD-3-clause`
- `Expat`
- `GPL-3`
- `GPL-3+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/underscore/1.13.4~dfsg+~1.11.4-3/


### `dpkg` source package: `unminimize=0.2.1`

Binary Packages:

- `unminimize=0.2.1`

Licenses: (parsed from: `/usr/share/doc/unminimize/copyright`)

- `GPL-2`
- `GPL-2.0+`

Source:

```console
$ apt-get source -qq --print-uris unminimize=0.2.1
'http://archive.ubuntu.com/ubuntu/pool/main/u/unminimize/unminimize_0.2.1.dsc' unminimize_0.2.1.dsc 1554 SHA512:28b51904aaf6edb27c93d250e5b91caa1d39ff749e059be036be4bf8ff710ee9812b5080c678b155db45dfbbb01dd30ea7908728aa5d0129108aa630db1c2aef
'http://archive.ubuntu.com/ubuntu/pool/main/u/unminimize/unminimize_0.2.1.tar.xz' unminimize_0.2.1.tar.xz 9400 SHA512:692ed9d0bb2d42ab5c74ef0f4c86d8f5922e4d1ee9d8efa8a03490437aff35c13b0114f7a62aa5464e95d4014db2745605a83fe7d9bfc81977de8ad56e3e901e
```

### `dpkg` source package: `ust=2.13.7-1.1ubuntu2`

Binary Packages:

- `liblttng-ust-common1t64:amd64=2.13.7-1.1ubuntu2`
- `liblttng-ust-ctl5t64:amd64=2.13.7-1.1ubuntu2`
- `liblttng-ust-dev:amd64=2.13.7-1.1ubuntu2`
- `liblttng-ust-python-agent1t64:amd64=2.13.7-1.1ubuntu2`
- `liblttng-ust1t64:amd64=2.13.7-1.1ubuntu2`

Licenses: (parsed from: `/usr/share/doc/liblttng-ust-common1t64/copyright`, `/usr/share/doc/liblttng-ust-ctl5t64/copyright`, `/usr/share/doc/liblttng-ust-dev/copyright`, `/usr/share/doc/liblttng-ust-python-agent1t64/copyright`, `/usr/share/doc/liblttng-ust1t64/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `Expat`
- `FSFAP`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `LGPL-2.1`
- `LGPL-2.1+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `util-linux=2.39.3-9ubuntu6.5`

Binary Packages:

- `bsdutils=1:2.39.3-9ubuntu6.5`
- `libblkid1:amd64=2.39.3-9ubuntu6.5`
- `libmount1:amd64=2.39.3-9ubuntu6.5`
- `libsmartcols1:amd64=2.39.3-9ubuntu6.5`
- `libuuid1:amd64=2.39.3-9ubuntu6.5`
- `mount=2.39.3-9ubuntu6.5`
- `util-linux=2.39.3-9ubuntu6.5`
- `uuid-dev:amd64=2.39.3-9ubuntu6.5`

Licenses: (parsed from: `/usr/share/doc/bsdutils/copyright`, `/usr/share/doc/libblkid1/copyright`, `/usr/share/doc/libmount1/copyright`, `/usr/share/doc/libsmartcols1/copyright`, `/usr/share/doc/libuuid1/copyright`, `/usr/share/doc/mount/copyright`, `/usr/share/doc/util-linux/copyright`, `/usr/share/doc/uuid-dev/copyright`)

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
$ apt-get source -qq --print-uris util-linux=2.39.3-9ubuntu6.5
'http://archive.ubuntu.com/ubuntu/pool/main/u/util-linux/util-linux_2.39.3-9ubuntu6.5.dsc' util-linux_2.39.3-9ubuntu6.5.dsc 4726 SHA512:be8fead4961e232992465ff9fce0286fda32445e44d1c9cc6b7b1135c1efea1ac941bb3e497f273e9af9414e299bce942eb677eebff5fc625533f6d02dd1b9cf
'http://archive.ubuntu.com/ubuntu/pool/main/u/util-linux/util-linux_2.39.3.orig.tar.xz' util-linux_2.39.3.orig.tar.xz 8526168 SHA512:a2de1672f06ca5d2d431db1265a8499808770c3781019ec4a3a40170df4685826d8e3ca120841dcc5df4681ca8c935a993317bd0dc70465b21bf8e0efef65afa
'http://archive.ubuntu.com/ubuntu/pool/main/u/util-linux/util-linux_2.39.3-9ubuntu6.5.debian.tar.xz' util-linux_2.39.3-9ubuntu6.5.debian.tar.xz 148016 SHA512:8c6db47b20b6a9dfe18a37b77308e0f99756f10e837f09cc7afe550b55a43f904fd2d6b5457b4a5519df9ca5422f4df76609e2bece2ffae84c6186cdb0cd4cb5
```

### `dpkg` source package: `xml-core=0.19`

Binary Packages:

- `xml-core=0.19`

Licenses: (parsed from: `/usr/share/doc/xml-core/copyright`)

- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/xml-core/0.19/


### `dpkg` source package: `xxhash=0.8.2-2build1`

Binary Packages:

- `libxxhash0:amd64=0.8.2-2build1`

Licenses: (parsed from: `/usr/share/doc/libxxhash0/copyright`)

- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `xz-utils=5.6.1+really5.4.5-1ubuntu0.2`

Binary Packages:

- `liblzma5:amd64=5.6.1+really5.4.5-1ubuntu0.2`

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
$ apt-get source -qq --print-uris xz-utils=5.6.1+really5.4.5-1ubuntu0.2
'http://archive.ubuntu.com/ubuntu/pool/main/x/xz-utils/xz-utils_5.6.1%2breally5.4.5-1ubuntu0.2.dsc' xz-utils_5.6.1+really5.4.5-1ubuntu0.2.dsc 2639 SHA512:b10ba1ba72e3f1ea6c12b5d1f84bf21b2651e5e796d35b821c14370ecb65953a02e32e3d5f21587191e5b62757b34ae0af2ba64b399670b4c4fd46e04b9b7811
'http://archive.ubuntu.com/ubuntu/pool/main/x/xz-utils/xz-utils_5.6.1%2breally5.4.5.orig.tar.xz' xz-utils_5.6.1+really5.4.5.orig.tar.xz 1680520 SHA512:5cbc3b5bb35a9f5773ad657788fe77013471e3b621c5a8149deb7389d48535926e5bed103456fcfe5ecb044b236b1055b03938a6cc877cfc749372b899fc79e5
'http://archive.ubuntu.com/ubuntu/pool/main/x/xz-utils/xz-utils_5.6.1%2breally5.4.5-1ubuntu0.2.debian.tar.xz' xz-utils_5.6.1+really5.4.5-1ubuntu0.2.debian.tar.xz 30776 SHA512:1891c935b3915749aaa4f29b494c3d3156dd7a04b4637148d6a668ab5fb464a0bd2be441108750e5601244921f38e47c2d25490cf07d0066da566e5d36756582
```

### `dpkg` source package: `zlib=1:1.3.dfsg-3.1ubuntu2.1`

Binary Packages:

- `zlib1g:amd64=1:1.3.dfsg-3.1ubuntu2.1`
- `zlib1g-dev:amd64=1:1.3.dfsg-3.1ubuntu2.1`

Licenses: (parsed from: `/usr/share/doc/zlib1g/copyright`, `/usr/share/doc/zlib1g-dev/copyright`)

- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris zlib=1:1.3.dfsg-3.1ubuntu2.1
'http://archive.ubuntu.com/ubuntu/pool/main/z/zlib/zlib_1.3.dfsg-3.1ubuntu2.1.dsc' zlib_1.3.dfsg-3.1ubuntu2.1.dsc 3116 SHA512:5cf00ba3f81611c9e94321e524dfcbbe19b7f7d8570e0bc15da334ecf72d212cc22366659ed5ede3e1716ba1ebd2e05c65663e64f1e283fb1f84a3956fd2f4c3
'http://archive.ubuntu.com/ubuntu/pool/main/z/zlib/zlib_1.3.dfsg.orig.tar.xz' zlib_1.3.dfsg.orig.tar.xz 1128572 SHA512:be6f020c691c61fe4ddcb27d3f8b2515435f544177e0b97286b5e85afc3862c1de6cd74a14ff6b065d620d046d35bf029fabfd1cf473f43a2cad60bf9ad55afe
'http://archive.ubuntu.com/ubuntu/pool/main/z/zlib/zlib_1.3.dfsg-3.1ubuntu2.1.debian.tar.xz' zlib_1.3.dfsg-3.1ubuntu2.1.debian.tar.xz 61028 SHA512:18f491ffac55e6f9464befc89bbe3067030dfd30d8093c06cd7aa511e4534123b87cecf8f2dde4c7447c77de7965b488de6f407637b4a1ace2f55afc0adae170
```
