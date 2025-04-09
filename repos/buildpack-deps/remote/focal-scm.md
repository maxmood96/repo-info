## `buildpack-deps:focal-scm`

```console
$ docker pull buildpack-deps@sha256:ae2c6c512988fcb5780082c1fbb0e21d5a8c6c5d376fd581aa68350e9d75583e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:focal-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:369f4b09a397d0d40a1c8adba0223197b8fd25b06500c2bd7ab76aec2a3b69a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.6 MB (99605999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5fe03dbe0806131982469bd0f9757c2bffbec29cdab41aa0ac00b13f1d694fb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7577a2ab12ee9be5df3b0c322f8c7e4cb7d72c7826b239c5a9581720d332213b`  
		Last Modified: Wed, 09 Apr 2025 01:45:55 GMT  
		Size: 11.2 MB (11150331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c877c591199a05136cbe615838a58a7f442fd6f8ab6f1220d44832d7d85f20`  
		Last Modified: Wed, 09 Apr 2025 02:12:02 GMT  
		Size: 60.9 MB (60945274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:focal-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:faf95c6808a15a9a4b29c81b19b4f5dca143916e70cadced9b0b50bfa71e1bb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6673370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad7fddb59e640a5431ae5d8796148af46483f130f271df382bddf4701618d868`

```dockerfile
```

-	Layers:
	-	`sha256:b8b35747e5852b1cb138d56505badb949971bc69b93769e57ac902e38d6de011`  
		Last Modified: Wed, 09 Apr 2025 02:12:01 GMT  
		Size: 6.7 MB (6665988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92d63d6158d3b124baa68e5b2f7c0d7fc9b97488736813b42c36a90ca693a179`  
		Last Modified: Wed, 09 Apr 2025 02:12:01 GMT  
		Size: 7.4 KB (7382 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:focal-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0ba9733556367b696f7f8c98162a8b06ea14e455f9b4ce45e091a19a7df636e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.1 MB (89122961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:377e8a14c1c6f6f2f02d1e4e2b9794620d29ee881d57a1658519a7d1f9dbbea0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:f76c848564adfa0c782654cd9423feee0ffacccd95abfe3e4e696203d5e61fbf in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:10b337d353b3ceaf6823ab2d8696989401feed741b22eb313c8a0cd378762d39`  
		Last Modified: Fri, 11 Oct 2024 04:41:36 GMT  
		Size: 23.6 MB (23620412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:961fa3ee3eee16522e395458be87f5269ec5b27ec4fcb4d916faeb1068afaba7`  
		Last Modified: Sat, 19 Oct 2024 06:42:29 GMT  
		Size: 9.6 MB (9620727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10a338f01587f18e017e42cf3dfc75e5bd303749299cb0e64ea2a2a0865922d2`  
		Last Modified: Sat, 19 Oct 2024 08:17:06 GMT  
		Size: 55.9 MB (55881822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:focal-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c18c710ecbecc029c07733f7765b2f163752893001e68ce08dfa5f0f3e846abe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6684182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c29e5d67ea012adced3850967514aa055bc6596d9ef92cf55c25639702fbffec`

```dockerfile
```

-	Layers:
	-	`sha256:40f96d345c76424d7b3c8ace311292ea3a9aa7f22d9b83d18a60094bf4a764d6`  
		Last Modified: Sat, 19 Oct 2024 08:17:05 GMT  
		Size: 6.7 MB (6676742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f0da6b23a5b46534b605e78a83f2bf98bdfc1c58eaaf4142df4f9670439c20a`  
		Last Modified: Sat, 19 Oct 2024 08:17:04 GMT  
		Size: 7.4 KB (7440 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:focal-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:6b30fe5bf79eee34ede4c981ec37e717dac184636d31316f4b5aaa4cb6679c82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.0 MB (98024179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78df7c0741cdc3adb599669b8f74233ec3eccaa3eb58c8a1976e46b9aa54db05`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a902a6ffa3ee5a0c3f67d06b1a3bb3611210a02b2f2878ae8c1ba1419d989ce1`  
		Last Modified: Sat, 19 Oct 2024 05:21:18 GMT  
		Size: 11.0 MB (10992039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:974843836b66b5df8f55da9465dfaca000af6e2d0abe0b8f6cf9013fb718f2c3`  
		Last Modified: Sat, 19 Oct 2024 06:23:32 GMT  
		Size: 61.1 MB (61058312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:focal-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a19eb135cd6e631684d950b21e75be25d53d984b22fee5ac59d8c35efa2190aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6686824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eca2dc35be6a27a8a79e0940d953aece87ff8ecadf07487672f9c679d28c687`

```dockerfile
```

-	Layers:
	-	`sha256:a5b24f0e1d3b860b1596fd6b36a9dc5f9db79e913aea0444d579207d300136ce`  
		Last Modified: Sat, 19 Oct 2024 06:23:30 GMT  
		Size: 6.7 MB (6679362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:833904452c5bb38d61fb3efa3215ce3556792679f83594c2de9df3253152ac2d`  
		Last Modified: Sat, 19 Oct 2024 06:23:29 GMT  
		Size: 7.5 KB (7462 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:focal-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:33b86d00f582735f5824627f2b00e208c7d8b34ddadb3bc23cb29905742e5bfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114720817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:010e13ed60cbe79221d96ee656704e070164fba35e4180acd3246634944599f9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:d85970cec61787609e3854cb76ce16d54fe420b254cf48fc9ed9ed678717ff28 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:92d54367a68b4f03400315732acb4290d88bb06f8fe1414fd823f93402bec922`  
		Last Modified: Tue, 08 Apr 2025 11:48:44 GMT  
		Size: 32.1 MB (32076946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbe8b02ff52733b6c9023254a29940996cd72195264668a2791dcfbd8d98610`  
		Last Modified: Wed, 09 Apr 2025 04:26:54 GMT  
		Size: 13.0 MB (12963091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a47c8098863d5f0589ae9f6a551c0ff5ca0ca9faf3385f60c211a8c0999d57a`  
		Last Modified: Wed, 09 Apr 2025 07:34:19 GMT  
		Size: 69.7 MB (69680780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:focal-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3de80617924648fe1e4fe2c056a4891ad9ca0e6b9aa9c556928844305e138103
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6681251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d80b59916f149bdc030ad5bdecfe14f37652b2f0f41e1f7b0a5ebf16b95c89b8`

```dockerfile
```

-	Layers:
	-	`sha256:75b1fe89e3b672c80aaa0b42d55ce55ca65d77cd3d82c34c27829cf6aa494553`  
		Last Modified: Wed, 09 Apr 2025 07:34:17 GMT  
		Size: 6.7 MB (6673837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fcd79a651e4b9bd965f0cbd761d522cf56048d68e67b1529107b72aa0b032fb`  
		Last Modified: Wed, 09 Apr 2025 07:34:16 GMT  
		Size: 7.4 KB (7414 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:focal-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:3341f3a008f5b68ecb5a5d23f6c5b6a25cf599768edbad405cd58a8963b643d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.4 MB (97416891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:748ca636ba7564f61ac0111839cc8ac0e8e327c6859dbe7f893e4d2f99474d50`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:82f0132f510f24adc12d74491187647b94a14baa7a57fd22a67a5c3767541496 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b35596e17e863edd4c594d026a60e36f73cc6a076370f55a24732114fd25ff68`  
		Last Modified: Tue, 08 Apr 2025 11:48:56 GMT  
		Size: 26.4 MB (26368190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4495dc22cf93325906d3dc47401597dbe3f0e5d18ba19d26285034bdf0c41a02`  
		Last Modified: Wed, 09 Apr 2025 04:10:51 GMT  
		Size: 10.7 MB (10702249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6fe3eec205cfbc7c8ab84f500e3b8710bf1bbea0a0750d4c476d2160c50c2f`  
		Last Modified: Wed, 09 Apr 2025 07:07:21 GMT  
		Size: 60.3 MB (60346452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:focal-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c745fda3f5a9495f1223fac0c50bb52425b5fafd6650c196c2f0e8eeb3d58b1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6673441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67a815b57b2e0480a247a5e22a4503071aa605cf3655a8fe552917aafe37cb4d`

```dockerfile
```

-	Layers:
	-	`sha256:b8af3428d4e9c849ea38ebd27fe7eafb21616536c6bbb18694cb4818365b17b2`  
		Last Modified: Wed, 09 Apr 2025 07:07:20 GMT  
		Size: 6.7 MB (6666061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64afe5460ca88630ee156be013d14713dce8b8f30bee3152a70f79ccca194eaf`  
		Last Modified: Wed, 09 Apr 2025 07:07:20 GMT  
		Size: 7.4 KB (7380 bytes)  
		MIME: application/vnd.in-toto+json
