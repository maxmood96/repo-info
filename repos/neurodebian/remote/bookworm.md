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
