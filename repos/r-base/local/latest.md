# `r-base:4.3.2`

## Docker Metadata

- Image ID: `sha256:4fcd3973c46d5d18c5da58714a8574cceb7c1e2a0424ef20c0a6e2b49a5a0239`
- Created: `2024-02-13T07:59:54.768796358Z`
- Virtual Size: ~ 851.41 Mb  
  (total size of all layers on-disk)
- Arch: `linux`/`amd64`
- Command: `["R"]`
- Environment:
  - `PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin`
  - `LC_ALL=en_US.UTF-8`
  - `LANG=en_US.UTF-8`
  - `R_BASE_VERSION=4.3.2`
- Labels:
  - `org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>`
  - `org.opencontainers.image.licenses=GPL-2.0-or-later`
  - `org.opencontainers.image.source=https://github.com/rocker-org/rocker`
  - `org.opencontainers.image.vendor=Rocker Project`

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
'http://http.debian.net/debian/pool/main/a/acl/acl_2.3.2-1.dsc' acl_2.3.2-1.dsc 2505 SHA256:cb36f16ade6d9cbe7155c74fefd8e56fb3308ee46bf7e8a909feacf48b90164d
'http://http.debian.net/debian/pool/main/a/acl/acl_2.3.2.orig.tar.xz' acl_2.3.2.orig.tar.xz 371680 SHA256:97203a72cae99ab89a067fe2210c1cbf052bc492b479eca7d226d9830883b0bd
'http://http.debian.net/debian/pool/main/a/acl/acl_2.3.2.orig.tar.xz.asc' acl_2.3.2.orig.tar.xz.asc 833 SHA256:184c6a903490885a096095db67b433a04542c6569f167cbe8115268c0f227273
'http://http.debian.net/debian/pool/main/a/acl/acl_2.3.2-1.debian.tar.xz' acl_2.3.2-1.debian.tar.xz 23276 SHA256:abf5d4f58886e3f27dfbd21c740406c425ed8a2bbdaa8def4509fe9b35adbc2a
```

### `dpkg` source package: `apt=2.7.10`

Binary Packages:

- `apt=2.7.10`
- `libapt-pkg6.0:amd64=2.7.10`

Licenses: (parsed from: `/usr/share/doc/apt/copyright`, `/usr/share/doc/libapt-pkg6.0/copyright`)

- `BSD-3-clause`
- `Expat`
- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/apt/2.7.10/


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
'http://http.debian.net/debian/pool/main/a/attr/attr_2.5.2-1.dsc' attr_2.5.2-1.dsc 2477 SHA256:5c14953fc436d6c4ba6dd4a00b2f82a923d5745cc2c993a630e50d9cabaeca0b
'http://http.debian.net/debian/pool/main/a/attr/attr_2.5.2.orig.tar.xz' attr_2.5.2.orig.tar.xz 334180 SHA256:f2e97b0ab7ce293681ab701915766190d607a1dba7fae8a718138150b700a70b
'http://http.debian.net/debian/pool/main/a/attr/attr_2.5.2.orig.tar.xz.asc' attr_2.5.2.orig.tar.xz.asc 833 SHA256:eeac729088d3c6379e91b7596cb3582e46b047c47f0fa3c5c77f9c9e84dc3a4c
'http://http.debian.net/debian/pool/main/a/attr/attr_2.5.2-1.debian.tar.xz' attr_2.5.2-1.debian.tar.xz 25848 SHA256:b4d0670ea47811670bb619252973c7fb186e54b28bd5f2ac3c1a34d6fd089741
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
'http://http.debian.net/debian/pool/main/a/audit/audit_3.1.2-2.dsc' audit_3.1.2-2.dsc 2403 SHA256:5abf7c25864df2c7c4cc29019e7f62eafb94b62594168d0f0531beca9c4f86b5
'http://http.debian.net/debian/pool/main/a/audit/audit_3.1.2.orig.tar.gz' audit_3.1.2.orig.tar.gz 1219860 SHA256:c0b1792d1f0a88c6f1828710509cbb987059fc68712c97669ca90eae103d287d
'http://http.debian.net/debian/pool/main/a/audit/audit_3.1.2-2.debian.tar.xz' audit_3.1.2-2.debian.tar.xz 18340 SHA256:a9dcaa337e5ab65d6ec86a7b251d2d64a8a3a43c81adc938897a7a3553faf5f5
```

### `dpkg` source package: `base-files=13`

Binary Packages:

- `base-files=13`

Licenses: (parsed from: `/usr/share/doc/base-files/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris base-files=13
'http://http.debian.net/debian/pool/main/b/base-files/base-files_13.dsc' base-files_13.dsc 1093 SHA256:9a355f5c19670ce338c4febb196c427cc5f67940953478b515d555fba9fbdddc
'http://http.debian.net/debian/pool/main/b/base-files/base-files_13.tar.xz' base-files_13.tar.xz 66064 SHA256:439153bdf296481135cb0b801fe46765dc83f8b9914a0275d6a162339de12f56
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
'http://http.debian.net/debian/pool/main/b/base-passwd/base-passwd_3.6.3.dsc' base-passwd_3.6.3.dsc 1762 SHA256:bac1a87f919fd8ab28480cc1fd8126b2068a577faf4223f8a2be6baf328d313e
'http://http.debian.net/debian/pool/main/b/base-passwd/base-passwd_3.6.3.tar.xz' base-passwd_3.6.3.tar.xz 58284 SHA256:83575327d8318a419caf2d543341215c046044073d1afec2acc0ac4d8095ff39
```

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
'http://http.debian.net/debian/pool/main/b/bash/bash_5.2.21-2.dsc' bash_5.2.21-2.dsc 2295 SHA256:134867cb0fb5bd81fcb3b90cf9e54db4eb8fa6c4ef65bfc6fe6d4c2a0703a8af
'http://http.debian.net/debian/pool/main/b/bash/bash_5.2.21.orig.tar.xz' bash_5.2.21.orig.tar.xz 5598816 SHA256:ec21ab4efd6bd7a6e2802fbda622b81bfc43a8095d721234d4bf075797683014
'http://http.debian.net/debian/pool/main/b/bash/bash_5.2.21-2.debian.tar.xz' bash_5.2.21-2.debian.tar.xz 87876 SHA256:419795e70b50d57effe7b993cbdf47ea57d5a59de9eb8a30b46a1a6057381344
```

### `dpkg` source package: `binutils=2.42-2`

Binary Packages:

- `binutils=2.42-2`
- `binutils-common:amd64=2.42-2`
- `binutils-x86-64-linux-gnu=2.42-2`
- `libbinutils:amd64=2.42-2`
- `libctf-nobfd0:amd64=2.42-2`
- `libctf0:amd64=2.42-2`
- `libgprofng0:amd64=2.42-2`
- `libsframe1:amd64=2.42-2`

Licenses: (parsed from: `/usr/share/doc/binutils/copyright`, `/usr/share/doc/binutils-common/copyright`, `/usr/share/doc/binutils-x86-64-linux-gnu/copyright`, `/usr/share/doc/libbinutils/copyright`, `/usr/share/doc/libctf-nobfd0/copyright`, `/usr/share/doc/libctf0/copyright`, `/usr/share/doc/libgprofng0/copyright`, `/usr/share/doc/libsframe1/copyright`)

- `GFDL`
- `GPL`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris binutils=2.42-2
'http://http.debian.net/debian/pool/main/b/binutils/binutils_2.42-2.dsc' binutils_2.42-2.dsc 12563 SHA256:b59f69a45b576ecf267290c46b3ed8161bdcc90b5e8d51d8e1cb16a5a2905ee6
'http://http.debian.net/debian/pool/main/b/binutils/binutils_2.42.orig.tar.xz' binutils_2.42.orig.tar.xz 27791308 SHA256:b2ca95ea1f2527aa225c3ed8b80de9dc366515c7a1219092d7111d870ec6f8a2
'http://http.debian.net/debian/pool/main/b/binutils/binutils_2.42-2.debian.tar.xz' binutils_2.42-2.debian.tar.xz 125972 SHA256:94eb0a675b86ee9e6eedb2f81fc57dee4c25135101b7a58fd9532340288e58d4
```

### `dpkg` source package: `boot=1.3-28.1-1`

Binary Packages:

- `r-cran-boot=1.3-28.1-1`

Licenses: (parsed from: `/usr/share/doc/r-cran-boot/copyright`)

- `'unlimited distribution'`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/boot/1.3-28.1-1/


### `dpkg` source package: `brotli=1.1.0-2`

Binary Packages:

- `libbrotli1:amd64=1.1.0-2+b3`

Licenses: (parsed from: `/usr/share/doc/libbrotli1/copyright`)

- `MIT`

Source:

```console
$ apt-get source -qq --print-uris brotli=1.1.0-2
'http://http.debian.net/debian/pool/main/b/brotli/brotli_1.1.0-2.dsc' brotli_1.1.0-2.dsc 2261 SHA256:39b06802a852629132d549a7f7449dee7f435e801706714a4bc2ea2f15b28f36
'http://http.debian.net/debian/pool/main/b/brotli/brotli_1.1.0.orig.tar.gz' brotli_1.1.0.orig.tar.gz 512036 SHA256:10973f4b4199eafa1d5735ef661ddb2ec2f97319ee9fd1824d4aabe08cff5265
'http://http.debian.net/debian/pool/main/b/brotli/brotli_1.1.0-2.debian.tar.xz' brotli_1.1.0-2.debian.tar.xz 5480 SHA256:3d913a3740bcad9a294007575a6beb1846beadbd62b44fb2bf9fdaeddea3236f
```

### `dpkg` source package: `build-essential=12.10`

Binary Packages:

- `build-essential=12.10`

Licenses: (parsed from: `/usr/share/doc/build-essential/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris build-essential=12.10
'http://http.debian.net/debian/pool/main/b/build-essential/build-essential_12.10.dsc' build-essential_12.10.dsc 2172 SHA256:b2d9c962b539f011807fdd62761f749eed12a7f061d75c3752a48bd2060030d4
'http://http.debian.net/debian/pool/main/b/build-essential/build-essential_12.10.tar.xz' build-essential_12.10.tar.xz 51760 SHA256:a367724c8788696a7cc6f8f09b341949c49fcd06684c3f0e3a1113bbaf75194a
```

### `dpkg` source package: `bzip2=1.0.8-5`

Binary Packages:

- `bzip2=1.0.8-5+b2`
- `libbz2-1.0:amd64=1.0.8-5+b2`
- `libbz2-dev:amd64=1.0.8-5+b2`

Licenses: (parsed from: `/usr/share/doc/bzip2/copyright`, `/usr/share/doc/libbz2-1.0/copyright`, `/usr/share/doc/libbz2-dev/copyright`)

- `BSD-variant`
- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris bzip2=1.0.8-5
'http://http.debian.net/debian/pool/main/b/bzip2/bzip2_1.0.8-5.dsc' bzip2_1.0.8-5.dsc 2206 SHA256:ed9c40f4de3f9e064535e15eac1c61a0f606763db98f4579dbc04067b94a8944
'http://http.debian.net/debian/pool/main/b/bzip2/bzip2_1.0.8.orig.tar.gz' bzip2_1.0.8.orig.tar.gz 810029 SHA256:ab5a03176ee106d3f0fa90e381da478ddae405918153cca248e682cd0c4a2269
'http://http.debian.net/debian/pool/main/b/bzip2/bzip2_1.0.8-5.debian.tar.bz2' bzip2_1.0.8-5.debian.tar.bz2 26787 SHA256:d68c6eba11d70e14319e24ef1451880a03023b2b75364646adb117086db36039
```

### `dpkg` source package: `ca-certificates=20240203`

Binary Packages:

- `ca-certificates=20240203`

Licenses: (parsed from: `/usr/share/doc/ca-certificates/copyright`)

- `GPL-2`
- `GPL-2+`
- `MPL-2.0`

Source:

```console
$ apt-get source -qq --print-uris ca-certificates=20240203
'http://http.debian.net/debian/pool/main/c/ca-certificates/ca-certificates_20240203.dsc' ca-certificates_20240203.dsc 1766 SHA256:629afee9b327ce4df4ad0d77ad7b10383474a432e1af30516a7e81669420109b
'http://http.debian.net/debian/pool/main/c/ca-certificates/ca-certificates_20240203.tar.xz' ca-certificates_20240203.tar.xz 263276 SHA256:3286d3fc42c4d11b7086711a85f865b44065ce05cf1fb5376b2abed07622a9c6
```

### `dpkg` source package: `cairo=1.18.0-1`

Binary Packages:

- `libcairo2:amd64=1.18.0-1+b1`

Licenses: (parsed from: `/usr/share/doc/libcairo2/copyright`)

- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris cairo=1.18.0-1
'http://http.debian.net/debian/pool/main/c/cairo/cairo_1.18.0-1.dsc' cairo_1.18.0-1.dsc 2772 SHA256:524223b43506f55b644770626b215cb694e6b8d52c57dbf149150453622a99da
'http://http.debian.net/debian/pool/main/c/cairo/cairo_1.18.0.orig.tar.xz' cairo_1.18.0.orig.tar.xz 33761148 SHA256:243a0736b978a33dee29f9cca7521733b78a65b5418206fef7bd1c3d4cf10b64
'http://http.debian.net/debian/pool/main/c/cairo/cairo_1.18.0-1.debian.tar.xz' cairo_1.18.0-1.debian.tar.xz 29720 SHA256:6cb6c2f74294818f9b6322b2431f994665ff12ac8d931e665e6feefbd0c6e3e4
```

### `dpkg` source package: `cdebconf=0.271`

Binary Packages:

- `libdebconfclient0:amd64=0.271`

Licenses: (parsed from: `/usr/share/doc/libdebconfclient0/copyright`)

- `BSD-2-Clause`
- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris cdebconf=0.271
'http://http.debian.net/debian/pool/main/c/cdebconf/cdebconf_0.271.dsc' cdebconf_0.271.dsc 2707 SHA256:626c8da9b0fd07f37c94940401a8ba92bc3c454673c266e9c927934139e2a079
'http://http.debian.net/debian/pool/main/c/cdebconf/cdebconf_0.271.tar.xz' cdebconf_0.271.tar.xz 284308 SHA256:b66fd2ea674d22f64a01672fe6c1891ef54ca906fb5c49d8362cba0d78b270c8
```

### `dpkg` source package: `cluster=2.1.6-1`

Binary Packages:

- `r-cran-cluster=2.1.6-1`

Licenses: (parsed from: `/usr/share/doc/r-cran-cluster/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris cluster=2.1.6-1
'http://http.debian.net/debian/pool/main/c/cluster/cluster_2.1.6-1.dsc' cluster_2.1.6-1.dsc 1831 SHA256:2a30de784a94d98b08ce82e1c6da81c851c83587ec87012b3df0f5d2ea759598
'http://http.debian.net/debian/pool/main/c/cluster/cluster_2.1.6.orig.tar.gz' cluster_2.1.6.orig.tar.gz 369050 SHA256:d1c50efafd35a55387cc5b36086b97d5591e0b33c48dc718005d2f5907113164
'http://http.debian.net/debian/pool/main/c/cluster/cluster_2.1.6-1.debian.tar.xz' cluster_2.1.6-1.debian.tar.xz 4356 SHA256:7c0fc2b7d445438fc5d92c8289369c8611024c07aa62f1203d16927842d4fb4d
```

### `dpkg` source package: `codetools=0.2-19-1`

Binary Packages:

- `r-cran-codetools=0.2-19-1`

Licenses: (parsed from: `/usr/share/doc/r-cran-codetools/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris codetools=0.2-19-1
'http://http.debian.net/debian/pool/main/c/codetools/codetools_0.2-19-1.dsc' codetools_0.2-19-1.dsc 1859 SHA256:c2254fd82acbc89bab6588b8d902be70baa79ad716ef261f3b04ba6333058940
'http://http.debian.net/debian/pool/main/c/codetools/codetools_0.2-19.orig.tar.gz' codetools_0.2-19.orig.tar.gz 38235 SHA256:c4b7e567c87f33dad85de92f79641e5e5b5deede6d19a9dfa47133d191782dab
'http://http.debian.net/debian/pool/main/c/codetools/codetools_0.2-19-1.debian.tar.xz' codetools_0.2-19-1.debian.tar.xz 2900 SHA256:23fb4526e3d9b4b18388b255d9deed50bf55b277f4abfdc7bc9b4556092090f1
```

### `dpkg` source package: `coreutils=9.4-3`

Binary Packages:

- `coreutils=9.4-3+b1`

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
$ apt-get source -qq --print-uris coreutils=9.4-3
'http://http.debian.net/debian/pool/main/c/coreutils/coreutils_9.4-3.dsc' coreutils_9.4-3.dsc 1860 SHA256:ca3e625d24ed3983ec88b11d80ae0200e89eb70f719f6da352cfa28a64d8b6fe
'http://http.debian.net/debian/pool/main/c/coreutils/coreutils_9.4.orig.tar.xz' coreutils_9.4.orig.tar.xz 5979200 SHA256:ea613a4cf44612326e917201bbbcdfbd301de21ffc3b59b6e5c07e040b275e52
'http://http.debian.net/debian/pool/main/c/coreutils/coreutils_9.4-3.debian.tar.xz' coreutils_9.4-3.debian.tar.xz 29716 SHA256:a4b4a1ee99cf8114a438b592cd7ffcbb3eb17ff8b8b7ca717509112481527567
```

### `dpkg` source package: `curl=8.5.0-2`

Binary Packages:

- `libcurl4:amd64=8.5.0-2`

Licenses: (parsed from: `/usr/share/doc/libcurl4/copyright`)

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
$ apt-get source -qq --print-uris curl=8.5.0-2
'http://deb.debian.org/debian/pool/main/c/curl/curl_8.5.0-2.dsc' curl_8.5.0-2.dsc 3117 SHA256:64ac1de3cabae24dcc1d403977cae690b902db3585b540ff0bd9ac9a83e2d052
'http://deb.debian.org/debian/pool/main/c/curl/curl_8.5.0.orig.tar.gz' curl_8.5.0.orig.tar.gz 4372979 SHA256:05fc17ff25b793a437a0906e0484b82172a9f4de02be5ed447e0cab8c3475add
'http://deb.debian.org/debian/pool/main/c/curl/curl_8.5.0.orig.tar.gz.asc' curl_8.5.0.orig.tar.gz.asc 488 SHA256:e5c4311a86b03daea93290de17cf0e3b46e468a1d99bd5b9934d91af5409d378
'http://deb.debian.org/debian/pool/main/c/curl/curl_8.5.0-2.debian.tar.xz' curl_8.5.0-2.debian.tar.xz 47912 SHA256:5e398fc2d420bfc3fedc4d3cdedfad8bc4eadf5445bf59905af0e6f2602fcb66
```

Other potentially useful URLs:

- https://sources.debian.net/src/curl/8.5.0-2/ (for browsing the source)
- https://sources.debian.net/src/curl/8.5.0-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/curl/8.5.0-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `cyrus-sasl2=2.1.28+dfsg1-4`

Binary Packages:

- `libsasl2-2:amd64=2.1.28+dfsg1-4+b1`
- `libsasl2-modules-db:amd64=2.1.28+dfsg1-4+b1`

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
'http://http.debian.net/debian/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.28%2bdfsg1-4.dsc' cyrus-sasl2_2.1.28+dfsg1-4.dsc 3224 SHA256:d2169fde5404f07f71ae5265e308f0239e2788c0f8115fa3f10ce83ba4c1fd5d
'http://http.debian.net/debian/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.28%2bdfsg1.orig.tar.xz' cyrus-sasl2_2.1.28+dfsg1.orig.tar.xz 794540 SHA256:e796a5d85d1a85e1b433d43504e467f9075c7ebc0b45730a3996cf11b1deada4
'http://http.debian.net/debian/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.28%2bdfsg1-4.debian.tar.xz' cyrus-sasl2_2.1.28+dfsg1-4.debian.tar.xz 96688 SHA256:10f7765c85fb0601c0e9cf9d0ac250d194cd7d190f4656ca52dcd993c731ff4c
```

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
'http://http.debian.net/debian/pool/main/d/dash/dash_0.5.12-6.dsc' dash_0.5.12-6.dsc 1520 SHA256:dfca9cb9a537d09c190baa9fb15848ecaa55f301843779f26260b1429cd72746
'http://http.debian.net/debian/pool/main/d/dash/dash_0.5.12.orig.tar.gz' dash_0.5.12.orig.tar.gz 246054 SHA256:6a474ac46e8b0b32916c4c60df694c82058d3297d8b385b74508030ca4a8f28a
'http://http.debian.net/debian/pool/main/d/dash/dash_0.5.12-6.debian.tar.xz' dash_0.5.12-6.debian.tar.xz 39116 SHA256:155173292d95943d2c737c0f7f4733bb6b39244522f810ee4a64f7be0f4865ab
```

### `dpkg` source package: `db5.3=5.3.28+dfsg2-4`

Binary Packages:

- `libdb5.3:amd64=5.3.28+dfsg2-4+b1`

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
'http://http.debian.net/debian/pool/main/d/db5.3/db5.3_5.3.28%2bdfsg2-4.dsc' db5.3_5.3.28+dfsg2-4.dsc 2190 SHA256:c25a3d8a199e6ea7a251a192acb6c8e5e130271dfa190b6486ac08dbb81a861b
'http://http.debian.net/debian/pool/main/d/db5.3/db5.3_5.3.28%2bdfsg2.orig.tar.xz' db5.3_5.3.28+dfsg2.orig.tar.xz 21287688 SHA256:ad41b507415dec8316e828b2230242af2251d2c86eefa3c7aa9ef47c5239ef33
'http://http.debian.net/debian/pool/main/d/db5.3/db5.3_5.3.28%2bdfsg2-4.debian.tar.xz' db5.3_5.3.28+dfsg2-4.debian.tar.xz 33624 SHA256:1cab3a408ba22a1307d4b55c5aff986423a75f8b95cc58b7bcaa143817bc1aa4
```

### `dpkg` source package: `debconf=1.5.85`

Binary Packages:

- `debconf=1.5.85`

Licenses: (parsed from: `/usr/share/doc/debconf/copyright`)

- `BSD-2-clause`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/debconf/1.5.85/


### `dpkg` source package: `debian-archive-keyring=2023.4`

Binary Packages:

- `debian-archive-keyring=2023.4`

Licenses: (parsed from: `/usr/share/doc/debian-archive-keyring/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris debian-archive-keyring=2023.4
'http://http.debian.net/debian/pool/main/d/debian-archive-keyring/debian-archive-keyring_2023.4.dsc' debian-archive-keyring_2023.4.dsc 1261 SHA256:c97d048486078fcc6866a477df83b19270ae872102f4ed64b5a5e9995ff79afa
'http://http.debian.net/debian/pool/main/d/debian-archive-keyring/debian-archive-keyring_2023.4.tar.xz' debian-archive-keyring_2023.4.tar.xz 177568 SHA256:7f9b64d7c5e748b0cb99fd0674d872111c219e119f296912c59fc61ab49bb78a
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
'http://http.debian.net/debian/pool/main/d/debianutils/debianutils_5.16.dsc' debianutils_5.16.dsc 1313 SHA256:fef33bd1a13391d16e0a1ee4b81c1b5bfaa85aeacf05290a9b09a5c4337c89e5
'http://http.debian.net/debian/pool/main/d/debianutils/debianutils_5.16.tar.xz' debianutils_5.16.tar.xz 105808 SHA256:eeb069c2639906f4181214dd1c4e448bc825229b0250ebf66f69c7344e8aa1e0
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
'http://http.debian.net/debian/pool/main/d/diffutils/diffutils_3.10-1.dsc' diffutils_3.10-1.dsc 1715 SHA256:f7542884c67d44f0af356c5365a3fef8a298f1fbcbebf9df81cfbc6d6937f05f
'http://http.debian.net/debian/pool/main/d/diffutils/diffutils_3.10.orig.tar.xz' diffutils_3.10.orig.tar.xz 1624240 SHA256:90e5e93cc724e4ebe12ede80df1634063c7a855692685919bfe60b556c9bd09e
'http://http.debian.net/debian/pool/main/d/diffutils/diffutils_3.10.orig.tar.xz.asc' diffutils_3.10.orig.tar.xz.asc 833 SHA256:a94faf8f1baa04ff220f7b2ccb137c16337284e023ebc4a1d5df475c08d810f7
'http://http.debian.net/debian/pool/main/d/diffutils/diffutils_3.10-1.debian.tar.xz' diffutils_3.10-1.debian.tar.xz 13952 SHA256:ebf51a7ceff8c882f997ca428232fd3b58ac59a70840c4b10f8fcfaa881598ce
```

### `dpkg` source package: `dpkg=1.22.4`

Binary Packages:

- `dpkg=1.22.4`
- `dpkg-dev=1.22.4`
- `libdpkg-perl=1.22.4`

Licenses: (parsed from: `/usr/share/doc/dpkg/copyright`, `/usr/share/doc/dpkg-dev/copyright`, `/usr/share/doc/libdpkg-perl/copyright`)

- `GPL-2`
- `GPL-2+`
- `public-domain-s-s-d`

Source:

```console
$ apt-get source -qq --print-uris dpkg=1.22.4
'http://deb.debian.org/debian/pool/main/d/dpkg/dpkg_1.22.4.dsc' dpkg_1.22.4.dsc 3041 SHA256:ee53c49c12d0f7e7616f0143fdbd6f587ed68c5241a739e9224302fa165e2f95
'http://deb.debian.org/debian/pool/main/d/dpkg/dpkg_1.22.4.tar.xz' dpkg_1.22.4.tar.xz 5623080 SHA256:40818c174e6074a190e0013fa0ea8b04db743b8e5e7a7818239510fbb4e6eb1d
```

Other potentially useful URLs:

- https://sources.debian.net/src/dpkg/1.22.4/ (for browsing the source)
- https://sources.debian.net/src/dpkg/1.22.4/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/dpkg/1.22.4/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `e2fsprogs=1.47.0-2`

Binary Packages:

- `e2fsprogs=1.47.0-2+b1`
- `libcom-err2:amd64=1.47.0-2+b1`
- `libext2fs2:amd64=1.47.0-2+b1`
- `libss2:amd64=1.47.0-2+b1`
- `logsave=1.47.0-2+b1`

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
$ apt-get source -qq --print-uris e2fsprogs=1.47.0-2
'http://http.debian.net/debian/pool/main/e/e2fsprogs/e2fsprogs_1.47.0-2.dsc' e2fsprogs_1.47.0-2.dsc 2846 SHA256:35b4de254e021f721362b767994598e249fea02e38ac446197cd9c22be1130fd
'http://http.debian.net/debian/pool/main/e/e2fsprogs/e2fsprogs_1.47.0.orig.tar.gz' e2fsprogs_1.47.0.orig.tar.gz 9637717 SHA256:6667afde56eef0c6af26684974400e4d2288ea49e9441bf5e6229195d51a3578
'http://http.debian.net/debian/pool/main/e/e2fsprogs/e2fsprogs_1.47.0.orig.tar.gz.asc' e2fsprogs_1.47.0.orig.tar.gz.asc 488 SHA256:704928204a52ddaa0ac8ef549c1bfba3c38e66c361d3853c8a4c38e6082b90f1
'http://http.debian.net/debian/pool/main/e/e2fsprogs/e2fsprogs_1.47.0-2.debian.tar.xz' e2fsprogs_1.47.0-2.debian.tar.xz 87328 SHA256:3a756e08d300666039e34577293d11d70c7a1da7850fad478580a81af6348277
```

### `dpkg` source package: `ed=1.20-1`

Binary Packages:

- `ed=1.20-1`

Licenses: (parsed from: `/usr/share/doc/ed/copyright`)

- `BSD-2-Clause`
- `FCONF`
- `FDOC`
- `FLOG`
- `GFDL-1.3`
- `GFDL-NIV-1.3+`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/ed/1.20-1/


### `dpkg` source package: `expat=2.5.0-2`

Binary Packages:

- `libexpat1:amd64=2.5.0-2+b2`

Licenses: (parsed from: `/usr/share/doc/libexpat1/copyright`)

- `MIT`

Source:

```console
$ apt-get source -qq --print-uris expat=2.5.0-2
'http://deb.debian.org/debian/pool/main/e/expat/expat_2.5.0-2.dsc' expat_2.5.0-2.dsc 1964 SHA256:b4aab5ad11812b0593128742f08be007a0c1663d683b7ef705d0660db6e94544
'http://deb.debian.org/debian/pool/main/e/expat/expat_2.5.0.orig.tar.gz' expat_2.5.0.orig.tar.gz 8320988 SHA256:ab00ee05c7067fd10a35c5d2a4922ebba746ddd50ff83b79c828da17bbdf1757
'http://deb.debian.org/debian/pool/main/e/expat/expat_2.5.0-2.debian.tar.xz' expat_2.5.0-2.debian.tar.xz 12804 SHA256:605973555634c2197ce219736cbb7eb17464894768c5fe2c4b8b8279f052ece5
```

Other potentially useful URLs:

- https://sources.debian.net/src/expat/2.5.0-2/ (for browsing the source)
- https://sources.debian.net/src/expat/2.5.0-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/expat/2.5.0-2/ (for access to the source package after it no longer exists in the archive)

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
'http://http.debian.net/debian/pool/main/f/findutils/findutils_4.9.0-5.dsc' findutils_4.9.0-5.dsc 2272 SHA256:7d723c60c50b8b624250ad7d6fbb1ca404756a7b69209753e57c8403e06a07a5
'http://http.debian.net/debian/pool/main/f/findutils/findutils_4.9.0.orig.tar.xz' findutils_4.9.0.orig.tar.xz 2046252 SHA256:a2bfb8c09d436770edc59f50fa483e785b161a3b7b9d547573cb08065fd462fe
'http://http.debian.net/debian/pool/main/f/findutils/findutils_4.9.0.orig.tar.xz.asc' findutils_4.9.0.orig.tar.xz.asc 488 SHA256:924c3719d066eda1b3e47175f8b83e90e9a23f0a639ebe7445621917b283c385
'http://http.debian.net/debian/pool/main/f/findutils/findutils_4.9.0-5.debian.tar.xz' findutils_4.9.0-5.debian.tar.xz 32744 SHA256:456831869d49d8906a98beb2bcbb61e5911d9c44082c4b716615bc23f26c4f20
```

### `dpkg` source package: `fontconfig=2.14.2-6`

Binary Packages:

- `fontconfig=2.14.2-6+b1`
- `fontconfig-config=2.14.2-6+b1`
- `libfontconfig1:amd64=2.14.2-6+b1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/fontconfig/2.14.2-6/


### `dpkg` source package: `foreign=0.8.86-1`

Binary Packages:

- `r-cran-foreign=0.8.86-1`

Licenses: (parsed from: `/usr/share/doc/r-cran-foreign/copyright`)

- `GPL`
- `GPL `

Source:

```console
$ apt-get source -qq --print-uris foreign=0.8.86-1
'http://http.debian.net/debian/pool/main/f/foreign/foreign_0.8.86-1.dsc' foreign_0.8.86-1.dsc 1838 SHA256:0bcc9a523a8c972c243c2df9b814d75914908d92566f2c1607708c1fe177eee7
'http://http.debian.net/debian/pool/main/f/foreign/foreign_0.8.86.orig.tar.gz' foreign_0.8.86.orig.tar.gz 361790 SHA256:a729120108b29ca9744cadd61e3e6a9dc4188a007055c22b6b9a30a676e8c3e1
'http://http.debian.net/debian/pool/main/f/foreign/foreign_0.8.86-1.debian.tar.xz' foreign_0.8.86-1.debian.tar.xz 4376 SHA256:35d6c74f913fdc2f501484cca7db0547f9199bf040846c88374854f19e7c2976
```

### `dpkg` source package: `freetype=2.13.2+dfsg-1`

Binary Packages:

- `libfreetype6:amd64=2.13.2+dfsg-1+b1`

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
$ apt-get source -qq --print-uris freetype=2.13.2+dfsg-1
'http://http.debian.net/debian/pool/main/f/freetype/freetype_2.13.2%2bdfsg-1.dsc' freetype_2.13.2+dfsg-1.dsc 3686 SHA256:0e00399f7835b49c2606053b6681d2ef43693c6d5d7e6c86c29d1784c5e95e5a
'http://http.debian.net/debian/pool/main/f/freetype/freetype_2.13.2%2bdfsg.orig-ft2demos.tar.xz' freetype_2.13.2+dfsg.orig-ft2demos.tar.xz 341140 SHA256:99ee2ed8b98bcfad17bc57c2d9699d764f20fe29ad304c69b8eb28834ca3b48e
'http://http.debian.net/debian/pool/main/f/freetype/freetype_2.13.2%2bdfsg.orig-ft2demos.tar.xz.asc' freetype_2.13.2+dfsg.orig-ft2demos.tar.xz.asc 833 SHA256:e58ba462f7bdcdc5899f777d33453c1ce6f6e46b080047580f45c9fd9f2dc08c
'http://http.debian.net/debian/pool/main/f/freetype/freetype_2.13.2%2bdfsg.orig-ft2docs.tar.xz' freetype_2.13.2+dfsg.orig-ft2docs.tar.xz 2173920 SHA256:685c25e1035a5076e5097186b3143b9c06878f3f9087d0a81e4d8538d5d15424
'http://http.debian.net/debian/pool/main/f/freetype/freetype_2.13.2%2bdfsg.orig-ft2docs.tar.xz.asc' freetype_2.13.2+dfsg.orig-ft2docs.tar.xz.asc 833 SHA256:d7e17c8a3bce50181530ebe06346f506cbfc92ecc5ca7cc395c7dbb24a71a5c0
'http://http.debian.net/debian/pool/main/f/freetype/freetype_2.13.2%2bdfsg.orig.tar.xz' freetype_2.13.2+dfsg.orig.tar.xz 2220368 SHA256:48c78a4194adfcd15a4d089f3206dab8454c311f5577f3ef7eaef95f777f86e6
'http://http.debian.net/debian/pool/main/f/freetype/freetype_2.13.2%2bdfsg-1.debian.tar.xz' freetype_2.13.2+dfsg-1.debian.tar.xz 43824 SHA256:c1db3a2bf2a754fc3666b06757f4055fa7f964b256aaa520f6b7142b68e3c0bb
```

### `dpkg` source package: `fribidi=1.0.13-3`

Binary Packages:

- `libfribidi0:amd64=1.0.13-3+b1`

Licenses: (parsed from: `/usr/share/doc/libfribidi0/copyright`)

- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris fribidi=1.0.13-3
'http://http.debian.net/debian/pool/main/f/fribidi/fribidi_1.0.13-3.dsc' fribidi_1.0.13-3.dsc 2007 SHA256:05a44442861c66fa72d7764ff4c4ad4cf46114eb7fb53268b8c46bc3e3fa06b9
'http://http.debian.net/debian/pool/main/f/fribidi/fribidi_1.0.13.orig.tar.xz' fribidi_1.0.13.orig.tar.xz 1170100 SHA256:7fa16c80c81bd622f7b198d31356da139cc318a63fc7761217af4130903f54a2
'http://http.debian.net/debian/pool/main/f/fribidi/fribidi_1.0.13-3.debian.tar.xz' fribidi_1.0.13-3.debian.tar.xz 8848 SHA256:6e1e94396207a0acfbaa4dcbbb06ccc110fd9f285fd39ca313b5a8a3da9936fa
```

### `dpkg` source package: `gcc-13=13.2.0-13`

Binary Packages:

- `cpp-13=13.2.0-13`
- `cpp-13-x86-64-linux-gnu=13.2.0-13`
- `g++-13=13.2.0-13`
- `g++-13-x86-64-linux-gnu=13.2.0-13`
- `gcc-13=13.2.0-13`
- `gcc-13-base:amd64=13.2.0-13`
- `gcc-13-x86-64-linux-gnu=13.2.0-13`
- `gfortran-13=13.2.0-13`
- `gfortran-13-x86-64-linux-gnu=13.2.0-13`
- `libgcc-13-dev:amd64=13.2.0-13`
- `libgfortran-13-dev:amd64=13.2.0-13`
- `libstdc++-13-dev:amd64=13.2.0-13`

Licenses: (parsed from: `/usr/share/doc/cpp-13/copyright`, `/usr/share/doc/cpp-13-x86-64-linux-gnu/copyright`, `/usr/share/doc/g++-13/copyright`, `/usr/share/doc/g++-13-x86-64-linux-gnu/copyright`, `/usr/share/doc/gcc-13/copyright`, `/usr/share/doc/gcc-13-base/copyright`, `/usr/share/doc/gcc-13-x86-64-linux-gnu/copyright`, `/usr/share/doc/gfortran-13/copyright`, `/usr/share/doc/gfortran-13-x86-64-linux-gnu/copyright`, `/usr/share/doc/libgcc-13-dev/copyright`, `/usr/share/doc/libgfortran-13-dev/copyright`, `/usr/share/doc/libstdc++-13-dev/copyright`)

- `Artistic`
- `GFDL-1.2`
- `GPL`
- `GPL-2`
- `GPL-3`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris gcc-13=13.2.0-13
'http://http.debian.net/debian/pool/main/g/gcc-13/gcc-13_13.2.0-13.dsc' gcc-13_13.2.0-13.dsc 39059 SHA256:1364ce788f123bb41b633c0a50b604d7ebb7823f81153ffe077f6a87bd114f7e
'http://http.debian.net/debian/pool/main/g/gcc-13/gcc-13_13.2.0.orig.tar.gz' gcc-13_13.2.0.orig.tar.gz 89714914 SHA256:eb19e797d4277a1ad26b1992bbf22dc66d11cce0c238491e746e50a7599aa064
'http://http.debian.net/debian/pool/main/g/gcc-13/gcc-13_13.2.0-13.debian.tar.xz' gcc-13_13.2.0-13.debian.tar.xz 1789428 SHA256:97e85b24c9ac130d9aec1ca26ac6b948338277929125aa956cbff009280a9648
```

### `dpkg` source package: `gcc-14=14-20240201-3`

Binary Packages:

- `gcc-14-base:amd64=14-20240201-3`
- `libasan8:amd64=14-20240201-3`
- `libatomic1:amd64=14-20240201-3`
- `libcc1-0:amd64=14-20240201-3`
- `libgcc-s1:amd64=14-20240201-3`
- `libgfortran5:amd64=14-20240201-3`
- `libgomp1:amd64=14-20240201-3`
- `libhwasan0:amd64=14-20240201-3`
- `libitm1:amd64=14-20240201-3`
- `liblsan0:amd64=14-20240201-3`
- `libquadmath0:amd64=14-20240201-3`
- `libstdc++6:amd64=14-20240201-3`
- `libtsan2:amd64=14-20240201-3`
- `libubsan1:amd64=14-20240201-3`

Licenses: (parsed from: `/usr/share/doc/gcc-14-base/copyright`, `/usr/share/doc/libasan8/copyright`, `/usr/share/doc/libatomic1/copyright`, `/usr/share/doc/libcc1-0/copyright`, `/usr/share/doc/libgcc-s1/copyright`, `/usr/share/doc/libgfortran5/copyright`, `/usr/share/doc/libgomp1/copyright`, `/usr/share/doc/libhwasan0/copyright`, `/usr/share/doc/libitm1/copyright`, `/usr/share/doc/liblsan0/copyright`, `/usr/share/doc/libquadmath0/copyright`, `/usr/share/doc/libstdc++6/copyright`, `/usr/share/doc/libtsan2/copyright`, `/usr/share/doc/libubsan1/copyright`)

- `Artistic`
- `GFDL-1.2`
- `GPL`
- `GPL-3`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris gcc-14=14-20240201-3
'http://http.debian.net/debian/pool/main/g/gcc-14/gcc-14_14-20240201-3.dsc' gcc-14_14-20240201-3.dsc 46482 SHA256:88e0f621b6c4ea4fcac1c824b322cf2e47937ed8db1d81ec126a347f44d631a9
'http://http.debian.net/debian/pool/main/g/gcc-14/gcc-14_14-20240201.orig.tar.gz' gcc-14_14-20240201.orig.tar.gz 89550763 SHA256:0572903e5285156e9711f33a47dae55b848fa590a28ab55faee9dbdbf8c228d3
'http://http.debian.net/debian/pool/main/g/gcc-14/gcc-14_14-20240201-3.debian.tar.xz' gcc-14_14-20240201-3.debian.tar.xz 536448 SHA256:312ec3695b7098b5ea87690bef16c0e8ac0719e1c69b60507c3dcdac2bbb73d6
```

### `dpkg` source package: `gcc-defaults=1.214`

Binary Packages:

- `cpp=4:13.2.0-7`
- `cpp-x86-64-linux-gnu=4:13.2.0-7`
- `g++=4:13.2.0-7`
- `g++-x86-64-linux-gnu=4:13.2.0-7`
- `gcc=4:13.2.0-7`
- `gcc-x86-64-linux-gnu=4:13.2.0-7`
- `gfortran=4:13.2.0-7`
- `gfortran-x86-64-linux-gnu=4:13.2.0-7`

Licenses: (parsed from: `/usr/share/doc/cpp/copyright`, `/usr/share/doc/cpp-x86-64-linux-gnu/copyright`, `/usr/share/doc/g++/copyright`, `/usr/share/doc/g++-x86-64-linux-gnu/copyright`, `/usr/share/doc/gcc/copyright`, `/usr/share/doc/gcc-x86-64-linux-gnu/copyright`, `/usr/share/doc/gfortran/copyright`, `/usr/share/doc/gfortran-x86-64-linux-gnu/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris gcc-defaults=1.214
'http://http.debian.net/debian/pool/main/g/gcc-defaults/gcc-defaults_1.214.dsc' gcc-defaults_1.214.dsc 36725 SHA256:000e5785b15c3858843df98d8d35c84b6fad33fa62f85f1db3666af9c5cf2e1b
'http://http.debian.net/debian/pool/main/g/gcc-defaults/gcc-defaults_1.214.tar.xz' gcc-defaults_1.214.tar.xz 64612 SHA256:2719b26b8321c2ac33620cf857956ef1d10f4432ce7690df7270a77fce996e56
```

### `dpkg` source package: `gdbm=1.23-5`

Binary Packages:

- `libgdbm-compat4:amd64=1.23-5+b1`
- `libgdbm6:amd64=1.23-5+b1`

Licenses: (parsed from: `/usr/share/doc/libgdbm-compat4/copyright`, `/usr/share/doc/libgdbm6/copyright`)

- `GFDL-NIV-1.3+`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris gdbm=1.23-5
'http://http.debian.net/debian/pool/main/g/gdbm/gdbm_1.23-5.dsc' gdbm_1.23-5.dsc 2426 SHA256:dfa39e3786b411990987e5fb1d04e47ee118460a85eae2c0e38a894c2e388a11
'http://http.debian.net/debian/pool/main/g/gdbm/gdbm_1.23.orig.tar.gz' gdbm_1.23.orig.tar.gz 1115854 SHA256:74b1081d21fff13ae4bd7c16e5d6e504a4c26f7cde1dca0d963a484174bbcacd
'http://http.debian.net/debian/pool/main/g/gdbm/gdbm_1.23.orig.tar.gz.asc' gdbm_1.23.orig.tar.gz.asc 181 SHA256:64ebb68cc68e8915d62cb20ea40323c00b56051f844589ee0a52169fff34cecb
'http://http.debian.net/debian/pool/main/g/gdbm/gdbm_1.23-5.debian.tar.xz' gdbm_1.23-5.debian.tar.xz 18260 SHA256:f3942cab494a5b994f9d4073379928e5ef9394a80663b3f0b8de4dceb1041288
```

### `dpkg` source package: `glib2.0=2.78.3-2`

Binary Packages:

- `libglib2.0-0:amd64=2.78.3-2`

Licenses: (parsed from: `/usr/share/doc/libglib2.0-0/copyright`)

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
$ apt-get source -qq --print-uris glib2.0=2.78.3-2
'http://deb.debian.org/debian/pool/main/g/glib2.0/glib2.0_2.78.3-2.dsc' glib2.0_2.78.3-2.dsc 3551 SHA256:e29d0e77603b8cb4a7781646b490a9902467716d73d7983c4ddd6401d1f1ebcc
'http://deb.debian.org/debian/pool/main/g/glib2.0/glib2.0_2.78.3.orig-unicode-data.tar.xz' glib2.0_2.78.3.orig-unicode-data.tar.xz 266184 SHA256:7c3e36ec1356ac025a92169b74c4c3e6858345f59ed4ea4cf0db300dec4fa21a
'http://deb.debian.org/debian/pool/main/g/glib2.0/glib2.0_2.78.3.orig.tar.xz' glib2.0_2.78.3.orig.tar.xz 5321388 SHA256:609801dd373796e515972bf95fc0b2daa44545481ee2f465c4f204d224b2bc21
'http://deb.debian.org/debian/pool/main/g/glib2.0/glib2.0_2.78.3-2.debian.tar.xz' glib2.0_2.78.3-2.debian.tar.xz 120396 SHA256:da1ab2fae981d9e4132795f5ec527cc398983aa1a94251c48b3e98e536a39a07
```

Other potentially useful URLs:

- https://sources.debian.net/src/glib2.0/2.78.3-2/ (for browsing the source)
- https://sources.debian.net/src/glib2.0/2.78.3-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/glib2.0/2.78.3-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `glibc=2.37-15~deb13u1`

Binary Packages:

- `libc-bin=2.37-15~deb13u1`
- `libc-dev-bin=2.37-15~deb13u1`
- `libc-l10n=2.37-15~deb13u1`
- `libc6:amd64=2.37-15~deb13u1`
- `libc6-dev:amd64=2.37-15~deb13u1`
- `locales=2.37-15~deb13u1`

Licenses: (parsed from: `/usr/share/doc/libc-bin/copyright`, `/usr/share/doc/libc-dev-bin/copyright`, `/usr/share/doc/libc-l10n/copyright`, `/usr/share/doc/libc6/copyright`, `/usr/share/doc/libc6-dev/copyright`, `/usr/share/doc/locales/copyright`)

- `GPL-2`
- `LGPL-2.1`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/glibc/2.37-15~deb13u1/


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
'http://http.debian.net/debian/pool/main/g/gmp/gmp_6.3.0%2bdfsg-2.dsc' gmp_6.3.0+dfsg-2.dsc 2251 SHA256:31bf88a2899f7a6eb2dc0db438ba2b27f87562dfe73815a3bbc8b65675ba1a51
'http://http.debian.net/debian/pool/main/g/gmp/gmp_6.3.0%2bdfsg.orig.tar.xz' gmp_6.3.0+dfsg.orig.tar.xz 1870556 SHA256:bd2966e6d277f79328e894a5a9f3ba3fbf2ed2be81def5f48623e30c23fb1572
'http://http.debian.net/debian/pool/main/g/gmp/gmp_6.3.0%2bdfsg-2.debian.tar.xz' gmp_6.3.0+dfsg-2.debian.tar.xz 19156 SHA256:07fbc1f67c1c076575f8196f3b5a2d2be0268be10940ca59293d7f1669365f4e
```

### `dpkg` source package: `gnupg2=2.2.40-1.1`

Binary Packages:

- `gpgv=2.2.40-1.1+b1`

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
$ apt-get source -qq --print-uris gnupg2=2.2.40-1.1
'http://http.debian.net/debian/pool/main/g/gnupg2/gnupg2_2.2.40-1.1.dsc' gnupg2_2.2.40-1.1.dsc 3832 SHA256:89bdffd4176066d37fb5d250a1e5512c428529d10f13413a12893f86a757697f
'http://http.debian.net/debian/pool/main/g/gnupg2/gnupg2_2.2.40.orig.tar.bz2' gnupg2_2.2.40.orig.tar.bz2 7301631 SHA256:1164b29a75e8ab93ea15033300149e1872a7ef6bdda3d7c78229a735f8204c28
'http://http.debian.net/debian/pool/main/g/gnupg2/gnupg2_2.2.40.orig.tar.bz2.asc' gnupg2_2.2.40.orig.tar.bz2.asc 228 SHA256:3907dc165299cd53c0b4aec862323c3bce6037c411600ec87dc5eed7a55eba4a
'http://http.debian.net/debian/pool/main/g/gnupg2/gnupg2_2.2.40-1.1.debian.tar.xz' gnupg2_2.2.40-1.1.debian.tar.xz 62368 SHA256:356b7c86afdbaab286c5b92816cd1e1f4616cb67d22407c616618ef4d1680a9b
```

### `dpkg` source package: `gnutls28=3.8.3-1`

Binary Packages:

- `libgnutls30:amd64=3.8.3-1`

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
$ apt-get source -qq --print-uris gnutls28=3.8.3-1
'http://http.debian.net/debian/pool/main/g/gnutls28/gnutls28_3.8.3-1.dsc' gnutls28_3.8.3-1.dsc 3231 SHA256:5c7590150a65e94ff4ae515fde96cc0daebf7927bf8c5bb17e808f156d7a40f4
'http://http.debian.net/debian/pool/main/g/gnutls28/gnutls28_3.8.3.orig.tar.xz' gnutls28_3.8.3.orig.tar.xz 6463720 SHA256:f74fc5954b27d4ec6dfbb11dea987888b5b124289a3703afcada0ee520f4173e
'http://http.debian.net/debian/pool/main/g/gnutls28/gnutls28_3.8.3.orig.tar.xz.asc' gnutls28_3.8.3.orig.tar.xz.asc 854 SHA256:b2b90d225728890b0e2aa7c05e5f25f8ba1282821b46e72cd99f0c732b639cef
'http://http.debian.net/debian/pool/main/g/gnutls28/gnutls28_3.8.3-1.debian.tar.xz' gnutls28_3.8.3-1.debian.tar.xz 76476 SHA256:d92c5799fb4dacf29ae2cf4c00fabee51c0444e1cdc590d7c8adb383143bdd49
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
'http://http.debian.net/debian/pool/main/g/graphite2/graphite2_1.3.14-2.dsc' graphite2_1.3.14-2.dsc 2568 SHA256:98ee6be2e35e2a4f7dbc71a21315399d59c4f79339cb832c6caccf8f62342d26
'http://http.debian.net/debian/pool/main/g/graphite2/graphite2_1.3.14.orig.tar.gz' graphite2_1.3.14.orig.tar.gz 6629829 SHA256:7a3b342c5681921ce2e0c2496509d30b5b078399d5a7bd2358f95166d57d91df
'http://http.debian.net/debian/pool/main/g/graphite2/graphite2_1.3.14-2.debian.tar.xz' graphite2_1.3.14-2.debian.tar.xz 14168 SHA256:dc46cc532a54adfc7ed5798061795120325bf0722221b2a6299f49c403ee9cd4
```

### `dpkg` source package: `grep=3.11-4`

Binary Packages:

- `grep=3.11-4`

Licenses: (parsed from: `/usr/share/doc/grep/copyright`)

- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris grep=3.11-4
'http://http.debian.net/debian/pool/main/g/grep/grep_3.11-4.dsc' grep_3.11-4.dsc 1642 SHA256:dd6f8eb933bc05446e483f7792c8bf0a1aba9d498e65c6ccafe64e9bf27ac054
'http://http.debian.net/debian/pool/main/g/grep/grep_3.11.orig.tar.xz' grep_3.11.orig.tar.xz 1703776 SHA256:1db2aedde89d0dea42b16d9528f894c8d15dae4e190b59aecc78f5a951276eab
'http://http.debian.net/debian/pool/main/g/grep/grep_3.11.orig.tar.xz.asc' grep_3.11.orig.tar.xz.asc 833 SHA256:89ec23ffd59b68822732dc8204fc89883c3af30a90ae390feb94346d9d09a589
'http://http.debian.net/debian/pool/main/g/grep/grep_3.11-4.debian.tar.xz' grep_3.11-4.debian.tar.xz 20468 SHA256:f10394b7589c58ca7de4b580692b1b59431f898cb2068e86222c174e093fdf49
```

### `dpkg` source package: `gzip=1.12-1`

Binary Packages:

- `gzip=1.12-1`

Licenses: (parsed from: `/usr/share/doc/gzip/copyright`)

- `FSF-manpages`
- `GFDL-1.3+-no-invariant`
- `GFDL-3`
- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris gzip=1.12-1
'http://http.debian.net/debian/pool/main/g/gzip/gzip_1.12-1.dsc' gzip_1.12-1.dsc 2009 SHA256:49a287787a0b4fc816eb576c011c472d1f630ec1778dfa120bd7fce4a844c253
'http://http.debian.net/debian/pool/main/g/gzip/gzip_1.12.orig.tar.xz' gzip_1.12.orig.tar.xz 825548 SHA256:ce5e03e519f637e1f814011ace35c4f87b33c0bbabeec35baf5fbd3479e91956
'http://http.debian.net/debian/pool/main/g/gzip/gzip_1.12.orig.tar.xz.asc' gzip_1.12.orig.tar.xz.asc 833 SHA256:3ed9ab54452576e0be0d477c772c9f47baa36415133fef7dd1fcf7b15480ba32
'http://http.debian.net/debian/pool/main/g/gzip/gzip_1.12-1.debian.tar.xz' gzip_1.12-1.debian.tar.xz 18736 SHA256:fcf2317e8eeddd66766ec5f3853025b109bd13815ec86ed6563e1af68d17193a
```

### `dpkg` source package: `harfbuzz=8.3.0-2`

Binary Packages:

- `libharfbuzz0b:amd64=8.3.0-2`

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
$ apt-get source -qq --print-uris harfbuzz=8.3.0-2
'http://http.debian.net/debian/pool/main/h/harfbuzz/harfbuzz_8.3.0-2.dsc' harfbuzz_8.3.0-2.dsc 2892 SHA256:e4464683b4936fd977ee5b62c9a6786a9be4966d111dea6b9278922819816895
'http://http.debian.net/debian/pool/main/h/harfbuzz/harfbuzz_8.3.0.orig.tar.xz' harfbuzz_8.3.0.orig.tar.xz 19002808 SHA256:109501eaeb8bde3eadb25fab4164e993fbace29c3d775bcaa1c1e58e2f15f847
'http://http.debian.net/debian/pool/main/h/harfbuzz/harfbuzz_8.3.0-2.debian.tar.xz' harfbuzz_8.3.0-2.debian.tar.xz 19796 SHA256:36267a5c7d65ce26dee24491aa8d95af6afe860c9dc4f908d7d3a1d290f9a896
```

### `dpkg` source package: `hostname=3.23+nmu2`

Binary Packages:

- `hostname=3.23+nmu2`

Licenses: (parsed from: `/usr/share/doc/hostname/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris hostname=3.23+nmu2
'http://http.debian.net/debian/pool/main/h/hostname/hostname_3.23%2bnmu2.dsc' hostname_3.23+nmu2.dsc 1431 SHA256:03fe3dcdda4e3abc3a5d8d7ed6eb63558d9fa0dfe68412667eac73945b47e506
'http://http.debian.net/debian/pool/main/h/hostname/hostname_3.23%2bnmu2.tar.xz' hostname_3.23+nmu2.tar.xz 12944 SHA256:e94bc2323862e1b49635c2b638aa905f14aa91d9eb525be8e8811a773ca3a60d
```

### `dpkg` source package: `icu=72.1-4`

Binary Packages:

- `icu-devtools=72.1-4+b1`
- `libicu-dev:amd64=72.1-4+b1`
- `libicu72:amd64=72.1-4+b1`

Licenses: (parsed from: `/usr/share/doc/icu-devtools/copyright`, `/usr/share/doc/libicu-dev/copyright`, `/usr/share/doc/libicu72/copyright`)

- `GPL-3`
- `MIT`

Source:

```console
$ apt-get source -qq --print-uris icu=72.1-4
'http://http.debian.net/debian/pool/main/i/icu/icu_72.1-4.dsc' icu_72.1-4.dsc 2252 SHA256:a6c7b8575cf6743674635fde3dca6edc3a3236de07df9f5a19d27dedcda923c2
'http://http.debian.net/debian/pool/main/i/icu/icu_72.1.orig.tar.gz' icu_72.1.orig.tar.gz 26303933 SHA256:a2d2d38217092a7ed56635e34467f92f976b370e20182ad325edea6681a71d68
'http://http.debian.net/debian/pool/main/i/icu/icu_72.1.orig.tar.gz.asc' icu_72.1.orig.tar.gz.asc 659 SHA256:87b6ff610d587292cec0444fa8cbbfb12994cb89bade40578f5ba6470de245c7
'http://http.debian.net/debian/pool/main/i/icu/icu_72.1-4.debian.tar.xz' icu_72.1-4.debian.tar.xz 62456 SHA256:df53fade18c408471c169b1edb569769f3b58edb27db73bfc5bc3a6534f82676
```

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
'http://http.debian.net/debian/pool/main/i/init-system-helpers/init-system-helpers_1.66.dsc' init-system-helpers_1.66.dsc 2234 SHA256:a1e2276879abfe63174797c94969bc8591b8a05f2bad6ae3f27379b472877d6d
'http://http.debian.net/debian/pool/main/i/init-system-helpers/init-system-helpers_1.66.tar.xz' init-system-helpers_1.66.tar.xz 44976 SHA256:da058b5623a7d3f39aee1761b173478fdbbdfdf743fd66e876e56039c708ce53
```

### `dpkg` source package: `isl=0.26-3`

Binary Packages:

- `libisl23:amd64=0.26-3+b2`

Licenses: (parsed from: `/usr/share/doc/libisl23/copyright`)

- `BSD-2-clause`
- `LGPL-2`
- `LGPL-2.1+`
- `MIT`

Source:

```console
$ apt-get source -qq --print-uris isl=0.26-3
'http://http.debian.net/debian/pool/main/i/isl/isl_0.26-3.dsc' isl_0.26-3.dsc 1832 SHA256:b943ed41e0d04bd86ea1a9a10e49a0ac1996ac534b67b968df4320880ec6e6e7
'http://http.debian.net/debian/pool/main/i/isl/isl_0.26.orig.tar.xz' isl_0.26.orig.tar.xz 2035560 SHA256:a0b5cb06d24f9fa9e77b55fabbe9a3c94a336190345c2555f9915bb38e976504
'http://http.debian.net/debian/pool/main/i/isl/isl_0.26-3.debian.tar.xz' isl_0.26-3.debian.tar.xz 24700 SHA256:c4a9367d892a12da46c54cbf6475f447e137ac3eff857baa91af94c99daed0a5
```

### `dpkg` source package: `jansson=2.14-2`

Binary Packages:

- `libjansson4:amd64=2.14-2+b2`

Licenses: (parsed from: `/usr/share/doc/libjansson4/copyright`)

- `Expat`

Source:

```console
$ apt-get source -qq --print-uris jansson=2.14-2
'http://http.debian.net/debian/pool/main/j/jansson/jansson_2.14-2.dsc' jansson_2.14-2.dsc 1980 SHA256:6296ddd9c0a022bd1b70074aefb171cfcdf5694a04ffd32b35fd66097621af87
'http://http.debian.net/debian/pool/main/j/jansson/jansson_2.14.orig.tar.gz' jansson_2.14.orig.tar.gz 141500 SHA256:c739578bf6b764aa0752db9a2fdadcfe921c78f1228c7ec0bb47fa804c55d17b
'http://http.debian.net/debian/pool/main/j/jansson/jansson_2.14-2.debian.tar.xz' jansson_2.14-2.debian.tar.xz 5428 SHA256:e89fe4fd8221f6934ddb50f2e7f8404311928d0e23e49a5599f3d3d14ee8cb88
```

### `dpkg` source package: `jbigkit=2.1-6.1`

Binary Packages:

- `libjbig0:amd64=2.1-6.1+b1`

Licenses: (parsed from: `/usr/share/doc/libjbig0/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris jbigkit=2.1-6.1
'http://http.debian.net/debian/pool/main/j/jbigkit/jbigkit_2.1-6.1.dsc' jbigkit_2.1-6.1.dsc 2089 SHA256:8dea586c47cb4b2436f77fd33ef4a702b9da936d74de8332a72a8ddbe8124e09
'http://http.debian.net/debian/pool/main/j/jbigkit/jbigkit_2.1.orig.tar.gz' jbigkit_2.1.orig.tar.gz 438710 SHA256:de7106b6bfaf495d6865c7dd7ac6ca1381bd12e0d81405ea81e7f2167263d932
'http://http.debian.net/debian/pool/main/j/jbigkit/jbigkit_2.1-6.1.debian.tar.xz' jbigkit_2.1-6.1.debian.tar.xz 9244 SHA256:c9ba99e84d18b1affdc97b26b625721ed06b41a92996d9b426b62c0dbe3868cd
```

### `dpkg` source package: `kernsmooth=2.23-22-1`

Binary Packages:

- `r-cran-kernsmooth=2.23-22-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris kernsmooth=2.23-22-1
'http://http.debian.net/debian/pool/main/k/kernsmooth/kernsmooth_2.23-22-1.dsc' kernsmooth_2.23-22-1.dsc 1891 SHA256:c11f3b845695cd9df646afeb82796e2bbea1cf6b7846757df46d899731cb7708
'http://http.debian.net/debian/pool/main/k/kernsmooth/kernsmooth_2.23-22.orig.tar.gz' kernsmooth_2.23-22.orig.tar.gz 25996 SHA256:76e044904606cab79c9edf4eae3ad63ac9d91a2962b44e063075b4b40e8574e9
'http://http.debian.net/debian/pool/main/k/kernsmooth/kernsmooth_2.23-22-1.debian.tar.xz' kernsmooth_2.23-22-1.debian.tar.xz 3456 SHA256:025a39f51d6b9c9c06dfdca32d6f675f01d20756097b16e78ac3ae82d9e70400
```

### `dpkg` source package: `keyutils=1.6.3-3`

Binary Packages:

- `libkeyutils1:amd64=1.6.3-3`

Licenses: (parsed from: `/usr/share/doc/libkeyutils1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2`
- `LGPL-2+`

Source:

```console
$ apt-get source -qq --print-uris keyutils=1.6.3-3
'http://http.debian.net/debian/pool/main/k/keyutils/keyutils_1.6.3-3.dsc' keyutils_1.6.3-3.dsc 2079 SHA256:0a4178e10982c7351da7db5b44b5c18807613ad066cb2e157d0756019764f0c1
'http://http.debian.net/debian/pool/main/k/keyutils/keyutils_1.6.3.orig.tar.gz' keyutils_1.6.3.orig.tar.gz 137022 SHA256:a61d5706136ae4c05bd48f86186bcfdbd88dd8bd5107e3e195c924cfc1b39bb4
'http://http.debian.net/debian/pool/main/k/keyutils/keyutils_1.6.3-3.debian.tar.xz' keyutils_1.6.3-3.debian.tar.xz 13328 SHA256:8c078d9de91f930df174eebc60e063e8fff574ac36c0f7ee18f7e21635d60af0
```

### `dpkg` source package: `krb5=1.20.1-5`

Binary Packages:

- `libgssapi-krb5-2:amd64=1.20.1-5+b1`
- `libk5crypto3:amd64=1.20.1-5+b1`
- `libkrb5-3:amd64=1.20.1-5+b1`
- `libkrb5support0:amd64=1.20.1-5+b1`

Licenses: (parsed from: `/usr/share/doc/libgssapi-krb5-2/copyright`, `/usr/share/doc/libk5crypto3/copyright`, `/usr/share/doc/libkrb5-3/copyright`, `/usr/share/doc/libkrb5support0/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris krb5=1.20.1-5
'http://http.debian.net/debian/pool/main/k/krb5/krb5_1.20.1-5.dsc' krb5_1.20.1-5.dsc 3304 SHA256:014d2e50cd3fe911c1499bb203f63ddd3b9f306650451bfb1d8c33d7449a6b10
'http://http.debian.net/debian/pool/main/k/krb5/krb5_1.20.1.orig.tar.gz' krb5_1.20.1.orig.tar.gz 8661660 SHA256:704aed49b19eb5a7178b34b2873620ec299db08752d6a8574f95d41879ab8851
'http://http.debian.net/debian/pool/main/k/krb5/krb5_1.20.1.orig.tar.gz.asc' krb5_1.20.1.orig.tar.gz.asc 833 SHA256:2afeec5dbc586cc40b7975645e02b4c41c4d719dd02213e828c72d8239d55666
'http://http.debian.net/debian/pool/main/k/krb5/krb5_1.20.1-5.debian.tar.xz' krb5_1.20.1-5.debian.tar.xz 104484 SHA256:aba9f1047af6733679eeffd2ff9dae6ede5089f8f57e8b1117a9ac935b136105
```

### `dpkg` source package: `lapack=3.12.0-3`

Binary Packages:

- `libblas-dev:amd64=3.12.0-3`
- `libblas3:amd64=3.12.0-3`
- `liblapack-dev:amd64=3.12.0-3`
- `liblapack3:amd64=3.12.0-3`

Licenses: (parsed from: `/usr/share/doc/libblas-dev/copyright`, `/usr/share/doc/libblas3/copyright`, `/usr/share/doc/liblapack-dev/copyright`, `/usr/share/doc/liblapack3/copyright`)

- `BSD-3-clause`
- `BSD-3-clause-intel`

Source:

```console
$ apt-get source -qq --print-uris lapack=3.12.0-3
'http://http.debian.net/debian/pool/main/l/lapack/lapack_3.12.0-3.dsc' lapack_3.12.0-3.dsc 3307 SHA256:e00e9d07a748ee1e48e6c3d879459de13d172bd267b45894b7893d2b15d8ea34
'http://http.debian.net/debian/pool/main/l/lapack/lapack_3.12.0.orig.tar.gz' lapack_3.12.0.orig.tar.gz 7933607 SHA256:eac9570f8e0ad6f30ce4b963f4f033f0f643e7c3912fc9ee6cd99120675ad48b
'http://http.debian.net/debian/pool/main/l/lapack/lapack_3.12.0-3.debian.tar.xz' lapack_3.12.0-3.debian.tar.xz 28756 SHA256:ff6dacfcd3d8502b2fe53ae8296a00f322055cdfbdb5b2edc1b292d522dc936e
```

### `dpkg` source package: `lattice=0.22-5-1`

Binary Packages:

- `r-cran-lattice=0.22-5-1`

Licenses: (parsed from: `/usr/share/doc/r-cran-lattice/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris lattice=0.22-5-1
'http://http.debian.net/debian/pool/main/l/lattice/lattice_0.22-5-1.dsc' lattice_0.22-5-1.dsc 1838 SHA256:6082e7c096e2eeb45c928b46b4e388bbefb659b1b44c47f6d3b11456d11d48bb
'http://http.debian.net/debian/pool/main/l/lattice/lattice_0.22-5.orig.tar.gz' lattice_0.22-5.orig.tar.gz 599044 SHA256:ba1fbe5e18a133507dca9851b7f933002bdb6d1f3ea5f410a0a441103b6da5f1
'http://http.debian.net/debian/pool/main/l/lattice/lattice_0.22-5-1.debian.tar.xz' lattice_0.22-5-1.debian.tar.xz 5380 SHA256:73affdebdc7025c2d7f7cfb1ad96aedf4569239a7a10b8de9466a95fb420abf7
```

### `dpkg` source package: `lerc=4.0.0+ds-4`

Binary Packages:

- `liblerc4:amd64=4.0.0+ds-4+b1`

Licenses: (parsed from: `/usr/share/doc/liblerc4/copyright`)

- `Apache-2.0`

Source:

```console
$ apt-get source -qq --print-uris lerc=4.0.0+ds-4
'http://http.debian.net/debian/pool/main/l/lerc/lerc_4.0.0%2bds-4.dsc' lerc_4.0.0+ds-4.dsc 2638 SHA256:1f5758010599f9fd8b52ecea0541addeb0ea968f37d383a747abaa2a956f717e
'http://http.debian.net/debian/pool/main/l/lerc/lerc_4.0.0%2bds.orig.tar.xz' lerc_4.0.0+ds.orig.tar.xz 348140 SHA256:acf855502fd3b950ee78f0b67bc9e9b39316b3526fbf6d8b8b1a9482fb756723
'http://http.debian.net/debian/pool/main/l/lerc/lerc_4.0.0%2bds-4.debian.tar.xz' lerc_4.0.0+ds-4.debian.tar.xz 8280 SHA256:513db93f198180d601bba09356bd447c57d3a6360119e289cba897bf9054e5ac
```

### `dpkg` source package: `less=590-2`

Binary Packages:

- `less=590-2`

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
$ apt-get source -qq --print-uris less=590-2
'http://http.debian.net/debian/pool/main/l/less/less_590-2.dsc' less_590-2.dsc 1883 SHA256:7c17d83b042bd870fd7aae452f66390dcd04fd7ba6d812d682021b21f99e52a4
'http://http.debian.net/debian/pool/main/l/less/less_590.orig.tar.gz' less_590.orig.tar.gz 352574 SHA256:6aadf54be8bf57d0e2999a3c5d67b1de63808bb90deb8f77b028eafae3a08e10
'http://http.debian.net/debian/pool/main/l/less/less_590.orig.tar.gz.asc' less_590.orig.tar.gz.asc 163 SHA256:1bd54dbadb45eeaeaf58cee2b7b4a701c634c11866082bc494752838af37c3db
'http://http.debian.net/debian/pool/main/l/less/less_590-2.debian.tar.xz' less_590-2.debian.tar.xz 22112 SHA256:f4ba54057ca3db7ed412f56979c2fe3bb49ed26697ce35017be3f35b368eded7
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
'http://deb.debian.org/debian/pool/main/libb/libbsd/libbsd_0.11.8-1.dsc' libbsd_0.11.8-1.dsc 2347 SHA256:ca60717663ed359f4ec7a854976242a9c4307923e5c6f9eb87a06707e8b447ba
'http://deb.debian.org/debian/pool/main/libb/libbsd/libbsd_0.11.8.orig.tar.xz' libbsd_0.11.8.orig.tar.xz 432376 SHA256:55fdfa2696fb4d55a592fa9ad14a9df897c7b0008ddb3b30c419914841f85f33
'http://deb.debian.org/debian/pool/main/libb/libbsd/libbsd_0.11.8.orig.tar.xz.asc' libbsd_0.11.8.orig.tar.xz.asc 931 SHA256:938fcc5b81422c36aae2417c0aacbc3bb782ab8e5def916c5ae473ed2b45df6a
'http://deb.debian.org/debian/pool/main/libb/libbsd/libbsd_0.11.8-1.debian.tar.xz' libbsd_0.11.8-1.debian.tar.xz 18288 SHA256:6764507e51c10c135d98b66693fd17e0d41673ce0352340c4396788cf904a0a5
```

Other potentially useful URLs:

- https://sources.debian.net/src/libbsd/0.11.8-1/ (for browsing the source)
- https://sources.debian.net/src/libbsd/0.11.8-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libbsd/0.11.8-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libcap-ng=0.8.4-1`

Binary Packages:

- `libcap-ng0:amd64=0.8.4-1`

Licenses: (parsed from: `/usr/share/doc/libcap-ng0/copyright`)

- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `LGPL-2.1`
- `LGPL-2.1+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/libcap-ng/0.8.4-1/


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
'http://http.debian.net/debian/pool/main/libc/libcap2/libcap2_2.66-5.dsc' libcap2_2.66-5.dsc 2204 SHA256:7d8fd6db23376ad9ded85aebd5d5ed9cf133b1e561d3ac2b43fdf5b0b63739a8
'http://http.debian.net/debian/pool/main/libc/libcap2/libcap2_2.66.orig.tar.xz' libcap2_2.66.orig.tar.xz 181592 SHA256:15c40ededb3003d70a283fe587a36b7d19c8b3b554e33f86129c059a4bb466b2
'http://http.debian.net/debian/pool/main/libc/libcap2/libcap2_2.66-5.debian.tar.xz' libcap2_2.66-5.debian.tar.xz 21648 SHA256:fee7fdec4c806808b3e4c56e53ff5614b92186ecc6fd23a9e88694cdd938c452
```

### `dpkg` source package: `libdatrie=0.2.13-3`

Binary Packages:

- `libdatrie1:amd64=0.2.13-3`

Licenses: (parsed from: `/usr/share/doc/libdatrie1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris libdatrie=0.2.13-3
'http://http.debian.net/debian/pool/main/libd/libdatrie/libdatrie_0.2.13-3.dsc' libdatrie_0.2.13-3.dsc 2236 SHA256:6ddcaf319da01cc044f9b335b6b01b608a0380ccdaecb06bda71710b6f4395bb
'http://http.debian.net/debian/pool/main/libd/libdatrie/libdatrie_0.2.13.orig.tar.xz' libdatrie_0.2.13.orig.tar.xz 314072 SHA256:12231bb2be2581a7f0fb9904092d24b0ed2a271a16835071ed97bed65267f4be
'http://http.debian.net/debian/pool/main/libd/libdatrie/libdatrie_0.2.13-3.debian.tar.xz' libdatrie_0.2.13-3.debian.tar.xz 9668 SHA256:e656d536beb5db9e52ef92dd1fccd5480ebd21e4eddbfe013c51a1e2ec45cf38
```

### `dpkg` source package: `libdeflate=1.19-1`

Binary Packages:

- `libdeflate0:amd64=1.19-1`

Licenses: (parsed from: `/usr/share/doc/libdeflate0/copyright`)

- `Expat`

Source:

```console
$ apt-get source -qq --print-uris libdeflate=1.19-1
'http://http.debian.net/debian/pool/main/libd/libdeflate/libdeflate_1.19-1.dsc' libdeflate_1.19-1.dsc 2196 SHA256:a0fc083efcf9b54596a885928f780745146c01c7f644bddee0945334ba57a5e8
'http://http.debian.net/debian/pool/main/libd/libdeflate/libdeflate_1.19.orig.tar.gz' libdeflate_1.19.orig.tar.gz 187684 SHA256:27bf62d71cd64728ff43a9feb92f2ac2f2bf748986d856133cc1e51992428c25
'http://http.debian.net/debian/pool/main/libd/libdeflate/libdeflate_1.19-1.debian.tar.xz' libdeflate_1.19-1.debian.tar.xz 4796 SHA256:eaaa5ceac6fffc48b53997df8cfec3152e7fc922214667dfe82a669b81ef99b1
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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/libffi/3.4.4-2/


### `dpkg` source package: `libgcrypt20=1.10.3-2`

Binary Packages:

- `libgcrypt20:amd64=1.10.3-2`

Licenses: (parsed from: `/usr/share/doc/libgcrypt20/copyright`)

- `GPL-2`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris libgcrypt20=1.10.3-2
'http://http.debian.net/debian/pool/main/libg/libgcrypt20/libgcrypt20_1.10.3-2.dsc' libgcrypt20_1.10.3-2.dsc 2799 SHA256:9313ff9de25bc77383776d8fc0c2c1bd7ed9521a95a07aac74678e78fe3f8a5d
'http://http.debian.net/debian/pool/main/libg/libgcrypt20/libgcrypt20_1.10.3.orig.tar.bz2' libgcrypt20_1.10.3.orig.tar.bz2 3783827 SHA256:8b0870897ac5ac67ded568dcfadf45969cfa8a6beb0fd60af2a9eadc2a3272aa
'http://http.debian.net/debian/pool/main/libg/libgcrypt20/libgcrypt20_1.10.3.orig.tar.bz2.asc' libgcrypt20_1.10.3.orig.tar.bz2.asc 390 SHA256:f02a5f961b89c034a78decbb355ea5a8d9356df5a9636dec53ae548d7d814b14
'http://http.debian.net/debian/pool/main/libg/libgcrypt20/libgcrypt20_1.10.3-2.debian.tar.xz' libgcrypt20_1.10.3-2.debian.tar.xz 36496 SHA256:34121246430b7dbbe3ea7cdb77133653707cb2480eaf794c76000aee9a8abc55
```

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
'http://http.debian.net/debian/pool/main/libg/libgpg-error/libgpg-error_1.47-3.dsc' libgpg-error_1.47-3.dsc 2896 SHA256:350733b58bfa6f865597b41c51a16403aec5818fd70c35306c61decf62af7d15
'http://http.debian.net/debian/pool/main/libg/libgpg-error/libgpg-error_1.47.orig.tar.bz2' libgpg-error_1.47.orig.tar.bz2 1020862 SHA256:9e3c670966b96ecc746c28c2c419541e3bcb787d1a73930f5e5f5e1bcbbb9bdb
'http://http.debian.net/debian/pool/main/libg/libgpg-error/libgpg-error_1.47.orig.tar.bz2.asc' libgpg-error_1.47.orig.tar.bz2.asc 228 SHA256:6ab547bf020761e1df80b08335773a91c345ff2c1344f15b1f7d195293ab21a5
'http://http.debian.net/debian/pool/main/libg/libgpg-error/libgpg-error_1.47-3.debian.tar.xz' libgpg-error_1.47-3.debian.tar.xz 18572 SHA256:3ba56dba7e31bf3bd771a89474a7581217ede3732c2fba8aca8629e6c4d92232
```

### `dpkg` source package: `libice=2:1.0.10-1`

Binary Packages:

- `libice6:amd64=2:1.0.10-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libice=2:1.0.10-1
'http://http.debian.net/debian/pool/main/libi/libice/libice_1.0.10-1.dsc' libice_1.0.10-1.dsc 2049 SHA256:adb7b4e250db838a476a44b5a941c8f935ac2b20858186f09228cd3e0696034d
'http://http.debian.net/debian/pool/main/libi/libice/libice_1.0.10.orig.tar.gz' libice_1.0.10.orig.tar.gz 481960 SHA256:1116bc64c772fd127a0d0c0ffa2833479905e3d3d8197740b3abd5f292f22d2d
'http://http.debian.net/debian/pool/main/libi/libice/libice_1.0.10-1.diff.gz' libice_1.0.10-1.diff.gz 11349 SHA256:d186b3877416a7e80f1923fe2fc736d576e585a41450bcf4cd5e74f9dd099362
```

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
'http://http.debian.net/debian/pool/main/libi/libidn2/libidn2_2.3.7-2.dsc' libidn2_2.3.7-2.dsc 1963 SHA256:ba763f71c75847be4c68557a937484ff9e676c0af8be9a6796c914dab1363a5f
'http://http.debian.net/debian/pool/main/libi/libidn2/libidn2_2.3.7.orig.tar.gz' libidn2_2.3.7.orig.tar.gz 2155214 SHA256:4c21a791b610b9519b9d0e12b8097bf2f359b12f8dd92647611a929e6bfd7d64
'http://http.debian.net/debian/pool/main/libi/libidn2/libidn2_2.3.7.orig.tar.gz.asc' libidn2_2.3.7.orig.tar.gz.asc 228 SHA256:d4e78fc1c5a5c35980be3a04dd864574f450d55921360b0aa19326c75ada4a98
'http://http.debian.net/debian/pool/main/libi/libidn2/libidn2_2.3.7-2.debian.tar.xz' libidn2_2.3.7-2.debian.tar.xz 16276 SHA256:1f0ca3a2bb2c745056933cb41d212965b6571c9a436f83d33cba15e932d88d29
```

### `dpkg` source package: `libjpeg-turbo=1:2.1.5-2`

Binary Packages:

- `libjpeg-dev:amd64=1:2.1.5-2+b2`
- `libjpeg62-turbo:amd64=1:2.1.5-2+b2`
- `libjpeg62-turbo-dev:amd64=1:2.1.5-2+b2`

Licenses: (parsed from: `/usr/share/doc/libjpeg-dev/copyright`, `/usr/share/doc/libjpeg62-turbo/copyright`, `/usr/share/doc/libjpeg62-turbo-dev/copyright`)

- `BSD-3-clause`
- `BSD-BY-LC-NE`
- `Expat`
- `NTP`
- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris libjpeg-turbo=1:2.1.5-2
'http://http.debian.net/debian/pool/main/libj/libjpeg-turbo/libjpeg-turbo_2.1.5-2.dsc' libjpeg-turbo_2.1.5-2.dsc 2493 SHA256:d718ead0dfbcbc8523665c02a7f7152e31039ded641d022868722623bb3b486d
'http://http.debian.net/debian/pool/main/libj/libjpeg-turbo/libjpeg-turbo_2.1.5.orig.tar.gz' libjpeg-turbo_2.1.5.orig.tar.gz 2264471 SHA256:254f3642b04e309fee775123133c6464181addc150499561020312ec61c1bf7c
'http://http.debian.net/debian/pool/main/libj/libjpeg-turbo/libjpeg-turbo_2.1.5-2.debian.tar.xz' libjpeg-turbo_2.1.5-2.debian.tar.xz 107768 SHA256:cdb2433c2f7101345c1ffa14efb943787c675b86354691a32490845fe4bc9237
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
'http://http.debian.net/debian/pool/main/libm/libmd/libmd_1.1.0-2.dsc' libmd_1.1.0-2.dsc 2280 SHA256:46cc951cd6d71bbfeff4522de66f968fb92601ec4cc622b07f6ac0a2a36ac5f0
'http://http.debian.net/debian/pool/main/libm/libmd/libmd_1.1.0.orig.tar.xz' libmd_1.1.0.orig.tar.xz 271228 SHA256:1bd6aa42275313af3141c7cf2e5b964e8b1fd488025caf2f971f43b00776b332
'http://http.debian.net/debian/pool/main/libm/libmd/libmd_1.1.0.orig.tar.xz.asc' libmd_1.1.0.orig.tar.xz.asc 833 SHA256:402fd3024e43ab975733d09e661804a58ca58697194e4b15216b1217cfe1dadb
'http://http.debian.net/debian/pool/main/libm/libmd/libmd_1.1.0-2.debian.tar.xz' libmd_1.1.0-2.debian.tar.xz 8244 SHA256:3b6ff35fc921eb5450fa9bf2d300c9e058e3771f96f8f13f759768fadd53324c
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
'http://http.debian.net/debian/pool/main/libn/libnsl/libnsl_1.3.0-3.dsc' libnsl_1.3.0-3.dsc 1955 SHA256:32ef29339eb7aa7aa8a150d4c71592475fdefc0cc45509b517f470dbdd88b371
'http://http.debian.net/debian/pool/main/libn/libnsl/libnsl_1.3.0.orig.tar.xz' libnsl_1.3.0.orig.tar.xz 321488 SHA256:eac3062957fa302c62eff4aed718a07bacbf9ceb0a058289f12a19bfdda3c8e2
'http://http.debian.net/debian/pool/main/libn/libnsl/libnsl_1.3.0-3.debian.tar.xz' libnsl_1.3.0-3.debian.tar.xz 4748 SHA256:a9172c5b27236cae278effdbe74447bdb2536afea8ad4c2a44d9661e02ae2d89
```

### `dpkg` source package: `libpaper=1.1.29`

Binary Packages:

- `libpaper-utils=1.1.29`
- `libpaper1:amd64=1.1.29`

Licenses: (parsed from: `/usr/share/doc/libpaper-utils/copyright`, `/usr/share/doc/libpaper1/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris libpaper=1.1.29
'http://http.debian.net/debian/pool/main/libp/libpaper/libpaper_1.1.29.dsc' libpaper_1.1.29.dsc 1604 SHA256:940adde11d3bd19c3be7e3e16cdd737ca8fa52fac31e002d2530beea3e64cfc9
'http://http.debian.net/debian/pool/main/libp/libpaper/libpaper_1.1.29.tar.gz' libpaper_1.1.29.tar.gz 44942 SHA256:26330e21e9a3124658d515fd850b0cde546ff42d89b2596a5264c5f1677f0547
```

### `dpkg` source package: `libpng1.6=1.6.42-1`

Binary Packages:

- `libpng-dev:amd64=1.6.42-1`
- `libpng16-16:amd64=1.6.42-1`

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
$ apt-get source -qq --print-uris libpng1.6=1.6.42-1
'http://deb.debian.org/debian/pool/main/libp/libpng1.6/libpng1.6_1.6.42-1.dsc' libpng1.6_1.6.42-1.dsc 2241 SHA256:a5e76ea544620bd5a052e8fbba32ea48ef9c2df8513fa4f77578cf9ffd20b18d
'http://deb.debian.org/debian/pool/main/libp/libpng1.6/libpng1.6_1.6.42.orig.tar.gz' libpng1.6_1.6.42.orig.tar.gz 1542966 SHA256:fe89de292e223829859d21990d9c4d6b7e30e295a268f6a53a022611aa98bd67
'http://deb.debian.org/debian/pool/main/libp/libpng1.6/libpng1.6_1.6.42-1.debian.tar.xz' libpng1.6_1.6.42-1.debian.tar.xz 31232 SHA256:40503aba31d34c524d410ca8e5ab51752c6f27020a072b1572e0a519aff30821
```

Other potentially useful URLs:

- https://sources.debian.net/src/libpng1.6/1.6.42-1/ (for browsing the source)
- https://sources.debian.net/src/libpng1.6/1.6.42-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libpng1.6/1.6.42-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libpsl=0.21.2-1`

Binary Packages:

- `libpsl5:amd64=0.21.2-1+b1`

Licenses: (parsed from: `/usr/share/doc/libpsl5/copyright`)

- `Chromium`
- `MIT`
- `gnulib`

Source:

```console
$ apt-get source -qq --print-uris libpsl=0.21.2-1
'http://http.debian.net/debian/pool/main/libp/libpsl/libpsl_0.21.2-1.dsc' libpsl_0.21.2-1.dsc 1622 SHA256:1ddb578f5865a447b11078993cef2138107c82f8590ec2516af6f9970a2d4e0f
'http://http.debian.net/debian/pool/main/libp/libpsl/libpsl_0.21.2.orig.tar.xz' libpsl_0.21.2.orig.tar.xz 1870352 SHA256:11e34380f2c81d6e72c710464aae3b680df4ddcc1007826c630fb03c7ca6aa54
'http://http.debian.net/debian/pool/main/libp/libpsl/libpsl_0.21.2-1.debian.tar.xz' libpsl_0.21.2-1.debian.tar.xz 11940 SHA256:78327367c83ce2dc6a8404f479a7589eacb0266f1d4a25619d5f6f00f98ab7b6
```

### `dpkg` source package: `libseccomp=2.5.5-1`

Binary Packages:

- `libseccomp2:amd64=2.5.5-1`

Licenses: (parsed from: `/usr/share/doc/libseccomp2/copyright`)

- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libseccomp=2.5.5-1
'http://http.debian.net/debian/pool/main/libs/libseccomp/libseccomp_2.5.5-1.dsc' libseccomp_2.5.5-1.dsc 2708 SHA256:d8ea2fb22a4ed90001a34ace6e6a6f41fd1d9404de923182f2dde6037fec22e5
'http://http.debian.net/debian/pool/main/libs/libseccomp/libseccomp_2.5.5.orig.tar.gz' libseccomp_2.5.5.orig.tar.gz 642445 SHA256:248a2c8a4d9b9858aa6baf52712c34afefcf9c9e94b76dce02c1c9aa25fb3375
'http://http.debian.net/debian/pool/main/libs/libseccomp/libseccomp_2.5.5.orig.tar.gz.asc' libseccomp_2.5.5.orig.tar.gz.asc 833 SHA256:f3bf8a946020d3047581f11fe6ac71971a842115ddb362562b193861ef57d97b
'http://http.debian.net/debian/pool/main/libs/libseccomp/libseccomp_2.5.5-1.debian.tar.xz' libseccomp_2.5.5-1.debian.tar.xz 17608 SHA256:0e14e878a97657d8ff660f32477461abbd3ce366e5c24df4e4385c3e64cacaac
```

### `dpkg` source package: `libselinux=3.5-2`

Binary Packages:

- `libselinux1:amd64=3.5-2`

Licenses: (parsed from: `/usr/share/doc/libselinux1/copyright`)

- `GPL-2`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris libselinux=3.5-2
'http://http.debian.net/debian/pool/main/libs/libselinux/libselinux_3.5-2.dsc' libselinux_3.5-2.dsc 2662 SHA256:cd6baa8aebf37a88355291bf5cb11a311463479fed8a9f479043d1fc12de25cc
'http://http.debian.net/debian/pool/main/libs/libselinux/libselinux_3.5.orig.tar.gz' libselinux_3.5.orig.tar.gz 211453 SHA256:9a3a3705ac13a2ccca2de6d652b6356fead10f36fb33115c185c5ccdf29eec19
'http://http.debian.net/debian/pool/main/libs/libselinux/libselinux_3.5.orig.tar.gz.asc' libselinux_3.5.orig.tar.gz.asc 981 SHA256:fd37d441e0c08cabe9ac8f7815f52355bab2011549ec5792424fe18be9e1e015
'http://http.debian.net/debian/pool/main/libs/libselinux/libselinux_3.5-2.debian.tar.xz' libselinux_3.5-2.debian.tar.xz 35992 SHA256:e385f14d9700187495a82e433b02b139aebe89c8ceccab5a21598dfef518b0de
```

### `dpkg` source package: `libsemanage=3.5-1`

Binary Packages:

- `libsemanage-common=3.5-1`
- `libsemanage2:amd64=3.5-1+b2`

Licenses: (parsed from: `/usr/share/doc/libsemanage-common/copyright`, `/usr/share/doc/libsemanage2/copyright`)

- `GPL-2`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris libsemanage=3.5-1
'http://http.debian.net/debian/pool/main/libs/libsemanage/libsemanage_3.5-1.dsc' libsemanage_3.5-1.dsc 2644 SHA256:7415394f12030387ebca4ab7845830984b1ceb7ec3256d30a1733ba7f59d18c1
'http://http.debian.net/debian/pool/main/libs/libsemanage/libsemanage_3.5.orig.tar.gz' libsemanage_3.5.orig.tar.gz 185060 SHA256:f53534e50247538280ed0d76c6ce81d8fb3939bd64cadb89da10dba42e40dd9c
'http://http.debian.net/debian/pool/main/libs/libsemanage/libsemanage_3.5.orig.tar.gz.asc' libsemanage_3.5.orig.tar.gz.asc 981 SHA256:f9126c861c666f3308b60cea4405c5e686a056113ca3cbd0a5b0e4af7600c8f5
'http://http.debian.net/debian/pool/main/libs/libsemanage/libsemanage_3.5-1.debian.tar.xz' libsemanage_3.5-1.debian.tar.xz 29956 SHA256:78b11321d014bd52e1fb67c38db5ec6518b0b566b58c6e35a18e894dacc24aee
```

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
'http://http.debian.net/debian/pool/main/libs/libsepol/libsepol_3.5-2.dsc' libsepol_3.5-2.dsc 2005 SHA256:0f7b4750fbb8f34841c31784e8fbc1a94949a83adbcb7103f0ae061198bc55e7
'http://http.debian.net/debian/pool/main/libs/libsepol/libsepol_3.5.orig.tar.gz' libsepol_3.5.orig.tar.gz 497522 SHA256:78fdaf69924db780bac78546e43d9c44074bad798c2c415d0b9bb96d065ee8a2
'http://http.debian.net/debian/pool/main/libs/libsepol/libsepol_3.5.orig.tar.gz.asc' libsepol_3.5.orig.tar.gz.asc 981 SHA256:2309ab5e7cd38e2eb9196f92a60e00d4508cb293f1181d34a5a050128c9b7b24
'http://http.debian.net/debian/pool/main/libs/libsepol/libsepol_3.5-2.debian.tar.xz' libsepol_3.5-2.debian.tar.xz 27596 SHA256:05de2029893ec20cde7687178003fc5161d606259dad218ad46e7332db922695
```

### `dpkg` source package: `libsm=2:1.2.3-1`

Binary Packages:

- `libsm6:amd64=2:1.2.3-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libsm=2:1.2.3-1
'http://http.debian.net/debian/pool/main/libs/libsm/libsm_1.2.3-1.dsc' libsm_1.2.3-1.dsc 2063 SHA256:5488f8de81d53c32cbb5f062b6a6f262cd067283b8082041392dc60f0d04002c
'http://http.debian.net/debian/pool/main/libs/libsm/libsm_1.2.3.orig.tar.gz' libsm_1.2.3.orig.tar.gz 445362 SHA256:1e92408417cb6c6c477a8a6104291001a40b3bb56a4a60608fdd9cd2c5a0f320
'http://http.debian.net/debian/pool/main/libs/libsm/libsm_1.2.3-1.diff.gz' libsm_1.2.3-1.diff.gz 8929 SHA256:7eb99ab50b19f26d1470f89e4b46891f6a697cb1794a58ed0d1376cceaf1b6a9
```

### `dpkg` source package: `libssh2=1.11.0-4`

Binary Packages:

- `libssh2-1:amd64=1.11.0-4`

Licenses: (parsed from: `/usr/share/doc/libssh2-1/copyright`)

- `BSD3`

Source:

```console
$ apt-get source -qq --print-uris libssh2=1.11.0-4
'http://http.debian.net/debian/pool/main/libs/libssh2/libssh2_1.11.0-4.dsc' libssh2_1.11.0-4.dsc 2289 SHA256:4e470d039d3fe584247ba6fe55d6df1f61b7d5ca1f6a20e935f3429fc2260bee
'http://http.debian.net/debian/pool/main/libs/libssh2/libssh2_1.11.0.orig.tar.gz' libssh2_1.11.0.orig.tar.gz 1053562 SHA256:3736161e41e2693324deb38c26cfdc3efe6209d634ba4258db1cecff6a5ad461
'http://http.debian.net/debian/pool/main/libs/libssh2/libssh2_1.11.0.orig.tar.gz.asc' libssh2_1.11.0.orig.tar.gz.asc 488 SHA256:b6a32c85a3f9b6f30f2b3595ba034b48a8508ee9c94708ef811f58fd7adfcdee
'http://http.debian.net/debian/pool/main/libs/libssh2/libssh2_1.11.0-4.debian.tar.xz' libssh2_1.11.0-4.debian.tar.xz 13892 SHA256:490185b99efe121a516dd36867ced264babbe638568ddaf8cf6a6b5ed1afc01a
```

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
'http://http.debian.net/debian/pool/main/libt/libtasn1-6/libtasn1-6_4.19.0-3.dsc' libtasn1-6_4.19.0-3.dsc 2662 SHA256:7fd9618be5b99035c7387d969b73365a57b1f6f01ec4abe0af332829af718190
'http://http.debian.net/debian/pool/main/libt/libtasn1-6/libtasn1-6_4.19.0.orig.tar.gz' libtasn1-6_4.19.0.orig.tar.gz 1786576 SHA256:1613f0ac1cf484d6ec0ce3b8c06d56263cc7242f1c23b30d82d23de345a63f7a
'http://http.debian.net/debian/pool/main/libt/libtasn1-6/libtasn1-6_4.19.0.orig.tar.gz.asc' libtasn1-6_4.19.0.orig.tar.gz.asc 228 SHA256:8410c0c004f3509c218a98b276b3308b9c46f48068e8b1a6d9ebfd61ea9f357a
'http://http.debian.net/debian/pool/main/libt/libtasn1-6/libtasn1-6_4.19.0-3.debian.tar.xz' libtasn1-6_4.19.0-3.debian.tar.xz 22084 SHA256:acb32dc03d8c2aeb10e0fb1c2a0247efdab0a6dc5e8f8a4d3cdcfe5ad26bb0df
```

### `dpkg` source package: `libthai=0.1.29-2`

Binary Packages:

- `libthai-data=0.1.29-2`
- `libthai0:amd64=0.1.29-2`

Licenses: (parsed from: `/usr/share/doc/libthai-data/copyright`, `/usr/share/doc/libthai0/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris libthai=0.1.29-2
'http://http.debian.net/debian/pool/main/libt/libthai/libthai_0.1.29-2.dsc' libthai_0.1.29-2.dsc 2319 SHA256:564814dc31a466566cb50c077c5f6c5926a451594f52a0fc6b6367100445dddb
'http://http.debian.net/debian/pool/main/libt/libthai/libthai_0.1.29.orig.tar.xz' libthai_0.1.29.orig.tar.xz 417728 SHA256:fc80cc7dcb50e11302b417cebd24f2d30a8b987292e77e003267b9100d0f4bcd
'http://http.debian.net/debian/pool/main/libt/libthai/libthai_0.1.29-2.debian.tar.xz' libthai_0.1.29-2.debian.tar.xz 12644 SHA256:18a66bc2e766f475c206492612eabe3a206642bb69866236eb4a0a4126bf4f41
```

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
'http://http.debian.net/debian/pool/main/libt/libtirpc/libtirpc_1.3.4%2bds-1.dsc' libtirpc_1.3.4+ds-1.dsc 2129 SHA256:543919b82d61d1dfcdbf7baac1ca2f9c65fa5840fd16eca2975bd2e1b5c37998
'http://http.debian.net/debian/pool/main/libt/libtirpc/libtirpc_1.3.4%2bds.orig.tar.gz' libtirpc_1.3.4+ds.orig.tar.gz 700735 SHA256:730101dbb756b258164e496109bfdeee87eb0fcc05cd5a820e5f34537a1e637d
'http://http.debian.net/debian/pool/main/libt/libtirpc/libtirpc_1.3.4%2bds-1.debian.tar.xz' libtirpc_1.3.4+ds-1.debian.tar.xz 11436 SHA256:1072d8af8e50a795d7c85f8ad5879ce9596ff0faa37f99fde745d090dcafd0c3
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
'http://http.debian.net/debian/pool/main/libu/libunistring/libunistring_1.1-2.dsc' libunistring_1.1-2.dsc 2031 SHA256:2d8f1274fdc9b7434e9dcc4a0a6891e36aa015f43e4a0638ec4de6837873bd98
'http://http.debian.net/debian/pool/main/libu/libunistring/libunistring_1.1.orig.tar.xz' libunistring_1.1.orig.tar.xz 2397676 SHA256:827c1eb9cb6e7c738b171745dac0888aa58c5924df2e59239318383de0729b98
'http://http.debian.net/debian/pool/main/libu/libunistring/libunistring_1.1.orig.tar.xz.asc' libunistring_1.1.orig.tar.xz.asc 833 SHA256:dadae6c38f85f9e8776231436c601c386924ceb44d511456c61c9be73608933d
'http://http.debian.net/debian/pool/main/libu/libunistring/libunistring_1.1-2.debian.tar.xz' libunistring_1.1-2.debian.tar.xz 14008 SHA256:93dd1881e69e6046e2d2ec20ce99f2ae07e4ba078c506cd40104e19e08c681d1
```

### `dpkg` source package: `libwebp=1.3.2-0.3`

Binary Packages:

- `libsharpyuv0:amd64=1.3.2-0.3`
- `libwebp7:amd64=1.3.2-0.3`

Licenses: (parsed from: `/usr/share/doc/libsharpyuv0/copyright`, `/usr/share/doc/libwebp7/copyright`)

- `Apache-2.0`
- `BSD-3-Clause`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/libwebp/1.3.2-0.3/


### `dpkg` source package: `libx11=2:1.8.7-1`

Binary Packages:

- `libx11-6:amd64=2:1.8.7-1`
- `libx11-data=2:1.8.7-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libx11=2:1.8.7-1
'http://http.debian.net/debian/pool/main/libx/libx11/libx11_1.8.7-1.dsc' libx11_1.8.7-1.dsc 2480 SHA256:96eddec7e55ab344ce654c5043d59bc8da6470eb7849a578c843af965dda79d1
'http://http.debian.net/debian/pool/main/libx/libx11/libx11_1.8.7.orig.tar.gz' libx11_1.8.7.orig.tar.gz 3185363 SHA256:793ebebf569f12c864b77401798d38814b51790fce206e01a431e5feb982e20b
'http://http.debian.net/debian/pool/main/libx/libx11/libx11_1.8.7.orig.tar.gz.asc' libx11_1.8.7.orig.tar.gz.asc 833 SHA256:c1cba69555c89e503abac81ebf1113a756f2fafd72677e7862b40f12208e0260
'http://http.debian.net/debian/pool/main/libx/libx11/libx11_1.8.7-1.diff.gz' libx11_1.8.7-1.diff.gz 74344 SHA256:57adc62acb0ba21a4cf444aaf03ea4adc7f732215df22afa8b8d6fd31d799d95
```

### `dpkg` source package: `libxau=1:1.0.9-1`

Binary Packages:

- `libxau6:amd64=1:1.0.9-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxau=1:1.0.9-1
'http://http.debian.net/debian/pool/main/libx/libxau/libxau_1.0.9-1.dsc' libxau_1.0.9-1.dsc 2183 SHA256:e6e059652cda7e5a49b6c9a70667639f32d629c20320487d16c642a06c1ebf85
'http://http.debian.net/debian/pool/main/libx/libxau/libxau_1.0.9.orig.tar.gz' libxau_1.0.9.orig.tar.gz 394068 SHA256:1f123d8304b082ad63a9e89376400a3b1d4c29e67e3ea07b3f659cccca690eea
'http://http.debian.net/debian/pool/main/libx/libxau/libxau_1.0.9.orig.tar.gz.asc' libxau_1.0.9.orig.tar.gz.asc 801 SHA256:af6104aaf3c5ede529e381237dd60f49640ec96593a84502fa493b86582b2f04
'http://http.debian.net/debian/pool/main/libx/libxau/libxau_1.0.9-1.diff.gz' libxau_1.0.9-1.diff.gz 10193 SHA256:7b34899563f172e8f11d061de41b58fe1c32f8683d985e57686677ccb7299a9a
```

### `dpkg` source package: `libxcb=1.15-1`

Binary Packages:

- `libxcb-render0:amd64=1.15-1`
- `libxcb-shm0:amd64=1.15-1`
- `libxcb1:amd64=1.15-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxcb=1.15-1
'http://http.debian.net/debian/pool/main/libx/libxcb/libxcb_1.15-1.dsc' libxcb_1.15-1.dsc 5344 SHA256:f689569f33e70ca4c95c91b094d0659eb49a958d9ac43186640338f9290e298b
'http://http.debian.net/debian/pool/main/libx/libxcb/libxcb_1.15.orig.tar.gz' libxcb_1.15.orig.tar.gz 650774 SHA256:1cb65df8543a69ec0555ac696123ee386321dfac1964a3da39976c9a05ad724d
'http://http.debian.net/debian/pool/main/libx/libxcb/libxcb_1.15-1.diff.gz' libxcb_1.15-1.diff.gz 26267 SHA256:639c719ed06ffc397b200a209abd1a049e21e9e19431fb14c9ca870de01a6eac
```

### `dpkg` source package: `libxcrypt=1:4.4.36-4`

Binary Packages:

- `libcrypt-dev:amd64=1:4.4.36-4`
- `libcrypt1:amd64=1:4.4.36-4`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxcrypt=1:4.4.36-4
'http://http.debian.net/debian/pool/main/libx/libxcrypt/libxcrypt_4.4.36-4.dsc' libxcrypt_4.4.36-4.dsc 1563 SHA256:8509256bf6ddedebfaf14ad777541d225a6c956f590602f85f5639efc652bfef
'http://http.debian.net/debian/pool/main/libx/libxcrypt/libxcrypt_4.4.36.orig.tar.xz' libxcrypt_4.4.36.orig.tar.xz 392732 SHA256:7b7abbc89f13f5194211aa6861ed954e4fa3a210a4cb64f7e13dc8cf413e7f2a
'http://http.debian.net/debian/pool/main/libx/libxcrypt/libxcrypt_4.4.36-4.debian.tar.xz' libxcrypt_4.4.36-4.debian.tar.xz 8216 SHA256:e61d8a486e6a80a2e3d629296988f8ff2e4dfbef018ec7e94543b5918ca1f329
```

### `dpkg` source package: `libxdmcp=1:1.1.2-3`

Binary Packages:

- `libxdmcp6:amd64=1:1.1.2-3`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxdmcp=1:1.1.2-3
'http://http.debian.net/debian/pool/main/libx/libxdmcp/libxdmcp_1.1.2-3.dsc' libxdmcp_1.1.2-3.dsc 2145 SHA256:f9697dca6a275aeee9a3eee9fb2d55e0f77485481e8b84efc6950fc9b1988460
'http://http.debian.net/debian/pool/main/libx/libxdmcp/libxdmcp_1.1.2.orig.tar.gz' libxdmcp_1.1.2.orig.tar.gz 404115 SHA256:6f7c7e491a23035a26284d247779174dedc67e34e93cc3548b648ffdb6fc57c0
'http://http.debian.net/debian/pool/main/libx/libxdmcp/libxdmcp_1.1.2-3.diff.gz' libxdmcp_1.1.2-3.diff.gz 18017 SHA256:5844df115c17e5ba40ac116f80373304d821c607e763ef6f40562421f5cc0cf3
```

### `dpkg` source package: `libxext=2:1.3.4-1`

Binary Packages:

- `libxext6:amd64=2:1.3.4-1+b1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxext=2:1.3.4-1
'http://http.debian.net/debian/pool/main/libx/libxext/libxext_1.3.4-1.dsc' libxext_1.3.4-1.dsc 2118 SHA256:25024f57d955739c6b858822bf93ec3c71400b56fc0d666826f440e3661fd7c0
'http://http.debian.net/debian/pool/main/libx/libxext/libxext_1.3.4.orig.tar.gz' libxext_1.3.4.orig.tar.gz 494434 SHA256:8ef0789f282826661ff40a8eef22430378516ac580167da35cc948be9041aac1
'http://http.debian.net/debian/pool/main/libx/libxext/libxext_1.3.4-1.diff.gz' libxext_1.3.4-1.diff.gz 12509 SHA256:b975870d6a7b791ffbe2d57efdf6e20c250c5e76d12e45b04c8655f593bb8337
```

### `dpkg` source package: `libxmu=2:1.1.3-3`

Binary Packages:

- `libxmuu1:amd64=2:1.1.3-3`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxmu=2:1.1.3-3
'http://http.debian.net/debian/pool/main/libx/libxmu/libxmu_1.1.3-3.dsc' libxmu_1.1.3-3.dsc 2165 SHA256:d9dfadd0a6be92f88b1151c695e5799f889a39047176f80a91fcba24333cd063
'http://http.debian.net/debian/pool/main/libx/libxmu/libxmu_1.1.3.orig.tar.gz' libxmu_1.1.3.orig.tar.gz 497343 SHA256:5bd9d4ed1ceaac9ea023d86bf1c1632cd3b172dce4a193a72a94e1d9df87a62e
'http://http.debian.net/debian/pool/main/libx/libxmu/libxmu_1.1.3-3.diff.gz' libxmu_1.1.3-3.diff.gz 8085 SHA256:6f599ddd7951a1db5c1899fcd2a7c0289ae4ec9f9a783bc5e5b209b83c7ea12d
```

### `dpkg` source package: `libxrender=1:0.9.10-1.1`

Binary Packages:

- `libxrender1:amd64=1:0.9.10-1.1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxrender=1:0.9.10-1.1
'http://http.debian.net/debian/pool/main/libx/libxrender/libxrender_0.9.10-1.1.dsc' libxrender_0.9.10-1.1.dsc 2072 SHA256:348ab15d05f1d802da485e4c6abdb9d5419691fb7c8ce44ca5b17b2b7f889ce8
'http://http.debian.net/debian/pool/main/libx/libxrender/libxrender_0.9.10.orig.tar.gz' libxrender_0.9.10.orig.tar.gz 373717 SHA256:770527cce42500790433df84ec3521e8bf095dfe5079454a92236494ab296adf
'http://http.debian.net/debian/pool/main/libx/libxrender/libxrender_0.9.10-1.1.diff.gz' libxrender_0.9.10-1.1.diff.gz 15201 SHA256:caf8c84085b3b0d073f738fa12d32d4eca2d8b669cb3c7f1b1cd2ce64b7b10b7
```

### `dpkg` source package: `libxss=1:1.2.3-1`

Binary Packages:

- `libxss1:amd64=1:1.2.3-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxss=1:1.2.3-1
'http://http.debian.net/debian/pool/main/libx/libxss/libxss_1.2.3-1.dsc' libxss_1.2.3-1.dsc 2203 SHA256:783dbcd49a0934d994693af676ee98734dad070ab2434a6afe831c2de0ecca1d
'http://http.debian.net/debian/pool/main/libx/libxss/libxss_1.2.3.orig.tar.gz' libxss_1.2.3.orig.tar.gz 385215 SHA256:4f74e7e412144591d8e0616db27f433cfc9f45aae6669c6c4bb03e6bf9be809a
'http://http.debian.net/debian/pool/main/libx/libxss/libxss_1.2.3.orig.tar.gz.asc' libxss_1.2.3.orig.tar.gz.asc 705 SHA256:4e900524d56c8e7263365267efa91bb3671110c9eb28ccab58f70e2188f0b91b
'http://http.debian.net/debian/pool/main/libx/libxss/libxss_1.2.3-1.diff.gz' libxss_1.2.3-1.diff.gz 7145 SHA256:9d381b48f1377f27c506113e1f9b7d6ee286b856421f7f2b27017f01dccfef04
```

### `dpkg` source package: `libxt=1:1.2.1-1.1`

Binary Packages:

- `libxt6:amd64=1:1.2.1-1.1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxt=1:1.2.1-1.1
'http://http.debian.net/debian/pool/main/libx/libxt/libxt_1.2.1-1.1.dsc' libxt_1.2.1-1.1.dsc 2170 SHA256:62859ce41aa5914f32715fadb9dc60a54cc1ef3331b2122969ffbe31e5d53be7
'http://http.debian.net/debian/pool/main/libx/libxt/libxt_1.2.1.orig.tar.gz' libxt_1.2.1.orig.tar.gz 1024473 SHA256:6da1bfa9dd0ed87430a5ce95b129485086394df308998ebe34d98e378e3dfb33
'http://http.debian.net/debian/pool/main/libx/libxt/libxt_1.2.1.orig.tar.gz.asc' libxt_1.2.1.orig.tar.gz.asc 358 SHA256:da406cc94c25ca6773bb37c2055e2eb5665491f7ca6dfc9ea04f0f30ea3fd098
'http://http.debian.net/debian/pool/main/libx/libxt/libxt_1.2.1-1.1.diff.gz' libxt_1.2.1-1.1.diff.gz 45585 SHA256:ae7993031f3d77fcdbc2540f9d1b6b4a0afafddd747f1de444e4ffe2fa678fca
```

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
'http://http.debian.net/debian/pool/main/libz/libzstd/libzstd_1.5.5%2bdfsg2-2.dsc' libzstd_1.5.5+dfsg2-2.dsc 2375 SHA256:4e27ea0c5e2564dd6cc93d95fddc56ef85c5388ea4a4a60d8cca0b4c18c1da4f
'http://http.debian.net/debian/pool/main/libz/libzstd/libzstd_1.5.5%2bdfsg2.orig.tar.xz' libzstd_1.5.5+dfsg2.orig.tar.xz 1784164 SHA256:d7cf3c10d416fd999cb8fcf7685d9268ba7bec8eb78121fc2d0d916fa393d22b
'http://http.debian.net/debian/pool/main/libz/libzstd/libzstd_1.5.5%2bdfsg2-2.debian.tar.xz' libzstd_1.5.5+dfsg2-2.debian.tar.xz 21068 SHA256:0a72f44f83cbd2dce66722f5c7844aaf8e5937066a795ca6b3d2b0eba69b9e73
```

### `dpkg` source package: `linux=6.6.13-1`

Binary Packages:

- `linux-libc-dev=6.6.13-1`

Licenses: (parsed from: `/usr/share/doc/linux-libc-dev/copyright`)

- `BSD-2-clause`
- `CRYPTOGAMS`
- `GPL-2`
- `GPL-2+-or-X11`
- `LGPL-2.1`
- `Unicode-data`
- `Xen-interface`

Source:

```console
$ apt-get source -qq --print-uris linux=6.6.13-1
'http://http.debian.net/debian/pool/main/l/linux/linux_6.6.13-1.dsc' linux_6.6.13-1.dsc 231670 SHA256:390171fd4c1332be06cc440734e26091f63ee2651787ad4a8bd47c1b6474c68c
'http://http.debian.net/debian/pool/main/l/linux/linux_6.6.13.orig.tar.xz' linux_6.6.13.orig.tar.xz 142662888 SHA256:a057cf7ae0d9714a7ab003b4b1a8ba996080c2469856998b4eb68ec9cdaa74e6
'http://http.debian.net/debian/pool/main/l/linux/linux_6.6.13-1.debian.tar.xz' linux_6.6.13-1.debian.tar.xz 1567188 SHA256:4fbb86f9ade7c9b4dc25420d46fff3b81b4337e39c568931d51d2bf9302739ff
```

### `dpkg` source package: `littler=0.3.19-1`

Binary Packages:

- `littler=0.3.19-1`
- `r-cran-littler=0.3.19-1`

Licenses: (parsed from: `/usr/share/doc/littler/copyright`, `/usr/share/doc/r-cran-littler/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris littler=0.3.19-1
'http://http.debian.net/debian/pool/main/l/littler/littler_0.3.19-1.dsc' littler_0.3.19-1.dsc 1874 SHA256:121781a5a11a34f02f6a91c0ce7e549eb4ca21ee408eea41fd9b523b363170d9
'http://http.debian.net/debian/pool/main/l/littler/littler_0.3.19.orig.tar.gz' littler_0.3.19.orig.tar.gz 122659 SHA256:e1cfab5cc300c5ff7dd12c906afac2c8d87fec3fc43f07a8d0cf4a059ba36509
'http://http.debian.net/debian/pool/main/l/littler/littler_0.3.19-1.debian.tar.xz' littler_0.3.19-1.debian.tar.xz 7128 SHA256:493e6c9ff89c2d765158c3dfa458a5222121e97276adf9d4d14c60c17b9f5735
```

### `dpkg` source package: `lz4=1.9.4-1`

Binary Packages:

- `liblz4-1:amd64=1.9.4-1+b2`

Licenses: (parsed from: `/usr/share/doc/liblz4-1/copyright`)

- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris lz4=1.9.4-1
'http://http.debian.net/debian/pool/main/l/lz4/lz4_1.9.4-1.dsc' lz4_1.9.4-1.dsc 1951 SHA256:e16302bca544d08d106efc216541f4a0403c8f8a5fad5eaac7588223a55af263
'http://http.debian.net/debian/pool/main/l/lz4/lz4_1.9.4.orig.tar.gz' lz4_1.9.4.orig.tar.gz 354063 SHA256:0b0e3aa07c8c063ddf40b082bdf7e37a1562bda40a0ff5272957f3e987e0e54b
'http://http.debian.net/debian/pool/main/l/lz4/lz4_1.9.4-1.debian.tar.xz' lz4_1.9.4-1.debian.tar.xz 8128 SHA256:47ceec5b95f42598f7b9280b03df9659f2ee6852720ec181488e83bd643f0e5f
```

### `dpkg` source package: `make-dfsg=4.3-4.1`

Binary Packages:

- `make=4.3-4.1`

Licenses: (parsed from: `/usr/share/doc/make/copyright`)

- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris make-dfsg=4.3-4.1
'http://http.debian.net/debian/pool/main/m/make-dfsg/make-dfsg_4.3-4.1.dsc' make-dfsg_4.3-4.1.dsc 2019 SHA256:d2523d94f4d4198df6801f238d36cf0dea2ab5521f1d19ee76b2e8ee1f1918bb
'http://http.debian.net/debian/pool/main/m/make-dfsg/make-dfsg_4.3.orig.tar.gz' make-dfsg_4.3.orig.tar.gz 1845906 SHA256:be4c17542578824e745f83bcd2a9ba264206187247cb6a5f5df99b0a9d1f9047
'http://http.debian.net/debian/pool/main/m/make-dfsg/make-dfsg_4.3-4.1.diff.gz' make-dfsg_4.3-4.1.diff.gz 50940 SHA256:753c254ecaba425ebe2e0a0fb4d299847701e1c3eeb43df563e39975cae56b4c
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
'http://http.debian.net/debian/pool/main/m/mawk/mawk_1.3.4.20240123-1.dsc' mawk_1.3.4.20240123-1.dsc 2180 SHA256:fe68f6fc0a7f78718ec1b2c8140ddbf6f6d482ea537eaba805b7a9b3c7dd2f4e
'http://http.debian.net/debian/pool/main/m/mawk/mawk_1.3.4.20240123.orig.tar.gz' mawk_1.3.4.20240123.orig.tar.gz 413943 SHA256:a8e319a83744b1f1fb6988dfa189d61887f866e9140cc9a49eb003b2b0655e88
'http://http.debian.net/debian/pool/main/m/mawk/mawk_1.3.4.20240123.orig.tar.gz.asc' mawk_1.3.4.20240123.orig.tar.gz.asc 729 SHA256:3b688572de36ecbb8a013cda92e294038324ed2745485e883508e9a6fdbd2472
'http://http.debian.net/debian/pool/main/m/mawk/mawk_1.3.4.20240123-1.debian.tar.xz' mawk_1.3.4.20240123-1.debian.tar.xz 15600 SHA256:fe64a2ee58597035b727f33dc80f459353670b32887877f73932ab7b7c028eb7
```

### `dpkg` source package: `mgcv=1.9-1-1`

Binary Packages:

- `r-cran-mgcv=1.9-1-1`

Licenses: (parsed from: `/usr/share/doc/r-cran-mgcv/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris mgcv=1.9-1-1
'http://http.debian.net/debian/pool/main/m/mgcv/mgcv_1.9-1-1.dsc' mgcv_1.9-1-1.dsc 1826 SHA256:402384fa1204a1101155a3c265e71927396ebad3a97a57c817db7e24cf5b4b94
'http://http.debian.net/debian/pool/main/m/mgcv/mgcv_1.9-1.orig.tar.gz' mgcv_1.9-1.orig.tar.gz 1083217 SHA256:700fbc37bedd3a49505b9bc4949faee156d9cfb4f669d797d06a10a15a5bdb32
'http://http.debian.net/debian/pool/main/m/mgcv/mgcv_1.9-1-1.debian.tar.xz' mgcv_1.9-1-1.debian.tar.xz 5528 SHA256:cf18ffe6e93b47a69db0b2c8d577312230fbe4bd3ce2fb2a050f8efa86593076
```

### `dpkg` source package: `mpclib3=1.3.1-1`

Binary Packages:

- `libmpc3:amd64=1.3.1-1+b2`

Licenses: (parsed from: `/usr/share/doc/libmpc3/copyright`)

- `LGPL-3`

Source:

```console
$ apt-get source -qq --print-uris mpclib3=1.3.1-1
'http://http.debian.net/debian/pool/main/m/mpclib3/mpclib3_1.3.1-1.dsc' mpclib3_1.3.1-1.dsc 1877 SHA256:b2252a499fd0f8e92ce2cf7d8e68477ffc9dd06127803a91f0a1115822efec75
'http://http.debian.net/debian/pool/main/m/mpclib3/mpclib3_1.3.1.orig.tar.gz' mpclib3_1.3.1.orig.tar.gz 773573 SHA256:ab642492f5cf882b74aa0cb730cd410a81edcdbec895183ce930e706c1c759b8
'http://http.debian.net/debian/pool/main/m/mpclib3/mpclib3_1.3.1-1.debian.tar.xz' mpclib3_1.3.1-1.debian.tar.xz 4656 SHA256:25adb496258adacad69c022d712f96fbc465bcef9fd4751829dc351d9ce6a45d
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
'http://http.debian.net/debian/pool/main/m/mpfr4/mpfr4_4.2.1-1.dsc' mpfr4_4.2.1-1.dsc 1959 SHA256:2fb0ea6c37591f03c7f3445fc6a298a10dbd9d7662ccb441f7da0e514d71986a
'http://http.debian.net/debian/pool/main/m/mpfr4/mpfr4_4.2.1.orig.tar.xz' mpfr4_4.2.1.orig.tar.xz 1493608 SHA256:277807353a6726978996945af13e52829e3abd7a9a5b7fb2793894e18f1fcbb2
'http://http.debian.net/debian/pool/main/m/mpfr4/mpfr4_4.2.1-1.debian.tar.xz' mpfr4_4.2.1-1.debian.tar.xz 12556 SHA256:06c6c90efe3653d44527bcd6cfd66563d62409bbb348eb32f33b480e30ad9993
```

### `dpkg` source package: `ncurses=6.4+20240113-1`

Binary Packages:

- `libncurses-dev:amd64=6.4+20240113-1`
- `libncurses6:amd64=6.4+20240113-1`
- `libncursesw6:amd64=6.4+20240113-1`
- `libtinfo6:amd64=6.4+20240113-1`
- `ncurses-base=6.4+20240113-1`
- `ncurses-bin=6.4+20240113-1`

Licenses: (parsed from: `/usr/share/doc/libncurses-dev/copyright`, `/usr/share/doc/libncurses6/copyright`, `/usr/share/doc/libncursesw6/copyright`, `/usr/share/doc/libtinfo6/copyright`, `/usr/share/doc/ncurses-base/copyright`, `/usr/share/doc/ncurses-bin/copyright`)

- `BSD-3-clause`
- `MIT/X11`
- `X11`

Source:

```console
$ apt-get source -qq --print-uris ncurses=6.4+20240113-1
'http://http.debian.net/debian/pool/main/n/ncurses/ncurses_6.4%2b20240113-1.dsc' ncurses_6.4+20240113-1.dsc 3827 SHA256:87b1133381c084e9a46636b99d97c23369e7a1fbd9c099b74e7c85af9c51657a
'http://http.debian.net/debian/pool/main/n/ncurses/ncurses_6.4%2b20240113.orig.tar.gz' ncurses_6.4+20240113.orig.tar.gz 3688489 SHA256:37a12a0f8ae2605012c9a164dd286b0cfa02b51b5055836d09eb3d597fc351b1
'http://http.debian.net/debian/pool/main/n/ncurses/ncurses_6.4%2b20240113.orig.tar.gz.asc' ncurses_6.4+20240113.orig.tar.gz.asc 729 SHA256:b70cfa4f155f61dfa7c085ad1e3f90c73132ad198764d7793a44cd7fdca51f1b
'http://http.debian.net/debian/pool/main/n/ncurses/ncurses_6.4%2b20240113-1.debian.tar.xz' ncurses_6.4+20240113-1.debian.tar.xz 49152 SHA256:409131a064b802189af98d809ae745c2dc021623db900e6c46f7da1b519d5110
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
'http://http.debian.net/debian/pool/main/n/nettle/nettle_3.9.1-2.dsc' nettle_3.9.1-2.dsc 2274 SHA256:8ba0494afc18b086ef61d61c3b14a27f1c999ee89fbc55288b7a81eff395e521
'http://http.debian.net/debian/pool/main/n/nettle/nettle_3.9.1.orig.tar.gz' nettle_3.9.1.orig.tar.gz 2396741 SHA256:ccfeff981b0ca71bbd6fbcb054f407c60ffb644389a5be80d6716d5b550c6ce3
'http://http.debian.net/debian/pool/main/n/nettle/nettle_3.9.1.orig.tar.gz.asc' nettle_3.9.1.orig.tar.gz.asc 573 SHA256:9746017a1a7fe60aad4b929ea592bc6ac51e12ea7179f289944eb44828d958af
'http://http.debian.net/debian/pool/main/n/nettle/nettle_3.9.1-2.debian.tar.xz' nettle_3.9.1-2.debian.tar.xz 24440 SHA256:75e4612ae51801a674c1697bd189811606e81e72e7ac25ef6c056b7a2a9b2986
```

### `dpkg` source package: `nghttp2=1.59.0-1`

Binary Packages:

- `libnghttp2-14:amd64=1.59.0-1`

Licenses: (parsed from: `/usr/share/doc/libnghttp2-14/copyright`)

- `BSD-2-clause`
- `Expat`
- `GPL-3`
- `GPL-3+ with autoconf exception`
- `MIT`
- `all-permissive`

Source:

```console
$ apt-get source -qq --print-uris nghttp2=1.59.0-1
'http://http.debian.net/debian/pool/main/n/nghttp2/nghttp2_1.59.0-1.dsc' nghttp2_1.59.0-1.dsc 2534 SHA256:c7709f9df579a18e3612040b886a41ee91248d91f959d1d87a50fdd847ba614f
'http://http.debian.net/debian/pool/main/n/nghttp2/nghttp2_1.59.0.orig.tar.gz' nghttp2_1.59.0.orig.tar.gz 1055492 SHA256:0dd5c980f1262ff5f03676fd99f46f250b66c842f7d864fa1ca9f8453e5f8868
'http://http.debian.net/debian/pool/main/n/nghttp2/nghttp2_1.59.0-1.debian.tar.xz' nghttp2_1.59.0-1.debian.tar.xz 11772 SHA256:8672ac178e36e1449e1217a53d670fd162d482e9e96a215dac4df166dcc27072
```

### `dpkg` source package: `nlme=3.1.164-1`

Binary Packages:

- `r-cran-nlme=3.1.164-1`

Licenses: (parsed from: `/usr/share/doc/r-cran-nlme/copyright`)

- `GPL`
- `GPL `

Source:

```console
$ apt-get source -qq --print-uris nlme=3.1.164-1
'http://http.debian.net/debian/pool/main/n/nlme/nlme_3.1.164-1.dsc' nlme_3.1.164-1.dsc 1840 SHA256:6e140f5d3d3a2f92de29c303a65e0144c97f2cbc298d5615fbc7a8845f2f7743
'http://http.debian.net/debian/pool/main/n/nlme/nlme_3.1.164.orig.tar.gz' nlme_3.1.164.orig.tar.gz 836832 SHA256:79a5a020ce7037b83ee6c28336e35a1310058c13fc59f7fcb11eca0bc9bdd4e8
'http://http.debian.net/debian/pool/main/n/nlme/nlme_3.1.164-1.debian.tar.xz' nlme_3.1.164-1.debian.tar.xz 7328 SHA256:31701dc6c1f5578910cf342309eb7bac2c983527f38d3cab84a9318c3b87a3d7
```

### `dpkg` source package: `openblas=0.3.25+ds-2`

Binary Packages:

- `libopenblas0-pthread:amd64=0.3.25+ds-2`

Licenses: (parsed from: `/usr/share/doc/libopenblas0-pthread/copyright`)

- `Apache-2.0`
- `BSD-2-clause`
- `BSD-2-clause-texas`
- `BSD-3-clause`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/openblas/0.3.25+ds-2/


### `dpkg` source package: `openldap=2.5.13+dfsg-5`

Binary Packages:

- `libldap-2.5-0:amd64=2.5.13+dfsg-5+b3`

Licenses: (parsed from: `/usr/share/doc/libldap-2.5-0/copyright`)

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
$ apt-get source -qq --print-uris openldap=2.5.13+dfsg-5
'http://http.debian.net/debian/pool/main/o/openldap/openldap_2.5.13%2bdfsg-5.dsc' openldap_2.5.13+dfsg-5.dsc 3233 SHA256:3192f78a46825039c6c9de6808ae98ab3d1c8846f43d2109ed654fd9c33fe472
'http://http.debian.net/debian/pool/main/o/openldap/openldap_2.5.13%2bdfsg.orig.tar.xz' openldap_2.5.13+dfsg.orig.tar.xz 3727704 SHA256:1d95c400a3eae6730246614ef16883de3dbd1b14b01a1ebe3a9aa1ccad2c13ec
'http://http.debian.net/debian/pool/main/o/openldap/openldap_2.5.13%2bdfsg-5.debian.tar.xz' openldap_2.5.13+dfsg-5.debian.tar.xz 164516 SHA256:161e22c1c79e2f7c6013cfc2bbf0265d6bbb78d91a0fcfa9ca866837f2c31d88
```

### `dpkg` source package: `openssl=3.1.5-1`

Binary Packages:

- `libssl3:amd64=3.1.5-1`
- `openssl=3.1.5-1`

Licenses: (parsed from: `/usr/share/doc/libssl3/copyright`, `/usr/share/doc/openssl/copyright`)

- `Apache-2.0`
- `Artistic`
- `GPL-1`
- `GPL-1+`

Source:

```console
$ apt-get source -qq --print-uris openssl=3.1.5-1
'http://http.debian.net/debian/pool/main/o/openssl/openssl_3.1.5-1.dsc' openssl_3.1.5-1.dsc 2451 SHA256:57b8018f770cfa4d68efb6ba1be0d8849a722de329425e2f37e2eba68b947f34
'http://http.debian.net/debian/pool/main/o/openssl/openssl_3.1.5.orig.tar.gz' openssl_3.1.5.orig.tar.gz 15663524 SHA256:6ae015467dabf0469b139ada93319327be24b98251ffaeceda0221848dc09262
'http://http.debian.net/debian/pool/main/o/openssl/openssl_3.1.5.orig.tar.gz.asc' openssl_3.1.5.orig.tar.gz.asc 833 SHA256:817a9db4196f2aa7dcb2d0775afaf83ec0eb372c865664c157345a4b0d3bc85b
'http://http.debian.net/debian/pool/main/o/openssl/openssl_3.1.5-1.debian.tar.xz' openssl_3.1.5-1.debian.tar.xz 69824 SHA256:2583bb40965003bcb7f922e80956e7a8a62c98b40e7586f6c34742c8de3c91fa
```

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
'http://http.debian.net/debian/pool/main/p/p11-kit/p11-kit_0.25.3-4.dsc' p11-kit_0.25.3-4.dsc 2538 SHA256:51ad57264f721d05a23a8f7291fb0135d46c371e6cc85aa09eed1743876c5b32
'http://http.debian.net/debian/pool/main/p/p11-kit/p11-kit_0.25.3.orig.tar.xz' p11-kit_0.25.3.orig.tar.xz 991528 SHA256:d8ddce1bb7e898986f9d250ccae7c09ce14d82f1009046d202a0eb1b428b2adc
'http://http.debian.net/debian/pool/main/p/p11-kit/p11-kit_0.25.3.orig.tar.xz.asc' p11-kit_0.25.3.orig.tar.xz.asc 228 SHA256:91fb1fd7690b953eb32bf9ca52ae1b2466457539ac849468f1d236673b354860
'http://http.debian.net/debian/pool/main/p/p11-kit/p11-kit_0.25.3-4.debian.tar.xz' p11-kit_0.25.3-4.debian.tar.xz 25704 SHA256:7d1e652ad42be131e079755ca8fe23a8ac64b4c7153d6dc52ce68727b14499b2
```

### `dpkg` source package: `pam=1.5.2-9.1`

Binary Packages:

- `libpam-modules:amd64=1.5.2-9.1+b1`
- `libpam-modules-bin=1.5.2-9.1+b1`
- `libpam-runtime=1.5.2-9.1`
- `libpam0g:amd64=1.5.2-9.1+b1`

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
$ apt-get source -qq --print-uris pam=1.5.2-9.1
'http://http.debian.net/debian/pool/main/p/pam/pam_1.5.2-9.1.dsc' pam_1.5.2-9.1.dsc 2502 SHA256:d4b7fa6507e266e715b5d8474ef251d18478e5b69f494f41bbcc49122e4ca42b
'http://http.debian.net/debian/pool/main/p/pam/pam_1.5.2.orig.tar.xz' pam_1.5.2.orig.tar.xz 988784 SHA256:e4ec7131a91da44512574268f493c6d8ca105c87091691b8e9b56ca685d4f94d
'http://http.debian.net/debian/pool/main/p/pam/pam_1.5.2-9.1.debian.tar.xz' pam_1.5.2-9.1.debian.tar.xz 130160 SHA256:075dbb4cc5b9cd3260861e9e1f65db17f934ff5c02c574a9fdfe0cb334c2f1b5
```

### `dpkg` source package: `pango1.0=1.51.0+ds-4`

Binary Packages:

- `libpango-1.0-0:amd64=1.51.0+ds-4`
- `libpangocairo-1.0-0:amd64=1.51.0+ds-4`
- `libpangoft2-1.0-0:amd64=1.51.0+ds-4`

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
$ apt-get source -qq --print-uris pango1.0=1.51.0+ds-4
'http://deb.debian.org/debian/pool/main/p/pango1.0/pango1.0_1.51.0%2bds-4.dsc' pango1.0_1.51.0+ds-4.dsc 3654 SHA256:72d88f378dcd67daf16e803cb59b74cb67996e01a55a48c497ee6d061949a1af
'http://deb.debian.org/debian/pool/main/p/pango1.0/pango1.0_1.51.0%2bds.orig.tar.xz' pango1.0_1.51.0+ds.orig.tar.xz 1731104 SHA256:df51bb6819e91fda4f6c8ba8d2bd51e437e6f7daa86419d69a15e33a99002170
'http://deb.debian.org/debian/pool/main/p/pango1.0/pango1.0_1.51.0%2bds-4.debian.tar.xz' pango1.0_1.51.0+ds-4.debian.tar.xz 41724 SHA256:30e6a27c1a1f441934e712e34e68462b442f5134208a44505464b53be3bfc740
```

Other potentially useful URLs:

- https://sources.debian.net/src/pango1.0/1.51.0+ds-4/ (for browsing the source)
- https://sources.debian.net/src/pango1.0/1.51.0+ds-4/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/pango1.0/1.51.0+ds-4/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `patch=2.7.6-7`

Binary Packages:

- `patch=2.7.6-7`

Licenses: (parsed from: `/usr/share/doc/patch/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris patch=2.7.6-7
'http://http.debian.net/debian/pool/main/p/patch/patch_2.7.6-7.dsc' patch_2.7.6-7.dsc 1706 SHA256:d954fd576d935ac54b7d44d4976eb52d0da84a57f7bad90c6e5bd5e33595030a
'http://http.debian.net/debian/pool/main/p/patch/patch_2.7.6.orig.tar.xz' patch_2.7.6.orig.tar.xz 783756 SHA256:ac610bda97abe0d9f6b7c963255a11dcb196c25e337c61f94e4778d632f1d8fd
'http://http.debian.net/debian/pool/main/p/patch/patch_2.7.6-7.debian.tar.xz' patch_2.7.6-7.debian.tar.xz 15084 SHA256:7725f30b042d8cf63516e480036e93ca2ff0ce5ad3754db4a4e69d33e96a2624
```

### `dpkg` source package: `pcre2=10.42-4`

Binary Packages:

- `libpcre2-16-0:amd64=10.42-4`
- `libpcre2-32-0:amd64=10.42-4`
- `libpcre2-8-0:amd64=10.42-4`
- `libpcre2-dev:amd64=10.42-4`
- `libpcre2-posix3:amd64=10.42-4`

Licenses: (parsed from: `/usr/share/doc/libpcre2-16-0/copyright`, `/usr/share/doc/libpcre2-32-0/copyright`, `/usr/share/doc/libpcre2-8-0/copyright`, `/usr/share/doc/libpcre2-dev/copyright`, `/usr/share/doc/libpcre2-posix3/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `BSD-3-clause-Cambridge with BINARY LIBRARY-LIKE PACKAGES exception`
- `X11`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris pcre2=10.42-4
'http://http.debian.net/debian/pool/main/p/pcre2/pcre2_10.42-4.dsc' pcre2_10.42-4.dsc 2302 SHA256:2796d9332a4b4abe5eeada4aa287e8f9765a497b4363e3c49815a6bca5845cfe
'http://http.debian.net/debian/pool/main/p/pcre2/pcre2_10.42.orig.tar.gz' pcre2_10.42.orig.tar.gz 2397194 SHA256:c33b418e3b936ee3153de2c61cc638e7e4fe3156022a5c77d0711bcbb9d64f1f
'http://http.debian.net/debian/pool/main/p/pcre2/pcre2_10.42-4.diff.gz' pcre2_10.42-4.diff.gz 8111 SHA256:b583a75e90b029616c6867eccfeb21031e62df98dd4462f9d13ccb95bb2f09e6
```

### `dpkg` source package: `perl=5.38.2-3`

Binary Packages:

- `libperl5.38:amd64=5.38.2-3`
- `perl=5.38.2-3`
- `perl-base=5.38.2-3`
- `perl-modules-5.38=5.38.2-3`

Licenses: (parsed from: `/usr/share/doc/libperl5.38/copyright`, `/usr/share/doc/perl/copyright`, `/usr/share/doc/perl-base/copyright`, `/usr/share/doc/perl-modules-5.38/copyright`)

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
$ apt-get source -qq --print-uris perl=5.38.2-3
'http://http.debian.net/debian/pool/main/p/perl/perl_5.38.2-3.dsc' perl_5.38.2-3.dsc 2933 SHA256:f9bcf5b9f37840805afe2ed77ba928e3f2e01e3683160ced93d7643be8c056e7
'http://http.debian.net/debian/pool/main/p/perl/perl_5.38.2.orig-regen-configure.tar.xz' perl_5.38.2.orig-regen-configure.tar.xz 418808 SHA256:4d1b34cc058f9963cb89785ecc040d57f6d7725cd83329cfa4ef8b27566454d2
'http://http.debian.net/debian/pool/main/p/perl/perl_5.38.2.orig.tar.xz' perl_5.38.2.orig.tar.xz 13679524 SHA256:d91115e90b896520e83d4de6b52f8254ef2b70a8d545ffab33200ea9f1cf29e8
'http://http.debian.net/debian/pool/main/p/perl/perl_5.38.2-3.debian.tar.xz' perl_5.38.2-3.debian.tar.xz 165464 SHA256:39652e1185d219f1c8a7d436cf6457ec002ae9e1dfc4ad016b36176c10e5847b
```

### `dpkg` source package: `pixman=0.42.2-1`

Binary Packages:

- `libpixman-1-0:amd64=0.42.2-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris pixman=0.42.2-1
'http://http.debian.net/debian/pool/main/p/pixman/pixman_0.42.2-1.dsc' pixman_0.42.2-1.dsc 2021 SHA256:393302f5ba22d1206c456902baa02cdd577cb74fe35ec6659f587cce67b91b3d
'http://http.debian.net/debian/pool/main/p/pixman/pixman_0.42.2.orig.tar.gz' pixman_0.42.2.orig.tar.gz 959669 SHA256:ea1480efada2fd948bc75366f7c349e1c96d3297d09a3fe62626e38e234a625e
'http://http.debian.net/debian/pool/main/p/pixman/pixman_0.42.2-1.diff.gz' pixman_0.42.2-1.diff.gz 319616 SHA256:dd6472676c68260a298e52f45c485d3cc85c4bf25df8af0f68e37acff7bfed8a
```

### `dpkg` source package: `pkgconf=1.8.1-1`

Binary Packages:

- `libpkgconf3:amd64=1.8.1-1+b2`
- `pkg-config:amd64=1.8.1-1+b2`
- `pkgconf:amd64=1.8.1-1+b2`
- `pkgconf-bin=1.8.1-1+b2`

Licenses: (parsed from: `/usr/share/doc/libpkgconf3/copyright`, `/usr/share/doc/pkg-config/copyright`, `/usr/share/doc/pkgconf/copyright`, `/usr/share/doc/pkgconf-bin/copyright`)

- `BSD-2`
- `BSD-4`
- `GPL-2`
- `GPL-2+`
- `ISC`
- `X11`

Source:

```console
$ apt-get source -qq --print-uris pkgconf=1.8.1-1
'http://http.debian.net/debian/pool/main/p/pkgconf/pkgconf_1.8.1-1.dsc' pkgconf_1.8.1-1.dsc 1570 SHA256:cf1f645d7a9522354a334130a55d16be7d62e304070d6675f826844b143dc47e
'http://http.debian.net/debian/pool/main/p/pkgconf/pkgconf_1.8.1.orig.tar.xz' pkgconf_1.8.1.orig.tar.xz 302372 SHA256:644361ada2942be05655d4452eb018791647c31bba429b287f1f68deb2dc6840
'http://http.debian.net/debian/pool/main/p/pkgconf/pkgconf_1.8.1-1.debian.tar.xz' pkgconf_1.8.1-1.debian.tar.xz 15060 SHA256:bd9330105d17bf4b9a9d2aaba4a150b35da21b7ba4b45d4bf7e034fa6e53ba2f
```

### `dpkg` source package: `r-base=4.3.2-1`

Binary Packages:

- `r-base=4.3.2-1`
- `r-base-core=4.3.2-1`
- `r-base-dev=4.3.2-1`
- `r-recommended=4.3.2-1`

Licenses: (parsed from: `/usr/share/doc/r-base/copyright`, `/usr/share/doc/r-base-core/copyright`, `/usr/share/doc/r-base-dev/copyright`, `/usr/share/doc/r-recommended/copyright`)

- `Artistic`
- `GPL-2`
- `GPL-3`
- `LGPL-2`
- `LGPL-2.1`
- `LGPL-3`

Source:

```console
$ apt-get source -qq --print-uris r-base=4.3.2-1
'http://http.debian.net/debian/pool/main/r/r-base/r-base_4.3.2-1.dsc' r-base_4.3.2-1.dsc 2925 SHA256:b90549669bd665e7976dcfbffbbc978411b50b99051f5ed4fce63eccbb2e4d4f
'http://http.debian.net/debian/pool/main/r/r-base/r-base_4.3.2.orig.tar.gz' r-base_4.3.2.orig.tar.gz 35039225 SHA256:b3f5760ac2eee8026a3f0eefcb25b47723d978038eee8e844762094c860c452a
'http://http.debian.net/debian/pool/main/r/r-base/r-base_4.3.2-1.debian.tar.xz' r-base_4.3.2-1.debian.tar.xz 99608 SHA256:891b00c0ff57af727818bf738ac97ef6fb43aef096a9553583b61c50043ce692
```

### `dpkg` source package: `r-cran-class=7.3-22-2`

Binary Packages:

- `r-cran-class=7.3-22-2`

Licenses: (parsed from: `/usr/share/doc/r-cran-class/copyright`)

- `GPL-2`
- `GPL-2 | GPL-3`

Source:

```console
$ apt-get source -qq --print-uris r-cran-class=7.3-22-2
'http://http.debian.net/debian/pool/main/r/r-cran-class/r-cran-class_7.3-22-2.dsc' r-cran-class_7.3-22-2.dsc 1873 SHA256:f1b705a3b059c4315228192b468c007b1414f26834a5ef5ea985ac7f928afdc2
'http://http.debian.net/debian/pool/main/r/r-cran-class/r-cran-class_7.3-22.orig.tar.gz' r-cran-class_7.3-22.orig.tar.gz 20812 SHA256:b6994164e93843fcc7e08dfdc8c8b4af6a5a10ef7153d2e72a6855342508d15c
'http://http.debian.net/debian/pool/main/r/r-cran-class/r-cran-class_7.3-22-2.debian.tar.xz' r-cran-class_7.3-22-2.debian.tar.xz 3300 SHA256:1c13438d7b1645c7f4b027488d93b4362698de4805b8a75c121d7a5ca8579098
```

### `dpkg` source package: `r-cran-docopt=0.7.1-2`

Binary Packages:

- `r-cran-docopt=0.7.1-2`

Licenses: (parsed from: `/usr/share/doc/r-cran-docopt/copyright`)

- `MIT`

Source:

```console
$ apt-get source -qq --print-uris r-cran-docopt=0.7.1-2
'http://http.debian.net/debian/pool/main/r/r-cran-docopt/r-cran-docopt_0.7.1-2.dsc' r-cran-docopt_0.7.1-2.dsc 2087 SHA256:f7713b448b9b14766351e295d3ee0059f3a1c6319ecdf5ef33d5da40bc609d1b
'http://http.debian.net/debian/pool/main/r/r-cran-docopt/r-cran-docopt_0.7.1.orig.tar.gz' r-cran-docopt_0.7.1.orig.tar.gz 29465 SHA256:9f473887e4607e9b21fd4ab02e802858d0ac2ca6dad9e357a9d884a47fe4b0ff
'http://http.debian.net/debian/pool/main/r/r-cran-docopt/r-cran-docopt_0.7.1-2.debian.tar.xz' r-cran-docopt_0.7.1-2.debian.tar.xz 2472 SHA256:3358c9988254f326b3d2a351f3a75fd3c655d56de13e7f822cceaf39fb1f7fca
```

### `dpkg` source package: `r-cran-mass=7.3-60.0.1-1`

Binary Packages:

- `r-cran-mass=7.3-60.0.1-1`

Licenses: (parsed from: `/usr/share/doc/r-cran-mass/copyright`)

- `GPL-2`
- `GPL-2 | GPL-3`

Source:

```console
$ apt-get source -qq --print-uris r-cran-mass=7.3-60.0.1-1
'http://http.debian.net/debian/pool/main/r/r-cran-mass/r-cran-mass_7.3-60.0.1-1.dsc' r-cran-mass_7.3-60.0.1-1.dsc 1879 SHA256:81e8b7f2fbccedf0b6017245a81e41dcb05ca03f6e259956ee0239030fdd2491
'http://http.debian.net/debian/pool/main/r/r-cran-mass/r-cran-mass_7.3-60.0.1.orig.tar.gz' r-cran-mass_7.3-60.0.1.orig.tar.gz 561605 SHA256:74df93593029b803d78902c95eddcaa2e7e9ed186ab0be40b56f3f8bfd13adbd
'http://http.debian.net/debian/pool/main/r/r-cran-mass/r-cran-mass_7.3-60.0.1-1.debian.tar.xz' r-cran-mass_7.3-60.0.1-1.debian.tar.xz 6580 SHA256:5b23896d80190419d91ff58408a971b40878b2ec550dc7e7a46292c2ff93e957
```

### `dpkg` source package: `r-cran-nnet=7.3-19-2`

Binary Packages:

- `r-cran-nnet=7.3-19-2`

Licenses: (parsed from: `/usr/share/doc/r-cran-nnet/copyright`)

- `GPL-2`
- `GPL-2 | GPL-3`

Source:

```console
$ apt-get source -qq --print-uris r-cran-nnet=7.3-19-2
'http://http.debian.net/debian/pool/main/r/r-cran-nnet/r-cran-nnet_7.3-19-2.dsc' r-cran-nnet_7.3-19-2.dsc 1848 SHA256:02c98934d24d70696c760e0e4fa8fae998a6ea275eb039ab140ef30d564523a3
'http://http.debian.net/debian/pool/main/r/r-cran-nnet/r-cran-nnet_7.3-19.orig.tar.gz' r-cran-nnet_7.3-19.orig.tar.gz 29152 SHA256:a9241f469270d3b03bbab7dc0d3c6a06a84010af16ba82fd3bd6660b35382ce7
'http://http.debian.net/debian/pool/main/r/r-cran-nnet/r-cran-nnet_7.3-19-2.debian.tar.xz' r-cran-nnet_7.3-19-2.debian.tar.xz 3332 SHA256:49aaccdda8d36b3f195ba69de26066b2e1245803a9ab4dafa536589fa85977b7
```

### `dpkg` source package: `r-cran-spatial=7.3-17-1`

Binary Packages:

- `r-cran-spatial=7.3-17-1`

Licenses: (parsed from: `/usr/share/doc/r-cran-spatial/copyright`)

- `GPL-2`
- `GPL-2 | GPL-3`

Source:

```console
$ apt-get source -qq --print-uris r-cran-spatial=7.3-17-1
'http://http.debian.net/debian/pool/main/r/r-cran-spatial/r-cran-spatial_7.3-17-1.dsc' r-cran-spatial_7.3-17-1.dsc 1884 SHA256:2b53f753efcdc641ef16e58e1bed93ee4a9d7bf52864e95359422d6c5ad4b5c0
'http://http.debian.net/debian/pool/main/r/r-cran-spatial/r-cran-spatial_7.3-17.orig.tar.gz' r-cran-spatial_7.3-17.orig.tar.gz 44661 SHA256:f1003ed8cff2a47169a4787c8be46e8c2c501cc06c8b1e5f97bf62507e5f5dd7
'http://http.debian.net/debian/pool/main/r/r-cran-spatial/r-cran-spatial_7.3-17-1.debian.tar.xz' r-cran-spatial_7.3-17-1.debian.tar.xz 3224 SHA256:1299d2624d2cd604237e97116659b15f60eb6bb6179c5265cee1b89a6b708fe8
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
'http://http.debian.net/debian/pool/main/r/readline/readline_8.2-3.dsc' readline_8.2-3.dsc 2783 SHA256:9a3f265e7bf77fd241f5b3cb5f10e9564b73c4422d18402a1fd36d4dbd34ac76
'http://http.debian.net/debian/pool/main/r/readline/readline_8.2.orig.tar.gz' readline_8.2.orig.tar.gz 3043952 SHA256:3feb7171f16a84ee82ca18a36d7b9be109a52c04f492a053331d7d1095007c35
'http://http.debian.net/debian/pool/main/r/readline/readline_8.2-3.debian.tar.xz' readline_8.2-3.debian.tar.xz 33220 SHA256:f1211d371626f139b2eb87a431cc9f58a09dca3391f3245bffe7ccdf95d72f28
```

### `dpkg` source package: `rmatrix=1.6-5-1`

Binary Packages:

- `r-cran-matrix=1.6-5-1`

Licenses: (parsed from: `/usr/share/doc/r-cran-matrix/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris rmatrix=1.6-5-1
'http://http.debian.net/debian/pool/main/r/rmatrix/rmatrix_1.6-5-1.dsc' rmatrix_1.6-5-1.dsc 1860 SHA256:efda0dde8bb6c35803ab73cd4f5dcdd7182c06b1596a9857987db304d2961690
'http://http.debian.net/debian/pool/main/r/rmatrix/rmatrix_1.6-5.orig.tar.gz' rmatrix_1.6-5.orig.tar.gz 2883851 SHA256:726c8d46626e73d1d6e76a74679813c6df96ffdee1aee45d94e7014cb4ceb97d
'http://http.debian.net/debian/pool/main/r/rmatrix/rmatrix_1.6-5-1.debian.tar.xz' rmatrix_1.6-5-1.debian.tar.xz 5928 SHA256:09cbdabaf4c04d382e5b48998edf7bc3c41b9a88ea2df548f76621453d4c82a4
```

### `dpkg` source package: `rpart=4.1.23-1`

Binary Packages:

- `r-cran-rpart=4.1.23-1`

Licenses: (parsed from: `/usr/share/doc/r-cran-rpart/copyright`)

- `GPL-2`
- `GPL-2+ | license included below`

Source:

```console
$ apt-get source -qq --print-uris rpart=4.1.23-1
'http://http.debian.net/debian/pool/main/r/rpart/rpart_4.1.23-1.dsc' rpart_4.1.23-1.dsc 1843 SHA256:84bfc4124dbebd5c3f22a7789ce61cb85d78bef62d8aa617e9438948996b0ac2
'http://http.debian.net/debian/pool/main/r/rpart/rpart_4.1.23.orig.tar.gz' rpart_4.1.23.orig.tar.gz 618016 SHA256:f9b89aed6aa6cea656a2dcb271574e969ce2b1c98beb07bd91e17339f6daabaf
'http://http.debian.net/debian/pool/main/r/rpart/rpart_4.1.23-1.debian.tar.xz' rpart_4.1.23-1.debian.tar.xz 4424 SHA256:5cb2cd24d3faede047e4637de541ddf5dc350ad1309ba0cc3c8e974328ee34f3
```

### `dpkg` source package: `rpcsvc-proto=1.4.3-1`

Binary Packages:

- `rpcsvc-proto=1.4.3-1`

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
$ apt-get source -qq --print-uris rpcsvc-proto=1.4.3-1
'http://http.debian.net/debian/pool/main/r/rpcsvc-proto/rpcsvc-proto_1.4.3-1.dsc' rpcsvc-proto_1.4.3-1.dsc 1999 SHA256:7d8e122bd18b02fe0de6d467a0ecdafff74035b3e1ed0da1c0c792d9c015682f
'http://http.debian.net/debian/pool/main/r/rpcsvc-proto/rpcsvc-proto_1.4.3.orig.tar.xz' rpcsvc-proto_1.4.3.orig.tar.xz 167964 SHA256:69315e94430f4e79c74d43422f4a36e6259e97e67e2677b2c7d7060436bd99b1
'http://http.debian.net/debian/pool/main/r/rpcsvc-proto/rpcsvc-proto_1.4.3-1.debian.tar.xz' rpcsvc-proto_1.4.3-1.debian.tar.xz 4228 SHA256:02034b9dadcf3af5424f72eb65c3842c8d7117b6b78e7a3c798316ceb60843d1
```

### `dpkg` source package: `rtmpdump=2.4+20151223.gitfa8646d.1-2`

Binary Packages:

- `librtmp1:amd64=2.4+20151223.gitfa8646d.1-2+b2`

Licenses: (parsed from: `/usr/share/doc/librtmp1/copyright`)

- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris rtmpdump=2.4+20151223.gitfa8646d.1-2
'http://http.debian.net/debian/pool/main/r/rtmpdump/rtmpdump_2.4%2b20151223.gitfa8646d.1-2.dsc' rtmpdump_2.4+20151223.gitfa8646d.1-2.dsc 2299 SHA256:a296819cd2ab5880b67ad963ef0867cb10e462f4403e52565aa863eb05bb1370
'http://http.debian.net/debian/pool/main/r/rtmpdump/rtmpdump_2.4%2b20151223.gitfa8646d.1.orig.tar.gz' rtmpdump_2.4+20151223.gitfa8646d.1.orig.tar.gz 142213 SHA256:5c032f5c8cc2937eb55a81a94effdfed3b0a0304b6376147b86f951e225e3ab5
'http://http.debian.net/debian/pool/main/r/rtmpdump/rtmpdump_2.4%2b20151223.gitfa8646d.1-2.debian.tar.xz' rtmpdump_2.4+20151223.gitfa8646d.1-2.debian.tar.xz 8096 SHA256:26d47de07d16285e4ca55b0828cbbf1ba35e671f9b3500a87e301fe755d26882
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
'http://http.debian.net/debian/pool/main/s/sed/sed_4.9-2.dsc' sed_4.9-2.dsc 1860 SHA256:17f10deac1b327cb2a623352cdc33444ac9c109359a0caa46b3980b0e415f671
'http://http.debian.net/debian/pool/main/s/sed/sed_4.9.orig.tar.xz' sed_4.9.orig.tar.xz 1397092 SHA256:6e226b732e1cd739464ad6862bd1a1aba42d7982922da7a53519631d24975181
'http://http.debian.net/debian/pool/main/s/sed/sed_4.9-2.debian.tar.xz' sed_4.9-2.debian.tar.xz 62756 SHA256:549fa5cec6eb4fde8cc74ca263b8bf42f947ede677e39d2afeedf661da1d4e52
```

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

Source:

```console
$ apt-get source -qq --print-uris sensible-utils=0.0.22
'http://http.debian.net/debian/pool/main/s/sensible-utils/sensible-utils_0.0.22.dsc' sensible-utils_0.0.22.dsc 1737 SHA256:2a49b3be4b85b3f455f9c15c26f9bfb6c508496025a414f32649b16fe6326773
'http://http.debian.net/debian/pool/main/s/sensible-utils/sensible-utils_0.0.22.tar.xz' sensible-utils_0.0.22.tar.xz 74412 SHA256:c744d604ad6e1f3c8b4831cd84d653cf86bf9867a856724bf3f4fceb2de215b5
```

### `dpkg` source package: `shadow=1:4.13+dfsg1-3`

Binary Packages:

- `login=1:4.13+dfsg1-3+b1`
- `passwd=1:4.13+dfsg1-3+b1`

Licenses: (parsed from: `/usr/share/doc/login/copyright`, `/usr/share/doc/passwd/copyright`)

- `BSD-3-clause`
- `GPL-1`
- `GPL-2`
- `GPL-2+`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/shadow/1:4.13+dfsg1-3/


### `dpkg` source package: `survival=3.5-7-1`

Binary Packages:

- `r-cran-survival=3.5-7-1`

Licenses: (parsed from: `/usr/share/doc/r-cran-survival/copyright`)

- `GPL-2`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/survival/3.5-7-1/


### `dpkg` source package: `systemd=255.3-2`

Binary Packages:

- `libsystemd0:amd64=255.3-2`
- `libudev1:amd64=255.3-2`

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
$ apt-get source -qq --print-uris systemd=255.3-2
'http://deb.debian.org/debian/pool/main/s/systemd/systemd_255.3-2.dsc' systemd_255.3-2.dsc 7045 SHA256:4b8806cb37214c9006e1f74bc16b5d1969b9296c59713de23247084566ccdbda
'http://deb.debian.org/debian/pool/main/s/systemd/systemd_255.3.orig.tar.gz' systemd_255.3.orig.tar.gz 14873273 SHA256:27807c65f969d0e0e44629dee8379e1e2c30e6c5e84be0389438c4ab1b225000
'http://deb.debian.org/debian/pool/main/s/systemd/systemd_255.3-2.debian.tar.xz' systemd_255.3-2.debian.tar.xz 174204 SHA256:1d1af57206309837dc65b4a233ffa14cc7c7ceefbe8b4c4a224b9bc05872a5e7
```

Other potentially useful URLs:

- https://sources.debian.net/src/systemd/255.3-2/ (for browsing the source)
- https://sources.debian.net/src/systemd/255.3-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/systemd/255.3-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `sysvinit=3.08-6`

Binary Packages:

- `sysvinit-utils=3.08-6`

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
$ apt-get source -qq --print-uris sysvinit=3.08-6
'http://http.debian.net/debian/pool/main/s/sysvinit/sysvinit_3.08-6.dsc' sysvinit_3.08-6.dsc 2359 SHA256:7bb250f3b216f67e213c3659958fe6115d6c6d7956950b12ea69117c8bf01151
'http://http.debian.net/debian/pool/main/s/sysvinit/sysvinit_3.08.orig.tar.gz' sysvinit_3.08.orig.tar.gz 513674 SHA256:325e42ae4ae5ae3e4d989e0604aeb5e4eae5f3ee21e401db3c79000718f8c836
'http://http.debian.net/debian/pool/main/s/sysvinit/sysvinit_3.08-6.debian.tar.xz' sysvinit_3.08-6.debian.tar.xz 138768 SHA256:dcf037d93671e1c9f70df6941fc735fc22b004be327087c121069eb5c1794e5c
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
'http://http.debian.net/debian/pool/main/t/tar/tar_1.35%2bdfsg-3.dsc' tar_1.35+dfsg-3.dsc 2009 SHA256:0ea713a8af04a41d297202e7ac20813735328a5f8d4de3882fba5595709955f8
'http://http.debian.net/debian/pool/main/t/tar/tar_1.35%2bdfsg.orig.tar.xz' tar_1.35+dfsg.orig.tar.xz 2111608 SHA256:9ae57e981c1e73c0eebc2b26c9b0c4497fe310ef1d516ea430efb5470b71f7a8
'http://http.debian.net/debian/pool/main/t/tar/tar_1.35%2bdfsg-3.debian.tar.xz' tar_1.35+dfsg-3.debian.tar.xz 20824 SHA256:6028f2172de2498b8fc2baef4854796d829ae7ba2a91de4f7615fe1a56729313
```

### `dpkg` source package: `tcl8.6=8.6.13+dfsg-2`

Binary Packages:

- `libtcl8.6:amd64=8.6.13+dfsg-2+b1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris tcl8.6=8.6.13+dfsg-2
'http://http.debian.net/debian/pool/main/t/tcl8.6/tcl8.6_8.6.13%2bdfsg-2.dsc' tcl8.6_8.6.13+dfsg-2.dsc 2120 SHA256:7965fd63c4cb970d0f675f574f6730114c806139e433cb3589a428658fc4d0cd
'http://http.debian.net/debian/pool/main/t/tcl8.6/tcl8.6_8.6.13%2bdfsg.orig.tar.gz' tcl8.6_8.6.13+dfsg.orig.tar.gz 6302749 SHA256:83bce7277e3825df0179567e0d8a431ebb1a126df53ea4a94af89dd4dd0f26d5
'http://http.debian.net/debian/pool/main/t/tcl8.6/tcl8.6_8.6.13%2bdfsg-2.debian.tar.xz' tcl8.6_8.6.13+dfsg-2.debian.tar.xz 14336 SHA256:899c8d800988caa1f5a8b070d3697f29c3d098754416cc2816b94dfa93aef009
```

### `dpkg` source package: `tex-gyre=20180621-6`

Binary Packages:

- `fonts-texgyre=20180621-6`

Licenses: (parsed from: `/usr/share/doc/fonts-texgyre/copyright`)

- `DejaVu-License`
- `GPL-2`
- `GPL-2+`
- `GUST-Font-License`

Source:

```console
$ apt-get source -qq --print-uris tex-gyre=20180621-6
'http://http.debian.net/debian/pool/main/t/tex-gyre/tex-gyre_20180621-6.dsc' tex-gyre_20180621-6.dsc 2241 SHA256:83a26e65fee0ac79f31a44e083e03da2fef7b031c70d0f336796782cc0fed099
'http://http.debian.net/debian/pool/main/t/tex-gyre/tex-gyre_20180621.orig.tar.gz' tex-gyre_20180621.orig.tar.gz 24033627 SHA256:fe6b0f8ca6890d4a369f36c3b45bc30470069701a2f59042178ad5933fc9cdb8
'http://http.debian.net/debian/pool/main/t/tex-gyre/tex-gyre_20180621-6.debian.tar.xz' tex-gyre_20180621-6.debian.tar.xz 11632 SHA256:731e04abb52038a7de626e4679d6b823b2d692be029bb88399951fb69b286f67
```

### `dpkg` source package: `tiff=4.5.1+git230720-4`

Binary Packages:

- `libtiff6:amd64=4.5.1+git230720-4`

Licenses: (parsed from: `/usr/share/doc/libtiff6/copyright`)

- `Hylafax`

Source:

```console
$ apt-get source -qq --print-uris tiff=4.5.1+git230720-4
'http://http.debian.net/debian/pool/main/t/tiff/tiff_4.5.1%2bgit230720-4.dsc' tiff_4.5.1+git230720-4.dsc 2322 SHA256:84f3fe1110e4633c897e63a6cc0122d2db3afb36140f089ec727ffe0f61facd1
'http://http.debian.net/debian/pool/main/t/tiff/tiff_4.5.1%2bgit230720.orig.tar.xz' tiff_4.5.1+git230720.orig.tar.xz 1781896 SHA256:0e51bcf3a3ffa5fc76ea6aeb74a797f95c84544fcc8b6a1ec5def967a78e9e12
'http://http.debian.net/debian/pool/main/t/tiff/tiff_4.5.1%2bgit230720-4.debian.tar.xz' tiff_4.5.1+git230720-4.debian.tar.xz 26260 SHA256:a4ba563349fe2e53759703dce1aa476cbb3621ab3b4389df97faf60dd06067ad
```

### `dpkg` source package: `tk8.6=8.6.13-2`

Binary Packages:

- `libtk8.6:amd64=8.6.13-2+b1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris tk8.6=8.6.13-2
'http://http.debian.net/debian/pool/main/t/tk8.6/tk8.6_8.6.13-2.dsc' tk8.6_8.6.13-2.dsc 2155 SHA256:12783fea0125ef3e67a1a07b2b24f7e27329214394ca5b543bd38716a91d7a1e
'http://http.debian.net/debian/pool/main/t/tk8.6/tk8.6_8.6.13.orig.tar.gz' tk8.6_8.6.13.orig.tar.gz 4546848 SHA256:2e65fa069a23365440a3c56c556b8673b5e32a283800d8d9b257e3f584ce0675
'http://http.debian.net/debian/pool/main/t/tk8.6/tk8.6_8.6.13-2.debian.tar.xz' tk8.6_8.6.13-2.debian.tar.xz 10740 SHA256:1e57bc189cfa3e73e140aa1853b91e6c9a4da99eccd931de24e0c2cd525f8319
```

### `dpkg` source package: `tzdata=2024a-1`

Binary Packages:

- `tzdata=2024a-1`

Licenses: (parsed from: `/usr/share/doc/tzdata/copyright`)

- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris tzdata=2024a-1
'http://http.debian.net/debian/pool/main/t/tzdata/tzdata_2024a-1.dsc' tzdata_2024a-1.dsc 2429 SHA256:16e9e28383d581d0440a379f14e96786308976a409ce2c3f7b64a4b0a2935bda
'http://http.debian.net/debian/pool/main/t/tzdata/tzdata_2024a.orig.tar.gz' tzdata_2024a.orig.tar.gz 451270 SHA256:0d0434459acbd2059a7a8da1f3304a84a86591f6ed69c6248fffa502b6edffe3
'http://http.debian.net/debian/pool/main/t/tzdata/tzdata_2024a.orig.tar.gz.asc' tzdata_2024a.orig.tar.gz.asc 833 SHA256:f64725f9f65419e7b009e3b95b75ea9516382d0be64aef63d78654d9c569ed0d
'http://http.debian.net/debian/pool/main/t/tzdata/tzdata_2024a-1.debian.tar.xz' tzdata_2024a-1.debian.tar.xz 122116 SHA256:2cdad8bafca6cbd13fe0c8f41e7c45bc4a30cdde631b5bb8438f850670513855
```

### `dpkg` source package: `ucf=3.0043+nmu1`

Binary Packages:

- `ucf=3.0043+nmu1`

Licenses: (parsed from: `/usr/share/doc/ucf/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris ucf=3.0043+nmu1
'http://http.debian.net/debian/pool/main/u/ucf/ucf_3.0043%2bnmu1.dsc' ucf_3.0043+nmu1.dsc 1567 SHA256:5ef70fa7a58cd3f162932661453a1e9d21d749b47a1aa84198f7c4cd9eac20ee
'http://http.debian.net/debian/pool/main/u/ucf/ucf_3.0043%2bnmu1.tar.xz' ucf_3.0043+nmu1.tar.xz 70916 SHA256:a07143046236cb082517e346362306cb3fe4d3634cad1add40c905b0e0ecf58c
```

### `dpkg` source package: `unzip=6.0-28`

Binary Packages:

- `unzip=6.0-28`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris unzip=6.0-28
'http://http.debian.net/debian/pool/main/u/unzip/unzip_6.0-28.dsc' unzip_6.0-28.dsc 1359 SHA256:f5b486028b61a145b591fdd96aaeaf89ef6eef164a299f43bd5e6704bdefc8a2
'http://http.debian.net/debian/pool/main/u/unzip/unzip_6.0.orig.tar.gz' unzip_6.0.orig.tar.gz 1376845 SHA256:036d96991646d0449ed0aa952e4fbe21b476ce994abc276e49d30e686708bd37
'http://http.debian.net/debian/pool/main/u/unzip/unzip_6.0-28.debian.tar.xz' unzip_6.0-28.debian.tar.xz 25032 SHA256:e51364116c84739c591728ecc841113a914fa11358fd10ff0d6813524d811bb9
```

### `dpkg` source package: `usrmerge=39`

Binary Packages:

- `usr-is-merged=39`

Licenses: (parsed from: `/usr/share/doc/usr-is-merged/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris usrmerge=39
'http://http.debian.net/debian/pool/main/u/usrmerge/usrmerge_39.dsc' usrmerge_39.dsc 981 SHA256:44027067423faefd31ac321c283fc9b07184fecbd5304ed41490c03825b89a28
'http://http.debian.net/debian/pool/main/u/usrmerge/usrmerge_39.tar.xz' usrmerge_39.tar.xz 14908 SHA256:90b4ee198469292da4ee8b4ce2ec7b3ec439d61e6beb3ed9d3fa82b0e46e7fa3
```

### `dpkg` source package: `util-linux=2.39.3-6`

Binary Packages:

- `bsdutils=1:2.39.3-6`
- `libblkid1:amd64=2.39.3-6`
- `libmount1:amd64=2.39.3-6`
- `libsmartcols1:amd64=2.39.3-6`
- `libuuid1:amd64=2.39.3-6`
- `mount=2.39.3-6`
- `util-linux=2.39.3-6`

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
$ apt-get source -qq --print-uris util-linux=2.39.3-6
'http://http.debian.net/debian/pool/main/u/util-linux/util-linux_2.39.3-6.dsc' util-linux_2.39.3-6.dsc 4608 SHA256:53a8bd6e71dbd9b053251b851f098a90c9ba28202e37d06e4f423e6349df77e1
'http://http.debian.net/debian/pool/main/u/util-linux/util-linux_2.39.3.orig.tar.xz' util-linux_2.39.3.orig.tar.xz 8526168 SHA256:7b6605e48d1a49f43cc4b4cfc59f313d0dd5402fa40b96810bd572e167dfed0f
'http://http.debian.net/debian/pool/main/u/util-linux/util-linux_2.39.3-6.debian.tar.xz' util-linux_2.39.3-6.debian.tar.xz 99148 SHA256:81abf57702e400d0052c8b30f396b0bad73aebaadceb935455017437b2abb2cf
```

### `dpkg` source package: `vim=2:9.1.0016-1`

Binary Packages:

- `vim-common=2:9.1.0016-1`
- `vim-tiny=2:9.1.0016-1`

Licenses: (parsed from: `/usr/share/doc/vim-common/copyright`, `/usr/share/doc/vim-tiny/copyright`)

- `Apache`
- `Apache-2.0`
- `Artistic`
- `Artistic-1`
- `BSD-2-clause`
- `BSD-3-clause`
- `Compaq`
- `EDL-1`
- `Expat`
- `GPL-1`
- `GPL-1+`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `OPL-1+`
- `UC`
- `Vim`
- `Vim-Regexp`
- `X11`
- `XPM`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris vim=2:9.1.0016-1
'http://http.debian.net/debian/pool/main/v/vim/vim_9.1.0016-1.dsc' vim_9.1.0016-1.dsc 2905 SHA256:80cecf5b5abbc6420dfb38b4774c4907e4b7623319ed8e9399163a384f0e61d7
'http://http.debian.net/debian/pool/main/v/vim/vim_9.1.0016.orig.tar.gz' vim_9.1.0016.orig.tar.gz 17621043 SHA256:abe876bb18554bb1eb69d23eaabe89caabeef182737e9e8bfa4cc298dee061df
'http://http.debian.net/debian/pool/main/v/vim/vim_9.1.0016-1.debian.tar.xz' vim_9.1.0016-1.debian.tar.xz 187588 SHA256:47b6e47308d5fc916b1c8d34cd88dc8abc281728f2c127657ff9b061680766f6
```

### `dpkg` source package: `wget=1.21.4-1`

Binary Packages:

- `wget=1.21.4-1+b1`

Licenses: (parsed from: `/usr/share/doc/wget/copyright`)

- `GFDL-1.2`
- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris wget=1.21.4-1
'http://http.debian.net/debian/pool/main/w/wget/wget_1.21.4-1.dsc' wget_1.21.4-1.dsc 2167 SHA256:885f3b8acfeaa27119296d18e2624cc80788670e585692375e82f381d2b99f3b
'http://http.debian.net/debian/pool/main/w/wget/wget_1.21.4.orig.tar.gz' wget_1.21.4.orig.tar.gz 5059591 SHA256:81542f5cefb8faacc39bbbc6c82ded80e3e4a88505ae72ea51df27525bcde04c
'http://http.debian.net/debian/pool/main/w/wget/wget_1.21.4.orig.tar.gz.asc' wget_1.21.4.orig.tar.gz.asc 854 SHA256:fb1ce21577dee962be8bf95cbf86f806815778264622a5d756324ff8dd3bfc57
'http://http.debian.net/debian/pool/main/w/wget/wget_1.21.4-1.debian.tar.xz' wget_1.21.4-1.debian.tar.xz 60692 SHA256:88857f1f61992bbbaa591149be2caf1cad9327c8c02c68a5ae6d078ed8f3678c
```

### `dpkg` source package: `xauth=1:1.1.2-1`

Binary Packages:

- `xauth=1:1.1.2-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris xauth=1:1.1.2-1
'http://http.debian.net/debian/pool/main/x/xauth/xauth_1.1.2-1.dsc' xauth_1.1.2-1.dsc 1840 SHA256:5b6f718530b68c385368bae7267e7dd0044882290e7b3e4fbe6d63bb8d65c9f0
'http://http.debian.net/debian/pool/main/x/xauth/xauth_1.1.2.orig.tar.gz' xauth_1.1.2.orig.tar.gz 214621 SHA256:84d27a1023d8da524c134f424b312e53cb96e08871f96868aa20316bfcbbc054
'http://http.debian.net/debian/pool/main/x/xauth/xauth_1.1.2-1.diff.gz' xauth_1.1.2-1.diff.gz 18091 SHA256:6afd6f9a3c9b6320e4b523bbe6e5ff3960d59310c9b0efc8b6496d39144710ed
```

### `dpkg` source package: `xdg-utils=1.1.3-4.1`

Binary Packages:

- `xdg-utils=1.1.3-4.1`

Licenses: (parsed from: `/usr/share/doc/xdg-utils/copyright`)

- `Expat`

Source:

```console
$ apt-get source -qq --print-uris xdg-utils=1.1.3-4.1
'http://http.debian.net/debian/pool/main/x/xdg-utils/xdg-utils_1.1.3-4.1.dsc' xdg-utils_1.1.3-4.1.dsc 1756 SHA256:c54ae65034c4c3e9f2208a44990111d34fc5ed1e689efd3907a2a8e5e965ccac
'http://http.debian.net/debian/pool/main/x/xdg-utils/xdg-utils_1.1.3.orig.tar.gz' xdg-utils_1.1.3.orig.tar.gz 297170 SHA256:d798b08af8a8e2063ddde6c9fa3398ca81484f27dec642c5627ffcaa0d4051d9
'http://http.debian.net/debian/pool/main/x/xdg-utils/xdg-utils_1.1.3-4.1.debian.tar.xz' xdg-utils_1.1.3-4.1.debian.tar.xz 15660 SHA256:0ea0b550719ab75f9a0fe58ed907673c5bcfc2bd87537845534694c502740aed
```

### `dpkg` source package: `xft=2.3.6-1`

Binary Packages:

- `libxft2:amd64=2.3.6-1+b1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris xft=2.3.6-1
'http://http.debian.net/debian/pool/main/x/xft/xft_2.3.6-1.dsc' xft_2.3.6-1.dsc 2006 SHA256:252220495bd12fac30d8f1b1994916beaed9c5149138dcc62e230fee17339530
'http://http.debian.net/debian/pool/main/x/xft/xft_2.3.6.orig.tar.gz' xft_2.3.6.orig.tar.gz 447498 SHA256:b7e59f69e0bbabe9438088775f7e5a7c16a572e58b11f9722519385d38192df5
'http://http.debian.net/debian/pool/main/x/xft/xft_2.3.6-1.diff.gz' xft_2.3.6-1.diff.gz 17995 SHA256:9d4c64fc52626134a3f753df88fceaba0cb460bd9b56544f0e42178deca77019
```

### `dpkg` source package: `xorg=1:7.7+23`

Binary Packages:

- `x11-common=1:7.7+23`

Licenses: (parsed from: `/usr/share/doc/x11-common/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris xorg=1:7.7+23
'http://http.debian.net/debian/pool/main/x/xorg/xorg_7.7%2b23.dsc' xorg_7.7+23.dsc 1975 SHA256:b06ef48b56736e0a0a48bcbc1afd2cf6dcd70959c2b52e195456a0392076469c
'http://http.debian.net/debian/pool/main/x/xorg/xorg_7.7%2b23.tar.gz' xorg_7.7+23.tar.gz 287306 SHA256:8458b8798d7d6098cd5259abc447d6c7a371e20e641cac82cf635296a71f468e
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
'http://http.debian.net/debian/pool/main/x/xxhash/xxhash_0.8.2-2.dsc' xxhash_0.8.2-2.dsc 1969 SHA256:8fbf9f5a50a4cf48e771e157e386bd2b2938e46cecd4bc53117ee1a4a615af1d
'http://http.debian.net/debian/pool/main/x/xxhash/xxhash_0.8.2.orig.tar.gz' xxhash_0.8.2.orig.tar.gz 1141188 SHA256:baee0c6afd4f03165de7a4e67988d16f0f2b257b51d0e3cb91909302a26a79c4
'http://http.debian.net/debian/pool/main/x/xxhash/xxhash_0.8.2-2.debian.tar.xz' xxhash_0.8.2-2.debian.tar.xz 4920 SHA256:fcbdd52df60936173524743680f6d3c504b9a90553fe113cd0aa531faf4f2c4d
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
'http://http.debian.net/debian/pool/main/x/xz-utils/xz-utils_5.4.5-0.3.dsc' xz-utils_5.4.5-0.3.dsc 2720 SHA256:3da917542fe87c05b058833bdd91929a5a42632f883d2fddd2dde74e2735bb0f
'http://http.debian.net/debian/pool/main/x/xz-utils/xz-utils_5.4.5.orig.tar.xz' xz-utils_5.4.5.orig.tar.xz 1680520 SHA256:da9dec6c12cf2ecf269c31ab65b5de18e8e52b96f35d5bcd08c12b43e6878803
'http://http.debian.net/debian/pool/main/x/xz-utils/xz-utils_5.4.5.orig.tar.xz.asc' xz-utils_5.4.5.orig.tar.xz.asc 833 SHA256:1fbf414df852daab603ad43a57348e4e5fc20c95ce10be16c433ee7c5e1da69b
'http://http.debian.net/debian/pool/main/x/xz-utils/xz-utils_5.4.5-0.3.debian.tar.xz' xz-utils_5.4.5-0.3.debian.tar.xz 26944 SHA256:5ac2b0fe0e5c24806fc0b9d72e5ed9b796532404170b4331e5482571ebc86f2a
```

### `dpkg` source package: `zip=3.0-13`

Binary Packages:

- `zip=3.0-13`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris zip=3.0-13
'http://http.debian.net/debian/pool/main/z/zip/zip_3.0-13.dsc' zip_3.0-13.dsc 1336 SHA256:9fad1b5bda0c38a6811494159953a19dc42b9022b29b73ba51f30d2bb48445e6
'http://http.debian.net/debian/pool/main/z/zip/zip_3.0.orig.tar.gz' zip_3.0.orig.tar.gz 1118845 SHA256:f0e8bb1f9b7eb0b01285495a2699df3a4b766784c1765a8f1aeedf63c0806369
'http://http.debian.net/debian/pool/main/z/zip/zip_3.0-13.debian.tar.xz' zip_3.0-13.debian.tar.xz 8688 SHA256:4f5aca2d9f6021d2fd73f2fc16e9a392ab98673a940b44cf78fe38b8cdec1ab9
```

### `dpkg` source package: `zlib=1:1.3.dfsg-3`

Binary Packages:

- `zlib1g:amd64=1:1.3.dfsg-3+b1`
- `zlib1g-dev:amd64=1:1.3.dfsg-3+b1`

Licenses: (parsed from: `/usr/share/doc/zlib1g/copyright`, `/usr/share/doc/zlib1g-dev/copyright`)

- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris zlib=1:1.3.dfsg-3
'http://http.debian.net/debian/pool/main/z/zlib/zlib_1.3.dfsg-3.dsc' zlib_1.3.dfsg-3.dsc 2547 SHA256:ff17bb7134b314999d3a205a056cb39235f18636253b4e39703c0d9bbbaa377b
'http://http.debian.net/debian/pool/main/z/zlib/zlib_1.3.dfsg.orig.tar.xz' zlib_1.3.dfsg.orig.tar.xz 1128572 SHA256:5eea0322c1c21c75cad3b607ac1c43ff5c71e014b8ac4a34300b5e2b80d02e70
'http://http.debian.net/debian/pool/main/z/zlib/zlib_1.3.dfsg-3.debian.tar.xz' zlib_1.3.dfsg-3.debian.tar.xz 17308 SHA256:3fab93040e86f3f980f90b03687a60c6aad097122e19d055aa8a3df58511e4eb
```
