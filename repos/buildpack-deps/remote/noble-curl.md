## `buildpack-deps:noble-curl`

```console
$ docker pull buildpack-deps@sha256:7903921918f19a097c6bb9b671653975f41607ab45f278d21b0c7aa1af2ab1c9
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

### `buildpack-deps:noble-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:a345a08bfb88e663d9d4d0b61dcbb0c4c66997c876f92edd5db9ff654b908249
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.4 MB (43364481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:480880658774d7eed305cbc7b23326df573fb3f979f9a8a1746d7fbdb7d5de60`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:11:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450086accc6bf61159108eda83fd8a98ffb3d28b7b751cdd690a270df67a3fd1`  
		Last Modified: Tue, 02 Jun 2026 08:11:15 GMT  
		Size: 13.6 MB (13631676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c59d4b26aaa478125acee0651a197ae70295feb5bc58ac19948ec38ed89ee3cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2614769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff0d5771bd0ae733b10eb971460cc7966d1028777f0a35b9ea042bebda1e77fe`

```dockerfile
```

-	Layers:
	-	`sha256:3123bc7afeb4bdcc212717a1c47b6fe6d8aa976ca86121f13cd924952645d7fa`  
		Last Modified: Tue, 02 Jun 2026 08:11:15 GMT  
		Size: 2.6 MB (2607855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15dc29556c420e5d741392e7f6595f8ff51eb8faa4cc0ac70bc1fb2aa593d2a8`  
		Last Modified: Tue, 02 Jun 2026 08:11:15 GMT  
		Size: 6.9 KB (6914 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:217378fad243b656e2cb57fd09908d181c34e2e299b543d3d6ce833d2f3adcf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39648634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f07a98b0ee4100ffb38ca3a9c60809356a9b05254e20142f12852d757e7fc068`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 20 May 2026 01:36:59 GMT
ARG RELEASE
# Wed, 20 May 2026 01:36:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:36:59 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:02 GMT
ADD file:6d117ff682b1d31146902ad551197b012e75561d62d92d029219fcbf5c493c35 in / 
# Wed, 20 May 2026 01:37:02 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:09:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a2dede8d0e9ca179460cb274dab10c5c4b741cf1544b130df872809a4467e3e4`  
		Last Modified: Wed, 20 May 2026 02:15:37 GMT  
		Size: 26.9 MB (26859709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b118b4a0c6ca2ad4f0b7d3f4e7f824e209e719825c9725ce8c175f943f51da2e`  
		Last Modified: Tue, 02 Jun 2026 08:09:35 GMT  
		Size: 12.8 MB (12788925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d921e9667cedb1b12e4e6581137e84ee7a276187ce1d81046efb0155e8236cfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2617139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8e7cd339e02f7b74335ecb2d5c05add657373e3a8e2e15c05e316c1e1a48f17`

```dockerfile
```

-	Layers:
	-	`sha256:ecf0308297fa08e4ef3c318f03f83f72e32c08c1ad9b9296defae9987b9c3b4f`  
		Last Modified: Tue, 02 Jun 2026 08:09:35 GMT  
		Size: 2.6 MB (2610159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3045fe1af7e7b6aed872b6c3462b6074fd89fd68327b76adce6bfaecd86a0e38`  
		Last Modified: Tue, 02 Jun 2026 08:09:35 GMT  
		Size: 7.0 KB (6980 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:4fdd715a74a3be40ef28f7594a7560afe86d0d2c588fe1343e45318948a7de65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42342964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f6bb9920ccb73b982afcd15e305e3be2ce05f3f40ebf7ce0253121ad848eccd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:11:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b224b62323017769a142e9665ce9c8ea5728f289ccf479c861e9809bad5d8376`  
		Last Modified: Tue, 02 Jun 2026 08:11:26 GMT  
		Size: 13.5 MB (13466558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fce4261b03f118e0b74db81fa377ec631fc0f70b614970e3b99651e17947dbc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2615908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90e1430fc2024f34914b702d1099fe30ffa63468cc6bd48899f767dc7e1d1629`

```dockerfile
```

-	Layers:
	-	`sha256:e87c285d152f54c8d46ef663d08085d8f840db94e9253578089cf66aed66a9e5`  
		Last Modified: Tue, 02 Jun 2026 08:11:26 GMT  
		Size: 2.6 MB (2608913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36a204d3abe547b55a3527b1c864284468b4cef4047966c42d711f2e572cab6a`  
		Last Modified: Tue, 02 Jun 2026 08:11:26 GMT  
		Size: 7.0 KB (6995 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:00823566e562a9d6ed56f5e4b68b5dba8b09dd6023249268e273e787bf410f4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50276005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b7c68de5c760eb6f4cf4c5ecbd9a892e6a3b70a7abc4723daa6b34f1bbd75e4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:26 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:26 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:29 GMT
ADD file:25dad72762cb0d82bbf57f17b8713b1ca4d35e813d99be37e61090f10acd5d92 in / 
# Wed, 20 May 2026 01:37:30 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:10:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e091f822489caa06bb3d2fde38646b1d65be890bc1155c44ed55dc18ce539afc`  
		Last Modified: Wed, 20 May 2026 02:15:44 GMT  
		Size: 34.3 MB (34314099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:187aeb2a9889fd701a0c7ee32834f3636fe8324b6c4bdb83baad19d7d389c281`  
		Last Modified: Tue, 02 Jun 2026 08:10:22 GMT  
		Size: 16.0 MB (15961906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1f25b41568d23dfcd85710cd41720c3d54700a5ba5272ce3f0ed6ed15227ba63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2619422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beacc54be7833048976856c46fbbfeda9893a89ff54285d8005b2b058994cf5d`

```dockerfile
```

-	Layers:
	-	`sha256:d2e0f819e39021be65e63d3d50d05ccc7f67f26273b59de044fd46a1d36f87d4`  
		Last Modified: Tue, 02 Jun 2026 08:10:21 GMT  
		Size: 2.6 MB (2612474 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92bc37c6de95392cbc22a5b77b35d227f4e90a30d893fe720d166e07051658ad`  
		Last Modified: Tue, 02 Jun 2026 08:10:21 GMT  
		Size: 6.9 KB (6948 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:b526a0583254061a9ec0c844047175c9bde972a0e9de1d493950cfdf1478bf81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45302031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ada55b98ebdd1a6c9ea56c4e083562b6215d3d2d51d5295a3399c854ee61abd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:24:05 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:24:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:24:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 09:24:43 GMT
ADD file:a9a4679e3df2846468311b83a8f6ab86f5a205bab966d3f236c9f30151010c5b in / 
# Fri, 10 Apr 2026 09:24:47 GMT
CMD ["/bin/bash"]
# Thu, 16 Apr 2026 16:43:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a7f0c74374451005259fe6b1b7ef3185055f2b6c419b5ba0ae8e4f55b1e1c31d`  
		Last Modified: Fri, 10 Apr 2026 09:34:45 GMT  
		Size: 31.0 MB (30965327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d138f08afae4216480b287afd5e7c2f6ebaea6563724878d446b7f725740d7`  
		Last Modified: Thu, 16 Apr 2026 16:44:25 GMT  
		Size: 14.3 MB (14336704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1830d242710808b7667b664ac6a42c9a0faf0751ef401bd526fe904551dcb3e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2608683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7847c88a9e935e506775c58aeccf1f57041b6eb3c19a5e94274e8597e0282d30`

```dockerfile
```

-	Layers:
	-	`sha256:a1060816b57683c27fc0703085a2a842d3bb4899d8cf50b0be3bbb66f700f952`  
		Last Modified: Thu, 16 Apr 2026 16:44:24 GMT  
		Size: 2.6 MB (2601736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77fbdca987cd88d91ecb0d17f42cd8bc9998090fc19c7117224b38877dedb373`  
		Last Modified: Thu, 16 Apr 2026 16:44:23 GMT  
		Size: 6.9 KB (6947 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:898bc65d4af813ce3a04941eeaa7a57488d6a451c2be6723d36a682656b3ad28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44857438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88b05b50a30cccc62b16381cb59566951051765ab4e4f51100231e97fd9aced1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:09 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:09 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:11 GMT
ADD file:b574b1e436c2db4e4d66f69c75e47a9aebf0da1ad375147eb2c0b7ff76c6ab7e in / 
# Wed, 20 May 2026 01:37:11 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:10:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c8ebd0a624851e8502e41ee64db2b6a45537554969784d82ebbc91c905cbc2ef`  
		Last Modified: Wed, 20 May 2026 02:16:00 GMT  
		Size: 29.9 MB (29912835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:591d53e14180df305f0fe02c9303d41b73a2de4393458677c78c708d80d4d6eb`  
		Last Modified: Tue, 02 Jun 2026 08:10:13 GMT  
		Size: 14.9 MB (14944603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7059f9ea8fa89101de1d54029a9bf5758afebc900b9d7d93efbdecc077eb80da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2617596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38b093bb44091b600de0f79b6c5e3adf8a5dd7141067c31d9f158c9d08ece99a`

```dockerfile
```

-	Layers:
	-	`sha256:963baf0b2d173666c783d310b8e4b9910f8548dde4bd9d464890c3d3e41c67f1`  
		Last Modified: Tue, 02 Jun 2026 08:10:13 GMT  
		Size: 2.6 MB (2610680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa5bd90e9b145c0f75ffd4cb57de5127601ee8a349616b94e3f77275455bb0af`  
		Last Modified: Tue, 02 Jun 2026 08:10:13 GMT  
		Size: 6.9 KB (6916 bytes)  
		MIME: application/vnd.in-toto+json
