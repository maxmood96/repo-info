## `buildpack-deps:mantic-scm`

```console
$ docker pull buildpack-deps@sha256:cb9c766fcc0d50072c6344a743ccc688b2ab81db1b5d827874cb29a4e21c003b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:mantic-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:419609933b12ca00c8a73e76e6cc3495af03cc6a0a55fba48a6587ea534edf82
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82709327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57264a7b401ab4cee2930269cd96560c3f9f21633772107aece54ae9ca0f535e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 09:35:50 GMT
ARG RELEASE
# Fri, 16 Feb 2024 09:35:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 09:35:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 09:35:50 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 16 Feb 2024 09:35:51 GMT
ADD file:fb2da00b24905f9231165c1a3f037a78a00c19ca26c375a018728838dfeb82d2 in / 
# Fri, 16 Feb 2024 09:35:52 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:06:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:06:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:83b8dadc4df3fdb50c87e452b3f9cfea60d51607db61aca9a1062c27c65ad0e2`  
		Last Modified: Tue, 05 Mar 2024 21:36:44 GMT  
		Size: 28.0 MB (28035167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb317c53627269ca09e9abcb9ab5a7700fe4050abfa54ef20c935f8a020b0d4`  
		Last Modified: Wed, 06 Mar 2024 04:16:23 GMT  
		Size: 9.9 MB (9910875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b21ae994c2a096a3b04d9c7a1755c60179f67ca190f61936d6da7e1729ee588`  
		Last Modified: Wed, 06 Mar 2024 04:16:41 GMT  
		Size: 44.8 MB (44763285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:e5484b6fe256cb6e89930e2d5e56234839ec79a1c309575c167094e2775b4dfb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.8 MB (83786267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afa350297409e6f07bdcaf1adaf35800d1668985e54ae3f2dd8febb7829cd286`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Apr 2024 15:50:42 GMT
ARG RELEASE
# Fri, 12 Apr 2024 15:50:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 12 Apr 2024 15:50:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 12 Apr 2024 15:50:42 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 12 Apr 2024 15:50:48 GMT
ADD file:7ae24dbfcd35eb56c9df6cfe135ee0660ec7885c25b732bd820de74e6e977e91 in / 
# Fri, 12 Apr 2024 15:50:48 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 02:22:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 02:22:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d03784ef1a0f8fba0d5ba66aa649704c0738839e0e0b7a3edcf32e7e679e3284`  
		Last Modified: Tue, 16 Apr 2024 02:33:44 GMT  
		Size: 25.7 MB (25685475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7dffb31d254b552d12914e690e612e00d722122772f28e4f60878569a1faaa`  
		Last Modified: Tue, 16 Apr 2024 02:33:41 GMT  
		Size: 9.2 MB (9151386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf231dd75ff3ba004a73cfe9bfe03f40adef2f17d2d7902e7670fd14d427bef`  
		Last Modified: Tue, 16 Apr 2024 02:34:00 GMT  
		Size: 48.9 MB (48949406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:9ccf88f399c9cff6c8ed719fcb831dc750d818d7e1caf28281ca866e40119703
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.7 MB (81720298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba43113abcdb73fcfeeeb6367d5a6cc42acc2a62753b02ed2977b68bd530e746`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Apr 2024 15:51:12 GMT
ARG RELEASE
# Fri, 12 Apr 2024 15:51:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 12 Apr 2024 15:51:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 12 Apr 2024 15:51:12 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 12 Apr 2024 15:51:14 GMT
ADD file:26243ab96da01a7d087b1c824a80d95c015b3c87952acd0ff162515d17c19a31 in / 
# Fri, 12 Apr 2024 15:51:14 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 02:00:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 02:01:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:14dec08930ea65c3dbde0e38ed54f079d9cc601f7e9429870443eb6f5c127ecd`  
		Last Modified: Tue, 16 Apr 2024 02:12:13 GMT  
		Size: 27.4 MB (27378355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a48b671c7c275cde8e73a26074b9763487010e57526a55b3e22e3bc0da54ec6b`  
		Last Modified: Tue, 16 Apr 2024 02:12:10 GMT  
		Size: 9.7 MB (9664437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6855e3956a9a4d92d9a1298b6fe89998168da253af783ba53efa35c4403235bd`  
		Last Modified: Tue, 16 Apr 2024 02:12:26 GMT  
		Size: 44.7 MB (44677506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:9b38b7bb69d4ee72d92323aedc6f0f18f4bbe24169f739aca4cee60db4325190
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.5 MB (93497609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d05ce9c0ce7c203b9f0b8bab6182574df361fa447a151c885c5fd63344739f6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Apr 2024 15:50:38 GMT
ARG RELEASE
# Fri, 12 Apr 2024 15:50:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 12 Apr 2024 15:50:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 12 Apr 2024 15:50:38 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 12 Apr 2024 15:50:42 GMT
ADD file:a8da603c55c74defd91d533f7d8ae1989fdabaffbd1dffc9bda21c86eb06e0dd in / 
# Fri, 12 Apr 2024 15:50:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 03:13:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 03:14:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5f150c6aafa2908189205a2f6135c61c644daafd16d4b9fbb420f2d36da7c9cd`  
		Last Modified: Tue, 16 Apr 2024 03:32:53 GMT  
		Size: 32.4 MB (32350225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:894c0745c5416dd216b7c49826dc5ede395abbe248d05a9409af9af764903622`  
		Last Modified: Tue, 16 Apr 2024 03:32:44 GMT  
		Size: 11.6 MB (11585816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22ce7686d375a21db004d3e3fe2d769bd8323976cc6e1f10f243c874c374105b`  
		Last Modified: Tue, 16 Apr 2024 03:33:11 GMT  
		Size: 49.6 MB (49561568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:00941026e37a1484f686ca9a2a474f528433f754763ca239de0f43fdc3406c00
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.9 MB (82902991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee1bf0812c59d692c7e98284c896fed765b91bf13aacd5de0b80b397e3b2829c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Apr 2024 15:51:31 GMT
ARG RELEASE
# Fri, 12 Apr 2024 15:51:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 12 Apr 2024 15:51:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 12 Apr 2024 15:51:31 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 12 Apr 2024 15:51:33 GMT
ADD file:13a7b46379c7483a76105798c32aac56ed459dca7ef015d973b0e1d68d9b7812 in / 
# Fri, 12 Apr 2024 15:51:33 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 01:28:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 01:28:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c38167d4d3684f5f8ee90b7adc5372841c98bba0d9aa208819985d030733dcfe`  
		Last Modified: Tue, 16 Apr 2024 01:37:51 GMT  
		Size: 27.9 MB (27890477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a15768582f995f80e1c5766c7d3c9f5c2a98ef818cd780593cc4ec8e4abebc68`  
		Last Modified: Tue, 16 Apr 2024 01:37:49 GMT  
		Size: 9.8 MB (9758725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c8626ab716cf334ee2c2065efea9a5208a1ca02fec3d802f60e7c3307826539`  
		Last Modified: Tue, 16 Apr 2024 01:38:05 GMT  
		Size: 45.3 MB (45253789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
