# `debian:trixie-slim`

## Docker Metadata

- Image ID: `sha256:ac7f91c70264dbf42a12bad61aae88f783e36bbf1625bc37a6167973a95ed819`
- Created: `2024-12-02T00:00:00Z`
- Virtual Size: ~ 83.91 Mb  
  (total size of all layers on-disk)
- Arch: `linux`/`amd64`
- Command: `["bash"]`
- Environment:
  - `PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin`

## `dpkg` (`.deb`-based packages)

### `dpkg` source package: `acl=2.3.2-2`

Binary Packages:

- `libacl1:amd64=2.3.2-2+b1`

Licenses: (parsed from: `/usr/share/doc/libacl1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2+`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris acl=2.3.2-2
'http://deb.debian.org/debian/pool/main/a/acl/acl_2.3.2-2.dsc' acl_2.3.2-2.dsc 2604 SHA256:1f42130ccb5442fe2db2aee1dcc03c51a31512dd2519a38e8fc9270c5abbc807
'http://deb.debian.org/debian/pool/main/a/acl/acl_2.3.2.orig.tar.xz' acl_2.3.2.orig.tar.xz 371680 SHA256:97203a72cae99ab89a067fe2210c1cbf052bc492b479eca7d226d9830883b0bd
'http://deb.debian.org/debian/pool/main/a/acl/acl_2.3.2.orig.tar.xz.asc' acl_2.3.2.orig.tar.xz.asc 833 SHA256:184c6a903490885a096095db67b433a04542c6569f167cbe8115268c0f227273
'http://deb.debian.org/debian/pool/main/a/acl/acl_2.3.2-2.debian.tar.xz' acl_2.3.2-2.debian.tar.xz 24296 SHA256:e27b6e194c0a7554595d76f96acdceb800631bdc46c36457b73bc7e4a0c5f2ee
```

Other potentially useful URLs:

- https://sources.debian.net/src/acl/2.3.2-2/ (for browsing the source)
- https://sources.debian.net/src/acl/2.3.2-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/acl/2.3.2-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `apt=2.9.14`

Binary Packages:

- `apt=2.9.14`
- `libapt-pkg6.0t64:amd64=2.9.14`

Licenses: (parsed from: `/usr/share/doc/apt/copyright`, `/usr/share/doc/libapt-pkg6.0t64/copyright`)

- `BSD-3-clause`
- `Expat`
- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/apt/2.9.14/


### `dpkg` source package: `attr=1:2.5.2-2`

Binary Packages:

- `libattr1:amd64=1:2.5.2-2`

Licenses: (parsed from: `/usr/share/doc/libattr1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2+`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris attr=1:2.5.2-2
'http://deb.debian.org/debian/pool/main/a/attr/attr_2.5.2-2.dsc' attr_2.5.2-2.dsc 2576 SHA256:814f167854daf20640bf4d83aa086135000e31f355d69711ef611235b7b999ac
'http://deb.debian.org/debian/pool/main/a/attr/attr_2.5.2.orig.tar.xz' attr_2.5.2.orig.tar.xz 334180 SHA256:f2e97b0ab7ce293681ab701915766190d607a1dba7fae8a718138150b700a70b
'http://deb.debian.org/debian/pool/main/a/attr/attr_2.5.2.orig.tar.xz.asc' attr_2.5.2.orig.tar.xz.asc 833 SHA256:eeac729088d3c6379e91b7596cb3582e46b047c47f0fa3c5c77f9c9e84dc3a4c
'http://deb.debian.org/debian/pool/main/a/attr/attr_2.5.2-2.debian.tar.xz' attr_2.5.2-2.debian.tar.xz 26592 SHA256:23c0ad870c6f6a75080d11b66e07cdb9db95805d61e218dc30f070d2f001ab9b
```

Other potentially useful URLs:

- https://sources.debian.net/src/attr/1:2.5.2-2/ (for browsing the source)
- https://sources.debian.net/src/attr/1:2.5.2-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/attr/1:2.5.2-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `audit=1:4.0.2-2`

Binary Packages:

- `libaudit-common=1:4.0.2-2`
- `libaudit1:amd64=1:4.0.2-2`

Licenses: (parsed from: `/usr/share/doc/libaudit-common/copyright`, `/usr/share/doc/libaudit1/copyright`)

- `GPL-1`
- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris audit=1:4.0.2-2
'http://deb.debian.org/debian/pool/main/a/audit/audit_4.0.2-2.dsc' audit_4.0.2-2.dsc 2408 SHA256:d0b9457933409cd3287bc0b8bfb10f41c08fb5b24bd5c5b8364125d5a6894974
'http://deb.debian.org/debian/pool/main/a/audit/audit_4.0.2.orig.tar.gz' audit_4.0.2.orig.tar.gz 1198769 SHA256:d5d1b5d50ee4a2d0d17875bc6ae6bd6a7d5b34d9557ea847a39faec531faaa0a
'http://deb.debian.org/debian/pool/main/a/audit/audit_4.0.2-2.debian.tar.xz' audit_4.0.2-2.debian.tar.xz 19228 SHA256:33030d53299c57cda73e9e45813b8488f9bc3ad8992aef0b740afabbf66a2ba2
```

Other potentially useful URLs:

- https://sources.debian.net/src/audit/1:4.0.2-2/ (for browsing the source)
- https://sources.debian.net/src/audit/1:4.0.2-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/audit/1:4.0.2-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `base-files=13.6`

Binary Packages:

- `base-files=13.6`

Licenses: (parsed from: `/usr/share/doc/base-files/copyright`)

- `GPL`
- `GPL-2+`
- `verbatim`

Source:

```console
$ apt-get source -qq --print-uris base-files=13.6
'http://deb.debian.org/debian/pool/main/b/base-files/base-files_13.6.dsc' base-files_13.6.dsc 1100 SHA256:f5fd18c61694f108b0f6fe0387d89c5eb581fb445db6253fac5f27eb26779d37
'http://deb.debian.org/debian/pool/main/b/base-files/base-files_13.6.tar.xz' base-files_13.6.tar.xz 68264 SHA256:ebe8647287f951ebf5f6ac94067a4cf14bf61752ca0ecc342245d13b1c520258
```

Other potentially useful URLs:

- https://sources.debian.net/src/base-files/13.6/ (for browsing the source)
- https://sources.debian.net/src/base-files/13.6/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/base-files/13.6/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `base-passwd=3.6.5`

Binary Packages:

- `base-passwd=3.6.5`

Licenses: (parsed from: `/usr/share/doc/base-passwd/copyright`)

- `GPL-2`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris base-passwd=3.6.5
'http://deb.debian.org/debian/pool/main/b/base-passwd/base-passwd_3.6.5.dsc' base-passwd_3.6.5.dsc 1762 SHA256:18802a37a5b32e5271e27512f3017c9aaf91497e96517fa5c586a50b03c71f6c
'http://deb.debian.org/debian/pool/main/b/base-passwd/base-passwd_3.6.5.tar.xz' base-passwd_3.6.5.tar.xz 60064 SHA256:bd30ab67b1f8029d3e70d3419e5033fb4595ab91c91307c3b7c00978e8d111b2
```

Other potentially useful URLs:

- https://sources.debian.net/src/base-passwd/3.6.5/ (for browsing the source)
- https://sources.debian.net/src/base-passwd/3.6.5/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/base-passwd/3.6.5/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `bash=5.2.32-1`

Binary Packages:

- `bash=5.2.32-1+b2`

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

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/bash/5.2.32-1/


### `dpkg` source package: `bzip2=1.0.8-6`

Binary Packages:

- `libbz2-1.0:amd64=1.0.8-6`

Licenses: (parsed from: `/usr/share/doc/libbz2-1.0/copyright`)

- `BSD-variant`
- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris bzip2=1.0.8-6
'http://deb.debian.org/debian/pool/main/b/bzip2/bzip2_1.0.8-6.dsc' bzip2_1.0.8-6.dsc 1604 SHA256:cd3bfd77254a6b5ef1be144bdc90a0dd374bc8206afd98ba4abf828741b79820
'http://deb.debian.org/debian/pool/main/b/bzip2/bzip2_1.0.8.orig.tar.gz' bzip2_1.0.8.orig.tar.gz 810029 SHA256:ab5a03176ee106d3f0fa90e381da478ddae405918153cca248e682cd0c4a2269
'http://deb.debian.org/debian/pool/main/b/bzip2/bzip2_1.0.8-6.debian.tar.bz2' bzip2_1.0.8-6.debian.tar.bz2 26991 SHA256:648ed0dac9a041ba6951e0cca521628aa39947cefee78139f7b934a5dc502095
```

Other potentially useful URLs:

- https://sources.debian.net/src/bzip2/1.0.8-6/ (for browsing the source)
- https://sources.debian.net/src/bzip2/1.0.8-6/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/bzip2/1.0.8-6/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `cdebconf=0.273`

Binary Packages:

- `libdebconfclient0:amd64=0.273`

Licenses: (parsed from: `/usr/share/doc/libdebconfclient0/copyright`)

- `BSD-2-Clause`
- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/cdebconf/0.273/


### `dpkg` source package: `coreutils=9.5-1`

Binary Packages:

- `coreutils=9.5-1+b1`

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
$ apt-get source -qq --print-uris coreutils=9.5-1
'http://deb.debian.org/debian/pool/main/c/coreutils/coreutils_9.5-1.dsc' coreutils_9.5-1.dsc 2104 SHA256:83558c321a5e7a39dcf538a5a425f03486fbd2e6d95941a17ed98d04ed5ea7af
'http://deb.debian.org/debian/pool/main/c/coreutils/coreutils_9.5.orig.tar.xz' coreutils_9.5.orig.tar.xz 6007136 SHA256:cd328edeac92f6a665de9f323c93b712af1858bc2e0d88f3f7100469470a1b8a
'http://deb.debian.org/debian/pool/main/c/coreutils/coreutils_9.5.orig.tar.xz.asc' coreutils_9.5.orig.tar.xz.asc 833 SHA256:b2843cd7c5972c7bc4d01fc34eb82e5a3ec84a199363288e3999304e3dddc805
'http://deb.debian.org/debian/pool/main/c/coreutils/coreutils_9.5-1.debian.tar.xz' coreutils_9.5-1.debian.tar.xz 21768 SHA256:fe704f7ba9b23cbc857e755bd3ec987228166b1342c1651f04bd16649b71d84d
```

Other potentially useful URLs:

- https://sources.debian.net/src/coreutils/9.5-1/ (for browsing the source)
- https://sources.debian.net/src/coreutils/9.5-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/coreutils/9.5-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `dash=0.5.12-9`

Binary Packages:

- `dash=0.5.12-9`

Licenses: (parsed from: `/usr/share/doc/dash/copyright`)

- `BSD-3-Clause`
- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris dash=0.5.12-9
'http://deb.debian.org/debian/pool/main/d/dash/dash_0.5.12-9.dsc' dash_0.5.12-9.dsc 1455 SHA256:aa5165888c75a39ec70477132329c7583863ee9762b6d07dc71fa2a5cdb84783
'http://deb.debian.org/debian/pool/main/d/dash/dash_0.5.12.orig.tar.gz' dash_0.5.12.orig.tar.gz 246054 SHA256:6a474ac46e8b0b32916c4c60df694c82058d3297d8b385b74508030ca4a8f28a
'http://deb.debian.org/debian/pool/main/d/dash/dash_0.5.12-9.debian.tar.xz' dash_0.5.12-9.debian.tar.xz 40096 SHA256:b5314d8c6cafae389559d6101dea059426263c95020ef5c547a59bcf5c0af2cc
```

Other potentially useful URLs:

- https://sources.debian.net/src/dash/0.5.12-9/ (for browsing the source)
- https://sources.debian.net/src/dash/0.5.12-9/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/dash/0.5.12-9/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/d/db5.3/db5.3_5.3.28%2bdfsg2-9.dsc' db5.3_5.3.28+dfsg2-9.dsc 2373 SHA256:045f392c75dffc9d4f3bd44978b90ca8d45b935cf0ae4202bf79a760f2ce07b1
'http://deb.debian.org/debian/pool/main/d/db5.3/db5.3_5.3.28%2bdfsg2.orig.tar.xz' db5.3_5.3.28+dfsg2.orig.tar.xz 21287688 SHA256:ad41b507415dec8316e828b2230242af2251d2c86eefa3c7aa9ef47c5239ef33
'http://deb.debian.org/debian/pool/main/d/db5.3/db5.3_5.3.28%2bdfsg2-9.debian.tar.xz' db5.3_5.3.28+dfsg2-9.debian.tar.xz 36412 SHA256:21fe6ee0491c83d0c34fe52e0e0e423946172eff68262584a0cc8ef880c36b74
```

Other potentially useful URLs:

- https://sources.debian.net/src/db5.3/5.3.28+dfsg2-9/ (for browsing the source)
- https://sources.debian.net/src/db5.3/5.3.28+dfsg2-9/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/db5.3/5.3.28+dfsg2-9/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `debconf=1.5.87`

Binary Packages:

- `debconf=1.5.87`

Licenses: (parsed from: `/usr/share/doc/debconf/copyright`)

- `BSD-2-clause`

Source:

```console
$ apt-get source -qq --print-uris debconf=1.5.87
'http://deb.debian.org/debian/pool/main/d/debconf/debconf_1.5.87.dsc' debconf_1.5.87.dsc 2035 SHA256:f46059b530efcb86082ee703225356869727e25babf9c3ad0c4a2e48f87e2977
'http://deb.debian.org/debian/pool/main/d/debconf/debconf_1.5.87.tar.xz' debconf_1.5.87.tar.xz 574232 SHA256:2b813be2ab3904a9194a07f2d97ab8e1d79c47ec2ca2f6a1f238c3cb4ff31c66
```

Other potentially useful URLs:

- https://sources.debian.net/src/debconf/1.5.87/ (for browsing the source)
- https://sources.debian.net/src/debconf/1.5.87/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/debconf/1.5.87/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `debian-archive-keyring=2023.4`

Binary Packages:

- `debian-archive-keyring=2023.4`

Licenses: (parsed from: `/usr/share/doc/debian-archive-keyring/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris debian-archive-keyring=2023.4
'http://deb.debian.org/debian/pool/main/d/debian-archive-keyring/debian-archive-keyring_2023.4.dsc' debian-archive-keyring_2023.4.dsc 1261 SHA256:c97d048486078fcc6866a477df83b19270ae872102f4ed64b5a5e9995ff79afa
'http://deb.debian.org/debian/pool/main/d/debian-archive-keyring/debian-archive-keyring_2023.4.tar.xz' debian-archive-keyring_2023.4.tar.xz 177568 SHA256:7f9b64d7c5e748b0cb99fd0674d872111c219e119f296912c59fc61ab49bb78a
```

Other potentially useful URLs:

- https://sources.debian.net/src/debian-archive-keyring/2023.4/ (for browsing the source)
- https://sources.debian.net/src/debian-archive-keyring/2023.4/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/debian-archive-keyring/2023.4/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `debianutils=5.21`

Binary Packages:

- `debianutils=5.21`

Licenses: (parsed from: `/usr/share/doc/debianutils/copyright`)

- `GPL-2`
- `GPL-2+`
- `SMAIL-GPL`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris debianutils=5.21
'http://deb.debian.org/debian/pool/main/d/debianutils/debianutils_5.21.dsc' debianutils_5.21.dsc 1631 SHA256:9e26a955c62d09a9401aeb53cb190eca078b2cc13ea33ec874e944e95c21935e
'http://deb.debian.org/debian/pool/main/d/debianutils/debianutils_5.21.tar.xz' debianutils_5.21.tar.xz 81916 SHA256:0053dcfd89e5c7dbfb2632450c00af6b8a646eeaaf185bbc8f2915488f994fe5
```

Other potentially useful URLs:

- https://sources.debian.net/src/debianutils/5.21/ (for browsing the source)
- https://sources.debian.net/src/debianutils/5.21/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/debianutils/5.21/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/d/diffutils/diffutils_3.10-1.dsc' diffutils_3.10-1.dsc 1715 SHA256:f7542884c67d44f0af356c5365a3fef8a298f1fbcbebf9df81cfbc6d6937f05f
'http://deb.debian.org/debian/pool/main/d/diffutils/diffutils_3.10.orig.tar.xz' diffutils_3.10.orig.tar.xz 1624240 SHA256:90e5e93cc724e4ebe12ede80df1634063c7a855692685919bfe60b556c9bd09e
'http://deb.debian.org/debian/pool/main/d/diffutils/diffutils_3.10.orig.tar.xz.asc' diffutils_3.10.orig.tar.xz.asc 833 SHA256:a94faf8f1baa04ff220f7b2ccb137c16337284e023ebc4a1d5df475c08d810f7
'http://deb.debian.org/debian/pool/main/d/diffutils/diffutils_3.10-1.debian.tar.xz' diffutils_3.10-1.debian.tar.xz 13952 SHA256:ebf51a7ceff8c882f997ca428232fd3b58ac59a70840c4b10f8fcfaa881598ce
```

Other potentially useful URLs:

- https://sources.debian.net/src/diffutils/1:3.10-1/ (for browsing the source)
- https://sources.debian.net/src/diffutils/1:3.10-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/diffutils/1:3.10-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `dpkg=1.22.11`

Binary Packages:

- `dpkg=1.22.11`

Licenses: (parsed from: `/usr/share/doc/dpkg/copyright`)

- `GPL-2`
- `GPL-2+`
- `public-domain-s-s-d`

Source:

```console
$ apt-get source -qq --print-uris dpkg=1.22.11
'http://deb.debian.org/debian/pool/main/d/dpkg/dpkg_1.22.11.dsc' dpkg_1.22.11.dsc 3144 SHA256:d850ae15f8a43c981edaace2003f93d44f6f23666917bd26472f266d172a03fa
'http://deb.debian.org/debian/pool/main/d/dpkg/dpkg_1.22.11.tar.xz' dpkg_1.22.11.tar.xz 5697040 SHA256:f318eb949b8e7ecd802b17b1a7e7cf4b17094c9577e1060653e9b838cdd31d80
```

Other potentially useful URLs:

- https://sources.debian.net/src/dpkg/1.22.11/ (for browsing the source)
- https://sources.debian.net/src/dpkg/1.22.11/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/dpkg/1.22.11/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `e2fsprogs=1.47.1-1`

Binary Packages:

- `e2fsprogs=1.47.1-1+b1`
- `libcom-err2:amd64=1.47.1-1+b1`
- `libext2fs2t64:amd64=1.47.1-1+b1`
- `libss2:amd64=1.47.1-1+b1`
- `logsave=1.47.1-1+b1`

Licenses: (parsed from: `/usr/share/doc/e2fsprogs/copyright`, `/usr/share/doc/libcom-err2/copyright`, `/usr/share/doc/libext2fs2t64/copyright`, `/usr/share/doc/libss2/copyright`, `/usr/share/doc/logsave/copyright`)

- `Apache-2`
- `Apache-2.0`
- `BSD-3-Clause`
- `BSD-3-Clause-Variant`
- `BSD-4-Clause-CMU`
- `Expat`
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
$ apt-get source -qq --print-uris e2fsprogs=1.47.1-1
'http://deb.debian.org/debian/pool/main/e/e2fsprogs/e2fsprogs_1.47.1-1.dsc' e2fsprogs_1.47.1-1.dsc 2936 SHA256:04ae87a924fa3c9826db58af7e48c48659979c3e71b81a64bcaa48bf6e82507e
'http://deb.debian.org/debian/pool/main/e/e2fsprogs/e2fsprogs_1.47.1.orig.tar.gz' e2fsprogs_1.47.1.orig.tar.gz 9952468 SHA256:9afcd201f39429d2db2492aeb13dba5e75d6cc50682b732dca35643bd5f092e3
'http://deb.debian.org/debian/pool/main/e/e2fsprogs/e2fsprogs_1.47.1.orig.tar.gz.asc' e2fsprogs_1.47.1.orig.tar.gz.asc 488 SHA256:19b5fed0eb91cd58f0f82252a7d3f72a803dc2f497bfa765034551d9feb06781
'http://deb.debian.org/debian/pool/main/e/e2fsprogs/e2fsprogs_1.47.1-1.debian.tar.xz' e2fsprogs_1.47.1-1.debian.tar.xz 89808 SHA256:8d4a4b695ca9012c4e21a727ba9f00bf09c2b7adffd83813e998bfa76ed106b0
```

Other potentially useful URLs:

- https://sources.debian.net/src/e2fsprogs/1.47.1-1/ (for browsing the source)
- https://sources.debian.net/src/e2fsprogs/1.47.1-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/e2fsprogs/1.47.1-1/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/f/findutils/findutils_4.10.0-3.dsc' findutils_4.10.0-3.dsc 2291 SHA256:fa6b67056d9e5b4d8edbfc8ab95ac15ac769b140284426973f6a1ef07a4594ec
'http://deb.debian.org/debian/pool/main/f/findutils/findutils_4.10.0.orig.tar.xz' findutils_4.10.0.orig.tar.xz 2240712 SHA256:1387e0b67ff247d2abde998f90dfbf70c1491391a59ddfecb8ae698789f0a4f5
'http://deb.debian.org/debian/pool/main/f/findutils/findutils_4.10.0.orig.tar.xz.asc' findutils_4.10.0.orig.tar.xz.asc 488 SHA256:7f53670eea6bd114e014571221eb652855c1129a3ed99f2a9257c2a313cc216f
'http://deb.debian.org/debian/pool/main/f/findutils/findutils_4.10.0-3.debian.tar.xz' findutils_4.10.0-3.debian.tar.xz 33364 SHA256:7d19668508523a6fcfb7731f5646305a8b1a00a3105ee3f0a5f167adf93a8a46
```

Other potentially useful URLs:

- https://sources.debian.net/src/findutils/4.10.0-3/ (for browsing the source)
- https://sources.debian.net/src/findutils/4.10.0-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/findutils/4.10.0-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `gcc-14=14.2.0-8`

Binary Packages:

- `gcc-14-base:amd64=14.2.0-8`
- `libgcc-s1:amd64=14.2.0-8`
- `libstdc++6:amd64=14.2.0-8`

Licenses: (parsed from: `/usr/share/doc/gcc-14-base/copyright`, `/usr/share/doc/libgcc-s1/copyright`, `/usr/share/doc/libstdc++6/copyright`)

- `Artistic`
- `GFDL-1.2`
- `GPL`
- `GPL-3`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris gcc-14=14.2.0-8
'http://deb.debian.org/debian/pool/main/g/gcc-14/gcc-14_14.2.0-8.dsc' gcc-14_14.2.0-8.dsc 46500 SHA256:f5a3c1957c655537433d5785c0aecbda712838f770672c975fbd29a122a1f4c5
'http://deb.debian.org/debian/pool/main/g/gcc-14/gcc-14_14.2.0.orig.tar.gz' gcc-14_14.2.0.orig.tar.gz 94299633 SHA256:e162a5ef3f0077ecae598c6556908d2ab80841532df3398072a96a6df6e6aa29
'http://deb.debian.org/debian/pool/main/g/gcc-14/gcc-14_14.2.0-8.debian.tar.xz' gcc-14_14.2.0-8.debian.tar.xz 2051624 SHA256:54c045291eec3b92f721ff236f83635ce6bafaa3e34ddbd137fdad3854953eb8
```

Other potentially useful URLs:

- https://sources.debian.net/src/gcc-14/14.2.0-8/ (for browsing the source)
- https://sources.debian.net/src/gcc-14/14.2.0-8/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/gcc-14/14.2.0-8/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `glibc=2.40-3`

Binary Packages:

- `libc-bin=2.40-3`
- `libc6:amd64=2.40-3`

Licenses: (parsed from: `/usr/share/doc/libc-bin/copyright`, `/usr/share/doc/libc6/copyright`)

- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris glibc=2.40-3
'http://deb.debian.org/debian/pool/main/g/glibc/glibc_2.40-3.dsc' glibc_2.40-3.dsc 7550 SHA256:ad595e37545bf472d2ce8de51712121c88ca960d2e5617af6359d795d7d35f84
'http://deb.debian.org/debian/pool/main/g/glibc/glibc_2.40.orig.tar.xz' glibc_2.40.orig.tar.xz 19517224 SHA256:0b89b8c058eaa0f1121a814be6196ce2048235b43d95714ce8278fe72c7cc34a
'http://deb.debian.org/debian/pool/main/g/glibc/glibc_2.40-3.debian.tar.xz' glibc_2.40-3.debian.tar.xz 417288 SHA256:1a30c14bc68422b6085c0a4d9f0db2be82dffd7da0bf3090307bbbe237c08f73
```

Other potentially useful URLs:

- https://sources.debian.net/src/glibc/2.40-3/ (for browsing the source)
- https://sources.debian.net/src/glibc/2.40-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/glibc/2.40-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `gmp=2:6.3.0+dfsg-2`

Binary Packages:

- `libgmp10:amd64=2:6.3.0+dfsg-2+b2`

Licenses: (parsed from: `/usr/share/doc/libgmp10/copyright`)

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

- http://snapshot.debian.org/package/gmp/2:6.3.0+dfsg-2/


### `dpkg` source package: `gnupg2=2.2.45-2`

Binary Packages:

- `gpgv=2.2.45-2`

Licenses: (parsed from: `/usr/share/doc/gpgv/copyright`)

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
$ apt-get source -qq --print-uris gnupg2=2.2.45-2
'http://deb.debian.org/debian/pool/main/g/gnupg2/gnupg2_2.2.45-2.dsc' gnupg2_2.2.45-2.dsc 3873 SHA256:27640274a66ba8449475377949a4e5fb5679293a8dbe5fff707d726c9bacfa5b
'http://deb.debian.org/debian/pool/main/g/gnupg2/gnupg2_2.2.45.orig.tar.bz2' gnupg2_2.2.45.orig.tar.bz2 7447141 SHA256:d1abecd2b6c052749fd5748ba9de7021567e06b573dc6becac8df25cb87500e8
'http://deb.debian.org/debian/pool/main/g/gnupg2/gnupg2_2.2.45.orig.tar.bz2.asc' gnupg2_2.2.45.orig.tar.bz2.asc 228 SHA256:4c70f582308e218bfd5ca3e4176d39c8fa15d39d3183c836daf13ab5371f68dd
'http://deb.debian.org/debian/pool/main/g/gnupg2/gnupg2_2.2.45-2.debian.tar.xz' gnupg2_2.2.45-2.debian.tar.xz 141036 SHA256:28fb29abeed25c221ec7877f5f028fb972fe3d7cc26040d09bb84d72d2cc6280
```

Other potentially useful URLs:

- https://sources.debian.net/src/gnupg2/2.2.45-2/ (for browsing the source)
- https://sources.debian.net/src/gnupg2/2.2.45-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/gnupg2/2.2.45-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `gnutls28=3.8.8-2`

Binary Packages:

- `libgnutls30t64:amd64=3.8.8-2`

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

Source:

```console
$ apt-get source -qq --print-uris gnutls28=3.8.8-2
'http://deb.debian.org/debian/pool/main/g/gnutls28/gnutls28_3.8.8-2.dsc' gnutls28_3.8.8-2.dsc 3236 SHA256:b9166175cbd952f9d5ec0ee8868d49a3213f6646d64ade9416969dd4587eeb07
'http://deb.debian.org/debian/pool/main/g/gnutls28/gnutls28_3.8.8.orig.tar.xz' gnutls28_3.8.8.orig.tar.xz 6696460 SHA256:ac4f020e583880b51380ed226e59033244bc536cad2623f2e26f5afa2939d8fb
'http://deb.debian.org/debian/pool/main/g/gnutls28/gnutls28_3.8.8.orig.tar.xz.asc' gnutls28_3.8.8.orig.tar.xz.asc 854 SHA256:add4e5e0c1a4b5c7c870c0c0c0a328a6c579f6e1cd49577e90e26273e1b67473
'http://deb.debian.org/debian/pool/main/g/gnutls28/gnutls28_3.8.8-2.debian.tar.xz' gnutls28_3.8.8-2.debian.tar.xz 77860 SHA256:058641644beb97899fc18558251e86ec314d2aaa8a995b96518f0ce3ef32a4e7
```

Other potentially useful URLs:

- https://sources.debian.net/src/gnutls28/3.8.8-2/ (for browsing the source)
- https://sources.debian.net/src/gnutls28/3.8.8-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/gnutls28/3.8.8-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `grep=3.11-4`

Binary Packages:

- `grep=3.11-4`

Licenses: (parsed from: `/usr/share/doc/grep/copyright`)

- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris grep=3.11-4
'http://deb.debian.org/debian/pool/main/g/grep/grep_3.11-4.dsc' grep_3.11-4.dsc 1642 SHA256:dd6f8eb933bc05446e483f7792c8bf0a1aba9d498e65c6ccafe64e9bf27ac054
'http://deb.debian.org/debian/pool/main/g/grep/grep_3.11.orig.tar.xz' grep_3.11.orig.tar.xz 1703776 SHA256:1db2aedde89d0dea42b16d9528f894c8d15dae4e190b59aecc78f5a951276eab
'http://deb.debian.org/debian/pool/main/g/grep/grep_3.11.orig.tar.xz.asc' grep_3.11.orig.tar.xz.asc 833 SHA256:89ec23ffd59b68822732dc8204fc89883c3af30a90ae390feb94346d9d09a589
'http://deb.debian.org/debian/pool/main/g/grep/grep_3.11-4.debian.tar.xz' grep_3.11-4.debian.tar.xz 20468 SHA256:f10394b7589c58ca7de4b580692b1b59431f898cb2068e86222c174e093fdf49
```

Other potentially useful URLs:

- https://sources.debian.net/src/grep/3.11-4/ (for browsing the source)
- https://sources.debian.net/src/grep/3.11-4/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/grep/3.11-4/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `gzip=1.12-1.1`

Binary Packages:

- `gzip=1.12-1.1`

Licenses: (parsed from: `/usr/share/doc/gzip/copyright`)

- `FSF-manpages`
- `GFDL-1.3+-no-invariant`
- `GFDL-3`
- `GPL-3`
- `GPL-3+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/gzip/1.12-1.1/


### `dpkg` source package: `hostname=3.25`

Binary Packages:

- `hostname=3.25`

Licenses: (parsed from: `/usr/share/doc/hostname/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris hostname=3.25
'http://deb.debian.org/debian/pool/main/h/hostname/hostname_3.25.dsc' hostname_3.25.dsc 1519 SHA256:80aadf116c3423044be69a4cef8ba2766f412bd4d46a500aacb61f303c19c4ef
'http://deb.debian.org/debian/pool/main/h/hostname/hostname_3.25.tar.xz' hostname_3.25.tar.xz 12804 SHA256:5bb5d1be011158090157c9e7587ae5606c262a5020ecdc5caac6686b9910592e
```

Other potentially useful URLs:

- https://sources.debian.net/src/hostname/3.25/ (for browsing the source)
- https://sources.debian.net/src/hostname/3.25/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/hostname/3.25/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `init-system-helpers=1.67`

Binary Packages:

- `init-system-helpers=1.67`

Licenses: (parsed from: `/usr/share/doc/init-system-helpers/copyright`)

- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris init-system-helpers=1.67
'http://deb.debian.org/debian/pool/main/i/init-system-helpers/init-system-helpers_1.67.dsc' init-system-helpers_1.67.dsc 2234 SHA256:26e89df8709f6af0bc7629df7d6ccd327227ab9be8788c9232ffe9b559a7e86d
'http://deb.debian.org/debian/pool/main/i/init-system-helpers/init-system-helpers_1.67.tar.xz' init-system-helpers_1.67.tar.xz 45180 SHA256:3fa7f7f1cffd0300363b49062c953023705009640e50141b00362e9fb40c5556
```

Other potentially useful URLs:

- https://sources.debian.net/src/init-system-helpers/1.67/ (for browsing the source)
- https://sources.debian.net/src/init-system-helpers/1.67/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/init-system-helpers/1.67/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/libb/libbsd/libbsd_0.12.2-2.dsc' libbsd_0.12.2-2.dsc 2446 SHA256:01eb1d0c896096f9038213f5f00376ecfd1c0d1def21b7042f28ae070e4837e3
'http://deb.debian.org/debian/pool/main/libb/libbsd/libbsd_0.12.2.orig.tar.xz' libbsd_0.12.2.orig.tar.xz 446032 SHA256:b88cc9163d0c652aaf39a99991d974ddba1c3a9711db8f1b5838af2a14731014
'http://deb.debian.org/debian/pool/main/libb/libbsd/libbsd_0.12.2.orig.tar.xz.asc' libbsd_0.12.2.orig.tar.xz.asc 833 SHA256:620dc92f158ebe0a650c0e92214a8121b927276895dc9a1dcaa38f627fa0fcb0
'http://deb.debian.org/debian/pool/main/libb/libbsd/libbsd_0.12.2-2.debian.tar.xz' libbsd_0.12.2-2.debian.tar.xz 18688 SHA256:36c878a32c1f190ca2cb474de5c6139990a6c029906493d3566770b1ebd569bf
```

Other potentially useful URLs:

- https://sources.debian.net/src/libbsd/0.12.2-2/ (for browsing the source)
- https://sources.debian.net/src/libbsd/0.12.2-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libbsd/0.12.2-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libcap-ng=0.8.5-4`

Binary Packages:

- `libcap-ng0:amd64=0.8.5-4`

Licenses: (parsed from: `/usr/share/doc/libcap-ng0/copyright`)

- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris libcap-ng=0.8.5-4
'http://deb.debian.org/debian/pool/main/libc/libcap-ng/libcap-ng_0.8.5-4.dsc' libcap-ng_0.8.5-4.dsc 1710 SHA256:a5745b7d68a11068ae5beddcc7fbc94cd87dd81cb2d7495e7d48610603be3526
'http://deb.debian.org/debian/pool/main/libc/libcap-ng/libcap-ng_0.8.5.orig.tar.gz' libcap-ng_0.8.5.orig.tar.gz 59265 SHA256:e4be07fdd234f10b866433f224d183626003c65634ed0552b02e654a380244c2
'http://deb.debian.org/debian/pool/main/libc/libcap-ng/libcap-ng_0.8.5-4.debian.tar.xz' libcap-ng_0.8.5-4.debian.tar.xz 7816 SHA256:f5d4e7f38bdbca87de77317ce95f973883081370ef257019b484e29e3368a20d
```

Other potentially useful URLs:

- https://sources.debian.net/src/libcap-ng/0.8.5-4/ (for browsing the source)
- https://sources.debian.net/src/libcap-ng/0.8.5-4/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libcap-ng/0.8.5-4/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libcap2=1:2.66-5`

Binary Packages:

- `libcap2:amd64=1:2.66-5+b1`

Licenses: (parsed from: `/usr/share/doc/libcap2/copyright`)

- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris libcap2=1:2.66-5
'http://deb.debian.org/debian/pool/main/libc/libcap2/libcap2_2.66-5.dsc' libcap2_2.66-5.dsc 2204 SHA256:7d8fd6db23376ad9ded85aebd5d5ed9cf133b1e561d3ac2b43fdf5b0b63739a8
'http://deb.debian.org/debian/pool/main/libc/libcap2/libcap2_2.66.orig.tar.xz' libcap2_2.66.orig.tar.xz 181592 SHA256:15c40ededb3003d70a283fe587a36b7d19c8b3b554e33f86129c059a4bb466b2
'http://deb.debian.org/debian/pool/main/libc/libcap2/libcap2_2.66-5.debian.tar.xz' libcap2_2.66-5.debian.tar.xz 21648 SHA256:fee7fdec4c806808b3e4c56e53ff5614b92186ecc6fd23a9e88694cdd938c452
```

Other potentially useful URLs:

- https://sources.debian.net/src/libcap2/1:2.66-5/ (for browsing the source)
- https://sources.debian.net/src/libcap2/1:2.66-5/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libcap2/1:2.66-5/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libffi=3.4.6-1`

Binary Packages:

- `libffi8:amd64=3.4.6-1`

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
$ apt-get source -qq --print-uris libffi=3.4.6-1
'http://deb.debian.org/debian/pool/main/libf/libffi/libffi_3.4.6-1.dsc' libffi_3.4.6-1.dsc 1948 SHA256:6734a8f8e237a7d5c4f52503f5e9cc193d16f8930a201bbf737f09cb31cfe28e
'http://deb.debian.org/debian/pool/main/libf/libffi/libffi_3.4.6.orig.tar.gz' libffi_3.4.6.orig.tar.gz 598175 SHA256:9ac790464c1eb2f5ab5809e978a1683e9393131aede72d1b0a0703771d3c6cda
'http://deb.debian.org/debian/pool/main/libf/libffi/libffi_3.4.6-1.debian.tar.xz' libffi_3.4.6-1.debian.tar.xz 10636 SHA256:7126c310b616e9c4c8fdd50bd857f54379d26897ab55383a25e89b6cbd69729c
```

Other potentially useful URLs:

- https://sources.debian.net/src/libffi/3.4.6-1/ (for browsing the source)
- https://sources.debian.net/src/libffi/3.4.6-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libffi/3.4.6-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libgcrypt20=1.11.0-6`

Binary Packages:

- `libgcrypt20:amd64=1.11.0-6`

Licenses: (parsed from: `/usr/share/doc/libgcrypt20/copyright`)

- `GPL-2`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris libgcrypt20=1.11.0-6
'http://deb.debian.org/debian/pool/main/libg/libgcrypt20/libgcrypt20_1.11.0-6.dsc' libgcrypt20_1.11.0-6.dsc 2877 SHA256:9d14f1cfec9a9c6523f9c469132634467daa43f83203f6339447fb6722b54b42
'http://deb.debian.org/debian/pool/main/libg/libgcrypt20/libgcrypt20_1.11.0.orig.tar.bz2' libgcrypt20_1.11.0.orig.tar.bz2 4180345 SHA256:09120c9867ce7f2081d6aaa1775386b98c2f2f246135761aae47d81f58685b9c
'http://deb.debian.org/debian/pool/main/libg/libgcrypt20/libgcrypt20_1.11.0.orig.tar.bz2.asc' libgcrypt20_1.11.0.orig.tar.bz2.asc 228 SHA256:9fedf4f7bb80d5178d4e26ec2f03ba5fc44eddfc72c2e9966d7d619aeee3df2c
'http://deb.debian.org/debian/pool/main/libg/libgcrypt20/libgcrypt20_1.11.0-6.debian.tar.xz' libgcrypt20_1.11.0-6.debian.tar.xz 39088 SHA256:f1b8c0dc512241b427d8c2f7617355a7f4c98def3d5689495b6051a275a1357f
```

Other potentially useful URLs:

- https://sources.debian.net/src/libgcrypt20/1.11.0-6/ (for browsing the source)
- https://sources.debian.net/src/libgcrypt20/1.11.0-6/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libgcrypt20/1.11.0-6/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libgpg-error=1.50-4`

Binary Packages:

- `libgpg-error0:amd64=1.50-4`

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

- http://snapshot.debian.org/package/libgpg-error/1.50-4/


### `dpkg` source package: `libidn2=2.3.7-2`

Binary Packages:

- `libidn2-0:amd64=2.3.7-2+b1`

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
$ apt-get source -qq --print-uris libidn2=2.3.7-2
'http://deb.debian.org/debian/pool/main/libi/libidn2/libidn2_2.3.7-2.dsc' libidn2_2.3.7-2.dsc 1963 SHA256:ba763f71c75847be4c68557a937484ff9e676c0af8be9a6796c914dab1363a5f
'http://deb.debian.org/debian/pool/main/libi/libidn2/libidn2_2.3.7.orig.tar.gz' libidn2_2.3.7.orig.tar.gz 2155214 SHA256:4c21a791b610b9519b9d0e12b8097bf2f359b12f8dd92647611a929e6bfd7d64
'http://deb.debian.org/debian/pool/main/libi/libidn2/libidn2_2.3.7.orig.tar.gz.asc' libidn2_2.3.7.orig.tar.gz.asc 228 SHA256:d4e78fc1c5a5c35980be3a04dd864574f450d55921360b0aa19326c75ada4a98
'http://deb.debian.org/debian/pool/main/libi/libidn2/libidn2_2.3.7-2.debian.tar.xz' libidn2_2.3.7-2.debian.tar.xz 16276 SHA256:1f0ca3a2bb2c745056933cb41d212965b6571c9a436f83d33cba15e932d88d29
```

Other potentially useful URLs:

- https://sources.debian.net/src/libidn2/2.3.7-2/ (for browsing the source)
- https://sources.debian.net/src/libidn2/2.3.7-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libidn2/2.3.7-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libmd=1.1.0-2`

Binary Packages:

- `libmd0:amd64=1.1.0-2+b1`

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
'http://deb.debian.org/debian/pool/main/libm/libmd/libmd_1.1.0-2.dsc' libmd_1.1.0-2.dsc 2280 SHA256:46cc951cd6d71bbfeff4522de66f968fb92601ec4cc622b07f6ac0a2a36ac5f0
'http://deb.debian.org/debian/pool/main/libm/libmd/libmd_1.1.0.orig.tar.xz' libmd_1.1.0.orig.tar.xz 271228 SHA256:1bd6aa42275313af3141c7cf2e5b964e8b1fd488025caf2f971f43b00776b332
'http://deb.debian.org/debian/pool/main/libm/libmd/libmd_1.1.0.orig.tar.xz.asc' libmd_1.1.0.orig.tar.xz.asc 833 SHA256:402fd3024e43ab975733d09e661804a58ca58697194e4b15216b1217cfe1dadb
'http://deb.debian.org/debian/pool/main/libm/libmd/libmd_1.1.0-2.debian.tar.xz' libmd_1.1.0-2.debian.tar.xz 8244 SHA256:3b6ff35fc921eb5450fa9bf2d300c9e058e3771f96f8f13f759768fadd53324c
```

Other potentially useful URLs:

- https://sources.debian.net/src/libmd/1.1.0-2/ (for browsing the source)
- https://sources.debian.net/src/libmd/1.1.0-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libmd/1.1.0-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libseccomp=2.5.5-2`

Binary Packages:

- `libseccomp2:amd64=2.5.5-2`

Licenses: (parsed from: `/usr/share/doc/libseccomp2/copyright`)

- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libseccomp=2.5.5-2
'http://deb.debian.org/debian/pool/main/libs/libseccomp/libseccomp_2.5.5-2.dsc' libseccomp_2.5.5-2.dsc 2708 SHA256:e69657cf7b3cf0219d4c6d72c81db1f7f2d9a8e090fd8a983d17a4a80363dcc2
'http://deb.debian.org/debian/pool/main/libs/libseccomp/libseccomp_2.5.5.orig.tar.gz' libseccomp_2.5.5.orig.tar.gz 642445 SHA256:248a2c8a4d9b9858aa6baf52712c34afefcf9c9e94b76dce02c1c9aa25fb3375
'http://deb.debian.org/debian/pool/main/libs/libseccomp/libseccomp_2.5.5.orig.tar.gz.asc' libseccomp_2.5.5.orig.tar.gz.asc 833 SHA256:f3bf8a946020d3047581f11fe6ac71971a842115ddb362562b193861ef57d97b
'http://deb.debian.org/debian/pool/main/libs/libseccomp/libseccomp_2.5.5-2.debian.tar.xz' libseccomp_2.5.5-2.debian.tar.xz 39004 SHA256:82fa4dfbea7c0ce54d18781230b9625c44fc83f495ef4a468beb2a33e98897ef
```

Other potentially useful URLs:

- https://sources.debian.net/src/libseccomp/2.5.5-2/ (for browsing the source)
- https://sources.debian.net/src/libseccomp/2.5.5-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libseccomp/2.5.5-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libselinux=3.7-3`

Binary Packages:

- `libselinux1:amd64=3.7-3+b1`

Licenses: (parsed from: `/usr/share/doc/libselinux1/copyright`)

- `GPL-2`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris libselinux=3.7-3
'http://deb.debian.org/debian/pool/main/libs/libselinux/libselinux_3.7-3.dsc' libselinux_3.7-3.dsc 2990 SHA256:18559f82479feb99d429eb20e4b4572825cb8cb8ce0d2534b69c145f80cd7230
'http://deb.debian.org/debian/pool/main/libs/libselinux/libselinux_3.7.orig.tar.gz' libselinux_3.7.orig.tar.gz 194834 SHA256:ea03f42d13a4f95757997dba8cf0b26321fac5d2f164418b4cc856a92d2b17bd
'http://deb.debian.org/debian/pool/main/libs/libselinux/libselinux_3.7.orig.tar.gz.asc' libselinux_3.7.orig.tar.gz.asc 833 SHA256:8dbd0457d227a7182b0a1f2f8659c2f4dd4ae837f5e69a17d1698f6c31c37f31
'http://deb.debian.org/debian/pool/main/libs/libselinux/libselinux_3.7-3.debian.tar.xz' libselinux_3.7-3.debian.tar.xz 41912 SHA256:db181834077ab5bbfc7118b3414d003b412f21463acd1924a25f826fa0f484ed
```

Other potentially useful URLs:

- https://sources.debian.net/src/libselinux/3.7-3/ (for browsing the source)
- https://sources.debian.net/src/libselinux/3.7-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libselinux/3.7-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libsemanage=3.7-2`

Binary Packages:

- `libsemanage-common=3.7-2`
- `libsemanage2:amd64=3.7-2+b1`

Licenses: (parsed from: `/usr/share/doc/libsemanage-common/copyright`, `/usr/share/doc/libsemanage2/copyright`)

- `GPL-2`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris libsemanage=3.7-2
'http://deb.debian.org/debian/pool/main/libs/libsemanage/libsemanage_3.7-2.dsc' libsemanage_3.7-2.dsc 2965 SHA256:77fd2cef54cbd51c3d76a622a0aefe4488ae9403db32c5c92c801bce181690ae
'http://deb.debian.org/debian/pool/main/libs/libsemanage/libsemanage_3.7.orig.tar.gz' libsemanage_3.7.orig.tar.gz 182896 SHA256:e166cae29a417dab008db9ca0874023f353a3017b07693a036ed97487eda35b1
'http://deb.debian.org/debian/pool/main/libs/libsemanage/libsemanage_3.7.orig.tar.gz.asc' libsemanage_3.7.orig.tar.gz.asc 833 SHA256:02981e0224fdf0141fc29b950f7e5aab1653d5fee6dcbf6d6a5ff976e5720cc8
'http://deb.debian.org/debian/pool/main/libs/libsemanage/libsemanage_3.7-2.debian.tar.xz' libsemanage_3.7-2.debian.tar.xz 35172 SHA256:eeb1ca76456ea4caf7850699d5999b7a9f5b49ebaa6a5a6929e84848305a297b
```

Other potentially useful URLs:

- https://sources.debian.net/src/libsemanage/3.7-2/ (for browsing the source)
- https://sources.debian.net/src/libsemanage/3.7-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libsemanage/3.7-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libsepol=3.7-1`

Binary Packages:

- `libsepol2:amd64=3.7-1`

Licenses: (parsed from: `/usr/share/doc/libsepol2/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris libsepol=3.7-1
'http://deb.debian.org/debian/pool/main/libs/libsepol/libsepol_3.7-1.dsc' libsepol_3.7-1.dsc 2085 SHA256:d5c8df3195e58607d769d6030b4254013bf483723084a42656cfb50a38b91fff
'http://deb.debian.org/debian/pool/main/libs/libsepol/libsepol_3.7.orig.tar.gz' libsepol_3.7.orig.tar.gz 511487 SHA256:cd741e25244e7ef6cd934d633614131a266c3eaeab33d8bfa45e8a93b45cc901
'http://deb.debian.org/debian/pool/main/libs/libsepol/libsepol_3.7-1.debian.tar.xz' libsepol_3.7-1.debian.tar.xz 27632 SHA256:fe5c57d69d081d60d423185bf339aa10755eb629d38f4129dd9944be64c6991b
```

Other potentially useful URLs:

- https://sources.debian.net/src/libsepol/3.7-1/ (for browsing the source)
- https://sources.debian.net/src/libsepol/3.7-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libsepol/3.7-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libtasn1-6=4.19.0-3`

Binary Packages:

- `libtasn1-6:amd64=4.19.0-3+b3`

Licenses: (parsed from: `/usr/share/doc/libtasn1-6/copyright`)

- `GFDL-1.3`
- `GPL-3`
- `LGPL`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libtasn1-6=4.19.0-3
'http://deb.debian.org/debian/pool/main/libt/libtasn1-6/libtasn1-6_4.19.0-3.dsc' libtasn1-6_4.19.0-3.dsc 2662 SHA256:7fd9618be5b99035c7387d969b73365a57b1f6f01ec4abe0af332829af718190
'http://deb.debian.org/debian/pool/main/libt/libtasn1-6/libtasn1-6_4.19.0.orig.tar.gz' libtasn1-6_4.19.0.orig.tar.gz 1786576 SHA256:1613f0ac1cf484d6ec0ce3b8c06d56263cc7242f1c23b30d82d23de345a63f7a
'http://deb.debian.org/debian/pool/main/libt/libtasn1-6/libtasn1-6_4.19.0.orig.tar.gz.asc' libtasn1-6_4.19.0.orig.tar.gz.asc 228 SHA256:8410c0c004f3509c218a98b276b3308b9c46f48068e8b1a6d9ebfd61ea9f357a
'http://deb.debian.org/debian/pool/main/libt/libtasn1-6/libtasn1-6_4.19.0-3.debian.tar.xz' libtasn1-6_4.19.0-3.debian.tar.xz 22084 SHA256:acb32dc03d8c2aeb10e0fb1c2a0247efdab0a6dc5e8f8a4d3cdcfe5ad26bb0df
```

Other potentially useful URLs:

- https://sources.debian.net/src/libtasn1-6/4.19.0-3/ (for browsing the source)
- https://sources.debian.net/src/libtasn1-6/4.19.0-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libtasn1-6/4.19.0-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libunistring=1.2-1`

Binary Packages:

- `libunistring5:amd64=1.2-1+b1`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/libunistring/1.2-1/


### `dpkg` source package: `libxcrypt=1:4.4.36-5`

Binary Packages:

- `libcrypt1:amd64=1:4.4.36-5`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxcrypt=1:4.4.36-5
'http://deb.debian.org/debian/pool/main/libx/libxcrypt/libxcrypt_4.4.36-5.dsc' libxcrypt_4.4.36-5.dsc 1576 SHA256:660fca79ca38888ed61e26f7ef6990299586471ff8462d6900abf1afe1e569e3
'http://deb.debian.org/debian/pool/main/libx/libxcrypt/libxcrypt_4.4.36.orig.tar.xz' libxcrypt_4.4.36.orig.tar.xz 392732 SHA256:7b7abbc89f13f5194211aa6861ed954e4fa3a210a4cb64f7e13dc8cf413e7f2a
'http://deb.debian.org/debian/pool/main/libx/libxcrypt/libxcrypt_4.4.36-5.debian.tar.xz' libxcrypt_4.4.36-5.debian.tar.xz 9184 SHA256:c520211106ab811788ba37fc766166a6cf17156882a13d7f0ab9de5834f95b52
```

Other potentially useful URLs:

- https://sources.debian.net/src/libxcrypt/1:4.4.36-5/ (for browsing the source)
- https://sources.debian.net/src/libxcrypt/1:4.4.36-5/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libxcrypt/1:4.4.36-5/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libzstd=1.5.6+dfsg-1`

Binary Packages:

- `libzstd1:amd64=1.5.6+dfsg-1+b1`

Licenses: (parsed from: `/usr/share/doc/libzstd1/copyright`)

- `BSD-3-clause`
- `Expat`
- `GPL-2`
- `zlib`

Source:

```console
$ apt-get source -qq --print-uris libzstd=1.5.6+dfsg-1
'http://deb.debian.org/debian/pool/main/libz/libzstd/libzstd_1.5.6%2bdfsg-1.dsc' libzstd_1.5.6+dfsg-1.dsc 2369 SHA256:c1774527814630f8e3ec1a6025d6b7a188ceccee002815ed143c3653e3b0b510
'http://deb.debian.org/debian/pool/main/libz/libzstd/libzstd_1.5.6%2bdfsg.orig.tar.xz' libzstd_1.5.6+dfsg.orig.tar.xz 1815380 SHA256:b3a60c7059886641830adf32c979be8d211da5d73fd05c7768f86d12d5bccec3
'http://deb.debian.org/debian/pool/main/libz/libzstd/libzstd_1.5.6%2bdfsg-1.debian.tar.xz' libzstd_1.5.6+dfsg-1.debian.tar.xz 22624 SHA256:33e540298d9fa29e12426a66e4b0b7715b3143659d16246e09c33f2fb69bad17
```

Other potentially useful URLs:

- https://sources.debian.net/src/libzstd/1.5.6+dfsg-1/ (for browsing the source)
- https://sources.debian.net/src/libzstd/1.5.6+dfsg-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libzstd/1.5.6+dfsg-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `lz4=1.9.4-3`

Binary Packages:

- `liblz4-1:amd64=1.9.4-3+b1`

Licenses: (parsed from: `/usr/share/doc/liblz4-1/copyright`)

- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris lz4=1.9.4-3
'http://deb.debian.org/debian/pool/main/l/lz4/lz4_1.9.4-3.dsc' lz4_1.9.4-3.dsc 1934 SHA256:30365311787d4d9753a83d88dad9fa4a085e075db5cdee50be54b241f1265abb
'http://deb.debian.org/debian/pool/main/l/lz4/lz4_1.9.4.orig.tar.gz' lz4_1.9.4.orig.tar.gz 354063 SHA256:0b0e3aa07c8c063ddf40b082bdf7e37a1562bda40a0ff5272957f3e987e0e54b
'http://deb.debian.org/debian/pool/main/l/lz4/lz4_1.9.4-3.debian.tar.xz' lz4_1.9.4-3.debian.tar.xz 7076 SHA256:199c96cd86297cde59c56286ecd1b4ffa334dc73c0f54d39b5058f7e0b73a31c
```

Other potentially useful URLs:

- https://sources.debian.net/src/lz4/1.9.4-3/ (for browsing the source)
- https://sources.debian.net/src/lz4/1.9.4-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/lz4/1.9.4-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `mawk=1.3.4.20240905-1`

Binary Packages:

- `mawk=1.3.4.20240905-1`

Licenses: (parsed from: `/usr/share/doc/mawk/copyright`)

- `CC-BY-3.0`
- `GPL-2`
- `GPL-2.0-only`
- `X11`

Source:

```console
$ apt-get source -qq --print-uris mawk=1.3.4.20240905-1
'http://deb.debian.org/debian/pool/main/m/mawk/mawk_1.3.4.20240905-1.dsc' mawk_1.3.4.20240905-1.dsc 2969 SHA256:df6bed9b7f37975fb7228fa5a3eb381bfe67cb3f3a4333ea8e69ddab4c881177
'http://deb.debian.org/debian/pool/main/m/mawk/mawk_1.3.4.20240905.orig.tar.gz' mawk_1.3.4.20240905.orig.tar.gz 423935 SHA256:a39967927dfa1b0116efc45b944a0f5b5b4c34f8e842a4b223dcdd7b367399e0
'http://deb.debian.org/debian/pool/main/m/mawk/mawk_1.3.4.20240905.orig.tar.gz.asc' mawk_1.3.4.20240905.orig.tar.gz.asc 729 SHA256:4360beec9fc972eba02f7af0a5340bd9a420c810d2424f50d34104b17386ac56
'http://deb.debian.org/debian/pool/main/m/mawk/mawk_1.3.4.20240905-1.debian.tar.xz' mawk_1.3.4.20240905-1.debian.tar.xz 15980 SHA256:3908cbe4d9c42f8cca1f2d3a5c77d6a9a630696c375ac25b99a19277d7925443
```

Other potentially useful URLs:

- https://sources.debian.net/src/mawk/1.3.4.20240905-1/ (for browsing the source)
- https://sources.debian.net/src/mawk/1.3.4.20240905-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/mawk/1.3.4.20240905-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `ncurses=6.5-2`

Binary Packages:

- `libtinfo6:amd64=6.5-2+b1`
- `ncurses-base=6.5-2`
- `ncurses-bin=6.5-2+b1`

Licenses: (parsed from: `/usr/share/doc/libtinfo6/copyright`, `/usr/share/doc/ncurses-base/copyright`, `/usr/share/doc/ncurses-bin/copyright`)

- `BSD-3-clause`
- `MIT/X11`
- `X11`

Source:

```console
$ apt-get source -qq --print-uris ncurses=6.5-2
'http://deb.debian.org/debian/pool/main/n/ncurses/ncurses_6.5-2.dsc' ncurses_6.5-2.dsc 3799 SHA256:c55a25d4697a881a12f98d9e69448a879fca1391663768822a7cc981b62b2b4c
'http://deb.debian.org/debian/pool/main/n/ncurses/ncurses_6.5.orig.tar.gz' ncurses_6.5.orig.tar.gz 3688489 SHA256:136d91bc269a9a5785e5f9e980bc76ab57428f604ce3e5a5a90cebc767971cc6
'http://deb.debian.org/debian/pool/main/n/ncurses/ncurses_6.5.orig.tar.gz.asc' ncurses_6.5.orig.tar.gz.asc 729 SHA256:c7541cdb9e27c159548d6ab2115b4e923d06d174dce7307f4a943de9421f3751
'http://deb.debian.org/debian/pool/main/n/ncurses/ncurses_6.5-2.debian.tar.xz' ncurses_6.5-2.debian.tar.xz 49852 SHA256:19df80accc1c6d978ca54eba2542ea77248e7a894bbf42a093aee0b4981fddf3
```

Other potentially useful URLs:

- https://sources.debian.net/src/ncurses/6.5-2/ (for browsing the source)
- https://sources.debian.net/src/ncurses/6.5-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/ncurses/6.5-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `nettle=3.10-1`

Binary Packages:

- `libhogweed6t64:amd64=3.10-1+b1`
- `libnettle8t64:amd64=3.10-1+b1`

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
$ apt-get source -qq --print-uris nettle=3.10-1
'http://deb.debian.org/debian/pool/main/n/nettle/nettle_3.10-1.dsc' nettle_3.10-1.dsc 2276 SHA256:25c9563ad861d8c62246687cc1aaace7d897db0e1aa287ef68485b89687aa739
'http://deb.debian.org/debian/pool/main/n/nettle/nettle_3.10.orig.tar.gz' nettle_3.10.orig.tar.gz 2640485 SHA256:b4c518adb174e484cb4acea54118f02380c7133771e7e9beb98a0787194ee47c
'http://deb.debian.org/debian/pool/main/n/nettle/nettle_3.10.orig.tar.gz.asc' nettle_3.10.orig.tar.gz.asc 573 SHA256:83f20f4bb5cc18335dacab8b8d01ddbae1b28453d889c5efcc2123987a8e09ca
'http://deb.debian.org/debian/pool/main/n/nettle/nettle_3.10-1.debian.tar.xz' nettle_3.10-1.debian.tar.xz 24936 SHA256:fd7181ca135b8a560b048ffba5b9f75e2ce7d0d61d3223c278c77ea89500b660
```

Other potentially useful URLs:

- https://sources.debian.net/src/nettle/3.10-1/ (for browsing the source)
- https://sources.debian.net/src/nettle/3.10-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/nettle/3.10-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `openssl=3.3.2-2`

Binary Packages:

- `libssl3t64:amd64=3.3.2-2`
- `openssl-provider-legacy=3.3.2-2`

Licenses: (parsed from: `/usr/share/doc/libssl3t64/copyright`, `/usr/share/doc/openssl-provider-legacy/copyright`)

- `Apache-2.0`
- `Artistic`
- `GPL-1`
- `GPL-1+`

Source:

```console
$ apt-get source -qq --print-uris openssl=3.3.2-2
'http://deb.debian.org/debian/pool/main/o/openssl/openssl_3.3.2-2.dsc' openssl_3.3.2-2.dsc 2808 SHA256:4a2d357c049c5f0da96fb9615e6ddbfface5a71de1dfa8a95120a251d1a3105d
'http://deb.debian.org/debian/pool/main/o/openssl/openssl_3.3.2.orig.tar.gz' openssl_3.3.2.orig.tar.gz 18076531 SHA256:2e8a40b01979afe8be0bbfb3de5dc1c6709fedb46d6c89c10da114ab5fc3d281
'http://deb.debian.org/debian/pool/main/o/openssl/openssl_3.3.2.orig.tar.gz.asc' openssl_3.3.2.orig.tar.gz.asc 833 SHA256:8a9ba21af0d770b3f9ee098269cfeb220a8b296639e6ad5d0593ffb7a15a742b
'http://deb.debian.org/debian/pool/main/o/openssl/openssl_3.3.2-2.debian.tar.xz' openssl_3.3.2-2.debian.tar.xz 52228 SHA256:d5d0c7c5a35e10b580b016866a75a454da3b477f90516501fa1861989befc33b
```

Other potentially useful URLs:

- https://sources.debian.net/src/openssl/3.3.2-2/ (for browsing the source)
- https://sources.debian.net/src/openssl/3.3.2-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/openssl/3.3.2-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `p11-kit=0.25.5-2`

Binary Packages:

- `libp11-kit0:amd64=0.25.5-2+b1`

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
$ apt-get source -qq --print-uris p11-kit=0.25.5-2
'http://deb.debian.org/debian/pool/main/p/p11-kit/p11-kit_0.25.5-2.dsc' p11-kit_0.25.5-2.dsc 2538 SHA256:5953f5639503fe32217117e222bbc231130d9e79dda74259b4017b7bfc5bd910
'http://deb.debian.org/debian/pool/main/p/p11-kit/p11-kit_0.25.5.orig.tar.xz' p11-kit_0.25.5.orig.tar.xz 1002056 SHA256:04d0a86450cdb1be018f26af6699857171a188ac6d5b8c90786a60854e1198e5
'http://deb.debian.org/debian/pool/main/p/p11-kit/p11-kit_0.25.5.orig.tar.xz.asc' p11-kit_0.25.5.orig.tar.xz.asc 228 SHA256:066c92b9d2accb2fda6a2f71e676fb6526fcc153051b1f04ee7d7c8c96a09989
'http://deb.debian.org/debian/pool/main/p/p11-kit/p11-kit_0.25.5-2.debian.tar.xz' p11-kit_0.25.5-2.debian.tar.xz 24108 SHA256:df84eb66f6dd2a53796dfbb2edc58a4b37046b19a8d186baf072163cd6c9c528
```

Other potentially useful URLs:

- https://sources.debian.net/src/p11-kit/0.25.5-2/ (for browsing the source)
- https://sources.debian.net/src/p11-kit/0.25.5-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/p11-kit/0.25.5-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `pam=1.5.3-7`

Binary Packages:

- `libpam-modules:amd64=1.5.3-7+b1`
- `libpam-modules-bin=1.5.3-7+b1`
- `libpam-runtime=1.5.3-7`
- `libpam0g:amd64=1.5.3-7+b1`

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
$ apt-get source -qq --print-uris pam=1.5.3-7
'http://deb.debian.org/debian/pool/main/p/pam/pam_1.5.3-7.dsc' pam_1.5.3-7.dsc 2253 SHA256:05666dde2c8057ff436975a5da7dad91210ab5a5dfdaea43976ac4a6bc75b1e7
'http://deb.debian.org/debian/pool/main/p/pam/pam_1.5.3.orig.tar.xz' pam_1.5.3.orig.tar.xz 1020076 SHA256:7ac4b50feee004a9fa88f1dfd2d2fa738a82896763050cd773b3c54b0a818283
'http://deb.debian.org/debian/pool/main/p/pam/pam_1.5.3.orig.tar.xz.asc' pam_1.5.3.orig.tar.xz.asc 801 SHA256:ce5690766060d60a8f0fba447f480d8d49988821740698cbdf2ecfd84dc8895c
'http://deb.debian.org/debian/pool/main/p/pam/pam_1.5.3-7.debian.tar.xz' pam_1.5.3-7.debian.tar.xz 139288 SHA256:494106a8f40a5436b82f8955e04a83598439b48636f16a30d0b6a32d86d0fc61
```

Other potentially useful URLs:

- https://sources.debian.net/src/pam/1.5.3-7/ (for browsing the source)
- https://sources.debian.net/src/pam/1.5.3-7/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/pam/1.5.3-7/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `pcre2=10.44-4`

Binary Packages:

- `libpcre2-8-0:amd64=10.44-4`

Licenses: (parsed from: `/usr/share/doc/libpcre2-8-0/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `BSD-3-clause-Cambridge with BINARY LIBRARY-LIKE PACKAGES exception`
- `X11`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/pcre2/10.44-4/


### `dpkg` source package: `perl=5.40.0-8`

Binary Packages:

- `perl-base=5.40.0-8`

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
$ apt-get source -qq --print-uris perl=5.40.0-8
'http://deb.debian.org/debian/pool/main/p/perl/perl_5.40.0-8.dsc' perl_5.40.0-8.dsc 2933 SHA256:8e28c6d3de17f273c8c56888c6e9ae18f76f680e5bb4f805b4abb5f8d1da5387
'http://deb.debian.org/debian/pool/main/p/perl/perl_5.40.0.orig-regen-configure.tar.xz' perl_5.40.0.orig-regen-configure.tar.xz 421080 SHA256:9b1f7f1f680cfd0174d1e11b4f8d06cce079798a0549f083f1c9ba15156be211
'http://deb.debian.org/debian/pool/main/p/perl/perl_5.40.0.orig.tar.xz' perl_5.40.0.orig.tar.xz 13804184 SHA256:d5325300ad267624cb0b7d512cfdfcd74fa7fe00c455c5b51a6bd53e5e199ef9
'http://deb.debian.org/debian/pool/main/p/perl/perl_5.40.0-8.debian.tar.xz' perl_5.40.0-8.debian.tar.xz 168236 SHA256:dc3776e2abbef5be6d533b8f9ce926b5770ae36025386679476fdf237e33f736
```

Other potentially useful URLs:

- https://sources.debian.net/src/perl/5.40.0-8/ (for browsing the source)
- https://sources.debian.net/src/perl/5.40.0-8/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/perl/5.40.0-8/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/s/sed/sed_4.9-2.dsc' sed_4.9-2.dsc 1860 SHA256:17f10deac1b327cb2a623352cdc33444ac9c109359a0caa46b3980b0e415f671
'http://deb.debian.org/debian/pool/main/s/sed/sed_4.9.orig.tar.xz' sed_4.9.orig.tar.xz 1397092 SHA256:6e226b732e1cd739464ad6862bd1a1aba42d7982922da7a53519631d24975181
'http://deb.debian.org/debian/pool/main/s/sed/sed_4.9-2.debian.tar.xz' sed_4.9-2.debian.tar.xz 62756 SHA256:549fa5cec6eb4fde8cc74ca263b8bf42f947ede677e39d2afeedf661da1d4e52
```

Other potentially useful URLs:

- https://sources.debian.net/src/sed/4.9-2/ (for browsing the source)
- https://sources.debian.net/src/sed/4.9-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/sed/4.9-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `shadow=1:4.16.0-5`

Binary Packages:

- `login.defs=1:4.16.0-5`
- `passwd=1:4.16.0-5`

Licenses: (parsed from: `/usr/share/doc/login.defs/copyright`, `/usr/share/doc/passwd/copyright`)

- `BSD-3-clause`
- `GPL-1`
- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/shadow/1:4.16.0-5/


### `dpkg` source package: `systemd=257~rc3-1`

Binary Packages:

- `libsystemd0:amd64=257~rc3-1`
- `libudev1:amd64=257~rc3-1`

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
$ apt-get source -qq --print-uris systemd=257~rc3-1
'http://deb.debian.org/debian/pool/main/s/systemd/systemd_257%7erc3-1.dsc' systemd_257~rc3-1.dsc 8665 SHA256:a7340c356731febbaeec44f360932cc9f9b5b7bae025c494b1f74f00b1edcd96
'http://deb.debian.org/debian/pool/main/s/systemd/systemd_257%7erc3.orig.tar.gz' systemd_257~rc3.orig.tar.gz 16226197 SHA256:bb0837988c3fb9b60d8ad38be791663a30cdb606242665f1157e1d884e2d892a
'http://deb.debian.org/debian/pool/main/s/systemd/systemd_257%7erc3-1.debian.tar.xz' systemd_257~rc3-1.debian.tar.xz 175832 SHA256:c068395d476f335812b83a72379072f04b4dd5a2edaff2e9ea149863db644a5b
```

Other potentially useful URLs:

- https://sources.debian.net/src/systemd/257~rc3-1/ (for browsing the source)
- https://sources.debian.net/src/systemd/257~rc3-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/systemd/257~rc3-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `sysvinit=3.11-1`

Binary Packages:

- `sysvinit-utils=3.11-1`

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
$ apt-get source -qq --print-uris sysvinit=3.11-1
'http://deb.debian.org/debian/pool/main/s/sysvinit/sysvinit_3.11-1.dsc' sysvinit_3.11-1.dsc 2347 SHA256:ba903d31738ab67544f8517f97c316909db1151da4218423b2a5666322842634
'http://deb.debian.org/debian/pool/main/s/sysvinit/sysvinit_3.11.orig.tar.gz' sysvinit_3.11.orig.tar.gz 514791 SHA256:32dd3370c2fb55cac87ee6b8e25074f769fd3ef1122ecfbb19fd7fea8a4d0414
'http://deb.debian.org/debian/pool/main/s/sysvinit/sysvinit_3.11-1.debian.tar.xz' sysvinit_3.11-1.debian.tar.xz 121272 SHA256:8fd6c705ebc0c5136e7ecbf2819eabf4fbba66476a3778cdd44d7ff9e8495205
```

Other potentially useful URLs:

- https://sources.debian.net/src/sysvinit/3.11-1/ (for browsing the source)
- https://sources.debian.net/src/sysvinit/3.11-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/sysvinit/3.11-1/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/t/tar/tar_1.35%2bdfsg-3.dsc' tar_1.35+dfsg-3.dsc 2009 SHA256:0ea713a8af04a41d297202e7ac20813735328a5f8d4de3882fba5595709955f8
'http://deb.debian.org/debian/pool/main/t/tar/tar_1.35%2bdfsg.orig.tar.xz' tar_1.35+dfsg.orig.tar.xz 2111608 SHA256:9ae57e981c1e73c0eebc2b26c9b0c4497fe310ef1d516ea430efb5470b71f7a8
'http://deb.debian.org/debian/pool/main/t/tar/tar_1.35%2bdfsg-3.debian.tar.xz' tar_1.35+dfsg-3.debian.tar.xz 20824 SHA256:6028f2172de2498b8fc2baef4854796d829ae7ba2a91de4f7615fe1a56729313
```

Other potentially useful URLs:

- https://sources.debian.net/src/tar/1.35+dfsg-3/ (for browsing the source)
- https://sources.debian.net/src/tar/1.35+dfsg-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/tar/1.35+dfsg-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `tzdata=2024b-3`

Binary Packages:

- `tzdata=2024b-3`

Licenses: (parsed from: `/usr/share/doc/tzdata/copyright`)

- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/tzdata/2024b-3/


### `dpkg` source package: `usrmerge=39`

Binary Packages:

- `usr-is-merged=39`

Licenses: (parsed from: `/usr/share/doc/usr-is-merged/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris usrmerge=39
'http://deb.debian.org/debian/pool/main/u/usrmerge/usrmerge_39.dsc' usrmerge_39.dsc 981 SHA256:44027067423faefd31ac321c283fc9b07184fecbd5304ed41490c03825b89a28
'http://deb.debian.org/debian/pool/main/u/usrmerge/usrmerge_39.tar.xz' usrmerge_39.tar.xz 14908 SHA256:90b4ee198469292da4ee8b4ce2ec7b3ec439d61e6beb3ed9d3fa82b0e46e7fa3
```

Other potentially useful URLs:

- https://sources.debian.net/src/usrmerge/39/ (for browsing the source)
- https://sources.debian.net/src/usrmerge/39/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/usrmerge/39/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `util-linux=2.40.2-11`

Binary Packages:

- `bsdutils=1:2.40.2-11`
- `libblkid1:amd64=2.40.2-11`
- `libmount1:amd64=2.40.2-11`
- `libsmartcols1:amd64=2.40.2-11`
- `libuuid1:amd64=2.40.2-11`
- `login=1:4.16.0-2+really2.40.2-11`
- `mount=2.40.2-11`
- `util-linux=2.40.2-11`

Licenses: (parsed from: `/usr/share/doc/bsdutils/copyright`, `/usr/share/doc/libblkid1/copyright`, `/usr/share/doc/libmount1/copyright`, `/usr/share/doc/libsmartcols1/copyright`, `/usr/share/doc/libuuid1/copyright`, `/usr/share/doc/login/copyright`, `/usr/share/doc/mount/copyright`, `/usr/share/doc/util-linux/copyright`)

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

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/util-linux/2.40.2-11/


### `dpkg` source package: `xxhash=0.8.2-2`

Binary Packages:

- `libxxhash0:amd64=0.8.2-2+b2`

Licenses: (parsed from: `/usr/share/doc/libxxhash0/copyright`)

- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris xxhash=0.8.2-2
'http://deb.debian.org/debian/pool/main/x/xxhash/xxhash_0.8.2-2.dsc' xxhash_0.8.2-2.dsc 1969 SHA256:8fbf9f5a50a4cf48e771e157e386bd2b2938e46cecd4bc53117ee1a4a615af1d
'http://deb.debian.org/debian/pool/main/x/xxhash/xxhash_0.8.2.orig.tar.gz' xxhash_0.8.2.orig.tar.gz 1141188 SHA256:baee0c6afd4f03165de7a4e67988d16f0f2b257b51d0e3cb91909302a26a79c4
'http://deb.debian.org/debian/pool/main/x/xxhash/xxhash_0.8.2-2.debian.tar.xz' xxhash_0.8.2-2.debian.tar.xz 4920 SHA256:fcbdd52df60936173524743680f6d3c504b9a90553fe113cd0aa531faf4f2c4d
```

Other potentially useful URLs:

- https://sources.debian.net/src/xxhash/0.8.2-2/ (for browsing the source)
- https://sources.debian.net/src/xxhash/0.8.2-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/xxhash/0.8.2-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `xz-utils=5.6.3-1`

Binary Packages:

- `liblzma5:amd64=5.6.3-1+b1`

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
$ apt-get source -qq --print-uris xz-utils=5.6.3-1
'http://deb.debian.org/debian/pool/main/x/xz-utils/xz-utils_5.6.3-1.dsc' xz-utils_5.6.3-1.dsc 2704 SHA256:840b9ae0e893d043de548c6df65a3a957dcd3977723eccf308ae8a61bb5dd288
'http://deb.debian.org/debian/pool/main/x/xz-utils/xz-utils_5.6.3.orig.tar.xz' xz-utils_5.6.3.orig.tar.xz 1328224 SHA256:db0590629b6f0fa36e74aea5f9731dc6f8df068ce7b7bafa45301832a5eebc3a
'http://deb.debian.org/debian/pool/main/x/xz-utils/xz-utils_5.6.3.orig.tar.xz.asc' xz-utils_5.6.3.orig.tar.xz.asc 833 SHA256:76b873c890e0b2cc0d3e790183d58acad724a8856a9ecb8491e127e5e5049837
'http://deb.debian.org/debian/pool/main/x/xz-utils/xz-utils_5.6.3-1.debian.tar.xz' xz-utils_5.6.3-1.debian.tar.xz 24548 SHA256:5de83aba4db209d8a30b9aaa390a8009086c42e1575a92182cb234c73c784f58
```

Other potentially useful URLs:

- https://sources.debian.net/src/xz-utils/5.6.3-1/ (for browsing the source)
- https://sources.debian.net/src/xz-utils/5.6.3-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/xz-utils/5.6.3-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `zlib=1:1.3.dfsg+really1.3.1-1`

Binary Packages:

- `zlib1g:amd64=1:1.3.dfsg+really1.3.1-1+b1`

Licenses: (parsed from: `/usr/share/doc/zlib1g/copyright`)

- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris zlib=1:1.3.dfsg+really1.3.1-1
'http://deb.debian.org/debian/pool/main/z/zlib/zlib_1.3.dfsg%2breally1.3.1-1.dsc' zlib_1.3.dfsg+really1.3.1-1.dsc 2637 SHA256:ede2791e29c1d3b422f9208bdd7edf040c20445ea1e7453a72037576e64fa197
'http://deb.debian.org/debian/pool/main/z/zlib/zlib_1.3.dfsg%2breally1.3.1.orig.tar.gz' zlib_1.3.dfsg+really1.3.1.orig.tar.gz 1325737 SHA256:60dd315c07f616887caa029408308a018ace66e3d142726a97db164b3b8f69fb
'http://deb.debian.org/debian/pool/main/z/zlib/zlib_1.3.dfsg%2breally1.3.1-1.debian.tar.xz' zlib_1.3.dfsg+really1.3.1-1.debian.tar.xz 16576 SHA256:9ed525955ce9fb0c1b39be8ff98f73450dbfc6305a9a27e6149c8972d38a0a9e
```

Other potentially useful URLs:

- https://sources.debian.net/src/zlib/1:1.3.dfsg+really1.3.1-1/ (for browsing the source)
- https://sources.debian.net/src/zlib/1:1.3.dfsg+really1.3.1-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/zlib/1:1.3.dfsg+really1.3.1-1/ (for access to the source package after it no longer exists in the archive)
