## `buildpack-deps:sid-curl`

```console
$ docker pull buildpack-deps@sha256:5e6129ac87e269b5561e7ad596af45961afb66a845839e706ebce2dba6223b15
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
$ docker pull buildpack-deps@sha256:7a67ecbe19a35c6d0516d7a1754a5065d4d2d159b9f0c541a43badb494f8413f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74647773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:817eac69051abd33d63732cca0f6a59cf558e4041ae4e1f230c87d396c8e7feb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 23:47:42 GMT
ADD file:6261ecb921e04d2b3f6fd44e5dcb5683154bc0beee4f26913c2be9395a060489 in / 
# Tue, 02 May 2023 23:47:43 GMT
CMD ["bash"]
# Wed, 17 May 2023 00:22:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ae396e350f30e1defad1bfa67a84b97389d42cf3442551e39a0e2bab6b53a50c`  
		Last Modified: Tue, 02 May 2023 23:51:56 GMT  
		Size: 49.3 MB (49299270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5394399a653714edce416717c938e83945318e2f603216d0c47c5ede1fbf955`  
		Last Modified: Wed, 17 May 2023 00:40:35 GMT  
		Size: 25.3 MB (25348503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:5eace7f2c0b54a2c519ec4827fc2c3b9c3f9b398a0b732c5b09469b51103211e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71176804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:109dedbc736aa9441000af8e52836c5cc7401da2c36b450ab4ea015c17ac4121`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 22:49:00 GMT
ADD file:2228a07c6ec82db1e0719684d77cecf448c3be947c2b1b48347ba5de9e5b57f8 in / 
# Tue, 02 May 2023 22:49:00 GMT
CMD ["bash"]
# Tue, 16 May 2023 23:52:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:90d5a5fdc15637fce928afc279fecd9adb82fe3c476f174458fc6bdd7fb4b57e`  
		Last Modified: Tue, 02 May 2023 22:51:47 GMT  
		Size: 47.2 MB (47167062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af3aabdf1b5f4fe267ba781854e71260b46210e5625adf002fe5ff5e24865561`  
		Last Modified: Tue, 16 May 2023 23:55:08 GMT  
		Size: 24.0 MB (24009742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:ad4c6c59c133f1c83e14408415c245a9d5979d6819ec6ea8a8728984c0ac9c1a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.2 MB (68207302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14b2f14477abcc375179b85adb2c0635d942596b2e833f3c64ee20ced09cf7f8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 23:48:42 GMT
ADD file:17739fc730ad8febc64f53eec61cbf10f8d2c5184cfda5466e89ab423a88f9d6 in / 
# Tue, 02 May 2023 23:48:42 GMT
CMD ["bash"]
# Wed, 17 May 2023 00:02:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b0b827c534260a55126ac3b18c14ea9160a3a3a03448b5c2b4462f9f3f4cf0ab`  
		Last Modified: Tue, 02 May 2023 23:53:05 GMT  
		Size: 45.0 MB (44988077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:858686fb647755cfaf9d97846212a8b1056f291d77f962bb8bf7be5d16a5ff60`  
		Last Modified: Wed, 17 May 2023 00:24:35 GMT  
		Size: 23.2 MB (23219225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:6a6dac9d42b7c53559b3ca1d7b732bb0b695f63eed184208d68389214e97d5d9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74241694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c338752c55db0af26e8cc5b4608eb514f07874903cbf8e46505304f1147bd155`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 03 May 2023 00:23:28 GMT
ADD file:cb107aa90220a9fc72fe1e3aa26878752691d6e9eb04696738920b5834c6d9e2 in / 
# Wed, 03 May 2023 00:23:29 GMT
CMD ["bash"]
# Tue, 16 May 2023 23:42:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:77a3c1a83d83f65ef8fd579d19879f09a4018e384f42cfa55f82d426f32ff840`  
		Last Modified: Wed, 03 May 2023 00:27:15 GMT  
		Size: 49.3 MB (49345262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f52781deab323ab07663419dcbd3af52651bfaf9895ae88fa6160c7a78b5c7c0`  
		Last Modified: Tue, 16 May 2023 23:57:13 GMT  
		Size: 24.9 MB (24896432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:b67005e28910dbabece72e3e56338a0719748d6472156af4e33639e1ca5c712d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76514485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d5aa7327927da33b24bd71991a3a0dc2bfa26adf1d417e8d78b77b7e364d96b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 03 May 2023 00:01:59 GMT
ADD file:4abf127b0d4037b2d94457a8ef168165ed6946fec0635fdaa845ed4ee8f74681 in / 
# Wed, 03 May 2023 00:02:00 GMT
CMD ["bash"]
# Tue, 16 May 2023 23:43:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:125509149936f5c9fc010cb99811f5cb23108af74e034fcf0903d3f2cc08d893`  
		Last Modified: Wed, 03 May 2023 00:06:56 GMT  
		Size: 50.3 MB (50321774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac4a96d98aebd4e76698b47d9e1a7e5c5b576c22314cb670e159aa6548a7e385`  
		Last Modified: Tue, 16 May 2023 23:47:11 GMT  
		Size: 26.2 MB (26192711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:3c5351c86676fc15bfeeddd4b3539ca51d71a9f79c1369cfbaf4c5bb9cb9209b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.5 MB (73508408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b8dc51d8d676ac8561aa1546d6171af3c2e0e84db4a0c32df99c20c4326a290`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 23:50:24 GMT
ADD file:3eff171361a4eb801d0fe38f81ca109a46285fd25a23f84aa338364d49c0591d in / 
# Tue, 02 May 2023 23:50:30 GMT
CMD ["bash"]
# Tue, 16 May 2023 23:54:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6ad09064fad2597f74f486eca3ca74c1f51072bf61093439cd70c0d5735689aa`  
		Last Modified: Tue, 02 May 2023 23:58:51 GMT  
		Size: 49.3 MB (49301428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48c533f052cb6f9d390977495e5045e622d198eff3064421eab4a0476cb44dc6`  
		Last Modified: Wed, 17 May 2023 00:06:07 GMT  
		Size: 24.2 MB (24206980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:9b0dad1773a7141210c32e58f762950d197409d83b5ffdcb7dcbbd4367ec6321
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.4 MB (80356675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c57b6beb12d6f188e87cebd0c3330fa3be1587db86b68d3824040fff1f043b7c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 03 May 2023 00:32:10 GMT
ADD file:c9bb656a5f751ff13849f6ca569f657cfc8dbe757b270dfa6e9fe2181e699494 in / 
# Wed, 03 May 2023 00:32:13 GMT
CMD ["bash"]
# Wed, 17 May 2023 00:21:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:71d18ac463268aeb15f1776de10a379de577489dfb1022fc92adf6187695aeeb`  
		Last Modified: Wed, 03 May 2023 00:37:22 GMT  
		Size: 53.3 MB (53307234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7506675c561fa99ba9e7606e22d38016062b4e3ff52b88e0ce9cefa5899e7d5`  
		Last Modified: Wed, 17 May 2023 00:49:28 GMT  
		Size: 27.0 MB (27049441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:89182118121172098f2071d177699ef2494e242a8387dc1378ecca698a23da5a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (69043740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32774ae41a041365691835ba01ddb670a369069ccc6f4796e2176467eb0de60e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 23:29:17 GMT
ADD file:4e365b380d9cfb77573624c399d3376d19fa5c7028c44b681071b426fb1c6db0 in / 
# Tue, 02 May 2023 23:29:19 GMT
CMD ["bash"]
# Wed, 17 May 2023 00:10:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:29b183cb384ba20db9a991d4213be72a43fcec3d5fc87f259bd5719d35027d1b`  
		Last Modified: Tue, 02 May 2023 23:32:35 GMT  
		Size: 45.5 MB (45510102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb4bc7d7e7f388c0265540f089e7c67a7aa86c6f5bfac0e5c45d897f3d99df03`  
		Last Modified: Wed, 17 May 2023 00:21:16 GMT  
		Size: 23.5 MB (23533638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f42332d7070fca07c9a43c87c3e1e4be35007e18e2ee1ec965cf50828c638dd5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73028231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7223246d95616667392392e306855578fd402e194c7b5ffcd849329e38743c17`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 03 May 2023 03:42:08 GMT
ADD file:f714218b704bfe42a591f19c2fc0360b178732edfcd6b12687ea572c74b84171 in / 
# Wed, 03 May 2023 03:42:11 GMT
CMD ["bash"]
# Tue, 16 May 2023 23:43:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9cad3c2eaf2133414000bf2d83ce6816eb4031d5b81288493af8102df33f2e4c`  
		Last Modified: Wed, 03 May 2023 03:45:13 GMT  
		Size: 47.7 MB (47675884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0bab5e47182cd759c84de89b674a6e02b13aef910e9d07d034d7b802c36c2c9`  
		Last Modified: Tue, 16 May 2023 23:55:48 GMT  
		Size: 25.4 MB (25352347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
