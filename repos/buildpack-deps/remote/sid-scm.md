## `buildpack-deps:sid-scm`

```console
$ docker pull buildpack-deps@sha256:076dded5ef5974f945b7b8d3c053b03f00c64780d1a0e4e3123d83ed40176840
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

### `buildpack-deps:sid-scm` - linux; amd64

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

### `buildpack-deps:sid-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:e8bddb7d1243fb39877ed10e87f7741805c465b7ef356467e1eb90b3f61c970b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.0 MB (132031195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27a72fe21681d89fb17dd1e9272bcd3085b96f3fe41c490e0b2bd6de30fc444d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:49:07 GMT
ADD file:e97cbdca31cc34df027df8a29da79dec8686613556a85f9e94434bf7952452ff in / 
# Tue, 02 Jul 2024 00:49:07 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:17:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 02 Jul 2024 01:18:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:00d6074b8078def64a01fe6a6ae8b9b4c88fda262cf81e16d90c7e7f16541209`  
		Last Modified: Tue, 02 Jul 2024 00:53:08 GMT  
		Size: 49.7 MB (49697271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f60563593e8bb3a3fcfcd7d9061a4aacccb82aa350743f3290a168dd08c3e89f`  
		Last Modified: Tue, 02 Jul 2024 01:24:52 GMT  
		Size: 18.0 MB (17969872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23186f8262bd00e188269c09360563f198acc4d7d678c6f5cf647da05eb8668`  
		Last Modified: Tue, 02 Jul 2024 01:25:10 GMT  
		Size: 64.4 MB (64364052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:e6ee6faba203addcf2570fda625f932d9d79581782d1173ef809dc6ebbb5fb2f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126271849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d47e4d80595d77d9da98f3a15c50f12f855dfa59e3ada90990ceb4d40e68d30`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 01:00:51 GMT
ADD file:204b9bd9d9bd808b15b0257739243338e223ade24ac2085e9c4ee95ac07d2795 in / 
# Tue, 02 Jul 2024 01:00:52 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:28:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 02 Jul 2024 01:28:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5771d15f45cf5483d59c36ac7d7cc82b87747d80582fa22fc972b5752cd511a6`  
		Last Modified: Tue, 02 Jul 2024 01:04:51 GMT  
		Size: 47.2 MB (47183831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0863392378e09c6e3f61df0d322c322e2bcb582a29f5b7e95a77fce23a171076`  
		Last Modified: Tue, 02 Jul 2024 01:41:23 GMT  
		Size: 17.4 MB (17360749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4fc9810575d09cc1a531b36b6dc5a6732c2497822817a275fa6e0f052b85729`  
		Last Modified: Tue, 02 Jul 2024 01:41:44 GMT  
		Size: 61.7 MB (61727269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm64 variant v8

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

### `buildpack-deps:sid-scm` - linux; 386

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

### `buildpack-deps:sid-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:41552a33bdd211da048c50b2941b9abc6ba764eef8107a3247a29146441ca3a4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.7 MB (136724018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1260ef239c1953462457c4510fd29a68e3ad24d1bed9d2f54f1f2ebb8f98e8f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 01:21:34 GMT
ADD file:38ebbca2b69d1a13c63e4290834a1071ff05cbc6ca9d34fccc4e1db7ea4e713f in / 
# Tue, 02 Jul 2024 01:21:37 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 02:12:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 02 Jul 2024 02:14:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:976737d71ea9234bc2fbae831a70295b014d7172cbb319c0c5e34bbba1f27f2c`  
		Last Modified: Tue, 02 Jul 2024 01:32:52 GMT  
		Size: 51.5 MB (51498083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e78b0ccee5fd0523050c17351663142460efff3d2e6ca95b728321b57c9bc99a`  
		Last Modified: Tue, 02 Jul 2024 02:35:55 GMT  
		Size: 19.5 MB (19507963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da7a3a9a98c51a48f7892479ba667dfa4f43f4d70fd9307a177bf51a95b6fdaa`  
		Last Modified: Tue, 02 Jul 2024 02:36:48 GMT  
		Size: 65.7 MB (65717972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:63f194c81e4c118a40fee36630d31e1e0c0acdc27929d898be8eaf7beecabdab
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.9 MB (149923694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82357a8dc90e376f70da320c77dc2fc0160eb3b4d23374466f7bd1de0897a29d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 01:18:42 GMT
ADD file:3dace89583571d938fe26db69a8298f77892aebb1a70e0e70c4df0d920e6711e in / 
# Tue, 02 Jul 2024 01:18:45 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:50:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 02 Jul 2024 01:51:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6b25364bfef282c79118e14cd54dbe5b982558a5939e2bdf63d94df980561937`  
		Last Modified: Tue, 02 Jul 2024 01:23:45 GMT  
		Size: 56.6 MB (56550979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bebf3b5ee4fc7445cb77fdf4fb4cb47ba2202118afdd12c9717312c0f227d074`  
		Last Modified: Tue, 02 Jul 2024 02:06:50 GMT  
		Size: 21.0 MB (20981632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26016ae5937fe37740b3fd6ff9a34640437bb4bff44a1627455139be3fe4ca32`  
		Last Modified: Tue, 02 Jul 2024 02:07:11 GMT  
		Size: 72.4 MB (72391083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:0ad683cbdb1b6e492abce84ebe3d406b4dc64a0b3bb091d9d5cadcb6317c7e03
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.7 MB (135676962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fcac10d16400adb64aa4ed98b52a743d727508be20eaa6fcf491ac7c420a56b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:31:50 GMT
ADD file:5f145818f2852834c826623d73119954ead96eb9bce2d43c78acb87643e22613 in / 
# Thu, 13 Jun 2024 01:31:53 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 02:02:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 02:05:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6ac783982847dc2f82c444819c90a10bdd382db79de84981f527e1462e567adf`  
		Last Modified: Thu, 13 Jun 2024 01:36:23 GMT  
		Size: 50.7 MB (50715744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1659c611213bc35c1eb01ea12d4ad271643ffd53f1e2e2bc4b26608a2487a2b`  
		Last Modified: Thu, 13 Jun 2024 02:14:02 GMT  
		Size: 18.7 MB (18705876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97fc926fbb86329f17c9d7a8101110c3dcd41d78ea4ae3f1d9f5edba14dde6dd`  
		Last Modified: Thu, 13 Jun 2024 02:15:27 GMT  
		Size: 66.3 MB (66255342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:10bbf4964ac4f29c8f72c1b5730b316de9f0cc56326afb136eeb95337204afaa
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.5 MB (140499141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:127ff97991c5094b28fb987042283e92cffcec56c5a2720ffb865faf49636e59`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:44:56 GMT
ADD file:474217365b4afce182f60b776ab37f3a44774c328ea278e1c48bc8410023f4c4 in / 
# Tue, 02 Jul 2024 00:44:58 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:36:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 02 Jul 2024 03:36:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c5f70336c1fb5eed68802971c844bdd7f3b8e20b7504d889927c061344c0235a`  
		Last Modified: Tue, 02 Jul 2024 00:49:53 GMT  
		Size: 52.3 MB (52278198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e1cb0f45994a8f1a86b716ad1a9e27bbe62bd52f2f3cd240600549728fbb719`  
		Last Modified: Tue, 02 Jul 2024 03:46:10 GMT  
		Size: 20.2 MB (20209404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d04e6243e34ae5a15b420d130874428d3e2bd90335a9f7c49eff8d32d63be20d`  
		Last Modified: Tue, 02 Jul 2024 03:46:25 GMT  
		Size: 68.0 MB (68011539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
