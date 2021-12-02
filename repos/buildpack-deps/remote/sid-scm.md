## `buildpack-deps:sid-scm`

```console
$ docker pull buildpack-deps@sha256:a38439ae3b96e7fc5f52011e5767ef4400c4a5428a4e9790ce319bea94d3d51c
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
$ docker pull buildpack-deps@sha256:f28d2d6e1776233ab20d37c9192876ae2b354e6eb27b5e358eea942fdb4a3487
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.7 MB (128650506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce5180d8eb28afc4cb0431784c7876ee583d6a4b54ddd7803124e57b3c3b914f`
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
# Thu, 02 Dec 2021 03:43:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:b80321460c0114c02492753431792e6c46ac3fe9b80600356543e3068ed7a067`  
		Last Modified: Thu, 02 Dec 2021 03:52:14 GMT  
		Size: 56.7 MB (56722501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:1783730181df97e59f6d8c14c4276b564fa279a7cb98e0e5021369e5b757d2c5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.4 MB (123402292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7829c469a1887981bb88d9005cdec6b84bccabaf5e6dc2e698490175ca7aa080`
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
# Thu, 02 Dec 2021 03:48:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:ced16911b039c1097a2b138cf1e729c67a19c941b575a03dee7c08a1c42d3e6f`  
		Last Modified: Thu, 02 Dec 2021 04:05:17 GMT  
		Size: 54.4 MB (54384666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:503309f2088e071dc6e55fe3dcccb818c5409a06396d9a1b27e5cf40f6ac7a91
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.4 MB (118395575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9b1a9d4f39bd3aa441ab5035d64758f0d14f2cb21e097708974c7431baca348`
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
# Thu, 02 Dec 2021 11:46:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:80273a3f397b2e47f3a65064b16f0b619eb3a2129a44b15d1f347c8ef553ea1f`  
		Last Modified: Thu, 02 Dec 2021 12:06:43 GMT  
		Size: 52.2 MB (52247072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:8df6f829d575ea99e125de3bab577ba0eb4c40eb5783f7ff11b63021d6b8d1aa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.5 MB (127477324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93502622e130715c56843e16deee158d3a5afe736290c100469cfd11e343de15`
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
# Thu, 02 Dec 2021 09:56:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:8dc6e77d5f506109f0f5f6e4966ba727a7c3642b324c5949e1dfca891a40241f`  
		Last Modified: Thu, 02 Dec 2021 10:07:44 GMT  
		Size: 56.8 MB (56756677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:1d02882df3820d09283a729b38d8ae0d4682ec62fdd19537ec3f6cced97b426a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.6 MB (131641845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:374268d5a1c98546987f58c5ff168fe7be3e3eea1e2be170cbcccc6f2273ab29`
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
# Thu, 02 Dec 2021 03:15:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:a99c83bcfec09f5a8285a2c904ff5ebadbe779a1888d98acbc22ff42f814c916`  
		Last Modified: Thu, 02 Dec 2021 03:24:10 GMT  
		Size: 58.1 MB (58139010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:550260958aaef481861f912e39f70f7fdd1c1e7024e058fae634214c71f755ad
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.2 MB (126152857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c8612d7fdc52c7272cddbb0a536022d9e70fb09534335f4fabc83d266172e49`
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
# Thu, 02 Dec 2021 04:21:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:f11f0ae65985544fc4af9dfed32cf43717ac87519a70907b32399aa3b9bdc13c`  
		Last Modified: Thu, 02 Dec 2021 04:32:35 GMT  
		Size: 55.6 MB (55554324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:ce119a9ed018af6e2bbed0bfa383e0551dabd07b11666cd30af0ba0933b6f6c8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.6 MB (138632547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1b52653939a4f57e58d6c3936e632decc51270b79a642a6f46866e106822725`
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
# Thu, 02 Dec 2021 12:42:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:990ba6858763a274b899da9a34d5f84598bd4e6dd076b319a268ef7fd61d7416`  
		Last Modified: Thu, 02 Dec 2021 12:58:06 GMT  
		Size: 61.4 MB (61393717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:8963a3d61e4c3d8f556c008a03bedcef239cb984ed5d4cfe38da92e01d9a5ecc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.7 MB (119734335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46e04c96d11a2d683bfeff1e5e487338b2d884f84026a93a03bdae943cdb8907`
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
# Thu, 02 Dec 2021 04:03:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:7b46552026ea3fee87ea1959d63905f5dc028cccb4ee43e623210e771c78f3cf`  
		Last Modified: Thu, 02 Dec 2021 04:39:19 GMT  
		Size: 52.8 MB (52817111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b5eb954993cf4cf7fd4f07ab8117fc7256cfe77507f40663f2ca0d956632b30a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.2 MB (126201268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a749816435e3ba6a170811f05bfa277143fd297a7744a05cf4d0c92b75f923f`
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
# Thu, 02 Dec 2021 08:23:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:a04b67e4108109ff26fc4cf7e8e573f64288ed5b8e504ea90e52e1f48c7ed4ef`  
		Last Modified: Thu, 02 Dec 2021 08:30:17 GMT  
		Size: 56.1 MB (56095661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
