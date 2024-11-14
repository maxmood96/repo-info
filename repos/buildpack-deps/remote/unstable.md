## `buildpack-deps:unstable`

```console
$ docker pull buildpack-deps@sha256:8f4a6ea8fa9457a602f66a1eb3a82d6032099f1916c34e3bd091053723485972
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 18
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
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:unstable` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:b0afb66526d240be44af24d222b1ce19acfe78052893de838fda19973402d501
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.4 MB (369418391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:667b3261aaabd8a7375c74cad935ce525d633924294649dbe9843ca6d64b82be`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c6dd4b778062640e2abc4c889c6db9feecceff7f28c2100dcfa570652558218c`  
		Last Modified: Tue, 12 Nov 2024 00:54:59 GMT  
		Size: 53.3 MB (53319444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73df9c0ffd5cfef9ed63d0dfdae57285f543f78320d947c5c4c2ab1422641cb3`  
		Last Modified: Tue, 12 Nov 2024 03:14:01 GMT  
		Size: 20.6 MB (20596172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0899f4ba4649838a893d7f1a70928afc27b147ea5051eac0853a716ef24ac8c8`  
		Last Modified: Tue, 12 Nov 2024 03:58:48 GMT  
		Size: 66.6 MB (66611604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ed16753ac0d236589a2917598d5bb24201a1ceaea372a998220ce50b9205de`  
		Last Modified: Tue, 12 Nov 2024 04:55:30 GMT  
		Size: 228.9 MB (228891171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1b890f2498c3d06d74a7599cb7d559795eec3be2ba36f8a137314885003385aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16842737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c73e51bc26aec5f86f0bc30b85d6af0a0476863bd7bcbefedc0bc2678c495610`

```dockerfile
```

-	Layers:
	-	`sha256:3442b9a36e4134cf6b67919c2d04b50476534f845c966ca8e6fb00848e915279`  
		Last Modified: Tue, 12 Nov 2024 04:55:27 GMT  
		Size: 16.8 MB (16832561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:540e6d55dabb7696f8459f07f029499d23edaa473f9379257c196530e33b6b4e`  
		Last Modified: Tue, 12 Nov 2024 04:55:27 GMT  
		Size: 10.2 KB (10176 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:64f60ab32c8ad2e44569bd34aeabfcbcae655596ac34599c5336dcb78f1347f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.7 MB (337698112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37fef2df89ec55a84f53ca077a2e2093c773663a924f03a53bdb6116f54dd565`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:48142c53989e584e5008e025d7add416317666ef57f1383dab96cb3b5dd1610c`  
		Last Modified: Tue, 12 Nov 2024 00:55:48 GMT  
		Size: 50.2 MB (50178305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:677e719f1a345c9d868951b12d49877be0a8ce88c74c1d28554e382cb36c8fb0`  
		Last Modified: Tue, 12 Nov 2024 06:29:07 GMT  
		Size: 19.6 MB (19609396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a80294a22345764a6f713791d5e78ceccbfde6983b0bf68a23d16e31cb7a8d6`  
		Last Modified: Tue, 12 Nov 2024 11:31:21 GMT  
		Size: 64.1 MB (64064343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aeecbd78ab8f389d36bc7c389a258f35fcb1d7c525c852264f355392a01b52a`  
		Last Modified: Tue, 12 Nov 2024 13:57:37 GMT  
		Size: 203.8 MB (203846068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d6d24b2e38e21cc1d214a4e09d6ef1cda2fb1f0fffa2e118fef221c726e42ede
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16634683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4da72b7f704e230a29b6d8886bd354cea7afd55b586897a8685011369124695d`

```dockerfile
```

-	Layers:
	-	`sha256:5cf2be7911debe59da7ccf2740ddae1696946eaf5fec6399bba7ceafa9082524`  
		Last Modified: Tue, 12 Nov 2024 13:57:33 GMT  
		Size: 16.6 MB (16624447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a10c1a45b73521ebcf10c889a4ba4d096cb8325e02ba6a3ce6727a8947f2c49`  
		Last Modified: Tue, 12 Nov 2024 13:57:32 GMT  
		Size: 10.2 KB (10236 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:b689eecf5e3ddb65c714aada92e223d285c4ac43f13e91a42bf2d70453e2f3da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.7 MB (319686589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d94e816c37f9669fbd10193e39b4d3611aa14e2da8cda9d3ae8ead77abaf4e5`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e17a4ae99f3dc5642f3037bdf67fdb8d526cf44879dc2a2a82dd78799b94cb90`  
		Last Modified: Tue, 12 Nov 2024 00:59:40 GMT  
		Size: 47.8 MB (47762858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0690a3ea44bb2abf7747807b4adbbe717ea3308dcc90d88289979cc43a641049`  
		Last Modified: Tue, 12 Nov 2024 16:01:31 GMT  
		Size: 18.9 MB (18945424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0b86dacd9090665be47b5966a673c201e9be17e12af3a6b155bc5749678a52`  
		Last Modified: Wed, 13 Nov 2024 07:40:03 GMT  
		Size: 61.6 MB (61581104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:793a5bb59c9cc98bd9311baf3dfda09c62cbbdad289968d6fd5656cf3da063b4`  
		Last Modified: Wed, 13 Nov 2024 15:30:35 GMT  
		Size: 191.4 MB (191397203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:530738ff9c47bd069bb02d245ff0123ec8dd415a3532a1dd1e8621051ad5d3c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16645114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a801ab949bf85d546299940055d3bf2f3c3e94bb32c4d18787a752812cd89f12`

```dockerfile
```

-	Layers:
	-	`sha256:e35074208bc1e0fcf2be2ab9ef53e3c24eff11330b9eed0f8de0c375af2162ba`  
		Last Modified: Wed, 13 Nov 2024 15:30:30 GMT  
		Size: 16.6 MB (16634879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0260b6276ba30dd6d8f32b40f4415e8c535d07e946b378fbbfb9a22caadebdba`  
		Last Modified: Wed, 13 Nov 2024 15:30:29 GMT  
		Size: 10.2 KB (10235 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:671281f0eec1276bc2ca656b2b1ffb8425ed67a0e49b294864caedd8fe344762
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.3 MB (363298796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53faff9404befb57b76d8c164f5d2ace4a89ec596aab481169cc2203aebf3535`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0c8e2196f060907b4d5381cc165d86913c4b9e9c632b3596563398b5e178a84a`  
		Last Modified: Tue, 12 Nov 2024 00:59:55 GMT  
		Size: 53.8 MB (53759747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2180b05bcdf8eaedc4db9cf7f65afe026827aad32c4e4b7f24679e6ea2c63305`  
		Last Modified: Tue, 12 Nov 2024 11:17:08 GMT  
		Size: 20.3 MB (20250755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da6ab97bb0c21d31a38290cf57289900a53f954b993db59f27f8cedb1eb175f`  
		Last Modified: Wed, 13 Nov 2024 02:43:36 GMT  
		Size: 66.6 MB (66621232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93041a7102a00ca946f6a90d08ab0c3a9d59d3a03288a28350e8a1ac235ee360`  
		Last Modified: Wed, 13 Nov 2024 08:06:27 GMT  
		Size: 222.7 MB (222667062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:71c45282a4a3d4f4ee1dea17c38671d449a920831950d40d29a12b53bd1b9d16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16945838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d5cff6b2c17508fdcba6df91b61b43021773e82df652eb69bbe2b5bedd58098`

```dockerfile
```

-	Layers:
	-	`sha256:c660a0272b5e1de7faeeab0d3f1cb410c5dd067c2142155738f05b844de3574d`  
		Last Modified: Wed, 13 Nov 2024 08:06:21 GMT  
		Size: 16.9 MB (16935582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d67bc6b3e84d44fb2ec77aecbbd46c6b065ae361aff2b410a64d8166d094b141`  
		Last Modified: Wed, 13 Nov 2024 08:06:20 GMT  
		Size: 10.3 KB (10256 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:174aa49a8c627409e7b2ef469e0b4ca424e1d67801529a24e00206f67c85e020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.6 MB (374625880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1e991a9111b7923adb2bf1517a0cea45e0e2cbe21c971a883abc5d20fe7018c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:266f316e766c7029b1cbb65159b6d9ea1da28d00e28cf109ea069ce95b082ac4`  
		Last Modified: Tue, 12 Nov 2024 00:55:10 GMT  
		Size: 54.2 MB (54192046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24546888a84a1c2171ba5648f213b4d3b8fee560f454ad1c12f583f6ce895c81`  
		Last Modified: Tue, 12 Nov 2024 02:37:52 GMT  
		Size: 21.7 MB (21725392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885dfc308254678967ab6d79ba6d40d73a4ad263c111beedb94327edea737b17`  
		Last Modified: Tue, 12 Nov 2024 03:14:27 GMT  
		Size: 68.5 MB (68538589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470064ab8c694d08e8b01d3ab58e57e6bbb9021d73b77eab103438c7c9d1b9de`  
		Last Modified: Tue, 12 Nov 2024 03:59:40 GMT  
		Size: 230.2 MB (230169853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c68dc1085e970079c0dad9475c90a626f3fac854d399d14c64fc0624e1214a07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16812358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3c69c51ca15442a3ea0f50ed9b720d7bc599cb88cfe9ea50099b42ec77303de`

```dockerfile
```

-	Layers:
	-	`sha256:e8d60b7da8728b26a8fa539127c6eb8ccfc4ff307613730c7801c4e74932bef0`  
		Last Modified: Tue, 12 Nov 2024 03:59:36 GMT  
		Size: 16.8 MB (16802204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5db9b50ef37135bc668d6adde1f571e925b918ed88cc1254591868dd645594d0`  
		Last Modified: Tue, 12 Nov 2024 03:59:35 GMT  
		Size: 10.2 KB (10154 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:ce8aa039e9a6e82c43c475c3fef10d04e2b8123d1061e406889d4b27902238ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.4 MB (347392359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:355f4a8116380ddc999b74d29f04f5c60cd5557750ff6bcdbdf6b754204fe5fe`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1f6d00c97864e98dad498c4c1087cda2fb16f2ac6e7a71ac1353418dd4215995`  
		Last Modified: Tue, 12 Nov 2024 00:59:58 GMT  
		Size: 52.3 MB (52275237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ee73bc743170bb5e4087d57c95a63d610fb1282220d73ff90af4707b831d99`  
		Last Modified: Tue, 12 Nov 2024 18:03:00 GMT  
		Size: 21.0 MB (20950191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63aac7a2dcb6a719b792ac16c19c2652ad08047befbc851b6ae687255f6838b0`  
		Last Modified: Wed, 13 Nov 2024 02:06:14 GMT  
		Size: 65.4 MB (65354987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b021b9b5ef29ca07d0584978e6368d7c104c4da333fb3b2f41e3c5fd0643928`  
		Last Modified: Wed, 13 Nov 2024 07:13:31 GMT  
		Size: 208.8 MB (208811944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8c879aa61306b6af21c2966d8d1d1c3b7ef264bd3594436ea3e5368f393c1aad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 KB (10009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7546a610f8060307d18969256b9af525deb7e2d6898ab8ac5b12b4a9eb135d6c`

```dockerfile
```

-	Layers:
	-	`sha256:8a2ea7b2944f183bac3a45fc36453a325c7160840c26f1b60d78a02b64bdc82c`  
		Last Modified: Wed, 13 Nov 2024 07:13:12 GMT  
		Size: 10.0 KB (10009 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:aa2bb04dc00e35c862bd85cef6e11376c81dfc145ef71edcf86c2b27bc83bc41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.2 MB (379158322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8d3e46f31c4cca769ed8baa17c1406024a216cbf674dbfad17680f8112624ec`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ac2d911f8489db0bbd6f313128660ffb4f315b3d99baed39d7128c198fea25b9`  
		Last Modified: Tue, 12 Nov 2024 00:59:35 GMT  
		Size: 57.3 MB (57309355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5f3e8aa1353894772b7fd9d91dc6448cf8573234fedf1ba1c8596471c52519`  
		Last Modified: Tue, 12 Nov 2024 08:30:11 GMT  
		Size: 22.0 MB (21992150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f36575664f661fb4663abf9a54ae38f6714b2f1a53511cc1ffe3d8ddb1acb8`  
		Last Modified: Tue, 12 Nov 2024 16:11:05 GMT  
		Size: 71.9 MB (71859244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa16d103a10149cc71323be1b243e7c5970ffd7abda2adce550572ce6183d1e`  
		Last Modified: Wed, 13 Nov 2024 00:16:46 GMT  
		Size: 228.0 MB (227997573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ee6c22b341c37400b40398ad3a5c48edf03c2821e2df1e51e37e5d6d19fd6563
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16840561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79bc0918bff770173a22720926245ea5872f77e77a2a6bcf71c8e1ba073e9b32`

```dockerfile
```

-	Layers:
	-	`sha256:04597ff4f6060e3464b3e1edb39aeca284fc455c65149552bfa1dc3557e395c2`  
		Last Modified: Wed, 13 Nov 2024 00:16:38 GMT  
		Size: 16.8 MB (16830353 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb4c649ff7e0878965ed21c805cdd1d6f0164b2e413054c4086d5b1394932145`  
		Last Modified: Wed, 13 Nov 2024 00:16:36 GMT  
		Size: 10.2 KB (10208 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:b151707d6758fa58e690e9d3d3c486f5cd8e4b545cb22fdae449de8dc33dbb32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **451.7 MB (451743115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41b067d1ca2443725f528f0f66bdf878fa5fb4da48e601f06b68679ed5cd8ae8`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0dca4f64307c74a46b21f69146149abf9e633cc0b181c05fb118d6e04f8d6365`  
		Last Modified: Tue, 12 Nov 2024 00:58:50 GMT  
		Size: 51.7 MB (51741042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c466fdbf53844e588f96639c3cb6fc67b78c84c769678e12defd736cd290219`  
		Last Modified: Wed, 13 Nov 2024 01:46:00 GMT  
		Size: 20.1 MB (20078602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:439d63c37fb468843722515950f8cedabe03fb1bda52b47185c22c3906764368`  
		Last Modified: Wed, 13 Nov 2024 13:12:18 GMT  
		Size: 65.7 MB (65673392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a3a1b053ddc1bc12cb41b43a94ab6d228f3c2e79855f38e66332ad654300bda`  
		Last Modified: Wed, 13 Nov 2024 20:07:35 GMT  
		Size: 314.3 MB (314250079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c902cea29ab122271fc0e092631d1073ad05fba0db5d4900d3060088fc21ed3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16904093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3efdbd0c5c214cb3c08f148a5c2e6de69cc171a1f300a8d84c775f736997ebe4`

```dockerfile
```

-	Layers:
	-	`sha256:8e8ccb0921437e151c9959f476a15dc19f198415860f53a23f31e278320b2203`  
		Last Modified: Wed, 13 Nov 2024 20:06:55 GMT  
		Size: 16.9 MB (16893886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b51e74453b1b89faff99c720dd20fa87719c301fa733e411642ba8ddc970dfc`  
		Last Modified: Wed, 13 Nov 2024 20:06:53 GMT  
		Size: 10.2 KB (10207 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:7df0d9603d537b9d3c5f1a8a582099e31643edb53b7140068d9af8477337c248
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.2 MB (345160340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c17453263e2e59ec60ea3dd351f693dd4ef90985f1a64c23abbb53ef8ba5906b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:01b62be41cbf7168e02a9fa648a1525f0c9095aef51faa9027bf3a9ff89c6b84`  
		Last Modified: Tue, 12 Nov 2024 01:00:18 GMT  
		Size: 53.0 MB (52980914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaa52c56b4fa2fb05d933bf62d254d5f4371a5a9e6992ccf74613eefe11aaa96`  
		Last Modified: Tue, 12 Nov 2024 09:02:57 GMT  
		Size: 21.7 MB (21709508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:371f5c95f0d6355567bbfbef044cac10682ae55767ca48b41b71050883b57bf6`  
		Last Modified: Tue, 12 Nov 2024 23:33:49 GMT  
		Size: 67.7 MB (67747015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef960ce691967777efc4ce38f0da26fa74108dcf45bb4fcff7e681d70ceda1c`  
		Last Modified: Wed, 13 Nov 2024 03:27:07 GMT  
		Size: 202.7 MB (202722903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fd3177a0dd921bb2feb75924cfe3587695a304cea8580c1951d0a2c6f6aa8025
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16634866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cad8aadf6c308c5edf63fd9014152f51b37b58c11162771288ed33d97585744e`

```dockerfile
```

-	Layers:
	-	`sha256:eb41514791b98768f3a0c6a5557723b8efeb52b01694a6ca70977a5710d8e7d2`  
		Last Modified: Wed, 13 Nov 2024 03:27:04 GMT  
		Size: 16.6 MB (16624690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b818347d73627d6e406ce24efeedffbd20244907dca8b460d44c47aeb13b5d54`  
		Last Modified: Wed, 13 Nov 2024 03:27:03 GMT  
		Size: 10.2 KB (10176 bytes)  
		MIME: application/vnd.in-toto+json
