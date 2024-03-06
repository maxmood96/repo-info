## `buildpack-deps:mantic-curl`

```console
$ docker pull buildpack-deps@sha256:600bdffbe1322915906b17dac7b63b3b303d1b274c7ce1b4ca53cfb3011ed555
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
$ docker pull buildpack-deps@sha256:e12b972188e84b41002773ea27e117b48ad461231fc8951ff4d369bffb2516fe
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 MB (37982461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cf40ae89d6804df3257bf478c70fcfa247c71deec7d451375130310d1f3c3f6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:05:31 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:05:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:05:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:05:31 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 23 Jan 2024 13:05:33 GMT
ADD file:838ff8a8551fa2cfda1c161126c2874266a0ede4da3a34241e7330da88d86319 in / 
# Tue, 23 Jan 2024 13:05:33 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 06:13:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ea0c8ce8e2754c0e73da06e3510634798297afe205bc4da78d2645daa8df3614`  
		Last Modified: Fri, 02 Feb 2024 00:52:51 GMT  
		Size: 28.1 MB (28071046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7126027d8121ee0a23bf9822b978f8c928f655c6b15b9534ac4195c8359fed01`  
		Last Modified: Fri, 02 Feb 2024 06:24:51 GMT  
		Size: 9.9 MB (9911415 bytes)  
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
$ docker pull buildpack-deps@sha256:4fda16a9a3241c3d059c4b278b1e93346e837be64697820ce6a351a839da963a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 MB (37019093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d089d52d87f42a3d35c223dfa42b1db04a61e6f576e94a6cbf3b1d33f34b427c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:11:20 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:11:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:11:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:11:20 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 23 Jan 2024 13:11:31 GMT
ADD file:b3803d650d7bc69a1591e4672278d8dfabc7c31ad2bdbaa54682acd051ee31c6 in / 
# Tue, 23 Jan 2024 13:11:31 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 00:57:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1f86d1d63a2b177dbd6ad8e2a2268f5e1928c4b7e18919644ae7b4d37998a7d1`  
		Last Modified: Fri, 02 Feb 2024 01:09:41 GMT  
		Size: 27.4 MB (27358488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d26bb3702bafec7c64da2e4d20d6372d3ab75a912e8640d4826ddc4c67a0bd6f`  
		Last Modified: Fri, 02 Feb 2024 01:09:38 GMT  
		Size: 9.7 MB (9660605 bytes)  
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
$ docker pull buildpack-deps@sha256:672f57e8ce41a9854457462a609881bf6a78f98f6afec1441939dff65d7219f0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 MB (37451380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:173781f822b0623706926ec60367b00f7352e2f977bb23b1f21af1780d80878f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:11:44 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:11:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:11:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:11:44 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 23 Jan 2024 13:11:46 GMT
ADD file:a5f8986f79fe314fa6c34aef3a2400bd666a4e11f62528f97810e7bd6191278c in / 
# Tue, 23 Jan 2024 13:11:46 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 01:18:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d651f63b259ec72c40c7984c744092854cb29b4cc8729dbfaff6b41cfc0040aa`  
		Last Modified: Fri, 02 Feb 2024 01:34:50 GMT  
		Size: 27.7 MB (27693181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e6ad91452f2f39c050b9f9a73910bf71da560c0e4c9345749cb6632041742a3`  
		Last Modified: Fri, 02 Feb 2024 01:34:49 GMT  
		Size: 9.8 MB (9758199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
