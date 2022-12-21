## `buildpack-deps:unstable-curl`

```console
$ docker pull buildpack-deps@sha256:2ee107e9a648bfc1c12bacedfc1a0f12348d4ea11b588c5e77af3ac78f5b5b3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 9
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:unstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:cb90d2f70c5df3903f617d8c027941c3095dc472547011b98dbfb5127673b1a6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70698692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3426e28065a7daeb5d2125e796c04d273282ccd93a1b19ec774a8055fbb10234`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:21:52 GMT
ADD file:643fde45a6d11f36b1178a022667e74288e58a263ac7999c7cb023cb3fcde3a8 in / 
# Tue, 06 Dec 2022 01:21:53 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:17:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:17:58 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:f8db6e5cd5802a750fd04af4eb64a857f779b9c2333d2d830a50d7b2983365c1`  
		Last Modified: Tue, 06 Dec 2022 01:26:42 GMT  
		Size: 50.3 MB (50309617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b904b10ee4925c81495d781c9278243be45e6e2feb4350d4e8780c3c15c9d65e`  
		Last Modified: Tue, 06 Dec 2022 02:23:48 GMT  
		Size: 9.0 MB (9019750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826135e5b952effdf73fc4ca5766716e2efde4728890f709a8e0629212bfb80f`  
		Last Modified: Tue, 06 Dec 2022 02:23:48 GMT  
		Size: 11.4 MB (11369325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:e6b513ed07692c4528997c944c4ea2337de9d8f172f57e84c609ea623f5a9c50
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68771521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cefdcae0513f02784fa9385b4e14491ff71b367c11acb17a8a22634f221e6611`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:49:41 GMT
ADD file:2ae6125a895056caf86a0ea412a141fc00bb6485fece6b14db7232b3e06e9849 in / 
# Tue, 06 Dec 2022 01:49:42 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:18:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:18:58 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:597e07fd6304947f2f5075e2d3adcf596e2fc483cd39c89bb38d405526e7277b`  
		Last Modified: Tue, 06 Dec 2022 01:55:00 GMT  
		Size: 49.3 MB (49283811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a52a8179cb55c483e9ef86416325d19f993898e7370b10006cec49f11f48c47a`  
		Last Modified: Tue, 06 Dec 2022 02:24:29 GMT  
		Size: 8.5 MB (8473505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698a17cfcb2f3bf2de3db866fee5370a21c0a926022c6b4818c44705dce6b935`  
		Last Modified: Tue, 06 Dec 2022 02:24:29 GMT  
		Size: 11.0 MB (11014205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0f8f5ff98a81e3445793f9dcc72e13d5556adde06126b2003f645c2fb9a8df73
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.9 MB (65863687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb646e2f7608eac7af3d879b82136a58d5d2f77ea2dc2830328d785d06820a06`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:00:16 GMT
ADD file:093cea1a330b5b622916fc88f1590ffa3550c325a154b1252e373bcc62c2d8f8 in / 
# Tue, 06 Dec 2022 01:00:17 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 09:52:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 09:52:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:8d49421b71b8e5160d614ec1ebf9631e35648ff6ac4faf9dea1dd1f58c66a799`  
		Last Modified: Tue, 06 Dec 2022 01:07:59 GMT  
		Size: 47.1 MB (47097030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bd85fcb17f6a807d4015c1f238527bd7c852594436f570de9e1b3983f313eec`  
		Last Modified: Tue, 06 Dec 2022 10:02:00 GMT  
		Size: 8.1 MB (8120557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8049c8a3eea493f66ad55e374f1960cb3acf925cd222f5ba087c8a6f37c4eea`  
		Last Modified: Tue, 06 Dec 2022 10:02:00 GMT  
		Size: 10.6 MB (10646100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:5b19150ca15f1eb7c7266fadcd800e667b3b9ff81e83013d843b4c45b6591249
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70508385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60199b467e5dd3ea8330df0ea5fec2a5472ed13a1ea6eb114fa2143a2402da54`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:40:22 GMT
ADD file:afdb0d23dc73b5f1a887a2dfc3fb8fc2ebf210e9ac6b5d6748cd89c77d9e436c in / 
# Wed, 21 Dec 2022 01:40:23 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:09:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:09:11 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:951a6c4c03238810abf592f0f3beb641ea6b4153bfa55acf62944018b9ed669b`  
		Last Modified: Wed, 21 Dec 2022 01:44:40 GMT  
		Size: 50.3 MB (50335976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdda1c5e6e87491ced136c13ab5b4f5638649dbeff005a13d621df9a094822a1`  
		Last Modified: Wed, 21 Dec 2022 02:14:29 GMT  
		Size: 8.8 MB (8843497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ae130f92dbc53edf856d24c52cbf32f0410d34ccacd94bac928422ef4f4fc7`  
		Last Modified: Wed, 21 Dec 2022 02:14:29 GMT  
		Size: 11.3 MB (11328912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:ff53a117e9b60e29554ee7b36e4794ea15cfc5d01e251be1394bf4be3cc3cac5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.1 MB (72116759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b0d7a5dc53dedf29d74ff9f64cdd1909b99dc8c0dd4989d440df464a3290a22`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:41:02 GMT
ADD file:0909d182d8916b1b37783d0c3582c9d3f3edddf6cd27e90100343ed0462c9c75 in / 
# Tue, 06 Dec 2022 01:41:03 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:10:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:10:55 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:1cd5a2a4c5902ff854cd1178702a69271f9bf768ae5b99124c16b51e5c2d42a1`  
		Last Modified: Tue, 06 Dec 2022 01:47:24 GMT  
		Size: 51.4 MB (51358972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d5c5bef3805a0d8c076d12c22f99b0c27a09807eb93eeb57ae35352e352cd30`  
		Last Modified: Tue, 06 Dec 2022 02:17:38 GMT  
		Size: 9.2 MB (9196899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccbaac64d951183e4d1471ee19eeb170556b928f547c45a65c32e7c20445e6bc`  
		Last Modified: Tue, 06 Dec 2022 02:17:38 GMT  
		Size: 11.6 MB (11560888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:6806effc67a77f3cf00b5ce667eeaac2ab83512231b85f08653165558c79273f
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69822894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0f1a535f6be64ad7f372060aa41a6240dc05264059c7a0443e21f07838115ad`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:56:07 GMT
ADD file:f0c5ebbf2aa59cd4e0996c808ed4d378c47b86ca4c00f63fa5de02b4cb838334 in / 
# Tue, 06 Dec 2022 01:56:12 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 17:24:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 17:25:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:dfb5e33f7f324b83c5e49e84922c9f448eace01382dd0e6ac683debf1a61eb39`  
		Last Modified: Tue, 06 Dec 2022 02:04:23 GMT  
		Size: 50.3 MB (50319836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:002b834f7ef2a923258cac3647eea1dc30607526608cb7736365eb762f58302d`  
		Last Modified: Tue, 06 Dec 2022 17:39:24 GMT  
		Size: 8.4 MB (8384243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e9bab24553411999fc0ee1271fd159e73a742187f55b55da1666e8215102677`  
		Last Modified: Tue, 06 Dec 2022 17:39:25 GMT  
		Size: 11.1 MB (11118815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:9869b694ab06acd8a055f31546e6cb8d97f34f82c37e3a2fa5255aefab2019a6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76089194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2bd157b1d5a2b612aced51384b263070e5e9ff759333ad6e2a9fd0925688d51`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:18:26 GMT
ADD file:bdb06f846e6364870996f9ac20fb236d99a0ac4e61f11a82dda8599bbd6ea354 in / 
# Tue, 06 Dec 2022 01:18:29 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 06:42:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 06:42:49 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:7e30927c2af9840769d712ec0a0e33b7ccaba3ec9a715660e8c1b04953084dec`  
		Last Modified: Tue, 06 Dec 2022 01:24:47 GMT  
		Size: 54.4 MB (54361158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a78655a02977225694ec4b2ed16679949be76009f0b14a3f968d3cdb59c8b7f5`  
		Last Modified: Tue, 06 Dec 2022 06:51:46 GMT  
		Size: 9.6 MB (9599186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e7619effb72c38f135dd9a28562bd32fe00ff1e2195159f614d39b386aefaff`  
		Last Modified: Tue, 06 Dec 2022 06:51:46 GMT  
		Size: 12.1 MB (12128850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:73d0a50e74fdd1a297a1ca3c8afa742ca10aff1aa8ab2c224ac29108c577fcc7
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65392530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3036fa88cc278dfc3d9373f9e07d6a1cb1adbbacdc69154db704fd7cf9cd67e9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:10:37 GMT
ADD file:4015fba6ec44f577975c8a81f9b36bce2279ff3b1d5f60ec7a5b825a3de24fa6 in / 
# Tue, 06 Dec 2022 01:10:40 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 01:56:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 01:58:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:d83455d266574a702e0c821e6553aee8131f9a4eb280d6f00a3d1537ebd37434`  
		Last Modified: Tue, 06 Dec 2022 01:28:50 GMT  
		Size: 46.5 MB (46548318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afe654b8ab984b15d53bc79ba1e0ac260ed383d76961efab3052d692338587ff`  
		Last Modified: Tue, 06 Dec 2022 02:29:19 GMT  
		Size: 8.1 MB (8113036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:868e6ef6fc1764d3fb706bbee33f7c1e8495e8c93620e0e59484158ba00131a7`  
		Last Modified: Tue, 06 Dec 2022 02:29:20 GMT  
		Size: 10.7 MB (10731176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:25c291637498d71d9032e363183fc0f32a5924c683eac412cf1ac0d33dc5caa5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.6 MB (68579597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17309b002a4c0d69e77f76d6431aea17d6de39f73bd8d5da94994dfa8033c274`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:43:23 GMT
ADD file:9c101517ec1598b49e898a5a60ee79d12ae039f3da76a37f4b9ecc5211ece070 in / 
# Tue, 06 Dec 2022 01:43:30 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:12:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:12:40 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:377056d01f15b8c008b4b2d5e74aef86cd1b3c25771df79e7a3d4592cbbee6d3`  
		Last Modified: Tue, 06 Dec 2022 01:49:02 GMT  
		Size: 48.7 MB (48699631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592ad70c75e8b0ca75e558f3a54c3713a77da7920e04007e9375d34fc22d8ab7`  
		Last Modified: Tue, 06 Dec 2022 02:20:36 GMT  
		Size: 8.7 MB (8653107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7ee9f87d81b16e0ab87064ce67465efa2eb9ba18cfc708c866166dc66456f13`  
		Last Modified: Tue, 06 Dec 2022 02:20:36 GMT  
		Size: 11.2 MB (11226859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
