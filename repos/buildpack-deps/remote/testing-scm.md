## `buildpack-deps:testing-scm`

```console
$ docker pull buildpack-deps@sha256:99781ec51c6ed647c425c9e10bf2db2102d6690c1ef8620b6ca2816cd54efb44
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
$ docker pull buildpack-deps@sha256:c0889aaa28d64a6b4800c6b3a31cd0b71d895768764afb3634e32c52ac1622d6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.4 MB (129411855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d09023ab2838b3cc0787375811bd30168a7d546949b877c8c032479a18c50775`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:22 GMT
ADD file:3b158c11a921c91aa3cebf5651e59c21fe59da295d3edc56147fefaa760329ff in / 
# Tue, 25 Oct 2022 01:43:23 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 09:21:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 09:21:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 25 Oct 2022 09:21:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3721e3e259583b8b78cfdeb51a553c189938925b902bceaa1f4f92e837fb9a23`  
		Last Modified: Tue, 25 Oct 2022 01:46:52 GMT  
		Size: 51.3 MB (51261783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71496268904f3a840d9bce0c685a75189d26a0bc17e7e433cb15e8591db71c94`  
		Last Modified: Tue, 25 Oct 2022 09:46:30 GMT  
		Size: 9.2 MB (9150622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6dabb627a933a05d9921efa339a1a23fb1601652ed637def09b8afb87cfde62`  
		Last Modified: Tue, 25 Oct 2022 09:46:31 GMT  
		Size: 11.9 MB (11876512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a1e1b526d184c32611382431c10f26791b2bc6d4785b7447b03ea96bc5e4104`  
		Last Modified: Tue, 25 Oct 2022 09:46:48 GMT  
		Size: 57.1 MB (57122938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:79ba49fdff89658bc634a23986e1ab9b110161365b07da586b51e6821667febb
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.7 MB (123725485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:651e64b63c1ed99939727ef75a475df40f1f5e0e275a1d7f8698ccdecfca7c4b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 01:48:32 GMT
ADD file:f5954c36a3601d3dcf67f8701fe7691c7a94bc36e88827c06ff7338a52d56c5f in / 
# Tue, 15 Nov 2022 01:48:34 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 05:38:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 05:39:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 15 Nov 2022 05:39:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:34757784ba8ccecfd4a2f549aff99cd98b7b291a61176def51827463bc77aa00`  
		Last Modified: Tue, 15 Nov 2022 01:53:14 GMT  
		Size: 49.3 MB (49265841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf55f2cf20315f11c0568b2c8e64fa08c08d44cd3c2ed5e281caebe13320c93c`  
		Last Modified: Tue, 15 Nov 2022 05:47:05 GMT  
		Size: 8.5 MB (8471441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9889ed4552e2f48445b3ae801a3f6bf662eac23614471014335840669c23ecf4`  
		Last Modified: Tue, 15 Nov 2022 05:47:06 GMT  
		Size: 11.0 MB (11025735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fdcd3cad57bb08b27e14dae1282646677672ad58c572057c39db8a0145596cb`  
		Last Modified: Tue, 15 Nov 2022 05:47:27 GMT  
		Size: 55.0 MB (54962468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:3b2359fa51e036a202bf9a75c2853877177d1f607603a73d6cadad0660a2d175
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 MB (120290039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2952dc0ab532177d524031719d0120dcb0e1491911f7d839cd79b56f1a9b0559`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 03:13:33 GMT
ADD file:5ab258b263409915dc783ead8a52ab1b91eb5dce1d1cfcadf9234ce60b961a00 in / 
# Tue, 25 Oct 2022 03:13:34 GMT
CMD ["bash"]
# Wed, 26 Oct 2022 04:33:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 04:33:40 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Oct 2022 04:34:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ea7580981dc6864bb654386e5ab137ff58cf1c1fc085457388952e4e7debac2c`  
		Last Modified: Tue, 25 Oct 2022 03:19:57 GMT  
		Size: 48.0 MB (47997492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acde535f4658ea997cbde733049d0a00b7e82e5f6a962d0d1de3f1a116380132`  
		Last Modified: Wed, 26 Oct 2022 05:09:24 GMT  
		Size: 8.3 MB (8253904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca86f9f1211aef6c21c8a62231a8b5899fe833387fbe61627b3d02e09c96826a`  
		Last Modified: Wed, 26 Oct 2022 05:09:24 GMT  
		Size: 11.1 MB (11112237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aff7ddd1797a39eeecaf41a28524e1f9a11aa19eb63b812371874360fdeee6f1`  
		Last Modified: Wed, 26 Oct 2022 05:09:46 GMT  
		Size: 52.9 MB (52926406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:bb7b1e35160737723d163a99c003b59c2f829df25dd8ce16e4a04ecf16969154
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127671759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2cdcef9cf554205f99a89b7054cbee1755e206d93e3ecd6482d0b5ceff7f61e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 01:40:57 GMT
ADD file:c622ea356e69bcfb00a0066c22b326eaa514f83ce688202c38b1cdf4e279f65f in / 
# Tue, 15 Nov 2022 01:40:58 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 05:34:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 05:34:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 15 Nov 2022 05:34:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d350c5c763d25fc284c82bdb22268efbb6376d35695fb6f09eef45b2f3dcbd9b`  
		Last Modified: Tue, 15 Nov 2022 01:43:42 GMT  
		Size: 50.4 MB (50353304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4219db6fe10658758cac25d3b75b8bfe44e9f64cd8b62b849437a2f61ea784f`  
		Last Modified: Tue, 15 Nov 2022 05:42:02 GMT  
		Size: 8.8 MB (8849933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10467211889673d69095f8078d54c47f3389e981ca843f1ce2131cd7bd39933f`  
		Last Modified: Tue, 15 Nov 2022 05:42:02 GMT  
		Size: 11.3 MB (11331971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:897f80388d4dcc10c369e14cd3fa87e7c5f8d619f9cbb7535d440efa4956b36d`  
		Last Modified: Tue, 15 Nov 2022 05:42:18 GMT  
		Size: 57.1 MB (57136551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:bb8f335fbccf0d2040d44a9901f5d5892fddf6faf56f84c2699db34d21e91570
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.3 MB (132265500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:533c3f4baead23baa420e1ab640834843dc1a50aec17fc4a2c085177b12d89ce`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 02:21:54 GMT
ADD file:f47fc1d53965bb08e38b482e78bd79e3cbeecc53e586ffd88bff0e6fed0a1f3c in / 
# Tue, 25 Oct 2022 02:21:55 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 05:12:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 05:12:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 25 Oct 2022 05:13:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:11f88873ba86e184f57ba78457d36c4f22e16eaffb9c293964adc7905e18bfe5`  
		Last Modified: Tue, 25 Oct 2022 02:27:09 GMT  
		Size: 52.2 MB (52224672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:683bf09527f61248ec1a0fa70be7388069c28d961ae31bd3a05c43ae41192a7a`  
		Last Modified: Tue, 25 Oct 2022 05:26:29 GMT  
		Size: 9.3 MB (9330348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:823ddfa7a0daf2e9e0c4b6ce038b2e2cce83bde4ba9aef56fb6911d8241ca03d`  
		Last Modified: Tue, 25 Oct 2022 05:26:29 GMT  
		Size: 12.1 MB (12094186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f47813fb488b28b2af09c6f4d188832f52b886546c7885a3bb2d1b67b0d69be`  
		Last Modified: Tue, 25 Oct 2022 05:26:48 GMT  
		Size: 58.6 MB (58616294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:f363c8e80be30cbe44ee66eb3eb3dfa50dc8ca9f177ab6f11f5c0acb74d610b3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127361128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4639c4ad46fd8d15598da4c49f5ffabdcd24e414cb66feb5d5c5a679a5dd0166`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 04:37:41 GMT
ADD file:a1c9e78f0a426fb245eff7a26706bf5500c9afba4a267812a4b2ec71113c371c in / 
# Tue, 25 Oct 2022 04:37:46 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 09:20:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 09:21:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 25 Oct 2022 09:23:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:132042cf7d4760fcfc85f263dd04337e03e7c8105a5e98f7b530ac7170f31a8e`  
		Last Modified: Tue, 25 Oct 2022 04:45:25 GMT  
		Size: 51.3 MB (51259641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d69a1dd49e6ce17928ad491f90ab6ce7d931f9c5e5a417a0d9fb3f1ce72b8b06`  
		Last Modified: Tue, 25 Oct 2022 09:48:41 GMT  
		Size: 8.5 MB (8513255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff5ed8c26291706609a5805858b3aef9cd315c13a4d16d8fb8a664ca1d3a86d`  
		Last Modified: Tue, 25 Oct 2022 09:48:41 GMT  
		Size: 11.6 MB (11632110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1d9c909aca86b92807e96dc4b657562ad939143011fac9714484bea28dd5c02`  
		Last Modified: Tue, 25 Oct 2022 09:49:31 GMT  
		Size: 56.0 MB (55956122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:8aedd3f69ab37457552ec526445326e02d180a5e2d4fcd5e9921b0acccee7f55
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.6 MB (139648414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06e4d95381966110ef09af6732f8433a26f7b8e7f0895481c387ea2612e84de8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 03:12:50 GMT
ADD file:1f55ca9aa64d69398e6bff99fdfd63dbf022ecefc46450a6fd32ae46e9718557 in / 
# Tue, 25 Oct 2022 03:12:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 06:09:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:09:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 25 Oct 2022 06:10:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:264fa02db63011b604885c7feecaeb78fbee4ce4d8191fa5050f4fef88c74001`  
		Last Modified: Tue, 25 Oct 2022 03:18:00 GMT  
		Size: 55.3 MB (55338800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f1baf225de572024a1c39187c5ece555fd8056d94bb80d56f889f4e825aa70b`  
		Last Modified: Tue, 25 Oct 2022 06:47:11 GMT  
		Size: 9.7 MB (9732694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c55c6a98be02e0940d4fe69cf5b8ef19e3e86304cda7170f1dd085e4a01338a2`  
		Last Modified: Tue, 25 Oct 2022 06:47:11 GMT  
		Size: 12.7 MB (12677561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e65982f752eb81f7771ff52e7dc61db3a43a5e7b89882ff7934a391492daaae`  
		Last Modified: Tue, 25 Oct 2022 06:47:45 GMT  
		Size: 61.9 MB (61899359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:221812309a8315f40e7a00439dfae7b687e3828c543190683390eec5bc6263dd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.5 MB (126484316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c27b9f13f925e68613971e6806d863cbc335c648a119e6ce33664f7874816557`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:13:56 GMT
ADD file:92a462945d4b32c30f41478992b9ab30d452ac37b0ecef64e2325e4e99296ea8 in / 
# Tue, 25 Oct 2022 01:13:58 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:29:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 02:29:40 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 25 Oct 2022 02:30:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e544dc28605cf962b36f5ba4703f824c022460d64f8973e49764cd76163df5ff`  
		Last Modified: Tue, 25 Oct 2022 01:18:08 GMT  
		Size: 49.6 MB (49578501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50715b09b75ed5a3b59f5532be8529ac130746e899c823894a3ee91fc976a5ed`  
		Last Modified: Tue, 25 Oct 2022 02:48:44 GMT  
		Size: 8.8 MB (8785586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09bb8ed5a6b2d134cb7b866721196b0adaa54ab94d27c13c65773f16fffc143d`  
		Last Modified: Tue, 25 Oct 2022 02:48:44 GMT  
		Size: 11.7 MB (11727044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094b78b28a264fd0d8e36e29b1b3e4c349049eedd6af26957228a4bb291b7f90`  
		Last Modified: Tue, 25 Oct 2022 02:48:58 GMT  
		Size: 56.4 MB (56393185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
