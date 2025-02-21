# `debian:trixie`

## Docker Metadata

- Image ID: `sha256:cf2d3b18757c46c0300732da55274bad7c291a4f89600dcd5634a11e7cea0bd0`
- Created: `2025-02-03T00:00:00Z`
- Virtual Size: ~ 117.89 Mb  
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

### `dpkg` source package: `apt=2.9.23`

Binary Packages:

- `apt=2.9.23`
- `libapt-pkg6.0t64:amd64=2.9.23`

Licenses: (parsed from: `/usr/share/doc/apt/copyright`, `/usr/share/doc/libapt-pkg6.0t64/copyright`)

- `BSD-3-clause`
- `Expat`
- `GPL-2`
- `GPL-2+`
- `curl`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/apt/2.9.23/


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
- `libaudit1:amd64=1:4.0.2-2+b1`

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

### `dpkg` source package: `base-passwd=3.6.6`

Binary Packages:

- `base-passwd=3.6.6`

Licenses: (parsed from: `/usr/share/doc/base-passwd/copyright`)

- `GPL-2`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris base-passwd=3.6.6
'http://deb.debian.org/debian/pool/main/b/base-passwd/base-passwd_3.6.6.dsc' base-passwd_3.6.6.dsc 1844 SHA256:c751de08700db6c297f6795982fec0751b4a5a65b645c357e87dfe09eb5e54d0
'http://deb.debian.org/debian/pool/main/b/base-passwd/base-passwd_3.6.6.tar.xz' base-passwd_3.6.6.tar.xz 60116 SHA256:cfcb17a5cfb5d7ce53f062b2a30c74ac7f9425af81010d3591aeffc60f269263
```

Other potentially useful URLs:

- https://sources.debian.net/src/base-passwd/3.6.6/ (for browsing the source)
- https://sources.debian.net/src/base-passwd/3.6.6/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/base-passwd/3.6.6/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `bash=5.2.37-1`

Binary Packages:

- `bash=5.2.37-1`

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
$ apt-get source -qq --print-uris bash=5.2.37-1
'http://deb.debian.org/debian/pool/main/b/bash/bash_5.2.37-1.dsc' bash_5.2.37-1.dsc 2294 SHA256:b278d0b2286838ffaa2b6529306625337404cd1ae6b52e9db7e54282462c0e5e
'http://deb.debian.org/debian/pool/main/b/bash/bash_5.2.37.orig.tar.xz' bash_5.2.37.orig.tar.xz 5600932 SHA256:370704c9c859f4060b7df19055e43bb9b5fa09d887699cf6ba87885c5485d36a
'http://deb.debian.org/debian/pool/main/b/bash/bash_5.2.37-1.debian.tar.xz' bash_5.2.37-1.debian.tar.xz 88276 SHA256:262083ffaddbe164060c03df7316fa1eca817443f56a652bb807cd2f9f365c74
```

Other potentially useful URLs:

- https://sources.debian.net/src/bash/5.2.37-1/ (for browsing the source)
- https://sources.debian.net/src/bash/5.2.37-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/bash/5.2.37-1/ (for access to the source package after it no longer exists in the archive)

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

### `dpkg` source package: `cdebconf=0.277`

Binary Packages:

- `libdebconfclient0:amd64=0.277`

Licenses: (parsed from: `/usr/share/doc/libdebconfclient0/copyright`)

- `BSD-2-Clause`
- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris cdebconf=0.277
'http://deb.debian.org/debian/pool/main/c/cdebconf/cdebconf_0.277.dsc' cdebconf_0.277.dsc 2707 SHA256:12afc241658ae9bcbb11d239d06e708fb6138b417b7ce9c31ac642f57fcc4613
'http://deb.debian.org/debian/pool/main/c/cdebconf/cdebconf_0.277.tar.xz' cdebconf_0.277.tar.xz 285420 SHA256:93a72ed5c5cab66f1f7439908348aa3bd97c4fa4a47416694e5dc3add2866e7b
```

Other potentially useful URLs:

- https://sources.debian.net/src/cdebconf/0.277/ (for browsing the source)
- https://sources.debian.net/src/cdebconf/0.277/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/cdebconf/0.277/ (for access to the source package after it no longer exists in the archive)

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

### `dpkg` source package: `dash=0.5.12-11`

Binary Packages:

- `dash=0.5.12-11`

Licenses: (parsed from: `/usr/share/doc/dash/copyright`)

- `BSD-3-Clause`
- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/dash/0.5.12-11/


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

### `dpkg` source package: `debconf=1.5.89`

Binary Packages:

- `debconf=1.5.89`

Licenses: (parsed from: `/usr/share/doc/debconf/copyright`)

- `BSD-2-clause`

Source:

```console
$ apt-get source -qq --print-uris debconf=1.5.89
'http://deb.debian.org/debian/pool/main/d/debconf/debconf_1.5.89.dsc' debconf_1.5.89.dsc 2035 SHA256:a3c32a3d878fc5bb72ddc1dadeea6faa423cf7de538e8018188a066bde2504d3
'http://deb.debian.org/debian/pool/main/d/debconf/debconf_1.5.89.tar.xz' debconf_1.5.89.tar.xz 574672 SHA256:6af2627425307318d410659104241f9a3c51aef49e57b066950baa4b18ad995f
```

Other potentially useful URLs:

- https://sources.debian.net/src/debconf/1.5.89/ (for browsing the source)
- https://sources.debian.net/src/debconf/1.5.89/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/debconf/1.5.89/ (for access to the source package after it no longer exists in the archive)

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

### `dpkg` source package: `diffutils=1:3.10-2`

Binary Packages:

- `diffutils=1:3.10-2`

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
$ apt-get source -qq --print-uris diffutils=1:3.10-2
'http://deb.debian.org/debian/pool/main/d/diffutils/diffutils_3.10-2.dsc' diffutils_3.10-2.dsc 1737 SHA256:e66b646eec15edcd185e4cc085deb8fe2925912a632a40cc98017f66ffecbab4
'http://deb.debian.org/debian/pool/main/d/diffutils/diffutils_3.10.orig.tar.xz' diffutils_3.10.orig.tar.xz 1624240 SHA256:90e5e93cc724e4ebe12ede80df1634063c7a855692685919bfe60b556c9bd09e
'http://deb.debian.org/debian/pool/main/d/diffutils/diffutils_3.10.orig.tar.xz.asc' diffutils_3.10.orig.tar.xz.asc 833 SHA256:a94faf8f1baa04ff220f7b2ccb137c16337284e023ebc4a1d5df475c08d810f7
'http://deb.debian.org/debian/pool/main/d/diffutils/diffutils_3.10-2.debian.tar.xz' diffutils_3.10-2.debian.tar.xz 14244 SHA256:8791e985aa96c331a8994484936b0da5b86373648f32feb29d47864f0488d613
```

Other potentially useful URLs:

- https://sources.debian.net/src/diffutils/1:3.10-2/ (for browsing the source)
- https://sources.debian.net/src/diffutils/1:3.10-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/diffutils/1:3.10-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `dpkg=1.22.11`

Binary Packages:

- `dpkg=1.22.11`

Licenses: (parsed from: `/usr/share/doc/dpkg/copyright`)

- `GPL-2`
- `GPL-2+`
- `public-domain-s-s-d`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/dpkg/1.22.11/


### `dpkg` source package: `e2fsprogs=1.47.2-1`

Binary Packages:

- `e2fsprogs=1.47.2-1`
- `libcom-err2:amd64=1.47.2-1`
- `libext2fs2t64:amd64=1.47.2-1`
- `libss2:amd64=1.47.2-1`
- `logsave=1.47.2-1`

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
$ apt-get source -qq --print-uris e2fsprogs=1.47.2-1
'http://deb.debian.org/debian/pool/main/e/e2fsprogs/e2fsprogs_1.47.2-1.dsc' e2fsprogs_1.47.2-1.dsc 3032 SHA256:e6392801ad349ed0217c45684b61db03b33fae940ceb4de23b71a24dab4e1bfc
'http://deb.debian.org/debian/pool/main/e/e2fsprogs/e2fsprogs_1.47.2.orig.tar.gz' e2fsprogs_1.47.2.orig.tar.gz 9996725 SHA256:6dcd67ff9d8b13274ba3f088e4318be4f5b71412cd863524423fc49d39a6371f
'http://deb.debian.org/debian/pool/main/e/e2fsprogs/e2fsprogs_1.47.2.orig.tar.gz.asc' e2fsprogs_1.47.2.orig.tar.gz.asc 488 SHA256:2063f62a198dd3df21f789c990c2cf9b4a5de24ed55f0b78d86e97e98daffc9d
'http://deb.debian.org/debian/pool/main/e/e2fsprogs/e2fsprogs_1.47.2-1.debian.tar.xz' e2fsprogs_1.47.2-1.debian.tar.xz 92348 SHA256:b9d1c79da5b32975f5771a5c487edbd9301729e6e813018209f31e2897a46617
```

Other potentially useful URLs:

- https://sources.debian.net/src/e2fsprogs/1.47.2-1/ (for browsing the source)
- https://sources.debian.net/src/e2fsprogs/1.47.2-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/e2fsprogs/1.47.2-1/ (for access to the source package after it no longer exists in the archive)

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

### `dpkg` source package: `gcc-14=14.2.0-12`

Binary Packages:

- `gcc-14-base:amd64=14.2.0-12`
- `libgcc-s1:amd64=14.2.0-12`
- `libstdc++6:amd64=14.2.0-12`

Licenses: (parsed from: `/usr/share/doc/gcc-14-base/copyright`, `/usr/share/doc/libgcc-s1/copyright`, `/usr/share/doc/libstdc++6/copyright`)

- `Artistic`
- `GFDL-1.2`
- `GPL`
- `GPL-3`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris gcc-14=14.2.0-12
'http://deb.debian.org/debian/pool/main/g/gcc-14/gcc-14_14.2.0-12.dsc' gcc-14_14.2.0-12.dsc 47361 SHA256:bd9560d7103cf389e090c15a8466ffa98a4992282a0d03a4d5f86e59e4cfe22a
'http://deb.debian.org/debian/pool/main/g/gcc-14/gcc-14_14.2.0.orig.tar.gz' gcc-14_14.2.0.orig.tar.gz 94299633 SHA256:e162a5ef3f0077ecae598c6556908d2ab80841532df3398072a96a6df6e6aa29
'http://deb.debian.org/debian/pool/main/g/gcc-14/gcc-14_14.2.0-12.debian.tar.xz' gcc-14_14.2.0-12.debian.tar.xz 2476312 SHA256:5468b4d838a7b168ecfcc031c50f7c9c33ff35e29545508a9979afe7667b7fc2
```

Other potentially useful URLs:

- https://sources.debian.net/src/gcc-14/14.2.0-12/ (for browsing the source)
- https://sources.debian.net/src/gcc-14/14.2.0-12/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/gcc-14/14.2.0-12/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `glibc=2.40-6`

Binary Packages:

- `libc-bin=2.40-6`
- `libc6:amd64=2.40-6`

Licenses: (parsed from: `/usr/share/doc/libc-bin/copyright`, `/usr/share/doc/libc6/copyright`)

- `BSD-2-clause`
- `BSD-3-clause-Berkeley`
- `BSD-3-clause-Carnegie`
- `BSD-3-clause-Oracle`
- `BSD-3-clause-WIDE`
- `BSL-1.0`
- `Carnegie`
- `DEC`
- `FSFAP`
- `GPL-2`
- `GPL-2+`
- `GPL-2+-with-link-exception`
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
- `PCRE`
- `SunPro`
- `Unicode-DFS-2016`
- `Univ-Coimbra`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris glibc=2.40-6
'http://deb.debian.org/debian/pool/main/g/glibc/glibc_2.40-6.dsc' glibc_2.40-6.dsc 7550 SHA256:019d68ab54e3e4e96587d3074136bfb8e89a425ad811d09f594598451b2bfbc8
'http://deb.debian.org/debian/pool/main/g/glibc/glibc_2.40.orig.tar.xz' glibc_2.40.orig.tar.xz 19517224 SHA256:0b89b8c058eaa0f1121a814be6196ce2048235b43d95714ce8278fe72c7cc34a
'http://deb.debian.org/debian/pool/main/g/glibc/glibc_2.40-6.debian.tar.xz' glibc_2.40-6.debian.tar.xz 458644 SHA256:fef3a1db6b8c45407897f4b0da3e718947ee78a4bf3a9e735172623df5d22e8c
```

Other potentially useful URLs:

- https://sources.debian.net/src/glibc/2.40-6/ (for browsing the source)
- https://sources.debian.net/src/glibc/2.40-6/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/glibc/2.40-6/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `gmp=2:6.3.0+dfsg-3`

Binary Packages:

- `libgmp10:amd64=2:6.3.0+dfsg-3`

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
$ apt-get source -qq --print-uris gmp=2:6.3.0+dfsg-3
'http://deb.debian.org/debian/pool/main/g/gmp/gmp_6.3.0%2bdfsg-3.dsc' gmp_6.3.0+dfsg-3.dsc 2251 SHA256:f7b64af28f52b7346bb8581e01d3c19daf769639345f234f8ae1e29c42171443
'http://deb.debian.org/debian/pool/main/g/gmp/gmp_6.3.0%2bdfsg.orig.tar.xz' gmp_6.3.0+dfsg.orig.tar.xz 1870556 SHA256:bd2966e6d277f79328e894a5a9f3ba3fbf2ed2be81def5f48623e30c23fb1572
'http://deb.debian.org/debian/pool/main/g/gmp/gmp_6.3.0%2bdfsg-3.debian.tar.xz' gmp_6.3.0+dfsg-3.debian.tar.xz 19912 SHA256:1d890bbe25dd649d2ddba1926483176520e50f22115a00566f250b613b8c20ad
```

Other potentially useful URLs:

- https://sources.debian.net/src/gmp/2:6.3.0+dfsg-3/ (for browsing the source)
- https://sources.debian.net/src/gmp/2:6.3.0+dfsg-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/gmp/2:6.3.0+dfsg-3/ (for access to the source package after it no longer exists in the archive)

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

### `dpkg` source package: `gzip=1.13-1`

Binary Packages:

- `gzip=1.13-1`

Licenses: (parsed from: `/usr/share/doc/gzip/copyright`)

- `FSF-manpages`
- `GFDL-1.3+-no-invariant`
- `GFDL-3`
- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris gzip=1.13-1
'http://deb.debian.org/debian/pool/main/g/gzip/gzip_1.13-1.dsc' gzip_1.13-1.dsc 1884 SHA256:4942638dbb63dc5690e0a95ed70ee9f11e93565c43941c2485da3e561ec72028
'http://deb.debian.org/debian/pool/main/g/gzip/gzip_1.13.orig.tar.xz' gzip_1.13.orig.tar.xz 838248 SHA256:7454eb6935db17c6655576c2e1b0fabefd38b4d0936e0f87f48cd062ce91a057
'http://deb.debian.org/debian/pool/main/g/gzip/gzip_1.13.orig.tar.xz.asc' gzip_1.13.orig.tar.xz.asc 833 SHA256:aa752d6460fff2e0064857f1c6057d2dc49a28a45ad28c6b29c525851d6771f1
'http://deb.debian.org/debian/pool/main/g/gzip/gzip_1.13-1.debian.tar.xz' gzip_1.13-1.debian.tar.xz 19028 SHA256:29319b3f91d8e03d940d4d7c0f2a5fe5ec4f2ba4a0e621c9ef2682f2d0240dd2
```

Other potentially useful URLs:

- https://sources.debian.net/src/gzip/1.13-1/ (for browsing the source)
- https://sources.debian.net/src/gzip/1.13-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/gzip/1.13-1/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/i/init-system-helpers/init-system-helpers_1.68.dsc' init-system-helpers_1.68.dsc 2209 SHA256:58bf10802cf5d2496059368948a80d4a49f768d27b918fbe6dc28353c6cda72c
'http://deb.debian.org/debian/pool/main/i/init-system-helpers/init-system-helpers_1.68.tar.xz' init-system-helpers_1.68.tar.xz 45168 SHA256:cdf1c7fe87362a4e3f7446a95b75c29ca6071fda3911adb269508203cd3c458d
```

Other potentially useful URLs:

- https://sources.debian.net/src/init-system-helpers/1.68/ (for browsing the source)
- https://sources.debian.net/src/init-system-helpers/1.68/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/init-system-helpers/1.68/ (for access to the source package after it no longer exists in the archive)

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

### `dpkg` source package: `libselinux=3.7-3.1`

Binary Packages:

- `libselinux1:amd64=3.7-3.1`

Licenses: (parsed from: `/usr/share/doc/libselinux1/copyright`)

- `GPL-2`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris libselinux=3.7-3.1
'http://deb.debian.org/debian/pool/main/libs/libselinux/libselinux_3.7-3.1.dsc' libselinux_3.7-3.1.dsc 2393 SHA256:4f043d9f3a173707e3caf0615e391a40909061bccdb874ae66ac8ff308eac1f0
'http://deb.debian.org/debian/pool/main/libs/libselinux/libselinux_3.7.orig.tar.gz' libselinux_3.7.orig.tar.gz 194834 SHA256:ea03f42d13a4f95757997dba8cf0b26321fac5d2f164418b4cc856a92d2b17bd
'http://deb.debian.org/debian/pool/main/libs/libselinux/libselinux_3.7.orig.tar.gz.asc' libselinux_3.7.orig.tar.gz.asc 833 SHA256:8dbd0457d227a7182b0a1f2f8659c2f4dd4ae837f5e69a17d1698f6c31c37f31
'http://deb.debian.org/debian/pool/main/libs/libselinux/libselinux_3.7-3.1.debian.tar.xz' libselinux_3.7-3.1.debian.tar.xz 42972 SHA256:64fe236a7d29ee53dd5263ab82fd5ce7bbe4dbbe30ceaacefe84d9e60484777c
```

Other potentially useful URLs:

- https://sources.debian.net/src/libselinux/3.7-3.1/ (for browsing the source)
- https://sources.debian.net/src/libselinux/3.7-3.1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libselinux/3.7-3.1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libsemanage=3.7-2.1`

Binary Packages:

- `libsemanage-common=3.7-2.1`
- `libsemanage2:amd64=3.7-2.1`

Licenses: (parsed from: `/usr/share/doc/libsemanage-common/copyright`, `/usr/share/doc/libsemanage2/copyright`)

- `GPL-2`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris libsemanage=3.7-2.1
'http://deb.debian.org/debian/pool/main/libs/libsemanage/libsemanage_3.7-2.1.dsc' libsemanage_3.7-2.1.dsc 2368 SHA256:7619c31cca56aacabf8bc9eec86db9e8fcf04dfb9568fb7b9e95816c110a6de2
'http://deb.debian.org/debian/pool/main/libs/libsemanage/libsemanage_3.7.orig.tar.gz' libsemanage_3.7.orig.tar.gz 182896 SHA256:e166cae29a417dab008db9ca0874023f353a3017b07693a036ed97487eda35b1
'http://deb.debian.org/debian/pool/main/libs/libsemanage/libsemanage_3.7.orig.tar.gz.asc' libsemanage_3.7.orig.tar.gz.asc 833 SHA256:02981e0224fdf0141fc29b950f7e5aab1653d5fee6dcbf6d6a5ff976e5720cc8
'http://deb.debian.org/debian/pool/main/libs/libsemanage/libsemanage_3.7-2.1.debian.tar.xz' libsemanage_3.7-2.1.debian.tar.xz 36680 SHA256:1625df7a9bcd8fa84a18d0a03bbf739ec6224fdac23c2e500d7c87620b789d17
```

Other potentially useful URLs:

- https://sources.debian.net/src/libsemanage/3.7-2.1/ (for browsing the source)
- https://sources.debian.net/src/libsemanage/3.7-2.1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libsemanage/3.7-2.1/ (for access to the source package after it no longer exists in the archive)

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

### `dpkg` source package: `libxcrypt=1:4.4.38-1`

Binary Packages:

- `libcrypt1:amd64=1:4.4.38-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxcrypt=1:4.4.38-1
'http://deb.debian.org/debian/pool/main/libx/libxcrypt/libxcrypt_4.4.38-1.dsc' libxcrypt_4.4.38-1.dsc 1573 SHA256:feba1874a84616791c1c17f9a290c9e97562b2904b3b0200edc82a2db54f3f07
'http://deb.debian.org/debian/pool/main/libx/libxcrypt/libxcrypt_4.4.38.orig.tar.xz' libxcrypt_4.4.38.orig.tar.xz 394216 SHA256:6a275a356622c64ba9f693892215dbb399c003a7a4afeed9c4c74070eaab20f4
'http://deb.debian.org/debian/pool/main/libx/libxcrypt/libxcrypt_4.4.38-1.debian.tar.xz' libxcrypt_4.4.38-1.debian.tar.xz 8512 SHA256:6b87bcb5325e417ab3f4c01c364233444b4c9008a69ec1d6fababb3f6e693a5e
```

Other potentially useful URLs:

- https://sources.debian.net/src/libxcrypt/1:4.4.38-1/ (for browsing the source)
- https://sources.debian.net/src/libxcrypt/1:4.4.38-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libxcrypt/1:4.4.38-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libzstd=1.5.6+dfsg-2`

Binary Packages:

- `libzstd1:amd64=1.5.6+dfsg-2`

Licenses: (parsed from: `/usr/share/doc/libzstd1/copyright`)

- `BSD-3-clause`
- `Expat`
- `GPL-2`
- `zlib`

Source:

```console
$ apt-get source -qq --print-uris libzstd=1.5.6+dfsg-2
'http://deb.debian.org/debian/pool/main/libz/libzstd/libzstd_1.5.6%2bdfsg-2.dsc' libzstd_1.5.6+dfsg-2.dsc 2369 SHA256:57f39cddb823019558f0f69f4fb9842a3b8c13cb3f9db8e6d8a7819c1e058b33
'http://deb.debian.org/debian/pool/main/libz/libzstd/libzstd_1.5.6%2bdfsg.orig.tar.xz' libzstd_1.5.6+dfsg.orig.tar.xz 1815380 SHA256:b3a60c7059886641830adf32c979be8d211da5d73fd05c7768f86d12d5bccec3
'http://deb.debian.org/debian/pool/main/libz/libzstd/libzstd_1.5.6%2bdfsg-2.debian.tar.xz' libzstd_1.5.6+dfsg-2.debian.tar.xz 23088 SHA256:5795e5c490e7087db756be093be00c02987ca7276713b7428e962a73b34294f1
```

Other potentially useful URLs:

- https://sources.debian.net/src/libzstd/1.5.6+dfsg-2/ (for browsing the source)
- https://sources.debian.net/src/libzstd/1.5.6+dfsg-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libzstd/1.5.6+dfsg-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `lz4=1.10.0-3`

Binary Packages:

- `liblz4-1:amd64=1.10.0-3`

Licenses: (parsed from: `/usr/share/doc/liblz4-1/copyright`)

- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris lz4=1.10.0-3
'http://deb.debian.org/debian/pool/main/l/lz4/lz4_1.10.0-3.dsc' lz4_1.10.0-3.dsc 1941 SHA256:2924972ba64b8f106f2bc56c697700047f8ff3f992265ef5e459219e512311eb
'http://deb.debian.org/debian/pool/main/l/lz4/lz4_1.10.0.orig.tar.gz' lz4_1.10.0.orig.tar.gz 387114 SHA256:537512904744b35e232912055ccf8ec66d768639ff3abe5788d90d792ec5f48b
'http://deb.debian.org/debian/pool/main/l/lz4/lz4_1.10.0-3.debian.tar.xz' lz4_1.10.0-3.debian.tar.xz 7484 SHA256:15b0f90c7c69c2e7b48edd075dc7df661abda62724adb745098e650abfa52af7
```

Other potentially useful URLs:

- https://sources.debian.net/src/lz4/1.10.0-3/ (for browsing the source)
- https://sources.debian.net/src/lz4/1.10.0-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/lz4/1.10.0-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `mawk=1.3.4.20240905-1`

Binary Packages:

- `mawk=1.3.4.20240905-1`

Licenses: (parsed from: `/usr/share/doc/mawk/copyright`)

- `CC-BY-3.0`
- `GPL-2`
- `GPL-2.0-only`
- `X11`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/mawk/1.3.4.20240905-1/


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

### `dpkg` source package: `openssl=3.4.0-2`

Binary Packages:

- `libssl3t64:amd64=3.4.0-2`
- `openssl-provider-legacy=3.4.0-2`

Licenses: (parsed from: `/usr/share/doc/libssl3t64/copyright`, `/usr/share/doc/openssl-provider-legacy/copyright`)

- `Apache-2.0`
- `Artistic`
- `GPL-1`
- `GPL-1+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/openssl/3.4.0-2/


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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/pam/1.5.3-7/


### `dpkg` source package: `pcre2=10.44-5`

Binary Packages:

- `libpcre2-8-0:amd64=10.44-5`

Licenses: (parsed from: `/usr/share/doc/libpcre2-8-0/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `BSD-3-clause-Cambridge with BINARY LIBRARY-LIKE PACKAGES exception`
- `X11`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris pcre2=10.44-5
'http://deb.debian.org/debian/pool/main/p/pcre2/pcre2_10.44-5.dsc' pcre2_10.44-5.dsc 2340 SHA256:6c27cbc1f6d00a5465b1f312363cec6a35a624a670475d13df21cc7cc8d54923
'http://deb.debian.org/debian/pool/main/p/pcre2/pcre2_10.44.orig.tar.gz' pcre2_10.44.orig.tar.gz 2552792 SHA256:86b9cb0aa3bcb7994faa88018292bc704cdbb708e785f7c74352ff6ea7d3175b
'http://deb.debian.org/debian/pool/main/p/pcre2/pcre2_10.44-5.diff.gz' pcre2_10.44-5.diff.gz 16032 SHA256:6077896df1f7fff961a3ee82ff29d571694f7fd85f030fc60d67f9bc326c395e
```

Other potentially useful URLs:

- https://sources.debian.net/src/pcre2/10.44-5/ (for browsing the source)
- https://sources.debian.net/src/pcre2/10.44-5/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/pcre2/10.44-5/ (for access to the source package after it no longer exists in the archive)

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/perl/5.40.0-8/


### `dpkg` source package: `rust-sequoia-sqv=1.2.1-5`

Binary Packages:

- `sqv=1.2.1-5`

Licenses: (parsed from: `/usr/share/doc/sqv/copyright`)

- `GPL-2`
- `GPL-2.0-or-later`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/rust-sequoia-sqv/1.2.1-5/


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

### `dpkg` source package: `shadow=1:4.16.0-7`

Binary Packages:

- `login.defs=1:4.16.0-7`
- `passwd=1:4.16.0-7`

Licenses: (parsed from: `/usr/share/doc/login.defs/copyright`, `/usr/share/doc/passwd/copyright`)

- `BSD-3-clause`
- `GPL-1`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris shadow=1:4.16.0-7
'http://deb.debian.org/debian/pool/main/s/shadow/shadow_4.16.0-7.dsc' shadow_4.16.0-7.dsc 2614 SHA256:c43f54503e32265b335a5a26c49b98371277dba2f8d189f2a76ff64365f94003
'http://deb.debian.org/debian/pool/main/s/shadow/shadow_4.16.0.orig.tar.xz' shadow_4.16.0.orig.tar.xz 2053720 SHA256:a0255570541a356c3718966987c8be0658691fda804826fda7576c8e69e0cfda
'http://deb.debian.org/debian/pool/main/s/shadow/shadow_4.16.0-7.debian.tar.xz' shadow_4.16.0-7.debian.tar.xz 170412 SHA256:24af58e3025ca769fcd9ce3e08f21059dcb85c3b14df93687c2b3d4cbace71d2
```

Other potentially useful URLs:

- https://sources.debian.net/src/shadow/1:4.16.0-7/ (for browsing the source)
- https://sources.debian.net/src/shadow/1:4.16.0-7/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/shadow/1:4.16.0-7/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `systemd=257.2-3`

Binary Packages:

- `libsystemd0:amd64=257.2-3`
- `libudev1:amd64=257.2-3`

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

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/systemd/257.2-3/


### `dpkg` source package: `sysvinit=3.13-1`

Binary Packages:

- `sysvinit-utils=3.13-1`

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

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/sysvinit/3.13-1/


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
'http://deb.debian.org/debian/pool/main/t/tar/tar_1.35%2bdfsg-3.1.dsc' tar_1.35+dfsg-3.1.dsc 2017 SHA256:5bb58d4966d94c99a9f1b182676089ecc05058d62fdb927f5c07539d9cda4077
'http://deb.debian.org/debian/pool/main/t/tar/tar_1.35%2bdfsg.orig.tar.xz' tar_1.35+dfsg.orig.tar.xz 2111608 SHA256:9ae57e981c1e73c0eebc2b26c9b0c4497fe310ef1d516ea430efb5470b71f7a8
'http://deb.debian.org/debian/pool/main/t/tar/tar_1.35%2bdfsg-3.1.debian.tar.xz' tar_1.35+dfsg-3.1.debian.tar.xz 21540 SHA256:0d0278034b82ed84dce04a461879b6e1871e4cb416a0ff04d3d35ff05fc30a53
```

Other potentially useful URLs:

- https://sources.debian.net/src/tar/1.35+dfsg-3.1/ (for browsing the source)
- https://sources.debian.net/src/tar/1.35+dfsg-3.1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/tar/1.35+dfsg-3.1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `tzdata=2024b-6`

Binary Packages:

- `tzdata=2024b-6`

Licenses: (parsed from: `/usr/share/doc/tzdata/copyright`)

- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/tzdata/2024b-6/


### `dpkg` source package: `util-linux=2.40.4-2`

Binary Packages:

- `bsdutils=1:2.40.4-2`
- `libblkid1:amd64=2.40.4-2`
- `libmount1:amd64=2.40.4-2`
- `libsmartcols1:amd64=2.40.4-2`
- `libuuid1:amd64=2.40.4-2`
- `login=1:4.16.0-2+really2.40.4-2`
- `mount=2.40.4-2`
- `util-linux=2.40.4-2`

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

- http://snapshot.debian.org/package/util-linux/2.40.4-2/


### `dpkg` source package: `xxhash=0.8.2-2`

Binary Packages:

- `libxxhash0:amd64=0.8.2-2+b2`

Licenses: (parsed from: `/usr/share/doc/libxxhash0/copyright`)

- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/xxhash/0.8.2-2/


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
