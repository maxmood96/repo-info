## `buildpack-deps:buster-curl`

```console
$ docker pull buildpack-deps@sha256:ffd3c5f81c7105727e2d10230693d331a94b318c63023d3db806d6516f054170
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:buster-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:ec7169f4c7701eea410a91ca9cb2c646a343a0348ac7e832c31bd9916cd9bb29
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68309652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77e2c3e5851248ac9a124fd4b5f7fbd012b3f0420beb48e0e07dcb6dbd424451`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:21:05 GMT
ADD file:00d8a84de32d523b936621886a10683664f38d8ec0846a60511fcf3a99d0e0c4 in / 
# Tue, 06 Dec 2022 01:21:06 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:15:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:15:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:620af4e91dbf80032eee9f1ff66a8b04119d7a329b2a13e007d69c8a0b337bf0`  
		Last Modified: Tue, 06 Dec 2022 01:25:30 GMT  
		Size: 50.4 MB (50448865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fae29f309a72482bf13fbb1a8f4889ab9107fcad0c9fda76586aa55445e93ded`  
		Last Modified: Tue, 06 Dec 2022 02:22:49 GMT  
		Size: 7.9 MB (7859378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28fca74d99b6532401bfe63d36e1bafb1ac839564d48aa4e6e0a6aa2706a4d12`  
		Last Modified: Tue, 06 Dec 2022 02:22:49 GMT  
		Size: 10.0 MB (10001409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:32d3f0264b1f587d1e4295569e5c23e27a7d2652a3b5d74a34259d0c2e84b366
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62412203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4289d9513dfb8695e331c05054183ff6b9f4fded46d48a89ee3fbd0047556627`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 00:59:07 GMT
ADD file:ee219183e8f6a070cc7dfe54397117bf655fa7e49d4a4bdf4263def0bf115d26 in / 
# Tue, 06 Dec 2022 00:59:08 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 09:51:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 09:51:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:9b267c960f47219a48e4194e0bb9cf819bb30aeae42c7f03732421b84855f2d3`  
		Last Modified: Tue, 06 Dec 2022 01:06:29 GMT  
		Size: 45.9 MB (45915455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b354c1a0edada6fedfe5eb9da51dfd01ed7f2a264e0d2af7227244e2673c4bd`  
		Last Modified: Tue, 06 Dec 2022 10:00:50 GMT  
		Size: 7.1 MB (7147798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:602ec6c8b9b029da92c6a3ab86cb03b7f1144a9dc62cac2535ba3491b2bf2ef9`  
		Last Modified: Tue, 06 Dec 2022 10:00:51 GMT  
		Size: 9.3 MB (9348950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:7ee70c191bfef30d16b8da6c3507574c2190230ccc29d3ad303a42ed5b5453a7
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.0 MB (66964541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65994d601951c1ee9054dd1c2ccdfb437de70c022efb34402251749956e9b4d6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:24 GMT
ADD file:2deba7c04e28d01997b865f366cdc8d38a80aa39720c4e4d1fc581ac17e8ce4a in / 
# Tue, 06 Dec 2022 01:40:25 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:06:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:06:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:47d0ec2abdb05569eada58143acd16d47ee4b07a33535544cf5bf267bde20cc3`  
		Last Modified: Tue, 06 Dec 2022 01:44:13 GMT  
		Size: 49.2 MB (49233737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:626af93612b745b80b7a70ce5fb9fc87baa4761919cb1bef555440f52c2942dd`  
		Last Modified: Tue, 06 Dec 2022 02:12:50 GMT  
		Size: 7.7 MB (7727211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:823037cfb749c6f284b1368decc632435d3a62f1190e4657fb94151c7c4473a1`  
		Last Modified: Tue, 06 Dec 2022 02:12:50 GMT  
		Size: 10.0 MB (10003593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:c7ec312f3215c24584f6f9b1e2526f95ad9eaa23f69b4aacab201b6d258a22ff
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69361765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0b1b976ccfc110e0d31dbc94834729c12196c3de98a1f0d6d5fc7ab80e1e91d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:05 GMT
ADD file:0688532a537bb23756917f3d062da18668cd55041d0ae6610cff386043ffbdd3 in / 
# Tue, 06 Dec 2022 01:40:05 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:08:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:08:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:54f3d93b8ab6f3a5195d99724d5bc911156006687d577448bd8e94d2fe049d4a`  
		Last Modified: Tue, 06 Dec 2022 01:46:02 GMT  
		Size: 51.2 MB (51207714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcafc40b392135cf50bd0cd3a3b92594a07197063a5cc3dd6c012fa7a6eebaa6`  
		Last Modified: Tue, 06 Dec 2022 02:16:33 GMT  
		Size: 8.0 MB (8026054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ee0381e45d30e80cab06cad63add4981be888be074fc187e1b72e75eb0da25f`  
		Last Modified: Tue, 06 Dec 2022 02:16:34 GMT  
		Size: 10.1 MB (10127997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
