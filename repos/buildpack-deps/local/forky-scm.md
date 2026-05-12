# `buildpack-deps:forky-scm`

## Docker Metadata

- Image ID: `sha256:1baef7a3a5e0168a6106de790a1e0bcf28980526089cab706845da1713f8aca6`
- Created: `2026-05-08T20:26:26.662481047Z`
- Virtual Size: ~ 387.07 Mb  
  (total size of all layers on-disk)
- Arch: `linux`/`amd64`
- Command: `["bash"]`
- Environment:
  - `PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin`

## `dpkg` (`.deb`-based packages)

### `dpkg` source package: `acl=2.3.2-3`

Binary Packages:

- `libacl1:amd64=2.3.2-3`

Licenses: (parsed from: `/usr/share/doc/libacl1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2+`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris acl=2.3.2-3
'http://deb.debian.org/debian/pool/main/a/acl/acl_2.3.2-3.dsc' acl_2.3.2-3.dsc 2642 SHA256:19a27264c715b57f954df7a753627d197c8ad839e4428d86455d82a29384b67b
'http://deb.debian.org/debian/pool/main/a/acl/acl_2.3.2.orig.tar.xz' acl_2.3.2.orig.tar.xz 371680 SHA256:97203a72cae99ab89a067fe2210c1cbf052bc492b479eca7d226d9830883b0bd
'http://deb.debian.org/debian/pool/main/a/acl/acl_2.3.2.orig.tar.xz.asc' acl_2.3.2.orig.tar.xz.asc 833 SHA256:184c6a903490885a096095db67b433a04542c6569f167cbe8115268c0f227273
'http://deb.debian.org/debian/pool/main/a/acl/acl_2.3.2-3.debian.tar.xz' acl_2.3.2-3.debian.tar.xz 25016 SHA256:a3ae602c78e6c3465560e695242d0a649223ddc90de5dc4c83688106e42ba009
```

Other potentially useful URLs:

- https://sources.debian.net/src/acl/2.3.2-3/ (for browsing the source)
- https://sources.debian.net/src/acl/2.3.2-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/acl/2.3.2-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `apr-util=1.6.3-4`

Binary Packages:

- `libaprutil1t64:amd64=1.6.3-4+b1`

Licenses: (parsed from: `/usr/share/doc/libaprutil1t64/copyright`)

- `Apache-2.0`

Source:

```console
$ apt-get source -qq --print-uris apr-util=1.6.3-4
'http://deb.debian.org/debian/pool/main/a/apr-util/apr-util_1.6.3-4.dsc' apr-util_1.6.3-4.dsc 2899 SHA256:331fa0cbca37f7406680fa9dbbe45fe5db9039c7e75cad0463af83be48239874
'http://deb.debian.org/debian/pool/main/a/apr-util/apr-util_1.6.3.orig.tar.bz2' apr-util_1.6.3.orig.tar.bz2 432692 SHA256:a41076e3710746326c3945042994ad9a4fcac0ce0277dd8fea076fec3c9772b5
'http://deb.debian.org/debian/pool/main/a/apr-util/apr-util_1.6.3.orig.tar.bz2.asc' apr-util_1.6.3.orig.tar.bz2.asc 833 SHA256:5fd08491a2cb35fdbf9fa93d753cfd25e59fe58a75a3f3ed62582ebf2a5b3a51
'http://deb.debian.org/debian/pool/main/a/apr-util/apr-util_1.6.3-4.debian.tar.xz' apr-util_1.6.3-4.debian.tar.xz 39104 SHA256:d5daefd55fe6d5c9d322c69f3b86f7acdb22c96b2b6f8f6f42c0086f3a383178
```

Other potentially useful URLs:

- https://sources.debian.net/src/apr-util/1.6.3-4/ (for browsing the source)
- https://sources.debian.net/src/apr-util/1.6.3-4/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/apr-util/1.6.3-4/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `apr=1.7.6-3`

Binary Packages:

- `libapr1t64:amd64=1.7.6-3+b1`

Licenses: (parsed from: `/usr/share/doc/libapr1t64/copyright`)

- `Apache-2.0`

Source:

```console
$ apt-get source -qq --print-uris apr=1.7.6-3
'http://deb.debian.org/debian/pool/main/a/apr/apr_1.7.6-3.dsc' apr_1.7.6-3.dsc 2402 SHA256:8a2947b338a2247bc6b58146c57a8d3db3253cffb9a63b62360e164ea4c7a37d
'http://deb.debian.org/debian/pool/main/a/apr/apr_1.7.6.orig.tar.bz2' apr_1.7.6.orig.tar.bz2 899670 SHA256:49030d92d2575da735791b496dc322f3ce5cff9494779ba8cc28c7f46c5deb32
'http://deb.debian.org/debian/pool/main/a/apr/apr_1.7.6.orig.tar.bz2.asc' apr_1.7.6.orig.tar.bz2.asc 898 SHA256:24c2f1ab9c7b9cc9410f44ddd7a659316993685fd9c4f8c4b7bc67eb3e83e331
'http://deb.debian.org/debian/pool/main/a/apr/apr_1.7.6-3.debian.tar.xz' apr_1.7.6-3.debian.tar.xz 42384 SHA256:62e334f0ffc583a3328e28e5749249fdaa56f1ee31208f80b869757192901034
```

Other potentially useful URLs:

- https://sources.debian.net/src/apr/1.7.6-3/ (for browsing the source)
- https://sources.debian.net/src/apr/1.7.6-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/apr/1.7.6-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `apt=3.2.0`

Binary Packages:

- `apt=3.2.0`
- `libapt-pkg7.0:amd64=3.2.0`

Licenses: (parsed from: `/usr/share/doc/apt/copyright`, `/usr/share/doc/libapt-pkg7.0/copyright`)

- `BSD-3-clause`
- `Expat`
- `GPL-2`
- `GPL-2+`
- `curl`

Source:

```console
$ apt-get source -qq --print-uris apt=3.2.0
'http://deb.debian.org/debian/pool/main/a/apt/apt_3.2.0.dsc' apt_3.2.0.dsc 3127 SHA256:364347278a531cf073f809a14f84617c2b935cfb324bd413aa01c214b6f8a3e8
'http://deb.debian.org/debian/pool/main/a/apt/apt_3.2.0.tar.xz' apt_3.2.0.tar.xz 2476660 SHA256:dcd186912a7b8553cc885412127925858ee340c655e2f26e77eacdab23f48089
```

Other potentially useful URLs:

- https://sources.debian.net/src/apt/3.2.0/ (for browsing the source)
- https://sources.debian.net/src/apt/3.2.0/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/apt/3.2.0/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `attr=1:2.5.2-4`

Binary Packages:

- `libattr1:amd64=1:2.5.2-4`

Licenses: (parsed from: `/usr/share/doc/libattr1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2+`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris attr=1:2.5.2-4
'http://deb.debian.org/debian/pool/main/a/attr/attr_2.5.2-4.dsc' attr_2.5.2-4.dsc 2614 SHA256:256e36ed6f60a39813a304a11617a3e573a11019db007a891bfeff7f2dad7175
'http://deb.debian.org/debian/pool/main/a/attr/attr_2.5.2.orig.tar.xz' attr_2.5.2.orig.tar.xz 334180 SHA256:f2e97b0ab7ce293681ab701915766190d607a1dba7fae8a718138150b700a70b
'http://deb.debian.org/debian/pool/main/a/attr/attr_2.5.2.orig.tar.xz.asc' attr_2.5.2.orig.tar.xz.asc 833 SHA256:eeac729088d3c6379e91b7596cb3582e46b047c47f0fa3c5c77f9c9e84dc3a4c
'http://deb.debian.org/debian/pool/main/a/attr/attr_2.5.2-4.debian.tar.xz' attr_2.5.2-4.debian.tar.xz 32372 SHA256:d49f176ceaceb3679141e9bb00a7595848e91b4c4db8682f81a828109ee6e2c7
```

Other potentially useful URLs:

- https://sources.debian.net/src/attr/1:2.5.2-4/ (for browsing the source)
- https://sources.debian.net/src/attr/1:2.5.2-4/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/attr/1:2.5.2-4/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `audit=1:4.1.2-1`

Binary Packages:

- `libaudit-common=1:4.1.2-1`
- `libaudit1:amd64=1:4.1.2-1+b1`

Licenses: (parsed from: `/usr/share/doc/libaudit-common/copyright`, `/usr/share/doc/libaudit1/copyright`)

- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris audit=1:4.1.2-1
'http://deb.debian.org/debian/pool/main/a/audit/audit_4.1.2-1.dsc' audit_4.1.2-1.dsc 2546 SHA256:5443f3ff043dd30cba1549f93940928d04c90cdc7598741a19f722d4109a7f4b
'http://deb.debian.org/debian/pool/main/a/audit/audit_4.1.2.orig.tar.gz' audit_4.1.2.orig.tar.gz 656095 SHA256:5c638bbeef9adb6c5715d3a60f0f5adb93e9b81633608af13d23c61f5e5db04d
'http://deb.debian.org/debian/pool/main/a/audit/audit_4.1.2-1.debian.tar.xz' audit_4.1.2-1.debian.tar.xz 19712 SHA256:1cb30c0bc4bed825cbac829cec4b840b9d0726dedaf25f57cbc3af9bc7d7bcc2
```

Other potentially useful URLs:

- https://sources.debian.net/src/audit/1:4.1.2-1/ (for browsing the source)
- https://sources.debian.net/src/audit/1:4.1.2-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/audit/1:4.1.2-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `base-files=14`

Binary Packages:

- `base-files=14`

Licenses: (parsed from: `/usr/share/doc/base-files/copyright`)

- `GPL`
- `GPL-2+`
- `verbatim`

Source:

```console
$ apt-get source -qq --print-uris base-files=14
'http://deb.debian.org/debian/pool/main/b/base-files/base-files_14.dsc' base-files_14.dsc 1207 SHA256:5cdce966268b529d7897b088f28d022093f390970eb63541f5e3753ca521c23b
'http://deb.debian.org/debian/pool/main/b/base-files/base-files_14.tar.xz' base-files_14.tar.xz 68388 SHA256:dbb9ebd9278b0507d82c29dff894caf9dfc2b46d35e33a4a1505c96c6c6e54d8
```

Other potentially useful URLs:

- https://sources.debian.net/src/base-files/14/ (for browsing the source)
- https://sources.debian.net/src/base-files/14/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/base-files/14/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `base-passwd=3.6.8`

Binary Packages:

- `base-passwd=3.6.8`

Licenses: (parsed from: `/usr/share/doc/base-passwd/copyright`)

- `GPL-2`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris base-passwd=3.6.8
'http://deb.debian.org/debian/pool/main/b/base-passwd/base-passwd_3.6.8.dsc' base-passwd_3.6.8.dsc 2044 SHA256:e76e572d2653f2b8eda64c662f5b4310a978ef1fdd039410ace5f6355c3af7d6
'http://deb.debian.org/debian/pool/main/b/base-passwd/base-passwd_3.6.8.tar.xz' base-passwd_3.6.8.tar.xz 61840 SHA256:fab3d0e6e8b641e116bda9bd5f7a7ed24482384c1513f6a369b506327fbc8dde
```

Other potentially useful URLs:

- https://sources.debian.net/src/base-passwd/3.6.8/ (for browsing the source)
- https://sources.debian.net/src/base-passwd/3.6.8/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/base-passwd/3.6.8/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `bash=5.3-2`

Binary Packages:

- `bash=5.3-2`

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
$ apt-get source -qq --print-uris bash=5.3-2
'http://deb.debian.org/debian/pool/main/b/bash/bash_5.3-2.dsc' bash_5.3-2.dsc 2141 SHA256:c4e8f54f49b0fc9a43ed59016c00626f354f3fd7dcb0894646496e9deae0f120
'http://deb.debian.org/debian/pool/main/b/bash/bash_5.3.orig.tar.xz' bash_5.3.orig.tar.xz 5571836 SHA256:a70de6bb41f5e192534a5a1836b1d7fad9a8d4818a6e1506d70f38441552c17a
'http://deb.debian.org/debian/pool/main/b/bash/bash_5.3-2.debian.tar.xz' bash_5.3-2.debian.tar.xz 91816 SHA256:e076ede422f979e4fbd1a0c5818b0a1dec87d6bcd3770eceb3dd8168522b48a5
```

Other potentially useful URLs:

- https://sources.debian.net/src/bash/5.3-2/ (for browsing the source)
- https://sources.debian.net/src/bash/5.3-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/bash/5.3-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `brotli=1.2.0-3`

Binary Packages:

- `libbrotli1:amd64=1.2.0-3`

Licenses: (parsed from: `/usr/share/doc/libbrotli1/copyright`)

- `MIT`

Source:

```console
$ apt-get source -qq --print-uris brotli=1.2.0-3
'http://deb.debian.org/debian/pool/main/b/brotli/brotli_1.2.0-3.dsc' brotli_1.2.0-3.dsc 2282 SHA256:81fefbd04efc85b4700bb2a76fbfe3418102289ad2ae1f392d0648d10a5ef9ac
'http://deb.debian.org/debian/pool/main/b/brotli/brotli_1.2.0.orig.tar.gz' brotli_1.2.0.orig.tar.gz 646398 SHA256:eb5f7dadf215d0670665fd81566e1fe2dfdc154d983f09142de7299df4c182e6
'http://deb.debian.org/debian/pool/main/b/brotli/brotli_1.2.0-3.debian.tar.xz' brotli_1.2.0-3.debian.tar.xz 5896 SHA256:d227ff2af4725de3f9fe994796df6416f4a050265c82188e16402742f771f623
```

Other potentially useful URLs:

- https://sources.debian.net/src/brotli/1.2.0-3/ (for browsing the source)
- https://sources.debian.net/src/brotli/1.2.0-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/brotli/1.2.0-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `bzip2=1.0.8-6`

Binary Packages:

- `libbz2-1.0:amd64=1.0.8-6+b2`

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

### `dpkg` source package: `ca-certificates=20260223`

Binary Packages:

- `ca-certificates=20260223`

Licenses: (parsed from: `/usr/share/doc/ca-certificates/copyright`)

- `GPL-2`
- `GPL-2+`
- `MPL-2.0`

Source:

```console
$ apt-get source -qq --print-uris ca-certificates=20260223
'http://deb.debian.org/debian/pool/main/c/ca-certificates/ca-certificates_20260223.dsc' ca-certificates_20260223.dsc 1766 SHA256:1513677cb1cf906a4b688279f86cdfda2a5373894c25521ed61eb6b2812ddf93
'http://deb.debian.org/debian/pool/main/c/ca-certificates/ca-certificates_20260223.tar.xz' ca-certificates_20260223.tar.xz 282672 SHA256:2fa2b00d4360f0d14ec51640ae8aea9e563956b95ea786e3c3c01c4eead42b56
```

Other potentially useful URLs:

- https://sources.debian.net/src/ca-certificates/20260223/ (for browsing the source)
- https://sources.debian.net/src/ca-certificates/20260223/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/ca-certificates/20260223/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `cdebconf=0.282`

Binary Packages:

- `libdebconfclient0:amd64=0.282+b3`

Licenses: (parsed from: `/usr/share/doc/libdebconfclient0/copyright`)

- `BSD-2-Clause`
- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris cdebconf=0.282
'http://deb.debian.org/debian/pool/main/c/cdebconf/cdebconf_0.282.dsc' cdebconf_0.282.dsc 2694 SHA256:eddf49a846ed6e9f4f20cb14975cca7107580c061bc748f2b51dc9d0b7f4ddf7
'http://deb.debian.org/debian/pool/main/c/cdebconf/cdebconf_0.282.tar.xz' cdebconf_0.282.tar.xz 286192 SHA256:7451627f8274a8db0a1d24c3c589ba163036ca79fdb96ed86ddd0157a4369618
```

Other potentially useful URLs:

- https://sources.debian.net/src/cdebconf/0.282/ (for browsing the source)
- https://sources.debian.net/src/cdebconf/0.282/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/cdebconf/0.282/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `coreutils=9.10-1`

Binary Packages:

- `coreutils=9.10-1`

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
$ apt-get source -qq --print-uris coreutils=9.10-1
'http://deb.debian.org/debian/pool/main/c/coreutils/coreutils_9.10-1.dsc' coreutils_9.10-1.dsc 2121 SHA256:4d924822bcf969e83dd8b98fd42194bbad1160a09d8338019e44ecc6c315e414
'http://deb.debian.org/debian/pool/main/c/coreutils/coreutils_9.10.orig.tar.xz' coreutils_9.10.orig.tar.xz 6507600 SHA256:16535a9adf0b10037364e2d612aad3d9f4eca3a344949ced74d12faf4bd51d25
'http://deb.debian.org/debian/pool/main/c/coreutils/coreutils_9.10.orig.tar.xz.asc' coreutils_9.10.orig.tar.xz.asc 833 SHA256:4faaa822d78cb8f7c67b6c89c92b107cc973a09bece6da6ab12285218e0e4105
'http://deb.debian.org/debian/pool/main/c/coreutils/coreutils_9.10-1.debian.tar.xz' coreutils_9.10-1.debian.tar.xz 22484 SHA256:eb9bb80fdee97fc5ae7550dfad6fbdc666483e354c813844aa775245ffcd84a6
```

Other potentially useful URLs:

- https://sources.debian.net/src/coreutils/9.10-1/ (for browsing the source)
- https://sources.debian.net/src/coreutils/9.10-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/coreutils/9.10-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `curl=8.19.0-3`

Binary Packages:

- `curl=8.19.0-3`
- `libcurl3t64-gnutls:amd64=8.19.0-3`
- `libcurl4t64:amd64=8.19.0-3`

Licenses: (parsed from: `/usr/share/doc/curl/copyright`, `/usr/share/doc/libcurl3t64-gnutls/copyright`, `/usr/share/doc/libcurl4t64/copyright`)

- `BSD-4-Clause-UC`
- `FSFUL`
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

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/curl/8.19.0-3/


### `dpkg` source package: `cyrus-sasl2=2.1.28+dfsg1-11`

Binary Packages:

- `libsasl2-2:amd64=2.1.28+dfsg1-11`
- `libsasl2-modules-db:amd64=2.1.28+dfsg1-11`

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
$ apt-get source -qq --print-uris cyrus-sasl2=2.1.28+dfsg1-11
'http://deb.debian.org/debian/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.28%2bdfsg1-11.dsc' cyrus-sasl2_2.1.28+dfsg1-11.dsc 3479 SHA256:60dfcaf966bf9bc1211ac307d36a635059a5ba364a98c1d9efcda8a0f5900d74
'http://deb.debian.org/debian/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.28%2bdfsg1.orig.tar.xz' cyrus-sasl2_2.1.28+dfsg1.orig.tar.xz 794540 SHA256:e796a5d85d1a85e1b433d43504e467f9075c7ebc0b45730a3996cf11b1deada4
'http://deb.debian.org/debian/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.28%2bdfsg1-11.debian.tar.xz' cyrus-sasl2_2.1.28+dfsg1-11.debian.tar.xz 102628 SHA256:9efbb3e4a6010aa7f25d1a73d9b42a63b10e29058c2083b0f0db3fe58cd49a77
```

Other potentially useful URLs:

- https://sources.debian.net/src/cyrus-sasl2/2.1.28+dfsg1-11/ (for browsing the source)
- https://sources.debian.net/src/cyrus-sasl2/2.1.28+dfsg1-11/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/cyrus-sasl2/2.1.28+dfsg1-11/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `dash=0.5.12-12`

Binary Packages:

- `dash=0.5.12-12`

Licenses: (parsed from: `/usr/share/doc/dash/copyright`)

- `BSD-3-Clause`
- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris dash=0.5.12-12
'http://deb.debian.org/debian/pool/main/d/dash/dash_0.5.12-12.dsc' dash_0.5.12-12.dsc 1460 SHA256:589efc4d87a4ae4745c273bdb33198d7c4f28a71736a8ece81d3677cf9c6e5ce
'http://deb.debian.org/debian/pool/main/d/dash/dash_0.5.12.orig.tar.gz' dash_0.5.12.orig.tar.gz 246054 SHA256:6a474ac46e8b0b32916c4c60df694c82058d3297d8b385b74508030ca4a8f28a
'http://deb.debian.org/debian/pool/main/d/dash/dash_0.5.12-12.debian.tar.xz' dash_0.5.12-12.debian.tar.xz 47300 SHA256:a278acb5d9a1f5d9a086d36a547287cbf3105b8f33c0e62d86d264decf5ba1ad
```

Other potentially useful URLs:

- https://sources.debian.net/src/dash/0.5.12-12/ (for browsing the source)
- https://sources.debian.net/src/dash/0.5.12-12/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/dash/0.5.12-12/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `db5.3=5.3.28+dfsg2-11`

Binary Packages:

- `libdb5.3t64:amd64=5.3.28+dfsg2-11+b1`

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
$ apt-get source -qq --print-uris db5.3=5.3.28+dfsg2-11
'http://deb.debian.org/debian/pool/main/d/db5.3/db5.3_5.3.28%2bdfsg2-11.dsc' db5.3_5.3.28+dfsg2-11.dsc 2032 SHA256:0550eb464a02703e35d86fbc4a7ac0736ab30b2a0ebe0818c490f7106d1d4230
'http://deb.debian.org/debian/pool/main/d/db5.3/db5.3_5.3.28%2bdfsg2.orig.tar.xz' db5.3_5.3.28+dfsg2.orig.tar.xz 21287688 SHA256:ad41b507415dec8316e828b2230242af2251d2c86eefa3c7aa9ef47c5239ef33
'http://deb.debian.org/debian/pool/main/d/db5.3/db5.3_5.3.28%2bdfsg2-11.debian.tar.xz' db5.3_5.3.28+dfsg2-11.debian.tar.xz 36580 SHA256:701601b7398c1ff8714594287db6c042b2cbc2e15bc98e85afd77c4324d3e3aa
```

Other potentially useful URLs:

- https://sources.debian.net/src/db5.3/5.3.28+dfsg2-11/ (for browsing the source)
- https://sources.debian.net/src/db5.3/5.3.28+dfsg2-11/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/db5.3/5.3.28+dfsg2-11/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `debconf=1.5.92`

Binary Packages:

- `debconf=1.5.92`

Licenses: (parsed from: `/usr/share/doc/debconf/copyright`)

- `BSD-2-clause`

Source:

```console
$ apt-get source -qq --print-uris debconf=1.5.92
'http://deb.debian.org/debian/pool/main/d/debconf/debconf_1.5.92.dsc' debconf_1.5.92.dsc 2202 SHA256:612d1b51713fc95b205b5f222af036b1541b13734e1f183a3f37e637eda187a9
'http://deb.debian.org/debian/pool/main/d/debconf/debconf_1.5.92.tar.xz' debconf_1.5.92.tar.xz 610068 SHA256:72265cb0315c0cc58a0d5abf0c032ffac2d071c8ba05bf830f9e0e73ca8ab219
```

Other potentially useful URLs:

- https://sources.debian.net/src/debconf/1.5.92/ (for browsing the source)
- https://sources.debian.net/src/debconf/1.5.92/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/debconf/1.5.92/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `debian-archive-keyring=2025.1`

Binary Packages:

- `debian-archive-keyring=2025.1`

Licenses: (parsed from: `/usr/share/doc/debian-archive-keyring/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris debian-archive-keyring=2025.1
'http://deb.debian.org/debian/pool/main/d/debian-archive-keyring/debian-archive-keyring_2025.1.dsc' debian-archive-keyring_2025.1.dsc 1267 SHA256:09604bd8d4562a1e942e5d1a19a6b82447cbdeb2e7c7f0df7c32a2503647ea47
'http://deb.debian.org/debian/pool/main/d/debian-archive-keyring/debian-archive-keyring_2025.1.tar.xz' debian-archive-keyring_2025.1.tar.xz 138248 SHA256:2d019c3fa19c42da4d37571e473c296286dad0214cb3bd5cafd99f04a8bf5471
```

Other potentially useful URLs:

- https://sources.debian.net/src/debian-archive-keyring/2025.1/ (for browsing the source)
- https://sources.debian.net/src/debian-archive-keyring/2025.1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/debian-archive-keyring/2025.1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `debianutils=5.23.2`

Binary Packages:

- `debianutils=5.23.2`

Licenses: (parsed from: `/usr/share/doc/debianutils/copyright`)

- `GPL-2`
- `GPL-2+`
- `SMAIL-GPL`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris debianutils=5.23.2
'http://deb.debian.org/debian/pool/main/d/debianutils/debianutils_5.23.2.dsc' debianutils_5.23.2.dsc 1908 SHA256:471b65deec232bb033f3e3e06d5bf64dac0ced474c6fd61d41538f3f3de876f8
'http://deb.debian.org/debian/pool/main/d/debianutils/debianutils_5.23.2.tar.xz' debianutils_5.23.2.tar.xz 82376 SHA256:79e524b7526dba2ec5c409d0ee52ebec135815cf5b2907375d444122e0594b69
```

Other potentially useful URLs:

- https://sources.debian.net/src/debianutils/5.23.2/ (for browsing the source)
- https://sources.debian.net/src/debianutils/5.23.2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/debianutils/5.23.2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `diffutils=1:3.12-1`

Binary Packages:

- `diffutils=1:3.12-1`

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
$ apt-get source -qq --print-uris diffutils=1:3.12-1
'http://deb.debian.org/debian/pool/main/d/diffutils/diffutils_3.12-1.dsc' diffutils_3.12-1.dsc 1875 SHA256:eb99be6cc60e71249bd119dfb66ada6a8c0fdd2e1bb8b1325f4801b813ad820c
'http://deb.debian.org/debian/pool/main/d/diffutils/diffutils_3.12.orig.tar.xz' diffutils_3.12.orig.tar.xz 1938800 SHA256:7c8b7f9fc8609141fdea9cece85249d308624391ff61dedaf528fcb337727dfd
'http://deb.debian.org/debian/pool/main/d/diffutils/diffutils_3.12.orig.tar.xz.asc' diffutils_3.12.orig.tar.xz.asc 833 SHA256:ad05b321b2f23441275af68072123a5907b05ad989335a9f1f6e3781cb0846a6
'http://deb.debian.org/debian/pool/main/d/diffutils/diffutils_3.12-1.debian.tar.xz' diffutils_3.12-1.debian.tar.xz 14752 SHA256:ffacb3eb9ad1a8cc90768e13e1d09da1b71cfab3cb99b1e0bd1f0ba26f89dd46
```

Other potentially useful URLs:

- https://sources.debian.net/src/diffutils/1:3.12-1/ (for browsing the source)
- https://sources.debian.net/src/diffutils/1:3.12-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/diffutils/1:3.12-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `dpkg=1.23.7`

Binary Packages:

- `dpkg=1.23.7`

Licenses: (parsed from: `/usr/share/doc/dpkg/copyright`)

- `GPL-2`
- `GPL-2+`
- `public-domain-s-s-d`

Source:

```console
$ apt-get source -qq --print-uris dpkg=1.23.7
'http://deb.debian.org/debian/pool/main/d/dpkg/dpkg_1.23.7.dsc' dpkg_1.23.7.dsc 3474 SHA256:1b1013edd98d1ef7b0d7c943f8a57a4cfffb6d54e8d1e00bda36f34f5aaeca83
'http://deb.debian.org/debian/pool/main/d/dpkg/dpkg_1.23.7.tar.xz' dpkg_1.23.7.tar.xz 5836724 SHA256:60fe2be72e5f0a4bb0ac7baff3b1697ebc5cfaac1885f66649521571a97440ad
```

Other potentially useful URLs:

- https://sources.debian.net/src/dpkg/1.23.7/ (for browsing the source)
- https://sources.debian.net/src/dpkg/1.23.7/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/dpkg/1.23.7/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `e2fsprogs=1.47.4-1`

Binary Packages:

- `libcom-err2:amd64=1.47.4-1`

Licenses: (parsed from: `/usr/share/doc/libcom-err2/copyright`)

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
$ apt-get source -qq --print-uris e2fsprogs=1.47.4-1
'http://deb.debian.org/debian/pool/main/e/e2fsprogs/e2fsprogs_1.47.4-1.dsc' e2fsprogs_1.47.4-1.dsc 3138 SHA256:3101f69bfafa37124a9e2238107324e899ac7c88760b542fe416962ae4569c0c
'http://deb.debian.org/debian/pool/main/e/e2fsprogs/e2fsprogs_1.47.4.orig.tar.gz' e2fsprogs_1.47.4.orig.tar.gz 10106395 SHA256:2cec05f39c20ee621f14926195664e66e6017190ac8e4bbdb16d86082e43c5da
'http://deb.debian.org/debian/pool/main/e/e2fsprogs/e2fsprogs_1.47.4.orig.tar.gz.asc' e2fsprogs_1.47.4.orig.tar.gz.asc 488 SHA256:c5a4b6cbf8e57dd83d239b23f5e847ed32bedab005d90e3334889b0662383ac7
'http://deb.debian.org/debian/pool/main/e/e2fsprogs/e2fsprogs_1.47.4-1.debian.tar.xz' e2fsprogs_1.47.4-1.debian.tar.xz 94496 SHA256:a288244fa6d7e1bbe11526417772e0c41b494e78372bbe275bd86aa8fdd6776c
```

Other potentially useful URLs:

- https://sources.debian.net/src/e2fsprogs/1.47.4-1/ (for browsing the source)
- https://sources.debian.net/src/e2fsprogs/1.47.4-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/e2fsprogs/1.47.4-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `expat=2.8.0-1`

Binary Packages:

- `libexpat1:amd64=2.8.0-1`

Licenses: (parsed from: `/usr/share/doc/libexpat1/copyright`)

- `MIT`

Source:

```console
$ apt-get source -qq --print-uris expat=2.8.0-1
'http://deb.debian.org/debian/pool/main/e/expat/expat_2.8.0-1.dsc' expat_2.8.0-1.dsc 1970 SHA256:db9e0413b7ad34bcdd63045b76144d7ee4ed423f09dbb20009138b46fead942e
'http://deb.debian.org/debian/pool/main/e/expat/expat_2.8.0.orig.tar.gz' expat_2.8.0.orig.tar.gz 8454954 SHA256:b6cfb7fee2d674587d94899d1f2dc039a7cbb65d167f0ba601d0b73a58f9db9e
'http://deb.debian.org/debian/pool/main/e/expat/expat_2.8.0-1.debian.tar.xz' expat_2.8.0-1.debian.tar.xz 13604 SHA256:fb3074f1e9ddcb0757a3c9c479edfa5c1f4cdfbbbab121d0a12971c9fa42927a
```

Other potentially useful URLs:

- https://sources.debian.net/src/expat/2.8.0-1/ (for browsing the source)
- https://sources.debian.net/src/expat/2.8.0-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/expat/2.8.0-1/ (for access to the source package after it no longer exists in the archive)

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/findutils/4.10.0-3/


### `dpkg` source package: `gcc-16=16-20260322-1`

Binary Packages:

- `gcc-16-base:amd64=16-20260322-1`
- `libgcc-s1:amd64=16-20260322-1`
- `libstdc++6:amd64=16-20260322-1`

Licenses: (parsed from: `/usr/share/doc/gcc-16-base/copyright`, `/usr/share/doc/libgcc-s1/copyright`, `/usr/share/doc/libstdc++6/copyright`)

- `Apache-2.0`
- `Artistic`
- `GFDL-1.2`
- `GPL`
- `GPL-3`
- `LGPL`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/gcc-16/16-20260322-1/


### `dpkg` source package: `gdbm=1.26-1`

Binary Packages:

- `libgdbm-compat4t64:amd64=1.26-1+b2`
- `libgdbm6t64:amd64=1.26-1+b2`

Licenses: (parsed from: `/usr/share/doc/libgdbm-compat4t64/copyright`, `/usr/share/doc/libgdbm6t64/copyright`)

- `GFDL-NIV-1.3+`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris gdbm=1.26-1
'http://deb.debian.org/debian/pool/main/g/gdbm/gdbm_1.26-1.dsc' gdbm_1.26-1.dsc 2234 SHA256:ba4b64d1275f986b40ca13e31ebef34e00e0c3227cfdc904fe4d84973af6a22b
'http://deb.debian.org/debian/pool/main/g/gdbm/gdbm_1.26.orig.tar.gz' gdbm_1.26.orig.tar.gz 1226591 SHA256:6a24504a14de4a744103dcb936be976df6fbe88ccff26065e54c1c47946f4a5e
'http://deb.debian.org/debian/pool/main/g/gdbm/gdbm_1.26-1.debian.tar.xz' gdbm_1.26-1.debian.tar.xz 16832 SHA256:3d358964671e794485be3b567751701061c5e46328ec303512ab26dfe246699d
```

Other potentially useful URLs:

- https://sources.debian.net/src/gdbm/1.26-1/ (for browsing the source)
- https://sources.debian.net/src/gdbm/1.26-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/gdbm/1.26-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `git=1:2.53.0-1`

Binary Packages:

- `git=1:2.53.0-1`
- `git-man=1:2.53.0-1`

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
- `dlmalloc`
- `mingw-runtime`

Source:

```console
$ apt-get source -qq --print-uris git=1:2.53.0-1
'http://deb.debian.org/debian/pool/main/g/git/git_2.53.0-1.dsc' git_2.53.0-1.dsc 2641 SHA256:26a8143dec60feb7c32c2121c6a7ca9c95ad9f673b818e0977469632da6ac4e2
'http://deb.debian.org/debian/pool/main/g/git/git_2.53.0.orig.tar.xz' git_2.53.0.orig.tar.xz 7993096 SHA256:5818bd7d80b061bbbdfec8a433d609dc8818a05991f731ffc4a561e2ca18c653
'http://deb.debian.org/debian/pool/main/g/git/git_2.53.0-1.debian.tar.xz' git_2.53.0-1.debian.tar.xz 832236 SHA256:fa73e2990d9f4d24ade7fc1ac9ac838abd6070caf7d3a57a446dd6ad1f20e7a2
```

Other potentially useful URLs:

- https://sources.debian.net/src/git/1:2.53.0-1/ (for browsing the source)
- https://sources.debian.net/src/git/1:2.53.0-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/git/1:2.53.0-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `glibc=2.42-15`

Binary Packages:

- `libc-bin=2.42-15`
- `libc-gconv-modules-extra:amd64=2.42-15`
- `libc6:amd64=2.42-15`

Licenses: (parsed from: `/usr/share/doc/libc-bin/copyright`, `/usr/share/doc/libc-gconv-modules-extra/copyright`, `/usr/share/doc/libc6/copyright`)

- `BSD-2-clause`
- `BSD-3-clause-Berkeley`
- `BSD-3-clause-Carnegie`
- `BSD-3-clause-Oracle`
- `BSD-3-clause-WIDE`
- `BSD-like-Spencer`
- `BSL-1.0`
- `CORE-MATH`
- `Carnegie`
- `DEC`
- `FSFAP`
- `GPL-2`
- `GPL-2+`
- `GPL-2+-with-link-exception`
- `GPL-3`
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
- `MIT-like-Lord`
- `PCRE`
- `SunPro`
- `Unicode-DFS-2016`
- `Univ-Coimbra`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris glibc=2.42-15
'http://deb.debian.org/debian/pool/main/g/glibc/glibc_2.42-15.dsc' glibc_2.42-15.dsc 8576 SHA256:f6383657608ce3465b2ea97fc6ba0749608f64045d67a1940b901f241d5065bc
'http://deb.debian.org/debian/pool/main/g/glibc/glibc_2.42.orig.tar.xz' glibc_2.42.orig.tar.xz 21052916 SHA256:69c1e915c8edd75981cbfc6b7654e8fc4e52a48d06b9f706f463492749a9b6fb
'http://deb.debian.org/debian/pool/main/g/glibc/glibc_2.42-15.debian.tar.xz' glibc_2.42-15.debian.tar.xz 439876 SHA256:4407a21be5854ca5f1f17c550a6b8586ef134f6eaaf0e6bc078435b468108c61
```

Other potentially useful URLs:

- https://sources.debian.net/src/glibc/2.42-15/ (for browsing the source)
- https://sources.debian.net/src/glibc/2.42-15/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/glibc/2.42-15/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `gmp=2:6.3.0+dfsg-5`

Binary Packages:

- `libgmp10:amd64=2:6.3.0+dfsg-5+b2`

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
$ apt-get source -qq --print-uris gmp=2:6.3.0+dfsg-5
'http://deb.debian.org/debian/pool/main/g/gmp/gmp_6.3.0%2bdfsg-5.dsc' gmp_6.3.0+dfsg-5.dsc 2230 SHA256:609cad99ebddece1d7028a9c3f0a728c68e5a5fbb15b879a2ea6107ea5b16168
'http://deb.debian.org/debian/pool/main/g/gmp/gmp_6.3.0%2bdfsg.orig.tar.xz' gmp_6.3.0+dfsg.orig.tar.xz 1870556 SHA256:bd2966e6d277f79328e894a5a9f3ba3fbf2ed2be81def5f48623e30c23fb1572
'http://deb.debian.org/debian/pool/main/g/gmp/gmp_6.3.0%2bdfsg-5.debian.tar.xz' gmp_6.3.0+dfsg-5.debian.tar.xz 20424 SHA256:9a41837b2e2678506c24c2791d3f551fdb61bb01cc5e79aaaf45c68a8f26089a
```

Other potentially useful URLs:

- https://sources.debian.net/src/gmp/2:6.3.0+dfsg-5/ (for browsing the source)
- https://sources.debian.net/src/gmp/2:6.3.0+dfsg-5/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/gmp/2:6.3.0+dfsg-5/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `gnupg2=2.4.9-4`

Binary Packages:

- `dirmngr=2.4.9-4`
- `gnupg=2.4.9-4`
- `gnupg-l10n=2.4.9-4`
- `gpg=2.4.9-4`
- `gpg-agent=2.4.9-4`
- `gpgconf=2.4.9-4`
- `gpgsm=2.4.9-4`

Licenses: (parsed from: `/usr/share/doc/dirmngr/copyright`, `/usr/share/doc/gnupg/copyright`, `/usr/share/doc/gnupg-l10n/copyright`, `/usr/share/doc/gpg/copyright`, `/usr/share/doc/gpg-agent/copyright`, `/usr/share/doc/gpgconf/copyright`, `/usr/share/doc/gpgsm/copyright`)

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
$ apt-get source -qq --print-uris gnupg2=2.4.9-4
'http://deb.debian.org/debian/pool/main/g/gnupg2/gnupg2_2.4.9-4.dsc' gnupg2_2.4.9-4.dsc 5467 SHA256:2e30a046b44729561cfe7805e66d6ab0d1c1aa583f90570e5429c6bb0c9cecbf
'http://deb.debian.org/debian/pool/main/g/gnupg2/gnupg2_2.4.9.orig.tar.bz2' gnupg2_2.4.9.orig.tar.bz2 8086407 SHA256:dd17ab2e9a04fd79d39d853f599cbc852062ddb9ab52a4ddeb4176fd8b302964
'http://deb.debian.org/debian/pool/main/g/gnupg2/gnupg2_2.4.9.orig.tar.bz2.asc' gnupg2_2.4.9.orig.tar.bz2.asc 265 SHA256:92e5f835c9d7d3b762e8bdc4ed05d705b19138b0097be3ed98eeedce356393e6
'http://deb.debian.org/debian/pool/main/g/gnupg2/gnupg2_2.4.9-4.debian.tar.xz' gnupg2_2.4.9-4.debian.tar.xz 104800 SHA256:3314f2d7271e98901d6a9680013f03c57ffbeb62186d12d479a01bd360c48a85
```

Other potentially useful URLs:

- https://sources.debian.net/src/gnupg2/2.4.9-4/ (for browsing the source)
- https://sources.debian.net/src/gnupg2/2.4.9-4/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/gnupg2/2.4.9-4/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `gnutls28=3.8.12-3`

Binary Packages:

- `libgnutls30t64:amd64=3.8.12-3`

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
- `MIT OR Unlicense`
- `The main library is licensed under GNU Lesser`

Source:

```console
$ apt-get source -qq --print-uris gnutls28=3.8.12-3
'http://deb.debian.org/debian/pool/main/g/gnutls28/gnutls28_3.8.12-3.dsc' gnutls28_3.8.12-3.dsc 3067 SHA256:49816fe7e27ac71df2a3c629c0834daa72da22a08821e1c9c95d18e99fd0d0a1
'http://deb.debian.org/debian/pool/main/g/gnutls28/gnutls28_3.8.12.orig.tar.xz' gnutls28_3.8.12.orig.tar.xz 6949604 SHA256:a7b341421bfd459acf7a374ca4af3b9e06608dcd7bd792b2bf470bea012b8e51
'http://deb.debian.org/debian/pool/main/g/gnutls28/gnutls28_3.8.12.orig.tar.xz.asc' gnutls28_3.8.12.orig.tar.xz.asc 996 SHA256:7a70d4071502974666f2f661e4ab06ba06076efd20468e4198f5f09c7ace41e2
'http://deb.debian.org/debian/pool/main/g/gnutls28/gnutls28_3.8.12-3.debian.tar.xz' gnutls28_3.8.12-3.debian.tar.xz 173324 SHA256:b331186c32e99ec8fc6fbd29b26f8bbae73863fad3efc8dbec9c83a21a748eb8
```

Other potentially useful URLs:

- https://sources.debian.net/src/gnutls28/3.8.12-3/ (for browsing the source)
- https://sources.debian.net/src/gnutls28/3.8.12-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/gnutls28/3.8.12-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `grep=3.12-1`

Binary Packages:

- `grep=3.12-1`

Licenses: (parsed from: `/usr/share/doc/grep/copyright`)

- `BSD-3-clause`
- `FSFAP`
- `FSFUL`
- `FSFULLR`
- `FSFULLR and/or GPL and/or LGPL`
- `GFDL-1.3`
- `GFDL-1.3+`
- `GPL`
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
- `X11`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris grep=3.12-1
'http://deb.debian.org/debian/pool/main/g/grep/grep_3.12-1.dsc' grep_3.12-1.dsc 1647 SHA256:ce35486482abc0591a00be0848c90a3f40ce14b62e501da637296d23bc4c29f4
'http://deb.debian.org/debian/pool/main/g/grep/grep_3.12.orig.tar.xz' grep_3.12.orig.tar.xz 1918448 SHA256:2649b27c0e90e632eadcd757be06c6e9a4f48d941de51e7c0f83ff76408a07b9
'http://deb.debian.org/debian/pool/main/g/grep/grep_3.12.orig.tar.xz.asc' grep_3.12.orig.tar.xz.asc 833 SHA256:62d4867d7cfff57a364b745866d798958a90286551fdf45d08df515fa8c79c25
'http://deb.debian.org/debian/pool/main/g/grep/grep_3.12-1.debian.tar.xz' grep_3.12-1.debian.tar.xz 24160 SHA256:5baef65e599c41285a0393c1c6845c03c9b29f14765447911a1871a50321fd42
```

Other potentially useful URLs:

- https://sources.debian.net/src/grep/3.12-1/ (for browsing the source)
- https://sources.debian.net/src/grep/3.12-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/grep/3.12-1/ (for access to the source package after it no longer exists in the archive)

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

### `dpkg` source package: `init-system-helpers=1.69`

Binary Packages:

- `init-system-helpers=1.69`

Licenses: (parsed from: `/usr/share/doc/init-system-helpers/copyright`)

- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris init-system-helpers=1.69
'http://deb.debian.org/debian/pool/main/i/init-system-helpers/init-system-helpers_1.69.dsc' init-system-helpers_1.69.dsc 2234 SHA256:99b681c969728fba085226b1d1fd25cc37c9fe16f9eb5118e679d845b50ae7ee
'http://deb.debian.org/debian/pool/main/i/init-system-helpers/init-system-helpers_1.69.tar.xz' init-system-helpers_1.69.tar.xz 45648 SHA256:e246ee7f39b110803e5307fdb25ec2fb5fe0c62dbd9274011803fef50af08100
```

Other potentially useful URLs:

- https://sources.debian.net/src/init-system-helpers/1.69/ (for browsing the source)
- https://sources.debian.net/src/init-system-helpers/1.69/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/init-system-helpers/1.69/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `keyutils=1.6.3-6`

Binary Packages:

- `libkeyutils1:amd64=1.6.3-6+b2`

Licenses: (parsed from: `/usr/share/doc/libkeyutils1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2`
- `LGPL-2+`

Source:

```console
$ apt-get source -qq --print-uris keyutils=1.6.3-6
'http://deb.debian.org/debian/pool/main/k/keyutils/keyutils_1.6.3-6.dsc' keyutils_1.6.3-6.dsc 2100 SHA256:e63869474c390d5d5bdee8492f7b2f4d6034ff10d8190da18593620c0f35fbf8
'http://deb.debian.org/debian/pool/main/k/keyutils/keyutils_1.6.3.orig.tar.gz' keyutils_1.6.3.orig.tar.gz 137022 SHA256:a61d5706136ae4c05bd48f86186bcfdbd88dd8bd5107e3e195c924cfc1b39bb4
'http://deb.debian.org/debian/pool/main/k/keyutils/keyutils_1.6.3-6.debian.tar.xz' keyutils_1.6.3-6.debian.tar.xz 16588 SHA256:6fc3c1217b8e92df9dff73e4919c45dff4ada5fd414ab57329af487f4476466a
```

Other potentially useful URLs:

- https://sources.debian.net/src/keyutils/1.6.3-6/ (for browsing the source)
- https://sources.debian.net/src/keyutils/1.6.3-6/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/keyutils/1.6.3-6/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `krb5=1.22.1-2`

Binary Packages:

- `libgssapi-krb5-2:amd64=1.22.1-2+b1`
- `libk5crypto3:amd64=1.22.1-2+b1`
- `libkrb5-3:amd64=1.22.1-2+b1`
- `libkrb5support0:amd64=1.22.1-2+b1`

Licenses: (parsed from: `/usr/share/doc/libgssapi-krb5-2/copyright`, `/usr/share/doc/libk5crypto3/copyright`, `/usr/share/doc/libkrb5-3/copyright`, `/usr/share/doc/libkrb5support0/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris krb5=1.22.1-2
'http://deb.debian.org/debian/pool/main/k/krb5/krb5_1.22.1-2.dsc' krb5_1.22.1-2.dsc 3378 SHA256:2f6e27442ee93856cdb52cf87050b7c2447239c2ad4e30da8a6d8972ac862c2d
'http://deb.debian.org/debian/pool/main/k/krb5/krb5_1.22.1.orig.tar.gz' krb5_1.22.1.orig.tar.gz 8747101 SHA256:1a8832b8cad923ebbf1394f67e2efcf41e3a49f460285a66e35adec8fa0053af
'http://deb.debian.org/debian/pool/main/k/krb5/krb5_1.22.1.orig.tar.gz.asc' krb5_1.22.1.orig.tar.gz.asc 833 SHA256:598334b7b54f63a2280f72cc566bee6f9cbc5ef4dcd9ccabd3a0460641908a64
'http://deb.debian.org/debian/pool/main/k/krb5/krb5_1.22.1-2.debian.tar.xz' krb5_1.22.1-2.debian.tar.xz 102864 SHA256:6256a11c4dec6ec9897fb6aee006a14cb13cfe89dc4e66cc9cfc3ed31294c59c
```

Other potentially useful URLs:

- https://sources.debian.net/src/krb5/1.22.1-2/ (for browsing the source)
- https://sources.debian.net/src/krb5/1.22.1-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/krb5/1.22.1-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libassuan=3.0.2-2`

Binary Packages:

- `libassuan9:amd64=3.0.2-2+b2`

Licenses: (parsed from: `/usr/share/doc/libassuan9/copyright`)

- `FSFULLR`
- `FSFULLRWD`
- `GPL-2`
- `GPL-2+ with Autoconf-data exception`
- `GPL-2+ with Libtool exception`
- `GPL-2.with.nonstandard.Autoconf-data.exception`
- `GPL-3`
- `GPL-3+`
- `GPL-3+ with Autoconf-2.0~Archive exception`
- `GPL-3+ with Autoconf-data exception`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`
- `LGPL-3+`
- `X11`

Source:

```console
$ apt-get source -qq --print-uris libassuan=3.0.2-2
'http://deb.debian.org/debian/pool/main/liba/libassuan/libassuan_3.0.2-2.dsc' libassuan_3.0.2-2.dsc 2682 SHA256:4c6b68814cef421d1768628b401a62176c579dc8e1e3026348d7ec159943f0c7
'http://deb.debian.org/debian/pool/main/liba/libassuan/libassuan_3.0.2.orig.tar.bz2' libassuan_3.0.2.orig.tar.bz2 593917 SHA256:d2931cdad266e633510f9970e1a2f346055e351bb19f9b78912475b8074c36f6
'http://deb.debian.org/debian/pool/main/liba/libassuan/libassuan_3.0.2.orig.tar.bz2.asc' libassuan_3.0.2.orig.tar.bz2.asc 228 SHA256:3799b287fd7d48f750597bd9104621d2cbafd508de83303b1a5f5eef08f06072
'http://deb.debian.org/debian/pool/main/liba/libassuan/libassuan_3.0.2-2.debian.tar.xz' libassuan_3.0.2-2.debian.tar.xz 17536 SHA256:05566fa4ac35ad6af7214ce01beeaffcc2ce1c13d20daac4cf86949c5fad25fc
```

Other potentially useful URLs:

- https://sources.debian.net/src/libassuan/3.0.2-2/ (for browsing the source)
- https://sources.debian.net/src/libassuan/3.0.2-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libassuan/3.0.2-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libbsd=0.12.2-2`

Binary Packages:

- `libbsd0:amd64=0.12.2-2+b2`

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

### `dpkg` source package: `libcap-ng=0.9.3-1`

Binary Packages:

- `libcap-ng0:amd64=0.9.3-1`

Licenses: (parsed from: `/usr/share/doc/libcap-ng0/copyright`)

- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris libcap-ng=0.9.3-1
'http://deb.debian.org/debian/pool/main/libc/libcap-ng/libcap-ng_0.9.3-1.dsc' libcap-ng_0.9.3-1.dsc 1743 SHA256:e7bbe42ea125011af00093a987a366a415f64cd8eb048bd77efa7aefe3745082
'http://deb.debian.org/debian/pool/main/libc/libcap-ng/libcap-ng_0.9.3.orig.tar.gz' libcap-ng_0.9.3.orig.tar.gz 126269 SHA256:bbdc4e114409877e358a2775db7441ca207f0f999f434c99f7327829ad1eaeb3
'http://deb.debian.org/debian/pool/main/libc/libcap-ng/libcap-ng_0.9.3-1.debian.tar.xz' libcap-ng_0.9.3-1.debian.tar.xz 7584 SHA256:7306445819e307017a8520b122a94df5e82c3978d1458b19649a209541917a2f
```

Other potentially useful URLs:

- https://sources.debian.net/src/libcap-ng/0.9.3-1/ (for browsing the source)
- https://sources.debian.net/src/libcap-ng/0.9.3-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libcap-ng/0.9.3-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libcbor=0.10.2-2.1`

Binary Packages:

- `libcbor0.10:amd64=0.10.2-2.1+b1`

Licenses: (parsed from: `/usr/share/doc/libcbor0.10/copyright`)

- `Expat`

Source:

```console
$ apt-get source -qq --print-uris libcbor=0.10.2-2.1
'http://deb.debian.org/debian/pool/main/libc/libcbor/libcbor_0.10.2-2.1.dsc' libcbor_0.10.2-2.1.dsc 2139 SHA256:342d29cb8aa4c4b0cba55d7072c4549eefa7c004939769b26ab4f43fb32daece
'http://deb.debian.org/debian/pool/main/libc/libcbor/libcbor_0.10.2.orig.tar.gz' libcbor_0.10.2.orig.tar.gz 289450 SHA256:e75f712215d7b7e5c89ef322a09b701f7159f028b8b48978865725f00f79875b
'http://deb.debian.org/debian/pool/main/libc/libcbor/libcbor_0.10.2-2.1.debian.tar.xz' libcbor_0.10.2-2.1.debian.tar.xz 6576 SHA256:ec78443d21d15864080d081de0290ee99385b462a063c50c36b61ce09a59fb3e
```

Other potentially useful URLs:

- https://sources.debian.net/src/libcbor/0.10.2-2.1/ (for browsing the source)
- https://sources.debian.net/src/libcbor/0.10.2-2.1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libcbor/0.10.2-2.1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libedit=3.1-20251016-1`

Binary Packages:

- `libedit2:amd64=3.1-20251016-1+b1`

Licenses: (parsed from: `/usr/share/doc/libedit2/copyright`)

- `BSD-3-clause`

Source:

```console
$ apt-get source -qq --print-uris libedit=3.1-20251016-1
'http://deb.debian.org/debian/pool/main/libe/libedit/libedit_3.1-20251016-1.dsc' libedit_3.1-20251016-1.dsc 2264 SHA256:82f4a6ba02d58128414520489537cd73d765c2ed3fb636cc6708f1c576f51bfe
'http://deb.debian.org/debian/pool/main/libe/libedit/libedit_3.1-20251016.orig.tar.gz' libedit_3.1-20251016.orig.tar.gz 549005 SHA256:21362b00653bbfc1c71f71a7578da66b5b5203559d43134d2dd7719e313ce041
'http://deb.debian.org/debian/pool/main/libe/libedit/libedit_3.1-20251016-1.debian.tar.xz' libedit_3.1-20251016-1.debian.tar.xz 16716 SHA256:f4044457a9648f00ea77e79069e0569f47d48c00b310150dcd070de689e4d8ed
```

Other potentially useful URLs:

- https://sources.debian.net/src/libedit/3.1-20251016-1/ (for browsing the source)
- https://sources.debian.net/src/libedit/3.1-20251016-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libedit/3.1-20251016-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `liberror-perl=0.17030-1`

Binary Packages:

- `liberror-perl=0.17030-1`

Licenses: (parsed from: `/usr/share/doc/liberror-perl/copyright`)

- `Artistic`
- `GPL-1`
- `GPL-1+`
- `MIT/X11`

Source:

```console
$ apt-get source -qq --print-uris liberror-perl=0.17030-1
'http://deb.debian.org/debian/pool/main/libe/liberror-perl/liberror-perl_0.17030-1.dsc' liberror-perl_0.17030-1.dsc 2337 SHA256:44590c5e4057ee2b2090b7ca661cdbead886528a2b5b5fa7ae708f8b9c1814bf
'http://deb.debian.org/debian/pool/main/libe/liberror-perl/liberror-perl_0.17030.orig.tar.gz' liberror-perl_0.17030.orig.tar.gz 33488 SHA256:34d382276c0fb0d6b38355b94c96a30b12d834d5662eb53f088ee25e3e712924
'http://deb.debian.org/debian/pool/main/libe/liberror-perl/liberror-perl_0.17030-1.debian.tar.xz' liberror-perl_0.17030-1.debian.tar.xz 4660 SHA256:6824b886f5068d9345279e2425b423fd47623c3ffe74732074b67c5863040ac7
```

Other potentially useful URLs:

- https://sources.debian.net/src/liberror-perl/0.17030-1/ (for browsing the source)
- https://sources.debian.net/src/liberror-perl/0.17030-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/liberror-perl/0.17030-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libffi=3.5.2-4`

Binary Packages:

- `libffi8:amd64=3.5.2-4`

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
$ apt-get source -qq --print-uris libffi=3.5.2-4
'http://deb.debian.org/debian/pool/main/libf/libffi/libffi_3.5.2-4.dsc' libffi_3.5.2-4.dsc 2093 SHA256:537ef63c317c13600feee9398eb5137d5e8e82326330d85252f257c44ab161af
'http://deb.debian.org/debian/pool/main/libf/libffi/libffi_3.5.2.orig.tar.gz' libffi_3.5.2.orig.tar.gz 598870 SHA256:dd19253d3007f366319a51d248a40c9e5fcace4498cbea990b566291844e4e30
'http://deb.debian.org/debian/pool/main/libf/libffi/libffi_3.5.2-4.debian.tar.xz' libffi_3.5.2-4.debian.tar.xz 11000 SHA256:b609c6c98ece9551817d00c570d6ced0553bcf261c4568750ca8be1c95e24177
```

Other potentially useful URLs:

- https://sources.debian.net/src/libffi/3.5.2-4/ (for browsing the source)
- https://sources.debian.net/src/libffi/3.5.2-4/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libffi/3.5.2-4/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libfido2=1.17.0-1`

Binary Packages:

- `libfido2-1:amd64=1.17.0-1`

Licenses: (parsed from: `/usr/share/doc/libfido2-1/copyright`)

- `BSD-2-clause`
- `ISC`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris libfido2=1.17.0-1
'http://deb.debian.org/debian/pool/main/libf/libfido2/libfido2_1.17.0-1.dsc' libfido2_1.17.0-1.dsc 2585 SHA256:d8895d511a6a9fffb19639bea47f27c9dc6a2ad6c2a4c09350034c2e2233a7b8
'http://deb.debian.org/debian/pool/main/libf/libfido2/libfido2_1.17.0.orig.tar.gz' libfido2_1.17.0.orig.tar.gz 714675 SHA256:c1012c8871d71b65872fd5ff1a9d6b0838a55683a03e85ba97479ce57129c736
'http://deb.debian.org/debian/pool/main/libf/libfido2/libfido2_1.17.0.orig.tar.gz.asc' libfido2_1.17.0.orig.tar.gz.asc 228 SHA256:7ae37a23c2152d5d0760e4a2518c1718da23c3c76f73124aead6a1a2fe00f4da
'http://deb.debian.org/debian/pool/main/libf/libfido2/libfido2_1.17.0-1.debian.tar.xz' libfido2_1.17.0-1.debian.tar.xz 68776 SHA256:ec214814a5c797091679d866bfb4aa24efda604bb8f969e387c0796dc266b3bf
```

Other potentially useful URLs:

- https://sources.debian.net/src/libfido2/1.17.0-1/ (for browsing the source)
- https://sources.debian.net/src/libfido2/1.17.0-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libfido2/1.17.0-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libgcrypt20=1.12.2-1`

Binary Packages:

- `libgcrypt20:amd64=1.12.2-1`

Licenses: (parsed from: `/usr/share/doc/libgcrypt20/copyright`)

- `GPL-2`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris libgcrypt20=1.12.2-1
'http://deb.debian.org/debian/pool/main/libg/libgcrypt20/libgcrypt20_1.12.2-1.dsc' libgcrypt20_1.12.2-1.dsc 2962 SHA256:84f47a6d056e207c99b7c125f57540a2371b9d0f4753d312befad0e1508a8f9d
'http://deb.debian.org/debian/pool/main/libg/libgcrypt20/libgcrypt20_1.12.2.orig.tar.bz2' libgcrypt20_1.12.2.orig.tar.bz2 4441855 SHA256:7ce33c2492221a0436f96a8500215e9f3e3dcb5fd26a757cd415e7a843babd5e
'http://deb.debian.org/debian/pool/main/libg/libgcrypt20/libgcrypt20_1.12.2.orig.tar.bz2.asc' libgcrypt20_1.12.2.orig.tar.bz2.asc 265 SHA256:8badf1f557b7b24ad5c9b96951c573c4f7b5cdecc7ea017edda00e8c985d25b1
'http://deb.debian.org/debian/pool/main/libg/libgcrypt20/libgcrypt20_1.12.2-1.debian.tar.xz' libgcrypt20_1.12.2-1.debian.tar.xz 39472 SHA256:46614c77c8ea09f230a19291facee4d555acb170f77c1c5758f3dea8b028f1eb
```

Other potentially useful URLs:

- https://sources.debian.net/src/libgcrypt20/1.12.2-1/ (for browsing the source)
- https://sources.debian.net/src/libgcrypt20/1.12.2-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libgcrypt20/1.12.2-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libgpg-error=1.59-4`

Binary Packages:

- `libgpg-error0:amd64=1.59-4`

Licenses: (parsed from: `/usr/share/doc/libgpg-error0/copyright`)

- `BSD-3-clause`
- `GPL-3`
- `GPL-3+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `g10-permissive`

Source:

```console
$ apt-get source -qq --print-uris libgpg-error=1.59-4
'http://deb.debian.org/debian/pool/main/libg/libgpg-error/libgpg-error_1.59-4.dsc' libgpg-error_1.59-4.dsc 2961 SHA256:a1a15efae74a417197e5fb384597e59afb9f127bc6d5eab7365fdb2089221028
'http://deb.debian.org/debian/pool/main/libg/libgpg-error/libgpg-error_1.59.orig.tar.bz2' libgpg-error_1.59.orig.tar.bz2 1123184 SHA256:a19bc5087fd97026d93cb4b45d51638d1a25202a5e1fbc3905799f424cfa6134
'http://deb.debian.org/debian/pool/main/libg/libgpg-error/libgpg-error_1.59.orig.tar.bz2.asc' libgpg-error_1.59.orig.tar.bz2.asc 265 SHA256:5d926335325ad13ec80ab0c0c3385357a84b6b1c7123b3c72681a495271dd196
'http://deb.debian.org/debian/pool/main/libg/libgpg-error/libgpg-error_1.59-4.debian.tar.xz' libgpg-error_1.59-4.debian.tar.xz 20040 SHA256:b058494a61a1361fcbeab5d81b07afa4750440f51b751066f16ecf8576d005d0
```

Other potentially useful URLs:

- https://sources.debian.net/src/libgpg-error/1.59-4/ (for browsing the source)
- https://sources.debian.net/src/libgpg-error/1.59-4/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libgpg-error/1.59-4/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libidn2=2.3.8-4`

Binary Packages:

- `libidn2-0:amd64=2.3.8-4+b2`

Licenses: (parsed from: `/usr/share/doc/libidn2-0/copyright`)

- `Expat`
- `FSFAP`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`
- `LGPL-3+`
- `Unicode`

Source:

```console
$ apt-get source -qq --print-uris libidn2=2.3.8-4
'http://deb.debian.org/debian/pool/main/libi/libidn2/libidn2_2.3.8-4.dsc' libidn2_2.3.8-4.dsc 2811 SHA256:a48a66a00e742b5985db5215dc99d59f5bc257de32ef62f9c71374934cc2ce8d
'http://deb.debian.org/debian/pool/main/libi/libidn2/libidn2_2.3.8.orig.tar.gz' libidn2_2.3.8.orig.tar.gz 718637 SHA256:bbad1678d35d28e2c62e6a2577083829461402d9e47b908791c55314a5cb5e04
'http://deb.debian.org/debian/pool/main/libi/libidn2/libidn2_2.3.8.orig.tar.gz.asc' libidn2_2.3.8.orig.tar.gz.asc 1223 SHA256:8995cab7db361d9d6989eab26d9b521c74236960a5d78250121c8d369b013bd8
'http://deb.debian.org/debian/pool/main/libi/libidn2/libidn2_2.3.8-4.debian.tar.xz' libidn2_2.3.8-4.debian.tar.xz 18116 SHA256:527b1675003a8be38cda322be1f3ba9352687f8d2ba438f0c82a06318848ff83
```

Other potentially useful URLs:

- https://sources.debian.net/src/libidn2/2.3.8-4/ (for browsing the source)
- https://sources.debian.net/src/libidn2/2.3.8-4/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libidn2/2.3.8-4/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libksba=1.6.8-2`

Binary Packages:

- `libksba8:amd64=1.6.8-2`

Licenses: (parsed from: `/usr/share/doc/libksba8/copyright`)

- `FSFUL`
- `GPL-3`
- `LGPL-2.1-or-later`

Source:

```console
$ apt-get source -qq --print-uris libksba=1.6.8-2
'http://deb.debian.org/debian/pool/main/libk/libksba/libksba_1.6.8-2.dsc' libksba_1.6.8-2.dsc 2480 SHA256:6b134b2362e4a9b2ac35d17d6dcc3cbf267b4ebfe5523eb4ebbda10d8686a30a
'http://deb.debian.org/debian/pool/main/libk/libksba/libksba_1.6.8.orig.tar.bz2' libksba_1.6.8.orig.tar.bz2 716917 SHA256:0f4510f1c7a679c3545990a31479f391ad45d84e039176309d42f80cf41743f5
'http://deb.debian.org/debian/pool/main/libk/libksba/libksba_1.6.8.orig.tar.bz2.asc' libksba_1.6.8.orig.tar.bz2.asc 464 SHA256:3358aaf4b8bbbcf7c30b441ee19dcc01a586d9a661b95a7cd2443e103a5f1242
'http://deb.debian.org/debian/pool/main/libk/libksba/libksba_1.6.8-2.debian.tar.xz' libksba_1.6.8-2.debian.tar.xz 14912 SHA256:484d137fe043d8736af9a1dfd22ee19bb3df39c70f36d6144901e5b370f8ae59
```

Other potentially useful URLs:

- https://sources.debian.net/src/libksba/1.6.8-2/ (for browsing the source)
- https://sources.debian.net/src/libksba/1.6.8-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libksba/1.6.8-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libmd=1.1.0-2`

Binary Packages:

- `libmd0:amd64=1.1.0-2+b2`

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

### `dpkg` source package: `libpsl=0.21.5-1`

Binary Packages:

- `libpsl5t64:amd64=0.21.5-1`

Licenses: (parsed from: `/usr/share/doc/libpsl5t64/copyright`)

- `Chromium`
- `MIT`
- `gnulib`

Source:

```console
$ apt-get source -qq --print-uris libpsl=0.21.5-1
'http://deb.debian.org/debian/pool/main/libp/libpsl/libpsl_0.21.5-1.dsc' libpsl_0.21.5-1.dsc 2286 SHA256:92f6579e39b641231bed1d679d491a678e249593b18ff58d9c8685af7aad8529
'http://deb.debian.org/debian/pool/main/libp/libpsl/libpsl_0.21.5.orig.tar.xz' libpsl_0.21.5.orig.tar.xz 2231868 SHA256:e428e8974aabb3bfe5e1ca2a2f8a72fc032d5be709ed43a7d8b48f714c7a5399
'http://deb.debian.org/debian/pool/main/libp/libpsl/libpsl_0.21.5-1.debian.tar.xz' libpsl_0.21.5-1.debian.tar.xz 11308 SHA256:9a48b7982f9bf2a076d2adbfce6cd0623103ef0c9b6aa7f2502eeb99ab47d960
```

Other potentially useful URLs:

- https://sources.debian.net/src/libpsl/0.21.5-1/ (for browsing the source)
- https://sources.debian.net/src/libpsl/0.21.5-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libpsl/0.21.5-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libseccomp=2.6.0-2`

Binary Packages:

- `libseccomp2:amd64=2.6.0-2+b1`

Licenses: (parsed from: `/usr/share/doc/libseccomp2/copyright`)

- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libseccomp=2.6.0-2
'http://deb.debian.org/debian/pool/main/libs/libseccomp/libseccomp_2.6.0-2.dsc' libseccomp_2.6.0-2.dsc 2622 SHA256:d05f94536558d34fa339326c6f958a3357b51efac8234470b5d97b69472db765
'http://deb.debian.org/debian/pool/main/libs/libseccomp/libseccomp_2.6.0.orig.tar.gz' libseccomp_2.6.0.orig.tar.gz 685655 SHA256:83b6085232d1588c379dc9b9cae47bb37407cf262e6e74993c61ba72d2a784dc
'http://deb.debian.org/debian/pool/main/libs/libseccomp/libseccomp_2.6.0.orig.tar.gz.asc' libseccomp_2.6.0.orig.tar.gz.asc 833 SHA256:52e338fa958128293cbd25d2be189e34da41c4f4abbb1b641cf58f373c001f94
'http://deb.debian.org/debian/pool/main/libs/libseccomp/libseccomp_2.6.0-2.debian.tar.xz' libseccomp_2.6.0-2.debian.tar.xz 20800 SHA256:ed705ec85719403e77d004c99c0b06b795f090c66fcae265c4bcf37ffea9cc27
```

Other potentially useful URLs:

- https://sources.debian.net/src/libseccomp/2.6.0-2/ (for browsing the source)
- https://sources.debian.net/src/libseccomp/2.6.0-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libseccomp/2.6.0-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libselinux=3.10-1`

Binary Packages:

- `libselinux1:amd64=3.10-1`

Licenses: (parsed from: `/usr/share/doc/libselinux1/copyright`)

- `GPL-2`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris libselinux=3.10-1
'http://deb.debian.org/debian/pool/main/libs/libselinux/libselinux_3.10-1.dsc' libselinux_3.10-1.dsc 3050 SHA256:60d0f0cabfe5aaf19179307dd81e89d957fae2b5a4f1e950766e14e8a673e6e9
'http://deb.debian.org/debian/pool/main/libs/libselinux/libselinux_3.10.orig.tar.gz' libselinux_3.10.orig.tar.gz 205800 SHA256:1ef216c5b56fb7e0a51cd2909787a175a17ee391e0467894807873539ebe766b
'http://deb.debian.org/debian/pool/main/libs/libselinux/libselinux_3.10.orig.tar.gz.asc' libselinux_3.10.orig.tar.gz.asc 1000 SHA256:39dac0fe73847c0329f59ffe138d7baba193f1edf9fd6d5d226335ef4543c17d
'http://deb.debian.org/debian/pool/main/libs/libselinux/libselinux_3.10-1.debian.tar.xz' libselinux_3.10-1.debian.tar.xz 51700 SHA256:64e32e99debda65bb5c4c761961568e7669b65867df266e199788cd4ea61f7dc
```

Other potentially useful URLs:

- https://sources.debian.net/src/libselinux/3.10-1/ (for browsing the source)
- https://sources.debian.net/src/libselinux/3.10-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libselinux/3.10-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libsemanage=3.10-1`

Binary Packages:

- `libsemanage-common=3.10-1`
- `libsemanage2:amd64=3.10-1`

Licenses: (parsed from: `/usr/share/doc/libsemanage-common/copyright`, `/usr/share/doc/libsemanage2/copyright`)

- `GPL-2`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris libsemanage=3.10-1
'http://deb.debian.org/debian/pool/main/libs/libsemanage/libsemanage_3.10-1.dsc' libsemanage_3.10-1.dsc 2980 SHA256:93d4b9b48d0f55d0a25fb577f96935670c180acfd4312e0f53f8288d73e65bef
'http://deb.debian.org/debian/pool/main/libs/libsemanage/libsemanage_3.10.orig.tar.gz' libsemanage_3.10.orig.tar.gz 185969 SHA256:1978894c414769ad77438d26886eaae3fb7bb74578ef2a5ad3130c89cb5cb1fe
'http://deb.debian.org/debian/pool/main/libs/libsemanage/libsemanage_3.10.orig.tar.gz.asc' libsemanage_3.10.orig.tar.gz.asc 1000 SHA256:0febd7548256966aeec3499dd88d9bdbc053bf4eae088c58e4898adb6de6ce38
'http://deb.debian.org/debian/pool/main/libs/libsemanage/libsemanage_3.10-1.debian.tar.xz' libsemanage_3.10-1.debian.tar.xz 38008 SHA256:d92d4c925abdb45e4c994a1ddb2555ef209e75be05438d38afa1f0de7088cfef
```

Other potentially useful URLs:

- https://sources.debian.net/src/libsemanage/3.10-1/ (for browsing the source)
- https://sources.debian.net/src/libsemanage/3.10-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libsemanage/3.10-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libsepol=3.10-1`

Binary Packages:

- `libsepol2:amd64=3.10-1`

Licenses: (parsed from: `/usr/share/doc/libsepol2/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris libsepol=3.10-1
'http://deb.debian.org/debian/pool/main/libs/libsepol/libsepol_3.10-1.dsc' libsepol_3.10-1.dsc 2385 SHA256:23e8195183bbbcf1afbee620e4b48414a8a4c8eeab12816549893531559d2825
'http://deb.debian.org/debian/pool/main/libs/libsepol/libsepol_3.10.orig.tar.gz' libsepol_3.10.orig.tar.gz 514545 SHA256:d555586797fa9f38344496d2a7ec1147b6caaf3fcc44c42d8d5173edd7a79a71
'http://deb.debian.org/debian/pool/main/libs/libsepol/libsepol_3.10.orig.tar.gz.asc' libsepol_3.10.orig.tar.gz.asc 1000 SHA256:bdd8affcf1f0dbb14e597f5111b07dfe972943f910002034bd1486dde22554ef
'http://deb.debian.org/debian/pool/main/libs/libsepol/libsepol_3.10-1.debian.tar.xz' libsepol_3.10-1.debian.tar.xz 34704 SHA256:a164c14ba168be1b2540513a4bd21fc908f8e7c162a82684f8e0feac1e424ed2
```

Other potentially useful URLs:

- https://sources.debian.net/src/libsepol/3.10-1/ (for browsing the source)
- https://sources.debian.net/src/libsepol/3.10-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libsepol/3.10-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libssh2=1.11.1-2`

Binary Packages:

- `libssh2-1t64:amd64=1.11.1-2`

Licenses: (parsed from: `/usr/share/doc/libssh2-1t64/copyright`)

- `BSD3`
- `ISC`

Source:

```console
$ apt-get source -qq --print-uris libssh2=1.11.1-2
'http://deb.debian.org/debian/pool/main/libs/libssh2/libssh2_1.11.1-2.dsc' libssh2_1.11.1-2.dsc 2329 SHA256:c3e8f28994a2c5607bce880a4ab00ff4bdc1b1004e70dda24e201c0c991dc3b4
'http://deb.debian.org/debian/pool/main/libs/libssh2/libssh2_1.11.1.orig.tar.gz' libssh2_1.11.1.orig.tar.gz 1093012 SHA256:d9ec76cbe34db98eec3539fe2c899d26b0c837cb3eb466a56b0f109cabf658f7
'http://deb.debian.org/debian/pool/main/libs/libssh2/libssh2_1.11.1.orig.tar.gz.asc' libssh2_1.11.1.orig.tar.gz.asc 488 SHA256:f5618c9356a1d5a8059d6cf64015d86547f06b2b8b1f542fbbaf381a736c8075
'http://deb.debian.org/debian/pool/main/libs/libssh2/libssh2_1.11.1-2.debian.tar.xz' libssh2_1.11.1-2.debian.tar.xz 17256 SHA256:98bc79ca01f308924f78e90b47e53d2ce7df1a0e19208d710730f4dfeadea5c5
```

Other potentially useful URLs:

- https://sources.debian.net/src/libssh2/1.11.1-2/ (for browsing the source)
- https://sources.debian.net/src/libssh2/1.11.1-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libssh2/1.11.1-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libtasn1-6=4.21.0-2`

Binary Packages:

- `libtasn1-6:amd64=4.21.0-2+b1`

Licenses: (parsed from: `/usr/share/doc/libtasn1-6/copyright`)

- `GFDL-1.3`
- `GPL-3`
- `LGPL`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libtasn1-6=4.21.0-2
'http://deb.debian.org/debian/pool/main/libt/libtasn1-6/libtasn1-6_4.21.0-2.dsc' libtasn1-6_4.21.0-2.dsc 2665 SHA256:781fb83a70d7e0357e6a70e54e11712b471ba11804e119d621682fc741376a4a
'http://deb.debian.org/debian/pool/main/libt/libtasn1-6/libtasn1-6_4.21.0.orig.tar.gz' libtasn1-6_4.21.0.orig.tar.gz 1816537 SHA256:1d8a444a223cc5464240777346e125de51d8e6abf0b8bac742ac84609167dc87
'http://deb.debian.org/debian/pool/main/libt/libtasn1-6/libtasn1-6_4.21.0.orig.tar.gz.asc' libtasn1-6_4.21.0.orig.tar.gz.asc 1223 SHA256:a81037649b953c9ecb2e8f8fa24cb5c79456fd9af31499d6b753fa6569656807
'http://deb.debian.org/debian/pool/main/libt/libtasn1-6/libtasn1-6_4.21.0-2.debian.tar.xz' libtasn1-6_4.21.0-2.debian.tar.xz 19408 SHA256:baeb1f6c25a1623e6b3834de85e2a69e81b82fdbd5bac9379fc5e699c83d9866
```

Other potentially useful URLs:

- https://sources.debian.net/src/libtasn1-6/4.21.0-2/ (for browsing the source)
- https://sources.debian.net/src/libtasn1-6/4.21.0-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libtasn1-6/4.21.0-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libtext-charwidth-perl=0.04-11`

Binary Packages:

- `libtext-charwidth-perl:amd64=0.04-11+b5`

Licenses: (parsed from: `/usr/share/doc/libtext-charwidth-perl/copyright`)

- `Artistic`
- `GPL-1+`

Source:

```console
$ apt-get source -qq --print-uris libtext-charwidth-perl=0.04-11
'http://deb.debian.org/debian/pool/main/libt/libtext-charwidth-perl/libtext-charwidth-perl_0.04-11.dsc' libtext-charwidth-perl_0.04-11.dsc 2162 SHA256:8a4f6e7a44880f8b4dd8f3dc0c97a39c6fef979f99899de4962c9ccfe84a2577
'http://deb.debian.org/debian/pool/main/libt/libtext-charwidth-perl/libtext-charwidth-perl_0.04.orig.tar.bz2' libtext-charwidth-perl_0.04.orig.tar.bz2 8327 SHA256:2990c13c3f4a5479d7dbc5a94b86c23798cf0dc7df54ffe54e065f072558b6ed
'http://deb.debian.org/debian/pool/main/libt/libtext-charwidth-perl/libtext-charwidth-perl_0.04-11.debian.tar.xz' libtext-charwidth-perl_0.04-11.debian.tar.xz 3016 SHA256:2590d0b6ee7b9cea5396debb96190077210874b4847e844f9eb0d8a4d87ba19c
```

Other potentially useful URLs:

- https://sources.debian.net/src/libtext-charwidth-perl/0.04-11/ (for browsing the source)
- https://sources.debian.net/src/libtext-charwidth-perl/0.04-11/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libtext-charwidth-perl/0.04-11/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libtext-wrapi18n-perl=0.06-10`

Binary Packages:

- `libtext-wrapi18n-perl=0.06-10`

Licenses: (parsed from: `/usr/share/doc/libtext-wrapi18n-perl/copyright`)

- `Artistic`
- `GPL-1`
- `GPL-1+`

Source:

```console
$ apt-get source -qq --print-uris libtext-wrapi18n-perl=0.06-10
'http://deb.debian.org/debian/pool/main/libt/libtext-wrapi18n-perl/libtext-wrapi18n-perl_0.06-10.dsc' libtext-wrapi18n-perl_0.06-10.dsc 1829 SHA256:726c08c23af488c28b70600a5c1632468f1535cb50dcd5255cc153a4f8558ed9
'http://deb.debian.org/debian/pool/main/libt/libtext-wrapi18n-perl/libtext-wrapi18n-perl_0.06.orig.tar.gz' libtext-wrapi18n-perl_0.06.orig.tar.gz 3797 SHA256:432c2a801efe9f12d631124c1163439eac4c99449ba13d80133c45ecacc627f5
'http://deb.debian.org/debian/pool/main/libt/libtext-wrapi18n-perl/libtext-wrapi18n-perl_0.06-10.debian.tar.xz' libtext-wrapi18n-perl_0.06-10.debian.tar.xz 3452 SHA256:751073476ee62cc3430ff0afcab74a4e02b432199d7612e1fd63105fc89ec378
```

Other potentially useful URLs:

- https://sources.debian.net/src/libtext-wrapi18n-perl/0.06-10/ (for browsing the source)
- https://sources.debian.net/src/libtext-wrapi18n-perl/0.06-10/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libtext-wrapi18n-perl/0.06-10/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libunistring=1.4.2-1`

Binary Packages:

- `libunistring5:amd64=1.4.2-1`

Licenses: (parsed from: `/usr/share/doc/libunistring5/copyright`)

- `BSD-3-clause`
- `FSFAP`
- `FSFUL`
- `FSFULLR`
- `GFDL-1.2+`
- `GFDL-1.3+`
- `GPL`
- `GPL-2`
- `GPL-2+`
- `GPL-2+ with Libtool exception`
- `GPL-2+,`
- `GPL-3`
- `GPL-3+`
- `ISC`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`
- `LGPL-3+`
- `Libtool-exception`
- `Unicode-DFS-2016`
- `X11`
- `bsd-3-clause`
- `gfdl-1.2+`
- `gfdl-1.3+`
- `isc`
- `public-domain`
- `unicode-dfs-2016`

Source:

```console
$ apt-get source -qq --print-uris libunistring=1.4.2-1
'http://deb.debian.org/debian/pool/main/libu/libunistring/libunistring_1.4.2-1.dsc' libunistring_1.4.2-1.dsc 2598 SHA256:23db4b46f7068c4100e7932280a18886d42b82577436b552a5f191e2b5fbe377
'http://deb.debian.org/debian/pool/main/libu/libunistring/libunistring_1.4.2.orig.tar.xz' libunistring_1.4.2.orig.tar.xz 2786084 SHA256:5b46e74377ed7409c5b75e7a96f95377b095623b689d8522620927964a41499c
'http://deb.debian.org/debian/pool/main/libu/libunistring/libunistring_1.4.2.orig.tar.xz.asc' libunistring_1.4.2.orig.tar.xz.asc 228 SHA256:45c91e28678c341a925a6b1237711d308249aef29db63d8df0376249ebf67d3b
'http://deb.debian.org/debian/pool/main/libu/libunistring/libunistring_1.4.2-1.debian.tar.xz' libunistring_1.4.2-1.debian.tar.xz 26820 SHA256:63a9396d129024ea6981d9de2dda4f9e5ef550c51a2be585271ce29b4da1325c
```

Other potentially useful URLs:

- https://sources.debian.net/src/libunistring/1.4.2-1/ (for browsing the source)
- https://sources.debian.net/src/libunistring/1.4.2-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libunistring/1.4.2-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libxcrypt=1:4.5.1-1`

Binary Packages:

- `libcrypt1:amd64=1:4.5.1-1+b1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxcrypt=1:4.5.1-1
'http://deb.debian.org/debian/pool/main/libx/libxcrypt/libxcrypt_4.5.1-1.dsc' libxcrypt_4.5.1-1.dsc 2434 SHA256:c9051653fc74d9209e8a3f8b496c359cfecdf7992b0a73f69c090973bae90e4b
'http://deb.debian.org/debian/pool/main/libx/libxcrypt/libxcrypt_4.5.1.orig.tar.xz' libxcrypt_4.5.1.orig.tar.xz 433264 SHA256:bddf278d44e2ecdbf1439a52ddc0bb292921dd9f3013030a2a8461c32a45533f
'http://deb.debian.org/debian/pool/main/libx/libxcrypt/libxcrypt_4.5.1-1.debian.tar.xz' libxcrypt_4.5.1-1.debian.tar.xz 8684 SHA256:b6096f6498adf5a94d727c9065ed33b784190e8c2cd3eda5f073e435708293ae
```

Other potentially useful URLs:

- https://sources.debian.net/src/libxcrypt/1:4.5.1-1/ (for browsing the source)
- https://sources.debian.net/src/libxcrypt/1:4.5.1-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libxcrypt/1:4.5.1-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libzstd=1.5.7+dfsg-3`

Binary Packages:

- `libzstd1:amd64=1.5.7+dfsg-3+b2`

Licenses: (parsed from: `/usr/share/doc/libzstd1/copyright`)

- `BSD-3-clause`
- `Expat`
- `GPL-2`
- `zlib`

Source:

```console
$ apt-get source -qq --print-uris libzstd=1.5.7+dfsg-3
'http://deb.debian.org/debian/pool/main/libz/libzstd/libzstd_1.5.7%2bdfsg-3.dsc' libzstd_1.5.7+dfsg-3.dsc 2490 SHA256:e32b7bb90ac7b312238add6abb77023cec6f59385b1c9a78b41b69ea2ef5001a
'http://deb.debian.org/debian/pool/main/libz/libzstd/libzstd_1.5.7%2bdfsg.orig.tar.xz' libzstd_1.5.7+dfsg.orig.tar.xz 1834780 SHA256:0c092ef267edce57ba7f3f2645c861f72eaf5e76273c6c3632869423464b90a5
'http://deb.debian.org/debian/pool/main/libz/libzstd/libzstd_1.5.7%2bdfsg-3.debian.tar.xz' libzstd_1.5.7+dfsg-3.debian.tar.xz 23164 SHA256:ada18b02a46878f2f0a845fd003179ab9591f7f96f0b984db06a024ab46ae81f
```

Other potentially useful URLs:

- https://sources.debian.net/src/libzstd/1.5.7+dfsg-3/ (for browsing the source)
- https://sources.debian.net/src/libzstd/1.5.7+dfsg-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libzstd/1.5.7+dfsg-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `lz4=1.10.0-10`

Binary Packages:

- `liblz4-1:amd64=1.10.0-10`

Licenses: (parsed from: `/usr/share/doc/liblz4-1/copyright`)

- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris lz4=1.10.0-10
'http://deb.debian.org/debian/pool/main/l/lz4/lz4_1.10.0-10.dsc' lz4_1.10.0-10.dsc 2069 SHA256:eb4cf57b1d20a136ed9fc3f8284a8c676fe93ae96a914df55a5be1c463e28aa5
'http://deb.debian.org/debian/pool/main/l/lz4/lz4_1.10.0.orig.tar.gz' lz4_1.10.0.orig.tar.gz 387114 SHA256:537512904744b35e232912055ccf8ec66d768639ff3abe5788d90d792ec5f48b
'http://deb.debian.org/debian/pool/main/l/lz4/lz4_1.10.0-10.debian.tar.xz' lz4_1.10.0-10.debian.tar.xz 12760 SHA256:2a18bcb82ad51ba330f97eeffe88a27100cc24862e59ec03157d82aa47726518
```

Other potentially useful URLs:

- https://sources.debian.net/src/lz4/1.10.0-10/ (for browsing the source)
- https://sources.debian.net/src/lz4/1.10.0-10/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/lz4/1.10.0-10/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `mawk=1.3.4.20260302-1`

Binary Packages:

- `mawk=1.3.4.20260302-1`

Licenses: (parsed from: `/usr/share/doc/mawk/copyright`)

- `CC-BY-3.0`
- `GPL-2`
- `GPL-2.0-only`
- `X11`

Source:

```console
$ apt-get source -qq --print-uris mawk=1.3.4.20260302-1
'http://deb.debian.org/debian/pool/main/m/mawk/mawk_1.3.4.20260302-1.dsc' mawk_1.3.4.20260302-1.dsc 2969 SHA256:26e1f5c5864ea340a8f16049025a31be2aa16c7bb59ad531616e7066032953e4
'http://deb.debian.org/debian/pool/main/m/mawk/mawk_1.3.4.20260302.orig.tar.gz' mawk_1.3.4.20260302.orig.tar.gz 438318 SHA256:e2c08a77d0a84a01f9be454d1ca3872d4f103f9ada683d075198b0c6e965633d
'http://deb.debian.org/debian/pool/main/m/mawk/mawk_1.3.4.20260302.orig.tar.gz.asc' mawk_1.3.4.20260302.orig.tar.gz.asc 729 SHA256:19d493061dff7df253d698f866be24856028155f51abb037fdb4ad2872d611f5
'http://deb.debian.org/debian/pool/main/m/mawk/mawk_1.3.4.20260302-1.debian.tar.xz' mawk_1.3.4.20260302-1.debian.tar.xz 16128 SHA256:0e9a3e00800cb10dab402196b0511ed19a9f626e351b6cc1b807026f3594de62
```

Other potentially useful URLs:

- https://sources.debian.net/src/mawk/1.3.4.20260302-1/ (for browsing the source)
- https://sources.debian.net/src/mawk/1.3.4.20260302-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/mawk/1.3.4.20260302-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `media-types=14.0.0`

Binary Packages:

- `media-types=14.0.0`

Licenses: (parsed from: `/usr/share/doc/media-types/copyright`)

- `ad-hoc`

Source:

```console
$ apt-get source -qq --print-uris media-types=14.0.0
'http://deb.debian.org/debian/pool/main/m/media-types/media-types_14.0.0.dsc' media-types_14.0.0.dsc 1917 SHA256:a81f910e05176114f966815e900fc6eed2b6c144ae3a234cb39e0c6b757a3ef2
'http://deb.debian.org/debian/pool/main/m/media-types/media-types_14.0.0.tar.xz' media-types_14.0.0.tar.xz 65204 SHA256:d5877ac8c1fa3661b3c9ace293ae154c844fad686786f085e954c014f7e73f4d
```

Other potentially useful URLs:

- https://sources.debian.net/src/media-types/14.0.0/ (for browsing the source)
- https://sources.debian.net/src/media-types/14.0.0/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/media-types/14.0.0/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `mercurial=7.2-5`

Binary Packages:

- `mercurial=7.2-5`
- `mercurial-common=7.2-5`

Licenses: (parsed from: `/usr/share/doc/mercurial/copyright`, `/usr/share/doc/mercurial-common/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris mercurial=7.2-5
'http://deb.debian.org/debian/pool/main/m/mercurial/mercurial_7.2-5.dsc' mercurial_7.2-5.dsc 2856 SHA256:bee8501c2c07dd3f7b72e30ab712db41a75074bc4ed2c1e1313275b9a5c030c6
'http://deb.debian.org/debian/pool/main/m/mercurial/mercurial_7.2.orig.tar.gz' mercurial_7.2.orig.tar.gz 9244423 SHA256:a250227eba47c6ad5aa32b9a72281343762f5d274ff38c53c2f43df5c63af3ec
'http://deb.debian.org/debian/pool/main/m/mercurial/mercurial_7.2.orig.tar.gz.asc' mercurial_7.2.orig.tar.gz.asc 659 SHA256:d39f1ba5defb6b24305af2956361fbca6ace286085f223197b96710bdc2a3b73
'http://deb.debian.org/debian/pool/main/m/mercurial/mercurial_7.2-5.debian.tar.xz' mercurial_7.2-5.debian.tar.xz 54988 SHA256:848e32d815f07114257c347dd4b6daf8ae16d63deaa20bd75adbc3e9f64aeb00
```

Other potentially useful URLs:

- https://sources.debian.net/src/mercurial/7.2-5/ (for browsing the source)
- https://sources.debian.net/src/mercurial/7.2-5/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/mercurial/7.2-5/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `ncurses=6.6+20251231-1`

Binary Packages:

- `libncursesw6:amd64=6.6+20251231-1+b1`
- `libtinfo6:amd64=6.6+20251231-1+b1`
- `ncurses-base=6.6+20251231-1`
- `ncurses-bin=6.6+20251231-1+b1`

Licenses: (parsed from: `/usr/share/doc/libncursesw6/copyright`, `/usr/share/doc/libtinfo6/copyright`, `/usr/share/doc/ncurses-base/copyright`, `/usr/share/doc/ncurses-bin/copyright`)

- `BSD-3-clause`
- `MIT/X11`
- `X11`

Source:

```console
$ apt-get source -qq --print-uris ncurses=6.6+20251231-1
'http://deb.debian.org/debian/pool/main/n/ncurses/ncurses_6.6%2b20251231-1.dsc' ncurses_6.6+20251231-1.dsc 4163 SHA256:1c7b340d53b1fc75df31bc219e6395c7d6474348b2ec968098c1a0cc7cecfe0e
'http://deb.debian.org/debian/pool/main/n/ncurses/ncurses_6.6%2b20251231.orig.tar.gz' ncurses_6.6+20251231.orig.tar.gz 3789898 SHA256:e280541f4f601b8586bec305976c873fd641607f9bc4254bf661034dcccac4e9
'http://deb.debian.org/debian/pool/main/n/ncurses/ncurses_6.6%2b20251231.orig.tar.gz.asc' ncurses_6.6+20251231.orig.tar.gz.asc 729 SHA256:ccb61134c7ffd365aa1f7f3afc3dadaadbda3a46aee463b289c9d0dddb2e9bd3
'http://deb.debian.org/debian/pool/main/n/ncurses/ncurses_6.6%2b20251231-1.debian.tar.xz' ncurses_6.6+20251231-1.debian.tar.xz 50852 SHA256:fd4a1fd7113e034175310bda8f4589854a0f66fe70482a6bd553de73d773303c
```

Other potentially useful URLs:

- https://sources.debian.net/src/ncurses/6.6+20251231-1/ (for browsing the source)
- https://sources.debian.net/src/ncurses/6.6+20251231-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/ncurses/6.6+20251231-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `netbase=6.5`

Binary Packages:

- `netbase=6.5`

Licenses: (parsed from: `/usr/share/doc/netbase/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris netbase=6.5
'http://deb.debian.org/debian/pool/main/n/netbase/netbase_6.5.dsc' netbase_6.5.dsc 899 SHA256:e8691899f57c06fcc383b0f2214b662137df539227d9d7811dc8223f32ebe4c7
'http://deb.debian.org/debian/pool/main/n/netbase/netbase_6.5.tar.xz' netbase_6.5.tar.xz 32544 SHA256:9116047aebbaa1698934052d01c6e09b4c3aed643e93df63d2ddcbec243c26d1
```

Other potentially useful URLs:

- https://sources.debian.net/src/netbase/6.5/ (for browsing the source)
- https://sources.debian.net/src/netbase/6.5/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/netbase/6.5/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `nettle=3.10.2-1`

Binary Packages:

- `libhogweed6t64:amd64=3.10.2-1+b1`
- `libnettle8t64:amd64=3.10.2-1+b1`

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
$ apt-get source -qq --print-uris nettle=3.10.2-1
'http://deb.debian.org/debian/pool/main/n/nettle/nettle_3.10.2-1.dsc' nettle_3.10.2-1.dsc 2297 SHA256:e2f713973191da5d021759173f2176c21abb5f9420df45cd93a8ff058d62493f
'http://deb.debian.org/debian/pool/main/n/nettle/nettle_3.10.2.orig.tar.gz' nettle_3.10.2.orig.tar.gz 2644644 SHA256:fe9ff51cb1f2abb5e65a6b8c10a92da0ab5ab6eaf26e7fc2b675c45f1fb519b5
'http://deb.debian.org/debian/pool/main/n/nettle/nettle_3.10.2.orig.tar.gz.asc' nettle_3.10.2.orig.tar.gz.asc 573 SHA256:3496de6ba5685733aaab2e4e611ea5860fdd76964c56c995f5a0b4c2ec5084ae
'http://deb.debian.org/debian/pool/main/n/nettle/nettle_3.10.2-1.debian.tar.xz' nettle_3.10.2-1.debian.tar.xz 25052 SHA256:6f5be658d8bfbc5ffd3c75bd15b8a40fd51c5dd4ae10519d7835be135944f0a7
```

Other potentially useful URLs:

- https://sources.debian.net/src/nettle/3.10.2-1/ (for browsing the source)
- https://sources.debian.net/src/nettle/3.10.2-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/nettle/3.10.2-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `nghttp2=1.69.0-1`

Binary Packages:

- `libnghttp2-14:amd64=1.69.0-1`

Licenses: (parsed from: `/usr/share/doc/libnghttp2-14/copyright`)

- `BSD-2-clause`
- `Expat`
- `GPL-3`
- `GPL-3+ with autoconf exception`
- `MIT`
- `all-permissive`

Source:

```console
$ apt-get source -qq --print-uris nghttp2=1.69.0-1
'http://deb.debian.org/debian/pool/main/n/nghttp2/nghttp2_1.69.0-1.dsc' nghttp2_1.69.0-1.dsc 2753 SHA256:ed3da08fe5fecf6c891d665a188253c86b5a1aad8013645202977cfba7fafc67
'http://deb.debian.org/debian/pool/main/n/nghttp2/nghttp2_1.69.0.orig.tar.gz' nghttp2_1.69.0.orig.tar.gz 2667714 SHA256:c866b7477cbb7512ab6863a685027adbb1bb8da8fc3bab7429ed43d3281d5aa9
'http://deb.debian.org/debian/pool/main/n/nghttp2/nghttp2_1.69.0.orig.tar.gz.asc' nghttp2_1.69.0.orig.tar.gz.asc 833 SHA256:d97bb0333f15587a12be5efbe883e223e90c7a214d738311ce71034203559f93
'http://deb.debian.org/debian/pool/main/n/nghttp2/nghttp2_1.69.0-1.debian.tar.xz' nghttp2_1.69.0-1.debian.tar.xz 15048 SHA256:f3867c74362b07c53bd4e983072051f4d41ac486f72de7a1efb40e9f2cc8b0cf
```

Other potentially useful URLs:

- https://sources.debian.net/src/nghttp2/1.69.0-1/ (for browsing the source)
- https://sources.debian.net/src/nghttp2/1.69.0-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/nghttp2/1.69.0-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `nghttp3=1.15.0-1`

Binary Packages:

- `libnghttp3-9:amd64=1.15.0-1`

Licenses: (parsed from: `/usr/share/doc/libnghttp3-9/copyright`)

- `FSFAP`
- `FSFUL`
- `FSFULLR`
- `GPL-2`
- `GPL-2+ with Autoconf generic exception`
- `GPL-2+ with Libtool Exception`
- `GPL-3`
- `GPL-3+`
- `GPL-3+ with Autoconf generic exception`
- `MIT`

Source:

```console
$ apt-get source -qq --print-uris nghttp3=1.15.0-1
'http://deb.debian.org/debian/pool/main/n/nghttp3/nghttp3_1.15.0-1.dsc' nghttp3_1.15.0-1.dsc 1612 SHA256:942f7905556604590b6b5c8a8f8626fa06ebd6176bc5817a7d3040dbc47613c4
'http://deb.debian.org/debian/pool/main/n/nghttp3/nghttp3_1.15.0.orig.tar.xz' nghttp3_1.15.0.orig.tar.xz 408660 SHA256:6da0cd06b428d32a54c58137838505d9dc0371a900bb8070a46b29e1ceaf2e0f
'http://deb.debian.org/debian/pool/main/n/nghttp3/nghttp3_1.15.0.orig.tar.xz.asc' nghttp3_1.15.0.orig.tar.xz.asc 833 SHA256:8fc15ae8b22970e54103a2166fe2d4ec1b0f17c3e3aba4bc5b39e33f5958d6f8
'http://deb.debian.org/debian/pool/main/n/nghttp3/nghttp3_1.15.0-1.debian.tar.xz' nghttp3_1.15.0-1.debian.tar.xz 8840 SHA256:46b242663cf3cbe0957948f46903fa926be895f38d98b6373b6db6d61a3a06e2
```

Other potentially useful URLs:

- https://sources.debian.net/src/nghttp3/1.15.0-1/ (for browsing the source)
- https://sources.debian.net/src/nghttp3/1.15.0-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/nghttp3/1.15.0-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `ngtcp2=1.22.1-1`

Binary Packages:

- `libngtcp2-16:amd64=1.22.1-1`
- `libngtcp2-crypto-gnutls8:amd64=1.22.1-1`
- `libngtcp2-crypto-ossl0:amd64=1.22.1-1`

Licenses: (parsed from: `/usr/share/doc/libngtcp2-16/copyright`, `/usr/share/doc/libngtcp2-crypto-gnutls8/copyright`, `/usr/share/doc/libngtcp2-crypto-ossl0/copyright`)

- `FSFAP`
- `FSFUL`
- `FSFULLR`
- `GPL-2`
- `GPL-2+ with Autoconf generic exception`
- `GPL-2+ with Libtool Exception`
- `GPL-3`
- `GPL-3+ with Autoconf Macro's Exception`
- `GPL-3+ with Autoconf generic exception`
- `ISC`
- `MIT`

Source:

```console
$ apt-get source -qq --print-uris ngtcp2=1.22.1-1
'http://deb.debian.org/debian/pool/main/n/ngtcp2/ngtcp2_1.22.1-1.dsc' ngtcp2_1.22.1-1.dsc 2599 SHA256:d3ce1fe931b39d3fd6feb4b7feb1a166319102de527b2c53f034193de2dc1f0d
'http://deb.debian.org/debian/pool/main/n/ngtcp2/ngtcp2_1.22.1.orig.tar.xz' ngtcp2_1.22.1.orig.tar.xz 692880 SHA256:dfd2c68bd64b89847c611425b9487105c46e8447b5c21e6aeb00642c8fbe2ca8
'http://deb.debian.org/debian/pool/main/n/ngtcp2/ngtcp2_1.22.1.orig.tar.xz.asc' ngtcp2_1.22.1.orig.tar.xz.asc 833 SHA256:802e87fd27427f2c91f80f38419858f5240f09d1f92cc4e2a70ec717be7c2283
'http://deb.debian.org/debian/pool/main/n/ngtcp2/ngtcp2_1.22.1-1.debian.tar.xz' ngtcp2_1.22.1-1.debian.tar.xz 11808 SHA256:368ac3aa1aaa0cb43f0ae243afa564fa13a960ae01b20a5a05377d4e3fbe3474
```

Other potentially useful URLs:

- https://sources.debian.net/src/ngtcp2/1.22.1-1/ (for browsing the source)
- https://sources.debian.net/src/ngtcp2/1.22.1-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/ngtcp2/1.22.1-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `npth=1.8-3`

Binary Packages:

- `libnpth0t64:amd64=1.8-3+b2`

Licenses: (parsed from: `/usr/share/doc/libnpth0t64/copyright`)

- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris npth=1.8-3
'http://deb.debian.org/debian/pool/main/n/npth/npth_1.8-3.dsc' npth_1.8-3.dsc 2188 SHA256:4d447cdfdc0034465181f7285ae7d52f4e1b7ca9a60f4fec4effae556d6d5c46
'http://deb.debian.org/debian/pool/main/n/npth/npth_1.8.orig.tar.bz2' npth_1.8.orig.tar.bz2 317739 SHA256:8bd24b4f23a3065d6e5b26e98aba9ce783ea4fd781069c1b35d149694e90ca3e
'http://deb.debian.org/debian/pool/main/n/npth/npth_1.8.orig.tar.bz2.asc' npth_1.8.orig.tar.bz2.asc 390 SHA256:1a2bd2f85ad832d5166e616cbf336b072c6bdc20335146c5adccd3e2795a24bc
'http://deb.debian.org/debian/pool/main/n/npth/npth_1.8-3.debian.tar.xz' npth_1.8-3.debian.tar.xz 8668 SHA256:b2ec0499de431042120dd56338f9f7ae600b1cbc00dcb71efe39d62d8960cb73
```

Other potentially useful URLs:

- https://sources.debian.net/src/npth/1.8-3/ (for browsing the source)
- https://sources.debian.net/src/npth/1.8-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/npth/1.8-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `openldap=2.6.10+dfsg-1`

Binary Packages:

- `libldap2:amd64=2.6.10+dfsg-1+b2`

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
$ apt-get source -qq --print-uris openldap=2.6.10+dfsg-1
'http://deb.debian.org/debian/pool/main/o/openldap/openldap_2.6.10%2bdfsg-1.dsc' openldap_2.6.10+dfsg-1.dsc 3285 SHA256:05cdd431ef995904f094f4464ca78d5d3b2abdbe4eefacd72446ff8443a2ffac
'http://deb.debian.org/debian/pool/main/o/openldap/openldap_2.6.10%2bdfsg.orig.tar.xz' openldap_2.6.10+dfsg.orig.tar.xz 3754560 SHA256:e871102bda1e42155fd4d6be4825a297e1c593cb0907b84fc7dde888dc847877
'http://deb.debian.org/debian/pool/main/o/openldap/openldap_2.6.10%2bdfsg-1.debian.tar.xz' openldap_2.6.10+dfsg-1.debian.tar.xz 170112 SHA256:2dc95ade5655d67c9043e45b5601734fdb7f668267682d087b595a80de24a500
```

Other potentially useful URLs:

- https://sources.debian.net/src/openldap/2.6.10+dfsg-1/ (for browsing the source)
- https://sources.debian.net/src/openldap/2.6.10+dfsg-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/openldap/2.6.10+dfsg-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `openssh=1:10.3p1-1`

Binary Packages:

- `openssh-client=1:10.3p1-1`

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
$ apt-get source -qq --print-uris openssh=1:10.3p1-1
'http://deb.debian.org/debian/pool/main/o/openssh/openssh_10.3p1-1.dsc' openssh_10.3p1-1.dsc 3583 SHA256:9e64ddb36ff17f643af4ce25fc8453c489cec9ee8173c91800468eb928e1db98
'http://deb.debian.org/debian/pool/main/o/openssh/openssh_10.3p1.orig.tar.gz' openssh_10.3p1.orig.tar.gz 2007369 SHA256:56682a36bb92dcf4b4f016fd8ec8e74059b79a8de25c15d670d731e7d18e45f4
'http://deb.debian.org/debian/pool/main/o/openssh/openssh_10.3p1.orig.tar.gz.asc' openssh_10.3p1.orig.tar.gz.asc 833 SHA256:d9cb0783c637211b03dfcd9d1e41cf721e0080855b273c56b795fa37988b70c4
'http://deb.debian.org/debian/pool/main/o/openssh/openssh_10.3p1-1.debian.tar.xz' openssh_10.3p1-1.debian.tar.xz 202424 SHA256:ce986735603ab2180f370c8e06de7a7185d5e06f6f2ea5848aa919355f4be891
```

Other potentially useful URLs:

- https://sources.debian.net/src/openssh/1:10.3p1-1/ (for browsing the source)
- https://sources.debian.net/src/openssh/1:10.3p1-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/openssh/1:10.3p1-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `openssl=3.6.2-1`

Binary Packages:

- `libssl3t64:amd64=3.6.2-1`
- `openssl=3.6.2-1`
- `openssl-provider-legacy=3.6.2-1`

Licenses: (parsed from: `/usr/share/doc/libssl3t64/copyright`, `/usr/share/doc/openssl/copyright`, `/usr/share/doc/openssl-provider-legacy/copyright`)

- `Apache-2.0`
- `Artistic`
- `GPL-1`
- `GPL-1+`

Source:

```console
$ apt-get source -qq --print-uris openssl=3.6.2-1
'http://deb.debian.org/debian/pool/main/o/openssl/openssl_3.6.2-1.dsc' openssl_3.6.2-1.dsc 2849 SHA256:c94552e5abc4935764624321bcd29e6c113c3c74af1b85239b523c9f01998e08
'http://deb.debian.org/debian/pool/main/o/openssl/openssl_3.6.2.orig.tar.gz' openssl_3.6.2.orig.tar.gz 54913556 SHA256:aaf51a1fe064384f811daeaeb4ec4dce7340ec8bd893027eee676af31e83a04f
'http://deb.debian.org/debian/pool/main/o/openssl/openssl_3.6.2.orig.tar.gz.asc' openssl_3.6.2.orig.tar.gz.asc 833 SHA256:c325b2975a9be4fe03425286badbe7a380a6f1e98325c180024182fca62396c1
'http://deb.debian.org/debian/pool/main/o/openssl/openssl_3.6.2-1.debian.tar.xz' openssl_3.6.2-1.debian.tar.xz 48404 SHA256:4fa6b0d775292b983fba3e5686c850253fc978e9c07c13efb6bca030ac2e93c3
```

Other potentially useful URLs:

- https://sources.debian.net/src/openssl/3.6.2-1/ (for browsing the source)
- https://sources.debian.net/src/openssl/3.6.2-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/openssl/3.6.2-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `p11-kit=0.26.2-2`

Binary Packages:

- `libp11-kit0:amd64=0.26.2-2`

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
- `customFSFULLRWD`

Source:

```console
$ apt-get source -qq --print-uris p11-kit=0.26.2-2
'http://deb.debian.org/debian/pool/main/p/p11-kit/p11-kit_0.26.2-2.dsc' p11-kit_0.26.2-2.dsc 2541 SHA256:066316279c279ca964caa83d92b0f9263914fbbe3c329419e3eec9ffb30540fb
'http://deb.debian.org/debian/pool/main/p/p11-kit/p11-kit_0.26.2.orig.tar.xz' p11-kit_0.26.2.orig.tar.xz 1069216 SHA256:09fd9f44da4813a3141e73d5e7cf7008e5660d0405f13d56c15e1da9dcecf828
'http://deb.debian.org/debian/pool/main/p/p11-kit/p11-kit_0.26.2.orig.tar.xz.asc' p11-kit_0.26.2.orig.tar.xz.asc 228 SHA256:a2c205bbac7857adc91eb2670304c2ac6649aa9eaf4aab81bf0e46e124f13d8b
'http://deb.debian.org/debian/pool/main/p/p11-kit/p11-kit_0.26.2-2.debian.tar.xz' p11-kit_0.26.2-2.debian.tar.xz 24392 SHA256:1e0be1ac6c3f47a44305855b1c54e22064516a258eef911119c4944d5530b87f
```

Other potentially useful URLs:

- https://sources.debian.net/src/p11-kit/0.26.2-2/ (for browsing the source)
- https://sources.debian.net/src/p11-kit/0.26.2-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/p11-kit/0.26.2-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `pam=1.7.0-5`

Binary Packages:

- `libpam-modules:amd64=1.7.0-5+b2`
- `libpam-modules-bin=1.7.0-5+b2`
- `libpam-runtime=1.7.0-5`
- `libpam0g:amd64=1.7.0-5+b2`

Licenses: (parsed from: `/usr/share/doc/libpam-modules/copyright`, `/usr/share/doc/libpam-modules-bin/copyright`, `/usr/share/doc/libpam-runtime/copyright`, `/usr/share/doc/libpam0g/copyright`)

- `BSD-3-clause`
- `BSD-tcp_wrappers`
- `Beerware`
- `GPL`
- `GPL-1`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+ with Bison exception`
- `LGPL-2`
- `LGPL-2+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris pam=1.7.0-5
'http://deb.debian.org/debian/pool/main/p/pam/pam_1.7.0-5.dsc' pam_1.7.0-5.dsc 2210 SHA256:5c127aa18c7cb52ec9ee91fa2099453b3a851bcc0088e79045384a2a508b341c
'http://deb.debian.org/debian/pool/main/p/pam/pam_1.7.0.orig.tar.xz' pam_1.7.0.orig.tar.xz 507824 SHA256:57dcd7a6b966ecd5bbd95e1d11173734691e16b68692fa59661cdae9b13b1697
'http://deb.debian.org/debian/pool/main/p/pam/pam_1.7.0.orig.tar.xz.asc' pam_1.7.0.orig.tar.xz.asc 801 SHA256:7a8ea18ec7d9dd1f8cbf9055c32128cbca8241aa63e9fea44d56ce6f0e15e441
'http://deb.debian.org/debian/pool/main/p/pam/pam_1.7.0-5.debian.tar.xz' pam_1.7.0-5.debian.tar.xz 145640 SHA256:d776d7cb6fc8b08273f96b7f843299356ef13c6756e30468c594ab28faf1701c
```

Other potentially useful URLs:

- https://sources.debian.net/src/pam/1.7.0-5/ (for browsing the source)
- https://sources.debian.net/src/pam/1.7.0-5/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/pam/1.7.0-5/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `pcre2=10.46-1`

Binary Packages:

- `libpcre2-8-0:amd64=10.46-1+b2`

Licenses: (parsed from: `/usr/share/doc/libpcre2-8-0/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `BSD-3-clause-Cambridge with BINARY LIBRARY-LIKE PACKAGES exception`
- `X11`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris pcre2=10.46-1
'http://deb.debian.org/debian/pool/main/p/pcre2/pcre2_10.46-1.dsc' pcre2_10.46-1.dsc 2337 SHA256:f07e05cd55dd8189d1a7eec2c3ed2d963f51a84ab5494567a112b42f8d525661
'http://deb.debian.org/debian/pool/main/p/pcre2/pcre2_10.46.orig.tar.gz' pcre2_10.46.orig.tar.gz 2718545 SHA256:8d28d7f2c3b970c3a4bf3776bcbb5adfc923183ce74bc8df1ebaad8c1985bd07
'http://deb.debian.org/debian/pool/main/p/pcre2/pcre2_10.46-1.diff.gz' pcre2_10.46-1.diff.gz 8748 SHA256:307f2b889eb62e71fba064fb6ec65a367f1a88ceb667c4d7109c8d3fe1859e88
```

Other potentially useful URLs:

- https://sources.debian.net/src/pcre2/10.46-1/ (for browsing the source)
- https://sources.debian.net/src/pcre2/10.46-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/pcre2/10.46-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `perl=5.40.1-7`

Binary Packages:

- `libperl5.40:amd64=5.40.1-7+b1`
- `perl=5.40.1-7+b1`
- `perl-base=5.40.1-7+b1`
- `perl-modules-5.40=5.40.1-7`

Licenses: (parsed from: `/usr/share/doc/libperl5.40/copyright`, `/usr/share/doc/perl/copyright`, `/usr/share/doc/perl-base/copyright`, `/usr/share/doc/perl-modules-5.40/copyright`)

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
$ apt-get source -qq --print-uris perl=5.40.1-7
'http://deb.debian.org/debian/pool/main/p/perl/perl_5.40.1-7.dsc' perl_5.40.1-7.dsc 2372 SHA256:b74d67b039d7bb2c2c63b0928fae9269f4c025ef6d09254af196827388ff885a
'http://deb.debian.org/debian/pool/main/p/perl/perl_5.40.1.orig-regen-configure.tar.xz' perl_5.40.1.orig-regen-configure.tar.xz 421056 SHA256:4ea023d08101443f6ed9dc3bdd9bb5f5e08087678dc9e443d195df22da36209a
'http://deb.debian.org/debian/pool/main/p/perl/perl_5.40.1.orig.tar.xz' perl_5.40.1.orig.tar.xz 13930924 SHA256:dfa20c2eef2b4af133525610bbb65dd13777ecf998c9c5b1ccf0d308e732ee3f
'http://deb.debian.org/debian/pool/main/p/perl/perl_5.40.1-7.debian.tar.xz' perl_5.40.1-7.debian.tar.xz 172940 SHA256:d9a0b6e8466e0b2061e6fe7605e1f316a86a8e2a95fb3ed7f9e91e698ff002cc
```

Other potentially useful URLs:

- https://sources.debian.net/src/perl/5.40.1-7/ (for browsing the source)
- https://sources.debian.net/src/perl/5.40.1-7/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/perl/5.40.1-7/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `pinentry=1.3.2-4`

Binary Packages:

- `pinentry-curses=1.3.2-4`

Licenses: (parsed from: `/usr/share/doc/pinentry-curses/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-3`
- `LGPL-3+`
- `X11`

Source:

```console
$ apt-get source -qq --print-uris pinentry=1.3.2-4
'http://deb.debian.org/debian/pool/main/p/pinentry/pinentry_1.3.2-4.dsc' pinentry_1.3.2-4.dsc 3209 SHA256:83960cadf15c5d1f570d15a8927f4bbeb11bc42704f1081a0c066143933cf4c3
'http://deb.debian.org/debian/pool/main/p/pinentry/pinentry_1.3.2.orig.tar.bz2' pinentry_1.3.2.orig.tar.bz2 612858 SHA256:8e986ed88561b4da6e9efe0c54fa4ca8923035c99264df0b0464497c5fb94e9e
'http://deb.debian.org/debian/pool/main/p/pinentry/pinentry_1.3.2.orig.tar.bz2.asc' pinentry_1.3.2.orig.tar.bz2.asc 427 SHA256:b95fc1c5ed983ca6c3376477d328010dce4a494fce491be02d4c5a1e018a516f
'http://deb.debian.org/debian/pool/main/p/pinentry/pinentry_1.3.2-4.debian.tar.xz' pinentry_1.3.2-4.debian.tar.xz 20068 SHA256:144c662e85ca16c99fa22b270aa1c1744082c27e536f50b86fbd2804991357ed
```

Other potentially useful URLs:

- https://sources.debian.net/src/pinentry/1.3.2-4/ (for browsing the source)
- https://sources.debian.net/src/pinentry/1.3.2-4/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/pinentry/1.3.2-4/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `procps=2:4.0.4-9`

Binary Packages:

- `libproc2-0:amd64=2:4.0.4-9+b2`
- `procps=2:4.0.4-9+b2`

Licenses: (parsed from: `/usr/share/doc/libproc2-0/copyright`, `/usr/share/doc/procps/copyright`)

- `GPL-2`
- `GPL-2.0+`
- `LGPL-2`
- `LGPL-2.0+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris procps=2:4.0.4-9
'http://deb.debian.org/debian/pool/main/p/procps/procps_4.0.4-9.dsc' procps_4.0.4-9.dsc 2124 SHA256:0ea43605b8d5d7ac4306af0dcd2d01e237cbaba6603b0cf248dd7cfd4364ac7a
'http://deb.debian.org/debian/pool/main/p/procps/procps_4.0.4.orig.tar.xz' procps_4.0.4.orig.tar.xz 1401540 SHA256:22870d6feb2478adb617ce4f09a787addaf2d260c5a8aa7b17d889a962c5e42e
'http://deb.debian.org/debian/pool/main/p/procps/procps_4.0.4-9.debian.tar.xz' procps_4.0.4-9.debian.tar.xz 45932 SHA256:4821ca009f83b05522bc97ddac82661898938323ef0808416bca7830ce19bd97
```

Other potentially useful URLs:

- https://sources.debian.net/src/procps/2:4.0.4-9/ (for browsing the source)
- https://sources.debian.net/src/procps/2:4.0.4-9/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/procps/2:4.0.4-9/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `python3-defaults=3.13.9-3`

Binary Packages:

- `libpython3-stdlib:amd64=3.13.9-3`
- `python3=3.13.9-3`
- `python3-minimal=3.13.9-3`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris python3-defaults=3.13.9-3
'http://deb.debian.org/debian/pool/main/p/python3-defaults/python3-defaults_3.13.9-3.dsc' python3-defaults_3.13.9-3.dsc 2479 SHA256:ec3e7c2d72a5370e7703f4f7a8fcb821a26fa5541a92640b5ed8146a560d8734
'http://deb.debian.org/debian/pool/main/p/python3-defaults/python3-defaults_3.13.9-3.tar.gz' python3-defaults_3.13.9-3.tar.gz 146945 SHA256:fecf2d8d17944801bac8f09e6b87707be373c9de09bb9bb320bc66ca8048e04c
```

Other potentially useful URLs:

- https://sources.debian.net/src/python3-defaults/3.13.9-3/ (for browsing the source)
- https://sources.debian.net/src/python3-defaults/3.13.9-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/python3-defaults/3.13.9-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `python3.13=3.13.12-1`

Binary Packages:

- `libpython3.13-minimal:amd64=3.13.12-1`
- `libpython3.13-stdlib:amd64=3.13.12-1`
- `python3.13=3.13.12-1`
- `python3.13-minimal=3.13.12-1`

Licenses: (parsed from: `/usr/share/doc/libpython3.13-minimal/copyright`, `/usr/share/doc/libpython3.13-stdlib/copyright`, `/usr/share/doc/python3.13/copyright`, `/usr/share/doc/python3.13-minimal/copyright`)

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
$ apt-get source -qq --print-uris python3.13=3.13.12-1
'http://deb.debian.org/debian/pool/main/p/python3.13/python3.13_3.13.12-1.dsc' python3.13_3.13.12-1.dsc 3699 SHA256:719bb6c94e12177e5005c66858f47c8f8d630ef89418b7f5494aeda4c5f6165d
'http://deb.debian.org/debian/pool/main/p/python3.13/python3.13_3.13.12.orig.tar.xz' python3.13_3.13.12.orig.tar.xz 22926488 SHA256:2a84cd31dd8d8ea8aaff75de66fc1b4b0127dd5799aa50a64ae9a313885b4593
'http://deb.debian.org/debian/pool/main/p/python3.13/python3.13_3.13.12.orig.tar.xz.asc' python3.13_3.13.12.orig.tar.xz.asc 963 SHA256:1a0f233d4f31ad9cdda8bfd4db856c74654704304816c00e5ca159e28fb1c925
'http://deb.debian.org/debian/pool/main/p/python3.13/python3.13_3.13.12-1.debian.tar.xz' python3.13_3.13.12-1.debian.tar.xz 261232 SHA256:07004fa9fe09ee7d14cfc0037a04ab08c4c52e91721682b92720839b76abe2d2
```

Other potentially useful URLs:

- https://sources.debian.net/src/python3.13/3.13.12-1/ (for browsing the source)
- https://sources.debian.net/src/python3.13/3.13.12-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/python3.13/3.13.12-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `readline=8.3-4`

Binary Packages:

- `libreadline8t64:amd64=8.3-4`
- `readline-common=8.3-4`

Licenses: (parsed from: `/usr/share/doc/libreadline8t64/copyright`, `/usr/share/doc/readline-common/copyright`)

- `GFDL`
- `GFDL-NIV-1.3+`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `ISC-no-attribution`

Source:

```console
$ apt-get source -qq --print-uris readline=8.3-4
'http://deb.debian.org/debian/pool/main/r/readline/readline_8.3-4.dsc' readline_8.3-4.dsc 2957 SHA256:fce5107e62911aa84c18d6049469cb34c31db7fd35ab9f8182e4da7fb6959527
'http://deb.debian.org/debian/pool/main/r/readline/readline_8.3.orig.tar.gz' readline_8.3.orig.tar.gz 3419642 SHA256:fe5383204467828cd495ee8d1d3c037a7eba1389c22bc6a041f627976f9061cc
'http://deb.debian.org/debian/pool/main/r/readline/readline_8.3-4.debian.tar.xz' readline_8.3-4.debian.tar.xz 28644 SHA256:506ec377afd3688752554271e6d9a69c12a4d19ec1c002116fc70967ca6a5bdf
```

Other potentially useful URLs:

- https://sources.debian.net/src/readline/8.3-4/ (for browsing the source)
- https://sources.debian.net/src/readline/8.3-4/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/readline/8.3-4/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `rtmpdump=2.6-1`

Binary Packages:

- `librtmp1:amd64=2.6-1`

Licenses: (parsed from: `/usr/share/doc/librtmp1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris rtmpdump=2.6-1
'http://deb.debian.org/debian/pool/main/r/rtmpdump/rtmpdump_2.6-1.dsc' rtmpdump_2.6-1.dsc 1633 SHA256:a2b6a4c34fe9366640132f4fcbaeeecc4433ac5cfb2bc0da459a95129a41c2f1
'http://deb.debian.org/debian/pool/main/r/rtmpdump/rtmpdump_2.6.orig.tar.xz' rtmpdump_2.6.orig.tar.xz 103936 SHA256:f88e141ea3e126574dce24dca364f209560e13097fbba9c7f6b2f47a9a167646
'http://deb.debian.org/debian/pool/main/r/rtmpdump/rtmpdump_2.6-1.debian.tar.xz' rtmpdump_2.6-1.debian.tar.xz 7900 SHA256:9fb8a025013189c7c768770c928fa46c44072049b9e9aa2a38045806c9afa018
```

Other potentially useful URLs:

- https://sources.debian.net/src/rtmpdump/2.6-1/ (for browsing the source)
- https://sources.debian.net/src/rtmpdump/2.6-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/rtmpdump/2.6-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `rust-sequoia-sq=1.3.1-8`

Binary Packages:

- `sq=1.3.1-8`

Licenses: (parsed from: `/usr/share/doc/sq/copyright`)

- `GPL-2`
- `GPL-2.0-or-later`
- `LGPL-2`
- `LGPL-2.0-or-later`

Source:

```console
$ apt-get source -qq --print-uris rust-sequoia-sq=1.3.1-8
'http://deb.debian.org/debian/pool/main/r/rust-sequoia-sq/rust-sequoia-sq_1.3.1-8.dsc' rust-sequoia-sq_1.3.1-8.dsc 4377 SHA256:06c0cc563233671903396bff662687bc05f867ad2a99583afc4e58a47e59e12d
'http://deb.debian.org/debian/pool/main/r/rust-sequoia-sq/rust-sequoia-sq_1.3.1.orig.tar.gz' rust-sequoia-sq_1.3.1.orig.tar.gz 740320 SHA256:5c04b662da1c207e79beaeff6e5ab2d713ab10c1263f64c367f8489aac815705
'http://deb.debian.org/debian/pool/main/r/rust-sequoia-sq/rust-sequoia-sq_1.3.1-8.debian.tar.xz' rust-sequoia-sq_1.3.1-8.debian.tar.xz 5552 SHA256:4d482fcd97225af8be97c20331136defd015aafbe4898c44e1332d3471d22d11
```

Other potentially useful URLs:

- https://sources.debian.net/src/rust-sequoia-sq/1.3.1-8/ (for browsing the source)
- https://sources.debian.net/src/rust-sequoia-sq/1.3.1-8/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/rust-sequoia-sq/1.3.1-8/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `rust-sequoia-sqv=1.3.0-5`

Binary Packages:

- `sqv=1.3.0-5+b1`

Licenses: (parsed from: `/usr/share/doc/sqv/copyright`)

- `LGPL-2`
- `LGPL-2.0-or-later`

Source:

```console
$ apt-get source -qq --print-uris rust-sequoia-sqv=1.3.0-5
'http://deb.debian.org/debian/pool/main/r/rust-sequoia-sqv/rust-sequoia-sqv_1.3.0-5.dsc' rust-sequoia-sqv_1.3.0-5.dsc 2630 SHA256:dd766214353afb35bc610df910323263abd79da52e9ed7d003858e4db3c590ac
'http://deb.debian.org/debian/pool/main/r/rust-sequoia-sqv/rust-sequoia-sqv_1.3.0.orig.tar.gz' rust-sequoia-sqv_1.3.0.orig.tar.gz 140759 SHA256:8924571d26720b245292ad3c450e4061fcb24890461874790549747bffa35e60
'http://deb.debian.org/debian/pool/main/r/rust-sequoia-sqv/rust-sequoia-sqv_1.3.0-5.debian.tar.xz' rust-sequoia-sqv_1.3.0-5.debian.tar.xz 3944 SHA256:ddff90296cb649bd9408e801f9f8cca28a36e63c7e2bab8db8c8716043152b3d
```

Other potentially useful URLs:

- https://sources.debian.net/src/rust-sequoia-sqv/1.3.0-5/ (for browsing the source)
- https://sources.debian.net/src/rust-sequoia-sqv/1.3.0-5/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/rust-sequoia-sqv/1.3.0-5/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `sed=4.9-3`

Binary Packages:

- `sed=4.9-3`

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
$ apt-get source -qq --print-uris sed=4.9-3
'http://deb.debian.org/debian/pool/main/s/sed/sed_4.9-3.dsc' sed_4.9-3.dsc 1860 SHA256:2d12b031a4f677470645b7be2c37e73aa74dd3d09f4dd50d70194f95087a20dc
'http://deb.debian.org/debian/pool/main/s/sed/sed_4.9.orig.tar.xz' sed_4.9.orig.tar.xz 1397092 SHA256:6e226b732e1cd739464ad6862bd1a1aba42d7982922da7a53519631d24975181
'http://deb.debian.org/debian/pool/main/s/sed/sed_4.9-3.debian.tar.xz' sed_4.9-3.debian.tar.xz 63196 SHA256:1104b995e0b29019598a1ca7de729c21ed1eb9d670998131c4f597243fa0ebdb
```

Other potentially useful URLs:

- https://sources.debian.net/src/sed/4.9-3/ (for browsing the source)
- https://sources.debian.net/src/sed/4.9-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/sed/4.9-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `sensible-utils=0.0.26`

Binary Packages:

- `sensible-utils=0.0.26`

Licenses: (parsed from: `/usr/share/doc/sensible-utils/copyright`)

- `All-permissive`
- `GPL-2`
- `GPL-2+`
- `configure`
- `installsh`

Source:

```console
$ apt-get source -qq --print-uris sensible-utils=0.0.26
'http://deb.debian.org/debian/pool/main/s/sensible-utils/sensible-utils_0.0.26.dsc' sensible-utils_0.0.26.dsc 1706 SHA256:ca691944ce867871cdc216dd142d66315523773646740cd2801cab85da5bcec5
'http://deb.debian.org/debian/pool/main/s/sensible-utils/sensible-utils_0.0.26.tar.xz' sensible-utils_0.0.26.tar.xz 76736 SHA256:46adb7a12d32a9323b29711bc6470628fcc0f94f1748fe5bae4729df50531f68
```

Other potentially useful URLs:

- https://sources.debian.net/src/sensible-utils/0.0.26/ (for browsing the source)
- https://sources.debian.net/src/sensible-utils/0.0.26/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/sensible-utils/0.0.26/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `serf=1.3.10-3`

Binary Packages:

- `libserf-1-1:amd64=1.3.10-3+b2`

Licenses: (parsed from: `/usr/share/doc/libserf-1-1/copyright`)

- `Apache`
- `Apache-2.0`
- `Zlib`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/serf/1.3.10-3/


### `dpkg` source package: `shadow=1:4.19.3-2`

Binary Packages:

- `login.defs=1:4.19.3-2`
- `passwd=1:4.19.3-2`

Licenses: (parsed from: `/usr/share/doc/login.defs/copyright`, `/usr/share/doc/passwd/copyright`)

- `BSD-3-clause`
- `GPL-1`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris shadow=1:4.19.3-2
'http://deb.debian.org/debian/pool/main/s/shadow/shadow_4.19.3-2.dsc' shadow_4.19.3-2.dsc 2871 SHA256:bd435c4c270c2392a5cacc44b090aa300f8d66ef426d079b4950367bbc6681dc
'http://deb.debian.org/debian/pool/main/s/shadow/shadow_4.19.3.orig.tar.xz' shadow_4.19.3.orig.tar.xz 2347720 SHA256:11a8f358910712cf957dd4fd205063fce7e386b68fc7dfe3a0e1e53155ec53c5
'http://deb.debian.org/debian/pool/main/s/shadow/shadow_4.19.3.orig.tar.xz.asc' shadow_4.19.3.orig.tar.xz.asc 833 SHA256:a70fd6edfd57598d187579276b10e75f0f117d417a3e2f63ea111e9f8010aec4
'http://deb.debian.org/debian/pool/main/s/shadow/shadow_4.19.3-2.debian.tar.xz' shadow_4.19.3-2.debian.tar.xz 174200 SHA256:1168455eea66aafb572bb0356c3bf547670ebb2ed411fd1c02eaabc3979ff399
```

Other potentially useful URLs:

- https://sources.debian.net/src/shadow/1:4.19.3-2/ (for browsing the source)
- https://sources.debian.net/src/shadow/1:4.19.3-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/shadow/1:4.19.3-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `sqlite3=3.46.1-9`

Binary Packages:

- `libsqlite3-0:amd64=3.46.1-9+b1`

Licenses: (parsed from: `/usr/share/doc/libsqlite3-0/copyright`)

- `GPL-2`
- `GPL-2+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris sqlite3=3.46.1-9
'http://deb.debian.org/debian/pool/main/s/sqlite3/sqlite3_3.46.1-9.dsc' sqlite3_3.46.1-9.dsc 2641 SHA256:9ebf8f5168120f5950abe53a6f995db5b7fbda0daefb85864c2bd7ff1d18a5dd
'http://deb.debian.org/debian/pool/main/s/sqlite3/sqlite3_3.46.1.orig-www.tar.xz' sqlite3_3.46.1.orig-www.tar.xz 5861820 SHA256:648df41a8e532882b1905df45919aae4bafaf74c455f66bc86f1f52f45c8b8f0
'http://deb.debian.org/debian/pool/main/s/sqlite3/sqlite3_3.46.1.orig.tar.xz' sqlite3_3.46.1.orig.tar.xz 8456776 SHA256:d0cdd2ece271b29e7ce18095745d892517ee26d0f270065b3a25c2e9eb11639c
'http://deb.debian.org/debian/pool/main/s/sqlite3/sqlite3_3.46.1-9.debian.tar.xz' sqlite3_3.46.1-9.debian.tar.xz 35848 SHA256:df4c95da200c01221809dc60f2b60618025c3f8565f43e6a5b18a7e34b5d615c
```

Other potentially useful URLs:

- https://sources.debian.net/src/sqlite3/3.46.1-9/ (for browsing the source)
- https://sources.debian.net/src/sqlite3/3.46.1-9/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/sqlite3/3.46.1-9/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `subversion=1.14.5-6`

Binary Packages:

- `libsvn1:amd64=1.14.5-6`
- `subversion=1.14.5-6`

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
$ apt-get source -qq --print-uris subversion=1.14.5-6
'http://deb.debian.org/debian/pool/main/s/subversion/subversion_1.14.5-6.dsc' subversion_1.14.5-6.dsc 3976 SHA256:b7c7eb4009f4251e23043adc68b486eb3b7539d57cbd03f496d66b1a767960e5
'http://deb.debian.org/debian/pool/main/s/subversion/subversion_1.14.5.orig.tar.gz' subversion_1.14.5.orig.tar.gz 11645728 SHA256:cd143fe8fdb1cd506c438eef1c772a2e87e1519e6b0be3fcd54a8c59e9022390
'http://deb.debian.org/debian/pool/main/s/subversion/subversion_1.14.5.orig.tar.gz.asc' subversion_1.14.5.orig.tar.gz.asc 2382 SHA256:91384669ad9125c6919b0b2ab0c345e6de3cd0f89affe04ab66dfe9c5e19d673
'http://deb.debian.org/debian/pool/main/s/subversion/subversion_1.14.5-6.debian.tar.xz' subversion_1.14.5-6.debian.tar.xz 300584 SHA256:242c7c9cd09a4d08c578500b4d78857047319601b8deb0cbca51e2bd47db4c94
```

Other potentially useful URLs:

- https://sources.debian.net/src/subversion/1.14.5-6/ (for browsing the source)
- https://sources.debian.net/src/subversion/1.14.5-6/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/subversion/1.14.5-6/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `systemd=260.1-1`

Binary Packages:

- `libsystemd-shared:amd64=260.1-1`
- `libsystemd0:amd64=260.1-1`
- `libudev1:amd64=260.1-1`
- `systemd=260.1-1`

Licenses: (parsed from: `/usr/share/doc/libsystemd-shared/copyright`, `/usr/share/doc/libsystemd0/copyright`, `/usr/share/doc/libudev1/copyright`, `/usr/share/doc/systemd/copyright`)

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
$ apt-get source -qq --print-uris systemd=260.1-1
'http://deb.debian.org/debian/pool/main/s/systemd/systemd_260.1-1.dsc' systemd_260.1-1.dsc 8607 SHA256:ae9dc2f650c52fd3a8388e8cb5121a3b6988e257fb97352e5871d5241d9717f8
'http://deb.debian.org/debian/pool/main/s/systemd/systemd_260.1.orig.tar.gz' systemd_260.1.orig.tar.gz 17581096 SHA256:11b9821892b75d19af7b21f0f7f4e53636638147faf3e6a4ded78b40cb38993f
'http://deb.debian.org/debian/pool/main/s/systemd/systemd_260.1-1.debian.tar.xz' systemd_260.1-1.debian.tar.xz 185416 SHA256:eb37d781bfa7e4395df6da4716f1aa31f4b7cfe6f247b0815f5bf178ccd0071e
```

Other potentially useful URLs:

- https://sources.debian.net/src/systemd/260.1-1/ (for browsing the source)
- https://sources.debian.net/src/systemd/260.1-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/systemd/260.1-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `sysvinit=3.18-1`

Binary Packages:

- `sysvinit-utils=3.18-1`

Licenses: (parsed from: `/usr/share/doc/sysvinit-utils/copyright`)

- `GPL-2`
- `GPL-2.0`
- `GPL-2.0+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris sysvinit=3.18-1
'http://deb.debian.org/debian/pool/main/s/sysvinit/sysvinit_3.18-1.dsc' sysvinit_3.18-1.dsc 2379 SHA256:27d9f67e77d4edba5f7c91f44f91f9a509f74af3fdf543aded0e49a9d3dd48c0
'http://deb.debian.org/debian/pool/main/s/sysvinit/sysvinit_3.18.orig.tar.gz' sysvinit_3.18.orig.tar.gz 512421 SHA256:be9fdd55f2c1d1469a1f9d69e9d6abf47a2c0003df987b72605c653e92e5bb14
'http://deb.debian.org/debian/pool/main/s/sysvinit/sysvinit_3.18-1.debian.tar.xz' sysvinit_3.18-1.debian.tar.xz 123048 SHA256:f393e8cc3826b52e0cd0637ff31ac332b97f660375389356491ab5612d9ed5f2
```

Other potentially useful URLs:

- https://sources.debian.net/src/sysvinit/3.18-1/ (for browsing the source)
- https://sources.debian.net/src/sysvinit/3.18-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/sysvinit/3.18-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `tar=1.35+dfsg-4`

Binary Packages:

- `tar=1.35+dfsg-4`

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
$ apt-get source -qq --print-uris tar=1.35+dfsg-4
'http://deb.debian.org/debian/pool/main/t/tar/tar_1.35%2bdfsg-4.dsc' tar_1.35+dfsg-4.dsc 2034 SHA256:493403c9708bdf8ccd516aea90d81058eeff058e7e459fcc46ffa78867554b39
'http://deb.debian.org/debian/pool/main/t/tar/tar_1.35%2bdfsg.orig.tar.xz' tar_1.35+dfsg.orig.tar.xz 2111608 SHA256:9ae57e981c1e73c0eebc2b26c9b0c4497fe310ef1d516ea430efb5470b71f7a8
'http://deb.debian.org/debian/pool/main/t/tar/tar_1.35%2bdfsg-4.debian.tar.xz' tar_1.35+dfsg-4.debian.tar.xz 21640 SHA256:9bb51d273e49502eab6d98228e8dd711c46a3418bf8428a2104148734810157e
```

Other potentially useful URLs:

- https://sources.debian.net/src/tar/1.35+dfsg-4/ (for browsing the source)
- https://sources.debian.net/src/tar/1.35+dfsg-4/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/tar/1.35+dfsg-4/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `tzdata=2026b-1`

Binary Packages:

- `tzdata=2026b-1`

Licenses: (parsed from: `/usr/share/doc/tzdata/copyright`)

- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris tzdata=2026b-1
'http://deb.debian.org/debian/pool/main/t/tzdata/tzdata_2026b-1.dsc' tzdata_2026b-1.dsc 2434 SHA256:d6952421d1c8aab7f5c71a1bff3c74f4d4fef4d48443429887e9a3f292c69b85
'http://deb.debian.org/debian/pool/main/t/tzdata/tzdata_2026b.orig.tar.gz' tzdata_2026b.orig.tar.gz 473703 SHA256:114543d9f19a6bfeb5bca43686aea173d38755a3db1f2eec112647ae92c6f544
'http://deb.debian.org/debian/pool/main/t/tzdata/tzdata_2026b.orig.tar.gz.asc' tzdata_2026b.orig.tar.gz.asc 833 SHA256:b69ac9d9c926cb5ef80ab0b4bbc2a462eb9b4b36167e4aac649d87b744f7ca8b
'http://deb.debian.org/debian/pool/main/t/tzdata/tzdata_2026b-1.debian.tar.xz' tzdata_2026b-1.debian.tar.xz 128320 SHA256:ca5955fa4f7e189a8a1bd55b261ac3c42fe9d243baab6321e50e7672fbb52dcf
```

Other potentially useful URLs:

- https://sources.debian.net/src/tzdata/2026b-1/ (for browsing the source)
- https://sources.debian.net/src/tzdata/2026b-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/tzdata/2026b-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `ucf=3.0053`

Binary Packages:

- `ucf=3.0053`

Licenses: (parsed from: `/usr/share/doc/ucf/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris ucf=3.0053
'http://deb.debian.org/debian/pool/main/u/ucf/ucf_3.0053.dsc' ucf_3.0053.dsc 1512 SHA256:fd21caa907dea5748255678817b002f6ffe0c19ee4c25897ff522791c3079a65
'http://deb.debian.org/debian/pool/main/u/ucf/ucf_3.0053.tar.xz' ucf_3.0053.tar.xz 71532 SHA256:070b252a17f80a43f831798686b413286c9f35e0a0b6582f81ef1856f2e7dd23
```

Other potentially useful URLs:

- https://sources.debian.net/src/ucf/3.0053/ (for browsing the source)
- https://sources.debian.net/src/ucf/3.0053/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/ucf/3.0053/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `utf8proc=2.11.3-2`

Binary Packages:

- `libutf8proc3:amd64=2.11.3-2`

Licenses: (parsed from: `/usr/share/doc/libutf8proc3/copyright`)

- `Expat`
- `Unicode`

Source:

```console
$ apt-get source -qq --print-uris utf8proc=2.11.3-2
'http://deb.debian.org/debian/pool/main/u/utf8proc/utf8proc_2.11.3-2.dsc' utf8proc_2.11.3-2.dsc 2284 SHA256:efd80658e840f49fd9116fba26cd8c08abc56a8ba7bae50064ef4564cc98259d
'http://deb.debian.org/debian/pool/main/u/utf8proc/utf8proc_2.11.3.orig.tar.gz' utf8proc_2.11.3.orig.tar.gz 202535 SHA256:abfed50b6d4da51345713661370290f4f4747263ee73dc90356299dfc7990c78
'http://deb.debian.org/debian/pool/main/u/utf8proc/utf8proc_2.11.3-2.debian.tar.xz' utf8proc_2.11.3-2.debian.tar.xz 6212 SHA256:4415e39b2e482c0bf01f371dc10755352479499f161ac3da42f0a9ff0f96658b
```

Other potentially useful URLs:

- https://sources.debian.net/src/utf8proc/2.11.3-2/ (for browsing the source)
- https://sources.debian.net/src/utf8proc/2.11.3-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/utf8proc/2.11.3-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `util-linux=2.42-5`

Binary Packages:

- `bsdutils=1:2.42-5`
- `libblkid1:amd64=2.42-5`
- `libmount1:amd64=2.42-5`
- `libsmartcols1:amd64=2.42-5`
- `libuuid1:amd64=2.42-5`
- `login=1:4.16.0-2+really2.42-5`
- `mount=2.42-5`
- `util-linux=2.42-5`

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

Source:

```console
$ apt-get source -qq --print-uris util-linux=2.42-5
'http://deb.debian.org/debian/pool/main/u/util-linux/util-linux_2.42-5.dsc' util-linux_2.42-5.dsc 5317 SHA256:fe9c2fff43586b5f2dd7161002c61bcf7b14acbd0e4f962d024efd0c96d0a63c
'http://deb.debian.org/debian/pool/main/u/util-linux/util-linux_2.42.orig.tar.xz' util-linux_2.42.orig.tar.xz 10608300 SHA256:3452b260bbaa775d6e749ac3bb22111785003fc1f444970025c8da26dfa758e9
'http://deb.debian.org/debian/pool/main/u/util-linux/util-linux_2.42-5.debian.tar.xz' util-linux_2.42-5.debian.tar.xz 101868 SHA256:0167f489c82c60f483fedbc895036ed6a49996dbe4c9f258b61e4353c9b41c19
```

Other potentially useful URLs:

- https://sources.debian.net/src/util-linux/2.42-5/ (for browsing the source)
- https://sources.debian.net/src/util-linux/2.42-5/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/util-linux/2.42-5/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `wget=1.25.0-2`

Binary Packages:

- `wget=1.25.0-2`

Licenses: (parsed from: `/usr/share/doc/wget/copyright`)

- `GFDL-1.2`
- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris wget=1.25.0-2
'http://deb.debian.org/debian/pool/main/w/wget/wget_1.25.0-2.dsc' wget_1.25.0-2.dsc 2251 SHA256:32caf133042db927360a8c35357e4b2877eb83ff0ca144ceb64508947d894f55
'http://deb.debian.org/debian/pool/main/w/wget/wget_1.25.0.orig.tar.gz' wget_1.25.0.orig.tar.gz 5263736 SHA256:766e48423e79359ea31e41db9e5c289675947a7fcf2efdcedb726ac9d0da3784
'http://deb.debian.org/debian/pool/main/w/wget/wget_1.25.0.orig.tar.gz.asc' wget_1.25.0.orig.tar.gz.asc 854 SHA256:47f0989685931c3df6166061069659bc13a75b221a62041625007fa2dad7411b
'http://deb.debian.org/debian/pool/main/w/wget/wget_1.25.0-2.debian.tar.xz' wget_1.25.0-2.debian.tar.xz 27884 SHA256:45d4411e892d12af710ddff536d2daf430031387e336153f5f996cf536487b90
```

Other potentially useful URLs:

- https://sources.debian.net/src/wget/1.25.0-2/ (for browsing the source)
- https://sources.debian.net/src/wget/1.25.0-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/wget/1.25.0-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `xxhash=0.8.3-2`

Binary Packages:

- `libxxhash0:amd64=0.8.3-2+b2`

Licenses: (parsed from: `/usr/share/doc/libxxhash0/copyright`)

- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris xxhash=0.8.3-2
'http://deb.debian.org/debian/pool/main/x/xxhash/xxhash_0.8.3-2.dsc' xxhash_0.8.3-2.dsc 1969 SHA256:9d1f7aaace7871fbdb8775d756c6eaca84e6ad5d8e9c6ac465b7e0adc06ff90c
'http://deb.debian.org/debian/pool/main/x/xxhash/xxhash_0.8.3.orig.tar.gz' xxhash_0.8.3.orig.tar.gz 1147630 SHA256:aae608dfe8213dfd05d909a57718ef82f30722c392344583d3f39050c7f29a80
'http://deb.debian.org/debian/pool/main/x/xxhash/xxhash_0.8.3-2.debian.tar.xz' xxhash_0.8.3-2.debian.tar.xz 5144 SHA256:13824bfb2b2367225dfe3090d0ae050614f1c470a47db7232a2e9d4b2b14ad31
```

Other potentially useful URLs:

- https://sources.debian.net/src/xxhash/0.8.3-2/ (for browsing the source)
- https://sources.debian.net/src/xxhash/0.8.3-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/xxhash/0.8.3-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `xz-utils=5.8.3-1`

Binary Packages:

- `liblzma5:amd64=5.8.3-1`

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
- `none`
- `permissive-nowarranty`

Source:

```console
$ apt-get source -qq --print-uris xz-utils=5.8.3-1
'http://deb.debian.org/debian/pool/main/x/xz-utils/xz-utils_5.8.3-1.dsc' xz-utils_5.8.3-1.dsc 2494 SHA256:7b18c92ac5a89489aa8a8a4fc3c648473c02d26becce206e6f1fc54f8213d931
'http://deb.debian.org/debian/pool/main/x/xz-utils/xz-utils_5.8.3.orig.tar.xz' xz-utils_5.8.3.orig.tar.xz 1548064 SHA256:fff1ffcf2b0da84d308a14de513a1aa23d4e9aa3464d17e64b9714bfdd0bbfb6
'http://deb.debian.org/debian/pool/main/x/xz-utils/xz-utils_5.8.3-1.debian.tar.xz' xz-utils_5.8.3-1.debian.tar.xz 27344 SHA256:0f216748e70690e5b7f1d0fc85e9e6e8e69626ad7e8ee24a67e45ac9f01db4c1
```

Other potentially useful URLs:

- https://sources.debian.net/src/xz-utils/5.8.3-1/ (for browsing the source)
- https://sources.debian.net/src/xz-utils/5.8.3-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/xz-utils/5.8.3-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `zlib=1:1.3.dfsg+really1.3.2-3`

Binary Packages:

- `zlib1g:amd64=1:1.3.dfsg+really1.3.2-3`

Licenses: (parsed from: `/usr/share/doc/zlib1g/copyright`)

- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris zlib=1:1.3.dfsg+really1.3.2-3
'http://deb.debian.org/debian/pool/main/z/zlib/zlib_1.3.dfsg%2breally1.3.2-3.dsc' zlib_1.3.dfsg+really1.3.2-3.dsc 2682 SHA256:46de917397a3bda8c3b812b118e25d38044a9e161fce5e35f850f4159eb0f0de
'http://deb.debian.org/debian/pool/main/z/zlib/zlib_1.3.dfsg%2breally1.3.2.orig.tar.gz' zlib_1.3.dfsg+really1.3.2.orig.tar.gz 1295859 SHA256:7b6903eb019983987b7112eccf90f1703f1c6c0e0cede36564bf611d19ca579d
'http://deb.debian.org/debian/pool/main/z/zlib/zlib_1.3.dfsg%2breally1.3.2-3.debian.tar.xz' zlib_1.3.dfsg+really1.3.2-3.debian.tar.xz 17972 SHA256:48f7309bccf9c81e9f68a7e22cf06e08a1f70b275535b953632fccb525c5439e
```

Other potentially useful URLs:

- https://sources.debian.net/src/zlib/1:1.3.dfsg+really1.3.2-3/ (for browsing the source)
- https://sources.debian.net/src/zlib/1:1.3.dfsg+really1.3.2-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/zlib/1:1.3.dfsg+really1.3.2-3/ (for access to the source package after it no longer exists in the archive)
