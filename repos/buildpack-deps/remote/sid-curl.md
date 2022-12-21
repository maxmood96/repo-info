## `buildpack-deps:sid-curl`

```console
$ docker pull buildpack-deps@sha256:ba67adfd409d0138038fc714ef1f056cfb280e6b02b8d4b0fd73e043ce4b6517
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

### `buildpack-deps:sid-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:17ab6bb2384aaba213932006bec94568edd72ab9551ef9c342beaa52da639fca
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70667434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4e8ee89aefe9678466b90cec8b35111a795e70bc6bcf7f7f7ced3c7e44cc13b`
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

### `buildpack-deps:sid-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:148a92d755f7f2916b12481ee33c76abe877066c98369ff46aa9404ea559949b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68749112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7da17c9bfb743ffea00056057b843e8dab15f7bae84fca02936900e3ed3fcb32`
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

### `buildpack-deps:sid-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:723454462b46c3071a1b1083b87d93223575eaab12cf652689732b945739d0cf
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.8 MB (65840117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f836d491b8a43622e2ff201557e259d0f7890b28b053493563132a85418994de`
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

### `buildpack-deps:sid-curl` - linux; arm64 variant v8

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

### `buildpack-deps:sid-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:39688e5acae617a66aacac8b2c337df17081834d9766015d93e90d43ef79ead8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.1 MB (72091705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9cda77143d276c8089ad774d900671ffe8b5effc6bb0b67e9a95784bc53fe84`
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

### `buildpack-deps:sid-curl` - linux; mips64le

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

### `buildpack-deps:sid-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:ef9bdd4e7805981e28f314b3f1d6ab2368ca0b597854b299c641c02ca4e980b9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76053714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3938d40149accd7e13667d3ae5d8ab4273dfd296e8ad33ae93a974fe776a560d`
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

### `buildpack-deps:sid-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:497cc8982890eab597c6d34bdad7c65b903ffb329fc1dd479748adab4dcd7558
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65240087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acb5da4fd1d86a7ef3a37f0981a23b5ed7a1ac32ca8221d418dafceb3054feee`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:10:21 GMT
ADD file:ce5483e7a7d6e8eae2ec1f1c22390523d24dd0e613a20f8d424c81a1e12240ab in / 
# Wed, 21 Dec 2022 01:10:24 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:04:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:05:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:ec8e0a8db89be83ab5fa46e2a3ecb60ab7e5df3621c585c4ae748c563af17385`  
		Last Modified: Wed, 21 Dec 2022 01:26:34 GMT  
		Size: 46.5 MB (46453589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5f8c6e126b4271f9c21a1890d7345d3a741f26baa2d58b1c871c87435c0d4b8`  
		Last Modified: Wed, 21 Dec 2022 02:33:08 GMT  
		Size: 8.1 MB (8052896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b45d51aafdd462331d0b5b67c93150c348af9265261f8e51be63ebd57302f9d4`  
		Last Modified: Wed, 21 Dec 2022 02:33:09 GMT  
		Size: 10.7 MB (10733602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:4631dd9828a650c102acc2203dbf5be68e220c70687a21e933c1bf3add86fcd0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.6 MB (68555494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:041c161a14034a5d80cdaaa87eaca46c4e285153821b9f921dd9239b2769edab`
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
