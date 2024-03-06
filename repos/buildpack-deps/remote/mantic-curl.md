## `buildpack-deps:mantic-curl`

```console
$ docker pull buildpack-deps@sha256:b2fb7a10e28652e02c3191ce47a15c8acfd40efe3c0321b90f0ca10151e5d7be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:mantic-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:0fca5ff13f7f7b5e8298b93f28e15134e4b2df1daf8baf6222f533d87509be11
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 MB (37946042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd1bae1a972ac939e27c44ab147653e269f4987bb9df150221ac1d013ec897b1`
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

### `buildpack-deps:mantic-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:7dbdd2bed195883ab42ed0ad0b96818a1787ca8e95534f13c5d82a54621cef1d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34836842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08a886df4f2c14a8b0a45e16f024da28bd47814a1fbbd2a042287c8906a1fef3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 10:00:27 GMT
ARG RELEASE
# Fri, 16 Feb 2024 10:00:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 10:00:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 10:00:27 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 16 Feb 2024 10:00:32 GMT
ADD file:a8ad044c0716add39fcee624f55c4ca977480f572c190628fd0dcd180478ffe1 in / 
# Fri, 16 Feb 2024 10:00:32 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:58:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:490b22d657a9bee69801f742987cf2202ef1facc1143749c551c75e40cb2b8fd`  
		Last Modified: Wed, 06 Mar 2024 03:12:23 GMT  
		Size: 25.7 MB (25683605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d74dd7838268a90e7e95de52c8608c15817df4a837c3718e184968aa8632638`  
		Last Modified: Wed, 06 Mar 2024 03:12:19 GMT  
		Size: 9.2 MB (9153237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:4341891a0761c7bcd09df0d6c13682f3d1c1479160b0333bf1089308cb974b70
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 MB (37028373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fe26cb29e36768799cbb3f4712ea4afbdaf4140eb64b1b05e8c996880413533`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 09:24:31 GMT
ARG RELEASE
# Fri, 16 Feb 2024 09:24:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 09:24:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 09:24:31 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 16 Feb 2024 09:24:36 GMT
ADD file:31c3d4b2613da88a6e201d2ec72f20609b03ad4d375d97b9c686cce80c24ab2f in / 
# Fri, 16 Feb 2024 09:24:36 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:40:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7c61e8985bd62f5d93258f96a729f264b9eb712d879491c8f79a3fd1a3fa54d0`  
		Last Modified: Wed, 06 Mar 2024 03:51:26 GMT  
		Size: 27.4 MB (27364411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:561438a9c1b423f692b4e8db906c99bc70f6080f9d43220d6ba38dde6ad43ea9`  
		Last Modified: Wed, 06 Mar 2024 03:51:23 GMT  
		Size: 9.7 MB (9663962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d305c5e6a0a1f1b89f5121496c829e2dd3e93d7fa8a139a2eecaa361e0c8fbaf
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43933112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6f789d7772d1087fb0373a1bca7a85cc9eded48bed7bb965aac975c8f30e81f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 09:36:48 GMT
ARG RELEASE
# Fri, 16 Feb 2024 09:36:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 09:36:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 09:36:48 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 16 Feb 2024 09:36:52 GMT
ADD file:cb1f81d9c266883aed50b7de079d58a9f6d90401d2d7ccf3aa7f9c5ad5eec617 in / 
# Fri, 16 Feb 2024 09:36:52 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:35:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:214a4d0fe457c3d67700d559db1bef30e158af48faba534bfe016fdb2e3b2662`  
		Last Modified: Wed, 06 Mar 2024 02:54:03 GMT  
		Size: 32.3 MB (32348067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa0dda02c37214de423eb7444d8a4123495e723c785f46d9699f2c2c60c0586`  
		Last Modified: Wed, 06 Mar 2024 02:53:56 GMT  
		Size: 11.6 MB (11585045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:72b4793c911a7c181fda7bfd7b1ac2c37d3283cf9cbe8fb031646d2175bbc135
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37646724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:901ab9ff2fd6adaa5c1a48a8a562f7cfe812fd1b5f12594eb071e136f4bf200a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 10:00:20 GMT
ARG RELEASE
# Fri, 16 Feb 2024 10:00:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 10:00:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 10:00:20 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 16 Feb 2024 10:00:23 GMT
ADD file:c9b844278d52249fbe30fc9a8c20ccae86a169f5c09f95ddddbbf9f2336bb40d in / 
# Fri, 16 Feb 2024 10:00:24 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:33:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0e673e987349120571169b0914846233abd87f13463706c302a73718492df637`  
		Last Modified: Wed, 06 Mar 2024 04:47:52 GMT  
		Size: 27.9 MB (27888596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4516c1c292430ff043c9c627134d0a108d22e18986e4d16c4a51c06f09a8cadd`  
		Last Modified: Wed, 06 Mar 2024 04:47:50 GMT  
		Size: 9.8 MB (9758128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
