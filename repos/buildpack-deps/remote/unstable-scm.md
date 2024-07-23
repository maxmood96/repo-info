## `buildpack-deps:unstable-scm`

```console
$ docker pull buildpack-deps@sha256:bd569b68994dcdaaac4a8ce73a1ee992ecabdbef837fa0b90e33d59cefe7dc52
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
$ docker pull buildpack-deps@sha256:c2f657e723a4dda941a6fe1b2ec74869a7c2c10dbba3ac74018edafd59744986
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.6 MB (138557713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2fa8d579066c57e85b3318dfbc239c3359ea0a94653e6ee189f158ef855f4e3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:57 GMT
ADD file:cf83030bc061e8d24d8a36b4edb2846333916985361600a06dfb635fd59c8068 in / 
# Tue, 02 Jul 2024 01:25:58 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:52:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 02 Jul 2024 01:52:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:2d149d696b13b9c3df064cbc77767f81d4635c7804547d50ff7da0c45c51990a`  
		Last Modified: Tue, 02 Jul 2024 01:30:17 GMT  
		Size: 52.6 MB (52634573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:141f0a6d32a670095c08b9b66b2a2940431d5dfb05055fa488081211c5c31c55`  
		Last Modified: Tue, 02 Jul 2024 02:02:19 GMT  
		Size: 19.0 MB (19022788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:282b146ad3f3822c7f15a1f42f4cecceab568029d29f1dfea9f25a23cbe136e0`  
		Last Modified: Tue, 02 Jul 2024 02:02:35 GMT  
		Size: 66.9 MB (66900352 bytes)  
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
$ docker pull buildpack-deps@sha256:743a0ce5bd6cfaa274351397485f81aad864345a0c13926d220cdee4eb03b940
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.6 MB (138593968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbc61761d538deeed0142d5c59ceecc4f78dcfcfb450e7f4089f6ba36739de0e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:40:14 GMT
ADD file:13d2e6714604c76eb37d955b64f923c5e9360ac3b98a7115cf15ce9e648a1a56 in / 
# Tue, 02 Jul 2024 00:40:14 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:53:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 02 Jul 2024 03:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5c22b1ba66cae5b1ecf15ba852e6873679650dcd639327a03cf68963e082f4be`  
		Last Modified: Tue, 02 Jul 2024 00:43:55 GMT  
		Size: 52.9 MB (52888757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d804209f40f917ece8cc23c76923f30be9ddf2f195247e71675942294360421e`  
		Last Modified: Tue, 02 Jul 2024 04:03:27 GMT  
		Size: 18.8 MB (18764353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b13905653e52085cac0034a182fbc6e1096638d960653d96dee8be2a517342f`  
		Last Modified: Tue, 02 Jul 2024 04:03:42 GMT  
		Size: 66.9 MB (66940858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:58032e34a1678f59cee53b8d3ba48b12cc3f75b61d9ec97ddadcaf2dce23971f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.3 MB (142303179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d79249b9fbf5f5a29c6c4bec3698f80c04f17f1ba16ef8d487977d2da86f789`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:49 GMT
ADD file:a08584f3c5024aeb655047534f24f132994ce1978bc3c1b585197931050df05d in / 
# Tue, 02 Jul 2024 00:39:50 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:09:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 02 Jul 2024 01:09:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:fcc722c6a8b995b7f273820b7fc927164f6709bd0e428b87e24702a321694439`  
		Last Modified: Tue, 02 Jul 2024 00:44:25 GMT  
		Size: 53.5 MB (53522389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd8e6a38c0f75fbaa782155e3b94e2d74aeb59d307bc3e812b341c5dda4c716e`  
		Last Modified: Tue, 02 Jul 2024 01:16:36 GMT  
		Size: 20.0 MB (20029986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95bd1c9fa39223666daa0aa317ef8df03f991cf958cadb2ed6c76caa40dcb40c`  
		Last Modified: Tue, 02 Jul 2024 01:16:57 GMT  
		Size: 68.8 MB (68750804 bytes)  
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
$ docker pull buildpack-deps@sha256:f96cb4ed9d65bc2f134e70ec4ec06cbd5c85b4b0504a225cff4315ed8c8227b1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135827645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51bac5dd12e16d55713e1db5e729f29cde5ac97748d2c50c3398cacfd525a733`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 06:00:05 GMT
ADD file:cb8450d273e9ca21e77fb71fa8d82d31fec1f23d51cec9972814bdc76724935c in / 
# Tue, 02 Jul 2024 06:00:07 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 09:09:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 02 Jul 2024 09:11:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:bdd8e78a3c764042cf6937012c6bcfab521fa52691a33dc6b9d4a6306b03976a`  
		Last Modified: Tue, 02 Jul 2024 06:02:52 GMT  
		Size: 50.9 MB (50937149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08f88c2caf91aebefce5b8a2304891f8ff04dba8ae30e8fcccc9fc289faba979`  
		Last Modified: Tue, 02 Jul 2024 09:17:48 GMT  
		Size: 18.7 MB (18694124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5e8a525751918610936d3d7c2f56948a95908e5fdc97875a13eabf5b5755181`  
		Last Modified: Tue, 02 Jul 2024 09:18:58 GMT  
		Size: 66.2 MB (66196372 bytes)  
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
