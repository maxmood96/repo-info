## `buildpack-deps:unstable-scm`

```console
$ docker pull buildpack-deps@sha256:471bc4b421e9679c2d03de9b202d5ba13d8dc5bac58151b95cf1d9fe878736b5
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

### `buildpack-deps:unstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:bfbeceb6f6ba6391d6267f489ea26bc2f67a55ddd1d74db872565ccadad3eead
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.9 MB (139874795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f69fc30003a7b48eb1d4b267523478260d578d8bb232cc6cdeddb9228c6c6b8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:31:41 GMT
ADD file:ae19349870cdfda1b68970255f5f5e8f9cd15173da02e9e3404d59044fd19f67 in / 
# Wed, 04 Sep 2024 22:31:41 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:57:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 22:58:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b801efa715ff197e658475851b26398377386b508d479b783c9178607c76738d`  
		Last Modified: Wed, 04 Sep 2024 22:35:42 GMT  
		Size: 53.2 MB (53156851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e326b497ff3a4775f962f932d2595cc3a818c3d98338e35ed89a10f0da2a3db2`  
		Last Modified: Wed, 04 Sep 2024 23:03:13 GMT  
		Size: 20.5 MB (20503274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5baac0b2d691022b6e9d2a4261f3c3547b5863197743e9544f77779e589aa6a9`  
		Last Modified: Wed, 04 Sep 2024 23:03:29 GMT  
		Size: 66.2 MB (66214670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:6f214b53497b9eb190b57aedfa8795b3a2aabc115bdfb664c43d7ecde50ea22a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.3 MB (133296593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eefba7a5e499120643c9f46e4fbf7d581c6cf2524d19e01a2df5b060c69e75e6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:49:13 GMT
ADD file:8e4509f73b7c89f169188002c34bc8d03af1dafaeb6a9966b6690f196913262b in / 
# Wed, 04 Sep 2024 21:49:14 GMT
CMD ["bash"]
# Thu, 05 Sep 2024 00:19:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 05 Sep 2024 00:19:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:2257c73c251c8a677a6bc4308ec105c9b65d8a38c219fae44f204b71a1e09836`  
		Last Modified: Wed, 04 Sep 2024 21:53:07 GMT  
		Size: 50.1 MB (50112415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e56f0ff50207b50910941d32d7eb987ffc9f05840ac70dad39d626390727102`  
		Last Modified: Thu, 05 Sep 2024 00:26:06 GMT  
		Size: 19.5 MB (19492440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc7ad08e7d81f82d9e2c4214b3dfd3cce995412f651a08e233d2f09274292773`  
		Last Modified: Thu, 05 Sep 2024 00:26:24 GMT  
		Size: 63.7 MB (63691738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:58eef75c65666ab0c1901a5ed3926cc420503406798bf43b3bcfb595fdca219a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.6 MB (127600826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4db5592be70d2653aafa4fd4e8efb48fae22c8c7c92d8c9b0a0073e302f0f939`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:58:58 GMT
ADD file:f0cfa70a19518f2db4a813f0c5ad2bd292465f48e4249c9e0d9007c839212dd0 in / 
# Wed, 04 Sep 2024 21:58:59 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:32:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 22:32:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:d301726964d3d126bb25d90398b0f8668a5991c47d9f237ff6b62cb806b4ac84`  
		Last Modified: Wed, 04 Sep 2024 22:03:18 GMT  
		Size: 47.6 MB (47606007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eb70807b318cdced87a6ceefdc2aff1fbeb7a14035b9b9a74dc61fbbc6fd45b`  
		Last Modified: Wed, 04 Sep 2024 22:38:08 GMT  
		Size: 18.8 MB (18846433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b337ebc4882ba5bf1b4d0ef428653fa3a9963e209aefc6227386f1a76b3176`  
		Last Modified: Wed, 04 Sep 2024 22:38:28 GMT  
		Size: 61.1 MB (61148386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ecd47ce655417046236fa338583989e36ecc53f867d47933265582e908a1447e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.1 MB (140083206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e972b8a71ab393c2c9304c58adf31611d2c570c44fcec1db32f605084068bc15`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:40:29 GMT
ADD file:b8e117af2c2835c43068cfc9561a100b4a2ded0418c44e6deb66f2d0a088ee52 in / 
# Wed, 04 Sep 2024 21:40:30 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:04:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 22:04:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c86b9ce17f63a085a98e1dec4b1098c61e3e6ddd530e88cc0814e54f39b2ffd3`  
		Last Modified: Wed, 04 Sep 2024 21:43:55 GMT  
		Size: 53.6 MB (53597233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b16294a36c4e8dd71bc29360d35bd73856218dada114029995773ff9ab59e9`  
		Last Modified: Wed, 04 Sep 2024 22:09:48 GMT  
		Size: 20.2 MB (20248325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:301ed4283c0e34c1b3349c61e47afaf58a71aecea82db8aee69f2c8a865f8c6e`  
		Last Modified: Wed, 04 Sep 2024 22:10:04 GMT  
		Size: 66.2 MB (66237648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:aa2ecf738666a323f7e7d8c40adf61d1138d84212e4b23d6c39bbb7ea60a62bd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.6 MB (143561799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e36838e7d0962b487fa77b20613101f2b9c894ccb77220e1de7af2b9eef4c0b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:45:28 GMT
ADD file:2bc6b9eb390a3ccf12bc1146e52a121a20e72c5ac0e9e0cdde8678b8a64da9f7 in / 
# Wed, 04 Sep 2024 22:45:29 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:16:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 23:16:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:3cd4933de503c208d05c5e30920d85a6bfda122663e7dee7dc0ccda09e2913d4`  
		Last Modified: Wed, 04 Sep 2024 22:49:47 GMT  
		Size: 54.0 MB (54033260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad7d866b9f17c613349e89d962df48f1e6d0377d80990fd18cec1acea8c7e4ee`  
		Last Modified: Wed, 04 Sep 2024 23:22:30 GMT  
		Size: 21.5 MB (21528771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0676697198fdfee6917623f8c11e9e2725eb0d2fed789bf0e71473beb1651938`  
		Last Modified: Wed, 04 Sep 2024 23:22:51 GMT  
		Size: 68.0 MB (67999768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:8af6d4267f7b2ae3a48c5178fc412b19cdb2a9bffd157640981b2c023643dd41
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.9 MB (137949597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf3348df9b9deb7caa5c063fbbba211170c944cfb05d10a13b94ad8b67cbfab8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:16:21 GMT
ADD file:cfc638665fbd1de945c77faa66094fdc1c2a7a3e61a02e7558b48593a3569760 in / 
# Wed, 04 Sep 2024 22:16:26 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:55:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 22:57:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:0fe676035759e9ba94505d30bcdda1c4551dcb03be9195f24905e870dce00126`  
		Last Modified: Wed, 04 Sep 2024 22:24:56 GMT  
		Size: 52.1 MB (52121073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb0177a8f9c1d11993a113ed4db6fe549ff6e3060d86438ab68826142d1fd2d`  
		Last Modified: Wed, 04 Sep 2024 23:16:19 GMT  
		Size: 20.8 MB (20846214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ac59bc75368032a1aacc11229b927d620146529073e342e9762c4d3c1ff58a`  
		Last Modified: Wed, 04 Sep 2024 23:17:12 GMT  
		Size: 65.0 MB (64982310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:e8aed150e2bfc5c50e50f61c2df8c049f4679922d12e85696155ceb7bbd643f7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.8 MB (151805038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82b8defb7b402fa6d091d061e89f4fb5739b404d875b4b71417e564957598438`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:26:57 GMT
ADD file:453c36dbaa10f4b5f78376389c491de28c32bc4115eeb5a4f9dc3a13f8f33c82 in / 
# Wed, 04 Sep 2024 22:27:00 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:06:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 23:07:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:70bcb153a291f652093922260a9f87ef3e1b69ec4d2c2aaa4a1c06a4f81059e1`  
		Last Modified: Wed, 04 Sep 2024 22:31:53 GMT  
		Size: 57.1 MB (57091003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a777502b1e690fe078a6dc8872c353c31e2cf3ce95361a50bc93892f2d11c5c`  
		Last Modified: Wed, 04 Sep 2024 23:15:52 GMT  
		Size: 23.2 MB (23153949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90af665d962e383e3f1c7578bf8044f6cd38edea60132aae6dd8346eb0999613`  
		Last Modified: Wed, 04 Sep 2024 23:16:11 GMT  
		Size: 71.6 MB (71560086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:a94c313135c49432dcc25f79928b6432dbe57b3358b23fe6f8e2731e7a13cee9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.9 MB (136916590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:789762e26029931eda37c3b67f68f8756948dc5bce4177216ab908a7803afe0b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:25:42 GMT
ADD file:f7660b52d63bdf7c045c4722f75fe4e353e88b57bffc834348ad141ea0d12995 in / 
# Wed, 04 Sep 2024 22:25:44 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:55:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 22:58:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:f9fbdbff518ec38d5367f0b03978c04c3107f39b06d2bb498f646b4903fd13db`  
		Last Modified: Wed, 04 Sep 2024 22:31:12 GMT  
		Size: 51.5 MB (51473852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea5ef465799bf40fb820e96c6cdb0b3ca4823cc42d2ef644d6b9684cb164fde`  
		Last Modified: Wed, 04 Sep 2024 23:07:16 GMT  
		Size: 20.0 MB (20026801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d55a7954253b1f3af858d514d5a50598aad4e02214e66bf45ff119714d2d5fd0`  
		Last Modified: Wed, 04 Sep 2024 23:08:21 GMT  
		Size: 65.4 MB (65415937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:1a7538359bf9f1b11be91b4bc365f4a674e73db7cf8b9a58e2a5678e3e7db3b2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.6 MB (141610892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e8dab2bdfd8e752900399d53743d189ceed42554ec901984badaf89e26a2bb3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:44:11 GMT
ADD file:22e5ad49d0ca958c0a6f6e6b30f8ff191ced56a0355a55b9de94b5753608a9f9 in / 
# Wed, 04 Sep 2024 21:44:13 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:55:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 23:55:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:9d384a3df86e2f0599dbfcd66ea74d1e111f1fdf220d3cb1876a56217b3b0016`  
		Last Modified: Wed, 04 Sep 2024 21:48:46 GMT  
		Size: 52.8 MB (52756590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e449488f758e004c2a6dc29ff404f6c16a453d094520240af9e42e846bacb7b1`  
		Last Modified: Thu, 05 Sep 2024 00:01:38 GMT  
		Size: 21.6 MB (21616565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5fcd27216accec74418e978fea2c6be2752504c8ece95ef0dde330d8a5c092`  
		Last Modified: Thu, 05 Sep 2024 00:01:55 GMT  
		Size: 67.2 MB (67237737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
