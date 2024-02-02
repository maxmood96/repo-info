## `buildpack-deps:mantic-scm`

```console
$ docker pull buildpack-deps@sha256:b6426733be59bed6827c25f3bea19830907791681ffe7936ca2d9465cc8e2b2c
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
$ docker pull buildpack-deps@sha256:99c3a2664ce84bfa30ea116c02fe29273756f572da22030b5571639edd5a7bea
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83269286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a63850e7827c39043becac3e1267d9f8c55bd3a2f90355076755ccb868a1fd9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Nov 2023 17:54:17 GMT
ARG RELEASE
# Thu, 30 Nov 2023 17:54:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Nov 2023 17:54:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Nov 2023 17:54:17 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 Nov 2023 17:54:19 GMT
ADD file:5430e0b4ea856c760b6e2b88e8c2cd2d49704ed2f3c53ae34c10750a608d40ec in / 
# Thu, 30 Nov 2023 17:54:19 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 04:21:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 01:50:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cb8122a41e708f03d563c8ba7400f85d27af325fae5fbf4e00380a11f4ca1fa9`  
		Last Modified: Sat, 02 Dec 2023 02:22:28 GMT  
		Size: 28.1 MB (28070890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3950b4737b0d86b7d5a2758a2148e06120a5a73d9f1593fe22ad1a7c8e83a83`  
		Last Modified: Sat, 02 Dec 2023 04:30:04 GMT  
		Size: 9.9 MB (9907996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e55d77a03c8c92313d594ba3785c087935d6e66a68604e51e8ca68fd88ee16e`  
		Last Modified: Wed, 17 Jan 2024 02:07:37 GMT  
		Size: 45.3 MB (45290400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:ff3b10e9e13834203eabf65da442e5e6e7f1dc28079bf6420697ef6d54c6f22d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84123043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:373f46ea9f5a4f678582773c3389d39f77fa333db7f4484f1353fc0d60d861ce`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:07:56 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:07:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:07:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:07:56 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 23 Jan 2024 13:07:59 GMT
ADD file:0d9a942fe0637d88a4a14b6ecc7a7eef481eed8189b687ba4205e1e9f0167188 in / 
# Tue, 23 Jan 2024 13:07:59 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 23:59:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:00:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e8e3654023548eb0bb2a22e6ea3ba6f3431e59857720b89349780156ca8c6629`  
		Last Modified: Fri, 02 Feb 2024 00:11:24 GMT  
		Size: 26.0 MB (26022139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80a8b0ea5368129fa3fad384fe27cca04d157f47585a126a9c99e150d044c11a`  
		Last Modified: Fri, 02 Feb 2024 00:11:21 GMT  
		Size: 9.2 MB (9151306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de61dd38dc0af18a380a823e58045d13cd0b6bf13c269d775509a8a308db69e4`  
		Last Modified: Fri, 02 Feb 2024 00:11:41 GMT  
		Size: 48.9 MB (48949598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:30d60af6834b94273aff3692ffe1b4737a398c442d812b60eeb95f68310a6d75
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.7 MB (81697099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e268880f7f6e31b0b6bd1171277d26005b2e7681f030a28a47fa390e3e4ad709`
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
# Fri, 02 Feb 2024 00:58:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:3fc3621d05b6a87c0189a07fccebe13e2ebcc2e4f796eb3d58eafa1fb5e33944`  
		Last Modified: Fri, 02 Feb 2024 01:09:55 GMT  
		Size: 44.7 MB (44678006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:66efafb92ffb24be5b1b7b30cf4cd6d0ebfac6688e93b50cf150959fd8f2d2f4
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.5 MB (93485764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7c5d4bd8caa62bca916fc82fc2196e2f5659372e4bf364afa13015117552b0f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:10:40 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:10:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:10:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:10:40 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 23 Jan 2024 13:10:44 GMT
ADD file:cc249c861dbf6f8c5b35113826ba4f44020a7744cc0904b7332241f16c9059b6 in / 
# Tue, 23 Jan 2024 13:10:44 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:14:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:15:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:56b9cdd13b9ab0beda6da966bcaa7ef66d9af53dd1af7f8369e53e309e55a3f7`  
		Last Modified: Fri, 02 Feb 2024 02:34:38 GMT  
		Size: 32.3 MB (32343234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f7cd38609ebf2672a483d1cb46351fd725b34f48984a193d2c9ed49602f4cd`  
		Last Modified: Fri, 02 Feb 2024 02:34:31 GMT  
		Size: 11.6 MB (11585183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde92598b4fc6ed5837ce31fc6e716b9e9a1bd45de6be16b7e87d47b25abc89d`  
		Last Modified: Fri, 02 Feb 2024 02:34:56 GMT  
		Size: 49.6 MB (49557347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:ef20740de594702ba23b9671b59da991be243890fee65645d06c8e2d794a6f85
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82683461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6882dfc675d521a8e479f6aae28a958103f516928aae183f69b45bb5861f880a`
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
# Fri, 02 Feb 2024 01:19:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:67d23dab9f284ea43a1eedf62d67c328771f3148bdb6b7011b59e1cfecfdfc4c`  
		Last Modified: Fri, 02 Feb 2024 01:35:04 GMT  
		Size: 45.2 MB (45232081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
