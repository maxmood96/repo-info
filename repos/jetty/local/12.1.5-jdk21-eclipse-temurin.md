# `jetty:12.1.5`

## Docker Metadata

- Image ID: `sha256:70434e0442e20c1f6098b3c363170fc14d0ce23d540441012a02a21b27eb34cd`
- Created: `2026-01-16T00:10:03.901835582Z`
- Virtual Size: ~ 501.41 Mb  
  (total size of all layers on-disk)
- Arch: `linux`/`amd64`
- Entrypoint: `["/docker-entrypoint.sh"]`
- Command: `["java","-jar","/usr/local/jetty/start.jar"]`
- Environment:
  - `PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin`
  - `JAVA_HOME=/opt/java/openjdk`
  - `LANG=en_US.UTF-8`
  - `LANGUAGE=en_US:en`
  - `LC_ALL=en_US.UTF-8`
  - `JAVA_VERSION=jdk-21.0.9+10`
  - `JETTY_VERSION=12.1.5`
  - `JETTY_HOME=/usr/local/jetty`
  - `JETTY_BASE=/var/lib/jetty`
  - `TMPDIR=/tmp/jetty`
  - `JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.5/jetty-home-12.1.5.tar.gz`
  - `JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3`
- Labels:
  - `org.opencontainers.image.ref.name=ubuntu`
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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `adduser=3.137ubuntu1`

Binary Packages:

- `adduser=3.137ubuntu1`

Licenses: (parsed from: `/usr/share/doc/adduser/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris adduser=3.137ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/a/adduser/adduser_3.137ubuntu1.dsc' adduser_3.137ubuntu1.dsc 1862 SHA512:4e32edd8d12689bc8f6fb2b5280b0504bbd19bdd963cebb32a016d87fbeb837cbfb9c4c544b37943adf346d33137c684936591ccbf5c89856a91f2777f00ae49
'http://archive.ubuntu.com/ubuntu/pool/main/a/adduser/adduser_3.137ubuntu1.tar.xz' adduser_3.137ubuntu1.tar.xz 280408 SHA512:46979160ef2f6b85097958cd11e549ae48efa24e1719155fd90ae7b322c0adac087cac7d0a709cd084ee11557575b05dfde89a9d63bcfd80fb47779c41098d48
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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `attr=1:2.5.2-1build1.1`

Binary Packages:

- `libattr1:amd64=1:2.5.2-1build1.1`

Licenses: (parsed from: `/usr/share/doc/libattr1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2+`
- `LGPL-2.1`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `audit=1:3.1.2-2.1build1.1`

Binary Packages:

- `libaudit-common=1:3.1.2-2.1build1.1`
- `libaudit1:amd64=1:3.1.2-2.1build1.1`

Licenses: (parsed from: `/usr/share/doc/libaudit-common/copyright`, `/usr/share/doc/libaudit1/copyright`)

- `GPL-1`
- `GPL-2`
- `LGPL-2.1`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `base-files=13ubuntu10.3`

Binary Packages:

- `base-files=13ubuntu10.3`

Licenses: (parsed from: `/usr/share/doc/base-files/copyright`)

- `GPL`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `base-passwd=3.6.3build1`

Binary Packages:

- `base-passwd=3.6.3build1`

Licenses: (parsed from: `/usr/share/doc/base-passwd/copyright`)

- `GPL-2`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris base-passwd=3.6.3build1
'http://archive.ubuntu.com/ubuntu/pool/main/b/base-passwd/base-passwd_3.6.3build1.dsc' base-passwd_3.6.3build1.dsc 1779 SHA512:b22ef01978e2b6aed82e54c28b7f06550cc0a41518f1561054148df9d3adb567e203b793e532924a9ae27201c5a2a31fef149f77217d06d8b12f8fce05e2f34d
'http://archive.ubuntu.com/ubuntu/pool/main/b/base-passwd/base-passwd_3.6.3build1.tar.xz' base-passwd_3.6.3build1.tar.xz 58252 SHA512:981b05acb6727b32fe343e761eeacee2a2061da3802999de7e10f95dfae3fdb0bd52b96001e13bf302f7be137ac6b85d6d36041ee29b9eb62f6fa21622a00ac9
```

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

Source:

```console
$ apt-get source -qq --print-uris bash=5.2.21-2ubuntu4
'http://archive.ubuntu.com/ubuntu/pool/main/b/bash/bash_5.2.21-2ubuntu4.dsc' bash_5.2.21-2ubuntu4.dsc 2437 SHA512:7e783b1a20b339b2c15070e1cf3419a10e94a17c9dda520025b6eeb07f285dcbe8455aa1647254fc422cb314dd1382ef97c65cab088793de699d4714f65eaa0d
'http://archive.ubuntu.com/ubuntu/pool/main/b/bash/bash_5.2.21.orig.tar.xz' bash_5.2.21.orig.tar.xz 5598816 SHA512:ccfd5201ebc32feb302db324868bec42a525a6b08176c77e16feb191fcd6ee4240182dcad783e6e3f010c6d33f356b2c628758f0387ef488ab8b3f932e54babb
'http://archive.ubuntu.com/ubuntu/pool/main/b/bash/bash_5.2.21-2ubuntu4.debian.tar.xz' bash_5.2.21-2ubuntu4.debian.tar.xz 94124 SHA512:cbe580880995984a6ceb6c980d2fa87bbb1ace85d834a147ce39eaf44692af654c2c537716a19c8ed21b20e8abad9240d3f3349cc51020aeba2cd6e490802725
```

### `dpkg` source package: `binutils=2.42-4ubuntu2.8`

Binary Packages:

- `binutils=2.42-4ubuntu2.8`
- `binutils-common:amd64=2.42-4ubuntu2.8`
- `binutils-x86-64-linux-gnu=2.42-4ubuntu2.8`
- `libbinutils:amd64=2.42-4ubuntu2.8`
- `libctf-nobfd0:amd64=2.42-4ubuntu2.8`
- `libctf0:amd64=2.42-4ubuntu2.8`
- `libgprofng0:amd64=2.42-4ubuntu2.8`
- `libsframe1:amd64=2.42-4ubuntu2.8`

Licenses: (parsed from: `/usr/share/doc/binutils/copyright`, `/usr/share/doc/binutils-common/copyright`, `/usr/share/doc/binutils-x86-64-linux-gnu/copyright`, `/usr/share/doc/libbinutils/copyright`, `/usr/share/doc/libctf-nobfd0/copyright`, `/usr/share/doc/libctf0/copyright`, `/usr/share/doc/libgprofng0/copyright`, `/usr/share/doc/libsframe1/copyright`)

- `GFDL`
- `GPL`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris binutils=2.42-4ubuntu2.8
'http://security.ubuntu.com/ubuntu/pool/main/b/binutils/binutils_2.42-4ubuntu2.8.dsc' binutils_2.42-4ubuntu2.8.dsc 10148 SHA512:be5a842fcc21200b65dac1f276a61edab9107ce3720e0f8742125d07e4244e4040718719a84ff6c5daeb0b1c2575a57b1c4f824dc996bd4dd8271c4613fb1adc
'http://security.ubuntu.com/ubuntu/pool/main/b/binutils/binutils_2.42.orig.tar.xz' binutils_2.42.orig.tar.xz 27567160 SHA512:155f3ba14cd220102f4f29a4f1e5cfee3c48aa03b74603460d05afb73c70d6657a9d87eee6eb88bf13203fe6f31177a5c9addc04384e956e7da8069c8ecd20a6
'http://security.ubuntu.com/ubuntu/pool/main/b/binutils/binutils_2.42-4ubuntu2.8.debian.tar.xz' binutils_2.42-4ubuntu2.8.debian.tar.xz 189180 SHA512:3d7e00b2e49b6b50293fbf2933dfaa98f5ed9f290d807507bdc1f7e361248c45eefe48207c3f4e20340fcfa1d7e1d28bad2c148d36e30a573cb0ea6fac4fb0d5
```

### `dpkg` source package: `brotli=1.1.0-2build2`

Binary Packages:

- `libbrotli1:amd64=1.1.0-2build2`

Licenses: (parsed from: `/usr/share/doc/libbrotli1/copyright`)

- `MIT`

Source:

```console
$ apt-get source -qq --print-uris brotli=1.1.0-2build2
'http://archive.ubuntu.com/ubuntu/pool/main/b/brotli/brotli_1.1.0-2build2.dsc' brotli_1.1.0-2build2.dsc 2401 SHA512:74b6f53c8917622cf69f3a5ec7d2032a5ffaf3673700efa7c0f1a095280024a48bee2518c17329d0d23a0c54d1868d0fa247e663aeca9b4587883b5f88eea1b6
'http://archive.ubuntu.com/ubuntu/pool/main/b/brotli/brotli_1.1.0.orig.tar.gz' brotli_1.1.0.orig.tar.gz 512036 SHA512:7a94f8b1ca1d3a411c6b5681bd2ed66183468f7b37a24741601d77ed4353577805de84c810dd26086d4afe6b11bfc4791db3ba7f6f9986bc7acbb8e9b43f488b
'http://archive.ubuntu.com/ubuntu/pool/main/b/brotli/brotli_1.1.0-2build2.debian.tar.xz' brotli_1.1.0-2build2.debian.tar.xz 5644 SHA512:d7f430be5228cfb92ccc2908b915ab817d6165291671721112c1b5511949e92a2bfd1017f7ad44afd00fa0a133c3724c02e9d22f81e2a726d9958bbdae9f44f0
```

### `dpkg` source package: `bzip2=1.0.8-5.1build0.1`

Binary Packages:

- `libbz2-1.0:amd64=1.0.8-5.1build0.1`

Licenses: (parsed from: `/usr/share/doc/libbz2-1.0/copyright`)

- `BSD-variant`
- `GPL-2`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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
'http://archive.ubuntu.com/ubuntu/pool/main/c/ca-certificates/ca-certificates_20240203.dsc' ca-certificates_20240203.dsc 1766 SHA512:3cd6d9322800a3469be7dcea1136daa0f9311ae148b258bbf6689d5992f4dda82351fba34d52bc07c505bf407f3f4feb4e284ecfc2fec18bb1c23b1652b98986
'http://archive.ubuntu.com/ubuntu/pool/main/c/ca-certificates/ca-certificates_20240203.tar.xz' ca-certificates_20240203.tar.xz 263276 SHA512:e9d7b5283c2be9425d18eb4a9b54b1fa54db0b9d1bdb28f9c6db7f8b2e03fd93442ac973f9b024b7a148d71ac2789edbc1207c2048ce4be589eb1a5376640670
```

### `dpkg` source package: `cdebconf=0.271ubuntu3`

Binary Packages:

- `libdebconfclient0:amd64=0.271ubuntu3`

Licenses: (parsed from: `/usr/share/doc/libdebconfclient0/copyright`)

- `BSD-2-Clause`
- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris cdebconf=0.271ubuntu3
'http://archive.ubuntu.com/ubuntu/pool/main/c/cdebconf/cdebconf_0.271ubuntu3.dsc' cdebconf_0.271ubuntu3.dsc 2910 SHA512:1c3864532126b71702307dfa4385e844363dcb8faf3f30009073dc0ebf6167ed97dd225679c3f6fb9650c5c41be8f5309668f2e4fe2d8ba798bd2cfc9dd18f36
'http://archive.ubuntu.com/ubuntu/pool/main/c/cdebconf/cdebconf_0.271ubuntu3.tar.xz' cdebconf_0.271ubuntu3.tar.xz 285500 SHA512:f9a3204842db5e0f0e042c9df72dee17692422bc4c745bc0c332317ec87dc219e26eda94404c1d7b0a6d5d6c2105da0b9ebe615c4897f012883bc8222f9ac85d
```

### `dpkg` source package: `coreutils=9.4-3ubuntu6.1`

Binary Packages:

- `coreutils=9.4-3ubuntu6.1`

Licenses: (parsed from: `/usr/share/doc/coreutils/copyright`)

- `BSD-4-clause-UC`
- `FSFULLR`
- `GFDL-1.3`
- `GFDL-NIV-1.3`
- `GPL-3`
- `GPL-3+`
- `ISC`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `curl=8.5.0-2ubuntu10.6`

Binary Packages:

- `curl=8.5.0-2ubuntu10.6`
- `libcurl4t64:amd64=8.5.0-2ubuntu10.6`

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
$ apt-get source -qq --print-uris curl=8.5.0-2ubuntu10.6
'http://security.ubuntu.com/ubuntu/pool/main/c/curl/curl_8.5.0-2ubuntu10.6.dsc' curl_8.5.0-2ubuntu10.6.dsc 3051 SHA512:befb2dcd69003718eef66ddd619e4756b087b14f25ff1cd3e84a39bc1011d64c68b4f9cf919fc5dc2a2998e1b46848cc00e2677f36af3e78638b7a730a28a84c
'http://security.ubuntu.com/ubuntu/pool/main/c/curl/curl_8.5.0.orig.tar.gz' curl_8.5.0.orig.tar.gz 4372979 SHA512:1ff70e8fd5f233b373dea2a031d46698c03ed35f384c2eacbe9368f9daed65e91d7f45ade350c3ac3dd3d662c913b17cdc8702a0c23879b0c78fbd396fd0b926
'http://security.ubuntu.com/ubuntu/pool/main/c/curl/curl_8.5.0-2ubuntu10.6.debian.tar.xz' curl_8.5.0-2ubuntu10.6.debian.tar.xz 63144 SHA512:cbcd07b07b961c3e6c23fd1701b270a48d372c60f55d9af16684f3fc5d832d24e965c0240ba4a92a198db45d1609daa7eb556ee59bfdf81f196c997a682131c3
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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `dash=0.5.12-6ubuntu5`

Binary Packages:

- `dash=0.5.12-6ubuntu5`

Licenses: (parsed from: `/usr/share/doc/dash/copyright`)

- `BSD-3-Clause`
- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris dash=0.5.12-6ubuntu5
'http://archive.ubuntu.com/ubuntu/pool/main/d/dash/dash_0.5.12-6ubuntu5.dsc' dash_0.5.12-6ubuntu5.dsc 2124 SHA512:f29c60c6d01fdf8d5c12b2924fcb2ba7a9e27025976b3158900c3e33eba7100dfe3158a1efb641177527b672fff0e9b1659ace0711063decca17e4e6f3d6dada
'http://archive.ubuntu.com/ubuntu/pool/main/d/dash/dash_0.5.12.orig.tar.gz' dash_0.5.12.orig.tar.gz 246054 SHA512:13bd262be0089260cbd13530a9cf34690c0abeb2f1920eb5e61be7951b716f9f335b86279d425dbfae56cbd49231a8fdffdff70601a5177da3d543be6fc5eb17
'http://archive.ubuntu.com/ubuntu/pool/main/d/dash/dash_0.5.12-6ubuntu5.debian.tar.xz' dash_0.5.12-6ubuntu5.debian.tar.xz 39616 SHA512:2524c1aaf0cf2f86a5fa87de998c8324a247760b59c86ef1b02ef6af298648842b1b467d3f8c6beda31bed3cc0db17fa189f20aab8305503b67df4f0c25a23d1
```

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
'http://archive.ubuntu.com/ubuntu/pool/main/d/db5.3/db5.3_5.3.28%2bdfsg2-7.dsc' db5.3_5.3.28+dfsg2-7.dsc 2374 SHA512:3877ed17196ea9d9bac87112b81461ba3bfa02fd5017043baf277728cc151bed2238a90f707464d0a4e24aab865bf5f6c0c6ee6d0eb5ec866efe4cea91f7b93c
'http://archive.ubuntu.com/ubuntu/pool/main/d/db5.3/db5.3_5.3.28%2bdfsg2.orig.tar.xz' db5.3_5.3.28+dfsg2.orig.tar.xz 21287688 SHA512:f9c9d042702ef3fcfdd4b4859583048f3396b161009dc24b6d3a2c53533d58214239fc80e2c42db17e9f092df44d531502737f3b368b956bff49ef057b6b51ef
'http://archive.ubuntu.com/ubuntu/pool/main/d/db5.3/db5.3_5.3.28%2bdfsg2-7.debian.tar.xz' db5.3_5.3.28+dfsg2-7.debian.tar.xz 35232 SHA512:9e91cdf98925d94c7f318e534474e208ce8796113867f290bcaf8ca9c3f35d309266a35e17eb5624246c5e0bf94e5893c203f5154d7d0ba50b13babf53339156
```

### `dpkg` source package: `debconf=1.5.86ubuntu1`

Binary Packages:

- `debconf=1.5.86ubuntu1`

Licenses: (parsed from: `/usr/share/doc/debconf/copyright`)

- `BSD-2-clause`

Source:

```console
$ apt-get source -qq --print-uris debconf=1.5.86ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/d/debconf/debconf_1.5.86ubuntu1.dsc' debconf_1.5.86ubuntu1.dsc 2030 SHA512:d06dc6bfa5e60ddb38839b25437641dcbd06acabc59dfa46955db87bf47370b381906916bde881de51a8dc4beaf1be9c3288bb25292718e608077c755a491988
'http://archive.ubuntu.com/ubuntu/pool/main/d/debconf/debconf_1.5.86ubuntu1.tar.xz' debconf_1.5.86ubuntu1.tar.xz 574112 SHA512:e63b3d4241e8b347fcd71f7ae838e6b0c40123bea65298a9492ae6dabb24e54d31176c11a8b1870edb5a96ea346080d2f9ca8821cef74e73f20c03265aafd95d
```

### `dpkg` source package: `debianutils=5.17build1`

Binary Packages:

- `debianutils=5.17build1`

Licenses: (parsed from: `/usr/share/doc/debianutils/copyright`)

- `GPL-2`
- `GPL-2+`
- `SMAIL-GPL`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris debianutils=5.17build1
'http://archive.ubuntu.com/ubuntu/pool/main/d/debianutils/debianutils_5.17build1.dsc' debianutils_5.17build1.dsc 1771 SHA512:4303221ace648a071b5de66dd570e334579cae327c5ad4f1bda10c957fca2f8f023f9ef6a0e1bf852ed378405a83106e85a76daf6fe9870b8f48655f1d15e8fe
'http://archive.ubuntu.com/ubuntu/pool/main/d/debianutils/debianutils_5.17build1.tar.xz' debianutils_5.17build1.tar.xz 80468 SHA512:a076c0457c2e8423ecbf2ea01c4ba029feb8eacadb5c2622422a22b24ed1d52b785fc7e651406b533e7f1e26466d6570a3719852885d5270ee058fde1d336742
```

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

Source:

```console
$ apt-get source -qq --print-uris diffutils=1:3.10-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/d/diffutils/diffutils_3.10-1build1.dsc' diffutils_3.10-1build1.dsc 2192 SHA512:60bfa2bb6c9316393e21d03863c0f7a837280bccd4bf20818ca6bc749328172f4dd433603c231d5ce17b6ed68d4070c7e5037546a94f71d8bc50b81578b9645f
'http://archive.ubuntu.com/ubuntu/pool/main/d/diffutils/diffutils_3.10.orig.tar.xz' diffutils_3.10.orig.tar.xz 1624240 SHA512:219d2c815a120690c6589846271e43aee5c96c61a7ee4abbef97dfcdb3d6416652ed494b417de0ab6688c4322540d48be63b5e617beb6d20530b5d55d723ccbb
'http://archive.ubuntu.com/ubuntu/pool/main/d/diffutils/diffutils_3.10.orig.tar.xz.asc' diffutils_3.10.orig.tar.xz.asc 833 SHA512:91aa1fcfca224454e292540ea7813f4a0eb348f06a4374017326d524949775359fc833de597cc201c97f357eb6c675800828a6e3332572376f3554f1f2e1aca1
'http://archive.ubuntu.com/ubuntu/pool/main/d/diffutils/diffutils_3.10-1build1.debian.tar.xz' diffutils_3.10-1build1.debian.tar.xz 14068 SHA512:36cb15f987cfd57dbe5bfe347a990887ffe52f8ba3756c4f806e78ba702d2b1acc2f316292bf1096a1a7db158358b4cd6261cabe70a77fd292945e07d5808cb5
```

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
'http://security.ubuntu.com/ubuntu/pool/main/d/dpkg/dpkg_1.22.6ubuntu6.5.dsc' dpkg_1.22.6ubuntu6.5.dsc 3156 SHA512:6c6f43612ac5f74937a2a83525ebb66a21af81e4678fd2b3bafbcb490e0e33be6a611b1475c205de378b64efdf7c615abd46b78c58b6c232145e7d2b75fe9d7b
'http://security.ubuntu.com/ubuntu/pool/main/d/dpkg/dpkg_1.22.6ubuntu6.5.tar.xz' dpkg_1.22.6ubuntu6.5.tar.xz 5547360 SHA512:a52c556b632205b84bf8e795f68f54fe7e78b251561d032be76ecde9c5e3d9a74c5358476956ab8c3b2fb0266a5f4a03f3d67ec7039e62dc56905ee8c52d2d5d
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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `expat=2.6.1-2ubuntu0.3`

Binary Packages:

- `libexpat1:amd64=2.6.1-2ubuntu0.3`

Licenses: (parsed from: `/usr/share/doc/libexpat1/copyright`)

- `MIT`

Source:

```console
$ apt-get source -qq --print-uris expat=2.6.1-2ubuntu0.3
'http://security.ubuntu.com/ubuntu/pool/main/e/expat/expat_2.6.1-2ubuntu0.3.dsc' expat_2.6.1-2ubuntu0.3.dsc 1474 SHA512:2331ab71158152f87fffa9e05e04b6f79bbeee7842cd957e3237847684b3508fb193850ca47049f1ed3284cc54d553183d9886de595a5ada114da20bf0119c69
'http://security.ubuntu.com/ubuntu/pool/main/e/expat/expat_2.6.1.orig.tar.gz' expat_2.6.1.orig.tar.gz 8414649 SHA512:cf6c64fc0ca55dd172ca8a6ca10d1fb2c915d0f941b0068f42cb90488022dea73e04119c49a1bd4ab9a5d425ddc132ae5f22260ff6d2e25204637a1169e7bd4f
'http://security.ubuntu.com/ubuntu/pool/main/e/expat/expat_2.6.1-2ubuntu0.3.debian.tar.xz' expat_2.6.1-2ubuntu0.3.debian.tar.xz 30100 SHA512:9b71cdafaacb1148f3e22cef6bde49f2701339a15c78ccf0df954c19bdba6b6f8ee778ab2227c8543f75bcc8b6e5f8e380e99d6d0c7ea4660526669e4d97df0e
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

Source:

```console
$ apt-get source -qq --print-uris findutils=4.9.0-5build1
'http://archive.ubuntu.com/ubuntu/pool/main/f/findutils/findutils_4.9.0-5build1.dsc' findutils_4.9.0-5build1.dsc 2404 SHA512:5cf7d85b815176d007607c61b6220ed1b9f921e1292b6ebe8603dcdc51c132040831b664c1da5a9e5c41afe350c7d9a6f6765b7f1404e36ed47aaa3735960680
'http://archive.ubuntu.com/ubuntu/pool/main/f/findutils/findutils_4.9.0.orig.tar.xz' findutils_4.9.0.orig.tar.xz 2046252 SHA512:ba4844f4403de0148ad14b46a3dbefd5a721f6257c864bf41a6789b11705408524751c627420b15a52af95564d8e5b52f0978474f640a62ab86a41d20cf14be9
'http://archive.ubuntu.com/ubuntu/pool/main/f/findutils/findutils_4.9.0.orig.tar.xz.asc' findutils_4.9.0.orig.tar.xz.asc 488 SHA512:b8e0b5471242912a20b9e468fa27b7f27339af5f7be8918173105262dee0152183bf4cf516844d348b206a694e028490d5d3b190f3aed8c698ba5444941f8dfc
'http://archive.ubuntu.com/ubuntu/pool/main/f/findutils/findutils_4.9.0-5build1.debian.tar.xz' findutils_4.9.0-5build1.debian.tar.xz 32864 SHA512:501c6e0100ac4a7b304700518c9d45c2f8a1f76bd5f12914c9b136e3b3d117115090177d5e6c863333982ca8ded70d188bbde2ff98d51c1d3c51ff247f5eb95b
```

### `dpkg` source package: `fontconfig=2.15.0-1.1ubuntu2`

Binary Packages:

- `fontconfig=2.15.0-1.1ubuntu2`
- `fontconfig-config=2.15.0-1.1ubuntu2`
- `libfontconfig1:amd64=2.15.0-1.1ubuntu2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris fontconfig=2.15.0-1.1ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/f/fontconfig/fontconfig_2.15.0-1.1ubuntu2.dsc' fontconfig_2.15.0-1.1ubuntu2.dsc 2817 SHA512:cd0eff27460c679b9d7db384bba94d4468f9cbf9d7bec41db6b12965f3d4ed48af35e73d3739d8ad8f5575bbc769379582e5e92e676dbe229260340f479c6d40
'http://archive.ubuntu.com/ubuntu/pool/main/f/fontconfig/fontconfig_2.15.0.orig.tar.xz' fontconfig_2.15.0.orig.tar.xz 1447820 SHA512:754cd5fffa198fc07a39cf7df683e9adfa7f54ab41fdff8c0eacc078fd35d3e01069ba343f2b045e0b40df88d9f1fc1ee0f7565799f9cb194a59cf95b64c4417
'http://archive.ubuntu.com/ubuntu/pool/main/f/fontconfig/fontconfig_2.15.0-1.1ubuntu2.debian.tar.xz' fontconfig_2.15.0-1.1ubuntu2.debian.tar.xz 30556 SHA512:a09fe533b6a684bc6e2bfc25eda89cad9f1020c3ba5738ff9799d770a3b6c09d6a12edfeeacffe38a73d8a3f28313e7108fa6f6acff70ba1eb346007f4bc73cb
```

### `dpkg` source package: `fonts-dejavu=2.37-8`

Binary Packages:

- `fonts-dejavu-core=2.37-8`
- `fonts-dejavu-mono=2.37-8`

Licenses: (parsed from: `/usr/share/doc/fonts-dejavu-core/copyright`, `/usr/share/doc/fonts-dejavu-mono/copyright`)

- `GPL-2`
- `GPL-2+`
- `bitstream-vera`

Source:

```console
$ apt-get source -qq --print-uris fonts-dejavu=2.37-8
'http://archive.ubuntu.com/ubuntu/pool/main/f/fonts-dejavu/fonts-dejavu_2.37-8.dsc' fonts-dejavu_2.37-8.dsc 2156 SHA512:c5632f8cf1fa690efc292e7ae8239265ac3a04e13423601d9a151b200ea36ae5242a0867428e3c7148c0cd5fa6b4ff3c368b53451f3234e20634f2fc6fe5c1fa
'http://archive.ubuntu.com/ubuntu/pool/main/f/fonts-dejavu/fonts-dejavu_2.37.orig.tar.bz2' fonts-dejavu_2.37.orig.tar.bz2 12050109 SHA512:e61fc8c675ef76edb49dd9a8caee62087280929bb8144b52aca2f8def30025c56246589ad8a6a806b9574e6876eedd16d57c70a6ce9c86817a2dfe39d8a2bb2b
'http://archive.ubuntu.com/ubuntu/pool/main/f/fonts-dejavu/fonts-dejavu_2.37-8.debian.tar.xz' fonts-dejavu_2.37-8.debian.tar.xz 13176 SHA512:7a19189a106a1243c64d43b050f87cba6f6c32d070f246aceb5ccc687401366825a31a653e45fa700e1593f7ed32340581988cfc1a489b5f8b705e80c2a891ee
```

### `dpkg` source package: `freetype=2.13.2+dfsg-1build3`

Binary Packages:

- `libfreetype6:amd64=2.13.2+dfsg-1build3`

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
$ apt-get source -qq --print-uris freetype=2.13.2+dfsg-1build3
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.13.2%2bdfsg-1build3.dsc' freetype_2.13.2+dfsg-1build3.dsc 3805 SHA512:a5d5084abbf710ff0cd16a2f268f6ae71db390ee4bbfd99ca30d37411a2a85cc81034618e05c6520fe061598a0dd5569aaa5fbf497cc43ab57e77a31da8925d8
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.13.2%2bdfsg.orig-ft2demos.tar.xz' freetype_2.13.2+dfsg.orig-ft2demos.tar.xz 341140 SHA512:aa83ba4212ff7c4453b72f036136cb9b04cacf7d196388a3e4752613e000b3bb45a4dcf63d3d1d5b3d6ada10720304b532fb6e33ed6a5b399dcce45c27af9ade
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.13.2%2bdfsg.orig-ft2demos.tar.xz.asc' freetype_2.13.2+dfsg.orig-ft2demos.tar.xz.asc 833 SHA512:07680e2919643cb1b964c311f1590fddd38f42189944b3e5e46a9c6a84688255749506f8a745d52255e3599e5136f3e8761d746a67cdcd6e565b8eaecb9fd792
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.13.2%2bdfsg.orig-ft2docs.tar.xz' freetype_2.13.2+dfsg.orig-ft2docs.tar.xz 2173920 SHA512:ca3438dcf6f995af556d8db3cb3cfdcabb81ab5a7dd88464ff757e3e418b3219b0011857cde8a338372e30d8375486ac8e50914da2ea948dc874f70010bce60c
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.13.2%2bdfsg.orig-ft2docs.tar.xz.asc' freetype_2.13.2+dfsg.orig-ft2docs.tar.xz.asc 833 SHA512:b346579fcc8f073e586135c72140c64bb3d5ca46201b879e3976b39a62a14f6668a5009d39b078e51d51a7301e346b4de6f7e9ee365f9b44146e67579aaf6500
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.13.2%2bdfsg.orig.tar.xz' freetype_2.13.2+dfsg.orig.tar.xz 2220368 SHA512:8809693981ea7ef274d882245e3257305b65ad73e5ae36bb7e4ffc769a97b726d6bd07f1627dae456519e02e3eaa43269769d7ad363f49b9247d27d2c6f47d6d
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.13.2%2bdfsg-1build3.debian.tar.xz' freetype_2.13.2+dfsg-1build3.debian.tar.xz 44000 SHA512:d0559397ed00e767a30915f9562a2c75d93d059a7f69100fea092b9c4a45d09ad07fac55e669eae145893a326b2f984105c65ad4bed7a29077b99cda579a4e0b
```

### `dpkg` source package: `gcc-14=14.2.0-4ubuntu2~24.04`

Binary Packages:

- `gcc-14-base:amd64=14.2.0-4ubuntu2~24.04`
- `libgcc-s1:amd64=14.2.0-4ubuntu2~24.04`
- `libstdc++6:amd64=14.2.0-4ubuntu2~24.04`

Licenses: (parsed from: `/usr/share/doc/gcc-14-base/copyright`, `/usr/share/doc/libgcc-s1/copyright`, `/usr/share/doc/libstdc++6/copyright`)

- `Artistic`
- `GFDL-1.2`
- `GPL`
- `GPL-3`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris gcc-14=14.2.0-4ubuntu2~24.04
'http://security.ubuntu.com/ubuntu/pool/main/g/gcc-14/gcc-14_14.2.0-4ubuntu2%7e24.04.dsc' gcc-14_14.2.0-4ubuntu2~24.04.dsc 46922 SHA512:95abfd5811a313d7f7571376f927cd956a29d33927b4ffe37f2d795dfa4475e371795b25977373617df61c32f85b87fcf46f2f66a1c67147e82a68db3c5d279f
'http://security.ubuntu.com/ubuntu/pool/main/g/gcc-14/gcc-14_14.2.0.orig.tar.gz' gcc-14_14.2.0.orig.tar.gz 97158172 SHA512:88621e344786a78d825110dbd46a9dc811ab0a3414bde97a700b0c90991020dc31dbba89cdbed24ef2875a63ae9c0adffdbc1064262e5270d80920c9964bfb21
'http://security.ubuntu.com/ubuntu/pool/main/g/gcc-14/gcc-14_14.2.0-4ubuntu2%7e24.04.debian.tar.xz' gcc-14_14.2.0-4ubuntu2~24.04.debian.tar.xz 1950240 SHA512:2b1894ebcb104b85da3c614e0a6c2e24b1f6c1f548645996d2cb0d274301284f1f4db0809c8355997b05fe64b76a73ee1b9499c7b1c229547bad79fee1954d59
```

### `dpkg` source package: `glibc=2.39-0ubuntu8.6`

Binary Packages:

- `libc-bin=2.39-0ubuntu8.6`
- `libc6:amd64=2.39-0ubuntu8.6`
- `locales=2.39-0ubuntu8.6`

Licenses: (parsed from: `/usr/share/doc/libc-bin/copyright`, `/usr/share/doc/libc6/copyright`, `/usr/share/doc/locales/copyright`)

- `GFDL-1.3`
- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris glibc=2.39-0ubuntu8.6
'http://security.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.39-0ubuntu8.6.dsc' glibc_2.39-0ubuntu8.6.dsc 9387 SHA512:6467b02c2dcf5a07856a3526ece393fdcd0f7c6aa9d22f20fd42a45a02ad050f995dabd7068f1ddd9aee6ab5ae7810590e00173ecf2ded40231c880d9bf28fe8
'http://security.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.39.orig.tar.xz' glibc_2.39.orig.tar.xz 18520988 SHA512:818f58172a52815b4338ea9f2a69ecaa3335492b9f8f64cbf8afb24c0d737982341968ecd79631cae3d3074ab0ae4bc6056fc4ba3ffe790849dc374835cd57e2
'http://security.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.39.orig.tar.xz.asc' glibc_2.39.orig.tar.xz.asc 833 SHA512:5c054af523bbf5c2453363c023eadd1a75b6a5ff55c739011030115d3b117dbfc7d80cc74fbf157ea74a8d24aa14ff560c675374f875ec5c1ed3030e26a5ee07
'http://security.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.39-0ubuntu8.6.debian.tar.xz' glibc_2.39-0ubuntu8.6.debian.tar.xz 467000 SHA512:5670e98edb2396b6f9fcf021c1f3da5fbb95ba7330e309f9039a5d0a3f148f4298454de70c565fdf9dfeb97edb4e9de6eeb65bd8e19d054c6346642867172d03
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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `gnupg2=2.4.4-2ubuntu17.4`

Binary Packages:

- `dirmngr=2.4.4-2ubuntu17.4`
- `gnupg=2.4.4-2ubuntu17.4`
- `gnupg-utils=2.4.4-2ubuntu17.4`
- `gpg=2.4.4-2ubuntu17.4`
- `gpg-agent=2.4.4-2ubuntu17.4`
- `gpgconf=2.4.4-2ubuntu17.4`
- `gpgsm=2.4.4-2ubuntu17.4`
- `gpgv=2.4.4-2ubuntu17.4`
- `keyboxd=2.4.4-2ubuntu17.4`

Licenses: (parsed from: `/usr/share/doc/dirmngr/copyright`, `/usr/share/doc/gnupg/copyright`, `/usr/share/doc/gnupg-utils/copyright`, `/usr/share/doc/gpg/copyright`, `/usr/share/doc/gpg-agent/copyright`, `/usr/share/doc/gpgconf/copyright`, `/usr/share/doc/gpgsm/copyright`, `/usr/share/doc/gpgv/copyright`, `/usr/share/doc/keyboxd/copyright`)

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
'http://security.ubuntu.com/ubuntu/pool/main/g/gnupg2/gnupg2_2.4.4-2ubuntu17.4.dsc' gnupg2_2.4.4-2ubuntu17.4.dsc 3984 SHA512:a6a2f49070db5db2bb85b7fd916728ed4e24e21e2746b2386b27f5573c13f9c2d9d55deabeac1fd9c0ce977d66706157a31e1ed386d663d1962176d3c0df74de
'http://security.ubuntu.com/ubuntu/pool/main/g/gnupg2/gnupg2_2.4.4.orig.tar.bz2' gnupg2_2.4.4.orig.tar.bz2 7886036 SHA512:3d1a3b08d1ce2319d238d8be96591e418ede1dc0b4ede33a4cc2fe40e9c56d5bbc27b1984736d8a786e7f292ddbc836846a8bdb4bf89f064e953c37cb54b94ef
'http://security.ubuntu.com/ubuntu/pool/main/g/gnupg2/gnupg2_2.4.4.orig.tar.bz2.asc' gnupg2_2.4.4.orig.tar.bz2.asc 386 SHA512:abb44c8bfa59e589bdcd660f1d1a2e268bade8729d95b34263e3d3b5388d1d2276420313989777938f17f97739c554808f97a63257ca0f53d2122a346d70ec85
'http://security.ubuntu.com/ubuntu/pool/main/g/gnupg2/gnupg2_2.4.4-2ubuntu17.4.debian.tar.xz' gnupg2_2.4.4-2ubuntu17.4.debian.tar.xz 97376 SHA512:61b874e2aa964df31649d1344281b7f99f1bde0b414719f1ff525f2e631729480d0eabf3c3e94643178a6674b3816e40ea92658e84ace8474351ef35620a464b
```

### `dpkg` source package: `gnutls28=3.8.3-1.1ubuntu3.4`

Binary Packages:

- `libgnutls30t64:amd64=3.8.3-1.1ubuntu3.4`

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
$ apt-get source -qq --print-uris gnutls28=3.8.3-1.1ubuntu3.4
'http://security.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.8.3-1.1ubuntu3.4.dsc' gnutls28_3.8.3-1.1ubuntu3.4.dsc 3397 SHA512:f0ba3871d3cf4b1325b0c0efa412146468fbf2fb0007972427cef545c6e84694b647b3a420e34ebfa689ccc3e2cc00166f42f84cb57f46c6d3fe9b9c6462af78
'http://security.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.8.3.orig.tar.xz' gnutls28_3.8.3.orig.tar.xz 6463720 SHA512:74eddba01ce4c2ffdca781c85db3bb52c85f1db3c09813ee2b8ceea0608f92ca3912fd9266f55deb36a8ba4d01802895ca5d5d219e7d9caec45e1a8534e45a84
'http://security.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.8.3.orig.tar.xz.asc' gnutls28_3.8.3.orig.tar.xz.asc 854 SHA512:8a13a834b57172b9504313eeb7d733d2c3d72971dd8adaa837bbd9d73b12fe2a67f7d07fbbaf643a34ff95acaa82458a88ce4118152ede8ece9be5a089b693c8
'http://security.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.8.3-1.1ubuntu3.4.debian.tar.xz' gnutls28_3.8.3-1.1ubuntu3.4.debian.tar.xz 100104 SHA512:aab92b406ef2b833d663f7662fd2ac61cada09251710b44d689c1ff73bbc5b451dce04675893a752392564048b78b19118ce23532d9ce7e726a678d92e7e3d1d
```

### `dpkg` source package: `grep=3.11-4build1`

Binary Packages:

- `grep=3.11-4build1`

Licenses: (parsed from: `/usr/share/doc/grep/copyright`)

- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris grep=3.11-4build1
'http://archive.ubuntu.com/ubuntu/pool/main/g/grep/grep_3.11-4build1.dsc' grep_3.11-4build1.dsc 2379 SHA512:5106f25775f36ba92fd7d73634d8c271fcea7dc9defef2f84d6080eb6a47dd0b1194272807267413807aa35d945c9bb66f076162d3eba539cc35eca5d255d2f9
'http://archive.ubuntu.com/ubuntu/pool/main/g/grep/grep_3.11.orig.tar.xz' grep_3.11.orig.tar.xz 1703776 SHA512:f254a1905a08c8173e12fbdd4fd8baed9a200217fba9d7641f0d78e4e002c1f2a621152d67027d9b25f0bb2430898f5233dc70909d8464fd13d7dd9298e65c42
'http://archive.ubuntu.com/ubuntu/pool/main/g/grep/grep_3.11.orig.tar.xz.asc' grep_3.11.orig.tar.xz.asc 833 SHA512:487aba063373ca0594c519991f19b2a6a33b3da0d74735c890f3828fd0880e7e6f64495d2c8f9efa5da53d1eb2d446609bab2399a4b89dcb4510a632e31ffb54
'http://archive.ubuntu.com/ubuntu/pool/main/g/grep/grep_3.11-4build1.debian.tar.xz' grep_3.11-4build1.debian.tar.xz 20584 SHA512:212c903c240071dda1d8e966991908730af26746558078262aa32b6b0683487cb510d9b9a2c40cafb31024e78e2c74d17eb5681e329aa142b0921b88cacef7eb
```

### `dpkg` source package: `gzip=1.12-1ubuntu3.1`

Binary Packages:

- `gzip=1.12-1ubuntu3.1`

Licenses: (parsed from: `/usr/share/doc/gzip/copyright`)

- `FSF-manpages`
- `GFDL-1.3+-no-invariant`
- `GFDL-3`
- `GPL-3`
- `GPL-3+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `hostname=3.23+nmu2ubuntu2`

Binary Packages:

- `hostname=3.23+nmu2ubuntu2`

Licenses: (parsed from: `/usr/share/doc/hostname/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris hostname=3.23+nmu2ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/h/hostname/hostname_3.23%2bnmu2ubuntu2.dsc' hostname_3.23+nmu2ubuntu2.dsc 1567 SHA512:a61538c601492aaba10aafc2b181f3db3f7f0ef768ce5fe4da1c4dece8655247627a77df89a7700938c665792cd134a46bfa8dd20ae59e7d0ccc199bd43b06a6
'http://archive.ubuntu.com/ubuntu/pool/main/h/hostname/hostname_3.23%2bnmu2ubuntu2.tar.xz' hostname_3.23+nmu2ubuntu2.tar.xz 13276 SHA512:ce7606f7bd3be9a2a2089955c1510244c8b5ef76d9e1978547870f2ff6e5fbb6cd12c040f38dc5473c46a2d77e7e7257da5787638cf5619adcced206c2c34419
```

### `dpkg` source package: `init-system-helpers=1.66ubuntu1`

Binary Packages:

- `init-system-helpers=1.66ubuntu1`

Licenses: (parsed from: `/usr/share/doc/init-system-helpers/copyright`)

- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris init-system-helpers=1.66ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/i/init-system-helpers/init-system-helpers_1.66ubuntu1.dsc' init-system-helpers_1.66ubuntu1.dsc 2353 SHA512:f6aafcef04d63b54d6ff273312ff2a9194345b8725bfbbaac69793a3d016cbda730f2de8de9862d8038c36ca0fba39b868d6d640701ccf8db417094816d0e9db
'http://archive.ubuntu.com/ubuntu/pool/main/i/init-system-helpers/init-system-helpers_1.66ubuntu1.tar.xz' init-system-helpers_1.66ubuntu1.tar.xz 45100 SHA512:222f73347b0ce9eb137c8ce5dc36e9fedbc8dc5ed3f1fde7fbf52258a5437d0a10d3d610ca1d1b206646bb92a5355d1061705440b2d22d9109b5de6d1cb92e98
```

### `dpkg` source package: `jansson=2.14-2build2`

Binary Packages:

- `libjansson4:amd64=2.14-2build2`

Licenses: (parsed from: `/usr/share/doc/libjansson4/copyright`)

- `Expat`

Source:

```console
$ apt-get source -qq --print-uris jansson=2.14-2build2
'http://archive.ubuntu.com/ubuntu/pool/main/j/jansson/jansson_2.14-2build2.dsc' jansson_2.14-2build2.dsc 2120 SHA512:46ec9f5477e738ee6ed2c10b7406dd0edcfe0148a394af3ca3ee214b14c9de95e691fefa34c3aa9770c1e23ec77d26b1f5149cc8faa4201f15680ba9f3a6d754
'http://archive.ubuntu.com/ubuntu/pool/main/j/jansson/jansson_2.14.orig.tar.gz' jansson_2.14.orig.tar.gz 141500 SHA512:c56e2e8d18819e3f5caa46edd4819694a240aeb3524a6f9d9f4465edf65b183d1870bd5d256cdd378d411a52979121369b951406fdf7bf323db5c30001fa1bc4
'http://archive.ubuntu.com/ubuntu/pool/main/j/jansson/jansson_2.14-2build2.debian.tar.xz' jansson_2.14-2build2.debian.tar.xz 5580 SHA512:1eec1f274a77512033b857a64bb26f8bc2fa98212c33c17dcfedbbd7f82711d32a803ad4ea4d8d158ef9949be2a69f3d5d4126fc4ac3b63c9200c361bba0f939
```

### `dpkg` source package: `keyutils=1.6.3-3build1`

Binary Packages:

- `libkeyutils1:amd64=1.6.3-3build1`

Licenses: (parsed from: `/usr/share/doc/libkeyutils1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2`
- `LGPL-2+`

Source:

```console
$ apt-get source -qq --print-uris keyutils=1.6.3-3build1
'http://archive.ubuntu.com/ubuntu/pool/main/k/keyutils/keyutils_1.6.3-3build1.dsc' keyutils_1.6.3-3build1.dsc 2211 SHA512:8a40b63e5c4ef4ae645ffdfc865ed91192a7dfc65c8271e59388e63d867b43ac0da90ca1f5e85682886e4561681b83f3bf8bc6a3d90f205dd0feea116f7a30b8
'http://archive.ubuntu.com/ubuntu/pool/main/k/keyutils/keyutils_1.6.3.orig.tar.gz' keyutils_1.6.3.orig.tar.gz 137022 SHA512:f65965b8566037078b8eeffa66c6fdbe121c8c2bea7fa5bce04cf7ba5ccc50d5b48e51f4a67ca91e4d5d9a12469e7e3eb3036c920ab25e3feba6e93b4c149cf9
'http://archive.ubuntu.com/ubuntu/pool/main/k/keyutils/keyutils_1.6.3-3build1.debian.tar.xz' keyutils_1.6.3-3build1.debian.tar.xz 13456 SHA512:ef729447f8f4adebdb986d115e227bd908b346e26115eb7a0385a084ad69f6772c914744d8c24928587247cd5fc329ed1305e9b006db276d0445b9614f20603f
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
'http://security.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.20.1-6ubuntu2.6.dsc' krb5_1.20.1-6ubuntu2.6.dsc 4125 SHA512:6bafe41a37f8bf133ccd7e1aa0d63a1464b411af60ee408a03de69debae259794606011ff42370d168f6bf74af34d90b635c007c9876657af7124259af84c99a
'http://security.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.20.1.orig.tar.gz' krb5_1.20.1.orig.tar.gz 8661660 SHA512:6f57479f13f107cd84f30de5c758eb6b9fc59171329c13e5da6073b806755f8d163eb7bd84767ea861ad6458ea0c9eeb00ee044d3bcad01ef136e9888564b6a2
'http://security.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.20.1.orig.tar.gz.asc' krb5_1.20.1.orig.tar.gz.asc 833 SHA512:1d3312bd67581e07adfdadf2c5fe394179631d8add8bd075efefe982a0de22369004e60a14422d426382c8c591e4181b9897088afe9d4e86f0b5a97e5954c67a
'http://security.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.20.1-6ubuntu2.6.debian.tar.xz' krb5_1.20.1-6ubuntu2.6.debian.tar.xz 122284 SHA512:402e34a374db1ece1ce0a604d84d697c590596d5e99601895d9c50c96fcbd8cb08d21b04201296411324b3ae4f169f2295aff825cee182cbbf139ccb16588fc9
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

Source:

```console
$ apt-get source -qq --print-uris libassuan=2.5.6-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/liba/libassuan/libassuan_2.5.6-1build1.dsc' libassuan_2.5.6-1build1.dsc 2734 SHA512:5a430eef8b98b19d7750ab96717a36749fd586533290ae3ab0129d4d7236f34c524e5fcdb7cc1105cf1fa16c64f604956ef36af0eb952cbf1308b61819364f57
'http://archive.ubuntu.com/ubuntu/pool/main/liba/libassuan/libassuan_2.5.6.orig.tar.bz2' libassuan_2.5.6.orig.tar.bz2 577012 SHA512:dcca942d222a2c226a7e34ba7988ee0c3c55bd6032166eb472caf2053db89aeeea7a40e93d8c2887c7ee73c5f838e8b0725e8cfb595accc1606646559362f7ee
'http://archive.ubuntu.com/ubuntu/pool/main/liba/libassuan/libassuan_2.5.6.orig.tar.bz2.asc' libassuan_2.5.6.orig.tar.bz2.asc 228 SHA512:aaa1222607320c260d7339a95cca6532947782520b07df3198a5a228129e0247b87f6f3b6fea17590147fbc7345ea36bfa8da45116d3d85c6fc2d4a3df0f629b
'http://archive.ubuntu.com/ubuntu/pool/main/liba/libassuan/libassuan_2.5.6-1build1.debian.tar.xz' libassuan_2.5.6-1build1.debian.tar.xz 14412 SHA512:a09775ff7ab780566ec1385cacb7dcd34b8b418f4472b5285b57d442ab21a4482fa720c43fdd81dda7e042300ff7ff97efa0bdb0ebdf7aa29d71b83ae3ee7b00
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

Source:

```console
$ apt-get source -qq --print-uris libcap-ng=0.8.4-2build2
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap-ng/libcap-ng_0.8.4-2build2.dsc' libcap-ng_0.8.4-2build2.dsc 2351 SHA512:bbe5c806e1495dbdd84b80217db334517f792caff349575687e181371c81b2ab503bc120d73eb91bdd084d2a86bec16c852f800fec60ef3ae5c237776f5122f7
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap-ng/libcap-ng_0.8.4.orig.tar.gz' libcap-ng_0.8.4.orig.tar.gz 59317 SHA512:3e640ba4bfa2d5b5d0eb463abca3b2c745b10e929571c0ec32eb068bdc41fd95e19f7131893a22ceebb4d1f1083d3d87d9a32f0808442d594ac5940791152acf
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap-ng/libcap-ng_0.8.4-2build2.debian.tar.xz' libcap-ng_0.8.4-2build2.debian.tar.xz 7384 SHA512:c21cf4b7df670034773ab883e5149bc28606d11416a5f075c85106395a6d46ea529227e270f9342c910631059b8cf94a55dc5cfa5ec908a6f57d6a8c0a32277e
```

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
'http://security.ubuntu.com/ubuntu/pool/main/libc/libcap2/libcap2_2.66-5ubuntu2.2.dsc' libcap2_2.66-5ubuntu2.2.dsc 2319 SHA512:563c9151918f788fb7ea210505c3f2f4c6375af6fa58f760d4efd051ac3bcb9a0dff8fc0407486c834b5a477831af8a50aaeb14728c93ffe88edf48e2a86391f
'http://security.ubuntu.com/ubuntu/pool/main/libc/libcap2/libcap2_2.66.orig.tar.xz' libcap2_2.66.orig.tar.xz 181592 SHA512:ac005b622f6e065f30ce282a5c87240e7b9da75366ee537aa4835bc501b44bc242c10a4ba4dc070e2415fc7f635d1c3c4e45fbeeaf962cf7973dda82bf6377f0
'http://security.ubuntu.com/ubuntu/pool/main/libc/libcap2/libcap2_2.66-5ubuntu2.2.debian.tar.xz' libcap2_2.66-5ubuntu2.2.debian.tar.xz 23076 SHA512:fd58def706a8d3f3f594ad986bf9385c2cba8af6f73f4bb04011815fe8b1e700368a2a15e7390842b3aba9ae72de9928009731bf1f318b48d8975e505f8f7f33
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

Source:

```console
$ apt-get source -qq --print-uris libffi=3.4.6-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libffi/libffi_3.4.6-1build1.dsc' libffi_3.4.6-1build1.dsc 2055 SHA512:21cc7b6880fac7c143e88a81c47e5144d38bea3fd66f71182d1408f56bfc6801d39481638e04c02bb29dfc2429e3d968b65591cf95d20cfeca6769684d3c86ac
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libffi/libffi_3.4.6.orig.tar.gz' libffi_3.4.6.orig.tar.gz 598175 SHA512:cbacde8911aa6a9fae5c0a8d5959221a25bf8a3310c44a7f4ef755e6676f5226b9f2d1c6cfb36c117ebed10d379aa24b4b7516c3e0dca3bf73f9439057463eb8
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libffi/libffi_3.4.6-1build1.debian.tar.xz' libffi_3.4.6-1build1.debian.tar.xz 10736 SHA512:432e6e7ddb9aecca508f982293112b2bf86f5da2d6d646437b10b2857dadaf2c8aecb1646d2e592c259df26a5240f69cc1411155cbad8c3d942748d6856e587c
```

### `dpkg` source package: `libgcrypt20=1.10.3-2build1`

Binary Packages:

- `libgcrypt20:amd64=1.10.3-2build1`

Licenses: (parsed from: `/usr/share/doc/libgcrypt20/copyright`)

- `GPL-2`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris libgcrypt20=1.10.3-2build1
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgcrypt20/libgcrypt20_1.10.3-2build1.dsc' libgcrypt20_1.10.3-2build1.dsc 2931 SHA512:bb535ccbaaac49199a4483dbf31799f9b4ecccdeec42294baa850879187df7afe57f187c7f16ec3e248905f99e01ba3a46b7a56e23780596716e8e8f4237b772
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgcrypt20/libgcrypt20_1.10.3.orig.tar.bz2' libgcrypt20_1.10.3.orig.tar.bz2 3783827 SHA512:8a8d4c61a6622d8481ceb9edc88ec43f58da32e316f79f8d4775325a48f8936aaa9eb355923b39e2c267b784e9c390600daeb62e0c94f00e30bbadb0d8c0865d
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgcrypt20/libgcrypt20_1.10.3.orig.tar.bz2.asc' libgcrypt20_1.10.3.orig.tar.bz2.asc 390 SHA512:9b176a7bca3b8521fe03c3f771a3d039c4e1da98f6ce61f6c1bbb485e5785ca58e191c4eb54d6c69a1ae79e82d786c22836bef96d30d7b9852b508f3b65fb15a
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgcrypt20/libgcrypt20_1.10.3-2build1.debian.tar.xz' libgcrypt20_1.10.3-2build1.debian.tar.xz 36604 SHA512:f203bb66fdbc4f45c512c768e36e13510bdf26eb04e8f78940299dc5bfed9ddf624a65a0a49b734314dee9362a178721d148aaf6b9723bcd9c7e627a52816a75
```

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libksba=1.6.6-1build1`

Binary Packages:

- `libksba8:amd64=1.6.6-1build1`

Licenses: (parsed from: `/usr/share/doc/libksba8/copyright`)

- `FSFUL`
- `GPL-3`
- `LGPL-2.1-or-later`

Source:

```console
$ apt-get source -qq --print-uris libksba=1.6.6-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/libk/libksba/libksba_1.6.6-1build1.dsc' libksba_1.6.6-1build1.dsc 2622 SHA512:9905b22e5b0cdce554951103b8fe95a259aca936f96e90380538f05065d3f1b27a7eee8f54f9372731413c245aa2506614baa8567cdba1a56850765dfb8572fd
'http://archive.ubuntu.com/ubuntu/pool/main/libk/libksba/libksba_1.6.6.orig.tar.bz2' libksba_1.6.6.orig.tar.bz2 708510 SHA512:3b30bef9452ae0c52b4a52e9145fbd6dc57cf7a2b59302e3af063db6b45384e8ed7af62604efd7939b9e0cb5931e946b15609888e9699fafe4acbb0cbf138087
'http://archive.ubuntu.com/ubuntu/pool/main/libk/libksba/libksba_1.6.6.orig.tar.bz2.asc' libksba_1.6.6.orig.tar.bz2.asc 228 SHA512:5bfd9441b3e46b24391c5d9360747c9eaabf9d645ceae27af241d4ed1f7e9cc0fb538dc6d8db757d444eefa8d45b2082fd055256160c59d97bf5121f05d750ef
'http://archive.ubuntu.com/ubuntu/pool/main/libk/libksba/libksba_1.6.6-1build1.debian.tar.xz' libksba_1.6.6-1build1.debian.tar.xz 14816 SHA512:12251deb546de2d2ba6dc2a7f8c01a22218579de7e9a16ae6ecf728e07404fc601bd85f43ce907c056dfdbe9c584887acef9f9a5a7090c75a3fb2c8d2e50d0c3
```

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libpng1.6=1.6.43-5ubuntu0.3`

Binary Packages:

- `libpng16-16t64:amd64=1.6.43-5ubuntu0.3`

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
$ apt-get source -qq --print-uris libpng1.6=1.6.43-5ubuntu0.3
'http://security.ubuntu.com/ubuntu/pool/main/libp/libpng1.6/libpng1.6_1.6.43-5ubuntu0.3.dsc' libpng1.6_1.6.43-5ubuntu0.3.dsc 2384 SHA512:a4a024fbfe9728cb52028d729326427f945e529aeaf844b889d01eb4f4efa7b7a049ab3648895e2f8155d08b841467029371a36c12c14b21dac3234e1541bec8
'http://security.ubuntu.com/ubuntu/pool/main/libp/libpng1.6/libpng1.6_1.6.43.orig.tar.gz' libpng1.6_1.6.43.orig.tar.gz 1554715 SHA512:3bb2a7b73113be42b09c2116e6c6f5a7ddb4e2ab06e0b13e10b7314acdccc4bb624ff602e16140c0484f6cde80efa190296226be3da195c6926819f07c723c12
'http://security.ubuntu.com/ubuntu/pool/main/libp/libpng1.6/libpng1.6_1.6.43-5ubuntu0.3.debian.tar.xz' libpng1.6_1.6.43-5ubuntu0.3.debian.tar.xz 38892 SHA512:e137bcb58708ed1e5658fab2e92587a2c251293c0a3bb86b1e2877d3cd98f6889314ba7c438bc505f7a011d98b15ee4edd933c946394ebf09c0eb2a6f9348a42
```

### `dpkg` source package: `libpsl=0.21.2-1.1build1`

Binary Packages:

- `libpsl5t64:amd64=0.21.2-1.1build1`

Licenses: (parsed from: `/usr/share/doc/libpsl5t64/copyright`)

- `Chromium`
- `MIT`
- `gnulib`

Source:

```console
$ apt-get source -qq --print-uris libpsl=0.21.2-1.1build1
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpsl/libpsl_0.21.2-1.1build1.dsc' libpsl_0.21.2-1.1build1.dsc 2425 SHA512:f6036e1386802ab44ad0d65b81f4e81dd2ac084da738752f058d58f8d96074b2ab7b00e8275cdd73bedb18d5ae6ba1fc4b19fb95d4b61e58df5695225629ef7c
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpsl/libpsl_0.21.2.orig.tar.xz' libpsl_0.21.2.orig.tar.xz 1870352 SHA512:5308feee863b84705246ce303c093e0c9fecd948ab382fd7480e9ea1ca5f72de42fc2c8f70472a97603580a3fd1eb2b552b093d79756e9fe93effba9f25b6aa4
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpsl/libpsl_0.21.2-1.1build1.debian.tar.xz' libpsl_0.21.2-1.1build1.debian.tar.xz 12244 SHA512:316b41dc3611a45c0b7ab0ec7fc617d2c710f8e11d943daefa524fc92155b63e777504a11dbe1b8427e1ad6d15f98095c90cd115df71fb8f90449a461dc9cd3d
```

### `dpkg` source package: `libseccomp=2.5.5-1ubuntu3.1`

Binary Packages:

- `libseccomp2:amd64=2.5.5-1ubuntu3.1`

Licenses: (parsed from: `/usr/share/doc/libseccomp2/copyright`)

- `LGPL-2.1`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libselinux=3.5-2ubuntu2.1`

Binary Packages:

- `libselinux1:amd64=3.5-2ubuntu2.1`

Licenses: (parsed from: `/usr/share/doc/libselinux1/copyright`)

- `GPL-2`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libsemanage=3.5-1build5`

Binary Packages:

- `libsemanage-common=3.5-1build5`
- `libsemanage2:amd64=3.5-1build5`

Licenses: (parsed from: `/usr/share/doc/libsemanage-common/copyright`, `/usr/share/doc/libsemanage2/copyright`)

- `GPL-2`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris libsemanage=3.5-1build5
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsemanage/libsemanage_3.5-1build5.dsc' libsemanage_3.5-1build5.dsc 3105 SHA512:310dd2c109462b4f44ddaef331f6a72758efd42d31591daba762fc629e2915c6dc6a16fccbb933089a406aea65b886e3408e10b49e2471abbad37a30c260ed0d
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsemanage/libsemanage_3.5.orig.tar.gz' libsemanage_3.5.orig.tar.gz 185060 SHA512:959fbd0d6bc6849da6caa13dc41c3f8818cbbd29f04b5d2ac7246c4b395b4f370f113a04cc9cfcb52be2afebfa636013ac4ad4011384c58c7ce066a45cae2751
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsemanage/libsemanage_3.5.orig.tar.gz.asc' libsemanage_3.5.orig.tar.gz.asc 981 SHA512:c0a5ddb69c32ddefa26b3d1ec676bcc373e959dd8b4a7fcf6e1f74a3ca8e9af22af851ca66d3c43a704215ff79d27244e33d23038ef2f52ccc321aeb5f0c2790
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsemanage/libsemanage_3.5-1build5.debian.tar.xz' libsemanage_3.5-1build5.debian.tar.xz 30188 SHA512:13561dae7133d128bc5db3528e38be2e9469e35a4796e92f192af3c95c29abb3934542244777d0f0754cc1f652ea816334b7fc5fe94d637fb35bf76a399059cd
```

### `dpkg` source package: `libsepol=3.5-2build1`

Binary Packages:

- `libsepol2:amd64=3.5-2build1`

Licenses: (parsed from: `/usr/share/doc/libsepol2/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris libsepol=3.5-2build1
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsepol/libsepol_3.5-2build1.dsc' libsepol_3.5-2build1.dsc 2458 SHA512:d28b899278cfcb721f13e512142e2540c2ec064458d6d5bee607b3b313b260a2a19e5d5131fc7dcde6edfbf24d73eaede6597444770d6be31011d861a1d72676
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsepol/libsepol_3.5.orig.tar.gz' libsepol_3.5.orig.tar.gz 497522 SHA512:66f45a9f4951589855961955db686b006b4c0cddead6ac49ad238a0e4a34775905bd10fb8cf0c0ff2ab64f9b7d8366b97fcd5b19c382dec39971a2835cc765c8
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsepol/libsepol_3.5.orig.tar.gz.asc' libsepol_3.5.orig.tar.gz.asc 981 SHA512:5aa46c3a7a5d7fa0d4376766b9444cdea1b14f3ec61725950a24fcb5ba2caae271a415c613807d06e4d9b04b40cda1525c12c442eed8a7e60fb5e5beacdaba3b
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsepol/libsepol_3.5-2build1.debian.tar.xz' libsepol_3.5-2build1.debian.tar.xz 27716 SHA512:9b2b126368c5e4f80d80940f7611103745b1da92bec6319f43f64cc3f6a5e13bab25758bad645e973773a4aab74fa3600694061a8368ca2176252320c0d9ebf6
```

### `dpkg` source package: `libssh=0.10.6-2ubuntu0.2`

Binary Packages:

- `libssh-4:amd64=0.10.6-2ubuntu0.2`

Licenses: (parsed from: `/usr/share/doc/libssh-4/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `LGPL-2.1`
- `LGPL-2.1+~OpenSSL`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris libssh=0.10.6-2ubuntu0.2
'http://security.ubuntu.com/ubuntu/pool/main/libs/libssh/libssh_0.10.6-2ubuntu0.2.dsc' libssh_0.10.6-2ubuntu0.2.dsc 2723 SHA512:0ce4ad1a7c238fa3dca8523f49833309c47aa55535c7d438d0c7d6a985e5346d2071d791c1847cbeea76502ca73276e1235dda81f075fc3e0ce90240656065f0
'http://security.ubuntu.com/ubuntu/pool/main/libs/libssh/libssh_0.10.6.orig.tar.xz' libssh_0.10.6.orig.tar.xz 561036 SHA512:40c62d63c44e882999b71552c237d73fc7364313bd00b15a211a34aeff1b73693da441d2c8d4e40108d00fb7480ec7c5b6d472f9c0784b2359a179632ab0d6c1
'http://security.ubuntu.com/ubuntu/pool/main/libs/libssh/libssh_0.10.6.orig.tar.xz.asc' libssh_0.10.6.orig.tar.xz.asc 833 SHA512:214d7920bebc80a8e6838c64ed06e070709a96fabfb4fff657b55f9588bc0e1612887fe887d23de73ad3540f3bb85288e62eb6a11ccd4bc80afbd44d34ba70d4
'http://security.ubuntu.com/ubuntu/pool/main/libs/libssh/libssh_0.10.6-2ubuntu0.2.debian.tar.xz' libssh_0.10.6-2ubuntu0.2.debian.tar.xz 47820 SHA512:92e9d5c401b22570cabac5c80c984b809d8fbcc537b464b7e5ec69eae254046cb56bb1d5029cc7ac11c0e8010f5501bf8495261f1022770eded064e4f6bb637c
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
'http://security.ubuntu.com/ubuntu/pool/main/libt/libtasn1-6/libtasn1-6_4.19.0-3ubuntu0.24.04.2.dsc' libtasn1-6_4.19.0-3ubuntu0.24.04.2.dsc 2801 SHA512:1f6d7b3a05b8f9b804d00fe726dbcd0ae0ed60d38483cecb45c8ddc6607a7cf11e1f7ea8e1001afc56b5c74be98893f063aa2dfd203df3f4c25fe211ca229692
'http://security.ubuntu.com/ubuntu/pool/main/libt/libtasn1-6/libtasn1-6_4.19.0.orig.tar.gz' libtasn1-6_4.19.0.orig.tar.gz 1786576 SHA512:287f5eddfb5e21762d9f14d11997e56b953b980b2b03a97ed4cd6d37909bda1ed7d2cdff9da5d270a21d863ab7e54be6b85c05f1075ac5d8f0198997cf335ef4
'http://security.ubuntu.com/ubuntu/pool/main/libt/libtasn1-6/libtasn1-6_4.19.0.orig.tar.gz.asc' libtasn1-6_4.19.0.orig.tar.gz.asc 228 SHA512:e0417625f8df22c6421914bf2d4f19d7f27260c24c04f50e59669681f326debe06ddef9dc5a2e20fda50feb30bbbf3f41597e64961257304ec2c407aa76d107e
'http://security.ubuntu.com/ubuntu/pool/main/libt/libtasn1-6/libtasn1-6_4.19.0-3ubuntu0.24.04.2.debian.tar.xz' libtasn1-6_4.19.0-3ubuntu0.24.04.2.debian.tar.xz 25112 SHA512:b64b55ad6138f12b1191039c1db36cba1b6add98bab5c399b338517284b4091ede2ce7a2e71f46f97c50584fb670bc2dd295caab108973aed0552353c1cb3158
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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libxcrypt=1:4.4.36-4build1`

Binary Packages:

- `libcrypt1:amd64=1:4.4.36-4build1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxcrypt=1:4.4.36-4build1
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxcrypt/libxcrypt_4.4.36-4build1.dsc' libxcrypt_4.4.36-4build1.dsc 2300 SHA512:5e9c4a5c26299ac291eb755a9a386ddaac65d6af2e6b9cc37c2803101e1d8b257a83eb36c12f2955873ee99a0a95f61ad2a204e5e5a2c88d33f043a426121c32
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxcrypt/libxcrypt_4.4.36.orig.tar.xz' libxcrypt_4.4.36.orig.tar.xz 392732 SHA512:82839d70fc068a4d4d5e14488ea7599e2430091ace53640d639628330eff52a058ac589b6b5a39bc6c83166e68cbf9b9e2024e0371df1f949336f633f2a1726e
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxcrypt/libxcrypt_4.4.36-4build1.debian.tar.xz' libxcrypt_4.4.36-4build1.debian.tar.xz 8356 SHA512:d181e5637d40e322cf03d80dff03acb9982c0a07a73229d660d8b2fcd02f31783347c0b0208d2ebb077bdf44e87330b04a8cd10a4bc272dbb0feca7f1adfe013
```

### `dpkg` source package: `libzstd=1.5.5+dfsg2-2build1.1`

Binary Packages:

- `libzstd1:amd64=1.5.5+dfsg2-2build1.1`

Licenses: (parsed from: `/usr/share/doc/libzstd1/copyright`)

- `BSD-3-clause`
- `Expat`
- `GPL-2`
- `zlib`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `lz4=1.9.4-1build1.1`

Binary Packages:

- `liblz4-1:amd64=1.9.4-1build1.1`

Licenses: (parsed from: `/usr/share/doc/liblz4-1/copyright`)

- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

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

Source:

```console
$ apt-get source -qq --print-uris mawk=1.3.4.20240123-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/m/mawk/mawk_1.3.4.20240123-1build1.dsc' mawk_1.3.4.20240123-1build1.dsc 2312 SHA512:ce2caf84e1323bee8329421cbda06d3cc6748c3e026a885996ca9cc1dad7b553f865f837821982e048c6456c09b6750d88da0412571011920f7f8a7239a45688
'http://archive.ubuntu.com/ubuntu/pool/main/m/mawk/mawk_1.3.4.20240123.orig.tar.gz' mawk_1.3.4.20240123.orig.tar.gz 413943 SHA512:f6d5da44280afeac4a9bb6d3788ed71ee816daaa5816f49b9d40add5292f3ae06e5af007a6c993d14405238cbb70ba4997fdd2fcd5901c9a1a4b61357045c4a6
'http://archive.ubuntu.com/ubuntu/pool/main/m/mawk/mawk_1.3.4.20240123.orig.tar.gz.asc' mawk_1.3.4.20240123.orig.tar.gz.asc 729 SHA512:3b4b8b8b7b74aff7061158a7c284d1949c09d52d78003b678c9dcc1da036a4d84b873103d76362866daf914d5a7d717c71baf13d30d7e882b03c5f87c8e4c452
'http://archive.ubuntu.com/ubuntu/pool/main/m/mawk/mawk_1.3.4.20240123-1build1.debian.tar.xz' mawk_1.3.4.20240123-1build1.debian.tar.xz 15704 SHA512:53a4367656e29f5897ba29cf38b30e2b3a2758d990bbd3a90bdbceb5d3c467615496407af8bd437b4df2e9518096865b7ec6739b0465e8bba20d87ed71782268
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

Source:

```console
$ apt-get source -qq --print-uris ncurses=6.4+20240113-1ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/n/ncurses/ncurses_6.4%2b20240113-1ubuntu2.dsc' ncurses_6.4+20240113-1ubuntu2.dsc 3963 SHA512:6a7865bb7f27ba20f443c43c00825aa8b4be3fd0dbd8da10571186c0a3ca074d82e30a08f854b6ec324a3663dae09d4d57c4e77617b08715a18b182a164a3c26
'http://archive.ubuntu.com/ubuntu/pool/main/n/ncurses/ncurses_6.4%2b20240113.orig.tar.gz' ncurses_6.4+20240113.orig.tar.gz 3688489 SHA512:45a4fbfa7d6fa51f7226b35698f2ca9b9f5bbbf3243cfee28886751244d238f698d5eaae1498ae9f7965b2d618a669ff827cfbba830e3a52a26bef825dec8ed9
'http://archive.ubuntu.com/ubuntu/pool/main/n/ncurses/ncurses_6.4%2b20240113.orig.tar.gz.asc' ncurses_6.4+20240113.orig.tar.gz.asc 729 SHA512:df94456e47857abfbb47f3a5a69f03b3d418a44542e1fa699c4b13eba812e5a85173cd651d77d07973f8f8d96bc301d7e413ad379f9ba1e9feb434c4da019f13
'http://archive.ubuntu.com/ubuntu/pool/main/n/ncurses/ncurses_6.4%2b20240113-1ubuntu2.debian.tar.xz' ncurses_6.4+20240113-1ubuntu2.debian.tar.xz 49372 SHA512:02fdd8f135b415d72ef4051b1002d0721a240f80b164d437592d5d6dfe44c4d3a0cd92baf5071047d826ca3b2039190ed19f3a092169d2a7af501c09e7ec45d0
```

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `npth=1.6-3.1build1`

Binary Packages:

- `libnpth0t64:amd64=1.6-3.1build1`

Licenses: (parsed from: `/usr/share/doc/libnpth0t64/copyright`)

- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris npth=1.6-3.1build1
'http://archive.ubuntu.com/ubuntu/pool/main/n/npth/npth_1.6-3.1build1.dsc' npth_1.6-3.1build1.dsc 2107 SHA512:83fc5c562da895742de6b46585a0707052e053804e3187525d290e0cc05938feb7681bb9a7dd053ed930a3774c7abc95a4d1a9e437930ca72c438e29cb7183d8
'http://archive.ubuntu.com/ubuntu/pool/main/n/npth/npth_1.6.orig.tar.bz2' npth_1.6.orig.tar.bz2 300486 SHA512:2ed1012e14a9d10665420b9a23628be7e206fd9348111ec751349b93557ee69f1176bcf7e6b195b35b1c44a5e0e81ee33b713f03d79a33d1ecd9037035afeda2
'http://archive.ubuntu.com/ubuntu/pool/main/n/npth/npth_1.6-3.1build1.debian.tar.xz' npth_1.6-3.1build1.debian.tar.xz 11036 SHA512:caf36d8727c335bbcf996421e65cf044d6468d95d70e9b671b57196341e49e67f687d6c80cab78d6c0388a90f795e4ed0ff28aaa0d4e7dd6f4701abdfc77a09a
```

### `dpkg` source package: `openldap=2.6.7+dfsg-1~exp1ubuntu8.2`

Binary Packages:

- `libldap2:amd64=2.6.7+dfsg-1~exp1ubuntu8.2`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `openssl=3.0.13-0ubuntu3.6`

Binary Packages:

- `libssl3t64:amd64=3.0.13-0ubuntu3.6`
- `openssl=3.0.13-0ubuntu3.6`

Licenses: (parsed from: `/usr/share/doc/libssl3t64/copyright`)

- `Apache-2.0`
- `Artistic`
- `GPL-1`
- `GPL-1+`

Source:

```console
$ apt-get source -qq --print-uris openssl=3.0.13-0ubuntu3.6
'http://security.ubuntu.com/ubuntu/pool/main/o/openssl/openssl_3.0.13-0ubuntu3.6.dsc' openssl_3.0.13-0ubuntu3.6.dsc 2512 SHA512:e57effde33e3e978184e1c2d5167d8f8c1c881aae59f81dfbedeca0004488434c3dff227bec9ca6e3f701c01a9c5a7a3c8ffb3fef3533d9dee0f46b64d03e535
'http://security.ubuntu.com/ubuntu/pool/main/o/openssl/openssl_3.0.13.orig.tar.gz' openssl_3.0.13.orig.tar.gz 15294843 SHA512:22f4096781f0b075f5bf81bd39a0f97e111760dfa73b6f858f6bb54968a7847944d74969ae10f9a51cc21a2f4af20d9a4c463649dc824f5e439e196d6764c4f9
'http://security.ubuntu.com/ubuntu/pool/main/o/openssl/openssl_3.0.13-0ubuntu3.6.debian.tar.xz' openssl_3.0.13-0ubuntu3.6.debian.tar.xz 169500 SHA512:bc33f7a4d5c577cc622062b2337a2b897bc06dd6592f6e636832529ff8ebde4f5fcb5d35589d041ec498386d7ec63df2b76f37aaab0b0cddf35a4d53c8a5cc3f
```

### `dpkg` source package: `p11-kit=0.25.3-4ubuntu2.1`

Binary Packages:

- `libp11-kit0:amd64=0.25.3-4ubuntu2.1`
- `p11-kit=0.25.3-4ubuntu2.1`
- `p11-kit-modules:amd64=0.25.3-4ubuntu2.1`

Licenses: (parsed from: `/usr/share/doc/libp11-kit0/copyright`, `/usr/share/doc/p11-kit/copyright`, `/usr/share/doc/p11-kit-modules/copyright`)

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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
'http://security.ubuntu.com/ubuntu/pool/main/p/pam/pam_1.5.3-5ubuntu5.5.dsc' pam_1.5.3-5ubuntu5.5.dsc 2727 SHA512:59b875e301869358617068f0e2ebcc884ae8c2fad24c487b15d347ee4b826df9a008aa74fa14aa99fc1300ab9fd07dbef6f025e50a005937a093df692f9befc0
'http://security.ubuntu.com/ubuntu/pool/main/p/pam/pam_1.5.3.orig.tar.xz' pam_1.5.3.orig.tar.xz 1020076 SHA512:af88e8c1b6a9b737ffaffff7dd9ed8eec996d1fbb5804fb76f590bed66d8a1c2c6024a534d7a7b6d18496b300f3d6571a08874cf406cd2e8cea1d5eff49c136a
'http://security.ubuntu.com/ubuntu/pool/main/p/pam/pam_1.5.3-5ubuntu5.5.debian.tar.xz' pam_1.5.3-5ubuntu5.5.debian.tar.xz 204688 SHA512:9c4e286ce3ea8bce267b7571f518e434a704d8c9a46c5de8cee1d0bf4b5303474a5549e5b188ba8b306b282a1797ab3418d299195557da8e275c5f005776f10d
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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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
'http://security.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.38.2-3.2ubuntu0.2.dsc' perl_5.38.2-3.2ubuntu0.2.dsc 3036 SHA512:bdd956f4f04ef15d13659bac27cce96c4d98caaacc586525302c9e14c865e7c9ae81b7369caf636fd73074edcbc56a6e204e3c2ab0c8f2db52f8fece9f0d4b6c
'http://security.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.38.2.orig-regen-configure.tar.xz' perl_5.38.2.orig-regen-configure.tar.xz 418808 SHA512:c4ea40ce9eda247c2ced678a75bdbd8bc292baee5ec3490cb00b1947277e1e0e9e5160d108676380efff13d4f1304f0c8d4eaa2c7e66e543ecd57e513075cb8c
'http://security.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.38.2.orig.tar.xz' perl_5.38.2.orig.tar.xz 13679524 SHA512:0ca51e447c7a18639627c281a1c7ae6662c773745ea3c86bede46336d5514ecc97ded2c61166e1ac15635581489dc596368907aa3a775b34db225b76d7402d10
'http://security.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.38.2-3.2ubuntu0.2.debian.tar.xz' perl_5.38.2-3.2ubuntu0.2.debian.tar.xz 171736 SHA512:9511993218de5c72dabb87e2ba13a00b034fbb96637b3791515cbac26fa9820067d95d48f165766cce1086304936c1de6150140023915437a91050f27aced32e
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

Source:

```console
$ apt-get source -qq --print-uris pinentry=1.2.1-3ubuntu5
'http://archive.ubuntu.com/ubuntu/pool/main/p/pinentry/pinentry_1.2.1-3ubuntu5.dsc' pinentry_1.2.1-3ubuntu5.dsc 3322 SHA512:86814cb072f65755573416f567476616d001aefa000362e84b751c85ed42b02297391fc67d7dfabcfd70d7e953e0b9d95b63d98222f8ea79aec527da37fc0c15
'http://archive.ubuntu.com/ubuntu/pool/main/p/pinentry/pinentry_1.2.1.orig.tar.bz2' pinentry_1.2.1.orig.tar.bz2 547698 SHA512:a665315628f4dcf07e16a22db3f3be15d7e7e93b3deec0546c7275b71b0e3bd65535a08af5e12d6339fd6595132df86529401d9d12bd17c428a3466e8dfafab6
'http://archive.ubuntu.com/ubuntu/pool/main/p/pinentry/pinentry_1.2.1.orig.tar.bz2.asc' pinentry_1.2.1.orig.tar.bz2.asc 390 SHA512:60b63b7fe2d6793840be55635f9a704cd42eda69ccaea2453d47b5f7a5198d313b8f23555972584f7f087fd5d0fc2a379bfc5f7512f325b018cc5c3e2e54a47e
'http://archive.ubuntu.com/ubuntu/pool/main/p/pinentry/pinentry_1.2.1-3ubuntu5.debian.tar.xz' pinentry_1.2.1-3ubuntu5.debian.tar.xz 19244 SHA512:7d4a8fe8920f1d6ef656ab485e2625bc646c5726ba18f91eedb3f4c95241680f2169b80791355e34a707bbebdb0de9986e264f2d8f36848e48a8300fc8497481
```

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

Source:

```console
$ apt-get source -qq --print-uris readline=8.2-4build1
'http://archive.ubuntu.com/ubuntu/pool/main/r/readline/readline_8.2-4build1.dsc' readline_8.2-4build1.dsc 2926 SHA512:8ad7e70792466e093ff1202b123e24c6fa1a9850e57ca0b775b06bfe4e502ef8ffc876eda32fb164565cda1e4e048f3f80e6ff69ae9c56f87841f15c759a7658
'http://archive.ubuntu.com/ubuntu/pool/main/r/readline/readline_8.2.orig.tar.gz' readline_8.2.orig.tar.gz 3043952 SHA512:0a451d459146bfdeecc9cdd94bda6a6416d3e93abd80885a40b334312f16eb890f8618a27ca26868cebbddf1224983e631b1cbc002c1a4d1cd0d65fba9fea49a
'http://archive.ubuntu.com/ubuntu/pool/main/r/readline/readline_8.2-4build1.debian.tar.xz' readline_8.2-4build1.debian.tar.xz 33816 SHA512:b8c92282e25f3d28acd02c1431088f5f29aa1398ce919c312de50813e8a0df07d973ffd49fccde51505538ed7e29f666d812931961746b12ebde219d16be914f
```

### `dpkg` source package: `rtmpdump=2.4+20151223.gitfa8646d.1-2build7`

Binary Packages:

- `librtmp1:amd64=2.4+20151223.gitfa8646d.1-2build7`

Licenses: (parsed from: `/usr/share/doc/librtmp1/copyright`)

- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris rtmpdump=2.4+20151223.gitfa8646d.1-2build7
'http://archive.ubuntu.com/ubuntu/pool/main/r/rtmpdump/rtmpdump_2.4%2b20151223.gitfa8646d.1-2build7.dsc' rtmpdump_2.4+20151223.gitfa8646d.1-2build7.dsc 2439 SHA512:5e2fb3986c0f0e2150c6054e0428adbf1719bb0c33f92ae4acb74a11e625d731ede0262f0d8887c769a95a61f3cd4d23d44bf2f375f0153eba6c0f25b68719c5
'http://archive.ubuntu.com/ubuntu/pool/main/r/rtmpdump/rtmpdump_2.4%2b20151223.gitfa8646d.1.orig.tar.gz' rtmpdump_2.4+20151223.gitfa8646d.1.orig.tar.gz 142213 SHA512:bdfcbab73179d614a295a7b136ea4c9d0ce4620883b493f298362784d245608cd6ad4b0ad30f94ed73a086b4555399521ae9e95b6375fce75e455ae68c055e7b
'http://archive.ubuntu.com/ubuntu/pool/main/r/rtmpdump/rtmpdump_2.4%2b20151223.gitfa8646d.1-2build7.debian.tar.xz' rtmpdump_2.4+20151223.gitfa8646d.1-2build7.debian.tar.xz 8464 SHA512:812edf4f933ad0f723404192bfbfceca86e58303169a30e3b1f47781b709b91a259621293533d31d7abd16bc522824e2db325426a4ce9a6b428b88d492ae4c6c
```

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

Source:

```console
$ apt-get source -qq --print-uris sed=4.9-2build1
'http://archive.ubuntu.com/ubuntu/pool/main/s/sed/sed_4.9-2build1.dsc' sed_4.9-2build1.dsc 1992 SHA512:c1fb23ca19645e3c77d7d466818b0ff15ec2fefa423d03c60746d3c441a767af9a551c0af022a5c17e69e58589b8004bc6e127dbb63d806c6269ba0ee2c1e8fd
'http://archive.ubuntu.com/ubuntu/pool/main/s/sed/sed_4.9.orig.tar.xz' sed_4.9.orig.tar.xz 1397092 SHA512:36157a4b4a2430cf421b7bd07f1675d680d9f1616be96cf6ad6ee74a9ec0fe695f8d0b1e1f0b008bbb33cc7fcde5e1c456359bbbc63f8aebdd4fedc3982cf6dc
'http://archive.ubuntu.com/ubuntu/pool/main/s/sed/sed_4.9-2build1.debian.tar.xz' sed_4.9-2build1.debian.tar.xz 62896 SHA512:e9e57380873aa800f7892d99dbebb362a2ba9f27cc984180753d306592d6ca572d0baa3c4faf4b10dbc2aa33985e759f668f1efb4e0b09e4ae2ae689e32969ad
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
'http://archive.ubuntu.com/ubuntu/pool/main/s/sensible-utils/sensible-utils_0.0.22.dsc' sensible-utils_0.0.22.dsc 1737 SHA512:be6eb8a63de0912e56d7039e616fa1ef362f1081e2edb893f3cfa8ccc3c5d2ed65ad2f477d6013b6a5ecf0f4b98a39de45ee073cdeeb3802f3eb51c754fda40d
'http://archive.ubuntu.com/ubuntu/pool/main/s/sensible-utils/sensible-utils_0.0.22.tar.xz' sensible-utils_0.0.22.tar.xz 74412 SHA512:c35ac6f9a27bf21bd496acb5ada2fd2e5eb101d661fe49a505a80dc507eea314b8b29388ae4852c14aff547fef8938f48a14898c49cf951d7ab13ccf48e77ed5
```

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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
'http://security.ubuntu.com/ubuntu/pool/main/s/sqlite3/sqlite3_3.45.1-1ubuntu2.5.dsc' sqlite3_3.45.1-1ubuntu2.5.dsc 2601 SHA512:fb56794498668ca451db41d705708b505877abaa88f4bd36b47d7642f3f9513fb3597c77517e05dd821c90a341de8c032c3f7f39ebdc40a33b99a1802f51907a
'http://security.ubuntu.com/ubuntu/pool/main/s/sqlite3/sqlite3_3.45.1.orig-www.tar.xz' sqlite3_3.45.1.orig-www.tar.xz 5693812 SHA512:dbbf32bad3912dca4d1d3366053c66dc53745d4e5c6892c10470b7452f338de03eee1406cb6c5a972c9890bd71a7b30563e4863f27bf0f2813a92ffdfd95832f
'http://security.ubuntu.com/ubuntu/pool/main/s/sqlite3/sqlite3_3.45.1.orig.tar.xz' sqlite3_3.45.1.orig.tar.xz 8257884 SHA512:8ea4a50fe730b072271978bbeee074d567bc8cbaa3bb4a8b8802e012d470fd482d800532eedea48a54fd64785f3b02aab7b033c8e2767a5e8b9f02a9cc844b80
'http://security.ubuntu.com/ubuntu/pool/main/s/sqlite3/sqlite3_3.45.1-1ubuntu2.5.debian.tar.xz' sqlite3_3.45.1-1ubuntu2.5.debian.tar.xz 35260 SHA512:a031e8f6aeefbb9ea45439a24dc82f9e74b12c3e92b6444057648cc07187c00a0ca6cf32a6c51c0e50787f41d525c687cc3dad7492b46d785fa1088b04d10ea1
```

### `dpkg` source package: `systemd=255.4-1ubuntu8.12`

Binary Packages:

- `libsystemd0:amd64=255.4-1ubuntu8.12`
- `libudev1:amd64=255.4-1ubuntu8.12`

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

Source:

```console
$ apt-get source -qq --print-uris sysvinit=3.08-6ubuntu3
'http://archive.ubuntu.com/ubuntu/pool/main/s/sysvinit/sysvinit_3.08-6ubuntu3.dsc' sysvinit_3.08-6ubuntu3.dsc 2495 SHA512:8200c0fa7220e8922a8546f4f1a4beb3a7194b23abd8730c82ea0cfa57bc6fba01e0b7883a0a9b5b1f10c7b7be805689db80df2930c6d345754a3b85a4ddac02
'http://archive.ubuntu.com/ubuntu/pool/main/s/sysvinit/sysvinit_3.08.orig.tar.gz' sysvinit_3.08.orig.tar.gz 513674 SHA512:63ed7ebd50944adce1a35af7798d0e2d6248f36a606f63bb7a567424555ec33e83c33b897528c801b4b4ac61b24d2a3555c9a690031c50a94e7ead83f37f8e96
'http://archive.ubuntu.com/ubuntu/pool/main/s/sysvinit/sysvinit_3.08-6ubuntu3.debian.tar.xz' sysvinit_3.08-6ubuntu3.debian.tar.xz 140128 SHA512:fa53bd172bf4ce998743f3011b44ebf188948ed436f202181fc6eb7d4535e4d1426aeeac76cda4a650b040d22f9487b890e9f826cd222ddc5e939901c5f7c67c
```

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

Source:

```console
$ apt-get source -qq --print-uris tar=1.35+dfsg-3build1
'http://archive.ubuntu.com/ubuntu/pool/main/t/tar/tar_1.35%2bdfsg-3build1.dsc' tar_1.35+dfsg-3build1.dsc 2141 SHA512:bb080610adc480448cf511d591eaaeb301395e5bbe01b16b254ad33edb33233aba18af79a4cf505fec330c83dac9570d84122432ff11b781a12c5dc409a173f6
'http://archive.ubuntu.com/ubuntu/pool/main/t/tar/tar_1.35%2bdfsg.orig.tar.xz' tar_1.35+dfsg.orig.tar.xz 2111608 SHA512:3aea32b5c8de229131308420d8a7aa57f7fd1b376980456dd1aa66f97509572750c3833ab9cc2edc6fdea51f802033598c83a0d6e7f18680b1638996f0acaae7
'http://archive.ubuntu.com/ubuntu/pool/main/t/tar/tar_1.35%2bdfsg-3build1.debian.tar.xz' tar_1.35+dfsg-3build1.debian.tar.xz 20948 SHA512:82b1a9f70c99c17f5288a4a9fbe8b1bef0adcd9543f97f876ee81afc16e3ac02e46182557406ff434ae90c81950f22346c3229ee3e5f5f9578dcf09a20053e9f
```

### `dpkg` source package: `tzdata=2025b-0ubuntu0.24.04.1`

Binary Packages:

- `tzdata=2025b-0ubuntu0.24.04.1`

Licenses: (parsed from: `/usr/share/doc/tzdata/copyright`)

- `ICU`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris tzdata=2025b-0ubuntu0.24.04.1
'http://security.ubuntu.com/ubuntu/pool/main/t/tzdata/tzdata_2025b-0ubuntu0.24.04.1.dsc' tzdata_2025b-0ubuntu0.24.04.1.dsc 2728 SHA512:e717b51a15bbdd64183841b5136194f75bc2affece27101e3d03ed5b4614959a7810d7e1cfc8e59d846fe87dec7ed01c1cc739a25a0abf95552215f0929ea318
'http://security.ubuntu.com/ubuntu/pool/main/t/tzdata/tzdata_2025b.orig.tar.gz' tzdata_2025b.orig.tar.gz 464295 SHA512:7d83741f3cae81fac8131994b43c55b6da7328df18b706e5ee40e9b3212bc506e6f8fc90988b18da424ed59eff69bce593f2783b7b5f18eb483a17aeb94258d6
'http://security.ubuntu.com/ubuntu/pool/main/t/tzdata/tzdata_2025b.orig.tar.gz.asc' tzdata_2025b.orig.tar.gz.asc 833 SHA512:ad39fe16b32fad7eee27ff968b4e8af23267ce586629ad70e7625136d2c3cc3a42295a87b3dc770c291aa9112c56301629c1fe379735f70008e62864ce4e735a
'http://security.ubuntu.com/ubuntu/pool/main/t/tzdata/tzdata_2025b-0ubuntu0.24.04.1.debian.tar.xz' tzdata_2025b-0ubuntu0.24.04.1.debian.tar.xz 188052 SHA512:8120a6b7f4381ce8f5e67b58f0cdc144905c8eed387c5b3ea820c19464308b0b2c9010ad498fe69e5161f4c23ccba78ee7f6d9dc7ac0caa23b18509ea4d8dad4
```

### `dpkg` source package: `ubuntu-keyring=2023.11.28.1`

Binary Packages:

- `ubuntu-keyring=2023.11.28.1`

Licenses: (parsed from: `/usr/share/doc/ubuntu-keyring/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris ubuntu-keyring=2023.11.28.1
'http://archive.ubuntu.com/ubuntu/pool/main/u/ubuntu-keyring/ubuntu-keyring_2023.11.28.1.dsc' ubuntu-keyring_2023.11.28.1.dsc 1872 SHA512:4d3c094e1e01367eb8303808ea5bfea696ee672d855a64272c9222400bec397ebbaa57783bbc8eb4365f0631c9951edeb1b12f04efb3e34275408ef57620f023
'http://archive.ubuntu.com/ubuntu/pool/main/u/ubuntu-keyring/ubuntu-keyring_2023.11.28.1.tar.xz' ubuntu-keyring_2023.11.28.1.tar.xz 20236 SHA512:b17824a91d6e25c5658eae8d9ae509a4158b406768d5d4a8e117a230226ab7cd4327cf7e5b9bbb7baae7c66f3807d27926de85a1ea5c11a82684a890aeb8fd18
```

### `dpkg` source package: `unminimize=0.2.1`

Binary Packages:

- `unminimize=0.2.1`

Licenses: (parsed from: `/usr/share/doc/unminimize/copyright`)

- `GPL-2`
- `GPL-2.0+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `util-linux=2.39.3-9ubuntu6.4`

Binary Packages:

- `bsdutils=1:2.39.3-9ubuntu6.4`
- `libblkid1:amd64=2.39.3-9ubuntu6.4`
- `libmount1:amd64=2.39.3-9ubuntu6.4`
- `libsmartcols1:amd64=2.39.3-9ubuntu6.4`
- `libuuid1:amd64=2.39.3-9ubuntu6.4`
- `mount=2.39.3-9ubuntu6.4`
- `util-linux=2.39.3-9ubuntu6.4`

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


### `dpkg` source package: `wget=1.21.4-1ubuntu4.1`

Binary Packages:

- `wget=1.21.4-1ubuntu4.1`

Licenses: (parsed from: `/usr/share/doc/wget/copyright`)

- `GFDL-1.2`
- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris wget=1.21.4-1ubuntu4.1
'http://security.ubuntu.com/ubuntu/pool/main/w/wget/wget_1.21.4-1ubuntu4.1.dsc' wget_1.21.4-1ubuntu4.1.dsc 2251 SHA512:d7b0fab6350ba51e5783ff8e931fd20894c8334c9f78f9f1c970a755d93e54ae501bdc5f5050d536a99472b536acb141ae67a4cbd43f014acbcaf2828ab3e6fb
'http://security.ubuntu.com/ubuntu/pool/main/w/wget/wget_1.21.4.orig.tar.gz' wget_1.21.4.orig.tar.gz 5059591 SHA512:7a1539045174f6b97ab6980811c2ac1799edc20db72987b5ba9b1710cffb19669a7736813d15c8da3aa2d4a384246ff946b77ecb0baeb6fd3e12ae591f1bf6a3
'http://security.ubuntu.com/ubuntu/pool/main/w/wget/wget_1.21.4.orig.tar.gz.asc' wget_1.21.4.orig.tar.gz.asc 854 SHA512:72603493c2d799dca08700175a2010d8736fd6d3cb9bea3987db8814e9f133ab0fbd1477892115f7fbbd1a7d4d416ec370bdbff6dbe8f00d1eea84f0c4f8d84b
'http://security.ubuntu.com/ubuntu/pool/main/w/wget/wget_1.21.4-1ubuntu4.1.debian.tar.xz' wget_1.21.4-1ubuntu4.1.debian.tar.xz 65000 SHA512:7f8d94188f21aeddf4a2b845839994f1ec90a1727891ad5496bdc3841600abed8d58b3c111a2ef33329d85b57dcd8364b4ab174acf93cfd5a0c3eb8487c917da
```

### `dpkg` source package: `xxhash=0.8.2-2build1`

Binary Packages:

- `libxxhash0:amd64=0.8.2-2build1`

Licenses: (parsed from: `/usr/share/doc/libxxhash0/copyright`)

- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris xxhash=0.8.2-2build1
'http://archive.ubuntu.com/ubuntu/pool/main/x/xxhash/xxhash_0.8.2-2build1.dsc' xxhash_0.8.2-2build1.dsc 2076 SHA512:9a1bc162cefe90fd63c2f1225ba28eda45a3972e2bf45fc851bc3c7adcf70e5be65a294aedebc47aedc05516f0c0d9fca065d64196d237497c44840dbf5305e9
'http://archive.ubuntu.com/ubuntu/pool/main/x/xxhash/xxhash_0.8.2.orig.tar.gz' xxhash_0.8.2.orig.tar.gz 1141188 SHA512:3e3eef21432fe88bc4dd9940ccad0308fdea3537b06fa5ac0e74c1bde53413dff29c8b3fc617a8a42b9ce88fcf213311d338a31b1ce73b3729342c9e68f06c78
'http://archive.ubuntu.com/ubuntu/pool/main/x/xxhash/xxhash_0.8.2-2build1.debian.tar.xz' xxhash_0.8.2-2build1.debian.tar.xz 5048 SHA512:c789fd0a22fd40db8983c0f69054141647ebaab94251598723ce1fdf894d0ed2d48c2d5a7f0df7d61e2d874485286e5742a546748d17cc22d5227ad61f6b4ef2
```

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
'http://security.ubuntu.com/ubuntu/pool/main/x/xz-utils/xz-utils_5.6.1%2breally5.4.5-1ubuntu0.2.dsc' xz-utils_5.6.1+really5.4.5-1ubuntu0.2.dsc 2639 SHA512:b10ba1ba72e3f1ea6c12b5d1f84bf21b2651e5e796d35b821c14370ecb65953a02e32e3d5f21587191e5b62757b34ae0af2ba64b399670b4c4fd46e04b9b7811
'http://security.ubuntu.com/ubuntu/pool/main/x/xz-utils/xz-utils_5.6.1%2breally5.4.5.orig.tar.xz' xz-utils_5.6.1+really5.4.5.orig.tar.xz 1680520 SHA512:5cbc3b5bb35a9f5773ad657788fe77013471e3b621c5a8149deb7389d48535926e5bed103456fcfe5ecb044b236b1055b03938a6cc877cfc749372b899fc79e5
'http://security.ubuntu.com/ubuntu/pool/main/x/xz-utils/xz-utils_5.6.1%2breally5.4.5-1ubuntu0.2.debian.tar.xz' xz-utils_5.6.1+really5.4.5-1ubuntu0.2.debian.tar.xz 30776 SHA512:1891c935b3915749aaa4f29b494c3d3156dd7a04b4637148d6a668ab5fb464a0bd2be441108750e5601244921f38e47c2d25490cf07d0066da566e5d36756582
```

### `dpkg` source package: `zlib=1:1.3.dfsg-3.1ubuntu2.1`

Binary Packages:

- `zlib1g:amd64=1:1.3.dfsg-3.1ubuntu2.1`

Licenses: (parsed from: `/usr/share/doc/zlib1g/copyright`)

- `Zlib`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

