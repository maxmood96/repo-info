## `buildpack-deps:noble-scm`

```console
$ docker pull buildpack-deps@sha256:3c8cdb4adf08f60cdcf4b73579a8e27b6638d5f7e495792c328e31691fdf6ea1
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

### `buildpack-deps:noble-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:639ff8ac40f76f4a17add5c702e2d4f962b4b1bd3cec9b1598b40fb6640fe9af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88701175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bdaf6dd5a2b245007d723e4716b14c998aafe8a0b8b924a6990140c954ce76b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 01:47:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 02:43:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87036178ad86a6ffffd0bfbc6472da5aebf31ed69c5b3f17251ddb308c41f20`  
		Last Modified: Tue, 07 Apr 2026 01:47:22 GMT  
		Size: 13.6 MB (13631344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30eaef83111d329f083aafe369304809b4c6d4f05a8d9cabbe3c275dee19dc18`  
		Last Modified: Tue, 07 Apr 2026 02:43:40 GMT  
		Size: 45.3 MB (45336372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3fc38fbc970958d982cd775287cf841f4b80a37fa26b6240d80d45b0f35b37ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5281883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ee4a6d816da3359c9c90858d9ac556f165e8149255ec7ca99fe100ab14a89c7`

```dockerfile
```

-	Layers:
	-	`sha256:c5c7acc3dc5bf27fad264d2b6b5b700330df270c5d802df3127099f982a41f20`  
		Last Modified: Tue, 07 Apr 2026 02:43:38 GMT  
		Size: 5.3 MB (5274622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c56558fabd13f1a8261ee56a45ddd3cf6dacb776bfc76fda84bcd29d0b1a8f18`  
		Last Modified: Tue, 07 Apr 2026 02:43:38 GMT  
		Size: 7.3 KB (7261 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:4fbaab1e7a07a258315065e9dd073f828b6b4316e5c80d1164a961491373659b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 MB (88522043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a5fdb65e8de4fe8d644588a2630301465a1b81d40bb18350c069c197c7d8b9b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:14:30 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:14:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:14:31 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:14:34 GMT
ADD file:68e3febb1e8418fa8ce83073bfbf6ec7236d81e7c8781177d7295e5adce34436 in / 
# Fri, 03 Apr 2026 15:14:34 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:02:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 03:49:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d7d21bc3f0364f0d98c41b0bcda87b8f2bfbf1688f75f6322ed679752a149163`  
		Last Modified: Fri, 03 Apr 2026 15:56:43 GMT  
		Size: 26.9 MB (26858365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae0da5755f16317e3ae70ab41f8cfd9bfaf9ebcfc807f501bfdf9301feb5834d`  
		Last Modified: Tue, 07 Apr 2026 02:02:19 GMT  
		Size: 12.8 MB (12788637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c02927550b435a954ad1bc7a94f1e70f5a5ffb07a1e0b6927f1936cd876cef`  
		Last Modified: Tue, 07 Apr 2026 03:50:05 GMT  
		Size: 48.9 MB (48875041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1d05b86642bda69220e27c6205ec2f6472d97402325affd4bb490b629bfb71cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5283246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5cbd90f154606def1a426c140aa4f50319e1b717c0eedda90ebadcfe5651e39`

```dockerfile
```

-	Layers:
	-	`sha256:6b308271b3bbf8f1dbc38bc2cea812e9a31adfa439602bfb891c896307d59db4`  
		Last Modified: Tue, 07 Apr 2026 03:50:04 GMT  
		Size: 5.3 MB (5275920 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49038335216f69039c22ca440a4b8a2814034faeae075913666534ab8ac9f0f9`  
		Last Modified: Tue, 07 Apr 2026 03:50:03 GMT  
		Size: 7.3 KB (7326 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:a317103f80e16d966f3f1bc7c4391cc8a6bdcd6efdca2f63f832ced777e1a77f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.6 MB (87613543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9de7e25b30b31e28279c050d4d8d74a4dd14686bd8a7a89ad7f775cd00b860c3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 01:50:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 02:54:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:250898647707f5617f944580836cdb26a429f5b2583cfefd84515874dcc57a45`  
		Last Modified: Tue, 07 Apr 2026 01:50:30 GMT  
		Size: 13.5 MB (13466018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759b38b74bc437a0488655af47936530d492f5f32fd7af8351b6fd1460780a14`  
		Last Modified: Tue, 07 Apr 2026 02:54:16 GMT  
		Size: 45.3 MB (45273450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a8343811b94bc6b0b217a2f62a53cdd29a53a4386c139526b077c0783a9508b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5289156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e4b1a164a9486e921715f27f01d7e408145368a3baba64be0a3c6752fb34dfc`

```dockerfile
```

-	Layers:
	-	`sha256:4dd97c2691cfd42aba2b520947e65f80e12af6ec28cf6c5c3cd4828209a8a27b`  
		Last Modified: Tue, 07 Apr 2026 02:54:15 GMT  
		Size: 5.3 MB (5281814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bd55bf8c3ee3d84cc7fe07a9a083a65dfe64001b77554b695e7ff0be44e0445`  
		Last Modified: Tue, 07 Apr 2026 02:54:15 GMT  
		Size: 7.3 KB (7342 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:87fc831fc1768ad7a569be42fc66202fdf99d28da7c48515c8542b298891976c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.7 MB (100716465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b600b36b0ccbb8e32679bc5f3eb020c9e7614ca3f4822e982f4a1fd1f7598c31`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:25 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:26 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:29 GMT
ADD file:ede7e3b047d459e8abfd20afae677192c0eab70c709496e87b2110289bfb5f3c in / 
# Fri, 03 Apr 2026 15:15:29 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 04:24:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 09:56:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2206a81f65df3147f8c62d4c01c47495515dae16f93ce6845cd7cdacdd206f1e`  
		Last Modified: Fri, 03 Apr 2026 15:56:51 GMT  
		Size: 34.3 MB (34313334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68f8c8315ff69e0ade5c27a5f32668c5ece93dfdbd029e67d7b478a2a133a289`  
		Last Modified: Tue, 07 Apr 2026 04:25:12 GMT  
		Size: 16.0 MB (15960385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d81007fb33e08eb5e24180ed20968c7c036bc484af1aeddba776ca581f9b36b3`  
		Last Modified: Tue, 07 Apr 2026 09:57:04 GMT  
		Size: 50.4 MB (50442746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d7670a4231c0deddc5eb1fa18a2abc57e2015ee27c88ea9d3c85faf9704a3ffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5289768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c23296991b22d4aa063c8bc0196bb8fb5ce51005c7f3854736455f962fbfda21`

```dockerfile
```

-	Layers:
	-	`sha256:7df89b5c5530084910364f58d291a46b58237cbc87c133ebc5ddd676b48b5d6e`  
		Last Modified: Tue, 07 Apr 2026 09:57:03 GMT  
		Size: 5.3 MB (5282476 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3183690815075838a7d894e7c4779b3c1851fcea95f38f79869eb6deee7f8c04`  
		Last Modified: Tue, 07 Apr 2026 09:57:02 GMT  
		Size: 7.3 KB (7292 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:81ccb86e17a410fc4f838bd35135e4780f2345968e6b6c7c03ff3b511d8fddbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101292606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:560be37159e0c58d3eb7885459c25ba22bbc484443a4f0f872cfa7d2077e5f85`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:35:32 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:35:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:35:33 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:36:09 GMT
ADD file:59e78909d1b1cd9a524f68d8ff44bb077ea09f4f39da5e046d635b48da9d33bf in / 
# Fri, 03 Apr 2026 15:36:13 GMT
CMD ["/bin/bash"]
# Thu, 09 Apr 2026 01:53:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Sat, 11 Apr 2026 03:05:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:23ef52cbd4674ce4f8269086177a6a1fc3abbc052567212551b8169743067808`  
		Last Modified: Fri, 03 Apr 2026 15:56:59 GMT  
		Size: 31.0 MB (30963791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f90ac4813ec6bbeb96b9ca1324f326cb79250eaeb56ecd108a3a0d03888dc3`  
		Last Modified: Thu, 09 Apr 2026 01:54:59 GMT  
		Size: 16.4 MB (16443158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:458c23f88fd80cd62b142ca8ede0942ed13340c22bab3bade167a2b7ad9289ef`  
		Last Modified: Sat, 11 Apr 2026 03:07:53 GMT  
		Size: 53.9 MB (53885657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c7f739ea05732d8e9c1777c0487c4fa8fd1d9370bb64c0b5cfee42943c957acd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5272312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaac9327e271ff4b74456bd1fc5d8445a320fc101e90535cfda1078eeb5dc3e1`

```dockerfile
```

-	Layers:
	-	`sha256:36970915303d81db363a43589d9ad1781c8af01e233c02e86ed52a4322ab631c`  
		Last Modified: Sat, 11 Apr 2026 03:07:46 GMT  
		Size: 5.3 MB (5265018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5170b9abf30cb1a46d3d8de9d55a75f016a98eb0d957a3103876e0f0a1251f06`  
		Last Modified: Sat, 11 Apr 2026 03:07:45 GMT  
		Size: 7.3 KB (7294 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:9c98afa71063a0f4e608a56812150ea0c14d89288fde2150620f522679f22eb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.7 MB (91677828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d89084f62040166a8c2277b4c94e8c14653ceb404b62e641922f20bc897f84b8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:12:46 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:12:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:12:46 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:12:48 GMT
ADD file:31d45a66208318e1066130bac8975f44dea6e7e93cbfb2d29b0888e686bb10d5 in / 
# Fri, 03 Apr 2026 15:12:48 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 03:06:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 04:55:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:248eeda3355e38b5891b7f407370b5faea53785cd947438684bf34a757d0f83c`  
		Last Modified: Fri, 03 Apr 2026 15:57:06 GMT  
		Size: 29.9 MB (29911843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cbc7b0e0dfda4f493fc8f104984fbea17a2f5d7d1345c3463d92d4acdb49dc8`  
		Last Modified: Tue, 07 Apr 2026 03:06:17 GMT  
		Size: 14.9 MB (14943206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd585f62eae2a6c89da020ab0ed29d752cd73be02dae049a068a3e8979f2970`  
		Last Modified: Tue, 07 Apr 2026 04:56:16 GMT  
		Size: 46.8 MB (46822779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b7651db169fe5458a5893d91ac0081191448beebbeb93c156b22437041a54c49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5284216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cc48de786900c4cb8065793bf6bad61a61ea1578b6f1cd2906cbd31313fb336`

```dockerfile
```

-	Layers:
	-	`sha256:2e1fdad410038f0a6014081ae297d233e712db83872db49d7150239d2f27a53a`  
		Last Modified: Tue, 07 Apr 2026 04:56:15 GMT  
		Size: 5.3 MB (5276954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf4d4a4f38944c582f4d3bcb3f114259a1cb4c6b2c010a6c9d213f71dbd819a9`  
		Last Modified: Tue, 07 Apr 2026 04:56:15 GMT  
		Size: 7.3 KB (7262 bytes)  
		MIME: application/vnd.in-toto+json
