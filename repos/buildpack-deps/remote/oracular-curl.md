## `buildpack-deps:oracular-curl`

```console
$ docker pull buildpack-deps@sha256:4b202798ed871af3ea0d1d493a09a797867a975bff1b36c67e9953937189bc88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:oracular-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:da6f89e9229b0475d241f6116e827a4a72232e5c4c0b2c77dd151ff1d1247f30
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46848858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c0c646cd4699048aafee145819910df21234b33880b64ab49def2b9837f40b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 09 Oct 2024 15:42:15 GMT
ARG RELEASE
# Wed, 09 Oct 2024 15:42:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Oct 2024 15:42:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Oct 2024 15:42:15 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 09 Oct 2024 15:42:18 GMT
ADD file:c6c1fcc53cf2d3beb705eee292dd1e6ef2980e7f6221cba9d5c4081038760fc1 in / 
# Wed, 09 Oct 2024 15:42:18 GMT
CMD ["/bin/bash"]
# Fri, 11 Oct 2024 23:44:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:43ed7ac192d3f50e551118286d2a59c5cdf9ae247515319b137995d2d91c1857`  
		Last Modified: Thu, 10 Oct 2024 06:10:56 GMT  
		Size: 31.5 MB (31497006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aebe8581de16e2d108a8b8b443bb95f82e5cad32c8f55539cb51fdde9b3436ca`  
		Last Modified: Fri, 11 Oct 2024 23:49:36 GMT  
		Size: 15.4 MB (15351852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:5cceb2f547cb52fc3342e32fef41d79dd9a16dd8b9eccb8cc68d586752442712
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.5 MB (42458114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f67665e512286002cbd3225e6ac838a3288fd31c2555234586ba4330b5621f93`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 09 Oct 2024 15:48:28 GMT
ARG RELEASE
# Wed, 09 Oct 2024 15:48:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Oct 2024 15:48:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Oct 2024 15:48:28 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 09 Oct 2024 15:48:31 GMT
ADD file:8e23d3c59f96fb90ac280b31339b3cdff6ade1865ca64b22d81f85a66b3808c2 in / 
# Wed, 09 Oct 2024 15:48:31 GMT
CMD ["/bin/bash"]
# Sat, 12 Oct 2024 00:40:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:aed21e28ca29b926cb189adb25146a9a8c068117edbe9a64ec7fb7ee97bcb402`  
		Last Modified: Sat, 12 Oct 2024 00:45:50 GMT  
		Size: 28.4 MB (28419590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f03bc67226a8aeed5fe9da57dbc1e718b4b9cb3ff6a8e9f88434bd6e0350067`  
		Last Modified: Sat, 12 Oct 2024 00:45:48 GMT  
		Size: 14.0 MB (14038524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:d026840c1f2c42096cdb088df4b14a7c9c852a36f2d035828d99c7b74ad528c1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46516178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffdcdec574fcb50d0bf5119678c2bc0dea93736af2dfe682c13957abdf5a1314`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 09 Oct 2024 15:42:32 GMT
ARG RELEASE
# Wed, 09 Oct 2024 15:42:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Oct 2024 15:42:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Oct 2024 15:42:32 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 09 Oct 2024 15:42:35 GMT
ADD file:897556c1de01d47a95fb4d7011c66a17502f56fb3838b2231407a26c3ec19779 in / 
# Wed, 09 Oct 2024 15:42:36 GMT
CMD ["/bin/bash"]
# Sat, 12 Oct 2024 00:03:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5bd0568efdad34fcc3fde5617d0aeb525b51e6dda58f9e060a25a75497dc7601`  
		Last Modified: Sat, 12 Oct 2024 00:08:40 GMT  
		Size: 31.4 MB (31391906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ec28f0bb6a14d9333d443320786a1a964cda0d56c3e4739c1c234be03b60ab`  
		Last Modified: Sat, 12 Oct 2024 00:08:37 GMT  
		Size: 15.1 MB (15124272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:817662eada8897a66e5dc015628c6f86e2f389162ec27464b08111d35facb2d3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.4 MB (53417670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:459d95a79091922cb35dccd5f8acb872291a6183b2b9d44b661fc36ec2f16826`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 09 Oct 2024 15:42:05 GMT
ARG RELEASE
# Wed, 09 Oct 2024 15:42:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Oct 2024 15:42:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Oct 2024 15:42:05 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 09 Oct 2024 15:42:09 GMT
ADD file:1f33027337aeb38d1fecb5ee33f2c55c6bd442e269ee902f5364ec863e957998 in / 
# Wed, 09 Oct 2024 15:42:09 GMT
CMD ["/bin/bash"]
# Fri, 11 Oct 2024 23:41:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:59fded0b17a5ce2788c02c2273aabe2d80b131c95c823e9d2c53804dc8397122`  
		Last Modified: Fri, 11 Oct 2024 23:48:13 GMT  
		Size: 36.2 MB (36191340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb2a0f576e77c90f975da926e3990ed176260de8a3c36a88eb5eedae452dfd28`  
		Last Modified: Fri, 11 Oct 2024 23:48:10 GMT  
		Size: 17.2 MB (17226330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:7ee40875c9bae0d9749f1240b3254b301a55e66e8f459064f75b40639506389c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.8 MB (56751087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92a2f966ccb05e961221b21a9db2d61c2a852abbe4fde1b1f73c04f1efe11b97`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 04:12:38 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:12:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:12:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:12:39 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 18 Sep 2024 04:13:12 GMT
ADD file:845e21eb0f8f24ff79deb49f33bb09a928b70e6af9d901303a950a5614468b9a in / 
# Wed, 18 Sep 2024 04:13:15 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 02:01:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:4ff6ad57950b3a2fb19ca28c995584b6b4061c2cb5c15ab51fa0c5f6afd06486`  
		Last Modified: Wed, 02 Oct 2024 02:17:56 GMT  
		Size: 38.5 MB (38536728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:683c6b81713c855136283c682cec256fa15a4d0c96793cb90da8c8604a3b3a87`  
		Last Modified: Wed, 02 Oct 2024 02:17:45 GMT  
		Size: 18.2 MB (18214359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:41a996db9213db8294e64f1a4ec828a25b048b6f37748fc974fae24e9ef2da57
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48349555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:571e0eacd2affb23496465cae630c9165b919bc6913371f3468b298362990bdc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 09 Oct 2024 15:41:46 GMT
ARG RELEASE
# Wed, 09 Oct 2024 15:41:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Oct 2024 15:41:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Oct 2024 15:41:46 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 09 Oct 2024 15:41:48 GMT
ADD file:e8f85fdb92ac3e5e436757449ac2447ad1520aad2682c8e0077efcce841566a1 in / 
# Wed, 09 Oct 2024 15:41:48 GMT
CMD ["/bin/bash"]
# Sat, 12 Oct 2024 00:14:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:d3b5ad6408cb1211e0e67e575d03b9f4cb668ee2412623f34d712fcefb3c6750`  
		Last Modified: Sat, 12 Oct 2024 00:19:21 GMT  
		Size: 31.4 MB (31434220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b0d91e3d271767afbce4ff60db4b1b486e55b4e4dc252a15928d1e45c9d9445`  
		Last Modified: Sat, 12 Oct 2024 00:19:20 GMT  
		Size: 16.9 MB (16915335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
