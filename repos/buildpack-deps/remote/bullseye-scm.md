## `buildpack-deps:bullseye-scm`

```console
$ docker pull buildpack-deps@sha256:6c6366a7b27f25994fa57634efceee78b9c3170bda0d03496761f1ea5b9cad54
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

### `buildpack-deps:bullseye-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:4f6022505aa84d15d888f51c649688151504c187c1f841544469dacf45f90a56
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.5 MB (125452120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b856a8ecc0bb59b2b02b293ea113334f1dd6d10d3f312a57f1d4463bcc9ff2f8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:48:53 GMT
ADD file:32519b03930d9f5db9010ae49e0987322ce19eab681ad5c841fe1cd6268ad2ee in / 
# Tue, 30 Mar 2021 21:48:53 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 23:00:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 23:00:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 30 Mar 2021 23:01:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6abc78d8e2422868f293b265b6c0ec3ba250fc4987f862ba05e86d7eb277f297`  
		Last Modified: Tue, 30 Mar 2021 21:52:53 GMT  
		Size: 54.9 MB (54868089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1424cff1d2b47e24acbeb3381319a9bbefd1f8dcae5c521f0198833d9b2911ec`  
		Last Modified: Tue, 30 Mar 2021 23:12:47 GMT  
		Size: 5.2 MB (5151423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:859f37c645b9a1a4967007d3e310ace7f83d9924b7fd77385ff9e2de20a55a5a`  
		Last Modified: Tue, 30 Mar 2021 23:12:48 GMT  
		Size: 10.9 MB (10867143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f1dad4b787cfa0293818e7bb90048de585a8c37b12fab90dc184d527078652`  
		Last Modified: Tue, 30 Mar 2021 23:13:10 GMT  
		Size: 54.6 MB (54565465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:65b1d5abdaf4011f4ddcb2eb367b171ef882182a0eeb3615bb0f52ba7a2ceee4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 MB (120346725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73ae2677f3f793e5481f04f5c65c7cc06ac45dff5cbe7662bfda414315e3bb5a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:49:55 GMT
ADD file:3a982d4cdc7d9461623d85a4b6162531ca9adf2921f0d43a0b548d3710392387 in / 
# Tue, 30 Mar 2021 21:49:57 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 23:43:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 23:43:26 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 30 Mar 2021 23:44:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:645891123da6b320ad4fd8cfadf96c77b7144dd25b617222de1fe718cde77e35`  
		Last Modified: Tue, 30 Mar 2021 21:57:27 GMT  
		Size: 52.4 MB (52401170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e2ae11e65cec397d581f8bfc50a0c3eb2d363cc2397beaa585ac385f720fcf`  
		Last Modified: Tue, 30 Mar 2021 23:59:40 GMT  
		Size: 5.1 MB (5061094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:131fae12c09181b2c23186780b133bfe60e76c8af6bc6af4943aed293c993b47`  
		Last Modified: Tue, 30 Mar 2021 23:59:40 GMT  
		Size: 10.6 MB (10569881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16e41b734e985a8d169b38913e5fe94cb0348ee05101bc3ad6b952ef8393bddd`  
		Last Modified: Wed, 31 Mar 2021 00:00:09 GMT  
		Size: 52.3 MB (52314580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:74d188f209ac11b64d23be572f271e5eebc0fefba8f78bfe250a98ff125772d7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115536058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28003b9786eb624168c82e284d50ab0e2230763f2a8b40110cb5f8f5be7c912f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 23:07:05 GMT
ADD file:81d46e360628ea35bb1ec870f07ccb5c7722c2af2296557ac007f32663ef1cec in / 
# Tue, 30 Mar 2021 23:07:09 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 01:18:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 01:18:53 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 31 Mar 2021 01:19:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c62a7336a784ff2e5eceb7d0da019a0022517c331efaef6fb92eca67135c6ac0`  
		Last Modified: Tue, 30 Mar 2021 23:15:13 GMT  
		Size: 50.1 MB (50069202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a5e37c5cf7fe4b128b7450320e29ce9023508d8710e2e020d7e16f2f5c8db48`  
		Last Modified: Wed, 31 Mar 2021 01:35:02 GMT  
		Size: 4.9 MB (4920655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a0d6ba1227e34af56c86a1a156db9127d0e70b920d2ad598b3f031d3b7190e`  
		Last Modified: Wed, 31 Mar 2021 01:35:02 GMT  
		Size: 10.2 MB (10218163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09cb7f9d788071f04087bc2a4b3685b07300fe256545a6865e9194b62df992e5`  
		Last Modified: Wed, 31 Mar 2021 01:35:32 GMT  
		Size: 50.3 MB (50328038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:7c25cbd3dd385ad51b77416c2df2fee42b34499570b62d334310c54215a3405b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124230140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71b9ccec91e6d01e3dadf63f54fd9b6c59a285e261881e6bec837de3e0cb73f2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:46:09 GMT
ADD file:d2b87aea7c45e4b0e478e3c2eabae00f1c80b5d77f8f579d2ff913c78b44b6b0 in / 
# Tue, 30 Mar 2021 21:46:12 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 00:11:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 00:11:58 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 31 Mar 2021 00:12:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1063bcb9135253bd841aad1946f348a3277d992a7ecba4ef1ef68217c3c1b019`  
		Last Modified: Tue, 30 Mar 2021 21:53:23 GMT  
		Size: 53.6 MB (53555197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890e5446d487fcab6d7189e7771c6a50252b2d857c9b70fd4cea1bcfe3a1c8a5`  
		Last Modified: Wed, 31 Mar 2021 00:28:24 GMT  
		Size: 5.1 MB (5140737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b996f43aeb591ca2dd4bc003c5c5e3e982c6b85b7cad5a14591b08209f01b95`  
		Last Modified: Wed, 31 Mar 2021 00:28:26 GMT  
		Size: 10.9 MB (10867476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d44941e2620f2cbcd9d88a5b4b0eb491639112c330530030fb953c4cb4a4a63`  
		Last Modified: Wed, 31 Mar 2021 00:28:49 GMT  
		Size: 54.7 MB (54666730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:de1b12e4f94094d1b5ab610a970f4910418e8402afd6d01d559618f041740452
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.3 MB (128319268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8334ad66e51e67e50cecaf219349110168e48677369b134ccb43a7412bf2d15d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:38:58 GMT
ADD file:b5024008ca4ac295c015d04d146515efd534f38efa8793979ad8a6c1cc41a2b8 in / 
# Tue, 30 Mar 2021 21:38:59 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 23:54:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 23:54:29 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 30 Mar 2021 23:54:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:46dc83097f0241a9cf1128d563661cf2cacf0ca9445152008a4c686a8d125595`  
		Last Modified: Tue, 30 Mar 2021 21:45:11 GMT  
		Size: 55.9 MB (55881315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96203cf1270a0522cb74805c17be141b6be163c96591b032d0aeceff808d7b6f`  
		Last Modified: Wed, 31 Mar 2021 00:06:09 GMT  
		Size: 5.3 MB (5280209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63af79a424e53c82e0807d0e90f60c2456bc0ce3accdcee7cb3f1f9f5f70a96c`  
		Last Modified: Wed, 31 Mar 2021 00:06:10 GMT  
		Size: 11.2 MB (11248664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aaa2fa19667aacbe54d69da17398fd2ae22b23b7bf991725d64c3139c6eb5cd`  
		Last Modified: Wed, 31 Mar 2021 00:06:41 GMT  
		Size: 55.9 MB (55909080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:a1cceb1c77c37347680f98c8b484710d6190d7fde9d817f3ba24964aabf523c6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.4 MB (122409976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:822f9211fa890535007617b9ba3d806e924e34de239c82cf41c3dfb6d5dc966e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 22:08:38 GMT
ADD file:4c1773eeb1eb8715f5ee35943b6ec536fef99670907da849b45a0a757fbba521 in / 
# Tue, 30 Mar 2021 22:08:39 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 23:06:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 23:06:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 30 Mar 2021 23:07:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a1bfb759abe39ebb60de9072afdd4e8e520a2faad8d254176313a6e6015b23b2`  
		Last Modified: Tue, 30 Mar 2021 22:14:13 GMT  
		Size: 53.1 MB (53127187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9534d5829810d03b9be336ae682a19f3b3af31e49b6b2cecd48345d02bd56074`  
		Last Modified: Tue, 30 Mar 2021 23:18:40 GMT  
		Size: 5.1 MB (5112994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7efe461f21748a446fa26cb598f3c639bb1d56f946ec69917e33bbf0d1afe79b`  
		Last Modified: Tue, 30 Mar 2021 23:18:41 GMT  
		Size: 10.9 MB (10870209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af545e3a0b4ad1282fd353de2b1a13f1cfb41fddeafbbd5d1ab541524ae6898a`  
		Last Modified: Tue, 30 Mar 2021 23:19:32 GMT  
		Size: 53.3 MB (53299586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:62fcf45a6b204bb95f3339852238f344f4e3e53ae7fb8d34a5995d70590c157b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134649620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce02f00828825bbd46391614e72ac414c02778b3983f86dbf6bd70d290d1e773`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 22:33:49 GMT
ADD file:b2e7a11ad622cae2b5772745c60f7e97c6bf288f72404afbcaf250515017a2e4 in / 
# Tue, 30 Mar 2021 22:34:07 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 01:47:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 01:49:55 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 31 Mar 2021 01:56:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6eaed89d6188915a9c2274bc56b9635ae1ea5b1e77d1120748b46640f4765416`  
		Last Modified: Tue, 30 Mar 2021 22:41:14 GMT  
		Size: 58.8 MB (58783363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e1756dd634c1f69e7a925677805154a179e7c2a6335d250723239abfeccb7dd`  
		Last Modified: Wed, 31 Mar 2021 03:24:53 GMT  
		Size: 5.4 MB (5399652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:400e9dcceace6a7d3980843c5a23b79a016c8578ff3a1c8498c6d1cc599025b9`  
		Last Modified: Wed, 31 Mar 2021 03:24:55 GMT  
		Size: 11.6 MB (11619548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f8aeaad4704c36be840decf2c93f132a8125c29d76c7893b9bf34cc430976d1`  
		Last Modified: Wed, 31 Mar 2021 03:25:26 GMT  
		Size: 58.8 MB (58847057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:a4aa216dcf90e8303388f73a5ea03a31e50ee23b3b8430877353e0d7ec5ebde7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.1 MB (123079305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1475ae8f037138501fe0d178a1059f1368e8774c677e158c7ec90565f3a51ea5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:42:00 GMT
ADD file:06cd9dd574d91229d3aa7c645dda03791fcfbea17bb5964aaa1c5830d4174ab2 in / 
# Tue, 30 Mar 2021 21:42:06 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 22:41:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 22:41:13 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 30 Mar 2021 22:41:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1babe08b94dd6b44aca97f5f46b49d3c3e8b1571a49971cc87c69f9c91056218`  
		Last Modified: Tue, 30 Mar 2021 21:45:29 GMT  
		Size: 53.1 MB (53148454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:870ee6737fff361d9c0e6f905afcc7d45e779397ee67aa5b284eea46c9bd446d`  
		Last Modified: Tue, 30 Mar 2021 22:48:10 GMT  
		Size: 5.1 MB (5134079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54e0f71a88fa90537f4f2b0b092586cde9dc64e5833c45246c5d15be4e2ea20`  
		Last Modified: Tue, 30 Mar 2021 22:48:16 GMT  
		Size: 10.8 MB (10758401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6830c9f51e858407cacbf4450a91779c76f65e97ce85e9cace8d2eb566302487`  
		Last Modified: Tue, 30 Mar 2021 22:48:34 GMT  
		Size: 54.0 MB (54038371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
