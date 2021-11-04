## `buildpack-deps:impish-curl`

```console
$ docker pull buildpack-deps@sha256:b8e6ef7f2b9e5ef1fad8e79719c732decff62f9a61fcbb61043a66c50626d1d4
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
$ docker pull buildpack-deps@sha256:54c923092a83d0fd403372895cc7a052c5d93975a64600e8b2dc87c3ce47494a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37624372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5784379919f76e6e2636d7558d1932259ce9a619c55a89fd18de979439e5a863`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 04 Nov 2021 22:20:34 GMT
ADD file:c061cabbaa10b98eed8dcea770d97000a2861c407f5208a0327bef2b38a99fee in / 
# Thu, 04 Nov 2021 22:20:35 GMT
CMD ["bash"]
# Thu, 04 Nov 2021 22:56:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Nov 2021 22:57:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:ae6e1b672be676522e8af69609544dd00b8517e394592a58194383b26e9b54c5`  
		Last Modified: Thu, 04 Nov 2021 22:21:31 GMT  
		Size: 30.4 MB (30378721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4488401b75c6ec432177829c795e1ec36857d568171ae1f197c2c24a9b7e7d8d`  
		Last Modified: Thu, 04 Nov 2021 23:03:09 GMT  
		Size: 3.7 MB (3693784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eb8a4e0bca131c5b9e451c10a345a0a13be03cf5ac1220cdc85f170d17be763`  
		Last Modified: Thu, 04 Nov 2021 23:03:09 GMT  
		Size: 3.6 MB (3551867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:impish-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:320faf26b91dadf96e3584a78a08c05d0592dfd89e440b6f97644a25e5115d6f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.1 MB (34107402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5ca790b6720183247a0a4cb2735fb3bf9773cba17b326e470a05ef7d20d5529`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 16 Oct 2021 01:12:36 GMT
ADD file:200fc5e8340bed54c8a1f2d364d7eecb37212e03a3c7c5f8b9fe94a5689b34fc in / 
# Sat, 16 Oct 2021 01:12:37 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 02:56:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 02:56:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:47d179bbc8c38e5833d8d05d251749ab4997c8e937e8913717f1124bdd9f3c75`  
		Last Modified: Sat, 16 Oct 2021 01:15:40 GMT  
		Size: 26.9 MB (26919116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08bb3c52ec36c639d0f08c768d92fdc4d7f3c666134b951d319f8898397c5a76`  
		Last Modified: Sat, 16 Oct 2021 03:07:20 GMT  
		Size: 3.4 MB (3445893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09246257384b997d403eae12b428a45f75bd853afa99e13b4ea5a6d3bda9c204`  
		Last Modified: Sat, 16 Oct 2021 03:07:19 GMT  
		Size: 3.7 MB (3742393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:impish-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:00c6025c7a15dfe57955537030d672bcdcaf4a2389fc446007e602d155927bf6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (36031863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b11808ca59b32ca29aceb263695f64a95c22f3784efef11a16304f51f440ff1a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 04 Nov 2021 21:55:45 GMT
ADD file:1b42b91df70bf5eb9529802354c8c97bb9ba991a7885a3fdd4ad5be4b662b70c in / 
# Thu, 04 Nov 2021 21:55:46 GMT
CMD ["bash"]
# Thu, 04 Nov 2021 22:28:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Nov 2021 22:29:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:07806c11d5adbc5d83daf2661f72147213f9056f681e452180dc14d81e368e17`  
		Last Modified: Thu, 04 Nov 2021 21:57:10 GMT  
		Size: 29.0 MB (29026100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a952a5c90bcb8e3a8ab1bd7854d8265e7fcb3cb0c0f417fb5722e8f3e0972208`  
		Last Modified: Thu, 04 Nov 2021 22:33:00 GMT  
		Size: 3.7 MB (3678628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cca9702f2a91f991f023bbb9b582e71befe4781bbaa74653b2458540b02c0e3`  
		Last Modified: Thu, 04 Nov 2021 22:32:59 GMT  
		Size: 3.3 MB (3327135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:impish-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4ac0688649cf19387d38e7b043f66225ec9f5309acad8674622821bc726b28c8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.6 MB (44569136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81e1b983abbb1ffbb8530aa484a7d0b2e197359e1b0c09e942016ffdbfe2d748`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 16 Oct 2021 00:37:08 GMT
ADD file:2882612be3480d0a26c565cfff723f6f7c913ecc1e3b982def388f5c29ad10e6 in / 
# Sat, 16 Oct 2021 00:37:12 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 01:18:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:19:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:4cfd5cbebb9f6bac4f6c4e8b0ed1450129f245085d7131094975207c3091fb66`  
		Last Modified: Sat, 16 Oct 2021 00:39:02 GMT  
		Size: 36.2 MB (36177739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5e42bcc4ae69e168604f5e12739b0b1eb5c7801c5bbba53b80248a3522d3b2`  
		Last Modified: Sat, 16 Oct 2021 01:31:20 GMT  
		Size: 4.1 MB (4149852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fbf4430060475cdfccdf811046cc128f1e962010f7015eb473cd56a44a181a8`  
		Last Modified: Sat, 16 Oct 2021 01:31:20 GMT  
		Size: 4.2 MB (4241545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:impish-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:79286edeff7a31bec8b2e2b654586ba284c8dbada8a7eac779484e0d00f8ecbd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34505933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a31712f5300998cfb5a7da064b6738fd8ce992f469228720944c925fc306ae57`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 16 Oct 2021 00:17:48 GMT
ADD file:8cf59b4b38ccab14d48f2740546784966d4b20690dc57f9018241a62adac259e in / 
# Sat, 16 Oct 2021 00:17:50 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 01:02:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:03:17 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:19a9653dc9c1bf288e8c03d2027a0edd6609e7bc4c852b05e2ba35e947868701`  
		Last Modified: Sat, 16 Oct 2021 00:31:12 GMT  
		Size: 27.2 MB (27208455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e415d53d305cea0edcb8861ea11f8c974a195af5e0bbab60d58e5e787c69b09`  
		Last Modified: Sat, 16 Oct 2021 01:31:29 GMT  
		Size: 3.5 MB (3494237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c502225d86b92683284985a96ecaca6eec34631b1832346308e6c7a4edb2378e`  
		Last Modified: Sat, 16 Oct 2021 01:31:28 GMT  
		Size: 3.8 MB (3803241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:impish-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:69d0be5d4a84d1fd9eccc366c301e3bb5eb1e5ee063ae63dfb73e0ab2b878b53
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 MB (38256713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4e776fddfc4e1399852bc124156b58b876d4f021cd53374abd1813b05be224c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 04 Nov 2021 22:00:03 GMT
ADD file:ab83cb3e32154ba2db5167029d8e8d5388c50b5c29d8c79c713c0e0d2d692d27 in / 
# Thu, 04 Nov 2021 22:00:05 GMT
CMD ["bash"]
# Thu, 04 Nov 2021 22:18:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Nov 2021 22:19:02 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:e737ddf26245fcdcc7eced9ccccb22176e9f1ba12d8f0d15cb1342c337544bdf`  
		Last Modified: Thu, 04 Nov 2021 22:01:24 GMT  
		Size: 30.5 MB (30525829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de0355a8a2f0153f71261e3597b628202632603a052d63c9cecc0e1da9659b7c`  
		Last Modified: Thu, 04 Nov 2021 22:23:03 GMT  
		Size: 3.8 MB (3767643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f088a56f227fe3f111d256ae3c603419e2b9c7ee314548ef27c2479050a69e`  
		Last Modified: Thu, 04 Nov 2021 22:23:03 GMT  
		Size: 4.0 MB (3963241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
