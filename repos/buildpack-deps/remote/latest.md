## `buildpack-deps:latest`

```console
$ docker pull buildpack-deps@sha256:34bc65ada587328fa2d981afe497617a5502afcd64358e3f24f5b58c77831e52
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:latest` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:66b399a0f86523f2395926abdfe951911afa50511cedc5d1a24f4fbea665e27c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.3 MB (349266350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a847434443a8427f04e1557140428137a084fa9fb1dc789dd063478bf276fc79`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7d98d813d54f6207a57721008a4081378343ad8f1b2db66c121406019171805b`  
		Last Modified: Thu, 17 Oct 2024 00:23:37 GMT  
		Size: 49.6 MB (49555023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da802df85c965baeca9d39869f9e2cbb3dc844d4627f413bfbb2f2c3d6055988`  
		Last Modified: Sat, 19 Oct 2024 00:54:48 GMT  
		Size: 24.1 MB (24051386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aadc5092c3b7a865666b14bef3d4d038282b19b124542f1a158c98ea8c1ed1b`  
		Last Modified: Sat, 19 Oct 2024 02:06:37 GMT  
		Size: 64.4 MB (64389695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad1c7cfc347f5c86fc2678b58f6a8fb6c6003471405760532fc3240b9eb1b343`  
		Last Modified: Sat, 19 Oct 2024 02:53:19 GMT  
		Size: 211.3 MB (211270246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:latest` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b84245017497eea4a96ce15840ff736602594d0e8caacf84ddcf1e6e75c89e45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15508225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ede7bdb92b398bd42c66bb41b29390d617a1b587e4801e9534c3420cf2d7aa33`

```dockerfile
```

-	Layers:
	-	`sha256:f3cba8bcc452cefedc461cca3685c5b6c37d514908d587d0e37481bc48ba50a0`  
		Last Modified: Sat, 19 Oct 2024 02:53:14 GMT  
		Size: 15.5 MB (15497685 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ece5456f1764c52cad682d0bc55c96cd82870bcf728a20da9c6dc65d508322b2`  
		Last Modified: Sat, 19 Oct 2024 02:53:13 GMT  
		Size: 10.5 KB (10540 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:latest` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:25b17e8aa430f3e5bcb80eb5bf8d037ec95ddd242aea4ec0f74d610061282790
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.6 MB (316629383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2c5935b372870d7f04491d61f1993c99057b2ad1f98130fcab6452319533806`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:54:12 GMT
ADD file:f8dacf0eafc6476110951ab49fd75768d4262a1b61984cf9b4625bdd369500eb in / 
# Thu, 17 Oct 2024 00:54:13 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:24:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 01:25:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 01:27:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:638c60a841003707ab5971d86e3c262372536df80608e7e3641e6ad7f5dff43e`  
		Last Modified: Thu, 17 Oct 2024 00:57:04 GMT  
		Size: 47.3 MB (47330521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c114860f8d70d4b0766d6eb509df94ed04b6a417e0ad9060f9a9d43e84064ae`  
		Last Modified: Thu, 17 Oct 2024 01:35:20 GMT  
		Size: 22.7 MB (22729227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1c96b0eadfdfa6388c6308313b6ff3f016dfa452d0521acc1979654342d6abf`  
		Last Modified: Thu, 17 Oct 2024 01:35:42 GMT  
		Size: 62.0 MB (61999097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:614584ff99d2c7b6591b578a66d10c94c81692c6a8c18b8a42671dc8fc7ad543`  
		Last Modified: Thu, 17 Oct 2024 01:36:25 GMT  
		Size: 184.6 MB (184570538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:9220348c2292a5c7836e61e5dcaced1895274a5fc67da8d9873bd3140bf89134
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.0 MB (301972566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9679c7123986773b7fb351e2663141d16472280b9d4938cb89a8abefaa75cf0c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 03:03:11 GMT
ADD file:2ce9af7b514320ba230746cbff4f2f2e2b8d4a62ac035ebbe6575e17544f6416 in / 
# Thu, 17 Oct 2024 03:03:11 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:27:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 03:27:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 03:29:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b683f99b4cdeb3cb4e487b268b3949647168e16d00d07e004e03af92331dbfed`  
		Last Modified: Thu, 17 Oct 2024 03:06:32 GMT  
		Size: 45.1 MB (45147940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3332329de6b42a2c5f534a6f40381b05e4356eb62a42408f66b4d98e78cfee55`  
		Last Modified: Thu, 17 Oct 2024 03:36:59 GMT  
		Size: 22.0 MB (21957453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d531afa8550e37b4fb5ecf878018cd17fb79413ab81359496c3eedd8bb0abca2`  
		Last Modified: Thu, 17 Oct 2024 03:37:18 GMT  
		Size: 59.6 MB (59639477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d133c6fb31d3251e78f2c641f7d145d5f5b2ab13265639c8eb02354c0ffe35d`  
		Last Modified: Thu, 17 Oct 2024 03:37:52 GMT  
		Size: 175.2 MB (175227696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f66285729903294ee7e6397f09e6e57a1c7b845f491a17236f379b66fca60bc5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.2 MB (340197975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eeedd65d53caa810d0605b471c43849f76115ad352b7c098195c75e586fe06e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:11:49 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
# Thu, 17 Oct 2024 01:11:50 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:30:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:30:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:31:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:437f71cf1903685ed3f6314161e121602758f809a760d2bd2293f7cd8ce1abe1`  
		Last Modified: Thu, 17 Oct 2024 04:36:08 GMT  
		Size: 23.6 MB (23594190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:143d0f027108dead9d56047ebcddbf6b5ce9a7d51ab49ac1eeef8590e7bd9764`  
		Last Modified: Thu, 17 Oct 2024 04:36:24 GMT  
		Size: 64.3 MB (64349510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac41aaa9ccd9258f7c6b8f1562698acdae4548533ae639ff6653baa08033c71c`  
		Last Modified: Thu, 17 Oct 2024 04:36:51 GMT  
		Size: 202.7 MB (202669297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; 386

```console
$ docker pull buildpack-deps@sha256:b1c21375b08b4d0f25f20769d2547d2948982c8e2744ea336a64d389f2a87c15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.9 MB (351867123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c98997c4e35d7cb7e3a88082701de0bd4f2daa9ee328f9cdbb34e20318504e1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:e37fc0b0dd2624a94de68cdbe58eebaee18abda02198698500c71668b8266ddd in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5ee14e62c4f0d03b8028e0020d16d7a49ad577754f60410febfbc7c58ae5defb`  
		Last Modified: Thu, 17 Oct 2024 00:42:10 GMT  
		Size: 50.6 MB (50576834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0968576d52726552d23c39a66f1a0ba3f2ca10d188a4fc6750691a97ed494efd`  
		Last Modified: Sat, 19 Oct 2024 00:54:55 GMT  
		Size: 24.9 MB (24894938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:118b4d3aa7d5b42c90f2dcf856bd26bfe40949f5a30646fbc676721418903875`  
		Last Modified: Sat, 19 Oct 2024 02:06:23 GMT  
		Size: 66.2 MB (66208418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d12ebe45cbbff83005bfa62fa86d2064e8ccedae2cd7617a6d60696a420bd1bb`  
		Last Modified: Sat, 19 Oct 2024 02:53:15 GMT  
		Size: 210.2 MB (210186933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:latest` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:34adb642fac5f95817489d8165bf13bf55504c9704e969f5d3c78af5f052ed5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15486776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:784a43af330dd7cc88d66c01cbd66a2333691dd02459d83800710b92e3e526ad`

```dockerfile
```

-	Layers:
	-	`sha256:7c909413102d12d54aa31d8cc5582cbe0762e5a40d49bbf051d2cfced9df8ae8`  
		Last Modified: Sat, 19 Oct 2024 02:53:11 GMT  
		Size: 15.5 MB (15476264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:854336bbcc82191d23e44fbe1fb86eed9659b15b27f56cc7343ed66df224eff6`  
		Last Modified: Sat, 19 Oct 2024 02:53:10 GMT  
		Size: 10.5 KB (10512 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:latest` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:eedf47cd0217818cf4687c2bed18ecec128b16af82475584ebbeabff390e5f70
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.3 MB (326348772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d71650f7afcc0ee2ce3640621c54788a7d5851b59ef46e25c54141eb87a7ea58`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:08:45 GMT
ADD file:5fa3d47e52ee376ed002c84d34e93fe11e6db2308915238c5d7a9a5840814eda in / 
# Thu, 17 Oct 2024 01:08:52 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:41:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 01:43:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 01:48:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7bf8417b2ab139177317d556c6249cee54f60148ccee016ec60d45a13a21c7c2`  
		Last Modified: Thu, 17 Oct 2024 01:17:24 GMT  
		Size: 49.6 MB (49561619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bb4cb3753c5260533ae9297767f8b73bc0cd6f1dc878635a173148920d80368`  
		Last Modified: Thu, 17 Oct 2024 02:08:35 GMT  
		Size: 23.6 MB (23647379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e244535d91d08a7c42eab7cd45ea82c43428356bc75a90c8d486507e9888f0a`  
		Last Modified: Thu, 17 Oct 2024 02:09:28 GMT  
		Size: 63.3 MB (63297195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ca8f8a184e3174b4b3b76091c95baf89a636e164f9c732b010464037c162209`  
		Last Modified: Thu, 17 Oct 2024 02:11:35 GMT  
		Size: 189.8 MB (189842579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:bafc61e1014935dde758d5d8c2f2cf3614486ab7024e8c1dd51e5eca3d9a1e60
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.4 MB (363396234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cfa68f72feb2ed3326c5b70c46fc86e32731822125a51dc10faaca60d96896e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:18:38 GMT
ADD file:c7ce4329d7c0cdfb8efa822e20a44ab1922fe70e4e8be36a317ec45c565a260b in / 
# Thu, 17 Oct 2024 01:18:40 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:42:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 01:43:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 01:44:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bbeb3fa4a5ad17047af70a984a8c9e89b0702821c59cb2290ff6c49eec8d704f`  
		Last Modified: Thu, 17 Oct 2024 01:21:33 GMT  
		Size: 53.6 MB (53555597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a4688a74de76e26de6977ef8438b7e0161edaee4d986ee61e62bc0b84b1163`  
		Last Modified: Thu, 17 Oct 2024 01:51:23 GMT  
		Size: 25.7 MB (25709972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f8022c20c080be7d80dd6512a4c9fed59039e755de95495c76a32f7c2baebf1`  
		Last Modified: Thu, 17 Oct 2024 01:51:43 GMT  
		Size: 69.8 MB (69829835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d27751f2c723de9cfb2cbb2775f1c16c1f3653cdff74eae652ff9cc1633eda6`  
		Last Modified: Thu, 17 Oct 2024 01:52:21 GMT  
		Size: 214.3 MB (214300830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:22357b5316cabb794fe07c11c4af17599270f951b8c9e21430952eb1f022716b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.8 MB (318793259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dc6716f9f26b5e12b4faf3947ea48f9b157956dc7cab733983b5e315635eac4`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:45:59 GMT
ADD file:be1cd8a5c7d60ebbe308ecf258da8f3d2dd59f7c877549c96e98e31165ba1eaf in / 
# Thu, 17 Oct 2024 01:46:00 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:40:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 03:40:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 03:42:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:510daf83b7a2b266658f37f8849eeeba99ab0f02d08ef5c1ea7f613451a81239`  
		Last Modified: Thu, 17 Oct 2024 01:50:15 GMT  
		Size: 47.9 MB (47938447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba66dca1247069bbe2e2adfc1cbc055a99250a0e8c3ec2bfbbb419a1f58e5bb5`  
		Last Modified: Thu, 17 Oct 2024 03:48:39 GMT  
		Size: 24.1 MB (24051978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d236e9b4fd4c23047a10cb64d0cfc027a005094af65d82f927b8a39dfe85c14f`  
		Last Modified: Thu, 17 Oct 2024 03:48:53 GMT  
		Size: 63.5 MB (63494989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77632955ee6981fa7ca39f104872912fb4579734ee466c2eb2d442ca4c8a29cd`  
		Last Modified: Thu, 17 Oct 2024 03:49:21 GMT  
		Size: 183.3 MB (183307845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
