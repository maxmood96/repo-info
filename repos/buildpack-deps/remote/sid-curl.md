## `buildpack-deps:sid-curl`

```console
$ docker pull buildpack-deps@sha256:4a90eb18841f278ad65d8ad1ea205c5c5f1c3fd90523815c80098838dcff924f
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

### `buildpack-deps:sid-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:35180b369e7edd104c37283709a781464901c9e4595ea40a760fb26fefb7a5be
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71657361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:672b397c199a6d0cf7ffe147a8b8d28c0eeeb5424ba92e27859c6965f1d45df9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:57 GMT
ADD file:cf83030bc061e8d24d8a36b4edb2846333916985361600a06dfb635fd59c8068 in / 
# Tue, 02 Jul 2024 01:25:58 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:52:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
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

### `buildpack-deps:sid-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:d7efe6058ae592d240b80557c609b94f92cdc25aabc3b5526382cc13b6e351b7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67667143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4870049d5430e9ade2158c11b37bc777ea21f540a10e034c99c5f999dae5d81b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:49:07 GMT
ADD file:e97cbdca31cc34df027df8a29da79dec8686613556a85f9e94434bf7952452ff in / 
# Tue, 02 Jul 2024 00:49:07 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:17:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
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

### `buildpack-deps:sid-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:6b7c8ef0cb2cc641c0ae66bf80c594ade531cbc2aa7c30b064d8c2fe548d2ea9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.5 MB (64544580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0235667726fd763e388e177e9c4e8488248c6c20a9f195bd303e266f62e33d5e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 01:00:51 GMT
ADD file:204b9bd9d9bd808b15b0257739243338e223ade24ac2085e9c4ee95ac07d2795 in / 
# Tue, 02 Jul 2024 01:00:52 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:28:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
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

### `buildpack-deps:sid-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:565aa9075ce6be708b8c521144ae8c1767a8ed5942f3f8b1295a4493b60f0a57
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71653110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cf790b8c8dcd40de930e7bb2cf6fc241552c0a3335cb4b13d3fb229e4becf95`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:40:14 GMT
ADD file:13d2e6714604c76eb37d955b64f923c5e9360ac3b98a7115cf15ce9e648a1a56 in / 
# Tue, 02 Jul 2024 00:40:14 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:53:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
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

### `buildpack-deps:sid-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:cbc03a326c4aa319c2a6bfe83b30a11d3a62514702bd17ce1f357463b74c9342
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73552375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5011edc87b1292ae58d52ae559fac0d4f36ae571cdfae864aa59d64c990f8c29`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:49 GMT
ADD file:a08584f3c5024aeb655047534f24f132994ce1978bc3c1b585197931050df05d in / 
# Tue, 02 Jul 2024 00:39:50 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:09:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
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

### `buildpack-deps:sid-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:e7c43a09e343f764f95d8f7bf39d4787362c24ef2a04b0d785f144e13704d64a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71006046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5dcb71db070af56e5623509f744a46602d6d0a7d68c7f875d8cbe8b3254dc51`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 01:21:34 GMT
ADD file:38ebbca2b69d1a13c63e4290834a1071ff05cbc6ca9d34fccc4e1db7ea4e713f in / 
# Tue, 02 Jul 2024 01:21:37 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 02:12:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
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

### `buildpack-deps:sid-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:621a41b7c86329978d58a0020a381ab46c4156357c7c1bfee22d792b01641c23
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.5 MB (77532611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44387e12bd22778e77d7e76dfd1172a3acded23a686886e54fddf4ae0d27dccb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 01:18:42 GMT
ADD file:3dace89583571d938fe26db69a8298f77892aebb1a70e0e70c4df0d920e6711e in / 
# Tue, 02 Jul 2024 01:18:45 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:50:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
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

### `buildpack-deps:sid-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:a5400bf2c9e5726109720d30527c96303f01fe54109ffcb1b08783471ee26ec3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69421620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0299e6f8b131914ed98855e3c32289e7c65840c305b555b6f722c760299539aa`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:31:50 GMT
ADD file:5f145818f2852834c826623d73119954ead96eb9bce2d43c78acb87643e22613 in / 
# Thu, 13 Jun 2024 01:31:53 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 02:02:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
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

### `buildpack-deps:sid-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:1156dc637809083ca89fc5e92971d6c5053dda32d04b659e9a45d0e8731ad93c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72487602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3660c5bf0430b4e3b8726a2aaa1b9b0260435ae0ca1f11125cfcb84889968521`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:44:56 GMT
ADD file:474217365b4afce182f60b776ab37f3a44774c328ea278e1c48bc8410023f4c4 in / 
# Tue, 02 Jul 2024 00:44:58 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:36:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
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
