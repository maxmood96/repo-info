## `buildpack-deps:lunar-curl`

```console
$ docker pull buildpack-deps@sha256:8c67c8ee3e76fc5a1d136122c8fd5b00736c48adc9cc85fcc2e35acc4b455570
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:lunar-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:4619b36099f9a6e5b99f2c03435877a36a1081b81fec753b8f31138a168e4d27
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 MB (37943069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c564d96298adfcdf101f37fc6da744ed339ecf7dd9bbb963c1016cca38a8da36`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Dec 2022 01:20:50 GMT
ADD file:3a69ab43af761d2eea701ad591edccb2b1f84ff63a25059ad9d5bc53358dedc1 in / 
# Fri, 09 Dec 2022 01:20:50 GMT
CMD ["bash"]
# Thu, 22 Dec 2022 19:26:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Dec 2022 19:27:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:a13f57ee816c77bd77798d728a3d73246552cac763e9c613b26aecd8441e43e6`  
		Last Modified: Fri, 09 Dec 2022 01:22:25 GMT  
		Size: 27.5 MB (27505626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb206e2c65ae53b38b00dbe71e2c1e6bb7b54b88640624201c2b86a1f5847b8`  
		Last Modified: Thu, 22 Dec 2022 19:32:28 GMT  
		Size: 6.8 MB (6780053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d01a823ce10ce5db3cb9c09adcc98b1c550a3ffa8adab1c26c5ae3eda5c0e65`  
		Last Modified: Thu, 22 Dec 2022 19:32:28 GMT  
		Size: 3.7 MB (3657390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ec28cd16d61a601f670e4edc7ab9202329a4c6d9891376bdcbfde9f6044db722
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37054939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa7b4e39950f35d0d8564dcf93b64d418add2134fa6563d7b59a0d3fffb4072c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Dec 2022 01:47:11 GMT
ADD file:7e5379395d9cd9ee04e9f4dcd8e394c2d1c29e9491757a29f4e37f807d3635c9 in / 
# Fri, 09 Dec 2022 01:47:11 GMT
CMD ["bash"]
# Thu, 22 Dec 2022 19:46:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Dec 2022 19:46:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:6101eb5b766f68aef80c6b84dc902199e26926e7dc981aa0ac38cb1c3075b5ef`  
		Last Modified: Fri, 09 Dec 2022 01:48:40 GMT  
		Size: 26.8 MB (26825777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d47c5b275711c889982121dbce8e6eb1df30a49c0cda62485bca0531a1823f6`  
		Last Modified: Thu, 22 Dec 2022 19:52:52 GMT  
		Size: 6.6 MB (6609996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1aa323bbd3d0e560aa576969c1bf8bbaaf5ef7b2c159c053e97229a8f208a2`  
		Last Modified: Thu, 22 Dec 2022 19:52:51 GMT  
		Size: 3.6 MB (3619166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:3fadf854c2ffd33c27b86afa44e7846ee17c8c407078260ec37f5423c7251907
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44237882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:666bdc2ff072134f50b39b801d14ea74e6d4c776abd87290e2b1efc83814c77a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Dec 2022 01:28:29 GMT
ADD file:fc908ee01c16840b84760d5041e467ede6748c61754d04faa691f9fb6ddf1686 in / 
# Fri, 09 Dec 2022 01:28:31 GMT
CMD ["bash"]
# Thu, 22 Dec 2022 19:40:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Dec 2022 19:41:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:08a75ad1a4a23cbc8eccc791fdfae97d71a324379cb275562275520611a56654`  
		Last Modified: Fri, 09 Dec 2022 01:31:25 GMT  
		Size: 32.1 MB (32104472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70c870358a362895034ccb4359831dc39366f11c4609b717d9c3a44e0282b11b`  
		Last Modified: Thu, 22 Dec 2022 19:49:56 GMT  
		Size: 7.8 MB (7754835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0d292dfd312b20bb9ad0a639938aaa822a0e0a09f07b775ef818d1c3483fd4`  
		Last Modified: Thu, 22 Dec 2022 19:49:55 GMT  
		Size: 4.4 MB (4378575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:2dc7c36ef51ed743a2eaddce63a69e2ef54975ed28a5ca8b3a3ac854fefd7645
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.5 MB (35505045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2333fa6aee4d03524f15ac7f2afc828afed0b811e2c1a2f87bde341ec46a21a6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Dec 2022 01:17:04 GMT
ADD file:dd674b2aba3f7d1f5bb21fe7f9173314f05007fa6b78d8efec97661a9bf7c748 in / 
# Fri, 09 Dec 2022 01:17:06 GMT
CMD ["bash"]
# Thu, 22 Dec 2022 19:12:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Dec 2022 19:13:16 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:6ced4571d7775ec15e8b89c410d607207d53803f56e764a02dbbde02cd345dd4`  
		Last Modified: Fri, 09 Dec 2022 01:40:36 GMT  
		Size: 25.7 MB (25674343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bb4476ae2074d1e5bb1f9442f0da2cf6977a81ea5526eea5879a654cbd20eeb`  
		Last Modified: Thu, 22 Dec 2022 19:21:32 GMT  
		Size: 5.9 MB (5927559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd258f4dab88306e41aad9845768a49cd66889bc363a5f1a5cd03af38a7bb7a`  
		Last Modified: Thu, 22 Dec 2022 19:21:28 GMT  
		Size: 3.9 MB (3903143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:80777d89198f3b4cf9cf0779b7aed1dcf92003547f66f596e094b9d6ba106d7a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36170675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0228c7f65e1d40071b3dc215235a91004dbc06229bdc5727951d243f3075dfe6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Dec 2022 01:53:35 GMT
ADD file:34ba36266e3f51a04f8105b97312cec6ad0e02db549c1a40af7b2b9b8b4527fb in / 
# Fri, 09 Dec 2022 01:53:39 GMT
CMD ["bash"]
# Thu, 22 Dec 2022 19:53:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Dec 2022 19:53:14 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:40f085afd82295659f70518a511d2ea24258833fac78ee993694322605814e97`  
		Last Modified: Fri, 09 Dec 2022 01:55:38 GMT  
		Size: 26.1 MB (26064347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b4ff57ac87df71f9147afd569d5c780b3c46584d3ae2a7ca33d038e5b2603c3`  
		Last Modified: Thu, 22 Dec 2022 19:59:01 GMT  
		Size: 6.5 MB (6463110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09dcb825ede09e4c615483b46aaf77e56e707f1a2e30ae7027eaf43484859483`  
		Last Modified: Thu, 22 Dec 2022 19:59:00 GMT  
		Size: 3.6 MB (3643218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
