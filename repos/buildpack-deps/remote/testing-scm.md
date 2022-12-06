## `buildpack-deps:testing-scm`

```console
$ docker pull buildpack-deps@sha256:d86deb93f3e3d5cdc6655e6b39dde9fd7e2c39d96e1b2dd6612e9ea58084fe1d
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

### `buildpack-deps:testing-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:577ab2f260f71b4b4a4408408eda983022a3d40b26dcd55acfd936363475f35b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.8 MB (127838256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5190a8ed17e6e7751cf6b3e22a2c3fcad79fb275a782db467486b20068b8679f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:20:17 GMT
ADD file:bc800ccc3502eee52ab13da7e930beeea45bff7ec8e6f625f2958550a0e0c4a0 in / 
# Tue, 06 Dec 2022 01:20:17 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:11:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:11:16 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 06 Dec 2022 02:11:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3d5213c1b98149df5de6014f7a0822d3f7c1239b55b191918b5019861d2385bf`  
		Last Modified: Tue, 06 Dec 2022 01:24:15 GMT  
		Size: 50.3 MB (50260519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7adf3c7a7c116d44387858d478529693ecefc787b2f5ab45aebdfe6884125ff8`  
		Last Modified: Tue, 06 Dec 2022 02:20:43 GMT  
		Size: 9.0 MB (9019439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4a4bc2fe30909b334399b20974788d0da585394e55d471a14a5f3e60134f81d`  
		Last Modified: Tue, 06 Dec 2022 02:20:43 GMT  
		Size: 11.4 MB (11368978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0b4c76cf5170ac15770cc8edd5f98ed33f766d4a9d72d3200443bb50df873eb`  
		Last Modified: Tue, 06 Dec 2022 02:20:59 GMT  
		Size: 57.2 MB (57189320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:01538b7f014c18aa5755a5aeca357fed2790481d451ea65ee107fb870dd048ee
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.7 MB (123656654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f684fae0ba99c5ff15cefaa04a1c6acd9ce108e39e82111c42d793876054956f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:48:36 GMT
ADD file:6f4f61d29cd543b4aac92345f1eafd1e5d79db8feeabac7b2a9bc503e68a105b in / 
# Tue, 06 Dec 2022 01:48:38 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:13:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:13:32 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 06 Dec 2022 02:14:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:378b1d254700c864b8aa581433afac6f6a683e7a13dcd04dea4c2a4f39262d45`  
		Last Modified: Tue, 06 Dec 2022 01:53:21 GMT  
		Size: 49.2 MB (49227330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e826d0e46f98778a11a16901155a7c927623ef76983dc642045b4027c428d37c`  
		Last Modified: Tue, 06 Dec 2022 02:21:49 GMT  
		Size: 8.5 MB (8473083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08de4522b4c18fa88e7bb28665965734e7db1c247bb0abb5a73dbb90706c686b`  
		Last Modified: Tue, 06 Dec 2022 02:21:49 GMT  
		Size: 11.0 MB (11013908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6633a312462679c7a403e220bef275aae8c452ea6ae5dd3493f1a95c930823d`  
		Last Modified: Tue, 06 Dec 2022 02:22:11 GMT  
		Size: 54.9 MB (54942333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d7473876411ec4c19adddea23b41ee2d3e584652b75fcd6f70628659b8442582
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118749075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69a472f37c631d24d90aa78aff32ff8923d6830011f6e087124eeb8d8601a8fd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 00:57:56 GMT
ADD file:82dd62a6df63f711bc714098f18b9106a7507772b5320c66a30f7ccba2ae24a0 in / 
# Tue, 06 Dec 2022 00:57:57 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 09:46:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 09:46:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 06 Dec 2022 09:47:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2e675a2bd8a737d1b09b68b33be3a9ae4bf0f69f7b1ce279fd4c63e38d294b1b`  
		Last Modified: Tue, 06 Dec 2022 01:04:50 GMT  
		Size: 47.0 MB (47047090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1269cf9b4020da3d5a105d4cb0de965da5ff3b3cdef38d40b0b2a8adba6d12ef`  
		Last Modified: Tue, 06 Dec 2022 09:58:20 GMT  
		Size: 8.1 MB (8120353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5338e4fef4822c3d44b512384c9d19acb8331d7a0fc436c4d45f8e273d696c18`  
		Last Modified: Tue, 06 Dec 2022 09:58:20 GMT  
		Size: 10.6 MB (10645726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f9e39420db977e65e05dee5a6f4a406a51b5e6d6d3d49f1ff88cf47bafa4f7`  
		Last Modified: Tue, 06 Dec 2022 09:58:40 GMT  
		Size: 52.9 MB (52935906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:3eb912a1065df2981edb99051872d2296d6144b13dcb470f012baa87c96c6d98
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.6 MB (127615018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af57e892af23744fff44dccc82c38aa4cea19f6293d28b68ae46f61c978f5346`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:39:50 GMT
ADD file:de3ed89259c63b45a553c11db2206a6ca4201bfd264f04890af2c672736c15b4 in / 
# Tue, 06 Dec 2022 01:39:50 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:02:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:02:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 06 Dec 2022 02:03:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6d78ccc24e38e1c539440b7f90d65e136bba8366864c2b4a45e3956272709049`  
		Last Modified: Tue, 06 Dec 2022 01:43:02 GMT  
		Size: 50.3 MB (50307715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bb26845d7157ae0fdc105d1666dd413b3f1236876c9e38fe497d4b566c5b8a0`  
		Last Modified: Tue, 06 Dec 2022 02:10:56 GMT  
		Size: 8.9 MB (8851114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aee48d89e1a98c15d782346793fdaba61be0e798358172b68670681463bdd69f`  
		Last Modified: Tue, 06 Dec 2022 02:10:56 GMT  
		Size: 11.3 MB (11325483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2882696f0c89ced811afa19b67056d882fbab71ccb7f7e31631ccdc1d1349d0`  
		Last Modified: Tue, 06 Dec 2022 02:11:13 GMT  
		Size: 57.1 MB (57130706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:47907807283ca26435ad4b3ae878332554fcca9ec9429713b54bac9730d2cf2d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 MB (130744403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e54168a3c6d3359d7791522c4e690fb2e254bc901a1c445d21f76848b7de5b1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:38:43 GMT
ADD file:6064ead20e3d5415784fcb74157c3ba1b90982f542deb132e9dabb2a1712e396 in / 
# Tue, 06 Dec 2022 01:38:44 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:05:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:05:30 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 06 Dec 2022 02:05:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:45070d389a5ecd4dae6cdcb3e06567c8481416cfb2efb085e318fb5e2d11393b`  
		Last Modified: Tue, 06 Dec 2022 01:44:36 GMT  
		Size: 51.3 MB (51301574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efe8313be6a60f2abeebcfad5a2e4539e7d4b28618e0b019908926dd39c9c1bd`  
		Last Modified: Tue, 06 Dec 2022 02:14:11 GMT  
		Size: 9.2 MB (9196657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aa4a90125b538cbb0d87c8c0d37737cdc01ed561a27c8ecfae4cc4f708aecc3`  
		Last Modified: Tue, 06 Dec 2022 02:14:11 GMT  
		Size: 11.6 MB (11560721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c4c1fe8d1b528c380407ded013fe72d397a8e0cc5e05d87cde0f468224efdfd`  
		Last Modified: Tue, 06 Dec 2022 02:14:30 GMT  
		Size: 58.7 MB (58685451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:c9ef6742bdc376bb0b803d373d3096d3e258cf82dc0691737e3de1ce8d19dd99
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.8 MB (125817881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d16f45c032cf531ba1f74c85f022ff64703cefca237002259855de0e40be450a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:53:35 GMT
ADD file:5f771b53cd80db61f6fcf0df30ca6b99cd2c768f57ab1ffdf53d1f646b7db7c2 in / 
# Tue, 06 Dec 2022 01:53:41 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 17:06:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 17:06:58 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 06 Dec 2022 17:08:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a9cc4004cb6d73c258a4d864dabb35e2beb3272eaf0de591430b0bb1af15141c`  
		Last Modified: Tue, 06 Dec 2022 02:01:46 GMT  
		Size: 50.3 MB (50259491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0bb8986f763b3dee4c5b32d9c82a018159c1bc6452e370fe08635660e89d7fe`  
		Last Modified: Tue, 06 Dec 2022 17:32:55 GMT  
		Size: 8.4 MB (8384079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a60f3afb7af77661e81375d03b106172646d324a7f36dcc156ffe006dd22158`  
		Last Modified: Tue, 06 Dec 2022 17:32:55 GMT  
		Size: 11.1 MB (11118473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc29876f092a179802df5708c39f6d2379d6f42f3ee77ce5ecf099fc21378b58`  
		Last Modified: Tue, 06 Dec 2022 17:33:46 GMT  
		Size: 56.1 MB (56055838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:346d445c513352178e82efc80785a56801b97af1a753244dce46ac7b138d31d5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.1 MB (138095188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad54a0a049d7c7d83d0da4653ff0a141cde3b616657e7148f6938197de51158`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:16:54 GMT
ADD file:394004d3191138471ba2dd50891718f9142a137ec9018f4f69a653139a98abf1 in / 
# Tue, 06 Dec 2022 01:16:57 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 06:34:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 06:35:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 06 Dec 2022 06:35:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c1206773e59171c1200c3692244202cc0da97f8fc41cb86ed64f742f1e75b47f`  
		Last Modified: Tue, 06 Dec 2022 01:22:51 GMT  
		Size: 54.3 MB (54319290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d2bf8fe0b01dd711eba4372279b1ec1baca4dda44423540050ddc904916d0bf`  
		Last Modified: Tue, 06 Dec 2022 06:48:23 GMT  
		Size: 9.6 MB (9598813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:594f52d0cb31836574048a516ce0e264a5125592606d1b50484ce8dc7c4f0b92`  
		Last Modified: Tue, 06 Dec 2022 06:48:23 GMT  
		Size: 12.1 MB (12128375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3402ebb5b72aa962b6cb50c3e3855f429e6f8cf5f152b11674362ce642dcf13d`  
		Last Modified: Tue, 06 Dec 2022 06:48:50 GMT  
		Size: 62.0 MB (62048710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:435edd6684979fd14d47ca81cf6f1b95ea55c8529b4af451ec3ed814db6c1cb9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124933533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d9b60c3d183ffc35f6413960a6f108663916e24f5a3368ceedcf37f2b0c4633`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:41:45 GMT
ADD file:45186e2067a128e8dbf3558a97cd5853548faaf7c2bb93ef1544ed66907fcf19 in / 
# Tue, 06 Dec 2022 01:41:55 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:06:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:06:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 06 Dec 2022 02:07:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:effa21bde36181862f20d53853fc03e36421f6a13d6aad41051d593fe9c7c097`  
		Last Modified: Tue, 06 Dec 2022 01:47:58 GMT  
		Size: 48.7 MB (48664905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67f5dcd56007991a3866c8b0bf2ee7220f18a57fb48ff74112e6c810f63c8b96`  
		Last Modified: Tue, 06 Dec 2022 02:18:52 GMT  
		Size: 8.7 MB (8652754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1216521a137ae490612192a50d936077fcb94da6292a8ef16485599b92a5ace`  
		Last Modified: Tue, 06 Dec 2022 02:18:51 GMT  
		Size: 11.2 MB (11226716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49291721bb021828aa82c6d2c7e2c9cc22d7fe71b2f0406cef91b807704ecbea`  
		Last Modified: Tue, 06 Dec 2022 02:19:06 GMT  
		Size: 56.4 MB (56389158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
