## `buildpack-deps:unstable-curl`

```console
$ docker pull buildpack-deps@sha256:8aa56db946657721290274101860209691527ebcbfa9126490023e56e446ddf7
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
$ docker pull buildpack-deps@sha256:5497a5c8187de3c3de33113bc8024bd48685ab6cca6daf32eb5415e79393238e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71928005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b124b746c0c0275093fe4501e9c67464a413dcc951fc499fe7808faeb7a4f99`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 02:49:37 GMT
ADD file:aa0a8871e20fb4e68758bdebe7ee1e99e982c5e9d2e97b73575b8dcc2ab4adf8 in / 
# Thu, 02 Dec 2021 02:49:37 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:43:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:43:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:af46a953975205f2d7320842b5338767ad3d4aa084267279fc21cdc807374c52`  
		Last Modified: Thu, 02 Dec 2021 02:56:05 GMT  
		Size: 55.7 MB (55746868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:923af8c82d6eb6585aa625d753ea67606bccd40758565b49eb6e0636c4281a9a`  
		Last Modified: Thu, 02 Dec 2021 03:51:55 GMT  
		Size: 5.3 MB (5276824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c97b84d4ef8d40d6b16c75023fa3aa650861e59f1151d2ab44e9643bfa121be`  
		Last Modified: Thu, 02 Dec 2021 03:51:55 GMT  
		Size: 10.9 MB (10904313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:6b207aa33eb534d8fffe5e65a5268d4c08d6e58d13376d5e76371c47e151a1c0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (69017626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43071757ae58c014490249682962a4d7777efa95aaec0ba0a669549165a91c69`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 02:54:44 GMT
ADD file:358278336204ee1e51bf00f8c88d281c73e7e5d5b537fca1ddea89c9e69da90e in / 
# Thu, 02 Dec 2021 02:54:45 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:47:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:47:34 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:92d580f40fe8bf02becf360f6a4dc76454bfd66964c4acc0ddcd113fa0e9c2d1`  
		Last Modified: Thu, 02 Dec 2021 03:13:27 GMT  
		Size: 53.2 MB (53226256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638194516b96610900042221009a8c126b7644c26fe612397f2b2622bdfd03ac`  
		Last Modified: Thu, 02 Dec 2021 04:04:39 GMT  
		Size: 5.2 MB (5180320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23b2f3d24644f1e0eec33ec3662f820a19dc6b8cfa47e1f1551776f80f739780`  
		Last Modified: Thu, 02 Dec 2021 04:04:41 GMT  
		Size: 10.6 MB (10611050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:58d6ebc48938c932553bfa5409364ab35ffbc1967d5e2eb30ce13d259c056b1d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.1 MB (66148503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1585f316366beb9dd39ea6881588dedecdd23014e2e6142eb7d694994b10a440`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 09:08:50 GMT
ADD file:9740c987db5f6d577c2e2575a0974eb1a867a5c79cca1eb79e7c19d112bea4d3 in / 
# Thu, 02 Dec 2021 09:08:51 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 11:45:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:46:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:366f7fef67fd1fee5779f5f26a7bf655fe3e0243c51566b5fc28b209c153a87e`  
		Last Modified: Thu, 02 Dec 2021 09:25:38 GMT  
		Size: 50.9 MB (50857401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b63a2c21d88128fa3e4e629036fbd1d1d18eb72a94a41ffddfbc249ba7bfda70`  
		Last Modified: Thu, 02 Dec 2021 12:05:54 GMT  
		Size: 5.0 MB (5037501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf3c060d5561088295a9205a8a15042f3a66b6758e385cae2e07d3f2f5f58e49`  
		Last Modified: Thu, 02 Dec 2021 12:05:56 GMT  
		Size: 10.3 MB (10253601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:1118f5614644a0c71cfbc50a8d7af08c8d8a74a22c466b7fd8e70945a6165961
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70720647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc2078739f55f856293e569b0c60561e1691290c757829294f993ca622c9d6d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 08:09:29 GMT
ADD file:55fe3fd1ac33de3f564d68a8c2ecffd0191c93450cb0d4cb1ad737305962c5f9 in / 
# Thu, 02 Dec 2021 08:09:30 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 09:55:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 09:56:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:670b98b9b0d3937727686672aa7a6a70d1575086655d0ec9a8862c567ab8b29e`  
		Last Modified: Thu, 02 Dec 2021 08:43:17 GMT  
		Size: 54.8 MB (54776380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:422c039fac9ed6d1af02d09d0682a0b85305423b6ebdae379fd5a6e6cc3f9157`  
		Last Modified: Thu, 02 Dec 2021 10:07:25 GMT  
		Size: 5.3 MB (5263651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a872e69f11058da0fafb7717fed9273710562e91c5a2614cc6733d685cdd4e`  
		Last Modified: Thu, 02 Dec 2021 10:04:43 GMT  
		Size: 10.7 MB (10680616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:8f3b1bea8283de16803f56da8cf0200f1b06fe08141e8eb9d0fef85c6e21310d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.5 MB (73502835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7abe172e8f15c513dd7563e0b67b7580a83733bd68152fd93ed347eb50be16a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 02:41:35 GMT
ADD file:166234c060754022c10737b949088caccb46aa6315aa91f9ff63dd1f60704729 in / 
# Thu, 02 Dec 2021 02:41:35 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:14:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:14:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:158718d3425b2eb9ceb4c5321a7633c30d7b948b7dfe2a98608b354788b1c2ab`  
		Last Modified: Thu, 02 Dec 2021 02:51:07 GMT  
		Size: 56.8 MB (56808054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fe1b108338e18a41ef0392f3153179fc4c7809ae0d46bd4c0ad04d928fa2ca`  
		Last Modified: Thu, 02 Dec 2021 03:23:43 GMT  
		Size: 5.4 MB (5408797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:360266616da2d6b21d216fa2104faaa2528b4c353538e2fc67ab8b0942e7f3fc`  
		Last Modified: Thu, 02 Dec 2021 03:23:44 GMT  
		Size: 11.3 MB (11285984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:2ddb6d4de48bfb58a9788724b6c91ad878b576ffdf7ec7578dfdca2347874ee8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70598533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6be14f7f4952f62773639e0a5f1e38276c775f4066645b7bd741e5799d1725f2`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 03:11:25 GMT
ADD file:756c847932d446a78e78b1785e3773acc2f468bed861faa53b3a777f03b1273d in / 
# Thu, 02 Dec 2021 03:11:26 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 04:19:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 04:20:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:851a637e7cfa078b1e4bcb2543d21b6bd9e139295986a256dac39682452e1a34`  
		Last Modified: Thu, 02 Dec 2021 03:48:41 GMT  
		Size: 54.5 MB (54455441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ed4124392ca3477be2c7aafcf44d0c7a1c0ac313b6aa4db5e42c0fd0d27038`  
		Last Modified: Thu, 02 Dec 2021 04:31:41 GMT  
		Size: 5.2 MB (5235788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d46352d707f92ef2034e26342ca34e8d34141a50bef2663631e66049929929`  
		Last Modified: Thu, 02 Dec 2021 04:31:45 GMT  
		Size: 10.9 MB (10907304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:6bc439b50a6635216b0d7d24a0416ef6ebf72bce3c177de8e157744fac45b976
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.2 MB (77238830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac3a814b9414858de639e53830841a6a7be1fc4e57bc380ac884490a7e378e42`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 07:23:26 GMT
ADD file:0ba5425cea9bcdb1fac898f3ddd38f4505205a5b32c1288a9a4ecece03ec10a1 in / 
# Thu, 02 Dec 2021 07:23:34 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 12:38:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 12:39:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:b9442172998188c0fffb75559bba82a9436fd970dbf2b25460afc71f86479c20`  
		Last Modified: Thu, 02 Dec 2021 07:33:54 GMT  
		Size: 60.0 MB (60041316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f5b299250e1b93acaab942bfa0d27e9d3870773ddfc17e10df4fd3d31f96f82`  
		Last Modified: Thu, 02 Dec 2021 12:57:42 GMT  
		Size: 5.5 MB (5538234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3154daa6ac50e0863a376a29692bd68a0e9a4a87862f71434ccc121a401f7b8c`  
		Last Modified: Thu, 02 Dec 2021 12:57:42 GMT  
		Size: 11.7 MB (11659280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:b8766ac83de9214e56be0de79150e874f989b94f86710ccd092db997076b0130
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.9 MB (66917224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2dc1dc067727e389dd30fbb51f7bde517f5f47e9f294494346026297a2442d4`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 03:16:27 GMT
ADD file:2408c0186c2415b201c5fb609f218da02da0aec9aff7f9467433a1bcbdeb0da9 in / 
# Thu, 02 Dec 2021 03:16:29 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:58:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:59:58 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:6a1cc4c4003753c168cfc12397594854587c6645c5f03e57779bd85f43632403`  
		Last Modified: Thu, 02 Dec 2021 03:32:36 GMT  
		Size: 51.5 MB (51509234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0400a63f68eccacb4581e73d2e13a149f13d2f96ede6f9a5041b48108f8267a`  
		Last Modified: Thu, 02 Dec 2021 04:37:08 GMT  
		Size: 5.1 MB (5089467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8536bb4db4e00844c1bdf6f562fd2fb2840423d4d90c98e791568915c641acf0`  
		Last Modified: Thu, 02 Dec 2021 04:37:11 GMT  
		Size: 10.3 MB (10318523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:9ed5c346c469ee3317e99814158b8372ca121e0efc6577630e4b1aecc75243e3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70105607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adb3146ef596b8c71f68c9cc26d7a26ac08d9c6903e989be3ac22c8dfcdf5e41`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 07:20:26 GMT
ADD file:d7694f1f6512fdbbb5735764707de9bd26f8f25119496509ff4d721f4776e1ce in / 
# Thu, 02 Dec 2021 07:20:29 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 08:23:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 08:23:13 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:3a71993c832edfb3256a0ce6f0d3fee82664f911373efacb0b2509901e613ab5`  
		Last Modified: Thu, 02 Dec 2021 07:26:28 GMT  
		Size: 54.1 MB (54051648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5059d18cc4add6886867dd20f08845df69f87db81dddd4aed5bbee167d1fcac3`  
		Last Modified: Thu, 02 Dec 2021 08:29:57 GMT  
		Size: 5.3 MB (5256958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:049ab954cc89b359baaed86b422549b3e98ca5da0abe2643498c79abc91f1ab0`  
		Last Modified: Thu, 02 Dec 2021 08:29:58 GMT  
		Size: 10.8 MB (10797001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
