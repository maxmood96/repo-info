## `buildpack-deps:sid`

```console
$ docker pull buildpack-deps@sha256:db85b8b807d11824f78d654a19542ab5ab3ee6427e877bad0c7d5b040800998f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 9
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:sid` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:d9fe0a0c36aff57611857ace9480a29ef5822730c0b938d025e0430a3cfc3cf3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.5 MB (400504739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79b01561b05ecba694439bf81795ba572a401858a3821337e62efea80edd5660`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:52:30 GMT
ADD file:7fec587617b78a81cacf7bfcdeac3b9e90b4135c4c242e80b5ea34f57d221168 in / 
# Wed, 10 Apr 2024 01:52:31 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 05:29:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 10 Apr 2024 05:30:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 10 Apr 2024 05:31:38 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:9c331a6d36afda0d91938277ed86b71e85bfb5904bb0efa434e13d0991817c34`  
		Last Modified: Wed, 10 Apr 2024 01:58:18 GMT  
		Size: 51.7 MB (51735884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dbc54dabf654d02139eee6023952ef9722f71eccc8835cd61dd4f574adcea59`  
		Last Modified: Wed, 10 Apr 2024 05:37:54 GMT  
		Size: 25.2 MB (25233975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3f084187fa2b14471c0826c24248ca716aaf99049ade3cc30674118bd1a7fd2`  
		Last Modified: Wed, 10 Apr 2024 05:38:11 GMT  
		Size: 68.5 MB (68535606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41470ed1825af4266d2101a16eb992f7f20951bd495af52d0d0cf5d496d1680e`  
		Last Modified: Wed, 10 Apr 2024 05:38:52 GMT  
		Size: 255.0 MB (254999274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:48fb4f0ca521b5a52c782f780e15840c8f4ad02e69a4e7c5ee1a5f739d2ea391
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.0 MB (360956786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f248e4a461676a68a8adffe7498c8578602961e0b730820838d17c6ad823d3fc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:50:32 GMT
ADD file:4a9afbefe640815ceed7c04b5539d7c65f79afb1c50420641fb90ea84d9456ee in / 
# Wed, 10 Apr 2024 00:50:33 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:47:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 10 Apr 2024 04:48:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 10 Apr 2024 04:51:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:435c81b262aa45b615a98b5b08f6124900f0a2f8c1b016424864ba2f1ed5bea0`  
		Last Modified: Wed, 10 Apr 2024 00:56:32 GMT  
		Size: 48.9 MB (48901894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1396417efc6e373a240285f028c909e31f5fb9efd13378c97dd450e23ed90a97`  
		Last Modified: Wed, 10 Apr 2024 04:57:34 GMT  
		Size: 24.0 MB (24026275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76004e4bc491beba63b8855446407f9a2d7d9e8296c8b5bc053170acc6c366d3`  
		Last Modified: Wed, 10 Apr 2024 04:57:55 GMT  
		Size: 66.2 MB (66197915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77e1b193533db9a069e7ae250e0775cf84487ec8262bcbb88a77329463085787`  
		Last Modified: Wed, 10 Apr 2024 04:58:37 GMT  
		Size: 221.8 MB (221830702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:2db99d690a40309169f5192ef966e1252739965770565e85ba476c39c4785739
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.3 MB (343337806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cacdc9b800b1dd1edc3404f1d2528e77096deae614c6d2153164f3f6cd64155d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:00:33 GMT
ADD file:b651a9e79740799ad0cf7f17474e58eefdc73e4611a56f8f166422f38c62fa53 in / 
# Wed, 10 Apr 2024 01:00:34 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:51:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 10 Apr 2024 06:51:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 10 Apr 2024 06:54:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:3bb537406eccf44a062d659169f21696e8c3000511c07deaf7acadb77364db29`  
		Last Modified: Wed, 10 Apr 2024 01:07:36 GMT  
		Size: 46.5 MB (46488213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa8bb32b6a8fa1654a8654ec8498eee6b8f5a14412626a85c0b6aa2517664a5`  
		Last Modified: Wed, 10 Apr 2024 07:03:37 GMT  
		Size: 23.3 MB (23259258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1684840457534f3c616560bbb71c0c6d2ccd3a666f6246ee27b8175ce907e517`  
		Last Modified: Wed, 10 Apr 2024 07:04:01 GMT  
		Size: 63.4 MB (63446378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e912ca74bbc3601ae2d9a866d63e95f7ac9dfcd072b04f9891215dc8f6e0b47c`  
		Last Modified: Wed, 10 Apr 2024 07:04:47 GMT  
		Size: 210.1 MB (210143957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:2210f307f8743f3ff1afcc23c9c646c581c66a65c9460a15f0a842b6cbc88769
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.3 MB (392324183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb6cf9cc1a2347a5b5de6e5aef9270141af95fb1d8d41cffc39b1a6adb365828`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:41:31 GMT
ADD file:69ea41e74fa7a7601d1adbbdf992359f0c16c551447466cb4aaeac1914dc2377 in / 
# Wed, 10 Apr 2024 00:41:32 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:26:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 10 Apr 2024 04:27:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 10 Apr 2024 04:28:47 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:de2b6ae488daf95901751cee985416dfee51a36f7f9f15e60031279618e00a20`  
		Last Modified: Wed, 10 Apr 2024 00:46:49 GMT  
		Size: 52.1 MB (52136998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5adedb09bcdae19c9c078aeaa62769929c3099af358e94efbac1473c079342b`  
		Last Modified: Wed, 10 Apr 2024 04:34:38 GMT  
		Size: 24.9 MB (24946126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:324a0d5b61d3a348879655c04f5c1126df0827ea0ca894a127660c330ef8602e`  
		Last Modified: Wed, 10 Apr 2024 04:34:54 GMT  
		Size: 68.7 MB (68702497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c64f3917d1c535fa410055152988df006865c9d281e95cc51412df61ddd63191`  
		Last Modified: Wed, 10 Apr 2024 04:35:26 GMT  
		Size: 246.5 MB (246538562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; 386

```console
$ docker pull buildpack-deps@sha256:67b9e36a91a76a258c3ecff6608d184272d713ac485aefc3e62332356bb0415c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.4 MB (400410824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9a1b8c1af15ca4335608a09301770f919fda12c9c0dabf44cc9e38c75457165`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:58:52 GMT
ADD file:e239896f7b5e011b6d0233f2b19722dd4ed9b477a41df953ada860d9292309a9 in / 
# Wed, 10 Apr 2024 00:58:53 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:59:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 10 Apr 2024 07:59:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 10 Apr 2024 08:01:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:aa1551ec75fa2e9c2e1970c5f0cf8c95e50b19638484e38cd439a1ae005100e7`  
		Last Modified: Wed, 10 Apr 2024 01:05:22 GMT  
		Size: 52.5 MB (52545296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d841d60f045a27d1521cf79ab6870b8315e8707b3fac64ae28185661bb2e97`  
		Last Modified: Wed, 10 Apr 2024 08:09:44 GMT  
		Size: 26.4 MB (26417056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ace810379e6d02a7cff3acb3d737b0fb1ee42e17edb6ab66e145774b40e0a35e`  
		Last Modified: Wed, 10 Apr 2024 08:10:08 GMT  
		Size: 70.4 MB (70433398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d4952c4b57fd74f15ecc90800c03d9e1bcd7942c069cb185de9343d3d13fe83`  
		Last Modified: Wed, 10 Apr 2024 08:11:06 GMT  
		Size: 251.0 MB (251015074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:b5224f59c01c64b248e9f48214432ae69669ab3e3bbe2f36a4412b60b58e4fdf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.5 MB (357495125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3615639b43b8508a560b974f0f2c8153011ac54069af729c882ebd1149beda34`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:54:42 GMT
ADD file:3fab027e6d739287e4b7349292c885c809a65c14845b5d292aebb3844ce27682 in / 
# Sat, 30 Mar 2024 20:54:48 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:27:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:29:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:35:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:cbe55b4cce02b94dd21e3b65d94bdb65a4b1119288ec18dec4cbfe762dc19adc`  
		Last Modified: Sat, 30 Mar 2024 21:01:00 GMT  
		Size: 50.6 MB (50600834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:195f963513fde292fd81669591d3906b0da2c957d9712fccfa5e3456c15942a0`  
		Last Modified: Sat, 30 Mar 2024 21:46:20 GMT  
		Size: 25.6 MB (25551593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70614ded1d05fb936c73b08a0c6dfe5d84789dc9d8bd520b58fc90ed5d9fc8a2`  
		Last Modified: Sat, 30 Mar 2024 21:47:10 GMT  
		Size: 65.2 MB (65151931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cec5d517bc6924cab27f5df1f01979046acdf9cdb844cd5281549ae70cffd261`  
		Last Modified: Sat, 30 Mar 2024 21:49:28 GMT  
		Size: 216.2 MB (216190767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:1d6ceba1d92b87bac5cb0eae4ce2ca18b313210b19fa1b8a1048e045383c6ce5
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.7 MB (415726511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05e1faa962365948f3a0e708c24ad4712aa140984ccaddc6127d655644bc18c5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:27:40 GMT
ADD file:b4d76c20a1ef31eb6916914baa486e040481cfc4a1f2464b19f7a54de07a7414 in / 
# Wed, 10 Apr 2024 01:27:43 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:46:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 10 Apr 2024 06:49:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 10 Apr 2024 07:01:50 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:149ef7b943fcf6c968df7da67a0cab193a9c8b879654558231f5a04b02ace929`  
		Last Modified: Wed, 10 Apr 2024 01:33:03 GMT  
		Size: 55.6 MB (55558752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23863b8ea71766628fe06ba3262e6ca0ca1b9427125763d73844952a82e439f7`  
		Last Modified: Wed, 10 Apr 2024 07:18:52 GMT  
		Size: 27.5 MB (27489062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0af6beb4c1564ee27dcd22b51d140012207437010746dbe861c9858b7791414`  
		Last Modified: Wed, 10 Apr 2024 07:19:13 GMT  
		Size: 74.2 MB (74243321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba5c25e977a23b5331edef4495b945d4ecc98790d53cc7b9ef2cb27a3c17b5bf`  
		Last Modified: Wed, 10 Apr 2024 07:20:01 GMT  
		Size: 258.4 MB (258435376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:1c9ddd9530a45d20762adb57ec2e4a54811657e63ea191369953df8b7928cf0d
```

-	Docker Version: 20.10.27
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.5 MB (428490682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d07901e48486434c12164a569efa963478849a6a283fe7cd212d8ec5c0b457a6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:08:58 GMT
ADD file:cf8b9266fc4180144feb816ff584ba8b6b03b244743764b117ff119f451aa497 in / 
# Wed, 10 Apr 2024 01:09:00 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 01:30:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 10 Apr 2024 01:32:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 10 Apr 2024 01:39:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c8bfd6a26c3a37b6a00ea3d238fb8eed745384d2bb98efaff22428174a68f6a1`  
		Last Modified: Wed, 10 Apr 2024 01:11:44 GMT  
		Size: 49.9 MB (49941022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a180df00bec725b09dac77cce3dc37d1d711ae817d8b4a36f2aa34d8d552ed`  
		Last Modified: Wed, 10 Apr 2024 01:39:42 GMT  
		Size: 24.9 MB (24904024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3ce99732b9cfa4521c0ab9070c5af6f235f8b3d7977ca84c4ec174dba2588aa`  
		Last Modified: Wed, 10 Apr 2024 01:40:47 GMT  
		Size: 68.0 MB (67976903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee47bc0f29c27ad588a2d49b024ed8a5415e1d7952943fa241190b9956657a2f`  
		Last Modified: Wed, 10 Apr 2024 01:45:48 GMT  
		Size: 285.7 MB (285668733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:0ab6408fe953fdba844e9f28fd84bad27343128fb92877616a42193aafd19704
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.1 MB (381093694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8359b9cab637f4730f0db133d0ab75b74fd74d0505850adb8e7d413822d008f0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:25:52 GMT
ADD file:90e106baf8019819d61f3875a3695b4ee1f0f47f890bc23db62485c13c0badfd in / 
# Wed, 10 Apr 2024 01:25:56 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 10 Apr 2024 07:01:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 10 Apr 2024 07:04:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:111a73d2cd21eab548d0ffddc9bb5a4d0a8616f2cef311480858e7b83b040f90`  
		Last Modified: Wed, 10 Apr 2024 01:49:40 GMT  
		Size: 51.1 MB (51141422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:417ceb5aa4e39ffe287fe10a3493d2f4d5523e68aa7a2824b810a3822bd3b198`  
		Last Modified: Wed, 10 Apr 2024 07:32:48 GMT  
		Size: 26.4 MB (26424048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7b51be5a8b279e9d858406806bb10f22ba19f1e529f4b8e300e3603f1323af1`  
		Last Modified: Wed, 10 Apr 2024 07:33:05 GMT  
		Size: 70.0 MB (70003319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b5312a2171b681d2ec26af9760d85151a2bb53ce93c99c1d00c7d23afef205`  
		Last Modified: Wed, 10 Apr 2024 07:33:41 GMT  
		Size: 233.5 MB (233524905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
