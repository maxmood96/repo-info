## `buildpack-deps:buster-curl`

```console
$ docker pull buildpack-deps@sha256:232ba9aff0f1ce473460e440e50d424b2d4f88603c94dd75d6acd91910fec127
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:buster-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:9e0b131e67840edbb241e8b7581b592cb477566f64131655fa4a21634f42ef41
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68308198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72404df5a5eb4d95eeb5a9ad3409584c6c5f7953dd5dbe044f6cedb0499022c0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:44:02 GMT
ADD file:259be79d94a2549a667ad08a093fe18f15a6c93d66a0723292f49294e31fc7a1 in / 
# Tue, 25 Oct 2022 01:44:02 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 09:25:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 09:25:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:fd31ec14dccdcda8f2472547f1a94ef0a23b8dabb764cd7b1d48aeee0afea7c8`  
		Last Modified: Tue, 25 Oct 2022 01:48:15 GMT  
		Size: 50.4 MB (50447742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b6422bfa32650e77d346bbb40c6b2a0dc34c863e10cfb1a117e8da9796694cd`  
		Last Modified: Tue, 25 Oct 2022 09:48:47 GMT  
		Size: 7.9 MB (7858969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:335cbfc794fe106b207828e6c9d76fb72aa4631aad91b744e23442082275b8af`  
		Last Modified: Tue, 25 Oct 2022 09:48:47 GMT  
		Size: 10.0 MB (10001487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-curl` - linux; arm variant v7

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

### `buildpack-deps:buster-curl` - linux; arm64 variant v8

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

### `buildpack-deps:buster-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:141fff8c2ffcc8259e3a47678ed76429a31d347a408e2f2f0888e736c49898dd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69361770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff4a03bb5b5ce0fe0aa8976c8784fc059747d3be27552c0f8e0fe675b0862c4d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 02:22:47 GMT
ADD file:7e14d4afa5499129c959c5ae5dc270e2fa04659c2c9b0527094cda3494c02d0f in / 
# Tue, 25 Oct 2022 02:22:47 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 05:16:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 05:16:41 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:76a731c42f665e7334a622f65117ef9389e97a878b7c74bb4a10dfe9cdb296c6`  
		Last Modified: Tue, 25 Oct 2022 02:28:50 GMT  
		Size: 51.2 MB (51207943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee1fc3722feabf994120ab8f7d4abab754206d1ca425b7274ce1db428f7a651`  
		Last Modified: Tue, 25 Oct 2022 05:28:54 GMT  
		Size: 8.0 MB (8025806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2019db6202a77d9f3c2e49a64c766b8b67d4290e0e66e1480fd8c576078914b2`  
		Last Modified: Tue, 25 Oct 2022 05:28:54 GMT  
		Size: 10.1 MB (10128021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
