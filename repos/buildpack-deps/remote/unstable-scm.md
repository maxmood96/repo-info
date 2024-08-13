## `buildpack-deps:unstable-scm`

```console
$ docker pull buildpack-deps@sha256:a6871fd1fbb706c9d8f6599e4c2ac233f3c96496f348e26c247ca9a5f7f3b67b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 9
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:unstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:63de544b1b3076182a7318beb845687cf1f23c4364f80f3ab1cd0885717fb036
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.6 MB (139557538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21eb3bd4bced03aeba49c5f17f1064be0c947b26ecec58d34a96dd41ba71d41a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:21:13 GMT
ADD file:ec9b256ad5af9d6c88b912d94fd4e58256e2b29a1c5ff616fe47488c72c1256c in / 
# Tue, 13 Aug 2024 00:21:13 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:46:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 00:46:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:0ee0708ec9247cb19ad61d1bba3a89642d7eb4cfcd5031f23018c732b0ce201c`  
		Last Modified: Tue, 13 Aug 2024 00:25:12 GMT  
		Size: 52.8 MB (52836188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ba418b28cb46180ce179bf48a7dfa7135087eefa79b479acfa16fedb4e4a1c2`  
		Last Modified: Tue, 13 Aug 2024 00:51:48 GMT  
		Size: 20.5 MB (20482905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23a515568b5fe34e15585cdfd456e9acee67d565f25f2bfc42df67c7b99ed3f3`  
		Last Modified: Tue, 13 Aug 2024 00:52:04 GMT  
		Size: 66.2 MB (66238445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:7177a05d7c22b3a9b2d05a23d3288d53fafa60f977a3de046d93d1e3294a97e5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.6 MB (131636157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:280ebc938aa661d553a0d9eb668d100e4f218a67504cf709cbbe6430f396df51`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 23:58:01 GMT
ADD file:95d0230b78af5d334bd0243ce6197c2140ec2471924e5ef4413707038e18e143 in / 
# Mon, 22 Jul 2024 23:58:02 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:44:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 03:45:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:ec2b125127e6f8d49325b626aa909fcd3b43a8d6c77bc97a74c5f2018c245546`  
		Last Modified: Tue, 23 Jul 2024 00:03:01 GMT  
		Size: 49.8 MB (49828856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b117c2153e64301fab367eee4a7771746dee9588d142dbd0e4791dc9a32239c3`  
		Last Modified: Tue, 23 Jul 2024 03:54:47 GMT  
		Size: 18.2 MB (18242564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c9873310e83bd2c9cddf329c78833d832e9bbd909cf26e632b676e3b31b940`  
		Last Modified: Tue, 23 Jul 2024 03:55:11 GMT  
		Size: 63.6 MB (63564737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:39c7d006924dc193dc2f5d78faa3f1d17c7e9aa6b3a182f32f75281bb942dfd5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.9 MB (125934153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c87e3a737cd11656c9a9dd1ce82646005ace4c4e66d8a1d15916c59c8511634e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:04:00 GMT
ADD file:31576c5cd1d1e13e2a728f71cf07534ba5b1b2ab9de9793a31cc07fcc990c347 in / 
# Tue, 23 Jul 2024 03:04:04 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:40:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 03:40:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:fa7817dbf291482bb88d91e0e917de78192dae47dd05161de99a0ed32a21527e`  
		Last Modified: Tue, 23 Jul 2024 03:08:25 GMT  
		Size: 47.3 MB (47311981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85dd4c3d5aa06a66cbc690f7dfe97a6c3194299eeb4d8911e0fc8c5a62f49d50`  
		Last Modified: Tue, 23 Jul 2024 03:49:38 GMT  
		Size: 17.6 MB (17608316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2530b2c70788d78360d3f365fdef0a3a385f75d30ac92e588df91acda5d06910`  
		Last Modified: Tue, 23 Jul 2024 03:50:00 GMT  
		Size: 61.0 MB (61013856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:c46a5d370e3e205ec7c0d3d5e1e370e287cd4d9af46a14cd58954b56e934360e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.6 MB (139647271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6db44b9367254b0b0bbd0f8d96643ea5c6b7907599774b9a875d2d6eda2ba9ed`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:40:28 GMT
ADD file:5d3aa31e5e33290bb28cfd74e2b2a88ce7e4415dc0d995c3c39d36c332bdbfcf in / 
# Tue, 13 Aug 2024 00:40:29 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:05:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:05:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:543c0d8816b61b146fc103b18d6ec335253cba7bad9fa7f1cb3e794a6b9e450c`  
		Last Modified: Tue, 13 Aug 2024 00:44:13 GMT  
		Size: 53.2 MB (53155250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42437a82bf9bbe8487117e25e8d86dc6640c415c01e295d2560ae15db12b5a94`  
		Last Modified: Tue, 13 Aug 2024 01:11:11 GMT  
		Size: 20.2 MB (20228217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6149cd0c731896a1b19323de76aaa6c32d3b8d0092d305902306e6795cb37d9`  
		Last Modified: Tue, 13 Aug 2024 01:11:27 GMT  
		Size: 66.3 MB (66263804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:01cdcc374f72d44626207be32c439902b464c3d3d658b27a0c29d7107189d7aa
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.3 MB (143268855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1b9cc4d75bad83ca4b442ce53584ba2058d9f735654e1925bd4e3b30136adf7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:39:51 GMT
ADD file:79c443f9d7d3c4ead1afa700b0409049a5e5def4db762097116c9f15a44a29ca in / 
# Tue, 13 Aug 2024 00:39:52 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:09:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:10:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:47aa20e0d3978e830fbdc52fb1b018e2dc37ff9f122461c55040f23300208844`  
		Last Modified: Tue, 13 Aug 2024 00:44:14 GMT  
		Size: 53.7 MB (53738474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce604b6ec46af20835c8de06fb56b6d31f8dce22f35194ea4cab29c2aac8c355`  
		Last Modified: Tue, 13 Aug 2024 01:16:14 GMT  
		Size: 21.5 MB (21505961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f51930d3a07571334ea27c6cab756bf536d9e8ac15d3dd0ba6ebcde49a8fe0`  
		Last Modified: Tue, 13 Aug 2024 01:16:36 GMT  
		Size: 68.0 MB (68024420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:15334f31455e132e2262d1167e932c92d2a60b10f7557b753356d655eb6feac4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.2 MB (136230786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddf6833d7529096fa1bb3815fec2f0d0ee573811115caa84d9329959be919808`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 00:41:03 GMT
ADD file:4c5b8a467710d6b46f986172bbe029a8628d9b5e288ce89ae0d2507c9c6a4f0d in / 
# Tue, 23 Jul 2024 00:41:09 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 01:40:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 01:42:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:547554521a86f8be7b55003b426c5518e59d2cad10d4457d287f4456f5b47111`  
		Last Modified: Tue, 23 Jul 2024 00:52:35 GMT  
		Size: 51.6 MB (51646553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68c0a36f24cc092af4605ed4efcf52aa8a41e0c0da13688560a4403d8ba28144`  
		Last Modified: Tue, 23 Jul 2024 02:05:09 GMT  
		Size: 19.8 MB (19769791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2faf5f50c37db38e90a50520c093b6fa2939d9fef5a62895ea90c91d02dbdeac`  
		Last Modified: Tue, 23 Jul 2024 02:06:02 GMT  
		Size: 64.8 MB (64814442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:fa91f7fe251a3e3a6e112335750dfcb83db9277a82a5fa58b45ecada4ffbfcae
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.4 MB (149436486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30ca1609d70f49394d680d1e00297b69c5471c813ff5070bb5360ed09c502aa4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 01:28:02 GMT
ADD file:585b8dcf2e4526cdaba5e616b7761a5b74b918d3740bb07d4bae9a885dd726a3 in / 
# Tue, 23 Jul 2024 01:28:05 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:35:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 02:35:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:bba0decf595ccf1bd757b6cf34465cdaa54fd8173ae0936ea4365d416401a52f`  
		Last Modified: Tue, 23 Jul 2024 01:32:48 GMT  
		Size: 56.7 MB (56726468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df406a521d8c92d349441aa62ad3b1bf57ec4505884acf3abaa7d36e0ea51411`  
		Last Modified: Tue, 23 Jul 2024 02:44:13 GMT  
		Size: 21.3 MB (21296883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:230b98c88f8a6ca27a89215004b3cdac4fa255a74553ee93c0bb336155b16701`  
		Last Modified: Tue, 23 Jul 2024 02:44:32 GMT  
		Size: 71.4 MB (71413135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:d808e4fb51a4250cbbec7903e02191a5a2dd381efb4732ad482d925c7040387e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.6 MB (136574683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f1ceb124a6788428e56e67e12a903afcc6cd5bd4556302fd4f9b1c59eb48ffd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:11:01 GMT
ADD file:97cc40f71485a0c47367bf7de8cb1715072dce719d216195de9b049516a29e45 in / 
# Tue, 13 Aug 2024 00:11:03 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:37:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 00:40:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:e7e6753663bf71667278434bd9ec3bfbf244788b1855805c384ac83204bc13ef`  
		Last Modified: Tue, 13 Aug 2024 00:16:18 GMT  
		Size: 51.1 MB (51106160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b04e5a15fbe73c8e7dfa541c5d04c781d3c5c4ac6a9ce7895b41cfeb8e40e71`  
		Last Modified: Tue, 13 Aug 2024 00:47:07 GMT  
		Size: 20.0 MB (20012849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65deb42d9c749a528063c18ed3482c3235a8863523f7fc5d895330b910edd50a`  
		Last Modified: Tue, 13 Aug 2024 00:48:15 GMT  
		Size: 65.5 MB (65455674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:6c8daa564a12c68f5fdd9e98aa37893e0024a408aa9ee724e7d2bb44b70fea5f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.0 MB (139980123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5535b3ab8cc246f97a1fe491db849a94bd5948200d49ca2d576954535f4ec275`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 02:29:15 GMT
ADD file:95a4cfad52ad69897cc13b974c9594de964886d46c30d9631ea74926a2fa92d0 in / 
# Tue, 23 Jul 2024 02:29:18 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:09:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 03:09:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c8768a7d57cf906ef686ceb35e7a6f68642e12ce3f36244a42bfd313f55747dc`  
		Last Modified: Tue, 23 Jul 2024 02:33:50 GMT  
		Size: 52.4 MB (52435495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dc02aad785807afd931690639de0be3fec099b62e37f4be13347783597758be`  
		Last Modified: Tue, 23 Jul 2024 03:16:04 GMT  
		Size: 20.5 MB (20478019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b20b90812b56a031f8fd0e591290e9252f35ca6f8f86d5550448fbfcba2c2560`  
		Last Modified: Tue, 23 Jul 2024 03:16:20 GMT  
		Size: 67.1 MB (67066609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
