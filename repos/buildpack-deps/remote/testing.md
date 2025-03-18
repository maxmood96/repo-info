## `buildpack-deps:testing`

```console
$ docker pull buildpack-deps@sha256:ef5466e2567ef036e76f3c674156a4d419b3563f7e6452a63c0ef2814120edb0
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
$ docker pull buildpack-deps@sha256:865defa61fa2613cad8601f5ebc893b90b78a38724958affca0e63b9f36d2d27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.7 MB (343745859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7613d03b19fbd40cb9de166ab5dbd953b4dd9c485c07786565216c98e99ecfa8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1740355200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:131ae520a4eaed5ef3f8bfb62695032fc5b0cf09159cb958245abf1bbddef3b8`  
		Last Modified: Tue, 25 Feb 2025 01:33:17 GMT  
		Size: 45.7 MB (45706841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2cfbb99d11f866136a1de25d46d555105f60a1f7b061aaf7d89155339ee129`  
		Last Modified: Tue, 25 Feb 2025 05:17:32 GMT  
		Size: 26.1 MB (26127258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eb7a39b0019bff7c7c84e047f3e1f583a04358b1f598c468c944216bf4311bf`  
		Last Modified: Tue, 25 Feb 2025 08:39:03 GMT  
		Size: 65.1 MB (65143611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60237d957f53ae60bd3916e6ad8c4604caad9c2bbf8d78ff4906450ef90d1d38`  
		Last Modified: Tue, 25 Feb 2025 10:18:55 GMT  
		Size: 206.8 MB (206768149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:25b4c5c1a4b9fa437d095141481a063242750032f39203252fcc4bfcd27e231f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16635094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65cc527e83936bef6f826ff3f72926a4a4e2e3d5feae5fa2fe352126f230130d`

```dockerfile
```

-	Layers:
	-	`sha256:e162587b3cf78d66751cf23cd7cd16414e67c9bc5eec90f74853f6a080a9f61e`  
		Last Modified: Tue, 25 Feb 2025 10:18:49 GMT  
		Size: 16.6 MB (16624841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c462b668af31d9a76c9146a96545d7324c03341bb37af1ddb852aa65529cef6`  
		Last Modified: Tue, 25 Feb 2025 10:18:48 GMT  
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
$ docker pull buildpack-deps@sha256:f57638717f702c4e105d2be75b4b715a0dce665ed0e64ac5c27b9654c28bde9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.0 MB (370023112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d05f7f77a11a4c564f62c6ad2d128d5f3c4abfc2d9b8c85058554595e4aefe6e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1740355200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4febb367456c7cd84b8043b3b3b3c93073aa9439fb54961fd46a9370758fe523`  
		Last Modified: Tue, 25 Feb 2025 01:33:49 GMT  
		Size: 47.9 MB (47858532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f249b42e8ca4f2ab0a926162c24ad19731e17ebec889633ecab6f0a37257460`  
		Last Modified: Tue, 25 Feb 2025 05:43:15 GMT  
		Size: 26.9 MB (26882202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99f03309824abf50aa8e904201f7f1a31ce290f54469b02ae3362c1a5c1d7b23`  
		Last Modified: Tue, 25 Feb 2025 11:56:14 GMT  
		Size: 67.5 MB (67528189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f22f1af1af1dd3b83b9bd33d792fffc7df05882197f8e35656f32537d3af2dc0`  
		Last Modified: Tue, 25 Feb 2025 15:27:20 GMT  
		Size: 227.8 MB (227754189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3eb58d627d47bbabda1df5ea93b93ecf8906adbc5354dad843f765ad6b633b21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16950596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b524bc034e73f7df3b9853fcf51a60e8756d31d6ff52c16eb1c4cd854f77c739`

```dockerfile
```

-	Layers:
	-	`sha256:85bc1733c317ce943f2e5a6a898f442ed9931a1b66369ce864608b35fcba6428`  
		Last Modified: Tue, 25 Feb 2025 15:27:15 GMT  
		Size: 16.9 MB (16940323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e92c8e9ca7faad7eb1d5cf76cbd4ba916a081247748d5cf5035411bfe29a339e`  
		Last Modified: Tue, 25 Feb 2025 15:27:14 GMT  
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
$ docker pull buildpack-deps@sha256:dbdb3935fc73e886dbad52d87770d957cbd7b3da319e52ce60b2cefcec3bae34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.0 MB (386010995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fba81901c03186a5e748c4da8f475c05b55c9ec495b47a53e65d539be72f5a9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1740355200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1ea3e230c71f31965fdc8d0bdc4e71749c73ddb97789439e708ba01bec0516b7`  
		Last Modified: Tue, 25 Feb 2025 01:34:02 GMT  
		Size: 51.1 MB (51131291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7136b138a9fbadd117790fd6473b3c1516b6ff1b1b1e5e321ff71f2a2c4c08c6`  
		Last Modified: Tue, 25 Feb 2025 04:34:33 GMT  
		Size: 29.0 MB (29016584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a7bb81cdfac8e52fedda82eb71511b491bce0161320904fa9a6cf3542f360d`  
		Last Modified: Tue, 25 Feb 2025 08:22:16 GMT  
		Size: 72.8 MB (72849870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b9193155e6433be9c72a79a072384c8d9c994e3a46f363cea47d85fe4057f4`  
		Last Modified: Tue, 25 Feb 2025 11:57:05 GMT  
		Size: 233.0 MB (233013250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:48fd5fa468890d51856d7aff2e9a851b53564b542061cffa5cb937f395acf140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16856443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb8a483835c66bb279c4c3c9d4c677d206b0c669dfde44cbd35fca6c0f140895`

```dockerfile
```

-	Layers:
	-	`sha256:2597092f65f219e1017531f65960cadade51c3e614910854a2debc90d3389932`  
		Last Modified: Tue, 25 Feb 2025 11:56:57 GMT  
		Size: 16.8 MB (16846218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b61ff43ae01014d70b7c430e3452a9a00f8aed1b4b057d9cdfe31fcbbc86bba8`  
		Last Modified: Tue, 25 Feb 2025 11:56:56 GMT  
		Size: 10.2 KB (10225 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:75a08081b54d2e72741a8dcc56634fe810b65b5c49af6d14164dd89f53e77798
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.5 MB (352454019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d0e746b391e6be1f516c21aa919b96d45adca4252a5ed707ed7d7734a10da80`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1740355200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ab0460cfb129d20515573ff27552b94c41a5822739be2d7bf548df5315225ee2`  
		Last Modified: Tue, 25 Feb 2025 01:34:35 GMT  
		Size: 47.5 MB (47508261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ec199ac309750ebc4bdf20cce23eb64ef847d0a7c63d2075c1e80b9a8017dc`  
		Last Modified: Tue, 25 Feb 2025 04:05:59 GMT  
		Size: 28.6 MB (28608136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4971e21f8d766abab097575a50fb382c4f9461b5b1c49e9167693254a56cb32e`  
		Last Modified: Tue, 25 Feb 2025 07:19:01 GMT  
		Size: 68.5 MB (68498289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d0b6a464804002fbaa4678001a519c5385071e63d3bd4b4e7858cdde7a3f3e`  
		Last Modified: Tue, 25 Feb 2025 09:27:04 GMT  
		Size: 207.8 MB (207839333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:16daf362086a893af19dddbf51277bb30758181aeae9b7b4dfee8cfc60e32c5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16650068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:011a61c624e103ec4a28e6055ef330a76c3b4134fb9ff34804f002b54dd56f58`

```dockerfile
```

-	Layers:
	-	`sha256:f112b533cb3db1e1b06faf1a3b4297d9b6925022230049af57923235606d1eee`  
		Last Modified: Tue, 25 Feb 2025 09:27:02 GMT  
		Size: 16.6 MB (16639876 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19418062cdc7e6cc001edf19870d3e1ccb3fc76b54f1765599a3e89a793ba0b9`  
		Last Modified: Tue, 25 Feb 2025 09:27:00 GMT  
		Size: 10.2 KB (10192 bytes)  
		MIME: application/vnd.in-toto+json
