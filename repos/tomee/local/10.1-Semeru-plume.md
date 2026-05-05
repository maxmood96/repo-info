# `tomee:10.1.4-jre25-Semeru-ubuntu-plume`

## Docker Metadata

- Image ID: `sha256:6431c58f5ff20e785a717f7746cb6027ce17c5a6b55cc058a3b206f7a74e41d7`
- Created: `2026-05-01T00:14:59.889409624Z`
- Virtual Size: ~ 413.73 Mb  
  (total size of all layers on-disk)
- Arch: `linux`/`amd64`
- Command: `["catalina.sh","run"]`
- Environment:
  - `PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin`
  - `LANG=en_US.UTF-8`
  - `LANGUAGE=en_US:en`
  - `LC_ALL=en_US.UTF-8`
  - `JAVA_VERSION=25.0.3.0`
  - `JAVA_HOME=/opt/java/openjdk`
  - `JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal`
  - `TOMEE_VER=10.1.4`
  - `TOMEE_BUILD=plume`
- Labels:
  - `org.opencontainers.image.version=22.04`

## `dpkg` (`.deb`-based packages)

### `dpkg` source package: `acl=2.3.1-1`

Binary Packages:

- `libacl1:amd64=2.3.1-1`

Licenses: (parsed from: `/usr/share/doc/libacl1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2+`
- `LGPL-2.1`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/acl/2.3.1-1/


### `dpkg` source package: `adduser=3.118ubuntu5`

Binary Packages:

- `adduser=3.118ubuntu5`

Licenses: (parsed from: `/usr/share/doc/adduser/copyright`)

- `GPL-2`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `apt=2.4.14`

Binary Packages:

- `apt=2.4.14`
- `libapt-pkg6.0:amd64=2.4.14`

Licenses: (parsed from: `/usr/share/doc/apt/copyright`, `/usr/share/doc/libapt-pkg6.0/copyright`)

- `GPL-2`
- `GPLv2+`

Source:

```console
$ apt-get source -qq --print-uris apt=2.4.14
'http://archive.ubuntu.com/ubuntu/pool/main/a/apt/apt_2.4.14.tar.xz' apt_2.4.14.tar.xz 2323176 SHA256:8d1b2748a6b5c99c9fd56dfadde280b85616dd67d22f7ca44f86225fa688a98c
'http://archive.ubuntu.com/ubuntu/pool/main/a/apt/apt_2.4.14.dsc' apt_2.4.14.dsc 2801 SHA256:317040c4ab15f20cc77460126fd78745814a81d73a6c37d0559876977a7dfe35
```

### `dpkg` source package: `attr=1:2.5.1-1build1`

Binary Packages:

- `libattr1:amd64=1:2.5.1-1build1`

Licenses: (parsed from: `/usr/share/doc/libattr1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2+`
- `LGPL-2.1`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `audit=1:3.0.7-1build1`

Binary Packages:

- `libaudit-common=1:3.0.7-1build1`
- `libaudit1:amd64=1:3.0.7-1build1`

Licenses: (parsed from: `/usr/share/doc/libaudit-common/copyright`, `/usr/share/doc/libaudit1/copyright`)

- `GPL-1`
- `GPL-2`
- `LGPL-2.1`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `base-files=12ubuntu4.7`

Binary Packages:

- `base-files=12ubuntu4.7`

Licenses: (parsed from: `/usr/share/doc/base-files/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris base-files=12ubuntu4.7
'http://archive.ubuntu.com/ubuntu/pool/main/b/base-files/base-files_12ubuntu4.7.tar.xz' base-files_12ubuntu4.7.tar.xz 81888 SHA256:000a3d5f46f1e1cc5379a8cb1b6461cff55f150b4847576d4f1f6e4ad628fdce
'http://archive.ubuntu.com/ubuntu/pool/main/b/base-files/base-files_12ubuntu4.7.dsc' base-files_12ubuntu4.7.dsc 1277 SHA256:cb8a669fec06f514fef89be1df6ef2e8b439197a6a962c3e1675be1fbe90dc3e
```

### `dpkg` source package: `base-passwd=3.5.52build1`

Binary Packages:

- `base-passwd=3.5.52build1`

Licenses: (parsed from: `/usr/share/doc/base-passwd/copyright`)

- `GPL-2`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `bash=5.1-6ubuntu1.1`

Binary Packages:

- `bash=5.1-6ubuntu1.1`

Licenses: (parsed from: `/usr/share/doc/bash/copyright`)

- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris bash=5.1-6ubuntu1.1
'http://archive.ubuntu.com/ubuntu/pool/main/b/bash/bash_5.1.orig.tar.xz' bash_5.1.orig.tar.xz 5802740 SHA256:d5eeee4f953c09826409d572e2e8996a2140d67eb8f382ce1f3a9d23883ad696
'http://archive.ubuntu.com/ubuntu/pool/main/b/bash/bash_5.1-6ubuntu1.1.debian.tar.xz' bash_5.1-6ubuntu1.1.debian.tar.xz 99944 SHA256:32332a77dedfbeee4deae3a435e07a9377a117d8326120abe0b26b92c60f5404
'http://archive.ubuntu.com/ubuntu/pool/main/b/bash/bash_5.1-6ubuntu1.1.dsc' bash_5.1-6ubuntu1.1.dsc 2409 SHA256:5c35c7efb7cfb6cfcaaaa4825ca7227151d434b4ff18b0ca88441c9f6dc9ba4e
```

### `dpkg` source package: `brotli=1.0.9-2build6`

Binary Packages:

- `libbrotli1:amd64=1.0.9-2build6`

Licenses: (parsed from: `/usr/share/doc/libbrotli1/copyright`)

- `MIT`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `bzip2=1.0.8-5build1`

Binary Packages:

- `libbz2-1.0:amd64=1.0.8-5build1`

Licenses: (parsed from: `/usr/share/doc/libbz2-1.0/copyright`)

- `BSD-variant`
- `GPL-2`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ca-certificates=20240203~22.04.1`

Binary Packages:

- `ca-certificates=20240203~22.04.1`

Licenses: (parsed from: `/usr/share/doc/ca-certificates/copyright`)

- `GPL-2`
- `GPL-2+`
- `MPL-2.0`

Source:

```console
$ apt-get source -qq --print-uris ca-certificates=20240203~22.04.1
'http://archive.ubuntu.com/ubuntu/pool/main/c/ca-certificates/ca-certificates_20240203%7e22.04.1.tar.xz' ca-certificates_20240203~22.04.1.tar.xz 263132 SHA256:1b2e51618421eb9375f2453156174b1addbaa91287567ef166c2554e2e78a17f
'http://archive.ubuntu.com/ubuntu/pool/main/c/ca-certificates/ca-certificates_20240203%7e22.04.1.dsc' ca-certificates_20240203~22.04.1.dsc 1850 SHA256:7a3f07d20b3488cbdeb8ee03a81dcb7b4b3e608f73dbf6774de705a9cd7e451b
```

### `dpkg` source package: `cdebconf=0.261ubuntu1`

Binary Packages:

- `libdebconfclient0:amd64=0.261ubuntu1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `coreutils=8.32-4.1ubuntu1.3`

Binary Packages:

- `coreutils=8.32-4.1ubuntu1.3`

Licenses: (parsed from: `/usr/share/doc/coreutils/copyright`)

- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris coreutils=8.32-4.1ubuntu1.3
'http://archive.ubuntu.com/ubuntu/pool/main/c/coreutils/coreutils_8.32.orig.tar.xz' coreutils_8.32.orig.tar.xz 5547836 SHA256:4458d8de7849df44ccab15e16b1548b285224dbba5f08fac070c1c0e0bcc4cfa
'http://archive.ubuntu.com/ubuntu/pool/main/c/coreutils/coreutils_8.32-4.1ubuntu1.3.debian.tar.xz' coreutils_8.32-4.1ubuntu1.3.debian.tar.xz 45556 SHA256:5ff54161038e479c904042f8848e40b40f5330bc4e4f2df9a474974f3d466061
'http://archive.ubuntu.com/ubuntu/pool/main/c/coreutils/coreutils_8.32-4.1ubuntu1.3.dsc' coreutils_8.32-4.1ubuntu1.3.dsc 2027 SHA256:26959de3887a535d7929e5f3ac18eab6eaba5f221cdcf3b4cf7b43c68d32f92b
```

### `dpkg` source package: `curl=7.81.0-1ubuntu1.23`

Binary Packages:

- `curl=7.81.0-1ubuntu1.23`
- `libcurl4:amd64=7.81.0-1ubuntu1.23`

Licenses: (parsed from: `/usr/share/doc/curl/copyright`, `/usr/share/doc/libcurl4/copyright`)

- `BSD-3-Clause`
- `BSD-4-Clause`
- `ISC`
- `curl`
- `other`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `cyrus-sasl2=2.1.27+dfsg2-3ubuntu1.2`

Binary Packages:

- `libsasl2-2:amd64=2.1.27+dfsg2-3ubuntu1.2`
- `libsasl2-modules-db:amd64=2.1.27+dfsg2-3ubuntu1.2`

Licenses: (parsed from: `/usr/share/doc/libsasl2-2/copyright`, `/usr/share/doc/libsasl2-modules-db/copyright`)

- `BSD-2-clause`
- `BSD-2.2-clause`
- `BSD-3-clause`
- `BSD-3-clause-JANET`
- `BSD-3-clause-PADL`
- `BSD-4-clause`
- `BSD-4-clause-UC`
- `FSFULLR`
- `GPL-3`
- `GPL-3+`
- `IBM-as-is`
- `MIT-CMU`
- `MIT-Export`
- `MIT-OpenVision`
- `OpenLDAP`
- `OpenSSL`
- `RSA-MD`
- `SSLeay`

Source:

```console
$ apt-get source -qq --print-uris cyrus-sasl2=2.1.27+dfsg2-3ubuntu1.2
'http://archive.ubuntu.com/ubuntu/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.27%2bdfsg2.orig.tar.xz' cyrus-sasl2_2.1.27+dfsg2.orig.tar.xz 829892 SHA256:f3d90671718e7dc1d46db7ccbad548d60ffe1edd1e9a620e5d3b779e6a0a9326
'http://archive.ubuntu.com/ubuntu/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.27%2bdfsg2-3ubuntu1.2.debian.tar.xz' cyrus-sasl2_2.1.27+dfsg2-3ubuntu1.2.debian.tar.xz 98836 SHA256:1b152ebdeb96d901f801d286e4d3e5e78bcf262d4d3b9c937c216770aeaeb262
'http://archive.ubuntu.com/ubuntu/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.27%2bdfsg2-3ubuntu1.2.dsc' cyrus-sasl2_2.1.27+dfsg2-3ubuntu1.2.dsc 3626 SHA256:f6afc91de318eda0251bcc8eb668d32d0db40e77d921ee57fd17dbcafb63e7ba
```

### `dpkg` source package: `dash=0.5.11+git20210903+057cd650a4ed-3build1`

Binary Packages:

- `dash=0.5.11+git20210903+057cd650a4ed-3build1`

Licenses: (parsed from: `/usr/share/doc/dash/copyright`)

- `BSD-3-Clause`
- `BSD-3-clause`
- `Expat`
- `FSFUL`
- `FSFULLR`
- `GPL-2`
- `GPL-2+`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `db5.3=5.3.28+dfsg1-0.8ubuntu3`

Binary Packages:

- `libdb5.3:amd64=5.3.28+dfsg1-0.8ubuntu3`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `debconf=1.5.79ubuntu1`

Binary Packages:

- `debconf=1.5.79ubuntu1`

Licenses: (parsed from: `/usr/share/doc/debconf/copyright`)

- `BSD-2-clause`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `debianutils=5.5-1ubuntu2`

Binary Packages:

- `debianutils=5.5-1ubuntu2`

Licenses: (parsed from: `/usr/share/doc/debianutils/copyright`)

- `GPL-2`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `diffutils=1:3.8-0ubuntu2`

Binary Packages:

- `diffutils=1:3.8-0ubuntu2`

Licenses: (parsed from: `/usr/share/doc/diffutils/copyright`)

- `GFDL`
- `GPL`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `dpkg=1.21.1ubuntu2.6`

Binary Packages:

- `dpkg=1.21.1ubuntu2.6`

Licenses: (parsed from: `/usr/share/doc/dpkg/copyright`)

- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`
- `public-domain-md5`
- `public-domain-s-s-d`

Source:

```console
$ apt-get source -qq --print-uris dpkg=1.21.1ubuntu2.6
'http://archive.ubuntu.com/ubuntu/pool/main/d/dpkg/dpkg_1.21.1ubuntu2.6.tar.xz' dpkg_1.21.1ubuntu2.6.tar.xz 5017128 SHA256:f66de0b3430a5545699361168824976acfa85f1308f00dde5bc35f39e15e2d02
'http://archive.ubuntu.com/ubuntu/pool/main/d/dpkg/dpkg_1.21.1ubuntu2.6.dsc' dpkg_1.21.1ubuntu2.6.dsc 2254 SHA256:45e8b9e16206bc27ebe1d6a0363c36135dd40c40d6105a8bb92258693f6822e8
```

### `dpkg` source package: `e2fsprogs=1.46.5-2ubuntu1.2`

Binary Packages:

- `e2fsprogs=1.46.5-2ubuntu1.2`
- `libcom-err2:amd64=1.46.5-2ubuntu1.2`
- `libext2fs2:amd64=1.46.5-2ubuntu1.2`
- `libss2:amd64=1.46.5-2ubuntu1.2`
- `logsave=1.46.5-2ubuntu1.2`

Licenses: (parsed from: `/usr/share/doc/e2fsprogs/copyright`, `/usr/share/doc/libcom-err2/copyright`, `/usr/share/doc/libext2fs2/copyright`, `/usr/share/doc/libss2/copyright`, `/usr/share/doc/logsave/copyright`)

- `GPL-2`
- `LGPL-2`

Source:

```console
$ apt-get source -qq --print-uris e2fsprogs=1.46.5-2ubuntu1.2
'http://archive.ubuntu.com/ubuntu/pool/main/e/e2fsprogs/e2fsprogs_1.46.5.orig.tar.gz' e2fsprogs_1.46.5.orig.tar.gz 9530158 SHA256:b7430d1e6b7b5817ce8e36d7c8c7c3249b3051d0808a96ffd6e5c398e4e2fbb9
'http://archive.ubuntu.com/ubuntu/pool/main/e/e2fsprogs/e2fsprogs_1.46.5.orig.tar.gz.asc' e2fsprogs_1.46.5.orig.tar.gz.asc 488 SHA256:b1e248ed73d4d67ac0cf7760e780e0a5cd2db85bbb9a5dcc235538b596128916
'http://archive.ubuntu.com/ubuntu/pool/main/e/e2fsprogs/e2fsprogs_1.46.5-2ubuntu1.2.debian.tar.xz' e2fsprogs_1.46.5-2ubuntu1.2.debian.tar.xz 86604 SHA256:b04fad2b12787628497127e6fab76de11c54229e08a406eba126df13f5224fdf
'http://archive.ubuntu.com/ubuntu/pool/main/e/e2fsprogs/e2fsprogs_1.46.5-2ubuntu1.2.dsc' e2fsprogs_1.46.5-2ubuntu1.2.dsc 3190 SHA256:6f41e832d3e69bff96374f20e886a286f6dd8cfff68c1f0fc902281ed365560a
```

### `dpkg` source package: `expat=2.4.7-1ubuntu0.7`

Binary Packages:

- `libexpat1:amd64=2.4.7-1ubuntu0.7`

Licenses: (parsed from: `/usr/share/doc/libexpat1/copyright`)

- `MIT`

Source:

```console
$ apt-get source -qq --print-uris expat=2.4.7-1ubuntu0.7
'http://archive.ubuntu.com/ubuntu/pool/main/e/expat/expat_2.4.7.orig.tar.gz' expat_2.4.7.orig.tar.gz 8316374 SHA256:ddc1111651cdd4095b67c9d9ed46babfb8fb64843d89ff785399f5739b84867b
'http://archive.ubuntu.com/ubuntu/pool/main/e/expat/expat_2.4.7-1ubuntu0.7.debian.tar.xz' expat_2.4.7-1ubuntu0.7.debian.tar.xz 37472 SHA256:20cc871a48373cafec06dd008798afcd891946f319254ac5a9f9c958456f09e6
'http://archive.ubuntu.com/ubuntu/pool/main/e/expat/expat_2.4.7-1ubuntu0.7.dsc' expat_2.4.7-1ubuntu0.7.dsc 1962 SHA256:b385c2614d9729d641b14b8cb3e95efb3a0a9afaa4dca23cebc75a792653c911
```

### `dpkg` source package: `findutils=4.8.0-1ubuntu3`

Binary Packages:

- `findutils=4.8.0-1ubuntu3`

Licenses: (parsed from: `/usr/share/doc/findutils/copyright`)

- `GFDL-1.3`
- `GPL-3`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `fontconfig=2.13.1-4.2ubuntu5`

Binary Packages:

- `fontconfig=2.13.1-4.2ubuntu5`
- `fontconfig-config=2.13.1-4.2ubuntu5`
- `libfontconfig1:amd64=2.13.1-4.2ubuntu5`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `fonts-dejavu=2.37-2build1`

Binary Packages:

- `fonts-dejavu-core=2.37-2build1`

Licenses: (parsed from: `/usr/share/doc/fonts-dejavu-core/copyright`)

- `GPL-2`
- `GPL-2+`
- `bitstream-vera`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `freetype=2.11.1+dfsg-1ubuntu0.3`

Binary Packages:

- `libfreetype6:amd64=2.11.1+dfsg-1ubuntu0.3`

Licenses: (parsed from: `/usr/share/doc/libfreetype6/copyright`)

- `BSD-3-Clause`
- `BSL-1.0`
- `FSFAP`
- `FTL`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `MIT`
- `OpenGroup-BSD-like`
- `Public-Domain`
- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris freetype=2.11.1+dfsg-1ubuntu0.3
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.11.1%2bdfsg.orig-ft2demos.tar.xz' freetype_2.11.1+dfsg.orig-ft2demos.tar.xz 257240 SHA256:c60620d49d0f16d95586eb868c01b129569409e6cfdcb87a78e0482a12604672
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.11.1%2bdfsg.orig-ft2demos.tar.xz.asc' freetype_2.11.1+dfsg.orig-ft2demos.tar.xz.asc 195 SHA256:d911a95830c50efcf60398e51db4ec307bbf4d24168377b515aded0611e977c0
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.11.1%2bdfsg.orig-ft2docs.tar.xz' freetype_2.11.1+dfsg.orig-ft2docs.tar.xz 2038348 SHA256:755e29908093c19138a38775784b0accf7e838ffa28a25b8722b3dfe651d80fa
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.11.1%2bdfsg.orig-ft2docs.tar.xz.asc' freetype_2.11.1+dfsg.orig-ft2docs.tar.xz.asc 195 SHA256:67cbc2f192460dc4d46129e7debe55b40a9fa6e224ffeed70b4cf397ebaccab5
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.11.1%2bdfsg.orig.tar.xz' freetype_2.11.1+dfsg.orig.tar.xz 1988020 SHA256:ef93541237834445eb7ff355e7d4139d48844f9c977a485dea1316df54994473
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.11.1%2bdfsg-1ubuntu0.3.debian.tar.xz' freetype_2.11.1+dfsg-1ubuntu0.3.debian.tar.xz 42292 SHA256:06de0e18b9ba09bbe576c2941784fe2c08cee498fdcc6d15b0e42eea92637e83
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.11.1%2bdfsg-1ubuntu0.3.dsc' freetype_2.11.1+dfsg-1ubuntu0.3.dsc 3791 SHA256:6048c3a9985b597d1964ca07e38deaaed6fdf743d39cf88d17887604e480dab8
```

### `dpkg` source package: `gcc-12=12.3.0-1ubuntu1~22.04.3`

Binary Packages:

- `gcc-12-base:amd64=12.3.0-1ubuntu1~22.04.3`
- `libgcc-s1:amd64=12.3.0-1ubuntu1~22.04.3`
- `libstdc++6:amd64=12.3.0-1ubuntu1~22.04.3`

Licenses: (parsed from: `/usr/share/doc/gcc-12-base/copyright`, `/usr/share/doc/libgcc-s1/copyright`, `/usr/share/doc/libstdc++6/copyright`)

- `Artistic`
- `GFDL-1.2`
- `GPL`
- `GPL-2`
- `GPL-3`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris gcc-12=12.3.0-1ubuntu1~22.04.3
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-12/gcc-12_12.3.0.orig.tar.gz' gcc-12_12.3.0.orig.tar.gz 91555468 SHA256:62b0fc89b6d41f9df2470d0fb4995f6ff5885f910518a2c6a44a6888ea5a9ea1
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-12/gcc-12_12.3.0-1ubuntu1%7e22.04.3.debian.tar.xz' gcc-12_12.3.0-1ubuntu1~22.04.3.debian.tar.xz 587456 SHA256:44074c3d5e7d97365f1f7b45291ade2ee40ed6300176530d912e7cc0ceba77ab
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-12/gcc-12_12.3.0-1ubuntu1%7e22.04.3.dsc' gcc-12_12.3.0-1ubuntu1~22.04.3.dsc 27845 SHA256:ec040a1fa94186bd53535f7156e086e67863bb55836ae7fd7fef64f1ab66b04d
```

### `dpkg` source package: `glibc=2.35-0ubuntu3.13`

Binary Packages:

- `libc-bin=2.35-0ubuntu3.13`
- `libc6:amd64=2.35-0ubuntu3.13`
- `locales=2.35-0ubuntu3.13`

Licenses: (parsed from: `/usr/share/doc/libc-bin/copyright`, `/usr/share/doc/libc6/copyright`, `/usr/share/doc/locales/copyright`)

- `GFDL-1.3`
- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris glibc=2.35-0ubuntu3.13
'http://archive.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.35.orig.tar.xz' glibc_2.35.orig.tar.xz 18165952 SHA256:5123732f6b67ccd319305efd399971d58592122bcc2a6518a1bd2510dd0cf52e
'http://archive.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.35.orig.tar.xz.asc' glibc_2.35.orig.tar.xz.asc 833 SHA256:853aaaf17d7366817e814057a467625ee7c0b26240e8b878db0f33c389c7bcb6
'http://archive.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.35-0ubuntu3.13.debian.tar.xz' glibc_2.35-0ubuntu3.13.debian.tar.xz 943368 SHA256:28173285cf885df068374baf9b513ede397988ea3f93a1377f0268fe257a62f4
'http://archive.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.35-0ubuntu3.13.dsc' glibc_2.35-0ubuntu3.13.dsc 8758 SHA256:b8e7304bc899913294f1f1a2b2633f84f3ea93208f8da1a33e1340c4ad06e359
```

### `dpkg` source package: `gmp=2:6.2.1+dfsg-3ubuntu1`

Binary Packages:

- `libgmp10:amd64=2:6.2.1+dfsg-3ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libgmp10/copyright`)

- `GPL`
- `GPL-2`
- `GPL-3`
- `LGPL-3`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `gnupg2=2.2.27-3ubuntu2.5`

Binary Packages:

- `dirmngr=2.2.27-3ubuntu2.5`
- `gpg=2.2.27-3ubuntu2.5`
- `gpg-agent=2.2.27-3ubuntu2.5`
- `gpgconf=2.2.27-3ubuntu2.5`
- `gpgv=2.2.27-3ubuntu2.5`

Licenses: (parsed from: `/usr/share/doc/dirmngr/copyright`, `/usr/share/doc/gpg/copyright`, `/usr/share/doc/gpg-agent/copyright`, `/usr/share/doc/gpgconf/copyright`, `/usr/share/doc/gpgv/copyright`)

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
$ apt-get source -qq --print-uris gnupg2=2.2.27-3ubuntu2.5
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnupg2/gnupg2_2.2.27.orig.tar.bz2' gnupg2_2.2.27.orig.tar.bz2 7191555 SHA256:34e60009014ea16402069136e0a5f63d9b65f90096244975db5cea74b3d02399
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnupg2/gnupg2_2.2.27-3ubuntu2.5.debian.tar.xz' gnupg2_2.2.27-3ubuntu2.5.debian.tar.xz 76672 SHA256:63239842abfe155bf3b0be202446a807a202a25f85257bc0331292602eb39666
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnupg2/gnupg2_2.2.27-3ubuntu2.5.dsc' gnupg2_2.2.27-3ubuntu2.5.dsc 3763 SHA256:1fb5930a84f846fec8322e6c32544ebb8118d618bbb175c1d38722def6f0d461
```

### `dpkg` source package: `gnutls28=3.7.3-4ubuntu1.8`

Binary Packages:

- `libgnutls30:amd64=3.7.3-4ubuntu1.8`

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
$ apt-get source -qq --print-uris gnutls28=3.7.3-4ubuntu1.8
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.7.3.orig.tar.xz' gnutls28_3.7.3.orig.tar.xz 6119292 SHA256:fc59c43bc31ab20a6977ff083029277a31935b8355ce387b634fa433f8f6c49a
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.7.3.orig.tar.xz.asc' gnutls28_3.7.3.orig.tar.xz.asc 833 SHA256:a2f95ac5d7dd951bddef01ec9930616dd1a5226173b3dc7896b3bed411c91d9a
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.7.3-4ubuntu1.8.debian.tar.xz' gnutls28_3.7.3-4ubuntu1.8.debian.tar.xz 109652 SHA256:c93f629fea192f758e8f28dd664310eedd5c926a5617278251e6428297c53a1e
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.7.3-4ubuntu1.8.dsc' gnutls28_3.7.3-4ubuntu1.8.dsc 3575 SHA256:96c27046146d8e3d4641d161126f53cc62f330e8234ac8efa8fcb90747356772
```

### `dpkg` source package: `grep=3.7-1build1`

Binary Packages:

- `grep=3.7-1build1`

Licenses: (parsed from: `/usr/share/doc/grep/copyright`)

- `GPL-3`
- `GPL-3+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `gzip=1.10-4ubuntu4.1`

Binary Packages:

- `gzip=1.10-4ubuntu4.1`

Licenses: (parsed from: `/usr/share/doc/gzip/copyright`)

- `FSF-manpages`
- `GFDL-1.3+-no-invariant`
- `GFDL-3`
- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris gzip=1.10-4ubuntu4.1
'http://archive.ubuntu.com/ubuntu/pool/main/g/gzip/gzip_1.10.orig.tar.gz' gzip_1.10.orig.tar.gz 1201421 SHA256:c91f74430bf7bc20402e1f657d0b252cb80aa66ba333a25704512af346633c68
'http://archive.ubuntu.com/ubuntu/pool/main/g/gzip/gzip_1.10.orig.tar.gz.asc' gzip_1.10.orig.tar.gz.asc 833 SHA256:b5e4942cca901ca37772d3ea060c4af6a1908719cec5327fbe033f9d30933f1b
'http://archive.ubuntu.com/ubuntu/pool/main/g/gzip/gzip_1.10-4ubuntu4.1.debian.tar.xz' gzip_1.10-4ubuntu4.1.debian.tar.xz 39520 SHA256:35a9967c2ab73e620fffad4cca6f65183dc83024aae4866cea92a1f26c8b6232
'http://archive.ubuntu.com/ubuntu/pool/main/g/gzip/gzip_1.10-4ubuntu4.1.dsc' gzip_1.10-4ubuntu4.1.dsc 2277 SHA256:ecdfb40e6271b4895e9b108be68d47d9b164903cdae7b8400478e1047adfd34e
```

### `dpkg` source package: `hostname=3.23ubuntu2`

Binary Packages:

- `hostname=3.23ubuntu2`

Licenses: (parsed from: `/usr/share/doc/hostname/copyright`)

- `GPL-2`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `init-system-helpers=1.62`

Binary Packages:

- `init-system-helpers=1.62`

Licenses: (parsed from: `/usr/share/doc/init-system-helpers/copyright`)

- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/init-system-helpers/1.62/


### `dpkg` source package: `keyutils=1.6.1-2ubuntu3`

Binary Packages:

- `libkeyutils1:amd64=1.6.1-2ubuntu3`

Licenses: (parsed from: `/usr/share/doc/libkeyutils1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2`
- `LGPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `krb5=1.19.2-2ubuntu0.7`

Binary Packages:

- `libgssapi-krb5-2:amd64=1.19.2-2ubuntu0.7`
- `libk5crypto3:amd64=1.19.2-2ubuntu0.7`
- `libkrb5-3:amd64=1.19.2-2ubuntu0.7`
- `libkrb5support0:amd64=1.19.2-2ubuntu0.7`

Licenses: (parsed from: `/usr/share/doc/libgssapi-krb5-2/copyright`, `/usr/share/doc/libk5crypto3/copyright`, `/usr/share/doc/libkrb5-3/copyright`, `/usr/share/doc/libkrb5support0/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris krb5=1.19.2-2ubuntu0.7
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.19.2.orig.tar.gz' krb5_1.19.2.orig.tar.gz 8741053 SHA256:10453fee4e3a8f8ce6129059e5c050b8a65dab1c257df68b99b3112eaa0cdf6a
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.19.2-2ubuntu0.7.debian.tar.xz' krb5_1.19.2-2ubuntu0.7.debian.tar.xz 124844 SHA256:b7e94dfecde73a4a79e7433fd8723851ad8886635d568fe99796f812a4fbc463
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.19.2-2ubuntu0.7.dsc' krb5_1.19.2-2ubuntu0.7.dsc 3697 SHA256:c987b71948299427d2f46ea0c64c9ebd9e5d06a55e6362839f77ee3c7adbd6ca
```

### `dpkg` source package: `libassuan=2.5.5-1build1`

Binary Packages:

- `libassuan0:amd64=2.5.5-1build1`

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


### `dpkg` source package: `libcap-ng=0.7.9-2.2build3`

Binary Packages:

- `libcap-ng0:amd64=0.7.9-2.2build3`

Licenses: (parsed from: `/usr/share/doc/libcap-ng0/copyright`)

- `GPL-2`
- `GPL-3`
- `LGPL-2.1`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libcap2=1:2.44-1ubuntu0.22.04.2`

Binary Packages:

- `libcap2:amd64=1:2.44-1ubuntu0.22.04.2`

Licenses: (parsed from: `/usr/share/doc/libcap2/copyright`)

- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libffi=3.4.2-4`

Binary Packages:

- `libffi8:amd64=3.4.2-4`

Licenses: (parsed from: `/usr/share/doc/libffi8/copyright`)

- `GPL`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/libffi/3.4.2-4/


### `dpkg` source package: `libgcrypt20=1.9.4-3ubuntu3`

Binary Packages:

- `libgcrypt20:amd64=1.9.4-3ubuntu3`

Licenses: (parsed from: `/usr/share/doc/libgcrypt20/copyright`)

- `GPL-2`
- `LGPL`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libgpg-error=1.43-3`

Binary Packages:

- `libgpg-error0:amd64=1.43-3`

Licenses: (parsed from: `/usr/share/doc/libgpg-error0/copyright`)

- `BSD-3-clause`
- `GPL-3`
- `GPL-3+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `g10-permissive`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/libgpg-error/1.43-3/


### `dpkg` source package: `libidn2=2.3.2-2build1`

Binary Packages:

- `libidn2-0:amd64=2.3.2-2build1`

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


### `dpkg` source package: `libksba=1.6.0-2ubuntu0.2`

Binary Packages:

- `libksba8:amd64=1.6.0-2ubuntu0.2`

Licenses: (parsed from: `/usr/share/doc/libksba8/copyright`)

- `FSFUL`
- `GPL-3`
- `LGPL-2.1-or-later`

Source:

```console
$ apt-get source -qq --print-uris libksba=1.6.0-2ubuntu0.2
'http://archive.ubuntu.com/ubuntu/pool/main/libk/libksba/libksba_1.6.0.orig.tar.bz2' libksba_1.6.0.orig.tar.bz2 662120 SHA256:dad683e6f2d915d880aa4bed5cea9a115690b8935b78a1bbe01669189307a48b
'http://archive.ubuntu.com/ubuntu/pool/main/libk/libksba/libksba_1.6.0.orig.tar.bz2.asc' libksba_1.6.0.orig.tar.bz2.asc 228 SHA256:c695098f67cc837071d899f0e15d993bcf29eaac8f1ca7428ee793d9c62c795c
'http://archive.ubuntu.com/ubuntu/pool/main/libk/libksba/libksba_1.6.0-2ubuntu0.2.debian.tar.xz' libksba_1.6.0-2ubuntu0.2.debian.tar.xz 16004 SHA256:51f00b01877995ccd56fc056cd5d50f9b5f676f0359385d4a4298c012203307f
'http://archive.ubuntu.com/ubuntu/pool/main/libk/libksba/libksba_1.6.0-2ubuntu0.2.dsc' libksba_1.6.0-2ubuntu0.2.dsc 2585 SHA256:d113abd41140b8f60638f31058674494053f4432fe15ef7da24b95627fc6a809
```

### `dpkg` source package: `libnsl=1.3.0-2build2`

Binary Packages:

- `libnsl2:amd64=1.3.0-2build2`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libpng1.6=1.6.37-3ubuntu0.4`

Binary Packages:

- `libpng16-16:amd64=1.6.37-3ubuntu0.4`

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
$ apt-get source -qq --print-uris libpng1.6=1.6.37-3ubuntu0.4
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpng1.6/libpng1.6_1.6.37.orig.tar.gz' libpng1.6_1.6.37.orig.tar.gz 1508805 SHA256:ca74a0dace179a8422187671aee97dd3892b53e168627145271cad5b5ac81307
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpng1.6/libpng1.6_1.6.37-3ubuntu0.4.debian.tar.xz' libpng1.6_1.6.37-3ubuntu0.4.debian.tar.xz 40160 SHA256:11dc3b351ccfe56c336dd3794d870453fce1c3cde0131e6ad4c6fdc6c4f655be
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpng1.6/libpng1.6_1.6.37-3ubuntu0.4.dsc' libpng1.6_1.6.37-3ubuntu0.4.dsc 2340 SHA256:74492c0a2d4b08be8592eb27aa021093b2eedf7276a326d7a5cf5106ce9a775a
```

### `dpkg` source package: `libpsl=0.21.0-1.2build2`

Binary Packages:

- `libpsl5:amd64=0.21.0-1.2build2`

Licenses: (parsed from: `/usr/share/doc/libpsl5/copyright`)

- `Chromium`
- `MIT`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libseccomp=2.5.3-2ubuntu3~22.04.1`

Binary Packages:

- `libseccomp2:amd64=2.5.3-2ubuntu3~22.04.1`

Licenses: (parsed from: `/usr/share/doc/libseccomp2/copyright`)

- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libseccomp=2.5.3-2ubuntu3~22.04.1
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libseccomp/libseccomp_2.5.3.orig.tar.gz' libseccomp_2.5.3.orig.tar.gz 637572 SHA256:59065c8733364725e9721ba48c3a99bbc52af921daf48df4b1e012fbc7b10a76
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libseccomp/libseccomp_2.5.3.orig.tar.gz.asc' libseccomp_2.5.3.orig.tar.gz.asc 833 SHA256:cc1cbe9d9eb6a67b78de107eb37b2bc8d7599e3c1d36699ae2528db489cb5d44
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libseccomp/libseccomp_2.5.3-2ubuntu3%7e22.04.1.debian.tar.xz' libseccomp_2.5.3-2ubuntu3~22.04.1.debian.tar.xz 24328 SHA256:cd582c847ced99c97f487b3f4a851bc1f2bed9065f90729d90dc8721b6dc483e
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libseccomp/libseccomp_2.5.3-2ubuntu3%7e22.04.1.dsc' libseccomp_2.5.3-2ubuntu3~22.04.1.dsc 2860 SHA256:e7f514056a28794c6a7067cd0881b5bf03e918578df3418eea6752cbfa83fd13
```

### `dpkg` source package: `libselinux=3.3-1build2`

Binary Packages:

- `libselinux1:amd64=3.3-1build2`

Licenses: (parsed from: `/usr/share/doc/libselinux1/copyright`)

- `GPL-2`
- `LGPL-2.1`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libsemanage=3.3-1build2`

Binary Packages:

- `libsemanage-common=3.3-1build2`
- `libsemanage2:amd64=3.3-1build2`

Licenses: (parsed from: `/usr/share/doc/libsemanage-common/copyright`, `/usr/share/doc/libsemanage2/copyright`)

- `GPL`
- `LGPL`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libsepol=3.3-1build1`

Binary Packages:

- `libsepol2:amd64=3.3-1build1`

Licenses: (parsed from: `/usr/share/doc/libsepol2/copyright`)

- `GPL`
- `LGPL`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libssh=0.9.6-2ubuntu0.22.04.7`

Binary Packages:

- `libssh-4:amd64=0.9.6-2ubuntu0.22.04.7`

Licenses: (parsed from: `/usr/share/doc/libssh-4/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `LGPL-2.1`
- `LGPL-2.1+~OpenSSL`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris libssh=0.9.6-2ubuntu0.22.04.7
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libssh/libssh_0.9.6.orig.tar.xz' libssh_0.9.6.orig.tar.xz 1053056 SHA256:86bcf885bd9b80466fe0e05453c58b877df61afa8ba947a58c356d7f0fab829b
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libssh/libssh_0.9.6.orig.tar.xz.asc' libssh_0.9.6.orig.tar.xz.asc 833 SHA256:050d4e532a614c20b4830ebc210bb28acee2ed458e694c8aedfe2ab152688298
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libssh/libssh_0.9.6-2ubuntu0.22.04.7.debian.tar.xz' libssh_0.9.6-2ubuntu0.22.04.7.debian.tar.xz 75780 SHA256:324c4371a1c73edab635a028c0049b8e568e43014148e87c0a5b3d2e791d2295
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libssh/libssh_0.9.6-2ubuntu0.22.04.7.dsc' libssh_0.9.6-2ubuntu0.22.04.7.dsc 2750 SHA256:7068a71d241496023af2b737f04f435ef80d36bd45d28ab4c42b31f76c3b30fe
```

### `dpkg` source package: `libtasn1-6=4.18.0-4ubuntu0.2`

Binary Packages:

- `libtasn1-6:amd64=4.18.0-4ubuntu0.2`

Licenses: (parsed from: `/usr/share/doc/libtasn1-6/copyright`)

- `GFDL-1.3`
- `GPL-3`
- `LGPL`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libtasn1-6=4.18.0-4ubuntu0.2
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtasn1-6/libtasn1-6_4.18.0.orig.tar.gz' libtasn1-6_4.18.0.orig.tar.gz 1724441 SHA256:4365c154953563d64c67a024b607d1ee75c6db76e0d0f65709ea80a334cd1898
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtasn1-6/libtasn1-6_4.18.0.orig.tar.gz.asc' libtasn1-6_4.18.0.orig.tar.gz.asc 228 SHA256:68edccaf988071e0c0154495e82be0b783553a49762381435accc79f2fdb463d
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtasn1-6/libtasn1-6_4.18.0-4ubuntu0.2.debian.tar.xz' libtasn1-6_4.18.0-4ubuntu0.2.debian.tar.xz 25324 SHA256:450340a2e588e4fcbfcbf2eece3c516a3fc25f6606e0fa341155326ab72137a0
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtasn1-6/libtasn1-6_4.18.0-4ubuntu0.2.dsc' libtasn1-6_4.18.0-4ubuntu0.2.dsc 2777 SHA256:959cc5799f608a5ddc7aba7fcc765588b5dc82c7d987bd17a4274222a5171d41
```

### `dpkg` source package: `libtirpc=1.3.2-2ubuntu0.1`

Binary Packages:

- `libtirpc-common=1.3.2-2ubuntu0.1`
- `libtirpc3:amd64=1.3.2-2ubuntu0.1`

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
$ apt-get source -qq --print-uris libtirpc=1.3.2-2ubuntu0.1
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtirpc/libtirpc_1.3.2.orig.tar.bz2' libtirpc_1.3.2.orig.tar.bz2 513151 SHA256:e24eb88b8ce7db3b7ca6eb80115dd1284abc5ec32a8deccfed2224fc2532b9fd
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtirpc/libtirpc_1.3.2-2ubuntu0.1.debian.tar.xz' libtirpc_1.3.2-2ubuntu0.1.debian.tar.xz 18364 SHA256:9e280f94501b63ba7e753f7bb71c1394f2615073e5022a1136632d32780027f8
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtirpc/libtirpc_1.3.2-2ubuntu0.1.dsc' libtirpc_1.3.2-2ubuntu0.1.dsc 2201 SHA256:082cce0086a92b4a2fef61bc5318b332b5cbedcafda5654faf51ed6c5b611533
```

### `dpkg` source package: `libunistring=1.0-1`

Binary Packages:

- `libunistring2:amd64=1.0-1`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/libunistring/1.0-1/


### `dpkg` source package: `libxcrypt=1:4.4.27-1`

Binary Packages:

- `libcrypt1:amd64=1:4.4.27-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/libxcrypt/1:4.4.27-1/


### `dpkg` source package: `libzstd=1.4.8+dfsg-3build1`

Binary Packages:

- `libzstd1:amd64=1.4.8+dfsg-3build1`

Licenses: (parsed from: `/usr/share/doc/libzstd1/copyright`)

- `BSD-3-clause`
- `Expat`
- `GPL-2`
- `zlib`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `lsb=11.1.0ubuntu4`

Binary Packages:

- `lsb-base=11.1.0ubuntu4`

Licenses: (parsed from: `/usr/share/doc/lsb-base/copyright`)

- `BSD-3-clause`
- `GPL-2`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `lz4=1.9.3-2build2`

Binary Packages:

- `liblz4-1:amd64=1.9.3-2build2`

Licenses: (parsed from: `/usr/share/doc/liblz4-1/copyright`)

- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `mawk=1.3.4.20200120-3`

Binary Packages:

- `mawk=1.3.4.20200120-3`

Licenses: (parsed from: `/usr/share/doc/mawk/copyright`)

- `GPL-2`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/mawk/1.3.4.20200120-3/


### `dpkg` source package: `ncurses=6.3-2ubuntu0.1`

Binary Packages:

- `libncurses6:amd64=6.3-2ubuntu0.1`
- `libncursesw6:amd64=6.3-2ubuntu0.1`
- `libtinfo6:amd64=6.3-2ubuntu0.1`
- `ncurses-base=6.3-2ubuntu0.1`
- `ncurses-bin=6.3-2ubuntu0.1`

Licenses: (parsed from: `/usr/share/doc/libncurses6/copyright`, `/usr/share/doc/libncursesw6/copyright`, `/usr/share/doc/libtinfo6/copyright`, `/usr/share/doc/ncurses-base/copyright`, `/usr/share/doc/ncurses-bin/copyright`)

- `BSD-3-clause`
- `MIT/X11`
- `X11`

Source:

```console
$ apt-get source -qq --print-uris ncurses=6.3-2ubuntu0.1
'http://archive.ubuntu.com/ubuntu/pool/main/n/ncurses/ncurses_6.3.orig.tar.gz' ncurses_6.3.orig.tar.gz 3583550 SHA256:97fc51ac2b085d4cde31ef4d2c3122c21abc217e9090a43a30fc5ec21684e059
'http://archive.ubuntu.com/ubuntu/pool/main/n/ncurses/ncurses_6.3.orig.tar.gz.asc' ncurses_6.3.orig.tar.gz.asc 729 SHA256:37b9e80c11fa02fbd8caf42ab9573427f54f2c7212eb4aeec9f455b5d79dee14
'http://archive.ubuntu.com/ubuntu/pool/main/n/ncurses/ncurses_6.3-2ubuntu0.1.debian.tar.xz' ncurses_6.3-2ubuntu0.1.debian.tar.xz 56080 SHA256:ca221fdf0d4a987b9719985a8c7a6e603a7ef8f855cdfaefe73b56c08130064a
'http://archive.ubuntu.com/ubuntu/pool/main/n/ncurses/ncurses_6.3-2ubuntu0.1.dsc' ncurses_6.3-2ubuntu0.1.dsc 3955 SHA256:ece6823e39b4c104937c90a26a54cef143b22916cee062d842a7356fa3bbe324
```

### `dpkg` source package: `nettle=3.7.3-1build2`

Binary Packages:

- `libhogweed6:amd64=3.7.3-1build2`
- `libnettle8:amd64=3.7.3-1build2`

Licenses: (parsed from: `/usr/share/doc/libhogweed6/copyright`, `/usr/share/doc/libnettle8/copyright`)

- `Expat`
- `GAP`
- `GPL`
- `GPL-2`
- `GPL-2+`
- `GPL-3+`
- `GPL-3+ with Autoconf exception`
- `LGPL`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-3+`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `nghttp2=1.43.0-1ubuntu0.2`

Binary Packages:

- `libnghttp2-14:amd64=1.43.0-1ubuntu0.2`

Licenses: (parsed from: `/usr/share/doc/libnghttp2-14/copyright`)

- `BSD-2-clause`
- `Expat`
- `GPL-3`
- `GPL-3+ with autoconf exception`
- `MIT`
- `SIL-OFL-1.1`
- `all-permissive`

Source:

```console
$ apt-get source -qq --print-uris nghttp2=1.43.0-1ubuntu0.2
'http://archive.ubuntu.com/ubuntu/pool/main/n/nghttp2/nghttp2_1.43.0.orig.tar.bz2' nghttp2_1.43.0.orig.tar.bz2 4521786 SHA256:556f24653397c71ebb8270b3c5e5507f0893e6eac2c6eeda6be2ecf6e1f50f62
'http://archive.ubuntu.com/ubuntu/pool/main/n/nghttp2/nghttp2_1.43.0-1ubuntu0.2.debian.tar.xz' nghttp2_1.43.0-1ubuntu0.2.debian.tar.xz 23788 SHA256:4517ea82d0a218a4a4c870724f9498b88bf3d8971113ebc746bf24a0df12af22
'http://archive.ubuntu.com/ubuntu/pool/main/n/nghttp2/nghttp2_1.43.0-1ubuntu0.2.dsc' nghttp2_1.43.0-1ubuntu0.2.dsc 2679 SHA256:44f56bd7ce62011d772fecdc39f0513e28bb8ac00fe8068e1f3a154e9bfd6c5b
```

### `dpkg` source package: `npth=1.6-3build2`

Binary Packages:

- `libnpth0:amd64=1.6-3build2`

Licenses: (parsed from: `/usr/share/doc/libnpth0/copyright`)

- `LGPL-2.1`
- `LGPL-2.1+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `openldap=2.5.20+dfsg-0ubuntu0.22.04.1`

Binary Packages:

- `libldap-2.5-0:amd64=2.5.20+dfsg-0ubuntu0.22.04.1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris openldap=2.5.20+dfsg-0ubuntu0.22.04.1
'http://archive.ubuntu.com/ubuntu/pool/main/o/openldap/openldap_2.5.20%2bdfsg.orig.tar.gz' openldap_2.5.20+dfsg.orig.tar.gz 5626931 SHA256:97d81c83e9d6278aee5a923cf8cd56d5b6447d1295c4f1ef7b28c43b95740525
'http://archive.ubuntu.com/ubuntu/pool/main/o/openldap/openldap_2.5.20%2bdfsg-0ubuntu0.22.04.1.debian.tar.xz' openldap_2.5.20+dfsg-0ubuntu0.22.04.1.debian.tar.xz 178364 SHA256:0b4bcc1c310064bc60c7521d9097ff0dcb80156a72aab4010c6437ee9600c57d
'http://archive.ubuntu.com/ubuntu/pool/main/o/openldap/openldap_2.5.20%2bdfsg-0ubuntu0.22.04.1.dsc' openldap_2.5.20+dfsg-0ubuntu0.22.04.1.dsc 3473 SHA256:e9eaccd861fbbe1671f408deddf02f4658ac5c98cd04a755fcd41f9860609da0
```

### `dpkg` source package: `openssl=3.0.2-0ubuntu1.23`

Binary Packages:

- `libssl3:amd64=3.0.2-0ubuntu1.23`
- `openssl=3.0.2-0ubuntu1.23`

Licenses: (parsed from: `/usr/share/doc/libssl3/copyright`, `/usr/share/doc/openssl/copyright`)

- `Apache-2.0`
- `Artistic`
- `GPL-1`
- `GPL-1+`

Source:

```console
$ apt-get source -qq --print-uris openssl=3.0.2-0ubuntu1.23
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssl/openssl_3.0.2.orig.tar.gz' openssl_3.0.2.orig.tar.gz 15038141 SHA512:f986850d5be908b4d6b5fd7091bc4652d7378c9bccebfbc5becd7753843c04c1eb61a1749c432139d263dfac33df0b1f6c773664b485cad47542266823a4eb03
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssl/openssl_3.0.2.orig.tar.gz.asc' openssl_3.0.2.orig.tar.gz.asc 488 SHA512:4303391a58107c76ad9b05510f5bfc95f687f4cb2f9ff5b03fb262ba99b573423ab83f0437471199954496799b343191b889ad9ef8fabdd7ee4ec3ec9b5f1d81
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssl/openssl_3.0.2-0ubuntu1.23.debian.tar.xz' openssl_3.0.2-0ubuntu1.23.debian.tar.xz 277852 SHA512:1de5b111ad19a4d0400c2195574737293a83a23d4f79ca44e86f09e8438f879d29888be39455f7483fdaf8a9314841ffb9511ace908813e7f849c4d98af53562
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssl/openssl_3.0.2-0ubuntu1.23.dsc' openssl_3.0.2-0ubuntu1.23.dsc 2730 SHA512:63c782499d5cee71f4d999ae0581c3b1f3ccc6f68b0147e1e3487c2dcd43e83c420b9a3d9bbf305ec6ed39f7dfc73e2386c2a5d89adc46878d8a36dd53d1d431
```

### `dpkg` source package: `p11-kit=0.24.0-6build1`

Binary Packages:

- `libp11-kit0:amd64=0.24.0-6build1`

Licenses: (parsed from: `/usr/share/doc/libp11-kit0/copyright`)

- `Apache-2.0`
- `BSD-3-Clause`
- `ISC`
- `ISC+IBM`
- `LGPL-2.1`
- `LGPL-2.1+`
- `permissive-like-automake-output`
- `same-as-rest-of-p11kit`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `pam=1.4.0-11ubuntu2.6`

Binary Packages:

- `libpam-modules:amd64=1.4.0-11ubuntu2.6`
- `libpam-modules-bin=1.4.0-11ubuntu2.6`
- `libpam-runtime=1.4.0-11ubuntu2.6`
- `libpam0g:amd64=1.4.0-11ubuntu2.6`

Licenses: (parsed from: `/usr/share/doc/libpam-modules/copyright`, `/usr/share/doc/libpam-modules-bin/copyright`, `/usr/share/doc/libpam-runtime/copyright`, `/usr/share/doc/libpam0g/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris pam=1.4.0-11ubuntu2.6
'http://archive.ubuntu.com/ubuntu/pool/main/p/pam/pam_1.4.0.orig.tar.xz' pam_1.4.0.orig.tar.xz 988908 SHA256:cd6d928c51e64139be3bdb38692c68183a509b83d4f2c221024ccd4bcddfd034
'http://archive.ubuntu.com/ubuntu/pool/main/p/pam/pam_1.4.0-11ubuntu2.6.debian.tar.xz' pam_1.4.0-11ubuntu2.6.debian.tar.xz 187648 SHA256:3c39973311d521677a9e35994eedf22fe24d0fc1da39f31abeeaab82eb3674f8
'http://archive.ubuntu.com/ubuntu/pool/main/p/pam/pam_1.4.0-11ubuntu2.6.dsc' pam_1.4.0-11ubuntu2.6.dsc 2728 SHA256:3a3ad2fc2206083b7b8b143e1adc904cb5399ba1be9067a749332194d87cbd47
```

### `dpkg` source package: `pcre2=10.39-3ubuntu0.1`

Binary Packages:

- `libpcre2-8-0:amd64=10.39-3ubuntu0.1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris pcre2=10.39-3ubuntu0.1
'http://archive.ubuntu.com/ubuntu/pool/main/p/pcre2/pcre2_10.39.orig.tar.gz' pcre2_10.39.orig.tar.gz 2309964 SHA256:0781bd2536ef5279b1943471fdcdbd9961a2845e1d2c9ad849b9bd98ba1a9bd4
'http://archive.ubuntu.com/ubuntu/pool/main/p/pcre2/pcre2_10.39-3ubuntu0.1.diff.gz' pcre2_10.39-3ubuntu0.1.diff.gz 11214 SHA256:cce22d08265cc8d322281242f555044a62302d4df9b0fa44c8c4536819dae47d
'http://archive.ubuntu.com/ubuntu/pool/main/p/pcre2/pcre2_10.39-3ubuntu0.1.dsc' pcre2_10.39-3ubuntu0.1.dsc 2142 SHA256:f78f76a3e7d1ebbe1f03df40211ffd4922337c7f7848097c399befb620a0a471
```

### `dpkg` source package: `pcre3=2:8.39-13ubuntu0.22.04.1`

Binary Packages:

- `libpcre3:amd64=2:8.39-13ubuntu0.22.04.1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris pcre3=2:8.39-13ubuntu0.22.04.1
'http://archive.ubuntu.com/ubuntu/pool/main/p/pcre3/pcre3_8.39.orig.tar.bz2' pcre3_8.39.orig.tar.bz2 1560758 SHA256:b858099f82483031ee02092711689e7245586ada49e534a06e678b8ea9549e8b
'http://archive.ubuntu.com/ubuntu/pool/main/p/pcre3/pcre3_8.39-13ubuntu0.22.04.1.debian.tar.gz' pcre3_8.39-13ubuntu0.22.04.1.debian.tar.gz 28251 SHA256:b6542e9adae20f212637f133e892c1d6874d9a21af928ed4cbd94fb77133916e
'http://archive.ubuntu.com/ubuntu/pool/main/p/pcre3/pcre3_8.39-13ubuntu0.22.04.1.dsc' pcre3_8.39-13ubuntu0.22.04.1.dsc 2101 SHA256:f9c1a08a5856eee3644a4f5bbffe62ff04d21940ebd7798e7b15f48463571867
```

### `dpkg` source package: `perl=5.34.0-3ubuntu1.5`

Binary Packages:

- `perl-base=5.34.0-3ubuntu1.5`

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
$ apt-get source -qq --print-uris perl=5.34.0-3ubuntu1.5
'http://archive.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.34.0.orig-regen-configure.tar.xz' perl_5.34.0.orig-regen-configure.tar.xz 415412 SHA256:b168f566401fdccc13d0616c258854c1e1a461276922babca617097cd9dfd85b
'http://archive.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.34.0.orig.tar.xz' perl_5.34.0.orig.tar.xz 12881416 SHA256:82c2e5e5c71b0e10487a80d79140469ab1f8056349ca8545140a224dbbed7ded
'http://archive.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.34.0-3ubuntu1.5.debian.tar.xz' perl_5.34.0-3ubuntu1.5.debian.tar.xz 200524 SHA256:b299fde16bfd7405e40d8afdeab05027be11a6fb409ac020f2052d079f0b1f54
'http://archive.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.34.0-3ubuntu1.5.dsc' perl_5.34.0-3ubuntu1.5.dsc 2976 SHA256:9e51731910bdc4c1aacbeda30d22b6f2daf015fc8601b5a5c6f518cda19150b2
```

### `dpkg` source package: `pinentry=1.1.1-1build2`

Binary Packages:

- `pinentry-curses=1.1.1-1build2`

Licenses: (parsed from: `/usr/share/doc/pinentry-curses/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-3`
- `LGPL-3+`
- `X11`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `procps=2:3.3.17-6ubuntu2.1`

Binary Packages:

- `libprocps8:amd64=2:3.3.17-6ubuntu2.1`
- `procps=2:3.3.17-6ubuntu2.1`

Licenses: (parsed from: `/usr/share/doc/libprocps8/copyright`, `/usr/share/doc/procps/copyright`)

- `GPL-2`
- `GPL-2.0+`
- `LGPL-2`
- `LGPL-2.0+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris procps=2:3.3.17-6ubuntu2.1
'http://archive.ubuntu.com/ubuntu/pool/main/p/procps/procps_3.3.17.orig.tar.xz' procps_3.3.17.orig.tar.xz 1008428 SHA256:4518b3e7aafd34ec07d0063d250fd474999b20b200218c3ae56f5d2113f141b4
'http://archive.ubuntu.com/ubuntu/pool/main/p/procps/procps_3.3.17-6ubuntu2.1.debian.tar.xz' procps_3.3.17-6ubuntu2.1.debian.tar.xz 35488 SHA256:7ecb85faef890f1f56c4e6d2eb73988b02283b32e6367a24cd006b91dfdb7979
'http://archive.ubuntu.com/ubuntu/pool/main/p/procps/procps_3.3.17-6ubuntu2.1.dsc' procps_3.3.17-6ubuntu2.1.dsc 2111 SHA256:2160554b394a265e1be8fe668ea15955ccbb89c5ccf8f53ea2b3f38abb3e2d93
```

### `dpkg` source package: `readline=8.1.2-1`

Binary Packages:

- `libreadline8:amd64=8.1.2-1`
- `readline-common=8.1.2-1`

Licenses: (parsed from: `/usr/share/doc/libreadline8/copyright`, `/usr/share/doc/readline-common/copyright`)

- `GFDL`
- `GPL-3`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/readline/8.1.2-1/


### `dpkg` source package: `rtmpdump=2.4+20151223.gitfa8646d.1-2build4`

Binary Packages:

- `librtmp1:amd64=2.4+20151223.gitfa8646d.1-2build4`

Licenses: (parsed from: `/usr/share/doc/librtmp1/copyright`)

- `GPL-2`
- `LGPL-2.1`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `sed=4.8-1ubuntu2`

Binary Packages:

- `sed=4.8-1ubuntu2`

Licenses: (parsed from: `/usr/share/doc/sed/copyright`)

- `GPL-3`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `sensible-utils=0.0.17`

Binary Packages:

- `sensible-utils=0.0.17`

Licenses: (parsed from: `/usr/share/doc/sensible-utils/copyright`)

- `All-permissive`
- `GPL-2`
- `GPL-2+`
- `configure`
- `installsh`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/sensible-utils/0.0.17/


### `dpkg` source package: `shadow=1:4.8.1-2ubuntu2.2`

Binary Packages:

- `login=1:4.8.1-2ubuntu2.2`
- `passwd=1:4.8.1-2ubuntu2.2`

Licenses: (parsed from: `/usr/share/doc/login/copyright`, `/usr/share/doc/passwd/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris shadow=1:4.8.1-2ubuntu2.2
'http://archive.ubuntu.com/ubuntu/pool/main/s/shadow/shadow_4.8.1.orig.tar.xz' shadow_4.8.1.orig.tar.xz 1611196 SHA256:a3ad4630bdc41372f02a647278a8c3514844295d36eefe68ece6c3a641c1ae62
'http://archive.ubuntu.com/ubuntu/pool/main/s/shadow/shadow_4.8.1-2ubuntu2.2.debian.tar.xz' shadow_4.8.1-2ubuntu2.2.debian.tar.xz 98488 SHA256:7ea89214714f06a15925f6fb89de4d96a61ad5fc18bbd2ed210e7c4568f63391
'http://archive.ubuntu.com/ubuntu/pool/main/s/shadow/shadow_4.8.1-2ubuntu2.2.dsc' shadow_4.8.1-2ubuntu2.2.dsc 2060 SHA256:09708d1e384f6b9d3ff1f65aa6c05db9260050e523c9e7a99331f60a42880d61
```

### `dpkg` source package: `sqlite3=3.37.2-2ubuntu0.5`

Binary Packages:

- `libsqlite3-0:amd64=3.37.2-2ubuntu0.5`

Licenses: (parsed from: `/usr/share/doc/libsqlite3-0/copyright`)

- `GPL-2`
- `GPL-2+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris sqlite3=3.37.2-2ubuntu0.5
'http://archive.ubuntu.com/ubuntu/pool/main/s/sqlite3/sqlite3_3.37.2.orig-www.tar.xz' sqlite3_3.37.2.orig-www.tar.xz 5694016 SHA256:63dbd1c7abab37ec5beed22dae75bac048efead0f19aa5cad49b4bd690335ebd
'http://archive.ubuntu.com/ubuntu/pool/main/s/sqlite3/sqlite3_3.37.2.orig.tar.xz' sqlite3_3.37.2.orig.tar.xz 7623768 SHA256:3157723da779963f7887f29de12289a4890f0c18eb17b570aa2c8d2c96d31d6f
'http://archive.ubuntu.com/ubuntu/pool/main/s/sqlite3/sqlite3_3.37.2-2ubuntu0.5.debian.tar.xz' sqlite3_3.37.2-2ubuntu0.5.debian.tar.xz 33900 SHA256:6ab1d798854f14fc298ac3cfc11ceb95081511721238d73ea60d075427717dc9
'http://archive.ubuntu.com/ubuntu/pool/main/s/sqlite3/sqlite3_3.37.2-2ubuntu0.5.dsc' sqlite3_3.37.2-2ubuntu0.5.dsc 2602 SHA256:c3fdde2feb1d2e12d0dd88674d854542878e612ad68a264ce0a9dcba45f31fe8
```

### `dpkg` source package: `systemd=249.11-0ubuntu3.20`

Binary Packages:

- `libsystemd0:amd64=249.11-0ubuntu3.20`
- `libudev1:amd64=249.11-0ubuntu3.20`

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
$ apt-get source -qq --print-uris systemd=249.11-0ubuntu3.20
'http://archive.ubuntu.com/ubuntu/pool/main/s/systemd/systemd_249.11.orig.tar.gz' systemd_249.11.orig.tar.gz 10622702 SHA256:305ba81cc33593bc2e8e9d6dc7f964b1c0a9303155fced5e6b1d236577441bf2
'http://archive.ubuntu.com/ubuntu/pool/main/s/systemd/systemd_249.11-0ubuntu3.20.debian.tar.xz' systemd_249.11-0ubuntu3.20.debian.tar.xz 268300 SHA256:5ee6145eb25c4a8b2419da5f146a22f9ae46f3e37af9acc90c73ee7424b8f8d6
'http://archive.ubuntu.com/ubuntu/pool/main/s/systemd/systemd_249.11-0ubuntu3.20.dsc' systemd_249.11-0ubuntu3.20.dsc 5907 SHA256:8f7b24a4b0f18fdf74fe35a20bba8ac10d71f6418792015bb19d9fe235f80cb6
```

### `dpkg` source package: `sysvinit=3.01-1ubuntu1`

Binary Packages:

- `sysvinit-utils=3.01-1ubuntu1`

Licenses: (parsed from: `/usr/share/doc/sysvinit-utils/copyright`)

- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `tar=1.34+dfsg-1ubuntu0.1.22.04.2`

Binary Packages:

- `tar=1.34+dfsg-1ubuntu0.1.22.04.2`

Licenses: (parsed from: `/usr/share/doc/tar/copyright`)

- `GPL-2`
- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris tar=1.34+dfsg-1ubuntu0.1.22.04.2
'http://archive.ubuntu.com/ubuntu/pool/main/t/tar/tar_1.34%2bdfsg.orig.tar.xz' tar_1.34+dfsg.orig.tar.xz 1981736 SHA256:7d57029540cb928394defb3b377b3531237c947e795b51aa8acac0c5ba0e4844
'http://archive.ubuntu.com/ubuntu/pool/main/t/tar/tar_1.34%2bdfsg-1ubuntu0.1.22.04.2.debian.tar.xz' tar_1.34+dfsg-1ubuntu0.1.22.04.2.debian.tar.xz 20544 SHA256:631c322d0cfcf547ac83a0cfea3324a85ef6ffe8706e51615869216d1bb970d8
'http://archive.ubuntu.com/ubuntu/pool/main/t/tar/tar_1.34%2bdfsg-1ubuntu0.1.22.04.2.dsc' tar_1.34+dfsg-1ubuntu0.1.22.04.2.dsc 1829 SHA256:8e03b501b3d49270d1b4df2db086e30ff4ea97b725b5477b34aac973ceb6f694
```

### `dpkg` source package: `tzdata=2026a-0ubuntu0.22.04.1`

Binary Packages:

- `tzdata=2026a-0ubuntu0.22.04.1`

Licenses: (parsed from: `/usr/share/doc/tzdata/copyright`)

- `ICU`

Source:

```console
$ apt-get source -qq --print-uris tzdata=2026a-0ubuntu0.22.04.1
'http://archive.ubuntu.com/ubuntu/pool/main/t/tzdata/tzdata_2026a.orig.tar.gz' tzdata_2026a.orig.tar.gz 471812 SHA256:77b541725937bb53bd92bd484c0b43bec8545e2d3431ee01f04ef8f2203ba2b7
'http://archive.ubuntu.com/ubuntu/pool/main/t/tzdata/tzdata_2026a.orig.tar.gz.asc' tzdata_2026a.orig.tar.gz.asc 833 SHA256:39525413908f3c28cd80dff718fc3a47a563871fd26ca3b526db2b5f700de3cb
'http://archive.ubuntu.com/ubuntu/pool/main/t/tzdata/tzdata_2026a-0ubuntu0.22.04.1.debian.tar.xz' tzdata_2026a-0ubuntu0.22.04.1.debian.tar.xz 181756 SHA256:26fae193bae0e8cc1905d1cf3ddfe1e12a152ef340125dee49c6c4ee1200f419
'http://archive.ubuntu.com/ubuntu/pool/main/t/tzdata/tzdata_2026a-0ubuntu0.22.04.1.dsc' tzdata_2026a-0ubuntu0.22.04.1.dsc 2541 SHA256:2eabe6ac25cbee2d15639c9c379fc79aa796cb0e08196a4442c0b77012ec9e0f
```

### `dpkg` source package: `ubuntu-keyring=2021.03.26`

Binary Packages:

- `ubuntu-keyring=2021.03.26`

Licenses: (parsed from: `/usr/share/doc/ubuntu-keyring/copyright`)

- `GPL`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ucf=3.0043`

Binary Packages:

- `ucf=3.0043`

Licenses: (parsed from: `/usr/share/doc/ucf/copyright`)

- `GPL-2`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/ucf/3.0043/


### `dpkg` source package: `usrmerge=25ubuntu2`

Binary Packages:

- `usrmerge=25ubuntu2`

Licenses: (parsed from: `/usr/share/doc/usrmerge/copyright`)

- `GPL v2`
- `GPL-2`
- `later (please see /usr/share/common-licenses/GPL-2)`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `util-linux=2.37.2-4ubuntu3.5`

Binary Packages:

- `bsdutils=1:2.37.2-4ubuntu3.5`
- `libblkid1:amd64=2.37.2-4ubuntu3.5`
- `libmount1:amd64=2.37.2-4ubuntu3.5`
- `libsmartcols1:amd64=2.37.2-4ubuntu3.5`
- `libuuid1:amd64=2.37.2-4ubuntu3.5`
- `mount=2.37.2-4ubuntu3.5`
- `util-linux=2.37.2-4ubuntu3.5`

Licenses: (parsed from: `/usr/share/doc/bsdutils/copyright`, `/usr/share/doc/libblkid1/copyright`, `/usr/share/doc/libmount1/copyright`, `/usr/share/doc/libsmartcols1/copyright`, `/usr/share/doc/libuuid1/copyright`, `/usr/share/doc/mount/copyright`, `/usr/share/doc/util-linux/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `BSD-4-clause`
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
$ apt-get source -qq --print-uris util-linux=2.37.2-4ubuntu3.5
'http://archive.ubuntu.com/ubuntu/pool/main/u/util-linux/util-linux_2.37.2.orig.tar.xz' util-linux_2.37.2.orig.tar.xz 5621624 SHA256:6a0764c1aae7fb607ef8a6dd2c0f6c47d5e5fd27aa08820abaad9ec14e28e9d9
'http://archive.ubuntu.com/ubuntu/pool/main/u/util-linux/util-linux_2.37.2-4ubuntu3.5.debian.tar.xz' util-linux_2.37.2-4ubuntu3.5.debian.tar.xz 115268 SHA256:fe69a2cc84ddcfb17a47f57b8c39c3919844bd92ef8868b40676656025f391c8
'http://archive.ubuntu.com/ubuntu/pool/main/u/util-linux/util-linux_2.37.2-4ubuntu3.5.dsc' util-linux_2.37.2-4ubuntu3.5.dsc 4550 SHA256:024c983405cf31b5ba1230c99d27fd340552c0f59e05b4d94f222d9e399ac522
```

### `dpkg` source package: `xxhash=0.8.1-1`

Binary Packages:

- `libxxhash0:amd64=0.8.1-1`

Licenses: (parsed from: `/usr/share/doc/libxxhash0/copyright`)

- `BSD-2-clause`
- `GPL-2`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/xxhash/0.8.1-1/


### `dpkg` source package: `xz-utils=5.2.5-2ubuntu1`

Binary Packages:

- `liblzma5:amd64=5.2.5-2ubuntu1`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `zlib=1:1.2.11.dfsg-2ubuntu9.2`

Binary Packages:

- `zlib1g:amd64=1:1.2.11.dfsg-2ubuntu9.2`

Licenses: (parsed from: `/usr/share/doc/zlib1g/copyright`)

- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris zlib=1:1.2.11.dfsg-2ubuntu9.2
'http://archive.ubuntu.com/ubuntu/pool/main/z/zlib/zlib_1.2.11.dfsg.orig.tar.gz' zlib_1.2.11.dfsg.orig.tar.gz 370248 SHA256:80c481411a4fe8463aeb8270149a0e80bb9eaf7da44132b6e16f2b5af01bc899
'http://archive.ubuntu.com/ubuntu/pool/main/z/zlib/zlib_1.2.11.dfsg-2ubuntu9.2.debian.tar.xz' zlib_1.2.11.dfsg-2ubuntu9.2.debian.tar.xz 60140 SHA256:5678d0b3d1e609297e5a3dedfcb3474bab1cafe82c0c29aec2cef01e49a88d39
'http://archive.ubuntu.com/ubuntu/pool/main/z/zlib/zlib_1.2.11.dfsg-2ubuntu9.2.dsc' zlib_1.2.11.dfsg-2ubuntu9.2.dsc 2649 SHA256:ac50a5e5803c128eaef7eceda71fa13ffab3ed1e949008be244d8754d9c59e47
```
