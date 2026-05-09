## `buildpack-deps:sid`

```console
$ docker pull buildpack-deps@sha256:193c3c44ef74fbdc5ae78e4cb29681eb7757fddd3920955a8a2b1aa7d3ebe3c7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:sid` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:190ce5fc174ecd7383b8e74e6eaa30386863d28248f696e622cfb0cb75c81949
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.3 MB (360328760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d13b75b3b14a87eb042e7a8238f206cfa18200d2a2c39584ebe3ed10f6043d12`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1777939200'
# Fri, 08 May 2026 19:40:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 20:26:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 21:17:48 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:099d3355eff9ccff1f5ee3b288e1ead2e7035e89d68d0fc80f60a9bd7a9815e3`  
		Last Modified: Fri, 08 May 2026 18:23:36 GMT  
		Size: 48.7 MB (48702238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69fa57e83b29efeaf3d37af3434d6c21acf443c2346367f49caf4c6efea18b60`  
		Last Modified: Fri, 08 May 2026 19:40:55 GMT  
		Size: 26.9 MB (26893395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3ea472587b5d0ea5e4527a273544c8354a60d406eef30abe1f16c1a2e24fce9`  
		Last Modified: Fri, 08 May 2026 20:27:15 GMT  
		Size: 76.9 MB (76898934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c23b0444f5b8480df51f6189d7981b8b6ab766d30776ac813728a01daa76dd9`  
		Last Modified: Fri, 08 May 2026 21:18:31 GMT  
		Size: 207.8 MB (207834193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:00f8e0e1a6e324cbac1fda8a6c7e898a7b37547b7041c09466cff8be163ec46a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16901934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc8c3e295a02300ea6cf2d78023405de215e31fa542d758ad2cff5caba980b9`

```dockerfile
```

-	Layers:
	-	`sha256:78c2e7f710e75a7025d4921e7d2fc8b161fb0777059dda9ec97cf31a97ab17b3`  
		Last Modified: Fri, 08 May 2026 21:18:27 GMT  
		Size: 16.9 MB (16891801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59541df29618faf4c64d7aa313e565423988bdfa0c9dc63f3ec29b047ac4298a`  
		Last Modified: Fri, 08 May 2026 21:18:26 GMT  
		Size: 10.1 KB (10133 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:2a9640dcf17d1efc94d00a60527c963709715559341c462d88b15ec07e9fce8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.1 MB (305060316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ac2ed48ba4ba95324d998f2f22516c09eea9b5d14036b578cfc5ea3ed18fa11`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1777939200'
# Fri, 08 May 2026 19:44:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 21:35:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 22:13:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:79db944cb324910e68326e7a22d4bc47bd01eb269d35b1d153975be52958d92f`  
		Last Modified: Fri, 08 May 2026 18:37:35 GMT  
		Size: 45.6 MB (45609975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ca5da1f5f4fb120cd7b2b40034ee2f9bf3ebf8737773b984403a970bf3e2fd`  
		Last Modified: Fri, 08 May 2026 19:45:01 GMT  
		Size: 24.6 MB (24605248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd8b20f1b602807fdd595831094bc74ca40f7858af75fa5510dd6910595d566`  
		Last Modified: Fri, 08 May 2026 21:35:25 GMT  
		Size: 71.5 MB (71476055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d23a6cd7ccbba38235da7cab3b8e7a034488dd9f4ea58598179dea8d7e758fb`  
		Last Modified: Fri, 08 May 2026 22:13:43 GMT  
		Size: 163.4 MB (163369038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:aafb77f859b76ec0df912c9c81bf5a4a343f4826802227f16af9e273908405ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16657093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38286e85600b409d0dc0ad51a4d5500a15149b2b81f161ad5ef70a5e82bc91c6`

```dockerfile
```

-	Layers:
	-	`sha256:1f7bbecb23266a3b9a7d4ac4ebc2affc21966d2e9f0453a7ce2a820ba0a7416e`  
		Last Modified: Fri, 08 May 2026 22:13:40 GMT  
		Size: 16.6 MB (16646896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73e0f5298219a1915919d2fd88ebd7ef7236645c5a1b10f40402922f5c154245`  
		Last Modified: Fri, 08 May 2026 22:13:39 GMT  
		Size: 10.2 KB (10197 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:19695f87a0d505077ab5cef22cc65d78c93de59c3dbe92b15c0de71fff0888d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.1 MB (349083665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00fc5b8e901856551259c26b38a518e40e42a2f3c24ca0f88ac1bb2b47cb0b35`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1777939200'
# Fri, 08 May 2026 19:42:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 20:32:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 21:17:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:99699fbc842c790e8471e4039d9c409499f27c659ef9c4d3336a0743660ec819`  
		Last Modified: Fri, 08 May 2026 18:26:06 GMT  
		Size: 48.7 MB (48734151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a8fe1ac3f05529fe3bd8a59a20b641133e27374191e01da78aeed091f2bc7b`  
		Last Modified: Fri, 08 May 2026 19:42:43 GMT  
		Size: 26.2 MB (26171326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d44d2c5450e62d768f4b870f1d64fbe0f35f64842962a55a3e8078b24f599148`  
		Last Modified: Fri, 08 May 2026 20:32:44 GMT  
		Size: 76.1 MB (76064963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a010f74a77cec0305e21572fdb6828b9a6567a28e157859a3fab62b53cd030`  
		Last Modified: Fri, 08 May 2026 21:18:24 GMT  
		Size: 198.1 MB (198113225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1509a29a8e152e3d5db25186410f4f6e48937487cc45bfca1b125c5ad2f8641f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16983123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb028e4ac36fa8461f068f25c898f2f24b9f75346dfc1272b415dda593364dcf`

```dockerfile
```

-	Layers:
	-	`sha256:807e8b027d06b750a3b76fd314cd18ca19463e8d0d3879b13c98d1c64fd42af3`  
		Last Modified: Fri, 08 May 2026 21:18:19 GMT  
		Size: 17.0 MB (16972910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ecf3b7c8cec5e56c942edf304130f68ec0e1ac64bb1eba2e9611885541dfb88`  
		Last Modified: Fri, 08 May 2026 21:18:18 GMT  
		Size: 10.2 KB (10213 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; 386

```console
$ docker pull buildpack-deps@sha256:b1790be03bca82bcdfd25e4975ae1bf00c49d07a19921d7e8827b46107a315a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.9 MB (367918209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a112e3f4c5cc2a5f417b298d8d369cd87d182061df19a89fc5ddc21602735ff9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1777939200'
# Fri, 08 May 2026 19:44:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 23:05:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 09 May 2026 02:30:17 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:673cf326009083501c3fabdd17567c937b894deb57d94461178ef18820adb917`  
		Last Modified: Fri, 08 May 2026 18:32:00 GMT  
		Size: 50.0 MB (50006715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e321fedc955b961c2c658a44d5ca3cbf39d67286d1387087c4563c14de6beaf2`  
		Last Modified: Fri, 08 May 2026 19:44:11 GMT  
		Size: 28.2 MB (28209562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50aed63d3cc12b285e748a36467b5f1679aeea9320464d6cdbf22ef3646a881c`  
		Last Modified: Fri, 08 May 2026 23:05:49 GMT  
		Size: 79.1 MB (79125872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e430e7418b2a592a43bcd48551dd9a740668bf8b164870c9907c56723441e3f7`  
		Last Modified: Sat, 09 May 2026 02:30:59 GMT  
		Size: 210.6 MB (210576060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2c7880d4705dbbe3075e1cf084cb9fac62f40b1577e5e5de903608ab455c2cfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16870925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f433f79ff37b6dc992f0baba7b5dfb03762acca65438589889b5574d21495108`

```dockerfile
```

-	Layers:
	-	`sha256:54db99378d1328aed63bab13e43f9bfa24f78de910ea18bdb10a4328d2072e6e`  
		Last Modified: Sat, 09 May 2026 02:30:55 GMT  
		Size: 16.9 MB (16860815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e94419f38fc4bd13266ce39e226583070dca595195960b3595a2d348e93b82c`  
		Last Modified: Sat, 09 May 2026 02:30:55 GMT  
		Size: 10.1 KB (10110 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:5a1741fac81a4533cfac2efbc3554506c0626fee228f069bf1c0850b14ea98e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.8 MB (358776873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:906b837c16f387e81fe1a985fe65f24589145196048fdb576453bbe2abb0eff2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1776729600'
# Wed, 22 Apr 2026 03:40:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 09:38:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 12:16:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f737822391dff66f42c11b9dc44b70287cb895238a82a880fb68ce9e44f2b3bd`  
		Last Modified: Wed, 22 Apr 2026 00:16:36 GMT  
		Size: 54.0 MB (53970920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d31f9fb5fb8a5668727ae17f4dee5b580a9b4c14b4594301d41edc4810d281`  
		Last Modified: Wed, 22 Apr 2026 03:40:33 GMT  
		Size: 29.2 MB (29188657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b0b1dad0ccda2527afbff0e20a6c17b5425e26426a389cc87cf625c9f409a9`  
		Last Modified: Wed, 22 Apr 2026 09:39:17 GMT  
		Size: 83.4 MB (83434536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c9e6862d09d71e62338318c4188728e1e72eec6391bcb725272725758677bd`  
		Last Modified: Wed, 22 Apr 2026 12:17:46 GMT  
		Size: 192.2 MB (192182760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3a8158f6a27d7fb6f5e5dd8acd9503f7c2b52e279783b5ec642e29449f594cde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16841371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93b47382ac9989ff0c55f76f68da71b0c1aac137eda9f9c47caee110c880a314`

```dockerfile
```

-	Layers:
	-	`sha256:fa9f15436709270a6823ffc197d039a2d3dc6c3265abd51e05efda89ee84bd1c`  
		Last Modified: Wed, 22 Apr 2026 12:17:43 GMT  
		Size: 16.8 MB (16831206 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c2b2601a24e07cdd879e3602d0ab27291ecb447de4cc0cba6709b33933dc6d5`  
		Last Modified: Wed, 22 Apr 2026 12:17:42 GMT  
		Size: 10.2 KB (10165 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:4a9bced1c66d89423c064cc03a85641d4f717eff9f16e03c9c25f9de0f23a587
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **466.7 MB (466713358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5b77b3154b6557786528e557e07c358dd3d79b8665e4a0f7f039aa172d0bcb4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1776729600'
# Thu, 23 Apr 2026 16:18:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sat, 25 Apr 2026 23:13:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sun, 26 Apr 2026 16:00:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:81bdcc2a2c75f60205e81aaab6ad24265169afebbe01f9647ffa51fb2405f8c4`  
		Last Modified: Wed, 22 Apr 2026 02:18:34 GMT  
		Size: 46.8 MB (46781244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f657cbba56f24dc0e9fdff00edac2ca19d5e98a8de59cf2582136511284eea`  
		Last Modified: Thu, 23 Apr 2026 16:20:36 GMT  
		Size: 26.4 MB (26432872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd30b3097dc0b79d7d23a554f029928d496ef8492dff6b493835ce6fa6de48db`  
		Last Modified: Sat, 25 Apr 2026 23:17:34 GMT  
		Size: 76.1 MB (76091843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d533802a32574ad16cbe7e1783c90a250eaf55c6b29fec65f3e0d15214e6f19`  
		Last Modified: Sun, 26 Apr 2026 16:15:52 GMT  
		Size: 317.4 MB (317407399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b6f13b9fbab722403edc5e43ad18706c3705322c7199faa149aa69a6ae648163
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16931829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04aff93c68ab46ef7f9d44f76eafe3ac13c93b1f2d4dee76e586254cebbf4415`

```dockerfile
```

-	Layers:
	-	`sha256:99158e3c5c92a79e4a1f50fbe3a1087a1964e67c659ff434e1ecbce3644556a0`  
		Last Modified: Sun, 26 Apr 2026 16:15:09 GMT  
		Size: 16.9 MB (16921665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d6417f4232b5f9acff0842549beea4cb52a31775b2745f4091cc41d5c556837`  
		Last Modified: Sun, 26 Apr 2026 16:15:04 GMT  
		Size: 10.2 KB (10164 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b696612c668e62da58331f9631f1ea8e248448277134664f7fd8a9d27e6a99d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.3 MB (332278045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af655fd3f05a42b72555c311e16b3f3c7e19687fc59154bc018b3d9e8eca9392`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1777939200'
# Fri, 08 May 2026 20:53:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 22:33:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 09 May 2026 00:14:47 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:107669ad500d1f91592ad03e52cc25095058c6b4b2e83b9adad6737bfa81cd40`  
		Last Modified: Fri, 08 May 2026 18:28:19 GMT  
		Size: 48.4 MB (48444076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc97077ab9739db4cafdc266dad352532794bc43462c59a59b2c72e9905c9a6b`  
		Last Modified: Fri, 08 May 2026 20:53:40 GMT  
		Size: 26.7 MB (26690958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff287d664c958fce4515d8b2c20dabe46ef9c7409eb524b5663736abf250d5a`  
		Last Modified: Fri, 08 May 2026 22:34:02 GMT  
		Size: 77.4 MB (77425475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd5a3007f2ffba600ae25166fe7af5c46e7fcdec6882177f35ffd65601b4fb3`  
		Last Modified: Sat, 09 May 2026 00:15:41 GMT  
		Size: 179.7 MB (179717536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ffa92684e54ffaa47301530190de27ff10f0008976024285a71f2c9f24095362
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16656048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c081f74aa4ff85aa48892f4e90d7104cff1d07b1b39049a00824d2c0d4a66e94`

```dockerfile
```

-	Layers:
	-	`sha256:f72e4013f2a69c379de539a02f654a7d98d980af32b4dbc7489ca64a72ee83bb`  
		Last Modified: Sat, 09 May 2026 00:15:37 GMT  
		Size: 16.6 MB (16645915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:caf5ac594ffd21a4cdc124219c15434067e397324d37e820f62f701f0d74ad91`  
		Last Modified: Sat, 09 May 2026 00:15:36 GMT  
		Size: 10.1 KB (10133 bytes)  
		MIME: application/vnd.in-toto+json
