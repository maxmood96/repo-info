## `buildpack-deps:noble-scm`

```console
$ docker pull buildpack-deps@sha256:4497b298132f5f9d606707e9744de523bc02ea3c24255bd8f28d90321210133d
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
$ docker pull buildpack-deps@sha256:6da6921cd43b7e2c1880b1841de27df5b237e25f37f2e7c4e7d245a78922473d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91173419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe77423028536f8fc8fba1790db7cf657a0039eb476b5783849caa256b2e31b0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:affcf24932dff649e2aba4f579c169f460375d428c50fcb251e53f98e4c30fc1`  
		Last Modified: Thu, 02 Oct 2025 04:52:18 GMT  
		Size: 16.0 MB (16023985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36dce96fa7416b8a57d7a219addbb30cf4c5868e9d6e1846e5cb7f9d6c3bb25`  
		Last Modified: Thu, 02 Oct 2025 08:26:05 GMT  
		Size: 45.4 MB (45426423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ffc971e57f212649d6321db293d9b0d664e3abec8a1f62bb6f069759ccbf04c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5281878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e77a845581a75f76d6e2782c3c7d2c0072013f2fdfcb154514db42b2281e568d`

```dockerfile
```

-	Layers:
	-	`sha256:acd15bc68e6dba344959a70f6fc410c7ace5a2d0daac1261b2a1005017f5bb3e`  
		Last Modified: Thu, 02 Oct 2025 10:19:27 GMT  
		Size: 5.3 MB (5274574 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c4615252701a818031728b1c335b076a45b0a93c83d7b46dc3c3de5ba8a5e1d`  
		Last Modified: Thu, 02 Oct 2025 10:19:28 GMT  
		Size: 7.3 KB (7304 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:12fa25f1eb4b62fde4f7470b3d01de5c2e196f27dc0fc5549f925f49b89d7a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.3 MB (90285657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f88e441df46233f5172ba4ef35682117f9f264dccfd9ed8190b055c129dbad82`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:51076814e2aa1389d29f1b4c38eee0cfbb1d321f099c50e09b19452198f65032 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6c9f3e8be363989d138b8e3a1316487da5ee2b8384d3c6b0f9b1a8290f57caff`  
		Last Modified: Tue, 30 Sep 2025 17:07:34 GMT  
		Size: 26.9 MB (26851149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82f18ea7fe9ef4178a0e236f41c554cead30170db066c48450b074df4ca534de`  
		Last Modified: Thu, 02 Oct 2025 01:11:12 GMT  
		Size: 14.6 MB (14569242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42003d15858f39d12322fbbb59f088f0569c5114141a064f9292c6ad7172be08`  
		Last Modified: Thu, 02 Oct 2025 02:14:57 GMT  
		Size: 48.9 MB (48865266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4488cbe1e0d88eaaff10358b35d7032769eab49522d5ab6eb227f33f62e0d8c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5283241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34f4e86d416829509a575c7891076a04a688943469346df19c599b3db4a062a8`

```dockerfile
```

-	Layers:
	-	`sha256:f35eb704f4e29baf7058ffa573d98fbd7e3b2fc8417b1d5adeb14fdddb0ca06e`  
		Last Modified: Thu, 02 Oct 2025 04:20:19 GMT  
		Size: 5.3 MB (5275872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb1fdda32d7a683fdb01ef5cbc13a78a415436be37c1add75375dcac0dbb6278`  
		Last Modified: Thu, 02 Oct 2025 04:20:20 GMT  
		Size: 7.4 KB (7369 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:231ed61e327d48f5ce013027d0b43e731735878dc43f28f7847fb03ee761c7cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89814825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c26068a62cc425330ebcd70afdffe51713215453c2e9914b29b46ffb9d2e71e2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88d4e5eb6699d3808078595f32cffad010cd267cf16038b9e1601e8ec9e37f7a`  
		Last Modified: Thu, 02 Oct 2025 02:14:19 GMT  
		Size: 15.7 MB (15678855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d578c8855badadeef1e8e1ad0e071290f9fbc8be7677300cee994d8861223e9`  
		Last Modified: Thu, 02 Oct 2025 02:15:01 GMT  
		Size: 45.3 MB (45274395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7c013fdd84e137916b491445240364921798c5fbbd5cae7a73c15e07d493c9c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5289151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:784556e9eb84306148b0c46811394b07a993ee240927a1293c91d9485288b746`

```dockerfile
```

-	Layers:
	-	`sha256:bb7f31d3f3b6a28ca89936c9308cf94c106c8edd08a969ae3f2ac6b5f1175b7d`  
		Last Modified: Thu, 02 Oct 2025 04:20:26 GMT  
		Size: 5.3 MB (5281766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:660a60e462fce17878a01692f0272359b03c76cf3d4ecf251bec28eeb0ab3fc8`  
		Last Modified: Thu, 02 Oct 2025 04:20:27 GMT  
		Size: 7.4 KB (7385 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:0fb7ae74cf1cab178aecf0f5f64dc04fd089d78620e5f440a8fd88f7b5447dad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.2 MB (103218487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:599d6734da96dd586c58714f42c7d7a9971d518dba48429fb6c53b07b6be00d9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:c654664ccaf1c501c787c924fddcfab7f9cdc324325d45748f97ee6d5ad63cec in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:15a6b79c4fd2f3417787ba4c0a8161183cf898454880102c719eb0c91671c218`  
		Last Modified: Tue, 30 Sep 2025 17:28:16 GMT  
		Size: 34.3 MB (34303547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32831262c9ed2d0082fc94e452de326736750e57be1861993e55b6c43bc96061`  
		Last Modified: Thu, 02 Oct 2025 01:12:58 GMT  
		Size: 18.6 MB (18574976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f54436de24358c986f80df683327e624c83c2566b8df8570538895b1d1d8d910`  
		Last Modified: Thu, 02 Oct 2025 05:01:08 GMT  
		Size: 50.3 MB (50339964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6f1518d27212519bdfd1da28b0d58979fa87ff6e377fb0e1ec67288d182b9103
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5289765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5223fc1a9dfaa3443d1ee671a65d7c2ce7bddbbb69730e9d4c3a21e312b0a822`

```dockerfile
```

-	Layers:
	-	`sha256:85ed409af8c12309bce34fa6f6e2884fea42e0212a6b8013703f404db1ec58ea`  
		Last Modified: Thu, 02 Oct 2025 07:19:56 GMT  
		Size: 5.3 MB (5282428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8dd48023e8a2c5753d4fa6b46e09e577f26caaa9eef2815b36d53eddd779dea`  
		Last Modified: Thu, 02 Oct 2025 07:19:57 GMT  
		Size: 7.3 KB (7337 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:cd2af051fa2f27ce1fe4ebe86b4edf16f36bae36e6aeb1c11b430aaaff21eb4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99157059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adae51d49d60c7a8e0f79c68df250990133598d346e8dbfe3b4abc28e3d589d9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:58fbc6777cd47d1e58396e2c0f70255ae3bd63d0ac2ea2138ed6e5e91fdd70b1 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:fc46b4719a7bc0e446bd2b472a339bdca3990f164daf9dde3e710206f93383d0`  
		Last Modified: Tue, 16 Sep 2025 19:54:09 GMT  
		Size: 31.0 MB (30950703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ef5352f27f8eaa4912970c5e40c708ff8676d4d3b32b568f91c0697ef0d269`  
		Last Modified: Wed, 17 Sep 2025 10:13:49 GMT  
		Size: 14.3 MB (14330275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c60c4f66e23d52d21fc7f3dc5c91cd17568df06d10b745951ee901f9d3229d`  
		Last Modified: Wed, 17 Sep 2025 13:34:45 GMT  
		Size: 53.9 MB (53876081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ccc77511e60d7ee408ad1522c3ab368f9af1979d4fada6e45c4c9fe707e22077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5272307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5187806a83feeff598abe92f20cde5320c30ac60308265f34cbde71e06a51c72`

```dockerfile
```

-	Layers:
	-	`sha256:b93099144546662ddece1659e22623054876482b71477d893edef3e0944fa748`  
		Last Modified: Wed, 17 Sep 2025 16:19:40 GMT  
		Size: 5.3 MB (5264970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fee40da18d1723f70b3e0b753ba8e0e783ccbe22031ae7dee77c11b0d38d2adb`  
		Last Modified: Wed, 17 Sep 2025 16:19:41 GMT  
		Size: 7.3 KB (7337 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:29d54e9f05fbbf5d68368de28c9977b3ae8b022fe39f62374abeaf3bdf1f43a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93679859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b0bbace26f05997238d696e929026db41f94b94a6d967654de7c653c2110ecb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:2df9e8bc7cd2e879b1bb1d4b43960e570cf8bf039e9c92e1b3599d2ec12b6674 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e9a7df0c6e08fd0434347bd07ecdade7cc5d006c086084ec4347cd24546ee1a5`  
		Last Modified: Tue, 30 Sep 2025 17:14:38 GMT  
		Size: 29.9 MB (29906146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afbcef77789b132db9a078a6302fcd340d67c834cc1c5a667cfffc3377db3882`  
		Last Modified: Thu, 02 Oct 2025 01:12:01 GMT  
		Size: 17.0 MB (17026854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23daf2b9224fce2c79e8979b00f4f503fe59502e9808135d3feefab2b5c4f67`  
		Last Modified: Thu, 02 Oct 2025 02:40:59 GMT  
		Size: 46.7 MB (46746859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ca3bb0ee0e372f8350f16c05349be23e07a773d4dc18b7ed89898d889a1b0892
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5284211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bfd8ce2f77bf8e441ea7e587d17f42d0f1f359ad3fa09652fff965b73574660`

```dockerfile
```

-	Layers:
	-	`sha256:098826c5042e9aee58c07fcd70f8e84b96560e49c9cfe8109dab90090b39cc61`  
		Last Modified: Thu, 02 Oct 2025 04:20:41 GMT  
		Size: 5.3 MB (5276906 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6aff7ea9a96edba4f56ee4fb2aafd500d68e986b3fbb9c33ea3862d9c5416c7f`  
		Last Modified: Thu, 02 Oct 2025 04:20:42 GMT  
		Size: 7.3 KB (7305 bytes)  
		MIME: application/vnd.in-toto+json
