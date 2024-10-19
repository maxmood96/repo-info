## `buildpack-deps:oracular-curl`

```console
$ docker pull buildpack-deps@sha256:03f80bb571a97f04cf6f6ce70cc27455bea50491907b2b311b5df89ec5c89623
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 7
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:oracular-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:c8064ce954a2d9c90bd2e16fdd31c7c0b20e66720232e562b71c781f6c00bf56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45957871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b7b838a1e6a2498c0f2b75d67c8db81136efdc82a162f30a7585633d1d465a7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:c6c1fcc53cf2d3beb705eee292dd1e6ef2980e7f6221cba9d5c4081038760fc1 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:372111cb3b6e75bbceae9a3a6c2d060e2fb7b2573e9ff6e1931f6de2798246c4`  
		Last Modified: Wed, 09 Oct 2024 16:53:13 GMT  
		Size: 30.6 MB (30600773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a944d883315edf8742919f6ef5b3c26a8ad272f5008425c60a2142fb1f5df853`  
		Last Modified: Sat, 19 Oct 2024 02:06:13 GMT  
		Size: 15.4 MB (15357098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:734f143b619a054aeaf675404b5a8b6bf169fef11b9e111e8a691436743a0b58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2465631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76d2b611b8af5dbe471921a51a30ed516be558eeaf85c1466481a13d6640a4ae`

```dockerfile
```

-	Layers:
	-	`sha256:04d1691c1daa2c8f7f4ed5fbb5bcfaa1d228a7b3502a02d4d0c606c8e2a69420`  
		Last Modified: Sat, 19 Oct 2024 02:06:13 GMT  
		Size: 2.5 MB (2458653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:470d7dbf100349d28fe574b0fc0e6eb056c846f0a7430a28ea4919e451ed1b6b`  
		Last Modified: Sat, 19 Oct 2024 02:06:13 GMT  
		Size: 7.0 KB (6978 bytes)  
		MIME: application/vnd.in-toto+json

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
$ docker pull buildpack-deps@sha256:d077992b788a9af765b5bd9cc8dfbfdfa4148a8f57a536e79b1c900ff703e118
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48689245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d71e2496c145fd637f68a99d79840efa4114692affcd6e12fa47c4173263fa86`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 09 Oct 2024 15:57:18 GMT
ARG RELEASE
# Wed, 09 Oct 2024 15:57:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Oct 2024 15:57:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Oct 2024 15:57:19 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 09 Oct 2024 15:57:49 GMT
ADD file:9744fb771a3525b1ecc8bb8c4ca623db4381f3fa78cd865afd2dc853a7ec0106 in / 
# Wed, 09 Oct 2024 15:57:52 GMT
CMD ["/bin/bash"]
# Sat, 12 Oct 2024 08:12:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:1f2879ef823c6b1610dab93bd22c73f73e429d2129258412afee5bf3a371ee53`  
		Last Modified: Sat, 12 Oct 2024 08:28:13 GMT  
		Size: 32.8 MB (32820966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ac0afb9bfdb4e033cce2424ac2751c72a5f25441b1d3b8722cb4a1d496177d9`  
		Last Modified: Sat, 12 Oct 2024 08:28:00 GMT  
		Size: 15.9 MB (15868279 bytes)  
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
