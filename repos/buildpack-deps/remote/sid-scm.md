## `buildpack-deps:sid-scm`

```console
$ docker pull buildpack-deps@sha256:e26cda543f43faad73ee329456f0339957459f706c54c28601eb337a87c97de7
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

### `buildpack-deps:sid-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:2cc4e1de08612b19eeabe556524be3442ee72ca8080f53010e8b16551b53b674
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.5 MB (131463873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3035b966ed9036ca2f656ab4ab1f3c96996937c514ca50d5deef155f7e6cf82`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:21:21 GMT
ADD file:e1060039de636fe2bfa207b8a071caa2d6ead322d1c2621e322409706dd97730 in / 
# Wed, 21 Dec 2022 01:21:22 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 11:17:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 11:17:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 21 Dec 2022 11:18:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fd14438c7d22fef775ab49a94c6b4c250839f557fcdd15c31806e0fd16591085`  
		Last Modified: Wed, 21 Dec 2022 01:26:09 GMT  
		Size: 50.3 MB (50286143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42cc8f0be92b36616eb2e66ef11a4ca3b0afdcf12001156b466f3b4ba9d8de6c`  
		Last Modified: Wed, 21 Dec 2022 11:23:35 GMT  
		Size: 9.0 MB (9011383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d830ca216826fe2a4f6f72ceaf720feb2700e57798116adfad2d37e4182a5e5`  
		Last Modified: Wed, 21 Dec 2022 11:23:35 GMT  
		Size: 11.4 MB (11369908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b6b17ea2a65093c478ec5181570b3d64d3d1e0f21283ee880611451c36d5ee`  
		Last Modified: Wed, 21 Dec 2022 11:23:54 GMT  
		Size: 60.8 MB (60796439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:9f98ea91970e25833ccdcbcd4f9ca3efec9b9c340eec97d85f1b2011170e8dd5
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.1 MB (127127389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:823ada119b52e40faf340e6eff77a3c79b2f0f30c9dc3b6bd6dbb4a379a68083`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:49:19 GMT
ADD file:7e649d148f5ac98acdfce2b45b373b5b22a9792e3d365d3f1dcb2414a59f4149 in / 
# Wed, 21 Dec 2022 01:49:20 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:22:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:22:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 21 Dec 2022 02:22:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3175fea42c68213e6e72826c3ee7daa4a58070ce07ae526e91c30a8743d89be1`  
		Last Modified: Wed, 21 Dec 2022 01:54:28 GMT  
		Size: 49.3 MB (49270781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e2f8a381ecb39f18e385e77a8e8d6e9d27b631c659084d0d9a3a82c5e9f9b47`  
		Last Modified: Wed, 21 Dec 2022 02:27:59 GMT  
		Size: 8.5 MB (8463955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:681a42b466ccec4b7ac8c821ac8ac7d1787f7968ea77629bcfd8efa108d32f4a`  
		Last Modified: Wed, 21 Dec 2022 02:27:59 GMT  
		Size: 11.0 MB (11014376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daf14e116100aa5dc86d38341ffec41bc259ac037aa38c189caa7b1d9f1d7f56`  
		Last Modified: Wed, 21 Dec 2022 02:28:21 GMT  
		Size: 58.4 MB (58378277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:ac1fc2aad3a34c055d0fdba3cabeeb60bb1de6f348aa2fb112746ef399009332
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.9 MB (121888730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98dbaa85a28d32b846d28be7f671d920fff2780789e7c8c5daecdd61d56318c8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:59:31 GMT
ADD file:9f6e7ad60906ff390d6369133d129df5057cc1505edafd2cccc2eefa5265ddaf in / 
# Wed, 21 Dec 2022 01:59:32 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:31:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:31:24 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 21 Dec 2022 02:31:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4d12d04403dcef32bd0b6201954d02c0de421dabf04dd54d568898f376cb96c5`  
		Last Modified: Wed, 21 Dec 2022 02:07:07 GMT  
		Size: 47.1 MB (47080683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f36680a9d2eba076180efb89a2b7a21233fc4e0a38e383b2c389f543e56a48be`  
		Last Modified: Wed, 21 Dec 2022 02:40:30 GMT  
		Size: 8.1 MB (8110360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edac00689713d5d2b7fdcc4f1c017ec260832d0c2a65021c7f013a4a71c9bdf0`  
		Last Modified: Wed, 21 Dec 2022 02:40:30 GMT  
		Size: 10.6 MB (10649074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aeb2e96f612174a7d5711371774c88238e9809c0d631f6a0e50ee1591e53bfc`  
		Last Modified: Wed, 21 Dec 2022 02:40:51 GMT  
		Size: 56.0 MB (56048613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:08d2f7a616113680eaf26871efece80e9fad1ca3afa715a34f127fa95202b09a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.2 MB (131173276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11f06580932d0b393e404f8dd737ab3a571d0feec26636717b103654b98bd293`
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
# Wed, 21 Dec 2022 02:09:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:b7c026988df51d7264167f40103dd5c01db4eb446f90f5f6787ce90289773298`  
		Last Modified: Wed, 21 Dec 2022 02:14:47 GMT  
		Size: 60.7 MB (60664891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:45780737749d5b2250ff5560cd1a826940ec84aab71d2c9e5700f3488c6f23c5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.8 MB (134785489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e5d31111730440e34e5b3f6d93df99beb1cd7cad8a592b00a7b831a0b4e4757`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:40:20 GMT
ADD file:d73a77dc412cd093f533d8c6403c7a4a629d7a7d31b1ffc8555e0f7876d98ec3 in / 
# Wed, 21 Dec 2022 01:40:21 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 09:56:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 09:56:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 21 Dec 2022 09:56:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e5477ffb90e4da3fe8a2c9a63f402783b74fb55b190b59240e4d1d7e5b55a2da`  
		Last Modified: Wed, 21 Dec 2022 01:46:35 GMT  
		Size: 51.3 MB (51340127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f17da88d33e2a230fdf9667832a8cc65fca073921763a6ecc2a858766d4f937d`  
		Last Modified: Wed, 21 Dec 2022 10:02:31 GMT  
		Size: 9.2 MB (9186105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6731e431ea7ae865d881e1efe5608caa34a7813792150546854d8a8462ced5ba`  
		Last Modified: Wed, 21 Dec 2022 10:02:32 GMT  
		Size: 11.6 MB (11565473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92098526686d85ac9d57db5247ad423ae9f730e32f823f543af5aa6acda0cd34`  
		Last Modified: Wed, 21 Dec 2022 10:02:51 GMT  
		Size: 62.7 MB (62693784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:999a1a8a7983de5343333637880de9f1aed2dc96f530547624a68eec3b94fa0d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.9 MB (131896713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad1c98e2ed4dddf1500242d88ae48d3fa9bb7ed8b69deec8b9e69ccfc99f4b95`
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
# Tue, 06 Dec 2022 17:27:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:d37e22a8513c4ccf09821ec9d4887f64f4be99e05b4a5b5385317c5fa9ffba1e`  
		Last Modified: Tue, 06 Dec 2022 17:40:17 GMT  
		Size: 62.1 MB (62073819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:0b4a8f272e834650ce564ecce341cefbc7e5f286051e928829900fdc04d10d26
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.4 MB (142360227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a601486c50ae9dc30e5c9429ce3914b97cdfe0eb32ab07ad8652dff850232e4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:17:58 GMT
ADD file:4af1feaa33ee2a3c1112b5ed0efbcccec637c4dc23a5af7d55343f6ab7005920 in / 
# Wed, 21 Dec 2022 01:18:01 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 04:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 04:58:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 21 Dec 2022 04:59:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:47dc200f753ddc67a9fec80382c7c2b6f164cb907748c309862373fa8d94c504`  
		Last Modified: Wed, 21 Dec 2022 01:23:50 GMT  
		Size: 54.3 MB (54332986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39e0edfe8dd05f3e4610a7a82df7e8bb9b034431efe825b28230c1de8996756`  
		Last Modified: Wed, 21 Dec 2022 05:08:00 GMT  
		Size: 9.6 MB (9590429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8048f68261b2fdcd0cc93bbe51dd77df8e43b57c3da698cc1c679e192bf4360`  
		Last Modified: Wed, 21 Dec 2022 05:08:00 GMT  
		Size: 12.1 MB (12130299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8b620fb2afe77eb55ca3e3b2572b191e4b091a398d986bc7b4e5242e9e7dd48`  
		Last Modified: Wed, 21 Dec 2022 05:08:30 GMT  
		Size: 66.3 MB (66306513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:80fe5d929462fbcb8fb502564ba1c94f3a1fb305aff0e201341b695be50f3fd5
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.0 MB (122015209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3095c5914c0792da561d083de7026417fc5bec6e01a866d86b2f8f8d796eac27`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:39:40 GMT
ADD file:cff1e1a432929527e9bb64bde53e2b614c941bd4631b7bd3634fdda8a7240455 in / 
# Wed, 05 Oct 2022 00:39:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 02:26:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 02:27:16 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Oct 2022 02:31:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9cc6da93595cf4d9d589de999765cc4f1efa5e0d8e23ca6dd8b73b18afdc8189`  
		Last Modified: Wed, 05 Oct 2022 00:57:59 GMT  
		Size: 48.9 MB (48857821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:554ce58712f86101a4716baede25ee43c9c1fc550b39fb4b3e5fa1622fd3b00b`  
		Last Modified: Wed, 05 Oct 2022 03:30:22 GMT  
		Size: 8.4 MB (8388012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd132871253f925889ef836099addcf830644843a64a1529bddc510390846a9b`  
		Last Modified: Wed, 05 Oct 2022 03:30:22 GMT  
		Size: 10.8 MB (10750715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73bfc76b3f6f1ba447e697e6e2190cf70e757458cce81446b79426ae4cccdb03`  
		Last Modified: Wed, 05 Oct 2022 03:33:00 GMT  
		Size: 54.0 MB (54018661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:60c144048d64d5eb7336f71bb2f493a0196c2be2a88a552b536d4d38386910de
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.3 MB (128284398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f820eed7b7cc3c9dea72e25564b11b55a104eb89d52ef909ee5b0a38bfd112e6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:43:28 GMT
ADD file:880ff0ee3680abb7b9e72fb9457e71f7e35b2ef7a1d47d57ca68904588756f83 in / 
# Wed, 21 Dec 2022 01:43:32 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 05:32:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 05:32:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 21 Dec 2022 05:33:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9c9fbadd05736c9fdf511ecc5d2eec08182e6f9bb03d6f8f6e50bedf7a713181`  
		Last Modified: Wed, 21 Dec 2022 01:49:29 GMT  
		Size: 48.7 MB (48679509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:058df70186424378c385e8a8dde6736d86be892623a861bc219d0d0bf7bbcdcd`  
		Last Modified: Wed, 21 Dec 2022 05:42:09 GMT  
		Size: 8.6 MB (8644714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7ba6ecb7ed0072a0da77532fc6849229a054af60d61f10211a44454d4eb710c`  
		Last Modified: Wed, 21 Dec 2022 05:42:09 GMT  
		Size: 11.2 MB (11231271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7919d00635ff8b88b24be338278ef649b8b57436307979c87b00f4a665f9c8cd`  
		Last Modified: Wed, 21 Dec 2022 05:42:25 GMT  
		Size: 59.7 MB (59728904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
