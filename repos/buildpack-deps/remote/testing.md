## `buildpack-deps:testing`

```console
$ docker pull buildpack-deps@sha256:1f8503d74a131d54c69b0d4cbc5e586459d017852e1d3db53b4256b1d6ab6f52
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:testing` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:eee9989bd699f66555dbf7dea533308af6f4886770d925fc2d73fe49143f4dd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.0 MB (391006302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65c0136ea1726181d106eac30bf3eea4d99c807380bd415eeac65744eec87f73`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1742169600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b312498eaedc471a9ee574437ddcf442ef14eadb9305c2ea1c843f2af922d473`  
		Last Modified: Mon, 17 Mar 2025 22:17:43 GMT  
		Size: 47.5 MB (47513473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307579de8afb457f38a2a818765fbf595dc7bca2e9022efb29cd9a1e5c6b6b9d`  
		Last Modified: Mon, 17 Mar 2025 23:14:00 GMT  
		Size: 26.2 MB (26230971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac8328f6595bc164f14568dbbd4ea22c25dd2666776b4b2c83c26194060e04be`  
		Last Modified: Tue, 18 Mar 2025 00:18:59 GMT  
		Size: 67.1 MB (67082633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39bf774555cfd226d5741c9cd16058cfeaed185e282618df682e0c3ec93dc15d`  
		Last Modified: Tue, 18 Mar 2025 01:13:48 GMT  
		Size: 250.2 MB (250179225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fd7c9cb8560a06fecb519728e3aa322ef4ce35ed522a6d3393477d04de6aec73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16857656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30818b762e79eddcfc19a26f7cf091838f72f2463b2bfba56a954510189d647d`

```dockerfile
```

-	Layers:
	-	`sha256:65c62650abd2f4e8b479599878317a30babb1004c3aea513b4bc6b36227480c0`  
		Last Modified: Tue, 18 Mar 2025 01:13:45 GMT  
		Size: 16.8 MB (16847463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78d76932b6ef3f6457ca7d29777eb91baffb0f7926797fa454abf6eee33045ae`  
		Last Modified: Tue, 18 Mar 2025 01:13:44 GMT  
		Size: 10.2 KB (10193 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:62f4ed8859f74593c2598cb5eed3fc0cd8aa72da0decf4d0955a9bd689d11867
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.9 MB (354855768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d0f1d470dabb961ab3be75325fe59c65dd8956b16c7ec53758404077d6d25dd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1742169600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:43d6e898d3a5beca16572b1a502b9433116891c583ecdbd0b66dccfd8af9e4fe`  
		Last Modified: Mon, 17 Mar 2025 22:21:05 GMT  
		Size: 45.7 MB (45737144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:023a0e893b154d7d5e322d742da1db8537753d0cf777b8cb73ca869670a0c807`  
		Last Modified: Tue, 18 Mar 2025 03:08:29 GMT  
		Size: 25.0 MB (24957496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86725112f5149cb61d854be49fdee119e7f61817be65303ade6d8bf0230a955`  
		Last Modified: Tue, 18 Mar 2025 05:18:53 GMT  
		Size: 64.8 MB (64765151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bcb91fae58b88ab15ec7eb1f6d2556f75c522489cd5f3e67ebfd4f77bf37b15`  
		Last Modified: Tue, 18 Mar 2025 07:49:51 GMT  
		Size: 219.4 MB (219395977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:69c1cf90b09348bc84d410e7a4349ef7163aaea8d2eae347e433ac9d4d249e9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16627740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb51bb9bef7ad012118a6bc655f203bdca1c4db54455aa0c1b51c44c1b561e20`

```dockerfile
```

-	Layers:
	-	`sha256:f1414f287c46637f387cdfeff64c89bcddf22bc691d326dce9d76543175fde94`  
		Last Modified: Tue, 18 Mar 2025 07:49:46 GMT  
		Size: 16.6 MB (16617487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4d384facb581646127c4149eede13b21772556c46072588d83605971e8cc55d`  
		Last Modified: Tue, 18 Mar 2025 07:49:45 GMT  
		Size: 10.3 KB (10253 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:9ada2df8c3939512b10d6bd71892396cfb7c485e9b613adf39b2fc0c65441398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.9 MB (325869960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8153257ba93e5a2a984f84fec6f2e9b094ada55e90db75605cb14aee20ba03cf`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1740355200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1268bec7b6bf92bd5fc4d4120fd51b9bde5a9c50d4b8a8decb59fbe4a53da6fb`  
		Last Modified: Tue, 25 Feb 2025 01:33:55 GMT  
		Size: 43.9 MB (43903193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe307003fac8d59260832b7e5476d782c0d94c51fc746df3d40b574a8cd73406`  
		Last Modified: Tue, 25 Feb 2025 07:18:31 GMT  
		Size: 25.3 MB (25278377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd6bd387fa259196771b277c7da226c32cee7039e9a1a5ee0456db83179c99f`  
		Last Modified: Tue, 25 Feb 2025 14:21:40 GMT  
		Size: 62.6 MB (62619925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba8d19cc4db2d31e2d8fef2869149912a0309eac662df4d539e320ad6ec0ee0`  
		Last Modified: Tue, 25 Feb 2025 16:59:22 GMT  
		Size: 194.1 MB (194068465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2a1aca6411f4d54c9a560c44866e4b4ce386f72fc4186e743e02dd6d78ad3301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16634678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e150576448e4e57c42ef98f05dc1ef74a45fe597b45a57a84c5a596ada4b22d1`

```dockerfile
```

-	Layers:
	-	`sha256:5b344b573f07e38933e409305a19f487887508c865ac7cb96d98eafa72514e82`  
		Last Modified: Tue, 25 Feb 2025 16:59:18 GMT  
		Size: 16.6 MB (16624426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6eada467ba8444dcc52b9391da7c382f4ac6df67e8417d64e198404b24ff269`  
		Last Modified: Tue, 25 Feb 2025 16:59:17 GMT  
		Size: 10.3 KB (10252 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f4e980f09d897376a0a5d5fd4af883334dca4fef4eabfccb3211751f246aa1e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.1 MB (381086194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dfc0b529ca4d96e75b234c54952b78954b2e83da03312643666817df4f00375`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1742169600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f094fa2db11dac08419411aeaf2d9c561365872610ec591de05f23f2fadff3bd`  
		Last Modified: Mon, 17 Mar 2025 22:19:09 GMT  
		Size: 47.9 MB (47886359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a84822f7d47020ba3b073f3f8ebb18e27a90b8e25a519c2b492131234a060ca6`  
		Last Modified: Tue, 18 Mar 2025 04:59:07 GMT  
		Size: 25.7 MB (25690430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcae46c8b749bfef6c1f2eaab2853deec3a02eb1815b00768b45dd741aa09214`  
		Last Modified: Tue, 18 Mar 2025 13:19:59 GMT  
		Size: 67.1 MB (67130545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93125d8cac1d8e5c7abb72bf5a7b7da662240c4c79d866d42fc2c723652ecb94`  
		Last Modified: Tue, 18 Mar 2025 14:41:44 GMT  
		Size: 240.4 MB (240378860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:198c4c1f1926d7edb81ec4c6d692f51532bce6bfd27f308a40d786bb97288afc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16942603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beb13d1a762bdaaf453a6edf58da962b5ba01cbf687b1dd8658b6596489139cb`

```dockerfile
```

-	Layers:
	-	`sha256:29fffe57dd60e26e6b68a6e4708d983bf8e0368989b8e3f8d5c5578ff215ad27`  
		Last Modified: Tue, 18 Mar 2025 14:41:39 GMT  
		Size: 16.9 MB (16932330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d121131108e502b8d85aa2964409f96f7fe652210bdd0eec9b6014a890db363`  
		Last Modified: Tue, 18 Mar 2025 14:41:38 GMT  
		Size: 10.3 KB (10273 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; 386

```console
$ docker pull buildpack-deps@sha256:2b9731f9af5989632e105629d24520b5db434c3b78c076df7ac084ad239e9d41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **399.8 MB (399807316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca0dfd93a73cc28816f2867a541be08d9aa751e919c87398e1f7e380ed3e8bc0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1742169600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7f35c21acae2ef6b77873a46c174f1da0b28fbc4ea787b7f5bb3bd79c145883f`  
		Last Modified: Mon, 17 Mar 2025 22:18:02 GMT  
		Size: 48.8 MB (48831362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2417ac61f214f6f239ee6ce6ccf4e9a29aead09dd8338aeca7ca8645adc7a0d3`  
		Last Modified: Mon, 17 Mar 2025 23:33:10 GMT  
		Size: 27.4 MB (27380417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825d4e842f60fe8bed8af22c7d26bd8c640142408d7c59da73f8a94bc3c79992`  
		Last Modified: Tue, 18 Mar 2025 00:19:28 GMT  
		Size: 69.1 MB (69050838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027c2be09dff5ed0645f6f8de11f5266ab76f77212ad7becbaf1701c02253ebe`  
		Last Modified: Tue, 18 Mar 2025 01:13:59 GMT  
		Size: 254.5 MB (254544699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9c3ca1ab015784394499d22c39701bc81519a10b4382f7da01f5c14a5a92452e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16827138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e63ed1f1ee0e0e21b5b0384d2e899b3f3b3f9450a592cf4d4207aa9a2647eb4f`

```dockerfile
```

-	Layers:
	-	`sha256:0c7590f6fb004d2a6cdbe4bd75883a81d994fda67edfca69dbc8d3c79264e571`  
		Last Modified: Tue, 18 Mar 2025 01:13:53 GMT  
		Size: 16.8 MB (16816967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cc66e97bbf537eed3149055021f8f5973da078e0edf87e21b4320aaacf0af52`  
		Last Modified: Tue, 18 Mar 2025 01:13:53 GMT  
		Size: 10.2 KB (10171 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:e658111f15ac1135dcc04f2146098d782fb66337c60dcb5844a94acbf730ce72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.0 MB (360960727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8530617c4a7c4e0a4f7d86ea5da8cea3bf9749c2c3389a05104dffbb93fa6a38`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'mips64el' out/ 'trixie' '@1740355200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b3018c8b96b9ba22f17940c42dddfbfef3058b787c07b7ccd94c52adb65aa552`  
		Last Modified: Tue, 25 Feb 2025 01:33:17 GMT  
		Size: 47.7 MB (47684440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d568a834d28f352d6c862c921a5a1525795a3ba966e684f287dc047fc5a62e6a`  
		Last Modified: Tue, 25 Feb 2025 20:40:18 GMT  
		Size: 27.5 MB (27466813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e30dd389c4f7f75e0238dc8b5aaa6b88b1024d42ca2aa910e605d4197c6c892`  
		Last Modified: Wed, 26 Feb 2025 02:28:14 GMT  
		Size: 66.7 MB (66667275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c956d55981ae0096e143abf54b4ef68b7f7cf55b6a0a6136a3db47638e19aea`  
		Last Modified: Wed, 26 Feb 2025 05:03:57 GMT  
		Size: 219.1 MB (219142199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:aaefe769cae43377a3074cff71943ebef3d519a5ba16844e550a3a86dfdb7b76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 KB (10026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3768c5fb46e71af9477fc192f0ce76f96c4b980f374563341a8fbecbb0716c6`

```dockerfile
```

-	Layers:
	-	`sha256:f02c4680b0573bb3a5b6b6c21f517839d1e882e3036acda9000a11b3957a2d13`  
		Last Modified: Wed, 26 Feb 2025 05:03:36 GMT  
		Size: 10.0 KB (10026 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:993ec975a109f3c7be9e15a87f733689f6721706ba61cc766bf3781609e8ee5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.2 MB (397237514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5113331d563073d42f994aa99c913cdac631ad36ebf83bda2e1997e61a8b7f3f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1742169600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:895a5f19953067f7b5f8d8697fd370f37def792e6b968ea95a15dd11594bc1a6`  
		Last Modified: Mon, 17 Mar 2025 22:20:07 GMT  
		Size: 51.2 MB (51162729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aeaa0f265ddf4206f6d845d5494e3733ac72919e3d0329859f2ce1f44f19c11`  
		Last Modified: Mon, 17 Mar 2025 23:57:42 GMT  
		Size: 27.8 MB (27773366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f105bd00bb4fe66e0c28648fd8c55c5c78baf7508cbe6b000b0ec61ceebf10`  
		Last Modified: Tue, 18 Mar 2025 07:15:25 GMT  
		Size: 72.4 MB (72444096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a07cc02047648edde215f40ec250120d1433488e72d57feec3961ebf2d69ff9`  
		Last Modified: Tue, 18 Mar 2025 13:59:36 GMT  
		Size: 245.9 MB (245857323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:00fd825a9319edd4a142fa16b216d3eaa6ff350ef78ef7c12f3f62b7fedaf12f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16849071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9644987a568c1ac9e3992ef79186bcf789fe2dec5e482ec298f15fe04f6d263`

```dockerfile
```

-	Layers:
	-	`sha256:7898ead0467b4f1c77b11a027da5f91fd9b76185f69d857fe89072c480640953`  
		Last Modified: Tue, 18 Mar 2025 13:59:23 GMT  
		Size: 16.8 MB (16838846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:209f01a6348252a5049893c867d38c99b0a979258304618df2b382a8eb634395`  
		Last Modified: Tue, 18 Mar 2025 13:59:22 GMT  
		Size: 10.2 KB (10225 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:38eb0c50dbb46ac02d82917b8a6f738b4290af6090318a393f581c6e917094db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.0 MB (363999107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18f3cfb7a8578e4dd14f259392f5a37657235dbd750ad501a1bef2274bdf50ad`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1742169600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2d25d70cc33acfbb261e54e41a50ee310f48343b555ff5a724ee79cad7214fbf`  
		Last Modified: Mon, 17 Mar 2025 22:51:24 GMT  
		Size: 47.5 MB (47548830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b74e201480524a9e7f1671230b2cae3b456d6d6a91a8a4a2b07140f308c08518`  
		Last Modified: Tue, 18 Mar 2025 02:48:54 GMT  
		Size: 27.4 MB (27392489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe56110fe210f7a220bd33778fbc68a1d3b26729f0b2ea2d7d03b68e494f18f4`  
		Last Modified: Tue, 18 Mar 2025 05:57:55 GMT  
		Size: 68.1 MB (68123437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd8b3af6b24d8432ec9aae2bd7e9960e1b60e218148a064934b4b04013ac747`  
		Last Modified: Tue, 18 Mar 2025 09:31:15 GMT  
		Size: 220.9 MB (220934351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b802ca56533c24e3881b900584b15f35d29e4cc92afa86153808612f7bb4cb12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16642720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e7c86e6c699a8231da500f81de12e53ca8d8b91fd57408af020e234c21317b3`

```dockerfile
```

-	Layers:
	-	`sha256:83e8d45bf449f2d1dc038e07b8870e8e82786cf8f0af6f7e112258fd7098f74b`  
		Last Modified: Tue, 18 Mar 2025 09:31:12 GMT  
		Size: 16.6 MB (16632528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0305de3b679c464394923e2421f8f14c3bd20b4807d3818b988b43cc2bed0e5`  
		Last Modified: Tue, 18 Mar 2025 09:31:11 GMT  
		Size: 10.2 KB (10192 bytes)  
		MIME: application/vnd.in-toto+json
