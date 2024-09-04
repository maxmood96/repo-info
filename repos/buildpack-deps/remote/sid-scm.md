## `buildpack-deps:sid-scm`

```console
$ docker pull buildpack-deps@sha256:191444ba5df9c465ca2c88ca5f5713ac9257a06e3a3ac9e39f88c4e816e92e64
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
$ docker pull buildpack-deps@sha256:63de544b1b3076182a7318beb845687cf1f23c4364f80f3ab1cd0885717fb036
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.6 MB (139557538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21eb3bd4bced03aeba49c5f17f1064be0c947b26ecec58d34a96dd41ba71d41a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:21:13 GMT
ADD file:ec9b256ad5af9d6c88b912d94fd4e58256e2b29a1c5ff616fe47488c72c1256c in / 
# Tue, 13 Aug 2024 00:21:13 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:46:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 00:46:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:0ee0708ec9247cb19ad61d1bba3a89642d7eb4cfcd5031f23018c732b0ce201c`  
		Last Modified: Tue, 13 Aug 2024 00:25:12 GMT  
		Size: 52.8 MB (52836188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ba418b28cb46180ce179bf48a7dfa7135087eefa79b479acfa16fedb4e4a1c2`  
		Last Modified: Tue, 13 Aug 2024 00:51:48 GMT  
		Size: 20.5 MB (20482905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23a515568b5fe34e15585cdfd456e9acee67d565f25f2bfc42df67c7b99ed3f3`  
		Last Modified: Tue, 13 Aug 2024 00:52:04 GMT  
		Size: 66.2 MB (66238445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:ed6500bcaea8b4c9ef0e46757565bc33aa4560e04e9b55175c0f215c480362f8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.0 MB (133028559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30ab093fb96c9708f9b4d2373530572077367c2ba35bfc1989e780f50b8e07aa`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:56:10 GMT
ADD file:cf690ebeafabc8d93fcaa85c06bf4be7451eca6abfcd3d67e6a0b14ecae9eed6 in / 
# Tue, 13 Aug 2024 00:56:11 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:24:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:24:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:bf57c73982c97d1f73ecf70b56ea68e85c073b81e6abeed2594a6b283cfa2910`  
		Last Modified: Tue, 13 Aug 2024 01:00:06 GMT  
		Size: 49.8 MB (49825762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff530185f1ceb17692b30c50fb36e4c0f4d38b0de29fcfddff312093b1ae816`  
		Last Modified: Tue, 13 Aug 2024 01:31:57 GMT  
		Size: 19.5 MB (19485490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff253c8c9180c53a680ac594e0b90ace399416d9f322bef4f9a66e3d0fe0c5af`  
		Last Modified: Tue, 13 Aug 2024 01:32:17 GMT  
		Size: 63.7 MB (63717307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:dd02f67c9b41f5eef066888f8502d0cfb64fd912f1f4c68e8bfdcaec2ca826ec
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.3 MB (127295500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dc0c701118f3c89d3d996b299b666ba1270e433c445470539de019d604b60c6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:58:22 GMT
ADD file:e72a0297e96519fce159ae96a576801ad216aaabe4ba4c18342172c3277d4f63 in / 
# Tue, 13 Aug 2024 00:58:23 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:27:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:28:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5985c1abf8d738f84db0f982b117de5f003cae7137cf3fbeccf69d06419b0eb0`  
		Last Modified: Tue, 13 Aug 2024 01:02:30 GMT  
		Size: 47.3 MB (47328276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60e5fa1410d891dd62139493e077da1c08e4361f989c17ff8f13e730fab01e12`  
		Last Modified: Tue, 13 Aug 2024 01:34:27 GMT  
		Size: 18.8 MB (18827633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e6153d95b768925d58e3d7337d7c9e0c02e7e5fea16c6a628693281bbba4e7e`  
		Last Modified: Tue, 13 Aug 2024 01:34:45 GMT  
		Size: 61.1 MB (61139591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm64 variant v8

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

### `buildpack-deps:sid-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:01cdcc374f72d44626207be32c439902b464c3d3d658b27a0c29d7107189d7aa
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.3 MB (143268855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1b9cc4d75bad83ca4b442ce53584ba2058d9f735654e1925bd4e3b30136adf7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:39:51 GMT
ADD file:79c443f9d7d3c4ead1afa700b0409049a5e5def4db762097116c9f15a44a29ca in / 
# Tue, 13 Aug 2024 00:39:52 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:09:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:10:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:47aa20e0d3978e830fbdc52fb1b018e2dc37ff9f122461c55040f23300208844`  
		Last Modified: Tue, 13 Aug 2024 00:44:14 GMT  
		Size: 53.7 MB (53738474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce604b6ec46af20835c8de06fb56b6d31f8dce22f35194ea4cab29c2aac8c355`  
		Last Modified: Tue, 13 Aug 2024 01:16:14 GMT  
		Size: 21.5 MB (21505961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f51930d3a07571334ea27c6cab756bf536d9e8ac15d3dd0ba6ebcde49a8fe0`  
		Last Modified: Tue, 13 Aug 2024 01:16:36 GMT  
		Size: 68.0 MB (68024420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:0bbb7d3555c5e266def6f06d169472398be0bfe917c38b3861dc1d36d788c967
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137528902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c85203536db60a8c20cdb824e4db7bc726e1e864a68108be5e92465d9919731`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:14:27 GMT
ADD file:c2b8305463bd9ec2de5e34b309a574fda4d3201acf2be1eeaf77b17be497d769 in / 
# Tue, 13 Aug 2024 00:14:35 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:12:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:14:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:96d1cb60a321cb9bcad04942005c2d893de36bfa358a946f876b980ee7696e7a`  
		Last Modified: Tue, 13 Aug 2024 00:25:52 GMT  
		Size: 51.7 MB (51720781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00b7d979c2998ea5e70acbec3a94f9d7fa9dc5f798c6ed50c16c126082a82356`  
		Last Modified: Tue, 13 Aug 2024 01:37:39 GMT  
		Size: 20.8 MB (20809745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9b82974da5a3d69a6ca94388b0a3f14e1fe28ce4d21ef9f4032d841f5325b32`  
		Last Modified: Tue, 13 Aug 2024 01:38:31 GMT  
		Size: 65.0 MB (64998376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4340b676a86c741205c6828d4978c183a33ab7cd51f670f731933698f6a24e2e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.2 MB (151233149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:358365cff60f4d16d7e2fab1ad5aec512ecfbe089679bd2d3b779001ce4f541d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:23:11 GMT
ADD file:e6eea681cf56e20007639454c01cfebeefac45036637c0c5aa781f32e61086f3 in / 
# Tue, 13 Aug 2024 00:23:13 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:26:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:27:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:f94a26791ad674a64a864ec5ea20fbd30c5f7f3fa34d6b6d03306d943685df53`  
		Last Modified: Tue, 13 Aug 2024 00:28:16 GMT  
		Size: 56.7 MB (56729826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca71ec9e44bb7c30c2064fe97015df0afbf2b63ff8f9d8c898855ea953932aa1`  
		Last Modified: Tue, 13 Aug 2024 01:37:08 GMT  
		Size: 23.1 MB (23143887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a172a0ce16e36a34ff88a2732bbe6037759cb39c60616bd29dbc966d3bb79ec3`  
		Last Modified: Tue, 13 Aug 2024 01:37:28 GMT  
		Size: 71.4 MB (71359436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:d808e4fb51a4250cbbec7903e02191a5a2dd381efb4732ad482d925c7040387e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.6 MB (136574683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f1ceb124a6788428e56e67e12a903afcc6cd5bd4556302fd4f9b1c59eb48ffd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:11:01 GMT
ADD file:97cc40f71485a0c47367bf7de8cb1715072dce719d216195de9b049516a29e45 in / 
# Tue, 13 Aug 2024 00:11:03 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:37:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 00:40:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:e7e6753663bf71667278434bd9ec3bfbf244788b1855805c384ac83204bc13ef`  
		Last Modified: Tue, 13 Aug 2024 00:16:18 GMT  
		Size: 51.1 MB (51106160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b04e5a15fbe73c8e7dfa541c5d04c781d3c5c4ac6a9ce7895b41cfeb8e40e71`  
		Last Modified: Tue, 13 Aug 2024 00:47:07 GMT  
		Size: 20.0 MB (20012849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65deb42d9c749a528063c18ed3482c3235a8863523f7fc5d895330b910edd50a`  
		Last Modified: Tue, 13 Aug 2024 00:48:15 GMT  
		Size: 65.5 MB (65455674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:7cb088f2d9bfba6b06089622747309a8a3e0272d0daa567059097be31e6d8c85
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.3 MB (141312776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84af870be03c1edab12a17bc767ce71cf4be64f10112ebde559f5afdea8b9762`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:43:57 GMT
ADD file:b1f8fb7433720897f885f62e5bb1f6d60cfbf4392c753cd6772799dbe4712db3 in / 
# Tue, 13 Aug 2024 00:44:00 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:19:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:20:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:99d54a6f148f09f9af6f5923c0f9be21666ce72118617d82a7147f9b44fb20bd`  
		Last Modified: Tue, 13 Aug 2024 00:48:34 GMT  
		Size: 52.5 MB (52451278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af2c8424c4be16350c34c6e764d7f747d730b61b1e8a159beefb887a4aec6f4`  
		Last Modified: Tue, 13 Aug 2024 01:26:16 GMT  
		Size: 21.6 MB (21592255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c43737168f685110fa0a3c4ec68bd02aecf241fa770d30b263bb78a2ad0f70`  
		Last Modified: Tue, 13 Aug 2024 01:26:30 GMT  
		Size: 67.3 MB (67269243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
