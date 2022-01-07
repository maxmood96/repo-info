## `buildpack-deps:impish-curl`

```console
$ docker pull buildpack-deps@sha256:2510d2efa56ad226a4d8cff1c9f69e86638c86037087f6561e5efb2d25cc70ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:impish-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:c7e49bc71e8d908965c879a3c44f27ac0717ff3a01aa4baf8bb728de0c32ea01
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37623972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:986822cad2111e1830fe7cb4c8c2919b3f2bee97fa592925713eeb40b21aeef4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:25:45 GMT
ADD file:f8a2d8d5948f5e12d6d04bf3b60fdbe16956e3a0d5486994c3088f3c9ddfe3b6 in / 
# Fri, 07 Jan 2022 02:25:45 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 03:16:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 03:16:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:688b037d2a94faed4d0a662851a3612e2a23a9e0e2636b9fc84be4f45a05f698`  
		Last Modified: Fri, 07 Jan 2022 02:27:28 GMT  
		Size: 30.4 MB (30377796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d5c296f670bfa970376b56606d3e5a2ceea40444d962aaab9bc917f5d0e7310`  
		Last Modified: Fri, 07 Jan 2022 03:24:55 GMT  
		Size: 3.7 MB (3694036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9090afc2d87cf8132a83d65478a454ac3c18914fdadd6eb28cc6e1024e8d77ad`  
		Last Modified: Fri, 07 Jan 2022 03:24:55 GMT  
		Size: 3.6 MB (3552140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:impish-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:4db51600c738c3133d96f0d9aed2e4ab2ce1800dc9f3813bf7166c949fd446b3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.1 MB (34105205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:457e0fea4bf7473a1fca9cf645104252d215b61836ef737e122be14033fd1755`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:27:09 GMT
ADD file:1943eb8161d1853aa98adec6971ce80e67c5ef8deafcefaa8809addbc3eee806 in / 
# Fri, 07 Jan 2022 02:27:10 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 03:02:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 03:03:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:2d5d37c142fbf68de0a42ff73e6ce8a0826e64699a992a9f245b81d99456b441`  
		Last Modified: Fri, 07 Jan 2022 02:31:42 GMT  
		Size: 26.9 MB (26918664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e42acc47d9b5e0e8682eb3111a2b29f00320248bba4041db18e90d6692916b5`  
		Last Modified: Fri, 07 Jan 2022 03:20:05 GMT  
		Size: 3.4 MB (3443485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:898f1d9d4b8b0313b8e81ee1c2495f22045cc018c1ff727f3fa71708b95528c0`  
		Last Modified: Fri, 07 Jan 2022 03:20:04 GMT  
		Size: 3.7 MB (3743056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:impish-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:e7439ca5ff39b7e6c7f4ab4fdf5961745203ab2f803f37713896a29a5b70bd8c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (36032463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45f9472620088d5641cd0396bea02b1787405475e7f13c7d55a3ea795340354b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 01:54:01 GMT
ADD file:313dff926c3a3dbea803ddccb86e973465260b7b2618bcbe33892115f68a773b in / 
# Fri, 07 Jan 2022 01:54:01 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 02:23:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 02:24:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:f0ffaea8604435228e4901f528ec20078ee34a6050875405766fd95208f0c31f`  
		Last Modified: Fri, 07 Jan 2022 01:56:10 GMT  
		Size: 29.0 MB (29026221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:035a5bcbd0ba88bd2c87185410a2859d04ba076d13564276d0090e20b7c3f439`  
		Last Modified: Fri, 07 Jan 2022 02:31:16 GMT  
		Size: 3.7 MB (3678819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6daffb48b0996f9247e0edaf560439b74457f0e8f98d4e6dc8c8cf33126d4064`  
		Last Modified: Fri, 07 Jan 2022 02:31:16 GMT  
		Size: 3.3 MB (3327423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:impish-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:5f3775b70607772f8837a069d02fa8a23ba0b242085e3170520da3a4a8d39b5b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.6 MB (44563723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28702f59747d2364a379deddac78fbb72a0aec14964bb2e5fb8629d6ef3f6342`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:20:45 GMT
ADD file:6c52e72233bc011d6cc1943cc59283ed3def1a426a7cf3b9b8a03320a1de85ac in / 
# Fri, 07 Jan 2022 02:20:48 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 03:00:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 03:01:24 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:5e28f686135f4d211abc5a5fe924bd23a6fee36d43e23d37529639850f708a22`  
		Last Modified: Fri, 07 Jan 2022 02:23:31 GMT  
		Size: 36.2 MB (36174729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:519e57ce751c93eab79167fffd034ab11fb1f3e684ad227a98e103d2d69a582d`  
		Last Modified: Fri, 07 Jan 2022 03:13:14 GMT  
		Size: 4.1 MB (4146848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8312c3e1c30adf889d9a77ae7b4ca31a2fe111d0d26d63eb4122fc4894cb7b21`  
		Last Modified: Fri, 07 Jan 2022 03:13:14 GMT  
		Size: 4.2 MB (4242146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:impish-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:5e94e03c1f46879565a0642fcc122635333b31ac277b126bd4ec27aead52784b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34501961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:446b07220590926773ecb885b550602af63127e9e80dde9f0b389f5b16e3bd55`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:19:54 GMT
ADD file:80d7cfc8a88ccc3ac0dd24dfba95a65c7e24cc96f880a61736d5ab358db84912 in / 
# Fri, 07 Jan 2022 02:19:56 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 03:22:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 03:22:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:41481709d1b8a29bbdd69a8df35aeab07866245eed21a54aa5f2d183351e4569`  
		Last Modified: Fri, 07 Jan 2022 02:39:10 GMT  
		Size: 27.2 MB (27207318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60d76cd11e8f1597cec35f9f56d5d5a51d72bd9e573affc336b7759ef3e318c6`  
		Last Modified: Fri, 07 Jan 2022 03:58:49 GMT  
		Size: 3.5 MB (3490604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de07f6850c026835bb34bed7b3387eb20ee6bfcfd87f56c0909e9cbeaa7d38be`  
		Last Modified: Fri, 07 Jan 2022 03:58:48 GMT  
		Size: 3.8 MB (3804039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:impish-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:e7d297470161f1cb35ecaa59e269df522c549969384be9106590f1e4a89c42b1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 MB (38257255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81d8008da67d1259e1a1947e8bd12c4161248619c87c61e24a715a295a147440`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 01:42:43 GMT
ADD file:d2d689ec5bbbbec520f5fc8ea75e1d642f177a30c5937027ca800b3a9ccf5b83 in / 
# Fri, 07 Jan 2022 01:42:45 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 02:07:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 02:07:17 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:77bd6b10105ec281aabfad8249bf82b48478e0eac3503dccd5d75db49b1dd586`  
		Last Modified: Fri, 07 Jan 2022 01:44:35 GMT  
		Size: 30.5 MB (30526144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ac2bdfd743d34b81a7e7855ce015d3dcab3c711230a384e4e0f31da363e5ec`  
		Last Modified: Fri, 07 Jan 2022 02:14:03 GMT  
		Size: 3.8 MB (3767780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f22dc9fa326e82f6b809f067452b917fde08df5f8c3ee42998a9c882963eeb1`  
		Last Modified: Fri, 07 Jan 2022 02:14:03 GMT  
		Size: 4.0 MB (3963331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
