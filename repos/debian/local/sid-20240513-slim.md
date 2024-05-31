# `debian:sid-slim`

## Docker Metadata

- Image ID: `sha256:f05f51b876563495e98c11082e8e4d9f92dfa967449d47b93030bb3f9828a2b0`
- Created: `2024-05-14T01:29:45.616576131Z`
- Virtual Size: ~ 81.88 Mb  
  (total size of all layers on-disk)
- Arch: `linux`/`amd64`
- Command: `["bash"]`
- Environment:
  - `PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin`

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
'http://deb.debian.org/debian/pool/main/a/acl/acl_2.3.2-2.dsc' acl_2.3.2-2.dsc 2604 SHA256:1f42130ccb5442fe2db2aee1dcc03c51a31512dd2519a38e8fc9270c5abbc807
'http://deb.debian.org/debian/pool/main/a/acl/acl_2.3.2.orig.tar.xz' acl_2.3.2.orig.tar.xz 371680 SHA256:97203a72cae99ab89a067fe2210c1cbf052bc492b479eca7d226d9830883b0bd
'http://deb.debian.org/debian/pool/main/a/acl/acl_2.3.2.orig.tar.xz.asc' acl_2.3.2.orig.tar.xz.asc 833 SHA256:184c6a903490885a096095db67b433a04542c6569f167cbe8115268c0f227273
'http://deb.debian.org/debian/pool/main/a/acl/acl_2.3.2-2.debian.tar.xz' acl_2.3.2-2.debian.tar.xz 24296 SHA256:e27b6e194c0a7554595d76f96acdceb800631bdc46c36457b73bc7e4a0c5f2ee
```

Other potentially useful URLs:

- https://sources.debian.net/src/acl/2.3.2-2/ (for browsing the source)
- https://sources.debian.net/src/acl/2.3.2-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/acl/2.3.2-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `apt=2.9.2`

Binary Packages:

- `apt=2.9.2`
- `libapt-pkg6.0t64:amd64=2.9.2`

Licenses: (parsed from: `/usr/share/doc/apt/copyright`, `/usr/share/doc/libapt-pkg6.0t64/copyright`)

- `BSD-3-clause`
- `Expat`
- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/apt/2.9.2/


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
'http://deb.debian.org/debian/pool/main/a/attr/attr_2.5.2-1.dsc' attr_2.5.2-1.dsc 2477 SHA256:5c14953fc436d6c4ba6dd4a00b2f82a923d5745cc2c993a630e50d9cabaeca0b
'http://deb.debian.org/debian/pool/main/a/attr/attr_2.5.2.orig.tar.xz' attr_2.5.2.orig.tar.xz 334180 SHA256:f2e97b0ab7ce293681ab701915766190d607a1dba7fae8a718138150b700a70b
'http://deb.debian.org/debian/pool/main/a/attr/attr_2.5.2.orig.tar.xz.asc' attr_2.5.2.orig.tar.xz.asc 833 SHA256:eeac729088d3c6379e91b7596cb3582e46b047c47f0fa3c5c77f9c9e84dc3a4c
'http://deb.debian.org/debian/pool/main/a/attr/attr_2.5.2-1.debian.tar.xz' attr_2.5.2-1.debian.tar.xz 25848 SHA256:b4d0670ea47811670bb619252973c7fb186e54b28bd5f2ac3c1a34d6fd089741
```

Other potentially useful URLs:

- https://sources.debian.net/src/attr/1:2.5.2-1/ (for browsing the source)
- https://sources.debian.net/src/attr/1:2.5.2-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/attr/1:2.5.2-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `audit=1:3.1.2-2.1`

Binary Packages:

- `libaudit-common=1:3.1.2-2.1`
- `libaudit1:amd64=1:3.1.2-2.1`

Licenses: (parsed from: `/usr/share/doc/libaudit-common/copyright`, `/usr/share/doc/libaudit1/copyright`)

- `GPL-1`
- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris audit=1:3.1.2-2.1
'http://deb.debian.org/debian/pool/main/a/audit/audit_3.1.2-2.1.dsc' audit_3.1.2-2.1.dsc 2762 SHA256:da742208cdf29f867c2dac37075ae03b596f46b3e1534442e6197f2e91147db6
'http://deb.debian.org/debian/pool/main/a/audit/audit_3.1.2.orig.tar.gz' audit_3.1.2.orig.tar.gz 1219860 SHA256:c0b1792d1f0a88c6f1828710509cbb987059fc68712c97669ca90eae103d287d
'http://deb.debian.org/debian/pool/main/a/audit/audit_3.1.2-2.1.debian.tar.xz' audit_3.1.2-2.1.debian.tar.xz 18696 SHA256:9660ada28d07bed94d34a4d8a0446881d927e172cc386b92357afec064a4352c
```

Other potentially useful URLs:

- https://sources.debian.net/src/audit/1:3.1.2-2.1/ (for browsing the source)
- https://sources.debian.net/src/audit/1:3.1.2-2.1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/audit/1:3.1.2-2.1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `base-files=13.2`

Binary Packages:

- `base-files=13.2`

Licenses: (parsed from: `/usr/share/doc/base-files/copyright`)

- `GPL`
- `GPL-2+`
- `verbatim`

Source:

```console
$ apt-get source -qq --print-uris base-files=13.2
'http://deb.debian.org/debian/pool/main/b/base-files/base-files_13.2.dsc' base-files_13.2.dsc 1101 SHA256:61fe2e331fff0bea1c9645f4f0c6ed95fd39840581859fb5325f1ecf6e650e30
'http://deb.debian.org/debian/pool/main/b/base-files/base-files_13.2.tar.xz' base-files_13.2.tar.xz 66928 SHA256:8319e3ca08917d6e219e620a4607a4f2ebda89c315f7d12694746ee6c5275471
```

Other potentially useful URLs:

- https://sources.debian.net/src/base-files/13.2/ (for browsing the source)
- https://sources.debian.net/src/base-files/13.2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/base-files/13.2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `base-passwd=3.6.3`

Binary Packages:

- `base-passwd=3.6.3`

Licenses: (parsed from: `/usr/share/doc/base-passwd/copyright`)

- `GPL-2`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris base-passwd=3.6.3
'http://deb.debian.org/debian/pool/main/b/base-passwd/base-passwd_3.6.3.dsc' base-passwd_3.6.3.dsc 1762 SHA256:bac1a87f919fd8ab28480cc1fd8126b2068a577faf4223f8a2be6baf328d313e
'http://deb.debian.org/debian/pool/main/b/base-passwd/base-passwd_3.6.3.tar.xz' base-passwd_3.6.3.tar.xz 58284 SHA256:83575327d8318a419caf2d543341215c046044073d1afec2acc0ac4d8095ff39
```

Other potentially useful URLs:

- https://sources.debian.net/src/base-passwd/3.6.3/ (for browsing the source)
- https://sources.debian.net/src/base-passwd/3.6.3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/base-passwd/3.6.3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `bash=5.2.21-2`

Binary Packages:

- `bash=5.2.21-2+b1`

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
$ apt-get source -qq --print-uris bash=5.2.21-2
'http://deb.debian.org/debian/pool/main/b/bash/bash_5.2.21-2.dsc' bash_5.2.21-2.dsc 2295 SHA256:134867cb0fb5bd81fcb3b90cf9e54db4eb8fa6c4ef65bfc6fe6d4c2a0703a8af
'http://deb.debian.org/debian/pool/main/b/bash/bash_5.2.21.orig.tar.xz' bash_5.2.21.orig.tar.xz 5598816 SHA256:ec21ab4efd6bd7a6e2802fbda622b81bfc43a8095d721234d4bf075797683014
'http://deb.debian.org/debian/pool/main/b/bash/bash_5.2.21-2.debian.tar.xz' bash_5.2.21-2.debian.tar.xz 87876 SHA256:419795e70b50d57effe7b993cbdf47ea57d5a59de9eb8a30b46a1a6057381344
```

Other potentially useful URLs:

- https://sources.debian.net/src/bash/5.2.21-2/ (for browsing the source)
- https://sources.debian.net/src/bash/5.2.21-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/bash/5.2.21-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `bzip2=1.0.8-5.1`

Binary Packages:

- `libbz2-1.0:amd64=1.0.8-5.1`

Licenses: (parsed from: `/usr/share/doc/libbz2-1.0/copyright`)

- `BSD-variant`
- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris bzip2=1.0.8-5.1
'http://deb.debian.org/debian/pool/main/b/bzip2/bzip2_1.0.8-5.1.dsc' bzip2_1.0.8-5.1.dsc 2189 SHA256:210e367658236ea084627394015d466554f1ed2353a5feee5756335dc56074e6
'http://deb.debian.org/debian/pool/main/b/bzip2/bzip2_1.0.8.orig.tar.gz' bzip2_1.0.8.orig.tar.gz 810029 SHA256:ab5a03176ee106d3f0fa90e381da478ddae405918153cca248e682cd0c4a2269
'http://deb.debian.org/debian/pool/main/b/bzip2/bzip2_1.0.8-5.1.debian.tar.bz2' bzip2_1.0.8-5.1.debian.tar.bz2 26823 SHA256:8d07df2356a8105cc1ad4a64eba54c89aeb732fdc285e845cea1f6f66dda432d
```

Other potentially useful URLs:

- https://sources.debian.net/src/bzip2/1.0.8-5.1/ (for browsing the source)
- https://sources.debian.net/src/bzip2/1.0.8-5.1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/bzip2/1.0.8-5.1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `cdebconf=0.271`

Binary Packages:

- `libdebconfclient0:amd64=0.271+b3`

Licenses: (parsed from: `/usr/share/doc/libdebconfclient0/copyright`)

- `BSD-2-Clause`
- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris cdebconf=0.271
'http://deb.debian.org/debian/pool/main/c/cdebconf/cdebconf_0.271.dsc' cdebconf_0.271.dsc 2707 SHA256:626c8da9b0fd07f37c94940401a8ba92bc3c454673c266e9c927934139e2a079
'http://deb.debian.org/debian/pool/main/c/cdebconf/cdebconf_0.271.tar.xz' cdebconf_0.271.tar.xz 284308 SHA256:b66fd2ea674d22f64a01672fe6c1891ef54ca906fb5c49d8362cba0d78b270c8
```

Other potentially useful URLs:

- https://sources.debian.net/src/cdebconf/0.271/ (for browsing the source)
- https://sources.debian.net/src/cdebconf/0.271/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/cdebconf/0.271/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `coreutils=9.4-3.1`

Binary Packages:

- `coreutils=9.4-3.1`

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
$ apt-get source -qq --print-uris coreutils=9.4-3.1
'http://deb.debian.org/debian/pool/main/c/coreutils/coreutils_9.4-3.1.dsc' coreutils_9.4-3.1.dsc 1868 SHA256:f18173c5b03135ec14e901748317ef5d05273dfbdebd76938988e2404f185aa1
'http://deb.debian.org/debian/pool/main/c/coreutils/coreutils_9.4.orig.tar.xz' coreutils_9.4.orig.tar.xz 5979200 SHA256:ea613a4cf44612326e917201bbbcdfbd301de21ffc3b59b6e5c07e040b275e52
'http://deb.debian.org/debian/pool/main/c/coreutils/coreutils_9.4-3.1.debian.tar.xz' coreutils_9.4-3.1.debian.tar.xz 29604 SHA256:326454b01befcd4116543c624f5515387f57f9655284330d1abb7c593abc001f
```

Other potentially useful URLs:

- https://sources.debian.net/src/coreutils/9.4-3.1/ (for browsing the source)
- https://sources.debian.net/src/coreutils/9.4-3.1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/coreutils/9.4-3.1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `dash=0.5.12-6`

Binary Packages:

- `dash=0.5.12-6`

Licenses: (parsed from: `/usr/share/doc/dash/copyright`)

- `BSD-3-Clause`
- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris dash=0.5.12-6
'http://deb.debian.org/debian/pool/main/d/dash/dash_0.5.12-6.dsc' dash_0.5.12-6.dsc 1520 SHA256:dfca9cb9a537d09c190baa9fb15848ecaa55f301843779f26260b1429cd72746
'http://deb.debian.org/debian/pool/main/d/dash/dash_0.5.12.orig.tar.gz' dash_0.5.12.orig.tar.gz 246054 SHA256:6a474ac46e8b0b32916c4c60df694c82058d3297d8b385b74508030ca4a8f28a
'http://deb.debian.org/debian/pool/main/d/dash/dash_0.5.12-6.debian.tar.xz' dash_0.5.12-6.debian.tar.xz 39116 SHA256:155173292d95943d2c737c0f7f4733bb6b39244522f810ee4a64f7be0f4865ab
```

Other potentially useful URLs:

- https://sources.debian.net/src/dash/0.5.12-6/ (for browsing the source)
- https://sources.debian.net/src/dash/0.5.12-6/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/dash/0.5.12-6/ (for access to the source package after it no longer exists in the archive)

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

Source:

```console
$ apt-get source -qq --print-uris db5.3=5.3.28+dfsg2-7
'http://deb.debian.org/debian/pool/main/d/db5.3/db5.3_5.3.28%2bdfsg2-7.dsc' db5.3_5.3.28+dfsg2-7.dsc 2374 SHA256:f7313fb306b5bf7ad6a428bffb581e649318859df139e35dd47c3d1f733803b2
'http://deb.debian.org/debian/pool/main/d/db5.3/db5.3_5.3.28%2bdfsg2.orig.tar.xz' db5.3_5.3.28+dfsg2.orig.tar.xz 21287688 SHA256:ad41b507415dec8316e828b2230242af2251d2c86eefa3c7aa9ef47c5239ef33
'http://deb.debian.org/debian/pool/main/d/db5.3/db5.3_5.3.28%2bdfsg2-7.debian.tar.xz' db5.3_5.3.28+dfsg2-7.debian.tar.xz 35232 SHA256:9cee8969e1f440ec8aa2fbacd3a5819907829e0e7e7f1f746dccaa2c93fbf3f2
```

Other potentially useful URLs:

- https://sources.debian.net/src/db5.3/5.3.28+dfsg2-7/ (for browsing the source)
- https://sources.debian.net/src/db5.3/5.3.28+dfsg2-7/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/db5.3/5.3.28+dfsg2-7/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `debconf=1.5.86`

Binary Packages:

- `debconf=1.5.86`

Licenses: (parsed from: `/usr/share/doc/debconf/copyright`)

- `BSD-2-clause`

Source:

```console
$ apt-get source -qq --print-uris debconf=1.5.86
'http://deb.debian.org/debian/pool/main/d/debconf/debconf_1.5.86.dsc' debconf_1.5.86.dsc 2035 SHA256:2528e4ed5f0873d5c425953d68bf6164959bd3f7430e53bce2bb99adf0e4a83a
'http://deb.debian.org/debian/pool/main/d/debconf/debconf_1.5.86.tar.xz' debconf_1.5.86.tar.xz 573944 SHA256:7128067f1144046a432784492c58839343768c15b32dc6fafbaa73200d3167d0
```

Other potentially useful URLs:

- https://sources.debian.net/src/debconf/1.5.86/ (for browsing the source)
- https://sources.debian.net/src/debconf/1.5.86/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/debconf/1.5.86/ (for access to the source package after it no longer exists in the archive)

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

### `dpkg` source package: `debianutils=5.17`

Binary Packages:

- `debianutils=5.17`

Licenses: (parsed from: `/usr/share/doc/debianutils/copyright`)

- `GPL-2`
- `GPL-2+`
- `SMAIL-GPL`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris debianutils=5.17
'http://deb.debian.org/debian/pool/main/d/debianutils/debianutils_5.17.dsc' debianutils_5.17.dsc 1631 SHA256:4ba4ecda8885ab0f45ef878d7bc62882c6673f74b1636109878e5c9ff5f0f88e
'http://deb.debian.org/debian/pool/main/d/debianutils/debianutils_5.17.tar.xz' debianutils_5.17.tar.xz 80356 SHA256:367654878388f532cd8a897fe64766e2d57ae4c60da1d4d8f20dcdf2fb0cbde8
```

Other potentially useful URLs:

- https://sources.debian.net/src/debianutils/5.17/ (for browsing the source)
- https://sources.debian.net/src/debianutils/5.17/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/debianutils/5.17/ (for access to the source package after it no longer exists in the archive)

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

### `dpkg` source package: `dpkg=1.22.6`

Binary Packages:

- `dpkg=1.22.6`

Licenses: (parsed from: `/usr/share/doc/dpkg/copyright`)

- `GPL-2`
- `GPL-2+`
- `public-domain-s-s-d`

Source:

```console
$ apt-get source -qq --print-uris dpkg=1.22.6
'http://deb.debian.org/debian/pool/main/d/dpkg/dpkg_1.22.6.dsc' dpkg_1.22.6.dsc 3041 SHA256:9e109e78ee459a132813c7f21a67a7845e26e3e203d5d51ea4ee81dd5abb3443
'http://deb.debian.org/debian/pool/main/d/dpkg/dpkg_1.22.6.tar.xz' dpkg_1.22.6.tar.xz 5630704 SHA256:4379123466cf1804f82aaac7fbea7133c58aefa178dfbf7029cdc61a8d220655
```

Other potentially useful URLs:

- https://sources.debian.net/src/dpkg/1.22.6/ (for browsing the source)
- https://sources.debian.net/src/dpkg/1.22.6/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/dpkg/1.22.6/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `e2fsprogs=1.47.1~rc2-1`

Binary Packages:

- `e2fsprogs=1.47.1~rc2-1`
- `libcom-err2:amd64=1.47.1~rc2-1`
- `libext2fs2t64:amd64=1.47.1~rc2-1`
- `libss2:amd64=1.47.1~rc2-1`
- `logsave=1.47.1~rc2-1`

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
$ apt-get source -qq --print-uris e2fsprogs=1.47.1~rc2-1
'http://deb.debian.org/debian/pool/main/e/e2fsprogs/e2fsprogs_1.47.1%7erc2-1.dsc' e2fsprogs_1.47.1~rc2-1.dsc 2983 SHA256:af93dc7e88a7cc95646b4fba5fb7da497112c9d0d0672a23a53130ffd3b5b1ec
'http://deb.debian.org/debian/pool/main/e/e2fsprogs/e2fsprogs_1.47.1%7erc2.orig.tar.gz' e2fsprogs_1.47.1~rc2.orig.tar.gz 9941383 SHA256:cfc9d0d6d1301357b420a40fd9c963bbc6563a03b3f29165162fd82c7470f97e
'http://deb.debian.org/debian/pool/main/e/e2fsprogs/e2fsprogs_1.47.1%7erc2.orig.tar.gz.asc' e2fsprogs_1.47.1~rc2.orig.tar.gz.asc 488 SHA256:e3429e842a50fb32e994dad37e54f5785b85f9a26cee8a7a26718804ea7f4ea7
'http://deb.debian.org/debian/pool/main/e/e2fsprogs/e2fsprogs_1.47.1%7erc2-1.debian.tar.xz' e2fsprogs_1.47.1~rc2-1.debian.tar.xz 89624 SHA256:50e1d2d28e07c53fefb5a10191c416f59777ee925a53cf3ce3ae6804673ccbeb
```

Other potentially useful URLs:

- https://sources.debian.net/src/e2fsprogs/1.47.1~rc2-1/ (for browsing the source)
- https://sources.debian.net/src/e2fsprogs/1.47.1~rc2-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/e2fsprogs/1.47.1~rc2-1/ (for access to the source package after it no longer exists in the archive)

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/findutils/4.9.0-5/


### `dpkg` source package: `gcc-14=14-20240429-1`

Binary Packages:

- `gcc-14-base:amd64=14-20240429-1`
- `libgcc-s1:amd64=14-20240429-1`
- `libstdc++6:amd64=14-20240429-1`

Licenses: (parsed from: `/usr/share/doc/gcc-14-base/copyright`, `/usr/share/doc/libgcc-s1/copyright`, `/usr/share/doc/libstdc++6/copyright`)

- `Artistic`
- `GFDL-1.2`
- `GPL`
- `GPL-3`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris gcc-14=14-20240429-1
'http://deb.debian.org/debian/pool/main/g/gcc-14/gcc-14_14-20240429-1.dsc' gcc-14_14-20240429-1.dsc 46429 SHA256:c1bc34eb39241e7af725468c3f6aaa5e679eb8673383698b8a10d49a3caf4c16
'http://deb.debian.org/debian/pool/main/g/gcc-14/gcc-14_14-20240429.orig.tar.gz' gcc-14_14-20240429.orig.tar.gz 92800748 SHA256:518c2e7625b65a7d0dfa246e9191b6ac4554b1033c4c2ad35319b322996d62fe
'http://deb.debian.org/debian/pool/main/g/gcc-14/gcc-14_14-20240429-1.debian.tar.xz' gcc-14_14-20240429-1.debian.tar.xz 577460 SHA256:f6e9a832ac04ff7d29ca772c83833a18b3303d6bd9a0cb978736b0b8394c5464
```

Other potentially useful URLs:

- https://sources.debian.net/src/gcc-14/14-20240429-1/ (for browsing the source)
- https://sources.debian.net/src/gcc-14/14-20240429-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/gcc-14/14-20240429-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `glibc=2.38-11`

Binary Packages:

- `libc-bin=2.38-11`
- `libc6:amd64=2.38-11`

Licenses: (parsed from: `/usr/share/doc/libc-bin/copyright`, `/usr/share/doc/libc6/copyright`)

- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris glibc=2.38-11
'http://deb.debian.org/debian/pool/main/g/glibc/glibc_2.38-11.dsc' glibc_2.38-11.dsc 7535 SHA256:e3673f0f0f7371335ed6d9ac1221d33c62604af8171686282a481da8e7a4aa80
'http://deb.debian.org/debian/pool/main/g/glibc/glibc_2.38.orig.tar.xz' glibc_2.38.orig.tar.xz 19761568 SHA256:cf335a1328f652a9c674dfaa02c756f3d9360e9a372f4b9ae5c04fd1a2eca942
'http://deb.debian.org/debian/pool/main/g/glibc/glibc_2.38-11.debian.tar.xz' glibc_2.38-11.debian.tar.xz 429076 SHA256:336d41903e4c2b12a71bb646b68c9c295c980a4a7f22a43da70aadbcfa80a825
```

Other potentially useful URLs:

- https://sources.debian.net/src/glibc/2.38-11/ (for browsing the source)
- https://sources.debian.net/src/glibc/2.38-11/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/glibc/2.38-11/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `gmp=2:6.3.0+dfsg-2`

Binary Packages:

- `libgmp10:amd64=2:6.3.0+dfsg-2+b1`

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
$ apt-get source -qq --print-uris gmp=2:6.3.0+dfsg-2
'http://deb.debian.org/debian/pool/main/g/gmp/gmp_6.3.0%2bdfsg-2.dsc' gmp_6.3.0+dfsg-2.dsc 2251 SHA256:31bf88a2899f7a6eb2dc0db438ba2b27f87562dfe73815a3bbc8b65675ba1a51
'http://deb.debian.org/debian/pool/main/g/gmp/gmp_6.3.0%2bdfsg.orig.tar.xz' gmp_6.3.0+dfsg.orig.tar.xz 1870556 SHA256:bd2966e6d277f79328e894a5a9f3ba3fbf2ed2be81def5f48623e30c23fb1572
'http://deb.debian.org/debian/pool/main/g/gmp/gmp_6.3.0%2bdfsg-2.debian.tar.xz' gmp_6.3.0+dfsg-2.debian.tar.xz 19156 SHA256:07fbc1f67c1c076575f8196f3b5a2d2be0268be10940ca59293d7f1669365f4e
```

Other potentially useful URLs:

- https://sources.debian.net/src/gmp/2:6.3.0+dfsg-2/ (for browsing the source)
- https://sources.debian.net/src/gmp/2:6.3.0+dfsg-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/gmp/2:6.3.0+dfsg-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `gnupg2=2.2.40-3`

Binary Packages:

- `gpgv=2.2.40-3`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/gnupg2/2.2.40-3/


### `dpkg` source package: `gnutls28=3.8.5-2`

Binary Packages:

- `libgnutls30t64:amd64=3.8.5-2`

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
$ apt-get source -qq --print-uris gnutls28=3.8.5-2
'http://deb.debian.org/debian/pool/main/g/gnutls28/gnutls28_3.8.5-2.dsc' gnutls28_3.8.5-2.dsc 3268 SHA256:ff96a5441cb3e65cfff2dcde9995ea2dec71eab45abc0fe3c595679867a2ef93
'http://deb.debian.org/debian/pool/main/g/gnutls28/gnutls28_3.8.5.orig.tar.xz' gnutls28_3.8.5.orig.tar.xz 6491504 SHA256:66269a2cfe0e1c2dabec87bdbbd8ab656f396edd9a40dd006978e003cfa52bfc
'http://deb.debian.org/debian/pool/main/g/gnutls28/gnutls28_3.8.5.orig.tar.xz.asc' gnutls28_3.8.5.orig.tar.xz.asc 228 SHA256:d02c2bc3b994b3fc81f76663a0570c156f9dd299a2151f04fd3429eca6569f52
'http://deb.debian.org/debian/pool/main/g/gnutls28/gnutls28_3.8.5-2.debian.tar.xz' gnutls28_3.8.5-2.debian.tar.xz 79356 SHA256:5a29cdcec8bc2cee41a179041063f0df762f6f43c83757f1e8c290f0606088de
```

Other potentially useful URLs:

- https://sources.debian.net/src/gnutls28/3.8.5-2/ (for browsing the source)
- https://sources.debian.net/src/gnutls28/3.8.5-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/gnutls28/3.8.5-2/ (for access to the source package after it no longer exists in the archive)

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

Source:

```console
$ apt-get source -qq --print-uris gzip=1.12-1.1
'http://deb.debian.org/debian/pool/main/g/gzip/gzip_1.12-1.1.dsc' gzip_1.12-1.1.dsc 2167 SHA256:212bff0edd2ccbbf816d7168f46f81d714b57043c249411e2e2d0fd71c3d3e40
'http://deb.debian.org/debian/pool/main/g/gzip/gzip_1.12.orig.tar.xz' gzip_1.12.orig.tar.xz 825548 SHA256:ce5e03e519f637e1f814011ace35c4f87b33c0bbabeec35baf5fbd3479e91956
'http://deb.debian.org/debian/pool/main/g/gzip/gzip_1.12.orig.tar.xz.asc' gzip_1.12.orig.tar.xz.asc 833 SHA256:3ed9ab54452576e0be0d477c772c9f47baa36415133fef7dd1fcf7b15480ba32
'http://deb.debian.org/debian/pool/main/g/gzip/gzip_1.12-1.1.debian.tar.xz' gzip_1.12-1.1.debian.tar.xz 19244 SHA256:d48d5314c0255114f43964f78b87262299bbac840e5f511a078e2d2590937ad6
```

Other potentially useful URLs:

- https://sources.debian.net/src/gzip/1.12-1.1/ (for browsing the source)
- https://sources.debian.net/src/gzip/1.12-1.1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/gzip/1.12-1.1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `hostname=3.23+nmu2`

Binary Packages:

- `hostname=3.23+nmu2`

Licenses: (parsed from: `/usr/share/doc/hostname/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris hostname=3.23+nmu2
'http://deb.debian.org/debian/pool/main/h/hostname/hostname_3.23%2bnmu2.dsc' hostname_3.23+nmu2.dsc 1431 SHA256:03fe3dcdda4e3abc3a5d8d7ed6eb63558d9fa0dfe68412667eac73945b47e506
'http://deb.debian.org/debian/pool/main/h/hostname/hostname_3.23%2bnmu2.tar.xz' hostname_3.23+nmu2.tar.xz 12944 SHA256:e94bc2323862e1b49635c2b638aa905f14aa91d9eb525be8e8811a773ca3a60d
```

Other potentially useful URLs:

- https://sources.debian.net/src/hostname/3.23+nmu2/ (for browsing the source)
- https://sources.debian.net/src/hostname/3.23+nmu2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/hostname/3.23+nmu2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `init-system-helpers=1.66`

Binary Packages:

- `init-system-helpers=1.66`

Licenses: (parsed from: `/usr/share/doc/init-system-helpers/copyright`)

- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris init-system-helpers=1.66
'http://deb.debian.org/debian/pool/main/i/init-system-helpers/init-system-helpers_1.66.dsc' init-system-helpers_1.66.dsc 2234 SHA256:a1e2276879abfe63174797c94969bc8591b8a05f2bad6ae3f27379b472877d6d
'http://deb.debian.org/debian/pool/main/i/init-system-helpers/init-system-helpers_1.66.tar.xz' init-system-helpers_1.66.tar.xz 44976 SHA256:da058b5623a7d3f39aee1761b173478fdbbdfdf743fd66e876e56039c708ce53
```

Other potentially useful URLs:

- https://sources.debian.net/src/init-system-helpers/1.66/ (for browsing the source)
- https://sources.debian.net/src/init-system-helpers/1.66/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/init-system-helpers/1.66/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libcap-ng=0.8.5-1`

Binary Packages:

- `libcap-ng0:amd64=0.8.5-1`

Licenses: (parsed from: `/usr/share/doc/libcap-ng0/copyright`)

- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris libcap-ng=0.8.5-1
'http://deb.debian.org/debian/pool/main/libc/libcap-ng/libcap-ng_0.8.5-1.dsc' libcap-ng_0.8.5-1.dsc 1638 SHA256:0b4a6e7ff74f5d888295bfab7f65f37255fb150e07bd8cedc0678c198b47bba0
'http://deb.debian.org/debian/pool/main/libc/libcap-ng/libcap-ng_0.8.5.orig.tar.gz' libcap-ng_0.8.5.orig.tar.gz 59265 SHA256:e4be07fdd234f10b866433f224d183626003c65634ed0552b02e654a380244c2
'http://deb.debian.org/debian/pool/main/libc/libcap-ng/libcap-ng_0.8.5-1.debian.tar.xz' libcap-ng_0.8.5-1.debian.tar.xz 7400 SHA256:17156cf9ef58de3e8c34a357c6afa47d54a42d2c185ffbd43fde7c4cf04937f1
```

Other potentially useful URLs:

- https://sources.debian.net/src/libcap-ng/0.8.5-1/ (for browsing the source)
- https://sources.debian.net/src/libcap-ng/0.8.5-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libcap-ng/0.8.5-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libcap2=1:2.66-5`

Binary Packages:

- `libcap2:amd64=1:2.66-5`

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

### `dpkg` source package: `libgcrypt20=1.10.3-2`

Binary Packages:

- `libgcrypt20:amd64=1.10.3-2+b1`

Licenses: (parsed from: `/usr/share/doc/libgcrypt20/copyright`)

- `GPL-2`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris libgcrypt20=1.10.3-2
'http://deb.debian.org/debian/pool/main/libg/libgcrypt20/libgcrypt20_1.10.3-2.dsc' libgcrypt20_1.10.3-2.dsc 2799 SHA256:9313ff9de25bc77383776d8fc0c2c1bd7ed9521a95a07aac74678e78fe3f8a5d
'http://deb.debian.org/debian/pool/main/libg/libgcrypt20/libgcrypt20_1.10.3.orig.tar.bz2' libgcrypt20_1.10.3.orig.tar.bz2 3783827 SHA256:8b0870897ac5ac67ded568dcfadf45969cfa8a6beb0fd60af2a9eadc2a3272aa
'http://deb.debian.org/debian/pool/main/libg/libgcrypt20/libgcrypt20_1.10.3.orig.tar.bz2.asc' libgcrypt20_1.10.3.orig.tar.bz2.asc 390 SHA256:f02a5f961b89c034a78decbb355ea5a8d9356df5a9636dec53ae548d7d814b14
'http://deb.debian.org/debian/pool/main/libg/libgcrypt20/libgcrypt20_1.10.3-2.debian.tar.xz' libgcrypt20_1.10.3-2.debian.tar.xz 36496 SHA256:34121246430b7dbbe3ea7cdb77133653707cb2480eaf794c76000aee9a8abc55
```

Other potentially useful URLs:

- https://sources.debian.net/src/libgcrypt20/1.10.3-2/ (for browsing the source)
- https://sources.debian.net/src/libgcrypt20/1.10.3-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libgcrypt20/1.10.3-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libgpg-error=1.49-2`

Binary Packages:

- `libgpg-error0:amd64=1.49-2`

Licenses: (parsed from: `/usr/share/doc/libgpg-error0/copyright`)

- `BSD-3-clause`
- `GPL-3`
- `GPL-3+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `g10-permissive`

Source:

```console
$ apt-get source -qq --print-uris libgpg-error=1.49-2
'http://deb.debian.org/debian/pool/main/libg/libgpg-error/libgpg-error_1.49-2.dsc' libgpg-error_1.49-2.dsc 2896 SHA256:8638b6639998a745cb377f8011609d5ed0b211f72cd01e63573a058d71e29cea
'http://deb.debian.org/debian/pool/main/libg/libgpg-error/libgpg-error_1.49.orig.tar.bz2' libgpg-error_1.49.orig.tar.bz2 1081175 SHA256:8b79d54639dbf4abc08b5406fb2f37e669a2dec091dd024fb87dd367131c63a9
'http://deb.debian.org/debian/pool/main/libg/libgpg-error/libgpg-error_1.49.orig.tar.bz2.asc' libgpg-error_1.49.orig.tar.bz2.asc 228 SHA256:2b781c0b6cd865c28ec1006cf9fb4390303b2d52ffc7ed09bcb58a01348ef870
'http://deb.debian.org/debian/pool/main/libg/libgpg-error/libgpg-error_1.49-2.debian.tar.xz' libgpg-error_1.49-2.debian.tar.xz 18804 SHA256:c60d7a21430651e8f36474bdb585096dd4fd52dc403fb99dfa2a874068211282
```

Other potentially useful URLs:

- https://sources.debian.net/src/libgpg-error/1.49-2/ (for browsing the source)
- https://sources.debian.net/src/libgpg-error/1.49-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libgpg-error/1.49-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libidn2=2.3.7-2`

Binary Packages:

- `libidn2-0:amd64=2.3.7-2`

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
'http://deb.debian.org/debian/pool/main/libm/libmd/libmd_1.1.0-2.dsc' libmd_1.1.0-2.dsc 2280 SHA256:46cc951cd6d71bbfeff4522de66f968fb92601ec4cc622b07f6ac0a2a36ac5f0
'http://deb.debian.org/debian/pool/main/libm/libmd/libmd_1.1.0.orig.tar.xz' libmd_1.1.0.orig.tar.xz 271228 SHA256:1bd6aa42275313af3141c7cf2e5b964e8b1fd488025caf2f971f43b00776b332
'http://deb.debian.org/debian/pool/main/libm/libmd/libmd_1.1.0.orig.tar.xz.asc' libmd_1.1.0.orig.tar.xz.asc 833 SHA256:402fd3024e43ab975733d09e661804a58ca58697194e4b15216b1217cfe1dadb
'http://deb.debian.org/debian/pool/main/libm/libmd/libmd_1.1.0-2.debian.tar.xz' libmd_1.1.0-2.debian.tar.xz 8244 SHA256:3b6ff35fc921eb5450fa9bf2d300c9e058e3771f96f8f13f759768fadd53324c
```

Other potentially useful URLs:

- https://sources.debian.net/src/libmd/1.1.0-2/ (for browsing the source)
- https://sources.debian.net/src/libmd/1.1.0-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libmd/1.1.0-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libseccomp=2.5.5-1`

Binary Packages:

- `libseccomp2:amd64=2.5.5-1`

Licenses: (parsed from: `/usr/share/doc/libseccomp2/copyright`)

- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libseccomp=2.5.5-1
'http://deb.debian.org/debian/pool/main/libs/libseccomp/libseccomp_2.5.5-1.dsc' libseccomp_2.5.5-1.dsc 2708 SHA256:d8ea2fb22a4ed90001a34ace6e6a6f41fd1d9404de923182f2dde6037fec22e5
'http://deb.debian.org/debian/pool/main/libs/libseccomp/libseccomp_2.5.5.orig.tar.gz' libseccomp_2.5.5.orig.tar.gz 642445 SHA256:248a2c8a4d9b9858aa6baf52712c34afefcf9c9e94b76dce02c1c9aa25fb3375
'http://deb.debian.org/debian/pool/main/libs/libseccomp/libseccomp_2.5.5.orig.tar.gz.asc' libseccomp_2.5.5.orig.tar.gz.asc 833 SHA256:f3bf8a946020d3047581f11fe6ac71971a842115ddb362562b193861ef57d97b
'http://deb.debian.org/debian/pool/main/libs/libseccomp/libseccomp_2.5.5-1.debian.tar.xz' libseccomp_2.5.5-1.debian.tar.xz 17608 SHA256:0e14e878a97657d8ff660f32477461abbd3ce366e5c24df4e4385c3e64cacaac
```

Other potentially useful URLs:

- https://sources.debian.net/src/libseccomp/2.5.5-1/ (for browsing the source)
- https://sources.debian.net/src/libseccomp/2.5.5-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libseccomp/2.5.5-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libselinux=3.5-2`

Binary Packages:

- `libselinux1:amd64=3.5-2+b2`

Licenses: (parsed from: `/usr/share/doc/libselinux1/copyright`)

- `GPL-2`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris libselinux=3.5-2
'http://deb.debian.org/debian/pool/main/libs/libselinux/libselinux_3.5-2.dsc' libselinux_3.5-2.dsc 2662 SHA256:cd6baa8aebf37a88355291bf5cb11a311463479fed8a9f479043d1fc12de25cc
'http://deb.debian.org/debian/pool/main/libs/libselinux/libselinux_3.5.orig.tar.gz' libselinux_3.5.orig.tar.gz 211453 SHA256:9a3a3705ac13a2ccca2de6d652b6356fead10f36fb33115c185c5ccdf29eec19
'http://deb.debian.org/debian/pool/main/libs/libselinux/libselinux_3.5.orig.tar.gz.asc' libselinux_3.5.orig.tar.gz.asc 981 SHA256:fd37d441e0c08cabe9ac8f7815f52355bab2011549ec5792424fe18be9e1e015
'http://deb.debian.org/debian/pool/main/libs/libselinux/libselinux_3.5-2.debian.tar.xz' libselinux_3.5-2.debian.tar.xz 35992 SHA256:e385f14d9700187495a82e433b02b139aebe89c8ceccab5a21598dfef518b0de
```

Other potentially useful URLs:

- https://sources.debian.net/src/libselinux/3.5-2/ (for browsing the source)
- https://sources.debian.net/src/libselinux/3.5-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libselinux/3.5-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libsemanage=3.5-1`

Binary Packages:

- `libsemanage-common=3.5-1`
- `libsemanage2:amd64=3.5-1+b3`

Licenses: (parsed from: `/usr/share/doc/libsemanage-common/copyright`, `/usr/share/doc/libsemanage2/copyright`)

- `GPL-2`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris libsemanage=3.5-1
'http://deb.debian.org/debian/pool/main/libs/libsemanage/libsemanage_3.5-1.dsc' libsemanage_3.5-1.dsc 2644 SHA256:7415394f12030387ebca4ab7845830984b1ceb7ec3256d30a1733ba7f59d18c1
'http://deb.debian.org/debian/pool/main/libs/libsemanage/libsemanage_3.5.orig.tar.gz' libsemanage_3.5.orig.tar.gz 185060 SHA256:f53534e50247538280ed0d76c6ce81d8fb3939bd64cadb89da10dba42e40dd9c
'http://deb.debian.org/debian/pool/main/libs/libsemanage/libsemanage_3.5.orig.tar.gz.asc' libsemanage_3.5.orig.tar.gz.asc 981 SHA256:f9126c861c666f3308b60cea4405c5e686a056113ca3cbd0a5b0e4af7600c8f5
'http://deb.debian.org/debian/pool/main/libs/libsemanage/libsemanage_3.5-1.debian.tar.xz' libsemanage_3.5-1.debian.tar.xz 29956 SHA256:78b11321d014bd52e1fb67c38db5ec6518b0b566b58c6e35a18e894dacc24aee
```

Other potentially useful URLs:

- https://sources.debian.net/src/libsemanage/3.5-1/ (for browsing the source)
- https://sources.debian.net/src/libsemanage/3.5-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libsemanage/3.5-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libsepol=3.5-2`

Binary Packages:

- `libsepol2:amd64=3.5-2+b1`

Licenses: (parsed from: `/usr/share/doc/libsepol2/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris libsepol=3.5-2
'http://deb.debian.org/debian/pool/main/libs/libsepol/libsepol_3.5-2.dsc' libsepol_3.5-2.dsc 2005 SHA256:0f7b4750fbb8f34841c31784e8fbc1a94949a83adbcb7103f0ae061198bc55e7
'http://deb.debian.org/debian/pool/main/libs/libsepol/libsepol_3.5.orig.tar.gz' libsepol_3.5.orig.tar.gz 497522 SHA256:78fdaf69924db780bac78546e43d9c44074bad798c2c415d0b9bb96d065ee8a2
'http://deb.debian.org/debian/pool/main/libs/libsepol/libsepol_3.5.orig.tar.gz.asc' libsepol_3.5.orig.tar.gz.asc 981 SHA256:2309ab5e7cd38e2eb9196f92a60e00d4508cb293f1181d34a5a050128c9b7b24
'http://deb.debian.org/debian/pool/main/libs/libsepol/libsepol_3.5-2.debian.tar.xz' libsepol_3.5-2.debian.tar.xz 27596 SHA256:05de2029893ec20cde7687178003fc5161d606259dad218ad46e7332db922695
```

Other potentially useful URLs:

- https://sources.debian.net/src/libsepol/3.5-2/ (for browsing the source)
- https://sources.debian.net/src/libsepol/3.5-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libsepol/3.5-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libtasn1-6=4.19.0-3`

Binary Packages:

- `libtasn1-6:amd64=4.19.0-3+b2`

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

- `libunistring5:amd64=1.2-1`

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
$ apt-get source -qq --print-uris libunistring=1.2-1
'http://deb.debian.org/debian/pool/main/libu/libunistring/libunistring_1.2-1.dsc' libunistring_1.2-1.dsc 2181 SHA256:5d951adce58920ab7e598f04b903f402382557ad102576d01184553437467dd6
'http://deb.debian.org/debian/pool/main/libu/libunistring/libunistring_1.2.orig.tar.xz' libunistring_1.2.orig.tar.xz 2502196 SHA256:632bd65ed74a881ca8a0309a1001c428bd1cbd5cd7ddbf8cedcd2e65f4dcdc44
'http://deb.debian.org/debian/pool/main/libu/libunistring/libunistring_1.2.orig.tar.xz.asc' libunistring_1.2.orig.tar.xz.asc 833 SHA256:91da3f033231a635dae9e0161c834b74e890e1eba19d4e5972b26c5c312ac2cb
'http://deb.debian.org/debian/pool/main/libu/libunistring/libunistring_1.2-1.debian.tar.xz' libunistring_1.2-1.debian.tar.xz 13656 SHA256:0605dbb77c072393abaa9e6ec8507d57d91f62aee4d7a7f968f295e4e9ab3bcf
```

Other potentially useful URLs:

- https://sources.debian.net/src/libunistring/1.2-1/ (for browsing the source)
- https://sources.debian.net/src/libunistring/1.2-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libunistring/1.2-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libxcrypt=1:4.4.36-4`

Binary Packages:

- `libcrypt1:amd64=1:4.4.36-4`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxcrypt=1:4.4.36-4
'http://deb.debian.org/debian/pool/main/libx/libxcrypt/libxcrypt_4.4.36-4.dsc' libxcrypt_4.4.36-4.dsc 1563 SHA256:8509256bf6ddedebfaf14ad777541d225a6c956f590602f85f5639efc652bfef
'http://deb.debian.org/debian/pool/main/libx/libxcrypt/libxcrypt_4.4.36.orig.tar.xz' libxcrypt_4.4.36.orig.tar.xz 392732 SHA256:7b7abbc89f13f5194211aa6861ed954e4fa3a210a4cb64f7e13dc8cf413e7f2a
'http://deb.debian.org/debian/pool/main/libx/libxcrypt/libxcrypt_4.4.36-4.debian.tar.xz' libxcrypt_4.4.36-4.debian.tar.xz 8216 SHA256:e61d8a486e6a80a2e3d629296988f8ff2e4dfbef018ec7e94543b5918ca1f329
```

Other potentially useful URLs:

- https://sources.debian.net/src/libxcrypt/1:4.4.36-4/ (for browsing the source)
- https://sources.debian.net/src/libxcrypt/1:4.4.36-4/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libxcrypt/1:4.4.36-4/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/libz/libzstd/libzstd_1.5.5%2bdfsg2-2.dsc' libzstd_1.5.5+dfsg2-2.dsc 2375 SHA256:4e27ea0c5e2564dd6cc93d95fddc56ef85c5388ea4a4a60d8cca0b4c18c1da4f
'http://deb.debian.org/debian/pool/main/libz/libzstd/libzstd_1.5.5%2bdfsg2.orig.tar.xz' libzstd_1.5.5+dfsg2.orig.tar.xz 1784164 SHA256:d7cf3c10d416fd999cb8fcf7685d9268ba7bec8eb78121fc2d0d916fa393d22b
'http://deb.debian.org/debian/pool/main/libz/libzstd/libzstd_1.5.5%2bdfsg2-2.debian.tar.xz' libzstd_1.5.5+dfsg2-2.debian.tar.xz 21068 SHA256:0a72f44f83cbd2dce66722f5c7844aaf8e5937066a795ca6b3d2b0eba69b9e73
```

Other potentially useful URLs:

- https://sources.debian.net/src/libzstd/1.5.5+dfsg2-2/ (for browsing the source)
- https://sources.debian.net/src/libzstd/1.5.5+dfsg2-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libzstd/1.5.5+dfsg2-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `lz4=1.9.4-2`

Binary Packages:

- `liblz4-1:amd64=1.9.4-2`

Licenses: (parsed from: `/usr/share/doc/liblz4-1/copyright`)

- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris lz4=1.9.4-2
'http://deb.debian.org/debian/pool/main/l/lz4/lz4_1.9.4-2.dsc' lz4_1.9.4-2.dsc 1891 SHA256:981c5eae455d61eb50ae995577adb9190ce8a8ef798f1fd1148ffafab8771dde
'http://deb.debian.org/debian/pool/main/l/lz4/lz4_1.9.4.orig.tar.gz' lz4_1.9.4.orig.tar.gz 354063 SHA256:0b0e3aa07c8c063ddf40b082bdf7e37a1562bda40a0ff5272957f3e987e0e54b
'http://deb.debian.org/debian/pool/main/l/lz4/lz4_1.9.4-2.debian.tar.xz' lz4_1.9.4-2.debian.tar.xz 8164 SHA256:a6fd6b4c5af5ccc84cf3ffc68256c9dcd586aaa3d319e71a4aa0acaa521c9f57
```

Other potentially useful URLs:

- https://sources.debian.net/src/lz4/1.9.4-2/ (for browsing the source)
- https://sources.debian.net/src/lz4/1.9.4-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/lz4/1.9.4-2/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/m/mawk/mawk_1.3.4.20240123-1.dsc' mawk_1.3.4.20240123-1.dsc 2180 SHA256:fe68f6fc0a7f78718ec1b2c8140ddbf6f6d482ea537eaba805b7a9b3c7dd2f4e
'http://deb.debian.org/debian/pool/main/m/mawk/mawk_1.3.4.20240123.orig.tar.gz' mawk_1.3.4.20240123.orig.tar.gz 413943 SHA256:a8e319a83744b1f1fb6988dfa189d61887f866e9140cc9a49eb003b2b0655e88
'http://deb.debian.org/debian/pool/main/m/mawk/mawk_1.3.4.20240123.orig.tar.gz.asc' mawk_1.3.4.20240123.orig.tar.gz.asc 729 SHA256:3b688572de36ecbb8a013cda92e294038324ed2745485e883508e9a6fdbd2472
'http://deb.debian.org/debian/pool/main/m/mawk/mawk_1.3.4.20240123-1.debian.tar.xz' mawk_1.3.4.20240123-1.debian.tar.xz 15600 SHA256:fe64a2ee58597035b727f33dc80f459353670b32887877f73932ab7b7c028eb7
```

Other potentially useful URLs:

- https://sources.debian.net/src/mawk/1.3.4.20240123-1/ (for browsing the source)
- https://sources.debian.net/src/mawk/1.3.4.20240123-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/mawk/1.3.4.20240123-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `ncurses=6.5-2`

Binary Packages:

- `libtinfo6:amd64=6.5-2`
- `ncurses-base=6.5-2`
- `ncurses-bin=6.5-2`

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

### `dpkg` source package: `nettle=3.9.1-2.2`

Binary Packages:

- `libhogweed6t64:amd64=3.9.1-2.2`
- `libnettle8t64:amd64=3.9.1-2.2`

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
$ apt-get source -qq --print-uris nettle=3.9.1-2.2
'http://deb.debian.org/debian/pool/main/n/nettle/nettle_3.9.1-2.2.dsc' nettle_3.9.1-2.2.dsc 2319 SHA256:170deeaaa8d5c3ab2a954daf7e83855c788c4ff2fdb2d8e5ca065be64b0a0001
'http://deb.debian.org/debian/pool/main/n/nettle/nettle_3.9.1.orig.tar.gz' nettle_3.9.1.orig.tar.gz 2396741 SHA256:ccfeff981b0ca71bbd6fbcb054f407c60ffb644389a5be80d6716d5b550c6ce3
'http://deb.debian.org/debian/pool/main/n/nettle/nettle_3.9.1.orig.tar.gz.asc' nettle_3.9.1.orig.tar.gz.asc 573 SHA256:9746017a1a7fe60aad4b929ea592bc6ac51e12ea7179f289944eb44828d958af
'http://deb.debian.org/debian/pool/main/n/nettle/nettle_3.9.1-2.2.debian.tar.xz' nettle_3.9.1-2.2.debian.tar.xz 24732 SHA256:65c36cbca1bb22f05c900f64d39f8bf39d85639243b0e3b4887ef613deedaf72
```

Other potentially useful URLs:

- https://sources.debian.net/src/nettle/3.9.1-2.2/ (for browsing the source)
- https://sources.debian.net/src/nettle/3.9.1-2.2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/nettle/3.9.1-2.2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `openssl=3.2.1-3`

Binary Packages:

- `libssl3t64:amd64=3.2.1-3`

Licenses: (parsed from: `/usr/share/doc/libssl3t64/copyright`)

- `Apache-2.0`
- `Artistic`
- `GPL-1`
- `GPL-1+`

Source:

```console
$ apt-get source -qq --print-uris openssl=3.2.1-3
'http://deb.debian.org/debian/pool/main/o/openssl/openssl_3.2.1-3.dsc' openssl_3.2.1-3.dsc 2482 SHA256:2d967e948f768ed05eb4f94755487bf2492a340d5f8038be91950f2a92cbb2d8
'http://deb.debian.org/debian/pool/main/o/openssl/openssl_3.2.1.orig.tar.gz' openssl_3.2.1.orig.tar.gz 17733249 SHA256:83c7329fe52c850677d75e5d0b0ca245309b97e8ecbcfdc1dfdc4ab9fac35b39
'http://deb.debian.org/debian/pool/main/o/openssl/openssl_3.2.1.orig.tar.gz.asc' openssl_3.2.1.orig.tar.gz.asc 833 SHA256:a394b4f5242feb8b828b398cbea809e07bb73e699ae0b84413efb8c5916361c1
'http://deb.debian.org/debian/pool/main/o/openssl/openssl_3.2.1-3.debian.tar.xz' openssl_3.2.1-3.debian.tar.xz 83124 SHA256:dc0ce3a5cee92d9fc13c912fd0be18b30592da553f16b07966cd01d5f887c882
```

Other potentially useful URLs:

- https://sources.debian.net/src/openssl/3.2.1-3/ (for browsing the source)
- https://sources.debian.net/src/openssl/3.2.1-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/openssl/3.2.1-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `p11-kit=0.25.3-5`

Binary Packages:

- `libp11-kit0:amd64=0.25.3-5`

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
$ apt-get source -qq --print-uris p11-kit=0.25.3-5
'http://deb.debian.org/debian/pool/main/p/p11-kit/p11-kit_0.25.3-5.dsc' p11-kit_0.25.3-5.dsc 2535 SHA256:9f8496bc8a19fd077af7080db3d1d9324dbcc1bc9b62beea81940976bfd1dff7
'http://deb.debian.org/debian/pool/main/p/p11-kit/p11-kit_0.25.3.orig.tar.xz' p11-kit_0.25.3.orig.tar.xz 991528 SHA256:d8ddce1bb7e898986f9d250ccae7c09ce14d82f1009046d202a0eb1b428b2adc
'http://deb.debian.org/debian/pool/main/p/p11-kit/p11-kit_0.25.3.orig.tar.xz.asc' p11-kit_0.25.3.orig.tar.xz.asc 228 SHA256:91fb1fd7690b953eb32bf9ca52ae1b2466457539ac849468f1d236673b354860
'http://deb.debian.org/debian/pool/main/p/p11-kit/p11-kit_0.25.3-5.debian.tar.xz' p11-kit_0.25.3-5.debian.tar.xz 27024 SHA256:d312f5794b2e303b04801815490be624a1c280787dddd3708d2f2e0cfcf4caeb
```

Other potentially useful URLs:

- https://sources.debian.net/src/p11-kit/0.25.3-5/ (for browsing the source)
- https://sources.debian.net/src/p11-kit/0.25.3-5/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/p11-kit/0.25.3-5/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `pam=1.5.3-7`

Binary Packages:

- `libpam-modules:amd64=1.5.3-7`
- `libpam-modules-bin=1.5.3-7`
- `libpam-runtime=1.5.3-7`
- `libpam0g:amd64=1.5.3-7`

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

### `dpkg` source package: `pcre2=10.42-4`

Binary Packages:

- `libpcre2-8-0:amd64=10.42-4+b1`

Licenses: (parsed from: `/usr/share/doc/libpcre2-8-0/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `BSD-3-clause-Cambridge with BINARY LIBRARY-LIKE PACKAGES exception`
- `X11`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris pcre2=10.42-4
'http://deb.debian.org/debian/pool/main/p/pcre2/pcre2_10.42-4.dsc' pcre2_10.42-4.dsc 2302 SHA256:2796d9332a4b4abe5eeada4aa287e8f9765a497b4363e3c49815a6bca5845cfe
'http://deb.debian.org/debian/pool/main/p/pcre2/pcre2_10.42.orig.tar.gz' pcre2_10.42.orig.tar.gz 2397194 SHA256:c33b418e3b936ee3153de2c61cc638e7e4fe3156022a5c77d0711bcbb9d64f1f
'http://deb.debian.org/debian/pool/main/p/pcre2/pcre2_10.42-4.diff.gz' pcre2_10.42-4.diff.gz 8111 SHA256:b583a75e90b029616c6867eccfeb21031e62df98dd4462f9d13ccb95bb2f09e6
```

Other potentially useful URLs:

- https://sources.debian.net/src/pcre2/10.42-4/ (for browsing the source)
- https://sources.debian.net/src/pcre2/10.42-4/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/pcre2/10.42-4/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `perl=5.38.2-4`

Binary Packages:

- `perl-base=5.38.2-4`

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

- http://snapshot.debian.org/package/perl/5.38.2-4/


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

### `dpkg` source package: `shadow=1:4.13+dfsg1-4`

Binary Packages:

- `login=1:4.13+dfsg1-4`
- `passwd=1:4.13+dfsg1-4`

Licenses: (parsed from: `/usr/share/doc/login/copyright`, `/usr/share/doc/passwd/copyright`)

- `BSD-3-clause`
- `GPL-1`
- `GPL-2`
- `GPL-2+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris shadow=1:4.13+dfsg1-4
'http://deb.debian.org/debian/pool/main/s/shadow/shadow_4.13%2bdfsg1-4.dsc' shadow_4.13+dfsg1-4.dsc 2428 SHA256:c805045a571b1a93e88fb65239c112dc39657bb08461efd7a575fbdea6dbe445
'http://deb.debian.org/debian/pool/main/s/shadow/shadow_4.13%2bdfsg1.orig.tar.xz' shadow_4.13+dfsg1.orig.tar.xz 1811752 SHA256:a8bb3a2aceff1cbe39d0f50687dcc1d7e7be0516a9d954d8e2eedb93f5906207
'http://deb.debian.org/debian/pool/main/s/shadow/shadow_4.13%2bdfsg1-4.debian.tar.xz' shadow_4.13+dfsg1-4.debian.tar.xz 82380 SHA256:baca35100bd6c1e54fa8b6653361eede47a0bc586bd91c88dcc9c7d08d47e8b7
```

Other potentially useful URLs:

- https://sources.debian.net/src/shadow/1:4.13+dfsg1-4/ (for browsing the source)
- https://sources.debian.net/src/shadow/1:4.13+dfsg1-4/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/shadow/1:4.13+dfsg1-4/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `systemd=255.5-1`

Binary Packages:

- `libsystemd0:amd64=255.5-1`
- `libudev1:amd64=255.5-1`

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

- http://snapshot.debian.org/package/systemd/255.5-1/


### `dpkg` source package: `sysvinit=3.09-1`

Binary Packages:

- `sysvinit-utils=3.09-1`

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
$ apt-get source -qq --print-uris sysvinit=3.09-1
'http://deb.debian.org/debian/pool/main/s/sysvinit/sysvinit_3.09-1.dsc' sysvinit_3.09-1.dsc 2347 SHA256:52ab503fb095bf8114fb17c4c8a28e4536ea37c69119672d5e94db0013b8c73f
'http://deb.debian.org/debian/pool/main/s/sysvinit/sysvinit_3.09.orig.tar.gz' sysvinit_3.09.orig.tar.gz 514145 SHA256:991c5d0100165d7896dae9df6a69877311cdd5349e32f7fc6960859f5f60a6ce
'http://deb.debian.org/debian/pool/main/s/sysvinit/sysvinit_3.09-1.debian.tar.xz' sysvinit_3.09-1.debian.tar.xz 120876 SHA256:f28ebfabc223fb522a5f1bb4720a6040e78e6eacca57d2e068084b55d6c44662
```

Other potentially useful URLs:

- https://sources.debian.net/src/sysvinit/3.09-1/ (for browsing the source)
- https://sources.debian.net/src/sysvinit/3.09-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/sysvinit/3.09-1/ (for access to the source package after it no longer exists in the archive)

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

### `dpkg` source package: `tzdata=2024a-4`

Binary Packages:

- `tzdata=2024a-4`

Licenses: (parsed from: `/usr/share/doc/tzdata/copyright`)

- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris tzdata=2024a-4
'http://deb.debian.org/debian/pool/main/t/tzdata/tzdata_2024a-4.dsc' tzdata_2024a-4.dsc 2429 SHA256:053c342511ece9a0eec2c9d60a6670dd9bce379dcb0bfad88d2167a2786ecb3f
'http://deb.debian.org/debian/pool/main/t/tzdata/tzdata_2024a.orig.tar.gz' tzdata_2024a.orig.tar.gz 451270 SHA256:0d0434459acbd2059a7a8da1f3304a84a86591f6ed69c6248fffa502b6edffe3
'http://deb.debian.org/debian/pool/main/t/tzdata/tzdata_2024a.orig.tar.gz.asc' tzdata_2024a.orig.tar.gz.asc 833 SHA256:f64725f9f65419e7b009e3b95b75ea9516382d0be64aef63d78654d9c569ed0d
'http://deb.debian.org/debian/pool/main/t/tzdata/tzdata_2024a-4.debian.tar.xz' tzdata_2024a-4.debian.tar.xz 124152 SHA256:ff5dbfa986ebcb1705ca0256163738c56538baf3a6778f53d616407d8da9ccac
```

Other potentially useful URLs:

- https://sources.debian.net/src/tzdata/2024a-4/ (for browsing the source)
- https://sources.debian.net/src/tzdata/2024a-4/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/tzdata/2024a-4/ (for access to the source package after it no longer exists in the archive)

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

### `dpkg` source package: `util-linux=2.40-8`

Binary Packages:

- `bsdutils=1:2.40-8`
- `libblkid1:amd64=2.40-8`
- `libmount1:amd64=2.40-8`
- `libsmartcols1:amd64=2.40-8`
- `libuuid1:amd64=2.40-8`
- `mount=2.40-8`
- `util-linux=2.40-8`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/util-linux/2.40-8/


### `dpkg` source package: `xxhash=0.8.2-2`

Binary Packages:

- `libxxhash0:amd64=0.8.2-2+b1`

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

### `dpkg` source package: `xz-utils=5.6.1+really5.4.5-1`

Binary Packages:

- `liblzma5:amd64=5.6.1+really5.4.5-1`

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
$ apt-get source -qq --print-uris xz-utils=5.6.1+really5.4.5-1
'http://deb.debian.org/debian/pool/main/x/xz-utils/xz-utils_5.6.1%2breally5.4.5-1.dsc' xz-utils_5.6.1+really5.4.5-1.dsc 2679 SHA256:7d7ab95b2004b949a083b66190ad8dc8272fae32e04888027a2a40976844207c
'http://deb.debian.org/debian/pool/main/x/xz-utils/xz-utils_5.6.1%2breally5.4.5.orig.tar.xz' xz-utils_5.6.1+really5.4.5.orig.tar.xz 1680520 SHA256:da9dec6c12cf2ecf269c31ab65b5de18e8e52b96f35d5bcd08c12b43e6878803
'http://deb.debian.org/debian/pool/main/x/xz-utils/xz-utils_5.6.1%2breally5.4.5-1.debian.tar.xz' xz-utils_5.6.1+really5.4.5-1.debian.tar.xz 27232 SHA256:0c54c44098e31a529c942faff69f8367cfdd5e80212139fca9b7ee40e7f86a45
```

Other potentially useful URLs:

- https://sources.debian.net/src/xz-utils/5.6.1+really5.4.5-1/ (for browsing the source)
- https://sources.debian.net/src/xz-utils/5.6.1+really5.4.5-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/xz-utils/5.6.1+really5.4.5-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `zlib=1:1.3.dfsg+really1.3.1-1`

Binary Packages:

- `zlib1g:amd64=1:1.3.dfsg+really1.3.1-1`

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
