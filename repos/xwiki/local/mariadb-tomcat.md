# `xwiki:18-mariadb-tomcat`

## Docker Metadata

- Image ID: `sha256:ab3ce623320b28fd5696e7efcbe3d02b0b87673c391c81cc147a9570d8e01451`
- Created: `2026-04-15T23:17:37.603399001Z`
- Virtual Size: ~ 1.32 Gb  
  (total size of all layers on-disk)
- Arch: `linux`/`amd64`
- Entrypoint: `["docker-entrypoint.sh"]`
- Command: `["xwiki"]`
- Environment:
  - `PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin`
  - `JAVA_HOME=/opt/java/openjdk`
  - `LANG=en_US.UTF-8`
  - `LANGUAGE=en_US:en`
  - `LC_ALL=en_US.UTF-8`
  - `JAVA_VERSION=jdk-21.0.10+7`
  - `CATALINA_HOME=/usr/local/tomcat`
  - `TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib`
  - `LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib`
  - `TOMCAT_MAJOR=10`
  - `TOMCAT_VERSION=10.1.54`
  - `TOMCAT_SHA512=8694b94324cf6f62ab032fa2438d7334518dcfcbf7878361b147246c46eb1e558c327f32c05fb4b7705c01fcca92fde392ce320934410f1169ff4ab36a1c7139`
  - `XWIKI_VERSION=18.2.1`
  - `XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/18.2.1`
  - `XWIKI_DOWNLOAD_SHA256=d18d8d16f39d6a37ba11c0015dbafced57183a9bdbdf35ed1103191e24dac7b2`
  - `MARIADB_JDBC_VERSION=3.5.7`
  - `MARIADB_JDBC_SHA256=07bb1229dc184f3313a5aef4c5a6b3207c8dbaa09db4a26814c936f004b4c526`
  - `MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.5.7`
  - `MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.5.7.jar`
  - `MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.5.7.jar`
- Labels:
  - `org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>`
  - `org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki`
  - `org.opencontainers.image.licenses=LGPL-2.1`
  - `org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git`
  - `org.opencontainers.image.url=https://hub.docker.com/_/xwiki`
  - `org.opencontainers.image.vendor=xwiki.org`
  - `org.opencontainers.image.version=24.04`

## `dpkg` (`.deb`-based packages)

### `dpkg` source package: `abseil=20220623.1-3.1ubuntu3.2`

Binary Packages:

- `libabsl20220623t64:amd64=20220623.1-3.1ubuntu3.2`

Licenses: (parsed from: `/usr/share/doc/libabsl20220623t64/copyright`)

- `Apache-2.0`

Source:

```console
$ apt-get source -qq --print-uris abseil=20220623.1-3.1ubuntu3.2
'http://security.ubuntu.com/ubuntu/pool/main/a/abseil/abseil_20220623.1-3.1ubuntu3.2.dsc' abseil_20220623.1-3.1ubuntu3.2.dsc 2683 SHA512:413059bae795a8924c2db9ac33ecf3270bb3247b34a148a23cd1c058719d5e7e286c99bce428cc14beede0d3e2d75fc4a7e4a424a36ddd8faaacc357eca40590
'http://security.ubuntu.com/ubuntu/pool/main/a/abseil/abseil_20220623.1.orig.tar.gz' abseil_20220623.1.orig.tar.gz 1957272 SHA512:3c7fca91a9bda39a43cbdbd855577f58a988a7dc214ac93ef7e4cb2cc6ec24149bd7a414b4f7caf35511eaaa296260051a3d02b69ee5fd6e3247100b0b12258e
'http://security.ubuntu.com/ubuntu/pool/main/a/abseil/abseil_20220623.1-3.1ubuntu3.2.debian.tar.xz' abseil_20220623.1-3.1ubuntu3.2.debian.tar.xz 10380 SHA512:6f8ca36063ee10af159f97ad552f3c61977487c06e26fc16daa0af3542e3777db4a75e60eca7878782b835b521c6f1df6ff14facc5d35549e28eebb2f0120678
```

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `apr=1.7.2-3.1ubuntu0.1`

Binary Packages:

- `libapr1t64:amd64=1.7.2-3.1ubuntu0.1`

Licenses: (parsed from: `/usr/share/doc/libapr1t64/copyright`)

- `Apache-2.0`

Source:

```console
$ apt-get source -qq --print-uris apr=1.7.2-3.1ubuntu0.1
'http://security.ubuntu.com/ubuntu/pool/main/a/apr/apr_1.7.2-3.1ubuntu0.1.dsc' apr_1.7.2-3.1ubuntu0.1.dsc 1808 SHA512:429a77d6c512856fad8593d2484f60f25877003b46696467a721a99bc3308335619e41412446a4c147aa4f8cd039df4084cca6261bf63ec0b9e21cb22242d318
'http://security.ubuntu.com/ubuntu/pool/main/a/apr/apr_1.7.2.orig.tar.bz2' apr_1.7.2.orig.tar.bz2 890218 SHA512:0a3a27ccc97bbe4865c1bc0b803012e3da6d5b1f17d4fb0da6f5f58eec01f6d2ae1f25e52896ea5f9c5ac04c5fddcfd1ac606b301c322cf40d5c4d4ce0a1b76e
'http://security.ubuntu.com/ubuntu/pool/main/a/apr/apr_1.7.2.orig.tar.bz2.asc' apr_1.7.2.orig.tar.bz2.asc 833 SHA512:77da1e516b30032419b36da8453f56c6149ad18631772613adb095b6eccb7606dc51589d33d422572d3fcefe8f6129bfbb06d0ab7fde5848d873856f4ed93940
'http://security.ubuntu.com/ubuntu/pool/main/a/apr/apr_1.7.2-3.1ubuntu0.1.debian.tar.xz' apr_1.7.2-3.1ubuntu0.1.debian.tar.xz 55364 SHA512:3d5aa043c300f8e505f1ac00d543710b3945638587cd39dad94519f61305270276866549523c0df4d1c962c2dde0a07e01a0da93f5a9399e7a194a25618ef63a
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


### `dpkg` source package: `argon2=0~20190702+dfsg-4build1`

Binary Packages:

- `libargon2-1:amd64=0~20190702+dfsg-4build1`

Licenses: (parsed from: `/usr/share/doc/libargon2-1/copyright`)

- `Apache-2.0`
- `CC0`

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


### `dpkg` source package: `avahi=0.8-13ubuntu6.1`

Binary Packages:

- `libavahi-client3:amd64=0.8-13ubuntu6.1`
- `libavahi-common-data:amd64=0.8-13ubuntu6.1`
- `libavahi-common3:amd64=0.8-13ubuntu6.1`

Licenses: (parsed from: `/usr/share/doc/libavahi-client3/copyright`, `/usr/share/doc/libavahi-common-data/copyright`, `/usr/share/doc/libavahi-common3/copyright`)

- `GPL`
- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris avahi=0.8-13ubuntu6.1
'http://security.ubuntu.com/ubuntu/pool/main/a/avahi/avahi_0.8-13ubuntu6.1.dsc' avahi_0.8-13ubuntu6.1.dsc 4203 SHA512:93a8193e20570493396539e91807d532ec5d4edff78e4bde9a7ccf4ca87f0d8de8cae0c4ed357406a541c2fc4c3843ca5c6943440095fcb48e7f68f3e7fe55d3
'http://security.ubuntu.com/ubuntu/pool/main/a/avahi/avahi_0.8.orig.tar.gz' avahi_0.8.orig.tar.gz 1591458 SHA512:c6ba76feb6e92f70289f94b3bf12e5f5c66c11628ce0aeb3cadfb72c13a5d1a9bd56d71bdf3072627a76cd103b9b056d9131aa49ffe11fa334c24ab3b596c7de
'http://security.ubuntu.com/ubuntu/pool/main/a/avahi/avahi_0.8-13ubuntu6.1.debian.tar.xz' avahi_0.8-13ubuntu6.1.debian.tar.xz 50612 SHA512:8b33bfca10efe03a526804a1616e622361f05d84748b6f998f354f748a12cf69377bf64ecc5a4f619e503f57df92bf214b385bc701af4ee95d2778592b1cac01
```

### `dpkg` source package: `base-files=13ubuntu10.4`

Binary Packages:

- `base-files=13ubuntu10.4`

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


### `dpkg` source package: `boost1.83=1.83.0-2.1ubuntu3.2`

Binary Packages:

- `libboost-iostreams1.83.0:amd64=1.83.0-2.1ubuntu3.2`
- `libboost-locale1.83.0:amd64=1.83.0-2.1ubuntu3.2`
- `libboost-thread1.83.0:amd64=1.83.0-2.1ubuntu3.2`

Licenses: (parsed from: `/usr/share/doc/libboost-iostreams1.83.0/copyright`, `/usr/share/doc/libboost-locale1.83.0/copyright`, `/usr/share/doc/libboost-thread1.83.0/copyright`)

- `Apache-2.0`
- `BSD2`
- `BSD3_DEShaw`
- `BSD3_Google`
- `BSL-1.0`
- `Caramel`
- `CrystalClear`
- `HP`
- `Jam`
- `Kempf`
- `MIT`
- `NIST`
- `OldBoost1`
- `OldBoost2`
- `OldBoost3`
- `Python`
- `SGI`
- `Spencer`
- `Zlib`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `brotli=1.1.0-2build2`

Binary Packages:

- `libbrotli1:amd64=1.1.0-2build2`

Licenses: (parsed from: `/usr/share/doc/libbrotli1/copyright`)

- `MIT`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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


### `dpkg` source package: `clucene-core=2.3.3.4+dfsg-1.2ubuntu2`

Binary Packages:

- `libclucene-contribs1t64:amd64=2.3.3.4+dfsg-1.2ubuntu2`
- `libclucene-core1t64:amd64=2.3.3.4+dfsg-1.2ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libclucene-contribs1t64/copyright`, `/usr/share/doc/libclucene-core1t64/copyright`)

- `Apache-2.0`
- `LGPL-2.1`
- `Reuters-21578 - Distribution 1.0`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `cups=2.4.7-1.2ubuntu7.9`

Binary Packages:

- `libcups2t64:amd64=2.4.7-1.2ubuntu7.9`

Licenses: (parsed from: `/usr/share/doc/libcups2t64/copyright`)

- `Apache-2.0`
- `Apache-2.0-with-GPL2-LGPL2-Exception`
- `BSD-2-Clause`
- `BSD-2-clause`
- `FSFUL`
- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris cups=2.4.7-1.2ubuntu7.9
'http://security.ubuntu.com/ubuntu/pool/main/c/cups/cups_2.4.7-1.2ubuntu7.9.dsc' cups_2.4.7-1.2ubuntu7.9.dsc 3188 SHA512:49aadaf466874815257b71ca96c1233c1c40397d7962620727dce95b452a8340f9ec3c44bed6855847090123dcbe932e7ee4fa3a9f617a9e047c940e7d99872d
'http://security.ubuntu.com/ubuntu/pool/main/c/cups/cups_2.4.7.orig.tar.gz' cups_2.4.7.orig.tar.gz 8134809 SHA512:914b574ff6d85de9f3471528b52d4a436c484c441f47651846e1bdfa00aec26774efd416ff466216d2bccf468f8a797b1e0d666b5c82abc87e77550ce8b00d39
'http://security.ubuntu.com/ubuntu/pool/main/c/cups/cups_2.4.7-1.2ubuntu7.9.debian.tar.xz' cups_2.4.7-1.2ubuntu7.9.debian.tar.xz 418144 SHA512:cbb3dbc2d630b20f6aef4deafa907b9737ee970df8724b7af2684574fcd01c62affd8df1c95857bc6c04577c8be9a67f692e8c6bcf3f2480df06cf205ce070e3
```

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

Source:

```console
$ apt-get source -qq --print-uris curl=8.5.0-2ubuntu10.8
'http://security.ubuntu.com/ubuntu/pool/main/c/curl/curl_8.5.0-2ubuntu10.8.dsc' curl_8.5.0-2ubuntu10.8.dsc 3051 SHA512:cdff7efe8d9e9693e138fbe1ac018e0f0ace38d4fcd68f1829fb7eb2f506b592e048b56109a89a54a0032fc7faa9b77a1655af7f956eca1152b9dfa811ed943f
'http://security.ubuntu.com/ubuntu/pool/main/c/curl/curl_8.5.0.orig.tar.gz' curl_8.5.0.orig.tar.gz 4372979 SHA512:1ff70e8fd5f233b373dea2a031d46698c03ed35f384c2eacbe9368f9daed65e91d7f45ade350c3ac3dd3d662c913b17cdc8702a0c23879b0c78fbd396fd0b926
'http://security.ubuntu.com/ubuntu/pool/main/c/curl/curl_8.5.0-2ubuntu10.8.debian.tar.xz' curl_8.5.0-2ubuntu10.8.debian.tar.xz 68580 SHA512:77e8200e621f66172bc9b53c25d0c53dc5ec08add353c2c72f2584b6e0fb15937e01611c6c8d5795ad8d3186bf60327e4ddaf3b3d48cbac97f2d080c3a1ffc18
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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `dconf=0.40.0-4ubuntu0.1`

Binary Packages:

- `libdconf1:amd64=0.40.0-4ubuntu0.1`

Licenses: (parsed from: `/usr/share/doc/libdconf1/copyright`)

- `GPL-3`
- `LGPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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


### `dpkg` source package: `elfutils=0.190-1.1ubuntu0.1`

Binary Packages:

- `libdw1t64:amd64=0.190-1.1ubuntu0.1`
- `libelf1t64:amd64=0.190-1.1ubuntu0.1`

Licenses: (parsed from: `/usr/share/doc/libdw1t64/copyright`, `/usr/share/doc/libelf1t64/copyright`)

- `BSD-2-clause`
- `GFDL-1.3`
- `GFDL-NIV-1.3`
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
$ apt-get source -qq --print-uris elfutils=0.190-1.1ubuntu0.1
'http://security.ubuntu.com/ubuntu/pool/main/e/elfutils/elfutils_0.190-1.1ubuntu0.1.dsc' elfutils_0.190-1.1ubuntu0.1.dsc 3410 SHA512:56440e43ecfac444cca2cbd6f2a33f2780cea395b5caa302587c4a1e602b3c4bb45dbcede76e7767b6f18f519458b52c6300ef83b80cdebc603418fe2a4a0889
'http://security.ubuntu.com/ubuntu/pool/main/e/elfutils/elfutils_0.190.orig.tar.bz2' elfutils_0.190.orig.tar.bz2 9162766 SHA512:9c4f5328097e028286c42f29e39dc3d80914b656cdfbbe05b639e91bc787ae8ae64dd4d69a6e317ce30c01648ded10281b86a51e718295f4c589df1225a48102
'http://security.ubuntu.com/ubuntu/pool/main/e/elfutils/elfutils_0.190-1.1ubuntu0.1.debian.tar.xz' elfutils_0.190-1.1ubuntu0.1.debian.tar.xz 46976 SHA512:f4bf523b754c8fd09c189483b3f084955b2b467e5e03338e2448ec0d4af478ea39a7d7bd4c2b7dfcfbe538a870ec452c51f840e6c33b0ffdec65837c2f6384cd
```

### `dpkg` source package: `expat=2.6.1-2ubuntu0.4`

Binary Packages:

- `libexpat1:amd64=2.6.1-2ubuntu0.4`

Licenses: (parsed from: `/usr/share/doc/libexpat1/copyright`)

- `MIT`

Source:

```console
$ apt-get source -qq --print-uris expat=2.6.1-2ubuntu0.4
'http://security.ubuntu.com/ubuntu/pool/main/e/expat/expat_2.6.1-2ubuntu0.4.dsc' expat_2.6.1-2ubuntu0.4.dsc 1945 SHA512:82a09968f6bdffeae412f3e96d26d09f43fc3e6a6c5bc57aa61eb6c589184d67f252ae3d36c30425dc8c7bcae62f15a745a13598bb9354a8d7b1fa5f8bf1cafe
'http://security.ubuntu.com/ubuntu/pool/main/e/expat/expat_2.6.1.orig.tar.gz' expat_2.6.1.orig.tar.gz 8414649 SHA512:cf6c64fc0ca55dd172ca8a6ca10d1fb2c915d0f941b0068f42cb90488022dea73e04119c49a1bd4ab9a5d425ddc132ae5f22260ff6d2e25204637a1169e7bd4f
'http://security.ubuntu.com/ubuntu/pool/main/e/expat/expat_2.6.1-2ubuntu0.4.debian.tar.xz' expat_2.6.1-2ubuntu0.4.debian.tar.xz 31092 SHA512:8d460f748c1b1d2e35805ec2f390b029841dc5dc0e3380205d65e12d30b3d15ea47c4572d13886192227a8a262224817fb90be75c75c43fcb299dee7bf6e545e
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
'http://security.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.13.2%2bdfsg-1ubuntu0.1.dsc' freetype_2.13.2+dfsg-1ubuntu0.1.dsc 3606 SHA512:22245fbb1266fc62fceaf84b1e80e6228c0ba847f916b2eef692509ceaa7cb45adfc5fdf8f6f561d68876bf07c161cfd4c3bc478ffd6557c6054cfb63c91cdf8
'http://security.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.13.2%2bdfsg.orig-ft2demos.tar.xz' freetype_2.13.2+dfsg.orig-ft2demos.tar.xz 341140 SHA512:aa83ba4212ff7c4453b72f036136cb9b04cacf7d196388a3e4752613e000b3bb45a4dcf63d3d1d5b3d6ada10720304b532fb6e33ed6a5b399dcce45c27af9ade
'http://security.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.13.2%2bdfsg.orig-ft2demos.tar.xz.asc' freetype_2.13.2+dfsg.orig-ft2demos.tar.xz.asc 833 SHA512:07680e2919643cb1b964c311f1590fddd38f42189944b3e5e46a9c6a84688255749506f8a745d52255e3599e5136f3e8761d746a67cdcd6e565b8eaecb9fd792
'http://security.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.13.2%2bdfsg.orig-ft2docs.tar.xz' freetype_2.13.2+dfsg.orig-ft2docs.tar.xz 2173920 SHA512:ca3438dcf6f995af556d8db3cb3cfdcabb81ab5a7dd88464ff757e3e418b3219b0011857cde8a338372e30d8375486ac8e50914da2ea948dc874f70010bce60c
'http://security.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.13.2%2bdfsg.orig-ft2docs.tar.xz.asc' freetype_2.13.2+dfsg.orig-ft2docs.tar.xz.asc 833 SHA512:b346579fcc8f073e586135c72140c64bb3d5ca46201b879e3976b39a62a14f6668a5009d39b078e51d51a7301e346b4de6f7e9ee365f9b44146e67579aaf6500
'http://security.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.13.2%2bdfsg.orig.tar.xz' freetype_2.13.2+dfsg.orig.tar.xz 2220368 SHA512:8809693981ea7ef274d882245e3257305b65ad73e5ae36bb7e4ffc769a97b726d6bd07f1627dae456519e02e3eaa43269769d7ad363f49b9247d27d2c6f47d6d
'http://security.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.13.2%2bdfsg-1ubuntu0.1.debian.tar.xz' freetype_2.13.2+dfsg-1ubuntu0.1.debian.tar.xz 44692 SHA512:67a909adcb43e69ac25e55e4c87f7389f79a9bc06ce7b33bdd13496aa68648ea1a2b5d3177b6cc805c8c3e4a36529a963c4313cb987a887b40089843a71178de
```

### `dpkg` source package: `gcc-14=14.2.0-4ubuntu2~24.04.1`

Binary Packages:

- `gcc-14-base:amd64=14.2.0-4ubuntu2~24.04.1`
- `libgcc-s1:amd64=14.2.0-4ubuntu2~24.04.1`
- `libgomp1:amd64=14.2.0-4ubuntu2~24.04.1`
- `libstdc++6:amd64=14.2.0-4ubuntu2~24.04.1`

Licenses: (parsed from: `/usr/share/doc/gcc-14-base/copyright`, `/usr/share/doc/libgcc-s1/copyright`, `/usr/share/doc/libgomp1/copyright`, `/usr/share/doc/libstdc++6/copyright`)

- `Artistic`
- `GFDL-1.2`
- `GPL`
- `GPL-3`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris gcc-14=14.2.0-4ubuntu2~24.04.1
'http://security.ubuntu.com/ubuntu/pool/main/g/gcc-14/gcc-14_14.2.0-4ubuntu2%7e24.04.1.dsc' gcc-14_14.2.0-4ubuntu2~24.04.1.dsc 46930 SHA512:e73c3c31529bf34e4cc91360a18ceed91c752bcd8344da68a0b9e9a178b0981fac02e88f12861b4dc60b261fe51fe931b4b27955d39191bc2c84142d704f4d51
'http://security.ubuntu.com/ubuntu/pool/main/g/gcc-14/gcc-14_14.2.0.orig.tar.gz' gcc-14_14.2.0.orig.tar.gz 97158172 SHA512:88621e344786a78d825110dbd46a9dc811ab0a3414bde97a700b0c90991020dc31dbba89cdbed24ef2875a63ae9c0adffdbc1064262e5270d80920c9964bfb21
'http://security.ubuntu.com/ubuntu/pool/main/g/gcc-14/gcc-14_14.2.0-4ubuntu2%7e24.04.1.debian.tar.xz' gcc-14_14.2.0-4ubuntu2~24.04.1.debian.tar.xz 1950432 SHA512:039f728b7fd2256dad82e120d48dbec7fbece9c1fb5bbfca9019312d5a4e6a799d2c81fa09b377b850375a89be262aa080587df562f4bd6b7b6eba17ab9e29f9
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
'http://security.ubuntu.com/ubuntu/pool/main/g/glib2.0/glib2.0_2.80.0-6ubuntu3.8.dsc' glib2.0_2.80.0-6ubuntu3.8.dsc 4542 SHA512:48e0f0df53d01363f614b73f158c7f4c39954f7a5b8aa991a235b3f71e3c61a087b7e0ced00827e849435a96e2dcb12c4ffb513b01b9cfe0e9f05622908b6e92
'http://security.ubuntu.com/ubuntu/pool/main/g/glib2.0/glib2.0_2.80.0.orig-unicode-data.tar.xz' glib2.0_2.80.0.orig-unicode-data.tar.xz 263364 SHA512:1d1c00d7416d90aac86d851fc2df94f2a97cb100a3b99f2ac28a0660deea64b994f56bbc7c05b6c7ef3b6c3a2cb18267ebc5d189abf58bd922321b509c86e2b6
'http://security.ubuntu.com/ubuntu/pool/main/g/glib2.0/glib2.0_2.80.0.orig.tar.xz' glib2.0_2.80.0.orig.tar.xz 5510536 SHA512:1514d62aeb4c4a1a1048ae0f84f7db7f0dbf355772b2dadf6a34ec547045b163a5e28331b096e7616fe3c9c19bed98025a0202b05073f5d7ee901d0efaffe143
'http://security.ubuntu.com/ubuntu/pool/main/g/glib2.0/glib2.0_2.80.0-6ubuntu3.8.debian.tar.xz' glib2.0_2.80.0-6ubuntu3.8.debian.tar.xz 166540 SHA512:09f2203f684462dfba86cde8239912fd364d695fc1f5e60f22a972b01111025c02dca51e1ead341c331ee47044afb231a64065ab0119bff9d7fa9fd6fe45bc52
```

### `dpkg` source package: `glibc=2.39-0ubuntu8.7`

Binary Packages:

- `libc-bin=2.39-0ubuntu8.7`
- `libc6:amd64=2.39-0ubuntu8.7`
- `locales=2.39-0ubuntu8.7`

Licenses: (parsed from: `/usr/share/doc/libc-bin/copyright`, `/usr/share/doc/libc6/copyright`, `/usr/share/doc/locales/copyright`)

- `GFDL-1.3`
- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris glibc=2.39-0ubuntu8.7
'http://security.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.39-0ubuntu8.7.dsc' glibc_2.39-0ubuntu8.7.dsc 9257 SHA512:413efc529754f26d91d4c9efb8b697df56dce1650c58016463795c487e9c11e6c296ee97ae652a1a4d395921075b85929ac02c649e19e5ecb2c24a300942003f
'http://security.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.39.orig.tar.xz' glibc_2.39.orig.tar.xz 18520988 SHA512:818f58172a52815b4338ea9f2a69ecaa3335492b9f8f64cbf8afb24c0d737982341968ecd79631cae3d3074ab0ae4bc6056fc4ba3ffe790849dc374835cd57e2
'http://security.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.39.orig.tar.xz.asc' glibc_2.39.orig.tar.xz.asc 833 SHA512:5c054af523bbf5c2453363c023eadd1a75b6a5ff55c739011030115d3b117dbfc7d80cc74fbf157ea74a8d24aa14ff560c675374f875ec5c1ed3030e26a5ee07
'http://security.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.39-0ubuntu8.7.debian.tar.xz' glibc_2.39-0ubuntu8.7.debian.tar.xz 469880 SHA512:12758ed1b5e0337ad202f8a66332fdbea8a217531a2a01819847d08207afa65b114943d712b8b27f83f0f370c07371fddd9ed20661f683fbb4d9386cd4f57893
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
'http://security.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.8.3-1.1ubuntu3.5.dsc' gnutls28_3.8.3-1.1ubuntu3.5.dsc 3397 SHA512:f27e044c5a43a466d94883b9578e7e5b8dda3b807de4dbbf533e34701c2146f43696260a47c18bf85d8801db1ab457d5a6772741f0f1dffcd31120203181ad5d
'http://security.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.8.3.orig.tar.xz' gnutls28_3.8.3.orig.tar.xz 6463720 SHA512:74eddba01ce4c2ffdca781c85db3bb52c85f1db3c09813ee2b8ceea0608f92ca3912fd9266f55deb36a8ba4d01802895ca5d5d219e7d9caec45e1a8534e45a84
'http://security.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.8.3.orig.tar.xz.asc' gnutls28_3.8.3.orig.tar.xz.asc 854 SHA512:8a13a834b57172b9504313eeb7d733d2c3d72971dd8adaa837bbd9d73b12fe2a67f7d07fbbaf643a34ff95acaa82458a88ce4118152ede8ece9be5a089b693c8
'http://security.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.8.3-1.1ubuntu3.5.debian.tar.xz' gnutls28_3.8.3-1.1ubuntu3.5.debian.tar.xz 109884 SHA512:66368bfc1a4266368bef58642388468f00e6da678632b7d7fb3d19c06f95d8b5187be80732d1b1b3c38dd1cdc280fc978b73e5f25a88baa74129e2185258e819
```

### `dpkg` source package: `gpgme1.0=1.18.0-4.1ubuntu4`

Binary Packages:

- `libgpgme11t64:amd64=1.18.0-4.1ubuntu4`
- `libgpgmepp6t64:amd64=1.18.0-4.1ubuntu4`

Licenses: (parsed from: `/usr/share/doc/libgpgme11t64/copyright`, `/usr/share/doc/libgpgmepp6t64/copyright`)

- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`
- `LGPL-3+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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


### `dpkg` source package: `grep=3.11-4build1`

Binary Packages:

- `grep=3.11-4build1`

Licenses: (parsed from: `/usr/share/doc/grep/copyright`)

- `GPL-3`
- `GPL-3+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `gst-plugins-base1.0=1.24.2-1ubuntu0.4`

Binary Packages:

- `libgstreamer-plugins-base1.0-0:amd64=1.24.2-1ubuntu0.4`

Licenses: (parsed from: `/usr/share/doc/libgstreamer-plugins-base1.0-0/copyright`)

- `BSD (2 clause)`
- `BSD (3 clause)`
- `GPL-2+`
- `LGPL`
- `LGPL-2+`
- `MIT/X11 (BSD like) LGPL-2+`

Source:

```console
$ apt-get source -qq --print-uris gst-plugins-base1.0=1.24.2-1ubuntu0.4
'http://security.ubuntu.com/ubuntu/pool/main/g/gst-plugins-base1.0/gst-plugins-base1.0_1.24.2-1ubuntu0.4.dsc' gst-plugins-base1.0_1.24.2-1ubuntu0.4.dsc 4113 SHA512:d17cbafc3563b4ca4cb14df70dc13acdd5463872d6a84fae35c4773119f090c15869375e11ca7c16146e6ff965621d8cd9298fe6fcfce72fcfe8cd3e6034513b
'http://security.ubuntu.com/ubuntu/pool/main/g/gst-plugins-base1.0/gst-plugins-base1.0_1.24.2.orig.tar.xz' gst-plugins-base1.0_1.24.2.orig.tar.xz 2421032 SHA512:8b4ffbbf427859c4d8ba889034b00ea8314e4357645c788f6b52d65a512ce76fa1840f2a4fd562d92b213ad9dc9636db44de289bc56600ae19bce39e156b1579
'http://security.ubuntu.com/ubuntu/pool/main/g/gst-plugins-base1.0/gst-plugins-base1.0_1.24.2.orig.tar.xz.asc' gst-plugins-base1.0_1.24.2.orig.tar.xz.asc 833 SHA512:996a9c50facd6d6b4e9496874320fcb1aa374b0ec0a14b9945238b7e233f933856f3b91cc332da2f1e246c870f51373b3d1b9de455bd3d70e51b5a32be429f70
'http://security.ubuntu.com/ubuntu/pool/main/g/gst-plugins-base1.0/gst-plugins-base1.0_1.24.2-1ubuntu0.4.debian.tar.xz' gst-plugins-base1.0_1.24.2-1ubuntu0.4.debian.tar.xz 57620 SHA512:d644ae71ab83c8a02b3d7c7a98a7aae8d0cab74b5aea4a2de79b42db9b4824d0d6d13f82f985df17bfb43f7cb087a922ba2803f83fc7bd797f64ed8f41697afa
```

### `dpkg` source package: `gstreamer1.0=1.24.2-1ubuntu0.1`

Binary Packages:

- `libgstreamer1.0-0:amd64=1.24.2-1ubuntu0.1`

Licenses: (parsed from: `/usr/share/doc/libgstreamer1.0-0/copyright`)

- `GPL-2+`
- `GPL-3+`
- `LGPL`
- `LGPL-2+`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris gstreamer1.0=1.24.2-1ubuntu0.1
'http://security.ubuntu.com/ubuntu/pool/main/g/gstreamer1.0/gstreamer1.0_1.24.2-1ubuntu0.1.dsc' gstreamer1.0_1.24.2-1ubuntu0.1.dsc 3161 SHA512:c44b2bcb46e1bc27fa70dfbb338ef53dee528ae63614cc1727438d59de8ae60dadad8b9ec90d0dbe5e7f2457f618891fcf8b049b007010659bf4d5a93e0a74b9
'http://security.ubuntu.com/ubuntu/pool/main/g/gstreamer1.0/gstreamer1.0_1.24.2.orig.tar.xz' gstreamer1.0_1.24.2.orig.tar.xz 1850672 SHA512:8d7b3e129025d66b0c3938fcb51574c378f5104cf44d1c827795f25687efc98e85bc0dac76bd8e8c4adf6434457495816a8a91a04734269722dcf7c2ed67f88b
'http://security.ubuntu.com/ubuntu/pool/main/g/gstreamer1.0/gstreamer1.0_1.24.2.orig.tar.xz.asc' gstreamer1.0_1.24.2.orig.tar.xz.asc 833 SHA512:191caa06febb372a402adbfd3b1e52cc702a6c98cff1de2a47aa96edeed197a46a5fc1f14fbd43791c67bb9336dd89f45b38f7e31781464d564609bd3f5a87ff
'http://security.ubuntu.com/ubuntu/pool/main/g/gstreamer1.0/gstreamer1.0_1.24.2-1ubuntu0.1.debian.tar.xz' gstreamer1.0_1.24.2-1ubuntu0.1.debian.tar.xz 50960 SHA512:a4dd33a3381c59ef061dedd01f76d4e7638fb68771437890daff17c71ee5a78f7958b363bbeef38aa04f27869038ef53756ef52c59079eecb1529ff3cdd0a508
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


### `dpkg` source package: `harfbuzz=8.3.0-2build2`

Binary Packages:

- `libharfbuzz-icu0:amd64=8.3.0-2build2`
- `libharfbuzz0b:amd64=8.3.0-2build2`

Licenses: (parsed from: `/usr/share/doc/libharfbuzz-icu0/copyright`, `/usr/share/doc/libharfbuzz0b/copyright`)

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


### `dpkg` source package: `hunspell=1.7.2+really1.7.2-10build3`

Binary Packages:

- `libhunspell-1.7-0:amd64=1.7.2+really1.7.2-10build3`

Licenses: (parsed from: `/usr/share/doc/libhunspell-1.7-0/copyright`)

- `GPL-2`
- `LGPL-2.1`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `hyphen=2.8.8-7build3`

Binary Packages:

- `libhyphen0:amd64=2.8.8-7build3`

Licenses: (parsed from: `/usr/share/doc/libhyphen0/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `MPL-1.1+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `icu=74.2-1ubuntu3.1`

Binary Packages:

- `libicu74:amd64=74.2-1ubuntu3.1`

Licenses: (parsed from: `/usr/share/doc/libicu74/copyright`)

- `GPL-3`
- `MIT`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `init-system-helpers=1.66ubuntu1`

Binary Packages:

- `init-system-helpers=1.66ubuntu1`

Licenses: (parsed from: `/usr/share/doc/init-system-helpers/copyright`)

- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `iso-codes=4.16.0-1`

Binary Packages:

- `iso-codes=4.16.0-1`

Licenses: (parsed from: `/usr/share/doc/iso-codes/copyright`)

- `LGPL-2.1`
- `LGPL-2.1+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/iso-codes/4.16.0-1/


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

### `dpkg` source package: `lcms2=2.14-2build1`

Binary Packages:

- `liblcms2-2:amd64=2.14-2build1`

Licenses: (parsed from: `/usr/share/doc/liblcms2-2/copyright`)

- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `IJG`
- `MIT`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `lerc=4.0.0+ds-4ubuntu2`

Binary Packages:

- `liblerc4:amd64=4.0.0+ds-4ubuntu2`

Licenses: (parsed from: `/usr/share/doc/liblerc4/copyright`)

- `Apache-2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libabw=0.1.3-1build4`

Binary Packages:

- `libabw-0.1-1:amd64=0.1.3-1build4`

Licenses: (parsed from: `/usr/share/doc/libabw-0.1-1/copyright`)

- `GPL-3`
- `LGPL-3`
- `MPL-1.1 | GPL-3 | LGPL-3`
- `MPL-2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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
- `libcap2-bin=1:2.66-5ubuntu2.2`

Licenses: (parsed from: `/usr/share/doc/libcap2/copyright`, `/usr/share/doc/libcap2-bin/copyright`)

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

### `dpkg` source package: `libcdr=0.1.7-1build2`

Binary Packages:

- `libcdr-0.1-1:amd64=0.1.7-1build2`

Licenses: (parsed from: `/usr/share/doc/libcdr-0.1-1/copyright`)

- `MPL-2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libdeflate=1.19-1build1.1`

Binary Packages:

- `libdeflate0:amd64=1.19-1build1.1`

Licenses: (parsed from: `/usr/share/doc/libdeflate0/copyright`)

- `Expat`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libdrm=2.4.125-1ubuntu0.1~24.04.1`

Binary Packages:

- `libdrm-common=2.4.125-1ubuntu0.1~24.04.1`
- `libdrm2:amd64=2.4.125-1ubuntu0.1~24.04.1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libe-book=0.1.3-2build6`

Binary Packages:

- `libe-book-0.1-1:amd64=0.1.3-2build6`

Licenses: (parsed from: `/usr/share/doc/libe-book-0.1-1/copyright`)

- `MPL-2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libeot=0.01-5build3`

Binary Packages:

- `libeot0:amd64=0.01-5build3`

Licenses: (parsed from: `/usr/share/doc/libeot0/copyright`)

- `GPL-2`
- `GPL-2+`
- `MPL-2.0`
- `other`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libepoxy=1.5.10-1build1`

Binary Packages:

- `libepoxy0:amd64=1.5.10-1build1`

Licenses: (parsed from: `/usr/share/doc/libepoxy0/copyright`)

- `Expat`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libepubgen=0.1.1-1ubuntu6`

Binary Packages:

- `libepubgen-0.1-1:amd64=0.1.1-1ubuntu6`

Licenses: (parsed from: `/usr/share/doc/libepubgen-0.1-1/copyright`)

- `MPL-2.0`
- `other`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libetonyek=0.1.10-5build1`

Binary Packages:

- `libetonyek-0.1-1:amd64=0.1.10-5build1`

Licenses: (parsed from: `/usr/share/doc/libetonyek-0.1-1/copyright`)

- `MPL 2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libexttextcat=3.4.7-1build1`

Binary Packages:

- `libexttextcat-2.0-0:amd64=3.4.7-1build1`
- `libexttextcat-data=3.4.7-1build1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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


### `dpkg` source package: `libfreehand=0.1.2-3build3`

Binary Packages:

- `libfreehand-0.1-1=0.1.2-3build3`

Licenses: (parsed from: `/usr/share/doc/libfreehand-0.1-1/copyright`)

- `GPL-3`
- `LGPL-3`
- `MPL-1.1 | GPL-3+ | LGPL-3+`
- `MPL-2.0`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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


### `dpkg` source package: `libksba=1.6.6-1build1`

Binary Packages:

- `libksba8:amd64=1.6.6-1build1`

Licenses: (parsed from: `/usr/share/doc/libksba8/copyright`)

- `FSFUL`
- `GPL-3`
- `LGPL-2.1-or-later`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `liblangtag=0.6.7-1build2`

Binary Packages:

- `liblangtag-common=0.6.7-1build2`
- `liblangtag1:amd64=0.6.7-1build2`

Licenses: (parsed from: `/usr/share/doc/liblangtag-common/copyright`, `/usr/share/doc/liblangtag1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL | MPL`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libmspub=0.1.4-3build7`

Binary Packages:

- `libmspub-0.1-1:amd64=0.1.4-3build7`

Licenses: (parsed from: `/usr/share/doc/libmspub-0.1-1/copyright`)

- `MPL-2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libmwaw=0.3.22-1build1`

Binary Packages:

- `libmwaw-0.3-3:amd64=0.3.22-1build1`

Licenses: (parsed from: `/usr/share/doc/libmwaw-0.3-3/copyright`)

- `BSD`
- `LGPL`
- `MPL2.0 | LGPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libodfgen=0.1.8-2build3`

Binary Packages:

- `libodfgen-0.1-1:amd64=0.1.8-2build3`

Licenses: (parsed from: `/usr/share/doc/libodfgen-0.1-1/copyright`)

- `LGPL`
- `MPL-2.0 | LGPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `liborcus=0.19.2-3build3`

Binary Packages:

- `liborcus-0.18-0:amd64=0.19.2-3build3`
- `liborcus-parser-0.18-0:amd64=0.19.2-3build3`

Licenses: (parsed from: `/usr/share/doc/liborcus-0.18-0/copyright`, `/usr/share/doc/liborcus-parser-0.18-0/copyright`)

- `Expat`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+ with autoconf exception`
- `MIT`
- `MPL-2.0`
- `other`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libpagemaker=0.0.4-1build4`

Binary Packages:

- `libpagemaker-0.0-0:amd64=0.0.4-1build4`

Licenses: (parsed from: `/usr/share/doc/libpagemaker-0.0-0/copyright`)

- `MPL-2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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
'http://security.ubuntu.com/ubuntu/pool/main/libp/libpng1.6/libpng1.6_1.6.43-5ubuntu0.5.dsc' libpng1.6_1.6.43-5ubuntu0.5.dsc 2384 SHA512:a14182cd7f13f9197e459e59ab360a3db55a4c8b83c4594ca2442ff073071def2a868b9e2fb345753579996146f90bdfaeae0c3147c61ea9d06a9150774597ec
'http://security.ubuntu.com/ubuntu/pool/main/libp/libpng1.6/libpng1.6_1.6.43.orig.tar.gz' libpng1.6_1.6.43.orig.tar.gz 1554715 SHA512:3bb2a7b73113be42b09c2116e6c6f5a7ddb4e2ab06e0b13e10b7314acdccc4bb624ff602e16140c0484f6cde80efa190296226be3da195c6926819f07c723c12
'http://security.ubuntu.com/ubuntu/pool/main/libp/libpng1.6/libpng1.6_1.6.43-5ubuntu0.5.debian.tar.xz' libpng1.6_1.6.43-5ubuntu0.5.debian.tar.xz 40772 SHA512:52d19a21825a99a19951e43a1850a2a03b77867f0f5d194d8db910c438d7c1153c4eceea6529a15e0a86c65be5822a071007edbd8cfe1a7c094ff38221a9b5cf
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


### `dpkg` source package: `libreoffice=4:24.2.7-0ubuntu0.24.04.4`

Binary Packages:

- `fonts-opensymbol=4:102.12+LibO24.2.7-0ubuntu0.24.04.4`
- `libreoffice=4:24.2.7-0ubuntu0.24.04.4`
- `libreoffice-base=4:24.2.7-0ubuntu0.24.04.4`
- `libreoffice-base-core=4:24.2.7-0ubuntu0.24.04.4`
- `libreoffice-base-drivers=4:24.2.7-0ubuntu0.24.04.4`
- `libreoffice-calc=4:24.2.7-0ubuntu0.24.04.4`
- `libreoffice-common=4:24.2.7-0ubuntu0.24.04.4`
- `libreoffice-core=4:24.2.7-0ubuntu0.24.04.4`
- `libreoffice-draw=4:24.2.7-0ubuntu0.24.04.4`
- `libreoffice-impress=4:24.2.7-0ubuntu0.24.04.4`
- `libreoffice-math=4:24.2.7-0ubuntu0.24.04.4`
- `libreoffice-report-builder-bin=4:24.2.7-0ubuntu0.24.04.4`
- `libreoffice-style-colibre=4:24.2.7-0ubuntu0.24.04.4`
- `libreoffice-uiconfig-base=4:24.2.7-0ubuntu0.24.04.4`
- `libreoffice-uiconfig-calc=4:24.2.7-0ubuntu0.24.04.4`
- `libreoffice-uiconfig-common=4:24.2.7-0ubuntu0.24.04.4`
- `libreoffice-uiconfig-draw=4:24.2.7-0ubuntu0.24.04.4`
- `libreoffice-uiconfig-impress=4:24.2.7-0ubuntu0.24.04.4`
- `libreoffice-uiconfig-math=4:24.2.7-0ubuntu0.24.04.4`
- `libreoffice-uiconfig-writer=4:24.2.7-0ubuntu0.24.04.4`
- `libreoffice-writer=4:24.2.7-0ubuntu0.24.04.4`
- `libuno-cppu3t64=4:24.2.7-0ubuntu0.24.04.4`
- `libuno-cppuhelpergcc3-3t64=4:24.2.7-0ubuntu0.24.04.4`
- `libuno-purpenvhelpergcc3-3t64=4:24.2.7-0ubuntu0.24.04.4`
- `libuno-sal3t64=4:24.2.7-0ubuntu0.24.04.4`
- `libuno-salhelpergcc3-3t64=4:24.2.7-0ubuntu0.24.04.4`
- `python3-uno=4:24.2.7-0ubuntu0.24.04.4`
- `uno-libs-private=4:24.2.7-0ubuntu0.24.04.4`
- `ure=4:24.2.7-0ubuntu0.24.04.4`

Licenses: (parsed from: `/usr/share/doc/fonts-opensymbol/copyright`, `/usr/share/doc/libreoffice/copyright`, `/usr/share/doc/libreoffice-base/copyright`, `/usr/share/doc/libreoffice-base-core/copyright`, `/usr/share/doc/libreoffice-base-drivers/copyright`, `/usr/share/doc/libreoffice-calc/copyright`, `/usr/share/doc/libreoffice-common/copyright`, `/usr/share/doc/libreoffice-core/copyright`, `/usr/share/doc/libreoffice-draw/copyright`, `/usr/share/doc/libreoffice-impress/copyright`, `/usr/share/doc/libreoffice-math/copyright`, `/usr/share/doc/libreoffice-report-builder-bin/copyright`, `/usr/share/doc/libreoffice-style-colibre/copyright`, `/usr/share/doc/libreoffice-uiconfig-base/copyright`, `/usr/share/doc/libreoffice-uiconfig-calc/copyright`, `/usr/share/doc/libreoffice-uiconfig-common/copyright`, `/usr/share/doc/libreoffice-uiconfig-draw/copyright`, `/usr/share/doc/libreoffice-uiconfig-impress/copyright`, `/usr/share/doc/libreoffice-uiconfig-math/copyright`, `/usr/share/doc/libreoffice-uiconfig-writer/copyright`, `/usr/share/doc/libreoffice-writer/copyright`, `/usr/share/doc/libuno-cppu3t64/copyright`, `/usr/share/doc/libuno-cppuhelpergcc3-3t64/copyright`, `/usr/share/doc/libuno-purpenvhelpergcc3-3t64/copyright`, `/usr/share/doc/libuno-sal3t64/copyright`, `/usr/share/doc/libuno-salhelpergcc3-3t64/copyright`, `/usr/share/doc/python3-uno/copyright`, `/usr/share/doc/uno-libs-private/copyright`, `/usr/share/doc/ure/copyright`)

- `Apache-2.0`
- `BSD-2-clause`
- `BSD-3-clause`
- `CC-BY-SA-3.0`
- `CC0-1.0`
- `Expat`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `LGPL-2`
- `LGPL-3`
- `LGPL-3+`
- `MIT`
- `MPL-1.1`
- `MPL-2.0`
- `other`

Source:

```console
$ apt-get source -qq --print-uris libreoffice=4:24.2.7-0ubuntu0.24.04.4
'http://security.ubuntu.com/ubuntu/pool/main/libr/libreoffice/libreoffice_24.2.7-0ubuntu0.24.04.4.dsc' libreoffice_24.2.7-0ubuntu0.24.04.4.dsc 26996 SHA512:51188e49a50416b07268472a83bc619ace032568b559d1438123e359914564a5913e8c5402eabd6462c8ae1058bdfc19f8d7da960a6ac4d1b4d69330381a7c37
'http://security.ubuntu.com/ubuntu/pool/main/libr/libreoffice/libreoffice_24.2.7.orig-helpcontent2.tar.xz' libreoffice_24.2.7.orig-helpcontent2.tar.xz 165548208 SHA512:f4021e8add490591997076a355a321f436b49e5aba9191ed5e9b6104176b42825678d824bb7c70235d6a3ae3b44db4b39c7a823b066ddc80d6dc630b0ed110fb
'http://security.ubuntu.com/ubuntu/pool/main/libr/libreoffice/libreoffice_24.2.7.orig-tarballs.tar.xz' libreoffice_24.2.7.orig-tarballs.tar.xz 213487760 SHA512:6b26f7f743a7d742958cb718877282cfd555e37421503e8ffbafa23269ef4db5398c15673b1d1067e03a3a790f7fae78d7a528b758e5c3988fac1976f06451a7
'http://security.ubuntu.com/ubuntu/pool/main/libr/libreoffice/libreoffice_24.2.7.orig-translations.tar.xz' libreoffice_24.2.7.orig-translations.tar.xz 222584892 SHA512:f878b8cb3dee544a7b7f4581f6a71f72c747a97fdf668fd7f680a29926dd821cae7453cda020e91016e1416943d88331c79129890a0d52dfbe8a0a5fcda2b23c
'http://security.ubuntu.com/ubuntu/pool/main/libr/libreoffice/libreoffice_24.2.7.orig-yaru.tar.xz' libreoffice_24.2.7.orig-yaru.tar.xz 19874368 SHA512:3c805e96dbe682f17c5b1b5fad1bf3445c7d4aa24b9a5700f508cdf1d2b7a2761f213f738d5c878643205c6f200af96c8c0aa226dcec2485fa6992f9d8f5727e
'http://security.ubuntu.com/ubuntu/pool/main/libr/libreoffice/libreoffice_24.2.7.orig.tar.xz' libreoffice_24.2.7.orig.tar.xz 279885536 SHA512:f5e9cfc9d37d4890f691fbdf424e68623bbb37d8a9910aad1dc1e26cb4d38f6e5ca15f5bceb08d1cac6cbc37a3ddb0e50b873405e9f277e199bf08d0838346da
'http://security.ubuntu.com/ubuntu/pool/main/libr/libreoffice/libreoffice_24.2.7.orig.tar.xz.asc' libreoffice_24.2.7.orig.tar.xz.asc 833 SHA512:55f9948e9403666867c178e72bb5f3c05744f84ad74c9b2bbf3b126ab86da77bdec164bc000826761cde4779fc36b77dcdfd668b001ee1790b271200a8c570ec
'http://security.ubuntu.com/ubuntu/pool/main/libr/libreoffice/libreoffice_24.2.7-0ubuntu0.24.04.4.debian.tar.xz' libreoffice_24.2.7-0ubuntu0.24.04.4.debian.tar.xz 2423480 SHA512:11a7fba94ece5458af0597f50168a55d735d57e5cac44692a044649aab4f41f974f2dca9be406f06eea2bbec0802c80923d4e48cd216b6dddce55ab0a6ff479b
```

### `dpkg` source package: `librevenge=0.0.5-3build1`

Binary Packages:

- `librevenge-0.0-0:amd64=0.0.5-3build1`

Licenses: (parsed from: `/usr/share/doc/librevenge-0.0-0/copyright`)

- `LGPL-2.1`
- `MPL-1.1 | GPL-3+ | LGPL-3+`
- `MPL-2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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
'http://security.ubuntu.com/ubuntu/pool/main/libs/libssh/libssh_0.10.6-2ubuntu0.4.dsc' libssh_0.10.6-2ubuntu0.4.dsc 2723 SHA512:ac04327b00245b0587b437293e7294bdb42f62463e1213a335e5ddb52d80332bb1abe0b7d7bea2a80ef7bd60597aeb809a9c657632d17c02d088af35b7e2c4d7
'http://security.ubuntu.com/ubuntu/pool/main/libs/libssh/libssh_0.10.6.orig.tar.xz' libssh_0.10.6.orig.tar.xz 561036 SHA512:40c62d63c44e882999b71552c237d73fc7364313bd00b15a211a34aeff1b73693da441d2c8d4e40108d00fb7480ec7c5b6d472f9c0784b2359a179632ab0d6c1
'http://security.ubuntu.com/ubuntu/pool/main/libs/libssh/libssh_0.10.6.orig.tar.xz.asc' libssh_0.10.6.orig.tar.xz.asc 833 SHA512:214d7920bebc80a8e6838c64ed06e070709a96fabfb4fff657b55f9588bc0e1612887fe887d23de73ad3540f3bb85288e62eb6a11ccd4bc80afbd44d34ba70d4
'http://security.ubuntu.com/ubuntu/pool/main/libs/libssh/libssh_0.10.6-2ubuntu0.4.debian.tar.xz' libssh_0.10.6-2ubuntu0.4.debian.tar.xz 56400 SHA512:6cbb685d4e981014fa7aa01509ead2ab95ce665ed94d2ccbeb2c8394e972c40567543cd7e9e9cd6eba77af1ff9212dd2493a9e45150179caaa6c40a7c4e2fa9b
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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libunwind=1.6.2-3build1.1`

Binary Packages:

- `libunwind8:amd64=1.6.2-3build1.1`

Licenses: (parsed from: `/usr/share/doc/libunwind8/copyright`)

- `Expat`
- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libvisio=0.1.7-1build9`

Binary Packages:

- `libvisio-0.1-1:amd64=0.1.7-1build9`

Licenses: (parsed from: `/usr/share/doc/libvisio-0.1-1/copyright`)

- `MIT | GPL-2`
- `MPL-2.0`

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


### `dpkg` source package: `libwpd=0.10.3-2build2`

Binary Packages:

- `libwpd-0.10-10:amd64=0.10.3-2build2`

Licenses: (parsed from: `/usr/share/doc/libwpd-0.10-10/copyright`)

- `LGPL`
- `MPL-2.0 | LGPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libwpg=0.3.4-3build1`

Binary Packages:

- `libwpg-0.3-3:amd64=0.3.4-3build1`

Licenses: (parsed from: `/usr/share/doc/libwpg-0.3-3/copyright`)

- `GPL`
- `LGPL`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libwps=0.4.14-2build1`

Binary Packages:

- `libwps-0.4-4:amd64=0.4.14-2build1`

Licenses: (parsed from: `/usr/share/doc/libwps-0.4-4/copyright`)

- `LGPL-2.1`
- `LGPL-2.1+`
- `MPL-2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libx11=2:1.8.7-1build1`

Binary Packages:

- `libx11-6:amd64=2:1.8.7-1build1`
- `libx11-data=2:1.8.7-1build1`
- `libx11-xcb1:amd64=2:1.8.7-1build1`

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


### `dpkg` source package: `libxinerama=2:1.1.4-3build1`

Binary Packages:

- `libxinerama1:amd64=2:1.1.4-3build1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libxml2=2.9.14+dfsg-1.3ubuntu3.7`

Binary Packages:

- `libxml2:amd64=2.9.14+dfsg-1.3ubuntu3.7`

Licenses: (parsed from: `/usr/share/doc/libxml2/copyright`)

- `ISC`
- `MIT-1`

Source:

```console
$ apt-get source -qq --print-uris libxml2=2.9.14+dfsg-1.3ubuntu3.7
'http://security.ubuntu.com/ubuntu/pool/main/libx/libxml2/libxml2_2.9.14%2bdfsg-1.3ubuntu3.7.dsc' libxml2_2.9.14+dfsg-1.3ubuntu3.7.dsc 3083 SHA512:bd10326e5294c4a92fb4918a363cb8861f7a20fc876ec1c11e7edb6482a53aee85471a0c274244eeeda96f65b57aa260071d9aa033f169cd4e7fdc943ef09e5d
'http://security.ubuntu.com/ubuntu/pool/main/libx/libxml2/libxml2_2.9.14%2bdfsg.orig.tar.xz' libxml2_2.9.14+dfsg.orig.tar.xz 2351200 SHA512:1eacc9ac2cd8d38b8466659b3b9d84b94eb765c8f869d6cca0da131060bbc35c2b31c6148d59690547871a20cea339eac8fbe953b4fe37cf0900862f3fd9621b
'http://security.ubuntu.com/ubuntu/pool/main/libx/libxml2/libxml2_2.9.14%2bdfsg-1.3ubuntu3.7.debian.tar.xz' libxml2_2.9.14+dfsg-1.3ubuntu3.7.debian.tar.xz 52444 SHA512:4090c7600387e0ed6dc7acfa7f691d6ee3cbcd2da2ba305848a42c6497f9ac4cbc2c87b8c2c0659b15afc7373f8aef2a8473a465157a1cc3a1d982b79c2d2ba9
```

### `dpkg` source package: `libxrandr=2:1.5.2-2build1`

Binary Packages:

- `libxrandr2:amd64=2:1.5.2-2build1`

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
'http://security.ubuntu.com/ubuntu/pool/main/libx/libxslt/libxslt_1.1.39-0exp1ubuntu0.24.04.3.dsc' libxslt_1.1.39-0exp1ubuntu0.24.04.3.dsc 2352 SHA512:7709b2e2900154e58c792fa288a99ab1b90863e7e02400e510507b78aeb7b1e0e302995146e247c371fe8311cfe42d4861e8d6c176b045dc118d65902dbf61ff
'http://security.ubuntu.com/ubuntu/pool/main/libx/libxslt/libxslt_1.1.39.orig.tar.xz' libxslt_1.1.39.orig.tar.xz 1578216 SHA512:c0c99dc63f8b2acb6cc3ad7ad684ffa2a427ee8d1740495cbf8a7c9b9c8679f96351b4b676c73ccc191014db4cb4ab42b9a0070f6295565f39dbc665c5c16f89
'http://security.ubuntu.com/ubuntu/pool/main/libx/libxslt/libxslt_1.1.39-0exp1ubuntu0.24.04.3.debian.tar.xz' libxslt_1.1.39-0exp1ubuntu0.24.04.3.debian.tar.xz 24380 SHA512:e9ea90695741f2a81ccf3ca36c1ffd3806ce158242a77e29f0282bf4b124d5dcc0f8b60bd870c56d168a71f61f43b667720c37741a23dd9a4280b0c22063c69f
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


### `dpkg` source package: `lp-solve=5.5.2.5-2ubuntu0.1`

Binary Packages:

- `lp-solve=5.5.2.5-2ubuntu0.1`

Licenses: (parsed from: `/usr/share/doc/lp-solve/copyright`)

- `LGPL`

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


### `dpkg` source package: `mhash=0.9.9.9-9build3`

Binary Packages:

- `libmhash2:amd64=0.9.9.9-9build3`

Licenses: (parsed from: `/usr/share/doc/libmhash2/copyright`)

- `LGPL-2`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `mythes=2:1.2.5-1build1`

Binary Packages:

- `libmythes-1.2-0:amd64=2:1.2.5-1build1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `nspr=2:4.35-1.1build1`

Binary Packages:

- `libnspr4:amd64=2:4.35-1.1build1`

Licenses: (parsed from: `/usr/share/doc/libnspr4/copyright`)

- `MPL-2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `nss=2:3.98-1ubuntu0.1`

Binary Packages:

- `libnss3:amd64=2:3.98-1ubuntu0.1`

Licenses: (parsed from: `/usr/share/doc/libnss3/copyright`)

- `BSD-3`
- `MPL-2.0`
- `Zlib`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris nss=2:3.98-1ubuntu0.1
'http://security.ubuntu.com/ubuntu/pool/main/n/nss/nss_3.98-1ubuntu0.1.dsc' nss_3.98-1ubuntu0.1.dsc 2271 SHA512:b48bb350c9aa44d4293e29424a48e181efc99b8bfc8cc1af0084e53121121ba13627923ec0b537e27f415a51b8b32b002a1a0dae9426f120ac039fd38beb6c57
'http://security.ubuntu.com/ubuntu/pool/main/n/nss/nss_3.98.orig.tar.gz' nss_3.98.orig.tar.gz 76685475 SHA512:4f335c5c284eff6424745cc15e32037715a915f6f61687ec36a8ffaef0e45d152602a1be275bbb2f14650c7d258d6488430cdcf512b18ba7cb73cd43ac625681
'http://security.ubuntu.com/ubuntu/pool/main/n/nss/nss_3.98-1ubuntu0.1.debian.tar.xz' nss_3.98-1ubuntu0.1.debian.tar.xz 19968 SHA512:70c73c1807c62477299c7a48a6cec73d5049af4545870170b7d8655d6daccfdbcce39d0b55cdc534d2251099f6a059cc86d0932be9b3167a7ef6c292111953e2
```

### `dpkg` source package: `openjpeg2=2.5.0-2ubuntu0.4`

Binary Packages:

- `libopenjp2-7:amd64=2.5.0-2ubuntu0.4`

Licenses: (parsed from: `/usr/share/doc/libopenjp2-7/copyright`)

- `BSD-2`
- `BSD-3`
- `LIBPNG`
- `LIBTIFF`
- `LIBTIFF-GLARSON`
- `LIBTIFF-PIXAR`
- `MIT`
- `ZLIB`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris openjpeg2=2.5.0-2ubuntu0.4
'http://security.ubuntu.com/ubuntu/pool/main/o/openjpeg2/openjpeg2_2.5.0-2ubuntu0.4.dsc' openjpeg2_2.5.0-2ubuntu0.4.dsc 2788 SHA512:504ee1b73f90ab1b56d1dd7c66685d9ac215975ed572e3d44e2a2ca4403453eb4ee18f40bc2d4c409d77ab8dcf06b0fea02cb4a7e7b0a16bca69312514b9aee0
'http://security.ubuntu.com/ubuntu/pool/main/o/openjpeg2/openjpeg2_2.5.0.orig.tar.xz' openjpeg2_2.5.0.orig.tar.xz 1221108 SHA512:a266297d60ff93e14dbee890b01a76870bda69f082dbe8932fc444ccd260c27aaaac8b22e3c00ca71930b2555a1cad6cf6ed0d5d882d9d13f472cc494cab8234
'http://security.ubuntu.com/ubuntu/pool/main/o/openjpeg2/openjpeg2_2.5.0-2ubuntu0.4.debian.tar.xz' openjpeg2_2.5.0-2ubuntu0.4.debian.tar.xz 20344 SHA512:4d19bfd8fdc6a3a6baa4cf37fb5e3d1f30bc7a57b80307f15d7f35cd7541993e4ce9a743f2c230606433fcdc3e90c82c31d94c6557597e2eadce15fea08f9e3a
```

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `openssl=3.0.13-0ubuntu3.9`

Binary Packages:

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
'http://security.ubuntu.com/ubuntu/pool/main/o/openssl/openssl_3.0.13-0ubuntu3.9.dsc' openssl_3.0.13-0ubuntu3.9.dsc 2512 SHA512:bd293e19828a97bde4d3c8327399fbddc65e9350cc0dced2d8daff15970bbd4fdae9996b43c31d324e829d55d98bcc0e03b0f5e4f07ef8282f6d16cb4ed7990d
'http://security.ubuntu.com/ubuntu/pool/main/o/openssl/openssl_3.0.13.orig.tar.gz' openssl_3.0.13.orig.tar.gz 15294843 SHA512:22f4096781f0b075f5bf81bd39a0f97e111760dfa73b6f858f6bb54968a7847944d74969ae10f9a51cc21a2f4af20d9a4c463649dc824f5e439e196d6764c4f9
'http://security.ubuntu.com/ubuntu/pool/main/o/openssl/openssl_3.0.13-0ubuntu3.9.debian.tar.xz' openssl_3.0.13-0ubuntu3.9.debian.tar.xz 181192 SHA512:a196f92fa68f7b5f55efe4a0805bdc62bd62b16c5d2cb9523d588c5c39bea68f9b386de6a1b832d41eadcb082f1e6ea2f8df56a9faaf5c022dbd6e872b90b077
```

### `dpkg` source package: `orc=1:0.4.38-1ubuntu0.1`

Binary Packages:

- `liborc-0.4-0t64:amd64=1:0.4.38-1ubuntu0.1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris orc=1:0.4.38-1ubuntu0.1
'http://security.ubuntu.com/ubuntu/pool/main/o/orc/orc_0.4.38-1ubuntu0.1.dsc' orc_0.4.38-1ubuntu0.1.dsc 2571 SHA512:cae63b07c180dcee83afdf1b294e9694d4449696fd29a9c5a8bd302b1535b016030d43f3a2f2a4622b0a0fcc79ad2ae10768314959827bf2265fabd399856c81
'http://security.ubuntu.com/ubuntu/pool/main/o/orc/orc_0.4.38.orig.tar.xz' orc_0.4.38.orig.tar.xz 227152 SHA512:49f34be85f6980e4b5e94f848016f5788b658323f3a120110bc237722ac99938c02976efbe96022d148054330432899533305d4dd21be8fab76fd1995179339a
'http://security.ubuntu.com/ubuntu/pool/main/o/orc/orc_0.4.38.orig.tar.xz.asc' orc_0.4.38.orig.tar.xz.asc 833 SHA512:5b1a348471fe0854731cc6e26b4e4b31a1f7e325aff85a998d6446f2d77296d1f3bd5d5212690aa8e23591dda2588374b854eaf5037d8d7ba0a9c7a5c2d205a4
'http://security.ubuntu.com/ubuntu/pool/main/o/orc/orc_0.4.38-1ubuntu0.1.debian.tar.xz' orc_0.4.38-1ubuntu0.1.debian.tar.xz 14488 SHA512:d4f8f81b7a0bd71435da74ca83cbc1b32bd1e5a28b13fe591d4d7edec8e0da81a4c34a5e314673692b94cf438fdec8b033b95aa0450a74a7c324316cc4b03ebf
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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `pixman=0.42.2-1build1`

Binary Packages:

- `libpixman-1-0:amd64=0.42.2-1build1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `poppler=24.02.0-1ubuntu9.8`

Binary Packages:

- `libpoppler134:amd64=24.02.0-1ubuntu9.8`

Licenses: (parsed from: `/usr/share/doc/libpoppler134/copyright`)

- `Apache-2.0`
- `GPL-2`
- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris poppler=24.02.0-1ubuntu9.8
'http://security.ubuntu.com/ubuntu/pool/main/p/poppler/poppler_24.02.0-1ubuntu9.8.dsc' poppler_24.02.0-1ubuntu9.8.dsc 3940 SHA512:d0d0bfcb54b77b1de1ef3a91b957e9bafd4a7609df7f96b1d93b1416c3fc12dd3d3c20ca8edb6eaa32fca823e5e482c7a0af923e77ea86775235fdde243603f5
'http://security.ubuntu.com/ubuntu/pool/main/p/poppler/poppler_24.02.0.orig.tar.gz' poppler_24.02.0.orig.tar.gz 1975230 SHA512:75fc41f94ad6848b834eab1cc9199c5ba55b30b12ffbe26d53fa85e86b9918999e752c82d2c5965d6669ace4d9658b1236159c9bfa4bbf40da2660dc00a19f37
'http://security.ubuntu.com/ubuntu/pool/main/p/poppler/poppler_24.02.0-1ubuntu9.8.debian.tar.xz' poppler_24.02.0-1ubuntu9.8.debian.tar.xz 43812 SHA512:0dcb44752aba54269f1215c9a865375a90250143d9500efb21886c3e2b1e8c35d80a0789a3dab407f2b5944b74f7c735475960a8c603789b182bdefcb4f34113
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


### `dpkg` source package: `python3-defaults=3.12.3-0ubuntu2.1`

Binary Packages:

- `libpython3-stdlib:amd64=3.12.3-0ubuntu2.1`
- `python3=3.12.3-0ubuntu2.1`
- `python3-minimal=3.12.3-0ubuntu2.1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris python3-defaults=3.12.3-0ubuntu2.1
'http://security.ubuntu.com/ubuntu/pool/main/p/python3-defaults/python3-defaults_3.12.3-0ubuntu2.1.dsc' python3-defaults_3.12.3-0ubuntu2.1.dsc 3116 SHA512:34bd93d70a55ea6e57e2c8adb7fab3a23507161c2ca61b2c089208cf3706455ef7e072cc04b68af9c1ecb04ed9636e65524501d9e2eb837319f220f275582c4b
'http://security.ubuntu.com/ubuntu/pool/main/p/python3-defaults/python3-defaults_3.12.3-0ubuntu2.1.tar.gz' python3-defaults_3.12.3-0ubuntu2.1.tar.gz 147765 SHA512:9a729a8df22e37d473d39b8c9c95b8c5a7ad8dfd244b3c87576d389f48543edeeaa0bd8b0557de3224d0dbd0f06e02b573cb18adf685a54c02bb485a21ec36e5
```

### `dpkg` source package: `python3.12=3.12.3-1ubuntu0.12`

Binary Packages:

- `libpython3.12-minimal:amd64=3.12.3-1ubuntu0.12`
- `libpython3.12-stdlib:amd64=3.12.3-1ubuntu0.12`
- `libpython3.12t64:amd64=3.12.3-1ubuntu0.12`
- `python3.12=3.12.3-1ubuntu0.12`
- `python3.12-minimal=3.12.3-1ubuntu0.12`

Licenses: (parsed from: `/usr/share/doc/libpython3.12-minimal/copyright`, `/usr/share/doc/libpython3.12-stdlib/copyright`, `/usr/share/doc/libpython3.12t64/copyright`, `/usr/share/doc/python3.12/copyright`, `/usr/share/doc/python3.12-minimal/copyright`)

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
$ apt-get source -qq --print-uris python3.12=3.12.3-1ubuntu0.12
'http://security.ubuntu.com/ubuntu/pool/main/p/python3.12/python3.12_3.12.3-1ubuntu0.12.dsc' python3.12_3.12.3-1ubuntu0.12.dsc 3311 SHA512:8a8634302a6f30b362f63b5c4b5ef128755b290706588b85770c0c9a397210ddbbb1645e045856d1392e7fb69c8824d7e1e7355a5dd83fb6c0e83fd939aea557
'http://security.ubuntu.com/ubuntu/pool/main/p/python3.12/python3.12_3.12.3.orig.tar.xz' python3.12_3.12.3.orig.tar.xz 20625068 SHA512:4a2213b108e7f1f1525baa8348e68b2a2336d925e60d0a59f0225fc470768a2c8031edafc0b8243f94dbae18afda335ee5adf2785328c2218fd64cbb439f13a4
'http://security.ubuntu.com/ubuntu/pool/main/p/python3.12/python3.12_3.12.3-1ubuntu0.12.debian.tar.xz' python3.12_3.12.3-1ubuntu0.12.debian.tar.xz 271148 SHA512:bc1400f4a5bc52d349e5c993ab217a329970f75e0fa068a9e7d71aac0c289bd30091184ffeb4b9d1b5a27e205c3932bf1c36acec4c26649d3b84d52a5e9ef553
```

### `dpkg` source package: `raptor2=2.0.16-3ubuntu0.1`

Binary Packages:

- `libraptor2-0:amd64=2.0.16-3ubuntu0.1`

Licenses: (parsed from: `/usr/share/doc/libraptor2-0/copyright`)

- `Apache-2.0`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris raptor2=2.0.16-3ubuntu0.1
'http://security.ubuntu.com/ubuntu/pool/main/r/raptor2/raptor2_2.0.16-3ubuntu0.1.dsc' raptor2_2.0.16-3ubuntu0.1.dsc 2272 SHA512:50e4b42a3534d19e2acee0e3576ea3a64255e469ba1a017b45e34e4af4d03f1ad20b3f85feca57551d82d896534ec88ac6f3a9a53f0155d56f4e4ff635be493d
'http://security.ubuntu.com/ubuntu/pool/main/r/raptor2/raptor2_2.0.16.orig.tar.gz' raptor2_2.0.16.orig.tar.gz 1750726 SHA512:9bd5cff36390e1e0ef15ac56e5413ecfceb4018cb531a4da8850d3623615f12a93690a78be61f9d9ae7a24e16f6446e356bc2b7f34051ddc077761d85a9b7c44
'http://security.ubuntu.com/ubuntu/pool/main/r/raptor2/raptor2_2.0.16-3ubuntu0.1.debian.tar.xz' raptor2_2.0.16-3ubuntu0.1.debian.tar.xz 14480 SHA512:8d202e53043d45f75a79e34445cd233fd2088ca50d2e5ae59f5b8d841f2aea0b858206faf989ac98ea1b1a78d90f7eb2a0f61013ed08a1195fcfdac027805efa
```

### `dpkg` source package: `rasqal=0.9.33-2.1build1`

Binary Packages:

- `librasqal3t64:amd64=0.9.33-2.1build1`

Licenses: (parsed from: `/usr/share/doc/librasqal3t64/copyright`)

- `Apache-2.0`
- `Apache-2.0+`
- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `public-domain`

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


### `dpkg` source package: `redland=1.0.17-3.1ubuntu3`

Binary Packages:

- `librdf0t64:amd64=1.0.17-3.1ubuntu3`

Licenses: (parsed from: `/usr/share/doc/librdf0t64/copyright`)

- `Apache-2.0`
- `LGPL-2.1`

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

### `dpkg` source package: `suitesparse=1:7.6.1+dfsg-1build1`

Binary Packages:

- `libcolamd3:amd64=1:7.6.1+dfsg-1build1`
- `libsuitesparseconfig7:amd64=1:7.6.1+dfsg-1build1`

Licenses: (parsed from: `/usr/share/doc/libcolamd3/copyright`, `/usr/share/doc/libsuitesparseconfig7/copyright`)

- `Apache-2.0`
- `BSD-2-clause`
- `BSD-3-clause`
- `Expat`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`
- `LGPL-3+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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
'http://security.ubuntu.com/ubuntu/pool/main/t/tiff/tiff_4.5.1%2bgit230720-4ubuntu2.5.dsc' tiff_4.5.1+git230720-4ubuntu2.5.dsc 2309 SHA512:e701ab6ae6250e22c2e49d58a8cf9615ba3034f6c55b2cfe78d64a8fde6c84eccb7cc95a8548be4af7a714c816ebeb5256204ed5dd75218a8e6095e1b3f5ec90
'http://security.ubuntu.com/ubuntu/pool/main/t/tiff/tiff_4.5.1%2bgit230720.orig.tar.xz' tiff_4.5.1+git230720.orig.tar.xz 1781896 SHA512:6bf9653f5c65d17c2944b20d14a5d5ab3b89d461bc6eb935a54aa8df99ce7221aeb2172f06b44affd06d81aeaab5698b90b07fde883167d0abf51debaaa6f71b
'http://security.ubuntu.com/ubuntu/pool/main/t/tiff/tiff_4.5.1%2bgit230720-4ubuntu2.5.debian.tar.xz' tiff_4.5.1+git230720-4ubuntu2.5.debian.tar.xz 33152 SHA512:cb76f5d937dc2bb9f0dd8fe2f99b7c97972068e3f5618976fd759d998009d46998fecc82673452e5cd966c71fe472031023b3ecd8fbd9e61605613f2d827c391
```

### `dpkg` source package: `tzdata=2026a-0ubuntu0.24.04.1`

Binary Packages:

- `tzdata=2026a-0ubuntu0.24.04.1`

Licenses: (parsed from: `/usr/share/doc/tzdata/copyright`)

- `ICU`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris tzdata=2026a-0ubuntu0.24.04.1
'http://security.ubuntu.com/ubuntu/pool/main/t/tzdata/tzdata_2026a-0ubuntu0.24.04.1.dsc' tzdata_2026a-0ubuntu0.24.04.1.dsc 2728 SHA512:a798cda54f303c368e7a8b650bc17589573286744ccd32feb7023c654ee8b656d66038e144bbfc5c489f313d426ab0b10e62f4772b28c9dadcb036f3a3435c34
'http://security.ubuntu.com/ubuntu/pool/main/t/tzdata/tzdata_2026a.orig.tar.gz' tzdata_2026a.orig.tar.gz 471812 SHA512:407e8e93aaa054a22a4a7d6d8cf480a20630073bf1a00956df16b10318f239a12015de38fad3072249193e314d6fddbff4e74afa40a88f7bf5c9eecc7659ea15
'http://security.ubuntu.com/ubuntu/pool/main/t/tzdata/tzdata_2026a.orig.tar.gz.asc' tzdata_2026a.orig.tar.gz.asc 833 SHA512:e84300a1a26c9bcd1f53dc9807794fc3424a362dff7101615592c8f323c4e5ad72be82c4d36220e2666376945f4aaaaa2fbcb87486eda90f23ea1b37e4cf3833
'http://security.ubuntu.com/ubuntu/pool/main/t/tzdata/tzdata_2026a-0ubuntu0.24.04.1.debian.tar.xz' tzdata_2026a-0ubuntu0.24.04.1.debian.tar.xz 188416 SHA512:84d284dba6a64e9b0b3d26f5b74a4ab57907edf0643f7e97393801aff6fa2ae70c1d94493111165c825fff41911f14da58f067c71fb9017e27b2578fad44f089
```

### `dpkg` source package: `ubuntu-keyring=2023.11.28.1`

Binary Packages:

- `ubuntu-keyring=2023.11.28.1`

Licenses: (parsed from: `/usr/share/doc/ubuntu-keyring/copyright`)

- `GPL`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `ucf=3.0043+nmu1`

Binary Packages:

- `ucf=3.0043+nmu1`

Licenses: (parsed from: `/usr/share/doc/ucf/copyright`)

- `GPL-2`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/ucf/3.0043+nmu1/


### `dpkg` source package: `unminimize=0.2.1`

Binary Packages:

- `unminimize=0.2.1`

Licenses: (parsed from: `/usr/share/doc/unminimize/copyright`)

- `GPL-2`
- `GPL-2.0+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `unzip=6.0-28ubuntu4.1`

Binary Packages:

- `unzip=6.0-28ubuntu4.1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris unzip=6.0-28ubuntu4.1
'http://security.ubuntu.com/ubuntu/pool/main/u/unzip/unzip_6.0-28ubuntu4.1.dsc' unzip_6.0-28ubuntu4.1.dsc 1891 SHA512:ff71afdca87465e64b9c58e154fa82ab59da90f416054492902077fa646955ea76d1c9c30558565e3af9c552aee8885de5e749dbff6da676af3013b713d87b26
'http://security.ubuntu.com/ubuntu/pool/main/u/unzip/unzip_6.0.orig.tar.gz' unzip_6.0.orig.tar.gz 1376845 SHA512:0694e403ebc57b37218e00ec1a406cae5cc9c5b52b6798e0d4590840b6cdbf9ddc0d9471f67af783e960f8fa2e620394d51384257dca23d06bcd90224a80ce5d
'http://security.ubuntu.com/ubuntu/pool/main/u/unzip/unzip_6.0-28ubuntu4.1.debian.tar.xz' unzip_6.0-28ubuntu4.1.debian.tar.xz 42948 SHA512:59effec60c41e20fe2f36782a62cf5456dd799b5432b75a4f46b8bcb6ff6d1b32d4ad2139183d99e76de573fb370b0745b97d3f207640a0872a4accfc9f4f3fa
```

### `dpkg` source package: `util-linux=2.39.3-9ubuntu6.5`

Binary Packages:

- `bsdutils=1:2.39.3-9ubuntu6.5`
- `libblkid1:amd64=2.39.3-9ubuntu6.5`
- `libmount1:amd64=2.39.3-9ubuntu6.5`
- `libsmartcols1:amd64=2.39.3-9ubuntu6.5`
- `libuuid1:amd64=2.39.3-9ubuntu6.5`
- `mount=2.39.3-9ubuntu6.5`
- `util-linux=2.39.3-9ubuntu6.5`

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
$ apt-get source -qq --print-uris util-linux=2.39.3-9ubuntu6.5
'http://security.ubuntu.com/ubuntu/pool/main/u/util-linux/util-linux_2.39.3-9ubuntu6.5.dsc' util-linux_2.39.3-9ubuntu6.5.dsc 4726 SHA512:be8fead4961e232992465ff9fce0286fda32445e44d1c9cc6b7b1135c1efea1ac941bb3e497f273e9af9414e299bce942eb677eebff5fc625533f6d02dd1b9cf
'http://security.ubuntu.com/ubuntu/pool/main/u/util-linux/util-linux_2.39.3.orig.tar.xz' util-linux_2.39.3.orig.tar.xz 8526168 SHA512:a2de1672f06ca5d2d431db1265a8499808770c3781019ec4a3a40170df4685826d8e3ca120841dcc5df4681ca8c935a993317bd0dc70465b21bf8e0efef65afa
'http://security.ubuntu.com/ubuntu/pool/main/u/util-linux/util-linux_2.39.3-9ubuntu6.5.debian.tar.xz' util-linux_2.39.3-9ubuntu6.5.debian.tar.xz 148016 SHA512:8c6db47b20b6a9dfe18a37b77308e0f99756f10e837f09cc7afe550b55a43f904fd2d6b5457b4a5519df9ca5422f4df76609e2bece2ffae84c6186cdb0cd4cb5
```

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

### `dpkg` source package: `xmlsec1=1.2.39-5build2`

Binary Packages:

- `libxmlsec1t64:amd64=1.2.39-5build2`
- `libxmlsec1t64-nss:amd64=1.2.39-5build2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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

### `dpkg` source package: `yajl=2.1.0-5build1`

Binary Packages:

- `libyajl2:amd64=2.1.0-5build1`

Licenses: (parsed from: `/usr/share/doc/libyajl2/copyright`)

- `ISC`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `zlib=1:1.3.dfsg-3.1ubuntu2.1`

Binary Packages:

- `zlib1g:amd64=1:1.3.dfsg-3.1ubuntu2.1`

Licenses: (parsed from: `/usr/share/doc/zlib1g/copyright`)

- `Zlib`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

