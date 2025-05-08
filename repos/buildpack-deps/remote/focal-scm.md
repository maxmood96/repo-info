## `buildpack-deps:focal-scm`

```console
$ docker pull buildpack-deps@sha256:fa56fe73b4475655b2f39d6376b6a6664d24b5c43227f709d4a923609f3286a1
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
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7577a2ab12ee9be5df3b0c322f8c7e4cb7d72c7826b239c5a9581720d332213b`  
		Last Modified: Thu, 08 May 2025 17:06:51 GMT  
		Size: 11.2 MB (11150331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c877c591199a05136cbe615838a58a7f442fd6f8ab6f1220d44832d7d85f20`  
		Last Modified: Thu, 08 May 2025 17:06:56 GMT  
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
$ docker pull buildpack-deps@sha256:44e98cb235ca83f15ac3dd13d244c716f93befebde14df1f13b845d345675634
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.1 MB (89123361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1fc87a2d446ba38b0c4aab8c3e0f0ef3ec604c32ec6c353835573f9cbf42c7d`
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
ADD file:bd50d86208ba682c6f55f52b7ec95adbfb2e247d9dfff47b9c3871d27a7b0d19 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:12c22ff1560db33ab4235fc5b1744509b7c274b95beb2a7ba7b6671705fcef6e`  
		Last Modified: Thu, 08 May 2025 17:24:17 GMT  
		Size: 23.6 MB (23624063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da7e36a763f959e9959a67d83a9318d563b85525cd5898dd19774da499cb0a5`  
		Last Modified: Wed, 09 Apr 2025 11:32:37 GMT  
		Size: 9.6 MB (9620939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df8cfc1c5d2280abe333b6e3ae8d6c857a34aec7fca5b6203efa3d9438d09a0`  
		Last Modified: Wed, 09 Apr 2025 12:17:38 GMT  
		Size: 55.9 MB (55878359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:focal-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:90934c4245591136a7df9416e4bf4097869637c864f9852ee73f799746176331
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6677236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34fa25a5d86fb056e542fc1efc3979864f01626bff475c881aa3d47ee05c3150`

```dockerfile
```

-	Layers:
	-	`sha256:3b04c2f02eb514d760c60ae6eda25f4a39a0c79f1dbc7901acbb943d45d405d7`  
		Last Modified: Wed, 09 Apr 2025 12:17:36 GMT  
		Size: 6.7 MB (6669796 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9552a2116ec7ce82a606363a495676e4d5277e4ba68cfc4d9aa70f61d4a0e0e0`  
		Last Modified: Wed, 09 Apr 2025 12:17:36 GMT  
		Size: 7.4 KB (7440 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:focal-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:3ea089dd94db7224e1e98abc62e13e19bcb8d4b354d9197ef5a4e3a8c7a6116d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.0 MB (98011832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36bafc2c692cd7d93b639bf5efa7a730ced975fd0a15ad8f71cba01e8c59b716`
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
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03900f2fdf5974424bfd298551b0e62da0045dd4710d9615492752026efcb4f5`  
		Last Modified: Thu, 08 May 2025 17:36:33 GMT  
		Size: 11.0 MB (10990957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1efdcfee37ba889d2ad71993cf205f4b2dc389a010af39dbdb021d9dbe7eb43c`  
		Last Modified: Thu, 08 May 2025 17:36:46 GMT  
		Size: 61.0 MB (61043214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:focal-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2d756e1cdcdc69d5c6ba06f13568c9c9dd7ba6385e04bfbe54a67365198e34c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6679871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7a658cb4e5f964822ddbecf8a6be1141313449e9d3bc80fe67ccd6fa10079f9`

```dockerfile
```

-	Layers:
	-	`sha256:a7083bfe8f09eab5fbcb651bc3e631660494394420efbe5487b20316db8e9fa0`  
		Last Modified: Wed, 09 Apr 2025 13:57:06 GMT  
		Size: 6.7 MB (6672409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c00175b35541c641aa739fbe201c3ab53447709b26a14bca62c4f4d4a9ad35d3`  
		Last Modified: Wed, 09 Apr 2025 13:57:05 GMT  
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
		Last Modified: Thu, 08 May 2025 21:39:31 GMT  
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
		Last Modified: Thu, 08 May 2025 19:47:37 GMT  
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
