<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `neurodebian`

-	[`neurodebian:bookworm`](#neurodebianbookworm)
-	[`neurodebian:bookworm-non-free`](#neurodebianbookworm-non-free)
-	[`neurodebian:bullseye`](#neurodebianbullseye)
-	[`neurodebian:bullseye-non-free`](#neurodebianbullseye-non-free)
-	[`neurodebian:forky`](#neurodebianforky)
-	[`neurodebian:forky-non-free`](#neurodebianforky-non-free)
-	[`neurodebian:jammy`](#neurodebianjammy)
-	[`neurodebian:jammy-non-free`](#neurodebianjammy-non-free)
-	[`neurodebian:latest`](#neurodebianlatest)
-	[`neurodebian:nd`](#neurodebiannd)
-	[`neurodebian:nd-non-free`](#neurodebiannd-non-free)
-	[`neurodebian:nd110`](#neurodebiannd110)
-	[`neurodebian:nd110-non-free`](#neurodebiannd110-non-free)
-	[`neurodebian:nd120`](#neurodebiannd120)
-	[`neurodebian:nd120-non-free`](#neurodebiannd120-non-free)
-	[`neurodebian:nd130`](#neurodebiannd130)
-	[`neurodebian:nd130-non-free`](#neurodebiannd130-non-free)
-	[`neurodebian:nd140`](#neurodebiannd140)
-	[`neurodebian:nd140-non-free`](#neurodebiannd140-non-free)
-	[`neurodebian:nd22.04`](#neurodebiannd2204)
-	[`neurodebian:nd22.04-non-free`](#neurodebiannd2204-non-free)
-	[`neurodebian:nd24.04`](#neurodebiannd2404)
-	[`neurodebian:nd24.04-non-free`](#neurodebiannd2404-non-free)
-	[`neurodebian:nd25.04`](#neurodebiannd2504)
-	[`neurodebian:nd25.04-non-free`](#neurodebiannd2504-non-free)
-	[`neurodebian:noble`](#neurodebiannoble)
-	[`neurodebian:noble-non-free`](#neurodebiannoble-non-free)
-	[`neurodebian:non-free`](#neurodebiannon-free)
-	[`neurodebian:plucky`](#neurodebianplucky)
-	[`neurodebian:plucky-non-free`](#neurodebianplucky-non-free)
-	[`neurodebian:sid`](#neurodebiansid)
-	[`neurodebian:sid-non-free`](#neurodebiansid-non-free)
-	[`neurodebian:trixie`](#neurodebiantrixie)
-	[`neurodebian:trixie-non-free`](#neurodebiantrixie-non-free)

## `neurodebian:bookworm`

```console
$ docker pull neurodebian@sha256:3781817d913ee5d56f77887c10cc8cf42516c30683672a6ea4f7a8b432d2b0c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:bookworm` - linux; amd64

```console
$ docker pull neurodebian@sha256:05aea33b07313b18ed01de4ab2ae06ed9b2d546335a1f9327c0bc995e5b83a64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59845703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7dfc8a55839663157a6aba43127208ac15cfb53aebb47042d2903aae22db74b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c6b11972fd12973831818babf60f1ffc1c4047507943d132dffc612884022858`  
		Last Modified: Mon, 29 Sep 2025 23:34:14 GMT  
		Size: 48.5 MB (48480557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e22dfc9371bd5451b52aa68b5daf06dfef29d6542df8b0fe5b7d20e9433b477`  
		Last Modified: Tue, 30 Sep 2025 00:16:14 GMT  
		Size: 11.3 MB (11269611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bbdeeebd686778d37b510ade531322cd97c929d72c59f001b9c8fb1f3d73c24`  
		Last Modified: Tue, 30 Sep 2025 00:16:13 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d874806bdf8c980e824c490f339970b81ff02843afe86de3cdbfdd45425b58fa`  
		Last Modified: Tue, 30 Sep 2025 00:16:14 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2a9e79214196194656296b10f16d9dc952464f9530672c37a1581933dc0d57`  
		Last Modified: Tue, 30 Sep 2025 00:16:14 GMT  
		Size: 93.4 KB (93363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6675649918c8891c0b7dd5b1384c9e7658e704541ed2c3f724b71056993a5271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd658c8e894a97cbf19d656d7b994f751ed624b572d963d9854cc18104f4b05e`

```dockerfile
```

-	Layers:
	-	`sha256:3fa0b54726e2c21f1537172fccbf34d53eadede1db4a89b9b838c78e1c33fd46`  
		Last Modified: Tue, 30 Sep 2025 22:07:23 GMT  
		Size: 4.1 MB (4075236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac555dc0da90f76cefef7f44c9e57d8d91f1ec3f36cba41b730becebeeeb0447`  
		Last Modified: Tue, 30 Sep 2025 22:07:24 GMT  
		Size: 14.0 KB (14008 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:885d0432b840a960d2af3a81ca5aae885bf5af08cd61088845e8b8dee0794d04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59708030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95661854959d110a69764b3cc43078b7ea99cf1b5597dbd1d96e37078f5d0c25`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f7b43f0d0a8b99591b27457b368e70a582002600d32503fd07798c1bee7cd134`  
		Last Modified: Mon, 29 Sep 2025 23:34:16 GMT  
		Size: 48.4 MB (48358915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59ee3668b41e5cd78c1271f8a55ff6c7f79be607b3881f0e810b053d2a59879`  
		Last Modified: Tue, 30 Sep 2025 00:19:38 GMT  
		Size: 11.3 MB (11253411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e21facce03c416f6b6b038ea1567e13187e8f88f83543487d66645815aa592c`  
		Last Modified: Tue, 30 Sep 2025 00:19:34 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a91a5654acaa81767b1cb906ed6e1b298ed98d03e537ce98a6a02c7ccae2647`  
		Last Modified: Tue, 30 Sep 2025 00:19:35 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:005232c823dc70fa622ff0308fa6bb27a5669e98a6559e582866767a89e77b59`  
		Last Modified: Tue, 30 Sep 2025 00:19:36 GMT  
		Size: 93.5 KB (93533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:cf061e895233b68256d177410cbec7182e037423d8bf0f05cf3b93926d77dd51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac60b8863cafd48c3cb4e1c0a16d6b174a586477c25b7b152c934539e292e41c`

```dockerfile
```

-	Layers:
	-	`sha256:e2002f290029233141183075e6c0fc0da5834fced553d054504439a296895855`  
		Last Modified: Tue, 30 Sep 2025 13:07:27 GMT  
		Size: 4.1 MB (4075478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82755eaef9819ef6f197394d209dcb151e24a5f15bc29628c34abd4fbcf1e4da`  
		Last Modified: Tue, 30 Sep 2025 13:07:27 GMT  
		Size: 14.1 KB (14133 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; 386

```console
$ docker pull neurodebian@sha256:d91e3880a0b832816150a13ad8aa9d5416a824b9da76477c9d2e8d9f32196349
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61252347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acddad54a54afb1f7a64db74d90ee9619a6f00598c1138fb05a3f4fc215d15a8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2212ccc79525753c3f36994bd936e194dcec09d69b21786be4caa60f697693d8`  
		Last Modified: Mon, 29 Sep 2025 23:34:26 GMT  
		Size: 49.5 MB (49466651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0fcf493e69eb4a8834c6f5d1209b483a9fa5de2fea0f19cdfc81de3c993f8a8`  
		Last Modified: Tue, 30 Sep 2025 20:21:23 GMT  
		Size: 11.7 MB (11690118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39be09859d19045ac15d7973f5449ba6128d3d33572d45507258428bf2566fbc`  
		Last Modified: Tue, 30 Sep 2025 01:17:21 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d33ed3c56380c617c61fc605987c9f6777075d5c303725f30d16f583b3c585`  
		Last Modified: Tue, 30 Sep 2025 01:17:20 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1419c195a2730d5dd40aab25b98cc1613239f1eeba9b4caa91a54e65104fcd03`  
		Last Modified: Tue, 30 Sep 2025 01:17:21 GMT  
		Size: 93.4 KB (93405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:919fbfc5f19953bad4e8d0116debfc9cee19d0a5bc03352cc45ae2fb1b96c479
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4087184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3b4ed69573c34fa3235d349ff3ff520ada93cb39f70becc9e250b577e319c58`

```dockerfile
```

-	Layers:
	-	`sha256:2f7f73fd5ce5669e280c57dbf3cdcf3992d91ca2d295130f6d7ef2d4f7c7765e`  
		Last Modified: Tue, 30 Sep 2025 16:07:26 GMT  
		Size: 4.1 MB (4073204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2806288d1c706feaca2efff856a8e800bed8536a2032d8951927220f8af4de8d`  
		Last Modified: Tue, 30 Sep 2025 16:07:27 GMT  
		Size: 14.0 KB (13980 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bookworm-non-free`

```console
$ docker pull neurodebian@sha256:d862dd1dc8d155384376cced3c739f8342968dec401b3ebdadbbf3371e2f3e84
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:bookworm-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:22518b5f38f00c2114e97b3187d585db438685a05930a18785e5b3adb73f6a1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59846138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55c97b3032259eac465ebf0c8ffe17b7906d09a91ee3ea949fd9dded523db104`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:c6b11972fd12973831818babf60f1ffc1c4047507943d132dffc612884022858`  
		Last Modified: Mon, 29 Sep 2025 23:34:14 GMT  
		Size: 48.5 MB (48480557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eedb6694c64cae843951d54e2b05e2610566e3fca8973c074796b9af8a498c77`  
		Last Modified: Tue, 30 Sep 2025 00:16:13 GMT  
		Size: 11.3 MB (11269576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e794520964c3a381276cce16943b4362333efd5977a64c5fbf154c77b6015c2`  
		Last Modified: Tue, 30 Sep 2025 00:16:13 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04fc78f7af59fd7cb66064d2b76dac7beff22e85aa7dccb731fa985ed7217c7a`  
		Last Modified: Tue, 30 Sep 2025 00:16:12 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7265c0ebb450e80f788f289e5b00ec5e5704aea9278a33f4c5ed429a4c20df73`  
		Last Modified: Tue, 30 Sep 2025 00:16:13 GMT  
		Size: 93.4 KB (93384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2065cea84fab934fcd1190024d9ddaba19177d1f00876c2ebb45a42ae19c4e22`  
		Last Modified: Tue, 30 Sep 2025 00:16:13 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f8b4ff6a2b23ebfcd87f18355293fc60648ca9af372ce29c6507b0427f7ac9cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4091307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ebf7e694489c6fbe6ffde1e32ef3bb99627d8f861c8bda8b0918f984935bb86`

```dockerfile
```

-	Layers:
	-	`sha256:b614fb6a5adfe55efbafba13c46d348a4d8670764d9d9a5ea0205ca21574afd4`  
		Last Modified: Tue, 30 Sep 2025 22:07:28 GMT  
		Size: 4.1 MB (4075272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c25191c38856398fb7ad3b288b257d6f3e09f8978cd82e718e4dd7a99c56489`  
		Last Modified: Tue, 30 Sep 2025 22:07:29 GMT  
		Size: 16.0 KB (16035 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:14c6af47ab2eb20d548a33b4950a8064cadf5103151dbde85721d736f7952549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59708446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:770036e294af01f132221eff46d03aeb9fd3ab8e68aedf7708ed786da2cebceb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:f7b43f0d0a8b99591b27457b368e70a582002600d32503fd07798c1bee7cd134`  
		Last Modified: Mon, 29 Sep 2025 23:34:16 GMT  
		Size: 48.4 MB (48358915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3898d44334f1abae852d530a5cade80ec1ebb870e449f5b99d9f961a5315a02`  
		Last Modified: Tue, 30 Sep 2025 00:19:22 GMT  
		Size: 11.3 MB (11253407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb9ea5bcd6e7676c1d1f0aa5b1f1be9505c317be092c246d08ef9e756cbfcbc`  
		Last Modified: Tue, 30 Sep 2025 00:19:20 GMT  
		Size: 1.9 KB (1897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ff8510b562165af3eb589e1fafdc7f2085c9e55c53a0d8875f05a9001553bf`  
		Last Modified: Tue, 30 Sep 2025 00:19:21 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b122a4615dd127bcc9eda078ce123a341c4fc07f38436b92fe87e539ecaa528`  
		Last Modified: Tue, 30 Sep 2025 00:19:20 GMT  
		Size: 93.5 KB (93508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a496b42997f524257237886d80a6f9fd59724b091a359ed42eb3d1f81b79ea2c`  
		Last Modified: Tue, 30 Sep 2025 00:19:21 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c13213fed3c5367640f48587d9c907be8453bb8585766bf1f5031f2d0df72438
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4091689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e6466a096093118b0e12f98547696e397648ac394f697616c6ccdf2feb87515`

```dockerfile
```

-	Layers:
	-	`sha256:03f9b0f7f7c935c94de22d574f043cc96ee44e8f1f089633c7290bacd55b2cae`  
		Last Modified: Wed, 01 Oct 2025 13:07:21 GMT  
		Size: 4.1 MB (4075514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee16f24e2006c7d9bf4faa0d7e58ef704cc6e5c6fad6790fb38d2403ecc35c06`  
		Last Modified: Wed, 01 Oct 2025 13:07:22 GMT  
		Size: 16.2 KB (16175 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:274603d10dd008ffaae3f5a404c2cb78e59ecd5706eb12e88af53bf598a57867
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61252715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fe2e21fcc30f1784d46cc228997afb47e22ffedd4a368dfcf05b81367454dfc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:2212ccc79525753c3f36994bd936e194dcec09d69b21786be4caa60f697693d8`  
		Last Modified: Mon, 29 Sep 2025 23:34:26 GMT  
		Size: 49.5 MB (49466651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8003e96b9e94adb93fc76f0aba6b61a61d93076bed93f875ac3df4c3b0774a6e`  
		Last Modified: Tue, 30 Sep 2025 00:46:13 GMT  
		Size: 11.7 MB (11690057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f40fff84c9df9d31e2e7597437f764b596d6d5cc1c91b257231aea263e70a9`  
		Last Modified: Tue, 30 Sep 2025 00:46:07 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a8e013318eab027adcaa49bd9383346d072bc458f9f83465706840e91c6917`  
		Last Modified: Tue, 30 Sep 2025 00:46:08 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66354afb13fc7968d1d014d293a2852ad99c3cd01320d7aeb89677a34f189aa1`  
		Last Modified: Tue, 30 Sep 2025 00:46:08 GMT  
		Size: 93.4 KB (93386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc70e80f96db7f036acc3d8b7e90b499de2481acd8fd1bfba443b9576700b711`  
		Last Modified: Tue, 30 Sep 2025 00:46:08 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a747702e7ac618c28924fff29384270841e58c2067491ed6db76abd16c244529
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a5eed2cc266a48e5259b2e7b9f08ec4d7cd2d6b99b22fe48f61fd62c376106b`

```dockerfile
```

-	Layers:
	-	`sha256:36458e6b34117b91d12dcd4244f4588605c8a0db6a8649b262ee724e880f54aa`  
		Last Modified: Tue, 30 Sep 2025 16:07:34 GMT  
		Size: 4.1 MB (4073240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e511c629df67a5cfedb1431796c40d83cf94f446c340de58678f642dfff2d9b5`  
		Last Modified: Tue, 30 Sep 2025 16:07:34 GMT  
		Size: 16.0 KB (16004 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bullseye`

```console
$ docker pull neurodebian@sha256:9aabbcc9e03997c57e0e300f2dadd2fa342925bacd78e396ab2dedb03b289cf4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:bullseye` - linux; amd64

```console
$ docker pull neurodebian@sha256:90176f97fbeae11e926a4772950ecca10e2cac52014b8440880689769c3365df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64964683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dc82a44200c756333f5b555fe7a18517fb0e92fa14bfb8e939dcea79230bdb9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:10ffc47270cd106d2d04bc7ef4749d579620e45a84804ba3b18f0898fe5ecc64`  
		Last Modified: Mon, 29 Sep 2025 23:35:07 GMT  
		Size: 53.8 MB (53756064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60bb421a4930e2bcfde978696c830086d079aab35ba1c99347833f8e9a58469`  
		Last Modified: Tue, 30 Sep 2025 00:15:28 GMT  
		Size: 11.1 MB (11105090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad624fd3765fa4362c54e7d7902aa10f74f77c89e10c5d6f4ef3738e7f4c924`  
		Last Modified: Tue, 30 Sep 2025 00:15:27 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34af5c9cf74d548174fc198db4c5d1e164a0a4675bd762f300faf38c09c4aea`  
		Last Modified: Tue, 30 Sep 2025 00:15:27 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b05496266e0f403e0eb9aea321c1dd77f9ac29cbc5a578e7df7394f0feacc0`  
		Last Modified: Tue, 30 Sep 2025 00:15:27 GMT  
		Size: 101.4 KB (101371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:959217a3a17ae0564029e292b48857c19adc7ab08ae21997f5e0bcf249e41801
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7a4fbfb290dbb27ae2e4c6f7927eaf589c86f437d64babd113afa7267425ab8`

```dockerfile
```

-	Layers:
	-	`sha256:038d0e059dd82b17c302359aad44c9de40c94e27e145ad3bb728283a6f7d6539`  
		Last Modified: Tue, 30 Sep 2025 22:07:33 GMT  
		Size: 4.4 MB (4367914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c8330d706ce39305f99b9284e3c88b0e8f8badbe1f221270ced21509706c480`  
		Last Modified: Tue, 30 Sep 2025 22:07:34 GMT  
		Size: 14.0 KB (14009 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:f1193f6efd10b3ab983be1a8a64f8bc1f80d64b6949e54e7176c742e507da012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63466646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:834c95321290bb80fbb943362f7d5a102ce1d13661db32987817f139a63ffe9b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9b16ae1bbd1ada84c12528379a10e280bd89e0d0332670c8487145eb77fe2fe1`  
		Last Modified: Mon, 29 Sep 2025 23:34:42 GMT  
		Size: 52.3 MB (52257414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:894e91d8dba15a3b763b66d3e1fa907c20e5798df7352d17a02c86a54ef49ef7`  
		Last Modified: Tue, 30 Sep 2025 00:19:07 GMT  
		Size: 11.1 MB (11105918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3ab01a5490af9a96585cc987dda6c3647ecbe6bd654e7fa53a48456dc97af64`  
		Last Modified: Tue, 30 Sep 2025 00:19:05 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b8850b1568c65c1aa3203524d059ed21067c8acebb918b2d7edba05cebf6cd9`  
		Last Modified: Tue, 30 Sep 2025 00:19:06 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9730b5ce5d13b5fdc73c132e2c8eaf827181f95f4c53bffa8a19c565e7050f68`  
		Last Modified: Tue, 30 Sep 2025 00:19:05 GMT  
		Size: 101.2 KB (101158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a9f859b786dd71ef74ce084e33053506531d50099df8ef357b1b521ca1cd7be2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb590ba3ea81ff5639de89ef0cfb6494e61d1ee64b8bda8dd09badffbb1ae10`

```dockerfile
```

-	Layers:
	-	`sha256:f53ebc9df093206078615000382c88d27601d1455ca54a8a0d09fca5be751a18`  
		Last Modified: Wed, 01 Oct 2025 13:07:27 GMT  
		Size: 4.4 MB (4367521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6ce6012efba0aca6b0600413c568d14a40e8b6d8cf7135dfd38e876c53a4cf4`  
		Last Modified: Wed, 01 Oct 2025 13:07:28 GMT  
		Size: 14.1 KB (14133 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; 386

```console
$ docker pull neurodebian@sha256:91101fc62f0e126e1cd22b32c58d8f9050a812c29710e233482ecddbaa252743
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66303068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e90773363c7472474f497049af1b4f0ea7b8fbed01c137c1aac71338c994a672`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ceabdec1cb201cbc144cbbf99606ecccc3942e0acc3ede261d7cced4e3f632e8`  
		Last Modified: Mon, 29 Sep 2025 23:35:34 GMT  
		Size: 54.7 MB (54699245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3377e521b27619564766572ea2f71b3559921ec242fbb887b220fd8413a3b667`  
		Last Modified: Tue, 30 Sep 2025 00:22:13 GMT  
		Size: 11.5 MB (11500396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f01d1de35df3c14a84ad0035183ed7c1104b2e5f80f45b2a9683829e522e075`  
		Last Modified: Tue, 30 Sep 2025 00:22:13 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8509e7b4bc6ce3aa5251a6dae3ad32ba389a23454d4b7adcc4c92228bf4f98fb`  
		Last Modified: Tue, 30 Sep 2025 00:22:13 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac8c536f22ee766f2f5e553467d1f35b363ded878c8e388bfe44b6499783cb0`  
		Last Modified: Tue, 30 Sep 2025 00:22:13 GMT  
		Size: 101.3 KB (101271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c76db36b16162a08fa0701b63ebd9bf847665060b220f003398bc6540ab20860
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4378414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d596924761808ea21d556fd70edd740ecb7db21d97fa41c4b2417381b5a578c0`

```dockerfile
```

-	Layers:
	-	`sha256:e2158b5c2f5dc79e1ae0eabfd7db426b9ae47d1458b5ea2e06392f51c07385dd`  
		Last Modified: Tue, 30 Sep 2025 16:07:37 GMT  
		Size: 4.4 MB (4364433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63a36ec09f808d990c39e454e9b1784b06d6f3c68279f34ac45742f93eeda259`  
		Last Modified: Tue, 30 Sep 2025 16:07:38 GMT  
		Size: 14.0 KB (13981 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:006bb654698876390f6861a0e01bc503f5089f6e891d33d3e93608e93295b9b6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:bullseye-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:ed53fdb5e8aa47b66a22d8e538658ebad6098cf08a563bc4364b74cbaf364af8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64965079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30dc7efdb549d31a79c7a7c2d7d9835c314a974733e6e4bf0eace26b5e2a4b01`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:10ffc47270cd106d2d04bc7ef4749d579620e45a84804ba3b18f0898fe5ecc64`  
		Last Modified: Mon, 29 Sep 2025 23:35:07 GMT  
		Size: 53.8 MB (53756064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2fca013c373c9ce58b6cae21ac454c7d47366050a594e13b8250f10afe79b75`  
		Last Modified: Tue, 30 Sep 2025 00:15:32 GMT  
		Size: 11.1 MB (11105101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5638541c3cf3d2a86eac6c5fcc3ffb9b67a57a9bf46c7182aa0c4e311665bdb5`  
		Last Modified: Tue, 30 Sep 2025 00:15:32 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499ba193c40041c0e5fa201d166aacdf33b0beb97469f81b7a403ada1b74aa64`  
		Last Modified: Tue, 30 Sep 2025 00:15:32 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cc132915d360c4f2d791549fd2ca2f013a650e235933b950b6ea0d7fffde166`  
		Last Modified: Tue, 30 Sep 2025 00:15:32 GMT  
		Size: 101.4 KB (101370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d96ede1e50978e8f730ea66b147365e342f86943fe800c73171995596daa40f`  
		Last Modified: Tue, 30 Sep 2025 00:15:32 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4af9a206596649c0e27466361f63c4c1a81826669a33c4bce29a21db8fb07424
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c73b451f85aca4ffbd5a0ea300b70f779265df1295afa1807295ddbcd3dc7b`

```dockerfile
```

-	Layers:
	-	`sha256:d9759dd16036ea272c06141d4b727faa571738fcb11840b1e3f52dddcaf0e3c3`  
		Last Modified: Tue, 30 Sep 2025 22:07:38 GMT  
		Size: 4.4 MB (4367950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4b0a72aaf5eddf29cbac0cfad24af7f1f15d3cce4607ecf2e443ecd47fdd859`  
		Last Modified: Tue, 30 Sep 2025 22:07:39 GMT  
		Size: 16.0 KB (16037 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:1f30c996b1974cb30d1db39be8e14d35af351b8c84dccb11cf951e3cc9d9f1ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63467126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:718623496dce620b8a091b46c678973300bfa6e35ec5b7adc0220eaa71a28437`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:9b16ae1bbd1ada84c12528379a10e280bd89e0d0332670c8487145eb77fe2fe1`  
		Last Modified: Mon, 29 Sep 2025 23:34:42 GMT  
		Size: 52.3 MB (52257414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e503815c3695e065c3bfebbe02e4ca6522e055f3d2811a15fbf0f7e671f7fe9a`  
		Last Modified: Tue, 30 Sep 2025 00:19:14 GMT  
		Size: 11.1 MB (11106034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74f4b86a4499aeaa235b1bb5c60fa3f1f0a538facfee71bd3bffeedb937421b7`  
		Last Modified: Tue, 30 Sep 2025 00:19:13 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a7c071199696c6bc66c27249bba23d3d61056f23bfd53331e3490c87150eac5`  
		Last Modified: Tue, 30 Sep 2025 00:19:13 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6374e812d78ea9095cd594a1ab8c52c5a1438b0e9701b7b90c66ffedf3bfbb15`  
		Last Modified: Tue, 30 Sep 2025 00:19:14 GMT  
		Size: 101.1 KB (101132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d983cf93511e8b9e722d857bbb40a47af2452461f6c49fafc915752f11dd59fc`  
		Last Modified: Tue, 30 Sep 2025 00:19:14 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:aad05f3c3dc155bb3e1cf0980fb82714fda5e4ad24ab9e3c31b7b0271f23d4fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6776e87ce097931b04f1195033a91a66a08f69df9c7afaf23fd077ed706a38cf`

```dockerfile
```

-	Layers:
	-	`sha256:f149e404fb039204918eb81df1083ab7710e02a97e75ad9a80312a7ad77fbb99`  
		Last Modified: Wed, 01 Oct 2025 13:07:33 GMT  
		Size: 4.4 MB (4367557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d584879ab879bad46254130981389b7b21180def03e30acc6871281df46d3102`  
		Last Modified: Wed, 01 Oct 2025 13:07:34 GMT  
		Size: 16.2 KB (16177 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:4eea0d4fd77d66b5b2802a7722eeb5fb2109fb7a02966f5d8635d076cda4536a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66303456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:542a028b735297cf6aaa7fbc7248c5fa8f08bb0f6a5152c346243217df1be188`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:ceabdec1cb201cbc144cbbf99606ecccc3942e0acc3ede261d7cced4e3f632e8`  
		Last Modified: Mon, 29 Sep 2025 23:35:34 GMT  
		Size: 54.7 MB (54699245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3377e521b27619564766572ea2f71b3559921ec242fbb887b220fd8413a3b667`  
		Last Modified: Tue, 30 Sep 2025 00:22:13 GMT  
		Size: 11.5 MB (11500396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f01d1de35df3c14a84ad0035183ed7c1104b2e5f80f45b2a9683829e522e075`  
		Last Modified: Tue, 30 Sep 2025 00:22:13 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8509e7b4bc6ce3aa5251a6dae3ad32ba389a23454d4b7adcc4c92228bf4f98fb`  
		Last Modified: Tue, 30 Sep 2025 00:22:13 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac8c536f22ee766f2f5e553467d1f35b363ded878c8e388bfe44b6499783cb0`  
		Last Modified: Tue, 30 Sep 2025 00:22:13 GMT  
		Size: 101.3 KB (101271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4e1e7d055597b7ae7b2fb8e3c043ee71c83f9caffb518b6a538a65f2c12f729`  
		Last Modified: Tue, 30 Sep 2025 00:22:19 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:99aaca37cdb012e66ae234bdb48111ffe493f7bf2d722d6de4fdc301d88509ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4380476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:337428655da965ead524ac77fe7953cb70305e76c5a4b1741367f923e55a810f`

```dockerfile
```

-	Layers:
	-	`sha256:c18dc37b060df10df4047be8729a361fc8895477639ac9b8c869cb13d6d9a49b`  
		Last Modified: Tue, 30 Sep 2025 16:07:45 GMT  
		Size: 4.4 MB (4364469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13d12e9ab20c1ea4a6f193720b7539452b9adcc7655702e761d5bf73575fe789`  
		Last Modified: Tue, 30 Sep 2025 16:07:45 GMT  
		Size: 16.0 KB (16007 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:forky`

```console
$ docker pull neurodebian@sha256:c92360ecb28f2f89c85be4dbf26acfe13eab117f3fb4b5207c4cd224a3ebb585
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:forky` - linux; amd64

```console
$ docker pull neurodebian@sha256:345b73cc3cff330f591113ad5c395e6f1d6d41737f1aa30d2cd0890eec290e20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60209260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29205c954925c1ecb55bac9ed0b80d21438ff3c4f7a6310eb2538739681d65a7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e4cfa25241b18c60e1d77cc5cfae85a9e13d25b981d6592cf216e6292e3a9555`  
		Last Modified: Mon, 29 Sep 2025 23:34:30 GMT  
		Size: 49.7 MB (49736818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ae5466bb071b4d5fd8eefcee42963b6fb9049be541a84881dc6308e473fc8e`  
		Last Modified: Tue, 30 Sep 2025 00:16:29 GMT  
		Size: 10.4 MB (10379739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1807ebbab503ae80b9399051b61f04755ca3d6aae60f4dc6d425a0bf7720c092`  
		Last Modified: Tue, 30 Sep 2025 00:16:28 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd66df67e8d400f04c58dbc6b030e39a1acf8a05e6146909b24aa7170753dc9`  
		Last Modified: Tue, 30 Sep 2025 00:16:28 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afa15f7f278e086ea0fbfd80f89d1c5006e7335cfc7be13c9460227d1cf6fbef`  
		Last Modified: Tue, 30 Sep 2025 00:16:28 GMT  
		Size: 89.8 KB (89801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:852b8be1f7037fff7d287538ad33f1cfc8866e29620587784f5b9d583b107b34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3617518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c24d1eb59953bf3dbf18bc9e6d60ee7930713fcdc584cf97746191124cd2ffe`

```dockerfile
```

-	Layers:
	-	`sha256:85f5c52cfdcf421d688db7359c6af95dcbf0fdc4dae316f1ddff761a459c067c`  
		Last Modified: Tue, 30 Sep 2025 22:07:43 GMT  
		Size: 3.6 MB (3603543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8e92428ab852a3e9d6c4f35263068e7e9d1f55e02615a19121b450e71837a5a`  
		Last Modified: Tue, 30 Sep 2025 22:07:44 GMT  
		Size: 14.0 KB (13975 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:48ce0de5fa5a7f531ef0099c39eb5a1f0f733aacb5a5202aee0d7072d739771e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60131499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea1ea47940a8675950da1ce2c4198af21b8d44ac640778235f4f68f05ff9bd4f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ed417fd581c20c18b8c6cfc58498c59128dd74498d5d6a89f9217103a4fbf9d4`  
		Last Modified: Mon, 29 Sep 2025 23:35:24 GMT  
		Size: 49.9 MB (49879877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15cff7a9b9fb682e2c2e6993119b846dc5b1d81710a757f010425ecbe1699e49`  
		Last Modified: Tue, 30 Sep 2025 00:20:07 GMT  
		Size: 10.2 MB (10158245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a548c6783d21d82bed7da77c4ca8c4b15bab1a515f2756f4695815fab7b460`  
		Last Modified: Tue, 30 Sep 2025 00:20:04 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9019ec9d5a01b9d86df23fc3e913b0e3cf0c7230ec7d73e3363eaca9b07a6e6c`  
		Last Modified: Tue, 30 Sep 2025 00:20:04 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c21116de06bfade79387d1406dc1f8cb6ecc55f6691c8ce21d819d9994eb77`  
		Last Modified: Tue, 30 Sep 2025 00:20:04 GMT  
		Size: 90.5 KB (90476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e91d5af2acabb5fc1c42402b01c0a6d4077ddbf95ec53c76ab3518d1f502c6e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3619158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:655998c0f6a1a91e187f80b049db97a567ec9001c232239e0970f3e7e5e3f149`

```dockerfile
```

-	Layers:
	-	`sha256:0cd9a524431ae523b0025aa698d246bafd57a0cdad0bbf85884164c814362b71`  
		Last Modified: Wed, 01 Oct 2025 13:07:38 GMT  
		Size: 3.6 MB (3605058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47f001f336ef37958e08b2b08580f72ea63e862ce86e03828d8a1eb665ee3ae5`  
		Last Modified: Wed, 01 Oct 2025 13:07:39 GMT  
		Size: 14.1 KB (14100 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky` - linux; 386

```console
$ docker pull neurodebian@sha256:93076c4c2d0e94886018f69e1152e8deaf2d4bed3e6efbcbafb955ac2a8821cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61744597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c512496e92c8a2ab4d459299062ede4abcb70e38f111d2e6aa0b505fac923153`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:376eb1520bb62885f5204083862e9559c55db2c2217bc7ae5d95166cd5564cbc`  
		Last Modified: Mon, 29 Sep 2025 23:35:30 GMT  
		Size: 51.1 MB (51119420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a865d211977b3f1fcb807a758d4ec086437dd6673f67e3e1d591e17e58882cb0`  
		Last Modified: Tue, 30 Sep 2025 00:23:14 GMT  
		Size: 10.5 MB (10532079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91719f443526b031661e5a96a385443574e851a066f71ada0666f70884b0e2dc`  
		Last Modified: Tue, 30 Sep 2025 00:23:13 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b17552004c93b6782e1e3a7a419888801d004eedb43de407b78b4ea866fea1b`  
		Last Modified: Tue, 30 Sep 2025 00:23:14 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d093529586e174c24eba4daef5bc737d33409e0ab114788aeeaecda34415aa42`  
		Last Modified: Tue, 30 Sep 2025 00:23:14 GMT  
		Size: 90.2 KB (90191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:88c49151d58c1387ab21df41ef3530d5a8bac401ff1fe37dee65a3caaded9855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3615449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bdd154be2b8b9d7924f741cf7a9dddc57d872f8fb9afe3536f35a8960c6cafa`

```dockerfile
```

-	Layers:
	-	`sha256:154737cd4e2fe16fcfe2381c2c77298084a954fbc4a92d2a4987a4f405a1af1b`  
		Last Modified: Tue, 30 Sep 2025 16:07:47 GMT  
		Size: 3.6 MB (3601504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6407fcef5a1ef280b76d26fac524a4f6552d3ed6baa7676692a8c113201710a`  
		Last Modified: Tue, 30 Sep 2025 16:07:48 GMT  
		Size: 13.9 KB (13945 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:forky-non-free`

```console
$ docker pull neurodebian@sha256:9eed6b58b84a550a5974629668891a7528c7538bb2eb7c3c961effa4073f6f6d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:forky-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:f5fe87c1e1ad0cc109f0cf8f6a9d2c6474eaacbdb1477dfc6342d827eb111f01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60209747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a9184bde64f75bc0898f709fdf492555b74abd3086acfa010bcd4c6dd3130ab`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:e4cfa25241b18c60e1d77cc5cfae85a9e13d25b981d6592cf216e6292e3a9555`  
		Last Modified: Mon, 29 Sep 2025 23:34:30 GMT  
		Size: 49.7 MB (49736818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e573455d7fb5304cf7248f536b62a4140b90208a5690f4a3a85adc6e5547e5b`  
		Last Modified: Tue, 30 Sep 2025 00:16:34 GMT  
		Size: 10.4 MB (10379740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b291dd14f83d964b7f57044bc7f4a04295df37ba77f9fb5dfc9bb9c7de1d8a`  
		Last Modified: Tue, 30 Sep 2025 00:16:34 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2837bde73fa3149d81eb22fd9ff320d18a2c316af16da953569a16018bd3f9a`  
		Last Modified: Tue, 30 Sep 2025 00:16:34 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c5c97b9334b4e50feeaa05190b4476afb1c64d57ae2a3336fbecf4267507ae`  
		Last Modified: Tue, 30 Sep 2025 00:16:34 GMT  
		Size: 89.8 KB (89840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:617c03802ed8fc2f823aeb323ee3010b4ad1f995325a6947fecb7a0a0a9461d3`  
		Last Modified: Tue, 30 Sep 2025 00:16:34 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7a40e42eeaf5bd5622f29cb6a9dccd0f2036541929f187703eab2dcd3cb73fc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3619581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3525f3a7effb0513b670c1151c6e814417883c77141c277e0dfaae15ca7ebd65`

```dockerfile
```

-	Layers:
	-	`sha256:bb336d527b6b81a8b19843c8b794c242c15418fb84454637d98af93a858b6d0c`  
		Last Modified: Tue, 30 Sep 2025 22:07:49 GMT  
		Size: 3.6 MB (3603579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e8bfedbe13e8c850a9352ab07cb8c2451926c8b22fbbef681706adcbcc2380f`  
		Last Modified: Tue, 30 Sep 2025 22:07:50 GMT  
		Size: 16.0 KB (16002 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c965c49aa2b396e0101b42550f4800063f3fd56d517bec513e386066326ed80c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60131972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3ed496450d5563feac3099d0ade1c40efe2acb32ecfd970708e5e9ea282cfd7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:ed417fd581c20c18b8c6cfc58498c59128dd74498d5d6a89f9217103a4fbf9d4`  
		Last Modified: Mon, 29 Sep 2025 23:35:24 GMT  
		Size: 49.9 MB (49879877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c28b9bca2f1012ffe43d4eed07697f7da1ec3a47f388e1ab9fd4ec84b4e6268`  
		Last Modified: Tue, 30 Sep 2025 00:20:12 GMT  
		Size: 10.2 MB (10158292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10b9f543673e23c7d03685762105c2796b3abb510f7e7108cef41bbbc9a9bfe`  
		Last Modified: Tue, 30 Sep 2025 00:20:11 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a233135e8a5c44543154aa30a4dcb42b38fda3e8ca06d93f639b9f507c3d4219`  
		Last Modified: Tue, 30 Sep 2025 00:20:12 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d384ab44da2640f654099b0207090ccab3d2b58cebd6b3258b13b298c5e3a926`  
		Last Modified: Tue, 30 Sep 2025 00:20:12 GMT  
		Size: 90.5 KB (90456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2747289e0447d3ae74f622064a865138a9eb14243918fc353cdbd2bf3d71df`  
		Last Modified: Tue, 30 Sep 2025 00:20:09 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a2db88cd42eb7894e3e8a21855afe072e4bacb15736552d6bdff99769a6b19f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3621236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65795b979a2c217fe3c2025935d0c3f835af9f1520d745f2a112578257a83bb3`

```dockerfile
```

-	Layers:
	-	`sha256:6dc4931ed3e401fa42d22b976d0772f8eafaefc7add51f5418cb8196a0eb1155`  
		Last Modified: Wed, 01 Oct 2025 13:07:44 GMT  
		Size: 3.6 MB (3605094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb89734c2b1f04a1157e15fb2b072b93a1559445ebf22f509e9bd6d50f99abd0`  
		Last Modified: Wed, 01 Oct 2025 13:07:45 GMT  
		Size: 16.1 KB (16142 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:f430324cf9cfaa124d9776470203aac188ea6774709949a77b63e213adfa7ec1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61745177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a38ab08689612a8e95f9cc551ea0e8a30bda1c448048e882314e67c82e2d34da`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:376eb1520bb62885f5204083862e9559c55db2c2217bc7ae5d95166cd5564cbc`  
		Last Modified: Mon, 29 Sep 2025 23:35:30 GMT  
		Size: 51.1 MB (51119420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec729a899466ae066afe6bfa44772bb49f12eb1ff9130de5775863dfce2fa5c`  
		Last Modified: Tue, 30 Sep 2025 00:23:18 GMT  
		Size: 10.5 MB (10532172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016bd38ecc73b56e051fb135bc2f1b210de58690a65bd5202836c5e688c442a8`  
		Last Modified: Tue, 30 Sep 2025 00:23:18 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b44b7f804d68298cf138540a3c3108a2814c8cc63932f7300357c68efe7054e`  
		Last Modified: Tue, 30 Sep 2025 00:23:18 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24e9b8bf1f68d7180b0cdf3058bac384f72680340471c2b07b70711bef9c350c`  
		Last Modified: Tue, 30 Sep 2025 00:23:18 GMT  
		Size: 90.2 KB (90232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bbf84aa702d16438adb1888b29adb0d130c0a91212dad4f8842d559e332ab6`  
		Last Modified: Tue, 30 Sep 2025 00:23:18 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3b490107fb10d10a6ec4ea0b23243b771a836b62a9ec8a2428a0dd7c4b38d4c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3617512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48447039b9ee7cf8a837ef0de7f2fc8a4c3e43acdd0ac2c4ad657cbc9f7839ef`

```dockerfile
```

-	Layers:
	-	`sha256:62948bb3b9d5b778029c610a4efda1d2a480c111bf40184b640d8df7f51d9e93`  
		Last Modified: Tue, 30 Sep 2025 16:07:55 GMT  
		Size: 3.6 MB (3601540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:153eff5adb942a4269e6f4cb5eb6afbaaab407c0686fde860d67023ab18eb4f2`  
		Last Modified: Tue, 30 Sep 2025 16:07:56 GMT  
		Size: 16.0 KB (15972 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:jammy`

```console
$ docker pull neurodebian@sha256:c6bbd2e1e36b66c40fd53f7b4a059adde6ca793f3c733562f99aafa599288aca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy` - linux; amd64

```console
$ docker pull neurodebian@sha256:d3ce910a25e1ada8fb29113c427d363d0950df18f993942bb1e966b293c906fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33275318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbc492e3e53cf64bb4f5f322e8772c61cb99e0627ce806d72563b7cd165fa6c0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Sat, 01 Mar 2025 01:29:10 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a4724a87526948a669d180182a6778e1e691c719838765abce4d01c46d3989`  
		Last Modified: Tue, 02 Sep 2025 00:23:48 GMT  
		Size: 3.6 MB (3625618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c380e33d94fb72232b49c8bc34ed7ec6d5fc476094360c374549509f46be63`  
		Last Modified: Tue, 02 Sep 2025 00:23:47 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df5b8f40e27413a9ed04a139b53a2d27ad574119fb38e07573119b5f1ba2b7cb`  
		Last Modified: Tue, 02 Sep 2025 00:23:41 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f236e29b2af85abd6976a93143c874089cd671b6c9dce78ea9370ae33bedea`  
		Last Modified: Tue, 02 Sep 2025 00:23:42 GMT  
		Size: 110.6 KB (110589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:34aff235caca5114ffe5988df3758c029134f3cfd79928f2b7b75e046d884177
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e35a861e1f8209aec3893a6055acb4e242ebe33c2703d85a893b48ff3b02363a`

```dockerfile
```

-	Layers:
	-	`sha256:7d41caedea004a5f24a35b74306fc2bb1a9a276bf38f155d55be744db8ac4a1e`  
		Last Modified: Tue, 02 Sep 2025 01:07:20 GMT  
		Size: 2.2 MB (2198320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b09e2e050c9cb1cb84b85074083ff037333a48e8c7fdc30b0f24b2e72482d686`  
		Last Modified: Tue, 02 Sep 2025 01:07:21 GMT  
		Size: 14.0 KB (13976 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:ae36027e8a53ebbe67fc5a247ce3721db455994cdd9c7fe2df2ffbd78da627bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31093913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8441f857a939d9eb264ff7103795215c13448469d105c5c5c7e2ab556229accb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
ARG RELEASE
# Tue, 23 Sep 2025 14:32:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 23 Sep 2025 14:32:09 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Tue, 23 Sep 2025 14:32:09 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:325d6f6c4d15398bceac73c423e869d31f8fcaacf16ca565983fdff9003cf76e`  
		Last Modified: Thu, 02 Oct 2025 01:27:05 GMT  
		Size: 3.6 MB (3598093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b7ad240b4794dcb9ff6ace41057dfeb2c804e8db2480980e681e206b8635676`  
		Last Modified: Thu, 02 Oct 2025 01:27:04 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ecc594e7b7209ce34aed504e0d23bbf64a12c46d335f394b14f2f46ba067f3a`  
		Last Modified: Thu, 02 Oct 2025 01:27:05 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e88a579f7a31e08c9eb8dcc30111f750f38aa584d7a7a3d6c5e8abb56f595860`  
		Last Modified: Thu, 02 Oct 2025 01:27:04 GMT  
		Size: 110.5 KB (110539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c773c982f1a26fe4ea848a6232124df833ffb6f941fdae72942deee77c6fc22e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d5f66dccecae4ef8f224184a495667a7d50c6d2962d94d04e0550f29fdd65ac`

```dockerfile
```

-	Layers:
	-	`sha256:d590c7dac959fee7986e5f332cc54f2808b6a714ae848fd9ad2f5a8c578b77fe`  
		Last Modified: Thu, 02 Oct 2025 04:07:27 GMT  
		Size: 2.2 MB (2198580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1385b30d72b453beeea33a81825a47038c89d6340a0d74c17ec2416c040452a`  
		Last Modified: Thu, 02 Oct 2025 04:07:28 GMT  
		Size: 14.1 KB (14101 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:jammy-non-free`

```console
$ docker pull neurodebian@sha256:8aed8de3f1160326e3957e3cbaa386a9ad82eeace52d585f8cc758faf39ec1f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:2fa15741085a7b9a111304f94de710a342d4003de42f96d7188ae76614ee49ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33275636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:691f3a6a8f1c8ad9cece02d2fe19baf080213cf7ed68cdb0ad98152ada06cb1f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Sat, 01 Mar 2025 01:29:10 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:644d350e6c4b05f6944ae006b8aab5488c91516ffd162cfaba7f84ac273d473b`  
		Last Modified: Tue, 02 Sep 2025 00:23:45 GMT  
		Size: 3.6 MB (3625625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d90e43a114a27e26541cb1e85f4e91c965938ba1a97cae143d255897aff2129a`  
		Last Modified: Tue, 02 Sep 2025 00:23:44 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19ac9ace5a9e24d09a5d74cfbef2b3423c8652f27e8f966bd9bc62e9113363ce`  
		Last Modified: Tue, 02 Sep 2025 00:23:45 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a32399516aec62d325145feb3435edfb7a8ae0199ff2cb6bbd66c90cccb4d2e3`  
		Last Modified: Tue, 02 Sep 2025 00:23:45 GMT  
		Size: 110.6 KB (110617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7cb48d532455ee1f3cb8304abe4242d944151fed04590177b16c700f70b807`  
		Last Modified: Tue, 02 Sep 2025 00:23:45 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c57cc66c296caefe8491e689ab76b85cfa5a28354db8fcaf6d4e285820860324
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:607be7f30cc779a1e17202a6d6c14b2ac08edabd49cd5703daef1c66963a2b95`

```dockerfile
```

-	Layers:
	-	`sha256:28344ea9cda64308e3f2beaec2b0f1ecf33f042627051ad839a05fbb550e8d2e`  
		Last Modified: Tue, 02 Sep 2025 01:07:24 GMT  
		Size: 2.2 MB (2198356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f32e711bd76c0a3933a65639adf42f2367cc2f94d3e8d671098de1fec9256e73`  
		Last Modified: Tue, 02 Sep 2025 01:07:25 GMT  
		Size: 16.2 KB (16206 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:3477c05d1c44a95df25451442a0582adc59b19a1fa02d71ac9defd2e99dea2f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31094169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bbe9716177d8f8c156f3750861d90f455ba6b3aed16e8bb8c0463bc4fd51b33`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
ARG RELEASE
# Tue, 23 Sep 2025 14:32:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 23 Sep 2025 14:32:09 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Tue, 23 Sep 2025 14:32:09 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f860954b7aec09e8e634d06f465a2fee9f5efc8618a451be9ca3999110a04e0`  
		Last Modified: Thu, 02 Oct 2025 01:27:26 GMT  
		Size: 3.6 MB (3598078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80240768d635dabbcefc8ff489dd31b390e710ec1a57a20717f266cbb43f3a12`  
		Last Modified: Thu, 02 Oct 2025 01:27:26 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d84b19e7977bcb10026b60e7b92462d7e2992d0969dcbd487e6c1716a80bc89c`  
		Last Modified: Thu, 02 Oct 2025 01:27:26 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a31027b0f91a269a073a36622efb6855af47112b4c53f9b2bdb4ffc8b6caaa`  
		Last Modified: Thu, 02 Oct 2025 01:27:26 GMT  
		Size: 110.5 KB (110527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b56be4a06905892f6b37985a75ee287ae36160af8de2c3299e76657303232f5`  
		Last Modified: Thu, 02 Oct 2025 01:27:26 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2d027eaa6f6342192209425d6ecebaa9137e2db5ac730d34139eff64a9ba7f0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62f4d6e154722074fc244a1c8c4b58453a017f4c753a2047c43d2a7e1d1ca1e0`

```dockerfile
```

-	Layers:
	-	`sha256:3446b6bd4ea75dde0ade5bf1621b0940160475b92f8445fadf17a1f4e63dfae7`  
		Last Modified: Thu, 02 Oct 2025 04:07:33 GMT  
		Size: 2.2 MB (2198616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34d889bfde4fce06c5ea57e1f1822e2efe7d3b957970ea5f2f890dc14ec4116c`  
		Last Modified: Thu, 02 Oct 2025 04:07:35 GMT  
		Size: 16.3 KB (16346 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:latest`

```console
$ docker pull neurodebian@sha256:87693cfb664c3983f3e574e1dcd5b58f82fd2618b8af3a364767508759c8e2c4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:latest` - linux; amd64

```console
$ docker pull neurodebian@sha256:5445400c594afd56d8608d270c0e840a5bdc8ce8eed14c50875b111ece8c8967
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59667200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1692c2ad0959aff9134072de309c7092e4303f34bd66175926b4536f01737b1b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cae3b572364a7d48f8485d67baee38e4e44e299b8c8c4d020ff7fb5fdd97f88c`  
		Last Modified: Mon, 29 Sep 2025 23:35:29 GMT  
		Size: 49.3 MB (49284626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf661b2ff63805151437f18c9fddf545dc18823488c0dbe851eafeba8066d82`  
		Last Modified: Wed, 01 Oct 2025 00:26:33 GMT  
		Size: 10.3 MB (10289495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030c7393f1d0600f3d5801fa9a09be77c972b3bf6cec3d9a0ceee41e16f80f79`  
		Last Modified: Tue, 30 Sep 2025 01:05:19 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7679f2a094fcaa509ff0dbff39c2f33e8f9ee67eba015e63ec580599369bd963`  
		Last Modified: Tue, 30 Sep 2025 01:05:20 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5fdaff3323992c80159a90ce241b8c1e2eecfc50b87e4e1f570519c04063c53`  
		Last Modified: Tue, 30 Sep 2025 01:05:19 GMT  
		Size: 90.2 KB (90176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:11379453b3c698293768b9d690e1a7e9d3b6991a688f6f2c6c9d46d25b7a1999
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3627275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e291424f296bf0582d068b79c4a19e3cf1f75fa0e7f7d4051e57733efe754ae`

```dockerfile
```

-	Layers:
	-	`sha256:a5d6e8b4a14ee685087c48f425191d4046aecfdc2e2dce91edd6ba320a8a65b9`  
		Last Modified: Tue, 30 Sep 2025 22:08:37 GMT  
		Size: 3.6 MB (3612981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cba41c16a9c24d09b71598c74915dea63db262a1a93abcbc3f0d247b9b4c11c2`  
		Last Modified: Tue, 30 Sep 2025 22:08:38 GMT  
		Size: 14.3 KB (14294 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:5d39e0ae09097ede0b7dcd605763843cc32f5d004f39cefe691f3534fcabf107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59815441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d12c54dcf7bbe6d3551a1d49ac956e0b9ef7c361391bd2511992d7c2ba5cc6f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:28aec8b14b3eeacbf47ef38af72fab694b109fdcdf31581722750599baf1a932`  
		Last Modified: Mon, 29 Sep 2025 23:35:17 GMT  
		Size: 49.6 MB (49648695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b6f6da96540c9f6cf298b7b364c63b1cf0c3929b805fed831b6c1c3eae4d87`  
		Last Modified: Tue, 30 Sep 2025 00:19:26 GMT  
		Size: 10.1 MB (10072980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a478dfca60a2c33636ca722a574ff603abd3fae381c95be0c7bf68323a3704`  
		Last Modified: Tue, 30 Sep 2025 00:19:27 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5474e962acd88276c7b9fa402cc148afe511eddb2832d559ea63b51fb720b0a`  
		Last Modified: Tue, 30 Sep 2025 00:19:28 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094906ccc10fa032c3efb4b206bda6edbedb9eca7903daa2ebdf676a5f615361`  
		Last Modified: Tue, 30 Sep 2025 00:19:28 GMT  
		Size: 90.9 KB (90866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2be449b53fb3b4125c74bfaf49a273c82589056f7a7b58ced28d693d35ecfd68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cf5e15992d5473686642c610909b239be7d6cf3f13bcfccc273a3f7cd5cd553`

```dockerfile
```

-	Layers:
	-	`sha256:ea9f419913ead7a4c0e010568c2d3864423e07529314b03a43cadf13070d7ebe`  
		Last Modified: Tue, 30 Sep 2025 13:07:45 GMT  
		Size: 3.6 MB (3614508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08e6d045cefb6337ce69dbe9c61d5d154f22a2ddc355e21d8fb66a2d9f615939`  
		Last Modified: Tue, 30 Sep 2025 13:07:46 GMT  
		Size: 14.4 KB (14431 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; 386

```console
$ docker pull neurodebian@sha256:8a46319c2bee6856b4f764ac30025c5587a5ee243fb31b30dbfc8d7fdbaa6d9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61356323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35e989f30d27cafca9de5bdca46f6e0f4139c1fd7362a134d113c77557fab4dc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f1c1f592b5569b5e2093c3107a48f2929b609f05af6d24c06d41a7ec1ae5e0e1`  
		Last Modified: Mon, 29 Sep 2025 23:35:36 GMT  
		Size: 50.8 MB (50800229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ab973589bc45010616b19754c3c69e0ae9f8ca8970197b3299d394ea33f588`  
		Last Modified: Tue, 30 Sep 2025 00:23:16 GMT  
		Size: 10.5 MB (10462616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3efbe96c0b7cb9c8886f791f5343077fbcb6ee8bf991286ebe52cab58d6cc892`  
		Last Modified: Tue, 30 Sep 2025 00:23:04 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dea642e4992382c23719b878885f48c32247f1f5867d347ad4c22d63c0a8720`  
		Last Modified: Tue, 30 Sep 2025 00:23:04 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6ae40746c8c652627ef29267be656c50aab350b775d26b475917c7e2742ed1`  
		Last Modified: Tue, 30 Sep 2025 00:23:04 GMT  
		Size: 90.6 KB (90577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:01edb6d5394be68b0049fb213c5711380de11bbe71bb915c1a99290309011366
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3625191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff7b3eabd530054c8c1027eb5ff3de1c92acd70f4dac5652e04a574e629a340c`

```dockerfile
```

-	Layers:
	-	`sha256:031421d4527aa62b75263e52be1877d3065aa1b9c5575c49b0f1fb55f48c5bf5`  
		Last Modified: Tue, 30 Sep 2025 16:08:34 GMT  
		Size: 3.6 MB (3610930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c15ca298c4f9b159a9a1e17f17ba6bf440488c13b2b3af4a01a92335f30ff50b`  
		Last Modified: Tue, 30 Sep 2025 16:08:34 GMT  
		Size: 14.3 KB (14261 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd`

```console
$ docker pull neurodebian@sha256:efce4ea64f54ce4a5c6ed6882dae178fd70c24cfeeb45d63e709d00dcf8c93cb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd` - linux; amd64

```console
$ docker pull neurodebian@sha256:d352e1bdaf20b107fa873d64a014ec03a55aef6211f5e056a6cd7f3ef5a88915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (60018849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71e0de86f6c90cc7f5b47e859e7f0734d0c0be75b51cc7cdd2e6b8ecce9e6673`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:edd38bdf09a62ab44ffab2a10058156dc336ea087cf3a73258758d9bc541ff85`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 48.4 MB (48376965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1964d781cff69dcbb8224608d47e77cbe0ca18c19fda7c500947ce54b349e439`  
		Last Modified: Tue, 30 Sep 2025 00:16:32 GMT  
		Size: 11.5 MB (11549277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8083c7a164d9c55e20112d87245a4ac7874df659703dae0592af0ea6dc17eec3`  
		Last Modified: Tue, 30 Sep 2025 00:16:30 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f64ec4cb897b141395739b755c043b36a97990c58c741b36add1af451669ac27`  
		Last Modified: Tue, 30 Sep 2025 00:16:30 GMT  
		Size: 267.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ce650969fa61f99b87dc4e0c2355ec5b19b5ca0c605b89d71edb13e8210bdf`  
		Last Modified: Tue, 30 Sep 2025 00:16:30 GMT  
		Size: 89.7 KB (89708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e7f9cddb4bcb9e61947b1cbfe3d7283a24493ed40d524daf2d52203c8bcf6a1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3589132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee385a97eca1722b360e37f2ea21db83a4ca65ddeeda1726838355898e459199`

```dockerfile
```

-	Layers:
	-	`sha256:3450fd91ed423943f5f1ccb0586891b2edc69f23515ac0c6df2af5f4ccf8ad17`  
		Last Modified: Tue, 30 Sep 2025 22:08:27 GMT  
		Size: 3.6 MB (3575185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7c306a879bd2d2a90c91968619437991d21396041c3e0a911e5cf413f8d409f`  
		Last Modified: Tue, 30 Sep 2025 22:08:28 GMT  
		Size: 13.9 KB (13947 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:f276efd9172e11522046410af5ce0eb50a69e25afff35700d60c8301448a2281
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59869090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afc5710290db43f8f232f408c6687165992caead41c0085fa62263a4362cb9db`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f5aae340a376cad680dc8a41a7fd30a241ed4bae3e53125ebb424c8fc7996aaa`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 48.5 MB (48487991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc322d3092244931732034d2c756709c302b50f1227794a20a81109328519c7`  
		Last Modified: Tue, 30 Sep 2025 00:20:10 GMT  
		Size: 11.3 MB (11287787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29113037dd1be00d90a636436bf0567190c0201bd65bbc714d71afbda2ab6950`  
		Last Modified: Tue, 30 Sep 2025 00:20:09 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f8fc058e5e886c0a4787a53a804e614a59df193c608a14fc339b41a0f5a7112`  
		Last Modified: Tue, 30 Sep 2025 00:20:09 GMT  
		Size: 267.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe019269d1c4393a725d347c2717dfe5b5dde34b8369131e2a6ebb3f43c61181`  
		Last Modified: Tue, 30 Sep 2025 00:20:09 GMT  
		Size: 90.4 KB (90409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:42c0f769a6605843de59dd9a117d96c8b7446f60fdebfc99b40a806828cd4cf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3590133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d0b0dd03b72ea4b6bf7ee568d8a3aee946316388d6e61e18483a3cb671d1a56`

```dockerfile
```

-	Layers:
	-	`sha256:6607e14c440cf1ec05381d57aab85c2f3e0692fc5eb4066035be42c25f0922e5`  
		Last Modified: Wed, 01 Oct 2025 13:07:53 GMT  
		Size: 3.6 MB (3576061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd0f3dce5e1f118d17d9bbbb63d168fd52f0fe2ccbc70d27cc2a73ce8c7c4605`  
		Last Modified: Wed, 01 Oct 2025 13:07:53 GMT  
		Size: 14.1 KB (14072 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd` - linux; 386

```console
$ docker pull neurodebian@sha256:0622b7c8607a17ed3f062dcbbe2e5ce444ad89bd2e586f4142e8de5a0190ac11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61496239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a7e383cde8bac028bea9bf478d11f6e67bf5fd643663cc161c83f71ffcd1d77`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d00269cb73b9e4cfebd155b431da849e0072689663a0a658044389a50f9d989d`  
		Last Modified: Mon, 29 Sep 2025 23:35:17 GMT  
		Size: 49.7 MB (49686171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6f6480fd49647a130c5672473eb706e570d0a7e2ffc738010f418159bb8f42`  
		Last Modified: Tue, 30 Sep 2025 00:23:15 GMT  
		Size: 11.7 MB (11717042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00bb6b77036d5b364bd2bb6f5016c7e6e6e1f51fd3acd6413ec0fffca6c7be09`  
		Last Modified: Tue, 30 Sep 2025 00:23:15 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ead752bbeef4f8b6544c7e6da0e9c452da6e55d7f7bf44255bc5705f3e41be`  
		Last Modified: Tue, 30 Sep 2025 00:23:15 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbee98413e70c0108e75166cd1eab704dbccca336d46231839dd53c9b6e22b1d`  
		Last Modified: Tue, 30 Sep 2025 00:23:15 GMT  
		Size: 90.1 KB (90122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:83a99d285742e7df8821f912e07a2fdc81967eff6e1c18910effd26a40e17be5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3587067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62902d1e1f48582360c7d309fa12760e834aea5cc58e13c631bcbb277337dbec`

```dockerfile
```

-	Layers:
	-	`sha256:cfa6aeb85429432a36111a8460eb077d4be2c8e303826ac96fdfe3489298992e`  
		Last Modified: Tue, 30 Sep 2025 16:08:22 GMT  
		Size: 3.6 MB (3573148 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe777d0a54bde48dc55901a7c0d9b6fc6677cdd0df0f45a4aba0d526aa5e4078`  
		Last Modified: Tue, 30 Sep 2025 16:08:23 GMT  
		Size: 13.9 KB (13919 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:97ae4ac92c67e53d9f68b612bc47d6a6995653609ebad9bf76d3bbb1049a3455
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:3e546a3eedb271a9eb8c8a3fd359cc34aa309cb0f055384484db71a135a5a035
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (60019399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:452d59ad840fbcfd81c522c18b87369321b77e10537e7abcd4be040eefd0fcf2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:edd38bdf09a62ab44ffab2a10058156dc336ea087cf3a73258758d9bc541ff85`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 48.4 MB (48376965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dbd61395bd6666c015e62c5fd23a5924635a999daa18e84a1346004e8e1a3fe`  
		Last Modified: Tue, 30 Sep 2025 00:16:35 GMT  
		Size: 11.5 MB (11549370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b39194b1de3ff41fb77cf0e8d5c69d997b6d0ca8d0a35c644b1ed207e9ef0a8c`  
		Last Modified: Tue, 30 Sep 2025 00:16:34 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a410d8cc2f19fa3ba9214b113c6f21d9fcf24c60ecacbc24a8352834dba93dae`  
		Last Modified: Tue, 30 Sep 2025 00:16:34 GMT  
		Size: 267.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1abee6b364777d5c62b6c23d22cb7f9c3d6718362d6fedc11ac022176f6a032c`  
		Last Modified: Tue, 30 Sep 2025 00:16:34 GMT  
		Size: 89.7 KB (89745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87144e73ed6f2011ee26137d4e17657da8fa9cc9fe23524733fc900fc0c488ce`  
		Last Modified: Tue, 30 Sep 2025 00:16:34 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c56ddafef222795b2c3e6d957988422562cc939522972b2cb37df0c29252914c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3591195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1397b37b2621de8dd3b31e24bb65583e05fb53d4bed8e7250620d68d1ccbbc83`

```dockerfile
```

-	Layers:
	-	`sha256:de1436e767210397db0ce0822cdab812243cbf01b60f76a691141e21d30f7036`  
		Last Modified: Tue, 30 Sep 2025 22:08:32 GMT  
		Size: 3.6 MB (3575221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fa86c35f97f132f3e730b9933892b76c47a6fa9c0a40ba58e5fdbac4999fde9`  
		Last Modified: Tue, 30 Sep 2025 22:08:33 GMT  
		Size: 16.0 KB (15974 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:d1bde026937e1caa698288efc4bf2f902fd5bfe8b097761380ce6579be8032c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59869395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcb38a560199cd70f43b3312deafda4e8d7630784a47d462c8d463746c3e2f43`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:f5aae340a376cad680dc8a41a7fd30a241ed4bae3e53125ebb424c8fc7996aaa`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 48.5 MB (48487991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c092a798258bf5d2b4e17d2853d10750c62f97c4fec6e26c8f61a18048faa488`  
		Last Modified: Tue, 30 Sep 2025 00:20:12 GMT  
		Size: 11.3 MB (11287724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64c43273a9ef2841db6b6ee9ceda6265917ad0b4211e8dc8a73519452685240`  
		Last Modified: Tue, 30 Sep 2025 00:20:10 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c947e3e247e08b3dab92c27fa882b771a9e33723d806b99a38f2d9b6495c5fcd`  
		Last Modified: Tue, 30 Sep 2025 00:20:10 GMT  
		Size: 267.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19175cb6fd3b21039e84ae39127512e4ead20fff2e78168aa04774a7596db3bd`  
		Last Modified: Tue, 30 Sep 2025 00:20:10 GMT  
		Size: 90.4 KB (90364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:856eb2da076a53a597a999f69ea08fd82bb2f890cc19581f2c0bc711d7c494fa`  
		Last Modified: Tue, 30 Sep 2025 00:20:11 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b7736fd4bfb116c8139cf451e99b821ca0b9886870a735e3a7840ce9cc0ab970
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3592211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9266b19a490b3159cd1b28ecdc40fb5c2597eff1c423e64dc7fb30105fb8f979`

```dockerfile
```

-	Layers:
	-	`sha256:55817bec929f30eee7545d679faf2afe6560b5846b64cd31c32ae3959a53caa6`  
		Last Modified: Wed, 01 Oct 2025 13:08:04 GMT  
		Size: 3.6 MB (3576097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76054e24cd08c07a3c052d751bc685a37453495f14f7032391965a4d9a083ca6`  
		Last Modified: Wed, 01 Oct 2025 13:08:05 GMT  
		Size: 16.1 KB (16114 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:83aacc7fb7b5c65ca54a080818e9df1beb9e2835d71400afb8c936d0be0596c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61496540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d626ce9d4f2fad6eab9d8e779976d51889a33cfcdd0cdf4d001d569d28c47a8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:d00269cb73b9e4cfebd155b431da849e0072689663a0a658044389a50f9d989d`  
		Last Modified: Mon, 29 Sep 2025 23:35:17 GMT  
		Size: 49.7 MB (49686171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e44f7b83abd8b70cd2ad8be2342045f1278f361d52d006293b6138988a57d04`  
		Last Modified: Tue, 30 Sep 2025 00:23:18 GMT  
		Size: 11.7 MB (11716994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e53eb5296e1a4de069da153195c7ba4f193ae52135e2fe3e4f00df0a32fabf`  
		Last Modified: Tue, 30 Sep 2025 00:23:17 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543f65dd046c1052fda8eb42005bccd5b42eab0bb6d48a74c2ba1fb663bafe25`  
		Last Modified: Tue, 30 Sep 2025 00:23:18 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d55663231e76515c4e6592b762a96895630954a6b668a4b634aba4b9391b3dc6`  
		Last Modified: Tue, 30 Sep 2025 00:23:17 GMT  
		Size: 90.1 KB (90053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f46582ec95217b2b184925612b84924c68c5346b759bdb1ab3841815dc207c91`  
		Last Modified: Tue, 30 Sep 2025 00:23:18 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:cb6e5622e428e267adef0d79727976efc8d4b353bca077aac7912d8c1e7d8390
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3589126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:519927b36064e015e1e86af0b2f1d9ab668b2d6045b87467db30fafc83bd1b8a`

```dockerfile
```

-	Layers:
	-	`sha256:73cd775764b53a6df1791f2a63e44e371b862cc68aa1b9f35d6e5d6dcbf5f8ea`  
		Last Modified: Tue, 30 Sep 2025 16:08:29 GMT  
		Size: 3.6 MB (3573184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1dbad6618782fdb70a1e53631f2316732918e54a51517310778994fd40f091f`  
		Last Modified: Tue, 30 Sep 2025 16:08:29 GMT  
		Size: 15.9 KB (15942 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd110`

```console
$ docker pull neurodebian@sha256:9aabbcc9e03997c57e0e300f2dadd2fa342925bacd78e396ab2dedb03b289cf4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd110` - linux; amd64

```console
$ docker pull neurodebian@sha256:90176f97fbeae11e926a4772950ecca10e2cac52014b8440880689769c3365df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64964683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dc82a44200c756333f5b555fe7a18517fb0e92fa14bfb8e939dcea79230bdb9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:10ffc47270cd106d2d04bc7ef4749d579620e45a84804ba3b18f0898fe5ecc64`  
		Last Modified: Mon, 29 Sep 2025 23:35:07 GMT  
		Size: 53.8 MB (53756064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60bb421a4930e2bcfde978696c830086d079aab35ba1c99347833f8e9a58469`  
		Last Modified: Tue, 30 Sep 2025 00:15:28 GMT  
		Size: 11.1 MB (11105090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad624fd3765fa4362c54e7d7902aa10f74f77c89e10c5d6f4ef3738e7f4c924`  
		Last Modified: Tue, 30 Sep 2025 00:15:27 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34af5c9cf74d548174fc198db4c5d1e164a0a4675bd762f300faf38c09c4aea`  
		Last Modified: Tue, 30 Sep 2025 00:15:27 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b05496266e0f403e0eb9aea321c1dd77f9ac29cbc5a578e7df7394f0feacc0`  
		Last Modified: Tue, 30 Sep 2025 00:15:27 GMT  
		Size: 101.4 KB (101371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:959217a3a17ae0564029e292b48857c19adc7ab08ae21997f5e0bcf249e41801
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7a4fbfb290dbb27ae2e4c6f7927eaf589c86f437d64babd113afa7267425ab8`

```dockerfile
```

-	Layers:
	-	`sha256:038d0e059dd82b17c302359aad44c9de40c94e27e145ad3bb728283a6f7d6539`  
		Last Modified: Tue, 30 Sep 2025 22:07:33 GMT  
		Size: 4.4 MB (4367914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c8330d706ce39305f99b9284e3c88b0e8f8badbe1f221270ced21509706c480`  
		Last Modified: Tue, 30 Sep 2025 22:07:34 GMT  
		Size: 14.0 KB (14009 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:f1193f6efd10b3ab983be1a8a64f8bc1f80d64b6949e54e7176c742e507da012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63466646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:834c95321290bb80fbb943362f7d5a102ce1d13661db32987817f139a63ffe9b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9b16ae1bbd1ada84c12528379a10e280bd89e0d0332670c8487145eb77fe2fe1`  
		Last Modified: Mon, 29 Sep 2025 23:34:42 GMT  
		Size: 52.3 MB (52257414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:894e91d8dba15a3b763b66d3e1fa907c20e5798df7352d17a02c86a54ef49ef7`  
		Last Modified: Tue, 30 Sep 2025 00:19:07 GMT  
		Size: 11.1 MB (11105918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3ab01a5490af9a96585cc987dda6c3647ecbe6bd654e7fa53a48456dc97af64`  
		Last Modified: Tue, 30 Sep 2025 00:19:05 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b8850b1568c65c1aa3203524d059ed21067c8acebb918b2d7edba05cebf6cd9`  
		Last Modified: Tue, 30 Sep 2025 00:19:06 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9730b5ce5d13b5fdc73c132e2c8eaf827181f95f4c53bffa8a19c565e7050f68`  
		Last Modified: Tue, 30 Sep 2025 00:19:05 GMT  
		Size: 101.2 KB (101158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a9f859b786dd71ef74ce084e33053506531d50099df8ef357b1b521ca1cd7be2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb590ba3ea81ff5639de89ef0cfb6494e61d1ee64b8bda8dd09badffbb1ae10`

```dockerfile
```

-	Layers:
	-	`sha256:f53ebc9df093206078615000382c88d27601d1455ca54a8a0d09fca5be751a18`  
		Last Modified: Wed, 01 Oct 2025 13:07:27 GMT  
		Size: 4.4 MB (4367521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6ce6012efba0aca6b0600413c568d14a40e8b6d8cf7135dfd38e876c53a4cf4`  
		Last Modified: Wed, 01 Oct 2025 13:07:28 GMT  
		Size: 14.1 KB (14133 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110` - linux; 386

```console
$ docker pull neurodebian@sha256:91101fc62f0e126e1cd22b32c58d8f9050a812c29710e233482ecddbaa252743
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66303068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e90773363c7472474f497049af1b4f0ea7b8fbed01c137c1aac71338c994a672`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ceabdec1cb201cbc144cbbf99606ecccc3942e0acc3ede261d7cced4e3f632e8`  
		Last Modified: Mon, 29 Sep 2025 23:35:34 GMT  
		Size: 54.7 MB (54699245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3377e521b27619564766572ea2f71b3559921ec242fbb887b220fd8413a3b667`  
		Last Modified: Tue, 30 Sep 2025 00:22:13 GMT  
		Size: 11.5 MB (11500396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f01d1de35df3c14a84ad0035183ed7c1104b2e5f80f45b2a9683829e522e075`  
		Last Modified: Tue, 30 Sep 2025 00:22:13 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8509e7b4bc6ce3aa5251a6dae3ad32ba389a23454d4b7adcc4c92228bf4f98fb`  
		Last Modified: Tue, 30 Sep 2025 00:22:13 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac8c536f22ee766f2f5e553467d1f35b363ded878c8e388bfe44b6499783cb0`  
		Last Modified: Tue, 30 Sep 2025 00:22:13 GMT  
		Size: 101.3 KB (101271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c76db36b16162a08fa0701b63ebd9bf847665060b220f003398bc6540ab20860
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4378414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d596924761808ea21d556fd70edd740ecb7db21d97fa41c4b2417381b5a578c0`

```dockerfile
```

-	Layers:
	-	`sha256:e2158b5c2f5dc79e1ae0eabfd7db426b9ae47d1458b5ea2e06392f51c07385dd`  
		Last Modified: Tue, 30 Sep 2025 16:07:37 GMT  
		Size: 4.4 MB (4364433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63a36ec09f808d990c39e454e9b1784b06d6f3c68279f34ac45742f93eeda259`  
		Last Modified: Tue, 30 Sep 2025 16:07:38 GMT  
		Size: 14.0 KB (13981 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:006bb654698876390f6861a0e01bc503f5089f6e891d33d3e93608e93295b9b6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd110-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:ed53fdb5e8aa47b66a22d8e538658ebad6098cf08a563bc4364b74cbaf364af8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64965079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30dc7efdb549d31a79c7a7c2d7d9835c314a974733e6e4bf0eace26b5e2a4b01`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:10ffc47270cd106d2d04bc7ef4749d579620e45a84804ba3b18f0898fe5ecc64`  
		Last Modified: Mon, 29 Sep 2025 23:35:07 GMT  
		Size: 53.8 MB (53756064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2fca013c373c9ce58b6cae21ac454c7d47366050a594e13b8250f10afe79b75`  
		Last Modified: Tue, 30 Sep 2025 00:15:32 GMT  
		Size: 11.1 MB (11105101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5638541c3cf3d2a86eac6c5fcc3ffb9b67a57a9bf46c7182aa0c4e311665bdb5`  
		Last Modified: Tue, 30 Sep 2025 00:15:32 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499ba193c40041c0e5fa201d166aacdf33b0beb97469f81b7a403ada1b74aa64`  
		Last Modified: Tue, 30 Sep 2025 00:15:32 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cc132915d360c4f2d791549fd2ca2f013a650e235933b950b6ea0d7fffde166`  
		Last Modified: Tue, 30 Sep 2025 00:15:32 GMT  
		Size: 101.4 KB (101370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d96ede1e50978e8f730ea66b147365e342f86943fe800c73171995596daa40f`  
		Last Modified: Tue, 30 Sep 2025 00:15:32 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4af9a206596649c0e27466361f63c4c1a81826669a33c4bce29a21db8fb07424
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c73b451f85aca4ffbd5a0ea300b70f779265df1295afa1807295ddbcd3dc7b`

```dockerfile
```

-	Layers:
	-	`sha256:d9759dd16036ea272c06141d4b727faa571738fcb11840b1e3f52dddcaf0e3c3`  
		Last Modified: Tue, 30 Sep 2025 22:07:38 GMT  
		Size: 4.4 MB (4367950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4b0a72aaf5eddf29cbac0cfad24af7f1f15d3cce4607ecf2e443ecd47fdd859`  
		Last Modified: Tue, 30 Sep 2025 22:07:39 GMT  
		Size: 16.0 KB (16037 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:1f30c996b1974cb30d1db39be8e14d35af351b8c84dccb11cf951e3cc9d9f1ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63467126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:718623496dce620b8a091b46c678973300bfa6e35ec5b7adc0220eaa71a28437`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:9b16ae1bbd1ada84c12528379a10e280bd89e0d0332670c8487145eb77fe2fe1`  
		Last Modified: Mon, 29 Sep 2025 23:34:42 GMT  
		Size: 52.3 MB (52257414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e503815c3695e065c3bfebbe02e4ca6522e055f3d2811a15fbf0f7e671f7fe9a`  
		Last Modified: Tue, 30 Sep 2025 00:19:14 GMT  
		Size: 11.1 MB (11106034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74f4b86a4499aeaa235b1bb5c60fa3f1f0a538facfee71bd3bffeedb937421b7`  
		Last Modified: Tue, 30 Sep 2025 00:19:13 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a7c071199696c6bc66c27249bba23d3d61056f23bfd53331e3490c87150eac5`  
		Last Modified: Tue, 30 Sep 2025 00:19:13 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6374e812d78ea9095cd594a1ab8c52c5a1438b0e9701b7b90c66ffedf3bfbb15`  
		Last Modified: Tue, 30 Sep 2025 00:19:14 GMT  
		Size: 101.1 KB (101132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d983cf93511e8b9e722d857bbb40a47af2452461f6c49fafc915752f11dd59fc`  
		Last Modified: Tue, 30 Sep 2025 00:19:14 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:aad05f3c3dc155bb3e1cf0980fb82714fda5e4ad24ab9e3c31b7b0271f23d4fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6776e87ce097931b04f1195033a91a66a08f69df9c7afaf23fd077ed706a38cf`

```dockerfile
```

-	Layers:
	-	`sha256:f149e404fb039204918eb81df1083ab7710e02a97e75ad9a80312a7ad77fbb99`  
		Last Modified: Wed, 01 Oct 2025 13:07:33 GMT  
		Size: 4.4 MB (4367557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d584879ab879bad46254130981389b7b21180def03e30acc6871281df46d3102`  
		Last Modified: Wed, 01 Oct 2025 13:07:34 GMT  
		Size: 16.2 KB (16177 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:4eea0d4fd77d66b5b2802a7722eeb5fb2109fb7a02966f5d8635d076cda4536a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66303456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:542a028b735297cf6aaa7fbc7248c5fa8f08bb0f6a5152c346243217df1be188`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:ceabdec1cb201cbc144cbbf99606ecccc3942e0acc3ede261d7cced4e3f632e8`  
		Last Modified: Mon, 29 Sep 2025 23:35:34 GMT  
		Size: 54.7 MB (54699245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3377e521b27619564766572ea2f71b3559921ec242fbb887b220fd8413a3b667`  
		Last Modified: Tue, 30 Sep 2025 00:22:13 GMT  
		Size: 11.5 MB (11500396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f01d1de35df3c14a84ad0035183ed7c1104b2e5f80f45b2a9683829e522e075`  
		Last Modified: Tue, 30 Sep 2025 00:22:13 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8509e7b4bc6ce3aa5251a6dae3ad32ba389a23454d4b7adcc4c92228bf4f98fb`  
		Last Modified: Tue, 30 Sep 2025 00:22:13 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac8c536f22ee766f2f5e553467d1f35b363ded878c8e388bfe44b6499783cb0`  
		Last Modified: Tue, 30 Sep 2025 00:22:13 GMT  
		Size: 101.3 KB (101271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4e1e7d055597b7ae7b2fb8e3c043ee71c83f9caffb518b6a538a65f2c12f729`  
		Last Modified: Tue, 30 Sep 2025 00:22:19 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:99aaca37cdb012e66ae234bdb48111ffe493f7bf2d722d6de4fdc301d88509ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4380476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:337428655da965ead524ac77fe7953cb70305e76c5a4b1741367f923e55a810f`

```dockerfile
```

-	Layers:
	-	`sha256:c18dc37b060df10df4047be8729a361fc8895477639ac9b8c869cb13d6d9a49b`  
		Last Modified: Tue, 30 Sep 2025 16:07:45 GMT  
		Size: 4.4 MB (4364469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13d12e9ab20c1ea4a6f193720b7539452b9adcc7655702e761d5bf73575fe789`  
		Last Modified: Tue, 30 Sep 2025 16:07:45 GMT  
		Size: 16.0 KB (16007 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd120`

```console
$ docker pull neurodebian@sha256:3781817d913ee5d56f77887c10cc8cf42516c30683672a6ea4f7a8b432d2b0c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd120` - linux; amd64

```console
$ docker pull neurodebian@sha256:05aea33b07313b18ed01de4ab2ae06ed9b2d546335a1f9327c0bc995e5b83a64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59845703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7dfc8a55839663157a6aba43127208ac15cfb53aebb47042d2903aae22db74b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c6b11972fd12973831818babf60f1ffc1c4047507943d132dffc612884022858`  
		Last Modified: Mon, 29 Sep 2025 23:34:14 GMT  
		Size: 48.5 MB (48480557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e22dfc9371bd5451b52aa68b5daf06dfef29d6542df8b0fe5b7d20e9433b477`  
		Last Modified: Tue, 30 Sep 2025 00:16:14 GMT  
		Size: 11.3 MB (11269611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bbdeeebd686778d37b510ade531322cd97c929d72c59f001b9c8fb1f3d73c24`  
		Last Modified: Tue, 30 Sep 2025 00:16:13 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d874806bdf8c980e824c490f339970b81ff02843afe86de3cdbfdd45425b58fa`  
		Last Modified: Tue, 30 Sep 2025 00:16:14 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2a9e79214196194656296b10f16d9dc952464f9530672c37a1581933dc0d57`  
		Last Modified: Tue, 30 Sep 2025 00:16:14 GMT  
		Size: 93.4 KB (93363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6675649918c8891c0b7dd5b1384c9e7658e704541ed2c3f724b71056993a5271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd658c8e894a97cbf19d656d7b994f751ed624b572d963d9854cc18104f4b05e`

```dockerfile
```

-	Layers:
	-	`sha256:3fa0b54726e2c21f1537172fccbf34d53eadede1db4a89b9b838c78e1c33fd46`  
		Last Modified: Tue, 30 Sep 2025 22:07:23 GMT  
		Size: 4.1 MB (4075236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac555dc0da90f76cefef7f44c9e57d8d91f1ec3f36cba41b730becebeeeb0447`  
		Last Modified: Tue, 30 Sep 2025 22:07:24 GMT  
		Size: 14.0 KB (14008 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:885d0432b840a960d2af3a81ca5aae885bf5af08cd61088845e8b8dee0794d04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59708030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95661854959d110a69764b3cc43078b7ea99cf1b5597dbd1d96e37078f5d0c25`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f7b43f0d0a8b99591b27457b368e70a582002600d32503fd07798c1bee7cd134`  
		Last Modified: Mon, 29 Sep 2025 23:34:16 GMT  
		Size: 48.4 MB (48358915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59ee3668b41e5cd78c1271f8a55ff6c7f79be607b3881f0e810b053d2a59879`  
		Last Modified: Tue, 30 Sep 2025 00:19:38 GMT  
		Size: 11.3 MB (11253411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e21facce03c416f6b6b038ea1567e13187e8f88f83543487d66645815aa592c`  
		Last Modified: Tue, 30 Sep 2025 00:19:34 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a91a5654acaa81767b1cb906ed6e1b298ed98d03e537ce98a6a02c7ccae2647`  
		Last Modified: Tue, 30 Sep 2025 00:19:35 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:005232c823dc70fa622ff0308fa6bb27a5669e98a6559e582866767a89e77b59`  
		Last Modified: Tue, 30 Sep 2025 00:19:36 GMT  
		Size: 93.5 KB (93533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:cf061e895233b68256d177410cbec7182e037423d8bf0f05cf3b93926d77dd51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac60b8863cafd48c3cb4e1c0a16d6b174a586477c25b7b152c934539e292e41c`

```dockerfile
```

-	Layers:
	-	`sha256:e2002f290029233141183075e6c0fc0da5834fced553d054504439a296895855`  
		Last Modified: Tue, 30 Sep 2025 13:07:27 GMT  
		Size: 4.1 MB (4075478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82755eaef9819ef6f197394d209dcb151e24a5f15bc29628c34abd4fbcf1e4da`  
		Last Modified: Tue, 30 Sep 2025 13:07:27 GMT  
		Size: 14.1 KB (14133 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120` - linux; 386

```console
$ docker pull neurodebian@sha256:d91e3880a0b832816150a13ad8aa9d5416a824b9da76477c9d2e8d9f32196349
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61252347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acddad54a54afb1f7a64db74d90ee9619a6f00598c1138fb05a3f4fc215d15a8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2212ccc79525753c3f36994bd936e194dcec09d69b21786be4caa60f697693d8`  
		Last Modified: Mon, 29 Sep 2025 23:34:26 GMT  
		Size: 49.5 MB (49466651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0fcf493e69eb4a8834c6f5d1209b483a9fa5de2fea0f19cdfc81de3c993f8a8`  
		Last Modified: Tue, 30 Sep 2025 20:21:23 GMT  
		Size: 11.7 MB (11690118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39be09859d19045ac15d7973f5449ba6128d3d33572d45507258428bf2566fbc`  
		Last Modified: Tue, 30 Sep 2025 01:17:21 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d33ed3c56380c617c61fc605987c9f6777075d5c303725f30d16f583b3c585`  
		Last Modified: Tue, 30 Sep 2025 01:17:20 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1419c195a2730d5dd40aab25b98cc1613239f1eeba9b4caa91a54e65104fcd03`  
		Last Modified: Tue, 30 Sep 2025 01:17:21 GMT  
		Size: 93.4 KB (93405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:919fbfc5f19953bad4e8d0116debfc9cee19d0a5bc03352cc45ae2fb1b96c479
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4087184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3b4ed69573c34fa3235d349ff3ff520ada93cb39f70becc9e250b577e319c58`

```dockerfile
```

-	Layers:
	-	`sha256:2f7f73fd5ce5669e280c57dbf3cdcf3992d91ca2d295130f6d7ef2d4f7c7765e`  
		Last Modified: Tue, 30 Sep 2025 16:07:26 GMT  
		Size: 4.1 MB (4073204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2806288d1c706feaca2efff856a8e800bed8536a2032d8951927220f8af4de8d`  
		Last Modified: Tue, 30 Sep 2025 16:07:27 GMT  
		Size: 14.0 KB (13980 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd120-non-free`

```console
$ docker pull neurodebian@sha256:d862dd1dc8d155384376cced3c739f8342968dec401b3ebdadbbf3371e2f3e84
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd120-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:22518b5f38f00c2114e97b3187d585db438685a05930a18785e5b3adb73f6a1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59846138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55c97b3032259eac465ebf0c8ffe17b7906d09a91ee3ea949fd9dded523db104`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:c6b11972fd12973831818babf60f1ffc1c4047507943d132dffc612884022858`  
		Last Modified: Mon, 29 Sep 2025 23:34:14 GMT  
		Size: 48.5 MB (48480557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eedb6694c64cae843951d54e2b05e2610566e3fca8973c074796b9af8a498c77`  
		Last Modified: Tue, 30 Sep 2025 00:16:13 GMT  
		Size: 11.3 MB (11269576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e794520964c3a381276cce16943b4362333efd5977a64c5fbf154c77b6015c2`  
		Last Modified: Tue, 30 Sep 2025 00:16:13 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04fc78f7af59fd7cb66064d2b76dac7beff22e85aa7dccb731fa985ed7217c7a`  
		Last Modified: Tue, 30 Sep 2025 00:16:12 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7265c0ebb450e80f788f289e5b00ec5e5704aea9278a33f4c5ed429a4c20df73`  
		Last Modified: Tue, 30 Sep 2025 00:16:13 GMT  
		Size: 93.4 KB (93384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2065cea84fab934fcd1190024d9ddaba19177d1f00876c2ebb45a42ae19c4e22`  
		Last Modified: Tue, 30 Sep 2025 00:16:13 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f8b4ff6a2b23ebfcd87f18355293fc60648ca9af372ce29c6507b0427f7ac9cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4091307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ebf7e694489c6fbe6ffde1e32ef3bb99627d8f861c8bda8b0918f984935bb86`

```dockerfile
```

-	Layers:
	-	`sha256:b614fb6a5adfe55efbafba13c46d348a4d8670764d9d9a5ea0205ca21574afd4`  
		Last Modified: Tue, 30 Sep 2025 22:07:28 GMT  
		Size: 4.1 MB (4075272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c25191c38856398fb7ad3b288b257d6f3e09f8978cd82e718e4dd7a99c56489`  
		Last Modified: Tue, 30 Sep 2025 22:07:29 GMT  
		Size: 16.0 KB (16035 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:14c6af47ab2eb20d548a33b4950a8064cadf5103151dbde85721d736f7952549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59708446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:770036e294af01f132221eff46d03aeb9fd3ab8e68aedf7708ed786da2cebceb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:f7b43f0d0a8b99591b27457b368e70a582002600d32503fd07798c1bee7cd134`  
		Last Modified: Mon, 29 Sep 2025 23:34:16 GMT  
		Size: 48.4 MB (48358915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3898d44334f1abae852d530a5cade80ec1ebb870e449f5b99d9f961a5315a02`  
		Last Modified: Tue, 30 Sep 2025 00:19:22 GMT  
		Size: 11.3 MB (11253407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb9ea5bcd6e7676c1d1f0aa5b1f1be9505c317be092c246d08ef9e756cbfcbc`  
		Last Modified: Tue, 30 Sep 2025 00:19:20 GMT  
		Size: 1.9 KB (1897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ff8510b562165af3eb589e1fafdc7f2085c9e55c53a0d8875f05a9001553bf`  
		Last Modified: Tue, 30 Sep 2025 00:19:21 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b122a4615dd127bcc9eda078ce123a341c4fc07f38436b92fe87e539ecaa528`  
		Last Modified: Tue, 30 Sep 2025 00:19:20 GMT  
		Size: 93.5 KB (93508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a496b42997f524257237886d80a6f9fd59724b091a359ed42eb3d1f81b79ea2c`  
		Last Modified: Tue, 30 Sep 2025 00:19:21 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c13213fed3c5367640f48587d9c907be8453bb8585766bf1f5031f2d0df72438
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4091689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e6466a096093118b0e12f98547696e397648ac394f697616c6ccdf2feb87515`

```dockerfile
```

-	Layers:
	-	`sha256:03f9b0f7f7c935c94de22d574f043cc96ee44e8f1f089633c7290bacd55b2cae`  
		Last Modified: Wed, 01 Oct 2025 13:07:21 GMT  
		Size: 4.1 MB (4075514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee16f24e2006c7d9bf4faa0d7e58ef704cc6e5c6fad6790fb38d2403ecc35c06`  
		Last Modified: Wed, 01 Oct 2025 13:07:22 GMT  
		Size: 16.2 KB (16175 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:274603d10dd008ffaae3f5a404c2cb78e59ecd5706eb12e88af53bf598a57867
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61252715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fe2e21fcc30f1784d46cc228997afb47e22ffedd4a368dfcf05b81367454dfc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:2212ccc79525753c3f36994bd936e194dcec09d69b21786be4caa60f697693d8`  
		Last Modified: Mon, 29 Sep 2025 23:34:26 GMT  
		Size: 49.5 MB (49466651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8003e96b9e94adb93fc76f0aba6b61a61d93076bed93f875ac3df4c3b0774a6e`  
		Last Modified: Tue, 30 Sep 2025 00:46:13 GMT  
		Size: 11.7 MB (11690057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f40fff84c9df9d31e2e7597437f764b596d6d5cc1c91b257231aea263e70a9`  
		Last Modified: Tue, 30 Sep 2025 00:46:07 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a8e013318eab027adcaa49bd9383346d072bc458f9f83465706840e91c6917`  
		Last Modified: Tue, 30 Sep 2025 00:46:08 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66354afb13fc7968d1d014d293a2852ad99c3cd01320d7aeb89677a34f189aa1`  
		Last Modified: Tue, 30 Sep 2025 00:46:08 GMT  
		Size: 93.4 KB (93386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc70e80f96db7f036acc3d8b7e90b499de2481acd8fd1bfba443b9576700b711`  
		Last Modified: Tue, 30 Sep 2025 00:46:08 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a747702e7ac618c28924fff29384270841e58c2067491ed6db76abd16c244529
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a5eed2cc266a48e5259b2e7b9f08ec4d7cd2d6b99b22fe48f61fd62c376106b`

```dockerfile
```

-	Layers:
	-	`sha256:36458e6b34117b91d12dcd4244f4588605c8a0db6a8649b262ee724e880f54aa`  
		Last Modified: Tue, 30 Sep 2025 16:07:34 GMT  
		Size: 4.1 MB (4073240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e511c629df67a5cfedb1431796c40d83cf94f446c340de58678f642dfff2d9b5`  
		Last Modified: Tue, 30 Sep 2025 16:07:34 GMT  
		Size: 16.0 KB (16004 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd130`

```console
$ docker pull neurodebian@sha256:87693cfb664c3983f3e574e1dcd5b58f82fd2618b8af3a364767508759c8e2c4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd130` - linux; amd64

```console
$ docker pull neurodebian@sha256:5445400c594afd56d8608d270c0e840a5bdc8ce8eed14c50875b111ece8c8967
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59667200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1692c2ad0959aff9134072de309c7092e4303f34bd66175926b4536f01737b1b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cae3b572364a7d48f8485d67baee38e4e44e299b8c8c4d020ff7fb5fdd97f88c`  
		Last Modified: Mon, 29 Sep 2025 23:35:29 GMT  
		Size: 49.3 MB (49284626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf661b2ff63805151437f18c9fddf545dc18823488c0dbe851eafeba8066d82`  
		Last Modified: Wed, 01 Oct 2025 00:26:33 GMT  
		Size: 10.3 MB (10289495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030c7393f1d0600f3d5801fa9a09be77c972b3bf6cec3d9a0ceee41e16f80f79`  
		Last Modified: Tue, 30 Sep 2025 01:05:19 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7679f2a094fcaa509ff0dbff39c2f33e8f9ee67eba015e63ec580599369bd963`  
		Last Modified: Tue, 30 Sep 2025 01:05:20 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5fdaff3323992c80159a90ce241b8c1e2eecfc50b87e4e1f570519c04063c53`  
		Last Modified: Tue, 30 Sep 2025 01:05:19 GMT  
		Size: 90.2 KB (90176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130` - unknown; unknown

```console
$ docker pull neurodebian@sha256:11379453b3c698293768b9d690e1a7e9d3b6991a688f6f2c6c9d46d25b7a1999
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3627275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e291424f296bf0582d068b79c4a19e3cf1f75fa0e7f7d4051e57733efe754ae`

```dockerfile
```

-	Layers:
	-	`sha256:a5d6e8b4a14ee685087c48f425191d4046aecfdc2e2dce91edd6ba320a8a65b9`  
		Last Modified: Tue, 30 Sep 2025 22:08:37 GMT  
		Size: 3.6 MB (3612981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cba41c16a9c24d09b71598c74915dea63db262a1a93abcbc3f0d247b9b4c11c2`  
		Last Modified: Tue, 30 Sep 2025 22:08:38 GMT  
		Size: 14.3 KB (14294 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:5d39e0ae09097ede0b7dcd605763843cc32f5d004f39cefe691f3534fcabf107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59815441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d12c54dcf7bbe6d3551a1d49ac956e0b9ef7c361391bd2511992d7c2ba5cc6f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:28aec8b14b3eeacbf47ef38af72fab694b109fdcdf31581722750599baf1a932`  
		Last Modified: Mon, 29 Sep 2025 23:35:17 GMT  
		Size: 49.6 MB (49648695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b6f6da96540c9f6cf298b7b364c63b1cf0c3929b805fed831b6c1c3eae4d87`  
		Last Modified: Tue, 30 Sep 2025 00:19:26 GMT  
		Size: 10.1 MB (10072980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a478dfca60a2c33636ca722a574ff603abd3fae381c95be0c7bf68323a3704`  
		Last Modified: Tue, 30 Sep 2025 00:19:27 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5474e962acd88276c7b9fa402cc148afe511eddb2832d559ea63b51fb720b0a`  
		Last Modified: Tue, 30 Sep 2025 00:19:28 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094906ccc10fa032c3efb4b206bda6edbedb9eca7903daa2ebdf676a5f615361`  
		Last Modified: Tue, 30 Sep 2025 00:19:28 GMT  
		Size: 90.9 KB (90866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2be449b53fb3b4125c74bfaf49a273c82589056f7a7b58ced28d693d35ecfd68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cf5e15992d5473686642c610909b239be7d6cf3f13bcfccc273a3f7cd5cd553`

```dockerfile
```

-	Layers:
	-	`sha256:ea9f419913ead7a4c0e010568c2d3864423e07529314b03a43cadf13070d7ebe`  
		Last Modified: Tue, 30 Sep 2025 13:07:45 GMT  
		Size: 3.6 MB (3614508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08e6d045cefb6337ce69dbe9c61d5d154f22a2ddc355e21d8fb66a2d9f615939`  
		Last Modified: Tue, 30 Sep 2025 13:07:46 GMT  
		Size: 14.4 KB (14431 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130` - linux; 386

```console
$ docker pull neurodebian@sha256:8a46319c2bee6856b4f764ac30025c5587a5ee243fb31b30dbfc8d7fdbaa6d9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61356323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35e989f30d27cafca9de5bdca46f6e0f4139c1fd7362a134d113c77557fab4dc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f1c1f592b5569b5e2093c3107a48f2929b609f05af6d24c06d41a7ec1ae5e0e1`  
		Last Modified: Mon, 29 Sep 2025 23:35:36 GMT  
		Size: 50.8 MB (50800229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ab973589bc45010616b19754c3c69e0ae9f8ca8970197b3299d394ea33f588`  
		Last Modified: Tue, 30 Sep 2025 00:23:16 GMT  
		Size: 10.5 MB (10462616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3efbe96c0b7cb9c8886f791f5343077fbcb6ee8bf991286ebe52cab58d6cc892`  
		Last Modified: Tue, 30 Sep 2025 00:23:04 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dea642e4992382c23719b878885f48c32247f1f5867d347ad4c22d63c0a8720`  
		Last Modified: Tue, 30 Sep 2025 00:23:04 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6ae40746c8c652627ef29267be656c50aab350b775d26b475917c7e2742ed1`  
		Last Modified: Tue, 30 Sep 2025 00:23:04 GMT  
		Size: 90.6 KB (90577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130` - unknown; unknown

```console
$ docker pull neurodebian@sha256:01edb6d5394be68b0049fb213c5711380de11bbe71bb915c1a99290309011366
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3625191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff7b3eabd530054c8c1027eb5ff3de1c92acd70f4dac5652e04a574e629a340c`

```dockerfile
```

-	Layers:
	-	`sha256:031421d4527aa62b75263e52be1877d3065aa1b9c5575c49b0f1fb55f48c5bf5`  
		Last Modified: Tue, 30 Sep 2025 16:08:34 GMT  
		Size: 3.6 MB (3610930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c15ca298c4f9b159a9a1e17f17ba6bf440488c13b2b3af4a01a92335f30ff50b`  
		Last Modified: Tue, 30 Sep 2025 16:08:34 GMT  
		Size: 14.3 KB (14261 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd130-non-free`

```console
$ docker pull neurodebian@sha256:0d9a4c13d4e7371ad64078f0d671c6383a8f7afdadf6df21e6ea836acc999891
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd130-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:2503ccc01a731af5b2d3d92f7327d9e31bbcb1011139a72879f223a379d18068
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59667538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b4b50aa0579a74bdcbb49a498d7315d494e61327bc54deff97aae76e3b57c4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:cae3b572364a7d48f8485d67baee38e4e44e299b8c8c4d020ff7fb5fdd97f88c`  
		Last Modified: Mon, 29 Sep 2025 23:35:29 GMT  
		Size: 49.3 MB (49284626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f805df92352cae0a0a2836745a1bb53b364d8cccb0a97b47b625e0dde43f3f`  
		Last Modified: Tue, 30 Sep 2025 00:16:34 GMT  
		Size: 10.3 MB (10289390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc43eb24082631f3aec7eb229fe3fb1fd1008d98e03bfbd5a612e46b23ba1e2`  
		Last Modified: Tue, 30 Sep 2025 00:16:33 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3328b63a48e14a4f9831671d91841324f4446ffc7c53aba7cd267daa4b4f80`  
		Last Modified: Tue, 30 Sep 2025 00:16:33 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b20b675e05429ab3c15103ae9009614f1f3725ae5cbad4733ca582901965b1`  
		Last Modified: Tue, 30 Sep 2025 00:16:33 GMT  
		Size: 90.2 KB (90174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1daee8250ea7ba96eac71bc0e2a8bbd64222f6a94bb432c8cd8623a6760f3002`  
		Last Modified: Tue, 30 Sep 2025 00:16:33 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:52e009a03c07d287b8712a89275cf62d910e6f735fb37cc5e7bab8beef1bbe66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3629346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34a745821a65d66b1aa0f33a69d19c1824d420dbebf69bdce4aa51155bb295fc`

```dockerfile
```

-	Layers:
	-	`sha256:458676c72d3376b2e2adc40b027530e16649d7cef3dce4f466fa9eafc5e2602b`  
		Last Modified: Tue, 30 Sep 2025 22:08:44 GMT  
		Size: 3.6 MB (3613021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d73401dfdc2638617c66e6f3c897b4abcb9fd9d44e04be80396ce82befadec0`  
		Last Modified: Tue, 30 Sep 2025 22:08:45 GMT  
		Size: 16.3 KB (16325 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:bb8a1f91ca3dda2b54c613358a3f2f2945bfc5deaafc4eeadb6eae89d044f6c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59815896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8008367a8e867e3902e67f9754a14d41e1c86f389a5a7ecb27933aff25207f1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:28aec8b14b3eeacbf47ef38af72fab694b109fdcdf31581722750599baf1a932`  
		Last Modified: Mon, 29 Sep 2025 23:35:17 GMT  
		Size: 49.6 MB (49648695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f827ec068a53d186059453e246d57e837a733af80e5e8a439634aaa8010cbc48`  
		Last Modified: Tue, 30 Sep 2025 00:19:31 GMT  
		Size: 10.1 MB (10073018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f2c0c542f12345a7b0b7332a3c30fbef3e0f06cb41dab53840a4e12b39a669`  
		Last Modified: Tue, 30 Sep 2025 00:19:30 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb99ddf347a9b9633f0d8033fe5a42e37880b4b2ddaf4bda2922f2c4bc504a8`  
		Last Modified: Tue, 30 Sep 2025 00:19:30 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7514b6a6ce06d47e1c9a211e6c9baac0edbdef4aa535d618f6415f0fbe994a`  
		Last Modified: Tue, 30 Sep 2025 00:19:31 GMT  
		Size: 90.8 KB (90837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73a6f3450e33d6d3354fde8b80a122a9643f6244d174f78222de5bd8feb1a930`  
		Last Modified: Tue, 30 Sep 2025 00:19:30 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f0d1fa2842c899d239f59156bb06dcb2aa6b4017485f5d1418867ab3b772ea22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3631025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfc74683096734fe8a7282c0c86a4b90695de4208566bde26b768822394849ba`

```dockerfile
```

-	Layers:
	-	`sha256:8358e4867b6f7d30ccde76e14fd6bc289cb71cee56a711c57179f8b40eda4b1c`  
		Last Modified: Wed, 01 Oct 2025 13:08:20 GMT  
		Size: 3.6 MB (3614548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7daca65ee14aa6ed1264b3293452c903db18d8777d168fdec82a6219fa454ed`  
		Last Modified: Wed, 01 Oct 2025 13:08:20 GMT  
		Size: 16.5 KB (16477 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:6f5f51db0117943740d24d6272ede6d385cf0de736a0a87db476f1cd373ac423
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61356742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28287d3132e454889d0cb4278309fdd1c117e4946ce49dd56a41083c2539181e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:f1c1f592b5569b5e2093c3107a48f2929b609f05af6d24c06d41a7ec1ae5e0e1`  
		Last Modified: Mon, 29 Sep 2025 23:35:36 GMT  
		Size: 50.8 MB (50800229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b43fce213f96af9285577072bd9752768a9c65a727ec564297271c4fb3dd675`  
		Last Modified: Tue, 30 Sep 2025 00:23:18 GMT  
		Size: 10.5 MB (10462626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e2e09d36685cd8530477135a922a156ccc8bfdf81e79a088f5c4b6bae27c7a`  
		Last Modified: Tue, 30 Sep 2025 00:23:13 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77747ec32ef9084e7a31f53e4895625940080c905fe34a4b4a1518a05da0be5c`  
		Last Modified: Tue, 30 Sep 2025 00:23:12 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afe8cd32135ae5186a68422d3154e344abce87331d1c80a54f49c008cafa3754`  
		Last Modified: Tue, 30 Sep 2025 00:23:13 GMT  
		Size: 90.5 KB (90540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6ade42626c18876d4e066d0491d60ce433a6f3f35060ac999555d4904dbba5`  
		Last Modified: Tue, 30 Sep 2025 00:23:13 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2e53fda5ed32d4582af0d59a52f6053c693f45de5a8593022784d862534f1272
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3627260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cff141d466be7fd3841ab7f3fdd7191cb53a6b2c3df26fa213fd731f4e39ea16`

```dockerfile
```

-	Layers:
	-	`sha256:fac33ea0fa1e517ae03eda600bab1c7ec5b8189b09fe01c651a4f7d35b69e1cd`  
		Last Modified: Tue, 30 Sep 2025 16:08:40 GMT  
		Size: 3.6 MB (3610970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39422b45dea80b7340f8112c3c76282ecdcfd55ec0cbdbbdbf5570d78a2d4128`  
		Last Modified: Tue, 30 Sep 2025 16:08:41 GMT  
		Size: 16.3 KB (16290 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd140`

```console
$ docker pull neurodebian@sha256:c92360ecb28f2f89c85be4dbf26acfe13eab117f3fb4b5207c4cd224a3ebb585
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd140` - linux; amd64

```console
$ docker pull neurodebian@sha256:345b73cc3cff330f591113ad5c395e6f1d6d41737f1aa30d2cd0890eec290e20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60209260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29205c954925c1ecb55bac9ed0b80d21438ff3c4f7a6310eb2538739681d65a7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e4cfa25241b18c60e1d77cc5cfae85a9e13d25b981d6592cf216e6292e3a9555`  
		Last Modified: Mon, 29 Sep 2025 23:34:30 GMT  
		Size: 49.7 MB (49736818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ae5466bb071b4d5fd8eefcee42963b6fb9049be541a84881dc6308e473fc8e`  
		Last Modified: Tue, 30 Sep 2025 00:16:29 GMT  
		Size: 10.4 MB (10379739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1807ebbab503ae80b9399051b61f04755ca3d6aae60f4dc6d425a0bf7720c092`  
		Last Modified: Tue, 30 Sep 2025 00:16:28 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd66df67e8d400f04c58dbc6b030e39a1acf8a05e6146909b24aa7170753dc9`  
		Last Modified: Tue, 30 Sep 2025 00:16:28 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afa15f7f278e086ea0fbfd80f89d1c5006e7335cfc7be13c9460227d1cf6fbef`  
		Last Modified: Tue, 30 Sep 2025 00:16:28 GMT  
		Size: 89.8 KB (89801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140` - unknown; unknown

```console
$ docker pull neurodebian@sha256:852b8be1f7037fff7d287538ad33f1cfc8866e29620587784f5b9d583b107b34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3617518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c24d1eb59953bf3dbf18bc9e6d60ee7930713fcdc584cf97746191124cd2ffe`

```dockerfile
```

-	Layers:
	-	`sha256:85f5c52cfdcf421d688db7359c6af95dcbf0fdc4dae316f1ddff761a459c067c`  
		Last Modified: Tue, 30 Sep 2025 22:07:43 GMT  
		Size: 3.6 MB (3603543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8e92428ab852a3e9d6c4f35263068e7e9d1f55e02615a19121b450e71837a5a`  
		Last Modified: Tue, 30 Sep 2025 22:07:44 GMT  
		Size: 14.0 KB (13975 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd140` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:48ce0de5fa5a7f531ef0099c39eb5a1f0f733aacb5a5202aee0d7072d739771e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60131499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea1ea47940a8675950da1ce2c4198af21b8d44ac640778235f4f68f05ff9bd4f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ed417fd581c20c18b8c6cfc58498c59128dd74498d5d6a89f9217103a4fbf9d4`  
		Last Modified: Mon, 29 Sep 2025 23:35:24 GMT  
		Size: 49.9 MB (49879877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15cff7a9b9fb682e2c2e6993119b846dc5b1d81710a757f010425ecbe1699e49`  
		Last Modified: Tue, 30 Sep 2025 00:20:07 GMT  
		Size: 10.2 MB (10158245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a548c6783d21d82bed7da77c4ca8c4b15bab1a515f2756f4695815fab7b460`  
		Last Modified: Tue, 30 Sep 2025 00:20:04 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9019ec9d5a01b9d86df23fc3e913b0e3cf0c7230ec7d73e3363eaca9b07a6e6c`  
		Last Modified: Tue, 30 Sep 2025 00:20:04 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c21116de06bfade79387d1406dc1f8cb6ecc55f6691c8ce21d819d9994eb77`  
		Last Modified: Tue, 30 Sep 2025 00:20:04 GMT  
		Size: 90.5 KB (90476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e91d5af2acabb5fc1c42402b01c0a6d4077ddbf95ec53c76ab3518d1f502c6e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3619158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:655998c0f6a1a91e187f80b049db97a567ec9001c232239e0970f3e7e5e3f149`

```dockerfile
```

-	Layers:
	-	`sha256:0cd9a524431ae523b0025aa698d246bafd57a0cdad0bbf85884164c814362b71`  
		Last Modified: Wed, 01 Oct 2025 13:07:38 GMT  
		Size: 3.6 MB (3605058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47f001f336ef37958e08b2b08580f72ea63e862ce86e03828d8a1eb665ee3ae5`  
		Last Modified: Wed, 01 Oct 2025 13:07:39 GMT  
		Size: 14.1 KB (14100 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd140` - linux; 386

```console
$ docker pull neurodebian@sha256:93076c4c2d0e94886018f69e1152e8deaf2d4bed3e6efbcbafb955ac2a8821cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61744597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c512496e92c8a2ab4d459299062ede4abcb70e38f111d2e6aa0b505fac923153`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:376eb1520bb62885f5204083862e9559c55db2c2217bc7ae5d95166cd5564cbc`  
		Last Modified: Mon, 29 Sep 2025 23:35:30 GMT  
		Size: 51.1 MB (51119420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a865d211977b3f1fcb807a758d4ec086437dd6673f67e3e1d591e17e58882cb0`  
		Last Modified: Tue, 30 Sep 2025 00:23:14 GMT  
		Size: 10.5 MB (10532079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91719f443526b031661e5a96a385443574e851a066f71ada0666f70884b0e2dc`  
		Last Modified: Tue, 30 Sep 2025 00:23:13 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b17552004c93b6782e1e3a7a419888801d004eedb43de407b78b4ea866fea1b`  
		Last Modified: Tue, 30 Sep 2025 00:23:14 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d093529586e174c24eba4daef5bc737d33409e0ab114788aeeaecda34415aa42`  
		Last Modified: Tue, 30 Sep 2025 00:23:14 GMT  
		Size: 90.2 KB (90191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140` - unknown; unknown

```console
$ docker pull neurodebian@sha256:88c49151d58c1387ab21df41ef3530d5a8bac401ff1fe37dee65a3caaded9855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3615449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bdd154be2b8b9d7924f741cf7a9dddc57d872f8fb9afe3536f35a8960c6cafa`

```dockerfile
```

-	Layers:
	-	`sha256:154737cd4e2fe16fcfe2381c2c77298084a954fbc4a92d2a4987a4f405a1af1b`  
		Last Modified: Tue, 30 Sep 2025 16:07:47 GMT  
		Size: 3.6 MB (3601504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6407fcef5a1ef280b76d26fac524a4f6552d3ed6baa7676692a8c113201710a`  
		Last Modified: Tue, 30 Sep 2025 16:07:48 GMT  
		Size: 13.9 KB (13945 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd140-non-free`

```console
$ docker pull neurodebian@sha256:9eed6b58b84a550a5974629668891a7528c7538bb2eb7c3c961effa4073f6f6d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd140-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:f5fe87c1e1ad0cc109f0cf8f6a9d2c6474eaacbdb1477dfc6342d827eb111f01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60209747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a9184bde64f75bc0898f709fdf492555b74abd3086acfa010bcd4c6dd3130ab`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:e4cfa25241b18c60e1d77cc5cfae85a9e13d25b981d6592cf216e6292e3a9555`  
		Last Modified: Mon, 29 Sep 2025 23:34:30 GMT  
		Size: 49.7 MB (49736818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e573455d7fb5304cf7248f536b62a4140b90208a5690f4a3a85adc6e5547e5b`  
		Last Modified: Tue, 30 Sep 2025 00:16:34 GMT  
		Size: 10.4 MB (10379740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b291dd14f83d964b7f57044bc7f4a04295df37ba77f9fb5dfc9bb9c7de1d8a`  
		Last Modified: Tue, 30 Sep 2025 00:16:34 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2837bde73fa3149d81eb22fd9ff320d18a2c316af16da953569a16018bd3f9a`  
		Last Modified: Tue, 30 Sep 2025 00:16:34 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c5c97b9334b4e50feeaa05190b4476afb1c64d57ae2a3336fbecf4267507ae`  
		Last Modified: Tue, 30 Sep 2025 00:16:34 GMT  
		Size: 89.8 KB (89840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:617c03802ed8fc2f823aeb323ee3010b4ad1f995325a6947fecb7a0a0a9461d3`  
		Last Modified: Tue, 30 Sep 2025 00:16:34 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7a40e42eeaf5bd5622f29cb6a9dccd0f2036541929f187703eab2dcd3cb73fc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3619581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3525f3a7effb0513b670c1151c6e814417883c77141c277e0dfaae15ca7ebd65`

```dockerfile
```

-	Layers:
	-	`sha256:bb336d527b6b81a8b19843c8b794c242c15418fb84454637d98af93a858b6d0c`  
		Last Modified: Tue, 30 Sep 2025 22:07:49 GMT  
		Size: 3.6 MB (3603579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e8bfedbe13e8c850a9352ab07cb8c2451926c8b22fbbef681706adcbcc2380f`  
		Last Modified: Tue, 30 Sep 2025 22:07:50 GMT  
		Size: 16.0 KB (16002 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd140-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c965c49aa2b396e0101b42550f4800063f3fd56d517bec513e386066326ed80c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60131972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3ed496450d5563feac3099d0ade1c40efe2acb32ecfd970708e5e9ea282cfd7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:ed417fd581c20c18b8c6cfc58498c59128dd74498d5d6a89f9217103a4fbf9d4`  
		Last Modified: Mon, 29 Sep 2025 23:35:24 GMT  
		Size: 49.9 MB (49879877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c28b9bca2f1012ffe43d4eed07697f7da1ec3a47f388e1ab9fd4ec84b4e6268`  
		Last Modified: Tue, 30 Sep 2025 00:20:12 GMT  
		Size: 10.2 MB (10158292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10b9f543673e23c7d03685762105c2796b3abb510f7e7108cef41bbbc9a9bfe`  
		Last Modified: Tue, 30 Sep 2025 00:20:11 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a233135e8a5c44543154aa30a4dcb42b38fda3e8ca06d93f639b9f507c3d4219`  
		Last Modified: Tue, 30 Sep 2025 00:20:12 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d384ab44da2640f654099b0207090ccab3d2b58cebd6b3258b13b298c5e3a926`  
		Last Modified: Tue, 30 Sep 2025 00:20:12 GMT  
		Size: 90.5 KB (90456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2747289e0447d3ae74f622064a865138a9eb14243918fc353cdbd2bf3d71df`  
		Last Modified: Tue, 30 Sep 2025 00:20:09 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a2db88cd42eb7894e3e8a21855afe072e4bacb15736552d6bdff99769a6b19f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3621236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65795b979a2c217fe3c2025935d0c3f835af9f1520d745f2a112578257a83bb3`

```dockerfile
```

-	Layers:
	-	`sha256:6dc4931ed3e401fa42d22b976d0772f8eafaefc7add51f5418cb8196a0eb1155`  
		Last Modified: Wed, 01 Oct 2025 13:07:44 GMT  
		Size: 3.6 MB (3605094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb89734c2b1f04a1157e15fb2b072b93a1559445ebf22f509e9bd6d50f99abd0`  
		Last Modified: Wed, 01 Oct 2025 13:07:45 GMT  
		Size: 16.1 KB (16142 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd140-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:f430324cf9cfaa124d9776470203aac188ea6774709949a77b63e213adfa7ec1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61745177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a38ab08689612a8e95f9cc551ea0e8a30bda1c448048e882314e67c82e2d34da`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:376eb1520bb62885f5204083862e9559c55db2c2217bc7ae5d95166cd5564cbc`  
		Last Modified: Mon, 29 Sep 2025 23:35:30 GMT  
		Size: 51.1 MB (51119420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec729a899466ae066afe6bfa44772bb49f12eb1ff9130de5775863dfce2fa5c`  
		Last Modified: Tue, 30 Sep 2025 00:23:18 GMT  
		Size: 10.5 MB (10532172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016bd38ecc73b56e051fb135bc2f1b210de58690a65bd5202836c5e688c442a8`  
		Last Modified: Tue, 30 Sep 2025 00:23:18 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b44b7f804d68298cf138540a3c3108a2814c8cc63932f7300357c68efe7054e`  
		Last Modified: Tue, 30 Sep 2025 00:23:18 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24e9b8bf1f68d7180b0cdf3058bac384f72680340471c2b07b70711bef9c350c`  
		Last Modified: Tue, 30 Sep 2025 00:23:18 GMT  
		Size: 90.2 KB (90232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bbf84aa702d16438adb1888b29adb0d130c0a91212dad4f8842d559e332ab6`  
		Last Modified: Tue, 30 Sep 2025 00:23:18 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3b490107fb10d10a6ec4ea0b23243b771a836b62a9ec8a2428a0dd7c4b38d4c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3617512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48447039b9ee7cf8a837ef0de7f2fc8a4c3e43acdd0ac2c4ad657cbc9f7839ef`

```dockerfile
```

-	Layers:
	-	`sha256:62948bb3b9d5b778029c610a4efda1d2a480c111bf40184b640d8df7f51d9e93`  
		Last Modified: Tue, 30 Sep 2025 16:07:55 GMT  
		Size: 3.6 MB (3601540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:153eff5adb942a4269e6f4cb5eb6afbaaab407c0686fde860d67023ab18eb4f2`  
		Last Modified: Tue, 30 Sep 2025 16:07:56 GMT  
		Size: 16.0 KB (15972 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd22.04`

```console
$ docker pull neurodebian@sha256:c6bbd2e1e36b66c40fd53f7b4a059adde6ca793f3c733562f99aafa599288aca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd22.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:d3ce910a25e1ada8fb29113c427d363d0950df18f993942bb1e966b293c906fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33275318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbc492e3e53cf64bb4f5f322e8772c61cb99e0627ce806d72563b7cd165fa6c0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Sat, 01 Mar 2025 01:29:10 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a4724a87526948a669d180182a6778e1e691c719838765abce4d01c46d3989`  
		Last Modified: Tue, 02 Sep 2025 00:23:48 GMT  
		Size: 3.6 MB (3625618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c380e33d94fb72232b49c8bc34ed7ec6d5fc476094360c374549509f46be63`  
		Last Modified: Tue, 02 Sep 2025 00:23:47 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df5b8f40e27413a9ed04a139b53a2d27ad574119fb38e07573119b5f1ba2b7cb`  
		Last Modified: Tue, 02 Sep 2025 00:23:41 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f236e29b2af85abd6976a93143c874089cd671b6c9dce78ea9370ae33bedea`  
		Last Modified: Tue, 02 Sep 2025 00:23:42 GMT  
		Size: 110.6 KB (110589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:34aff235caca5114ffe5988df3758c029134f3cfd79928f2b7b75e046d884177
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e35a861e1f8209aec3893a6055acb4e242ebe33c2703d85a893b48ff3b02363a`

```dockerfile
```

-	Layers:
	-	`sha256:7d41caedea004a5f24a35b74306fc2bb1a9a276bf38f155d55be744db8ac4a1e`  
		Last Modified: Tue, 02 Sep 2025 01:07:20 GMT  
		Size: 2.2 MB (2198320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b09e2e050c9cb1cb84b85074083ff037333a48e8c7fdc30b0f24b2e72482d686`  
		Last Modified: Tue, 02 Sep 2025 01:07:21 GMT  
		Size: 14.0 KB (13976 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd22.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:ae36027e8a53ebbe67fc5a247ce3721db455994cdd9c7fe2df2ffbd78da627bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31093913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8441f857a939d9eb264ff7103795215c13448469d105c5c5c7e2ab556229accb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
ARG RELEASE
# Tue, 23 Sep 2025 14:32:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 23 Sep 2025 14:32:09 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Tue, 23 Sep 2025 14:32:09 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:325d6f6c4d15398bceac73c423e869d31f8fcaacf16ca565983fdff9003cf76e`  
		Last Modified: Thu, 02 Oct 2025 01:27:05 GMT  
		Size: 3.6 MB (3598093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b7ad240b4794dcb9ff6ace41057dfeb2c804e8db2480980e681e206b8635676`  
		Last Modified: Thu, 02 Oct 2025 01:27:04 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ecc594e7b7209ce34aed504e0d23bbf64a12c46d335f394b14f2f46ba067f3a`  
		Last Modified: Thu, 02 Oct 2025 01:27:05 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e88a579f7a31e08c9eb8dcc30111f750f38aa584d7a7a3d6c5e8abb56f595860`  
		Last Modified: Thu, 02 Oct 2025 01:27:04 GMT  
		Size: 110.5 KB (110539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c773c982f1a26fe4ea848a6232124df833ffb6f941fdae72942deee77c6fc22e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d5f66dccecae4ef8f224184a495667a7d50c6d2962d94d04e0550f29fdd65ac`

```dockerfile
```

-	Layers:
	-	`sha256:d590c7dac959fee7986e5f332cc54f2808b6a714ae848fd9ad2f5a8c578b77fe`  
		Last Modified: Thu, 02 Oct 2025 04:07:27 GMT  
		Size: 2.2 MB (2198580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1385b30d72b453beeea33a81825a47038c89d6340a0d74c17ec2416c040452a`  
		Last Modified: Thu, 02 Oct 2025 04:07:28 GMT  
		Size: 14.1 KB (14101 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd22.04-non-free`

```console
$ docker pull neurodebian@sha256:8aed8de3f1160326e3957e3cbaa386a9ad82eeace52d585f8cc758faf39ec1f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd22.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:2fa15741085a7b9a111304f94de710a342d4003de42f96d7188ae76614ee49ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33275636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:691f3a6a8f1c8ad9cece02d2fe19baf080213cf7ed68cdb0ad98152ada06cb1f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Sat, 01 Mar 2025 01:29:10 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:644d350e6c4b05f6944ae006b8aab5488c91516ffd162cfaba7f84ac273d473b`  
		Last Modified: Tue, 02 Sep 2025 00:23:45 GMT  
		Size: 3.6 MB (3625625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d90e43a114a27e26541cb1e85f4e91c965938ba1a97cae143d255897aff2129a`  
		Last Modified: Tue, 02 Sep 2025 00:23:44 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19ac9ace5a9e24d09a5d74cfbef2b3423c8652f27e8f966bd9bc62e9113363ce`  
		Last Modified: Tue, 02 Sep 2025 00:23:45 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a32399516aec62d325145feb3435edfb7a8ae0199ff2cb6bbd66c90cccb4d2e3`  
		Last Modified: Tue, 02 Sep 2025 00:23:45 GMT  
		Size: 110.6 KB (110617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7cb48d532455ee1f3cb8304abe4242d944151fed04590177b16c700f70b807`  
		Last Modified: Tue, 02 Sep 2025 00:23:45 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c57cc66c296caefe8491e689ab76b85cfa5a28354db8fcaf6d4e285820860324
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:607be7f30cc779a1e17202a6d6c14b2ac08edabd49cd5703daef1c66963a2b95`

```dockerfile
```

-	Layers:
	-	`sha256:28344ea9cda64308e3f2beaec2b0f1ecf33f042627051ad839a05fbb550e8d2e`  
		Last Modified: Tue, 02 Sep 2025 01:07:24 GMT  
		Size: 2.2 MB (2198356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f32e711bd76c0a3933a65639adf42f2367cc2f94d3e8d671098de1fec9256e73`  
		Last Modified: Tue, 02 Sep 2025 01:07:25 GMT  
		Size: 16.2 KB (16206 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd22.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:3477c05d1c44a95df25451442a0582adc59b19a1fa02d71ac9defd2e99dea2f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31094169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bbe9716177d8f8c156f3750861d90f455ba6b3aed16e8bb8c0463bc4fd51b33`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
ARG RELEASE
# Tue, 23 Sep 2025 14:32:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 23 Sep 2025 14:32:09 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Tue, 23 Sep 2025 14:32:09 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f860954b7aec09e8e634d06f465a2fee9f5efc8618a451be9ca3999110a04e0`  
		Last Modified: Thu, 02 Oct 2025 01:27:26 GMT  
		Size: 3.6 MB (3598078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80240768d635dabbcefc8ff489dd31b390e710ec1a57a20717f266cbb43f3a12`  
		Last Modified: Thu, 02 Oct 2025 01:27:26 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d84b19e7977bcb10026b60e7b92462d7e2992d0969dcbd487e6c1716a80bc89c`  
		Last Modified: Thu, 02 Oct 2025 01:27:26 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a31027b0f91a269a073a36622efb6855af47112b4c53f9b2bdb4ffc8b6caaa`  
		Last Modified: Thu, 02 Oct 2025 01:27:26 GMT  
		Size: 110.5 KB (110527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b56be4a06905892f6b37985a75ee287ae36160af8de2c3299e76657303232f5`  
		Last Modified: Thu, 02 Oct 2025 01:27:26 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2d027eaa6f6342192209425d6ecebaa9137e2db5ac730d34139eff64a9ba7f0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62f4d6e154722074fc244a1c8c4b58453a017f4c753a2047c43d2a7e1d1ca1e0`

```dockerfile
```

-	Layers:
	-	`sha256:3446b6bd4ea75dde0ade5bf1621b0940160475b92f8445fadf17a1f4e63dfae7`  
		Last Modified: Thu, 02 Oct 2025 04:07:33 GMT  
		Size: 2.2 MB (2198616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34d889bfde4fce06c5ea57e1f1822e2efe7d3b957970ea5f2f890dc14ec4116c`  
		Last Modified: Thu, 02 Oct 2025 04:07:35 GMT  
		Size: 16.3 KB (16346 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd24.04`

```console
$ docker pull neurodebian@sha256:601a9326e0a01d824205506822eb0d0b09a022e87c0383dbdec7ae4fefc52094
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd24.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:6e7f58bb0cfe1bea3aad771ecabd3a44351dc0a9f5932dabf7ec4519ad107f17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33392869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:921c74d53c91f9ad2210028b2a0641105d5aa867dc06219db16d00d87ad81ad4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Sep 2025 05:42:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:42:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:42:34 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Wed, 10 Sep 2025 05:42:34 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fccbf205b0feed79e5a4c0fd567b19ca963dbf78a57d11fc40829d8c4e97332a`  
		Last Modified: Tue, 23 Sep 2025 19:50:17 GMT  
		Size: 3.6 MB (3562782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72cb51ace634b4c46be5cfb2b382a2ff2593246498d7f91b23878bc384da4994`  
		Last Modified: Tue, 23 Sep 2025 19:50:17 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93e752d4601b9ad24a79f82c0d2e65a331623203915426246c09b29b10d1daff`  
		Last Modified: Tue, 23 Sep 2025 19:50:17 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fed9e79b1808f3bfb39d86ef7054ee5aaddfbbc29138f02a9e27be064290626`  
		Last Modified: Tue, 23 Sep 2025 19:50:17 GMT  
		Size: 103.7 KB (103728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c0601720cf5237977e729e625168c37135934a5bfad7c6d11bd16caa3abfb2bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2134841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc0bdfba6fb54c95cd9b03ea726d2d73347752552939d7511d32863543fd93df`

```dockerfile
```

-	Layers:
	-	`sha256:778594aca3ad20875cc6e85e9bd7a41cbca87b1aad2dd7b1cd395e8343555f42`  
		Last Modified: Tue, 23 Sep 2025 22:08:16 GMT  
		Size: 2.1 MB (2120865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c646c57bd302244cf50328462ef336139f1b76f7ef0b61c85c8b191c2578a22`  
		Last Modified: Tue, 23 Sep 2025 22:08:17 GMT  
		Size: 14.0 KB (13976 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd24.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:076ee02e994b28c4a5b8dca7ce94c0f397d53bf29584490bd1aa926ed68f3fb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32530114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:967aac5c12962e1d96fe8450ccb5368757669504e3dd34bbd125834fcee87385`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
ARG RELEASE
# Tue, 23 Sep 2025 14:32:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 23 Sep 2025 14:32:09 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Tue, 23 Sep 2025 14:32:09 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5d958d3bf78161fb8399d840252a91e567621f23d8189ec65cf293daeb29e9`  
		Last Modified: Thu, 02 Oct 2025 01:27:26 GMT  
		Size: 3.6 MB (3561059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed06b06cf1782d19fce6854a3fdbd239671d3c0de2b7950030170d34daa68a8`  
		Last Modified: Thu, 02 Oct 2025 01:27:26 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae680b1104d31c61ce1e3fe7a96e662af254480a8959d2cbc333210779552d77`  
		Last Modified: Thu, 02 Oct 2025 01:27:26 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b997e8e2c8ba403851c3d5a909927a6b9fd30e7a663418e0bf508fc166bd59e`  
		Last Modified: Thu, 02 Oct 2025 01:27:26 GMT  
		Size: 104.6 KB (104569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:57dd191d5f7c286cf74f6038e19a321e4fbbe2cdef34cc598341f17fd604f5e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2136011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e92002c627339bfe8e554b57adb9a10dae839783d84629f5a0b88d875a93c524`

```dockerfile
```

-	Layers:
	-	`sha256:9080f7f8187a0300ca15ea60cb19daf274f8b2affc20fd54f7c5a0046bf05db3`  
		Last Modified: Thu, 02 Oct 2025 04:07:49 GMT  
		Size: 2.1 MB (2121910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:158d749cd930e4e3a30c6b24908775a1b0162badfc7aae6623b1779e5fdb00a7`  
		Last Modified: Thu, 02 Oct 2025 04:07:50 GMT  
		Size: 14.1 KB (14101 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd24.04-non-free`

```console
$ docker pull neurodebian@sha256:219b81ee3ea119f602da5be2d6ac8a6b92ddb6d3831b4f446ed2b19658fd2edf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd24.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:5cb24cd0d31ddf07361ddd6915f2875ccce0b2a817940f3bed3239387080d196
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33393311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7193e3ef313d576c7ec5aff9de8ebeac84f342281ca232406cf718be6f057c44`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Sep 2025 05:42:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:42:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:42:34 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Wed, 10 Sep 2025 05:42:34 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22453f061905988e7a38756b38268897e1279f5316c63c8c8e0bbf35821a11b5`  
		Last Modified: Tue, 23 Sep 2025 19:50:24 GMT  
		Size: 3.6 MB (3562788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb17416e2a9decfd5a9dae04d172177794e85b5e8a02b0856bef7360ac6e351`  
		Last Modified: Tue, 23 Sep 2025 19:50:22 GMT  
		Size: 2.6 KB (2639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b40caedc1a972bdbcf830c7bc893e1f24a7f24b32a89aa191bf07182d24cf1c`  
		Last Modified: Tue, 23 Sep 2025 19:50:22 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2edcd2e81cf967c2935308f39c789275c106d80c1d814788739c97120bdcd2f3`  
		Last Modified: Tue, 23 Sep 2025 19:50:24 GMT  
		Size: 103.7 KB (103732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b42d11768aff5c784656946d3a4a2200dfce8359cd76cd0811245a9de240fdc`  
		Last Modified: Tue, 23 Sep 2025 19:50:24 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:282ca38d641b7e76ea886e653055ef0d620215113f3143fd6d7f06f6ecc8c92d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a636120cb7f5b416947ebd8fe170064e7052e00e5c03bd0a8da1e6abe7a083da`

```dockerfile
```

-	Layers:
	-	`sha256:0ee240e7724aa490468bb3ca16845d89c126b8d864e750e4162f702595841bf0`  
		Last Modified: Tue, 23 Sep 2025 22:08:23 GMT  
		Size: 2.1 MB (2120901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d99c65737e8512a7e532402e2a1ad232cdc56a884d88f5988a5be2fc877a447`  
		Last Modified: Tue, 23 Sep 2025 22:08:25 GMT  
		Size: 16.2 KB (16206 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd24.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:7b522c003933a47c8c0f9b32bafb78491a94918d6fd4bcd1bebb88b3bd64e708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32530521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:016ced27f6d136fa7c8db691ecc0cc4c3082709a5f6492fee3632890273d7be6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
ARG RELEASE
# Tue, 23 Sep 2025 14:32:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 23 Sep 2025 14:32:09 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Tue, 23 Sep 2025 14:32:09 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff9603b9fed4fd0e79270f575fa1032a1302dbe75f6f75bb04ef5363f5d109d6`  
		Last Modified: Thu, 02 Oct 2025 02:11:05 GMT  
		Size: 3.6 MB (3561046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfefb88d9e8857fd2dcdfa903adba4094035048fc91d82278fea3b9114b8dc32`  
		Last Modified: Thu, 02 Oct 2025 02:11:05 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139257581c6379b55d3d864ab5d201bd0178b911fdf2a4fa443c35c6d91b984c`  
		Last Modified: Thu, 02 Oct 2025 02:11:05 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1482b405085b76759ca5bd549426d9878d324d876bd686d53ba3bb1552cf22f0`  
		Last Modified: Thu, 02 Oct 2025 02:11:05 GMT  
		Size: 104.6 KB (104562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8edc7ade024ef6eabdef1d07c630d0d2534a7d0c8db41589ea6bfd223566f963`  
		Last Modified: Thu, 02 Oct 2025 02:11:04 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8d7228a286d9ddfd5ccc7178bcde9b74cbac183eb366168bf888007abc200015
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2138290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a22ad839acfc2e52967b283ed23a90cbc88fea240c19acc0f6cf08b5d28df915`

```dockerfile
```

-	Layers:
	-	`sha256:9f032be40c1141dddf92311e89310979dd021da4c50052a1a040a45bff616fdc`  
		Last Modified: Thu, 02 Oct 2025 04:07:53 GMT  
		Size: 2.1 MB (2121946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d111ec1a636f78d4b3b945b7247a7cf03d23f1402f2c76d0733b8449c58f807`  
		Last Modified: Thu, 02 Oct 2025 04:07:54 GMT  
		Size: 16.3 KB (16344 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd25.04`

```console
$ docker pull neurodebian@sha256:c07a39520ff2ac1e221a0d80eef416fb13a3b50c379dd58b03ee26f415df78c5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd25.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:6322daba776047203e0ced8569c868ebf29469cc97beb4d40167a96e78b0781e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.7 MB (36683854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb204028022f14c775b1a01a0e6b5680e6f83ee7b29431942339b03ec1ef56b2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Sep 2025 05:06:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:06:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:06:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:06:32 GMT
LABEL org.opencontainers.image.version=25.04
# Wed, 10 Sep 2025 05:06:34 GMT
ADD file:d17f4a4666630f8b9d15b4dc3923b653110adbab5c7c5d0bd03975e1894a7a36 in / 
# Wed, 10 Sep 2025 05:06:35 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian plucky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel plucky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a54a536f5c04d9395dbeed64c1972fe7c7df89f5374561b8718bebbfe644fd94`  
		Last Modified: Wed, 10 Sep 2025 15:57:46 GMT  
		Size: 29.7 MB (29715598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd8ede25d5f6706cb5b167461e801339927d4611c1da403c8250ac378ddcfb7`  
		Last Modified: Tue, 23 Sep 2025 22:26:32 GMT  
		Size: 6.9 MB (6861972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec816bcc7cf2b053c961623151b0268f109f9e53fb129b0fc9b149923b86e82`  
		Last Modified: Tue, 23 Sep 2025 20:39:55 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59056df6d286e5985b947bc18ee07511e950a5349b0b13984de6db2a8f2513bd`  
		Last Modified: Tue, 23 Sep 2025 20:39:55 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8771ca24af01363d8cda256698c58be88eaea12c0112b987ed8a53008b5f5c19`  
		Last Modified: Tue, 23 Sep 2025 20:39:55 GMT  
		Size: 103.4 KB (103374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd25.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:537ad54b6cf21fe615b2e0e2732211cad355f574a621a1d6aa47eb8f34cb73c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2143334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0554c38615907e72e31a0c9088a0465da2512a6b6285cb2fee497af880261606`

```dockerfile
```

-	Layers:
	-	`sha256:a537f26d2a75268cc0c2340f0a56a2a926d075599bf01609ca246c8a93907697`  
		Last Modified: Tue, 23 Sep 2025 22:08:27 GMT  
		Size: 2.1 MB (2129347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1b8a5eba4c1480cdf810d035ee6146646fe0b9357628b7b6b0b2f1b7f07fb16`  
		Last Modified: Tue, 23 Sep 2025 22:08:28 GMT  
		Size: 14.0 KB (13987 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd25.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:6667dee1f4700b6c08fdc2f2bae912623ef381278232f323f34f64f91ec027b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34807896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8c227e7f12655cdd1b389f08a7f72a0ea4cf3573cfad98d7ab0c03b9835498a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
ARG RELEASE
# Tue, 23 Sep 2025 14:32:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.version=25.04
# Tue, 23 Sep 2025 14:32:09 GMT
ADD file:27dc1d8469805e72ba7acb716a3ad7a458b855b3d087a6a329f89b7984665276 in / 
# Tue, 23 Sep 2025 14:32:09 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian plucky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel plucky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cdaac74006805135fbc40fc717498e32e43f548eeffe2ebe7f6969c6793b30e3`  
		Last Modified: Fri, 26 Sep 2025 13:27:11 GMT  
		Size: 28.3 MB (28308681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39211871011dc55aa58cc1fa22fb437042a89ba5d84b5abd5cee4f729766768`  
		Last Modified: Thu, 02 Oct 2025 01:27:58 GMT  
		Size: 6.4 MB (6392239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:596143ba030519fbeacce5f8028818d0023b3955641545e7d02c75e6a3c2636c`  
		Last Modified: Thu, 02 Oct 2025 01:27:56 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333214f1cd6fdef7b238200911fe3f2767cc558bc2aaf38c6bee3f9c0baa65df`  
		Last Modified: Thu, 02 Oct 2025 01:27:56 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffbe79341808dd41033e1eba73148b98940fc951a7de757f49842c1c5e7089ed`  
		Last Modified: Thu, 02 Oct 2025 01:27:56 GMT  
		Size: 104.1 KB (104067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd25.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:12d1bda7d2d12bfcbb2bd0522a1704a3487ec4269ce7c79dccc8b0b0f97ca220
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2143743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5a8bd9e2af6a31c11834bf19f889b4e54bac2ee26fdbc967d938391d2d71472`

```dockerfile
```

-	Layers:
	-	`sha256:0900ad7e6c2b6407afb169a9407959f591a5205e2b5ed1f0a81bd2cf563c1640`  
		Last Modified: Thu, 02 Oct 2025 04:07:59 GMT  
		Size: 2.1 MB (2129631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73198358e11962cd8b5ca86c016e556a5cd69077b2fb8a041ac56504fee57a03`  
		Last Modified: Thu, 02 Oct 2025 04:08:00 GMT  
		Size: 14.1 KB (14112 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd25.04-non-free`

```console
$ docker pull neurodebian@sha256:5b0c2a225e6329dab3acb4204dc19939b172be86d3b4fb466176333671ef8da9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd25.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:6f2fd2053ab55f4ed0f32335cd7c408a2a49f774023796246410732e2d79eab3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.7 MB (36684222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03e54e1b72b1b30dfd9c532e8cedb42616dae141eaed43398938bea205f04224`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Sep 2025 05:06:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:06:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:06:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:06:32 GMT
LABEL org.opencontainers.image.version=25.04
# Wed, 10 Sep 2025 05:06:34 GMT
ADD file:d17f4a4666630f8b9d15b4dc3923b653110adbab5c7c5d0bd03975e1894a7a36 in / 
# Wed, 10 Sep 2025 05:06:35 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian plucky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel plucky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:a54a536f5c04d9395dbeed64c1972fe7c7df89f5374561b8718bebbfe644fd94`  
		Last Modified: Wed, 10 Sep 2025 15:57:46 GMT  
		Size: 29.7 MB (29715598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300d91a073c3de45299a9951ce458fdc9dd0726ebe2c3484b0ff2b4a6ce43272`  
		Last Modified: Tue, 23 Sep 2025 19:49:54 GMT  
		Size: 6.9 MB (6861937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29f6b0123d6642e0a554854d25d43ca72c8ea91e97630087a39c5a4cf6f6f487`  
		Last Modified: Tue, 23 Sep 2025 19:49:54 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a00eac3b2ba933fbe20eccc5fe7b75d3cf8676fda517a051e0d52e3b6cce80`  
		Last Modified: Tue, 23 Sep 2025 19:49:54 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e8e3a01396d97b5dd266fbbebaefbe15a336d9ccb6ce73015849692597622f9`  
		Last Modified: Tue, 23 Sep 2025 19:49:54 GMT  
		Size: 103.3 KB (103346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1ee462167714b0d2d3cde489b2babffa0c01dd6cc4f746da5d2d32faefd9d7`  
		Last Modified: Tue, 23 Sep 2025 19:49:54 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd25.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:783d45c2c26278b7ef6837b4aa2d8450c7aced352f4adc6a86e6e162015c2690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2145600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d9b704a6d99a8795b326f247b27fe8e4096b5a24720beb22bbc2b523beb3610`

```dockerfile
```

-	Layers:
	-	`sha256:1b8f8c6ce03fbd59ba66ffd5942cb9d76560076191400c1af5f338dc04d20586`  
		Last Modified: Tue, 23 Sep 2025 22:08:32 GMT  
		Size: 2.1 MB (2129383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c0672d816407ee45341f651895fc66f5d7f8df58f36f013d6b0d6885a4c25bd`  
		Last Modified: Tue, 23 Sep 2025 22:08:33 GMT  
		Size: 16.2 KB (16217 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd25.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:6610a796644c77428e638f20adaea39e1b352d6df81444cf240b550d9fcc39bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34808280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ace4d2fd78a80fb2cfdbb5dacac0c27ef015fc81fce8a4a581a90ae622f77a2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
ARG RELEASE
# Tue, 23 Sep 2025 14:32:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.version=25.04
# Tue, 23 Sep 2025 14:32:09 GMT
ADD file:27dc1d8469805e72ba7acb716a3ad7a458b855b3d087a6a329f89b7984665276 in / 
# Tue, 23 Sep 2025 14:32:09 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian plucky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel plucky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:cdaac74006805135fbc40fc717498e32e43f548eeffe2ebe7f6969c6793b30e3`  
		Last Modified: Fri, 26 Sep 2025 13:27:11 GMT  
		Size: 28.3 MB (28308681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b639f1c25a7007bec82384a2d7b07ce825cbf93fed2b8d5ddf5b79684341db23`  
		Last Modified: Thu, 02 Oct 2025 01:27:59 GMT  
		Size: 6.4 MB (6392231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:596143ba030519fbeacce5f8028818d0023b3955641545e7d02c75e6a3c2636c`  
		Last Modified: Thu, 02 Oct 2025 01:27:56 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333214f1cd6fdef7b238200911fe3f2767cc558bc2aaf38c6bee3f9c0baa65df`  
		Last Modified: Thu, 02 Oct 2025 01:27:56 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bcc9617dde3e2759df04f681b1f7813356d3d79dba0d30a8553f82fd6740843`  
		Last Modified: Thu, 02 Oct 2025 01:27:57 GMT  
		Size: 104.0 KB (104030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030e59682cd05fb69799eac290fd97eab1237f806966583ebc88a6cd4e931a8a`  
		Last Modified: Thu, 02 Oct 2025 01:27:57 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd25.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e37121db5f0632df5c979126b26e3ff7dc2b85092f31c99953e6013b2e7fde2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2146024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d35eb4831e0fabe4b2f4f385f3cd447a01a9205dc79823808321c0eba3fd28ea`

```dockerfile
```

-	Layers:
	-	`sha256:a55c84bda7f22c51d223cc14def8f0de9e350f125007252cdf37c9af5d9a5ce4`  
		Last Modified: Thu, 02 Oct 2025 04:08:09 GMT  
		Size: 2.1 MB (2129667 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:646d2405aaabb4226273d83bd22d655e641bbbd5c5da52281d759e07884441e0`  
		Last Modified: Thu, 02 Oct 2025 04:08:10 GMT  
		Size: 16.4 KB (16357 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:noble`

```console
$ docker pull neurodebian@sha256:601a9326e0a01d824205506822eb0d0b09a022e87c0383dbdec7ae4fefc52094
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:noble` - linux; amd64

```console
$ docker pull neurodebian@sha256:6e7f58bb0cfe1bea3aad771ecabd3a44351dc0a9f5932dabf7ec4519ad107f17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33392869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:921c74d53c91f9ad2210028b2a0641105d5aa867dc06219db16d00d87ad81ad4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Sep 2025 05:42:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:42:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:42:34 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Wed, 10 Sep 2025 05:42:34 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fccbf205b0feed79e5a4c0fd567b19ca963dbf78a57d11fc40829d8c4e97332a`  
		Last Modified: Tue, 23 Sep 2025 19:50:17 GMT  
		Size: 3.6 MB (3562782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72cb51ace634b4c46be5cfb2b382a2ff2593246498d7f91b23878bc384da4994`  
		Last Modified: Tue, 23 Sep 2025 19:50:17 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93e752d4601b9ad24a79f82c0d2e65a331623203915426246c09b29b10d1daff`  
		Last Modified: Tue, 23 Sep 2025 19:50:17 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fed9e79b1808f3bfb39d86ef7054ee5aaddfbbc29138f02a9e27be064290626`  
		Last Modified: Tue, 23 Sep 2025 19:50:17 GMT  
		Size: 103.7 KB (103728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c0601720cf5237977e729e625168c37135934a5bfad7c6d11bd16caa3abfb2bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2134841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc0bdfba6fb54c95cd9b03ea726d2d73347752552939d7511d32863543fd93df`

```dockerfile
```

-	Layers:
	-	`sha256:778594aca3ad20875cc6e85e9bd7a41cbca87b1aad2dd7b1cd395e8343555f42`  
		Last Modified: Tue, 23 Sep 2025 22:08:16 GMT  
		Size: 2.1 MB (2120865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c646c57bd302244cf50328462ef336139f1b76f7ef0b61c85c8b191c2578a22`  
		Last Modified: Tue, 23 Sep 2025 22:08:17 GMT  
		Size: 14.0 KB (13976 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:noble` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:076ee02e994b28c4a5b8dca7ce94c0f397d53bf29584490bd1aa926ed68f3fb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32530114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:967aac5c12962e1d96fe8450ccb5368757669504e3dd34bbd125834fcee87385`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
ARG RELEASE
# Tue, 23 Sep 2025 14:32:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 23 Sep 2025 14:32:09 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Tue, 23 Sep 2025 14:32:09 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5d958d3bf78161fb8399d840252a91e567621f23d8189ec65cf293daeb29e9`  
		Last Modified: Thu, 02 Oct 2025 01:27:26 GMT  
		Size: 3.6 MB (3561059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed06b06cf1782d19fce6854a3fdbd239671d3c0de2b7950030170d34daa68a8`  
		Last Modified: Thu, 02 Oct 2025 01:27:26 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae680b1104d31c61ce1e3fe7a96e662af254480a8959d2cbc333210779552d77`  
		Last Modified: Thu, 02 Oct 2025 01:27:26 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b997e8e2c8ba403851c3d5a909927a6b9fd30e7a663418e0bf508fc166bd59e`  
		Last Modified: Thu, 02 Oct 2025 01:27:26 GMT  
		Size: 104.6 KB (104569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:57dd191d5f7c286cf74f6038e19a321e4fbbe2cdef34cc598341f17fd604f5e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2136011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e92002c627339bfe8e554b57adb9a10dae839783d84629f5a0b88d875a93c524`

```dockerfile
```

-	Layers:
	-	`sha256:9080f7f8187a0300ca15ea60cb19daf274f8b2affc20fd54f7c5a0046bf05db3`  
		Last Modified: Thu, 02 Oct 2025 04:07:49 GMT  
		Size: 2.1 MB (2121910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:158d749cd930e4e3a30c6b24908775a1b0162badfc7aae6623b1779e5fdb00a7`  
		Last Modified: Thu, 02 Oct 2025 04:07:50 GMT  
		Size: 14.1 KB (14101 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:noble-non-free`

```console
$ docker pull neurodebian@sha256:219b81ee3ea119f602da5be2d6ac8a6b92ddb6d3831b4f446ed2b19658fd2edf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:noble-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:5cb24cd0d31ddf07361ddd6915f2875ccce0b2a817940f3bed3239387080d196
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33393311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7193e3ef313d576c7ec5aff9de8ebeac84f342281ca232406cf718be6f057c44`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Sep 2025 05:42:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:42:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:42:34 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Wed, 10 Sep 2025 05:42:34 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22453f061905988e7a38756b38268897e1279f5316c63c8c8e0bbf35821a11b5`  
		Last Modified: Tue, 23 Sep 2025 19:50:24 GMT  
		Size: 3.6 MB (3562788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb17416e2a9decfd5a9dae04d172177794e85b5e8a02b0856bef7360ac6e351`  
		Last Modified: Tue, 23 Sep 2025 19:50:22 GMT  
		Size: 2.6 KB (2639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b40caedc1a972bdbcf830c7bc893e1f24a7f24b32a89aa191bf07182d24cf1c`  
		Last Modified: Tue, 23 Sep 2025 19:50:22 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2edcd2e81cf967c2935308f39c789275c106d80c1d814788739c97120bdcd2f3`  
		Last Modified: Tue, 23 Sep 2025 19:50:24 GMT  
		Size: 103.7 KB (103732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b42d11768aff5c784656946d3a4a2200dfce8359cd76cd0811245a9de240fdc`  
		Last Modified: Tue, 23 Sep 2025 19:50:24 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:282ca38d641b7e76ea886e653055ef0d620215113f3143fd6d7f06f6ecc8c92d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a636120cb7f5b416947ebd8fe170064e7052e00e5c03bd0a8da1e6abe7a083da`

```dockerfile
```

-	Layers:
	-	`sha256:0ee240e7724aa490468bb3ca16845d89c126b8d864e750e4162f702595841bf0`  
		Last Modified: Tue, 23 Sep 2025 22:08:23 GMT  
		Size: 2.1 MB (2120901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d99c65737e8512a7e532402e2a1ad232cdc56a884d88f5988a5be2fc877a447`  
		Last Modified: Tue, 23 Sep 2025 22:08:25 GMT  
		Size: 16.2 KB (16206 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:noble-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:7b522c003933a47c8c0f9b32bafb78491a94918d6fd4bcd1bebb88b3bd64e708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32530521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:016ced27f6d136fa7c8db691ecc0cc4c3082709a5f6492fee3632890273d7be6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
ARG RELEASE
# Tue, 23 Sep 2025 14:32:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 23 Sep 2025 14:32:09 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Tue, 23 Sep 2025 14:32:09 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff9603b9fed4fd0e79270f575fa1032a1302dbe75f6f75bb04ef5363f5d109d6`  
		Last Modified: Thu, 02 Oct 2025 02:11:05 GMT  
		Size: 3.6 MB (3561046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfefb88d9e8857fd2dcdfa903adba4094035048fc91d82278fea3b9114b8dc32`  
		Last Modified: Thu, 02 Oct 2025 02:11:05 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139257581c6379b55d3d864ab5d201bd0178b911fdf2a4fa443c35c6d91b984c`  
		Last Modified: Thu, 02 Oct 2025 02:11:05 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1482b405085b76759ca5bd549426d9878d324d876bd686d53ba3bb1552cf22f0`  
		Last Modified: Thu, 02 Oct 2025 02:11:05 GMT  
		Size: 104.6 KB (104562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8edc7ade024ef6eabdef1d07c630d0d2534a7d0c8db41589ea6bfd223566f963`  
		Last Modified: Thu, 02 Oct 2025 02:11:04 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8d7228a286d9ddfd5ccc7178bcde9b74cbac183eb366168bf888007abc200015
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2138290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a22ad839acfc2e52967b283ed23a90cbc88fea240c19acc0f6cf08b5d28df915`

```dockerfile
```

-	Layers:
	-	`sha256:9f032be40c1141dddf92311e89310979dd021da4c50052a1a040a45bff616fdc`  
		Last Modified: Thu, 02 Oct 2025 04:07:53 GMT  
		Size: 2.1 MB (2121946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d111ec1a636f78d4b3b945b7247a7cf03d23f1402f2c76d0733b8449c58f807`  
		Last Modified: Thu, 02 Oct 2025 04:07:54 GMT  
		Size: 16.3 KB (16344 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:non-free`

```console
$ docker pull neurodebian@sha256:0d9a4c13d4e7371ad64078f0d671c6383a8f7afdadf6df21e6ea836acc999891
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:2503ccc01a731af5b2d3d92f7327d9e31bbcb1011139a72879f223a379d18068
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59667538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b4b50aa0579a74bdcbb49a498d7315d494e61327bc54deff97aae76e3b57c4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:cae3b572364a7d48f8485d67baee38e4e44e299b8c8c4d020ff7fb5fdd97f88c`  
		Last Modified: Mon, 29 Sep 2025 23:35:29 GMT  
		Size: 49.3 MB (49284626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f805df92352cae0a0a2836745a1bb53b364d8cccb0a97b47b625e0dde43f3f`  
		Last Modified: Tue, 30 Sep 2025 00:16:34 GMT  
		Size: 10.3 MB (10289390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc43eb24082631f3aec7eb229fe3fb1fd1008d98e03bfbd5a612e46b23ba1e2`  
		Last Modified: Tue, 30 Sep 2025 00:16:33 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3328b63a48e14a4f9831671d91841324f4446ffc7c53aba7cd267daa4b4f80`  
		Last Modified: Tue, 30 Sep 2025 00:16:33 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b20b675e05429ab3c15103ae9009614f1f3725ae5cbad4733ca582901965b1`  
		Last Modified: Tue, 30 Sep 2025 00:16:33 GMT  
		Size: 90.2 KB (90174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1daee8250ea7ba96eac71bc0e2a8bbd64222f6a94bb432c8cd8623a6760f3002`  
		Last Modified: Tue, 30 Sep 2025 00:16:33 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:52e009a03c07d287b8712a89275cf62d910e6f735fb37cc5e7bab8beef1bbe66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3629346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34a745821a65d66b1aa0f33a69d19c1824d420dbebf69bdce4aa51155bb295fc`

```dockerfile
```

-	Layers:
	-	`sha256:458676c72d3376b2e2adc40b027530e16649d7cef3dce4f466fa9eafc5e2602b`  
		Last Modified: Tue, 30 Sep 2025 22:08:44 GMT  
		Size: 3.6 MB (3613021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d73401dfdc2638617c66e6f3c897b4abcb9fd9d44e04be80396ce82befadec0`  
		Last Modified: Tue, 30 Sep 2025 22:08:45 GMT  
		Size: 16.3 KB (16325 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:bb8a1f91ca3dda2b54c613358a3f2f2945bfc5deaafc4eeadb6eae89d044f6c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59815896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8008367a8e867e3902e67f9754a14d41e1c86f389a5a7ecb27933aff25207f1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:28aec8b14b3eeacbf47ef38af72fab694b109fdcdf31581722750599baf1a932`  
		Last Modified: Mon, 29 Sep 2025 23:35:17 GMT  
		Size: 49.6 MB (49648695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f827ec068a53d186059453e246d57e837a733af80e5e8a439634aaa8010cbc48`  
		Last Modified: Tue, 30 Sep 2025 00:19:31 GMT  
		Size: 10.1 MB (10073018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f2c0c542f12345a7b0b7332a3c30fbef3e0f06cb41dab53840a4e12b39a669`  
		Last Modified: Tue, 30 Sep 2025 00:19:30 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb99ddf347a9b9633f0d8033fe5a42e37880b4b2ddaf4bda2922f2c4bc504a8`  
		Last Modified: Tue, 30 Sep 2025 00:19:30 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7514b6a6ce06d47e1c9a211e6c9baac0edbdef4aa535d618f6415f0fbe994a`  
		Last Modified: Tue, 30 Sep 2025 00:19:31 GMT  
		Size: 90.8 KB (90837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73a6f3450e33d6d3354fde8b80a122a9643f6244d174f78222de5bd8feb1a930`  
		Last Modified: Tue, 30 Sep 2025 00:19:30 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f0d1fa2842c899d239f59156bb06dcb2aa6b4017485f5d1418867ab3b772ea22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3631025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfc74683096734fe8a7282c0c86a4b90695de4208566bde26b768822394849ba`

```dockerfile
```

-	Layers:
	-	`sha256:8358e4867b6f7d30ccde76e14fd6bc289cb71cee56a711c57179f8b40eda4b1c`  
		Last Modified: Wed, 01 Oct 2025 13:08:20 GMT  
		Size: 3.6 MB (3614548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7daca65ee14aa6ed1264b3293452c903db18d8777d168fdec82a6219fa454ed`  
		Last Modified: Wed, 01 Oct 2025 13:08:20 GMT  
		Size: 16.5 KB (16477 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:6f5f51db0117943740d24d6272ede6d385cf0de736a0a87db476f1cd373ac423
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61356742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28287d3132e454889d0cb4278309fdd1c117e4946ce49dd56a41083c2539181e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:f1c1f592b5569b5e2093c3107a48f2929b609f05af6d24c06d41a7ec1ae5e0e1`  
		Last Modified: Mon, 29 Sep 2025 23:35:36 GMT  
		Size: 50.8 MB (50800229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b43fce213f96af9285577072bd9752768a9c65a727ec564297271c4fb3dd675`  
		Last Modified: Tue, 30 Sep 2025 00:23:18 GMT  
		Size: 10.5 MB (10462626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e2e09d36685cd8530477135a922a156ccc8bfdf81e79a088f5c4b6bae27c7a`  
		Last Modified: Tue, 30 Sep 2025 00:23:13 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77747ec32ef9084e7a31f53e4895625940080c905fe34a4b4a1518a05da0be5c`  
		Last Modified: Tue, 30 Sep 2025 00:23:12 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afe8cd32135ae5186a68422d3154e344abce87331d1c80a54f49c008cafa3754`  
		Last Modified: Tue, 30 Sep 2025 00:23:13 GMT  
		Size: 90.5 KB (90540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6ade42626c18876d4e066d0491d60ce433a6f3f35060ac999555d4904dbba5`  
		Last Modified: Tue, 30 Sep 2025 00:23:13 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2e53fda5ed32d4582af0d59a52f6053c693f45de5a8593022784d862534f1272
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3627260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cff141d466be7fd3841ab7f3fdd7191cb53a6b2c3df26fa213fd731f4e39ea16`

```dockerfile
```

-	Layers:
	-	`sha256:fac33ea0fa1e517ae03eda600bab1c7ec5b8189b09fe01c651a4f7d35b69e1cd`  
		Last Modified: Tue, 30 Sep 2025 16:08:40 GMT  
		Size: 3.6 MB (3610970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39422b45dea80b7340f8112c3c76282ecdcfd55ec0cbdbbdbf5570d78a2d4128`  
		Last Modified: Tue, 30 Sep 2025 16:08:41 GMT  
		Size: 16.3 KB (16290 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:plucky`

```console
$ docker pull neurodebian@sha256:c07a39520ff2ac1e221a0d80eef416fb13a3b50c379dd58b03ee26f415df78c5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:plucky` - linux; amd64

```console
$ docker pull neurodebian@sha256:6322daba776047203e0ced8569c868ebf29469cc97beb4d40167a96e78b0781e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.7 MB (36683854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb204028022f14c775b1a01a0e6b5680e6f83ee7b29431942339b03ec1ef56b2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Sep 2025 05:06:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:06:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:06:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:06:32 GMT
LABEL org.opencontainers.image.version=25.04
# Wed, 10 Sep 2025 05:06:34 GMT
ADD file:d17f4a4666630f8b9d15b4dc3923b653110adbab5c7c5d0bd03975e1894a7a36 in / 
# Wed, 10 Sep 2025 05:06:35 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian plucky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel plucky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a54a536f5c04d9395dbeed64c1972fe7c7df89f5374561b8718bebbfe644fd94`  
		Last Modified: Wed, 10 Sep 2025 15:57:46 GMT  
		Size: 29.7 MB (29715598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd8ede25d5f6706cb5b167461e801339927d4611c1da403c8250ac378ddcfb7`  
		Last Modified: Tue, 23 Sep 2025 22:26:32 GMT  
		Size: 6.9 MB (6861972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec816bcc7cf2b053c961623151b0268f109f9e53fb129b0fc9b149923b86e82`  
		Last Modified: Tue, 23 Sep 2025 20:39:55 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59056df6d286e5985b947bc18ee07511e950a5349b0b13984de6db2a8f2513bd`  
		Last Modified: Tue, 23 Sep 2025 20:39:55 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8771ca24af01363d8cda256698c58be88eaea12c0112b987ed8a53008b5f5c19`  
		Last Modified: Tue, 23 Sep 2025 20:39:55 GMT  
		Size: 103.4 KB (103374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:plucky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:537ad54b6cf21fe615b2e0e2732211cad355f574a621a1d6aa47eb8f34cb73c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2143334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0554c38615907e72e31a0c9088a0465da2512a6b6285cb2fee497af880261606`

```dockerfile
```

-	Layers:
	-	`sha256:a537f26d2a75268cc0c2340f0a56a2a926d075599bf01609ca246c8a93907697`  
		Last Modified: Tue, 23 Sep 2025 22:08:27 GMT  
		Size: 2.1 MB (2129347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1b8a5eba4c1480cdf810d035ee6146646fe0b9357628b7b6b0b2f1b7f07fb16`  
		Last Modified: Tue, 23 Sep 2025 22:08:28 GMT  
		Size: 14.0 KB (13987 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:plucky` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:6667dee1f4700b6c08fdc2f2bae912623ef381278232f323f34f64f91ec027b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34807896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8c227e7f12655cdd1b389f08a7f72a0ea4cf3573cfad98d7ab0c03b9835498a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
ARG RELEASE
# Tue, 23 Sep 2025 14:32:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.version=25.04
# Tue, 23 Sep 2025 14:32:09 GMT
ADD file:27dc1d8469805e72ba7acb716a3ad7a458b855b3d087a6a329f89b7984665276 in / 
# Tue, 23 Sep 2025 14:32:09 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian plucky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel plucky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cdaac74006805135fbc40fc717498e32e43f548eeffe2ebe7f6969c6793b30e3`  
		Last Modified: Fri, 26 Sep 2025 13:27:11 GMT  
		Size: 28.3 MB (28308681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39211871011dc55aa58cc1fa22fb437042a89ba5d84b5abd5cee4f729766768`  
		Last Modified: Thu, 02 Oct 2025 01:27:58 GMT  
		Size: 6.4 MB (6392239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:596143ba030519fbeacce5f8028818d0023b3955641545e7d02c75e6a3c2636c`  
		Last Modified: Thu, 02 Oct 2025 01:27:56 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333214f1cd6fdef7b238200911fe3f2767cc558bc2aaf38c6bee3f9c0baa65df`  
		Last Modified: Thu, 02 Oct 2025 01:27:56 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffbe79341808dd41033e1eba73148b98940fc951a7de757f49842c1c5e7089ed`  
		Last Modified: Thu, 02 Oct 2025 01:27:56 GMT  
		Size: 104.1 KB (104067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:plucky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:12d1bda7d2d12bfcbb2bd0522a1704a3487ec4269ce7c79dccc8b0b0f97ca220
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2143743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5a8bd9e2af6a31c11834bf19f889b4e54bac2ee26fdbc967d938391d2d71472`

```dockerfile
```

-	Layers:
	-	`sha256:0900ad7e6c2b6407afb169a9407959f591a5205e2b5ed1f0a81bd2cf563c1640`  
		Last Modified: Thu, 02 Oct 2025 04:07:59 GMT  
		Size: 2.1 MB (2129631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73198358e11962cd8b5ca86c016e556a5cd69077b2fb8a041ac56504fee57a03`  
		Last Modified: Thu, 02 Oct 2025 04:08:00 GMT  
		Size: 14.1 KB (14112 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:plucky-non-free`

```console
$ docker pull neurodebian@sha256:5b0c2a225e6329dab3acb4204dc19939b172be86d3b4fb466176333671ef8da9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:plucky-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:6f2fd2053ab55f4ed0f32335cd7c408a2a49f774023796246410732e2d79eab3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.7 MB (36684222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03e54e1b72b1b30dfd9c532e8cedb42616dae141eaed43398938bea205f04224`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Sep 2025 05:06:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:06:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:06:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:06:32 GMT
LABEL org.opencontainers.image.version=25.04
# Wed, 10 Sep 2025 05:06:34 GMT
ADD file:d17f4a4666630f8b9d15b4dc3923b653110adbab5c7c5d0bd03975e1894a7a36 in / 
# Wed, 10 Sep 2025 05:06:35 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian plucky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel plucky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:a54a536f5c04d9395dbeed64c1972fe7c7df89f5374561b8718bebbfe644fd94`  
		Last Modified: Wed, 10 Sep 2025 15:57:46 GMT  
		Size: 29.7 MB (29715598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300d91a073c3de45299a9951ce458fdc9dd0726ebe2c3484b0ff2b4a6ce43272`  
		Last Modified: Tue, 23 Sep 2025 19:49:54 GMT  
		Size: 6.9 MB (6861937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29f6b0123d6642e0a554854d25d43ca72c8ea91e97630087a39c5a4cf6f6f487`  
		Last Modified: Tue, 23 Sep 2025 19:49:54 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a00eac3b2ba933fbe20eccc5fe7b75d3cf8676fda517a051e0d52e3b6cce80`  
		Last Modified: Tue, 23 Sep 2025 19:49:54 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e8e3a01396d97b5dd266fbbebaefbe15a336d9ccb6ce73015849692597622f9`  
		Last Modified: Tue, 23 Sep 2025 19:49:54 GMT  
		Size: 103.3 KB (103346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1ee462167714b0d2d3cde489b2babffa0c01dd6cc4f746da5d2d32faefd9d7`  
		Last Modified: Tue, 23 Sep 2025 19:49:54 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:plucky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:783d45c2c26278b7ef6837b4aa2d8450c7aced352f4adc6a86e6e162015c2690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2145600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d9b704a6d99a8795b326f247b27fe8e4096b5a24720beb22bbc2b523beb3610`

```dockerfile
```

-	Layers:
	-	`sha256:1b8f8c6ce03fbd59ba66ffd5942cb9d76560076191400c1af5f338dc04d20586`  
		Last Modified: Tue, 23 Sep 2025 22:08:32 GMT  
		Size: 2.1 MB (2129383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c0672d816407ee45341f651895fc66f5d7f8df58f36f013d6b0d6885a4c25bd`  
		Last Modified: Tue, 23 Sep 2025 22:08:33 GMT  
		Size: 16.2 KB (16217 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:plucky-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:6610a796644c77428e638f20adaea39e1b352d6df81444cf240b550d9fcc39bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34808280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ace4d2fd78a80fb2cfdbb5dacac0c27ef015fc81fce8a4a581a90ae622f77a2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
ARG RELEASE
# Tue, 23 Sep 2025 14:32:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.version=25.04
# Tue, 23 Sep 2025 14:32:09 GMT
ADD file:27dc1d8469805e72ba7acb716a3ad7a458b855b3d087a6a329f89b7984665276 in / 
# Tue, 23 Sep 2025 14:32:09 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian plucky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel plucky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:cdaac74006805135fbc40fc717498e32e43f548eeffe2ebe7f6969c6793b30e3`  
		Last Modified: Fri, 26 Sep 2025 13:27:11 GMT  
		Size: 28.3 MB (28308681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b639f1c25a7007bec82384a2d7b07ce825cbf93fed2b8d5ddf5b79684341db23`  
		Last Modified: Thu, 02 Oct 2025 01:27:59 GMT  
		Size: 6.4 MB (6392231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:596143ba030519fbeacce5f8028818d0023b3955641545e7d02c75e6a3c2636c`  
		Last Modified: Thu, 02 Oct 2025 01:27:56 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333214f1cd6fdef7b238200911fe3f2767cc558bc2aaf38c6bee3f9c0baa65df`  
		Last Modified: Thu, 02 Oct 2025 01:27:56 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bcc9617dde3e2759df04f681b1f7813356d3d79dba0d30a8553f82fd6740843`  
		Last Modified: Thu, 02 Oct 2025 01:27:57 GMT  
		Size: 104.0 KB (104030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030e59682cd05fb69799eac290fd97eab1237f806966583ebc88a6cd4e931a8a`  
		Last Modified: Thu, 02 Oct 2025 01:27:57 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:plucky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e37121db5f0632df5c979126b26e3ff7dc2b85092f31c99953e6013b2e7fde2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2146024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d35eb4831e0fabe4b2f4f385f3cd447a01a9205dc79823808321c0eba3fd28ea`

```dockerfile
```

-	Layers:
	-	`sha256:a55c84bda7f22c51d223cc14def8f0de9e350f125007252cdf37c9af5d9a5ce4`  
		Last Modified: Thu, 02 Oct 2025 04:08:09 GMT  
		Size: 2.1 MB (2129667 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:646d2405aaabb4226273d83bd22d655e641bbbd5c5da52281d759e07884441e0`  
		Last Modified: Thu, 02 Oct 2025 04:08:10 GMT  
		Size: 16.4 KB (16357 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:efce4ea64f54ce4a5c6ed6882dae178fd70c24cfeeb45d63e709d00dcf8c93cb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:sid` - linux; amd64

```console
$ docker pull neurodebian@sha256:d352e1bdaf20b107fa873d64a014ec03a55aef6211f5e056a6cd7f3ef5a88915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (60018849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71e0de86f6c90cc7f5b47e859e7f0734d0c0be75b51cc7cdd2e6b8ecce9e6673`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:edd38bdf09a62ab44ffab2a10058156dc336ea087cf3a73258758d9bc541ff85`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 48.4 MB (48376965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1964d781cff69dcbb8224608d47e77cbe0ca18c19fda7c500947ce54b349e439`  
		Last Modified: Tue, 30 Sep 2025 00:16:32 GMT  
		Size: 11.5 MB (11549277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8083c7a164d9c55e20112d87245a4ac7874df659703dae0592af0ea6dc17eec3`  
		Last Modified: Tue, 30 Sep 2025 00:16:30 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f64ec4cb897b141395739b755c043b36a97990c58c741b36add1af451669ac27`  
		Last Modified: Tue, 30 Sep 2025 00:16:30 GMT  
		Size: 267.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ce650969fa61f99b87dc4e0c2355ec5b19b5ca0c605b89d71edb13e8210bdf`  
		Last Modified: Tue, 30 Sep 2025 00:16:30 GMT  
		Size: 89.7 KB (89708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e7f9cddb4bcb9e61947b1cbfe3d7283a24493ed40d524daf2d52203c8bcf6a1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3589132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee385a97eca1722b360e37f2ea21db83a4ca65ddeeda1726838355898e459199`

```dockerfile
```

-	Layers:
	-	`sha256:3450fd91ed423943f5f1ccb0586891b2edc69f23515ac0c6df2af5f4ccf8ad17`  
		Last Modified: Tue, 30 Sep 2025 22:08:27 GMT  
		Size: 3.6 MB (3575185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7c306a879bd2d2a90c91968619437991d21396041c3e0a911e5cf413f8d409f`  
		Last Modified: Tue, 30 Sep 2025 22:08:28 GMT  
		Size: 13.9 KB (13947 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:f276efd9172e11522046410af5ce0eb50a69e25afff35700d60c8301448a2281
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59869090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afc5710290db43f8f232f408c6687165992caead41c0085fa62263a4362cb9db`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f5aae340a376cad680dc8a41a7fd30a241ed4bae3e53125ebb424c8fc7996aaa`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 48.5 MB (48487991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc322d3092244931732034d2c756709c302b50f1227794a20a81109328519c7`  
		Last Modified: Tue, 30 Sep 2025 00:20:10 GMT  
		Size: 11.3 MB (11287787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29113037dd1be00d90a636436bf0567190c0201bd65bbc714d71afbda2ab6950`  
		Last Modified: Tue, 30 Sep 2025 00:20:09 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f8fc058e5e886c0a4787a53a804e614a59df193c608a14fc339b41a0f5a7112`  
		Last Modified: Tue, 30 Sep 2025 00:20:09 GMT  
		Size: 267.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe019269d1c4393a725d347c2717dfe5b5dde34b8369131e2a6ebb3f43c61181`  
		Last Modified: Tue, 30 Sep 2025 00:20:09 GMT  
		Size: 90.4 KB (90409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:42c0f769a6605843de59dd9a117d96c8b7446f60fdebfc99b40a806828cd4cf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3590133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d0b0dd03b72ea4b6bf7ee568d8a3aee946316388d6e61e18483a3cb671d1a56`

```dockerfile
```

-	Layers:
	-	`sha256:6607e14c440cf1ec05381d57aab85c2f3e0692fc5eb4066035be42c25f0922e5`  
		Last Modified: Wed, 01 Oct 2025 13:07:53 GMT  
		Size: 3.6 MB (3576061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd0f3dce5e1f118d17d9bbbb63d168fd52f0fe2ccbc70d27cc2a73ce8c7c4605`  
		Last Modified: Wed, 01 Oct 2025 13:07:53 GMT  
		Size: 14.1 KB (14072 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; 386

```console
$ docker pull neurodebian@sha256:0622b7c8607a17ed3f062dcbbe2e5ce444ad89bd2e586f4142e8de5a0190ac11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61496239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a7e383cde8bac028bea9bf478d11f6e67bf5fd643663cc161c83f71ffcd1d77`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d00269cb73b9e4cfebd155b431da849e0072689663a0a658044389a50f9d989d`  
		Last Modified: Mon, 29 Sep 2025 23:35:17 GMT  
		Size: 49.7 MB (49686171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6f6480fd49647a130c5672473eb706e570d0a7e2ffc738010f418159bb8f42`  
		Last Modified: Tue, 30 Sep 2025 00:23:15 GMT  
		Size: 11.7 MB (11717042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00bb6b77036d5b364bd2bb6f5016c7e6e6e1f51fd3acd6413ec0fffca6c7be09`  
		Last Modified: Tue, 30 Sep 2025 00:23:15 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ead752bbeef4f8b6544c7e6da0e9c452da6e55d7f7bf44255bc5705f3e41be`  
		Last Modified: Tue, 30 Sep 2025 00:23:15 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbee98413e70c0108e75166cd1eab704dbccca336d46231839dd53c9b6e22b1d`  
		Last Modified: Tue, 30 Sep 2025 00:23:15 GMT  
		Size: 90.1 KB (90122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:83a99d285742e7df8821f912e07a2fdc81967eff6e1c18910effd26a40e17be5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3587067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62902d1e1f48582360c7d309fa12760e834aea5cc58e13c631bcbb277337dbec`

```dockerfile
```

-	Layers:
	-	`sha256:cfa6aeb85429432a36111a8460eb077d4be2c8e303826ac96fdfe3489298992e`  
		Last Modified: Tue, 30 Sep 2025 16:08:22 GMT  
		Size: 3.6 MB (3573148 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe777d0a54bde48dc55901a7c0d9b6fc6677cdd0df0f45a4aba0d526aa5e4078`  
		Last Modified: Tue, 30 Sep 2025 16:08:23 GMT  
		Size: 13.9 KB (13919 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:sid-non-free`

```console
$ docker pull neurodebian@sha256:97ae4ac92c67e53d9f68b612bc47d6a6995653609ebad9bf76d3bbb1049a3455
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:sid-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:3e546a3eedb271a9eb8c8a3fd359cc34aa309cb0f055384484db71a135a5a035
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (60019399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:452d59ad840fbcfd81c522c18b87369321b77e10537e7abcd4be040eefd0fcf2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:edd38bdf09a62ab44ffab2a10058156dc336ea087cf3a73258758d9bc541ff85`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 48.4 MB (48376965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dbd61395bd6666c015e62c5fd23a5924635a999daa18e84a1346004e8e1a3fe`  
		Last Modified: Tue, 30 Sep 2025 00:16:35 GMT  
		Size: 11.5 MB (11549370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b39194b1de3ff41fb77cf0e8d5c69d997b6d0ca8d0a35c644b1ed207e9ef0a8c`  
		Last Modified: Tue, 30 Sep 2025 00:16:34 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a410d8cc2f19fa3ba9214b113c6f21d9fcf24c60ecacbc24a8352834dba93dae`  
		Last Modified: Tue, 30 Sep 2025 00:16:34 GMT  
		Size: 267.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1abee6b364777d5c62b6c23d22cb7f9c3d6718362d6fedc11ac022176f6a032c`  
		Last Modified: Tue, 30 Sep 2025 00:16:34 GMT  
		Size: 89.7 KB (89745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87144e73ed6f2011ee26137d4e17657da8fa9cc9fe23524733fc900fc0c488ce`  
		Last Modified: Tue, 30 Sep 2025 00:16:34 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c56ddafef222795b2c3e6d957988422562cc939522972b2cb37df0c29252914c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3591195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1397b37b2621de8dd3b31e24bb65583e05fb53d4bed8e7250620d68d1ccbbc83`

```dockerfile
```

-	Layers:
	-	`sha256:de1436e767210397db0ce0822cdab812243cbf01b60f76a691141e21d30f7036`  
		Last Modified: Tue, 30 Sep 2025 22:08:32 GMT  
		Size: 3.6 MB (3575221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fa86c35f97f132f3e730b9933892b76c47a6fa9c0a40ba58e5fdbac4999fde9`  
		Last Modified: Tue, 30 Sep 2025 22:08:33 GMT  
		Size: 16.0 KB (15974 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:d1bde026937e1caa698288efc4bf2f902fd5bfe8b097761380ce6579be8032c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59869395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcb38a560199cd70f43b3312deafda4e8d7630784a47d462c8d463746c3e2f43`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:f5aae340a376cad680dc8a41a7fd30a241ed4bae3e53125ebb424c8fc7996aaa`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 48.5 MB (48487991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c092a798258bf5d2b4e17d2853d10750c62f97c4fec6e26c8f61a18048faa488`  
		Last Modified: Tue, 30 Sep 2025 00:20:12 GMT  
		Size: 11.3 MB (11287724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64c43273a9ef2841db6b6ee9ceda6265917ad0b4211e8dc8a73519452685240`  
		Last Modified: Tue, 30 Sep 2025 00:20:10 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c947e3e247e08b3dab92c27fa882b771a9e33723d806b99a38f2d9b6495c5fcd`  
		Last Modified: Tue, 30 Sep 2025 00:20:10 GMT  
		Size: 267.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19175cb6fd3b21039e84ae39127512e4ead20fff2e78168aa04774a7596db3bd`  
		Last Modified: Tue, 30 Sep 2025 00:20:10 GMT  
		Size: 90.4 KB (90364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:856eb2da076a53a597a999f69ea08fd82bb2f890cc19581f2c0bc711d7c494fa`  
		Last Modified: Tue, 30 Sep 2025 00:20:11 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b7736fd4bfb116c8139cf451e99b821ca0b9886870a735e3a7840ce9cc0ab970
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3592211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9266b19a490b3159cd1b28ecdc40fb5c2597eff1c423e64dc7fb30105fb8f979`

```dockerfile
```

-	Layers:
	-	`sha256:55817bec929f30eee7545d679faf2afe6560b5846b64cd31c32ae3959a53caa6`  
		Last Modified: Wed, 01 Oct 2025 13:08:04 GMT  
		Size: 3.6 MB (3576097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76054e24cd08c07a3c052d751bc685a37453495f14f7032391965a4d9a083ca6`  
		Last Modified: Wed, 01 Oct 2025 13:08:05 GMT  
		Size: 16.1 KB (16114 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:83aacc7fb7b5c65ca54a080818e9df1beb9e2835d71400afb8c936d0be0596c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61496540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d626ce9d4f2fad6eab9d8e779976d51889a33cfcdd0cdf4d001d569d28c47a8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:d00269cb73b9e4cfebd155b431da849e0072689663a0a658044389a50f9d989d`  
		Last Modified: Mon, 29 Sep 2025 23:35:17 GMT  
		Size: 49.7 MB (49686171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e44f7b83abd8b70cd2ad8be2342045f1278f361d52d006293b6138988a57d04`  
		Last Modified: Tue, 30 Sep 2025 00:23:18 GMT  
		Size: 11.7 MB (11716994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e53eb5296e1a4de069da153195c7ba4f193ae52135e2fe3e4f00df0a32fabf`  
		Last Modified: Tue, 30 Sep 2025 00:23:17 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543f65dd046c1052fda8eb42005bccd5b42eab0bb6d48a74c2ba1fb663bafe25`  
		Last Modified: Tue, 30 Sep 2025 00:23:18 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d55663231e76515c4e6592b762a96895630954a6b668a4b634aba4b9391b3dc6`  
		Last Modified: Tue, 30 Sep 2025 00:23:17 GMT  
		Size: 90.1 KB (90053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f46582ec95217b2b184925612b84924c68c5346b759bdb1ab3841815dc207c91`  
		Last Modified: Tue, 30 Sep 2025 00:23:18 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:cb6e5622e428e267adef0d79727976efc8d4b353bca077aac7912d8c1e7d8390
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3589126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:519927b36064e015e1e86af0b2f1d9ab668b2d6045b87467db30fafc83bd1b8a`

```dockerfile
```

-	Layers:
	-	`sha256:73cd775764b53a6df1791f2a63e44e371b862cc68aa1b9f35d6e5d6dcbf5f8ea`  
		Last Modified: Tue, 30 Sep 2025 16:08:29 GMT  
		Size: 3.6 MB (3573184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1dbad6618782fdb70a1e53631f2316732918e54a51517310778994fd40f091f`  
		Last Modified: Tue, 30 Sep 2025 16:08:29 GMT  
		Size: 15.9 KB (15942 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:trixie`

```console
$ docker pull neurodebian@sha256:87693cfb664c3983f3e574e1dcd5b58f82fd2618b8af3a364767508759c8e2c4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:trixie` - linux; amd64

```console
$ docker pull neurodebian@sha256:5445400c594afd56d8608d270c0e840a5bdc8ce8eed14c50875b111ece8c8967
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59667200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1692c2ad0959aff9134072de309c7092e4303f34bd66175926b4536f01737b1b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cae3b572364a7d48f8485d67baee38e4e44e299b8c8c4d020ff7fb5fdd97f88c`  
		Last Modified: Mon, 29 Sep 2025 23:35:29 GMT  
		Size: 49.3 MB (49284626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf661b2ff63805151437f18c9fddf545dc18823488c0dbe851eafeba8066d82`  
		Last Modified: Wed, 01 Oct 2025 00:26:33 GMT  
		Size: 10.3 MB (10289495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030c7393f1d0600f3d5801fa9a09be77c972b3bf6cec3d9a0ceee41e16f80f79`  
		Last Modified: Tue, 30 Sep 2025 01:05:19 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7679f2a094fcaa509ff0dbff39c2f33e8f9ee67eba015e63ec580599369bd963`  
		Last Modified: Tue, 30 Sep 2025 01:05:20 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5fdaff3323992c80159a90ce241b8c1e2eecfc50b87e4e1f570519c04063c53`  
		Last Modified: Tue, 30 Sep 2025 01:05:19 GMT  
		Size: 90.2 KB (90176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:11379453b3c698293768b9d690e1a7e9d3b6991a688f6f2c6c9d46d25b7a1999
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3627275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e291424f296bf0582d068b79c4a19e3cf1f75fa0e7f7d4051e57733efe754ae`

```dockerfile
```

-	Layers:
	-	`sha256:a5d6e8b4a14ee685087c48f425191d4046aecfdc2e2dce91edd6ba320a8a65b9`  
		Last Modified: Tue, 30 Sep 2025 22:08:37 GMT  
		Size: 3.6 MB (3612981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cba41c16a9c24d09b71598c74915dea63db262a1a93abcbc3f0d247b9b4c11c2`  
		Last Modified: Tue, 30 Sep 2025 22:08:38 GMT  
		Size: 14.3 KB (14294 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:5d39e0ae09097ede0b7dcd605763843cc32f5d004f39cefe691f3534fcabf107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59815441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d12c54dcf7bbe6d3551a1d49ac956e0b9ef7c361391bd2511992d7c2ba5cc6f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:28aec8b14b3eeacbf47ef38af72fab694b109fdcdf31581722750599baf1a932`  
		Last Modified: Mon, 29 Sep 2025 23:35:17 GMT  
		Size: 49.6 MB (49648695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b6f6da96540c9f6cf298b7b364c63b1cf0c3929b805fed831b6c1c3eae4d87`  
		Last Modified: Tue, 30 Sep 2025 00:19:26 GMT  
		Size: 10.1 MB (10072980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a478dfca60a2c33636ca722a574ff603abd3fae381c95be0c7bf68323a3704`  
		Last Modified: Tue, 30 Sep 2025 00:19:27 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5474e962acd88276c7b9fa402cc148afe511eddb2832d559ea63b51fb720b0a`  
		Last Modified: Tue, 30 Sep 2025 00:19:28 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094906ccc10fa032c3efb4b206bda6edbedb9eca7903daa2ebdf676a5f615361`  
		Last Modified: Tue, 30 Sep 2025 00:19:28 GMT  
		Size: 90.9 KB (90866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2be449b53fb3b4125c74bfaf49a273c82589056f7a7b58ced28d693d35ecfd68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cf5e15992d5473686642c610909b239be7d6cf3f13bcfccc273a3f7cd5cd553`

```dockerfile
```

-	Layers:
	-	`sha256:ea9f419913ead7a4c0e010568c2d3864423e07529314b03a43cadf13070d7ebe`  
		Last Modified: Tue, 30 Sep 2025 13:07:45 GMT  
		Size: 3.6 MB (3614508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08e6d045cefb6337ce69dbe9c61d5d154f22a2ddc355e21d8fb66a2d9f615939`  
		Last Modified: Tue, 30 Sep 2025 13:07:46 GMT  
		Size: 14.4 KB (14431 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie` - linux; 386

```console
$ docker pull neurodebian@sha256:8a46319c2bee6856b4f764ac30025c5587a5ee243fb31b30dbfc8d7fdbaa6d9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61356323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35e989f30d27cafca9de5bdca46f6e0f4139c1fd7362a134d113c77557fab4dc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f1c1f592b5569b5e2093c3107a48f2929b609f05af6d24c06d41a7ec1ae5e0e1`  
		Last Modified: Mon, 29 Sep 2025 23:35:36 GMT  
		Size: 50.8 MB (50800229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ab973589bc45010616b19754c3c69e0ae9f8ca8970197b3299d394ea33f588`  
		Last Modified: Tue, 30 Sep 2025 00:23:16 GMT  
		Size: 10.5 MB (10462616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3efbe96c0b7cb9c8886f791f5343077fbcb6ee8bf991286ebe52cab58d6cc892`  
		Last Modified: Tue, 30 Sep 2025 00:23:04 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dea642e4992382c23719b878885f48c32247f1f5867d347ad4c22d63c0a8720`  
		Last Modified: Tue, 30 Sep 2025 00:23:04 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6ae40746c8c652627ef29267be656c50aab350b775d26b475917c7e2742ed1`  
		Last Modified: Tue, 30 Sep 2025 00:23:04 GMT  
		Size: 90.6 KB (90577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:01edb6d5394be68b0049fb213c5711380de11bbe71bb915c1a99290309011366
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3625191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff7b3eabd530054c8c1027eb5ff3de1c92acd70f4dac5652e04a574e629a340c`

```dockerfile
```

-	Layers:
	-	`sha256:031421d4527aa62b75263e52be1877d3065aa1b9c5575c49b0f1fb55f48c5bf5`  
		Last Modified: Tue, 30 Sep 2025 16:08:34 GMT  
		Size: 3.6 MB (3610930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c15ca298c4f9b159a9a1e17f17ba6bf440488c13b2b3af4a01a92335f30ff50b`  
		Last Modified: Tue, 30 Sep 2025 16:08:34 GMT  
		Size: 14.3 KB (14261 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:trixie-non-free`

```console
$ docker pull neurodebian@sha256:0d9a4c13d4e7371ad64078f0d671c6383a8f7afdadf6df21e6ea836acc999891
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:trixie-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:2503ccc01a731af5b2d3d92f7327d9e31bbcb1011139a72879f223a379d18068
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59667538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b4b50aa0579a74bdcbb49a498d7315d494e61327bc54deff97aae76e3b57c4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:cae3b572364a7d48f8485d67baee38e4e44e299b8c8c4d020ff7fb5fdd97f88c`  
		Last Modified: Mon, 29 Sep 2025 23:35:29 GMT  
		Size: 49.3 MB (49284626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f805df92352cae0a0a2836745a1bb53b364d8cccb0a97b47b625e0dde43f3f`  
		Last Modified: Tue, 30 Sep 2025 00:16:34 GMT  
		Size: 10.3 MB (10289390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc43eb24082631f3aec7eb229fe3fb1fd1008d98e03bfbd5a612e46b23ba1e2`  
		Last Modified: Tue, 30 Sep 2025 00:16:33 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3328b63a48e14a4f9831671d91841324f4446ffc7c53aba7cd267daa4b4f80`  
		Last Modified: Tue, 30 Sep 2025 00:16:33 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b20b675e05429ab3c15103ae9009614f1f3725ae5cbad4733ca582901965b1`  
		Last Modified: Tue, 30 Sep 2025 00:16:33 GMT  
		Size: 90.2 KB (90174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1daee8250ea7ba96eac71bc0e2a8bbd64222f6a94bb432c8cd8623a6760f3002`  
		Last Modified: Tue, 30 Sep 2025 00:16:33 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:52e009a03c07d287b8712a89275cf62d910e6f735fb37cc5e7bab8beef1bbe66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3629346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34a745821a65d66b1aa0f33a69d19c1824d420dbebf69bdce4aa51155bb295fc`

```dockerfile
```

-	Layers:
	-	`sha256:458676c72d3376b2e2adc40b027530e16649d7cef3dce4f466fa9eafc5e2602b`  
		Last Modified: Tue, 30 Sep 2025 22:08:44 GMT  
		Size: 3.6 MB (3613021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d73401dfdc2638617c66e6f3c897b4abcb9fd9d44e04be80396ce82befadec0`  
		Last Modified: Tue, 30 Sep 2025 22:08:45 GMT  
		Size: 16.3 KB (16325 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:bb8a1f91ca3dda2b54c613358a3f2f2945bfc5deaafc4eeadb6eae89d044f6c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59815896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8008367a8e867e3902e67f9754a14d41e1c86f389a5a7ecb27933aff25207f1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:28aec8b14b3eeacbf47ef38af72fab694b109fdcdf31581722750599baf1a932`  
		Last Modified: Mon, 29 Sep 2025 23:35:17 GMT  
		Size: 49.6 MB (49648695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f827ec068a53d186059453e246d57e837a733af80e5e8a439634aaa8010cbc48`  
		Last Modified: Tue, 30 Sep 2025 00:19:31 GMT  
		Size: 10.1 MB (10073018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f2c0c542f12345a7b0b7332a3c30fbef3e0f06cb41dab53840a4e12b39a669`  
		Last Modified: Tue, 30 Sep 2025 00:19:30 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb99ddf347a9b9633f0d8033fe5a42e37880b4b2ddaf4bda2922f2c4bc504a8`  
		Last Modified: Tue, 30 Sep 2025 00:19:30 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7514b6a6ce06d47e1c9a211e6c9baac0edbdef4aa535d618f6415f0fbe994a`  
		Last Modified: Tue, 30 Sep 2025 00:19:31 GMT  
		Size: 90.8 KB (90837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73a6f3450e33d6d3354fde8b80a122a9643f6244d174f78222de5bd8feb1a930`  
		Last Modified: Tue, 30 Sep 2025 00:19:30 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f0d1fa2842c899d239f59156bb06dcb2aa6b4017485f5d1418867ab3b772ea22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3631025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfc74683096734fe8a7282c0c86a4b90695de4208566bde26b768822394849ba`

```dockerfile
```

-	Layers:
	-	`sha256:8358e4867b6f7d30ccde76e14fd6bc289cb71cee56a711c57179f8b40eda4b1c`  
		Last Modified: Wed, 01 Oct 2025 13:08:20 GMT  
		Size: 3.6 MB (3614548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7daca65ee14aa6ed1264b3293452c903db18d8777d168fdec82a6219fa454ed`  
		Last Modified: Wed, 01 Oct 2025 13:08:20 GMT  
		Size: 16.5 KB (16477 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:6f5f51db0117943740d24d6272ede6d385cf0de736a0a87db476f1cd373ac423
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61356742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28287d3132e454889d0cb4278309fdd1c117e4946ce49dd56a41083c2539181e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:f1c1f592b5569b5e2093c3107a48f2929b609f05af6d24c06d41a7ec1ae5e0e1`  
		Last Modified: Mon, 29 Sep 2025 23:35:36 GMT  
		Size: 50.8 MB (50800229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b43fce213f96af9285577072bd9752768a9c65a727ec564297271c4fb3dd675`  
		Last Modified: Tue, 30 Sep 2025 00:23:18 GMT  
		Size: 10.5 MB (10462626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e2e09d36685cd8530477135a922a156ccc8bfdf81e79a088f5c4b6bae27c7a`  
		Last Modified: Tue, 30 Sep 2025 00:23:13 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77747ec32ef9084e7a31f53e4895625940080c905fe34a4b4a1518a05da0be5c`  
		Last Modified: Tue, 30 Sep 2025 00:23:12 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afe8cd32135ae5186a68422d3154e344abce87331d1c80a54f49c008cafa3754`  
		Last Modified: Tue, 30 Sep 2025 00:23:13 GMT  
		Size: 90.5 KB (90540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6ade42626c18876d4e066d0491d60ce433a6f3f35060ac999555d4904dbba5`  
		Last Modified: Tue, 30 Sep 2025 00:23:13 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2e53fda5ed32d4582af0d59a52f6053c693f45de5a8593022784d862534f1272
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3627260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cff141d466be7fd3841ab7f3fdd7191cb53a6b2c3df26fa213fd731f4e39ea16`

```dockerfile
```

-	Layers:
	-	`sha256:fac33ea0fa1e517ae03eda600bab1c7ec5b8189b09fe01c651a4f7d35b69e1cd`  
		Last Modified: Tue, 30 Sep 2025 16:08:40 GMT  
		Size: 3.6 MB (3610970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39422b45dea80b7340f8112c3c76282ecdcfd55ec0cbdbbdbf5570d78a2d4128`  
		Last Modified: Tue, 30 Sep 2025 16:08:41 GMT  
		Size: 16.3 KB (16290 bytes)  
		MIME: application/vnd.in-toto+json
