# `ros:jazzy-ros-base`

## Docker Metadata

- Image ID: `sha256:277f4249e792af1be98e76d5e3b71faa7086aaeb9f5a90e902c9461a6ac3e673`
- Created: `2026-04-15T21:46:18.157250947Z`
- Virtual Size: ~ 879.48 Mb  
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
'http://archive.ubuntu.com/ubuntu/pool/main/a/acl/acl_2.3.2.orig.tar.xz' acl_2.3.2.orig.tar.xz 371680 SHA256:97203a72cae99ab89a067fe2210c1cbf052bc492b479eca7d226d9830883b0bd
'http://archive.ubuntu.com/ubuntu/pool/main/a/acl/acl_2.3.2.orig.tar.xz.asc' acl_2.3.2.orig.tar.xz.asc 833 SHA256:184c6a903490885a096095db67b433a04542c6569f167cbe8115268c0f227273
'http://archive.ubuntu.com/ubuntu/pool/main/a/acl/acl_2.3.2-1build1.1.debian.tar.xz' acl_2.3.2-1build1.1.debian.tar.xz 23472 SHA256:0d324adb403a50aa2889a11e098d34ce5adecd1cb89f83799f66dbb1d8b71280
'http://archive.ubuntu.com/ubuntu/pool/main/a/acl/acl_2.3.2-1build1.1.dsc' acl_2.3.2-1build1.1.dsc 2616 SHA256:da831b979338d324df2adcedd5a06f9a5f303e83be2b43d58ee39288dde8fc88
```

### `dpkg` source package: `adduser=3.137ubuntu1`

Binary Packages:

- `adduser=3.137ubuntu1`

Licenses: (parsed from: `/usr/share/doc/adduser/copyright`)

- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ann=1.1.2+doc-9build1`

Binary Packages:

- `libann0=1.1.2+doc-9build1`

Licenses: (parsed from: `/usr/share/doc/libann0/copyright`)

- `GPL-3`
- `GPL-3.0+`
- `LGPL-2.1`
- `LGPL-2.1+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `aom=3.8.2-2ubuntu0.1`

Binary Packages:

- `libaom3:amd64=3.8.2-2ubuntu0.1`

Licenses: (parsed from: `/usr/share/doc/libaom3/copyright`)

- `BSD-2-Clause`
- `BSD-2-clause`
- `BSD-3-clause`
- `Expat`
- `ISC`
- `public-domain-md5`

Source:

```console
$ apt-get source -qq --print-uris aom=3.8.2-2ubuntu0.1
'http://archive.ubuntu.com/ubuntu/pool/main/a/aom/aom_3.8.2.orig.tar.gz' aom_3.8.2.orig.tar.gz 5466676 SHA256:08be381e014c3cf508293f9127c8e24cc35262c6e9c805b0a8313cebf99cbcda
'http://archive.ubuntu.com/ubuntu/pool/main/a/aom/aom_3.8.2-2ubuntu0.1.debian.tar.xz' aom_3.8.2-2ubuntu0.1.debian.tar.xz 22776 SHA256:a1c3b5c2db4cdb1756aecd90f474d0be1447196330bf385f9db600455b817d27
'http://archive.ubuntu.com/ubuntu/pool/main/a/aom/aom_3.8.2-2ubuntu0.1.dsc' aom_3.8.2-2ubuntu0.1.dsc 2395 SHA256:2cba9732b1e244fd5d59feaffa23fac4258c3914a8d30d627a7ce562fadbbbae
```

### `dpkg` source package: `apparmor=4.0.1really4.0.1-0ubuntu0.24.04.6`

Binary Packages:

- `libapparmor1:amd64=4.0.1really4.0.1-0ubuntu0.24.04.6`

Licenses: (parsed from: `/usr/share/doc/libapparmor1/copyright`)

- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris apparmor=4.0.1really4.0.1-0ubuntu0.24.04.6
'http://archive.ubuntu.com/ubuntu/pool/main/a/apparmor/apparmor_4.0.1really4.0.1.orig.tar.gz' apparmor_4.0.1really4.0.1.orig.tar.gz 6984984 SHA256:b0d72cedc48e533d189ea415bde721ad597101c77fa398fdd2858ec4f58f7e26
'http://archive.ubuntu.com/ubuntu/pool/main/a/apparmor/apparmor_4.0.1really4.0.1-0ubuntu0.24.04.6.debian.tar.xz' apparmor_4.0.1really4.0.1-0ubuntu0.24.04.6.debian.tar.xz 139420 SHA256:51a252cd1729abd4900107ed80aef09868f8719fc5336b81749379fe42167f7c
'http://archive.ubuntu.com/ubuntu/pool/main/a/apparmor/apparmor_4.0.1really4.0.1-0ubuntu0.24.04.6.dsc' apparmor_4.0.1really4.0.1-0ubuntu0.24.04.6.dsc 3434 SHA256:5e8a01d1e3319f0c0d4d93805e9133c36a2b39b065ef871d114563ca225fa32d
```

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
'http://archive.ubuntu.com/ubuntu/pool/main/a/apt/apt_2.8.3.tar.xz' apt_2.8.3.tar.xz 2354680 SHA256:088522b3613b28fdbcfa61f1f7e476bf6dc6b0120a8f74409e9527580c9f9d3b
'http://archive.ubuntu.com/ubuntu/pool/main/a/apt/apt_2.8.3.dsc' apt_2.8.3.dsc 2973 SHA256:1d41cd04115e1a79f0fa4d738e5c34603ae8a4f40122d8a18a622fd6d20a5523
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
'http://archive.ubuntu.com/ubuntu/pool/main/a/attr/attr_2.5.2.orig.tar.xz' attr_2.5.2.orig.tar.xz 334180 SHA256:f2e97b0ab7ce293681ab701915766190d607a1dba7fae8a718138150b700a70b
'http://archive.ubuntu.com/ubuntu/pool/main/a/attr/attr_2.5.2.orig.tar.xz.asc' attr_2.5.2.orig.tar.xz.asc 833 SHA256:eeac729088d3c6379e91b7596cb3582e46b047c47f0fa3c5c77f9c9e84dc3a4c
'http://archive.ubuntu.com/ubuntu/pool/main/a/attr/attr_2.5.2-1build1.1.debian.tar.xz' attr_2.5.2-1build1.1.debian.tar.xz 26032 SHA256:9d020c0d557c8a932da9e330683e2cfaa8afc932bd9181b96dfda23077901e7f
'http://archive.ubuntu.com/ubuntu/pool/main/a/attr/attr_2.5.2-1build1.1.dsc' attr_2.5.2-1build1.1.dsc 2588 SHA256:0397ea8ae0991bbf21ca031e5312439f3b050f185c3016ef52ba4c627493debe
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
'http://archive.ubuntu.com/ubuntu/pool/main/a/audit/audit_3.1.2.orig.tar.gz' audit_3.1.2.orig.tar.gz 1219860 SHA256:c0b1792d1f0a88c6f1828710509cbb987059fc68712c97669ca90eae103d287d
'http://archive.ubuntu.com/ubuntu/pool/main/a/audit/audit_3.1.2-2.1build1.1.debian.tar.xz' audit_3.1.2-2.1build1.1.debian.tar.xz 18860 SHA256:ed9d8bb3ff1194b6c8943c7768596383f995b1d45dbc57b8f5ca5868a7b22558
'http://archive.ubuntu.com/ubuntu/pool/main/a/audit/audit_3.1.2-2.1build1.1.dsc' audit_3.1.2-2.1build1.1.dsc 2848 SHA256:3df86dee4b6d645173901fad492776add35f82c4e7c58cd8a4f82931a2588324
```

### `dpkg` source package: `base-files=13ubuntu10.4`

Binary Packages:

- `base-files=13ubuntu10.4`

Licenses: (parsed from: `/usr/share/doc/base-files/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris base-files=13ubuntu10.4
'http://archive.ubuntu.com/ubuntu/pool/main/b/base-files/base-files_13ubuntu10.4.tar.xz' base-files_13ubuntu10.4.tar.xz 94240 SHA256:3656f87d5a7ed92ac53cece416f918099e7e4f90281c3effcc346e2ce09c653d
'http://archive.ubuntu.com/ubuntu/pool/main/b/base-files/base-files_13ubuntu10.4.dsc' base-files_13ubuntu10.4.dsc 1642 SHA256:db0386e7111a5e0b1f9d473b1fdae76f421f0df4e66edfdbc8060cf3dc92a561
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


### `dpkg` source package: `binutils=2.42-4ubuntu2.10`

Binary Packages:

- `binutils=2.42-4ubuntu2.10`
- `binutils-common:amd64=2.42-4ubuntu2.10`
- `binutils-x86-64-linux-gnu=2.42-4ubuntu2.10`
- `libbinutils:amd64=2.42-4ubuntu2.10`
- `libctf-nobfd0:amd64=2.42-4ubuntu2.10`
- `libctf0:amd64=2.42-4ubuntu2.10`
- `libgprofng0:amd64=2.42-4ubuntu2.10`
- `libsframe1:amd64=2.42-4ubuntu2.10`

Licenses: (parsed from: `/usr/share/doc/binutils/copyright`, `/usr/share/doc/binutils-common/copyright`, `/usr/share/doc/binutils-x86-64-linux-gnu/copyright`, `/usr/share/doc/libbinutils/copyright`, `/usr/share/doc/libctf-nobfd0/copyright`, `/usr/share/doc/libctf0/copyright`, `/usr/share/doc/libgprofng0/copyright`, `/usr/share/doc/libsframe1/copyright`)

- `GFDL`
- `GPL`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris binutils=2.42-4ubuntu2.10
'http://archive.ubuntu.com/ubuntu/pool/main/b/binutils/binutils_2.42.orig.tar.xz' binutils_2.42.orig.tar.xz 27567160 SHA256:f6e4d41fd5fc778b06b7891457b3620da5ecea1006c6a4a41ae998109f85a800
'http://archive.ubuntu.com/ubuntu/pool/main/b/binutils/binutils_2.42-4ubuntu2.10.debian.tar.xz' binutils_2.42-4ubuntu2.10.debian.tar.xz 196552 SHA256:6acc777971890cb1efaeeb33a0a5358651c71067ced69dcfd59da7d0977f7530
'http://archive.ubuntu.com/ubuntu/pool/main/b/binutils/binutils_2.42-4ubuntu2.10.dsc' binutils_2.42-4ubuntu2.10.dsc 10152 SHA256:a14a8e2efdb3566955476bccd2248cebed5cf2a2f5d28e223d08200ec1a18d75
```

### `dpkg` source package: `brotli=1.1.0-2build2`

Binary Packages:

- `libbrotli1:amd64=1.1.0-2build2`

Licenses: (parsed from: `/usr/share/doc/libbrotli1/copyright`)

- `MIT`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `build-essential=12.10ubuntu1`

Binary Packages:

- `build-essential=12.10ubuntu1`

Licenses: (parsed from: `/usr/share/doc/build-essential/copyright`)

- `GPL`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `bullet=3.24+dfsg-2.1build1`

Binary Packages:

- `libbullet-dev:amd64=3.24+dfsg-2.1build1`
- `libbullet3.24t64:amd64=3.24+dfsg-2.1build1`

Licenses: (parsed from: `/usr/share/doc/libbullet-dev/copyright`, `/usr/share/doc/libbullet3.24t64/copyright`)

- `Apache-2.0`
- `BSD-2-clause`
- `BSD-3-clause`
- `BSL-1.0`
- `Elsevier-CDROM-License`
- `Expat`
- `GNU-All-Permissive-License`
- `GPL-2`
- `GPL-2+`
- `Zlib`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `bzip2=1.0.8-5.1build0.1`

Binary Packages:

- `bzip2=1.0.8-5.1build0.1`
- `libbz2-1.0:amd64=1.0.8-5.1build0.1`

Licenses: (parsed from: `/usr/share/doc/bzip2/copyright`, `/usr/share/doc/libbz2-1.0/copyright`)

- `BSD-variant`
- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris bzip2=1.0.8-5.1build0.1
'http://archive.ubuntu.com/ubuntu/pool/main/b/bzip2/bzip2_1.0.8.orig.tar.gz' bzip2_1.0.8.orig.tar.gz 810029 SHA256:ab5a03176ee106d3f0fa90e381da478ddae405918153cca248e682cd0c4a2269
'http://archive.ubuntu.com/ubuntu/pool/main/b/bzip2/bzip2_1.0.8-5.1build0.1.debian.tar.bz2' bzip2_1.0.8-5.1build0.1.debian.tar.bz2 26927 SHA256:0ac0bd78fc0a7f6311a0bb62e81037ec920eb29e315261032ee84c4018e600f3
'http://archive.ubuntu.com/ubuntu/pool/main/b/bzip2/bzip2_1.0.8-5.1build0.1.dsc' bzip2_1.0.8-5.1build0.1.dsc 2220 SHA256:edf9f297ccfba3fc6f89d64fb6c63d866527498d21d0f0771a60f2fb7bc9b16a
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


### `dpkg` source package: `cairo=1.18.0-3build1`

Binary Packages:

- `libcairo2:amd64=1.18.0-3build1`

Licenses: (parsed from: `/usr/share/doc/libcairo2/copyright`)

- `LGPL-2.1`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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
'http://archive.ubuntu.com/ubuntu/pool/main/c/coreutils/coreutils_9.4.orig.tar.xz' coreutils_9.4.orig.tar.xz 5979200 SHA256:ea613a4cf44612326e917201bbbcdfbd301de21ffc3b59b6e5c07e040b275e52
'http://archive.ubuntu.com/ubuntu/pool/main/c/coreutils/coreutils_9.4-3ubuntu6.2.debian.tar.xz' coreutils_9.4-3ubuntu6.2.debian.tar.xz 42032 SHA256:6cd2ec4b6af4c52d5aa7bf6b5843bbb9b878be42d91b279de8b7afae843c8fa0
'http://archive.ubuntu.com/ubuntu/pool/main/c/coreutils/coreutils_9.4-3ubuntu6.2.dsc' coreutils_9.4-3ubuntu6.2.dsc 2030 SHA256:a16ffb435f38507bea51474f5e40a26e4c8191d2190da8770e8e4726c18e37ba
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
- `libcurl3t64-gnutls:amd64=8.5.0-2ubuntu10.8`
- `libcurl4t64:amd64=8.5.0-2ubuntu10.8`

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
'http://archive.ubuntu.com/ubuntu/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.28%2bdfsg1.orig.tar.xz' cyrus-sasl2_2.1.28+dfsg1.orig.tar.xz 794540 SHA256:e796a5d85d1a85e1b433d43504e467f9075c7ebc0b45730a3996cf11b1deada4
'http://archive.ubuntu.com/ubuntu/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.28%2bdfsg1-5ubuntu3.1.debian.tar.xz' cyrus-sasl2_2.1.28+dfsg1-5ubuntu3.1.debian.tar.xz 98324 SHA256:a1017cf9d4fd098325338d1d7f1f71cb87102934e7b35c8f5e726d246360689e
'http://archive.ubuntu.com/ubuntu/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.28%2bdfsg1-5ubuntu3.1.dsc' cyrus-sasl2_2.1.28+dfsg1-5ubuntu3.1.dsc 3501 SHA256:6ede2d7122c4ea1e807f45b647edbdf9fb1521ad09b0ca0b9b48f220ef33f23f
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


### `dpkg` source package: `dbus-python=1.3.2-5build3`

Binary Packages:

- `python3-dbus=1.3.2-5build3`

Licenses: (parsed from: `/usr/share/doc/python3-dbus/copyright`)

- `AFL-2.1`
- `AFL-2.1,`
- `Expat`
- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `dbus=1.14.10-4ubuntu4.1`

Binary Packages:

- `libdbus-1-3:amd64=1.14.10-4ubuntu4.1`

Licenses: (parsed from: `/usr/share/doc/libdbus-1-3/copyright`)

- `AFL-2.1`
- `AFL-2.1,`
- `BSD-3-clause`
- `BSD-3-clause-generic`
- `Expat`
- `FSF-unlimited-permission`
- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `Tcl-BSDish`
- `autoconf-archive-permissive`
- `g10-permissive`

Source:

```console
$ apt-get source -qq --print-uris dbus=1.14.10-4ubuntu4.1
'http://archive.ubuntu.com/ubuntu/pool/main/d/dbus/dbus_1.14.10.orig.tar.xz' dbus_1.14.10.orig.tar.xz 1372328 SHA256:ba1f21d2bd9d339da2d4aa8780c09df32fea87998b73da24f49ab9df1e36a50f
'http://archive.ubuntu.com/ubuntu/pool/main/d/dbus/dbus_1.14.10.orig.tar.xz.asc' dbus_1.14.10.orig.tar.xz.asc 833 SHA256:5f292cd0603c3d736026ed3f4d1c1937847981669c1f0a389083518f013e1081
'http://archive.ubuntu.com/ubuntu/pool/main/d/dbus/dbus_1.14.10-4ubuntu4.1.debian.tar.xz' dbus_1.14.10-4ubuntu4.1.debian.tar.xz 69668 SHA256:c28e0e4840bf3c3f3cbdacae9b7228bb4694dd234f325535942dde76af3c322e
'http://archive.ubuntu.com/ubuntu/pool/main/d/dbus/dbus_1.14.10-4ubuntu4.1.dsc' dbus_1.14.10-4ubuntu4.1.dsc 3746 SHA256:3d9037176550657a3584f7640027a6d970c85b0cd158a2be7e8051aab1349edb
```

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


### `dpkg` source package: `distlib=0.3.8-1`

Binary Packages:

- `python3-distlib=0.3.8-1`

Licenses: (parsed from: `/usr/share/doc/python3-distlib/copyright`)

- `BSD-3-clause`
- `Python`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/distlib/0.3.8-1/


### `dpkg` source package: `dpkg=1.22.6ubuntu6.5`

Binary Packages:

- `dpkg=1.22.6ubuntu6.5`
- `dpkg-dev=1.22.6ubuntu6.5`
- `libdpkg-perl=1.22.6ubuntu6.5`

Licenses: (parsed from: `/usr/share/doc/dpkg/copyright`, `/usr/share/doc/dpkg-dev/copyright`, `/usr/share/doc/libdpkg-perl/copyright`)

- `GPL-2`
- `GPL-2+`
- `public-domain-s-s-d`

Source:

```console
$ apt-get source -qq --print-uris dpkg=1.22.6ubuntu6.5
'http://archive.ubuntu.com/ubuntu/pool/main/d/dpkg/dpkg_1.22.6ubuntu6.5.tar.xz' dpkg_1.22.6ubuntu6.5.tar.xz 5547360 SHA256:a70af49fb54dff0a34cdb194b1aafb4c844c445ad3769dec30cb45939432a185
'http://archive.ubuntu.com/ubuntu/pool/main/d/dpkg/dpkg_1.22.6ubuntu6.5.dsc' dpkg_1.22.6ubuntu6.5.dsc 3156 SHA256:ea558d3274f841093bb59fd86492488341ead15fc5aa9600bb7961fd20816c7d
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
'http://archive.ubuntu.com/ubuntu/pool/main/e/e2fsprogs/e2fsprogs_1.47.0.orig.tar.gz' e2fsprogs_1.47.0.orig.tar.gz 9637717 SHA256:6667afde56eef0c6af26684974400e4d2288ea49e9441bf5e6229195d51a3578
'http://archive.ubuntu.com/ubuntu/pool/main/e/e2fsprogs/e2fsprogs_1.47.0.orig.tar.gz.asc' e2fsprogs_1.47.0.orig.tar.gz.asc 488 SHA256:704928204a52ddaa0ac8ef549c1bfba3c38e66c361d3853c8a4c38e6082b90f1
'http://archive.ubuntu.com/ubuntu/pool/main/e/e2fsprogs/e2fsprogs_1.47.0-2.4%7eexp1ubuntu4.1.debian.tar.xz' e2fsprogs_1.47.0-2.4~exp1ubuntu4.1.debian.tar.xz 90580 SHA256:26b381ec175ff52d1cc2fd1b217f84b9e1d7d33a58dcbaf8942115dd27a03f84
'http://archive.ubuntu.com/ubuntu/pool/main/e/e2fsprogs/e2fsprogs_1.47.0-2.4%7eexp1ubuntu4.1.dsc' e2fsprogs_1.47.0-2.4~exp1ubuntu4.1.dsc 3294 SHA256:215fe7b95c246894654c59a01514dfdc16ec17a0dcb09dc7a7c1ec1246ed4964
```

### `dpkg` source package: `eigen3=3.4.0-4build0.1`

Binary Packages:

- `libeigen3-dev=3.4.0-4build0.1`

Licenses: (parsed from: `/usr/share/doc/libeigen3-dev/copyright`)

- `BSD-3-clause`
- `LGPL-2.1`
- `LGPL-2.1+`
- `MPL-2`

Source:

```console
$ apt-get source -qq --print-uris eigen3=3.4.0-4build0.1
'http://archive.ubuntu.com/ubuntu/pool/universe/e/eigen3/eigen3_3.4.0.orig.tar.bz2' eigen3_3.4.0.orig.tar.bz2 2143091 SHA256:b4c198460eba6f28d34894e3a5710998818515104d6e74e5cc331ce31e46e626
'http://archive.ubuntu.com/ubuntu/pool/universe/e/eigen3/eigen3_3.4.0-4build0.1.debian.tar.xz' eigen3_3.4.0-4build0.1.debian.tar.xz 20600 SHA256:e0af8f536c9f6e2e5344219a0f56a5f456286f4e4ae2f68f8ecc14755c621b7a
'http://archive.ubuntu.com/ubuntu/pool/universe/e/eigen3/eigen3_3.4.0-4build0.1.dsc' eigen3_3.4.0-4build0.1.dsc 2202 SHA256:5ee1a1ea1c1afae4f28e12923b0cfe4023bc965fba28c6c1a47b9b152906b5c8
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
'http://archive.ubuntu.com/ubuntu/pool/main/e/expat/expat_2.6.1.orig.tar.gz' expat_2.6.1.orig.tar.gz 8414649 SHA256:14113ed69357172a0bf5a268793c8b5b01afc77c7a2e5fb8dd0b06cb87c02c4a
'http://archive.ubuntu.com/ubuntu/pool/main/e/expat/expat_2.6.1-2ubuntu0.4.debian.tar.xz' expat_2.6.1-2ubuntu0.4.debian.tar.xz 31092 SHA256:8a24bd6c87fe292a2f00a2df71f7d2bbe3713fa63b1952c8552cdac4288d10fd
'http://archive.ubuntu.com/ubuntu/pool/main/e/expat/expat_2.6.1-2ubuntu0.4.dsc' expat_2.6.1-2ubuntu0.4.dsc 1945 SHA256:a25d3fde103454ad5d34d4770bd5adb60bb5872da775df74cad193b5c4de1dff
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


### `dpkg` source package: `fontconfig=2.15.0-1.1ubuntu2`

Binary Packages:

- `fontconfig=2.15.0-1.1ubuntu2`
- `fontconfig-config=2.15.0-1.1ubuntu2`
- `libfontconfig1:amd64=2.15.0-1.1ubuntu2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `fonts-dejavu=2.37-8`

Binary Packages:

- `fonts-dejavu-core=2.37-8`
- `fonts-dejavu-mono=2.37-8`

Licenses: (parsed from: `/usr/share/doc/fonts-dejavu-core/copyright`, `/usr/share/doc/fonts-dejavu-mono/copyright`)

- `GPL-2`
- `GPL-2+`
- `bitstream-vera`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/fonts-dejavu/2.37-8/


### `dpkg` source package: `freetype=2.13.2+dfsg-1ubuntu0.1`

Binary Packages:

- `libfreetype6:amd64=2.13.2+dfsg-1ubuntu0.1`

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
$ apt-get source -qq --print-uris freetype=2.13.2+dfsg-1ubuntu0.1
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.13.2%2bdfsg.orig-ft2demos.tar.xz' freetype_2.13.2+dfsg.orig-ft2demos.tar.xz 341140 SHA256:99ee2ed8b98bcfad17bc57c2d9699d764f20fe29ad304c69b8eb28834ca3b48e
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.13.2%2bdfsg.orig-ft2demos.tar.xz.asc' freetype_2.13.2+dfsg.orig-ft2demos.tar.xz.asc 833 SHA256:e58ba462f7bdcdc5899f777d33453c1ce6f6e46b080047580f45c9fd9f2dc08c
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.13.2%2bdfsg.orig-ft2docs.tar.xz' freetype_2.13.2+dfsg.orig-ft2docs.tar.xz 2173920 SHA256:685c25e1035a5076e5097186b3143b9c06878f3f9087d0a81e4d8538d5d15424
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.13.2%2bdfsg.orig-ft2docs.tar.xz.asc' freetype_2.13.2+dfsg.orig-ft2docs.tar.xz.asc 833 SHA256:d7e17c8a3bce50181530ebe06346f506cbfc92ecc5ca7cc395c7dbb24a71a5c0
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.13.2%2bdfsg.orig.tar.xz' freetype_2.13.2+dfsg.orig.tar.xz 2220368 SHA256:48c78a4194adfcd15a4d089f3206dab8454c311f5577f3ef7eaef95f777f86e6
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.13.2%2bdfsg-1ubuntu0.1.debian.tar.xz' freetype_2.13.2+dfsg-1ubuntu0.1.debian.tar.xz 44692 SHA256:41371d9748c0e6f407c44c52c7fe5fbd4fbc2276a168ae528404731ae2e95b31
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.13.2%2bdfsg-1ubuntu0.1.dsc' freetype_2.13.2+dfsg-1ubuntu0.1.dsc 3606 SHA256:05368dead2fd8739fb2aa3a11e6ffd4376039b57536cc1c5cdadceb75496f385
```

### `dpkg` source package: `fribidi=1.0.13-3build1`

Binary Packages:

- `libfribidi0:amd64=1.0.13-3build1`

Licenses: (parsed from: `/usr/share/doc/libfribidi0/copyright`)

- `LGPL-2.1`
- `LGPL-2.1+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `gcc-13=13.3.0-6ubuntu2~24.04.1`

Binary Packages:

- `cpp-13=13.3.0-6ubuntu2~24.04.1`
- `cpp-13-x86-64-linux-gnu=13.3.0-6ubuntu2~24.04.1`
- `g++-13=13.3.0-6ubuntu2~24.04.1`
- `g++-13-x86-64-linux-gnu=13.3.0-6ubuntu2~24.04.1`
- `gcc-13=13.3.0-6ubuntu2~24.04.1`
- `gcc-13-base:amd64=13.3.0-6ubuntu2~24.04.1`
- `gcc-13-x86-64-linux-gnu=13.3.0-6ubuntu2~24.04.1`
- `libgcc-13-dev:amd64=13.3.0-6ubuntu2~24.04.1`
- `libstdc++-13-dev:amd64=13.3.0-6ubuntu2~24.04.1`

Licenses: (parsed from: `/usr/share/doc/cpp-13/copyright`, `/usr/share/doc/cpp-13-x86-64-linux-gnu/copyright`, `/usr/share/doc/g++-13/copyright`, `/usr/share/doc/g++-13-x86-64-linux-gnu/copyright`, `/usr/share/doc/gcc-13/copyright`, `/usr/share/doc/gcc-13-base/copyright`, `/usr/share/doc/gcc-13-x86-64-linux-gnu/copyright`, `/usr/share/doc/libgcc-13-dev/copyright`, `/usr/share/doc/libstdc++-13-dev/copyright`)

- `Artistic`
- `GFDL-1.2`
- `GPL`
- `GPL-2`
- `GPL-3`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris gcc-13=13.3.0-6ubuntu2~24.04.1
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-13/gcc-13_13.3.0.orig.tar.gz' gcc-13_13.3.0.orig.tar.gz 92761021 SHA256:3b85d91bf38d1b858d9d01134f4046b3359731968ed4e6e912d29717a35d1a46
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-13/gcc-13_13.3.0-6ubuntu2%7e24.04.1.debian.tar.xz' gcc-13_13.3.0-6ubuntu2~24.04.1.debian.tar.xz 646156 SHA256:5523658f272ad6d15a83b6e26d178fbd5cb7709ec7ce2ca52b0c843e19c228e3
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-13/gcc-13_13.3.0-6ubuntu2%7e24.04.1.dsc' gcc-13_13.3.0-6ubuntu2~24.04.1.dsc 39540 SHA256:86b4012c312ac13e3e092877719a62a5b5dbab082ae7e9680780a25c6a13ddc6
```

### `dpkg` source package: `gcc-14=14.2.0-4ubuntu2~24.04.1`

Binary Packages:

- `gcc-14-base:amd64=14.2.0-4ubuntu2~24.04.1`
- `libasan8:amd64=14.2.0-4ubuntu2~24.04.1`
- `libatomic1:amd64=14.2.0-4ubuntu2~24.04.1`
- `libcc1-0:amd64=14.2.0-4ubuntu2~24.04.1`
- `libgcc-s1:amd64=14.2.0-4ubuntu2~24.04.1`
- `libgfortran5:amd64=14.2.0-4ubuntu2~24.04.1`
- `libgomp1:amd64=14.2.0-4ubuntu2~24.04.1`
- `libhwasan0:amd64=14.2.0-4ubuntu2~24.04.1`
- `libitm1:amd64=14.2.0-4ubuntu2~24.04.1`
- `liblsan0:amd64=14.2.0-4ubuntu2~24.04.1`
- `libquadmath0:amd64=14.2.0-4ubuntu2~24.04.1`
- `libstdc++6:amd64=14.2.0-4ubuntu2~24.04.1`
- `libtsan2:amd64=14.2.0-4ubuntu2~24.04.1`
- `libubsan1:amd64=14.2.0-4ubuntu2~24.04.1`

Licenses: (parsed from: `/usr/share/doc/gcc-14-base/copyright`, `/usr/share/doc/libasan8/copyright`, `/usr/share/doc/libatomic1/copyright`, `/usr/share/doc/libcc1-0/copyright`, `/usr/share/doc/libgcc-s1/copyright`, `/usr/share/doc/libgfortran5/copyright`, `/usr/share/doc/libgomp1/copyright`, `/usr/share/doc/libhwasan0/copyright`, `/usr/share/doc/libitm1/copyright`, `/usr/share/doc/liblsan0/copyright`, `/usr/share/doc/libquadmath0/copyright`, `/usr/share/doc/libstdc++6/copyright`, `/usr/share/doc/libtsan2/copyright`, `/usr/share/doc/libubsan1/copyright`)

- `Artistic`
- `GFDL-1.2`
- `GPL`
- `GPL-3`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris gcc-14=14.2.0-4ubuntu2~24.04.1
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-14/gcc-14_14.2.0.orig.tar.gz' gcc-14_14.2.0.orig.tar.gz 97158172 SHA256:768c314c11eeab56ccebb91eb42ec4a41122fa94f0d83400126401942622197b
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-14/gcc-14_14.2.0-4ubuntu2%7e24.04.1.debian.tar.xz' gcc-14_14.2.0-4ubuntu2~24.04.1.debian.tar.xz 1950432 SHA256:cfece214c2fb790ef5f3baffb9a53e40618e7ae12d053610b251e94d77d08ade
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-14/gcc-14_14.2.0-4ubuntu2%7e24.04.1.dsc' gcc-14_14.2.0-4ubuntu2~24.04.1.dsc 46930 SHA256:50950080874a6ec6780dd60c243e21d9cda9d736bb32bca98d16095d27cc01b5
```

### `dpkg` source package: `gcc-defaults=1.214ubuntu1`

Binary Packages:

- `cpp=4:13.2.0-7ubuntu1`
- `cpp-x86-64-linux-gnu=4:13.2.0-7ubuntu1`
- `g++=4:13.2.0-7ubuntu1`
- `g++-x86-64-linux-gnu=4:13.2.0-7ubuntu1`
- `gcc=4:13.2.0-7ubuntu1`
- `gcc-x86-64-linux-gnu=4:13.2.0-7ubuntu1`

Licenses: (parsed from: `/usr/share/doc/cpp/copyright`, `/usr/share/doc/cpp-x86-64-linux-gnu/copyright`, `/usr/share/doc/g++/copyright`, `/usr/share/doc/g++-x86-64-linux-gnu/copyright`, `/usr/share/doc/gcc/copyright`, `/usr/share/doc/gcc-x86-64-linux-gnu/copyright`)

- `GPL-2`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `gdbm=1.23-5.1build1`

Binary Packages:

- `libgdbm-compat4t64:amd64=1.23-5.1build1`
- `libgdbm6t64:amd64=1.23-5.1build1`

Licenses: (parsed from: `/usr/share/doc/libgdbm-compat4t64/copyright`, `/usr/share/doc/libgdbm6t64/copyright`)

- `GFDL-NIV-1.3+`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `git=1:2.43.0-1ubuntu7.3`

Binary Packages:

- `git=1:2.43.0-1ubuntu7.3`
- `git-man=1:2.43.0-1ubuntu7.3`

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
$ apt-get source -qq --print-uris git=1:2.43.0-1ubuntu7.3
'http://archive.ubuntu.com/ubuntu/pool/main/g/git/git_2.43.0.orig.tar.xz' git_2.43.0.orig.tar.xz 7382996 SHA256:5446603e73d911781d259e565750dcd277a42836c8e392cac91cf137aa9b76ec
'http://archive.ubuntu.com/ubuntu/pool/main/g/git/git_2.43.0-1ubuntu7.3.debian.tar.xz' git_2.43.0-1ubuntu7.3.debian.tar.xz 795448 SHA256:5bb363b59fda93816ec9ef34476e720b4f66f4b9947866bfaf414964be7dd4a7
'http://archive.ubuntu.com/ubuntu/pool/main/g/git/git_2.43.0-1ubuntu7.3.dsc' git_2.43.0-1ubuntu7.3.dsc 2972 SHA256:1e3e5b83bf41318cc957a9e471ed82f8ca4d6befe91b008699959072c97430f4
```

### `dpkg` source package: `glib2.0=2.80.0-6ubuntu3.8`

Binary Packages:

- `libglib2.0-0t64:amd64=2.80.0-6ubuntu3.8`

Licenses: (parsed from: `/usr/share/doc/libglib2.0-0t64/copyright`)

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

Source:

```console
$ apt-get source -qq --print-uris glib2.0=2.80.0-6ubuntu3.8
'http://archive.ubuntu.com/ubuntu/pool/main/g/glib2.0/glib2.0_2.80.0.orig-unicode-data.tar.xz' glib2.0_2.80.0.orig-unicode-data.tar.xz 263364 SHA256:38680f78a0ae6258826418cb5096c19ae3566ba8fee0a2112a0ec40056e58729
'http://archive.ubuntu.com/ubuntu/pool/main/g/glib2.0/glib2.0_2.80.0.orig.tar.xz' glib2.0_2.80.0.orig.tar.xz 5510536 SHA256:8228a92f92a412160b139ae68b6345bd28f24434a7b5af150ebe21ff587a561d
'http://archive.ubuntu.com/ubuntu/pool/main/g/glib2.0/glib2.0_2.80.0-6ubuntu3.8.debian.tar.xz' glib2.0_2.80.0-6ubuntu3.8.debian.tar.xz 166540 SHA256:3ee18682434b0213fbc7f5892527f748810a657aba2353d660c5eb30ed1656f0
'http://archive.ubuntu.com/ubuntu/pool/main/g/glib2.0/glib2.0_2.80.0-6ubuntu3.8.dsc' glib2.0_2.80.0-6ubuntu3.8.dsc 4542 SHA256:d44112b09956f61ffd5790a1a40e42558dca287052a945078cffff9b2490ee84
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
'http://archive.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.39.orig.tar.xz' glibc_2.39.orig.tar.xz 18520988 SHA256:f77bd47cf8170c57365ae7bf86696c118adb3b120d3259c64c502d3dc1e2d926
'http://archive.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.39.orig.tar.xz.asc' glibc_2.39.orig.tar.xz.asc 833 SHA256:2cce427ef7933c17379f5514e4f0ccf8dffae5bf8c72f0f7e0bf8b8401f34be5
'http://archive.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.39-0ubuntu8.7.debian.tar.xz' glibc_2.39-0ubuntu8.7.debian.tar.xz 469880 SHA256:9642284fbb90ca3b56af777e3e5d6989bf3f80ba5d0c37c4ec0c94fb37912b70
'http://archive.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.39-0ubuntu8.7.dsc' glibc_2.39-0ubuntu8.7.dsc 9257 SHA256:1d210efa9b492a2c340c709714abced58ef843009009b1fe4d1282796e0719d9
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
'http://archive.ubuntu.com/ubuntu/pool/main/g/gmp/gmp_6.3.0%2bdfsg.orig.tar.xz' gmp_6.3.0+dfsg.orig.tar.xz 1870556 SHA256:bd2966e6d277f79328e894a5a9f3ba3fbf2ed2be81def5f48623e30c23fb1572
'http://archive.ubuntu.com/ubuntu/pool/main/g/gmp/gmp_6.3.0%2bdfsg-2ubuntu6.1.debian.tar.xz' gmp_6.3.0+dfsg-2ubuntu6.1.debian.tar.xz 38908 SHA256:0a7592ee94876fcc0dba60c9a9fba806a72752c104c04d553803e1b7a97026a3
'http://archive.ubuntu.com/ubuntu/pool/main/g/gmp/gmp_6.3.0%2bdfsg-2ubuntu6.1.dsc' gmp_6.3.0+dfsg-2ubuntu6.1.dsc 2345 SHA256:7fdd2464ee453296e33598dad6f84dd489640c08f50552389469bcf90537582e
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
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnupg2/gnupg2_2.4.4.orig.tar.bz2' gnupg2_2.4.4.orig.tar.bz2 7886036 SHA256:67ebe016ca90fa7688ce67a387ebd82c6261e95897db7b23df24ff335be85bc6
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnupg2/gnupg2_2.4.4.orig.tar.bz2.asc' gnupg2_2.4.4.orig.tar.bz2.asc 386 SHA256:47986167998b2cb6be4e4cdeef0c468139e06580ed65ce2cf241c527d74e54db
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnupg2/gnupg2_2.4.4-2ubuntu17.4.debian.tar.xz' gnupg2_2.4.4-2ubuntu17.4.debian.tar.xz 97376 SHA256:234250d6e9288ddb8e481f2da515ffa2bb384be0d9edd818487a82f15e8f307c
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnupg2/gnupg2_2.4.4-2ubuntu17.4.dsc' gnupg2_2.4.4-2ubuntu17.4.dsc 3984 SHA256:81a51e04b3b4ae3da32314cca791c9872cc8ca1600d859feb7c8d43536c05f54
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
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.8.3.orig.tar.xz' gnutls28_3.8.3.orig.tar.xz 6463720 SHA256:f74fc5954b27d4ec6dfbb11dea987888b5b124289a3703afcada0ee520f4173e
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.8.3.orig.tar.xz.asc' gnutls28_3.8.3.orig.tar.xz.asc 854 SHA256:b2b90d225728890b0e2aa7c05e5f25f8ba1282821b46e72cd99f0c732b639cef
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.8.3-1.1ubuntu3.5.debian.tar.xz' gnutls28_3.8.3-1.1ubuntu3.5.debian.tar.xz 109884 SHA256:d3ae87f0d815bed4f8f5547b8e38d97d8e875759d18ccc0cd65f1c97161d997d
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.8.3-1.1ubuntu3.5.dsc' gnutls28_3.8.3-1.1ubuntu3.5.dsc 3397 SHA256:6b041109100adb6b1a2acaa0bc5727b4fd2c95b980a885db5ae29c761c10cec4
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


### `dpkg` source package: `graphite2=1.3.14-2build1`

Binary Packages:

- `libgraphite2-3:amd64=1.3.14-2build1`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `graphviz=2.42.2-9ubuntu0.1`

Binary Packages:

- `graphviz=2.42.2-9ubuntu0.1`
- `libcdt5:amd64=2.42.2-9ubuntu0.1`
- `libcgraph6:amd64=2.42.2-9ubuntu0.1`
- `libgvc6=2.42.2-9ubuntu0.1`
- `libgvpr2:amd64=2.42.2-9ubuntu0.1`
- `liblab-gamut1:amd64=2.42.2-9ubuntu0.1`
- `libpathplan4:amd64=2.42.2-9ubuntu0.1`

Licenses: (parsed from: `/usr/share/doc/graphviz/copyright`, `/usr/share/doc/libcdt5/copyright`, `/usr/share/doc/libcgraph6/copyright`, `/usr/share/doc/libgvc6/copyright`, `/usr/share/doc/libgvpr2/copyright`, `/usr/share/doc/liblab-gamut1/copyright`, `/usr/share/doc/libpathplan4/copyright`)

- `EPL-1.0`
- `MIT`
- `X/MIT`
- `zlib-style`

Source:

```console
$ apt-get source -qq --print-uris graphviz=2.42.2-9ubuntu0.1
'http://archive.ubuntu.com/ubuntu/pool/universe/g/graphviz/graphviz_2.42.2.orig.tar.bz2' graphviz_2.42.2.orig.tar.bz2 30740923 SHA256:1daed697d9cdd7fac3b320336fa98dd3518dd211769301dc716869fc3d5409b1
'http://archive.ubuntu.com/ubuntu/pool/universe/g/graphviz/graphviz_2.42.2-9ubuntu0.1.debian.tar.xz' graphviz_2.42.2-9ubuntu0.1.debian.tar.xz 39936 SHA256:59515ec4d4ae8bfae21f40a05fd4d56fa2c96ebc149244465f50fc74cbcf2ec4
'http://archive.ubuntu.com/ubuntu/pool/universe/g/graphviz/graphviz_2.42.2-9ubuntu0.1.dsc' graphviz_2.42.2-9ubuntu0.1.dsc 3295 SHA256:178a4c1c789f63e588a26a8cf486dabab3ab0066a4e8da746a51e56b986b412d
```

### `dpkg` source package: `grep=3.11-4build1`

Binary Packages:

- `grep=3.11-4build1`

Licenses: (parsed from: `/usr/share/doc/grep/copyright`)

- `GPL-3`
- `GPL-3+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `gts=0.7.6+darcs121130-5.2build1`

Binary Packages:

- `libgts-0.7-5t64:amd64=0.7.6+darcs121130-5.2build1`

Licenses: (parsed from: `/usr/share/doc/libgts-0.7-5t64/copyright`)

- `LGPL-2`
- `LGPL-2+`

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
'http://archive.ubuntu.com/ubuntu/pool/main/g/gzip/gzip_1.12.orig.tar.xz' gzip_1.12.orig.tar.xz 825548 SHA256:ce5e03e519f637e1f814011ace35c4f87b33c0bbabeec35baf5fbd3479e91956
'http://archive.ubuntu.com/ubuntu/pool/main/g/gzip/gzip_1.12-1ubuntu3.1.debian.tar.xz' gzip_1.12-1ubuntu3.1.debian.tar.xz 21180 SHA256:1d0fe69725211bb5d9fc9287ec04493b964e6ff8d7f2d1ae8495d976d5cf9ee0
'http://archive.ubuntu.com/ubuntu/pool/main/g/gzip/gzip_1.12-1ubuntu3.1.dsc' gzip_1.12-1ubuntu3.1.dsc 2042 SHA256:62dd2256518d009efdb82d03e1f11ab4239d619bce546b210561abccc4d2a23d
```

### `dpkg` source package: `harfbuzz=8.3.0-2build2`

Binary Packages:

- `libharfbuzz0b:amd64=8.3.0-2build2`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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
'http://archive.ubuntu.com/ubuntu/pool/main/i/icu/icu_74.2.orig.tar.gz' icu_74.2.orig.tar.gz 26618071 SHA256:5e4fb11d6a3e6b85afb55de8da8a71538f1d8fd64fce893986b37d60e5bb0091
'http://archive.ubuntu.com/ubuntu/pool/main/i/icu/icu_74.2.orig.tar.gz.asc' icu_74.2.orig.tar.gz.asc 659 SHA256:1ca528b0017bae639fec7e89e3f988d0fa7def3e2436e5f7f5f9ec7dec2d9ece
'http://archive.ubuntu.com/ubuntu/pool/main/i/icu/icu_74.2-1ubuntu3.1.debian.tar.xz' icu_74.2-1ubuntu3.1.debian.tar.xz 64432 SHA256:45c74f50709547b0bfe3de020fd77be92c44d55e7020e718b0a47a0d0382f074
'http://archive.ubuntu.com/ubuntu/pool/main/i/icu/icu_74.2-1ubuntu3.1.dsc' icu_74.2-1ubuntu3.1.dsc 2350 SHA256:6cbf2e7018b5d16d634994e32af96f4d60f4468c36674c57f897b68812bbd883
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


### `dpkg` source package: `isl=0.26-3build1.1`

Binary Packages:

- `libisl23:amd64=0.26-3build1.1`

Licenses: (parsed from: `/usr/share/doc/libisl23/copyright`)

- `BSD-2-clause`
- `LGPL-2`
- `LGPL-2.1+`
- `MIT`

Source:

```console
$ apt-get source -qq --print-uris isl=0.26-3build1.1
'http://archive.ubuntu.com/ubuntu/pool/main/i/isl/isl_0.26.orig.tar.xz' isl_0.26.orig.tar.xz 2035560 SHA256:a0b5cb06d24f9fa9e77b55fabbe9a3c94a336190345c2555f9915bb38e976504
'http://archive.ubuntu.com/ubuntu/pool/main/i/isl/isl_0.26-3build1.1.debian.tar.xz' isl_0.26-3build1.1.debian.tar.xz 24948 SHA256:e05d478dbbdd772cc4cffba3428ac70788cab1fddaaba3e275917a92ef1f9e3a
'http://archive.ubuntu.com/ubuntu/pool/main/i/isl/isl_0.26-3build1.1.dsc' isl_0.26-3build1.1.dsc 1918 SHA256:8a552d2e58565e2c7186158d5c1c5a9e0417a9dde017bc37a23f06757c09d6a2
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

- `libjbig0:amd64=2.1-6.1ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libjbig0/copyright`)

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.20.1.orig.tar.gz' krb5_1.20.1.orig.tar.gz 8661660 SHA256:704aed49b19eb5a7178b34b2873620ec299db08752d6a8574f95d41879ab8851
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.20.1.orig.tar.gz.asc' krb5_1.20.1.orig.tar.gz.asc 833 SHA256:2afeec5dbc586cc40b7975645e02b4c41c4d719dd02213e828c72d8239d55666
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.20.1-6ubuntu2.6.debian.tar.xz' krb5_1.20.1-6ubuntu2.6.debian.tar.xz 122284 SHA256:58e9a5265de110bcebfaf1f88efc384673508302abed9ec189e2f8f9053abe70
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.20.1-6ubuntu2.6.dsc' krb5_1.20.1-6ubuntu2.6.dsc 4125 SHA256:52ce15dc89411879dc429344ae34ceec3f6301d425257b858804cf8baa8a4c13
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
'http://archive.ubuntu.com/ubuntu/pool/main/l/lapack/lapack_3.12.0.orig.tar.gz' lapack_3.12.0.orig.tar.gz 7933607 SHA256:eac9570f8e0ad6f30ce4b963f4f033f0f643e7c3912fc9ee6cd99120675ad48b
'http://archive.ubuntu.com/ubuntu/pool/main/l/lapack/lapack_3.12.0-3build1.1.debian.tar.xz' lapack_3.12.0-3build1.1.debian.tar.xz 28916 SHA256:e97519fe8f738e8040f2e5b35dded211f60923bbaba34f33387c2cdb0488c358
'http://archive.ubuntu.com/ubuntu/pool/main/l/lapack/lapack_3.12.0-3build1.1.dsc' lapack_3.12.0-3build1.1.dsc 3417 SHA256:f8a39e4b7c0174f1a7fc320e6ae3bd56ff038984c0d02a950f02436f1a222125
```

### `dpkg` source package: `lerc=4.0.0+ds-4ubuntu2`

Binary Packages:

- `liblerc4:amd64=4.0.0+ds-4ubuntu2`

Licenses: (parsed from: `/usr/share/doc/liblerc4/copyright`)

- `Apache-2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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
'http://archive.ubuntu.com/ubuntu/pool/main/liba/libarchive/libarchive_3.7.2.orig.tar.xz' libarchive_3.7.2.orig.tar.xz 5237056 SHA512:a21bebb27b808cb7d2ed13a70739904a1b7b55661d8dea83c9897a0129cf71e20c962f13666c571782ff0f4f753ca885619c2097d9e7691c2dee4e6e4b9a2971
'http://archive.ubuntu.com/ubuntu/pool/main/liba/libarchive/libarchive_3.7.2.orig.tar.xz.asc' libarchive_3.7.2.orig.tar.xz.asc 659 SHA512:c2ce850088245d7723720737d74d1cc1819984d01b3f9e4ed96b0757f4c6d6d511b78792181a12400c563632d74edcd0c2c3a4b7527cba40ada7ef74488078fc
'http://archive.ubuntu.com/ubuntu/pool/main/liba/libarchive/libarchive_3.7.2-2ubuntu0.6.debian.tar.xz' libarchive_3.7.2-2ubuntu0.6.debian.tar.xz 38028 SHA512:61ad04e7c320b27130bc8cbd930e43e6874028b13ae059e1580461a4e7f904d58c2d800221f57d81a2fe956579e87a9b3045f79bc4ab44eb944f440ece06283e
'http://archive.ubuntu.com/ubuntu/pool/main/liba/libarchive/libarchive_3.7.2-2ubuntu0.6.dsc' libarchive_3.7.2-2ubuntu0.6.dsc 2733 SHA512:1391a0262aace597c13c9ca49ab66bf962edc2a119a726271a9d11d3469cd664881b8e5e18ab3e0a0368f2b44e12ebc3a80a417530bf37ab86f142afb71b08cf
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


### `dpkg` source package: `libbsd=0.12.1-1build1.1`

Binary Packages:

- `libbsd0:amd64=0.12.1-1build1.1`

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
$ apt-get source -qq --print-uris libbsd=0.12.1-1build1.1
'http://archive.ubuntu.com/ubuntu/pool/main/libb/libbsd/libbsd_0.12.1.orig.tar.xz' libbsd_0.12.1.orig.tar.xz 444048 SHA256:d7747f8ec1baa6ff5c096a9dd587c061233dec90da0f1aedd66d830f6db6996a
'http://archive.ubuntu.com/ubuntu/pool/main/libb/libbsd/libbsd_0.12.1.orig.tar.xz.asc' libbsd_0.12.1.orig.tar.xz.asc 833 SHA256:04a4b66da93ea3c761e15fcedd705a969b67597d0619c3ebc5fe3cf72d477f1f
'http://archive.ubuntu.com/ubuntu/pool/main/libb/libbsd/libbsd_0.12.1-1build1.1.debian.tar.xz' libbsd_0.12.1-1build1.1.debian.tar.xz 18732 SHA256:4086dc52ae53f0d7625a593c331460377868edc2a5606f4d8a341565aa94b2be
'http://archive.ubuntu.com/ubuntu/pool/main/libb/libbsd/libbsd_0.12.1-1build1.1.dsc' libbsd_0.12.1-1build1.1.dsc 2458 SHA256:a44c2a70dbb9703c342ae49525507d22795b37308302c6167d72c3cbd3e76236
```

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libdatrie=0.2.13-3build1`

Binary Packages:

- `libdatrie1:amd64=0.2.13-3build1`

Licenses: (parsed from: `/usr/share/doc/libdatrie1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libde265=1.0.15-1build3`

Binary Packages:

- `libde265-0:amd64=1.0.15-1build3`

Licenses: (parsed from: `/usr/share/doc/libde265-0/copyright`)

- `BSD-4-clause`
- `GPL-3`
- `GPL-3+`
- `LGPL-3`
- `LGPL-3+`
- `other-1`
- `public-domain-1`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libdeflate=1.19-1build1.1`

Binary Packages:

- `libdeflate0:amd64=1.19-1build1.1`

Licenses: (parsed from: `/usr/share/doc/libdeflate0/copyright`)

- `Expat`

Source:

```console
$ apt-get source -qq --print-uris libdeflate=1.19-1build1.1
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libdeflate/libdeflate_1.19.orig.tar.gz' libdeflate_1.19.orig.tar.gz 187684 SHA256:27bf62d71cd64728ff43a9feb92f2ac2f2bf748986d856133cc1e51992428c25
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libdeflate/libdeflate_1.19-1build1.1.debian.tar.xz' libdeflate_1.19-1build1.1.debian.tar.xz 5004 SHA256:58f866e842d3d8cf6735e6a2cf7be887c712f8c07f8352a94e2fc4fed9d008bf
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libdeflate/libdeflate_1.19-1build1.1.dsc' libdeflate_1.19-1build1.1.dsc 2306 SHA256:3a2552cdace2cae2b98b81b64d225f4247bc2ed4409dc0ff9eff1db9843d79d0
```

### `dpkg` source package: `liberror-perl=0.17029-2`

Binary Packages:

- `liberror-perl=0.17029-2`

Licenses: (parsed from: `/usr/share/doc/liberror-perl/copyright`)

- `Artistic`
- `GPL-1`
- `GPL-1+`
- `MIT/X11`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/liberror-perl/0.17029-2/


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


### `dpkg` source package: `libgd2=2.3.3-9ubuntu5`

Binary Packages:

- `libgd3:amd64=2.3.3-9ubuntu5`

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
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgpg-error/libgpg-error_1.47.orig.tar.bz2' libgpg-error_1.47.orig.tar.bz2 1020862 SHA256:9e3c670966b96ecc746c28c2c419541e3bcb787d1a73930f5e5f5e1bcbbb9bdb
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgpg-error/libgpg-error_1.47.orig.tar.bz2.asc' libgpg-error_1.47.orig.tar.bz2.asc 228 SHA256:6ab547bf020761e1df80b08335773a91c345ff2c1344f15b1f7d195293ab21a5
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgpg-error/libgpg-error_1.47-3build2.1.debian.tar.xz' libgpg-error_1.47-3build2.1.debian.tar.xz 18776 SHA256:f02a079a6ddf9930659c3402820b6bd190687e8f1c223f340c965a9da74abcd5
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgpg-error/libgpg-error_1.47-3build2.1.dsc' libgpg-error_1.47-3build2.1.dsc 3007 SHA256:3c8abf463c9ade945fe2e9d87c4aa2bff0026964207b07e99432d9ef6d9436d8
```

### `dpkg` source package: `libheif=1.17.6-1ubuntu4.2`

Binary Packages:

- `libheif-plugin-aomdec:amd64=1.17.6-1ubuntu4.2`
- `libheif-plugin-libde265:amd64=1.17.6-1ubuntu4.2`
- `libheif1:amd64=1.17.6-1ubuntu4.2`

Licenses: (parsed from: `/usr/share/doc/libheif-plugin-aomdec/copyright`, `/usr/share/doc/libheif-plugin-libde265/copyright`, `/usr/share/doc/libheif1/copyright`)

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
$ apt-get source -qq --print-uris libheif=1.17.6-1ubuntu4.2
'http://archive.ubuntu.com/ubuntu/pool/main/libh/libheif/libheif_1.17.6.orig.tar.gz' libheif_1.17.6.orig.tar.gz 1433302 SHA256:8390baf4913eda0a183e132cec62b875fb2ef507ced5ddddc98dfd2f17780aee
'http://archive.ubuntu.com/ubuntu/pool/main/libh/libheif/libheif_1.17.6-1ubuntu4.2.debian.tar.xz' libheif_1.17.6-1ubuntu4.2.debian.tar.xz 12620 SHA256:84834591ea45e4910984b90c7ff4aabef76d2df0f209b1a2bd93f96bdf227444
'http://archive.ubuntu.com/ubuntu/pool/main/libh/libheif/libheif_1.17.6-1ubuntu4.2.dsc' libheif_1.17.6-1ubuntu4.2.dsc 3350 SHA256:874e1a1ccd3b5662e2d03a44ed6db48fdfc87b9d09312ab0e50a1ae8878b7af8
```

### `dpkg` source package: `libice=2:1.0.10-1build3`

Binary Packages:

- `libice6:amd64=2:1.0.10-1build3`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libidn2/libidn2_2.3.7.orig.tar.gz' libidn2_2.3.7.orig.tar.gz 2155214 SHA256:4c21a791b610b9519b9d0e12b8097bf2f359b12f8dd92647611a929e6bfd7d64
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libidn2/libidn2_2.3.7.orig.tar.gz.asc' libidn2_2.3.7.orig.tar.gz.asc 228 SHA256:d4e78fc1c5a5c35980be3a04dd864574f450d55921360b0aa19326c75ada4a98
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libidn2/libidn2_2.3.7-2build1.1.debian.tar.xz' libidn2_2.3.7-2build1.1.debian.tar.xz 16468 SHA256:50d3154a3a5b3506aa340c1784f96bfe0f4c5608e2a1a9dd265aa204da4ef327
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libidn2/libidn2_2.3.7-2build1.1.dsc' libidn2_2.3.7-2build1.1.dsc 2651 SHA256:fa2970145d391578511ef78bc74a9ba7a57cff510d9e5fba39520f63b023986c
```

### `dpkg` source package: `libjpeg-turbo=2.1.5-2ubuntu2`

Binary Packages:

- `libjpeg-turbo8:amd64=2.1.5-2ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libjpeg-turbo8/copyright`)

- `BSD-3-clause`
- `BSD-BY-LC-NE`
- `Expat`
- `NTP`
- `Zlib`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libjpeg8-empty=8c-2ubuntu11`

Binary Packages:

- `libjpeg8:amd64=8c-2ubuntu11`

Licenses: (parsed from: `/usr/share/doc/libjpeg8/copyright`)

- `LGPL-2.1`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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
'http://archive.ubuntu.com/ubuntu/pool/main/libm/libmd/libmd_1.1.0.orig.tar.xz' libmd_1.1.0.orig.tar.xz 271228 SHA256:1bd6aa42275313af3141c7cf2e5b964e8b1fd488025caf2f971f43b00776b332
'http://archive.ubuntu.com/ubuntu/pool/main/libm/libmd/libmd_1.1.0.orig.tar.xz.asc' libmd_1.1.0.orig.tar.xz.asc 833 SHA256:402fd3024e43ab975733d09e661804a58ca58697194e4b15216b1217cfe1dadb
'http://archive.ubuntu.com/ubuntu/pool/main/libm/libmd/libmd_1.1.0-2build1.1.debian.tar.xz' libmd_1.1.0-2build1.1.debian.tar.xz 8448 SHA256:ed337af7e336b7dbb6b246c339baa34c9e832bf614a44d06158238259df12307
'http://archive.ubuntu.com/ubuntu/pool/main/libm/libmd/libmd_1.1.0-2build1.1.dsc' libmd_1.1.0-2build1.1.dsc 2391 SHA256:11dfd22bba97a4c4ca6c09f34743ac6c72a34eb81344e3a1681c45e2d60ce239
```

### `dpkg` source package: `libpng1.6=1.6.43-5ubuntu0.5`

Binary Packages:

- `libpng16-16t64:amd64=1.6.43-5ubuntu0.5`

Licenses: (parsed from: `/usr/share/doc/libpng16-16t64/copyright`)

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
$ apt-get source -qq --print-uris libpng1.6=1.6.43-5ubuntu0.5
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpng1.6/libpng1.6_1.6.43.orig.tar.gz' libpng1.6_1.6.43.orig.tar.gz 1554715 SHA256:fecc95b46cf05e8e3fc8a414750e0ba5aad00d89e9fdf175e94ff041caf1a03a
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpng1.6/libpng1.6_1.6.43-5ubuntu0.5.debian.tar.xz' libpng1.6_1.6.43-5ubuntu0.5.debian.tar.xz 40772 SHA256:515c41c24126e5267743587b45a07899b319e471b38ecff1a797979d5842c7a4
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpng1.6/libpng1.6_1.6.43-5ubuntu0.5.dsc' libpng1.6_1.6.43-5ubuntu0.5.dsc 2384 SHA256:04ccb4e03446287f69952983bae24cc74d379bcf9cfcc543a6255622cc53d292
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
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libseccomp/libseccomp_2.5.5.orig.tar.gz' libseccomp_2.5.5.orig.tar.gz 642445 SHA256:248a2c8a4d9b9858aa6baf52712c34afefcf9c9e94b76dce02c1c9aa25fb3375
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libseccomp/libseccomp_2.5.5.orig.tar.gz.asc' libseccomp_2.5.5.orig.tar.gz.asc 833 SHA256:f3bf8a946020d3047581f11fe6ac71971a842115ddb362562b193861ef57d97b
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libseccomp/libseccomp_2.5.5-1ubuntu3.1.debian.tar.xz' libseccomp_2.5.5-1ubuntu3.1.debian.tar.xz 24484 SHA256:ee1e79bc46f18a992ac80f349fdd5cfa0b5f2f6b298473b587c7cf5af89a8df6
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libseccomp/libseccomp_2.5.5-1ubuntu3.1.dsc' libseccomp_2.5.5-1ubuntu3.1.dsc 2838 SHA256:8039579c8cd02819d8246b40483d69e2113979b5acc5900d7206e0b4bebff392
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
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libselinux/libselinux_3.5.orig.tar.gz' libselinux_3.5.orig.tar.gz 211453 SHA256:9a3a3705ac13a2ccca2de6d652b6356fead10f36fb33115c185c5ccdf29eec19
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libselinux/libselinux_3.5.orig.tar.gz.asc' libselinux_3.5.orig.tar.gz.asc 981 SHA256:fd37d441e0c08cabe9ac8f7815f52355bab2011549ec5792424fe18be9e1e015
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libselinux/libselinux_3.5-2ubuntu2.1.debian.tar.xz' libselinux_3.5-2ubuntu2.1.debian.tar.xz 38112 SHA256:13e47e0983f59235e34f5abe07a2a0d1af3dd2d255962c6a50fac4698c3fe891
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libselinux/libselinux_3.5-2ubuntu2.1.dsc' libselinux_3.5-2ubuntu2.1.dsc 3098 SHA256:96134581a745ed85b3d5f1c24cdd88fa7d3e29548c0f80a683094ed886b7f150
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


### `dpkg` source package: `libsm=2:1.2.3-1build3`

Binary Packages:

- `libsm6:amd64=2:1.2.3-1build3`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


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
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libssh/libssh_0.10.6.orig.tar.xz' libssh_0.10.6.orig.tar.xz 561036 SHA256:1861d498f5b6f1741b6abc73e608478491edcf9c9d4b6630eef6e74596de9dc1
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libssh/libssh_0.10.6.orig.tar.xz.asc' libssh_0.10.6.orig.tar.xz.asc 833 SHA256:140420406d7796548b0beaf736e73864c32291787cf2bd3983fdbc41741494ae
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libssh/libssh_0.10.6-2ubuntu0.4.debian.tar.xz' libssh_0.10.6-2ubuntu0.4.debian.tar.xz 56400 SHA256:13cb7f1a5b294bf5b0a9970acf22a7ccdfca5be546495b930960f0508725e4b9
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libssh/libssh_0.10.6-2ubuntu0.4.dsc' libssh_0.10.6-2ubuntu0.4.dsc 2723 SHA256:dec8669834a233aa336e7607395dbd8c5946f1f83cb6792772bf0c2e09825f7b
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
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtasn1-6/libtasn1-6_4.19.0.orig.tar.gz' libtasn1-6_4.19.0.orig.tar.gz 1786576 SHA256:1613f0ac1cf484d6ec0ce3b8c06d56263cc7242f1c23b30d82d23de345a63f7a
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtasn1-6/libtasn1-6_4.19.0.orig.tar.gz.asc' libtasn1-6_4.19.0.orig.tar.gz.asc 228 SHA256:8410c0c004f3509c218a98b276b3308b9c46f48068e8b1a6d9ebfd61ea9f357a
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtasn1-6/libtasn1-6_4.19.0-3ubuntu0.24.04.2.debian.tar.xz' libtasn1-6_4.19.0-3ubuntu0.24.04.2.debian.tar.xz 25112 SHA256:23e6e79b1be16c247e0d3b152a5838d5d182a788ba053c640b2a120b8b00adad
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtasn1-6/libtasn1-6_4.19.0-3ubuntu0.24.04.2.dsc' libtasn1-6_4.19.0-3ubuntu0.24.04.2.dsc 2801 SHA256:a322b48ad14f13ef24ccebcc1feab975817c67000382096146a281d0b4354e7e
```

### `dpkg` source package: `libthai=0.1.29-2build1`

Binary Packages:

- `libthai-data=0.1.29-2build1`
- `libthai0:amd64=0.1.29-2build1`

Licenses: (parsed from: `/usr/share/doc/libthai-data/copyright`, `/usr/share/doc/libthai0/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libtool=2.4.7-7build1`

Binary Packages:

- `libltdl7:amd64=2.4.7-7build1`

Licenses: (parsed from: `/usr/share/doc/libltdl7/copyright`)

- `GFDL-1.3`
- `GFDL-NIV-1.3+`
- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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
'http://archive.ubuntu.com/ubuntu/pool/main/libu/libunistring/libunistring_1.1.orig.tar.xz' libunistring_1.1.orig.tar.xz 2397676 SHA256:827c1eb9cb6e7c738b171745dac0888aa58c5924df2e59239318383de0729b98
'http://archive.ubuntu.com/ubuntu/pool/main/libu/libunistring/libunistring_1.1.orig.tar.xz.asc' libunistring_1.1.orig.tar.xz.asc 833 SHA256:dadae6c38f85f9e8776231436c601c386924ceb44d511456c61c9be73608933d
'http://archive.ubuntu.com/ubuntu/pool/main/libu/libunistring/libunistring_1.1-2build1.1.debian.tar.xz' libunistring_1.1-2build1.1.debian.tar.xz 14188 SHA256:06254c8f2ad989bd8ff267fd921d6711fbc0390ff10b99bc3be09fe870baab5e
'http://archive.ubuntu.com/ubuntu/pool/main/libu/libunistring/libunistring_1.1-2build1.1.dsc' libunistring_1.1-2build1.1.dsc 2292 SHA256:496ec65625b57a9c5cd0577843814cbd4701ab123a6146a56053dcc9463ae09e
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


### `dpkg` source package: `libwebp=1.3.2-0.4build3`

Binary Packages:

- `libsharpyuv0:amd64=1.3.2-0.4build3`
- `libwebp7:amd64=1.3.2-0.4build3`

Licenses: (parsed from: `/usr/share/doc/libsharpyuv0/copyright`, `/usr/share/doc/libwebp7/copyright`)

- `Apache-2.0`
- `BSD-3-Clause`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libx11=2:1.8.7-1build1`

Binary Packages:

- `libx11-6:amd64=2:1.8.7-1build1`
- `libx11-data=2:1.8.7-1build1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libxau=1:1.0.9-1build6`

Binary Packages:

- `libxau6:amd64=1:1.0.9-1build6`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libxaw=2:1.0.14-1build2`

Binary Packages:

- `libxaw7:amd64=2:1.0.14-1build2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libxcb=1.15-1ubuntu2`

Binary Packages:

- `libxcb-render0:amd64=1.15-1ubuntu2`
- `libxcb-shm0:amd64=1.15-1ubuntu2`
- `libxcb1:amd64=1.15-1ubuntu2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


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


### `dpkg` source package: `libxdmcp=1:1.1.3-0ubuntu6`

Binary Packages:

- `libxdmcp6:amd64=1:1.1.3-0ubuntu6`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libxext=2:1.3.4-1build2`

Binary Packages:

- `libxext6:amd64=2:1.3.4-1build2`

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
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxml2/libxml2_2.9.14%2bdfsg.orig.tar.xz' libxml2_2.9.14+dfsg.orig.tar.xz 2351200 SHA256:4fe913dec8b1ab89d13b489b419a8203176ea39e931eaa0d25b17eafb9c279e9
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxml2/libxml2_2.9.14%2bdfsg-1.3ubuntu3.7.debian.tar.xz' libxml2_2.9.14+dfsg-1.3ubuntu3.7.debian.tar.xz 52444 SHA256:84f32df78b0f40bfa4fd9fbb9aeb4bc034828b4fea4cfa30b3824a8f05a70d20
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxml2/libxml2_2.9.14%2bdfsg-1.3ubuntu3.7.dsc' libxml2_2.9.14+dfsg-1.3ubuntu3.7.dsc 3083 SHA256:033de6bba6af3395efb09d5e5b68a82ea8662740f50b49bddec5695cc6d5c3b0
```

### `dpkg` source package: `libxmu=2:1.1.3-3build2`

Binary Packages:

- `libxmu6:amd64=2:1.1.3-3build2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libxpm=1:3.5.17-1build2`

Binary Packages:

- `libxpm4:amd64=1:3.5.17-1build2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libxrender=1:0.9.10-1.1build1`

Binary Packages:

- `libxrender1:amd64=1:0.9.10-1.1build1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libxslt=1.1.39-0exp1ubuntu0.24.04.3`

Binary Packages:

- `libxslt1.1:amd64=1.1.39-0exp1ubuntu0.24.04.3`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxslt=1.1.39-0exp1ubuntu0.24.04.3
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxslt/libxslt_1.1.39.orig.tar.xz' libxslt_1.1.39.orig.tar.xz 1578216 SHA256:2a20ad621148339b0759c4d4e96719362dee64c9a096dbba625ba053846349f0
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxslt/libxslt_1.1.39-0exp1ubuntu0.24.04.3.debian.tar.xz' libxslt_1.1.39-0exp1ubuntu0.24.04.3.debian.tar.xz 24380 SHA256:f235c6088b4c5ec813caba9273b4a670935e4faa11768fa33f993455460ebf00
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxslt/libxslt_1.1.39-0exp1ubuntu0.24.04.3.dsc' libxslt_1.1.39-0exp1ubuntu0.24.04.3.dsc 2352 SHA256:25e60a82ccec471407248c0725eb51e85464b6e87fa032bca685c55d42ab8722
```

### `dpkg` source package: `libxt=1:1.2.1-1.2build1`

Binary Packages:

- `libxt6t64:amd64=1:1.2.1-1.2build1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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

- `libzstd-dev:amd64=1.5.5+dfsg2-2build1.1`
- `libzstd1:amd64=1.5.5+dfsg2-2build1.1`

Licenses: (parsed from: `/usr/share/doc/libzstd-dev/copyright`, `/usr/share/doc/libzstd1/copyright`)

- `BSD-3-clause`
- `Expat`
- `GPL-2`
- `zlib`

Source:

```console
$ apt-get source -qq --print-uris libzstd=1.5.5+dfsg2-2build1.1
'http://archive.ubuntu.com/ubuntu/pool/main/libz/libzstd/libzstd_1.5.5%2bdfsg2.orig.tar.xz' libzstd_1.5.5+dfsg2.orig.tar.xz 1784164 SHA256:d7cf3c10d416fd999cb8fcf7685d9268ba7bec8eb78121fc2d0d916fa393d22b
'http://archive.ubuntu.com/ubuntu/pool/main/libz/libzstd/libzstd_1.5.5%2bdfsg2-2build1.1.debian.tar.xz' libzstd_1.5.5+dfsg2-2build1.1.debian.tar.xz 21288 SHA256:c1df6d2628b26d085259b8e7ac020eb060e4c1feca98d6103058eda5ded725bc
'http://archive.ubuntu.com/ubuntu/pool/main/libz/libzstd/libzstd_1.5.5%2bdfsg2-2build1.1.dsc' libzstd_1.5.5+dfsg2-2build1.1.dsc 2485 SHA256:c190a5dff9e7c5b5b1399f0d701bb2c173bc7cbdf14d5e05970f5ac066c25570
```

### `dpkg` source package: `linux=6.8.0-110.110`

Binary Packages:

- `linux-libc-dev:amd64=6.8.0-110.110`

Licenses: (parsed from: `/usr/share/doc/linux-libc-dev/copyright`)

- `GPL-2`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `lsb-release-minimal=12.0-2`

Binary Packages:

- `lsb-release=12.0-2`

Licenses: (parsed from: `/usr/share/doc/lsb-release/copyright`)

- `ISC`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/lsb-release-minimal/12.0-2/


### `dpkg` source package: `lto-disabled-list=47`

Binary Packages:

- `lto-disabled-list=47`

Licenses: (parsed from: `/usr/share/doc/lto-disabled-list/copyright`)

- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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
- `liblz4-dev:amd64=1.9.4-1build1.1`

Licenses: (parsed from: `/usr/share/doc/liblz4-1/copyright`, `/usr/share/doc/liblz4-dev/copyright`)

- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris lz4=1.9.4-1build1.1
'http://archive.ubuntu.com/ubuntu/pool/main/l/lz4/lz4_1.9.4.orig.tar.gz' lz4_1.9.4.orig.tar.gz 354063 SHA256:0b0e3aa07c8c063ddf40b082bdf7e37a1562bda40a0ff5272957f3e987e0e54b
'http://archive.ubuntu.com/ubuntu/pool/main/l/lz4/lz4_1.9.4-1build1.1.debian.tar.xz' lz4_1.9.4-1build1.1.debian.tar.xz 8356 SHA256:9551b039576db7c87f38c3c847283877de65114cca06488accb9596a7c4f1ead
'http://archive.ubuntu.com/ubuntu/pool/main/l/lz4/lz4_1.9.4-1build1.1.dsc' lz4_1.9.4-1build1.1.dsc 2061 SHA256:ba7b585b15d8b4c955dd68c7af5aa89901cfbb3fdb4f2607ccad51628857d669
```

### `dpkg` source package: `make-dfsg=4.3-4.1build2`

Binary Packages:

- `make=4.3-4.1build2`

Licenses: (parsed from: `/usr/share/doc/make/copyright`)

- `GPL-3`
- `GPL-3+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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


### `dpkg` source package: `mpclib3=1.3.1-1build1.1`

Binary Packages:

- `libmpc3:amd64=1.3.1-1build1.1`

Licenses: (parsed from: `/usr/share/doc/libmpc3/copyright`)

- `LGPL-3`

Source:

```console
$ apt-get source -qq --print-uris mpclib3=1.3.1-1build1.1
'http://archive.ubuntu.com/ubuntu/pool/main/m/mpclib3/mpclib3_1.3.1.orig.tar.gz' mpclib3_1.3.1.orig.tar.gz 773573 SHA256:ab642492f5cf882b74aa0cb730cd410a81edcdbec895183ce930e706c1c759b8
'http://archive.ubuntu.com/ubuntu/pool/main/m/mpclib3/mpclib3_1.3.1-1build1.1.debian.tar.xz' mpclib3_1.3.1-1build1.1.debian.tar.xz 4844 SHA256:1a5294ea4ffb07338252041b22038be6bcc0fce3622a7dcfd7521a4529796090
'http://archive.ubuntu.com/ubuntu/pool/main/m/mpclib3/mpclib3_1.3.1-1build1.1.dsc' mpclib3_1.3.1-1build1.1.dsc 1963 SHA256:3025acde5f262fde13b7678cf7d5a3f2216a7d62cad764879a0764654ab91c05
```

### `dpkg` source package: `mpfr4=4.2.1-1build1.1`

Binary Packages:

- `libmpfr6:amd64=4.2.1-1build1.1`

Licenses: (parsed from: `/usr/share/doc/libmpfr6/copyright`)

- `GFDL-1.2`
- `LGPL-3`

Source:

```console
$ apt-get source -qq --print-uris mpfr4=4.2.1-1build1.1
'http://archive.ubuntu.com/ubuntu/pool/main/m/mpfr4/mpfr4_4.2.1.orig.tar.xz' mpfr4_4.2.1.orig.tar.xz 1493608 SHA256:277807353a6726978996945af13e52829e3abd7a9a5b7fb2793894e18f1fcbb2
'http://archive.ubuntu.com/ubuntu/pool/main/m/mpfr4/mpfr4_4.2.1-1build1.1.debian.tar.xz' mpfr4_4.2.1-1build1.1.debian.tar.xz 12760 SHA256:55770c471715c710690129e45c627d77da05547a8f6faee81dd420a9b2b5fded
'http://archive.ubuntu.com/ubuntu/pool/main/m/mpfr4/mpfr4_4.2.1-1build1.1.dsc' mpfr4_4.2.1-1build1.1.dsc 2045 SHA256:9adabba2fbe45f0705b630b9b225752d945718ed4742b1c5b9fb1aa0fbcd0766
```

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
'http://archive.ubuntu.com/ubuntu/pool/main/n/nettle/nettle_3.9.1.orig.tar.gz' nettle_3.9.1.orig.tar.gz 2396741 SHA256:ccfeff981b0ca71bbd6fbcb054f407c60ffb644389a5be80d6716d5b550c6ce3
'http://archive.ubuntu.com/ubuntu/pool/main/n/nettle/nettle_3.9.1.orig.tar.gz.asc' nettle_3.9.1.orig.tar.gz.asc 573 SHA256:9746017a1a7fe60aad4b929ea592bc6ac51e12ea7179f289944eb44828d958af
'http://archive.ubuntu.com/ubuntu/pool/main/n/nettle/nettle_3.9.1-2.2build1.1.debian.tar.xz' nettle_3.9.1-2.2build1.1.debian.tar.xz 24848 SHA256:be4ad3b97b32c4c4bacc10aa4caef2f3fa0840c21c642407fc3d48c4535b7c5e
'http://archive.ubuntu.com/ubuntu/pool/main/n/nettle/nettle_3.9.1-2.2build1.1.dsc' nettle_3.9.1-2.2build1.1.dsc 2325 SHA256:db439554d51174b657660a2a47d3d4128838e063f3c9c7da67bb3fe91931d1d2
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
'http://archive.ubuntu.com/ubuntu/pool/main/n/nghttp2/nghttp2_1.59.0.orig.tar.gz' nghttp2_1.59.0.orig.tar.gz 1055492 SHA256:0dd5c980f1262ff5f03676fd99f46f250b66c842f7d864fa1ca9f8453e5f8868
'http://archive.ubuntu.com/ubuntu/pool/main/n/nghttp2/nghttp2_1.59.0-1ubuntu0.2.debian.tar.xz' nghttp2_1.59.0-1ubuntu0.2.debian.tar.xz 14204 SHA256:20392558c0dbdfa6d60efe56e6c3c958bffe1d52bc7569c7ac1be43f729e38ca
'http://archive.ubuntu.com/ubuntu/pool/main/n/nghttp2/nghttp2_1.59.0-1ubuntu0.2.dsc' nghttp2_1.59.0-1ubuntu0.2.dsc 2624 SHA256:64378996facf9ded9c4088ee54254048cba5b3c191f177867363652e8bb0b6d9
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
'http://archive.ubuntu.com/ubuntu/pool/main/n/numactl/numactl_2.0.18.orig.tar.gz' numactl_2.0.18.orig.tar.gz 218289 SHA256:8cd6c13f3096e9c2293c1d732f56e2aa37a7ada1a98deed3fac7bd6da1aaaaf6
'http://archive.ubuntu.com/ubuntu/pool/main/n/numactl/numactl_2.0.18-1ubuntu0.24.04.1.debian.tar.xz' numactl_2.0.18-1ubuntu0.24.04.1.debian.tar.xz 7936 SHA256:4f4c6d80e15af0eba522e6d777d372b74be223405fb3100bff14baaa42578296
'http://archive.ubuntu.com/ubuntu/pool/main/n/numactl/numactl_2.0.18-1ubuntu0.24.04.1.dsc' numactl_2.0.18-1ubuntu0.24.04.1.dsc 2144 SHA256:fde5318bd6384807136bcb1abd118cc1001954becd99b63717d3dae7a7f88b00
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
'http://archive.ubuntu.com/ubuntu/pool/main/o/openldap/openldap_2.6.10%2bdfsg.orig.tar.xz' openldap_2.6.10+dfsg.orig.tar.xz 3754560 SHA256:e871102bda1e42155fd4d6be4825a297e1c593cb0907b84fc7dde888dc847877
'http://archive.ubuntu.com/ubuntu/pool/main/o/openldap/openldap_2.6.10%2bdfsg-0ubuntu0.24.04.1.debian.tar.xz' openldap_2.6.10+dfsg-0ubuntu0.24.04.1.debian.tar.xz 191132 SHA256:91bdd643954645ce8ba51152516831ce4dcb497a222b88a5df847c4780e5f79e
'http://archive.ubuntu.com/ubuntu/pool/main/o/openldap/openldap_2.6.10%2bdfsg-0ubuntu0.24.04.1.dsc' openldap_2.6.10+dfsg-0ubuntu0.24.04.1.dsc 3653 SHA256:63be3643ff4157d84ef8bd9763fb7252695ceaea46773277600377417ecd21de
```

### `dpkg` source package: `openssl=3.0.13-0ubuntu3.9`

Binary Packages:

- `libssl-dev:amd64=3.0.13-0ubuntu3.9`
- `libssl3t64:amd64=3.0.13-0ubuntu3.9`
- `openssl=3.0.13-0ubuntu3.9`

Licenses: (parsed from: `/usr/share/doc/libssl3t64/copyright`)

- `Apache-2.0`
- `Artistic`
- `GPL-1`
- `GPL-1+`

Source:

```console
$ apt-get source -qq --print-uris openssl=3.0.13-0ubuntu3.9
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssl/openssl_3.0.13.orig.tar.gz' openssl_3.0.13.orig.tar.gz 15294843 SHA512:22f4096781f0b075f5bf81bd39a0f97e111760dfa73b6f858f6bb54968a7847944d74969ae10f9a51cc21a2f4af20d9a4c463649dc824f5e439e196d6764c4f9
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssl/openssl_3.0.13-0ubuntu3.9.debian.tar.xz' openssl_3.0.13-0ubuntu3.9.debian.tar.xz 181192 SHA512:a196f92fa68f7b5f55efe4a0805bdc62bd62b16c5d2cb9523d588c5c39bea68f9b386de6a1b832d41eadcb082f1e6ea2f8df56a9faaf5c022dbd6e872b90b077
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssl/openssl_3.0.13-0ubuntu3.9.dsc' openssl_3.0.13-0ubuntu3.9.dsc 2512 SHA512:bd293e19828a97bde4d3c8327399fbddc65e9350cc0dced2d8daff15970bbd4fdae9996b43c31d324e829d55d98bcc0e03b0f5e4f07ef8282f6d16cb4ed7990d
```

### `dpkg` source package: `orocos-kdl=1.5.1-4build1`

Binary Packages:

- `liborocos-kdl-dev:amd64=1.5.1-4build1`
- `liborocos-kdl1.5:amd64=1.5.1-4build1`
- `python3-pykdl:amd64=1.5.1-4build1`

Licenses: (parsed from: `/usr/share/doc/liborocos-kdl-dev/copyright`, `/usr/share/doc/liborocos-kdl1.5/copyright`, `/usr/share/doc/python3-pykdl/copyright`)

- `BSD-2-clause`
- `LGPL-2.1`
- `LGPL-2.1+`

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
'http://archive.ubuntu.com/ubuntu/pool/main/p/p11-kit/p11-kit_0.25.3.orig.tar.xz' p11-kit_0.25.3.orig.tar.xz 991528 SHA256:d8ddce1bb7e898986f9d250ccae7c09ce14d82f1009046d202a0eb1b428b2adc
'http://archive.ubuntu.com/ubuntu/pool/main/p/p11-kit/p11-kit_0.25.3-4ubuntu2.1.debian.tar.xz' p11-kit_0.25.3-4ubuntu2.1.debian.tar.xz 26028 SHA256:f6e9bd39af9478e27900e9b557dc9352f5dcebb2da3ad8a0193686ebfe322cb2
'http://archive.ubuntu.com/ubuntu/pool/main/p/p11-kit/p11-kit_0.25.3-4ubuntu2.1.dsc' p11-kit_0.25.3-4ubuntu2.1.dsc 2405 SHA256:8c97d633fe815e73655b4d4b25a997a967eebca33b42db38a07b706db692a13c
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
'http://archive.ubuntu.com/ubuntu/pool/main/p/pam/pam_1.5.3.orig.tar.xz' pam_1.5.3.orig.tar.xz 1020076 SHA256:7ac4b50feee004a9fa88f1dfd2d2fa738a82896763050cd773b3c54b0a818283
'http://archive.ubuntu.com/ubuntu/pool/main/p/pam/pam_1.5.3-5ubuntu5.5.debian.tar.xz' pam_1.5.3-5ubuntu5.5.debian.tar.xz 204688 SHA256:391da0d96481d5df4ee3952d8cac5a1496ff65fcb5e76f62caae8fdc2e866b44
'http://archive.ubuntu.com/ubuntu/pool/main/p/pam/pam_1.5.3-5ubuntu5.5.dsc' pam_1.5.3-5ubuntu5.5.dsc 2727 SHA256:7f29945c6c01f7a1710401ab9ef0c2a1132fffeefecbaa308c2570d8515ee50a
```

### `dpkg` source package: `pango1.0=1.52.1+ds-1build1`

Binary Packages:

- `libpango-1.0-0:amd64=1.52.1+ds-1build1`
- `libpangocairo-1.0-0:amd64=1.52.1+ds-1build1`
- `libpangoft2-1.0-0:amd64=1.52.1+ds-1build1`

Licenses: (parsed from: `/usr/share/doc/libpango-1.0-0/copyright`, `/usr/share/doc/libpangocairo-1.0-0/copyright`, `/usr/share/doc/libpangoft2-1.0-0/copyright`)

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


### `dpkg` source package: `patch=2.7.6-7build3`

Binary Packages:

- `patch=2.7.6-7build3`

Licenses: (parsed from: `/usr/share/doc/patch/copyright`)

- `GPL`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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
'http://archive.ubuntu.com/ubuntu/pool/main/p/pcre2/pcre2_10.42.orig.tar.gz' pcre2_10.42.orig.tar.gz 2397194 SHA256:c33b418e3b936ee3153de2c61cc638e7e4fe3156022a5c77d0711bcbb9d64f1f
'http://archive.ubuntu.com/ubuntu/pool/main/p/pcre2/pcre2_10.42-4ubuntu2.1.diff.gz' pcre2_10.42-4ubuntu2.1.diff.gz 8431 SHA256:29c5cb6ff392544bf48bd3ec2a98aa0da5297457fa4f4199a1c392ec3d41f19c
'http://archive.ubuntu.com/ubuntu/pool/main/p/pcre2/pcre2_10.42-4ubuntu2.1.dsc' pcre2_10.42-4ubuntu2.1.dsc 2277 SHA256:6272177be186d6f8ad16b668bb508b2e07645e05b5b8402d446492cb6d18104e
```

### `dpkg` source package: `perl=5.38.2-3.2ubuntu0.2`

Binary Packages:

- `libperl5.38t64:amd64=5.38.2-3.2ubuntu0.2`
- `perl=5.38.2-3.2ubuntu0.2`
- `perl-base=5.38.2-3.2ubuntu0.2`
- `perl-modules-5.38=5.38.2-3.2ubuntu0.2`

Licenses: (parsed from: `/usr/share/doc/libperl5.38t64/copyright`, `/usr/share/doc/perl/copyright`, `/usr/share/doc/perl-base/copyright`, `/usr/share/doc/perl-modules-5.38/copyright`)

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
'http://archive.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.38.2.orig-regen-configure.tar.xz' perl_5.38.2.orig-regen-configure.tar.xz 418808 SHA256:4d1b34cc058f9963cb89785ecc040d57f6d7725cd83329cfa4ef8b27566454d2
'http://archive.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.38.2.orig.tar.xz' perl_5.38.2.orig.tar.xz 13679524 SHA256:d91115e90b896520e83d4de6b52f8254ef2b70a8d545ffab33200ea9f1cf29e8
'http://archive.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.38.2-3.2ubuntu0.2.debian.tar.xz' perl_5.38.2-3.2ubuntu0.2.debian.tar.xz 171736 SHA256:f7149a24aef35ff716fe9e6c724f8f9a769d1c77cddd6db301b7b7c450989b75
'http://archive.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.38.2-3.2ubuntu0.2.dsc' perl_5.38.2-3.2ubuntu0.2.dsc 3036 SHA256:4940986b06decbd6b6bbcc40770508d72cbb06c9b4350e703fe555daaa74956b
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


### `dpkg` source package: `pixman=0.42.2-1build1`

Binary Packages:

- `libpixman-1-0:amd64=0.42.2-1build1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


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
'http://archive.ubuntu.com/ubuntu/pool/main/p/procps/procps_4.0.4.orig.tar.xz' procps_4.0.4.orig.tar.xz 1401540 SHA256:22870d6feb2478adb617ce4f09a787addaf2d260c5a8aa7b17d889a962c5e42e
'http://archive.ubuntu.com/ubuntu/pool/main/p/procps/procps_4.0.4-4ubuntu3.2.debian.tar.xz' procps_4.0.4-4ubuntu3.2.debian.tar.xz 38784 SHA256:519e5cd39f4a8401dfd892134f3c5ccf5221f23fe32174393ce81cc45526f05e
'http://archive.ubuntu.com/ubuntu/pool/main/p/procps/procps_4.0.4-4ubuntu3.2.dsc' procps_4.0.4-4ubuntu3.2.dsc 2251 SHA256:eee89a6469fcc4fb8ee3844b10bf48c894322ff781e92732554c7ceed680c5a1
```

### `dpkg` source package: `pybind11=2.11.1-2`

Binary Packages:

- `pybind11-dev=2.11.1-2`

Licenses: (parsed from: `/usr/share/doc/pybind11-dev/copyright`)

- `BSD-2-Clause`
- `BSD-3-Clause`
- `BSD-3-Clause+CLA`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/pybind11/2.11.1-2/


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
'http://archive.ubuntu.com/ubuntu/pool/universe/p/python-argcomplete/python-argcomplete_3.1.4.orig.tar.gz' python-argcomplete_3.1.4.orig.tar.gz 79529 SHA256:72558ba729e4c468572609817226fb0a6e7e9a0a7d477b882be168c0b4a62b94
'http://archive.ubuntu.com/ubuntu/pool/universe/p/python-argcomplete/python-argcomplete_3.1.4-1ubuntu0.1.debian.tar.xz' python-argcomplete_3.1.4-1ubuntu0.1.debian.tar.xz 8116 SHA256:cedffaabe1930ddce0b8fb197e4ed600c8221403c1b5fd766010d7d103b57b3c
'http://archive.ubuntu.com/ubuntu/pool/universe/p/python-argcomplete/python-argcomplete_3.1.4-1ubuntu0.1.dsc' python-argcomplete_3.1.4-1ubuntu0.1.dsc 2509 SHA256:c4377d2b568aa7ec6fe31f9266cf7c7f459c93c747642a6717da0848b688146a
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
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-cryptography/python-cryptography_41.0.7.orig.tar.gz' python-cryptography_41.0.7.orig.tar.gz 630892 SHA256:13f93ce9bea8016c253b34afc6bd6a75993e5c40672ed5405a9c832f0d4a00bc
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-cryptography/python-cryptography_41.0.7-4ubuntu0.4.debian.tar.xz' python-cryptography_41.0.7-4ubuntu0.4.debian.tar.xz 13648 SHA256:bed8f4ba2a32d22bc36cf72434612cde9cf2ca40521c1b1b05801e55882f5f0d
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-cryptography/python-cryptography_41.0.7-4ubuntu0.4.dsc' python-cryptography_41.0.7-4ubuntu0.4.dsc 3363 SHA256:a45c188893f0aaa8b71ad7fa9adaf41b6beef3d45650f447cb2d7c5583d2ca61
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


### `dpkg` source package: `python-notify2=0.3-5`

Binary Packages:

- `python3-notify2=0.3-5`

Licenses: (parsed from: `/usr/share/doc/python3-notify2/copyright`)

- `BSD-3-Clause`
- `LGPL-2.1`
- `LGPL-2.1+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/python-notify2/0.3-5/


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
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-zipp/python-zipp_1.0.0.orig.tar.gz' python-zipp_1.0.0.orig.tar.gz 10821 SHA256:d38fbe01bbf7a3593a32bc35a9c4453c32bc42b98c377f9bff7e9f8da157786c
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-zipp/python-zipp_1.0.0-6ubuntu0.1.debian.tar.xz' python-zipp_1.0.0-6ubuntu0.1.debian.tar.xz 4188 SHA256:0a9ced99171dcc1904d2fef982c35c796e9c80d9a920dd618078c357b8981801
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-zipp/python-zipp_1.0.0-6ubuntu0.1.dsc' python-zipp_1.0.0-6ubuntu0.1.dsc 1616 SHA256:b64a8f5fcd78afe01b9cdbb61f7a5e8eae3baa5e6f3966a6efe33cd585b0330b
```

### `dpkg` source package: `python3-catkin-pkg-modules=1.1.0-2`

Binary Packages:

- `python3-catkin-pkg-modules=1.1.0-2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-colcon-argcomplete=0.3.3+upstream-1`

Binary Packages:

- `python3-colcon-argcomplete=0.3.3+upstream-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-colcon-bash=0.5.0-100`

Binary Packages:

- `python3-colcon-bash=0.5.0-100`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-colcon-cd=0.2.1-100`

Binary Packages:

- `python3-colcon-cd=0.2.1-100`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-colcon-cmake=0.2.29-100`

Binary Packages:

- `python3-colcon-cmake=0.2.29-100`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-colcon-common-extensions=0.3.0-100`

Binary Packages:

- `python3-colcon-common-extensions=0.3.0-100`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-colcon-core=0.20.1+upstream-1`

Binary Packages:

- `python3-colcon-core=0.20.1+upstream-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-colcon-defaults=0.2.9+upstream-1`

Binary Packages:

- `python3-colcon-defaults=0.2.9+upstream-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-colcon-devtools=0.3.0-100`

Binary Packages:

- `python3-colcon-devtools=0.3.0-100`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-colcon-library-path=0.2.1-100`

Binary Packages:

- `python3-colcon-library-path=0.2.1-100`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-colcon-metadata=0.2.5-100`

Binary Packages:

- `python3-colcon-metadata=0.2.5-100`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-colcon-mixin=0.2.3-100`

Binary Packages:

- `python3-colcon-mixin=0.2.3-100`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-colcon-notification=0.3.1+upstream-1`

Binary Packages:

- `python3-colcon-notification=0.3.1+upstream-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-colcon-output=0.2.14+upstream-1`

Binary Packages:

- `python3-colcon-output=0.2.14+upstream-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-colcon-package-information=0.4.1+upstream-1`

Binary Packages:

- `python3-colcon-package-information=0.4.1+upstream-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-colcon-package-selection=0.2.10-100`

Binary Packages:

- `python3-colcon-package-selection=0.2.10-100`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-colcon-parallel-executor=0.3.0-100`

Binary Packages:

- `python3-colcon-parallel-executor=0.3.0-100`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-colcon-pkg-config=0.1.0-100`

Binary Packages:

- `python3-colcon-pkg-config=0.1.0-100`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-colcon-powershell=0.5.0+upstream-1`

Binary Packages:

- `python3-colcon-powershell=0.5.0+upstream-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-colcon-python-setup-py=0.2.9-100`

Binary Packages:

- `python3-colcon-python-setup-py=0.2.9-100`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-colcon-recursive-crawl=0.2.3-100`

Binary Packages:

- `python3-colcon-recursive-crawl=0.2.3-100`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-colcon-ros=0.5.0+upstream-1`

Binary Packages:

- `python3-colcon-ros=0.5.0+upstream-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-colcon-test-result=0.3.8-100`

Binary Packages:

- `python3-colcon-test-result=0.3.8-100`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-colcon-zsh=0.5.0-100`

Binary Packages:

- `python3-colcon-zsh=0.5.0-100`

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
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3-defaults/python3-defaults_3.12.3-0ubuntu2.1.tar.gz' python3-defaults_3.12.3-0ubuntu2.1.tar.gz 147765 SHA256:1a6b241d5fb2df35d0f1b683a783ced7b4fe0f05c29db3d3592e64da8cc188ae
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3-defaults/python3-defaults_3.12.3-0ubuntu2.1.dsc' python3-defaults_3.12.3-0ubuntu2.1.dsc 3116 SHA256:79676920120c7f45f1605d92047174fca9cc75a39d9df91c9740be98fb8cc542
```

### `dpkg` source package: `python3-rosdep-modules=0.26.0-1`

Binary Packages:

- `python3-rosdep-modules=0.26.0-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3-rosdep=0.26.0-1`

Binary Packages:

- `python3-rosdep=0.26.0-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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


### `dpkg` source package: `python3-vcstool=0.3.0-1`

Binary Packages:

- `python3-vcstool=0.3.0-1`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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


### `dpkg` source package: `ros-jazzy-action-msgs=2.0.3-1noble.20260412.032342`

Binary Packages:

- `ros-jazzy-action-msgs=2.0.3-1noble.20260412.032342`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-action-msgs/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-actionlib-msgs=5.3.7-1noble.20260412.034232`

Binary Packages:

- `ros-jazzy-actionlib-msgs=5.3.7-1noble.20260412.034232`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-actionlib-msgs/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-auto=2.5.6-2noble.20260225.232257`

Binary Packages:

- `ros-jazzy-ament-cmake-auto=2.5.6-2noble.20260225.232257`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-auto/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-copyright=0.17.5-1noble.20260410.113746`

Binary Packages:

- `ros-jazzy-ament-cmake-copyright=0.17.5-1noble.20260410.113746`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-copyright/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-core=2.5.6-2noble.20260224.191131`

Binary Packages:

- `ros-jazzy-ament-cmake-core=2.5.6-2noble.20260224.191131`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-core/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-cppcheck=0.17.5-1noble.20260410.113607`

Binary Packages:

- `ros-jazzy-ament-cmake-cppcheck=0.17.5-1noble.20260410.113607`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-cppcheck/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-cpplint=0.17.5-1noble.20260410.105800`

Binary Packages:

- `ros-jazzy-ament-cmake-cpplint=0.17.5-1noble.20260410.105800`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-cpplint/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-export-definitions=2.5.6-2noble.20260224.232207`

Binary Packages:

- `ros-jazzy-ament-cmake-export-definitions=2.5.6-2noble.20260224.232207`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-export-definitions/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-export-dependencies=2.5.6-2noble.20260225.043730`

Binary Packages:

- `ros-jazzy-ament-cmake-export-dependencies=2.5.6-2noble.20260225.043730`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-export-dependencies/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-export-include-directories=2.5.6-2noble.20260224.232223`

Binary Packages:

- `ros-jazzy-ament-cmake-export-include-directories=2.5.6-2noble.20260224.232223`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-export-include-directories/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-export-interfaces=2.5.6-2noble.20260225.042039`

Binary Packages:

- `ros-jazzy-ament-cmake-export-interfaces=2.5.6-2noble.20260225.042039`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-export-interfaces/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-export-libraries=2.5.6-2noble.20260224.232254`

Binary Packages:

- `ros-jazzy-ament-cmake-export-libraries=2.5.6-2noble.20260224.232254`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-export-libraries/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-export-link-flags=2.5.6-2noble.20260225.042107`

Binary Packages:

- `ros-jazzy-ament-cmake-export-link-flags=2.5.6-2noble.20260225.042107`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-export-link-flags/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-export-targets=2.5.6-2noble.20260225.042100`

Binary Packages:

- `ros-jazzy-ament-cmake-export-targets=2.5.6-2noble.20260225.042100`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-export-targets/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-flake8=0.17.5-1noble.20260410.113910`

Binary Packages:

- `ros-jazzy-ament-cmake-flake8=0.17.5-1noble.20260410.113910`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-flake8/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-gen-version-h=2.5.6-2noble.20260225.042237`

Binary Packages:

- `ros-jazzy-ament-cmake-gen-version-h=2.5.6-2noble.20260225.042237`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-gen-version-h/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-gmock=2.5.6-2noble.20260225.215706`

Binary Packages:

- `ros-jazzy-ament-cmake-gmock=2.5.6-2noble.20260225.215706`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-gmock/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-gtest=2.5.6-2noble.20260225.145055`

Binary Packages:

- `ros-jazzy-ament-cmake-gtest=2.5.6-2noble.20260225.145055`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-gtest/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-include-directories=2.5.6-2noble.20260225.042241`

Binary Packages:

- `ros-jazzy-ament-cmake-include-directories=2.5.6-2noble.20260225.042241`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-include-directories/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-libraries=2.5.6-2noble.20260225.042312`

Binary Packages:

- `ros-jazzy-ament-cmake-libraries=2.5.6-2noble.20260225.042312`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-libraries/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-lint-cmake=0.17.5-1noble.20260410.113602`

Binary Packages:

- `ros-jazzy-ament-cmake-lint-cmake=0.17.5-1noble.20260410.113602`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-lint-cmake/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-pep257=0.17.5-1noble.20260410.113929`

Binary Packages:

- `ros-jazzy-ament-cmake-pep257=0.17.5-1noble.20260410.113929`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-pep257/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-pytest=2.5.6-2noble.20260225.145739`

Binary Packages:

- `ros-jazzy-ament-cmake-pytest=2.5.6-2noble.20260225.145739`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-pytest/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-python=2.5.6-2noble.20260225.042312`

Binary Packages:

- `ros-jazzy-ament-cmake-python=2.5.6-2noble.20260225.042312`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-python/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-ros=0.12.0-3noble.20260225.232209`

Binary Packages:

- `ros-jazzy-ament-cmake-ros=0.12.0-3noble.20260225.232209`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-ros/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-target-dependencies=2.5.6-2noble.20260225.043936`

Binary Packages:

- `ros-jazzy-ament-cmake-target-dependencies=2.5.6-2noble.20260225.043936`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-target-dependencies/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-test=2.5.6-2noble.20260225.143205`

Binary Packages:

- `ros-jazzy-ament-cmake-test=2.5.6-2noble.20260225.143205`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-test/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-uncrustify=0.17.5-1noble.20260410.113615`

Binary Packages:

- `ros-jazzy-ament-cmake-uncrustify=0.17.5-1noble.20260410.113615`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-uncrustify/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-version=2.5.6-2noble.20260225.042330`

Binary Packages:

- `ros-jazzy-ament-cmake-version=2.5.6-2noble.20260225.042330`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-version/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake-xmllint=0.17.5-1noble.20260410.113914`

Binary Packages:

- `ros-jazzy-ament-cmake-xmllint=0.17.5-1noble.20260410.113914`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake-xmllint/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cmake=2.5.6-2noble.20260225.222913`

Binary Packages:

- `ros-jazzy-ament-cmake=2.5.6-2noble.20260225.222913`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cmake/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-copyright=0.17.5-1noble.20260410.105859`

Binary Packages:

- `ros-jazzy-ament-copyright=0.17.5-1noble.20260410.105859`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-copyright/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cppcheck=0.17.5-1noble.20260410.080408`

Binary Packages:

- `ros-jazzy-ament-cppcheck=0.17.5-1noble.20260410.080408`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cppcheck/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-cpplint=0.17.5-1noble.20260410.080348`

Binary Packages:

- `ros-jazzy-ament-cpplint=0.17.5-1noble.20260410.080348`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-cpplint/copyright`)

- `Apache License 2.0`
- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-flake8=0.17.5-1noble.20260410.113507`

Binary Packages:

- `ros-jazzy-ament-flake8=0.17.5-1noble.20260410.113507`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-flake8/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-index-cpp=1.8.2-1noble.20260412.024949`

Binary Packages:

- `ros-jazzy-ament-index-cpp=1.8.2-1noble.20260412.024949`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-index-cpp/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-index-python=1.8.2-1noble.20260412.024953`

Binary Packages:

- `ros-jazzy-ament-index-python=1.8.2-1noble.20260412.024953`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-index-python/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-lint-auto=0.17.5-1noble.20260410.080333`

Binary Packages:

- `ros-jazzy-ament-lint-auto=0.17.5-1noble.20260410.080333`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-lint-auto/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-lint-cmake=0.17.5-1noble.20260410.080405`

Binary Packages:

- `ros-jazzy-ament-lint-cmake=0.17.5-1noble.20260410.080405`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-lint-cmake/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-lint-common=0.17.5-1noble.20260410.114154`

Binary Packages:

- `ros-jazzy-ament-lint-common=0.17.5-1noble.20260410.114154`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-lint-common/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-lint=0.17.5-1noble.20260410.080358`

Binary Packages:

- `ros-jazzy-ament-lint=0.17.5-1noble.20260410.080358`

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


### `dpkg` source package: `ros-jazzy-ament-pep257=0.17.5-1noble.20260410.113520`

Binary Packages:

- `ros-jazzy-ament-pep257=0.17.5-1noble.20260410.113520`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-pep257/copyright`)

- `Apache License 2.0`
- `MIT`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-uncrustify=0.17.5-1noble.20260410.080359`

Binary Packages:

- `ros-jazzy-ament-uncrustify=0.17.5-1noble.20260410.080359`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-uncrustify/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ament-xmllint=0.17.5-1noble.20260410.113521`

Binary Packages:

- `ros-jazzy-ament-xmllint=0.17.5-1noble.20260410.113521`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ament-xmllint/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-builtin-interfaces=2.0.3-1noble.20260412.031450`

Binary Packages:

- `ros-jazzy-builtin-interfaces=2.0.3-1noble.20260412.031450`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-builtin-interfaces/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-class-loader=2.7.0-3noble.20260226.003328`

Binary Packages:

- `ros-jazzy-class-loader=2.7.0-3noble.20260226.003328`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-class-loader/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-common-interfaces=5.3.7-1noble.20260412.035857`

Binary Packages:

- `ros-jazzy-common-interfaces=5.3.7-1noble.20260412.035857`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-common-interfaces/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-composition-interfaces=2.0.3-1noble.20260412.034209`

Binary Packages:

- `ros-jazzy-composition-interfaces=2.0.3-1noble.20260412.034209`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-composition-interfaces/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-console-bridge-vendor=1.7.1-3noble.20260225.232019`

Binary Packages:

- `ros-jazzy-console-bridge-vendor=1.7.1-3noble.20260225.232019`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-console-bridge-vendor/copyright`)

- `Apache License 2.0`
- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-diagnostic-msgs=5.3.7-1noble.20260412.034614`

Binary Packages:

- `ros-jazzy-diagnostic-msgs=5.3.7-1noble.20260412.034614`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-diagnostic-msgs/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-domain-coordinator=0.12.0-3noble.20260225.051359`

Binary Packages:

- `ros-jazzy-domain-coordinator=0.12.0-3noble.20260225.051359`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-domain-coordinator/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-eigen3-cmake-module=0.3.0-3noble.20260225.233716`

Binary Packages:

- `ros-jazzy-eigen3-cmake-module=0.3.0-3noble.20260225.233716`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-eigen3-cmake-module/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-fastcdr=2.2.7-1noble.20260225.051855`

Binary Packages:

- `ros-jazzy-fastcdr=2.2.7-1noble.20260225.051855`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-fastcdr/copyright`)

- `Apache 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-fastrtps-cmake-module=3.6.3-1noble.20260225.234436`

Binary Packages:

- `ros-jazzy-fastrtps-cmake-module=3.6.3-1noble.20260225.234436`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-fastrtps-cmake-module/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-fastrtps=2.14.6-1noble.20260303.233638`

Binary Packages:

- `ros-jazzy-fastrtps=2.14.6-1noble.20260303.233638`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-fastrtps/copyright`)

- `Apache 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-foonathan-memory-vendor=1.3.1-3noble.20260225.055155`

Binary Packages:

- `ros-jazzy-foonathan-memory-vendor=1.3.1-3noble.20260225.055155`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-foonathan-memory-vendor/copyright`)

- `Apache License 2.0`
- `zlib License`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-geometry-msgs=5.3.7-1noble.20260412.033928`

Binary Packages:

- `ros-jazzy-geometry-msgs=5.3.7-1noble.20260412.033928`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-geometry-msgs/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-geometry2=0.36.20-1noble.20260412.060249`

Binary Packages:

- `ros-jazzy-geometry2=0.36.20-1noble.20260412.060249`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-geometry2/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-gmock-vendor=1.14.9000-2noble.20260225.143751`

Binary Packages:

- `ros-jazzy-gmock-vendor=1.14.9000-2noble.20260225.143751`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-gmock-vendor/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-gtest-vendor=1.14.9000-2noble.20260225.055309`

Binary Packages:

- `ros-jazzy-gtest-vendor=1.14.9000-2noble.20260225.055309`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-gtest-vendor/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-kdl-parser=2.11.0-3noble.20260412.025844`

Binary Packages:

- `ros-jazzy-kdl-parser=2.11.0-3noble.20260412.025844`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-kdl-parser/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-keyboard-handler=0.3.2-1noble.20260225.235108`

Binary Packages:

- `ros-jazzy-keyboard-handler=0.3.2-1noble.20260225.235108`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-keyboard-handler/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-launch-ros=0.26.11-1noble.20260412.042642`

Binary Packages:

- `ros-jazzy-launch-ros=0.26.11-1noble.20260412.042642`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-launch-ros/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-launch-testing-ament-cmake=3.4.10-1noble.20260412.025830`

Binary Packages:

- `ros-jazzy-launch-testing-ament-cmake=3.4.10-1noble.20260412.025830`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-launch-testing-ament-cmake/copyright`)

- `Apache License 2.0`
- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-launch-testing-ros=0.26.11-1noble.20260412.043323`

Binary Packages:

- `ros-jazzy-launch-testing-ros=0.26.11-1noble.20260412.043323`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-launch-testing-ros/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-launch-testing=3.4.10-1noble.20260412.025508`

Binary Packages:

- `ros-jazzy-launch-testing=3.4.10-1noble.20260412.025508`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-launch-testing/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-launch-xml=3.4.10-1noble.20260412.025343`

Binary Packages:

- `ros-jazzy-launch-xml=3.4.10-1noble.20260412.025343`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-launch-xml/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-launch-yaml=3.4.10-1noble.20260412.025341`

Binary Packages:

- `ros-jazzy-launch-yaml=3.4.10-1noble.20260412.025341`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-launch-yaml/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-launch=3.4.10-1noble.20260412.025232`

Binary Packages:

- `ros-jazzy-launch=3.4.10-1noble.20260412.025232`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-launch/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-liblz4-vendor=0.26.10-2noble.20260408.222020`

Binary Packages:

- `ros-jazzy-liblz4-vendor=0.26.10-2noble.20260408.222020`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-liblz4-vendor/copyright`)

- `Apache License 2.0`
- `BSD`
- `GPLv2`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-libstatistics-collector=1.7.4-1noble.20260412.041007`

Binary Packages:

- `ros-jazzy-libstatistics-collector=1.7.4-1noble.20260412.041007`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-libstatistics-collector/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-libyaml-vendor=1.6.3-2noble.20260225.235345`

Binary Packages:

- `ros-jazzy-libyaml-vendor=1.6.3-2noble.20260225.235345`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-libyaml-vendor/copyright`)

- `Apache License 2.0`
- `MIT`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-lifecycle-msgs=2.0.3-1noble.20260412.032912`

Binary Packages:

- `ros-jazzy-lifecycle-msgs=2.0.3-1noble.20260412.032912`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-lifecycle-msgs/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-mcap-vendor=0.26.10-2noble.20260408.222435`

Binary Packages:

- `ros-jazzy-mcap-vendor=0.26.10-2noble.20260408.222435`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-mcap-vendor/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-message-filters=4.11.12-1noble.20260412.042737`

Binary Packages:

- `ros-jazzy-message-filters=4.11.12-1noble.20260412.042737`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-message-filters/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-nav-msgs=5.3.7-1noble.20260412.034710`

Binary Packages:

- `ros-jazzy-nav-msgs=5.3.7-1noble.20260412.034710`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-nav-msgs/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-orocos-kdl-vendor=0.5.1-2noble.20260225.234720`

Binary Packages:

- `ros-jazzy-orocos-kdl-vendor=0.5.1-2noble.20260225.234720`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-orocos-kdl-vendor/copyright`)

- `Apache License 2.0`
- `LGPL-2.1-or-later`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-osrf-pycommon=2.1.7-1noble.20260225.055811`

Binary Packages:

- `ros-jazzy-osrf-pycommon=2.1.7-1noble.20260225.055811`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-osrf-pycommon/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-pluginlib=5.4.5-1noble.20260412.025240`

Binary Packages:

- `ros-jazzy-pluginlib=5.4.5-1noble.20260412.025240`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-pluginlib/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-pybind11-vendor=3.1.3-1noble.20260226.000033`

Binary Packages:

- `ros-jazzy-pybind11-vendor=3.1.3-1noble.20260226.000033`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-pybind11-vendor/copyright`)

- `Apache License 2.0`
- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-python-cmake-module=0.11.1-2noble.20260226.000327`

Binary Packages:

- `ros-jazzy-python-cmake-module=0.11.1-2noble.20260226.000327`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-python-cmake-module/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-python-orocos-kdl-vendor=0.5.1-2noble.20260226.001217`

Binary Packages:

- `ros-jazzy-python-orocos-kdl-vendor=0.5.1-2noble.20260226.001217`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-python-orocos-kdl-vendor/copyright`)

- `Apache License 2.0`
- `LGPL-2.1-or-later`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rcl-action=9.2.9-1noble.20260412.041043`

Binary Packages:

- `ros-jazzy-rcl-action=9.2.9-1noble.20260412.041043`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rcl-action/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rcl-interfaces=2.0.3-1noble.20260412.033104`

Binary Packages:

- `ros-jazzy-rcl-interfaces=2.0.3-1noble.20260412.033104`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rcl-interfaces/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rcl-lifecycle=9.2.9-1noble.20260412.040958`

Binary Packages:

- `ros-jazzy-rcl-lifecycle=9.2.9-1noble.20260412.040958`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rcl-lifecycle/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rcl-logging-interface=3.1.1-1noble.20260226.002403`

Binary Packages:

- `ros-jazzy-rcl-logging-interface=3.1.1-1noble.20260226.002403`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rcl-logging-interface/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rcl-logging-spdlog=3.1.1-1noble.20260226.003321`

Binary Packages:

- `ros-jazzy-rcl-logging-spdlog=3.1.1-1noble.20260226.003321`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rcl-logging-spdlog/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rcl-yaml-param-parser=9.2.9-1noble.20260226.005115`

Binary Packages:

- `ros-jazzy-rcl-yaml-param-parser=9.2.9-1noble.20260226.005115`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rcl-yaml-param-parser/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rcl=9.2.9-1noble.20260412.040633`

Binary Packages:

- `ros-jazzy-rcl=9.2.9-1noble.20260412.040633`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rcl/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rclcpp-action=28.1.18-1noble.20260412.042748`

Binary Packages:

- `ros-jazzy-rclcpp-action=28.1.18-1noble.20260412.042748`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rclcpp-action/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rclcpp-components=28.1.18-1noble.20260412.042656`

Binary Packages:

- `ros-jazzy-rclcpp-components=28.1.18-1noble.20260412.042656`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rclcpp-components/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rclcpp-lifecycle=28.1.18-1noble.20260412.042728`

Binary Packages:

- `ros-jazzy-rclcpp-lifecycle=28.1.18-1noble.20260412.042728`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rclcpp-lifecycle/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rclcpp=28.1.18-1noble.20260412.041931`

Binary Packages:

- `ros-jazzy-rclcpp=28.1.18-1noble.20260412.041931`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rclcpp/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rclpy=7.1.11-1noble.20260412.041747`

Binary Packages:

- `ros-jazzy-rclpy=7.1.11-1noble.20260412.041747`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rclpy/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rcpputils=2.11.3-1noble.20260226.002359`

Binary Packages:

- `ros-jazzy-rcpputils=2.11.3-1noble.20260226.002359`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rcpputils/copyright`)

- `Apache License 2.0`
- `BSD-3-Clause`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rcutils=6.7.5-1noble.20260226.001538`

Binary Packages:

- `ros-jazzy-rcutils=6.7.5-1noble.20260226.001538`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rcutils/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rmw-dds-common=3.1.1-1noble.20260412.033108`

Binary Packages:

- `ros-jazzy-rmw-dds-common=3.1.1-1noble.20260412.033108`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rmw-dds-common/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rmw-fastrtps-cpp=8.4.3-1noble.20260412.034154`

Binary Packages:

- `ros-jazzy-rmw-fastrtps-cpp=8.4.3-1noble.20260412.034154`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rmw-fastrtps-cpp/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rmw-fastrtps-shared-cpp=8.4.3-1noble.20260412.033316`

Binary Packages:

- `ros-jazzy-rmw-fastrtps-shared-cpp=8.4.3-1noble.20260412.033316`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rmw-fastrtps-shared-cpp/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rmw-implementation-cmake=7.3.3-1noble.20260225.225156`

Binary Packages:

- `ros-jazzy-rmw-implementation-cmake=7.3.3-1noble.20260225.225156`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rmw-implementation-cmake/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rmw-implementation=2.15.6-1noble.20260412.040200`

Binary Packages:

- `ros-jazzy-rmw-implementation=2.15.6-1noble.20260412.040200`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rmw-implementation/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rmw=7.3.3-1noble.20260226.004315`

Binary Packages:

- `ros-jazzy-rmw=7.3.3-1noble.20260226.004315`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rmw/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-robot-state-publisher=3.3.3-3noble.20260412.044622`

Binary Packages:

- `ros-jazzy-robot-state-publisher=3.3.3-3noble.20260412.044622`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-robot-state-publisher/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ros-base=0.11.0-1noble.20260412.071950`

Binary Packages:

- `ros-jazzy-ros-base=0.11.0-1noble.20260412.071950`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ros-base/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ros-core=0.11.0-1noble.20260412.053408`

Binary Packages:

- `ros-jazzy-ros-core=0.11.0-1noble.20260412.053408`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ros-core/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ros-environment=4.2.1-1noble.20260225.043405`

Binary Packages:

- `ros-jazzy-ros-environment=4.2.1-1noble.20260225.043405`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ros-environment/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ros-workspace=1.0.3-7noble.20260224.191628`

Binary Packages:

- `ros-jazzy-ros-workspace=1.0.3-7noble.20260224.191628`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ros-workspace/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ros2action=0.32.9-1noble.20260412.053021`

Binary Packages:

- `ros-jazzy-ros2action=0.32.9-1noble.20260412.053021`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ros2action/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ros2bag=0.26.10-2noble.20260412.065702`

Binary Packages:

- `ros-jazzy-ros2bag=0.26.10-2noble.20260412.065702`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ros2bag/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ros2cli-common-extensions=0.3.1-1noble.20260412.053337`

Binary Packages:

- `ros-jazzy-ros2cli-common-extensions=0.3.1-1noble.20260412.053337`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ros2cli-common-extensions/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ros2cli=0.32.9-1noble.20260412.042300`

Binary Packages:

- `ros-jazzy-ros2cli=0.32.9-1noble.20260412.042300`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ros2cli/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ros2component=0.32.9-1noble.20260412.052519`

Binary Packages:

- `ros-jazzy-ros2component=0.32.9-1noble.20260412.052519`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ros2component/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ros2doctor=0.32.9-1noble.20260412.042619`

Binary Packages:

- `ros-jazzy-ros2doctor=0.32.9-1noble.20260412.042619`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ros2doctor/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ros2interface=0.32.9-1noble.20260412.042621`

Binary Packages:

- `ros-jazzy-ros2interface=0.32.9-1noble.20260412.042621`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ros2interface/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ros2launch=0.26.11-1noble.20260412.043200`

Binary Packages:

- `ros-jazzy-ros2launch=0.26.11-1noble.20260412.043200`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ros2launch/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ros2lifecycle=0.32.9-1noble.20260412.052446`

Binary Packages:

- `ros-jazzy-ros2lifecycle=0.32.9-1noble.20260412.052446`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ros2lifecycle/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ros2multicast=0.32.9-1noble.20260412.053041`

Binary Packages:

- `ros-jazzy-ros2multicast=0.32.9-1noble.20260412.053041`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ros2multicast/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ros2node=0.32.9-1noble.20260412.042626`

Binary Packages:

- `ros-jazzy-ros2node=0.32.9-1noble.20260412.042626`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ros2node/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ros2param=0.32.9-1noble.20260412.052450`

Binary Packages:

- `ros-jazzy-ros2param=0.32.9-1noble.20260412.052450`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ros2param/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ros2pkg=0.32.9-1noble.20260412.042622`

Binary Packages:

- `ros-jazzy-ros2pkg=0.32.9-1noble.20260412.042622`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ros2pkg/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ros2plugin=5.4.5-1noble.20260412.042739`

Binary Packages:

- `ros-jazzy-ros2plugin=5.4.5-1noble.20260412.042739`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ros2plugin/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ros2run=0.32.9-1noble.20260412.053103`

Binary Packages:

- `ros-jazzy-ros2run=0.32.9-1noble.20260412.053103`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ros2run/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ros2service=0.32.9-1noble.20260412.052412`

Binary Packages:

- `ros-jazzy-ros2service=0.32.9-1noble.20260412.052412`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ros2service/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-ros2topic=0.32.9-1noble.20260412.042628`

Binary Packages:

- `ros-jazzy-ros2topic=0.32.9-1noble.20260412.042628`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-ros2topic/copyright`)

- `Apache License 2.0`
- `BSD-3-Clause`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosbag2-compression-zstd=0.26.10-2noble.20260412.054126`

Binary Packages:

- `ros-jazzy-rosbag2-compression-zstd=0.26.10-2noble.20260412.054126`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosbag2-compression-zstd/copyright`)

- `Apache 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosbag2-compression=0.26.10-2noble.20260412.053554`

Binary Packages:

- `ros-jazzy-rosbag2-compression=0.26.10-2noble.20260412.053554`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosbag2-compression/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosbag2-cpp=0.26.10-2noble.20260412.043347`

Binary Packages:

- `ros-jazzy-rosbag2-cpp=0.26.10-2noble.20260412.043347`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosbag2-cpp/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosbag2-interfaces=0.26.10-2noble.20260412.033118`

Binary Packages:

- `ros-jazzy-rosbag2-interfaces=0.26.10-2noble.20260412.033118`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosbag2-interfaces/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosbag2-py=0.26.10-2noble.20260412.060353`

Binary Packages:

- `ros-jazzy-rosbag2-py=0.26.10-2noble.20260412.060353`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosbag2-py/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosbag2-storage-default-plugins=0.26.10-2noble.20260412.065628`

Binary Packages:

- `ros-jazzy-rosbag2-storage-default-plugins=0.26.10-2noble.20260412.065628`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosbag2-storage-default-plugins/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosbag2-storage-mcap=0.26.10-2noble.20260412.043351`

Binary Packages:

- `ros-jazzy-rosbag2-storage-mcap=0.26.10-2noble.20260412.043351`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosbag2-storage-mcap/copyright`)

- `Apache-2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosbag2-storage-sqlite3=0.26.10-2noble.20260412.043751`

Binary Packages:

- `ros-jazzy-rosbag2-storage-sqlite3=0.26.10-2noble.20260412.043751`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosbag2-storage-sqlite3/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosbag2-storage=0.26.10-2noble.20260412.042713`

Binary Packages:

- `ros-jazzy-rosbag2-storage=0.26.10-2noble.20260412.042713`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosbag2-storage/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosbag2-transport=0.26.10-2noble.20260412.054424`

Binary Packages:

- `ros-jazzy-rosbag2-transport=0.26.10-2noble.20260412.054424`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosbag2-transport/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosbag2=0.26.10-2noble.20260412.070736`

Binary Packages:

- `ros-jazzy-rosbag2=0.26.10-2noble.20260412.070736`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosbag2/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosgraph-msgs=2.0.3-1noble.20260412.033127`

Binary Packages:

- `ros-jazzy-rosgraph-msgs=2.0.3-1noble.20260412.033127`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosgraph-msgs/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-adapter=4.6.7-1noble.20260225.225255`

Binary Packages:

- `ros-jazzy-rosidl-adapter=4.6.7-1noble.20260225.225255`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-adapter/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-cli=4.6.7-1noble.20260225.142152`

Binary Packages:

- `ros-jazzy-rosidl-cli=4.6.7-1noble.20260225.142152`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-cli/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-cmake=4.6.7-1noble.20260226.001208`

Binary Packages:

- `ros-jazzy-rosidl-cmake=4.6.7-1noble.20260226.001208`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-cmake/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-core-generators=0.2.1-1noble.20260412.030913`

Binary Packages:

- `ros-jazzy-rosidl-core-generators=0.2.1-1noble.20260412.030913`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-core-generators/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-core-runtime=0.2.1-1noble.20260412.030912`

Binary Packages:

- `ros-jazzy-rosidl-core-runtime=0.2.1-1noble.20260412.030912`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-core-runtime/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-default-generators=1.6.0-3noble.20260412.032513`

Binary Packages:

- `ros-jazzy-rosidl-default-generators=1.6.0-3noble.20260412.032513`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-default-generators/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-default-runtime=1.6.0-3noble.20260412.032511`

Binary Packages:

- `ros-jazzy-rosidl-default-runtime=1.6.0-3noble.20260412.032511`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-default-runtime/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-dynamic-typesupport-fastrtps=0.1.0-3noble.20260304.002637`

Binary Packages:

- `ros-jazzy-rosidl-dynamic-typesupport-fastrtps=0.1.0-3noble.20260304.002637`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-dynamic-typesupport-fastrtps/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-dynamic-typesupport=0.1.2-3noble.20260226.003402`

Binary Packages:

- `ros-jazzy-rosidl-dynamic-typesupport=0.1.2-3noble.20260226.003402`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-dynamic-typesupport/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-generator-c=4.6.7-1noble.20260412.025459`

Binary Packages:

- `ros-jazzy-rosidl-generator-c=4.6.7-1noble.20260412.025459`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-generator-c/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-generator-cpp=4.6.7-1noble.20260412.025832`

Binary Packages:

- `ros-jazzy-rosidl-generator-cpp=4.6.7-1noble.20260412.025832`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-generator-cpp/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-generator-py=0.22.2-1noble.20260412.030620`

Binary Packages:

- `ros-jazzy-rosidl-generator-py=0.22.2-1noble.20260412.030620`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-generator-py/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-generator-rs=0.4.11-1noble.20260412.030734`

Binary Packages:

- `ros-jazzy-rosidl-generator-rs=0.4.11-1noble.20260412.030734`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-generator-rs/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-generator-type-description=4.6.7-1noble.20260412.025231`

Binary Packages:

- `ros-jazzy-rosidl-generator-type-description=4.6.7-1noble.20260412.025231`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-generator-type-description/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-parser=4.6.7-1noble.20260225.230105`

Binary Packages:

- `ros-jazzy-rosidl-parser=4.6.7-1noble.20260225.230105`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-parser/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-pycommon=4.6.7-1noble.20260226.000402`

Binary Packages:

- `ros-jazzy-rosidl-pycommon=4.6.7-1noble.20260226.000402`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-pycommon/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-runtime-c=4.6.7-1noble.20260226.002400`

Binary Packages:

- `ros-jazzy-rosidl-runtime-c=4.6.7-1noble.20260226.002400`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-runtime-c/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-runtime-cpp=4.6.7-1noble.20260226.003416`

Binary Packages:

- `ros-jazzy-rosidl-runtime-cpp=4.6.7-1noble.20260226.003416`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-runtime-cpp/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-runtime-py=0.13.1-2noble.20260226.000416`

Binary Packages:

- `ros-jazzy-rosidl-runtime-py=0.13.1-2noble.20260226.000416`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-runtime-py/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-typesupport-c=3.2.2-1noble.20260412.030231`

Binary Packages:

- `ros-jazzy-rosidl-typesupport-c=3.2.2-1noble.20260412.030231`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-typesupport-c/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-typesupport-cpp=3.2.2-1noble.20260412.030737`

Binary Packages:

- `ros-jazzy-rosidl-typesupport-cpp=3.2.2-1noble.20260412.030737`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-typesupport-cpp/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-typesupport-fastrtps-c=3.6.3-1noble.20260412.030624`

Binary Packages:

- `ros-jazzy-rosidl-typesupport-fastrtps-c=3.6.3-1noble.20260412.030624`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-typesupport-fastrtps-c/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-typesupport-fastrtps-cpp=3.6.3-1noble.20260412.030048`

Binary Packages:

- `ros-jazzy-rosidl-typesupport-fastrtps-cpp=3.6.3-1noble.20260412.030048`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-typesupport-fastrtps-cpp/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-typesupport-interface=4.6.7-1noble.20260225.225451`

Binary Packages:

- `ros-jazzy-rosidl-typesupport-interface=4.6.7-1noble.20260225.225451`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-typesupport-interface/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-typesupport-introspection-c=4.6.7-1noble.20260412.025838`

Binary Packages:

- `ros-jazzy-rosidl-typesupport-introspection-c=4.6.7-1noble.20260412.025838`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-typesupport-introspection-c/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rosidl-typesupport-introspection-cpp=4.6.7-1noble.20260412.030123`

Binary Packages:

- `ros-jazzy-rosidl-typesupport-introspection-cpp=4.6.7-1noble.20260412.030123`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rosidl-typesupport-introspection-cpp/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-rpyutils=0.4.2-1noble.20260225.142204`

Binary Packages:

- `ros-jazzy-rpyutils=0.4.2-1noble.20260225.142204`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-rpyutils/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-sensor-msgs-py=5.3.7-1noble.20260412.035802`

Binary Packages:

- `ros-jazzy-sensor-msgs-py=5.3.7-1noble.20260412.035802`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-sensor-msgs-py/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-sensor-msgs=5.3.7-1noble.20260412.034842`

Binary Packages:

- `ros-jazzy-sensor-msgs=5.3.7-1noble.20260412.034842`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-sensor-msgs/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-service-msgs=2.0.3-1noble.20260412.031935`

Binary Packages:

- `ros-jazzy-service-msgs=2.0.3-1noble.20260412.031935`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-service-msgs/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-shape-msgs=5.3.7-1noble.20260412.035632`

Binary Packages:

- `ros-jazzy-shape-msgs=5.3.7-1noble.20260412.035632`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-shape-msgs/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-spdlog-vendor=1.6.1-1noble.20260225.225958`

Binary Packages:

- `ros-jazzy-spdlog-vendor=1.6.1-1noble.20260225.225958`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-spdlog-vendor/copyright`)

- `Apache License 2.0`
- `MIT`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-sqlite3-vendor=0.26.10-2noble.20260408.222053`

Binary Packages:

- `ros-jazzy-sqlite3-vendor=0.26.10-2noble.20260408.222053`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-sqlite3-vendor/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-sros2-cmake=0.13.6-1noble.20260412.053208`

Binary Packages:

- `ros-jazzy-sros2-cmake=0.13.6-1noble.20260412.053208`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-sros2-cmake/copyright`)

- `Apache 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-sros2=0.13.6-1noble.20260412.042622`

Binary Packages:

- `ros-jazzy-sros2=0.13.6-1noble.20260412.042622`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-sros2/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-statistics-msgs=2.0.3-1noble.20260412.033131`

Binary Packages:

- `ros-jazzy-statistics-msgs=2.0.3-1noble.20260412.033131`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-statistics-msgs/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-std-msgs=5.3.7-1noble.20260412.033140`

Binary Packages:

- `ros-jazzy-std-msgs=5.3.7-1noble.20260412.033140`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-std-msgs/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-std-srvs=5.3.7-1noble.20260412.033137`

Binary Packages:

- `ros-jazzy-std-srvs=5.3.7-1noble.20260412.033137`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-std-srvs/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-stereo-msgs=5.3.7-1noble.20260412.035620`

Binary Packages:

- `ros-jazzy-stereo-msgs=5.3.7-1noble.20260412.035620`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-stereo-msgs/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-tf2-bullet=0.36.20-1noble.20260412.051516`

Binary Packages:

- `ros-jazzy-tf2-bullet=0.36.20-1noble.20260412.051516`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-tf2-bullet/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-tf2-eigen-kdl=0.36.20-1noble.20260412.040107`

Binary Packages:

- `ros-jazzy-tf2-eigen-kdl=0.36.20-1noble.20260412.040107`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-tf2-eigen-kdl/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-tf2-eigen=0.36.20-1noble.20260412.051518`

Binary Packages:

- `ros-jazzy-tf2-eigen=0.36.20-1noble.20260412.051518`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-tf2-eigen/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-tf2-geometry-msgs=0.36.20-1noble.20260412.053505`

Binary Packages:

- `ros-jazzy-tf2-geometry-msgs=0.36.20-1noble.20260412.053505`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-tf2-geometry-msgs/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-tf2-kdl=0.36.20-1noble.20260412.053442`

Binary Packages:

- `ros-jazzy-tf2-kdl=0.36.20-1noble.20260412.053442`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-tf2-kdl/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-tf2-msgs=0.36.20-1noble.20260412.034900`

Binary Packages:

- `ros-jazzy-tf2-msgs=0.36.20-1noble.20260412.034900`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-tf2-msgs/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-tf2-py=0.36.20-1noble.20260412.052955`

Binary Packages:

- `ros-jazzy-tf2-py=0.36.20-1noble.20260412.052955`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-tf2-py/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-tf2-ros-py=0.36.20-1noble.20260412.053403`

Binary Packages:

- `ros-jazzy-tf2-ros-py=0.36.20-1noble.20260412.053403`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-tf2-ros-py/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-tf2-ros=0.36.20-1noble.20260412.044056`

Binary Packages:

- `ros-jazzy-tf2-ros=0.36.20-1noble.20260412.044056`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-tf2-ros/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-tf2-sensor-msgs=0.36.20-1noble.20260412.053455`

Binary Packages:

- `ros-jazzy-tf2-sensor-msgs=0.36.20-1noble.20260412.053455`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-tf2-sensor-msgs/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-tf2-tools=0.36.20-1noble.20260412.053524`

Binary Packages:

- `ros-jazzy-tf2-tools=0.36.20-1noble.20260412.053524`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-tf2-tools/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-tf2=0.36.20-1noble.20260412.034858`

Binary Packages:

- `ros-jazzy-tf2=0.36.20-1noble.20260412.034858`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-tf2/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-tinyxml2-vendor=0.9.2-1noble.20260225.230621`

Binary Packages:

- `ros-jazzy-tinyxml2-vendor=0.9.2-1noble.20260225.230621`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-tinyxml2-vendor/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-tracetools=8.2.5-1noble.20260226.001709`

Binary Packages:

- `ros-jazzy-tracetools=8.2.5-1noble.20260226.001709`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-tracetools/copyright`)

- `Apache 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-trajectory-msgs=5.3.7-1noble.20260412.034949`

Binary Packages:

- `ros-jazzy-trajectory-msgs=5.3.7-1noble.20260412.034949`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-trajectory-msgs/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-type-description-interfaces=2.0.3-1noble.20260412.032338`

Binary Packages:

- `ros-jazzy-type-description-interfaces=2.0.3-1noble.20260412.032338`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-type-description-interfaces/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-uncrustify-vendor=3.0.1-1noble.20260225.230730`

Binary Packages:

- `ros-jazzy-uncrustify-vendor=3.0.1-1noble.20260225.230730`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-uncrustify-vendor/copyright`)

- `Apache License 2.0`
- `GNU General Public License v2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-unique-identifier-msgs=2.5.0-3noble.20260412.031407`

Binary Packages:

- `ros-jazzy-unique-identifier-msgs=2.5.0-3noble.20260412.031407`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-unique-identifier-msgs/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-urdf-parser-plugin=2.10.0-3noble.20260226.001913`

Binary Packages:

- `ros-jazzy-urdf-parser-plugin=2.10.0-3noble.20260226.001913`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-urdf-parser-plugin/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-urdf=2.10.0-3noble.20260412.025422`

Binary Packages:

- `ros-jazzy-urdf=2.10.0-3noble.20260412.025422`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-urdf/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-urdfdom-headers=1.1.2-1noble.20260225.142752`

Binary Packages:

- `ros-jazzy-urdfdom-headers=1.1.2-1noble.20260225.142752`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-urdfdom-headers/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-urdfdom=4.0.2-1noble.20260225.232653`

Binary Packages:

- `ros-jazzy-urdfdom=4.0.2-1noble.20260225.232653`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-urdfdom/copyright`)

- `BSD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-visualization-msgs=5.3.7-1noble.20260412.035359`

Binary Packages:

- `ros-jazzy-visualization-msgs=5.3.7-1noble.20260412.035359`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-visualization-msgs/copyright`)

- `Apache License 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-yaml-cpp-vendor=9.0.1-1noble.20260225.230938`

Binary Packages:

- `ros-jazzy-yaml-cpp-vendor=9.0.1-1noble.20260225.230938`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-yaml-cpp-vendor/copyright`)

- `Apache License 2.0`
- `MIT`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ros-jazzy-zstd-vendor=0.26.10-2noble.20260408.222105`

Binary Packages:

- `ros-jazzy-zstd-vendor=0.26.10-2noble.20260408.222105`

Licenses: (parsed from: `/usr/share/doc/ros-jazzy-zstd-vendor/copyright`)

- `Apache License 2.0`
- `BSD`

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
'http://archive.ubuntu.com/ubuntu/pool/main/s/setuptools/setuptools_68.1.2.orig.tar.gz' setuptools_68.1.2.orig.tar.gz 2198001 SHA256:3d4dfa6d95f1b101d695a6160a7626e15583af71a5f52176efa5d39a054d475d
'http://archive.ubuntu.com/ubuntu/pool/main/s/setuptools/setuptools_68.1.2-2ubuntu1.2.debian.tar.xz' setuptools_68.1.2-2ubuntu1.2.debian.tar.xz 17712 SHA256:535a05c43a79ba7519c1a791ba5ef75350d8e48c5b4bb8ddb7c626733a3f36b5
'http://archive.ubuntu.com/ubuntu/pool/main/s/setuptools/setuptools_68.1.2-2ubuntu1.2.dsc' setuptools_68.1.2-2ubuntu1.2.dsc 2296 SHA256:b3bdc1cbae0009f96916286d76877bbb53bb92414be9d10845b84ebb6bf99184
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
'http://archive.ubuntu.com/ubuntu/pool/main/s/shadow/shadow_4.13%2bdfsg1.orig.tar.xz' shadow_4.13+dfsg1.orig.tar.xz 1811752 SHA256:a8bb3a2aceff1cbe39d0f50687dcc1d7e7be0516a9d954d8e2eedb93f5906207
'http://archive.ubuntu.com/ubuntu/pool/main/s/shadow/shadow_4.13%2bdfsg1-4ubuntu3.2.debian.tar.xz' shadow_4.13+dfsg1-4ubuntu3.2.debian.tar.xz 96392 SHA256:ff01a3e94111ca8c4dca097ebe54edbee912cbdeba042c214bfa4c34e7839f61
'http://archive.ubuntu.com/ubuntu/pool/main/s/shadow/shadow_4.13%2bdfsg1-4ubuntu3.2.dsc' shadow_4.13+dfsg1-4ubuntu3.2.dsc 2400 SHA256:0be17fd044f3e23f714a5b286a04bd040f246af1ac32fcc406b63756baa9c368
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
- `libsqlite3-dev:amd64=3.45.1-1ubuntu2.5`

Licenses: (parsed from: `/usr/share/doc/libsqlite3-0/copyright`, `/usr/share/doc/libsqlite3-dev/copyright`)

- `GPL-2`
- `GPL-2+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris sqlite3=3.45.1-1ubuntu2.5
'http://archive.ubuntu.com/ubuntu/pool/main/s/sqlite3/sqlite3_3.45.1.orig-www.tar.xz' sqlite3_3.45.1.orig-www.tar.xz 5693812 SHA256:79b60798195a024d447e661e5bbc1eb40af50387ebf840e6f581190cc02064b6
'http://archive.ubuntu.com/ubuntu/pool/main/s/sqlite3/sqlite3_3.45.1.orig.tar.xz' sqlite3_3.45.1.orig.tar.xz 8257884 SHA256:e32e817f7b4166a301f60b14a711871bfab7d35c1d7e29b585dfc479ae150aa4
'http://archive.ubuntu.com/ubuntu/pool/main/s/sqlite3/sqlite3_3.45.1-1ubuntu2.5.debian.tar.xz' sqlite3_3.45.1-1ubuntu2.5.debian.tar.xz 35260 SHA256:b8f41cb7843f513934307d07047b185c316c3a72c650eaece0926e02d1dfc377
'http://archive.ubuntu.com/ubuntu/pool/main/s/sqlite3/sqlite3_3.45.1-1ubuntu2.5.dsc' sqlite3_3.45.1-1ubuntu2.5.dsc 2601 SHA256:6816e069bf0306f294001e1ed0ee578a272baced39c7afe4151053ab069a70b4
```

### `dpkg` source package: `sudo=1.9.15p5-3ubuntu5.24.04.2`

Binary Packages:

- `sudo=1.9.15p5-3ubuntu5.24.04.2`

Licenses: (parsed from: `/usr/share/doc/sudo/copyright`)

- `BSD-2-Clause`
- `BSD-3-Clause`
- `GPL-2`
- `GPL-2+`
- `ISC`
- `Zlib`
- `other`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris sudo=1.9.15p5-3ubuntu5.24.04.2
'http://archive.ubuntu.com/ubuntu/pool/main/s/sudo/sudo_1.9.15p5.orig.tar.gz' sudo_1.9.15p5.orig.tar.gz 5306611 SHA256:558d10b9a1991fb3b9fa7fa7b07ec4405b7aefb5b3cb0b0871dbc81e3a88e558
'http://archive.ubuntu.com/ubuntu/pool/main/s/sudo/sudo_1.9.15p5.orig.tar.gz.asc' sudo_1.9.15p5.orig.tar.gz.asc 833 SHA256:ca030b4dc43915f0802311384e6cdeae030a765ad51ca116d9d022893eb8e35e
'http://archive.ubuntu.com/ubuntu/pool/main/s/sudo/sudo_1.9.15p5-3ubuntu5.24.04.2.debian.tar.xz' sudo_1.9.15p5-3ubuntu5.24.04.2.debian.tar.xz 71516 SHA256:20813d44820701a71acfdc693018f303dd43e61357b89cbda5892645c769a335
'http://archive.ubuntu.com/ubuntu/pool/main/s/sudo/sudo_1.9.15p5-3ubuntu5.24.04.2.dsc' sudo_1.9.15p5-3ubuntu5.24.04.2.dsc 2763 SHA256:958c187c118c684aeb455afa3b49309e9c609d854f1fb702780a025d8be7450a
```

### `dpkg` source package: `systemd=255.4-1ubuntu8.15`

Binary Packages:

- `libsystemd0:amd64=255.4-1ubuntu8.15`
- `libudev1:amd64=255.4-1ubuntu8.15`

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
$ apt-get source -qq --print-uris systemd=255.4-1ubuntu8.15
'http://archive.ubuntu.com/ubuntu/pool/main/s/systemd/systemd_255.4.orig.tar.gz' systemd_255.4.orig.tar.gz 14952427 SHA256:96e75bd08c57ad401677456fb88ef54a9f05bb1695693013bc6ecce839640fd5
'http://archive.ubuntu.com/ubuntu/pool/main/s/systemd/systemd_255.4-1ubuntu8.15.debian.tar.xz' systemd_255.4-1ubuntu8.15.debian.tar.xz 264648 SHA256:0e63b049e745afdeec38be8ea086c1969c568ef704df48bf6ffebaeba5a7d618
'http://archive.ubuntu.com/ubuntu/pool/main/s/systemd/systemd_255.4-1ubuntu8.15.dsc' systemd_255.4-1ubuntu8.15.dsc 7324 SHA256:0037037654eaf11e527954282b92daad1285140313da25abdb4507bcebebe087
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


### `dpkg` source package: `tiff=4.5.1+git230720-4ubuntu2.5`

Binary Packages:

- `libtiff6:amd64=4.5.1+git230720-4ubuntu2.5`

Licenses: (parsed from: `/usr/share/doc/libtiff6/copyright`)

- `Hylafax`

Source:

```console
$ apt-get source -qq --print-uris tiff=4.5.1+git230720-4ubuntu2.5
'http://archive.ubuntu.com/ubuntu/pool/main/t/tiff/tiff_4.5.1%2bgit230720.orig.tar.xz' tiff_4.5.1+git230720.orig.tar.xz 1781896 SHA256:0e51bcf3a3ffa5fc76ea6aeb74a797f95c84544fcc8b6a1ec5def967a78e9e12
'http://archive.ubuntu.com/ubuntu/pool/main/t/tiff/tiff_4.5.1%2bgit230720-4ubuntu2.5.debian.tar.xz' tiff_4.5.1+git230720-4ubuntu2.5.debian.tar.xz 33152 SHA256:e3106320d41790b741b0db9a7fccf72b6a8d425743b6407e9a9dd369d958be76
'http://archive.ubuntu.com/ubuntu/pool/main/t/tiff/tiff_4.5.1%2bgit230720-4ubuntu2.5.dsc' tiff_4.5.1+git230720-4ubuntu2.5.dsc 2309 SHA256:46e2765124bce104413733352d548117c5e9cee73953758a2040df613f3d6b9c
```

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
'http://archive.ubuntu.com/ubuntu/pool/main/t/tzdata/tzdata_2026a.orig.tar.gz' tzdata_2026a.orig.tar.gz 471812 SHA256:77b541725937bb53bd92bd484c0b43bec8545e2d3431ee01f04ef8f2203ba2b7
'http://archive.ubuntu.com/ubuntu/pool/main/t/tzdata/tzdata_2026a.orig.tar.gz.asc' tzdata_2026a.orig.tar.gz.asc 833 SHA256:39525413908f3c28cd80dff718fc3a47a563871fd26ca3b526db2b5f700de3cb
'http://archive.ubuntu.com/ubuntu/pool/main/t/tzdata/tzdata_2026a-0ubuntu0.24.04.1.debian.tar.xz' tzdata_2026a-0ubuntu0.24.04.1.debian.tar.xz 188416 SHA256:31c2e4fa4da6dd0579e2b6172d3e30123e909d37742be6eda71b2819d0e78ad8
'http://archive.ubuntu.com/ubuntu/pool/main/t/tzdata/tzdata_2026a-0ubuntu0.24.04.1.dsc' tzdata_2026a-0ubuntu0.24.04.1.dsc 2728 SHA256:e6c10889a33dba55bcf422dc2fc4d2635d29b95eb366fd88e2017c0ba1503f88
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
'http://archive.ubuntu.com/ubuntu/pool/main/u/unminimize/unminimize_0.2.1.tar.xz' unminimize_0.2.1.tar.xz 9400 SHA256:f15f4c1df275fa116024ea1142730f524cc552da1222effeec981aebc04f7461
'http://archive.ubuntu.com/ubuntu/pool/main/u/unminimize/unminimize_0.2.1.dsc' unminimize_0.2.1.dsc 1554 SHA256:04cec314558830aba7f2c0a47fc156875c083db3f711d5525bea25a9a26fb638
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
'http://archive.ubuntu.com/ubuntu/pool/main/u/util-linux/util-linux_2.39.3.orig.tar.xz' util-linux_2.39.3.orig.tar.xz 8526168 SHA256:7b6605e48d1a49f43cc4b4cfc59f313d0dd5402fa40b96810bd572e167dfed0f
'http://archive.ubuntu.com/ubuntu/pool/main/u/util-linux/util-linux_2.39.3-9ubuntu6.5.debian.tar.xz' util-linux_2.39.3-9ubuntu6.5.debian.tar.xz 148016 SHA256:e0130fe89b648a42710af003c965f9622707c69045aab442d17e028e232f105c
'http://archive.ubuntu.com/ubuntu/pool/main/u/util-linux/util-linux_2.39.3-9ubuntu6.5.dsc' util-linux_2.39.3-9ubuntu6.5.dsc 4726 SHA256:206b6fb92d3cb0f6b1a959a6173d81ebf4e0a340564378ac49667a16968578d8
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


### `dpkg` source package: `xorg=1:7.7+23ubuntu3`

Binary Packages:

- `x11-common=1:7.7+23ubuntu3`

Licenses: (parsed from: `/usr/share/doc/x11-common/copyright`)

- `GPL`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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
- `xz-utils=5.6.1+really5.4.5-1ubuntu0.2`

Licenses: (parsed from: `/usr/share/doc/liblzma5/copyright`, `/usr/share/doc/xz-utils/copyright`)

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
'http://archive.ubuntu.com/ubuntu/pool/main/x/xz-utils/xz-utils_5.6.1%2breally5.4.5.orig.tar.xz' xz-utils_5.6.1+really5.4.5.orig.tar.xz 1680520 SHA256:da9dec6c12cf2ecf269c31ab65b5de18e8e52b96f35d5bcd08c12b43e6878803
'http://archive.ubuntu.com/ubuntu/pool/main/x/xz-utils/xz-utils_5.6.1%2breally5.4.5-1ubuntu0.2.debian.tar.xz' xz-utils_5.6.1+really5.4.5-1ubuntu0.2.debian.tar.xz 30776 SHA256:fcf6b1a987c3c82a4382b2f17a194aa9fbb1a05f307a00baf253307b10bf5ca8
'http://archive.ubuntu.com/ubuntu/pool/main/x/xz-utils/xz-utils_5.6.1%2breally5.4.5-1ubuntu0.2.dsc' xz-utils_5.6.1+really5.4.5-1ubuntu0.2.dsc 2639 SHA256:72f961b40534c1254edf0950e1826635c1aaae72f2aaa588423d833374307396
```

### `dpkg` source package: `yaml-cpp=0.8.0+dfsg-6build1`

Binary Packages:

- `libyaml-cpp-dev:amd64=0.8.0+dfsg-6build1`
- `libyaml-cpp0.8:amd64=0.8.0+dfsg-6build1`

Licenses: (parsed from: `/usr/share/doc/libyaml-cpp-dev/copyright`, `/usr/share/doc/libyaml-cpp0.8/copyright`)

- `GPL-2`
- `GPL-2.0+`
- `X11`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `zlib=1:1.3.dfsg-3.1ubuntu2.1`

Binary Packages:

- `zlib1g:amd64=1:1.3.dfsg-3.1ubuntu2.1`
- `zlib1g-dev:amd64=1:1.3.dfsg-3.1ubuntu2.1`

Licenses: (parsed from: `/usr/share/doc/zlib1g/copyright`, `/usr/share/doc/zlib1g-dev/copyright`)

- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris zlib=1:1.3.dfsg-3.1ubuntu2.1
'http://archive.ubuntu.com/ubuntu/pool/main/z/zlib/zlib_1.3.dfsg.orig.tar.xz' zlib_1.3.dfsg.orig.tar.xz 1128572 SHA256:5eea0322c1c21c75cad3b607ac1c43ff5c71e014b8ac4a34300b5e2b80d02e70
'http://archive.ubuntu.com/ubuntu/pool/main/z/zlib/zlib_1.3.dfsg-3.1ubuntu2.1.debian.tar.xz' zlib_1.3.dfsg-3.1ubuntu2.1.debian.tar.xz 61028 SHA256:958c7031c02f894516492954153c8d760d94e20a4039e48ca7231880b913ae26
'http://archive.ubuntu.com/ubuntu/pool/main/z/zlib/zlib_1.3.dfsg-3.1ubuntu2.1.dsc' zlib_1.3.dfsg-3.1ubuntu2.1.dsc 3116 SHA256:d083d6e1eb6f7f0dc5b107b0cc6b898f097947e1317769553f1c5c5d71ea5073
```
