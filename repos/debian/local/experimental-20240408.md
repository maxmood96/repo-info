# `debian:experimental`

## Docker Metadata

- Image ID: `sha256:606a3149af36460e1c22e7c6b337e1146321152c185f19c3d7f9127693efc45c`
- Created: `2024-04-10T01:54:13.177045217Z`
- Virtual Size: ~ 122.91 Mb  
  (total size of all layers on-disk)
- Arch: `linux`/`amd64`
- Command: `["bash"]`
- Environment:
  - `PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin`

## `dpkg` (`.deb`-based packages)

### `dpkg` source package: `acl=2.3.2-1`

Binary Packages:

- `libacl1:amd64=2.3.2-1`

Licenses: (parsed from: `/usr/share/doc/libacl1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2+`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris acl=2.3.2-1
'http://deb.debian.org/debian/pool/main/a/acl/acl_2.3.2-1.dsc' acl_2.3.2-1.dsc 2505 SHA256:cb36f16ade6d9cbe7155c74fefd8e56fb3308ee46bf7e8a909feacf48b90164d
'http://deb.debian.org/debian/pool/main/a/acl/acl_2.3.2.orig.tar.xz' acl_2.3.2.orig.tar.xz 371680 SHA256:97203a72cae99ab89a067fe2210c1cbf052bc492b479eca7d226d9830883b0bd
'http://deb.debian.org/debian/pool/main/a/acl/acl_2.3.2.orig.tar.xz.asc' acl_2.3.2.orig.tar.xz.asc 833 SHA256:184c6a903490885a096095db67b433a04542c6569f167cbe8115268c0f227273
'http://deb.debian.org/debian/pool/main/a/acl/acl_2.3.2-1.debian.tar.xz' acl_2.3.2-1.debian.tar.xz 23276 SHA256:abf5d4f58886e3f27dfbd21c740406c425ed8a2bbdaa8def4509fe9b35adbc2a
```

Other potentially useful URLs:

- https://sources.debian.net/src/acl/2.3.2-1/ (for browsing the source)
- https://sources.debian.net/src/acl/2.3.2-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/acl/2.3.2-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `apt=2.7.14`

Binary Packages:

- `apt=2.7.14`
- `libapt-pkg6.0t64:amd64=2.7.14`

Licenses: (parsed from: `/usr/share/doc/apt/copyright`, `/usr/share/doc/libapt-pkg6.0t64/copyright`)

- `BSD-3-clause`
- `Expat`
- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/apt/2.7.14/


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

### `dpkg` source package: `base-files=13`

Binary Packages:

- `base-files=13`

Licenses: (parsed from: `/usr/share/doc/base-files/copyright`)

- `GPL`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/base-files/13/


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

- `bash=5.2.21-2`

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

### `dpkg` source package: `e2fsprogs=1.47.0-2.4`

Binary Packages:

- `e2fsprogs=1.47.0-2.4`
- `libcom-err2:amd64=1.47.0-2.4`
- `libext2fs2t64:amd64=1.47.0-2.4`
- `libss2:amd64=1.47.0-2.4`
- `logsave=1.47.0-2.4`

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
$ apt-get source -qq --print-uris e2fsprogs=1.47.0-2.4
'http://deb.debian.org/debian/pool/main/e/e2fsprogs/e2fsprogs_1.47.0-2.4.dsc' e2fsprogs_1.47.0-2.4.dsc 3159 SHA256:955af7a0d797182731dee25b2687039d4475d079f1e5b16f2783823cf5d5cdf1
'http://deb.debian.org/debian/pool/main/e/e2fsprogs/e2fsprogs_1.47.0.orig.tar.gz' e2fsprogs_1.47.0.orig.tar.gz 9637717 SHA256:6667afde56eef0c6af26684974400e4d2288ea49e9441bf5e6229195d51a3578
'http://deb.debian.org/debian/pool/main/e/e2fsprogs/e2fsprogs_1.47.0.orig.tar.gz.asc' e2fsprogs_1.47.0.orig.tar.gz.asc 488 SHA256:704928204a52ddaa0ac8ef549c1bfba3c38e66c361d3853c8a4c38e6082b90f1
'http://deb.debian.org/debian/pool/main/e/e2fsprogs/e2fsprogs_1.47.0-2.4.debian.tar.xz' e2fsprogs_1.47.0-2.4.debian.tar.xz 88124 SHA256:7f0bfd12b86f7bdbeed311e4219765769a991b282d9a01ad37d4ba3c6b080d70
```

Other potentially useful URLs:

- https://sources.debian.net/src/e2fsprogs/1.47.0-2.4/ (for browsing the source)
- https://sources.debian.net/src/e2fsprogs/1.47.0-2.4/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/e2fsprogs/1.47.0-2.4/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/f/findutils/findutils_4.9.0-5.dsc' findutils_4.9.0-5.dsc 2272 SHA256:7d723c60c50b8b624250ad7d6fbb1ca404756a7b69209753e57c8403e06a07a5
'http://deb.debian.org/debian/pool/main/f/findutils/findutils_4.9.0.orig.tar.xz' findutils_4.9.0.orig.tar.xz 2046252 SHA256:a2bfb8c09d436770edc59f50fa483e785b161a3b7b9d547573cb08065fd462fe
'http://deb.debian.org/debian/pool/main/f/findutils/findutils_4.9.0.orig.tar.xz.asc' findutils_4.9.0.orig.tar.xz.asc 488 SHA256:924c3719d066eda1b3e47175f8b83e90e9a23f0a639ebe7445621917b283c385
'http://deb.debian.org/debian/pool/main/f/findutils/findutils_4.9.0-5.debian.tar.xz' findutils_4.9.0-5.debian.tar.xz 32744 SHA256:456831869d49d8906a98beb2bcbb61e5911d9c44082c4b716615bc23f26c4f20
```

Other potentially useful URLs:

- https://sources.debian.net/src/findutils/4.9.0-5/ (for browsing the source)
- https://sources.debian.net/src/findutils/4.9.0-5/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/findutils/4.9.0-5/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `gcc-14=14-20240330-1`

Binary Packages:

- `gcc-14-base:amd64=14-20240330-1`
- `libgcc-s1:amd64=14-20240330-1`
- `libstdc++6:amd64=14-20240330-1`

Licenses: (parsed from: `/usr/share/doc/gcc-14-base/copyright`, `/usr/share/doc/libgcc-s1/copyright`, `/usr/share/doc/libstdc++6/copyright`)

- `Artistic`
- `GFDL-1.2`
- `GPL`
- `GPL-3`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris gcc-14=14-20240330-1
'http://deb.debian.org/debian/pool/main/g/gcc-14/gcc-14_14-20240330-1.dsc' gcc-14_14-20240330-1.dsc 46429 SHA256:9de0b0d51f5c0343a3568ea7a3cb9382e88364966a51c5612e016ec3d0eeacb8
'http://deb.debian.org/debian/pool/main/g/gcc-14/gcc-14_14-20240330.orig.tar.gz' gcc-14_14-20240330.orig.tar.gz 92673045 SHA256:25c8bfe87ea63efec67120a8ea99c2710de7b7525009b20453313a64ceb7c7f5
'http://deb.debian.org/debian/pool/main/g/gcc-14/gcc-14_14-20240330-1.debian.tar.xz' gcc-14_14-20240330-1.debian.tar.xz 539176 SHA256:ace05fba034750cf35e9ee8871830d44c47db3fb7bafec6297f76484384b6f7f
```

Other potentially useful URLs:

- https://sources.debian.net/src/gcc-14/14-20240330-1/ (for browsing the source)
- https://sources.debian.net/src/gcc-14/14-20240330-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/gcc-14/14-20240330-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `glibc=2.37-15.1`

Binary Packages:

- `libc-bin=2.37-15.1`
- `libc6:amd64=2.37-15.1`

Licenses: (parsed from: `/usr/share/doc/libc-bin/copyright`, `/usr/share/doc/libc6/copyright`)

- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris glibc=2.37-15.1
'http://deb.debian.org/debian/pool/main/g/glibc/glibc_2.37-15.1.dsc' glibc_2.37-15.1.dsc 9076 SHA256:c5af467421538a96ab5aaceb299a1ef0306298c96a5e1363c323f7892795e5b5
'http://deb.debian.org/debian/pool/main/g/glibc/glibc_2.37.orig.tar.xz' glibc_2.37.orig.tar.xz 19503016 SHA256:d05f010158c16cef110fa1ab560c31477249ee2105360101858a5146aa6fe7d0
'http://deb.debian.org/debian/pool/main/g/glibc/glibc_2.37-15.1.debian.tar.xz' glibc_2.37-15.1.debian.tar.xz 411636 SHA256:b4a9eb4dad44e833299196361c3f7b3918683f55316b28d4c55b50068cb0422e
```

Other potentially useful URLs:

- https://sources.debian.net/src/glibc/2.37-15.1/ (for browsing the source)
- https://sources.debian.net/src/glibc/2.37-15.1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/glibc/2.37-15.1/ (for access to the source package after it no longer exists in the archive)

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

Source:

```console
$ apt-get source -qq --print-uris gnupg2=2.2.40-3
'http://deb.debian.org/debian/pool/main/g/gnupg2/gnupg2_2.2.40-3.dsc' gnupg2_2.2.40-3.dsc 3788 SHA256:4424b8ce66f8f90c25cf072063d39a37ebbb59cbc09a4b140eb177b0bf014357
'http://deb.debian.org/debian/pool/main/g/gnupg2/gnupg2_2.2.40.orig.tar.bz2' gnupg2_2.2.40.orig.tar.bz2 7301631 SHA256:1164b29a75e8ab93ea15033300149e1872a7ef6bdda3d7c78229a735f8204c28
'http://deb.debian.org/debian/pool/main/g/gnupg2/gnupg2_2.2.40.orig.tar.bz2.asc' gnupg2_2.2.40.orig.tar.bz2.asc 228 SHA256:3907dc165299cd53c0b4aec862323c3bce6037c411600ec87dc5eed7a55eba4a
'http://deb.debian.org/debian/pool/main/g/gnupg2/gnupg2_2.2.40-3.debian.tar.xz' gnupg2_2.2.40-3.debian.tar.xz 62828 SHA256:f58d627f2f49b195debff767ddd5173b467628e697c9964e62727eeeea31914b
```

Other potentially useful URLs:

- https://sources.debian.net/src/gnupg2/2.2.40-3/ (for browsing the source)
- https://sources.debian.net/src/gnupg2/2.2.40-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/gnupg2/2.2.40-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `gnutls28=3.8.5-1`

Binary Packages:

- `libgnutls30t64:amd64=3.8.5-1`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/gnutls28/3.8.5-1/


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

### `dpkg` source package: `libcap-ng=0.8.4-2`

Binary Packages:

- `libcap-ng0:amd64=0.8.4-2`

Licenses: (parsed from: `/usr/share/doc/libcap-ng0/copyright`)

- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `LGPL-2.1`
- `LGPL-2.1+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/libcap-ng/0.8.4-2/


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

- `libgcrypt20:amd64=1.10.3-2`

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

### `dpkg` source package: `libgpg-error=1.47-3`

Binary Packages:

- `libgpg-error0:amd64=1.47-3`

Licenses: (parsed from: `/usr/share/doc/libgpg-error0/copyright`)

- `BSD-3-clause`
- `GPL-3`
- `GPL-3+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `g10-permissive`

Source:

```console
$ apt-get source -qq --print-uris libgpg-error=1.47-3
'http://deb.debian.org/debian/pool/main/libg/libgpg-error/libgpg-error_1.47-3.dsc' libgpg-error_1.47-3.dsc 2896 SHA256:350733b58bfa6f865597b41c51a16403aec5818fd70c35306c61decf62af7d15
'http://deb.debian.org/debian/pool/main/libg/libgpg-error/libgpg-error_1.47.orig.tar.bz2' libgpg-error_1.47.orig.tar.bz2 1020862 SHA256:9e3c670966b96ecc746c28c2c419541e3bcb787d1a73930f5e5f5e1bcbbb9bdb
'http://deb.debian.org/debian/pool/main/libg/libgpg-error/libgpg-error_1.47.orig.tar.bz2.asc' libgpg-error_1.47.orig.tar.bz2.asc 228 SHA256:6ab547bf020761e1df80b08335773a91c345ff2c1344f15b1f7d195293ab21a5
'http://deb.debian.org/debian/pool/main/libg/libgpg-error/libgpg-error_1.47-3.debian.tar.xz' libgpg-error_1.47-3.debian.tar.xz 18572 SHA256:3ba56dba7e31bf3bd771a89474a7581217ede3732c2fba8aca8629e6c4d92232
```

Other potentially useful URLs:

- https://sources.debian.net/src/libgpg-error/1.47-3/ (for browsing the source)
- https://sources.debian.net/src/libgpg-error/1.47-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libgpg-error/1.47-3/ (for access to the source package after it no longer exists in the archive)

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

- `libselinux1:amd64=3.5-2+b1`

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

### `dpkg` source package: `ncurses=6.4+20240113-1`

Binary Packages:

- `libtinfo6:amd64=6.4+20240113-1`
- `ncurses-base=6.4+20240113-1`
- `ncurses-bin=6.4+20240113-1`

Licenses: (parsed from: `/usr/share/doc/libtinfo6/copyright`, `/usr/share/doc/ncurses-base/copyright`, `/usr/share/doc/ncurses-bin/copyright`)

- `BSD-3-clause`
- `MIT/X11`
- `X11`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/ncurses/6.4+20240113-1/


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

### `dpkg` source package: `p11-kit=0.25.3-4`

Binary Packages:

- `libp11-kit0:amd64=0.25.3-4`

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
$ apt-get source -qq --print-uris p11-kit=0.25.3-4
'http://deb.debian.org/debian/pool/main/p/p11-kit/p11-kit_0.25.3-4.dsc' p11-kit_0.25.3-4.dsc 2538 SHA256:51ad57264f721d05a23a8f7291fb0135d46c371e6cc85aa09eed1743876c5b32
'http://deb.debian.org/debian/pool/main/p/p11-kit/p11-kit_0.25.3.orig.tar.xz' p11-kit_0.25.3.orig.tar.xz 991528 SHA256:d8ddce1bb7e898986f9d250ccae7c09ce14d82f1009046d202a0eb1b428b2adc
'http://deb.debian.org/debian/pool/main/p/p11-kit/p11-kit_0.25.3.orig.tar.xz.asc' p11-kit_0.25.3.orig.tar.xz.asc 228 SHA256:91fb1fd7690b953eb32bf9ca52ae1b2466457539ac849468f1d236673b354860
'http://deb.debian.org/debian/pool/main/p/p11-kit/p11-kit_0.25.3-4.debian.tar.xz' p11-kit_0.25.3-4.debian.tar.xz 25704 SHA256:7d1e652ad42be131e079755ca8fe23a8ac64b4c7153d6dc52ce68727b14499b2
```

Other potentially useful URLs:

- https://sources.debian.net/src/p11-kit/0.25.3-4/ (for browsing the source)
- https://sources.debian.net/src/p11-kit/0.25.3-4/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/p11-kit/0.25.3-4/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `pam=1.5.3-6`

Binary Packages:

- `libpam-modules:amd64=1.5.3-6`
- `libpam-modules-bin=1.5.3-6`
- `libpam-runtime=1.5.3-6`
- `libpam0g:amd64=1.5.3-6`

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

- http://snapshot.debian.org/package/pam/1.5.3-6/


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

### `dpkg` source package: `perl=5.38.2-3.2`

Binary Packages:

- `perl-base=5.38.2-3.2`

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
$ apt-get source -qq --print-uris perl=5.38.2-3.2
'http://deb.debian.org/debian/pool/main/p/perl/perl_5.38.2-3.2.dsc' perl_5.38.2-3.2.dsc 2946 SHA256:9d5494b48f76abdb907fe4ef6fb85c71c0bae503edb69a782b6dce4de33e47a2
'http://deb.debian.org/debian/pool/main/p/perl/perl_5.38.2.orig-regen-configure.tar.xz' perl_5.38.2.orig-regen-configure.tar.xz 418808 SHA256:4d1b34cc058f9963cb89785ecc040d57f6d7725cd83329cfa4ef8b27566454d2
'http://deb.debian.org/debian/pool/main/p/perl/perl_5.38.2.orig.tar.xz' perl_5.38.2.orig.tar.xz 13679524 SHA256:d91115e90b896520e83d4de6b52f8254ef2b70a8d545ffab33200ea9f1cf29e8
'http://deb.debian.org/debian/pool/main/p/perl/perl_5.38.2-3.2.debian.tar.xz' perl_5.38.2-3.2.debian.tar.xz 165800 SHA256:31c8950b4bba7b2f48a88b44d335c14e3ba2506f260e82023df533163570a7cc
```

Other potentially useful URLs:

- https://sources.debian.net/src/perl/5.38.2-3.2/ (for browsing the source)
- https://sources.debian.net/src/perl/5.38.2-3.2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/perl/5.38.2-3.2/ (for access to the source package after it no longer exists in the archive)

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

### `dpkg` source package: `systemd=255.4-1`

Binary Packages:

- `libsystemd0:amd64=255.4-1+b1`
- `libudev1:amd64=255.4-1+b1`

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
$ apt-get source -qq --print-uris systemd=255.4-1
'http://deb.debian.org/debian/pool/main/s/systemd/systemd_255.4-1.dsc' systemd_255.4-1.dsc 7133 SHA256:d161f791833ede65dd861262509d2fbbb7ff02771969493b04472ad2994e3c07
'http://deb.debian.org/debian/pool/main/s/systemd/systemd_255.4.orig.tar.gz' systemd_255.4.orig.tar.gz 14952427 SHA256:96e75bd08c57ad401677456fb88ef54a9f05bb1695693013bc6ecce839640fd5
'http://deb.debian.org/debian/pool/main/s/systemd/systemd_255.4-1.debian.tar.xz' systemd_255.4-1.debian.tar.xz 172068 SHA256:16cc8104b8f2c5fd598218d48bb1b107719ce25e94055d5dd18ae551bd90a012
```

Other potentially useful URLs:

- https://sources.debian.net/src/systemd/255.4-1/ (for browsing the source)
- https://sources.debian.net/src/systemd/255.4-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/systemd/255.4-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `sysvinit=3.08-7`

Binary Packages:

- `sysvinit-utils=3.08-7`

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

- http://snapshot.debian.org/package/sysvinit/3.08-7/


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

### `dpkg` source package: `tzdata=2024a-2`

Binary Packages:

- `tzdata=2024a-2`

Licenses: (parsed from: `/usr/share/doc/tzdata/copyright`)

- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/tzdata/2024a-2/


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

### `dpkg` source package: `util-linux=2.39.3-11`

Binary Packages:

- `bsdutils=1:2.39.3-11`
- `libblkid1:amd64=2.39.3-11`
- `libmount1:amd64=2.39.3-11`
- `libsmartcols1:amd64=2.39.3-11`
- `libuuid1:amd64=2.39.3-11`
- `mount=2.39.3-11`
- `util-linux=2.39.3-11`

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

- http://snapshot.debian.org/package/util-linux/2.39.3-11/


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

### `dpkg` source package: `zlib=1:1.3.dfsg-3.1`

Binary Packages:

- `zlib1g:amd64=1:1.3.dfsg-3.1`

Licenses: (parsed from: `/usr/share/doc/zlib1g/copyright`)

- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris zlib=1:1.3.dfsg-3.1
'http://deb.debian.org/debian/pool/main/z/zlib/zlib_1.3.dfsg-3.1.dsc' zlib_1.3.dfsg-3.1.dsc 2882 SHA256:0f9b4fcf23b881f0c90f2e758fd66f7774e9f5709ecf9d127173d38167187992
'http://deb.debian.org/debian/pool/main/z/zlib/zlib_1.3.dfsg.orig.tar.xz' zlib_1.3.dfsg.orig.tar.xz 1128572 SHA256:5eea0322c1c21c75cad3b607ac1c43ff5c71e014b8ac4a34300b5e2b80d02e70
'http://deb.debian.org/debian/pool/main/z/zlib/zlib_1.3.dfsg-3.1.debian.tar.xz' zlib_1.3.dfsg-3.1.debian.tar.xz 17496 SHA256:cfc55d2ce0e66259293ebe2ae986e54835a5ad6a4731aa88ad3dfdf1d7fa40e2
```

Other potentially useful URLs:

- https://sources.debian.net/src/zlib/1:1.3.dfsg-3.1/ (for browsing the source)
- https://sources.debian.net/src/zlib/1:1.3.dfsg-3.1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/zlib/1:1.3.dfsg-3.1/ (for access to the source package after it no longer exists in the archive)
