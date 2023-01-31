## `buildpack-deps:focal-curl`

```console
$ docker pull buildpack-deps@sha256:ca05539607afdf51652fadf1bb882baaaeff23e11ed00335b0ab507b90bc9368
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:focal-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:9bd96799abaf771d64834ebaaeaf5040928fe28593df060270b6fc6690c2c899
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.9 MB (39940549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:381ac8331d7f12b1a0f907c205582c581ca32ebd7b7f747050f7fc1f1be04693`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 13:19:55 GMT
ARG RELEASE
# Thu, 26 Jan 2023 13:19:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 13:19:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 13:19:55 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 26 Jan 2023 13:19:57 GMT
ADD file:8b180a9b4497de0c6e131d6b48cf5c69a885379e63033ab9639d1655991e626c in / 
# Thu, 26 Jan 2023 13:19:57 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 17:44:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 17:44:16 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:7608715873ec5c02d370e963aa9b19a149023ce218887221d93fe671b3abbf58`  
		Last Modified: Thu, 26 Jan 2023 17:04:53 GMT  
		Size: 28.6 MB (28577884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:775acd67f6a888f53509c802ed2de62951e811db02a6fbb1180e5212bec2871f`  
		Last Modified: Tue, 31 Jan 2023 18:01:38 GMT  
		Size: 7.7 MB (7735447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6e51b341c75f39cf0b77e180991d99eb663f87efc35a66d782bca873366333a`  
		Last Modified: Tue, 31 Jan 2023 18:01:37 GMT  
		Size: 3.6 MB (3627218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:82d51504764d0f07a5fb5829d049b1d7d842d06aadbf066e88b7c40270c5d803
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.4 MB (34415637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:831dccf8c7d60c9dc2aa39e418fc5862e8ab666000572459532db9f26c95d583`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 13:35:44 GMT
ARG RELEASE
# Thu, 26 Jan 2023 13:35:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 13:35:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 13:35:44 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 26 Jan 2023 13:35:48 GMT
ADD file:6566d63937dd1808d3a4ea5591d4369b9083772d48fad60626fb91243a9f3f53 in / 
# Thu, 26 Jan 2023 13:35:49 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 17:53:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 17:54:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:316383d79e03258e1fee780854f6da78da364194ded4ace8bff50687070e1c8f`  
		Last Modified: Sat, 28 Jan 2023 04:40:09 GMT  
		Size: 24.6 MB (24586318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cedd9bc11bf3ade87673ffaf52bd72191419695a3f156525f1f6385e99c62852`  
		Last Modified: Tue, 31 Jan 2023 18:15:25 GMT  
		Size: 6.7 MB (6724879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d1bd20eaac6b7c8a879f3f79f1c3afc52c5d00881d69d150b174ccd3bb2062f`  
		Last Modified: Tue, 31 Jan 2023 18:15:24 GMT  
		Size: 3.1 MB (3104440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:0767b4c95dae9dbaa7774b499cea4a7dae7d45401fcf42a5d068e2e4784dfd74
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.4 MB (38408467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b3c73f8b607d6e91dcb234ea5c85bb9bcad9d99b0a83085b1b0f92f7f91de9a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 13:50:26 GMT
ARG RELEASE
# Thu, 26 Jan 2023 13:50:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 13:50:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 13:50:26 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 26 Jan 2023 13:50:33 GMT
ADD file:72ca0af0100de6591b59c44bd8856655c8441eb0fcbf7c32e427f6be5108a4a4 in / 
# Thu, 26 Jan 2023 13:50:33 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 18:16:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 18:16:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:70cf24b162395e1500d40f2b012f253bfd5d15f029ef9d636620fa2365ae503c`  
		Last Modified: Sat, 28 Jan 2023 04:42:53 GMT  
		Size: 27.2 MB (27193737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95ffbf27218ff7413bd6ccd35ddc8ac48fc4a05acd8799064b8b91a5591be3da`  
		Last Modified: Tue, 31 Jan 2023 18:33:58 GMT  
		Size: 7.6 MB (7598288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da4945eb9097cf0ab7dbe5663c4bbb6b98322edaae571cdae5b7eb063f086cd7`  
		Last Modified: Tue, 31 Jan 2023 18:33:57 GMT  
		Size: 3.6 MB (3616442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:aa391c563e346de8f951a909643304fbbf026b4718f2383b9d0b2e30acfc8117
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46476089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f98a291fd3d185dce69e17e17b21086a64f4961aa0d8cb1bebaad4a6a1bddc00`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 13:47:16 GMT
ARG RELEASE
# Thu, 26 Jan 2023 13:47:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 13:47:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 13:47:17 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 26 Jan 2023 13:47:20 GMT
ADD file:987b941a34ad98533c64e74a3d57b9c1b983ff16c8f36e21d29278a30a2403ee in / 
# Thu, 26 Jan 2023 13:47:20 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 17:47:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 17:47:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:0c2f997991bfe2ed920105bb595c3662038cc90a08c6db9888fffdfa8c673b16`  
		Last Modified: Tue, 31 Jan 2023 18:14:55 GMT  
		Size: 33.3 MB (33300341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f3363ea482048a0047bc689846ce7a4167fe085ed44686a4ead8b4effc8b611`  
		Last Modified: Tue, 31 Jan 2023 18:14:49 GMT  
		Size: 8.7 MB (8688990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acf921c3d774eec221e933b317431dc49da977aa5345a4ae5b0280db08ff0aeb`  
		Last Modified: Tue, 31 Jan 2023 18:14:48 GMT  
		Size: 4.5 MB (4486758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:fbdcfe03e4affad8be30b628b9e6103bf372130fb546581665208b731c37e51f
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.1 MB (34098144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19dbe709d0741532f57054b0936076eb6c802cb4f9247aca16a0ac9b9d35d2ab`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Dec 2022 01:10:28 GMT
ADD file:50c1d21a50d57d99470bd427f2ee427504ad0602a5046dbc6a04680574d27f39 in / 
# Fri, 09 Dec 2022 01:10:29 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 02:09:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 02:10:31 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:1bf57572b326faac5012873a6b3ea48eee0fe2649c47d425e34e149459c96c29`  
		Last Modified: Fri, 09 Dec 2022 01:32:24 GMT  
		Size: 24.2 MB (24245212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4633ed51036c9ce6577aa52028505a911429672b56dfad24f4015a5cb66b2059`  
		Last Modified: Fri, 09 Dec 2022 02:53:34 GMT  
		Size: 6.7 MB (6707636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f109750e4f2fde1559a0ea960213c81c032abe5d0abdd633294140c78d783fc`  
		Last Modified: Fri, 09 Dec 2022 02:53:28 GMT  
		Size: 3.1 MB (3145296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:71646caa4ee547d9f1b011bae59e018af0b641a7a7948a56a95ade3f1e0fe8fc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 MB (37933609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e01b20aaa1c8b46fc349fea2234d85e361ba6c585f16c58b1d82d608e325e57e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 13:21:27 GMT
ARG RELEASE
# Thu, 26 Jan 2023 13:21:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 13:21:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 13:21:27 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 26 Jan 2023 13:21:29 GMT
ADD file:4d5fa9b68af51e9c8cd7b25fb55ddd47256efb0b2eda9432507b72b7c1a17053 in / 
# Thu, 26 Jan 2023 13:21:30 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 17:39:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 17:39:32 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:cbc0e1117f61ba365a9a02263b82c04f704d5d162aa31b25a9326797dd1c7084`  
		Last Modified: Tue, 31 Jan 2023 17:54:46 GMT  
		Size: 27.0 MB (27016130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d68caacb20eb4390abe02f30b918bd6fde7dca313df1c7e97a5c7b4bc9a888`  
		Last Modified: Tue, 31 Jan 2023 17:54:43 GMT  
		Size: 7.4 MB (7375281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27d1fec08539e04cc6494a503fa735bf370900c6c6ff97feb9085eba16d290a2`  
		Last Modified: Tue, 31 Jan 2023 17:54:43 GMT  
		Size: 3.5 MB (3542198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
