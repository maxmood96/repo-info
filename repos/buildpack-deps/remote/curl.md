## `buildpack-deps:curl`

```console
$ docker pull buildpack-deps@sha256:410750d22d86bd025eb89fe66c68fde9db067ebc4f34f23437f95b45f6091a4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:197b15ed15a83fc72a51ac30c2916354eabb7f7f8887578dd1aaf08ebf6cd0ca
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.2 MB (68190393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fd844eee586769fbfc3ae0ffa62ddcf4bcb8dd460b08b3adbbe327a7b8cc258`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:37:07 GMT
ADD file:e05e45c33042db4ec7f71a5952d65ee8cb3786dcd76fa7a990f48a2def1344e2 in / 
# Wed, 26 Feb 2020 00:37:07 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:06:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 01:06:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:50e431f790939a2f924af65084cc9d39c3d3fb9ad2d57d183b7eadf86ea46992`  
		Last Modified: Wed, 26 Feb 2020 00:44:04 GMT  
		Size: 50.4 MB (50381971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8c6d374ea51e3dd671f71b28d025a7794ebea181b00838987d0b4d8a51372f`  
		Last Modified: Wed, 26 Feb 2020 01:20:25 GMT  
		Size: 7.8 MB (7812140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85513200d847a64a6e8f2cb714e2169f559b24b7736c586ff7b9aaedf71f410`  
		Last Modified: Wed, 26 Feb 2020 01:20:25 GMT  
		Size: 10.0 MB (9996282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:982fa740c320b556ad4ddf7f863e914fd9e84dd3c9a4e3c72ce2679675f3f846
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.1 MB (65141797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d94eb7c7462c8a2733a7508aad2741b2657210f55171ac2e96a501362c58a456`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:47:18 GMT
ADD file:c5d04d0713a74a05133d8fc49f69a750c709995827984d401d465d98bd5617d4 in / 
# Wed, 26 Feb 2020 00:47:22 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 03:36:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 03:36:49 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:d16b9694b13fa6f8cd07399e1efcfc873f65232f05b1c9a7efabbcee33aa682a`  
		Last Modified: Wed, 26 Feb 2020 00:58:52 GMT  
		Size: 48.1 MB (48095674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40d619f5a52d61c3703980a2b8ac1e91d74e42191916956f6a7402bd4e6b042b`  
		Last Modified: Wed, 26 Feb 2020 04:00:55 GMT  
		Size: 7.4 MB (7358998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfdddb8ce863c2392a2f21c39d31e7db5065eb0b82730dd4f5ed94ded4b2a61`  
		Last Modified: Wed, 26 Feb 2020 04:00:55 GMT  
		Size: 9.7 MB (9687125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:c342b21207b0428d0b5542d6640518cb1b13d88867f1bf6c1846eb133eb6e328
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62302403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c871cfc236d8a331c2defacb0c8be3965f9dd4452d2016f484dc3bd001fbc94`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:50:58 GMT
ADD file:38fdfcc3155e437ce162aa0ed9dcdc5893b8145e2f3ede2858ed2187d79bf718 in / 
# Wed, 26 Feb 2020 00:51:08 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 02:11:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 02:11:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:3182cf45068cd9734abd8e38dedbb9930ede35ee8c11376ca2684e86f9a1aa85`  
		Last Modified: Wed, 26 Feb 2020 01:07:03 GMT  
		Size: 45.9 MB (45862691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b727ab99a6a790544e023dbba8625605266dd84b3a69acaa541144ad632f4ba`  
		Last Modified: Wed, 26 Feb 2020 02:33:37 GMT  
		Size: 7.1 MB (7096560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab9435f7cf0c46bc6621020fd229e7de8baa61f71059cb9a34b9f681caed9aa`  
		Last Modified: Wed, 26 Feb 2020 02:33:38 GMT  
		Size: 9.3 MB (9343152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:e419963172eb4f6acbc817fba405b0cea5c2dae77b4c708d61271ac3d0e645b7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66835208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0f9749d4b327882e58c9c923ae1affb7b7bb59231cccef4d9ee526a38c32268`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:46:17 GMT
ADD file:e3320653f0d517a6181aa46fb47407790018e2d8dee590005ffdbee3d04f72d4 in / 
# Wed, 26 Feb 2020 00:46:19 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 03:50:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 03:50:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:77b067f4ec14d48dbc8cd83b7a46fbb5f21fe01ea8911db256cc0168a30c1f5b`  
		Last Modified: Wed, 26 Feb 2020 00:55:50 GMT  
		Size: 49.2 MB (49169974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:194f1ca8932d9ee1727375561698745fa548546f609956c4aca9fed0b48d41a1`  
		Last Modified: Wed, 26 Feb 2020 04:05:25 GMT  
		Size: 7.7 MB (7681467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88425686f799f708ae776f78a6d01c179a52f55fc5b32de874db3c4ace2dd156`  
		Last Modified: Wed, 26 Feb 2020 04:05:25 GMT  
		Size: 10.0 MB (9983767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:9a382bdd8833844c6dd50b4d641c5dd7a64b0c78bece8823eeb2eeccc0084cd0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69466230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1313b24082c9e214bc097371384886b03ac654c67bfb40544339396a9c0cc1e4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 00:39:25 GMT
ADD file:3dbe042e711d452b61bbca02798da5695de980649d3fd51ae6983b2445eaa792 in / 
# Tue, 31 Mar 2020 00:39:25 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:10:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:10:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:acd641cee0ec134334632eecb48cf0c487a224a27ad5661fcd7eed50b0a1ab34`  
		Last Modified: Tue, 31 Mar 2020 00:45:15 GMT  
		Size: 51.1 MB (51146119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2912921d73f5acd94695512133a967d88800cdad68ebd0d274df8c09b5094faa`  
		Last Modified: Tue, 31 Mar 2020 01:29:04 GMT  
		Size: 8.0 MB (7981618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:735acdf625f8ccb783f82429001ad885a8456b5844304818e223e547bc91b55c`  
		Last Modified: Tue, 31 Mar 2020 01:29:05 GMT  
		Size: 10.3 MB (10338493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:9af0d3c6a321da609ab7d097d5e0bda277692644759e764a150a541f62593ec5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73118320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db291a1ce2392b8a60509e4fd0cb8351f5b094b123485055ca851f7d7bbccece`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 01:30:27 GMT
ADD file:b58865b3fd36d440998ef82e567179a9cd6b9ce0343d5e5a15a0b4f856f211c7 in / 
# Wed, 26 Feb 2020 01:30:35 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 08:02:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 08:03:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:928614537d6dedbdf79cc24c5c56bf98c3ed88f9d91a9ec1105d2a133611b0fd`  
		Last Modified: Wed, 26 Feb 2020 01:49:54 GMT  
		Size: 54.1 MB (54138444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f499895181a6ad2e0a4c9fdaf499ffa2704adc3eb69595e994d38b563c6000e8`  
		Last Modified: Wed, 26 Feb 2020 08:48:45 GMT  
		Size: 8.3 MB (8252620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:887a1613f8e8808f8cdb481db1614b9d79f0dc57f17235b478bd4c6c95849e29`  
		Last Modified: Wed, 26 Feb 2020 08:48:45 GMT  
		Size: 10.7 MB (10727256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:3a0cc7b13b31cd8182b7baa03ec6129d1f42c59faff05a6e0f131e4b7d1ac9af
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66222462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c6cb6d8582e1c1c65d033ff6c99afc6f61cc8ce8719f756fa4f69204b667c7d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:42:32 GMT
ADD file:80536bfff518f6b425ad359b86a124f79ccdc82deb3e648f1746a7c87a1fcad0 in / 
# Wed, 26 Feb 2020 00:42:35 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 04:33:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 04:33:27 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:0a3603da42bb9e22573006a7f894b198954caeab529e2e041660e12c4fe62462`  
		Last Modified: Wed, 26 Feb 2020 00:47:26 GMT  
		Size: 49.0 MB (48958029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a7b142236e4c473f4fd19a0485f74364510f658dc999627e6c41f4684a50d5`  
		Last Modified: Wed, 26 Feb 2020 04:47:32 GMT  
		Size: 7.4 MB (7382213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f2c5965845a6f2fd1bfaa3a4814a17655d46330b5f60ed861daaa390d5b82a2`  
		Last Modified: Wed, 26 Feb 2020 04:47:37 GMT  
		Size: 9.9 MB (9882220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
