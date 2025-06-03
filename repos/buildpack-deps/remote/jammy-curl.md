## `buildpack-deps:jammy-curl`

```console
$ docker pull buildpack-deps@sha256:860ebe9ff5b69329b30fc3be51060cc1a36148f68458726e884dc13d548b11f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:jammy-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:8aa53e4af6265e66975936493b886e169fdd33c3d9bb2e00a16f3605a25377a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 MB (36636254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3b4b35b4127f1d205752b49d9458fd6ff5db0250df9aeab06c86e7b2dce6e04`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e524470d282633f4218fb18055b7a6aa7285ad735cc3f9ab2e51f1a3e8d068`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 7.1 MB (7103251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:71d8ad0945ed1986b6e60ca4f829f24615a59e0b6b5a53c504b9365cd84f14bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3083483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e017e7bd9bcfca8be3ea752d381f5d1968950ffeee27e64beb5c2768b48194`

```dockerfile
```

-	Layers:
	-	`sha256:e84b4cd5194f8333e5816dcfa5994eb68816a45220a8261be78b6a8f55647971`  
		Last Modified: Tue, 03 Jun 2025 04:15:38 GMT  
		Size: 3.1 MB (3076561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cee4743b2924fb9d3c630b5c88df132609f097591394026dd28013b6b6168d69`  
		Last Modified: Tue, 03 Jun 2025 04:15:38 GMT  
		Size: 6.9 KB (6922 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:f0bdc34da79fd92c6ed228f40c9d3a9e06c9d18b893078d106d19b3b524d244a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.6 MB (33648136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1fda1d56af9b61da7250025d4c471ff4dbd03f0e45aa8911f3d3a7688409aef`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:a68d8d0994670732edac30efcee96eec3850856e5c33c1c7fee7fdc59173ac3d in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f35c50ead1843adba7d4d13281d31bc17c201a55b8bd1a3961e1bcfd131b762d`  
		Last Modified: Tue, 03 Jun 2025 13:42:56 GMT  
		Size: 26.6 MB (26640475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ade18f0cb153eb0e80505edf909a0b5fb573468108f73d59398826c27dd2252`  
		Last Modified: Tue, 03 Jun 2025 17:26:26 GMT  
		Size: 7.0 MB (7007661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a675317bbde51a07f19ea4c5dcdc97c5a736507e4cf2f7d465131a6f268a363c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3085852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed6652d7ff6d701046aec5b11332715d81aed75253426a64deb3bcefefff6ad6`

```dockerfile
```

-	Layers:
	-	`sha256:a37257fb22a321dee92adb3332e60fb6ddc4f6635b8c9e6fd795a6bf130b087c`  
		Last Modified: Tue, 03 Jun 2025 04:15:34 GMT  
		Size: 3.1 MB (3078868 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f1efd7f3e66897ac6c4c5c6c930a21539ee3f3910866d4359f3da869c6e1261`  
		Last Modified: Tue, 03 Jun 2025 04:15:33 GMT  
		Size: 7.0 KB (6984 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f7bb22815d26d65707f9b2267ae604e5248b230882583c4006438144c9c7c256
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.4 MB (34404654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:129ea5a4fb2408b801168dd5f026d250f0bb726ad7ba0d72431c7b9ba4b21278`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfc8f9e3619942200ecbccd8a285496c9f5f75c9e60a1de3a2f4dc84b79a25af`  
		Last Modified: Tue, 03 Jun 2025 13:35:49 GMT  
		Size: 7.0 MB (7049073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:78e58c2767e4383c106f37dbf65973978c1946cd2458aff9d8cb775611b6a3e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3083832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc780d13a01f5763336aca170ba5c066214aa5cbbbcdb3123402e41c355642c0`

```dockerfile
```

-	Layers:
	-	`sha256:d3fbb0e1d7532461953778ee7312af9e6052be33e01fe2ab88414e5bdfb75ffc`  
		Last Modified: Tue, 03 Jun 2025 04:17:10 GMT  
		Size: 3.1 MB (3076828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e9440d982306a0dd067dbcc0313e22adb3f3452fca8393ea01b750647ae0259`  
		Last Modified: Tue, 03 Jun 2025 04:17:10 GMT  
		Size: 7.0 KB (7004 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:8127911a3fc6d5376a797a0c21aa17c2d0849ff3a401ec6451bf115cfe7e2997
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.6 MB (42621418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96a82a616f33d1f16b8e8f5fc0c9a14a166e4c8ed5700f4a4eae06149f6cce38`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:ff7ae346164d0b3da702390fb0f6f4187ba164036794a6081fdf0f9817b59053 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9b728b0b1adf8a1b191ffc8bfd1fbfbb2bc25a989db32698511ae9a36f8b82a7`  
		Last Modified: Tue, 03 Jun 2025 13:34:58 GMT  
		Size: 34.4 MB (34440357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f199bc4ad98d2856395093db736f7cee937c730bb3d218bbf267319ae0f77073`  
		Last Modified: Tue, 03 Jun 2025 15:23:17 GMT  
		Size: 8.2 MB (8181061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:175fd5f00f480b613963b265792f99b02a1239c5f67c0cf9ffbef65530b5dd44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3088153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:272a6d557b897181c960d867814c080f4737c4dcaec4708aa88838f29683922b`

```dockerfile
```

-	Layers:
	-	`sha256:4754e62641918898e784aa67f23ee31d7039402bae2e438d03ecf36ef96ba613`  
		Last Modified: Tue, 03 Jun 2025 04:16:14 GMT  
		Size: 3.1 MB (3081197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd7a7542eceee19063fd49e8865f4532a31860efdf4bc582072b7e1493c84621`  
		Last Modified: Tue, 03 Jun 2025 04:16:13 GMT  
		Size: 7.0 KB (6956 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:bcb87ae63473ef1ee1f6856f75df56eb2badb1eb5048932309573ede2de87621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 MB (34154794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:586b5c3df2f623503fb586891b32c608c7c6586c129bf1191ab341ca3a219cc6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:805054292411bfacf95662e1995adf90eef5abc97c604865fe65b213d7b41a1d in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:37769df37bf710dfefa24b110325d4a7bc5e0c1af364d18ad2da15a09b327dde`  
		Last Modified: Tue, 03 Jun 2025 13:32:31 GMT  
		Size: 27.0 MB (27038448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03983569ea2a2387b0d1cda89603d34e38695b0e017dd4a2109d9c8e42ba2191`  
		Last Modified: Tue, 03 Jun 2025 17:26:49 GMT  
		Size: 7.1 MB (7116346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:546ac053f980bcad999aed389a16b8e82e8d60f85c078b3776e90ec295822f03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3077405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:714deaed3b634d3cb5f21575dc57f8ab8b5fa8001c110facff64c9d7101df8cb`

```dockerfile
```

-	Layers:
	-	`sha256:06294deb2484d7b5a74592fdc6a864e41bcf848507578002050f076a39e7b5eb`  
		Last Modified: Tue, 03 Jun 2025 04:17:50 GMT  
		Size: 3.1 MB (3070449 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:399330ab45f80dbd1fcab869e3b9194d4695d0fd046f09c89f178cd1f04b005e`  
		Last Modified: Tue, 03 Jun 2025 04:17:50 GMT  
		Size: 7.0 KB (6956 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:3fe2ce5faca3a9658efa9bb0f3164379ebbd78a561469a1f4d90d5d5586da4d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 MB (35014714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c21ab896881d2d309111eaacdb04ca82969d6fb97aae97d21dd259a3a008459`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:f153a831e3d8b37cf290a0e64d208348b0231dc123ac8127decb555f982fe306 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cfa1809998a055f097abf4f27759694a126f64b86912d130052f49642e2be80b`  
		Last Modified: Tue, 03 Jun 2025 13:35:34 GMT  
		Size: 28.0 MB (28000600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d72f21f5960e611ba62223730c2365f458813d47dda4f15dd2001615e7599f`  
		Last Modified: Tue, 03 Jun 2025 15:23:17 GMT  
		Size: 7.0 MB (7014114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:dcac6981572960b85875a823a5867acb43858e1412e747a424b29478cfe0b200
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3085702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:753d279597a3428e8ce1a2c7c2c06d438e2a0bd9907a65b41534b2ffff9b6719`

```dockerfile
```

-	Layers:
	-	`sha256:625f0861579f84e4a26e161c306420c59792b0fdd690c409aac7ff3831e7dd51`  
		Last Modified: Tue, 03 Jun 2025 04:16:02 GMT  
		Size: 3.1 MB (3078778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b2d84bb050348b74769f62013e7aebc8592f802edac578ef583af8505c191dc`  
		Last Modified: Tue, 03 Jun 2025 04:16:02 GMT  
		Size: 6.9 KB (6924 bytes)  
		MIME: application/vnd.in-toto+json
