## `buildpack-deps:trixie-curl`

```console
$ docker pull buildpack-deps@sha256:aaad3e1a778f02632ddaf5a1f4d002c6b5b0dfccb32d8bd88c9dd4eb423a5d32
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

### `buildpack-deps:trixie-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:9c75b7563b930bff763dec4ea7b9f97261b6d7aa446202240ba8ef534e5ca738
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76075117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdddb18cc17a290f069ecafd4676bfe129e5f2aaf4a9b7a28cf96ae52cc8ce1c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:37:59 GMT
ADD file:8ad3e26aeda90bbd087b64f3a0110c8f2e520a774d62a26d5aeb7c5006e472ca in / 
# Wed, 31 Jan 2024 22:38:00 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:29:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a946c083680d9a81b8eb8383bbc21cd34444b1c5f3212c5d3fc463e0220d7b73`  
		Last Modified: Wed, 31 Jan 2024 22:44:39 GMT  
		Size: 52.3 MB (52283197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2aaa07716edd95aa6e78fbf886a2b62004144888c2eb3728580637af2de7642`  
		Last Modified: Wed, 31 Jan 2024 23:36:36 GMT  
		Size: 23.8 MB (23791920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:df7c9595206514a99d2f1bd89d012f4e3721ac1bca68b8fa08ae914590399d81
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.1 MB (72133500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8a97c53229b5026c5850603dac3341aa7c22673919291795678b49880673df0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:46:08 GMT
ADD file:7144257253ce293f694d917fb06ea4d03cb3cffd94c432e47fa5a77e03a5a2f7 in / 
# Wed, 31 Jan 2024 22:46:09 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:20:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9be7d01dbe3e5ca74f21aad18f318e9da338902efa0bdf09221df8cf061d6b3a`  
		Last Modified: Wed, 31 Jan 2024 22:51:27 GMT  
		Size: 49.4 MB (49400791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a34997ca134aedbce87b0387fb6c33340c58bb878c2ee87be402220de4c0f68`  
		Last Modified: Wed, 31 Jan 2024 23:26:16 GMT  
		Size: 22.7 MB (22732709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:adff5af2e421721f0594d2a1ddc5c0065cce13204c3217d549dc07d16d49f0c7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68943434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1fdc86f6449d18128d083311849af2a1f51b49709a333dd1e7fd287fa54a526`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:47:01 GMT
ADD file:313528f956e019639cb41933c0f6d14e7dca01353fe4ca789d7ac69e4c131ccd in / 
# Wed, 31 Jan 2024 22:47:01 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 02:55:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:30dca4c17f72b09129956e26ae0841f8c684bf0810e63983ab453762044c668b`  
		Last Modified: Wed, 31 Jan 2024 22:53:21 GMT  
		Size: 46.9 MB (46892605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43baa7a4e2b9b0f5f9670286f20f999f396d37b58f26795cb62ee2e3cb4647d6`  
		Last Modified: Thu, 01 Feb 2024 03:02:59 GMT  
		Size: 22.1 MB (22050829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f94442107673ba98dce40ae18bb0c5157589f8a0a31969039f0f47ab8966952a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75698646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f425a02055ba9a29659238a7d2d0ecec6c60512085fda16ab27c4c4010774c04`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:46:18 GMT
ADD file:22615a550fb316cdf09ee3c185139fbdb9bf6b776c7f96bba26ba5cc5b14fbb4 in / 
# Wed, 31 Jan 2024 22:46:19 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:49:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b24f8e2b921fe314282df3bbfa20988c1046ee499441de80fd5229551987d1eb`  
		Last Modified: Wed, 31 Jan 2024 22:52:31 GMT  
		Size: 52.2 MB (52161387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3734a145b10aaff86d0b31ab8c862448f17bd19fd0bf41ea74f065b5217e8d0`  
		Last Modified: Wed, 31 Jan 2024 23:55:53 GMT  
		Size: 23.5 MB (23537259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:9a5f681bfc51b9fbb37b5825f5edd3c78d648e5e6b96c961f114d9bdba6db757
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (78011698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59c048c496b2873336578aa7b7c5d880581b7d6776b96ef8b295414496db2ccc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:41:43 GMT
ADD file:443c10cf2bd14299f3b496a80df4429c5642d898fb2f3e8c184e8c4d58fb8cd2 in / 
# Wed, 31 Jan 2024 22:41:44 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:42:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c71e0026d29ede0429851d35323a9a769fb82ad7760740b559b172f3789ae3b7`  
		Last Modified: Wed, 31 Jan 2024 22:49:09 GMT  
		Size: 53.1 MB (53140039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e20811788aefb929a0e339e49aea232089bba4dfdd96c9f7d13061e0608071c`  
		Last Modified: Wed, 31 Jan 2024 23:50:35 GMT  
		Size: 24.9 MB (24871659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:34138dd064835e205f758b372bb4e6b3290e8c786bbda787488b9cef9c377e6b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75553043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d301258f600a50dbedeff7d57cf964de2e97346c4fd9829d8d4193c4e0fd8e6a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:34:03 GMT
ADD file:534203d126346e48b8c0d0430dcecaa093294a7a3c98d571701aab3e6c36d391 in / 
# Wed, 31 Jan 2024 22:34:09 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 07:36:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b3d1be35073c977f0bb775d26df73db32aabd06a76b52f045f43c249f737a518`  
		Last Modified: Wed, 31 Jan 2024 22:45:28 GMT  
		Size: 51.4 MB (51373756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b29775ff2e6dca77fd66e0ebc9778fa50a528946fea171a8991f404341704a4e`  
		Last Modified: Thu, 01 Feb 2024 07:55:48 GMT  
		Size: 24.2 MB (24179287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:118430b1869f01f710d0c4107bcf6c221a7afd930c73ce730bf12e95fbd8e2ca
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.4 MB (82391924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:123f43854fa4a7022ab1f801e519f2be0edc86e84bf3ae9dae0a8328ce2f94c4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:32:14 GMT
ADD file:9862d7fda5f3fc5c48229d44a182f0619051f084c461b10ae5cd841f609dd876 in / 
# Wed, 31 Jan 2024 22:32:17 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:42:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fbf7f53bb9540a00260474ff7da2e470dc3eecfdc9849d2cfb73bb9e5f549622`  
		Last Modified: Wed, 31 Jan 2024 22:38:21 GMT  
		Size: 56.2 MB (56198785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89ba056f52a3a3f9fb8ddeab8c15f4923d3aee8ca28982082fee3b8e7078539e`  
		Last Modified: Wed, 31 Jan 2024 23:51:34 GMT  
		Size: 26.2 MB (26193139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:01ceae4114d87a829e01a45909ca6970bb8c733e9f15a76c9d80d4ce9e572630
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76562018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84aa229d7bfb226c57feb7c30b4d271a72fe2a3d27c7472e75a152214eb08be8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:18:29 GMT
ADD file:3b31c2bd33a3d7e6352823413292afa26a09dbcdbc56396202701f16e609204c in / 
# Wed, 31 Jan 2024 23:18:33 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 07:46:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:651c4bce8b545a7028c9eea81f8b25dae93c9bf0073fff7020f5784448310184`  
		Last Modified: Wed, 31 Jan 2024 23:31:42 GMT  
		Size: 51.7 MB (51697772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a8bef819e59def6e5aacc1cfae21f5a548b594589a04dd83f55049c50ac9a9a`  
		Last Modified: Thu, 01 Feb 2024 08:22:11 GMT  
		Size: 24.9 MB (24864246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
