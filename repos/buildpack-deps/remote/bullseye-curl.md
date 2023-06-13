## `buildpack-deps:bullseye-curl`

```console
$ docker pull buildpack-deps@sha256:e50e7b355da55408d742318086ee7dd09f56a893e1880e35079eb3e07f32b34a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:bullseye-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:4f506a79180d04630dbca864acf49f652d3d4f6f65b09a0552788660ccb29182
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70815494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6c098925de347118e323ed82795b2106da6e4e3fee1365a7c2cd0d296390a13`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jun 2023 23:20:54 GMT
ADD file:e530b0563ea53d97b2f28e62149a665900196f86611df99a88c7a8ab2097b95d in / 
# Mon, 12 Jun 2023 23:20:54 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 03:29:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:93c2d578e4211e82e47e7ada9ed05d1869a2362c6f7509f2ee8d91ccebfb7fbd`  
		Last Modified: Mon, 12 Jun 2023 23:26:08 GMT  
		Size: 55.1 MB (55055162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87e6f3487e1d7e61ee7a415e0ced4eb6f0b3484eb1e15a4339d110d3cadf899`  
		Last Modified: Tue, 13 Jun 2023 03:37:33 GMT  
		Size: 15.8 MB (15760332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:6a5559099cc883cc44cc4ccf28d5476d4552d4281d4f40e62546a94a511a3514
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.9 MB (67915423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92354b57e20325c0c72d6a12ddaaec64054b5465a3b899fa8ee05689da565f7a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:48:32 GMT
ADD file:9572a8fcb9c86e8a9dbfe623c732cc4ba1c4f5670490191a7e639a272d5b6e97 in / 
# Tue, 23 May 2023 00:48:33 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:15:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b053976742ca5b01bcefb7df8fc77a58d0becb4ce508792491574463930569c4`  
		Last Modified: Tue, 23 May 2023 00:50:55 GMT  
		Size: 52.5 MB (52546536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae14fc3c88d12fab00e99f27b0c64eebba1d2189ed894e16dc646bb11ce7b1e7`  
		Last Modified: Tue, 23 May 2023 01:21:39 GMT  
		Size: 15.4 MB (15368887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:167eaf11706faed925f6770b9344d5fb370f828606d0100cd037615e212dbdca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.1 MB (65086740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddae117a5256c119e502a5063ae083f4b2367d27596865a1bfbd424836d9ca59`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jun 2023 23:58:34 GMT
ADD file:6edc8f94d2ebc83d6081e1c4567963d0060a842c767eaff959a6e5c6d09247b5 in / 
# Mon, 12 Jun 2023 23:58:34 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 04:55:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:23807bbf2a5fd14b7975a9e82f4a5530bbba520f31b382cc4b4ce2e77e075ace`  
		Last Modified: Tue, 13 Jun 2023 00:04:02 GMT  
		Size: 50.2 MB (50218141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe3330bf88d2bbd0baa313813532130c140958ecb30e8bdd1d1a990d63261a23`  
		Last Modified: Tue, 13 Jun 2023 05:03:43 GMT  
		Size: 14.9 MB (14868599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ee960ca1be08a9547b096959e85df644beab81ccc6744ff48770f0d33f29cfd2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69450699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccce098a154b29a1f3bf60ce0c77e811fc1654850833035c9307677aee64e1ae`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jun 2023 23:40:22 GMT
ADD file:caddd2f40296ec5c1bf7487617ca8694cfff9a1d9b7484159e203b6514cb5f5f in / 
# Mon, 12 Jun 2023 23:40:23 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 03:01:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:663ccfaf62a5d7b997bca03d1dc6d5dfff01b9e0de08d86dbea8957ea92d7d16`  
		Last Modified: Mon, 12 Jun 2023 23:44:25 GMT  
		Size: 53.7 MB (53704136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:751c9c60873892c6128382a04355bf76576dd23d87e5fdad03161dba5a2db45e`  
		Last Modified: Tue, 13 Jun 2023 03:08:33 GMT  
		Size: 15.7 MB (15746563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:a0abc80f82c051e1c24f4eafaa4899562496f8146e7ed34fad576859ca93a3f9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72304065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebda5e706f7627f73142b4a46f7fa9178c04035a29bb4d4ee8850de0f1110a27`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jun 2023 23:39:39 GMT
ADD file:4b1f447e0b75fbe493bd68bb77b74f4ba1c61ac8e14226e3c511b3a1c3d5721a in / 
# Mon, 12 Jun 2023 23:39:40 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 01:04:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0997ae72d27731326552ad4699d630b4932f3d31abc07a62105a0eb16b54173a`  
		Last Modified: Mon, 12 Jun 2023 23:46:43 GMT  
		Size: 56.0 MB (56040665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f5dde02e53ba41cbb376df97a5a106dcdacfee9b317fa635acdef0e92431e5`  
		Last Modified: Tue, 13 Jun 2023 01:12:41 GMT  
		Size: 16.3 MB (16263400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:4bfe1bd232fa52d0d3927bf469124981cd8d5c11742b18c42331e601195e8644
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68790877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e13e418a67dc95d7579285ca1e295119dbd27d56863139a868bc24c04336881`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jun 2023 00:09:46 GMT
ADD file:7ba4829e0a582c8a2e5a1d362ca30cfba3fa2911594faf9598927255100965b0 in / 
# Tue, 13 Jun 2023 00:09:51 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 02:03:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ec034d426521af0a9addba08124f06b364f3364fd20ec9aec4e3364104a793d1`  
		Last Modified: Tue, 13 Jun 2023 00:23:13 GMT  
		Size: 53.3 MB (53270410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c6f4361e85b8c11a8c3186bfe513ee8546a5cc99eccb71ce813c015f5e68947`  
		Last Modified: Tue, 13 Jun 2023 02:23:10 GMT  
		Size: 15.5 MB (15520467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:3c6519166a9e4e2090695d4a11965b43865b30b27bbd4f6495c88ae175822fc4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75676820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92b59ce0d09310b7c9d23b3959cac6b2af2f5bc7f52f4a880f8133fa62d4542d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 01:17:14 GMT
ADD file:ed39869ee4bb8e1901b71feb9cadfe754e42304e134f2542e516e162ca710ec8 in / 
# Tue, 23 May 2023 01:17:17 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:51:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f530a46e89ee571046fe19b22f563df6c84a31f6593a1e6ed49dbd16e34145de`  
		Last Modified: Tue, 23 May 2023 01:21:34 GMT  
		Size: 58.9 MB (58923948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ab487ec97d3b4e6daa6d35b4bb8035441fa255fd4eb9e82e01142e91968e7ea`  
		Last Modified: Tue, 23 May 2023 02:01:01 GMT  
		Size: 16.8 MB (16752872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:4cbb2559219a71f1815a933346f8548179eb3fa1bc7e3cada8b0f50b0babd135
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68914023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f7096b88e5bbd28b8eee117b6967f9367f4d94618ae5dd0fdc78cbd5a2fdaf1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:42:35 GMT
ADD file:a054112be60c3f2d7811b27cde82bccfd1c2747f29b7611ee68b21cd9f3d3d54 in / 
# Tue, 23 May 2023 00:42:41 GMT
CMD ["bash"]
# Tue, 23 May 2023 02:33:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:44d1d02f91725dd9ae742f7c70add814dc3da3fde438adb01e65e1f8b0eba613`  
		Last Modified: Tue, 23 May 2023 00:45:33 GMT  
		Size: 53.3 MB (53282114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4000487deec97f7a3856b8eeb8f2984dff7a59cabf8346950db508cca6afadb`  
		Last Modified: Tue, 23 May 2023 02:38:46 GMT  
		Size: 15.6 MB (15631909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
