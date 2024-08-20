# `buildpack-deps:sid-curl`

## Docker Metadata

- Image ID: `sha256:c3647ed5810949bbe8d894a4b2290f0a8af05479d3712f47399cac937258acdf`
- Created: `2024-08-13T00:46:13.537444561Z`
- Virtual Size: ~ 173.53 Mb  
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

### `dpkg` source package: `adduser=3.137`

Binary Packages:

- `adduser=3.137`

Licenses: (parsed from: `/usr/share/doc/adduser/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris adduser=3.137
'http://deb.debian.org/debian/pool/main/a/adduser/adduser_3.137.dsc' adduser_3.137.dsc 1671 SHA256:e4be6fbfa9db7ca7054a1c31dd2f1503340187b547112c960f2482ce3642f837
'http://deb.debian.org/debian/pool/main/a/adduser/adduser_3.137.tar.xz' adduser_3.137.tar.xz 279192 SHA256:229a61803664c2850f7d8d93e6650cd0b340ea3bbd1b954271719679ea3b0dd0
```

Other potentially useful URLs:

- https://sources.debian.net/src/adduser/3.137/ (for browsing the source)
- https://sources.debian.net/src/adduser/3.137/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/adduser/3.137/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `apt=2.9.7`

Binary Packages:

- `apt=2.9.7`
- `libapt-pkg6.0t64:amd64=2.9.7`

Licenses: (parsed from: `/usr/share/doc/apt/copyright`, `/usr/share/doc/libapt-pkg6.0t64/copyright`)

- `BSD-3-clause`
- `Expat`
- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/apt/2.9.7/


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

### `dpkg` source package: `audit=1:4.0.1-1`

Binary Packages:

- `libaudit-common=1:4.0.1-1`
- `libaudit1:amd64=1:4.0.1-1`

Licenses: (parsed from: `/usr/share/doc/libaudit-common/copyright`, `/usr/share/doc/libaudit1/copyright`)

- `GPL-1`
- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris audit=1:4.0.1-1
'http://deb.debian.org/debian/pool/main/a/audit/audit_4.0.1-1.dsc' audit_4.0.1-1.dsc 2408 SHA256:a99597cde67f951b29b1559796e4f44f7692ce71235aa431ac99254ded7a0a83
'http://deb.debian.org/debian/pool/main/a/audit/audit_4.0.1.orig.tar.gz' audit_4.0.1.orig.tar.gz 1194961 SHA256:3890319b8536446d70801e20a5790c63e879f99be83875a858460641c6c7aff4
'http://deb.debian.org/debian/pool/main/a/audit/audit_4.0.1-1.debian.tar.xz' audit_4.0.1-1.debian.tar.xz 19796 SHA256:2e2217a8227a8021fa5b2376bb779ad0006706ae2ed9e92dbb22ae36c0345a75
```

Other potentially useful URLs:

- https://sources.debian.net/src/audit/1:4.0.1-1/ (for browsing the source)
- https://sources.debian.net/src/audit/1:4.0.1-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/audit/1:4.0.1-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `base-files=13.5`

Binary Packages:

- `base-files=13.5`

Licenses: (parsed from: `/usr/share/doc/base-files/copyright`)

- `GPL`
- `GPL-2+`
- `verbatim`

Source:

```console
$ apt-get source -qq --print-uris base-files=13.5
'http://deb.debian.org/debian/pool/main/b/base-files/base-files_13.5.dsc' base-files_13.5.dsc 1100 SHA256:e5e4772aae38b90b23b882f18a277f9c9dc72f1861a0743bd26ec1af0a056492
'http://deb.debian.org/debian/pool/main/b/base-files/base-files_13.5.tar.xz' base-files_13.5.tar.xz 68200 SHA256:a478a680b60c63c0ae78fef166ae681adc945b29a2aea4c2d03ba2921b72d419
```

Other potentially useful URLs:

- https://sources.debian.net/src/base-files/13.5/ (for browsing the source)
- https://sources.debian.net/src/base-files/13.5/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/base-files/13.5/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `base-passwd=3.6.4`

Binary Packages:

- `base-passwd=3.6.4`

Licenses: (parsed from: `/usr/share/doc/base-passwd/copyright`)

- `GPL-2`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris base-passwd=3.6.4
'http://deb.debian.org/debian/pool/main/b/base-passwd/base-passwd_3.6.4.dsc' base-passwd_3.6.4.dsc 1762 SHA256:83d6855b38a0ab900d28d14bc3a0c0b97c60d5461143e51ccc2b0f8f7ea92cc8
'http://deb.debian.org/debian/pool/main/b/base-passwd/base-passwd_3.6.4.tar.xz' base-passwd_3.6.4.tar.xz 58420 SHA256:4b5232c5910932215b87bbde6f3c6c9a97021fe7902bd837b1ede8cc0be84a65
```

Other potentially useful URLs:

- https://sources.debian.net/src/base-passwd/3.6.4/ (for browsing the source)
- https://sources.debian.net/src/base-passwd/3.6.4/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/base-passwd/3.6.4/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `bash=5.2.21-2.1`

Binary Packages:

- `bash=5.2.21-2.1+b1`

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

- http://snapshot.debian.org/package/bash/5.2.21-2.1/


### `dpkg` source package: `brotli=1.1.0-2`

Binary Packages:

- `libbrotli1:amd64=1.1.0-2+b4`

Licenses: (parsed from: `/usr/share/doc/libbrotli1/copyright`)

- `MIT`

Source:

```console
$ apt-get source -qq --print-uris brotli=1.1.0-2
'http://deb.debian.org/debian/pool/main/b/brotli/brotli_1.1.0-2.dsc' brotli_1.1.0-2.dsc 2261 SHA256:39b06802a852629132d549a7f7449dee7f435e801706714a4bc2ea2f15b28f36
'http://deb.debian.org/debian/pool/main/b/brotli/brotli_1.1.0.orig.tar.gz' brotli_1.1.0.orig.tar.gz 512036 SHA256:10973f4b4199eafa1d5735ef661ddb2ec2f97319ee9fd1824d4aabe08cff5265
'http://deb.debian.org/debian/pool/main/b/brotli/brotli_1.1.0-2.debian.tar.xz' brotli_1.1.0-2.debian.tar.xz 5480 SHA256:3d913a3740bcad9a294007575a6beb1846beadbd62b44fb2bf9fdaeddea3236f
```

Other potentially useful URLs:

- https://sources.debian.net/src/brotli/1.1.0-2/ (for browsing the source)
- https://sources.debian.net/src/brotli/1.1.0-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/brotli/1.1.0-2/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/c/ca-certificates/ca-certificates_20240203.dsc' ca-certificates_20240203.dsc 1766 SHA256:629afee9b327ce4df4ad0d77ad7b10383474a432e1af30516a7e81669420109b
'http://deb.debian.org/debian/pool/main/c/ca-certificates/ca-certificates_20240203.tar.xz' ca-certificates_20240203.tar.xz 263276 SHA256:3286d3fc42c4d11b7086711a85f865b44065ce05cf1fb5376b2abed07622a9c6
```

Other potentially useful URLs:

- https://sources.debian.net/src/ca-certificates/20240203/ (for browsing the source)
- https://sources.debian.net/src/ca-certificates/20240203/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/ca-certificates/20240203/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `cdebconf=0.272`

Binary Packages:

- `libdebconfclient0:amd64=0.272`

Licenses: (parsed from: `/usr/share/doc/libdebconfclient0/copyright`)

- `BSD-2-Clause`
- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris cdebconf=0.272
'http://deb.debian.org/debian/pool/main/c/cdebconf/cdebconf_0.272.dsc' cdebconf_0.272.dsc 2707 SHA256:6b7c44f5d9881eb26c5f1d18d01015702b6fee1ce3751f8c5512d9371637eee7
'http://deb.debian.org/debian/pool/main/c/cdebconf/cdebconf_0.272.tar.xz' cdebconf_0.272.tar.xz 284488 SHA256:822883bc337bb06be4a9e6dba2fedf8d9ec3596cef8456be76eed6382ac773f9
```

Other potentially useful URLs:

- https://sources.debian.net/src/cdebconf/0.272/ (for browsing the source)
- https://sources.debian.net/src/cdebconf/0.272/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/cdebconf/0.272/ (for access to the source package after it no longer exists in the archive)

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

### `dpkg` source package: `curl=8.9.1-2`

Binary Packages:

- `curl=8.9.1-2`
- `libcurl3t64-gnutls:amd64=8.9.1-2`

Licenses: (parsed from: `/usr/share/doc/curl/copyright`, `/usr/share/doc/libcurl3t64-gnutls/copyright`)

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
$ apt-get source -qq --print-uris curl=8.9.1-2
'http://deb.debian.org/debian/pool/main/c/curl/curl_8.9.1-2.dsc' curl_8.9.1-2.dsc 3279 SHA256:955e5786e00c488eff1df859a22bd451ae8cf3cd7b0b457985aed0e4db4ed157
'http://deb.debian.org/debian/pool/main/c/curl/curl_8.9.1.orig.tar.gz' curl_8.9.1.orig.tar.gz 4200000 SHA256:291124a007ee5111997825940b3876b3048f7d31e73e9caa681b80fe48b2dcd5
'http://deb.debian.org/debian/pool/main/c/curl/curl_8.9.1.orig.tar.gz.asc' curl_8.9.1.orig.tar.gz.asc 488 SHA256:0bff807d70e37880e89c539439d86e1004a7f8a011b06c713de9bd64afb550e5
'http://deb.debian.org/debian/pool/main/c/curl/curl_8.9.1-2.debian.tar.xz' curl_8.9.1-2.debian.tar.xz 51912 SHA256:5271b8306f3cdca09d3f57f2aac9b6e06db818dde977a97b51a5f5619fa1a064
```

Other potentially useful URLs:

- https://sources.debian.net/src/curl/8.9.1-2/ (for browsing the source)
- https://sources.debian.net/src/curl/8.9.1-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/curl/8.9.1-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `cyrus-sasl2=2.1.28+dfsg1-7`

Binary Packages:

- `libsasl2-2:amd64=2.1.28+dfsg1-7`
- `libsasl2-modules-db:amd64=2.1.28+dfsg1-7`

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
$ apt-get source -qq --print-uris cyrus-sasl2=2.1.28+dfsg1-7
'http://deb.debian.org/debian/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.28%2bdfsg1-7.dsc' cyrus-sasl2_2.1.28+dfsg1-7.dsc 3223 SHA256:892d527c81c9332b8392e86e35feee992ba1f7f1148ea21ecc7abfa1b2e5f84f
'http://deb.debian.org/debian/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.28%2bdfsg1.orig.tar.xz' cyrus-sasl2_2.1.28+dfsg1.orig.tar.xz 794540 SHA256:e796a5d85d1a85e1b433d43504e467f9075c7ebc0b45730a3996cf11b1deada4
'http://deb.debian.org/debian/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.28%2bdfsg1-7.debian.tar.xz' cyrus-sasl2_2.1.28+dfsg1-7.debian.tar.xz 98928 SHA256:f0f78918499794014036065f015f6d5f7d314c13015e4116a86182fa4993fad5
```

Other potentially useful URLs:

- https://sources.debian.net/src/cyrus-sasl2/2.1.28+dfsg1-7/ (for browsing the source)
- https://sources.debian.net/src/cyrus-sasl2/2.1.28+dfsg1-7/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/cyrus-sasl2/2.1.28+dfsg1-7/ (for access to the source package after it no longer exists in the archive)

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

### `dpkg` source package: `debianutils=5.20`

Binary Packages:

- `debianutils=5.20`

Licenses: (parsed from: `/usr/share/doc/debianutils/copyright`)

- `GPL-2`
- `GPL-2+`
- `SMAIL-GPL`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris debianutils=5.20
'http://deb.debian.org/debian/pool/main/d/debianutils/debianutils_5.20.dsc' debianutils_5.20.dsc 1631 SHA256:ceb4258f9923aef343cc281419140b00e89274eb2e89d12e459bcd8a9abc1ef1
'http://deb.debian.org/debian/pool/main/d/debianutils/debianutils_5.20.tar.xz' debianutils_5.20.tar.xz 80776 SHA256:dce8731adee52d1620d562c1d98b8f4177b4ae591b7a17091ffe09700dbd4be8
```

Other potentially useful URLs:

- https://sources.debian.net/src/debianutils/5.20/ (for browsing the source)
- https://sources.debian.net/src/debianutils/5.20/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/debianutils/5.20/ (for access to the source package after it no longer exists in the archive)

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

- `e2fsprogs=1.47.1-1`
- `libcom-err2:amd64=1.47.1-1`
- `libext2fs2t64:amd64=1.47.1-1`
- `libss2:amd64=1.47.1-1`
- `logsave=1.47.1-1`

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

### `dpkg` source package: `gcc-14=14.2.0-2`

Binary Packages:

- `gcc-14-base:amd64=14.2.0-2`
- `libgcc-s1:amd64=14.2.0-2`
- `libstdc++6:amd64=14.2.0-2`

Licenses: (parsed from: `/usr/share/doc/gcc-14-base/copyright`, `/usr/share/doc/libgcc-s1/copyright`, `/usr/share/doc/libstdc++6/copyright`)

- `Artistic`
- `GFDL-1.2`
- `GPL`
- `GPL-3`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris gcc-14=14.2.0-2
'http://deb.debian.org/debian/pool/main/g/gcc-14/gcc-14_14.2.0-2.dsc' gcc-14_14.2.0-2.dsc 46572 SHA256:ec6f4d89f91eef87f5403e394421f366bc4016161fa65ff01972aae727f3825f
'http://deb.debian.org/debian/pool/main/g/gcc-14/gcc-14_14.2.0.orig.tar.gz' gcc-14_14.2.0.orig.tar.gz 94299633 SHA256:e162a5ef3f0077ecae598c6556908d2ab80841532df3398072a96a6df6e6aa29
'http://deb.debian.org/debian/pool/main/g/gcc-14/gcc-14_14.2.0-2.debian.tar.xz' gcc-14_14.2.0-2.debian.tar.xz 1641968 SHA256:39186bd12fbe63e10ea6d9284392f31bae05700a47813121e3542895dc2e777c
```

Other potentially useful URLs:

- https://sources.debian.net/src/gcc-14/14.2.0-2/ (for browsing the source)
- https://sources.debian.net/src/gcc-14/14.2.0-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/gcc-14/14.2.0-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `glibc=2.39-6`

Binary Packages:

- `libc-bin=2.39-6`
- `libc6:amd64=2.39-6`

Licenses: (parsed from: `/usr/share/doc/libc-bin/copyright`, `/usr/share/doc/libc6/copyright`)

- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris glibc=2.39-6
'http://deb.debian.org/debian/pool/main/g/glibc/glibc_2.39-6.dsc' glibc_2.39-6.dsc 7550 SHA256:cc87529a64264bd02661b058e5e49808df329a18daa80311e87b95bc622f1a74
'http://deb.debian.org/debian/pool/main/g/glibc/glibc_2.39.orig.tar.xz' glibc_2.39.orig.tar.xz 19076836 SHA256:207e5c93a158e5b45a2b42530660fe7717d4b45e00f96e58496389c2ef868157
'http://deb.debian.org/debian/pool/main/g/glibc/glibc_2.39-6.debian.tar.xz' glibc_2.39-6.debian.tar.xz 452016 SHA256:4bf30eea4909beb71db0bccd8d1add18922934c16f02bea5586bfc77a582a9f2
```

Other potentially useful URLs:

- https://sources.debian.net/src/glibc/2.39-6/ (for browsing the source)
- https://sources.debian.net/src/glibc/2.39-6/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/glibc/2.39-6/ (for access to the source package after it no longer exists in the archive)

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

### `dpkg` source package: `gnupg2=2.2.43-8`

Binary Packages:

- `dirmngr=2.2.43-8`
- `gnupg=2.2.43-8`
- `gnupg-l10n=2.2.43-8`
- `gpg=2.2.43-8`
- `gpg-agent=2.2.43-8`
- `gpgconf=2.2.43-8`
- `gpgsm=2.2.43-8`
- `gpgv=2.2.43-8`

Licenses: (parsed from: `/usr/share/doc/dirmngr/copyright`, `/usr/share/doc/gnupg/copyright`, `/usr/share/doc/gnupg-l10n/copyright`, `/usr/share/doc/gpg/copyright`, `/usr/share/doc/gpg-agent/copyright`, `/usr/share/doc/gpgconf/copyright`, `/usr/share/doc/gpgsm/copyright`, `/usr/share/doc/gpgv/copyright`)

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
$ apt-get source -qq --print-uris gnupg2=2.2.43-8
'http://deb.debian.org/debian/pool/main/g/gnupg2/gnupg2_2.2.43-8.dsc' gnupg2_2.2.43-8.dsc 3834 SHA256:8cd7674efe59b305abe9faf50895582c2276f066dadb8a6ce9586311c0d8a365
'http://deb.debian.org/debian/pool/main/g/gnupg2/gnupg2_2.2.43.orig.tar.bz2' gnupg2_2.2.43.orig.tar.bz2 7435426 SHA256:a3b34c40f455d93054d33cf4cf2a8ce41149d499eca2fbb759619de04822d453
'http://deb.debian.org/debian/pool/main/g/gnupg2/gnupg2_2.2.43.orig.tar.bz2.asc' gnupg2_2.2.43.orig.tar.bz2.asc 228 SHA256:adb6964121fde1299f0db31fe7380812f4b6bb66f4eaabdc4ab5c79480e6b701
'http://deb.debian.org/debian/pool/main/g/gnupg2/gnupg2_2.2.43-8.debian.tar.xz' gnupg2_2.2.43-8.debian.tar.xz 139592 SHA256:a99aef15523464a944797f89c01da967fc4860ec9c0897686844e2552583a8fe
```

Other potentially useful URLs:

- https://sources.debian.net/src/gnupg2/2.2.43-8/ (for browsing the source)
- https://sources.debian.net/src/gnupg2/2.2.43-8/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/gnupg2/2.2.43-8/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `gnutls28=3.8.6-2`

Binary Packages:

- `libgnutls30t64:amd64=3.8.6-2`

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
$ apt-get source -qq --print-uris gnutls28=3.8.6-2
'http://deb.debian.org/debian/pool/main/g/gnutls28/gnutls28_3.8.6-2.dsc' gnutls28_3.8.6-2.dsc 3269 SHA256:4ec462fc0173a7e33a7051586ea4486b4856cbd97e38e9a96f88f033cf0862f8
'http://deb.debian.org/debian/pool/main/g/gnutls28/gnutls28_3.8.6.orig.tar.xz' gnutls28_3.8.6.orig.tar.xz 6517476 SHA256:2e1588aae53cb32d43937f1f4eca28febd9c0c7aa1734fc5dd61a7e81e0ebcdd
'http://deb.debian.org/debian/pool/main/g/gnutls28/gnutls28_3.8.6.orig.tar.xz.asc' gnutls28_3.8.6.orig.tar.xz.asc 228 SHA256:53ad69e21ea74447117aa55e51853c49e745f2c1e2de97539c6fbbec306cf65e
'http://deb.debian.org/debian/pool/main/g/gnutls28/gnutls28_3.8.6-2.debian.tar.xz' gnutls28_3.8.6-2.debian.tar.xz 77512 SHA256:7a71826206b082d6742fafcb6dee37aa9ae147b9bad8a69875f5eed8ea7a915b
```

Other potentially useful URLs:

- https://sources.debian.net/src/gnutls28/3.8.6-2/ (for browsing the source)
- https://sources.debian.net/src/gnutls28/3.8.6-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/gnutls28/3.8.6-2/ (for access to the source package after it no longer exists in the archive)

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
'http://deb.debian.org/debian/pool/main/k/keyutils/keyutils_1.6.3-3.dsc' keyutils_1.6.3-3.dsc 2079 SHA256:0a4178e10982c7351da7db5b44b5c18807613ad066cb2e157d0756019764f0c1
'http://deb.debian.org/debian/pool/main/k/keyutils/keyutils_1.6.3.orig.tar.gz' keyutils_1.6.3.orig.tar.gz 137022 SHA256:a61d5706136ae4c05bd48f86186bcfdbd88dd8bd5107e3e195c924cfc1b39bb4
'http://deb.debian.org/debian/pool/main/k/keyutils/keyutils_1.6.3-3.debian.tar.xz' keyutils_1.6.3-3.debian.tar.xz 13328 SHA256:8c078d9de91f930df174eebc60e063e8fff574ac36c0f7ee18f7e21635d60af0
```

Other potentially useful URLs:

- https://sources.debian.net/src/keyutils/1.6.3-3/ (for browsing the source)
- https://sources.debian.net/src/keyutils/1.6.3-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/keyutils/1.6.3-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `krb5=1.21.3-3`

Binary Packages:

- `libgssapi-krb5-2:amd64=1.21.3-3`
- `libk5crypto3:amd64=1.21.3-3`
- `libkrb5-3:amd64=1.21.3-3`
- `libkrb5support0:amd64=1.21.3-3`

Licenses: (parsed from: `/usr/share/doc/libgssapi-krb5-2/copyright`, `/usr/share/doc/libk5crypto3/copyright`, `/usr/share/doc/libkrb5-3/copyright`, `/usr/share/doc/libkrb5support0/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris krb5=1.21.3-3
'http://deb.debian.org/debian/pool/main/k/krb5/krb5_1.21.3-3.dsc' krb5_1.21.3-3.dsc 3381 SHA256:561af05f1e9c42ca9eab01eaa7ea6cd903494bb5b462917c8fff7d86bbedc872
'http://deb.debian.org/debian/pool/main/k/krb5/krb5_1.21.3.orig.tar.gz' krb5_1.21.3.orig.tar.gz 9136145 SHA256:b7a4cd5ead67fb08b980b21abd150ff7217e85ea320c9ed0c6dadd304840ad35
'http://deb.debian.org/debian/pool/main/k/krb5/krb5_1.21.3.orig.tar.gz.asc' krb5_1.21.3.orig.tar.gz.asc 833 SHA256:85047c935fe949ef2e275885451b168557b923dd13a5aab0ef8fe6acd27b94d7
'http://deb.debian.org/debian/pool/main/k/krb5/krb5_1.21.3-3.debian.tar.xz' krb5_1.21.3-3.debian.tar.xz 103380 SHA256:c7b7bceb2f1bd782d0118904bded8ddaba1aaa54f1b3b2fc0dc3ecaeac450b5b
```

Other potentially useful URLs:

- https://sources.debian.net/src/krb5/1.21.3-3/ (for browsing the source)
- https://sources.debian.net/src/krb5/1.21.3-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/krb5/1.21.3-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libassuan=2.5.6-1`

Binary Packages:

- `libassuan0:amd64=2.5.6-1+b1`

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
'http://deb.debian.org/debian/pool/main/liba/libassuan/libassuan_2.5.6-1.dsc' libassuan_2.5.6-1.dsc 1997 SHA256:5216dd7bca769143cf39673b018a11b2601fde867fd4b62226088bb9177415b5
'http://deb.debian.org/debian/pool/main/liba/libassuan/libassuan_2.5.6.orig.tar.bz2' libassuan_2.5.6.orig.tar.bz2 577012 SHA256:e9fd27218d5394904e4e39788f9b1742711c3e6b41689a31aa3380bd5aa4f426
'http://deb.debian.org/debian/pool/main/liba/libassuan/libassuan_2.5.6.orig.tar.bz2.asc' libassuan_2.5.6.orig.tar.bz2.asc 228 SHA256:a1be6f5611de2f563a904c539e0415dd5823d9e1c4c0c1071418e7412174eaea
'http://deb.debian.org/debian/pool/main/liba/libassuan/libassuan_2.5.6-1.debian.tar.xz' libassuan_2.5.6-1.debian.tar.xz 14284 SHA256:58a3077b2ecda637de25f54320a3ad2087a250f6f8118271ea22968a4e994ca7
```

Other potentially useful URLs:

- https://sources.debian.net/src/libassuan/2.5.6-1/ (for browsing the source)
- https://sources.debian.net/src/libassuan/2.5.6-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libassuan/2.5.6-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libbsd=0.12.2-1`

Binary Packages:

- `libbsd0:amd64=0.12.2-1`

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
$ apt-get source -qq --print-uris libbsd=0.12.2-1
'http://deb.debian.org/debian/pool/main/libb/libbsd/libbsd_0.12.2-1.dsc' libbsd_0.12.2-1.dsc 2347 SHA256:18bfe06bd7f6d5e3f77f7827bcf129014918952cdcd6102288afdae8120dc6c9
'http://deb.debian.org/debian/pool/main/libb/libbsd/libbsd_0.12.2.orig.tar.xz' libbsd_0.12.2.orig.tar.xz 446032 SHA256:b88cc9163d0c652aaf39a99991d974ddba1c3a9711db8f1b5838af2a14731014
'http://deb.debian.org/debian/pool/main/libb/libbsd/libbsd_0.12.2.orig.tar.xz.asc' libbsd_0.12.2.orig.tar.xz.asc 833 SHA256:620dc92f158ebe0a650c0e92214a8121b927276895dc9a1dcaa38f627fa0fcb0
'http://deb.debian.org/debian/pool/main/libb/libbsd/libbsd_0.12.2-1.debian.tar.xz' libbsd_0.12.2-1.debian.tar.xz 18612 SHA256:618f0d116e18729cb7d5b93095e112c429aad294993b4def2c0498761d4646e9
```

Other potentially useful URLs:

- https://sources.debian.net/src/libbsd/0.12.2-1/ (for browsing the source)
- https://sources.debian.net/src/libbsd/0.12.2-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libbsd/0.12.2-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libcap-ng=0.8.5-1`

Binary Packages:

- `libcap-ng0:amd64=0.8.5-1+b1`

Licenses: (parsed from: `/usr/share/doc/libcap-ng0/copyright`)

- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `LGPL-2.1`
- `LGPL-2.1+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/libcap-ng/0.8.5-1/


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

### `dpkg` source package: `libgpg-error=1.50-3`

Binary Packages:

- `libgpg-error0:amd64=1.50-3`

Licenses: (parsed from: `/usr/share/doc/libgpg-error0/copyright`)

- `BSD-3-clause`
- `GPL-3`
- `GPL-3+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `g10-permissive`

Source:

```console
$ apt-get source -qq --print-uris libgpg-error=1.50-3
'http://deb.debian.org/debian/pool/main/libg/libgpg-error/libgpg-error_1.50-3.dsc' libgpg-error_1.50-3.dsc 2935 SHA256:a8eb9b7620ead8c5b650167511c6350674b76844242c881433855d323c3c6b4c
'http://deb.debian.org/debian/pool/main/libg/libgpg-error/libgpg-error_1.50.orig.tar.bz2' libgpg-error_1.50.orig.tar.bz2 1082003 SHA256:69405349e0a633e444a28c5b35ce8f14484684518a508dc48a089992fe93e20a
'http://deb.debian.org/debian/pool/main/libg/libgpg-error/libgpg-error_1.50.orig.tar.bz2.asc' libgpg-error_1.50.orig.tar.bz2.asc 228 SHA256:cbc77b528a1c018f56a83bc46d721dd8aed48f2f9b9c884a62879d33b96d424a
'http://deb.debian.org/debian/pool/main/libg/libgpg-error/libgpg-error_1.50-3.debian.tar.xz' libgpg-error_1.50-3.debian.tar.xz 19072 SHA256:3398312c01344483374d81fa3e47402deb5f6e8f060bea2040b136a87b2f3454
```

Other potentially useful URLs:

- https://sources.debian.net/src/libgpg-error/1.50-3/ (for browsing the source)
- https://sources.debian.net/src/libgpg-error/1.50-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libgpg-error/1.50-3/ (for access to the source package after it no longer exists in the archive)

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

### `dpkg` source package: `libksba=1.6.7-2`

Binary Packages:

- `libksba8:amd64=1.6.7-2`

Licenses: (parsed from: `/usr/share/doc/libksba8/copyright`)

- `FSFUL`
- `GPL-3`
- `LGPL-2.1-or-later`

Source:

```console
$ apt-get source -qq --print-uris libksba=1.6.7-2
'http://deb.debian.org/debian/pool/main/libk/libksba/libksba_1.6.7-2.dsc' libksba_1.6.7-2.dsc 2482 SHA256:47f8b314c6b74fdcfb42390327dc0441c6ba6bfdb4511ca12e2b4478fc452e1c
'http://deb.debian.org/debian/pool/main/libk/libksba/libksba_1.6.7.orig.tar.bz2' libksba_1.6.7.orig.tar.bz2 706437 SHA256:cf72510b8ebb4eb6693eef765749d83677a03c79291a311040a5bfd79baab763
'http://deb.debian.org/debian/pool/main/libk/libksba/libksba_1.6.7.orig.tar.bz2.asc' libksba_1.6.7.orig.tar.bz2.asc 228 SHA256:cd704f8100151752b12776fa87dac42a3f99334ed155bcbcbaeda8e786581316
'http://deb.debian.org/debian/pool/main/libk/libksba/libksba_1.6.7-2.debian.tar.xz' libksba_1.6.7-2.debian.tar.xz 14872 SHA256:28f0ef1f9dd2a7f1cef23e49393d750d50aade01476462d8d5225a23e4ad9929
```

Other potentially useful URLs:

- https://sources.debian.net/src/libksba/1.6.7-2/ (for browsing the source)
- https://sources.debian.net/src/libksba/1.6.7-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libksba/1.6.7-2/ (for access to the source package after it no longer exists in the archive)

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

### `dpkg` source package: `libpsl=0.21.2-1.1`

Binary Packages:

- `libpsl5t64:amd64=0.21.2-1.1`

Licenses: (parsed from: `/usr/share/doc/libpsl5t64/copyright`)

- `Chromium`
- `MIT`
- `gnulib`

Source:

```console
$ apt-get source -qq --print-uris libpsl=0.21.2-1.1
'http://deb.debian.org/debian/pool/main/libp/libpsl/libpsl_0.21.2-1.1.dsc' libpsl_0.21.2-1.1.dsc 2285 SHA256:b9b5496ca2bffb827cb0b2d997469908a2b7a7475c20a11c02f9dcd1ed2a0cc9
'http://deb.debian.org/debian/pool/main/libp/libpsl/libpsl_0.21.2.orig.tar.xz' libpsl_0.21.2.orig.tar.xz 1870352 SHA256:11e34380f2c81d6e72c710464aae3b680df4ddcc1007826c630fb03c7ca6aa54
'http://deb.debian.org/debian/pool/main/libp/libpsl/libpsl_0.21.2-1.1.debian.tar.xz' libpsl_0.21.2-1.1.debian.tar.xz 12120 SHA256:0eccab147b6dfbfb7f5ad40fb5bd9f888d72a0fe44e7d1801811c34a9acad1a7
```

Other potentially useful URLs:

- https://sources.debian.net/src/libpsl/0.21.2-1.1/ (for browsing the source)
- https://sources.debian.net/src/libpsl/0.21.2-1.1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libpsl/0.21.2-1.1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libseccomp=2.5.5-1`

Binary Packages:

- `libseccomp2:amd64=2.5.5-1+b1`

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

- `libselinux1:amd64=3.5-2+b4`

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
- `libsemanage2:amd64=3.5-1+b4`

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

### `dpkg` source package: `libssh2=1.11.0-7`

Binary Packages:

- `libssh2-1t64:amd64=1.11.0-7`

Licenses: (parsed from: `/usr/share/doc/libssh2-1t64/copyright`)

- `BSD3`
- `ISC`

Source:

```console
$ apt-get source -qq --print-uris libssh2=1.11.0-7
'http://deb.debian.org/debian/pool/main/libs/libssh2/libssh2_1.11.0-7.dsc' libssh2_1.11.0-7.dsc 2328 SHA256:8c6c145427dddd3844ab55f9a8ee77f834dbdee05e1f7ebbc25ebf7623b53c70
'http://deb.debian.org/debian/pool/main/libs/libssh2/libssh2_1.11.0.orig.tar.gz' libssh2_1.11.0.orig.tar.gz 1053562 SHA256:3736161e41e2693324deb38c26cfdc3efe6209d634ba4258db1cecff6a5ad461
'http://deb.debian.org/debian/pool/main/libs/libssh2/libssh2_1.11.0.orig.tar.gz.asc' libssh2_1.11.0.orig.tar.gz.asc 488 SHA256:b6a32c85a3f9b6f30f2b3595ba034b48a8508ee9c94708ef811f58fd7adfcdee
'http://deb.debian.org/debian/pool/main/libs/libssh2/libssh2_1.11.0-7.debian.tar.xz' libssh2_1.11.0-7.debian.tar.xz 17000 SHA256:f579fa06d5f2ca2dd89634cb8e40557c4c1606308823ac99a258bdde2cd3bdb6
```

Other potentially useful URLs:

- https://sources.debian.net/src/libssh2/1.11.0-7/ (for browsing the source)
- https://sources.debian.net/src/libssh2/1.11.0-7/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libssh2/1.11.0-7/ (for access to the source package after it no longer exists in the archive)

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


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/libxcrypt/1:4.4.36-4/


### `dpkg` source package: `libzstd=1.5.6+dfsg-1`

Binary Packages:

- `libzstd1:amd64=1.5.6+dfsg-1`

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

- `liblz4-1:amd64=1.9.4-3`

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

### `dpkg` source package: `mawk=1.3.4.20240622-2`

Binary Packages:

- `mawk=1.3.4.20240622-2`

Licenses: (parsed from: `/usr/share/doc/mawk/copyright`)

- `CC-BY-3.0`
- `GPL-2`
- `GPL-2.0-only`
- `X11`

Source:

```console
$ apt-get source -qq --print-uris mawk=1.3.4.20240622-2
'http://deb.debian.org/debian/pool/main/m/mawk/mawk_1.3.4.20240622-2.dsc' mawk_1.3.4.20240622-2.dsc 2969 SHA256:cc95afc29fa8e4406f42cd3887de7a10b9d70a84d70341d4e7c962438686db2f
'http://deb.debian.org/debian/pool/main/m/mawk/mawk_1.3.4.20240622.orig.tar.gz' mawk_1.3.4.20240622.orig.tar.gz 414190 SHA256:4e917e87a7a9fbaf76995784a4b0b5dc0dd954b977d0983030f78f6a07b1a765
'http://deb.debian.org/debian/pool/main/m/mawk/mawk_1.3.4.20240622.orig.tar.gz.asc' mawk_1.3.4.20240622.orig.tar.gz.asc 729 SHA256:1c66d8d18bf562d492a3b33a379c51ec80e111f8203a9546969fd7e436cb7041
'http://deb.debian.org/debian/pool/main/m/mawk/mawk_1.3.4.20240622-2.debian.tar.xz' mawk_1.3.4.20240622-2.debian.tar.xz 16136 SHA256:66d5c0f334acce8cd329f3807252d19c53b6b3cecbbf4d42d7c239f54f3ad296
```

Other potentially useful URLs:

- https://sources.debian.net/src/mawk/1.3.4.20240622-2/ (for browsing the source)
- https://sources.debian.net/src/mawk/1.3.4.20240622-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/mawk/1.3.4.20240622-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `ncurses=6.5-2`

Binary Packages:

- `libncursesw6:amd64=6.5-2`
- `libtinfo6:amd64=6.5-2`
- `ncurses-base=6.5-2`
- `ncurses-bin=6.5-2`

Licenses: (parsed from: `/usr/share/doc/libncursesw6/copyright`, `/usr/share/doc/libtinfo6/copyright`, `/usr/share/doc/ncurses-base/copyright`, `/usr/share/doc/ncurses-bin/copyright`)

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

### `dpkg` source package: `netbase=6.4`

Binary Packages:

- `netbase=6.4`

Licenses: (parsed from: `/usr/share/doc/netbase/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris netbase=6.4
'http://deb.debian.org/debian/pool/main/n/netbase/netbase_6.4.dsc' netbase_6.4.dsc 898 SHA256:dc26cfcaa49fd874cc27c65216b2f8b6d3ad62845b78da4bdf0aea55592af756
'http://deb.debian.org/debian/pool/main/n/netbase/netbase_6.4.tar.xz' netbase_6.4.tar.xz 32712 SHA256:fa6621826ff1150e581bd90bc3c8a4ecafe5df90404f207db6dcdf2c75f26ad7
```

Other potentially useful URLs:

- https://sources.debian.net/src/netbase/6.4/ (for browsing the source)
- https://sources.debian.net/src/netbase/6.4/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/netbase/6.4/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `nettle=3.10-1`

Binary Packages:

- `libhogweed6t64:amd64=3.10-1`
- `libnettle8t64:amd64=3.10-1`

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

### `dpkg` source package: `nghttp2=1.62.1-2`

Binary Packages:

- `libnghttp2-14:amd64=1.62.1-2`

Licenses: (parsed from: `/usr/share/doc/libnghttp2-14/copyright`)

- `BSD-2-clause`
- `Expat`
- `GPL-3`
- `GPL-3+ with autoconf exception`
- `MIT`
- `all-permissive`

Source:

```console
$ apt-get source -qq --print-uris nghttp2=1.62.1-2
'http://deb.debian.org/debian/pool/main/n/nghttp2/nghttp2_1.62.1-2.dsc' nghttp2_1.62.1-2.dsc 2531 SHA256:5f457052ee3dad45dce4848fc5bc25106fd5e519972de5788b0841e07e31aee5
'http://deb.debian.org/debian/pool/main/n/nghttp2/nghttp2_1.62.1.orig.tar.gz' nghttp2_1.62.1.orig.tar.gz 1066103 SHA256:73c8af772dd2b30cedc114d37291cf1485b0a7ce11833595fc2aec7b3ce3ba5c
'http://deb.debian.org/debian/pool/main/n/nghttp2/nghttp2_1.62.1-2.debian.tar.xz' nghttp2_1.62.1-2.debian.tar.xz 38852 SHA256:82131a80852fcc53d378d4e3cb0e27d0b6044ac595d01806b807713942fbfcac
```

Other potentially useful URLs:

- https://sources.debian.net/src/nghttp2/1.62.1-2/ (for browsing the source)
- https://sources.debian.net/src/nghttp2/1.62.1-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/nghttp2/1.62.1-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `nghttp3=1.4.0-1`

Binary Packages:

- `libnghttp3-9:amd64=1.4.0-1`

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
$ apt-get source -qq --print-uris nghttp3=1.4.0-1
'http://deb.debian.org/debian/pool/main/n/nghttp3/nghttp3_1.4.0-1.dsc' nghttp3_1.4.0-1.dsc 1355 SHA256:dfad9bb2b9bc5224d395e6b2cf594d07f1710a3112c2563495c4629baff43186
'http://deb.debian.org/debian/pool/main/n/nghttp3/nghttp3_1.4.0.orig.tar.gz' nghttp3_1.4.0.orig.tar.gz 628880 SHA256:43a78073b103acd4668c8d3314eb98e5d002095c1e49014e48ca20bd3094408f
'http://deb.debian.org/debian/pool/main/n/nghttp3/nghttp3_1.4.0-1.debian.tar.xz' nghttp3_1.4.0-1.debian.tar.xz 4504 SHA256:93489c65249d1d63e2c30ace29eecf2322ca6ac0cd719bb6c6f2279d70867954
```

Other potentially useful URLs:

- https://sources.debian.net/src/nghttp3/1.4.0-1/ (for browsing the source)
- https://sources.debian.net/src/nghttp3/1.4.0-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/nghttp3/1.4.0-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `ngtcp2=1.6.0-1`

Binary Packages:

- `libngtcp2-16:amd64=1.6.0-1`
- `libngtcp2-crypto-gnutls8:amd64=1.6.0-1`

Licenses: (parsed from: `/usr/share/doc/libngtcp2-16/copyright`, `/usr/share/doc/libngtcp2-crypto-gnutls8/copyright`)

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
$ apt-get source -qq --print-uris ngtcp2=1.6.0-1
'http://deb.debian.org/debian/pool/main/n/ngtcp2/ngtcp2_1.6.0-1.dsc' ngtcp2_1.6.0-1.dsc 1717 SHA256:551144fea304c7c9d79f67feddfcd5b80eca2aee853afd95c4a864755ad1ff70
'http://deb.debian.org/debian/pool/main/n/ngtcp2/ngtcp2_1.6.0.orig.tar.bz2' ngtcp2_1.6.0.orig.tar.bz2 807796 SHA256:3e40cfb92ab710295cb7c07721db28d16c6f251f61420a462c448cf39a59cc29
'http://deb.debian.org/debian/pool/main/n/ngtcp2/ngtcp2_1.6.0-1.debian.tar.xz' ngtcp2_1.6.0-1.debian.tar.xz 6016 SHA256:147a059def5ea5ce156c5707ba610e1beff414f1ce3049db985ec553f1015bec
```

Other potentially useful URLs:

- https://sources.debian.net/src/ngtcp2/1.6.0-1/ (for browsing the source)
- https://sources.debian.net/src/ngtcp2/1.6.0-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/ngtcp2/1.6.0-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `npth=1.6-3.1`

Binary Packages:

- `libnpth0t64:amd64=1.6-3.1`

Licenses: (parsed from: `/usr/share/doc/libnpth0t64/copyright`)

- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris npth=1.6-3.1
'http://deb.debian.org/debian/pool/main/n/npth/npth_1.6-3.1.dsc' npth_1.6-3.1.dsc 1967 SHA256:3545fbabbf59c9427a6dc98f903f4ac50786fdfc2ce3f42a21668ec3151c25f7
'http://deb.debian.org/debian/pool/main/n/npth/npth_1.6.orig.tar.bz2' npth_1.6.orig.tar.bz2 300486 SHA256:1393abd9adcf0762d34798dc34fdcf4d0d22a8410721e76f1e3afcd1daa4e2d1
'http://deb.debian.org/debian/pool/main/n/npth/npth_1.6-3.1.debian.tar.xz' npth_1.6-3.1.debian.tar.xz 10924 SHA256:e2fb2f56060991436622ddc1dc52df8f3f3e87bc9325a8b30920fce5aa0f3e30
```

Other potentially useful URLs:

- https://sources.debian.net/src/npth/1.6-3.1/ (for browsing the source)
- https://sources.debian.net/src/npth/1.6-3.1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/npth/1.6-3.1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `openldap=2.5.18+dfsg-2`

Binary Packages:

- `libldap-2.5-0:amd64=2.5.18+dfsg-2`

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
$ apt-get source -qq --print-uris openldap=2.5.18+dfsg-2
'http://deb.debian.org/debian/pool/main/o/openldap/openldap_2.5.18%2bdfsg-2.dsc' openldap_2.5.18+dfsg-2.dsc 3312 SHA256:0825ff7a10b669bce5b31199ec4a2dcf018080011a1c1020774cec734b465a45
'http://deb.debian.org/debian/pool/main/o/openldap/openldap_2.5.18%2bdfsg.orig.tar.xz' openldap_2.5.18+dfsg.orig.tar.xz 3684372 SHA256:06c2f0ee591594ae28cfbde843a70b3e009b1f09d7f3110a1570236ac46a86b5
'http://deb.debian.org/debian/pool/main/o/openldap/openldap_2.5.18%2bdfsg-2.debian.tar.xz' openldap_2.5.18+dfsg-2.debian.tar.xz 170128 SHA256:a3606da0c79d9f34a7cae36dac835ffd2ccdd4eda51eea1fdf6d209698fcfc13
```

Other potentially useful URLs:

- https://sources.debian.net/src/openldap/2.5.18+dfsg-2/ (for browsing the source)
- https://sources.debian.net/src/openldap/2.5.18+dfsg-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/openldap/2.5.18+dfsg-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `openssl=3.3.1-2`

Binary Packages:

- `libssl3t64:amd64=3.3.1-2`
- `openssl=3.3.1-2`

Licenses: (parsed from: `/usr/share/doc/libssl3t64/copyright`, `/usr/share/doc/openssl/copyright`)

- `Apache-2.0`
- `Artistic`
- `GPL-1`
- `GPL-1+`

Source:

```console
$ apt-get source -qq --print-uris openssl=3.3.1-2
'http://deb.debian.org/debian/pool/main/o/openssl/openssl_3.3.1-2.dsc' openssl_3.3.1-2.dsc 2656 SHA256:273996d3239fd8d2576cf4f0203bea8904156e9c0c4199a71f7e81ce7bfec4ff
'http://deb.debian.org/debian/pool/main/o/openssl/openssl_3.3.1.orig.tar.gz' openssl_3.3.1.orig.tar.gz 18055752 SHA256:777cd596284c883375a2a7a11bf5d2786fc5413255efab20c50d6ffe6d020b7e
'http://deb.debian.org/debian/pool/main/o/openssl/openssl_3.3.1.orig.tar.gz.asc' openssl_3.3.1.orig.tar.gz.asc 833 SHA256:a1ca1547057b75e1750717d69a35a5373544cb42f671a1a7f672c4237aab1248
'http://deb.debian.org/debian/pool/main/o/openssl/openssl_3.3.1-2.debian.tar.xz' openssl_3.3.1-2.debian.tar.xz 66364 SHA256:a4bf418b4eb38f58a0c3ba0705b1b93077d21d1dfe75071cefb9a33519eda6c7
```

Other potentially useful URLs:

- https://sources.debian.net/src/openssl/3.3.1-2/ (for browsing the source)
- https://sources.debian.net/src/openssl/3.3.1-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/openssl/3.3.1-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `p11-kit=0.25.5-2`

Binary Packages:

- `libp11-kit0:amd64=0.25.5-2`

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

### `dpkg` source package: `perl=5.38.2-5`

Binary Packages:

- `perl-base=5.38.2-5`

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
$ apt-get source -qq --print-uris perl=5.38.2-5
'http://deb.debian.org/debian/pool/main/p/perl/perl_5.38.2-5.dsc' perl_5.38.2-5.dsc 2938 SHA256:c3d9624788c42bcf14003bd110013858906279596a487735cc39494778070137
'http://deb.debian.org/debian/pool/main/p/perl/perl_5.38.2.orig-regen-configure.tar.xz' perl_5.38.2.orig-regen-configure.tar.xz 418808 SHA256:4d1b34cc058f9963cb89785ecc040d57f6d7725cd83329cfa4ef8b27566454d2
'http://deb.debian.org/debian/pool/main/p/perl/perl_5.38.2.orig.tar.xz' perl_5.38.2.orig.tar.xz 13679524 SHA256:d91115e90b896520e83d4de6b52f8254ef2b70a8d545ffab33200ea9f1cf29e8
'http://deb.debian.org/debian/pool/main/p/perl/perl_5.38.2-5.debian.tar.xz' perl_5.38.2-5.debian.tar.xz 168016 SHA256:ef455488cb518f06cb10f3ed927b05e86df347ed22942874bd3f08a197047b0a
```

Other potentially useful URLs:

- https://sources.debian.net/src/perl/5.38.2-5/ (for browsing the source)
- https://sources.debian.net/src/perl/5.38.2-5/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/perl/5.38.2-5/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `pinentry=1.2.1-3`

Binary Packages:

- `pinentry-curses=1.2.1-3+b2`

Licenses: (parsed from: `/usr/share/doc/pinentry-curses/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-3`
- `LGPL-3+`
- `X11`

Source:

```console
$ apt-get source -qq --print-uris pinentry=1.2.1-3
'http://deb.debian.org/debian/pool/main/p/pinentry/pinentry_1.2.1-3.dsc' pinentry_1.2.1-3.dsc 3170 SHA256:679a692b8a34c68a9146869347a09164d952a4b79dd2daa6ca20a1caa6aed8e8
'http://deb.debian.org/debian/pool/main/p/pinentry/pinentry_1.2.1.orig.tar.bz2' pinentry_1.2.1.orig.tar.bz2 547698 SHA256:457a185e5a85238fb945a955dc6352ab962dc8b48720b62fc9fa48c7540a4067
'http://deb.debian.org/debian/pool/main/p/pinentry/pinentry_1.2.1.orig.tar.bz2.asc' pinentry_1.2.1.orig.tar.bz2.asc 390 SHA256:9f7d9c7509e4ff4161a043893d76183bd975230fcad671b643c90f78e500ba95
'http://deb.debian.org/debian/pool/main/p/pinentry/pinentry_1.2.1-3.debian.tar.xz' pinentry_1.2.1-3.debian.tar.xz 18864 SHA256:7919390ebf6fdf2f8e4e05231bc1348edb119396d29d66718478775bb4c9a0ba
```

Other potentially useful URLs:

- https://sources.debian.net/src/pinentry/1.2.1-3/ (for browsing the source)
- https://sources.debian.net/src/pinentry/1.2.1-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/pinentry/1.2.1-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `readline=8.2-4`

Binary Packages:

- `libreadline8t64:amd64=8.2-4`
- `readline-common=8.2-4`

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

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/readline/8.2-4/


### `dpkg` source package: `rtmpdump=2.4+20151223.gitfa8646d.1-2`

Binary Packages:

- `librtmp1:amd64=2.4+20151223.gitfa8646d.1-2+b4`

Licenses: (parsed from: `/usr/share/doc/librtmp1/copyright`)

- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris rtmpdump=2.4+20151223.gitfa8646d.1-2
'http://deb.debian.org/debian/pool/main/r/rtmpdump/rtmpdump_2.4%2b20151223.gitfa8646d.1-2.dsc' rtmpdump_2.4+20151223.gitfa8646d.1-2.dsc 2299 SHA256:a296819cd2ab5880b67ad963ef0867cb10e462f4403e52565aa863eb05bb1370
'http://deb.debian.org/debian/pool/main/r/rtmpdump/rtmpdump_2.4%2b20151223.gitfa8646d.1.orig.tar.gz' rtmpdump_2.4+20151223.gitfa8646d.1.orig.tar.gz 142213 SHA256:5c032f5c8cc2937eb55a81a94effdfed3b0a0304b6376147b86f951e225e3ab5
'http://deb.debian.org/debian/pool/main/r/rtmpdump/rtmpdump_2.4%2b20151223.gitfa8646d.1-2.debian.tar.xz' rtmpdump_2.4+20151223.gitfa8646d.1-2.debian.tar.xz 8096 SHA256:26d47de07d16285e4ca55b0828cbbf1ba35e671f9b3500a87e301fe755d26882
```

Other potentially useful URLs:

- https://sources.debian.net/src/rtmpdump/2.4+20151223.gitfa8646d.1-2/ (for browsing the source)
- https://sources.debian.net/src/rtmpdump/2.4+20151223.gitfa8646d.1-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/rtmpdump/2.4+20151223.gitfa8646d.1-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `rust-sequoia-sq=0.37.0-1`

Binary Packages:

- `sq=0.37.0-1+b1`

Licenses: (parsed from: `/usr/share/doc/sq/copyright`)

- `GPL-2`
- `GPL-2.0-or-later`
- `LGPL-2`
- `LGPL-2.0-or-later`

Source:

```console
$ apt-get source -qq --print-uris rust-sequoia-sq=0.37.0-1
'http://deb.debian.org/debian/pool/main/r/rust-sequoia-sq/rust-sequoia-sq_0.37.0-1.dsc' rust-sequoia-sq_0.37.0-1.dsc 3827 SHA256:c8ee3dc01acee4c8499ade2fe4d397d5eb307a04788bd79368db062f9a53a21f
'http://deb.debian.org/debian/pool/main/r/rust-sequoia-sq/rust-sequoia-sq_0.37.0.orig.tar.gz' rust-sequoia-sq_0.37.0.orig.tar.gz 515850 SHA256:74617574f63f2f7c4e2c7f1f67f5ad354ec1ca8f373e0369689f29e4981dff24
'http://deb.debian.org/debian/pool/main/r/rust-sequoia-sq/rust-sequoia-sq_0.37.0-1.debian.tar.xz' rust-sequoia-sq_0.37.0-1.debian.tar.xz 52436 SHA256:2c494ba433dda102baf324608b43e837c949e6227762fc8fdf4a9cb6e0a3aba6
```

Other potentially useful URLs:

- https://sources.debian.net/src/rust-sequoia-sq/0.37.0-1/ (for browsing the source)
- https://sources.debian.net/src/rust-sequoia-sq/0.37.0-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/rust-sequoia-sq/0.37.0-1/ (for access to the source package after it no longer exists in the archive)

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

### `dpkg` source package: `shadow=1:4.16.0-4`

Binary Packages:

- `login.defs=1:4.16.0-4`
- `passwd=1:4.16.0-4`

Licenses: (parsed from: `/usr/share/doc/login.defs/copyright`, `/usr/share/doc/passwd/copyright`)

- `BSD-3-clause`
- `GPL-1`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris shadow=1:4.16.0-4
'http://deb.debian.org/debian/pool/main/s/shadow/shadow_4.16.0-4.dsc' shadow_4.16.0-4.dsc 2614 SHA256:cbb20576e02bb4dedf10723243b33897f57cffb26c85d585882b6485dadeeead
'http://deb.debian.org/debian/pool/main/s/shadow/shadow_4.16.0.orig.tar.xz' shadow_4.16.0.orig.tar.xz 2053720 SHA256:a0255570541a356c3718966987c8be0658691fda804826fda7576c8e69e0cfda
'http://deb.debian.org/debian/pool/main/s/shadow/shadow_4.16.0-4.debian.tar.xz' shadow_4.16.0-4.debian.tar.xz 169620 SHA256:7bb1a604494dc9567be64fa50994b72fd51011af86095d566bd71832c4d98d36
```

Other potentially useful URLs:

- https://sources.debian.net/src/shadow/1:4.16.0-4/ (for browsing the source)
- https://sources.debian.net/src/shadow/1:4.16.0-4/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/shadow/1:4.16.0-4/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `sqlite3=3.46.0-1`

Binary Packages:

- `libsqlite3-0:amd64=3.46.0-1`

Licenses: (parsed from: `/usr/share/doc/libsqlite3-0/copyright`)

- `GPL-2`
- `GPL-2+`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/sqlite3/3.46.0-1/


### `dpkg` source package: `systemd=256.4-3`

Binary Packages:

- `libsystemd0:amd64=256.4-3`
- `libudev1:amd64=256.4-3`

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

- http://snapshot.debian.org/package/systemd/256.4-3/


### `dpkg` source package: `sysvinit=3.10-1`

Binary Packages:

- `sysvinit-utils=3.10-1`

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
$ apt-get source -qq --print-uris sysvinit=3.10-1
'http://deb.debian.org/debian/pool/main/s/sysvinit/sysvinit_3.10-1.dsc' sysvinit_3.10-1.dsc 2347 SHA256:d8e1cd5ea470a0e059425772a9f4ca0d37d2db5db9ce1e6d1bf77d67604fef21
'http://deb.debian.org/debian/pool/main/s/sysvinit/sysvinit_3.10.orig.tar.gz' sysvinit_3.10.orig.tar.gz 514655 SHA256:9fbee91fbe496e207db7ab4cdfbe4f97f8795925343a76b4f3392e741b0e103b
'http://deb.debian.org/debian/pool/main/s/sysvinit/sysvinit_3.10-1.debian.tar.xz' sysvinit_3.10-1.debian.tar.xz 121244 SHA256:b2b13c317bb07b80a3621213f820465d93b23140643fb64415656c01f4d41ba7
```

Other potentially useful URLs:

- https://sources.debian.net/src/sysvinit/3.10-1/ (for browsing the source)
- https://sources.debian.net/src/sysvinit/3.10-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/sysvinit/3.10-1/ (for access to the source package after it no longer exists in the archive)

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

### `dpkg` source package: `util-linux=2.40.2-6`

Binary Packages:

- `bsdutils=1:2.40.2-6`
- `libblkid1:amd64=2.40.2-6`
- `libmount1:amd64=2.40.2-6`
- `libsmartcols1:amd64=2.40.2-6`
- `libuuid1:amd64=2.40.2-6`
- `login=1:4.16.0-2+really2.40.2-6`
- `mount=2.40.2-6`
- `util-linux=2.40.2-6`

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

- http://snapshot.debian.org/package/util-linux/2.40.2-6/


### `dpkg` source package: `wget=1.24.5-2`

Binary Packages:

- `wget=1.24.5-2+b1`

Licenses: (parsed from: `/usr/share/doc/wget/copyright`)

- `GFDL-1.2`
- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris wget=1.24.5-2
'http://deb.debian.org/debian/pool/main/w/wget/wget_1.24.5-2.dsc' wget_1.24.5-2.dsc 2212 SHA256:6d0c93504683c1bcfcfcf0fe65bfb6d9d1e1e4f2a0f80719bb3bf41859731662
'http://deb.debian.org/debian/pool/main/w/wget/wget_1.24.5.orig.tar.gz' wget_1.24.5.orig.tar.gz 5182521 SHA256:fa2dc35bab5184ecbc46a9ef83def2aaaa3f4c9f3c97d4bd19dcb07d4da637de
'http://deb.debian.org/debian/pool/main/w/wget/wget_1.24.5.orig.tar.gz.asc' wget_1.24.5.orig.tar.gz.asc 854 SHA256:2991bfab0481793d3587d5e94531d1f48297877e1d1ff88d0bc03f1b0fb19fe5
'http://deb.debian.org/debian/pool/main/w/wget/wget_1.24.5-2.debian.tar.xz' wget_1.24.5-2.debian.tar.xz 61884 SHA256:e0457915d31b96d1725c45ee8bf240a9d715cf23db972a09f4a49c32412e619e
```

Other potentially useful URLs:

- https://sources.debian.net/src/wget/1.24.5-2/ (for browsing the source)
- https://sources.debian.net/src/wget/1.24.5-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/wget/1.24.5-2/ (for access to the source package after it no longer exists in the archive)

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

### `dpkg` source package: `xz-utils=5.6.2-2`

Binary Packages:

- `liblzma5:amd64=5.6.2-2`

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
$ apt-get source -qq --print-uris xz-utils=5.6.2-2
'http://deb.debian.org/debian/pool/main/x/xz-utils/xz-utils_5.6.2-2.dsc' xz-utils_5.6.2-2.dsc 2704 SHA256:3eadad7376915923c17d22cbe3905c3985b538ada1f46dc742a1675819130af5
'http://deb.debian.org/debian/pool/main/x/xz-utils/xz-utils_5.6.2.orig.tar.xz' xz-utils_5.6.2.orig.tar.xz 1307448 SHA256:a9db3bb3d64e248a0fae963f8fb6ba851a26ba1822e504dc0efd18a80c626caf
'http://deb.debian.org/debian/pool/main/x/xz-utils/xz-utils_5.6.2.orig.tar.xz.asc' xz-utils_5.6.2.orig.tar.xz.asc 833 SHA256:297c242cb55ae70242e8773ee8099c6561b9d8a49dab3b3cfccb33465c108e20
'http://deb.debian.org/debian/pool/main/x/xz-utils/xz-utils_5.6.2-2.debian.tar.xz' xz-utils_5.6.2-2.debian.tar.xz 24560 SHA256:b269af8285f4226b2e70e98e917a16b83cbe316e27d6121d11a0b89f0d39a7c9
```

Other potentially useful URLs:

- https://sources.debian.net/src/xz-utils/5.6.2-2/ (for browsing the source)
- https://sources.debian.net/src/xz-utils/5.6.2-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/xz-utils/5.6.2-2/ (for access to the source package after it no longer exists in the archive)

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
