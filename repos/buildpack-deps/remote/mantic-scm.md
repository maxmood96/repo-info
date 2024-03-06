## `buildpack-deps:mantic-scm`

```console
$ docker pull buildpack-deps@sha256:4890c01a9b71277c18cf5443357940910465d0b995519b130b5ece33c6415e83
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
$ docker pull buildpack-deps@sha256:243bdb387568cd69fc6bbbf39ddae9a36a05f2f804a0cc770819b8486a7cdd70
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82745141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bb0593c144279dfca7eeb415785711a1ef877b3cdd99931cfca9beb5c6060d4`
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
# Fri, 02 Feb 2024 06:13:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:8e30486de06cd814f639bb675162234bd141b86426c87d43f70eb1fbebf35b62`  
		Last Modified: Fri, 02 Feb 2024 06:25:08 GMT  
		Size: 44.8 MB (44762680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:1b1e9d9758301286327426af6e70aa5e7b8f216cbbd269c7edb29a983d63f446
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.8 MB (83787725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f9df0c6a52502c3869f438d017cae886cfeaf9e60f8fffd62af11e496fd0d92`
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
# Wed, 06 Mar 2024 02:59:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:9155ba03212deb920e05dc77749cc267b5b6fcdc16bda27f00864d27e0607886`  
		Last Modified: Wed, 06 Mar 2024 03:12:42 GMT  
		Size: 49.0 MB (48950883 bytes)  
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
$ docker pull buildpack-deps@sha256:bcdd59a28ed12834d023ba530aba7e94e8c017295320aa4f73958d863770616d
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.5 MB (93489959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4557f6a8a7ff4ac3b6bdad4b5eba002b8979f1bf9ad6336c32e511facc61e88`
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
# Wed, 06 Mar 2024 02:36:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:aa179ccd4d1ba32381ba7b18ea7a19fe2a7be5021377e619dcd5ea87d94344d0`  
		Last Modified: Wed, 06 Mar 2024 02:54:21 GMT  
		Size: 49.6 MB (49556847 bytes)  
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
