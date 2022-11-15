## `buildpack-deps:testing-curl`

```console
$ docker pull buildpack-deps@sha256:07f064fcdd4cdfd43929180fe8679f1416569b8901fe1ae6110299227d39643a
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

### `buildpack-deps:testing-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:0e1ada6b7e93d3e1e78f748a46718c3cf9b3f7ae56fc982ae8dfcfe4e178074a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72288917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32d410c76dcf4a6bee4635384b965d4d33b4335b901e616ad70faecc7aedfb40`
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

### `buildpack-deps:testing-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:425efa0c6e88e4b9b33f158ae8d1e6b2f01c472bf26a22e3d7efc668f3b1ced0
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68763017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f99a41e9121b4cf98a9d22083053ab22eb76f5e92dc879d86a5571519d38580`
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

### `buildpack-deps:testing-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:c0e55d6ff12bef4f3084d35ac551c89ce3bde4e10dcccf4f8b1bec148e0f3ad6
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.4 MB (67363633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce258f1511aeb23b872bad65c8a06347b58915c7d93a87ff919291a4065bfe9e`
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

### `buildpack-deps:testing-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f5ef37ac55de039b76fcd658289dd943acc8f6b926babab0cfd34433e69dba15
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70535208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cccbbfc448205e1422d09340746f891db10f98d56d3e0ba20d88b39b88115982`
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

### `buildpack-deps:testing-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:167dce0d41220877a7d69d1e1e4402a1f7db01d68c2ede73609723628b0d8d40
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73649206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e11ce92eb7a28e68b38ee4db9094ad80ebf756d2c10f5310aacf4d6fe927bfc`
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

### `buildpack-deps:testing-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:a9ec86038bd70a78f5de7b698315ffdc3ad579e867c4874b12bc32f4813ca2be
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.4 MB (71405006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf273a19696b7bc943b4c5093d8172bb2986f3792b41e11da47dcb0379b2dd81`
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

### `buildpack-deps:testing-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:8e9cde9494655880ad5e98d1f19c1e7753f180d5e1350dc775dd60d8d1f98846
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.7 MB (77749055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3320b26d31e084b5b012dcb3b58bcd0cddfcb8d3c6ed8349cebe37bed468b61`
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

### `buildpack-deps:testing-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:894b1261a23e6de74babe1ee3f40ba9e50b5c66394124baddfddd8c053c67ccf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70091131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0d41791c8becaef1121c6430e271e2135e1dc7887ebe7a1da86fdacbd5a8eaa`
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
