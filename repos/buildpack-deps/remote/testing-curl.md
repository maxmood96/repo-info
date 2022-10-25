## `buildpack-deps:testing-curl`

```console
$ docker pull buildpack-deps@sha256:819ba56ff1dff9a8893e39926e707c87a102f2a5b1243c8d05e720e365cc6922
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
$ docker pull buildpack-deps@sha256:20a4a8343b1da71a409f34e1f00df05ec1afb92deef31bf069ccfcba95ef865a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70284894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50b5509fe779851e321daf80c976e594a6bc3082ea32eb4bd672f0808170781a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 03:05:47 GMT
ADD file:226ff5e5e8066a03822e2865c6f72c554de94710c5664ee8bebd127d8aa32388 in / 
# Tue, 25 Oct 2022 03:05:48 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 06:08:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:08:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:cff7bd795d206b13b585de0da179a0c9616a5278eb7d74a97c97746085567403`  
		Last Modified: Tue, 25 Oct 2022 03:10:30 GMT  
		Size: 50.2 MB (50178371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40202823259eac4be0260092f1fb5f25fa9d866c32ec384dcadb0c7bb6bf8363`  
		Last Modified: Tue, 25 Oct 2022 06:17:42 GMT  
		Size: 8.6 MB (8599297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72794c6cd90917676f9d44ebd1f1f244c5564c41ea99e25ce09ad37df455551`  
		Last Modified: Tue, 25 Oct 2022 06:17:42 GMT  
		Size: 11.5 MB (11507226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:5b0dee0e2cc0e1938cf13bff64e7e8012209764899a65e170b1d0ebc91e645e3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68750987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d654a5ab6c7cd35f5bd3a5856e37d1f2b004dd7fd02791250fb62401d704090`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Oct 2022 23:57:54 GMT
ADD file:9f3a74b8856c0affe36dd4e0700a8a2686a9d2275934fd9af95135f13731d10e in / 
# Tue, 04 Oct 2022 23:57:54 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:29:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 00:29:13 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:b2ee1685df1bf13149eece9e0085c6befe355f21deeea69484a3ab1fab51e40c`  
		Last Modified: Wed, 05 Oct 2022 00:03:53 GMT  
		Size: 49.7 MB (49692608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:237b865ef48770b9d41964e18461ec2d393677f4fc653a0953e9f0b9773d47ac`  
		Last Modified: Wed, 05 Oct 2022 00:52:01 GMT  
		Size: 8.4 MB (8396889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:902b8eea02f53006b302a3dbae787275ce520ccf78df670e0dcafbfd1c4e17cd`  
		Last Modified: Wed, 05 Oct 2022 00:52:01 GMT  
		Size: 10.7 MB (10661490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:2ccd628358c05a1df1a611b3f2ddb74940265bbf961c494a44ad3dcdd8faf922
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.1 MB (72079033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bf40f5b1eb3957c789e1c4d10270c32dd0616f31b280461f8d4e00e823a5552`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:45:44 GMT
ADD file:83253dd857c3f1ea456b2b77494a2d865a467a36c188ecaeaf493faa5afb4c1c in / 
# Tue, 25 Oct 2022 05:45:44 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:56:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:56:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:bec7a4c1eec818efa32bedb19eba072edfb65db7384f73efc2a6ee7b13a3ca49`  
		Last Modified: Tue, 25 Oct 2022 05:48:08 GMT  
		Size: 51.3 MB (51263048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4dc154ad7b510114eae26976432c9de05c3e285368849cc3bf60481e326fa2`  
		Last Modified: Tue, 25 Oct 2022 08:29:25 GMT  
		Size: 9.0 MB (8982532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4415de5e6c24b057c96d4d8d3d21d5834d4e30729a87dda8eb4f92335d108f53`  
		Last Modified: Tue, 25 Oct 2022 08:29:25 GMT  
		Size: 11.8 MB (11833453 bytes)  
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
