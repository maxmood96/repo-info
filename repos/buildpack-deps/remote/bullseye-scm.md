## `buildpack-deps:bullseye-scm`

```console
$ docker pull buildpack-deps@sha256:a82b1a6f082d0ed7ed8d581c511f9603d0d634cc0377dec346422ea09dc1b030
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
$ docker pull buildpack-deps@sha256:ce20d2552bb0c5b928bcb0e04cfd6058e9cd765f9a4c4e7a53254d3c2fc30629
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.5 MB (125496597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c54c9580cf7437cbbb84ff4cb13c0ad4098d3361df95144b2b9ae3ed03f035`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:20:10 GMT
ADD file:5c0c0fbac6fe503c1d3e894e0b3b1081172862074ceed378a7e4b82810536415 in / 
# Tue, 09 Jun 2020 01:20:10 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 01:44:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 01:44:55 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Jun 2020 01:45:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:07f1101e3e85b531862163b4177bce7f401eac107a6537ab74195b395aab30b7`  
		Last Modified: Tue, 09 Jun 2020 01:25:12 GMT  
		Size: 51.4 MB (51413507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3778b8917e949d9f5a076dfa475de8efd560f3537663e53ea97e720164dd04a8`  
		Last Modified: Tue, 09 Jun 2020 01:58:55 GMT  
		Size: 7.9 MB (7920377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4483e6954e0bd5f111c062eb05965cd7e6719912e726370891437022744c5b6`  
		Last Modified: Tue, 09 Jun 2020 01:58:55 GMT  
		Size: 10.5 MB (10488194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4457fc20950e802370e7f15361944b8f58ae25f895ca6cd42e008e97f37e60fd`  
		Last Modified: Tue, 09 Jun 2020 01:59:10 GMT  
		Size: 55.7 MB (55674519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:80dc6e43ffce422199c091abcb69f79891fd0b189cb75cc0a00e0d67193cb5c6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120370404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b41ac1e5fc9f58bc63c9843bffa4fe73ca11f6f7cec05d3e7479e39931fc6900`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 00:50:42 GMT
ADD file:ce6e6e497a66e2260260f97fe2b75c1b96d64554c5be6b85940fc97e2668da58 in / 
# Tue, 09 Jun 2020 00:50:47 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 01:23:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 01:23:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Jun 2020 01:24:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0cdc268ccc707144d53d65848999b81d39614c650312788e7e7f99c56bad6d97`  
		Last Modified: Tue, 09 Jun 2020 00:58:27 GMT  
		Size: 49.4 MB (49386621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d86dad966a8a2c2ed7fa83ce42c1fab459f250a20c801eeaf7703e5022cf7bfe`  
		Last Modified: Tue, 09 Jun 2020 01:56:29 GMT  
		Size: 7.5 MB (7500258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5380110dfa23bbdc9c556dbde735e0c5c0b768f93dfc86e54d0c9e2adb417562`  
		Last Modified: Tue, 09 Jun 2020 01:56:30 GMT  
		Size: 10.2 MB (10175863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd1be4fce84e1c9c761b63c553df33838f2c301c69f612c6a0c17003702eadf4`  
		Last Modified: Tue, 09 Jun 2020 01:56:54 GMT  
		Size: 53.3 MB (53307662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:09045d0c513ff14b62be45236791142c3bc5e5f1e529bdb60729b7ab28aedae3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 MB (115351772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e47f785ed6f54fdee147ba9825f66ed91f09b5674678c2d1d2b74d276f2e131`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 00:59:35 GMT
ADD file:2ade41d5fab2319a3cbf973cc24aec4f6b9e2b14fa04578886fa1cbe30e511ef in / 
# Tue, 09 Jun 2020 00:59:37 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 01:37:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 01:38:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Jun 2020 01:38:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1c27049a799a3404864ae1732d5aeaafaef7ce0fbbde552819e2c88bf38ae9da`  
		Last Modified: Tue, 09 Jun 2020 01:09:22 GMT  
		Size: 47.2 MB (47197823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63b26b1bf1a6c82f64fb3246383f0e2081a0624861a1d56ae6b025e7406652be`  
		Last Modified: Tue, 09 Jun 2020 02:09:55 GMT  
		Size: 7.2 MB (7243223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6ad054395bdad7163609959df4dbaf402b1787fb76da08b5c5f89358ac9f2e1`  
		Last Modified: Tue, 09 Jun 2020 02:09:55 GMT  
		Size: 9.8 MB (9823296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cf531c73c6f446da9fd9e5bfae5da82ba0d7fc288a2c05cb2981e723a94e0fc`  
		Last Modified: Tue, 09 Jun 2020 02:10:19 GMT  
		Size: 51.1 MB (51087430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:06537bb9d61c1e7e6fece52511270125626d325532e6236f28c42945810fb550
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.3 MB (127316061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b3ceb06299fe8bf1cf0bfbe7636f66e6e53f31e30214e1b09ef88d73f3ce785`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:39:52 GMT
ADD file:19b87dac8088f103e1a9992c229b17344439af0da8af45bc6d678f69471077d4 in / 
# Wed, 22 Jul 2020 00:39:54 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 01:08:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 01:09:55 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 01:12:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:508fd3fb95b7fcde22f3f927caabf293cc04dcbdb4c45b85a5130d5122e12a0c`  
		Last Modified: Wed, 22 Jul 2020 00:46:40 GMT  
		Size: 52.9 MB (52886369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5915a33a39d2dc36bde47815617bc03c29dc80e9539719e24091c59faeb64f73`  
		Last Modified: Wed, 22 Jul 2020 01:33:46 GMT  
		Size: 6.6 MB (6634801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696ea5d467b9d2286b1dcd428b411982c7ca3d5a2471f013ef721842af48ec9b`  
		Last Modified: Wed, 22 Jul 2020 01:33:46 GMT  
		Size: 10.6 MB (10591622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65ce2f62ac83f0fb7af53d2e4faa8b93e2b37157d2cfd0eb7725e95b633a33e1`  
		Last Modified: Wed, 22 Jul 2020 01:34:12 GMT  
		Size: 57.2 MB (57203269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:64e3c0d96bba9be04ffb9d8750f21201747b11ea081c20e26faa3adc3f6c9293
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.0 MB (129016003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b1a9be4d8fc78c7086c774c7c473c726a77b550a92bbb18c0b975d8345cd6c9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:39:02 GMT
ADD file:8b8ef4a5f8149eba4e2e5c50f0e95fcf5b9e729c8fdf74e04ac12871a5e80281 in / 
# Tue, 09 Jun 2020 01:39:02 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 02:09:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 02:09:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Jun 2020 02:09:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e2c89c7c8738f073b61540c4d15c26608d6fa4a9756e727acf258769f4f15726`  
		Last Modified: Tue, 09 Jun 2020 01:44:12 GMT  
		Size: 52.5 MB (52522870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f68ddf662651a633a2f0e4f65ad7228c24d57d8b14286a1b62fac342f6375f75`  
		Last Modified: Tue, 09 Jun 2020 02:30:14 GMT  
		Size: 8.1 MB (8099334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efad6eefe2105d3cfe168434dd0f3ae253e5013636bf2e2cce89b8545995ea84`  
		Last Modified: Tue, 09 Jun 2020 02:30:14 GMT  
		Size: 10.9 MB (10869142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66019f865e61d00591abfb7d0e9c883b48388b55debf3277d36172b8bd3a424a`  
		Last Modified: Tue, 09 Jun 2020 02:30:44 GMT  
		Size: 57.5 MB (57524657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:4a4886053ef4cf59ff7b0faacbfbaca597ad92d739141f2287c6497eb7140de7
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.7 MB (122726423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d08fb85567629695b13194105787b344e4dbbc44279a61b59f25e60e06099e3e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:08:53 GMT
ADD file:080fe104a5c84718f0c41015a3a4bf48ef0d94088beb50e3b0346ea572302008 in / 
# Tue, 09 Jun 2020 01:08:54 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 01:46:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 01:46:27 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Jun 2020 01:47:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4295b4a99b75e24118d0a604e63b142af1639be17451d6724215fd11e6fdd041`  
		Last Modified: Tue, 09 Jun 2020 01:16:09 GMT  
		Size: 50.2 MB (50162108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6b19c74224bd3e9030de803cd7b2cf6f938ee3548998819522a786837b1caf`  
		Last Modified: Tue, 09 Jun 2020 02:06:44 GMT  
		Size: 7.4 MB (7447679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e65e61fe718bcf10bce9dbbedd4844ba55e178913be199a5e4cd26a5ca17f1`  
		Last Modified: Tue, 09 Jun 2020 02:06:44 GMT  
		Size: 10.5 MB (10505180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65ba7560d369d9be99a66746b1d7e1a04d087826851c960badca01c94c787d53`  
		Last Modified: Tue, 09 Jun 2020 02:07:39 GMT  
		Size: 54.6 MB (54611456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:f8ceda459e55a680c2c0b4c57fc5d84f00076c056afd07547b9898e91e0dc58c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135788924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ce8a02b1187756382e1acaca30de0e0b3bd1c94d801588440ff120164535d12`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:21:05 GMT
ADD file:6e35f025b9b04e8864b94d9eee0225ff993cbeedecd7bd805002a3c5d3a76bba in / 
# Tue, 09 Jun 2020 01:21:10 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 02:45:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 02:46:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Jun 2020 02:47:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:92571d4834cabeca9400dd51bae9bdc41218cc857202b01ef83f6ee357784097`  
		Last Modified: Tue, 09 Jun 2020 01:28:39 GMT  
		Size: 55.1 MB (55147983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6088d8f42ecc239b36ce954e9d66d43e9651f30b809d5d1be486643a2ab46659`  
		Last Modified: Tue, 09 Jun 2020 03:40:52 GMT  
		Size: 8.3 MB (8345448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db3ec7901544300bb7ab1472297521c3c44db747007d75b46b2cd95b1eb1af0`  
		Last Modified: Tue, 09 Jun 2020 03:40:52 GMT  
		Size: 11.2 MB (11227910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3a032438787728277a3f2f6530d043962d63b3ba5c4109fbd329f60f903394f`  
		Last Modified: Tue, 09 Jun 2020 03:41:39 GMT  
		Size: 61.1 MB (61067583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:1754731c2b8c2b069b732ac94918e01cb17c017b52349b78969aa003c39f95c1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125681103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6193e592885e27f3708e99bf7466af138b44361e4f7fe29175e768261eca554`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:41:56 GMT
ADD file:64e5f3d6bda82e2ceaeaede4b9646a695e0b5c2daf32f3ceac3f8404c189999e in / 
# Wed, 22 Jul 2020 00:41:58 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 01:03:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 01:03:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 01:04:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eec92be71167cbdfe66ed0a95cf2650cfae8fc7e2f6d3c038707f63a74aa347f`  
		Last Modified: Wed, 22 Jul 2020 00:45:06 GMT  
		Size: 52.4 MB (52406289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c7d5f37f3ba0ac86762ed35d75a67c2913a5142f0395028219243aee7bb41b`  
		Last Modified: Wed, 22 Jul 2020 01:11:26 GMT  
		Size: 6.6 MB (6599170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f76cc1489ae85b994163f909e22b33f76692a45947a1fba3d3d821d5327b317c`  
		Last Modified: Wed, 22 Jul 2020 01:11:26 GMT  
		Size: 10.5 MB (10460561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9640f5165a5b3657fe9e2a6073f569c99ab970b92a2820d0a281d0ab86fba7fe`  
		Last Modified: Wed, 22 Jul 2020 01:11:39 GMT  
		Size: 56.2 MB (56215083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
