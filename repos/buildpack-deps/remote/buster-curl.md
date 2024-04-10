## `buildpack-deps:buster-curl`

```console
$ docker pull buildpack-deps@sha256:a1fe08a5a6c24c57bb26c44410dfab4d81a11e9ceaa3882321c833e8fb9de331
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:buster-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:c0e6775692799dd3231566da39efcd7deca3e56643ecb6b8364af9d118dbf567
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68089839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79f257116d1e01d1a04ea40abe5506efaed3ca51e62b01cb6f2177218c8d0a66`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:21 GMT
ADD file:c76ecdf17d2140aebb59f0261fd464e159af74b6489e79a1a10ad55941a63582 in / 
# Wed, 10 Apr 2024 01:51:22 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 05:27:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:13dc5104e330a0605d2251ca4b7184ca5c05c0c068e626b00515daf54ba1a917`  
		Last Modified: Wed, 10 Apr 2024 01:56:34 GMT  
		Size: 50.5 MB (50504020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a2be0394bca1f01401189d28d39b1fb8bded550d9905f371ad19c22c885f00`  
		Last Modified: Wed, 10 Apr 2024 05:36:56 GMT  
		Size: 17.6 MB (17585819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:2ab02a05859571cb4009246f72dc198ed3f214b676b77dc33d071feac212f41d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62180004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5eab61cfdb0b578b9aa447a867f6eaa471b9d347bfa197ac5761d5f631485a75`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:58:59 GMT
ADD file:56eb0c1e9a01d2e3320b2f3d897736bfe09ccb53ef1ae8bfea2b9d4099bc1d6b in / 
# Wed, 10 Apr 2024 00:59:00 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:47:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:300908ef79221077165ff78ff105758d14dd67c42610c4e0aafdd731a920a871`  
		Last Modified: Wed, 10 Apr 2024 01:05:35 GMT  
		Size: 46.0 MB (45962444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a28291d070880fd3bc1d1083c0a3dfd62197b6f8f9b8f0222bebfb7abc3998c`  
		Last Modified: Wed, 10 Apr 2024 07:02:28 GMT  
		Size: 16.2 MB (16217560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:967dc05e2249f9e76af5d49bcb47942569f076ac46b2f8453b9fe5ec1cb889a8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66747349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed617d849b916a7323c765653f3ced6d3a3af6f4bd6469d6726ae6048f78685f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:45 GMT
ADD file:9b995c280b9e45d7ee0b5a7151b97767f47960ed492e35fd55c5eec6917bde2c in / 
# Wed, 10 Apr 2024 00:40:45 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:24:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5173f9984b20306181404de41336884e6153c70a737a933879b7878563fc5bad`  
		Last Modified: Wed, 10 Apr 2024 00:45:06 GMT  
		Size: 49.3 MB (49290826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5a2fef8d22586d8b400820a7eb103890ffb31484294a394d9d1f6c707a2bb9c`  
		Last Modified: Wed, 10 Apr 2024 04:33:49 GMT  
		Size: 17.5 MB (17456523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:8275c22139b832f406cfbd9b9bc4ce66f57013e8dac1d64f3135d1335bf5415d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69355039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82149eada0485f28a9641351fd752fc666fb669e44e750855f16c629979cb5df`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:58:33 GMT
ADD file:c816729e048abb40ca265a52e15f687e96a04fac489fca5504d6f1a6c1036f44 in / 
# Tue, 12 Mar 2024 00:58:33 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 07:44:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:738abb02da0a502d42242343d73d542ff3cbebcc7bfda5ae91845cb7a4177497`  
		Last Modified: Tue, 12 Mar 2024 01:03:51 GMT  
		Size: 51.3 MB (51255592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ac5971128c8aa1a16550a107f729e02bba65015ab53141a24c171ec7a05b79a`  
		Last Modified: Tue, 12 Mar 2024 07:56:03 GMT  
		Size: 18.1 MB (18099447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
