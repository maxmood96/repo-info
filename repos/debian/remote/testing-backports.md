## `debian:testing-backports`

```console
$ docker pull debian@sha256:b32e67d9bd11b918680f5a79ae32cfe89127078c16d3c7030339b6ecbe7e9e12
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

### `debian:testing-backports` - linux; amd64

```console
$ docker pull debian@sha256:e86c4b3c72a0e8768b551a6c28932e95ddef46f3e4f04bb112b7dc762d915eda
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49299469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1294805f7eb298e58fafe932b38e0a21f5937227e5f253c3dc3d64988473a5bb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 23:48:15 GMT
ADD file:27b4229d808812579f1eb7609d08a5bb2177380a480279009a4ea17e05193323 in / 
# Tue, 02 May 2023 23:48:16 GMT
CMD ["bash"]
# Tue, 02 May 2023 23:48:18 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:56c7136ddbfad3eea4cd5c38c0703e58fd25630219d5462a9099387c4b3a4160`  
		Last Modified: Tue, 02 May 2023 23:52:53 GMT  
		Size: 49.3 MB (49299248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6401c83577903f6232bbd710060d2f90fecad3738c81eb1d49b11bd794829f7`  
		Last Modified: Tue, 02 May 2023 23:53:01 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:4f040e1a48bf0661e574c6c14cd4dc348711d3e10f5c5200581b6840a0c91540
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47169197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f52411e941d9dcab84bcfff62108c2acfe48559e182bc2627d32441fda875bd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:49:21 GMT
ADD file:8bfc1bdd1aefc17e766ace2a5ef94212c34e4ec0baf682e09fa19f8f8ceebbe0 in / 
# Tue, 23 May 2023 00:49:21 GMT
CMD ["bash"]
# Tue, 23 May 2023 00:49:23 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:2afa9817c92f049426ef34c4e496612296fd43c570dd699e15025931720995c8`  
		Last Modified: Tue, 23 May 2023 00:52:37 GMT  
		Size: 47.2 MB (47168972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6411bd3580692c71648a48a1c7c4c91fcc2a2d3597043f44edd008495550dc15`  
		Last Modified: Tue, 23 May 2023 00:52:45 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:1597e9260aae2772a7133ad9edd4070ba7348dc26af51df29331b564902ce1de
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (44990134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dc40b471a9e3f86d40dbb84afa1fd052f4917f8b8e99fe2d9aa2c2a80c5bf60`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:59:33 GMT
ADD file:b45b7f53a73d545a30b9417e03361bb65d2c95b24d1bec13975609a91a7b5be9 in / 
# Tue, 23 May 2023 00:59:33 GMT
CMD ["bash"]
# Tue, 23 May 2023 00:59:36 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:7ddc338d3f8f98508a610351bc3241f078b421eb6193b9aa7dca3d304d8dc133`  
		Last Modified: Tue, 23 May 2023 01:04:11 GMT  
		Size: 45.0 MB (44989914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6edad5fdd49f027d2ce6b1921e32ce005512a3f1323a48e74171b04796dc82e9`  
		Last Modified: Tue, 23 May 2023 01:04:21 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:8709377f35a980b8e1e7f4df0563f54fb830dd45ea15ded8efa4e7a11ebdd71d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49348009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd10872f09e4d747a9a33c7c28d1fec1d9c5c0b82b6d977fdb9c63ef5bd1b0d9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:44:13 GMT
ADD file:f5e81f28718d3bd832678fa284dcfc626b1a1bd4811a8912a05b9fcefd40d358 in / 
# Tue, 23 May 2023 00:44:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 00:44:16 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:93ff152152cfe9dc0fb257b029c2b1838408f3bee982bb891d1f5b4212469796`  
		Last Modified: Tue, 23 May 2023 00:48:27 GMT  
		Size: 49.3 MB (49347786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed9f8f4a52af285bed9c9695b1ca3b42fe8cc47e2123b95177cc5660b3408dc`  
		Last Modified: Tue, 23 May 2023 00:48:36 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:a34d35a56e3ac700d8461491c7c8027719cbed881cf1d0117c42588f9e0fbb96
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50323412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48464041e8c0ae381568e26f1d306aae1b380ee3c093b24f31935283c011ba86`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:41:48 GMT
ADD file:1bdef5bd1420f24f40c30a4d083111b4d3e9a5ac634f66b36b0e9a671c2a1e8f in / 
# Tue, 23 May 2023 00:41:49 GMT
CMD ["bash"]
# Tue, 23 May 2023 00:41:53 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b0a3731306483602be1aa1da6fa48174e0149f3d89a9d569dfc958efbe3b2242`  
		Last Modified: Tue, 23 May 2023 00:47:21 GMT  
		Size: 50.3 MB (50323189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6015481688f12e64b3d80d1ff46a284304c371d064f3b8d211558017bf0ec53c`  
		Last Modified: Tue, 23 May 2023 00:47:29 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; mips64le

```console
$ docker pull debian@sha256:54100d71c786d8db8d8562af7023a5d293aadb4d410d3a25ebd7f2ca8a41ae3b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49304464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd2ec23af9bedb49503f1dd78d6f8af5dc7a0785c3677d4f39471e93eea43367`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 01:13:46 GMT
ADD file:7dc98d86d0fc624f9d3bdb025637a3999c222454b159557cd5c010871a74836d in / 
# Tue, 23 May 2023 01:13:51 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:14:05 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8119bb11dde1051309b0b2b2d7fcdf8ca913220682229258d5650bb2ec33b863`  
		Last Modified: Tue, 23 May 2023 01:22:23 GMT  
		Size: 49.3 MB (49304240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:261c33ef7caed46449ba2a1064f434b2a842459be15a6f8b935f4393bd365bb2`  
		Last Modified: Tue, 23 May 2023 01:22:32 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:156ab50461e41220bc6347c1a2a8495ec43b166beeaa8e16e41f5c19b033b3c8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53312551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7c42db36d5476673f68b00e96c3bd427941ae96f5e553c218eae9dc47fec2aa`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 01:19:03 GMT
ADD file:f0b69885ec260d5afe906ac0ce6237b90b7b5f97af772312b51309e76de2e0ea in / 
# Tue, 23 May 2023 01:19:05 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:19:09 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8e93931daf477030b8cc7fe17ae2e8a0f7cb156f1b6c1c0b010849a9e112ab45`  
		Last Modified: Tue, 23 May 2023 01:23:56 GMT  
		Size: 53.3 MB (53312325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97f513d841c85d12a70ef1cf65468153a3ad18d5c9da8df05282d658a370e75`  
		Last Modified: Tue, 23 May 2023 01:24:06 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:778bda3594123edabff13e3e31a198185c1733491e2d01eeb7cf0bff4a37d005
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47673699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd56d7f88324543692eb5a3696d99abce18b523e21bd366d992a576f04d50aeb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:43:47 GMT
ADD file:6dfd7d21cdfe9dee2a7cad47d8e2e22e6e56bd924f036cb45c183fe31efe66cc in / 
# Tue, 23 May 2023 00:43:49 GMT
CMD ["bash"]
# Tue, 23 May 2023 00:43:54 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:af4d11b0c6366f32a980344976c0622adf11030b727c114fcc65377cb3f44688`  
		Last Modified: Tue, 23 May 2023 00:46:43 GMT  
		Size: 47.7 MB (47673474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:913ea609cdd6a96e8cf48c4709c1519473bb0da85b3446ab5f8de88a50de77ec`  
		Last Modified: Tue, 23 May 2023 00:46:48 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
