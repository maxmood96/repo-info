## `buildpack-deps:unstable-scm`

```console
$ docker pull buildpack-deps@sha256:d7084ff2b88f835e98b854926768223091de7ee5525fcd48dc174f94f94634f2
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

### `buildpack-deps:unstable-scm` - linux; arm variant v7

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

### `buildpack-deps:unstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:1cf41ee43f2dcebac58d3d31699511f01cb1fd6c33e6b87e9efaa2eb8c588c2c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.4 MB (138445772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8a0753a5fa3df21365b12d290b55a52348ba29f83267c404d1b3a1b16cfc217`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:53 GMT
ADD file:0df3518c1c665e2879ed3c7b7c5961b53fc28709cc135a245b209411a275c037 in / 
# Thu, 13 Jun 2024 00:40:54 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:25:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:26:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:844667f4b2125bd419ff2157667c09ca5b8d442b399e2db99e62277881555d82`  
		Last Modified: Thu, 13 Jun 2024 00:45:41 GMT  
		Size: 52.7 MB (52683111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de631d800a2d5597fbeefa6256f2a1b9ec1248adc1daeb69a836e05978fa6d5c`  
		Last Modified: Thu, 13 Jun 2024 01:32:52 GMT  
		Size: 18.8 MB (18771377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d43c1cffc0bde8580055dfb72c20e5ff7b0e65c7530d279c7ccb77fada1a6f`  
		Last Modified: Thu, 13 Jun 2024 01:33:07 GMT  
		Size: 67.0 MB (66991284 bytes)  
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
$ docker pull buildpack-deps@sha256:d5b3761a2c69c40a67cfe43d555d91639833c674141e152e0902b90ab666b06a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.6 MB (136584514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cee1a4671781997c0c429a87c5300817b20a91aeae4bedfcfc8697ee76951f3c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:13:44 GMT
ADD file:bc1c5f4f7dc974780be655fc08cd2e36c5d04921a942dd0065534fe0f2520661 in / 
# Thu, 13 Jun 2024 01:13:50 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 02:17:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 02:19:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:371a3512d511da5522a67af4d5945c86f5bf5015bc3be3dfc08ea50797400367`  
		Last Modified: Thu, 13 Jun 2024 01:25:20 GMT  
		Size: 51.3 MB (51279195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52e19ab65511529aa4e809a989c916e7d1eea56540a36758da55666b6d063b69`  
		Last Modified: Thu, 13 Jun 2024 02:42:33 GMT  
		Size: 19.5 MB (19513685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a59683027da59c0bb0526447861a6a715f53ce57d4a231feeedcc859064169e`  
		Last Modified: Thu, 13 Jun 2024 02:43:27 GMT  
		Size: 65.8 MB (65791634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; ppc64le

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

### `buildpack-deps:unstable-scm` - linux; riscv64

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

### `buildpack-deps:unstable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:48f217bdc48e4ae27359b00644f902d584272e1fdc115b214bc3bededbf46420
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.3 MB (140308743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18108f3d86f384cbbb190d0c4a6eaa845d4a8744be40ef032068666b13e5318a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:44:00 GMT
ADD file:48df1edc9b73475781ccac0eb967ca97c87c5a3132a7c9058519fad686260867 in / 
# Thu, 13 Jun 2024 00:44:02 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 05:25:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 05:25:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:f539c970b22ae85b0b82128798f27249002cae24f6d005cd8df7e2098a346a0d`  
		Last Modified: Thu, 13 Jun 2024 00:48:56 GMT  
		Size: 52.1 MB (52054394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98301e222cdd3787932e298432980b45832dc8bafb525d89b9f56907acf79064`  
		Last Modified: Thu, 13 Jun 2024 05:32:33 GMT  
		Size: 20.2 MB (20215760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25c89dc2e12ec49de6459e71f70fedab5f35e68d27cc98813aad170a96c48ead`  
		Last Modified: Thu, 13 Jun 2024 05:32:48 GMT  
		Size: 68.0 MB (68038589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
