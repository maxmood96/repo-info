## `buildpack-deps:oldstable-curl`

```console
$ docker pull buildpack-deps@sha256:02d8488a10da7fd01311effa6af38c48b6313df91d15b4cd184869daf6220c8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:oldstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:238cbb1c4381f21d35228593283f3a7f2d1f68dc0d5640f46a87d4b140b79fde
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60513404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74d4bce9719f5816419885eec84869868cd1357c2c207c0f4d66e9de8b935517`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:22:48 GMT
ADD file:21bf6969c2166c361350c07b1089a1a4b34b7cd3e802a602385d83c49f44a7f6 in / 
# Thu, 23 Apr 2020 00:22:48 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:59:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 00:59:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:99760bc62448fbba69f6f0981d09bb4b7532e17362ecfb709141a7195d9b01d3`  
		Last Modified: Thu, 23 Apr 2020 00:27:35 GMT  
		Size: 45.4 MB (45375951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3fa264a7a881e244e7fd3420edda0d550ee3b26ed870f5c021d937497ffd602`  
		Last Modified: Thu, 23 Apr 2020 01:05:50 GMT  
		Size: 10.8 MB (10797279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a222a2af289fc1fe54c037f02e7651e0aead2f81f40cb2885786bfe57aed10a9`  
		Last Modified: Thu, 23 Apr 2020 01:05:48 GMT  
		Size: 4.3 MB (4340174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:b8f11af4cd3def2431b1560b72c073382e36c39af0c0d6e6b917f6adcf04f5b3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.1 MB (58093930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a027ce03570f4275e3ad1d7b257cc5f1e41abe0fca2627b63d2993ae005001e1`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 00:54:28 GMT
ADD file:c32e9d5ebedbf7d4d46c8547ec1385d73ff4bb1d974ef50c0f8b5eff16b5a6b8 in / 
# Thu, 16 Apr 2020 00:54:30 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 07:58:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 07:58:34 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:1f3041cb19a4c1ef6e07f5cd99b75e4a39e4467bbb70f15c5a0f391e26752e76`  
		Last Modified: Thu, 16 Apr 2020 01:02:13 GMT  
		Size: 44.1 MB (44068060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23d3830d6b9ee5a39d175e90acabdb00e95db1dde0ad55a7a6a2f613083ee9a2`  
		Last Modified: Thu, 16 Apr 2020 08:09:51 GMT  
		Size: 9.9 MB (9866674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dcaa03069fade4274b1c026a1a89b48bbca5a2acc893cb7959369ea62f92fc0`  
		Last Modified: Thu, 16 Apr 2020 08:09:49 GMT  
		Size: 4.2 MB (4159196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:9f969bf48361eb06d6b5ebf48bd7b6581a629825444cbfe394bf16ba2e036823
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.5 MB (55518404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d75a83bde16af7f7f79274488f96b287527f3663352bfaf6e6ee7048638cb9e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 01:04:37 GMT
ADD file:b83ed4f9f7c8b10eba728f85030722a771b39336afd7ff9eef2eb6b94791533e in / 
# Thu, 16 Apr 2020 01:04:40 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 01:50:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 01:50:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:37d8a5aac9ec54f7757e1243cff051c8372be0cf907e086fba2607e08d2a4135`  
		Last Modified: Thu, 16 Apr 2020 01:12:16 GMT  
		Size: 42.1 MB (42101227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3f4f4abba4245745ee86a35473696f5ecbe961a03af35bd6f07b2253c3bedba`  
		Last Modified: Thu, 16 Apr 2020 01:59:44 GMT  
		Size: 9.5 MB (9498336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3accf104e4ac412a36f3c1fc31fb94722661bf356ac878a4b502dc20086c8d2f`  
		Last Modified: Thu, 16 Apr 2020 01:59:42 GMT  
		Size: 3.9 MB (3918841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:7535ce17e2f77b9c0836bbbd1526a862b1cf8d6ec1ab98eb13844ed2babb6cca
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.0 MB (57002051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f84be3dd8e36cad9e62ed9f952584ec3b90ad153bde2db019fa8bb48110dce4`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 02:44:49 GMT
ADD file:6d09304a2db2752e78b9ce9610594102dc756aa4cd210f85bbfa21105c7dd88f in / 
# Thu, 16 Apr 2020 02:44:52 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 03:21:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 03:21:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:65d54b492d599e7c785a582a0f70195e1f09f0886e54cb7788f1021f383eb4ed`  
		Last Modified: Thu, 16 Apr 2020 02:51:10 GMT  
		Size: 43.2 MB (43159230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be35cdee43e0bbb89c0867d201ff274ba25b6ea9bfe7f8f0c1d1d6de36ab08a`  
		Last Modified: Thu, 16 Apr 2020 03:30:52 GMT  
		Size: 9.7 MB (9748442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b803ac2c0e69edab9b8db20bee0f9dfc0191a7975c94d4d2ea0088d5a1759be8`  
		Last Modified: Thu, 16 Apr 2020 03:30:51 GMT  
		Size: 4.1 MB (4094379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:64c50404ec21fdf8b6fe72868ff0915c901dc8afa6924c1b8eba533907a384f7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61474497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d511533d7b62a50de0efe2f3434b4b5ec5f56fcab394a4889ed737afdfa276e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 01:43:06 GMT
ADD file:298a4dfec0058f9502705ebab6ca3787b1bcb5845d21ecfcd1771505b061b061 in / 
# Thu, 16 Apr 2020 01:43:06 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 02:33:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 02:33:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:aedad1667b3098c616b8251fdfca8170596731152b6043a01601df826b79b4e0`  
		Last Modified: Thu, 16 Apr 2020 01:49:17 GMT  
		Size: 46.1 MB (46094897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5a13ff1ee1a9968ed086324092c33ec123f94ecb99ccede500342483418d840`  
		Last Modified: Thu, 16 Apr 2020 02:40:58 GMT  
		Size: 10.8 MB (10818136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6cdc434eb33063a8439a59c1a179e4fa3c9d968ee9a3ad4e2ff12714e1b77b1`  
		Last Modified: Thu, 16 Apr 2020 02:40:57 GMT  
		Size: 4.6 MB (4561464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:03e8bbdecd8906effedcd0592d8d89c8a4045ac503879bb6d6a87f663cdbb8b5
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59269890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d8f0a1c7a6c759a4420c53a972758c43c52bd34c989d00bea7bdbd099a8c744`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:12:30 GMT
ADD file:076cd21ba96c7d91a0af4f716c8309a9b092cbbcd4c11f5ead2e2a91dae43736 in / 
# Thu, 23 Apr 2020 00:12:31 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:00:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 01:00:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:3535f2056d5540d877f08809fd21e68e9db2ecaa1af00cb85b4522a16c35e414`  
		Last Modified: Thu, 23 Apr 2020 00:22:41 GMT  
		Size: 45.0 MB (45048818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e3b44e91d14a9d07b503cf60d0ed04ee5d11eebacef157dabfa2c6d4a62fed`  
		Last Modified: Thu, 23 Apr 2020 01:17:13 GMT  
		Size: 9.8 MB (9826234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ecb2ad4ea35a7a01e57dfa74ff5af3cdcfad24105d385a7b475a3d0a9e9f4e1`  
		Last Modified: Thu, 23 Apr 2020 01:17:10 GMT  
		Size: 4.4 MB (4394838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:e4869bee27b110319b6d14e892e311ed58e01fb046422076e1b132d5ec5023c9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59945063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa1eada6859f0cfa64d2cacc9febc814119f2753b44d8ae7604068e22413441a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 01:43:04 GMT
ADD file:d4949f465ac0dbf2adcd2e1b8f1d0feafefbf5ca291cc71952eb3ad16ee14985 in / 
# Thu, 16 Apr 2020 01:43:11 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 06:02:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 06:03:24 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:3071a1f69d49da5ef8731d119a68201faab21b496e239d4b67677cf66ba3d98e`  
		Last Modified: Thu, 16 Apr 2020 02:03:49 GMT  
		Size: 45.6 MB (45646020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9c622e17c315eff3fdebc5db0e9b85f745434834b8f6f35fb284c0a6415e40a`  
		Last Modified: Thu, 16 Apr 2020 06:27:24 GMT  
		Size: 10.0 MB (10002451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be3d6b2c6b9995d22ea2928ba6dac51748f74b7c8ad0c833e2f3e31530bbad5e`  
		Last Modified: Thu, 16 Apr 2020 06:27:18 GMT  
		Size: 4.3 MB (4296592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:bd461c2eec8fd175a12dbe458f6feb108a82888f39ab1db5a0333f21515e9ea2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59930887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:571100bb5fc3ad197d73b30d1f8f132abc10eaaeb37374ea4ff8e875c68c5ecd`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 00:43:47 GMT
ADD file:bf54e49d85edbe8d61bd9e868d71faf0f26b4474f23eda7b692abfaf7aea50a4 in / 
# Thu, 16 Apr 2020 00:43:49 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 02:02:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 02:02:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:b4e6598a8ad88c3d661d89d6fda41ee33a54f3c6f16c4988cceaa6fd0afd04bb`  
		Last Modified: Thu, 16 Apr 2020 00:48:18 GMT  
		Size: 45.2 MB (45232626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9cb98b0a4ec56e95b4ba3f3261ba975cd69e2a0240149eb53e4bbff9739e272`  
		Last Modified: Thu, 16 Apr 2020 02:08:04 GMT  
		Size: 10.3 MB (10325610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06c82c0f221bc14891b71387b7587fd4f2a615d339ecf0afadce350f82b3e098`  
		Last Modified: Thu, 16 Apr 2020 02:08:03 GMT  
		Size: 4.4 MB (4372651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
