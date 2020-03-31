## `buildpack-deps:buster-scm`

```console
$ docker pull buildpack-deps@sha256:6d189e2979dc13a3ab696afa63d8152c6fb958d781cbc45f7fdc09b339b0bfe0
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

### `buildpack-deps:buster-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:0c429209cac674fc37ed1388943b1fe96c51d5ef3412453ee1c304fd8dee0a62
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.0 MB (119980931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a691d2461acb89f92d42d0a1e9441dc01edcf9a9de10d33853b35af263bb9ab0`
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
# Wed, 26 Feb 2020 01:06:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:55769680e8277a4ff083d05f0993d1483b3d26b93a8814cf3c6f04fe5975ffa0`  
		Last Modified: Wed, 26 Feb 2020 01:20:44 GMT  
		Size: 51.8 MB (51790538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:29786198424c8ec78237bc16d26787b166a13efe42be23a598da7d598f448ada
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114673902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:175dc827dcffa05ab5e4f1ce66bebda3cbe2209286583619abffc388074a2c83`
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
# Wed, 26 Feb 2020 03:37:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:50b633f1fed3a08247a3f321c140c5df5252f77726e6c0943dacad6a73a7cc24`  
		Last Modified: Wed, 26 Feb 2020 04:01:22 GMT  
		Size: 49.5 MB (49532105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:6fe6a742de9e8aa6df4ece3aa98ee11f046656d2b989c2fc5024b5113ab2a945
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.6 MB (109617433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6a0513f1b2dcb767bbf1324830f63507a253a35b75d8d37efc1aa1d37b12d7b`
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
# Wed, 26 Feb 2020 02:12:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:4f2ad791c8431e9b6624239d0b1fee2523df27584a263ec1d8d525201bb44087`  
		Last Modified: Wed, 26 Feb 2020 02:34:01 GMT  
		Size: 47.3 MB (47315030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:a38c83ca23b2e8c383cd80bc2d1197d315d90809ee1f4d056adbd18f8b1b58f6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118938148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a7db2d126cc287ff1412d1444d1b4248f338f6605c8630c4f7e4fb321508c03`
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
# Wed, 26 Feb 2020 03:51:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:4c349f2c39d405d81a454ff62bdd8753ad71aeb8e8c1e300f3d7d19cd78eaced`  
		Last Modified: Wed, 26 Feb 2020 04:05:53 GMT  
		Size: 52.1 MB (52102940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:d146ab4a50de07636b045d3dbfbcb3f1bb867c35471c388db5e4567023978e73
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122846285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fff3b65e9a34db05552e6402b82f01ae5f04ff8bca64390ef8f7608d0b48467`
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
# Tue, 31 Mar 2020 01:11:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:386e97cf1d6fd009009b5f713b87e4f65e1504caca058d8794c6f6f23639d099`  
		Last Modified: Tue, 31 Mar 2020 01:29:25 GMT  
		Size: 53.4 MB (53380055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4d4ea0cda9aab6c243b5231ea90c0119cdef36b8f2fc53c8ab3fc9178bd3a0e9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.5 MB (130510395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:341485559e2c77147ae2ae833cedda1b26a36d069719a7a79d7c20787a23f33f`
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
# Wed, 26 Feb 2020 08:05:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:6753b4bd70abfe94b10e69e3b643900c4f2e72961c4db6310963cd4c21303d5c`  
		Last Modified: Wed, 26 Feb 2020 08:49:40 GMT  
		Size: 57.4 MB (57392075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:7646e80fe1d0087daea56b0f52fea7c3a44e70ea2f07bc908b6ddddda2c63b63
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117549718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b5d0afaa53be173229fefbf2eb8b3d425808be560dade5114fed6d2b232228c`
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
# Wed, 26 Feb 2020 04:34:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:942858cf91c54d2d1efa88f24491ba2b93cd15ed968d4f5e193c5e26ca4236e1`  
		Last Modified: Wed, 26 Feb 2020 04:47:51 GMT  
		Size: 51.3 MB (51327256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
