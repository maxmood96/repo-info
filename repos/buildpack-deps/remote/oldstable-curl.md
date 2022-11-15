## `buildpack-deps:oldstable-curl`

```console
$ docker pull buildpack-deps@sha256:72301252b6ca86ddaecd551683670176d9258e37f376cab6d64d3e1723870495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:oldstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:2d19b5d5a36b2aca9616da3cf6011a85b40fdd3a06886513dc0fcbc6af099f52
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68309191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1538a2ce68665a5acbcabcc51869e06543f8661679ed5f7b65c81faff517dec8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 04:05:03 GMT
ADD file:96ca7e18b6141668321140f8ae1a496641f631313035513f1f9314e9dad2cd71 in / 
# Tue, 15 Nov 2022 04:05:04 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 10:25:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 10:25:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:2730d739afad9b8ff3e3029e23fd69d9533603751d6e42053ce0068c2b58e258`  
		Last Modified: Tue, 15 Nov 2022 04:09:05 GMT  
		Size: 50.4 MB (50448823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a122751b35336c158fc53a3bb03c6b11b414387589e5455e99baecdd803c6318`  
		Last Modified: Tue, 15 Nov 2022 10:32:48 GMT  
		Size: 7.9 MB (7858972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a277c3efe7c0d28e443180df5a70570f6baed1f16a4ceeb88e9dd299df62dc6`  
		Last Modified: Tue, 15 Nov 2022 10:32:48 GMT  
		Size: 10.0 MB (10001396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:1df74213cb0f7792624ad370cb22aaf4d5fa50c9c939a0cfaa56a37b9fd76d80
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62412806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:403e3475f4d0a33ea5cfd89ad7695a6693f73c61ca375f6e614574d60a771015`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 03:14:44 GMT
ADD file:68e8c9a779cffc9968c1d577e6367eb14306b9cb1ef195c63c2def986afcec06 in / 
# Tue, 25 Oct 2022 03:14:45 GMT
CMD ["bash"]
# Wed, 26 Oct 2022 04:37:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 04:37:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:a96a0f5b8ad36dd704fa61a4d79f60b2467017919db6ccc83b23de2d450aa97c`  
		Last Modified: Tue, 25 Oct 2022 03:21:42 GMT  
		Size: 45.9 MB (45916231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:effd5ac5b158fe16c9f433d43a240f34a43c487c5068e15f63e4b8d39950d235`  
		Last Modified: Wed, 26 Oct 2022 05:12:02 GMT  
		Size: 7.1 MB (7147662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42c96180c4ced7c4701fea5d141a40207e07023179440f5fae4f42b21f491bda`  
		Last Modified: Wed, 26 Oct 2022 05:12:03 GMT  
		Size: 9.3 MB (9348913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f0fef9597218cf68c545420ebd356c389eeca3c914870b632a0b6edda7eb6a4e
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.0 MB (66963799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f231b4003c248fef2cab6822e3fbf4a5074709cbfadb7abb1f7fc6fef06b82c0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:26 GMT
ADD file:2122642b8ad9a333f73cba41ff9cc829542740e0e3c88379a7c9511fbfc28991 in / 
# Tue, 15 Nov 2022 01:41:27 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 05:37:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 05:37:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:34983cc1fd1c67f0d8b7b8b4320539206a1c098388b3a671abe88b45f157978d`  
		Last Modified: Tue, 15 Nov 2022 01:44:52 GMT  
		Size: 49.2 MB (49233786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35873fa6ec375a28180771e63a96f2039703f6658efa32da2e83a64f6919bf1e`  
		Last Modified: Tue, 15 Nov 2022 05:43:54 GMT  
		Size: 7.7 MB (7726432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07615c620859a5288e844fd58e708c735c884a4b600e9ea4bd3f26ca5744f723`  
		Last Modified: Tue, 15 Nov 2022 05:43:55 GMT  
		Size: 10.0 MB (10003581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:f0f233359e429a11c8a52f0969b058387587607d8bccf357f6ed8d543153d8aa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69361409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87477bc89f97cd52addafd30952e9faa7b556526e4257f4d934dcc6ef251a511`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:38 GMT
ADD file:e8c5010609ee5ceb22093e461dbe3f9748a4d6ca2fd436e635276b0f99e777e8 in / 
# Tue, 15 Nov 2022 01:41:39 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 07:05:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 07:05:24 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:a9674eda0741cb717f181697e2f2695ea87fdaf557d253407a096f80ad4f9fb3`  
		Last Modified: Tue, 15 Nov 2022 01:47:27 GMT  
		Size: 51.2 MB (51207653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dca530492bb92e888ea6ace416a72ac4994f0f9d5924fed0d0428af0a89574c`  
		Last Modified: Tue, 15 Nov 2022 07:12:52 GMT  
		Size: 8.0 MB (8025826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9316598250dc58d9f716af1423dd3c55cd9f630968b4820d4a9b320b61b3412`  
		Last Modified: Tue, 15 Nov 2022 07:12:53 GMT  
		Size: 10.1 MB (10127930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
